---
jcr-language: en_us
title: Okta Active Directory-integrering med Adobe Learning Manager
description: Okta Active Directory-integrering med Adobe Learning Manager
contentowner: nluke
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---



# Okta Active Directory-integrering med Adobe Learning Manager {#okta-active-directory-integration-with-adobe-learning-manager}

I det här dokumentet får du lära dig hur du integrerar Adobe Learning Manager med Okta Active Directory (AD). När du integrerar Adobe Learning Manager med Okta AD kan du:

* Kontrollera och kontrollera åtkomst till Learning Manager i Okta AD.
* Gör det möjligt för användare att automatiskt logga in på Adobe Learning Manager med sina Okta AD-konton.
* Hantera dina konton på en central plats - Okta-portalen.

Adobe Learning Manager stöder identitetsleverantörs- (IdP) och tjänsteleverantörsinitierad enkel inloggning.

## Skapa ett program i OKTA

1. Logga in som administratör på Okta AD.
1. Klicka på **[!UICONTROL Applications]**. Då öppnas Application Store i Okta.

   ![](assets/cp-application-store.png)

   *Visa appbutik i Okta*

1. Klicka på **[!UICONTROL Create App Integration]**.

   ![](assets/cp-app-integrations.png)

   *Välj Skapa programintegrering*

1. Välj **[!UICONTROL SAML 2.0]** från det nya programintegreringsfönstret.

   ![](assets/cp-saml2.0.png)

   *Välj alternativet SAML2.0*

1. Välj **[!UICONTROL Create SAML integration]** > **[!UICONTROL General settings page]**. Ange ett programnamn.

   Observera att detta kan vara vilket namn som helst för att unikt identifiera ditt program. När du är klar klickar du på **[!UICONTROL Next]**.

   ![](assets/cp-saml-integration.png)

   *Ange programmets namn*

1. Utför följande steg på sidan Konfigurera SAML-inställningar:

   **För IdP-konfiguration:**

   1. I fältet URL för enkel inloggning skriver du URL:en: [https://learningmanager.adobe.com/saml/SSO](https://learningmanager.adobe.com/saml/SSO)
   1. Skriv URL:en i fältet Audience URL: [https://learningmanager.adobe.com](https://learningmanager.adobe.com/)
   1. I dialogrutan **Namn-ID-format** rullgardinsmenyn väljer du **E-postadress**.
   1. I dialogrutan **Användarnamn för program** väljer du Okta-användarnamn.
   1. Om du vill skicka ytterligare attribut kan du lägga till attributen under **Attributsatser** (Valfritt)

   ![](assets/cp-saml-integration-step1.png)

   *Lägg till SAML-attribut*

   **För SP-konfiguration:**

   1. I fältet URL för enkel inloggning skriver du URL:en: [https://learningmanager.adobe.com/saml/SSO](https://learningmanager.adobe.com/saml/SSO)
   1. Skriv URL:en i fältet Audience URL: [https://learningmanager.adobe.com](https://learningmanager.adobe.com/)
   1. I listrutan Namn-ID-format väljer du **E-postadress**.
   1. I listrutan Program, användarnamn, väljer du Okta-användarnamn.
   1. Klicka på **Visa avancerade inställningar**.
   1. Under **Signaturalgoritm**, välj RSA-SHA256
   1. I dialogrutan **Assertion Algorithm**, välj SHA256
   1. I dialogrutan **Assertion Encryption** listruta, markera **Krypterad**.

   1. I dialogrutan **Krypteringscertifikat** , överför certifikatfilen som delas av Adobe.
   1. Om du vill skicka ytterligare attribut kan du lägga till attributen under **Attributsatser** (Valfritt).

   ![](assets/cp-saml-integration-step2.png)

   *Lägg till ytterligare attribut*

   När du är klar klickar du på **[!UICONTROL Next]**.

1. Inställningen **Feedback**  -fliken är valfri. När du har valt alternativen och gett din feedback, klickar du på **[!UICONTROL Finish]**.

   ![](assets/cp-saml-integration-step3.png)

   *Slutför SAML-konfigurationen*

## Extrahera URL som initierats av IdP och metadatafil

Gör som följer för att visa den URL och metadatafil som initierats av IdP/SP:

1. Öppna det program du har skapat.
1. Enligt **Enkel inloggning (SSO)** flik klickar du på **[!UICONTROL View Instructions]**.

   ![](assets/cp-prime-sso.png)

   *Välj fliken SSO*

   **För IdP:**

   1. Identitetsleverantörens URL för enkel inloggning är den IdP-initierade URL:en.
   1. Kopiera all text som finns under **Valfritt** område.
   1. Öppna ett nytt anteckningsblock och klistra in den kopierade texten.
   1. Klicka **[!UICONTROL File]** > **[!UICONTROL Save as]** > &quot;filnamn.xml&quot;. Detta blir metadatafilen.

   **För SP:**

   1. Identitetsleverantörens URL för enkel inloggning är den IdP-initierade URL:en.
   1. Identitetsleverantörens utfärdare är enhets-id:t.
   1. Kopiera all text som finns under **Valfritt** område.
   1. Öppna ett nytt anteckningsblock och klistra in den kopierade texten.
   1. Klicka på **[!UICONTROL File]** > **[!UICONTROL Save as]** > **[!UICONTROL filename.xml]**. Detta blir metadatafilen.

   ![](assets/cp-saml-integration-step4.png)

   *Spara SP XML-fil*

   Du måste spara den här filen i ett XML-format.

## Konfigurera SSO för Adobe Learning Manager

Utför stegen som nämns i artikeln nedan för att konfigurera enkel inloggning (SSO) för Adobe Learning Manager.

<!--

article not in TOC

[SSO Authentication](/help/migrated/kb/sso-authentication-for-learning-manager.md)
-->