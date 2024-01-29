---
jcr-language: en_us
title: Learning Manager-integrering med Slack
description: Learning Manager-integrering med Slack
contentowner: dvenkate
source-git-commit: 864b1796f1ca99ae7b5643e8c58d1756ff2461a1
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 0%

---



# Learning Manager-integrering med Slack

Vi har **borttagen** **Slack** som en koppling i Learning Manager. Du har inte längre åtkomst till Slack-anslutningen.

Som användare av Slack kan du installera Adobe Learning Manager-appen från appkatalogen Slack till dina Slack-team och utforska Learning Manager-innehåll direkt från Slack. Du kan interagera med Primebot för att söka efter nya kurser, se rekommendationer och få meddelanden om kommande deadlines i Learning Manager. Du kan också registrera dig och gå direkt till din utbildning inifrån Slack.

Learning Manager-appen för Slack stöds inte i en Azure-instans av Learning Manager.

## Installera Adobe Learning Manager-appen {#installingadobecaptivateprimeapp}

En elev kan installera appen CP Prime i sitt Slack-konto. Installera programmet genom att öppna programkatalogen i ditt Slack-konto och söka efter Learning Manager. Hämta och installera programmet. Om programmet inte godkänns på ditt konto kontaktar du din integreringsadministratör för godkännande. Om det redan har godkänts kan du logga in.

## Godkänna elevinloggning som integrationsadministratör {#approvinglearnersigninasanintegrationadmin}

Följ de här stegen som integrationsadministratör för att godkänna behörigheten för en elev att använda Prime-programmet på Slack.

1. Välj **[!UICONTROL Applications]** i den vänstra rutan och klicka på **[!UICONTROL Featured apps]** -fliken.

   ![](assets/featuredapps.jpg)

1. Klicka på **[!UICONTROL Slack]** panel > sidan Slack-integrering öppnas. Klicka **[!UICONTROL Approve]** i det övre högra hörnet för att godkänna programmet.

   ![](assets/approval.png)

1. Gå tillbaka till **[!UICONTROL Applications]** sidan. När Slack har godkänts ska det upptas i **[!UICONTROL External Apps]** -fliken.
1. Elever kan nu logga in på sitt primära konto med hjälp av Slack.

## Primebot-funktioner {#primebotfunctionalities}

Du kan nu börja interagera med Primeboten. Här är funktionerna i roboten.

1 - Kommando

&#42;/prime&#42; kan användas för engångsfrågor som rör ditt Adobe Learning Manager-konto.

Följande underkommandon finns:

/prime find `<query>` - söka efter kurser, certifieringar etc.

/prime rekommenderar - visa rekommendationer

/prime deadlines - visa försenade och kommande deadlines

/prime-registreringar - visa registreringar

/prime-färdigheter - visa färdigheter

/prime notifications - visa meddelanden

/prime-kataloger - visa kataloger

/prime bjud in - [Endast administratör] bjud in Slack-användare i det nuvarande teamet att testa primebot

/prime profile- visa profil

/prime logga ut - logga ut från ditt Prime-konto i det här Slack-teamet

/prime help - visa hjälpmeddelande

2 - Rekommendera

Du kan prova en fras som `show my recommendations` för att få en personlig lista över rekommenderade kurser, certifieringar och utbildningsprogram från ditt Adobe Learning Manager-konto.

3 - Sökning

Du kan prova fraser som `search for machine learning` eller `search for artificial intelligence`. Du kan ange typen av utbildningsobjekt med fraser som `search for machine learning certifications`, `search for artificial intelligence courses` eller `search for adobe photoshop job aids`. Du kan också söka i en katalog med fraser som `search for machine learning in Lynda catalog`.

4 - Tidsfrister

Använd fras som `show my deadlines` för att få en lista över försenade och kommande deadlines från ditt Adobe Learning Manager-konto. Du kan filtrera bort försenade eller kommande deadlines med fraser som `show my overdue deadlines` eller `show my upcoming deadlines`.
