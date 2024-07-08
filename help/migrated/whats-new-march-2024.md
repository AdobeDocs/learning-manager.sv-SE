---
description: Läs mer om de nya funktionerna och förbättringarna i mars 2024-versionen av Adobe Learning Manager
jcr-language: en_us
title: Sammanfattning av nya funktioner
contentowner: jayakarr
exl-id: 603f1f1c-bf8d-4807-b9f7-b10ded19a91e
source-git-commit: c833d92533b7fbf5a87c980d8b5e088185d02ef5
workflow-type: tm+mt
source-wordcount: '3903'
ht-degree: 0%

---

# Sammanfattning av nya funktioner {#new-features-summary}

Lär dig mer om de nya funktionerna och förbättringarna i mars 2024-versionen av Adobe Learning Manager.

Utforska några av de senaste funktionerna i Adobe Learning Manager, till exempel:

1. Importera kunskaper från externa källor
1. Stöd för flera varumärken
1. Checklista för omvärdering-aktivitetsmodul
1. Vitmärkt app för mobilt lärande

>[!NOTE]
>
>Kolla in det här [webbseminariet](https://learningmanager.adobe.com/app/learner?accountId=98632#/course/9212121) för att lära dig mer om de nya funktionerna i den här versionen.


## Vad är nytt i den här versionen {#whatsnewandchanged}

### Importera kunskaper från externa källor

Importera kunskaper från innehållsleverantörer, till exempel LinkedIn och Go1, med hjälp av respektive anslutningsprogram. Den här förbättringen är en del av målet mot Learning Managers förmåga att integrera med externa Skills Clouds och Talent Management Systems. De importerade färdigheterna läggs till i de administratörsdefinierade färdigheterna i Learning Manager och är tillgängliga för författare när du skapar kursen. Förbättringar har också gjorts av färdighetssökningsfunktionen på plattformen för att ge en bättre sökupplevelse när kontot har ett stort antal färdigheter.

Visa [importkunskaper](administrators/feature-summary/import-skills-external-sources.md) om du vill veta mer.

### Anpassat varumärke

Du kommer nu att kunna anpassa vissa gränssnittselement – organisationsnamnet, logotypen och användargränssnittstemat baserat på de användargrupper som är tillgängliga i kontot. En organisation med flera avdelningar kan till exempel ställa in en anpassad logotyp och ett UI-tema som ska visas för varje avdelning.

>[!NOTE]
>
>Den här funktionen för flera varumärken gäller inte för Admins vy. De kommer alltid att se varumärkesprofilering på organisationsnivå i sitt konto. Detta beror på att det här är en funktion som riktar sig till eleverna, och administratörer kanske inte vill ha den på sitt konto.

Visa [Flera anpassade varumärken](administrators/feature-summary/themes.md#multiple-branding) för mer information.


## Ändringar för konton med stor användarbas

### Admin- Kurs- eller utbildningsvägssidor

Om ett stort antal elever är inskrivna på kursen, till exempel fler än 50 000, visas inte listan över elever. Du kan antingen söka efter en elev i *sökfältet Sök elever* eller välja länken **Ladda ner** högst upp i sökfältet för att ladda ner listan över elever.

### Sidan Admin- Elever

När du söker efter en användare laddar **alternativen Ladda ner elev** och **Exportera** ner samma rapport. Under tiden, när du söker efter en användargrupp, kan du nu ladda ner filtrerade användare från den användargruppen. När du söker i en användargrupp,
Alternativet Ladda **ned elevlista** ändras till **Ladda ned elevlista för användargrupp** Alternativet **Exportera** laddar ned hela listan igen.

### Sidan Admin- Användare

#### Interna användare

Om antalet användare till exempel överstiger 50 000 visas ett meddelande om att ladda ned data för en mer detaljerad analys senare. Sökfältet är nu framträdande och visar en användare i formatet *Namn, e-post | UUID*.

>[!NOTE]
>
>UUID visas bara om UUID är aktiverat för kontot.

#### Externa användare

För externa användare gäller samma beteende. Om antalet användare är stort kan du ladda ner användarna och även hämta uppgifter om en användare efter en sökning i formatet *Namn, e-post | UUID*.

#### Sidan Användarrensning

På sidan Användarrensning har vi tagit bort sorteringsfunktionen **för borttagna användare för Datum borttagen**. Du kan bara sortera på UUID:erna.

### Sidor för admin-instans

#### Kurs eller utbildningsväg

Om antalet inskrivningar är stort visas inte antalet elever i Adobe Learning Manager. Istället kommer det att finnas en ikon som du kan välja och se antalet elever och navigera till sidan Elever.

Antalet elever kommer att visas som ett ungefärligt värde. Till exempel, om antalet elever är fler än 50 000, kommer värdet att visas som 50K+.

### Admin- L1/L3 sidor

Om antalet kursinskrivningar är stort på L1 Feedback-sidan visas inte listan över elever. I stället kan du exportera listan över användare för en mer detaljerad analys senare.

Sökningen har stöd för förskrivning och resultaten är begränsade till den valda instansen.

#### Sidan Närvaro och poängsättning

När du söker efter en användare på sidan körs sökningen över alla tillgängliga instanser. Resultatet är dock för den valda instansen.

Om du söker efter en användargrupp på sidan Närvaro och antalet användare överstiger 10 000 i användargruppen oavsett registrering, kan du bara utföra åtgärder på gruppnivå. Du kommer inte att kunna visa listan över användare.

Om antalet användare i användargruppen är färre än 10 000 kan du utföra enskilda åtgärder på användarnivå tillsammans med åtgärder på gruppnivå. I det här fallet inaktiveras inte listan över användare.

### Sidan Admin- Certifieringar

Om det finns ett stort antal användare som är registrerade för en certifiering i aktuella versioner av Adobe Learning Manager kan du inte visa de oregistrerade eleverna eftersom **listrutan Status** är inaktiverad.

Om antalet registrerade användare är stort i den här versionen av Adobe Learning Manager visas bara två alternativ i **listrutan Status** : **Registrerad** och **Avregistrerad**. Alternativet **Registrerad** är markerat som standard. Om du väljer **Avregistrerad** visas listan över inskrivna elever.

#### Ändringar i användargrupp

Om antalet användare i användargruppen är färre än till exempel 50 000 **visar listrutan Status** alla alternativ – Certifierad, Tilldelad och Upphör att gälla.

Om antalet användare i en användargrupp är stort **visar rullgardinsmenyn Status** bara två alternativ - **Registrerade** och **Avregistrerade**, enligt den nya designen.

### Jämförelsetabell

<table>
    <tbody>
        <tr>
            <td><b>Sida</b></td>
            <td><b>Före ändring av tröskelvärden</b></td>
            <td><b>Efter ändring av tröskelvärde</b></td>
        </tr>
        <tr>
            <td>Admin- Kursomgång</td>
            <td>Instanser visas som utformade med följande:
            <ul>
                <li>Moduler</li>
                <li>Inskrivna elever</li>
                <li>Sessioner</li>
                <li>Utmärkelsetecken</li>
                <li>L1-feedback aktiverad</li>
                <li>Aviseringar</li>
                <li>Poäng för spelifiering</li>
                <li>QR-kod</li>
                <li>Tillägg för utbildningsväg</li>
            </ul>
            <td>
                <ul>
                    <li>Om antalet registreringar överskrider det fördefinierade tröskelvärdet kommer ALM inte att visa antalet. det kommer att ersätta räkningen med en ikon, som när du klickar på visar det faktiska antalet elever och en länk som tar dig till sidan Elever.</li>
                    <li>Antalet anmälningar kommer att visas i ett ungefärligt format. Till exempel, om antalet är mer än 50 000, kommer antalet att visas som 50K+ på kursnivå.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Sidan Admin- Elever</td>
            <td>
                    <ul>
                        <li>Listan över elever visas för varje instans.</li>
                        <li>Du kan söka efter en användare eller användargrupp som är inskriven på en kurs.</li>
                        <li>Den exporterade rapporten består inte av något filter för användargrupp.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Valet av instans är inaktiverat.</li>
                    <li>Ladda ned elevlista laddar också ned samma data förutom i ett fall. Om du söker efter en användargrupp och sedan väljer Ladda ned elevlista kommer den att ladda ned användargruppsdata.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Admin- L1/L3 feedbacksida</td>
            <td>
                <p>Ingen förändring i det befintliga beteendet</p>
            </td>
            <td>
                <ul>
                    <li>Valet av instans är inaktiverat.</li>
                    <li>Om inskrivningen till en kurs är över 50K, listar ALM inte elever och visar endast sökfältet. Om registreringen är mindre än 50K visar ALM både elevlista och sökfält.</li>
                    <li>Listning är inaktiverat som standard.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Admin- Sida för närvaro och poängsättning</td>
            <td>
                <p>Ingen förändring i det befintliga beteendet</p>
            </td>
            <td>
                <ul>
                    <li>Valet av instans inaktiveras när du söker efter en användare.</li>
                    <li>Om antalet användare till exempel överstiger 50 000 visas ytterligare ett meddelande om att ladda ned data för en mer detaljerad analys senare. Sökfältet är nu framträdande och visar en användare i formatet Namn, e-post | UUID.</li>
                    <li>Om antalet användare i användargruppen är färre än 10 000 oavsett registrering kan du utföra enskilda åtgärder på användarnivå tillsammans med åtgärder på gruppnivå. I det här fallet inaktiveras inte listan över användare.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Admin- L2 Quiz Resultatsida</td>
            <td>
                    <ul>
                        <li>Användarsökning implementeras också.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Användarsökning implementeras också. Medan typeahead-sökningar på LO-nivå filtreras listan till den valda instansen.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Sidan Admin- Användare (internt, externt)</td>
            <td>
                    <ul>
                        <li>E-post-ID:t visas när du söker efter en användare.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Om antalet användare till exempel överstiger 50 000 visas ytterligare ett meddelande om att ladda ned data för en mer detaljerad analys senare. Sökfältet är nu framträdande och visar en användare i formatet Namn, e-post | UUID.</li>
                    <li>På sidan Användarrensning har vi tagit bort sorteringsfunktionen för borttagna användare på **Datum raderad**. Du kan bara sortera på UUID:erna.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Instruktörer - Inlämning</td>
            <td>
                    <ul>
                        <li>Sidnumrering av moduler som ska lämnas in.</li>
                        <li>Som lärare kan du nu filtrera filinlämningar från elever baserat på status, avslutande granskning, väntar på inlämning, godkänd och misslyckad. </li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Du kan bara söka efter användare, inte användargrupper i det fallet.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Räkna med förhandsgranskning som elevsida</td>
            <td>
                    <ul>
                        <li>Antalet inkluderar data från registrering av högre ordning.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Antal exkluderar data från registreringar med högre ordning.</li>
                </ul>
            </td>
        </tr>
    </tbody>
</table>

## Avancerade sökfunktioner

I den här versionen har vi förbättrat sökupplevelsen. Sökresultaten hämtas inte bara baserat på metadata, utan även semantisk sökning och innehållssökning för att härleda resultat baserat på precision, aktualitet och relevant innehåll.

Den här ändringen återspeglar följande:

* Katalog och sidan Min utbildning: Hovringsåtgärden för kurs, utbildningsväg och certifiering har tagits bort.
* Utseendet på sökfältet.
* Filtertaggar har lagts till i utbildningsappen.

Om du vill aktivera sökfunktionerna kontaktar du CSAM-teamet på Adobe Learning Manager.

## Ändringar i användargränssnittet {#ui-changes}

### Sida för att skapa kurser

När du mappar kurserna till en färdighetsnivå är listan över färdigheter först sökbar. Med andra ord, sök efter färdigheter, så visas en lista över färdigheter som matchar den sökta termen.

### Användargrupper

#### Administratör: Sidan Elever

När du söker efter en användare laddar **alternativen Ladda ner elev** och **Exportera** ner samma rapport. Under tiden, när du söker efter en användargrupp, kan du nu ladda ner filtrerade användare från den användargruppen. När du söker efter en användargrupp ändras listan **Ladda ned elev** till **Ladda ned elevlista för användargrupp** Alternativet **Exportera** laddar ned hela listan igen.

## Ändringar i rapporter

* Kolumnerna Taggar och Färdigheter i Utbildningsrapporten ändras till Tagg och Färdigheter.
* Lade till rapporten [Gamification Audit Trail](administrators/feature-summary/reports.md#gamification-audit-trail).
* Om ett konto innehåller fler än 280000 elever som tilldelats en färdighet laddas färdighetsinlärningsrapporten ned som en zippad csv.
Om kontot har färre än 250000 elever laddas samma rapport ned som en CSV-fil.
På sidan Admin väljer du **Admin** > **Skills** > **Skill** > **Learners**. Rapporten laddas ned som CSV.
* Rapporten [](administrators/feature-summary/reports.md#session-summary-report) Sessionssammanfattning har två nya kolumner – Platsinformation och Platsregion.

## Ändringar i skapandet av klassrum

Baserat på [administratörsinställningar](administrators/feature-summary/classroom.md#classroom-settings) kan [du som författare skapa, ändra och ta bort platser](administrators/feature-summary/classroom.md#add-classroom-location).

>[!NOTE]
>
>När du lägger till plats- och katalogetiketter ser författare (på sidan för att skapa kurser) och administratörer (på instanssidan) en automatiskt ifylld lista över platser respektive katalogetiketter.

Som administratör kan du tillämpa begränsningar för en författare att ändra eller ta bort en klassrumsplats. Visa [inställningarna](administrators/feature-summary/classroom.md#classroom-settings) för Classroom om du vill ha mer information.

## Ändringar av flexibel utbildningsväg

Alla konton (gamla och nya) kommer att börja inkludera tidsgräns för registrering, tidsgräns för avregistrering och platsgräns i Learner-appen för en flexibel utbildningsväg.
Elever kommer nu att kunna anmäla sig till Flexibel utbildningsväg utan att välja någon instans av kursen.

## Ny utlösare för utbildningsplaner

En ny utlösare har lagts till på inställningssidan för utbildningsplanen. Författare och administratörer kommer nu att kunna utlösa åtgärder när en elev misslyckas med en modul i en kurs.

Visa [utbildningsplaner](administrators/feature-summary/learning-plans.md) för mer information.

## Ny inlämningsstatus

Som lärare kan du nu filtrera filinlämningar från elever baserat på status, avslutande granskning, väntar på inlämning, godkänd och misslyckad.

Visa [sändningsstatus](instructors/feature-summary/learners.md#filter-file-submissions) för mer information.

## Förbättringar av checklistor

I mars 2024-versionen av Adobe Learning Manager är förbättringarna av arbetsflödet för checklistan följande:

### Tillåt inte förlopp för att misslyckas med en checklista

När du skapar en checklista kan en författare välja **Aktivera** i avsnittet Obligatorisk checklista. Om du gör det förhindrar du att en elev fortsätter i modulen om de misslyckas med checklistan. De kan bara fortsätta om de klarar checklistan.

Checklistans granskare, det vill säga instruktörer eller chefer, kan sedan kontrollera checklistans status. Granskare kan också granska en elevs checklista i fel ordning.

### Omvärdering av en checklista

När du skapar en checklista kan en författare välja **Aktivera** i avsnittet Omvärdering. Genom att göra det kan en chef eller instruktör omvärdera en elev tills de klarar checklistan.

Om modulen är obligatorisk är kryssrutan för omvärdering markerad som standard.

En instruktör eller chef kan också ändra statusen för en checklista från Misslyckad till Godkänd när omvärdering är aktiverad.

På sidan Checklista kan en lärare se antalet elever i väntande tillstånd. Som instruktör kan du utvärdera en elev och godkänna eller underkänna dem. Om en elev är i ett misslyckat tillstånd kan du bara visa checklistan när omvärdering inte är aktiverad.

Det innebär att **kryssrutan Aktivera inte var markerad i avsnittet Omvärdering** när checklistan skapades. Om den här kryssrutan är markerad kan du se knappen Visa/Omvärdera på sidan Checklista för lärare.

Genom att välja knappen kan du omvärdera en elev och markera dem som godkända eller misslyckade.

>[!NOTE]
>
>Båda dessa funktioner - Omvärdering och Att göra checklista som obligatorisk - gäller endast för nyskapade moduler. När en kurs väl är publicerad kan dessa inte slås på/av.


Visa [Skapa en checklista](authors/feature-summary/courses.md#checklist-fail) för mer information.

## Andra förbättringar

### Sessionsrelaterade e-postaviseringar

I tidigare versioner av Adobe Learning Manager fick en elev inte sessionsrelaterade e-postmeddelanden, uppdaterade sessionsuppgifter, sessionsinbjudningar och sessionspåminnelser när:

* Eleverna har slutfört en kurs,
* nya sessioner läggs till i en kurs, eller
* Det finns ändringar i befintliga sessioner.

I mars 2024-versionen av Adobe Learning Manager är följande nya ändringar:

* Sessionsinformation uppdaterad och sessionsinbjudan (för elev och lärare)
   * För framtida sessioner kommer e-postmeddelanden för **sessionsinformation att uppdateras**, **sessionsinbjudningar** för inskrivna elever och nuvarande lärare att fasas ut. För tidigare sessioner kommer e-postmeddelanden för **uppdaterade** sessionsuppgifter och **sessionsinbjudningar** för inskrivna elever och nuvarande lärare att förbli som de är.
* Påminnelser via e-post (för administratör och elev)
   * För framtida sessioner kommer endast **e-postmeddelanden med sessionspåminnelser** att skickas.

>[!NOTE]
>
>E-postmeddelandena är inte beroende av att sessionen och kursen är klar.


### Ändringar av AEM referenswebbplats

På en AEM referenswebbplats har vi lagt till stöd för att lägga till administratörsuppdateringstoken i Learner Access Token.

### Dölja inlämningar från lärare

Om en lärare inte vidtar någon åtgärd (godkänner eller avvisar) för inlämningen efter att eleverna har laddat upp sina filer med hjälp av arbetsflödet för filinlämning, döljs inlämnings-URL:en från vyn efter ett fördefinierat antal dagar. Kontakta CSAM-teamen i Adobe Learning Manager för att ställa in eller ändra antalet dagar.

### Ändringar i produktterminologin

Vi har lagt till kolumnerna *Instance* och *Learner* i vokabulären för produktterminologi.

### Ändringar i mobilappen

I den här versionen av mobilappen kan eleverna schemalägga och hantera försenade kurspåminnelser. Genom att klicka på en försenad påminnelse kan du komma åt följande alternativ:

* Avbryt
* Gå till kurs
* Påminn mig igen om 3 dagar
* Påminn mig igen om en vecka

På Android: Om du klickar på push-meddelandet kommer du till sidan Kursöversikt ****.
På iOS: Om du klickar på push-meddelandet kommer du till appens startsida. Detta är en känd begränsning i iOS.

### Ändringar av checklista i Learner-appen på Salesforce

Om en elev misslyckas med en checklista kan han eller hon inte gå vidare till nästa modul eller kurs. När kryssrutan Obligatorisk checklista är markerad kan eleven inte gå vidare i en kurs om han eller hon inte klarar checklistan.

Precis som med webbappen, om en elev misslyckas med en checklista i Salesforce-appen, kommer de att se ett meddelande och kommer inte att gå vidare.

### Ändringar i Connect VC

I aktuella versioner av Adobe Learning Manager markeras en elev som **Inte närvarande** när han eller hon är registrerad för en Connect VC-session, men inte uppfyllde slutförandekriterierna.

I den här versionen ändras statusen till **Har ännu inte markerats**.

### Vit etikettering i Adobe Learning Manager

Mobilappen Adobe Learning Manager har nu stöd för vit märkning, vilket innebär att du nu kan lansera appen under ditt eget varumärke.

Visa vit märkning i [Adobe Learning Manager-mobilappen](white-label.md) för mer information.

### Ny kolumn i CSV:er för migrering

I den här versionen finns det en ny, valfri kolumn, uniqueLoId, i följande CSV:er för migrering.

* certification.csv
* course.csv
* learning_program.csv

>[!NOTE]
>
>Kolumnen **uniqueLoId** är valfri.


Om du utför en migrering för att uppdatera en befintlig kurs eller utbildningsplan eller certifiering läggs kursen eller utbildningsplanen eller certifieringen med **de unika LOId-filerna** till i författarappen.

När du migrerar måste du uppdatera uniqueLOId-värdena **** i CSV:erna för kursen eller utbildningsplanen eller certifieringen, även om det är en valfri kolumn.

Om uniqueLoIId-kolumnen **** inte läggs till innan du utför migreringen medan du uppdaterar den befintliga kursen eller utbildningsplanen eller certifieringen som har **uniqueLOId-värden**, kommer uniqueLOId-värdena **att åsidosättas med NULL-värden efter migreringen**.

>[!NOTE]
>
>Kolumnen, **uniqueLoId**, gäller inte för CSV-filen för jobbhjälp.


>[!IMPORTANT]
>
>Kolumnvärdena måste vara unika för hela kontot. Du kan inte använda samma värde med en kurs eller certifiering.

Ladda ned CSV:erna från migreringshandboken[](integration-admin/feature-summary/migration-manual.md#csv-specifications-and-sample-csvs).


### Betyg för appar

En elev kan ge sin feedback om Adobe Learning Manager-appen för att ytterligare förbättra appupplevelsen. Om eleven ger betyget fyra stjärnor eller mer visas ett popup-fönster som ber eleven att betygsätta appen i Play Store eller App Store.

### Bluejeans har nått slutet av sin livslängd (EOL) i februari 2024

Vi vill informera dig om att Bluejeans har nått slutet av sin livslängd (EOL) i februari 2024. Efter februari 2024 kommer Bluejeans inte längre att få uppdateringar eller support. Våra CSAM- och supportteam hjälper dig med alla frågor eller funderingar du kan ha under denna övergångsperiod.

Visa [Connectors i Adobe Learning Manager](integration-admin/feature-summary/connectors.md) om du vill ha mer information om hur du konfigurerar kopplingar.

### Ändringar i rapporten Inloggningsåtkomst

Rapporten Inloggningsåtkomst kommer endast att vara tillgänglig för de senaste fem kvartalen. Om någon integrationsadministratör begär nedladdning på begäran av den enhetliga exporten med **inloggningsåtkomst** markerad visas ett felmeddelande i Adobe Learning Manager. Det finns dock ingen inverkan på andra rapporter.

### Ändringar i ADFS

Fälten Employee Type (Anställningstyp) och Anställnings-ID (Anställnings-ID) från ADFS är nu tillgängliga i Adobe Learning Manager, baserat på mappningarna.

## API-ändringar i den här versionen

### API:er för elever

I den här versionen har vi lagt till API-stöd för elever så att de kan visa varumärkeslogotypen och anpassade teman på användargruppsnivå.

API:erna /account och /user?include=account returnerar fyra fält som åsidosätts specifikt för det aktiva fältet för användaren tillhör logoUrl, logoStyling och themeData.

### Nya attribut

Ett nytt attribut, isExpiredSubmission, i learningObjectResource, som visar om inlämningen i resursen har upphört att gälla eller inte.

* GET /account API: Returnerar det nya attributet **expireSubmissionDuration** X, där X är antalet dagar som angetts. Om det inte anges returneras 0
* GET /LO API med resursen innehåller det nya attributet **isExpiredSubmission**&quot; Sant eller Falskt.
   * True, om överföringen har upphört att gälla och &quot;submissionUrl&quot; inte visas.
   * Om det är falskt har överföringen inte upphört att gälla och &quot;submissionUrl&quot; hämtas.

### API-ändringar i checklista

En kurs kan bestå av flera moduler varav Checklista är en typ av modul. Den här checklistemodulen utvärderas av läraren och kan markeras som Misslyckad eller Lyckad baserat på utvärdering.

Men i båda fallen markeras checklistans status som Slutförd och på så sätt markeras kursen som Slutförd.

I den här versionen innehåller LO-API:et parametern *isChecklistMandatory*. Om värdet är True är checklistan obligatorisk.

### Stöd för flera språk

En administratör kan nu ladda ned L1-feedbackrapporten på det språk som han eller hon väljer. Du kan dock inte ladda ned L1-feedbackrapporter för Power BI ännu. I API-begäran använder du parametern preferredLocale för att ange valfritt språk.

### Ändringar i antalet instanssammanfattningar

Detta gäller för konton där registreringarna för en Classroom/VC-kurs är fler än 1000.

Om antalet är färre än 1000 ogiltigförklarar registreringarna cachen och returnerar de uppdaterade värdena i ett GET Summary API-anrop, till exempel antal registreringar, slutförande och seatLimit.

Om kontot är aktiverat för den här funktionen och antalet registreringar är fler än 1000 hämtas värdena från cachen.

### Föråldrade sökvägar

För närvarande följer Learning Manager API:er en diagramdatastruktur, vilket gör att du kan hämta data genom att bläddra i API-modellen genom inkluderingar. Även om du kan gå igenom ett API upp till sju nivåer är det beräkningsmässigt dyrt att hämta data med ett enda API-anrop.

Vi rekommenderar att alla befintliga och nya kunder ringer små samtal flera gånger i stället för ett stort samtal. Den här metoden förhindrar att oönskade data läses in i samtalet.

#### Vilka sökvägar är inaktuella?

Följande sökvägar är inaktuella:

* /learningObjects
   * Föråldrade sökvägar:
      * enrollment.loInstance.loResources.resources
      * instances.loResources.resources
   * Befintliga sökvägar:
      * enrollment.loInstance
      * instances.loResources
* /lärandeobjekt/{id}
   * Inaktuell sökväg:
      * enrollment.instances.subLoInstances.learningObject
   * Befintlig sökväg:
      * enrollment.instances.subLoInstances
* /Antagning
   * Inaktuell sökväg:
      * loInstance.learningObject.enrollment
   * Ny sökväg:
      * loInstance.learningObject
* /lärandeobjekt/{id}
   * Inaktuell sökväg:
      * instance.subLoInstances.learningObject.enrollment.loResourceGrades
   * Ny sökväg:
      * instance.subLoInstances

### Ändringar i arkivering av inloggningsåtkomst och användargranskningsrapport för jobb-API

Med den här versionen kommer jobb-API:et att behålla inloggningsåtkomstrapporten upp till fem kvartal och användargranskningsrapporten i sex månader. Om du vill ladda ned data som är äldre än den här tidsperioden måste du skicka arkivparametern och ange kvartal och år. Se exempelnyttolasten.

```
{
    "data": {
        "type": "job",
        "attributes": {
            "description": "description of your choice",
            "jobType": "generateLoginAccessReport",
            "payload": {
                "fromDate": "2023-04-01T18:30:00.000Z",
                "toDate": "2023-04-30T18:30:00.000Z",
                "archive": {
                    "quarter": "4",
                    "year": "2021"
                }
            }
        }
    }
}
```

Om du försöker ladda ned rapporten Inloggningsåtkomst **** som sträcker sig längre än fem kvartal visas ett felmeddelande. Ett liknande felmeddelande visas om du försöker ladda ned rapporten för **användargranskning** som går längre än sex månader.

### Inaktuella API:er

Visa [API-utfasningar i Adobe Learning Manager](api-deprecations-list.md) för en kumulativ lista över alla inaktuella API:er i produkten.

## Buggar åtgärdade i den här uppdateringen {#bug-fixes}

* När en elev är inskriven på en kurs och sedan försöker skriva in sig på en annan kurs visas ett varningsmeddelande.
* En användargrupp visas i Sök även efter att den har tagits bort.
* När användare utlöser många Learner Transcripts med en stor mängd data blockeras Learner Transcripts-kön och förhindrar en ny begäran.
* Om ett barnkonto begär att dess föräldrakonto ska dela en rapport kan föräldrakontot inte göra det.
* URL:erna från en kurs och en Utbildningsväg omdirigeras till felaktiga platser.
* En elev visar ibland kursinstansen för en annan kurs när han eller hon klickar på kurslänken på katalogsidan.
* Knappen Avregistrera **** visas inte som förväntat efter den första registreringen, men knappen visas efter en uppdatering.
* Du kan inte spara Innehåll eller ett quiz som har ett tomt utrymme i namnet.
* I kurser som godkänts av chefer kan du skriva in elever i en användargrupp på nytt.
* I vissa fall, om du försöker lägga till ytterligare ett aktivt fält, visas felmeddelandet &quot;Aktiva fält kunde inte sparas.&quot;.
* Texten flödar över i namnet på en kurs i ett kurskort i avsnittet Relaterade kurser.
* När du har växlat en instans och registrerat en elev i instansen finns de gamla instanserna fortfarande i Outlook-kalendern.
* När en elev från ett kamratkonto försöker välja miniatyren för en kurs visas ett felmeddelande.
* När elever anmäler sig till en kurs får de flera aviseringar om inskrivningen.
* Om en användare manuellt ändrar namnet på de kataloger som skapats i en anslutning skapas nya kataloger och kurserna publiceras i de felaktiga katalogerna.
* Användare som tillhör inaktiva konton får fortfarande e-postmeddelanden om prenumerationer.

### API-relaterade buggfixar

* API:et GET/users hämtar inte information om en Manager.
* I ett konto skapades användare genom en schemalagd FTP-användarimport under ett schemalagt driftstopp.
* När du har tagit bort eller dragit tillbaka en kursomgång och valt nästa aktiva instans **i mobilappen eller det immersiva läget visas knappen Registrera intresse** i stället för **Anmäl** dig.
* När en elev från ett kamratkonto försöker välja miniatyrbilden för en kurs med hjälp av Learning Object API visas felet 403 Förbjudet.

## Systemkrav

Visa [systemkrav för](system-requirements.md) Adobe Learning Manager.

## Tidigare versioner av Adobe Learning Manager

* [Version från november 2023](whats-new-november-2023.md)
* [Version från juli 2023](whats-new-2023-july.md)
