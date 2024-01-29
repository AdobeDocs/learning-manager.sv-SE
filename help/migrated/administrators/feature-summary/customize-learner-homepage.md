---
jcr-language: en_us
title: Anpassa elevens startsida
description: En administratör kan anpassa elevens startsida och göra den mer modern, innehållsdriven och anpassad för en elev.
contentowner: saghosh
source-git-commit: 2dd741a9e0e49986df34bd415ea57f9e64f3b26a
workflow-type: tm+mt
source-wordcount: '1132'
ht-degree: 0%

---



# Anpassa elevens startsida

## Översikt {#overview}

En administratör kan anpassa elevens startsida och göra den mer modern, innehållsdriven och anpassad för en elev.

Det anpassade tillvägagångssättet erbjuder ett widgetat sätt att bygga en Elevstartsida, som organisationens administratör kan konfigurera i administratörens användargränssnitt på ett WYSIWYG-sätt.

Upplevelsen drivs av en personlig utbildningsrekommendation från en AI-driven algoritm som analyserar innehåll från tredje part för branschens färdigheter, införlivar kollegial aktivitet och elevernas intresseområden med hjälp av explicita och implicita data.

## Konfigurera elevens startsida {#configurethelearnerhomepage}

På fliken **Varumärkning** > **Elevens startsida** kan administratören anpassa startsidan för en elev så att hen ser ett helt förnyat utseende och känsla när hen loggar in i elevappen.

Administratörer kan konfigurera gränssnittet (utseendet och känslan) från Admin-appen (**Varumärkning** > **Elevens startsida** -fliken).

Administratörer kan växla till widgetvyn Immersive UI, anpassa widgetar/funktioner därefter och sedan aktivera det immersiva användargränssnittet.

Inställningen **Elevens startsida** innehåller följande avsnitt:

## Alternativ för uppslukande layout {#immersivelayoutoption}

Om du vill visa layouten för en djup sida aktiverar du alternativet **Integrerande**. Du kan växla det här alternativet i **Varumärkning > Allmänt**.

I tidigare versioner fanns alternativen för elevens startsida i Inställningar.

Här är de alternativ som du kan ange:

**Upplevelser på hemsidan:** Aktivera antingen **Klassisk** eller **Integrerande**. Om du väljer Immersive visas följande alternativ:

* **Utbildningstyp:** Välj endera **Industri** eller **Anpassad**. Anpassade utbildningar skapas internt. Branschanpassade utbildningar inkluderar innehåll från tredjepartsleverantörer.

![](assets/select-homepage-experience.png)

*Ställ in startsidan genom att välja Bransch eller Anpassad*

Alternativet **Låt eleven utforska intresseområden** finns både för klassisk och uppslukande upplevelse.

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Om du väljer Anpassa...</b></p></td>
   <td>
    <p><b>Om du väljer Branschjusterad...</b><br></p></td>
  </tr>
  <tr>
   <td>
    <p>Du kan välja högst ett internt och externt aktivt fält.</p></td>
   <td>
    <p>Du kan välja högst fem och minst ett fält. Som standard används alternativet <b>Profil </b>har markerats.</p></td>
  </tr>
 </tbody>
</table>

Om det finns färre än 1 000 elever betraktas hela kontot som ett enda scope. Detta gäller specifikt för typen Anpassad utbildning. Om kontot har färre än 1 000 användare betraktas det fullständiga kontot som dess omfattning.

>[!NOTE]
>
>Kryssrutan **Utforska färdigheter** har flyttats till Inställningar > Allmänt.

Det här aktiveras och tonas ned om alternativet för fördjupad upplevelse väljs. Den här kryssrutan aktiveras endast för Classic Experience.

![](assets/option-immersive.png)

*Val för klassisk upplevelse*

Den uppslukande layouten är standard för alla nya konton. Layouten styrs av widgetar som en administratör kan aktivera eller inaktivera. Beroende på hur widgetarna är placerade återspeglas detta på elevens startsida.

Här är de widgetar som du kan aktivera/inaktivera.

Du kan förhandsgranska elevgränssnittet innan elevgränssnittet aktiveras.

För befintliga konton är alternativet **Integrerande** kommer att **AV**. Det har aktiverats för nytt konto med Social och Spelifiering PÅ.

![](assets/immersive-layout-widgets.png)

*Förhandsvisa elevgränssnittet*

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Widget</b></p></td>
   <td>
    <p><b>Beskrivning</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Masthead</p></td>
   <td>
    <p><b>Vad är ett Masthead och hur anpassar jag Elevens Masthead? </b><br></p>
    <p>Det är en välkommen banner för elever. Banderollen kan vara en bild eller en video. Du kan rikta in masthead på specifika användargrupper och en elev visar Masthead så fort han/hon landar på hemsidan. En användargrupp kan se flera hero images eller videoklipp enligt den målplan som administratören har angett. </p>
    <p>Så här laddar en administratör upp en banderoll:</p>
    <ol>
     <li>I den vänstra panelen klickar du på <b>Meddelanden</b>.<br></li>
     <li>Klicka på i det övre högra hörnet på sidan <b>Lägg till</b>.</li>
     <li>Från <b>Text </b>listruta, välja <b>Som Masthead</b>.</li>
     <li>Skriv ett meddelande som ska visas i masthead.</li>
     <li>Överför en bild eller video.</li>
     <li>Välj målgrupp. Välj en användargrupp eller utbildning där huvuddokumentet ska visas.</li>
     <li>Spara meddelandet om masthead.</li>
    </ol></td>
  </tr>
  <tr>
   <td>
    <p>Mitt lärande</p></td>
   <td>
    <p>Visar utbildningsobjekten som eleven nyligen besökt. </p></td>
  </tr>
  <tr>
   <td>
    <p>Kalender</p></td>
   <td>
    <p>Visar olika kommande klassrums- och virtuella klassrumsträningar för eleverna per månad. Sådana som eleven kan registrera sig för eller redan har registrerats till visas, inklusive chefsgodkända utbildningar. </p></td>
  </tr>
  <tr>
   <td>
    <p>Spelifiering</p></td>
   <td>
    <p>Visar resultattavlan baserat på utbildningsaktiviteter.</p></td>
  </tr>
  <tr>
   <td>
    <p>Social utbildning</p></td>
   <td>
    <p>Visar aktiviteter och inlägg från användare som tillhör samma användaromfattning som eleven. </p></td>
  </tr>
  <tr>
   <td>
    <p>Rekommenderas av organisationen</p></td>
   <td>
    <p>När den här widgeten är aktiverad rekommenderas utbildningar till specifika användargrupper. Varje användargrupp kan få en eller flera utbildningar som mål och målplanen baseras på en tidsram. <br></p>
    <ul>
     <li>
      <p>För det första: administratören <a href="announcements.md#recommendation">skapar ett meddelande</a> av typ <b>Som rekommendation</b> och väljer sedan ut den utbildning och de grupper som krävs. En elev som tillhör en användargrupp kan se den rekommenderade utbildningen.</p></li>
     <li>
      <p>För det andra kan administratören också avgöra om rekommendationerna börjar gälla omedelbart eller vid ett visst datum.</p></li>
    </ul></td>
  </tr>
  <tr>
   <td>
    <p>Rekommendation baserat på intresseområde</p></td>
   <td>
    <p>Visar utbildningsobjekt baserat på elevens valda intresseområde. Rekommendationen drivs av en maskininlärningsalgoritm.</p></td>
  </tr>
  <tr>
   <td>
    <p>Bläddra efter katalog<br></p></td>
   <td>
    <p>Visar kataloger som paneler på startsidan. </p></td>
  </tr>
  <tr>
   <td>
    <p>Rekommendation baserat på kollegas uppgift<br></p></td>
   <td>
    <p>Visar utbildning baserat på vad en elevs kollegor tar. Detta drivs återigen av en maskininlärningsalgoritm.</p></td>
  </tr>
 </tbody>
</table>

När du har sparat ändringarna återspeglar elevens startsida alla ändringar.

När eleven loggar in i elevappen via en webbläsare kan hen se följande uppslukande layout:

<table>
 <tbody>
  <tr>
   <td>
    <p><strong>Startsida</strong></p><img src="assets/home-page1.png"></td>
   <td>
    <p><strong>Min utbildningslista</strong></p><img src="assets/learning-list.jpg"></td>
   <td>
    <p><strong>Visa katalog</strong></p><img src="assets/catalog-new.jpg"></td>
  </tr>
 </tbody>
</table>

*Visa djup layout för olika avsnitt på startsidan*

## Alternativet Klassisk layout {#classiclayoutoption}

Den användargränssnittslayout som hittills alltid har funnits kallas nu klassisk layout. När du väljer det här alternativet återgår elevens startsida till den klassiska layouten.

![](assets/classic-layout.png)

*Förhandsvisa klassisk layout*

## Konfigurera rekommendationsinställningar {#configurerecommendationsettings}

På **Varumärkning** > **Allmänt** kan du konfigurera rekommendationsomfattningar för interna och externa elever och göra det möjligt för elever att välja färdigheter på elevens startsida.

På fliken **Allmänt** -sidan har du följande alternativ:

<table>
 <tbody>
  <tr>
   <td>
    <p>Organisationsnamn</p></td>
   <td>
    <p>Namnet på organisationen som eleven tillhör.</p></td>
  </tr>
  <tr>
   <td>
    <p>underdomän</p></td>
   <td>
    <p>Organisationens underdomän.</p></td>
  </tr>
  <tr>
   <td>
    <p>Utforma logotyper</p></td>
   <td>
    <p>Så här visas din logotyp och ditt företagsnamn i Learning Manager.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>Teman</p></td>
   <td>
    <p>Temat som tillämpas på Learning Manager.</p></td>
  </tr>
  <tr>
   <td>
    <p>Anpassa</p></td>
   <td>
    <p>Med Adobe Learning Manager kan du anpassa ditt konto för att ge dina användare en rikare upplevelse.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>Elevens startsida</p></td>
   <td>
    <p>Välj endera <b>Klassisk </b>eller <b>Integrerande</b>. Om du väljer Immersive visas andra alternativ.</p></td>
  </tr>
  <tr>
   <td>
    <p>Utbildningstyp<br></p></td>
   <td>
    <p>Välj endera <b>Egen </b>eller <b>Branschanpassad</b>. Om det finns färre än 1 000 elever betraktas hela kontot som ett enda scope. Rekommendationen är baserad på alla elever.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>Inställning av rekommendationsomfattning<br></p></td>
   <td>
    <p>Välj ett eller flera aktiva fält. För <b>Egen</b>, kan du välja högst ett aktivt fält. För <b>Branschanpassad</b>kan du välja högst fem aktiva fält.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>Låt eleven utforska intresseområden</p></td>
   <td>
    <p>Endast för klassisk användning. Välj <b>Ja </b>eller <b>Nej</b>.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>Uppmana användare att välja intresseområden (kompetenser) <br></p></td>
   <td>
    <p>Endast för en uppslukande upplevelse. Välj <b>Ja</b> eller <b>Nej</b>. <br></p></td>
  </tr>
 </tbody>
</table>
