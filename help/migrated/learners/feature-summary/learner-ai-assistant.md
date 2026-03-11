---
description: AI-assistenten (beta) för elever är en GenAI-driven chattföljeslagare i Adobe Learning Manager som hjälper elever att få snabba, korrekta svar från sitt tilldelade utbildningsinnehåll. Genom att använda naturliga språkfrågor kan elever omedelbart få fokuserade svar med tydliga citat, vilket gör det enkelt att hitta rätt information, verifiera källor och lära sig effektivt utan att söka igenom hela kurser.
jcr-language: en_us
title: AI-assistent för elever i Adobe Learning Manager
exl-id: 8203488d-74a6-4463-9383-76d16cabccfa
source-git-commit: 583074cf56b7c468d0027ea6bb4ed500f57e5421
workflow-type: tm+mt
source-wordcount: '1872'
ht-degree: 0%

---

# AI-assistent för elever

AI-assistenten (beta) för elever hjälper dem att snabbt hitta svar från det tilldelade utbildningsinnehållet utan att bläddra igenom hela kurser. Du kan ställa frågor på ett enkelt språk och få korrekta, fokuserade svar med källänkar till relevant kursinnehåll.

>[!IMPORTANT]
>
>AI Assistant för elever är för närvarande tillgänglig som en betafunktion. Funktioner, scenarier som stöds och begränsningar kan ändras allt eftersom funktionen utvecklas.


## Vad är AI-assistenten för elever

AI Assistant är en generativ AI-driven chattföljeslagare i Adobe Learning Manager som levererar snabba, exakta svar med hjälp av ditt betrodda utbildningsinnehåll. Det innehåller citat så att du alltid vet källan till informationen.

### Funktioner

- **Intelligent frågesvar**
   - Samtal med enkeltur och flersväng
   - Naturlig språkförståelse på engelska
   - Svar från kurser, certifieringar, utbildningsvägar och arbetsstöd
   - Smarta klarlägganden av frågor när frågorna är tvetydiga

- **Innehållskällor och citat**
   - Hämtar svar från tillgängliga resurser i kataloger som stöds
   - Tillhandahåller citat med direkta länkar till källmaterial
   - Stöder alla Learning Manager-innehållsformat (statiska och interaktiva): PDF, DOCX, PPTX, XLSX, ljud (MP3, WAV, M4A), video (MP4, MOV, WMV), HTML, SCORM 2004 och SCORM 1.2

- **Användarupplevelse**
   - Gränssnitt för sidopanel från alla elevsidor
   - Responsiv design som anpassar sig till innehållsområdet
   - Chatthistorik bibehållen i webbläsarsessionen
   - Rensa platta vid ny inloggning eller siduppdatering
   - Vänlig, tydlig och pedagogiskt sund ton

- **Administratörskontroller**
   - Aktivera eller inaktivera funktionen på kontonivån
   - Kontrollera åtkomst för användargrupper
   - Välj vilka kataloger som ska ingå i AI-svar
   - Godkännandekrav för användningsvillkor enligt Adobe AI-riktlinjer

## Innehållstyper som stöds

AI-assistenten hämtar information från utbildningsinnehåll som tilldelats dig, inklusive:

- **Dokument:** PDF, Word, PowerPoint, Excel, HTML
- **Media:** Ljud (MP3, WAV, M4A), video (MP4, MOV, WMV)
- **Interaktivt innehåll:** SCORM 1.2, SCORM 2004
- **Typer av utbildningsobjekt:** Kurser, utbildningsvägar, certifieringar, arbetsstöd

Adobe behandlar ditt utbildningsinnehåll på ett säkert sätt med hjälp av betrodda tjänster.

### Begränsningar för kataloger och innehållskällor

AI-assistenten använder bara innehåll från **interna** kataloger som uttryckligen har konfigurerats av administratörer.

Följande innehållskällor stöds inte i den aktuella versionen:

- **Delade** kataloger
- **Förvärvade** kataloger
- **Externa** kataloger
- **Standardkataloger**
- Innehållsbibliotek från tredje part (t.ex. LinkedIn Learning eller Go1)

Om du inte har tillgång till en kurs eller ett arbetsstöd kommer AI-assistenten inte att hitta information från det innehållet, och citationslänkar kommer inte att vara tillgängliga.

## Användningsfall

### Teknisk elev

Sarah är en försäljningsingenjör som lär sig mer om grafikkort. Hon behöver snabbt förstå de tekniska specifikationerna och fördelarna för att kunna svara på kundernas frågor med tillförsikt.

AI Assistant hjälper Sarah med:

- Tydlig, teknisk förklaring av komplex GPU-arkitektur
- Fördjupa förståelsen för olika grafikkort och deras olikheter
- Förklaring av exempel så att Sarah kan relatera funktioner till verkliga användningsfall

### Kundsupport

Marcus är supportspecialist på ett partnerföretag. Han behöver snabba svar om produktfunktioner för att hjälpa kunder utan att eskalera till teknikerteam.

AI Assistant hjälper Marcus med:

- Hitta relevant supportinnehåll för vanliga kundfrågor
- Ställa frågor som klargör när det ursprungliga svaret inte är tillräckligt specifikt
- Hitta rekommendationer för relaterade felsökningskurser för att förbättra sina färdigheter

### Ny medarbetarintroduktion

Jennifer har precis gått med i företaget och är överväldigad av mängden utbildningsmaterial. Hon behöver ett sätt att hitta specifik information utan att gå igenom hela kurser.

AI Assistant hjälper Jennifer med:

- Få stegvisa anvisningar om att skicka in utgiftsrapporter
- Upptäck kurser om företagspolicyer utan att bläddra i hela katalogen
- Fäst henne vid rätt avsnitt av en kurs utan att göra henne titta på timmar av video

## Hur AI-assistenten använder innehåll

AI-assistenten hittar korrekta svar från ditt utbildningsinnehåll. Så här fungerar det.

### Vilket innehåll använder AI-assistenten

AI-assistenten besvarar frågor med enbart det utbildningsinnehåll som aktiverats av kontoadministratören. Innehåll från de valda katalogerna indexeras.

AI-assistenten analyserar ditt tilldelade utbildningsinnehåll för att generera fokuserade, sammanhangsberoende svar:

- Varje svar innehåller citat som refererar till det ursprungliga källinnehållet.
- Du kan välja ett citat för att komma direkt till den aktuella kursen, modulen eller dokumentet.
- Citat hjälper dig att verifiera information och utforska ytterligare sammanhang när det behövs.

### Strömmande svar

AI-assistenten levererar svaren progressivt allteftersom de genereras, så att du kan börja läsa direkt utan att vänta på att hela svaret läses in.

### Citat och källgenomskinlighet

Varje AI Assistant-svar innehåller citat som länkar direkt till den ursprungliga kursen, modulen eller utbildningsobjektet. Med citat kan du:

- Välj ett infogat citattecken om du vill gå till det exakta avsnittet som refereras.
- Öppna den fullständiga källistan genom att välja **Visa källor** längst ned i svaret.
- Verifiera information och utforska ytterligare sammanhang från den auktoritativa källan.

> **VIKTIGT**
> AI Assistant ger svar baserat på innehåll som aktiverats av administratören. Om du inte har tillgång till ett refererat objekt visas meddelandet &quot;stöds inte&quot; när du försöker öppna det.


## Inbyggda uppmaningar

AI-assistenten innehåller inbyggda uppmaningar som hjälper dig att snabbt komma igång med vanliga frågor och scenarier. De här anvisningarna visar hur du interagerar med assistenten och visar vilka typer av frågor du kan ställa.

![Inbyggda uppmaningar tillhandahålls av elevassistenten](assets/built-in-prompt-new.png)

Organisationer kan anpassa inbyggda uppmaningar som återspeglar deras utbildningsmål, roller, terminologi eller specifika användningsfall. Administratörer kan arbeta med sina Customer Success Manager för att konfigurera eller uppdatera inbyggda uppmaningar. I den aktuella versionen kan du inte anpassa uppmaningar direkt i Adobe Learning Manager-gränssnittet.

## Konfigurera AI-assistenten (administratörer)

![AI-aktiverad elevassistent](assets/learner-ai-assistant-new.png)

Administratörer väljer vilka användargrupper och **interna** kataloger som ska ha åtkomst till AI Assistant-funktionen. Se till att katalogerna du tilldelar endast innehåller utbildningsinnehåll som är lämpligt för AI-svar och -citat och att katalogerna är **interna** (inte **delade**, **förvärvade** eller **externa**).

Innan du konfigurerar AI Assistant måste du bekräfta att du har administratörsuppgifter och har identifierat vilka användargrupper och kataloger som ska ha åtkomst.

### Konfigurera åtkomst till AI Assistant

Så här aktiverar du elevens AI-assistent:

1. Logga in på Adobe Learning Manager som administratör.

2. Välj **Inställningar** på startsidan.
   ![Administratörskonsol med alternativet Inställningar i den vänstra rutan](assets/settings-menu.png)

3. Välj **Elevens AI-assistent (beta)** på menyn **Inställningar**.
   ![Administratörskonsolen visar alternativet Elevens AI-assistent i den vänstra rutan](assets/learner-assistant-ai-beta.png)

4. Välj växlingsfunktionen för att aktivera **elevens AI-assistent (beta)**.
   ![Administratörskonsolen visar växlingsknappen aktiverad för elevens AI-assistent](assets/learner-assistant-toggle.png)

5. Välj en eller flera användargrupper från alternativet **Kvalificerade användargrupper**.

6. Välj **Spara** för att tillämpa inställningarna för användargruppen.

7. Välj en eller flera kataloger från alternativet **Kataloger som är berättigade**.

8. Välj **Spara** för att tillämpa kataloginställningarna.

>[!IMPORTANT]
>
>Endast **interna** kataloger stöds. Om en **delad**, **förvärvad**, **extern** eller annan icke-intern katalog väljs, kommer dess innehåll inte att visas av AI-assistenten, även om den visas i listan **Kataloger som är berättigade**.

## Starta AI-assistenten (elever)

Så här startar du AI-assistenten:

1. Logga in på Adobe Learning Manager som elev.

2. Välj **Fråga AI-assistenten** på startsidan.
   ![Elevens startsida visar Be AI-assistenten att välja och öppna Elevens AI-assistentpanel](assets/ask-ai-assistant.png)

3. När skärmen **Elevens AI-assistent** visas väljer du **Kom igång**.
   ![Välj Kom igång för att starta elevassistenten](assets/get-started-learner-assistant.png)

>[!NOTE]
>
>När du startar AI-assistenten för första gången måste du ge ditt samtycke innan du använder den. Dialogrutan för godkännande visas bara vid den första starten. Vid alla kommande starter tas du direkt till AI-assistenten för att ange dina ledord.

4.Skriv ditt ledord i textfältet.
<!-- ![Type prompt in the Learner Assistant](assets/type-prompt-new.png) -->

5.Tryck på **Enter** för att få ett svar. Granska svar, källor och rekommendationer.

Du kan:

- Välj citatnumret infogat för att gå till det exakta refererade avsnittet
- Öppna den fullständiga listan över källor genom att välja **Visa källor** längst ned i svaret

![Visa källor i svaret](assets/show-sources-latest.png)

AI Assistant innehåller citat med varje svar för att visa var informationen kommer ifrån. Varje citat länkar direkt till den ursprungliga kursen, modulen eller utbildningsobjektet som användes för att generera svaret.

Du kan markera valfritt citat för att öppna kurssidan i Adobe Learning Manager och granska hela innehållet i dess sammanhang. Citat hjälper dig att verifiera information, utforska ytterligare detaljer och fortsätta lära dig från den auktoritativa källan.

## Åtkomst till AI-assistenten via sökning

Du kan också starta AI-assistenten direkt från sökfältet. Skriv frågan i sökfältet och välj sedan **Fråga AI-assistenten** bland alternativen som visas.

![Gå till elevassistenten från sökfältet](assets/learner-assistant-search-new.png)

## Ge feedback på AI-assistentens svar

Din feedback på svaren som genereras av AI-assistenten (beta) hjälper till att förbättra dess noggrannhet, relevans och övergripande prestanda.

### Gilla eller ogilla ett svar

- Välj **Tummen upp**, välj det som var till hjälp i svaret, lägg till kommentarer och välj sedan **Skicka**.
- Välj **Tummen ner**, välj anledningen till att svaret inte var till hjälp, lägg till kommentarer och välj sedan **Skicka**.

## Börja chatta

Genom att starta en ny chatt kan du börja en ny konversation, rensa tidigare sammanhang så att assistenten kan fokusera på det nya ämnet utan att referera till tidigare interaktioner.

Om du vill rensa den aktuella konversationen och börja om väljer du **Ny chatt** på skärmen AI-assistent och väljer sedan **Ja**.

![Starta en ny chatt i elevassistenten](assets/start-new-chat.png)

AI-assistenten ger elever snabba, sammanhangsberoende svar, stöder flera innehållstyper och erbjuder infogade citat för genomskinlighet. Administratörer kan kontrollera åtkomsten, vilket säkerställer att AI-assistenten är anpassad till organisationens behov och förbättrar utbildningsupplevelsen.


## Felsöka problem med AI-assistenten

> **ANTECKNING**
> När du har konfigurerat en ny katalog kan du vänta 4-5 timmar tills innehållet är indexerat och tillgängligt för AI Assistant-svar.

### Ingen åtkomst till innehåll

**Problem:** En elev har åtkomst till AI-assistenten men får svaret &quot;Jag har inget svar på den här frågan&quot;.

**Möjliga orsaker:**

- Elevens kataloger ingår inte i AI Assistant-konfigurationen.
- Innehåll relaterat till frågan finns inte i de valda katalogerna eller så är katalogerna tomma.
- Eleven har inte synlighet för det relevanta innehållet.

**Lösning:**

- Kontrollera elevens katalogåtkomst.
- Kontrollera vilka kataloger som är aktiverade i AI Assistant-inställningarna.
- Se till att det finns relevant innehåll i dessa kataloger.
- Vänta några timmar efter att du har lagt till nytt innehåll innan du indexerar det.

### Irrelevanta svar eller svar av dålig kvalitet

**Problem:** AI-assistenten ger svar som inte matchar frågan eller har låg kvalitet.

**Möjliga orsaker:**

- Frågan är för bred eller tvetydig.
- Relevant innehåll har dåliga metadata (beskrivningar, taggar).
- Innehållsstrukturen gör det svårt att extrahera information.

**Lösning:**

- Uppmuntra elever att ställa mer specifika frågor.
- Granska och förbättra kursbeskrivningar och metadata.
- Se till att innehållet har tydliga rubriker och strukturer.
- Granska den detaljerade användningsrapporten för att identifiera mönster.
- Överväg att skapa arbetsstöd för vanliga frågor.

### Frågor som inte omfattas

**Problem:** En elev ställer frågor som inte har med utbildningsinnehåll att göra.

**Exempel:**

- Allmänna kunskapsfrågor (&quot;Vem är presidenten?&quot;)
- Personliga åsikter (&quot;Vad tycker du om X?&quot;)
- Olämpligt innehåll

AI-assistenten är utformad för att svara på frågor som endast baseras på tilldelat utbildningsinnehåll och svarar inte på frågor som inte omfattas.
