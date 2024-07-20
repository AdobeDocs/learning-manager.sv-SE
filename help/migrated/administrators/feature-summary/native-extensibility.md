---
title: Inbyggd utbyggbarhet
description: Skapa anpassade upplevelser i den inbyggda versionen av Adobe Learning Manager, så att du inte kan använda headless för enklare fall.
exl-id: 510bd00f-4f52-4705-817e-4ee73380ca90
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 2%

---

# Inbyggd utbyggbarhet

Du kan konfigurera anpassade upplevelser i den systemspecifika versionen av Adobe Learning Manager, så att du inte kan använda headless för enklare fall. Du kan också skapa anpassade program och placera dem på olika platser i den ursprungliga versionen av arbetsflödena för elev, chef, administratör, författare eller instruktör.

Adobe Learning Manager stöder 15 anropspunkter mellan administratör, författare, elev, chef och instruktörsapp.

## Skapa ett tillägg

1. Du som är administratör väljer **[!UICONTROL Native Extensions]** i den vänstra panelen.
1. Välj Lägg till ett tillägg.
1. Skriv namnet på tillägget i fältet **[!UICONTROL Name]**.
1. Skriv beskrivningen av tillägget i fältet **[!UICONTROL Description]**.
1. Välj en startpunkt. En startpunkt är en plats i Adobe Learning Manager där det går att infoga en länk eller knapp i ett anpassat program. Följande startpunkter är tillgängliga:

   I det här exemplet väljer du **[!UICONTROL Admin]**, **[!UICONTROL Author: Course]**, **[!UICONTROL Learning Path]** - **[!UICONTROL Instances]** - **[!UICONTROL Instance row]**.

   ![Tilläggsbild](assets/list-native-extensions.png)
   *Välj startpunkt*

1. Ange tilläggsetiketten som ska visas i användargränssnittet i fältet **[!UICONTROL Extension Label]**.
1. Ange URL-adressen där du vill ha tillägget i fältet **[!UICONTROL URL]**.
1. På rullgardinsmenyn Öppna i väljer du om du vill starta tillägget i en modal eller i en ny flik.
1. Välj storleken på det modala fönstret. Alternativen är tillgängliga om du har valt *Modalt i appen* i föregående steg.

   För att bibehålla tillgängligheten i popup-fönstret måste tilläggsprogrammet skickas till händelsen när de har det sista fokuserbara elementet på sin webbplats och sedan väljer användaren TAB-tangenten. Det här behövs för att behålla fokus i popup-fönstret för att stödja tillgänglighet.

   ```
   window.parent.postMessage({*}
   
   { type: 'ALM_EXTENSION_APP', eventType: 'trapFocusInModal' }
   
   ,{}'');
   ```

1. Ange tilläggets omfattning. Följande omfång är tillgängliga:

   * **[!UICONTROL All Courses, Learning Paths and Certifications]**: Det här tillägget är aktiverat för alla kurser, utbildningsvägar och certifieringar. Tillsammans med administratörer kan författare inaktivera den för vissa kurser, utbildningsvägar och certifieringar.
   * **[!UICONTROL Selected Courses, Learning Paths and Certifications]**: Det här tillägget är inaktiverat för alla kurser, utbildningsvägar och certifieringar. Tillsammans med administratörer kan författare aktivera det för vissa kurser, utbildningsvägar och certifieringar.

1. Välj växlingsknappen **[!UICONTROL Activate]** för att aktivera tillägget. När tillägget har aktiverats visas det på den angivna anropspunkten enligt omfånget.
1. Välj **[!UICONTROL Save]** i det övre högra hörnet på sidan för att skapa tillägget.

## Öppna tillägget som administratör

1. Välj **[!UICONTROL Learning Paths]** i det vänstra verktygsfältet som administratör.
1. Välj en kurs > **[!UICONTROL View Learning Path]**.
1. Välj **[!UICONTROL Instances]** i den vänstra panelen.
1. Välj **[!UICONTROL More]** i avsnittet Instanser. Tillägget visas i avsnittet Instanser.

   ![instansbild](assets/instances-extension.png)
   *Välj tillägget*

   När du väljer filnamnstillägget visas det i det modala fönstret.

## Öppna tillägget som författare

1. Välj **[!UICONTROL Learning Paths]** i det vänstra verktygsfältet som administratör.
1. Välj en kurs > **[!UICONTROL View Learning Path]**.
1. Välj **[!UICONTROL Instances]** i den vänstra panelen.
1. Välj **[!UICONTROL More]** i avsnittet Instanser. Tillägget visas i avsnittet Instanser.

   ![instansbild](assets/instances-extension.png)
   *Få åtkomst till tillägget som författare*

   När du väljer filnamnstillägget visas det i det modala fönstret.

## Visa alla tillägg

Som administratör kan du visa alla tillägg på sidan Systemspecifika tillägg. Du kan se listan genom att välja Inbyggda tillägg i programmets vänstra panel.

![visa tilläggsbild](assets/view-extensions.png)
*Visa alla tillägg*

## Aktivera eller inaktivera ett tillägg

Du som är författare kan aktivera eller inaktivera ett tillägg för en kurs, certifiering eller utbildningsväg på sidan Inställningar för en kurs.

![Aktivera tilläggsbild](assets/activate-extension.png)
*Aktivera ett tillägg*

## Dela en åtkomstnyckel

Du måste dela åtkomstnyckeln om du konfigurerar ett registreringstillägg.

Detta är viktigt eftersom om nyckeln inte genereras och delas kommer autentiseringen för registreringen att misslyckas och eleverna kan inte registrera sig för kurserna.

Åtkomstnyckeln måste delas för registrering i kurs eller utbildningsväg och certifikat.

Generera nyckeln på fliken Inställningar.

![Dela nyckelbild](assets/share-extension.png)
*Dela åtkomstnyckeln*

## Hämta tilläggsrapport

Du kan hämta den här rapporten på två sätt.

**Konfigurationsrapport för tillägg**

1. Välj **[!UICONTROL Extension Configuration Report]** på sidan Inbyggda tillägg.

   ![rapportbild](assets/extension-config-report.png)
   *Hämta tilläggsrapport*

   Rapporten genereras.

1. Välj OK.

   ![Genererar rapportbild](assets/generating-report.png)
   *Genererar rapporten*

   Rapporten innehåller följande fält:

   * Namn på förlängning
   * Poäng för tillämpning
   * Etikett
   * Öppna i URL
   * Omfång
   * Aktivera
   * LO unikt ID
   * Utbildnings-ID
   * Utbildningstyp
   * Utbildningsnamn

**Sidan Rapporter**

1. I **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]** väljer du **[!UICONTROL Extension Configuration Report]**.

   ![bild av sidan Rapporter](assets/extension-report-page.png)
   *Hämta rapporten från sidan Rapporter*

Tillståndet måste vara i intervallet **0-4294967295** när registreringstillståndet konfigureras.
