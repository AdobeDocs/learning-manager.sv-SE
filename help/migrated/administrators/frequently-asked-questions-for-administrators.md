---
jcr-language: en_us
title: Vanliga frågor för administratörer
description: Vanliga frågor för Adobe Learning Manager-administratörer
contentowner: manochan
exl-id: 8b113a4e-73f4-4cd5-982a-cefdf5388e91
source-git-commit: 5676ddb238309bc643394af1dde3cba7f8ac6699
workflow-type: tm+mt
source-wordcount: '2460'
ht-degree: 0%

---

# Vanliga frågor för administratörer

<table>
 <tbody>
  <tr>
   <td><img src="assets/administrator2.png"></td>
   <td>
    <p>Läs vidare för att lära dig mer om vanliga frågor från Learning Manager som är kopplade till administratörsrollen. </p></td>
  </tr>
 </tbody>
</table>

+++Kan jag lägga till flera användare samtidigt? Hur?

Ja, du kan lägga till användare i grupp genom att använda funktionen för CSV-överföring. Klicka [här](/help/migrated/administrators/add-users-in-bulk.md) för mer information.

+++

+++Jag skrev fel e-post-ID när jag skapade inloggning för mina elever, hur korrigerar jag det?

För att åtgärda en användarinloggning måste du importera CSV i Learning Manager. En CSV-exempelfil bifogas längst ned på den här sidan som referens. Eftersom e-post anses vara en unik identifierare för en person kan den inte redigeras. Gör så här:

1. Lägg till samma användare med rätt e-post-ID i CSV och se till att han förblir chef för andra användare genom att lägga till hans e-post-ID i kolumnen &quot;E-post till anställds chef&quot; i CSV-exempelfilen.
1. Lägg till andra användare i ditt konto i CSV-filen, inklusive dig själv
1. Importera den här filen från Learning Manager-administrationsprogrammet ->Användare ->Lägg till ->Importera CSV
1. Mappa alla fält, enligt anvisningarna i dialogrutan, till motsvarande CSV-kolumner.
1. Klicka på Spara.

Användare ska läggas till på sidan Elever.

[Exempel för Learning Manager CSV.csv](https://helpx.adobe.com/content/dam/help/en/captivate_prime/learning-manager-sample-csv.zip)

+++

+++Hur skapar jag aviseringar?

Du kan skapa aviseringar i Adobe Learning Manager 1.0. Mer information finns i [aviseringsfråga](/help/migrated/administrators/feature-summary/user-notifications.md).

+++

+++Hur lägger jag till certifikat för kurserna?

Adobe Learning Manager tillhandahåller inte certifikat för kurserna. Administratören kan dock skapa utmärkelsetecken för varje kurs genom att klicka på fliken Märken i den vänstra panelen. När administratören registrerar elever för en kurs kan administratören även koppla ett utmärkelsetecken till kursen.

+++

+++Hur importerar jag signaturer för certifikaten?

I Adobe Learning Manager finns ingen funktion för att importera signaturer för certifieringen eller märket.

+++

+++Kan jag ställa in en kalender för kurserna? Hur?

I Adobe Learning Manager 1.0 har vi inga planer på att ange en kurskalender.

+++

+++Hur gör jag för att registrera elever på väntelistan direkt?

Elever sätts upp på väntelistan till en klassrumskurs när antalet platser är begränsade, baserat på ordningen i vilken de registrerat sig. Administratörer kan välja elever på väntelistan och tilldela platser som ersätter platsgränsen för en klassrumskurs. Elever registreras till kursen så snart administratören tilldelar dem en plats.

1. Klicka på Kurser i den vänstra rutan när du har loggat in som administratör.
1. Klicka på kursnamnet på valfri klassrumskurs i listan med tillgängliga kurser. En ny sida med detaljerad information om kursen visas.
1. Klicka på Väntelista i den vänstra rutan på sidan för kursinformation. En lista med elever på väntelistan visas på sidan.
1. Välj eleverna och klicka på Allokera platser för att registrera eleverna direkt på kurserna istället för platsgränsen.

Mer information finns i funktionen [Väntelista och närvaro](/help/migrated/administrators/feature-summary/waitlist-attendance-management.md).

+++

+++Hur registrerar jag närvaro för elever i klassrumsmoduler?

Ja, du kan registrera närvaro genom att följa stegen nedan:

1. Klicka på Kurser i den vänstra rutan när du har loggat in som administratör.
1. Klicka på kursnamnet på valfri klassrumsmodul/kurs i listan med tillgängliga kurser. En ny sida med detaljerad information om kursen visas.
1. Välj eleverna och klicka på Spara för att registrera att kursen är slutförd.

Om det finns flera moduler i en kurs och eleven endast har slutfört en av dem, kan du välja en enda modul och klicka på Spara för att markera slutförandet för eleven. Om eleven slutför alla moduler på en kurs kan du klicka på Välj alla alternativ och klicka på Spara.

Mer information finns i funktionen [Väntelista och närvaro](/help/migrated/administrators/feature-summary/waitlist-attendance-management.md).

+++

+++Hur inkluderar jag alternativet med L3-feedback?

Du kan lägga till feedback om L3 medan du registrerar elever till kurserna. Lägg till en L3-feedbackfråga genom att följa stegen nedan:

1. Klicka på Kurser i den vänstra rutan när du har loggat in som administratör. Listor över alla kurser visas på den högra sidan.
1. Klicka på den kursruta som du vill lägga till L3-feedback för
1. Klicka på instance default (standardinställning) i den vänstra rutan.
1. Klicka på växlingsknappen för cirkel på bredvid L3 - feedback om beteendeförändring för att välja den.
1. Lägg till L3-feedbackfrågan i textområdet under L3-frågan.

+++

+++Hur söker jag chefens nominering till chefsnominerad kurs?

Som administratör kan du söka till chefens nominering för kurserna genom att följa stegen nedan:

1. Klicka på Kurser i den vänstra rutan
1. Håll muspekaren över en chefsnominerad kurs och klicka på **[!UICONTROL Seek Manager Nomination]**.

1. Klicka på länken **[!UICONTROL Managers nominated]** följt av länken **[!UICONTROL Add Managers]** i listan med instanser.

1. Lägg till chefens namn, antalet tilldelade platser och klicka på bockmarkeringen för att spara ändringarna.

När du skapar kurserna väljer författaren vilken typ av kurs som chefsnominerad.

+++

+++Hur registrerar jag eleven för en viss kurs?

Registrera elever på kurser genom att följa stegen nedan:

1. Klicka på Kurser i den vänstra rutan när du har loggat in som administratör. Lista över alla kurser visas på höger sida.
1. Välj den kurs som du vill lägga till elever för och håll pekaren över den.
1. Klicka på Registrera elever och lägg till namnet på elever. **Obs!** Du kan lägga till en eller flera elever åt gången.

+++

+++Hur tilldelar man elever en viss kompetens?

Tilldela elever kompetenser genom att följa stegen nedan:

1. Klicka på **[!UICONTROL Skills]** i den vänstra rutan när du har loggat in som administratör.
1. Välj en eller flera kompetenser genom att klicka på kryssrutorna vid varje kompetens och klicka på rullgardinsmenyn **[!UICONTROL Actions]** i det övre högra hörnet på sidan.
1. Klicka på Tilldela till användare.
1. Börja skriva namnet på användaren, välj från rullgardinsmenyn och klicka på **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Du kan registrera flera elever för färdigheter genom att klicka på Lägg till fler användare och genom att upprepa det fjärde steget.

+++

+++Hur skapar man en session för utbildningsprogram?

Skapa ett utbildningsprogram genom att följa stegen nedan:

1. Klicka på Utbildningsprogram i den vänstra rutan. Sidan Utbildningsprogram visas med en lista över befintliga utbildningsprogram.
1. Klicka på Lägg till längst upp till höger på sidan.\
   Ange programnamn, översikt och beskrivning och klicka på Spara.
1. Klicka på Kurser i den vänstra rutan.
1. Lägg till en eller flera kurser genom att klicka på + på varje kursruta.

   >[!NOTE]
   >
   >Du måste publicera utbildningsprogrammet innan du registrerar elever eller en instans.

1. Klicka på Instanser i den vänstra rutan och klicka på **[!UICONTROL Add new instances]** i det högra hörnet av sidan för att inkludera information om instansen.

Mer information om utbildningsprogram finns i [Funktionen Utbildningsprogram.](/help/migrated/administrators/feature-summary/learning-programs.md)

+++

+++Hur ändrar eller anpassar jag rapporter för alla roller?

Klicka på rullgardinspilen i det övre högra hörnet av varje rapport för att redigera/ändra rapporter. Klicka på spara när du är klar med ändringarna och visa den ändrade rapporten.

+++

+++Hur ändrar jag kurser, utbildningsprogram och företagsprofil?

Du kan redigera kurser eller utbildningsprogram även efter att du har publicerat dem. Mer information finns i [Kurser](/help/migrated/administrators/feature-summary/courses.md) och [utbildningsprogram](/help/migrated/administrators/feature-summary/learning-programs.md) Hjälpinnehåll.

Om du vill ändra företagsprofilen klickar du på **[!UICONTROL Settings]** i den vänstra rutan och sedan på **[!UICONTROL Change]** i det övre högra hörnet på sidan.

+++

+++Hur söker jag efter kurserna?

Klicka på Kurser i den vänstra rutan när du har loggat in som administratör. En lista över alla tillgängliga kurser visas.

Du kan söka på kurser på två sätt:

1. Klicka på sökikonen som visas i det övre högra hörnet. Ett sökfält visas. Skriv in kursnamnet eller några nyckelord som är associerade med dina kurser för att hitta dina kurser.
1. Genom att filtrera kurslistor med filtren.

Du kan filtrera kurserna efter tillstånd som Alla, Publicerade och Utfasade genom att klicka på vart och ett av dessa alternativ. Du kan också söka baserat på kompetenser genom att klicka på Kompetenser och välja var och en av dem.

Beroende på ditt val kan du visa den filtrerade listan över kurser och välja de kurser som krävs.

+++

+++Kan jag ändra teman för programmet? Hur?

Ja, du kan ändra teman och varumärke för Learning Manager-programmet enligt organisationens krav. En uppsättning med fem representativa bilder tillhandahålls för att förhandsgranska dina färgtemaändringar innan du tillämpar dem på ditt program. Bläddra igenom bilderna genom att klicka på symbolerna &lt; och > till vänster och höger om bilderna för att förhandsgranska dem.

Klicka på **[!UICONTROL Branding]** i den vänstra rutan för att uppdatera organisationens namn, ändra underdomänen, loggstilar och teman. Klicka på **[!UICONTROL Edit]** bredvid vart och ett av dessa ämnen för att ändra innehållet.

Mer information finns i [Hjälp med färgteman och varumärken](/help/migrated/administrators/feature-summary/themes.md).

+++

+++Hur ställer jag in märken för kurserna?

1. Klicka på Märken i den vänstra rutan när du har loggat in som administratör.
1. Klicka på Lägg till längst upp till höger på sidan som visas.
1. LÄGG TILL UTMÄRKELSENAMN.
1. Ladda upp märket genom att klicka på Ladda upp märke och klicka på Spara.

+++

+++Hur skapar jag spelifieringspoäng för kurserna?

Du kan ställa in spelifieringspunkter för elever genom att följa stegen nedan:

1. Klicka på Spelifiering när du har loggat in som administratör. En sida visas med en lista över nivåer av brons, silver, guld och platina och de poäng som krävs för att uppnå motsvarande nivå. Det finns en lista med uppgifter och motsvarande punkter.
1. Klicka på ikonen Redigera bredvid varje uppgift för att ställa in/ändra punkterna.

Mer information finns i [Spelifieringsfunktion](/help/migrated/administrators/feature-summary/gamification.md).

+++

+++Hur skapar jag rapporter för chefer och elever?

Du kan skapa rapporter genom att följa stegen nedan:

1. Klicka på Rapporter i den vänstra rutan. Sidan Rapportsammanfattning visas.
1. Klicka på **[!UICONTROL Add]** längst upp till höger på sidan Rapporter.

   Dialogrutan **[!UICONTROL Add Report]** visas.

1. Fyll i alla obligatoriska fält och klicka på Spara.

Endast administratörer och chefer kan skapa eller visa rapporter. Mer information finns i [rapportfunktionen](/help/migrated/administrators/feature-summary/reports.md).

+++

+++Hur byter jag till elev, chef och författarroller?

Du kan växla ditt konto och logga in på andra roller, som elev, chef och författare, utan att logga ut från ditt konto.

1. Klicka på rullgardinspilen bredvid din profilbild i det övre högra hörnet på sidan.\
   En snabbmeny visas.
1. Välj varje tillgänglig roll för att få åtkomst till respektive rollkonton.

+++

+++Hur inkluderar jag meddelanden för användarna?

Chefer, författare och elever kan se meddelanden baserat på kursaktiviteterna. Administratören kan aktivera/inaktivera meddelanden för alla användare genom att följa stegen nedan:

1. Klicka på E-postmallar i den vänstra rutan och välj flikarna Allmänt, Användarregistrering, Slutföranden och Feedback.
1. Från händelserna som visas nedan klickar du på växlingsknapparna Nej/Ja bredvid **varje &#x200B;** händelse och väljer Ja för att aktivera meddelande. Klicka på Nej om du inte vill skicka meddelanden för en viss händelse.

+++

+++Hur tillåter jag extern registrering till kurserna?

Adobe Learning Manager ger dig möjlighet att registrera externa avdelningsmedlemmar eller anställda i din organisation på programmet.

1. Klicka på **[!UICONTROL Users]** i den vänstra rutan.
1. Klicka på **[!UICONTROL External]** i den vänstra rutan.
1. Klicka på **[!UICONTROL Add]** längst upp till höger på sidan.

   Dialogrutan Lägg till användare visas.

1. Lägg till profilnamnet, chefens e-postadress, tilldelade platser, utgångsinformation. Du kan också lägga till en bild i den externa profilen.
1. Klicka på **[!UICONTROL Save]**.

Administratören kan kopiera registreringsadressen och skicka den till den externa registreringsgruppen. De externa användarna kan registrera sig, logga in på Learning Manager-programmet och få tillgång till sina kurser.

+++

+++Hur lägger jag till frågeformulär för L1-feedback?

Skapa ett feedbackfrågeformulär som elever kan använda efter att ha slutfört kurserna. Det finns som standard tre exempelfrågor. Skapa ett frågeformulär genom att följa stegen nedan.

1. Klicka på Feedback i den vänstra rutan. Ett fönster med ett feedbackfrågeformulär visas.
1. Klicka på **[!UICONTROL Edit]** för att lägga till/ändra enkäten.

Du kan lägga till en uppsättning frågeformulär och välja att inte visa upp dem om du inte behöver dem. Klicka på kryssrutan för att aktivera/inaktivera en viss fråga.

+++

+++Hur ställer jag in kunskaper och nivåer?

1. Klicka på Kompetenser i den vänstra rutan i fönstret Administratör.
1. Klicka på Lägg till för att lägga till nya kompetenser.
1. Lägg till kompetensnamn, beskrivning och motsvarande poäng för varje nivå.

   Som standard kommer en enda nivå med 0 krediter att vara tillgänglig för varje kompetens.

1. Klicka på [!UICONTROL **Lägg till nivå**] för att lägga till en ny nivå för varje kompetens och klicka på Spara. Du kan lägga till upp till fem nivåer.

När kompetensen har sparats kan du inte ta bort nivåer från kompetensen. Administratören kan också tilldela elever en viss kompetens och nivå.

+++

+++Hur konfigurerar jag faktureringssystemet för min organisations kurser?

1. Klicka på [!UICONTROL **Fakturering**] i den vänstra rutan.

   Faktureringsinformation visas på sidan.

1. Klicka på fliken [!UICONTROL **Prenumerera**].
1. Skriv in antalet paket som du vill beställa i fältet Elevpaket och klicka på Beställ längst upp till höger på sidan.

   Välj antalet paket baserat på antalet elever i organisationen och gör beställningen. Om du vill ha en process som styrs av en inköpsorder kan du skriva till oss på [learningmanagersales@adobe.com](mailto:learningmanagersales@adobe.com).

1. Ange dina kontaktuppgifter, välj kreditkortstyp, ange kreditkortsuppgifter och klicka på Slutför beställning.

Mer information finns i [Faktureringshantering](/help/migrated/administrators/feature-summary/billing-management.md).

+++

+++Kan jag anpassa certifikatdesignen? Hur?

I Adobe Learning Manager kan du identifiera elever genom att utfärda utmärkelsetecken. Se funktionen Märken om du vill ha mer information.  Se även certifieringsfunktionen.

+++

+++Hur skapar jag företagsprofilen?

1. När du har loggat in som administratör klickar du på **[!UICONTROL Company Info]** i den vänstra rutan.
1. Lägg till företagsprofil, underdomän och logotyp genom att klicka på alla dessa alternativ på sidan.

+++

+++Hur lägger jag till kurser?

Om du vill lägga till kurser måste du byta roll som författare. Du kan bara visa listan över tillgängliga kurser baserat på deras status som **[!UICONTROL Complete]**, **[!UICONTROL Published]** och **[!UICONTROL Retired]**.

Klicka på **[!UICONTROL Courses]** i den vänstra rutan för att visa kurser. Se [Skapa kurser](/help/migrated/administrators/feature-summary/courses.md)för mer information

+++

+++Hur lägger jag till olika roller i programmet?

Följ stegen nedan om du vill lägga till nya användare:

1. Klicka på Användare i den vänstra rutan när du har loggat in som administratör. Du kan också lägga till användare genom att klicka på Komma igång i den vänstra rutan i fönstret och genom att klicka på Lägg till användare.
1. Om du vill lägga till nya användare klickar du på Lägg till längst upp till höger på sidan.

Som standard tilldelas alla nya användare en elevroll. Du kan tilldela administratörs- eller författarroller till eleverna genom att klicka på **[!UICONTROL Actions]** i det övre högra hörnet på sidan och välja **[!UICONTROL Assign Role]** > **[!UICONTROL Make Author]** eller **[!UICONTROL Make Admin]**.

Mer information om hur du lägger till elever, författare och administratörer finns i funktionen [Lägg till nya användare](/help/migrated/administrators/feature-summary/add-users-user-groups.md).

+++

+++Hur ändrar man en bakgrundsbild för en elev?

Kontakta supportteamet för Learning Manager.

+++

+++Var hittar jag mitt konto-ID för Learning Manager?

Du kan hämta konto-ID från webbläsaren där Learning Manager är öppet.

*/app/admin?i_qp_user_id=12761637&amp;**accountId=6849***

+++

+++Finns det en rapport jag kan skriva, eller en som någon kan dra för mig, som kommer att visa mig en lista över alla kurser i LMS?

Ja, du kan hämta en **[!UICONTROL Training Report]** som innehåller alla kurser, utbildningsprogram och certifieringar i LMS. Ladda ned rapporten genom att följa stegen nedan:

1. Logga in som administratör.
2. Klicka på **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]** > **[!UICONTROL Excel Reports]** > **[!UICONTROL Trainings Report]**.
3. Välj **[!UICONTROL All Trainings]** i listrutan.
4. Klicka på **[!UICONTROL Download]**.

+++

+++Var kan jag hämta datorversionen av programmet?

Följ stegen nedan för att hämta datorversionen:

1. Logga in som administratör.
2. Klicka på **[!UICONTROL Social Learning]** > **[!UICONTROL Settings]**.
3. Klicka på hyperlänken under **[!UICONTROL Download Configuration]** beroende på ditt operativsystem.

+++
