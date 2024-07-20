---
jcr-language: en_us
title: CSS-mall för textredigerare
description: CSS-mall för textredigerare
contentowner: saghosh
preview: true
source-git-commit: 9325abb9cda8c8a019c9d72c1944a8284f38f83e
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---



# CSS-mall för textredigerare

## Varför krävs CSS?

RTF består av HTML-kod. Om markeringen återges i befintligt skick kommer standardformatet att användas i webbläsaren. Det här passar ofta inte så bra ihop med företagets stilriktlinjer. En CSS krävs för att uppfylla riktlinjerna.

## Standardformat

Den bifogade CSS-formatmallen innehåller den formatering som används av Learning Manager. Formateringen ändras med tanke på de flesta användningsfallen. Hämta den bifogade CSS-filen och importera den till webbappen enligt dina konventioner och bygg system. De CSS-klasser som definierats har namnutrymmen under klassen ql-editor och påverkar inte dina befintliga format.

## Anpassa format

Standardstilen kanske inte uppfyller alla behov. Anpassningarna kan göras genom att åsidosätta den CSS-kod som anges. All formatering lindas under ql-editor som underordnade väljare. Följande klasser används:

* **Indrag**: li.ql-indent-$number. $number varierar från 1-9
* **storlek**: ql-size-small, ql-size-large, ql-size-large
* **justering**: ql-align-center, ql-align-adjust, ql-align-right
* **färg**: ql-färg-$färg. $color = vit, röd, orange, gul, grön, blå, lila
* **bakgrund**: ql-bg-$color. $color = svart, röd, orange, gul, grön, blå, lila
* **html-taggar**: p, ol, ul, pre, blockquote, h1, h2, h3, h4, h5, h6

[CSS-fil som ska användas för anpassning.](assets/ql-headless.css)
