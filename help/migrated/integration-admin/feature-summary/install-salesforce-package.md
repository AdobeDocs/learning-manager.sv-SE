---
jcr-language: en_us
title: Installera Salesforce-paket
description: Learning Manager erbjuder ett Salesforce-apppaket. När de har installerats och konfigurerats i SFDC kan försäljningsanställda utföra sina utbildningsaktiviteter i SFDC-portalen. Den här appen gör det möjligt för SFDC-användare att utforska nya utbildningar, visa rekommendationer och konsumera dem direkt i SFDC-portalen. Användare får också meddelanden som skickas av administratörer i form av toppannonser direkt i appen i SFDC-portalen.
contentowner: saghosh
exl-id: 2b1c32e7-81af-4c13-a2bd-66684cde084e
source-git-commit: fb946ae98dce45156e2f4c1cf992319405403ea9
workflow-type: tm+mt
source-wordcount: '1012'
ht-degree: 0%

---

# Installera Salesforce-paket

## Översikt

Learning Manager erbjuder ett Salesforce-apppaket. När de har installerats och konfigurerats i SFDC kan försäljningsanställda utföra sina utbildningsaktiviteter i SFDC-portalen. Den här appen gör det möjligt för SFDC-användare att utforska nya utbildningar, visa rekommendationer och konsumera dem direkt i SFDC-portalen. Användare får också meddelanden som skickas av administratörer i form av toppannonser direkt i appen i SFDC-portalen.

### Konfigurera i Learning Manager-appen

1. Logga in på ditt Learning Manager Admin-konto som Integration Admin.
1. Klicka på **[!UICONTROL Applications]** > **[!UICONTROL Featured Apps]**.
1. Klicka på **[!UICONTROL Salesforce]**.
1. På sidan Salesforce-appen noterar du program-ID:t (även kallat klient-ID) och klienthemligheten som nämns i beskrivningen.
1. Klicka på **[!UICONTROL Approve]** och din app måste godkännas.
1. Klicka på **[!UICONTROL Developer Resources]** > **[!UICONTROL Access Tokens for Testing and Development]**.
1. I avsnittet Hämta OAuth-kod måste klient-ID:t och omfånget anges till - admin:read,admin:write. Klicka på **[!UICONTROL Submit]**.
1. I Hämta uppdateringstoken anger du klient-ID och klienthemlighet. Klicka **[!UICONTROL Submit]** och anteckna uppdateringstoken.

### Skapa konto i Salesforce-appen

1. Skapa ett konto på registreringssidan för Salesforce. Du måste skapa ett Salesforce-konto i utvecklar- eller företagsutgåvan.  [Webbadress för](https://developer.salesforce.com/signup) registrering för utvecklare. Se till att du måste använda e-post-ID:t för att registrera dig för Salesforce som du använde för Learning Manager.
1. Verifiera ditt konto via verifieringsmailet.
1. Skapa ett lösenord och logga in på Salesforce.
1. Notera Salesforce-url:en efter inloggning (t.ex. site.lightning.force.com)

### Installera Learning Manager-paketet

Om du vill installera paketet måste du först ta bort det befintliga paketet i Salesforce. Innan du avinstallerar måste du aktivera inställningarna, som visas nedan. Det är obligatoriskt att använda dessa inställningar, annars kommer du inte att kunna installera paketet.

![](assets/uninstall-package.png)

*Installera Learning Manager-paketet*

>[!NOTE]
>
>Adobe Learning Manager-appen stöds endast i Salesforce Lightning-vyn.

1. Starta url:en  [för](https://test.salesforce.com/packaging/installPackage.apexp?p0=04tDb000000LRvP) Learning Manager-paketet.
1. På inloggningssidan **** klickar du på **[!UICONTROL Use Custom Domain]**.

1. Ange paketets URL och klicka på **[!UICONTROL Continue]**. Installationssidan måste ha alternativet Installera endast för administratörer markerat. Ändra inte det här alternativet.
1. Klicka på **Install**. När paketet är installerat klickar du på **[!UICONTROL Done]**. Du dirigeras till sidan Installerade paket och du kan se det installerade Adobe Learning Manager-paketet.

1. Gå till startprogrammet (bredvid Inställningar) och sök efter Adobe Learning Manager.
1. Konfigurera appen genom att klicka på **[!UICONTROL Configure]**.
1. Klicka **[!UICONTROL New]** och lägg till följande information:

   * **Config:** Ange ett namn som du väljer.
   * **ClientID:** Ange det värde som du fick från det första avsnittet.
   * **ClientSecret:** Ange det värde som du fick från det första avsnittet.
   * **RefreshToken:** Ange det värde som du fick från det första avsnittet.
   * **LearningManagerBaseURL:** URL:en till den webbplats där Learning Manager finns.
   * **Inaktivera omdirigering:** Inaktivera omdirigering till elevens startsida i Learning Manager.

>[!NOTE]
>
>Du kan bara skapa en enda konfiguration. Om du försöker lägga till en annan konfiguration visas ett felmeddelande. Konfigurationen mappar Salesforce-kontot med Learner-kontot.

### Lägg till inställningar för fjärrplats

1. I det övre högra hörnet på sidan klickar du på **[!UICONTROL Setup]**.
1. I **Snabbsökning** söker du efter Inställningar för fjärrplats.
1. Klicka på **[!UICONTROL New Remote Site]**.
1. Ange detaljerna:

   1. **Namn på fjärrplats:** Ange ett namn som du väljer.
   1. **URL för fjärrplats:** URL:en för den webbplats där Learning Manager finns.

1. Starta Learning Manager.

### Lägg till Adobe-domänen i Salesforce betrodda URL:er

Så här lägger du till Adobe-domänen i betrodda URL:er:

1. I Salesforce-konsolen går du till **[!UICONTROL Setup]** > **[!UICONTROL Quick Find]**.
1. Sök efter **[!UICONTROL Trusted URLs]** och välj **[!UICONTROL New Trusted URL]**.
1. Skriv ett namn i **[!UICONTROL API Name]** fältet.
1. Skriv `*.adobe.com` in i URL-fältet.
1. Markera alla kryssrutor i **CSP-direktiv** och spara ändringarna.
1. Redigera uppdateringstoken för Salesforce-appen och spara den.
1. Starta om Salesforce-appen.

### Aktivera aviseringar för Learning Manager-appen

1. I det övre högra hörnet klickar du på **Inställningar**.
1. Sök efter anpassade aviseringar.
1. Klicka på **[!UICONTROL New]**.
1. Ange följande information:

   1. **Namn på anpassad avisering:** LearningManagerNotification
   1. **API-namn:** LearningManagerNotification

1. Välj både **Dator** och **Mobil** som kanaler som stöds.

1. Klicka på **[!UICONTROL Save]**.
1. För att aktivera push-meddelanden för mobila enheter, följ stegen nedan:

   1. Installera Salesforce-mobilappen i din mobiltelefon.
   1. Logga in på appen med dina inloggningsuppgifter.
   1. Gå till **Inställningar** > **inställningar för** meddelandeleverans.
   1. Lägg till Salesforce för iOS och Android.

### Avinstallera Learning Manager från Salesforce

1. I Salesforce-appen går du till Installerade paket.
1. Klicka på **[!UICONTROL Uninstall]**.

## Konfigurera Learning Manager för Salesforce-användare

Learning Manager-appen är också tillgänglig för användare som finns i alla Salesforce-konton. Salesforce-administratören kan lägga till användare baserat på profilerna. Salesforce-profilerna liknar vad de är i Learning Manager. Till exempel Administratör, Integrationsadministratör, Instruktör och så vidare. Salesforce-administratören kan också skapa en anpassad profil.

### Profil

Som Salesforce-administratör kan du antingen tilldela profilerna till användare eller skapa en anpassad profil.

>[!NOTE]
>
>Användarna måste finnas i både Salesforce och Learning Manager.

![](assets/create-profile.png)

*Tilldela en profil till en elev*

När du lägger till en elev måste du tilldela en specifik profil till eleven. Gå sedan till den profilen och bevilja den åtkomst som krävs.

För att elever ska kunna se Learning Manager-appen måste du aktivera appen för alla elever.

Nästa steg är att ge behörighet att komma åt Learning Manager-appen.

![](assets/permission-set.png)

*Lägga till behörigheter för att få åtkomst till Learning Manager-appen*

När du installerar paketet skapas en ny behörighetsgrupp, **Adobe Learning Manager User**. Gå till behörighetsgruppen och lägg sedan till användarna.

Välj användare och tilldela behörigheterna därefter. Eleverna kan nu komma åt appen Learning Manager.

Välj nu en profil, till exempel Standardprofil för en användare, och klicka på profilen. Klicka på **[!UICONTROL Edit]** och markera kryssrutan **Adobe Learning Manager** i **avsnittet Anpassade appinställningar**. Detta gör appen tillgänglig för användaren.

I avsnittet Inställningar för **anpassad flik** i **listrutan Startsida** väljer du alternativet **[!UICONTROL Default On]**.

Du måste göra appen synlig för alla profiler.

Klicka och **[!UICONTROL Save]** eleverna som tillhör alla profiler kommer åt Learning Manager-appen.
