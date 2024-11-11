---
jcr-language: en_us
title: Webhooks
description: Läs mer om webbhookar som du kan skicka realtidsinformation om, till exempel kursregistrering, skapande av kurser och annan information till en specifik URL
contentowner: chandrum
source-git-commit: e4b0526e11083d116bf4ca4b0816892e0e8f0f9d
workflow-type: tm+mt
source-wordcount: '1664'
ht-degree: 1%

---

# Webhooks

Med en webhook kan en enhet automatiskt skicka realtidsdata eller meddelanden till en annan enhet när en specifik händelse inträffar. Det kommer att göra det möjligt för ett program att förse andra program med information utan att ständigt begära det. Om en användare till exempel slutför en kurs i LMS (Learning Management System) kan en webhook automatiskt skicka den informationen till en annan plattform, till exempel ett CRM- eller rapporteringsverktyg. Webhooks används ofta i integreringar för att automatisera processer och minska behovet av manuella uppdateringar mellan system. Konfigurera webhooks genom att ange en återanropsadress som du vill skicka data till.

## Webhooks jämfört med API:er

Webhooks och API:er hjälper båda system att kommunicera med varandra, men de fungerar på olika sätt. Med API:er delas informationen bara när användaren begär den. Om en elev till exempel behöver data om kursförlopp skickar hen en begäran till API:t, som sedan tillhandahåller informationen. Å andra sidan skickar webhookar automatiskt data omedelbart när en händelse inträffar. Om en elev till exempel slutför en kurs kommer den att skicka data omedelbart till avlyssnarens URL utan några manuella begäranden.

## Vad är API:er i realtid?

Med API:er i realtid kan program direkt utbyta data när en händelse inträffar. Till skillnad från traditionella API:er, som väntar på att en användare ska begära information, delar API:er i realtid data så fort det sker. Webhooks fungerar som ett API i realtid och hjälper till att dela data omedelbart när den angivna händelsen inträffar. Real-time API ser till att denna dataöverföring sker omedelbart utan att någon manuell begäran behövs, vilket gör att systemen kan hållas uppdaterade omedelbart.

## Webhook-händelser

Webhook-händelser är specifika åtgärder som sker i ett system som automatiskt skickar data till en avlyssnar-URL. När en elev till exempel registrerar sig för en kurs utlöses en webhook-händelse och skickar registreringsinformationen till lyssnarens URL.
Webhook-händelser delas in i två kategorier:

* **Realtidshändelser**: Händelser bearbetas och skickas i realtid till ett mål-URL
* **Icke-realtidshändelser**: Händelser bearbetas i grupper och skickas vid angivna tider i stället för i realtid

## Lyssnar-URL

En Avlyssnar-URL är en slutpunkt eller ett mål som tar emot datainformation när en händelse inträffar. När en specifik händelse inträffar, t.ex. en användare som registrerar sig för en kurs, skickar systemet automatiskt informationen till denna URL utan någon manuell begäran. Lyssnar-URL:en är den adress där alla dessa uppdateringar levereras.
Webhook skickar relevant information i ett JSON-format. Här är ett exempel på nyttolast för en händelse som utlösts i Adobe Learning Manager:

```
{
  "accountId": 1010,
  "events": [
    {
      "eventId": "d5fb7071-10a9-46b2-9f9e-79dde346c052",
      "eventName": "COURSE_ENROLLMENT_BATCH",
      "timestamp": 1727414643000,
      "eventInfo": "1727414643000-047210-84242-0",
      "data": {
        "userId": 4279332,
        "loId": "course:7374992",
        "loInstanceId": "course:7376092_10250977",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": 1727414643
      }
    }
  ]
}
```

## Skapa och hantera webhookar - integrationsadministratör

Följ stegen nedan för att skapa webbhooks-integrering i Adobe Learning Manager:

1. Logga in som **[!UICONTROL Integration Admin]**.
2. På startsidan väljer du **[!UICONTROL Webhooks]** > **[!UICONTROL Add Webhook]**.

   ![](assets/create-webhook.png)
   _Lägg till en webhook_

3. Ange **[!UICONTROL Name]** och **[!UICONTROL Description]** för webhooken.
4. Ange avlyssnarens URL som **[!UICONTROL Target URL]** där du vill skicka händelsedata.
5. Välj någon av autentiseringsmetoderna:
Autentisering i webbhookar är en säkerhetsmetod för att säkerställa att data som skickas till en avlyssnar-URL kommer från en betrodd källa.
   * **[!UICONTROL None]**: Ingen autentisering krävs.
   * **[!UICONTROL Basic]**: Det här är autentiseringsbaserad. Ange användarnamn och lösenord.
   * **[!UICONTROL Signature]**: Systemet skapar en speciell signatur och lägger till den i webhook-data. Den mottagande servern kontrollerar koden för att se till att data är verkliga och inte har ändrats. Generera en signatur och använd den för autentisering. Hämta signaturen som JSON.
6. Välj webhook-händelser från listrutan **[!UICONTROL Trigger events]**.

   >[!NOTE]
   >
   >Du kan även testa webhookarna genom att markera alternativet Testa webhookar på sidan Lägg till webhook.

7. Välj växlingsknappen **[!UICONTROL Activation Status]** för att aktivera webhooken. När det har aktiverats skickas data när de markerade händelserna inträffar.

>[!NOTE]
>
>Du kan skapa och hantera upp till fem webbhookar.

### Redigera webbhookar - integrationsadministratör

Så här redigerar du webhookar från Adobe Learning Manager:

1. Logga in som **[!UICONTROL Integration Admin.]**
2. Välj **[!UICONTROL Webhooks]** på startsidan.
3. Välj den webhook du vill redigera.

   ![](assets/edit-webhook.png)
   _Redigera webhooken_
4. Välj **[!UICONTROL Edit]** för att ändra webhookens information och välj **[!UICONTROL Save]**.

### Ta bort webbhookar - integrationsadministratör

Så här redigerar du webhookar från Adobe Learning Manager:

1. Logga in som **[!UICONTROL Integration Admin]**.
2. Välj **[!UICONTROL Webhooks]** på startsidan.
3. Välj den webhook som du vill ta bort.
4. Välj **[!UICONTROL Delete]** för att ta bort webhooks.

![](assets/delete-webhooks.png)
_Ta bort webhook_

### Ta bort webhookar - integrationsadministratör

Gör så här för att ta webhookarna ur bruk:

1. Logga in som **[!UICONTROL Integration Admin]**.
2. Välj **[!UICONTROL Webhooks]** på startsidan.
3. Välj den webhook du vill redigera.
4. Välj **[!UICONTROL Edit]** och inaktivera **[!UICONTROL Activation Status]** för att ta webhooken ur bruk.

![](assets/retire-webhook.png)
_Ta webhooken ur bruk_

## Händelser i realtid

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

## Händelser som inte sker i realtid

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

## Bästa metoder för webhookar

Webhookar möjliggör händelsestyrd kommunikation i realtid mellan tjänster. Felaktig implementering kan dock leda till förlorade händelser, långsamma systemprestanda eller säkerhetsrisker. Nedan visas de bästa metoderna för att implementera webhookar, med fokus på feltolerans, tillförlitlighet och säkerhet.

### Feltolerans

Feltoleransen för ALM-webhooksystemet ger rekommendationer för prenumeranter som hanterar potentiella problem, t.ex. händelseförlust, dubbletthändelser och leverans utanför beställning.

ALM har en anslutningstidsgräns på 10 sekunder och en sockettimeout på 5 sekunder. Förväntningarna är att kunden bekräftar meddelandet så snart det tar emot dem. Detta är för att säkerställa att klienten inte fördröjs under bearbetning av meddelanden. Om det finns någon nedströmsbearbetning som är tidskrävande, klienten bör ändå bekräfta händelsen omedelbart och sedan hantera nedströmsbearbetningen i sin ände.

#### Datalagring

Evenemangen sparas i 7 dagar. Om de inte bearbetas inom den här tiden går de förlorade för alltid. Om återställning sker den sista dagen och det behövs mer tid förlängs inte kvarhållningsperioden.
Om händelser produceras snabbare än de konsumeras kan vissa händelser gå förlorade. Även om detta är ovanligt, abonnenter bör övervaka för att förhindra att det blir en långsiktig fråga.

#### Inaktivera webhookar

När en prenumerant inte svarar på webhook-händelser gör ALM-systemet ett nytt försök att använda webhookar med exponentiell backoff för att undvika att överväldiga prenumeranten.

Återförsöksprocessen startar med ett inledande intervall på 5 sekunder. Om prenumeranten inte svarar fördubblas väntetiden till 10, 20, 40 och 80 sekunder, och ökar så småningom till maximalt 5 minuter. När det når 5 minuter fortsätter systemet att försöka igen var femte minut tills kvarhållningsperioden på 7 dagar är slut. Om prenumeranten fortfarande inte svarar under hela den här perioden inaktiveras webhooken automatiskt. En påminnelse kommer att skickas till prenumeranten med jämna mellanrum.

#### Duplicera händelser

Om det tar mer än fem sekunder för en prenumerant att svara efter att en händelse har bearbetats, kan systemet försöka behandla samma händelse igen. Vi rekommenderar att du använder händelse-ID:n för att hålla reda på vilka händelser som redan har bearbetats. Och om en webhook kraschar efter att händelsen har skickats men innan du sparar att den har bearbetats, kan samma händelsegrupp försöka igen. Vi rekommenderar att du använder batch-ID:n eller enskilda händelse-ID:n för att känna igen och ignorera eventuella dubbletter.

#### Oordnade händelser

ALM försöker hålla händelserna i rätt ordning, men ibland kan händelserna levereras i fel ordning, särskilt mellan realtidshändelser och händelser utanför realtid.

Om en administratör registrerar flera elever i en kurs samtidigt markeras registreringshändelserna som icke-realtid. Men om en elev slutför kursen snabbt markeras slutförandehändelsen som realtid och kan levereras före registreringshändelserna.

#### Rekommendation för feltolerans

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


## Exempel på nyttolaster för händelserna

+++CI_STATS

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "01234567-0458-4450-b5dd-6bc1edr4560",
      "eventName": "CI_STATS",
      "timestamp": 1725604147,
      "eventInfo": "1725604145-LoSt",
      "data": {
        "loInstanceId": "course:1234567_123456775",
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
      "eventId": "29123ec1-4576-4ec5-a057-3a6dr45t9d6",
      "eventName": "COURSE_ENROLLMENT",
      "timestamp": 1725524713,
      "eventInfo": "1725524713000-040366-10488-0",
      "data": {
        "userId": 1234567,
        "loId": "course:1234567",
        "loInstanceId": "course:1234567_1234567",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": 1725524713
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
      "eventId": "29572ec1-4576-4ec5-a057-3wsd43r59d6",
      "eventName": "COURSE_ENROLLMENT_BATCH",
      "timestamp": 1725524713,
      "eventInfo": "1725524713000-040366-10488-0",
      "data": {
        "userId": 1234567,
        "loId": "course:1234567",
        "loInstanceId": "course:12345678_123456788",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": 1725524713
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
      "eventId": "c1a3168c-6c98-4ed3-b0b0-ba3da5087c1c",
      "eventName": "COURSE_COMPLETED",
      "timestamp": 1725523823,
      "eventInfo": "1725523823000-040363-12018-0",
      "data": {
        "userId": 12345678,
        "loId": "course:12345671",
        "loInstanceId": "course:1234567_12345674",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": 1725523818,
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
      "eventId": "c1a3168c-6c98-4ed3-b0b0-ba3da5087c1c",
      "eventName": "COURSE_COMPLETED_BATCH",
      "timestamp": 1725523823,
      "eventInfo": "1725523823000-040363-12018-0",
      "data": {
        "userId": 112345678,
        "loId": "course:12345678",
        "loInstanceId": "course:1234567_12345678",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": 1725523818,
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
      "eventId": "96ed0791-338f-4c4c-83bc-9fwfr4564965",
      "eventName": "LEARNING_PATH_ENROLLMENT",
      "timestamp": 1725604249,
      "eventInfo": "1725604248000-040653-71396-0",
      "data": {
        "userId": 11234567,
        "loId": "learningProgram:123456",
        "loInstanceId": "learningProgram:12345_134567",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": 1725604248
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
      "eventId": "96edft791-338f-4c4c-83bc-9f7erf94965",
      "eventName": "LEARNING_PATH_ENROLLMENT",
      "timestamp": 1725604249,
      "eventInfo": "1725604248000-040653-71396-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:12347",
        "loInstanceId": "learningProgram:12345_12345",
        "loType": "learningProgram",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": 1725604248
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
      "eventId": "e207104e-d554-4027-944b-08fty6fdddf",
      "eventName": "LEARNING_PATH_COMPLETED",
      "timestamp": 1725604392,
      "eventInfo": "1725604391000-040653-314618-0",
      "data": {
        "userId": 11080928,
        "loId": "learningProgram:12345",
        "loInstanceId": "learningProgram:12345_95662",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": 1725604380,
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
      "eventId": "e207104e-d554-4027-944b-086debefdddf",
      "eventName": "LEARNING_PATH_COMPLETED",
      "timestamp": 1725604392,
      "eventInfo": "1725604391000-040653-314618-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:12345",
        "loInstanceId": "learningProgram:12345_95662",
        "loType": "learningProgram",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": 1725604380,
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
      "eventId": "8bdfr76-148e-4128-80e9-b89123456755",
      "eventName": "CERTIFICATION_ENROLLMENT",
      "timestamp": 1725604672,
      "eventInfo": "1725604672000-040654-559128-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:1234567",
        "loInstanceId": "certification:123456_160299",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": 1725604672
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
      "eventId": "8b2ee776-148e-4128-80e9-12345678",
      "eventName": "CERTIFICATION_ENROLLMENT_BATCH",
      "timestamp": 1725604672,
      "eventInfo": "1725604672000-040654-559128-0",
      "data": {
        "userId": 123456788,
        "loId": "certification:1234567",
        "loInstanceId": "certification:12345678_160299",
        "loType": "certification",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": 1725604672
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
      "eventId": "b8b63bf8-7521-4bc0-bc51-7f951ff63ea9",
      "eventName": "CERTIFICATION_COMPLETED",
      "timestamp": 1725604769,
      "eventInfo": "1725604768000-040654-756257-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:1245678",
        "loInstanceId": "certification:1234567_160299",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": 1725604740
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
      "eventId": "b8b63bf8-7521-4bc0-bc51-7f951ff63ea9",
      "eventName": "CERTIFICATION_COMPLETED_BATCH",
      "timestamp": 1725604769,
      "eventInfo": "1725604768000-040654-756257-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:134567",
        "loInstanceId": "certification:1234567_160299",
        "loType": "certification",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": 1725604740
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
      "eventId": "dd04d3a4-c3df-44fa-a1cf-7edd6e3d2075",
      "eventName": "LEARNER_PROGRESS",
      "timestamp": 1725604552,
      "eventInfo": "1725604551000-297002-5823-0",
      "data": {
        "loId": "course:7542090",
        "loType": "course",
        "userId": 12345678,
        "loInstanceId": "course:1234567_11234567",
        "dateStarted": 1725604380,
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
      "eventId": "f3417817-8cb8-40ea-a441-813bec1c7724",
      "eventName": "COURSE_UNENROLLMENT",
      "timestamp": 1725515824,
      "eventInfo": "1725506253000-040298-24078-0",
      "data": {
        "userId": 12345671,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14450088",
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
      "eventId": "f3417817-8cb8-40ea-a441-8123e45724",
      "eventName": "COURSE_UNENROLLMENT_BATCH",
      "timestamp": 1725515824,
      "eventInfo": "1725506253000-040298-24078-0",
      "data": {
        "userId": 123456781,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14450088",
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
      "eventId": "8e5df878-1dfd-47ac-9bfe-7d123456d1",
      "eventName": "LEARNING_PATH_UNENROLLMENT",
      "timestamp": 1725516573,
      "eventInfo": "1725506667000-040299-28209-0",
      "data": {
        "userId": 12345678,
        "loId": "learning_program:1234567",
        "loInstanceId": "learning_program:1234567_109139",
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
      "eventId": "8e5df878-1dfd-47ac-9bfe-7d4952e3edd1",
      "eventName": "LEARNING_PATH_UNENROLLMENT",
      "timestamp": 1725516573,
      "eventInfo": "1725506667000-040299-28209-0",
      "data": {
        "userId": 1234567,
        "loId": "learning_program:1234567",
        "loInstanceId": "learning_program:1234567_109139",
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
      "eventId": "7902766b-54d8-472d-b933-7e89d1b75ef8",
      "eventName": "CERTIFICATION_UNENROLLMENT",
      "timestamp": 1725517341,
      "eventInfo": "1725507900000-040304-1065-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:1234567",
        "loInstanceId": "certification:12345678_162078",
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
      "eventId": "7902766b-54d8-472d-b933-7e89d1b75ef8",
      "eventName": "CERTIFICATION_UNENROLLMENT_BATCH",
      "timestamp": 1725517341,
      "eventInfo": "1725507900000-040304-1065-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:1234567",
        "loInstanceId": "certification:1234567_162078",
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
      "eventId": "1712349f-26ec-453c-b56a-cdf18a841948",
      "eventName": "LEARNING_OBJECT_DRAFT",
      "timestamp": 1725519188,
      "eventInfo": "1725519188000-040344-48604-0",
      "data": {
        "loId": "course:12345671",
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
      "eventId": "023456-5517-4c09-9cde-d953cdd8582c",
      "eventName": "LEARNING_OBJECT_DELETION",
      "timestamp": 1725605296,
      "eventInfo": "1234567800-040656-662792-0",
      "data": {
        "loId": "course:1234567",
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
  "accountId": 1234,
  "events": [
    {
      "eventId": "22345668-af3e-4dd3-a515-ce19d7234873",
      "eventName": "LEARNING_OBJECT_MODIFICATION_BATCH",
      "timestamp": 1725523081,
      "eventInfo": "123456000-039736-54153-0",
      "data": {
        "loId": "learningProgram:1234567",
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
  "accountId": 1234,
  "events": [
    {
      "eventId": "2234567068-af3e-4dd3-a515-ce19d7234873",
      "eventName": "LEARNING_OBJECT_MODIFICATION_BATCH",
      "timestamp": 1725523081,
      "eventInfo": "123456700-039736-54153-0",
      "data": {
        "loId": "learningProgram:1234567",
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
      "eventId": "b131da98-ab8d-43e9-b671-e79131cd69dc",
      "eventName": "LEARNING_OBJECT_INSTANCE_MODIFICATION",
      "timestamp": 1725603298,
      "eventInfo": "1723456000-040649-741781-0",
      "data": {
        "loInstanceId": "course:12345678_14453691",
        "loId": "course:12345678",
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
      "eventId": "b23458-ab8d-43e9-b671-e79131cd69dc",
      "eventName": "LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH",
      "timestamp": 1725603298,
      "eventInfo": "112345000-040649-741781-0",
      "data": {
        "loInstanceId": "course:12345678_14453691",
        "loId": "course:1234568",
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
      "eventId": "1234560-d73a-457b-83f3-666ba9654edb",
      "eventName": "LEARNING_OBJECT_INSTANCE_DELETION",
      "timestamp": 1725605491,
      "eventInfo": "17223456700-040657-236307-0",
      "data": {
        "loInstanceId": "course:1234567_14453849",
        "loId": "course:1234567",
        "loType": "course"

      }
    }
  ]
}
```

+++

