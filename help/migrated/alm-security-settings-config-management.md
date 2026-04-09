---
title: Adobe Learning Manager - säkerhetsinställningar och konfigurationshantering
description: I det här dokumentet beskrivs Adobe Learning Manager administratörskontotyper, säkerhetsrelaterade inställningar, rekommenderade säkra standardinställningar, API-funktioner, exportfunktioner, konfigurationsjämförelsemetoder, publiceringsrutiner och versionshistorik. Den ger detaljerad vägledning om hur behöriga konton fungerar, deras säkerhetskonsekvenser och hur konfigurationshantering stöds på plattformen.
jcr-language: en-us
exl-id: a2e34104-c417-407f-af85-9f3f4b2a9fcb
source-git-commit: 3188d7f5593aeee87978e1e46456f01e1f41d57b
workflow-type: tm+mt
source-wordcount: '1954'
ht-degree: 0%

---

# Säkerhetsinställningar och konfigurationshantering

Den här guiden innehåller detaljerade svar på FedRAMP-rekommendationer (FRR-RSC-03 till FRR-RSC-08) för Adobe Learning Manager (ALM). Här beskrivs bästa säkerhetspraxis, rekommenderade säkra standardinställningar och verktyg för granskning, export och hantering av behöriga kontoinställningar. Dokumentet är utformat för administratörer och efterlevnadsteam för att säkerställa säker konfiguration och hantering av ALM-konton.

Här framhålls också områden där ALM uppfyller eller delvis uppfyller FedRAMP-standarderna, med referenser till stöddokumentation och resurser som finns tillgängliga på Adobe Experience League.

+++Vilka säkerhetsrelaterade inställningar kan bara hanteras av Anpassade administratörer eller Integreringsadministratörer i Adobe Learning Manager, och vilka är deras säkerhetskonsekvenser?

Adobe Learning Manager två privilegierade kontotyper - Anpassad administratör och Integreringsadministratör. Var och en av dem har en definierad uppsättning säkerhetsrelevanta inställningar med dokumenterade konsekvenser.

**Anpassad administratör - vad de kan använda**:

* Anpassade roller konfigureras av den fullständiga administratören på ALM-administratör > Användare > Anpassade roller. En anpassad administratör kan ges åtkomst till en eller flera av dessa behörighetskategorier: Kontobehörigheter (tillkännagivanden, spelifiering, färdigheter, användarhantering), Funktionsprivilegier (kataloger, rapporter, taggar) och Privilegier för utbildningsobjekt (kurser, certifieringar, utbildningsvägar).
* Omfång är den mest säkerhetskänsliga inställningen: en anpassad roll kan begränsas till specifika användargrupper och/eller specifika kataloger. Utan begränsning av omfånget har en anpassad roll effektivt plattformsövergripande åtkomst till de tilldelade funktionerna - vilket närmar sig det utrymme som en fullständig administratör har.
* Om en anpassad roll ges inställningsåtkomst under Kontobehörigheter kan den anpassade administratören ändra inloggningsmetoder, meddelandeinställningar och konfigurationer på kontonivå - ett privilegium med stor inverkan som bara bör beviljas med uttrycklig affärsmotivering.

**Integreringsadministratör - vad de kan använda**:

* Integreringsadministratörer hanterar programregistreringar för OAuth 2.0 via Integreringsadministratör > Program > Registrera. De väljer ett av sex OAuth-omfång, som sträcker sig från elevens läsåtkomst till administratörsrollen och läs- och skrivåtkomst. Läs- och skrivomfattning för administratörer ger det registrerade programmet samma behörigheter som en fullständig administratör via API:et.
* Integreringsadministratörer konfigurerar FTP-, SFTP-, Salesforce-, Workday- och andra anslutningar som importerar användarposter, rolltilldelningar och kursslutföranden - och exporterar plattformsdata till externa system.
* Integreringsadministratörer konfigurerar webhookar som skickar ALM-händelsedata i realtid (registreringar, slutföranden, rolländringar) till externa URL:er. En äventyrad eller felkonfigurerad webhook-slutpunkt är en dataexfiltreringsrisk.
* Integreringsadministratörer kan konfigurera LTI-integreringar. När LTI har aktiverats kan det inte inaktiveras.

**Referenser**:

* [Anpassade roller | Adobe Learning Manager](https://experienceleague.adobe.com/sv/docs/learning-manager/using/admin/custom-role)
* [Hantera anpassade roller via CSV | Adobe Learning Manager](https://experienceleague.adobe.com/sv/docs/learning-manager/using/integration/configure-role-csv-files)
* [Användarhandbok för programutvecklare \| Adobe Learning Manager](https://experienceleague.adobe.com/sv/docs/learning-manager/using/integration/developer-manual)
* [Adobe Learning Manager-anslutningar](https://experienceleague.adobe.com/sv/docs/learning-manager/using/integration/connectors)

+++

+++Vilka är de rekommenderade säkra standardinställningarna för administratörskonton och privilegierade konton på toppnivå i Adobe Learning Manager, och var är de konfigurerade?

Adobe Learning Manager-dokument som är specifika rekommenderade säkra standardvärden för både administratörsrollen och behöriga kontotyper.

* **Administratörskontots standardinställningar på toppnivå (konfigurerat vid första etableringen)**:

* Inloggningsmetod för interna användare: Enkel inloggning (SSO) via SAML 2.0: konfigurerad på ALM-administratör > Inställningar > Inloggningsmetoder. Använd inte Adobe ID för personal eller administratörer.
* Tvåstegsverifiering (2FA): Krävs för alla användare: konfigurerad i Adobe Admin Console > Inställningar > Säkerhet och integritet > Autentiseringsinställningar.
* Maximal sessionslängd: 8 timmar (eller per organisationspolicy): konfigurerat på Adobe Admin Console > Inställningar > Säkerhet och integritet > Avancerade inställningar.
* Maximal inaktiv tid: 30 minuter (eller per organisationspolicy): samma plats som ovan.
* Inaktiv automatisk borttagning av användare: Aktiverad med en organisationsdefinierad kvarhållningsperiod (t.ex. 90 dagars inaktivitet): ALM-administratör > Inställningar > Allmänt.
* Extern användarprofil som upphör att gälla: Ställ in varje extern profil när den skapas: ALM-administratör > Användare > Extern. Inga obestämda externa profiler.
* Begränsningar av IP-åtkomst: Begränsa till godkända IP-intervall där det är möjligt: Admin Console > Inställningar > Avancerade inställningar.

**Standardvärden för anpassad administratörsroll (konfigurerade när varje roll skapades)**:

* OAuth-omfattning för registrerade program: minsta nödvändiga omfattning. Ge aldrig administratörsrollen läs-/skrivåtkomst om det inte är absolut nödvändigt.
* Omfång för anpassad roll: begränsa till specifika användargrupper och specifika kataloger. Skapa inte anpassade roller med omfånget Alla användare och Alla kataloger om inte funktionen verkligen kräver det.
* Inställningsåtkomst i anpassade roller: Bevilja inte om inte den specifika funktionen kräver det, med tanke på risken för eskalering av behörigheter.

**Standardinställningar för integrationsadministratör**:

* API OAuth-omfattning: välj det mest restriktiva omfång som uppfyller integreringens krav. Ge inte administratörer läs-/skrivbehörighet till program som bara behöver elevens läsbehörighet.
* Anslutningsuppgifter, LTI-autentiseringsuppgifter och webhook-URL:er: behandla som känsliga hemligheter - dela aldrig via e-post eller bekräfta för källkontroll.

**Referenser**:

* [Inställningar | Adobe Learning Manager](https://experienceleague.adobe.com/sv/docs/learning-manager/using/admin/custom-role)
* [Säker användarautentisering och lösenord | Adobe Admin Console](https://helpx.adobe.com/se/enterprise/using/authentication-settings.html)
* [Anpassade roller | Adobe Learning Manager](https://experienceleague.adobe.com/sv/docs/learning-manager/using/admin/custom-role)

+++

+++Gör Adobe Learning Manager det möjligt för administratörer att jämföra aktuella kontoinställningar med de rekommenderade säkra standardinställningarna?

Det finns ingen särskild jämförelsetavla i Adobe Learning Manager där aktuella inställningar visas automatiskt vid sidan av rekommenderade säkra standardinställningar.

**Anpassad rollrapport: aktuella privilegierade rolltilldelningar**:

* I ALM går du till Admin > Användare > Anpassade roller och klickar på Hämta (längst upp till höger) för att exportera en CSV-fil med alla anpassade roller, deras behörighetsgrupper och deras omfångstilldelningar.
* Jämför denna export med de rekommenderade standardinställningarna i AVSNITT 8 i FRR-RSC-02 - och kontrollera specifikt om någon anpassad roll har inställningsåtkomst, omfånget Alla användare eller omfånget Alla kataloger utan dokumenterad motivering.

**ALM REST API: programmatisk konfigurationshämtning**:

* Slutpunkten GET/konto returnerar konfigurationsdata på kontonivå i JSON-format, som kan nås med OAuth-omfång för administratörsrollen. Kunderna kan programmässigt anropa denna slutpunkt och skilja svaret från en baslinje som härleds från de rekommenderade standardvärdena i FRR-RSC-02, avsnitt 8.
* Slutpunkten GET /users (med filtret include=roll) returnerar aktuella rolltilldelningar för alla användare, vilket möjliggör automatisk identifiering av oväntade rolltilldelningar.

>[!NOTE]
>
>Adobe Learning Manager har inget inbyggt gränssnitt för jämförelse sida vid sida. Kunder som behöver automatisk kontroll av konfigurationsefterlevnad bör integrera ALM REST API med sina befintliga verktyg.

**Referens**

* [Användarhandbok för programutvecklare | Adobe Learning Manager](https://experienceleague.adobe.com/sv/docs/learning-manager/using/integration/developer-manual)

+++

+++Kan administratörer exportera aktuella säkerhetsrelevanta inställningar och konfigurationer från Adobe Learning Manager i ett maskinläsbart format?

Adobe Learning Manager stöder export av säkerhetsrelevanta konfigurationsdata via flera olika mekanismer. Ingen enskild export ger en fullständig ögonblicksbild av alla säkerhetsinställningar samtidigt, men följande exporter täcker tillsammans hela omfattningen av säkerhetsrelevanta data.

**ALM REST API: JSON-export av aktuella rolltilldelningar och kontokonfiguration**:

* GET/konto: returnerar kontonivåinställningar i JSON, inklusive konfigurationsdata för aktiv inloggning och kontometadata.
* GET /users?include=role: returnerar alla användare med deras aktuella tilldelade roller i JSON.
* GET/userGroups - returnerar alla användargrupper och deras medlemskap som är relevanta för granskning av anpassat rollomfång.
* Alla API-svar är JSON (vnd.api+json). Autentisering använder OAuth 2.0 med läs-/skrivomfattning för administratörsrollen.

**CSV-export med anpassade roller: aktuella definitioner av privilegierade roller**:

* ALM-administratör > Användare > Anpassade roller > Hämta exporterar en CSV-fil med alla anpassade rolldefinitioner, deras behörighetskategorier och omfångstilldelningar.
* Den här exporten kan användas som en maskinläsbar ögonblicksbild av den aktuella konfigurationen för behöriga konton.
**

**Jobb-API: bulkanvändar- och rolldata**:

* ALM Jobs API stöder generering på begäran av användarrapporter (inklusive rolltilldelningar) i CSV-format. Dessa kan schemaläggas och förbrukas av externa kompatibilitetsverktyg eller SIEM-verktyg.

**Referens**

* [Användarhandbok för programutvecklare | Adobe Learning Manager](https://experienceleague.adobe.com/sv/docs/learning-manager/using/integration/developer-manual)

+++

+++Tillhandahåller Adobe Learning Manager ett API där säkerhetsinställningarna kan visas och justeras programmatiskt?

Adobe Learning Manager har ett komplett REST API v2 som möjliggör programmatisk visning och justering av säkerhetsrelevanta inställningar med hjälp av OAuth 2.0-autentisering. Nedan följer de specifika API-funktionerna som är relevanta för säkerhetsinställningar:

**Autentisering och omfattning**:

* Programmen registreras av integreringsadministratören på Integreringsadministratör > Program > Registrera. OAuth 2.0 Client ID och Secret utfärdas per program.
* Sex omfattningar är tillgängliga. Läs- och skrivåtkomst krävs för hantering av säkerhetsinställningar. Detta ger programmet samma åtkomst som en fullständig administratör via API:et.
* Åtkomsttoken hämtas via standardauktoriseringskoden för OAuth eller flödet för klientautentiseringsuppgifter. Bas-URL: https://learningmanager.adobe.com/primeapi/v2/

**Hantering av användare och roller via API**:

* GET/användare: hämta alla användare och deras nuvarande roller
* POST/användare: tillhandahålla nya användare programmässigt
* PATCH /users/{id}: uppdatera användarattribut inklusive rolltilldelningar
* DELETE /users/{id}: inaktivera ett användarkonto
* POST /users/{id}/purge: Töm en användare och alla tillhörande poster permanent

Hämtning av kontokonfiguration:

* GET /account: returnerar konfiguration på kontonivå, inklusive kontoinställningsdata i JSON-format, inklusive fält som complianceLabelDefaultID, showComplianceLabel och custom_injektions.

+++

+++Publicerar Adobe Learning Manager sin vägledning för säker konfiguration i ett maskinläsbart format som OSCAL, JSON eller YAML?

Adobe Learning Manager publicerar för närvarande inte sin handbok för säker konfiguration i ett maskinläsbart format. Vägledningen i [FRR-RSC-01](/help/migrated/alm-administrative-lifecycle.md) och [FRR-RSC-02](/help/migrated/alm-secure-administration-guide.md) publiceras som läsbar dokumentation på Adobe Experience League i HTML och hämtningsbara dokumentformat.

Det finns ingen offentligt tillgänglig OSCAL-komponentdefinition, YAML-baslinje eller JSON-principfil som kodar de rekommenderade säkra standardinställningarna för Adobe Learning Manager.

Kunder som behöver en automatisk jämförelse av aktuella inställningar mot rekommenderade baslinjer bör använda [ALM REST API](https://experienceleague.adobe.com/sv/docs/learning-manager/using/integration/developer-manual) för att hämta aktuella konfigurationsdata i JSON-format.

+++

+++Är Adobe Learning Manager användarhandbok för säker konfiguration offentligt tillgänglig utan krav på inloggning eller särskild åtkomst?

**Vad är offentligt tillgängligt**:

* [FRR-RSC-01: Säker administrationsguide](/help/migrated/alm-administrative-lifecycle.md): Fullständig livscykelvägledning för administratörskonton på högsta nivå.
* [FRR-RSC-02: Administrativa säkerhetsinställningar och implikationer](/help/migrated/alm-secure-administration-guide.md): alla säkerhetsrelevanta inställningar, deras konsekvenser och rekommenderade standardvärden.
* FRR-RSC-03-10 (detta dokument) - Frågor och svar på alla åtta FedRAMP BÖR rekommendationer.

+++

+++Tillhandahåller Adobe Learning Manager versionshistorik och en versionshistorik som gör det möjligt för byråer att spåra ändringar i säkerhetsrelevanta inställningar och rekommenderade standardinställningar över tid?

Adobe Learning Manager har en offentlig, detaljerad versionshistorik för varje produktuppdatering. Säkerhetsrelevanta ändringar av administrativa inställningar, autentiseringsfunktioner, API-slutpunkter och rollhanteringsfunktioner dokumenteras i varje version.

**ALM-versionsinformation: numrerad, kumulativ ändringshistorik**:

* Adobe publicerar numrerade versionsinformation för varje Adobe Learning Manager-uppdatering (t.ex. uppdatering 100, uppdatering 99). Dessa publiceras på Experience League och dokumenterar alla nya funktioner, förändringar av existerande inställningar, tillägg och borttagningar av API:er, anslutningsändringar och borttagna funktioner.
* Varje versionsinformation innehåller ett särskilt avsnitt för API-ändringar, med nya slutpunkter, ändrade svarsfält och utfasningar som är direkt relevanta för säkerhetsrelevanta konfigurationsfunktioner.

**Nyheter: sammanfattning av funktioner per version**:

* Varje större version har en dedikerad sida &quot;Nyheter&quot; som dokumenterar nya säkerhetsrelevanta funktioner med sammanhang. Versionsinformationen innehåller till exempel ändringar av behörighetshantering för anpassade roller, tillägg av CSV-skapade behörighetsinställningar för anpassade roller och ändringar av API-hastighetsbegränsning.

**Lista över API-borttagningar: auktoritativ post med borttagna API-funktioner**:

* Adobe har en dedikerad sida för API-utfasningar där alla utfasade och borttagna ALM API-slutpunkter listas tillsammans med den utgivningsversion där varje utfasning inträffade.

**Referenser**:

* [Versionsinformation om Adobe Learning Manager](https://experienceleague.adobe.com/sv/docs/learning-manager/using/introduction/release-notes)
* [Nyheter i Adobe Learning Manager](https://experienceleague.adobe.com/sv/docs/learning-manager/using/introduction/whats-new-july-2024)
* [API-borttagningar i Adobe Learning Manager](https://experienceleague.adobe.com/sv/docs/learning-manager/using/introduction/api-deprecations-list)

+++
