---
jcr-language: en_us
title: Integrering med Adobe Connect
description: Författare kan skapa virtuella klassrumskurser med Adobe Connect när kurser skapas. För att aktivera Adobe Connect för ditt Learning Manager-konto måste du kontakta organisationens administratör.
exl-id: 3386ab89-fe13-42fc-9943-b7ff278ed7e9
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 0%

---

# Integrering med Adobe Connect

Författare kan skapa virtuella klassrumskurser med Adobe Connect när kurser skapas. För att aktivera Adobe Connect för ditt Learning Manager-konto måste du kontakta organisationens administratör.

## Skapa en virtuell klassrumskurs (VC) med Adobe Connect {#createvirtualclassroomvccoursewithadobeconnect}

1. På sidan Mina kurser klickar du på Lägg till moduler och väljer Virtuellt klassrum. Dialogrutan Skapa virtuellt klassrum visas.
1. I alternativet **Konferenssystem** väljer du Adobe Connect.

   ![](assets/create-vc-author.png)

   *Skapa ett virtuellt klassrum*

1. Ange titel, beskrivning, VC-datum, starttid och sluttid.

   Om Adobe Connect inte är konfigurerat för ditt konto visas ett varningsmeddelande som i skärmbilden ovan. Mallalternativ, instruktörer och andra Adobe Connect-alternativ är inaktiverade. Du måste kontakta administratören för att konfigurera Adobe Connect för ditt konto.

1. Adobe Learning Manager-programmet hämtar standardmallarna (möten, utbildning och evenemang) och instruktörslistan (användare med värdbehörigheter) från Adobe Connect. Välj önskad mall.
1. Välj instruktör för din VC-kurs i listan över instruktörer.

   ![](assets/instructors-list-author.png)

   *Välj instruktör i listan*

1. Ange kriterier för slutförande av VC-kursen. Kriterier för slutförande är den procentandel av den totala längden på kursen som en elev måste delta i för att anses vara slutförd. Till exempel, längden på kursen är 1 timme. Om du anger 50 % som kriterium för slutförande, anses kursen vara slutförd för eleven om en elev deltar i kursen även under 30 minuter.
1. Klicka på **[!UICONTROL Done]**.

## Delade mallar i Adobe Connect {#sharedtemplatesofadobeconnect}

Som standard hämtas alla delade mallar som har skapats i Adobe Connect-konto till Learning Manager-programmet. Du kan lägga till anpassade mallar genom att göra dem till delade mallar i Adobe Connect-kontot.
