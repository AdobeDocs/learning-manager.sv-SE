---
jcr-language: en_us
title: Automatiska popup-fönster för L1-feedback visas inte
description: Så här löser du felet "L1-feedback automatisk popup visas inte"
contentowner: saghosh
source-git-commit: ec79aa3dd6225cc424721afb50702963c1b125eb
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---



# Automatiska popup-fönster för L1-feedback visas inte

## Problem

Den automatiska popup-menyn för L1-feedback visas inte för en elev efter att ha slutfört kursen.

## Orsak

Ibland kan det hända att en elev inte får L1-feedback efter att ha slutfört en viss kurs eller får ett meddelande enligt nedan:

![](assets/l1-feedback.png)

*Det går inte att ta emot feedback om L1*

Detta kan bero på följande:

1. Feedback har inte ställts in för att visas efter slutförande av kursen.
1. Påminnelser har inaktiverats.
1. En påminnelse är schemalagd att visas efter en viss tid.

## Upplösning

1. Se till att alternativet &quot;Visa frågeformuläret omedelbart efter att kursen har slutförts&quot; är aktiverat i **Kurs** > **Instanser** > **Feedback om L1**.
   <!--![](assets/l1-feedback.png)-->
1. Som administratör går du till **Inställningar > Feedback**. Kontrollera när påminnelsen har schemalagts. Om det är inplanerat **Efter kurs** slutförande, ändra alternativet till **På kurs** slutförande.
1. Aktivera följande e-postmallar: **E-postmallar > Påminnelser och uppdateringar > Be eleven om feedback på kursen**. Om alternativet är inaktiverat ska du aktivera det och sedan testa.
1. Om stegen ovan inte fungerar tar du bort påminnelsen i **Admin > Inställningar > Feedback**. Skapa ett för Vid slutförande av kurs och ställ in upprepningen enligt kravet.
