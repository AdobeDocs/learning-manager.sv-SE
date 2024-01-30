---
jcr-language: en_us
title: Tillgänglighet i Adobe Learning Manager
description: I det här dokumentet beskrivs tillgänglighetsstödet i Learning Manager Learning Management System för elever med funktionshinder. Den förser även användarna med navigeringsalternativ och tillgänglighetsfunktioner på plattformen.
contentowner: saghosh
preview: true
source-git-commit: 92b3c83ec04de927f9066db6b79e8b19872d2b46
workflow-type: tm+mt
source-wordcount: '932'
ht-degree: 0%

---



# Tillgänglighet i Adobe Learning Manager

I det här dokumentet beskrivs tillgänglighetsstödet i Learning Manager Learning Management System för elever med funktionshinder. Den förser även användarna med navigeringsalternativ och tillgänglighetsfunktioner på plattformen.

Learning Manager följer W3C:s WCAG 2.1 Level A- och AA-tillgänglighetsstandarder för plattformen.

Med elevrollen Adobe Learning Manager kan elever navigera på plattformen och dra nytta av följande viktiga tillgänglighetsfunktioner:

* Raster Reader
* Tangentbord
* Undertexter
* Annat

## Stöd för Screen Reader {#supportforscreenreaders}

Adobe Learning Manager stöder skärmläsare som NVDA, JAWS och Voice-over på dator, Talkback och Voice-over på mobil, vilket gör det möjligt för elever att läsa upp texten på Learning Manager-plattformen och navigera därefter.

Här är den kombination av skärmläsare och webbläsare som vi stöder på datorn:

<table> 
 <tbody>
  <tr> 
   <td><p style="text-align: left;"><b>Operativsystem</b></p></td> 
   <td><p style="text-align: left;"><b>Webbläsare</b></p></td> 
   <td><p style="text-align: left;"><b>Skärmläsare</b></p></td> 
  </tr> 
  <tr> 
   <td><p>Windows</p></td> 
   <td><p>Krom</p></td> 
   <td><p>NVDA</p></td> 
  </tr> 
  <tr> 
   <td><p>Windows</p></td> 
   <td><p>Firefox</p></td> 
   <td><p>Käftar</p></td> 
  </tr> 
  <tr> 
   <td><p>macOS</p></td> 
   <td><p>Safari</p></td> 
   <td><p>VoiceOver</p></td> 
  </tr> 
  <tr> 
   <td><p>Android</p></td> 
   <td><p>Krom</p></td> 
   <td><p>Talkback</p></td> 
  </tr> 
  <tr> 
   <td><p>iOS</p></td> 
   <td><p>Safari</p></td> 
   <td><p>VoiceOver</p></td> 
  </tr> 
 </tbody>
</table>

## Stöd för tangentbordsnavigering {#supportforkeyboardnavigation}

Elever kan använda standardnycklar för att navigera på sidorna med eller utan skärmläsare. Det hjälper elever att navigera bland elementen på sidan och läsa innehållet med en skärmläsare.

Dessutom stöder Learning Manager följande kortkommandon:

<table> 
 <tbody>
  <tr> 
   <td><p><b>Funktion</b></p></td> 
   <td><p><b>Windows</b></p></td> 
   <td><p><b>macOS</b></p></td> 
  </tr> 
  <tr> 
   <td><p>Hoppa över navigering</p></td> 
   <td><p>Alt+1</p></td> 
   <td><p>Alt+1</p></td> 
  </tr> 
  <tr> 
   <td><p>Funktion<br></p></td> 
   <td><p>Windows<br></p></td> 
   <td><p>macOS<br></p></td> 
  </tr> 
  <tr> 
   <td><p>Användarmeddelande<br></p></td> 
   <td><p>Alt+2<br></p></td> 
   <td><p>Alt+2<br></p></td> 
  </tr> 
  <tr> 
   <td><p>Profilinställningar<br></p></td> 
   <td><p>Alt+3<br></p></td> 
   <td><p>Alt+3<br></p></td> 
  </tr> 
  <tr> 
   <td><p>Global sökning<br></p></td> 
   <td><p>Alt+4<br></p></td> 
   <td><p>Alt+4<br></p></td> 
  </tr> 
  <tr> 
   <td><p>Hoppa över navigering<br></p></td> 
   <td><p>Alt+1<br></p></td> 
   <td><p>Alt+1<br></p></td> 
  </tr> 
 </tbody>
</table>

## Spelarkontroller

<table> 
 <tbody>
  <tr> 
   <td><p><b>Funktion</b></p></td> 
   <td><p><b>Windows</b></p></td> 
   <td><p><b>macOS</b></p></td> 
  </tr> 
  <tr> 
   <td><p>Spela upp/pausa</p></td> 
   <td><p>Alt+P</p></td> 
   <td><p>Alternativ+P</p></td> 
  </tr> 
  <tr> 
   <td><p>Alt+V</p></td> 
   <td><p>Alternativ+V</p></td> 
   <td><p>Volym</p></td> 
  </tr> 
  <tr> 
   <td><p>Alt+M</p></td> 
   <td><p>Alt+M</p></td> 
   <td><p>Helskärm</p></td> 
  </tr> 
 </tbody>
</table>

## Annat stöd {#supportforcolorcontrast}

Utbildningsrollen för Learning Manager stöder flera andra tillgänglighetsfunktioner, däribland:

1. Semantisk struktur till elevens rollsidor, inklusive rubrik, listmarkering, beskrivande titlar osv. tillhandahålls.
1. Stöd för webbläsarzoomning upp till 200 % utan förlust av innehåll eller funktionalitet bibehålls genom elevrollen.
1. Färgkontrast för text- och icke-textelement behålls i elevrollen. Använd kommandot [Klart](/help/migrated/administrators/feature-summary/themes.md) tema.
1. Stöd för W3C:s WAI ARIA-designmönster för att upprätthålla konsekvens och bästa praxis i branschen.

Mer information finns i:

* [Rapport om tillgänglighetsöverensstämmelse för en elev](https://www.adobe.com/accessibility/compliance/adobe-captivate-prime-web-2019-learner-portal-acr.html)
* [Rapport om tillgänglighetsöverensstämmelse för alla roller](https://www.adobe.com/accessibility/compliance/adobe-captivate-prime-web-2019-acr.html)

## De viktigaste arbetsflödena för Learning Manager (elevroll) {#captivateprimetopworkflowslearnerrole}

Låt oss titta på hur tillgänglighetsfunktioner hjälper dig att navigera bland några viktiga funktioner för elever i Learning Manager.

Använd kommandot `kbd Tab`för att navigera bland elementen på sidan. Använd kommandot `kbd Shift + Tab` för att vända navigeringsriktningen. Tangentbordsfokus anges med en blå kontur som visas runt ett element. En skärmläsare bör läsa upp texten för elementet i fråga.

## Sök efter en utbildning i Learning Manager {#searchforatrainingincaptivateprime}

1. Använd dessa tips för att navigera och nå sökrutan i det övre högra hörnet av startsidan.
1. Skriv texten med tangentbordet. Sökresultatet visas.
1. Använda tangentbordet `kbd Up/Down` pilar för att navigera genom resultaten eller träffen `kbd ENTER`om du vill visa alla resultat.

1. När utbildningen har identifierats, träffa `kbd ENTER`för att gå till utbildningssidan.

## Genomför en utbildning i Adobe Learning Manager {#consumeatraininginadobecaptivateprime}

1. När en utbildning har identifierats ska du `kbd Tab`eller `kbd Shift + Tab` för att navigera till knappen Registrera dig/Starta. Knappstatus beror på din registreringsstatus för den utbildningen.

1. Träff `kbd ENTER`för att påbörja utbildningen.
1. Detta är de kontroller som visas oberoende av innehållstyp:

   * Innehållsförteckning
   * Anteckningar
   * Spela upp/Pausa
   * Helskärm
   * Stäng-knapp
   * Inställningar
   * Etikett för modulnamn

1. Följande kontroller visas baserat på innehållstypen:

   * Videoinnehåll - framåt, bakåt, reglage.
   * DOKUMENTINNEHÅLL - SIDNUMMER, UPPÅT, NEDÅT, ZOOMA IN, ZOOMA UT.
   * eLEARNING - knapp för undertext.

1. Tryck på tangentbordskontroller `kbd Tab`eller `kbd Shift + Tab` för att navigera mellan kontrollerna och träffa `kbd ENTER`för att aktivera/inaktivera en kontroll.

1. För DOKUMENTTYP använder du pilkontroller som `kbd UP/DOWN` för att bläddra igenom dokumentet.

## Tillgänglighetsstöd för specifika behov

Låt oss titta på de tillgänglighetsfunktioner som elever kan använda baserat på sina specifika behov.

### Användare som är döva eller hör dåligt

* Använd undertexter som är tillgängliga i material som har skapats med Adobe Captivate-utvecklingsverktyget.
* För videor kan författare koda videorna med text med stängd bildtext. Sådana videor har inbäddade undertexter och kan konsumeras av eleverna.
* Learning Manager stöder möjligheten att ladda upp WebVTT-filer med stängd bildtext för videoinnehåll. Mer information finns i  [*Överför WebVTT-fil för textning till hörselskadade*](/help/migrated/authors/feature-summary/content-library.md).

### Blinda eller synskadade användare

* Använd de vanliga kortkommandona och kommandona för att bläddra på sidan.
* Användning av skärmläsare, som nämns ovan, för att läsa upp informationen på webbsidan.
* Användning av skärmförstorare för att zooma skärmen för att förbättra läsbarheten och kan zooma webbläsaren till 200 % för att läsa innehållet.

### Användare som har problem med färg

Elevrollen Adobe Learning Manager strävar efter att ge användarna ett användargränssnitt som är tydligt och läsbart i enlighet med WCAG 2.1-standarder.

För en bättre upplevelse på elevsidan använder du [Klart tema](/help/migrated/administrators/feature-summary/themes.md).

### Användare med begränsad rörlighet och räckvidd

Adobe Learning Manager fortsätter att fokusera på tillgänglighet och har planer på att förbättra de nuvarande funktionerna så att elever i systemet lättare kan navigera genom elevrollen.

### Stöd för dold textning i videor

När du skapar en kurs kan användarna ladda upp webVTT-filer tillsammans med videofilerna. Elever kan sedan visa undertexter när de tittar på videorna.

## Vad som kommer att tas upp i en framtida version {#whatwillbeaddressedinafuturerelease}

* Stöd för textning för hörselskadade för videor. Författare bör ha möjlighet att ladda upp SRT-filer tillsammans med videofilerna. Elever ska kunna se undertexter för videor.
