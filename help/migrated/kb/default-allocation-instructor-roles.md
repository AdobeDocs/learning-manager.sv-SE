---
jcr-language: en_us
title: Standardtilldelning av instruktörsroller till användargrupper i Learning Manager
description: Standardtilldelning av instruktörsroller till användargrupper i Learning Manager
contentowner: nluke
preview: true
source-git-commit: 66dfaaaf723382eada39e2be29dfd49b795107a0
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---



# Standardtilldelning av instruktörsroller till användargrupper i Learning Manager

## Problem

Alla användare som tilldelas en session tilldelas rollen instruktör.

## Beskrivning

Det finns scenarier där en session kan kräva flera instruktörer, eller där en administratör/författare tilldelar en användargrupp en session. Detta leder till att alla användare i användargruppen tilldelas rollen instruktör.

## Orsak

Eftersom roller inte kan förgrenade vid grupptilldelning av användare i en användargrupp tilldelas instruktörsrollen alla användare.

## Lösning

Skapa anpassade användargrupper för att filtrera användarrollerna som är tilldelade till en session. Så här tar du bort de tilldelade instruktörsrollerna i en användargrupp:

1. Logga in som administratör. Klicka på i den vänstra panelen **[!UICONTROL Email Templates]**.
1. Om du vill undvika e-postutlösare för de ändringar som ska göras klickar du på **[!UICONTROL Disable All]**.

   ![](assets/instructor-disable-all.png)

1. Gå till **Användare** > **Användargrupp**. Klicka **[!UICONTROL Add]**.

   ![](assets/instructor-usergroups.png)

1. Skapa en anpassad användargrupp i fönstret Lägg till användargrupp på följande sätt:

   * Ange ett namn på den anpassade gruppen i dialogrutan **[!UICONTROL Name]** område.
   * Under **[!UICONTROL Include Learners]** -fältet lägger du till användargruppen som du vill filtrera instruktörer för.
   * Under **[!UICONTROL Exclude Learners]** -fältet lägger du till de användare som du vill behålla instruktörsrollen för.

   ![](assets/instructor-add-ug.png)

   Stegen ovan skapar en lista över användare som ska läggas till i inkluderingsuppsättningen och tar bort specifika användare (instruktörer) som nämns i uteslutningsuppsättningen.

1. Klicka **[!UICONTROL Save]** de ändringar som gjorts.
1. Sök efter den skapade anpassade användargruppen genom att gå till **[!UICONTROL Users]** > **[!UICONTROL Internal]**.

   ![](assets/instructor-custom-ug.png)

1. Markera kryssrutan för att välja alla användare i gruppen.

   ![](assets/instructor-bulk-ug.png)

1. Klicka **[!UICONTROL Actions]** > **[!UICONTROL Remove Role]** > **[!UICONTROL Remove Instructor]**.

Se till att alla e-postutlösare som inaktiverades i steg 2 återaktiveras när de är klara.
