---
jcr-language: en_us
title: xAPI i Learning Manager
description: Experience API (xAPI) är en programspecifikation för e-utbildning som gör att utbildningsinnehåll och utbildningssystem kan kommunicera med varandra på ett sätt som registrerar och spårar alla typer av utbildningsupplevelser.
exl-id: 8e36b538-a451-448e-a65d-08d286adcfdb
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 0%

---

# xAPI i Learning Manager

## Vad är xAPI? {#whatisxapi}

Experience API (xAPI) är en programspecifikation för e-utbildning som gör att utbildningsinnehåll och utbildningssystem kan kommunicera med varandra på ett sätt som registrerar och spårar alla typer av utbildningsupplevelser. Utbildningsupplevelser registreras i en utbildningspostbutik (LRS). LRS kan finnas inom traditionella system för hantering av inlärning eller på egen hand.

Mer information om xAPI finns på: [https://github.com/adlnet/xAPI-Spec](https://github.com/adlnet/xAPI-Spec).

## Hur stöder Learning Manager xAPI? {#howdoescaptivateprimesupportxapi}

Learning Manager har en inbyggd utbildningspostbutik. Denna LRS har full kapacitet att acceptera xAPI-satser från innehåll som har lagrats i Learning Manager. Den accepterar till och med xAPI-satser som genereras av tredje part. Dessa xAPI-satser lagras i Learning Manager och de kan sedan exporteras utanför Learning Manager för att visualiseras till ett datalagringssystem från tredje part.

## När använder du xAPI? {#whendoyouusexapi}

I allt högre grad finns ett behov av att samla slutanvändarens utbildningsupplevelser som spänner över flera system.  Det finns också ett behov av att spåra elevens exakta engagemang med utbildningsinnehåll. Det går bortom Start, Pågår och Slutförande (som är de enda attribut som registreras av SCORM).

## Använda xAPI i Learning Manager {#usingxapiinprime}

## Konfigurera ditt program {#setupyourapplication}

1. Logga in som integreringsadministratör. Välj **[!UICONTROL Applications]** > **[!UICONTROL Register]**.

   ![](assets/appregistration.png)

1. Registrera en ny ansökan.

   ![](assets/appregistration.png)

1. Definiera programmets omfattning.

   * Om **[!UICONTROL Admin role xAPI read and write access]** är aktiverat kan administratören publicera och hämta xAPI-satser och -dokument.
   * Om **[!UICONTROL Learner role xAPI read and write access]** är aktiverat kan administratören publicera och hämta xAPI-satser och -dokument.

1. Spara ändringarna. Du får ditt utvecklar-id och din hemlighet.

**Slutpunkter**:

Klicka på länken nedan för att visa swagger-dokumentet för xAPI:

[https://learningmanagereu.adobe.com/docs/primeapi/xapi/](https://learningmanagereu.adobe.com/docs/primeapi/xapi/)

Obs! Den version av xAPI som stöds i Learning Manager är 1.0.3.

## API-autentisering {#apiauthentication}

Learning Manager xAPI använder OAuth 2.0 Framework för att autentisera och auktorisera dina klientprogram. När du har registrerat programmet kan du hämta clientId och clientSecret. Hämta URL används i webbläsare eftersom den autentiserar Learning Manager-användare med deras förkonfigurerade konton, som SSO och Adobe ID.

```
GET https://learningmanager.adobe.com/oauth/o/authorize?client_id=<Enter your clientId>&redirect_uri=<Enter a url to redirect to>&state=<Any String data>&scope=<admin:xapi or learner:xapi>&response_type=CODE.
```

## Spåra xAPI-satser som Learning Manager LO {#trackingxapistatementsasprimelo}

Som författare kan du nu välja xAPI-modul när du skapar kurser för att övervaka användarupplevelsen utanför Learning Manager. Du kan till exempel använda den här funktionen för att utvärdera aktiviteter för användare på en tredjepartsplattform som används för kursförbrukning.

1. När du skapar en **[!UICONTROL Activity Module]** använder du snabbmenyn för att välja **[!UICONTROL xAPI-based Module.]** i **&lbrace;1**&#x200B;alternativet[!UICONTROL Type]

   ![](assets/xapimodulecreation.png)

1. Du ombeds att ange en IRI. Om alternativet inte anges genererar Learning Manager ett automatiskt.

   IRI för en aktivitet är unik för ett konto. Det innebär att två moduler i Learning Manager inte kan ha samma IRI. En ny IRI genereras i följande fall:

   * När en kurs med xAPI-modulen delas mellan konton.
   * När en certifiering med xAPI-modulen återkommer



   Alla xAPI-satser med den nämnda IRI spåras i modulen ovan och återspeglas i Learning Manager-rapporterna.

1. Gå tillbaka till sidan Aktivitetsmodul om du vill kopiera den automatiskt genererade IRI.
1. Publish modulen.

**Viktiga saker att observera:**

* Learning Manager har för närvarande bara stöd för mbox som identifierare. Andra identifierare, inklusive mboz_sha1, openid, account stöds inte.

* StateId och profileId är ett UUID när de används med Learning Manager.
* PUT-begäran skriver inte över dokumentet för xAPI-agenter/profil, aktivitet/profil och aktivitet/tillstånd
* Oidentifierad grupp stöds inte i Actor.
* Parametern related_activities stöds inte i instruktionen GET.
* Parametrarna format=ids och format=canonical stöds inte i GET-satser.
* När xAPI-instruktionen annulleras ångras inte några åtgärder som inträffade i Learning Manager när utdraget bokfördes.

## Generera rapporter {#generatereports}

xAPI-rapporter kan genereras som Excel-rapporter. Öppna **[!UICONTROL Reports]** > **[!UICONTROL Excel reports]** > **[!UICONTROL xAPI activity report]** som administratör.

Den nedladdade rapporten hämtar all information som publicerats av eleven och administratören för ett kontoutdrag.

Samma rapporter kan genereras/schemaläggas med FTP- och Box-anslutningar för alla tredjepartsintegreringar. Gör så här:

Logga in som Integreringsadministratör > Öppna FTP-/Box-anslutning > Välj xAPI-aktivitetsrapport i den vänstra rutan> Välj om du vill schemalägga/generera en rapport.

![](assets/xapischedule.png)

* När endast Raw-poäng skickas i xAPI-instruktion utan maxpoäng visas quiz-poäng inte i LT.

* För att få procentpoängen i Learning Manager skickas skalade poäng via xAPI.

## Exempelrapport {#samplereport}

[Exempel på xAPI-rapport.](assets/xapireport8842560559890766717csv.zip)
