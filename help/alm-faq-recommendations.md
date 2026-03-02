---
title: Livscykel för administratörskonton i Adobe Learning Manager
description: Det här dokumentet innehåller en omfattande sammanfattning av Adobe Learning Manager ALM-funktioner (Security Account Management), konfiguration och regelefterlevnad i linje med FedRAMP-rekommendationerna.
jcr-language: en-us
source-git-commit: 06051e44c0a6bc8ae60e44272ba088f2f6ff281f
workflow-type: tm+mt
source-wordcount: '1706'
ht-degree: 0%

---


# Säkerhetsrekommendationer för Adobe Learning Manager

## Vilka säkerhetsrelaterade inställningar kan bara hanteras av Anpassade administratörer eller Integreringsadministratörer i Adobe Learning Manager, och vilka är deras säkerhetskonsekvenser?

Adobe Learning Manager två privilegierade kontotyper - Custom Administrator och Integration Administrator - har var och en en definierad uppsättning av säkerhetsrelevanta inställningar med dokumenterade konsekvenser.

### Anpassad administratör: vad de kan arbeta med:

* Anpassade roller konfigureras av den fullständiga administratören på ALM-administratör > Användare > Anpassade roller. En anpassad administratör kan ges åtkomst till en eller flera av dessa behörighetskategorier: Kontobehörigheter (tillkännagivanden, spelifiering, färdigheter, användarhantering), Funktionsprivilegier (kataloger, rapporter, taggar) och Privilegier för utbildningsobjekt (kurser, certifieringar, utbildningsvägar).
* Omfång är den mest säkerhetskänsliga inställningen: en anpassad roll kan begränsas till specifika användargrupper och/eller specifika kataloger. Utan begränsning av omfånget har en anpassad roll effektivt plattformsövergripande åtkomst till de tilldelade funktionerna - vilket närmar sig det utrymme som en fullständig administratör har.
* Om en anpassad roll ges inställningsåtkomst under Kontobehörigheter kan den anpassade administratören ändra inloggningsmetoder, meddelandeinställningar och konfigurationer på kontonivå - ett privilegium med stor inverkan som bara bör beviljas med uttrycklig affärsmotivering.
* En anpassad administratör med inställningsåtkomst som också har enhetsåtkomst för användare kan tilldela sig själv den fullständiga administratörsrollen, vilket eskalerar till fullständig administrativ kontroll.

### Integreringsadministratör: vad de kan fungera:

* Integreringsadministratörer hanterar programregistreringar för OAuth 2.0 via Integreringsadministratör > Program > Registrera. De väljer ett av sex OAuth-omfång, som sträcker sig från elevens läsåtkomst till administratörsrollen och läs- och skrivåtkomst. Läs- och skrivomfattning för administratörer ger det registrerade programmet samma behörigheter som en fullständig administratör via API:et.
* Integreringsadministratörer konfigurerar FTP-, SFTP-, Salesforce-, Workday- och andra anslutningar som importerar användarposter, rolltilldelningar, kursslutföranden och exporterar plattformsdata till externa system.
* OAuth-omfattning för registrerade program: minsta nödvändiga omfattning. Ge aldrig administratörsrollen läs-/skrivåtkomst om det inte är absolut nödvändigt.
* Integreringsadministratörer konfigurerar webhookar som skickar ALM-händelsedata i realtid (registreringar, slutföranden, rolländringar) till externa URL:er. En äventyrad eller felkonfigurerad webhook-slutpunkt är en dataexfiltreringsrisk.
* Integreringsadministratörer kan konfigurera LTI-integreringar. När LTI har aktiverats kan det inte inaktiveras. Exponerade LTI-autentiseringsuppgifter ger obehörig åtkomst till kursinnehåll från externa LMS-plattformar.


## Vilka är de rekommenderade säkra standardinställningarna för administratörskonton och privilegierade konton på toppnivå i Adobe Learning Manager, och var är de konfigurerade?

### Standardinställningar för administratörskonton på toppnivå (konfigurerade vid första etablering):

* Inloggningsmetod för interna användare: Enkel inloggning (SSO) via SAML 2.0: konfigurerad på ALM-administratör > Inställningar > Inloggningsmetoder. Använd inte Adobe ID för personal eller administratörer.
* Tvåstegsverifiering (2FA): Krävs för alla användare: konfigurerad i Adobe Admin Console > Inställningar > Säkerhet och integritet > Autentiseringsinställningar.
* Maximal sessionslängd: 8 timmar (eller per organisationspolicy): konfigurerat på Adobe Admin Console > Inställningar > Säkerhet och integritet > Avancerade inställningar.
* Maximal inaktiv tid: 30 minuter (eller per organisationspolicy): samma plats som ovan.
* Inaktiv automatisk borttagning av användare: Aktiverad med en organisationsdefinierad kvarhållningsperiod (t.ex. 90 dagars inaktivitet): ALM-administratör > Inställningar > Allmänt.
* Extern användarprofil som upphör att gälla: Ställ in varje extern profil vid skapande - ALM-administratör > Användare > Extern. Inga obestämda externa profiler.
* Begränsningar för IP-åtkomst: Begränsa till godkända IP-intervall där det är möjligt - Admin Console > Inställningar > Avancerade inställningar.

### Standardinställningar för anpassade administratörsroller (konfigurerade när varje roll skapades):

* OAuth-omfattning för registrerade program: minsta nödvändiga omfattning. Ge aldrig administratörsrollen läs-/skrivåtkomst om det inte är absolut nödvändigt.
* Omfång för anpassad roll: begränsa till specifika användargrupper och specifika kataloger. Skapa inte anpassade roller med omfånget Alla användare och Alla kataloger om inte funktionen verkligen kräver det.
* Inställningsåtkomst i anpassade roller: Bevilja inte om inte den specifika funktionen kräver det, med tanke på risken för eskalering av behörigheter.

### Standardinställningar för integrationsadministratör:

* API OAuth-omfattning: välj det mest restriktiva omfång som uppfyller integreringens krav. Ge inte administratörer läs-/skrivbehörighet till program som bara behöver elevens läsbehörighet.
* Anslutningsuppgifter, LTI-autentiseringsuppgifter och webhook-URL:er: behandla som känsliga hemligheter - dela aldrig via e-post eller bekräfta för källkontroll.

## Gör Adobe Learning Manager det möjligt för administratörer att jämföra aktuella kontoinställningar med de rekommenderade säkra standardinställningarna?

Det finns ingen särskild jämförelsetavla i Adobe Learning Manager där aktuella inställningar visas automatiskt vid sidan av rekommenderade säkra standardinställningar. Med tre plattformsfunktioner kan administratörer emellertid granska och jämföra aktuella konfigurationer manuellt eller programmatiskt.

### Rapport över anpassade roller - aktuella privilegierade rolltilldelningar:

I ALM går du till Admin > Användare > Anpassade roller och klickar på Hämta (längst upp till höger) för att exportera en CSV-fil med alla anpassade roller, deras behörighetsgrupper och deras omfångstilldelningar.

### ALM REST API - programmatisk konfigurationshämtning:

* Slutpunkten GET/konto returnerar konfigurationsdata på kontonivå i JSON-format, som kan nås med OAuth-omfång för administratörsrollen. Kunderna kan anropa slutpunkten programmatiskt.
* Slutpunkten GET /users (med filtret include=roll) returnerar aktuella rolltilldelningar för alla användare, vilket möjliggör automatisk identifiering av oväntade rolltilldelningar. Använd Jobb-API:et för massexport av användare.

## Kan administratörer exportera aktuella säkerhetsrelevanta inställningar och konfigurationer från Adobe Learning Manager i ett maskinläsbart format?

Adobe Learning Manager stöder export av säkerhetsrelevanta konfigurationsdata via flera olika mekanismer. Ingen enskild export ger en fullständig ögonblicksbild av alla säkerhetsinställningar samtidigt, men följande exporter täcker tillsammans hela omfattningen av säkerhetsrelevanta data.

### Granskningslogg för Admin Console - CSV-export av alla autentiserings- och rolländringar:

* Gå till **Insikter > Loggar > Granskningslogg** i Adobe Admin Console, tillämpa filter efter behov och klicka på **Exportera CSV**
* Den exporterade CSV-filen registrerar alla administrativa åtgärder, inklusive: 2FA tvångsåtgärder ändringar, sessionsbegränsningsändringar, tilldelning och borttagning av administratörsroller, borttagningar av användare och ändringar av produktberättigande - allt med tidsstämplar och aktörsidentitet.
* Data sparas i 90 dagar. Global Admin Console-användare kan exportera loggar i alla organisationer.

### ALM REST API - JSON-export av aktuella rolltilldelningar och kontokonfiguration:

* `GET /account` - returnerar inställningar på kontonivå i JSON, inklusive aktiva inloggningskonfigurationsdata och kontometadata.
* `GET /users?include=role` - returnerar alla användare med sina aktuella tilldelade roller i JSON.
* `GET /userGroups` - returnerar alla användargrupper och deras medlemskap som är relevanta för granskning av anpassat rollomfång.
* Alla API-svar är JSON (`vnd.api+json`). Autentisering använder OAuth 2.0 med läs-/skrivomfattning för administratörsrollen.

### CSV-export av anpassade roller - aktuella definitioner av privilegierade roller:

* ALM-administratör > Användare > Anpassade roller > Hämta exporterar en CSV-fil med alla anpassade rolldefinitioner, deras behörighetskategorier och omfångstilldelningar.
* Den här exporten kan användas som en maskinläsbar ögonblicksbild av den aktuella konfigurationen för behöriga konton.

### Jobb-API - massanvändar- och rolldata:

* ALM Jobs API stöder generering på begäran av användarrapporter (inklusive rolltilldelningar) i CSV-format. Dessa kan schemaläggas och förbrukas av externa kompatibilitetsverktyg eller SIEM-verktyg.

Mer information finns i [Användarhandboken för programutvecklare](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/developer-manual) för Adobe Learning Manager.

## Tillhandahåller Adobe Learning Manager ett API där säkerhetsinställningarna kan visas och justeras programmatiskt?

Adobe Learning Manager har ett komplett REST API v2 som möjliggör programmatisk visning och justering av säkerhetsrelevanta inställningar med hjälp av OAuth 2.0-autentisering. Nedan följer de specifika API-funktionerna som är relevanta för säkerhetsinställningar:

### Autentisering och omfattning

* Program registreras av integreringsadministratören på **Integreringsadministratör > Program > Registrera**. OAuth 2.0 Client ID och Secret utfärdas per program.
* Sex omfattningar är tillgängliga. För hantering av säkerhetsinställningar krävs **läs-/skrivåtkomst för administratörsrollen**. Detta ger programmet samma åtkomst som en fullständig administratör via API:et.
* Åtkomsttoken hämtas via standardauktoriseringskoden för OAuth eller flödet för klientautentiseringsuppgifter.\
  **Bas-URL:**\
  `https://learningmanager.adobe.com/primeapi/v2/`

### Hantering av användare och roller via API

* `GET /users` - hämta alla användare och deras aktuella roller
* `POST /users` - tillhandahålla nya användare programmässigt
* `PATCH /users/{id}` - uppdatera användarattribut inklusive rolltilldelningar
* `DELETE /users/{id}` - inaktivera ett användarkonto
* `POST /users/{id}/purge` - Töm en användare och alla tillhörande poster permanent

### Hämtning av kontokonfiguration

* `GET /account` - returnerar konfiguration på kontonivå, inklusive kontoinställningsdata i JSON-format, inklusive fält som:
   * `complianceLabelDefaultID`
   * `showComplianceLabel`
   * `custom_injections`

### Adobe User Management API (Admin Console-lager)

* Adobe User Management API (UMAPI) ger programmerad åtkomst till Admin Console-åtgärder:
   * Användaretablering
   * Tilldelning av produktberättigande
   * Tilldelning av systemadministratörsroller på organisationsnivå
* UMAPI är separat från ALM REST API och fungerar på organisationsnivå i Adobe. Använd den för att automatisera rolltilldelningar i Admin Console och användaretablering.

## Publicerar Adobe Learning Manager sin vägledning för säker konfiguration - de rekommenderade standardinställningarna - i ett maskinläsbart format som OSCAL, JSON eller YAML?

Adobe Learning Manager publicerar för närvarande inte sin handbok för säker konfiguration i ett maskinläsbart format.

## Är Adobe Learning Manager användarhandbok för säker konfiguration offentligt tillgänglig utan krav på inloggning eller särskild åtkomst?

Ja. Adobe Learning Manager handbok för säker konfiguration är offentligt tillgänglig på Adobe Experience League. Inget konto, ingen inloggning eller licens krävs för att komma åt den.

Vad är offentligt tillgängligt:

* FRR-RSC-01: Säker administrationshandbok: Fullständig livscykelvägledning för administratörskonton på översta nivån.
* FRR-RSC-02: Administrativa säkerhetsinställningar och implikationer - alla säkerhetsrelevanta inställningar, deras konsekvenser och rekommenderade standardvärden.

## Tillhandahåller Adobe Learning Manager versionshistorik och en versionshistorik som gör det möjligt för byråer att spåra ändringar i säkerhetsrelevanta inställningar och rekommenderade standardinställningar över tid?

Adobe Learning Manager har en offentlig, detaljerad versionshistorik för varje produktuppdatering. Säkerhetsrelevanta ändringar av administrativa inställningar, autentiseringsfunktioner, API-slutpunkter och rollhanteringsfunktioner dokumenteras i varje version.

### ALM-versionsinformation - numrerad, kumulativ ändringshistorik

* Adobe publicerar numrerade versionsanteckningar för varje Adobe Learning Manager-uppdatering (t.ex. *Update 100*, *Update 99*).
* Dessa publiceras den **Experience League** och dokumentet:
   * Nya funktioner
   * Ändringar i befintliga inställningar
   * Tillägg och borttagningar av API
   * Kopplingsändringar
   * Borttagna funktioner
* Varje versionsinformation innehåller ett särskilt avsnitt för **API-ändringar**, med följande information:
   * Nya slutpunkter
   * Ändrade svarsfält
   * Avskrivningar
   * Dessa är direkt relevanta för säkerhetsrelevanta konfigurationskapacitet.

### Sidor med &quot;Nyheter&quot; - sammanfattning av funktioner per version

* Varje större version har en dedikerad **-**-sida som dokumenterar nya säkerhetsrelevanta funktioner med kontext.
* Exempel på dokumenterade säkerhetsrelaterade uppdateringar är:
   * Ändringar i behörighetshantering för anpassade roller
   * Tillägg av CSV-skapade behörigheters synlighet för anpassade roller
   * Ändringar av API-hastighetsbegränsning

### Lista över API-borttagningar - auktoritativ post över borttagna API-funktioner

* Adobe har en dedikerad **API-utfasningssida** som visar alla utfasade och borttagna ALM API-slutpunkter, inklusive den utgivningsversion där utfasningen inträffade.
* Exempel på utfasningar av betydelse för säkerheten är:
   * Ändringar av sorterings- och åsidosättningsbeteende för slutpunkten `GET /users`
   * Krav på meddelande- och rapportdatumfilter

