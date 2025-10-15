---
description: Läs mer om att skapa L1-feedbackformulär för eleverna
jcr-language: en_us
title: L1-feedbackformulär
source-git-commit: 70baa9d9871fb05e988973b61ce0af105459afb3
workflow-type: tm+mt
source-wordcount: '1111'
ht-degree: 0%

---


# L1-feedbackformulär

>[!IMPORTANT]
>
>Den förbättrade L1-feedbackfunktionen distribueras till utvalda kunder. Om du inte ser den här funktionen i ditt konto kan du titta i [Lägg till L1- och L3-feedback](/help/migrated/administrators/feature-summary/courses.md#add-l1-and-l3-feedback) om du vill ha mer information om den befintliga feedbackfunktionen.
>
>Kontakta ditt CSM-team (Customer Success Manager) för att aktivera det nya feedbacksystemet och lära dig mer om migreringstidslinjen.

Med feedbackfunktionen på nivå 1 (L1) i Adobe Learning Manager kan elever dela med sig av sin feedback efter att ha slutfört en kurs eller ett utbildningssteg. Denna feedback hjälper administratörer att utvärdera kurskvaliteten, instruktörens effektivitet och den övergripande utbildningsupplevelsen.

Administratörer kan nu skapa och hantera flera återanvändbara feedbackformulär och tilldela dem till specifika kurser och utbildningsvägar.

Funktionen ger större flexibilitet genom att administratörer kan:

* Skapa återanvändbara feedbackformulär
* Anpassa feedback för olika kurser eller utbildningsvägar
* Tilldela anpassade formulär efter behov

**[!UICONTROL L1 Feedback Report]** och **[!UICONTROL Feedback Report]** (anpassad rapport) innehåller nu två nya kolumner: Namn på feedbackformulär och Version av feedback. Kolumnerna innehåller information om de feedbackformulär som används.

## Skapa L1-feedbackformulär

Administratörer kan skapa flera L1-feedbackformulär på kontonivå och tilldela rätt formulär till en kurs, utbildningsväg eller certifiering.

Så här skapar du ett L1-feedbackformulär:

1. Logga in på Adobe Learning Manager som administratör.
2. Välj **[!UICONTROL Feedback forms]**.

   ![](assets/feedback-form.png)
   _Administratörens startsida som visar alternativet Feedbackformulär för att skapa och hantera feedbackformulär_
3. Välj **[!UICONTROL Add form]**.

   ![](assets/add-form.png)
   _Feedbackformulärskärmen visar knappen Lägg till formulär för att skapa feedbackformulären_
4. Välj **[!UICONTROL Default template language]** och sedan **[!UICONTROL Save]**.

   ![](assets/default.png)
   _Lägg till ett nytt mallmeddelande som visar alternativ för att välja standardspråk_
5. Skriv formulärets rubrik och beskrivning.

   ![](assets/field-name.png)
   _Sidan Lägg till feedbackformulär som visar ett alternativ skriver formulärets rubrik och formulärbeskrivning_
6. Välj en frågetyp från följande på menyn **[!UICONTROL Add Question]**:

   a. **[!UICONTROL Free Text]**: Gör det möjligt för elever att ge svar med egna ord.

   * Skriv frågan i textfältet **[!UICONTROL Question]**.
   * Välj växlingsknappen **[!UICONTROL Mandatory]** för att göra frågan obligatorisk.
     ![](assets/free-text.png)
     _Lägg till en fritextfråga i feedbackformuläret_

   b. **[!UICONTROL Numerical Scale/NPS]**: Elever kan betygsätta hur nöjda eller sannolika de är med kursen genom att använda en numerisk skala (vanligtvis 1 till 10).

   * Skriv frågan i textfältet **[!UICONTROL Question]**.
   * Välj klassificeringsintervall (1 till 10).
   * Välj växlingsknappen **[!UICONTROL Mandatory]** för att göra frågan obligatorisk.
     ![](assets/numerical.png)\
     _Lägg till en numerisk fråga/NPS-skalfråga i feedbackformuläret_

   c. **[!UICONTROL Likert Scale]**: Elever kan ange hur mycket de samtycker till en instruktion, från Inte alls till Instämmer helt.

   * Skriv frågan i textfältet **[!UICONTROL Question]**.
   * Välj växlingsknappen **[!UICONTROL Mandatory]** för att göra frågan obligatorisk.
     ![](assets/likert.png)
     _Lägg till en Likertskalafråga i feedbackformuläret_

   d. **[!UICONTROL Course Effectiveness Score]**: En skala för att mäta hur effektivt en kurs påverkar eleverna med hjälp av ett relativt klassificeringssystem.

   * En fördefinierad fråga med en Likertskala från 1 till 10 läggs till i feedbackformuläret.
   * Du kan bara lägga till en **[!UICONTROL Course Effectiveness Score]**-fråga och den kan inte redigeras
     ![](assets/course-effective.png)
     _Lägg till frågan om effektiviteten för kursen i feedbackformuläret_
7. Välj **[!UICONTROL Save]**. Du kan visa de skapade formulären i avsnittet Feedback i Forms.

### Förhandsgranska feedbackformuläret

Du kan förhandsgranska feedbackformuläret genom att välja Förhandsgranska på engelska (USA). Om du har skapat formuläret på flera språk kan du även förhandsgranska det på varje språk. Visa det här [avsnittet](/help/migrated/administrators/feature-summary/l1-feedback-form.md#add-feedback-forms-in-other-languages) om du vill lära dig hur du lägger till feedbackformulär på andra språk.

![](assets/preview.png)
_Feedbackformulärskärmen visar förhandsgranskningsalternativet om du vill visa feedbackformuläret på standardspråket_

### Lägg till feedbackformulär på andra språk

Skapa översättningar för frågorna i feedbackformuläret på flera språk. Men du kan bara lägga till eller ta bort frågor på standardspråket (till exempel engelska). För andra språk kan du endast översätta de frågor som ursprungligen lades till på standardspråket. Det är inte möjligt att lägga till eller ta bort frågor direkt i de översatta versionerna.

1. Välj **[!UICONTROL Add New Language]** i feedbackformuläret.

   ![](assets/add-new-language.png)
   _Lägg till en ny språkversion i feedbackformuläret_
2. Välj önskat språk och välj **[!UICONTROL Save]**.
3. Gå till fliken för språket som du lade till.
4. Välj **[!UICONTROL Translate]** bredvid varje fråga för att lägga till din översättning.

   ![](assets/translate.png)
   _Skärmen Feedback visar alternativet Översätt för att översätta frågorna till respektive språk_

   >[!NOTE]
   >
   >Poängfrågan för Kursens effektivitet översätts automatiskt.

5. När du har lagt till översättningarna väljer du **[!UICONTROL Save]**.

## Ange ett feedbackformulär som standard

Administratörer kan upprätta standardformulär för feedback för kurser i eget tempo, i klassrum, i virtuella klassrum och blandade kurser. När standardformuläret har konfigurerats visas det automatiskt för elever vid slutförande av en kurs. Detta standardformulär kommer att tillämpas på alla kurser om inte administratören väljer att tilldela ett annat feedbackformulär för specifika kurser.

![](assets/set-as-default.png)
_Skärmen Feedbackformulär visar alternativ för att ange standardformulär för feedback_

## Konfigurera inställningar för elevfeedback

Administratörer kan konfigurera följande inställningar i avsnittet elevfeedback:

* **[!UICONTROL Enable form to capture learners' feedback for this Course]**: Aktivera det här alternativet om du vill samla in feedback från elever för kursen. När det här alternativet är aktiverat uppmanas elever att ge feedback efter att kursen har slutförts.
* **[!UICONTROL Form setting]**: När det här alternativet är aktiverat öppnas feedbackformuläret automatiskt för elever direkt efter att de har slutfört kursen, vilket gör det lättare att samla in feedback i tid.

![](assets/course-settigs.png)
_Skärmen för elevfeedback visar inställningarna för elevfeedback_

>[!NOTE]
>
>Kursinstanser använder standardformuläret för feedback från kursnivån. När du skapar nya instanser använder de också standardformuläret på kursnivå i stället för kontonivån.

### Ändra standardformuläret för feedback för en kurs

Standardformuläret för feedback gäller alla kurser. Administratörer kan antingen skapa ett nytt formulär eller välja ett i den befintliga listan. Om du vill ändra standardformulären för feedback måste elevfeedback vara aktiverad för den här kursen.

Så här ändrar du standardformuläret för feedback:

1. Välj **[!UICONTROL Courses]** på administratörens startsida.
2. Välj en kurs i avsnittet **[!UICONTROL Course]**.
3. Välj **[!UICONTROL View Course]** och sedan **[!UICONTROL Learner feedback]**.

   ![](assets/edit-form.png)
   _Skärmar för elevfeedback visar alternativet Redigera för att ändra formuläret_
4. Välj **[!UICONTROL Edit]** i avsnittet **[!UICONTROL Learner feedback]**.
5. Välj **[!UICONTROL Change form]**.

   ![](assets/change-form.png)
   _Skärmar för elevfeedback visar alternativet Ändra formulär för att ändra feedbackformuläret för kursen_
6. Välj ett annat feedbackformulär från menyn eller välj **[!UICONTROL Start with a blank form]** för att skapa ett nytt.

   ![](assets/pick.png)
   _Lägg till en formulärskärm som visar alternativet att välja från den tillgängliga mallen eller skapa ett nytt formulär_
7. Välj **[!UICONTROL Save]** för att tillämpa ändringarna.

Om en kurs använder standardformuläret för feedback och standardformuläret uppdateras på kontonivån kommer alla sådana kurser automatiskt att återspegla det nya formuläret. Men om en administratör ändrar formuläret eller tilldelar ett nytt formulär på kursnivån kommer framtida ändringar av standardformuläret inte att påverka kursens feedbackformulär.

Instansen använder feedbackformuläret på kursnivå som standard. Om en administratör ändrar feedbackformuläret på kursnivån kommer det inte att påverka det formulär som redan har angetts på instansnivå. Alla nya instanser som skapas efter ändringen använder dock det uppdaterade feedbackformuläret på kursnivå som standard.

Gör på samma sätt för att ändra standardformulären för feedback för en utbildningsväg.

>[!NOTE]
>
>Om du inte ändrar formuläret kommer kursen att använda standardformuläret för feedback.



