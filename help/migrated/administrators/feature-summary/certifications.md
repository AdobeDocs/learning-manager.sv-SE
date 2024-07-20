---
description: Lär dig skapa certifieringar, registrera elever och redigera publicerade certifieringar.
jcr-language: en_us
title: Certifieringar
contentowner: manochan
exl-id: 406d1c33-aac3-47e1-9b32-83874976ce54
source-git-commit: 69ef7d1e27fac3db49cbb4b9f9403f74e146efb5
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 2%

---

# Certifieringar

Lär dig skapa certifieringar, registrera elever och redigera publicerade certifieringar.

Certifiera dina elever som engångsföreteelse eller enligt en återkommande tidsram med den här funktionen. Endast administratörer kan definiera certifieringarna för elever.

Som administratör kan du skapa ett certifieringsprogram som antingen är internt värdbaserat eller genomförs av en tredje part. Vid intern certifiering anger du de kurser som en elev måste slutföra för att bli certifierad. Publish programmet och tilldela det sedan till elever.

## Skapa en certifiering {#createacertification}

1. Klicka på **[!UICONTROL Certification]** i den vänstra rutan.\
   En sida visas med en lista över alla utkast och publicerat tillstånd för certifieringarna.

1. Visa certifieringar i olika lägen:

   1. Klicka på fliken **[!UICONTROL Draft]** om du vill se alla certifieringar som är i utkastläge. Du måste slutföra skapandet av dem.
   1. Klicka på **[!UICONTROL Published]** för att se alla certifieringar som publicerats av dig.
   1. Klicka på **[!UICONTROL All]** för att visa certifieringarna i alla tillstånd.
   1. Sortera och visa listan med certifieringar i stigande eller fallande ordning eller baserat på det datum du uppdaterade dem.

1. Klicka på **[!UICONTROL Add]**.

   En ny certifieringssida visas.

![](assets/add-new-certification.png)

*Visa sidan för att lägga till en certifiering*

1. Lägg till certifikatnamn och beskrivning.

<table>
 <tbody>
  <tr>
   <th>Fält</th>
   <th>Beskrivning</th>
  </tr>
  <tr>
   <td>Antal dagar för slutförande</td>
   <td>Sista datum för certifieringen. Ange ett numeriskt värde.</td>
  </tr>
  <tr>
   <td>Typ</td>
   <td>
    <p>Typ av certifiering:</p>
    <ul>
     <li><b>Återkommande</b>- Välj det här alternativet om certifieringen måste ske efter varje år, två år eller tre år.</li>
     <li><b>Permanent</b>- Välj det här alternativet om certifieringen måste vara engångskravet.</li>
    </ul></td>
  </tr>
  <tr>
   <td>Omtilldelning</td>
   <td>Välj om du vill att certifikatet ska omtilldelas baserat på slutförandedatum eller baserat på registreringsdatum.<br></td>
  </tr>
  <tr>
   <td>Giltighet (i månader) <br></td>
   <td>Ange hur länge certifieringen kan förbli giltig.</td>
  </tr>
  <tr>
   <td>Ordningsföljd på kurser<br></td>
   <td>Bestäm om elever ska utföra kurserna på ett ordnat eller oordnat sätt.<br></td>
  </tr>
  <tr>
   <td>Avregistrering<br></td>
   <td>Aktivera eller inaktivera alternativet för att låta elever avregistrera sig själva.</td>
  </tr>
  <tr>
   <td>Certifieringsutfärdare<br></td>
   <td>
    <p>Välj <b>Intern</b> om den tillhör din organisation, eller välj <b>Extern</b> för externa organisationscertifieringar.</p>
    <p>När du väljer <b>Extern certifiering</b> visas ytterligare två alternativ:</p>
    <ul>
     <li>Samma som godkännandedatum<br></li>
     <li>Inskickat av elev<br></li>
    </ul>
    <p>Elever kan ange rätt slutförandedatum för externa certifieringar. I tidigare versioner angavs slutförandedatumet som standard av Prime, baserat på datumet för chefens godkännande. Slutförandedatum som tillhandahålls av eleven ska vara senare än skapandedatumet för certifikatet<span>.</span></p></td>
  </tr>
  <tr>
   <td>Varaktighet</td>
   <td>Om du har valt Extern certifiering anger du varaktigheten i minuter.</td>
  </tr>
  <tr>
   <td>Taggar</td>
   <td>Ange de taggar som du vill koppla till certifikatet. Taggar är användbara när du vill söka efter certifikatet.</td>
  </tr>
  <tr>
   <td>Välj kataloger<br></td>
   <td>Välj den katalog där certifikatet är en del av.</td>
  </tr>
 </tbody>
</table>

Välj nivå för produkter, roller och roller i avsnittet **[!UICONTROL Recommend for]** för att föreslå den här utbildningsvägen för användare som har uttryckt intresse för dessa produkter och roller.

![](assets/recommend-for.png)

*Rekommendation*

Välj de kurser som ska läggas till i certifieringen från fliken **[!UICONTROL Courses]** > **[!UICONTROL Catalog]**.

Håll muspekaren över varje kursruta och klicka på + för att lägga till dem i certifieringen. Klicka på **[!UICONTROL Preview]** för att visa kursen som elev innan du lägger till den.

1. Klicka på fliken **[!UICONTROL Curriculum]** för att visa/verifiera listan över kurser som du har lagt till.
1. Klicka på **[!UICONTROL Publish]**.

## Mappning av kursinstanser för certifieringar {#courseinstancemappingforcertifications}

Så här mappar du kursen och instansen för certifieringar:

1. Klicka på Certifieringar i den vänstra rutan.
1. I listan över certifieringar väljer du Visa certifiering av certifieringen där du vill mappa kursen och instansen.
1. I den vänstra rutan klickar du på Kurser. Kurserna för certifieringen visas. Klicka på Redigera.
1. Håll pekaren över kursen där du vill ange instansmappningen och välj Kursinstansmappning.
1. I popup-fönstret som visas väljer du instansen av kursen som ska levereras för certifieringen som du har valt.
1. Klicka på Spara.

En administratör kan lägga till klassrums- och virtuella klassrumstyper till ett utbildningsprogram. Vilken session författaren än har gett när kursen skapades blir standardinstansen. När administratören lägger till kurser i ett utbildningsprogram mappas det som standard till standardinstansen av alla kurser, men administratören kan ändra instansmappningen. Antalet kurser som läggs till i ett utbildningsprogram visas också på instanssidan enligt nedan.

## Aktivera fullständig katalogkontroll {#catalog}

Precis som att bevilja fullständig [katalogkontroll för utbildningar eller moduler](shared-catalog-full-control.md) kan du även aktivera fullständig katalogkontroll för certifieringar.

## Registrera eller avregistrera elever till certifieringen {#enrollorunenrolllearnerstothecertification}

Mer information om hur du registrerar elever och hur du följer dem finns i [Registrerar elever](courses.md#main-pars_header_1058138132).

## Avregistrering av elever {#unenrollmentforlearners}

När du skapar certifieringar har administratören ett alternativ för att välja om elever kan avregistrera sig själva från certifieringen. Om Administratör väljer alternativet kan eleven avregistrera sig själv.

![](assets/unenrollment.png)

*Välj att avregistrera elever*

## Markera slutförande {#markcompletion}

Administratörer kan markera en certifiering som slutförd med det alternativ som är tillgängligt för dem. Gör så här för att markera slutförandet av en certifiering.

1. Öppna **[!UICONTROL Certification]** > **[!UICONTROL Learners]**.

   Sidan Elever öppnas med listan över registrerade elever.

1. Markera en/flera/alla elever för att markera slutförande av certifieringen med kryssrutan Tillgänglig för varje elev.
1. Klicka på **[!UICONTROL Action]** > **[!UICONTROL Mark completion.]**

   Observera att om en certifiering har flera kurser kommer slutförande att markeras för alla kurser.

## Obligatoriska kurser för extern certifiering {#mandatory}

I tidigare versioner av Learning Manager var slutförande av kursen från eleven i extern certifiering inte obligatoriskt för att slutföra ett certifikat.

Du kan nu göra kurser obligatoriska genom att aktivera alternativet **[!UICONTROL Set required courses as Mandatory for Certificate Completion]** på fliken Kursplan när du redigerar certifieringen.

## Redigera en publicerad certifiering {#editingapublishedcertification}

En certifiering kan redigeras av en administratör vid publicerat tillstånd. I det här läget kan administratören redigera alla avsnitt i en certifiering och publicera igen.

Om du vill redigera en publicerad certifiering klickar du på certifieringskortet och sedan på **[!UICONTROL Edit]** längst upp till höger på sidan.

När du redigerar avsnitt i en certifiering och måste flytta från sidan, måste du publicera certifieringen igen. Du får en dialogruta där du ombeds att publicera certifieringen.

![](assets/edit-a-certificate.png)

*Redigera ett certifikat*

## Prenumeration {#subscription}

En administratör kan hämta quiz-poäng och elevstatusrapporter. De kan ange rapportfrekvens, e-postämne och mottagarnas e-post-ID. Beroende på den angivna frekvensen får mottagaren ett e-postmeddelande med rapporten bifogad.

![](assets/report-subscription.jpeg)

*Ange rapportfrekvens och andra egenskaper*
