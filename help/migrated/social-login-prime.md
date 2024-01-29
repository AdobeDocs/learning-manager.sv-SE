---
jcr-language: en_us
title: Social inloggning i Learning Manager
description: Social inloggning i Learning Manager
contentowner: saghosh
preview: true
source-git-commit: ccdb222228f76fdae63ebb0a808824ad6ac1db7f
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---



# Social inloggning i Learning Manager

Du kan använda dina inloggningsuppgifter för Facebook, LinkedIn eller Twitterna för att logga in på Learning Manager.

## Konfigurera social inloggning {#setupsociallogin}

1. Kontakta din kundansvarige om du vill att han/hon ska konfigurera kontot.

   Följ i annat fall stegen nedan.

1. Sök efter kontot där du vill konfigurera social inloggning.
1. Ändra inloggningen till SSO.
1. Klicka på Avancerat. Ange följande JSON.

   ```
   \{"linkedIn":true,"microsoft":true,"twitter":true,"facebook":true,"editingAllowed":true
   ```

   Om det är en felaktig JSON visas ett undantag.

   Den här sociala inloggningsfunktionen används bara för INTERNA användare.

