---
jcr-language: en_us
title: Stöd för anpassad domän
description: Anpassade domäner stöds inte i en Azure-instans av Learning Manager.
contentowner: saghosh
exl-id: 162ce268-48e3-4c7e-acb1-5181cebbb18d
source-git-commit: a09c81a6dacbfc4bb55db39e64820ba87ce53d09
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Stöd för anpassad domän

Anpassade domäner stöds inte i en Azure-instans av Learning Manager.

## Översikt {#overview}

Stöd för anpassade domäner ger kunderna fullständig kontroll över det domännamn som de kan använda för sitt konto i Learning Manager. En kund måste köpa den anpassade domänen separat och arbeta med Adobe-teamet för att ställa in den som sin inloggnings-URL för utbildningsplattformen.

Det gör att kunden kan märka inloggnings- och åtkomstupplevelsen med vita etiketter så att användarna inte ser att det finns någon Adobe eller Adobe Learning Manager.

Du skulle till exempel vilja anpassa din domän så att dina användare får samma upplevelse som om de är på Adobe-domänen. Om ABC Inc vill utbilda sina kunder vill det att de ska landa på en domän som heter `abc.com/mylearning`, i stället för `learningmanager.adobe.com/abc-inc/mylearning`.

>[!NOTE]
>
>En förutsättning är att du registrerar domänen och sedan får du vägledning av Adobe att anpassa webbadressen.


Funktionen Anpassad domän är tillgänglig till en extra kostnad. Kontakta din Customer Success Manager för mer information.

* För elevrollen börjar domänen med `https://cdn.<customer_custom_domain>/` Till exempel `https://cdn.elearningstage1.cpdomaintest.in/`
* För alla andra roller börjar domänen med `https://<customer_custom_domain>/`. Exempel: `https://elearningstage1.cpdomaintest.in/`
* Den faktiska inloggnings-URL:en är `https://<customer_custom_domain>/acapindex` eller `https://<customer_custom_domain>/login`.

>[!NOTE]
>
>Ersätt `<customer_custom_domain>` med organisationens faktiska domän.

## Så här konfigurerar du en anpassad domän på ett konto {#howtosetupacustomdomainonanaccount}

En förutsättning är att kunden äger ett domännamn och köper domänen från en leverantör.

Låt oss till exempel tänka på att en kund äger en fiktiv domän, **acme.com**. Kunden vill att Learning Manager-innehåll ska visas från **learning.acme.com**.

Följ proceduren nedan för att konfigurera en anpassad domän.

1. Kunden måste **lägga till tre CNAME**-poster i domänen:

   * **learning.acme.com:** Offentlig slutpunkt för ALB för Learning Manager som delas av Adobe
   * **lrs.learning.acme.com:** Offentlig ALB-slutpunkt som pekas ut av learning.acme.com
   * **cdn.learning.acme.com:** CDN-slutpunkt delas av Adobe

1. Kunden måste tillhandahålla SSL-certifikat för dessa domäner:

   * learning.acme.com
   * lrs.learning.acme.com
   * cdn.learning.acme.com

1. Adobe kommer att ladda upp dessa SSL-certifikat till AWS ALB för att visa förfrågningar till domänerna.
1. Adobe lägger till learning.acme.com i sitt SAN-certifikat.
1. Adobe kommer att generera SP-metadata för kunden eftersom metadata kommer att innehålla anpassade domäner-URL:er.

   * Om kunden vill logga in på sociala medier måste Adobe inkludera mönster för omdirigerings-URL för de sociala webbplatserna i listan över tillåtna webbadresser.
   * Om kunden har aktiverat enkel inloggning måste kunden arbeta med sin IdP för att inkludera sina domäner i omdirigerings-URL:erna. Kunden måste dela IdP-metadatas-XML med Adobe. Adobe måste sedan uppdatera SSO-inställningarna för kundens konto.

1. Adobe kommer sedan att ändra S3 CORS-reglerna så att de inkluderar kundens domän.
