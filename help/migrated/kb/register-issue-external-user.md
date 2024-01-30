---
jcr-language: en_us
title: Det går inte att registrera sig som en extern användare
description: Externa elever kan inte registrera sig för en profil i Adobe Learning Manager.
contentowner: nluke
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 3%

---



# Det går inte att registrera sig som en extern användare

## Problem

Externa elever kan inte registrera sig till en profil.

## Fel

Mejl-ID är redan registrerat. Använd en annan mejladress.

![](assets/cp-register-profile.png)

*Felmeddelande för ett redan registrerat e-postmeddelande*

## Beskrivning

Det finns scenarier där en användare inte kan registrera sig till en extern profil. Användaren får ovanstående fel när han/hon registrerar sig.

## Orsak

Det här problemet uppstår i ett av följande scenarier:

* Användaren är redan registrerad i en annan extern profil.
* Användaren är redan en intern elev.
* Användaren är i ett borttaget tillstånd.

## Upplösning:

**Scenario 1:** Användaren är redan registrerad i en annan extern profil.

1. Logga in som administratör.
1. Under **Hantera** klickar du på **[!UICONTROL Users]** > **[!UICONTROL External]**.
1. Öppna profilen som användaren redan ingår i genom att klicka på de platser som används

   ![](assets/cp-seats-used.png)

   *Öppna användarens profil*

1. Välj användaren och klicka på **[!UICONTROL Actions]** > **[!UICONTROL Change Profile]**.

   ![](assets/cp-change-profile.png)

   *Ändra användarprofil*

   Detta öppnar ett fönster där du kan välja en ny profil enligt nedan.

   ![](assets/cp-select-profiles.png)

   *Välj användarprofil*

1. När du har valt klickar du på **[!UICONTROL Change]**.

**Scenario 2:** Användaren finns som en intern elev.

1. Logga in som administratör.
1. Under **Hantera** klickar du på **[!UICONTROL Users]** > **[!UICONTROL Internal]**.
1. Klicka för att öppna en elevprofil och klicka på ikonen Redigera.

   ![](assets/cp-internal-learner.png)

   *Öppna en intern elevprofil*

1. Ändra elevens e-postadress eller lägg till *_old* till befintlig e-postadress. Detta frigör e-postadressen.

   Exempel: Om elevens e-postadress är *<abc@adobe.com>,* ändra den till *<abc_old@adobe.com>*

1. Klicka **Spara** för att behålla ändringarna.

**Scenario 3**: Användaren är i ett borttaget tillstånd.

1. Logga in som administratör.
1. Under **Hantera** klickar du på **[!UICONTROL Users]** > **[!UICONTROL User Cleanup]**.
1. Välj eleven och klicka på ikonen Redigera.

   ![](assets/cp-deleted-learner.png)

   *Redigera användarens e-postadress*

1. Ändra elevens e-postadress eller lägg till *_old* till befintlig e-postadress. Detta frigör e-postadressen.

   Exempel: Om elevens e-postadress är **<abc@adobe.com>**, ändra den till **<abc_old@adobe.com>**.
