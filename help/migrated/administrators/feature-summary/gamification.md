---
description: Spelifiering är ett sätt att använda spelteknik och spelmekanik i icke-spelkontexter för att engagera användare i att tjäna poäng under inlärningen.
jcr-language: en_us
title: Spelifiering
contentowner: manochan
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '1398'
ht-degree: 0%

---



# Spelifiering

Spelifiering är ett sätt att använda spelteknik och spelmekanik i icke-spelkontexter för att engagera användare i att tjäna poäng under inlärningen.

## Översikt {#overview}

Med Learning Manager kan du använda ett strukturellt spelifieringslager på innehållet för att engagera elever och motivera dem att uppnå sina utbildningsmål. Det gör det möjligt för eleverna att få poäng för olika utbildningsaktiviteter och uppnå brons-, silver-, guld- och platinanivåer.

Som standard är vissa exempelspelifieringspunkter och data tillgängliga för användare för att förstå mönstret. Du kan ändra punkterna på motsvarande sätt.

<!--A sample illustration is provided below that shows all the tasks and points.

![](assets/gamification-feb12-e1439214291423.png)-->

## Spelifieringsinställningar {#gamificationsettings}

Följ stegen nedan för att komma åt inställningarna:

1. Logga in som administratör och klicka på i den vänstra rutan **[!UICONTROL Gamification]**.
1. När du skapar ett nytt Learning Manager-konto är spelifiering inaktiverat som standard. Klicka på för att aktivera den **[!UICONTROL Enable]** längst upp till höger på sidan.

## Administratörsåtgärder {#administratoractions}

Administratören kan skapa en lista över konfidentiella användare, återställa spelifieringspunkter och inaktivera/aktivera spelifieringsfunktionen för elever. Klicka på listrutan Åtgärder i det övre högra hörnet på sidan för att visa åtgärderna som visas i ögonblicksbilden nedan.

![](assets/gamification-actions.png)

*Spelifieringsalternativ för en administratör*

## Sekretessinställningar {#confidentialitysettings}

Om det behövs kan du göra vissa hanteringsanvändare mer sekretessbelagda. Konfidentiella användares spelifieringsaktiviteter är inte synliga för andra elever i resultatlistan.

Sekretessinställningar kan användas för både interna och externa användare.

1. Klicka **[!UICONTROL Gamification]** > **[!UICONTROL Settings]** > **[!UICONTROL Confidentiality Settings]**.

![](assets/confidentiality-settings.png)

*Visa sekretessinställningar*

1. Klicka på kryssrutan bredvid Användarnamn bland användarna i listan och klicka på Dölj om du vill göra användaren konfidentiell.

   >[!NOTE]
   >
   >Du kan identifiera konfidentiella användare i listan med användare genom att markera kryssrutan vid användarnamnet.

1. Klicka på fliken Konfidentiella användare för att visa listan över konfidentiella användare. Som standard visas de inte. Klicka på rullgardinsikonen för att visa listan.
1. Markera kryssrutan vid användarnamnet i listan Konfidentiella användare och klicka på Lägg till för att ta bort användarna från listan Konfidentiella.

## Återställ spelifiering {#resetgamification}

Du kan återställa elevens spelifieringspoäng och även återställa konfigurationsinställningarna. Om du väljer att återställa användarpoäng raderas alla poäng som användarna tjänat in och återställs till noll. Om du väljer att återställa användarpoäng och konfigurationsinställningar återställs alla standardpunkter som har tilldelats nivåer och uppgifter till noll.

Återställ spelifieringsinställningar kan användas för både interna och externa användare.

Om du vill återställa elevens poäng och konfiguration klickar du på Återställ spelifiering och väljer ett alternativ efter dina behov. Du kan välja mellan att återställa elevpoäng och att återställa elevpoäng och konfigurationsinställningarna. När du har valt klickar du på OK.

![](assets/reset-gamification.png)

*Återställ spelifieringspunkterna*

## Inaktivera spelifiering {#disablegamification}

Klicka [!UICONTROL **Spelifiering**] > [!UICONTROL **Spelifieringsfunktion**]. Detta gör att du kan aktivera funktionen för spelifiering och resultattavlan separat för dina elever. Välj mellan Aktivera för interna elever och Aktivera för externa elever enligt kraven och klicka på OK. Alla punkter bibehålls när du aktiverar spelifieringen igen.

![](assets/gamification-feature.png)

*Inaktivera spelifiering*

Du kan inaktivera spelifiering för både interna och externa användare.

## Ställ in punkter {#setuppoints}

Administratörer kan konfigurera spelifieringspunkter för elever genom att följa stegen nedan:

1. Klicka **[!UICONTROL Gamification]** när du har loggat in som administratör.\
   En sida visas med en lista över nivåer av brons, silver, guld och platina och de poäng som krävs för att uppnå varje nivå. En lista över aktiviteter och motsvarande punkter visas.
1. Klicka på Redigera-ikonen bredvid varje uppgift för att ställa in punkterna.
1. Ändra frekvensen för aktiviteter som att slutföra ett visst antal kurser per månad, kvartal eller år.
1. Klicka **[!UICONTROL Save]**.

## Uppgifter {#tasks}

Det finns fem spelifieringsuppgifter för elever där administratören kan ange poängen. En bild som visar alla elevuppgifter och poäng visas nedan:

>[!NOTE]
>
>Spelifieringspoäng för elever inom en viss uppgift är inte kumulativa. Men poängen läggs till i elevkontot kumulativt om eleverna får dessa poäng för olika uppgifter.

När administratörer tilldelar kurser till poäng måste de se till att eleverna får poängen gradvis.

**För snabb elev**

Denna uppgift är tillämplig när en elev slutför ett visst antal kurser inom en månad/kvartal/år. Denna uppgift är att uppmuntra snabba elever.

Du kan se följande möjliga scenarier:

1. När elever slutför två kurser inom en månad/kvartal/år får de 20 poäng.
1. När elever slutför fyra kurser inom en månad/kvartal/år får de 100 poäng.
1. När eleverna slutför åtta kurser får de 300 poäng.
1. När eleverna slutför tio kurser får de 500 poäng.

>[!NOTE]
>
>Administratören kan ändra tidsperioden och antalet kurser som krävs för att slutföra för att tjäna motsvarande poäng.

Inom en uppgift ges inte poäng till elever kumulativt. Säg att en elev slutför ett par kurser och får 20 poäng. När eleverna slutför fyra kurser får de 100 poäng men de befintliga 20 poängen beaktas inte.

**För elev med egenhanterad utbildning (a)**

Denna uppgift är tillämplig när elever registrerar sig för föreskrivet antal kurser och slutför inom en månad/kvartal/år. I det här fallet kan administratören aktivera den här uppgiften för att tilldela poäng och uppmuntra dem.

Möjliga scenarier:

1. När elever registrerar sig för en kurs inom en månad/kvartal/år får de 50 poäng.
1. När elever registrerar sig för två kurser under en månad/kvartal/år får de 150 poäng.

>[!NOTE]
>
>Administratören kan ändra tidsperioden och antalet kurser.

**För elev med egenhanterad utbildning (b)**

Denna uppgift kan utföras när elever registrerar sig och slutför fler kurser än vad som krävs för att slutföra under en månad/kvartal/år. I sådana fall kan administratören aktivera uppgiften för att tilldela poäng och uppmuntra dem.

Möjliga scenarier för elever att registrera sig för kurser utöver de tilldelade kurserna:

1. När elever registrerar sig för en kurs inom en månad/kvartal/år får de 20 poäng.
1. När elever registrerar sig för två kurser under en månad/kvartal/år får de 100 poäng.
1. När elever registrerar sig för tre kurser under en månad/kvartal/år får de 300 poäng.
1. När elever registrerar sig för fyra kurser under en månad/kvartal/år får de 500 poäng.

>[!NOTE]
>
>Administratören kan ändra tidsperioden och antalet kurser. Det tredje scenariot kan till exempel ändras till fem kurser i stället för tre för att ge 80 poäng.

**För förkovran (a)**

Denna uppgift är tillämplig när elever slutför ett visst antal kompetenser. Administratören kan välja den här uppgiften för att uppmuntra elever att få så många kompetenser som möjligt.

Möjliga scenarier för förkovran i kompetenser:

1. När en elev uppnår en kompetens får hen 100 poäng.
1. När en elev uppnår två kompetenser får denne 300 poäng.
1. När en elev uppnår tre kompetenser får denne 600 poäng.
1. När en elev uppnår fyra kompetenser får denne 900 poäng.

>[!NOTE]
>
>Tidsperioden gäller inte för den här uppgiften. Administratören kan ändra antalet kurser för varje scenario.

**För förkovran (b)**

Denna uppgift är tillämplig när elever slutför varje högre nivå inom en kompetens.

Möjliga scenarier för vidareutbildning på nivåer inom en viss kompetens:

1. När elever når en nivå får de 100 poäng.
1. När elever når upp till två nivåer får de 200 poäng.
1. När eleverna når upp till tre nivåer får de 500 poäng.

>[!NOTE]
>
>Tidsperioden gäller inte för den här uppgiften. Om elever uppnår en högre nivå och sedan uppnår en lägre nivå av en kompetens får de poäng endast för den högre nivån.

**Poäng för tidigt slutförande**

Denna uppgift är tillämplig för elever när de blir de första N eleverna att slutföra kursen.

Möjligt scenario:\
När en elev blir en av de första tio eleverna som slutför kursen får han/hon 100 poäng.

**Poäng för slutförande i tid**

Denna uppgift är tillämplig för elever när de slutför en kurs inom ett visst antal dagar efter registrering till kursen.

Möjligt scenario:\
När en elev slutför en kurs inom 10 dagar i början av kursen får hen 100 poäng.

## spelifiering på gruppnivå {#grouplevelgamification}

Administratörer kan definiera omfattningen av spelifieringen genom att ändra omfångsinställningarna. Du kan välja att aktivera spelifiering bland liknande profilanvändare, grupper eller platser.

1. Klicka på i Administratörsinloggning **[!UICONTROL Gamification]** i den vänstra rutan.
1. Öppna **[!UICONTROL Gamifications]** > **[!UICONTROL Settings]** > **[!UICONTROL Scope Settings]**. Inställningen [!UICONTROL Gamification Scope Settings] visas.

   ![](assets/scope-settings.png)

   *Visa dialogrutan Inställningar för spelifieringsomfattning*

1. Klicka på alternativet **[!UICONTROL Enable Scope Settings]**.

1. Välj Användaregenskap i listrutan.

   <!--![](assets/user-charecteristic.png)-->

1. Välj det värde som motsvarar den användaregenskap du har valt. Om du till exempel har valt användaregenskapen som profil måste du välja värdet i listrutan. Ett exempel på profilvärden visas i skärmbilden nedan som referens.

   <!--![](assets/value.png)-->

1. Klicka **[!UICONTROL Save].**
