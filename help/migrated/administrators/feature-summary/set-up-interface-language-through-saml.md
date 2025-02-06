---
description: Lär dig konfigurera gränssnittsspråket med SAML
jcr-language: en_us
title: Konfigurera gränssnittsspråk via SAML
contentowner: chandrum
source-git-commit: 448119eda15c8d7dfe10150c09fbbe7c530f35e8
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---


# Konfigurera gränssnittsspråk via SAML

Adobe Learning Manager (ALM) accepterar nu ett SAML-attribut för språk. Attributet mappas sedan till användarens gränssnitts- och innehållsinställningar, vilket ger en smidig interaktion med LMS på önskat språk. Konfigurationen av språkinställningarna hanteras via plattformen Identity and Access Management (IAM) med hjälp av SAML för enkel inloggning (SSO). Detta stöder inloggning både från tjänsteleverantören (SP) och från identitetsleverantören (IdP) så att användarna kan se gränssnittet och innehållet på sitt valda språk. Arbetsflödet är följande:

1. Skapa program i Okta
2. Lägg till en användare i Okta
3. Konfigurera SSO i ALM

## Skapa program i Okta

Följ de här stegen om du vill skapa ett program i Okta:

1. Skapa ett utvecklarkonto i Okta med företagets e-postadress och logga in på ditt konto.
2. Välj **[!UICONTROL Applications]** > **[!UICONTROL Create App Integration]**.
3. Välj **[!UICONTROL SAML 2.0]** och sedan **[!UICONTROL Next]**.
4. Ange ett namn för programmet och välj Nästa.
5. Konfigurera följande fält:

   * **[!UICONTROL Single Sign-On URL]**: Ange den specifika domän-URL som du vill länka programmet till (till exempel [https://learningmanagerstage.adobe.com/saml/SSO](https://learningmanagerstage.adobe.com/saml/SSO)). Ändra miljö-URL:en om det behövs.
   * **[!UICONTROL Audience URI (SP Entity ID)]**: Använd samma miljö-URL som ovan.
   * **[!UICONTROL Name ID Format]**: Välj e-postadress.
   * **[!UICONTROL Application Username]**: Välj Okta-användarnamn.

6. Lägg till följande (eller ytterligare fält efter behov) under Attributsatser:
   * **Namn**: språkområde
   * **Namnformat**: Odefinierat
   * **Värde**: user.locale

7. Välj Nästa och välj sedan Slutför.
8. När du är klar bläddrar du ned till SAML-signeringscertifikat:

   * Sök efter raden där statusen är **[!UICONTROL Active]**.
   * Välj **[!UICONTROL Actions]** > **[!UICONTROL View IdP Metadata]**.
   * Detta öppnar en XML-fil i en ny flik. Kopiera XML-koden och spara den lokalt som en .xml-fil.

## Lägg till en användare i Okta

Gör så här om du vill skapa en användare i Okta:

1. Välj **[!UICONTROL Directory]** > **[!UICONTROL People]** och välj sedan **[!UICONTROL Add Person]**.
2. Ange nödvändig information för användaren och välj **[!UICONTROL Save]**.
3. Sök efter och välj den nya användarens användarnamn.
4. Välj **[!UICONTROL Assign Application]**.
5. Välj programmet du skapade tidigare och välj sedan **[!UICONTROL Save]**.
6. Gå till användarens profil och välj **[!UICONTROL Edit]**.
7. I fältet locale skriver du det obligatoriska värdet (till exempel fr_FR, en_US) och väljer **[!UICONTROL Save]**.

## Konfigurera SSO i ALM

Så här konfigurerar du enkel inloggning i ALM:

1. Logga in som administratör.
2. Välj **[!UICONTROL Settings]** > **[!UICONTROL Login Methods]**.
3. Gå till fliken **[!UICONTROL Single Sign-On (SSO) Configuration]**.
4. Välj **[!UICONTROL Add new SSO configuration]**.

   ![](assets/sso-add.PNG)
   _Lägg till SSO i ALM_

5. Konfigurera följande information och välj Spara.
   * Ange ett namn på konfigurationen.
   * Välj **[!UICONTROL IDP Initiated]** i listrutan **[!UICONTROL Single Sign-On (SSO) Settings]**.
   * För **[!UICONTROL IDP-Initiated Authentication URL]**:

      * Öppna XML-metadatafilen som du hämtade tidigare.
      * Sök efter platsvärdet och kopiera det.
      * Klistra in det här värdet i fältet URL för IdP-initierad autentisering.

   * För **[!UICONTROL Metadata XML File]**: Överför XML-filen som du hämtade tidigare.

6. Gå tillbaka till fliken **[!UICONTROL Setup]**.
7. I listrutan väljer du **[!UICONTROL Single Sign-On Configuration]**.
8. Välj konfigurationsnamnet du skapade tidigare i listrutan **[!UICONTROL SSO Setup]**.
9. Välj **[!UICONTROL Save]**.

## Inställning för användarinloggning och språk

När en användare loggar in med autentiseringsuppgifterna via SSO mappas språkattributet som skickas från IdP till användarens gränssnitts- och innehållsspråkfält i ALM. Språkinställningarna visas direkt i användargränssnittet och innehållet utan någon cachelagringstid.

Användarna kan manuellt uppdatera sina språkinställningar i avsnittet för användarprofiler. Dessa manuellt uppdaterade språkinställningar fortsätter att gälla och åsidosätts inte av IdP-inställningarna under framtida inloggningar.

Om en användare tas bort från ALM utan vidare, behålls språkinställningarna i databasen. När samma användare läggs till igen återställs det tidigare angivna språket.

Administratörer kan kontrollera rapporter på användaraktivitet, utbildningssammanfattning och efterlevnadstavla för språkspecifik information.


