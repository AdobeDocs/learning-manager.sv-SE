---
title: Nyheter i Adobe Learning Manager-versionen från april 2026
description: Läs om de nya funktionerna, förbättringarna och viktiga uppdateringar i Adobe Learning Manager i april 2026-versionen.
exl-id: 4d2129c4-42d8-446f-8837-879b5c2f42bf
source-git-commit: 48a20033896a9d9f370c2e53bce353a886b05e35
workflow-type: tm+mt
source-wordcount: '7400'
ht-degree: 0%

---

# Kommande ändringar i Adobe Learning Manager

<!-- >>[!IMPORTANT]
>
>The Adobe Learning Manager October 2025 release is now live. View [What's New](/help/migrated/whats-new.md) for more information on the latest features and enhancements. This page will be updated with the new features and enhancements for the next release. Stay tuned for more updates. -->

## Översikt över versionen

I april 2026-versionen av Adobe Learning Manager introduceras en rad förbättringar som gör inlärningen smidigare för elever, enklare att hantera för administratörer och mer flexibel för instruktörer, inklusive tydligare navigering i Fluidic Player med etiketten &quot;Nästa modul&quot; och en särskild avgångsknapp, stöd för flera samtidiga zoomsessioner så att team kan köra parallella virtuella klasser utan manuell konfiguration och bättre synlighet för delade kurser genom att visa den verkliga författaren i stället för &quot;Extern&quot; Författare&quot; i kollegiala konton. Uppdateringen visar också utgångsdatum för utbildningsobjekt i elev-API:er för att hjälpa LXP:er att markera tidskänsliga utbildningar, lägger till stöd för flera språk för arbetsstöd så att ett arbetsstöd kan bära alla språkversioner och låter administratörer begränsa när moduler kan startas genom att definiera start-/slutfönster som är användbara för kohorter eller tidsinställda program.

Externa system som använder LTI kan nu ange spelarspråket automatiskt, vilket ger eleverna en konsekvent språkupplevelse på olika plattformar. Flera checklista uppgraderingar anländer också, inklusive viktade poäng, flerspråkig frågetext och valfria granskningskommentarer för rikare feedback. ALM fångar nu flera quiz-försök som kontrolleras i SCORM-innehåll och rapporterar varje försök i L2-rapportering. Instruktörer kan också själva generera QR-koder för omedelbar registrering och närvarospårning under personliga sessioner, och Captivate-innehåll spelas upp tydligare med en enhetlig innehållsförteckning, slutförandebockar på bildrutenivå och tillförlitliga anteckningsexporter. Generellt sett fokuserar utgåvan på tydlighet, konsekvens, flerspråkig beredskap, effektivitet i administratörers arbete och mer flexibel leverans av utbildning.

## Fluidic Player-navigering - visa namnet på nästa modul

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

Spelarens förhandsgranskning i Admin > Varumärke återspeglar nu den nya etiketten, t.ex. Nästa modul: Lektion 2. Detta gör att administratörer kan se det uppdaterade navigeringsbeteendet.

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

Den kommande uppgraderingen till Zoom Connector förbättrar avsevärt hur Adobe Learning Manager hanterar Virtual Instructor-Led Training (VILT). Tidigare kunde användarna bara skapa en zoomsession i taget. Med den nya uppdateringen kan administratörer och författare schemalägga flera zoomsessioner samtidigt med hjälp av standardintegrering.

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

* Organisationer kan använda sin befintliga zoomallokeringsmodell (ett konto per tränare, per affärsenhet osv.) samtidigt som de integrerar helt med Adobe Learning Manager.

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

* Elevupplevelsen är i linje med förväntningarna från det primära kontot (till exempel att se &quot;Cloud Academy Team&quot; i stället för &quot;Extern författare&quot;).

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

## Begränsa när moduler kan startas

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

* **Kohortbaserat aktiveringsprogram**: I det här programmet låses en ny modul upp varje vecka. Innehållet för Vecka 1 är tillgängligt direkt, medan Vecka 2 är synlig men kan inte startas förrän ett visst datum. Vecka 3 följer samma grindningsprocess. Elever kan se hela utbildningsvägen, men systemet styr när de faktiskt kan påbörja varje steg.

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

* Alla moduler som riktar sig till elever (SCORM, PDF, HTML osv.) kan finnas på flera innehållsspråk så att eleverna kan välja vilket språk de föredrar.

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

   * Kursöversikten och modulvyn visar inte en LMS-omförsöksknapp för den modulen.

   * Försökshantering (till exempel försök i frågeformuläret) styrs av själva innehållet.

#### Rapportering

L2-quizrapporten uppdateras för att behandla varje försök på innehållsnivå som en separat försöksrad:

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

Den exporterade QR-koden PDF kommer att innehålla:

* Kursnamn

* Instansnamn

* Sessionsnamn

Dessa gör det enkelt för instruktörer och samordnare att identifiera och skriva ut rätt QR-kod för varje session.

### Viktiga fördelar

* **Instruktörsautonomi**: Instruktörer behöver inte längre vänta på att administratörer ska skapa QR-koder. De kan generera dem direkt för varje session, förbättra smidigheten och minska de allmänna kostnaderna för samordningen.

* **Bättre klassrumslogistik**: Instruktörer kan hantera registrering och närvaro på plats med hjälp av QR-koder om de är på promenad eller på plats (t.ex. fältarbetare, personal på verkstadsgolvet eller externa deltagare).

* **Minskad administrativ arbetsbelastning**: Administratörsteam kan fokusera på konfiguration och styrning i stället för att hantera rutinmässiga begäranden om generering av QR-kod för varje session.

### Användningsfall

* Organisationer som kör stora volymer sessioner på plats (till exempel produktutbildning för proffs) kan ge instruktörer möjlighet att skriva ut sessionsspecifika QR-koder som registrerar och markerar närvaro med en skanning.

* Inom detaljhandels-, tillverknings- och hälsovårdsutbildning, där elever ofta deltar i sessioner direkt från golvet eller utan förregistrering, kan en QR-kod (&quot;Enroll + Attendance&quot;) läggas vid dörren. Detta gör det möjligt för elever att själva betjäna sin registrering och närvaro via sina telefoner.

* Utbildningshändelser för partners eller kunder gör att utbildaren på plats enkelt kan anpassa sig till förändringar i rummet, ytterligare sessioner eller extra deltagare utan att behöva rådfråga administratören om nya QR-koder.

## Förbättringar av Captivate och ALM-spelare

### Översikt

Den här förbättringen förbättrar upplevelsen av att spela upp Adobe Captivate-innehåll i Adobe Learning Manager-spelaren (ALM), särskilt efter de senaste förändringarna i Captivate arkitektur. Syftet är att göra det möjligt för elever att interagera med Captivate-moduler i ALM och samtidigt säkerställa att navigering, slutförandespårning och anteckning är tydliga, konsekventa och tillförlitliga.

### Nyheter

#### Enhetlig upplevelse av innehållsförteckningen

* Endast ALM-innehållet visas på spelarens vänstra sida.

* Captivate egen TOC döljs när modulen spelas upp i ALM.

* Detta eliminerar dubbletter, säkerställer en enda sanningskälla för navigering och frigör skärmytor.

#### Feedback om visuellt slutförande

* ALM-innehållsförteckningen visar gröna skalmarkeringar (eller motsvarande visuella ledtrådar) som indikerar slutförande på bildrutenivå.

* I takt med att eleverna går vidare genom diabilderna i Captivate visar ALM-TOC vilka diabilder som har slutförts, i linje med elevens förväntningar på moderna kursspelare.

#### Sammanhangsberoende förloppskontroller

* Spelarkontrollerna anpassar sig efter bildtyp:

   * För videobildrutor:

      * Visa en tidsförloppsindikator som återspeglar videouppspelningen.

* För icke-videobilder:

   * Visa sidnavigeringskontroller (nästa/föregående bild osv.) i stället för en icke-fungerande tidsrad.

      * På så sätt undviker du att visa irrelevanta eller icke-fungerande kontroller på vissa bildtyper.

#### Förenklad navigering

* Det separata modulnavigeringsfältet (ALM) och kursnavigeringsfältet kommer att slås samman till ett enda, intuitivt fält.

* Den här enhetliga navigeringen:

   * Skiljer sig tydligt från att gå genom modulen Captivate jämfört med att gå tillbaka till kurs-/modulnivå.

   * Minskar förvirring orsakad av flera staplar med överlappande syften.

#### Länkning av tillförlitliga anteckningar

* Anteckningar länkas till bildnummer i stället för tidsstämplar.

* Den här ändringen:

   * Korrigerar exportfel som orsakas av saknade eller felaktiga tidsstämplar.

   * Gör att anteckningar kan exporteras på ett enhetligt sätt som PDF, med en tillförlitlig mappning mellan anteckningar och det bildsammanhang som de tillhör.

### Viktiga fördelar

* Renare upplevelse för en spelare: Eleverna interagerar med en TOC och en navigeringsmodell vilket minskar förvirringen och den kognitiva belastningen.

* Exakta angivelser av slutförande och förlopp: Skjutmarkeringar och sammanhangsberoende kontroller hjälper elever att förstå var de är och vad som finns kvar.

* Mer robust anteckning och export: Genom att koppla anteckningar till bilder i stället för sköra tidsstämplar återfår användarna ett tillförlitligt arbetsflöde från anteckningar till PDF, även med bildbaserat Captivate-innehåll.

* Bevarat arbetsflöde för författare: Författarna behåller enkelheten i Captivate direktpublicering till ALM, medan eleverna får en modern, integrerad uppspelningsupplevelse utan extra redigeringsbördor.

### Användningsfall

* Aktiveringsprogram som använder Captivate för interaktiva simuleringar kan distribuera innehåll i ALM, vilket säkerställer att navigering, spårning av slutföranden och anteckningar fungerar konsekvent för elever.

* Organisationer som använder Captivate som sitt huvudsakliga verktyg för innehållsredigering kan upprätthålla publicering med ett klick och undvika att blanda ihop dubbla innehållsförteckningar och icke-funktionskontroller för elever.

* Organisationer som använder anteckningar som exporterats från Captivate-innehåll i ALM (för coaching, compliance eller record) kan komma åt följande:

   * Anteckningar länkar korrekt till bilder.

   * PDF genereras som förväntat.

## Ändringar i elevens betygsutdrag

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

### Sammanfattningstabell

| **Modultyp** | **Aktiv tid (räknad)** | **Inaktiv tid (utesluten)** |
| --- | --- | --- |
| **Video/ljud** | Uppspelningstid | Inte påbörjad; avslutad; pausad **\>10 min** |
| **Statisk (PDF/PPT/DOC)** | Fliken aktiv **och** aktivitet under de senaste **10 minuterna** | Ingen aktivitet **\>10 min**; fliken är inaktiv |
| **SCORM** | Tid rapporterad efter innehållskörning | Det går inte att identifiera inaktivitet |
| **Captivate** | Bildbaserad tidsinställning | Det går inte att identifiera inaktivitet |
| **xAPI** | Fliken är aktiv | Inaktiv flik |
| **HTML** | Spelarens öppningstid med en flik aktiv | Inaktiv flik |
| **LTI Producer/Consumer** | Om LTI-innehåll spelas i ALM:s spelare (dvs. ALM konsumerar LTI-innehåll som finns på ett annat LMS som agerar som producent) gäller denna tidsödande logik.<br><br>Men om innehållet spelas upp utanför LMS (det vill säga om innehållet finns i ALM, är ALM producenten, men uppspelningen sker i en extern spelare) gäller inte den här delen av tidsberäkningslogiken.  <br>**Obs!**: LTI Consumer stöds inte i Adobe Learning Manager. | Inaktiv flik |

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























<!-- See this [article](/help/migrated/administrators/feature-summary/reports/learner-transcripts.md) for more information on Learner Transcript report.

The downloaded Learner Transcript report contains the new column: Mark Completed Date (UTC TimeZone).

![Learner Transcript reports showing marked completed dates (highlighted in yellow) for course completion tracking in Adobe Learning](/help/migrated/assets/mark-completion-column.png)
_Learner Transcript report displays a new column in yellow highlighting individual completion dates for each user_

## Enhanced User Report with extended data fields

**Overview**

The User Report now includes additional fields to improve user tracking and organizational mapping.

**What's new**

* Internal User ID column: Provides unique internal identifiers for smooth user tracking across different systems and API endpoints.
* Manager Email column: Includes direct manager contact information for organizational hierarchy tracking.

**Key benefits**

* Simplified user identification and eliminates issues when mapping users across multiple systems.
* Supports downstream user management workflows through integration capabilities.
* Improved organizational mapping and better understanding of reporting relationships.
* Maintains organizational boundaries and prevents accidental cross-communication.

### User Report with the new column

See this [article](/help/migrated/administrators/feature-summary/reports.md#user-activity-dashboards) to learn how to download the User Report. 

The downloaded User Report file contains the new columns: Internal User ID and Manager Email.

![User Report showing the internal user ID and manager email columns highlighted in yellow](/help/migrated/assets/user-report-columns.png) 
_User Reports highlighting internal user IDs and manager email addresses to streamline user management_

## FTP User Report with Internal User ID support

**Overview**

The FTP-based User Report now includes Internal User ID support, providing a unified approach to data export and integration for headless implementations.

**What's new**

* User Reports are now available through [Custom FTP](/help/migrated/integration-admin/feature-summary/connectors.md#custom-ftp) alongside existing reports (Gamification Transcripts, Learner Transcripts, Trainings Report).
* The Internal User ID column is now consistent across all export methods (FTP, Jobs API, and UI).

**Key benefits**

* Simplified data management with a single source for all necessary reports.
* Better data consistency by ensuring uniform user identification across reporting periods.
* Automated workflow support by enabling bulk operations and analytics workflows with consistent identifiers.
The User Report downloaded from FTP folder contains the new column, Internal User ID.

## Include suspended users in Learner Transcripts

**Overview**

Organizations can now include suspended users (those with disabled external profiles) in Learner Transcripts, ensuring comprehensive historical learning data retention.

**What's new**

* Configurable suspended user visibility with an account-level flag to include suspended users in the Learner Transcripts.
* Historical data retention even after deactivation of suspended external profiles.

**Implementation requirements**

* Contact your Customer Success Manager (CSM) to enable the account-level flag.

>[!NOTE]
>
>This flag is disabled by default for existing accounts and must be explicitly requested for new accounts.

## Scoped announcement permissions for custom administrators

**Overview**

Custom administrators can now create announcements, but only for their assigned user groups or catalogs. This prevents unintended communication across organizational boundaries.

**What's new**

* Custom administrators can only create announcements for users within their assigned scope.
* Announcements can be scoped to specific user groups or catalogs.
* Full administrators maintain visibility and control over all announcements, including those created by scoped custom administrators.

**Key benefits**

* Targeted communication ensuring announcements reach only relevant audiences.
* Reduced information overload by preventing irrelevant notifications from reaching unintended users.
* Maintains organizational boundaries and prevents accidental cross-communication.

**Important considerations**

* If a custom administrator's scope changes, affected announcements display a warning icon and require individual scope resets.
* Each announcement must be updated individually when scope changes occur.
* The Notification Announcement report shows only learners within the custom administrator's assigned scope.

**Use cases**

* Franchise organizations where regional managers need to communicate only with their franchisees.
* Large organizations with regional or departmental administrators targeting announcements to their teams.

### Create announcement for the assigned scope

A custom administrator can create announcements limited to their assigned user groups and catalogs, ensuring messages reach the right audience and preventing unnecessary notifications.

To create an announcement for the assigned scope:

1. Log in to Adobe Learning Manager as an administrator.
2. Select **[!UICONTROL Announcement]** in the left navigation pane.
3. Select **[!UICONTROL Add]**. 
   
   ![](/help/migrated/assets/create-add-announcement.png)
   _Announcements page in Adobe Learning Manager, where administrators can create and manage announcements for targeted user groups_

4. Select the **[!UICONTROL Announcement Type]** from the dropdown menu.
        a. **[!UICONTROL As Notification]**
        b. **[!UICONTROL As Masthead]**
        c. **[!UICONTROL As Recommendation]**
        d. **[!UICONTROL As Email]**
5. Select **[!UICONTROL As Masthead]**. 
6. Select the language and upload an image for the masthead. 
7. Optionally, add a URL for the action button. 
   
   ![](/help/migrated/assets/announcement-screen.png)
   _Create Announcement screen allowing administrators to set announcement type, upload attachments, and add action buttons_

    The assigned scope is pre-selected in the **[!UICONTROL Scope]** section and cannot be modified by administrators.
    
    >[!NOTE]
    >
    >**[!UICONTROL For Notification]** and **[!UICONTROL Email]** announcements, they can include additional user groups and catalogs if these overlap with their assigned scope.

8. Select **[!UICONTROL Save]**.

Only learners within the custom administrator's scope will be able to view the announcement. See this [article](/help/migrated/administrators/feature-summary/announcements.md) to learn how to create multiple types of announcements. 

### Reset the scope by Custom administrators

Custom administrators can reset the scope of their published announcements if an administrator has changed the scope of them. Once the scope is reset, the updated scope will be applied to the announcement, and only learners within the new scope will be able to see the announcement.

To reset the scope:

1. Log in to Adobe Learning Manager as a custom administrator.
2. Select **[!UICONTROL Announcement]** in the left navigation pane.
3. Select **[!UICONTROL Published]** tab.
4. Select any announcement and then select setting icon. 
5. Select **[!UICONTROL Edit]**. 

   ![](assets/select-edit-published-announcement.png)
   _Announcement screen showing the published announcements with edit, publish and other options_

6. Select **Reset**. 

   ![](assets/reset-the-scope.png)
   _Announcement showing a scope change notification, with an option for custom administrators to reset and update the scope selection to reflect new access permissions_

The scope will be updated, and only users within the updated scope will be able to view the announcement.

### Edit the announcement through administrator UI

Administrators can view announcements created by custom administrators through their interface. They have the ability to edit these announcements only by modifying or removing the assigned scope. If scope changes are not made, administrators cannot make further edits to the announcement.

To edit the announcement through administrator UI:

1. Log in to Adobe Learning Manager as an administrator.
2. Select **[!UICONTROL Announcement]** in the left navigation pane.
3. Select **[!UICONTROL Published]** tab.
4. Select any announcement and then select setting icon.
5. Select **[!UICONTROL Edit]**. 

   ![](assets/select-edit-published-announcement.png)
   _Announcement screen showing the published announcements with edit, publish and other options_

6. Select **[!UICONTROL Remove]**. 
   
   ![](assets/remove-the-scope.png)
   _Announcement screen indicating that scope must be removed to allow administrators to edit announcements created for scoped user groups_

Administrator can edit the announcement after removing the scope.

## Tag users in social boards

**Overview**

Social learning boards now support user tagging functionality, enabling more targeted discussions and improved collaboration within learning communities. Learners can be tagged in social learning posts and comments through the learner app, APIs, and Adobe Learning Manager reference site.

**What's new**

* **@username tagging**: Users can tag other board members using the "@username" format.
* **Scope-restricted tagging**: Only users with access to the specific board can be tagged, ensuring privacy and relevance.
* **Multi-channel notifications**: Tagged users receive both in-app and email notifications with direct links to relevant posts or comments.

**Key features**

* Users outside the board's scope cannot be tagged, preventing unwanted notifications.
* If a tagged user is deleted from the system, their mention appears as "anonymous".
* Tagging user groups or "@all" is not permitted to prevent notification spam.

**Use cases**

* Healthcare professionals seeking input from specific colleagues on medical cases.
* Subject matter experts being consulted on specialized topics.
* Team discussions requiring input from specific stakeholders.
* Knowledge sharing sessions with targeted expert involvement.

### Tag users in social board posts

Learners can now tag specific board members in posts or comments using @username. Tagging is limited to members with access to that board.

To tag users in a social board:

1. Log in to Adobe Learning Manager as a learner. 
2. Select **[!UICONTROL Social Learning]** in the left navigation pane.
   
   ![](/help/migrated/assets/select-social-learning-admin.png)
   _Enable collaborative learning by selecting Social Learning to access discussion boards, share insights, and tag users for interactive engagement_

3. Select **[!UICONTROL New Post]**.
   
   ![](assets/select-new-post.png)
   _Start a new discussion by selecting New Post in Social Learning to share knowledge with the tagged users_

4. Before tagging users, select the board from the **[!UICONTROL Post this to a Discussion Board]** option.

   ![](assets/select-boards-in-social-board.png)
   _Select a discussion board to post and tag users, enabling targeted collaborative conversations in Social Learning_

5. Type your post details, then tag a user by entering the @ symbol followed by their name (for example, @andrew). When you type @ followed by the first three letters of the user's name, it displays a list of matching users.
 
   ![](assets/type-a-user-tag.png)
   _Tag users in your discussion post by typing @ followed by the username to enable targeted collaboration within Social Learning boards_

6. Select the desired user from the list.
7. Select **[!UICONTROL Post]**. 

The tagged users receive both in-app and email notifications with a direct link to the post, making discussions more targeted and collaborative.

### Tag users based on the board's scope

Scope-restricted tagging allows users to tag only those learners who have permission to access a specific board. This helps maintain privacy by preventing tagging of users outside the scope. 

If you try tagging learners who are outside the board's scope, no suggestions will appear, and you won't be able to tag them. Refer to this [article](/help/migrated/administrators/feature-summary/social-learning-configurations-as-an-admin.md) to learn more about Social Learning Scope. 

## Tag deleted users in comments

If a user who has been deleted is tagged in a Social Learning post, their name will show as Anonymous in the post. The comment and tag remain visible for context, but profile link or details are not shown.

![](assets/deleted-users-tagged.png) 
_Social Learning post highlighting how a deleted user appears as Anonymous when tagged_

## Job Aids report with direct access links

**Overview**

The Job Aids report has been enhanced to include direct download links to job aids, streamlining content management and audit processes for administrators and authors.

**What's new**

* Job Aid Link column: Direct access to job aid files and external URLs from within the report.
* Role-based access control: Link accessibility depends on user roles and catalog permissions.
* Deleted job aids remain accessible if still linked to active courses.

**Key benefits**

* Direct file downloads and URL access from within the report.
* Eliminates manual effort in locating and downloading job aids for compliance or accessibility audits. 

**Use cases**

* Authors or administrators conduct regular accessibility audits on job aids, as required by large organizations.
* Any scenario where quick, role-based access to job aid files is needed for review or compliance.

### Job Aids Report with the new column

See this [article](/help/migrated/administrators/feature-summary/reports.md#job-aids-report) to learn how to download Job Aids Report.

The Job Aids Report can be downloaded from the Reports section and now includes direct download links for each job aid.

![](assets/job-aid-report.png) 
_Job Aids Report displays direct download links, making it easy to access and download job aids in Adobe Learning Manager_

## API updates

### Learner API enhancements for quiz performance tracking

**Overview**

The `GET /loResourceGrades` API has been enhanced to provide detailed quiz performance data, enabling more sophisticated analytics and automated decision-making.

**What's new**

The API response now includes two additional fields:

* **[!UICONTROL highestScore]**: The best score achieved by a learner across all quiz attempts
* **[!UICONTROL maxScore]**: The total possible score for the quiz

**API response example**

```
{
    "links": {
        "self": "https://learningmanagerstage1.adobe.com/primeapi/v2/loResourceGrades/course:15067_30122_41715_1_3400468"
    },
    "data": {
        "id": "course:15067_30122_41715_1_3400468",
        "type": "learningObjectResourceGrade",
        "attributes": {
            "completed": false,
            "duration": 0,
            "hasPassed": false,
            "highestScore": 0,
            "maxScore": 0,. 
            "progressPercent": 0,
            "score": 0
        },
        "relationships": {
            "loResource": {
                "data": {
                    "id": "course:15067_30122_41715_1",
                    "type": "learningObjectResource"
                }
            }
        }
    }
}
```

In response, **course:15067_30122_41715_1_3400468** is the ID of the Learning Object resource grade for which the information is being requested. The `learningObjectResourceGrad`e id can be obtained from the `GET /enrollments/{id}` API.  

**Key benefits**

* Enables detailed quiz performance analysis for learning effectiveness measurement.
* Supports progression rules based on highest achievement rather than most recent attempts.
* Provides complete picture of learner quiz performance over time.

**How the API works**

1. A user attempts a quiz multiple times; each attempt is recorded.
2. The API provides both the highest score achieved and the maximum possible score for the quiz.
3. External systems can use this data to trigger automated actions, such as enrolling users in new courses based on their best performance.

**Use cases**

* Headless learning systems require automated enrollment decisions.
* Learning analytics platforms tracking learner achievement patterns.
* Compliance systems with performance-based progression requirements.

### Migration API enhancements

**Overview**
Adobe Learning Manager now supports the migration of various data objects into an account via the migration process. This process can be initiated via both APIs and the User Interface. When a migration fails, errors are available for download via the interface. These errors are useful in debugging migration errors and managing the migration runs. 

With this release, the error logs will also be available to download via the APIs for efficient, programmatic error tracking and debugging.

**API changes**

There is a new migration API, `runStatus`, which allows integration administrators to check the status of migration runs triggered via the API, something not possible in previous versions of Adobe Learning Manager. 

Additionally, `runStatus` API now provides a direct link to download error logs (CSV) for completed runs. Note that the link is valid for seven days only, and the logs are retained for one month.

The `startRun` API's response has been updated to include the migration project ID, sprint ID, and sprint run ID, which are required to query the new status endpoint. 

#### runStatus API

**Description**

Retrieves the status of an existing migration run.

**Endpoint**

```
GET /bulkimport/runStatus
```

**Parameters**

* **migrationProjectId**: (Required). A unique identifier for a migration project. A migration project is used to transfer data and content from an existing Learning Management System (LMS) to Adobe Learning Manager. Each migration project can consist of multiple sprints, which are smaller units of migration tasks.

* **sprintId**: (Required). A unique identifier for a sprint within a migration project. A sprint is a subset of migration tasks that includes specific learning items (e.g., courses, modules, learner records) to be migrated from an existing LMS to Adobe Learning Manager. Each sprint can be executed independently, allowing for phased migration.

* **sprintRunId**: (Required). A unique identifier used to track the execution of a specific sprint within a migration project. It's associated with the actual migration process for the items defined in a sprint. The sprintRunId helps in monitoring, troubleshooting, and managing the migration job.

**Response**

```
{
  "sprintId": 2510080,
  "sprintRunId": 2740845,
  "migrationProjectId": 2509173,
  "startTime": 1746524711052,
  "endTime": 1746524711052,
  [
    {
      "id": 2609923,
      "lastHeartbeatTime": 1746524711052,
      "objectName": "content",
      "jobState": "COMPLETED",
      "errorCsvLink": "",
      "errorLogLink": "migration/5830/2509173/2510080/2740845/content_err.csv",
      "sequenceNumber": 1
    },
    {
      "id": 2609922,
      "lastHeartbeatTime": 1746524713577,
      "objectName": "course",
      "jobState": "WAITING_IN_QUEUE",
      "errorCsvLink": "",
      "errorLogLink": null,
      "sequenceNumber": 2
    }
  ]
}
```

#### startRun API

The `startRun` API response was updated to include three additional fields- migrationProjectId, sprintId, and sprintRunId. These fields allow users to track and query the status of specific migration runs using the new runStatus API.

```
curl -X GET --header 'Accept: text/html' 'https://learningmanager.adobe.com/primeapi/v2/bulkimport/runStatus?migrationProjectId=001&sprintId=10001&sprintRunId=7'
```

Produces the following response. The response contains:

* migrationId
* sprintId
* sprintRunId

**Response**

```
{
  "status": "OK",
  "title": "BULKIMPORT_RUN_INITIATED_SUCCESSFULLY",
  "source": {
    "info": "Success",
    "migrationInfo": {
      "migrationProjectId": "001",
      "sprintId": "10001",
      "sprintRunId": "7"
    }
  }
}
```

### Social API changes (user tag, comments, and replies)

**Overview**

Adobe Learning Manager now supports @user tagging functionality in Social Learning boards, enabling learners to mention and notify peers within posts, comments, and replies. This feature enhances collaboration and content discovery across the platform.

This release introduces new API capabilities to support user mentions, including enhanced POST and GET endpoints, as well as a new search functionality for tagged users.

**API changes overview**

* Updated POST APIs for creating posts/comments/replies with user mentions
* Updated GET APIs with user mention data in responses

**Format of user mentions**

A user is mentioned using the format: @(user:userId)

#### Create post with mentions

**Endpoint**

```
POST /primeapi/v2/posts
```

**Description**

Create a new social learning post with user mentions.

**Request body**

```
{
  "data": {
    "type": "post",
    "attributes": {
      "boardId": 13282,
      "accountId": 11152,
      "text": "<p>This is a new post mentioning @[user:11257229]</p>",
      "createdByUserId": 11257228,
      "postType": "discussion"
    },
    "id": null
  }
}
```

**Response**

Standard post creation response with mention data included in the _userMentions_ relationship.

#### Create comment with mentions

**Endpoint**

```
POST /primeapi/v2/comments
```

**Description** 

Add a comment to a post with user mentions.

**Request body**

```
{
  "data": {
    "type": "comment",
    "attributes": {
      "postId": 20746,
      "accountId": 11152,
      "text": "<p>Test Comment @[user:11257229]</p>",
      "createdByUserId": 11257228,
      "commentLevel": 0
    },
    "id": null
  }
}
```

#### Create reply with mentions

**Endpoint**

```
POST /primeapi/v2/replies
```

**Description**

Reply to a comment with user mentions.

**Request body**

```
{
  "data": {
    "type": "reply",
    "attributes": {
      "postId": 20746,
      "accountId": 11152,
      "text": "<p>Thanks for the update @[user:11257229]</p>",
      "createdByUserId": 11257228,
      "commentLevel": 1,
      "parentCommentId": 55621
    },
    "id": null
  }
}
```

#### Retrieve posts with mentions

**Endpoint**

```
GET /primeapi/v2/posts/{id}
```

**Description**

Retrieve post details, including mentioned users.

**Response**

```
{
  "links": {
    "self": "https://learningmanager.adobe.com/primeapi/v2/posts/7522"
  },
  "data": {
    "id": "7522",
    "type": "post",
    "attributes": {
      "commentCount": 3,
      "dateCreated": "2025-06-10T11:33:29.000Z",
      "dateUpdated": "2025-06-25T14:52:04.000Z",
      "downVote": 0,
      "postingType": "DEFAULT",
      "richText": "<p>my updated fourth post @[user:14707776] second mention my first post</p>",
      "state": "ACTIVE",
      "text": "my updated fourth post @[user:14707776] second mention my first post",
      "upVote": 0,
      "viewsCount": 0
    },
    "relationships": {
      "createdBy": {
        "data": {
          "id": "14707776",
          "type": "user"
        }
      },
      "parent": {
        "data": {
          "id": "3971",
          "type": "board"
        }
      },
      "userMentions": {
        "data": [
          {
            "id": "14707776",
            "type": "user"
          }
        ]
      }
    }
  },
  "included": [
    {
      "id": "14707776",
      "type": "user",
      "attributes": {
        "avatarUrl": "https://cpcontents.adobe.com/public/images/default_user_avatar.svg",
        "binUserId": "45664b87-75a3-43ec-b0b7-5064958eac6f",
        "email": "user@example.com",
        "enrollOnClick": false,
        "fields": {
          "Location": "BLR"
        },
        "gamificationEnabled": true,
        "lastLoginDate": "2025-06-27T11:21:17.000Z",
        "name": "John Doe",
        "pointsEarned": 1690,
        "pointsRedeemed": 0,
        "preferredResolution": "AUTO",
        "profile": "admin",
        "roles": [
          "Learner",
          "Admin",
          "Author",
          "Instructor",
          "Integration Admin",
          "Manager"
        ],
        "state": "ACTIVE",
        "userType": "Internal"
      },
      "relationships": {
        "account": {
          "data": {
            "id": "9238",
            "type": "account"
          }
        }
      }
    }
  ]
}
```

### Social API changes (user search)

**Endpoint**

```
GET /primeapi/v2/users/search?q={searchTerm}&context=tagging
```

**Description**

Search for users available for tagging based on social scope settings.

**Request parameters**


* q (required): Search term (minimum 3 characters).
* context: Set to "tagging" to get users eligible for mentions.
* boardId (optional): Board ID to filter users based on access permissions.

**Response**

```
{
  "data": [
    {
      "id": "11257229",
      "type": "user",
      "attributes": {
        "name": "Jane Smith",
        "email": "jane.smith@example.com",
        "avatarUrl": "https://cpcontents.adobe.com/public/images/default_user_avatar.svg",
        "userType": "Internal",
        "state": "ACTIVE"
      }
    }
  ]
}
```

### Implementation guidelines

#### Character limits

* Posts: 4000-character limit applies, with each tagged user reducing available characters by a fixed amount.
* Comments: 1000-character limit.

#### Mention validation

* Users can only be tagged by username or email (not UUID).
* Internal users cannot tag external users and vice versa.
* Tagging availability follows existing social scope settings.
* Board permissions determine tagging eligibility (Public/Private).

#### Notifications

* Multiple mentions of the same user in one post result in a single notification.
* Original post owner receives notifications only when specifically tagged.

#### Error handling

* Invalid user IDs in mentions return validation errors.
* GDPR and soft-deleted users appear anonymous in tagged content.

### Language-based learner progress

Currently, learner progress is tracked only for the selected locale language, causing significant progress loss when switching languages/locales in the player. This limitation creates poor user experience where learners lose their learning progress when exploring content in different languages.

**Current issues**

* **Progress override**: The progress for each module in the player is tracked at both the user and module levels. This leads to a situation where a user's progress is overridden when they switch back to a previously used locale for the same module.
* **Progress reset**: For instance, if a learner achieves 75% progress in Locale A (English) and then switches to Locale B (Spanish), upon returning to Locale A, their progress resets to 0% instead of resuming from 75%.

To resolve these limitations, the API has been enhanced to support locale-specific progress tracking:

* **Locale-specific storage**: When a learner switches locales (for example, from Locale A to Locale B) within the player, the system now saves the progress state separately for each locale of the content.
* **Progress resumption**: When the user switches back to a previously used locale (from Locale B back to Locale A), the content resumes from where they left off in that specific locale.
* **Independent progress tracking**: Each locale maintains its own state of progress, allowing learners to explore content in multiple languages without losing their individual progress in each language.

#### API changes

The following APIs have been enhanced to support the new locale parameter:

* GET Player State API
* POST Player State API

#### GET Player State API

**Endpoint**

```
GET /primeapi/v2/users/{userId}/playerState
```

**Description**

Retrieves the current state of a learning object for a specific user and locale.

**Parameters**

|Parameter |Type |Location |Required |Description |
|---|---|---|---|---|
|userId |String |Path |Yes |Unique identifier of the user |
|loId |String |Query |Yes |Learning Object identifier in format lo:{id} |
|loResourceId |String |Query |Yes |Learning Object resource identifier in format course:{loId_loInstanceId_moduleId_moduleVersion}|
|csrf_token |String |Query |Yes |CSRF protection token |
|locale |String |Query |Optional |Locale identifier for language-specific progress (e.g., "en-US", "es-ES") |

**Example request**

```
GET /primeapi/v2/users/12345/playerState?loId=lo:67890&loResourceId=course:67890_1_mod123_v2&csrf_token=abc123&locale=en-US
```

**Response behavior**

* If the locale parameter is provided and a locale-specific state exists, the API returns the progress for that locale.
* If the locale parameter is provided but no locale-specific state exists, the API performs a fallback search for the default state.
* If the locale parameter is omitted, the API returns the default state (maintains backward compatibility).
* For headless requests where the locale is null, the API falls back to the default state lookup.

#### POST Player State API

**Endpoint**

POST /primeapi/v2/users/{userId}/playerState

**Description**

Updates or creates the current state of a learning object for a specific user and locale.

**Parameters**

|Parameter |Type |Location |Required |Description |
|---|---|---|---|---|
|userId |String |Path |Yes |Unique identifier of the user |
|loId |String |Query |Yes |Learning Object identifier in format lo:{id} |
|loResourceId |String |Query |Yes |Learning Object resource identifier in format course:{loId_loInstanceId_moduleId_moduleVersion} |
|csrf_token |String |Query |Yes |CSRF protection token |
|locale |String |Query |Optional |Locale identifier for language-sp|

**Request body**

The request body contains the Learning Object state data specific to the locale.

**Example request**

```
POST /primeapi/v2/users/12345/playerState?loId=lo:67890&loResourceId=course:67890_1_mod123_v2&csrf_token=abc123&locale=en-US
```

```
{
  "progress": 75,
  "completionStatus": "incomplete",
  "timeSpent": 1800,
  "lastAccessedPage": 5,
  // Additional state data
}
```

The API creates or updates the Learning Object state for the specified locale.

## Go1 integration enhancements

**Overview**

Go1 integration is enhanced to allow direct curation of Go1 courses for creating Learning Programs (LP) within Adobe Learning Manager. This update supports the inclusion of Go1 courses in recurring certifications and introduces a new version of the Go1 content hub experience, enabling more efficient course curation.

**What's new**

* Create and manage playlists directly within Go1 using AI chat assistance or manual selection.
* Include Go1 courses in recurring certification cycles with automatic progress reset.
* Upgraded content discovery interface for improved browsing and content curation.

**Key benefits**

* AI-assisted playlist creation significantly speeds content grouping and delivery.
* Enables use of Go1 content for recurring regulatory training requirements.
* Clear preview-and-purchase model supports informed content investment decisions.
* Improved discovery and curation tools for better content management.

**Important notes**

* All Go1 features require an active Go1 license.
* Previous free Go1 content will be decommissioned. Organizations must preview and purchase required content bundles.
* Administrators and authors can create and manage playlists; learners maintain view-only access.

**Use cases**

* Organizations requiring extensive external content libraries for comprehensive training programs.
* Compliance-focused training programs needing regular content updates and delivery cycles.
* Learning teams are seeking to reduce content curation overhead through AI assistance.

### Add Go1 playlist to a Learning Path

Administrators can create a learning path that includes a Go1 playlist, so learners can access selected third-party courses as part of their training.

To create a learning path:

1. Log in to Adobe Learning Manager as an administrator.
2. Select **[!UICONTROL Learning Paths]** in the left navigation pane. 
3. Select **[!UICONTROL Add]**. 

   ![](assets/select-add-to-lp.png)
   _Select Add in the Learning Paths section to create and organize new structured training programs for your learners_

4. Type the required details and select **[!UICONTROL Save]**. See this [article](/help/migrated/administrators/feature-summary/learning-paths.md) for more information. 
5. Select **[!UICONTROL Add Go1 Courses]**.

   ![alt text](assets/select-go1-courses.png)
   _Add Go1 courses to your Sales Engineers Skill Development playlist to expand learning options with curated third-party content_

6. In the **[!UICONTROL Library]**, search for and select **[!UICONTROL Create playlist]** and choose from one of the following:
    a. **[!UICONTROL with AI]**: Create a playlist with the help of AI.
    b. **[!UICONTROL by myself]**: Create a playlist by manually adding courses to it. 

**Create a playlist with AI**

Administrators can type the playlist description in the AI prompt. The AI will curate the related courses and create a playlist based on the requirements. AI generates playlists by interpreting the learning goal or prompt provided by the user. When creating a playlist, admins can select to curate content 'with AI' which allows the system to use large language models to understand the specified learning objectives and content preferences like duration and type. The AI then searches the content library for relevant learning objects that match these criteria.

To create a playlist with AI:

1. Select **[!UICONTROL Create playlist]** and then select **[!UICONTROL with AI]**.
   
   ![](assets/select-by-AI-playlist.png)
   _Create curated playlists with AI, which enables automated course recommendations tailored to learner needs_

2. Type a short description about your playlist in the **[!UICONTROL Enter your learning goal]** text field.
3. Select **[!UICONTROL Next]**. 
   
   ![](assets/type-a-prompt.png)
   _Type your learning goal to create a custom playlist, helping Adobe Learning Manager recommend targeted courses tailored to your learners' needs_

4. Choose the skills from the list.
   
   ![](assets/select-skills.png)
   _Choose the skills from the list to curate the courses for the Sales Engineer_
5. Select the course duration and type for your playlist.
6. Select **[!UICONTROL Generate playlist]**. The playlist is created with 10 courses, and administrators can use it to create a Learning Path.
   
   ![](assets/created-playlist.png)
   _Review your curated Sales Engineer Skills Enhancement Playlist in Adobe Learning Manager_
7. Select **[!UICONTROL Add to Library]**.
8. Select **Yes** in the confirmation prompt.
9. Select the playlist from the **[!UICONTROL Select playlist to import prompt]**. 

   ![](assets/add-playlist-to-lp.png)
   _Select and import the Sales Engineer Skills Enhancement Playlist from the Go1 Library in Adobe Learning Manager_

10. Select **[!UICONTROL Add Playlists to Learning Path]** and then **[!UICONTROL Publish]**. 

The courses in the playlist will be added to the Learning Path. Administrators can then enroll learners, who can immediately begin taking the courses.

**Create a playlist manually**

Manually select courses that best match learners' requirements and curate additional relevant courses.

To create a playlist manually:

1. Select **[!UICONTROL Create playlist]** and then select **[!UICONTROL by myself]**.
   
   ![](assets/select-manual-playlist.png)
   _Manually create a playlist giving administrators full control to curate courses based on specific learner needs_

2. Type the title and description of your playlist.
 
   ![](assets/type-title-and-description.png)
   _Add a title and description to your playlist in Adobe Learning Manager to clearly define its purpose and help guide learners toward targeted skill development_

3. Select **[!UICONTROL Create]**. 
4. Select **[!UICONTROL Add item]** to add the related courses. 
   
   ![](assets/add-items.png)
   _Add items to your Sales Engineers Skill Development playlist in Adobe Learning Manager to curate targeted courses_

5. Search and select the required courses. 

The playlist has been created with related courses, and administrators can use it to create a learning path. 

## Save player state progress for languages

**Overview**

The Fluidic Player now saves your progress separately for each language within a module. This means you can switch between languages and pick up exactly where you left off in each one, instead of losing your progress and starting over.

**Key benefits**

* Jump between languages and resume from your exact position in each one.
* Perfect for learners who need to access content in multiple languages during their learning journey.
* Complete the module in any language while maintaining progress in all languages you've accessed.

**Use cases**

* Global organizations with employees who speak multiple languages and may need to reference content in their native language and English.
* Compliance training where learners might start in one language but need to complete in another for certification purposes.
* Technical training programs where learners might understand concepts better in their native language but need English terminology for their work.

**Important notes**

* The Fluidic Player's language preference is retained within a session. If a learner changes the language and moves to another module, the new language is used for subsequent modules, as long as the player remains open.
* The grade (completion status) is still tracked at the module level, not per locale. The first locale in which the completion criteria are met will update the grade for the module. If a learner completes the module in one language and then switches to another, any further grade updates will be overwritten from the previous grade, but progress for each locale is still preserved.

## Custom roles import support in incremental user import

Adobe Learning Manager now supports custom role imports in the existing multi-incremental user import workflow (regular full user import + incremental enabled flow). This enhancement allows role.csv and user_role.csv files to be uploaded and processed incrementally, without requiring full data uploads each time.

Previously, role.csv and user_role.csv files could only be uploaded in full mode, meaning administrators had to include all previously added role definitions and assignments in every upload. With this new incremental support, only new or modified role data needs to be uploaded, reducing overheads and improving efficiency.

**What's new**

1. Incremental support for custom roles and role assignments:

    * role.csv  and  user_role.csv can now be processed incrementally in the multi-file incremental workflow.
    * No need to upload all existing role and user role data with every import.

2. Enhanced multi-incremental workflow implementation:

    * Create separate folders in FTP for each uploaded user import file.
    * Each folder contains:

        * The user import file- (File1.csv)
        * Corresponding role and role assignment files- (File1_role.csv, File1_user_role.csv)

    For example, user1.csv corresponds to user1_role.csv (custom roles) and user1_user_roles.csv (user-role mapping).

    **Example FTP structure before processing:**

    ```
    import/user/internal/  
         File1.csv  
         File2.csv  
        File3.csv  

    UserRole/  
        File1_role.csv  
        File1_user_role.csv  
        File2_role.csv  
        File2_user_role.csv  
        File3_role.csv  
        File3_user_role.csv  
    ```
 
3. Adobe Learning Manager also supports up to 20 incremental user CSVs and their corresponding custom roles CSVs, making it suitable for large-scale operations.

**Use cases**

* Global companies manage regional teams by uploading multiple incremental user files for each region (EU, America, Asia), allowing administrators to update users and assign new roles for each region in a single workflow.
* Large enterprises automate onboarding and permissions by regularly ingesting incremental user updates from HR systems. This supports seamless updates to user profiles and granular role assignments without manual intervention.

### New columns added to CSV files

Three new columns have been introduced to enhance the data captured in user, role, and user-role CSV exports/imports:

* **User Registration State (user.csv)**: Indicates the current registration status of the user.
* **Role State (role.csv)**: Indicates the current status of roles within the system.
* **User Role State (user_role.csv)**: Indicates the status of the user-role association. 

>[!NOTE]
>
>The above CSV changes apply only to the accounts that use incremental users.

Download the [sample CSVs](assets/sample-csv-Incremnetal.zip) here. 

## Reset recommendations in Salesforce app

**Overview**

Previously, learners using the Adobe Learning Manager Salesforce app could only select roles and recommendation preferences once. If their role changed, they were required to access the native Adobe Learning Manager app to update their profile and receive relevant course recommendations. This made the learning experience and contributed to lower engagement within the Salesforce environment.

**What's new**

Adobe Learning Manager now features a  **[!UICONTROL Reset Interests]** button within the Salesforce app. Learners can now reset their roles and learning preferences without needing to leave Salesforce or sign in into the native Adobe Learning Manager app. This enhancement streamlines access to personalized learning content, ensuring recommendations remain relevant as users' roles evolve.

**Use cases**

* Learners who change job roles, teams, or responsibilities can quickly reset their preferences to receive updated and relevant course recommendations all within the Salesforce app.
* By removing the need to switch to the native Adobe Learning Manager app, the learning journey is smoother, encouraging ongoing engagement and consumption of recommended content through Salesforce.
* Administrators benefit from higher rates of learning completion and better alignment between user roles and recommended content, without extra support or guidance on switching platforms.

### Reset interest in the Salesforce app

To reset the interests and recommendations from the Salesforce app:

1. Log in to Adobe Learning Manager app for Salesforce as a learner.
2. Select **[!UICONTROL Reset Interests]** option at the bottom.

The learner's recommendation or interest will be reset from the Adobe Learning Manager Salesforce app. 

## Create learning portals with Experience Builder

>[!IMPORTANT]
>
>We are excited to announce that Experience Builder, the innovative tool for creating customizable learning portals, will be available following the October 2025 release of Adobe Learning Manager.
>
>Stay tuned for more updates as we approach the release date. We look forward to seeing how you use Experience Builder to transform your learning portals.
>
>For any questions or additional information, contact your Customer Success Manager.

**Introduction**

Experience Builder is a no-code/low-code tool in Adobe Learning Manager that helps you create customized learning portals. It allows you to design branded, user-friendly learning portals without needing technical skills or extensive coding knowledge.
With Experience Builder, you can create new pages, menus, and widgets to deliver personalized learning experiences for your audience quickly and easily. With Experience Builder, you can quickly create new pages, menus, and widgets to deliver personalized learning experiences for your audience.

**Problem statement**

Before Experience Builder, organizations faced several challenges:

1. **Limited customization**: Portals had fixed designs with few options to reflect your brand. Administrators could only make basic changes, such as modifying headers, footers, or colors, which limited the ability to create unique experiences.
2. **Cost**: Building custom portals required expensive developers and long timelines, often taking 6 to 9 months to complete. This approach increased the total cost of ownership and delayed deployment.
3. **Generic experiences**: Everyone saw the same content, even if it wasn't relevant to their role or needs. This lack of personalization reduced learner engagement and satisfaction.
4. **Technical barriers**: Non-technical administrators struggled to create or update portals because they needed coding knowledge or external support.

Experience Builder solves these problems by providing a simple, no-code/low-code solution for creating personalized, branded portals.

It allows administrators to design portals that meet their organization's needs without relying on technical expertise or external developers.

**Key benefits**

**Easy customization**

* Design portals that match your brand with custom headers, footers, logos, and layouts.
* Use widgets to add dynamic content like courses, categories, and HTML elements.
* Create pages and menus tailored to specific audiences, ensuring learners see relevant content.

**No-code/low-code solution**

* Administrators can create and manage portals without coding knowledge, making it accessible to non-technical users.
* Drag-and-drop functionality simplifies the process of building pages and menus.

**Personalized learning**

* Configure pages and menus to display content relevant to specific user groups, such as sales teams, designers, or engineers.
* Use hidden pages to provide exclusive content accessible only through direct links.

**Global reach**

* Create multilingual pages to support learners around the world.
* Localize content to cater to diverse audiences and improve accessibility.

**Mobile-friendly**

* Learners can access content on any device, including phones and tablets.
* Preview pages in both desktop and mobile views to ensure a smooth experience.

**Real-world use cases**

**Branded portals**

* Create a learning portal that looks like your company's website, complete with logos, colors, and layouts.
* For example, a healthcare company can design a portal that matches its corporate branding while integrating learning content.

**Role-based learning**

* Build pages for specific roles, like engineers, sales teams, or designers.
* For instance, sales teams might see product training, while engineers access technical courses.

**Product training**

* Set up separate pages for different products, such as Photoshop, Illustrator, or other offerings.
* Each page can include widgets displaying courses, certifications, and resources related to the product.

**Employee and customer training**

* Use the portal for onboarding new employees, training external partners, or educating customers about your products.
* For example, a software company can create a portal for customer tutorials and troubleshooting guides.

**Localized content**

* Offer content in multiple languages for global learners.
* For instance, a multinational company can create pages in English, Spanish, and French to cater to its diverse workforce.

### Building blocks of Experience Builder

The main components and building blocks of Experience Builder are structured to provide flexibility, ease of use, and targeted learning experiences. Below is a detailed breakdown:

#### Pages

Pages are the foundation of building a learning portal in Experience Builder. Administrators can create new pages tailored to specific audiences or purposes. Additionally, administrators can:

* Create custom pages with flexible layouts (rows and columns).
* Add widgets to populate pages with content.
* Manage page lifecycle with draft and published states.
* Hide pages from menus while keeping them accessible via direct links.

For example, a page for sales training might include widgets displaying relevant courses, testimonials, and a calendar of upcoming sessions.

#### Menus

Menus organize pages into navigable structures for learners. Administrators can:

* Create custom menus to group pages for specific user groups.
* Add hierarchy and ordering to prioritize visibility for specific audiences.
* Include submenus for grouping related pages.

For example, a menu called Resources might include pages for eBooks, videos, and FAQs.

#### Widgets

Widgets allow administrators to add dynamic content and functionality to pages. The following widgets are available:

* Calendar
* Categories
* Compliance Status
* Courses & Paths
* Content Box
* Gamification
* HTML
* Iframe
* My Learning
* Social Learning

For example, a page might include a Courses & Paths widget to display recommended courses and a Calendar widget for upcoming training sessions.

#### Branding tools

Experience Builder provides tools to customize the appearance of the portal. Administrators can:

* Customize headers, footers, and layouts to match corporate branding.
* Use CSS and JavaScript for advanced styling.

For example, a healthcare company might use branding tools to create a portal that matches their corporate website's look and feel.

### Get started with Experience Builder

A software company wants to build a training portal for its customers. The portal will have pages for different products like Photoshop and Illustrator, organized in menus. It will include widgets that show courses, certifications, and upcoming training sessions.

#### Create a page

To create a page in Adobe Learning Manager:

1. Log in to Adobe Learning Manager as an administrator. 
2. Select **[!UICONTROL Branding]** in the left navigation pane. 
3. Select **[!UICONTROL Custom Pages]**.
4. Select **[!UICONTROL Create page]**.

   ![](assets/select-create-page.png)
   _Custom Pages screen showing the Create page option to design new custom learning experiences_

5. Type the **[!UICONTROL Page name]** (for example, Photoshop training).
6. Type the **[!UICONTROL Page description]** (for example, Learn how to use Photoshop effectively). 
7. Select the page type from the following:

    * **[!UICONTROL Build using ALM widgets]**: Administrator can create a page using the existing Adobe Learning Manager widgets.
    * **[!UICONTROL External page]**: The administrator can add a URL for the external page. If you select the page type as external, add the URL in the Page URL text field.

8. Select the **[!UICONTROL Change icon]** to change the page's icon.
 
   ![](assets/create-page-screen.png)
   _Courses page creation screen displaying options to type the page name, description, type, and icon for a customized learner page_
9. Select **[!UICONTROL Add New Language]** to add the default language for the page. 
10. Select **[!UICONTROL Save]**. 

The page has been created and saved as a draft in the Custom Pages section. Administrators can edit and design the drafted pages using the widgets. 

#### Design page in Experience Builder

Adobe Learning Manager enables administrators to design pages tailored to their requirements using customizable widgets.
To design the page in Experience Builder:

1. Log in to Adobe Learning Manager as an administrator. 
2. Select **[!UICONTROL Branding]** in the left navigation pane. 
3. Select **[!UICONTROL Custom Pages]** and then select the required page. 
4. Select **[!UICONTROL Page Design]**.  
5. Select **[!UICONTROL Edit]**. 
 
   ![](assets/edit-the-page.png)
   _Edit mode allows administrators to design course pages by organizing sections and adding widgets in their preferred language_

6. Choose the options from **[!UICONTROL Select section layout]** dropdown.
7. Select a section from the following based on the number and size of the widgets you want to add in the section:

    * **[!UICONTROL 1 column-Full section width]**: Content spans the entire section width for maximum space.
    * **[!UICONTROL 2 columns-1/2 section width each]**: Two equal-width columns split the section evenly.
    * **[!UICONTROL 2 columns-2/3 and 1/3 section width respectively]**: Main content takes two-thirds, side content one-third.
    * **[!UICONTROL 2 columns-1/3 and 2/3 section width respectively]**: Side content takes one-third, main content two-thirds.
    * **[!UICONTROL 3 columns-1/3 section width each]**: Three equal-width columns divide the section into thirds.
 
   ![](assets/select-section-layout.png)
   _Section layout selection dialog allows administrators to choose single or multi-column widget arrangements for custom page design_

8. Select **[!UICONTROL Proceed]**.
9. Select **[!UICONTROL Add widget]**.
 
   ![](assets/select-add-widgets.png)
   _The page design screen allows administrators to select and add widgets to customize their course pages_

10. Choose the required widget and then select **[!UICONTROL Proceed]**. 
11. Configure the widget and select **[!UICONTROL Add widget]**. See this [section](#add-and-configure-widgets) for adding and configuring the widgets.
12. Select **[!UICONTROL Save]** and choose from the following options:

    * **[!UICONTROL Save as Draft]**: The page will be saved as a draft. The administrator can edit the page later.
    * **[!UICONTROL Save & Publish]**: The page will be published, and the administrator can add this page to the Menu. 
   
   ![](assets/select-save-options.png)
   _Save options allow administrators to choose between saving a page as a draft for future editing or publishing it for learner access_

The page can be saved as a draft or published. Administrators can edit drafts before publishing and can also update and republish published pages.

#### Add and configure widgets

**Calendar widget**

This widget visually presents courses and schedules in calendar format. It supports filters by catalog, enrollment status, location, product, and role. The responsive design adapts to various grid sizes.

To configure the Calendar widget:

1. Follow steps 1-9 from the [Design page in Experience Builder](#design-page-in-experience-builder). 
2. Select **[!UICONTROL Calendar]** and then select **[!UICONTROL Proceed]**.
 
   ![](assets/select-calendar.png)
   _Widget selection screen highlighting the Calendar widget option to display training sessions in a calendar_

3. Type a **[!UICONTROL Widget title]** and **[!UICONTROL Widget description]**.
 
   ![](assets/configure-calendar-widget.png)
   _Calendar widget customization screen, where administrators can set the widget title, description, and select catalogs_

4. Select a catalog by searching to display its courses and learning paths within the **[!UICONTROL Calendar]** widget.
5. Select **[!UICONTROL Add Widget]**.

The Calendar widget will be added to the page. Administrator can add other widgets and publish the page.

**Categories widget**

This widget displays categories (e.g., roles, catalogs) as tiles, leading to filtered views or specific pages.

To configure the Categories widget:

1. Follow steps 1-9 from the [Design page in Experience Builder](#design-page-in-experience-builder).  
2. Select **[!UICONTROL Categories]** and then select **[!UICONTROL Proceed]**. 
 
   ![](assets/select-categories-widget.png)
   _Widget selection screen highlighting the Categories widget option to organize learning content by catalog, product, or role for easy navigation_

3. Select the details to display on the category cards:

    * **[!UICONTROL Category Image]**
    * **[!UICONTROL Category Description]**

4. Type a **[!UICONTROL Widget title]** and **[!UICONTROL Widget description]**.
5. Search for and choose a catalog from the **[!UICONTROL Category source]**.
 
   ![](assets/configure-calendar-widget.png)
   _Configure Categories widget options to set widget title and description, and select the category source_

6. Select **[!UICONTROL Add Widget]**.

The Categories widget will be added to the page. Administrators can add other widgets and publish the page.

**Compliance widget**

This widget supports filtering similar to a calendar, but is focused on compliance-related learning objects. It allows learners to modify or remove compliance label filters dynamically.

To configure the Compliance widget:

1. Follow steps 1-9 from the [Design page in Experience Builder](#design-page-in-experience-builder).  
2. Select **[!UICONTROL Compliance Status]** and then select **[!UICONTROL Proceed]**.
 
   ![](assets/select-compliance-status.png)
   _Widget selection screen highlighting the Compliance Status widget used to display learner enrollments with deadlines and status indicators_

3. Type a **[!UICONTROL Widget title]** and **[!UICONTROL Widget description]**.
 
   ![](assets/configure-compliance.png)
   _Compliance Status widget screen, where administrators can set the widget title and description to display enrollment deadlines and status for learners_

4. Select **[!UICONTROL Add widget]**.

The Compliance status widget will be added to the page. Administrators can add other widgets and publish the page.

**Courses and paths widget**

This widget displays a strip of course or path tiles, customizable to show different details. 

To configure the Courses and Paths widget:

1. Follow steps 1-9 from the [Design page in Experience Builder](#design-page-in-experience-builder). 
2. Select **[!UICONTROL Courses & Paths]**.
 
   ![](assets/select-course-path.png)
   _Widget selection screen highlighting the Courses & Paths widget for displaying courses, learning paths, certifications, and job aids as interactive cards for learners_

3. Select **[!UICONTROL Proceed]**. 
4. Type **[!UICONTROL Widget title]** and **[!UICONTROL Widget description]**. 
5. Select the catalogs or manually choose up to 25 courses to display.
    
   ![](assets/configure-course-paths.png)
   _Courses & Paths widget where administrators set the widget title, description, and select courses or learning paths to display as interactive cards_

6. Select **[!UICONTROL Add widget]**. 

The Courses & Paths widget will be added to the page. Administrators can add other widgets and publish the page.

**Content Box widget**

This widget allows creating sections with titles, descriptions, images, and CTAs. 

To configure Content Box widget:

1. Follow steps 1-9 from the [Design page in Experience Builder](#design-page-in-experience-builder).
2. Select **[!UICONTROL Content Box]** and then select **[!UICONTROL Proceed]**. 
 
   ![](assets/select-content-box.png)
   _Widget selection screen highlighting the Content Box widget for displaying custom images, text, and action buttons to enhance learner engagement_

3. Type the **[!UICONTROL Title]** and **[!UICONTROL Description]**.
4. Type the text into the **[!UICONTROL Action button label]** and provide a link. 
5. Select any of the options for Background fill:

    * **[!UICONTROL Color]**: Select the color from the color picker or type the color code in the text field.
    * **[!UICONTROL Image]**: Browse and upload a picture.

6. Adjust the box height using the **[!UICONTROL Content box height]** option. 
7. Select the text formatting options.
 
   ![](assets/configure-content-box.png)
   _Content Box widget customization screen, where administrators can enter a title, description, action button label, and link_

8. Select **[!UICONTROL Add widgets]**. 

The Content Box widget will be added to the page. Administrators can add other widgets and publish the page.

**Gamification widget**

This widget shows gamification and points earned by learners in a leaderboard format. It has been updated for Experience Builder with a name, description, and localization customization.

To configure the Gamification widget:

1. Follow steps 1-9 from the [Design page in Experience Builder](#design-page-in-experience-builder).
2. Select **[!UICONTROL Gamification]** and then select **[!UICONTROL Proceed]**. 
 
   ![](assets/select-gamification.png)
   _Widget selection screen highlighting the Gamification widget used to display learning activities and achievements on the leaderboard_

3. Type the **[!UICONTROL Widget title]** and **[!UICONTROL Widget description]**. 
4. Select **[!UICONTROL Add widgets]**. 

The Gamification widget will be added to the page. Administrators can add other widgets and publish the page.

**HTML widget**

This widget allows custom HTML, CSS, and JS code to be embedded, providing flexibility for static content like testimonials. 

To configure the HTML widget:

1. Follow steps 1-9 from the [Design page in Experience Builder](#design-page-in-experience-builder).
2. Select **[!UICONTROL HTML]** and then select **[!UICONTROL Proceed]**. 
 
   ![](assets/select-html.png)
   _Widget selection screen highlighting the HTML widget for customizing pages using HTML, CSS, and JavaScript code_

3. Type your **[!UICONTROL HTML]**, **[!UICONTROL CSS]**, and **[!UICONTROL JavaScript]** code in the respective fields. 
4. Select **[!UICONTROL Add widget]**. 

The HTML widget will be added to the page. Administrators can add other widgets and publish the page.

**IFrame widget**

This widget allows embedding external web applications or webpages directly within the page. Includes options to name, describe, and localize the iframe content.

To configure the Iframe widget:

1. Follow steps 1-9 from the [Design page in Experience Builder](#design-page-in-experience-builder).
2. Select **[!UICONTROL Iframe]** and then select **[!UICONTROL Proceed]**. 
 
   ![](assets/select-iframe.png)
   _Widget selection screen highlighting the Iframe widget for embedding external applications or web pages within a selected section_

3. Type the URL in the **[!UICONTROL Page linked to Action button]** option.
4. Adjust the Iframe height using the **[!UICONTROL Iframe height]** option.     
 
   ![](assets/configure-iframe.png)
   _Iframe widget customization screen, where administrators can enter a page URL and specify iframe height to embed external content_

5. Select **[!UICONTROL Add widget]**. 

The Iframe widget will be added to the page. Administrators can add other widgets and publish the page.

**My Learning widget**

This widget is similar to the Courses and Paths widget, but filters content specifically for each learner, showing their personalized set of enrolled learning objects.

To configure the My Learning widget:

1. Follow steps 1-9 from the [Design page in Experience Builder](#design-page-in-experience-builder). 
2. Select **[!UICONTROL My Learning]** and then select **[!UICONTROL Proceed]**. 
 
   ![](assets/select-my-learning.png)
   _Widget selection screen, highlighting the My Learning widget used to display the learner's personalized list of enrolled courses_

3. Type the **[!UICONTROL Widget title]** and **[!UICONTROL Widget description]**.
4. Select **[!UICONTROL Add widget]**.

My Learning widget will be added to the page. Administrators can add other widgets and publish the page.

**Social Learning widget**

This widget enables social collaboration functionalities such as posts, comments, and user tagging within the platform. It is enhanced for Experience Builder with customization options, including name and localization.

To configure the Social Learning widget:

1. Follow steps 1-9 from the [Design page in Experience Builder](#design-page-in-experience-builder). 
2. Select **[!UICONTROL Social Learning]** and then select **[!UICONTROL Proceed]**. 
 
   ![](assets/select-social-learning.png) 
   _Widget selection screen highlighting the Social Learning widget for displaying a posts to encourage collaboration and engagement_

3. Type the **[!UICONTROL Widget title]** and **[!UICONTROL Widget description]**.
4. Select **[!UICONTROL Add widget]**. 

The Social Learning widget will be added to the page. Administrators can add other widgets and publish the page.

#### Organize pages into a menu

Menus help organize and link pages in Experience Builder, making it easy for learners to navigate your learning portal. Administrators can create menus, add pages to them, and customize which menus are shown to specific audiences. 

**Create a menu**

To create a menu:

1. Log in to Adobe Learning Manager as an administrator.
2. Select **[!UICONTROL Branding]** in the left navigation pane.
3. Select **[!UICONTROL Menu]** and then select **[!UICONTROL Create]**.
 
   ![](assets/select-create-menu.png)
   _Menu screen showing options to view, organize, and create customized menus for different learner groups_

4. Type the **[!UICONTROL Menu name]** (for example, Product Training) and select the user group in the **[!UICONTROL Visible to]** option.
   
   ![](assets/type-menu-name.png)
   _Create menu screen, where administrators can enter a menu name for internal use and specify user groups to control menu visibility_

5. Choose the custom page from the **[!UICONTROL Select pages]** option. 
 
   ![](assets/select-custom-pages.png)
   _Page selection screen, highlighting the option to include the custom page for user groups and customize the menu order_

6. Select **[!UICONTROL Preview menu]** to view the menu before saving it. 
7. Select **[!UICONTROL Save]**.

The created menu will be visible for the selected learners. They can access the custom pages through their Learner UI. 
 
![](assets/view-the-custom-pages.png)
_Learner UI displaying the custom page with featured training modules and easy navigation from the sidebar menu_

#### Manage pages lifecycle

Administrators can use the Custom Pages section to edit, delete, and duplicate the pages.

**Edit the page**

To edit the custom pages:

1. Log in to Adobe Learning Manager as an administrator.
2. Select **[!UICONTROL Branding]** in the left navigation pane.
3. Select **[!UICONTROL Custom Pages]**.
4. Select the required page and then select **[!UICONTROL Edit]**. 
5. Select **[!UICONTROL Save]**.

The page will be updated with the changes. 

![](assets/edit-the-page-custom.png)
_Edit the custom page, allowing administrators to update the page name, description, and type_

**Delete the page**

To delete the page:

1. Log in to Adobe Learning Manager as an administrator.
2. Select **[!UICONTROL Branding]** in the left navigation pane.
3. Select **[!UICONTROL Custom Pages]**.
4. Select the required page.
5. Select **[!UICONTROL Action]** and then select **[!UICONTROL Delete]**. 
 
![](assets/duplicate-the-page.png)
_Custom Pages screen displaying options to delete custom pages created for product training_

**Duplicate the page**

To duplicate the page:

1. Log in to Adobe Learning Manager as an administrator.
2. Select **[!UICONTROL Branding]** in the left navigation pane.
3. Select **[!UICONTROL Custom Pages]**.
4. Select the required page.
5. Select **[!UICONTROL Action]** and then select **[!UICONTROL Duplicate]**. 
 
![](assets/duplicate-the-page.png)
_Custom Pages screen displaying options to duplicate the custom pages created for product training_

#### Preview the pages

To preview the pages:

1. Log in to Adobe Learning Manager as an administrator.
2. Select **[!UICONTROL Branding]** in the left navigation pane.
3. Select **[!UICONTROL Custom Pages]**.
4. Select the required page and then select **[!UICONTROL Page Design]**
5. Select **[!UICONTROL Edit]** and then select **[!UICONTROL Preview page]** to view the portal's preview. 

![](assets/preview-page.png)
_Page preview showing a custom page layout with a banner, featured courses_

#### Localize the pages

When an admin adds multiple languages to the custom pages, add the widget details for each language in the corresponding language tab next to the default language tab.

![](assets/localize-pages.png) 
_Administrators can add widget details for additional languages, such as French, alongside the default language_

#### Set up hidden pages

The hide pages option allows administrators to keep the Learner UI clean by showing fewer pages. Administrators can hide pages from the menu so learners don't see them in learner UI, but learners can still reach those pages in other ways. For example, the Catalog page can be hidden from the menu but accessed through other navigation paths.
 
![](assets/select-hidden-pages.png)
_Menu configuration screen showing hidden pages such as Catalog, Social Learning, Skills, and Badges_ -->





<!-- We're excited to share several important updates coming to Adobe Learning Manager with the upcoming releases. These enhancements aim to streamline admin workflows, improve data reporting accuracy, and strengthen role-based controls.

These changes are designed to reduce manual effort, support automation, and improve governance across training operations.

## Capture instructor-marked completions in Learner Transcript

### Audience  

Administrator and automation owners 

### Overview 

In Adobe Learning Manager, when using incremental Learner Transcripts (LT) for automation workflows, instructor-marked completions made after the session date are not captured. The completion timestamp reflects the original session end time (not the time the instructor marked the completion). Since these updates fall outside the one-day change window used for incremental LT generation, as a result, learners' attendance and completion data are excluded from reports, leading to inaccurate or incomplete downstream reporting and potential compliance gaps. 

### What has changed 

Learner Transcript (LT) reports include completions marked by instructors after the session date. This ensures that any delayed attendance marking is correctly reflected in the transcript export. 

Attendance states like "Attended with pass/fail" will appear automatically in incremental LT exports. 

### What's new 

* New column: Mark Completed Date (UTC TimeZone). 
* Completion Source is available at module level. 
* Compatible with connector-based or job API-generated LT reports. 

![](assets/capture-instructor.png)

**Action required**

* If your automation depends on column positions, ensure logic accounts for the new column. 
* If using column names, no changes are required. 
* Retrofitted completions (manual imports) are not included. 

## Download links in Job Aids report

### Audience 

Administrator, custom administrator, and automation owners 

### Overview 

The Job Aids report includes a direct download link for each job aid, allowing quick access from the report itself. 

### What's new  

A new column, **[!UICONTROL Job Aid Link]**, has been added to the third position in the report. It links directly to the job aid if it's a file or shows the external URL provided by the author. 

Users with access (admin/authors and custom roles) can download the job aid using this link. 

![](assets/download-links-for-job-aid.png) 

### Action required 

* Review automated workflows using Job Aids reports (using Jobs API). 
* If the script is based on column position, update scripts accordingly. 
* No action is needed if using column names. 

## Internal User ID and Manager Email columns added to User Report

### Audience 

Administrators (and custom administrators) using the **[!UICONTROL User Report]** (**[!UICONTROL Admin]** > **[!UICONTROL Users]** > **[!UICONTROL Internal]** > **[!UICONTROL Export User data]**) downloaded from the administrator User Interface. 

### Overview 

To assist in user identification and integration workflows, two columns, **[!UICONTROL Internal User ID]** and **[!UICONTROL Manager Email]** have been added to the User report, exported via the User Interface. 

### What's new 

The User report includes a user's internal user ID and their manager's email address, to map them uniquely across different tools or API endpoints. 

### Action required 

* If using this report in automated flows, then this newly added column should be taken care of in automation.  
* No changes are needed if workflows are not impacted. 

## Scoped announcement permissions for custom administrators

### Audience 

Custom administrators 

### Overview 

Custom administrators can create announcements only for the user groups or catalogs within their defined scope. 

### What's new 

* Scoping rules allow custom administrators to create announcements for specific user groups or catalogs only. 
* When defining a custom role, administrators can assign announcement permissions with scope on user groups or catalogs. 
* Custom administrators are limited to creating announcements within their given scope. 
* The notification announcement report for custom administrators will display learners only within their assigned scope. 

### Action required 

* The format of the report will remain unchanged. If custom administrators download it from the User Interface, the content of the report will be subject to their scope. 
* No modifications are necessary if this report is not utilized in any automated or downstream workflow.

See the [Release notes](https://experienceleague.adobe.com/sv/docs/learning-manager/using/introduction/release-notes) article for a cumulative list of new features and changes to Adobe Learning Manager.-->
