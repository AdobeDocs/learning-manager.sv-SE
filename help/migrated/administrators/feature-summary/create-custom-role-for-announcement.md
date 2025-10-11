---
title: Anpassad roll med omfattande meddelandebehörigheter
jcr-language: en_us
description: Läs om hur du skapar en anpassad roll i Adobe Learning Manager som endast tillåter meddelanden för utvalda kataloger och användargrupper.
source-git-commit: 85eeebb33a67bf5528c88b26941345e00e98e0d3
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---


# Anpassad roll med omfattande meddelandebehörigheter

Administratörer kan skapa anpassade roller med meddelandebehörigheter som är begränsade till specifika kataloger och användargrupper. Detta säkerställer att meddelanden är riktade, relevanta och endast synliga för de avsedda eleverna. Omfångsmeddelanden säkerställer att rätt användare får relevanta meddelanden utan att skicka information till andra.

## Skapa en anpassad roll med ett specifikt omfång

Administratören kan skapa en anpassad roll med meddelandebehörigheter som är begränsade till en viss katalog och användargrupp.

Så här skapar du en anpassad roll med en specifik omfattning:

1. Logga in på Adobe Learning Manager som administratör.
2. Välj **[!UICONTROL Users]** i den vänstra navigeringsrutan.

   ![](assets/select-uses-admin.png)
   _Tilldela användare anpassade roller för målinriktade behörigheter och ansvarsområden i Adobe Learning Manager_

3. Välj Anpassade roller.
4. Välj Skapa anpassad roll.

   ![](assets/create-custom-roles.png)
   _Tilldela anpassade roller till användare för att anpassa behörigheter och effektivisera den administrativa kontrollen för specifika användargrupper eller kataloger_

5. Ange namnet på och beskrivningen av den anpassade rollen.
6. Välj Meddelande under Kontobehörigheter.

   ![](assets/select-announcement.png)
   _Aktivera meddelandebehörigheter under Kontobehörigheter så att anpassade administratörer kan hantera riktad kommunikation inom omfattningen_

7. Välj Ange åtkomst per katalog under Omfång för funktionsbehörighet och välj katalogen.
8. I samma avsnitt väljer du Ange åtkomst per användargrupp och väljer önskad
användargrupp.

   ![](assets/select-scope-announcement.png)
   _Ange användargrupp- och katalogomfång för att se till att anpassade administratörer kan hantera behörigheter och åtkomst endast inom sina tilldelade omfång_

9. Välj och lägg till användaren som du vill tilldela den här anpassade rollen. De tilldelade användarna kan skapa ett meddelande för sitt omfång.

En anpassad administratör kan skapa meddelanden som är begränsade till de användargrupper och kataloger som de tilldelats, vilket säkerställer att meddelandena når rätt målgrupp och förhindrar onödiga meddelanden. För aviseringar och e-postmeddelanden kan administratörer lägga till extra användargrupper, men endast användare inom det definierade omfånget får dem. För rekommendations- och Masthead-meddelanden kan du bara välja användargrupper inom det tilldelade omfånget.

## Skapa meddelande för det tilldelade omfånget

En anpassad administratör kan skapa meddelanden som är begränsade till de användargrupper och kataloger som de tilldelats, vilket säkerställer att meddelandena når rätt målgrupp och förhindrar onödiga meddelanden.

Så här skapar du ett meddelande för det tilldelade omfånget:

1. Logga in på Adobe Learning Manager som en anpassad administratör.
2. Välj **[!UICONTROL Announcement]** i den vänstra navigeringsrutan.
3. Välj **[!UICONTROL Add]**.

   ![](/help/migrated/assets/create-add-announcement.png)
   _Sidan Meddelanden i Adobe Learning Manager, där administratörer kan skapa och hantera meddelanden för målanvändargrupper_

4. Välj **[!UICONTROL Announcement Type]** i listrutan.
a. **[!UICONTROL As Notification]**
b. **[!UICONTROL As Masthead]**
c. **[!UICONTROL As Recommendation]**
d. **[!UICONTROL As Email]**
5. Välj **[!UICONTROL As Masthead]**.
6. Välj språk och överför en bild för masthead.
7. Du kan även lägga till en URL till åtgärdsknappen.

   ![](/help/migrated/assets/announcement-screen.png)
   _Skapa en meddelandeskärm där administratörer kan ange meddelandetyp, överföra bilagor och lägga till åtgärdsknappar_

   Det tilldelade omfånget är förvalt i avsnittet **[!UICONTROL Scope]** och kan inte ändras av anpassade administratörer.

   >[!NOTE]
   >
   >**[!UICONTROL For Notification]**- och **[!UICONTROL Email]**-meddelanden, de kan innehålla ytterligare användargrupper och kataloger om dessa överlappar deras tilldelade omfång.

8. Välj **[!UICONTROL Save]**.

Det är bara elever inom den anpassade administratörens omfattning som kan se meddelandet. Om du vill ha mer information om hur du skapar flera typer av meddelanden läser du i den här [artikeln](/help/migrated/administrators/feature-summary/announcements.md).

## Återställ omfattningen av anpassade administratörer

Anpassade administratörer kan återställa omfattningen av sina publicerade meddelanden om en administratör har ändrat deras omfattning. När omfattningen har återställts tillämpas det uppdaterade omfånget på tillkännagivandet och endast elever inom det nya omfånget kan se tillkännagivandet.

Så här återställer du omfånget:

1. Logga in på Adobe Learning Manager som en anpassad administratör.
2. Välj **[!UICONTROL Announcement]** i den vänstra navigeringsrutan.
3. Välj fliken **[!UICONTROL Published]**.
4. Välj ett meddelande och välj sedan inställningsikon.
5. Välj **[!UICONTROL Edit]**.

   ![](/help/migrated/assets/select-edit-published-announcement.png)
   _Meddelandeskärmen visar de publicerade meddelandena med alternativ för redigering, publicering och annat_

6. Välj **Återställ**.

   ![](/help/migrated/assets/reset-the-scope.png)
   _Meddelande som visar ett meddelande om scopeändring, med ett alternativ för anpassade administratörer att återställa och uppdatera scopevalet för att återspegla nya åtkomstbehörigheter_

Omfattningen uppdateras och endast användare inom det uppdaterade omfånget kan se tillkännagivandet.

## Redigera meddelandet via administratörsgränssnittet

Administratörer kan redigera och hantera alla meddelanden som skapas av anpassade administratörer. Om en administratör försöker redigera ett meddelande som skapats av en anpassad administratör med en viss omfattning visas ett varningsmeddelande i meddelandet med information om omfattningen **[!UICONTROL Remove]**. Administratören kan ta bort omfattningen för att göra meddelandet tillgängligt för alla. I det här fallet får den anpassade administratören en varning om att meddelandets omfattning har ändrats.

Så här redigerar du meddelandet via administratörsgränssnittet:

1. Logga in på Adobe Learning Manager som administratör.
2. Välj **[!UICONTROL Announcement]** i den vänstra navigeringsrutan.
3. Välj fliken **[!UICONTROL Published]**.
4. Välj ett meddelande och välj sedan inställningsikon.
5. Välj **[!UICONTROL Edit]**.

   ![](/help/migrated/assets/select-edit-published-announcement.png)
   _Meddelandeskärmen visar de publicerade meddelandena med alternativ för redigering, publicering och annat_

6. Välj **[!UICONTROL Remove]**.

   ![](/help/migrated/assets/remove-the-scope.png)
   _En meddelandeskärm som anger att omfånget måste tas bort för att administratörer ska kunna redigera meddelanden som skapats för användargrupper med omfång_

Administratören kan redigera meddelandet efter att omfånget har tagits bort.
