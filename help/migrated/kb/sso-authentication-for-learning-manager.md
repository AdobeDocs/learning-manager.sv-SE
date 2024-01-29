---
description: Detta dokument hjälper dig att konfigurera SSO-autentisering för att logga in på ditt Learning Manager-konto.
jcr-language: en_us
title: Logga in på Learning Manager med SSO-autentisering
contentowner: dvenkate
source-git-commit: a186a600e632e9a564c4ff30d1897c2cdf0d5aac
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---



# Logga in på Learning Manager med SSO-autentisering

Detta dokument hjälper dig att konfigurera SSO-autentisering för att logga in på ditt Learning Manager-konto.

Utför följande steg för att konfigurera SSO-autentisering:

1. Öppna **[!UICONTROL Settings]** > **[!UICONTROL Login Methods.]**

   ![](assets/login-methods.png)

1. Välj **[!UICONTROL Internal Users]** eller **[!UICONTROL External Users]** beroende på dina behov.
1. Klicka på listrutan bredvid  **[!UICONTROL login]** och välj **[!UICONTROL Single Sign-On]**.

   ![](assets/single-sign-on.png)

1. Klicka på för att justera inställningarna för enkel inloggning (SSO)  **[!UICONTROL Change.]**

   ![](assets/change.png)

1. Enter  **[!UICONTROL IDP-initiated Authentication URL]** som du fått av din tjänsteleverantör och ladda upp XML-filen genom att klicka på **[!UICONTROL IDP Metadata XML File.]**

   ![](assets/sso-configuration.png)

   Den SSO som du konfigurerar i Learning Manager bör ha stöd för SAML 2.0.

   Nu kan du logga in på Learning Manager med SSO-autentisering.

