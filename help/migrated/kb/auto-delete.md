---
jcr-language: en_us
title: Användaren tas bort automatiskt i Learning Manager
description: En användare raderas från Learning Manager, men administratören har aldrig utfört någon sådan åtgärd.
contentowner: nluke
source-git-commit: 66dfaaaf723382eada39e2be29dfd49b795107a0
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---



# Användaren tas bort automatiskt i Learning Manager {#user-gets-auto-deleted-in-learning-manager}

## Problem

En användare raderas från Learning Manager, men administratören har aldrig utfört någon sådan åtgärd.

## Orsak

I Adobe Learning Manager finns det ett alternativ som gör att du kan ta bort en användare om han/hon inte har loggat in till systemet under en viss tid.

## Hur ändrar/tillämpar jag inställningen?

### För interna elever

1. Logga in som **Administratör**.
1. Under **Konfigurera** klickar du på **Inställningar** > **Allmänt**.
1. På sidan Allmänna inställningar finns mer information i för alternativet **Ta bort interna användare automatiskt**.
1. Klicka **[!UICONTROL Edit]** för att ange antalet dagar i fältet, för att automatiskt ta bort en elev som inte har kommit åt systemet.

   ![](assets/cp-autodelete-internal.png)

   *Redigera antalet dagar*

>[!NOTE]
>
>   Lämna fältet tomt om du inte vill ta bort användarna automatiskt.


1. Klicka **[!UICONTROL Save]** för att behålla de inställningar du gjort.

### För externa elever:

1. Logga in som **Administratör**.
1. Under **Hantera** klickar du på **[!UICONTROL Users]** > **[!UICONTROL External]**.
1. Klicka på namnet på den externa användare som inställningen ska användas för.

   Då öppnas fönstret **Redigera profil för extern registrering** -fönstret.

1. Klicka **[!UICONTROL Advanced Settings]** längst ned till vänster.

   ![](assets/cp-autodelete-external.png)

   *Välj alternativet Avancerade inställningar*

1. I dialogrutan **Inloggningskrav** anger du antalet dagar som en elev automatiskt ska tas bort om hen inte har åtkomst till systemet.
1. Klicka **[!UICONTROL Save]** för att behålla de inställningar du gjort.
