---
jcr-language: en_us
title: Markeringsknappar visas inte i Learning Manager
description: På grund av saknade alternativknappar kan en administratör inte tilldela eller ta bort roller, skicka ett välkomstmeddelande eller ta bort en användare.
contentowner: nluke
exl-id: d2c86f9f-3e79-4f1f-992e-f92873940061
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# Markeringsknappar visas inte i Learning Manager

## Problem

På grund av saknade alternativknappar kan en administratör inte utföra följande (listan är inte fullständig):

* Tilldela eller ta bort roller.
* Skicka ett välkomstmeddelande.
* Ta bort en användare.

## Orsak

Problemet uppstår på grund av felaktiga teman i kontot.

![](assets/radio-buttons.png)

*Alternativknappar syns inte*

## Upplösning

Läs in temana igen och åtgärda alternativknapparnas utseende. Gör följande:

1. Klicka på **[!UICONTROL Branding]** som administratör.
1. Klicka på **[!UICONTROL Edit]i avsnittet** Teman **.**
1. Välj ett tema och spara ändringarna.

   ![](assets/set-themes.png)

   *Välj ett tema*

1. Återgå till föregående tema och spara ändringarna.
1. Logga ut från Adobe Learning Manager och logga in igen.
