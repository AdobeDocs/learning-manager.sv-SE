---
description: Lär dig hur du får åtkomst till, hämtar och tolkar feedbackrapporten i Adobe Learning Manager. Förstå rapportkolumner, frågetyper, chefs- och elevsvar och hur feedbackinsikter stöder utvärdering av utbildning och kontinuerlig förbättring.
jcr-language: en_us
title: Feedbackrapport i Adobe Learning Manager
source-git-commit: e0553621dd67338d2433bb1f82af43cacc2d8b8c
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 5%

---


# Feedbackrapport

## Översikt

Feedbackrapporten i Adobe Learning Manager samlar in både Nivå 1 (elevfeedback) och Nivå 3 (chefsfeedback) efter att elever har slutfört utbildningsobjekten. I denna rapport ges en strukturerad översikt över både subjektiva och objektiva svar från elever och chefer.

Rapporten spårar elevdetaljer som namn, e-post, feedback, formulärnamn, version och språk och samlar in svar på administratörsdefinierade frågor. Den registrerar också elevens val för varje fråga (till exempel Instämmer helt, Instämmer eller Instämmer inte).

## Syfte och fördelar

* Ger användbara insikter för att förbättra kurskvaliteten och utbildningseffektiviteten i stort.
* Förfina navigerings-, plats- och leveransmetoder baserat på direkt feedback från användare.

## Användningsfall

* **Identifiera snabbt innehållsproblem**: Administratörer kan upptäcka låga betyg eller upprepade negativa kommentarer och uppdatera utbildningsobjekten utan att vänta på supportärenden eller eskaleringar.
* **Mät utbildningens effektivitet**: Teamen kan jämföra elevfeedback från flera kurser eller versioner för att förstå vilka utbildningsobjekt som fungerar bra och som kan behöva omarbetas.
* **Spåra elevens engagemang med feedbackformulär**: Administratörer kan se hur många elever som svarar på eller hoppar över frågor, vilket hjälper dem att förfina feedbackformulär för att förbättra svarskvaliteten och slutförandegraden.

## Så här hämtar du feedbackrapporten

1. Logga in på Adobe Learning Manager som administratör.
2. Välj **[!UICONTROL Reports]** från den vänstra navigeringsmenyn.
   ![](assets/select-report.png)
   _På administratörens startsida visas alternativet Rapporter markerat för hämtning av rapporter_

3. Välj **[!UICONTROL Custom Reports]** i Rapporter och välj sedan **[!UICONTROL Excel Reports]**.
4. Välj **[!UICONTROL Feedback Report]**.
   ![](assets/select-feedback-report.png)
   _I avsnittet Anpassade rapporter visas alternativet att välja Feedbackrapport för att komma åt elevens och chefens feedbackdata_

5. Välj **[!UICONTROL All Trainings]** eller **[!UICONTROL Selected Trainings]** och datumintervallet. Om du väljer det andra alternativet kan du lägga till högst 10 kurser eller utbildningsvägar och generera deras feedbackrapport. Dessutom kan du generera rapporten i upp till ett år.
   ![](assets/feedback-report.png)
   _Konfigurera feedbackrapporten genom att välja utbildningsomfattning, ange datumintervall och välja översättningsalternativ innan du hämtar_

6. Välj det språk du vill översätta feedback om L1 till. Objektiva frågor och deras svar översätts till det valda språket när den språkversionen är uttryckligen definierad. Endast de subjektiva frågor som är uttryckligen definierade på det valda språket visas i rapporten.  Svar på subjektiva frågor skulle vara på det ursprungliga svarsspråket.
7. Välj **[!UICONTROL Download]** för att hämta rapporten.

## Vad innehåller feedbackrapporten?

Detta är standardkolumnerna i rapporten på kontonivå:

| Kolumn | Beskrivning |
|----|----|
| Typ av feedback | Anger om feedback kommer från eleven (L1) eller chefen (L3) |
| Användarnamn | Namnet på den elev som slutförde utbildningen |
| Mejladress till användare | Elevens e-postadress |
| Utbildnings-ID | En systemgenererad unik identifierare som tilldelas varje utbildningsobjekt (kurs, certifiering eller utbildningsväg) |
| Utbildningsnamn | Namnet på utbildningsobjektet som feedback har skickats för |
| Utbildningsinstans | Instansnamn på utbildningen (för kurser i flera instanser) |
| Utbildningstyp | Typ av utbildning (kurs, certifiering, utbildningsväg) |
| Typ av feedbackformulär | Typ/kategori av feedbackformulär som används (t.ex. blandade kurser, kurser i egen takt och klassrumskurser) |
| Namn på feedbackformulär | Namn på feedbackformuläret |
| Feedbackversion | Versionsnummer för feedbackformuläret |
| Nuvarande chef | Namn på elevens chef |
| Mejladress till nuvarande chef | E-postadress till elevens chef |
| Datum för slutförande | Det datum då eleven slutförde utbildningen |
| Datum för feedback | Det datum då eleven skickade in feedbacken |
| Ursprungligt språk för L1-feedback | Det språk som eleven ursprungligen skickade in feedback om L1 på |
| L3 Likert-skala fråga 1 | Mäter elevens resultat efter avslutad utbildning med hjälp av en bedömningsskala |
| L3 Likert-skalesvar 1 | Chefens svar på den här Likert-skalafrågan |
| FRITEXTFRÅGA 1 FÖR L3 | Fritextfråga har lagts till i L3-feedbackformuläret för chefer. Kan konfigureras som valfritt eller obligatoriskt |
| L3 fritextsvar 1 | Chefens svar på fritextfrågan |

Följande kolumner visas i rapporten på kontonivå baserat på de fyra typer av frågor som lagts till i feedbackformuläret:

| Kolumn | Beskrivning |
|---|---|
| Kurseffektivitet | Den fördefinierade frågan om kurseffektivitet som visas i formuläret |
| Svar på kurseffektivitet | Elevens svar på frågan om kurseffektivitet |
| NPS-fråga 1 | Första Net Promoter Score-frågan |
| NPS-intervall 1 | Använd bedömningsskala (t.ex. 0 till 10) |
| NPS-svar 1 | Elevens betyg för NPS fråga 1 |
| Likert fråga 1 | Första Likert-skalafråga |
| Likert svar 1 | Svar på Likert-fråga 1 |
| Textfråga 1 | Den första öppna frågan/textfrågan i formuläret |
| Textsvar 1 | Elevens svar på textfråga 1 |


>[!NOTE]
>
>Rapporten på kontonivå innehåller även alla aktiva fält som konfigurerats för elever.

Följande kolumner visas i rapporten Nivå för utbildningsobjekt:

| Kolumn | Beskrivning |
|---|---|
| Elev | Elevens namn |
| E-post | Elevens e-postadress |
| Namn på feedbackformulär | Namn på feedbackformuläret |
| Feedbackversion | Versionsnummer för feedbackformuläret |
| Elevspråk | Språk som valts av eleven |

>[!NOTE]
>
>Nivårapporten för utbildningsobjekt innehåller även de frågor som lagts till i feedbackformuläret. Varje fråga visas som en kolumnrubrik, och elevens svar på dessa frågor visas på motsvarande rader nedan.
