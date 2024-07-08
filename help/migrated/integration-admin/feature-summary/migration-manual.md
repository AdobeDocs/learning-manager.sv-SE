---
description: Referenshandbok för integrationsadministratörer som vill migrera ett befintligt LMS till Adobe Learning Manager LMS.
jcr-language: en_us
title: Handbok för migrering
exl-id: bfdd5cd8-dc5c-4de3-8970-6524fed042a8
source-git-commit: 7be69e68f3b8970e090c8eccd25771cd2e5e99f1
workflow-type: tm+mt
source-wordcount: '3604'
ht-degree: 1%

---

# Handbok för migrering

Referensmanual för integrationsadministratörer som vill migrera ett befintligt LMS till Learning Manager LMS

<!-- ## Overview {#overview} -->

## Scenario för användning {#usagescenario}

I allmänhet har stora företag sitt interna LMS eller någon leverantör som tillhandahåller äldre Learning Management System. LMS består av ditt företags utbildningsinnehåll och utbildningsdata. När du som företag köper Learning Manager kanske du vill flytta ditt befintliga LMS-innehåll och data till Learning Manager så att du kan dra nytta av fördelarna med ett modernt och intuitivt LMS utan att förlora någon av organisationens äldre data.

Learning Manager tillhandahåller de verktyg och specifikationer som krävs så att organisationens integrationsadministratör kan konfigurera och utföra migreringsuppgifterna.

Från och med idag kan en organisations administratörer komma åt migreringsfunktionen i Learning Manager genom att kontakta Adobes supportteam. Om du vill aktivera migreringsfunktionen på ditt konto kan du kontakta Adobe Learning Manager-supportteamet.

## Migreringsprocessen {#apidescription}

Förutsättningar för migrering, viktiga steg som ingår i migreringsprocessen, migreringssprintar, specifikationer, migreringssteg för data och innehåll förklaras i det här avsnittet på följande sätt:

### Förutsättningar {#prerequisites}

Learning Manager-teamet förväntar sig att följande uppgifter utförs av organisationens integrationsadministratörer innan migreringsprocessen påbörjas:

* Integrationsadministratören extraherar data och innehåll från det befintliga LMS:et och omvandlar data till de filformat som definieras av Learning Manager.
* Learning Manager stöder inte import av användare som en del av migreringsprocessen och förväntar sig att organisationen importerar användare med hjälp av anslutningsappar. Adobe Systems förväntar sig att dessa anslutningar konfigureras före migreringsprocessen. Mer information finns i hjälpen](connectors.md) för [Learning Manager-anslutningsappar.

Learning Manager rekommenderar att administratörer kan prova migreringsprocessen i ett utvärderingskonto innan de migrerar data och innehåll till produktionsmiljön för Learning Manager.

### Viktiga steg i migreringsprocessen {#keystepsofmigrationprocess}

De viktigaste stegen för att migrera innehåll och data från ett befintligt LMS till Learning Manager är följande:

1. Integrationsadministratören eller partnern utvärderar befintliga LMS-data och innehåll som behöver migreras.
1. Integrationsadministratören utvärderar de verktyg och specifikationer som Learning Manager tillhandahåller för att mata in data och innehåll.
1. Integrationsadministratören skriver kod eller utför manuellt arbete för att exportera träningsdata och innehåll från det äldre LMS:et baserat på den funktionalitet som tillhandahålls av det äldre LMS:et.
1. När träningsdata och innehåll är tillgängligt analyserar och mappar integrationsadministratören data och innehåll så att de matchar migreringsspecifikationerna för Learning Manager.
1. Integrationsadministratören använder de verktyg som tillhandahålls av Learning Manager för att migrera i följande ordning:

   1. Överför eleverna till Learning Manager
   1. Överför utbildningsinnehåll till Learning Manager och
   1. Överför slutligen träningsdata till Learning Manager.

Organisationen kan börja använda Learning Manager LMS tillsammans med det äldre innehållet.

### Omfång för migreringsobjekt {#scopeofmigrationobjects}

Du kan bara migrera innehåll för följande utbildningsobjekt:

* Modul
* Utmärkelsetecken
* Kurs
* Modulens version
* Kurstillfälle
* Delkurs
* Kompetenser
* Kompetensnivå
* Färdighet kurs
* Certifiering
* Certifiering kurs
* Åtagande om certifiering
* Utbildningsprogram
* Kurs i utbildningsprogram
* Instans av utbildningsprogram
* Kurstillfälle för utbildningsprogram
* Arbetsstöd
* Version för jobbstöd
* Kurs i arbetsstöd
* Kompetens inom arbetsstöd
* Registrering
* Registrering av certifiering
* Registrering för utbildningsprogram
* Registrering av jobbstöd
* Betyg på användarkurs



### Viktiga begrepp inom migration {#keyconceptsofmigration}

Några av de viktigaste begreppen i migreringsprocessen för Learning Manager förklaras kortfattat för din snabbreferens, enligt följande:

**Projekt för migrering**

I Learning Manager består ett migreringsprojekt av en eller flera sprintar. Du kan också ha flera migreringsprojekt för ditt konto. Migreringsprocessen i Learning Manager börjar med att du skapar ett migreringsprojekt.

**Sprinta**

En sprint i migreringsprocessen för Learning Manager definierar en uppsättning migreringsobjekt som du har valt att migrera från det befintliga LMS:et. Ett migreringsobjekt kan vara en kursmodul, elevposter eller en uppsättning kurser. Du kan ha flera inlärningsdataobjekt i en sprint. Du kan köra migreringsjobb i varje sprint.

**Sprintlöpningar**

Sprint Run är en process för att starta ett Sprint-migreringsjobb. Du kan stoppa sprintkörningen när som helst under en körning.

**Repriser av sprintar**

Du kan köra en migreringssprint igen när den har slutförts när som helst. Den här situationen med omkörning eller omkörning av en sprint inträffar när du vill lägga till data i ett sprintobjekt och migrera dem till programmet igen eller korrigera felen i CSV:er.

**CSV-specifikation**

Learning Manager ger dig en uppsättning [standardspecifikationer för](migration-manual.md#main-pars_header_140933605) CSV. Det bästa sättet är att gå igenom dessa CSV-specifikationer innan du börjar med migreringsprocessen. Integrationsadministratören för din organisation kan analysera de befintliga dataformaten och mappa dem så att de matchar de CSV-mallobjekt som tillhandahålls av Learning Manager.

**Taggar för migreringsprojekt**

Adobe Systems rekommenderar att du använder en uppsättning nyckelord som taggar för att enkelt identifiera dina migreringsprojekt i Learning Manager-programmet. Med de här taggarna kan du identifiera dina projekt internt i Learning Manager-programmet vid en viss tidpunkt.

**Innehållslös modul**

Med Learning Manager kan du ladda upp en modul utan innehåll. Adobe Systems betraktar det som en innehållslös modul i Learning Manager. I ett scenario där du vill migrera en del av äldre data från ditt befintliga LMS utan att behöva något innehåll kan du ladda upp den module_version.csv filen utan URL-referens.

## CSV-specifikationer och exempel på CSV:er {#csv}

Nedan hittar du de standardspecifikationer för CSV som du kan använda för att mappa med dina befintliga LMS-migreringsdata. Klicka på csv-specifications och sample-csvs för att ladda ned zip-filer. Den nedladdade csv-specifications.zip innehåller sju Excel-arkfiler. Dessa excel-arkfiler är specifikationer med beskrivningar för att du ska förstå hur du fyller i de .csv filerna. Motsvarande .csv filer ska innehålla data för varje fält i det föreskrivna formatet enligt beskrivningen i dessa .xlsx filer.

<table border="1" cellspacing="0" cellpadding="0" width="100%">
 <tbody>
  <tr>
   <th>
    <p><b>Sl.no</b></p></th>
   <th>
    <p><b>Filnamn</b></p></th>
   <th>
    <p><b>Beskrivning av innehåll</b></p></th>
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
    <p>Nämn ett författarnamn för en viss kurs eftersom flera författarnamn ibland inte visas korrekt i applikationen efter migreringen. </p></td>
  </tr>
  <tr>
   <td>
    <p>4</p></td>
   <td>
    <p>module_version.xlsx </p></td>
   <td>
    <p>Metadata för module_version.csv</p></td>
   <td>
    <p>Se till att du anger URL-sökvägen till Box-kontomappen där du laddade upp innehållet. </p></td>
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
    <p>Se till att varje post i sessionens csv är kopplad till minst en modul för klassrum/virtuellt klassrum</p></td>
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
    <p>Metadata för skill.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>9</p></td>
   <td>
    <p>skill_level.xlsx</p></td>
   <td>
    <p>Metadata för skill_level.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>10</p></td>
   <td>
    <p>skill_course.xlsx</p></td>
   <td>
    <p>Metadata för skill_course.csv</p></td>
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
    <p>Varje job_aid som migreras måste ha en eller flera job_aid versioner.</p></td>
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
    <p>Ange de obligatoriska uppgifterna i .csv-filen även om de inte är obligatoriska. Utan den här informationen kan det hända att Learning Manager-programmet inte återspeglar några data även om .csv bearbetas för migrering. sample-csvs.zip fil innehåller sju .csv filer med liknande namngivningskonvention som ovan.</p></td>
  </tr>
  <tr>
   <td>
    <p>27</p></td>
   <td>
    <p>user_skill.xlsx</p></td>
   <td>
    <p><br>
      Metadata för user_skill.csv</p></td>
   <td>
    <p> </p></td>
  </tr>
 </tbody>
</table>

Learning Manager har endast stöd för datum- och tidsvärden i UTF 8- och 32-bitarsformat. Du kan få fel under migreringen om du nämner datum i CSV-filer med ett datum utanför intervallet som 2038-07-17T08:53:21.000Z eller 1980-04-17T08:13:25.322Z.

* [sample-csvs.zip](assets/sample-csvs.zip)
* [csv_specifications.zip](assets/csv-specifications.zip)

Du måste vara medveten om följande beroenden av CSV-filer under importen:

* module_version.csv är beroende av module.csv
* course_instance.csv är beroende av course.csv
* course_module.csv är beroende av course.csv, module.csv och module_version.csv
* course_instance.csv är beroende av course.csv
* session.csv är beroende av course.csv och module.csv
* enrollment.csv är beroende av course.csv
* user_course_grade.csv är beroende av course.csv och module.csv
* skill_course.csv är beroende av course.csv
* skill_level.csv är beroende av skill.csv
* learning_program_instance.csv är beroende av learning_program och learning_program_course.csv
* learning_program_course.csv är beroende av learning_program.csv
* learning_program_enrollment.csv är beroende av learning_program och learning_program_instance.csv
* learning_program_instance_course_instance.csv är beroende av learning_program.csv, learning_program_instance.csv och course_instance.csv
* certification_course.csv är beroende av certification.csv och course.csv
* certification_commit.csv är beroende av certification.csv och certification_course.csv
* certification_enrollment.csv är beroende av certification.csv, certification_course.csv och certification_enrollment.csv



## Förfarande vid migrering {#migrationprocedure}

Innan du börjar med migreringsproceduren är det viktigt att notera följande punkter:

* Endast ett migreringsprojekt kan vara aktivt på ett konto vid en viss tidpunkt. I ett projekt kan endast en sprint vara aktiv vid en viss tidpunkt.
* Du kan inte ångra en körning som redan är i migreringsprocessen. Du kan dock använda det befintliga borttagningsalternativet i varje funktion i Learning Manager för att ångra migrering av data eller innehåll.
* Så snart migreringsprojektet startar flyttas det till tillståndet &quot;Under migrering&quot;. Under migreringen kan ingen annan roll än integrationsadministratörsrollen logga in på Learning Manager.

### Skapa FTP- och Box-konton {#creatingftpandboxaccounts}

Det är mycket viktigt att planera migreringsprojektet. Vi rekommenderar att du delar upp dina projekt i flera sprintar och tydligt identifierar vad du vill migrera i varje sprint. Det kan till och med vara en bra idé att göra en viss validering efter varje sprint för att känna sig säker på de data som migreras i den sprinten, i stället för en stor valideringsfas i slutet av projektet. Innan du startar sprinten som en del av migreringsprojektet måste du ladda upp CSV-filer för data och innehåll på FTP- respektive Box-servrar. Om du inte har konton för Custom FTP och Box kan du skapa dem.

<!--**Create FTP account**-->

<!--Click **[!UICONTROL Request for CSV FTP folder]**. A pop-up dialog appears prompting you to enter your e-mail id. Go through online instructions and create an FTP account. As soon as you create your account, you can view your migration project and sprint project folders in FTP. 

A sample snapshot of project files and folder of FTP is shown below for your reference. -->

<!--![](assets/exavault-migration-upload-folders.png)-->

**Skapa Box-konto**

Skapa en mapp för uppladdning av innehåll på ett liknande sätt som när du skapar FTP-mappen. Klicka på Migrering i den vänstra rutan och klicka på Begär en mapp för innehållsuppladdning längst ned på sidan som visas.

Du skulle få ett e-postmeddelande från Box med en länk till den delade mappen. Om du inte har ett box-konto klickar du på Registrera dig och skapar ett konto. Inloggningsinstruktioner skickas till e-post-ID för integrationsadministratören.

**Ladda upp data (.csv filer) till FTP-mappar eller Box-mappar**

Att skapa ett FTP- eller Box-konto är en förutsättning innan du skapar ett migreringsprojekt. Så i det här skedet kan du skapa ett migreringsprojekt och sprint i Learning Manager-applikationen.  Se avsnittet Migreringsprocedur **för** data och innehåll på den här sidan för att skapa ett migreringsprojekt.

I FTP- eller Box-kontot klickar du på projektmappens namn och sedan på sprintnamnet. I sprintmappen kan du ladda upp de .csv datafiler som du tänker migrera. För att ladda upp, klicka på Ladda upp filer knappen högst upp i FTP eller Box server och släpp de .csv filerna. Ett exempel på en ögonblicksbild efter uppladdning till FTP visas nedan som referens.

<!--![](assets/exavault-upload.png)-->

Du kan gå tillbaka till migreringsprojektet för Learning Manager, klicka på **[!UICONTROL Refresh]** och visa alla .csv datatyper som visas i din migreringssprint.

**Ladda upp utbildningsinnehåll till innehållsmappar**

Ladda upp utbildningsinnehållet från ditt befintliga LMS till ditt Box-konto. Om du redan har skapat migreringsprojektet och sprinten fyller Box-kontot i migreringsprojektet och sprintnamnet. Du kan ladda upp innehållet i samma sökväg. Se avsnittet Migreringsprocedur **för** data och innehåll på den här sidan för att skapa ett migreringsprojekt.

Du kan dra och släppa innehållsfilerna eller klicka och **[!UICONTROL Upload]** välja filerna från skrivbordet. Om filstorleken på ditt innehåll är enorm kan du uppleva en viss fördröjning när du laddar upp filerna. Beroende på filens storlek varierar den tid det tar att ladda upp filerna till ditt Box-konto.

Ett exempel på en ögonblicksbild av Box-kontot efter att du har laddat upp innehåll till det visas nedan som referens:

![](assets/box-account.png)

*Filer i Box-konto*

När filerna har laddats upp till ditt Box-konto ser du till att du nämner den relativa sökvägen till den här Box-innehållsfilen i module_version.csv filen. Det här är ett obligatoriskt steg för att du ska kunna ange sökvägen till modulinnehållet.

När du har loggat in på FTP- och Box-servrarna och laddat upp innehållet visas CSV-platserna som visas i ögonblicksbilden nedan i Learning Manager.

![](assets/after-setup.jpg)

*CSV-platser i Box-konto*

## Procedur för migrering av data och innehåll {#dataandcontentmigrationprocedure}

Proceduren för att migrera företagets LMS-data och innehåll till Learning Manager förklaras på följande sätt:

Gå igenom förutsättningarna för migreringsprocessen innan du börjar med migreringen. Se avsnittet CSV-specifikationer [och exempel på CSV:er](migration-manual.md#main-pars_header_140933605) på den här sidan och förbered CSV:erna för data- och innehållsmigrering.

1. Logga in på Learning Manager-applikationen som integrationsadministratör och klicka på **[!UICONTROL Migration]** i den vänstra rutan.

   Startsidan för migreringsprojekt visas. Om din organisation redan har skapat migreringsprojekt kan du visa en lista över alla migreringsprojekt på den här sidan.

1. Klicka på **[!UICONTROL New]** längst upp till höger på sidan för att skapa ett migreringsprojekt. Du kan också klicka **[!UICONTROL Create a migration project]** på länken på sidan för att skapa ett migreringsprojekt. Sidan Skapa ett migreringsprojekt visas.

   Om du inte redan har skapat en FTP-mapp kommer du att uppmanas att skapa en FTP-mapp på kontot. Det här är ett obligatoriskt steg innan du börjar skapa ett migreringsprojekt.

   ![](assets/create-project.png)
   *Skapa FTP-mapp*

   Ange projektnamn, projekttagg, kurskatalog och beskrivning för migreringsprojektet. Klicka på **[!UICONTROL Create]**.

   Dina migreringsdataobjekt identifieras med hjälp av den här taggen för migreringsprojekt. Om du inte har någon specifik kurskatalog väljer du standardkatalogen i rullgardinsmenyn. Alla kurser som du migrerar med hjälp av ett migreringsprojekt kommer att ingå i katalogen som du väljer i det här skedet. Om du inte väljer någon katalog kommer alla migrerade kurser att vara en del av standardkatalogen.

1. Konfigurationssidan för sprint visas som du ser i följande ögonblicksbild. Du måste skapa en sprint som en del av migreringsprojektet. Välj Sprintnamn och ge en kort beskrivning av sprinten. Du kan välja Ja om du vill migrera innehåll som en del av den här sprinten. Klicka på **[!UICONTROL Next]**.

   ![](assets/users-modified-sprint.png)
   *Migrering av sprint*

   Markera kryssrutan med rubriken **Användare har lagts till eller ändrats sedan den senaste körningen** för att synkronisera listan över användare med Learning Manager-programmet. Om du migrerar innehåll och data till Learning Manager-programmet kanske detta inte krävs. Men om det finns en tidsfördröjning mellan din tidigare sprintmigrering till den senaste sprintmigreringen är det bästa sättet att du väljer att synkronisera listan över användare. Det här steget gör att Learning Manager-databasen kan synkroniseras med dina LMS-användare.

   Det här synkroniseringssteget rekommenderas när enrollment.csv och user_course_grade.csv migreras. Det här steget gör det möjligt för Learning Manager-databasen att vara synkroniserad med din migreringsdatabas och säkerställer att alla användare vars poster som ska migreras i Sprint är tillgängliga i Migreringsdatabasen.

1. Du kan starta Sprint-migreringen med dina uppladdade data och innehåll. Klicka på **[!UICONTROL Refresh]** länken innan du startar sprintkörningen för att synkronisera FTP- och innehållsmapparna med Learning Manager-applikationen.

   ![](assets/sprint1-filesupload.png)
   *Starta sprintmigrering*

   Klicka på **[!UICONTROL Start]** längst upp till höger på sidan. Du kan klicka **[!UICONTROL Stop]** när som helst under sprintmigreringsprocessen för att avbryta sprintmigreringen.

   Migreringsstatus visas för vart och ett av sprintdataobjekten och innehållet. Kontrollera antalet lyckade och misslyckade objekt som en del av migreringssprintkörningen.

   Om du laddar upp modulinnehåll kontrollerar du att sökvägen till innehållsmappen anges i module_version.csv. Om du missar det här steget kan du stöta på fel under migreringen. Om du till exempel laddar upp innehåll i en modul i egen takt, till exempel videor, måste du ange en relativ Box URL-sökväg i module_version.csv. För Aktivitetsmodulinnehåll kan du ange URL-namnet.

   Ett exempel på en ögonblicksbild av förloppsdialogrutan finns nedan som referens. Som du ser i ögonblicksbilden kan du visa antalet poster som bearbetas för varje migreringsdataobjekt tillsammans med status för lyckade och misslyckade objekt. Klicka på Ladda ned felposter mot de misslyckade objekten för att ladda ned och visa felloggarna. Du kan åtgärda problemen i CSV och ladda upp igen i FTP.

   ![](assets/sample-sprint-progress-status.png)
   *Visa sprintförlopp*

   Klicka på Sprintlista i den vänstra rutan om du vill visa en lista över alla sprintar i ett migreringsprojekt. Du kan visa en lista över alla sprintar, antalet körningar som du har kört för varje sprint, startdatum, varaktighet och slutförandestatus enligt exempelbilden nedan.

   ![](assets/sprint-list.png)
   *Visa lista över sprintar*

1. När du har laddat upp de senast uppdaterade CSV:erna kan du klicka på Kör igen i det övre högra hörnet på sidan. Kör om bearbetar alla dataobjekt en gång till och ignorerar de objekt som inte har några ändringar. När du är nöjd med migreringen av dataobjekt i en sprint kan du markera vårmigreringen som slutförd genom att klicka på knappen högst upp på sidan. Du kan starta en ny sprint med fler dataobjekt senare. När en sprint har markerats som slutförd kan du inte köra den igen. På samma sätt kan du ha valfritt antal sprintar i ett migreringsprojekt. När du är nöjd med migreringsstatusen för alla sprintar kan du markera migreringsprojektet som slutfört genom att klicka på **länken Markera projekt som slutfört** på sidan Sprintlista.

   Innan du markerar migreringsprojektet som slutfört måste du se till att alla sprintar i projektet är klara. När du har markerat migreringsprojektet som slutfört kan du inte gå tillbaka och skapa några sprintar i projektet eller göra några ändringar i projektet. Du måste skapa ett annat migreringsprojekt och lägga till sprintar i det.

## Verifiering av migrering {#registration}

När du har migrerat utbildningsdata och innehåll från organisationens äldre LMS kan du verifiera importerade data och innehåll med hjälp av olika funktioner för utbildningsobjekt. Du kan till exempel logga in på Learning Manager-applikationen som administratör och verifiera tillgängligheten för importerade moduler och kursdata och innehåll.

## Eftermontering vid migrering {#retrofittinginmigration}

Med den här integreringsfunktionen kan du anpassa historiska data för ett lärobjekt i efterhand från en äldre lärplattform till en aktiv kurs som har skapats i Learning Manager.

Nedan hittar du de standardspecifikationer för CSV som du kan använda för att mappa med dina befintliga LMS-migreringsdata. Klicka på csv-specifications och sample-csvs för att ladda ned zip-filer. Den nedladdade csv-specifications.zip innehåller fyra Excel-arkfiler. Dessa excel-arkfiler är specifikationer med beskrivningar för att du ska förstå hur du fyller i de .csv filerna. Motsvarande .csv filer ska innehålla data för varje fält i det föreskrivna formatet enligt beskrivningen i dessa .xlsx filer.

1-enrollment.xlsx innehåller beskrivningar av metadata som krävs för retrofit_enrollment.csv fil.

2-certification_enrollment.xlsx innehåller beskrivningar av metadata som krävs för retrofit_certification_enrollment.csv fil.

3-learning_program_enrollment.xlsx innehåller beskrivningar av metadata som krävs för retrofit_learning_program_enrollment.csv fil.

4-user_course_grades.xlsx innehåller beskrivningar av metadata som krävs för retrofit_user_course_grades.csv fil.
[csv-specifications.zip](assets/csv-specifications.zip)

>[!NOTE]
>
>UUID (Universally Unique Id) är också en kolumn i migrerings-csv-filen.


## Felsöka migreringsproblem {#troubleshootingmigrationissues}

[Klicka här](../../kb/troubleshooting-migration.md) för att lära dig mer om lösningen/lösningen på de problem som integrationsadministratörer står inför när de migrerar data och innehåll från sitt befintliga LMS till Learning Manager-applikationen.

## Tips för användarhantering {#usermanagement}

I det här avsnittet hittar du några av tipsen för att förstå hur användare betraktas och hanteras i Learning Manager. Dessa koncept skulle hjälpa dig att hantera användarna bättre när du använder CSV-import, anslutningsprogram och migreringsfunktioner i Learning Manager.

## ID:n för utbildningschef {#captivateprimeids}

Learning Manager tillhandahåller två typer av unika ID:n för användare:

* E-post-ID
* UUID (universellt unikt id)

Learning Manager stöder UUID för att ge organisationer flexibilitet när det gäller att kontrollera användarkonton. Om du som administratör har UUID för användare i ett konto kan du ändra e-post-ID:n för användare för det kontot.

**Användningsscenario för UUID i en organisation**

Tänk dig ett scenario där en anställd A ansluter sig till ett företag som heter Learning Manager som entreprenör. Under avtalsperioden får Learning Manager-företaget inte tillhandahålla företagets e-post-ID som```A@example.com```, istället kan företaget endast överväga den anställdes personliga e-postkonto, säg. ```A@gmail.com``` Efter att ha fullgjort 6 månaders kontraktsperiod, om samma anställd A går med i Learning Manager som heltidsanställd, kanske Learning Manager vill ändra sitt e-post-ID till sitt företags e-post-ID: ```A@example.com```.

Att ha UUID-åtkomst till användarkontot kommer att gynna företagets Learning Manager i ovan nämnda scenario. Learning Manager-företaget kan enkelt ersätta det personliga e-post-ID:t för anställd A med ett officiellt e-post-ID. Den anställdes poster som är relevanta för det här kontot påverkas inte av den här ändringen.

## Identifiering av en användare {#singleuseridentification}

Learning Manager identifierar och kommer ihåg hur en enskild användare läggs till i den, till exempel med hjälp av självregistrering, med hjälp av CSV-uppladdning eller en enskild användare som läggs till med hjälp av användargränssnittet eller med hjälp av API.

* Om en enskild användare läggs till med hjälp av användargränssnittet (UI) eller via API:et kan du ta bort en sådan typ av enskilda användare med hjälp av användargränssnittet eller via API.
* Du kan uppdatera enskilda användare med hjälp av CSV-uppladdningsprocessen, men du måste komma ihåg att dessa enskilda användare behandlas som CSV-användare och att CSV-arbetsflödena gäller för sådana användare.

## Tilldela rollen Chef {#assigningmanagerrole}

Du kan inte tilldela en chefsroll direkt till någon användare i Learning Manager. En användare X kan bara bli Learning Manager Manager när du anger ett Manager-attribut för en användare (t.ex. Y) i det kontot som X.

I ett scenario där X är chef för användare, till exempel A, B och C, om X lämnar organisationen måste du se till att attributet Chef för A, B och C är inställt på den nya chefen. Alternativt kan du också ange attributet Manager för dessa användare som ROOT tillfälligt och tilldela med det nya Manager-namnet senare.

Mer information om det här avsnittet finns i följande hjälpinnehåll:

* [Vanliga frågor och svar om att ladda upp CSV-filer](/help/migrated/administrators/add-users-in-bulk.md)
* [Funktionshjälp om hur du lägger till användare](/help/migrated/administrators/feature-summary/add-users-user-groups.md)
