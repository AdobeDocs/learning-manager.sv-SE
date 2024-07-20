---
jcr-language: en_us
title: Användaren tas bort automatiskt i Learning Manager
description: En användare raderas från Learning Manager, men administratören har aldrig utfört någon sådan åtgärd.
contentowner: nluke
exl-id: 9e293da3-bcbf-4798-b391-aef53ef8d946
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Användaren tas bort automatiskt i Learning Manager {#user-gets-auto-deleted-in-learning-manager}

## Problem

En användare raderas från Learning Manager, men administratören har aldrig utfört någon sådan åtgärd.

## Orsak

I Adobe Learning Manager finns det ett alternativ som gör att du kan ta bort en användare om han eller hon inte har loggat in till systemet under en viss tid.

## Hur ändrar/tillämpar jag inställningen?

### För interna elever

1. Logga in som **administratör**.
1. Klicka på **Inställningar** > **Allmänt** under **Konfigurera**.
1. På sidan Allmänna inställningar finns mer information om alternativet **Ta bort interna användare automatiskt**.
1. Klicka på **[!UICONTROL Edit]** för att ange antalet dagar i fältet, för att automatiskt ta bort en elev som inte har öppnat systemet.

   ![](assets/cp-autodelete-internal.png)

   *Redigera antalet dagar*

>[!NOTE]
>
>   Lämna fältet tomt om du inte vill ta bort användarna automatiskt.


1. Klicka på **[!UICONTROL Save]** om du vill behålla inställningarna.

### För externa elever:

1. Logga in som **administratör**.
1. Klicka på **[!UICONTROL Users]** > **[!UICONTROL External]** under **Hantera**.
1. Klicka på namnet på den externa användare som inställningen ska användas för.

   Då öppnas fönstret **Redigera extern registreringsprofil**.

1. Klicka på **[!UICONTROL Advanced Settings]** i det nedre vänstra hörnet.

   ![](assets/cp-autodelete-external.png)

   *Välj alternativet Avancerade inställningar*

1. I fältet **Inloggningskrav** anger du antalet dagar som en elev ska tas bort automatiskt om hen inte har åtkomst till systemet.
1. Klicka på **[!UICONTROL Save]** om du vill behålla inställningarna.
