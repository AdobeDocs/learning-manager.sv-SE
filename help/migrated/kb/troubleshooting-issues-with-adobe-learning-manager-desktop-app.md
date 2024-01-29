---
description: Det här dokumentet innehåller grundläggande felsökningstips för att lösa några av de vanligaste problemen vid installation och användning av Adobe Learning Manager-datorprogrammet.
jcr-language: en_us
title: Felsöka problem med skrivbordsappen Adobe Learning Manager
contentowner: kuppan
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '1434'
ht-degree: 0%

---



# Felsöka problem med skrivbordsappen Adobe Learning Manager

Det här dokumentet innehåller grundläggande felsökningstips för att lösa några av de vanligaste problemen vid installation och användning av Adobe Learning Manager-datorprogrammet.

## Jag kan inte göra följande {#iamunabletodothefollowing}

+++Jag kan inte hämta datorprogrammet Adobe Learning Manager

1. Kontrollera inställningarna för internetanslutningen och brandväggen.
1. Klicka på i Social utbildning **[!UICONTROL New Post]** för att skapa ett inlägg. Om du inte har någon anslagstavla ska du skapa en anslagstavla först.
1. Klicka på något av följande alternativ för inläggsknappar som visas för att skapa innehåll som Screen Shot, Record Audio, Record Video, Learning Manager Gallery. Du dirigeras till skrivbordsprogramsidan för Adobe Learning Manager där du kan ladda ned datorprogrammet Adobe Learning Manager till datorn.
1. Du behöver ett giltigt Adobe Learning Manager-konto där Social utbildning är aktiverat av administratören. Din administratör kan också ha inaktiverat hämtningar via webbläsaren. Kontakta din Adobe Learning Manager-administratör för mer information om hur du hämtar datorprogrammet Adobe Learning Manager.

+++

+++Jag kan inte installera datorprogrammet Adobe Learning Manager

1. Se till att systemet uppfyller de lägsta systemkraven. Se [Systemkrav för appen Adobe Learning Manager för dator](../learners/adobe-learning-manager-app-for-desktop/adobe-learning-manager-desktop-app-system-requirements.md).
1. Rensa tidigare installationer av Adobe Learning Manager-datorprogram. Mer information finns i  [Rengöra tidigare installationer](#howtocleanuppreviousinstallationsofadobelearningmanagerdesktopapp) för mer information.
1. För fel under installationsprocessen, se [Hitta programloggar](#howtofindapplicationlogs). Kontakta administratören för Adobe Learning Manager-datorprogrammet för mer hjälp.

+++

+++Jag kan inte starta datorprogrammet Adobe Learning Manager

1. Kontrollera att skrivbordsprogrammet Adobe Learning Manager har hämtats och installerats.
1. Klicka på i Social utbildning **[!UICONTROL New Post]** (Om du inte har en anslagstavla, skapa då en anslagstavla). Klicka på något av följande alternativ för inläggsknappar som visas - Ta en skärmbild, Ljudinspelning, Videoinspelning, Galleri för Adobe Learning Manager. Du omdirigeras till en sida där du kan starta datorprogrammet Adobe Learning Manager.
1. Om appen inte startar kan du också starta den från Start-menyn i Windows eller från Launchpad i Mac OS X.

+++

+++Jag kan inte logga in på mitt konto i datorprogrammet Adobe Learning Manager

1. Se till att du är ansluten till internet och att brandväggsinställningarna inte blockerar datorprogrammet Adobe Learning Manager.
1. Kontrollera att du har ett giltigt Adobe Learning Manager-elevkonto med Social utbildning aktiverat.
1. Om du fortfarande inte kan logga in avslutar och startar du om datorprogrammet Adobe Learning Manager och försöker sedan igen.
1. Kontakta din Adobe Learning Manager-administratör om du vill ha mer hjälp.

+++

+++Jag kan inte se min webbkamera/mikrofon som listas i Adobe Learning Manager-datorprogrammet

1. Kontrollera att webbkameran/mikrofonen är korrekt ansluten till systemet och fungerar som den ska.
1. Kontrollera att du har installerat de senaste drivrutinerna för webbkameran/mikrofonen. Vissa enheter fungerar inte som de ska utan dedikerade drivrutiner.
1. Återställ programpreferenserna och starta sedan om datorprogrammet Adobe Learning Manager och försök igen. Mer information finns i [Så här återställer du programinställningarna](#howtoresetapplicationpreferences).
1. Om du använder Mac OS X Mojave 10.14 kan du bevilja behörigheter till Adobe Learning Manager-datorprogrammet för att få åtkomst till webbkameran/mikrofonen. Mer information finns i [Så här ställer du in webbkamera/mikrofonbehörighet på OSX Mojave](#howtosetwebcammicrophonepermissionsonMacOSXMojave).

+++

+++Jag kan inte publicera mina inlägg från datorprogrammet Adobe Learning Manager

1. Se till att du har ett giltigt Adobe Learning Manager-elevkonto med Social utbildning aktiverat av din Adobe Learning Manager-administratör.
1. Återställ programpreferenserna och starta sedan om datorprogrammet Adobe Learning Manager och försök igen. Mer information finns i [Så här återställer du programinställningarna](#howtoresetapplicationpreferences).
1. Aktivera avancerad loggning vid fel i publiceringen. Mer information finns i [Aktivera avancerad loggning](#howtoenableadvancedlogging), starta om Adobe Learning Manager-datorprogrammet, gör om stegen ovan som orsakar felet. Skicka de senaste programloggarna till din Adobe Learning Manager-administratör för att få hjälp. Mer information finns i [Hitta programloggar](#howtofindapplicationlogs).

+++

+++Jag kan inte se eller öppna mina äldre projekt

1. Du kan bara se projekt som har skapats med ditt Adobe Learning Manager-konto på samma dator som de skapades på.
1. Återställ programpreferenserna och starta sedan om datorprogrammet Adobe Learning Manager och försök igen. Mer hjälp finns i [Så här återställer du programinställningarna](#howtoresetapplicationpreferences).
1. Aktivera avancerad loggning om fel uppstår när projekt öppnas. Mer information finns i [Aktivera avancerad loggning](#howtoenableadvancedlogging). Starta om skrivbordsprogrammet Adobe Learning Manager och gör om stegen som orsakar felet. Skicka de senaste programloggarna till din Adobe Learning Manager-administratör för att få hjälp. Mer information finns i [Hitta programloggar](#howtofindapplicationlogs).

+++

## Hur återställer man programpreferenserna? {#howtoresetapplicationpreferences}

### Windows {#windows}

1. Om du vill öppna dialogrutan Kör trycker du på **Windows + R** nycklar.
1. Text `**%APPDATA%\\..\\Local\\Adobe\\Learning Manager 1.0**` och tryck på Retur.
1. Ta bort filerna som heter **preferences.json** och **preferences.xml**.

### MAC OS X {#macosx}

1. Öppna Finder.
1. Så här öppnar du **Gå till** mappdialogruta, tryck på **cmd + skift + G** nycklar.
1. Text `**~/Library/Application Support/Adobe/Learning Manager 1.0**` och tryck på Retur.
1. Ta bort filerna som heter **preferences.json** och **preferences.xml**.

## Hur hittar jag programloggar? {#howtofindapplicationlogs}

### Windows {#application-logs}

1. Om du vill öppna dialogrutan Kör trycker du på **Windows + R** nycklar.
1. Text `**%TEMP%\\elthor**` och tryck på Retur.
1. Sortera mapparna efter **Ändrad den** och öppna den senaste mappen. Den här mappen innehåller de senaste programloggarna.

### MAC OS X {#MacOSX-1}

1. Öppna **Finder**.
1. Så här öppnar du **Gå till mapp** dialogrutan trycker du på **cmd + skift + G** nycklar.
1. Skriv &quot;**/var/folders**&quot; (utan citattecken) och tryck på Retur.
1. Sök efter **elthor**&quot; i sökfältet och öppna mappen.
1. Sortera mapparna efter **Ändrat datum** och öppna den senaste mappen. Den här mappen innehåller de senaste programloggarna.

## Hur aktiverar jag avancerad loggning? {#howtoenableadvancedlogging}

### Windows {#Windows-1}

1. Om du vill öppna dialogrutan Kör trycker du på **Windows-tangenten + R**.****
1. Skriv &quot;**%APPDATA%\\..\\Local\\Adobe\\Learning Manager 1.0**&quot; (utan citattecken) och tryck på Retur.****
1. Ta en säkerhetskopia av filen **preferences.json** och öppna den sedan i en textredigerare.****
1. Sök efter nyckeln **debugMode** och ändra egenskapen value för den här nyckeln till &quot;**sann**&quot; (utan citattecken).

### MAC OS X {#MacOSX-2}

1. Öppna Finder.
1. Så här öppnar du **Gå till mapp** dialogruta, tryck på **cmd + skift + G**.
1. Skriv &quot;**~/Library/Application Support/Adobe/Learning Manager 1.0**&quot; (utan citattecken) och tryck på Retur.
1. Ta en säkerhetskopia av filen **preferences.json** och öppna den sedan i en textredigerare.
1. Sök efter nyckeln **debugMode** och ändra egenskapen value för den här nyckeln till &quot;**sann**&quot; (utan citattecken)

## Hur ställer du in behörighet för webbkamera/mikrofon på Mac OS X Mojave? {#howtosetwebcammicrophonepermissionsonmacosxmojave}

1. Klicka **[!UICONTROL System Preferences]** ikonen i Dock.
1. Klicka **[!UICONTROL Security & Privacy]** > **[!UICONTROL Privacy].**
1. Klicka **[!UICONTROL Webcam and Microphone options]** och se till att kryssrutan Adobe Learning Manager är markerad. Om du inte ser Adobe Learning Manager i listan ska du först installera och starta datorprogrammet Adobe Learning Manager.

## Hur rensar man cachen för uppdateringar av Adobe Learning Manager för dator? {#howtocleanupadobecaptivateprimefordesktopupdatescache}

### Windows {#clean-previous-installation}

1. Om du vill öppna dialogrutan Kör trycker du på **Windows-tangenten + R**.
1. Text `**%APPDATA%\\..\\Local\\Adobe\\Learning Manager 1.0**` och tryck på Retur.
1. Ta bort mappen som heter **uppdateringar**.

### MAC OS X {#MacOSX-3}

1. Öppna Finder.
1. Så här öppnar du **Gå till mapp** dialogruta, tryck på **cmd + skift + G**.
1. Text `**~/Library/Application Support/Adobe/Learning Manager 1.0**` och tryck på Retur.
1. Ta bort mappen som heter **uppdateringar**.

## Hur rensar man den temporära mappen för Adobe Learning Manager för dator? {#howtocleanupadobecaptivateprimefordesktoptempfolder}

### Windows {#clean-previous-installation-1}

1. Om du vill öppna dialogrutan Kör trycker du på **Windows-tangenten + R**.
1. Skriv &quot;**%TEMP%**&quot; (utan citattecken) och tryck på Retur.
1. Ta bort mappen som heter **elthor**&quot;.

### MAC OS X {#MacOSX-4}

1. Öppna Finder.
1. Så här öppnar du **Gå till mapp** dialogruta, tryck på **cmd + skift + G** nycklar.
1. Skriv &quot;**/var/folders**&quot; (utan citattecken) och tryck på Retur.
1. Sök efter **elthor**&quot; i sökfältet.
1. Ta bort mappen som heter **elthor**&quot;.

## Hur hittar jag Adobe Learning Manager för datorprojekt? {#howtolocateadobecaptivateprimefordesktopprojects}

### Windows {#Windows-2}

1. Om du vill öppna dialogrutan Kör trycker du på **Windows-tangenten + R**.
1. Skriv &quot;**~/DOCUMENTS/MY Adobe LEARNING MANAGER PROJECTS**&quot; (utan citattecken) och tryck på Retur.
1. Du eller din Adobe Learning Manager-administratör kan ha ändrat standardprojektmappens plats. Kontakta administratören för mer hjälp med att hitta och rensa projekt.

### MAC OS X {#MacOSX-5}

1. Öppna Finder.
1. Så här öppnar du **Gå till mapp** dialogruta, tryck på **cmd + skift + G** nycklar.
1. Skriv &quot;**~/DOCUMENTS/MY Adobe LEARNING MANAGER PROJECTS**&quot; (utan citattecken) och tryck på Retur.

   Du eller din Adobe Learning Manager-administratör kan ha ändrat standardprojektmappens plats. Kontakta administratören för mer hjälp om hur du lokaliserar och rensar projekt.

## Hur rensar man tidigare installationer av Adobe Learning Manager-datorprogram? {#howtocleanuppreviousinstallationsofadobelearningmanagerdesktopapp}

### Windows {#Windows-3}

1. Så här öppnar du **Kör dialog,** pressa **Windows-tangenter + R**.
1. Skriv regedit och sök &quot;**HKEY_LOCAL_MACHINE \\SOFTWARE\\Classes\\Installer\\**&quot; (utan citattecken) eller &quot;**HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Installer\\UserData\\S-1-5-18\\Products\\**&quot; (utan citattecken) och tryck på Retur.
1. Sök efter mappen Adobe Learning Manager och hitta den tidigare installationen. Ta bort registerposten.  Du hittar tangenten genom att trycka på F3.

### MAC OS X {#MacOSX-6}

Flytta filerna från följande sökväg **/Applications/Adobe Learning Manager/Users/Shared/Adobe/Learning Manager Assets/1.0**&quot; till papperskorgen och töm sedan papperskorgen.
