---
title: Motsvarigheter och suppleanter i Adobe Learning Manager
description: Leverera en friktionsfri utbildningsupplevelse och ta bort överflödig utbildning med motsvarigheter och alternativ i ALM. Med den här nya funktionen kan administratörer konfigurera enkelriktade (alternativa) eller dubbelriktade (motsvarande) regler, där slutförande av en utbildning automatiskt ger alternativt slutförande av en annan
jcr-language: en-us
source-git-commit: e70a3b5a5d1080dc4b3a56aa726c717120c6bfa3
workflow-type: tm+mt
source-wordcount: '3457'
ht-degree: 0%

---


# Suppleanter och motsvarande

## Introduktion

I många organisationer stöter elever på utbildningssituationer där olika kurser lagligen kan uppfylla samma krav. När ska till exempel en ny kurs ersätta en äldre kurs? När bör en mer omfattande kurs ersätta en kortare kurs eller när bör en särskild ersättningskurs erbjudas?

Funktionen Alternate Courses eller Learning Path ger ALM ett formellt sätt att säga:

&quot;Om eleven har slutfört denna utbildning ska denne anses ha uppfyllt det relaterade utbildningskravet.&quot;

Funktionen fungerar i alla kurser och utbildningsvägar och ser till att krav längre fram, som krav på förutsättningar och efterlevnadsregler, uppfylls, och gör detta utan att tvinga eleverna att gå igenom redundant innehåll. Den rapporterar också korrekt genom att registrera vad som slutfördes direkt jämfört med vad som var nöjd via ett alternativ.

I kärnan introducerar funktionen konceptet för ett alternativt slutförande: ett speciellt slutförandetillstånd som skapas automatiskt när en elev slutför en konfigurerad källutbildning som räknas mot ett annat målutbildningsmål.

## Alternativa relationer

Vissa utbildningsrelationer är dubbelriktade, vilket innebär att varje kurs kan tillfredsställa den andras krav. Detta är i själva verket ett scenario där två utbildningar behandlas som ömsesidigt utbytbara. Enkelriktade förhållanden gör det däremot möjligt för en utbildning att uppfylla kravet på en annan, men inte tvärtom. ALM modellerar båda scenarierna med samma underliggande alternativa slutförandemekanism.

* **Dubbelriktad relation (motsvarande):** När du slutför en utbildning uppfyller du kraven för den andra.
* **Enkelriktad relation:** Utbildning A uppfyller utbildning B, men A räcker inte för att slutföra B. Detta är vanligt när en nyare eller mer omfattande version bör räknas in i ett äldre krav, men inte tvärtom.

Till exempel när en mer omfattande supermängdkurs täcker allt i en enklare delmängdskurs. Slutförande av delmängden bör uppfylla kravet för delmängden, men inte nödvändigtvis tvärtom.

En nyare, utökad kurs som bör räknas till ett äldre krav.

En kurs som är utformad för en specifik målgrupp (t.ex. en regional eller tillgänglighetsanpassad variant) och som fortfarande uppfyller samma krav som grundkursen.

En förbättrad ny version av en kurs som organisationen vill räkna för ett äldre krav, men den äldre versionen ska inte räknas för det nya kravet.

I alternativfilmer är förhållandet normalt ett sätt. Om kurs A är ett alternativ till kurs B, kan uppfyllande av A uppfylla B:s krav, men att slutföra B uppfyller inte nödvändigtvis A.

När en konfigurerad källutbildning är slutförd ger ALM automatiskt ett alternativt resultat för en eller flera målutbildningar.

## Vilka problem löser man med detta?

Utan suppleanter stöter administratörer och elever på flera återkommande problem:

* Elever ombeds ofta att repetera kurser som täcker innehåll som de redan har slutfört i en annan version eller ett annat format.
* Det är enklare att uppdatera kompatibilitetsprogram eftersom administratörer kan ersätta eller omstrukturera utbildningar utan att elever som har slutfört äldre versioner tvingas att ta om alternativt eller ersatt innehåll.
* Logiken som krävs är stel. Om en utbildningsväg förutsätter en viss kurs finns det inget rent sätt att erkänna att en annan utbildning är tillräckligt bra.
* Rapportering och revision är svårare. Det finns ingen formell signal som visar att ett krav uppfylldes genom ett alternativt slutförande och inget enkelt sätt att spåra källan till krediten.

Alternativfunktionen åtgärdar dessa problem genom att:

* Förhindra dubbelarbete för elever när ersättare är giltiga.
* Tillåta administratörer att ändra utbildningsstrukturer (till exempel byta en kurs i en bana) utan att bryta slutföranden för elever som tog den tidigare versionen.
* Att tillåta krav och efterlevnadskontroller som respekterar både direkta slutföranden och alternativa eller likvärdiga slutföranden.
* I utskrifter och rapporter tydligt anteckna om en utbildning har fullgjorts direkt eller fullgjorts genom ett alternativt förhållande, tillsammans med vilket utbildningen tjänade som källa.

## Så här fungerar funktionen begreppsmässigt

Funktionen bygger på tre huvudidéer: **relationer**, **alternativa slutföranden** och **nedströmsbeteenden**.

### Relationer mellan utbildningar

Administratörer definierar relationer mellan kurser och utbildningsvägar. För varje relation väljer de en källa och ett eller flera mål. En enskild kurs kan ha upp till 30 mål beroende på hur många tidigare eller relaterade utbildningar den bör uppfylla.

För motsvarande kan administratörer göra relationen dubbelriktad om de vill att båda utbildningarna ska tillfredsställa varandra. För alternativ behåller administratörer normalt riktningen ett*sätt för att återspegla att endast vissa ersättningar är tillåtna.

Dessa relationer lagras på utbildningsnivå, inte på elevnivå. När de har konfigurerats och aktiverats kan de användas   för alla pågående och framtida slutföranden av källutbildningen, med förbehåll för inställningar på kontonivå som t.ex. om retroaktivt slutförande är aktiverat.

### Alternativ slutförande

När en elev slutför en källutbildning granskar ALM alla konfigurerade alternativa relationer och skapar för varje relevant målutbildning en alternativ slutförandepost. Den här posten skiljer sig från ett normalt slutförande:

* Det markerar målutbildningen för eleven men håller koll på att den slutfördes via alternativa istället för direkt.
* Den registrerar vilken källutbildning som användes för att uppfylla målet.
* Den lagras i en särskild struktur så att rapporter kan skilja mellan direkta och alternativa slutföranden.

Elever kommer att se alternativ slutföring även om de inte är registrerade. Elevens betygsrapport (LT) innehåller endast poster med utbildningar som eleven har registrerat sig för.

#### Elevens appupplevelse för alternativa och likvärdiga slutföranden

Alternativa avslut visas tydligt i elevappen så att eleverna tydligt kan förstå hur ett utbildningskrav uppfylldes, samtidigt som konsekvensen med utskrifter och rapporter bibehålls.

#### LO-kortbeteende

##### Alternativ slutförandestatus

När en elev slutför en utbildning via en alternativ relation visar kortet för utbildningsobjekt (LO) en distinkt status som är **Slutförd via Alternativ**. Den här visuella skillnaden hjälper elever att skilja mellan direkta slutföranden och slutföranden som beviljas genom konfigurerade relationer.

#### Indikator för slutförandemetod

LO-kortet innehåller en indikator för slutförandemetod (till exempel en etikett eller ikon) för att visa att slutförandet uppnåddes med ett alternativ. Om ett alternativt slutförande senare återkallas på grund av ändringar som retroaktiv slutföring eller borttagning av källutbildningen, kommer ALM att ångra alla gränssnittstillägg som gjorts för alternativt slutförande. Eleven kommer fortfarande inte att kunna ange LO enligt det aktuella katalogåtkomstbeteendet.

#### Insyn och revisionsdetaljer

Elever kan öppna LO-kortet för att se ytterligare information, bland annat:

* Källkursen eller utbildningsvägen som gav det alternativa slutförandet

Detta garanterar genomskinlighet.

#### Filtrera och visa

##### Filter för slutförandemetod

Elevappen har ett filter som gör att eleverna kan skilja mellan:

* Slutfört
* Slutfört via alternativa (detta filtrerar LO:er som endast har alternativa slutföranden. Om en LO har alternativ samt direkt slutförande kommer den inte att inkluderas.)
* När du väljer **Slutfört** och **Slutfört via alternativ** kan du se alla slutföranden

Detta gör det möjligt för elever att snabbt förstå hur deras utbildningskrav uppfylldes.

##### Betygsutskrifts- och framstegsvyer

Filtret för slutförandemetod är tillgängligt i elevvyer. Till exempel:

* Spårningsavsnitt för status och slutförande

Dessa synpunkter visar tydligt vilka utbildningar som fullgjorts direkt och vilka som fullgjorts genom suppleanter.

<!--## Configure equivalent courses (complete each other)

Use this workflow to define courses that are **equal in value**, where completing either course should automatically complete the other.

1. Launch ALM and navigate to courses.
2. Select a course to configure.
3. Navigate to the **Alternates** section.
4. Search for and select one or more related courses.
5. For each selected course, enable **Completes each other**.
6. Save the configuration.

**Result**

- ALMm records a **bi-directional equivalence relationship**.
- Either course can act as a completion source for the other.

## Configure alternate courses (superset → subset)

Use this workflow when one course is a **superset** of another and should satisfy completion for the simpler or subset course.

1. Launch ALM and navigate to courses.
2. Select the **superset (primary)** course.
3. Go to the **Alternates** section.
4. Select one or more **alternate (subset)** courses.
5. Leave the relationship as **alternate** (do not enable completes each other).
6. Save the configuration.

**Result**

- Completion flows **one-way** from the source course to the alternate.
- Reverse completion is not applied.

## Apply completion logic after source course completion

Automatically evaluate and apply alternate or equivalent completion once a learner completes a configured source course. ALM:

1. Detects completion of a **source course**.
2. Evaluates configured relationships:
   - Equivalent relationships
   - Alternate relationships
3. For each related course:
   - Marks the course as completed if conditions are met
4. Creates a completion record with method **Alternate**.

**Key system rules**

- Alternate completion:
  - Satisfies prerequisites
  - Allows progress in learning paths and certifications
- Alternate completion does **not** award:
  - Skills
  - Badges
  - Gamification credits

## Record completion in Learning Transcript

Ensure alternate and equivalent completions are clearly distinguishable from direct completions for audit and reporting. ALM:

1. Updates the **Learner Transcript (LT)**.
2. Sets:
   - Completion status = Completed
   - Completion method = **Alternate**
3. Sets completion date equal to the **source course completion date**.

## Enable retroactive completion (optional)

Apply alternate or equivalent completion benefits to learners who completed source courses **before** the relationships were configured.

1. Open **Account-level settings** from Administrator home > Settings > General.
2. Enable **Retroactive completion**.
3. Save the configuration.

ALM:

1. Scans historical learner completions.
2. Applies alternate or equivalent completion where applicable.
3. Updates learner transcripts automatically.

## Enable retroactive incompletion (irreversible)

Revoke previously applied alternate or equivalent completions when relationships are removed or corrected.

1. Open **Account-level settings**.
2. Enable **Retroactive incompletion**.
3. Modify or remove alternate/equivalent relationships.

ALM:

1. Identifies impacted alternate completions.
2. Revokes previously applied alternate or equivalent completions.
3. Updates transcript entries to **Alternate (Revoked)**.-->

### Heltäckande flöde

**För elever**

1. Gå till **Min utbildning** eller **Slutförda kurser** i elevappen.
2. Granska LO-kort för att identifiera utbildningar markerade som **Slutförda via Alternativ**.
3. Öppna ett LO-kort för att visa detaljer (på sidan Översikt) om källutbildningen.
4. Använd filtret för att välja **Direkt**, **Alternativ** eller **Alla**.
5. Granska den uppdaterade listan baserat på den valda slutförandemetoden.

**För administratörer och författare**

* Konfigurera alternativa relationer mellan kurser eller utbildningsvägar i administratörsgränssnittet.

## Retroaktivt slutförande och slutförande

ALM stöder retroaktiv slutförande och retroaktiv inslutförande för att säkerställa att alternativa relationer förblir korrekta över tid, även när relationer ändras eller tas bort efter att elever redan har slutfört utbildning.

### Retroaktivt slutförande

#### Definition

När retroaktiv slutföring är aktiverad får elever som har slutfört en källkurs automatiskt en alternativ slutföring för målkursen om en alternativ relation skapas senare. Detta säkerställer att det historiska lärandet infrias utan att eleverna behöver genomgå utbildningen på nytt.

#### Så här fungerar det

1. En administratör möjliggör retroaktiv slutförande på kontonivå.
2. Administratören definierar en alternativ relation mellan en käll- och målutbildning.
3. Systemet söker igenom historiska slutförandeposter för källutbildningen.
4. Berättigade elever ges alternativt slutförande av målutbildningen.
5. Dessa poster visas som **slutförda via alternativa** i elevens utskrifter och rapporter.

>[!NOTE]
>
>När retroaktiv slutförande är aktiverat gäller det bara relationer som skapas efteråt. Det gäller inte relationer som redan fanns innan den retroaktiva inställningen aktiverades.

### Retroaktiv slutförande

#### Definition

När retroaktiv slutförande är aktiverat återkallas alternativa slutföranden om den underliggande alternativa relationen tas bort eller om källutbildningen tas bort.
Detta säkerställer att systemet återspeglar aktuella och giltiga utbildningsrelationer.

#### Så här fungerar det

1. En administratör möjliggör retroaktiv slutförande på kontonivå.
2. Administratören tar bort en alternativ relation eller tar bort källutbildningen.
3. Systemet identifierar elever som har fått alternativt slutförande via den berörda relationen.
4. Motsvarande alternativa slutförandeposter återkallas.
5. Återkallade poster markeras som **Alternativa (återkallade)** i utskrifter och rapporter för granskningssynlighet.

#### Inverkan på förutsättningarna

Alternativa slutföranden, inklusive sådana som beviljas retroaktivt, behandlas som giltiga slutföranden vid bedömning av förutsättningar. Om en elev har **slutfört via Alternativ** kan hen fortsätta med kurser som kräver målutbildningen.

Om ett alternativt slutförande senare återkallas genom ett retroaktivt slutförande kan eleven förlora behörigheten till kurser som är beroende av den förutsättningen. Om eleven inte startade den beroende/efterföljande LO:n kommer behörigheten som administreras av källans LO att återställas. Om eleven redan har startat eller slutfört beroende/efterföljande LO kommer detta inte att påverka.

#### Inverkan på utbildningsvägar och certifieringar

Alternativa slutföranden bidrar till slutförande av utbildningsvägar och permanenta certifieringar. Elever kan gå vidare eller slutföra dessa program när obligatoriska utbildningar har uppfyllts via alternativa relationer.

Om ett alternativt slutförande återkallas kan de berörda utbildningsvägarna eller certifieringarna förlora förloppet tills kravet är uppfyllt genom ett giltigt slutförande.

### Heltäckande arbetsflöde

#### Aktivera retroaktivt slutförande eller slutförande

1. Administratörer navigerar till kontoinställningar och aktiverar retroaktiv slutföring och/eller retroaktiv slutföring.
2. Administratörer skapar, ändrar eller tar bort alternativa relationer mellan utbildningar.

#### Systemåtgärder

* **För retroaktiv slutförande**:
Systemet tillåter alternativa slutföranden baserat på tidigare slutföranden av källor.
* **För retroaktiv slutföring**:
Systemet återkallar alternativa slutföranden när relationer tas bort eller källutbildningar raderas.

#### Elevupplevelse

Elever ser uppdaterade slutförandestatusar på LO-kort och i utskrifter, som:

* **Slutfört via alternativ**

När ett alternativt slutförande återkallas visas ingen etikett i elevgränssnittet. I rapporter och utskrifter visas slutförandemetoderna som:

* Alternativ
* Alternativ (återkallat)
* Direkt

Kontroller av förutsättningar, förlopp för utbildningsväg och uppdatering av certifieringsstatus dynamiskt baserat på det aktuella slutförandetillståndet.

Ordnade LO:er låses upp dynamiskt baserat på alternerande slutförande.

Kompetenser, utmärkelsetecken, spelifieringspoäng eller feedback delas inte ut till elever vid alternativt slutförande av mål.

#### Rapportering och revision

Alla retroaktiva ändringar återspeglas i rapporten Utbildningsbevis (LT). När källan har tagits bort kan elevens betygsutdrag fortfarande visa ett källutbildningsID bredvid **Återkallat alternativ**. Rapporter skiljer tydligt mellan direkta slutföranden, alternativa slutföranden och återkallade alternativa slutföranden till stöd för efterlevnad, supportutredningar och revisioner.

Registreringsrapporten lämnar fältet Källtext för slutförande tomt om rapporten är direkt slutförd, medan elevens betygsutdrag visar e-postadressen och typen för samma.

När ett mål tas bort från källan (eller när själva källan tas bort) kanske inte registreringsrapporten visar samma **alternativa eller alternativa (återkallade)**-status som i elevens betygsutdrag.

Även när   **Alternativ** är inaktiverade, historiska poster i **Innehållsgranskning** eller **Registrering** rader kan fortfarande visa aktivitet relaterad till alternativ.

Slutförandedatumet kan infalla före registreringsdatumet när en LO slutförs via en alternativ sökväg **före** då eleven faktiskt registrerar sig. Eftersom alternativa slutföranden kan ske oavsett elevstatus (**Registrerad**, **Inte registrerad** eller **Pågår**) kan eleverna slutföra LO först och endast registrera sig för målkursen senare.

## Effekten av att ta bort källutbildning i alternativa lösningar

Livscykeltillståndet för en källutbildning (indragen eller borttagen) påverkar direkt hur alternativa slutföranden behålls för elever. ALM hanterar dessa scenarier på olika sätt för att bevara den historiska noggrannheten samtidigt som de aktuella relationerna förblir giltiga.

### Ta bort källutbildning

#### Definition

Vid utfasning av en kurs är den inte längre tillgänglig för nya registreringar samtidigt som den finns kvar i systemet för tidigare referens-, rapporterings- och revisionsändamål.

#### Påverkan

* Befintliga alternativa slutföranden som har beviljats genom den utfasade källkursen är fortfarande giltiga.
* Elever som tidigare har slutfört källkursen fortsätter att ha alternativ slutförande för målkursen.
* Inga nya alternativa slutföranden genereras från den utfasade kursen, eftersom den inte kan slutföras av nya elever.
* Elevens utskrifter och rapporter fortsätter att visa **Slutförda via alternativa** för berörda elever.

### Radera källutbildning

#### Definition

När du tar bort en kurs tas den bort helt från systemet, inklusive slutförandeposter och konfigurerade relationer.

#### Påverkan

* Om en källutbildning tas bort kan statusen ändras till **Alternativ (återkallad)**. Utfasning av en LO utlöser inte denna status.
* Om retroaktiv slutförande är aktiverat återkallas alla alternativa slutföranden som beviljats via kursen för borttagen källa.
* Elevens betygsutdrag och rapporter uppdateras för att visa **Alternativa (återkallade)** för granskning och efterlevnadssynlighet.
* Slutförande av utbildningsvägar och tillgång till certifikat påverkas inte.
* Inga ytterligare alternativa slutföranden kan beviljas från kursen som tagits bort.

#### Arbetsflöde

1. En administratör tar bort eller tar bort källkursen med administratörsgränssnittet.
2. Systemet utvärderar alla alternativa slutföranden som härleds från källkursen.
3. Slutförandestatus uppdateras baserat på kursens tillstånd:
   * **Utfasade:** Befintliga alternativa slutföranden förblir oförändrade.
   * **Borttaget:** Alternativa slutföranden återkallas om retroaktiv inslutförande aktiveras.
4. Elevens utskrifter och rapporter återspeglar den uppdaterade statusen för att stödja efterlevnad och revisionskrav.

## Ingen länkning av relationer

ALM stöder inte länkning av alternativa relationer. Alternativa slutföranden beviljas endast för direkt konfigurerade relationer och överlappas inte av flera nivåer av kurser.

### Koncept: ingen länkning av relationer

#### Definition

kedjning avser att tillåta alternativa relationer att sprida sig över flera kurser. Om till exempel kurs A är ett alternativ till kurs B, och kurs B är ett alternativ till kurs C, innebär kedjning att slutföra kurs A ger bidrag till kurs C.

#### integritetspolicy

Kedjning stöds inte. Alternativa och likvärdiga relationer utvärderas bara på en enda nivå. När du slutför en källkurs beviljas alternativt slutförande endast till dess omedelbara målkurs eller målkurser, inte till några mål nedströms.

### Arbetsflöde

#### Relationsinställningar

En administratör definierar alternativa relationer mellan kurser, till exempel:

* Kurs A → kurs B
* Kurs B → kurs C

#### Slutförandehändelse

En elev slutför kurs A direkt.

#### Systemåtgärd

* Systemet beviljar alternativt slutförande för kurs B om förhållandet A → B är definierat.
* Systemet beviljar inte alternativt slutförande för kurs C, även om det finns en B- → C-relation.

#### Krav för direkt slutförande

För att få alternativ slutföring av kurs C måste eleven:

* Genomför kurs B direkt, eller
* Slutför en kurs som uttryckligen är konfigurerad som ett direkt alternativ till eller motsvarande för kurs C.

## Konsekvenser

### Inga indirekta fördelar

Elever kan inte få tillgodoräknande om slutförande av kurser längre ned i en relationskedja om inte varje kurs (eller dess direkta alternativ) har slutförts. Detta garanterar att utbildningskraven uppfylls på ett tydligt och förutsägbart sätt.

### Förenklad granskning och rapportering

Rapporter och elevutskrifter visar endast alternativa slutföranden för direkta relationer. På så sätt undviker man komplexa granskningsspår i flera steg och skapar klarhet när man granskar hur ett slutförande har beviljats.

## Katalogdelning med kollegiala konton: relationer delas inte

Katalogdelning tillåter att LO:er delas mellan kollegiala konton, men alternativa och likvärdiga relationer hanteras oberoende inom varje konto och delas inte.

### Koncept: katalogdelning och relationer

#### Katalogdelning

Konton kan dela kataloger med kollegiala konton för att ge åtkomst till kurser, utbildningsvägar och andra LO:er över konton.

#### Relationer delas inte

Alternativa, ekvivalenta och alternerande slutföranderelationer som konfigurerats i källkontot delas inte och replikeras inte när en katalog delas. Varje konto underhåller och utvärderar sina egna relationer oberoende av varandra.

### Arbetsflöde

#### Katalogdelning

En administratör i **Konto A** delar en katalog som innehåller LO:er med **Konto B**.

#### Relationskonfiguration

Konto A kan ha alternativa relationer definierade bland LO:erna i den delade katalogen.

#### Kollegial kontoåtkomst

Konto B får åtkomst till de delade utbildningsobjekten men ärver inte några alternativa relationer som konfigurerats i konto A.

#### Oberoende ledning

Om konto B kräver liknande alternativt beteende måste en administratör i konto B manuellt konfigurera relationerna inom det kontot.

#### Konsekvenser

##### Ingen automatisk relationsspridning

Alternativa relationer är inte automatiskt tillgängliga i kollegiala konton genom katalogdelning.

##### Manuell konfiguration krävs

Varje kollegialt konto ansvarar för att definiera och hantera sina egna relationer för delade LO:er.

##### Överensstämmelseöverväganden

Slutförande, uppfyllelse av förutsättningar och rapportering kan skilja sig åt mellan olika konton såvida inte relationerna avsiktligt bringas i linje genom manuell konfiguration.

## Nedströmsbeteende

När det finns en alternativ slutförd utbildning använder ALM den i nedströmskontroller:

* Om målutbildningen är en **förutsättning** för andra utbildningar blir eleven berättigad till dessa utbildningar som om hen hade slutfört målet.
* Om målet är en **obligatorisk kurs i en utbildningsväg** kan sökvägens slutförandelogik behandla eleven som att ha slutfört den delen och fortsätta för att markera banan som slutförd när andra villkor är uppfyllda.
* Efterlevnadstavlor och andra instrumentpaneler, till exempel en kontrollpanel för gruppframgång som är beroende av om ett utbildningskrav uppfylls, kan inkludera elever som bara har alternativa slutföranden.

Systemet skiljer mellan faktisk slutföring och alternerande slutförande så att

* Om eleven senare slutför målutbildningen direkt och slutför den, kan detta direkta slutförande åsidosätta behovet av alternativt slutförande.
* Om relationen mellan källa och mål tas bort eller ändras kan ALM ta bort de alternativa slutförandena utan att röra äkta slutföranden, förutsatt att retroaktiva slutföranden är aktiverade för kontot.

Alternativa avslut är utformade så att de inte stör den faktiska elevaktiviteten på målutbildningen. De fungerar som ett överlägg som kan revideras om relationerna förändras.

## E-postmeddelanden och meddelanden

Så snart en elev slutför en kurs ska hen få ett meddelande i appen och ett e-postmeddelande som visar kursens status och hur den slutfördes - huruvida den slutfördes via en alternativ kurs.

>[!NOTE]
>
>Alternativ slutföring kan fortfarande utlösa meddelanden om LO-mål i kataloger där eleven inte kan se. Alternativa meddelanden om slutförande/slutförande kanske inte visas på samma sätt i mobilappen som på andra ställen.

## Lägg till en alternativ kurs

Administratörer kan lägga till alternativa kurser och vägar så att elever har flera val att slutföra sina kurser och vägar.

1. Gå till avsnittet **Utbildning** > **Kurser**. En lista över tillgängliga kurser visas.
   ![](assets/ALM-courses-main.png)
   *Lista över kurser*
2. Navigera till kursen som du vill lägga till en alternativ kurs för.
   ![](assets/ALM-course-single.png)
   *Lägg till en alternativ kurs i en kurs*
3. Gå till avsnittet **Hantera** > **Alternativa kurser/sökvägar**.
   ![](assets/ALM-alt-train-paths.png)
   *Alternativa utbildningar/banor*
4. Välj **Lägg till kurser/banor**. En lista över tillgängliga kurser visas.
   ![](assets/ALM-alt-courses-list.png)
   *Lista över tillgängliga kurser*
5. Markera de kurser som du vill ska markeras som **Alternativa** genom att markera kryssrutan för varje kurs överst till vänster i rutan.
   ![](assets/ALM-alt-courses-added.png)
   *Lägg till alternativ kurs*
6. Välj **Lägg till**.

   >[!NOTE]
   >
   >Nu kan du ta bort de alternativa kurserna om du vill. Om du vill ta bort de alternativa kurserna väljer du **Ta bort alternativ** bredvid varje kurs till höger.

7. Välj **Spara**. De alternativa kurserna sparas nu.

Förloppet påverkas inte av alternativ slutföring. När en kurs eller utbildningsväg har slutförts via ett alternativt slutförande kan eleven fortfarande komma åt och konsumera den direkt för att förstärka inlärningen och få fördelar nedströms (till exempel spelifieringspoäng). I sådana fall återspeglar förloppsstatusen elevens faktiska förlopp från direkt förbrukning, oberoende av det alternativa slutförandeläget. Du får även ett meddelande i appen och ett e-postmeddelande om slutförandet via ett alternativ.

Det finns flera fördelar med denna komplettering, vilka anges nedan:

* Detta räknas som slutförande som en del av utbildningsvägen där detta finns.
* Detta öppnar även andra länkade kurser/vägar.

## Inställningar för privilegierade användare

Med följande inställningar kan privilegierade användare använda retroaktiva slutföranden och slutföranden.

1. Gå till avsnittet **Konfigurera** > **Inställningar** > **Grundläggande** > **Allmänt** > **Alternativa kurser/vägar**.
2. Välj **Aktivera retroaktiva slutföranden** och **Aktivera retroaktiva slutföranden** eller bara en av de två enligt dina behov.
   ![](assets/ALM-alt-train-paths-settings-powerusers.png)
   *Aktivera retroaktiv slutföring eller slutförande*

## Elevens betygsrapporter

Hur en elev slutför en kurs/vägar beskrivs i rapporten Elevens betygsutdrag. Följande scenarier fångas upp:

1. När en elev slutför en kurs direkt utan att välja en annan kurs återspeglas det i rapporten Elevens betygsutdrag
2. När en elev slutför en alternativ kurs återspeglas det i elevens betygsrapport
3. När alla alternativa slutföranden återkallas på grund av retroaktiv inslutföring och relationsborttagning visas det i rapporten Elevens betygsutdrag.
