---
title: Kommande ändringar i Adobe Learning Manager
description: Läs om de nya funktionerna, förbättringarna och viktiga uppdateringarna som snart kommer till Adobe Learning Manager. Håll dig informerad om vad som ändras så att du kan planera framåt och få ut mesta möjliga av de senaste förbättringarna.
exl-id: 4d2129c4-42d8-446f-8837-879b5c2f42bf
source-git-commit: ffb4883227f1e461df5fc4a025fef1ba1b8568c2
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---

# Kommande ändringar i Adobe Learning Manager

Vi är glada över att kunna dela flera viktiga uppdateringar som kommer till Adobe Learning Manager med de kommande versionerna. Förbättringarna syftar till att effektivisera administrativa arbetsflöden, förbättra datarapporteringens exakthet och stärka rollbaserade kontroller.

Dessa ändringar är utformade för att minska manuell ansträngning, stödja automatisering och förbättra styrningen i alla utbildningsverksamheter.

## Slutföranden som markerats med Capture-instruktör i elevens betygsutdrag

### Målgrupp

Administratörs- och automatiseringsägare

### Översikt

När inkrementella elevtranskriberingar (LT) används i automatiserade arbetsflöden i Adobe Learning Manager hämtas inte instruktörsmarkerade slutföranden som gjorts efter sessionsdatumet. Tidsstämpeln för slutförande återspeglar den ursprungliga sessionens sluttid (inte den tid som instruktören markerade slutförandet). Eftersom dessa uppdateringar inte ingår i den endagsändringsperiod som används för inkrementell LT-generering utesluts därför elevernas närvaro- och slutförandedata från rapporterna, vilket leder till felaktig eller ofullständig nedströmsrapportering och potentiella efterlevnadsluckor.

### Vad har förändrats

Elevens betygsutdrag (LT) omfattar slutföranden som markerats av instruktörer efter sessionsdatumet. Det säkerställer att eventuella markeringar för fördröjd närvaro återspeglas korrekt i transkriptionsexporten.

Närvarotillstånd som &quot;Närvarat och godkänd/ej godkänd&quot; visas automatiskt vid inkrementella LT-exporter.

### Nyheter

* Ny kolumn: Markera slutförandedatum (tidszonen UTC).
* Slutförandekälla är tillgänglig på modulnivå.
* Kompatibel med anslutningsbaserade eller jobb-API-genererade LT-rapporter.

![](assets/capture-instructor.png)

**Åtgärd krävs**

* Om automatiseringen är beroende av kolumnpositioner kontrollerar du logiska konton för den nya kolumnen.
* Om du använder kolumnnamn behövs inga ändringar.
* Eftermonterade färdigställningar (manuella importer) ingår inte.

## Hämtningslänkar i rapporten Arbetsstöd

### Målgrupp

Administratörer, anpassade administratörer och automationsägare

### Översikt

Rapporten om arbetsstöd innehåller en länk för direkt nedladdning av varje arbetsstöd, vilket ger snabb åtkomst till själva rapporten.

### Nyheter

En ny kolumn, **[!UICONTROL Job Aid Link]**, har lagts till i den tredje positionen i rapporten. Den länkar direkt till arbetsstödet om det är en fil eller visar den externa URL som författaren har angett.

Användare med åtkomst (administratör/författare och anpassade roller) kan hämta arbetsstödet med den här länken.

![](assets/download-links-for-job-aid.png)

### Åtgärd som krävs

* Granska automatiserade arbetsflöden med hjälp av arbetsstödsrapporter (med Jobb-API).
* Om skriptet baseras på kolumnplaceringen uppdaterar du skripten.
* Ingen åtgärd krävs om du använder kolumnnamn.

## Kolumner för internt användar-ID och e-post för chef har lagts till i användarrapporten

### Målgrupp

Administratörer (och anpassade administratörer) som använder **[!UICONTROL User Report]** (**[!UICONTROL Admin]** > **[!UICONTROL Users]** > **[!UICONTROL Internal]** > **[!UICONTROL Export User data]**) som hämtats från administratörens användargränssnitt.

### Översikt

För att underlätta arbetsflödena för användaridentifiering och integrering har två kolumner, **[!UICONTROL Internal User ID]** och **[!UICONTROL Manager Email]**, lagts till i användarrapporten som exporteras via användargränssnittet.

### Nyheter

Användarrapporten innehåller ett användares interna användar-ID och chefens e-postadress, för att mappa dem unikt till olika verktyg eller API-slutpunkter.

### Åtgärd som krävs

* Om du använder den här rapporten i automatiserade flöden bör den här nyligen tillagda kolumnen hanteras i automatisering.
* Inga ändringar behövs om arbetsflöden inte påverkas.

## Omfattade behörigheter för meddelanden för anpassade administratörer

### Målgrupp

Anpassade administratörer

### Översikt

Anpassade administratörer kan bara skapa meddelanden för användargrupper eller kataloger inom sitt definierade omfång.

### Nyheter

* Omfångsregler tillåter anpassade administratörer att endast skapa meddelanden för specifika användargrupper eller kataloger.
* När administratörer definierar en anpassad roll kan de tilldela behörigheter för meddelanden med omfattning på användargrupper eller kataloger.
* Anpassade administratörer kan bara skapa meddelanden inom sitt givna omfång.
* Meddelanderapporten för anpassade administratörer visar elever endast inom deras tilldelade omfång.

### Åtgärd som krävs

* Rapportens format förblir oförändrat. Om anpassade administratörer hämtar det från användargränssnittet, kommer rapportens innehåll att omfattas av deras omfattning.
* Inga ändringar krävs om rapporten inte används i något automatiserat eller efterföljande arbetsflöde.

I artikeln [Versionsinformation](https://experienceleague.adobe.com/sv/docs/learning-manager/using/introduction/release-notes) finns en sammanfattande lista med nya funktioner och ändringar av Adobe Learning Manager.
