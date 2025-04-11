---
jcr-language: en_us
title: Lägga till flera användare samtidigt
description: Lär dig lägga till flera användare åt gången.
contentowner: saghosh
exl-id: c3309ce5-8764-452e-82d5-5637c23c661b
source-git-commit: a28ac8f57710c118ca4ad02872fd100c6f24beac
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# Lägga till användare i grupp

I den här utbildningen får du lära dig hur du lägger till användare i grupp via en CSV-fil.

[![knapp](feature-summary/assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/7555555)

Om du inte kan starta träningen skriver du till <almacademy@adobe.com>.

## Så här lägger du till flera användare

Du kan lägga till flera användare samtidigt genom att följa stegen nedan:

1. Klicka **[!UICONTROL Users]** på den vänstra rutan i Administratörsinloggning och klicka sedan på **[!UICONTROL Add]** > **[!UICONTROL Upload a csv]**. En popup-dialogruta visas.

1. Du kan lägga till flera användare med hjälp av en . CSV-fil. Klicka **[!UICONTROL Import]** och välj/öppna den .csv filen från din dator.

1. När du har importerat filen mappar du innehållet i CSV-filen med programetiketterna när du överför .csv-filen första gången.

   För alla efterföljande överföringar beaktas tidigare inställningar för etiketter. Klicka på **[!UICONTROL Save]** efter att du har slutfört datamappningen och klicka på **[!UICONTROL Add]** för att överföra den mappade CSV-filen.

1. Klicka på **[!UICONTROL Save]** efter att du har slutfört datamappningen och klicka på **[!UICONTROL Add]** för att överföra den mappade CSV-filen.

## CSV-uppladdning med obligatoriska fält {#csvuploadwithmandatoryfields}

Det är inte obligatoriskt att lägga till användarens profil och chefens e-post-ID i CSV-filen. Användarnamn och användarens e-post-ID är de enda obligatoriska fälten.

I det här fallet behandlas företagets administratör som chef för användare som standard. Som standard betraktas medarbetaren som användarens profil.

>[!NOTE]
>
>Om du vill lägga till nya användare skapar du en ny CSV-fil med deras uppgifter och laddar upp den. Det går inte att uppdatera och ladda upp en befintlig CSV-fil igen.

**Exempel på CSV**

Exempel på CSV-fil för Learning Manager finns nedan med obligatoriska fält.
[Sample-CSV-name-email.zip](assets/sample-csv-name-email.zip)

## CSV-uppladdning med alla fält {#csvuploadwithallthefields}

Innan du inkluderar chefens e-post-ID för en medarbetare ser du till att chefen först läggs till som medarbetare i CSV. Se t.ex. medarbetarens namn, Howard Walters i bilden nedan:

![](assets/csv-example.png)

*CSV-mall för överföring*

Administratörer i en organisation kan också lägga till sig själva som anställda och nämna sin chefs e-post-ID som root.

**Exempel på CSV**

Exempel på CSV-fil för Learning Manager finns nedan med alla fält.
[learning-manager-sample-csv.zip](assets/learning-manager-sample-csv.zip).

Mer information finns i  [Använda hjälpinnehåll för CSV-uppladdningsfunktionen](/help/migrated/administrators/feature-summary/add-users-user-groups.md) .
