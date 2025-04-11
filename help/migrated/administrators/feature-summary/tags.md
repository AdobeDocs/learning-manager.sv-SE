---
description: Lär dig hantera taggar i Learning Manager.
jcr-language: en_us
title: Taggar
contentowner: dvenkate
exl-id: ea39d2a2-3d2b-43ae-8f8d-b97420b9d008
source-git-commit: a28ac8f57710c118ca4ad02872fd100c6f24beac
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 0%

---

# Taggar

Administratörer kan nu hantera taggar i Learning Manager. Använd bättre taggning och hanterbar databas för att hjälpa elever att söka bättre och få lämpliga sökresultat snabbt. Du kan hantera överflödiga, felstavade och irrelevanta taggar med den här funktionen. Du kan också lägga till, redigera, ta bort, lägga till och ersätta märkord.

Listan med utbildningsobjekt som är associerade med taggen kan visas genom att klicka på antalet bredvid varje tagg. Listan visar antalet kurser, utbildningsprogram, certifikat, arbetsstöd och innehållsgrupper. Klicka på något av dessa alternativ för att visa listan.

Du kan sortera taggarna baserat på användning eller alfabetisk ordning med alternativet **[!UICONTROL Sort By]**.

## Introduktion till taggar

Denna utbildning lär dig lägga till, redigera, ersätta, lägga till och ta bort taggar. Du får också lära dig ändra behörighetsinställningar och använda taggfilter.

[![knapp](assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/8318920)

Skriv till <almacademy@adobe.com> om du inte kan starta utbildningen.

## Lägg till/ta bort/redigera taggar {#adddeleteedittags}

1. Klicka på **[!UICONTROL Tags]** på den vänstra navigeringspanelen som administratör. Sidan **[!UICONTROL Tag Management]** öppnas.
1. Klicka på **[!UICONTROL Add]** om du vill lägga till en ny tagg. Knappen Lägg till finns i det övre högra hörnet på sidan. Om det inte finns några befintliga taggar kommer knappen **[!UICONTROL Add]** också att vara tillgänglig i mitten av sidan **[!UICONTROL Tag Management]**.

   När du lägger till flera taggar avgränsar du dem med (,) eller (;). Ett taggnamn får innehålla högst 50 tecken.

1. Om du vill ta bort en befintlig tagg markerar du taggen genom att klicka i kryssrutan. Du kan markera upp till femtio taggar som ska tas bort samtidigt. Gör så här för att radera:

   * Markera taggarna som ska tas bort > öppna rullgardinsmenyn **[!UICONTROL Action]** > välj **[!UICONTROL Delete]**.

1. Du kan bara redigera en tagg åt gången. Om du vill redigera en tagg gör du så här:

   * Välj taggen för att redigera > öppna **[!UICONTROL Actions]**rullgardinsmenyn > klicka på **[!UICONTROL Edit]**.

   Dialogrutan **[!UICONTROL Edit Tag]** visas. Ange det nya taggnamnet och klicka på **[!UICONTROL Save]**.

   Om det taggnamn du angav redan finns visas ett varningsmeddelande i Adobe Learning Manager. Det får inte finnas två taggar med samma namn.

## Ersätt taggar {#replacetags}

1. Markera märkorden som du vill ersätta. Du kan markera upp till 50 taggar samtidigt. Öppna rullgardinsmenyn **[!UICONTROL Actions]** och välj **[!UICONTROL Replace]**.
1. De markerade taggarna visas i dialogrutan **[!UICONTROL Replace Tags]**.

1. I alternativet **[!UICONTROL Name for replaced tags]** anger du namnet på den nya tagg som du vill ersätta de markerade taggarna med. Du kan antingen ersätta dem med ett befintligt märkord i listrutan eller lägga till ett nytt märkord.

   Semikolon eller kommatecken får inte ingå i taggnamnet.  Observera att taggar utan semikolon och visning av felmeddelanden när du använder sådana taggar som en del av en LO inte hanteras för migreringsscenarier.

1. Klicka på **[!UICONTROL Replace]**.

## Lägg till taggar {#appendtags}

Om åtgärden Lägg till används för taggar läggs den nya/befintliga taggen till i alla listor över LO:er och innehållsgrupper som är kopplade till de markerade taggarna.

1. Markera taggarna som du vill lägga till. Du kan markera upp till 50 taggar samtidigt. Öppna listrutan Åtgärder och välj **[!UICONTROL Append]**.
1. De markerade taggarna visas i dialogrutan **[!UICONTROL Append Tags]**.
1. Du kan lägga till ytterligare en tagg till all utbildning med de markerade taggarna genom att ange namnet på **[!UICONTROL New Tag]** eller i listrutan med de befintliga taggarna. Den nya taggen läggs till i all tillhörande utbildning i Learning Manager.

   Semikolon eller kommatecken får inte ingå i taggnamnet. Om det används visar Prime ett felmeddelande. Observera att taggar utan semikolon och visning av felmeddelanden när du använder sådana taggar som en del av en LO inte hanteras för migreringsscenarier.

1. Klicka på **[!UICONTROL Append]**.

## Inställningar {#settings}

Som administratör kan du ge författaren behörighet att skapa taggar genom att klicka på inställningsalternativet.

![](assets/unknown-1.jpeg)

*Inställningssida för att skapa en tagg*

* När en användare har behörighet att skapa taggar och väljer befintliga taggar som för närvarande är ogiltiga,

  Ett felmeddelande visas som föreslår att den markerade taggen inte längre är giltig. Nya taggar skapas genom att tecken som inte stöds tas bort. I det här fallet bör författaren kunna se sina gamla taggar ändras till nya taggar innan han sparar.

* Om användaren inte har behörighet att skapa nya taggar visas ett felmeddelande om att den valda taggen inte längre är giltig. Författare kan kontakta administratörerna för att ändra ogiltiga taggar.

  Författare kan inte skapa eller spara ogiltiga taggar. De kan ta bort ogiltiga taggar och lägga till andra befintliga giltiga taggar och fortsätta.
