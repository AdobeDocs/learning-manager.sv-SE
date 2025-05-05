---
description: Det här dokumentet innehåller grundläggande felsökningstips för att lösa några av de vanligaste problemen vid installation och användning av Adobe Learning Manager-datorprogrammet.
jcr-language: en_us
title: Felsöka problem med Adobe Learning Manager-datorprogrammet
contentowner: kuppan
exl-id: 68d40a52-e048-43af-a7aa-917b569b583d
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '1434'
ht-degree: 0%

---

# Felsöka problem med Adobe Learning Manager-datorprogrammet

Det här dokumentet innehåller grundläggande felsökningstips för att lösa några av de vanligaste problemen vid installation och användning av Adobe Learning Manager-datorprogrammet.

## Jag kan inte göra följande {#iamunabletodothefollowing}

+++Jag kan inte hämta Adobe Learning Manager-datorprogrammet

1. Kontrollera inställningarna för internetanslutningen och brandväggen.
1. Klicka på **[!UICONTROL New Post]** i Social utbildning för att skapa ett inlägg. Om du inte har någon anslagstavla ska du skapa en anslagstavla först.
1. Klicka på något av följande alternativ för inläggsknappar som visas för att skapa innehåll som Screen Shot, Record Audio, Record Video, Learning Manager Gallery. Du omdirigeras till sidan för Adobe Learning Manager-datorprogrammet där du kan hämta Adobe Learning Manager-datorprogrammet för datorn.
1. Du måste ha ett giltigt Adobe Learning Manager-konto där Social utbildning är aktiverat av administratören. Din administratör kan också ha inaktiverat hämtningar via webbläsaren. Kontakta Adobe Learning Manager-administratören för mer information om hur du hämtar Adobe Learning Manager-datorprogrammet.

+++

+++Jag kan inte installera Adobe Learning Manager-datorprogrammet

1. Se till att systemet uppfyller de lägsta systemkraven. Se [Systemkrav för Adobe Learning Manager-datorprogrammet](../learners/adobe-learning-manager-app-for-desktop/adobe-learning-manager-desktop-app-system-requirements.md).
1. Rensa tidigare installationer av Adobe Learning Manager-datorprogram. Mer information finns i [Rensa tidigare installationer](#howtocleanuppreviousinstallationsofadobelearningmanagerdesktopapp) för mer information.
1. Information om fel under installationsprocessen finns i [Så här hittar du programloggar](#howtofindapplicationlogs). Kontakta administratören för Adobe Learning Manager-datorprogrammet för mer hjälp.

+++

+++Jag kan inte starta Adobe Learning Manager-datorprogrammet

1. Kontrollera att Adobe Learning Manager-datorprogrammet är hämtat och installerat.
1. Klicka på **[!UICONTROL New Post]** i Social utbildning (om du inte har en anslagstavla skapar du en anslagstavla). Klicka på något av följande alternativ för inläggsknappar som visas - Ta en skärmbild, Ljudinspelning, Videoinspelning, Adobe Learning Manager Gallery. Du omdirigeras till en sida där du kan starta Adobe Learning Manager-datorprogrammet.
1. Om appen inte startar kan du också starta den från Start-menyn i Windows eller från Launchpad i Mac OS X.

+++

+++Jag kan inte logga in på mitt konto i Adobe Learning Manager-datorprogrammet

1. Se till att du är ansluten till internet och att brandväggsinställningarna inte blockerar Adobe Learning Manager-datorprogrammet.
1. Se till att du har ett giltigt Adobe Learning Manager-elevkonto med Social utbildning aktiverat.
1. Om du fortfarande inte kan logga in avslutar och startar du om Adobe Learning Manager-datorprogrammet och försöker sedan igen.
1. Kontakta Adobe Learning Manager-administratören om du behöver mer hjälp.

+++

+++Jag kan inte se min webbkamera/mikrofon i Adobe Learning Manager-datorprogrammet

1. Kontrollera att webbkameran/mikrofonen är korrekt ansluten till systemet och fungerar som den ska.
1. Kontrollera att du har installerat de senaste drivrutinerna för webbkameran/mikrofonen. Vissa enheter fungerar inte som de ska utan dedikerade drivrutiner.
1. Återställ programpreferenserna och starta sedan om Adobe Learning Manager-datorprogrammet och försök igen. Mer information finns i [Så här återställer du programinställningarna](#howtoresetapplicationpreferences).
1. Om du använder Mac OS X Mojave 10.14 kan du bevilja behörigheter till Adobe Learning Manager-datorprogrammet för att få åtkomst till webbkameran/mikrofonen. Mer information finns i [Så här anger du behörigheter för webbkamera/mikrofon i OSX Mojave](#howtosetwebcammicrophonepermissionsonMacOSXMojave).

+++

+++Jag kan inte publicera mina inlägg från Adobe Learning Manager-datorprogrammet

1. Se till att du har ett giltigt Adobe Learning Manager-elevkonto med Social utbildning aktiverat av Adobe Learning Manager-administratören.
1. Återställ programpreferenserna och starta sedan om Adobe Learning Manager-datorprogrammet och försök igen. Mer information finns i [Så här återställer du programinställningarna](#howtoresetapplicationpreferences).
1. Aktivera avancerad loggning vid fel i publiceringen. Mer information finns i [Så här aktiverar du avancerad loggning](#howtoenableadvancedlogging), startar om Adobe Learning Manager-datorprogrammet och gör om stegen ovan som orsakar felet. Skicka de senaste programloggarna till Adobe Learning Manager-administratören för hjälp. Mer information finns i [Hitta programloggar](#howtofindapplicationlogs).

+++

+++Jag kan inte se eller öppna mina äldre projekt

1. Du kan bara se projekt som har skapats med ditt Adobe Learning Manager-konto på samma dator som de skapades på.
1. Återställ programpreferenserna och starta sedan om Adobe Learning Manager-datorprogrammet och försök igen. Se [Så här återställer du programinställningarna](#howtoresetapplicationpreferences) om du vill ha hjälp.
1. Aktivera avancerad loggning om fel uppstår när projekt öppnas. Mer information finns i [Aktivera avancerad loggning](#howtoenableadvancedlogging). Starta om Adobe Learning Manager-datorprogrammet och gör om stegen som orsakar felet. Skicka de senaste programloggarna till Adobe Learning Manager-administratören för hjälp. Mer information finns i [Hitta programloggar](#howtofindapplicationlogs).

+++

## Hur återställer man programpreferenserna? {#howtoresetapplicationpreferences}

### Windows {#windows}

1. Tryck på **Windows + R** för att öppna dialogrutan Kör.
1. Skriv `**%APPDATA%\\..\\Local\\Adobe\\Learning Manager 1.0**` och tryck på Enter.
1. Ta bort filerna **preferences.json** och **preferences.xml**.

### MAC OS X {#macosx}

1. Öppna Finder.
1. Om du vill öppna dialogrutan **Gå till**-mappen trycker du på **Cmd + Skift + G**.
1. Skriv `**~/Library/Application Support/Adobe/Learning Manager 1.0**` och tryck på Enter.
1. Ta bort filerna **preferences.json** och **preferences.xml**.

## Hur hittar jag programloggar? {#howtofindapplicationlogs}

### Windows {#application-logs}

1. Du öppnar dialogrutan Kör genom att trycka på **Windows + R**.
1. Skriv `**%TEMP%\\elthor**` och tryck på Enter.
1. Sortera mapparna efter **ändringsdatum** och öppna den senaste mappen. Den här mappen innehåller de senaste programloggarna.

### MAC OS X {#MacOSX-1}

1. Öppna **Finder**.
1. Om du vill öppna dialogrutan **Gå till mapp** trycker du på **Kommando + Skift + G**.
1. Skriv **/var/folders** (utan citattecken) och tryck på Retur.
1. Sök efter &quot;**elthor**&quot; i sökfältet och öppna mappen.
1. Sortera mapparna efter **Ändrat datum** och öppna den senaste mappen. Den här mappen innehåller de senaste programloggarna.

## Hur aktiverar jag avancerad loggning? {#howtoenableadvancedlogging}

### Windows {#Windows-1}

1. Om du vill öppna dialogrutan Kör trycker du på **Windows-tangenten + R**.**&#x200B;**
1. Skriv &quot;**%APPDATA%\\..\\Local\\Adobe\\Learning Manager 1.0**&quot; (utan citattecken) och tryck på Retur.**&#x200B;**
1. Säkerhetskopiera filen **preferences.json** och öppna den sedan i en textredigerare.**&#x200B;**
1. Sök efter nyckeln **debugMode** och ändra den här nyckelns värdeegenskap till **true** (utan citattecken).

### MAC OS X {#MacOSX-2}

1. Öppna Finder.
1. Om du vill öppna dialogrutan **Gå till mapp** trycker du på **Cmd + Skift + G**.
1. Skriv **~/Library/Application Support/Adobe/Learning Manager 1.0** (utan citattecken) och tryck på Retur.
1. Säkerhetskopiera filen **preferences.json** och öppna den sedan i en textredigerare.
1. Sök efter nyckeln **debugMode** och ändra den här nyckelns värdeegenskap till **true** (utan citattecken)

## Hur ställer du in behörighet för webbkamera/mikrofon på Mac OS X Mojave? {#howtosetwebcammicrophonepermissionsonmacosxmojave}

1. Klicka på ikonen **[!UICONTROL System Preferences]** i Dock.
1. Klicka på **[!UICONTROL Security & Privacy]** > **[!UICONTROL Privacy].**
1. Klicka på **[!UICONTROL Webcam and Microphone options]** och se till att Adobe Learning Manager är markerat. Om Adobe Learning Manager inte visas installerar och startar du först Adobe Learning Manager-datorprogrammet.

## Hur rensar jag cachen för Adobe Learning Manager-uppdateringar för dator? {#howtocleanupadobecaptivateprimefordesktopupdatescache}

### Windows {#clean-previous-installation}

1. Tryck på **Windows-tangenten + R** för att öppna dialogrutan Kör.
1. Skriv `**%APPDATA%\\..\\Local\\Adobe\\Learning Manager 1.0**` och tryck på Enter.
1. Ta bort mappen **updates**.

### MAC OS X {#MacOSX-3}

1. Öppna Finder.
1. Om du vill öppna dialogrutan **Gå till mapp** trycker du på **Cmd + Skift + G**.
1. Skriv `**~/Library/Application Support/Adobe/Learning Manager 1.0**` och tryck på Enter.
1. Ta bort mappen **updates**.

## Hur rensar man den temporära mappen för Adobe Learning Manager för datorer? {#howtocleanupadobecaptivateprimefordesktoptempfolder}

### Windows {#clean-previous-installation-1}

1. Tryck på **Windows-tangenten + R** för att öppna dialogrutan Kör.
1. Skriv &quot;**%TEMP%**&quot; (utan citattecken) och tryck på Retur.
1. Ta bort mappen **elthor**.

### MAC OS X {#MacOSX-4}

1. Öppna Finder.
1. Om du vill öppna dialogrutan **Gå till mapp** trycker du på **Cmd + Skift + G**.
1. Skriv **/var/folders** (utan citattecken) och tryck på Retur.
1. Sök efter &quot;**elthor**&quot; i sökfältet.
1. Ta bort mappen **elthor**.

## Hur hittar jag Adobe Learning Manager för datorprojekt? {#howtolocateadobecaptivateprimefordesktopprojects}

### Windows {#Windows-2}

1. Tryck på **Windows-tangenten + R** för att öppna dialogrutan Kör.
1. Skriv **~/Documents/My Adobe Learning Manager Projects** (utan citattecken) och tryck på Retur.
1. Du eller din Adobe Learning Manager-administratör kan ha ändrat standardprojektmappens plats. Kontakta administratören för mer hjälp med att hitta och rensa projekt.

### MAC OS X {#MacOSX-5}

1. Öppna Finder.
1. Om du vill öppna dialogrutan **Gå till mapp** trycker du på **Cmd + Skift + G**.
1. Skriv **~/Documents/My Adobe Learning Manager Projects** (utan citattecken) och tryck på Retur.

   Du eller din Adobe Learning Manager-administratör kan ha ändrat standardprojektmappens plats. Kontakta administratören för mer hjälp om hur du lokaliserar och rensar projekt.

## Hur rensar jag tidigare installationer av Adobe Learning Manager-datorprogrammet? {#howtocleanuppreviousinstallationsofadobelearningmanagerdesktopapp}

### Windows {#Windows-3}

1. Om du vill öppna dialogrutan **Kör ska du** trycka på&#x200B;**Windows-tangenterna + R**.
1. Skriv regedit och sök efter &quot;**HKEY_LOCAL_MACHINE \\SOFTWARE\\Classes\\Installer\\**&quot; (utan citattecken) eller &quot;**HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Installer\\UserData\\S-1-5-18\\Products\\**&quot; (utan citattecken) och tryck på Retur.
1. Leta reda på mappen Adobe Learning Manager och den tidigare installationen. Ta bort registerposten.  Du hittar tangenten genom att trycka på F3.

### MAC OS X {#MacOSX-6}

Flytta filerna från följande sökväg: **/Applications/Adobe Learning Manager/Users/Shared/Adobe/Learning Manager Assets/1.0** till papperskorgen och töm den sedan.
