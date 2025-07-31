---
jcr-language: en_us
title: Användarhandbok för webhookar
description: Läs mer om användning av webhookar, bästa praxis och begränsningar
contentowner: chandrum
exl-id: e6a63ffb-7fdd-46e4-b5e6-20ce36861cef
source-git-commit: 4c04757d78d599ca30e3cd26257a967d5b9e3fdc
workflow-type: tm+mt
source-wordcount: '3360'
ht-degree: 1%

---

# Användarhandbok för webhookar

Webhookar är ett sätt för webbprogram att kommunicera med varandra automatiskt och i realtid.

Till skillnad från traditionella API:er, som väntar på att en användare ska begära information, delar API:er i realtid data så fort det sker. Webhooks fungerar som ett API i realtid och hjälper till att dela data omedelbart när den angivna händelsen inträffar.

## Enheter

För att förstå webhooks-händelser måste vi först vara medvetna om vilka entiteter som är inblandade och vilka utlösande villkor som gäller för dessa händelser.

### Utbildningsobjekt

Följande händelser stöds för utbildningsobjekt (kurs, utbildningsväg eller certifieringar).

#### Utkast

När ett utbildningsobjekt skapas från användargränssnittet startar det i läget **Utkast**. Det innebär att utbildningsobjektet ännu inte har publicerats och inte är tillgängligt för eleverna. Händelsen **LEARNING_OBJECT_DRAFT** aktiveras så länge utbildningsobjektet förblir ett utkast. Alla successiva uppdateringar av utkastet kommer också att utlösa denna händelse.

#### Uppdatera

När utbildningsobjektet har publicerats ändras dess tillstånd från **Utkast** till **Publicerat**. Under den här övergången genererar Webhook händelsen **LEARNING_OBJECT_MODIFICATION** eftersom utbildningsobjektet ändras från **Utkast** till **Publicerat**. Alla efterföljande ändringar och uppdateringar av LO kommer också att utlösa en **LEARNING_OBJECT_MODIFICATION**-händelse.

Händelsen **LEARNING_OBJECT_MODIFICATION** aktiveras också när utbildningsobjektet tas ur bruk. Med den här indragna åtgärden markeras de underliggande instanserna som uppdaterade eftersom dessa instanser utfasas när det överordnade utbildningsobjektet är i inaktuellt läge.

#### Ta bort

När du tar bort ett utbildningsobjekt genereras händelsen **LEARNING_OBJECT_DELETION**. Den här händelsen indikerar att utbildningsobjektet har raderats och att det inte längre är tillgängligt för elever.

Förutom realtidshändelser har utbildningsobjekthändelser även en batchmotsvarighet (icke-realtidshändelse), som utlöses som en del av händelsen **LEARNING_OBJECT_MODIFICATION_BATCH**. Den här händelsen inträffar när ett utbildningsobjekt skapas eller ändras via migreringsarbetsflödet. Eftersom åtgärder för att skapa och ta bort utbildningsobjekt inte stöds via migrering finns det inga motsvarande utkast- eller borttagningshändelser för dessa åtgärder.

### Instanser av utbildningsobjekt

Nedan visas de händelser som stöds för instanser av utbildningsobjekt.

#### Uppdatera

När en instans har skapats genereras händelsen **LEARNING_OBJECT_INSTANCE_MODIFICATION**. Utbildningsobjektinstanser i Adobe Learning Manager har inte statusen **Utkast**. Därför stöder inte Adobe Learning Manager en **LEARNING_OBJECT_INSTANCE_DRAFT-händelse**. Den här händelsen genereras när en instans skapas, ändras eller dras tillbaka.

Förutom att den här händelsen genereras när en instans skapas, uppdateras eller fasas ut, genereras den också automatiskt när dess överordnade utbildningsobjekt markeras som **utfasat**. Det beror på att när ett utbildningsobjekt dras tillbaka måste även de underliggande instanserna markeras som **utfasade**.

#### Ta bort

När en instans tas bort genereras händelsen **LEARNING_OBJECT_INSTANCE_DELETION**. Den här händelsen gäller endast kursinstanser som innehåller moduler i eget tempo, eftersom Adobe Learning Manager endast tillåter administratörer att ta bort kursinstanser där modultypen sker i egen takt. Adobe Learning Manager stöder inte explicita borttagningar för andra typer av kursmoduler, inte för instanser av utbildningsvägar eller certifieringsinstanser.

Instansen av utbildningsobjektet har också en motsvarighet som inte finns i realtid, som visas som en del av händelsen **LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH**. Den här händelsen utlöses när en instans av ett utbildningsobjekt skapas eller ändras via migreringsarbetsflödet. Eftersom utkast- och borttagningsåtgärder för utbildningsobjektinstanser inte stöds i migreringen är motsvarande utkast- och borttagningshändelser inte tillgängliga.

### Registrering

När en elev utför en registreringsåtgärd utlöses en realtidsregistreringshändelse. Beroende på typ av utbildningsobjekt kan registreringshändelsen i realtid ingå i en av följande kategorier:

* COURSE_ENROLLMENT
* LEARNING_PATH_ENROLLMENT
* CERTIFICATION_ENROLLMENT

Registreringshändelser har batchmotsvarigheter utöver dessa realtidshändelser. När en registrering utlöses av en administratör, chef eller plattform utlöses icke-realtidshändelser för registrering. Baserat på utbildningsobjekttypen kan batchregistreringshändelsen vara något av följande:

* COURSE_ENROLLMENT_BATCH
* LEARNING_PATH_ENROLLMENT_BATCH
* CERTIFICATION_ENROLLMENT_BATCH

### Avregistrering

När en elev utför en avregistreringsåtgärd utlöses en avregistreringshändelse i realtid. Beroende på typ av utbildningsobjekt kan avregistreringshändelsen i realtid ingå i en av följande kategorier:

* COURSE_UNENROLLMENT
* LEARNING_PATH_UNENROLLMENT
* CERTIFICATION_UNENROLLMENT

Förutom dessa händelser finns det även satsvis avregistreringshändelser. När en avregistrering markeras av en administratör, chef eller plattform utlöses avregistreringshändelser som inte rör realtid. Baserat på utbildningsobjekttypen kan batchavregistreringshändelsen vara något av följande:

* COURSE_UNENROLLMENT_BATCH
* LEARNING_PATH_UNENROLLMENT_BATCH
* CERTIFICATION_UNENROLLMENT_BATCH

### Slutförande

Händelsen för slutförande i realtid utlöses när en elev slutför ett utbildningsobjekt. Beroende på typen av utbildningsobjekt kan händelsen slutförande i realtid ingå i en av följande kategorier:

* COURSE_COMPLETED
* LEARNING_PATH_COMPLETED
* CERTIFICATION_COMPLETED

Förutom dessa realtidshändelser finns det även satsvis slutförandehändelser. När en administratör, chef eller plattform till exempel markerar ett utbildningsobjekt som slutfört utlöses händelser som inte rör slutförande i realtid. Beroende på typ av utbildningsobjekt kan batchslutförandehändelsen ingå i en av följande kategorier:

* COURSE_COMPLETED_BATCH
* LEARNING_PATH_COMPLETED_BATCH
* CERTIFICATION_COMPLETED_BATCH

### Elevframsteg

När en elev registrerar sig för ett utbildningsobjekt och påbörjar modulen spåras elevens framsteg. Dessa data ingår i **LEARNER_PROGRESS**-händelsen. Händelsen kan fördröjas med upp till 15 minuter, eftersom framstegsspårningen är beroende av komplex aggregeringslogik, som inte är realtid.

### CI-status

Realtidshändelsen **CI_STATS** utlöses när platsen eller väntelistan ändras för en kursinstans. Dessa data hämtas endast på instansnivå. Dessutom utlöses denna händelse för kurser och inte för andra utbildningsvägar eller certifieringar, eftersom platstillgång och väntelista är attribut som är specifika för en kurs och dess instans.

## Ordning på evenemang

Adobe Learning Manager ser till att händelser ordnas för varje konto. Det kan dock finnas skillnader när meddelanden korreleras mellan registrerings- eller slutförandehändelser och händelser som rör framsteg. Detta beror på att elevframstegshändelsen kan fördröjas med upp till 15 minuter, eftersom framstegsspårning bygger på komplex aggregeringslogik, vilket inte är realtid. Dessutom kommer förloppshändelser från olika datakällor, så deras ordning kan inte garanteras i förhållande till registrerings- och slutförandehändelser. Därför tillhandahåller Adobe Learning Manager bästa praxis för klienter när de lyssnar på dessa händelser.

Om slutförandehändelsen inträffar före elevens förloppshändelse kan klienten ignorera elevens förloppshändelse. Detta beror på att elevframstegshändelsen kan fördröjas med upp till 15 minuter, medan slutförandehändelsen kan utlösas innan framstegshändelsen tas emot. Eftersom erhållande av en slutförandehändelse indikerar att utbildningsobjektet är slutfört, innebär det att förloppet har nått 100 %.

I det sällsynta fall då registreringshändelsen kommer efter elevens framgångshändelse kan klienten ignorera registreringshändelsen. Detta beror på att framsteg endast kan spåras efter att eleven har registrerat sig för utbildningsobjektet. Att du får en progress-händelse indikerar att utbildningsobjektet har startats, vilket endast sker efter en lyckad registrering.

## Realtidshändelser jämfört med grupperade händelser

Vissa händelser har motsvarigheter i realtid och icke-realtid, som nämns ovan. Det kan finnas frågor om när du ska prenumerera på realtidshändelser och när du ska prenumerera på händelser som inte sker i realtid. Nedan följer riktlinjer som kan följas utifrån de enheter som beskrivs ovan.

### Händelser i realtid

| S.No | Webhook-händelser | Beskrivning |
|---|---|---|
| 1 | CI_STATS | Utlöses när det sker ett byte av plats eller väntelista för en kursinstans. |
| 2 | COURSE_ENROLLMENT | Utlöses när en elev registrerar sig för en kurs. |
| 3 | COURSE_COMPLETED | Utlöses när en elev slutför en kurs. |
| 4 | LEARNING_PATH_ENROLLMENT | Utlöses när en elev registrerar sig för en utbildningsväg. |
| 5 | LEARNING_PATH_COMPLETED | Utlöses när en elev slutför en utbildningsväg. |
| 6 | CERTIFICATION_ENROLLMENT | Utlöses när en elev registrerar sig för en certifiering. |
| 7 | CERTIFICATION_COMPLETED | Utlöses när en elev slutför en certifiering. |
| 8 | COURSE_UNENROLLMENT | Utlöses när en elev avregistrerar sig från en kurs. |
| 9 | LEARNING_PATH_UNENROLLMENT | Utlöses när en elev avregistrerar sig från en utbildningsväg. |
| 10 | CERTIFICATION_UNENROLLMENT | Utlöses när en elev avregistrerar sig från en certifiering. |
| 11 | LEARNING_OBJECT_DRAFT | Utlöses när ett utbildningsobjekt skapas i utkastläge. |
| 12 | LEARNING_OBJECT_DELETION | Utlöses under borttagningen av ett utbildningsobjekt. |
| 13 | LEARNING_OBJECT_MODIFICATION | Utlöses under modifieringen av ett utbildningsobjekt. |
| 14 | LEARNING_OBJECT_INSTANCE_MODIFICATION | Utlöses när en instans för utbildningsobjekt skapas eller ändras.<div><b>Obs!</b> Vi rekommenderar att du bara använder kursinstanser efter att kursen har publicerats.</div> |
| 15 | LEARNING_OBJECT_INSTANCE_DELETION | Utlöses under borttagningen av en instans av utbildningsobjekt. |

### Händelser som inte sker i realtid

| S.No | Webhook-händelser | Beskrivning |
|---|---|---|
| 1 | COURSE_ENROLLMENT_BATCH | Utlöses när en administratör/chef/plattform registrerar elever för en kurs. |
| 2 | COURSE_COMPLETED_BATCH | Utlöses när en administratör/chef/plattform markerar en kurs som slutförd. |
| 3 | LEARNING_PATH_ENROLLMENT_BATCH | Utlöses när en administratör/chef/plattform registrerar elever på en utbildningsväg. |
| 4 | LEARNING_PATH_COMPLETED_BATCH | Utlöses när en administratör/chef markerar en utbildningsväg som slutförd. |
| 5 | CERTIFICATION_ENROLLMENT_BATCH | Utlöses när en administratör/chef/plattform registrerar elever i en certifiering. |
| 6 | CERTIFICATION_COMPLETED_BATCH | Utlöses när en administratör/chef/plattform markerar en certifiering som slutförd. |
| 7 | LEARNER_PROGRESS | Spårar förloppet för en elev när en modul har slutförts. |
| 8 | COURSE_UNENROLLMENT_BATCH | Utlöses när en administratör/chef/plattform avregistrerar elever från en kurs. |
| 9 | LEARNING_PATH_UNENROLLMENT_BATCH | Utlöses när en administratör/chef/plattform avregistrerar elever från en utbildningsväg. |
| 10 | CERTIFICATION_UNENROLLMENT_BATCH | Utlöses när en administratör/chef/plattform avregistrerar elever från en certifiering. |
| 11 | LEARNING_OBJECT_MODIFICATION_BATCH | Utlöses under ändringen av ett utbildningsobjekt via migreringsarbetsflöde. |
| 12 | LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH | Utlöses när en instans av ett utbildningsobjekt skapas eller ändras via migreringsarbetsflöde. |

### Utbildningsobjekt och dess instanser

* Prenumerera på realtidshändelser när du vill lyssna efter ändringar av utbildningsobjekt som har gjorts med gränssnittsåtgärder av roller som Administratör, Författare osv.
* Prenumerera på händelser som inte sker i realtid eller gruppvis när du vill lyssna efter ändringar av utbildningsobjekt som har gjorts via arbetsflöden för migrering.

### Registrering, avregistrering och slutförande

* Prenumerera på realtidshändelser när du vill lyssna på registreringar, avregistreringar eller slutföranden som utförs av elever.
* Prenumerera på händelser som inte sker i realtid eller gruppvis när du vill lyssna på registreringar, avregistreringar eller slutföranden som markerats av admin, chef, plattform osv.

### Elevframsteg

* Prenumerera på händelsen när du vill lyssna efter en elevs statusändringar.

>[!NOTE]
>
>I ovanstående scenarier (registrering, avregistrering, slutförande och förlopp) kan attributsammansättningar som består av userId och loInstanceId unikt identifiera en post.

### Kursinstansstatistik

* Prenumerera på **CI_STATS**-realtidshändelsen när du vill lyssna efter ändringar av tillgängligheten för platser eller väntelistor.

## Nyttolast för webhook-händelse

Som en del av webhooks-svarets nyttolast genererar Adobe Learning Manager attribut som krävs för att unikt identifiera en entitet. Dessa kommer att sändas ut i samma format och enligt de standarder som används av det offentliga API:t, vilket säkerställer att webhook-data är synkroniserade med de offentliga API-data. Visa [Exempel på nyttolaster](/help/migrated/integration-admin/feature-summary/webhooks-usage-guide.md#sample-payloads-for-the-events) för att se nyttolaster för de olika händelserna.

## Använda webhookar för att skapa en extern databas eller meddelandetjänst

Ett av de användningsfall vi har hört där webhookar kan vara användbara är för att bygga en databas på kundens sida. Adobe Learning Manager har sin egen databas och sitt eget schema, men kunder har inte tillgång till det.

Frågan är: hur kan kunder bygga en databas med hjälp av händelser från webhooks?

Eftersom Adobe Learning Manager inte direkt exponerar tabellposterna och schemat kan man förlita sig på Webhooks-lösningen för att skapa en extern databas genom att använda händelserna för att fylla i den. I den här versionen tillhandahåller vi händelser för utbildningsobjekt, instanser av utbildningsobjekt, registrering, avregistrering, slutförande, framsteg och kursinstansstatistik.

### Bygga en databas från utbildningsobjekthändelser

Utbildningsobjektets händelser visar `loId` och `loType` för att identifiera en entitet. Dessa attribut räcker dock inte för att skapa en extern databas för utbildningsobjekt. Kunder kommer att behöva ytterligare fält för att ytterligare beskriva utbildningsobjektet.
Det finns två sätt att hämta ytterligare data:

#### Generera en utbildningsdatarapport för att hämta alla data

Den här metoden bör användas när utbildningsobjekt skapas i grupp via arbetsflöden som migrering. Målet här är att generera rapporten **[!UICONTROL Training Data]** med alla utbildningsobjekt hämtade som en del av migreringsarbetsflödet. För att optimera importprocessen bör du ställa in exportens starttid på den tid då migreringen utlöstes. Detta säkerställer att endast utbildningsobjekt som införs via migrering exporteras i rapporten, eftersom historiska data redan kommer att finnas tillgängliga i kundens databas.

#### Fråga efter information från det offentliga API-GETEN /learningObjects - Admin-omfånget

Den här metoden bör användas när utbildningsobjekt skapas via arbetsflöden i realtid. Kunden bör ha ett eget cachelagringslager för att grupplagra utbildningsobjekten som skickas via händelserna och sedan fråga API:t `GET /learningObjects` genom att skicka dessa ID:n för utbildningsobjekt. Anledningen till att ha ett cachelagringslager är att se till att de offentliga API-hastighetsgränserna inte överskrids. För närvarande har vi administratörsgränser inställda på 500 förfrågningar per timme för ` GET /learningObject` API:er. Om den här gränsen överskrids kommer den offentliga API-tjänsten att svara med ett **HTTP 429-meddelande om för många förfrågningar**.

### Bygga databas från instans av utbildningsobjekt och CI_STATS-händelser

Instanshändelsen för utbildningsobjekt genererar attributen `loInstanceId`, `loId` och `loType` för kurser och utbildningsvägar. På samma sätt gäller **CI_STATS**-händelsen endast kurser eftersom `seatLimit`, `seatAvailability`, `waitListLimit`, `waitlistAvailability` osv., endast gäller kurser.

I vissa användningsfall krävs ytterligare instansdata, som instansnamn, tillstånd osv. Om du vill hämta ytterligare instansdata ska följande metod användas:

#### Fråga efter information från public-api-GET /learningobjects - administratörsomfattning

Kunder kan använda API:et `GET /learningObjects` som nämns ovan, tillsammans med instanser som ingår för att hämta information om instanser. De bör fortfarande följa metoden som nämns i [avsnittet](/help/migrated/integration-admin/feature-summary/webhooks-usage-guide.md#query-the-information-from-the-public-api-get-learningobjects-admin-scope) för att säkerställa att hastighetsgränserna inte överskrids.


>[!NOTE]
>
>1. Certifieringar har inte förekomstkonceptet i ALM.
>2. Det finns inget behov av att hämta ytterligare data för CI_STATS eftersom samma information redan skulle ha hämtats som en del av utbildningsobjektets instanshändelser.

### Bygger databas från händelser för registrering, avregistrering, slutförande och förlopp

Elevregistrering, avregistrering, slutförande och förlopp skickas som separata händelser i Adobe Learning Manager. Eleven identifieras av attributet `userId`. Det kan dock finnas vissa scenarier där ytterligare elevinformation, som namn, e-post osv., krävs för underordnade arbetsflöden på kundsidan. För att hämta dessa data kan kunderna följa den metod som beskrivs nedan:

#### Exportera användarrapporten från administratören eller kopplingar

Denna metod bör användas när massarbetsflöden är inblandade, t.ex. vid massregistrering eller avregistrering av massdata. Användarrapporten från Adobe Learning Manager innehåller all användarinformation. Genom att korrelera `userId` som erhölls från webhook-händelsen kan kunder slå upp den här rapporten (som kan visas på kundsidan som en databas, cache eller API-slutpunkt) för att hämta ytterligare information som Namn, E-post, UUID osv. Den här metoden kan användas för att synka användare varje vecka eller dag.

#### Frågeinformation från offentlig API-GET/användare - administratörsomfattning

Den här metoden kan användas när användarna inte är tillgängliga i rapporten ovan. Kombinationen av 1 och 2 gör att alla befintliga användare som skapats tidigare kan omfattas av **[!UICONTROL User Report]**, medan nyskapade användare fortfarande kan hämtas från API:et. Om **[!UICONTROL User Report]** saknar data kan kunden skicka användar-ID:n som indataargument till API:t `GET /users` för att hämta användarinformation. Denna information bör cachelagras på kundsidan för att förhindra upprepade anrop av det offentliga API:t för samma uppsättning användare. Observera att vi för närvarande har hastighetsgränser för administratörer inställda på 500 förfrågningar per timme för API:er för GET/användare. Alla förfrågningar som överskrider den här gränsen resulterar i svaret **HTTP 429 för många förfrågningar**.

## Feltolerans

Feltoleransen för ALM-webhooksystemet ger rekommendationer för prenumeranter som hanterar potentiella problem, t.ex. händelseförlust, dubbletthändelser och leverans utanför beställning.

ALM har en anslutningstidsgräns på 10 sekunder och en sockettimeout på 5 sekunder. Förväntningarna är att kunden bekräftar meddelandet så snart det tar emot dem. Detta är för att säkerställa att klienten inte fördröjs under bearbetning av meddelanden. Om det finns någon nedströmsbearbetning som är tidskrävande, klienten bör ändå bekräfta händelsen omedelbart och sedan hantera nedströmsbearbetningen i sin ände.

### Datalagring

Evenemangen sparas i 7 dagar. Om de inte bearbetas inom den här tiden går de förlorade för alltid. Om återställning sker den sista dagen och det behövs mer tid förlängs inte kvarhållningsperioden.
Om händelser produceras snabbare än de konsumeras kan vissa händelser gå förlorade. Även om detta är ovanligt, abonnenter bör övervaka för att förhindra att det blir en långsiktig fråga.

### Inaktivera webhookar

När en prenumerant inte svarar på webhook-händelser gör ALM-systemet ett nytt försök att använda webhookar med exponentiell backoff för att undvika att överväldiga prenumeranten.

Återförsöksprocessen startar med ett inledande intervall på 5 sekunder. Om prenumeranten inte svarar fördubblas väntetiden till 10, 20, 40 och 80 sekunder, och ökar så småningom till maximalt 5 minuter. När det når 5 minuter fortsätter systemet att försöka igen var femte minut tills kvarhållningsperioden på 7 dagar är slut. Om prenumeranten fortfarande inte svarar under hela den här perioden inaktiveras webhooken automatiskt. En påminnelse kommer att skickas till prenumeranten med jämna mellanrum.

### Duplicera händelser

Om det tar mer än fem sekunder för en prenumerant att svara efter att en händelse har bearbetats, kan systemet försöka behandla samma händelse igen. Vi rekommenderar att du använder händelse-ID:n för att hålla reda på vilka händelser som redan har bearbetats. Och om en webhook kraschar efter att händelsen har skickats men innan du sparar att den har bearbetats, kan samma händelsegrupp försöka igen. Vi rekommenderar att du använder batch-ID:n eller enskilda händelse-ID:n för att känna igen och ignorera eventuella dubbletter.

### Rekommendation för feltolerans

För att förhindra dessa fel bör prenumeranter aktivt övervaka webhook-händelser och ställa in varningar för problem som missade händelser, dubbla leveranser eller oordnade sekvenser.

## Specifika riktlinjer för webhook-händelser

1. Om du får en LEARNER_PROGRESS -händelse först ska du ignorera händelserna nedan:

   * COURSE_ENROLLMENT
   * COURSE_ENROLLMENT_BATCH
   * LEARNING_PATH_ENROLLMENT
   * LEARNING_PATH_ENROLLMENT_BATCH
   * CERTIFICATION_ENROLLMENT
   * CERTIFICATION_ENROLLMENT_BATCH

2. Ignorera händelsen LEARNER_PROGRESS om den inträffar efter följande händelser:

   * COURSE_COMPLETED
   * COURSE_COMPLETED_BATCH
   * LEARNING_PATH_COMPLETED
   * LEARNING_PATH_COMPLETED_BATCH
   * CERTIFICATION_COMPLETED
   * CERTIFICATION_COMPLETED_BATCH

3. Använd fältet tidsstämpel för att ange om händelsen ska ignoreras eller bearbetas, förutom för händelsen LEARNER_PROGRESS.

## Bra metoder för konsumtion av webhookar

* Webhook-lösningen används för att hantera system med hög genomströmning där hastighet och låg latens är viktiga. Kunden bör därför se till att händelsen bekräftas så snart den har tagits emot. Även om ytterligare bearbetning behövs på kundens sida (t.ex. hämtning av data från rapporter, API eller andra åtgärder), ska bekräftelsen skickas så snart händelsen har tagits emot och det är upp till klienten att behandla händelsen senare.
* Om man inte erkänner händelsen så snart som möjligt kan det påverka händelsernas realtidskaraktär, eftersom efterföljande händelser kommer att utsändas först när den tidigare bekräftelsen har mottagits.
* Klienter kan svara med en godkänd HTTP 202-statuskod för att bekräfta att händelsen har accepterats.

## Begränsningar

* Arbetsstöd övervägs inte för webhook-händelser under kategorin LO:er eftersom de vanligtvis används för att hjälpa elever att slutföra andra utbildningsobjekt.
* En pensionering av en utbildningsobjektinstans betraktas som en uppdateringshändelse. Det skulle inte finnas någon delete-händelse för en instans eftersom den bara kan dras tillbaka, inte tas bort.
* Sessionsändringar samlades då in som en del av instansens uppdateringshändelse. Detta gäller endast kurser. Det kommer inte att ske någon ökning från enheter på lägre nivå för instanser av utbildningsvägar eller certifieringsinstanser.
* Om en utbildningsväg innehåller en kurs och en elev slutför kursen via utbildningsvägen kommer två **elevframsteg** händelser att genereras - en för kursen och en för utbildningsvägen.
* Vissa arbetsflöden beräknar attribut för utbildningsobjekt, t.ex. varaktighet och leveranstyp, asynkront. Därför genereras händelser för dessa utbildningsobjekt när cron-jobbet har bearbetats klart.
* Om en kurs registreras via ett överordnat utbildningsprogram eller en certifiering, kommer händelserna för registrering, avregistrering och slutförande endast att utlösas för det överordnade utbildningsprogrammet eller certifieringen. Dessa händelser utlöses inte för den underordnade kursen eftersom registreringen skedde indirekt.
* Webhooks stöds endast för konton med statusen **[!UICONTROL ACTIVE]**. De är inte tillgängliga för **[!UICONTROL TRIAL]**- eller **[!UICONTROL INACTIVE]**-konton.

## Exempel på nyttolaster för händelserna

+++CI_STATS

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12345-0458-4450-b5dd-6bc1ef4f8b50",
      "eventName": "CI_STATS",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123456785-LoSt",
      "data": {
        "loInstanceId": "course:12345678_14448475",
        "waitlistCount": 0,
        "enrollmentCount": 10,
        "seatLimit": 30
      }
    }
  ]
}
```

+++

+++COURSE_ENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12345c1-4576-4ec5-a057-3a6f078cc9d6",
      "eventName": "COURSE_ENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123424713000-040366-10488-0",
      "data": {
        "userId": 12345678,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++COURSE_ENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234ec1-4576-4ec5-a057-3a6f078cc9d6",
      "eventName": "COURSE_ENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123424713000-040366-10488-0",
      "data": {
        "userId": 12345678,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++COURSE_COMPLETED

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "c2345c-6c98-4ed3-b0b0-ba3da5087c1c",
      "eventName": "COURSE_COMPLETED",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "12345823000-040363-12018-0",
      "data": {
        "userId": 11080928,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14448484",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
        "hasPassed": true
      }
    }
  ]
}
```

+++

+++COURSE_COMPLETED_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "c23458c-6c98-4ed3-b0b0-ba3da5087c1c",
      "eventName": "COURSE_COMPLETED_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123456823000-040363-12018-0",
      "data": {
        "userId": 12345678,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14448484",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
        "hasPassed": true
      }
    }
    ]
}
```

+++

+++LEARNING_PATH_ENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234791-338f-4c4c-83bc-9f73ea794965",
      "eventName": "LEARNING_PATH_ENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123404248000-040653-71396-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:1234567",
        "loInstanceId": "learningProgram:1234567_109139",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++LEARNING_PATH_ENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12340791-338f-4c4c-83bc-9f73ea794965",
      "eventName": "LEARNING_PATH_ENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123404248000-040653-71396-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:1234557",
        "loInstanceId": "learningProgram:1234557_109139",
        "loType": "learningProgram",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++LEARNING_PATH_COMPLETED

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "123404e-d554-4027-944b-086debefdddf",
      "eventName": "LEARNING_PATH_COMPLETED",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234604391000-040653-314618-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:92348",
        "loInstanceId": "learningProgram:92348_95662",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
        "hasPassed": true
      }
    }
  ]
  }
```

+++

+++LEARNING_PATH_COMPLETED_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12344e-d554-4027-944b-086debefdddf",
      "eventName": "LEARNING_PATH_COMPLETED_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123404391000-040653-314618-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:92348",
        "loInstanceId": "learningProgram:92348_95662",
        "loType": "learningProgram",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
        "hasPassed": true
      }
    } 
    ]
    }
```

+++

+++CERTIFICATION_ENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234e776-148e-4128-80e9-b896a460b655",
      "eventName": "CERTIFICATION_ENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "12344672000-040654-559128-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:123418",
        "loInstanceId": "certification:123418_160299",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
}
```

+++

+++CERTIFICATION_ENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "123472ec1-4576-4ec5-a057-3a6f078cc9d6",
      "eventName": "CERTIFICATION_ENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234524713000-040366-10488-0",
      "data": {
        "userId": 12345678,
        "loId": "course:123456798",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++CERTIFICATION_COMPLETED

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234bf8-7521-4bc0-bc51-7f951ff63ea9",
      "eventName": "CERTIFICATION_COMPLETED",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123454768000-040654-756257-0",
      "data": {
        "userId": 123456728,
        "loId": "certification:123418",
        "loInstanceId": "certification:134518_160299",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++CERTIFICATION_COMPLETED_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "123453bf8-7521-4bc0-bc51-7f951ff63ea9",
      "eventName": "CERTIFICATION_COMPLETED_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234604768000-040654-756257-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:123418",
        "loInstanceId": "certification:123418_160299",
        "loType": "certification",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++LEARNER_PROGRESS

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "d1234d3a4-c3df-44fa-a1cf-7edd6e3d2075",
      "eventName": "LEARNER_PROGRESS",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235604551000-297002-5823-0",
      "data": {
        "loId": "course:7542090",
        "loType": "course",
        "userId": 12380928,
        "loInstanceId": "course:7232090_10423047",
        "dateStarted": "2024-11-08T03:49:52.000Z",
        "progressPercent": 50
      }
}
]
}
```

+++

+++COURSE_UNENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "f3237817-8cb8-40ea-a441-813bec1c7724",
      "eventName": "COURSE_UNENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1345506253000-040298-24078-0",
      "data": {
        "userId": 12311591,
        "loId": "course:12324298",
        "loInstanceId": "course:12324298_14450088",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
      }
    }
  ]
}
```

+++

+++COURSE_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "f2317817-8cb8-40ea-a441-813bec1c7724",
      "eventName": "COURSE_UNENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "17235506253000-040298-24078-0",
      "data": {
        "userId": 12311591,
        "loId": "course:12324298",
        "loInstanceId": "course:12324298_14450088",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL"
    }
   }
  ]
}
```

+++

+++LEARNING_PATH_UNENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "823df878-1dfd-47ac-9bfe-7d4952e3edd1",
      "eventName": "LEARNING_PATH_UNENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235506667000-040299-28209-0",
      "data": {
        "userId": 12311591,
        "loId": "learning_program:123157",
        "loInstanceId": "learning_program:123157_109139",
        "loType": "learning_program",
        "enrollmentSource": "SELF_ENROLL",
      }
    }
]
}
```

+++

+++LEARNING_PATH_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "8e23f878-1dfd-47ac-9bfe-7d4952e3edd1",
      "eventName": "LEARNING_PATH_UNENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235506667000-040299-28209-0",
      "data": {
        "userId": 12311591,
        "loId": "learning_program:123157",
        "loInstanceId": "learning_program:123157_109139",
        "loType": "learning_program",
        "enrollmentSource": "ADMIN_ENROLL"
      }
    }
]
}
```

+++

+++CERTIFICATION_UNENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "7232766b-54d8-472d-b933-7e89d1b75ef8",
      "eventName": "CERTIFICATION_UNENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235507900000-040304-1065-0",
      "data": {
        "userId": 12311591,
        "loId": "certification:123199",
        "loInstanceId": "certification:123199_162078",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL"
      }
    }
  ]
}
```

+++

+++CERTIFICATION_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "7202766b-54d8-472d-b933-7e89d1b75ef8",
      "eventName": "CERTIFICATION_UNENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1735507900000-040304-1065-0",
      "data": {
        "userId": 12511591,
        "loId": "certification:139199",
        "loInstanceId": "certification:139199_162078",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_DRAFT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12345da9f-26ec-453c-b56a-cdf18a841948",
      "eventName": "LEARNING_OBJECT_DRAFT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234519188000-040344-48604-0",
      "data": {
        "loId": "course:1234091",
        "loType": "course"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_DELETION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234a690-5517-4c09-9cde-d953cdd8582c",
      "eventName": "LEARNING_OBJECT_DELETION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235605296000-040656-662792-0",
      "data": {
        "loId": "course:12319716",
        "loType": "course"
      }
    }
   ]
}
```

+++

+++LEARNING_OBJECT_MODIFICATION

```
{
  "accountId": 8308,
  "events": [
    {
      "eventId": "223e068-af3e-4dd3-a515-ce19d7234873",
      "eventName": "LEARNING_OBJECT_MODIFICATION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123350842000-039736-54153-0",
      "data": {
        "loId": "learningProgram:123836",
        "loType": "learningProgram"
      }
    }
   ]
}
```

+++

+++LEARNING_OBJECT_MODIFICATION_BATCH

```
{
  "accountId": 8308,
  "events": [
    {
      "eventId": "1234e068-af3e-4dd3-a515-ce19d7234873",
      "eventName": "LEARNING_OBJECT_MODIFICATION_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235350842000-039736-54153-0",
      "data": {
        "loId": "learningProgram:123836",
        "loType": "learningProgram"
      }
    }
   ]
}
```

+++

+++LEARNING_OBJECT_INSTANCE_MODIFICATION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "121da98-ab8d-43e9-b671-e79131cd69dc",
      "eventName": "LEARNING_OBJECT_INSTANCE_MODIFICATION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235603297000-040649-741781-0",
      "data": {
        "loInstanceId": "course:12324298_14453691",
        "loId": "course:12324298",
        "loType": "course"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1231da98-ab8d-43e9-b671-e79131cd69dc",
      "eventName": "LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123603297000-040649-741781-0",
      "data": {
        "loInstanceId": "course:12324298_14453691",
        "loId": "course:12324298",
        "loType": "course"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_INSTANCE_DELETION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12d16e90-d73a-457b-83f3-666ba9654edb",
      "eventName": "LEARNING_OBJECT_INSTANCE_DELETION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235605491000-040657-236307-0",
      "data": {
        "loInstanceId": "course:12319674_14453849",
        "loId": "course:12319674",
        "loType": "course"
      }
    }
  ]
}
```

+++
