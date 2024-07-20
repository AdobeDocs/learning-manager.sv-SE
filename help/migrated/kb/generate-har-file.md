---
description: Läs vidare för att veta hur man skapar HAR-filer på Google Chrome.
jcr-language: en_us
title: Generera en HAR-fil
contentowner: dvenkate
exl-id: 99fe78e8-b5e7-40a7-b9a5-efc2382de993
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# Generera en HAR-fil

Läs vidare för att veta hur man skapar HAR-filer på Google Chrome.

Så här skapar du en HAR-fil:

1. Öppna ett Google Chrome-fönster och öppna en ny flik.
1. Öppna utvecklarverktyg på sidan, högerklicka > Inspect.
1. Öppna fliken **[!UICONTROL Network]**. Kontrollera att den röda postknappen är aktiv. Aktivera kryssrutan **[!UICONTROL Preserve Log]**.

   ![](assets/preserve-log-checkbox.png)

   *Markera kryssrutan Bevara logg på fliken Nätverk*

1. Logga in på [Learning Manager](https://learningmanager.adobe.com/acapindex.html) med dina inloggningsuppgifter och gå kursen. Gör alla åtgärder som leder till problemet.
1. Högerklicka i utvecklarverktygen och välj **Spara allt som HAR med innehåll**.

   I vissa versioner av Google Chrome kan du behöva markera **[!UICONTROL Copy]** > **[!UICONTROL Copy all as HAR]**.

   ![](assets/copy-hra.png)

   *Kopiera alla maskinvarufiler*

1. Klistra in det kopierade innehållet i en anteckningsfil. Spara den på skrivbordet som **logs.har** och skicka den via e-post till Adobe.
