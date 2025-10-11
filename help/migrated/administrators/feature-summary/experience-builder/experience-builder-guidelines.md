---
title: Riktlinjer och begränsningar för Experience Builder i Adobe Learning Manager
description: Experience Builder-riktlinjer och begränsningar ger elever personliga kurs- och innehållsförslag med AI-drivna algoritmer.
jcr-language: en-us
source-git-commit: b3124c47d56a50437cb284fe809828bcd4c4008d
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 0%

---


# Riktlinjer och begränsningar för Experience Builder

Experience Builder är ett kraftfullt verktyg som utformats för att hjälpa användare att enkelt skapa dynamiska och engagerande webbsidor. För att säkerställa optimala prestanda, användbarhet och säkerhet är det viktigt att följa vissa riktlinjer och rekommendationer när du konfigurerar sidor, använder widgetar och anpassar layouter. Det här dokumentet innehåller en detaljerad översikt över viktiga anteckningar och punkter som användare bör tänka på när de arbetar med Experience Builder.

Den information som beskrivs här täcker viktiga aspekter som sid- och widgetkonfigurationer, anpassningsalternativ, hantering av anpassad kod och säkerhetsaspekter. Genom att följa dessa rekommendationer kan användarna maximera effektiviteten i sina Experience Builder-projekt, undvika vanliga fallgropar och smidigt anpassa sig till uppdateringar och ändringar.

## Konfiguration av sidor och widgetar

### Maximalt antal sidor

Du kan skapa upp till 1 000 sidor i Experience Builder. Detta är den övre gränsen, men det rekommenderas att planera sidor strategiskt för att undvika onödig komplexitet.

### Widgetar per sida

* **Skarp gräns**: Högst 25 widgetar kan läggas till på en sida.
* **Rekommenderad gräns**: För bättre prestanda rekommenderar vi att du inte använder fler än 10 widgetar per sida.
* **API-baserade widgetar**: Widgets som är beroende av ALM API:er (t.ex. kurser och vägar, kategori, Min utbildning, Social utbildning, kalender, efterlevnad, resultattavla) bör vara begränsade till 10 per sida.
* **Oberoende widgetar**: Widgetar som HTML och rutan Innehåll, som inte är beroende av ALM-API:er, kan användas upp till den fasta gränsen på 25 widgetar.

### Widgetar för engångsbruk

Vissa widgetar, t.ex. Kalender, Social utbildning, Efterlevnad och Resultattavla, bör bara användas en gång per sida. Om du använder dem flera gånger kan det leda till prestandaproblem, särskilt för widgetar som kalendern, som kräver betydande resurser för att läsa in sessioner.

### Riktlinjer för storleksändring av widget

Widgetar som Kalender, Resultattavla, Social och Efterlevnad bör placeras i layouter med en minsta bredd på en tredjedel av sidan. Widgetar med ett enda kort är bäst lämpade för den här bredden för att säkerställa optimal visning. Widgetar som Kalender och Efterlevnad (utökad vy) är utformade för halvbreddslayouter för att erbjuda en bättre användarupplevelse. För andra layoutstorlekar kommer widgetar att justeras responsivt för att passa det tillgängliga utrymmet och bibehålla användbarheten.

Om du använder widgetar inom dessa rekommenderade riktlinjer för storlek förbättras användarinteraktionen generellt.

## Riktlinjer för anpassning

### Standardavstånd för pixlar

**Lodrätt avstånd**: Standardvärdet för lodrätt avstånd mellan widgetar är 80 pixlar.
**Horisontellt avstånd**: Standardvärdet för horisontellt avstånd mellan widgetar är 20 pixlar.

### Anpassad CSS

Användare kan åsidosätta standardavstånd och andra visuella egenskaper med anpassad CSS.

Steg för anpassning:

* Inspect sidelementen för att identifiera CSS-klasser.
* Tillämpa ändringar på global nivå, widgetnivå eller sidnivå.

Om du till exempel vill minska det vertikala avståndet mellan widgetar ändrar du CSS-egenskapen för den relevanta klassen.

## Menyplacering

Menyer finns högst upp eller till vänster på sidan. Ytterligare justeringar kan göras med anpassad CSS-kod.

## Funktionsspecifika rekommendationer

### Widgetar för social utbildning och spelifiering

* Om dessa funktioner är inaktiverade måste administratörerna ta bort motsvarande widgetar från sidorna manuellt.
* Sidorna bör utformas på nytt så att de förblir funktionella och visuellt intakta när dessa funktioner har inaktiverats.

## Hantera anpassad kod

### Effekten av uppdateringar

* Befintlig anpassad kod (HTML, CSS, JS) som injiceras i backend kanske inte fungerar som förväntat efter uppdateringar av Experience Builder.
* Användarna måste skriva om sin kod för att anpassa den till nya gränssnittsändringar, till exempel uppdaterade klassnamn.

### Stöd för frontend

* Lägg till anpassad kod direkt i administratörsportalen med hjälp av HTML-widgetar eller CSS/JS-block på kontonivå.

### Friskrivning

* Anpassad kod kanske inte fungerar som förväntat med framtida versioner, vilket kräver justeringar. Var beredd att uppdatera koden efter varje utgåva.

## Allmänna rekommendationer

### Prestandaöverväganden

* Undvik att överskrida de rekommenderade widgetgränserna för att förhindra prestandaförsämring.
* Om du använder resursintensiva widgetar (till exempel en kalender) flera gånger på en sida kan det påverka sidans inläsningstider avsevärt.

### Säkerhetsaspekter

* **HTML-widgetar**: Du måste se till att koden hanterar säkerhetsproblem som XSS-attacker (Cross-site Skript), eftersom de ligger utanför Experience Builders kontroll.
* **Anpassad sidfot**: Se till att HTML följer bästa säkerhetspraxis när du anpassar sidfoten med hjälp av CSS.

### Bryta ändringar

Uppdateringar av Experience Builder kan introducera brytningsändringar för anpassningar. Du måste

* Justera koden så att den matchar nya gränssnittselement.
* Testa anpassningarna efter varje uppdatering.

## Ytterligare information

### Anpassad CSS-implementering

* Du kan inspektera sidelement, kopiera CSS-klasser och tillämpa önskade egenskaper för att anpassa layouter globalt, på widgetnivå eller på sidnivå.

### Widget ID:n och sid-ID:n

Varje widget och sida har unika ID:n som kan användas för riktade CSS-ändringar. Detta möjliggör anpassning på olika nivåer:

* Global nivå: Tillämpa CSS-ändringar på alla sidor.
* Widgetnivå: Tillämpa CSS-ändringar på specifika widgetar.
* Sidnivå: Tillämpa CSS-ändringar på alla widgetar på en viss sida.










