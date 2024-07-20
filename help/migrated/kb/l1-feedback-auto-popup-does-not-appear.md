---
jcr-language: en_us
title: Automatiska popup-fönster för L1-feedback visas inte
description: Så här löser du felet "L1-feedback automatisk popup visas inte"
contentowner: saghosh
exl-id: 47edcd7f-e332-4a75-a025-fd07737d0b70
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
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

1. Se till att alternativet Visa frågeformuläret omedelbart efter att kursen har slutförts är aktiverat i **Kurs** > **Instanser** > **L1-feedback**.
   <!--![](assets/l1-feedback.png)-->
1. Som administratör går du till **Inställningar > Feedback**. Kontrollera när påminnelsen har schemalagts. Om det är schemalagt till **Efter att kursen** har slutförts ändrar du alternativet till **På kurs** slutförande.
1. Aktivera följande e-postmallar: **E-postmallar > Påminnelser och uppdateringar > Begär feedback från elev för kurs**. Om alternativet är inaktiverat ska du aktivera det och sedan testa.
1. Om stegen ovan inte fungerar tar du bort påminnelsen i **Admin > Inställningar > Feedback**. Skapa ett för Vid slutförande av kurs och ställ in upprepningen enligt kravet.
