---
title: Adobe Learning Manager - handbok för säker administration
description: I den här handboken beskrivs säkerhetsinställningar, roller och bästa praxis för hantering av administratörssäkerhet och åtkomstkontroll i Adobe Learning Manager för att säkerställa efterlevnad och säkerhet.
jcr-language: en-us
exl-id: 67dd9334-9718-4b2a-841e-5d8bd5c42714
source-git-commit: 5682c45a4e5789a3eede53faf7cb257cd9685759
workflow-type: tm+mt
source-wordcount: '2354'
ht-degree: 0%

---

# Administrativa säkerhetsinställningar och säkerhetskonsekvenser

## Administrativa roller med säkerhetspåverkan

Adobe Learning Manager använder en rollbaserad åtkomstkontrollmodell (RBAC). I följande tabell mappas FedRAMP-kontonivåer till de ALM-roller som det refereras till i hela dokumentet:

| FedRAMP-term | ALM-roll | Säkerhetsrelevans |
|-------------|---------|------------------|
| Administratörskonto på toppnivå | Administratör | Fullständig kontroll på kontonivå. Exklusiv åtkomst till alla säkerhetsrelevanta inställningar som beskrivs i det här dokumentet. Det är den roll som det hänvisas till i hela den här handboken när termen &quot;högsta administrativa konto&quot; används. |
| Privilegierat konto (omfattning) | Anpassad administratör | Delegerad administrativ åtkomst som omfattar specifika funktioner, användargrupper eller kataloger. Det går inte att komma åt säkerhetsinställningar på kontonivå om de inte uttryckligen har beviljats. |
| Privilegierat konto (integrering) | Integreringsadministratör | Hanterar integreringar, API-registreringar och anslutningskonfigurationer. Utökade privilegier för integrationshantering. Det går inte att ändra andra säkerhetsinställningar på kontonivå. |

>[!NOTE]
>
>Endast användare som uttryckligen har tilldelats dessa roller kan ändra inställningar av administrativ eller säkerhetsrelaterad natur. Inställningarna i avsnitten 3-7 är endast tillgängliga för administratörsrollen om inget annat anges.

## Inställningar för inloggning och autentisering

Inställningarna för inloggning och autentisering styr hur alla användare, inklusive administratörer, får åtkomst till ALM-plattformen. Dessa inställningar konfigureras uteslutande av administratörsrollen och har en direkt och betydande inverkan på hela kontots säkerhet.

### Konfiguration av inloggningsmetod

**Plats:** ALM-administratör > Inställningar > Inloggningsmetoder

Administratören styr den autentiseringsmetod som används för alla interna och externa användare. Bland alternativen finns:

- **Adobe ID:** Användare autentiserar sig via sitt eget Adobe-konto. Hanteras av Adobe, inte av organisationen.
- **Enkel inloggning (SSO) via SAML 2.0:** Användare autentiserar sig via organisationens identitetsleverantör (IdP). Organisationen har fullständig kontroll över autentisering, MFA och sessionspolicy.
- **ID för Learning Manager:** Endast tillgängligt för externa användare. Användarna skapar ett plattformsspecifikt användarnamn och lösenord.
- **Flera SSO-konfigurationer:** Upp till 20 SSO-konfigurationer kan läggas till för att stödja olika användargrupper, platser eller organisationsenheter

| Inloggningsmetod | Säkerhetskonsekvenser | Rekommendation |
|-------------|---------------------|----------------|
| **Adobe ID** | Organisationen har ingen kontroll över lösenordspolicy, MFA eller kontoåterställning. Ett komprometterat personligt Adobe-konto ger åtkomst till ALM-plattformen. | **REKOMMENDERAS INTE** för administrativa eller interna användare. Använd endast när enkel inloggning inte är tillgänglig. |
| **SSO (SAML 2.0/Federated ID)** | Autentiseringen styrs helt av organisationens IdP. MFA, sessionstimeout och policyer för villkorlig åtkomst tillämpas på IdP-nivå. Omedelbart återkallande vid användarens avgång. | **REKOMMENDERAS** för alla interna användare och administratörer. Ger den högsta nivån av organisatorisk kontroll. |
| **ID för Learning Manager** | Användarna hanterar lösenord själva utanför organisationens identitetsinfrastruktur. Det går inte att tvinga MFA via ALM. Lösenordsstyrkan beror på användarens beteende. | Godtagbart endast för externa användare. Inte lämplig för anställda eller administratörer. |

>[!CAUTION]
>
>Om inloggningsmetoden är inställd på Adobe ID för interna användare förlorar organisationen möjligheten att framtvinga multifaktorautentisering, kontrollera lösenordskomplexiteten eller omedelbart återkalla åtkomsten när en användare lämnar organisationen. Detta ökar avsevärt risken för obehörig åtkomst.

Mer information finns i [Anpassade roller](https://experienceleague.adobe.com/sv/docs/learning-manager/using/admin/custom-role).

### Multifaktorautentisering (MFA)

**Plats:** Adobe Admin Console > Inställningar > Säkerhet och integritet > Autentiseringsinställningar

MFA-tvång för **Adobe ID**- och **Enterprise ID**-användare har konfigurerats av **systemadministratören** i Adobe Admin Console, inte i själva ALM-programmet.  För användare med **Federated ID/SSO** används MFA hos organisationens identitetsleverantör.

- **Kräv 2FA:** Användare kan inte inaktivera tvåstegsverifiering. Ger ett starkt skydd mot referensstöld och nätfiske.
- **Valfritt 2FA:** Användare väljer om tvåstegsverifiering ska aktiveras eller inte. Betydligt svagare säkerhetsställning.
- **MFA har inte konfigurerats:** Enbart lösenord skyddar åtkomsten. Hög risk, särskilt för förvaltningskonton.

>[!IMPORTANT]
>
>Administrativa konton utan påtvingat makroekonomiskt stöd löper betydligt större risk för obehörig åtkomst. En komprometterad administratörsuppgift utan MFA ger fullständig kontokontroll, inklusive möjligheten att ändra alla säkerhetsinställningar.

### Sessionens livslängd och tidsgräns för inaktivitet

**Plats:** Adobe Admin Console > Inställningar > Säkerhet och integritet > Avancerade inställningar

**Systemadministratören** konfigurerar den maximala livslängden för aktiva sessioner och organisationens tidsgräns för inaktiva sessioner. Dessa inställningar gäller för alla användare, inklusive administratörer.

- **Maximal sessionslängd:** Framtvingar ny autentisering efter en angiven period oavsett aktivitet. Begränsar möjlighetens fönster om en session äventyras.
- **Maximal inaktiv tid:** Avslutar sessioner som har varit inaktiva under en angiven period. Skyddar mot oövervakade autentiserade sessioner på delade eller olåsta enheter.

## Inställningar för rolltilldelning och behörighetsomfång

Inställningarna för rolltilldelning och behörighetsområde avgör vem som har administrativ åtkomst i ALM och vad de kan göra. De här säkerhetsinställningarna hör till de mest effektfulla på plattformen. Endast administratörsrollen kan skapa, tilldela, ändra eller återkalla administrativa roller.

### Tilldelning av administrativa roller

**Plats:** ALM-administratör > Användare > Internt > Åtgärder > Tilldela roll / Ta bort roll

**Administratören** kan bevilja eller återkalla följande roller:

- **Administratör:** Fullständig åtkomst på kontonivå
- **Författare:** Åtkomst till att skapa innehåll
- **Anpassad administratör:** Administratörsbehörighet (se avsnitt 4.2)
- **Integreringsadministratör:** Integrering och API-åtkomst (se avsnitt 7)

| Inställning/åtgärd | Säkerhetskonsekvenser | Rekommenderad praxis |
|---|---|---|
| **Beviljar administratörsroll** | Fullständig kontokontroll. En användare med den här rollen kan ändra alla inställningar i det här dokumentet, inklusive att konfigurera om autentiseringen och återkalla andra administratörers åtkomst. | Tilldela endast ett minsta antal användare med ett verifierat affärsbehov. Upprätthåll en dokumenterad lista över alla innehavare av administratörsroller. |
| **Det går inte att återkalla roller vid avgång** | Avgående användare behåller åtkomsten till administrativa funktioner. Risk för obehörig åtkomst, dataexfiltrering eller sabotage. | Ta bort roller omedelbart när en användares anställningsuppgifter eller administrativa ansvarsområden ändras. Genomför regelbundna åtkomstgranskningar. |
| **Övertilldela breda roller** | Bred administrativ åtkomst ökar den potentiella effekten av ett skadat konto och minskar ansvarigheten för administrativa åtgärder. | Tillämpa principen om minst privilegier. Föredra omfångsroller (till exempel Anpassad administratör) där det är möjligt. |

### Anpassad konfiguration av administratörsroll

**Plats:** ALM-administratör > Användare > Anpassade roller > Skapa roll

Tillämpa principen om **minsta behörighet**. Använd **Anpassade administratörsroller** för att delegera specifika funktioner (se avsnitt 4.2).

**Administratören** kan skapa anpassade roller som beviljar en definierad delmängd administrativa behörigheter. Anpassade roller kan omfång till specifika användargrupper, kataloger eller funktionsuppsättningar, vilket begränsar räckvidden för delegerad administrativ åtkomst.

**Tillgängliga behörighetskategorier omfattar:**

- **Kontobehörigheter:** Åtkomst till systemövergripande konfigurationer som meddelanden, spelifiering, färdigheter och användarhantering.
- **Funktionsprivilegier (kärna):** Åtkomst till kataloger, rapporter och taggar.
- **Funktionsprivilegier (utbildningsobjekt):** Tillgång till kurser, certifieringar, utbildningsvägar och arbetsstöd.
- **Omfång:** Begränsa rollen till specifika användargrupper och/eller kataloger.

| Konfigurationsbeslut | Säkerhetskonsekvenser | Rekommenderad praxis |
|---|---|---|
| **Skapa en alltför bred anpassad roll** | En anpassad roll med orimliga behörigheter ger liten säkerhetsfördel jämfört med den fullständiga administratörsrollen och ökar sprängningsradien för ett skadat konto. | Omfång för anpassade roller till den minsta uppsättning behörigheter som krävs för den specifika funktionen. Föredrar roller med katalogomfattning och användargruppsomfattning. |
| **Bevilja åtkomst till inställningar för en anpassad administratör** | Anpassade administratörer med inställningsåtkomst kan ändra inloggningsmetoder, meddelandeinställningar och andra konfigurationer på kontonivå. | Bevilja bara inställningsåtkomst till anpassade roller när det uttryckligen krävs. Granska vilka anpassade roller som regelbundet har den här behörigheten. |
| **Granskar inte anpassade rolltilldelningar** | Odokumenterade eller ogranskade anpassade roller kan ackumuleras med tiden, vilket kan leda till att privilegier krypas. | Hämta den anpassade rollrapporten (**Användare > Anpassade roller > Hämta**) med jämna mellanrum och granska alla aktiva anpassade rolltilldelningar. |

## Inställningar för användaretablering och åtkomsthantering

Inställningarna för användaretablering styr hur användare läggs till på plattformen, hur länge de förblir aktiva och när deras data tas bort. Dessa inställningar konfigureras uteslutande av administratörsrollen och har direkta säkerhetskonsekvenser för dataexponering och åtkomstkontroll.

| Inställning | Plats | Säkerhetskonsekvenser | Rekommenderad standard |
|---|---|---|---|
| **Automatisk borttagning av inaktiva användare** | ALM-administratör > Inställningar > Allmänt | Utan automatisk borttagning ackumuleras inaktiva konton. Vilande konton är ett vanligt mål för obehörig åtkomst eftersom de kan förbli oövervakade. | Aktivera. Ange en kvarhållningsperiod som är anpassad till organisationspolicyn (t.ex. 90 dagars inaktivitet). |
| **Extern användarprofil upphör att gälla** | ALM-administratör > Användare > Externt > Lägg till profil | Externa användarprofiler utan förfallodatum förblir tillgängliga på obestämd tid. Partner eller leverantörer som inte längre behöver åtkomst behåller en aktiv startpunkt. | Ange ett förfallodatum på varje extern användarprofil när den skapas. |
| **Länkkontroller för självregistrering** | ALM-administratör > Användare > Internt > Lägg till > Självregistrering | Med en länk för självregistrering kan alla användare som har URL:en skapa ett elevkonto. Om det inte hanteras kan det leda till att obehöriga eller oväntade användare får plattformsåtkomst. | Generera självregistreringslänkar bara vid behov. Inaktivera eller återkalla oanvända länkar omedelbart. |
| **Pausa/återuppta extern profil** | ALM-administratör > Användare > Externa > Åtgärder > Paus | Att pausa en extern profil förhindrar nya användare från att registrera sig men påverkar inte dem som redan är registrerade. Om du inte pausar inaktiva externa profiler kan oavsiktliga registreringar vara tillåtna. | Pausa externa profiler när registrering inte längre behövs. Ta bort profiler som är permanent inaktiva. |
| **Ta bort och rensa användare** | ALM-administratör > Användare > Interna > Åtgärder > Ta bort / Användarrensning > Ta bort | Borttagna användare inaktiveras, men deras data bevaras. Om du rensar permanent tas alla användardata bort. Underlåtenhet att rensa avgående användare kan behålla känsliga utbildningsposter och PII utöver den föreskrivna kvarhållningsperioden. | Rensa användarposter i enlighet med företagets policyer för datalagring och sekretess. Rengöring är oåterkalleligt. |

>[!IMPORTANT]
>
>Rensning är permanent och oåterkallelig. Alla utbildningsposter, registreringsdata och användarinformation tas bort. Om en rensad användare refereras i anslutningskonfigurationer, kommer dessa anslutningar att inaktiveras. Bekräfta markeringen noggrant innan du utför en rensning.

## Inställningar för rapportering och dataåtkomst

Rapporterings- och dataåtkomstinställningarna avgör vilka användare som kan visa, generera och exportera plattformsdata. Felkonfiguration av dessa inställningar kan leda till exponering av känslig personlig, organisatorisk eller kompatibilitetsrelaterad information.

| Inställning | Plats | Säkerhetskonsekvenser | Rekommenderad standard |
|---|---|---|---|
| **Bevilja rapportåtkomst till anpassade roller** | ALM-administratör > Användare > Anpassade roller > Funktionsprivilegier > Rapporter | Rapporter kan innehålla personligt identifierbar information (PII), data om slutförande av kurs, bedömningspoäng och elevframsteg. Tillgången till rapporteringsfunktioner bör begränsas till användare med ett verifierat affärsbehov. | Bevilja rapportåtkomst endast till roller med ett specifikt, dokumenterat behov. Använd skrivskyddad åtkomst när skrivåtkomst inte krävs. |
| **Fullständig kontroll kontra skrivskyddad rapportomfattning** | ALM-administratör > Användare > Anpassade roller > Sammanfattningsrapport för konto | Fullständig kontroll över kontosammanfattningsrapport ger anpassad administratörssynlighet över alla användargrupper och kataloger, oavsett rollomfattning. Detta kan visa data utanför det avsedda omfånget för en administratörsroll med omfång. | Bevilja fullständig kontroll över sammanfattningsrapporten för konton endast till roller som verkligen kräver rapporteringssynlighet för hela organisationen. |
| **xAPI- och e-postrapportåtkomst** | ALM-administratör > Användare > Anpassade roller | xAPI-rapporter och e-postrapporter är endast tillgängliga för den fullständiga administratörsrollen. Dessa rapporter kan innehålla detaljerade beteendedata och kommunikationsdata. Åtkomsten är begränsad på grund av design. | Försök inte delegera åtkomst till xAPI eller e-postrapporter via anpassade roller. De är endast administratörer per design. |
| **Exporterade användardata** | ALM-administratör > Användare > Internt > Exportera användardata | Funktionen Exportera användardata genererar en hämtbar fil som innehåller alla interna användarposter. Dessa uppgifter måste hanteras i enlighet med organisationens säkerhets- och integritetspolicy. | Begränsa exportkapaciteten till behörig personal. Behandla exporterade data som känsliga. Den får inte lagras eller överföras utanför godkända system. |

## Inställningar för integrering och API-åtkomst

Inställningarna Integrering och API-åtkomst styr hur externa system ansluter till Adobe Learning Manager. Dessa inställningar ger åtkomst bortom ALM-användargränssnittet och kan, om de inte är konfigurerade, exponera plattformsdata och funktioner för obehöriga system.  Integreringsinställningarna hanteras av rollen Integreringsadministratör. Med rollen Fullständig administratör kan du granska, godkänna och återkalla registrerade program.

| Inställning | Plats | Säkerhetskonsekvenser | Rekommenderad standard |
|---|---|---|---|
| **API-programregistrering** | Integreringsadministratör > Program > Registrera | När du registrerar ett program skapas autentiseringsuppgifter för OAuth 2.0 (klient-ID och hemlighet) som kan användas för att komma åt ALM-data och funktioner programmatiskt. Överdrivet breda OAuth-omfång (till exempel läsning/skrivning av administratörsrollen) ger fullständig administrativ API-åtkomst. | Bevilja det minsta nödvändiga OAuth-omfånget. Granska och återkalla oanvända eller äldre programregistreringar med jämna mellanrum. Behandla klientautentiseringsuppgifter som känsliga hemligheter. |
| **OAuth-programomfattning** | Integreringsadministratör > Program > Registrera > Omfång | De tillgängliga OAuth-scopen sträcker sig från elevens läsåtkomst till administratörens läs- och skrivåtkomst. Med läs-/skrivbehörighet för administratörsroller kan ett program ändra data som en administratör kan ändra, inklusive användarroller och säkerhetsinställningar. | Använd det mest restriktiva OAuth-omfånget som uppfyller integreringens krav. Ge aldrig administratörsrollen läs-/skrivåtkomst om det inte är absolut nödvändigt. |
| **Anslutningskonfiguration (FTP, Salesforce, HRIS osv.)** | Integreringsadministratör > Anslutningar | Anslutningar möjliggör automatisk import och export av användardata, färdigheter och slutförda kurser. Felkonfigurerade anslutningar kan importera felaktiga användardata, tilldela oavsiktliga roller eller exportera känsliga data till obehöriga mål. | Granska alla aktiva anslutningskonfigurationer med jämna mellanrum. Se till att datakällor och destinationer är godkända. Inaktivera anslutningar som inte längre används. |
| **Konfiguration av webhook** | Integreringsadministratör > Webhookar | Webhookar skickar ALM-händelsedata i realtid (registreringar, slutföranden, användarändringar) till en angiven extern URL. En felkonfigurerad eller äventyrad webhook-slutpunkt kan resultera i dataexfiltrering eller exponering av känsliga elevhändelser. | Registrera endast verifierade, organisationsgodkända webhook-URL:er. Granska aktiva webhook-konfigurationer regelbundet. Ta bort inaktiva eller okända webhooks omedelbart. |
| **LTI-integrationskonfiguration** | Integreringsadministratör > LTI-integreringar | LTI-integrering gör att ALM kan agera som LTI-leverantör eller konsument, vilket gör att externa LMS-plattformar kan komma åt ALM-kurser. När LTI har aktiverats kan det inte inaktiveras. Exponerade LTI-autentiseringsuppgifter kan ge obehörig åtkomst till kursinnehållet. | Aktivera bara LTI när det finns ett verifierat integreringskrav. Behandla LTI-inloggningsuppgifter som känsliga. Dela bara autentiseringsuppgifter med auktoriserade LMS-administratörer. |

## Administrativt konfigurationsansvar och delat ansvar

Administrationsinställningarna i Adobe Learning Manager kan konfigureras av kunderna och ingår i de kundhanterade säkerhetskontrollerna i Adobe modell för delat ansvar.

| Adobe ansvar | Kundens ansvar |
|---|---|
| Säker drift av ALM-plattformen och underliggande infrastruktur. | Konfiguration av alla administrativa roller och behörigheter. |
| Tillämpning av den rollbaserade åtkomstkontrollmodellen (RBAC). | Välja och genomdriva lämpliga inloggningsmetoder och MFA. |

Mer information om Adobe Learning Manager säkerhetsrutiner finns i:

**Referens:** [Adobe Learning Manager-säkerhetsöversikt (PDF)](https://experienceleague.adobe.com/docs/learning-manager/assets/alm-security-whitepaper-2024.pdf?lang=sv-SE)

## Dokumentunderhåll

Det här dokumentet kan uppdateras regelbundet för att återspegla ändringar i Adobe Learning Manager-funktioner eller säkerhetsvägledning. Versionen och det senast uppdaterade datumet sparas i dokumentets metadata och i FedRAMP-auktoriseringspaketet. Användare bör läsa den offentligt tillgängliga versionen på Adobe Experience League för att säkerställa att de använder de senaste riktlinjerna.
