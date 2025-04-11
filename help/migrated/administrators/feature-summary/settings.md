---
description: Lär dig mer om kontoinställningarna för Learning Manager som du kan konfigurera som administratör.
jcr-language: en_us
title: Inställningar
contentowner: manochan
exl-id: a563d955-f67e-4218-88df-625cde673601
source-git-commit: a28ac8f57710c118ca4ad02872fd100c6f24beac
workflow-type: tm+mt
source-wordcount: '3626'
ht-degree: 1%

---

# Inställningar

Lär dig mer om kontoinställningarna för Learning Manager som du kan konfigurera som administratör.

Du kan ändra dina profilinställningar för administratörer och uppdatera dina kontoinställningar. Visa din profilinformation, lägg till/ändra profilfoto och ändra **[!UICONTROL About me]**-innehåll. Uppdatera företagsinformationen, konfigurera inloggningsmetoder för användare och konfigurera anslutningsintegrering via kontoinställningar.

![](assets/settings-admin.png)

## Konfigurera ditt Adobe Learning Manager

Den här utbildningen beskriver grunderna i inställningar på kontonivå.

[![knapp](assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/7476018)


Skriv till <almacademy@adobe.com> om du inte kan starta utbildningen.

## Kontoinställningar {#accountsettings}

Klicka på **[!UICONTROL Settings]** i den vänstra rutan om du vill uppdatera organisationens kontoinställningar.

**Grundläggande information (företagsinformation)**

Klicka på **[!UICONTROL Change]** på sidan och redigera inställningar för land, tidszon, språkinställning och räkenskapsår.

**Konfigurera kontaktadministratören**

Om du vill lägga till eller ändra supportadministratörernas e-postadresser för din organisation kan du konfigurera genom att klicka **[!UICONTROL General]** i den vänstra rutan. Klicka intill **[!UICONTROL Change]** **[!UICONTROL Support Email ID]** och lägg till e-post-ID:n. E-post skickas till dessa administratörer när eleven klickar **[!UICONTROL Contact Admin]** på sidfoten på sidan.

Lägg till ytterligare e-postadresser med semikolon som avgränsare.

**Inloggningsmetoder** - Administratörer kan välja i vilket läge interna eller externa användare kan komma åt kontot.

* **Interna användare:** Du kan ange Adobe ID eller enkel inloggning som inloggningsläge för interna användare.
* **Externa användare:** Du kan ange Adobe ID eller Single Sign-On eller Learning Manager-ID för externa användare.

Om du väljer, Learning Manager ID, kan externa användare logga in på detta konto efter att ha skapat sitt användarnamn och lösenord för Learning Manager.

>[!NOTE]
>
>Om det finns flera externa profiler kan alla profiler ha samma typ av inloggning. Om inloggningstypen till exempel är Adobe ID behöver alla profiler endast logga in med Adobe ID. Varje profil kan inte ha sin egen inloggningstyp.

Du kan komma åt Learning Manager-programmet med Adobe ID eller genom att använda enkel inloggning (SSO). Enkel inloggning är en mekanism som gör att användaren kan autentisera en gång och få åtkomst till flera program många gånger. Den här konfigurationen är inte obligatorisk för organisationen. Om din organisation har SAML 2.0-baserad SSO-leverantör kan du använda den för att konfigurera Learning Manager-programmet. Konfigurationen krävs på organisationsnivå och i Learning Manager-programmet. Om du väljer att använda SSO ska du kontakta Adobe support för att få konfigurationsinstruktioner

**Feedback**

Klicka på **[!UICONTROL Feedback]** i den vänstra rutan för att ställa in frågeformuläret och få feedback från elever efter att ha slutfört en kurs. Se [Hjälpinnehåll för kursfunktioner](/help/migrated/administrators/feature-summary/courses.md#add-l1-and-l3-feedback) om hur du skapar feedback om L1 och L3.

**Flera försök**

Välj **[!UICONTROL Settings]** > **[!UICONTROL General]** > **[!UICONTROL Multiple Attempts]**.

Om du markerar kryssrutan Flera försök kan skaparna ange Flera försök för interaktiva e-utbildningskurser eller moduler. När du markerar den andra kryssrutan kan administratörer ange Oändligt antal försök som standard för alla nya interaktiva e-utbildningskurser som skapas.

![](assets/admin-config.png)

*Markera kryssrutan Flera försök*

**Kursmoderering**

Klicka på **[!UICONTROL General]** i den vänstra rutan och välj alternativet Kursmoderering för att aktivera funktionen Kursmoderering. Mer information om funktionen finns i [Kursmoderering](courses.md#main-pars_header_1879001177).

**Diskussionstavla**

Om du markerar kryssrutan Diskussionstavla kan elever och instruktörer lägga upp kommentarer för kurser med hjälp av fliken Diskussion på sidan Kurser i appen Elever. Men om kursinställningarna indikerar att den här funktionen inte är vald har inställningarna på kursnivå företräde framför administratörsinställningarna.

**Elevtavla**

Klicka på instrumentpanelen i den vänstra rutan. På den här sidan kan du välja vilka widgetar som du vill visa på sidan Elever. Markera de widgetar som du vill aktivera på sidan Elever. Widgetar som inte är markerade visas inte på sidan Elever.

**Adobe Connect**

Klicka på **[!UICONTROL Adobe Connect]** i den vänstra rutan för att konfigurera Adobe Connect-kontot som värd för virtuella klassrumssessioner. Mer information finns i [Funktionshjälp för Adobe Connect](adobeconnect-integration.md).

## Allmänna inställningar {#general}

Aktivera eller inaktivera följande inställningar:

<table>
 <tbody>
  <tr>
   <th>
    <p><b>Namn</b></p>
    </th>
   <th>
    <p><b>Beskrivning</b></p>
   </th>
  </tr>
  <tr>
   <td>Visa kurseffektivitet</td>
   <td>Om det här alternativet är aktiverat kan elever se aktuell kurseffektivitet på panelen Kurs. Den här funktionen är endast tillgänglig för kurser. Stjärngradering stöds inte för utbildningsprogram eller certifikat. Den är tillgänglig för kurser och utbildningsprogram men inte certifieringar.</td>
  </tr>
  <tr>
   <td>Kursens måttlighet</td>
   <td>Om detta är aktiverat måste alla ändringar av kurser godkännas av administratören innan kurserna blir synliga för eleverna.</td>
  </tr>
  <tr>
   <td>Diskussionstavla</td>
   <td>Om du markerar kryssrutan Diskussionstavla kan elever och instruktörer lägga upp kommentarer för kurser med hjälp av fliken Diskussion på sidan Kurser i appen Elever. Men om kursinställningarna indikerar att den här funktionen inte är vald har inställningarna på kursnivå företräde framför administratörsinställningarna.</td>
  </tr>
  <tr>
   <td>Flera försök</td>
   <td>Om detta är aktiverat kan författaren konfigurera flera försök för kursmoduler.</td>
  </tr>
  <tr>
   <td>Alternativet Utforska färdigheter</td>
   <td>Om det här alternativet är aktiverat kan eleverna utforska kollegor och ledarskapsfärdigheter och prenumerera på de färdigheter de väljer.</td>
  </tr>
  <tr>
   <td>Synlighet för kompetenser/taggar</td>
   <td>Visa alla kompetenser och taggar för elever. Du kan antingen visa alla färdigheter och taggar, visa kompetenser och taggar som är tilldelade eller de som ingår i katalogerna som är synliga för eleven.</td>
  </tr>
  <tr>
   <td>Unika ID för utbildningsobjekt</td>
   <td>Om detta är aktiverat kan en administratör eller författare lägga till ett unikt ID för varje utbildningsobjekt.</td>
  </tr>
  <tr>
   <td>Visa filterpaneler</td>
   <td>
    <p><a id="filter-panels"></a>Kontrollera vilka filterpaneler som är tillgängliga för användare i elevappen för att förfina deras sökresultat. Alternativen är följande:</p>
    <ul>
     <li>Kataloger</li>
     <li>Typ</li>
     <li>Format</li>
     <li>Varaktighet</li>
     <li>Kompetenser</li>
     <li>Färdighetsnivåer</li>
     <li>Taggar</li>
    </ul>
    <p>När eleven startar elevappen kan eleven se filtren i sina respektive paneler i avsnitten Min inlärning och Katalog.</p>
    <p><b>Obs: </b>Filtren <b>Format </b>och <b>Duration </b>är avstängda som standard och visas inte för eleverna direkt efter lanseringen. Administratören bör aktivera dem. <br></p></td>
  </tr>
  <tr>
   <td>Visa kataloglista</td>
   <td>Om detta är aktiverat kan elever se en lista över alla kataloger som är tillgängliga för dem. Elever kan använda detta för att förfina hur utbildningsobjekten visas.</td>
  </tr>
  <tr>
   <td>Produktterminologi</td>
   <td>Learning Manager har en standardterminologi som används i hela produkten. Ändra terminologin så att den passar organisationens behov.</td>
  </tr>
  <tr>
   <td>Uppdatering av modulversion</td>
   <td>Konfigurera standardinställningen för att uppdatera innehåll. Inställningarna kan ändras för varje innehåll från kurssidan.</td>
  </tr>
  <tr>
   <td>Registrera användare automatiskt</td>
   <td>Om det här alternativet är aktiverat registreras nyligen importerade användare automatiskt. Användare måste som standard registreras manuellt innan de kan börja använda Learning Manager.</td>
  </tr>
  <tr>
   <td><a id="autodelete"></a>Ta bort interna användare automatiskt</td>
   <td>Om det här alternativet är aktiverat raderas interna användare automatiskt om de inte har tillgång till systemet på ett visst antal dagar. Den här funktionen gäller användare som bara har rollen <b>Elev</b>. Användarna måste kontakta administratören för att återställa åtkomsten.<br></td>
  </tr>
  <tr>
   <td>Visa katalogetiketter</td>
   <td>Om detta är aktiverat kan administratörer och författare ange katalogetiketter och värden och länka dem till utbildningsobjekt. Om du väljer det här alternativet kan författare även lägga till kurser, utbildningsvägar, certifieringar eller arbetsstöd i katalogerna.</td>
  </tr>
  <tr>
   <td>Elever kan visa sina poäng</td>
   <td>Om detta är aktiverat kan eleverna visa sina poäng i elevens betygsutdrag.</td>
  </tr>
  <tr>
   <td>Sammandragsmeddelande</td>
   <td>
    <p>En administratör kan aktivera eller inaktivera att skicka ett e-postmeddelande till elever. Administratören kan också styra frekvensen för de e-postmeddelanden som skickas.</p>
    <ul>
     <li>För <b>aktiva konton</b> inaktiveras sammanfattningsmeddelanden som standard, vilket administratören kan aktivera manuellt.</li>
     <li>För <b>testkonton</b> förblir alternativet för sammanfattningsmeddelanden inaktiverat och administratören kan inte aktivera alternativet.</li>
    </ul>
    <p>Om funktionen är avaktiverad gäller följande:</p>
    <ul>
     <li>Alternativet <b>Sammandrag av e-post</b> inaktiveras.</li>
     <li>En elev kan inte se användarinställningen för e-postsammandragsprenumeration.</li>
    </ul>
    <p> Om funktionen är aktiverad gäller följande:</p>
    <ul>
     <li>Administratören kan aktivera och ändra alternativet för e-postsammanfattning.</li>
     <li>Från <b>Profilinställningarna </b> i elevappen kan en elev (inte i DND-listan) välja att prenumerera/avbryta prenumerationen på sammanfattningsmeddelandet.</li>
    </ul></td>
  </tr>
  <tr>
   <td>Aktivera ikoner för utbildningskort<br></td>
   <td>Om det är aktiverat visas ikoner på utbildningskort i elevappen.<br></td>
  </tr>
  <tr>
   <td>Sidfotslänkar</td>
   <td>
    <p>Lägg till länkar eller e-postadresser som visas som sidfötter. Du kan lägga till högst tre sidfotslänkar.</p>
    <p>Så här anpassar du länkarna i sidfoten:</p>
    <ol>
     <li>Klicka på <b>Lägg till fler</b>, ange namn och URL eller e-post-ID i de angivna fälten. Ange http:// eller https:// som prefix för URL:en.</li>
     <li>Om du vill sprida ändringen över alla språk klickar du på <b>Replikera</b>. Detta säkerställer att alla språk får namnet och URL:en.</li>
     <li>Klicka på <b>Spara</b> för att spara ändringarna. Du kan se ett popup-meddelande som bekräftar ändringen. När du har klickat på OK fylls sidfoten i med de nya länkarna.</li>
    </ol>
    <p>Dessutom kan du:</p>
    <ul>
     <li><b>Klicka på ikonen Återställ</b> för att återställa standardvärdena i fälten Hjälp</b> och <b>Kontaktadministratör</b>.<b></li>
     <li>Anpassa länken i sidfoten för alla språk. Klicka på rullgardinsmenyn <b>Språk</b>, välj språk och lägg till <b>Namn</b> och <b>URL</b> i de angivna fälten. När du har sparat ändringarna visas de uppdaterade länkarna i sidfoten.<br></li>
    </ul></td>
  </tr>
  <tr>
   <td>Rapportera tidszon<br></td>
   <td>
    <p>Ange en inställning på kontonivå för att exportera utbildningsbeviset i följande tidszoner:</p>
    <ul>
     <li>UTC (Standardbeteende)</li>
     <li>Tidszonsinställning på kontonivå</li>
    </ul>
    <p>Elevens betygsutdrag som har hämtats med Job API hämtar också data i den valda tidszonen.</p>
    <p><b>Obs! </b>Ingen ändring förväntas i elevens betygsutdrag som standard direkt efter utgivningen. Administratörer kan konfigurera den här inställningen från Admin &gt; Inställningar &gt; Allmänt &gt; Tidszon för rapport.</p></td>
  </tr>
 </tbody>
</table>

<table border="0" cellpadding="0" cellspacing="0" width="1709">
 <tbody>
  <tr>
   <td height="20" width="147">Namn</td>
   <td>Beskrivning</td>
  </tr>
  <tr>
   <td height="20">Visa kurseffektivitet</td>
   <td>Om det här alternativet är aktiverat kan elever se aktuell kurseffektivitet på panelen Kurs.</td>
  </tr>
  <tr>
   <td height="20">Kursmoderering</td>
   <td>Om detta är aktiverat måste alla ändringar av kurser godkännas av administratören innan kurserna blir synliga för eleverna.</td>
  </tr>
  <tr>
   <td height="20">Diskussionstavla</td>
   <td>Om du markerar kryssrutan Diskussionstavla kan elever och instruktörer lägga upp kommentarer för kurser med hjälp av fliken Diskussion på sidan Kurser i appen Elever. Men om kursinställningarna indikerar att den här funktionen inte är vald har inställningarna på kursnivå företräde framför administratörsinställningarna.</td>
  </tr>
  <tr>
   <td height="20">Flera försök</td>
   <td>Om detta är aktiverat kan författaren konfigurera flera försök för kursmoduler.</td>
  </tr>
  <tr>
   <td height="20">Utforska kompetensalternativ</td>
   <td>Om det här alternativet är aktiverat kan eleverna utforska kollegor och ledarskapsfärdigheter och prenumerera på de färdigheter de väljer.</td>
  </tr>
  <tr>
   <td height="20">Synlighet för kompetenser/taggar</td>
   <td>Visa alla kompetenser och taggar för elever. Du kan antingen visa alla färdigheter och taggar, visa kompetenser och taggar som är tilldelade eller de som ingår i katalogerna som är synliga för eleven.</td>
  </tr>
  <tr>
   <td height="20">Unika ID för utbildningsobjekt</td>
   <td>Om detta är aktiverat kan en administratör eller författare lägga till ett unikt ID för varje utbildningsobjekt.</td>
  </tr>
  <tr>
   <td rowspan="10" height="191">Visa filterpaneler</td>
   <td>Kontrollera vilka filterpaneler som är tillgängliga för användare i elevappen för att förfina deras sökresultat. Alternativen är följande:</td>
  </tr>
  <tr>
   <td height="19">Kataloger</td>
  </tr>
  <tr>
   <td height="19">Typ</td>
  </tr>
  <tr>
   <td height="19">Format</td>
  </tr>
  <tr>
   <td height="19">Varaktighet</td>
  </tr>
  <tr>
   <td height="19">Kompetenser</td>
  </tr>
  <tr>
   <td height="19">Kunskapsnivåer</td>
  </tr>
  <tr>
   <td height="19">Taggar</td>
  </tr>
  <tr>
   <td height="19">När eleven startar elevappen kan eleven i avsnitten Min utbildning och Katalog se filtren i sina respektive paneler.</td>
  </tr>
  <tr>
   <td height="20">Obs! Filtrens format och längd är avstängda som standard och visas inte för eleverna direkt efter releasen. Administratören bör aktivera dem. </td>
  </tr>
  <tr>
   <td height="20">Visa kataloglista</td>
   <td>Om detta är aktiverat kan elever se en lista över alla kataloger som är tillgängliga för dem. Elever kan använda detta för att förfina hur utbildningsobjekten visas.</td>
  </tr>
  <tr>
   <td height="20">Produktterminologi</td>
   <td>Learning Manager har en standardterminologi som används i hela produkten. Ändra terminologin så att den passar organisationens behov.</td>
  </tr>
  <tr>
   <td height="20">Uppdatering av modulversion</td>
   <td>Konfigurera standardinställningen för att uppdatera innehåll. Inställningarna kan ändras för varje innehåll från kurssidan.</td>
  </tr>
  <tr>
   <td height="20">Registrera användare automatiskt</td>
   <td>Om det här alternativet är aktiverat registreras nyligen importerade användare automatiskt. Användare måste som standard registreras manuellt innan de kan börja använda Learning Manager.</td>
  </tr>
  <tr>
   <td height="20">Ta bort interna användare automatiskt</td>
   <td>Om det här alternativet är aktiverat raderas interna användare automatiskt om de inte har tillgång till systemet på ett visst antal dagar. Den här funktionen gäller användare som bara har rollen Elev. Användarna måste kontakta administratören för att återställa åtkomsten.</td>
  </tr>
  <tr>
   <td height="20">Visa katalogetiketter</td>
   <td>Om detta är aktiverat kan administratörer och författare ange katalogetiketter och värden och länka dem till utbildningsobjekt.</td>
  </tr>
  <tr>
   <td height="20">Elever kan visa sina poäng</td>
   <td>Om detta är aktiverat kan eleverna visa sina poäng i elevens betygsutdrag.</td>
  </tr>
  <tr>
   <td rowspan="9" height="172">E-post med sammandrag</td>
   <td>En administratör kan aktivera eller inaktivera sändning av ett e-postmeddelande till elever. Administratören kan också styra frekvensen för de e-postmeddelanden som skickas.</td>
  </tr>
  <tr>
   <td height="19">För aktiva konton kommer sammanfattade e-postmeddelanden att inaktiveras som standard, vilket administratören kan aktivera manuellt.</td>
  </tr>
  <tr>
   <td height="19">För utvärderingskonton förblir alternativet för sammanfattade e-postmeddelanden inaktiverat och administratören kan inte aktivera alternativet.</td>
  </tr>
  <tr>
   <td height="19">Om funktionen är inaktiverad:</td>
  </tr>
  <tr>
   <td height="19">Alternativet Sammanfattad e-post kommer att inaktiveras.</td>
  </tr>
  <tr>
   <td height="19">En elev kan inte se användarinställningen för e-postsammandragsprenumeration.</td>
  </tr>
  <tr>
   <td height="19"> Om funktionen är aktiverad gäller följande:</td>
  </tr>
  <tr>
   <td height="19">Administratören kan aktivera och ändra alternativet för e-postsammanfattning.</td>
  </tr>
  <tr>
   <td height="20">I profilinställningarna i elevappen kan en elev (inte i DND-listan) välja att prenumerera/avregistrera sig från e-postmeddelandet.</td>
  </tr>
  <tr>
   <td height="20">Aktivera ikoner för utbildningskort</td>
   <td>Om det är aktiverat visas ikoner på utbildningskort i elevappen.</td>
  </tr>
  <tr>
   <td rowspan="8" height="153">Sidfotslänkar</td>
   <td>Lägg till länkar eller e-postadresser som visas som sidfötter. Du kan lägga till högst tre sidfotslänkar.</td>
  </tr>
  <tr>
   <td height="19">Så här anpassar du länkarna i sidfoten:</td>
  </tr>
  <tr>
   <td height="19">1. Klicka på Lägg till fler, ange namn och webbadress eller e-post-id i de angivna fälten. Ange http:// eller https:// som prefix för URL:en.</td>
  </tr>
  <tr>
   <td height="19">2. Om du vill låta ändringen överlappa alla språk klickar du på Replikera. Detta säkerställer att alla språk får namnet och URL-adressen.</td>
  </tr>
  <tr>
   <td height="19">3. Klicka på Spara för att spara ändringarna. Du kan se ett popup-meddelande som bekräftar ändringen. När du har klickat på OK fylls sidfoten i med de nya länkarna.</td>
  </tr>
  <tr>
   <td height="19">Dessutom kan du:</td>
  </tr>
  <tr>
   <td height="19">Klicka på återställningsikonen för att återställa standardvärdena i fälten Hjälp och Kontakta administratören.</td>
  </tr>
  <tr>
   <td height="20">Anpassa länken i sidfoten för alla språk. Klicka på listrutan Språk, välj språk och lägg till Namn och URL i de angivna fälten. När du har sparat ändringarna visas de uppdaterade länkarna i sidfoten.</td>
  </tr>
  <tr>
   <td rowspan="5" height="96">Rapportera tidszon</td>
   <td> Ange en inställning på kontonivå för att exportera utbildningsbeviset i följande tidszoner:</td>
  </tr>
  <tr>
   <td height="19">UTC (Standardbeteende)</td>
  </tr>
  <tr>
   <td height="19">Tidszonsinställning på kontonivå</td>
  </tr>
  <tr>
   <td height="19">Elevens betygsutdrag som har hämtats med Job API hämtar också data i den valda tidszonen.</td>
  </tr>
  <tr>
   <td height="20">Obs! Ingen ändring förväntas i elevens betygsutdrag som standard omedelbart efter utgivningen. Administratörer kan konfigurera den här inställningen från Admin &gt; Inställningar &gt; Allmän &gt; Rapporttidszon.</td>
  </tr>
  <tr>
   <td height="19">Integrering med Badgr</td>
   <td>Om det är aktiverat kommer eleverna att kunna ladda upp sina märken till Badgr-webbplatsen. I scenarier med kundutbildning vill organisationer kunna "certifiera" sina kunder och ge dem en möjlighet att visa sina inloggningsuppgifter via sociala medier. Detta motiverar eleven att gå en utbildning och dela med sig av sina prestationer till andra. </td>
  </tr>
  <tr>
   <td height="135">
    <p>Visa gradering</p></td>
   <td>
    <ul>
     <li>Om alternativet <b>Kurseffektivitet</b> är aktiverat kan eleverna bara se värdet av kursens effektivitet.</li>
     <li>Om alternativet <b>Stjärnbetyg</b> är aktiverat kommer eleverna endast att kunna se det genomsnittliga stjärnbetyget och antalet elever som har bedömt kursen.<br></li>
    </ul>
    <p>Den här funktionen är endast tillgänglig för kurser. Stjärnklassificering stöds inte för utbildningsprogram eller certifikat.<br><br><b></b>Den här ändringen påverkar endast learner-appen. </p>
    <p>I alla andra appar (admin, författare, chef, anpassad administratör, anpassad författare) kommer ändringar i inställningarna (stjärnbetyg/kurseffektivitet/inaktivering av showbetyg) inte att ha någon effekt. </p>
    <p>För nya konton kommer avsnittet <b>Visa stjärngraderingar</b> att ha alternativet <b>Stjärngradering</b> aktiverat som standard.</p>
    <p>Om alternativet <b>Kurseffektivitet</b> har aktiverats för befintliga konton aktiveras avsnittet <b>Visa betyg</b> med alternativet Kurseffektivitet valt. Om alternativet <b>Kurseffektivitet</b>s är inaktiverat kommer avsnittet <b>Visa klassificeringar</b> också att inaktiveras. När avsnittet <b>Visa stjärngraderingar</b> är aktiverat kommer alternativet <b>Stjärngradering</b> att vara aktiverat som standard.</p></td>
  </tr>
  <tr>
   <td height="19">Fasa ut</td>
   <td>Välj något av följande alternativ för pensionering:<li>När de har fasats ut kan registrerade elever se och utföra åtgärder, men ännu inte registrerade elever förlorar åtkomsten.</li><li>När elever har dragit sig tillbaka förlorar både registrerade och ännu inte registrerade elever åtkomst.</li><div><b>Obs!</b> Du kan ta bort kurser, utbildningsvägar eller certifieringar från översiktssidorna.</div> </td>
  </tr>
 </tbody>
</table>

<table>
 <tbody>
  <tr>
   <td>
    <p>Utbildningsvägar</p></td>
   <td>
    <p>Om alternativet <b>Aktivera utökade funktioner i utbildningsvägen</b> är aktiverat kan administratörer inkludera utbildningsvägar i utbildningsvägar och kombinera dessa med kurser. Alternativet är oåterkalleligt.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>Instruktörshantering<br></p></td>
   <td>
    <p>Aktivera den här inställningen om du vill begränsa listan över instruktörer som kan väljas när klassrumssessioner/virtuella klassrumssessioner skapas. Alla användare med behörighet som instruktör kan endast tilldelas som instruktör till en session. Den här begränsningen gäller inte migreringsarbetsflöden.<br></p>
  </td>
  <tr>
    <td>
      <p>Import av kompetenser</p>
    </td>
    <td>
      <p>Om det här alternativet är aktiverat kan du välja en extern källa för att importera kompetenser. Kunskaperna för befintliga utbildningsresurser importeras till databasen för kompetenser en gång under den första körningen. För all efterföljande import av utbildningsresurser importeras kunskaperna till kunskapsdatabasen endast för nyligen importerade objekt.
      När alternativet har aktiverats går åtgärden inte att ångra. Du kan inte inaktivera eller byta till en annan källa senare.
      </p>
    </td>
  </tr>
  </tr>
 </tbody>
</table>

>[!NOTE]
>
>När inställningen för kompetensimport har aktiverats kan inte kontolayouten växlas till klassisk vy, d.v.s. växling till klassiskt konto inaktiveras efter att alternativet **Kompetensimport** har aktiverats.

## Byta namn på utbildningsobjekt {#renaminglearningobjects}

Den här funktionen är endast tillgänglig på engelska.

Administratörer kan nu byta namn på lärobjekt i Learning Manager. Följande är de terminologier som kan döpas om.

Modul\
Kurs\
Utbildningsprogram\
Certifiering\
Utbildningsplan\
Arbetsstöd\
Katalog\
Kompetens\
Utmärkelsetecken\
Meddelande\
Mitt lärande\
Resultattavla\
Effektivitet\
Förkunskapskrav\
Förarbete\
Kärninnehåll\
Testning\
I egen takt\
Blandat\
Klassrum\
Virtuellt klassrum\
Aktivitet

## Profilinställningar {#profilesettings}

1. Klicka på rullgardinspilen i det övre högra hörnet bredvid ditt foto/konto och välj **[!UICONTROL Profile Settings]**.
1. I popup-dialogrutan kan du lägga till/ändra ett foto genom att hålla muspekaren över det och klicka på **[!UICONTROL Edit]** i profilfotoområdet.
1. Lägg till/ändra **[!UICONTROL About]**-innehåll genom att klicka på **[!UICONTROL Edit]** bredvid det.
1. Klicka på **[!UICONTROL Save].**

## Innehållsmapp {#content-folder}

Learning Manager har stöd för mappar med privat innehåll. En administratör kan konfigurera privata innehållsmappar och ge åtkomst till specifika anpassade författare med hjälp av anpassade roller. Observera att standardförfattare (även kallade fullständiga författare) fortsätter att ha tillgång till allt innehåll i kontot. Därför har fullständiga författare tillgång till alla mappar och allt innehåll.

Innehållsmappar kan konfigureras av administratörer. Först när innehållsmappar har konfigurerats blir de synliga för författare och kan placera innehållet i en eller flera mappar.

Om du vill lägga till en innehållsmapp klickar du på **[!UICONTROL Settings]** > **[!UICONTROL Content Folder]** i administratörsappen.

![](assets/manage-content-folders.png)

*Ändra inställningar för innehållsmappen*

### Mapp

En mapp är en innehållsdatabas, som är en delmängd av hela innehållsbiblioteket som är tillgängligt på ett konto med följande egenskaper:

* Endast en administratör kan skapa, redigera eller ta bort en mapp.
* En administratör kan styra åtkomsten till mappar som en del av att definiera roller endast för anpassade administratörer.
* Innehållet **måste alltid associeras med minst en mapp**. Till att börja med kommer allt innehåll att vara kopplat till den gemensamma mappen, som senare kan ändras.
* Innehållet kan kopplas till flera mappar när det skapas, vilket också blir möjligt genom en kopiering
* Alla mappnamn måste vara unika i kontot, annars uppstår ett fel när en mapp namnges.

Mappar styr bara synligheten för innehållet och skapar inte kopior av innehållet. Därför visas redigering av innehåll i alla associerade mappar.

### mappen Gemensamma filer

En gemensam mapp finns alltid på ett konto och till att börja med kommer allt innehåll att vara en del av denna mapp. Senare kan författare flytta innehåll från den här mappen till andra mappar. En gemensam mapp har följande egenskaper:

* Allt innehåll kopplat till den här mappen är som standard tillgängligt för alla typer av författare.
* Innehåll som är en del av en gemensam mapp kan inte ingå i någon annan mapp. Det motsatta gäller också.

Den här mappen kan inte ingå i en konfigurerbar rolldefinition. Att inte ha en gemensam mapp i en konfigurerbar rolldefinition begränsar därför inte åtkomsten till en gemensam mapp.

### Privat mapp

* Alla mappar som skapas av en administratör är privata.

### Mappåtgärder

**Lägg till en mapp**

Om du vill lägga till en mapp klickar du på **[!UICONTROL Add]** i fönstrets övre högra hörn.

**Ta bort en mapp**

Du kan även ta bort en mapp. Markera mappen som ska tas bort, klicka på menyn Åtgärder och klicka sedan på **[!UICONTROL Delete Folder]**.

>[!NOTE]
>
>Mappar kan tas bort när allt associerat innehåll också är kopplat till andra mappar. Om det finns innehåll som är länkat till endast den mapp som tas bort flyttar du först innehållet till en annan mapp och tar sedan bort mappen.

## Klassrum

Administratörer kan använda den här inställningen för att skapa och konfigurera ett bibliotek med klassrumsplatser. Författare kan välja en förkonfigurerad plats för att konfigurera sina klassrumshändelser. Välj en plats från biblioteket för att automatiskt fylla i platsinformation, URL och platsgräns.

Som administratör kan du antingen:

### Importera CSV-platser

Lägg till platser i ditt konto genom att importera en CSV-fil med platser. CSV-filen måste innehålla kolumnen Ort.

### Lägg till en plats

Lägg till följande:

1. Platsnamn: Ange namnet på klassrummet.
2. Platsinformation: Ange information om platsen.
3. Platsregion: Det angivna värdet visas som filter för utbildningsplatser för elever.
4. Plats-URL: Ange platsens URL.
5. Platsbegränsning: Ange rummets sittplatskapacitet.

![klassrumsplats](assets/location-alm.gif)

*Lägg till klassrumsplatser*

Du kan även lägga till platsen med hjälp av en CSV-fil. CSV-filen måste innehålla fälten:

* name
* information
* URL
* Gräns för antal platser
* region

<!--![Add classroom locations](assets/add-classroom-csv.png)-->

### Inställningar {#admin-classroom-settings}

Välj **Redigera** för att ändra följande:

* **Tillåt författare att skapa platser**: När det här alternativet är aktiverat listas alla platser som har skapats av författare under fliken Alla platser. Elever kan också se de här platserna under Katalog- och kalenderfilter.
* **Tillåt författare att ändra och ta bort platser**:
När funktionen är aktiverad kan författare ändra och ta bort alla klassrumsplatser. Författarnas ändringar kommer att återspeglas på alla plattformar, inklusive rapporter.

## Vanliga frågor {#frequentlyaskedquestions}

+++Hur skapar man olika mappar för innehållsbiblioteket?

Klicka på **[!UICONTROL Settings]** > **[!UICONTROL Content Folder]**. För att lägga till en mapp, klicka på **[!UICONTROL Add]** i det övre högra hörnet och i dialogrutan anger du namnet och beskrivningen av mappen.

Innehållsmappar kan konfigureras av administratörer. Det är först när innehållsmapparna har konfigurerats som de blir synliga för författare och de kan placera innehållet i en eller flera mappar.

Mer information finns i avsnittet om [Innehållsmapp](settings.md#content-folder).
+++

+++Hur lägger man till räkenskapsår för kontot?

Klicka på **[!UICONTROL Change]** i **[!UICONTROL Settings]** > **[!UICONTROL Basic Info]**. Välj månad i listrutan **[!UICONTROL Financial year starts from]**.
+++
