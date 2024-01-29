---
jcr-language: en_us
title: Lägga till användare i grupp
description: Lär dig lägga till flera användare åt gången.
contentowner: saghosh
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---



# Lägga till användare i grupp

Ja, du kan lägga till flera användare åt gången genom att följa stegen nedan:

1. Klicka **[!UICONTROL Users]** i den vänstra rutan i Administratörsinloggning och klicka sedan på **[!UICONTROL Add]** > **[!UICONTROL Upload a csv]**. En popup-dialogruta visas.

1. Du kan lägga till flera användare med hjälp av en .CSV-fil. Klicka **[!UICONTROL Import]** och välj/öppna .csv-filen från datorn.

1. När du har importerat filen mappar du innehållet i CSV-filen med programetiketterna när du överför .csv-filen första gången.

   För alla efterföljande överföringar beaktas tidigare inställningar för etiketter. Klicka **[!UICONTROL Save]** efter att du har slutfört datamappningen och klickar på **[!UICONTROL Add]** för att överföra den mappade CSV-filen.

1. Klicka **[!UICONTROL Save]** efter att du har slutfört datamappningen och klickar på **[!UICONTROL Add]** för att överföra den mappade CSV-filen.

## CSV-överföring med obligatoriska fält {#csvuploadwithmandatoryfields}

Det är inte obligatoriskt att lägga till användarens profil och chefens e-post-ID i CSV-filen. Användarnamn och användarens e-post-ID är de enda obligatoriska fälten.

I så fall behandlas företagets administratör som standard som chef för användarna. Som standard betraktas anställd som användarens profil.

**CSV-exempel**

CSV-exempelfilen för Learning Manager finns nedan med obligatoriska fält.
[Sample-CSV-name-email.zip](assets/sample-csv-name-email.zip)

## CSV-överföring med alla fält {#csvuploadwithallthefields}

Innan du inkluderar chefens e-post-ID för en medarbetare ser du till att chefen först läggs till som medarbetare i CSV. Se t.ex. medarbetarens namn, Howard Walters i bilden nedan:

![](assets/csv-example.png)

*CSV-mall för överföring*

Administratörer i en organisation kan också lägga till sig själva som anställda och nämna deras chefs e-post-id som rot.

**CSV-exempel**

CSV-exempelfilen för Learning Manager finns nedan med alla fält.
[learning-manager-sample-csv.zip](assets/learning-manager-sample-csv.zip).

Se  [Använda CSV-överföring](/help/migrated/administrators/feature-summary/add-users-user-groups.md) för mer information.
