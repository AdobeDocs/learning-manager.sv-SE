---
description: Läs mer om Experience Builder, ett felfritt/lågkodsverktyg i Adobe Learning Manager som administratörer kan använda för att designa och publicera varumärkta, användarvänliga sidor utan expertkunskaper.
jcr-language: en_us
title: Experience Builder i Adobe Learning Manager
source-git-commit: b1225d4c1c322a75d97c813b0d97eb3229ffd35c
workflow-type: tm+mt
source-wordcount: '993'
ht-degree: 0%

---


# Översikt

Experience Builder är ett no-code-/low-code-verktyg i Adobe Learning Manager som hjälper dig att skapa anpassade utbildningsportaler. Det gör att du kan designa varumärkta, användarvänliga utbildningsportaler utan att behöva tekniska färdigheter eller omfattande kodningskunskaper.

Med Experience Builder kan administratörer enkelt skapa sidor, menyer och widgetar och leverera personliga utbildningsupplevelser som är anpassade för deras målgrupp

Många organisationer kämpar med att anpassa sina utbildningsportaler utan teknisk hjälp eller dyra systemintegratörer. De vill ha portaler som matchar deras varumärke, levererar riktat innehåll och anpassar sig till olika elevgrupper samtidigt som de är snabba och enkla att skapa.

Experience Builder är ett no-code-/low-code-verktyg i Adobe Learning Manager som hjälper dig att skapa anpassade utbildningsportaler. Det gör att du kan designa varumärkta, användarvänliga utbildningsportaler utan att behöva tekniska färdigheter eller omfattande kodningskunskaper.
Med Experience Builder kan du skapa nya sidor, menyer och widgetar som ger din målgrupp anpassade utbildningsupplevelser snabbt och enkelt. Med Experience Builder kan du snabbt skapa nya sidor, menyer och widgetar som ger din målgrupp personliga utbildningsupplevelser.

## Problemet som Experience Builder löser

I Experience Builder hanteras de vanliga utmaningar som organisationer ställs inför när de anpassar sina utbildningsportaler utan större teknisk hjälp eller dyra systemintegratörer. Det överbryggar gapet mellan två primära alternativ:

* Den färdiga standardupplevelsen som erbjuder begränsad anpassning och kan få alla utbildningsportaler att se likadana ut.
* En fjärradministrerad implementering som möjliggör helt anpassade portaler men som innebär stora utmaningar, bland annat lång tid till marknaden (normalt 3-6 månader), beroende av ett utvecklingsteam och höga kostnader.

Experience Builder ger en medelväg och gör det möjligt att skapa portaler som passar varumärket och unika inlärningsresor utan de höga kostnader och den utveckling som krävs för ett fjärradministrerat tillvägagångssätt.

## Viktiga fördelar med att använda Experience Builder

Funktionen att använda sidor, widgetar eller menyer ger flera viktiga fördelar:

* **Enkel anpassning**: Du kan designa portaler som matchar ditt varumärke exakt med anpassade sidhuvuden, sidfötter, logotyper och layouter. Möjligheten att mata in anpassade HTML, CSS och JavaScript ger avancerad kontroll för en helt varumärkesanpassad upplevelse.
* **Personligt lärande**: En viktig fördel är möjligheten att kunna erbjuda olika upplevelser för olika elever. Du kan konfigurera sidor och menyer för specifika användargrupper (t.ex. säljteam, designer eller tekniker) och se till att de bara ser innehåll som är relevant för dem. Detta är idealiskt för att skapa riktade mikroinlärningskampanjer för specifika team eller tidsperioder.
* **Inget gränssnitt med kod/låg kod**: Administratörer kan skapa utbildningsupplevelser via ett guidat visuellt gränssnitt i stället för att skriva kod. Med den här metoden kan administratörer skapa och hantera avancerade portaler utan tekniska färdigheter eller omfattande kodningskunskaper.
* **Global och mobilanpassad**: Experience Builder stöder skapandet av flerspråkiga sidor för att tillgodose olika globala målgrupper och är utformat för att vara mobilvänligt. Det ger en smidig upplevelse för elever på stationära datorer, telefoner och surfplattor.

## Vanliga användningssätt

Experience Builder kan användas för olika utbildningsscenarier som involverar interna medarbetare och externa användare.

* **Rollbaserade utbildningsportaler**: Organisationer med specifika behov av utbildning på avdelningar, t.ex. ett ekonomiskt företag med separata sälj- och kundteam, kan skapa särskilda utbildningssidor för varje grupp för att säkerställa att innehållet är mycket relevant.
* **Evenemangsspecifika utbildningssidor**: Du kan skapa tillfälliga specialsidor för företagsevenemang som ett teknikertoppmöte eller en försäljningsstart. Dessa sidor kan innehålla sessionsinformation, talarlistor och en händelsekalenderwidget, och kan endast rikta sig till det relevanta teamet under en viss tid innan de återgår till standardportalupplevelsen.
* **Kundakademier**: Med Experience Builder kan byråer skapa kundinriktade akademier som återspeglar deras varumärkesidentitet och få en anpassad upplevelse utan den tid och kostnad som förknippas med en huvudlös konstruktion.

## Autentiserade arbetsflöden för den externa portalen

Kundinriktade akademier som byggts med Experience Builder hanteras helt inom Adobe Learning Manager. Dessa portaler använder Adobe Learning Manager inbyggda system för autentisering, behörigheter och säkerhet.

Varje extern elev måste logga in på Adobe Learning Manager och vara medlem i minst en användargrupp. För närvarande stöder Experience Builder inte icke-autentiserade eller offentliga portaler. För alla personliga upplevelser måste eleverna logga in på Adobe Learning Manager.

Administratörer kan använda alternativet Experience Builder **[!UICONTROL Menu]** för att tilldela specialbyggda sidor som landningssidor för specifika användargrupper. När elever från den gruppen loggar in dirigerar Adobe Learning Manager dem automatiskt till den tilldelade startsidan, vilket skapar en personlig och varumärkesanpassad upplevelse för den målgruppen, t.ex. kundutbildning, partneraktivering eller introduktion.

### Krav och begränsningar

* Autentisering krävs: Anpassat innehåll, anpassade sidor och menyer är endast tillgängliga för autentiserade användare i Adobe Learning Manager.
* Tilldelning av användargrupper: Elever måste läggas till i rätt användargrupper för att få åtkomst till sina angivna målsidor och menyer.
* Gruppbaserade målsidor: Inställningen för landningssida gäller alla medlemmar i en användargrupp, vilket säkerställer enhetliga upplevelser för liknande målgrupper.
* Anpassningsomfång: Experience Builder stöder omfattande anpassningar av användargränssnitt och layout med hjälp av widgetar, HTML och iFrames. Avancerade integreringar som e-handel, federerad enkel inloggning eller externa dataanslutningar kan dock kräva en hybrid eller fjärradministrerad implementering.

### Arbetsflöde för konfiguration av extern portal

* Definiera användargrupper: Skapa eller identifiera grupper i ALM som representerar din externa målgrupp (t.ex. kunder, partner eller distributörer). Mer information om användargrupper finns i [Användargrupper i Adobe Learning Manager](/help/migrated/administrators/feature-summary/user-group.md).
* Tilldela elever i grupper: Lägg till varje extern elev i rätt användargrupp så att de dirigeras till rätt portalupplevelse efter inloggning.
* Designportalsidor: Använd Experience Builder för att skapa varumärkta sidor med Adobe Learning Manager-widgetar, HTML- och iFrame-komponenter. Visa [Skapa en anpassad sida i Experience Builder](/help/migrated/administrators/feature-summary/experience-builder/create-a-page.md) om du vill ha mer information.
* Konfigurera menyer och landningssidor: I Menu Creator tilldelar du varje användargrupp en unik meny och anger dess anpassade portalsida som landningssida. Visa [Skapa en meny](/help/migrated/administrators/feature-summary/experience-builder/create-a-menu.md) om du vill ha mer information.
* Testa och Publish: Verifiera navigering, innehållssynlighet och siddirigering för varje användargrupp innan du publicerar portalen.
