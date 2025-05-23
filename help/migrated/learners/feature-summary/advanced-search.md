---
jcr-language: en_us
title: AI-baserad sökning i Adobe Learning Manager
description: Läs mer om den AI-drivna sökningen i Adobe Learning Manager
exl-id: 9982a8be-b2e6-42a4-836a-7f9337588ae8
source-git-commit: 3c8bee8994ab13aacf8f4e1f4c9371f5808e17ce
workflow-type: tm+mt
source-wordcount: '1173'
ht-degree: 0%

---

# Avancerad AI-sökning i Adobe Learning Manager

Sökfunktionen i Adobe Learning Manager förbättrar användarupplevelsen genom att de kan hitta relevant innehåll effektivt och hjälpa dem att konsumera rätt innehåll.

Adobe Learning Manager introducerar en AI-driven sökfunktion som kombinerar lexikala och semantiska sökningar. Med den här förbättrade funktionen kan elever hitta relevant innehåll effektivt. Den avancerade AI-baserade sökningen förstår betydelsen av din fråga och ger relevanta resultat.

## Viktiga fördelar

* **Smartare sökning**: Förstår kontexten och avsikten bakom söktermer
* **Förbättrad relevans**: Ger resultat baserat på frågans betydelse
* **Förbättrad användarupplevelse**: Hjälper elever att konsumera rätt innehåll

>[!NOTE]
>
>AI-driven sökning är endast tillgänglig för elever.

## Varför är sökning viktigt?

Sökfunktionen är viktig av flera skäl:

* **Användarupplevelse**: Gör användaren nöjdare genom att aktivera snabb informationshämtning
* **Effektivitet**: Sparar tid genom att minska arbetet med att hitta specifikt innehåll.
* **Tillgänglighet**: Effektiva sökfunktioner gör information mer tillgänglig och gör att användarna kan interagera med innehåll som är relevant för deras behov.
* **Anpassning**: Avancerade söksystem kan skräddarsy resultat baserat på användarinställningar och på så sätt förbättra den presenterade informationens relevans.

## Nya sökfunktioner på webben

När människor söker på nätet förändras söksättet, och sökmotorerna anpassar sig för att hänga med. Detta är några av de viktigaste sätten som människor söker efter information på senare tid:

* **Avsiktsdriven**: I stället för att skriva exakta nyckelord uttrycker användarna nu sina behov med fraser som jag vill eller måste. Moderna sökmotorer förstår syftet bakom dessa fraser och ger mer relevanta resultat.
* **Rankade resultat**: Sökresultaten organiseras utifrån vad andra användare tyckte var till hjälp. Det innebär att det mest användbara innehållet visas högst upp, vilket gör det lättare att hitta kvalitetsinformation.
* **Flera källor**: Ju fler källor en sökmotor täcker, desto bättre resultat. Genom att hämta information från en mängd olika pålitliga källor, sökmotorer ger mer kompletta och exakta svar.
* **Anpassad**: Sökmotorer justerar resultat baserat på faktorer som tid, plats och användarinställningar. Detta gör det lättare för användarna att hitta information som passar deras specifika behov just nu.

## Varför är Adobe Learning Manager sökning bättre

Adobe Learning Manager är en smartare och mer avancerad sökfunktion. Den matchar inte bara nyckelord utan förstår också innebörden av användarfrågor för att hitta de mest relevanta resultaten.

* **AI-baserad**: Adobe Learning Manager använder avancerade AI-tekniker för att förstå innebörden bakom sökavsikten och inte bara orden. Detta hjälper till att visa resultat som verkligen matchar det användaren vill ha, vilket gör sökningar mer exakta.
* **Peer-Driven**: Adobe Learning Manager använder ett intervall av kurskvalitetsparametrar för att rangordna de mest användbara resultaten. Denna rangordningsalgoritm är utbildad i 50 miljoner datapunkter som regelbundet ger poäng för allt innehåll i databasen
* **Omfattande**: Adobe Learning Manager söker igenom hela biblioteket, inklusive eget innehåll, titlar på kurser från tredje part, beskrivningar, taggar, anpassade anteckningar och andra metadata. För innehåll som Video och PDF transkriberas och söks det automatiskt i transkriptionen.

## Adobe Learning Manager AI-drivna sökning

Adobe Learning Manager använder avancerad AI-teknik för att förbättra sökupplevelsen och göra det enklare att hitta relevant utbildningsinnehåll. Huvudkomponenterna i avancerad sökning beskrivs nedan.

### Identifiera nyckeltermer

Adobe Learning Manager använder NLP (Natural Language Processing) för att identifiera viktiga nyckelord från kurstitlar och beskrivningar. Sedan fokuseras det på dessa sökord för att ge bättre sökresultat, vilket hjälper till att förbättra resultaten med dessa sökord jämfört med andra resultat. Om en elev till exempel söker efter **Photoshop Basics** kommer Adobe Learning Manager att prioritera ordet **Photoshop** för att visa de mest relevanta kurserna.

![](assets/search-2.png)
_Prioritera nyckelordet_

I skärmbilden ovan söker en elev efter kurser med termen **Komma igång med Photoshop**. Sökningen prioriterar ordet **Photoshop** för att hitta de mest relevanta kurserna om **Photoshop**. För nyckelordet komma igång, det förstår avsikten och letar efter liknande ord för att visa de bästa matchningarna. På så sätt ser eleven kurser som fokuserar på Photoshop och lämpar sig för nybörjare.

### Expandera frågan

Adobe Learning Manager utvidgar användarfrågan till mer sammanhangsbaserad mening för att få bättre resultat. På så sätt får sökalgoritmen mer sammanhang tillsammans med användarfrågan. Även om elever använder allmänna termer kan de fortfarande hitta användbara resultat. Om en elev till exempel söker efter **kundtjänstgrunder** försöker den hitta nyckelordet från frågan och utöka resten av frågan till liknande fraser.

![](assets/search-1.png)
_Utöka frågan_

### Metadatasökning för kurs

Adobe Learning Manager metadatasökning omfattar metadata från både interna och importerade kurser (t.ex. från LinkedIn Learning eller Go1). Den här funktionen söker igenom dina kurstitlar, beskrivningar, taggar, anpassade anteckningar och andra metadata. Det hjälper till att göra resultaten bättre och mer exakta genom att använda många olika metadata för att hitta resultat.
Obs! Kunddata, inklusive innehåll och transkriberingar, delas inte med någon extern tjänst för AI-driven sökning. Allt innehåll lagras i det aktuella lagringssystemet.

#### Sökning i innehåll

Adobe Learning Manager har förbättrade sökfunktioner som gör att användare kan söka inom det faktiska innehållet i olika filtyper, inklusive videoklipp, ljudfiler, PDF, dokument, presentationer och kalkylblad. Systemet transkriberar automatiskt detta innehåll för att tillhandahålla mer omfattande och korrekta sökresultat. Dessutom ingår inspelningar från Adobe Connect-möten i sökningen, så att viktig information inte går förlorad. Om en matchning hittas i innehållet, höjer sökmodellen rangordningen för innehållet i slutresultaten. Den slutliga rankningen bestäms av flera faktorer, enligt beskrivningen i avsnittet [AI-driven sökning och omrankning](/help/migrated/learners/feature-summary/advanced-search.md#ai-powered-search-and-re-ranking).

>[!NOTE]
>
>Innehåll som nyligen lagts till, t.ex. videoklipp eller PDF, kommer att vara tillgängligt för sökning i innehållet efter en bearbetningsperiod på 24 timmar.

### Semantisk sökning

I Adobe Learning Manager ingår nu semantisk sökning tillsammans med vanlig lexikal sökning, vilket förbättrar sökresultatens exakthet. Genom att generera vektorinbäddningar från kurstitlar och beskrivningar skapas en omfattande vektordatabas. När en elev skickar en fråga vektoriserar systemet frågan och utför likhetsmatchning för att identifiera de mest relevanta resultaten. Om en elev till exempel söker efter en nybörjarkurs i Photoshop, förstår systemet begäran och hittar kurser som är särskilt användbara för Photoshop-nybörjare .

![](assets/semantic-search.png)
_Semantisk sökning_

>[!NOTE]
>
>Semantisk sökning stöder för närvarande endast engelskt innehåll.

### AI-driven sökning och omrankning

Adobe Learning Manager sökmotor leder branschen genom att kombinera traditionell och avancerad teknik. Den kombinerar traditionella sökmetoder som frasmatchning och avancerad semantisk sökning för att ge omfattande resultat. Systemet rankar dessa resultat baserat på nyckelfaktorer som registreringsnummer, publiceringsdatum, betyg och popularitet. Detta garanterar högkvalitativa matcher från alla index, vägledda av vår kurs kvalitet ranking system.

Generellt sett är AI-drivna sökningar utformade för att vara grundliga, korrekta och användarvänliga, vilket hjälper elever att snabbt hitta de resurser de behöver för att stödja sin utbildningsresa.

>[!NOTE]
>
>1. Kunder som använder en fjärradministrerad implementering måste följa API-dokumentationen för att aktivera avancerad sökning
>2. Avancerad sökning är för närvarande inte tillgängligt för Salesforce-programmet.
>3. Kunddata, inklusive innehåll och transkriptioner, delas inte med någon extern tjänst för AI-driven sökning. Allt innehåll lagras säkert i det befintliga lagringssystemet.
