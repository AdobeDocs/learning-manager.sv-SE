---
description: Det här dokumentet innehåller grundläggande felsökningstips för att lösa några av de vanligaste problemen som kan uppstå när du migrerar data och innehåll från ett befintligt LMS till Learning Manager.
jcr-language: en_us
title: Felsöka migreringsproblem
contentowner: jayakarr
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '847'
ht-degree: 0%

---



# Felsöka migreringsproblem

Det här dokumentet innehåller grundläggande felsökningstips för att lösa några av de vanligaste problemen som kan uppstå när du migrerar data och innehåll från ett befintligt LMS till Learning Manager.

## Allmänna migreringsproblem {#genericmigrationissues}

### Kan inte logga in på FTP-mapp eller innehållsmapp {#unabletologintoftpfolderorcontentfolder}

Kontrollera att dina konton har skapats i FTP- och Box-tjänsterna. När du skapar ett migreringsprojekt begär du att få konfigurera de här två tjänsterna. Så snart du har skapat tjänsterna får du e-postmeddelanden från Exavault och Box för att återställa eller ställa in lösenorden. Om du inte kommer ihåg lösenorden kan du återställa dem genom att besöka webbplatserna Exavault och Box.

### Jobb visas inte ens när du klickar på Uppdatera {#jobsarenotreflectedevenafterclickingrefreshbutton}

* Se till att CSV-filerna överförs till rätt mapp i Exavault FTP. Banstrukturen ska vara följande:

`code Account>Project>Sprint location`

* Kontrollera att filnamnen för CSV-filerna överensstämmer med CSV-specifikationsnamnen:

   * course.csv
   * course_instance.csv
   * course_module.csv
   * enrollment.csv
   * module.csv
   * module_version.csv
   * user_course_grade.csv

### Fel visas för jobb med felposter {#failuresareshownforjobswitherrorrecords}

1. Hämta felloggarna genom att klicka på **Hämta felposter** länk
1. Korrigera de ursprungliga CSV-filerna baserat på de rapporterade felen och
1. Kör Sprinten igen med de ändrade CSV-filerna.

Det bästa sättet är att köra ändrade CSV-filer på en ny utskrift när antalet ändringar är färre jämfört med det totala antalet poster.

### Det går inte att logga in på Learning Manager-programmet även efter att Sprint-migreringen har stoppats {#unabletologintocaptivateprimeapplicationevenafterstoppingthesprintmigration}

Det kan ta 10-15 minuter att låsa upp ett konto när en Sprintkörning har stoppats eller slutförts. Försök att komma åt programmet efter 15 minuter.

### Vissa migreringsjobb visar status Pågår även efter att Stopp har utlösts. {#someofthemigrationjobsdisplayinprogressstatusevenafterstopistriggered}

Det kan ta 10-15 minuter att sluta köra alla jobb när det är i läget Pågår. Kontrollera statusen igen efter tio minuter.

### Det går inte att skapa en utskrift eftersom knappen är inaktiverad {#unabletocreateasprintasthebuttonisdisabled}

Se till att den aktuella utskrift är markerad som slutförd innan du skapar en utskrift. Klicka **[!UICONTROL Mark Sprint Complete]** längst upp på sidan för att slutföra en Sprint-migrering.

### Det går inte att markera ett migreringsprojekt som slutfört eftersom knappen är inaktiverad {#unabletomarkamigrationprojectascompleteasthebuttonisdisabled}

Se till att aktuell Sprint är markerad som slutförd innan du markerar migreringsprojektets slutförande. Klicka **[!UICONTROL Mark Sprint Complete]** längst upp på sidan för att slutföra en Sprint-migrering.

## CSV-problem {#csvissues}

### module_version.csv filmigrering misslyckas och innehåll migreras inte ännu {#moduleversioncsvfilemigrationisfailingandcontentisnotmigratedyet}

Se till att innehållet är tillgängligt i mappen Innehåll (Box-konto under det angivna migreringsprojektet, sprint-sökväg). Se också till att du har valt alternativet **Ja** för **Kommer du att migrera innehåll för det här trycket?** -frågan på den sida där sprinten skapas.

Om du glömmer bort att markera **Ja**, och fortsätta vidare i denna sprint, sedan måste du vänta tills du slutför denna sprint. Skapa ytterligare ett spurt och se till att klicka **[!UICONTROL Yes]**.

### enrollment.csv- eller user_course_grade.csv-poster misslyckas med ett felmeddelande: Inte ett giltigt ID för Learning Manager {#enrollmentcsvorusercoursegradecsvrecordsfailwithanerrormessagenotavalidprimeid}

Se till att e-post-id:t som tillhandahålls som en del av fälten userId, assignedByUserID tillhör giltiga Learning Manager-användare. Om inte, lägg till användaren, skapa en ny utskrift med **Synka användare** alternativet har valts. Om användaren inte ingår i organisationen lägger du till användaren som borttagen användare i Learning Manager med CSV-specifikationen Lägg till användare. En CSV-exempelspecifikation för att lägga till borttagna användare finns nedan som referens.

[Users.csv](assets/users.zip) Se **CSV-specifikationer och CSV-exempelfiler** avsnitt i [Migreringshandbok](../integration-admin/feature-summary/migration-manual.md) för att hämta alla CSV-specifikationer och CSV-exempelfiler.

### Kurser visas tomma eller felaktiga moduler spelas upp för en migrerad kurs {#coursesappearblankorincorrectmodulesplayforamigratedcourse}

Se till att **moduleOrderInCourse** nyckelvärde för en kurs börjar med **0** och är i kontinuerlig ordning. Ordningen enligt courseModuleType ska vara PRETEST, TESTOUT, CONTENT

Se också till att två versioner av Activity, Classroom och VC inte är kopplade till den befintliga kursen.

### Ta emot ett meddelande som &quot;Modul är redan länkad till en befintlig kurs&quot; {#receivingamessageasmoduleisalreadylinkedwithanexistingcourse}

Learning Manager tillåter inte länkning av Activity/VC/Classroom-modul till mer än en kurs. Kontrollera att modulen inte är länkad till några andra kurser.

### Alla kurser visar den senaste versionen av Activity/VC/Classroom-moduler även om kurserna är kopplade till olika modulversioner {#allthecoursesshowthelatestversionofactivityvcclassroommoduleseventhoughthecoursesarelinkedwithdifferentmoduleversions}

Versionshantering av moduler för Aktivitet, Klassrum och Virtuellt klassrum stöds inte i Learning Manager. Om du anger versioner via filen moduleVersion.csv uppdateras den befintliga filen i stället för att en ny version skapas.

### Önskad varaktighet visas inte för en migrerad Aktivitet/VC/Klassrum-modul {#desireddurationdoesnotappearforamigratedactivityvcclassroommodule}

Önskad varaktighet är inte en giltig post för modulen Aktivitet/VC/Klassrum.

### Hyperlänks-URL öppnas inte i Learning Manager {#hyperlinkurldoesntopenupincaptivateprime}

Se till att de tillhandahållna länkarna är förinstallerade med &quot;http://&#39;&quot; eller &quot;https://&#39;

### ModuleVersion-migreringen misslyckas med fel om att filen inte hittades {#moduleversionmigrationfailswithfilenotfounderrors}

Se till att den refererade filen finns i innehållsmappen och att den har migrerats.

### ModuleVersion-migreringen misslyckas med ett felmeddelande som &quot;Ett internt fel har inträffat - för modul : x och moduleVersion : y&quot; {#moduleversionmigrationfailswithanerrormessageasaninternalerrorhasoccurredformodulexandmoduleversiony}

Kör sprinten igen för att lösa problemet.
