---
description: Det här dokumentet innehåller ett rekommenderat sätt för organisationer att installera och konfigurera Adobe Learning Manager. Learning Manager-teamet föreslår ett tillvägagångssätt i flera faser för att komma igång med programmet. Det är inte obligatoriskt för dig att följa alla faser i en viss sekvens.
jcr-language: en_us
title: Riktlinjer för bästa metoder för att konfigurera Learning Manager
contentowner: jayakarr
preview: true
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '3384'
ht-degree: 0%

---



# Riktlinjer för bästa metoder för att konfigurera Learning Manager

Det här dokumentet innehåller ett rekommenderat sätt för organisationer att installera och konfigurera Adobe Learning Manager. Learning Manager-teamet föreslår ett tillvägagångssätt i flera faser för att komma igång med programmet. Det är inte obligatoriskt för dig att följa alla faser i en viss sekvens.

Dessa faser kan utföras av tre olika roller, av en eller flera personer beroende på din organisations konfiguration. De tre rollerna är följande:

1. **IT-administratör** - IT-administratören utför aktiverings- eller integrationsrelaterade aktiviteter kopplade till Learning Manager-programmet i en organisation. IT-administratören kan även lägga till en eller flera användare och utföra rollen som integrationsadministratör.
1. **Författare** - Författare skapar utbildningsinnehåll som krävs för organisationens utbildningskrav. Den som skriver utbildnings- eller utbildningsmaterial för din organisation kan börja skapa det grundläggande innehåll som krävs för Learning Manager-programmet.
1. **Learning Manager-administratör** - Learning Manager-programadministratör utför konfigurations- och konfigureringsaktiviteter. På vissa företag kan IT-administratören även spela rollen som programadministratör för Learning Manager.

Du kan gå igenom informationsgrafiken nedan för att få en översikt över faserna och motsvarande uppgifter.

![](assets/learning-manager-getting-started.jpg)

I det här skedet antar vi att din organisation redan har fått licensnyckeln och att du har aktiverat Learning Manager-kontot. Som nämns i infografiken förklaras de tre spåren på följande sätt:

## Fas 1 - Teknisk konfiguration (IT-administratör) {#phase1technicalsetupitadministrator}

I spår 1 kan IT-administratören för din organisation byta till rollen Integreringsadministratör i Learning Manager-programmet och utföra vissa aktiveringar och integreringar enligt följande:

### Aktivera/lägg till aktiva fält (administratör för Learning Manager) {#enableaddactivefieldscaptivateprimeadministrator}

Förutom de aktiva fält som tillhandahålls av användare under registreringen kan administratören lägga till fler aktiva fält. Administratören kan även aktivera/inaktivera användarfälten. Värdena för dessa aktiva fält genereras från metadata från olika datakällor som är kopplade till användarkonton. Se [Hjälp för aktiva fält](feature-summary/add-users-user-groups.md#active-fields) för mer information.

### Enkel inloggning (SSO) {#singlesignonsso}

Du kan komma åt Learning Manager-programmet med Adobe ID eller genom att använda enkel inloggning (SSO). Enkel inloggning är en mekanism som gör att användaren kan autentisera en gång och få åtkomst till flera program många gånger. Den här konfigurationen är inte obligatorisk för organisationen. Om din organisation har SAML 2.0-baserad SSO-leverantör kan du använda den för att konfigurera Learning Manager-programmet. Konfigurationen krävs på organisationsnivå och i Learning Manager-programmet. Om du väljer att använda SSO ska du kontakta Adobe support för att få konfigurationsinstruktioner. Se [Hjälp med inställningar](feature-summary/settings.md) för mer information.

### Massimport av användare {#bulkimportofusers}

När du har ett stort antal användare i organisationen kan du importera alla användare i grupp till Learning Manager-programmet med hjälp av en .CSV-fil. Innan du gör det föreslår vi att du exporterar listan med användare från organisationens HR-program i .CSV-format. Även om du inte massimporterar användarna i det här skedet kan du bekanta dig med CSV-formatet. Börja med att importera i Learning Manager genom att överföra .CSV-filen och mappa programdatafälten till organisationens CSV-kolumner. Se [Hjälp med massimport](add-users-in-bulk.md) för mer information.

### FTP-anslutningsintegrering {#ftpconnectorintegration}

Om du råkar ut för kontinuerliga utökningar eller borttagningar av anställda i din organisation kan du välja att automatisera massimporten av användare med hjälp av FTP-anslutning. Du måste upprätta en anslutning först och sedan kan du överföra en CSV-fil och mappa CSV-attributen med motsvarande Learning Manager-fält. Du kan schemalägga den automatiska importen och även synkronisera den om det behövs. Se [Hjälp om FTP-anslutning](../integration-admin/feature-summary/connectors.md#ftpconnector) för mer information.

### Integrering med Salesforce-anslutningsprogram {#salesforceconnectorintegration}

Om du har Salesforce-konto i din organisation kan du automatisera processen att importera alla användare från Salesforce till Learning Manager-programmet. Om du vill använda den här funktionen kan du använda Salesforce-anslutning för att integrera Learning Manager med Salesforce-konto och automatisera datasynkronisering. Använd funktionen för automatisk schemaläggning för att utföra automatisk användarimport regelbundet. Du kan också utföra synkning varje dag. Se [Hjälp om Salesforce-anslutningsprogram](../integration-admin/feature-summary/connectors.md#sfconnector) för mer information.

### Integrering med Adobe Connect {#adobeconnectintegration}

Om du använder Adobe Connect i ditt företag kan du integrera det med Adobe Learning Manager-program för att ge elever en sömlös användarupplevelse. Tack vare integreringen kan eleverna komma åt virtuella klassrum direkt i Learning Manager-appen med ett enda klick utan att behöva logga in på Adobe Connect igen. Med hjälp av den här funktionen kan eleverna också använda de inspelade virtuella klassrumssessionerna i Learning Manager-programmet. Integrera inställningarna först om du vill integrera dem. Användning **Inställningar > Adobe Connect > Konfigurera nu** för att tillhandahålla Connect URL och inloggningsuppgifter och integrera. Se [Integreringshjälp för Adobe Connect](feature-summary/adobeconnect-integration.md) för mer information.

### Programregistrering i Salesforce {#salesforceappregistration}

Dina företagselever kan få sömlös erfarenhet av att komma åt Learning Manager-appen direkt på sina Salesforce-konton. Elever kan komma åt sitt tilldelade utbildningsinnehåll som kurser, utbildningsprogram och arbetsstöd från Salesforce-programmet. Användarna kan också få åtkomst till meddelanden och meddelanden från Learning Manager-appen i Salesforce. Om du vill använda den här funktionen måste du registrera den utvalda Salesforce-appen i Learning Manager-programmet. Se [Hjälp för Salesforce-program](../integration-admin/feature-summary/sfdc-app.md) för att lära dig mer om installations- och användningsinstruktionerna.

## Fas 2 - Platskonfiguration (administratör för Learning Manager) {#phase2siteconfigurationcaptivateprimeadministrator}

Programadministratören för Learning Manager på din organisation måste konfigurera eller konfigurera vissa funktioner innan du börjar implementera dem för dina elever.

### Varumärkning {#branding}

En organisation kan vilja visa företagslogotypen i Learning Manager-programmet, ha en egen domän i URL:en, visa organisationsnamnet och visa färgscheman som matchar en organisations varumärke. Med Learning Manager kan organisationer använda alla dessa funktioner. Om du vill anpassa inställningar och använda ditt eget varumärke klickar du på avsnittet Varumärke i den vänstra rutan. Klicka på Redigera bredvid alla dessa alternativ och anpassa efter dina behov. Se [Hjälp för varumärken och teman](feature-summary/themes.md) för mer information.

### Lägg till användare/användargrupper {#addusersusergroups}

Eftersom eleverna är de primära användarna av ditt utbildningsinnehåll är det primära steget att lägga till användare i systemet för hantering av inlärning. Lägg till användare i Learning Manager-programmet och tilldela dem roller. Du kan lägga till användare på följande sätt:

#### Lägg till användare (internt) {#addusersinternal}

* **Som en enskild användare** - Om du lägger till enskilda användare i Learning Manager-appen kan du testa med några av användarna innan du lägger till dem i grupp. Det här alternativet är också användbart om du vill lägga till fler enskilda användare vid behov, efter massimport av användare.
* **Självregistrering** - Med det här alternativet kan administratörer göra det möjligt för sina anställda att registrera sig för Learning Manager.
* **Massimport** (med CSV-överföring) - Med det här alternativet kan du importera användare i grupp till Learning Manager-programmet. En förutsättning är att du sparar listan över användare i CSV-format innan du använder den här funktionen.

#### Lägga till användare (externa profiler) {#addusersexternalprofiles}

* Genom extern registrering - Med det här alternativet kan du registrera externa avdelningsmedlemmar eller externa anställda i din organisation på programmet.

#### Lägg till användargrupper {#addusergroups}

Learning Manager-programmet genererar standardanvändargrupper baserat på liknande attribut. Förutom standardgrupperna kan du skapa anpassade användargrupper baserat på parametrar som beteckning, plats så att du kan använda dessa grupper i bland annat spelifiering och rapporter. Se [Hjälp för Lägg till användare](feature-summary/add-users-user-groups.md) för mer information.

### Tilldela roller {#assignroles}

När användarna har lagts till i Learning Manager kan administratören börja tilldela rollerna Författare, Administratör eller Integrationsadministratör till användarna enligt organisationens krav. Om du vill tilldela roller till användare kan du klicka på **[!UICONTROL Users]**  i den vänstra rutan markerar du kryssrutan vid varje användarnamn och klickar på **[!UICONTROL Actions]** för att välja den roll du vill tilldela. Chefsroller tilldelas användare av Adobe Learning Manager baserat på de roller/behörigheter som nämns av din organisation i CSV-filen. Du kan också ändra användarnas roller som chefer med hjälp av arbetsflödet Redigera användare. Se [Hjälp för Lägg till användare](feature-summary/add-users-user-groups.md) för mer information.

### Meddelandemallar {#notificationtemplates}

Meddelanden kan vara användbara för användare i ett system för hantering av inlärning som vill få information om sin status eller få information om händelserna/aktiviteterna. När du skapar kurser, konfigurerar funktionerna eller förbrukar kurser går användare igenom flera händelser som utlöser meddelanden till elever, chefer, administratörer eller författare. Learning Manager innehåller olika e-postmeddelandemallar i programmet. Du som är administratör kan anpassa dem enligt organisationens krav. Om du vill skapa e-postmeddelanden väljer du **E-postmallar** i den vänstra rutan och klicka på mallnamnet. Se [Hjälp för e-postmallar](feature-summary/email-templates.md) för mer information

**Inaktivera e-postmeddelanden (rekommenderas)**

Som standard är meddelandena aktiverade i Learning Manager-programmet. Du kan stänga av aviseringar i det här skedet om du inte vill meddela dina anställda i organisationen.

### Tecken {#badges}

Utmärkelsetecken är ett mått på prestation som din medarbetare kan tjäna på att ha slutfört en kurs. Yrkesverksamma över hela världen använder dessa utmärkelsetecken som en representation av en viss färdighet eller en utbildningsinsats. Du kan skapa en samling utmärkelsetecken så att du kan tilldela eleverna dem när utbildningsinnehållet är klart. Om du vill börja skapa märken kan du klicka på **[!UICONTROL Badges]** i den vänstra rutan. Se  [Hjälp för märken](feature-summary/badges.md) för mer information.

### Feedback {#feedback}

Feedback är en av de viktiga faktorerna i ett LMS för att mäta inlärningsförloppet hos elever och för att garantera kvalitet i utbildningsinnehållet. Learning Manager erbjuder två typer av feedback-alternativ till användare.

* Feedback om L1 är den feedback som elever ger efter att ha slutfört kursen.
* Feedback om L3 är den feedback som ges av chefer till elever baserat på kursens inverkan på elevernas beteende och dagliga aktiviteter.

Det är valfritt för organisationer att använda den här funktionen. Administratörer kan anpassa feedbackmallarna enligt organisationens krav. För att använda den här funktionen måste administratören aktivera alternativ för L1- och L3-feedback på kursinstansnivå. För att konfigurera feedback väljer du en kurs, klickar på Instansstandard i den vänstra rutan och aktiverar alternativet feedback. Se [Feedback-hjälp](feature-summary/courses.md) för mer information.

### Spelifiering {#gamification}

Att hålla elever engagerade medan de konsumerar innehållet är en av de utmaningar som organisationer står inför. Spelifiering ökar slutförandegraden genom att engagera och motivera elever att uppnå sina mål med spelteknik. Elever kan tävla med sina kollegor för att få poäng för olika utbildningsaktiviteter och uppnå brons-, silver-, guld- och platinanivåer. Administratörer kan aktivera/inaktivera varje spelifieringsuppgift och ändra tilldelningen av poäng till uppgifter. Learning Manager tillhandahåller spelifieringsfunktionen med vissa standardinställningar. Du kan börja använda funktionen med standardinställningarna under en tid och sedan välja att anpassa. Du behöver inte konfigurera/ändra inställningarna för den här funktionen. Om du har en ämnesexpert i din organisation rekommenderar vi att du konfigurerar inställningarna innan du använder den. Se [Hjälp med spelifiering](feature-summary/gamification.md) för mer information.

### Skapa utbildningsobjekt {#createlearningobjects}

Detta är det logiska stadiet där alla tre spåren (spår 1, spår 2 och spår 3) sammanstrålar så att du kan gå vidare med nästa åtgärd.

När du har skapat moduler och kurser kan du börja skapa utbildningsobjekt på högre nivå, som certifieringar, utbildningsprogram eller arbetsstöd för att gå vidare. Innan du börjar skapa utbildningsobjekt måste du se till att du redan har lagt till några användare i Learning Manager-programmet, skapat några moduler och kurser.

#### Skapa certifieringar {#createcertifications}

Certifiering är ett bevis på slutförande av ett utbildningsinnehåll eller ett bevis på prestation för elever på engångsbasis eller enligt en återkommande tidsram. Registrering av elever till utbildningsinnehåll kan ökas genom att ge certifiering till elever efter slutförande av kursen. Som administratör kan du skapa ett certifieringsprogram som antingen finns internt eller utförs av en tredje part. Definiera de kurser som en elev måste slutföra för att bli certifierad i den interna certifieringen. Innan du skapar certifieringen måste du se till att du har några kurser tillgängliga på kontot. Se  [Hjälp med certifiering](feature-summary/certifications.md) för mer information om hur du skapar certifieringar.

#### Skapa arbetsstöd {#createjobaids}

Arbetsstöd är ett arkiv med utbildningsinnehåll som är tillgängligt för elever utan några registrerings- eller slutförandekriterier. Elever kan hänvisa till dessa arbetsstöd när de är på jobbet för att få hjälp med att utföra någon aktivitet eller uppgift i en organisation. Även om det inte är obligatoriskt att använda arbetsstöd som en del av kursskapandet, rekommenderar Learning Manager-teamet att du skapar arbetsstöd som en bästa metod för din organisation. Se  [Hjälp med arbetsstöd](../authors/feature-summary/job-aids.md) för information om hur man skapar arbetsstöd.

#### Skapa utbildningsprogram {#createlearningprograms}

Utbildningsprogram är en uppsättning unikt utformade kurser som uppfyller specifika elevmål. Innan du skapar utbildningsprogram måste du se till att du redan har skapat några kurser eller att det finns befintliga kurser på ditt konto.  Även om det är valfritt för en organisation att använda den här funktionen rekommenderar Learning Manager-teamet dig att använda den för att inskärpa fokuserad utbildning för dina anställda. Om du vill börja använda utbildningsprogrammen klickar du på Utbildningsprogram i den vänstra rutan, väljer en uppsättning kurser i katalogen och publicerar. Se [Hjälp för utbildningsprogram](feature-summary/learning-programs.md) för specifika instruktioner.

### Skapa kataloger {#createcatalogs}

Du kan använda kataloger i en organisation för att skapa ett målinnehåll eller klassificera innehåll efter en definierad uppsättning elever. I Learning Manager är en katalog en samling utbildningsobjekt som kurser, certifieringar eller utbildningsprogram. Du kan välja önskade utbildningsobjekt när du skapar kataloger. Se till att du redan har skapat en uppsättning kurser, certifieringar eller utbildningsprogram innan du skapar katalogerna. Du kan skapa anpassade kataloger med en uppsättning utbildningsobjekt om du vill tilldela dem till interna eller externa användargrupper. Se  [Hjälp för kataloger](feature-summary/catalogs.md) för mer information om kataloger.

### Aktivera e-postmeddelanden/användaråtkomst {#turnonemailnotificationsuseraccess}

I det här skedet kan du aktivera e-postaviseringar för användarna i dina program och även aktivera användaråtkomst.

## Fas 3 - Författarkurser (författare) {#phase3authoringcoursesauthor}

Innehållsutvecklare eller författare i din organisation kan börja skapa utbildningsinnehållet. Det är obligatoriskt att du skapar moduler och kurser som utgör grunden för allt utbildningsinnehåll i Learning Manager-appen.

### Skapa moduler {#createmodules}

Moduler är de grundläggande byggstenarna i Learning Manager-programmet. Om du vill ordna ditt utbildningsinnehåll kan du börja skapa moduler som författare. Med Learning Manager kan du välja någon av de fyra typerna av kursmoduler, som klassrumsmoduler, moduler för eget tempo, Aktivitet och virtuella klassrum. Se  [Hjälp om moduler](../authors/how-to-choose-modules.md) för att lära dig vilken typ av kursmodul som passar bäst för din organisations behov.

### Skapa kurser {#createcourses}

Administratörer kan ta på sig rollen Författare i Learning Manager-programmet och skapa kurser. I Learning Manager-programmet är en kurs en grundläggande enhet med ett antal moduler som kan tilldelas eleven. Elever konsumerar kurser. Du kan börja skapa kurser genom att välja moduler du skapat tidigare, koppla kompetenser som du vill att elever ska uppnå från kursen, koppla nivåer, poäng och utmärkelsetecken till en kurs, välja arbetsstöd, förutsättningar och resurser baserat på ditt val och publicera kursen. Du kan också skapa flera instanser av en kurs så att du kan tilldela kursinstanserna till flera elever i olika tidszoner, scheman och så vidare. Se  [Hjälp med kurser](../authors/feature-summary/courses.md)för mer information om hur du skapar en kurs.

### Skapa utbildningsobjekt {#Createlearningobjects-1}

Detta är det logiska stadiet där alla tre spåren (spår 1, spår 2 och spår 3) sammanstrålar så att du kan gå vidare med nästa åtgärd.

När du har skapat moduler och kurser kan du börja skapa utbildningsobjekt på högre nivå, som certifieringar, utbildningsprogram eller arbetsstöd för att gå vidare. Innan du börjar skapa utbildningsobjekt måste du se till att du redan har lagt till några användare i Learning Manager-programmet, skapat några moduler och kurser.

#### Skapa certifieringar {#Createcertifications-1}

Certifiering är ett bevis på slutförande av ett utbildningsinnehåll eller ett bevis på prestation för elever på engångsbasis eller enligt en återkommande tidsram. Registrering av elever till utbildningsinnehåll kan ökas genom att ge certifiering till elever efter slutförande av kursen. Som administratör kan du skapa ett certifieringsprogram som antingen finns internt eller utförs av en tredje part. Definiera de kurser som en elev måste slutföra för att bli certifierad i den interna certifieringen. Innan du skapar certifieringen måste du se till att du har några kurser tillgängliga på kontot. Se  [Hjälp med certifiering](feature-summary/certifications.md) för mer information om hur du skapar certifieringar.

#### Skapa arbetsstöd {#CreateJobaids-1}

Arbetsstöd är ett arkiv med utbildningsinnehåll som är tillgängligt för elever utan några registrerings- eller slutförandekriterier. Elever kan hänvisa till dessa arbetsstöd när de är på jobbet för att få hjälp med att utföra någon aktivitet eller uppgift i en organisation. Även om det inte är obligatoriskt att använda arbetsstöd som en del av kursskapandet, rekommenderar Learning Manager-teamet att du skapar arbetsstöd som en bästa metod för din organisation. Se  [Hjälp med arbetsstöd](../authors/feature-summary/job-aids.md) för information om hur man skapar arbetsstöd.

#### Skapa utbildningsprogram {#Createlearningprograms-1}

Utbildningsprogram är en uppsättning unikt utformade kurser som uppfyller specifika elevmål. Innan du skapar utbildningsprogram måste du se till att du redan har skapat några kurser eller att det finns befintliga kurser på ditt konto.  Även om det är valfritt för en organisation att använda den här funktionen rekommenderar Learning Manager-teamet dig att använda den för att inskärpa fokuserad utbildning för dina anställda. Om du vill börja använda utbildningsprogrammen klickar du på Utbildningsprogram i den vänstra rutan, väljer en uppsättning kurser i katalogen och publicerar. Se [Hjälp för utbildningsprogram](feature-summary/learning-programs.md) för specifika instruktioner.

## Fas 4 - Hantera ditt LMS ( Learning Manager-administratör) {#phase4managingyourlmscaptivateprimeadministrator}

### Meddelanden {#announcements}

Meddelanden är användbara för organisationen för att samtidigt skicka viktig information till alla elever på ett konto. I Learning Manager-programmet är ett meddelande ett multimediemeddelande (text, bild eller video) som en administratör kan skapa och sända till en definierad uppsättning användargrupper och utbildningsobjekt. Du kan skicka meddelanden direkt eller schemalägga dem så att de utlöses automatiskt på ett visst datum. Om du vill använda den här funktionen i Learning Manager-programmet väljer du Meddelanden i den vänstra rutan och klickar på Lägg till för att skapa meddelanden. Se [Hjälp för meddelanden](feature-summary/announcements.md) för mer information.

### Användarregistrering {#userenrollment}

Användarregistrering är ett viktigt steg i ett LMS-program. I det här skedet kan du börja registrera eleverna för olika utbildningsobjekt i Learning Manager-programmet. Du kan registrera elever manuellt eller automatiserat genom att använda utbildningsplaner.

#### Manuell registrering {#manualenrollment}

* **Självregistrering -** Om du aktiverar det här alternativet när du skapar ett utbildningsobjekt kan elever registrera sig själva för utbildningsobjekten.
* **Chefsgodkännande** - Om du väljer detta alternativ i registreringstypen när du skapar en kurs måste cheferna godkänna elevens registrering.
* **Chefens nominering** - Om du väljer denna registreringstyp när kursen skapas måste sådana kurser nomineras av Chefer.
* **Administratörsregistrering** - I det här fallet kan administratören registrera några av eleverna utifrån organisationens krav.

Se [Hjälp med användarregistrering](feature-summary/courses.md)för mer information.

Registrera elever manuellt i utbildningsobjekt på följande fyra sätt:

### Automatisk registrering {#automatedenrollment}

Automatisera elevernas registrering till utbildningsobjekt med hjälp av utbildningsplaner.

#### Utbildningsplaner (baserat på utlösare) {#learningplansbasedontriggers}

Du kan använda utbildningsplaner för att automatiskt tilldela kurser, utbildningsprogram eller certifieringar till elever baserat på förekomsten av vissa händelser. Till exempel,

* Ny användare läggs till
* Användare ändrar användargrupp
* Eleven slutför ett utbildningsobjekt
* Användaren slutför en kompetens

Se [Hjälp för utbildningsplaner](feature-summary/learning-plans.md)  för mer information.

### Skapa rapporter {#createreports}

I det här skedet kan du börja skapa och hantera olika typer av rapporter.

Med Adobe Learning Manager kan du skapa olika rapporter för att följa, övervaka och kontrollera elevaktiviteter. Du kan använda följande tre typer av rapporteringsfunktioner för att generera rapporter:

* **Rapporttavla** - Skapa summeringsrapporter för att få användbara insikter om dina elevers förbrukning av utbildningsinnehåll, baserat på olika kategorier som användargrupper, effektivitet, elevers tid på kurser och så vidare.
* **Elevens betygsutdrag** - Skapa elevcentrerade rapporter med fullständig elevhistorik från registreringsdagen till i dag.
* **Kursrapporter** - Skapa elevens kurskonsumtionsstatistik från enskilda kurser. Du kan också skapa quiz-rapporter på kursnivå.

Se  [Hjälp för rapporter](feature-summary/reports.md) för mer information om rapportgenereringsprocessen.

Mer information om användning av Learning Manager-programfunktioner finns i [Hjälp för Learning Manager](../topics.md) baserat på varje roll.
