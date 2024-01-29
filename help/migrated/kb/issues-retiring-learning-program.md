---
jcr-language: en_us
title: Problem med att dra tillbaka ett utbildningsprogram
description: Problem med att dra tillbaka ett utbildningsprogram i Adobe Learning Manager
contentowner: nluke
source-git-commit: 66dfaaaf723382eada39e2be29dfd49b795107a0
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---



# Problem med att dra tillbaka ett utbildningsprogram

## Problem

Ett utbildningsprogram pensioneras automatiskt.

## Orsak

Det finns situationer där ett utbildningsprogram har fasats ut utan att en administratör/författare uttryckligen har fasat ut LP.

Det här problemet uppstår eftersom ett utbildningsprogram är en samling kurser. De högre orderutbildningarna upphör om någon av kurserna i den innehåller en utfasad instans eller kursinstansen upphör.

## Upplösning

Följ stegen nedan för att kontrollera kursen som innehåller en utfasad instans:

1. Logga in som administratör och starta relevant utbildningsprogram.

1. Klicka **[!UICONTROL Instances]** > **Ckurser**. Sidan listar alla kurser som ingår i detta utbildningsprogram. Du kommer att kunna se kursen som innehåller en utfasad instans.

   ![](assets/retired-instance.png)

   *Visa lista över alla kurser*

1. När du har listat ut kursinstansen som har fasats ut klickar du på **[!UICONTROL Courses]** > **[!UICONTROL Open the course]**.

1. Klicka **[!UICONTROL Instances]**. I den utgångna instansen klickar du på **[!UICONTROL Edit]** och redigera sedan slutförandedatumet till ett framtida datum som du vill att instansen ska gå i pension till.

   ![](assets/completion-date.png)

   *Redigera slutförandedatum för en kurs*

1. När du är klar klickar du på listrutan som visas på bilden nedan. Klicka sedan på **[!UICONTROL Reopen Instance]**.

   ![](assets/re-open-instance.png)

   *Öppna kursinstansen igen*

1. Besök relevant utbildningsprogram. Klicka **[!UICONTROL Instances]** och utför föregående steg för att öppna utbildningsprogrammets instans igen.
