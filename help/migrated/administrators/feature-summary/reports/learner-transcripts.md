---
description: Elevens betygsutdrag i Adobe Learning Manager (ALM) ger administratörer möjlighet att övervaka elevens framsteg inom kurser, moduler, utbildningsvägar och certifieringar. Den stöder resultatutvärderingar, efterlevnadsövervakning, revisioner och extern rapportering. Rapporten ger en fullständig sammanfattning av en elevs engagemang och resultat.
jcr-language: en_us
title: Elevens betygsutdrag i Adobe Learning Manager
source-git-commit: 6fceea6cc1f5fbe47e0dbb211cfb9e2de67957f6
workflow-type: tm+mt
source-wordcount: '4775'
ht-degree: 4%

---


# Elevens betygsutdrag i Adobe Learning Manager

## Översikt

Elevens betygsutdrag i Adobe Learning Manager (ALM) ger administratörer möjlighet att spåra elevens framsteg på detaljnivå genom kurser, moduler, utbildningsvägar och certifieringar. Transkriberingsdata hjälper till vid prestationsgranskningar, efterlevnadsspårning, revisioner och externa rapporteringsbehov.

>[!NOTE]
>
>Elevens betygsutdrag är tillgängliga för hämtning av administratörer, anpassade administratörer, chefer eller elever.

Nedladdningsupplevelsen för elevens betygsutdrag och den resulterande filen skiljer sig åt beroende på användarroll. Administratörer och anpassade administratörer kan generera utskrifter för flera elever och ha tillgång till bredare datauppsättningar, medan eleverna bara kan ladda ned sina egna utskrifter via sina profilinställningar. Gränssnittet för nedladdning varierar också: administratörer använder avsnittet Rapporter, medan elever hämtar transkriptioner från sin profil. De hämtade filerna kan innehålla olika kolumner och detaljnivåer beroende på roll och behörigheter.

För elever måste de öppna sina profilinställningar och sedan hämta utbildningsutskrifterna som en Excel-fil. Den här transkriptionen, som har genererats för en enskild elev, beskriver deras personliga inlärningsresa. Den innehåller namnen på utbildningsvägar, kurser, instanser och moduler samt viktiga datum som registrering, slutförande och slutdatum. Den spårar också deras framsteg genom status, betyg, quizpoäng (inklusive högsta poäng och maximumpoäng) och gjorda försök. Dessutom visas utbildnings-ID, varaktighet, datum för avregistrering, priser och eventuella inlämningskommentarer. Denna rapport ger en omfattande översikt över en enskild elevs engagemang och resultat.

Organisationer kan använda Elevens betygsutdrag för att lägga till data om utbildningsbeteenden i ett företagsdatalager, där man kan kombinera utbildningsdata med andra företagsdata för att analysera korrelationer mellan utbildningsbeteende och andra processdata.

## Syfte och fördelar

* Skapar granskningsfärdiga poster för myndighetskrav med tidsstämplar och bevis på slutförande.
* Kopplar utbildningsaktiviteter till medarbetarutveckling och kompetensutveckling.
* Spårar certifieringsstatus för roller som kräver obligatorisk utbildning.
* Stödjer kvantitativ mätning av utbildningsprogrammets effektivitet.

## Användningsfall för elevbetygsutdrag

Elevens BETYGSUTDRAG i Adobe Learning Manager spårar utbildning, regelefterlevnad och kompetensutveckling, vilket gör det möjligt för avdelningar att verifiera slutförande och bedöma programmets effektivitet i hela organisationen.  Följande användningsfall visar hur Elevens betygsutdrag stöder organisationens behov av efterlevnad, kompetensspårning och effektivitet i programmet.

* En organisation för finansiella tjänster måste styrka att alla kundinriktade anställda har genomgått obligatorisk efterlevnadsutbildning före den föreskrivna tidsfristen.
* IT-avdelningen behöver utvärdera befintliga Java-programmeringsfunktioner mot framtida projektkrav.
* HR vill utvärdera hur effektivt det nya medarbetarintroduktionsprogrammet är på olika avdelningar.
* Driftsteamet måste säkerställa att alla fälttekniker upprätthåller de säkerhetscertifieringar som krävs.

## Åtkomstkontroll och behörigheter

**Administratörer**

* Administratörer kan generera utskrifter för alla elever i alla kataloger.
* Anpassade administratörer kan bara visa utskrifter för elever inom sina tilldelade användargrupper och kataloger.

**Omfångsbaserade begränsningar**

* Anpassade administratörer kan bara visa utskrifter för elever inom sina tilldelade användargrupper.
* Rapporter innehåller endast utbildningsobjekt från kataloger som administratören har behörighet att komma åt.

## Så här genererar du elevbetygsutdrag

1. Logga in på Adobe Learning Manager som administratör.
2. Välj **[!UICONTROL Reports]** från den vänstra navigeringsmenyn.
3. Välj **[!UICONTROL Custom Reports]** i Rapporter och välj sedan **[!UICONTROL Excel Reports]**.
4. Välj **[!UICONTROL Learner Transcripts]**.
5. Välj **[!UICONTROL Generate New]**.
6. Välj det datumintervall som du vill att transkriptionen ska genereras för. Du kan ändra både start- och slutdatum med alternativet **[!UICONTROL Choose dates]** i listrutan Datumintervall.
7. Markera följande:
a. Välj elevernas namn i avsnittet **[!UICONTROL Select Learners]**. Du kan välja användare eller användargrupper, eller så kan du kopiera och klistra in e-postadresserna till de elever som du vill generera utskrifter för. Se avsnittet [Generera elevens betygsutdrag](#generate-learner-transcript-using-copy-paste) med kopiera och klistra in för mer information. Om du inte markerar något används standardinställningen Alla värden.
b. Välj specifika kataloger i listrutan **[!UICONTROL Select Catalogs]**. Transkriptionen laddas bara ned för de angivna katalogerna. Om du inte markerar något används standardinställningen Alla värden.
c. Välj **[!UICONTROL Enrollment Status]**. Den här listrutan innehåller följande alternativ:

       * Välj alla
       * slutfört
       * Pågår
       * HAR INTE STARTATS
       * avregistrerad
   &#x200B;8. Avancerade alternativ: Välj **[!UICONTROL Advanced options]** för att hämta utskrifterna och inkludera följande:

   a. Ladda ned utskrifter för elever som har tagits bort från ett konto genom att markera kryssrutan **[!UICONTROL Include deleted Learners]**.
b. Ladda ned information om modulnivå i elevens betygsutdrag genom att aktivera kryssrutan **[!UICONTROL Enable module level information]**. I det här fallet hämtas modulnamn och den tid som används för varje modul som en del av utskriften om det här alternativet är aktiverat.
c. Ladda ned kompetensdata och sammanfattningsblad genom att markera kryssrutan **[!UICONTROL Include skills data and summary sheets]**. Mer information finns i avsnittet Excel-rapporter.
&#x200B;9. Du kan också välja vilka kolumner som ska fyllas i i rapporten. Det ger flexibilitet att hämta rapporter med specifika kolumnvärden efter behov. Välj kolumnerna i listrutan.
Betygsutdrag genereras och laddas ned till din dator som .zip-filer när kompetensdata inte ingår. Om kryssrutan Kunskapsdata är aktiverad genereras och hämtas utskrifter som . xlsx-filer.

### Generera elevens betygsutdrag med kopiera och klistra in

Att hämta elevens betygsutdrag blir en omständlig process eftersom det bara kan erhållas för en elev eller användargrupp en i taget. Med funktionen för att kopiera och klistra in kan du här kopiera listan över elevens e-postadresser och klistra in den på en gång.

1. Välj fliken **[!UICONTROL Email IDs]** för att ange den kopierade listan över unika e-postadresser.
2. Klistra in unika ID:n för elever som du vill lägga till separerade med ett komma, semikolon eller radbrytning.
3. Välj **[!UICONTROL Validate Emails Ids]** för att kontrollera om det e-post-ID som du har angett är giltigt. Om den angivna e-postadressen är felaktig markeras den med rött tillsammans med ett valideringsmeddelande.

   >[!NOTE]
   >
   >Knappen Generera förblir inaktiverad om inte alla angivna e-post-ID:n är korrekta.

4. Välj **[!UICONTROL Generate]** för att generera elevens betygsutdrag för alla nämnda e-postadresser.

   >[!NOTE]
   >
   >Generering av elevtranskriberingar kan kombineras för e-post-ID som anges på fliken Användare och e-post-ID.

### Vad innehåller rapporten Elevens betygsutdrag

Rapporten Elevens betygsutdrag är en kombination av användar-, registrerings- och utbildningsobjektsrelaterad information.
Följande tabeller beskriver varje typ:

**Användarrelaterad information**

Följande kolumner identifierar eleven.

| Fält | Beskrivning |
|---|---|
| Namn | Elevens namn. |
| E-post | Elevens e-postadress. |
| Adobe ID | Det här fältet fylls bara i när användare loggar in med sina Adobe ID. Om de har tillgång till Adobe Learning Manager via en organisationsdefinierad [enkel inloggning (SSO)](/help/migrated/administrators/feature-summary/multiple-sso-logins.md) är Adobe ID-fältet tomt. |
| Unikt användar-ID | Unikt användar-ID är ett externt ID som genereras av konton om de inte har e-post-ID:n för alla användare, eller unika e-post-ID:n för alla användare.  <br>Fältet unikt användar-ID är ett valfritt fält som kan aktiveras för ett konto. Huvudsyftet med fältet är att tillåta konton att tagga varje användare med ett unikt ID för att spåra dem, uppdatera användarposter via API:er, granska eller synkronisera data i automatiserade arbetsflöden. Varje användare taggas via CSV-import av användare.Adobe Learning Manager </br><br>Om ett konto har valt Unikt användar-ID anges kolumnen i rapporterna, till exempel elevens betygsutdrag.</br> |

**Registreringsrelaterad information**

Följande kolumner visar aktivitet, förlopp eller försök.

| Fält | Beskrivning |
|---|---|
| Registreringsdatum (tidszonen UTC) | Datum- och tidsstämpel för elevens registrering till typen av utbildningsobjekt, vilket är kurs, certifiering eller utbildningsväg. |
| Markera som slutförandedatum (tidszonen UTC) | Datum- och tidsstämpel för när en instruktör markerar en session eller modul som slutförd. Observera att om en session inte har ägt rum visas kolumnen tom i rapporten. Om en session har inträffat och instruktören inte har markerat sessionen som slutförd visas kolumnen tom i rapporten. |
| Påbörjad datum (tidszonen UTC) | Datum och tid då eleven startade utbildningsobjektet. Om det är tomt innebär det att eleven inte har startat detta ännu. |
| Slutförandedatum (tidszonen UTC) | Datum och tid då eleven slutförde detta. Tomt innebär att eleven inte har slutfört detta ännu. |
| Markera som slutförandedatum (tidszonen UTC) | Fångar det exakta datumet och den exakta tiden när en instruktör markerar en session eller modul som slutförd. |
| Deadline (tidszonen UTC) | Datum och tid då eleven förväntas slutföra detta utbildningsobjekt. Tomt innebär att det inte finns någon tidsfrist för detta. |
| Försenad | Aktuell försenad status för eleven som är registrerad för utbildningsobjektet. Ja/nej |
| Status | Anger elevens status vid genomgång av kurs, certifiering eller utbildningsväg.  De tillgängliga statusarna har inte startats, avregistrerats, pågår eller slutförts. |
| Status % | Aktuell förlopp % av eleven som deltar i kursen, certifieringen eller utbildningsvägen. |
| Använd tid (minuter) | Utbildningstid som eleven tillbringar i LO visar modulnivåraderna den individuella modulbaserade inlärningstiden. Raderna Kurs/utbildningsväg/Certifikatnivå visar den sammanlagda inlärningstiden. |
| Gradering | Anger om eleven lyckats. &quot;Godkänt&quot;, om användaren har uppfyllt kriterierna för detta, annars &quot;Misslyckat&quot;. |
| Quizpoäng | Den senaste quiz-poängen som erhållits av eleven. Kan vara tomt om eleven inte har försökt genomföra frågeformuläret eller innehållet inte har något quiz eller om administratören/instruktören inte har tilldelat någon poäng. Kolumnen används för att registrera poängen från det senaste försöket i ett quiz. Om en användare till exempel gör flera försök (till exempel får 10, 50 och 30 poäng på tre försök) kommer kolumnen Quiz_score att visa poängen från det senaste försöket, som är 30. Anta att ett quiz har en högsta poäng på 100 och att en användare gör tre försök med poängen 30, 60 och 90. I kolumnen Quiz_score visas 90 (den senaste poängen), medan poängen för Highest_Quiz_score visar 90 (den bästa poängen för alla försök) och Quiz_score_max förblir 100 (den högsta möjliga poängen). |
| Quiz_score_max | De senaste maximala quiz-poängen som är möjliga för modulen. Det kan vara tomt om eleven inte har försökt utföra quiz eller om innehållet inte har några quiz. Kolumnen Quiz_score_max representerar det högsta möjliga poängvärdet som kan uppnås för ett visst quiz eller en viss modul. Eftersom Quiz_score_max förblir konstant är det användbart i rapporter att visa den totala uppnåeliga poängen för ett quiz eller en modul, oavsett användarens prestanda. |
| Högsta quizpoäng | Kolumnen Highest_Quiz_score representerar det högsta poäng som en användare får för alla försök i ett visst quiz. Om en användare till exempel gör tre försök med poängen 10, 20 och 15 kommer poängen för Highest_Quiz_score att visa 20, eftersom det är den högsta poängen som uppnås. |
| Highest_Quiz_score_max | Högsta möjliga quiz-poäng för modulen. Det kan vara tomt om eleven inte har försökt utföra quiz eller om innehållet inte har några quiz. Högsta möjliga poäng som associeras med det högsta quiz-poängförsöket som en elev gjort vid flera försök. Det är inte den högsta poäng som eleven har uppnått. Istället ger den maximala poäng som var möjlig i försöket där eleven gjorde sitt högsta. |
| Antal gjorda försök | Det totala antalet försök som har gjorts av eleven hittills för denna modul. |
| Max antal tillåtna försök | Det maximala antalet försök som tillåts för eleven att konsumera modulen. |
| Kommentarer till ansökan | Kommentarer från en elevs chef efter att denne har slutfört ett utbildningsobjekt.<br>Data för inskickade kommentarer från instruktören ingår i modulen för inskickade filer. Mer information finns i <a href="https://experienceleague.adobe.com/en/docs/learning-manager/using/instructor/modules#filesubmissionforactivitymodules">Modules-Adobe Learning Manager.</a></br> |
| Källa för slutförande | Avser ursprunget eller metoden genom vilken en elevs slutförande av en kurs, utbildningsväg eller certifiering registreras. Det hjälper administratörer att förstå hur slutförandet uppnåddes eller loggades i systemet. Kolumnen anger om slutförandet har rapporterats av dig själv eller underlättats av en viss roll eller konfiguration. Obs! När en elev markeras som närvarat automatiskt vid VC-anslutningsarbetsflöden kommer källan att visa &quot;SELF, &lt;elevs_e-postadress>&quot;. |
| Kommentar kring slutförande | Administratörens kommentarer när denne markerar en elev som slutförd efter att denne har slutfört en kurs, certifiering eller utbildningsväg. Administratören kan lägga till slutförandekommentarer för en eller flera elever. |

**Information relaterad till utbildningsobjekt**

Dessa avser kurser, moduler, utbildningsvägar, certifieringar och så vidare.

| Fält | Beskrivning |
|---|---|
| Namn på utbildningsplan | Utbildningsplanens titel. |
| LP/Certifiering/Kurs | Utbildningsobjektets titel. |
| Typ | Typen av utbildningsobjekt som användaren var registrerad för. Exempel:<ul><li>Utbildningsväg</li><li>Certifiering</li><li>Kurs</li></ul> |
| Inbäddad väg | En inbäddad bana är en typ av utbildningsväg som ingår i en annan kurs eller utbildningsväg. Fältet anger att en elev slutför utbildningsvägen som en del av en annan utbildningsväg i stället för som en fristående uppgift. |
| Kurs | Namnet på kursen där användaren är registrerad. När den är tom representerar raden antingen en certifierings- eller utbildningsväg. <br><b>Obs!</b> Även om utbildningsvägar och utbildningar består av enskilda kurser eller kapslade utbildningsvägar, behåller varje komponent sin egen oberoende post. Detta säkerställer att framsteg, slutförande och rapporteringsdata spåras separat för både det överordnade och det underordnade elementet.</br> |
| LO unikt ID | Det här är en valfri, administratörstilldelad identifierare för ett utbildningsobjekt (kurs, certifiering eller utbildningsväg) i Adobe Learning Manager. Det används främst av organisationer som har sina egna externa system-id för utbildningsinnehåll och som vill mappa dessa id till ALM-utbildningsobjekt för integrerings- eller rapporteringsändamål. Det LO-unika ID:t finns bara om kontot har aktiverat den här funktionen och författaren har tilldelat ett ID under skapandet av LO. Obs! Utbildnings-ID:t finns alltid och identifierar varje utbildningsobjekt i ALM på ett unikt sätt. LO-unikt ID är avsett för mappning mellan system och krävs inte för ALM-standardåtgärder. |
| Instans | Namnet på instansen för användaren av utbildningsobjektet är registrerat i. |
| Urvalskriterier | Denna kolumn anger hur eleven registrerades för utbildningsobjektet (kurs, certifiering eller utbildningsväg). Värdet fastställs enligt följande:<ul><li>Admin/Manager-registrering: Visar direkt när en elev registreras direkt av en administratör eller chef. </li><li>Registrering till utbildningsplan: Visar automatiskt registrerade när en elev registreras via en utbildningsplan eller utlösare för automatisk registrering.</li><li>Administratören registrerar användargrupp: Visar användargruppsnamnen om eleven registrerades som en del av en användargrupp. </li><li>Kapslade utbildningsvägar: Om utbildningsväg 1 innehåller utbildningsväg 2, som innehåller kurs A: För LP2 och kurs A, är värdet överordnat. För LP1 är värdet direkt. </li><li>Självregistrering: visar sig själv när eleven registrerar sig. </li></ul>Värdet i den här kolumnen återspeglar den faktiska registreringsmetoden och LO-hierarkin, enligt beskrivningen ovan.<ul><li>Registrering av elev i utbildningsplan: Värde: Autoregistrerad Eleven registreras automatiskt via en utbildningsplan eller utlösare för automatisk registrering. </li><li>Elever som registrerar sig: Värde: Själv Eleven registrerar sig direkt för kursen, certifieringen eller utbildningsvägen. </li>Admin - registrera eleven direkt (med elevens e-postadress/namn): Värde: Direkt. Administratören eller chefen registrerar eleven manuellt genom att ange elevens e-postadress eller namn. <li>Registrering via en användargrupp: Värde: Användargruppnamn Eleven är registrerad som en del av en användargrupp. Om en elev tillhör flera användargrupper visar rapporten de relevanta användargrupper som registreringen skedde genom.  </li><li>Utbildningsobjekt registrerat på grund av registrering i utbildningsväg: värde: sökväg. Eleven är registrerad till en kurs eller modul eftersom den ingår i en större utbildningsväg som hen har tilldelats.</li></ul> |
| Modul | Namn på modul i kurserna. Endast de moduler som har statusen Slutfört eller Pågår visas i rapporten. Om statusen inte har startats eller avregistrerats förblir kolumnen Modul tom.<br>Hämta information på modulnivå i elevens betygsutdrag genom att markera kryssrutan <b>Aktivera information på modulnivå</b>. I det här fallet hämtas modulnamn och tiden som används för varje modul som en del av transkriptionen om det här alternativet är aktiverat.</br> |
| Modul-ID | Namn på modul i kurserna.  Endast de moduler som har statusen Slutfört eller Pågår visas i rapporten. Om en modul inte har startats av eleven visas inte raden för den modulen i elevens betygsutdrag. Endast moduler med status Slutfört eller Pågår inkluderas. Hämta information på modulnivå i elevens betygsutdrag genom att markera kryssrutan Aktivera information på modulnivå. I det här fallet hämtas modulnamn och den tid som används för varje modul som en del av utskriften om det här alternativet är aktiverat. |
| Modul-ID | Modulens unika ID. Obs! Kolumnen Modul-ID visas bara i rapporten om du har markerat kryssrutan Inkludera modulinformation när du genererar transkriptionen. |
| Version | Modulversionen refererar till den specifika versionen av en modul som en elev har interagerat med. Detta är särskilt användbart när en modul har genomgått uppdateringar eller ändringar, eftersom det gör det möjligt för administratörer att spåra vilken version av modulen som användes av eleven.<br>När en författare överför en ny modulversion behandlar Adobe Learning Manager den som en ny version av den befintliga modulen. Det gör att innehållet kan uppdateras utan att alla elever störs.</br><br>Versionen visas om kryssrutan <b>Aktivera modulnivåinformation</b> markerades när rapporten skapades.</br><br>Mer information finns i <a href="https://elearning.adobe.com/2023/03/updating-the-module-in-adobe-learning-manager-how-to-replace-a-content-module-in-a-course-without-disturbing-the-users-progress" />Uppdatera en modul i Adobe Learning Manager</a>.</br> |
| Leveranstyp | Anger hur modulen levereras: blandat klassrum, klassrum eller virtuellt klassrum. |
| Språk | Språk som modulen förbrukas av eleven. Den här kolumnen visar endast värdet för eLearning-moduler. |
| Gradering | Anger om eleven lyckats. &quot;Godkänt&quot;, om användaren har uppfyllt kriterierna för detta, annars &quot;Misslyckat&quot;. |

>[!INFO]
>
>Följande kolumner är dolda i Elevens betygsutdrag:
>
>* Antal registreringar
>* Antal startade
>* Antal slutföranden
>* Ska vara klar om N dagar
>* Ska vara klar om N dagar för användare
>* Antal (status större än N %)
>* Antal (status större än N %) för användare
>
>Dessa kolumner visas bara om du har markerat Inkludera kompetensdata och sammanfattningsblad när transkriptionen genereras. Dessa kolumner används för att beräkna sammanfattningsdetaljer för en elev som är registrerad för ett utbildningsobjekt.

| Fält | Beskrivning |
|---|---|
| Utbildnings-ID | En systemgenererad unik identifierare som tilldelas varje utbildningsobjekt (kurs, certifiering eller utbildningsväg). Utbildnings-ID:et är detsamma för alla elever och alla registreringar av detta utbildningsobjekt. Det används för att identifiera själva innehållet, inte enskilda elevregistreringar. |
| Varaktighet för utbildning eller modul (min) | I den här kolumnen visas förväntad varaktighet (i minuter) för en kurs, modul eller utbildningsaktivitet enligt definitionen när kursen skapades. Det är inte den faktiska tid en elev tillbringar, utan den konfigurerade/tilldelade varaktigheten som representerar hur lång utbildningen förväntas ta.  Den här kolumnen visar den totala varaktigheten (i minuter) för det tilldelade utbildningsobjektet, som kan vara antingen en utbildningsväg eller en enskild kurs. <br><b>Varaktighet för utbildningsväg:</b> Om utbildningsobjektet är en utbildningsväg beräknas varaktigheten som summan av varaktigheterna för alla kurser i utbildningsvägen.</br><br>Exempel: Om kurs 1 = 50 min och kurs 2 = 60 min, gäller längden på utbildningsvägen = 110 min.</br><br><b>Enskild kurslängd:</b>Om utbildningsobjektet är en enskild kurs (inte en del av en utbildningsväg) återspeglar varaktigheten den tid som krävs för enbart den kursen.</br> |
| Embedded_Course_ID | Kolumnen fylls i när raden representerar en utbildningsväg eller själva certifieringen. Den visar id:n för de enskilda kurser som är inbäddade i utbildningsvägen eller certifieringen. Det fylls inte i när raden i sig är en kurs eftersom det inte finns några inbäddade objekt. |
| Inbäddat väg-ID | Kolumnen identifierar det unika id:t för inbäddade utbildningsvägar. Det hjälper dig att hålla koll på kurser inom utbildningsvägar och ger dig insyn i den hierarkiska strukturen för utbildningsvägar. |
| Avregistreringsdatum (tidszonen UTC) | Datum då eleven avregistrerat sig för typen av utbildningsobjekt. |
| Pris($) | Priset på utbildningsobjektet som det har köpts för från kurskatalogen. För att den här kolumnen ska visas i elevens betygsutdrag måste administratören aktivera kryssrutan Aktivera priser för kurser > Utbildningsvägar > Certifieringar från kontoinställningarna. |

## Excel-rapporter

I dialogrutan Elevens betygsutdrag kan du även ladda ned kompetensdata och sammanfattningar som Excel-filer. Markera kryssrutan **[!UICONTROL Include Skills data and summary sheets]** och välj sedan **[!UICONTROL Generate]** för att hämta en Excel-fil med följande blad:

* Sammanfattning av utbildning I
* Sammanfattning av utbildning II
* Sammanfattning av efterlevnad
* Betygsutdrag för kompetensen
* Sammanfattning av kompetens I
* Sammanfattning av kompetens II

### Vad innehåller utbildningssammanfattningen?

Håll koll på utbildningsvägar, kurser eller certifieringar som används aktivt. Håll koll på pågående aktivitet samt kommande datum då utbildning ska vara genomförd.

* Antal registrerade elever: Anger hur många elever som har registrerats för ett visst utbildningsobjekt (kurs, utbildningsväg eller certifiering), oavsett om de har påbörjat det eller inte.
* Antal elever som har startat: Visar antalet elever som har startat eller startat kursen, certifieringen eller utbildningsvägen.
* Antal elever som har slutfört: Visar hur många elever som har slutfört utbildningen och uppfyller alla dess kriterier för slutförande.
* Antal elever som har gjort framsteg ≥ N%: återspeglar antalet elever som har uppnått minst det angivna tröskelvärdet för framsteg (t.ex. 70%) i utbildningen, även om de inte har slutfört den.
* Antal elever med inlämningsdatum om N dagar: Anger hur många elever som har utbildning som ska vara klar inom de kommande N dagarna (t.ex. 7 dagar), vilket är användbart för att identifiera kommande deadlines.

### Hur data ska tolkas

I den här utbildningssammanfattningen som jag rapporterar finns två utbildningsvägar som har tilldelats eleven.

* Användaren är registrerad i två utbildningsvägar och har startat båda.
* Ingen av utbildningsvägarna har slutförts än.
* Eleven har ännu inte kommit längre än tröskelvärdet på 70 % på någon av banorna.
* Inga förfallodatum infaller inom de närmaste sju dagarna för någon av utbildningarna.

### Vad innehåller sammanfattning av utbildning II?

Spåra utbildningsaktivitet per elev. Spåra registreringar, pågående aktivitet samt slutdatum för elever.

* Antal registrerade utbildningsobjekt: Totalt antal utbildningsobjekt (LO) som eleven är registrerad för i varje kurs, certifiering eller utbildningsväg.
* Antal påbörjade utbildningsobjekt: Anger hur många av de registrerade utbildningsobjekten som eleven har startat eller startat.
* Antal slutförda utbildningsobjekt: visar hur många av de påbörjade LO:erna som eleven har slutfört helt.
* Antal utbildningsobjekt med framsteg ≥ N%: återspeglar antalet LO där eleven har uppnått minst den angivna tröskelnivån för framsteg (i detta fall 70%).
* Antal utbildningsobjekt med inlämningsdatum om N dagar: Identifierar LO:er som förfaller inom ett angivet antal dagar (i det här fallet 7 dagar), vilket hjälper till att hålla koll på kommande deadlines.

### Hur data ska tolkas

* Eleven är registrerad i två utbildningsobjekt och har påbörjat båda.
* Inga utbildningsobjekt har slutförts.
* Eleven har ännu inte nått 70% framsteg i någon av dem.
* Inget av utbildningsobjekten förfaller inom de kommande 7 dagarna.

### Vad innehåller formuläret för överensstämmelsesammanfattning?

Håll koll på elever som har kommande inlämningsdatum för viktiga kurser, utbildningsvägar eller certifieringar.

| Kolumn | Beskrivning |
|---|---|
| Typ | LO-typen som utbildningssammanfattningen ska visa data för. |
| Radetiketter (vänster sidokolumn) | Elevnamnet med listan över LO som eleven är registrerad för. |

### Vad innehåller bladet för kunskapsöverföring

| Kolumn | Beskrivning |
|---|---|
| Namn | Fullständigt namn på eleven som är associerad med kompetensbeviset. |
| E-post | Elevens e-postadress. |
| Unikt användar-ID | Organisationsdefinierad unik identifierare för eleven. |
| Kompetens | Namnet på kompetensen som har tilldelats eleven (till exempel Java-programmering, ledarskap). |
| Kompetensnivå | Kunskapsnivån inom den kompetens som eleven förväntas uppnå (t.ex. Nybörjare, Mellannivå, Avancerat). |
| Poäng som krävs | Antal utbildningspoäng som behövs för att uppnå den tilldelade kompetensnivån. |
| Intjänade poäng | Antalet poäng som eleven har tjänat in för att slutföra den tilldelade kompetensnivån. |
| Andel slutförd | Procentandelen av nödvändiga krediter som eleven har slutfört. |
| Tilldelat datum (UTC) | Datumet då kompetensen tilldelades eleven. |
| Uppnått datum (UTC) | Det datum då eleven uppnådde de nödvändiga tillgodoräknandena och uppfyllde kompetensnivåkriterierna. |
| Chefens namn | Namn på elevens chef som övervakar utbildningsförloppet. |

### Vad innehåller sammanfattningen av kompetensen I?

| Kolumn | Beskrivning |
|---|---|
| Efter | Representerar antalet elever som uppnådde en kompetens före en angiven period (i dagar), efter vilken kompetensen anses vara föråldrad eller kräver uppdatering. Användbart för att identifiera elever med uppnådda eller utgångna kompetenser.<br>Mer information finns i <a href="https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/skills-levels"> kunskapsnivåer</a>. |
| Namn | Fullständigt namn på den elev som kompetensen är tilldelad. |
| Chefens namn | Namn på elevens rapportansvarige. |
| Radetiketter | Det specifika kunskapsnamnet som har tilldelats elever som visas på den här raden. Används som en grupperingsrubrik för att sammanfatta data om elevens kompetens under varje kompetenskategori. |
| Antal användare som ska ha denna kompetens | Totalt antal elever som har tilldelats den specifika kompetensen. |
| Antal användare som har erhållit den här kompetensen | Antal elever som har slutfört de utbildningsobjekt som krävs för att uppnå kompetensen. |
| Antal elever vars kompetens behöver fräschas upp | Antalet elever vars kompetensuppfyllelsedatum överskrider det definierade uppdateringströskeln. |
| Andel efterlevnad (baserat på uppnådd kompetens) | Efterlevnads- eller antagandegraden för kompetensen. |


### Vad innehåller kompetenssammanfattning II?

| Kolumn | Beskrivning |
|---|---|
| Efter | Antal kompetenser som uppnåtts av eleven före det definierade uppdateringströskeln (i dagar). Detta identifierar färdigheter som kan vara föråldrade och som behöver fräschas upp. |
| Kompetens | Namn på kompetensen/kompetenserna som har tilldelats elever. Det här kan kopplas till ett eller flera utbildningsobjekt, t.ex. kurser, certifieringar eller utbildningsvägar. |
| Chefens namn | Namnet på elevens direktchef. |
| Radetiketter | Elevens fullständiga namn. För varje elev visas kunskaper och framsteg i efterföljande kolumner. |
| Antal kompetenser varje användare ska ha | Totalt antal kompetenser som har tilldelats eleven. |
| Antal kompetenser varje användare har | Totalt antal kompetenser som eleven har uppnått genom att slutföra associerade utbildningsobjekt. |
| Antal kompetenser som behöver fräschas upp | Antalet uppnådda kompetenser som har överskridit uppdateringens varaktighet och nu kräver förlängning. Detta värde hjälper till att spåra utbildningsbehov för efterlevnad eller kontinuerlig utveckling. |
| Andel efterlevnad | Anger elevens övergripande efterlevnadsnivå baserat på uppnådd kompetens. |

## Historik över nedladdningar av elevbetygsutdrag

Historiken över nedladdningar av elevens betygsutdrag gör det möjligt för administratörer att spåra vem som har laddat ned varje elevs betygsutdrag och vilka användare de har öppnat. Den här funktionen är särskilt användbar i företags- och regelefterlevnadsfokuserade miljöer där flera intressenter kan behöva se utbildningsposter.

När du har hämtat ett elevintyg visar sidan Elevens betygsutdrag alla betygsutdrag som genereras av någon på plattformen.

Listan innehåller följande attribut:

* Från och Till: Längden på de utskrifter som ska hämtas.
* Genererad av: E-postadressen till den användare som har hämtat rapporten eller begärt hämtningen.
* Elever: Eleverna eller elevgrupperna vars utskrifter ska hämtas.
* Filter tillämpade: Filtren som tillämpades för registreringsstatus.
* Ytterligare data inkluderade: Ytterligare data (borttagna elever, modulinformation och kompetensdata och sammanfattningar) som administratören hade begärt från alternativet Avancerat i det modala fönstret Lägg till elevens betygsutdrag
* Status: Hämtat, köat eller pågående.
* Avbryt: Avbryt rapportgenereringen när som helst.

## Ytterligare saker att tänka på vid elevens betygsutdrag

Elevens betygsutdrag omfattar flera beteenden som administratörer bör vara medvetna om:

**Visning av utbildningsväg och kursförlopp**

Alla kurser som ingår i en utbildningsväg (LP) kommer att visas i elevens betygsutdrag, även om eleven har gjort framsteg inom endast en av kurserna. Detta garanterar fullständig synlighet för en utbildningsväg, även när förloppet är delvis slutfört.

**Data för borttagna elever**

Om en elev har tagits bort från plattformen visar deras betygsutdrag inte sina poster i rapporter som har genererats för den användargrupp de ingick i. Det innebär att poster för borttagna elever utesluts från filtrerade rapporter som skapas med hjälp av användargruppsfilter.

Men du kan fortfarande hämta data för de borttagna eleverna. Om du har valt alternativet **[!UICONTROL Include deleted learners]** när du ställer in filtren för att skapa rapporten kan du hämta rapporten för de borttagna eleverna.

**Beteende för anpassade administratörer**

Anpassade administratörer med en definierad omfattning (t.ex. begränsad till specifika kataloger eller användargrupper) ser filtrerade transkriptionsdata baserat på deras omfattning:

* Omfång för användargrupp: Endast elever i den anpassade administratörens omfång för användargruppen inkluderas i rapporten.
* Katalogomfattning: Endast utbildningsobjekt (kurser, certifieringar och utbildningsvägar) som tilldelats de kataloger som omfattas inkluderas i rapporten.
* Filtrerade kolumner: Kolumnerna förblir desamma. Endast raderna kommer att omfattas baserat på omfattningar för kataloger och användargrupper.

Detta garanterar att anpassade administratörer med ett omfång endast visar elevens data och utbildningsinnehåll som de har behörighet att hantera.

**Anslutningsstöd**

Elevens betygsrapport kan nås via administratörsgränssnittet [FTP, Box, jobb-API eller Power BI](/help/migrated/integration-admin/feature-summary/connectors.md). Det ingår inte i de samlade rapporterna från Salesforce, Power BI och Marketo Engage.

Enhetliga rapporter som hämtas från Salesforce, Marketo Engage och Power BI innehåller färre kolumner än elevens betygsutdrag.






