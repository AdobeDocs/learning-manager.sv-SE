---
jcr-language: en_us
title: Det gick inte att söka efter en kurs i Learning Manager
description: En elev kan inte söka en kurs i Learning Manager.
contentowner: nluke
exl-id: 702aacb7-a0b9-48fb-8a3d-425bfea63f65
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 1%

---

# Det gick inte att söka efter en kurs i Learning Manager

## Problem

En elev kan inte söka en kurs i Learning Manager.

## Scenario 1: Registrering sker via ett högre utbildningsobjekt

### Sammanfattning

Det finns scenarier där en elev söker igenom en kurs och kursen inte är listad. Men om eleven har registrerat sig för ett utbildningsprogram/en certifiering kan eleven se kursen inuti utbildningsobjektet.

### Varför händer detta?

I Learning Manager, när en elev registreras genom ett utbildningsprogram/en certifiering, sker registreringen för den kursen via utbildningsprogrammet/certifieringen.

Därför kan eleven inte söka efter de fristående kurserna under **Min utbildning**.

Eleven kan dock inte se kurserna i utbildningsprogrammet/certifieringen.

## Scenario 2: Eleven har inte tillgång till katalogen som innehåller kursen.

### Sammanfattning

En elev kan inte söka kurser i katalogen eller instrumentpanelen för utbildning.

### Varför händer detta?

Problemet uppstår om:

* Eleven är inte en del av katalogen som innehåller kursen **ELLER**
* Kursen är inte en del av katalogen som eleven har tillgång till.

### Upplösning

1. Logga in som administratör.

1. Klicka på **[!UICONTROL Catalog]** och bläddra till katalogen som innehåller kursen.
1. Klicka på **[!UICONTROL Share Internally]** eller **[!UICONTROL Content]** (beroende på scenariot ovan).

   ![](assets/cp-share-internally.png)

   *Dela katalogen internt*

1. Granska scenarierna nedan:

   * Eleven är inte en del av katalogen

     Om du vill dela katalogen klickar du på **[!UICONTROL Add]** och lägger till användargruppen som användaren ingår i. Klicka på **[!UICONTROL Save]**.

     ![](assets/cp-add-user-group.png)

     *Lägg till användargruppen*

   * Kursen ingår inte i katalogen

     Klicka på **[!UICONTROL Add Content]** i avsnittet Innehåll och välj kursen som du vill lägga till i katalogen.

     ![](assets/cp-add-content.png)

     *Lägg till innehåll i kursen*
