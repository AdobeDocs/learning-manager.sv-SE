---
jcr-language: en_us
title: API-borttagningar i Adobe Learning Manager
description: I takt med att API:erna i Adobe Learning Manager utvecklas organiseras och uppgraderas API:er regelbundet. När API:er utvecklas blir det gamla API:t inaktuellt och så småningom borttaget. Den här sidan innehåller information som du behöver känna till när du migrerar från föråldrade API-versioner till nyare och stabilare API-versioner.
contentowner: saghosh
exl-id: 0fe9a3cb-9114-42d6-81ae-1a4f28c984fa
source-git-commit: 670d0477b246af2a0257e41eca799817e391b348
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 0%

---

# Borttagningar och ändringar av API i Adobe Learning Manager

## API-utfasningar i mars 2024-versionen av Adobe Learning Manager

<!-- ### Changes in Rate Limits

With the next release of Adobe Learning Manager, we're restructuring API rate limits for new accounts. For existing accounts, only the Admin APIs will be rate-limited. After 90 days (about 3 months), we will restructure rate limits for all APIs, but existing accounts will be whitelisted according to current usage. Existing accounts need to revisit their learner API usage. 

For new accounts, if they want to increase the rate limits, they must contact the Customer Success team of ALM. 

#### Which APIs will be rate limited 

For new accounts, all Admin, Learner, and Search APIs will have rate limits and burst enforced.  

The API burst rate or burst limit refers to the maximum number of requests allowed to be made to an API in a short burst within a limited timeframe. 

The following table lists the rate and burst limits for the APIs.

<table>
    <tr>
        <th>API</th>
        <th>Number of requests-RPM</th>
        <th>Number of requests-Burst</th>
    </tr>
    <tr>
        <td>Admin</td>
        <td>5</td>
        <td>5</td>
    </tr>
    <tr>
        <td>Learner</td>
        <td>20</td>
        <td>5</td>
    </tr>
    <tr>
        <td>Search</td>
        <td>50</td>
        <td>5</td>
    </tr>
</table>
-->

### Ändringar av förskjutningsgränser

På grund av att ett stort antal poster har hämtats av förskjutningsvärdet och att den totala prestandan har blivit långsammare tillämpar vi en gräns på **500** poster. I nästa version returnerar **GET users**-API:t för både admin och elev högst **500** poster.

Använd API:et **GET-jobb** om du behöver fler poster.

<!--### Exclude paths 

At present, Learning Manager APIs follow a graph data structure, which allows you to fetch data by traversing the API model through includes. Even though you could traverse an API up to seven levels, fetching the data using a single API call is computationally expensive. 

We recommend that all existing and new customers make small calls multiple times instead of one large call. This approach will prevent unwanted data from being loaded in the call. 

We want to enforce these restrictions on new accounts and maintain a whitelist of existing accounts.-->

#### Vilka sökvägar är inaktuella

Följande sökvägar har tagits bort:

* /learningObjects
   * Borttagna sökvägar:
      * enrollment.loInstance.loResources.resources
      * instances.loResources.resources
   * Nya banor:
      * enrollment.loInstance.loResources
      * instances.loResources

* /learningObjects/{id}
   * Föråldrad sökväg:
      * enrollment.instances.subLoInstances.learningObject
   * Ny bana:
      * enrollment.instances.subLoInstances

* /enrollments
   * Föråldrad sökväg:
      * loInstance.learningObject.enrollment
   * Ny bana:
      * loInstance.learningObject

* /learningObjects/{id}
   * Föråldrad sökväg:
      * instance.subLoInstances.learningObject.enrollment.loResourceGrades
   * Ny bana:
      * instance.subLoInstances

<!--### Instance summary count changes 

Currently, in the LO summary endpoint, you fetch the number of all possible instances. For example, for a course, you can view the number of enrollments and waitlists in the response for **GET /learningObjects/{loId}/instances/{loInstanceId}/summary**. You can then view the completionCount and enrollmentCount in the response. If the course is a VC or classroom, you can also view its seat limit and waitlist limit. 

The process of retrieving the completion and enrollment counts is computationally expensive, therefore the calculation is done on a request basis. If the data is not present in the cache, the data is reloaded, which is computationally intensive. If there are many users enrolling in a course, the counts will be large, and effectively impacts CPU performance. 

In the next release of Adobe Learning Manager, in the LO Instance summary endpoint, the completionCount, enrollmentCount, seatLimit, and waitlistCount are cached. The cached information persists till there are changes in enrollments or unenrollments. For counts exceeding 1000 enrollments, we'll assume the estimated counts, and invalidate the results for all existing and new accounts.

>[!NOTE]
>
>For counts, such as, completionCount, enrollmentCount, seatLimit, and waitlistCount exceeding1000, it's advisable to interpret them as estimates rather than precise figures, as these will be retrieved from cache.-->

### Sortera på namn

I nästa version av Adobe Learning Manager kommer namn och -name att tas bort i sorteringsfältet för följande API:er:

* GET /userGroups/{userGroupId}/users
* GET/användare

>[!NOTE]
>
>Sortera efter namn och -name kommer att tas bort för alla befintliga och nya konton.


## API-utfasningar i november 2023-versionen av Adobe Learning Manager

### Åsidosättningsflagga

I november 2023-versionen av Adobe Learning Manager har vi tagit bort åsidosättningsflaggan från API:erna. Åsidosättningsflaggan ingår inte i den offentliga API-specifikationen och är avsedd för serverdelstestning. Flaggan har nu tagits bort för Elevers API:er. Flaggan är dock fortfarande giltig för Admin API:er.

Anledningen till att vi tar bort flaggan för Elevers API:er är att åsidosättningsflaggan hämtade en stor mängd data via Elevers API:er.

Framöver kommer följande Elev-API att sluta fungera eftersom det har åsidosättningsflaggan.

_/primeapi/v2/users?page[offset]=0&amp;page[limit]=10&amp;sort=id&amp;override=TRUE_

### API-ändringar för nya kompetensbaserade rekommendationer

Adobe Learning Manager förbättrar rekommendationerna för kund- och partneraktiverade konton. Denna förbättring av rekommendationsalgoritmen med ändringen av rangordningsalgoritmen för kurs, utbildningsväg och certifiering ger en bättre användarupplevelse vid innehållsidentifiering.

Algoritmen tillåter inte längre peer-baserade rekommendationer. Ändringen påverkar inte de befintliga användarna, men alternativet Branschjusterad finns kvar. För alternativet Anpassad tillåter Adobe Learning Manager inte längre anpassat peer-baserat val.

Den kollegiala gruppen blir nu ett konto, och eleverna ser en sträng som visar de populära ämnena i gruppen. Alla rekommendationer är förklarliga. Om du till exempel visar något i ett ämne kommer kortet på remsan att visa orsaken till kursen.

### Ändringar i aviseringsrapporten

I tidigare versioner av Adobe Learning Manager hade meddelanderapporten inga filter. Adobe Learning Manager har hämtat alla meddelanden på kontot.

I november 2023-versionen har vi lagt till ett datumfilter som du kan använda för att hämta meddelandena inom en angiven period.  Du kan dock bara hämta rapporten för de senaste sex månaderna.

### Borttagning av höga förskjutningsvärden i slutpunkten GET/användare

För att förbättra systemprestanda och hantera resursutnyttjande mer effektivt har Adobe utfasat höga motvärden i slutpunkten GET/users för både **ADMIN** och **ELEVER**. Vi rekommenderar att du använder **Jobs API** för att hämta poster med ett förskjutningsvärde.

