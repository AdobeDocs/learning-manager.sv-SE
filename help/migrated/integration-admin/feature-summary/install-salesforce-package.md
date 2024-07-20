---
jcr-language: en_us
title: Installera Salesforce-paket
description: Learning Manager erbjuder ett Salesforce-programpaket. När de har installerats och konfigurerats i SFDC kan säljpersonal utföra sin utbildningsverksamhet inom SFDC-portalen. Med den här appen kan SFDC-användare utforska nya utbildningar, visa rekommendationer och konsumera dem direkt i SFDC-portalen. Användarna får också meddelandena som skickas av administratörer i form av mastheads direkt i appen inom SFDC-portalen.
contentowner: saghosh
exl-id: 2b1c32e7-81af-4c13-a2bd-66684cde084e
source-git-commit: fb946ae98dce45156e2f4c1cf992319405403ea9
workflow-type: tm+mt
source-wordcount: '1012'
ht-degree: 0%

---

# Installera Salesforce-paket

## Översikt

Learning Manager erbjuder ett Salesforce-programpaket. När de har installerats och konfigurerats i SFDC kan säljpersonal utföra sin utbildningsverksamhet inom SFDC-portalen. Med den här appen kan SFDC-användare utforska nya utbildningar, visa rekommendationer och konsumera dem direkt i SFDC-portalen. Användarna får också meddelandena som skickas av administratörer i form av mastheads direkt i appen inom SFDC-portalen.

### Konfigurera i Learning Manager-appen

1. Logga in på ditt Learning Manager-administratörskonto som integrationsadministratör.
1. Klicka på **[!UICONTROL Applications]** > **[!UICONTROL Featured Apps]**.
1. Klicka på **[!UICONTROL Salesforce]**.
1. Anteckna program-ID (kallas även klient-ID ) och klienthemligheten som nämns i beskrivningen på sidan Salesforce-program.
1. Klicka på **[!UICONTROL Approve]** så måste programmet godkännas.
1. Klicka på **[!UICONTROL Developer Resources]** > **[!UICONTROL Access Tokens for Testing and Development]**.
1. I avsnittet Hämta OAuth-kod måste klient-ID:et och omfånget vara inställt på - admin:read,admin:write. Klicka på **[!UICONTROL Submit]**.
1. Ange klient-ID och klienthemlighet i Hämta uppdateringstoken. Klicka på **[!UICONTROL Submit]** och notera uppdateringstoken.

### Skapa konto i Salesforce-program

1. Skapa ett konto på registreringssidan för Salesforce. Du måste skapa ett Salesforce-konto i en utvecklar- eller enterprise-version.  [URL för registrering av utvecklare](https://developer.salesforce.com/signup). Se till att du använder e-post-ID för att registrera dig för Salesforce som du har använt för Learning Manager.
1. Verifiera ditt konto via e-postmeddelandet.
1. Skapa ett lösenord och logga in på Salesforce.
1. Observera Salesforce-URL:en efter inloggning (till exempel site.lightning.force.com)

### Installera Learning Manager-paket

Om du vill installera paketet måste du först ta bort det befintliga paketet i Salesforce. Innan du avinstallerar måste du aktivera inställningarna, som visas nedan. Att tillämpa dessa inställningar är obligatoriskt, annars kan du inte installera paketet.

![](assets/uninstall-package.png)

*Installera Learning Manager-paketet*

>[!NOTE]
>
>Adobe Learning Manager-programmet stöds bara i Salesforce Lightning-vyn.

1. Starta [URL till Learning Manager-paketet](https://test.salesforce.com/packaging/installPackage.apexp?p0=04tDb000000LRvP).
1. Klicka på **[!UICONTROL Use Custom Domain]** på sidan **Inloggning**.

1. Ange paketets URL och klicka på **[!UICONTROL Continue]**. Alternativet Installera endast för administratörer måste vara markerat på installationssidan. Ändra inte det här alternativet.
1. Klicka på **Inshög**. Klicka på **[!UICONTROL Done]** när paketet har installerats. Du kommer till sidan Installerade paket där du kan se det installerade Adobe Learning Manager-paketet.

1. Gå till Appstartaren (bredvid Konfiguration) och sök efter Adobe Learning Manager.
1. Klicka på **[!UICONTROL Configure]** om du vill konfigurera programmet.
1. Klicka på **[!UICONTROL New]** och lägg till följande information:

   * **Konfiguration:** Ange ett namn som du vill använda.
   * **ClientID**: Ange värdet som du fick från det första avsnittet.
   * **Klienthemlighet:** Ange värdet som du fick från det första avsnittet.
   * **RefreshToken:** Ange värdet som du fick från det första avsnittet.
   * **LearningManagerBaseURL:** URL:en till webbplatsen där Learning Manager finns.
   * **Inaktivera omdirigering:** Inaktivera omdirigering till elevens startsida i Learning Manager.

>[!NOTE]
>
>Du kan bara skapa en enda konfiguration. Om du försöker lägga till en annan konfiguration visas ett felmeddelande. Konfigurationen mappar Salesforce-kontot med elevkontot.

### Lägg till fjärrplatsinställningar

1. Klicka på **[!UICONTROL Setup]** i det övre högra hörnet på sidan.
1. Sök efter fjärrplatsinställningar i **Snabbsökning**.
1. Klicka på **[!UICONTROL New Remote Site]**.
1. Ange uppgifterna:

   1. **Namn på fjärrplats:** Ange ett namn som du väljer.
   1. **URL till fjärrwebbplats:** URL till webbplatsen där Learning Manager finns.

1. Starta Learning Manager.

### Lägg till Adobe-domänen i Betrodda Salesforce-URL:er

Så här lägger du till Adobe-domänen i betrodda URL:er:

1. Gå till **[!UICONTROL Setup]** > **[!UICONTROL Quick Find]** i Salesforce-konsolen.
1. Sök efter **[!UICONTROL Trusted URLs]** och välj **[!UICONTROL New Trusted URL]**.
1. Skriv ett namn i fältet **[!UICONTROL API Name]**.
1. Skriv `*.adobe.com` i URL-fältet.
1. Markera alla kryssrutor i **CSP-direktiv** och spara ändringarna.
1. Redigera uppdateringstoken för Salesforce-programmet och spara den.
1. Starta om Salesforce-programmet.

### Aktivera meddelanden för Learning Manager-appen

1. Klicka på **Inställningar** i det övre högra hörnet.
1. Sök efter anpassade meddelanden.
1. Klicka på **[!UICONTROL New]**.
1. Ange följande uppgifter:

   1. **Anpassat aviseringsnamn:** LearningManagerNotification
   1. **API-namn:** LearningManagerNotification

1. Välj både **Dator** och **Mobil** som kanaler som stöds.

1. Klicka på **[!UICONTROL Save]**.
1. Följ stegen nedan för att aktivera push-meddelanden för mobila enheter:

   1. Installera Salesforce-mobilappen i din mobiltelefon.
   1. Logga in på programmet med dina inloggningsuppgifter.
   1. Gå till **Inställningar** > **Inställningar för meddelandeleverans**.
   1. Lägg till Salesforce för iOS och Android.

### Avinstallera Learning Manager från Salesforce

1. Gå till Installerade paket i Salesforce-programmet.
1. Klicka på **[!UICONTROL Uninstall]**.

## Konfigurera Learning Manager för Salesforce-användare

Learning Manager-programmet är också tillgängligt för användare som finns på alla Salesforce-konton. Salesforce-administratören kan lägga till användare baserat på profilerna. Salesforce-profilerna liknar dem i Learning Manager. Det kan till exempel gälla Administratör, Integreringsadministratör, Instruktör och så vidare. Salesforce-administratören kan också skapa en anpassad profil.

### Profil

Som Salesforce-administratör kan du antingen tilldela användare profilerna eller skapa en anpassad profil.

>[!NOTE]
>
>Användarna måste finnas i både Salesforce och Learning Manager.

![](assets/create-profile.png)

*Tilldela en elev en profil*

När du lägger till en elev måste du tilldela eleven en specifik profil. Gå sedan till den profilen och ge den åtkomst som krävs.

För att elever ska kunna se Learning Manager-appen måste du aktivera den för alla elever.

Nästa steg är att ge behörighet för åtkomst till Learning Manager-appen.

![](assets/permission-set.png)

*Lägg till behörigheter för att komma åt Learning Manager-appen*

När du installerar paketet skapas en ny behörighetsgrupp, **Adobe Learning Manager-användare**. Gå till behörighetsgruppen och lägg sedan till användarna.

Välj användare och tilldela behörigheter i enlighet med detta. Eleverna kan nu komma åt Learning Manager-appen.

Välj sedan en profil, till exempel en standardprofil för en användare, och klicka på profilen. Klicka på **[!UICONTROL Edit]** och aktivera kryssrutan **Adobe Learning Manager** i avsnittet **Anpassade appinställningar**. Detta gör programmet tillgängligt för användaren.

Välj alternativet **[!UICONTROL Default On]** i avsnittet **Anpassade flikinställningar** i listrutan **Elevens startsida**.

Du måste göra programmet synligt för alla profiler.

Klicka på **[!UICONTROL Save]** så får eleverna som tillhör alla profiler åtkomst till Learning Manager-appen.
