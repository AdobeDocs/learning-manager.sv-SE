---
jcr-language: en_us
title: API-dokumentation för inbäddad Player-interaktion
description: Lär dig mer om olika API:er för att lyssna på händelser och utlösa åtgärder i den inbäddade spelaren
contentowner: chandrum
exl-id: 4734ecc1-cc8a-40b0-8997-32a31ec661ec
source-git-commit: 3d183dc40e4d1962d25160b74d8cf6cfa26e3171
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 8%

---

# API-dokumentation för inbäddad Player-interaktion

Adobe Learning Manager tillhandahåller ett bibliotek som kan integreras i ett program. Det här biblioteket innehåller olika API:er för att lyssna på händelser och utlösa åtgärder i den inbäddade spelaren.

Med de tillhandahållna API:erna kan du spela upp, pausa och utföra andra åtgärder på spelaren.

## Läs in biblioteket

Biblioteket är tillgängligt på den här [platsen](https://cpcontents.adobe.com/public/publiccdn/playerInteractionLib.min.js).

Läs in biblioteket genom att följa stegen nedan:

1. Läs in js-filen i konsumentprogrammet.
2. När biblioteket laddas fylls window.cpPlayerLib i.

>[!NOTE]
>
>Om du inte använder prod US anger du parametrarna cpPlayerLib.env och cpPlayerLib.sourceOrigin baserat på din env.

Standardvärdena är:

* window.cpPlayerLib.env = [https://learningmanager.adobe.com/app/player](https://learningmanager.adobe.com/app/player);
* window.cpPlayerLib.sourceOrigin = &quot;[https://cpcontents.adobe.com](https://cpcontents.adobe.com/)&quot;;

### Tillgängliga metoder

Biblioteket cpPlayerLib består av följande funktioner:

**startPlayer**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>startPlayer</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Läser in en spelare i appen.</td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>LoID : Utbildningsobjekts-ID.</li><li>konto-ID : konto-ID för ALM-kontot.</li><li>userId : Användar-id.</li><li>accessToken : Åtkomsttoken.</li><li>domRefId: ID:t för div-behållaren där spelaren måste renderas.</li><li>onModuleLoaded: Den här funktionen anropas när modulerna med nedanstående information läses in.</li><br><li>contentType</li><li>loId</li><li>moduleId</li><li>Genomgång av</li><li>currentLanguage</li><li>availableLanguages</li><li>isCCAvailable</li><li>ccEnabled</li></br></td>
</tr>
<tr>
<td>Returer</td>
<td>Returnerar ett löfte. Vid lösning av löftet, en playerObj kommer att passeras.</td>
</tr>
<tr>
<td>Undantag</td>
<td>Löftet kommer att resultera i ett undantag.</td>
</tr>
<tr>
<td>Exempelkod</td>
<td>cpPlayerLib.startPlayer(loId, accountId, userId, accessToken, domRefId, onModuleLoaded).then((playerObj) =&gt; {//playerObj har API:er för att interagera med spelaren}) &gt;</td>
</tr>
</tbody>
</table>

**getAllPlayers**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>getAllPlayers</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Returnerar alla spelarobjekt på den aktuella sidan.</td>
</tr>
<tr>
<td>Parametrar</td>
<td>Inget</td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>cpPlayerLib.getAllPlayers()</td>
</tr>
</tbody>
</table>

**getPlayer**


<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>getPlayer</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Returnerar ett spelarobjekt med angivet ID för utbildningsobjekt.</td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>LoID : Utbildningsobjekts-ID.</li></td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>cpPlayerLib.getPlayer(loId)</td>
</tr>
</tbody>
</table>

**navigateToModule**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>navigateToModule</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Gå till nästa modul.</td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>moduleId: modul-id.</li></td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>playerObj.navigateToModule(moduleID)</td>
</tr>
</tbody>
</table>

**nästa**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>nästa</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Gå till nästa modul.</td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>Inget</li></td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>playerObj.next()</td>
</tr>
</tbody>
</table>

**tidigare**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>föregående</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Gå till föregående modul.</td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>Inget</li></td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>playerObj.previous()</td>
</tr>
</tbody>
</table>

**toggleTOC**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>toggleTOC</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Växla panelen för innehållsförteckning i spelaren.</td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>Inget</li></td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>playerObj.toggleTOC()</td>
</tr>
</tbody>
</table>

**växlingsanteckningar**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>toggleNotes</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Växla anteckningspanelen i spelaren.</td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>Inget</li></td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>playerObj.toggleNotes()</td>
</tr>
</tbody>
</table>

**toggleClosedCaption**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>toggleClosedCaption</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Aktivera/avaktivera visning av undertexter i spelaren.</td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>Inget</li></td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>playerObj.toggleClosedCaption()</td>
</tr>
</tbody>
</table>

**changeLanguage**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>changeLanguage</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Ändra språk för innehållet i spelaren.</td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>språk: Språkkoden som ska anges.</li></td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>playerObj.changeLanguage("es")</td>
</tr>
</tbody>
</table>

**closePlayer**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>closePlayer</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Stäng spelaren och ta bort den från sidan. </td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>Inget</li></td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>playerObj.closePlayer()</td>
</tr>
</tbody>
</table>

**togglePlayPause**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>togglePlayPause</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Växla mellan att spela upp och pausa innehållet i spelaren.</td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>Inget</li></td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>playerObj.togglePlayPause()</td>
</tr>
</tbody>
</table>

**setVolume**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>setVolume</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Ställ in volymen för spelaren. Värdet måste vara mellan 0 och 1.</td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>volym: Volymens värde. Giltigt intervall är 0-1. </li></td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>playerObj.setVolume(0.5)</td>
</tr>
</tbody>
</table>

**setPlayBackSpeed**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>setPlayBackSpeed</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Ställ in uppspelningshastigheten i spelaren.</td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>hastighet: värdet på den hastighet som ska anges. Giltiga värden är .25, .5, .75, 1, 1.25, 1.5, 1.75, 2.</li></td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>playerObj.setPlayBackSpeed(1.25)</td>
</tr>
</tbody>
</table>

**sök**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>söka</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Hoppa till när som helst på videon.</td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>tid: Dags att hoppa till. Tiden är i sekunder.</li></td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>playerObj.seek(50)</td>
</tr>
</tbody>
</table>

**framåt**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>vidarebefordra</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Hoppa framåt i videon med 10 sekunder.</td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>Inget</li></td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>playerObj.forward()</td>
</tr>
</tbody>
</table>

**bakåt**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>efterbliven</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Hoppa bakåt i videon med 10 sekunder.</td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>Inget</li></td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>playerObj.backward()</td>
</tr>
</tbody>
</table>

**navigateToPage**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>navigateToPage</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Hoppa till angiven sida på PPT/PDF.</td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>pageNumber: Sidnumret som du vill gå till.</li></td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>playerObj.navigateToPage (5)</td>
</tr>
</tbody>
</table>

**nextPage**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>nextPage</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Hoppa till nästa sida på PPT/PDF.</td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>Inget</li></td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>playerObj.nextPage()</td>
</tr>
</tbody>
</table>

**previousPage**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>previousPage</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Hoppa till föregående sida på PPT/PDF.</td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>Inget</li></td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>playerObj.previousPage()</td>
</tr>
</tbody>
</table>

**zoomaIn**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>zoomIn</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Zooma in på innehåll på en PPT/PDF.</td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>Inget</li></td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>playerObj.zoomIn()</td>
</tr>
</tbody>
</table>

**zooma ut**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>zoomOut</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Zooma ut på innehåll på en PPT/PDF.</td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>Inget</li></td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>playerObj.zoomOut()</td>
</tr>
</tbody>
</table>

**downloadJobAid**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>downloadJobAid</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Ladda ned arbetsstöd från en kurs.</td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>Inget</li></td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>playerObj.downloadJobAid()</td>
</tr>
</tbody>
</table>

**toggleJobAidPullout**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>toggleJobAidPullout</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Om du vill ladda ned ett arbetsstöd eller inte.</td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>Inget</li></td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>playerObj.toggleJobAidPullout()</td>
</tr>
</tbody>
</table>

**helskärm**

<table>
<tbody>
<tr>
<td>Metodnamn</td>
<td>fullScreen</td>
</tr>
<tr>
<td>Beskrivning</td>
<td>Ställ in spelaren på helskärmsläge.</td>
</tr>
<tr>
<td>Parametrar</td>
<td><li>Inget</li></td>
</tr>
</tr>
<tr>
<td>Exempelkod</td>
<td>playerObj.fullScreen()</td>
</tr>
</tbody>
</table>

## Lista över händelser

**onPlayerEvents(callBack)**

När du registrerar återanropsfunktionen anropas alla spelarhändelser. Händelsenamnen är följande:

* SPELA UPP (video/ljud/CP)
* PAUSA (Video/Ljud/CP)
* TIMEUPDATE (video/ljud/CP)
* PAGECHANGE (PPT/PDF)
* ANTECKNAT (allt innehåll)
* STARTAD (allt innehåll)
* INLEDDES (allt innehåll)
* SLUTFÖRT (allt innehåll)
* GODKÄNT (allt innehåll)
* MISSLYCKADES (allt innehåll)

**onStreamingEvents(callBack)**

När du registrerar återanropsfunktionen anropas alla Player-satser som skickas för att spåra användaraktivitet.
