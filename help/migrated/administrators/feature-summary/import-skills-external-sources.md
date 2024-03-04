---
jcr-language: en_us
title: Importera kompetenser från externa källor
description: Importera kompetenser från innehållsleverantörer, t.ex. LinkedIn och Go1, genom att använda respektive kopplingar.  De importerade kunskaperna läggs till i de administratörsdefinierade kunskaperna i Learning Manager och kommer att vara tillgängliga för författare under arbetsflödet för att skapa kursen.
contentowner: saghosh
source-git-commit: fc77dad8f39d6d29c8ec74eb5ba137bf12ab7f8c
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---


# Importera kompetenser från externa källor

Importera kompetenser från innehållsleverantörer, t.ex. LinkedIn och Go1, genom att använda respektive kopplingar. Denna förbättring är en del av målet mot Learning Managers förmåga att integrera med externa Skills Clouds och Talent Management Systems. De importerade kunskaperna läggs till i de administratörsdefinierade kunskaperna i Learning Manager och kommer att vara tillgängliga för författare under arbetsflödet för att skapa kursen. Förbättringar har också gjorts i kompetenssökningsfunktionen på hela plattformen för att ge en bättre sökupplevelse när kontot har ett stort antal färdigheter.

## Konfigurera färdighetsimport

Följ stegen i proceduren för att aktivera kunskapsimport i kontot.

1. I Admin-programmet väljer du **Inställningar** i den vänstra rutan.
1. Välj **Allmänt**.
1. I dialogrutan **Import av kompetenser** -sektionen väljer du **Aktivera**. Om detta är aktiverat kan du välja en extern källa som du vill importera **Kompetenser**. Kunskaperna för befintliga utbildningsresurser importeras till databasen för kompetenser en gång under den första körningen. För all efterföljande import av utbildningsresurser importeras kunskaperna till kunskapsdatabasen endast för nyligen importerade objekt.
1. Välj en innehållsleverantör i listrutan.

## Arbetsflöde för integreringsadministratör

Integreringsadministratören överför CSV-filerna (kompetens, kompetensnivå och kurs) och migrerar sedan kurserna till kontot. När administratören till exempel har valt LinkedIn Learning kan integrationsadministratören schemalägga en aktivitet där både färdigheter och nivåer importeras till Adobe Learning Manager.

## Exportera kompetenserna

Som administratör

1. Välj **Kompetenser** i den vänstra rutan.
1. Välj källa för valfri kompetens. Du kan se kurser, arbetsstöd, registrerade elever och instruktörer för kursen.

### Redigera en kompetens

Välj en kompetens. I dialogrutan **Redigera en kompetens** kan du inte redigera namnet på och beskrivningen av kompetensen. Du kan dock lägga till kompetensdomäner och ett utmärkelsetecken för kompetensen.