---
jcr-language: en_us
title: Det går inte att uppnå en kompetens efter att ha slutfört en kurs
description: En elev får inte någon färdighet ens efter att ha slutfört en kurs. De färdigheter som tilldelas den kursen förblir under arbete för eleven.
contentowner: nluke
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---



# Det går inte att uppnå en kompetens efter att ha slutfört en kurs

## Problem

En elev får inte någon färdighet ens efter att ha slutfört en kurs. De kompetenser som tilldelas den kursen förblir som **Pågår** för eleven.

## Orsak

Problemet uppstår om **Poäng som krävs** för att uppnå denna kompetens är större än **Intjänade poäng** av eleven efter att ha slutfört kursen.

## Lösning

Kontrollera aktuell **Kompetenspoäng** och **punkt** information som krävs för att uppnå kompetensen. Följ stegen nedan:

1. Generera en **Elevens betygsutdrag** rapport.
1. När du genererar elevutdraget klickar du på **[!UICONTROL Advanced Options]** och markera alternativet **[!UICONTROL Include Skills data and summary sheets]**.

   ![](assets/advanced-options.png)

   *Välj alternativet Inkludera kompetensdata och sammanfattningar*

1. Öppna den hämtade elevens betygsrapport.
1. Gå till **[!UICONTROL Skills transcript]** blad. Här visas **[!UICONTROL Credits Required]** och **[!UICONTROL Credits Earned]** av eleven.

   I exemplet nedan krävs till exempel 50 poäng för att uppnå kompetensen för en kurs. Men, eleven har uppnått endast en kredit.

   ![](assets/skill-transcript.png)

   *Visa obligatoriska krediter*

1. Om du vill kontrollera tillskrivningar för en viss kompetens loggar du in som administratör och går till **Kompetenser** -fliken, enligt nedan:

   ![](assets/skill.png)

   *Starta fliken Kompetenser*

1. Logga in som författare och öppna kursen om du vill kontrollera antalet poäng som har tilldelats en kurs. Klicka **[!UICONTROL Settings]** > **Kurskompetenser** som visas nedan:

   ![](assets/course-skills.png)

   *Visa kurskompetenser*
