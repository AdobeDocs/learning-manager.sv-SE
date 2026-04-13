---
description: Läs mer om elevens betygsutdrag
jcr-language: en_us
title: Ändringar i elevens betygsutdrag
source-git-commit: cd0737061029e75953fa23cf3d12409b1407772a
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---


# Ändringar av elevens betygsutdrag i aprilutgåvan

## Kolumnen Slutförandemetod

Kolumnen **Slutförandemetod** visar hur varje post i administratörens elevbetygsutdrag har slutförts.

**Värden:**

1. **Direkt** (för direkta slutföranden)
2. **Alternativ** (för slutföranden som uppnås via alternativa relationer)
3. **Alternativet har återkallats** (när alla alternativa slutföranden har återkallats på grund av retroaktiv inslutföring och relationsborttagning)

>[!NOTE]
>
>Den här kolumnen är inte synlig i elevens LT. Den är bara tillgänglig i admin LT för rapporterings- och spårningsändamål.

**Effekt**: Möjliggör tydliga granskningsspår, efterlevnadsspårning och genomskinlighet för administratörer angående hur en kurs har slutförts.

## Alternativ spårning vid slutförande i elevens betygsutdrag

Alternativa slutföranden gör det möjligt för elever att få tillgodoräkna sig slutförande för en målkurs eller utbildningsväg när de har slutfört en motsvarande källkurs eller kurs, baserat på etablerade relationer.

I elevens betygsutdrag (LT) påverkar alternativa slutföranden tre befintliga kolumner: **Status**, **Slutförandedatum** och **Slutförandekälla**.

- **Status**: Statusen kan vara **Slutförd** även om eleven inte har slutfört målkursen eller målsökvägen direkt på grund av att kursen har slutförts alternativt. Andra statusar (**Inte påbörjat**, **Pågår**, **Avregistrerad**) påverkas inte.
- **Slutförandedatum**: Datumet ärvs från källkursen eller sökvägen om slutförandet inte har slutförts. Om eleven senare slutför målet direkt uppdateras datumet för att återspegla det direkta slutförandet.
- **Källa för slutförande**: Hämtar utbildnings-ID för de källkurser eller sökvägar som tillhandahöll den alternativa slutförandet. Flera aktiva källor visas som kommaavgränsade ID:n. Om källor återkallas återstår endast aktiva. Om det finns flera källor används det tidigaste slutförandedatumet.

**Effekt**: Alternativa slutföranden minskar den manuella avstämningen, automatiserar framstegsspårning i utbildningsvägar och certifieringar samt stöder kompatibilitetskrav.

>[!NOTE]
>
>Elevens betygsutdrag visar inte kolumnen **Slutförandemetod**. Den här kolumnen är endast tillgänglig i adminelevens betygsutdrag.

## Logik för slutförandedatum för alternativ

Kolumnen **Slutförandedatum** i elevens betygsutdrag används för både direkta och alternativa slutföranden.

- Vid alternativa fullgöranden visar datumet när eleven slutförde källkursen eller sökvägen.
- Om eleven senare slutför målet direkt, uppdateras slutförandedatumet till det direkta slutförandedatumet.
- Ingen ny kolumn introduceras för alternativa slutförandedatum.
- Om flera källor anger alternativ slutförande används det tidigaste aktiva slutförandedatumet.
- Om en källa återkallas (med retroaktiv inslutförande aktiverat) uppdateras datumet till nästa tidigaste aktiva källa eller rensas om inga aktiva källor finns kvar.

**Effekt**: Garanterar korrekt historikspårning och konsekvent rapportering, även när alternativa relationer ändras över tid.

## Återkallade alternativa slutföranden

Återkallade alternativa slutföranden inträffar när alla källrelationer för en målkurs eller utbildningsväg tas bort, förutsatt att retroaktiv inslutföring är aktiverad.

### Utlösarvillkor

- Retroaktiv slutförande måste aktiveras på kontonivån.
- Återkallandet sker bara när **alla** aktiva källrelationer tas bort.
- Om minst en källa finns kvar, kvarstår den alternativa slutföringen och den slutförda källkolumnen uppdateras därefter.

### Effekt på elevens betygsutdrag

- **Status**: Om alla alternativa slutföranden återkallas och det inte finns något direkt slutförande, uppdateras statusen (till exempel från **Slutfört** till **Inte påbörjat** eller **Pågår**).
- **Slutförandedatum**: Rensas om inga aktiva källor finns kvar och inget slutförande sker direkt.
- **Slutförandekälla**: Uppdaterad för att ta bort återkallade källor; rensad om alla källor återkallas.

Om eleven har ett direkt slutförande påverkar inte återkallande av alternativa källor slutförandestatus eller slutförandedatum.

>[!NOTE]
>
>Om flera källor har tillhandahållit alternativ slutförande och endast vissa återkallas, återspeglar transkriptionen återstående aktiva källor och deras tidigaste slutförandedatum. Om alla källor återkallas och det inte finns något direkt slutförande förlorar eleven slutförandestatusen för målet.

## Förbättrad rapportering för granskningskommentarer

Granskningskommentarer från checklistmoduler ingår nu i elevens betygsrapport under en kolumn med nytt namn, **Granskarens kommentarer**.

**Effekt**: Gör det möjligt för elever och administratörer att visa konsoliderad feedback, förbättra transparensen och stödja prestandautvärdering.

## Förbättrad beräkning av inlärningstid

Rapporten Elevens betygsutdrag använder nu förfinad logik för att skilja mellan aktiv och inaktiv inlärningstid baserat på användaraktivitet och webbläsarens flikfokus.

**Effekt**: Ger mer exakt mätning av elevengagemanget och stöd för efterlevnadsrapportering och analyser.
