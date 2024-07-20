---
jcr-language: en_us
title: Det går inte att registrera sig som en extern användare
description: Externa elever kan inte registrera sig för en profil i Adobe Learning Manager.
contentowner: nluke
exl-id: b1a9ecb6-75a8-44f7-b169-f77d7a4f6c2c
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
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
1. Klicka på **[!UICONTROL Users]** > **[!UICONTROL External]** under **Hantera**.
1. Öppna profilen som användaren redan ingår i genom att klicka på de platser som används

   ![](assets/cp-seats-used.png)

   *Öppna användarens profil*

1. Välj användaren, klicka på **[!UICONTROL Actions]** > **[!UICONTROL Change Profile]**.

   ![](assets/cp-change-profile.png)

   *Ändra användarens profil*

   Detta öppnar ett fönster där du kan välja en ny profil enligt nedan.

   ![](assets/cp-select-profiles.png)

   *Välj användarprofil*

1. Klicka på **[!UICONTROL Change]** när du har valt.

**Scenario 2:** Användaren finns som en intern elev.

1. Logga in som administratör.
1. Klicka på **[!UICONTROL Users]** > **[!UICONTROL Internal]** under **Hantera**.
1. Klicka för att öppna en elevprofil och klicka på ikonen Redigera.

   ![](assets/cp-internal-learner.png)

   *Öppna en intern elevprofil*

1. Ändra elevens e-postadress eller lägg till *_old* till den befintliga e-postadressen. Detta frigör e-postadressen.

   Om elevens e-postadress till exempel är *<abc@adobe.com>,* ändrar du den till *<abc_old@adobe.com>*

1. Klicka på **Spara** för att behålla ändringarna.

**Scenario 3**: Användaren är i ett borttaget tillstånd.

1. Logga in som administratör.
1. Klicka på **[!UICONTROL Users]** > **[!UICONTROL User Cleanup]** under **Hantera**.
1. Välj eleven och klicka på ikonen Redigera.

   ![](assets/cp-deleted-learner.png)

   *Redigera användarens e-postadress*

1. Ändra elevens e-postadress eller lägg till *_old* till den befintliga e-postadressen. Detta frigör e-postadressen.

   Om elevens e-postadress till exempel är **<abc@adobe.com>** ändrar du den till **<abc_old@adobe.com>**.
