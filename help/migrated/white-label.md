---
jcr-language: en_us
title: Vit märkning i mobilappen Adobe Learning Manager
description: Vit märkning är en metod att byta namn på en app eller tjänst med ditt eget varumärke och anpassa den som om du vore den ursprungliga skaparen. I Adobe Learning Manager kan du använda vit etikettering i mobilappen så att du kan byta varumärke på appen och göra den tillgänglig för användarna under ditt eget varumärke.
contentowner: saghosh
exl-id: f37c86e6-d4e3-4095-9e9d-7a5cd0d45e43
source-git-commit: 0c97b147a1e4c6e1a4a0cc69f56f8e9420c4602b
workflow-type: tm+mt
source-wordcount: '2081'
ht-degree: 0%

---

# Vit märkning i mobilappen Adobe Learning Manager

Adobe Learning Manager-mobilappen stöder nu vit märkning, vilket innebär att du nu kan släppa appen under ditt eget varumärke.

ALM kommer att göra tillgängliga uppdaterade vita märkta binära filer enligt följande tidslinjer:

1. För större versioner av mobilappen kommer filer att göras tillgängliga två veckor i förväg.
2. För alla planerade uppdateringar av brådskande korrigeringar kommer filer att göras tillgängliga en vecka i förväg.
3. För oplanerade, brådskande och omedelbara korrigeringar kommer filer att göras tillgängliga så gott de kan.

Binärfiler görs tillgängliga i kundens utsedda mappar. Kontakta dina CSM:er för att få åtkomst till filerna. Kunden ansvarar för publicering i rätt tid och relaterade processer.

## Hur du ska börja förbereda för att starta ett program med vit etikett

Gör så här för att distribuera och hantera ditt eget program med vita etiketter:

1. Förbered resurserna (t.ex. en välkomstbild) och texten så att båda kan användas i appen och beskrivningen i app/play-butiken.

1. Tilldela en teknisk resurs som kan:

   * Genererar certifikatfiler för push-meddelanden.
   * Signera programmets binärfiler som tillhandahålls av ALM-teamet.
   * Ladda upp och hantera publiceringsprocessen. Publiceringsprocessen kräver kommunikation mellan apphanteraren och app/play store-team om att din app följer alla publiceringsriktlinjer. Från ALM får du en helt kompatibel app binär.

## Översikt

Vit märkning är en metod att byta namn på en app eller tjänst med ditt eget varumärke och anpassa den som om du vore den ursprungliga skaparen. I Adobe Learning Manager kan du använda vit etikettering i mobilappen så att du kan byta varumärke på appen och göra den tillgänglig för användarna under ditt eget varumärke.

## Vad kan anpassas

Du kan anpassa följande:

### Fält

<table>

 <tbody>

  <tr>

   <td>

    <p>Konto-ID</p>

   </td>

   <td>

    <p>ID för ditt konto. Observera att det vitmärkta programmet inte är tillgängligt för elever som tillhör något annat konto.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Ytterligare konto-ID</p>

   </td>

   <td>

    <p>Lägg till flera konton (underdomäner) om du vill. Lägg till underdomänerna som kommaavgränsade utan mellanslag. Till exempel acc01,acc02,acc03 och så vidare.<br> <b>Obs!</b> Du måste lägga till konto-ID när du anger underdomänerna.</br> </p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Programnamn</p></td>

   <td>

    <p>Namnet som du vill använda för appen.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Kortnamn för app</p>

   </td>

   <td>

    <p>I fall där namnet på appen är långt ska du ge den ett kort namn som visas på enheten.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Internt programnamn</p></td>

   <td>

    <p>Namnet som operativsystemet identifierar programmet med. Det format som vanligtvis används är: com.company-name.product-name.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Internt programnamn - iOS</p>

   </td>

   <td>

    <p>Namnge programmet på ett annat sätt om användarna använder iOS. Vi rekommenderar att du använder samma namn för både iOS och Android.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Appikon</p>

   </td>

   <td>

    <p>Appikonen som png. Den här ikonen visas i ditt program. Formatet som ska namnges är account-id_appIcon.png. Appikonens dimensioner är 512 × 512 pixlar.<div>Observera att Apple inte tillåter Alpha-kanal i appikoner. Se därför till att ta bort Alpha-kanalen från mediefilen innan du skickar in den.</div></p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Appstartskärm</p></td>

   <td>

    <p>Ange en bild (png) som visas när användarna startar programmet på programmets välkomstskärm. Formatet som ska namnges är account-id_splashIcon.png. De kvadratiska välkomstskärmarna är 1 052 × 1 052 pixlar och de cirkelbaserade välkomstskärmarna är 768 x 768 pixlar.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Klient-ID och Klienthemlighet</p>

   </td>

   <td>

    <p>Integreringsadministratören för ditt konto tillhandahåller informationen medan du registrerar programmet. Integreringsadministratören måste använda detta:<ul><li>elev:läsa,elev:skriva som roll</li><li>internt program name://redirect som omdirigerings-URL</li></ul></p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Kontologotyp</p>

   </td>

   <td>

    <p>Den URL som är värd för organisationens logotyp. Ange en cpcontent-länk som kontologotyp. Webbadressen måste vara webbkodad.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Appbutikens ID för appen (iOS)</p>

   </td>

   <td>

    <p>Det ID som krävs för att implementera force-uppdateringen. Appen måste veta att eleven ska omdirigeras till appbutiken för att uppdatera appen.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Google Play Store-id för appen (Android)</p>

   </td>

   <td>

    <p>Det ID som krävs för att implementera force-uppdateringen.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Värdnamn för djuplänkning</p>

   </td>

   <td>

    <p>Använd Learning Manager om du vill vara värd för dina djuplänkar. Om du vill använda ett annat värdnamn som en djuplänk anger du värddatorns URL. Exempel: learningmanager.adobe.com.</p>

   </td>

  </tr>

 </tbody>

</table>

>[!NOTE]
>
>Ange informationen i dina CSAM-filer så att de kan lägga till den i din anpassade binära app.


#### Uppdatera webbplatsassociationen för att hantera anpassade djuplänkar

Om du använder en anpassad domän eller Learning Manager\*.adobe.com som värd behöver du inte vidta några åtgärder. Men om du använder en anpassad lösning eller ett specifikt värdnamn för webbadresserna ska du lägga till platsassociationsfilerna.

>[!CAUTION]
>
>Om filerna inte visas fungerar inte djuplänkarna. Se till att filerna finns.


Mer information finns på följande länkar:

* [Android](https://learningmanager.adobe.com/.well-known/assetlinks.json)
* [iOS](https://learningmanager.adobe.com/.well-known/apple-app-site-association)

## Skaffa ett team-id till App Store

För att få ditt team-id:

1. Logga in på ditt **[!UICONTROL Apple Developer]**-konto.
2. Välj **[!UICONTROL Membership Details]** högst upp på sidan och kopiera ditt team-id.

Detta ID krävs för att lägga till den vita märkta programposten i metadatafilerna för att aktivera djuplänkning.

## Skaffa SHA-256-fingeravtrycket för Android

SHA-256-fingeravtrycket för Android-signeringscertifikatet krävs när appposten med vit etikett läggs till.

Så här genererar du SHA-256-fingeravtryck:

1. Kör följande kommando:

```
keytool -list -v -keystore <keystore/jks file> -alias <aliaskey> -storepass <storepassword> -keypass <keypassword>
```

Leta reda på Certifikatfingeravtryck i utdata och kopiera sedan SHA-256-värdet. Dela det här fingeravtrycket efter behov för konfigurationen för djuplänkning.

## Generera push-meddelanden

Det krävs två olika mekanismer för att skicka push-meddelanden till Android- och iOS-program.

* Generera certifikat för push-meddelanden för iOS.
* För Android anger du en servernyckel som genereras från Firebase-projektet.

Följ anvisningarna nedan för att konfigurera projekten i Firebase:

### Push-aviseringar på iOS

Ett push-meddelandecertifikat är en kryptografisk autentiseringsuppgift inom iOS-apputveckling som utfärdas av Apple och som gör det möjligt för en server att på ett säkert sätt skicka push-meddelanden till en iOS-enhet via Apple Push Notification Service (APN:er).

Certifikatet garanterar säker kommunikation mellan servern (eller leverantören) och Apple APN-filer när push-meddelanden skickas till iOS-enheter.

Både Android och iOS använder Firebase Cloud Messaging (FCM) som tjänst för att skicka push-meddelanden till enheter.

### Så här genererar du certifikatet i iOS

Följ proceduren:

1. Generera eller hämta **Push Notification-certifikatet** och den privata nyckeln (.p12). Mer information finns i [Apple-utvecklardokumentet](https://developer.apple.com/documentation/usernotifications/setting_up_a_remote_notification_server/establishing_a_certificate-based_connection_to_apns).

1. Installera p12-filen när filen har hämtats. Använd lösenordet för att installera i din **Nyckelhanterare**.

1. Gå till **Mina certifikat** och exportera certifikatet. Se till att du väljer MIME-typen .cer.

1. Kör följande kommandon när du har p12-filen och CER-filen tillgängliga:

```
- openssl pkcs12 -in privatekey.p12 -out myapnappkey.pem -nodes –clcerts

- openssl x509 -in privatekey.cer -inform DER -out myapnsappcert.pem 

- openssl s_client -connect gateway.sandbox.push.apple.com:2195 -cert myapnsappcert.pem -key myapnappkey.pem 
```

Om du kan ansluta till servern är certifikatet du har skapat giltigt. Kopiera certifikatet och värdena för den privata nyckeln från filen myapnappkey.pem.

### Push-meddelanden på Android

För Android måste användaren ange filen services.json från Firebase-projektet för att lägga till posten i SNS-tjänsten.

Skapa ett projekt i Firebase och dela filen services.json till CSM-teamet. Denna fil behövs för tokenbaserad post i SNS. Observera att servernyckeln inte längre används. Se [Skapa projekt i Firebase](#create-project-in-firebase).

Gör så här för att hämta filen services.json:

1. Logga in på **Firebase**-konsolen.
1. Gå till **Projektinställningar** och välj **Molnmeddelanden**.
1. Hitta **Firebase Cloud Messaging API** och välj **Hantera tjänstkonton**.
1. På sidan **Tjänstkonton** väljer du **Tjänstkonton** i den vänstra panelen.
1. Hitta din projektpost och välj **Hantera information** under åtgärder.

   >[!NOTE]
   >
   >   Projektposten kommer att ha formatet &lt;-accountname->@appspot.gserviceaccount.com.

1. Gå till fliken **Nycklar** och välj **Lägg till nyckel**.
1. Om det inte finns någon nyckel väljer du **Skapa ny nyckel** och väljer **JSON** som nyckeltyp. JSON-filen genereras och hämtas.
1. Om det redan finns en nyckel väljer du **Överför befintlig nyckel**, klistrar in nyckeln och överför den. JSON-filen genereras och hämtas.

<!-- Set up a project in Firebase and share the server key with the CSAM.-->

Kontakta CSM-teamet och dela JSON-filen för att lägga till posten till SNS-tjänsterna på AWS. Användare måste få posten registrerad i SNS-tjänsten för push-meddelandet, vilket kräver att de delar certifikaten som genereras ovan för validering.

## Skapa projekt i Firebase {#create-project-in-firebase}

### Android

Återanvänd samma projekt som du skapade i stegen ovan för push-meddelanden.

[Lägg till projektet](https://learn.microsoft.com/en-us/xamarin/android/data-cloud/google-messaging/firebase-cloud-messaging) i Firebase och hämta ***google-services.json***-filen.

### iOS

[Lägg till projektet](https://firebase.google.com/docs/ios/setup) i Firebase och hämta ***GoogleService-Info.plist***-filen.

>[!IMPORTANT]
>
>Skicka filerna till Adobe Learning Manager CSAM-teamet som ska inkludera i bygget av den binära appfilen.


## Generera signerade binärfiler

### iOS

<!--```
sh""" xcodebuild -exportArchive -archivePath Runner.xcarchive -exportPath "ipa_path/" -exportOptionsPlist {ExportFile} 

mv ipa_path/*.ipa "${env.AppName}_signed.ipa" """ 
```-->

Mappen `<root>` innehåller filen **Runner.xcarchive.zip**. Kör kommandona nedan för att generera den signerade binärfilen:

1. Kör följande kommando för att packa upp arkivet:

   ```
   unzip Runner.xcarchive.zip
   ```

2. Gå till programkatalogen:

   ```
   cd Runner.xcarchive/Products/Applications/Runner.app
   ```

3. Kopiera etableringsfilen för mobil:

   ```
   cp <path>/<mobile-provisioningfile>.mobileprovision embedded.mobileprovision
   ```

4. Kör följande kommando för att uppdatera din signeringsinformation till ramverksbiblioteket:

   ```
   codesign -f -s "Distribution Certificate Name" Frameworks/*
   ```

5. Gå tillbaka till mappen `<root>` (där Runner.xcarchive.zip finns):

   ```
   cd <root>
   ```

6. Exportera arkivet med xcodebuild:

   ```
   xcodebuild -exportArchive -archivePath Runner.xcarchive -exportPath ipa_path/ -exportOptionsPlist <path>/<ExportOptions-file>.plist
   ```

7. Leta reda på .ipa-filen i mappen ipa_path.
8. Överför .ipa-filen till webbplatsen `Diawi`.
9. När det är helt uppladdat väljer du knappen **[!UICONTROL Send]**.
10. När det är klart får du en QR-kod och en länk.
11. Öppna QR-koden eller länken direkt i Safari.

Om enheten ingår i etableringsprofilen ska installationen fortsätta på enheten.

>[!NOTE]
>
>Du behöver XCode 15.2 eller senare för att skapa de signerade binärfilerna.


### Android

**För apk-filen**

>[!IMPORTANT]
>
>Innan du kör kommandot `apksigner` kör du följande kommandon för att exportera ditt Keystore-lösenord och nyckelaliaslösenord som miljövariabler:
>
>```
>export KS_PASS=your_keystore_password
>export KEY_PASS=your_key_password
>```

```
sh""" <path>/apksigner sign --ks $storeFile. --ks-pass env:KS_PASS --ks-key-alias $key_alias --key-pass env:KEY_PASS --out app-release-signed.apk -v app-release.apk """
```

>[!NOTE]
>
>Sökvägen till verktyget `apksigner` ser vanligtvis ut så här: ~/Library/Android/sdk/build-tools/30.0.3/apksigner.

**För aab-filen**

>[!NOTE]
>
>Du behöver verktyg för Android SDK för att bygga de signerade binärfilerna.

Play Store kräver Android-binärfiler i aab-format för publicering. Därför tillhandahåller vi den osignerade .aab-filen.

>[!NOTE]
>
>När du skapar en keystore-fil måste du generera ett keystore-lösenord, ett alias för signeringsnyckel och ett lösenord för signeringsnyckel.

Följ proceduren nedan för att signera .aab-filen:

Kör följande kommando:

```
<path>/jarsigner -verbose -sigalg SHA256withRSA -digestalg SHA-256 -keystore <keystore-file> app-release.aab <signingKeyAlias>
```

>[!NOTE]
>
>**[!UICONTROL jarsigner]** ingår i Java. Se till att du använder Java 21.

Ange följande lösenord när du uppmanas till det:

* Keystore-lösenord
* lösenord för signeringsnyckelalias

Du kan använda den medföljande appen. Men om du behöver generera en apk från en aab-fil, följ dessa steg:

>[!NOTE]
>
>Du måste installera **[!UICONTROL bundletool]** för att generera APK:er.


Kör följande kommando för att skapa apk-filen:

```
java -jar <path>/bundletool-all.jar  build-apks --bundle=app-release.aab --output=my_app.apks --mode=universal
```

Packa upp filen med följande kommando:

```
unzip my_app.apks -d output_dir
```

Du hämtar apk-filen från mappen **[!UICONTROL output_dir]**.

**Nästa steg**

När du har genererat binärfilerna överför du dem till Play Store eller App Store.

### Skicka apparna till butiken för granskning

När du har skaffat de sista binärfilerna kan du ladda upp dem till respektive appbutiker (iOS eller Android) för granskning. Följ de här stegen för att överföra binärfilerna till appbutikerna.

**iOS**

1. Logga in på Transporter-appen med dina App Store-inloggningsuppgifter.
2. Välj knappen **+** längst upp till vänster och överför produktionscertifikatet (.ipa-filen).
3. Om .ipa-filen är rätt uppmanas du att överföra appen till App Store.
4. Logga in på App Store när programmet har levererats. Inom några timmar kommer den binära filen att visas i avsnittet TestFlight. Du kan aktivera det för testning av det slutliga hälsotillståndet i TestFlight före appgranskningen och använda detta IPA som det binära när du skickar in appen för en ny version.

**Android**

1. Öppna Google Play Store Console.
2. Gå till **[!UICONTROL Dashboard]** > **[!UICONTROL View App Releases]** > **[!UICONTROL Release Dashboard]** och välj sedan **[!UICONTROL Create New Release]**.
3. Överför den genererade .aab-filen som programpaket och ange versionsinformation, som versionsnummer och nyheter.
4. Spara ändringarna och skicka programmet för granskning.
5. Se till att programdistributionen är 100 % (Google ställer in den på 20 % som standard).

#### Användbara länkar för apppublicering

**Android**

[Skapa och konfigurera appen](https://support.google.com/googleplay/android-developer/answer/9859152?hl=en)
[Förbered programmet för granskning](https://support.google.com/googleplay/android-developer/answer/9859455?sjid=2454409340679630327-AP)

**iOS**

[Skicka för granskning](https://developer.apple.com/help/app-store-connect/manage-submissions-to-app-review/submit-for-review)

## Hur tillämpar jag ändringarna?

Skickar de nödvändiga resurserna och filerna till CSM-teamet. CSM-teamet fyller sedan i [formuläret](https://forms.office.com/r/bJRRaRBvSh) med de ändringar som krävs och bifogar de resurser som krävs. Teamet kommer då att granska och informera teknikerteamen om ändringarna. Teknikteamet kommer sedan att skapa en version och dela den med CSM-teamet.

CSM-teamet delar bygget med kunden.

## Vad kan inte anpassas

* Skärmen Uppdatera lösenord
* Skapa en kontoskärm
