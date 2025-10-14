---
description: Installera Microsoft Teams-anslutning i Adobe Learning Manager
jcr-language: en_us
title: Installera Microsoft Teams-anslutning i Adobe Learning Manager
contentowner: saghosh
exl-id: 68092187-ac69-4727-a3dc-f3047a1e164d
source-git-commit: 6192559436074c3270644850b202589961e7b81b
workflow-type: tm+mt
source-wordcount: '1094'
ht-degree: 0%

---

# Installera Microsoft Teams-anslutning i Adobe Learning Manager

## Översikt

Microsoft Teams ® är en beständig chattbaserad samarbetsplattform som har fullt stöd för dokumentdelning, onlinemöten och andra funktioner för affärskommunikation.

Adobe Learning Manager använder en virtuell klassrumskontakt som kan användas för att integrera Microsoft Teams-möten med Learning Manager.

Microsoft Teams-anslutning ansluter Learning Manager- och Microsoft Teams-system för att möjliggöra automatisk virtuell mötessynkronisering. I följande lista visas anslutningsmöjligheterna för Microsoft Teams:

**Konfigurera virtuella sessioner med Microsoft Teams**

Med den här anslutningen kan du integrera ditt Adobe Learning Manager-konto med ditt Microsoft Teams-konto. Anslutningen gör det möjligt för en författare i Learning Manager att använda Microsoft Teams som teknikleverantör för de virtuella klassrumsmoduler som skapas i Learning Manager.

**Tillåt Microsoft Teams att autentisera elever vid inträde i virtuellt klassrum**

Med den här anslutningen kan du konfigurera Microsoft Teams Meeting Organizer från Learning Manager när du skapar ett möte. Mötesorganisatören kan hantera lobbyn för att begränsa eller tillåta inträde i ett möte samt kontrollera andra mötesalternativ som tillhandahålls av Microsoft Teams.

**Använd automatisk synkronisering av användarslutförande**

Med den automatiska synkroniseringsprocessen för slutförande av användare kan en Learning Manager-administratör automatiskt hämta slutförandeposterna och URL-inspelningen för Microsoft Teams-mötet.

## Roller i Microsoft Teams

Om du organiserar ett möte med flera deltagare kan du tilldela roller till varje deltagare så att en deltagare kan veta vad han/hon kan göra i mötet.

Det finns två roller att välja mellan: **presentatör** och **deltagare**.

Mer information finns i [Roller i ett teammöte - Microsoft](https://support.microsoft.com/en-us/office/roles-in-a-teams-meeting-c16fa7d0-1666-4dde-8686-0a0bfe16e019).

## Konfigurera Microsoft Teams-anslutning

>[!NOTE]
>
>Objekt som är märkta &lt;Developer/Optional> nedan är valfria och mest för att konfigurera testversions-/utvecklarklienter med Microsoft om användaren inte har en produktionsanvändare. Dessa är valfria eftersom de för det mesta redan skulle ha utförts av teamets administratör.

## Skapa ett utvecklarkonto för E5 Microsoft &lt;Developer/Optional>

Du kan använda Microsoft Teams-anslutning om du har Office 365 E3 eller Office 365 E5. Det rekommenderade alternativet är Office 365 E5.

* Gå till sidan [Microsoft-planer](https://www.microsoft.com/en-in/microsoft-365/enterprise/compare-office-365-plans?&ef_id=CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE:G:s&OCID=AID2100137_SEM_CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE:G:s&lnkd=Google_O365SMB_Brand&gclid=CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE). På webbsidan kan du antingen köpa E3- eller E5-konto eller klicka på Prova gratis.
* Ange den information som krävs och skapa ett konto.

>[!NOTE]
>
>Kontot måste använda formatet `<username>@<company name>.onmicrosoft.com`.

## Skapa program för Microsoft Teams-anslutning

1. Gå till [Microsoft Azure®-portalen](https://portal.azure.com/).
1. Logga in med Microsoft E5-kontot som du skapade i föregående avsnitt.
1. Sök efter **Azure Active Directory**.
1. Klicka på **[!UICONTROL App Registrations]**.
1. Klicka på **[!UICONTROL New Registration]**, ange följande information och registrera programmet:

   1. **Namn** - valfritt namn.
   1. **Kontotyper som stöds** - Konton i valfri organisationskatalog (valfri Azure Active Directory - multitenant).
   1. **Omdirigerings-URI (valfritt)** - valfritt fält som anger svars-URL:en.

1. Lägg märke till följande ID i kolumnen **Essentials**, som kommer att användas mer under integreringen:

   1. **Program-ID (klient)**
   1. **Katalog-ID (klient)**

1. Sök efter klientautentiseringsuppgifter och klicka på **[!UICONTROL Add a certificate or secret]**.
1. Klicka på **[!UICONTROL New Client secret]** och lägg till följande information:

   1. **Beskrivning** - Ange ett namn.
   1. **Förfaller** - Ställ in på valfritt värde (rekommenderat värde är 24 månader. Se till att nya klientautentiseringsuppgifter genereras när den föregående har upphört att gälla).

Observera klientsekretessen, som kommer att användas ytterligare under integreringen.

## Skaffa åtkomstbehörighet till Microsoft Teams-kopplingen

1. Gå till [Microsoft Azure-portalen](https://portal.azure.com/).
1. Logga in med Microsoft E5 som du skapade tidigare.
1. Sök efter **Azure Active Directory**.
1. Klicka på **[!UICONTROL App Registrations]**.
1. Klicka på programmet som du skapade i föregående avsnitt.
1. Klicka på **[!UICONTROL API permissions]**.
1. Klicka på **[!UICONTROL Add a permission]**.
1. Välj **[!UICONTROL Microsoft Graph]** > **[!UICONTROL Application permissions]** och lägg till följande behörigheter:

   1. Chat.Read.All
   1. Directory.Read.All
   1. OnlineMeetingArtifact.Read.All
   1. OnlineMeetings.Read.All
   1. OnlineMeetings.ReadWrite.All
   1. User.Read.All
   1. OnlineMeetingRecording.Read.All

1. Klicka på **[!UICONTROL Grant admin access for Adobe]**.
1. Klicka på **[!UICONTROL App roles]** > **[!UICONTROL Create app role]**.
1. Ange följande värden:

   1. **Visningsnamn** - Namn på API-/behörighetsnamnet (till exempel Calendars.ReadWrite).

   1. **Tillåtna medlemstyper** - Ange både användare och program (Användare/Grupper + Program).

   1. **Värde** - Namn på API-/behörighetsnamnet (till exempel Calendars.ReadWrite).

   1. **Beskrivning** - Namn på API-/behörighetsnamnet (till exempel Calendars.ReadWrite).

   1. **Vill du aktivera den här programrollen?** - Markera den här kryssrutan.

1. Upprepa de föregående stegen för alla nio API:er/behörigheter som har lagts till.

## Konfigurera åtkomstpolicyn med hjälp av PowerShell-skript

Om du vill konfigurera programåtkomstprincipen för Microsoft Teams-anslutningen genom att köra PowerShell-skript följer du proceduren som beskrivs i det här [dokumentet](https://docs.microsoft.com/en-us/graph/cloud-communication-online-meeting-application-access-policy).

Detta gör det möjligt för kontakten att få tillgång till Microsoft Teams onlinemöten.

>[!NOTE]
>
>I dokumentet ovan utför du valfritt steg 5 också för att se till att alla aktiva användare kan tilldelas rollen som arrangör från Learning Manager Author-appen. Om det här steget inte utförs kommer användare inte att ha åtkomstbehörighet att vara organisatörer och det går inte att skapa möten (Microsoft API:er anser att organisatören skapar ett teammöte).

## Konfigurera Microsoft Teams-anslutning i Learning Manager

1. Logga in i Learning Manager som **integrationsadministratör**.

1. På sidan Anslutningar väljer du Microsoft Teams-anslutning och klickar på **[!UICONTROL Connect]**.

1. Ange följande värden:

   1. **Anslutningsnamn** - Ange namnet som författaren ska se när sessionen skapas.

   1. **Microsoft Teams-klient-ID** - Ange det tidigare fastställda värdet.

   1. **Microsoft Teams-klient-ID** - Ange det tidigare fastställda värdet.

   1. **Microsoft Teams-klienthemlighet** - Ange det tidigare fastställda värdet.

   1. **Microsoft Teams Admin-användarmeddelande** - Ange standardepostadress för organisatören. Denna användare (vanligtvis en tjänstanvändare) skapar mötet om ingen uttrycklig organisatör väljs från Learning Manager-författarappen.

## Tilldela användare licenser &lt;Developer/Optional>

1. Besök [https://admin.microsoft.com/#/homepage](https://admin.microsoft.com/#/homepage).
1. Klicka på **[!UICONTROL Users]** > **[!UICONTROL Active Users]**.
1. Klicka på **[!UICONTROL More actions for Users]** för de användare som du vill ge åtkomst till Microsoft Teams.
1. Klicka på **[!UICONTROL Manage Product Licenses]**.
1. Aktivera licens för Office 365 E5 utan ljudkonferenser.

<!--## Record a session

The API used for recording a session is a protected API. To access the API, you must request access from Microsoft. For more information, see this  [document](https://docs.microsoft.com/en-us/graph/teams-protected-apis).

In the document,

*"To request access to these protected APIs, complete the following  [request form](https://aka.ms/teamsgraph/requestaccess). We review access requests every Wednesday and deploy approvals every Friday, except during major holiday weeks in the U.S. Submissions during those weeks will be processed the following non-holiday week. To verify whether your request has been approved, test your application access on the next applicable Monday."*

For learners, the recording URL is displayed on the VC course overview page.

After 30 minutes of completing a course, the attendance for the learner gets marked. -->

## Vanliga frågor

+++Vem är organisatör och presentatör?

I [dokumentationen](https://support.microsoft.com/en-us/office/roles-in-a-teams-meeting-c16fa7d0-1666-4dde-8686-0a0bfe16e019) från Microsoft finns information om olika funktioner som stöds av Microsoft Teams.

+++

+++Bör en organisatör vara registrerad användare i både Learning Manager och Microsoft Teams?

Ja, arrangören bör också vara en del av både Learning Manager och Microsoft Teams. Dessutom måste organisatören vara en del av samma Microsoft-klient som är konfigurerad i integrationsadministratörsappen.

+++

+++Ska en presentatör vara registrerad användare i både Learning Manager och Microsoft Teams?

Ja, presentatören bör också ingå i både Learning Manager och Microsoft Teams. Presentatören måste ha ett Azure Active Directory-ID (kan vara en del av samma klientorganisation som organisatören eller en del av en annan klientorganisation). Dessutom kan även anonyma användare (användare som bara loggar in med användarnamnet och inte en del av Active Directory) göras till presentatörer av organisatören/befintliga presentatörer under mötet.

+++

+++Microsoft Teams har möten, webbseminarier och liveevenemang. Vilken stöder Teams-anslutningen?

För närvarande stöder Teams-anslutningen bara Meetings i Microsoft Teams. Mer information finns i det här [dokumentet](https://docs.microsoft.com/en-us/microsoftteams/quick-start-meetings-live-events).

+++
