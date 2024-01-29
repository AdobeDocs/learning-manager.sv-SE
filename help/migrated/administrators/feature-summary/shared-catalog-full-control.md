---
jcr-language: en_us
title: Aktivera fullständig kontroll över delad katalog
description: Aktivera fullständig kontroll över den delade katalogen i Adobe Learning Manager
contentowner: saghosh
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 0%

---



# Aktivera fullständig kontroll över delad katalog

## Skapa katalog {#createcatalog}

Administratörer kan skapa en katalog med kurser, utbildningsprogram, arbetsstöd och certifieringar.

Mer information finns i [Kataloger](/help/migrated/administrators/feature-summary/catalogs.md).

## Dela katalog {#sharecatalog}

Du kan dela katalogerna med interna användare i en organisation eller med externa användare. Delningen är dock exklusiv. Med andra ord kan en internt delad katalog inte delas med externa grupper och vice versa.

Kurser, utbildningsprogram, arbetsstöd och certifieringar är de utbildningsobjekt som stöds för en delad katalog.

Mer information finns i [Dela kataloger](/help/migrated/administrators/feature-summary/catalogs.md).

## Aktivera fullständig kontroll över delad katalog {#fullcontrol}

Du kan bevilja fullständig åtkomst till katalogen för externa konton. Kontots administratör kan sedan acceptera katalogen och kan följaktligen lägga till eller ta bort utbildningar eller moduler.

För att ge fullständig kontroll till ett externt konto

1. När du har lagt till utbildningar i en katalog måste du dela katalogen med externa användare.
1. I dialogrutan Externt konto lägger du till underdomänen och e-post-ID för administratören för den externa organisationen.
1. I alternativet Katalogkontroll, växlar du knappen för att tillåta fullständig kontroll över katalogen till externa användare.

   ![](assets/catalog-control.png)

   *Tillåt fullständig kontroll över delad katalog*

   När du tillåter fullständig katalogkontroll godkänner administratören för den externa organisationen begäran om att tillåta ändringar i katalogen. Författaren till den externa organisationen kan sedan redigera kurserna eller lägga till moduler.

   Se avsnitten nedan för mer information.

## Administratör för extern organisation {#administratorofexternalorganization}

När administratören för den tidigare organisationen har aktiverat fullständig kontroll över katalogen accepterar administratören för den externa organisationen begäran och visar den.

1. Klicka på meddelandeikonen för att visa meddelandet om att acceptera katalogen.

   <!--![](assets/notification-to-acceptcatalog.png)-->

1. Om du vill acceptera inbjudan till katalogen klickar du på Acceptera.
1. Om du startar katalogen som har delats med dig i listan med kataloger visas ett meddelande om att katalogen nu har fullständig kontroll.

   ![](assets/catalog-details.png)

   *Visa kataloginformation*

1. Du kan ändra namnet på katalogen och beskrivningen.

## Dela katalog för utbildningsprogram, certifiering och arbetsstöd {#sharecatalogforlearningprogramcertificationandjobaids}

Liksom att bevilja fullständig katalogkontroll för kurser kan administratören också bevilja fullständig katalogkontroll för följande:

* Utbildningsprogram
* Certifieringar
* Arbetsstöd

## Återställ kurs {#resetcourse}

1. På det katalogkort som har en trasig länk klickar du på **[!UICONTROL Reset Course]**.

<!-- ![](assets/reset-course.png)-->

1. Ett varningsmeddelande visas när du har klickat på knappen Återställ. Återställer kursen:

   * Tar bort allt nyligen tillagt innehåll från katalogen.
   * Katalogen uppdateras synkroniserat med den ursprungliga delade katalogen.
   * Återställer relationen med det överordnade utbildningsobjektet.

   Återställningen av katalogen går inte att ångra. Du kan inte ångra de ändringar du har gjort i katalogen.

1. Acceptera ändringarna genom att klicka på Ja.
1. I kurskatalogen kan du se att katalogen inte har meddelandet *Bruten länk* längre.

   När du visar kataloginformationen ser du att katalogen nu är återställd till sitt ursprungliga läge.

## Lägg till ett utbildningsobjekt igen {#readdalearningobject}

Om du har tagit bort en kurs, ett utbildningsprogram, en certifiering eller ett arbetsstöd av misstag kan du återställa det.

Om du vill återställa ett borttaget utbildningsobjekt klickar du på Lägg till igen.

Åtgärden ångrar åtgärden och återställer utbildningsobjektet i katalogvyn.

![](assets/re-add-button.png)

*Lägg till ett utbildningsobjekt igen*

När du har klickat på knappen Lägg till igen visas ett bekräftelsemeddelande om att utbildningsobjektet har lagts till i katalogen.

## Extern organisation {#externalorganization}

När administratören för det externa kontot har accepterat katalogen kan författaren nu lägga till kurser och utbildningsprogram.

1. Du som är användare får ett meddelande om att katalogen nu är tillgänglig på ditt konto.
1. Klicka på för att se listan över kurser **[!UICONTROL Courses]** i den vänstra navigeringsrutan. Du kan se alla kurser som du har skapat och delat med dig.
1. Om du vill visa kursdetaljerna klickar du på **[!UICONTROL View Course]** på kurskortet.

   <!--![](assets/view-course.png)-->

1. På detaljsidan för kursen kan du se information om kursen och de delade modulerna. Om du vill lägga till en modul klickar du på Lägg till moduler. När du lägger till moduler till befintliga moduler visas de nya modulerna i slutet av de befintliga modulerna. Du kan när som helst ändra ordningsföljden för modulerna.
1. När du har lagt till modulerna klickar du på Återpublicera.

   När du har återpublicerat modulerna visas ett meddelande på katalogkortet *Bruten länk*.

   Eftersom du har uppdaterat originalkatalogen med nya moduler finns inte längre den befintliga relationen med den förvärvade kursen.

   Utbildningsobjektet kommer inte att vara synkroniserat med källkontot eftersom innehållet i utbildningsobjektet har ändrats.

   <!--![](assets/link-broken.png)-->

Om du efter att ha lagt till och publicerat om modulen känner att du har lagt till eller tagit bort en kurs i katalogen av misstag tidigare, kan du återställa modulen och återställa den till dess ursprungliga skick när den delades med fullständig kontroll.
