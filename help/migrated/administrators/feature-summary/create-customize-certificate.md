---
title: Skapa och anpassa ett certifikat
description: Med anpassade certifikat i Adobe Learning Manager (ALM) kan administratörer och författare designa, hantera och utfärda anpassade certifikat för elever.
jcr-language: en-us
exl-id: 99e20f00-9f8f-477f-9416-24636ed23b87
source-git-commit: 13fbdb95129ba7612e8e42d3da88ef3c6784e729
workflow-type: tm+mt
source-wordcount: '2628'
ht-degree: 0%

---

# Anpassade certifikat i Adobe Learning Manager

## Introduktion

Anpassade certifikat i Adobe Learning Manager ändrar hur administratörer utformar, hanterar och levererar certifikat om slutförande.

Administratörer kan:

- Designa certifikat i en visuell redigerare i arbetsytans stil i stället för att skriva kod.
- Bifoga certifikat till kurser, utbildningsvägar och certifieringar med flexibla standardinställningar.
- Använd generativa bakgrunder med Adobe Firefly-teknik samtidigt som du tänker på varumärkes- och efterlevnadsbehov.
- Migrera från befintliga HTML-mallar och se till att de är kompatibla med tidigare elevposter.

Certifieringsprocessen följer den befintliga modellen för utmärkelsetecken och prestationer i Learning Manager, så elevbeteendet förblir bekant medan administratörer och supportteam lägger mindre tid på certifikatsåtgärder.

>[!NOTE]
>
>Certifikatfunktioner som använder generativ AI omfattas av kvoter. Gränsen är 10 000 förfrågningar per kund.

## Viktiga funktioner i anpassad certifiering

### Certifikatsdesigner (redigera i arbetsytans stil)

En dra och släpp-certifikatdesigner erbjuder en WYSIWYG-arbetsyta (what-you-see-is-what-you-get) där administratörer kan skapa och hantera designer utan HTML- eller CSS-kunskaper.

**Visuell redigering**

- Dra, placera, ändra storlek på, vänd och rotera text och bilder.
- Justera element (överst, nederst, till vänster, till höger), lägg underst eller lägg överst.
- Duplicera eller klona element för snabbare layoutarbete.

**Element som stöds**

- Textfält med funktioner för teckensnitt, färg, storlek och justering.
- Dynamiska platshållare (t.ex. elevens namn, kurs eller certifieringsnamn, datum, kontofält och aktiva användarfält där endast attribut med ett värde tillåts).
- Bilder, inklusive logotyper och märken, med manuell storleksändring som föredras framför automatisk passning för förutsägbar layout.

**Bakgrund och layout**

- Stående eller liggande orientering (fast efter skapandet).
- Bakgrunder som enfärgade bilder eller bilder med justerbar genomskinlighet.
- Bildgalleri med fördefinierade bilder och delade bakgrunder.
- Zoomreglage (50 %-150 %) och stödraster- eller fästjustering.

**Lokalisering**

- Stöd för flera språk där varje språk har sin egen layoutfil.
- När du lägger till en språkinställning kopieras dess layout från standardspråket och kan sedan anpassas.
- Listrutan Språk med förhandsgranskning per språk i designläge.

**Utkast och publiceringslivscykel**

- Spara konstruktioner som utkast; utkast kan inte användas för utfärdande.
- Efter publicering är designstrukturen låst. Vissa redigeringar kan kräva duplicering av designen i stället.
- Förhandsvisning i realtid av PDF för att kontrollera layouten före lanseringen.

### Mallkatalog och -lista

Sidan **Certifikatdesign** hjälper administratörer att hantera certifikatmallar i stor skala:

- Rutbaserad katalog med **publicerade** och **utkast** flikar.
- Sök efter certifikatnamn; filtrera efter **Orientering**.
- Åtgärder för varje design:
   - Duplicera (för varianter).
   - Ställ in som standard på nivån **Konto**, **Kurs**, **Utbildningsväg** eller **Certifiering**.
   - Ta bort eller inaktivera mallar som inte längre används.
- Stöd för tredjepartsleverantörsmallar som kan registreras och återanvändas.

### Flexibel konfiguration och arv

Administratörer kan konfigurera certifikat på flera nivåer:

**Standardinställningar på kontonivå**

- Ange en standardcertifikatdesign för alla nya utbildningsobjekt (LO).
- Standardvärdet fungerar som utgångspunkt. Befintliga LO:er ändras inte automatiskt när kontots standardvärden ändras.

**Åsidosättningar på instansnivå**

- Konfiguration på instansnivå för kurser, certifieringar och utbildningsvägar, inklusive:
   - Varumärkning per grupp (till exempel för olika regioner eller partnerkonton).
   - Olika certifikatutformningar för återkommande certifieringscykler.

**Certifikatupplösning och grundinställning**

När en elev slutför utbildningen väljer Learning Manager en design i följande ordning:

- LO-instanskonfiguration
- LO-konfiguration
- LO-standardmall
- Standardmall för konto

### Generativa bakgrunder med Adobe Firefly-teknik

Formgivaren kan integreras med Adobe Firefly för att hjälpa kunder att skapa enhetliga, varumärkesanpassade certifikat i stor skala:

- Administratörer genererar bakgrunder från nyckelordsuppmaningar och ett färgschema (t.ex. &quot;minimalistisk, hälso- och sjukvård, blågrön palett&quot;).
- Ett utvalt nyckelordsbibliotek stöder vanliga branscher (frakt, hälso- och sjukvård och annat) för användare som inte är formgivare.
- Genererade bilder läggs till i bakgrundsgalleriet och kan återanvändas i olika mallar.
- Kredit och nivåindelning för Firefly-användning i Learning Manager definieras av produktpolicyn.

### Migrering av äldre HTML-certifikat

Befintliga HTML- eller ZIP-certifikatmallar behålls men kan inte redigeras i den nya designern:

- Äldre mallar migreras med flaggor som `isLegacy`/`is_active`.
- De visas som icke-redigerbara poster (ingen WYSIWYG-förhandsgranskning) och förblir giltiga för historisk användning.
- När märken var knutna till äldre mallar gör migreringen att certifikaten kan hämtas. Om konfigurationen inte kan bevaras gäller globala standardvärden.

### Generering och förbakning av PDF

Förbättra körningsprestanda och elevupplevelsen:

- Certifikat förbakas vid slutförande (när LO:n slutförs) och cachelagras sedan så att eleverna snabbt kan hämta dem.
- Befintliga elevflöden för hämtning av certifikat via **Badges** och **Achievements** är desamma.

## Utmaningen

Idag är certifikathanteringen i Learning Manager beroende av en kodtung, supporttung modell:

**Högt beroende av CSM och supportteam**: Administratörer tillhandahåller HTML- eller ZIP-filer som CSM eller teknisk överföring via interna verktyg. Varje ändring (varumärkning, logotyper, förordningstext, signaturer) kräver en intern biljett- och distributionscykel.

**Begränsad flexibilitet för företagsteam**: Marknadsförings-, efterlevnads- eller HR-team behöver ofta lokala certifikatuppdateringar (språk, kampanjer, landsspecifika regler). Det aktuella arbetsflödet gör uppdateringarna långsammare och fördröjer efterlevnadsprogrammen.

**Fragmenterad konfiguration och otydligt arv**: Äldre HTML-mallar kan ställas in på konto-, utbildningsobjekts- och utbildningsobjektnivå med komplexa återgångsregler. Utan tydlig konfiguration i flera nivåer kan det vara svårt att se vilken mall som gäller var.

**Begränsningar för länkning av utmärkelsetecken** Certifikat är nära kopplade till **märken**:

- Ett certifikat måste vara kopplat till ett märke. Inget certifikat utfärdas.
Den kopplingen kan komplicera designändringar när administratörer vill ha certifikat utan spelifieringselement.

**Icke-visuell redigering och inkonsekvens i varumärket**: HTML-baserade certifikat är flexibla men kräver klientkompetens som många administratörer inte har. Vissa kunder förlitar sig på generiska standardcertifikat, vilket försvagar varumärkets enhetlighet.

**Konkurrensgap**: Vissa system för hantering av inlärning inkluderar inbyggda anpassade certifikatutvecklare (t.ex. Docebo). Utformning av självbetjäningscertifikat har varit en lucka i Adobe Learning Manager.

Resultatet är långsam förändring, hög supportkostnad och en redigeringsupplevelse som inte matchar administratörens förväntningar för certifikat och autentiseringsuppgifter.

## Hur anpassade certifieringar hanterar dessa utmaningar

### Självbetjänande, administratörsvänliga arbetsflöden

Här är arbetsflödena:

- Certifikatdesignern och listan ersätter HTML uppladdningsskript och intern etablering med en administratörsdriven upplevelse:
- Administratörer skapar, publicerar och fasar ut certifikatdesigner i Learning Manager utan kod eller CSM-inblandning.
- Designuppdateringar (till exempel säsongsbetonade eller partnerspecifika varumärken) tar bara några minuter i användargränssnittet i stället för biljetter och tekniska cykler.
- Standardinställningar på kontonivå och nivå för utbildningsobjekt minskar upprepad konfiguration per objekt.

### Minskade supportkostnader och operativa risker

Genom att konsolidera certifikathanteringen under **Achievements** med en tydlig användarupplevelse:

- Arbetsbelastningar för &quot;ladda upp eller ändra mitt certifikat&quot;-förfrågningar försvinner för CSM och teknikerteam.
- Produkten tillämpar säkra begränsningar (till exempel låst orientering, icke-redigerbara äldre mallar) för att minska risken för befintliga distributioner.
- Migrerade äldre mallar gör att historiska certifikat är tillgängliga utan extra supportinsats.

### Styrning, konsekvens och varumärkeskontroll

Standardvärden, Firefly och gallerier hjälper kunderna att:

- Skicka mallar för varumärkning en gång på kontonivån och åsidosätt endast vid behov.
- Använd Firefly-bakgrunder i företagsvakter i stället för externa ad hoc-resurser.
- Styr certifikat genom publicerings- och utfasningstillstånd, med förhandsgranskningsbara utkast före lansering.

### Justering med befintliga flöden för utmärkelsetecken och certifikat

Designen behåller den aktuella elevsökvägen: certifikaten hämtas fortfarande från **Badges** och **Achievements**, vilket begränsar omskolning.

### Prestanda och skalbarhet

Prestanda för färdigbakade certifikat och JSON-driven återgivning:

- Certifikat genereras när de är klara och lagras, så nedladdning är i själva verket en statisk hämtning.
- JSON-baserade designer är lätta att använda vid redigering och rendering under körning i stor skala.

## Verkliga användningsfall

### Utbildning av kunder och partner: varumärkta autentiseringsuppgifter i stor skala

**Scenario:** Ett programvaruföretag driver kund- och partnerskolor med hundratals program i olika regioner och varumärken.

- Använd standardmallar på kontonivå med Firefly-genererade bakgrunder justerade till varje produktlinje.
- Lägg till språkspecifika layouter för lokaliserade certifieringstitlar, ansvarsfriskrivningar och signaturer.
- För premiumpartner: duplicera basmallar och lägg till partnersamarbete (logotyp och juridisk text) på instansnivå.
- Med färdigbakade PDF kan partners hämta certifikat direkt efter att de har slutfört partnercertifieringarna, med minimal belastning på Learning Manager.

Mönstret passar franchise- eller multi-brand-ekosystem där certifikat förstärker varumärkes- och partnervärden (till exempel stora partnernätverk som RealPage).

### Regelefterlevnads- och regelutbildning: miljöer med stora förändringar och flera språk

**Scenario:** Ett reglerat företag måste uppdatera ordalydelsen i efterlevnadscertifikatet, ofta efter land och språk.

- **Administratörsledd redigering** gör att juridiska team och efterlevnadsteam kan ändra formuleringar och dynamiska fält utan tekniska biljetter.
- Språkspecifika layouter stöder **lands- eller regionspecifika friskrivningar** och signaturer för en delad designstruktur.
- **Återställningslogik** ser till att systemet fortfarande använder säkra standardvärden om en specifik LO-instansmall saknas och undviker utfärdandefel.

Detta gäller hälso- och sjukvård, ekonomi, myndigheter och andra branscher där certifikattexten ofta ändras och revideras.

### Återkommande certifieringar med kollegialt eller delat kataloginnehåll

**Scenario:** Ett Master Learning Manager-konto delar innehåll med flera **kollegiala konton** (till exempel många kundkonton), vart och ett med återkommande certifieringar och egna certifikat.

- Kollegiala konton kan **lägga till förvärvade kurser i återkommande certifieringar** och konfigurera **lokala certifikatmallar** på instansnivå.
- Kursuppdateringar från huvudkontot flödar in i upprepningar som förväntat, medan certifikatutformningar kan förbli **per kund**.

### Interna aktiverings- och ledarskapsprogram

**Scenario:** Interna program (till exempel chefsacceleratorer eller produktakademier) vill ha **visuellt åtskilda certifikat** som administratörer kan uppdatera utan att arbeta i HTML.

- Programägare kan utforma **programmärkta mallar** (t.ex. interna akademier eller bilder i MAP-stil) utan HTML-kunskaper.
- Åsidosättningar på instansnivå gör att olika kohorter eller regioner kan använda varianter (till exempel kohortspecifik eller regional varumärkning).
- Firefly-bakgrunder har stöd för **händelsespecifika eller kohortspecifika** bilder med mindre beroende av designteam.

### Övergång från äldre HTML-certifikat

**Scenario:** Befintliga kunder använder anpassade HTML5-certifikat som hanteras via CSM.

- Äldre HTML- eller ZIP-mallar migreras och markeras som äldre, vilket bevarar tidigare användning och hämtningar.
- Administratörer kan gå över till designbaserade mallar över tid, med början med högprioriterade program.
- Om migreringen inte kan bevara en mappning (till exempel utmärkelsetecken som har inaktiverats mitt på vägen) återgår systemet till den globala standardmallen så att eleverna inte blockeras.

## Skapa ett anpassat certifikat

**Förutsättning**

Om du vill använda bilder från Firefly måste din Adobe Learning Manager-instans integreras med Firefly.

1. Logga in på Adobe Learning Manager som **administratör**.
2. I avsnittet **Konfigurera** väljer du **Prestationer**. Sidan **Märken** öppnas.
   ![Skapa ett anpassat certifikat](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate1.png)
   *Navigera till Achievements på den vänstra navigeringspanelen*

3. Välj **Certifikat** i den vänstra navigeringspanelen. Sidan **Certifikat** öppnas.
   ![Skapa ett anpassat certifikat](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate2.png)
   *Certifikatsidan*

4. Välj **Nytt certifikat** i det övre högra området på sidan. Dialogrutan **Skapa ett nytt certifikat** öppnas.
5. Välj **Liggande** eller **Stående**, beroende på hur du vill att certifikatet ska se ut. När du har valt en orientering ser du en tom mall och färdiga mallar för den orienteringen.
   ![Skapa ett anpassat certifikat](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate3.png)
   *Liggande eller stående alternativ*

6. Välj en tom mall eller en befintlig mall.
7. Ange ett certifikatnamn.
8. I listrutan väljer du ett standardspråk.
9. Välj **Skapa**. Om du valde den tomma mallen visas en tom arbetsyta under certifikatnamnet.
10. Lägg till element: **Text**, **Bild**, **Dynamiskt värde** och **Certifikatbakgrund**.
    ![Skapa ett anpassat certifikat](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate4.png)
    *Lägg till element i certifikatet*

11. För **text** lägger du till innehåll under **Förformaterad text** eller **Textmallar** eller lägger till anpassad text. Texten visas på arbetsytan. När text är markerad visas formateringsalternativen ovanför arbetsytan. Om du vill ta bort innehåll som du inte vill ta bort väljer du ikonen **Ta bort** i arbetsytans övre högra hörn.
12. Om du vill lägga till bilder väljer du **Bild** bredvid **Lägg till element**. Överför bilder från datorn eller välj bilder från kategorilistorna.
13. Välj **Dynamiskt värde** för att lägga till grundläggande information, katalogetiketter och aktiva fält.
14. Välj **Certifikatbakgrund** för att använda färger eller bilder. Om du vill skapa bilder med Adobe Firefly väljer du **Generera bild**.
15. Beskriv vad du vill (upp till 100 tecken) i promptfältet och välj **Generera**. Fyra bildalternativ visas baserat på ditt ledord.
16. Markera den bild du vill använda. Den används som certifikatbakgrund.
    ![Skapa ett anpassat certifikat](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate5.png)
    *Lägg till en bild i certifikatet*

17. Välj **Förhandsgranska** om du vill granska certifikatet innan du publicerar det. På så sätt kan du förstå hur certifikatet ser ut.
    ![Skapa ett anpassat certifikat](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate6.png)
    *Förhandsgranska certifikatet*

18. I förhandsgranskningen kan du spara på Google Drive, hämta, skriva ut eller använda andra alternativ som anteckningar eller dokumentegenskaper.
19. Klicka på **Spara som utkast** om du vill fortsätta senare eller välj **Publish** om du vill publicera certifikatet. Efter publicering kan elever hämta certifikatet när de når den konfigurerade milstolpen.

När du har sparat ett certifikat under **Publicerat** eller **Utkast** kan du redigera, klona, byta namn på eller ta bort det.

## Redigera ett anpassat certifikat

1. I avsnittet **Konfigurera** väljer du **Prestationer**. Sidan **Märken** öppnas.
2. Välj **Certifikat** i den vänstra navigeringspanelen. Sidan **Certifikat** öppnas.
3. Välj fliken **Publicerat** eller **Utkast** för det önskade certifikatet.
4. Öppna åtgärdsmenyn (**...**) för certifikatet och välj **Redigera**.
   ![Redigera certifikat från åtgärdsmenyn](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0001.png)
   *Alternativet Redigera i listrutan*

5. Gör dina ändringar.
6. Markera **Publish** eller **Spara som utkast**.

## Klona ett anpassat certifikat

Använd **Klona** när du vill ha en kopia av ett certifikat för ett nytt namn eller ett liknande användningsfall. När du har klonat byter du namn på certifikatet så att det får ett distinkt namn. Annars kan namnet matcha källan även om du har ändrat designen.

>[!NOTE]
>
>Du kan inte ange ett nytt namn medan du sparar direkt efter kloningen. Byt namn på certifikatet efter att det har sparats som ett utkast eller efter att det har publicerats.

1. I avsnittet **Konfigurera** väljer du **Prestationer**. Sidan **Märken** öppnas.
2. Välj **Certifikat** i den vänstra navigeringspanelen. Sidan **Certifikat** öppnas.
3. Välj fliken **Publicerat** eller **Utkast** för det önskade certifikatet.
4. Öppna åtgärdsmenyn (**...**) för certifikatet och välj **Klona**.
   ![Klona certifikat från åtgärdsmenyn](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0002.png)
   *Alternativet Klona i listrutan*

5. Gör dina ändringar.

6. Markera **Publish** eller **Spara som utkast**.

7. Byt namn på det klonade certifikatet med hjälp av stegen i [Byt namn på ett anpassat certifikat](#rename-a-custom-certificate).

## Byta namn på ett anpassat certifikat

Du kan byta namn på ett certifikat utan att klona det.

1. I avsnittet **Konfigurera** väljer du **Prestationer**. Sidan **Märken** öppnas.
2. Välj **Certifikat** i den vänstra navigeringspanelen. Sidan **Certifikat** öppnas.
3. Välj fliken **Publicerat** eller **Utkast** för det önskade certifikatet.

4. Öppna åtgärdsmenyn (**...**) för certifikatet och välj **Byt namn**.
   ![Byt namn på certifikat från åtgärdsmenyn](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0003.png)
   *Alternativet Byt namn i listrutan*

5. Ange det nya namnet i dialogrutan **Byt namn på certifikat**.
   ![Dialogrutan Byt namn på certifikat](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0004.png)
   *Ange ett nytt namn*

6. Välj **Spara**. Learning Manager visar ett bekräftelsemeddelande.

## Ta bort ett anpassat certifikat

Det går inte att ångra borttagning av ett certifikat. Fortsätt bara om du är säker.

>[!NOTE]
>
>Du kan inte ta bort ett certifikat som är kopplat till ett utbildningsobjekt eller en utbildningsinstans.

1. I avsnittet **Konfigurera** väljer du **Prestationer**. Sidan **Märken** öppnas.
2. Välj **Certifikat** i den vänstra navigeringspanelen. Sidan **Certifikat** öppnas.
3. Välj fliken **Publicerat** eller **Utkast** för det önskade certifikatet.
4. Öppna åtgärdsmenyn (**...**) för certifikatet och välj **Ta bort**. Ett bekräftelsemeddelande visas i Adobe Learning Manager.
   ![Ta bort certifikat från åtgärdsmenyn](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0005.png)
   *Alternativet Ta bort i listrutan*
   ![Bekräfta borttagning av certifikat](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0006.png)
   *Bekräftelsemeddelande*

5. Välj **Ja**. Om certifikatet inte är kopplat till ett utbildningsobjekt eller en instans slutför Learning Manager borttagningen och kan visa en ny bekräftelse.

## Ange ett anpassat certifikat som standardcertifikat

Du kan ange ett certifikat som standard för:

- Utbildningar
- Utbildningsvägar
- Certifieringar
- Alla

![Standardcertifikatalternativ](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0007.png)
*Ange som standardcertifikat*

1. I avsnittet **Konfigurera** väljer du **Prestationer**. Sidan **Märken** öppnas.
2. Välj **Certifikat** i den vänstra navigeringspanelen. Sidan **Certifikat** öppnas.
3. Välj fliken **Publicerat** eller **Utkast** för det önskade certifikatet.
4. Öppna åtgärdsmenyn (**...**) för certifikatet, välj **Ange som standard** och välj sedan ett av de fyra alternativen. Learning Manager visar ett bekräftelsemeddelande.
5. Välj **Ja**. Learning Manager visar ytterligare en bekräftelse. Certifikatet visar etiketten **Standard för** med den valda kategorin (till exempel **Standard för utbildningar**).
   ![Standard för kategorietikett på certifikat](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0008.png)
   *När det har blivit standardcertifikatet*
