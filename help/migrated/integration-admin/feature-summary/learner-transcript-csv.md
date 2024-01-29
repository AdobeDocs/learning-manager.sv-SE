---
jcr-language: en_us
title: Tolka elevens betygsutdrag CSV
description: Tolka elevens betygsutdrag CSV
contentowner: saghosh
preview: true
source-git-commit: fba5e5ddc1964b485be473bf356806f234688cf4
workflow-type: tm+mt
source-wordcount: '2997'
ht-degree: 0%

---



# Tolka elevens betygsutdrag CSV

Elevens betygsutdrag är ett av de mest omtyckta som används i Adobe Learning Manager. Rapporten gör det möjligt för en att få nästan alla möjliga detaljer i en enda rapport i CSV-format.

Förutom att vara en rapport som användare kan hämta för att spåra och analysera utbildningsbeteenden, kan rapporten också ses som det format i vilket Learning Manager kan konfigureras för att exportera data om utbildningsbeteenden till externa program/system.

Ett typiskt företagsscenario är att göra en periodisk export av elevens betygsutdrag för Learning Manager, analysera det för att extrahera elever som slutför ett viktigt utbildningsprogram och göra en beställning på en presentkort för att känna igen och belöna slutföranden i tid.

Ett annat användningsfall är att lägga till utbildningsbeteendedata i ett företagsdatalager, där man kanske vill kombinera utbildningsdata med andra företagsdata för att analysera korrelationer mellan utbildningsbeteende och andra processdata.

I resten av dokumentet beskriver vi kort hur du kan hämta elevens betygsutdrag från Learning Manager och sedan gå vidare till att tillhandahålla information om hur varje rad och kolumn i rapporten behöver tolkas.

Denna information kan vara användbar för alla utvecklare som avser att integrera Learning Manager med andra system genom att bearbeta de exporterade elevens betygsdata.

## Hämta elevens betygsutdrag från användargränssnittet {#fetchlearnertranscriptfromtheuserinterface}

Från Profilinställningarna kan en elev ladda ned sitt betygsutdrag. Mer information finns i *** [Ladda ned elevens betygsutdrag](../../administrators/feature-summary/learner-transcripts.md)***.

Administratörer kan generera elevbetygsutdrag för hela organisationen, en specifik uppsättning användare eller en specifik uppsättning utbildningsobjekt eller en specifik uppsättning användare och utbildningsobjekt. De kan också få alla utbildningsposter för ett tidsintervall och indikera om modulnivåinformation krävs (som standard utelämnas information på modulnivå). Mer information finns i [***Ladda ned elevens betygsutdrag***](../../administrators/feature-summary/learner-transcripts.md).

<!--Update above link?-->

Administratörer kan också konfigurera systemet för att regelbundet skicka e-post till elevens betygsutdrag.

Elevens betygsutdrag som genereras via gränssnittet kommer att vara en Excel-fil, som också innehåller &quot;Kompetensbetygsutdrag&quot;. I det här dokumentet hänvisar vi till vad som genereras i CSV-formatet, en rapport som innehåller utbildningsaktiviteter som gäller registrering, start, framsteg eller slutförande av ett utbildningsobjekt.

## Exportera elevens betygsutdrag {#exportlearnertranscript}

När elevens betygsutdrag måste förbrukas av ett externt system tillhandahåller Learning Manager en funktion som kallas Exportera data, där elevens betygsutdrag är en av de typer av data som kan exporteras. Som förklaras i ingressen krävs detta för integrering av Learning Manager med ett externt system som behöver bearbeta utbildningsbeteendedata eller för att fylla ett företags datalager med utbildningsbeteendedata.

Mer information om hur de kopplingar som stöder export av elevens betygsutdrag finns i [Avsnittet Exportera data](/help/migrated/integration-admin/feature-summary/connectors.md) i FTP-, Box- och PowerBI-anslutningarna.

Syftet med dessa kopplingar är att regelbundet exportera data till en nedströmsapplikation (en gång i N dagar). Så dessa kopplingar exporterar bara inkrementella data för utbildningsbeteende i varje körning. Observera att dessa anslutningar inte tillåter hämtning av poster som gäller en viss delmängd av användare eller utbildningsobjekt - det är alltid data om alla användare och alla utbildningsobjekt i kontot.

När det gäller PowerBI bör kunden tillhandahålla en arbetsyta där Learning Manager kan fortsätta att exportera dessa data stegvis till en dynamiskt skapad datauppsättning. Kopplingen exporterar bara data, och kunderna måste skapa sina egna rapporter/instrumentpaneler baserade på denna datauppsättning efter behov.

Nästa avsnitt innehåller information om hur ett nedströmssystem ska tolka posterna i elevens betygsutdrag.

## Tolka elevens betygsutdrag {#interpretthelearnertranscript}

Varje rad i en elevens betygsutdrag kan betraktas som något utbildningsbeteende som fångades i Learning Manager under en viss tidsperiod. Vanligtvis exporterar kopplingarna inkrementella data och därför representerar raderna utbildningsaktiviteter som inträffade mellan den senaste körningen av kopplingen och den aktuella körningen.

Kopplingarna ger dig naturligtvis även möjlighet att hämta elevens betygsutdrag på begäran, och i det här fallet kan användaren ange ett startdatum och slutdatumet antas vara nu. Vanligtvis skulle man göra detta en gång initialt och sedan ställa in anslutningen för att exportera den inkrementella elevens betygsutdrag vid en viss tid på dagen, en gång i N dagar (standardvärdet för N, som är 1).

Låt oss nu definiera vad som menas med inkrementell elevtranskribering

I elevens betygsutdrag representerar varje rad en specifik aktivitet som involverar en specifik elev och ett specifikt utbildningsobjekt. Vi är främst intresserade av vilket tillstånd en elev befinner sig i med avseende på utbildningsobjektet - **Registrerad**, **Startat**, **Pågår** och **Slutfört**. Därför innehåller elevens betygsutdrag även fyra motsvarande datum.

Nu finns det tre typer av utbildningsobjekt där Learning Manager spårar elevens framsteg och exporterade data innehåller statusinformation på modulnivå, vilket är den mest detaljerade innehållsenhet som en elev kan uppleva i Learning Manager.

* **Kurs** - en sammansättning av en eller flera moduler
* **Utbildningsprogram** - en sammansättning av en eller flera kurser,
* **Certifiering** - en sammansättning av en eller flera kurser.

Varje rad i elevens betygsutdrag kan gälla en viss användares engagemang i en modul, kurs, utbildningsprogram eller certifiering. När en användare registreras till ett utbildningsprogram kommer transkriptionen att ange att användaren är e

Kolumnerna i Elevens betygsutdrag innehåller olika delar av information som gäller varje utbildningsaktivitet, och följande tabeller beskriver semantiken i varje kolumn.

## Elevens betygsutdrag

<table> 
 <tbody> 
  <tr> 
   <th width="158" valign="bottom"><p><b>Kolumnnamn</b></p></th> 
   <th width="160" valign="bottom"><p><b>Typ av värde</b></p></th> 
   <th width="306" valign="bottom"><p><b>Beskrivning</b></p></th> 
  </tr> 
  <tr> 
   <td><p><b>Namn</b></p></td> 
   <td><p>Töm aldrig</p></td> 
   <td><p>Elevens namn</p></td> 
  </tr> 
  <tr> 
   <td><p><b>mejl</b></p></td> 
   <td><p>Töm aldrig</p></td> 
   <td><p>Elevens e-postadress</p></td> 
  </tr> 
  <tr> 
   <td valign="bottom"><b>Adobe ID</b></td> 
   <td valign="bottom">Kan vara tomt</td> 
   <td valign="bottom">Elevens Adobe ID</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Unikt användar-ID</b></td> 
   <td height="19" width="283">Kan vara tomt</td> 
   <td height="19" width="728">Elevens unika användar-ID. Den här kolumnen baseras på serverdelsinställningen om aktiverad/inaktiverad på kontonivå.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Namn på utbildningsplan</b></p></td> 
   <td valign="middle"><p>Kan vara tomt</p></td> 
   <td valign="middle">Namn på utbildningsplanen (om det finns någon) som användaren automatiskt har tilldelats till via.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>LP/Certifiering/Kurs</b></p></td> 
   <td valign="middle"><p>Töm aldrig</p></td> 
   <td valign="middle"><p>Utbildningsprogrammets, certifieringens eller kursens namn</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Text</b></p></td> 
   <td valign="middle">Töm aldrig</td> 
   <td valign="middle"><p>Typen av utbildningsobjekt som användaren registrerades till.</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Kurs</b></p></td> 
   <td valign="middle"><p>Kan vara tomt</p></td> 
   <td valign="middle">Namnet på kursen där användaren är registrerad. När det är tomt representerar raden antingen ett certifierings- eller utbildningsprogram. </td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>LO unikt ID</b></td> 
   <td height="19" width="283">Kan vara tomt</td> 
   <td height="19" width="728">Unikt LO-ID för utbildningsobjekt. Den här kolumnen baseras på inställningen om aktiverad/inaktiverad på kontonivå</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Instans  </b></p></td> 
   <td valign="middle">Töm aldrig</td> 
   <td valign="middle">Namnet på instansen av LO-användaren är registrerad i. </td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Urvalskriterier</b></p></td> 
   <td valign="middle"><p>Töm aldrig</p></td> 
   <td valign="middle"><p>Grunden för registrering (hur denna elev registrerades i denna LO).</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Modul</b></p></td> 
   <td valign="middle"><p>Kan vara tomt</p></td> 
   <td valign="middle">Namn på modul i kurserna. När den är tom representerar den här raden antingen en kurs, ett utbildningsprogram eller en certifiering.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Version</b></td> 
   <td height="19" width="283">Kan vara tomt</td> 
   <td height="19" width="728">Modulversion</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Leveranstyp</b></td> 
   <td height="19" width="283">Kan vara tomt</td> 
   <td height="19" width="728">Modulens leveranstyp - eLearning, F2F, VC, Aktivitet.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Språk</b></td> 
   <td height="19" width="283">Kan vara tomt</td> 
   <td height="19" width="728">Språk som modulen förbrukas av eleven. Den här kolumnen visar endast värdet för eLearning-moduler.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Kommentar</b></td> 
   <td height="19" width="283">Kan vara tomt</td> 
   <td height="19" width="728">Kommentarer som lagts till av administratören, instruktör för eleven, vid markering av användarnärvaro.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Registreringsdatum (tidszonen Asien/Calcutta)</b></td> 
   <td height="19" width="283">Töm aldrig</td> 
   <td height="19" width="728">Datum för elevens registrering till LO-typen.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Påbörjad datum (tidszonen Asien/Calcutta)</b></td> 
   <td><p>Kan vara tomt</p></td> 
   <td height="19" width="728">Datum då eleven startade LO. Om det är tomt innebär det att eleven inte har startat detta ännu.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Slutförandedatum (tidszonen Asien/Calcutta)</b></td> 
   <td><p>Kan vara tomt</p></td> 
   <td><p>Datum då eleven slutförde detta. Tomt innebär att eleven inte har slutfört detta ännu.</p></td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Deadline (tidszonen Asien/Calcutta)</b></td> 
   <td><p>Kan vara tomt</p></td> 
   <td height="19" width="728">Datum då eleven förväntas slutföra denna LO. Tomt innebär att det inte finns någon tidsfrist för detta.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Försenad</b></td> 
   <td height="19" width="283">Ja/nej</td> 
   <td height="19" width="728">Aktuell försenad status för eleven som är registrerad i LO. Ja/nej</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Status</b></p></td> 
   <td valign="middle">Inte påbörjat/slutfört/Pågår/Avregistrerat</td> 
   <td valign="middle">Aktuell förlopp i procent av eleven som är registrerad i LO.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Status %</b></p></td> 
   <td valign="middle">Kan vara tomt</td> 
   <td valign="middle"><p>Anger i vilken utsträckning eleven har slutfört detta.</p></td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Använd tid (minuter)</b></td> 
   <td height="38" width="283">Kan vara tomt</td> 
   <td height="38" width="728">Utbildningstid som använts av eleven i LO visar modulnivåraderna den individuella modulbaserade inlärningstiden. Nivåraderna för kursen/programmet/certifikatet visar den sammanlagda inlärningstiden.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Gradering</b></p></td> 
   <td valign="middle">Godkänt/ej godkänt</td> 
   <td valign="middle">Indikerar att eleven har lyckats. "Godkänt", om användaren har uppfyllt kriterierna för detta, annars "Misslyckat".</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Quiz-poäng</b></p></td> 
   <td valign="middle">Kan vara tomt</td> 
   <td valign="middle">Den senaste quiz-poängen som erhållits av eleven. Kan vara tomt om eleven inte har försökt genomföra frågeformuläret eller innehållet inte har något quiz i det eller admin/instruktör inte har tilldelat någon poäng.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Quiz_score_max</b></td> 
   <td height="38" width="283">Kan vara tomt</td> 
   <td height="38" width="728">Den senaste maximala quiz-poängen som är möjlig för modulen. Kan vara tomt om eleven inte har försökt utföra quiz eller om innehållet inte har något quiz.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Högsta quiz-poäng</b></td> 
   <td height="38" width="283">Kan vara tomt</td> 
   <td height="38" width="728">Högsta quiz-poäng som eleven fått vid flera försök. Kan vara tomt om eleven inte har försökt utföra quiz eller innehållet inte har något quiz i det eller admin / instruktör inte har tilldelat någon poäng.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Highest_Quiz_score_max</b></td> 
   <td height="38" width="283">Kan vara tomt</td> 
   <td height="38" width="728">Högsta möjliga quiz-poäng för modulen. Kan vara tomt om eleven inte har försökt utföra quiz eller om innehållet inte har något quiz.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Antal gjorda försök</b></td> 
   <td height="19" width="283">Kan vara tomt</td> 
   <td height="19" width="728">Det totala antalet försök som hittills har gjorts av eleven för denna modul.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Maximalt antal tillåtna försök</b></td> 
   <td height="19" width="283">Kan vara tomt</td> 
   <td height="19" width="728">Det maximala antalet tillåtna försök för eleven att konsumera modulen.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>användarstatus</b></p></td> 
   <td valign="middle">Töm aldrig</td> 
   <td valign="middle">Elevens användarstatus: Aktiv/Borttagen/Avstängd.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Grupperbart aktivt fält</b></td> 
   <td height="38" width="283">Kan vara tomt</td> 
   <td height="38" width="728">För varje grupperbart aktivt fält i kontot kommer det att finnas en kolumn, där kolumnnamnet är det för aktivt fält och värdet kommer att vara det specifika värdet som eleven har för det fältet.</td> 
  </tr> 
  <tr> 
   <td><p><b>Chefens namn</b></p></td> 
   <td><p><i>Kan vara tomt</i></p></td> 
   <td height="19" width="728">Elevens chefsnamn</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Antal registreringar</b></td> 
   <td height="38" width="283">1 eller 0</td> 
   <td height="38" width="728">Antal registreringar för eleven i LO. Den högsta LO-raden visar ett värde = '1'. På underutbildningen visas värdet 0.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Antal startade</b></td> 
   <td height="19" width="283">1 eller 0</td> 
   <td height="19" width="728">Antal elever för LO har startat. Den högsta LO-raden visar ett värde = '1'. På underutbildningen visas värdet 0.</td> 
  </tr> 
  <tr> 
   <td height="58" width="283"><b>Antal slutföranden</b></td> 
   <td height="58" width="283">1 eller 0</td> 
   <td height="58" width="728">Antal slutföranden för eleven i LO. Raden för högsta LO-nivån visar värdet = '1' om eleven väntar på slutförande av utbildningen. Underutbildningarna visar värdet 0 även i läget Väntande. Raden för högsta LO-nivån visar värdet = '0', om eleven har slutfört utbildningen.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Ska vara klar om N dagar</b></td> 
   <td height="38" width="283">1 eller 0</td> 
   <td height="38" width="728">Detta visar värdet '1' eller '0' beroende på instansdeadline för utbildaren som är registrerad för. Det beror på värdet som angetts i Utbildningssammanfattning I blad &gt; Inlämningsdatum kommer in.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Ska vara klar om N dagar för användare</b></td> 
   <td height="38" width="283">1 eller 0</td> 
   <td height="38" width="728">Detta visar värdet '1' eller '0' beroende på instansdeadline för utbildaren som är registrerad för. Det beror på det värde som angetts i utbildningssammanfattning II &gt; fältet Inlämningsdatum kommer in.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Antal (status större än N %)</b></td> 
   <td height="38" width="283">1 eller 0</td> 
   <td height="38" width="728">Detta visar värdet '1' eller '0' beroende på elevens framsteg under utbildningen. Det beror på värdet som angetts i Utbildningssammanfattning I blad &gt; fältet Status större än.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Antal (status större än N %) för användare</b></td> 
   <td height="38" width="283">1 eller 0</td> 
   <td height="38" width="728">Detta visar värdet '1' eller '0' beroende på elevens framsteg under utbildningen. Det beror på det värde som angetts i Utbildningssammanfattning II &gt; fältet Status större än.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283">T<b>ID för regn</b></td> 
   <td height="19" width="283">Töm aldrig</td> 
   <td height="19" width="728">Utbildningens utbildnings-ID.</td> 
  </tr> 
  <tr> 
   <td height="20" width="283"><b>Varaktighet för utbildning eller modul (min)</b></td> 
   <td height="20" width="283">Töm aldrig</td> 
   <td height="20" width="728">Total utbildningstid eller modullängd (min) för standardinstansen av utbildningen.</td> 
  </tr> 
 </tbody> 
</table>

### Sammanfattning av utbildning I

<table cellpadding="1" cellspacing="0" border="1"> 
 <tbody> 
  <tr> 
   <th>Kolumnnamn<br></th> 
   <th>Typ av värde</th> 
   <th>Beskrivning</th> 
  </tr> 
  <tr> 
   <td height="19" width="264">Text</td> 
   <td height="19" width="253">Alla, utbildningsprogram, certifikat, kurs.</td> 
   <td height="19" width="412">LO-typen som utbildningssammanfattningstabellen ska visa data för.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Grupperbart fält (profil)</td> 
   <td height="19" width="253">Töm aldrig</td> 
   <td height="19" width="412">Profilen som utbildningssammanfattningen ska visa data för.</td> 
  </tr> 
  <tr> 
   <td height="38" width="264">Chefens namn</td> 
   <td height="38" width="253">Töm aldrig</td> 
   <td height="38" width="412">Chefens namn, vars underordnade data för LO-engagemang ska visas i tabellen Sammanfattning av utbildning.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Radetiketter</td> 
   <td height="19" width="253">Töm aldrig</td> 
   <td height="19" width="412">LO-namnet med listan över elever som är registrerade i LO.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Antal registrerade elever</td> 
   <td height="19" width="253">Töm aldrig</td> 
   <td height="19" width="412">Antal elever som registrerats i LO.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Antal elever som har startat</td> 
   <td height="19" width="253">Töm aldrig</td> 
   <td height="19" width="412">Antal elever som har startat LO.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Antal elever som har slutfört</td> 
   <td height="19" width="253">Töm aldrig</td> 
   <td height="19" width="412">Antal elever som har slutfört LO.</td> 
  </tr> 
  <tr> 
   <td height="38" width="264">Antal elever som gjort framsteg &gt;= N %</td> 
   <td height="38" width="253">Töm aldrig</td> 
   <td height="38" width="412">Antal elever som gjort framsteg &gt;= N % (värden).</td> 
  </tr> 
  <tr> 
   <td height="39" width="264">Antal elever med inlämningsdatum om N dagar</td> 
   <td height="39" width="253">Töm aldrig</td> 
   <td height="39" width="412">Antal elever med inlämningsdatum om N dagar (värden).</td> 
  </tr> 
 </tbody> 
</table>

### Sammanfattning av utbildning II

| Kolumnnamn | Typ av värde | Beskrivning |
|---|---|---|
| Text | Alla, utbildningsprogram, certifikat, kurs. | LO-typen som utbildningssammanfattningstabellen ska visa data för. |
| Grupperbart fält (profil) | Töm aldrig | Profilen som utbildningssammanfattningen ska visa data för. |
| Chefens namn | Töm aldrig | Chefens namn, vars underordnade data för LO-engagemang ska visas i tabellen Sammanfattning av utbildning. |
| Radetiketter | Töm aldrig | Elevnamnet med listan över LO-elever är registrerat i. |
| Antal registrerade utbildningsobjekt | Töm aldrig | Antal utbildningsobjekt som eleven är registrerad till. |
| Antal påbörjade utbildningsobjekt | Töm aldrig | Antalet utbildningsobjekt som eleven har startat. |
| Antal slutförda utbildningsobjekt | Töm aldrig | Antal elever med utbildningsobjekt har slutfört. |
| Antal utbildningsobjekt med framsteg >= N % | Töm aldrig | Antal elever Objektelever har gjort framsteg >= N %. |
| Antal utbildningsobjekt med inlämningsdatum om N dagar | Töm aldrig | Antal utbildningsobjekt med inlämningsdatum om N dagar. |

### Sammanfattning av efterlevnad

| Kolumnnamn | Typ av värde | Beskrivning |
|---|---|---|
| Text | Alla, utbildningsprogram, certifikat, kurs. | LO-typen som utbildningssammanfattningstabellen ska visa data för. |
| Radetiketter (vänster sidokolumn) | Töm aldrig | Elevnamnet med listan över LO-elever är registrerat i. |
| Radetiketter (vänster sidokolumn) | Töm aldrig | Elevnamnet med listan över LO-elever är registrerat i. |

### Kompetensbetygsättning

| .Kolumnnamn | Typ av värde | Beskrivning |
|---|---|---|
| Namn | Töm aldrig | Elevens namn |
| mejl | Töm aldrig | Elevens e-postadress |
| Adobe ID | Kan vara tomt | Elevens Adobe ID |
| Unikt användar-ID | Kan vara tomt | Elevens unika användar-ID. Den här kolumnen baseras på serverdelsinställningen om aktiverad/inaktiverad på kontonivå. |
| Kompetens | Töm aldrig | Tilldelat kompetensnamn till eleven. |
| Kompetensnivå | Töm aldrig | Tilldelad kompetensnivå till eleven. |
| Poäng som krävs | Töm aldrig | Totala poäng som krävs av eleven för att uppnå kompetensen. |
| Intjänade poäng | Töm aldrig | Totala poäng som erhållits av eleven för kompetensen. |
| Andel slutfört | Töm aldrig | Förloppsprocent för att uppnå kompetensen. |
| Tilldelat datum (tidszonen UTC) | Töm aldrig | Datum då kompetensen tilldelades eleven. |
| Uppnått datum (tidszonen UTC) | Töm aldrig | Datum då eleven uppnådde kompetensen. |
| användarstatus | Töm aldrig | Elevens användarstatus: Aktiv/Borttagen/Avstängd. |
| Grupperbart aktivt fält | Kan vara tomt | För varje grupperbart aktivt fält i kontot kommer det att finnas en kolumn, där kolumnnamnet är det för aktivt fält och värdet kommer att vara det specifika värdet som eleven har för det fältet. |
| Chefens namn | Kan vara tomt | Elevens chefsnamn. |

### Sammanfattning av kompetens I

| Kolumnnamn | Typ av värde | Beskrivning |
|---|---|---|
| Efter | Töm aldrig | Antal elever som uppnådde kompetensen, före angivet (värde) antal dagar som behöver fräschas upp. |
| Namn | Namn på alla eller alla elever | Elevens namn som har tilldelats en kompetens. |
| Chefens namn | Töm aldrig | Chefens namn, vars underordnade data om kompetensintegrering ska visas i registret Kompetenssammanfattning. |
| Radetiketter | Töm aldrig | Kompetensnamnet med listan över elever som har tilldelats kompetensen. |
| Antal användare som ska ha denna kompetens | Töm aldrig | Antal elever som har tilldelats kompetensen. |
| Antal användare som har erhållit den här kompetensen | Töm aldrig | Antal elever som har uppnått kompetensen. |
| Antal elever vars kompetens behöver fräschas upp | Töm aldrig | Antal elever vars kompetens behöver fräschas upp. |
| Andel efterlevnad (baserat på uppnådd kompetens) | Töm aldrig | Förloppsprocenten för den tilldelade kompetensen. |

### Sammanfattning av kompetens II

| Kolumnnamn | Typ av värde | Beskrivning |
|---|---|---|
| Efter | Töm aldrig | Antal elever som uppnådde kompetensen före det angivna (värde) antalet dagar som behöver fräschas upp. |
| Kompetens | Namn på alla eller alla kompetenser | Kompetensnamnen som tilldelas elever. |
| Chefens namn | Töm aldrig | Chefens namn, vars underordnade data om kompetensintegrering ska visas i registret Kompetenssammanfattning. |
| Radetiketter | Töm aldrig | Elevens namn med listan över tilldelade kompetenser. |
| Antal kompetenser varje användare ska ha | Töm aldrig | Antal kompetenser som har tilldelats eleven. |
| Antal kompetenser varje användare har | Töm aldrig | Antal kompetenser som uppnåtts av eleven. |
| Antal kompetenser som behöver fräschas upp | Töm aldrig | Antal elever vars kompetens behöver fräschas upp. |
| Andel efterlevnad | Töm aldrig | Förloppsprocenten för den tilldelade kompetensen. |

* Ibland kan administratörer markera slutförande för ett utbildningsobjekt manuellt (särskilt för klassrumskurser) mycket efter klassen. I ett sådant scenario, om Exportera data är inställda för att exportera LT dagligen, kan det faktiska slutförandedatumet redan ha passerats och exporten kommer därför aldrig att få sådana slutförandeposter som markerades som slutförda långt efter att klassen inträffade. När detta upptäcks bör du överväga att exportera transkriptionen från ett visst startdatum till ett visst datum (på begäran) i användargränssnittet och sedan ta den till det efterföljande programmet för &quot;sen bearbetning&quot;. När du gör det kan du behöva ignorera poster som redan har bearbetats.
* Flera försök för en modul beror på om det är aktiverat för den LO:n. När det här alternativet är aktiverat ser du nu ett försök i en CSV-rad som är relaterad till en modul. Alla försök under en dag kanske inte rapporteras, så du kan se det totala antalet försök som ökas med mer än ett. Även ett försök kanske inte nödvändigtvis förbättra en poäng, och vid varje givet tillfälle kommer du bara att få den bästa poängen.
