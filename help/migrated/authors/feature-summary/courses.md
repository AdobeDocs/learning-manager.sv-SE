---
description: Läs den här artikeln om du vill lära dig hur du skapar kurser, certifieringar och utbildningsprogram i Learning Manager.
jcr-language: en_us
title: Skapa, ändra och publicera kurser
contentowner: manochan
source-git-commit: 147e9edfe323f3d0851880cd401067daa1cee84f
workflow-type: tm+mt
source-wordcount: '6741'
ht-degree: 0%

---



# Skapa, ändra och publicera kurser

Läs den här artikeln om du vill lära dig hur du skapar kurser, certifieringar och utbildningsprogram i Learning Manager.

Författare kan skapa utbildningsobjekt som kurser, certifieringar och utbildningsplaner. Elever kan nyttja dessa utbildningsobjekt, medan administratörer kan spåra elevernas framsteg.

## Kurser i Learning Manager {#coursesincaptivateprime}

Med Adobe Learning Manager kan författare skapa kurser med hjälp av en eller flera moduler som är relaterade till virtuell träning, självstudier, klassrumsutbildning och aktiviteter. Administratörer kan vidare använda dessa kurser för att skapa kursinstanser, registrera elever, tilldela utmärkelsetecken och aktivera feedback för kurserna. De kan också skapa utbildningsprogram, utbildningsplaner och certifieringar med hjälp av dessa kurser.

Författare kan använda e-utbildningsinnehåll som skapats med vilket e-utbildningsverktyg som helst. Andra kursformat som kan användas är videofiler, PDF, doc, docx, PPT och PPTX.

## Skapa en kurs - grundläggande arbetsflöde {#createacoursebasicworkflow}

Följ stegen nedan för att skapa en kurs:

1. Logga in på Adobe Learning Manager som författare eftersom det bara är författare som har behörighet att skapa kurser. På sidan Komma igång klickar du på **[!UICONTROL Create Courses]**.
1. På fliken **Kursöversikt** -sidan, ange namnet på kursen. Ange nu en kort beskrivning av kursen som visas på kurskortet. Beskrivningen får innehålla högst 140 tecken. Ange sedan den detaljerade översikten för kursen som visas på sidan Kursinformation. Beskrivningen får inte överstiga 1 500 tecken.

   Som författare kan du se beskrivningen av modulerna när du lägger till modulen i en kurs.

1. För att göra din kurs tillgänglig på andra språk klickar du på Lägg till nytt språk från det övre vänstra hörnet på sidan. Välj det eller de språk som du vill göra kursen tillgänglig på. Klicka på **[!UICONTROL Save]**. Mer information finns i [Lägg till innehåll för olika språk](/help/migrated/authors/feature-summary/content-library.md).
1. **Ändra kursinställningar**-

   1. Välj en färdighet för kursen på sidan Kursinställningar. Välj önskad kompetens i listrutan Kompetens. I listrutan Nivå väljer du sedan önskad nivå.
   1. Välj kursfärdigheter, nivå och ange poäng för kompetensen. Lägg till fler kompetenser om det behövs.
   1. Från **Registreringstyp** Välj typ av registrering i listrutan.

   Följande typer av registreringar finns:

   * **Nominerad från chef:** Endast chefer kan nominera dessa kurser. En elev kan inte registrera sig för dessa typer av kurser.
   * **Godkänt av chef:** Cheferna godkänner dessa kurser. Elever kan registrera sig för dessa kurser, men de registreras inte direkt till dessa typer av kurser utan chefens godkännande. En aviseringsbegäran skickas till chefer när elever registrerar sig för dessa typer av kurser. Efter chefens godkännande listas dessa kurser som registrerade för elever.
   * **Egenregistrerad:** Elever kan direkt registrera sig för denna typ av kurser.

1. Klicka på för att spara ändringarna **[!UICONTROL Save]**. Klicka på för att publicera kursen **[!UICONTROL Publish]**.

## Skapa en kurs - avancerat arbetsflöde {#createacourseadvancedworkflow}

1. Logga in på Adobe Learning Manager som författare eftersom det bara är författare som har behörighet att skapa kurser. På sidan Komma igång klickar du på **[!UICONTROL Create Courses]**.
1. På fliken **Kursöversikt** -sidan, ange namnet på kursen. Ange nu en kort beskrivning av kursen som visas på kurskortet. Beskrivningen får innehålla högst 140 tecken. Ange sedan den detaljerade översikten för kursen som visas på sidan Kursinformation. Beskrivningen får inte överstiga 1 500 tecken.
1. För att göra din kurs tillgänglig på andra språk klickar du på Lägg till nytt språk från det övre vänstra hörnet på sidan. Välj det eller de språk som du vill göra kursen tillgänglig på. Klicka på **[!UICONTROL Save]**. Mer information finns i [Lägg till innehåll för olika språk](/help/migrated/authors/feature-summary/content-library.md).
1. **Ändra kursinställningar**-

   1. Välj en färdighet för kursen på sidan Kursinställningar. Välj önskad kompetens i listrutan Kompetens. I listrutan Nivå väljer du sedan önskad nivå.
   1. Välj kursfärdigheter, nivå och ange poäng för kompetensen. Lägg till fler kompetenser om det behövs.
   1. Från **Registreringstyp** Välj typ av registrering i listrutan.

   Följande typer av registreringar finns:

   * **Nominerad från chef:** Endast chefer kan nominera dessa kurser. En elev kan inte registrera sig för dessa typer av kurser.
   * **Godkänt av chef:** Cheferna godkänner dessa kurser. Elever kan registrera sig för dessa kurser, men de registreras inte direkt till dessa typer av kurser utan chefens godkännande. En aviseringsbegäran skickas till chefer när elever registrerar sig för dessa typer av kurser. Efter chefens godkännande listas dessa kurser som registrerade för elever.
   * **Egenregistrerad:** Elever kan direkt registrera sig för denna typ av kurser.

1. Välj om du vill ange ett pris för kursen eller göra den gratis. Om du vill att kursen ska betalas väljer du alternativet **[!UICONTROL Paid]** och ange ett pris. Priset visas sedan på kurskortet och kursöversiktssidan för en elev.

   OBS! Detta aktiveras bara när Adobe Commerce-anslutningen har konfigurerats.

1. Aktivera kryssrutan om du vill ge elever möjlighet att avregistrera sig själva från din kurs **Elever kan avregistrera sig själva**.
1. **Instanskonfiguration**

   Om du aktiverar det här alternativet kan elever som är i läget Pågår besöka andra instanser och registrera sig där. En elev kan sedan behålla förloppet i föregående instans.

   Om du efter att ha publicerat kursen kommer tillbaka till sidan Inställningar är alternativet inte längre redigerbart.

   Du kan aktivera alternativet för följande kurstyper:

   * I egen takt
   * Klassrum
   * Aktivitet
   * Blandat

   Obs! Om du har aktiverat alternativet Instanskonfiguration i källkursen när du duplicerar en kurs förblir alternativet inaktiverat i målkursen.

   **Instansväxling stöds inte för**:

   * Betalda kurser
   * Kurser av typen chefsnominerad registrering.

   Konfigurationen av instansväxling sprids inte till kollegiala konton om den delas via katalogen. Alternativet förblir inaktiverat i målkursen.

1. **Flera registreringar**

   Med hjälp av detta kan du registrera elever i mer än en kursinstans vid en eller olika perioder.

   Aktivera reglaget **Flera registreringar** för att växla mellan olika kursregistreringar för en elev. Om du har aktiverat instansväxling kan du inte använda Flera registreringar.

1. Välj de kurser som är obligatoriska och som måste slutföras innan du påbörjar kursen. Klicka på fältet Kurser och välj från listan över kurser.
1. Aktivera **Aktivera** **Förutsättningar** kryssrutan om du vill att de obligatoriska kurserna ska vara obligatoriska.
1. Lägg till nyckelord som taggar relaterade till din kurs. Dessa taggar hjälper eleverna att enkelt hitta din kurs under sökningen. Alla dessa taggar läggs till automatiskt baserat på de moduler som vi har lagt till. Om du har andra taggar som du vill lägga till i kursen kan du ange dem.
1. Lägg till nyckelord som taggar relaterade till din kurs. Dessa taggar hjälper eleverna att enkelt hitta din kurs under sökningen. Alla dessa taggar läggs till automatiskt baserat på de moduler som vi har lagt till. Om du har andra taggar som du vill lägga till i kursen kan du ange dem.
1. I fältet Ta bort automatiskt väljer du ett datum när kursen tas ur bruk. Administratören måste aktivera alternativet Ta bort automatiskt först.
1. Klicka på för att spara ändringarna **[!UICONTROL Save]**. Klicka på för att publicera kursen **[!UICONTROL Publish]**.

## Spelifieringspunkter

Du kan tilldela spelifieringspoäng på kurs- och kursinstansnivåerna. På så sätt kan du ge poäng till olika kurser eller instanser. Elever sporras att gå specifika kurser eller föredrar en viss kursinstans framför andra.

1. På kursinstansnivå väljer du **[!UICONTROL Gamification Points]**.

![spelifieringspunkter](assets/select-gamification-points-new.png)

*Ange spelifieringspunkter*

1. Välj **[!UICONTROL Edit]**.
1. Om du väljer Använd inställningar på kursnivå visas följande alternativ:

   * **[!UICONTROL On completion]**: Välj den här funktionen om du vill att eleven ska få 100 poäng när denne slutför en kurs.
   * **Fler regler**

      * **[!UICONTROL Early completion]**: Om du väljer detta får de första 30 eleverna 100 poäng när de slutför en kurs.
      * **[!UICONTROL Timely completion]**: Om du väljer detta tilldelas eleverna 100 poäng om de slutför en kurs inom 999 dagar.

1. Om du **[!UICONTROL Use custom settings]** visas följande alternativ:

   * **[!UICONTROL On completion]**: Välj den här funktionen om du vill att eleven ska få 100 poäng när denne slutför en kurs.
   * **Fler regler**

      * **[!UICONTROL Early completion]**: Om du väljer detta alternativ kan du bestämma hur många elever som ska tilldelas specifika poäng.
      * **[!UICONTROL Timely completion]**: Om du väljer detta alternativ kan du bestämma antalet poäng som elever tilldelas om de slutför en kurs inom en angiven tid.

   ![spelifieringspunkter](assets/gamification-custom-settings.png)

   *Ange tidigt slutförande i tid*

1. Välj **[!UICONTROL Save]**.

## Samla utbildningsresurser

En författare kan bestämma om han eller hon vill aggregera utbildningsresurserna på nivån Utbildningsplan eller låta dem stanna på nivån för en enskild kurs.

Som författare väljer du **[!UICONTROL Learning Path]** > **[!UICONTROL Settings]**. Klicka på **[!UICONTROL Edit]**.

I dialogrutan **[!UICONTROL Resources]** , kryssrutan Visa resurser för ingående kurs sammansatt på nivån Utbildningsväg, när den är aktiverad visar huruvida resurser på kursnivå ska visas på nivån Utbildningsväg.

>[!NOTE]
>
>På sidan Inställningar för en utbildningsväg kan en administratör också aktivera det här alternativet, som visar resurser på kursnivån som skulle visas på nivån Utbildningsväg.

## Schemaläggningsassistent

Hantera konflikter vid bokning av instruktörer och klassrum. Om du vill veta vid vilken tidpunkt och vilket datum en instruktör är tillgänglig innan du tilldelar honom till kursen ska du använda schemaläggningsassistenten.

När du skapar en kurs, för en VC- eller CR-kurs, klickar du på Scheduling Assistant.

![Välj schemaläggningsassistenten](assets/scheduling-assistant.png)

*Starta schemaläggningsassistenten*

Schemaläggningsassistenten öppnas.

![Schemaläggningsassistenten](assets/scheduling-assistant-window.png)

*Dialogrutan Schemaläggningsassistenten*

Med schemaläggningsassistenten kan du:

* Sök lärare efter deras namn.
* Sök instruktörer efter deras kunskaper.

### Sök instruktörer efter namn

I fältet Instruktör skriver du namnet på instruktören eller söker efter ett ofullständigt instruktörsnamn. En lista med instruktörer visas, där du kan välja en instruktör.

![Sök instruktörer efter namn](assets/search-instructor.png)

*Sök efter lärare*

Flera instruktörer kan väljas men endast en instruktör kan tilldelas åt gången. Den valda tiden markeras i fönstret för tidskonflikt. I närheten av instruktören visas en kryssikon som du klickar på för att ta bort instruktören.

![Välj flera instruktörer](assets/busy-times.png)

*Sök efter flera instruktörer*

### Sök instruktörer efter kompetens

Sök efter en instruktör med en eller flera färdigheter. För sökningen används operatorn OCH.

Kompetenser kan endast sökas efter delar av eller hela kompetensnamnet, inte efter kompetensnivå.

På assistenten anger du instruktörens namn, plats och platsgräns.

Du kan också söka kompetens, som visas efter att du har klickat på filterikonen till höger i sökrutan Instruktör. Skärmbilden nedan visar knappen.

![Ange färdigheter för instruktör](assets/scheduling-assistant-instructor-skill.png)

*Sök efter instruktörer efter kompetens*

### Filter för användargrupper

Välj filtret i fältet Instruktör. Det finns en **[!UICONTROL User Group]** filtrera en skapare eller egen skapare kan hitta rätt instruktör genom att använda värdena i användargruppen.

Om båda filtren används visas en lista med instruktörer som tillhör användargruppen och som har de valda kunskaperna.

Detta gäller schemaläggningsassistenten på sidan Kurser eller instanser.

![schemaläggningsassistent](assets/scheduling-assistant-2.png)

*Filtrera på användargrupper*

### Instanssida

Du kan också komma åt Schemaläggningsassistenten från instanssidan, som visas nedan.

Schemaläggningsassistenten finns även på instanssidan för administratörer och anpassade administratörer/författare.

![Schemaläggningsassistenten från instanssidan](assets/instances-scheduling.png)

*Schemalägg instruktörer från sidan Instanser*

### Sök efter en plats

Du kan söka efter en plats genom att ange både klassrumsnamnet och platsregionsnamnet på både modulsidan och sidan Schemaläggningsassistenten.

## RTF-formatering

När du skapar en kurs, ett utbildningsprogram, en certifiering eller ett arbetsstöd kan författaren mata in olika typer av innehåll som text, bild eller använda olika textformateringsalternativ.

När du skapar en kurs kan du se textredigeraren i fältet Kursöversikt. Du kan formatera innehåll, lägga till bilder, lägga till hyperlänkar och så vidare.

![](assets/rich-text-editor-author.png)

*Starta textredigeraren*

På samma sätt kan du använda textredigeraren för att ändra beskrivningen när du skapar en:

**Utbildningsprogram**

![](assets/lp-rte-new.png)

*Använd textredigerare för ett utbildningsprogram*

**Certifiering**

![](assets/cert-rte-new.png)

*Använda textredigerare för ett certifikat*

**Arbetsstöd**

![](assets/job-aid-rte-new.png)

*Använd RTF-redigerare för arbetsstöd*

Dessutom kan du använda textredigeraren för andra språk.

## Stöd för RTF-beskrivning för fjärradministrerat användargränssnitt

### Varför krävs CSS?

RTF består av HTML-kod. Om markeringen återges i befintligt skick kommer standardformatet att användas i webbläsaren. Det här passar ofta inte så bra ihop med företagets stilriktlinjer. En CSS krävs för att uppfylla riktlinjerna.

### Standardformat

Den bifogade CSS-formatmallen innehåller den formatering som används av Learning Manager. Formateringen ändras med tanke på de flesta användningsfallen. Hämta den bifogade CSS-filen och importera den till webbappen enligt dina konventioner och bygg system. De CSS-klasser som definierats har namnutrymmen under klassen ql-editor och påverkar inte dina befintliga format.

### Anpassa format

Standardstilen kanske inte uppfyller alla behov. Anpassningarna kan göras genom att åsidosätta den CSS-kod som anges. All formatering lindas under ql-editor som underordnade väljare. Följande klasser används:

* Indrag: **li.ql-indent-$number**. $number varierar från 1-9
* storlek: **ql-size-small**, **ql-size-large**, **ql-size-large**

* justering: **ql-align-center**, **ql-align-adjust**, **ql-align-right**

* färg: **ql-color-$color**. $color = vit, röd, orange, gul, grön, blå, lila
* bakgrund: **ql-bg-$color**. $color = svart, röd, orange, gul, grön, blå, lila
* html-taggar: p, ol, ul, pre, blockquote, h1, h2, h3, h4, h5, h6

[CSS-fil som ska användas för anpassning.](assets/ql-headless.css)

### API-ÄNDRINGAR FÖR ATT AKTIVERA ÅTERGIVNING AV RTF-ÖVERSIKTER

När kunder bygger ett fjärradministrerat gränssnitt måste de visa utbildningsobjekten i det anpassade användargränssnitt som de utvecklar. För att göra detta använder man vanligtvis [GET /learningObjects](https://learningmanagereu.adobe.com/docs/primeapi/v2/#!/learning_object/get_learningObjects) API som visas. Nu när Learning Manager stöder hämtning av &quot;RTF&quot; för översiktsfältet visar även datamodellen för utbildningsobjekt i API-svaren samma sak. Se fältet med namnet &quot;richTextOverview&quot; i avsnittet om modellen i API-svaret nedan. Observera även att fältet som visades tidigare (&quot;översikt&quot;) förblir oförändrat för bakåtkompatibilitet.

```
{ 
 "data": [ 
 { 
 "id": "string", 
 "type": "string", 
 "attributes": { 
 … 
 "localizedMetadata": [ 
 { 
 "description": "string", 
 "locale": "string", 
 "name": "string", 
 "overview": "string", 
 "richTextOverview": "string" 
 } 
 ], 
 … 
 }, 
 "relationships": { 
 … 
 } 
 } 
 } 
 ] 
} 
```

Kunder som redan använder översiktsfältet påverkas inte i sitt huvudlösa gränssnitt och ser bara vanlig text som förut. Om kunder vill använda RTF-översikten måste de skapa rikt formaterade översikter för sina utbildningsobjekt i användargränssnittet för författare och efter det kommer Learning Manager att börja returnera RTF-översikten också, utöver oformaterad text (som tidigare) i API-svarsmodellen.

Kunden måste dock inkludera en CSS-kod för att kunna återge den detaljerade texten i användargränssnittet. Detta förklaras i detalj i följande avsnitt.

## Tillåt flera försök {#allowmultipleattempts}

När administratören har aktiverat flera försök kan du som författare konfigurera flera försök för en interaktiv e-utbildningsmodul på kurs- eller modulnivå.

![](assets/allow-multipe-attempts.png)

*Konfigurera flera försök för en interaktiv e-utbildningsmodul*

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Alternativ</b></p></td>
   <td>
    <p><b>Beskrivning</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Ställ in antal försök till</p></td>
   <td>
    <p>Du kan ställa in antalet försök för en modul till oändligt eller ange en definitiv gräns.<span style="font-size: 0.8125rem;">Försöksinformationen visas för eleven när den har aktiverats. Eleven kan välja att göra om ett försök med modulen genom att klicka på knappen Försök igen.</span></p></td>
  </tr>
  <tr>
   <td>
    <p>Avsluta nytt försök så snart modulen har slutförts eller godkänts</p></td>
   <td>
    <p>Aktivera kryssrutan "Stoppa nytt försök när modulen är slutförd eller godkänd" för att konfigurera när elever ska hindras från att välja alternativet nytt försök. Alternativet "Försök igen" kommer att tas bort från elevvyn när de har slutfört modulen.</p></td>
  </tr>
  <tr>
   <td>
    <p>Lås modul mellan försök 0:0:1 format: dagar/timmar/minuter</p></td>
   <td>
    <p>Du kan låsa moduler under en viss tid mellan försöken genom att aktivera kryssrutan "<b>Lås modul mellan försök 0:0:1 format: dagar/timmar/minuter</b>". När en modul är låst kan eleven inte besöka modulen förrän den angivna låsningstiden har gått ut. </p>
    <p>Du kan definiera slutkriterierna för ett försök genom att välja kommandot<b>Avslutning av spelare</b>" eller "<b>Slutförande</b>" kryssrutor.</p></td>
  </tr>
  <tr>
   <td>
    <p>Avslutning av spelare</p></td>
   <td>
    <p>Varje modulstart behandlas som ett nytt försök om kriteriet väljs som<b>Avslutning av spelare</b>". En elev uppmanas att ange information om modullås och försök till detaljer när spelaren stängs.</p></td>
  </tr>
  <tr>
   <td>
    <p>Slutförande</p></td>
   <td>
    <p>Om slutet av ett försök baseras på <b>Slutförande</b>, beräknas den utifrån kriterier för lyckat innehåll. Eleverna får inte göra om försök med modulen förrän innehållet har skickat informationen om slutförandet. Information om modullås och försök meddelas eleven när ett försök avslutas.</p></td>
  </tr>
  <tr>
   <td>
    <p>Ange tidsgräns för att slutföra modul</p></td>
   <td>
    <p>Författare kan ange en tidsgräns för att slutföra en modul genom att aktivera kryssrutan, "<b>Ange tidsgräns för att slutföra modul</b>".</p>
    <p>Varje spelaruppskjutning betraktas som ett nytt försök och eleven uppmanas att ange tidsinformationen vid uppskjutningen.</p>
    <p><b>Obs!</b><span style="font-size: 0.8125rem;">Försöket avslutas automatiskt när tiden har gått ut. Att även stänga spelaren kommer att avsluta det aktuella försöket.</span></p></td>
  </tr>
  <tr>
   <td>
    <p>Flera försök på modulnivå</p></td>
   <td>
    <p>Om du väljer ett försök på modulnivå från listrutan Ange försök på kan du konfigurera alternativen på individuell modulnivå.</p></td>
  </tr>
 </tbody>
</table>

## Kursmoduler {#coursemodules}

### Lägg till moduler {#addmodules}

Nu kan du lägga till modulerna Innehåll, Förarbete och Testa. **Innehåll** moduler är de viktigaste moduler som kursen består av. **Förarbete** moduler innehåller viss grundläggande information som kan hjälpa elever att förbereda sig för kursen. Dessa moduler är inte obligatoriska för eleverna att slutföra. **Testning** Modulerna hjälper elever att hoppa över innehållet och göra provet om de redan känner till innehållet och vill göra provet för att uppfylla efterlevnadskravet.

Följ stegen nedan om du vill lägga till en innehållsmodul:

1. Klicka på **[!UICONTROL Add Modules]**. Det finns fyra alternativ för att lägga till moduler. Det första alternativet är att lägga till moduler i eget tempo. Det här är modulerna som du skapar och lägger till i modulbiblioteket i Adobe Learning Manager. Det andra alternativet är att konfigurera det virtuella klassrummet. Den tredje är att konfigurera en klassrumsmodul och den fjärde är Aktivitetsmodul.

   ![](assets/select-module-type.png)

   *Lägg till en modul för en kurs*

   **Modul för eget tempo:** I det här läget kan du starta och slutföra en kursmodul i din egen takt. Du kan ange ett eget schema.

   När du har klickat på alternativet visas en lista med moduler för eget tempo som redan har lagts till i modulbiblioteket. Här kan du antingen bläddra igenom listan och välja vilka du vill lägga till, eller så kan du söka efter moduler genom att skriva modulens namn i sökfältet eller modultaggarna.

   När du har valt moduler klickar du på **[!UICONTROL Add]**. Dessa moduler visas nu i avsnittet Innehåll.

   Du kan även ändra ordning på modulerna. Dra en modul och flytta den uppåt eller nedåt och ordna modulerna i rätt ordning.

   **Virtuell klassrumsmodul:** I det här läget kan eleverna delta i onlinelektioner live ledda av en utbildad instruktör. Ange sessionens titel, beskrivning och varaktighet. Du kan också ange webbadressen till konferensen och vilka instruktörer som ska leda sessionen. Klicka på för att spara ändringarna **[!UICONTROL Done]**.

   ![](assets/1st-image.png)

   *Lägg till en VC-modul*

   När du skapar en kurs med hjälp av dialogrutan Virtuell klassrumskonfiguration anger du **Konferenssystem** till den Teams-anslutning som du skapade. Välj om du vill ha en mötesorganisatör för evenemanget.

   Om du **Ja** För en mötesorganisatör måste du ange namnet på organisatören. Ange namnet och välj organisatör.

   **Förbipasserande lobby**

   * Om du **Ja** kan alla elever ansluta till mötet,.
   * Om du **Nej** skickas en begäran till organisatören om att tillåta eller förhindra eleven från att delta i mötet.

   **Obs!** En elev måste vara tillgänglig på Microsoft Teams. Eleven kan dock gå med i Learning Manager som gäst.

   **Klassrumsmodul:** I detta läge deltar eleverna vid personliga lektioner ledda av en utbildad instruktör. Ange sessionens titel, beskrivning och varaktighet. Du kan också ange var klassen och instruktörerna som ska genomföra sessionen ska vara placerade. Klicka på för att spara ändringarna **[!UICONTROL Done]**.

   ![](assets/classroom-module.png)

   *Lägg till en klassrumsmodul*

   När du skapar en kurs ska du i dialogrutan Konfiguration av virtuellt klassrum ställa in konferenssystemet på Microsoft Teams-anslutningen som du skapade. Välj om du vill ha en mötesorganisatör för evenemanget.

   Om du väljer Ja för en mötesorganisatör måste du ange namnet på organisatören. Skriv namnet på organisatören och välj organisatören.

   **Förbipasserande lobby**

   * Om du väljer Ja kan alla elever ansluta till mötet.
   * Om du väljer Nej skickas en begäran till organisatören om att tillåta eller förhindra eleven från att ansluta till mötet.

   **Obs!** Om en elev vill komma till Microsoft Teams som gäst måste han/hon ange e-postadressen. E-postmeddelandet måste finnas i Learning Manager.

   **Aktivitetsmodul:** I det här läget måste eleverna slutföra en uppsättning aktiviteter, som workshops, övningar, enkäter och andra utbildningsaktiviteter. Ange rubriken, beskrivningen och den externa webbadressen för referens. Klicka på för att spara ändringarna **[!UICONTROL Done]**.

   ![](assets/activity-module.png)

   *Lägg till en aktivitetsmodul*

   Du kan ange varaktigheten när du lägger till en aktivitetsmodul i en kurs för filinlämning av aktivitetstyp och xAPI-baserade moduler.

1. På samma sätt lägger du till moduler för lägena Förarbete och Testa.
1. Välj ordningsföljd för moduler i sorterad eller osorterad ordning enligt dina önskemål.

   Om du väljer **Beställt** visas modulerna i samma ordning som du skapade dem. Om du väljer **Osorterad**, modulerna är inte sekvenserade. Elever kan slutföra modulerna i valfri ordning.

1. I rullgardinsmenyn Obligatoriska moduler väljer du antalet moduler som eleven måste ta för att slutföra kursen.
1. Lägg till en omslagsbild och banderollbilden för kursen. Katalogerna skapas av administratören. Mer information finns i [Kataloger](/help/migrated/administrators/feature-summary/catalogs.md).

   **Obs!** De rekommenderade måtten är:

   * **Framsidesbild:** 300 px x 300 px
   * **Banderollbild:** 1 600 px x 140 px

1. I det övre högra hörnet på sidan klickar du på **[!UICONTROL Save]**.

## Checklista {#create-checklist}

Utvärdering är en viktig aspekt av alla system för hantering av inlärning. Utvärderingar online är ett av de bästa sätten att utvärdera en elevs förståelse av ett ämne. Men ofta är det nödvändigt att utvärdera en persons förståelse när hon/han är på jobbet genom att observera honom/henne utföra de nödvändiga uppgifterna.

Man kan tänka sig butiksanställda eller lagerarbetare som genomgår en utvärdering för de uppgifter de förväntas utföra på daglig basis. Det kan vara de steg som utförs för att reparera en kaffemaskin eller de steg som krävs för att packa ett material. Instruktörer kan utvärdera anställda för sådana uppgifter på grundval av en checklista och utvärdera dem som godkända eller underkända i utvärderingsaktiviteten.

### Skapa en checklista {#createachecklist}

Det är bara en författare som kan skapa en checklista. En checklista är en typ av aktivitetsmodul. När du konfigurerar en aktivitetsmodul kan du som författare välja en aktivitet som **Checklista** som visas nedan:

![](assets/checklist-option.png)

*Skapa en checklista*

När du har valt alternativet **Checklista** visas ytterligare några alternativ.

**Typ av checklista:** Välj ett alternativ, **Ja/nej** eller **1-5**. Om du väljer Ja/Nej innehåller checklistan frågor som bara kan besvaras med Ja eller Nej. Om du väljer 1-5 kan du se en Likertchecklista, där du kan betygsätta en fråga på en femgradig skala.

**Kriterier för godkänt:**

<table>
 <tbody>
  <tr>
   <td>
    <p>Om du hade valt <b>Ja/nej</b>, sedan...</p></td>
   <td>
    <p>Om du hade valt <b>1-5</b>, sedan...</p></td>
  </tr>
  <tr>
   <td>
    <p>Ange kriteriet för godkänt som antalet svar som Ja. Om du till exempel anger 3, klarar eleven kursen om han/hon får minst tre <b>Ja </b>svar, när de utvärderas av en instruktör.</p></td>
   <td>
    <p>Ange kriterier för godkänt som ett tröskelvärde för ett tal mellan 1 och 5. Om du till exempel anger 2 och 4, klarar eleven kursen om han/hon uppnår minst <b>två </b>utvärderingar som har poäng högre än eller lika med <b>fyra</b>.</p></td>
  </tr>
 </tbody>
</table>

Välj en eller flera instruktörer som ska utvärdera eleven.

Om du har något att kommentera eller en anteckning kan du även lägga till det i **Kommentar till instruktör** textfält.

Nu lägger du till checklistefrågorna. Klicka på **[!UICONTROL Add]**. Du kan bara lägga till högst 150 frågor.

![](assets/add-checklist-questions.png)

*Lägg till checklistefrågor*

Om du vill lägga till fler frågor klickar du på **[!UICONTROL Add more]**.

Spara ändringarna, lägg till modulen och publicera kursen.

### Lägg till kompetenser {#addskills}

Ange följande information på den här sidan:

1. Välj kursfärdigheter, nivå och ange poäng för kompetensen. Lägg till fler kompetenser om det behövs.

   ![](assets/course-skills.png)

   *Lägg till färdigheter för en kurs*

1. Välj typ av registrering. Följande alternativ finns:

   * **Nominerad från chef:** Endast chefer kan nominera dessa kurser. En elev kan inte registrera sig för dessa typer av kurser.
   * **Godkänt av chef:** Cheferna godkänner dessa kurser. Elever kan registrera sig för dessa kurser, men de registreras inte direkt till dessa typer av kurser utan chefens godkännande. En aviseringsbegäran skickas till chefer när elever registrerar sig för dessa typer av kurser. Efter chefens godkännande listas dessa kurser som registrerade för elever.
   * **Egenregistrerad:** Elever kan direkt registrera sig för denna typ av kurser.

1. Aktivera kryssrutan om du vill ge elever möjlighet att avregistrera sig själva från din kurs **Elever kan avregistrera sig själva**.
1. Välj de kurser som är obligatoriska och som måste slutföras innan du påbörjar kursen. Klicka på fältet Kurser och välj från listan över kurser.

   ![](assets/prerequisite-courses.png)

   *Lägg till obligatoriska kurser*

1. Aktivera **Förutsättningar** kryssrutan om du vill att de obligatoriska kurserna ska vara obligatoriska.
1. Lägg till nyckelord som taggar relaterade till din kurs. Dessa taggar hjälper eleverna att enkelt hitta din kurs under sökningen. Alla dessa taggar läggs till automatiskt baserat på de moduler som vi har lagt till. Om du har andra taggar som du vill lägga till i kursen kan du ange dem.
1. Lägg till profilerna för din målgrupp för kursen genom att klicka i textområdet och välja profilerna från förslagen.
1. Lägg till resursfiler till din kurs som extra material. Dra dina material som text, video eller ljudfiler.
1. Nu kommer den här kursen att vara tillgänglig för dessa elever som har dessa profiler som en rekommenderad kurs. Du kan även bifoga ytterligare resurser till dina elever i detta avsnitt. Elever kommer att kunna hämta dessa filer för senare referens. När du är klar med alla dessa ändringar går du vidare och klickar på **[!UICONTROL Save]** längst upp till höger. Då sparas kursen som ett utkast. Kursen sparas som utkast som standard.

## Tilldela instruktörer för moduler {#assigninstructorsformodules}

1. När du har skapat moduler till din kurs kan du tilldela instruktörer till modulerna. På kontrollpanelen för författare klickar du på **[!UICONTROL Course Catalog]**.
1. Klicka på kursen vars modul du vill tilldela instruktörer.
1. Från **Lägg till moduler** klickar du på modulen som du vill tilldela en instruktör.
1. I dialogrutan **Instruktör** anger du användarnamnet på den användare som du vill tilldela instruktörsrollen.

   ![](assets/instructor-field.png)

   *Tilldela en instruktörsroll till en användare*

1. Om du vill återpublicera kursen med uppdateringarna klickar du på **[!UICONTROL Republish]**.

## Checklista för observation

En checklista modul kan nu granskas av chefer förutom instruktörer. Personer chefer, samt icke-hierarkiska chefer, såsom butikschefer eller platschefer, kan granska och slutföra checklistan.

Kursförfattare kan lägga till personhanterare och icke-hierarkiska chefer (om tillämpligt) som granskare genom att välja dessa rollalternativ i avsnittet Granskare när de konfigurerar en checklistmodul. Detta kan göras på kursinstansnivå.

![Checklista för chefer](assets/manager-checklist.png)

*Lägga till granskare i en aktivitetsmodul*

Välja kommandot **[!UICONTROL +Managers]** Alternativet gör att en elevs chef i organisationshierarkin automatiskt kan granska checklistan. Du behöver inte söka efter och lägga till chefsnamn individuellt.

Om din kontoadministratör har konfigurerat icke-hierarkiska chefsroller (t.ex. platshanterare eller platshanterare) genom att använda alternativet Aktiva fält, kommer dessa chefsroller att vara tillgängliga för dig att välja och aktivera dem för att granska checklistan.

Du behöver inte söka efter och lägga till chefsnamn individuellt. När elever registrerar sig för checklistan kommer den automatiskt att skicka ett meddelande till sina chefer/butikschefer för granskning tillsammans med vald instruktör. Det här arbetsflödet gör det enkelt för författare att inte nämna enskilda chefers namn.

I exempelskärmbilden ovan väljer du &quot;**[!UICONTROL +Store Managers]** Alternativet gör att den icke-hierarkiska chefen automatiskt justeras mot eleven för att granska checklistan. Observera att &quot;store&quot; här ersätts av det aktiva fält som administratören har definierat.

Uppdateringar av checklistmodulen inkluderar även meddelanden till instruktörer och chefer när en elev är registrerad i en kurs som har en checklistmodul i sig. Granskaren får ett meddelande i Learning Manager-meddelandecentret samt på instruktörens/chefens instrumentpanel om att en checklisteåtgärd ska utföras.

<!--![View notification for enrollment](assets/checklist-notification.png)-->

Granskaren kan visa information om alla väntande checklista för granskningsobjekt från menyn Checklistor samt meddelandemenyn när hen loggar in som instruktör/chef.

![Certifikatsgodkännanden](assets/pending-task-managers.png)

*Godkännanden för certifiering*

När granskaren har klickat på Granska checklista kan han/hon slutföra utvärderingen.

![Granska väntande checklista för granskningsobjekt](assets/evaluation-checklist.png)

*Granska väntande checklista för granskningsobjekt*

Rapporteringen kan hämtas på checklistor, som innehåller detaljerad information om elevutvärdering, granskarens namn, roll och e-post.

CSV-filen med checklisterapporter innehåller de nya och uppdaterade fälten:

* Granskarens namn i stället för instruktörens namn
* Granskarens e-postadress i stället för instruktörens
* Granskarroll - möjliga värden är Chef, Butik/Platshanteraren, Instruktör

## Förhandsgranska en kurs {#previewacourse}

När kursen har skapats och sparats som ett utkast kan du förhandsgranska kursen som elev och sedan publicera den för att göra den tillgänglig i kurskatalogen.

Klicka på för att förhandsgranska kursen **[!UICONTROL Preview as learner]**.

![Förgranska en kurs som elev](assets/preview-as-a-learner.png)

*Förgranska en kurs som elev*

Detta öppnar kursen **Översikt** sida för dig där du kan se moduler, deras ordning och andra detaljer som rör kursen.

![](assets/overview-page.png)

*Visa moduler och annan relaterad information*

Om du vill se hur eleverna kan uppleva kursen klickar du på var och en av dessa moduler för att börja spela upp den. Detta börjar spela kursen i Fluidic Player.

## Publicera en kurs {#publishacourse}

Efter att ha förhandsgranskat kursen som elev kan du publicera den, så att den blir tillgänglig för elever att konsumera. Observera att kursen fortfarande är i utkastläge.

Kursens livscykel ser normalt ut så här:

* **Utkast** - När en författare har skapat en kurs och sparat den. I det här läget är kursen inte tillgänglig för elever ännu.
* **Publicerat** - När en författare har slutfört publiceringen av en kurs. I det här läget är kursen tillgänglig så att elever kan registrera sig. Du kan även redigera en kurs i det här läget.
* **Utfasad** - Efter att ha publicerat en kurs kan författaren flytta den till ett utfasat tillstånd om författaren inte vill att kursen ska visas i kurskatalogen för elever.
* **Raderat** - En kurs under borttaget tillstånd är när den tas bort helt från Adobe Learning Manager-appen. Det är bara författare som kan ta bort kurser när de är i tillståndet Utkast eller Utfasad.

![](assets/typical-course-lifecycle.png)

*Arbetsflöde för en kurscykel*

Om du vill publicera kursen som du har skapat klickar du på **[!UICONTROL Publish]** längst upp till höger på sidan.

![](assets/publish-a-course.png)

*Publicera en kurs*

I bekräftelsemeddelandet som visas klickar du på **[!UICONTROL OK]**.

Kursen är nu tillgänglig i kurskatalogen.

## Visa en kurs {#viewacourse}

Du kan visa en lista över alla tillgängliga kurser som författare. Klicka på Kurskatalog för att se alla kurser i Learning Manager-kontot. För att se alla dina redigerade kurser i Learning Manager, klicka på **[!UICONTROL My Courses]**.

Håll pekaren över alternativen på kurskortet och klicka på **[!UICONTROL View Course]**.

![](assets/view-a-course.png)

*Visa en kurs*

Fönstret med kursinformation visas. Kursen är i skrivskyddat läge. Om du vill ändra kursen klickar du på **[!UICONTROL Edit]**.

## Ta bort en kurs {#retireacourse}

Om du tar en kurs ur bruk kan du inte registrera nya elever på kursen. Elever som redan är registrerade kan ta kursen.

Om du vill ta en kurs ur bruk ska du gå till kurskortet, hålla pekaren över alternativen och klicka på Ta bort kurs.

![](assets/retiring-course.png)

*Ta bort en kurs*

I bekräftelsefönstret som visas klickar du på **[!UICONTROL Yes]**.

## Duplicera en kurs {#duplicateacourse}

Du kan skapa en kopia av kursen och sedan ändra kursen. Om du vill säkerhetskopiera kursen kan du duplicera den.

## Sök efter kurser {#searchforcourses}

Adobe Learning Manager gör det enklare för dig att snabbt hitta de kurser du väljer. Du kan söka efter dina kurser på följande sätt:

**Sökfält:** Klicka på sökfältet längst upp till höger på fliken **KURSKATALOG** sidan. Skriv in kursnamnet eller nyckelord som är associerade med dina kurser. Du kan också söka med taggar som läggs till när kursen skapas. Taggar är sökbara i sökfältet för kurser, vilket innebär att taggarna visas i sökfältet när du skriver.

![](assets/search-field.png)

*Sök efter kurser*

**Filtrera listan med kurser:** Du kan filtrera kurserna efter tillstånd som Alla, Publicerat, Utkast och Utfasade. Beroende på ditt val kan du visa den filtrerade listan över kurser och välja de kurser som krävs.

Du som är författare kan även sortera kurserna så att de lättare hittar den kurs du behöver. Klicka **[!UICONTROL Sort by]** och välj alfabetisk stigande ordning, alfabetisk fallande ordning, datum då kursen skapades, datum då kursen uppdaterades och kursernas effektivitet.

![](assets/filter-list-of-courses.png)

*Filtrera lista med kurser*

## Registrera elever i en kurs {#enrolllearnersinacourse}

Om du vill registrera elever för kurserna, eller om du vill tillåta chefer att nominera elever för kurserna, måste du växla till administratörsläget eftersom endast administratörer har behörighet att registrera elever för kurserna.

Växla till administratörsläge genom att

1. Klicka på din profilbild och välj sedan Administratör.
1. Klicka på i administratörsläge **[!UICONTROL Courses]** i den vänstra rutan. På denna sida kan du se alla kurser som har skapats av alla författare i ditt Learning Manager-konto.
1. För att registrera eleverna håller du pekaren över kurskortet så kan du se alternativet **Registrera elever**. Klicka på det här alternativet.

   ![](assets/enroll-learners.png)

   *Registrera elever på en kurs*

1. I dialogrutan Registrera elever kan du i det övre högra hörnet se att alternativet **Standardinstans** har markerats. Så snart en kurs skapas av en författare skapas en standardinstans av kursen.

   ![](assets/default-instance.png)

   *Visa standardinstans av en kurs*

1. Börja skriva namnet på en elev i fältet Inkludera elever och välj en elev. Här kan du även lägga till användargrupper. Om du vill registrera alla elever i ditt Learning Manager-konto börjar du skriva alla. Du kan även registrera elever i ett team.

   ![](assets/include-learners.png)

   *Lägg till elever i en kurs*

1. Om du vill utesluta någon elev från kursen. anger du namnet på eleven i **Exkludera elever** område.
1. När du har registrerat eleverna klickar du på **[!UICONTROL Proceed]**. I dialogrutan Registrera elever kan du visa sammanfattningen av registreringen.

   ![](assets/summary-of-enrollment.png)

   *Visa kursregistreringssammanfattning*

1. För att registrera alla elever i kursen klickar du på **[!UICONTROL Enroll]**. Dessa elever har nu registrerats för denna kurs. Eleverna får ett meddelande om att gå vidare och ta kursen. Upprepa registreringsproceduren om du vill registrera fler elever.

## Ändringar av kursinstanssidan för Connect VC-moduler {#connect-vc}

När du hämtar en Connect-kurs kan du skapa två typer av rum:

* Dynamisk
* Bestående

En beständig URL har alltid åtgärdats. Men för användare som inte har Connect och ett eget mötesrum måste de använda ett dynamiskt mötesrum under körning. Då kan människor ansluta sig till mötet.

![](assets/dynamic-room-options.png)

*Alternativ för dynamiska mötesrum*

Du kan nu ändra URL:en för det beständiga rummet på **Kursinstans** sidan.

<!--| ![](assets/persistentroomdropdown.png) | ![](assets/courseinstancepage-persistentroom.png) |
|---|---|-->

## Avregistrera elever från en kurs {#unenrolllearnersfromacourse}

När du skapar en kurs kan en författare aktivera alternativet **Elever kan avregistrera sig själva**, så att elever som deltar i kursen kan rulla ut från kursen.

En administratör kan också avregistrera elever från kursen.

![](assets/unenroll-learners.png)

*Avregistrera elever från en kurs*

Mer information finns i [Avregistrera elever](/help/migrated/administrators/feature-summary/courses.md).

## Lägg till kursmoduler för Captivate och Presenter {#addcoursemodulesforcaptivateandpresenter}

Du kan även publicera kursmodulerna till Learning Manager från Adobe Captivate och Adobe Presenter via menyn Publicera.

1. I Captivate klickar du på **[!UICONTROL Publish]** > **[!UICONTROL Publish to Learning Manager]**.
1. Ange underdomännamnet eller e-post-ID och klicka på **[!UICONTROL Submit]**. Om du har flera konton uppmanas du att välja konto.
1. Logga in med autentiseringsuppgifterna för Adobe. Om du inte har ett Adobe-ID klickar du på **[!UICONTROL Create Account]**. Efter auktoriseringen dirigeras du till modulpubliceringssidan.
1. Ange all grundläggande information om modulen och klicka på Publicera.

Du kan se den publicerade modulen på sidan Learning Manager-moduler. Mer information finns i [Publicera projekt till Adobe Learning Manager](https://helpx.adobe.com/captivate/classic/publish-project-to-captivate-prime.html).

## Kurseffektivitet {#courseeffectiveness}

Poäng för kurseffektivitet hjälper författare att utvärdera kurserna som inte fungerar enligt elevernas behov och ändra dem därefter. Kursens effektivitet utvärderas för att förstå nyttan av en kurs för eleven. Det är en kombination av resultat från elevfeedback på kursinnehållet. Kursens quiz är ett resultat för en elev och chefens feedback som utvärderar en elev baserat på inlärning från kursen.

in **Mina kurser** kan en författare visa kurseffektivitet på kursens miniatyrbilder som visas på ögonblicksbilden nedan. Du kan se betyget för den här kursen som 100.

<!--![](assets/course-rating.png)-->

Värdet för kurseffektivitet har erhållits med beaktande av L1-, L2- och L3-feedbackvärden. Klicka på värdet för kurseffektivitet för att visa uppdelningen av varje feedback. En popup-meny visas enligt nedan.

![](assets/how-course-effectivenessiscalculated.png)

*Beräkning av kurseffektivitet*

I den här exempelögonblicksbilden fick 1 av 1 användare alla tre typerna av feedback, därför är poängen 100/100. Från den här tabellen kan du förstå den feedback som saknas för att förbättra den övergripande effektiviteten. Om du vill se hur kurseffektiviteten beräknas, klickar du på nedåtpilen längst ned till höger på snabbmenyn.

<!--![](assets/how-course-effectivenessiscalculated1.png)-->

Enligt cirkeldiagrammet ovan viktas L3-feedback från chefen mer.

## Certifieringar och utbildningsprogram {#certificationsandlearningprograms}

Både Författare och Administratör kan skapa certifieringar och utbildningsprogram för elever från appen Författare. På startsidan klickar du på antingen Certifieringar eller Utbildningsprogram för att skapa respektive utbildningsobjekt.

Mer information om hur du skapar och hanterar certifieringar och utbildningsprogram finns i  [Certifieringar](/help/migrated/administrators/feature-summary/certifications.md) och  [Utbildningsprogram](/help/migrated/administrators/feature-summary/learning-programs.md).

## Obligatoriska kurser för extern certifiering {#mandatorycoursesforexternalcertification}

I tidigare versioner av Learning Manager var slutförande av kursen från eleven i extern certifiering inte obligatoriskt för att slutföra ett certifikat.

Du kan nu göra kurser obligatoriska genom att aktivera alternativet **Ange kurser som krävs som obligatoriska för slutförande av certifikat** på fliken Kursplan.

![](assets/set-required-coursesasmandatory.png)

*Ange obligatoriska kurser för att slutföra ett certifikat*

När kurser anges som obligatoriska:

* På chefens inlämningssida visas eleverna först efter att eleverna har slutfört kurserna.
* Eleven kan bara ladda upp en fil efter att ha slutfört kursen.

## Vanliga frågor {#frequentlyaskedquestions}

+++Hur tar man bort &quot;sök chefsnominering&quot; för en kurs?

Gör följande:

1. Logga in på Learning Manager som författare.
1. Öppna kursen.
1. I den vänstra rutan klickar du på **[!UICONTROL Settings]** > **[!UICONTROL Edit]**.
1. På fliken **Registreringstyp** listruta, ändra registreringstypen från **Nominerad från chef** till **Godkänt av chef** eller **Egenregistrerad**.

1. När du har ändrat typ av registrering, publicera kursen igen.

+++

+++Hur kombinerar man kurser?

Du kan kombinera kurser via ett utbildningsprogram.

1. Logga in på Learning Manager som administratör.
1. I den vänstra rutan klickar du på **[!UICONTROL Learning Programs]**.
1. Om du vill lägga till ett utbildningsprogram klickar du på **[!UICONTROL Add]**.
1. Ange information om utbildningsprogrammet och spara utbildningsprogrammet genom att klicka på **[!UICONTROL Save]**.
1. När du har skapat utbildningsprogrammet klickar du på **[!UICONTROL Catalog]**.
1. Klicka på ett kurskort **[!UICONTROL Add]** som visas nedan. Upprepa processen för alla kurser du vill lägga till i utbildningsprogrammet.

![](assets/add-catalog.png)

När du har lagt till alla kurser som krävs i utbildningsprogrammet klickar du på **[!UICONTROL Publish]**.

I ett utbildningsprogram kan du bara lägga till egenregistrerade kurser och inte chefsnominerade eller chefsgodkända kurser. Detta är ett standardbeteende i Learning Manager.

+++

+++Hur ser man till att alla elever inte kan se alla kurser?

Det kan du göra med hjälp av kataloger. En standardkatalog innehåller alla kurser som har lagts till i Learning Manager som standard.

Du måste inaktivera standardkatalogen och skapa anpassade kataloger.

1. Logga in på Learning Manager som administratör.
1. I den vänstra rutan klickar du på **[!UICONTROL Catalogs]**.
1. Skapa en katalog genom att klicka på **[!UICONTROL Create]**. Ange informationen och klicka på **[!UICONTROL Save]**.

1. I katalogalternativen kan du välja olika typer av utbildningar som du kan lägga till, till exempel utbildningsprogram, certifiering eller kurs.
1. I avsnittet Utbildningsprogram klickar du på **[!UICONTROL Add Content]**.
1. I den vänstra rutan klickar du på **[!UICONTROL Share Internally]** eller **[!UICONTROL Share Externally]** beroende på vilken målgrupp du vill rikta in dig på.

1. Lägg till en användargrupp genom att klicka på **[!UICONTROL Add User Groups]**.
1. På sidan Kataloger inaktiverar du **D[!UICONTROL efault Catalog]** och aktivera katalogen som du har skapat.

![](assets/enable-custom-catalog.png)

+++

+++Hur gör jag för att registrera dig för en slutförd kurs igen?

En slutförd kurs kan inte återställas. En elev **kan inte omregistreras** till en slutförd kurs.

+++

+++Hur kan elever se kursen även efter att de har slutfört den?

En elev kan visa en kurs efter slutförande genom att klicka på knappen Besök igen i kursen.

Utför stegen nedan:

1. Logga in som elev.
1. Öppna kursen som du har slutfört.
1. Klicka på **[!UICONTROL Revisit]**.

+++

+++Hur lägger man till en resursfil i kursen?

När du skapar en kurs kan du lägga till video-, ljud-, pdf- eller textfiler till kursen som är relevanta för kursen så att eleven kan få tillgång till ytterligare utbildningsmaterial.

![](assets/add-resources.png)

+++

+++Hur ställer du in flera försök på modul?

**Krav:** Administratören måste aktivera alternativet **Flera försök** i **Inställningar > Allmänt** i appen Admin.

Du som är författare aktiverar alternativet Kursöversikt på sidan Kursöversikt **Tillåt flera försök**.

Mer information finns i [avsnitt om flera försök](courses.md#Allowmultipleattempts).

+++

+++Kan du hämta material som har överförts till Adobe Learning Manager för att ändra materialet?

Nej, innehållet som laddas upp i Learning Manager är en publicerad zip-fil och är inte källfilen. Även om innehållet hämtas kan det därför inte redigeras i ett redigeringsverktyg. Du behöver en källfil för att redigera innehållet.

+++

