---
description: Läs mer om de nya funktionerna och förbättringarna i juli 2024-versionen av Adobe Learning Manager
jcr-language: en_us
title: Sammanfattning av nya funktioner
source-git-commit: 7e3b19d29b9de23ea489c5651ef0aef1d4ec3005
workflow-type: tm+mt
source-wordcount: '2156'
ht-degree: 1%

---


# Sammanfattning av nya funktioner {#new-features-summary}

Läs mer om de nya funktionerna och förbättringarna i juli 2024-versionen av Adobe Learning Manager.

## Förbättring av instrumentpanelen för efterlevnad

### Vad är en instrumentpanel för efterlevnad? {#whatiscompliancedashboard}

Med **[!UICONTROL Compliance Dashboard]** Adobe **Learning Manager** kan chefer övervaka och övervaka elevernas framsteg mot sina utbildningsmål. De kan kontrollera om teammedlemmarna håller deadlines och hänger med i sin inlärningsprocess, vilket hjälper till att säkerställa efterlevnad. Administratören kan konfigurera instrumentpanelen för efterlevnad och dela med cheferna.

Om du vill komma åt instrumentpanelen för efterlevnad i Admin-appen väljer du **[!UICONTROL Reports]** > **[!UICONTROL Learning Summary]** > **[!UICONTROL Compliance Dashboard]**.

### Vad ändras i versionen?

Med den förbättrade instrumentpanelen för efterlevnad kan administratörer och chefer visa kurser, utbildningsvägar eller certifieringar av efterlevnadstyp som är relaterade till deras specifika kategori (till exempel försäljning, marknadsföring och juridik). Administratörer kan kategorisera anpassade efterlevnadskurser i specifika kategorier. Anpassade efterlevnadskategorier drivs av katalogetiketter.  Administratörer kan skapa en kursinstrumentpanel och dela den med chefer. Chefer kan sedan visa samma instrumentpanel på sina respektive instanser. Förbättringar har också gjorts i användargränssnittet för instrumentpanelen för efterlevnad och e-postmeddelanden om efterlevnad.![](assets/compliance-dashboard-admin.png)

#### Arbetsflöde

Här är stegen för att använda den förbättrade instrumentpanelen för efterlevnad:

| Roll | Uppgift | Ytterligare information |
|---|---|---|
| Admin | Skapa anpassade efterlevnadsetiketter | Mer information finns i den här artikeln[: Skapa anpassade efterlevnadsetiketter](/help/migrated/administrators/feature-summary/reports.md#compliance-dashboard) |
| Författare | Lägg till dessa etiketter i kursen | Mer information finns i den här artikeln [Lägga till efterlevnadsetiketter i en kurs/utbildningsväg/certifiering](/help/migrated/authors/feature-summary/courses.md#add-compliance-labels-to-courselearning-pathcertification) . |
| Admin | Skapa instrumentpanelen med efterlevnadskursen och dela den med chefer | Mer information finns i den här artikeln [: Skapa och dela en instrumentpanel](/help/migrated/administrators/feature-summary/reports.md#create-and-share-a-compliance-dashboard) för efterlevnad. |
| Chef | Visa instrumentpanelen för efterlevnad | Mer information finns i den här artikeln [Efterlevnadsstatus](/help/migrated/managers/feature-summary/manager-dashboard.md#compliance-status) |

## Förnyelse av användargränssnittet för elever

>[!IMPORTANT]
>
>Det nya användargränssnittet för elever kommer att släppas i faser.

Learner **UI** har uppdaterats med en mer elegant och modern design. Sidorna **[!UICONTROL Learner Home]**, **[!UICONTROL My Learning]**, **[!UICONTROL Catalog]** och **[!UICONTROL Course Overview]** landningssidorna får ett nytt och modernt utseende. Kurskorten har också fått en ny design för att visa detaljer på ett modernt sätt. Om du håller muspekaren över ett kurskort visas kursbeskrivning och publiceringsdatum.

>[!NOTE]
>
>Det förnyade användargränssnittet gäller endast för den integrerande layouten. Dessa ändringar stöds inte på mobilwebben eller i appen ännu och kommer att uppdateras i en framtida version.

![](assets/old-ui.png)
_Gammalt användargränssnitt_

![](assets/new-ui.png)
_Nytt användargränssnitt_

### Vad ändras i den här versionen

**Modernisera utseende och känsla**

De nya uppfräschade visuella elementen ligger i linje med moderna designtrender, vilket gör att produkten ser intuitiv och tilltalande ut. Detta inkluderar en ny toppannons, sidopanel och widgetar med modernt utseende.

**Förbättrad användarupplevelse**

Deltagarna kommer nu att se en liknande kortvy på följande sidor: Startsida, Katalog, Min inlärning och Kursöversikt som erbjuder en enhetlig upplevelse.

Se [startsidan](/help/migrated/learners/feature-summary/learner-home-page.md) för Learner för mer information.

**Ändringar av kurspubliceringsdatum**

Med den här förbättringen kommer publiceringsdatumen för LinkedIn- och Go1-kurser som importeras till Adobe Learning Manager att vara de faktiska publiceringsdatumen på LinkedIn och Go1. Du kan också se de faktiska publiceringsdatumen för LinkedIn- och Go1-kurserna i användargränssnittet. Visa [kurskort](/help/migrated/learners/feature-summary/learner-home-page.md#course-cards) för mer information.

## Uppdateringar av icke-inloggade upplevelser

Med den icke-inloggade upplevelsen kan du skapa en realtidsupplevelse för icke-inloggade kunder. Detta fungerar som en målsida för deras marknadsföringskampanjer, vilket ger tillräckligt med information för att uppmuntra till registreringar.

### Vad ändras i den här versionen

Kunder kan köpa en premiumplan för att skapa dessa mycket skalbara icke-inloggade upplevelser. Den här icke-loggade [upplevelsen, som drivs av Training Data Access](/help/migrated/integration-admin/feature-summary/connectors.md#training-data-access), ger realtidsdata om platsgränser, upptagna platser, gränser för väntelistor och antal väntelistor med hjälp av Adobe Learning Manager API:er. Kunder kan använda dessa API:er för att erbjuda icke-inloggade elever sök- och filtreringsfunktioner och en fullständig kurssammanfattning. Mer information om API:erna finns i den här artikeln [Icke-inloggade API:er](/help/migrated/integration-admin/feature-summary/non-logged-in-apis.md) .

>[!NOTE]
>
>Kontakta supportteamet eller CSAM för att köpa premiumplanen.

## Stöd för flera lagerhållningsenheter (SKU:er)

Elever kan nu lägga till flera kurser, utbildningsvägar eller certifieringar i kundvagnen och köpa dem tillsammans.

### Vad ändras i versionen?

Tidigare kunde eleverna bara köpa en kurs i taget. I den här versionen av **Adobe Learning Manager** kan de köpa flera kurser, utbildningsvägar eller certifieringar samtidigt med hjälp av kundvagnen.

Den här funktionen är endast tillgänglig i elevapparna (befintligt användargränssnitt, nytt användargränssnitt för elever och mobil integrerande app).

Visa [kundvagn med flera artiklar i ALM](/help/migrated/learners/feature-summary/multi-item-cart.md)

## Stöd för HTML5-innehåll i Fluidic Player

**Adobe Learning Manager** har nu stöd för att överföra HTML5-innehåll som en .zip fil till innehållsbiblioteket. När dessa filer har laddats upp kan de inkluderas som moduler i en kurs. Författare kan också definiera slutförandekriterier för HTML5-moduler i egen takt, vilket gör det möjligt att antingen fylla i markerade elever eller automatiskt slutföra dem vid start.

### Vad ändras i den här versionen

Adobe Learning Manager har nu stöd för HTML5-innehåll i kurser i egen takt. Författare kan lägga till HTML5-innehåll som en .zip-fil i innehåll i egen takt. Eleverna kan visa HTML5-innehållet i Fluidic Player. Med den nya funktionen kan eleverna nu markera kursen som slutförd direkt i Fluidic Player för kurser i egen takt. Se [Lägg till HTML5-filtyp i innehållsbiblioteket](/help/migrated/authors/feature-summary/content-library.md#add-html5-file-type-in-the-content-library) för mer information.

Med den nya förbättringen kommer kursen med den externa länken automatiskt att markeras som slutförd när URL:en besöks, så länge författaren har ställt in slutförandekriterierna till det nya alternativet **[!UICONTROL On Launching content]**. Det nya alternativet **[!UICONTROL Completion Criteria]** har lagts till på sidan Aktivitetsmodul där författaren kan ställa in ifyllnadskriterier för de externa länkarna. Se [Lägg till HTML-länk i aktivitetsmodulen](/help/migrated/authors/feature-summary/courses.md#add-html-link-in-the-activity-module) för mer information.

![](assets/completion-criteria-activity-module.png)
_Alternativ för slutförandekriterium-Aktivitetsmodul_

## Försenade push-notiser för kurser i mobilappen

Eleverna kommer att få push-meddelanden när de missar en kursdeadline. Med den här nya förbättringen har eleverna nu möjlighet att antingen skjuta upp en påminnelse i 24 timmar eller bli påminda nästa vecka för varje försenad påminnelse de får. Detta gäller endast för försenade anmälningar om tidsfrist. Visa [Schemalägg push-meddelandet](/help/migrated/learners/feature-summary/user-notifications.md#schedule-the-push-notification)

## API-ändringar i den här versionen

### API för sökning

Sök-API:et innehåller följande ändringar:

Elever kan söka efter taggar i katalogfilter med hjälp av API:et ```GET /search``` . Elever kan söka efter taggarna genom att välja ```tag``` som ett värde för ```filter.loTypes``` parameter.

**Exempel på curl**

```
curl -X GET --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 5a858f23924f4feafa38ae8d6c4d97b6' 'https://example.com/primeapi/v2/search?page[limit]=10&query=Business&autoCompleteMode=true&filter.loTypes=tag&sort=relevance&filter.ignoreEnhancedLP=true&matchType=phrase&persistSearchHistory=true&stemmed=false&highlightResults=true'
```

De nya filtren, tillgänglig plats, tillgänglig väntelista och tidsintervallfilter har lagts till i följande API:er: ```GET /search``` och `GET /learningObjects`.

De nya filtren `filter.session.includeEnrollmentDeadline` har lagts till i följande API.```GET /search```

### API för konto

Den nya kolumnen `custom_injections`, , och `complianceLabelDefaultID` har lagts till i API:et för att hämta kontodata för användarslutpunkten ```GET /account``` `showComplianceLabel`.

### API för lärobjekt

Följande ändringar har gjorts i API:t för utbildningsobjekt i den här uppdateringen:

Det nya svarets äldre författar-ID och annan information som läggs till under `authorDetails` i API:t `GET /learningObjects` . Dessutom har ett nytt filter, `filter.authors`, lagts till för att filtrera äldre författare och deras kurser.

Det nya attributet som anropas `effectivenessIndex` hjälper dig att få information om kursens effektivitet.

**Exempel på curl**

```
curl --location 'https://example.com/primeapi/v2/learningObjects/course%3A9790045?enforcedFields%5BlearningObject%5D=effectivenessData' \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth 598665ab5c8a99bea0e774d9faf7f3ca'
```

Det nya svaret `whoShouldTake`, som ger information om vem som ska gå den här kursen, har lagts till i följande API:er: `POST /learningObjects/query`, `GET /learningObjects/{id}`, och `GET /learningObjects`.

**Exempel på curl**

```
curl -X GET --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 28a83fb8c87579af8ebc4434cc80f0c0' 'https://example.com/primeapi/v2/learningObjects/course%3A1131255' 
```

Det nya svaret `waitlistLimit`, som ger information om begränsning av väntelista, har lagts till i API:et `GET /learningObjects` .

Det nya svaret `count` , som ger det totala antalet inlärningsobjekt, har lagts till i API: `GET/ learningObjects` erna och `POST/ learningObjects/query`.

De nya svaren, `catalogFieldId` och `fieldValueId` har lagts till under `catalogLabels` i `GET/ learningObjects` API.

Elever kan hämta katalogetikettvärdena i API:et `GET /preview/learningObjects`.

### Nytt API för att få antal på marknadsplatsen

I den här versionen har ett nytt API `GET /search/marketplace/count` lagts till. Detta hjälper dig att få räkningen på de tillgängliga inlärningsobjekten på innehållsmarknaden.

**Exempel på curl**

```
curl -X GET --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth d8631c7b0e3b5d2ae00422ef30aaecfc' 'https://example.com/primeapi/v2/search/marketplace/count?query=course'
```

**Exempel på svar**

```
{
  "count": 54910
}
```

### API för instans av utbildningsobjekt

Följande ändringar har gjorts i API:t för inlärningsobjektsinstansen i den här uppdateringen:

I den här versionen har en ny nyckel med namnet `gamificationEnabled` lagts till i API:et för inlärningsobjektsinstansen `GET /learningObjects/{loId}/instances/{loInstanceId}`.

**Exempel på curl**

```
curl --location 'http://example.com/acapapi/primeapi/v2/learningObjects/learningProgram:12756/instances/learningProgram:12756_15644' 
```

Det nya `gamificationSettings` attributet till ovanstående API för att få information om Gamification-inställningarna. Till exempel: `GET /learningObjects/{loId}/instances/{loInstanceId}/gamificationSettings`.

**Exempel på curl**

```
curl --location 'http://example.com/acapapi/primeapi/v2/learningObjects/learningProgram:103852/instances/learningProgram:103852_103526/gamificationSettings'
```

Det nya `leaderboard` attributet till ovanstående API för att få information om Gamification-inställningarna. Till exempel: `GET /learningObjects/{loId}/instances/{loInstanceId}/leaderboard`.

**Exempel på curl**

```
curl --location 'https://example.com/primeapi/v2/learningObjects/learningProgram:106339/instances/learningProgram:106339_105775/leaderboard' \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth de4b5ee6efdd42375130db27ff503dd4'
```

### Ändringar av offsetgränser

För att förbättra systemprestanda och hantera resursutnyttjande mer effektivt har Adobe tagit bort höga förskjutningsvärden i slutpunkten GET /users för både ADMIN- och LEARNER-omfången. Vi rekommenderar att du använder jobb-API:et för att hämta posterna med ett förskjutningsvärde.

### Inaktuella API:er

Visa [API-utfasningar i Adobe Learning Manager](/help/migrated/api-deprecations-list.md) för en kumulativ lista över alla inaktuella API:er i produkten.

## Ändringar i rapporteringen

### Instrumentpanel för efterlevnad

I den här versionen har rapporten Instrumentpanel för efterlevnad två nya kolumner:

* Status
* Typ av krav

Detta är ett tillägg till de redan befintliga kolumnerna:

* Användarnamn
* Mejladress till användare
* LP/Certifiering/Kurs
* Typ
* Registreringsdatum (tidszonen UTC)
* Deadline (tidszonen UTC)
* Slutförandedatum (tidszonen UTC)
* Status %

### Rapport om träning

Träningsrapporten i Admin > Reports > anpassade rapporter **och jobb-API:** et **brukade ha kolumner som kallades** Skill(s)**och** Tag(s)**.********** Dessa kolumner har nu bytt namn till **Färdigheter** och **Taggar**.

### Rapport om innehållsgranskning

I den här versionen innehåller rapporten **[!UICONTROL Content Audit Trail]** nu följande nya attribut i kolumnen Ändringstyp:

* Lägg till användargrupp
* Ta bort användargrupp
* Lägg till anpassad etikett
* Ta bort anpassad etikett
* Lägg till delad katalog
* Ta bort delad katalog
* Uppdatering av delad katalog

## Bugg åtgärdad i den här uppdateringen

**Inlämning av aktivitet**

* Det går inte att ladda upp en fil igen till modulen för aktivitetssändning med ett fel 500 i nätverksanropet.

**Application Programming Interface**

* Det går inte att skapa ett Connect VC-möte om flera instruktörer har samma e-postadress.
* När du har registrerat dig för en utbildningsväg visar MS Teams VC en felaktig URL på översiktssidan.
* Den försignerade URL:en för användarrapporten som tillhandahålls som en del av jobb-API-svaret upphör att gälla efter sex timmar.
* När du genererar en inskrivningsrapport för en kurs visas ett felaktigt kursnamn i kolumnen Kursnamn.
* Migreringsarbetaren misslyckas med att skicka det unika lo-ID:t när han eller hon anropar bulk-API:et för kursen, men id:t tas bort.
* När en kurs ingår i en specifik katalog som en användare har åtkomst till (medan standardkatalogen är inaktiverad), trots inställningen som hindrar oregistrerade elever från att se kursen, kan du fortfarande hämta kursens metadata via learningobject/id-slutpunkten.
* Kunskapsfiltret fungerar inte som förväntat när skillname har kommatecken i namnet i API:et GET /learningObject.
* Det finns inkonsekvens i tidsstämpelmetadata för filen i datakvarhållningsarbetaren för SFTP.
* Om en anslutningsapp tas bort och konfigureras om verkar projektets migreringsstatus vara stängd.
* Träningsrapporten har &quot;Tag(s)&quot; som kolumnrubrik i stället för &quot;Tags&quot;.
* Exporten av Commerce-anslutningsprogrammet misslyckas om katalogen är inaktiverad och om någon av de exporterade kurserna bara är en del av den inaktiverade katalogen.

**Intygande**

* Ibland misslyckas det att registrera en användare på nytt för en återkommande certifiering.

**Anpassad roll**

* I vissa fall, när en anpassad administratör försöker byta till en instruktörsroll, visas fel 403 förbjudet.

**E-postmall och avisering**

* När en session har avbrutits skickas inte e-postmeddelandena till den sista uppsättningen lärare när lärarna tas bort från sessionen.
* Organisatören får inga e-postmeddelanden för MS Teams efter att ha skapat en virtuell instruktörsledd utbildning. Först efter att kursen är publicerad och e-postmallar är aktiverade utlöses e-postmeddelandena.
* Ibland består en e-postmall av ett felaktigt datumformat och översättning.

**Elev**

* När en elev är inskriven i flera instanser av en kurs och du laddar ner närvarorapporten innehåller rapporten felaktig information.
* En användare kan se en annan användares privata inlägg om de läggs till i en offentlig händelse.
* I vissa fall kan du inte avregistrera elever från en certifiering. Ett felmeddelande visas när du försöker avregistrera dig.
* En certifiering markeras som slutförd även efter att en administratör har markerat den som slutförd efter att ha valt endast en kurs.
* En administratör kan inte markera en VC som slutförd om sessionens sluttid ändras till ett tidigare datum.
* Rapporten Sessionsnärvaro visas som &quot;Ej närvarande&quot; för elever som står på en väntelista.

**App för elever**

* När du har laddat ner kursanteckningarna som PDF visas anteckningarna slumpmässigt. De följer inte ordern.

**Utbildningsväg**

* När du har valt en färdighet i en utbildningsväg visas inte listrutan som förväntat när du markerar textfältet.
* I vissa fall kan du inte ta bort kunskaper från en utbildningsväg.

**Utbildningsprogram**

* Om ett flexibelt utbildningsprogram har många kurser slutförs inte utbildningsplanen även om en administratör har markerat den som slutförd.
* Kolumnen last_modified_by i registreringsrapporten uppdateras inte när en elev byter instans.

**Rapport**

* I vissa fall kan en administratör inte exportera träningsrapporten.
* När ett SCORM-innehåll innehåller frågor eller svar som är längre än 32 767 tecken kan du inte ladda ner kursquizrapporten i Excel.
* När du har valt Återställ Gamification återställs inte datumet för uppnådd nivå.

**Söka**

* För närvarande, efter att ha exporterat alla användargrupper, finns även borttagna användargrupper i utdata.
* På grund av tillfälliga sökproblem kan du inte söka efter en certifiering.

## Känt problem i den här versionen

Den mobila offlinespelaren läser inte in HTML5-innehållet.

## Systemkrav

Visa [systemkrav för](/help/migrated/system-requirements.md) Adobe Learning Manager.

## Tidigare versioner av Adobe Learning Manager

* [Version från mars 2024](/help/migrated/whats-new-march-2024.md)
* [Version från november 2023](/help/migrated/whats-new-november-2023.md)
