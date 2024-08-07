---
description: Läs om de nya funktionerna och förbättringarna i mars 2024-utgåvan av Adobe Learning Manager
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

Läs om de nya funktionerna och förbättringarna i mars 2024-versionen av Adobe Learning Manager.

Utforska några av de senaste Adobe Learning Manager-funktionerna, till exempel:

1. Importera kompetenser från externa källor
1. Stöd för flera varumärken
1. Modul för omvärdering av checklista-aktivitet
1. Vitmärkt app för mobil inlärning

>[!NOTE]
>
>Titta på det här [webbseminariet](https://learningmanager.adobe.com/app/learner?accountId=98632#/course/9212121) om du vill veta mer om de nya funktionerna i den här versionen.


## Nyheter i den här versionen {#whatsnewandchanged}

### Importera kompetenser från externa källor

Importera kunskaper från innehållsleverantörer, till exempel LinkedIn och Go1, genom att använda respektive kopplingar. Denna förbättring är en del av målet mot Learning Managers förmåga att integrera med externa Skills Clouds och Talent Management Systems. De importerade kunskaperna läggs till i de administratörsdefinierade kunskaperna i Learning Manager och kommer att vara tillgängliga för författare under arbetsflödet för att skapa kursen. Förbättringar har också gjorts i kompetenssökningsfunktionen på hela plattformen för att ge en bättre sökupplevelse när kontot har ett stort antal färdigheter.

Visa [Importera kompetenser](administrators/feature-summary/import-skills-external-sources.md) om du vill veta mer.

### Anpassad varumärkning

Du kan nu anpassa vissa användargränssnittselement - organisationsnamnet, logotypen och användargränssnittstemat baserat på de användargrupper som är tillgängliga på kontot. En organisation med flera avdelningar kan till exempel ställa in en anpassad logotyp och ett användargränssnittstema som ska visas för varje avdelning.

>[!NOTE]
>
>Funktionen för flera varumärken gäller inte administratörsvyn. De ser alltid varumärken på organisationsnivå i sina konton. Det beror på att det här är en funktion som är riktad till elever och att administratörer kanske inte vill ha den på sina konton.

Visa [Flera anpassade varumärken](administrators/feature-summary/themes.md#multiple-branding) om du vill ha mer information.


## Ändringar för konton med stor användarbas

### Admin - sidor för kurs eller utbildningsväg

Om ett stort antal elever är registrerade på kursen, till exempel fler än 50 000, visas listan med elever inte. Du kan antingen söka efter en elev i sökfältet *Sök elever* eller välja länken **Hämta** längst upp i sökfältet för att hämta listan över elever.

### Admin - sidan Elever

När du söker efter en användare hämtar alternativen **Hämta elev** och **Exportera** samma rapport. Under tiden kan du när du söker efter en användargrupp hämta filtrerade användare från den användargruppen. När du söker i en användargrupp
**Hämta elevlistan** ändras till **Hämta elevlistan för användargruppen** Alternativet **Exportera** hämtar hela listan igen.

### Administratör - sidan Användare

#### Interna användare

Om antalet användare överstiger t.ex. 50 000 visas ett meddelande om att hämta data för en mer detaljerad analys senare. Sökfältet är nu framträdande och visar en användare i formatet *Namn, e-post | UUID*.

>[!NOTE]
>
>UUID visas bara om UUID är aktiverat för kontot.

#### Externa användare

För externa användare gäller samma beteende. Om antalet användare är stort kan du hämta användarna och även hämta information om en användare efter en sökning i formatet *Namn, e-post | UUID*.

#### Sidan Användarrensning

På sidan Användarrensning har vi tagit bort sorteringsfunktionen **Datum borttagen** för borttagna användare. Du kan bara sortera på UUID:n.

### Admin - instanssidor

#### Kurs eller utbildningsväg

Om antalet registreringar är stort visar Adobe Learning Manager inte antalet elever. Istället kommer det att finnas en ikon, som du kan välja och visa antalet elever och gå till sidan Elever.

Antalet elever visas som ett ungefärligt värde. Om antalet elever till exempel är fler än 50 000 visas värdet som 50K+.

### Admin - L1/L3-sidor

Om antalet kursregistreringar är stort på sidan L1-feedback visas listan med elever inte. Du kan i stället exportera användarlistan för en mer detaljerad analys senare.

Sökningen stöder kommande text och resultaten är begränsade till den markerade instansen.

#### Närvaro och poäng

När du söker efter en användare på sidan utförs sökningen i alla tillgängliga instanser. Resultatet är för den markerade instansen.

Om du på sidan Närvaro söker efter en användargrupp och antalet användare överstiger 10 000 i användargruppen oavsett registrering, kan du bara utföra åtgärder på gruppnivå. Du kan inte se listan över användare.

Om antalet användare i användargruppen är färre än 10 000 kan du utföra enskilda åtgärder på användarnivå tillsammans med åtgärder på gruppnivå. I det här fallet är listan över användare inte inaktiverad.

### Admin - sidan Certifieringar

Om det finns ett stort antal användare som är registrerade för en certifiering i de aktuella versionerna av Adobe Learning Manager kan du inte visa avregistrerade elever eftersom listrutan **Status** är inaktiverad.

Om antalet registrerade användare är stort i den här versionen av Adobe Learning Manager visas bara två alternativ i listrutan **Status** - **Registrerade** och **Avregistrerade**. Alternativet **Registrerad** är valt som standard. Om du väljer **Avregistrerade** visas listan med avregistrerade elever.

#### Ändringar i användargrupper

Om antalet användare i användargruppen är färre än, till exempel 50 000, visas alla alternativ i listrutan **Status** - Certifierad, Tilldelad och Utgående.

Om antalet användare i en användargrupp är stort visas bara två alternativ i listrutan **Status** - **Registrerade** och **Avregistrerade**, enligt den nya designen.

### Jämförelsetabell

<table>
    <tbody>
        <tr>
            <td><b>Sida</b></td>
            <td><b>Före tröskeländring</b></td>
            <td><b>Efter tröskeländring</b></td>
        </tr>
        <tr>
            <td>Admin - kursinstans</td>
            <td>Instanser visas som om de vore utformade med följande:
            <ul>
                <li>Moduler</li>
                <li>Elever registrerade</li>
                <li>Sessioner</li>
                <li>Utmärkelsetecken</li>
                <li>L1-feedback aktiverad</li>
                <li>Aviseringar</li>
                <li>Spelifieringspunkter</li>
                <li>QR-kod</li>
                <li>Tillägg för utbildningsväg</li>
            </ul>
            <td>
                <ul>
                    <li>Om antalet registreringar överskrider det på förhand angivna tröskelvärdet visar ALM inte antalet utan ersätter antalet med en ikon som visar det faktiska antalet elever och en länk för att ta dig till sidan Elever när du klickar på den.</li>
                    <li>Antalet registreringar visas i ungefärligt format. Om siffran till exempel är högre än 50 000 visas antalet som 50 K+ på kursnivån.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Admin - sidan Elever</td>
            <td>
                    <ul>
                        <li>Listan med elever visas för varje instans.</li>
                        <li>Du kan söka efter en användare eller användargrupp som är registrerad på en kurs.</li>
                        <li>Den exporterade rapporten innehåller inget filter för användargrupp.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Markeringen av instansen är inaktiverad.</li>
                    <li>Hämta elevlistan hämtar också samma data förutom ett fall. Om du söker efter en användargrupp och sedan väljer Hämta elevlista kommer den att hämta användargruppsdata.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Admin - L1/L3-feedbacksida</td>
            <td>
                <p>Ingen förändring i befintligt beteende</p>
            </td>
            <td>
                <ul>
                    <li>Markeringen av instansen är inaktiverad.</li>
                    <li>Om registreringen till en kurs är högre än 50 000 listas inte elever i ALM och endast sökfältet visas. Om registreringen är mindre än 50 000 visas både elevlista och sökfält i ALM.</li>
                    <li>Listan är inaktiverad som standard.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Administratör - sida för närvaro och poäng</td>
            <td>
                <p>Ingen förändring i befintligt beteende</p>
            </td>
            <td>
                <ul>
                    <li>Val av instans inaktiveras när en användare söks.</li>
                    <li>Om antalet användare överstiger, till exempel, 50 000, kommer det att finnas ett extra meddelande för att ladda ner data för en mer detaljerad analys senare. Sökfältet är nu framträdande och visar en användare i formatet Namn, E-post | UUID</li>
                    <li>Om antalet användare i användargruppen är färre än 10 000 oavsett registrering kan du utföra åtgärder på enskild användarnivå tillsammans med åtgärder på gruppnivå. I det här fallet är listan över användare inte inaktiverad.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Admin - L2 quiz-poängsida</td>
            <td>
                    <ul>
                        <li>Även användarsökning implementeras.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Även användarsökning implementeras. När skrivhuvudet söks på LO-nivå filtreras listan till den markerade instansen.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Administratör - sidan Användare (intern, extern)</td>
            <td>
                    <ul>
                        <li>E-post-ID visas när du söker en användare.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Om antalet användare överstiger, till exempel, 50 000, kommer det att finnas ett extra meddelande för att ladda ner data för en mer detaljerad analys senare. Sökfältet är nu framträdande och visar en användare i formatet Namn, E-post | UUID</li>
                    <li>För borttagna användare på sidan Användarrensning har vi tagit bort sorteringsfunktionen den **Borttaget**. Du kan bara sortera på UUID:n.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Instruktörer - ansökan</td>
            <td>
                    <ul>
                        <li>Sidnumrering av moduler som ska lämnas in.</li>
                        <li>Instruktörer kan nu filtrera filansökningar från elever baserat på status, slutar på granskning, väntar på inlämning, godkändes och misslyckades. </li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Du kan bara söka efter användare, inte användargrupper i den instansen.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Räkna med förhandsgranskning som elevsida</td>
            <td>
                    <ul>
                        <li>Antal inkluderar data från registrering av högre order.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Antal exkluderar data från registreringar av högre order.</li>
                </ul>
            </td>
        </tr>
    </tbody>
</table>

## Avancerade sökfunktioner

I den här versionen har vi förbättrat sökfunktionen. Sökresultaten hämtas inte bara utifrån metadata utan också semantisk och innehållsrik sökning för att få resultat baserade på precision, aktuell information och relevant innehåll.

Ändringen gäller följande:

* Katalog och Min utbildningssida: hovringsåtgärden för kurs, utbildningsväg och certifiering har tagits bort.
* Utseendet på sökfältet.
* Filtertaggar har lagts till i utbildningsappen.

Kontakta Adobe Learning Manager CSAM-team om du vill aktivera sökfunktionerna.

## Ändringar i användargränssnittet {#ui-changes}

### Sida för att skapa kurs

När du mappar kurserna till en kompetensnivå visas listan med kompetenser med sökförst. Med andra ord, sök färdigheter, och du kommer att se en lista över färdigheter som matchar söktermen.

### Användargrupper

#### Administratör: sidan Elever

När du söker efter en användare hämtar alternativen **Hämta elev** och **Exportera** samma rapport. Under tiden kan du när du söker efter en användargrupp hämta filtrerade användare från den användargruppen. När du söker i en användargrupp ändras listan **Hämta elevlista** till **Hämta elevlista för användargrupp** Alternativet **Exportera** hämtar hela listan igen.

## Ändringar i rapporter

* Kolumnerna Taggar och Kompetens i rapporten Utbildningar har ändrats till Tagg och Kompetenser.
* Granskningsspåret [Spelifiering](administrators/feature-summary/reports.md#gamification-audit-trail) har lagts till.
* Om ett konto innehåller fler än 280000 elever som har tilldelats en kompetens hämtas rapporten om kompetensen-eleven som en zippad CSV-fil.
Om kontot har färre än 250000 elever hämtas samma rapport som en CSV-fil.
På sidan Admin väljer du **Admin** > **Kompetenser** > **Kompetens** > **Elever**. Rapporten hämtas i CSV-format.
* [Sessionssammanfattningsrapporten](administrators/feature-summary/reports.md#session-summary-report) har två nya kolumner - Platsinformation och Platsregion.

## Ändringar i skapandet av klassrum

Enligt [administratörsinställningarna](administrators/feature-summary/classroom.md#classroom-settings) kan du som författare [skapa, ändra och ta bort platser](administrators/feature-summary/classroom.md#add-classroom-location).

>[!NOTE]
>
>När du lägger till plats- och katalogetiketter visas en automatiskt ifylld lista med platser och katalogetiketter för författare (på sidan för att skapa kurs) och administratörer (på instanssidan).

Du som är administratör kan tillämpa begränsningar för en författare så att hen kan ändra eller ta bort en klassrumsplats. Visa [klassrumsinställningar](administrators/feature-summary/classroom.md#classroom-settings) om du vill ha mer information.

## Förändringar av flexibel utbildningsväg

Alla konton (gamla och nya) i börjar inklusive registreringsdeadline, deadline för avregistrering och platsgräns i elevappen för en flexibel utbildningsväg.
Elever nu kommer att kunna registrera sig för en flexibel utbildningsväg utan att välja någon instans av kursen.

## Ny utlösare för utbildningsplaner

En ny utlösare har lagts till på inställningssidan för utbildningsplanen. Författare och administratörer kan nu utlösa åtgärder när en elev misslyckas med en modul i en kurs.

Titta i [utbildningsplaner](administrators/feature-summary/learning-plans.md) om du vill ha mer information.

## Ny inlämningsstatus

Instruktörer kan nu filtrera filansökningar från elever baserat på status, slutar på granskning, väntar på inlämning, godkändes och misslyckades.

Se [Överföringsstatus](instructors/feature-summary/learners.md#filter-file-submissions) för mer information.

## Förbättringar av checklista

I mars 2024-versionen av Adobe Learning Manager har följande förbättringar gjorts i arbetsflödet för checklistan:

### Tillåt inte förlopp när en checklista misslyckas

När en checklista skapas kan en författare välja **Aktivera** i avsnittet Obligatorisk checklista. Detta förhindrar en elev från att fortsätta i modulen om hen inte uppfyller checklistan. De kan bara fortsätta om de klarar checklistan.

Checklistegranskarna, dvs. instruktörer eller chefer, kan sedan kontrollera checklistans status. Granskare kan också granska en elevs checklista i fel ordning.

### Omprövning av checklista

När du skapar en checklista kan en författare välja **Aktivera** i avsnittet Utvärdering. Om du gör det kan en chef eller instruktör utvärdera en elev på nytt tills de godkänns i checklistan.

Om modulen är obligatorisk är kryssrutan för ny utvärdering markerad som standard.

En instruktör eller chef kan också ändra statusen för en checklista från Misslyckad till Godkänd när omutvärdering är aktiverad.

På sidan Checklista kan en instruktör se antalet elever i läget Väntande. Du som är instruktör kan utvärdera en elev och godkänna eller underkänna den. Om en elev är i ett misslyckat tillstånd kan du bara visa checklistan när omvärdering inte är aktiverad.

Det innebär att kryssrutan **Aktivera** inte markerades i avsnittet Omvärdering när checklistan skapades. Om den här kryssrutan är markerad kan du se knappen Visa/omutvärdera på sidan Checklista för instruktör.

Genom att välja knappen kan du omvärdera en elev och markera den som godkänd eller ej godkänd.

>[!NOTE]
>
>Båda dessa funktioner - omvärdering och att göra checklistan obligatorisk - gäller endast nya moduler. När en kurs har publicerats kan den inte slås på/av.


Visa [Skapa en checklista](authors/feature-summary/courses.md#checklist-fail) om du vill ha mer information.

## Andra förbättringar

### Sessionsrelaterade e-postmeddelanden

I tidigare versioner av Adobe Learning Manager kunde en elev inte skicka sessionsrelaterade e-postmeddelanden, sessionsdetaljerna har uppdaterats, sessionsinbjudan och sessionspåminnelse när:

* Elever har slutfört en kurs,
* Nya sessioner läggs till i en kurs eller
* Befintliga sessioner har ändrats.

De nya ändringarna är följande i mars 2024-utgåvan av Adobe Learning Manager:

* Sessionsdetaljerna har uppdaterats och inbjudan till session (för elev och instruktör)
   * För framtida sessioner kommer e-postmeddelanden om **Sessionsdetaljer som har uppdaterats**, **Sessionsinbjudan** för registrerade elever och aktuella instruktörer att tas bort. För tidigare sessioner kommer e-postmeddelanden om **Sessionsdetaljer har uppdaterats** och **Sessionsinbjudan** för registrerade elever och aktuella instruktörer att förbli oförändrade.
* E-postpåminnelse (för administratör och elev)
   * För framtida sessioner skickas endast **Sessionspåminnelse** e-postmeddelanden.

>[!NOTE]
>
>E-postmeddelandena beror inte på om sessionen och kursen har slutförts.


### Ändringar i referenswebbplats för AEM

På en AEM-referensplats har vi lagt till stöd för att lägga till en administrativ uppdateringstoken till elevåtkomsttoken.

### Dölj bidrag från instruktörer

Om en instruktör inte vidtar någon åtgärd (godkänner eller avvisar) när en fil skickas, efter att eleverna har överfört sina filer med hjälp av arbetsflödet för inlämning, döljs inlämnings-URL:en i vyn efter ett fördefinierat antal dagar. Kontakta CSAM-teamen hos Adobe Learning Manager för att ange eller ändra antalet dagar.

### Ändringar i produktterminologi

Vi har lagt till kolumnerna *Instans* och *Elev* i terminologiordförrådet för produkten.

### Ändringar i mobilappar

I den här mobilappsversionen kan elever schemalägga och hantera påminnelser om försenade kurser. Om du klickar på en påminnelse som borde ha skickats för länge sedan kan du få tillgång till följande alternativ:

* Avbryt
* Gå till kurs
* Påminn mig igen om tre dagar
* Påminn mig igen om en vecka

På Android: Om du klickar på push-meddelandet dirigeras du till sidan **Kursöversikt**.
I iOS: Om du klickar på push-meddelandet dirigeras du till appens startsida. Detta är en känd begränsning i iOS.

### Checklisteändringar i elevappen i Salesforce

Om en elev misslyckas med en checklista kan hen inte fortsätta till nästa modul eller kurs. När kryssrutan Obligatorisk checklista är markerad kan eleven inte gå vidare i en kurs om hen inte lyckas med checklistan.

Om en elev, precis som med webbappen, misslyckas med att checka in ett Salesforce-program, ser hen ett meddelande och kommer inte att gå vidare.

### Ändringar i Connect VC

I aktuella versioner av Adobe Learning Manager har en elev markerats som **Inte närvarat** när hen registrerar sig för en Connect VC-session, men den uppfyllde inte slutförandevillkoren.

I den här versionen ändras statusen till **Ännu ej markerad**.

### Vit märkning i Adobe Learning Manager

Adobe Learning Manager-mobilappen stöder nu vit märkning, vilket innebär att du nu kan släppa appen under ditt eget varumärke.

Visa vit etikettering i [Adobe Learning Manager-mobilappen](white-label.md) om du vill veta mer.

### Ny kolumn i CSV-migreringsfiler

I den här versionen finns en ny, valfri kolumn, uniqueLoId, i följande migrerings-CSV-filer.

* certification.csv
* course.csv
* learning_program.csv

>[!NOTE]
>
>Kolumnen **uniqueLoId** är valfri.


Om du migrerar för att uppdatera en befintlig kurs eller utbildningsplan eller certifiering läggs kursen eller utbildningsplanen eller certifieringen med **uniqueLOId** s till i skaparappen.

Under migreringen måste du uppdatera värdena **uniqueLOId** i CSV-filerna för kurs- eller utbildningsplan eller certifiering, även om det är en valfri kolumn.

Om kolumnen **uniqueLoId** inte läggs till innan migreringen utförs när den befintliga kursen eller utbildningsplanen uppdateras eller om certifieringen har **uniqueLOId** s, kommer värdena för **uniqueLOId** att åsidosättas med NULL-värden efter migreringen.

>[!NOTE]
>
>Kolumnen **uniqueLoId** är inte tillämplig på CSV-filen för arbetsstöd.


>[!IMPORTANT]
>
>Kolumnvärdena måste vara unika för hela kontot. Du kan inte använda samma värde med en kurs eller certifiering.

Hämta CSV-filerna från [migreringshandboken](integration-admin/feature-summary/migration-manual.md#csv-specifications-and-sample-csvs).


### Appklassificering

En elev kan ge feedback om Adobe Learning Manager-appen för att ytterligare förbättra appupplevelsen. Om eleven ger fyra stjärnor eller mer visas ett popup-fönster där eleven uppmanas att betygsätta appen i Play Store eller App Store.

### Bluejeans har nått sitt slut i februari 2024

Vi vill informera dig om att Bluejeans har nått sitt slut (EOL) på Februari 2024. Efter februari 2024 kommer Bluejeans inte längre att få uppdateringar eller support. Våra CSAM- och supportteam hjälper dig med eventuella frågor eller funderingar under övergångsperioden.

I [Anslutningar i Adobe Learning Manager](integration-admin/feature-summary/connectors.md) finns mer information om hur du konfigurerar anslutningar.

### Ändringar i rapporten om inloggningsåtkomst

Rapporten för inloggningsåtkomst kommer bara att vara tillgänglig för de senaste fem kvartalen. Om någon integrationsadministratör begär hämtning på begäran av den enhetliga exporten med **inloggningsåtkomst** markerat, visar Adobe Learning Manager ett felmeddelande. Andra rapporter påverkas dock inte.

### ADFS-ändringar

Fälten Anställningstyp och Anställds-ID från ADFS är nu tillgängliga i Adobe Learning Manager, baserat på mappningarna.

## API-ändringar i den här versionen

### Elevens API

I den här versionen har vi lagt till API-stöd för elever för att visa varumärkets logotyp och personliga teman på användargruppsnivå.

API:erna /account och /user?include=account returnerar fyra fält som är åsidosatta och specifika för användarens aktiva fält. De tillhör logoUrl, logoStyling och themeData.

### Nya attribut

Ett nytt attribut, isExpiredSubmission, i learningObjectResource, som visar om överföringen i resursen har upphört att gälla eller inte.

* GETS-/konto-API: Returnerar det nya attributet **expireSubmissionDuration** X, där X är antalet angivna dagar. Om det inte anges returneras 0
* GET-/LO-API:t med resursen innehåller det nya attributet **isExpiredSubmission**, Sant eller Falskt.
   * Sant om inlämningen har upphört att gälla och &quot;submissionUrl&quot; inte visas.
   * Om värdet är Falskt har överföringen inte förfallit och &quot;submissionUrl&quot; har hämtats.

### API-ändringar i checklista

En kurs kan bestå av flera moduler varav Checklista är en typ av modul. Den här checklistmodulen utvärderas av instruktören och kan markeras som Misslyckad eller Lyckad baserat på utvärdering.

Men i båda fallen markeras checklistestatusen som Slutförd och på så sätt markeras kursen som Slutförd.

I den här versionen innehåller LO API parametern *isChecklistMandatory*. Om värdet är True är checklistan obligatorisk.

### Stöd för flera språk

En administratör kan nu hämta rapporten med L1-feedback på det språk han eller hon väljer. Du kan dock inte hämta L1-feedbackrapporter för Power BI än. I API-begäran använder du parametern preferredLocale för att ange önskat språk.

### Ändringar i antalet instanssammanfattningar

Detta gäller konton där registreringarna för en Classroom/VC-kurs överstiger 1 000.

Om antalet är färre än 1 000 gör registreringarna cachen ogiltig och returnerar de uppdaterade GETTERNA i ett API-anrop för värdesammanfattning, som antal registreringar, slutförande och SeatLimit.

Om kontot är aktiverat för den här funktionen och antalet registreringar är fler än 1 000, hämtas värdena från cacheminnet.

### Borttagna banor

För närvarande följer Learning Manager API:er en diagramdatastruktur, som gör att du kan hämta data genom att gå igenom API-modellen via inkluderingar. Även om du kan gå igenom ett API upp till sju nivåer, är det datormässigt dyrt att hämta data med ett enda API-anrop.

Vi rekommenderar att alla befintliga och nya kunder ringer små samtal flera gånger i stället för ett stort samtal. På så sätt förhindrar du att oönskade data läses in i samtalet.

#### Vilka sökvägar är inaktuella

Följande sökvägar har tagits bort:

* /learningObjects
   * Borttagna sökvägar:
      * enrollment.loInstance.loResources.resources
      * instances.loResources.resources
   * Befintliga sökvägar:
      * enrollment.loInstance
      * instances.loResources
* /learningObjects/{id}
   * Föråldrad sökväg:
      * enrollment.instances.subLoInstances.learningObject
   * Befintlig sökväg:
      * enrollment.instances.subLoInstances
* /enrollments
   * Föråldrad sökväg:
      * loInstance.learningObject.enrollment
   * Ny bana:
      * loInstance.learningObject
* /learningObjects/{id}
   * Föråldrad sökväg:
      * instance.subLoInstances.learningObject.enrollment.loResourceGrades
   * Ny bana:
      * instance.subLoInstances

### Ändringar i inloggningsåtkomst och användargranskningsrapport för jobb-API

I den här versionen kommer jobb-API att behålla inloggningsåtkomstrapporten upp till fem kvartal och användarens granskningsrapport i sex månader. Om du vill hämta data som är äldre än den här tidsperioden måste du skicka arkivparametern och ange kvartal och år. Se exempelnyttolasten.

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

Om du försöker hämta rapporten **Inloggningsåtkomst** som sträcker sig längre än fem kvartal visas ett felmeddelande. Ett liknande felmeddelande visas om du försöker hämta **användargranskningsrapporten** som sträcker sig längre än sex månader.

### Föråldrade API:er

Visa [API-borttagningar i Adobe Learning Manager](api-deprecations-list.md) om du vill ha en kumulativ lista över alla inaktuella API:er i produkten.

## Fel som är åtgärdade i den här uppdateringen {#bug-fixes}

* När en elev registreras till en kurs och sedan försöker registrera sig till en annan kurs visas ett varningsmeddelande.
* En användargrupp visas i Sök även efter att den har raderats.
* När användare utlöser många elevbetygsutdrag med stora mängder data blockeras elevens betygsutdrag och en ny begäran förhindras.
* Om ett underordnat konto begär att dess överordnade konto ska dela en rapport kan det överordnade kontot inte göra det.
* URL:erna från en kurs och en utbildningsväg omdirigeras till felaktiga platser.
* En elev visar periodvis kursinstansen för en annan kurs genom att klicka på kurslänken på katalogsidan.
* Knappen **Avregistrera** visas inte som förväntat efter den första registreringen, men knappen visas efter en uppdatering.
* Du kan inte spara Innehåll eller ett quiz-meddelande som har ett tomt utrymme i namnet.
* I chefsgodkända kurser kan du registrera elever i en användargrupp på nytt.
* Om du försöker lägga till ytterligare ett aktivt fält kan felmeddelandet &quot;Aktiva fält kunde inte sparas&quot; visas i vissa fall.
* Texten flödar över i namnet på en kurs i ett kurskort i avsnittet Relaterade kurser.
* Efter att ha bytt instans och registrerat en elev till instansen finns de gamla instanserna fortfarande kvar i Outlook-kalendern.
* När en elev från ett kollegialt konto försöker välja miniatyrbilden för en kurs visas ett felmeddelande.
* När elever registrerar sig för en kurs får de flera meddelanden om registreringen.
* Om en användare ändrar namnet på katalogerna som skapats i en koppling manuellt, skapas nya kataloger och kurserna publiceras i felaktiga kataloger.
* Användare som tillhör inaktiva konton får fortfarande prenumerationsmeddelanden via e-post.

### API-relaterade felkorrigeringar

* API-GETEN/användarna hämtar inte information om en chef.
* I ett konto har användarna skapats via en schemalagd FTP-användarimport under ett schemalagt driftstopp.
* I mobilappen eller immersivt läge visas knappen **Registrera intresse** i stället för **Registrera dig** när en kursinstans har raderats eller tagits ur bruk och nästa aktiva instans har valts.
* När en elev från ett kollegialt konto försöker välja miniatyrbild för en kurs med hjälp av API:et för utbildningsobjekt visas felet 403 Förbjudet.

## Systemkrav

Visa [Systemkrav för Adobe Learning Manager](system-requirements.md).

## Tidigare utgåvor av Adobe Learning Manager

* [November 2023-utgåvan](whats-new-november-2023.md)
* [Juli 2023-utgåvan](whats-new-2023-july.md)
