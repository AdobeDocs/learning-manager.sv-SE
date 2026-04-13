---
description: Läs om de nya funktionerna och förbättringarna, inklusive API- och webhookändringar, i april 2026-versionen av Adobe Learning Manager
jcr-language: en_us
title: Nyheter i Adobe Learning Manager-versionen från april 2026
exl-id: da46f186-3ff3-422a-af49-31c7405fd584
source-git-commit: 971a9c79fc2b831b990e30a44a2eeab5d5c5ce63
workflow-type: tm+mt
source-wordcount: '1768'
ht-degree: 0%

---

# Nyheter i Adobe Learning Manager-versionen från april 2026

**För elever:** Fluidic-spelaren visar nu nästa modulnamn och en knapp för att avsluta. Spelarens språk kan ställas in via LTI för en konsekvent upplevelse på olika plattformar. Den anpassade parameterns namn är &quot;locale&quot; och den accepterar språkkoden. Till exempel locale=fr-FR. Captivate-innehåll innehåller en enhetlig innehållsförteckning, slutförandeskalor på bildnivå och tillförlitliga anteckningsexporter. Flerspråksstöd finns tillgängligt för arbetsstöd, checklistefrågor och videotextspår (VTT). AI-assistenten hjälper elever att få svar inom utbildningsupplevelsen.

**För administratörer och författare:** Zoom-kopplingen stöder flera samtidiga VILT-sessioner. Delade kurser i kollegiala konton visar den verkliga författaren istället för &quot;Extern författare&quot;. Administratörer kan begränsa när moduler kan startas. Förfallodatum för utbildningsobjekt visas i elevens API:er. Checklistmoduler har stöd för viktad poäng, flerspråkig frågetext och valfria granskningskommentarer. Anpassade certifikat har en dra och släpp-redigerare med dynamiska fält och AI-genererade bakgrunder. Med den icke inloggade Experience Builder kan du skapa offentliga utbildningssidor utan att behöva logga in.

**För instruktörer:** Generera QR-koder för instansregistrering och sessionsnärvaro. Lägg till kommentarer eller feedback under utvärderingen av checklistan.

**Rapportering och analys:** SCORM-innehåll kan nu rapportera flera frågeformulärsförsök i L2-rapportering. Beräkning av använd utbildningstid har förbättrats i elevens betygsutdrag. Rapporter om utbildningstranskribering för administratörer uppdateras. Avancerade sökförbättringar är tillgängliga.

**Inloggningsmetod:** Lär dig hur OpenID Connect-inloggning fungerar i Adobe Learning Manager för elever, författare och administratörer. OpenID Connect (OIDC) är en vanlig inloggningsmetod som bygger på webbstandarder. Många organisationer använder
en identitetsleverantör (till exempel Okta, Google Workspace eller Microsoft Entra ID) för anställda och partner.

Visa [logga in med OIDC](/help/migrated/oidc.md) om du vill ha mer information.

## Webhookar och migrering i alternativa tecken och motsvarande

### Webhooks

När en elev slutför en kurs via ett alternativt system eller en relation, utlöser ALM en webhook-händelse som är separat från standardwebhooken för slutförande av kurs. Detta garanterar att integreringar kan svara olika på olika kompletteringar där så behövs. Webhook-händelser utlöses också när retroaktiv slutföring eller retroaktiv inslutförande sker, vilket omfattar historiska uppdateringar samt relationsändringar.

Mer information finns i [webhookar](/help/migrated/integration-admin/feature-summary/webhooks.md#webhooks-for-alternates).

### Migrering

Den CSV-baserade datamodellen och migreringsbeteendet för att införa ekvivalens för utbildningsobjekt (LO) i systemet beskrivs i [Webhooks](/help/migrated/integration-admin/feature-summary/migration-manual.md#migration-for-alternates-and-equivalents).

## Rensa borttagna användare automatiskt

Raderingen av borttagna användare automatiskt är en funktion som rensar data för användare som redan har raderats i ALM. Rensning sker efter en konfigurerbar lagringsperiod, med fokus på gruppåtgärder så att stora kundkonton kan hanteras effektivt utan att försämra prestanda.

Visa [Automatisk rensning av borttagna användare](/help/migrated/administrators/feature-summary/purge-users.md#auto-purge-of-deleted-users) om du vill ha mer information.

## Ange åtkomsttidskontroll för modul

Förbättringen gör att författare och administratörer i Adobe Learning Manager kan definiera ett tidsfönster då elever tillåts starta en modul. Utanför det konfigurerade start-/slutfönstret syns modulen i kursstrukturen, men eleverna kan inte initiera den.

Mer information finns i [Ange åtkomsttidskontroll för modul](/help/migrated/administrators/feature-summary/module-access-time-control.md).

## Ändringar i elevens betygsutdrag

Den här versionen förbättrar rapporten Utbildningsutskrifter (LT) med tydligare hörbarhet och kompatibilitetsstöd.

* En ny kolumn för slutförandemetod i Admin LT visar om slutföranden var direkta, alternativa eller återkallade, medan alternativa slutföranden nu påverkar status, slutförandedatum och slutförandekälla med ärvda datum från källutbildningar och uppdatering när källor återkallas eller direkta slutföranden sker.
* Återkallade alternativ justerar automatiskt status, slutförandedatum och slutförandekälla när alla kvalificerade relationer tas bort med retroaktiv inslutförande aktiverat.
* Granskarfeedback från checklistmoduler är standardiserad under den omdöpta granskarens kommentarskolumn mellan admin- och elevlistor och alla exportkanaler.
* Slutligen är det nu bättre att skilja aktiv tid från inaktiv tid i beräkningarna av inlärningstiden, vilket förbättrar precisionen i engagemang och rapportering av regelefterlevnad.

Se [Ändringar i rapporten Elevens betygsutdrag](/help/migrated/administrators/feature-summary/reports/changes-in-learner-transcript.md) för mer information.

## Checklista med kommentarsfunktion för granskare

Med den här funktionen kan granskare lägga till kommentarer eller feedback under utvärderingen av checklistan. Du kan ge personlig och användbar feedback för varje elev. Du kan även välja att visa ditt namn med dina kommentarer för genomskinlighet. Alla kommentarer sparas i elevens betygsutdrag och ingår i checklisterapporter.

Mer information finns i [Konfigurera checklista med kommentarer](/help/migrated/authors/feature-summary/courses.md#checklist-with-commenting).

## Stöd för checklista på flera språk

Med den här funktionen kan du skapa och hantera checklistmoduler på flera språk. Varje checklista med frågor, instruktioner och utvärderingskriterier kan översättas så att granskare och elever interagerar med checklistan på det språk de föredrar. I systemet visas checklistan på användarens valda innehållsspråk, vilket förbättrar tillgängligheten och efterlevnaden för globala team.

Visa [Skapa en flerspråkig checklista i moduler](/help/migrated/authors/feature-summary/courses.md#create-a-multi-language-checklist)

## Checklista för frågeviktning för instruktörsutvärderingar

Med den här funktionen kan du tilldela olika maxpoäng (viktning) för varje checklistefråga. Du kan återspegla den varierande betydelsen eller svårigheten av varje fråga, som stöder mer exakta och meningsfulla utvärderingar. Systemet beräknar den totala poängen baserat på dina indata och avgör om eleven klarar eller misslyckas enligt de kriterier du ställer in.

Visa [Skapa viktade checklistefrågor](/help/migrated/authors/feature-summary/courses.md#how-to-create-a-weighted-checklist)

## Anpassade certifikat

Med anpassade certifikat i Adobe Learning Manager (ALM) kan administratörer och författare designa, hantera och utfärda anpassade certifikat för elever.

I funktionen ingår en dra och släpp-redigerare, dynamiska fält, flerspråkigt stöd och AI-genererade bakgrunder, vilket gör att organisationer kan skapa varumärkta certifikat utan teknisk expertis.

Visa [Utforma anpassade certifikat](/help/migrated/administrators/feature-summary/create-customize-certificate.md)

## Upplevelser som inte är inloggade i Experience Builder

Med den icke-inloggade upplevelsen i Experience Builder kan organisationer visa sitt utbildningsinnehåll och sina portalsidor för alla besökare, inklusive dem som inte har loggat in. Den här funktionen är utformad för att locka, informera och engagera blivande elever genom att erbjuda en smidig och varumärkt förhandsvisning av dina utbildningserbjudanden innan de måste logga in eller registrera sig.

Visa [Ej inloggad upplevelse i Experience Builder](/help/migrated/administrators/feature-summary/experience-builder/non-logged-in-experience.md)

## Avancerade sökförbättringar

Sökresultaten i Avancerad sökning är nu mer exakta och relevanta. Exakta nyckelordsmatchningar rankas högre över både sökning i innehåll och metadata, vilket gör det lättare för elever att hitta exakt det de söker efter.

Elever kan nu också se registrerade utbildningsobjekt i sökresultat, även om de inte ingår i en tillgänglig katalog, vilket säkerställer att inget relevant innehåll missas. Dessutom har rangordningen av arbetsstöd förbättrats både för avancerad sökning och sökning i innehåll, och de mest relevanta resurserna hittas snabbare.

## Flerspråkigt arbetsstöd

Med hjälp av flerspråkiga arbetsstöd i Adobe Learning Manager (ALM) kan författare och administratörer tillhandahålla stöddokument, guider eller resurser på flera språk i en och samma arbetsstödspost. Elever i olika regioner kan komma åt relevant material på sitt önskade språk, vilket förbättrar förståelse, efterlevnad och användarupplevelse.

Titta i [Lägg till flerspråkiga arbetsstöd](/help/migrated/authors/feature-summary/job-aids.md#create-a-multilingual-job-aid) om du vill ha mer information.

## Stöd för flerspråkiga videotextspår (VTT) (för författare)

Stöd för flerspråkiga videotextspår (VTT) i Adobe Learning Manager gör det möjligt för författare att tillhandahålla undertexter och bildtexter för video- och ljudinnehåll på flera språk. Den här funktionen effektiviserar lokaliseringen, gör utbildningen tillgänglig för en global publik och ser till att tillgänglighetskrav uppfylls. Författare kan automatiskt generera, översätta, granska och redigera VTT-filer direkt inom plattformen.

Mer information finns i [Flerspråkigt VTT-stöd](/help/migrated/authors/feature-summary/content-library.md#multi-lingual-vtt-support).

## Visa originalförfattare för delade kurser i kollegiala konton

När en kurs delas via katalogen till ett kollegialt konto, ger Adobe Learning Manager författaren etiketten &quot;Extern författare&quot; i vyn Elev, Administratör och Författare för det mottagande kontot. Detta kan innebära utmaningar för elever och administratörer, särskilt i stora företag, eftersom det blir svårt att identifiera och kontakta rätt innehållsägare när problem eller frågor uppstår.

Förbättringen gör att upphovsinformation bevaras och visas för delade kurser i kollegiala konton, i stället för att ersättas av en allmän platshållare.

### Nyheter

Visa det faktiska författarnamnet för delade kurser i kollegiala konton

För kurser som delas via externa kataloger eller kollegiala kataloger visas nu det ursprungliga författarnamnet från källkontot i det mottagande kontot i stället för &quot;Extern författare&quot;.

Detta gäller

* Elevapp (kurskort eller kursinformation).
* Administratör och författare visar när de förhandsgranskar som elev.

Visa [Visning av författarnamn för delade kurser](/help/migrated/administrators/feature-summary/peer-account.md#author-name-display-for-shared-courses-including-previously-acquired-courses) om du vill ha mer information.

## Motsvarigheter och alternativ

Leverera en friktionsfri utbildningsupplevelse och ta bort överflödig utbildning med motsvarigheter och alternativ i ALM. Med den här nya funktionen kan administratörer konfigurera enkelriktade (alternativa) eller dubbelriktade (motsvarande) regler, där slutförande av en utbildning automatiskt ger alternativt slutförande av en annan. Funktionen är utformad för att effektivisera stora inlärningsekosystem och ser till att elever hoppar över innehåll de redan har bemästrat. Dessutom minskar organisationen administrationssupportbiljetterna drastiskt, eliminerar manuella åsidosättningar och upprätthåller en renare, mer exakt elevpost.

Mer information finns i [Motsvarigheter och alternativ](/help/migrated/administrators/feature-summary/alternates-equivalence.md).

## QR-koder för instruktör för instansregistrering och sessionsnärvaro

Instruktörer kan själva generera QR-koder för:

* Registrering av kursinstans,
* Sessionens närvaro, eller
* Registrering + närvaro tillsammans

på sessionsnivå. Det är utformat för situationer där elever går in i ett fysiskt klassrum eller ett hybridklassrum och kräver ett snabbt självbetjäningsalternativ för att registrera och registrera sin närvaro med en QR-kod.

Visa [Hämta QR-koder för registrering och närvaro för elever](/help/migrated/instructors/feature-summary/learners.md#download-qr-codes-for-learner-enrollment-and-attendance) om du vill ha mer information.

## Kalenderinbjudningar (ICS) med sessionslänkar

Adobe Learning Manager innehåller länken **Anslut till session direkt i kalenderinbjudningar (ICS-filer)** som skickas till elever och instruktörer. Det gör att deltagarna kan ansluta till sessioner direkt från sin kalender utan att söka efter e-postmeddelandet för sessionen.

Den här förbättringen förbättrar upplevelsen för kalenderklienter som **Gmail** och **Outlook**.

Visa [kalenderinbjudningar med sessionslänkar](/help/migrated/instructors/feature-summary/learners.md#joining-a-session-from-gmail) om du vill ha mer information.

## AI-assistent för elever

AI-assistenten (beta) för elever hjälper dem att snabbt hitta svar från det tilldelade utbildningsinnehållet utan att bläddra igenom hela kurser. Du kan ställa frågor på ett enkelt språk och få korrekta, fokuserade svar med källänkar till relevant kursinnehåll.

Funktioner, scenarier som stöds och begränsningar kan ändras allt eftersom funktionen utvecklas. AI Assistant är en generativ AI-driven chattföljeslagare i Adobe Learning Manager som levererar snabba, exakta svar med hjälp av ditt betrodda utbildningsinnehåll. Det innehåller citat så att du alltid vet källan till informationen.

Visa [AI-assistent för elever](/help/migrated/learners/feature-summary/learner-ai-assistant.md)


## API-ändringar i versionen

I aprilversionen 2026 av Adobe Learning Manager introduceras fokuserade förbättringar av det offentliga API:t kring alternativ och motsvarigheter, tidsbegränsad åtkomst till innehåll, innehållsdrivna frågeformulärsförsök, icke-inloggade upplevelser och arbetsstödshantering. Ändringarna är utformade för att i stor utsträckning vara bakåtkompatibla samtidigt som de möjliggör mer exakta integreringar.

Visa [API-ändringar i aprilversionen](/help/migrated/api-changes-alm.md)

## Systemkrav

Visa [Systemkrav för Adobe Learning Manager](/help/migrated/system-requirements.md).

## Versionsinformation

Läs [versionsinformationen](/help/migrated/release-note/release-notes.md) om du vill ha de senaste versionsuppdateringarna.

## Tidigare utgåvor av Adobe Learning Manager

* [Adobe Learning Manager oktober 2025-versionen](/help/migrated/whats-new-october-2025.md)
* [Adobe Learning Manager-versionen från maj 2025](/help/migrated/whats-new-may-2025.md)
