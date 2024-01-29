---
jcr-language: en_us
title: Det går inte att visa vissa kurser under katalogen när en certifiering skapas
description: När du söker efter en viss kurs för att lägga till den i en certifiering kan du inte visa kursen under katalogen.
contentowner: saghosh
source-git-commit: 864b1796f1ca99ae7b5643e8c58d1756ff2461a1
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---



# Det går inte att visa vissa kurser under katalogen när en certifiering skapas

## Problem

När du söker efter en viss kurs för att lägga till den i en certifiering kan du inte visa kursen under katalogen.

## Registreringstyper

Det finns tre registreringstyper i Learning Manager:

* Egenregistrerad
* Nominerad från chef
* Godkänt av chef

## Egenregistrerad

Elever kan direkt registrera sig för denna typ av kurser.

## Godkänt av chef

Dessa kurser måste godkännas av chefer. Elever kan registrera sig för dessa kurser, men de registreras inte direkt till denna typ av kurser utan chefens godkännande. En aviseringsbegäran skickas till chefer när elever registrerar sig för dessa typer av kurser. Efter chefens godkännande kommer dessa kurser att listas som registrerade för elever.

## Nominerad från chef

Dessa kurser kan endast nomineras av chefer. En elev kan inte registrera sig för dessa typer av kurser.

## Nästa steg

I en certifiering kan du bara lägga till egenregistrerade kurser och inte chefsnominerade eller chefsgodkända kurser.

* **Permanent certifiering:**  Du kan lägga till en CR- eller VC-sessionskurs i en certifiering.
* **Återkommande certifieringar:** Du kan inte lägga till någon CR- eller VC-sessionskurs i en certifiering.

Detta är ett standardbeteende i Learning Manager.
