---
jcr-language: en_us
title: Distributionshandbok för Learning Manager - Avsnitt 2
contentowner: sanm
preview: true
source-git-commit: fba5e5ddc1964b485be473bf356806f234688cf4
workflow-type: tm+mt
source-wordcount: '2206'
ht-degree: 1%

---



# Distributionshandbok för Learning Manager - Avsnitt 2

## Teknisk installation {#technicalsetup}

Den tekniska konfigurationen för ditt Learning Manager-konto krävs främst för enterprise-användare. I det här dokumentet beskrivs hur du konfigurerar enkel inloggning för organisationen och integrerar Learning Manager med anslutningar från tredje part.

### Konfigurera enkel inloggning {#configuresinglesignon}

En av dina första uppgifter som systemadministratör i Admin Console är att definiera och konfigurera ett identitetssystem som dina slutanvändare ska autentiseras mot. Allt eftersom organisationen köper licenser för Learning Manager måste du driftsätta dessa licenser till slutanvändarna. Och för det behöver du ett sätt att autentisera dessa användare. Utför följande procedur för att konfigurera enkel inloggning för användarna.

1. Klicka på **[!UICONTROL ** Inställningar **>** Inloggningsmetoder **på startsidan för Learning Manager.]**

   ![](assets/configure-sso-step1.png)

1. Beroende på användartyp väljer du antingen **[!UICONTROL ** Interna användare **eller** Externa användare **.]**



1. I **[!UICONTROL **Logga in**]**listrutan väljer du **[!UICONTROL ** Enkel inloggning **.]**

   ![](assets/configure-sso-step3.png)

1. Klicka på **[!UICONTROL **&#x200B;Ändra **om du vill konfigurera inställningarna för enkel inloggning.]**

   ![](assets/configure-sso-step4.png)

1. I fältet ****[!UICONTROL IDP-Initiated Authentication URL]**** anger du den autentiserings-URL som du fått av tjänsteleverantören.



   ![](assets/configure-sso-step5.png)

1. Klicka på **[!UICONTROL **Överför **]**bredvid XML-fältet **[!UICONTROL  **IDP-metadata **]******och överför XML-filen.
1. Klicka på **[!UICONTROL ** Spara **.]**
1. SSO-autentiseringen har konfigurerats för ditt konto. Du bör kunna logga in på ditt Learning Manager-konto med SSO.

   ***SSO-konfigurationen i Learning Manager bör ha stöd för SAML 2.0.***

## Migrering av användardata {#migrationofuserdata}

När ditt företag köper Learning Manager som administratör är migrering ett av de viktigaste stegen du behöver utföra. Det är av största vikt att du flyttar ditt befintliga utbildningsinnehåll och dina användardata till Learning Manager. Följande migreringsarbetsflöde hjälper dig att dra nytta av fördelarna med modernt och intuitivt LMS utan att förlora några av organisationens gamla data.

Med Learning Manager kan du migrera från ditt befintliga LMS via en steg-för-steg-guide, i iterativa sprintar. Du får fullständig insyn i statusen för varje sprint för att säkerställa att eleverna upplever noll driftstopp när du migrerar äldre data till Adobe Learning Manager.

Du måste ha administratörsbehörighet för integrering för att kunna utföra migreringsarbetsflödet. Som administratör kan du antingen ta på dig rollen som integrationsadministratör eller tilldela en annan användare den här rollen.

**Vi kan ta Shaleens hjälp här för att skapa en visuell bild.**

1. Förkunskapskrav
1. Utvärdering av det befintliga innehållet och användardata
1. Exportera och mappa data från befintligt LMS
1. Konfigurera FTP- och BOX-mappar för migrering
1. Överför eleverna till Learning Manager
1. Överför utbildningsinnehåll till Learning Manager
1. Överför återstående data till Learning Manager



### Förkunskapskrav {#prerequisite}

Innan du startar migreringsprocessen måste du utföra följande krav:

* Extrahering av data och innehåll från det befintliga LMS och omvandling av data till filformaten som definierats av Learning Manager.
* Importera användare via FTP- och BOX-anslutningar. Integreringsadministratören måste se till att anslutningarna är konfigurerade före migreringsprocessen.



***Vi rekommenderar att administratörer testar migreringsprocessen på ett testkonto innan de migrerar data och innehåll till Learning Manager-produktionsmiljön. ***

### Utvärdera och exportera data {#evaluatingandexportingdata}

Integreringsadministratören bör först titta på de data som är tillgängliga i det aktuella LMS:et. Som integrationsadministratör kan du bara migrera följande utbildningsobjekt:

* Modul
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
* Registreringar
* Registrering till certifiering
* Registrering till utbildningsprogram
* Kursens betygsättning



När du har utvärderat dina befintliga data måste du mappa dessa data till CSV-standardspecifikationerna i Learning Manager. Hämta följande ***csv-fications.zip***-exempelfil som innehåller sju Excel-ark som krävs för den här migreringen. Dessa Excel-ark innehåller specifikationer med beskrivningar som hjälper dig att mappa befintliga data till fälten i .csv-filer.

<!--
<Download link to the zip file>
-->

Kontrollera att varje .csv-fil innehåller data för varje fält i det föreskrivna formatet:

<table> 
 <tbody> 
  <tr> 
   <th width="7%" valign="top"><p><strong>Nej.</strong></p></th> 
   <th width="29%" valign="top"><p><strong>Excel-bladnamn</strong></p></th> 
   <th width="31%" valign="top"><p><strong>Beskrivning av innehåll</strong></p></th> 
   <th width="31%" valign="top"><p><strong>Anteckningar</strong></p></th> 
  </tr> 
  <tr> 
   <td><p>1</p></td> 
   <td><p>module.xlsx</p></td> 
   <td><p>Metadata för module.csv</p></td> 
   <td><p> </p></td> 
  </tr> 
  <tr> 
   <td><p>2</p></td> 
   <td><p>course.xlsx</p></td> 
   <td><p>Metadata för course.csv</p></td> 
   <td><p>Nämn ett författarnamn för en viss kurs eftersom flera författarnamn ibland inte visas korrekt i programmet efter migreringen. </p></td> 
  </tr> 
  <tr> 
   <td><p>3</p></td> 
   <td><p>module_version.xlsx </p></td> 
   <td><p>Metadata för module_version.csv</p></td> 
   <td><p>Ange URL-sökvägen till Box-kontomappen dit du överförde innehållet. </p></td> 
  </tr> 
  <tr> 
   <td><p>4</p></td> 
   <td><p>course_instance.xlsx</p></td> 
   <td><p>Metadata för course_instance.csv </p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>5</p></td> 
   <td><p>course_module.xlsx</p></td> 
   <td><p>Metadata för course_module.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>6</p></td> 
   <td><p>skill.xlsx</p></td> 
   <td><p>Metadata för skills.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>7</p></td> 
   <td><p>skills_level.xlsx</p></td> 
   <td><p>Metadata för skills_level.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>8</p></td> 
   <td><p>skills_course.xlsx</p></td> 
   <td><p>Metadata för skills_course.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>9</p></td> 
   <td><p>Certification.xlsx</p></td> 
   <td><p>Metadata för Certification.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>10</p></td> 
   <td><p>certification_course.xlsx</p></td> 
   <td><p>Metadata för certification_course.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>11</p></td> 
   <td><p>certification_commit.xlsx</p></td> 
   <td><p>Metadata för certification_commit.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>12</p></td> 
   <td><p>learning_program.xlsx</p></td> 
   <td><p>Metadata för learning_program.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>13</p></td> 
   <td><p>learning_program_course.xls </p></td> 
   <td><p>Metadata för learning_program_course.csv </p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>14</p></td> 
   <td><p>learning_program_instance.xlsx </p></td> 
   <td><p>Metadata för learning_program_instance.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>15</p></td> 
   <td><p>learning_program_instance_course_instance.xlsx </p></td> 
   <td><p>Metadata för learning_program_instance_course_instance.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>16</p></td> 
   <td><p>enrollments.xlsx</p></td> 
   <td><p>Metadata för enrollments.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>17</p></td> 
   <td><p>certification_enrollment.xlsx</p></td> 
   <td><p>Metadata för certification_enrollment.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>18</p></td> 
   <td><p>learning_program_enrollment.xlsx</p></td> 
   <td><p>Metadata för learning_program_enrollment.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>19</p></td> 
   <td><p>User_course_grade.xlsx</p></td> 
   <td><p>Metadata för User_course_grade.csv</p></td> 
   <td><p>Ange nödvändiga elevdata i .csv-filen även om de inte är obligatoriska. Utan den här informationen kanske programmet Learning Manager inte återspeglar några data, även om .csv-filen bearbetas för migrering. </p></td> 
  </tr> 
 </tbody> 
</table>

***Learning Manager stöder endast datum- och tidsvärden i UTF 8- och 32-bitarsformat. Det kan uppstå fel under migreringen om du anger ett datum i CSV-filer som inte ligger inom det tillåtna intervallet, t.ex. 2038-07-17T08:53:21.000Z eller 1980-04-17T08:13:25.322Z.***

### Beroenden vid import av data till csv-filer {#dependencieswhileimportingdatatocsvfiles}

När du importerar befintliga data till CSV-standardformatet bör du vara medveten om följande beroenden:

* module_version.csv är beroende av module.csv
* course_instance.csv är beroende av course.csv
* course_module.csv är beroende av course.csv, module.csv och module_version.csv
* course_instance.csv är beroende av course.csv
* enrollment.csv är beroende av course.csv
* user_course_grade.csv är beroende av course.csv och module.csv
* skills_course.csv är beroende av course.csv
* skills_level.csv är beroende av skills.csv
* learning_program_instance.csv är beroende av utbildningsprogrammet och learning_program_course.csv
* learning_program_course.csv är beroende av learning_program.csv
* learning_program_enrollment.csv är beroende av utbildningsprogram och learning_program_instance.csv
* learning_program_instance_course_instance.csv är beroende av learning_program.csv, learning_program_instance.csv och course_instance.csv
* certification_course.csv är beroende av certification.csv och course.csv
* certification_commit.csv är beroende av certification.csv och certification_course.csv
* certification_enrollment.csv är beroende av certification.csv, certification_course.csv och certification_enrollment.csv



När du har exporterat informationen sparar du .csv-filerna på den lokala datorn. Filerna kan nu släppas i FTP- eller BOX-mapparna.

## Konfigurera FTP- och BOX-mappar för migreringen {#setupftpandboxfoldersforthemigration}

Innan du planerar och startar den faktiska migreringen av allt innehåll måste du konfigurera FTP- och BOX-mapparna. Du behöver dessa mappar för att släppa dina .csv-filer i dessa mappar. När ditt äldre innehåll, i form av .csv-filer, är tillgängligt i FTP- och BOX-mapparna kan informationen konsumeras i Learning Manager.

### Skapa ett FTP-konto {#setupanftpaccount}

Klicka på **[!UICONTROL ** Begäran om CSV FTP-mapp **på startsidan för Integreringsadministratör.]** Ange ditt e-post-ID i popup-dialogrutan som visas. Gå igenom onlineguiden för att skapa FTP-kontot för Exavault. När du har skapat ditt konto kan du visa migreringsprojektet och sprintprojektmapparna i Exavault FTP.

Se ett exempel på en ögonblicksbild av projektfilerna och mappen för ExaVault på följande sätt:

![](assets/set-up-an-ftp-account.png)

När du har konfigurerat FTP-mappen visar systemet meddelandet &quot;FTP-mappinstallationen är klar&quot;.

## Skapa ett BOX-konto {#setupaboxaccount}

Så här skapar du ett BOX-konto och skapar en BOX-mapp:

Välj Migrering på startsidan för Integreringsadministratör.

I avsnittet Inställningar klickar du på Begär för en Box-mapp.

![](assets/set-up-a-box-account.png)

I fältet ****[!UICONTROL Enter Email]**** anger du e-post-ID:t där du vill få inloggningsinstruktionerna för att ansluta till Box.

Klicka på **[!UICONTROL ** Anslut **.]**

Du skulle få ett e-postmeddelande från Box med en länk till den delade mappen. Om du inte har ett Box-konto klickar du på Registrera dig och skapar ett konto. Inloggningsinstruktioner skickas sedan till e-post-ID för integreringsadministratören.

När du har sparat anslutningen visar migreringssidan meddelandet: &quot;Konfigurationen av Box-mappen är klar&quot;.

## Migrera innehållet till Learning Manager {#migratingthecontenttocaptivateprime}

Innan du startar migreringen är det viktigt att tänka på följande:

* Endast ett migreringsprojekt kan vara aktivt på ett konto vid en viss tidpunkt. Inom ett projekt kan endast en sprint vara aktiv vid en given tidpunkt.
* Du kan inte ångra en körning som redan bearbetas. Du kan dock använda det befintliga borttagningsalternativet i varje funktion i Learning Manager för att ångra migrering av data eller innehåll.

Så snart som migreringsprojektet inleds förflyttas projektet till ett tillstånd av &quot;Under migration&quot;. I det här läget kan ingen annan användare än integrationsadministratören logga in på Learning Manager.

Överföra utbildningsinnehåll till innehållsmappar:

Klicka på **[!UICONTROL Migration.]** på startsidan för Integreringsadministratör

På startsidan för migrering visar systemet de migreringsprojekt som redan har skapats i din organisation.

Klicka på **[!UICONTROL **Nytt**]**i det övre högra hörnet på sidan om du vill skapa ett migreringsprojekt.

***Om du inte redan har skapat en FTP-mapp kommer du att uppmanas att skapa ett FTP-mappkonto för Exavault. Det här är ett obligatoriskt steg innan du börjar skapa ett migreringsprojekt. ***

Ange namnet på projektet på sidan ****[!UICONTROL Create a New Migration Project]****.

![](assets/migrating-the-content-1.png)

Ange en tagg för projektet, kurskatalogen och ange en beskrivning för migreringsprojektet. Dina migreringsdataobjekt identifieras med hjälp av migreringsprojekttaggen. Om du inte har någon specifik kurskatalog väljer du standardkatalogen från listrutan kommer alla kurser som du migrerar med ett migreringsprojekt att inkluderas i katalogen som du väljer i det här skedet. Om du inte väljer någon katalog kommer alla migrerade kurser att bli en del av standardkatalogen.

Klicka på **[!UICONTROL Create.]**

Skapa en utskrift för ditt migreringsprojekt på sidan Konfiguration av Sprint. En Sprint i migreringsprocessen för Learning Manager definierar en uppsättning migreringsobjekt som du har valt att migrera från det befintliga LMS:et.

![](assets/migrating-the-content-2.png)

Ange ett namn för sprinten och beskriv sprinten.

Välj ****[!UICONTROL Users have been added or modified since the last run check box]**** för att synkronisera listan över användare med Learning Manager-programmet. Om du migrerar innehåll och data till Learning Manager-appen kanske detta inte är nödvändigt. Men om det finns en tidsfördröjning mellan din tidigare sprintmigrering till den senaste spurtmigreringen rekommenderar vi att du väljer att synka användarlistan. Det här steget gör att Learning Manager-databasen kan synkroniseras med dina LMS-användare.

***Synkroniseringssteget rekommenderas när enrollment.csv och user_course_grade.csv migreras. Det här steget gör att Learning Manager-databasen kan synkroniseras med din migreringsdatabas och säkerställer att alla användare vars poster ska migreras i Sprint är tillgängliga i migreringsdatabasen.***

Klicka på **[!UICONTROL ** Nästa **.]**

Klicka på **[!UICONTROL **Starta**]**för att starta Sprintmigreringen med dina överförda data och ditt innehåll. Klicka på ****[!UICONTROL Refresh]**** innan du startar Sprint Run för att synkronisera FTP- och innehållsmapparna med Learning Manager.

![](assets/migrating-the-content-3.png)

Du kan klicka på ****[!UICONTROL Stop]****när som helst under utskriftsmigreringen för att avbryta utskriftsmigreringen.

Systemet visar migreringsstatus mot varje utskriftsdataobjekt och innehåll. Kontrollera antalet lyckade och misslyckade objekt som en del av migreringspurten.

Om du överför modulinnehåll kontrollerar du att sökvägen till innehållsmappen finns i *module_version.csv *filen. Om du missar det här steget kan du stöta på fel under migreringen. Om du till exempel överför innehåll i en modul som du själv har skapat, till exempel videor, måste du ange den relativa URL-sökvägen för Box i *module_version.csv *filen.

En ögonblicksbild av migreringsförloppet visas nedan som referens. Som visas i ögonblicksbilden kan du visa antalet poster som har bearbetats för varje migreringsdataobjekt tillsammans med status för slutförda och misslyckade objekt. Klicka på Hämta felloggar vid de misslyckade objekten för att hämta och visa felloggarna. Du kan åtgärda problemen i CSV-filen och överföra dem igen via FTP.

![](assets/migrating-the-content-4.png)

Klicka på **[!UICONTROL **Sprint**]**i det vänstra navigeringsfönstret för att visa listan över alla sprintar i ett migreringsprojekt. Du kan se en lista över alla sprintar, antalet sprintar du utförde för varje sprint, startdatum, varaktighet och slutförandestatus enligt exemplet nedan.

![](assets/migrating-the-content-5.png)

Klicka på **[!UICONTROL **Sprint**]**i det vänstra navigeringsfönstret för att visa listan över alla sprintar i ett migreringsprojekt. Du kan se en lista över alla sprintar, antalet sprintar du utförde för varje sprint, startdatum, varaktighet och slutförandestatus enligt exemplet nedan.

Klicka på **[!UICONTROL **Sprint**]**i det vänstra navigeringsfönstret för att visa listan över alla sprintar i ett migreringsprojekt. Du kan se en lista över alla sprintar, antalet sprintar du utförde för varje sprint, startdatum, varaktighet och slutförandestatus enligt exemplet nedan.

***Innan du markerar migreringsprojektet som slutfört ser du till att alla sprintar i projektet är slutförda. När du har markerat migreringsprojektet som slutfört kan du inte gå tillbaka och skapa sprintar i det projektet. Du kan inte göra några ändringar i det projektet. Du kan bara skapa ett annat migreringsprojekt och lägga till sprints till det.***

När du har migrerat utbildningsdata och -innehåll från organisationens äldre LMS kontrollerar du om data och innehåll importeras korrekt. Du kan verifiera genom att logga in som administratör och verifiera att importerade moduler och kursdata och innehåll är tillgängliga

Användbara resurser om migrering finns i:

* Felsöka migreringsproblem
* Vanliga frågor om överföring av CSV-filer

