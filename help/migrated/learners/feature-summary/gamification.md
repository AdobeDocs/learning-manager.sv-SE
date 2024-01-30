---
description: Engagera användare med hjälp av spelifieringstekniker i Learning Manager.
jcr-language: en_us
title: Spelifiering
contentowner: manochan
source-git-commit: a8dec2a5e91b6d989a7fb9161e84fcb1f8de752d
workflow-type: tm+mt
source-wordcount: '1456'
ht-degree: 0%

---



# Spelifiering

Engagera användare med hjälp av spelifieringstekniker i Learning Manager.

Spelifiering är ett sätt att använda spelteknik och spelmekanik i icke-spelkontexter för att engagera användare i att tjäna poäng under inlärningen.

## Översikt {#overview}

För att engagera elever och motivera dem att uppnå sina mål genom att använda speltekniker ska du använda spelifieringsfunktionen i Learning Manager. Elever kan tävla med sina kollegor för att få poäng för olika utbildningsaktiviteter och uppnå brons-, silver-, guld- och platinanivåer.

Elever kan också se prestationsnivån baserat på de poäng de har tjänat in. Nivåerna inkluderar Snabb elev, Självdriven och så vidare. **Både interna och externa elever har tillgång till den här funktionen.**

## Resultattavla {#leaderboard}

Leaderboard är en spelifieringsfunktion som fungerar som en resultattavla för att visa upp rankingpoäng av ledande konkurrenter. Elever kan se sina spelifieringspoäng med resultattavlan.

Klicka på på elevens startsida **[!UICONTROL Gamification]** från den vänstra rutan. Klicka på länken Resultattavla för att se resultatlistan. Den här funktionen gör det möjligt för elever att förstå hur de klarar sig mot en viss gruppmedlem. Det visar också deras rankingposition i förhållande till andra medlemmar i laget.

Några av funktionerna i Leaderboard för elever:

* Elever som är registrerade för en instans av ett utbildningsprogram kan se varandras poäng om spelifiering har aktiverats för den instansen.
* Klicka **[!UICONTROL Add colleagues]** för att inkludera teammedlem som du vill jämföra med. Teammedlemmens profilbild läggs till i tidslinjens skala högst upp på resultatlistan. Tidslinjens skala visar punkterna i början och flyttar positionen åt höger när du uppnår fler punkter än teammedlemmarna. Du kan bara jämföra det med andra medlemmar i samma grupp.
* **Användargrupper:** Du kan när som helst välja de teammedlemmars profiler som du vill jämföra din ranking med genom att använda **[!UICONTROL Rank Me With]** alternativ. I fältet Välj användargrupper skriver du in och väljer gruppen. Listan över alla teammedlemmar tillsammans med deras senaste poäng visas nedan. Både interna och externa användare kan se listan, men endast interna användare kan söka efter andra interna elever.

* I dialogrutan Personer runt din rang visas dessutom namnen på de teammedlemmar som är ovan, under eller på samma nivå som du.
* När en extern användare konverteras till en intern användare uppdateras tidslinjen automatiskt.

## Poäng för konsekvent lärande

Adobe Learning Manager introducerar en ny spelifieringsuppgift som uppmuntrar användare att använda utbildningsplattformen konsekvent och engagera sig i utbildningsaktiviteterna. För att stödja den här uppgiften kan administratören nu konfigurera en ny regel som tilldelar poäng om eleven utför utbildningsaktiviteter i 1, 2, 3 eller 4 dagar under en vecka, månad eller ett kvartal.

Observera att spelifieringspoängen för denna regel tilldelas en gång var 24:e timme. Om en elev till exempel utför en utbildningsaktivitet idag klockan 08.00 Pacific Standard Time (PST) och har fått spelifieringspoäng för idag, kommer han eller hon imorgon endast att komma i fråga för spelifieringspoäng om han eller hon utför en utbildningsaktivitet någon gång efter klockan 08.00 PST.

Följande aktiviteter betraktas som utbildningsaktiviteter:

* Förbrukar en kurs, utbildningsväg eller certifiering i fluidic-spelaren.
* Hämtar ett arbetsstöd.
* Hämtar en bilaga.
* Lägger till anteckningar.
* Gå till instrumentpanelen för socialt lärande.
* Kommentera instrumentpanelen för social utbildning.
* Inlägg på instrumentpanel för social utbildning.

**Spelifieringspunkter för att ge feedback om L1 och L3 och stjärnbetyg**

Adobe Learning Manager gör det nu möjligt för en administratör att aktivera ett spelifieringskriterium som tilldelar poäng till användare när de ger L1-feedback, L3-feedback och ett stjärnbetyg.

![](assets/feedback-rating.png)

*Visa feedback och betygsättning*

Den här funktionen uppmuntrar användarna att aktivt ge feedback, vilket gynnar både elever och administratörer som nu bättre förstår elevens synvinkel och kan bättre utvärdera effektiviteten av en kurs.

## Uppgifter {#tasks}

Det finns fem spelifieringsuppgifter för elever. Du kan visa spelifieringspunkter i cirkeln i det övre högra hörnet av fönstret på elevens startsida. Klicka på Spelification om du vill visa allokeringen för varje uppgift.

Systemet visar sidan Spelifiering som visar alla elevens uppgifter och poäng:

>[!NOTE]
>
>Spelifieringspunkter inom en viss uppgift är inte kumulativa. Men poängen läggs till i elevkontot kumulativt om eleverna kommer över dessa punkter med olika uppgifter.
>
>När administratörer tilldelar kurser till poäng måste de se till att eleverna får poängen gradvis.

**För snabb elev**

Denna uppgift är tillämplig när en elev slutför vissa kurser inom en månad/kvartal/år. Denna uppgift är att uppmuntra snabba elever.

Du kan se följande möjliga scenarier:

1. När elever slutför två kurser inom en månad/kvartal/år får de 20 poäng.
1. När elever slutför fyra kurser inom en månad/kvartal/år får de 100 poäng.
1. När eleverna slutför åtta kurser får de 300 poäng.
1. När eleverna slutför tio kurser får de 500 poäng.

>[!NOTE]
>
>Administratören kan ändra tidsperioden och antalet kurser som krävs för att slutföra för att tjäna motsvarande poäng.
>
>Inom en uppgift ges inte poäng till elever kumulativt. Anta t.ex. att en elev slutför en kurs och får 20 poäng. När elever slutför två kurser får de 100 poäng men de befintliga 20 poängen beaktas inte.

**För elev med egenhanterad utbildning (a)**

Denna uppgift är tillämplig när elever registrerar sig för föreskrivet antal kurser och slutför inom en månad/kvartal/år. I det här fallet kan administratören aktivera den här uppgiften för att tilldela poäng och uppmuntra dem.

Möjliga scenarier:

1. När elever registrerar sig för en kurs inom en månad/kvartal/år får de 50 poäng.
1. När elever registrerar sig för två kurser under en månad/kvartal/år får de 150 poäng.

>[!NOTE]
>
>Administratören kan ändra tidsperioden och antalet kurser.

**För elev med egenhanterad utbildning(b)**

Denna uppgift kan utföras när elever registrerar sig och slutför fler kurser än vad som krävs för att slutföra under en månad/kvartal/år. I sådana fall kan administratören aktivera uppgiften för att tilldela poäng och uppmuntra dem.

Möjliga scenarier för elever att registrera sig för kurser utöver de tilldelade kurserna:

1. När elever registrerar sig för en kurs inom en månad/kvartal/år får de 20 poäng.
1. När elever registrerar sig för två kurser under en månad/kvartal/år får de 100 poäng.
1. När elever registrerar sig för tre kurser inom en månad/kvartal/år får de extra 300 poäng.
1. När elever registrerar sig för fyra kurser under en månad/kvartal/år får de extra 500 poäng.

>[!NOTE]
>
>Administratören kan ändra tidsperioden och antalet kurser. Det tredje scenariot kan till exempel ändras till fem kurser i stället för tre för att ge 80 poäng.

**För förkovran (a)**

Denna uppgift är tillämplig när elever slutför ett antal kompetenser. Administratören kan välja den här uppgiften för att uppmuntra elever att få så många kompetenser som möjligt.

Möjliga scenarier för förkovran i kompetenser:

1. När elever uppnår en kompetens får de 100 poäng.
1. När eleverna uppnår två kompetenser får de 300 poäng.
1. När eleverna uppnår tre kompetenser får de 600 poäng.
1. När eleverna uppnår fyra kompetenser får de 900 poäng.

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
>Tidsperioden gäller inte för den här uppgiften. Administratören kan ändra antalet nivåer för varje scenario. Om elever uppnår en högre nivå och sedan uppnår en lägre nivå av en kompetens får de poäng endast för den högre nivån.

**Poäng för tidigt slutförande**

Denna uppgift är tillämplig för elever när de blir de första N eleverna att slutföra kursen.

Möjligt scenario:\
När en elev blir en av de första tio eleverna som slutför kursen får han/hon 100 poäng.

**Poäng för slutförande i tid**

Denna uppgift är tillämplig för elever när de slutför en kurs inom ett angivet antal dagar före deadline för slutförande av kurs.

Möjligt scenario:\
När en elev slutför en kurs inom 10 dagar i början av kursen får hen 100 poäng.

**Uppnå nivåer**

Elevstatus på Nivå visas längst upp till höger på sidan i en cirkel, på sidan Mina kurser. Elever kan uppnå följande olika nivåer baserat på antalet poäng som uppnås under utbildningsperioden:

1. Brons - när eleven uppnår 1500 poäng.
1. Silver - när eleven uppnår 2 500 poäng.
1. Guld - när eleven uppnår 3000 poäng.
1. Platina - när eleven når 5000 poäng.

## Vanliga frågor {#frequentlyaskedquestions}

**1. Hur ser man resultattavlan som en elev?**

I elevappen klickar du på **[!UICONTROL Social Learning]**. Den sociala resultattavlan visas längst ned till höger på sidan.
