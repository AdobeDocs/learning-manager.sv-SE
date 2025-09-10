---
jcr-language: en_us
title: Integrera Adobe Learning Manager med AEM
description: Learning Manager är ett system för hantering av inlärning med ett inbyggt system för hantering av utbildningsinnehåll. Användarna hanterar sitt utbildningsinnehåll genom att ladda upp det till Learning Manager så att Learning Manager utför versionshantering, allokering till kurser, definierar synligheten för elever , spårar förbrukning och rapporterar tillbaka till administratörer.
contentowner: saghosh
exl-id: 61fae7bd-1703-4ed1-9bd9-07387d67a91c
source-git-commit: aa8a45427e7e78ac66a21531a9511bf9a21d03b4
workflow-type: tm+mt
source-wordcount: '3047'
ht-degree: 0%

---


# Integrera Adobe Learning Manager med AEM

Adobe Learning Manager (ALM) integreras med Adobe Experience Manager-webbplatser (AEM). Det gör att du kan skapa en egen webbplats och responsiva mobilgränssnitt för Adobe Learning Manager med minimal kodning. Med denna integrering kan du skapa anpassade utbildningsupplevelser för dina användare.

För att skapa en sådan upplevelse tillhandahåller ALM ett Adobe Learning Manager-referenspaket för webbplats (ALM-referenspaket för webbplats) för AEM Sites i form av en ZIP-fil som du kan installera på din AEM Sites-instans.

Paketet innehåller webbsidesmallar och webbplatskomponenter från AEM Sites tillsammans med inbäddningsbara widgetar, t.ex. Utbildningskatalog, inbäddade widgetar, kalender och så vidare.

När du har installerat ALM-referenspaketet kan du börja skapa en webbplats för Adobe Learning Manager som du kan vara värd för på din AEM Sites-instans. Användarna kan sedan dra och släppa komponenterna på webbplatsen.

>[!IMPORTANT]
>
>ALM-paket (Adobe Learning Manager) för AEM Sites är ett snabbstartskodblock för implementering. Detta paket är utformat för fjärradministrerad driftsättning. Efter implementeringen av den tillhandahållna kodbasen ska den implementerande parten ansvara för löpande underhåll och vidareutveckling, vilket är praxis med fjärradministrerade program baserade på Adobe Learning Manager.

## Installera ALM-referensplatspaket

### Krav

* Licenser för AEM Sites och Adobe Commerce.
* AEM On-premise 6.5 eller Adobe Experience Manager - Cloud Service
* Adobe Commerce 2.4.3

När du har skyddat AEM Sites-miljön måste du installera ALM-referenspaketet. Detta paket innehåller AEM-webbsidor och webbplatskomponenter som hjälper dig att konstruera utbildningsplattformen.

Referenswebbplatspaketet finns på [**GitHub-databasen**](https://github.com/adobe/adobe-learning-manager-reference-site/releases/tag/1.0.0).

Mer information finns i filen VIKTIGT.

## Hämta innehållspaketet {#downloadthecontentpackage}

Installationsprogrammet levereras som ett AEM-innehållspaket. [***Hämta paketet***](https://github.com/adobe/adobe-learning-manager-reference-site).

Innehållspaketet, som finns som en zip-fil, är kompatibelt med AEM 6.4 och AEM 6.5.

## Installera Learning Manager-komponent {#installcaptivateprimecomponent}

Installera Learning Manager-innehållspaketet med hjälp av AEM Package Manager:

>[!NOTE]
>
>Mer information om hur du installerar paket finns i [***Arbeta med paket***](https://experienceleague.adobe.com/docs/experience-manager-65/administering/contentmanagement/package-manager.html?lang=sv-SE#how-to-work-with-packages).

1. Öppna AEM Package Manager när du är AEM-författare.
1. Klicka på knappen **[!UICONTROL Upload Package]**.
1. Klicka på **[!UICONTROL Browse]** och överför innehållspaketet.
1. Klicka på **[!UICONTROL Upload]**.
1. När paketet har överförts installerar du innehållspaketet genom att markera det och klicka på **[!UICONTROL Install]**.

   ![](assets/install-package.jpg)

   *Installera innehållspaketet*

## Skapa ett program i [!DNL Adobe Learning Manager]

När du har installerat AEM-webbplatspaketet måste du konfigurera ett ALM-program för att ansluta utbildningsportalen till AEM-webbplatsen.

Detta scenario gäller när AEM används med [!DNL Adobe Learning Manager].

Följ stegen nedan:

1. Klicka på **[!UICONTROL Applications]** som integreringsadministratör.
1. Om du vill skapa ett nytt program klickar du på **[!UICONTROL Register]** i det övre högra hörnet på sidan.
1. Ange följande information på skärmen Registrera ett nytt program:

   1. Programnamn: Namnet på programmet som du skapar.
   1. URL: Din organisations URL.
   1. Omdirigeringsdomäner: Värddomänerna för AEM-webbplatsen. Du kan även använda jokertecken.
   1. Beskrivning: Beskrivning av programmet.
   1. Omfång: Välj läsåtkomst för elevrollen och elevrollen skrivåtkomst.
   1. Endast för det här kontot?: Välj Ja om du vill använda programmet för det befintliga ALM-kontot.

1. När du har gjort ändringarna klickar du på Spara.

Anteckna programautentiseringsuppgifterna från skärmen.

![](assets/application-credentials.png)
*Programautentiseringsuppgifter*

Klicka på **[!UICONTROL Approve]** för att godkänna programmet.

## Hämta token

1. Klicka på **[!UICONTROL Access Tokens for Testing and Development]** på fliken Utvecklarresurser.

   ![](assets/access-tokens.png)

   *Välj åtkomsttoken för testning och utveckling*

1. Ange följande uppgifter:

   ![](assets/access-token-details.png)
   *Ange tokeninformation*

   1. Hämta OAuth-kod: Ange klient-ID från föregående avsnitt och ändra omfånget. Klicka på Skicka för att få OAuth-koden.
   1. Hämta uppdateringstoken: Ange klient-ID:t och hemligheten från föregående avsnitt. Ange även OAuth-koden som du fick från föregående steg. Klicka på Skicka.
   1. Hämta åtkomsttoken: Ange klient-ID:t och hemligheten från föregående avsnitt. Ange även uppdateringstoken som du fick från föregående steg. Klicka på Skicka.
   1. Hämta information om åtkomsttoken: Ange den åtkomsttoken som du fick i det föregående steget. Klicka på Skicka.

1. Du kan hämta informationen från JSON-svaret som följer. Svaret består av åtkomsttoken, uppdateringstoken, användarroll, konto-ID, användar-ID och hur lång tid som förfaller. Notera uppdateringstoken eftersom du kommer att återanvända den.

## Konfigurera ALM-konto i AEM

1. Starta din AEM-instans.
1. Klicka på Inställningar > Cloud Service.
1. Klicka på Konfiguration av Adobe Learning Manager.

   ![](assets/alm-configuration.png)
   *Välj Adobe Learning Manager-konfiguration*

1. Klicka på Skapa > Konfigurationsmapp. Ge mappen ett namn.

   ![](assets/create-folder.png)
   *Skapa konfiguration*

1. Välj den konfiguration du skapade i utbildningsprojektet.

1. Ange konfigurationsinformation.

   ![](assets/account-congiguration.png)
   *Skapa konfigurationsmappen*

   1. Adobe Learning Manager-läge: Välj hur du vill att elever som är inloggade och inte är det ska lära sig.
   1. Adobe Learning Manager-URL: Ange URL:en till ALM-instansen där utbildningstjänsterna finns.
   1. Konto-ID: ID för ALM-kontot.
   1. Klient-ID, Klienthemlighet och Författarens uppdateringstoken: Ange de autentiseringsuppgifter du fick när du skapade programmet i ALM.
   1. Anpassning av widget: Mer information finns i [Integrera med AEM](/help/migrated/integrate-aem-learning-manager.md) `.`

1. Spara och stäng konfigurationen.

### AEM + Adobe Learning Manager (inloggade/ej inloggade användare)

Med Adobe Learning Manager kan du nu visa upp dina produkter och utbildningar för befintliga och potentiella kunder och partner utan att behöva skapa eller logga in konton. Den här funktionen hjälper dig att anpassa produkter och utbildningar genom att ge elever en snabb och enkel förhandsvisning av utbildningen, vilket hjälper till att framhäva och främja produktfunktioner. Därför kan du effektivt visa upp dina produkter och erbjudanden, särskilt för potentiella kunder och partners, vilket resulterar i ökad produktmedvetenhet. Enkel åtkomst och bättre åtkomlighet leder till ökat intresse, vilket hjälper till att driva utbildningsregistreringar och inlärningsanpassning.

Med hjälp av det här arbetsflödet kan en elev förhandsgranska en utbildning, få tillgång till utbildningsinformation eller söka efter utbildning utan att logga in på Adobe Learning Manager. Det här arbetsflödet gäller inte det inbyggda Learning Manager-gränssnittet (gäller ENDAST AEM Sites och andra fjärradministrerade gränssnitt).

**Konfigurera och aktivera anslutningen för utbildningsplattformen**

I det här avsnittet beskrivs de steg som krävs för att konfigurera och aktivera följande anslutning:

**Åtkomst till utbildningsdata**

Med den här anslutningen kan ditt AEM Sites-baserade eller något annat anpassat användargränssnitt hämta och återge utbildningsinformation till eleverna och göra en sömlös sökning efter utbildningsinformation antingen före eller efter att en elev loggar in.

Den här anslutningen krävs bara om du använder AEM Sites-baserade eller andra fjärradministrerade gränssnitt.

Kopplingen exporterar utbildningsmetadata till en datalagrings- och hämtningslösning samt ett sökaktiveringssystem. Du kan därför konfigurera ditt AEM Sites-baserade eller något annat anpassat användargränssnitt för användning av dessa två tjänster för att hämta utbildningsdata, återge webbsidor och ge eleverna tillgång till optimerade sökfunktioner för utbildning. Ett gränssnitt som inte är inloggat i AEM Sites kan till exempel använda de exporterade metadata som är till hjälp för en elev att söka efter, bläddra bland och komma åt utbildningssidor som visar utbildningsinformation.

Aktivera den här anslutningen för att skapa och återge dina AEM Sites-baserade webbsidor och leverera anpassade upplevelser till dina elever både före och efter inloggningen. Aktivera den här anslutningen för att skapa och återge dina AEM Sites-baserade webbsidor och leverera anpassade upplevelser till dina elever både före och efter inloggningen.

* Bas-URL för Adobe Learning Manager CDN - Ange bas-URL:en för CDN-tjänstsökvägen för datahämtning från anslutningssidan för utbildningsdataåtkomst.
* Uppdateringstoken för administratör - Ange den uppdateringstoken som du fastställde i det tidigare avsnittet.
* Bas-URL för utbildningsmetadata - ange bas-URL:en för sökaktiveringen och sökvägen till sökdatahämtningstjänsten från sidan Anslutning av utbildningsdata.
* URL för Adobe Learning Manager-registrering - ange URL för självregistrering som genererats av kontots integreringsadministratör och som används av elever för att registrera sig för utbildning.

### AEM + Adobe Learning Manager + Adobe Commerce (inloggade/ej inloggade användare)

Adobe Learning Manager tillhandahåller nu lösningar som hjälper dig att sömlöst integrera utbildningsplattformen med Adobe Commerce. Med den här versionen kan du enkelt ansluta dina inbyggda AEM-platsbaserade eller andra Headless Learning Manager-gränssnitt till Adobe Commerce. Med integreringen kan du förverkliga e-handelsmöjligheter inom utbildningsplattformen. Du kan nu erbjuda kunder och affärspartners betald utbildning samt enkelt möjliggöra inköp av utbildning i både inbyggda och icke-inbyggda Learning Manager-gränssnitt. En elev kan även förhandsgranska en utbildning, få tillgång till utbildningsinformation eller söka efter utbildning utan att logga in på Adobe Learning Manager.

En användare kan använda det redan befintliga AEM-programmet och godkänna det i stället för att skapa ett.

* Bas-URL för Adobe Learning Manager CDN - Ange bas-URL:en för CDN-tjänstsökvägen för datahämtning från anslutningssidan för Adobe Commerce.
* Adobe Commerce-URL - Ange URL:en till den Adobe Commerce-instans du använder.
* GraphQL-proxysökväg - Komponenterna för Learning Manager på klientsidan kommer åt Adobe Commerce GraphQL-slutpunkten direkt, och därför kan CORS-fel uppstå. För att undvika det här felet måste alla anrop antingen skickas från samma slutpunkt som AEM eller skickas via en proxy som lägger till CORS-rubriker.
* Adobe Commerce-butiksnamn - Ange det Adobe Commerce-butiksnamn som du fastställde i det tidigare avsnittet.
* Livslängd för Adobe Commerce-kundtoken (i sekunder) - Ange livstid för kundtoken som anger den förutbestämda perioden för en inloggningssession.
* Uppdateringstoken för administratör - Ange den uppdateringstoken som du fastställde i det tidigare avsnittet.

## Anpassa webbsidor

Anpassa dina webbsidor med hjälp av webbplatsen AEM-referenser och de tillgängliga widgetarna.

1. Starta din AEM-instans.
1. Klicka på Webbplatser och öppna konfigurationssidan.
1. Klicka på **[!UICONTROL Learning Site]** > **[!UICONTROL Language Masters]** > **[!UICONTROL English]**. Alla webbsidor i projektet ingår i mappen.

   ![](assets/list-webpages.png)
   *Visa alla webbsidor*

1. Välj en mall och klicka på **[!UICONTROL Edit]**.

1. På sidan klickar du på knappen Komponentinställningar och ändrar komponentens egenskaper.

   ![](assets/settings-button.png)
   *Knappen Välj inställningar*

1. Förhandsgranska ändringarna eller publicera sidan.

## Skapa webbsidor

Förutom de mallar du kan använda som tillhandahålls av referenspaketet för webbplatser kan du också skapa webbsidor baserade på mallarna i AEM.

1. På AEM-huvudsidan klickar du på Skapa > Sida.

1. Välj den mall som du vill anpassa. Klicka på Nästa.

1. Ange sidegenskaper.

   ![](assets/page-properties.png)
   *Sidegenskaper*

1. Klicka på **[!UICONTROL Create]** för att skapa sidan.

1. Välj den nya sidan och klicka på **[!UICONTROL Edit]**.

1. Infoga en komponent på sidan, till exempel **Utbildningsinnehåll**.

   ![](assets/learning-content.png)
   *Filtrera efter plats*

1. Välj de katalogfilter som ska visas på sidan.

## Skapa webbplats från utkast

ALM-referenspaketet innehåller en plan för utbildningswebbplatsen som du kan använda för att skapa en webbplats för utbildningsplattformen. Med AEM-ritningar kan du skapa webbsidor direkt från AEM Sites-komponenter. Du behöver inte använda några mallar.

1. Klicka på **[!UICONTROL Sites]** på AEM-startsidan.

1. Klicka på **[!UICONTROL Create]** > **[!UICONTROL Site]**.

1. Klicka på Utskrift av utbildningswebbplats.

   ![](assets/learning-site-blueprint.png)

   *Skapa en webbplats från utkast*

1. Klicka på Nästa.

1. På egenskapssidan anger du sidans metadata. Klicka på Skapa.

   ![](assets/blueprint-properties.png)
   *Välj plan för utbildningswebbplats*

1. Klicka på hyperlänken Hem om du vill gå till startsidan för webbplatsen som du har skapat. På den här sidan kan du anpassa widgetarna och katalogkomponenterna.

## Koda din webbplats

Förutom att använda de inbyggda mallarna och skapa din webbplats från grunden med hjälp av WYSIWYG-komponenterna, kan du också skriva kod och bygga webbplatsen.

Koden finns i [GitHub-referensplatsen](https://github.com/adobe/adobe-learning-manager-reference-site) så att du kan komma igång.

Huvuddelarna i mallen är:

* kärna: Java-paket som innehåller alla kärnfunktioner som OSGi-tjänster, lyssnare eller schemaläggare, samt komponentrelaterad Java-kod som servlets eller begärandefilter.
* ui.apps: innehåller /apps (och /etc) delar av projektet, dvs JS&amp;CSS-klientbibliotek, komponenter, mallar.
* ui.content: Innehåller exempelinnehåll med komponenterna från ui.apps
* ui.frontend: Innehåller React-komponenter.

All kod finns i rapporten så att du kommer igång.

## Importera och lägg till Learning Manager-komponenter på befintlig webbsida eller i befintlig mall

När du installerar AEM-referensplatspaket läggs Learning Manager-komponenterna till i din AEM Sites-instans. Som standard kan du lägga till de här komponenterna på webbprojektets (webbplats) utbildningswebbplats, som vi tillhandahåller direkt i lådan. Dessa komponenter finns även på webbplatsen som du skapar från planen för utbildningswebbplatsen.

Om du vill använda dessa nyligen tillagda Learning Manager-komponenter i ditt befintliga webbprojekt eller på din webbplats bör du importera dem på följande sätt.

1. Installera ALM-referensplatspaketet.

1. Öppna webbprojektet och gå till HTML-filen (för den webbsida eller webbmall där du vill lägga till komponenterna i Learning Manager).
1. Ansluta till ett möte

   Öppna HTML-filen och lägg till följande kodfragment i sidkomponenten så att koden körs innan utbildningskomponenterna som finns i sidåtergivningen.

   *`<sly data-sly-use.configModel="com.adobe.learning.core.models.GlobalConfigurationModel"/>`*
   *`<meta name="cp-config" content="${configModel.config}" />`*

   Föregående kod lägger till den mappade konfigurationen i metataggen på sidan, vilket krävs för att utbildningskomponenterna ska återges. Mer information finns på [referenswebbplatsen för Adobe Learning Manager](https://github.com/adobe/adobe-learning-manager-reference-site/blob/master/ui.apps/src/main/content/jcr_root/apps/learning/components/page/customheaderlibs.html).

1. Se till att du har mappat konfigurationen till webbprojektet.
1. Öppna AEM Sites-mallen där du vill importera Learning Manager-komponenterna.
1. På mallsidans redigerare går du till behållaren Tillåtna komponenter och väljer **Policy**.
1. På sidan Policy går du till Egenskaper > Tillåtna komponenter och väljer följande komponenter: Utbildning - innehåll, Utbildning - formulär och Utbildning - struktur

Följande procedur gör att mallen kan uppfylla klientbiblioteksberoendena för de importerade Learning Manager-komponenterna.

Webbsidorna som innehåller dessa komponenter bör läsa in dessa bibliotek för att kunna återge och använda komponenterna.

1. På mallsidans redigerare klickar du på Sidinformation och sedan på Sidpolicy.
1. På sidan Policy går du till Egenskaper > Klientbibliotek och lägger till dessa på mallsidan:

   1. learning.site
   1. learning.ui
   1. learning.commerce

När du har sparat den här mallen kan du lägga till Learning Manager-komponenterna på alla webbsidor som härleds från mallen.

## Konfigurera widgeten i AEM {#configurethewidgetinaem}

För widgetkonfiguration behöver AEM-skaparen bara den uppdateringstoken som tillhandahålls av integreringsadministratören för Learning Manager.

Du kan också ange flera kontokonfigurationer på flera sidor.

1. Klicka på **[!UICONTROL Tools]** > **[!UICONTROL Cloud Services]** > **[!UICONTROL Learning Manager Widget Configuration]**.
1. Klicka på **[!UICONTROL Create]**.
1. Ange uppdateringstoken här. Förbered de andra inställningarna.
1. Värdnamn bör ändras till &quot;learningmanagereu&quot; för EU-regioner.
1. Spara och stäng konfigurationen.
1. Välj en konfiguration och publicera den.

## AEM Author {#aemauthor}

AEM-skaparen måste först lägga till komponenten i AEM-mallen

AEM-utvecklaren kan sedan dra och släppa Adobe Learning Manager-komponenten och konfigurera därefter.

Learning Manager-komponenten kräver att den konfiguration som skapades i ovanstående steg mappas till sidan.  Författaren kan mappa konfigurationen genom att redigera sidegenskaper under **[!UICONTROL Advanced]** > **[!UICONTROL Configuration]** > **[!UICONTROL Cloud Configuration]** och ange sökvägen till konfigurationen. På så sätt kan författaren skapa konfigurationer för flera Learning Manager-konton och mappa var och en till olika webbplatser-sidor. Om en konfiguration inte mappas till sidan läser komponenten konfigurationen från mallsidan rekursivt tills den hittar en.

## Elev {#learner}

Eleven kan ta kurserna från sidan.

För att kunna komma åt Learning Manager-widgeten måste eleven vara en inloggad AEM-användare. Egenskapen **email** ska också finnas i noden /profile i elevens rep:User-nod. Denna e-postadress ska vara exakt densamma som den som finns i Learning Manager-kontot.

Eleven kan ta kurserna från sidan.

Kursens förlopp sparas också.

Följande widgetar finns:

1. Spelifiering
1. Utbildningskalender
1. Social widget
1. Katalogwidget
1. Mitt lärande
1. Rekommendation baserad på kollegialt lärande
1. Recommendations efter administratör
1. Rekommendation baserat på elevintressen

Om det inte finns några rekommendationer visas widgeten tom.

## Stöd för Skyline

Skyline är molnversionen av AEM. Du måste först installera Skyline från pakethanteraren. För att kunna använda Skyline-komponenten i AEM måste en användare finnas i Learning Manager-kontot. Med andra ord måste användarens e-postadress finnas i kontot.

### Distribuera Stadssilhuett

Stegen för att konfigurera Skyline nämns i [GitHub-rapporten](https://github.com/adobe/captivate-prime-aem-components).

## Min utbildningswidget

Med widgeten **[!UICONTROL My Learning]** kan du visa utbildning från en viss katalog eller en uppsättning kataloger för en användare.

Välj **[!UICONTROL Properties]** bland alternativen i avsnittet **[!UICONTROL Catalog]** i sidegenskaperna.

<!--![](assets/catalog-widget.png)-->

Katalogalternativen innehåller följande alternativ:

* **[!UICONTROL Catalog ids]:** Kommaavgränsade katalog-ID:n som utbildningen måste visas för.
* **[!UICONTROL Sort]:** Sorteringsordning för utbildningen. Alternativen är - namn, datum, skapad, datumRegistrerad och så vidare.
* **[!UICONTROL Learner State]:** Returnerar all utbildning som använder följande som filter: registrerad, påbörjad, slutförd och inte registrerad. Sökresultaten visas inte om sorteringsalternativet är dateEnrolled, dueDate eller dateEnrolled.
* **[!UICONTROL Skill name]:** Den kompetens som används för att filtrera exakt utbildning.
* **[!UICONTROL Tag name]:** Taggen som används för att filtrera exakta resultat.

Här är några ytterligare komponenter som du kan anpassa:

**[!UICONTROL Learning Object Types]:** Filter enligt typen för utbildningsobjektet. De typer som stöds är: kurs, certifiering, jobAid och learningProgram.

I AEM kommer korttiteln i en remsa att vara tom från början. I Egenskaper skriver du titeln i widgets.html.

**Anpassning**

Du kan anpassa utseendet och känslan på layouten med hjälp av widgets.html. Du kan ändra utseendet på korten som visas och anpassa temat.

I avsnittet **[!UICONTROL General Settings]** kan du välja primär- och sekundärfärger för korten och ange egenskaper för att anpassa temat.

```
{ 
 "globalCssText":"@import url('https://fonts.googleapis.com/css2?family=Grandstander:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');", 
 "fontNames":"Grandstander", 
 "cardLayout":{ 
 "cardLayoutName":"compact", 
 "cardPrimaryColor":"#376BA4", 
 "cardSecondaryColor":"#F98EB0", 
 "startedStateTextColor":"#ffffff", 
 "continueStateTextColor":"#ffffff", 
 "revisitStateTextColor":"#ffffff", 
 "startedStateColor":"#a0a0a0", 
 "continueStateColor":"#f9a122", 
 "revisitedStateColor":"#7fbc64", 
 "textPrimaryColor":"#ffffff", 
 "textSecondaryColor":"#d93f3f", 
 "navIconColor":"#a0a0a0" 
 } 
}
```

### Konfigurera widgetarna för Mina sparade kurser på AEM-webbplatser

Med widgeten Sparade kurser kan elever visa bokmärkta eller sparade kurser direkt på sina utbildningssidor, vilket ger enkel åtkomst till kurser de vill gå igenom eller slutföra senare.

Så här konfigurerar du widgeten Mina sparade kurser på AEM-webbplatser:

1. Starta AEM-webbplatserna.
2. Öppna sidan i läget **[!UICONTROL Edit]**.
3. Gå till **[!UICONTROL Components Browser]** och lägg till **[!UICONTROL My Learning widget]** på sidan.
4. Markera komponenten och välj sedan **[!UICONTROL Configure]**.
5. Välj **[!UICONTROL My Saved Courses]** i listrutan i **[!UICONTROL Properties]**.
6. Välj **[!UICONTROL Done]** och uppdatera sedan sidan i läget **[!UICONTROL Preview]** eller **[!UICONTROL Publish]**.

Widgeten visar de sparade kurserna för eleverna.


### Ignorera högre ordning för LO-registrering

Om kryssrutan **Ignorera registrering av högre ordningsföljd** är aktiverad och en användare registreras direkt i ett utbildningsprogram eller en certifiering, kommer kurserna för det certifieringen eller utbildningsprogrammet att visas för användaren i widgetarna.

Om kryssrutan är inaktiverad visas inte de kurser som finns i utbildningsprogrammet eller certifieringen där användaren inte har registrerat sig direkt.

![](assets/higher-order-lo.png)

*Markera kryssrutan Ignorera registrering till högre order-LO.

Inställningen används sedan på widgeten.

### Säkerhet

Fälten Klient-ID och Klienthemlighet läggs till. Dessutom maskeras uppdateringstoken. När en användare har skapat hela konfigurationen, om användaren öppnar konfigurationen igen för att redigera den eller om någon annan användare öppnar den här konfigurationen, maskeras uppdateringstoken.
