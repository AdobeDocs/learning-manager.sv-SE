---
jcr-language: en_us
title: Inloggningsproblem i Learning Manager
description: Inloggningsproblem i Adobe Learning Manager
contentowner: nluke
source-git-commit: ec79aa3dd6225cc424721afb50702963c1b125eb
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---



# Inloggningsproblem i Learning Manager

## Problem

Det gick inte att logga in på Adobe Learning Manager.

## Fel

När du försöker logga in på Adobe Learning Manager visas felmeddelandet nedan:

![](assets/cp-error.png)

*Felmeddelande för en session som har upphört*

## Orsak

När en användare loggar in via SSO skapas en sessionscookie som lagras i webbläsaren. Det gör också att användaren kan logga in på andra program. De flesta enkel inloggning (SSO) är konfigurerade att logga ut efter 24 timmar. Användaren måste autentisera sig igen för en ny session.

I vissa fall kan inte en användare komma åt systemet på grund av gamla SSO-cookies. Dessa cookies vidarebefordras till Adobe Learning Manager för autentisering. Sessionen avslutas inte om användaren inte stänger webbläsaren på länge eller inte har loggat ut.

Adobe Learning Manager avvisar dessa gamla cookies, vilket resulterar i ett fel.

## Upplösning

Prova följande alternativ om en inaktuell cookie avvisas av Adobe Learning Manager:

1. Rensa webbläsarens cookies och cacheminne. Mer information finns i [dokument](unable-log-in-learning-manager.md).

   Alternativt kan IdP-administratören definiera en forcerad utloggning efter en viss angiven tid. Det här steget autentiserar användaren igen för att starta en ny session.

Det finns andra skäl till varför detta fel uppstår, men det ovan nämnda är ett vanligt scenario.

## Referenslänkar:

[Microsoft: session med villkorsstyrd åtkomst under en livstid](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/howto-conditional-access-session-lifetime)
