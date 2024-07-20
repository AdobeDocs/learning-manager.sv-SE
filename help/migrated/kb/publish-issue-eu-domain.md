---
jcr-language: en_us
title: Det gick inte att publicera till EU-domänen för Learning Manager
description: Det går inte att publicera från Adobe Captivate till Adobe Learning Manager-domänen i Adobe Learning Manager.
contentowner: nluke
exl-id: fb8ae1af-9902-4901-8263-fb3ebff98fbc
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# Det gick inte att publicera till EU-domänen för Learning Manager {#unable-to-publish-to-learning-manager-eu-domain}

## Problem

Det gick inte att publicera från Adobe Captivate till Adobe Learning Manager-domänen.

## Fel

Inga konton hittades

## Beskrivning

Det finns scenarier där författare försöker publicera en kurs från Adobe Captivate till Adobe Learning Manager. De kan dock inte göra det eftersom de får felmeddelandet &quot;Inget konto hittades&quot;.

## Orsak

Det här problemet uppstår eftersom Adobe Captivate som standard är konfigurerat för att publicera innehåll till den amerikanska domänen Adobe Learning Manager.

## Upplösning:

Saker att notera:

* Stäng Adobe Captivate-programmet om det är öppet.
* Du behöver administratörsåtkomst på datorn för att utföra stegen nedan. Om du inte har administratörsåtkomst kontaktar du IT-teamet och får hjälp.

Utför stegen nedan:

1. Gå till installationkatalogen för Adobe Captivate.

   Till exempel är `kbd C:\\Program Files\\Adobe\\Adobe Captivate 2019 x64` (2019 Captivate. (Detta skiljer sig om du använder en annan version av Adobe Captivate).

1. Kopiera konfigurationsfilen **AdobeCaptivate.ini** till skrivbordet.

   ![](assets/cp-captivate.ini.png)
   *Visa konfigurationsfilen*

1. Öppna den kopierade filen från skrivbordet till en Anteckningar.
1. Ändra värdet för LearningManagerBaseUrl = `https://learningmanager.adobe.com/inappstarter` till LearningManagerBaseUrl = `https://learningmanagereu.adobe.com/inappstarter`

   ![](assets/cp-primebaseurl.png)
   *Visa PrimeBaseURL*

1. Spara ändringar som gjorts i Anteckningar.
1. Kopiera den sparade filen som du redigerade och klistra in den på filsökvägen. Ersätt originalfilen i `kbd C:\\Program Files\\Adobe\\Adobe Captivate 2019 x64`
1. När du är klar startar du Adobe Captivate och försöker publicera till Adobe Learning Manager.
