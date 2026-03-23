---
title: Nyheter i Adobe Learning Manager-versionen från april 2026
description: Läs om de nya funktionerna, förbättringarna och viktiga uppdateringar i Adobe Learning Manager i april 2026-versionen.
exl-id: 4d2129c4-42d8-446f-8837-879b5c2f42bf
source-git-commit: 47d49f4bbb81db88635b2c115768e15a3818e153
workflow-type: tm+mt
source-wordcount: '20175'
ht-degree: 0%

---

# Uppdateringar i Adobe Learning Manager

>[!IMPORTANT]
>
>Funktionerna i den här versionen är tillgängliga som betaversioner. Funktionaliteten och beteendet kan ändras innan produkten blir allmänt tillgänglig. Dela feedback via dina vanliga supportkanaler i Adobe.


Det här dokumentet innehåller en sammanfattning av de nya funktionerna, förbättringarna och uppdateringarna i april 2026-versionen av Adobe Learning Manager. Använd det för att planera ändringar i organisationen och förstå vad som är tillgängligt för elever, administratörer och författare.

**För elever:** Fluidic-spelaren visar nu nästa modulnamn och en knapp för att avsluta. Spelarens språk kan ställas in via LTI för en konsekvent upplevelse på olika plattformar. Captivate-innehåll innehåller en enhetlig innehållsförteckning, slutförandeskalor på bildnivå och tillförlitliga anteckningsexporter. Flerspråksstöd finns tillgängligt för arbetsstöd, checklistefrågor och videotextspår (VTT). AI-assistenten hjälper elever att få svar inom utbildningsupplevelsen.

**För administratörer och författare:** Zoom Connector stöder flera samtidiga VILT-sessioner. Delade kurser i kollegiala konton visar den verkliga författaren istället för &quot;Extern författare&quot;. Administratörer kan begränsa när moduler kan startas. Förfallodatum för utbildningsobjekt visas i elevens API:er. Checklistmoduler har stöd för viktad poäng, flerspråkig frågetext och valfria granskningskommentarer. Anpassade certifikat har en dra och släpp-redigerare med dynamiska fält och AI-genererade bakgrunder. Med den icke inloggade Experience Builder kan du skapa offentliga utbildningssidor utan att behöva logga in.

**För instruktörer:** Generera QR-koder för instansregistrering och sessionsnärvaro. Lägg till kommentarer eller feedback under utvärderingen av checklistan.

**Rapportering och analys:** SCORM-innehåll kan nu rapportera flera frågeformulärsförsök i L2-rapportering. Beräkning av använd utbildningstid har förbättrats i elevens betygsutdrag. Rapporter om utbildningstranskribering för administratörer uppdateras. Avancerade sökförbättringar är tillgängliga.

## Fluidic-spelarnavigering: visa namnet på nästa modul

### Översikt

Den här förbättringen ingick redan i november 2025-versionen av Adobe Learning Manager.

Åtgärden &quot;Nästa&quot; i spelaren indikerar vad som kommer att hända när användaren klickar på den genom att visa namnet på nästa modul eller kurs och genom att uttryckligen signalera när eleven är på väg att lämna spelaren.

### Nyheter

**&quot;Nästa modul: etiketten {ModuleName}&quot; i spelaren**

Nästa-ikonen i Fluidic-spelaren visar nu namnet på nästa modul i kursen. Till exempel Nästa modul: Lektion 2 - Komma igång.

Detta gäller där eleven förflyttar sig från en modul till nästa inom samma kurs.

**Rensa avslutningsåtgärden för den sista modulen**

När eleven finns på den sista modulen i en kurs visas en ny Avsluta-åtgärdsknapp, som indikerar att klicka på den för att stänga spelaren och återföra den till kurskontexten.

**Responsivt beteende för mobilinnehåll och PDF-innehåll**

I mindre visningsrutor (till exempel ~320 px bredd) kan Nästa etikett vara förkortad eller dold och endast visa ikonen för att undvika överlappning med PDF-kontroller.

För PDF-moduler justerar spelaren reglagen till en egen rad, så att navigeringsetiketter och PDF-reglage inte stör varandra.

**Uppdaterad administratör > Varumärkning > Förhandsgranskning av spelare**

Spelarens förhandsgranskning i Admin > Varumärke visar nu den nya etiketten, till exempel Nästa modul: Lektion 2. Detta gör att administratörer kan se det uppdaterade navigeringsbeteendet.

### Viktiga fördelar

**Tydligare navigering för elever**

Elever behöver inte längre gissa vad som händer när de väljer Nästa. Etiketten anger tydligt vad som kommer härnäst, oavsett om det är en modul eller en kurs. Denna minskning av tvetydigheten bidrar till att minska tvekan och förvirring, särskilt hos stora målgrupper inom kundutbildning där många elever kanske inte är bekanta med LMS-gränssnitt.

**Högre slutförandegrad för kurser**

Genom att tydligt ange nästa steg (nästa modul: {ModuleName}) och lägga till en distinkt avslutningsåtgärd för den slutliga modulen minskar sannolikheten för att elever överger kursen eller förbiser det sista slutförandesteget.

**En mer förutsägbar användarupplevelse på alla enheter**

De uppdaterade etiketterna justeras mot beteendet och ikonerna Nästa eller Föregående på stationära datorer, surfplattor och mobila enheter. Layoutbegränsningar respekteras på alla enheter och i PDF så att reglagen förblir användbara och åtkomliga.

Detta är särskilt viktigt för fjärradministrerade implementeringar där Fluidic-spelaren är inbäddad i en anpassad inlärningsupplevelse.

### Användningsfall

**Kundens och partnerns utbildningsportaler (fjärradministrerade eller AEM-integrerade)**

Konton som använder Adobe Learning Manager i en helt fjärradministrerad konfiguration, som dirigerar elever från externa marknadsföringskanaler. Dessa elever:

* Ofta förbrukar videoinnehåll i långa sekvenser.

* Förvänta dig en upplevelse i kursplanstil där systemet tydligt visar nästa avsnitt/modul.

I dessa miljöer kommer etiketten **Nästa modul:{ModuleName}**:

* Förstärker färdens guidade natur.

* Minimerar bortfall mellan moduler.

**Efterlevnads- och certifieringskurser med beställda moduler**

I reglerade eller efterlevnadstunga scenarier:

* Elever måste slutföra en strikt sekvens av moduler.

* Författare inaktiverar ofta innehållsförteckningen för att undvika att hoppa över.

Här visas **Nästa modul:{ModuleName}**:

* Bekräftar för elever att de följer rätt ordning.

* Gör det mindre troligt att de misstolkar Nästa åtgärd och avslutar tidigt.

**Utbildningsvägar där kurserna följer varandra**

Där utbildningsvägar eller motsvarande kedjar flera kurser. Detta är användbart när man bygger sekvenser i kursplanstil för en stor publik.

**Mobil-först-förbrukning**

För elever som främst använder mobiler eller surfplattor:

* Uppdaterade etiketter och responsivt beteende säkerställer att navigeringen är förståelig utan att du behöver förlita dig på små stängda ikoner eller dolda kontroller.

* Det är viktigt för kundutbildning, gigarbetare eller elever i frontlinjen som kan komma åt innehåll under korta sessioner på mobila enheter.

## Zoomkoppling - skapa flera samtidiga zoomsessioner

### Översikt

Uppgraderingen av Zoom Connector förbättrar hur Adobe Learning Manager hanterar VILT (Virtual Instructor-Led Training). Tidigare kunde användarna bara skapa en zoomsession i taget. Med den nya uppdateringen kan administratörer och författare schemalägga flera zoomsessioner samtidigt med hjälp av standardintegrering.

### Nyheter

#### Stöd för flera samtidiga zoomsessioner via anslutningen

* Zoom Connector tillåter nu att mer än en VILT-session skapas vid samma datum/tid från ALM.

* Schemaläggningslogiken tillämpar inte längre ett villkor om att zooma en gång i taget på konto-/anslutningsnivå.

* Administratörer och författare kan konfigurera överlappande VILT-sessioner (till exempel regionala klassrum, parallella spår eller upprepade sessioner för olika partnergrupper) utan att behöva kringgå problemet.

#### Möten skapas med instruktörens zoom-identitet (inte superadministratören för zoom)

Anslutningen har uppdaterats så att:

* Zoommöten skapas nu med instruktörens e-postadress i stället för superadministratörens e-postadress för Zoom.

* Varje instruktörs Zoom-konto kan vara värd för sina egna möten parallellt med andra instruktörer, inom gränserna för den befintliga Zoom-planen.

**Anteckning**:

* Endast en instruktör per möte stöds fortfarande.

* Om en instruktörs e-postadress uppdateras senare i Adobe Learning Manager förblir befintliga möten kopplade till det ursprungliga e-postmeddelandet som användes när det skapades.

#### Inga fler manuella inklistringar av zoom-URL för samtidiga sessioner

Tidigare, när en andra eller tredje zoomsession skulle köras samtidigt:

* Författarna var tvungna att manuellt skapa zoommöten utanför ALM och sedan klistra in webbadressen för zoomkoppling i kursinstanskonfigurationen.

* Detta var felbenäget och gynnades inte av anslutningsfunktioner som närvarospårning.

Med den uppdaterade anslutningen:

* Alla sessioner kan skapas direkt från ALM-gränssnittet med zoomkontakten, även om de överlappar varandra i tiden.

* Sessionens livscykel (skapande/annullering) hanteras fortfarande centralt via integrering.

### Viktiga fördelar

#### Bättre VILT-schemaläggning i stor skala

Organisationer kan nu:

* Kör flera zoombaserade virtuella klassrum samtidigt (t.ex. parallellspår på ett virtuellt toppmöte, regionala grupper eller separata partnerutbildningssessioner).

* Undvik flaskhalsar som tidigare tvingade administratörer att serialisera sessioner eller förlita sig på manuell zoomhantering.

#### Minskade omkostnader för administratör och författare

Förbättringen tar bort:

* Skapa zoommöten utanför Adobe Learning Manager manuellt.

* Kopiera och klistra in zoom-URL:er i varje kursinstans för överlappande sessioner.

* Risk för felkonfigurerade länkar, felaktiga möten eller utebliven närvarospårning.

Administratörer och författare kan hantera alla zoomsessioner från Adobe Learning Manager med hjälp av välbekanta arbetsflöden.

#### Bättre inriktning mot zoomallokering och instruktörsroller

Genom att knyta möten till individuella instruktörskonton Zooma:

* Varje instruktör kan arbeta inom sina egna gränser för zoomlicenser.

* Organisationer kan använda sin befintliga modell för zoomtilldelning (ett konto per utbildare, per affärsenhet osv.) samtidigt som den är fullt integrerad med Adobe Learning Manager.

* Det undviker flaskhalsen med en enda punkt vid användning av en delad zoomanvändare för superadministratörer för alla sessioner.

### Användningsfall

#### Flerspåriga virtuella evenemang och toppmöten

Kundutbildningsteam som genomför stora evenemang (t.ex. produktstartläger, partnertoppmöten eller certifieringsveckor) kan:

* Konfigurera flera zoombaserade sessioner på samma plats (för olika spår eller ämnen).

* Hantera dem alla som VILT-moduler under Adobe Learning Manager kurser och utbildningsvägar.

* Ge eleverna en enhetlig upplevelse när anslutningen hanterar allt underliggande zoommöte som skapas.

#### Global partner- och kundutbildning

Organisationer som utbildar kunder och partner i olika regioner kan:

* Kör separata zoomsessioner för EMEA, APAC och Amerika vid överlappande tider för att matcha lokal arbetstid.

* Undvik att tvinga fram en enda global tidslängd eller manuell zoominställning för ytterligare kohorter.

#### Intern aktivering

Interna aktiveringsteam (försäljning, support osv.) kan:

* Schemalägg parallella introduktionssessioner eller rollbaserade utbrytningar (till exempel separata zoomrum för utvecklare, administratörer och affärsintressenter) i ALM.

* Håll alla sessioner inom ALM:s VILT-modell för rapportering och efterlevnadssyften, i stället för att delvis gå över till ohanterade Zoom-möten.

## Visa originalförfattare för delade kurser i kollegiala konton

### Översikt

När en kurs delas via katalogen till ett kollegialt konto, ger Adobe Learning Manager författaren etiketten &quot;Extern författare&quot; i vyn Elev, Administratör och Författare för det mottagande kontot. Detta kan innebära utmaningar för elever och administratörer, särskilt i stora företag, eftersom det blir svårt att identifiera och kontakta rätt innehållsägare när problem eller frågor uppstår.

Förbättringen gör att upphovsinformation bevaras och visas för delade kurser i kollegiala konton, i stället för att ersättas av en allmän platshållare.

### Nyheter

Visa det faktiska författarnamnet för delade kurser i kollegiala konton

För kurser som delas via externa kataloger eller kollegiala kataloger visas nu det ursprungliga författarnamnet från källkontot i det mottagande kontot i stället för &quot;Extern författare&quot;.

Detta gäller

* Elevapp (kurskort eller kursinformation).

* Administratör och författare visar när de förhandsgranskar som elev.

### Viktiga fördelar

#### Direkt ägarsynlighet för delat innehåll

Elever och administratörer i kollegiala konton kan nu:

* Se vem som har skrivit kursen, även om den förvärvas via en delad katalog.

* Undvik den generiska och oanvändbara etiketten &quot;Extern författare&quot;.

#### Mer konsekvent upplevelse av flera klientorganisationer och kollegiala konton

För kunder som kör scenarier med flera klientorganisationer eller utökade företag:

* Samma kurs visas med konsekvent skaparanpassning på alla konton.

* Elevupplevelsen är i linje med förväntningarna från det primära kontot (till exempel att se källkontots författarnamn i stället för &quot;Extern författare&quot;).

### Användningsfall

#### Stora företag med kollegiala konton

Företaget använder ALM med:

* Ett huvudkonto som äger de kanoniska kurserna, och

* Kollegiala konton som hämtar innehåll via delade kataloger.

Elever i kollegiala konton behöver veta vilket team av företagsteam som har författat en kurs för att dirigera frågor eller förbättringsförslag korrekt.

Med denna förbättring:

* Delade kurser visar nu rätt namn på den som har skapat företaget i kollegiala konton.

* Företagets interna supportbelastning minskar eftersom elever och lokala administratörer vet vem de ska kontakta.

#### Intern delning av flera affärsenheter

Där en affärsenhet kurerar lärande för andra:

* Den ägande affärsenheten kan identifieras i fältet författare på alla konton som använder den.

* Lokala l&amp;D-administratörer kan snabbt se om en kurs underhålls lokalt eller av en annan affärsenhet och samarbeta i enlighet med detta.

## Exponeringsförfallodatum för utbildningsobjekt (dra tillbaka automatiskt) i elevens API:er

### Översikt

Den här förbättringen gör att datumet för automatisk pensionering av ett utbildningsobjekt (LO) blir tillgängligt direkt via Adobe Learning Manager elevinriktade API:er. När en kurs, utbildningsväg eller certifiering har konfigurerats med ett utgångsdatum eller datum för automatisk utfasning, ingår den informationen nu i LO-data som returneras av viktiga elevslutpunkter.

### Nyheter

#### Nytt utgångsfält/fält för automatisk utfasning i elevens LO API:er

* Elevens LO API:er (till exempel slutpunkterna som returnerar utbildningsobjekt till elevupplevelsen och till externa plattformar) inkluderar nu LO-utgångsdatumet (automatiskt utfasningsdatum som konfigurerats för det utbildningsobjektet).

* Det här fältet returneras som en del av LO-enheten i svar som:

   * Hämta utbildningsobjekt (LO-information).

   * LO-data som används för att fylla i elevens startsida, katalog och sökresultat.

* Fältet kompletterar den befintliga completionDeadline som redan finns på instansnivån. Det nya fältet är specifikt det automatiska återtagningsdatumet på LO-nivå.

#### Tillgänglighet i elevupplevelser med sökstöd

Eftersom utgångsdatumet visas som en del av den sökstödda LO-representationen är det nu tillgängligt överallt där ALM eller en extern plattform använder:

* sök-API:er eller

* sökdrivna kataloger och förslag för att konstruera elevvyer.

**Omfång och undantag**

Förbättringen gäller endast elevens API:er.

### Viktiga fördelar

#### Elevupplevelse som känner av att giltighetstiden går ut i anpassade LXP:er

För stora och medelstora företag kan deras anpassade LXP nu få LO-information direkt från ALM, så att de kan:

* Visa etiketterna &quot;Förfaller den {date}&quot; eller &quot;Förfaller snart&quot; på kurskort och detaljsidor.

* Kommunicera tydligare så att eleverna prioriterar utbildning som snart ska gå i pension.

Detta är särskilt viktigt för efterlevnad eller tidsbunden produktutbildning, där utbildningsobjekt uppdateras regelbundet och äldre versioner pensioneras.

#### Bättre vägledning för elever om vilka utbildningar de ska gå nu

Genom att exponera LO-förfallodatum kan elevupplevelsen:

* Markera kurser som fortfarande är giltiga jämfört med kurser som snart ska fasas ut.

* Hjälp elever att undvika att registrera sig för utbildningar som inte längre kommer att vara tillgängliga eller giltiga inom en snar framtid.

#### Överensstämmelse med befintliga tidsdata för slutförande

Tidigare har elevens API redan exponerat completion-level completionDeadline, men inte automatiskt utfasningsdatum på LO-nivå. Med den här ändringen:

Följande utbildningsaspekter finns tillgängliga:

* &quot;När måste jag vara klar med den här instansen?&quot; (tidsfrist för slutförande).

* &quot;När erbjuds denna utbildning?&quot; (datum för automatisk pensionering/förfallodatum).

### Användningsfall

#### Ett globalt företag med strikt hantering av kursernas livscykel

Företag som regelbundet går i pension och ersätter kurser (t.ex. regel-, produkt- eller metoduppdateringar) kan:

* Undvik att elever förvirras av om en utbildning fasas ut.

* Driva eleverna mot de mest aktuella, långlivade erbjudandena.

Deras anpassade portaler och interna verktyg kan nu läsa utgångsdatumet direkt från ALM via elevens API:er.

#### Externa kund- eller partnerskolor

För kund- och partnerutbildning lägger marknadsföringssidor och portaler ofta vikt vid aktuell utbildning.

Genom att ha förfallodatum i LO API kan Experience Builder:

* Dölj eller tona ned innehåll som är nära pensionering.

* Skapa &quot;Sista chansen att slutföra&quot;-kampanjer.

## Flerspråkigt stöd för arbetsstöd

### Översikt

Förbättringen utvidgar Adobe Learning Manager lokaliseringsmodell till arbetsstöd, vilket gör att författare kan bifoga olika innehållsfiler per språk till ett enda arbetsstöd. I stället för att skapa separata arbetsstöd för varje språk kan författare nu hantera alla lokaliserade versioner som ett logiskt arbetsstöd.

### Nyheter

#### Uppladdning av språkspecifikt innehåll för arbetsstöd

Författare kan bifoga olika filer per språk som stöds till ett enda arbetsstöd, som kurser och andra LO:er.

Upplevelsen att skapa/redigera arbetsstöd har nu stöd för:

* Välja ett språk.

* Överför den språkspecifika filen för det språket i samma arbetsstödsentitet.

#### Konsekvent språkhantering i spelare- och elevgränssnittet

Fluidic-spelaren har uppdaterats så att när en elev öppnar arbetsstöd visas den innehållsvariant som motsvarar elevens språk (om tillgänglig).

Administratörer och författare kan visa arbetsstöd som enskilda objekt med språkvarianter, i stället för som separata objekt per språk.

### Viktiga fördelar

#### Arbetsstöd för alla språk

Författare kan undvika att skapa separata arbetsstöd per språk.

Alla språkvarianter av samma arbetsstöd (till exempel en procedur, SOP, checklista PDF eller referensguide) kan hanteras på ett enda ställe.

#### Bättre erfarenheter för globala elever

Eleverna ser arbetsstödet automatiskt på det språk de föredrar, vilket innebär att det finns

* Mindre förvirring om vilken version som ska öppnas.

* Mindre risk för att komma åt inaktuella eller föråldrade kopior.

Detta är särskilt användbart i flerspråkiga organisationer där samma process eller produktdokumentation måste finnas tillgänglig på flera språk.

### Användningsfall

#### Global lansering av referensinnehåll

Ett företag måste tillhandahålla arbetsstöd på flera språk till elever över hela världen, t.ex.

* Referensblad för produkter.

* Bearbeta checklistor.

* Stöd för spelböcker

I stället för att skapa separata arbetsstöd som &quot;Product Quick Start - EN&quot;, &quot;Product Quick Start - DE&quot;, &quot;Product Quick Start - JP&quot; etc., kan de skapa ett arbetsstöd, bifoga lokaliserade filer för varje språk och låta ALM leverera rätt version till varje elev baserat på språkinställningar.

#### Kund- eller partnerinriktad dokumentation för flera marknader

För kund- och partnerskolor kan arbetsstöd omfatta följande:

* Produktfuskpapper

* Integreringsguider

* Stödarbetsflöden

Med flerspråkigt arbetsstöd:

* Varje partner ser den lokaliserade versionen utan att tvingas välja mellan språkspecifika poster.

* Marknadsförings- och aktiveringsteam kan hantera ett arbetsstöd per ämne på alla platser.

## Ange begränsning för modulens starttid

### Översikt

Förbättringen gör att författare och administratörer i Adobe Learning Manager kan definiera ett tidsfönster då elever tillåts starta en modul. Utanför det konfigurerade start-/slutfönstret syns modulen i kursstrukturen, men eleverna kan inte initiera den.

Denna kapacitet är viktig för användare som behöver bättre kontroll över när visst innehåll blir tillgängligt eller inte borde initieras, till exempel i tidsbestämda program, kohortbaserad utbildning eller tidskänsliga övningar.

### Nyheter

Författare kan nu på modulnivå inom en kurs konfigurera ett startdatum/tid och ett slutdatum/tid som styr när elever tillåts starta den modulen. I detta fönster fungerar modulen som vanligt; före starttiden eller efter sluttiden ser eleven modulen i kurskonturen men kan inte starta den.

Konfigurationen visas i användargränssnittet för kursredigeringen som ytterligare schemaläggningskontroller för specifika modultyper, till exempel innehåll, frågeformulär eller aktiviteter för eget tempo. Administratörer kan använda dessa kontroller för att skapa moduler som öppnas i faser eller för att förhindra sena starter i program där innehåll måste förbrukas inom en angiven tidsram.

#### Viktiga fördelar

Den största fördelen är möjligheten att styra när moduler är tillgängliga. Utbildningsteam kan synkronisera modultillgänglighet med verkliga evenemang, som lanseringar av nya produkter, deadlines och interna program. Detta säkerställer att eleverna slutför nödvändigt innehåll innan de får tillgång till senare moduler.

Till exempel kan kohort 1 endast komma åt modul 2 under vecka 2, medan modul 3 förblir låst fram till vecka 3, vilket eliminerar behovet av att manuellt dölja och visa innehåll eller skapa separata kursversioner.

Detta förbättrar elevupplevelsen: istället för att ta itu med moduler som tekniskt går att komma åt men inte bör vara det då (eller redan bör vara slutförda), ser eleverna en kursstruktur där de moduler de får starta tydligt överensstämmer med det avsedda schemat.

#### Användningsfall

* **Kohortbaserat aktiveringsprogram**: I det här programmet öppnas en ny modul varje vecka. Innehållet för Vecka 1 är tillgängligt direkt, medan Vecka 2 är synlig men kan inte startas förrän ett visst datum. Vecka 3 följer samma grindningsprocess. Elever kan se hela utbildningsvägen, men systemet styr när de faktiskt kan påbörja varje steg.

* **Tidsbunden produkt- eller kampanjutbildning**: Marknadsförings- eller produktteam kan skapa en utbildningsmodul som endast ska användas när en kampanj är aktiv eller när en viss version av en produkt fortfarande är tillgänglig. Detta startfönster ser till att eleverna inte påbörjar en modul om en avvecklad produktversion efter den angivna sluttiden.

* **Bedömnings- eller tentamensmiljöer**: Organisationer kan öppna en modul (t.ex. ett test) för ett kort, väldefinierat fönster (t.ex. &quot;du kan starta tentamen när som helst mellan 9:00 och 12:00 ett visst datum&quot;). Elever kan inte påbörja tentamen utanför det fönstret, vilket stödjer rättvis schemaläggning över tidszoner och kohorter.

## Kontrollera spelarspråk via anpassad LTI-parameter

### Översikt

Förbättringen gör att externa plattformar kan använda LTI (Learning Tools Interoperability) för att ange språket för Adobe Learning Manager-innehåll vid lanseringen. I stället för att vara beroende av att eleven byter språk i Fluidic Player kan LTI-konsumenten skicka en språkkod via en anpassad LTI-parameter. Adobe Learning Manager kommer sedan att använda denna kod för att välja lämplig språkvariant.

### Nyheter

Externa plattformar som fungerar som LTI-användare kan nu passera en anpassad språkparameter (och relaterade spelarinställningar) när ALM-innehåll startas. ALM läser parametern och:

* Anger spelarspråket därefter.

* Startar motsvarande språkvariant av modulen när innehåll på flera språk är konfigurerat.

Det innebär att en förstagångselev väljer franska på den externa plattformen och ser ALM-spelaren och modulen direkt på franska utan att behöva justera något i ALM.

Förbättringen omfattar även scenarier där den externa plattformen behandlar ALM som en fjärradministrerad innehållsspelare. Du kan t.ex. dölja navigeringselement och innehållsförteckning genom att skicka ytterligare anpassade parametrar för att justera vissa inställningar för användargränssnittet. Dessa inställningar fungerar tillsammans med parametern language, vilket gör att den externa plattformen kan ge en smidig, varumärkt upplevelse samtidigt som ALM används för uppspelning och spårning.

### Viktiga fördelar

* **Konsekvent språkupplevelse i olika system**: När en elev väljer ett språk i den externa portalen återspeglas det valet omedelbart i ALM. Detta säkerställer att eleverna inte stöter på några avvikelser mellan portalens språk och kursen. Som ett resultat av detta kommer de inte att behöva söka efter en språkinställning i spelaren.

* **Språkspecifik rapportering**: I deras plattform överensstämmer språkval med ALM, vilket förbättrar noggrannheten i deras analys och elevspårning. Denna inriktning stöder också konfigurationer där ALM:s egna språkkontroller avsiktligt är inaktiverade eller dolda i Fluidic Player för specifika kurser. I dessa fall fungerar den externa plattformen som den enda sanningskällan för språk.

### Användningsfall

* Ett betydande användningsfall innefattar stora företag som använder LTI-baserade integreringar. Elever registrerar sig först och väljer ett språk på plattformen. Sedan startar de ALM-utbildningar genom LTI. Med denna förbättring öppnas ALM-modulen automatiskt på spanska när eleven väljer spanska. Det innebär att eleverna inte behöver justera språkinställningarna i ALM. Språkbaserad rapportering överensstämmer dessutom fortfarande med vad elever ser och upplever i ALM.

* En annan tillämpning är leverans av fjärradministrerade kursupplevelser inom en kund- eller partnerportal. I den här konfigurationen kan portalen bädda in ALM-innehåll med en iFrame, medan all navigering och språkanvändning hanteras utanför ALM. Genom att använda anpassade LTI-parametrar kan portalen se till att ALM-spelaren visas på rätt språk och att alla onödiga gränssnittselement (till exempel innehållsförteckning och navigeringsknappar) är dolda. Detta gör att eleverna kan uppfatta en enda sammanhängande tillämpning snarare än en osammanhängande samling verktyg.

* Detta är fördelaktigt för organisationer som bedriver storskalig utbildning i flera språk med ett annat LMS eller en annan utbildningsplattform. De kan standardisera sin användning av den plattformen för att hantera elevprofiler, välja språk och presentera kataloger. Under tiden fungerar ALM som en pålitlig innehålls- och spårningsmotor som respekterar de språkinställningar och användarinteraktioner som anges av det externa systemet vid varje LTI-lansering.

## Checklista för frågeviktning för instruktörsutvärderingar

### Översikt

Förbättringen introducerar viktade checklistor, vilket gör det möjligt för instruktörer och chefer att utvärdera elever med hjälp av graderade skalor och totala poäng, snarare än att behandla varje checklista fråga som likvärdig. Målet är att underlätta upprättandet av checklistor genom att genomföra viktade utvärderingar av frågor, vilket gör det möjligt att återspegla den relativa betydelsen av olika åtgärder eller färdigheter inom en enda checklista.

### Nyheter

Checklistor har stöd för följande typer:

1. Ja/nej
Beteendet är detsamma som i dag: varje fråga är ja/nej och kriteriet för godkänt baseras på antalet ja-svar.

2. Frågor med samma vikt

   * Frågor får poäng på en numerisk skala (0-10 som standard), där:

      * Maximi-/minvärdena på skalan kan anpassas på checklistenivån.

      * Skalan kan nu börja på 0 (föregående minimipoäng var 1).

   * Alla frågor delar samma maximala poäng, så checklistan fungerar som en enhetlig graderad skala för varje fråga.

3. Frågor med olika vikt

   * Varje fråga har sin egen maxpoäng (vikt).

   * Kriterierna för godkänt beror på procentandelen av det totala möjliga poängtalet som eleven uppnår i checklistan (till exempel &quot;godkänt om eleven uppnår ≥ 70 % av det totala tillgängliga poängvärdet&quot;).

För alla typer av checklistor:

* **Granskaren** (instruktör eller chef) utvärderar eleven enligt den konfigurerade typen av checklista:

   * Väljer Ja/Nej.

   * Välj poäng på den definierade skalan.

* Checklisterapporten **Checklista** har uppdaterats så att den inkluderar följande för frågor med olika vikt:

   * Högsta poäng för varje fråga.

   * Poängen som uppnås av varje elev för den frågan.

Detta möjliggör analys av övergripande prestanda och frågespecifika prestanda baserat på de avsedda vikterna.

### Viktiga fördelar

* **Bättre och mer realistiska bedömningar**: Instruktörer kan återspegla verkliga prioriteringar genom att ge fler poäng till kritiska beteenden och färre till mindre sådana, samtidigt som de använder ett arbetsflöde med checklistor som passar för observerade eller praktiska uppgifter.

* **Total-score-baserat godkännande/underkännande**: Utvärderingarna kan baseras på den övergripande procentpoängen, inte bara hur många frågor som klarar ett tröskelvärde, vilket ligger närmare den typiska kompetensen eller graderingsschemat.

* **Bättre rapportering**: Uppdaterade checklisterapporter visar högsta poäng och uppnådda poäng per fråga, vilket gör att programägare och kvalitetsteam kan identifiera specifika svaga punkter och förbättra vägledning för utbildning eller utvärdering.

### Användningsfall

* **Företagets kompetensbedömningar**: Teknikerna bedöms via praktiska, scenariobaserade checklistor där vissa diagnostiska steg eller kommunikationssteg måste väga tyngre än kosmetiska steg eller lågrisksteg. Viktade frågor och total-score-kriterier gör dessa bedömningar mer trovärdiga och prediktiva för verkliga resultat.

* **Iakttagelser av säkerhet och regelefterlevnad**: Inom hälso- och sjukvård, tillverkning eller fältservice kan viktiga säkerhetssteg ges högre maxpoäng, vilket säkerställer att om en säkerhetskritisk åtgärd saknas får det större effekt på totalpoängen än om ett mindre steg i proceduren saknas.

* **Coaching och kalibrering**: Med max och uppnådda poäng per fråga i rapporten kan chefer se exakt var eleverna underpresterar och kalibrera instruktörer om hur de poängsätter konsekvent.

## Flerspråkigt stöd för checklistefrågor

### Översikt

Förbättringen introducerar flerspråkigt stöd för checklistefrågor, vilket gör det möjligt för granskare att utvärdera och poängsätta checklistor på det språk de föredrar. Den här funktionen är särskilt användbar i flerspråkiga regioner och globala distributioner, eftersom den gör det möjligt för författare att skapa lokaliserade frågor om checklistor för varje innehållsspråk som stöds samtidigt som en enda checklistmodul och en konsekvent utvärderingsprocess upprätthålls.

I Adobe Learning Manager idag:

* Alla moduler som riktar sig till elever (SCORM, PDF, HTML osv.) kan erbjudas på flera innehållsspråk så att eleverna kan välja vilket språk de vill använda.

* I en checklistmodul utvärderar granskare (instruktörer/chefer) elever baserat på de frågor som definierats i checklistan.

### Nyheter

**Redigering**

* Författare kan nu lägga till checklistefrågor på alla språk som valts på kursnivån.

* För varje checklista:

   * Författaren förväntas tillhandahålla motsvarande frågetext på varje innehållsspråk där kursen finns.

   * Frågeställaren ansvarar för att frågorna har en enhetlig innebörd på alla språk.

**Granska upplevelsen**

* Granskarna ser checklistefrågor och utvärderingsgränssnittet på sitt valda innehållsspråk.

* När en fråga utvärderas på ett språk:

   * Utvärderingen (poäng, ja/nej, status) är logiskt sett densamma för alla språk. Det är en enda checklista med flerspråkiga vyer, inte separata checklistor per språk.

**Rapportering**

Checklisterapporten visar frågetexten på användarens innehållsspråk:

* En administratör eller granskare som kör rapporten på varje språk ser de lokaliserade frågenamnen för det språket.

* De bakomliggande svaren och poängen förblir desamma; endast frågeetiketter översätts.

### Viktiga fördelar

* **Bättre granskarupplevelse**: Granskarna kan arbeta helt på sitt eget språk, läsa frågor och spela in utvärderingar utan språkbarriärer.

* **Anpassning av regler och policy**: I regioner med krav på språklig jämlikhet (till exempel nederländska/franska i Belgien) kan checklistor nu uppfylla samma standarder som andra utbildningsmaterial, vilket minskar risken för efterlevnad.

* **Konsekvent utvärderingslogik**: Även om texten är lokaliserad delas utvärdering och poäng mellan alla språk, vilket säkerställer att resultaten är jämförbara och centralt hanterade.

### Användningsfall

* Franchise för flera länder som arbetar på flera språk kan distribuera en enda kurs och checklista samtidigt som du kan erbjuda lokala granskningsupplevelser i varje område.

* Alla globala företag med lokala instruktörer (t.ex. EMEA, LATAM eller APAC) kan låta granskarna arbeta på sitt lokala språk samtidigt som de delar samma globala checklistedesign och rapportering.

## Checklista med kommentarsfunktion för granskare

### Översikt

Förbättringen introducerar en kommentarsfunktion för checklisteutvärderingar, som gör det möjligt för granskare, t.ex. instruktörer och chefer, att ge kvalitativ feedback tillsammans med de numeriska poängen. Denna feedback kan göras synlig för elever vid behov.

Målet är att stödja checklistebaserade utvärderingar där mentorfeedback är lika avgörande som det numeriska resultatet. Detta inkluderar att framhäva specifika styrkor, områden för förbättring eller ge sammanhang för den givna poängen.

I dag kan granskare:

* Utvärdera en checklista för varje elev, fråga för fråga.

* Visa resultat och utvärdera elever som har misslyckats på nytt.

I verkliga scenarier, t.ex. inom flyget, bedömer fältutbildare agenter och flygplatspersonal. På samma sätt använder instruktörer och mentorer i små och medelstora företag ofta checklistor för att utvärdera arbetsresultaten. Dessa checklistor innehåller vanligtvis inte ett strukturerat avsnitt för att samla in berättande feedback som rör utvärderingen.

### Nyheter

#### Redigeringsalternativ

Författare kan konfigurera varje checklista till:

* Aktivera eller inaktivera kommentarsfunktioner för granskare.

* Bestäm om granskarens namn ska visas för elever tillsammans med kommentarer.

Det gör att organisationer kan anpassa kommentarers synlighet efter sina kultur- och integritetskrav.

#### Granskningsupplevelse

När kommentarer är aktiverade:

* Granskare (instruktörer/chefer) kan lägga till valfria kommentarer när de utvärderar en checklista.

* De kan välja om kommentarer är synliga för elever, baserat på inställningarna i checklistan.

Om en elev utvärderas på nytt kan hen uppdatera eller ändra kommentarer för att återspegla den senaste bedömningen.

#### Rapportering och anmälningar

* Checklisterapporten får en ny kolumn för granskarens kommentarer som innehåller kommentaren som tillhandahölls under utvärderingen.

* Eleverna får meddelanden (på plattformen och via e-post) när en checklista utvärderas. Dessa meddelanden inkluderar:

   * Kommentaren och

   * Granskarens namn, om de har konfigurerats för att vara synliga.

Detta garanterar att feedback inte bara lagras utan även aktivt visas för elever.

### Viktiga fördelar

* **Bättre, coachliknande feedback**: Numeriska poäng kompletteras med sammanhangsberoende kommentarer, vilket gör checklistor till ett mer effektivt verktyg för coachning, inte bara efterlevnad.

* **Spårbarhet och granskningsbarhet**: Organisationer får en permanent redovisning av vem som utvärderade vem, när och vad de sa, vilket är viktigt i reglerade miljöer och viktiga roller.

* **Bättre engagemang bland elever**: Eleverna får tydlig vägledning kopplad till specifika utvärderingar, vilket förbättrar deras förståelse för förväntningar och efterföljande steg.

### Användningsfall

* Organisationer med reglerade miljöer kan använda kommentarer för att dokumentera klinisk bedömning eller feedback för personal som observeras på fältet.

* Luftfarts- och marktjänstorganisationer kan bifoga detaljerade anteckningar om driftsprestanda, säkerhetsrutiner och kundinriktat beteende, vilket gör en checklista till ett strukturerat debrief-verktyg.

* I mentorskap och utvärdering av små och medelstora företag kan instruktörer fånga nyanserade observationer som inte skulle passa in i en poäng ensam, till exempel &quot;hanteras eskalering bra men behöver förbättra tidshantering&quot; eller &quot;utmärkt felsökningsflöde; missade ett dokumentationssteg.&quot;

## Flera försök och frågeformulärsrapportering på innehållsnivå

### Översikt

>[!IMPORTANT]
>
>Observera att funktionen bara är tillgänglig efter att den har aktiverats på kontot. Kontakta ALM-supporten.


För närvarande stöder ALM flera försök på LMS-nivå via funktionen Multiple Quiz Attempt (MQA):

* Författare kan konfigurera försök på kursnivå (tillämpas på alla quiz-bärande moduler i kursen) eller på modulnivå (per quiz-modul).

* Försök kan vara:

   * Ett visst tal (till exempel 3 försök) eller

   * Oändligt antal försök, styrt på LMS-nivå.

* När en elev förbrukar en modul genom Fluidic-spelaren och sedan stänger spelaren eller slutför modulen, behandlas den sessionen som ett enda LMS-försök.

* Varje LMS-försök registreras i L2-frågeformulärsrapporten som en ny rad.

Men om själva innehållsfilen (till exempel ett artikulera SCORM-frågeformulär) implementerar sin egen flerförsökslogik, särskiljer eller spårar ALM:s L2-frågeformulärsrapport inte dessa interna försök korrekt.

Den här förbättringen introducerar spårning på innehållsnivå för flera försök till frågeformulär, vilket gör att Adobe Learning Manager kan fånga upp varje försök i själva innehållet i L2-quizrapporten. Det är utformat för situationer där verktyget för innehållsredigering (till exempel artikulera SCORM) hanterar frågeformulärsförsök oberoende av varandra. Med den här funktionen återspeglas försök korrekt i ALM-rapporter utan att vara beroende av MQA-inställningar (Multiple Quiz Attempt) på LMS-nivå.

### Nyheter

#### Författarflagga för försök på innehållsnivå

* När du överför innehåll till innehållsbiblioteket kan författare nu ange att flera försök är inbäddade i en viss innehållsfil.

* Det här är en inställning per innehåll som talar om för ALM att behandla försök som definieras i innehållet som sanningskällan.

#### Kurs-/modulbeteende

När sådant innehåll används i en kurs

* Modulen hämtar sina försök från innehållet, inte från LMS MQA.

* Elever kan bara se ett försök på LMS-nivå:

   * Kursöversikten och modulvyn visar inte en LMS-knapp för &quot;försök igen&quot; för den modulen.

   * Försökshantering (till exempel försök i frågeformuläret) styrs av själva innehållet.

#### Rapportering

I L2-frågeformulärsrapporten behandlas varje försök på innehållsnivå som en separat försöksrad:

* Varje internt quiz-försök som konfigurerats i innehållet visas som en egen rad i L2-quiz-rapporten, ungefär som hur försök på LMS-nivå representeras i dag.

* Formatet för varje rad förblir detsamma som befintliga flerförsöksrader i L2-rapportering (samma kolumner, struktur och semantik).

* Detta ger en konsekvent rapporteringsupplevelse:

   * Oavsett om försöken styrs av LMS MQA eller av innehållet visar L2-frågeformulärsrapporten en rad per försök.

#### Viktiga fördelar

* Exakt försökshistorik för SCORM-frågeformulär där försök styrs internt av verktyg som articulate, utan att tvinga MQA-konfigurationen på LMS-nivå överst.

* Renare elevupplevelse: För innehållskontrollerade försök ser eleverna en enda plats på LMS-nivå och behöver inte interagera med kontroller för LMS-återförsök. Alla återförsök hanteras inom det frågesportgränssnitt som de redan känner till.

* Flexibel arkitektur: Användarna kan välja om ALM MQA eller försök på innehållsnivå ska styra beteendet per modul, beroende på hur deras innehåll har skapats och hur de föredrar att hantera försök.

* Konsekvent rapporteringsmodell: Nedströmsanvändare av L2-frågeformulärsrapporten kan behandla varje rad som &quot;ett försök&quot;, oavsett var försökslogiken kommer ifrån.

#### Användningsfall

* Organisationer som använder articulate SCORM kan behålla sin självständiga frågelogik i SCORM-paketet samtidigt som de får korrekta rapporter på försöksnivå i ALM utan extra LMS-konfiguration.

* Organisationer som använder SCORM-innehåll som leverantören tillhandahåller kan undvika behovet av att ändra eller implementera ytterligare försök och försöka igen med MQA på LMS-nivå.

## QR-koder för instruktör för instansregistrering och sessionsnärvaro

### Översikt

Den här förbättringen ger instruktörer möjlighet att själva generera QR-koder för:

* Registrering av kursinstans,

* Sessionens närvaro, eller

* Registrering + närvaro tillsammans

på sessionsnivå. Det är utformat för situationer där elever går in i ett fysiskt klassrum eller ett hybridklassrum och kräver ett snabbt självbetjäningsalternativ för att registrera och registrera sin närvaro med en QR-kod.

### Nyheter

#### Instruktörsgenererade QR-koder

* Instruktörer kan generera QR-koder på sessionsnivå för:

   * Registrera dig i instans: Elever söker för att registrera sig till instansen som innehåller den aktuella sessionen.

   * Markera sessionsnärvaro: Elever söker under/efter sessionen för att registrera närvaro för den specifika sessionen.

   * Registrera dig i instans + markera närvaro i session : En kombinerad QR för inklistringar som ännu inte har registrerats och behöver sin närvaro markerad i ett steg.

* Instruktörer kan exportera de QR-koder de behöver baserat på scenariot (registrering, närvaro eller båda).

#### QR-kodpaketering

Den exporterade QR-kodens PDF innehåller:

* Kursnamn

* Instansnamn

* Sessionsnamn

Dessa gör det enkelt för instruktörer och samordnare att identifiera och skriva ut rätt QR-kod för varje session.

### Viktiga fördelar

* **Instruktörsautonomi**: Instruktörer behöver inte längre vänta på att administratörer ska skapa QR-koder. De kan generera dem direkt för varje session, förbättra smidigheten och minska de allmänna kostnaderna för samordningen.

* **Bättre klassrumslogistik**: Instruktörer kan hantera registrering och närvaro på plats med hjälp av QR-koder om de är på promenad eller på plats (t.ex. fältarbetare, personal på verkstadsgolvet eller externa deltagare).

* **Minskad administrativ arbetsbelastning**: Administratörsteam kan fokusera på konfiguration och styrning i stället för att hantera rutinmässiga begäranden om generering av QR-kod för varje session.

### Användningsfall

* Organisationer som kör stora volymer sessioner på plats (till exempel produktutbildning för proffs) kan göra det möjligt för instruktörer att skriva ut sessionsspecifika QR-koder som registrerar och markerar närvaro med en skanning.

* Inom detaljhandels-, tillverknings- och hälsovårdsutbildning, där elever ofta deltar i sessioner direkt från golvet eller utan förregistrering, kan en QR-kod (&quot;Enroll + Attendance&quot;) läggas vid dörren. Detta gör det möjligt för elever att själva betjäna sin registrering och närvaro via sina telefoner.

* Utbildningshändelser för partners eller kunder gör att utbildaren på plats enkelt kan anpassa sig till förändringar i rummet, ytterligare sessioner eller extra deltagare utan att behöva rådfråga administratören om nya QR-koder.

## Förbättringar av Captivate och ALM-spelare

### Översikt

Den här förbättringen förbättrar upplevelsen av att spela upp Adobe Captivate-innehåll i Adobe Learning Manager-spelaren (ALM), särskilt efter de senaste förändringarna i Captivate arkitektur. Syftet är att göra det möjligt för elever att interagera med Captivate-moduler i ALM och samtidigt säkerställa att navigering, slutförandespårning och anteckning är tydliga, konsekventa och tillförlitliga.

### Nyheter

#### Enhetlig upplevelse av innehållsförteckningen

* Bara ALM-innehållet visas på spelarens vänstra sida.

* Captivate egen TOC är dold när modulen spelas i ALM.

* Detta eliminerar dubbletter, säkerställer en enda sanningskälla för navigering och frigör skärmytor.

#### Feedback om visuellt slutförande

* Innehållsförteckningen för ALM visar gröna skalmarkeringar (eller motsvarande visuella ledtrådar) som indikerar slutförande på bildrenivå.

* I takt med att eleverna går vidare genom diabilderna i Captivate visar ALM-TOC vilka diabilder som har slutförts, i linje med elevens förväntningar på moderna kursspelare.

#### Sammanhangsberoende förloppskontroller

* Spelarkontrollerna anpassar sig efter bildtyp:

   * För videobildrutor:

      * Visa en tidsförloppsindikator som återspeglar videouppspelningen.

* För icke-videobilder:

   * Visa reglage för bildnavigering (nästa/föregående bild osv.) i stället för en icke-fungerande tidsstapel.

      * På så sätt undviker du att visa irrelevanta eller icke-fungerande kontroller på vissa bildtyper.

#### Förenklad navigering

* Det separata modulnavigeringsfältet (ALM) och kursnavigeringsfältet har slagits samman till ett enda intuitivt fält.

* Den här enhetliga navigeringen:

   * Skiljer sig tydligt från att gå genom modulen Captivate jämfört med att gå tillbaka till kurs-/modulnivå.

   * Minskar förvirring orsakad av flera staplar med överlappande syften.

#### Länkning av tillförlitliga anteckningar

* Anteckningar är länkade till bildnummer snarare än tidsstämplar.

* Den här ändringen:

   * Korrigerar exportfel som orsakas av saknade eller felaktiga tidsstämplar.

   * Gör att anteckningar kan exporteras på ett enhetligt sätt som PDF, med en tillförlitlig mappning mellan anteckningar och det bildsammanhang som de tillhör.

### Viktiga fördelar

* Renare upplevelse för en spelare: Eleverna interagerar med en TOC och en navigeringsmodell vilket minskar förvirringen och den kognitiva belastningen.

* Exakta angivelser av slutförande och förlopp: Skjutmarkeringar och sammanhangsberoende kontroller hjälper elever att förstå var de är och vad som finns kvar.

* Tillförlitligare anteckning och export: Genom att koppla anteckningar till bilder i stället för sköra tidsstämplar återfår användarna ett tillförlitligt arbetsflöde från anteckningar till PDF, även med bildbaserat Captivate-innehåll.

* Bevarat arbetsflöde för författare: Författarna behåller enkelheten i Captivate direktpublicering till ALM, medan eleverna får en modern, integrerad uppspelningsupplevelse utan extra redigeringsbördor.

### Användningsfall

* Aktiveringsprogram som använder Captivate för interaktiva simuleringar kan distribuera innehåll i ALM, vilket säkerställer att navigering, spårning av slutföranden och anteckningar fungerar konsekvent för elever.

* Organisationer som använder Captivate som sitt huvudsakliga verktyg för innehållsredigering kan upprätthålla publicering med ett klick och undvika att blanda ihop dubbla innehållsförteckningar och icke-funktionskontroller för elever.

* Organisationer som använder anteckningar som exporterats från Captivate-innehåll i ALM (för coaching, compliance eller record) kan komma åt följande:

   * Anteckningar länkar korrekt till bilder.

   * PDF genereras som förväntat.

## Förbättrad beräkning av inlärningstid i elevbetygsutdrag

### Översikt

Adobe Learning Manager har reviderat hur man beräknar inlärningstiden i Elevens betygsutdrag med versionen från april 2026. Tidigare kunde rapporteringslogiken leda till felaktiga tider om eleverna lämnade spelaren öppen utan att engagera sig i innehållet, vilket orsakade diskrepanser. Den nya metoden spårar nu aktiv tid baserat på användarengagemang, särskilt när fliken är i fokus och när det sker användaraktivitet. Den här ändringen resulterar i mer exakta data.

Uppdateringen förbättrar rapporter och instrumentpaneler och hjälper administratörer att säkerställa efterlevnad och spåra elevframsteg. Efter utgåvan kan du granska elevens betygsutdrag för att se dessa förbättringar.

Den uppdaterade beräkningsmetoden fokuserar på verkligt engagemang, t.ex. aktivt flikfokus och nyligen genomförda användarinteraktioner, vilket förbättrar noggrannheten i tidsrapporteringen inom följande områden:

* Elevens betygsutdrag (UI)
* Mått för administratörstavla
* Rapporter om kursregistrering
* API:er och anslutningar

### Vad har ändrats

Kolumnen **Använd utbildningstid** i elevens betygsutdrag använder nu förbättrad logik för att beräkna tiden mer exakt. I stället för att bara spåra spelarens öppnings-/stängningstider skiljer systemet nu mellan aktiva och inaktiva perioder baserat på användarens engagemang.

* **Aktiv tid**: Tid då eleven är aktivt engagerad (till exempel på rätt flik utför åtgärder som att bläddra eller titta på video).
* **Inaktiv tid**: Tid när eleven inte är engagerad (till exempel byter flik, ingen aktivitet på mer än 10 minuter), vilket undantas från summan.

Detta gäller de flesta modultyper, med undantag för SCORM-, Captivate- och XAPI-moduler, som behåller den ursprungliga logiken.

### Så här fungerar det

Den nya beräkningen varierar beroende på modultyp:

* **Video- och ljudmoduler**: Aktiv när innehållet spelas upp, även om eleven växlar till en annan flik. Flikfokus krävs inte för att spåra uppspelningstid.
* **Statiska moduler (PDF, PPT, Excel och liknande)**: Aktiv om du är på fliken och utför aktiviteter (musrörelse, bläddring, klickning, tangentbordsinmatning) under de senaste 10 minuterna. Om det inte finns någon aktivitet på 10 minuter växlas den till inaktiv.
* **SCORM och Captivate** behåller den ursprungliga öppna/stäng-logiken.
* **xAPI** använder nu tabbbaserad aktiv tidsidentifiering, där tiden endast räknas när fliken är aktiv. Observera att AICC-innehåll **inte stöds**.
* **HTML, LTI och annat innehåll**: Kan variera. Kontrollera elevens betygsutdrag för noggrannhet.

Inaktiv tid subtraheras, vilket säkerställer att endast verklig engagemangstid rapporteras.

>[!NOTE]
>
>Om din bärbara dator försätts i viloläge kan det hända att inlärningstiden inte spåras korrekt. Detta beror på att aktivitetsspårning pausas medan systemet är i viloläge och endast återupptas när den bärbara datorn vaknar.


### Sammanfattningstabell

| **Modultyp** | **Aktiv tid (räknad)** | **Inaktiv tid (utesluten)** |
| --- | --- | --- |
| **Video/ljud** | Uppspelningstid | Inte påbörjad; avslutad; pausad **\>10 min** |
| **Statisk (PDF/PPT/DOC)** | Fliken aktiv **och** aktivitet under de senaste **10 minuterna** | Ingen aktivitet **\>10 min**; fliken är inaktiv |
| **SCORM** | Tid rapporterad efter innehållskörning | Det går inte att identifiera inaktivitet |
| **Captivate** | Bildbaserad tidsinställning | Det går inte att identifiera inaktivitet |
| **xAPI** | Fliken är aktiv | Inaktiv flik |
| **HTML** | Spelarens öppningstid med en flik aktiv | Inaktiv flik |
| **LTI Producer/Consumer** | Om LTI-innehåll spelas upp i ALM:s spelare (dvs. ALM förbrukar LTI-innehåll som finns på ett annat LMS som fungerar som producent) gäller denna tidsödande logik.<br><br>Om innehållet spelas upp utanför LMS:en (dvs. innehållet finns i ALM, då är ALM producent, men uppspelningen sker i en extern spelare), så gäller inte denna del av tidsberäkningslogiken gälla.  <br>**Obs!**: LTI Consumer stöds inte i Adobe Learning Manager. | Inaktiv flik |

**Anteckning**:

* **Återbesök och parallella sessioner**: Räkna som aktiva när ovanstående villkor uppfylls.
* **Alla enheter, webbläsare, språk**: Ingår. Offline mobilanvändning läggs till efter synkronisering.

### Fördelar med den nya beräkningen

* **Korrekt rapportering**: Eliminerar uppblåsta tider från obevakade spelare, vilket ger realistiska inlärningstider.
* **Bättre efterlevnad**: Stödjer korrekt spårning för obligatorisk utbildning (till exempel ett företags krav på 5 timmars månadsvis).
* **Förbättrade instrumentpaneler**: Diagram över användaraktivitet och tidsödande rapporter återspeglar nu faktiskt engagemang.
* **Elevinsikter**: Hjälper administratörer att identifiera verkliga framsteg och ta itu med oengagerade elever.

### Rapporterings- och analyseffekt

* **Elevens betygsutdrag:** &quot;Använd utbildningstid&quot; återspeglar nu **verkligt engagemang**.
* **Administratörsinstrumentpanelen:** Mätvärden som inkluderar tid (till exempel plattor med &quot;tillbringad tid&quot; och trender) visar **lägre men mer realistiska** värden i scenarier där inaktiv tid tidigare blåste upp resultat.
* **Kursregistreringsrapporter:** Tidsrelaterade fält använder **ny beräkning** efter start.
* **Jämförbarhetsanteckning:** Eftersom historiska data inte beräknas om kan tidsserieanalyser som sträcker sig över utgivningsdatumet visa en **stegvis ändring**. Överväg kommentarer eller segmentering efter datum i analysverktygen.

### API och anslutningar

* **Inga schemaändringar** för befintliga slutpunkter/fält som rapporterar använd tid.
* **Fältsemantiken** uppdateras för att återspegla _beräkning av aktiv tid_ för sessionerna **efter** att funktionen har startats.
* **Anslutningar och exporter** som förbrukar tidsödande fält får automatiskt de uppdaterade värdena framöver.

### Bakåtkompatibilitet och datamigrering

* **Historiska sessioner:** Beräknas inte om.
* **Nya sessioner:** Använd **nya** aktiv tid-beräkningen.
* **Blandade perioder:** För revisioner eller longitudinell rapportering, segmentera efter **före/efter lansering** för att undvika feltolkning.

### Kända begränsningar

* **Interaktivt innehåll** (SCORM/Captivate) förlitar sig fortfarande på tidsinställning från innehållsleverantören. Identifiering i viloläge i innehållet är inte tillgängligt.
* **Iframe-baserat innehåll** (HTML/xAPI) begränsar identifiering av finkorniga interaktioner. Tabbfokus används istället.

### Vanliga frågor

**Ändrar den här uppdateringen historikposter?**

Nej. Ändringen gäller endast sessioner efter att funktionen har startats.

**Hur verifierar jag ändringarna?**

Kontrollera elevens betygsutdrag för de senaste modulerna och jämför tiden med förväntade tider.

**Påverkar detta alla konton?**

Ja, det är en global uppdatering för alla Adobe Learning Manager-konton.

**Behöver elever vidta åtgärder?**

Nej. Ändringen är automatisk och transparent för elever.

**Vad händer om elever lämnar innehållet öppet?**

Inaktiv tid är nu utesluten, vilket förhindrar överrapportering.

**Pausas video-/ljudsessioner automatiskt när fliken är inaktiv?**

Nej. Uppspelningsbeteendet ändras inte. Tiden räknas inte när den pausas > 10 minuter eller inte spelas upp aktivt.

**Visas aktivitet offline för mobila enheter?**

Ja. Offlineanvändning ingår när enheten synkroniseras.

**Vad ska jag göra om mina instrumentpaneler nu visar lägre genomsnitt?**

Detta är förväntat där inaktiv tid hade tidigare uppblåsta resultat. Anteckna instrumentpaneler och justera mål efter behov.

**Finns det några förutsättningar?**

Ingen, ändringen sker automatiskt.

## Uppdatering av rapporter om utbildningsbevis för administratörer

Vi uppdaterar LT-rapporterna (Learning Transcript) för administratörer för att bättre stödja checklistebaserade utvärderingar och granskarfeedback.

## Vad förändras?

### &#x200B;1. Kolumnnamnändring i Admin Learning-betygsutdrag

Den befintliga kolumnen **Skicka kommentar** i Admin Learning
Betygsutdrag:

1. **Namnet har ändrats till:** `Reviewer's remarks`

### Data som visas i den här kolumnen:

* **För inlämningsmoduler:**
Kolumnen fortsätter att visa inskickningskommentaren (ingen beteendeförändring).

* **För checklistmoduler:**
Kolumnen visar nu utvärderingskommentaren (granskarens kommentarer).

Den här ändringen gäller alla Admin LT-källor:

* LT har hämtats från administratörsgränssnittet
* LT som erhållits via jobb-API
* LT genererad via kopplingar

Efter denna ändring innehåller samma kolumn: - Skicka kommentarer för inlämningsmoduler

* Utvärderingskommentarer för checklistemoduler

Under det nya rubriknamnet **Granskarens kommentarer**.

### &#x200B;2. Ny kolumn i anslutningsbaserad export av utbildningstranskriberingar

För anslutningsexporterade utbildningsutskrifter:

* En ny kolumn med namnet **Granskarens kommentarer** läggs till i slutet av rapporten.
* Den här kolumnen innehåller granskarens kommentarer, justerade till det beteende som beskrivs ovan:
   * Synpunkter på inlämningen av moduler
   * Utvärderingskommentarer för checklistemoduler

## Inverkan på befintliga integreringar och automatiseringar

Läs igenom följande scenarier om du använder rapporter om utbildningstranskribering i anpassade integreringar, automatiseringar eller externa rapporteringsverktyg:

| Scenario | Påverkan | Åtgärd som krävs |
|----------|--------|----------------|
| Du identifierar fält i Admin LT efter kolumnnamn (till exempel &quot;Skicka kommentar&quot;) | Kolumnrubriken ändras till Granskarens kommentarer. | Ja. Uppdatera eventuella mappningar eller logik som refererar till kommentaren för inlämning för att använda granskarens kommentarer. |
| Du identifierar fält i Admin LT endast efter kolumnposition (indexbaserat) | Placeringen av den här kolumnen förblir densamma i Admin LT. | Vanligtvis ingen åtgärd. Om din logik inte är beroende av rubriktexten behövs ingen ändring för Admin LT. Ändra bara kolumnnamnet om kolumnen &quot;Skicka kommentarer&quot; används nu. |
| Du använder LT som exporterats av anslutningen och förlitar dig på ett fast kolumnantal eller en specifik position för sista kolumnen | En ny kolumn läggs till i slutet av rapporten. | Ja. Justera parsnings- eller valideringslogiken för att ta hänsyn till en extra kolumn i slutet av filen. |
| Du använder LT som exporterats av anslutningen och mappar efter kolumnnamn | En ny kolumn Granskarens kommentarer är tillgängliga. | Valfritt. Ingen ändring krävs om du inte vill använda den nya kommentarsinformationen för granskare/checklista. |

**Vad du bör göra**

* Granska alla skript, ETL-jobb, instrumentpaneler eller integreringar som förbrukar rapporter från Admin Learning-betygsutdrag.
* Om du refererar till det gamla kolumnnamnet _Skicka kommentar_, uppdaterar du konfigurationen eller koden för att använda det nya kolumnnamnet Granskarens kommentarer.
* Om du använder anslutningsbaserade LT-exporter och antar ett fast antal kolumner eller en fast sista kolumn, uppdaterar du logiken så att en ytterligare kolumn hanteras i slutet av exporten.

Om din nuvarande implementering enbart bygger på kolumnpositioner i Admin LT och inte valideras eller är beroende av kolumnrubriktexten behövs ingen ändring för själva Admin LT. Det är bara anslutningsexporter som behöver uppmärksammas när du är beroende av en fast layout.


## Upplevelser som inte är inloggade i Experience Builder

Med den icke-inloggade upplevelsen i Experience Builder kan organisationer visa sitt utbildningsinnehåll och sina portalsidor för alla besökare, inklusive dem som inte har loggat in. Den här funktionen är utformad för att locka, informera och engagera blivande elever genom att erbjuda en smidig och varumärkt förhandsvisning av dina utbildningserbjudanden innan de måste logga in eller registrera sig.

Med den här funktionen kan du skapa och anpassa offentliga sidor med samma användarvänliga dra och släpp-gränssnitt som i Experience Builder. Du kan visa upp kurskataloger, kategorier, banor och avancerat statiskt innehåll, inklusive bilder, text, HTML och inbäddade iframes, för alla som besöker din portal. Det gör det enkelt att lyfta fram utbildningsprogram, främja nya kurser och ge viktig information till en bredare publik.

Besökare kan bläddra i katalogen, visa information om kurser och instanser och använda den globala sökningen för att utforska tillgängliga utbildningsmöjligheter. Åtgärder som kräver en användares identitet, till exempel att registrera sig för en kurs, komma åt anpassade funktioner (som kalender, efterlevnad, resultattavla eller social utbildning) eller att konsumera utbildning, kommer dock att uppmana besökaren att logga in. Detta tillvägagångssätt säkerställer att känslig och personlig information förblir säker samtidigt som det möjliggör en omfattande förhandsgranskning.

Administratörer har möjlighet att konfigurera vilka sidor och widgetar som är synliga för användare som inte är inloggade, vilket säkerställer att endast lämpligt innehåll visas. Sidorna kan ställas in så att de är tillgängliga för både inloggade och icke-inloggade användare, eller endast för en av dessa grupper. I Experience Builder finns ett förhandsgranskningsläge som du kan använda till att visa exakt hur sidorna kommer att visas för besökarna innan de publiceras.

ALM-integreringsadministratören måste aktivera Training Data Access Connector för att aktivera funktionen. Anslutningen ser till att kursmetadata är offentligt tillgängliga.

Varumärkning och lokalisering stöds fullt ut, vilket gör att du kan anpassa sidtitlar, favoritikoner och språkinställningar efter organisationens identitet och tillgodose målgruppens behov. Som en del av övergången till den förbättrade upplevelsen kommer den äldre startsidan för icke-inloggade användare att tas bort. Därför bör allt nytt offentligt innehåll skapas med Experience Builder.

### Funktionens syfte

Med den icke-inloggade upplevelsen i Experience Builder kan organisationer visa upp sitt utbildningsinnehåll och sina portalsidor för vem som helst utan att användarna behöver logga in. Detta hjälper till att locka, informera och engagera potentiella elever genom att tillhandahålla en förhandsvisning av tillgänglig utbildning och resurser innan registrering eller autentisering behövs.

### Verkliga användningsfall vid icke-inloggad användning

* **Marknadsföring och utåtriktad verksamhet**: Organisationer kan marknadsföra sina utbildningsprogram till externa målgrupper, t.ex. potentiella kunder, partner eller arbetssökande, genom att göra kurskataloger och programinformation offentligt tillgängliga.
* **Undersökning före registrering**: Elever kan bläddra bland tillgängliga kurser, visa översikter och utforska kategorier innan de bestämmer sig för att registrera sig eller logga in, vilket hjälper dem att fatta informerade beslut om registrering.
* **Företagsutbildningsportaler**: Företag kan tillhandahålla en offentlig portal för efterlevnad eller introduktionsinformation, så att nya anställda eller leverantörer kan se vilken utbildning som finns tillgänglig innan de får inloggningsuppgifter.
* **Landningssidor för evenemang eller kampanjer**: Organisationer som kör utbildningskampanjer eller evenemang kan skapa särskilda offentliga sidor för att framhäva utvalda kurser, scheman eller resurser, vilket ökar synligheten och engagemanget.
* **Enheter för sökmotoroptimering och upptäckbarhet**: Genom att göra utvalda sidor och kataloger offentliga förbättrar organisationer sin sökmotorsynlighet och hjälper människor att upptäcka sina utbildningsalternativ online.

### Viktiga begrepp för icke-inloggad upplevelse

Med Experience Builders icke-inloggade upplevelse kan du offentligt visa upp utbildningsinnehåll och portalsidor, så att besökare kan bläddra utan att logga in.

* **Skapa offentliga sidor och menyer**: Du skapar sidor och en enda meny som alla har åtkomst till, oavsett inloggningsstatus.
* **Lägg bara till widgetar som stöds**: Du inkluderar widgetar som inte behöver användarkontext (kategorier, kurser och utbildningsvägar, innehållsruta, HTML, iframe), medan systemet döljer användarspecifika widgetar.
* **Konfigurera adaptivt sidbeteende**: Du avgör om en sida visas för både inloggade och icke inloggade användare och systemet anpassar synliga widgetar och innehåll baserat på inloggningsläget.
* **Förhandsgranska båda upplevelserna**: Du använder förhandsgranskningsalternativen för att se hur sidorna ser ut för inloggade och icke inloggade användare, med skillnader i widgetens synlighet och innehåll.
* **Aktivera global sökning**: Besökare söker efter kurser och innehåll, men får bara grundläggande sökfunktioner utan avancerad AI-integrering.
* **Låt besökare bläddra bland katalog- och kursöversikter**: Besökare utforskar katalogsidor, kursdetaljer och instanser, men måste logga in för att registrera sig eller få tillgång till personliga funktioner.
* **Anpassa varumärkning och lokalisering**: Du anger favoritikoner och språkinställningar som matchar organisationens varumärkes- och tillgänglighetsbehov.
* **Aktivera anslutningen för utbildningsdataåtkomst**: Du aktiverar den här anslutningen för att exportera kursmetadata för offentlig visning, vilket håller icke-inloggade sidor uppdaterade.
* **Hantera hög trafik med delad infrastruktur**: Systemet hanterar stora volymer av anonyma besökare med hjälp av delade resurser och hastighetsbegränsning.
* **Optimera för SEO**: Plattformen förbereder offentliga sidor för sökmotorindexering, vilket gör utbildningsinnehållet lättare att hitta.

### Förutsättningar för att inte vara inloggad

* Du måste aktivera Training Data Access Connector i integrationsadministratören innan du kan använda den icke-inloggade upplevelsen.
* Kopplingen exporterar kursmetadata till ett offentligt arkiv, vilket håller icke-inloggade sidor uppdaterade.

#### Initiering av anslutningen för utbildningsdataåtkomst

Träningsdataåtkomstanslutningen (TDA) är en viktig förutsättning för att aktivera den nya icke-inloggade Experience Builder-funktionen i ALM. Anslutningen underlättar export av utbildningsmetadata, vilket gör att din portal kan visa kursinformation för användare som inte är inloggade.

* **Anslutningsaktivering**: Du måste aktivera TDA-anslutningen från panelen för integrationsadministratörer. Det här steget aktiverar den icke-inloggade Experience Builder-funktionen och gör relevanta gränssnittsalternativ synliga i administratörsgränssnittet.
* **Metadataexport**: När anslutningen har aktiverats exporteras viktiga utbildningsmetadata (t.ex. kursnamn, beskrivning, översikt, betyg, varaktighet och färdigheter) från ALM till ett offentligt arkiv. Dessa data används för att fylla i icke-inloggade sidor och widgetar.
* **Schemaläggning och synkronisering**: Exportprocessen kan schemaläggas (t.ex. varje dag) för att se till att din portal återspeglar de senaste kursuppdateringarna. Ändringar som görs i ALM visas på icke-inloggade sidor efter nästa exportcykel, beroende på cache-lagring och exportfrekvens.
* **Funktionstillgänglighet**: De funktioner i Experience Builder som inte är inloggade, inklusive menyskapande, widgetstöd och katalogsynlighet, är bara tillgängliga efter att TDA-anslutningen har initierats. Om anslutningen inte är aktiverad förblir Experience Builder begränsat till inloggade användarscenarier.
* **Migrering och support**: För konton som övergår från äldre, icke-inloggade startsidafunktioner är initieringen av TDA-anslutningen det första steget mot migrering. Då kan du använda den nya Experience Builder-applikationens flexibilitet och förbättrade funktioner.


### Vad besökare kan göra utan att logga in

På en webbplats som inte är inloggad Experience Builder kan besökare bläddra i utbildningskatalogen genom att öppna katalogsidan för offentliga kataloger. De kan använda filter som katalog, produkt, roll, typ, färdigheter och taggar beroende på hur du har konfigurerat platsen. Besökare kan också söka efter utbildningar med hjälp av det globala sökfältet i sidhuvudet (om det är aktiverat) och visa sökresultat direkt på katalogsidan.

Besökare kan visa utbildningsinformation genom att öppna översiktssidor för kurser, utbildningsvägar och certifieringar. Dessa sidor visar viktiga metadata, inklusive titel, beskrivning, författare, varaktighet, format, taggar och färdigheter.

Dessutom kan besökare utforska statiskt innehåll och reklaminnehåll. De kan läsa text och innehållsblock, visa banderoller och bildpaneler och interagera med inbäddade iFrame-objekt som externa mikrowebbplatser, videor eller verktyg.

Om en besökare klickar på Registrera dig eller försöker starta utbildning uppmanas hen att logga in eller registrera sig. Efter lyckad inloggning omdirigeras besökaren till rätt sida, oavsett om det är startsidan, en anpassad sida eller den specifika utbildning som de valt.

### Vad är inte tillgängligt utan att logga in

På en Experience Builder-webbplats som inte är inloggad kan besökare inte komma åt funktioner eller innehåll som kräver användarautentisering. De kan inte registrera sig för utbildningar, starta eller konsumera kurser eller komma åt personliga widgetar som Min utbildning, Kalender, Efterlevnad, Ledartavla eller Social utbildning. Dessa widgetar är beroende av användarspecifika data och är bara tillgängliga efter inloggning.

Besökare kan inte heller utföra åtgärder som att registrera sig för en kurs eller komma åt innehåll som kräver spårning av förlopp eller användarkontext. Om du försöker registrera dig eller starta en utbildning uppmanas besökaren att logga in eller registrera sig innan han/hon fortsätter.

### Widgetar som stöds i icke-inloggat läge

I icke-inloggat läge stöds endast widgetar som inte kräver användarspecifika data. Dessa omfattar:

* Kategorier, widget, som visar tillgängliga utbildningskategorier.
* Widgeten Kurser och banor som visar kurser och utbildningsvägar från den offentliga katalogen.
* Innehållsruta, för att lägga till statisk text, bilder eller kampanjinnehåll.
* HTML-widgeten för att bädda in anpassat HTML-innehåll.
* iFrame-widgeten, för att visa externa webbplatser, videor eller verktyg på sidan.
* Widgetar som kräver användarkontext, t.ex. Min utbildning, Kalender, Efterlevnad, Ledartavla och Social utbildning, är inte tillgängliga i icke-inloggat läge.

### Sidor och menyer som inte är inloggade

* Endast en meny som inte är inloggad stöds, och den är synlig för alla besökare utan autentisering.
* Sidor kan läggas till i både inloggade och icke-inloggade menyer. Om en sida finns på båda sidorna anpassas widgetarna och innehållet efter användarens inloggningsläge.
* Menyer som inte är inloggade har ingen målgruppsanpassning eller anpassning. Alla ser samma uppsättning sidor.
* Widgetar som inte stöds i icke-inloggat läge döljs automatiskt. Sidlayouten justeras för att fylla luckor.
* Meny- och sidhantering (lägga till, förhandsgranska, ta bort) fungerar som inloggat läge, men med anpassningar för begränsningar som inte är inloggade.

### Sök- och katalogbeteende

I icke-inloggat läge kan användare komma åt katalogsidan och använda sökning för att bläddra bland tillgängliga kurser och utbildningsvägar. Katalogsidan visar alla offentliga kurser, tillsammans med filter och sökfunktioner, med samma kontoinställningar som i inloggat läge. När en användare söker visas resultaten på katalogsidan, och användare kan visa kurs- och instansöversiktssidor utan att logga in. Åtgärder som registrering kräver dock inloggning.

Om en användare försöker registrera sig kräver systemet att användaren loggar in först. Sökningen efter icke-inloggade användare är enklare än den för inloggade användare och omfattar inte avancerade funktioner som AI Assistant-integrering.

### Tekniskt genomförande

#### Konfiguration av anslutningen för utbildningsdataåtkomst

Du måste aktivera anslutningen för utbildningsdataåtkomst i panelen Integreringsadministratör innan du kan använda funktionen för Experience Builder som inte är inloggad. Med den här anslutningen exporteras utbildningsmetadata från ALM till ett offentligt arkiv, vilket gör det tillgängligt via API:er för sidor som inte är inloggade. Anslutningsinställningarna är en förutsättning för att aktivera funktionen och ser till att portalen visar aktuell utbildningsinformation.

#### Exportera och synkronisera metadata

Kopplingen exporterar viktiga metadatafält som kursnamn, översikt, beskrivning, gradering, varaktighet och färdigheter. Du kan schemalägga exporter (till exempel dagligen) för att hålla din portal synkroniserad med ALM. Alla metadatafält kanske inte ingår. Kontakta den tekniska avdelningen för en fullständig lista. Exporterade data används för att fylla i sidor som inte är inloggade, och ändringar i ALM visas efter nästa exportcykel.

#### Frekvens för cachelagring och export

Systemet använder backend-exportfrekvens och frontend-cachelagring för att hantera datauppdateringar. Ändringar som görs i ALM återspeglas i din portal efter den schemalagda exporten och cacheuppdateringen. Vissa uppdateringar kanske inte visas omedelbart på grund av dessa mekanismer. Om du behöver snabbare uppdateringar justerar du exportschemat eller rensar cachen efter behov.

#### Stöd för CSS/JS-anpassning

Du kan använda anpassade CSS och JavaScript på både inloggade och icke-inloggade sidor med hjälp av fliken Anpassning. Detta gör att du kan upprätthålla en konsekvent varumärkning, lägga till anpassade användargränssnittselement och förbättra användarupplevelsen i hela portalen. Alla anpassningar tillämpas globalt, vilket säkerställer ett enhetligt utseende och känsla.

#### URL-skillnader och varumärkning (favicon, sidrubrik)

Sidor som inte är inloggade och inloggade kan ha olika URL:er för att skilja mellan användartillstånd. Du kan anpassa favicon och sidtiteln för din portal, vilket stärker din varumärkesidentitet. De här funktionerna är tillgängliga i Experience Builder. Kontakta tekniker för senaste status om icke-inloggad support.

### Prestanda och skalbarhet

#### Delad stack jämfört med premiumstack

Den delade stacken gör det möjligt för flera kunder att använda det icke-inloggade Experience Builder på gemensam infrastruktur, med stöd för standardtrafiknivåer. Premium-stacken är ett betalt alternativ som ger tillgång till dedikerade resurser, realtidsfunktioner och högre platsgränser för kunder med avancerade behov. Välj stack utifrån dina förväntade trafik- och affärskrav.

#### Trafikbegränsningar och hastighetsbegränsningar

Den delade stacken tillämpar trafikbegränsningar för att säkerställa en rättvis användning bland kunderna. Teknikteamet implementerar hastighetsbegränsningar för att förhindra att en enskild kund förbrukar alla resurser. Om du planerar marknadsföringskampanjer eller förväntar dig mycket trafik ska du samordna dig med teknikerna för att förstå dina gränser och undvika avbrott i tjänsten. Hastighetsbegränsning hjälper till att upprätthålla systemets stabilitet och prestanda för alla användare.

#### Överväganden gällande multitenans och sökmotoroptimering

Plattformen har stöd för flera klientorganisationer, vilket gör att flera kunder kan ha sina portaler på delade infrastrukturer. Sidor som inte är inloggade är SEO-vänliga, tillsammans med sitemap.xml och robots.txt för att optimera sökmotorsynligheten. Detta säkerställer att din portal kan upptäckas och indexeras på rätt sätt av sökmotorer.

### Migrering och borttagning

#### Övergång från befintlig startsida som inte är inloggad

Du bör återskapa din startsida med det nya Experience Builder för ökad flexibilitet, widgetstöd och förbättrad användarupplevelse. Övergångsplanen säkerställer minimala störningar och fortsatt stöd.

#### Kommunikationsplan

Kunder som använder den äldre startsidan får tydlig information om tidslinjen för utfasningen och migreringsstegen. Stöd kommer att ges för att hjälpa dig att flytta din hemsida till den nya Experience Builder-plattformen, vilket säkerställer att du drar nytta av nya funktioner och pågående uppdateringar.

### Lokaliserings- och inloggningsstöd

#### Återställningslogik för språkinställning

Sidor visas på det språk som de skapades på. Om en användares språkinställning inte är tillgänglig använder systemet en reservlogik för att välja nästa bästa tillgängliga språkinställning. Det garanterar att användarna alltid ser innehållet på ett språk som stöds, vilket förbättrar tillgängligheten och användarnas tillfredsställelse.

#### Inloggningstyper som stöds

Den icke-inloggade upplevelsen har stöd för alla inloggningstyper i ALM, inklusive enkel inloggning och standardinloggning. Användare kan bläddra i innehåll utan att logga in och kommer att uppmanas att logga in när det behövs, till exempel för att registrera sig för en kurs eller komma åt personliga funktioner. Detta ger en smidig övergång från bläddring till engagemang.


### Icke-inloggade API:er

#### API för utbildningsobjekt för admin

Icke-inloggade Experience Builder-sidor och fjärradministrerade portaler ordnar eller filtrerar ofta kurser baserat på produkt och roll. API:et för Admin LO har förbättrats för att säkerställa att dessa associationer är konsekvent tillgängliga för serverdelsintegreringar och fjärradministrerade integrationer samt för TDA-anslutningen.

**Slutpunkt och beteende**

Du fortsätter att använda den befintliga Admin LO-slutpunkten:

```
GET /primeapi/v2/learningObjects/{loId}?enforcedFields[learningObject]=products,roles
```

Där:

* loId är utbildningsobjektets ID (till exempel kurs:12345).
* enforcedFields[learningObject] instruerar API:t att uttryckligen inkludera produkter och roller för den LO:n.

Detta uppnås genom att säkerställa att LO:s produkt- och rollassociationer är närvarande i svaret när de begärs via enforcedFields. Svaret innehåller sedan, i attribut, de produkt- och rollmetadata som behövs för att beräkna eller visa de rekommenderade produkterna (rec\_products) och rollerna (rec\_roles) för Experience Builder och andra användare.

Ett vanligt samtal från en administratör eller integrering ser ut så här:

```
url -X GET \
 "https://{your-domain}/primeapi/v2/learningObjects/course:12345?enforcedFields[learningObject]=products,roles" \
 -H "Authorization: Bearer {admin\_token}" \
 -H "Accept: application/vnd.api+json
```

Den returnerade LO JSON är samma grundläggande struktur som tidigare, men nu kan du lita på att produkt-/rollfält är närvarande när du begär dem med enforcedFields. Integreringar som inte använder enforcedFields fortsätter att fungera som tidigare.

#### Lista utbildningsobjekt - stöd för arbetsstöd i effectiveModifiedDate-filter

**Syfte**

Anslutningsprogrammet för utbildningsdataåtkomst (TDA) och fjärradministrerade implementeringar behöver ofta utföra inkrementell synkronisering baserat på utbildningsobjektens **effektiva ändringsdatum**. Fram till den här versionen hanterades inte arbetsstöd (LO-typ arbetsstöd) korrekt när det kombinerades med effectiveModifiedDate-filter. I den här versionen har det här problemet åtgärdats så att arbetsstöd kan synkroniseras stegvis precis som kurser och utbildningsvägar.

**Slutpunkt och beteende**

Du använder den befintliga slutpunkten för LO-listan med datumfilter och LO-typ:

```
GET /primeapi/v2/learningObjects
 ?filter.effectiveModifiedDate.fromDate=2025-03-15T13:14:56.000Z
 &filter.effectiveModifiedDate.toDate=2025-03-20T13:14:56.000Z
 &filter.loTypes=jobAid
```

Tidigare, när filter.loTypes=jobAid kombinerades med ett effectiveModifiedDate-intervall, uteslöt filtret i själva verket JobAids, och anropet betedde sig som om JobAids inte stöddes.

Från den här uppdateringen och framåt returnerar anropet bara JobAid-utbildningsobjekt vars effectiveModifiedDate ligger inom det angivna fönstret.

```
{
 "links": {
 "self": "https://acapapiserver/primeapi/v2/learningObjects?page[limit]=10&filter.effectiveModifiedDate.fromDate=2026-01-19T13:14:56.000Z&filter.effectiveModifiedDate.toDate=2026-01-21T13:14:56.000Z&filter.loTypes=jobAid"
 },
 "data": [
 {
 "id": "jobAid:144968",
 "type": "learningObject",
 "attributes": {
 "authorNames": ["Author"],
 "dateCreated": "2026-01-20T08:48:55.000Z",
 "datePublished": "2026-01-20T08:48:55.000Z",
 "dateUpdated": "2026-01-20T08:48:55.000Z",
 "effectiveModifiedDate": "2026-01-05T07:31:18.000Z",
 "loType": "jobAid",
 "loFormat": "Content",
 "loResourceType": "Content",
 "localizedMetadata": [
 {
 "description": "Link jobAid new",
 "locale": "en-US",
 "name": "Link jobAid new"
 },
 {
 "description": "Link jobAid new fre",
 "locale": "fr-FR",
 "name": "Link jobAid new fre"
 }
 ],
 "relationships": {
 "authors": {
 "data": [
 { "id": "13385176", "type": "user" }
 ]
 },
 "instances": {
 "data": [
 { "id": "jobAid:144891\_-1", "type": "learningObjectInstance" }
 ]
 }
 }
 }
 }
 ]
}
```

Det innebär att du nu säkert kan implementera inkrementell JobAid-synkning baserad på effectiveModifiedDate, på samma sätt som du redan gör för andra typer.

Om du utelämnar filter.loTypes=jobAid ändras beteendet för andra LO-typer. Ändringen påverkar bara kombinationen av JobAid med det filtret.

#### **Meny-API: Filter för menyer som inte är inloggade**

**Syfte**

Experience Builder och frontender utan huvud behöver ett enkelt sätt att hämta den **icke-inloggade menyn**, som definierar navigering för offentliga besökare. Innan den här versionen var du tvungen att hämta alla menyer och sedan använda anpassad logik för att identifiera vilken som representerade den icke-inloggade navigeringen. Den här versionen lägger till ett enkelt serverfilter.

**Slutpunkt och beteende**

Du använder den befintliga Menu-listan med slutpunkt med en ny frågeparameter:

```
GET /primeapi/v2/templates/menus?include=pages,subMenus.pages&isNonLoggedIn=true
```

Huvudpunkterna är följande:

* include=pages,subMenus.pages är valfritt men rekommenderas när du behöver sid- och undermenysidinformationen i samma svar.
* isNonLoggedIn=true är ny i den här versionen och talar om för servern att endast returnera menyer som är flaggade som icke-inloggade menyer.

Utan parametern isNonLoggedIn fungerar slutpunkten exakt som förut och returnerar menyer enligt det befintliga standardbeteendet. Med isNonLoggedIn=true returnerar den vanligtvis den enda meny som används av den icke-inloggade upplevelsen för ditt konto (eftersom det normalt finns en icke-inloggad meny per konto).

I praktiken kan en kund nu utfärda:

```
curl -X GET \
 "https://{your-domain}/primeapi/v2/templates/menus?include=pages,subMenus.pages&isNonLoggedIn=true" \
 -H "Authorization: Bearer {admin\_token}" \
 -H "Accept: application/vnd.api+json"
```

och få tillbaka den icke-inloggade navigeringsstrukturen i ett samtal, med alla sidor som bör vara synliga för anonyma besökare.

Detta är särskilt användbart när du skapar en webbplats som inte är inloggad och vill spegla samma navigering som Experience Builder använder eller när du felsöker om menyn som inte är inloggad har konfigurerats korrekt.

### Tillåt listning av anpassade domäner

Den icke-inloggade stacken består av:

* En offentlig CDN-domän (till exempel cpcontents.adobe.com eller yourdomain.example.com) som visar layouter, konfiguration-JSON och statiska resurser.
* En offentlig Elasticsearch-slutpunkt (ES) som betjänar katalog- och sökdata, men bara om begäran kommer från en **tillåten domän** för det ALM-kontot.

När du inför en anpassad domän fungerar den sömlöst utan extra ansträngning att följa den befintliga processen för att lägga till en anpassad domän.

#### Förutsättningar

Innan du godkänner en anpassad domän som inte är inloggad:

1. Den anpassade domänen är konfigurerad för ditt ALM-konto (DNS för academy.yourcompany.com pekar till exempel på Adobe/Akamai och certifikat tillhandahålls).
2. Anslutningsprogrammet **Åtkomst till utbildningsdata (TDA)** har aktiverats för kontot.
3. Funktionen **Experience Builder som inte är inloggad** har aktiverats (Adobe).

Dessa steg säkerställer att:

* Ditt konto har en **konto-JSON** som inte är inloggad (kallas ofta accountConfig / experienceBuilderConfig) och som innehåller fält som cpDomain, almDomain, almCdnBaseUrl, esBaseUrl och domäner som tillåts.
* Den icke-inloggade stacken vet var data ska skickas och från vilka domäner begäranden ska godkännas.

#### Hur tillåtelselista fungerar

Tillåtelselistan lagras i konfigurationen som TDA exporterar och stacken som inte är inloggad läses. Konfigurationen omfattar:

* ALM-domäner (cpDomain, almDomain).
* **URL-bas-URL:en** för innehåll som inte är inloggat (almCdnBaseUrl).
* URL:en **offentlig sökbas** (esBaseUrl).
* Listan över domäner som tillåts göra offentliga icke-inloggade anrop för det kontot.

För att Experience Builder som inte är inloggad ska fungera på en anpassad domän:

* Webbläsaren måste läsa in den icke-inloggade HTML från den anpassade domänen (eller från den ALM-icke-inloggade CDN-domänen, beroende på konfigurationen).
* Anrop från den domänen till offentliga ES- och CDN-slutpunkter måste accepteras. Det händer bara om domänen finns på listan med tillåtna domäner.

Den här versionen lägger till en ny CDN-domän, cpcontents.adobe.com, som inte är inloggad och anger att den måste placeras i de **tillåtna domänerna** i TDA-anslutningen. För befintliga interna användare som inte är inloggade krävs en uppdatering.

#### Tillåt lista en anpassad domän

**Konfigurera den anpassade domänen i ALM**

Arbeta tillsammans med Adobe för att registrera din domän, t.ex. academy.yourcompany.com, som anpassad domän för ditt ALM-konto. Du uppdaterar DNS så att den pekar på Adobe Akamai enligt instruktionerna och väntar på att SSL och routning ska slutföras.

I det här läget kan både inloggad och icke-inloggad trafik nå ALM via den domänen, men icke-inloggade sök- och kataloganrop kan fortfarande blockeras om domänen inte är tillåten.

**Aktivera TDA och icke-inloggad Experience Builder**

Se till att:

* Anslutningen **Åtkomst till utbildningsdata** har aktiverats.
* Funktionen **Ej inloggad Experience Builder** är aktiverad för kontot.

Aktivering av TDA skapar eller uppdaterar JSON för det icke inloggade kontot. För nya konton tillåter processen även en lista över den nya CDN-domänen som inte är inloggad (cpcontent.adobe.com) som standard, så den offentliga ES-slutpunkten förväntar sig anrop från den domänen.

För konton som redan använde den äldre icke-inloggade stacken måste befintliga anslutningar tas bort och återskapas för att den nya domänen ska kunna hämtas.

**Lägg till den anpassade domänen i listan över tillåtna domäner**

Den kritiska delen talar om för den icke-inloggade ES-stacken att academy.yourcompany.com är ett godkänt ursprung. Det finns två gemensamma vägar.

1. **Återaktivera TDA-anslutningen (enkel, självbetjäningsvänlig)**

Befintliga inhemska användare som inte är inloggade måste ta bort och återaktivera TDA-anslutningen så att den nya domänen automatiskt tillåts. Genom att göra detta uppnår du två saker:

1. JSON-kontot som inte är inloggat genereras om.
2. De tillåtna domänerna uppdateras med den nya CDN-domänen som inte är inloggad och din anpassade domän.

Detta rekommenderas när du har ett litet antal konton och kan tolerera att du tillfälligt inaktiverar och återaktiverar anslutningen.

1. **Kontrollera att domänen verkligen är tillåtelselistad**

Efter tillåt listning, öppna din icke-inloggade webbplats på den anpassade domänen och inspektera webbläsarens nätverksanrop.

Du vill se:

* Förfrågningar till almCdnBaseUrl (till exempel <https://cpcontent.adobe.com/>...) med 200/304.
* Förfrågningar till esBaseUrl (offentligt sök-API, till exempel <https://primeapps.adobe.com/almsearch/api/v1/>...) JSON har returnerats med sök-/katalogdata.

Om dessa anrop returnerar 4xx eller explicita fel som föreslår &quot;ej betrodd domän&quot; eller &quot;ursprung ej tillåtet&quot;, är tillåtelselistan ofullständig eller felkonfigurerad och supporten måste justera den.

Den icke-inloggade LLD:n noterar också att kontokonfigurationen kan innehålla ett förväntat domänvärde. Vid körning kontrollerar webbplatsen att domänen i URL:en matchar det som angetts i konfigurationen. Om den inte gör det kan användaren omdirigeras till en felsida. Detta skyddar mot att en kunds konfiguration nås via en annan kunds domän.

### Använda rekommendationer i Experience Builder som inte är inloggad

Med den icke-inloggade Experience Builder kan du skapa offentliga utbildningssidor där besökare kan bläddra i din katalog och se markerat innehåll innan de loggar in. Även om dessa besökare är anonyma kan du ändå presentera rekommenderade utbildningar med hjälp av metadata och widgetar.

I den inloggade elevappen kan rekommendationer anpassas: de kan bero på elevens profil, historia, färdigheter och framsteg. I upplevelsen **Inte inloggad** finns det ingen elevidentitet än, så plattformen kan inte anpassa per användare.

Recommendations i icke-inloggat läge är därför:

* **Kurerat eller regelbaserat**: baserat på katalog, produkt, roll, etiketter, taggar och andra metadata.
* **Segmentorienterat**: &quot;rekommenderas för utvecklare&quot;, &quot;rekommenderas för partner&quot;, &quot;visas för nybörjare&quot;.
* **Marknadsföringsfokuserad**: Används för att locka och vägleda besökare som vill registrera sig när de loggar in.

### Metadata och API:er som stöder rekommendationer

Bakom kulisserna använder icke-inloggade sidor:

* **TDA-kopplingen** för att exportera metadata för utbildningsobjekt (kurser, vägar, certifieringar, arbetsstöd) till ett offentligt sökindex.
* Den **offentliga sökstacken** för att svara på frågor från icke-inloggade widgetar (katalog, sökning, kurser och sökvägar, kategorier).
* **API:et för Admin-utbildningsobjekt** för att visa produkt- och rollmetadata som kan användas för rekommendationsregler.

I den här versionen utökades API:et för Admin LO så att produkt- och rollassociationer är tillförlitligt tillgängliga:

```
GET /primeapi/v2/learningObjects/{loId}?enforcedFields[learningObject]=products,roles
```

Detta gör det möjligt för widgetar och rubrikfria integreringar att skapa regelbaserade rekommendationer med hjälp av produkter, roller, katalogetiketter, taggar och andra fält på ett konsekvent sätt.

### Utforma rekommendationsavsnitt med Experience Builder-widgetar

Du skapar rekommendationsavsnitt på icke-inloggade sidor genom att kombinera **Experience Builder-widgetar** med metadatafilter.

#### **Widget för kurser och banor**

Använd widgeten **Kurser och banor** när du vill visa en rad eller ett rutnät med rekommenderade objekt. I dess konfiguration kan du välja:

* Vilka kataloger att hämta från.
* Vilka katalogetiketter, produkter, roller eller taggar som ska användas som filter.
* Om du vill visa kurser, vägar, certifieringar, arbetsstöd eller en blandning.
* Sortering och maximalt antal objekt.

Du kan till exempel skapa

* &quot;Rekommenderas för utvecklare&quot;: Filtrera efter en produkt eller roll du använder för utvecklarinnehåll.
* &quot;Börja här&quot;: filtrera efter en etikett som &quot;Starter&quot; eller &quot;Onboarding&quot;.
* &quot;Utvalt det här kvartalet&quot;: filtreras av en tidsbunden etikett som utvalda-q3-2026.

Widgeten lär sig inte av beteendet utan visar det som matchar de metadataregler du definierar. Ur besökarens synvinkel ser det dock ut som en rekommendationsremsa.

#### **Kategoriwidget**

Använd widgeten **Kategorier** för att hjälpa besökare att navigera till rekommenderade uppsättningar innehåll, även om de inte känner till dina produktnamn.

Du kan konfigurera plattor som representerar ett segment, till exempel:

* &quot;För administratörer&quot;
* &quot;För säljteam&quot;
* &quot;För partner&quot;
* &quot;Efter produktlinje&quot;

Varje ruta kan länka antingen till:

* En filtrerad katalogsida (t.ex. den katalog som filtreras av vissa produkter eller etiketter).
* En dedikerad icke-inloggad sida som använder kurser och sökvägar som är förkonfigurerade för det segmentet.

Detta ger dig en upplevelse av &quot;rekommenderade banor efter segment&quot; utan anpassning.

### Skapa segmentbaserade rekommendationer

Eftersom icke-inloggade besökare ännu inte har någon ALM-profil är det bra att utforma rekommendationer **efter segment** och låta besökarna välja själva.

1. Använd en **icke-inloggad startsida** som kortfattat förklarar vem din akademi är till för och visar ett litet antal ingångspunkter för segment (t.ex. &quot;Utvecklare&quot;, &quot;Marknadsförare&quot;, &quot;Partner&quot;, &quot;Nya anställda&quot;). Detta kan du göra med en Kategorier-widget eller en enkel innehållsruta eller ett HTML-avsnitt med knappar.
2. Skapa en **dedikerad, ej inloggad sida** i Experience Builder för varje segment. På den sidan använder du en eller flera kurser och sökvägar som har konfigurerats med filter som representerar vad som &quot;rekommenderas&quot; för den gruppen. För &quot;Utvecklare&quot; kan du till exempel filtrera på:
   1. KATALOG = &quot;OFFENTLIG UTBILDNING&quot;
   2. Produkt = &quot;Adobe Experience Manager&quot;
   3. Taggar = &quot;Grundläggande för utvecklare&quot;
3. Använd de här segmentsidorna som mål för dina marknadsföringskampanjer och som mål för panelerna på den icke-inloggade startsidan.

Besökare uppfattar att de ser rekommendationer som är skräddarsydda efter deras situation, även om logiken definieras i designläge via metadata.

### Övergå från icke-inloggade till personliga rekommendationer

Rekommendationer som inte är inloggade handlar främst om **upptäckbarhet** och **konvertering**. När besökarna bestämmer sig för att registrera sig eller påbörja utbildningen kommer de att logga in och bli fullvärdiga elever med en profil och historik.

Det vanliga flödet är:

1. En besökare upptäcker innehåll via de rekommenderade avsnitten som inte är inloggade (hemrekommendationer, landningssidor för segment, utvalda rader).
2. De klickar i en kurs- eller banöversikt och väljer att registrera sig eller börja.
3. ALM uppmanar dem att registrera sig eller logga in.
4. När de har loggat in tar den inloggade standardupplevelsen över, bland annat:
   1. &quot;Mitt lärande&quot;
   2. Inloggad katalog med personlig status
   3. Alla interna rekommendationssystem du använder för befintliga elever.

Med andra ord hjälper de inloggade rekommendationerna dem att bestämma vad de ska göra härnäst och fortsätta.

### Hur arbetsstöd kan användas i den nya, icke-inloggade Experience Builder

I **användargränssnittet** deltar arbetsstöd i icke-inloggade upplevelser främst genom widgetarna som kan visa utbildningsobjekt:

1. **Widgeten Kurser och banor**
Denna widget kan visa flera LO-typer, inklusive arbetsstöd. På sidor som inte är inloggade kan du konfigurera den för att:
   1. Inkludera eller exkludera arbetsstöd uttryckligen.
   2. Filtrera jobbhjälp efter katalog, produkt, roll, etiketter, taggar och andra metadata.
   3. Presentera dem tillsammans med kurser och vägar eller som en separat &quot;Resurser&quot; remsa.

På en offentlig landningssida kan du till exempel konfigurera en remsa med titeln &quot;Användbara resurser&quot; som endast visar arbetsstöd och en annan remsa med titeln &quot;Rekommenderade kurser&quot; som visar kurser och vägar.

1. **Katalogsida och sökning**
Ytorna för de **kataloger** och **sökningar** som inte är inloggade använder det offentliga sökindexet (matas av anslutningen för utbildningsdataåtkomst). Indexet stöder nu arbetsstöd korrekt, så:
   1. Sökresultat som inte är inloggade kan innehålla arbetsstöd.
   2. Icke-inloggade katalogfilter (efter typ, produkt, taggar osv.) kan innehålla arbetsstöd så länge din kontokonfiguration och dina widgetar är inställda för att visa dem.
2. **LO-översiktssidor**
När en besökare klickar på ett arbetsstöd från någon widget eller från katalogen går de till en **LO-översiktssida** för det arbetsstödet i icke-inloggat läge. Därifrån kan de läsa dess beskrivning och metadata. Faktisk nedladdning eller konsumtion kräver vanligtvis fortfarande inloggning, men förekomst och upptäckbarhet av själva arbetsstödet hanteras av den icke-inloggade upplevelsen.

### Så här visas arbetsstöd via API:er som inte är inloggade

På **API-sidan** stöds arbetsstöd av:

1. Anslutningen **Åtkomst till utbildningsdata och offentlig sökning**
TDA exporterar arbetsstödsmetadata tillsammans med andra LO-typer till det offentliga sökindexet som hanterar icke-inloggade sök- och katalogfrågor. Det är vad Experience Builder och huvudlösa fronter förlitar sig på.
2. Listan **Utbildningsobjekt med effectiveModifiedDate**
I den här versionen korrigerades slutpunkten för LO-listan så att arbetsstöd fungerar korrekt med filtret effectiveModifiedDate. Du kan nu ringa:

```
GET /primeapi/v2/learningObjects
 ?filter.effectiveModifiedDate.fromDate=2026-01-19T13:14:56.000Z
 &filter.effectiveModifiedDate.toDate=2026-01-21T13:14:56.000Z
 &filter.loTypes=jobAid
```

Före denna ändring returnerade inte arbetsstöd på ett tillförlitligt sätt genom att kombinera effectiveModifiedDate med loTypes=jobAid. Detta innebär följande:

1. Dina TDA- eller ETL-jobb kan **stegvis synka arbetsstöd** för icke-inloggade upplevelser, på samma sätt som de gör för kurser och vägar.
2. Alla implementeringar utan huvud som bygger en offentlig arbetsstödskatalog kan fråga efter ändringar baserat på effectiveModifiedDate och loType=jobAid.

**Anteckning**:

I icke-inloggat läge:

* Arbetsstöd kan främst **upptäckas**: besökare kan se att de finns, läsa beskrivningar och förstå hur de stöder ämnen eller kurser.
* Faktisk **förbrukning** (hämtning eller öppning av arbetsstödsinnehåll) kräver vanligtvis fortfarande inloggning, särskilt om arbetsstöd anses ingå i licensierat eller internt innehåll.

### Ändringar i en kort beskrivning i LO-sökningen (ej inloggad)

I stacken som inte är inloggad görs sökningar och listor över utbildningsobjekt (LO:er) med anslutningen Training Data Access (TDA) och ett offentligt Elasticsearch-index. Historiskt sett har denna stapel använt ett enda översikts-/beskrivningsfält för varje LO. Kunder som bygger huvudlösa icke-inloggade portaler ville visa samma korta beskrivning på LO-brickor som det inloggade elevgränssnittet visar, i stället för bara den långa översikten.

Ändringen introducerar stöd för LO **kort beskrivning** i icke-inloggade API:er för sökning och listning:

* För **kurser** är den befintliga gränssnittssemantiken:
* Inloggade kort visar en kort beskrivning (140 tecken långt fält) om det finns, annars faller de tillbaka till den långa detaljerade översikten.
* För **utbildningsvägar** använder det inloggade användargränssnittet fältet Fördelar som en kort beskrivning, om det har definierats, och återgår till översikten i annat fall.
* För **certifieringar** används en kort beskrivning, med en längre certifieringsöversikt som reserv.
* För **arbetsstöd** används fältet för huvudbeskrivning.

### Andra ändringar

#### Begränsning som innebär att inga två konton kan dela samma anpassade domän

I arkitekturer för inloggning och inloggning i Adobe Learning Manager behandlas en **anpassad domän** (t.ex. academy.example.com) som en globalt unik nyckel som måste mappas till exakt ett ALM-konto, så att plattformen tillämpar en fast begränsning som **inga två konton kan dela samma anpassade domän**. Detta krävs för säkerhet, routning och enkel inloggning: routningslagret och den icke-inloggade stacken använder domänen för att söka efter rätt kontokonfiguration (inklusive dess icke-inloggade konto-JSON, Experience Builder-menyer, varumärkning och TDA/sökslutpunkter).

Att tillåta samma anpassade domän på två konton skulle göra det omöjligt att garantera vilket kontos data returneras, orsaka läckage mellan klientorganisationer och även korrupta genererade artefakter som sitemap.xml och robots.txt som produceras per konto men upptäcks av sökmotorer per värd. Operativt innebär det att när du tilldelar eller flyttar en anpassad domän måste du först se till att den inte är kopplad till något annat konto (eller avregistrerar den där) och att Adobe interna verktyg avvisar försök att binda samma domän till flera konton.

#### Webbläsarcachelagring av resurser i den icke-inloggade upplevelsen

I den icke-inloggade upplevelsen i Adobe Learning Manager är webbläsarcachelagring av resurser en kärndel av prestations- och storleksstrategin, eftersom offentliga sidor måste hantera stor, ibland taggig marknadsföringstrafik med låg latens och minimal ursprungslast. Statiska och halvstatiska resurser som det icke inloggade HTML-skalet (till exempel index.html/guest.html), konfiguration på kontonivå JSON (account.json eller config.json), Experience Builder-sidlayout JSON (menyer, widgetlayouter, kortinställningar), CSS, JS, bilder och favikoner hanteras från ett Akamai-CDN (cpcontents.adobe.com / cpcontent.adobe.com) med cacherubriker som uppmuntrar båda CDN-side och browser-side reuse, så att efter den första sidan ladda webbläsaren kan återge efterföljande icke-inloggade sidor till stor del från sin cache, omvalidera endast vid behov via ETag eller Last-Modified.

## Flerspråkigt arbetsstöd

### Introduktion

Med hjälp av flerspråkiga arbetsstöd i Adobe Learning Manager (ALM) kan författare och administratörer tillhandahålla stöddokument, guider eller resurser på flera språk i en och samma arbetsstödspost. Elever i olika regioner kan komma åt relevant material på sitt önskade språk, vilket förbättrar förståelse, efterlevnad och användarupplevelse.

### Föregående beteende

Tidigare stöddes endast en innehållsfil per arbetsstöd i ALM, även om namnet och beskrivningen kunde lokaliseras. För att kunna tillhandahålla samma resurs på flera språk var författarna tvungna att skapa separata arbetsstöd för varje språk. Detta ledde till dubbelarbete, förvirring och ökade administrativa omkostnader. Det fanns inget enhetligt sätt att hantera flerspråkiga resurser, vilket gjorde det svårt att säkerställa konsekvens och spåra användning.

### Användningsfall

* **Global personalanpassning**: Ta fram säkerhetsmanualer, processguider eller referensdokument på flera språk till en mängd olika personer.
* **Regelefterlevnad**: Se till att alla anställda får samma efterlevnadsdokumentation på sitt modersmål.
* **Konsekvent introduktion**: Ange checklistor för nybörjare eller vanliga frågor på lokala språk för nyanställda över hela världen.
* **Minskad duplicering**: Hantera alla språkversioner av ett arbetsstöd i en enda post, vilket förenklar uppdateringar och rapportering.

### Viktiga funktioner

* **Stöd för flera språk**: Bifoga en unik fil eller URL för varje språk som stöds i ett enda arbetsstöd.
* **Lokaliserat namn och beskrivning**: Ange jobbstödets namn och beskrivning på varje språk.
* **Enhetlig hantering**: Redigera, uppdatera och rapportera om alla språkversioner från ett enda ställe.
* **Bakåtkompatibilitet**: Befintliga enspråkiga arbetsstöd replikeras automatiskt till alla tillagda språk tills nya filer har överförts.

### Skapa flerspråkigt arbetsstöd

1. Gå till rollen Författare och välj **Arbetsstöd**.
2. Välj **Skapa arbetsstöd**.
3. Ange arbetsstödets namn och beskrivning på standardspråket.
4. Lägg till den primära innehållsfilen eller URL-adressen för standardspråket.
5. Spara arbetsstödet.

### Lägg till ytterligare språk

1. I jobbstödsredigeraren väljer du **Lägg till språk**.
2. Välj önskat språk i listan.
3. För varje tillagt språk:
   * Ange det lokaliserade namnet och beskrivningen.
   * Överför motsvarande innehållsfil eller ange en språkspecifik URL.
4. Upprepa för alla obligatoriska språk.

### Redigera och hantera språk

1. Om du vill uppdatera en fil eller en beskrivning för ett visst språk väljer du fliken Språk och gör önskade ändringar.
2. Om ett språk läggs till efter att arbetsstödet har publicerats tilldelas originalfilen automatiskt det nya språket tills en unik fil överförs.
3. Ta bort eller ersätt filer för valfritt språk efter behov.

### Publish och elevupplevelse

1. Publicera arbetsstödet när alla språk och filer har lagts till.
2. Elever ser arbetsstödet på sitt valda innehållsspråk, med rätt fil eller URL.
3. Om en elevs språk inte är tillgängligt visas standardspråkfilen.

### Rapportering

1. Ladda ned jobbstödsrapporter för att visa detaljer om alla filer och språk som är associerade med varje arbetsstöd.
2. Rapporter innehåller språk, filnamn och användningsdata för spårning.

### Bästa praxis

* Tillhandahålla korrekta översättningar för namn, beskrivningar och innehållsfiler.
* Granska och uppdatera filer regelbundet för att säkerställa konsekvens mellan olika språk.
* Använd tydliga namnkonventioner för att särskilja filer för olika språk.
* Testa elevupplevelsen genom att byta innehållsspråk för att verifiera att filen levereras korrekt.

### Felsökning

* **Fil saknas för ett språk**: Standardfilen visas. Se till att rätt fil har överförts för alla språk.
* **Äldre arbetsstöd**: Lägg till nya språkfiler som ersätter automatiskt replikerade original.
* **Felaktigt språk visas**: Kontrollera elevens språkinställningar och arbetsstödets språkkonfiguration.

Med hjälp av flerspråkiga arbetsstöd kan du leverera stödresurser till en global publik på en och samma plats, minska dubbelarbete och se till att alla elever får rätt information på det språk de föredrar. Med den här funktionen blir Adobe Learning Manager mer tillgängligt, kompatibelt och administrationseffektivt.

## Få svar med AI-assistenten för elever

AI Assistant för elever är en AI-driven assistent i Adobe Learning Manager som utformats för att hjälpa dig att hitta den information du behöver snabbare. Genom att ställa frågor på naturligt språk kan du få sammanhangsberoende förklaringar, ta fram relevanta kurser och hämta insikter från utbildningsinnehåll - utan att bläddra i kataloger manuellt.

### Funktioner

* **Smarta frågesvar:** Hanterar både enkeltur- och flersvängningssamtal så att du kan ställa frågor på ett naturligt sätt. Svar fås från kurser, utbildningsvägar, certifieringar och arbetsstöd.
* **Innehållsgrundade svar med citat:** Hämtar information direkt från utbildningsmaterial och innehåller citat som pekar tillbaka till den ursprungliga kursen, modulen eller resursen.
* **Bred innehållskompatibilitet:** Stöder en mängd olika format, inklusive dokument, presentationer, videoklipp, ljudfiler, HTML-innehåll och SCORM-moduler (Sharable Content Object Reference Model).
* **Sömlös användarupplevelse:** Finns som en sidopanel på elevernas sidor och upprätthåller sessionsbaserad chatthistorik för kontinuitet.
* **Robusta administratörskontroller:** Administratörer kan aktivera eller inaktivera assistenten, begränsa åtkomsten för användargrupper och välja vilka interna kataloger som ska användas som källa för AI-genererade svar.

### Fördelar

* **Snabbare åtkomst till kunskap:** Du får snabba svar på dina frågor, vilket eliminerar behovet av att navigera genom flera kurser eller dokument.
* **Högre engagemang:** Samtalsinteraktioner gör inlärningen naturligare, mer intuitiv och mer tillgänglig.
* **Bättre förståelse:** Du kan ställa uppföljningsfrågor för att förtydliga begrepp och utforska ämnen mer ingående.
* **Skalbar utbildningssupport:** Automatiserade AI-drivna svar minimerar beroendet av ämnesexperter och supportteam.

Läs mer om [AI-assistent för elever](/help/migrated/learners/feature-summary/learner-ai-assistant.md).

## Stöd för flerspråkiga videotextspår (VTT)

Stöd för flerspråkiga videotextspår (VTT) i Adobe Learning Manager gör det möjligt för författare att tillhandahålla undertexter och bildtexter för video- och ljudinnehåll på flera språk. Den här funktionen effektiviserar lokaliseringen, gör utbildningen tillgänglig för en global publik och ser till att tillgänglighetskrav uppfylls. Författare kan automatiskt generera, översätta, granska och redigera VTT-filer direkt inom plattformen.

### Användningsfall

* **Global utbildning:** Leverera videoinnehåll med undertextning på flera språk så att det når internationella elever.
* **Tillgänglighetsefterlevnad:** Skriv bildtexter på önskat språk för hörselskadade användare.
* **Snabbare lokalisering:** Minska den manuella ansträngningen och påskynda innehållets lansering genom att automatiskt generera och översätta VTT-filer.
* **Konsekvent upplevelse:** Se till att alla elever får samma information, oavsett språk.

### Viktiga funktioner

* **Automatisk VTT-generering:** Överför en video- eller ljudfil och generera VTT-bildtexter automatiskt på originalspråket.
* **Flerspråkig översättning:** Översätt bildtexter till något av de 39 icke-engelska språk som stöds.
* **Granska och redigera i appen:** Granska, redigera och hämta VTT-filer före publicering.
* **Meddelanden:** Ta emot meddelanden i appen när genereringen och översättningen av VTT är slutförd.
* **Smidig publicering:** Publish har slutfört bildtexter som elever kan få åtkomst till på sitt valda språk.

### Ladda upp innehåll och generera VTT

1. Gå till innehållsbiblioteket och välj **Lägg till innehåll**.
2. Överför MP3- eller MP4-filen.
3. I dialogrutan för överföring väljer du alternativet att **generera översättning**.
4. Välj det ursprungliga innehållsspråket (filens språk används som standard).
5. Välj ytterligare målspråk för översättning (upp till 39 stöds).
6. Välj **Spara**. Systemet börjar skapa och översätta VTT-filer.

### Övervaka förloppet

1. När du har sparat visas den nya innehållsposten i innehållsbiblioteket.
2. En förloppsindikator visar status för generering och översättning av VTT.
3. Du får ett meddelande i programmet när processen har slutförts.

### Granska och redigera VTT-filer

1. Öppna innehållet i läget **Redigera** i innehållsbiblioteket.
2. Välj länken **Granska** bredvid VTT-filen för varje språk.
3. Ett popup-fönster visar bildtexterna för det språket.
4. Redigera bildtexter direkt i popup-fönstret eller hämta VTT-filen för offlineredigering.
5. När du har gjort ändringar överför eller klistrar du in den ändrade bildtexten i popup-fönstret igen.
6. Spara ändringarna.

### Publish-bildtexter

1. När du är nöjd med alla språkbeskrivningar publicerar du innehållet.
2. Elever ser undertextningsalternativ på alla publicerade språk när de tittar på videon.

### Ytterligare information

* **Språk som stöds:** Alla 39 språk som inte stöds av Adobe Learning Manager.
* **Meddelanden:** Författare meddelas när genereringen och översättningen av VTT är slutförd.
* **Redigeringsflexibilitet:** Bildtexter kan redigeras i appen eller offline och överföras på nytt.
* **Skalbarhet:** Utformad för lokaliserings- och tillgänglighetsbehov i företagsklass.
* **Du behöver inte göra någon manuell VTT-överföring:** Systemet kan skapa VTT-filer från början med hjälp av den video/ljud som överförts.

### Bästa praxis

* Granska alltid automatiskt genererade bildtexter för noggrannhet före publicering.
* Tillhandahåll översättningar för alla större elevgrupper för att maximera tillgängligheten.
* Använd meddelandesystemet för att hålla dig uppdaterad om bearbetningsstatus.
* Uppdatera bildtexter regelbundet om videoinnehållet ändras.

### Felsökning

* Om VTT-genereringen misslyckas kontrollerar du att filen har ett format som stöds (MP3/MP4).
* Kontrollera att de saknade språken stöds och är markerade under överföringen.
* Om bildtexterna inte är synkroniserade kan du justera tidsinställningen med redigeraren i appen.

Stöd för flerspråkig VTT gör att du kan erbjuda lättillgängliga, lokaliserade videoupplevelser effektivt. Genom att använda automatisk generering, översättning och redigering i appen kan du se till att innehållet når och stöder alla elever, oavsett språk.

## Utforma anpassade certifikat

Med anpassade certifikat i Adobe Learning Manager (ALM) kan administratörer och författare designa, hantera och utfärda anpassade certifikat för elever. I funktionen ingår en dra och släpp-redigerare, dynamiska fält, flerspråkigt stöd och AI-genererade bakgrunder så att organisationer kan skapa varumärkta certifikat utan teknisk expertis.

### Föregående beteende

Tidigare var skapandet av certifikat i ALM begränsat av rigiditet i mallarna, brist på anpassning och tekniska hinder (t.ex. redigering i HTML). Kunderna ville ha enklare sätt att designa certifikat, lägga till dynamiska fält (t.ex. elevnamn eller instruktör) och stödja flera språk, samtidigt som varumärket förblir konsekvent och visuellt tilltalande.

### Användningsfall

* **Varumärkt erkännande**: Utfärda certifikat med företagslogotyper, färger och teckensnitt för efterlevnad, utbildning eller resultat.
* **Dynamisk anpassning**: Fyll automatiskt i elevnamn, instruktörsnamn och andra aktiva fält.
* **Flerspråkig leverans**: Ange certifikat på flera språk för globala elever.
* **Flexibel design**: Skapa certifikat för landskap eller porträtt, använd AI-genererade bakgrunder och förhandsgranska före publicering.

### Få åtkomst till anpassade certifikat

1. Gå till avsnittet **Achievements** på startsidan för Admin (kallades tidigare **Badges**).
2. Välj **Certifikat** för att visa, skapa eller hantera certifikatmallar.

### Skapa ett certifikat

1. Välj **Skapa certifikat**.
2. Välj stående eller liggande orientering.
3. Välj en befintlig mall eller utgå från en tom arbetsyta.
4. Ange ett certifikatnamn och ett standardspråk.
5. Lägg till med dra och släpp-redigeraren:
   * Textfält (med alternativ för teckensnitt, färg och placering)
   * Bilder (logotyper, ikoner osv.)
   * Dynamiska fält (elevnamn, instruktörsnamn osv.)
   * Certifikatbakgrunder (heltäckande färg, uppladdad bild eller AI-genererad bild)
6. För AI-genererade bakgrunder: Skriv en uppmaning (till exempel &quot;elever i ett klassrum&quot;) om att generera bakgrunder med AI.

### Lägga till dynamiska fält

Dynamiska fält i anpassade Adobe Learning Manager-certifikat är platshållare som automatiskt fyller i relevant information, t.ex. elevens namn, instruktörens namn eller andra kontospecifika data, när certifikatet skapas. Det möjliggör personliga och kontextmedvetna certifikat utan manuell redigering.

1. Infoga dynamiska variabler som elevnamn, instruktörsnamn eller andra aktiva fält.
2. Fälten fylls i automatiskt när certifikatet utfärdas.

### Flerspråkigt stöd

1. Lägg till nya språk (t.ex. franska, tyska) i certifikatet.
2. Ange översatt text för varje språk.
3. Hantera översättningar och förhandsgranska certifikat på varje språk.

### Förhandsgranska och publicera

1. Använd förhandsgranskningsfunktionen för att se hur certifikatet ser ut för eleverna.
2. Hämta eller skriv ut förhandsgranskningen för granskning.
3. Spara som utkast för att fortsätta redigera senare eller publicera när det är klart.

### Tillämpa certifikat

1. Administratörer kan ange standardcertifikat för kontot.
2. Författare kan bifoga certifikat till specifika förekomster av utbildningsobjekt (kurser, vägar osv.).
3. Välj olika certifikat på instansnivå efter behov.

### Hantera certifikat

1. Visa publicerade certifikat och utkastcertifikat i biblioteket.
2. Redigera, uppdatera eller ta bort mallar efter behov.
3. Certifikat kan återanvändas i flera instanser.

Anpassade certifikat i ALM ger ett flexibelt sätt att designa och utfärda personliga, varumärkta och flerspråkiga certifikat. Funktionen förenklar certifikathanteringen, förbättrar elevigenkänningen och stöder globala krav på efterlevnad och varumärkning.

## Flerspråkigt arbetsstöd

Med hjälp av flerspråkiga arbetsstöd i Adobe Learning Manager (ALM) kan författare och administratörer tillhandahålla stöddokument, guider eller resurser på flera språk i en och samma arbetsstödspost. Elever i olika regioner kan komma åt relevant material på sitt önskade språk, vilket förbättrar tillgänglighet, efterlevnad och användarupplevelse.

### Föregående beteende

Tidigare tillät ALM endast en innehållsfil per arbetsstöd, även om namnet och beskrivningen kunde lokaliseras. För att kunna tillhandahålla samma resurs på flera språk var författarna tvungna att skapa separata arbetsstöd för varje språk. Detta ledde till dubbelarbete, förvirring och ökade administrativa insatser. Det fanns inget enhetligt sätt att hantera flerspråkiga resurser, vilket gjorde det svårt att säkerställa konsekvens och spåra användning.

### Användningsfall

* **Global personalhantering**: Ta fram säkerhetshandböcker, processguider eller referensdokument på flera språk till en mängd olika medarbetare.
* **Regelefterlevnad**: Se till att alla anställda får samma efterlevnadsdokumentation på sitt modersmål.
* **Konsekvent introduktion**: Ange checklistor för nybörjare eller vanliga frågor på lokala språk för nyanställda över hela världen.
* **Minskad duplicering**: Hantera alla språkversioner av ett arbetsstöd i en enda post, vilket förenklar uppdateringar och rapportering.

### Skapa ett flerspråkigt arbetsstöd

1. Gå till rollen Författare och välj **Arbetsstöd**.
2. Välj **Skapa arbetsstöd**.
3. Ange arbetsstödets namn och beskrivning på standardspråket.
4. Överför den primära innehållsfilen eller ange en URL-adress för standardspråket.
5. Spara arbetsstödet.

### Lägg till ytterligare språk

1. I jobbstödsredigeraren väljer du **Lägg till språk**.
2. Välj önskat språk i listan.
3. För varje tillagt språk:
   * Ange det lokaliserade namnet och beskrivningen.
   * Överför motsvarande innehållsfil eller ange en språkspecifik URL.
4. Upprepa för alla obligatoriska språk.

### Redigera och hantera språk

1. Om du vill uppdatera en fil eller en beskrivning för ett visst språk väljer du fliken Språk och gör önskade ändringar.
2. Om ett språk läggs till efter att arbetsstödet har publicerats tilldelas originalfilen automatiskt det nya språket tills en unik fil överförs.
3. Ta bort eller ersätt filer för valfritt språk efter behov.

### Publish och elevupplevelse

1. Publicera arbetsstödet när alla språk och filer har lagts till.
2. Elever ser arbetsstödet på sitt valda innehållsspråk, med rätt fil eller URL.
3. Om en elevs språk inte är tillgängligt visas standardspråkfilen.

### Rapportering

1. Ladda ned jobbstödsrapporter för att visa detaljer om alla filer och språk som är associerade med varje arbetsstöd.
2. Rapporter innehåller språk, filnamn och användningsdata för spårning.

Med flerspråkiga arbetsstöd i ALM kan du leverera stödresurser till en global publik i en enda ingång, minska dubbelarbete och se till att alla elever får rätt information på sitt önskade språk. Med den här funktionen blir Adobe Learning Manager mer tillgängligt, kompatibelt och administrationseffektivt.

## Uppspelningsförbättringar för kurser som genererats av Captivate

Genom uppdateringen förbättras uppspelningsupplevelsen för Adobe Captivate-innehåll i ALM avsevärt genom att ett enhetligt och smidigt gränssnitt introduceras.

ALM-spelaren visar nu en enda konsoliderad innehållsförteckning, döljer Captivate-innehållsförteckningen och visar tydliga indikatorer för slutförande på bildnivå, inklusive gröna skalmarkeringar för att följa utvecklingen.

Systemet förenklar navigering genom att lägga samman modul- och kurskontroller i ett intuitivt fält, vilket minskar elevförvirringen.

Förloppskontrollerna som känner av sammanhanget gör det enklare att använda eftersom förloppsindikatorn bara visas på videobildrutor och bildnavigeringskontrollerna bara på icke-videobildrutor.

Dessutom länkar systemet nu anteckningar till bildnummer i stället för tidsstämplar, vilket säkerställer tillförlitliga PDF-exporter och åtgärdar inkonsekvenser i tidigare format.

## Förbättringar av checklista

### Stöd för checklista på flera språk

Med den här funktionen kan du skapa och hantera checklistmoduler på flera språk. Varje checklista med frågor, instruktioner och utvärderingskriterier kan översättas så att granskare och elever interagerar med checklistan på det språk de föredrar. I systemet visas checklistan på användarens valda innehållsspråk, vilket förbättrar tillgängligheten och efterlevnaden för globala team.

1. Lägg till eller redigera en checklistmodul i kursen.
2. Välj alla språk du vill ha stöd för bland språkalternativen.
3. Ange översättningar för varje fråga, instruktion och utvärderingskriterium för checklistan.
4. Spara ändringarna. Checklistan visas på granskarens eller elevens valda innehållsspråk.
5. Om du lägger till ett nytt språk senare måste du ange översättningar för alla frågor och villkor innan du publicerar.
6. När du hämtar checklisterapporter väljer du önskat språk för att visa rapporten på det språket.

### Checklista för frågeviktning för instruktörsutvärderingar

Med den här funktionen kan du tilldela olika maxpoäng (viktning) för varje checklistefråga. Du kan återspegla den varierande betydelsen eller svårigheten av varje fråga, som stöder mer exakta och meningsfulla utvärderingar. Systemet beräknar den totala poängen baserat på dina indata och avgör om eleven klarar eller misslyckas enligt de kriterier du ställer in.

1. När du lägger till en checklistmodul väljer du **Anpassad poäng**.
2. För varje checklistefråga anger du ett unikt maxvärde som återspeglar dess betydelse.
3. Definiera den övergripande godkända poängen för checklistan.
4. Spara och publicera checklistan.
5. Som instruktör eller granskare utvärderar du varje elev genom att tilldela ett poäng för varje fråga (upp till det maximala antalet du anger).
6. Systemet beräknar den totala poängen och fastställer status för godkänt/underkänt.
7. Hämta checklisterapporter för att visa både uppnådda och maximala poäng för varje fråga samt totala poäng.

### Checklista med kommentarsfunktion för granskare

Med den här funktionen kan granskare lägga till kommentarer eller feedback under utvärderingen av checklistan. Du kan ge personlig och användbar feedback för varje elev. Du kan även välja att visa ditt namn med dina kommentarer för genomskinlighet. Alla kommentarer sparas i elevens betygsutdrag och ingår i checklisterapporter.

1. Aktivera **Granskarkommentarer** när du konfigurerar checklistan.
2. Du kan också aktivera **Visa granskarens namn till eleven** om du vill att ditt namn ska visas med dina kommentarer.
3. Under utvärderingen anger du kommentarer eller feedback för eleven i fältet för angivna kommentarer.
4. Välj om dina kommentarer ska vara synliga för eleven.
5. Skicka in din utvärdering. Om det här alternativet är aktiverat ser eleven dina kommentarer och ditt namn jämte sina resultat.
6. Alla kommentarer sparas i elevens betygsutdrag och inkluderas i checklisterapporter för framtida referens.

## Avancerade sökförbättringar

Den här utgåvan innehåller förbättringar av sökning i innehåll genom att visa kurser med innehåll som matchar fråga högre upp i rang. Arbetsstöd ingår nu också i avancerad sökrankning.

## Motsvarigheter och alternativ

### Översikt

I många organisationer stöter elever på utbildningssituationer där olika kurser lagligen kan uppfylla samma krav?Till exempel när en ny kurs ersätter en äldre, när en mer omfattande kurs kan ersätta en kortare eller när en särskild ersättningskurs behöver erbjudas.

Funktionen Alternate Courses eller Learning Path ger ALM ett formellt sätt att säga:

&quot;Om eleven har slutfört denna utbildning ska denne anses ha uppfyllt det relaterade utbildningskravet.&quot;

Funktionen fungerar i alla kurser och utbildningsvägar och ser till att krav längre fram, som krav på förutsättningar och efterlevnadsregler, uppfylls, och gör detta utan att tvinga eleverna att gå igenom redundant innehåll. Den rapporterar också korrekt genom att registrera vad som slutfördes direkt jämfört med vad som var nöjd via ett alternativ.

I kärnan introducerar funktionen konceptet för ett alternativt slutförande: ett speciellt slutförandetillstånd som skapas automatiskt när en elev slutför en konfigurerad källutbildning som räknas mot ett annat målutbildningsmål.

### Ekvivalens med alternativ

Vissa utbildningsrelationer är dubbelriktade, vilket innebär att varje kurs kan tillfredsställa den andras krav. Detta är i själva verket ett scenario där två utbildningar behandlas som ömsesidigt utbytbara. Enkelriktade förhållanden gör det däremot möjligt för en utbildning att uppfylla kravet på en annan, men inte tvärtom. ALM modellerar båda scenarierna med samma underliggande alternativ*slutförandemekanism.

* **Dubbelriktad relation:** Slutförande av någon av utbildningarna uppfyller kraven för den andra.
* **Enkelriktad relation:** Utbildning A uppfyller utbildning B, men A räcker inte för att slutföra B. Detta är vanligt när en nyare eller mer omfattande version bör räknas in i ett äldre krav, men inte tvärtom.

Alternativa tecken används oftast i **enkelriktade** scenarier?Till exempel när en mer omfattande supermängdskurs täcker allt i en enklare delmängdskurs. Slutförande av delmängden bör uppfylla kravet för delmängden, men inte nödvändigtvis tvärtom.

* En nyare, utökad kurs som bör räknas till ett äldre krav.
* En kurs som utformats för en specifik målgrupp (t.ex. en regional eller tillgänglighetsanpassad variant) som fortfarande uppfyller samma krav som grundkursen.
* En förbättrad ny version av en kurs som organisationen vill räkna för ett äldre krav, men den äldre versionen ska inte räknas för det nya kravet.

I alternativa tecken är relationen normalt **en*väg**. Om kurs A är ett alternativ till kurs B kan ett ifyllande av A uppfylla B:s krav, men att slutföra B uppfyller inte nödvändigtvis A.

Både ekvivalens och alternativsystem delar samma underliggande mekanism i ALM: när en konfigurerad källutbildning är slutförd, ger ALM automatiskt ett alternativt resultat för en eller flera målutbildningar.

### Vilka problem löser man med detta?

Utan suppleanter och likvärdighet står administratörer och elever inför flera återkommande problem:

* Elever ombeds ofta att repetera kurser som täcker innehåll som de redan har slutfört i en annan version eller ett annat format.
* Det är enklare att uppdatera kompatibilitetsprogram eftersom administratörer kan ersätta eller omstrukturera utbildningar utan att elever som har slutfört äldre versioner måste ta tillbaka motsvarande eller ersatt innehåll.
* Logiken som krävs är stel. Om en utbildningsväg förutsätter en viss kurs finns det inget rent sätt att erkänna att en annan utbildning är tillräckligt bra.
* Rapportering och revision är svårare. Det finns ingen formell signal som visar att ett krav uppfylldes genom ett alternativt slutförande och inget enkelt sätt att spåra källan till krediten.

Funktionen Alternativ och ekvivalens åtgärdar dessa problem genom att:

* Förhindra dubbelarbete för elever när ersättare är giltiga.
* Tillåta administratörer att ändra utbildningsstrukturer (till exempel byta en kurs i en bana) utan att bryta slutföranden för elever som tog den tidigare versionen.
* Att tillåta krav och efterlevnadskontroller som respekterar både direkta slutföranden och alternativa eller likvärdiga slutföranden.
* I utskrifter och rapporter tydligt anteckna om en utbildning har fullgjorts direkt eller fullgjorts genom ett alternativt förhållande, tillsammans med vilket utbildningen tjänade som källa.

### Så här fungerar funktionen begreppsmässigt

Funktionen bygger på tre huvudidéer: **relationer**, **alternativa slutföranden** och **nedströmsbeteenden**.

#### Relationer mellan utbildningar

Administratörer definierar relationer mellan kurser och utbildningsvägar. För varje relation väljer de en **källa** och ett eller flera **mål**. En enskild kurs kan ha upp till 30 mål beroende på hur många tidigare eller relaterade utbildningar den bör uppfylla.

För ekvivalens kan administratörer göra relationen **dubbelriktad** om de vill att båda utbildningarna ska tillfredsställa varandra. För suppleanter behåller administratörer normalt riktningen ett * sätt för att återspegla att endast vissa ersättningar är tillåtna.

Dessa relationer lagras på utbildningsnivå, inte på elevnivå. När de har konfigurerats och aktiverats gäller de för alla aktuella och framtida slutföranden av källutbildningen, med förbehåll för inställningar på kontonivå, till exempel om retroaktivt slutförande är aktiverat.

### Alternativ slutförande

När en elev slutför en källutbildning granskar ALM alla konfigurerade alternativa eller likvärdiga relationer och skapar för varje relevant målutbildning en **alternerande slutförandepost**. Den här posten skiljer sig från ett normalt slutförande:

* Det markerar målutbildningen för eleven men håller koll på att den slutfördes via alternativ eller likvärdighet snarare än direkt.
* Den registrerar vilken källutbildning som användes för att uppfylla målet.
* Den lagras i en särskild struktur så att rapporter kan skilja mellan direkta och alternativa slutföranden.

Elever kommer att se alternativ slutföring även om de inte är registrerade. Elevens betygsrapport (LT) innehåller endast poster med utbildningar som eleven har registrerat sig för.

### Elevens appupplevelse för alternativa och likvärdiga slutföranden

Alternativa och likvärdiga slutföranden visas tydligt i elevappen så att eleverna tydligt kan förstå hur ett utbildningskrav uppfylldes, samtidigt som konsekvensen med utskrifter och rapporter bibehålls.

#### LO-kortbeteende

#### Alternativ slutförandestatus

När en elev slutför en utbildning via en alternativ eller motsvarande relation visas en särskild status för kortet Utbildningsobjekt (LO), till exempel **Slutfört via Alternativ**.\
Den här visuella skillnaden hjälper elever att skilja mellan direkta slutföranden och slutföranden som beviljas genom konfigurerade relationer.

#### Indikator för slutförandemetod

LO-kortet innehåller en indikator för slutförandemetod (till exempel en etikett eller ikon) som visar att slutförandet skedde via ett **alternativ**.\
Om en alternativ slutföring senare återkallas på grund av ändringar, t.ex. retroaktiv slutföring eller borttagning av källutbildningen, uppdateras LO-kortet med **Alternativ (återkallat)**.

#### Insyn och revisionsdetaljer

Elever kan öppna LO-kortet för att se ytterligare information, bland annat:

* Källkursen eller utbildningsvägen som gav det alternativa slutförandet
* Slutförandedatum som är kopplat till källutbildningen

Detta garanterar öppenhet och stöder revisioner och efterlevnadskontroller.

#### Filtrera och visa

#### Filter för slutförandemetod

Elevappen har ett filter som gör att eleverna kan skilja mellan:

* **Direkta** slutföranden
* **Alternativa slutföranden**
* **Alla** slutföranden

Detta gör det möjligt för elever att snabbt förstå hur deras utbildningskrav uppfylldes.

#### Betygsutskrifts- och framstegsvyer

Filtret för slutförandemetod är tillgängligt i vyer vända mot elever, som:

* Utbildningsutskrifter
* Spårningsavsnitt för status och slutförande

Dessa synpunkter visar tydligt vilka utbildningar som fullgjorts direkt och vilka som fullgjorts genom alternativa lösningar eller likvärdighet.

#### Rapporteringsjustering

Filtreringslogiken i elevappen justeras mot kolumnen **Slutförandemetod** som används i rapporter.\
Detta garanterar konsekvens mellan vad elever ser i användargränssnittet och vad administratörer ser i exporter och efterlevnadsrapporter.

#### Slut *på* flödet

#### För elever

1. Gå till **Min utbildning** eller **Slutförda kurser** i elevappen.
2. Granska LO-kort för att identifiera utbildningar markerade som **Slutförda via Alternativ**.
3. Öppna ett LO-kort för att se information om källans utbildnings- och slutförandedatum.
4. Använd filtermenyn i transkriberings- eller kurslistvyer för att välja **Direkt**, **Alternativ** eller **Alla**.
5. Granska den uppdaterade listan baserat på den valda slutförandemetoden.

#### För administratörer och författare

1. Konfigurera likvärdiga eller alternativa relationer mellan kurser eller utbildningsvägar i administratörsgränssnittet.
2. Kontrollera att alternativa slutföranden återspeglas korrekt på LO-kort och i filter som vänder sig till eleven*.
3. Använd elevvyer och elevrapporter för att bekräfta konsekvens mellan användargränssnittsdata och exporterade data.
4. Om en källutbildning har fasats ut eller tagits bort validerar du att de aktuella LO-korten har uppdaterats (visar till exempel **Alternativ (återkallat)** i tillämpliga fall).

## Retroaktivt slutförande och slutförande

ALM stöder retroaktiv slutföring och retroaktiv inslutförande för att säkerställa att alternativa och likvärdiga relationer förblir korrekta över tid, även när relationer skapas, ändras eller tas bort efter att elever redan har slutfört utbildningen.

### Retroaktivt slutförande

#### Definition

När retroaktiv slutföring är aktiverad får elever som har slutfört en källkurs automatiskt en alternativ slutföring av målkursen om en motsvarande eller alternativ relation skapas senare.\
Detta säkerställer att det historiska lärandet infrias utan att eleverna behöver genomgå utbildningen på nytt.

#### Så här fungerar det

1. En administratör möjliggör retroaktiv slutförande på kontonivå.
2. Administratören definierar en motsvarande eller alternativ relation mellan en käll- och målutbildning.
3. Systemet söker igenom historiska slutförandeposter för källutbildningen.
4. Berättigade elever ges alternativt slutförande av målutbildningen.
5. Dessa poster visas som **slutförda via alternativa** i elevens utskrifter och rapporter.

### Retroaktiv slutförande

#### Definition

När retroaktiv slutförande är aktiverat återkallas alternativa slutföranden om den underliggande motsvarande eller alternativa relationen tas bort eller om källutbildningen tas bort.\
Detta säkerställer att systemet återspeglar aktuella och giltiga utbildningsrelationer.

#### Så här fungerar det

1. En administratör möjliggör retroaktiv slutförande på kontonivå.
2. Administratören tar bort en alternativ eller motsvarande relation eller tar bort källutbildningen.
3. Systemet identifierar elever som har fått alternativt slutförande via den berörda relationen.
4. Motsvarande alternativa slutförandeposter återkallas.
5. Återkallade poster markeras som **Alternativa (återkallade)** i utskrifter och rapporter för granskningssynlighet.

### Inverkan på förutsättningarna

Alternativa slutföranden, inklusive sådana som beviljas retroaktivt, behandlas som giltiga slutföranden vid bedömning av förutsättningar.\
Om en elev har **slutfört via Alternativ** kan hen fortsätta med kurser som kräver målutbildningen.

Om ett alternativt slutförande senare återkallas genom ett retroaktivt slutförande kan eleven förlora rätten till kurser som var beroende av det kravet.

### Inverkan på utbildningsvägar och certifieringar

Alternativa slutföranden bidrar till framsteg och slutförande av utbildningsvägar och certifieringar.\
Elever kan gå vidare eller slutföra dessa program när obligatoriska utbildningar har uppfyllts via alternativa eller likvärdiga relationer.

Om ett alternativt slutförande återkallas kan de berörda utbildningsvägarna eller certifieringarna förlora status för förlopp eller slutförande tills kravet är uppfyllt genom ett giltigt slutförande.

### Avsluta *till* arbetsflödet

#### Aktivera retroaktivt slutförande eller slutförande

1. Administratörer navigerar till kontoinställningar och aktiverar retroaktiv slutföring och/eller retroaktiv slutföring.
2. Administratörer skapar, ändrar eller tar bort motsvarande eller alternativa relationer mellan utbildningar.

#### Systemåtgärder

* **För retroaktiv slutföring:**\
  Systemet tillåter alternativa slutföranden baserat på tidigare slutföranden av källor.
* **För retroaktiv slutföring:**\
  Systemet återkallar alternativa slutföranden när relationer tas bort eller källutbildningar raderas.

#### Elevupplevelse

Elever ser uppdaterade slutförandestatusar på LO-kort och i utskrifter, som:

* **Slutfört via alternativ**
* **Alternativ (återkallat)**

Kontroller av förutsättningar, förlopp för utbildningsväg och uppdatering av certifieringsstatus dynamiskt baserat på det aktuella slutförandetillståndet.

#### Rapportering och revision

Alla retroaktiva ändringar återspeglas i rapporten Utbildningsbevis (LT).\
Rapporter skiljer tydligt mellan direkta slutföranden, alternativa slutföranden och återkallade alternativa slutföranden till stöd för efterlevnad, supportutredningar och revisioner.

### Retroaktivt slutförande och slutförande

ALM stöder retroaktiv slutföring och retroaktiv inslutförande för att säkerställa att alternativa och likvärdiga relationer förblir korrekta över tid, även när relationer skapas, ändras eller tas bort efter att elever redan har slutfört utbildningen.

#### Retroaktivt slutförande

#### Definition

När retroaktiv slutföring är aktiverad får elever som har slutfört en källkurs automatiskt en alternativ slutföring av målkursen om en motsvarande eller alternativ relation skapas senare.\
Detta säkerställer att det historiska lärandet infrias utan att eleverna behöver genomgå utbildningen på nytt.

#### Så här fungerar det

1. En administratör möjliggör retroaktiv slutförande på kontonivå.
2. Administratören definierar en motsvarande eller alternativ relation mellan en käll- och målutbildning.
3. Systemet söker igenom historiska slutförandeposter för källutbildningen.
4. Berättigade elever ges alternativt slutförande av målutbildningen.
5. Dessa poster visas som **slutförda via alternativa** i elevens utskrifter och rapporter.

#### Retroaktiv slutförande

#### Definition

När retroaktiv slutförande är aktiverat återkallas alternativa slutföranden om den underliggande motsvarande eller alternativa relationen tas bort eller om källutbildningen tas bort.\
Detta säkerställer att systemet återspeglar aktuella och giltiga utbildningsrelationer.

#### Så här fungerar det

1. En administratör möjliggör retroaktiv slutförande på kontonivå.
2. Administratören tar bort en alternativ eller motsvarande relation eller tar bort källutbildningen.
3. Systemet identifierar elever som har fått alternativt slutförande via den berörda relationen.
4. Motsvarande alternativa slutförandeposter återkallas.
5. Återkallade poster markeras som **Alternativa (återkallade)** i utskrifter och rapporter för granskningssynlighet.

#### Inverkan på förutsättningarna

Alternativa slutföranden, inklusive sådana som beviljas retroaktivt, behandlas som giltiga slutföranden vid bedömning av förutsättningar.\
Om en elev har **slutfört via Alternativ** kan hen fortsätta med kurser som kräver målutbildningen.

Om ett alternativt slutförande senare återkallas genom ett retroaktivt slutförande kan eleven förlora rätten till kurser som var beroende av det kravet.

#### Inverkan på utbildningsvägar och certifieringar

Alternativa slutföranden bidrar till framsteg och slutförande av utbildningsvägar och certifieringar.\
Elever kan gå vidare eller slutföra dessa program när obligatoriska utbildningar har uppfyllts via alternativa eller likvärdiga relationer.

Om ett alternativt slutförande återkallas kan de berörda utbildningsvägarna eller certifieringarna förlora status för förlopp eller slutförande tills kravet är uppfyllt genom ett giltigt slutförande.

#### Avsluta *till* arbetsflödet

#### Aktivera retroaktivt slutförande eller slutförande

1. Administratörer navigerar till kontoinställningar och aktiverar retroaktiv slutföring och/eller retroaktiv slutföring.
2. Administratörer skapar, ändrar eller tar bort motsvarande eller alternativa relationer mellan utbildningar.

#### Systemåtgärder

* **För retroaktiv slutföring:**\
  Systemet tillåter alternativa slutföranden baserat på tidigare slutföranden av källor.
* **För retroaktiv slutföring:**\
  Systemet återkallar alternativa slutföranden när relationer tas bort eller källutbildningar raderas.

#### Elevupplevelse

Elever ser uppdaterade slutförandestatusar på LO-kort och i utskrifter, som:

* **Slutfört via alternativ**
* **Alternativ (återkallat)**

Kontroller av förutsättningar, förlopp för utbildningsväg och uppdatering av certifieringsstatus dynamiskt baserat på det aktuella slutförandetillståndet.

#### Rapportering och revision

Alla retroaktiva ändringar återspeglas i rapporten Utbildningsbevis (LT).\
Rapporter skiljer tydligt mellan direkta slutföranden, alternativa slutföranden och återkallade alternativa slutföranden till stöd för efterlevnad, supportutredningar och revisioner.

### Webhookar för motsvarigheter och alternativ

ALM tillhandahåller dedikerade webhook-händelser för likvärdiga och alternativa slutföranden för att stödja automatisering, integrationer och synkronisering med externa system.

Dessa händelser gör det möjligt för externa konsumenter att på ett tillförlitligt sätt skilja mellan direkta slutföranden och slutföranden som beviljas genom alternativa eller likvärdiga förhållanden.

#### Översikt

När en elev slutför en kurs via ett alternativt eller motsvarande förhållande, utlöser ALM en webhook-händelse som är separat från standardwebhooken för slutförande av kurs.\
Detta garanterar att integreringar kan svara olika på olika kompletteringar där så behövs.

Webhook-händelser utlöses också när retroaktiv slutföring eller retroaktiv inslutförande sker, vilket omfattar historiska uppdateringar samt relationsändringar.

#### Beteende för webhook-händelse

* En distinkt webhook-händelse utlöses när en elev får statusen **Slutförd via Alternativ** för en målkurs.
* Händelsen genereras när eleven slutför en konfigurerad källkurs som uppfyller målet genom en likvärdig eller alternativ relation.
* Denna webhook utlöses inte för slutförande av direktkurs.
* När retroaktiv slutförande eller retroaktiv inslutförande är aktiverat, genereras webhook-händelser för varje berörd elev och målkurs.

#### Information om nyttolast för webhook

Nyttolasten för en webhook för alternativ slutförande innehåller följande nyckelattribut:

* **Elevens ID**\
  Identifierar den elev som fick det alternativa slutförandet.

* **Källkurs**\
  Kursen eller utbildningsvägen som eleven slutförde direkt.

* **Målkurs**\
  Kursen som markeras som slutförd via det alternativa eller likvärdiga förhållandet.

* **Slutförandemetod**\
  Anger att slutförandemetoden är **alternativ**.

* **Slutförandedatum**\
  Härledd från slutförandedatumet för källkursen.

* **Relationstyp**\
  Anger om relationen är **likvärdig** eller **alternativ**.

I retroaktiva slutförandescenarier indikerar webhook-händelser att en befintlig alternativ slutföring har återkallats.

#### Integreringsöverväganden

Externa system kan använda dessa webhook-händelser för att:

* Uppdatera elevposter
* Synkronisera slutförandestatus
* Utlösa meddelanden eller underordnade arbetsflöden
* Underhåll granskningsspår för efterlevnadssyften

Webhook-användare bör uttryckligen skilja mellan **direkta** och **alternativa** slutföranden.\
Alternativa avslutningar ger inte färdigheter, utmärkelsetecken eller spelifieringsersättning och bör hanteras därefter i nedströmssystem.

### Effekten av att lägga ned och ta bort källutbildning i motsvarigheter och alternativ

Livscykeltillståndet för en källutbildning (indragen eller borttagen) påverkar direkt hur alternativa och likvärdiga slutföranden bevaras för elever. ALM hanterar dessa scenarier på olika sätt för att bevara den historiska noggrannheten samtidigt som de aktuella relationerna förblir giltiga.

#### Källutbildning läggs ned

##### Definition

Vid utfasning av en kurs är den inte längre tillgänglig för nya registreringar samtidigt som den finns kvar i systemet för tidigare referens-, rapporterings- och revisionsändamål.

##### Påverkan

* Befintliga alternativa slutföranden som har beviljats genom den utfasade källkursen är fortfarande giltiga.
* Elever som tidigare har slutfört källkursen fortsätter att ha alternativ slutförande för målkursen.
* Inga nya alternativa slutföranden genereras från den utfasade kursen, eftersom den inte kan slutföras av nya elever.
* Elevens utskrifter och rapporter fortsätter att visa **Slutförda via alternativa** för berörda elever.

#### Radera källutbildning

#### Definition

När du tar bort en kurs tas den bort helt från systemet, inklusive slutförandeposter och konfigurerade relationer.

#### Påverkan

* Om retroaktiv slutförande är aktiverat återkallas alla alternativa slutföranden som beviljats via kursen för borttagen källa.
* Elevens betygsutdrag och rapporter uppdateras för att visa **Alternativa (återkallade)** för granskning och efterlevnadssynlighet.
* Elever kan förlora status framsteg eller slutförande i utbildningsvägar, certifieringar eller förutsättningar som var beroende av den återkallade alternativa slutförandet.
* Inga ytterligare alternativa slutföranden kan beviljas från kursen som tagits bort.

#### Arbetsflöde

1. En administratör tar bort eller tar bort källkursen med administratörsgränssnittet.
2. Systemet utvärderar alla alternativa och likvärdiga slutföranden som härleds från källkursen.
3. Slutförandestatus uppdateras baserat på kursens tillstånd:
   * **Utfasade:** Befintliga alternativa slutföranden förblir oförändrade.
   * **Borttaget:** Alternativa slutföranden återkallas om retroaktiv inslutförande aktiveras.
4. Elevens utskrifter och rapporter återspeglar den uppdaterade statusen för att stödja efterlevnad och revisionskrav.

### Ingen länkning av relationer

ALM stöder inte länkning av alternativa eller likvärdiga relationer. Alternativa slutföranden beviljas endast för direkt konfigurerade relationer och överlappas inte av flera nivåer av kurser.

#### Koncept: ingen länkning av relationer

#### Definition

Kedjning innebär att tillåta alternativa eller likvärdiga relationer att sprida sig över flera kurser.\
Om till exempel kurs A är ett alternativ till kurs B, och kurs B är ett alternativ till kurs C, innebär kedjning att slutföra kurs A ger bidrag till kurs C.

#### integritetspolicy

Kedjning stöds inte.\
Alternativa och likvärdiga relationer utvärderas bara på en enda nivå. När du slutför en källkurs beviljas alternativt slutförande endast till dess omedelbara målkurs eller målkurser, inte till några mål nedströms.

#### Arbetsflöde

#### Relationsinställningar

En administratör definierar alternativa eller likvärdiga relationer mellan kurser, till exempel:

* Kurs A → kurs B
* Kurs B → kurs C

#### Slutförandehändelse

En elev slutför kurs A direkt.

#### Systemåtgärd

* Systemet beviljar alternativt slutförande för kurs B om förhållandet A → B är definierat.
* Systemet beviljar inte alternativt slutförande för kurs C, även om det finns en B- → C-relation.

#### Krav för direkt slutförande

För att få alternativ slutföring av kurs C måste eleven:

* Genomför kurs B direkt, eller
* Slutför en kurs som uttryckligen är konfigurerad som ett direkt alternativ till eller motsvarande för kurs C.

### Konsekvenser

#### Inga indirekta fördelar

Elever kan inte få tillgodoräknande om slutförande av kurser längre ned i en relationskedja om inte varje kurs (eller dess direkta alternativ) har slutförts.\
Detta garanterar att utbildningskraven uppfylls på ett tydligt och förutsägbart sätt.

#### Förenklad granskning och rapportering

Rapporter och elevutskrifter visar endast alternativa slutföranden för direkta relationer.\
På så sätt undviker man komplexa granskningsspår i flera steg och skapar klarhet när man granskar hur ett slutförande har beviljats.

### Katalogdelning med kollegiala konton: relationer delas inte

Katalogdelning gör att utbildningsobjekt (LO:er) kan delas mellan kollegiala konton, men alternativa och likvärdiga relationer hanteras oberoende inom varje konto och delas inte.

#### Koncept: katalogdelning och relationer

#### Katalogdelning

Konton kan dela kataloger med kollegiala konton för att ge åtkomst till kurser, utbildningsvägar och andra utbildningsobjekt i alla konton.

#### Relationer delas inte

Alternativa, ekvivalenta och alternerande slutföranderelationer som konfigurerats i källkontot delas inte och replikeras inte när en katalog delas.\
Varje konto underhåller och utvärderar sina egna relationer oberoende av varandra.

### Arbetsflöde

#### Katalogdelning

En administratör i **Konto A** delar en katalog som innehåller utbildningsobjekt med **Konto B**.

#### Relationskonfiguration

Konto A kan ha alternativa eller likvärdiga relationer definierade bland utbildningsobjekten i den delade katalogen.

#### Kollegial kontoåtkomst

Konto B får åtkomst till de delade utbildningsobjekten men ärver inte några alternativa eller likvärdiga relationer som konfigurerats i konto A.

#### Oberoende ledning

Om konto B kräver liknande alternativt eller likvärdigt beteende måste en administratör i konto B manuellt konfigurera relationerna inom det kontot.

#### Konsekvenser

#### Ingen automatisk relationsspridning

Alternativa och likvärdiga relationer är inte automatiskt tillgängliga i kollegiala konton genom katalogdelning.

#### Manuell konfiguration krävs

Varje kollegialt konto ansvarar för att definiera och hantera sina egna relationer för delade utbildningsobjekt.

#### Överensstämmelseöverväganden

Slutförande, uppfyllelse av förutsättningar och rapportering kan skilja sig åt mellan olika konton såvida inte relationerna avsiktligt bringas i linje genom manuell konfiguration.


### Nedströmsbeteende

När det finns en alternativ slutförd utbildning använder ALM den i nedströmskontroller:

* Om målutbildningen är en **förutsättning** för andra utbildningar blir eleven berättigad till dessa utbildningar som om hen hade slutfört målet.
* Om målet är en **obligatorisk kurs i en utbildningsväg** kan sökvägens slutförandelogik behandla eleven som att ha slutfört den delen och fortsätta för att markera banan som slutförd när andra villkor är uppfyllda.
* Efterlevnadstavlor och andra instrumentpaneler, till exempel en kontrollpanel för gruppframgång som är beroende av om ett utbildningskrav uppfylls, kan inkludera elever som bara har alternativa slutföranden.

Systemet skiljer mellan faktisk slutföring och alternerande slutförande så att

* Om eleven senare slutför målutbildningen direkt och slutför den, kan detta direkta slutförande åsidosätta behovet av alternativt slutförande.
* Om relationen mellan källa och mål tas bort eller ändras kan ALM ta bort eller justera de alternativa slutförandena utan att röra äkta slutföranden, förutsatt att retroaktiva slutföranden är aktiverade för kontot.

Alternativa avslut är utformade så att de inte stör den faktiska elevaktiviteten på målutbildningen. De fungerar som ett överlägg som kan revideras om relationerna förändras.