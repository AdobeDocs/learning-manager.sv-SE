---
description: Elevens AI-assistent (beta) är en GenAI-driven chattföljeslagare i Adobe Learning Manager som hjälper elever att få snabba, korrekta svar från sitt tilldelade utbildningsinnehåll. Genom att använda naturliga språkfrågor kan elever omedelbart få fokuserade svar med tydliga citat, vilket gör det enkelt att hitta rätt information, verifiera källor och lära sig effektivt utan att söka igenom hela kurser.
jcr-language: en_us
title: Elev/AI-assistent (beta) i Adobe Learning Manager
exl-id: 8203488d-74a6-4463-9383-76d16cabccfa
source-git-commit: e009abe66258700cf28d3cf212a2d086689e179c
workflow-type: tm+mt
source-wordcount: '2150'
ht-degree: 0%

---

# Elevassistent

Elevens AI-assistent (beta) för elever hjälper dem att snabbt hitta svar från det tilldelade utbildningsinnehållet utan att bläddra igenom hela kurser. Du kan ställa frågor på ett enkelt språk och få korrekta, fokuserade svar med källänkar till relevant kursinnehåll.

>[!IMPORTANT]
>
>Elevens AI-assistent är för närvarande i betaversion och släpps genom en stegvis utrullning. Åtkomsten kan variera beroende på användare.


## Vad är Elevens AI-assistent?

Elevens AI-assistent är en GenAI-driven chattföljeslagare i Adobe Learning Manager som levererar snabba, korrekta svar på elevfrågor med hjälp av det betrodda utbildningsinnehåll som är tillgängligt för dem i Adobe Learning Manager. Det innehåller också citat, så att eleverna alltid vet källan till informationen.

## Varför använda den?

* Elever drabbas av innehållsöverbelastning och vet ofta inte var de ska börja eller vilken resurs de ska använda.

* Regler för katalog och åtkomst gör det svårt att identifiera vilket innehåll som är tillgängligt för dem.

* Utbildningsresorna är uppdelade i flera olika format och utbildningstyper, t.ex. kurser, virtuella klassrum, arbetsstöd och utvärderingar.

* Det finns inget enkelt och enhetligt sätt att hämta specifik information från olika format som SCORM, PDF, dokument, videoklipp eller utskrifter.

* Olika elevroller och branscher (t.ex. försäljning, marknadsföring, support, verksamhet) har unika informationsbehov som kräver snabba, kontextuella svar.

## Vilka typer av innehåll kan AI Assistant transkribera

AI-assistenten kan hitta information från alla typer av utbildningsinnehåll som tilldelats dig, inklusive:

* **Dokument:** PDF, Word, PowerPoint, Excel, HTML

* **Media:** Ljud (mp3, wav, m4a), video (mp4, mov, wmv)

* **Interaktivt innehåll:** SCORM 1.2, SCORM 2004,

* **Typ av utbildningsobjekt:** kurser, utbildningsvägar, certifieringar, arbetsstöd

Adobe transkriberar utbildningsinnehållet på ett säkert sätt med hjälp av betrodda externa bearbetningstjänster som tillhandahålls i Adobe privata VPC-miljöer.

**VIKTIGT**

AI-assistenten förbrukar bara innehåll som är:

* Tillgängligt i kataloger som konfigurerats för elevassistenten av administratörer

* Ingår i Adobe Learning Manager interna kataloger.

Delade, förvärvade, externa eller andra icke-interna kataloger stöds inte som innehållskällor för AI-assistenten i den aktuella versionen.

Om du inte har tillgång till en kurs kommer de relaterade citeringslänkarna inte att vara tillgängliga för dig. Bibliotek från tredje part (som LinkedIn Learning eller Go1) ingår inte för att hämta svar.

## Samtalsfunktioner

AI-assistenten stöder både enskilda frågor och flersidiga samtal. Det påminner om dina tidigare frågor under samma session.

**Exempel på konversation:**

Du: &quot;Vad är återbetalningspolicyn?&quot;
Assistent: tillhandahåller sammanfattning
Du: &quot;Vad händer med återbetalningar efter 30 dagar?&quot;
Assistent: Returnerar mer specifik information

## Användningsfall för AI-assistent

### Stöd för just-in-time-utbildning (alla elever)

Elever behöver ofta snabba svar när de arbetar, inte fullständiga kursrepriser. AI-assistenten gör det möjligt att omedelbart hämta exakt information från tilldelat utbildningsinnehåll.

**Vad det hjälper med:**

* Få direkta svar på specifika frågor från kurser, arbetsstöd och dokument

* Gå till exakta refererade avsnitt med hjälp av citat

* Minska tiden du lägger på att söka i flera utbildningsobjekt

![Stöd för just-in-time-utbildning med elevassistenten](assets/just-in-time.png)

### Försäljningsaktivering och kundkonversationer

Säljteamen behöver snabb, korrekt produkt- och processinformation under pågående kundinteraktioner. AI-assistenten fungerar som en kunskapsföljeslagare på begäran.

**Vad det hjälper med:**

* Hämta uppdaterade produktfunktioner och placering

* Generera snabba försäljningsskript eller samtalspunkter från utbildningsinnehåll

* Jämför produktversioner eller erbjudanden med hjälp av tilldelat utbildningsmaterial

* Förstärk dina säljkunskaper utan att behöva gå om hela kurser

![Försäljningsaktivering med elevassistenten](assets/sales-enablement.png)

**Exempel 2**

**Syfte:** Visa att AI-assistenten kan hjälpa säljare att svara på frågor om kundjämförelser direkt.

**Rekommenderad uppmaning:** Jämför Adobe Learning Manager och ett vanligt LMS för företagsutbildning. Visa jämförelsen i tabellformat.

![Tabellutdata i elevassistenten](assets/tabular-format.png)

### Marknadsförings- och kampanjberedskap

Marknadsföringsteam behöver ofta snabba uppdateringar innan de granskar, startar eller diskuterar med intressenter. AI-assistenten sammanfattar komplext utbildningsinnehåll i användbara insikter.

**Vad det hjälper med:**

* Sammanfatta långa kurser eller videor i viktiga hämtningar

* Uppdatera process- eller produktkunskaper före möten

* Upptäck relaterat utbildningsinnehåll för att fördjupa expertisen

![Marknadsförings- och kampanjberedskap med elevassistenten](assets/marketing-readiness.png)

### Förtydligande av drift och processer

Drift, support och interna team förlitar sig på korrekt processdokumentation. AI-assistenten hjälper till att klargöra policyer och arbetsflöden direkt.

**Vad det hjälper med:**

* Hitta svar om interna processer, standardförfaranden (SOP) och efterlevnadsriktlinjer

* Förtydliga detaljer på stegnivå utan att bläddra i långa dokument

* Minska beroendet av små och medelstora företag vid upprepade frågor

![Drifts- och processdokumentation med elevassistenten](assets/operational-process.png)

### Snabbare start- och rollövergångar

Nyanställda och anställda som går in i nya roller kämpar ofta med att navigera i stora utbildningskataloger. AI-assistenten påskyndar upptakten genom att vägleda dem till relevanta svar.

**Vad det hjälper med:**

* Svara på vanliga introduktionsfrågor från tilldelat innehåll

* Ge snabba förklaringar av rollspecifika begrepp

* Stöd självstyrd utbildning utan överbelastning av information

![Introduktion till anställda](assets/onboarding.png)

### Kunskapsuppdatering och kontinuerligt lärande

Erfarna elever behöver snabba uppdateringar snarare än fullständig omskolning. AI-assistenten stöder kontinuerlig utbildning i arbetsflödet.

**Vad det hjälper med:**

* Uppdatera kunskaper på begäran utan att gå om kurserna

* Förstärka utbildningsresultaten efter slutförd utbildning

* Uppmuntra frekventa, lågpresterande engagemang i utbildningsmaterial

![Kunskapsuppdateringssvar i elevassistenten](assets/knowledge-refresh.png)

## Så här använder elevens AI-assistent innehåll

Elevens AI-assistent hjälper dig att snabbt hitta korrekta svar medan du lär dig. Om du vill använda det på ett effektivt sätt bör du förstå vilket innehåll assistenten använder, vad den inte använder och hur den genererar svar.

### Vilket innehåll använder AI Assistant

Elevens AI-assistent besvarar frågor med hjälp av endast utbildningsinnehållet som har tilldelats dig i Adobe Learning Manager.

* Assistenten använder innehåll från interna kataloger som administratören aktiverar för elevens AI-assistent.

* Assistenten respekterar din roll, ditt gruppmedlemskap och dina katalogbehörigheter när information hämtas.

### Vilket innehåll använder inte AI-assistenten?

Elevens AI-assistent begränsar svaren till det utbildningsomfång som du har tilldelats.

* Den använder inte innehåll från standardkataloger, delade kataloger, förvärvade kataloger, externa kataloger eller andra icke-interna kataloger.

* Det hämtar inte information från externa innehållsbibliotek som LinkedIn Learning eller Go1.

* Den surfar inte på Internet och kommer inte åt externa webbplatser för att generera svar.

### Hur AI-assistenten genererar svar

Elevens AI-assistent analyserar ditt tilldelade utbildningsinnehåll för att generera fokuserade och sammanhangsberoende svar.

* Varje svar innehåller citat som refererar till det ursprungliga källinnehållet.

* Du kan välja ett citat för att komma direkt till den aktuella kursen, modulen eller dokumentet.

* Citat hjälper dig att verifiera information och utforska ytterligare sammanhang när det behövs.

### Använd AI-assistenten på ett ansvarsfullt sätt

Använd Elevens AI-assistent som ett hjälpmedel vid inlärning för att utforska, uppdatera och förstärka kunskaper.

* Behandla svar som vägledning baserat på tillgängligt utbildningsinnehåll.

* Se det citerade källmaterialet för fullständig och auktoritativ information.

### Så här kontrollerar administratörer åtkomst

Administratörer hanterar åtkomsten till elevens AI-assistent och kontrollerar innehållet som den använder.

* Administratörer tilldelar assistenten till specifika användargrupper.

* Administratörer väljer vilka interna kataloger som assistenten kan använda som innehållskällor.

* Dessa kontroller säkerställer att assistenten enbart tar fram godkänt och relevant utbildningsinnehåll.

## Inbyggda uppmaningar

Elevens AI-assistent innehåller en uppsättning inbyggda uppmaningar som hjälper elever att snabbt komma igång med vanliga frågor och scenarier. Dessa uppmaningar vägleder elever om hur de interagerar med assistenten och visar vilka typer av frågor de kan ställa.

![Inbyggda uppmaningar tillhandahålls av elevassistenten](assets/built-in-prompts.png)

Inbyggda uppmaningar är anpassningsbara per konto. Organisationer kan skräddarsy dessa ledord så att de återspeglar deras utbildningsmål, elevroller, terminologi eller specifika användningsfall.

Administratörer kan arbeta med sin CSM (Customer Success Manager) för att konfigurera, ändra eller uppdatera de inbyggda dialogrutorna för sina konton. Snabb anpassning hanteras på kontonivå och kan inte konfigureras direkt i Adobe Learning Manager-användargränssnittet i den aktuella versionen.

Uppmaningarna som visas för elever kan variera mellan olika konton beroende på vilken konfiguration som har definierats med Adobe.

## Aktivera elevens AI-assistent

![AI-aktiverad elevassistent](assets/learner-ai-assistant.png)

AI-assistenten (beta) tillhandahåller AI-drivet stöd för att hjälpa elever att upptäcka och hantera innehåll mer effektivt. Administratörer styr åtkomsten genom att tilldela funktionen till specifika användargrupper och kataloger. Endast interna kataloger ska användas när AI-assistenten konfigureras. Innehåll från delade, förvärvade, externa eller andra icke-interna kataloger stöds inte för ytan i AI-assistentens svar och citat.

Administratörer väljer vilka användargrupper och interna kataloger som får åtkomst till AI Assistant-funktionen. De bör se till att de kataloger som tilldelats endast innehåller det utbildningsinnehåll som är lämpligt för att visas genom AI-svar och -citat, och att dessa kataloger är interna, inte delade, förvärvade eller externa.

Innan du konfigurerar AI Assistant (beta) ska du bekräfta att du har administratörsuppgifter och har identifierat vilka användargrupper och kataloger som ska ha åtkomst till funktionen.

### Konfigurera åtkomst till elevassistenten

Så här aktiverar du elevens AI-assistent:

&#x200B;1. Logga in på Adobe Learning Manager som administratör.

2.Välj **Inställningar** på startsidan.

![Administratörskonsol med alternativet Inställningar i den vänstra rutan](assets/settings-menu.png)

&#x200B;3. Välj **Elevens AI-assistent (beta)** på menyn **Inställningar**.

![Administratörskonsolen visar alternativet Elevens AI-assistent i den vänstra rutan](assets/learner-assistant-ai-beta.png)

&#x200B;4. Välj växlingskontrollen för att aktivera **elevens AI-assistent (beta)**.

![Administratörskonsolen visar växlingsknappen aktiverad för elevens AI-assistent](assets/learner-assistant-toggle.png)

&#x200B;5. Välj en eller flera användargrupper bland de **kvalificerade användargrupperna**.

&#x200B;6. Välj **Spara** för att tillämpa användargruppsinställningarna.

&#x200B;7. Välj en eller flera kataloger från alternativet **Kataloger som är berättigade**.

&#x200B;8. Välj **Spara** för att tillämpa kataloginställningarna.

>[!IMPORTANT]
>
>AI-assistenten stöder bara interna kataloger. Om en delad, förvärvad, extern eller annan icke-intern katalog väljs kommer dess innehåll inte att visas av AI-assistenten, även om katalogen visas i listan över berättigade kataloger.

## Få åtkomst till elevens AI-assistent i Adobe Learning Manager

Adobe Learning Manager elevs-AI-assistent (beta) hjälper dig att hitta svar snabbt medan du lär dig. Det här intelligenta verktyget svarar direkt på dina frågor om kurser, innehåll och plattformsfunktioner, allt från ditt elevkonto.

AI-assistenten kan bara använda innehåll från interna kataloger som din administratör har aktiverat för elevassistenten. Innehåll som endast finns i Delade, Förvärvade eller Externa kataloger inkluderas inte.

Elevens AI-assistent (beta) är endast tillgänglig för utvalda elever.

### Starta AI-assistenten

Starta Elevers AI-assistent:

&#x200B;1. Logga in på Adobe Learning Manager som elev.

&#x200B;2. Välj **Fråga AI-assistenten** på startsidan.

![Elevens startsida visar Be AI-assistenten att välja och öppna Elevens AI-assistentpanel](assets/ask-ai-assistant.png)

&#x200B;3. När skärmen **Elevens AI-assistent (beta)** visas väljer du **Kom igång**.

![Välj Kom igång för att starta elevassistenten](assets/get-started-learner-assistant.png)

>[!NOTE]
>
>När du startar AI-assistenten för första gången måste du ge ditt samtycke innan du använder den. Dialogrutan för godkännande visas bara vid den första starten. Vid alla kommande starter tas du direkt till AI-assistenten för att ange dina ledord.

4.Skriv ditt ledord i textfältet.

![Skriv en uppmaning i elevassistenten](assets/type-prompt.png)

5.Tryck på **Enter** för att få ett svar. Granska svar, källor och rekommendationer.

Adobe tillåter omedelbar anpassning på kontonivå. Kontakta Adobe Customer Success Manager (CSM) om du vill konfigurera eller uppdatera inbyggda uppmaningar.

AI Assistant-svar inkluderar citat med varje svar så att eleverna enkelt kan verifiera var informationen kommer ifrån. Varje referens som citeras länkar tillbaka till den ursprungliga kursmodulen, arbetsstöd eller annat utbildningsinnehåll.

Elever kan:

* Välj citatnumret infogat för att gå till det exakta refererade avsnittet

* Öppna den fullständiga listan över källor genom att välja **Visa källor** längst ned i svaret

![Visa källor i svaret](assets/show-sources.png)

Elevassistenten innehåller citat med varje svar för att visa var informationen kommer ifrån. Varje citat länkar direkt till den ursprungliga kursen, modulen eller utbildningsobjektet som användes för att generera svaret.

Du kan välja vilken hänvisning som helst för att öppna den faktiska kurssidan i Adobe Learning Manager och granska hela innehållet i dess sammanhang. Citat hjälper dig att verifiera information, utforska ytterligare detaljer och fortsätta lära dig från den auktoritativa källan.

## Åtkomst till AI-assistenten med hjälp av sökning

Administratörer kan också starta AI-assistenten direkt från sökfältet. Skriv din fråga och välj **Fråga AI-assistenten** bland alternativen nedan för att få svar från det tilldelade utbildningsinnehållet.

![Gå till elevassistenten från sökfältet](assets/learner-assistant-search.png)

## Ge feedback på elevens AI-assistenters svar (beta)

Din feedback på svaren som genereras av elevens AI-assistent (beta) hjälper till att förbättra dess noggrannhet, relevans och övergripande prestanda.

### Gilla eller ogilla ett svar

* Välj **Tummen upp**, välj det som var till hjälp i svaret, lägg till kommentarer och välj sedan **Skicka**.

![Markera tummen upp för att rösta upp ett svar](assets/thumbs-up.png)

* Välj **Tummen ner**, välj anledningen till att svaret inte var till hjälp, lägg till kommentarer och välj sedan **Skicka**.

![Markera tummen ned om du vill nedrösta ett svar](assets/thumbs-down.png)

## Starta ny chatt i AI Assistant

Elever kan när som helst rensa den aktuella konversationen och starta en ny chatt.

* Välj **Ny chatt** på AI Assistant-skärmen och välj sedan **Ja**.

![Starta en ny chatt i elevassistenten](assets/start-new-chat.png)
