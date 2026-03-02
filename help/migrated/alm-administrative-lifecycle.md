---
title: Livscykel för administratörskonton i Adobe Learning Manager
description: Det här dokumentet innehåller omfattande vägledning om säker hantering av administratörskonton på toppnivå i Adobe Learning Manager (ALM) för att uppfylla FedRAMP-kraven och bästa säkerhetsrutiner.
jcr-language: en-us
source-git-commit: db3ed4dc44da75b418e923999bdf3776bf81b11f
workflow-type: tm+mt
source-wordcount: '2122'
ht-degree: 0%

---


# Administratörskontotyper i Adobe Learning Manager

## ALM-rollmappning

I Adobe Learning Manager är administratörsrollen den högsta nivån. Det här är den roll som det hänvisas till när denna guide använder FedRAMP-termen &quot;administrationskonto på högsta nivån&quot;. Anpassade administratörer och integreringsadministratörer behandlas som privilegierade konton (omfång).

I tabellen nedan mappas FedRAMP-kontonivåer till de specifika roller som används i Adobe Learning Manager:

| FedRAMP-term | ALM-rollnamn | Beskrivning |
|--------------------------------------|----------------------------|-------------|
| Administratörskonto på toppnivå | Administratör | Högsta privilegierade roll i ALM. Full kontroll över användare, roller, utbildningsinnehåll, rapportering, integreringar och alla systemkonfigurationer. Mappar direkt till FedRAMP-definitionen för administratörskonton på högsta nivån. |
| Privilegierat konto (omfattning) | Anpassad administratör | En definierad delmängd av administratörsbehörigheter som omfattar specifika funktioner (till exempel rapportering och kataloghantering). Har inte fullständig kontroll på kontonivå. |
| Privilegierat konto (integrering) | Integreringsadministratör | Hanterar integreringar och API-baserad åtkomst mellan ALM och externa system. Utökade privilegier endast för integrationshantering. |


Adobe Learning Manager använder en rollbaserad åtkomstkontrollmodell (RBAC) för att hantera administratörsåtkomst. Administrativa roller tilldelas endast av auktoriserade administratörer.

Mer information finns i [Anpassade roller i Adobe Learning Manager](https://experienceleague.adobe.com/sv/docs/learning-manager/using/admin/custom-role)

## Identitetstyper och rekommenderad autentisering

Adobe Admin Console stöder tre identitetstyper för administratörskonton. Valet av identitetstyp har direkta säkerhetskonsekvenser:

| Identitetstyp | Beskrivning | Säkerhetsrekommendation |
|---------------------------|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| Adobe ID (personligt ID) | Standardtyp; hanteras av Adobe. Vem som helst kan skapa ett. | REKOMMENDERAS INTE för administratörer. Organisationen har ingen kontroll över den här kontotypen. |
| Enterprise ID | Organisationsägt konto som hanteras av en Admin Console-systemadministratör. | Godtagbart om Federated ID/SSO inte är tillgängligt. Tvinga 2FA. |
| Federated ID (SSO) | Organisationsägd; integrerad med SAML 2.0 SSO. Organisationen kontrollerar autentiseringen helt. | REKOMMENDERAS. Autentiserar via organisationens IdP. Stöder MFA-krav på identitetsleverantörsnivå. |

Mer information finns här:

* [Identitetstyper](https://helpx.adobe.com/se/enterprise/using/admin-console.html)
* [Säker användarautentisering och lösenord](https://helpx.adobe.com/se/enterprise/using/authentication-settings.html)

## Rolltilldelning och åtkomstkontroll

Åtkomsten till administratörskonton i Adobe Learning Manager styrs genom uttrycklig [rolltilldelning](https://experienceleague.adobe.com/sv/docs/learning-manager/using/admin/user-management/add-users-user-groups) av en befintlig administratör. Säker administrativ åtkomst kännetecknas av följande:

* Administrativa roller tilldelas endast av auktoriserade administratörer.
* Åtkomsten är rollbaserad och omfattas enligt tilldelade behörigheter.
* Organisationer ansvarar för att begränsa den administrativa åtkomsten för användare med ett legitimt affärsbehov.

Adobe rekommenderar att kunderna regelbundet ser över sin behörighet för administration för att säkerställa att principen om minsta privilegier följs.

## Tillämpa multifaktorautentisering (MFA)

Adobe rekommenderar starkt att administratörer inför tvåstegsverifiering (2FA) över hela organisationen. MFA gäller användare av Enterprise ID och Adobe ID. Federated IDS användare bör ha tillämpat MFA hos sin organisations identitetsleverantör.

För att upprätthålla 2FA i Adobe Admin Console:

1. Logga in i Adobe Admin Console.
2. Gå till Inställningar > Säkerhet och integritet > Autentiseringsinställningar.
3. Aktivera tvåstegsverifiering och välj alternativet Tvinga för att hindra användare från att inaktivera den.
4. Du kan även konfigurera IP-baserade åtkomstbegränsningar och avancerade sessionsinställningar (maximal sessionslängd/maximal inaktiv tid).

>[!IMPORTANT]
>
>Adobe rekommenderar att du tillämpar 2FA och inte lämnar det valfritt för användare. Det kan ta upp till 24 timmar att tillämpa 2FA. För Federated ID-användare: framtvinga MFA hos identitetsleverantören.

Mer information finns i [Säker användarautentisering](https://helpx.adobe.com/se/enterprise/using/authentication-settings.html).


## Logga in som administratör

ALM [Administratörer](https://experienceleague.adobe.com/sv/docs/learning-manager/using/get-started/getting-started-admin) loggar in direkt på ALM-plattformen med organisationsuppgifter som hanteras via Admin Console.

### Tilldela en administratörsroll

Inom ALM-plattformen konfigurerar administratörer administrativ åtkomst genom att skapa och hantera roller, tilldela behörigheter till användare och definiera behörighetsomfång baserat på operativt ansvar.

Tilldela administratörsrollen i ALM:

1. Logga in på Adobe Learning Manager som administratör.
2. Gå till Användare > Intern.
3. Sök efter eller välj målanvändaren.
4. Välj Åtgärder > Tilldela roll > Skapa administratör.

Med anpassade administrativa roller kan kunder delegera administrativa uppgifter samtidigt som de har centraliserad kontroll över behörigheter på kontonivå. Anpassade administratörer kan omfattas av specifika användargrupper eller kataloger.

Mer information finns i [Lägga till användare och användargrupper](https://experienceleague.adobe.com/sv/docs/learning-manager/using/admin/user-management/add-users-user-groups).

## Konfigurera inloggningsmetoder och SSO

ALM-administratörer styr vilka inloggningsmetoder som är tillgängliga för alla användare via Inställningar > Inloggningsmetoder, en viktig säkerhetsrelevant konfiguration:

* **Interna användare**: Ställ in inloggningsläget på Adobe ID eller enkel inloggning (SSO). SSO via SAML 2.0 rekommenderas starkt.
* **Externa användare**: Ställ in inloggningsläget på Adobe ID, SSO eller Learning Manager ID. Anpassa den valda metoden till organisationens säkerhetspolicy.

Adobe rekommenderar att du använder Federated ID/SAML 2.0 SSO som inloggningsmetod för alla interna användare. Detta säkerställer att autentiseringen styrs helt av organisationens identitetsleverantör, vilket möjliggör centraliserad MFA-tillämpning och omedelbar kontoåterkallning vid användarens avgång.

Mer information finns i [Inställningar](https://experienceleague.adobe.com/sv/docs/learning-manager/using/admin/settings).

## Rekommenderade säkra standardvärden för etablering

När ett ALM-konto först etableras rekommenderar Adobe att du verifierar följande standardinställningar innan du ger någon administratör operativ åtkomst:

| Inställning | Rekommenderad säkerhetsstandard | Var kan man konfigurera |
|------------------------------|------------------------------------------------------------------|-------------------------------------------------|
| Inloggningsmetod - interna användare | Enkel inloggning (SSO)/Federated ID | ALM > Inställningar > Inloggningsmetoder |
| Tvåstegsverifiering (2FA) | Kräv (inte valfritt för någon användare) | Admin Console > Inställningar > Säkerhet och integritet |
| Maximal sessionslängd | 8 timmar eller per organisationspolicy | Admin Console > Inställningar > Avancerade inställningar |
| Maximal inaktiv tid | 30 minuter eller per organisationspolicy | Admin Console > Inställningar > Avancerade inställningar |
| Omfång för administratörsroll | Minsta behörighet - använd anpassade administratörsroller där det är möjligt | ALM > Användare > Anpassade roller |
| Extern användare har upphört | Ange ett förfallodatum på alla externa användarprofiler | ALM > Användare > Extern |

### Inledande checklista för installation för nya administratörer

När du etablerar ett nytt administratörskonto på högsta nivån ska du slutföra följande innan du beviljar operativ åtkomst:

* Bekräfta identitetstypen är Enterprise ID eller Federated ID - inte Personligt Adobe ID.
* Tvinga 2FA på Admin Console-nivå (Inställningar > Autentiseringsinställningar).
* Konfigurera SSO/Federated ID om det inte redan har aktiverats.
* Ställ in Maximal sessionslängd och Maximal inaktiv tid i Admin Console > Inställningar > Avancerade inställningar.
* Begränsa omfattningen av administratörsrollen - tilldela endast de behörigheter som krävs för användarens ansvar.
* Verifiera att administratörskontot är knutet till en e-postadress för organisationen som styrs av ditt IT-team.
* Dokumentera kontot i organisationens privilegierade åtkomstregister.

## Förvaltning av förvaltningskonton

### Dagliga administrativa uppgifter

Administrationskonton används för att utföra dagliga operativa uppgifter, däribland följande:

* **Hantering av användarlivscykel**: Skapa användare, uppdatera profiler och göra rolländringar.
* **Hantera utbildningsinnehåll**: Hantera kurser, utbildningsprogram, certifieringar och kataloger.
* **Rapportering och analys**: Genererar och granskar rapporter om elevframsteg och plattformsanvändning.
* **Integreringar och systemkonfiguration**: Hantera anslutningar, API-baserad åtkomst och inställningar på systemnivå.

Administratörer förväntas följa organisationens interna åtkomstkontroll och ändra hanteringsprinciper när de utför administrativa åtgärder.

Se [Vanliga frågor för Adobe Learning Manager-administratörer](https://experienceleague.adobe.com/sv/docs/learning-manager/using/faq/frequently-asked-questions-for-administrators)


### Rollhierarki och delegering

Adobe Admin Console använder en hierarkisk administratörsstruktur. Systemadministratörer kan delegera ansvar till roller med lägre privilegier för att minska angreppsytan för administratörskontot på högsta nivån:

* Produktadministratör: Hanterar åtkomst till specifika Adobe-produkter (t.ex. Adobe Learning Manager).
* Produktprofiladministratör: Hanterar användarmedlemskap i specifika produktprofiler.
* Administratör av användargrupp: Hanterar användargruppsmedlemskap.
* ALM Custom Admin: Omfångsrik administratör inom ALM med konfigurerbara behörigheter per katalog och användargrupp.

### Löpande styrningspraxis

Följande praxis bör följas av organisationer som löpande driver ALM-administratörskonton:

* **Regelbunden granskning av åtkomst**: Granska regelbundet listan över systemadministratörer i Admin Console (Användare > Administratörer) och ALM-administratörer (Användare > Intern) för att se till att endast aktuell, auktoriserad personal innehar dessa roller.
* **Övervakning av granskningsloggen**: Alla ändringar som har gjorts av administratörer registreras i granskningsloggen i Admin Console. Systemadministratörer har full insyn. Kontrollera loggen regelbundet för att se om det finns obehöriga ändringar.
* **Lägsta stående åtkomst**: Undvik att använda administratörskonton på högsta nivån för rutinuppgifter. Reservera fullständig administratörsåtkomst för uppgifter som kräver det.
* **Sessionssäkerhet**: Konfigurera Maximal sessionslängd och Maximal inaktiv tid i Admin Console > Inställningar > Avancerade inställningar för att begränsa exponeringen från obevakade sessioner.

Se [Översikt av Admin Console](https://helpx.adobe.com/se/enterprise/using/admin-console.html) för mer information.

### Hantera användarkonton under administratörskontroll

ALM-administratörer hanterar interna och externa användarkonton. Verksamhet av betydelse för skyddet omfattar följande:

* Automatisk borttagning av användare: I Inställningar kan administratörer konfigurera inaktiva interna användare så att de tas bort automatiskt efter ett visst antal dagar, vilket minskar risken för vilande konton.
* Externa användares förfallodatum: Administratörer anger ett förfallodatum när de skapar externa användarprofiler. Utgångna konton flyttas automatiskt till inaktivt läge.
* Ta bort användare: Administratörer kan ta bort användare manuellt via Användare > Interna > Åtgärder > Ta bort användare.
* Rensning av användare: Efter borttagningen kan administratörer permanent rensa användarposter för att efterleva principer för datalagring och förhindra obehörig åtkomst till inaktuella användardata.

Mer information finns här:

* [Lägga till användare och användargrupper](https://experienceleague.adobe.com/sv/docs/learning-manager/using/admin/user-management/add-users-user-groups)
* [Rensa användare](https://experienceleague.adobe.com/sv/docs/learning-manager/using/admin/purge-users)

## Avveckling av förvaltningskonton

Administratörsåtkomst måste tas bort när den inte längre behövs. Avveckling av administrativa konton kan omfatta följande:

* Återkalla administrativa roller från användare.
* Minska behörigheter när fullständig administratörsåtkomst inte längre behövs.
* Ta bort användare från systemet vid behov.

Regelbunden granskning och borttagning av onödig administrativ åtkomst bidrar till att mindre privilegierade kan få åtkomst.

### Ta bort systemadministratörsrättigheter (Admin Console)

När en systemadministratör lämnar organisationen eller ändrar roller måste behörigheterna återkallas omedelbart:

1. Logga in i Adobe Admin Console som systemadministratör.
2. Gå till Användare > Administratörer.
3. Markera administratören som ska tas bort.
4. Klicka på ikonen Fler alternativ (...) > Redigera administratör och ta sedan bort systemadministratörsrollen - ELLER välj Ta bort användare för att helt ta bort användaren från organisationen.
5. Om administratören hade andra roller (produktadministratör, supportadministratör osv.) återkallar du dem också.

>[!IMPORTANT]
>
>Om den avgående administratören är avtalsägare för organisationen måste rollen Avtalsägare överföras till en annan person innan den kan tas bort. Kontakta Adobe support vid behov.

Mer information finns här:

* [Skapa, uppdatera eller ta bort användarkonton i Admin Console](https://helpx.adobe.com/se/enterprise/using/manage-users-individually.html)
* [Lämna ett konto som organisationen äger](https://helpx.adobe.com/se/enterprise/using/leave-organization.html)

### Ta bort ALM-administratörsrollen

Så här återkallar du ALM-administratörsåtkomst utan att ta bort användarens konto (t.ex. när personen fortfarande är elev):

1. Logga in på Adobe Learning Manager som administratör.
2. Gå till Användare > Intern.
3. Sök efter och markera användaren.
4. Välj Åtgärder > Ta bort roll > Ta bort administratör.

Användaren återgår till elevrollen. Deras utbildningshistorik och kursregistreringar bevaras.

Mer information finns i [Lägga till användar- och användargrupper](https://experienceleague.adobe.com/sv/docs/learning-manager/using/admin/user-management/add-users-user-groups).

### Ta bort och ta bort användare

När en användare lämnar organisationen helt och deras konto bör tas bort från plattformen:

* Ta bort användaren: Användare > Intern > välj användare > Åtgärder > Ta bort användare. Detta inaktiverar kontot och tar bort aktiv åtkomst.
* Rensa användaren: Efter borttagningen går du till Användare > Användarrensning, väljer borttagningsmånaden, markerar användaren och väljer Åtgärder > Rensa användare. Om du rensar permanent tas alla användarposter bort.

Mer information finns i [Rensa användare](https://experienceleague.adobe.com/sv/docs/learning-manager/using/admin/purge-users).


## Säkerhet och delat ansvar

Adobe Learning Manager fungerar enligt en modell med delat ansvar:

* Adobe ansvarar för att säkra den underliggande ALM-plattformen och ALM-infrastrukturen.
* Kunderna ansvarar för hantering av administrativ åtkomst, rolltilldelningar och aktiviteter under användarlivscykeln inom sina ALM-konton.

Mer information om Adobe Learning Manager säkerhetsrutiner finns i [Adobe Learning Manager säkerhetsöversikt (PDF)](https://experienceleague.adobe.com/docs/learning-manager/assets/alm-security-whitepaper-2024.pdf?lang=sv-SE)

## Dokumentunderhåll

Det här dokumentet kan uppdateras regelbundet för att återspegla ändringar i Adobe Learning Manager-funktionen eller bästa administrationssätt. Versionen och det senast uppdaterade datumet sparas i dokumentets metadata och i FedRAMP-auktoriseringspaketet. Användare bör läsa den offentligt tillgängliga versionen på Adobe Experience League för att säkerställa att de använder de senaste riktlinjerna.

## Förbättrad säkerhetstäckning

### SCG-ENH-CMP

Adobe underhåller dokumenterad komponentinventering, ägandeskap och livscykelhanteringsprocesser för att säkerställa kontrollerad konfiguration och efterlevnad mellan systemkomponenter.

### SCG-ENH-API

Adobe tillämpar standardiserade API-säkerhetskontroller, inklusive autentisering, auktorisering och övervakning, med stöd av dokumenterad styrning och plattformsskydd.

### SCG-ENH-MRG

Adobe tillämpar formella ändrings- och sammanslagningshanteringsprocesser, inklusive gransknings- och godkännandekontroller, för att upprätthålla systemintegriteten och minska distributionsrisken.

### SCG-ENH-VRH

Adobe följer en definierad sårbarhetshanterings- och åtgärdsprocess som omfattar identifiering, prioritering, spårning och snabb lösning.
