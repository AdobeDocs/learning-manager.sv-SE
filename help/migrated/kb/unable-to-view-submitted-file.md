---
jcr-language: en_us
title: Det går inte att visa filformatet i Adobe Learning Manager
description: Instruktörer kan inte se filer som elever har laddat upp i modulen för inlämningsaktivitet.
contentowner: nluke
exl-id: b4a0af25-14ae-46f1-9afd-0bf2aace7fe2
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 1%

---

# Det går inte att visa filformatet i Adobe Learning Manager

## Problem

En instruktör kan inte se filbidrag som en elev har överfört.

## Beskrivning

Instruktörer kan inte visa filer som elever har överfört i **modulen för inlämningsaktivitet**.

En elev hade till exempel registrerat sig för en instans med namnet **Testinstans** av en kurs, som visas nedan:

![](assets/test-instance.png)

*Visa instans*

Eleven öppnar sedan kursen och laddar upp en fil i modulen Aktivitet.

När instruktören försöker godkänna inskickningen kan instruktören inte göra det.

![](assets/activity.png)

*Ladda upp en fil i aktivitetsmodulen*

## Orsak

Om det inte finns någon instruktör i kursinstansen där eleven är registrerad visas problemet.

## Upplösning

Utför stegen nedan om du vill kontrollera om en instruktör har lagts till i kursinstansen:

1. Gå till kursinställningarna.
1. Klicka på **[!UICONTROL Instances]i avsnittet** Hantera **.**
1. Klicka på **[!UICONTROL Sessions]** i instansen där eleven är registrerad.

   ![](assets/check-instructor.png)

   *Välj sessioner i instansen*

   Ingen instruktör har tilldelats den här sessionen.

1. Klicka på **[!UICONTROL Edit]**. Lägg till den instruktör som godkänner filöverföringen.

   ![](assets/assign-instructor.png)

   *Lägg till instruktören*
1. Spara ändringarna.
