---
description: Läs den här artikeln om du vill veta hur du hanterar deltagarna, skickar kursrelaterade e-postmeddelanden och påminnelser för dina sessioner.
jcr-language: en_us
title: Hantera elever för din session
contentowner: shhivkum
exl-id: 2f4f8589-2350-4683-a141-809084d6309a
source-git-commit: 890315af5dc413c859315dc12d5d9618f67afc8e
workflow-type: tm+mt
source-wordcount: '1864'
ht-degree: 1%

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

### Hämta QR-koder för registrering och närvaro för elever

Instruktörer kan ladda ned QR-koder för sina tilldelade sessioner så att elever kan registrera sig för en kursinstans och markera närvaro eller slutförande genom att skanna QR-koden.

Det gör det möjligt för instruktörer att hantera deltagande i sessioner oberoende av varandra utan att behöva hjälp av administratören.

Följande steg är lämpliga för båda:

* Fysiska klassrumssessioner
* Onlineklassrumssessioner

Under en fysisk klassrumssession måste du som instruktör generera rätt QR-kod och klistra in den i klassrummet (eller skicka runt den) där eleverna deltar i sessionen så att de kan skanna QR-koden och markera sin registrering eller närvaro eller båda beroende på QR-koden.

Under en onlineklassrumssession kan du som instruktör skicka den genererade QR-koden via e-post, ett meddelandesystem eller på annat sätt så att eleverna kan skanna QR-koden och markera sin registrering eller närvaro eller båda beroende på QR-koden.


#### Hämta QR-koder för en session

1. Logga in på Adobe Learning Manager med rollen **instruktör**.
2. Gå till **instrumentpanelen för instruktörer**.
3. Öppna relevant **kursinstans**.
4. Välj fliken **Sessioner**.
5. Välj en session som är tilldelad dig.
6. Välj **QR-kod för session**.
   ![](assets/instructor-QR-code.png)

Du kan hämta följande QR-koder:

* **QR-kod för registrering** - gör det möjligt för elever att registrera sig för kursinstansen
* **Närvarokod QR** - markerar närvaro för sessionen
* **Registrering + närvarokod QR** - registrerar elever och markerar närvaro i en enda skanning

QR-koden hämtas som en PDF och kan delas digitalt eller visas under sessionen.

#### Vad händer när elever skannar QR-koden

* Elever skannar QR-koden med en mobil enhet.
* Adobe Learning Manager validerar eleven och sessionen.
* Baserat på QR-kodtyp:
   * Elever är registrerade i kursinstansen eller
   * Närvaro och slutförande registreras för sessionen

Alla uppdateringar återspeglas automatiskt i elevregister, utskrifter och rapporter.

#### Anteckningar

* QR-koder är bara tillgängliga för instruktörer som har tilldelats till sessionen.
* Regler för registrering, närvaro och slutförande som konfigurerats för kursen och sessionen fortsätter att gälla.
* Befintliga arbetsflöden för elevframsteg och rapportering förblir oförändrade.

#### Användningsfall

* Organisationer som kör stora volymer sessioner på plats (till exempel produktutbildning för proffs) kan göra det möjligt för instruktörer att skriva ut sessionsspecifika QR-koder som registrerar och markerar närvaro med en skanning.

* Inom detaljhandels-, tillverknings- och hälsovårdsutbildning, där elever ofta deltar i sessioner direkt från golvet eller utan förregistrering, kan en QR-kod (&quot;Enroll + Attendance&quot;) läggas vid dörren. Detta gör det möjligt för elever att själva betjäna sin registrering och närvaro via sina telefoner.

* Utbildningshändelser för partners eller kunder gör att utbildaren på plats enkelt kan anpassa sig till förändringar i rummet, ytterligare sessioner eller extra deltagare utan att behöva rådfråga administratören om nya QR-koder.

### Kalenderinbjudningar

* När en elev eller instruktör är registrerad i en klassrums- eller virtuell klassrumssession skickar Learning Manager en kalenderinbjudan (ICS-fil).
* Kalenderinbjudan omfattar:
   * Sessionens datum och tid
   * Sessionsdetaljer
   * **Direktsessionskopplingslänk** i kalenderbeskrivningen

Deltagarna kan öppna kalenderhändelsen och ansluta till sessionen direkt från sin kalender.

#### Ansluta till en session från Gmail

1. Öppna **Google Calendar**.
2. Välj sessionshändelsen.
3. Om du vill ha information om händelsen klickar du på länken **Anslut till session**.
4. Sessionen öppnas direkt i Adobe Learning Manager eller i det konfigurerade virtuella klassrumsverktyget.

Du behöver inte öppna det ursprungliga e-postmeddelandet för att komma åt sessionslänken.

#### Anslut till en session från andra kalenderklienter

Sessionslänken ingår i kalenderns händelsetext och är tillgänglig från:

* Microsoft Outlook
* Apple Calendar
* Andra kalenderprogram som stöder ICS-filer

#### Anteckningar

* Kalenderinbjudningar genereras automatiskt av Learning Manager.
* Tidszoninformationen i kalenderinbjudan justeras baserat på elevens valda tidszon.
* Den här förbättringen gäller nya inbjudningar till kalendern.
* Administratörer eller instruktörer behöver inte göra någon ytterligare konfiguration.


## Markera som slutförd för elever

Instruktörer kan markera varje elevs status som godkänd eller ej direkt från sidan Elever. Med den här funktionen kan instruktörer spela in resultatet av klassrumssessioner eller virtuella klassrumssessioner korrekt utifrån elevens prestanda.

Så här markerar du framgångar för elever:

1. Logga in på Adobe Learning Manager som instruktör.
2. Välj **[!UICONTROL Upcoming Sessions]** i den vänstra navigeringsrutan.
3. Välj **[!UICONTROL Learners]**.
4. Välj eleverna och sedan **[!UICONTROL Actions]**.
5. Välj något av alternativen nedan för att markera framgången för de valda eleverna:

   * **[!UICONTROL Mark Attended and Pass]**: Elever som markerats som godkända har slutfört modulen.
   * **[!UICONTROL Mark Attended and Fail]**: Elever som markerats som misslyckade har slutfört modulen men inte godkänts.

   ![I listrutan Åtgärder markeras alternativen &quot;Markera som närvarat och godkänd&quot; och &quot;Markera som närvarat och ej godkänd&quot; för instruktörer för att ange varje elevs framgångsstatus](/help/migrated/instructors/feature-summary/assets/mark-success-instructor.png)
   _Elevsida som visar menyn Åtgärder med alternativen Markera som närvarat och Godkänd och Markera som närvarat och Misslyckad markerade för att registrera elevresultat_

6. Välj **[!UICONTROL Yes]** i bekräftelsemeddelandet.

## Skicka e-postmeddelanden till elever {#sendemailstolearners}

Du kan skicka e-postmeddelanden till specifika eller alla deltagare för din session. Funktionen Skicka e-post är mycket användbar om du vill bekräfta elevernas närvaro eller om du vill skicka ut meddelanden om sessionen. Du kan också använda alternativet Skicka e-post till alla för att skicka uppgifter och sessionsmaterial via e-post eller skicka allmän kommunikation till alla elever.

Gör något av följande för att skicka e-postmeddelanden till elever från sidan Elever i instruktörsappen:

* Om du vill skicka e-postmeddelanden till specifika deltagare markerar du deltagaren och klickar på Åtgärder > Skicka e-post till markerade.
* Om du vill skicka e-postmeddelanden till alla deltagare för att skicka ett kursmaterial eller en uppgift klickar du på Åtgärder > Skicka e-post till alla.

## Svar på Capture-inbjudan

Instruktörer kan endast samla elevernas inbjudningssvar när alternativet **[!UICONTROL Invite Reply]** har aktiverats av ACAP-administratören. Administratörer måste kontakta supportteamet på [learningmanagersupport@adobe.com](mailto:learningmanagersupport@adobe.com) för att aktivera funktionen.

När du är klar kan du visa inbjudningssvaren i avsnittet **[!UICONTROL Learners]**. Gå till valfri session, välj **[!UICONTROL Learners]** och välj inbjudningssvaret i listrutan.

![](assets/invitation-status.png)

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
