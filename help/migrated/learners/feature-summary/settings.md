---
description: Läs den här artikeln för att lära dig hur du anger elevprofilinställningar och lägger till ett profilfoto. Lär dig ladda ner elevens betygsutdrag för din profil.
jcr-language: en_us
title: Profilinställningar
contentowner: manochan
source-git-commit: a495c86f8dff3ebc51e7700a3f3bcf7ce57d1311
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

---



# Profilinställningar

Läs den här artikeln för att lära dig hur du anger elevprofilinställningar och lägger till ett profilfoto. Lär dig ladda ner elevens betygsutdrag för din profil.

## Konfigurera profilinställningar {#configuringprofilesettings}

1. Klicka på nedrullningspilen bredvid din profil eller foto längst upp till höger på sidan.
1. Välj Profilinställningar.
1. Du kan utföra följande åtgärder i popup-dialogrutan som visas:

   * Lägg till/uppdatera profilfoto: Håll pekaren över fotot. Klicka på Överför och lägg till ett foto. Klicka på Redigera för att ändra fotot.
   * Ta bort foto: håll pekaren över profilfotot. Klicka på Ta bort.
   * Lägg till Om mig-innehåll genom att klicka i textområdet under det.
   * Ändra Om mig-innehåll genom att klicka på Redigera bredvid fältet.
   * Ange språkinställning för din profil. I listrutan Språk väljer du önskat språk.
   * Ställ in aktuell språkinställning för din profil.
   * Ange tidszonen för din profil.
   * Ladda ned elevens betygsutdrag med dina data.

   ![](assets/learner-preferences.png)
   *Visa elevpreferenser*

   När du klickar på länken Hämta mitt utbildningsutdrag XLS hämtas ett Excel-ark till systemet. Detta Excel-ark innehåller information om de utbildningsobjekt som du förbrukar, slutförandestatus för varje utbildningsobjekt, motsvarande förfallodatum, uppnådda kompetenser osv. Hämta det här bladet för att snabbt få övergripande data för din utbildningsprofil.

1. Om en administratör har aktiverat Sammandrag av e-post och du inte finns med på DND-listan kan du prenumerera eller avbryta prenumerationen på sammandrag av e-post. Aktivera alternativet nedan.

   ![](assets/digest-email-option-learner.png)
   *Prenumerera eller avbryt prenumerationen på sammanfattningsmeddelanden*

   Beroende på vilken frekvens som angetts av administratören får du, eleven får e-postmeddelandet varannan vecka eller varje månad.

## Avsluta prenumerationen på sammanfattningsmeddelanden {#unsubscribefromdigestemails}

När du får ett e-postmeddelande kan du avregistrera dig från prenumerationen genom att klicka på **Avsluta prenumerationen** -länken längst ned i e-postmeddelandet.

När du har klickat **[!UICONTROL Unsubscribe]**, du omdirigeras till din **Profilinställningar** där du kan inaktivera alternativet att ta emot e-postmeddelanden.

## Anatomi för ett sammanfattningsmeddelande {#anatomyofadigestemail}

Ett sammanfattningsmeddelande består av följande avsnitt:

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Avsnitt</b></p></td>
   <td>
    <p><b>Beskrivning</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Sammanfattning av personlig utbildning</p></td>
   <td>
    <p>I det här avsnittet anpassas en elevs utbildningsstatistik genom att antalet minuter som ägnas åt utbildningar anges.</p>
    <p>Baserat på den tid som eleven lagt ner anpassas innehållet enligt reglerna som definieras nedan:</p>
    <p>Om (time_sent) &gt;= 60 minuter visas följande text:</p>
    <p><i>"Under de senaste två veckorna/en månad har du tagit <b>(tid_förbrukad)</b> minuter av utbildning för att vidareutbilda dig. Nedan följer några rekommendationer som hjälper dig att lära dig mer." </i></p>
    <p> Om (time_spending) &lt; 60 min visas följande text:</p>
    <p><i>"Under de senaste två veckorna/en månad har du tagit <b>(tid_förbrukad)</b> minuter av utbildning för att vidareutbilda dig. Nedan följer några rekommendationer som vi hoppas att du kan ha nytta av för att komma igång och fortsätta."</i></p></td>
  </tr>
  <tr>
   <td>
    <p>Utbildningsaktivitet</p></td>
   <td>
    <p>Det här avsnittet visar sammanfattningen av utbildningsaktiviteten på organisationsnivå för det kontot.</p>
    <p>Sammanfattningen av utbildningsaktiviteten består av följande: </p>
    <ul>
     <li>Antal utbildningar som är tillgängliga på kontot.</li>
     <li>Antal medelever som aktivt har fullföljt utbildningsaktiviteterna.</li>
     <li>Antal utbildningstimmar som arbetskollegorna tillbringat.</li>
     <li>Genomsnittlig tid (i minuter) som kollegor lagt ned på att förkovra sig på kontot.</li>
    </ul></td>
  </tr>
  <tr>
   <td>
    <p>Rekommenderade kurser</p></td>
   <td>
    <p>Det här är ett anpassat avsnitt som innehåller de rekommenderade utbildningarna för elever. I det här avsnittet kan en elev se tre utbildningar som valdes ut av rekommendationsmotorn.</p>
    <p>Varje utbildning har en Utforska-knapp som omdirigeras till elevappens startsida när du klickar på den.  </p></td>
  </tr>
  <tr>
   <td>
    <p>Resultattavla</p></td>
   <td>
    <p>Visar ett stapeldiagram där varje stapel representerar en elev tillsammans med spelifieringspunkter för varje elev (endast om administratören har aktiverat spelifiering för alla elever).</p>
    <p>Resultattavlan visar följande:</p>
    <ul>
     <li>Poäng som en elev tjänat in.</li>
     <li>Poäng som behövs för att nå nästa nivå.</li>
    </ul>
    <p>Det finns också en mini resultattavla som visar ledaren, och två elever närmast eleven i detta användaromfång.</p>
    <p>Om resultatlistan är tom visas inte det här avsnittet i e-postmeddelandet.</p></td>
  </tr>
  <tr>
   <td>
    <p><a>Sociala inlägg</a></p></td>
   <td>
    <p>Det här avsnittet visar de tre senaste sociala inläggen.</p>
    <p>En elev kan se datumet för skapandet, tavlans namn, titeln på inlägget om det finns, användarnamn och ikonen för skaparen. Inlägget kan också innehålla en video, ett dokument, en pdf eller någon annan fil.</p>
    <p>Varje inlägg har länkar som dirigerar om eleven till sidan för social utbildning i elevappen.</p>
    <p>Om det inte finns några nya inlägg kommer det här avsnittet i e-postmeddelandet inte att vara synligt för eleven.</p></td>
  </tr>
 </tbody>
</table>

## Vanliga frågor {#frequentlyaskedquestions}

**1). Hur laddar man ner en elevs betygsutdrag som elev?**

I det övre högra hörnet klickar du på **[!UICONTROL user profile]** > **[!UICONTROL Profile Settings]**. Klicka på i dialogrutan som visas **Hämta mitt utbildningstranskribering (XLS)**.

![](assets/dowload-lt.png)
*Ladda ned elevens betygsutdrag*
