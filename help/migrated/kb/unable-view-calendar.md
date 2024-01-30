---
jcr-language: en_us
title: Det gick inte att visa kalendern
description: När en administratör försöker redigera förfallodatumet för en extern registreringsprofil och klickar på kalendern för att redigera förfallodatumet, visas inte kalendern.
contentowner: saghosh
source-git-commit: 8b29ac996962e7ce8fbda51f3421c9a5f248fcf6
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---



# Det gick inte att visa kalendern

## Problem

Du kan inte visa kalendern när du redigerar förfallodatumet för en extern profil.

## Beskrivning

När en administratör försöker redigera förfallodatumet för en extern registreringsprofil och klickar på kalendern för att redigera förfallodatumet, visas inte kalendern.

## Orsak

Problemet uppstår på grund av följande:

* Zoomnivån i webbläsaren är över 100 %.
* Skalan och layouten i visningsinställningarna är större än 100 %.

## Upplösning

### Webbläsare

1. Starta webbläsaren.
1. Logga in på Adobe Learning Manager.
1. Klicka på zoomikonen i adressfältet.
1. Klicka på **[!UICONTROL Reset]**.
1. Ändra sista giltighetsdatum för registreringsprofilen.

### Bildskärmsinställningar

1. Klicka på **[!UICONTROL Start]** > **[!UICONTROL Settings]** > **[!UICONTROL System]**.
1. Klicka på **[!UICONTROL Display]**.
1. Enligt **[!UICONTROL Scale and layout]** använder du listrutan. Ändra inställningarna till 100 %.

   ![](assets/scale-layout.png)

   *Ändra visningsinställningar*

1. Starta om datorn.
