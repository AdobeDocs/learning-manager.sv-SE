---
description: Referenshandbok för integrationsadministratörer som vill migrera ett befintligt LMS till Adobe Learning Manager LMS.
jcr-language: en_us
title: Migreringshandbok
exl-id: bfdd5cd8-dc5c-4de3-8970-6524fed042a8
source-git-commit: 898103cd6cda48bf4303c660b6c635d3208deca5
workflow-type: tm+mt
source-wordcount: '3602'
ht-degree: 1%

---

# Migreringshandbok

Referenshandbok för integrationsadministratörer som vill migrera ett befintligt LMS till Learning Manager LMS

<!-- ## Overview {#overview} -->

## Användningsscenario {#usagescenario}

I allmänhet har stora företag sina interna system för hantering av inlärning eller en leverantör som tillhandahåller äldre system för hantering av inlärning. LMS består av företagets utbildningsinnehåll och utbildningsdata. Om du är ett företag när du köper Learning Manager kanske du vill flytta ditt befintliga LMS-innehåll och -data till Learning Manager så att du kan dra nytta av fördelarna med modernt och intuitivt LMS utan att förlora någon av organisationens gamla data.

Learning Manager tillhandahåller de verktyg och specifikationer som behövs för att din organisations integrationsadministratör ska kunna konfigurera och utföra migreringsuppgifterna.

Från och med idag kan migreringsfunktionen i Learning Manager nås av en organisations administratörer genom att kontakta Adobe supportteam. Om du vill aktivera migreringsfunktionen i ditt konto kan du kontakta Adobe Learning Manager-supportteamet.

## Migreringsprocess {#apidescription}

Förutsättningar för migrering, viktiga steg som rör migreringsprocessen, migreringspurter, specifikationer, migrering av data och innehåll förklaras i det här avsnittet enligt följande:

### Krav {#prerequisites}

Learning Manager-teamet förväntar sig att följande uppgifter utförs av organisationens integrationsadministratörer innan migreringsprocessen inleds:

* Integreringsadministratören extraherar data och innehåll från det befintliga LMS-systemet och omvandlar data till de filformat som definierats av Learning Manager.
* Learning Manager stöder inte import av användare som en del av migreringsprocessen och förväntar sig att organisationen importerar användare med hjälp av kopplingar. Adobe Systems förväntar sig att dessa anslutningar är konfigurerade före migreringsprocessen. Se [Hjälp för Learning Manager-anslutningar](connectors.md) för mer information.

Learning Manager rekommenderar att administratörer kan testa migreringsprocessen på ett testkonto innan de migrerar data och innehåll till Learning Manager-produktionsmiljön.

### Viktiga steg i migreringsprocessen {#keystepsofmigrationprocess}

De viktigaste stegen när du migrerar innehåll och data från ett befintligt LMS till Learning Manager är följande:

1. Integreringsadministratören eller integrationspartnern utvärderar befintliga LMS-data och innehåll som behöver migreras.
1. Integration Administrator utvärderar de verktyg och specifikationer som Learning Manager tillhandahåller för att hämta data och innehåll.
1. Integreringsadministratören skriver kod eller utför manuellt arbete för att exportera utbildningsdata och innehåll från det äldre LMS baserat på de funktioner som tillhandahålls av det äldre LMS.
1. När utbildningsdata och -innehåll är tillgängliga analyserar och mappar integrationsadministratören data och innehåll för att matcha migreringsspecifikationerna för Learning Manager.
1. Integreringsadministratören använder verktygen som tillhandahålls av Learning Manager för att migrera i följande ordning:

   1. Överför eleverna till Learning Manager
   1. Överför utbildningsinnehåll till Learning Manager och
   1. Till sist överför vi utbildningsdata till Learning Manager.

Organisationen kan börja använda Learning Manager LMS tillsammans med det äldre innehållet.

### Omfång för migreringsobjekt {#scopeofmigrationobjects}

Du kan bara migrera innehåll för följande utbildningsobjekt:

* Modul
* Utmärkelsetecken
* Kurs
* Modulversion
* Kursinstans
* Kursmodul
* Kompetenser
* Färdighet
* Kompetenskurs
* Certifiering
* Certifieringskurs
* Bekräfta certifiering
* Utbildningsprogram
* kurs i utbildningsprogram
* Instans för utbildningsprogram
* Kursinstans för utbildningsprogram
* Arbetsstöd
* Version av arbetsstöd
* Arbetsstödskurs
* Arbetsstödskunskaper
* Registrering
* Registrering till certifiering
* Registrering till utbildningsprogram
* Arbetsstödsregistrering
* Kursens betygsättning



### Viktiga begrepp inom migrering {#keyconceptsofmigration}

Några av de viktigaste begreppen i migreringsprocessen för Learning Manager förklaras kort så här:

**Migreringsprojekt**

I Learning Manager består ett migreringsprojekt av en eller flera sprintar. Du kan också ha flera migreringsprojekt för ditt konto. Migreringsprocessen i Learning Manager börjar med att skapa ett migreringsprojekt.

**Sprint**

En Sprint i migreringsprocessen för Learning Manager definierar en uppsättning migreringsobjekt som du har valt att migrera från det befintliga LMS:et. Ett migreringsobjekt kan vara en kursmodul, elevposter eller ett antal kurser. Du kan ha flera utbildningsdataobjekt i en sprint. Du kan utföra migreringsjobb i varje sprint.

**Sprint Runs**

Sprint Run är processen att starta ett Sprint-migreringsjobb. Du kan stoppa sprinten när som helst under en körning.

**Sprint Re-run**

Du kan köra ett migreringsspurt igen när som helst efter att det har slutförts. Den här situationen med rekörning eller rekörning av en sprint inträffar när du vill lägga till data i ett sprintobjekt och migrera det till programmet igen eller korrigera felen i CSV-filer.

**CSV-specifikation**

Learning Manager innehåller en uppsättning [CSV-standardspecifikationer](migration-manual.md#main-pars_header_140933605). Det bästa sättet är att gå igenom dessa CSV-specifikationer innan du börjar migrera. Integreringsadministratören för din organisation kan analysera de befintliga dataformaten och mappa dem så att de matchar de CSV-mallobjekt som Learning Manager tillhandahåller.

**Taggar för migreringsprojekt**

Adobe Systems rekommenderar att du använder en uppsättning nyckelord som taggar för att identifiera dina migreringsprojekt enkelt i Learning Manager-programmet. Med hjälp av dessa taggar kan du identifiera dina projekt internt i Learning Manager-appen vid valfri tidpunkt.

**Innehållslös modul**

Med Learning Manager kan du ladda upp en modul utan innehåll. Adobe Systems ser den som en innehållslös modul i Learning Manager. I ett scenario där du vill migrera en del av den äldre informationen från ditt befintliga LMS utan behov av något innehåll, kan du överföra filen module_version.csv utan URL-referens.

## CSV-specifikationer och CSV-exempelfiler {#csv}

Nedan hittar du specifikationerna för CSV-standardfiler som du kan använda för att mappa med befintliga LMS-migreringsdata. Klicka på csv-specifikationer och exempel-csv:er för att hämta zip-filer. Den hämtade csv-fications.zip innehåller sju Excel-arkfiler. De här Excel-arkfilerna är specifikationer med beskrivningar som hjälper dig att förstå hur du fyller upp .csv-filerna. Motsvarande .csv-filer ska innehålla data för varje fält i det föreskrivna format som förklaras i dessa .xlsx-filer.

<table border="1" cellspacing="0" cellpadding="0" width="100%">
 <tbody>
  <tr>
   <th>
    <p><b>Sl.no</b></p></th>
   <th>
    <p><b>Filnamn</b></p></th>
   <th>
    <p><b>Innehållsbeskrivning</b></p></th>
   <th>
    <p>Anteckningar</p></th>
  </tr>
  <tr>
   <td>
    <p>1</p></td>
   <td>
    <p>module.xlsx</p></td>
   <td>
    <p>Metadata för module.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>2</p></td>
   <td>
    <p>badge.xlsx</p></td>
   <td>
    <p>Metadata för badge.xlsx</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>3</p></td>
   <td>
    <p>course.xlsx</p></td>
   <td>
    <p>Metadata för course.csv</p></td>
   <td>
    <p>Nämn ett författarnamn för en viss kurs eftersom flera författarnamn ibland inte visas korrekt i programmet efter migreringen. </p></td>
  </tr>
  <tr>
   <td>
    <p>4</p></td>
   <td>
    <p>module_version.xlsx </p></td>
   <td>
    <p>Metadata för module_version.csv</p></td>
   <td>
    <p>Se till att du anger URL-sökvägen till Box-kontomappen där du överförde innehållet. </p></td>
  </tr>
  <tr>
   <td>
    <p>5</p></td>
   <td>
    <p>course_instance.xlsx</p></td>
   <td>
    <p>Metadata för course_instance.csv </p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>6</p></td>
   <td>
    <p>session.xlsx</p></td>
   <td>
    <p>Metadata för session.csv</p></td>
   <td>
    <p>Se till att alla poster i CSV-filen för sessionen är kopplade till minst en klassrums-/virtuell klassrumsmodul</p></td>
  </tr>
  <tr>
   <td>
    <p>7</p></td>
   <td>
    <p>course_module.xlsx</p></td>
   <td>
    <p>Metadata för course_module.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>8</p></td>
   <td>
    <p>skill.xlsx</p></td>
   <td>
    <p>Metadata för skills.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>9</p></td>
   <td>
    <p>skills_level.xlsx</p></td>
   <td>
    <p>Metadata för skills_level.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>10</p></td>
   <td>
    <p>skills_course.xlsx</p></td>
   <td>
    <p>Metadata för skills_course.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>11</p></td>
   <td>
    <p>certification.xlsx</p></td>
   <td>
    <p>Metadata för Certification.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>12</p></td>
   <td>
    <p>certification_course.xlsx</p></td>
   <td>
    <p>Metadata för certification_course.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>13</p></td>
   <td>
    <p>certification_commit.xlsx</p></td>
   <td>
    <p>Metadata för certification_commit.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>14</p></td>
   <td>
    <p>learning_program.xlsx</p></td>
   <td>
    <p>Metadata för learning_program.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>15</p></td>
   <td>
    <p>learning_program_course.xls </p></td>
   <td>
    <p>Metadata för learning_program_course.csv </p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>16</p></td>
   <td>
    <p>learning_program_instance.xlsx </p></td>
   <td>
    <p>Metadata för learning_program_instance.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>17</p></td>
   <td>
    <p>learning_program_instance_course_instance.xlsx </p></td>
   <td>
    <p>Metadata för learning_program_instance_course_instance.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>18</p></td>
   <td>
    <p>job_aid.xlsx</p></td>
   <td>
    <p>Metadata för job_aid.csv</p></td>
   <td>
    <p>Varje migrerat job_aid kräver en eller flera versioner av job_aid.</p></td>
  </tr>
  <tr>
   <td>
    <p>19</p></td>
   <td>
    <p>Job_aid_version.xlsx</p></td>
   <td>
    <p>Metadata för job_aid_version.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>20</p></td>
   <td>
    <p>job_aid_course.xlsx</p></td>
   <td>
    <p>Metadata för job_aid_course.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>21</p></td>
   <td>
    <p>job_aid_skills.xlsx</p></td>
   <td>
    <p>Metadata för job_aid_skills.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>22</p></td>
   <td>
    <p>enrollments.xlsx</p></td>
   <td>
    <p>Metadata för enrollments.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>23</p></td>
   <td>
    <p>certification_enrollement.xlsx</p></td>
   <td>
    <p>Metadata för certification_enrollement.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>24</p></td>
   <td>
    <p>learning_program_enrollment.xlsx</p></td>
   <td>
    <p>Metadata för learning_program_enrollment.csv<br><br></p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>25</p></td>
   <td>
    <p>job_aid_enrollment.xlsx</p></td>
   <td>
    <p>Metadata för job_aid_enrollment.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>26</p></td>
   <td>
    <p>user_course_grade.xlsx</p></td>
   <td>
    <p><br>
      Metadata för user_course_grade.csv</p></td>
   <td>
    <p>Ange nödvändiga elevdata i .csv-filen även om de inte är obligatoriska. Utan den här informationen kanske programmet Learning Manager inte återspeglar några data, även om .csv-filen bearbetas för migrering. Filen sample-csvs.zip innehåller sju .csv-filer med liknande namngivningsregler som ovan.</p></td>
  </tr>
 </tbody>
</table>

Learning Manager stöder endast datum- och tidsvärden i UTF 8- och 32-bitarsformat. Du kan få fel under migreringen om du nämner datum i CSV-filer med ett ogiltigt datum som 2038-07-17T08:53:21.000Z eller 1980-04-17T08:13:25,322 Z

* [sample-csvs.zip](assets/sample-csvs.zip)
* [csv_fications.zip](assets/csv-specifications.zip)

Du måste vara medveten om följande beroenden av CSV-filer under importen:

* module_version.csv är beroende av module.csv
* course_instance.csv är beroende av course.csv
* course_module.csv är beroende av course.csv, module.csv och module_version.csv
* course_instance.csv är beroende av course.csv
* session.csv är beroende av course.csv och module.csv
* enrollment.csv är beroende av course.csv
* user_course_grade.csv är beroende av course.csv och module.csv
* skills_course.csv är beroende av course.csv
* skills_level.csv är beroende av skills.csv
* learning_program_instance.csv är beroende av learning_program och learning_program_course.csv
* learning_program_course.csv är beroende av learning_program.csv
* learning_program_enrollment.csv är beroende av learning_program och learning_program_instance.csv
* learning_program_instance_course_instance.csv är beroende av learning_program.csv, learning_program_instance.csv och course_instance.csv
* certification_course.csv är beroende av certification.csv och course.csv
* certification_commit.csv är beroende av certification.csv och certification_course.csv
* certification_enrollment.csv är beroende av certification.csv, certification_course.csv och certification_enrollment.csv

## Migreringsprocessen {#migrationprocedure}

Innan du börjar med migreringsproceduren är det viktigt att tänka på följande:

* Endast ett migreringsprojekt kan vara aktivt på ett konto vid en viss tidpunkt. Inom ett projekt kan endast en sprint vara aktiv vid en given tidpunkt.
* Du kan inte ångra en körning som redan pågår i migreringsprocessen. Du kan dock använda det befintliga borttagningsalternativet i varje funktion i Learning Manager för att ångra migrering av data eller innehåll.
* Så snart migreringsprojektet inleds hamnar det i ett tillstånd av &quot;Under migration&quot;. Under migreringen kan ingen annan roll än integrationsadministratörsrollen logga in på Learning Manager.

### Skapa FTP- och Box-konton {#creatingftpandboxaccounts}

Det är mycket viktigt att du planerar ditt migreringsprojekt. Vi rekommenderar att du delar upp dina projekt i flera sprintar och tydligt anger vad du vill flytta i varje sprint. Det kan till och med vara en god idé att göra en viss validering efter varje sprint för att känna sig säker på de data som migreras i den sprinten, i stället för en stor valideringsfas i slutet av projektet. Innan du börjar skriva ut som en del av ditt migreringsprojekt måste du överföra data- och CSV-innehållsfiler i FTP- respektive Box-servrar. Om du inte har några konton för anpassad FTP och Box kan du skapa dem.

<!--**Create FTP account**-->

<!--Click **[!UICONTROL Request for CSV FTP folder]**. A pop-up dialog appears prompting you to enter your e-mail id. Go through online instructions and create an FTP account. As soon as you create your account, you can view your migration project and sprint project folders in FTP. 

A sample snapshot of project files and folder of FTP is shown below for your reference. -->

<!--![](assets/exavault-migration-upload-folders.png)-->

**Skapa Box-konto**

Skapa en mapp för innehållsöverföring i en liknande process som följer för att skapa FTP-mappar. Klicka på Migrering i den vänstra rutan och klicka på Begär en mapp för överföring av innehåll längst ned på sidan som visas.

Du skulle få ett e-postmeddelande från Box med en länk till den delade mappen. Om du inte har ett Box-konto klickar du på Registrera dig och skapar ett konto. Inloggningsinstruktioner skickas till e-post-ID för integreringsadministratören.

**Överför data (.csv-filer) till FTP- eller Box-mappar**

Du måste skapa ett FTP- eller Box-konto innan du skapar ett migreringsprojekt. Så i det här skedet kan du skapa ett migreringsprojekt och Sprint i Learning Manager-programmet.  Se **Förfarande för migrering av data och innehåll** på den här sidan om du vill skapa ett migreringsprojekt.

I FTP- eller Box-kontot klickar du på namnet på projektmappen och sedan på namnet på utskriftsbilden. I mappen sprint kan du överföra de .csv-datafiler som du tänker migrera. Om du vill överföra klickar du på knappen Överför filer högst upp i FTP- eller Box-servern och släpper .csv-filerna. En exempelögonblicksbild efter överföring till FTP visas nedan som referens.

<!--![](assets/exavault-upload.png)-->

Du kan komma tillbaka till migreringsprojektet för Learning Manager, klicka på **[!UICONTROL Refresh]** och visa alla .csv-datatyper som anges i migreringsprofilen.

**Överföra utbildningsinnehåll till innehållsmappar**

Överför utbildningsinnehållet för ditt befintliga LMS till ditt Box-konto. Om du redan har skapat migreringsprojektet och sprintar fylls migreringsprojektet och sprintnamnet i Box-kontot. Du kan överföra innehållet på samma sökväg. Se **Förfarande för migrering av data och innehåll** på den här sidan om du vill skapa ett migreringsprojekt.

Du kan dra och släppa innehållsfilerna eller klicka på **[!UICONTROL Upload]** och välj filerna från skrivbordet. Om filstorleken för ditt innehåll är stor kan du uppleva en viss fördröjning vid överföring av filerna. Beroende på filens storlek varierar den tid det tar att överföra filerna till ditt Box-konto.

En exempelögonblicksbild av Box-kontot efter att ha överfört innehåll till det visas nedan som referens:

![](assets/box-account.png)

*Filer i Box-konto*

När filerna har överförts till ditt Box-konto ser du till att du nämner den relativa sökvägen för Boxs innehållsfil i module_version.csv -filen. Det här är ett obligatoriskt steg där du måste ange sökvägen till modulinnehållet.

När du har loggat in på FTP- och Box-servrarna och överfört innehållet, visas CSV-platserna som i ögonblicksbilden nedan i Learning Manager.

![](assets/after-setup.jpg)

*CSV-platser i Box-konto*

## Förfarande för migrering av data och innehåll {#dataandcontentmigrationprocedure}

Proceduren för att migrera dina Enterprise LMS-data och -innehåll till Learning Manager beskrivs nedan:

Gå igenom förutsättningarna för migreringsprocessen innan du börjar med migreringen. Se [CSV-specifikationer och CSV-exempelfiler](migration-manual.md#main-pars_header_140933605) på den här sidan och förbereda CSV-filerna för data- och innehållsmigrering.

1. Logga in på Learning Manager-programmet som integrationsadministratör och klicka på **[!UICONTROL Migration]** i den vänstra rutan.

   Startsidan för Migreringsprojekt visas. Om din organisation redan har skapat migreringsprojekt kan du visa listan över alla migreringsprojekt på den här sidan.

1. Klicka **[!UICONTROL New]** skapa ett migreringsprojekt i det övre högra hörnet på sidan. Du kan också klicka på **[!UICONTROL Create a migration project]** för att skapa ett migreringsprojekt. Sidan Skapa ett migreringsprojekt visas.

   Om du inte redan har skapat en FTP-mapp kommer du att uppmanas att skapa en FTP-mapp i kontot. Det här är ett obligatoriskt steg innan du börjar skapa ett migreringsprojekt.

   ![](assets/create-project.png)
   *Skapa FTP-mapp*

   Ange projektnamnet, projekttaggen, kurskatalogen och beskrivningen för ditt migreringsprojekt. Klicka på **[!UICONTROL Create]**.

   Migreringsdataobjekten identifieras med den här migreringsprojekttaggen. Om du inte har någon specifik kurskatalog väljer du standardkatalogen i listrutan. Alla kurser som du migrerar med ett migreringsprojekt inkluderas i katalogen som du väljer i det här skedet. Om du inte väljer någon katalog kommer alla migrerade kurser att bli en del av standardkatalogen.

1. Sidan Konfiguration av utskrift visas som i följande ögonblicksbild. Du måste skapa ett språng som en del av migreringsprojektet. Välj Sprintnamn och en kort beskrivning av sprinten. Du kan välja Ja om du vill migrera innehåll som en del av det här steget. Klicka på **[!UICONTROL Next]**.

   ![](assets/users-modified-sprint.png)
   *Sprintmigrering*

   Markera kryssrutan med titeln **Användare har lagts till eller ändrats sedan den senaste körningen**, för att synkronisera listan över användare med Learning Manager-programmet. Om du migrerar innehåll och data till Learning Manager-appen kanske detta inte krävs. Men om det finns ett tidsintervall mellan din tidigare spurtmigrering till den senaste spurtmigreringen är det bästa praxis att du väljer att synkronisera användarlistan. Det här steget gör att Learning Manager-databasen kan synkroniseras med dina LMS-användare.

   Det här synkroniseringssteget rekommenderas när enrollment.csv och user_course_grade.csv migreras. Det här steget gör att Learning Manager-databasen kan synkroniseras med din migreringsdatabas och säkerställer att alla användare vars poster ska migreras i Sprint är tillgängliga i migreringsdatabasen.

1. Du kan starta Sprintmigreringen med dina överförda data och ditt innehåll. Klicka **[!UICONTROL Refresh]** länk innan du startar Sprint Run för att synka FTP- och innehållsmappar med Learning Manager-programmet.

   ![](assets/sprint1-filesupload.png)
   *Starta migrering av sprint*

   Klicka **[!UICONTROL Start]** längst upp till höger på sidan. Du kan klicka **[!UICONTROL Stop]** när som helst under Sprint-migreringsprocessen för att avbryta sprint-migreringen.

   Migreringsstatusen visas för alla utskriftsdataobjekt och -innehåll. Kontrollera antalet lyckade och misslyckade objekt som en del av migreringspurten.

   Om du överför modulinnehåll kontrollerar du att sökvägen till innehållsmappen finns i module_version.csv. Om du missar det här steget kan du stöta på fel under migreringen. Om du till exempel överför innehåll i moduler, som videor, i egen takt måste du ange en relativ sökväg till Box-URL i module_version.csv. För innehåll i modulen Aktivitet kan du ange URL-namnet.

   En ögonblicksbild av förloppsdialogrutan visas nedan som referens. Som visas i ögonblicksbilden kan du visa antalet poster som har bearbetats för varje migreringsdataobjekt tillsammans med status för slutförda och misslyckade objekt. Klicka på Hämta felloggar vid de misslyckade objekten för att hämta och visa felloggarna. Du kan åtgärda problemen i CSV-filen och överföra dem igen via FTP.

   ![](assets/sample-sprint-progress-status.png)
   *Visa utskriftsförlopp*

   Klicka på Sprint list i den vänstra rutan om du vill visa listan över alla sprintar i ett migreringsprojekt. Du kan se en lista över alla sprintar, antalet sprintar du utförde för varje sprint, startdatum, varaktighet och slutförandestatus enligt exemplet nedan.

   ![](assets/sprint-list.png)
   *Visa lista med utskrifter*

1. När du har överfört de senast uppdaterade CSV-filerna kan du klicka på Kör igen längst upp till höger på sidan. Alla dataobjekt bearbetas igen och de objekt som inte har ändrats ignoreras. När du är nöjd med migreringen av dataobjekt i en sprint kan du markera vårmigreringen som slutförd genom att klicka på knappen högst upp på sidan. Du kan starta en ny spurt med fler dataobjekt senare. När en utskrift har markerats som slutförd kan du inte köra den igen. På samma sätt kan du i ett migreringsprojekt ha valfritt antal sprintar. När du är nöjd med migreringsstatusen för alla sprintar kan du markera migreringsprojektet som slutfört genom att klicka på **Markera projekt som slutfört** på sidan Sprint List.

   Innan du markerar migreringsprojektet som slutfört måste du se till att alla sprintar i projektet är slutförda. När du har markerat migreringsprojektet som slutfört kan du inte gå tillbaka och skapa sprintar i det projektet eller göra ändringar i det. Du måste skapa ett annat migreringsprojekt och lägga till sprints.

## Migreringsverifiering {#registration}

När du har migrerat utbildningsdata och -innehåll från organisationens äldre LMS kan du verifiera importerade data och innehåll med hjälp av olika funktioner i utbildningsobjekt. Du kan till exempel logga in som administratör på Learning Manager-programmet och kontrollera tillgängligheten för importerade moduler och kursdata och -innehåll.

## Eftermontering i migrering {#retrofittinginmigration}

Med den här integreringsfunktionen kan du anpassa historiska data för ett utbildningsobjekt från ett äldre system för hantering av inlärning till en aktiv kurs som skapas i Learning Manager.

Nedan hittar du specifikationerna för CSV-standardfiler som du kan använda för att mappa med befintliga LMS-migreringsdata. Klicka på csv-specifikationer och exempel-csv:er för att hämta zip-filer. Den hämtade csv-fications.zip innehåller fyra Excel-arkfiler. De här Excel-arkfilerna är specifikationer med beskrivningar som hjälper dig att förstå hur du fyller upp .csv-filerna. Motsvarande .csv-filer ska innehålla data för varje fält i det föreskrivna format som förklaras i dessa .xlsx-filer.

1-enrollment.xlsx-innehåller beskrivningar av metadata som krävs för retrofit_enrollment.csv-filen.

2-certification_enrollment.xlsx-innehåller beskrivningar av metadata som krävs för retrofit_certification_enrollment.csv-filen.

3-learning_program_enrollment.xlsx-innehåller beskrivningar av metadata som krävs för filen retrofit_learning_program_enrollment.csv.

4-user_course_grades.xlsx-innehåller beskrivningar av metadata som krävs för retrofit_user_course_grades.csv-filen.
[csv-fications.zip](assets/csv-specifications.zip)

>[!NOTE]
>
>UUID (Universally Unique Id) är också en kolumn i CSV-filen för migrering.


## Felsöka migreringsproblem {#troubleshootingmigrationissues}

[Klicka här](../../kb/troubleshooting-migration.md) för att lära dig mer om hur du löser de problem som integrationsadministratörer möter när de migrerar data och innehåll från sina befintliga LMS till Learning Manager-programmet.

## Tips för användarhantering {#usermanagement}

I det här avsnittet hittar du några av tipsen som hjälper dig att förstå hur användare beaktas och hanteras i Learning Manager. Dessa koncept skulle hjälpa dig att hantera användarna bättre när du använder CSV-import, kopplingar och migreringsfunktioner i Learning Manager.

## ID för Learning Manager {#captivateprimeids}

I Learning Manager finns två typer av unika ID:n för användare:

* Mejl-ID
* UUID (universellt unikt ID)

Learning Manager har stöd för UUID för att ge organisationer flexibilitet när det gäller att kontrollera användarkonton. Om du som administratör har ett UUID för användare på ett konto kan du ändra e-postadresserna för användarna för det kontot.

**Användningsscenario för UUID i en organisation**

Tänk dig ett scenario där en anställd A går med i ett företag som heter Learning Manager, som uppdragstagare. Under avtalsperioden kan Learning Manager-företaget inte tillhandahålla företagets e-post-ID som A@example.com, i stället kan företaget endast överväga den anställdes personliga e-postkonto, till exempel A@gmail.com. Efter att ha slutfört sex månaders avtalsperiod kan Learning Manager vilja ändra sitt e-post-id till företagets e-postadress om samma anställd A går med i Learning Manager som heltidsanställd: A@example.com.

Om du har UUID-åtkomst till användarkontot kan företaget Learning Manager dra nytta av ovanstående scenario. Learning Manager-företaget kan enkelt ersätta den personliga e-post-id för medarbetare A med ett officiellt e-post-id. Medarbetarens poster som är relevanta för det här kontot påverkas inte av den här ändringen.

## Identifiering av en enskild användare {#singleuseridentification}

Learning Manager identifierar och kommer ihåg hur en enskild användare läggs till i den, t.ex. genom självregistrering, med CSV-uppladdning, eller en enskild användare som lagts till med hjälp av användargränssnittet eller med API.

* Om en enskild användare läggs till med hjälp av användargränssnittet eller API:et kan du ta bort en sådan typ av enskilda användare med hjälp av användargränssnittet eller API:et.
* Du kan uppdatera enskilda användare med CSV-uppladdningsprocessen, men du måste komma ihåg att dessa enskilda användare behandlas som CSV-användare och att CSV-arbetsflödena gäller sådana användare.

## Tilldela chefsroll {#assigningmanagerrole}

Du kan inte tilldela en chefsroll direkt till någon användare i Learning Manager. En användare X kan bara bli en Learning Manager-hanterare när du anger ett Manager-attribut för en användare (till exempel Y) i kontot som X.

I ett scenario där X är chef för användare, till exempel A, B och C, måste du se till att chefsattributet för A, B och C är inställt på den nya chefen om X lämnar organisationen. Du kan också ställa in chefsattributet för dessa användare som ROOT tillfälligt och tilldela med det nya chefsnamnet senare.

Mer information om det här avsnittet finns i följande hjälpinnehåll:

* [Vanliga frågor om överföring av CSV-filer](/help/migrated/administrators/add-users-in-bulk.md)
* [Funktionshjälp för att lägga till användare](/help/migrated/administrators/feature-summary/add-users-user-groups.md)
