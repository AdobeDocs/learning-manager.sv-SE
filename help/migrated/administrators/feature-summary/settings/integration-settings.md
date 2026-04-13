---
description: Läs mer om hur integreringsinställningar kopplar Adobe Learning Manager till tredjepartslösningar
jcr-language: en_us
title: Integreringsinställningar i Adobe Learning Manager
source-git-commit: 03123dcd8d9066cdfcb0fe97e61acb3df625a23e
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 0%

---


# Integreringsinställningar i Adobe Learning Manager

## Inloggningsmetoder

Adobe Learning Manager tillhandahåller flera inloggningsmetoder för att säkerställa säker och flexibel åtkomst för interna och externa användare. Administratörer kan konfigurera de här inloggningsmetoderna utifrån organisationens krav.

Följande inloggningsmetoder är tillgängliga:

* ADOBE LEARNING MANAGER ID
* Adobe ID
* Enkel inloggning (SSO)

### Interna användare

I avsnittet Interna användare kan du konfigurera inloggningsalternativ specifikt för interna användare. Interna användare kan komma åt kontot med antingen Adobe ID eller SSO.

**Adobe ID:**

* Interna användare kan logga in med sina inloggningsuppgifter för Adobe ID.
* Passar organisationer som redan använder Adobe-tjänster.

**Enkel inloggning (SSO):**

* Gör att interna användare kan använda organisationens identitetsleverantör (IdP) med enkel inloggning.
* Stöder SAML 2.0-baserad autentisering för sömlös inloggning.

Om du vill tillåta SSO-inloggning för interna användare väljer du Aktivera flera SSO för inloggning och börjar konfigurera SSO.

**[!UICONTROL SSO Active Field]** i Adobe Learning Manager används för att mappa SSO-konfigurationer (Single Sign-On) till specifika användarattribut eller användargrupper. Du kan konfigurera det här fältet för att aktivera flera SSO-konfigurationer för interna användare baserat på deras organisation, plats eller andra kriterier.

### Externa användare

I avsnittet Externa användare i Adobe Learning Manager kan du hantera externa elever, till exempel partner eller byråer, som behöver begränsad åtkomst till Adobe Learning Manager-kontot. Detta avsnitt innehåller verktyg för att skapa registreringsprofiler, hantera externa användargrupper och konfigurera inställningar som är specifika för externa elever.

Externa användare kan logga in på följande sätt:

* Adobe ID: Externa användare kan logga in med sina inloggningsuppgifter för Adobe ID.
* Enkel inloggning (SSO): Externa användare kan logga in via SSO om de har konfigurerats av administratören.
* Adobe Learning Manager ID: Externa användare kan skapa ett användarnamn och lösenord för Learning Manager för att komma åt plattformen.

**Viktiga punkter:**

* Du kan aktivera en eller flera inloggningsmetoder för externa användare.
* Om du väljer Adobe Learning Manager ID måste externa användare skapa sina egna inloggningsuppgifter.
* SSO kan konfigureras för externa användare utifrån organisationens behov.

### SSO-konfiguration i Adobe Learning Manager

Adobe Learning Manager stöder enkel inloggning (SSO) så att användarna kan autentisera en gång och få åtkomst till flera program. Administratörer kan konfigurera enkel inloggning för både interna och externa användare med SAML 2.0-baserade leverantörer.

Mer information finns i [SSO-inloggning i Adobe Learning Manager](/help/migrated/administrators/feature-summary/multiple-sso-logins.md).

>[!NOTE]
>
>* Upp till 20 SSO-konfigurationer kan läggas till på ett konto.
>* Kontakta Adobe-supporten och be om hjälp med SAML 2.0-baserade SSO-leverantörer.

## Datakällor

Med datakällor kan du eller integreringsadministratörer integrera externa system för import och synkronisering av användar- och utbildningsdata. Den här funktionen säkerställer sömlös datahantering och synkronisering med system som HRMS, Salesforce, FTP och andra.

**Exempel på datakälltyper**

* **FTP-anslutningar**: Med FTP-baserade datakällor kan organisationer överföra användardatafiler direkt till Adobe Learning Manager via säkra filöverföringsprotokoll. Dessa anslutningar är särskilt användbara för satsimport av användarinformation, kursregistreringar och andra massdataåtgärder.
* **Tredjepartsintegreringar**: Adobe Learning Manager stöder integrering med olika företagssystem via färdiga anslutningar. Dessa integreringar kan omfatta HR-hanteringssystem, plattformar för kundrelationshantering och andra system för hantering av inlärning.
*** Salesforce-integrering**: Salesforce-kopplingen aktiverar direkt synkronisering av användardata, kursinformation och utbildningsposter mellan Salesforce och Adobe Learning Manager.

Mer information finns i [Anslutningar i Adobe Learning Manager](/help/migrated/integration-admin/feature-summary/connectors.md).

## Kollegiala konton

Med kollegiala konton i Adobe Learning Manager kan du dela köpta platser och visa rapporter över associerade konton. Den här funktionen är användbar för organisationer som behöver samarbeta eller dela resurser mellan olika konton.

Mer information finns i [Kollegiala konton](/help/migrated/administrators/feature-summary/peer-account.md) i Adobe Learning Manager.





