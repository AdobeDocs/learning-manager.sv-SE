---
jcr-language: en_us
title: Credly
description: Läs mer om att integrera med ALM för att hantera och dela externa utmärkelsetecken från plattformen i olika sociala mediekanaler
contentowner: chandrum
exl-id: 168f7ff8-51f5-4962-bf76-af909fc5565b
source-git-commit: f3a0ec693e1a2e75cdad24f91f22a0290d62740d
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Credly

[Med kredit](https://info.credly.com/) är en digital plattform för inloggningsuppgifter som gör det möjligt för elever och organisationer att tjäna in, dela och verifiera yrkesmässiga prestationer, till exempel utmärkelsetecken eller certifieringar. Elever kan hantera och dela utmärkelsetecken via sin kreditprofil på sociala medier och andra platser.

## Förutsättning

Skapa ett kreditkonto för din organisation. Lägg till elever på Krediter med hjälp av deras e-postadresser i Adobe Learning Manager. Detta gör att eleverna kan se utmärkelsetecknen på Credly och Adobe Learning Manager.

## Lägg till kreditkopplingen i Adobe Learning Manager

Följ de här stegen för att lägga till kreditkopplingen i Adobe Learning Manager:

1. Logga in som **[!UICONTROL Integration Admin]**.
2. Välj **[!UICONTROL Credly]** > **Anslut** för att lägga till **[!UICONTROL Credly]**-anslutningen i Adobe Learning Manager.

   ![](assets/connector-credly.png)
   _Lägg till kreditkoppling_

3. Skriv **[!UICONTROL Connection Name]**.
4. Skriv **[!UICONTROL Organization ID]** och **[!UICONTROL Authorization token]**.

   >[!NOTE]
   >
   >Varje märke i Crely har ett organisations-ID och en auktoriseringstoken. Kopiera de här värdena från Credly.

5. Skriv **[!UICONTROL Hostname]** och välj **[!UICONTROL Connect]**.

## Migrera märken från Crely

Med badge.csv i Adobe Learning Manager kan du migrera märken från det befintliga LMS-systemet eller andra system. Badge.csv har uppdaterats med två nya kolumner:

* externalBadgeId
* externalBadgeProvider

Externt utmärkelsetecken-ID refererar till ID:t för utmärkelsetecknet i plattformen Creded och den externa utfärdaren av utmärkelsetecknet är Credly. Lägg till dessa värden i badge.csv och följ stegen som nämns i [migreringshandboken](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/migration-manual#migrationprocedure) för att migrera CSV-filen.

## Skapa en kompetens - administratör

När märket har importerats till Adobe Learning Manager kan administratören skapa det som en kompetens. Information om hur du skapar en kompetens finns i [Skapa och ändra kompetenser](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/skills-levels).

### Tilldela kompetensen/utmärkelsetecknet till utbildningsobjektet - författare

Författaren/administratören kan tilldela dessa kreditimporterade ALM-märken till en kurs, utbildningsväg eller certifiering (inte bara färdigheter) och om förbrukningen av dessa utbildningsobjekt kommer märket att uppnås och kan visas på Crely och ALM App.

Elever kan logga in på Creredly och se utmärkelsetecknen på Credly-plattformen. Från Credly kan de dela märken på externa plattformar som LinkedIn och andra sociala medier.
