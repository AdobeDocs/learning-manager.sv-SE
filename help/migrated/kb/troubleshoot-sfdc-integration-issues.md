---
jcr-language: en_us
title: Felsöka problem med Salesforce-integrering (SFDC) med Adobe Learning Manager
description: felsöka vanliga problem med Salesforce-integrering (SFDC) med Adobe Learning Manager (ALM), inklusive misslyckade exporter, fältbehörighetsproblem i SFDC-anpassade objekt och viktiga kompatibilitetsanteckningar för SFDC-ALM.
contentowner: saghosh
source-git-commit: cedb4acc89e7d972a4752e10c4fb6930c4633f6a
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---


# Felsöka problem med Salesforce-integrering (SFDC) med Adobe Learning Manager

## Felsöka SFDC-exportfel (ingen export under mer än 2-3 timmar)

Om SFDC-exporten inte har slutförts på mer än **2-3 timmar** kan du använda stegen nedan för att identifiera och förstå problemet.

1. Gå till sidan **Salesforce-startsida**.
2. Skriv **i sökrutan** Snabbsökning **`Bulk Data Load Jobs`** och öppna den.
3. Sidan visar massdatainläsningsjobb för de **senaste sju dagarna**.
4. Leta efter jobb som är relaterade till **Adobe Learning Manager-objekt (ALM)**.
5. Klicka på det jobb som du vill undersöka.
6. Bläddra till den **nedre** delen av jobbdetaljsidan för att visa **felmeddelandet** och ytterligare information.

I många fall är grundorsaken **otillräckliga behörigheter på fältnivå i SFDC**. Det misslyckade fältnamnet kan se ut så här:

- `cp_Module_ID`
- eller andra `cp_...`-fält relaterade till anpassade ALM-objekt.

Om sådana fält visas i felmeddelandet fortsätter du till nästa avsnitt.

## Bevilja fältbehörigheter i anpassade ALM-objektfält i SFDC

Använd funktionen **Fälttillgänglighet** för att åtgärda behörighetsproblem för specifika fält (till exempel `cp_Module_ID`).

### Steg

1. Gå till sidan **Salesforce-startsida**.
2. Skriv **i sökrutan** Snabbsökning **`Field Accessibility`** och öppna den.
3. I listan med objekt väljer du relevant **rapporttyp/objekt**.
   - Exempel: `cp_LearnerTranscript_xxxx_xxxx` för rapporten Elevens betygsutdrag (LT).
4. Välj **&quot;Visa efter fält&quot;** på nästa sida.
5. I listrutan **fält** väljer du fältet som visas i exportfelet
   - Exempel: `cp_Module_ID`.
6. Klicka på posten **&quot;Dold&quot;** i åtkomstmatrisen för profilen **Systemadministratör** (och andra relevanta profiler, om det behövs).
7. På nästa sida:
   - Aktivera **&quot;Synlig&quot;** när så är lämpligt.
   - Klicka på **Spara** längst ned på sidan.
8. När du har sparat återgår du till vyn för fälttillgänglighet. Fältet ska nu visas som **&quot;Redigerbar&quot;** för **Systemadministratör** (och alla andra profiler som du har uppdaterat).

## Upprepa för alla berörda fält och försök exportera igen

1. **Upprepa** fälttillgänglighetsstegen i avsnitt 2 för **varje fält** som har rapporterats ha behörighetsproblem i **Massinläsningsjobb för data**.
2. När alla problematiska fält har rätt synlighet och redigeringsbehörigheter:
   - Gå tillbaka till **Adobe Learning Manager**.
   - I konfigurationen **SFDC-anslutning** **gör du om exporten**.


## Viktiga noteringar och begränsningar

Tänk på dessa SFDC-ALM-specifikationer när du utformar eller felsöker integreringar.

### Inget automatiskt skapande av objekt/fält i SFDC

- **SFDC-kopplingen skapar inte nya objekt eller fält i Salesforce**.
- Om ett **nytt fält har lagts till i ALM** och du vill att det ska visas i SFDC:
   - Skapa manuellt **motsvarande anpassade fält** i SFDC.
   - **Mappa** det anpassade SFDC-fältet till **lämpligt ALM-fält** i anslutningskonfigurationen.
   - Kontrollera att det nya fältet har **rätt behörigheter på fältnivå** (använd avsnitt 2).

### Återanrops-URL för ALM-konton med anpassade domäner

- Om ALM-kontot använder en **anpassad domän**, måste teknikerteamet **lägga till den anpassade domänen** i **listan över tillåtna återanrops-URL** för SFDC-anslutarens OAuth-produktionsprogram.
- Detta görs via en **Jira-begäran** till tekniker.
- Utan detta kan OAuth-flödet för anslutningen misslyckas.

### Tidszonsbegränsning (endast UTC)

- Om SFDC-organisationen använder en annan **tidszon än UTC** kan **data om slutförande och registrering saknas** under synkningen.
- Orsak: ALM **stöder för närvarande bara UTC-tidszonen** för SFDC-integreringen.
- Intern referens: PAPI-24525 har höjts för att stödja ytterligare tidszoner.

### Begränsning av filterdatatyp (plocklista kontra checklista)

- ALM har stöd för import av **SFDC-filter som har skapats med listrutefält**.
- ALM **stöder inte** filter baserat på fälten för checklista/multimarkering.
- Orsak: ALM **stöder bara strängdatatyper** för SFDC-filter.
