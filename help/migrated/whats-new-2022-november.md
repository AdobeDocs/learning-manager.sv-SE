---
title: Nyheter i den här versionen (november 2022)
description: Läs om de nya funktionerna och förbättringarna i Adobe Learning Manager
hidefromtoc: true
source-git-commit: 1da0911a4d0c2ae5cb01bbb2b7955675b0dfcdde
workflow-type: tm+mt
source-wordcount: '1994'
ht-degree: 1%

---

# Nyheter i den här versionen (november 2022)

<!--
IN-PROGRESS

<https://helpx.adobe.com/learning-manager/whats-new-nov-2022.html>
-->

## Konfiguration av flera SSO

Adobe Learning Manager stöder för närvarande en inloggningsmetod för interna användare och en inloggningsmetod för externa användare. Detta skapar begränsningar i fall där kunderna har sina anställda och sina egna kunder och kanalpartner på samma konto.

Eftersom Adobe Learning Manager har som mål att stödja flera typer av användargrupper som loggar in på plattformen, har det nu stöd för flera inloggningsmetoder via flera SSO-konfigurationer för både interna och externa användare.

Mer information finns i [Flera SSO-inloggningar](/help/migrated/administrators/feature-summary/multiple-sso-logins.md).

## Stöd för funktioner som inte är inloggade

Den inbyggda portalen för Adobe Learning Manager har nu stöd för icke-inloggade funktioner för att komma åt en utbildningsportal.

Eleverna kan nu upptäcka och komma åt utbildningswebbplatsen, kolla in olika kurser och tillgängligt innehåll och bestämma sig för att logga in för att delta i kurserna.

Den här funktionen gör det enklare att skapa en kundinriktad utbildningsportal där elever kan bläddra bland olika kurser utan att vara inloggade från början.

Mer information finns i [Ej inloggad för elever](/help/migrated/administrators/feature-summary/non-logged-in-experience-learners.md).

## Förbättringar av sidan Utbildningsöversikt

Sidan Utbildningsöversikt har nu ett uppdaterat användargränssnitt så att eleverna får en förbättrad upplevelse när de deltar i en kurs.

Övriga förbättringar:

* Bokmärk en utbildning.
* Rekommendation om relaterade kurser.
* Information om utbildningsväg för kurser och utbildningsvägar.
* Klickbara författarnamn.
* Brödsmulor för enklare navigering.

## Förbättringar av sidan Utbildningsöversikt

Sidan Utbildningsöversikt har nu ett uppdaterat användargränssnitt så att eleverna får en förbättrad upplevelse när de deltar i en kurs.

Övriga förbättringar:

* Bokmärk en utbildning.
* Rekommendation om relaterade kurser.
* Information om utbildningsväg för kurser och utbildningsvägar.
* Klickbara författarnamn.
* Brödsmulor för enklare navigering.

## Profilsida för författare

På profilsidan för författare visas all utbildning som har skapats av en viss författare.

Elever kan enkelt hitta författarspecifik information och all utbildning som skapas av författaren.

## Bokmärkta utbildningar

Elever kan spara (med knappen Spara) eller skapa ett bokmärke för dem från rutan Kurs eller översiktssidan. Alla bokmärkta kurser finns på elevens hemsida.

## Anpassning av spelare

I den här versionen kan du anpassa Fluidic-spelaren för att matcha varumärkningskraven för en kurs.

Du kan visa och dölja olika spelarinställningar och alternativ baserat på innehållskraven och bevilja kontroll till elever baserat på innehållstyp. Du kan tillämpa den här ändringen på både inbyggda och fjärradministrerade implementeringar.

Du kan ändra följande alternativ:

* Växla innehållsförteckning
* Anteckningar
* Språk
* Hastighet
* Undertext
* Volym
* Uppspelningskontroller

## Personifiering av elev och chef

Administratörer kan starta en personifierad session där de kan logga in för en annan användares räkning på sitt konto i rollen som elev och chef.

Mer information finns i [Personifiering av elev och chef](/help/migrated/administrators/feature-summary/impersonation-learner-manager.md).

## Andra förbättringar

### Granskningslogg för e-postmeddelanden

Administratörer kan nu komma åt alla e-postloggar som skickas från systemet via en rapport för e-postgranskningsspår.

Den här loggen innehåller alla data om e-postmeddelanden som skickats de senaste 30 dagarna och uppdateras varje dag. Dessutom innehåller rapporten information om till exempel levererad status, avsändare, mottagare, ämne och innehållsmetadata.

Hämta rapporten från Rapporter > Anpassade rapporter > Excel-rapporter > E-postrapport. Det visas ett meddelande via vilket du kan hämta rapporten.

Denna rapport består av följande fält:

* Tidpunkt för utlöst mejl (tidszonen UTC)
* Tidpunkt för senaste händelsestatus (tidszonen UTC)
* Leveransstatus
* Mottagarmejl
* Avsändarens användar-ID
* Ämne för mejlet
* Enhetstyp
* Enhetsnamn
* Enhets-ID

### Meddelande om elevs på väntelista

När en författare lägger till en ny instans kan författaren utlösa ett e-postmeddelande för att meddela elever på väntelistan om andra instanser. Eleverna får ett e-postmeddelande om ändringen.

### E-postmallar på instansnivå

Du kan anpassa e-postmeddelanden för varje instans av en utbildning.

Var författaren eller administratören kan lägga till en ny instans kan mallen för en enskild instans redigeras.

Om en kurs till exempel har olika målgruppstyper kan du ändra e-postmallen därefter.

![e-postmallar](assets/email-template.png)

Mallens prioritet anges nedan:

1. Mall på instansnivå
2. Mall för utbildningsnivå
3. Mall på kontonivå

### Kommentarer från instruktören när du accepterar ansökningar

Instruktörer kan nu lägga till kommentarer och samtidigt ta emot bidrag från elever. Eleven får ett e-postmeddelande och ett meddelande i appen (om det är aktiverat) när inlämningen har godkänts av instruktören. De inlämningsrelaterade kommentarerna finns i elevens betygsutdrag för både admin och elev.

### Förbättringar relaterade till sökning

En elevs senaste sökhistorik visas så att hen kan se alla tidigare sökningar.

Sökresultaten är nu konsekventa över allt formellt och informellt lärande (social utbildning). Resultaten inkluderar utbildning, social utbildning och matchningar för innehållsplats.

Sökningen är mer fokuserad och riktad, där du kan visa sökresultaten på tre platser, formellt lärande, socialt lärande och Content Marketplace.

![sök](assets/search-image.png)

#### Frasbaserad sökning

I den här versionen av Adobe Learning Manager har vi ersatt Typeahead-sökning med frasdriven sökning.

#### Senaste sökningar

En elev kan bara visa sina senaste sökningar i den aktuella sessionen.

### Katalog med kostnadsfria kurser för Content Marketplace

En uppsättning med 50 kostnadsfria kurser av hög kvalitet är nu tillgänglig direkt vid leverans från innehållets marknadsplats för elever.

### Stöd för indonesiska språket

Bahasa Indonesia läggs nu till som ett gränssnittsspråk i elevernas och chefernas appar.

### Obligatoriskt författarfält

När du skapar en kurs är fältet Författare obligatoriskt.

### Ändringar i Content Marketplace

* Nyskapade testkonton listar en ny katalog med 50 kostnadsfria kurser på Content Marketplace som är tillgängliga för användare.
* En elev kan nu se antalet sökresultat och länka inbäddade länkar för omdirigering till Content Marketplace.

### Integrerande mobiländringar

I den här versionen kan omslutande webbanvändare utföra de uppgifter som anges nedan:

* Skapa - enkätinlägg
* Redigera inlägg - alla typer, RTE
* Arbetsflöde för e-handel.
* Förhandsgranska modul: Eleverna får funktionen Modulförhandsgranskning i Mobile Immersive. Denna ändring gör det möjligt för elever att förhandsgranska modulen innan de registrerar sig för en kurs.
* Kopiera en URL.
* Radera en tavla.

### Ändringar i zoomkoppling

JWT-apptypen kommer att fasas ut i juni 2023. Vi rekommenderar att du skapar OAuth- eller OAuth-appar för server-till-server som ersätter funktionen hos ett JWT-program i kontot.

### Rapport för spelifiering

I den här versionen får du tillgång till en rapport som visar olika kurser där spelifiering har aktiverats.

### Importera språkinställning via CSV

När du importerar en CSV-fil innehåller CSV-filen fälten Gränssnittsspråk, Innehållsspråk och Tidszon.

Administratören kan också exportera rapporten, som innehåller samma fält som ovan.

* Gränssnittsspråk
* Språk för innehåll
* Tidszon

Förutom administratörer kan en anpassad administratör även exportera rapporten.

![språkrapport](assets/language-report.png)

#### Inverkan på lokalisering

* Kolumnnamnen kan inte lokaliseras och måste vara som de är (gränssnittsspråk, innehållsspråk, tidszon).
* Språkkoderna är skiftlägesokänsliga.
* Även om det inte finns någon begränsning för landskoden kan du bara ange språkkoden. Till exempel är både &quot;it_IT&quot; och &quot;it&quot; giltiga.
* Om det finns någon diskrepans i rapporten på grund av en felaktig språkkod fortsätter CSV-bearbetningen som vanligt och påverkar inte de andra posterna i CSV-filen. Språkinställningen för användaren med fel språkinställning uppdateras inte. Resten av data uppdateras.

## API-ändringar och -förbättringar

### VC-anslutningar

Om ett administratörs e-post-ID används för att konfigurera VC-kopplingen måste just den administratören ha behörighet för följande:

* Skapa ett möte
* Uppdatera ett möte
* Hämtar närvarorapport

När VC-mötet skapas eller uppdateras måste instruktörerna AVSLUTA mötet inom 30 minuter från den schemalagda sluttiden för mötet.

### Bokmärk

Följande API:er har lagts till för bokmärkning av en kurs på sidan Utbildningsöversikt:

* Hämta alla bokmärken: `primeapi/v2/bookmarks`
* Skapa ett bokmärke: `primeapi/v2/learningObjects/{id}/bookmark`
* Ta bort ett bokmärke: `primeapi/v2/learningObjects/{id}/bookmark`

### Stöd för metadata och innehåll på flera språk via migrering

För alla typer av utbildning som stöds på plattformen (kurser, utbildningsvägar, moduler, certifieringar och arbetsstöd) kan migrering till flera språk nu stödjas via CSV-filer med extra kolumner för ytterligare språk.

#### Förutsättningar

Skapa migreringsprojektet som en integrationsadministratör och dela sedan migrationProjectId med ALM-supportteamet, så att flaggan för flera språk kan aktiveras från servern.

#### Omfattning av migreringsobjekt för flera språk

* Modul
* Kurs
* Modulversion
* Certifiering
* Utbildningsprogram
* Arbetsstöd
* Version av arbetsstöd

#### CSV-specifikation

Adobe Learning Manager innehåller en uppsättning CSV-standardspecifikationer för migrering med flera språk. Det bästa sättet är att gå igenom dessa CSV-specifikationer innan du börjar migrera. Organisationens integrationsadministratör kan analysera de befintliga dataformaten och mappa dem så att de matchar de CSV-mallobjekt som Learning Manager tillhandahåller.

#### Ändringar med stöd för flera språk

* Kolumnen module_version stöds inte i module_version.csv och course_module.csv.
* Det går inte att uppdatera module_version i samma körning (i samma körning går det inte att migrera modulen med två versioner med samma modul).
* Uppdatering av innehåll eller metadata betraktas som modulversionsuppdatering från module_version.csv.
* Det går inte att stödja uppdateringen Job_Aid_Version via job_aid_version.csv

### Återkalla autentiseringstoken och cookie

Ett fjärradministrerat LMS-program får upp refresh_token vid den första inloggningen. Därefter används refresh_token för att generera access_token för dess klientprogram för att göra API-anrop. På samma sätt använder innehållsuppspelning oauth-slutpunkt för att generera cookie för att hantera uppspelning som involverar flera innehållsfiler och API-anrop som anropas av dessa filer med cookie. Cookien som genereras av oauth har samma giltighet som access_token, som är sju dagar. När en cookie har genererats går den inte att rensa, till skillnad från vanlig utloggning i webbprogram. Oauth-cookien och webbprogramcookien är två olika cookies och känner inte till varandra.

Så för att rensa cookie har vi infört en ny slutpunkt som återkallar refresh_token, cookie och både cookie- och uppdateringstoken.

**Detaljer**

**Slutpunkt**

`POST oauth/o/revoke`

**Frågeparametrar**

* `cookie=true|false` - anger att en cookie måste återkallas
* `refresh_token=true|false` - anger att uppdatera

**Text för begäran**

Text som krävs för att återkalla refresh_token eller (refresh_token och cookie)

```
{
      "client_id": <>,
      "client_secret": <>,
      "refresh_token": <>
}
Body required for revoking oauth cookie only
{
      "access_token": <>
}
```

### API:er som har publicerats

I den här versionen har vi gjort några API:er offentliga.

| API | Typ | Beskrivning |
|---|---|---|
| /social/search | GET | Sök i sociala medier. |
| /tillkännagivanden | GET | Få detaljerad information om tillkännagivandet på masthead som tilldelats eleven. |
| /tillkännagivanden/`{id}` | GET | Få detaljerad information om tillkännagivandet på masthead som tilldelats eleven. |
| /learningObjects/`{id}`/loResources/{loResourcesId} | GET | Ladda upp URL:en för filen för loResource av resurstypen &#39;Activity&#39; där filinlämning krävs. |
| /arbetsstöd/`{jobAidId}`/jobAidDownloads | GET | Ställ in nedladdningsrapport för arbetsstöd. |
| /bulkimport/startrun | POST | Kör massimport. |
| /bulkimport/cansync | GET | Synkronisera massimport. |
| /search | GET | DELETEMEBOB |
| /uploadInfo | GET | Hämta information om uppdatering av innehåll. |
| /uploadSigner | GET | Hämta en signatur för innehållet to_sign. |
| /avatar | POST | Uppdaterar elevens avatarbild med en ny bild. |
| /avatar | DELETE | Tar bort elevens avatarbild. |

### Salesforce-program

Inställningen **Ignorera högre ordningsföljd LO** alternativet måste vara aktiverat i Salesforce-programmet så att alla kurser, utbildningsprogram och certifikat kan visas samtidigt.

### API:er för anpassning av spelare

I den här versionen har vi tillhandahållit API:er för att anpassa en spelare. Du kan:

* Starta eller ladda spelaren.
* Gå till en viss modul.
* Växla innehållsförteckning.
* Ändra språk.
* Stäng spelaren.
* Spela upp, pausa, framåt, bakåt, sök, ändra volym eller ändra hastighet.
* Spela in händelser som avges från spelaren.

### Visa väntelistepositionen för en elev

GETEN /registreringar/{id}/waitlistPosition API under LO API hämtar väntelistepositionen för en användare för en angiven registrering.

### Inlämning av slutförandedatum i externa certifieringar

Attributet /primeapi/v2/learningObjects/certification:xxxxx API kommer att ha attributet completionDateSameAsApprovalDate för att ange att certifikatet har slutförandedatum för certifieringen aktiverat för eleven eller inte tillsammans med flaggan true/false.

### Hämta LO-förhandsgranskningsdata

GETEN /preview/learningObjects/{id} API har lagts till för att få förhandsgranskningsinformation om ett utbildningsobjekt.

### Flytta externa användare i profiler

Inställningen `PUT primeapi/v2/externalProfiles/{currentep}/users/{userid}?` anrop hjälper till att flytta en användare till en annan extern profil genom att ange ett nytt externalProfile-id.

### Lägg till användare i externa profiler

Inställningen `POST /externalProfiles/{id}/users` lägger till externa användare i en extern profil.

## Versionsinformation

Mer information om aktuella och tidigare versioner av Learning Manager-webbappen och enhetsappen finns i [Versionsinformation](/help/migrated/release-note/release-notes.md).

## Felkorrigeringar

Om du vill se de fel som är åtgärdade i den här uppdateringen, se [Buggar i fast lista](release-note/release-notes.md#bugs-fixed-in-this-release).

## Systemkrav

[Systemkrav för Learning Manager](/help/migrated/system-requirements.md)
