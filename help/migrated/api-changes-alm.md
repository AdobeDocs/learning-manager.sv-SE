---
description: API-ändringar i ALM
jcr-language: en_us
title: API-ändringar i aprilversionen
source-git-commit: 3b35c16d74c83329cee24ee9ad007a53ccbd8cf3
workflow-type: tm+mt
source-wordcount: '4093'
ht-degree: 0%

---


# API-ändringar i aprilversionen 2026

I aprilversionen 2026 av Adobe Learning Manager introduceras fokuserade förbättringar av det offentliga API:t kring alternativ och motsvarigheter, tidsbegränsad åtkomst till innehåll, innehållsdrivna frågeformulärsförsök, icke-inloggade upplevelser och arbetsstödshantering. Ändringarna är utformade för att i stor utsträckning vara bakåtkompatibla samtidigt som de möjliggör mer exakta integreringar.

## Adaptiv utbildning för utbildningsvägar

Den här versionen innehåller komplett stöd för offentligt API för anpassningsbara utbildningsvägar. Utbildningsvägar (LP) kan nu definiera anpassningsbara regler som styr vilka avsnitt och underutbildningsobjekt (sub-LO:er) som är synliga för olika elevgrupper, och det offentliga API:t återspeglar detta beteende.

Följande slutpunkter påverkas:

- GET /primeapi/v2/learningObjects?filter.loTypes=learningPath
- GET /primeapi/v2/learningObjects/{loId}

Ett nytt booleskt attribut, attributes.isAdaptive, indikerar att ett utbildningsprogram använder adaptiva regler. När flaggan är true tolkas section-attributet adaptivt.

För elevanrop returneras bara avsnitt som är synliga för den aktuella eleven. Varje avsnitt innehåller en lista över utbildningsobjekt-ID:n (loID:n), en obligatorisk flagga och ett obligatorisktLOCcount som beräknas baserat på den adaptiva konfigurationen för den eleven samt ett sectionId. Relationen relations.subLOs filtreras nu också, så den innehåller endast de underutbildningsobjekt som är synliga för den eleven.

För administratörsanrop kan avsnitt dessutom visa en adaptiveConfig-matris. Detta beskriver de adaptiva reglerna per användargrupp, inklusive userGroupId, userGroupName och huruvida avsnittet är obligatoriskt för den gruppen. Administratörsinriktade verktyg kan använda det för att visualisera och hantera anpassningsbara regler.

Återställ slutförande för utbildningsprogram

Versionen introducerar ett API för att __uppdatera (återställa) slutförande__ för utbildningsobjekt, inklusive adaptiva utbildningsprogram. Detta stöder scenarier som omskolning, periodiska uppdateringar av regelefterlevnad eller programomstarter.

En ny slutpunkt är tillgänglig:

```
POST /primeapi/v2/learningObjects/{loId}/instances/{loInstanceId}/refreshCompletion
```

Den här åtgärden kräver lämpliga skrivbehörigheter och återställer slutförandeläget för den angivna instansen av utbildningsobjekt i den angivna användarkontexten. Det är avsett att användas i automatiseringar på administratörssidan eller av elevverktyg med noggrann omfattning.

En gruppversion av den här funktionen planeras via ett jobb-API. Formen för begäran är utformad för att nå användare via e-post, användar-ID eller användargrupp-ID, till exempel:

```
{  
  "emails": ["[user1@example.com](mailto:user1@example.com)", "[user2@example.com](mailto:user2@example.com)"],  
  "userIds": ["12345", "67890"],  
  "userGroupIds": ["ug1", "ug2"]  
}  
```

Integreringar bör använda detta API när de behöver starta om elever i varje program eller kurs. Klienter måste hantera felsvar på ett smidigt sätt: API:t kan avvisa uppdateringsbegäranden där en återställning inte är tillämplig (t.ex. när inget slutförande finns eller utbildningsobjekttyper som inte stöds).

## Motsvarigheter och alternativa kompletteringar

För att stödja implementeringar där flera utbildningsobjekt kan uppfylla samma krav introducerar versionen ekvivalenter och alternativa slutföranden som offentliga API:er.

Slutpunkterna för utbildningsobjektet innehåller nu denna information:

```
- GET /primeapi/v2/learningObjects
- GET /primeapi/v2/learningObjects/{loId}
```

Ett nytt booleskt attribut, attributes.isAlternateComplete, indikerar om elevens slutförande för ett givet utbildningsobjekt är resultatet av ett alternativt eller likvärdigt utbildningsobjekt i stället för själva objektet. När detta är sant visar relationen relations.alternateCompletions de utbildningsobjekt som fungerade som alternativ. Detta gör det möjligt för efterföljande rapporter och instrumentpaneler att skilja mellan direkta och alternativa slutföranden och att visa vilket alternativ som uppfyllde kravet.

Dessutom möjliggör en vy med relaterade utbildningsobjekt identifiering av potentiella alternativ som kan tillfredsställa ett utbildningsobjekt. Detta visas via:

```
GET /primeapi/v2/learningObjects/{loId}/relatedLOs?type=sourceAlternateLOs&limit={n}
```

Svaret returnerar utbildningsobjekt som kan fungera som alternativ och innehåller ett meta.count-fält som anger det totala antalet sådana alternativ, oberoende av den aktuella gränsen. Integreringar kan använda detta för att visa rekommenderade motsvarigheter eller för att skapa administrativa vyer av alternativa mappningar.

## Användningsfall för rapportering och analys

Användare som genererar rapporter eller analyser bör uppdatera sin logik för att lägga till isAlternateComplete och alternateCompletions i sina rapporteringsarbetsflöden.

Rapporteringsintegreringar som förbrukar slutförandedata (till exempel LT-export, anpassade datalagerfeeds eller BI-instrumentpaneler) bör utöka sin logik för att läsa och behålla båda attributen.isAlternateComplete och relations.alternateCompletions från LO API:erna:

- När isAlternateComplete == false:\
  Behandla posten som ett __direkt slutförande__ av LO, som i dag.
- När isAlternateComplete == true:
   - Flagga posten som en __alternativ slutförandemetod__ i rapporten (t.ex. en kolumn av typen &quot;Slutförandemetod&quot; med värdena DIRECT jämfört med ALTERNATE).
   - Använd relationship.alternateCompletions.data[*].id för att registrera __vilka LO:er__ som beviljade denna slutföring (till exempel &quot;Kurs B slutförd via alternativ kurs A&quot;).

Typiska användningsfall:

- _Efterlevnadsrapporter_ - visar att en efterlevnadskurs har slutförts via en godkänd motsvarighet och listar källkursen som uppfyllde kravet.
- _Instrumentpaneler för förlopp i programmet_ - skilja elever som har slutfört en bana _direkt_ från de som har slutfört den via alternativa metoder för mer exakta förlopps- och reparationsvyer.
- _Granskningsspår_ - för alla LO-märkta isAlternateComplete=true kan granskare se exakt vilka alternativa utbildningar som användes för att bevilja slutförandet.

Utan att inkludera dessa två fält kommer nedströmsrapporter att behandla alternativa slutföranden som vanliga slutföranden och kommer _inte att kunna förklara_ *varför* en elev visar sig ha slutfört en utbildning som hen aldrig slutfört direkt.

## Elevers beteende jämfört med Admin LO API

Den flerspråkiga arbetsstödsstrukturen är identisk i både elev- och administratörs LO API:er. Elevomfattning returnerar bara de arbetsstöd som är synliga för eleven, men för varje synligt arbetsstöd visar den alla konfigurerade språkinställningar via flera resursenheter (en per språkinställning) och flera lokaliserade metadata. Administratörsomfånget returnerar alla jobbinslag som administratören kan hantera, med samma LO-modell och språkspecifika resurs-ID. Kunder med elevomfattning bör välja den resurs vars attribut.språkområde bäst matchar elevens innehållsspråk, medan administratörsverktyg kan räkna upp alla språk för rapportering och hantering.

## Checklista med kommentarsfunktion

För att stödja arbetsflöden där granskare kan dela strukturerad feedback om checklistebaserade aktiviteter tar den här versionen fram *checklista med kommentarer* och granskarens synlighetskontroller via resurs-API:et för utbildningsobjekt.

Checklisterrelaterade metadata visas på enheter learningObjectResource (JApiLOResource, &quot;type&quot;: &quot;learningObjectResource&quot;) som representerar checklisteresurser inom en kurs eller annat utbildningsobjekt.

Informationen är tillgänglig via:

```
GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources
```

När utbildningsobjektinstansen innehåller resurser av checklisttyp visar motsvarande learningObjectResource-poster i den inkluderade arrayen kommentars- och granskarsynlighetsattribut under attribut och granskaridentitet under relationer.

### Nya kommentarsattribut för checklista

För checklistresurser kan följande attribut finnas i learningObjectResource:

- attributes.checklistComment\
  En fritextkommentar som lämnas av granskaren för eleven, till exempel:\
  &quot;checklistComment&quot;: &quot;Utmärkt prestanda! Alla säkerhetsprotokoll följdes korrekt.&quot;\
  Det här attributet fylls i _endast om_:
   - showChecklistComment är true, och
   - konfigurationen av checklistan har enable_reviewer_comments aktiverat.
- attributes.showChecklistComment\
  En boolesk flagga som anger om granskarens kommentarer ska visas för eleven:\
  &quot;showChecklistComment&quot;: true\
  Det här attributet finns _bara när_ enable_reviewer_comments är aktiverat i konfigurationen av checklistan.\
  Klienter bör använda den här flaggan för att avgöra om checklista ska återges eller inte i elevupplevelser.
- attributes.showReviewerNameToLearner\
  En boolesk flagga som styr om eleven ska se granskarens identitet:\
  &quot;showReviewerNameToLearner&quot;: true\
  När värdet är true kan klienter använda relationen checklistReviewedBy (se nedan) för att lösa och visa granskarens namn (t.ex. via ett API för användarsökning).

Annan checklistspecifik kontext, som checklistEvaluationStatus, isChecklistMandatory, resourceSubType: &quot;CHECKLIST&quot; och submissionDate finns också tillgängliga på samma learningObjectResource för att stödja mer omfattande checklista för användargränssnitt och rapportering.

### Granskarens identitetsrelation

När granskarens namn ska vara synliga innehåller learningObjectResource en relation som pekar på granskarens användare:

```
"relationships": {
  "checklistReviewedBy": {
    "data": {
      "id": "user_id",
      "type": "user"
    }
  }
}
```

Den här relationen fylls i _bara om_:

- showReviewerNameToLearner är true och
- checklistaReviewby är inte null (dvs. checklistan har granskats).

Klientprogram bör:

1. Kontrollera attributes.showReviewerNameToLearner.
2. Om true och relations.checklistReviewby.data finns anropar du lämpligt användar-API för att matcha &quot;id&quot;: &quot;user_id&quot; till ett visningsnamn.
3. Rendera granskarens namn bredvid checklistan, kommentaren eller statusen efter behov.

### Åtkomst till resurser och kommentarer för checklistor

För att hämta checklisteresurser och deras kommentarer för ett visst utbildningsobjekt ska klienterna:

- Samtal

```
GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources
```

- I svaret:
   - Använd relations.instance från huvudobjektet learningObject för att hitta relevanta learningObjectInstance-poster i.
   - Från varje learningObjectInstance följer du relations.loResources för att hitta learningObjectResource-poster.
   - Filtrera learningObjectResource-poster där:
      - attributes.resourceSubType == &quot;CHECKLIST&quot; (för checklisteresurser) och
      - valfritt attributes.showChecklistComment == true för att hitta checklistor med elevsynliga kommentarer.

- För varje checklista learningObjectResource förbrukar du:
   - attributes.checklistComment (om det finns ett sådant och showChecklistComment är sant)
   - attributes.checklistEvaluationStatus (t.ex. &quot;GODKÄND&quot;)
   - attributes.showReviewerNameToLearner
   - relations.checklistReviewby (om närvarande) för att identifiera granskaren.

Det här mönstret gör att fjärradministrerade eller anpassade klienter kan återge en omfattande checklista, inklusive status, obligatoriska/valfria flaggor och granskarens feedback, direkt från Prime API:er.

### Överväganden gällande rapportering och användarupplevelser

- _Rapportering och analys_
Integreringar som spårar elevers resultat på checklistor kan innehålla:
   - checklistaEvaluationStatus för godkännande/underkännande eller andra statusindikatorer.
   - isChecklistaObligatorisk att skilja mellan obligatoriska och valfria checklisteaktiviteter.
   - Närvaro eller frånvaro av checklistaKommentera och visaChecklistaKommentar för revisioner av feedbackens täckning.
- _Elevupplevelser_
Gränssnittsimplementeringar bör:
   - Respektera showChecklistComment innan kommentarer visas.
   - Använd showReviewerNameToLearner och checklistReviewedBy för att bestämma om granskarens namn ska visas eller om granskningen ska förbli anonym.
   - Återgå smidigt när kommentarer har inaktiverats eller inte finns kvar, fortfarande med utvärderingsstatus och inlämningsinformation.

## Flerspråkigt stöd för arbetsstöd

För att stödja implementeringar där arbetsstöd måste levereras på flera språk till både elever och administratörer, utökar den här versionen hanteringen av arbetsstöd så att *en resurs per plats* returneras i stället för en enda hårdkodad en-US-resurs.

Flerspråkiga arbetsstöd fortsätter att använda den befintliga hierarkin:

_utbildningsobjekt_ (lo) → _learningObjectResource_ (loResource) → _resurs_

Inga ändringar krävs i API-avtalet. Allt lokaliserat arbetsstöd passar in i den här strukturen naturligt, med separata resursenheter per språkområde och delade lokaliserade metadata på nivåerna learningObject/learningObjectResource.

Arbetsstödsdata visas via:

```
GET /primeapi/v2/learningObjects/jobAid:{jobAidId}?include=instances.loResources.resources
```

När ett arbetsstöd har flera språkvarianter innehåller den inkluderade arrayen flera &quot;type&quot;: &quot;resource&quot;-poster - en för varje språk (till exempel en-US, fr-FR, es-ES), alla länkade från en enda learningObjectResource.

### Arbetsstödsstruktur på flera språk

Flerspråkigt arbetsstöd:

- _learningObject (typ: learningObject)_
   - Innehåller localizedMetadata med flera poster (t.ex. en-US, fr-FR) så att klienter kan visa jobbstödets titel/beskrivning på lämpligt språk.
- _learningObjectInstance (typ: learningObjectInstance)_
   - Hänvisar till en eller flera learningObjectResource-poster via relations.loResources.
- _learningObjectResource (typ: learningObjectResource)_
   - Innehåller gemensam konfiguration (innehållstyp, version osv.) och lokaliserade metadata på flera språk.
   - Länkar till en eller flera resursenheter via relations.resources.
- _resurs (typ: resurs)_
   - *En per språkområde*, var och en med eget ID, eget språk, namn och egen webbadress (plats/downloadUrl).

Ett typiskt mönster för flerspråkiga arbetsstöd är:

- learningObjectResource med localizedMetadata för en-US och fr-FR
- relations.resources.data som pekar på:
   - resurs med språkinställning: &quot;en-US&quot;
   - resurs med språkinställning: &quot;fr-FR&quot;

Klienter kan välja lämplig resurs genom att matcha elevens språkinställning med fältet resource.attributes.locale.

### Nytt resurs-ID-format för arbetsstöd

Om du vill kunna skilja mellan flera lokaliserade varianter av en jobbbiståndsresurs har _resurs-ID-formatet ändrats_.

_Gammalt resurs-ID-format_

Tidigare användes ett ogenomskinligt ID-format för arbetsstödsresurser, till exempel:

arbetsstöd:131032_-1_-1_2_resource

Det här formatet kodade inte nationella inställningar, och API:er visade endast en resurs (vanligtvis en-US).

_Nytt resurs-ID-format (flerspråksanpassat)_

Det nya formatet är:

```
jobAid:<jobAidId>_<version>_<localeCode>
```

Exempel:

- arbetsstöd:131032_2_en-US
- arbetsstöd:131032_2_fr_FR
- arbetsstöd:131032_2_es_ES

Visuell nedbrytning:

```
jobAid:131032_2_fr_FR

        │      │ │ │

        │      │ │ └──► Locale Code (fr_FR, en_US, es_ES, etc.)

        │      │ └────► Version (2)

        │      └──────► JobAid ID (131032)

        └─────────────► Resource Type Prefix ("jobAid:")
```

Med den här strukturen kan klienter:

- Identifiera snabbt vilket arbetsstöd och vilken version en resurs tillhör.
- Inled språkinställningen direkt från resurs-ID:t vid behov.

### Bakåtkompatibilitet: 

```/resources/{resourceId}```

Den äldre resursslutpunkten är fortfarande tillgänglig:

```GET /primeapi/v2/resources/{resourceId}

```

Nu är den _bakåtkompatibel_ med både gamla och nya ID-format:

- _Gammalt ID-format_ (till exempel arbetsstöd:131032_-1_-1_2_resource)
   - Fortsätter att fungera.
   - Returnerar den _först skapade resursen_ som är associerad med den äldre identifieraren (vanligtvis den ursprungliga en-US-resursen).
- _Nytt ID-format_ (till exempel arbetsstöd:131032_2_fr_FR)
   - Returnerar den _exakta språkspecifika resursen_ som motsvarar detta ID.
   - Detta möjliggör exakt hämtning och manipulering av lokaliserade varianter av arbetsstöd.

Integreringar som för närvarande lagrar eller refererar till gamla resurs-ID:n kan fortsätta att fungera utan ändringar, medan nyare implementeringar uppmuntras att använda det nya ID-formatet för språkspecifika åtgärder.

### Överväganden om integrering och användarupplevelser

- _Användargränssnitt för elev/administratör_
   - Använd learningObject.localizedMetadata och learningObjectResource.localizedMetadata för att presentera titlar och beskrivningar på rätt språk.
   - Använd resource.attributes.locale för att välja rätt URL (plats / downloadUrl) för elevens språkområde.
   - Implementera återgångsbeteende (till exempel, återgå till en-US) om en elevs exakta språk inte är tillgängligt.
- _API:er och lagring_
   - Spara _resurs-ID:n i nytt format_ (```jobAid:<jobAidId>_<version>_<localeCode>```) för nya integreringar för att aktivera entydig språkspecifik hämtning.
   - Äldre ID:n kan fortfarande användas med /resources/{resourceId}, men de skiljer inte mellan olika språk.

## Tidsbegränsningar för startmoduler

Vissa utbildningsupplevelser måste endast vara tillgängliga inom ett angivet tidsintervall. Versionen visar information om tid och plats för utbildningsobjekt och introducerar en valideringsslutpunkt som kontrollerar om en elev kan starta en resurs vid den aktuella tidpunkten.

Metadata för tid/plats är tillgängliga via slutpunkten:

```GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources```

På utbildningsobjektets resursnivå kan ett timeSlot-objekt nu finnas i attributen, med startTime- och endTime-värden i UTC. Detta anger under vilket fönster som resursen kan startas.

Innan du startar en modul kan integreringar anropa en ny valideringsslutpunkt:

```GET /primeapi/v2/learningObjects/{loId}/instances/{loInstanceId}/loResources/{loResourceId}/canStart```

Denna slutpunkt, som är avsedd för scenarier som läses av elever, returnerar huruvida eleven för närvarande får starta resursen med hänsyn till konfigurerad tid, leveranstyp och andra backend-regler.

Anpassade spelare och klientapplikationer bör använda canStart för att tvinga fram tidsbaserad åtkomst och använda timeSlot-metadata för att visa tydliga meddelanden om när innehåll blir tillgängligt eller upphör att gälla. Negativa svar från canStart bör hanteras uttryckligen för att informera elever om varför innehållet inte kan startas än eller längre.

## Innehållsdrivna frågeformulär som körs på flera försök

Vissa innehållspaket implementerar sin egen försöksspårning i stället för att enbart förlita sig på Adobe Learning Manager. Versionen introducerar en flagga som indikerar när försök görs av själva innehållet.

Genom:

```GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources```

Utbildningsobjektresurser kan nu visa ett booleskt attribut med attributet hasContentDrivenAttemptTracking. När detta är sant hanterar frågesporten eller modulen försök internt (till exempel via SCORM eller xAPI-logik), och plattformens standardräknare för försök kanske inte helt återspeglar elevens upplevelse.

Integreringar som visar antalet försök eller styr återförsöksbeteendet bör kontrollera den här flaggan. När det är aktiverat ska de inte sluta sig till försöksgränser enbart från plattformsmetadata och ska vara beredda att förlita sig på rapportering på innehållssidan (till exempel via xAPI-satser) eller företagsspecifika regler.

## Beteendeförändring i ID-format för arbetsstödsresurs

Den här versionen introducerar en viktig __beteendeförändring__ i formatet för resurs-ID:n för arbetsstöd. Även om det inte finns någon ny slutpunkt har det en direkt inverkan på system som lagrar eller parsar dessa ID:n.

Tidigare använde resurs-ID:n för arbetsstöd ett format som:

```jobAid:<jobAidId>_-1_-1_2_resource```

I aprilversionen 2026 ska detta ersättas med ett förenklat och mer explicit format:

```jobAid:<jobAidId>_<version>_<localeCode>```

Till exempel:

arbetsstöd:131032_2_fr_FR

Komponenterna är:

- ```<jobAidId>```: det numeriska ID:t för arbetsstöd (till exempel 131032),
- ```<version>```: versionsnumret för arbetsstödet (till exempel 2),
- ```<localeCode>```: språkkoden (t.ex. en_US, fr_FR, es_ES).

Alla integreringar som indexerar resurser eller finns kvar i resurs-ID:n för arbetsstöd måste uppdatera sin parsnings- och lagringslogik så att det nya formatet känns igen. Eftersom identifierarna i sig ändras rekommenderar vi starkt att du återskapar alla lokala index som är transparenta med resurs-ID:n för arbetsstöd efter uppgradering till versionen från april 2026.

## Ställ in kursbannerbilder via migrering

Du kan nu ställa in eller uppdatera kursbannerbilder i Adobe Learning Manager som en del av ditt standardarbetsflöde för migrering. Det hjälper dig att starta eller rensa stora kataloger samtidigt som kurssidorna hålls visuellt konsekventa, utan manuell redigering

### Där banderollbilder definieras

Banderollbilder konfigureras i migreringsfilen _course.csv_, som du redan använder för att tillhandahålla kursmetadata, till exempel:

- id
- CourseName
- CourseCreationDate
- tillstånd
- författare
- thumbnailUrl

Med den här förbättringen innehåller specifikationen course.csv ytterligare en _valfri kolumn_ för kursbannerbilden. Det exakta rubriknamnet definieras i CSV-specifikationen som du hämtar från ditt Learning Manager-konto (den kan till exempel visas som bannerUrl eller bannerImageUrl).

Banderollkolumnen:

- Pekar på den bildfil som du vill använda som _kursbanner_.
- Fungerar på samma sätt som ThumbnailUrl när du använder bilder som finns i din konfigurerade innehållslagring (Box/FTP).

### Förbereda banderollbilder för migrering

1. Överför bannerbilder: Placera dina bannerbildfiler i samma Box- eller FTP-plats som du använder för andra migreringsresurser, enligt den befintliga katalogstrukturen.
2. Kontrollera filformat:
Använd ett av de bildformat som stöds (till exempel png, jpg, jpeg, gif) enligt beskrivningen i systemkraven:
   1. [*Systemkrav*](/help/migrated/system-requirements.md)
3. Uppdatera course.csv: Referera till banderollbildens relativa sökväg eller identifierare i kolumnen Ny banderoll. Ett konceptuellt exempel:

```
id,courseName,courseCreationDate,state,author,thumbnailUrl,bannerUrl  
12345,DEMO1,2018-05-05T08:56:21.000Z,Published,Sudheer,pic1.png,banners/banner1.png  
45678,DEMO2,2018-05-05T08:56:21.000Z,Published,Sudheer,pic2.png,banners/banner2.png  
```

### Använda banderoller under en migreringskörning

När course.csv har uppdaterats är flödet detsamma som all annan migrering:

1. _Överför CSV-filer_
Överför den uppdaterade Course.csv (och andra relevanta filer) till Box/FTP-mappen som är konfigurerad för migrering. Filnamn måste matcha de namn som anges i csv_fications.zip exakt (de är skiftlägeskänsliga).
2. _Starta en sprintkörning_
Starta en migreringskörning på _spurt_ i Adobe Learning Manager som integrationsadministratör, som inkluderar course.csv.\
   Migreringsmotorn läser banderollkolumnen och använder banderollbilden på varje kurs.
3. _Granska resultat och felloggar_
Efter sprinten:
   1. Verifiera banderoller i apparna _Författare_ och _Elev_.
   2. Om vissa rader misslyckas (till exempel på grund av en ogiltig filsökväg eller ett format som inte stöds) hämtar du CSV-filen med felet från migreringskörningen och korrigerar data.

### Nya kurser jämfört med befintliga kurser

Banderollfältet fungerar i båda scenarierna:

- _Nya kurser har skapats via migrering_
När en kurs skapas för första gången från course.csv och banderollkolumnen är ifylld ställs den banderollen in omedelbart.
- _Befintliga kurser (eftermontering/korrigeringar)_
Om du kör migreringen igen med samma kurs-ID och ett nytt banderollvärde:
   - Learning Manager hittar den befintliga kursen.
   - Banderollbilden är _uppdaterad_ till den nya bild som anges i CSV-filen.

De faktiska kolumnnamnen och sökvägarna måste matcha den _hämtade CSV-specifikationen_ och innehållslagringslayouten.

## Ta bort orderkolumn i LearningProgramCourse

Adobe Learning Manager har nu stöd för en förenklad modell för _kursbeställning inuti utbildningsvägar (utbildningsprogram)_ under migrering. Som en del av den här ändringen tas kolumnen _order bort_ från migreringsfilen learning_program_course.csv.

Tidigare innehöll filen learning_program_course.csv en kolumn (kallas ofta för order eller liknande) som användes för att:

- Ange uttryckligen _positionen_ för varje kurs i ett utbildningsprogram, baserat på det numeriska värdet i den kolumnen.
- Kräv att administratörer eller skript underhåller den här numeriska sekvensen manuellt, särskilt när kurser infogas eller ordnas om.

Nu använder Adobe Learning Manager inte längre orderkolumnen i learning_program_course.csv för att avgöra kursordningen. Migreringens CSV-fil fokuserar i stället på _vilka kurser som tillhör vilket utbildningsprogram_, snarare än hur de ordnas numeriskt.

## Inverkan på CSV-filer för migrering

### learning_program_course.csv

Du bör behandla den äldre kolumnen för ordningsföljd som borttagen eller ignorerad:

- Förlita dig inte på order för att kontrollera kurssekvensen i ett utbildningsprogram under migrering.
- Om du fortfarande har en orderkolumn från äldre mallar:
   - Learning Manager ignorerar det för beställning.
   - Du kan ta bort det säkert från CSV-filen med tiden för att förenkla migreringsfilerna.
- Den centrala mappningen som krävs kvarstår:
   - Utbildningsprogram-id ↔ kurs-id (och alla andra fortfarande dokumenterade kolumner som id, learningProgramId, courseId och datum).

Använd alltid de senaste [_CSV-specifikationerna_](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/migration-manual) från ditt Learning Manager-konto (via csv_fications.zip) för att bekräfta den aktuella rubrikuppsättningen och kraven.

## timeZoneCode i kursinstanser

Från och med den här versionen visar kursinstansmodellen (learningObjectInstance) ett nytt attribut:

timeZoneCode - ett strängfält som uttryckligen länkar en kursinstans till en av kontots konfigurerade tidszoner.

Detta gör att klienter kan:

- Lös tidszonen för en kursinstans på ett konsekvent, API-drivet sätt.
- Tolka och visa alla datum/tider på förekomstnivå korrekt för den förekomsten, oavsett användarens egen tidszon.

### Där timeZoneCode visas

Fältet läggs till i attributen för modellen learningObjectInstance
endast för kursinstanser.

Exempel:

```
{
  "id": "course:1262748_1359228",
  "type": "learningObjectInstance",
  "attributes": {
    "dateCreated": "2019-08-06T13:50:39.000Z",
    "isAET": false,
    "isDefault": true,
    "timeZoneCode": "356",
    "isFlexible": false,
    "state": "Active",
    "localizedMetadata": [
      {
        "locale": "en-US",
        "name": "Default instance"
      }
    ]
  }
}
```

### Så löser du timeZoneCode

Den numeriska timeZoneCode är en uppslagsnyckel i kontots tidszonskatalog, som visas via konto-API:et:

```http
GET /primeapi/v2/account
Authorization: Bearer <access_token>
```

I svaret anges tidszonerna i:

```
"data": {
  "attributes": {
    "timeZones": [
      {
        "name": "Etc/GMT+12",
        "timeZoneCode": "356",
        "utcOffset": -720,
        "utcOffsetCode": "UTC-12:00(Etc/GMT+12)",
        "zoneId": "Etc/GMT+12"
      },
      "..."
    ]
  }
}
```

### Rekommenderat klientflöde:

1. Anropa GET/konto en gång, cacheattribut.timeZones för klienten.
2. För varje kursinstans:
   - Läs attributes.timeZoneCode.
   - Hitta motsvarande post i tidszoner där timeZoneCode matchar.
   - Använd den postens zoneId, utcOffset och utcOffsetCode för visning och schemaläggningslogik.

## Asynkrona offentliga API:er för medlemskap i användargrupper

### Introduktion

Adobe Learning Manager visar två _asynkrona API:er för administratörer_ för att hantera medlemskap i användargrupper (UG):

- POST /async/userGroups/{userGroupId}/users - lägg till användare i en användargrupp asynkront
- DELETE /async/userGroups/{userGroupId}/users - ta bort användare asynkront från en användargrupp

I stället för att uppdatera medlemskapet i samma begäran accepterar dessa API:er din batch och returnerar ett _händelse-ID_. Det faktiska resultatet levereras senare via webhooks.

Använd dem när

- Du hanterar stora grupper eller frekventa batchuppdateringar.
- Latens är mindre viktigt än tillförlitlighet och genomströmning.
- Du skapar integreringar (HR, CRM, LXP) i stället för UI-klick.

För små, interaktiva administratörsåtgärder kan du fortsätta använda de synkrona `/userGroups/{id}/users` API:erna.

### Autentisering och bas-URL

Dessa API:er ingår i standardytan för __v2 Admin API__.

- [URL (prod) för bas](https://learningmanager.adobe.com/docs/primeapi/v2/)
- Autentisering: OAuth 2.0-åtkomsttoken med `admin:write`-omfång
- Obligatoriska sidhuvuden:
   - Auktorisering: Bearer &lt;åtkomsttoken>
   - Innehållstyp: application/json
   - Acceptera: application/json

Allmänt beteende och omfattning i Admin API finns i:

- [Användarhandbok för utvecklare](/help/migrated/integration-admin/feature-summary/developer-manual.md)
- [API-referenshandbok](https://learningmanager.adobe.com/docs/primeapi/v2/)

### Format för begäran

Både __lägg till__ och __ta bort__ använder exakt samma kroppsform.

#### Text

```
{
  "metadata": {
    "event_id": "my-optional-correlation-id",
    "sourceSystem": "HRIS",
    "batchId": "hr_2026_03_30_0001"
  },
  "data": [
    { "type": "user", "id": "11101219" },
    { "type": "user", "id": "11101220" }
  ]
}
```

#### data (obligatoriskt)

data är listan över användarresursidentifierare för den här batchen.

- `type` måste vara &quot;user&quot;.
- `id` är _numeriskt användar-ID_ i ALM (inte e-post, inte UUID).

#### Begränsningar

- `data` måste finnas och inte vara tom.
- Minst en användare krävs.
- Den maximala nyttolaststorleken är 20 användare per begäran.
- Alla id måste vara numeriska och hänvisa till giltiga användare.

Om något av dessa villkor misslyckas returnerar API ett fel och inget står i kö.

#### metadata (valfritt)

`metadata` är ytterligare korrelationsdata som du vill ska upprepas i webhooken.

Normal användning:

- `event_id` - korrelations-ID du genererar.
- `sourceSystem` - namnet på det överordnade systemet.
- `batchId` - batch- eller jobbidentifierare.

Tjänsten returnerar det här objektet oförändrat i webhook-svaret, så du kan matcha återanropet med ditt interna jobb.

Begränsningar:

- Valfritt - kan utelämnas helt.
- Den kombinerade längden på alla nycklar och värden får inte överstiga 1 000 tecken.

### Svarsformat

Båda slutpunkterna svarar synkront med ett händelse-ID:

```
{ "event_id": "cd2972c8-cb15-47a0-a23f-e4a16cb720f5" }
```

Beteende:

- Om `metadata.event_id` skickas används det värdet.
- Annars genererar tjänsten ett UUID.

Du bör alltid:

- Lagra denna `event_id` som primär identifierare för batchen.
- Förvänta dig att få samma värde i webhook-återanropet.

Visa [Webhookar för att lägga till och ta bort användargruppsmedlemskap](/help/migrated/integration-admin/feature-summary/webhooks.md#webhooks-for-adding-and-removing-user-group-membership) om du vill ha mer information.

## Vanliga frågor

_Hur ändrar aprilversionen 2026 learningObjects API för adaptiva utbildningsprogram?_

Denna version lägger till en isAdaptive-flagga på utbildningsprogram och gör avsnitt och subLO:er elevmedvetna. I adaptiva program ser eleverna bara de avsnitt och underutbildningsobjekt som är synliga för dem baserat på adaptiva regler, medan administratörer kan se den underliggande adaptiva konfigurationen för en användargrupp.

_Behöver jag uppdatera integreringen om den förutsätter att alla avsnitt och underordnade LO:er alltid returneras?_

Ja. För adaptiva utbildningsprogram returnerar API nu bara de avsnitt och sub-LO:er som är synliga för den aktuella eleven. Klientkoden bör behandla svaret som den auktoritativa, eventuellt filtrerade vyn i stället för att anta en fullständig lista.

_Hur kan jag programmässigt återställa en elevs slutförande för en kurs eller ett utbildningsprogram?_

Använd den nya slutpunkten:

```POST /primeapi/v2/learningObjects/{loId}/instances/{loInstanceId}/refreshCompletion```
Detta återställer slutförandet för målinstansen när behörigheter och tillstånd tillåter det.

_Hur vet jag om en elev har slutfört något via ett alternativt eller motsvarande utbildningsobjekt?_

Kontrollera attributet isAlternateComplete på utbildningsobjektet. Om det är sant visar relationen alternateCompletions de utbildningsobjekt som fungerade som alternativ för den elevens slutförande.

_Hur hittar jag alla alternativ som kan uppfylla ett visst utbildningsobjekt?_

Använd följande slutpunkt:

```GET /primeapi/v2/learningObjects/{loId}/relatedLOs?type=sourceAlternateLOs&limit={n}```

och använd datamatrisen (för alternativen) och meta.count (för det totala antalet alternativ).

_Hur vet jag om en elev får starta en modul just nu?_

Först hämtar du resursens timeSlot från:

```GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources```
och använd sedan

```GET /primeapi/v2/learningObjects/{loId}/instances/{loInstanceId}/loResources/{loResourceId}/canStart```

_Vad innebär ContentDrivenAttemptTracking för en resurs?_

Det indikerar att försöksspårning styrs av själva innehållet (till exempel via SCORM/xAPI-logik) snarare än bara av plattformsräknare. När det är sant ska du inte bara förlita dig på antalet plattformsförsök eller begränsningar för din användarupplevelse och rapportering.

_Hur hittar jag menyer som är lämpliga för användare som inte är inloggade (offentliga upplevelser)?_

Användning:

```GET /primeapi/v2/templates/menus?include=pages,subMenus.pages&isNonLoggedIn=true```

Detta returnerar meny- och sidstrukturer som filtrerats för anonyma användare, och som lämpar sig för Experience Builder eller andra huvudlösa webbplatser.

_Vad har ändrats i jobbstödsfiltreringen med effectiveModifiedDate?_

Begäranden som kombinerar filter.effectiveModifiedDate med filter.loTypes=jobAid returnerar nu korrekt endast arbetsstöd inom det angivna datumfönstret.

_Vad har ändrats i ID-formatet för arbetsstödsresursen och hur ska jag hantera det?_

ID-formatet har ändrats från värden som:

```jobAid:<jobAidId>_-1_-1_2_resource```

till:

```jobAid:<jobAidId>_<version>_<localeCode>```

till exempel jobAid:131032_2_fr_FR. Alla system som lagrar eller parsar resurs-ID:n för arbetsstöd måste uppdateras och du bör planera för att återskapa lokala index som är transparenta med dessa ID:n efter uppgradering till versionen från april 2026.
