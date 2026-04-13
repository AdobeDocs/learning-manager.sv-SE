---
description: Läs mer om metoden för OIDC-inloggning
jcr-language: en_us
title: Logga in på Adobe Learning Manager med OpenID Connect
source-git-commit: 7c430e3fbb2716455310f2130d73af10ce2e56c7
workflow-type: tm+mt
source-wordcount: '1402'
ht-degree: 0%

---


# Logga in på Adobe Learning Manager med OpenID Connect (OIDC)

Lär dig hur OpenID Connect-inloggning fungerar i Adobe Learning Manager för elever, författare och administratörer. I den här artikeln beskrivs upplevelsen, inte implementeringen.

## Förstå inloggning med OpenID Connect

OpenID Connect (OIDC) är en vanlig inloggningsmetod som bygger på webbstandarder. Många organisationer använder en identitetsleverantör (till exempel Okta, Google Workspace eller Microsoft Entra ID) för anställda och partner.

När din organisation aktiverar OIDC för Adobe Learning Manager:

* Du loggar in på organisationens vanliga inloggningssida, inte ett lösenord som bara gäller Adobe Learning Manager, om inte organisationen väljer något annat.
* När du har autentiserat får Adobe Learning Manager den information som organisationen tillåter (t.ex. dina e-postadresser och profilattribut) och öppnar rätt upplevelse för dig: Elev, Författare, Administratör eller andra roller som ditt konto stöder.

OIDC är ett alternativ till andra inloggningsalternativ som ditt konto kan erbjuda, till exempel Adobe ID eller SAML-baserad enkel inloggning (SSO). Din administratör avgör vilka metoder som är tillgängliga.

## Varför organisationer väljer OpenID Connect

Organisationer väljer ofta OIDC eftersom:

* Användarna ser samma identitetsupplevelse för företaget eller molnet som de använder för andra program.
* Lösenordsprinciper, multifaktorautentisering och kontolivscykel hanteras i identitetsleverantören i enlighet med andra företagsappar.
* OIDC följer mönster som liknar andra moderna inloggningsflöden från ett användar- och IT-perspektiv, utan det tyngre dokumentutbyte som är kopplat till vissa konfigurationer med endast SAML.

Upplevelsen är fortfarande densamma: gå till Learning Manager, logga in där din organisation säger åt dig och landa i appen.

## Vad du ser när du loggar in

### Öppna Adobe Learning Manager

Du kan använda:

* Adobe Learning Manager-huvudwebbadressen för din miljö
* En anpassad domän som din organisation har konfigurerat, om en sådan används
* En länk från en e-post-, inbjudan- eller självregistreringssida
* Ett bokmärke eller en djuplänk till en viss kurs, katalogsida eller resurs

Om ditt konto använder OIDC omdirigeras vanligtvis webbläsaren till organisationens identitetsleverantör när du startar inloggningen.

### Logga in med din organisation

Ange dina inloggningsuppgifter på identitetsleverantörens sida och slutför alla extra steg som organisationen behöver, t.ex. multifaktorautentisering. Det här steget utförs utanför Adobe Learning Manager eget inloggningsformulär när OIDC är den metod som används. Från ditt perspektiv känns det som att logga in på ditt företags- eller skolkonto. Du kanske inte ser tekniska termer som *OIDC* eller *OAuth* under det här steget.

### Återgå till Adobe Learning Manager

När du har loggat in kommer webbläsaren tillbaka till Adobe Learning Manager. Produkten:

* Känner igen dig med hjälp av den e-postadress och profilinformation som identitetsleverantören delar enligt organisationens inställningar
* Tillämpar dina behörigheter i Adobe Learning Manager (elev, författare, administratör, integrationsadministratör och så vidare)
* Öppnar lämplig app eller område (till exempel elevupplevelsen jämfört med admin- eller författarupplevelsen), enligt hur Adobe Learning Manager tilldelar roller för ditt konto

Om något går fel (ditt konto har till exempel inte etablerats eller din organisation blockerar åtkomsten) kanske du ser ett fel eller inte kan fortsätta. Kontakta ditt interna IT-team eller din Adobe Learning Manager-administratör.

## Använd andra inloggningsalternativ med OpenID Connect

Adobe Learning Manager kan stödja fler än en inloggningsmetod på ett konto (flera SSO-alternativ). Till exempel:

* Vissa användare loggar in med Adobe ID
* Andra använder SAML SSO
* Andra använder OIDC

Vilka alternativ som visas beror på hur ditt konto är konfigurerat. Att aktivera OIDC för din organisation tar inte automatiskt bort andra metoder om inte dina administratörer ändrar den konfigurationen.

## Funktioner och scenarier som stöds

Följande beteenden stöds när din organisation använder OIDC med Adobe Learning Manager, i enlighet med hur andra företags inloggningsmetoder förväntas fungera.

### Tabell 1. OIDC-stöd i vanliga scenarier

| Område | Vad det innebär för dig |
| --- | --- |
| Interna och externa användare | Anställda och inbjudna externa användare (till exempel partner) kan använda OIDC där din administratör aktiverar det, inklusive flöden som utgår från självregistreringslänkar när ditt konto har konfigurerats för det. |
| Första gången åtkomst | Om du tillåts av policyn kan din första lyckade OIDC-inloggning skapa eller länka din användare i Adobe Learning Manager enligt organisationens regler, på liknande sätt som andra SSO-alternativ. |
| Profil och attribut | Information som e-post och andra attribut kan uppdateras från identitetsleverantören med tiden, så att din Adobe Learning Manager-profil förblir kopplad till organisationens katalog enligt vad administratören konfigurerar. |
| Mörka länkar | Länkar som pekar på en specifik sida eller resurs i Learning Manager (inte bara startsidan) stöds. Du kan landa på det avsedda innehållet efter inloggning när organisationens inställningar tillåter det. |
| Returnera bana | Efter autentiseringen kan du återvända till den plats du försökte nå (till exempel samma kurs- eller katalog-URL som du startade från), i stället för att alltid landa på en allmän startsida. |
| Anpassad domän | Om ditt företag använder ett anpassat värdnamn för Adobe Learning Manager stöds OIDC-inloggning även i det sammanhanget. |
| Mobil | Inloggning på telefoner och surfplattor via webbläsare eller upplevelser som stöds stöds. |
| Publish till Adobe Learning Manager (Prime) | Arbetsflöden som involverar publicering av innehåll till Learning Manager från anslutna verktyg fortsätter att stödjas när ditt konto använder OIDC, i enlighet med din integreringskonfiguration. |
| Identifierarbaserad inloggning | Om ditt konto är beroende av stabila identifierare (utöver enbart e-post) för matchande konton, stöds dessa flöden för OIDC enligt administratörens konfiguration. |

Om ett visst arbetsflöde inte fungerar kan orsaken vara identitetsleverantörens inställningar, kontoetablering eller tilldelning av Adobe Learning Manager-roller. Din administratör kan verifiera det.

## Så här fungerar roller efter inloggning

Adobe Learning Manager avgör vad du kan göra utifrån ditt kontos roller och behörigheter, inte utifrån själva OIDC-protokollet. OIDC fastställer bara vem du är och vad din organisation delar med Adobe Learning Manager.

* Elever ser vanligtvis utbildning, kataloger och utbildningsplaner.
* Författare kan skapa eller välja ut innehåll.
* Administratörer hanterar användare, konfiguration och rapportering.

Om du hamnar på fel ställe eller saknar den åtkomst du förväntar dig kan du be Adobe Learning Manager-administratören att kontrollera din profil och ditt gruppmedlemskap.

## Felsökning av vanliga problem

### Tabell 2. Felsöka OIDC-inloggning

| Problem | Vad du ska prova |
| --- | --- |
| Omdirigeringsslinga eller tom sida | Rensa cookies för din Learning Manager-URL och identitetsleverantör, testa en annan webbläsare eller prova ett privat fönster. Om problemet kvarstår kontaktar du IT. Företagsproxyservrar eller identitetsleverantörens sessionspolicyer stör ibland. |
| &quot;Åtkomst nekad&quot; eller liknande efter identitetsleverantörens inloggning | Din identitetsleverantör godkände dig, men Adobe Learning Manager kanske inte har en matchande användare eller så kanske ditt konto saknar licens eller roll. Kontakta Adobe Learning Manager-administratören. |
| Fel språk eller profilinformation | Attributmappningen styrs av din organisation. Fråga administratören om katalogattribut ska vara drivkraft för språk- eller profilfält. |
| Deep Link öppnade startsidan i stället för resursen | Retursökväg och djuplänksbeteende kan bero på hur länken delades och din session. Prova länken igen efter en fullständig inloggning eller fråga administratören om länkformatet stöds för externa användare. |

## Vad administratörer bör känna till

Om du konfigurerar Adobe Learning Manager för organisationen konfigureras OIDC med identitetsleverantörens programregistrering: klientidentifierare, slutpunkter för auktorisering, token, användarinformation och den omdirigerings-URL som Adobe Learning Manager använder för att slutföra inloggningen. Värdena kommer från identitetsleverantörens dokumentation. Inställningarna måste matcha din identitetsleverantör och Learning Manager så att användarna ser en smidig omdirigering och retur.

Slutanvändarna behöver inte hantera dessa värden. De behöver bara rätt URL till Learning Manager (eller anpassad domän) och, i tillämpliga fall, inbjudan eller självregistreringslänkar från ditt team.

## Sammanfattning

* Med OIDC kan användare logga in på Adobe Learning Manager via organisationens vanliga identitetsleverantör med ett välbekant omdirigerings- och returflöde.
* Efter inloggning använder Adobe Learning Manager e-post och delade attribut för att identifiera användaren och tillämpa roller (elev, författare, administratör och så vidare).
* Självregistrering, flera SSO-alternativ, attributuppdateringar, etablering av användare för första gången, djuplänkar, retursökväg, anpassade domäner, mobil, Publish till Adobe Learning Manager och identifierarbaserad matchning stöds beroende på din kontokonfiguration.
* Andra inloggningsmetoder (som Adobe ID eller SAML) är fortfarande tillgängliga när administratörerna aktiverar dem.
