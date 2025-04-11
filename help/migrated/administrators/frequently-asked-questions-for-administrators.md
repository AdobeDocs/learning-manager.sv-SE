---
jcr-language: en_us
title: Vanliga frågor för administratörer
description: Vanliga frågor för Adobe Learning Manager-administratörer
contentowner: manochan
exl-id: 8b113a4e-73f4-4cd5-982a-cefdf5388e91
source-git-commit: 2548370c5b943964e200b6c1d5a4d0d9ca386ba6
workflow-type: tm+mt
source-wordcount: '2557'
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

+++Nytt Experience League-meddelande

Vi har nöjet att meddela att på vår resa mot en bättre anslutning till Adobe-familjen kommer Adobe Learning Manager att lägga till ytterligare en kanal i supportprocessen. Från 12 maj 2025 kan du nu skapa ärenden direkt från Adobe Experience League. I Experience League finns för närvarande Adobe Learning Manager självhjälpsdokumentation, användarhandböcker och bästa praxis. De kommer att vara din primära resurs för alla supportbehov, från självbetjäning till agentbaserad kommunikation. Vi uppskattar din förståelse och ditt stöd när vi gör denna viktiga övergång.

+++

+++Kan jag lägga till flera användare samtidigt? Hur?

Ja, du kan lägga till användare i grupp genom att använda funktionen för CSV-överföring. Klicka [här](/help/migrated/administrators/add-users-in-bulk.md) för mer information.

+++

+++Jag skrev fel e-post-ID när jag skapade inloggning för mina elever, hur korrigerar jag det?

För att fixa användarinloggning måste du importera CSV i Learning Manager. Ett exempel på en CSV-fil bifogas längst ned på den här sidan som referens. Eftersom e-post betraktas som en unik identifierare för en person kan den inte redigeras. Följ de här stegen:

1. Lägg till samma användare med rätt e-post-ID i CSV och se till att han förblir chef för andra användare genom att lägga till hans e-post-ID i kolumnen &quot;E-postadress till den anställdes chef&quot; i CSV-exempelfilen.
1. Lägg till andra användare i ditt konto i CSV-filen, inklusive dig själv
1. Importera den här filen från Learning Manager-administrationsprogrammet ->Användare ->Lägg till ->Importera CSV
1. Mappa alla fält, enligt anvisningarna i dialogrutan, till motsvarande CSV-kolumner.
1. Klicka på Spara.

Användare ska läggas till på sidan Elever.

[Exempel på CSV.csv för Learning Manager](https://helpx.adobe.com/content/dam/help/en/captivate_prime/learning-manager-sample-csv.zip)

+++

+++Hur ställer jag in varningar?

I Adobe Learning Manager 1.0 kan du skapa meddelanden. Mer information finns i  [frågan om](/help/migrated/administrators/feature-summary/user-notifications.md) meddelanden.

+++

+++Hur lägger jag till certifikat för kurserna?

Adobe Learning Manager tillhandahåller inte certifikat för kurserna. Administratören kan dock skapa utmärkelsetecken för varje kurs genom att klicka på fliken Märken i den vänstra panelen. När administratören skriver in elever till en kurs kan han också koppla ett märke tillsammans med den.

+++

+++Hur importerar jag signaturer för certifikaten?

I Adobe Learning Manager finns det ingen funktion för att importera signaturer för certifieringen eller märket.

+++

+++Kan jag sätta upp en kalender för kurserna? Hur?

I Adobe Learning Manager 1.0 har vi inga möjligheter att ställa in kalendern för kurserna.

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
1. Från listan över tillgängliga kurser klickar du på kursnamnet för valfri klassrumsmodul/kurs. En ny sida visas med detaljerad information om kursen.
1. Välj eleverna och klicka på Spara för att registrera slutförandet av kursen.

Om det finns flera moduler i en kurs och eleven bara har slutfört en av dem, kan du välja en enskild modul och klicka på Spara för att markera slutförandet för eleven. Om eleven slutför alla moduler i en kurs kan du klicka på alternativet Välj alla och klicka på Spara.

För mer information, se  [funktionen för väntelista och närvaro](/help/migrated/administrators/feature-summary/waitlist-attendance-management.md) .

+++

+++Hur inkluderar jag alternativet med L3-feedback?

Du kan lägga till feedback om L3 medan du registrerar elever till kurserna. Lägg till en L3-feedbackfråga genom att följa stegen nedan:

1. Klicka på Kurser i den vänstra rutan när du har loggat in som administratör. Listor över alla kurser visas på den högra sidan.
1. Klicka på den kursruta som du vill lägga till L3-återkoppling för
1. Klicka på instansstandard i den vänstra rutan.
1. Klicka på cirkeln på växlingsknappen bredvid L3 - Feedback om beteendeförändring för att välja den.
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
1. Välj en eller flera färdigheter genom att klicka på kryssrutor för varje kompetens och klicka på **[!UICONTROL Actions]** rullgardinsmenyn längst upp till höger på sidan.
1. Klicka på Tilldela till användare.
1. Börja skriva namnet på användaren, välj i listrutan och klicka på **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Du kan registrera flera elever för färdigheter genom att klicka på Lägg till fler användare och genom att upprepa det fjärde steget.

+++

+++Hur skapar man en session för utbildningsprogram?

Skapa ett utbildningsprogram genom att följa stegen nedan:

1. Klicka på Utbildningsprogram i den vänstra rutan. Sidan Utbildningsprogram visas med en lista över befintliga utbildningsprogram.
1. Klicka på Lägg till längst upp till höger på sidan.\
   Ange programnamn, översikt, beskrivning och klicka på Spara.
1. Klicka på Kurser i den vänstra rutan.
1. Lägg till en eller flera banor genom att klicka på + på varje kursruta.

   >[!NOTE]
   >
   >Du måste publicera utbildningsprogrammet innan du registrerar elever eller en instans.

1. Klicka på Instanser i den vänstra rutan och klicka på **[!UICONTROL Add new instances]** i det högra hörnet av sidan för att inkludera information om instansen.

Mer information om utbildningsprogram finns i [Funktionen Utbildningsprogram.](/help/migrated/administrators/feature-summary/learning-programs.md)

+++

+++Hur ändrar eller anpassar jag rapporter för alla roller?

Klicka på rullgardinspilen i det övre högra hörnet av varje rapport för att redigera/ändra rapporter. Klicka på Spara när du har slutfört ändringarna och visa den ändrade rapporten.

+++

+++Hur ändrar jag kurser, utbildningsprogram och företagsprofil?

Du kan redigera kurser eller utbildningsprogram även efter att du har publicerat dem. Mer information finns i hjälpinnehållet för  [kurser](/help/migrated/administrators/feature-summary/courses.md) och  [utbildningsprogram](/help/migrated/administrators/feature-summary/learning-programs.md) .

Om du vill ändra företagsprofilen klickar du på **[!UICONTROL Settings]** i den vänstra rutan och sedan på **[!UICONTROL Change]** i det övre högra hörnet på sidan.

+++

+++Hur söker jag efter kurserna?

Klicka på Kurser i den vänstra rutan när du har loggat in som administratör. En lista över alla tillgängliga kurser visas.

Du kan söka på kurser på två sätt:

1. Klicka på sökikonen som visas i det övre högra hörnet. Ett sökfält visas. Skriv in kursnamnet eller några nyckelord som är associerade med dina kurser för att hitta dina kurser.
1. Genom att filtrera listan över kurser med hjälp av filtren.

Du kan filtrera kurserna efter tillstånd, till exempel Alla, publicerade och Tillbakadragna, genom att klicka på vart och ett av dessa alternativ. Du kan också söka baserat på kompetenser genom att klicka på Kompetenser och genom att välja var och en av dem.

Baserat på ditt val kan du se den filtrerade listan över kurser och välja de kurser som krävs.

+++

+++Kan jag ändra teman för applikationen? Hur?

Ja, du kan ändra teman och varumärke för Learning Manager-applikationen enligt kraven i din organisation. En uppsättning med fem representativa bilder tillhandahålls för att förhandsgranska dina färgtemaändringar innan du tillämpar dem på ditt program. Bläddra igenom dessa bilder genom att klicka &lt; and > på symbolerna till vänster respektive höger sida av bilderna för att förhandsgranska.

Klicka **[!UICONTROL Branding]** på den vänstra rutan för att uppdatera ditt organisationsnamn, ändra underdomän, loggstilar och teman. Klicka intill **[!UICONTROL Edit]** vart och ett av dessa avsnitt för att ändra innehållet.

Mer information finns i hjälpen](/help/migrated/administrators/feature-summary/themes.md) för [färgteman och varumärken.

+++

+++Hur ställer jag in emblem för kurserna?

1. Klicka på Märken i den vänstra rutan när du har loggat in som administratör.
1. Klicka på Lägg till längst upp till höger på sidan som visas.
1. LÄGG TILL UTMÄRKELSENAMN.
1. Ladda upp märket genom att klicka på Ladda upp märke och klicka på Spara.

+++

+++Hur ställer jag in spelifieringspoäng för banorna?

Du kan ställa in spelifieringspoäng för elever genom att följa stegen nedan:

1. Klicka på Spelifiering när du har loggat in som administratör. En sida visas med en lista över brons-, silver-, guld- och platinanivåer och de poäng som krävs för att uppnå motsvarande varje nivå. Det finns en lista med uppgifter och motsvarande punkter.
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

+++Hur inkluderar jag aviseringar för användarna?

Chefer, författare och elever kan se aviseringar baserat på kursaktiviteterna. Administratören kan aktivera/inaktivera aviseringar för alla användare genom att följa stegen nedan:

1. Klicka på E-postmallar i den vänstra rutan och välj flikarna Allmänt, Användarregistreringar, Slutföranden och Feedback.
1. Från händelserna nedan klickar du på växlingsknapparna Nej/Ja intill **varje **händelse och väljer Ja för att aktivera avisering. Klicka på Nej om du inte vill skicka meddelanden för en viss händelse.

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

Skapa ett frågeformulär för återkoppling som kan användas av eleverna efter att ha slutfört kurserna. Tre exempelfrågor är tillgängliga som standard. Skapa ett frågeformulär genom att följa stegen nedan.

1. Klicka på Feedback i den vänstra rutan. Ett fönster med ett feedbackfrågeformulär visas.
1. Klicka på **[!UICONTROL Edit]** för att lägga till/ändra enkäten.

Du kan lägga till en uppsättning frågeformulär och välja att inte visa upp dem om du inte behöver dem. Klicka på kryssrutan för att aktivera/inaktivera en viss fråga.

+++

+++Hur ställer jag in färdigheter och nivåer?

1. Klicka på Kompetenser i den vänstra rutan i administratörsfönstret.
1. Klicka på Lägg till för att lägga till nya kompetenser.
1. Lägg till kompetensnamn, beskrivning och motsvarande poäng för varje nivå.

   Som standard kommer en enda nivå med 0 poäng att vara tillgänglig för varje kompetens.

1. Klicka på [!UICONTROL **Lägg till nivå**] för att lägga till en ny nivå till varje kompetens och klicka på Spara. Du kan lägga till upp till 5 nivåer.

När kompetensen har sparats kan du inte ta bort nivåer från kompetensen. Administratören kan också tilldela elever till en viss kompetens och nivå.

+++

+++Hur ställer jag in faktureringssystem för min organisations kurser?

1. Klicka på [!UICONTROL **Fakturering**] i den vänstra rutan.

   Faktureringsinformation visas på sidan.

1. [!UICONTROL **Klicka på fliken Prenumerera**].
1. Skriv in antalet paket som du vill beställa i fältet Elevpaket och klicka på Beställ längst upp till höger på sidan.

   Välj antal paket baserat på antalet elever i din organisation och gör din beställning. För en inköpsorderdriven process, skriv till oss på  [learningmanagersales@adobe.com](mailto:learningmanagersales@adobe.com).

1. Ange din kontaktinformation, välj kreditkortstyp, ange kreditkortsuppgifter och klicka på Slutför beställning.

Mer information finns i [Faktureringshantering](/help/migrated/administrators/feature-summary/billing-management.md).

+++

+++Kan jag anpassa certifikatdesignen? Hur?

I Adobe Learning Manager kan du känna igen elever genom att dela ut märken. Se funktionen Märken om du vill ha mer information.  Se även Certifieringsfunktion.

+++

+++Hur ställer jag in min företagsprofil?

1. När du har loggat in som administratör klickar du på **[!UICONTROL Company Info]** i den vänstra rutan.
1. Lägg till företagsprofil, underdomän, logotyp genom att klicka på vart och ett av dessa alternativ på sidan.

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

+++Finns det en rapport som jag kan ta fram, eller en som någon kan ta fram åt mig, som visar mig en lista över alla kurser i LMS:et?

Ja, du kan dra en **[!UICONTROL Training Report]** som innehåller alla kurser, inlärningsprogram, certifiering i LMS. Följ stegen nedan för att ladda ner rapporten:

1. Logga in som administratör.
2. Klicka på **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]** > **[!UICONTROL Excel Reports]** > **[!UICONTROL Trainings Report]**.
3. Välj **[!UICONTROL All Trainings]** i listrutan.
4. Klicka på **[!UICONTROL Download]**.

+++

+++Var kan jag ladda ner skrivbordsversionen av appen?

Följ stegen nedan för att ladda ner skrivbordsversionen:

1. Logga in som administratör.
2. Klicka på **[!UICONTROL Social Learning]** > **[!UICONTROL Settings]**.
3. Under **[!UICONTROL Download Configuration]** klickar du på hyperlänken beroende på ditt operativsystem.

+++
