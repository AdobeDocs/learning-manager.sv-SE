---
description: Administratörer kan starta en personifierad session där de kan logga in för en annan användares räkning på sitt konto i sin elev- och chefsroll.
jcr-language: en_us
title: Personifiering av elev och chef
contentowner: saghosh
exl-id: 0306f255-283f-43b9-9494-11b3dc3765da
source-git-commit: f44f44ab34acc42edb79d66588ad986d629734ff
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Personifiering av elev och chef {#impersonation-of-learner-and-manager}

I stora organisationer behöver kundsupportpersonalen personifieringsförmåga för att felsöka problem som elever ställs inför.

Med den här möjligheten att uppträda som andra användare kan administratörer identifiera och utföra alla aktiviteter som utförs av elever och chefer i deras organisation.

>[!NOTE]
>
>Anpassade administratörer kan inte uppträda som användare. Det är bara administratörer som kan utföra användarpersonifiering.

## Så här fungerar det

Administratörer kan söka efter en användare (intern eller extern) och sedan uppträda som en användare. Administratören omdirigeras sedan till användarens sida (chefsapp om relevant eller annan elevapp) och loggar sedan ut administratören från sessionen. Administratören omdirigeras sedan till sidan Slutför din profil om detta är inställt för användaren som har personifierats av administratören.

Det här måste du tänka på när du imiterar en användare:

* Alla administratörer ser den här funktionen som standard.
* Endast aktiva användare på kontot kan personifieras.
* En administratör kan inte uppträda som sig själv.
* En anpassad administratör med åtkomst till sidan Användare kan uppträda som användare.
* En administratör/anpassad administratör kan bara personifiera i 60 minuter.
* En anpassad administratör med skrivskyddad åtkomst kan inte uppträda som användare.

## Uppträd som en användare

Om du vill uppträda som en användare följer du stegen nedan:

1. Logga in på programmet som administratör.
1. Välj Profil > Uppträd som användare.

   Du kan bara uppträda som en användare åt gången.

1. Sök efter en användare (intern/extern) i sökrutan som finns i det modala fönstret. Du kan bara uppträda som en användare åt gången. Välj Fortsätt.

   Du kan även söka med användarens e-postadress, UUID och så vidare.

1. Ett meddelande visas med en bekräftelse på att du kommer att uppträda som en användare.

   Välj Fortsätt.

   Ett bekräftelsemeddelande, &quot;Personifieringsläge: Du är inloggad som &quot;användarnamn (användarens e-postadress). Utloggning&quot; visas i sidhuvudet.

**En personifierad session varar i 60 minuter.**

När du byter till en elev eller chefsroll visas ett meddelande om att administratören är i personifieringsläge för användaren.

## Rapport över inloggning och åtkomst

Administratörens inloggning och åtkomst registreras i inloggnings- och åtkomstrapporten. För varje användare som personifieras av administratören skapas en post i rapporten.

Kolumnerna som ingår i funktionen är:

* Uppträder som användarnamn
* Uppträder som användares mejladress

Dessa kolumner läggs till i slutet av rapporten.

Varje inloggning räknas separat i rapporten.

## Vad stöds inte

* Uppträd som AEM-komponenter.
* Personifiering i mobilappen.
* Personifiering i mobilen.
* Personifiering av immersiva appar. Det gäller bara ALM-appar.

## Vanliga frågor

+++Kan jag logga in på Adobe Learning Manager även när jag personifieras?

Ja, inloggningen för en användare är oberoende av personifiering.
+++

+++Räknas impersoneringshändelser unikt?

Ja, varje inloggning/besök av admin medan personifiering räknas separat.
+++

+++Vad är tidsgränsen för personifiering?

Det är 60 minuter. Om en användare som personifierar stänger webbläsarfönstret och sedan navigerar till en primär URL inom 60 minuter fortsätter personifieringsaktiviteten och banderollmeddelandet måste visas.
+++
