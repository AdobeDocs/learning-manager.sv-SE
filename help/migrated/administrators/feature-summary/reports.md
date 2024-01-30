---
description: Läs mer om de rapporter som är kopplade till administratörsrollen i Learning Manager-programmet.
jcr-language: en_us
title: Rapporter
contentowner: manochan
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '6225'
ht-degree: 2%

---



# Rapporter

Läs mer om de rapporter som är kopplade till administratörsrollen i Learning Manager-programmet.

Med Adobe Learning Manager kan du skapa olika rapporter för att följa, övervaka och kontrollera elevaktiviteter. Elevaktiviteter spåras och hämtas automatiskt till databasen. Chefs- och administratörsrapporter genereras från databasen.

## Översikt {#overview}

Genereringsprocessen för rapporter är densamma för både Administratör och Chef. Chefer kan visa rapporter som motsvarar deras underordnade, medan administratörer kan visa alla rapporter som gäller för hela organisationen.

Rapporter sammanställs i en kontrollpanel. En rapport måste finnas inuti en kontrollpanel. A **[!UICONTROL Default Dashboard]** finns som standard på sidan Rapporter. Alla rapporter som läggs till av dig placeras på den här standardkontrollpanelen. Om du vill lägga till rapporter i enskilda kontrollpaneler använder du listrutepilen och väljer **[!UICONTROL Add Report]**. Mer information om hur du skapar kontrollpaneler finns i avsnittet Kontrollpaneler på den här sidan.

## Instrumentpaneler med utbildningssammanfattning {#dashboards}

Se en sammanfattande rapport över alla utbildningsaktiviteter i plattformen. På den här sidan visas följande sammanfattningsinformation för den valda rotanvändarens team och externa profiler. Du kan även välja Tidsintervall:

* Utbildningssammanfattning i form av registreringar, vyer och slutföranden
* Viktigaste kompetenserna
* Sammanfattning av efterlevnad

![](assets/summary-charts.png)
*Sammanfattningsdiagram*

Om det finns interna rotnivåhanterare visas de efter varandra.

Alla externa profiler visas efter interna profiler (interna rotnivåanvändare).

Om en extern profil har en chef visas chefshierarkin i **[!UICONTROL Showing Data For]** listruta. - Användaren kommer att listas i chefshierarkin på sidan med all information (utbildningssammanfattning, efterlevnad och kompetensstatus)

I annat fall visas alla enskilda användaruppgifter i listan.

Om du vill se mer detaljerad information om registreringar av olika interna team klickar du på **[!UICONTROL Learning Summary Details]**.

![](assets/learning-sunnarydetails.png)
*Sammanfattning av utbildning*

När du klickar på en registrering kan du se eleverna för varje chef och registrering till vilka utbildningsobjekt. Du kan också se förloppet och slutförandet för varje elev.

![](assets/learners-for-a-manager.png)
*AEE-elever som har tilldelats en chef*

Klicka på ett team och exportera dess rapport som en CSV. En administratör kan exportera rapporten för valfri användargrupp eller enskild användare genom att välja Användargruppen eller enskild användare och sedan exportera information från listrutan Åtgärd.

Du kan också se ett stapeldiagram över kompetenser som pågår och har uppnåtts. Du kan lägga till/ta bort kompetenser som du vill ha med i diagrammet.

![](assets/skill-status-stackedbarchart.png)
*Skivstatusstaplat stapeldiagram*

I den slutliga visualiseringen kan du kontrollera elevers efterlevnadsstatus och vidta lämpliga åtgärder.

Dessutom kan en administratör visa enskilda utbildningsdata på efterlevnadstavlan.

Administratören har till exempel identifierat tre utbildningar för att spåra efterlevnad. Learning Manager tillhandahåller ögonblicksbilden av kompatibilitet för alla tre utbildningarna samtidigt.

Nu kan en administratör klicka på valfri utbildning och snabbt se efterlevnad för den valda utbildningen.

![](assets/compliance-dashboard.png)
*Visa efterlevnadstavla*

Du kan också se efterlevnadsstatusen för varje internt team.

Klicka på länken **[!UICONTROL Compliance Status Details]** längst ned i visualiseringen.

Du kan se att antalet elever i teamet för ett team bryter mot eller följer utbildningsefterlevnaden.

![](assets/compliance-statusofateam.png)
*Efterlevnadsstatus för ett team*

## Dela utbildning med chefer

Learning Manager erbjuder efterlevnadstavla till alla administratörer och chefer. Chefer tycker att det är mycket användbart att följa hur deras teammedlemmar följer en viss utbildning. Samtidigt vill administratörer att alla chefer ska lägga till efterlevnadsutbildningar på sin kontrollpanel och spåra dem.

I Learning Manager **[!UICONTROL Share with Managers]** Med arbetsflödet kan administratörer dela utbildning med chefer så att de kan läggas till i en chefs efterlevnadstavla. Chefer behöver alltså inte vidta några åtgärder och kan börja spåra efterlevnad omedelbart.

En administratör kan dela en uppsättning utbildningskurser med chefer enskilt eller med en grupp. Denna delning kan hjälpa en chef att enkelt följa hur hans/hennes team följer den angivna utbildningen.

Administratören kan &quot;skicka&quot; en standardlista över efterlevnadsutbildning som ska visas på chefens efterlevnadstavla.

### Dela utbildning

1. in **[!UICONTROL Reports]** > **[!UICONTROL Learning Summary]**, bläddrar nedåt och klickar på fliken **[!UICONTROL Share with Managers]**.

   ![](assets/share-with-managers.png)
   *Dela utbildning med chefer*

1. Om du vill lägga till utbildning eller flera utbildningar klickar du på **[!UICONTROL Share more]**.

1. I dialogrutan **[!UICONTROL Share with Managers]** väljer du utbildningarna och cheferna.

   ![](assets/select-training.png)
   *Välj utbildning att dela med chefer*

1. Klicka på **[!UICONTROL Share]**.

Utbildningen delas nu med den angivna chefen.

### Visa utbildning

Klicka på i listan över delade utbildningar **[!UICONTROL View]**. Du kan se utbildningen som är tilldelad en chef eller vissa chefer.

### Dra in utbildning

1. Om du vill dra tillbaka utbildningen från en chef klickar du på **[!UICONTROL Withdraw]**.

1. Klicka på **[!UICONTROL Proceed]**. Detta drar tillbaka tidigare delad utbildning från chefens efterlevnadstavla.

## Kontrollpaneler för användaraktivitet {#useractivitydashboards}

Se en sammanfattning av all användaraktivitet på plattformen över tid. Konfigurera användargrupper och tillämpa filter.

Kontrollpanelen för användaraktivitet visar aktiviteten för användare på kontot. De tre rapporterna som visas är:

* **Registrerade användare:** Den här rapporten innehåller information om antalet användare som är registrerade på ditt konto varje vecka. För konton med licenser för månatliga aktiva enheter visas MAU-enheterna i stället i rapporten.

* **Rapport över användarbesök:** Den här rapporten innehåller information om antalet användare som dagligen använder plattformen. Månadsvis rapport finns också tillgänglig.

* **Rapport över använd utbildningstid:** Den här rapporten innehåller information om den utbildningstid som används i plattformen varje dag. Månadsvis rapport finns också tillgänglig.

## Registrerade användare {#registeredusers}

Learning Manager registrerar antalet användare som registreras i systemet varje vecka. Administratörer kan se den här rapporten för att få en uppfattning om det registrerade antalet användare den dagen i veckan. Det registrerade antalet ändras inte om det en gång förvarats under en vecka. Därför är historiskt registrerat antal inte relaterat till den aktuella uppsättningen elever i systemet.

Den här rapporten innehåller information om antalet användare som är registrerade på ditt konto varje vecka.

För konton med licenser för månatliga aktiva enheter visas MAU-enheterna i stället i rapporten.

![](assets/registered-usersreport.png)
*Rapport över registrerade användare*

***För månatliga Access-enhetskonton:***

**Månadsvis rapport över aktiva användare**

Den här rapporten visar antalet elever som är aktiva på utbildningsplattformen varje månad. Användaren anses vara aktiv under månaden om han/hon utför någon av de utbildningsåtgärder som nämns här. Det är samma sätt som Månadens aktiva enheter räknas.

Det månatliga aktiva antalet när det har räknats och lagrats i en månad ändras inte. Därför är det historiska antal som visas inte relaterat till den aktuella uppsättningen elever i systemet.

## Användarbesök {#uservisits}

Den här rapporten visar det totala antalet elever som har tillgång till systemet under en dag- eller månadsperiod. Att bläddra på utbildningsplattformen utan att använda något lärande anses också som att &quot;komma åt&quot; utbildningsplattformen. Detta hjälper administratören att förstå den totala mängden användare som har åtkomst till systemet. Den första månaden skapar Learning Manager en post med det totala antalet användare som har tillgång till plattformen under föregående månad. Det registrerar även användargruppsinformation för dessa användare.

Endast de användargrupper som konfigurerats av administratören registreras. Detta gör att administratörerna kan tillämpa filter på användargrupper även för historiska månadsdata. Observera att om konfigurationen av användargrupper ändras och Learning Manager inte har registrerat data för denna användargrupp under tidigare månader kan inte Learning Manager visa data för dessa nykonfigurerade användargrupper under de föregående månaderna.

Den här rapporten innehåller användare som använder plattformen med alla format som webben, mobilappen, fjärradministrerade anpassade lösningar och så vidare. Användningsdiagrammet för enhetsappen anger endast de användare som använder plattformen med Learning Managers enhetsapp. Detta hjälper administratörer att identifiera användningen av mobilappen i sina konton.

![](assets/user-visit-report.png)
*Besöksrapport för användare*

## Rapport över använd utbildningstid {#learningtimespentreport}

Här visas ett linjediagram med två axlar som visar den totala inlärningstiden för alla elever under en 12-månadersperiod. Den andra axeln representerar mediantid för att lära sig för en individ.

Tiden för olika utbildningsobjekt, till exempel utbildningsprogram och certifieringar, beräknas för följande:

* Kurs i egen takt med statiskt och interaktivt innehåll
* Aktivitetskurser med URL.
* Helgsessioner med helgflaggan aktiverad.
* VC-anslutningssession där närvaro markeras automatiskt.
* Den tid som ägnas åt olika utbildningsobjekt, till exempel utbildningsprogram och certifieringar
* xAPI-satser för en xAPI-aktivitetskurs.

Du kan exportera diagrammet som ett Excel-kalkylblad ytterligare.

Det finns ett filter för att välja konfiguration av användargrupp, vilket underlättar visning av data med avseende på olika användargrupper.

Det valda filtret för datum och användargrupp används i alla relevanta diagram på kontrollpanelen.

>[!NOTE]
>
>För **[!UICONTROL User Visits]** och **[!UICONTROL Learning Time Spent]** rapporter kommer standarddata (när ingen användargrupp har konfigurerats) som visas att gälla för hela kontot.

## Instrumentpanel för utbildningsinnehåll {#trainingcontentdashboard}

På instrumentpanelen för utbildningsinnehåll finns insikter om utbildningar som är tillgängliga på plattformen. Du kan visa populära utbildningar eller spåra alla tillgängliga utbildningar.

## Utbildningsrapport {#trainingsreport}

Den här rapporten innehåller information om det totala antalet utbildningar som är tillgängliga på plattformen (i publicerat skick) per månad under månad. Det ger en antydan om antalet utbildningar som erbjuds över tiden.

![](assets/training-report.png)
*Utbildningsrapport*

## Aktiv utbildningsrapport {#activetrainingsreport}

Den här rapporten innehåller information om utbildningarna som är aktiva inom det valda tidsintervallet. Aktiva utbildningar är utbildningar som registreras, visas i spelare eller slutförs inom angiven tid.

För aktiva utbildningar kommer data för alla rotanvändargrupper (med chefsroll) att vara tillgängliga för urval när ingen konfiguration av användargrupper är klar. Förutom rotanvändargrupperna kan du konfigurera ytterligare 10 användargrupper om det behövs.

![](assets/active-trainingsreport.png)
*Rapport över aktiva utbildningar*

>[!NOTE]
>
>Data visas inte som förväntat när **[!UICONTROL All Users]** och **[!UICONTROL 12 months]** filter har valts, men data visas när du väljer **[!UICONTROL All internal user group].**

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Referens</b></p></td>
   <td>
    <p><b>Metrisk</b></p></td>
   <td>
    <p><b>Beskrivning</b></p></td>
  </tr>
  <tr>
   <td>
    <p>1</p></td>
   <td>
    <p>Startförhållande (%)</p></td>
   <td>
    <p>Förhållandet mellan antalet elever som har startat kursen och antalet registreringar.</p></td>
  </tr>
  <tr>
   <td>
    <p>2</p></td>
   <td>
    <p>Andel slutfört (%)</p></td>
   <td>
    <p>Förhållandet mellan det totala antalet användare som har slutfört kursen och det totala antalet användare som har startat kursen.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>3</p></td>
   <td>
    <p>Feedback från elev</p></td>
   <td>
    <p>Genomsnitt av alla L1-feedbacksvar som mottagits på en skala från 1 till 10 avrundat till närmaste heltal.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>4</p></td>
   <td>
    <p>Feedback från chef</p></td>
   <td>
    <p>Genomsnitt av alla L3-svar som mottagits på en skala från 1 till 5 avrundat till närmaste heltal<br></p></td>
  </tr>
 </tbody>
</table>

Utbildningsrapporten har ytterligare två kolumner:

1. Genomsnittlig stjärnrankning för en kurs.
1. Antal elever som har betygsatt kursen.
1. Inbäddad väg
1. Inbäddat väg-ID
1. Inbäddat kurs-ID

>[!NOTE]
>
>Startkvot, slutförandegrad, elevfeedback och chefsfeedback påverkas inte av de filter som tillämpas. Filtren påverkar endast registrering, visningar och slutföranden.

>[!NOTE]
>
>För båda rapporterna (Utbildningsinnehåll, Användaraktivitet) kan du konfigurera högst 10 användargrupper. Det kan ta upp till 24 timmar för bearbetningen att slutföras och göra de nyligen konfigurerade filtren tillgängliga.

## Tavelrapporter {#dashboardreports}

En kontrollpanel är en samling rapporter. Rapporter kan grupperas i en kontrollpanel enligt ditt val.

## Exempelrapporter {#samplereports}

Inställningen **[!UICONTROL Sample Reports]** för att visa några indikativa rapporter som baseras på exempeldatapunkter. Utforska dessa rapporter och få en uppfattning om olika typer av funktionsrika rapporter som du kan generera med hjälp av dina kontodata.

## Tavelrapporter {#DashboardReports-1}

Klicka på fliken Tavla för att se alla tavlor som du har skapat. Från **[!UICONTROL View Dashboard]** I listrutan kan du välja standardtavlan eller en kontrollpanel som du har skapat.

## Skapa en kontrollpanel {#createadashboard}

1. Om du vill börja skapa egna tavlor klickar du på Lägg till tavla till höger på sidan.

   ![](assets/add-dashboards.png)
   *Lägga till kontrollpaneler*

1. Ange namn och beskrivning för instrumentpanelen.
1. Om du vill dela kontrollpanelen med en chef väljer du dem i **[!UICONTROL Share With]** område. Du kan använda valfria normala urvalskriterier för den här åtgärden.
1. Klicka **[!UICONTROL Save].**

Du kan visa den nyligen skapade tavlan i **[!UICONTROL Dashboard Reports]** -fliken.

Om du vill lägga till rapporter på tavlan klickar du på listrutan i det övre högra hörnet av tavlan och klickar på **[!UICONTROL Add Report]**. Den rapport du skapar på det här sättet är kopplad till din kontrollpanel.

>[!NOTE]
>
>Rapporterna som du skapar genom att klicka på Lägg till längst upp till höger på sidan Rapporter läggs till i standardkontrollpanelen.

## Delade instrumentpaneler {#shareddashboards}

Delade tavlor är en samling rapporter som har delats med dig av andra användare i organisationen. Alla rapporter som du lägger till på en delad tavla delas automatiskt med andra användare som har åtkomst till den tavlan.

Du kan dela tavlan på följande två sätt:

* Genom att ange användare i **[!UICONTROL Share With]** fält som instrumentpanelen delas med.
* Välj Redigera tavla i listrutan och ange användarinformation för att dela tavlan.

>[!NOTE]
>
>En chef kan bara visa rapporter om sina teammedlemmar från en delad kontrollpanel.

## Nedladdningar {#downloads}

Det exporterade kalkylbladet med kontrollpanelsrapporter innehåller detaljerad information i stället för rapportsammanfattning. Den nedladdade rapporten följer formatet för elevens betygsutdrag.

## Skapa rapporter {#report}

1. Klicka på Rapporter i den vänstra rutan. Sidan Rapportsammanfattning visas.

   >[!NOTE]
   >
   >Som standard visas minst tre exempelrapporter på fliken Exempeltavla. Du kan bara visa exempelrapporter för att få en uppfattning om hur du kan skapa och anpassa dem.

1. I det övre högra hörnet på sidan klickar du på **[!UICONTROL Add]**.
1. I dialogrutan **[!UICONTROL Add Report]** i listrutan Typ kan du välja antingen en av de fördefinierade rapporterna eller så kan du välja **[!UICONTROL Custom]**. Om du väljer en fördefinierad rapport ser du att formuläret är förifyllt. Du kan göra ytterligare ändringar i vissa av fälten och klicka på **[!UICONTROL Save]**. Rapporten läggs då till i din standardtavla.

   ![](assets/create-report.png)
   *Skapa rapport*

   in **[!UICONTROL Report Type]** kan du välja en fördefinierad uppsättning med rapporter eller anpassade värden. Du kan visa följande rapporter som en del av en fördefinierad uppsättning rapporter:

   * Kompetenser som tilldelats och uppnåtts
   * Kurs registrerad och slutförd
   * Kursernas effektivitet
   * Registrerade och slutförda utbildningsprogram
   * Använd utbildningstid per kurs
   * Använd utbildningstid per kvartal
   * Slutförande av certifiering

1. Välj **[!UICONTROL Y-axis]** för din rapport från rullgardinsmenyn. För vissa av de valda kriterierna kan du välja ett eller flera lägen från lägesalternativen. Till exempel för ett primärt kriterium för kursregistreringsstatistik kan tillstånden vara slutförda, ofullständiga och registrerade. Primära intervalldata visas i form av stolpdiagram i rapporten.

   ![](assets/axes-for-reports.png)
   *Axlar för rapporter*

1. Välj det sekundära **[!UICONTROL Y-axis]** kriterier/intervall för rapporten i listrutealternativen. Om du till exempel har ett registreringsalternativ för utbildningsprogram väljer du ett eller flera tillstånd i listrutan Tillstånd. Sekundära områdesdata representeras i form av linjediagram.
1. Markera X**-axel**-kriterierna för rapporten i listrutan. Om x-axeln väljs som datum, finns det ett alternativ för att gruppera x-axelkriteriet efter dag, månad, kvartal och år.
1. Välj önskat alternativ i listrutan i avsnittet Tidsrymd. Du kan välja bland följande alternativ:

   * Senaste månaden
   * Kvartal
   * År
   * QTD (senaste 90 dagarna)
   * YTD (senaste 365 dagarna)
   * Datumintervall. Ange värden i **[!UICONTROL From]** och **[!UICONTROL To]** datumfält.

   ![](assets/time-filter-for-report.png)

1. **Avsnittet Filter**

   Filter visas längst ned i dialogrutan Lägg till rapport baserat på de typer av rapporter som du har valt. Några av de mer framträdande filtren nämns nedan.

   * **Chef:** Du kan välja en av hanterarna baserat på hierarki. För vissa chefer kan det finnas underordnade chefer och flera anställda som rapporterar till varje underordnad chef.
   * **Profil:** Välj din medarbetares beteckning. Det skulle vara till hjälp för att visa rapporter om anställda baserat på deras profil/beteckning. Till exempel datavetare, ingenjör.
   * **Användargrupp:** Välj den användargrupp som du vill filtrera rapporterna från. Learning Manager hämtar användargrupperna som definierats för ditt konto från funktionen Användare.
   * **Innehåll:** Du kan filtrera din rapport baserat på valfri kurs genom att välja dem i listrutan.

   Expandera det här avsnittet och välj de filter som behövs.

   ![](assets/choose-filters.png)
   *Välj filter*

1. Klicka **[!UICONTROL Save]** för att slutföra rapporten.

   ![](assets/sample-report.png)
   *Exempelrapport*

## Redigera en rapport {#editareport}

I rapporten klickar du på pilen och väljer alternativet **[!UICONTROL Edit Report]**.

![](assets/edit-a-report-1.png)
*Redigera en rapport*

Gör de ändringar som krävs i rapporten. Klicka på för att spara ändringarna **[!UICONTROL Save]**.

## Flytta en rapport till en kontrollpanel {#moveareporttoadashboard}

Välj det här alternativet om du vill flytta den aktuella rapporten till en befintlig kontrollpanel. Om du vill flytta rapporten klickar du på alternativet **[!UICONTROL Move to Dashboard]**.

![](assets/move-a-report.png)
*Flytta en rapport till en kontrollpanel*

Välj tavlan dit du vill att rapporten ska flyttas och klicka på **[!UICONTROL Move]**.

## Skapa en kopia av en rapport {#createacopyofareport}

Om du vill skapa en kopia av rapporten väljer du alternativet **[!UICONTROL Create a Copy]**.

![](assets/copy-a-report.png)
*Skapa en kopia av en rapport*

Välj tavlan dit du vill kopiera rapporten. Börja kopiera genom att klicka på **[!UICONTROL Copy]**.

## Ta bort en rapport {#deleteareport}

Välj alternativet om du vill ta bort en rapport **[!UICONTROL Delete Report]**. När du har tagit bort rapporten kan du inte återställa den. Processen är oåterkallelig. Var försiktig när du tar bort en rapport.

![](assets/delete-a-report.png)
*Ta bort en rapport*

## Hämta en rapport {#downloadareport}

Välj alternativet om du vill hämta rapporten **[!UICONTROL Download Report]**.

![](assets/download-a-report.png)
*Hämta en rapport*

## Ändra storlek på en rapport {#resizeareport}

Du kan ändra storlek på dina rapporter i storlekarna 1×1 (medel) och 1×2 (stor). Detta ger dig en bättre fastighet att visa dina rapporter. Du kan också enkelt panorera och zooma i dessa rapporter.

## Filter {#filters}

Filter visas i **[!UICONTROL Add]** Rapportera längst ned baserat på de typer av rapporter som du har valt. Några av de mer framträdande filtren nämns nedan.

**Chef** Du kan välja en av hanterarna baserat på hierarki. För vissa chefer kan det finnas underordnade chefer och flera anställda som rapporterar till varje underordnad chef.

**Profil** Välj din medarbetares beteckning. Det skulle vara till hjälp för att visa rapporter om anställda baserat på deras profil/beteckning. Till exempel datavetare, ingenjör.

**Användargrupp** Välj den användargrupp som du vill filtrera rapporterna från. Learning Manager hämtar användargrupperna som definierats för ditt konto från funktionen Användare.

**Kurs** Du kan filtrera din rapport baserat på valfri kurs genom att välja dem i listrutan.

![](assets/sample-report-admin.png)
*Filtrera en rapport*

Ovanför teckenförklaringen kan du visa en zoomningsruta. För markören över det, klicka och dra tvärsnittet över någon del av diagramområdet i zoomningsrutan för att zooma in.

Du kan visa de sekundära y-axelvärdena i form av en linje tvärs över diagramstaplarna. I exemplet ovan kan du till exempel se värdena för effektivitet i grå linje tvärs över diagrammet.

## Rapporter om användargrupper {#user-group-reporting}

Spåra hur användargrupper som avdelningar, externa partner och roller presterar i jämförelse med andra användargrupper eller mot andra utbildningsmål.

### Användargrupper {#usergroups}

Om du vill skapa rapporter baserade på användargrupper väljer du **[!UICONTROL User Group]** i x-axeln från listan med rullgardinsalternativ som visas i skärmbilden nedan.

![](assets/user-group-reports.png)
*Rapporter om användargrupper*

Om du vill välja en användargrupp skriver du namnet på gruppen. Du kan se de föreslagna grupperna som visas enligt den sträng du anger. När du ser en lista över grupper väljer du önskad användargrupp.

Du kan också välja flera användargrupper med hjälp av typsnittssökning.

Om du har valt flera användargrupper när du har sparat och genererat den här rapporten, genereras rapporten med alla användargrupper som visas i stapeldiagrammet bredvid varandra längs x-axeln.

Med den här rapporten över användargrupper kan du jämföra prestanda hos en avdelning/roll med den andra för att utvärdera deras utbildningsresultat.

### Anpassade användargrupper/användarattribut {#customusergroupsuserattributes}

Du kan också skapa anpassade användargrupper med funktionen Lägg till användare/användargrupper i Learning Manager. När du har skapat användargrupperna kan du skapa rapporter för dessa anpassade användargrupper med hjälp av en lista med attribut som plats, gren.

Välj alternativet för användarattribut i x-axeln och välj attributet på menyn **markera** bredvid den. Om du vill skapa en anpassad användargruppsrapport baserad på dessa attribut måste du också välja lämplig användargrupp i filtret.

## Typer av rapporter {#typesofreports}

Adobe Learning Manager stöder fyra huvudtyper av rapporter såsom slutförande, tidsåtgång, färdigheter och effektivitet. Du kan använda följande rapporttyper för att generera rapporter om fler än 300 varianter:

* Statistik för kursleverans för elever
* Effektivitetsrapport för kurser
* Rapport över elevens kompetens
* Statistik för registrering i utbildningsprogram för elever
* Utbildningstid som elever lagt ner
* Antal elever
* Slutförande av certifiering

## Visa rapporter {#viewingreports}

På sidan Rapporter kan du visa alla rapporter. Du kan minimera varje rapport genom att klicka på minusikonen (-) längst upp till höger i varje rapport. Klicka på ikonen (+) för att visa din rapport igen.

## Snabbvy med olika datum {#quickviewwithdifferentdates}

Du kan ändra datumintervallet/värdet för en rapport och visa snabbt för ett annat datum utan att ändra och spara rapporten. Klicka på redigeringsikonen (som visas med en pil i ögonblicksbilden nedan) bredvid datumintervallet, t.ex. QTD, sista året. Bekräfta ändringen genom att välja det nya värdet på snabbmenyn och klicka på bockmarkeringen. Du kan avbryta ändringen genom att klicka på X-markeringen.

>[!NOTE]
>
>Datumvärdena som du använder för att visa rapporten är tillfälliga. Den här vyn av rapporten hämtas inte när du väljer hämtningsalternativet. Den här vyn är bara tillfällig vy.

![](assets/learner-count-report.png)
*Visa antal elever*

## Snabbvy med olika chefer {#quickviewwithdifferentmanagers}

Om det finns flera chefer som rapporterar till dig kan du visa rapporterna snabbt för varje chef. Om du vill visa unika rapporter för varje chef väljer du namnet på chefen i listrutan.

>[!NOTE]
>
>De chefsvärden som du använder för att visa rapporten är tillfälliga. Den här vyn av rapporten hämtas inte när du väljer hämtningsalternativet. Den här vyn är bara tillfällig vy.

## Visa kursrapporter {#viewcoursereports}

Du kan visa rapporterna för varje kurs genom att följa stegen nedan:

1. Klicka **[!UICONTROL View course reports]** på fliken Mina kontrollpaneler på sidan Rapporter.\
   En popup-dialogruta visas. Ett textinmatningsfält visas där du kan ange önskad kurs och föreslagna kursnamn visas i listrutan. Välj kursen från listan som visas.

   ![](assets/view-course-report-300x117.png)

   *Visa kursrapporter*

1. Välj en valfri kurs i listrutan och klicka på Visa.
1. Du dirigeras till sidan quiz-poängresultat för den valda kursen för att visa den kursspecifika rapporten.

**Redigera/Flytta till tavla/Skapa en kopia/Ta bort/Ändra storlek på rapport**

Om du vill visa listrutealternativ som Redigera/Flytta till kontrollpanel/Skapa en kopia/Ta bort/Ändra storlek klickar du på rullgardinspilen längst upp till höger i varje rapport.

![](assets/edit-options-dashboard-300x126.png)

*Redigera/Flytta till tavla/Skapa en kopia/Ta bort/Ändra storlek på rapporter*

**[!UICONTROL Edit]** Om du vill gå tillbaka till de ursprungliga värdena när du ändrar data klickar du på Återställ. Klicka på Spara när du har ändrat värdena.

**[!UICONTROL Move to Dashboard]** Du kan flytta den aktuella rapporten till en annan kontrollpanel som väljs i listan över kontrollpaneler.

**[!UICONTROL Create a Copy]** Du kan kopiera rapporten till samma eller en annan kontrollpanel, som väljs i listan över kontrollpaneler.

**[!UICONTROL Delete]** Klicka på Ta bort för att ta bort rapporten. Ett varningsmeddelande/bekräftelsemeddelande visas innan du kan ta bort rapporten.

**[!UICONTROL Resize]** Du kan ändra storlek på dina rapporter i storlekarna 1×1 (medel) och 2×2 (stor).

## Generera och visa rapporter för kollegialt konto {#generateandviewreportsforpeeraccount}

Som administratör kan du, förutom att skapa rapporter för ditt konto, även generera och visa rapporter för kollegiala konton som du har angett.

När du har upprättat ett kollegialt konto hos en annan användare kan du visa rapporterna för det kollegiala kontot från **[!UICONTROL Reports]** sidan. När du skapar en rapport visas **[!UICONTROL Select Account]** område. I listrutan som listar alla kollegiala konton som du är associerad med väljer du det konto som du vill visa de delade rapporterna för.

När du skapar ett kollegialt konto och alternativet Dela katalog inte har valts kan du inte visa det kollegiala kontot i den här listan.

![](assets/acc1-jpg.png)
*Hantera rapporter för kollegialt konto*

1. Markera x- och y-axlarna för den här rapporten och ange datumet för rapporten.
1. Observera att knappen Delade kataloger är automatiskt aktiverad i filterfältet. Det är obligatoriskt. Om Delad katalog inte är aktiverad innebär det att du inte kan generera eller visa rapporter för det kollegiala kontot.
1. I listrutan nedan Delad katalog väljer du den delade katalog som du vill visa rapporten för.
1. Klicka [!UICONTROL **Spara**].

   ![](assets/acc2.png)
   *Välj Delad katalog för kollegialt konto*

1. När du har klickat **[!UICONTROL Save]**, du kan visa den grafiska representationen av dina rapporter på standardkontrollpanelen. Från den här instrumentpanelen kan du filtrera rapporten ytterligare av chefen för det specifika kollegiala kontot.
1. Om det sker några ändringar i katalogen från din sida återspeglas ändringarna omedelbart i de rapporter och tavlor som genereras av kollegiet. Men när kollegan ändrar katalogen visas inte ändringarna automatiskt på instrumentpanelen.
1. Om du vill att instrumentpanelen ska uppdateras automatiskt måste din kollega skicka en ny kollegial begäran till dig.

   >[!NOTE]
   >
   >Chefer kan inte visa kollegiala rapporter.

## E-postprenumerationer {#emailsubscriptions}

Du kan få dina favoritrapporter via e-post genom att prenumerera på dem.

in **[!UICONTROL Reports]** klickar du på  **[!UICONTROL Subscription]** -fliken. Sidan Rapportprenumeration visas.

Du väljer rapportnamnet i listrutan genom att börja skriva rapportnamnet i fältet Rapporter. Välj hur ofta du vill skicka e-post i listrutan. Du kan lägga till e-postmeddelandets ämne och ange ett alternativt e-post-ID.

Du kan redigera och radera prenumerationer.

## Excel-rapporter {#excelreports}

Inställningen **[!UICONTROL Excel Reports]** på fliken kan du exportera rapporter i XLS-filformat.

Nedan visas de rapporttyper som är tillgängliga för hämtning.

* Kursrapporter
* Elevens betygsutdrag
* Notisrapport
* Arbetsstödsrapport
* Verifieringskedja för innehåll
* Verifieringskedja för användare
* Rapport över inloggning/åtkomst
* Spelifieringsutdrag

## Elevens betygsutdrag {#learnertranscripts}

Elevens betygsutdrag i Excel-rapporter visar kolumnerna Obligatoriska krediter och intjänade poäng i decimaltal.

## Kursrapporter {#coursereports}

Du som är administratör kan hämta rapporter för kurser. Gör så här:

1. Öppna **[!UICONTROL Reports]** > **[!UICONTROL Excel Reports]** > **[!UICONTROL Course Reports]**.
1. Inställningen **[!UICONTROL Course Report]** visas. Välj kursen som du vill hämta rapporten för och klicka på **[!UICONTROL Show]**.

   ![](assets/course-reports.png)
   *Kursrapporter*

1. Du omdirigeras till kurssidan. Du kan exportera quiz-poäng per användare och per fråga baserat på varje registrering genom att välja den specifika registreringstypen.
1. Välj **[!UICONTROL Export Quiz Score]** för att exportera rapporten. A **[!UICONTROL Generating Report Request]** visas. Klicka **[!UICONTROL OK]** för att bekräfta.

   ![](assets/generating-reportrequest.png)
   *Genererar rapportförfrågan*

   >[!NOTE]
   >
   >Den exporterade quiz-poängrapporten innehåller poänginformationen för varje försök om alternativet Flera försök är konfigurerat för modulen.

## Elevens betygsutdrag {#LearnerTranscripts-1}

Med Adobe Learning Manager kan administratörer i en organisation generera utskrifter som är kopplade till elever. Elevens betygsrapport innehåller följande:

1. Elevens betygsutdrag: instrumentpanel för utbildningsaktivitet
1. Kompetens: instrumentpanel för kompetens
1. Efterlevnadstavla

Elevens betygsutdrag i Excel-rapporter visar kolumnerna Obligatoriska krediter och intjänade poäng i decimaltal.

Mer information om hur du genererar rapporter om elevens betygsutdrag finns i [Elevens betygsutdrag](learner-transcripts.md).

## Meddelanderapporter {#announcementsreports}

Administratörer kan skapa rapporter över alla meddelanden som skickas. Rapporten innehåller information om:

* Meddelandetyp
* Meddelandenamn
* Meddelandedatum
* Tillstånd för tillkännagivandet
* Elevnamn

Gör något av följande för att hämta en rapport:

1. Öppna **[!UICONTROL Reports]** > **[!UICONTROL Excel Reports]** > **[!UICONTROL Announcements Report]**. Inställningen **[!UICONTROL Generating Report Request]** dialogrutan öppnas. Klicka på OK.
1. [!UICONTROL **Meddelanden**] > [!UICONTROL **Åtgärder**] > [!UICONTROL **Exportera rapport**].

   ![](assets/announcements.png)
   *Meddelanderapport*

1. Du kan extrahera en rapport för ett specifikt meddelande genom att klicka på Exportera rapport under ikonen för inställningar.

   ![](assets/announcements-specific-report.png)
   *Rapport för specifika meddelanden*

## Arbetsstödsrapport {#jobaidsreport}

Arbetsstöd är utbildningsinnehåll som en elev kan komma åt utan att behöva registrera sig för ett specifikt utbildningsobjekt som en kurs eller ett utbildningsprogram. Administratörer kan extrahera och ladda ner Job Aids-rapporten.

Den extraherade rapporten innehåller information om följande:

* Namn
* Typ av arbetsstöd
* Status för arbetsstöd (offentliggjort eller återkallat)
* Registreringsdatum
* Datum för slutförande
* Nedladdningsdatum
* Elevnamn
* Chefens namn
* Skapad av

Gör något av följande för att hämta en rapport:

* Öppna  **[!UICONTROL Reports]** > **[!UICONTROL Excel Reports]** > **[!UICONTROL Job Aid Reports]**. Inställningen **[!UICONTROL Generating Report Request]** visas. Klicka på **[!UICONTROL Ok]**.
* Öppna **[!UICONTROL Job Aid]** > **[!UICONTROL Actions]** > **[!UICONTROL Export Report]**.

![](assets/job-aids.png)
*Arbetsstödsrapport*

* Du kan även extrahera en rapport för ett specifikt arbetsstöd genom att klicka på **[!UICONTROL Export Report]** under ikonen för inställningar.

![](assets/job-aid-specific-download.png)
*Rapport om specifikt arbetsstöd*

### Arbetsstödsrapport

När du har valt **[!UICONTROL Job Aids Report]** I listan visas två alternativ:

![rapport om arbetsstöd](assets/job-aids-new.png)
*Ladda ned rapport om arbetsstöd för användarregistrering*

**Alla arbetsstöd**: Om antalet arbetsstöd i kontot är färre än 10 miljoner, kommer den genererade rapporten att innehålla registreringsinformation för alla arbetsstöd. Detta är standardvalet. Om antalet rader överstiger 10 miljoner visas ett fel och du måste välja de nödvändiga arbetsstöden manuellt.

**Utvalda arbetsstöd**: Om du väljer det här alternativet kan du ange de arbetsstöd som du vill generera rapporten för. Du kan välja högst tio arbetsstöd. Adobe Learning Manager kontrollerar om antalet arbetsstöd överstiger 10 miljoner.

![registrera dig för arbetsstödsrapport](assets/job-aids-2-new.png)
*Välj arbetsstöd*

**Arbetsstödsrapport**

Om du väljer det här alternativet hämtas information om alla arbetsstöd i systemet tillsammans med metadata och utbildning.

Den hämtade rapporten består av följande fält:

* Arbetsstödsnamn
* Språk
* ID
* Typ
* Varaktighet (minuter)
* Status
* Datum för publicering (tidszonen UTC)
* Skapad per namn
* Skapad per mejl
* Skapat av unikt användar-ID
* Katalog(er)
* Utbildningsväg(ar)
* Kurs(er)
* Tagg(ar)
* Kompetens(er)

**Registreringsrapport för arbetsstöd**

Registreringsrapporten innehåller information om användarregistrering och annan information.

Den hämtade rapporten består av följande fält:

* Arbetsstödsnamn
* Typ
* Status
* Datum registrerad (tidszonen UTC)
* Datum för slutförande (tidszonen UTC)
* Nedladdningsdatum (tidszonen UTC)
* Elevnamn
* E-post
* Unikt användar-ID
* Chefens namn
* Mejladress till chef
* Unikt användar-ID för chef
* Tilldelad efter namn
* Tilldelad per e-post
* Tilldelat av unikt användar-ID
* Skapad per namn
* Skapad per e-post
* Skapat av unikt användar-ID
* Jobbkod
* Nytt fält
* Profil

### Verifieringskedjan för innehåll {#contentaudittrailreports}

Använd kommandot **[!UICONTROL Content Audit Trail]** rapportgenerator för att generera en rapport över alla ändringar och redigeringar av en kurs under dess livslängd i systemet. Följande information hämtades i den genererade rapporten.

* Objekt-id
* Objektnamn
* Objekttyp
* Ändringstyp
* Beskrivning
* Refererat objekt-ID
* Refererat objektnamn
* Ändrat per användarnamn
* Ändrad av användar-ID
* Ändringsdatum (tidszonen UTC)

Information om metadata hämtas inte i den genererade rapporten.

Följ de här stegen för att generera en granskningsrapport för kursspår.

1. Välj **[!UICONTROL Report]** > **[!UICONTROL Excel reports]** > **[!UICONTROL Course Audit Trail]**. Inställningen **[!UICONTROL Content Audit Trail]** visas.

   ![](assets/course-audit-trial.png)
   *Verifieringskedja för kurs*

1. Välj kursen, utbildningsprogrammet och certifieringen som du vill hämta rapporten för. Om det inte anges hämtas alla rapporter som standard.
1. Välj ett datumintervall för rapporten och klicka på **[!UICONTROL Generate]**.
1. Rapporten skapas och du meddelas att innehållsgranskningsrapporten är klar. Du kan hämta rapporten.

## Verifieringskedjan för användare {#useraudittrailreports}

Verifieringskedjan för användare visar livscykeln för användare, användargrupper och självregistreringsprofiler. Tillägg av användare, borttagning, ändring i chef, registreras. Skapande och radering av självregistreringsprofiler registreras. Du kan även pausa och återuppta självregistreringen.

Du kan lägga till, aktivera, inaktivera, pausa och återuppta för externa profiler medan du kan lägga till, ta bort, pausa och återuppta för egenregistrering. CSV-uppladdningar hämtas också.

1. Välj  **[!UICONTROL Report > Excel report > User Trail]**. Dialogrutan Verifieringskedja för användare visas.
1. Dialogrutan Verifieringskedja för användare visas. Välj datumintervallet på snabbmenyn. Du kan antingen välja att generera rapport för den senaste veckan, den senaste månaden eller välja anpassat datum.

   ![](assets/user-audit-trail.png)
   *Verifieringskedja för användare*

1. Klicka **[!UICONTROL Generate]** för att generera rapporten.

Det finns två filter på **[!UICONTROL User Audit Trail Report]** dialog.

**Filter för datumintervall:** Välj det datumintervall som du vill generera rapporten för. Det finns tre alternativ:

* Senaste veckan
* Senaste månaden
* Anpassat datum

Välj elevfilter: Sök efter en användare eller användargrupp.

Den exporterade rapporten innehåller data för de användare som uppfyller båda de angivna sökkriterierna.

![](assets/user-audit-trail.png)
*Verifieringskedja för användare*

>[!NOTE]
>
>När en kompetens tilldelas eller tas bort kan kompetensen spåras för användargranskningsrapporten för både tilldelade och borttagna.

## Spelifieringsrapporter {#gamification}

Administratörer kan hämta transkribering av spelifiering i CSV-format. Du kan antingen hämta rapporten för enskilda användare eller användargrupper. Användarnamn, användarens e-postadress, användarens UUID, det totala antalet gjorda användarpoäng, uppdelning av insamlade poäng, namnet på de grupper som användaren spelar i, namnet på chefen och aktiva fältvärden hämtas i rapporten. Administratörer kan använda den här rapporten för att utvärdera och förstå användarrankningar på organisationsnivå eller för en viss grupp.

1. Välj Rapport > Excel-rapport > Spelifieringsrapport.

   ![](assets/gamification.png)
   *Spelifieringsrapport*

1. Dialogrutan Transkribering av spelifiering visas. Välj elever genom att använda deras namn, profil, användargrupper, e-post-ID eller UUID.

   ![](assets/gamification-transcriptsdialog.png)
   *Dialogrutan Transkribering av spelifiering*

1. Klicka  **[!UICONTROL Generate]** för att generera rapporten.

   När du har genererat rapporten för en elev måste du kunna exportera aktuell och uppnådd information för alla användare (interna, externa eller borttagna) på kontot. Du kan också kontrollera datumen för de nivåer som en elev uppnått:

   * Brons har uppnåtts datum
   * Silver har uppnåtts datum
   * Guld har uppnåtts datum
   * Platina har uppnåtts datum

   Dessa kolumner innehåller de datum då nivån uppnåddes för första gången. Kolumnen **[!UICONTROL Current Level]** visar elevens aktuella nivå.

   När administratören återställer spelifieringen återställs alla poäng för eleven därefter.

## Rapport över registrering och avregistrering {#enrollmentandunenrollmentreport}

Administratörer och chefer kan extrahera en rapport över elever som har registrerats och avregistrerats. Som administratör kan du se någon av eleven, administratören eller chefen som har registrerats eller avregistrerats från en instans av en kurs, ett utbildningsprogram eller en certifiering och exportera rapporten. Medan du som är chef kan du bara hämta en rapport om dina teammedlemmar. Som chef kan du inte se raderade elever eller ditt namn i chefsappen som en registrerad eller oregistrerad elev.

Hämta en rapport genom att följa dessa steg: Öppna  **[!UICONTROL Course/ Learning program/ Certification]** > **[!UICONTROL Learners]** > **[!UICONTROL Action]** > **[!UICONTROL Export report]**.

![](assets/unenrollment.png)
*Avregistreringsrapport*

## Feedbackrapport {#feedback-report}

Som administratör kan du nu hämta både elevfeedback (L1) och chefsfeedback (L3) för valda utbildningar under en angiven period.

Du kan exportera data från användargränssnittet eller via PowerBI-anslutningen för mer djupgående analys.

Feedback-rapporter om L1 och L3 ger ett alternativ för att hämta en konsoliderad feedback-rapport för L1- och L3-svaren för valda utbildningar för en **ett år** intervall eller för upp till 10 Valda utbildningar för valfritt datumintervall.

Logga in som administratör och klicka på **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]** och i listan med rapporter klickar du på **[!UICONTROL Feedback Report]**.

![](assets/download-feedbackreport.png)
*Hämta feedbackrapporten*

Om du klickar på Hämta efter att du har valt filtren visas ett meddelande om att du vill hämta rapporten i CSV-format.

Den hämtade rapporten innehåller information som utbildningsnamn och -typ, instansnamn, elevnamn och e-postadress, typ av feedback: L1 eller L3, datum för feedback som har skickats för nya data.

För befintliga data före den här funktionsimplementeringen visas LO-slutförandedatum, LO-slutförandedatum, L1-feedbackfråga Faktisk text och text i klassrum i egen takt i olika kolumner, L1-feedback respektive svar, chefens namn och e-postadress, L3-feedbackvärde och inlämningsdatum, Aktiva fält.

Du kan också exportera data från användargränssnittet eller till Power BI, som stöder alla utbildningar för alla datumintervall för mer djupgående analyser

## Utbildningsrapport {#training-report}

Learning Manager stöder utbildningsrapport som gör det möjligt för administratörer att hämta utbildningsinformation och tillhörande metadata som författare, publiceringsdatum, färdigheter, katalogetiketter osv.

I Admin-programmet klickar du på **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]** > **[!UICONTROL Excel Reports]** > **[!UICONTROL Trainings Report]**.

Du kan hämta rapporter för följande:

* Valda utbildningar (gräns 10) - väljer en eller flera utbildningar (upp till 10) från valfri katalog
* Utbildningar i valda kataloger (gräns 5) - (katalogval kommer att finnas tillgängligt upp till fem kataloger)
* Alla utbildningar - (alla utbildningar på kontot)

![](assets/download-trainingreport.png)
*Hämta utbildningsrapport*

I avsnittet Avancerade alternativ finns följande alternativ:

* Inkludera kursmappningar med utbildningsprogram/certifiering
* Inkludera modulnivåinformation

När du har valt filtren och klickar på Hämta får du ett meddelande om att hämta rapporten i CSV-format.

Rapporten innehåller följande fält:

*Katalognamn, Utbildningstyp, Utbildnings-ID, Utbildningens unika ID, Utbildningsnamn, Underordnade utbildningar, Moduler, Utbildningens eller modulens längd, Format, Utbildningens status, Kompetens, Författare, Senast publicerat datum, Senast slutfört datum, Instruktörer Registreringsantal, Antal påbörjade, Antal slutförda, Gen. L1-poäng, Gen. L2-poäng, Avg L2-poäng mottagna, Antal mottagna svar, L3-svar. och taggar.*

![](assets/more-options.png)
*Ytterligare alternativ*

## Sammanfattningsrapport för session

Sessionssammanfattningsrapporten innehåller alla sessioner som är planerade för en elev inom ett visst datum.

Detta gör att administratören kan exportera alla virtuella sessionsdetaljer och klassrumssessionsdetaljer som faller under det angivna datumintervallet. Administratören kan också exportera sessionsrapporten för specifika utbildningar eller instruktörer.

Det hjälper även administratören att förstå de sessioner som planeras varje månad och identifiera instruktörernas schema och de sessioner som redan har levererats.

Som administratör klickar du på **[!UICONTROL Custom Reports]** > **[!UICONTROL Session Summary Report]**.

Välj datumintervall och utbildning eller instruktör för en sammanfattning i dialogrutan som följer.

![](assets/session-summary-report.png)
*Sammanfattningsrapport för session*

Den hämtade csv-filen innehåller följande fält:

* Startdatum och -tid
* Slutdatum och sluttid

* Modulnamn
* Sessionens varaktighet (i minuter)
* Platsantal
* Plats
* Instansnamn

* Kursnamn
* Kurs-ID
* Instruktörens namn
* Mejladress till instruktör
* Antal registreringar

* Sessionstyp
* Väntlistegräns
* Antal väntelistor
* Mejladress till användare på väntelistan

## Rapport över instruktörsanvändning

Den här rapporten visar den tid (i minuter) som en instruktör tilldelar sessioner varje dag. Rapporten kan laddas ned under tre månader från det valda startdatumet.

Hämta rapporten genom att klicka på **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]** > **[!UICONTROL Instructor Utilization Report]**.

Välj en instruktör eller flera instruktörer och datumintervallet.

![Hämta användningsrapport för instruktör](assets/utilization-report.png)
*Hämta användningsrapport för instruktör*

Den hämtade rapporten innehåller följande fält:

* Instruktörens namn
* Instruktörs-ID
* Kompetensnivå
* Datum som kolumner. Om instruktören används på ett datum visas antalet sessioner. Om instruktören inte används på en dag visas värdet noll.

Rapporten innehåller poster för tre månader från den valda månaden.

Lämna fältet Instruktör tomt om du vill hämta poster för alla instruktörer.

En anpassad administratör med behörighet att generera rapporter kan också hämta den här rapporten.

## Verifieringskedjan för användare - rapport

Den här rapporten innehåller information om elever som bytte instans, &quot;från instans&quot; till &quot;instans&quot;, växlade efter tid, datum osv.

Välj elever eller en användargrupp.

Hämta rapporten genom att klicka på **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]** > **[!UICONTROL User Audit Trail Report]**.

![Hämta rapport över verifieringskedja för användare](assets/user-audit-report.png)

*Hämta rapport över verifieringskedja för användare*

## Rapport över utbildningsplan

Den här rapporten innehåller information om alla utbildningsplaner i ett konto, t.ex. relaterade användargrupper, status och utlösarinformation.

Rapporten innehåller följande:

* Utbildningsplanens namn
* Text (inträffar när)
* Utbildning (slutförd)
* Kompetens (uppnådd)
* Datum (på datum)
* Åtgärd
* Status, skapad av
* Skapandedatum
* Senast ändrad den
* Användargrupp (gäller för)
* Användargrupp (lägg till)
* Registrera dig efter
* Typ(er) av utbildningselement
* Utbildningselement
* Instanser av utbildningselement
* Utbildningselement
* Slutförandedatum
* Påminnelse om utbildningselement
* Omfång – katalog
* Omfång – användargrupp

## Vanliga frågor {#frequentlyaskedquestions}

+++Hur delar man en anpassad tavla med en chef?

Ange namn och beskrivning när du skapar en kontrollpanel. Om du vill dela med chefer anger du chefens namn i **[!UICONTROL Share With]** område.

![](assets/share-dashboard-manager.png)
*Dela en tavla*
+++
