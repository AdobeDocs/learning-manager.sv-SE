---
jcr-language: en_us
title: Lägga till användare i grupp
description: Lär dig lägga till flera användare åt gången.
contentowner: saghosh
exl-id: c3309ce5-8764-452e-82d5-5637c23c661b
source-git-commit: 96602899dd76eae14a6b7e1808d529756657e7b8
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# Lägga till användare i grupp

>[!INFO]
>
>I den här utbildningen får du lära dig hur du lägger till användare i grupp via en CSV-fil.<br><br>[![knapp](feature-summary/assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/7555555)</br></br>

Skriv till <almacademy@adobe.com> om du inte kan starta utbildningen.

## Lägga till flera användare

Du kan lägga till flera användare samtidigt genom att följa stegen nedan:

1. Klicka på **[!UICONTROL Users]** i den vänstra rutan i Administratörsinloggning och klicka sedan på **[!UICONTROL Add]** > **[!UICONTROL Upload a csv]**. En popup-dialogruta visas.

1. Du kan lägga till flera användare med hjälp av en .CSV-fil. Klicka på **[!UICONTROL Import]** och välj/öppna .csv -filen från datorn.

1. När du har importerat filen mappar du innehållet i CSV-filen med programetiketterna när du överför .csv-filen första gången.

   För alla efterföljande överföringar beaktas tidigare inställningar för etiketter. Klicka på **[!UICONTROL Save]** efter att du har slutfört datamappningen och klicka på **[!UICONTROL Add]** för att överföra den mappade CSV-filen.

1. Klicka på **[!UICONTROL Save]** efter att du har slutfört datamappningen och klicka på **[!UICONTROL Add]** för att överföra den mappade CSV-filen.

## CSV-överföring med obligatoriska fält {#csvuploadwithmandatoryfields}

Det är inte obligatoriskt att lägga till användarens profil och chefens e-post-ID i CSV-filen. Användarnamn och användarens e-post-ID är de enda obligatoriska fälten.

I så fall behandlas företagets administratör som standard som chef för användarna. Som standard betraktas anställd som användarens profil.

>[!NOTE]
>
>Om du vill lägga till nya användare skapar du en ny CSV-fil med information och överför den. Det går inte att uppdatera och överföra en befintlig CSV-fil på nytt.

**Exempel-CSV**

CSV-exempelfilen för Learning Manager finns nedan med obligatoriska fält.
[Sample-CSV-name-email.zip](assets/sample-csv-name-email.zip)

## CSV-överföring med alla fält {#csvuploadwithallthefields}

Innan du inkluderar chefens e-post-ID för en medarbetare ser du till att chefen först läggs till som medarbetare i CSV. Se t.ex. medarbetarens namn, Howard Walters i bilden nedan:

![](assets/csv-example.png)

*CSV-mall för överföring*

Administratörer för en organisation kan också lägga till **sig själva** som anställda och ange chefens e-post-ID som rot.

**Exempel-CSV**

CSV-exempelfilen för Learning Manager finns nedan med alla fält.
[learning-manager-sample-csv.zip](assets/learning-manager-sample-csv.zip).

Se [Hjälpinnehåll för funktionen Överför CSV](/help/migrated/administrators/feature-summary/add-users-user-groups.md) om du vill veta mer.
