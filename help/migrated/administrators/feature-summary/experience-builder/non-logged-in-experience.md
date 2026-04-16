---
description: Förklarar hur Experience Builder kan publicera offentliga utbildningssidor och kataloger för anonyma besökare, inklusive nyckelfunktioner, widgetar som stöds, förutsättningar (Training Data Access Connector), begränsningar och vägledning för konfiguration, skalbarhet och migrering från den äldre, icke-inloggade startsidan.
jcr-language: en_us
title: Konfigurera och hantera sidor som inte är inloggade i Experience Builder
exl-id: e4685cab-08ca-4b6b-93f4-a9eecf382dc4
source-git-commit: 2f9e931523da6e3e1ed2cf60f1ad05f5caf3cc1b
workflow-type: tm+mt
source-wordcount: '6056'
ht-degree: 0%

---


# Upplevelser som inte är inloggade i Experience Builder

## Introduktion

Med den icke-inloggade upplevelsen i Experience Builder kan organisationer visa sitt utbildningsinnehåll och sina portalsidor för alla besökare, inklusive dem som inte har loggat in. Den här funktionen är utformad för att locka, informera och engagera blivande elever genom att erbjuda en smidig och varumärkt förhandsvisning av dina utbildningserbjudanden innan de måste logga in eller registrera sig.

Med den här funktionen kan du skapa och anpassa offentliga sidor med samma användarvänliga dra och släpp-gränssnitt som i Experience Builder. Du kan visa upp kurskataloger, kategorier, banor och avancerat statiskt innehåll, inklusive bilder, text, HTML och inbäddade iframes, för alla som besöker din portal. Det gör det enkelt att lyfta fram utbildningsprogram, främja nya kurser och ge viktig information till en bredare publik.

Besökare kan bläddra i katalogen, visa information om kurser och instanser och använda den globala sökningen för att utforska tillgängliga utbildningsmöjligheter. Åtgärder som kräver en användares identitet, till exempel att registrera sig för en kurs, komma åt anpassade funktioner (som kalender, efterlevnad, resultattavla eller social utbildning) eller att konsumera utbildning, kommer dock att uppmana besökaren att logga in. Detta tillvägagångssätt säkerställer att känslig och personlig information förblir säker samtidigt som det möjliggör en omfattande förhandsgranskning.

Administratörer har möjlighet att konfigurera vilka sidor och widgetar som är synliga för användare som inte är inloggade, vilket säkerställer att endast lämpligt innehåll visas. Sidorna kan ställas in så att de är tillgängliga för både inloggade och icke-inloggade användare, eller endast för en av dessa grupper. I Experience Builder finns ett förhandsgranskningsläge som du kan använda till att visa exakt hur sidorna kommer att visas för besökarna innan de publiceras.

ALM-integreringsadministratören måste aktivera Training Data Access Connector för att aktivera funktionen. Anslutningen ser till att kursmetadata är offentligt tillgängliga.

Varumärkning och lokalisering stöds fullt ut, vilket gör att du kan anpassa sidtitlar, favoritikoner och språkinställningar efter organisationens identitet och tillgodose målgruppens behov. Som en del av övergången till den förbättrade upplevelsen kommer den äldre startsidan för icke-inloggade användare att tas bort. Därför bör allt nytt offentligt innehåll skapas med Experience Builder.

## Funktionens syfte

Med den icke-inloggade upplevelsen i Experience Builder kan organisationer visa upp sitt utbildningsinnehåll och sina portalsidor för vem som helst utan att användarna behöver logga in. Detta hjälper till att locka, informera och engagera potentiella elever genom att tillhandahålla en förhandsvisning av tillgänglig utbildning och resurser innan registrering eller autentisering behövs.

## Verkliga användningsfall där ingen är inloggad

- **Marknadsföring och utåtriktad verksamhet**: Organisationer kan marknadsföra sina utbildningsprogram till externa målgrupper, t.ex. potentiella kunder, partner eller arbetssökande, genom att göra kurskataloger och programinformation offentligt tillgängliga.
- **Undersökning före registrering**: Elever kan bläddra bland tillgängliga kurser, visa översikter och utforska kategorier innan de bestämmer sig för att registrera sig eller logga in, vilket hjälper dem att fatta informerade beslut om registrering.
- **Företagsutbildningsportaler**: Företag kan tillhandahålla en offentlig portal för efterlevnad eller introduktionsinformation, så att nya anställda eller leverantörer kan se vilken utbildning som finns tillgänglig innan de får inloggningsuppgifter.
- **Landningssidor för evenemang eller kampanjer**: Organisationer som kör utbildningskampanjer eller evenemang kan skapa särskilda offentliga sidor för att framhäva utvalda kurser, scheman eller resurser, vilket ökar synligheten och engagemanget.
- **SEO och upptäckbarhet**: Genom att göra utvalda sidor och kataloger offentliga förbättrar organisationer sin sökmotorsynlighet, vilket gör det lättare för människor att upptäcka sina utbildningsalternativ online.

## Viktiga begrepp för icke-inloggad upplevelse

Med Experience Builders icke-inloggade upplevelse kan du offentligt visa upp utbildningsinnehåll och portalsidor, så att besökare kan bläddra utan att logga in.

- **Skapa offentliga sidor och menyer**: Du skapar sidor och en enda meny som alla har åtkomst till, oavsett inloggningsstatus.
- **Lägg bara till widgetar som stöds**: Du inkluderar widgetar som inte behöver användarkontext (kategorier, kurser och utbildningsvägar, innehållsruta, HTML, iframe), medan systemet döljer användarspecifika widgetar.
- **Konfigurera adaptivt sidbeteende**: Du avgör om en sida visas för både inloggade och icke inloggade användare och systemet anpassar synliga widgetar och innehåll baserat på inloggningsläget.
- **Förhandsgranska båda upplevelserna**: Du använder förhandsgranskningsalternativen för att se hur sidorna ser ut för inloggade och icke inloggade användare, med skillnader i widgetens synlighet och innehåll.
- **Aktivera global sökning**: Besökare söker efter kurser och innehåll, men får bara grundläggande sökfunktioner utan avancerad AI-integrering.
- **Låt besökare bläddra bland katalog- och kursöversikter**: Besökare utforskar katalogsidor, kursdetaljer och instanser, men måste logga in för att registrera sig eller få tillgång till personliga funktioner.
- **Anpassa varumärkning och lokalisering**: Du anger favoritikoner och språkinställningar som matchar organisationens varumärkes- och tillgänglighetsbehov.
- **Aktivera anslutningen för utbildningsdataåtkomst**: Du aktiverar den här anslutningen för att exportera kursmetadata för offentlig visning, vilket håller icke-inloggade sidor uppdaterade.
- **Hantera hög trafik med delad infrastruktur**: Systemet hanterar stora volymer av anonyma besökare med hjälp av delade resurser och hastighetsbegränsning.
- **Optimera för SEO**: Plattformen förbereder offentliga sidor för sökmotorindexering, vilket gör utbildningsinnehållet lättare att hitta.

## Förutsättningar för att inte vara inloggad

- Du måste aktivera Training Data Access Connector i integrationsadministratören innan du kan använda den icke-inloggade upplevelsen.
- Kopplingen exporterar kursmetadata till ett offentligt arkiv, vilket håller icke-inloggade sidor uppdaterade.

### TDA-anslutningsinitiering

Träningsdataåtkomstanslutningen (TDA) är en viktig förutsättning för att aktivera den nya icke-inloggade Experience Builder-funktionen i ALM. Anslutningen underlättar export av utbildningsmetadata, vilket gör att din portal kan visa kursinformation för användare som inte är inloggade.

- **Anslutningsaktivering**: Du måste aktivera TDA-anslutningen från panelen för integrationsadministratörer. Det här steget låser upp de funktioner i Experience Builder som inte är inloggade och gör relevanta gränssnittsalternativ synliga i administratörsgränssnittet.
- **Metadataexport**: När anslutningen har aktiverats exporteras viktiga utbildningsmetadata (t.ex. kursnamn, beskrivning, översikt, betyg, varaktighet och färdigheter) från ALM till ett offentligt arkiv. Dessa data används för att fylla i icke-inloggade sidor och widgetar.
- **Schemaläggning och synkronisering**: Exportprocessen kan schemaläggas (t.ex. varje dag) för att säkerställa att portalen återspeglar de senaste kursuppdateringarna. Ändringar som görs i ALM visas på icke-inloggade sidor efter nästa exportcykel, beroende på cache-lagring och exportfrekvens.
- **Funktionstillgänglighet**: De funktioner i Experience Builder som inte är inloggade, inklusive menyskapande, widgetstöd och katalogsynlighet, är bara tillgängliga efter att TDA-anslutningen har initierats. Om anslutningen inte är aktiverad förblir Experience Builder begränsat till inloggade användarscenarier.
- **Migrering och support**: För konton som övergår från äldre, icke-inloggade startsidafunktioner är initieringen av TDA-anslutningen det första steget mot migrering. Det garanterar att du kan utnyttja den nya Experience Builder-funktionen med dess flexibilitet och förbättrade funktioner.

## Vad besökare kan göra utan att logga in

På en webbplats som inte är inloggad Experience Builder kan besökare bläddra i utbildningskatalogen genom att öppna katalogsidan för offentliga kataloger. De kan använda filter som katalog, produkt, roll, typ, färdigheter och taggar beroende på hur du har konfigurerat platsen. Besökare kan också söka efter utbildningar med hjälp av det globala sökfältet i sidhuvudet (om det är aktiverat) och visa sökresultat direkt på katalogsidan.

Besökare kan visa utbildningsinformation genom att öppna översiktssidor för kurser, utbildningsvägar och certifieringar. Dessa sidor visar viktiga metadata, inklusive titel, beskrivning, författare, varaktighet, format, taggar och färdigheter.

Dessutom kan besökare utforska statiskt innehåll och reklaminnehåll. De kan läsa text och innehållsblock, visa banderoller och bildpaneler och interagera med inbäddade iFrame-objekt som externa mikrowebbplatser, videor eller verktyg.

Om en besökare klickar på Registrera dig eller försöker starta utbildning uppmanas hen att logga in eller registrera sig. Efter lyckad inloggning omdirigeras besökaren till rätt sida, oavsett om det är startsidan, en anpassad sida eller den specifika utbildning som de valt.

## Vad är inte tillgängligt utan att logga in

På en Experience Builder-webbplats som inte är inloggad kan besökare inte komma åt funktioner eller innehåll som kräver användarautentisering. De kan inte registrera sig för utbildningar, starta eller konsumera kurser eller komma åt personliga widgetar som Min utbildning, Kalender, Efterlevnad, Ledartavla eller Social utbildning. Dessa widgetar är beroende av användarspecifika data och är bara tillgängliga efter inloggning.

Besökare kan inte heller utföra åtgärder som att registrera sig för en kurs eller komma åt innehåll som kräver spårning av förlopp eller användarkontext. Om du försöker registrera dig eller starta en utbildning uppmanas besökaren att logga in eller registrera sig innan han/hon fortsätter.

## Widgetar som stöds i icke-inloggat läge

I icke-inloggat läge stöds endast widgetar som inte kräver användarspecifika data. Dessa omfattar:

- Kategorier, widget, som visar tillgängliga utbildningskategorier.
- Widgeten Kurser och banor som visar kurser och utbildningsvägar från den offentliga katalogen. 1
- Innehållsruta, för att lägga till statisk text, bilder eller kampanjinnehåll.
- HTML-widgeten för att bädda in anpassat HTML-innehåll.
- iFrame-widgeten, för att visa externa webbplatser, videor eller verktyg på sidan.
- Widgetar som kräver användarkontext, t.ex. Min utbildning, Kalender, Efterlevnad, Ledartavla och Social utbildning, är inte tillgängliga i icke-inloggat läge.

Widgetar som kräver användarkontext, t.ex. Min utbildning, Kalender, Efterlevnad, Ledartavla och Social utbildning, är inte tillgängliga i icke-inloggat läge

## Sidor och menyer som inte är inloggade

- Endast en meny som inte är inloggad stöds, och den är synlig för alla besökare utan autentisering.
- Sidor kan läggas till i både inloggade och icke-inloggade menyer. Om en sida finns på båda sidorna anpassas widgetarna och innehållet efter användarens inloggningsläge.
- Menyer som inte är inloggade har ingen målgruppsanpassning eller anpassning. Alla ser samma uppsättning sidor.
- Widgetar som inte stöds i icke-inloggat läge döljs automatiskt. Sidlayouten justeras för att fylla luckor.
- Meny- och sidhantering (lägga till, förhandsgranska, ta bort) fungerar som inloggat läge, men med anpassningar för begränsningar som inte är inloggade.

## Sök- och katalogbeteende

I icke-inloggat läge kan användare komma åt katalogsidan och använda sökning för att bläddra bland tillgängliga kurser och utbildningsvägar. Katalogsidan visar alla offentliga kurser, tillsammans med filter och sökfunktioner, med samma kontoinställningar som i inloggat läge. När en användare söker visas resultaten på katalogsidan, och användare kan visa kurs- och instansöversiktssidor utan att logga in. Åtgärder som registrering kräver dock inloggning.

Om en användare försöker registrera sig kräver systemet att användaren loggar in först. Sökningen efter icke-inloggade användare är enklare än den för inloggade användare och omfattar inte avancerade funktioner som AI Assistant-integrering.

## Tekniskt genomförande

### Konfiguration av anslutningen för utbildningsdataåtkomst

Du måste aktivera anslutningen för utbildningsdataåtkomst i panelen Integreringsadministratör innan du kan använda funktionen för Experience Builder som inte är inloggad. Med den här anslutningen exporteras utbildningsmetadata från ALM till ett offentligt arkiv, vilket gör det tillgängligt via API:er för sidor som inte är inloggade. Anslutningsinställningarna är en förutsättning för att aktivera funktionen och ser till att portalen visar aktuell utbildningsinformation.

Exportera och synkronisera metadata\
Kopplingen exporterar viktiga metadatafält som kursnamn, översikt, beskrivning, gradering, varaktighet och färdigheter. Du kan schemalägga exporter (till exempel dagligen) för att hålla din portal synkroniserad med ALM. Alla metadatafält kanske inte ingår. Kontakta den tekniska avdelningen för en fullständig lista. Exporterade data används för att fylla i sidor som inte är inloggade, och ändringar i ALM visas efter nästa exportcykel.

Frekvens för cachelagring och export\
Systemet använder backend-exportfrekvens och frontend-cachelagring för att hantera datauppdateringar. Ändringar som görs i ALM återspeglas i din portal efter den schemalagda exporten och cacheuppdateringen. Vissa uppdateringar kanske inte visas omedelbart på grund av dessa mekanismer. Om du behöver snabbare uppdateringar justerar du exportschemat eller rensar cachen efter behov.

Stöd för CSS/JS-anpassning\
Du kan använda anpassade CSS och JavaScript på både inloggade och icke-inloggade sidor med hjälp av fliken Anpassning. Detta gör att du kan upprätthålla en konsekvent varumärkning, lägga till anpassade användargränssnittselement och förbättra användarupplevelsen i hela portalen. Alla anpassningar tillämpas globalt, vilket säkerställer ett enhetligt utseende och känsla.

URL-skillnader och varumärkning (favicon, sidrubrik)\
Sidor som inte är inloggade och inloggade kan ha olika URL:er för att skilja mellan användartillstånd. Du kan anpassa favicon och sidtiteln för din portal, vilket stärker din varumärkesidentitet. De här funktionerna är tillgängliga i Experience Builder. Kontakta tekniker för senaste status om icke-inloggad support.

## Prestanda och skalbarhet

### Delad stack jämfört med premiumstack

Den delade stacken gör det möjligt för flera kunder att använda det icke-inloggade Experience Builder på gemensam infrastruktur, med stöd för standardtrafiknivåer. Premium-stacken är ett betalt alternativ som ger tillgång till dedikerade resurser, realtidsfunktioner och högre platsgränser för kunder med avancerade behov. Välj stack utifrån dina förväntade trafik- och affärskrav.

### Trafikbegränsningar och hastighetsbegränsningar

Den delade stacken tillämpar trafikbegränsningar för att säkerställa en rättvis användning bland kunderna. Teknikteamet implementerar hastighetsbegränsningar för att förhindra att en enskild kund förbrukar alla resurser. Om du planerar marknadsföringskampanjer eller förväntar dig mycket trafik ska du samordna dig med teknikerna för att förstå dina gränser och undvika avbrott i tjänsten. Hastighetsbegränsning hjälper till att upprätthålla systemets stabilitet och prestanda för alla användare.

Överväganden gällande multitenans och sökmotoroptimering\
Plattformen har stöd för flera klientorganisationer, vilket gör att flera kunder kan ha sina portaler på delade infrastrukturer. Sidor som inte är inloggade är SEO-vänliga, tillsammans med sitemap.xml och robots.txt för att optimera sökmotorsynligheten. Detta säkerställer att din portal kan upptäckas och indexeras på rätt sätt av sökmotorer.

## Migrering och borttagning

### Övergång från befintlig startsida som inte är inloggad

Den gamla startsidan som inte är inloggad tas bort. Nya konton ser inte det här alternativet, och befintliga konton som använder det meddelas om att migrera till den Experience Builder-baserade lösningen. Du bör återskapa din startsida med det nya Experience Builder för ökad flexibilitet, widgetstöd och förbättrad användarupplevelse. Övergångsplanen säkerställer minimala störningar och fortsatt stöd.

Kommunikationsplan\
Kunder som använder den äldre startsidan får tydlig information om tidslinjen för utfasningen och migreringsstegen. Stöd kommer att ges för att hjälpa dig att flytta din hemsida till den nya Experience Builder-plattformen, vilket säkerställer att du drar nytta av nya funktioner och pågående uppdateringar.

### Lokaliserings- och inloggningsstöd

Återställningslogik för språkinställning\
Sidor visas på det språk som de skapades på. Om en användares språkinställning inte är tillgänglig använder systemet en reservlogik för att välja nästa bästa tillgängliga språkinställning. Det garanterar att användarna alltid ser innehållet på ett språk som stöds, vilket förbättrar tillgängligheten och användarnas tillfredsställelse.

Inloggningstyper som stöds\
Den icke-inloggade upplevelsen har stöd för alla inloggningstyper i ALM, inklusive enkel inloggning och standardinloggning. Användare kan bläddra i innehåll utan att logga in och kommer att uppmanas att logga in när det behövs, till exempel för att registrera sig för en kurs eller komma åt personliga funktioner. Detta ger en smidig övergång från bläddring till engagemang.

## Icke-inloggade API:er

### API för utbildningsobjekt för admin

Icke-inloggade Experience Builder-sidor och fjärradministrerade portaler ordnar eller filtrerar ofta kurser baserat på produkt och roll. API:et för Admin LO har förbättrats för att säkerställa att dessa associationer är konsekvent tillgängliga för serverdelsintegreringar och fjärradministrerade integrationer samt för TDA-anslutningen.

**Slutpunkt och beteende**

Du fortsätter att använda den befintliga Admin LO-slutpunkten:

GET /primeapi/v2/learningObjects/{loId}?enforcedFields[learningObject]=products,roles


Där:

- loId är utbildningsobjektets ID (till exempel kurs:12345).
- enforcedFields[learningObject] instruerar API:t att uttryckligen inkludera produkter och roller för den LO:n.

Detta uppnås genom att säkerställa att LO:s produkt- och rollassociationer är närvarande i svaret när de begärs via enforcedFields. Svaret innehåller sedan, i attribut, de produkt- och rollmetadata som behövs för att beräkna eller visa de rekommenderade produkterna (rec_products) och rollerna (rec_roles) för Experience Builder och andra användare.

Ett vanligt samtal från en administratör eller integrering ser ut så här:

curl -X GET \
  &quot;https://{your-domain}/primeapi/v2/learningObjects/course:12345?enforcedFields[learningObject]=products,roles&quot; \
  -h &quot;Auktorisering: Innehavare {admin_token}&quot; \
  -H &quot;Acceptera: application/vnd.api+json&quot;

Den returnerade LO JSON är samma grundläggande struktur som tidigare, men nu kan du lita på att produkt-/rollfält är närvarande när du begär dem med enforcedFields. Integreringar som inte använder enforcedFields fortsätter att fungera som tidigare.

### Lista utbildningsobjekt - stöd för arbetsstöd i effectiveModifiedDate-filter

**Syfte**

Anslutningsprogrammet för utbildningsdataåtkomst (TDA) och fjärradministrerade implementeringar behöver ofta utföra inkrementell synkronisering baserat på utbildningsobjektens **effektiva ändringsdatum**. Fram till den här versionen hanterades inte arbetsstöd (LO-typ arbetsstöd) korrekt när det kombinerades med effectiveModifiedDate-filter. I den här versionen har det här korrigerats så att arbetsstöd kan synkroniseras stegvis precis som kurser och utbildningsvägar.

**Slutpunkt och beteende**

Du använder den befintliga slutpunkten för LO-listan med datumfilter och LO-typ:

GET /primeapi/v2/learningObjects\
?filter.effectiveModifiedDate.fromDate=2025-03-15T13:14:56.000Z\
&amp;filter.effectiveModifiedDate.toDate=2025-03-20T13:14:56.000Z\
&amp;filter.loTypes=jobAid


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
        "authorNames": ["Sid"],  
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
              { "id": "jobAid:144891_-1", "type": "learningObjectInstance" }  
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

### **Meny-API: Icke-inloggat menyfilter**

**Syfte**

Experience Builder och frontender utan huvud behöver ett enkelt sätt att hämta den **icke-inloggade menyn**, som definierar navigering för offentliga besökare. Innan den här versionen var du tvungen att hämta alla menyer och sedan använda anpassad logik för att identifiera vilken som representerade den icke-inloggade navigeringen. Den här versionen lägger till ett enkelt serverfilter.

**Slutpunkt och beteende**

Du använder den befintliga Menu-listan med slutpunkt med en ny frågeparameter:

GET /primeapi/v2/templates/menus?include=pages,subMenus.pages&amp;isNonLoggedIn=true


Huvudpunkterna är följande:

- include=pages,subMenus.pages är valfritt men rekommenderas när du behöver sid- och undermenysidinformationen i samma svar.
- isNonLoggedIn=true är ny i den här versionen och talar om för servern att endast returnera menyer som är flaggade som icke-inloggade menyer.

Utan parametern isNonLoggedIn fungerar slutpunkten exakt som förut och returnerar menyer enligt det befintliga standardbeteendet. Med isNonLoggedIn=true returnerar den vanligtvis den enda meny som används av den icke-inloggade upplevelsen för ditt konto (eftersom det normalt bara finns en icke-inloggad meny per konto).

I praktiken kan en kund nu utfärda:

curl -X GET \
  &quot;https://{your-domain}/primeapi/v2/templates/menus?include=pages,subMenus.pages&amp;isNonLoggedIn=true&quot; \
  -h &quot;Auktorisering: Innehavare {admin_token}&quot; \
  -H &quot;Acceptera: application/vnd.api+json&quot;


och få tillbaka den icke-inloggade navigeringsstrukturen i ett samtal, med alla sidor som bör vara synliga för anonyma besökare.

Detta är särskilt användbart när du skapar en webbplats som inte är inloggad och vill spegla samma navigering som Experience Builder använder eller när du felsöker om menyn som inte är inloggad har konfigurerats korrekt.

## Tillåt listning av anpassade domäner

Den icke-inloggade stacken består av:

- En offentlig CDN-domän (till exempel cpcontents.adobe.com eller yourdomain.example.com) som visar layouter, konfiguration-JSON och statiska resurser.
- En offentlig Elasticsearch-slutpunkt (ES) som betjänar katalog- och sökdata, men bara om begäran kommer från en **tillåten domän** för det ALM-kontot.

När du inför en anpassad domän fungerar den sömlöst utan extra ansträngning att följa den befintliga processen för att lägga till en anpassad domän.

### Förutsättningar

Innan du godkänner en anpassad domän som inte är inloggad:

1. Den anpassade domänen är konfigurerad för ditt ALM-konto (DNS för academy.yourcompany.com pekar till exempel på Adobe/Akamai och certifikat tillhandahålls).
2. Anslutningsprogrammet **Åtkomst till utbildningsdata (TDA)** har aktiverats för kontot.
3. Funktionen **Experience Builder som inte är inloggad** har aktiverats (Adobe).

Dessa steg säkerställer att:

- Ditt konto har en **konto-JSON** som inte är inloggad (kallas ofta accountConfig / experienceBuilderConfig) och som innehåller fält som cpDomain, almDomain, almCdnBaseUrl, esBaseUrl och domäner som tillåts.
- Den icke-inloggade stacken vet var data ska skickas och från vilka domäner begäranden ska godkännas.

### Hur tillåtelselista fungerar

Tillåtelselistan lagras i konfigurationen som TDA exporterar och stacken som inte är inloggad läses. Konfigurationen omfattar:

- ALM-domäner (cpDomain, almDomain).
- **URL-bas-URL:en** för innehåll som inte är inloggat (almCdnBaseUrl).
- URL:en **offentlig sökbas** (esBaseUrl).
- Listan över domäner som tillåts göra offentliga icke-inloggade anrop för det kontot.

För att Experience Builder som inte är inloggad ska fungera på en anpassad domän:

- Webbläsaren måste läsa in den icke-inloggade HTML från den anpassade domänen (eller från den ALM-icke-inloggade CDN-domänen, beroende på konfigurationen).
- Anrop från den domänen till offentliga ES- och CDN-slutpunkter måste accepteras. Det händer bara om domänen finns på listan med tillåtna domäner.

Den här versionen lägger till en ny CDN-domän, cpcontents.adobe.com, som inte är inloggad och anger att den måste placeras i de **tillåtna domänerna** i TDA-anslutningen. För befintliga interna användare som inte är inloggade krävs en uppdatering.

### Tillåt lista en anpassad domän

**Konfigurera den anpassade domänen i ALM**

Arbeta tillsammans med Adobe för att registrera din domän, t.ex. academy.yourcompany.com, som anpassad domän för ditt ALM-konto. Du uppdaterar DNS så att den pekar på Adobe Akamai enligt instruktionerna och väntar på att SSL och routning ska slutföras.

I det här läget kan både inloggad och icke-inloggad trafik nå ALM via den domänen, men icke-inloggade sök- och kataloganrop kan fortfarande blockeras om domänen inte är tillåten.

**Aktivera TDA och icke-inloggad Experience Builder**

Se till att:

- Anslutningen **Åtkomst till utbildningsdata** har aktiverats.
- Funktionen **Ej inloggad Experience Builder** är aktiverad för kontot.

Aktivering av TDA skapar eller uppdaterar JSON för det icke inloggade kontot. För nya konton tillåter processen även en lista över den nya CDN-domänen som inte är inloggad (cpcontent.adobe.com) som standard, så den offentliga ES-slutpunkten förväntar sig anrop från den domänen.

För konton som redan använde den äldre icke-inloggade stacken, anropar M45-specifikationen att befintliga anslutningar måste tas bort och återskapas för att hämta den nya domänen.

**Lägg till den anpassade domänen i listan över tillåtna domäner**

Den kritiska delen talar om för den icke-inloggade ES-stacken att academy.yourcompany.com är ett godkänt ursprung. Det finns två gemensamma vägar.

1. **Återaktivera TDA-anslutningen (enkel, självbetjäningsvänlig)**

Experience Builder M45 wiki förklarar att befintliga inbyggda icke-inloggade användare måste ta bort och återaktivera TDA-anslutningen så att den nya domänen automatiskt tillåts. Genom att göra detta uppnår du två saker:
1. JSON-kontot som inte är inloggat genereras om.
2. Domänerna på listan över tillåtna domäner uppdateras och inkluderar den nya CDN-domänen som inte är inloggad och din anpassade domän.

Detta rekommenderas när du har ett litet antal konton och kan tolerera att du tillfälligt inaktiverar och återaktiverar anslutningen.

1. **Kontrollera att domänen verkligen är tillåtelselistad**

Efter tillåt listning, öppna din icke-inloggade webbplats på den anpassade domänen och inspektera webbläsarens nätverksanrop.

Du vill se:

- Förfrågningar till almCdnBaseUrl (till exempel [https://cpcontent.adobe.com/](https://cpcontent.adobe.com/)...) med 200/304.
- Förfrågningar till esBaseUrl (offentligt sök-API, till exempel [https://primeapps.adobe.com/almsearch/api/v1/](https://primeapps.adobe.com/almsearch/api/v1/)...) JSON har returnerats med sök-/katalogdata.

Om dessa anrop returnerar 4xx eller explicita fel som föreslår &quot;ej betrodd domän&quot; eller &quot;ursprung ej tillåtet&quot;, är tillåtelselistan ofullständig eller felkonfigurerad och supporten måste justera den.

Den icke-inloggade LLD:n noterar också att kontokonfigurationen kan innehålla ett förväntat domänvärde. Vid körning kontrollerar webbplatsen att domänen i URL:en matchar det som angetts i konfigurationen. Om den inte gör det kan användaren omdirigeras till en felsida. Detta skyddar mot att en kunds konfiguration nås via en annan kunds domän.

## Använda rekommendationer i Experience Builder som inte är inloggad

Med den icke-inloggade Experience Builder kan du skapa offentliga utbildningssidor där besökare kan bläddra i din katalog och se markerat innehåll innan de loggar in. Även om dessa besökare är anonyma kan du ändå presentera rekommenderade utbildningar med hjälp av metadata och widgetar.

I den inloggade elevappen kan rekommendationer anpassas: de kan bero på elevens profil, historia, färdigheter och framsteg. I upplevelsen **Inte inloggad** finns det ingen elevidentitet än, så plattformen kan inte anpassa per användare.

Recommendations i icke-inloggat läge är därför:

- **Kurerat eller regelbaserat**: baserat på katalog, produkt, roll, etiketter, taggar och andra metadata.
- **Segmentorienterat**: &quot;rekommenderas för utvecklare&quot;, &quot;rekommenderas för partner&quot;, &quot;visas för nybörjare&quot;.
- **Marknadsföringsfokuserad**: Används för att locka och vägleda besökare som vill registrera sig när de loggar in.

### Metadata och API:er som stöder rekommendationer

Bakom kulisserna använder icke-inloggade sidor:

- **TDA-kopplingen** för att exportera metadata för utbildningsobjekt (kurser, vägar, certifieringar, arbetsstöd) till ett offentligt sökindex.
- Den **offentliga sökstacken** för att svara på frågor från icke-inloggade widgetar (katalog, sökning, kurser och sökvägar, kategorier).
- **API:et för Admin-utbildningsobjekt** för att visa produkt- och rollmetadata som kan användas för rekommendationsregler.

I den här versionen utökades API:et för Admin LO så att produkt- och rollassociationer är tillförlitligt tillgängliga:

GET /primeapi/v2/learningObjects/{loId}?enforcedFields[learningObject]=products,roles

Detta gör det möjligt för widgetar och rubrikfria integreringar att skapa regelbaserade rekommendationer med hjälp av produkter, roller, katalogetiketter, taggar och andra fält på ett konsekvent sätt.

### Utforma rekommendationsavsnitt med Experience Builder-widgetar

Du skapar rekommendationsavsnitt på icke-inloggade sidor genom att kombinera **Experience Builder-widgetar** med metadatafilter.

#### **Widget för kurser och banor**

Använd widgeten **Kurser och banor** när du vill visa en rad eller ett rutnät med rekommenderade objekt. I dess konfiguration kan du välja:

- Vilka kataloger att hämta från.
- Vilka katalogetiketter, produkter, roller eller taggar som ska användas som filter.
- Om du vill visa kurser, vägar, certifieringar, arbetsstöd eller en blandning.
- Sortering och maximalt antal objekt.

Du kan till exempel skapa

- &quot;Rekommenderas för utvecklare&quot;: Filtrera efter en produkt eller roll du använder för utvecklarinnehåll.
- &quot;Börja här&quot;: filtrera efter en etikett som &quot;Starter&quot; eller &quot;Onboarding&quot;.
- &quot;Utvalt det här kvartalet&quot;: filtreras av en tidsbunden etikett som utvalda-q3-2026.

Widgeten lär sig inte av beteendet utan visar det som matchar de metadataregler du definierar. Ur besökarens synvinkel ser det dock ut som en rekommendationsremsa.

#### **Kategoriwidget**

Använd widgeten **Kategorier** för att hjälpa besökare att navigera till rekommenderade uppsättningar innehåll, även om de inte känner till dina produktnamn.

Du kan konfigurera plattor som representerar ett segment, till exempel:

- &quot;För administratörer&quot;
- &quot;För säljteam&quot;
- &quot;För partner&quot;
- &quot;Efter produktlinje&quot;

Varje ruta kan länka antingen till:

- En filtrerad katalogsida (t.ex. den katalog som filtreras av vissa produkter eller etiketter).
- En dedikerad icke-inloggad sida som använder kurser och sökvägar som är förkonfigurerade för det segmentet.

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

## Hur arbetsstöd kan användas i den nya, icke-inloggade Experience Builder

I **användargränssnittet** deltar arbetsstöd i icke-inloggade upplevelser främst genom widgetar som kan visa utbildningsobjekt:

1. **Widget för kurser och banor**\
   Denna widget kan visa flera LO-typer, inklusive arbetsstöd. På sidor som inte är inloggade kan du konfigurera den för att:
   1. Inkludera eller exkludera arbetsstöd uttryckligen.
   2. Filtrera jobbhjälp efter katalog, produkt, roll, etiketter, taggar och andra metadata.
   3. Presentera dem tillsammans med kurser och vägar eller som en separat &quot;Resurser&quot; remsa.

På en offentlig landningssida kan du till exempel konfigurera en remsa med titeln &quot;Användbara resurser&quot; som endast visar arbetsstöd och en annan remsa med titeln &quot;Rekommenderade kurser&quot; som visar kurser och vägar.

1. **Katalogsida och sökning**\
   De **kataloger** och **sökytor som inte är inloggade använder det offentliga sökindexet (som matas av anslutningen för utbildningsdataåtkomst).** Indexet stöder nu arbetsstöd korrekt, så:
   1. Sökresultat som inte är inloggade kan innehålla arbetsstöd.
   2. Icke-inloggade katalogfilter (efter typ, produkt, taggar osv.) kan innehålla arbetsstöd så länge din kontokonfiguration och dina widgetar är inställda för att visa dem.
2. **LO-översiktssidor**\
   När en besökare klickar på ett arbetsstöd från en widget eller från katalogen visas en **LO-översiktssida** för det arbetsstödet i icke-inloggat läge. Därifrån kan de läsa dess beskrivning och metadata. Faktisk nedladdning eller konsumtion kräver vanligtvis fortfarande inloggning, men förekomst och upptäckbarhet av själva arbetsstödet hanteras av den icke-inloggade upplevelsen.

### Så här visas arbetsstöd via API:er som inte är inloggade

På **API-sidan** stöds arbetsstöd av:

1. Anslutningen **Åtkomst till utbildningsdata och offentlig sökning**\
   TDA exporterar arbetsstödsmetadata tillsammans med andra LO-typer till det offentliga sökindexet som hanterar icke-inloggade sök- och katalogfrågor. Det är vad Experience Builder och frontend utan fjärradministration är beroende av.
2. Listan **Utbildningsobjekt med effectiveModifiedDate**\
   I den här versionen korrigerades slutpunkten för LO-listan så att arbetsstöd fungerar korrekt med filtret effectiveModifiedDate. Du kan nu ringa:

GET /primeapi/v2/learningObjects\
?filter.effectiveModifiedDate.fromDate=2026-01-19T13:14:56.000Z\
&amp;filter.effectiveModifiedDate.toDate=2026-01-21T13:14:56.000Z\
&amp;filter.loTypes=jobAid


Före denna ändring returnerade inte arbetsstöd på ett tillförlitligt sätt genom att kombinera effectiveModifiedDate med loTypes=jobAid. Nu gör den det, vilket dokumenteras i den offentliga API-ändringen för *M45*-wiki. Detta innebär följande:

1. Dina TDA- eller ETL-jobb kan **stegvis synka arbetsstöd** för icke-inloggade upplevelser, på samma sätt som de gör för kurser och vägar.
2. Alla implementeringar utan huvud som bygger en offentlig arbetsstödskatalog kan fråga efter ändringar baserat på effectiveModifiedDate och loType=jobAid.

Exempelsvaret i M45-dokumentet visar ett learningObject med loType: &quot;jobAid&quot; och loFormat: &quot;Content&quot; returneras när det här mönstret används.

1. API:et **Admin LO**\
   M45 är inte specifikt för icke-inloggade men uppdaterar också API:t för administratörslogik för att konsekvent visa produkt- och rollmetadata för alla LO-typer via:

GET /primeapi/v2/learningObjects/{loId}?enforcedFields[learningObject]=products,roles


När det gäller arbetsstöd innebär det att du kan hantera deras produkt, roll, etiketter och taggar centralt och förlita dig på dessa metadata i offentliga, icke-inloggade upplevelser, till exempel i avsnitten &quot;Resurser för marknadsförare&quot; eller produktspecifika landningssidor.

**Anteckning**:

I icke-inloggat läge:

- Arbetsstöd kan främst **upptäckas**: besökare kan se att de finns, läsa beskrivningar och förstå hur de stöder ämnen eller kurser.
- Faktisk **förbrukning** (hämtning eller öppning av arbetsstödsinnehåll) kräver vanligtvis fortfarande inloggning, särskilt om arbetsstöd anses ingå i licensierat eller internt innehåll.

## Ändringar i &quot;kort beskrivning&quot; i LO-sökning (ej inloggad)

I stacken som inte är inloggad görs sökningar och listor över utbildningsobjekt (LO:er) med anslutningen Training Data Access (TDA) och ett offentligt Elasticsearch-index. Historiskt sett har denna stapel använt ett enda översikts-/beskrivningsfält för varje LO. Kunder som bygger huvudlösa icke-inloggade portaler ville visa samma korta beskrivning på LO-brickor som det inloggade elevgränssnittet visar, i stället för bara den långa översikten.

Ändringen introducerar stöd för LO **kort beskrivning** i icke-inloggade API:er för sökning och listning:

- För **kurser** är den befintliga gränssnittssemantiken:
   - Inloggade kort visar &quot;Kortfattad beskrivning&quot; (140 tecken långt fält) om det finns; annars faller de tillbaka till den långa &quot;Detaljerad översikt&quot;.
- För **utbildningsvägar** använder det inloggade användargränssnittet fältet Fördelar som kort beskrivning, om det har definierats, och återgår till översikten i annat fall.
- För **certifieringar** används en kort &quot;Beskrivning&quot; med en längre &quot;Certifieringsöversikt&quot; som reserv.
- För **arbetsstöd** används fältet för huvudbeskrivning.

## Andra ändringar

### Begränsning som innebär att inga två konton kan dela samma anpassade domän

I arkitekturer för inloggning och inloggning i Adobe Learning Manager behandlas en **anpassad domän** (t.ex. academy.example.com) som en globalt unik nyckel som måste mappas till exakt ett ALM-konto, så att plattformen tillämpar en fast begränsning som **inga två konton kan dela samma anpassade domän**. Detta krävs för säkerhet, routning och enkel inloggning: routningslagret och den icke-inloggade stacken använder domänen för att söka efter rätt kontokonfiguration (inklusive dess icke-inloggade konto-JSON, Experience Builder-menyer, varumärkning och TDA/sökslutpunkter).

Att tillåta samma anpassade domän på två konton skulle göra det omöjligt att garantera vilket kontos data returneras, orsaka läckage mellan klientorganisationer och även korrupta genererade artefakter som sitemap.xml och robots.txt som produceras per konto men upptäcks av sökmotorer per värd. Operativt innebär det att när du tilldelar eller flyttar en anpassad domän måste du först se till att den inte är kopplad till något annat konto (eller avregistrerar den där) och att Adobe interna verktyg avvisar försök att binda samma domän till flera konton.

### Webbläsarcachelagring av resurser i den icke-inloggade upplevelsen

I den icke-inloggade upplevelsen i Adobe Learning Manager är webbläsarcachelagring av resurser en kärndel av prestations- och storleksstrategin, eftersom offentliga sidor måste hantera stor, ibland taggig marknadsföringstrafik med låg latens och minimal ursprungslast. Statiska och halvstatiska resurser som det icke inloggade HTML-skalet (till exempel index.html/guest.html), konfiguration på kontonivå JSON (account.json eller config.json), Experience Builder-sidlayout JSON (menyer, widgetlayouter, kortinställningar), CSS, JS, bilder och favikoner hanteras från ett Akamai-CDN (cpcontents.adobe.com / cpcontent.adobe.com) med cacherubriker som uppmuntrar båda CDN-side och browser-side reuse, så att efter den första sidan ladda webbläsaren kan återge efterföljande icke-inloggade sidor till stor del från sin cache, omvalidera endast vid behov via ETag eller Last-Modified.

## Öppna alternativen för startsidan

På Adobe Learning Manager-startsidan väljer du **Varumärkning**. I den vänstra rutan väljer du sedan Ej inloggad startsida.

![Alternativ för startsida](/help/migrated/administrators/feature-summary/assets/non-logged-in-homepage.png)

*Välj alternativet Ej inloggad startsida*

## Lägg till en banderoll

Lägg till en banderoll för alla marknadsföringsmeddelanden eller visa dagens populära ämne. Välj **Lägg till banderoll**.

![banderoll](/help/migrated/administrators/feature-summary/assets/add-banner-image.png)

*Lägg till en banderoll*

Bläddra till platsen för bilden som ska användas som banderoll. Ange sedan en länk som en åtgärdsknapp på banderollbilden.

## Lägg till kategorier

Den här komponenten kan användas för att filtrera katalogen efter taggar, färdigheter och katalog. Detta avsnitt innehåller ett sidhuvud och en beskrivning för varje kategori. När användaren klickar omdirigeras användaren till katalogsidan med de filter som används.

Välj **[!UICONTROL Add category]**. Ange sedan information om kategorin.

![lägg till kategori](/help/migrated/administrators/feature-summary/assets//add-category.png)

*Lägg till kategorierna*

Spara kategorin. Kategorin läggs till i avsnittet.

## Lägg till en katalog

Lägg till en katalog för icke-inloggade användare så att de kan bläddra i all utbildning på plattformen.

![lägg till katalog](/help/migrated/administrators/feature-summary/assets//add-catalog.png)

*Lägg till en katalog*

All exporterad utbildning kommer att finnas.
