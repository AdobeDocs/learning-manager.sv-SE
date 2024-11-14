---
description: Läs om de nya funktionerna och förbättringarna i november 2024-versionen av Adobe Learning Manager
jcr-language: en_us
title: Sammanfattning av nya funktioner
exl-id: 4dfe0e31-d202-4a6e-8c4f-43851218699f
source-git-commit: a19e538ed152b3435adf2f3405bff1ae75576978
workflow-type: tm+mt
source-wordcount: '3053'
ht-degree: 1%

---

# Sammanfattning av nya funktioner {#new-features-summary}

Läs om de nya funktionerna och förbättringarna i november 2024-versionen av Adobe Learning Manager.

* **AI-baserad sökning:** Kombinerar lexikala och semantiska sökningar för smartare, kontextmedvetna resultat.
* **Webhooks**: Integrera med webhooks för att skicka realtidsinformation till specifika URL:er.
* **Utbildningsverktyg och interoperabilitet (LTI)**: Stöder LTI för kompatibilitet med andra LMS-plattformar.
* **Integrering med autentiseringsuppgifter**: Hantera och dela externa utmärkelsetecken via Kreditera.
* **Förbättringar av efterlevnadstavlan**: Dela instrumentpaneler med andra administratörer och ange standardwidgetar för efterlevnad på elevens startsidor.
* **Stöd för flera språk**: Skapa språkspecifika instanser för klassrums- och virtuella klassrumsmoduler.
* **Anpassade roller**: Förbättrad kontroll över användarroller och behörigheter.
* **Slutförandekommentarer**: Lägg till kommentarer när du markerar elever som slutförda.
* **Användargruppsrapport**: Hantera användargrupper med detaljerade rapporter.
* **Väntelisterapport**: Ladda ned väntelistan med elever för kursinstanser.
* **Tillgänglighetsförbättringar**: Stöd för alt-text på maskhuvuden och företagslogotyper.
* **Stöd för hindi**: Stöd för gränssnittsspråk för hindi.
* **Svordomskontroll**: Blockera sociala inlägg som innehåller förbjudna ord.
* **Optimering av e-postmallar**: Kombinerade och optimerade e-postmallar för instruktörstilldelningar och sessionsavbrott.
* **Kriterier för slutförande av MS Teams**: Ange lägsta närvarotid för VILT-sessioner.
* **Nya migreringsarbetsflöden**: Migreringsändringar omfattar kriterier för slutförande av kurser och moduler och migrering av moduler till mappar.

## AI-baserad sökning i Adobe Learning Manager

Adobe Learning Manager gör om det sätt på vilket elever söker kurser eller utbildningar. Den introducerar en AI-driven sökfunktion som kombinerar lexikala och semantiska sökningar. Sökningen är nu smartare eftersom den söker efter specifika termer och förstår sammanhang och avsikt bakom dem. Den avancerade sökningen förstår innebörden av din fråga och ger relevanta resultat. Det identifierar huvudfokus i sökningen för att ge dig den mest kompletta uppsättningen resultat.

Läs den här artikeln [Avancerad sökning](/help/migrated/learners/feature-summary/advanced-search.md) om du vill ha mer information.

## Webhooks

Med Adobe Learning Manager kan du integrera med webhookar och skicka realtidsinformation, till exempel kursregistrering, kursskapande och annan information, till en specifik URL.

Med en webhook i ALM kan en enhet automatiskt skicka data till ett annat program via HTTP. Det kommer att göra det möjligt för ett program att förse andra program med information utan att ständigt begära det. Om en användare till exempel slutför en kurs i ett system för hantering av inlärning (LMS) kan en webhook automatiskt skicka den informationen till en annan plattform, till exempel ett CRM- eller rapporteringsverktyg. Webhooks används ofta i integreringar för att automatisera processer och minska behovet av manuella uppdateringar mellan system. Konfigurera webhooks genom att ange en återanropsadress som du vill skicka data till.

Läs den här artikeln [Webhookar](/help/migrated/integration-admin/feature-summary/webhooks.md) om du vill ha mer information.

## Interoperabilitet för utbildningsverktyg

Adobe Learning Manager stöder nu LTI för att förbättra interoperabiliteten mellan Adobe Learning Manager och andra system för hantering av inlärning (LMS).

### Vad är LTI?

LTI (Learning Tools Interoperability) är en standard som gör att externa verktyg och innehållsleverantörer kan ansluta till ett system för hantering av inlärning (LMS). Användarna kan komma åt externt utbildningsinnehåll från externa innehållsleverantörer direkt i sitt LMS utan att logga in eller gå till ett annat LMS.

LTI som verktygsleverantör: LTI som verktygsleverantör tillåter externa system att integreras med ett LMS. Adobe Learning Manager fungerar som en LTI Tool Provider, och ger andra LMS-plattformar tillgång till kurser, certifikat och utbildningsvägar från Adobe Learning Manager direkt i deras LMS.

LTI som verktygskonsument: LTI som verktygskonsument låter LMS integrera externa verktyg via Learning Tools Interoperability (LTI). I detta scenario är LMS en konsument av tjänster som tillhandahålls av externa verktyg. Adobe Learning Manager fungerar som en LTI Tool-konsument och kan integrera utbildningsverktyg från tredje part. Detta ger Adobe Learning Manager-elever möjlighet att delta i kurser, certifikat eller utbildningsvägar från externa verktyg i Adobe Learning Manager.

Läs den här artikeln [Interoperabilitet för utbildningsverktyg](/help/migrated/integration-admin/feature-summary/learning-tools-interoperability.md) om du vill ha mer information.

## Credly

Med hjälp av kredit kan en administratör i ALM hantera och dela externa utmärkelsetecken från plattformen i olika sociala mediekanaler.

### Vad är Credly?

Credly är en digital inloggningsplattform som gör det möjligt för elever och organisationer att tjäna in, dela och verifiera yrkesmässiga prestationer, som märken eller certifieringar. Elever kan hantera och dela utmärkelsetecken via sin kreditprofil på sociala medier och andra platser.

### Integrera med Adobe Learning Manager

Lägg först till kreditkontakten i Adobe Learning Manager (ALM). Migrera sedan de befintliga utmärkelsetecknen från Creded för att säkerställa kontinuiteten för elevprestationer. Slutligen kan du skapa en kompetens i Adobe Learning Manager och hitta rätt utbildningsväg för att förbättra elevutvecklingen och erkännandet.

Läs den här artikeln [Tillfälligt](/help/migrated/integration-admin/feature-summary/credly-integration.md) om du vill ha mer information

## Efterlevnadstavla

I den här versionen kan administratörer nu dela kontrollpanelen med andra administratörer, anpassade administratörer och butikschefer, vilket ger dem omedelbar tillgång till efterlevnadstavlorna. De kan nu ställa in standardwidgeten för efterlevnad på elevens startsida, så att eleverna kan spåra sina efterlevnadskrav. Se den här artikeln [Efterlevnadstavla](/help/migrated/administrators/feature-summary/reports.md#share-compliance-dashboard-with-admins-and-custom-admins) för mer information.

## Stöd för flera språk

Med Adobe Learning Manager (ALM) kan författare nu skapa språkspecifika instanser med språktaggning för klassrums- och virtuella klassrumsmoduler. Elever kan komma åt CR/VC-moduler på önskat språk. En författare kan till exempel skapa en CR/VC-modul med två instanser: en på engelska och en på franska. Elever kan välja instanserna på sitt önskade språk.

Se den här artikeln [Lägg till utbildningsobjekt på olika språk](/help/migrated/authors/feature-summary/add-new-language-learning-objects.md#multi-language-support-for-crvc-instances-with-language-tagging) för mer information.

## Anpassade roller

Med anpassade roller kan administratörer definiera specifika roller och ansvarsområden för olika användargrupper, vilket ger bättre hantering och kontroll. I den här versionen förbättrar ALM anpassade roller genom att ge mer detaljerad kontroll över följande avsnitt.

* Användare
* Kurser
* Utbildningsvägar
* Certifieringar
* Arbetsstöd
* Kataloger

Administratörer kan tilldela exakta behörigheter baserat på användaransvar och se till att varje grupp bara har tillgång till relevanta funktioner och innehåll. Dessa förbättrade kontroller möjliggör mer detaljerad hantering av viktiga avsnitt.

Logga in som administratör och gå till **[!UICONTROL Users]** > **[!UICONTROL Custom Roles]** för att skapa och hantera anpassade roller.

Läs den här artikeln [Anpassade roller](/help/migrated/administrators/feature-summary/custom-role.md) om du vill ha mer information.

## Kommentarer till slutförande

Administratörer kan nu lägga till kommentarer när de markerar elever som slutförda i kurser, utbildningsvägar eller certifieringar. Administratörer kan lägga till kommentarer för en eller flera elever samtidigt och kommentarerna visas i rapporten [Elevens betygsutdrag](/help/migrated/administrators/feature-summary/reports.md#learner-transcripts).

Mer information finns i den här artikeln [Kommentarer till slutförande](/help/migrated/administrators/feature-summary/courses.md#completion-comments).

## Rapport över användargrupp

Adobe Learning Manager nya **[!UICONTROL User Group Report]** hjälper till att hantera användargrupper genom att synliggöra grupper som lämnas ohanterade när administratörer lämnar organisationen. Administratörer kan komma åt rapporterna under avsnittet **[!UICONTROL Users]** > **[!UICONTROL User Group]**. Den innehåller detaljerad information om varje grupp, inklusive:

* Typ av användargrupp
* Gruppnamn
* Beskrivning
* Skapad av (namn)
* Skapad av (e-post)
* Skapad den (tidszonen UTC)
* Antal användare

Läs den här artikeln [Rapport om användargrupper](/help/migrated/administrators/feature-summary/add-users-user-groups.md#user-group-report) om du vill ha mer information.

## Väntelisterapport

Med Adobe Learning Manager nya **[!UICONTROL Waitlist Report]** kan administratörer hämta elevlista på väntelistan för alla instanser av en kurs. Administratörer och instruktörer kan komma åt den här rapporten från avsnittet **[!UICONTROL Waitlist]** på sidan **[!UICONTROL Course]** eller **[!UICONTROL Session Overview]**. Väntelisterapporten kan hämtas från avsnitten Admin och Instruktör.

Följande kolumner är tillgängliga i väntelisterapporten:

* Kursnamn
* Instansnamn
* Instans-ID:
* Instansstatus
* Användarnamn
* E-post
* Unikt användar-ID
* Datum registrerad (tidszonen UTC)
* Status
* Väntelistenummer
* Väntlistegräns
* Platsbegränsning

Se de här artiklarna [Väntelisterapport](/help/migrated/administrators/feature-summary/courses.md#waitlist-report) och [Väntelisterapport](/help/migrated/instructors/feature-summary/learners.md#waitlist-report) för att hämta rapporten från avsnittet Administratör och instruktör.

## Tillgänglighet på elevens startsida

Adobe Learning Manager stöder nu alt-text för alla mastheads för att förbättra tillgängligheten för elever. Det gör att elever med särskilda behov kan använda skärmläsare för att läsa alt-texten och förstå bilden. Du kan välja flera språk och ange alt-text för varje språk. Se till att du lägger till alt-texten på respektive språk. Se till att företagslogotypen på ditt konto också innehåller alt-text med företagsnamnet.
Läs den här artikeln [Tillkännagivande](/help/migrated/administrators/feature-summary/announcements.md#masthead) om du vill ha mer information.

## Stöd för hindi

Adobe Learning Manager introducerar nu hindi som ett av plattformens gränssnittsspråk och stöder plattformens tillväxt i Indien. Stöd för infödda hindi-talare säkerställer att alla funktioner, rapporter och den övergripande användarupplevelsen är fullt tillgängliga för användarna.

Gör så här för att ändra gränssnittsspråk:

1. Logga in som **[!UICONTROL Admin]**.
2. Gå till **[!UICONTROL Profile Settings]** > **[!UICONTROL Interface Language]**.
3. Välj **[!UICONTROL Hindi]** som gränssnittsspråk.


## Svordomskontroll för inlägg i sociala medier

Adobe Learning Manager blockerar nu inlägg i sociala medier i appen Elever med förbjudna ord. Detta hjälper till att hålla saker och ting professionella och överensstämmande, särskilt inom känsliga områden som hälso- och sjukvård.

## Optimering av e-postmall

### Skicka e-post till elever när en instruktör har tilldelats

De befintliga e-postadresserna **[!UICONTROL You have been added as an Instructor]** och **[!UICONTROL VCProvider Session Details]** har kombinerats till ett e-postmeddelande **[!UICONTROL You have been added as a UserType]**. **[!UICONTROL UserType]** blir antingen **[!UICONTROL Instructor]** eller **[!UICONTROL Organizer]**, baserat på användarens roll. Dessa e-postmeddelanden var inte tillgängliga i användargränssnittet förut. De har nu kombinerats i ett enda e-postmeddelande och lagts till i användargränssnittet. Administratörer kan komma åt den här mallen i avsnittet **[!UICONTROL Email Template]**. Det aktiveras som standard för alla nya och befintliga konton, men administratörer kan inaktivera eller aktivera det från samma avsnitt. Det här e-postmeddelandet skickas när en session skapas och en instruktör tilldelas, oavsett om det är för sessioner som Zoom, Teams, Connect eller andra tjänster.

### Skicka e-post till elever när en session avbryts

Instruktörer som tas bort från en session får nu endast ett e-postmeddelande om annullering av session. Tidigare har de fått både en annullering och en uppdatering via e-post. Instruktörer som blir kvar i en session får ett e-postmeddelande om en sessionsuppdatering tillsammans med en ny inbjudan till sessionen.

## Kriterier för MS Teams-slutförande

För närvarande anges elever som närvarade även om de deltar i en vilt-session (Virtual Instructor-Led Training) under bara några sekunder. I den här versionen har vi infört kriterier för slutförande av Teams-moduler för att säkerställa en mer korrekt närvaro. Författare kan nu ange en minimitid som elever måste tillbringa i en VILT-session för att deras närvaro ska räknas.

Det här är en serverdelsfunktion som är inaktiverad som standard. Kontakta din CSM för att aktivera den.

## Migreringsändringar

Följande ändringar görs i arbetsflödet för migrering:

* Migrera moduler till specifika mappar.
* Tilläggskriterier för moduler.
* Tillagda kriterier för slutförande av kurser

### Ändringar i modulmigrering

När du migrerar moduler till ALM sparas de som standard i den gemensamma mappen. I den här versionen har vi lagt till en ny kolumn med namnet `folder` i filen [module_version.csv](assets/module_version.csv). Administratörer kan använda den här kolumnen för att ange mappnamnet dit modulerna ska gå efter migreringen. Administratörer kan också placera en enskild modul i flera mappar genom att lista mappnamnen avgränsade med kommatecken.

Mappkolumnen använder strängdatatypen och det är en valfri kolumn. Följande villkor gäller för mappkolumnen:

* Mappnamnet som du lägger till bör vara en befintlig innehållsmapp i ALM-kontot.
* Värdena ska vara kommaavgränsade.
* Om du lägger till ett nytt mappnamn för en modul som redan finns i en annan mapp kommer det nya värdet inte att skriva över eller ersätta den tilldelade mappen. Modulen läggs till i den nya mappen och förblir dessutom tillgänglig i den befintliga mappen.
* Om värdet är tomt används **[!UICONTROL Public]** som standard för mappen.

Mer information finns i filen [module_version_csv spec](assets/4-module_version.xlsx).

### Ändringar i modulmigrering - slutförandekriterier

Administratörer kan ange slutförandekriterier för modulerna under modulmigreringen. I den här versionen har vi lagt till nya kolumner `completionCriteria`, `viewPercent` och `quizData` i [module_version.csv](assets/module_version.csv).

Följande villkor gäller för de nya kolumnerna:

1. `completionCriteria`:

   * Datatypen ska vara ett strängvärde och de värden som stöds är:
      * `LAUNCH_CONTENT`
      * `VIEW_PERCENT`
      * `QUIZ`
      * `MARK_COMPLETE`
   * Lägg bara till slutförandekriterier på modulnivå för modultyper i eget tempo.
   * De värden som stöds för statiskt innehåll är `LAUNCH_CONTENT` och `VIEW_PERCENT`.
   * De värden som stöds för interaktivt innehåll är `LAUNCH_CONTENT`, `VIEW_PERCENT` och `QUIZ`.
   * De värden som stöds för HTML5-innehåll är `LAUNCH_CONTENT` och `MARK_COMPLETE`.

2. `viewPercent`:

   * Datatypen för kolumnen ska vara ett heltal och värdet måste vara mellan 0 och 100.
   * När completionCriteria är inställt på `VIEW_PERCENT` anger du önskad visningsprocent i den här kolumnen eller lämnar den tom.

3. `quizData`:

   * Datatypen ska vara ett strängvärde och de värden som stöds är `QUIZ_ATTEMPTED`, `QUIZ_PASSED` och `QUIZPASSED_OR_LIMITREACHED`.
   * När `completionCriteria` är inställt på `QUIZ` anger du rätt frågeformulärsvärde i kolumnen `quizData`.

Mer information finns i filen [module_version_csv spec](assets/4-module_version.xlsx).

### Ändringar i kursmigrering - kriterier för slutförande

Administratörer kan specificera slutförandekriterierna för kurserna under kursmigreringen. I den här versionen har vi lagt till en ny kolumn med namnet `completionCriteria` i [course.csv](assets/course.csv).

Följande villkor gäller för kolumnen `completionCriteria`:

* Datatypen ska vara antingen sträng eller siffra, och det är ett valfritt fält.
* Värdena ska vara `ALL`, `X` och `SELECTEDMODULES`.
* X är ett heltalsvärde som ska vara större än 0 och mindre än det totala antalet moduler.
* Om du ställer in `completionCriteria` på `SELECTEDMODULES` måste du markera de obligatoriska modulerna i filen [course_module.csv](assets/course_module.csv).
* Ange `TRUE` eller `FALSE` i kolumnen `optionalCriteria`. Om du anger värdet `TRUE` blir modulen obligatorisk.

Mer information finns i [CSV-specifikation för kurs](assets/3-course.xlsx) och filen [CSV-specifikation för kurs_modul](assets/6-course_module.xlsx).

## API-ändringar

Detta är API-ändringarna:

* **API för sökning**:
   * Nytt lägesfilter med alternativ: classicSearch och advanceSearch.
   * Nytt loMetadata-alternativ för snippTypes.
* **Meddelande-API**:
   * Innehåller altText-attribut för masthead-beskrivningar.
* **Instans-API:er**:
   * Nytt språkattribut för att hämta språkinformation.
* **SVORDOMSKONTROLL**:
   * Uppdaterade API:er för att söka efter förbjudna ord i kommentarer och svar på sociala inlägg:
* **RPM- och bränningsbegränsning**:
   * Lade till RPM (förfrågningar per minut) och brusgränser för alla API:er.
* **API:er för utmärkelsetecken**:
   * Nytt attribut för externalProvider för att hämta information om externa utmärkelsetecken.
* **Jobb-API**:
   * Hämta användargruppsrapport och granskningsrapport för anpassade roller med hjälp av jobb-API:et.

### Ändringar i API för sökning

API:t för sökning har nu ett nytt lägesfilter med två alternativ: `classicSearch` och `advanceSearch`. Det finns också ett nytt `loMetadata`-alternativ för `snippetTypes`. Du får bäst resultat om du inkluderar `loMetadata` i `snippetTypes` när du använder läget `advanceSearch`.

### Ändringar i meddelande-API

`GET /announcements API` innehåller nu attributet `altText` för att ange masthead-beskrivningen.

#### Exempelbegäran med cURL:

```
curl -X GET --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 12345678' 'https://abcd.adobe.com/primeapi/v2/announcements/123456'
```

#### Exempelsvar:

```
{
  "links": {
    "self": "https://abcd.adobe.com/primeapi/v2/announcements/123456"
  },
  "data": {
    "id": "12345",
    "type": "adminAnnouncement",
    "attributes": {
      "actionUrl": "google.com",
      "announcementType": "MASTHEAD",
      "expiryDate": "2038-01-19T03:14:07.000Z",
      "liveDate": "2024-07-31T11:11:30.000Z",
      "contentMetaData": [
        {
          "contentType": "IMAGE",
          "contentUrl": "https://abcd.adobe.com",
          "locale": "en-US",
          "altText": "Moonlight - english changed new",
          "thumbnailUrl": "https://abcd.adobe.com/"
        },      ]
    }
  }
}
```

### Ändringar i instans-API:er

Det nya `locale`-attributet har lagts till i följande API:er för att hämta språkinformation.

* `GET /learningObjects/{loId}/instances/{loInstanceId}`
* `GET /learningObjects/{id}?include=instances,enrollment.loInstance`
* `GET /learningObjects?include=instances,enrollment.loInstance`
* `GET /learningObjects/{id}/relatedLOs?include=instances,enrollment.loInstance`
* `POST /learningObjects/query?include=instances,enrollment.loInstance`
* `POST /search/query?include=model.instances`
* `GET /search?include=model.instances`

#### Exempelbegäran med cURL:

```
curl --location 'http://abcd.com/primeapi/v2/learningObjects/course:1234567/instances/course:1234567_1234567' \
```

#### Exempelbegäran:

```
{
    "links": {
        "self": "http://abcd.com/primeapi/v2/learningObjects/course:1234567/instances/course:1234567_1234567"
    },
    "data": {
        "id": "course:1234567_1234567",
        "type": "learningObjectInstance",
        "attributes": {
            "dateCreated": "2024-02-27T09:21:25.000Z",
            "isAET": false,
            "isDefault": true,
            "isFlexible": false,
            "locale": "en-US",
            "state": "Active",
            "localizedMetadata": [
                {
                    "locale": "en-US",
                    "name": "Default instance"
                }
            ]
        },
        "relationships": {
            "learningObject": {
                "data": {
                    "id": "course:1234567",
                    "type": "learningObject"
                }
            },
            "loResources": {
                "data": [
                    {
                        "id": "course:123456_1234567_1234567_1",
                        "type": "learningObjectResource"
                    }
                ]
            }
        }
    }
}
```

### Offentliga API-ändringar för svordomskontroll

Följande API:er har uppdaterats för att utföra profanity-kontroller för kommentarer och svar på sociala inlägg.

* `POST /boards/{id}/posts `
* `PATCH /posts/{id}`
* `POST /posts/{id}/comments`
* `PATCH /comments/{id}`
* `POST /comments/{id}/replies`
* `PATCH /replies/{id}`

Om ett begränsat ord hittas i inlägget skickas följande svar.

#### Exempelsvar:

```
{
  "status": "FORBIDDEN",
  "title": "BAD_WORD_FOUND",
  "source": {
    "info": "Unacceptable word found in post"
  }
}
```

### Förändringar i varv/min- och sprängningsbegränsning

I den här versionen har RPM (Begäranden per minut) och burst-gränser lagts till för alla API:er. Den maximala RPM för varje API kan kontrolleras på Swagger-sidan.

RPM är antalet begäranden som du kan skicka till API-servern på en minut. Burst-gränsen tillåter ett högre antal förfrågningar under en kort tid, vilket går utöver den vanliga hastighetsgränsen. API:t `learningObject` tillåter till exempel högst 15 förfrågningar per minut. Om den här gränsen överskrids returnerar API ett felmeddelande.

### Ändringar i API:er för märken

Det nya attributet `externalProvider` har lagts till i följande API:er för att hämta information om externa märken, inklusive badge ID och providernamn.

* `GET /badges `
* `GET /badges/{id}`
* `GET /skills?include=levels.badge`
* `GET /skills/{id}?include=levels.badge`
* `GET /learningObjects/{loId}/instances/{loInstanceId}?include=badge`
* `GET /users/{userId}/userBadges`
* `GET /users/{userId}/userBadges/{id}`

#### Exempelbegäran med cURL:

```
curl -X GET --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 123456789' 'https://abcd.adobe.com/primeapi/v2/badges/44'
```

#### Exempelsvar:

```
{
  "links": {
    "self": "https://abcd.adobe.com/primeapi/v2/badges/44"
  },
  "data": {
    "id": "44",
    "type": "badge",
    "attributes": {
      "imageUrl": "https://abcd.com/accountassets/1/badges/download.png",
      "name": "external badge",
      "state": "Active",
      "externalProvider": {
        "id": "1234sjd-b272-4de1-9b60-1234567",
        "provider": "credly"
      }
    }
  }
}
```

### Hämta granskningsrapporter för användargrupper och anpassade roller via jobb-API

Användaren kan hämta **[!UICONTROL User Group Report]** och **[!UICONTROL Custom Role Audit Report]** med hjälp av `Job API`.

#### Exempelbegäran för hämtning av användargruppsrapport:

```
curl -X POST --header 'Content-Type: application/vnd.api+json;charset=UTF-8' --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 12345678' -d '{ \ 
     "data": { \ 
         "type": "job", \ 
         "attributes": { \ 
             "jobType": "generateUserGroupReport" \ 
         } \ 
    } \ 
 }' 'https://abcd.adobe.com/primeapi/v2/jobs'
```

#### Exempelbegäran för hämtning av granskningsrapport för anpassade roller:

```
curl -X POST --header 'Content-Type: application/vnd.api+json;charset=UTF-8' --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 1234567' -d '{
    "data": {
        "type": "job",
        "attributes": {
            "description": "description of your choice",
            "jobType": "generateCustomRoleAuditReport",
            "payload":{
                 "fromDate": "2020-01-01T18:30:00.000Z",
                 "toDate": "2024-09-31T18:30:00.000Z",
                 "locale":  "en-US"
            }
        }
   }
}
```

### Felmeddelande för brödtext för ingen begäran

Vi har infört specifika felmeddelanden för fall där begärandetexten är obligatorisk men inte har angetts i API:et.

#### Exempel på felmeddelande:

```
{
    "status": "BAD_REQUEST",
    "title": "Generic Error"
}
```

## Förbättrade rapporter

Administratörer hittar dessa rapporteringsändringar i avsnittet **Admin** > **Rapporter**.

### Rapport med utbildningsbetygsutdrag

Rapporten **[!UICONTROL Learning Transcripts]** kommer att innehålla två nya kolumner:

* **[!UICONTROL Module ID]**: Visar den unika identifieraren för varje modul. Den nya kolumnen har lagts till efter den befintliga **[!UICONTROL Module]**-kolumnen.
* **[!UICONTROL Course Instance ID]**: Visar den unika identifieraren för varje kursinstans. Den nya kolumnen har lagts till efter den befintliga **[!UICONTROL Instance]**-kolumnen.
* **[!UICONTROL Completion Comment]**: Den här kolumnen innehåller de kommentarer som administratören har angett när slutförandet av användaren markeras. Den nya kolumnen har lagts till i slutet av rapporten.


### Sammanfattningsrapport för session

Rapporten **[!UICONTROL Session Summary]** kommer att innehålla tre nya kolumner:

* Kolumnen **[!UICONTROL Module ID]** har lagts till före kolumnen **[!UICONTROL Session Name]**.
* Kolumnen **[!UICONTROL Session ID]** har lagts till före kolumnen **[!UICONTROL Session Name]**.
* Kolumnen **[!UICONTROL Course Instance ID]** har lagts till efter kolumnen **[!UICONTROL Instance Name]**.
* Kolumnen **[!UICONTROL Completion Count]** har lagts till efter kolumnen **[!UICONTROL Enrollment Count]**.

## Fel som är åtgärdade i den här uppdateringen

* Korrigerade felet som inträffade vid överföring av videoklipp från aktivitetsmodulen vid filöverföring på Android- och iOS-enheter.
* Korrigerade problemet med att öppna kurser i mobilappen; webbversionen fungerar korrekt.
* Korrigerade problemet med visning av arbetsstöd och andra resurser i Safari.
* Korrigerade problemet som hindrade användare från att hämta arbetsstöd i mobilappen.
* Korrigerade felet i dokumentationen för API:et för korrigeringsanvändaren.
* Korrigerade problemet där organisatörer inte fick e-postmeddelanden när en session togs bort från kursen.
* Korrigerade problemet där organisatörer inte får e-postmeddelanden om annullering av session när en modul tas bort från kursen och publiceras igen.
* Lade till stöd för att inkludera specialtecknen &quot;+&quot; och &quot;-&quot; i e-postadresser när externa användare skapas.
* Korrigerade problemet där synkronisering av enhetliga rapporter i Marketo-kopplingen misslyckas om rapporten om användarkompetens innehåller dubbla citattecken i CSV-postvärdet
* Korrigerade problemet där slutpunkten `/skills` returnerar rätt tillstånd för Admin API, men elevens API visar konsekvent felaktiga eller cachelagrade data.
* Korrigerade problemet med att Go1-introduktion för gratiskurser misslyckades när kontot inte har Go1-anslutningen konfigurerad.
* Korrigerade problemet där kurser i utbildningsvägen (LP) inte är tillgängliga via migrering om eleven redan har slutfört LP.
* Korrigerade problemet där CSV-filen för inkrementella användare misslyckas när både användarens chef och hanterare på överhoppningsnivå anges som SU (superanvändare) i stället för admin och inte ingår i CSV-filen.
* Korrigerade omfångsproblemen för butikschefer i kontrollpanelrapporter.
* Korrigerade problemet där xapi_iri inte togs bort när en utkastkurs togs bort.
* Korrigerade problemet som förhindrade att ett unikt LO-ID lades till i vissa scenarier.
* Korrigerade problemet där egenskapen IsEmbeddable i utbildningsplanen inte uppdaterades korrekt i delade utbildningsplaner.
* Problemet med att visa utbildningsvägar under den totala tiden i vyn Elev har korrigerats.
* Problemet med att elever kan registrera sig eller registrera sig via självregistreringslänkar även efter att deras konton har tagits bort har korrigerats.
* Korrigerade problemet där `www` togs bort när länkar lades till i kursbeskrivningen när kursen skapades.
* Korrigerade ett problem där jobbstöd för att dölja information och hämta inte fungerade korrekt.
* Korrigerade ett problem där enkel inloggning (SSO) inte fungerade för nya användare som lagts till via självregistreringslänken med ett IP-ID.
* Ett problem har korrigerats där meddelandedata inte hämtades efter att ett meddelande togs bort.
* Korrigerade problemet med otillräckliga sökresultat när du sökte efter användare via e-post.

## Systemkrav

Visa [Systemkrav för Adobe Learning Manager](/help/migrated/system-requirements.md).

## Tidigare utgåvor av Adobe Learning Manager

* [Juli 2024-utgåvan](/help/migrated/whats-new-july-2024.md)
* [Marsversionen 2024](/help/migrated/whats-new-march-2024.md)
