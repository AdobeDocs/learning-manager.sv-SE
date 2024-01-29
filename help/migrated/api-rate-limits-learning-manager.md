---
jcr-language: en_us
title: API-hastighetsbegränsningar i Learning Manager
contentowner: saghosh
preview: true
source-git-commit: 544c695a77c21dd9162b9b943b6119d27aa373dc
workflow-type: tm+mt
source-wordcount: '1757'
ht-degree: 0%

---



# API-hastighetsbegränsningar i Learning Manager

## Introduktion till hastighetsbegränsning {#introductiontoratelimiting}

Adobe Learning Manager har en omfattande uppsättning REST API som hjälper kunder att skapa program som kan integreras med Learning Manager och till och med anpassade användarupplevelser och tillägg till arbetsflöden som hjälper deras företag.

När ett API anropas finns delade datorresurser som används i Learning Manager-servrarna, och därför måste vi vara försiktiga och se till att applikationerna fungerar bra och inte äventyrar plattformens prestanda och tillgänglighetsegenskaper. Detta åstadkoms genom att införa begränsningar för hur API-klienter ringer samtal (frekvens och hastighet).

Ett program kan till exempel försöka hämta alla användare till kontot och kan göra flera paginerade API-anrop i snabb takt. Och av misstag kan en utvecklare kalla detta i en snäv slinga vilket resulterar i en enorm belastning på servern och gör applikationer tröga och även äventyra plattformen genom att förbruka mer resurser än vad som är avsett eller krävs.

För att lösa det här problemet inför vi hastighetsbegränsningar för hur många API-anrop som kan göras av en enskild användare i ett specifikt klientprogram för ett specifikt konto. Vi mäter detta i termer av Begäranden Per minut, förkortat RPM. När vi till exempel säger att maxgränsen för GET API-anrop är 600 varv/min innebär det bara att en enskild användare inte kan överskrida maxgränsen på 600 anrop per minut, och om användaren överskrider den gränsen kommer användaren att få en begränsad hastighet. Begärandena spåras med millisekundsmått, så denna gräns motsvarar en begäran var 100:e millisekund (ms). Det finns ytterligare en parameter, Burst, som också definieras tillsammans med hastighetsgränsen, som definierar hur många förfrågningar en användare kan göra utöver den angivna hastigheten (i vårt fall 600RPM). Om till exempel Burst-parametern är 10, innebär det att upp till 10 kortplatser kommer att tilldelas i en kö och när en begäran anländer &quot;för tidigt&quot; (i vårt fall tidigare än 100 ms), behandlas den omedelbart om det finns en kortplats tillgänglig för den i kön. Platsen markeras sedan som &quot;tagen&quot; och frigörs inte för användning av en annan begäran förrän lämplig tid har passerat (i vårt fall efter 100ms). Verklig trafik är i allmänhet med sprickor, och det är där burst parametern hjälper. För Learning Manager-plattformen definierar vi gränser för en specifik API-version (till exempel V2), en roll (elev/administratör) och ett verb (GET/PUT/POST/DELETE/PATCH). I exemplet ovan skulle vi säga att räntesatsen är (600, 10).

Även om vi alltid har haft hastighetsbegränsningar för Public API i Learning Manager har vi varit ganska liberala med att tillåta en mycket hög RPM hittills. I och med tillväxten av din favoritutbildningsplattform har vi dock sett en snabb ökning av användningen av vårt API, och vi har beslutat att göra dessa hastighetsbegränsningar uttryckligen dokumenterade för alla våra kunders bästa och för bättre hantering av plattformen. I det här sammanhanget har vi uppgraderat vårt API för att börja returnera ett nytt API-svar (HTTP-statuskod 429), som du inte har sett hittills. Det här svaret ges till API-klienter när hastighetsgränsen överskrids. Klientprogram måste nu hantera denna svarskod så att den passar logiken i deras program. Det här dokumentet är främst avsett för att hjälpa utvecklare att få den information de behöver för att införliva rätt logik i sin kod när de ser ett sådant svar.

## Hur bekräftar man de påtvingade hastighetsbegränsningarna? {#howtoconfirmtheenforcedratelimits}

Svarsrubrikerna innehåller följande information för varje begäran:

```
x-rate-limit: 600r/m 
x-burst: 10
```

* x-rate-limit anger basvärdet för begärandefrekvensen i termer av begäranden per minut.
* x-burst anger hur många begäranden som överskrider basbegärandefrekvensen som accepteras för att behandlas omedelbart.

## Hur hittar jag fel som orsakas av hastighetsbegränsningar? {#howtocatcherrorscausedbyratelimits}

För varje förfrågan kan du kontrollera om du har ökat i taxegränsen. Om du får svarskoden 429, &quot;{&quot;message&quot;:&quot;429 För många förfrågningar&quot;}&quot;, har du nått hastighetsgränsen.

Det är bästa praxis att inkludera kod i skriptet som fångar upp 429 svar. Om skriptet ignorerar felet &quot;För många förfrågningar&quot; och fortsätter att försöka göra förfrågningar kan du börja få null-fel. Då kommer felinformationen inte att vara användbar för att diagnostisera problemet.

En curl-begäran som till exempel hoppar in i hastighetsgränsen kan returnera följande svar:

```
< HTTP/2 429 
< date: Wed, 04 Nov 2020 06:53:04 GMT 
< content-type: application/json; charset=utf-8 
< server: openresty 
< x-rate-limit: 60r/m 
< x-burst: 10 
< retry-after: 10.752 
< access-control-allow-credentials: true 
< access-control-allow-methods: GET, POST, OPTIONS, PUT, HEAD, DELETE, PATCH 
< access-control-allow-headers: X-acap-all-roles, X-acap-account,X-acap-user,X-acap-caller-role,Keep-Alive,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type, x-experience-api-version, Authorization, X-CSRF-TOKEN, X-HTTP-Method-Override 
< strict-transport-security: max-age=31536000; includeSubDomains 
< x-frame-options: SAMEORIGIN 
< x-xss-protection: 1 
< x-content-type-options: nosniff 
< x-request-id: gwBBFC9741-58A5-43B1-B1FE-7D14275961E7 
< strict-transport-security: max-age=31536000; includeSubDomains
```

Svaret innehåller information om följande nycklar:

```
status: 429 
retry-after: 10.752
```

Statuskoden 429 innebär &quot;för många begäranden&quot; och att den aktuella begäran inte behandlas. Huvudet retry-after anger att du kan försöka med API-anropet på 10,752 sekunder. Din kod bör sluta göra ytterligare API-begäranden tills det har gått tillräckligt lång tid för att försöka igen.

Följande pseudokod visar ett enkelt sätt att fånga upp hastighetsbegränsningsfel:

```
response = request.get(url) 
if response.status equals 429: 
    alert('Rate limited. Waiting to retry…') 
    wait(response.retry-after) 
    retry(url)
```

Vi har faktiskt till och med skapat ett dummy API för Learning Manager så att du kan experimentera och bli bekväm med att hantera statuskoden 429.

```
curl -X GET --header 'Accept: application/json' --header 'Authorization: oauth < 
<token>
  >' 'https://learningmanager.adobe.com/learningmanagerapi/v2/dummy 
</token>
```

Detta dummy API har en gräns på:

```
x-rate-limit: 5r/m 
x-burst: 2
```

Gränsen för dummy API är avsiktligt låg, så att du stöter dig in i hastighetsgränserna mycket snabbt och sedan kan fokusera mer på att utveckla koden för att fånga upp och hantera hastighetsbegränsningsfel.

## Testa dummy API {#testingthedummyapi}

Vi har angett en slutpunkt där du kan kontrollera hur hastighetsbegränsning fungerar. För detta har vi skapat en särskild slutpunkt som heter GET /dummy och som har elevens läsomfattning. Detta API har avsiktligt konfigurerats för en mycket strikt hastighetsgräns på 5 förfrågningar per minut, med sprängningsgräns = 2.

Du kan enkelt testa det här genom att trycka på den här slutpunkten med hastigheter under 5 varv/min och över 5 varv/min. Skriv kod för att hantera HTTPS-statuskoden 429 och baserat på informationen i svarsrubrikerna.

För att göra det enkelt för dig kan kolla in detta exempel JavaScript kod som illustrerar detta. Klicka här [rulla med](https://jsfiddle.net/ACAPJS/9yv8zcmL/) och se hur koden fungerar.

Det här programmet kräver att du anger en programtoken för elevroll för ditt konto. Se [Användarhandbok för programutvecklare](https://captivateLearning Manager.adobe.com/docs/Learning ManagerAPI/v2/) för information om API-token och du kan använda Hjälp för token i avsnittet Utvecklarresurser i programmet Learning Manager Integration Admin för att generera token.

Det här programmet gör 10 anrop till dummy API i en slinga, på en gång. Eftersom hastighetsgränsen är (5, 2) för dummy API, kommer hastighetsgränsen att överskridas efter de första 5+2 anropen som tas emot av Learning Manager, och du kommer att se ett framgångsrikt svar för dem.

Observera dock hur detta program letar efter 429 statuskod som svar och hur de hanteras. När programmet får ett sådant svar skriver det ut informationen i API-svaret, väntar på föreslagen tid och gör om de misslyckade försöken.

## Bästa praxis för att hantera hastighetsbegränsning {#bestpracticestohandleratelimiting}

Många gånger ändras inte data på ett konto så ofta. Till exempel kanske inte kurserna på ett konto ändras så ofta. I stället för att försöka få alla data varje gång, se om du kan få specifika data när du behöver dem och överväga att använda en cache mekanism. På så sätt, när din ansökan verkligen behöver göra många samtal, du kommer att ha tillräcklig kvot inom din taxa gränser för att göra dessa viktiga samtal.

Vissa data kan ändras oftare och du kan behöva hämta dem oftare. Även om så är fallet, fråga dig själv om ditt program har råd att ha något föråldrade data (något som kan finnas i din cache, som du hämtade N minuter sedan), eftersom det kan ha någon inverkan på användarens arbetsflöde. Även om du måste hämta nya data från servrarna, kan du återigen vara klok i att hämta just de data du behöver, istället för att få allt.

Det kommer också att finnas tillfällen, när du har inget val att få en massa data eftersom API kanske inte är tillräckligt flexibelt för att ge dig exakt vad du vill med bara ett samtal. Se om API:et tillhandahåller filter och sorteringsvillkor som kan användas för att minimera antalet anrop och du bör fortfarande överväga cachelagring eftersom många användare på ditt konto kan behöva samma data.

När du får för mycket data i samband med ett interaktivt program med ett användargränssnitt är det troligt att programmet försöker göra för mycket och kan överväldiga användaren med mycket information/funktionalitet som påverkar användarupplevelsen i ditt program.

När du skapar ett icke-interaktivt program (kanske något som ett dagligt jobb) kan du behöva hämta en massa data i grupp. I sådana fall bör du använda Job API som i första hand är utformat för att returnera gruppdata i CSV-format. Observera att jobb-API:t har en kvotbegränsning som du kan anropa dem N gånger om dagen.

Eftersom Learning Manager har implementerat JSONAPI-specifikationerna finns det API där du även kan läsa in vissa data separat. Detta kommer att hjälpa dig att spara att göra ytterligare API-anrop, men du kommer att behöva byta detta med att få data alltför ivrigt. Eftersom de sidinlästa data ibland kan vara mycket stora, gör du i sidindelade API-anrop att den maximala sidstorleken är begränsad till 10, men för API-anrop utan inkluderar kan du kanske ange en större sidstorlek (upp till 100)

Så småningom, om du gör en hel del API-begäranden på kort tid, du kommer att stöta till API-hastighetsgränsen för förfrågningar. När du har nått gränsen slutar Learning Manager att behandla fler förfrågningar tills en viss tid har gått.

Hastighetsbegränsningarna beskrivs i det sista avsnittet i den här artikeln. Du bör bekanta dig med gränserna.

## Hastighetsbegränsningar för V2 API-slutpunkter {#ratelimitsforv2apiendpoints}

Följande tabell visar gränserna för de olika V2-slutpunkterna. För närvarande införs inga begränsningar för kunderna, men dessa begränsningar kommer att gälla från och med den DD/MM/ÅÅÅÅ. Det blir därför viktigt för kunder att granska sina befintliga programs kod för att se hur de kan justera sin kod för att vara medvetna om dessa hastighetsbegränsningar och hantera API-svaren med HTTP-statuskoden 429.

<table> 
 <tbody>
  <tr> 
   <td><p><b>Åtgärd</b></p></td> 
   <td><p><b>Admin-API</b></p></td> 
   <td><p><b>Elevens API</b></p></td> 
  </tr> 
  <tr> 
   <td><p>DELETE</p></td> 
   <td><p>25, 10) <br></p></td> 
   <td><p>(20, 10)<br></p></td> 
  </tr> 
  <tr> 
   <td><p>PATCH</p></td> 
   <td><p>(60, 20)</p></td> 
   <td><p>(15, 5) <br></p></td> 
  </tr> 
  <tr> 
   <td><p>POST</p></td> 
   <td><p>(30, 10)<br></p></td> 
   <td><p>(30, 10)<br></p></td> 
  </tr> 
  <tr> 
   <td><p>PUT</p></td> 
   <td><p>(20, 10)<br></p></td> 
   <td><p>(20, 10)<br></p></td> 
  </tr> 
  <tr> 
   <td><p>GET</p></td> 
   <td><p>(100, 100)<br></p></td> 
   <td><p>(100, 30)<br></p></td> 
  </tr> 
 </tbody>
</table>

