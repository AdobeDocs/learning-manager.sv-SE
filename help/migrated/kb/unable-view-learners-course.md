---
jcr-language: en_us
title: Det går inte att visa elever i en kurs
description: På fliken Elever för en kurs visas inte någon elev som är registrerad i Adobe Learning Manager. Men om du genererar en rapport kan du visa de registrerade eleverna i rapporten.
contentowner: saghosh
exl-id: 2ea54347-fa6b-493e-b73c-d350efb2aaaf
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 1%

---

# Det går inte att visa elever i en kurs

## Problem

Du kan inte se elever som är registrerade för en kurs.

## Beskrivning

På fliken Elever för en kurs visas ingen registrerad elev. Men om du genererar en rapport kan du visa de registrerade eleverna i rapporten.

![](assets/no-learners.png)

*Ingen elev visas*

## Orsak

Om en elev är registrerad via ett högre utbildningsobjekt (utbildningsprogram eller certifiering) kommer eleven att vara synlig på fliken Elev på det högre utbildningsobjektet. Eleven är inte sökbar under fliken Elever på kursen.

**Så här visar du vilket objekt för högre utbildning som eleven är registrerad på?**

Du kan kontrollera den här informationen i rapporten Utbildningsbevis. Följ stegen nedan för att generera en elevbetygsutdrag:

1. Logga in som administratör.
1. Klicka på **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]** > **[!UICONTROL Excel Reports]** > **[!UICONTROL Learner Transcript]**.

1. Ange namnet på **[!UICONTROL Learner]** och ange intervallet **[!UICONTROL Date]**.
1. Expandera avsnittet **[!UICONTROL Advanced Options]** och välj alternativet **[!UICONTROL Enable module level information]**.
1. Klicka på **[!UICONTROL Generate]**.

   På elevens betygsutdrag kan du se vilket högre utbildningsobjekt eleven är registrerad via.
