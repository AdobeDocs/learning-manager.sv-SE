---
description: Läs den här artikeln om du vill veta hur du hanterar deltagarna, skickar kursrelaterade e-postmeddelanden och påminnelser för dina sessioner.
jcr-language: en_us
title: Hantera elever för din session
contentowner: shhivkum
exl-id: 2f4f8589-2350-4683-a141-809084d6309a
source-git-commit: b01bf6bf89a3b9d860df712df1b7ef3a859407ed
workflow-type: tm+mt
source-wordcount: '1012'
ht-degree: 2%

---

# Hantera elever för din session

Läs den här artikeln om du vill veta hur du hanterar deltagarna, skickar kursrelaterade e-postmeddelanden och påminnelser för dina sessioner.

## Se sessioner eller moduler med väntande granskningar {#pending}

Instruktörer kan se sessioner eller moduler med väntande granskningar.

På sidan Sessioner/moduler visas kolumnen **Väntande granskningar** som visar antalet väntande granskningar för motsvarande session/aktivitet.

## Hantera väntelista för din session {#managewaitlistforyoursession}

När eleverna registrerar sig för din modul kan du se den senaste statusen för registreringen och väntelistan på sidan Väntelista.

1. I instruktörsappen väljer du Kommande sessioner > Väntelista i det vänstra navigeringsfönstret.

   Du kan se platsbegränsningen, antalet platser som är tillsatta och antalet lediga platser. En tabell visar även de elever som har satts upp på väntelistan. Detta är tomt om det inte finns några köer på väntelistan.

   ![](assets/waitlist.png)
   *Visa elever på väntelistan*

1. Välj den eller de elever som du vill bekräfta i väntelistan.
1. Välj Åtgärder > Bekräfta elever.

   De elever som du har bekräftat läggs till i listan över bekräftade elever.

Instruktörer kan avregistrera elever från sessioner. Detta avregistrerar dem också från motsvarande utbildningar. Välj fliken **[!UICONTROL Waitlist]**. Markera kryssrutan elever som ska avregistreras. Om du vill avregistrera dig väljer du **[!UICONTROL Actions]** > **[!UICONTROL Unenroll learners]**.

![](assets/unenroll-learners.png)
*Avregistrera eleverna*

### Väntelisterapport

Adobe Learning Manager nya **[!UICONTROL Waitlist Report]** tillåter instruktörer att ladda ned elevlista på väntelistan för alla instanser av en kurs. Instruktörer kan komma åt den här rapporten från avsnittet **[!UICONTROL Waitlist]** på sidan **[!UICONTROL Session Overview]**.

Följande kolumner är tillgängliga i väntelisterapporten:

* Kursnamn
* Instansnamn
* Instans-ID:
* Instansstatus
* Användarnamn
* E-post
* Unikt användar-ID
* Datum registrerad (tidszonen UTC)
* Status
* Väntelistenummer
* Väntlistegräns
* Platsbegränsning

Så här hämtar du rapporten från instruktörsavsnittet:

1. Logga in som **[!UICONTROL Instructor]**.
2. Välj en session på startsidan.
3. Välj alternativet **[!UICONTROL Waitlist]** på sidan **[!UICONTROL Session Overview]**.
4. Välj **[!UICONTROL Actions]** > **[!UICONTROL Export Report]** för att hämta rapporten **[!UICONTROL Waitlist]**.

## Markera närvaro för sessionen {#markattendanceforyoursession}

Du kan visa antalet bekräftade elever som deltar i sessionen, deras namn, deltagarstatus för eleverna och annan information från sidan Elever.

1. Klicka på Kommande sessioner > Elever i det vänstra navigeringsfönstret.
1. Välj eleven eller eleverna från listan över deltagare och gör något av följande:

   * Markera närvaro genom att klicka på Åtgärder > Markera närvaro. När statusen har angetts som Närvarat kan du inte ändra statusen.
   * Markera frånvaro genom att klicka på Åtgärder > Inte närvarat.
   * Klicka på Åtgärder > Ta bort elever om du vill ta bort en elev på grund av annullering eller av andra skäl.

   En elev kan inte slutföra en modul förrän närvarostatusen är Närvarat.

   ![](assets/markattendance.png)
   *Markera elevnärvaro*

## Skicka e-postmeddelanden till elever {#sendemailstolearners}

Du kan skicka e-postmeddelanden till specifika eller alla deltagare för din session. Funktionen Skicka e-post är mycket användbar om du vill bekräfta elevernas närvaro eller om du vill skicka ut meddelanden om sessionen. Du kan också använda alternativet Skicka e-post till alla för att skicka uppgifter och sessionsmaterial via e-post eller skicka allmän kommunikation till alla elever.

Gör något av följande för att skicka e-postmeddelanden till elever från sidan Elever i instruktörsappen:

* Om du vill skicka e-postmeddelanden till specifika deltagare markerar du deltagaren och klickar på Åtgärder > Skicka e-post till markerade.
* Om du vill skicka e-postmeddelanden till alla deltagare för att skicka ett kursmaterial eller en uppgift klickar du på Åtgärder > Skicka e-post till alla.

## Exportera elevlista {#exportinglearnerslist}

Du som är instruktör kan enkelt markera närvaron för alla elever genom att exportera deltagarlistan som en PDF. För att exportera deltagarlistan, från eleven i den vänstra rutan. Klicka på Åtgärder > Exportera elevlista (PDF).

När deltagarlistan har bekräftats för din session kan du exportera den som en PDF. I den här lätttryckta PDF-filen visas eleverna som en tabell. Du kan sedan markera närvaron eller ge poäng och göra eller lämna anteckningar till eleven, allt i samma PDF.

Lägg märke till en QR-kod i det övre högra hörnet av den här PDF. Denna funktion gör det möjligt för enskilda elever att skanna koden med Learning Manager-mobilappen för att markera sin närvaro.

![](assets/exportpdf.png)
*Skanna QR-koden för att markera närvaro*

## Godkänn eller avvisa ansökningar {#approveorrejectsubmissions}

Om elever har överfört dokument som tilldelningar, rapporter eller bedömningar för sessionen kan du visa dokumenten på sidan Inlämningar. Du kan använda materialet för att gradera eleven och antingen godkänna eller avslå ansökan.

1. I den vänstra rutan klickar du på antingen Kommande sessioner eller Tidigare sessioner, baserat på schemat för din session.
1. Klicka på kursen som du vill visa bidrag för.

   I den vänstra rutan klickar du på Submissions (Inlämningar).

1. Du kan visa bidrag från elever för den session som du valde. Markera den sändning du vill godkänna eller avvisa och klicka på Godkänn eller Avslå.

   Status för inskickningen ändras till Godkänd eller Avslagen beroende på din åtgärd.

## Konfigurera påminnelser för sessionen {#configureremindersforyoursession}

1. I den vänstra rutan klickar du på Kommande sessioner.
1. Klicka på kursen som du vill ställa in påminnelsen för. I den vänstra rutan klickar du på Påminnelser.
1. I panelen Välj påminnelse klickar du på Ange påminnelse.

   ![](assets/setreminder.png)
   *Konfigurera påminnelser för sessionen*

1. Gör så här:

   * I dialogrutan Inställningar för påminnelse anger du alternativ för när påminnelsen ska skickas till elever: Före deadline, På deadline eller Efter deadline.
   * I fältet Dagar före deadline anger du antalet dagar före deadline när du vill skicka påminnelsen till elever.
   * Ställ in upprepningen för påminnelsen.

   ![](assets/remindersettings.png)
   *Visa påminnelseinställningar*

1. Gör något av följande:

   * Klicka på bockmarkeringen för att spara påminnelsen.
   * Klicka på krysset om du vill avbryta påminnelsen.

   En automatisk kurspåminnelse skickas till alla elever vid det angivna datum som du har angett i påminnelseinställningarna.

   Om du redan har angett påminnelser för dina sessioner kan du se dem under befintliga påminnelsepaneler. Dessutom kan du lägga till ytterligare påminnelser i dina befintliga påminnelser.

   Om du vill ta bort en befintlig påminnelse klickar du på påminnelsen. Klicka på ikonen Ta bort (papperskorgen) för att ta bort påminnelsen på popup-menyn som visas.
