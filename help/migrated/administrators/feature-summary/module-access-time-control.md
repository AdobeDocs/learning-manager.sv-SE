---
description: Ange ett tidsfönster då elever tillåts starta en modul.
jcr-language: en_us
title: Kontroll av modulåtkomsttid
contentowner: mmanuel
source-git-commit: 6423fd5c0853705a28c6c67b6936d93e68cbca20
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 0%

---

# Kontroll av modulåtkomsttid

## Översikt

Förbättringen gör att författare och administratörer i Adobe Learning Manager kan definiera ett tidsfönster då elever tillåts starta en modul. Utanför det konfigurerade start-/slutfönstret syns modulen i kursstrukturen, men eleverna kan inte initiera den.

Den här funktionen är viktig för användare som behöver bättre kontroll över när visst innehåll blir tillgängligt eller inte borde initieras på t.ex. schemalagda program, kohortbaserad utbildning eller tidskänsliga övningar.

## Nyheter

Författare kan nu på modulnivå inom en kurs konfigurera ett startdatum/tid och ett slutdatum/tid som styr när elever tillåts starta den modulen. I detta fönster fungerar modulen som vanligt; före starttiden eller efter sluttiden ser eleven modulen i kurskonturen men kan inte starta den.
Konfigurationen visas i användargränssnittet för kursredigeringen som ytterligare schemaläggningskontroller för specifika modultyper, till exempel innehåll, frågeformulär eller aktiviteter för eget tempo. Administratörer kan använda dessa kontroller för att skapa moduler som öppnas i faser eller för att förhindra sena starter i program där innehåll måste förbrukas inom en angiven tidsram.

## Viktiga fördelar

Den största fördelen är möjligheten att styra när moduler är tillgängliga. Utbildningsteam kan synkronisera modultillgänglighet med verkliga evenemang, som lanseringar av nya produkter, deadlines och interna program. Detta säkerställer att eleverna slutför nödvändigt innehåll innan de får tillgång till senare moduler.
Till exempel kan kohort 1 endast komma åt modul 2 under vecka 2, medan modul 3 förblir låst fram till vecka 3, vilket eliminerar behovet av att manuellt dölja och visa innehåll eller skapa separata kursversioner.
Detta förbättrar elevupplevelsen: i stället för att ta itu med moduler som tekniskt går att komma åt men som inte borde vara det då (eller redan borde vara slutförda), ser eleverna en kursstruktur där de moduler de får starta tydligt överensstämmer med det avsedda schemat.

## Användningsfall

**Kohortbaserat aktiveringsprogram**: I det här programmet öppnas en ny modul varje vecka. Innehållet för Vecka 1 är tillgängligt direkt, medan Vecka 2 är synlig men kan inte startas förrän ett visst datum. Vecka 3 följer samma grindningsprocess. Elever kan se hela utbildningsvägen, men systemet styr när de faktiskt kan påbörja varje steg.
**Tidsbunden produkt- eller kampanjutbildning**: Marknadsförings- eller produktteam kan skapa en utbildningsmodul som endast ska nås när en kampanj är aktiv eller när en viss version av en produkt fortfarande är tillgänglig. Detta startfönster ser till att eleverna inte påbörjar en modul om en avvecklad produktversion efter den angivna sluttiden.
**Bedömnings- eller tentamensmiljöer**: Organisationer kan öppna en modul (t.ex. ett test) för ett kort, väldefinierat fönster (t.ex. &quot;du kan starta tentamen när som helst mellan 9:00 och 12:00 ett visst datum&quot;). Elever kan inte påbörja tentamen utanför det fönstret, vilket stödjer rättvis schemaläggning över tidszoner och kohorter.

## Ange åtkomsttid för modul

1. Logga in i Adobe Learning Manager som författare.
2. Gå till avsnittet **Utbildning** > **Kurser**. ALM visar en lista med kurser.![alt-text](/help/migrated/administrators/feature-summary/assets/module-access-time1.png)
3. Välj kursen som du vill ställa in begränsningen för.
4. Välj **instanser**. ALM visar en lista med instanser.
5. Välj **Moduler** i instansavsnittet som du vill ange åtkomstgränsen för. Knappen **Redigera** visas.![alt-text](/help/migrated/administrators/feature-summary/assets/module-access-time2.png) ![alt-text](/help/migrated/administrators/feature-summary/assets/module-access-time3.png)
6. Välj **Redigera**. De relevanta avsnitten som hör till modulen öppnas längst ned på sidan.![alt-text](/help/migrated/administrators/feature-summary/assets/module-access-time4.png)
7. För varje avsnitt väljer du ett från-datum, ett från-datum, ett till-datum och en till-tid.
8. Välj **Spara**. ALM visar meddelandet &quot;Mappningen har sparats.&quot;










