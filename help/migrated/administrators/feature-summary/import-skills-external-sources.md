---
jcr-language: en_us
title: Importera kompetenser från externa källor
description: Importera kompetenser från innehållsleverantörer, t.ex. LinkedIn och Go1, genom att använda respektive kopplingar.  De importerade kunskaperna läggs till i de administratörsdefinierade kunskaperna i Learning Manager och kommer att vara tillgängliga för författare under arbetsflödet för att skapa kursen.
contentowner: saghosh
exl-id: 3bcd8fc6-16e4-4f66-a5c6-15b3d606f0c2
source-git-commit: 64d63c46fc0f9e5daada1eb391e720dc45fbab89
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# Importera kompetenser från externa källor

Importera kompetenser från innehållsleverantörer, t.ex. LinkedIn och Go1, genom att använda respektive kopplingar. Denna förbättring är en del av målet mot Learning Managers förmåga att integrera med externa Skills Clouds och Talent Management Systems. De importerade kunskaperna läggs till i de administratörsdefinierade kunskaperna i Learning Manager och kommer att vara tillgängliga för författare under arbetsflödet för att skapa kursen. Förbättringar har också gjorts i kompetenssökningsfunktionen på hela plattformen för att ge en bättre sökupplevelse när kontot har ett stort antal färdigheter.

## Konfigurera färdighetsimport

Följ stegen i proceduren för att aktivera kunskapsimport i kontot.

1. I Admin-programmet väljer du **Inställningar** i den vänstra rutan.
1. Välj **Allmänt**.
1. I dialogrutan **Import av kompetenser** -sektionen väljer du **Aktivera**. Om det här alternativet är aktiverat kan du välja en extern källa för att importera kunskaper. När de har aktiverats för all efterföljande import av utbildningsresurser importeras kunskaperna till kunskapsdatabasen för nyligen importerade objekt. Kunskaperna för befintliga utbildningsresurser kan importeras till kunskapsdatabasen en gång och för att köra den första körningen ska du kontakta din CSM.
1. Välj en innehållsleverantör i listrutan.

Du som är administratör kan bara importera kunskaper från en kompetenskälla.

### Standardkompetensnivå

Standardkompetensnivån är en och tillgodoräknandet är 10 efter att kunskaperna har migrerats. Administratören kan ändra krediten senare.

Du kan inte redigera namnet på kompetensen, beskrivningen och lägga till nivåer i externa kompetenser. Du kan dock lägga till domän, märken och redigera krediter.

### Standardkursfärdigheter och -poäng

När du har importerat kunskaper läggs de till i utbildningsresurserna som importerats från källan som valdes som kunskapskälla. Om din kompetenskälla till exempel var LinkedIn Learning har alla utbildningsresurser som importeras från LinkedIn Learning de färdigheter som den tillhandahåller. När de importeras till utbildningsresurser ger varje utbildningsresurs automatiskt 10 krediter. Kontakta din CSM om du vill ändra detta.

#### Rapportering

Kolumnen **Källa** med values- internal, LinkedIn Learning, Go1, som anger källan till kunskapsimport.

De nyligen tillagda kunskaperna kommer att vara överst.

På sidan Kursinställningar visas kolumnen **Tilldelad av** innehåller värden, intern och innehållsleverantör.


## Arbetsflöde för integreringsadministratör

Integreringsadministratören överför CSV-filerna (kompetens, kompetensnivå och kurs) och migrerar sedan kurserna till kontot. När administratören till exempel har valt LinkedIn Learning kan integrationsadministratören schemalägga en aktivitet där både färdigheter och nivåer importeras till Adobe Learning Manager.

## Exportera kompetenserna

Som administratör

1. Välj **Kompetenser** i den vänstra rutan.
1. Välj källa för valfri kompetens. Du kan se kurser, arbetsstöd, registrerade elever och instruktörer för kursen.

### Redigera en kompetens

Välj en kompetens. I dialogrutan **Redigera en kompetens** kan du inte redigera namnet på och beskrivningen av kompetensen. Du kan dock lägga till kompetensdomäner och ett utmärkelsetecken för kompetensen.
