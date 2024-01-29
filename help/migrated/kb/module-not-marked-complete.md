---
jcr-language: en_us
title: Modulen är markerad som ofullständig när kursen har slutförts i Adobe Learning Manager
description: Även efter att en elev slutför en kurs i Adobe Learning Manager markeras modulen som ofullständig.
contentowner: nluke
source-git-commit: ec79aa3dd6225cc424721afb50702963c1b125eb
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---



# Modulen är markerad som ofullständig när kursen har slutförts i Adobe Learning Manager

## Problem

Även efter att en elev slutför en kurs i Adobe Learning Manager markeras modulen som ofullständig.

## Orsak

SCORM 2004 definierar kriterierna för framgång och slutförande och skickar rapporterna för båda separat.

Låt det till exempel finnas en innehållsuppsättning med en **Kriterier för slutförande** av 100 % bildvyer och **Kriterier för slutförande** anges som &quot;Quiz har godkänts&quot;.

En elev slutför kursen men misslyckas i quiz. I det här fallet är förloppet 100 %, men modulen är markerad som ofullständig eftersom eleven inte uppfyller **Kriterier för slutförande**.

## Lösning

Frågan gäller rapporteringen **Inställningar** för projektet. Författaren måste verifiera de villkor som ställts upp för slutförande och framgång av kursen.

Om det behövs några ändringar kan författaren göra det med ett innehållsredigeringsverktyg som Adobe Captivate Classic. Författaren kan sedan uppdatera modulen.

![](assets/scorm.png)

*Visa rapporteringsinställningar för Captivate Classic*
