---
jcr-language: en_us
title: Installera Salesforce-paket
description: Learning Manager erbjuder ett Salesforce-programpaket. När de har installerats och konfigurerats i SFDC kan säljpersonal utföra sin utbildningsverksamhet inom SFDC-portalen. Med den här appen kan SFDC-användare utforska nya utbildningar, visa rekommendationer och konsumera dem direkt i SFDC-portalen. Användarna får också meddelandena som skickas av administratörer i form av mastheads direkt i appen inom SFDC-portalen.
contentowner: saghosh
source-git-commit: ab6737e8b43222a6538921b0628a504a5f15859d
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---



# Installera Salesforce-paket

## Översikt

Learning Manager erbjuder ett Salesforce-programpaket. När de har installerats och konfigurerats i SFDC kan säljpersonal utföra sin utbildningsverksamhet inom SFDC-portalen. Med den här appen kan SFDC-användare utforska nya utbildningar, visa rekommendationer och konsumera dem direkt i SFDC-portalen. Användarna får också meddelandena som skickas av administratörer i form av mastheads direkt i appen inom SFDC-portalen.

### Konfigurera i Learning Manager-appen

1. Logga in på ditt Learning Manager-administratörskonto som integrationsadministratör.
1. Klicka **[!UICONTROL Applications]** > **[!UICONTROL Featured Apps]**.
1. Klicka på **[!UICONTROL Salesforce]**.
1. Anteckna program-ID (kallas även klient-ID ) och klienthemligheten som nämns i beskrivningen på sidan Salesforce-program.
1. Klicka **[!UICONTROL Approve]** och programmet måste godkännas.
1. Klicka **[!UICONTROL Developer Resources]** > **[!UICONTROL Access Tokens for Testing and Development]**.
1. I avsnittet Hämta OAuth-kod måste klient-ID:et och omfånget vara inställt på - admin:read,admin:write. Klicka på **[!UICONTROL Submit]**.
1. Ange klient-ID och klienthemlighet i Hämta uppdateringstoken. Klicka **[!UICONTROL Submit]** och anteckna uppdateringstoken.

### Skapa konto i Salesforce-program

1. Skapa ett konto på registreringssidan för Salesforce. Du måste skapa ett Salesforce-konto i en utvecklar- eller enterprise-version.  [URL för utvecklarregistrering](https://developer.salesforce.com/signup). Se till att du använder e-post-ID för att registrera dig för Salesforce som du har använt för Learning Manager.
1. Verifiera ditt konto via e-postmeddelandet.
1. Skapa ett lösenord och logga in på Salesforce.
1. Observera Salesforce-URL:en efter inloggning (till exempel site.lightning.force.com)

### Installera Learning Manager-paket

Om du vill installera paketet måste du först ta bort det befintliga paketet i Salesforce. Innan du avinstallerar måste du aktivera inställningarna, som visas nedan. Att tillämpa dessa inställningar är obligatoriskt, annars kan du inte installera paketet.

![](assets/uninstall-package.png)

*Installera Learning Manager-paketet*

>[!NOTE]
>
>Adobe Learning Manager-appen stöds bara i Salesforce Lightning-vyn.

1. Starta  [URL till Learning Manager-paket](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Ftest.salesforce.com%2Fpackaging%2FinstallPackage.apexp%3Fp0%3D04t1k0000008YWn&amp;data=04%7C01%7Ckillamse%40adobe.com%7Cf588f553fc694d2edee108d9a5c74711%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C637723097572585825%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=mhYKVdwvS4F7WPruy0Kvw%2FsqgWxzTQpaZJyEACu8CNw%3D&amp;reserved=0).
1. I dialogrutan **Inloggning** sida, klicka på **[!UICONTROL Use Custom Domain]**.

1. Ange paketets URL och klicka på **[!UICONTROL Continue]**. Alternativet Installera endast för administratörer måste vara markerat på installationssidan. Ändra inte det här alternativet.
1. Klicka **INShög**. När paketet har installerats klickar du på **[!UICONTROL Done]**. Du kommer till sidan Installerade paket och kan se Adobe Learning Manager-installationspaketet.

1. Gå till Appstartaren (bredvid Konfiguration) och sök efter Adobe Learning Manager.
1. Om du vill konfigurera programmet klickar du på **[!UICONTROL Configure]**.
1. Klicka **[!UICONTROL New]** och lägg till följande information:

   * **Konfiguration:** Ange ett namn du vill använda.
   * **Klient-ID**: Ange värdet som du fick från det första avsnittet.
   * **Klienthemlighet:** Ange värdet som du fick från det första avsnittet.
   * **RefreshToken:** Ange värdet som du fick från det första avsnittet.
   * **LearningManagerBaseURL:** URL till webbplatsen där Learning Manager finns.
   * **Inaktivera omdirigering:** Inaktivera omdirigering till elevens startsida i Learning Manager.

>[!NOTE]
>
>Du kan bara skapa en enda konfiguration. Om du försöker lägga till en annan konfiguration visas ett felmeddelande. Konfigurationen mappar Salesforce-kontot med elevkontot.

### Lägg till fjärrplatsinställningar

1. Klicka på i det övre högra hörnet på sidan **[!UICONTROL Setup]**.
1. in **Snabbsökning**, sök efter Inställningar för fjärrplats.
1. Klicka på **[!UICONTROL New Remote Site]**.
1. Ange uppgifterna:

   1. **Namn på fjärrplats:** Ange ett namn du vill använda.
   1. **URL för fjärrwebbplats:** URL till webbplatsen där Learning Manager finns.

1. Starta Learning Manager.

### Aktivera meddelanden för Learning Manager-appen

1. Klicka på i det övre högra hörnet **Konfiguration**.
1. Sök efter anpassade meddelanden.
1. Klicka på **[!UICONTROL New]**.
1. Ange följande uppgifter:

   1. **Anpassat aviseringsnamn:** LearningManagerNotification
   1. **API-namn:** LearningManagerNotification

1. Välj båda **Skrivbord** och **Mobil** som kanaler som stöds.

1. Klicka på **[!UICONTROL Save]**.
1. Följ stegen nedan för att aktivera push-meddelanden för mobila enheter:

   1. Installera Salesforce-mobilappen i din mobiltelefon.
   1. Logga in på programmet med dina inloggningsuppgifter.
   1. Gå till **Konfiguration** > **Inställningar för meddelandeleverans**.
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

När du installerar paketet skapas en ny behörighetsgrupp, **Användare av Adobe Learning Manager**. Gå till behörighetsgruppen och lägg sedan till användarna.

Välj användare och tilldela behörigheter i enlighet med detta. Eleverna kan nu komma åt Learning Manager-appen.

Välj sedan en profil, till exempel en standardprofil för en användare, och klicka på profilen. Klicka **[!UICONTROL Edit]** och i **Anpassade appinställningar** -avsnittet, aktivera kryssrutan **Adobe Learning Manager**. Detta gör programmet tillgängligt för användaren.

I dialogrutan **Anpassade flikinställningar** avsnitt i **Startsida för elev** listruta väljer du alternativet **[!UICONTROL Default On]**.

Du måste göra programmet synligt för alla profiler.

Klicka **[!UICONTROL Save]** och eleverna som tillhör alla profiler får tillgång till Learning Manager-appen.
