---
description: Skapa utbildningsplaner för administratörer i Learning Manager.
jcr-language: en_us
title: Utbildningsplaner
contentowner: manochan
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '1400'
ht-degree: 0%

---


# Utbildningsplaner

Skapa utbildningsplaner för administratörer i Learning Manager.

## Översikt {#overview}

En utbildningsplan är en uppsättning regler som registrerar elever för angivna utbildningar baserat på vissa kriterier.

Med en utbildningsplan kan en administratör automatiskt tilldela kurser, utbildningsprogram eller certifieringar baserat på förekomsten av vissa händelser, som att ta in en ny anställd eller ändra de anställdas beteckning eller plats.

När en anställd t.ex. går med i en organisation tilldelas orienteringsprogrammet för nya anställda automatiskt till den anställde. Om en anställd befordras som chef tilldelas medarbetaren automatiskt ett nytt chefsorienteringsprogram.

Du kan registrera elever för alla kurser och utbildningsprogram automatiskt baserat på en fördefinierad uppsättning händelser. Du kan skapa utbildningsvägar till eleverna genom att automatiskt tilldela en uppföljningsutbildningsaktivitet efter att en elev har slutfört en kompetens, kurs eller ett utbildningsprogram.

## Skapa utbildningsplaner {#createlearningplans}

Om du vill skapa en utbildningsplan måste du logga in som administratör.

1. I den vänstra rutan klickar du på **[!UICONTROL Learning Plans]**. Om det finns några befintliga händelser visas de på sidan. Men om du konfigurerar funktionen för utbildningsplanen för första gången går du vidare till nästa steg.
1. I det övre högra hörnet på sidan klickar du på **[!UICONTROL Add]**. I dialogrutan **[!UICONTROL Add Learning Plan]** -dialogrutan anger du namnet på utbildningsplanen som en anställd måste genomföra.

   ![](assets/add-learning-plandialog.png)

1. I dialogrutan **[!UICONTROL Occurs when]** listrutan väljer du önskad händelse. Alternativen bestämmer när en elev tar kursen. När du har valt typ av evenemang väljer du lämplig utbildning, kurser, utbildningsprogram eller certifiering.

   **Obs!** Både administratörer och författare kan skapa händelser för automatisk registrering.

   Händelserna är:

   **1 - Ny elev läggs till:** När en ny användare eller anställd ansluter sig till organisationen.

   ![](assets/new-learner-is-added.png)

   **2 - Eleven läggs till i en grupp:** När en ny användare eller anställd går med i en grupp.  Ange och välj användargruppen i listrutan som den här händelsen gäller. Du kan välja flera grupper. Du kan också tilldela den här händelsen till alla befintliga medlemmar i dessa grupper genom att välja alternativet.

   ![](assets/learner-gets-addedtoagroup.png)

   Den här utbildningsplanen är särskilt utformad för ***Custom- Groupe*** användare. Skriv namnet på gruppen i fältet och välj gruppen eller grupperna med hjälp av sökningstypen framåt.

   **3 - Eleven slutför ett utbildningsobjekt:** Händelsen utlöses när en elev slutför ett utbildningsobjekt som kurs, utbildningsprogram och så vidare. Välj utbildningsobjektet som den här händelsen gäller för. Välj slutförandestatus för händelsen. Du kan även välja den användargrupp som eleven tillhör. Ange antalet dagar som denna händelse utlöses efter att utbildningsobjektet har slutförts. Välj alternativet om du vill tilldela denna händelse till befintliga användare som redan har slutfört utbildningsobjektet.

   ![](assets/learner-completealearningobject.png)

   **4 - Eleven uppnår en färdighetsnivå:** Ange kompetensnamnet och välj kompetensnivå. Du kan också välja den användargrupp som denna elev tillhör. Det är valfritt. Ange antalet dagar som den här händelsen ska utlösas när kompetensen har uppnåtts. Välj alternativet om du vill tilldela denna händelse till befintliga elever som redan har uppnått denna kompetens.

   ![](assets/learner-achievesaskilllevel.png)

   Ange dessutom antalet dagar efter vilka utbildningsplanen måste tilldelas eleverna.

   ![](assets/assign-learning.png)

   **5 - På ett visst datum:** När händelserna måste inträffa på ett visst datum. Välj det datum då händelsen måste tilldelas. Välj de användargrupper som händelsen ska tilldelas automatiskt till. Välj de instanser som ska tilldelas och om du vill kan du ange efter hur många dagar händelsen måste utlösas.

   ![](assets/on-a-specific-date.png)

1. För alla händelser kan du välja instansen från **[!UICONTROL Instance]** listruta. Du kan även välja instanser av den tilldelade utbildningen för valfri händelse.

   ![](assets/choose-instance.png)

   I Learning Manager skapar en utbildningsplan en egen instans, Auto. När du väljer en grupp, till exempel Alla elever, registreras då som standard alla elever i utbildningsplanen i instansen Auto.

   När du sparar utbildningsplanen visas instansen Auto som ett alternativ i **[!UICONTROL Select Instance]** Listrutan i avsnittet Elever för en kurs.

1. Om du vill spara utbildningsplanen klickar du på **[!UICONTROL Save]**.

## Avregistrera dig från utbildning {#unenroll-training}

När en utbildningsplan läggs till kan administratören avregistrera användare från specifika utbildningar baserat på vissa utlösare.

I Admin-programmet klickar du på **[!UICONTROL Learning Plans]** > **[!UICONTROL Add]**.

Nästa avsnitt representerar de utlösare där alternativet **[!UICONTROL Unenroll from Training]** har lagts till.

## Eleven tas bort från en grupp {#learnergetsremovedfromagroup}

1. Lägg till en eller flera användargrupper. Om flera grupper väljs utlöses planen när en elev tas bort från någon av de nämnda grupperna.
1. Välj åtgärden som **[!UICONTROL Unenroll from training]**.

   1. Administratören kan välja de utbildningar som användaren ska avregistreras från när den tas bort från användargruppen.
   1. Instansen och slutförandedatumet gäller inte i det här scenariot.

![](assets/image038.png)

## Eleven slutför en utbildning {#learnercompletesatraining}

1. Lägg till en eller flera användargrupper. Om flera grupper väljs utlöses planen när en elev slutför den angivna utbildningen.
1. Välj åtgärden som **[!UICONTROL Unenroll from training]**.

   1. Administratören kan välja de utbildningar som användaren ska avregistreras från när de läggs till i användargruppen.
   1. Instans- och slutförandedatum gäller inte i det här fallet.

![](assets/image040.png)

## Eleven läggs till i en grupp {#learnergetsaddedtoagroup}

1. Lägg till en eller flera användargrupper. Om flera grupper väljs utlöses planen när en elev läggs till i någon av de nämnda grupperna.
1. Välj åtgärden Avregistrera dig från utbildning.

   1. Administratören kan välja de utbildningar som användaren ska avregistreras från när de läggs till i användargruppen.
   1. Instans- och slutförandedatum gäller inte i det här fallet.

![](assets/image043.png)

## Eleven uppnår en kompetensnivå {#learnerachievesaskilllevel}

1. Ange den kompetens som ska uppnås.
1. Lägg till en eller flera användargrupper. Om flera grupper väljs utlöses planen när en elev uppnår den valda kompetensen.

![](assets/image045.png)

## På ett visst datum {#onaspecificdate}

1. Välj det datum då elever ska avregistreras.
1. Lägg till en eller flera användargrupper. Om flera grupper väljs utlöses planen på datumet och avregistrerar användarna, som ingår i de valda grupperna.
1. Välj åtgärden Avregistrera dig från utbildning.

   1. Administratören kan välja de utbildningar som användaren ska avregistreras från när denne avregistreras på det angivna datumet.
   1. Instans- och slutförandedatum gäller inte i det här fallet.

![](assets/image047.png)

## Redigera en utbildningsplan {#editalearningplan}

När du har skapat en utbildningsplan kan administratören redigera/uppdatera utbildningsplanen när som helst. Klicka på utbildningsplanens namn och ändra värdena i **[!UICONTROL Edit Learning Plan]** popup-dialogruta som visas. Klicka **[!UICONTROL Save]**.

## Aktivera en utbildningsplan {#enablealearningplan}

Som standard är alla nya utbildningsplaner som du har skapat i inaktiverat läge. Du måste göra det möjligt för en plan att tilldela en elev. När du aktiverar kryssrutan **[!UICONTROL Current Learners]** aktiveras händelsen av sig själv.

För att aktivera en utbildningsplan

1. Välj den plan du vill aktivera i listan över utbildningsplaner.

   ![](assets/list-of-learningplans.png)

1. I det övre högra hörnet på sidan klickar du på **[!UICONTROL Actions]** > **[!UICONTROL Enable]**. Då aktiveras utbildningsplanen.

## Radera en utbildningsplan {#deletealearningplan}

För att radera en utbildningsplan,

1. Välj den plan som du vill ta bort i listan över utbildningsplaner.
1. I det övre högra hörnet på sidan klickar du på **[!UICONTROL Actions]** > **[!UICONTROL Delete]**.

## Inaktivera en utbildningsplan {#disablealearningplan}

Om du vill inaktivera en utbildningsplan

1. Klicka på fliken **[!UICONTROL Enabled]**.
1. Välj den plan som du vill inaktivera i listan över utbildningsplaner.
1. I det övre högra hörnet på sidan klickar du på **[!UICONTROL Actions]** > **[!UICONTROL Disable]**. Då flyttas planen till **[!UICONTROL Disabled]** -fliken.

## Filtrera en utbildningsplan {#filteralearningplan}

Du kan filtrera utbildningsplaner efter typen av händelse som användes när en utbildningsplan skapades. Klicka **[!UICONTROL Type]** och välj ett alternativ för att visa utbildningsplaner som matchar urvalet.

![](assets/filter-a-learningplan.png)

## Vanliga frågor {#frequentlyaskedquestions}

1. Hur konfigurerar jag Learning Manager för automatiska registreringar för registrering av nya anställningar?

   I dialogrutan **[!UICONTROL Occurs when]** listruta väljer du alternativet **[!UICONTROL New Learner is added]**. Tilldela sedan utbildningsobjekten, instansen och slutförandedatumet för eleven. Både administratörer och författare kan skapa händelser för automatisk registrering. Aktivera händelsen när den har skapats.

1. Hur konfigurerar jag en utbildningsplan/automatisk registrering för klassrumskurs och virtuella klassrumskurser?

   Vi rekommenderar att du konfigurerar kursinstansen med obligatoriska sessionsdetaljer. Skapa sedan en utbildningsplan och mappa den till kursinstansen som redan har skapats.

1. Hur visar jag listan över elever som har registrerats för en specifik utbildningsplan?

   När instansen Auto skapas klickar du på **[!UICONTROL Course]** > **[!UICONTROL Learners]** och välj önskad instans från **[!UICONTROL Instance]** listruta.
