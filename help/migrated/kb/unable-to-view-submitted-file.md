---
jcr-language: en_us
title: Det går inte att visa filformatet i Adobe Learning Manager
description: Instruktörer kan inte se filer som elever har laddat upp i modulen för inlämningsaktivitet.
contentowner: nluke
source-git-commit: 8b29ac996962e7ce8fbda51f3421c9a5f248fcf6
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 1%

---



# Det går inte att visa filformatet i Adobe Learning Manager

## Problem

En instruktör kan inte se filbidrag som en elev har överfört.

## Beskrivning

Instruktörer kan inte se filer som elever har laddat upp i **Modul för inlämningsaktivitet**.

En elev hade till exempel registrerat sig för en instans med namnet **Testinstans** i en kurs, enligt nedan:

![](assets/test-instance.png)

*Visa instans*

Eleven öppnar sedan kursen och laddar upp en fil i modulen Aktivitet.

När instruktören försöker godkänna inskickningen kan instruktören inte göra det.

![](assets/activity.png)

*Ladda upp en fil i modulen Aktivitet*

## Orsak

Om det inte finns någon instruktör i kursinstansen där eleven är registrerad visas problemet.

## Upplösning

Utför stegen nedan om du vill kontrollera om en instruktör har lagts till i kursinstansen:

1. Gå till kursinställningarna.
1. I dialogrutan **Hantera** avsnitt, klicka på **[!UICONTROL Instances].**
1. I instansen där eleven är registrerad klickar du på **[!UICONTROL Sessions]**.

   ![](assets/check-instructor.png)

   *Välj Sessioner i instansen*

   Ingen instruktör har tilldelats den här sessionen.

1. Klicka på **[!UICONTROL Edit]**. Lägg till den instruktör som godkänner filöverföringen.

   ![](assets/assign-instructor.png)

   *Lägg till instruktören*
1. Spara ändringarna.

