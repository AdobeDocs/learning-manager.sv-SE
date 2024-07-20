---
jcr-language: en_us
title: Modulen är markerad som ofullständig när kursen har slutförts i Adobe Learning Manager
description: Även efter att en elev slutför en kurs i Adobe Learning Manager markeras modulen som ofullständig.
contentowner: nluke
exl-id: c0f14f2e-733a-4b4f-a2c2-4c0b33a15fa1
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# Modulen är markerad som ofullständig när kursen har slutförts i Adobe Learning Manager

## Problem

Även efter att en elev slutför en kurs i Adobe Learning Manager markeras modulen som ofullständig.

## Orsak

SCORM 2004 definierar kriterierna för framgång och slutförande och skickar rapporterna för båda separat.

Låt det till exempel finnas en innehållsuppsättning med **Slutförandekriterier** för 100 % bildvyer och **Kriterier för slutförande** som har angetts som &quot;Quiz godkänns&quot;.

En elev slutför kursen men misslyckas i quiz. I det här fallet är förloppet 100 %, men modulen är markerad som ofullständig eftersom eleven inte uppfyller **framgångsvillkoren**.

## Lösning

Problemet är relaterat till rapporteringen av **Inställningar** för projektet. Författaren måste verifiera de villkor som ställts upp för slutförande och framgång av kursen.

Om det behövs några ändringar kan författaren göra det med ett innehållsredigeringsverktyg som Adobe Captivate Classic. Författaren kan sedan uppdatera modulen.

![](assets/scorm.png)

*Visa rapporteringsinställningar för Captivate Classic*
