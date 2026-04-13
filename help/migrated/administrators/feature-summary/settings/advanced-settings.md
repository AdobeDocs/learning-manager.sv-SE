---
description: Läs mer om att konfigurera avancerade inställningar i Adobe Learning Manager
jcr-language: en_us
title: Avancerade inställningar i Adobe Learning Manager
source-git-commit: 03123dcd8d9066cdfcb0fe97e61acb3df625a23e
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---


# Avancerade inställningar i Adobe Learning Manager

## Katalogetiketter

Katalogetiketter i Adobe Learning Manager används för att tagga utbildningsobjekt (kurser, certifieringar, utbildningsvägar osv.) med specifika fält och värden. De här etiketterna hjälper dig och författarna att kategorisera och ordna innehåll effektivt, vilket möjliggör bättre filtrering, spårning och rapportering.

Mer information finns i [Katalogetiketter i Adobe Learning Manager](/help/migrated/administrators/feature-summary/catalog-labels.md).


>[!NOTE]
>
>* Obligatoriska etiketter: Du kan välja att göra katalogetiketter obligatoriska för författare när kursen skapas.
>* Författararbetsflöde: Författare måste lägga till kompatibilitetsetiketter när de skapar eller redigerar kurser för att säkerställa korrekt kategorisering.

## Innehållsmapp

Med innehållsmappar kan du ordna och hantera innehåll genom att skapa privata eller gemensamma mappar. Den här funktionen ser till att innehållet bara är tillgängligt för vissa författare eller grupper, vilket ger bättre kontroll över synlighet och hantering av innehållet.

**Viktiga punkter:**

En mapp är en innehållsdatabas, som är en delmängd av hela innehållsbiblioteket som är tillgängligt på ett konto med följande egenskaper:

* Det är bara du (administratör) som kan skapa, redigera eller ta bort en mapp.
* Du kan bara styra åtkomst till mappar som en del av definitionen av roller för anpassade administratörer.
* Innehållet måste alltid vara kopplat till minst en mapp. Till att börja med kommer allt innehåll att kopplas till den gemensamma mappen, som senare kan ändras.
* Innehållet kan kopplas till flera mappar när det skapas, vilket också blir möjligt genom en kopiering
* Alla mappnamn måste vara unika i kontot, annars uppstår ett fel när en mapp namnges.

Mappar styr bara synligheten för innehållet och skapar inte kopior av innehållet. Därför visas redigering av innehåll i alla associerade mappar.

**Gemensam mapp**

En gemensam mapp finns alltid på ett konto och till att börja med kommer allt innehåll att vara en del av denna mapp. Senare kan författare flytta innehåll från den här mappen till andra mappar. En gemensam mapp har följande egenskaper:

* Allt innehåll kopplat till den här mappen är som standard tillgängligt för alla typer av författare.
* Innehåll som är en del av en gemensam mapp kan inte ingå i någon annan mapp. Det motsatta gäller också.

Den här mappen kan inte ingå i en konfigurerbar rolldefinition. Att inte ha en gemensam mapp i en konfigurerbar rolldefinition begränsar därför inte åtkomsten till en gemensam mapp.

**Privat mapp**

Alla mappar som du skapar är privata.

**Lägg till en innehållsmapp**

Så här lägger du till en innehållsmapp:

1. Välj **[!UICONTROL Settings]** > **[!UICONTROL Content Folder]**.
2. Välj **[!UICONTROL Add]** för att skapa en ny mapp.
3. Ange namnet på och beskrivningen av den mapp som ska skapas.

   ![Alt-text](assets/advanced-settings-picture1.png)

4. Välj **[!UICONTROL Save]** för att skapa mappen.

**Mappåtgärder**

* **[!UICONTROL Add a folder]**: Om du vill lägga till en mapp markerar du mappen och väljer sedan **[!UICONTROL Add]** i skärmens övre högra hörn.
* **[!UICONTROL Delete a folder]**: Om du vill ta bort en mapp markerar du mappen som ska tas bort, väljer menyn **[!UICONTROL Actions]** och väljer sedan **[!UICONTROL Delete Folder]**.

## Klassrumsplatser

Skapa och hantera ett bibliotek med fysiska eller virtuella klassrumsplatser. Dessa platser kan användas av författare och administratörer för att konfigurera lärarledda utbildningshändelser. Funktionen gör att klassrumsinformation, till exempel platsbegränsningar och platsinformation, är förkonfigurerad och lätt att komma åt.

Mer information finns i [Lägga till klassrumsplatser i Adobe Learning Manager](/help/migrated/administrators/feature-summary/classroom.md).

## Rapporter

I det här avsnittet kan du konfigurera kontrollpanelerna Efterlevnad och Gruppframgång.

![Alt-text](assets/advanced-settings-picture2.png)

Mer information finns här:

* [Efterlevnadstavla](/help/migrated/administrators/feature-summary/reports.md#compliance-dashboard)
* [Tavla för slutförda grupper](/help/migrated/administrators/feature-summary/group-success-dashboard.md)


