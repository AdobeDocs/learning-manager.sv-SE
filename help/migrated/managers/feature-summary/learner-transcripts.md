---
description: Lär dig ladda ned elevens betygsutdrag baserat på användare, utbildningsobjekt eller kunskaper i Learning Manager.
jcr-language: en_us
title: Elevens betygsutdrag
exl-id: 8204aa1e-0e0d-4d9e-9dc0-6260667bf4e7
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '911'
ht-degree: 0%

---

# Elevens betygsutdrag

Lär dig ladda ned elevens betygsutdrag baserat på användare, utbildningsobjekt eller kunskaper i Learning Manager.

Med Adobe Learning Manager kan chefer i en organisation generera utskrifter som är kopplade till elever.

## Generera elevbetygsutdrag {#generatelearnertranscripts}

1. Klicka på **[!UICONTROL Reports]** i den vänstra rutan i chefsinloggning för att generera elevens betygsutdrag.
1. Klicka på fliken **[!UICONTROL My Reports]** på sidan.
1. Klicka på länken **[!UICONTROL Learner Transcripts]**.

   ![](assets/learner-transcripts.png)

   *Skapa rapporter för elevutskrifter*

1. Dialogrutan Elevens betygsutdrag visas. Välj det datumintervall som du vill att transkriptionen ska genereras för.

   >[!NOTE]
   >
   >Som standard är från-startdatum elevens registreringsdatum och till-datum är alltid det aktuella datumet. Du kan bara ändra startdatumet från när du behöver informationen.

1. Välj elevnamnen i fältet Välj elever och klicka på **[!UICONTROL Generate]**.

Du kan välja en enskild elev eller grupper av elever. Lägg till fler elever genom att klicka på Lägg till fler elever.

Betygsutdrag genereras och hämtas till datorn som .xls-filer. Varje XLS-Excel-fil har sju ark. Mer information finns nedan:

## Ladda ned elevens betygsutdrag baserat på tidszonen {#lt-timezone}

Precis som en administratör kan en chef även välja vilka kolumner som ska exporteras. Dessutom kan en chef ladda ned elevens betygsutdrag baserat på den tidszon som han/hon har valt i profilinställningarna.

Om hanteraren aktiverar det här alternativet väljs tidszonen från den som angetts på sidan med profilinställningar, som visas nedan.

>[!NOTE]
>
>Kryssrutan Tidszon är inaktiverad för en ny chef.

![](assets/image030.png)

*Ladda ned elevens betygsutdrag för en tidszon*

## Elevens filinnehåll i betygsutdrag {#learnertranscriptfilecontent}

En vanlig betygsfil för elever består av sex Excel-ark i en enda fil. Elevens betygsblad ger en övergripande inblick i data inklusive antalet elever som deltar per kurs, deras färdigheter, tävlingsprocenten baserat på kurs eller elev och en efterlevnadstavla. Följande instrumentpaneler är tillgängliga i elevutskrifter:

**Elevens betygsutdrag**

I Excel-bladet för elevbetygsutdrag, tillsammans med profilinformation om eleven, finns information om utbildningsobjektets förbrukning, t.ex. registreringsdatum, startdatum, uppnådd grad, erhållna quizpoäng osv. Om kurser ingår i något utbildningsprogram listas de separat, bortsett från enskilda uppgifter om kursens förbrukning.

**1 - tavla för utbildningsaktivitet**

På den här LO-specifika instrumentpanelen kan du se antalet elever för varje kurs, utbildningsprogram eller certifiering. Du kan visa förloppsindikatorn för elever för ett visst utbildningsobjekt. Denna tabell visar data som antal elever som har slutfört kursen eller utbildningsprogrammet, elever under utveckling och elevens förfallodatum.

Användarnas förlopp för den specifika kursen beräknas baserat på inmatningsfälten där du anger tröskelvärdena för förfallodatum och förloppsprocent. Om du till exempel anger 7 dagar och 70 % som värden i inmatningsfältet visas kursförloppet för kurser som förfaller om 7 dagar och för kurser som har mer än 70 % förlopp. Du kan också ändra tidsperioden i tabellen, där ändrade data visas automatiskt på kontrollpanelen.

**2 - tavla för utbildningsaktivitet**

Utbildningstavlan visar data för en specifik användare. På den här instrumentpanelen kan du se de kurser, utbildningsprogram eller certifieringar som en viss användare har registrerat sig för. Tabellen visar även data om vilka utbildningsobjekt användaren har slutfört, vilka utbildningsobjekt som pågår och kommande inlämningsdatum för användaren.

Användarnas förlopp för varje kurs beräknas utifrån de indata som du anger. Det vill säga värdena för förfallodatum och förloppsprocent. Om du till exempel anger 7 dagar och 70 % som värden i inmatningsfältet visas användarens förlopp för olika kurser som förfaller om 7 dagar och för kurser som har mer än 70 % förlopp.

**Kompetens**

I kompetensbladet anges färdighetsnamn, kompetensnivå, obligatoriska poäng, intjänade poäng, slutförandeprocent och andra profiluppgifter. Nedan hittar du ett exempel på en ögonblicksbild av Excel-sidan för kompetens.

**Tavla för kompetens**

På den här instrumentpanelen kan du se om din organisation är utrustad med olika färdigheter. För en specifik kompetens kan du kontrollera antalet användare i en organisation som förväntas ha denna kompetens kontra antalet som faktiskt har denna kompetens. Kontrollpanelen anger även vilka användare som kan behöva uppdatera sina kunskaper. Detta värde beräknas utifrån de indata som du anger i inmatningsfältet. Om du till exempel anger 50 dagar som indata visar kontrollpanelen data om användare som kan behöva uppdatera sina kunskaper efter 50 dagar.

Denna tavla för kompetenser är mer användarspecifik. Du kan filtrera en eller flera användare och visa deras kunskapsnivå som en kontrollpanel. Detta blad kan hjälpa chefer och administratörer att spåra hur skickliga varje elev är jämfört med hur skickliga de förväntas vara. Instrumentpanelen för kompetens belyser också de elever som behöver uppdatera sina färdigheter. Elevens uppdateringslista beräknas utifrån antalet dagar som du anger i inmatningsfältet.

**Efterlevnadstavla**

Efterlevnadstavlan består av två delar - efterlevnadsrapport per användare och efterlevnadsrapport per utbildning. För den användarbaserade rapporten kan du använda efterlevnadstavlan för att spåra användare som har kommande förfallodatum för viktiga efterlevnadsinitiativ. För den utbildningsbaserade rapporten kan du filtrera på utbildningsprogram eller certifiering.

Filtrera efter inlämningsdatum för att visa relevanta data för båda efterlevnadsrapporterna.
