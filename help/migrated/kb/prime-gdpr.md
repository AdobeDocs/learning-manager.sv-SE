---
jcr-language: en_us
title: Learning Manager-kompatibilitet till GDPR
description: Adobe Learning Manager-efterlevnad av GDPR
contentowner: dvenkate
exl-id: 8ea31464-b4ce-49e8-b471-5630f0216aa4
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 0%

---

# Learning Manager-kompatibilitet till GDPR

>[!IMPORTANT]
>
>Innehållet i detta dokument är inte juridisk rådgivning och är inte avsett att ersätta juridisk rådgivning. Rådgör med ditt företags juridiska avdelning om GDPR.

+++Vad är GDPR?

GDPR är en ny EU-förordning som träder i kraft den 25 maj 2018. Det ger en stark kontroll över dataskyddet och gör det möjligt för slutanvändarna att ta kontroll över sina egna personuppgifter.

+++

+++Hur eller varför gäller det dig som Adobe Learning Manager-kund?

Medan GDPR är en EU-förordning, är den tillämplig på affärsenheter över hela världen, som samlar in personuppgifter för alla användare som kan vara bosatta i EU.  Du som är Learning Manager-kund kan utvärdera om GDPR gäller din organisation.

+++

+++Vilken roll spelar Adobe i detta som leverantör av Learning Manager?

Enligt GDPR betraktas du som [personuppgiftsansvarig](https://gdpr-info.eu/art-24-gdpr/) om ditt företag tillhandahåller en produkt eller tjänst till invånare i EU och bestämmer hur och varför de ska samla in, spåra och övervaka deras data. Om du är Adobe Learning Manager-kund och utför någon av dessa uppgifter betraktas du som personuppgiftsansvarig.

Företag som bearbetar data åt styrenheter anses vara [databehandlare](https://gdpr-info.eu/art-28-gdpr/). Som leverantör av molnlagrade LMS Adobe Learning Manager har Adobe rollen som personuppgiftsbiträde. Här är mer information om [GDPR och ditt företag](https://www.adobe.com/privacy/general-data-protection-regulation.html).

+++

+++Hur gör Learning Manager det möjligt för dig att efterleva GDPR?

Learning Manager har inbyggda verktyg och processer som hjälper dig med GDPR-kompatibilitet. Om du vill ha support för processer som går längre än produkten för att helt uppfylla kraven i förordningen, kan du fortfarande behöva utvärdera det med ditt efterlevnadsteam.

**Rätt att glömma - Datakontrollanten nås:** GDPR kräver att datakontrollanterna stöder funktionen Rätt att glömma för sina användare. Detta innebär att alla användare har rätt att begära att den personuppgiftsansvarige permanent raderar alla personuppgifter som lagras för den användaren. Om du får en sådan begäran och ytterligare utvärderar att det är en giltig begäran tillhandahålls den här funktionen nu i Learning Manager via funktionen [Rensa användare](../administrators/feature-summary/purge-users.md). Med den här funktionen kan administratören initiera en permanent borttagning av data som rör en viss person, på den enskilda personens begäran, vid vilken tidpunkt Learning Manager omedelbart kommer att ta bort data från sin databas och en rensning av säkerhetskopieringsloggarna (avsedda för återställning av systemet) kommer också att följa automatiskt.

**Rätt att glömma - Når personuppgiftsbiträdet:** Slutanvändaren kan också kontakta Adobe oberoende för att ta bort sin PII. I så fall identifierar Learning Manager automatiskt vilka konton som äger PII för den användaren och Adobe meddelar administratören omedelbart om en sådan begäran. Administratören kan sedan utvärdera giltigheten av förfrågan och ta ett samtal om förfrågan via funktionen Rensa användare.

**Rätt till åtkomst:** Med GDPR kan slutanvändaren begära data som en kontrollant kan ha lagrat för den slutanvändaren. För att stödja denna begäran kan Learning Manager låta administratören själv generera elevens betygsutdrag som kan delas med användaren.

**Integritet efter design, datakryptering:** Vi bearbetar data både under överföring och i vila med de bästa krypteringsstandarderna för att säkerställa datasäkerhet. De krypteringsalgoritmer som används är SHA-256. Detta säkerställer att alla data som du lagrar är tillräckligt skyddade så att de inte hamnar i fel händer.

+++
