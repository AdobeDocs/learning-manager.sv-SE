---
description: Läs om de nya funktionerna och förbättringarna i oktober 2025-versionen av Adobe Learning Manager
jcr-language: en_us
title: Nyheter i Adobe Learning Manager oktober 2025-versionen
source-git-commit: b1225d4c1c322a75d97c813b0d97eb3229ffd35c
workflow-type: tm+mt
source-wordcount: '5540'
ht-degree: 0%

---


# Nyheter i Adobe Learning Manager oktober 2025-versionen

I oktober 2025-versionen av Adobe Learning Manager introduceras viktiga förbättringar som förbättrar rapporteringsnoggrannheten, utökar integreringsfunktionerna och förbättrar utbildningsupplevelsen för administratörer, författare och elever.

* Experience Builder: Designa varumärkesanpassade, rollbaserade utbildningsportaler som är anpassade till din organisations behov. Skapa varumärkta, rollbaserade utbildningsportaler med widgetar, menyer och sidor.
* Social taggning på inlärningstavlor: Elever kan nu tagga kollegor med @username i inlägg och kommentarer, vilket möjliggör riktat samarbete och riktade aviseringar inom sociala inlärningsgrupper.
* Behörigheter för meddelanden som omfattas: Anpassade administratörer kan skapa meddelanden som är begränsade till deras tilldelade användargrupper eller kataloger, vilket garanterar riktad kommunikation och minskar informationsöverbelastning.
* Språkbaserad framstegsspårning: Elevframsteg sparas nu oberoende för varje språk, vilket möjliggör sömlös växling mellan språk utan att förlora framsteg.
* Inkrementell hantering av anpassade roller: Administratörer kan nu hantera anpassade roller mer effektivt med stöd för inkrementell och multiinkrementell import i Adobe Learning Manager.
* Förbättrade API:er för analys och migrering: Nya och förbättrade API:er ger bättre quiz-prestandaspårning, övervakning av migreringsstatus och stöd för användartaggning i social utbildning.

## Experience Builder

Experience Builder är ett no-code-/low-code-verktyg i Adobe Learning Manager som hjälper dig att skapa anpassade utbildningsportaler. Det gör att du kan designa varumärkta, användarvänliga utbildningsportaler utan att behöva tekniska färdigheter eller omfattande kodningskunskaper.
Med Experience Builder kan administratörer enkelt skapa sidor, menyer och widgetar och leverera personliga utbildningsupplevelser som är anpassade för deras målgrupp.

Innan Experience Builder ställdes organisationer inför flera utmaningar:

1. **Begränsad anpassning**: Portaler har fasta designer med få alternativ som återspeglar ditt varumärke. Administratörer kunde bara göra grundläggande ändringar, som att ändra sidhuvuden, sidfötter eller färger, vilket begränsade möjligheten att skapa unika upplevelser.
2. **Kostnad**: Det tog ofta 6 till 9 månader att slutföra arbetet med att skapa anpassade portaler och det tog lång tid för utvecklare att slutföra dem. Denna metod ökade den totala ägandekostnaden och försenade driftsättningen.
3. **Allmänna upplevelser**: Alla såg samma innehåll, även om det inte var relevant för deras roll eller behov. Denna brist på personalisering minskade elevernas engagemang och tillfredsställelse.
4. **Tekniska hinder**: Icke-tekniska administratörer har haft problem med att skapa eller uppdatera portaler eftersom de behövde kodningskunskap eller extern support.

Experience Builder löser dessa problem genom att tillhandahålla en enkel lösning utan koder eller med låg kod för att skapa personliga portaler med varumärke.

Det gör att administratörer kan utforma portaler som uppfyller deras organisations behov utan att förlita sig på teknisk expertis eller externa utvecklare.

**Användningsfall**

* **Varumärkta portaler**: Skapa en portal som matchar ditt företags webbplats med logotyper, färger och layouter. Ett vårdföretag kan till exempel utforma en portal som återspeglar företagets varumärke samtidigt som det levererar utbildningsinnehåll.
* **Rollbaserad utbildning**: Skapa sidor som är anpassade för specifika roller. Säljteam kan se produktutbildning, medan tekniker får tillgång till tekniska kurser.
* **Produktutbildning**: Konfigurera särskilda sidor för olika produkter, till exempel Photoshop eller Illustrator, med widgetar som visar kurser, certifieringar och relaterade resurser.

I [Experience Builder](/help/migrated/administrators/feature-summary/experience-builder/overview.md) finns mer information om hur du skapar anpassade sidor med hjälp av widgetar.

## Språkbaserad elevstatus

För närvarande spårar Adobe Learning Manager endast elevframsteg för det valda språkområdet, vilket orsakar betydande förluster av framsteg när man byter språk/språkinställningar i spelaren. Denna begränsning kan leda till en dålig användarupplevelse, eftersom elever kan förlora sina framsteg när de öppnar innehåll på olika språk. Förloppet för varje modul i spelaren spåras på både användar- och modulnivå. Detta leder till en situation där en användares förlopp åsidosätts när hen växlar tillbaka till ett tidigare använt språk för samma modul.

Om en elev till exempel gör 75 % framsteg i språk A (engelska) och sedan byter till språk B (spanska), då de återvänder till språk A, återställs deras framsteg till 0 % istället för att återgå från 75 %.

För att åtgärda dessa begränsningar har funktionen förbättrats så att den stöder språkspecifik framstegsspårning:

* **Språkspecifik lagring**: När en elev byter språkversion (till exempel från språk A till språk B) i spelaren, sparas nu förloppsindikatorn separat i Adobe Learning Manager för varje språkområde.
* **Återupptagande av förloppet**: När användaren växlar tillbaka till ett tidigare använt språk (från språk B tillbaka till språk A), återupptas innehållet där det slutade på det språket.
* **Oberoende framstegsspårning**: Varje språk bibehåller sitt eget framstegsläge, vilket gör att elever kan utforska innehåll på flera språk utan att förlora sina individuella framsteg på varje språk.

Följande innehållstyper stöds inte för språkbaserade elevframsteg:

* Video- och ljudinnehåll stöds inte.
* Innehåll från tredje part, som Go1, LinkedIn Learning, getAbstract och Harvard ManageMentor stöds inte.
* Innehåll som inte skickar data till utbildningspostlagret (LRS) kommer inte att ha framsteg spårade eller sparade.
* Användare av mobilappar kan inte spåra förloppet för den här funktionen i offlineläge.

Titta i [Min utbildning](/help/migrated/learners/feature-summary/courses.md#language-based-progress-management) om du vill ha mer information om språkbaserade elevframsteg.

## Inkrementellt stöd och stöd för flera roller

Adobe Learning Manager stöder nu inkrementell och flerstegsimport för anpassade roller och rolltilldelningar. Vid stegvis import kan administratörer överföra endast nya, uppdaterade eller borttagna poster för användarna i stället för att överföra hela CSV-filen på nytt.

Genom att importera flera steg utökas denna möjlighet genom att stora organisationer kan dela upp inkrementella filer efter region eller avdelning (till exempel USA, EU, APAC) och bearbeta dem parallellt. Adobe Learning Manager stöder också upp till 20 inkrementella användar-CSV:er och deras motsvarande anpassade roller CSV:er, vilket gör det skalbart för stora åtgärder.

Administratörer kan nu ladda upp roll- och användarrollfiler (role.csv och user_role.csv) inkrementellt tillsammans med användarfiler (user.csv) i stället för att alltid göra fullständiga uppladdningar. Varje användarimport (user1.csv) är länkad med sina egna roll- och rollmappningsfiler (user1_role.csv, user1_user_role.csv), som lagras i separata FTP-mappar.

Följande tre extra kolumner har lagts till i följande CSV-filer:

* Användarregistreringstillstånd (user.csv): Anger aktuell registreringsstatus för användaren i systemet (till exempel aktiv, inaktiv eller borttagen).
* Role State (role.csv): Anger om en anpassad roll för närvarande är aktiv eller inaktiv på kontot.
* Användarrolltillstånd (user_role.csv): Definierar status för mappningen mellan en användare och en roll och visar om tilldelningen är aktiv eller har tagits bort.

Adobe Learning Manager samlar nu in åtgärder för att lägga till, uppdatera och ta bort i användargranskningsrapporter och anpassade rollrapporter, vilket ger administratörer bättre insyn i ändringar.

>[!NOTE]
>
>Dessa ändringar gäller endast de konton som använder inkrementella användare.

Visa [Inkrementellt och flerinkrementellt stöd för anpassade roller](/help/migrated/integration-admin/feature-summary/configure-role-csv-files.md#incremental-and-multi-incremental-support-for-custom-roles) om du vill ha mer information om inkrementellt och flerinkrementellt stöd för anpassade roller.

## Go1-integreringsförbättringar

Go1-integreringen har förbättrats så att du kan gå vidare med Go1-kurser för att skapa utbildningsprogram (LP) i Adobe Learning Manager. Denna uppdatering stödjer inkluderandet av Go1-kurser i återkommande certifieringar och introducerar en ny version av Go1-innehållsnavet som möjliggör effektivare kurskurser.

* Skapa och hantera spellistor direkt i Go1 med hjälp av AI-chattassistans eller manuellt val.
* Inkludera Go1-kurser i återkommande certifieringscykler med automatisk återställning av förloppet. I [Certifieringar](/help/migrated/administrators/feature-summary/certifications.md) finns mer information om hur du skapar certifikat.
* Uppgraderat gränssnitt för innehållsidentifiering för förbättrad bläddring och kuratering av innehåll.

**Viktiga anteckningar**

* Alla Go1-funktioner kräver en aktiv Go1-licens.
* Det tidigare kostnadsfria Go1-innehållet kommer att avvecklas. Organisationer måste förhandsgranska och köpa nödvändiga innehållspaket.
* Administratörer och författare kan skapa och hantera spellistor. Elever har endast visningsåtkomst.

Titta på [Kurera Go1-kurser till utbildningsvägen](/help/migrated/administrators/feature-summary/content-marketplace/curate-go1-playlist.md) om du vill ha mer information om hur du lägger till Go1-kurser till utbildningsvägen.

## Stöd för vimeo-URL:er i modulen Aktivitet

Modulen Aktivitet stöder nu inbäddning av Vimeo-URL:er, som liknar YouTube-inbäddningar. Med den här förbättringen kan administratörer lägga till Vimeo-videolänkar direkt i modulen Aktivitet. När författare skapar en kurs och lägger till en aktivitetsmodul ser de nu ett alternativ för att inkludera en Vimeo-URL. På samma sätt som YouTube-länkar läggs till kan författare klistra in en Vimeo-länk direkt i modulkonfigurationen. När videon har publicerats kan eleverna spela upp Vimeo-videon smidigt i elevappen utan att omdirigeras utanför plattformen.

Titta i [Lägg till moduler](/help/migrated/authors/feature-summary/courses.md#add-modules) om du vill ha mer information om hur du lägger till moduler i kurserna.

## Tidszoninformation för CR/VC-moduler

Tidszoninformation visas nu för modulerna Klassrum (CR) och Virtuellt klassrum (VC) på sidan Kursöversikt, sidan Instans, sidan Förgranska elev och i Kalenderwidgeten. Elever och administratörer kan tydligt se tidszonen som är associerad med schemalagda sessioner på nyckelsidor och kalenderinbjudningar. Elever kan planera och ansluta till sessioner bättre utan att det uppstår missförstånd i tidszonen. Den här förbättringen är endast tillgänglig i appen Immersive Learner.

Elever i olika regioner kan bekräfta sessionstiden i rätt tidszon. Om du visar tidszonen tydligt kan du förhindra missade sessioner och se till att kalendern schemaläggs korrekt.

## Fyll i författarnamnet automatiskt medan du skapar en kurs

När kursen skapas fylls fältet **[!UICONTROL Author(s)]** automatiskt i med namnet på de författare som skapar kursen. Författare behöver inte längre ange sina egna namn manuellt. Ytterligare författare kan fortfarande läggas till eller uppdateras efter behov.

För organisationer med strikta regler för ägarskap av innehåll ser en automatisk ifyllning till att Författarna alltid är korrekt tilldelade. När du redigerar en befintlig kurs kan författaren uppdatera eller lägga till medförfattare utan att den automatiskt ifyllda posten går förlorad.

Visa [Skapa en kurs](/help/migrated/authors/feature-summary/courses.md#create-a-course---advanced-workflow) om du vill ha mer information om hur du skapar en kurs.

## Sök efter externa profiler när du ändrar profil

Tidigare bläddrade administratörer igenom hela listan över externa profiler och valde manuellt den önskade profilen vid återtilldelning av elever. Detta gjorde processen tidskrävande, särskilt för konton med många profiler. Med den här förbättringen kan administratörer och anpassade administratörer nu söka efter externa profiler direkt på fliken under arbetsflödet för att ändra profil.

**Användningsfall**

* I konton med hundratals externa profiler (t.ex. franchise-platser, partnerföretag eller regionala grupper) kan administratörer nu hitta den exakta profilen direkt med hjälp av sökning, vilket minskar antalet fel och sparar tid.
* Under organisationsförändringar, som fusioner eller omjusteringar på avdelningar, kan elever behöva flyttas i grupp till nya externa profiler. Den sökbaserade återtilldelningen gör uppgiften smidigare och mer exakt.

Visa [Ändra den externa profilen](/help/migrated/administrators/feature-summary/add-users-user-groups.md#change-profile) om du vill ha mer information om hur du ändrar profilen.

## Lägg till en medarrangör för Microsoft Teams-sessioner

Tidigare kunde författare endast tilldela en organisatör till Microsoft Teams-sessioner. Med den här förbättringen kan administratörer nu lägga till medorganisatörer i en session. Ett nytt fält, **[!UICONTROL Co-Organizer]**, har introducerats i Microsoft Teams-sessioner, vilket gör att författarna kan tilldela ytterligare organisatörer vid sidan av den primära organisatören.

Författare kan utse flera medorganisatörer för varje Microsoft Teams-session. Medorganisatörer har samma åtkomst och behörigheter som den primära organisatören. Författare kan lägga till upp till 10 organisatörer per session, vilket ger större flexibilitet och förbättrar sessionshanteringen.

**Användningsfall**

När du genomför storskaliga sessioner med många elever kan medorganisatörer hjälpa till att hantera närvaro, moderera diskussioner och övervaka chatt medan den primära organisatören fokuserar på att leverera utbildningen.

I artikeln [Lägg till moduler](/help/migrated/authors/feature-summary/courses.md#add-modules) finns mer information om hur du lägger till CR/VC-sessioner till kurserna.

## Hämta rapport över intresserade elever

När en administratör tar alla kursinstanser ur bruk (till exempel i slutet av kurscykeln) ersätts knappen **[!UICONTROL Enroll]** på sidan **[!UICONTROL Course Overview]** med alternativet [!UICONTROL Register Interest]. Elever kan välja det här alternativet för att uttrycka sitt intresse för kursen. Administratörer kan nu visa och exportera en lista över elever som har registrerat intresse för en kurs.

Administratörer kan sedan komma åt listan och hämta den som en rapport. En **[!UICONTROL Interested Learners]**-knapp har lagts till på kurssidan när inga aktiva instanser är tillgängliga. Det visar elevens namn och det datum då hen registrerade intresse i administratörsgränssnittet.

Administratörer kan välja **[!UICONTROL Actions]** och sedan välja **[!UICONTROL Export Report]** för att exportera **[!UICONTROL Interested Learners report]**.

![](assets/register-interest.png)
_Avsnittet Kursöversikt där elever kan se alternativet Registrera intresse_

Visa [Hämta den intresserade eleven](/help/migrated/administrators/feature-summary/courses.md#download-the-interested-learner-report) om du vill ha mer information.

## Återställ rekommendationer i Salesforce-programmet

Tidigare kunde elever som använde Adobe Learning Manager Salesforce-programmet bara välja roller och rekommendationspreferenser en gång. Om de måste byta till det inbyggda Adobe Learning Manager-programmet för att uppdatera sin profil och få relevanta kursrekommendationer. Med den senaste förbättringen kan elever nu snabbt återställa sina preferenser direkt i Salesforce-appen när deras jobbroll, team eller ansvarsområden ändras.

Denna smidiga process säkerställer att de fortsätter att få uppdaterade, relevanta kursrekommendationer utan att lämna Salesforce. Administratörer drar nytta av att utbildningarna slutförs oftare och att användarroller och rekommenderat innehåll anpassas bättre, allt utan att ge extra stöd eller vägledning när de byter plattform.

Adobe Learning Manager har nu en **[!UICONTROL Reset Interests]**-knapp i Salesforce-appen. Elever kan nu återställa sina roller och inlärningsinställningar utan att behöva lämna Salesforce eller logga in på det inbyggda Adobe Learning Manager-programmet.

Titta i [Återställ rekommendationer i Salesforce-programmet](/help/migrated/learners/feature-summary/sfdc-app.md#reset-recommendations-in-salesforce-app) om du vill ha mer information om återställningsrekommendationer i Salesforce-programmet.

## Förbättrad kalenderwidget

Elever kan nu se både tidigare och kommande sessioner i kalenderwidgeten. De kan gå igenom kalendern till vilket datum som helst och kontrollera sessionsdetaljerna. Det innebär att de kan granska sessioner som redan har ägt rum och hjälpa dem att spåra vad de har missat eller deltagit i. De kan också se alla kommande sessioner under de kommande 24 månaderna, inklusive innevarande månad, vilket gör det lättare att planera och hantera sina scheman.

I [Kalender](/help/migrated/learners/feature-summary/learner-home-page.md#calendar) finns mer information om kalenderwidgeten.

## Tagga användare på sociala tavlor

Sociala anslagstavlor har nu stöd för användartaggning, vilket möjliggör mer riktade diskussioner och förbättrat samarbete inom utbildningsgrupper. Elever kan taggas i inlägg om social utbildning och kommentarer via elevappen, API:er och referenswebbplatsen för Adobe Learning Manager.

Användare utanför tavlans omfattning kan inte taggas, vilket förhindrar oönskade meddelanden. Om en taggad användare tas bort från systemet visas användarens omnämnande som &quot;anonym&quot;. Det är inte tillåtet att tagga användargrupper eller &quot;@all&quot; för att förhindra skräppost.

* **@username**: Användarna kan tagga andra tavlans medlemmar med formatet @username.
* **Omfångsbegränsad taggning**: Endast användare med åtkomst till den specifika tavlan kan taggas, vilket garanterar sekretess och relevans.
* **Flerkanalsmeddelanden**: Taggade användare får både aviseringar i appen och e-postmeddelanden med direktlänkar till relevanta inlägg eller kommentarer.

**Användningsfall**

* Hälso- och sjukvårdspersonal som vill ha information från kollegor om medicinska fall: Tagging gör det möjligt för läkare och sjuksköterskor att snabbt meddela rätt specialister, vilket garanterar snabb och korrekt rådgivning om komplexa patientfall.
* Ämnesområde Experter som konsulteras i specialiserade ämnen: Genom att tagga experter kan team direkt involvera rätt personer, minska svarstiden och förbättra beslutsfattandet för tekniska frågor eller nischfrågor.
* Teamdiskussioner som kräver synpunkter från specifika intressenter: Genom att tagga intressenterna ser man till att relevanta beslutsfattare är medvetna om uppdateringar och kan ge synpunkter, hålla projekt på rätt spår och anpassa sig till affärsmål.

Titta i [Användartaggning på socialtavlor](/help/migrated/learners/feature-summary/social-learning-web-user.md#tag-users-in-social-board-posts) om du vill ha mer information om att tagga användare på socialtavlor.

## Omfattade behörigheter för meddelanden för anpassade administratörer

Anpassade administratörer kan nu skapa meddelanden, men bara för sina tilldelade användargrupper eller kataloger. Detta förhindrar oavsiktlig kommunikation över organisatoriska gränser. Anpassade administratörer kan bara skapa meddelanden för användare inom sitt tilldelade omfång. Meddelanden kan omfattas av specifika användargrupper eller kataloger. Fullständiga administratörer behåller synligheten och kontrollen över alla meddelanden, inklusive de som skapas av anpassade administratörer med omfång.

**Viktiga fördelar**

* Riktad kommunikation som ser till att meddelanden når ut till enbart relevanta målgrupper.
* Minskad överbelastning av informationen genom att förhindra att irrelevanta meddelanden når oavsiktliga användare.
* Bibehåller organisatoriska gränser och förhindrar oavsiktlig korskommunikation.

**Viktiga anteckningar**

* Om en anpassad administratörs omfång ändras, visas en varningsikon för de meddelanden som påverkas och individuella omfång återställs.
* Varje meddelande måste uppdateras individuellt när omfånget ändras.
* I rapporten [Aviseringsmeddelande](/help/migrated/administrators/feature-summary/announcements.md) visas endast elever inom den anpassade administratörens tilldelade omfattning.

**Användningsfall**

* Franchiseorganisationer där regionala chefer bara behöver kommunicera med sina franchisetagare.
* Stora organisationer med regionala administratörer eller avdelningsadministratörer som skickar meddelanden till sina team.

Visa [Skapa meddelande för det tilldelade omfånget](/help/migrated/administrators/feature-summary/announcements.md#create-announcement-for-the-assigned-scope) om du vill ha mer information om hur du skapar meddelanden för det tilldelade omfånget.

## Markera en anpassad roll när du publicerar ett innehåll från Adobe Captivate

När en användare publicerar innehåll från Adobe Captivate till Adobe Learning Manager och har flera anpassade roller, uppmanas hen att välja den specifika anpassade roll som kursen ska publiceras under. Detta säkerställer att rätt rollägarskap och behörigheter tillämpas på den publicerade kursen.

I [Anpassad roll](/help/migrated/administrators/feature-summary/custom-role.md) finns mer information om hur du skapar anpassade roller för användarna.

## Förbättringar av widgeten Sparat av mig

Tidigare visades alla kurser i katalogen när du valde remsan **[!UICONTROL Saved By Me]**. Nu ser eleverna bara sina bokmärkta kurser i remsan **[!UICONTROL Saved By Me]** på elevens startsida. Om du väljer den här remsan kommer eleverna till katalogsidan, där endast de kurser de har sparat visas.

I katalogen kan elever använda ytterligare filter för att förfina sin sökning. När ett filter används visas bara kurser som uppfyller de valda kriterierna. Tidigare bokmärkta kurser visas bara om de matchar det använda filtret.

I [Konfigurera sparade kurswidgetar på AEM-webbplatser](/help/migrated/integrate-aem-learning-manager.md#configure-my-saved-courses-widgets-in-aem-sites) finns mer information om sparade kurswidgetar på AEM-webbplatser.

## Stöd för att visa författarnamn i delade kurser

Tidigare, när en kurs delades med ett [kollegialt konto](/help/migrated/administrators/feature-summary/peer-account.md), visades författaren som extern författare. Nu visas författarens namn på kurser, oavsett om de är en intern användare av huvudkontot eller en äldre författare (dvs. ett namn som anges som en sträng i fältet Författare vid skapande av kurs). Om du väljer en författare visas antalet kurser som hen har delat med det kollegiala kontot, men dessa Författare är inte faktiska användare i det kollegiala kontot.

Om en användare tas bort från huvudkontot tas användarens data bort där, men författarinformationen finns kvar på alla kollegiala konton där användarens innehåll har delats.

>[!NOTE]
>
>Det här är en flaggbaserad funktion. Kontakta kundsupportteamet på [learningmanagersupport@adobe.com](mailto:learningmanagersupport@adobe.com) om du vill aktivera det här alternativet.

Titta i [Kollegialt konto](/help/migrated/administrators/feature-summary/peer-account.md) om du vill ha mer information om delning av innehåll till kollegialt konto.

## Sök synlighet för utbildningsobjekt av lägre ordning

Tidigare visade sökresultat inte konsekvent enskilda kurser när de ingick i högre utbildningsobjekt som utbildningsvägar eller certifieringar. Om en elev endast var registrerad på en utbildningsväg eller ett certifikat returnerade sökningen endast den högre ordningsstrukturen och inte den enskilda kursen.

Med den här förbättringen kan eleverna nu se enskilda kurser i sökresultat, även när de ingår i utbildningsvägar eller certifieringar. En ny administratörsinställning, **[!UICONTROL Show all enrolled courses in search results]**, har introducerats. När det här alternativet är aktiverat visas alltid själva kursen tillsammans med relaterade utbildningsvägar eller certifieringar när du söker efter en viss kurs.

I [Inställningar](/help/migrated/administrators/feature-summary/settings.md#general-settings) finns mer information om allmänna inställningar.

## API-ändringar

### Förbättringar av migrerings-API

Adobe Learning Manager stöder nu migrering av olika dataobjekt till ett konto via migreringsprocessen. Denna process kan initieras via både API:er och användargränssnittet. När en migrering misslyckas är fel tillgängliga för hämtning via gränssnittet. De här felen är användbara vid felsökning av migreringsfel och hantering av migreringskörningar.

I den här versionen kommer felloggarna också att vara tillgängliga att hämta via API:erna för effektiv, programmatisk felspårning och felsökning.

**API-ändringar**

Det finns ett nytt migrerings-API, `runStatus`, som gör att integreringsadministratörer kan kontrollera statusen för migreringskörningar som utlösts via API:t. Detta är inte möjligt i tidigare versioner av Adobe Learning Manager.

Dessutom tillhandahåller `runStatus` API nu en direktlänk för att hämta felloggar (CSV) för slutförda körningar. Observera att länken endast är giltig i sju dagar, och loggarna sparas i en månad.

API-svaret för `startRun` har uppdaterats för att inkludera migreringsprojektets ID, sprint-ID och sprint-körnings-ID, som krävs för att fråga den nya statusslutpunkten.

#### runStatus API

**Beskrivning**

Hämtar status för en befintlig migreringskörning.

**Slutpunkt**

```
GET /bulkimport/runStatus
```

**Parametrar**

* **migrationProjectId**: (obligatoriskt). En unik identifierare för ett migreringsprojekt. Ett migreringsprojekt används för att överföra data och innehåll från ett befintligt system för hantering av inlärning (LMS) till Adobe Learning Manager. Varje migreringsprojekt kan bestå av flera sprintar, som är mindre enheter för migreringsuppgifter.

* **sprintId**: (obligatoriskt). En unik identifierare för ett sprint inom ett migreringsprojekt. Ett språng är en delmängd migreringsuppgifter som omfattar specifika utbildningsobjekt (t.ex. kurser, moduler och elevposter) som ska migreras från ett befintligt LMS till Adobe Learning Manager. Varje sprint kan utföras oberoende av varandra, vilket möjliggör en stegvis migration.

* **sprintRunId**: (obligatoriskt). En unik identifierare som används för att spåra körningen av ett specifikt sprint inom ett migreringsprojekt. Det är kopplat till den faktiska migreringsprocessen för de objekt som definieras i en sprint. SprintRunId hjälper till att övervaka, felsöka och hantera migreringsjobbet.

**Svar**

```
{
  "sprintId": 2510080,
  "sprintRunId": 2740845,
  "migrationProjectId": 2509173,
  "startTime": 1746524711052,
  "endTime": 1746524711052,
  [
    {
      "id": 2609923,
      "lastHeartbeatTime": 1746524711052,
      "objectName": "content",
      "jobState": "COMPLETED",
      "errorCsvLink": "",
      "errorLogLink": "migration/5830/2509173/2510080/2740845/content_err.csv",
      "sequenceNumber": 1
    },
    {
      "id": 2609922,
      "lastHeartbeatTime": 1746524713577,
      "objectName": "course",
      "jobState": "WAITING_IN_QUEUE",
      "errorCsvLink": "",
      "errorLogLink": null,
      "sequenceNumber": 2
    }
  ]
}
```

#### startRun-API

API-svaret `startRun` uppdaterades så att det inkluderade ytterligare tre fält - migrationProjectId, sprintId och sprintRunId. Dessa fält gör det möjligt för användare att spåra och fråga status för specifika migreringskörningar med det nya runStatus-API:et.

```
curl -X GET --header 'Accept: text/html' 'https://learningmanager.adobe.com/primeapi/v2/bulkimport/runStatus?migrationProjectId=001&sprintId=10001&sprintRunId=7'
```

Ger följande svar. Svaret innehåller:

* `migrationId`
* `sprintId`
* `sprintRunId`

**Svar**

```
{
  "status": "OK",
  "title": "BULKIMPORT_RUN_INITIATED_SUCCESSFULLY",
  "source": {
    "info": "Success",
    "migrationInfo": {
      "migrationProjectId": "001",
      "sprintId": "10001",
      "sprintRunId": "7"
    }
  }
}
```

I [Migreringshandboken](/help/migrated/integration-admin/feature-summary/migration-manual.md) finns mer information om hur du migrerar innehåll från befintligt LMS.

### Ändringar i socialt API (användartagg, kommentarer och svar)

Adobe Learning Manager har nu stöd @user taggningsfunktionen på anslagstavlor, så att elever kan nämna och meddela kollegor i inlägg, kommentarer och svar. Den här funktionen förbättrar samarbetet och innehållsidentifieringen på plattformen.

Den här versionen introducerar nya API-funktioner för att stödja användaromnämnanden, däribland förbättrade slutpunkter för POST och GET samt en ny sökfunktion för taggade användare.

**Översikt över API-ändringar**

* Uppdaterade POST-API:er för att skapa inlägg/kommentarer/svar med användaromnämnanden
* API:er för GET har uppdaterats med användaromnämnandedata i svar

**Format för användaromnämnanden**

En användare omnämns med formatet: @(användare:userId)

#### Skapa inlägg med omnämnanden

**Slutpunkt**

```
POST /primeapi/v2/posts
```

**Beskrivning**

Skapa ett nytt inlägg om social utbildning med användaromnämnanden.

**Text för begäran**

```
{
  "data": {
    "type": "post",
    "attributes": {
      "boardId": 13282,
      "accountId": 11152,
      "text": "<p>This is a new post mentioning @[user:11257229]</p>",
      "createdByUserId": 11257228,
      "postType": "discussion"
    },
    "id": null
  }
}
```

**Svar**

Standardsvar efter skapande med omnämnandedata som ingår i relationen _userMentions_.

#### Skapa kommentar med omnämnanden

**Slutpunkt**

```
POST /primeapi/v2/comments
```

**Beskrivning**

Lägg till en kommentar till ett inlägg med användaromnämnanden.

**Text för begäran**

```
{
  "data": {
    "type": "comment",
    "attributes": {
      "postId": 20746,
      "accountId": 11152,
      "text": "<p>Test Comment @[user:11257229]</p>",
      "createdByUserId": 11257228,
      "commentLevel": 0
    },
    "id": null
  }
}
```

#### Skapa svar med omnämnanden

**Slutpunkt**

```
POST /primeapi/v2/replies
```

**Beskrivning**

Svara på en kommentar med användaromnämnanden.

**Text för begäran**

```
{
  "data": {
    "type": "reply",
    "attributes": {
      "postId": 20746,
      "accountId": 11152,
      "text": "<p>Thanks for the update @[user:11257229]</p>",
      "createdByUserId": 11257228,
      "commentLevel": 1,
      "parentCommentId": 55621
    },
    "id": null
  }
}
```

#### Hämta inlägg med omnämnanden

**Slutpunkt**

```
GET /primeapi/v2/posts/{id}
```

**Beskrivning**

Hämta inläggsinformation, inklusive nämnda användare.

**Svar**

```
{
  "links": {
    "self": "https://learningmanager.adobe.com/primeapi/v2/posts/7522"
  },
  "data": {
    "id": "7522",
    "type": "post",
    "attributes": {
      "commentCount": 3,
      "dateCreated": "2025-06-10T11:33:29.000Z",
      "dateUpdated": "2025-06-25T14:52:04.000Z",
      "downVote": 0,
      "postingType": "DEFAULT",
      "richText": "<p>my updated fourth post @[user:14707776] second mention my first post</p>",
      "state": "ACTIVE",
      "text": "my updated fourth post @[user:14707776] second mention my first post",
      "upVote": 0,
      "viewsCount": 0
    },
    "relationships": {
      "createdBy": {
        "data": {
          "id": "14707776",
          "type": "user"
        }
      },
      "parent": {
        "data": {
          "id": "3971",
          "type": "board"
        }
      },
      "userMentions": {
        "data": [
          {
            "id": "14707776",
            "type": "user"
          }
        ]
      }
    }
  },
  "included": [
    {
      "id": "14707776",
      "type": "user",
      "attributes": {
        "avatarUrl": "https://cpcontents.adobe.com/public/images/default_user_avatar.svg",
        "binUserId": "45664b87-75a3-43ec-b0b7-5064958eac6f",
        "email": "user@example.com",
        "enrollOnClick": false,
        "fields": {
          "Location": "BLR"
        },
        "gamificationEnabled": true,
        "lastLoginDate": "2025-06-27T11:21:17.000Z",
        "name": "John Doe",
        "pointsEarned": 1690,
        "pointsRedeemed": 0,
        "preferredResolution": "AUTO",
        "profile": "admin",
        "roles": [
          "Learner",
          "Admin",
          "Author",
          "Instructor",
          "Integration Admin",
          "Manager"
        ],
        "state": "ACTIVE",
        "userType": "Internal"
      },
      "relationships": {
        "account": {
          "data": {
            "id": "9238",
            "type": "account"
          }
        }
      }
    }
  ]
}
```

### Ändringar i socialt API (användarsökning)

**Slutpunkt**

```
GET /primeapi/v2/users/search?q={searchTerm}&context=tagging
```

**Beskrivning**

Sök efter användare som är tillgängliga för taggning baserat på inställningarna för socialt omfång.

**Parametrar för förfrågan**


* q (obligatoriskt): Sökord (minst 3 tecken).
* kontext: Ställ in som &quot;taggning&quot; för att få användare berättigade till omnämnanden.
* boardId (valfritt): Tavlans-id för att filtrera användare baserat på åtkomstbehörigheter.

**Svar**

```
{
  "data": [
    {
      "id": "11257229",
      "type": "user",
      "attributes": {
        "name": "Jane Smith",
        "email": "jane.smith@example.com",
        "avatarUrl": "https://cpcontents.adobe.com/public/images/default_user_avatar.svg",
        "userType": "Internal",
        "state": "ACTIVE"
      }
    }
  ]
}
```

### Förbättringar av elevs-API för prestandaspårning

API:t `GET /loResourceGrades` har förbättrats för att tillhandahålla detaljerade information om frågesportens prestanda, vilket möjliggör mer avancerade analyser och automatiserat beslutsfattande.

API-svaret innehåller nu ytterligare två fält:

* **[!UICONTROL highestScore]**: Det bästa resultatet som en elev har uppnått under alla frågeformulärsförsök
* **[!UICONTROL maxScore]**: Total möjlig poäng för quiz

**Exempel på API-svar**

```
{
    "links": {
        "self": "https://learningmanagerstage1.adobe.com/primeapi/v2/loResourceGrades/course:15067_30122_41715_1_3400468"
    },
    "data": {
        "id": "course:15067_30122_41715_1_3400468",
        "type": "learningObjectResourceGrade",
        "attributes": {
            "completed": false,
            "duration": 0,
            "hasPassed": false,
            "highestScore": 0,
            "maxScore": 0,. 
            "progressPercent": 0,
            "score": 0
        },
        "relationships": {
            "loResource": {
                "data": {
                    "id": "course:15067_30122_41715_1",
                    "type": "learningObjectResource"
                }
            }
        }
    }
}
```

Som svar är **kurs:15067_30122_41715_1_3400468** ID:t för utbildningsobjektets resursgrad som informationen begärs för. Du kan hämta `learningObjectResourceGrad`e-id från API:t `GET /enrollments/{id}`.

### API-svar stöder skiftlägeskänslighet för författarnamn

API-svaret ger nu det exakta skiftläget för äldre författarnamn som anges när kursen skapas eller uppdateras. Detta garanterar att namn visas konsekvent i elevgränssnittet och offentliga API:er.

* När ett nytt författarnamn läggs till sparas ärendet och returneras exakt som det har angetts.
* Om ett befintligt författarnamn tas bort och läggs till igen med ett annat ärende, kommer det uppdaterade ärendet att hedras och återspeglas i alla kurser där författarnamnet används.
* Ingen automatisk migrering görs för tidigare lagrade namn. Detta beteende följs bara av nya eller uppdaterade namn.

### Förbättringar av Calendar API

Kalendern läser nu in sessioner för den månad som har valts av användaren. Om du vill hämta både tidigare och kommande sessioner via API:t har en ny `year`-parameter lagts till i elevslutpunkten `GET /users/{id}/calendar`. Parametrarna `month` och `year` måste anges tillsammans för att hämta sessionsinformation.

**Exempel på curl**

```
curl -X GET --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth a4ae04eb9f06f4bf88abcde17' 'https://abc.adobe.com/primeapi/v2/users/12345678/calendar?month=7&year=2025&currentMonthOnly=false&filter.allSessions=false'
```

### Stöd för slutförande av markeringar via administratörs-API

Tidigare hade det offentliga API:t inte stöd för instansbaserad slutförandemarkering i scenarier med flera registreringar. Med den här förbättringen kan du nu inkludera kursinstans-ID i begärandetexten för `POST /users/{userId}/userModuleGrade` och administratören kan markera slutförande för en specifik instans.

### Ange användar-ID-inställning för SCORM-rapportering

Vissa kunder kräver elevens UUID (Universally Unique Identifier) i stället för standardanvändar-ID för slutförande av SCORM-innehåll. Genom att använda UUID får du mer exakt spårning över utbildningsprogram och förhindrar dubblering av licensanvändning i MAU-konton (månadsvis aktiva användare).

En ny inställning på kontonivå, `reporting_userid_preference`, har lagts till för att stödja detta. När den här inställningen är aktiverad skickas UUID i stället för user_id när elever slutför SCORM-innehåll.

>[!NOTE]
>
> Kontakta vårt kundsupportteam på [learningmanagersupport@adobe.com](mailto:learningmanagersupport@adobe.com) för att konfigurera den här inställningen.

Det nya attributet `reportingUserIdPreference` har introducerats till `get /account` för att spåra användar-ID-inställningarna.

### Författarinformation i delade kurser

I utbildningsobjekts-API:et har sättet som information om författare returneras uppdaterats för att skilja mellan kurser med huvudkonto och kurser som delas med kollegiala konton:

* Delade kurser (kollegialt konto): Information om författaren returneras nu under ett nytt attribut, `authorDetails`. Attributet tillhandahåller författarnamnet även när kursen kommer från ett annat konto.

* Huvudkontokurser: Information om författaren fortsätter att returneras under det befintliga `authors`-attributet utan att det aktuella beteendet ändras.

Den här ändringen säkerställer konsekvens i hur författardata exponeras via API för både huvud- och delade kurser, samtidigt som kompatibiliteten för befintliga integreringar bevaras.

## Ändringar i webhooks

### Registrera LinkedIn Learning-webhookar med anslutningen

Tidigare var administratörer tvungna att manuellt registrera LinkedIn Learning-webhookar i Adobe Learning Manager via API:er. Med den här förbättringen stöder nu LinkedIn Learning (LIL)-anslutningen automatiskt registrering av webhookar under ny anslutningsinställning i ALM. **OAuth-serverns URL** och **klientserverns URL** fylls i automatiskt på konfigurationssidan för LinkedIn Learning.

Titta i [LinkedIn Learning](/help/migrated/integration-admin/feature-summary/connectors.md#linkedin-learning-connector) om du vill ha mer information om LinkedIn Learning-integrering.

### Ändringar av MAU-licensanvändningen i LinkedIn Learning

Tidigare räknade Adobe Learning Manager inte licensanvändningen för MAU-konton (månatliga aktiva användare) när en elev slutförde en LinkedIn-utbildningskurs direkt på LinkedIn utbildningsplattform. Licensförbrukningen utlöstes bara för kurser som togs via Adobe Learning Manager-spelaren, vilket resulterade i felaktig spårning av månadsvisa aktiva användare (MAU).

Med den här förbättringen genererar Adobe Learning Manager nu en extern webhook när en elev genomför en kurs på LinkedIn utbildningsplattform. När Adobe Learning Manager tar emot den här webhooken görs en beräkning av licensanvändningen för att säkerställa korrekt spårning på båda plattformarna.

## Rapportera ändringar

### Instruktörsmarkerade slutföranden i elevbetygsutdrag

Inkrementella elevbetygsutdrag fångar nu instruktörsmarkerade slutföranden, även om närvaro registreras efter sessionsdatumet.
Denna förbättring åtgärdar ett kritiskt avbrott i inkrementella elevutskrifter där instruktörsmärkta slutföranden tidigare missades om närvaro registrerades efter det ursprungliga sessionsdatumet.

Inkrementella elevbetygsutdrag är schemalagda rapporter som endast samlar de ändringar (t.ex. slutföranden eller framstegsuppdateringar) som sker inom en angiven period, snarare än att tillhandahålla en fullständig historisk datadumpning. De används ofta för automatisering, instrumentpaneler och integreringar, vilket gör det möjligt för användare att effektivt spåra senaste utbildningsaktiviteter utan att bearbeta hela transkriptionshistoriken varje gång.

* **Markera som slutförd datum (tidszonen UTC)**: En ny tidsstämpelkolumn som anger exakt datum och tid när en instruktör markerar en session eller modul som slutförd.
* **Förbättrad källspårning för slutförande**: Spårar den specifika instruktören och modulen (till exempel &quot;Classroom&quot;) där slutföranden spelades in.

Dessa ändringar säkerställer att slutföranden markerade efter sessionsdatumet återspeglas korrekt i inkrementella elevens betygsutdrag.

**Användningsfall**

* Organisationer med klassrumssessioner där instruktörer kan markera närvarodagar efter den faktiska sessionen.
* Automatiserade system eller instrumentpaneler som är beroende av inkrementella elevutskrifter för efterlevnad eller rapportering.

![Elevens betygsrapporter visar markerade slutförandedatum (gulmarkerat) för spårning av kursens slutförande i Adobe-inlärning](/help/migrated/assets/mark-completion-column.png)
_Elevens betygsrapport visar en ny kolumn i gult som visar enskilda slutförandedatum för varje användare_

Titta i [Elevens betygsutdrag](/help/migrated/administrators/feature-summary/reports/learner-transcripts.md)om du vill ha mer information om elevens betygsrapport.

### Förbättrad användarrapport med utökade datafält

Användarrapporten innehåller nu ytterligare fält för att förbättra användarspårning och organisationsmappning. Uppdateringarna förenklar användaridentifiering, stöder integrering med arbetsflöden för hantering av nedströmsanvändare, förbättrar förståelsen av rapporteringsrelationer och upprätthåller organisationsgränser för att förhindra oavsiktlig korskommunikation.

* Kolumnen Internt användar-ID: tillhandahåller unika interna identifierare för smidig användarspårning i olika system och API-slutpunkter.
* E-postkolumn för chef: Innehåller kontaktinformation för direktchef för spårning av organisationshierarki.

![Användarrapport som visar det interna användar-ID:t och chefens e-postkolumner markerade med gult](/help/migrated/assets/user-report-columns.png)
_Användarrapporter som visar interna användar-ID:n och chefens e-postadresser för att effektivisera användarhanteringen_

Visa [Hämta användarrapporten](/help/migrated/administrators/feature-summary/add-users-user-groups.md#download-the-user-report) om du vill ha mer information om användarrapporten.

### Användarrapport i FTP, anpassad FTP och Box

**Översikt**

Användarrapport är nu tillgänglig för Box-, FTP- och anpassade FTP-anslutningar, utöver befintliga jobb-API:er. Dessa rapporter ger detaljerad information om internt användar-ID, användarens e-postadress, namnet, chefens e-postadress, användartypen med mera.

Rapporter kan genereras på begäran eller schemaläggas, med data lagrade i respektive anslutning för enkel åtkomst och analys. Den här förbättringen förbättrar övervakning och granskning av användaraktiviteter och ger stöd för bättre säkerhet och efterlevnadsspårning.

Dessa rapporter är tillgängliga parallellt med befintliga rapporter, t.ex. användarregistrering, inloggningsåtkomst, spelifiering och utbildning, vilket gör det möjligt för administratörer att komma åt alla viktiga rapporter från en enda plats för effektiv datahantering och dataanalys.

Visa [Connector](/help/migrated/integration-admin/feature-summary/connectors.md) om du vill ha mer information om FTP-, Anpassad FTP- och Box-anslutning.

### Inkludera avbrutna användare i elevens betygsutdrag

**Översikt**

Organisationer kan nu inkludera avstängda användare (de med inaktiverade externa profiler) i elevens betygsutdrag för att säkerställa omfattande lagring av historiska inlärningsdata.

* Flagga på kontonivå för att konfigurera avbruten användarsynlighet, vilket gör att avbrutna användare kan visas i elevens betygsutdrag.
* Tidigare lagring av uppgifter även efter inaktivering av externa profiler som hängt sig.

**Implementeringskrav**

* Kontakta din CSM (Customer Success Manager) för att aktivera flaggan på kontonivå.

>[!NOTE]
>
>Flaggan är inaktiverad som standard för befintliga konton och måste uttryckligen begäras för nya konton.

Visa [Elevens betygsutdrag](/help/migrated/administrators/feature-summary/reports/learner-transcripts.md) artikel mer information.

### Rapport om arbetsstöd med direktlänkar

**Översikt**

Rapporten om arbetsstöd har förbättrats så att den innehåller direkthämtningslänkar till arbetsstöd, effektivisering av innehållshantering och granskningsprocesser för administratörer och författare. Den här förbättringen ger direkt filhämtning och URL-åtkomst inifrån rapporten. Slipp manuella försök med att hitta och ladda ner arbetsstöd för efterlevnad eller tillgänglighetsgranskningar.

* Kolumnen Arbetsstödslänk: Direkt åtkomst till filer för arbetsstöd och externa URL:er i rapporten.
* Rollbaserad åtkomstkontroll: Länkåtkomsten beror på användarroller och katalogbehörigheter.
* Borttagna arbetsstöd förblir tillgängliga om de fortfarande är kopplade till aktiva kurser.

**Användningsfall**

* Författare eller administratörer genomför regelbundna tillgänglighetsgranskningar av arbetsstöd i enlighet med kraven från stora organisationer.
* Alla scenarier där snabb, rollbaserad åtkomst till arbetsstödsfiler behövs för granskning eller efterlevnad.

![](/help/migrated/assets/job-aid-report.png)
_Arbetsstödsrapporten visar direkthämtningslänkar för att göra det enkelt att komma åt och hämta arbetsstöd i Adobe Learning Manager_

I [Arbetsstödsrapporten](/help/migrated/administrators/feature-summary/reports.md#job-aids-report) finns mer information om arbetsstödsrapporten.

## Fel som är åtgärdade i den här uppdateringen

* Quizpoäng för L2 har nu genererats korrekt för icke-interaktiva quiz-frågor, inklusive information om användare som har slutfört dem.
* Signaturen skickas nu korrekt till målvärden när autentiseringsmekanismen är inställd på Signatur under anslutningskonfigurationen.
* Dummy-användare som skapades under Adobe Connect-sessioner togs inte bort efter att sessionen slutförts. SnapLogic-pipelinen tar nu bort dessa användare korrekt, även när API:t `principals-delete` tidigare returnerade ett 200-svar utan att ta bort dem.
* `null` `eventDetail`-objekt i API-svar orsakar inte längre undantag. Systemet hoppar nu över null-poster och bearbetar hela matrisen, vilket säkerställer fullständiga inspelningar.
* Kolumnen Datum för feedback i feedbackrapporter visar nu rätt datum. Tidigare skickades sekunder felaktigt till konstruktorn Date, som förväntar sig millisekunder, vilket gör att datum visas som januari 1970. Detta har korrigerats för att säkerställa korrekt datumvisning när feedbackrapporter skapas.
* Elever kan nu uppdatera registreringen i en Flex-utbildningsväg även om en av kursinstanserna har fasats ut. Förut orsakade ett konsolfel (det gick inte att läsa egenskaper för odefinierade) när en ny instans valdes och uppdateringen förhindrades.
* Resursnamn i utbildningsvägar visas nu korrekt utan att ordet bryts.
* LinkedIn Learning-webbhookar aktiveras nu från LIL-anslutningen när anslutningar skapas för nya användare. Systemet registrerar också kontot via det privata API:t och visar ytterligare konfigurationsinformation (OAuth-URL och klientorganisations-URL) på sidan Konfigurera i LinkedIn Learning.
* Värden för användarattribut som uppdaterats via SAML-arbetsflöden (`UpdateUserWorkerTask`) sparas nu med sina ursprungliga skiftlägen i stället för att konverteras till gemener.
* Om du ändrar ordning på moduler i en kurs återställs inte längre antalet Obligatoriska moduler till &quot;Alla&quot;. Antalet förblir nu konfigurerat.
* Go1-pipelines hanterar nu språkkoder på ett konsekvent sätt genom att mappa koder med två bokstäver till koder med fyra bokstäver, som liknar LinkedIn Learning-pipelines.
* I Konton för pensionering+ såg elever tidigare &quot;Den här kursen finns inte&quot; när de startar en kurs på utbildningsvägen efter att ha avregistrerat sig från en certifiering. Registreringskällor har nu uppdaterats korrekt, vilket gör att kurser i utbildningsvägar kan startas utan fel.
* När filen module_version.csv innehåller contentType-fält med tomma värden eller null fungerar kursens skapande nu utan problem.
* Kurser visas nu korrekt vid filtrering efter katalog- eller katalogetikett. Tidigare visades inte kurser när de här filtren användes på kurssidan, även om de var kopplade till katalogen.
* I elevappen fastnade ett tryck på TAB i Fluidic-spelaren på knappen Enter Fullscreen. Tangentbordsnavigering går nu korrekt genom alla skärmelement.
* Om du håller muspekaren över långa kursnamn i chefens apps efterlevnadstavla visas nu det fullständiga namnet för registrerade eller kompatibla kurser.
* Endast Delade eller DOLDA accepteras för kolumnen för modulsynlighet i module.csv. Alla andra värden utlöser ett fel under migreringen, vilket förhindrar fel på backend-servern.
* När du skapar en ny administratör med blandade e-postmeddelanden skapas inte längre dubbla användarposter när UUID är inaktiverat. Systemet hanterar nu konsekvent e-postskiftläge för att förhindra dubbletter.
* Anteckningar PDF visas nu korrekt för kurser i språk som arabiska, grekiska, hebreiska, hindi, thailändska och ukrainska. Tidigare såg figurer förvrängda ut i det nedladdade PDF även om de visades korrekt i spelaren.

## Systemkrav

Visa [Systemkrav för Adobe Learning Manager](/help/migrated/system-requirements.md).

## Versionsinformation

Läs [versionsinformationen](/help/migrated/release-note/release-notes.md) om du vill ha de senaste versionsuppdateringarna.

## Tidigare utgåvor av Adobe Learning Manager

* [Adobe Learning Manager-versionen från maj 2025](/help/migrated/whats-new-may-2025.md)
* [Adobe Learning Manager november 2025-utgåvan](/help/migrated/whats-new-nov-24.md)


