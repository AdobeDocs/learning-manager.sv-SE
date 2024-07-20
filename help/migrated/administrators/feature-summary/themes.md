---
description: Färgteman och varumärken i Learning Manager
jcr-language: en_us
title: Färgteman
contentowner: jayakarr
exl-id: 8616e38a-023f-4acb-ac68-df71a5153ad2
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '1176'
ht-degree: 0%

---

# Färgteman

Färgteman och varumärken i Learning Manager

Med Learning Manager kan du ändra utseendet på appen för att matcha din organisations krav på varumärken.

## Anpassa användargränssnittet

I den här utbildningen kommer du att utforska sätt att anpassa utseendet på gränssnittet så att det matchar en organisations krav på varumärke.

[![knapp](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&amp;sdid=QBWYPFSV&amp;mv=display&amp;mv2=display#/course/8318823)

Skriv till <almacademy@adobe.com> om du inte kan starta utbildningen.

## Varumärke {#branding}

Klicka på **[!UICONTROL Branding]** i den vänstra rutan för att uppdatera organisationens namn, ändra underdomänen, loggstilar och teman. Klicka på **[!UICONTROL Edit]** bredvid vart och ett av dessa ämnen för att ändra innehållet.

## Formatera logotyp {#logostyling}

Klicka på **[!UICONTROL Edit]** för att ställa in utseendet på din logotyp och ditt företagsnamn i Learning Manager-programmet.

Klicka på **[!UICONTROL Upload new logo]** och välj logotypen på datorn för att överföra. Du kan förhandsgranska logotypens utseende och organisationens namn nedan. Välj en rubrikstil och klicka på **[!UICONTROL Save]**.

## Teman {#themes}

En uppsättning med fem representativa bilder tillhandahålls för att förhandsgranska dina färgtemaändringar innan du tillämpar dem på ditt program. Bläddra igenom bilderna genom att klicka på symbolerna &lt; och > till vänster och höger om bilderna för att förhandsgranska dem. Du kan också klicka i navigeringscirklarna längst ned i de här bilderna för att bläddra igenom uppsättningen med förhandsvisningsbilder.

**Välj ett tema**

Klicka på **[!UICONTROL Show hints]** under det här avsnittet för att visa tipsen på bilden som visas nedan.

![](assets/themes-preview-images.png)

*Visa tips för ett tema*

Learning Manager-programmet erbjuder fem färgtemaalternativ för användare:

* Prime-standard
* Stenar
* Karneval
* Höst
* Vinterhimmel
* Klart

>[!NOTE]
>
>Det livfulla temat är kompatibelt med hjälpmedel.


![](assets/prime-customize-theme.png)

*Anpassa färger i ett tema*

Du kan anpassa färg på den översta raden, accentfärg (till exempel ikonfärg i den vänstra rutan), primärfärg och intensitet på sidofält för teman förutom standardtemat.

I väljaren **[!UICONTROL Primary color]** kan du välja den färg som används för det fördjupande användargränssnittet.

Om du vill anpassa väljer du tematyp i den vänstra rutan och klickar på rutorna bredvid varumärkets färg och sidopanelens ikonfärger. Klicka på sidofältet i sidofältets ljusstyrka, dra framåt eller bakåt för att justera ljusstyrkan. Titta på förhandsvisningen i bilderna ovan när du ändrar dessa alternativ.

Klicka på **[!UICONTROL Reset Theme]** om du vill återställa temats ursprungliga inställningar. Klicka på **[!UICONTROL Save]** när du är klar med ändringarna.

**Direktförhandsvisning**

Klicka på **[!UICONTROL Live Preview]** i det nedre vänstra hörnet i avsnittet Teman. Ett popup-fönster visas enligt nedan:

![](assets/live-theme-preview.png)

*Popup-fönstret Direktförhandsvisning*

Välj önskat tema i listrutan, justera inställningarna och klicka på **[!UICONTROL Preview]** för att se ändringarna direkt i ditt program. Nu kan du gå igenom alla funktioner i programmet och bevittna ändringarna. Du kan också ändra dina roller när du går igenom förhandsvisning i realtid. När du är nöjd med ändringarna kan du återgå till popup-funktionen för förhandsvisning av live-tema och klicka på **[!UICONTROL Apply Theme]**.

Medan du förhandsgranskar ändringarna live visas popup-fönstret för direktförhandsgranskning av tema fortfarande längst ned på skärmen. Du kan välja att minimera popup-fönstret.

## Flera varumärken {#multiple-branding}

Så här implementerar du flera varumärken:

1. I Admin-appen väljer du **Varumärkning** i den vänstra rutan.
1. Välj **Redigera** i avsnittet Flera varumärken.
1. Välj växlingsknappen och aktivera den.

### Interna användare

1. Välj ett aktivt fält i listrutan.
1. Baserat på urvalet kan du ändra organisationens namn och ladda upp en ny logotyp för användarna.

### Externa användare

1. Välj ett aktivt fält i listrutan.
1. Baserat på urvalet kan du ändra organisationens namn och ladda upp en ny logotyp för användarna.

>[!NOTE]
>
>Interna användare kan ha aktiva fält som Externa användare (t.ex. måste administratören lägga till flera varumärken för interna användare och externa användare separat genom att välja aktiva fältvärden separat.)

#### Viktiga saker att observera

* En administratör kan lägga till varumärket i flera nivåer för det här aktiva fältvärdet och den externa användaren kan logga in med olika mekanismer (SSO Single (Okta, Mini Orange), Social inloggning) och kontrollera om varumärket används.
* En extern användare har ett aktivt fält och ett aktivt fältvärde som den interna användaren: Även om det delas måste det anges separat i det flera varumärket av administratören. När det har tillämpats kan externa användare logga in med olika mekanismer (SSO Single (Okta, Mini Orange), Social inloggning) och kontrollera om varumärket kan användas.
* En extern användare som flyttas från en profil till en annan: Om den externa användaren flyttas från en profil till en annan påverkas inte det aktiva fältvärdet för användaren, såvida inte det aktiva fältvärdet redigeras/tas bort av administratören eller den externa användaren när denne loggar in eller registrerar sig

>[!NOTE]
>
>När flera varumärken anges för både interna och externa användare, med samma aktiva fältnamn, med samma aktiva fältvärde men olika konfiguration. I det här fallet rekommenderar vi att kunderna använder samma konfigurationsinställning (logotyp, tema, organisationsnamn) för att undvika diskrepans.


## Anpassa ditt konto {#customize}

Med Adobe Learning Manager kan du anpassa ditt konto för att ge en förbättrad användarupplevelse.

I listan nedan visas de komponenter som kan anpassas. Kontakta Learning Manager [support](mailto:captivateprimesupport@adobe.com) om du vill anpassa kontot.

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Anpassa</b></p></td>
   <td>
    <p><b>Vad rekommenderas</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Anpassa färger på utbildningskort</p></td>
   <td>
    <p> </p>
    <ul>
     <li>Högst 12 egna färger. </li>
     <li>Färger tillämpas på alla utbildningsobjekt. Färgerna kommer att appliceras sekventiellt på alla utbildningsobjekt (utbildningar) och den hexadecimala färgkoden är det format som krävs för alla färger,#ffffff.</li>
     <li>Om bara en färg anges används den färgen på alla utbildningsobjekt.</li>
    </ul>
    <p> </p></td>
  </tr>
  <tr>
   <td>
    <p>Bild för markörpekare</p></td>
   <td>
    <p>Den anpassade bilden visas när användaren hovrar över ett utbildningsobjekt. </p>
    <ul>
     <li>Anpassad bild som används visas när användaren för musen över Learning Manager-webbsidan.<br></li>
     <li>Rekommenderad storlek - 16 × 16 eller 24 × 24 px</li>
     <li>Rekommenderat bildformat - PNG, JPG</li>
    </ul></td>
  </tr>
  <tr>
   <td>
    <p>Förloppsikonbild</p></td>
   <td>Visas när du navigerar mellan sidor. Finns på platser där du ser den "4-kvadratiska" förlopp gif. 
    <ul>
     <li>Rekommenderad storlek - högst 32 × 32 px</li>
     <li>Rekommenderat bildformat - GIF, PNG, JPG</li>
    </ul>
    <p> </p></td>
  </tr>
  <tr>
   <td>
    <p>Teckensnitt</p></td>
   <td>
    <p>Om du vill använda teckensnitten måste du ha ett CDN. Dessutom måste du dela teckensnittsfamiljen som ska användas.</p>
    <p><b>Obs!</b> Teckensnittsfamiljen måste stödjas i alla webbläsare.</p></td>
  </tr>
  <tr>
   <td>
    <p>Bakgrundsbild</p></td>
   <td>
    <p>En bakgrundsbild syns bara i elevrollen. </p>
    <p>Du måste ha bilden som du behöver för att ansöka till elevens bakgrund.</p>
    <ul>
     <li><b>Rekommenderat bildformat:</b> PNG, JPG, JPEG</li>
     <li><b>Rekommenderad storlek: </b>1400x908 px</li>
    </ul></td>
  </tr>
 </tbody>
</table>

## Konfigurera rekommendationsinställningar {#configurerecommendationsettings}

Du kan konfigurera rekommendationsomfattningar för interna och externa elever på **Varumärkning** > **Allmänt** och göra det möjligt för elever att välja färdigheter på elevens startsida.

På sidan **Allmänt** finns följande alternativ:

<table>
 <tbody>
  <tr>
   <td>
    <p>Elevens startsida</p></td>
   <td>
    <p>Välj antingen <strong>Klassisk </strong>eller <strong>Immersive</strong>. Om du väljer Immersive visas andra alternativ.</p></td>
  </tr>
  <tr>
   <td>
    <p>Utbildningstyp<br></p></td>
   <td>
    <p>Välj antingen <strong>Anpassad </strong>eller <strong>Branschanpassad</strong>. Om det finns färre än 1 000 elever betraktas hela kontot som ett enda scope. Rekommendationen är baserad på alla elever.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>Inställning av rekommendationsomfattning<br></p></td>
   <td>
    <p>Välj ett eller flera aktiva fält. För <strong>Anpassad</strong> kan du välja högst ett aktivt fält. För <strong>Branschjusterade</strong> kan du välja högst fem aktiva fält.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>Låt eleven utforska intresseområden</p></td>
   <td>
    <p>Endast för klassisk användning. Välj <strong>Ja </strong>eller <strong>Nej</strong>.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>Uppmana användare att välja intresseområden (kompetenser) <br></p></td>
   <td>
    <p>Endast för en uppslukande upplevelse. Välj <strong>Ja</strong> eller <strong>Nej</strong>. </p></td>
  </tr>
 </tbody>
</table>
