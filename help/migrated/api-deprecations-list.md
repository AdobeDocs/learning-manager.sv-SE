---
jcr-language: en_us
title: API-borttagningar i Adobe Learning Manager
description: I takt med att API:erna i Adobe Learning Manager utvecklas omorganiseras eller uppgraderas API:er regelbundet. När API:er utvecklas blir det gamla API:t inaktuellt och så småningom borttaget. Den här sidan innehåller information som du behöver känna till när du migrerar från föråldrade API-versioner till nyare och stabilare API-versioner.
contentowner: saghosh
source-git-commit: 01cdcd816fe101af55adf0902f4e3660a1a098ce
workflow-type: tm+mt
source-wordcount: '847'
ht-degree: 0%

---


# Borttagningar och ändringar av API i Adobe Learning Manager

## API-borttagningar i mars 2024-versionen av Adobe Learning Manager

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

På grund av att ett stort antal poster har hämtats av förskjutningsvärdet och att den totala prestandan har blivit långsammare tillämpar vi en gräns på **500** register. I nästa version kommer **GET användare** API returnerar högst **500** register.

Om du behöver fler poster använder du **GET jobb** API.

Ändringen av förskjutningsgränser gäller för alla nya kunder. För befintliga kunder gäller 90-dagarsregeln.

### Exkludera sökvägar

För närvarande följer Learning Manager API:er en diagramdatastruktur, som gör att du kan hämta data genom att gå igenom API-modellen via inkluderingar. Även om du kan gå igenom ett API upp till sju nivåer, är det datormässigt dyrt att hämta data med ett enda API-anrop.

Vi rekommenderar att alla befintliga och nya kunder ringer små samtal flera gånger i stället för ett stort samtal. På så sätt förhindrar du att oönskade data läses in i samtalet.

Vi vill upprätthålla dessa restriktioner för nya konton och upprätthålla en tillåtelselista över befintliga konton.

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

### Antal ändringar av instanssammanfattning

För närvarande hämtar du antalet alla möjliga instanser i LO Summary-slutpunkten. För en kurs kan du till exempel visa antalet registreringar och väntelistor i svaret på **GET /learningObjects/{loId}/instanser/{loInstanceId}/summary**. Du kan sedan visa completionCount och enrollmentCount i svaret. Om kursen är VC eller klassrum kan du även se platsbegränsningen och väntelistan.

Processen för att hämta antal slutförda och registreringar är beräkningskrävande, därför görs beräkningen på begäran. Om data inte finns i cacheminnet läses de in igen, vilket är beräkningsintensivt. Om det finns många användare som registrerar sig för en kurs är antalet stora och påverkar effektivt CPU-prestandan.

I nästa version av Adobe Learning Manager cachelagras slutpunkterna completionCount, enrollmentCount, seatLimit och waitlistCount i slutpunkten för LO-instanssammanfattningen. Den cachelagrade informationen kvarstår tills det finns ändringar i registreringar eller avregistreringar. För antal som överskrider 1 000 registreringar antar vi de uppskattade antalet och ogiltigförklarar resultaten för alla befintliga och nya konton.

>[!NOTE]
>
>För antal, till exempel completionCount, enrollmentCount, seatLimit och waitlistCount, som överstiger 1000, är det lämpligt att tolka dem som uppskattningar snarare än exakta siffror, eftersom dessa hämtas från cachen.

### Sortera på namn

I nästa version av Adobe Learning Manager kommer namn och -namn att tas bort i sorteringsfältet för följande API:er:

* GET /userGroups/{userGroupId}/users
* GET/användare

>[!NOTE]
>
>Sortera efter namn och -name kommer att tas bort för alla befintliga och nya konton.


## API-borttagningar i november 2023-versionen av Adobe Learning Manager

### Åsidosättningsflagga

I november 2023-versionen av Adobe Learning Manager har vi tagit bort åsidosättningsflaggan från API:erna. Åsidosättningsflaggan ingår inte i den offentliga API-specifikationen och är avsedd för serverdelstestning. Flaggan har nu tagits bort för Elevers API:er. Flaggan är dock fortfarande giltig för Admin API:er.

Anledningen till att vi tar bort flaggan för Elevers API:er är att åsidosättningsflaggan hämtade en stor mängd data via Elevers API:er.

Framöver kommer följande Elev-API att sluta fungera eftersom det har åsidosättningsflaggan.

_/primeapi/v2/users?page[utjämna]=0&amp;sida[gräns]=10&amp;sort=id&amp;override=TRUE_

### API-ändringar för nya kompetensbaserade rekommendationer

Adobe Learning Manager förbättrar rekommendationerna för kund- och partneraktiverade konton. Denna förbättring av rekommendationsalgoritmen med ändringen av rangordningsalgoritmen för kurs, utbildningsväg och certifiering ger en bättre användarupplevelse vid innehållsidentifiering.

Algoritmen tillåter inte längre peer-baserade rekommendationer. Ändringen påverkar inte de befintliga användarna, men alternativet Branschjusterad finns kvar. För alternativet Anpassad tillåter Adobe Learning Manager inte längre anpassat peer-baserat val.

Den kollegiala gruppen blir nu ett konto, och eleverna ser en sträng som visar de populära ämnena i gruppen. Alla rekommendationer är förklarliga. Om du till exempel visar något i ett ämne kommer kortet på remsan att visa orsaken till kursen.

### Ändringar i aviseringsrapporten

I tidigare versioner av Adobe Learning Manager saknades filter för meddelanderapporten. Adobe Learning Manager har hämtat alla aviseringar på kontot.

I november 2023-versionen har vi lagt till ett datumfilter som du kan använda för att hämta meddelandena inom en angiven period.  Du kan dock bara hämta rapporten för de senaste sex månaderna.