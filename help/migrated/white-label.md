---
jcr-language: en_us
title: Vit märkning i mobilappen Adobe Learning Manager
description: Vit märkning är en metod att byta namn på en app eller tjänst med ditt eget varumärke och anpassa den som om du vore den ursprungliga skaparen. I Adobe Learning Manager kan du använda vit etikettering i mobilappen så att du kan byta varumärke på appen och göra den tillgänglig för dina användare under ditt eget varumärke.
contentowner: saghosh
exl-id: f37c86e6-d4e3-4095-9e9d-7a5cd0d45e43
source-git-commit: 8fe01ca3c0e11d5d62645f4fa7695fce504e0da2
workflow-type: tm+mt
source-wordcount: '1051'
ht-degree: 0%

---

# Vit märkning i mobilappen Adobe Learning Manager

Mobilappen Adobe Learning Manager har nu stöd för vit märkning, vilket innebär att du nu kan släppa appen under ditt eget varumärke.

## Hur du ska börja förbereda för att starta ett program med vit etikett

Gör så här för att distribuera och hantera ditt eget program med vita etiketter:

1. Förbered resurserna (t.ex. en välkomstbild) och texten så att båda kan användas i appen och beskrivningen i app/play-butiken.

1. Tilldela en teknisk resurs som kan:

* Genererar certifikatfiler för push-meddelanden.
* Signera programmets binärfiler som tillhandahålls av ALM-teamet.
* Ladda upp och hantera publiceringsprocessen. Publiceringsprocessen kräver kommunikation mellan apphanteraren och app/play store-team om att din app följer alla publiceringsriktlinjer. Från ALM får du en helt kompatibel app binär.

## Översikt

Vit märkning är en metod att byta namn på en app eller tjänst med ditt eget varumärke och anpassa den som om du vore den ursprungliga skaparen. I Adobe Learning Manager kan du använda vit etikettering i mobilappen så att du kan byta varumärke på appen och göra den tillgänglig för dina användare under ditt eget varumärke.

## Vad kan anpassas

Du kan anpassa följande:

### Fält

<table>

    <tbody>

    <tr>

   <td>

    <p>Konto-ID</p></td>

   <td>

    <p>ID för ditt konto. Observera att det vitmärkta programmet inte är tillgängligt för elever som tillhör något annat konto.</p></td>

  </tr>

  <tr>

   <td>

    <p>Ytterligare konto-ID</p></td>

   <td>

    <p>Lägg till flera konton (underdomäner) om du vill. Lägg till underdomänerna som kommaavgränsade utan mellanslag. Till exempel acc01,acc02,acc03 och så vidare.<br> <b>Obs!</b> Du måste lägga till konto-ID när du anger underdomänerna.</br> </p></td>

  </tr>

  <tr>

  <td>

  <p>Programnamn</p></td>

  <td>

  <p>Namnet som du vill använda för appen.</p></td>

  </tr>

  <tr>

  <td>

  <p>Kortnamn för app</p></td>

  <td>

  <p>I fall där namnet på appen är långt ska du ge den ett kort namn som visas på enheten.</p></td>

  </tr>

   <tr>

  <td>

  <p>Internt programnamn</p></td>

  <td>

  <p>Namnet som operativsystemet identifierar programmet med. Det format som vanligtvis används är: com.company-name.product-name.</p></td>

  </tr>

  <tr>

  <td>

  <p>Internt programnamn - iOS</p></td>

  <td>

  <p>Namnge programmet på ett annat sätt om användarna använder iOS. Vi rekommenderar att du använder samma namn för både iOS och Android.</p></td>

  </tr>

  <tr>

  <td>

  <p>Appikon</p></td>

  <td>

  <p>Appikonen som png. Den här ikonen visas i ditt program. Formatet som ska namnges är account-id_appIcon.png.</p></td>

  </tr>

  <tr>

  <td>

  <p>Appstartskärm</p></td>

  <td>

  <p>Ange en bild (png) som visas när användarna startar programmet på programmets välkomstskärm. Formatet som ska namnges är account-id_splashIcon.png.</p></td>

  </tr>

  <tr>

  <td>

  <p>Klient-ID och Klienthemlighet</p></td>

  <td>

  <p>Integreringsadministratören för ditt konto tillhandahåller informationen medan du registrerar programmet. Integreringsadministratören måste använda följande: * elev:läs,elev:skriv som roll * internt program name://redirect som omdirigerings-URL

  </p></td>

  </tr>

  <tr>

  <td>

  <p>Kontologotyp</p></td>

  <td>

  <p>Den URL som är värd för organisationens logotyp. Ange en cpcontent-länk som kontologotyp. Webbadressen måste vara webbkodad.</p></td>

  </tr>

  <tr>

  <td>

  <p>Appbutikens ID för appen (iOS)</p></td>

  <td>

  <p>Det ID som krävs för att implementera force-uppdateringen. Appen måste veta att eleven ska omdirigeras till appbutiken för att uppdatera appen.</p></td>

  </tr>

   <tr>

  <td>

  <p>Google Play Store-id för appen (Android)</p></td>

  <td>

  <p>Det ID som krävs för att implementera force-uppdateringen.</p></td>

  </tr>

  <tr>

  <td>

  <p>Värdnamn för djuplänkning</p></td>

  <td>

  <p>Använd Learning Manager om du vill vara värd för dina djuplänkar. Om du vill använda ett annat värdnamn som en djuplänk anger du värddatorns URL. Exempel: learningmanager.adobe.com.</p></td>

  </tr>

    </tbody>

</table>


#### Uppdatera webbplatsassociation

Om du använder en anpassad domän eller Learning Manager\*.adobe.com som värd behöver du inte vidta några åtgärder. Men om du använder en anpassad lösning eller ett specifikt värdnamn för webbadresserna ska du lägga till platsassociationsfilerna.

Mer information finns på följande länkar:

- [Android](https://learningmanager.adobe.com/.well-known/assetlinks.json)

- [iOS](https://learningmanager.adobe.com/.well-known/apple-app-site-association)

## Generera certifikat för push-meddelanden

### Certifikat för push-meddelanden i iOS

Ett push-meddelandecertifikat är en kryptografisk autentiseringsuppgift inom iOS-apputveckling som utfärdas av Apple och som gör det möjligt för en server att på ett säkert sätt skicka push-meddelanden till en iOS-enhet via Apple Push Notification Service (APN:er).

Certifikatet garanterar säker kommunikation mellan servern (eller leverantören) och Apple APN-filer när push-meddelanden skickas till iOS-enheter.

Både Android och iOS använder Firebase Cloud Messaging (FCM) som tjänst för att skicka push-meddelanden till enheter.

### Så här genererar du certifikatet i iOS

Följ proceduren:

1. Generera eller hämta **Certifikat för push-meddelanden** och privat nyckel (.p12). Mer information finns i [Utvecklardokument för Apple](https://developer.apple.com/documentation/usernotifications/setting_up_a_remote_notification_server/establishing_a_certificate-based_connection_to_apns).

1. Installera p12-filen när filen har hämtats. Använd lösenordet för att installera i **Åtkomst till nyckelringen**.

1. Gå till **Mina certifikat** och exportera certifikatet. Se till att du väljer MIME-typen .cer.

1. Kör följande kommandon när du har p12-filen och CER-filen tillgängliga:

```
- openssl pkcs12 -in privatekey.p12 -out myapnappkey.pem -nodes –clcerts

- openssl x509 -in privatekey.cer -inform DER -out myapnsappcert.pem 

- openssl s_client -connect gateway.sandbox.push.apple.com:2195 -cert myapnsappcert.pem -key myapnappkey.pem 
```

Om du kan ansluta till servern är certifikatet du har skapat giltigt. Kopiera certifikatet och värdena för den privata nyckeln från filen myapnappkey.pem.

1. Kontakta CSM-teamet och få filerna tillagda i SNS-tjänsterna på AWS. Användare måste få posten registrerad i SNS-tjänsten för push-meddelandet, vilket kräver att de delar certifikaten som genereras ovan för validering.

>[!NOTE]
>
>För Android måste användaren ange servernyckeln från det Firebase-projekt som de skapar för Android för att lägga till posten i SNS-tjänsten.


## Lägg till projektet i Firebase

### Android

[Lägg till projektet](https://learn.microsoft.com/en-us/xamarin/android/data-cloud/google-messaging/firebase-cloud-messaging) i Firebase och hämta ***google-services.json*** fil.

### iOS

[Lägg till projektet](https://firebase.google.com/docs/ios/setup) till Firebase och hämta ***GoogleService-Info.plist*** fil.

## Generera signerade binärfiler

### iOS

```
sh""" xcodebuild -exportArchive -archivePath ./mobile-app-embedding-immersive/build/ios/archive/Runner.xcarchive -exportPath "ipa_path/" -exportOptionsPlist ./deviceAppBuildScripts/${ExportFile} 

mv ipa_path/*.ipa "${env.AppName}_signed.ipa" """ 
```

>[!NOTE]
>
>Du behöver XCode 14.2 eller senare för att skapa de signerade binärfilerna.


## Android

```
sh""" ~/Library/Android/sdk/build-tools/30.0.3/apksigner sign --ks $storeFile --ks-pass "pass:$store\_password" --ks-key-alias $key\_alias --key-pass "pass:$key\_password" --out app-release-signed.apk -v app-release.apk """
```

>[!NOTE]
>
>Du behöver verktyg för Android SDK för att bygga de signerade binärfilerna.

**Nästa steg**

När du har genererat binärfilerna överför du dem till Play Store eller App Store.

## Hur tillämpar jag ändringarna?

Skickar de nödvändiga resurserna och filerna till CSM-teamet. CSM-teamet fyller sedan i [form](https://forms.office.com/r/bJRRaRBvSh) har gjort de ändringar som krävs och bifogar de mediefiler som krävs. Teamet kommer då att granska och informera teknikerteamen om ändringarna. Teknikteamet kommer sedan att skapa en version och dela den med CSM-teamet.

CSM-teamet delar bygget med kunden.

## Vad kan inte anpassas

- Skärmen Uppdatera lösenord
- Skapa en kontoskärm
