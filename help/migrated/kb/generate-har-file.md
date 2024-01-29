---
description: Läs vidare för att veta hur man skapar HAR-filer på Google Chrome.
jcr-language: en_us
title: Generera en HAR-fil
contentowner: dvenkate
source-git-commit: ec79aa3dd6225cc424721afb50702963c1b125eb
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---



# Generera en HAR-fil

Läs vidare för att veta hur man skapar HAR-filer på Google Chrome.

Så här skapar du en HAR-fil:

1. Öppna ett Google Chrome-fönster och öppna en ny flik.
1. Öppna utvecklarverktyg på sidan, högerklicka > Inspect.
1. Öppna fönstret **[!UICONTROL Network]** -fliken. Kontrollera att den röda postknappen är aktiv. Aktivera **[!UICONTROL Preserve Log]** -kryssrutan.

   ![](assets/preserve-log-checkbox.png)

   *Markera kryssrutan Bevara logg på fliken Nätverk*

1. Logga in på [Learning Manager](https://learningmanager.adobe.com/acapindex.html) använda dina inloggningsuppgifter och gå kursen. Gör alla åtgärder som leder till problemet.
1. Högerklicka och välj i utvecklarverktyg **Spara allt som fast med innehåll**.

   I vissa versioner av Google Chrome kan du behöva välja **[!UICONTROL Copy]** > **[!UICONTROL Copy all as HAR]**.

   ![](assets/copy-hra.png)

   *Kopiera alla maskinvarufiler*

1. Klistra in det kopierade innehållet i en anteckningsfil. Spara den på skrivbordet som **logs.har** och skicka det via e-post till Adobe.
