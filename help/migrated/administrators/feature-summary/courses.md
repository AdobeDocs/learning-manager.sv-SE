---
description: Det här dokumentet består av hjälp med att skapa kursmoduler, instanser och kurser för administratörsrollen.
jcr-language: en_us
title: Skapa kursinstanser och utbildningsvägar
contentowner: manochan
exl-id: aba7417b-26a0-4160-878c-5814f84e5155
source-git-commit: 40cd12c186463517b20017229e44b6864056dedf
workflow-type: tm+mt
source-wordcount: '5635'
ht-degree: 1%

---

# Skapa kursinstanser och utbildningsvägar

Det här dokumentet består av hjälp med att skapa kursmoduler, instanser och kurser för administratörsrollen.

Författare skapar kurser. Elever kan gå kurserna och administratörer kan spåra elevers resultat baserat på kursförbrukningen.

## Översikt {#overview}

Författare skapar kurser. Elever följer sedan kurserna och administratörer kan spåra elevernas resultat baserat på kursförbrukningen. Administratörer kan se kurser som skapats av författare och utföra vissa aktiviteter som förklaras i det här avsnittet. Administratörer kan skapa unika utbildningsprogram med en fördefinierad uppsättning kurser för elever.

## Skapa instans av en kurs {#createinstanceofacourse}

### Konfigurera instanser

I den här utbildningen får du lära dig hur du konfigurerar instansstandardinställningar, lägger till en ny instans, annullerar och öppnar en instans på nytt och konfigurerar e-postmallar för en instans.

[![knapp](assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/8318911)

Skriv till <almacademy@adobe.com> om du inte kan starta utbildningen.

### Skapa en instans

När en författare har skapat en kurs kan du skapa instanser av kursen. Genom att skapa instanser av en kurs kan du erbjuda samma kurs till dina elever vid olika tidsperioder. Elever kan välja vilken instans som helst och registrera sig. Du kan konfigurera varje instans så att den har sin egen uppsättning med utmärkelsetecken, feedback och andra inställningar.

Om du vill skapa en instans

1. Klicka på **[!UICONTROL Courses]** i den vänstra rutan i webbapplikationen Administratör.
1. Välj önskad kurs i listan över kurser och klicka på **[!UICONTROL View Course]**.

   ![](assets/view-course.png)

   *Visa en kurs*

1. Klicka på **[!UICONTROL Instances]** i den vänstra rutan om du vill skapa instanser. Varje kurs har en instans som standard. Du kan antingen ändra standardinstansen eller lägga till instanser. Du kan inte ta bort kursinstansen.
1. Om du vill skapa en instans klickar du på **[!UICONTROL Add New Instance]** i det övre högra hörnet av kursinformationen. En ny instans av kursen visas.
1. Ange instansens egenskaper:

   * I fältet **[!UICONTROL Instance Name]** anger du namnet på den instans som du vill associera med kursen. Se till att du använder ett unikt namn för instansen.
   * Ange deadline för slutförande för instansen. Eleverna måste få statusen slutförd för kursen senast detta datum.
   * Klicka på **[!UICONTROL Show More Options]** om du vill visa andra alternativ för deadline.
   * **[!UICONTROL Enrollment Deadline]:** Det här är det datum då en elev förväntas registrera sig för ett utbildningsobjekt vid egenregistrering.
   * **[!UICONTROL Unenrollment Deadline]:** Du kan välja att begränsa avregistrering av eleven själv genom att ha en deadline för avregistrering.
   * **[!UICONTROL Timezone]:** Sök och välj sedan **[!UICONTROL Timezone]** i listrutan.

   En administratör kan besluta att ha tidsgränser för slutförande av en kurs eller ett utbildningsprogram baserat på behov. Vi rekommenderar dock att du har en för klassrums-/virtuella klassrumsbaserade utbildningar.

   ![](assets/create-an-instance.png)

   *Ange deadline för slutförande*

### Visa instansens egenskaper {#viewpropertiesoftheinstance}

![](assets/properties-of-aninstance.png)

*Visa egenskaper för instansen*

1. **Moduler:** Antalet moduler som har skapats av författaren till kursen
1. **Elever registrerade:** Antalet elever som har registrerats för kursen av administratören.
1. **Sessioner:** Antalet virtuella klassrums- och klassrumsmoduler i kursen.
1. **Feedback aktiverad:** Visar om L1-, L2- och L3-feedback har aktiverats för den här kursen.

>[!NOTE]
>
>Administratören avbryter sessionerna genom att gå till Instanser > Sessioner och välja Avbryt session.

### Hantera instanser

>[!INFO]
>
>I den här utbildningen får du lära dig redigera instansinformation och instansegenskaper.<br><br>[![knapp](assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/8318912)</br></br>

Skriv till <almacademy@adobe.com> om du inte kan starta utbildningen.

### Ta bort en instans {#retireaninstance}

Utför stegen nedan om du vill ta en instans ur bruk.

1. I instansen väljer du listrutan och väljer alternativet **[!UICONTROL Retire instance]**.

   ![](assets/retire-an-instance.png)

   *Ta en instans ur bruk*

1. Klicka på fliken **[!UICONTROL Retired]** på sidan Instanser om du vill söka efter alla utfasade instanser.

### Återställa en instans {#restoreaninstance}

Så här återställer du en utfasad instans till ett aktiveringsläge:

1. I instansen klickar du på listrutan och väljer alternativet **[!UICONTROL Reopen instance]**.

   ![](assets/restore-an-instance.png)

   *Återställ en instans*

1. Instansen återställs nu till ett aktivt läge.

### Ta bort en instans

Administratörer kan ta bort instansen med alternativet **Ta bort den här instansen** direkt efter att den har skapats. Du kan inte ta bort instanser om det finns en session länkad till den eller om det finns elever som är registrerade till den.

![](assets/delete-this-instance.png)

*Ta bort en instans*

>[!NOTE]
>
>Du kan inte ta bort standardinstansen.

### Skicka e-postmeddelanden på instansnivå

Så här skickar du e-postmeddelanden på instansnivå till registrerade elever:

1. Välj alternativ för valfri instans på sidan **[!UICONTROL Instances]** och klicka sedan på **[!UICONTROL Email Enrolled Learners]**.

![e-postmeddelanden på instansnivå](assets/adhoc-email.png)

*Skicka e-post till elever som har registrerat sig för instansen*

1. I dialogrutan **[!UICONTROL Create Announcement]** väljer du Skriv som e-post. Ange ämne, skriv meddelandet och klicka på **[!UICONTROL Save]**. Utbildningen väljs ut automatiskt.

   ![Skapa meddelande som e-post](assets/email-announcement.png)

   *Skapa meddelande som e-post*

1. När du har klickat på **[!UICONTROL Save]** visas ett bekräftelsemeddelande om att meddelandet har skapats. Klicka på **[!UICONTROL Publish Now]** för att publicera meddelandet.

   ![Meddelandet har skapats](assets/announcement-successful.png)

## Registrera elever på kurser

Under den här utbildningen kommer du att lära dig hur du registrerar, avregistrerar och återregistrerar elever.

[![knapp](assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/8318916)

Skriv till <almacademy@adobe.com> om du inte kan starta utbildningen.

### Registrera elever i olika instanser

1. Välj en kurs i listan över kurser.
1. Välj **[!UICONTROL Learners]** i den vänstra panelen.
1. Välj **[!UICONTROL Enroll]**.

   ![Registrera elever](assets/enroll-learners-new.png)

   *Publish kursen*

1. I dialogrutan [!UICONTROL **Registrera elever**] kan du:

   * Välj en instans för att registrera en elev från listrutan Välj instans.
   * Välj användaren eller användargrupperna eller båda i fältet Inkludera elever.
   * Välj de elever som du vill ska uteslutas från instansen i fältet Exkludera elever.
   * Längst ned i dialogrutan väljer du Ja om du vill att en eller flera elever ska registrera sig för den valda instansen.

1. Välj **[!UICONTROL Proceed]**.

   ![fortsätt](assets/proceed.png)

   *Fortsätt till registrering av elever*

### Visa registreringsrapport för en instans

1. Välj en kurs i listan över kurser.
1. Välj **[!UICONTROL Learners]** i den vänstra panelen.
1. Välj **[!UICONTROL Actions]** > **[!UICONTROL Export]**.

Excel-filen innehåller kalkylblad för varje instans. Ett kalkylblad består av följande fält:

* Elever
* E-post
* Unikt användar-ID
* Kursnamn
* LO unikt ID
* Status
* Urvalskriterier
* Registreringsdatum/avregistreringsdatum (tidszonen UTC)
* Slutförandedatum (tidszonen UTC)
* Inlämningsdatum (tidszonen UTC)
* Påbörjad datum (tidszonen UTC)
* Quiz-poäng
* Chefens namn
* Adress
* användarstatus
* Expertområde
* Kommentarer
* Antal besök
* Besöksdatum
* Tidsstämplar (tidszonen UTC)
* Använd tid (i minuter)

>[!NOTE]
>
>Om du aktiverar multiregistrering läggs flera rader till i elevens betygsrapport för varje kurs (en rad för varje instans).
>
>Om du har ställt in rapporteringsautomatisering som endast förutser en rad per kurs måste du göra de nödvändiga justeringarna av rapporteringsautomatiseringen innan du aktiverar funktionen Flerregistrering.

### Hantera elevlista för en kurs {#managelearnerslistforacourse}

1. Klicka på kursnamnet på kursens miniatyrbild.
1. Klicka på **[!UICONTROL Learners]** i den vänstra rutan.

![](assets/courses-learners.png)

*Välj elever i en kurs*

Du kan utföra följande åtgärder från sidan Elever:

* Markera eleven du vill ta bort och klicka på [!UICONTROL **Åtgärder**] > [!UICONTROL **Ta bort**].
* Markera den elev vars närvaro du vill markera och klicka på [!UICONTROL **Åtgärder**] > [!UICONTROL **Markera som slutförd**].

Klicka på [!UICONTROL **Återställ**] om du vill att eleverna ska kunna återställa en modul och konsumera modulen igen. Klicka på Ja i dialogrutan som visas för att bekräfta återställningen. Moduler som har slutförts kan inte återställas. Endast felaktiga eller ofullständiga moduler kan återställas.

Du kan också exportera elevlistan i ett Excel-ark. Om du vill exportera elevlistan klickar du på [!UICONTROL **Åtgärder**] > [!UICONTROL **Exportera**].

>[!NOTE]
>
>Om det finns flera instanser för en kurs visas elevlistan i Excel på varje flik separat. Elevlistan består av elevnamn, status och urvalskriterier. Elevstatus kan vara **Inte påbörjat**, **Pågår** eller **Slutfört**.

### Exportera elever i väntande godkännandetillstånd

En administratör, chef eller anpassad administratör kan exportera data för elever som har statusen Väntande på registrering till godkännande. Du kan exportera data via fliken **Kurs > Elev** och klicka på listrutan Åtgärd.

Alternativet finns när ingen elev är registrerad/väntar på godkännande av chefsgodkänd kurs och en tom rapport genereras. Du kan också exportera när elever är i väntande tillstånd för godkännande, registreringsläge, väntande tillstånd och avregistrerat tillstånd.

Rapporten innehåller data för aktiva, borttagna och avbrutna användare om de väntar på godkännande. Rapporten innehåller också data om interna och externa användare som är i väntande läge för godkännande.

Om en elev som tidigare befann sig i väntande tillstånd för godkännande avregistrerar sig, kommer hans/hennes meritlista inte att finnas med i rapporten. Även om en elev som tidigare befann sig i läget Väntande godkännande och registreras till kursen av admin/chef/anpassad admin-registrering, finns hans/hennes post i rapporten.

## Hantera massregistrering, närvaro och slutförande av elever {#bulk-enrollment}

Med hjälp av massregistreringsfunktionen i Adobe Learning Manager kan administratörer effektivt registrera stora elevgrupper i kurser, certifieringar eller utbildningsprogram genom att ladda upp en CSV-fil. Denna process sparar tid, garanterar konsekvens och stöder skalbarhet i organisationen. Dessutom kan administratörer och instruktörer uppdatera elevinformation, närvaro och slutföranden i grupp genom att överföra CSV-filer, minimera manuellt arbete och säkerställa datanoggrannhet.

Du kan använda samma CSV-filformat för registrering, närvaro och slutförande. Ange bara elevers mejl-ID under kolumnen &quot;E-post&quot; och spara filen med ett namn som baseras på åtgärden, till exempel bulk_enrollment.csv, bulk_attendance.csv eller bulk_completion.csv. Endast CSV-format stöds. UTF-8-format stöds inte. Hämta [CSV-exempelfilen](assets/Sample-Bulk-Action-CSV.csv).

### Registrera elever i grupp med en CSV

I stället för att lägga till elever en i taget kan administratörer registrera upp till 100 000 användare samtidigt genom att överföra en CSV-fil. Filen måste innehålla en kolumn märkt **userEmail** med e-postadresserna till eleverna som ska registreras.

Så här registrerar du elever i grupp med CSV:

1. Logga in som administratör.
2. Välj en kurs i avsnittet **[!UICONTROL Courses]**.
3. Välj **[!UICONTROL Learners]** på sidan **[!UICONTROL Course Overview]**.
4. Välj **[!UICONTROL Enroll]** och sedan **[!UICONTROL Upload a CSV]**.\
   ![](assets/upload-a-csv-learners.png)
   _Registrerar elev med CSV-uppladdning_
5. Överför en CSV-fil och välj **[!UICONTROL Proceed]**.

CSV-filen innehåller en kolumn som är märkt Användarens e-postadress. Ange e-postadresserna till användarna i den här kolumnen.

### Markera slutförande av kurs i bulk

Administratörer kan snabbt markera slutförda kurser för många elever samtidigt genom att ladda upp en CSV-fil med sina e-postadresser. Det sparar tid jämfört med att uppdatera varje elev individuellt. CSV-kolumnen userEmail visar vilka elever som ska uppdateras. Du kan märka upp till 10 000 elever som slutförda i en överföring.

Så här markerar du massslutförande:

1. Välj en kurs i avsnittet **[!UICONTROL Courses]**.
2. Välj **[!UICONTROL Learners]** på sidan **[!UICONTROL Course Overview]**.
3. Välj **[!UICONTROL Actions]** och sedan **[!UICONTROL Mark Completion]**.
4. Välj **[!UICONTROL Bulk]**.
5. Överför en CSV-fil med en kolumn för userEmail som visar elever som har slutfört kursen.

   ![](assets/bulk-completion.png)
   _Markerar massslutförande med CSV_

### Markera närvaro i bulk

Administratörer kan markera närvaron för många elever samtidigt med en funktion för gruppnärvaro. I stället för att uppdatera varje elevs närvaro individuellt kan administratörer överföra en CSV-fil som innehåller elevernas e-postadresser. Kolumnen userEmail i CSV-filen identifierar vilka elevers närvaro som ska registreras. Denna process kan hantera upp till 10 000 elever i en enda överföring, vilket gör närvaromarkeringen snabbare och effektivare.

Så här markerar du gruppnärvaron:

1. Välj en kurs i avsnittet **[!UICONTROL Courses]**.
2. Välj **[!UICONTROL Attendance & Scoring]** på sidan **[!UICONTROL Course Overview]**.
3. Välj **[!UICONTROL Actions]** och sedan **[!UICONTROL Mark Bulk Attended]**.
4. Överför en CSV-fil som innehåller kolumnen userEmail med e-postadresserna till de elever vars närvaro du vill uppdatera.

   ![](assets/mark-bulk-attendance.png)
   _Markera gruppnärvaro med CSV_

>[!NOTE]
>
>Du kan markera närvaro för upp till 10 000 användare i grupp med CSV.

### Vanliga CSV-överföringsfel

* Elevens e-postadress i CSV-filen finns inte i Adobe Learning Manager-användarkatalogen.
* Filformatet är felaktigt.
* Filen innehåller extra kolumner eller ogiltiga data.

![](assets/error-bulk.png)
_Felmeddelande_

Du kan hämta och visa CSV-filen med en lista över fel med misslyckade användare på radnivå för enkel identifiering.

## Väntelista

Väntelisteavsnittet gör det möjligt för elever att väntelista sig till klassrumskurser när antalet platser är begränsade, baserat på den ordning i vilken de registrerat sig. Administratörer kan hantera detta genom att välja elever på väntelistan och tilldela platser utöver den ursprungliga gränsen. När en plats har tilldelats av administratören registreras eleven omedelbart till kursen.

### Väntelisterapport

Med Adobe Learning Manager kan administratörer hämta listan över elever på väntelistan för alla instanser av en kurs. Administratörer kan komma åt den här rapporten från avsnittet Väntelista på sidan **[!UICONTROL Course Overview]**.

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

Så här hämtar du rapporten från avsnittet Administratör:

1. Logga in som **[!UICONTROL Admin]**.
2. Gå till avsnittet **[!UICONTROL Course]** och välj den obligatoriska kursen.
3. Välj alternativet **[!UICONTROL Waitlist]** på sidan **[!UICONTROL Course overview]**.
4. Välj **[!UICONTROL Actions]** > **[!UICONTROL Export Report]** för att hämta rapporten **[!UICONTROL Waitlist]**.

   ![](assets/export-report-waitlist.png)
   _Exportera rapport_

## Exportera elevnärvaro {#attendance}

För alla klassrum och VC-kurser kan du ladda ned listan över elever som har deltagit i denna kurs, för alla instanser.

Klicka på **[!UICONTROL Attendance and Scoring]** i den högra rutan på sidan med kursinformation.

Klicka på rullgardinsmenyn **[!UICONTROL Actions]** i det övre högra hörnet på sidan. Klicka sedan på alternativet **[!UICONTROL Export Learner List (PDF)]**.

![](assets/export-list-of-learners.png)

*Exportera listan över elever som PDF*

PDF kan du visa samma uppsättning med elever som en instruktör gör.

När du hämtar PDF kan du se tidszonen (i UTC) som användes när kursen skapades.

## Lägg till feedback om L1 och L3 {#addl1andl3feedback}

>[!NOTE]
>
>Om det här feedbackalternativet inte visas på ditt konto har ditt konto redan uppgraderats till det nya formuläret L1-feedback. Mer information finns i [L1-feedbackformuläret](/help/migrated/administrators/feature-summary/l1-feedback-form.md).


Du kan lägga till L1- och L3-feedbackalternativ medan du skapar kurserna:

1. Klicka på Kurser i den vänstra rutan när du har loggat in som administratör. Lista över alla kurser visas på höger sida.
1. Klicka på den kursruta som du vill lägga till feedback om L1 eller L3 för.
1. Klicka på instance default (standardinställning) i den vänstra rutan.
1. Klicka på växlingsknappen för cirkel på bredvid L1- eller L3-feedback för att aktivera den.
1. Lägg till L3-feedbackfrågan i textområdet under L3-frågan.

### Obligatorisk L1-feedback {#mandatory-l1-feedback}

Du kan göra alla frågor eller den första frågan obligatoriska i en L1-feedback.

![](assets/make-all-questionsmandatory.png)

*Gör alla frågor eller den första frågan obligatoriska i en L1-feedback*

Nu kan du skapa frågorna, som nu blir obligatoriska.

![](assets/create-mandatoryquestions.png)

*Skapa frågorna*

Om de två obligatoriska frågorna av någon anledning inte har någon text visas frågorna inte i feedbackformuläret.

>[!NOTE]
>
>Det räcker inte att du aktiverar dessa inställningar på utbildningsprograminstansen. Du måste också aktivera dessa inställningar på nivån Kursinstans för varje kurs i Utbildningsprogrammet.

Om du aktiverar **[!UICONTROL Make All Questions Mandatory]** på sidan Standardinställningar för instans ärvs dessa inställningar av alla nya instanser som skapas därefter.

![](assets/instance-defaults-makeallquestionsmandatory.png)

*Visa sidan för instansstandardvärden*

### L1-feedback på kursnivå {#l1-feedback-course-level}

I tidigare versioner av Learning Manager kunde en administratör aktivera L1-feedback för utbildningsprogrammet.

I den här versionen av Learning Manager kan administratören skicka feedback om L1 för alla kurser som ingår i utbildningsprogrammet. Administratören måste se till att L1-feedback är aktiverad för alla kurser på kursinstansnivå.

1. Klicka på **[!UICONTROL Learning Programs]** > **[!UICONTROL View Learning Program]** i Admin-appen för att aktivera L1-feedback för varje kurs.

1. Klicka på **[!UICONTROL Instances]** > **[!UICONTROL L1 Feedback Enabled]**.

1. Aktivera alternativet **[!UICONTROL Enable for Each Course]**.

   ![](assets/enable-l1-feedbackforcourse.png)

   *Aktivera kursfeedback*

   Endast aktivering av den här funktionen på nivån Utbildningsprogram aktiverar inte L1-feedback för kurserna i det här programmet. Gå till varje kurs i utbildningsprogrammet och aktivera växlingsknappen L1-feedback för att aktivera L1-feedback.

   ![](assets/l1-reaction-feedback.png)

   *Aktivera L1-feedback för varje kurs*

   Om L1-feedback är aktiverad för alla kurser men är inaktiverad i instansen för utbildningsprogrammet kommer feedback om L1 inte att utlösas för kurserna.

### Språkspecifika frågeformulärsrapporter

Quizrapporter hjälper till att utvärdera en elevs resultat efter slutförande av ett utbildningsprogram eller en kurs.

Learning Manager underlättar för närvarande inlärning i 13 gränssnittsspråk och 32 innehållsspråk. Även om det här alternativet är elevvänligt och underlättar för oss att stödja våra globala elever är det besvärligt för administratörer att hämta rapporter som de försöker hämta på olika platser.

Quiz-rapporter, visa data på olika språk förutsatt att kursen erbjuds på flera språk. Hittills har rapporter som skapats av Admin visat svar under varandra oberoende av vilket språk frågeformuläret användes på. **Exempel**: Om en användare har gjort ett frågeformulär på nederländska kan administratören bara visa de frågeformulärsrapporter som användare på nederländska försöker sig på åt gången. Administratören som har valt engelska som gränssnittsspråk kunde inte visa rapporter för alla användare samtidigt, oavsett språket som användes.

Detta korrigeras nu eftersom administratören nu kan visa alla rapporter på respektive språk som eleven försökt alla på en gång, oavsett vilken innehållsplats som valts. Quiz-försök på olika språk läggs till som ytterligare kolumner i frågeformulärsrapporten.

### Aktivera L1-feedback på kontonivå {#l1-feedback-account-level}

*Aktivera L1-feedback på kontonivå*

En administratör kommer att kunna aktivera L1-feedback för nyligen skapade kurser och utbildningsprogram genom att aktivera den här inställningen på kontonivå. Att aktivera den här inställningen påverkar dock inte befintliga kurser och utbildningsprogram

Om detta är aktiverat kommer feedback för alla nya utbildningar och nya instanser att vara aktiverad som standard. Om en författare/administratör besöker instansen, standardvärden och stänger av den manuellt, respekteras instansen.

Om du vill aktivera L1-feedback klickar du på **[!UICONTROL Settings]** > **[!UICONTROL Feedback]** i Admin-appen.

![](assets/l1-feedback-settings.png)

*Visa sidan Feedback-inställningar*

Klicka på **[!UICONTROL Edit]** i det övre högra hörnet och växla alternativet för att aktivera L1-feedback.

När en författare skapar en kurs aktiveras **[!UICONTROL L1 feedback]** automatiskt för den nya kursen på instanssidan i Admin-appen.

<!--![](assets/l1-feedback-enabled.png)-->

Du kan också inaktivera L1-feedback genom att växla alternativet **[!UICONTROL Enable]**, som visas nedan:

![](assets/disable-l1-feedback.png)

*Aktivera eller inaktivera L1-feedback*

### Lägg till beskrivande frågor för L1- och L3-feedback {#descriptive}

Som en del av november-versionen av Learning Manager har ett alternativ för att lägga till beskrivande frågor tillhandahållits. Administratörer har möjlighet att lägga till dessa frågor för elever. Denna bestämmelse kompletterar standarduppsättningen med frågor som tillhandahålls av Learning Manager. Du kan också göra dem obligatoriska genom att välja alternativet under frågan.

Du kan lägga till två beskrivande frågor för L1-feedback och en beskrivande fråga för L3-feedback.

När du har aktiverat L1-feedback kan du visa alternativen som visas på följande ögonblicksbild.

![](assets/l1-feedback-desc-questions.png)

*Lägg till beskrivande frågor för feedback om L1 och L3*

Om du vill att frågeformuläret ska visas för eleven omedelbart efter slutförandet av kursen kan du välja alternativet.

Nedan visas ett urval av L1-frågeformuläret som referens. Elever kan se frågeformuläret i nedanstående format. Test-1 och Test-2 är beskrivande frågor.

![](assets/l1-output.png)

*Frågor om feedback på en exempelkurs*

När du har aktiverat L3-feedback kan du visa alternativen som visas på ögonblicksbilden nedan:

![](assets/l3-feedback-desc-questions.png)

*Aktivera L3-feedback*

Fråga 2 är den beskrivande frågan för L3-feedback. Du kan göra det obligatoriskt genom att klicka på alternativet under frågan.

Nedan visas ett urval av L3-frågeformuläret som referens. Elever kan se frågeformuläret i nedanstående format.

![](assets/l3-output.png)

*Visa L3-feedbackutdata*

### Ställ in L1- och L3-feedbackfrågeformulär {#setupl1andl3feedbackquestionnaire}

Du kan ställa in L1- och L3-feedbackfrågeformulär och även ställa in påminnelser på kontonivå.

1. Klicka på **[!UICONTROL Settings]** och sedan på **[!UICONTROL Feedback]** i den vänstra rutan när du har loggat in som administratör.\
   Sidan med feedbackinställningar visas med två flikar: **[!UICONTROL L1 Feedback]** och **[!UICONTROL L3 Feedback]**.\
   Fliken **[!UICONTROL L1 Feedback]** består av en lista med standardekät **[!UICONTROL L1 feedback]** för klassrumskurser och kurser i egen takt tillsammans med påminnelseinställningar. På fliken **[!UICONTROL L3 Feedback]** kan du visa standardinställningarna för L3-feedback och påminnelser.

1. Klicka på Redigera längst upp till höger på sidan om du vill ändra den befintliga enkäten.\
   På fliken **[!UICONTROL L1 Feedback]** kan du aktivera/inaktivera varje fråga genom att klicka på växlingsknappen Ja/Nej.\
   På fliken **[!UICONTROL L3 Feedback]** kan du ändra standardsatsen för feedback.\
   Klicka på **[!UICONTROL Add New Reminder]** längst ned på sidan och välj när påminnelserna ska skickas.

1. Klicka på **[!UICONTROL Save]** längst upp till höger på sidan.

I L1-feedback kan du se två uppsättningar frågeformulär tillsammans med en standardfråga. Det första frågeformuläret avser kurser i egen takt som också kan användas för aktivitetsbaserade kurser. Andra uppsättningen enkäter kan användas för kurser av typen klassrum och virtuellt klassrum.

## Visa feedback om L1 och L3 {#viewl1andl3feedback}

Du kan visa L1-feedback från elever för en kurs och L3-feedback från chefer för elever.

1. Klicka på valfri kursruta i kurslistan.
1. Klicka på L1-feedback eller L3-feedback i den vänstra rutan för att se den feedback som tagits emot.
1. Välj instansen i listrutan för att visa återkopplingen för den specifika instansen.

## Diskussionstavla

Funktionen Diskussionstavla gör att eleverna kan se kursdiskussionerna. Du som är administratör kan ta bort alla kommentarer efter behov. Administratörer kan aktivera det här alternativet under kursinställningar.

## Kursmoderering {#coursemoderation}

När en författare lägger till, uppdaterar eller tar bort moduler och återpublicerar en kurs får alla administratörer ett meddelande om detta. Administratörer kan sedan visa ändringarna, jämföra det gamla och det nya innehållet genom att klicka på länken och godkänna eller avslå ändringarna.

Klicka på **[!UICONTROL Settings]** > **[!UICONTROL General]** för att aktivera kursmoderering. Markera kryssrutan **[!UICONTROL Course Moderation]** för att aktivera funktionen.

![](assets/2.png)

*Aktivera kursmoderering*

Klicka på meddelandet för att se de ändringar som författaren har gjort i kursen. Godkänn eller avvisa sedan de ändringar som författaren har gjort. Om du väljer att godkänna kommer kursen att publiceras igen. Om du avvisar uppdateringarna finns den tidigare versionen av kursen kvar. I båda fallen skickas ett meddelande till författaren.

![](assets/1.png)

*Författarförfrågningar för kursuppdateringar*

Om det finns flera författare som uppdaterar samma kurs kommer den senaste eller senast utförda ändringen att återspeglas i administratörens meddelande. Sedan kan du godkänna eller avvisa de senaste ändringarna.

## Exportera checklistedata {#export-checklist-data}

Öppna en kurs som innehåller en checklista från listan över kurser. I den vänstra rutan visas alternativet **[!UICONTROL Checklist]**.

![](assets/export-checklist.png)

*Exportera checklistedata*

Klicka på alternativet och utför följande på kurssidan:

1. Markera instansen och modulen.
1. Klicka på **[!UICONTROL Actions]** > **[!UICONTROL Export]** och exportera sedan elevens checklisterapport.

På sidan **[!UICONTROL Checklist]** kan en instruktör exportera checklisterapporten från listrutan **[!UICONTROL Actions]**.

CSV-rapporten innehåller följande fält:

* Användarnamn
* Mejladress till användare
* Chefens namn och e-postadress
* Utbildningsnamn
* Utbildningsinstans
* Instruktörens namn och e-postadress
* Inskickat den
* Utvärderingsstatus
* Frågor med faktisk text
* Användarstatus
* Profil
* Aktiva fält

När du laddar ned en rapport efter att du har valt ett statusfilter, kommer den nedladdade elevens betygsrapport att innehålla elevdata baserat på det tillämpade statusfiltret. Det tillagda filtret visas även för anpassad administratör och chef när de ska generera ett elevintyg.

## Visa kurser {#viewingcourses}

Du som är administratör kan visa en lista över alla tillgängliga kurser.   Klicka på **[!UICONTROL Courses]** i den vänstra rutan för att visa listan över kurser med alternativ för sökning och filter. Du kan också visa kursens effektivitetsprocent för varje kurs på kursens miniatyrbilder.

>[!NOTE]
>
>Du kan ta en kurs ur bruk efter att den har konsumerats av elever eller när du vill lägga till en viss kurs efter publicering. Du kan endast dra in en kurs när den är i publicerat tillstånd. Du kan visa en lista över alla utfasade kurser genom att klicka på fliken **[!UICONTROL Retired]**.

## Visa quiz-poäng {#viewquizscores}

1. Klicka på kursnamnet på kursens miniatyrbild.
1. Klicka på Quiz-poäng i den vänstra rutan.

Du kan visa quiz-poängen för en viss kurs baserat på användarnamn eller baserat på varje fråga. Välj Efter användare eller Efter fråga flikar därefter.

Välj instanstypen från rullgardinsmenyn för att visa poängen baserat på varje instans av kursen.

## Standardinstans

Administratörer kan ange standardmärken, inställningar för spelifiering och påminnelser på sidan **[!UICONTROL Default Instance]**. Om du vill ändra standardinstansinställningarna väljer du **[!UICONTROL Default Instance]** > **[!UICONTROL Edit]**.

* **[!UICONTROL Badge]**: Välj standardmärken i listrutan.
* **[!UICONTROL Gamification]**: Konfigurera inställningar för spelifiering, inklusive poäng för slutförande, tidig slutförande och slutförande. Administratörer har möjlighet att välja inställningar på kontonivå eller anpassa spelifieringspunkterna för den här instansen.
* **[!UICONTROL L1 Reaction Feedback]**: Aktivera fördefinierade frågor för elevfeedback efter slutförande av kursen, med alternativ för att göra frågor obligatoriska.
***[!UICONTROL &#x200B; L3 Behaviour Change Feedback]**: Aktivera feedbackfrågor för elevens chef när kursen har slutförts.
***[!UICONTROL &#x200B; Reminder Settings]**: Ställ in och hantera påminnelser om deadlines med alternativ för eskalering.

### Ange eskaleringsnivå {#escalation}

För att skicka e-postmeddelanden måste en administratör uttryckligen välja eskaleringsnivån för att:

* Chef
* Chef och överhoppad chefsnivå

![](assets/escalation-notification.png)

*Ställ in eskaleringsnivå*

## Kommentarer till slutförande

Administratörer kan lämna kommentarer när de markerar en elev som slutförd för kurser, utbildningsvägar eller certifieringar. Kommentarerna är till hjälp när det gäller regelefterlevnad och revision. Administratörer kan enkelt lägga till kommentarer för en elev eller flera elever samtidigt.

### Lägga till kommentarer om slutförande

Gör så här för att lägga till kommentarer om slutförande:

1. Logga in som **[!UICONTROL Admin]**.
2. Gå till sidan **[!UICONTROL Courses]** och välj en kurs.
3. Välj **[!UICONTROL Learners]** på kurssidan.
4. Välj den enskilda eleven eller flera elever.
5. Välj **[!UICONTROL Actions]** och sedan **[!UICONTROL Mark Completion]**.
6. Skriv den avslutande kommentaren i dialogrutan.

   ![](assets/comments.png)
   _Slutförandekommentar_

Den här processen är densamma för utbildningsvägar och certifieringar. För utbildningsvägar kan du filtrera och välja alla kurser eller bara enskilda kurser som ska markeras som slutförda.

![](assets/learning-path.png)
_Välj flera kurser att slutföra_

Kommentarer visas i rapporten [Elevens betygsutdrag](/help/migrated/administrators/feature-summary/reports.md#learner-transcripts).

## Förhandsgranska kurser {#previewcourses}

Administratören kan förhandsgranska kurser genom att klicka på alternativet **[!UICONTROL Preview as learner]** medan kursmodulerna visas.

1. Klicka på **[!UICONTROL Courses]** i den vänstra rutan när du har loggat in som administratör.
1. Klicka på en kursruta i listan över kurser på sidan.
1. Klicka på Förhandsgranska som elev i den vänstra rutan och klicka på modulnamnet på sidan för att förhandsgranska kursmodulen i spelaren.

## Kurseffektivitet {#courseeffectiveness}

Kursens effektivitet utvärderas för att förstå nyttan av en kurs för eleven. Det är en kombination av resultat från elevfeedback på kursinnehållet, quizresultaten för en elev och chefens feedback som utvärderar en elev baserat på lärdomar från kursen.

Administratören kan visa kurseffektivitetsklassificeringen på kursens miniatyrbilder så som visas på ögonblicksbilden nedan. Du kan se betyget för den här kursen som 100.

<!--![](assets/course-effectiveness-tag1.png)-->

Värdet för kurseffektivitet har erhållits med beaktande av L1-, L2- och L3-feedbackvärden. Klicka på värdet för kurseffektivitet för att visa uppdelningen av varje feedback. Ett popup-fönster visas enligt nedan.

![](assets/course-effectiveness.png)

*Visa kurseffektivitet för L1-, L2- och L3-feedback*

I den här exempelögonblicksbilden fick 1 av 1 användare alla tre feedback, därav är poängen 100/100. Från den här tabellen kan du förstå att om någon av de tre återkopplingarna (L1, L2 och L3 ) inte ges för en kurs, har det en negativ inverkan på den totala effektiviteten. Klicka på nedåtpilen i det nedre högra hörnet av popup-fönstret för att se hur beräkningarna av kurseffektivitet görs.

![](assets/course-effectiveness-calculations.png)

*Beräkning av kurseffektivitet*

Enligt cirkeldiagrammet ovan viktas L3-feedback från chefen mer.

## Söka efter kurser och utbildningsprogram {#searchingcoursesandlearningprograms}

Adobe Learning Manager gör det enklare för dig att snabbt hitta de kurser/utbildningsprogram du väljer. Du kan söka efter dina kurser på två sätt:

1. Använda sökfältet. Klicka på sökikonen som visas i det övre högra hörnet. Ett sökfält visas. Skriv in kursnamnet eller nyckelord som är associerade med dina kurser för att hitta dina kurser/utbildningsprogram. Du kan också söka med fördefinierade taggar som Captivate, C, Java och HTML. Taggar är sökbara i sökfältet, vilket innebär att taggarna visas i sökfältet när du skriver.
1. Genom att filtrera listan över kurser/utbildningsprogram med filtren. Du kan filtrera kurserna efter tillstånd som Alla, Publicerade, Utkast och Utfasade. Utkastfilter visas inte i administratörsläge.

Du kan söka baserat på kompetenser genom att klicka på Kompetenser och välja dem. Som administratör kan du sortera kurserna på fyra sätt så att du lättare hittar den kurs du behöver. Klicka på Sortera efter och välj Alfabetisk stigande ordning, Alfabetisk fallande ordning, Kursens uppdaterade datum eller kursernas effektivitet.

<!--![](assets/admin-sortby.png)-->

Du kan sortera utbildningsprogram på tre sätt: stigande i alfabetisk ordning, fallande i alfabetisk ordning och baserat på uppdaterat datum.

## Registrera elever {#enrollinglearners}

Du kan följa samma steg för att registrera elever för kurser, utbildningsprogram och certifieringar. Chefer kan även registrera elever under honom/henne med följande steg.

Administratören registrerar vissa elever för obligatoriska kurser enligt organisationens krav:

1. Håll muspekaren på publicerade kursplattor och klicka på Registrera elever.\
   Du kan även klicka på en publicerad kursruta och klicka på elever i den vänstra rutan. En sida med en lista med elever visas. Klicka på Registrera.\
   Dialogrutan Registrera elever visas.

1. Välj instansen i listrutan Välj instans. I listrutan visas alla instanser, inklusive aktiva, utfasade och utgångna instanser.

>[!NOTE]
>
>Administratören kan ta bort registrerade elever för en kurs genom att klicka på rullgardinspilen på sidan Elever och genom att klicka på **[!UICONTROL Actions]** > **[!UICONTROL Remove]**.

![](assets/enroll-learners.png)

*Lägg till kommentarer när du registrerar elever*

*Registrera elever*

## Användare

+++Inkludera elever

Välj de användargrupper och enskilda elever (med e-post-ID eller namn) som du vill inkludera. Lägg till alla användargrupper i en överlappning under samma uppsättning. Om du vill lägga till en annan användargrupp i unionen använder du en ny inkluderingsuppsättning.

+++

+++Exkludera elever

Välj de användargrupper och enskilda elever (med e-post-ID eller namn) som du vill utesluta. Lägg till alla användargrupper i en överlappning under samma uppsättning. Om du vill lägga till en annan användargrupp i en union använder du en ny inkluderingsuppsättning.

+++

## Mejl-ID för användare

+++Mejl-ID

Kopiera och klistra in e-post-id för elever som du vill registrera, separerade med semikolon, kommatecken eller radavstånd. Använd alternativet **[!UICONTROL Validate Email Ids]** för att validera posterna. Alla ogiltiga poster visas markerade med rött. Ta bort eller korrigera dessa poster och fortsätt genom att klicka på **[!UICONTROL Proceed.]**

![](assets/email-id-option.png)

*Registrera elever*

Dialogrutan Sammanfattning visas med antalet användare från inkluderingsuppsättningen, exkluderingsuppsättningen och användare som redan är registrerade i kursinstansen.

+++

### Lägg till kommentarer när du registrerar elever {#enroll-comments}

<!---![](assets/enroll-learners-dialog.png)-->

Som administratör eller chef kan du lägga till kommentarer när du registrerar elever för en kurs. Du kan nämna ytterligare information om kohorten av användare som registreras. Dessa data exporteras i kursrapporter.

Kommentaren visas **inte** för eleven.

När en administratör genererar elevens kursrapport visas eventuella kommentarer i rapporten. Dialogrutan Sammanfattning visas med antalet användare från inkluderingsuppsättningen, exkluderingsuppsättningen och användare som redan är registrerade i kursinstansen.

I dialogrutan **[!UICONTROL Enroll Learners]** expanderar du alternativet **[!UICONTROL Advanced Options]**. Ange den obligatoriska kommentaren i fältet **[!UICONTROL Additional Comment]**.

![](assets/comment-for-learner.png)

*Lägg till kommentarer för elever*

## Sök efter registrerade användare {#searchforusers}

Sök efter registrerade användare i utbildningsobjektets elevavsnitt med hjälp av typbaserad sökning. Med Type Ahead-sökning kan du progressivt söka efter registrerade användare med hjälp av namn, e-post-ID och uuid.

![](assets/typeahead.gif)

*Genomgång av sökning efter registrerade användare*

Den här typen av sökning kallas ibland även automatisk komplettering, inkrementell sökning, sökning allteftersom du skriver, textbunden sökning eller direktsökning.

När du skriver för en elev eller en användargrupp i sökfältet hittas en eller flera matchningar för söktermerna och visas direkt för dig.

Processen gör att du kan hitta vad du letar efter på ett mycket snabbare och mindre besvärligt sätt än att utföra ett antal sökningar i en rad.

Elever eller användargrupper visas i alla instanser efter en sökning. För varje elev visas instansen där eleven är registrerad i kolumnen **[!UICONTROL Instance]**.

![](assets/search-result.png)

*Visa sökresultat*

Med hjälp av funktionen för framförläsning kan du:

* Visa alla registrerade användare, oavsett instans.
* Visa alla användargrupper som har en eller flera registrerade användare.

När en sökning har utförts kan du inte filtrera elever efter instanser. Alternativet att välja en instans i listrutan **[!UICONTROL Select Instance]** är inaktiverat.

Med sökresultaten kan du dessutom välja en elev eller användargrupp och utföra följande åtgärder:

* Avregistrera
* Markera slutförande
* Återställ modul

När du utför en sökning är alternativet Avregistrera > Massutskick i listrutan Åtgärder inaktiverat för kurs-/utbildningsprogrammet.

## Dela QR-kod med elever som ska registreras, slutföras eller båda {#shareqrcodewithlearnerstoenrollcompleteorboth}

Administratörer i Adobe Learning Manager kan dela QR-koderna med elever för att snabbt registrera sig för kursen. De tre olika QR-koderna används för att markera &quot;registrering&quot;, &quot;slutförande&quot; eller &quot;registrering och slutförande&quot; för en kurs.

Elever kan helt enkelt skanna den aktuella QR-koden med Adobe Learning Manager-enhetsappen.

**Så här hämtar du QR-koden**:

1. Klicka på **[!UICONTROL Courses]** i avsnittet Utbildning på den vänstra navigeringspanelen.
1. Välj en kurs > **[!UICONTROL View course]**.
1. Klicka på **[!UICONTROL Instances]** > **[!UICONTROL More]** > **[!UICONTROL QR code]**.

   <!--![](assets/admin-instance-edit.png)-->

1. Aktivera QR-koden och klicka sedan på hämtningsikonerna Registrera, Slutför och Registrera och slutför för att hämta en PDF-fil som innehåller QR-koden för var och en. Administratören kan sedan dela QR-koden med elever.

   ![](assets/qr-code-download-01.png)

   *Dela QR-koden med elever*

## Hämta rapporten för intresserad elev

Visa [Registrera ett intresse för kurserna](/help/migrated/learners/feature-summary/courses.md#register-interest-for-the-courses) för att lära dig hur elever kan anmäla sitt intresse.

Administratörer kan visa elevens intresse och hämta rapporten Intresserad elev på sidan Kursöversikt.

Så här hämtar du rapporten för intresserad elev:

1. Logga in på Adobe Learning Manager som administratör.
2. Gå till **[!UICONTROL Courses]** och välj kursen.
3. Välj **[!UICONTROL Interested Learners]**.

   ![](assets/select-interested-learner.png)
   _Sidan Kursöversikt i administratörsgränssnittet visar avsnittet Intresserad elev för att visa och hämta rapporten_
4. Välj Åtgärder och välj sedan Exportera rapport.
Rapporten med listan över intresserade elever laddas ned. Rapporten innehåller följande kolumner:

   * Kurs-ID
   * Elevnamn
   * E-post
   * Typ
   * Status
   * Registreringsdatum och -tid (UTC)
   * Aktiv status

>[!NOTE]
>
>Rapporten inkluderar elevens UUID om den är aktiverad för kontot.

## Kursens livscykel {#courselifecycle}

Kursens livscykel ser normalt ut så här:

**Utkast** - när en författare har skapat en kurs och sparat den. I det här läget är kursen inte tillgänglig för elever ännu. Du kan radera en kurs i det här tillståndet.

**Publicerad** - när en författare har slutfört publiceringen av en kurs. I det här läget är kursen tillgänglig så att elever kan registrera sig.

**Utfasad** - Efter att ha publicerat en kurs kan en författare flytta den till ett utfasat tillstånd om han eller hon inte vill att kursen ska visas i kurskatalogen för elever. Du kan publicera om eller radera en kurs i det här tillståndet.

**Borttaget** - En kurs under borttaget tillstånd tas bort helt från Adobe Learning Manager-programmet. Kurser kan bara tas bort av författare när de har statusen utkast. Du kan också ta bort kurser från utfasat tillstånd.

![](assets/lifecycle-03.png)

*Arbetsflöde i en kurscykel*

## Meddelandeinställningar {#notificationsettings}

Som administratör kan du justera aviseringsinställningarna. Mer information finns i [Meddelanden.](user-notifications.md)

## Vanliga frågor {#frequentlyaskedquestions}

+++Hur återställer jag modulen som administratör?

Klicka på **[!UICONTROL Actions]** > **[!UICONTROL Reset Modules]** på sidan Elever för en kurs, välj eleven eller eleverna eller en grupp.

![](assets/reset-modules.png)

*Visningsalternativ för att återställa moduler*

När du har klickat på alternativet återställs status för moduler för alla valda elever. Modulerna som slutförs återställs inte.

+++

+++Hur lägger man till kurs-URL så att elever omdirigeras direkt till kursen?

För musen över ett kurskort och klicka på **[!UICONTROL Copy URL]**. När du har kopierat URL:en kan eleverna komma åt kursen direkt med URL:en.

+++

+++Hur öppnar man en instans på nytt?

Om du vill öppna en utfasad instans på nytt klickar du på listrutan i instansen och klickar på **[!UICONTROL Reopen instance]**.

+++
