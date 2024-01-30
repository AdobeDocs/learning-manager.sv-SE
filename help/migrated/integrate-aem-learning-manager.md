---
jcr-language: en_us
title: Integrera Learning Manager med AEM
description: Learning Manager är ett system för hantering av inlärning med ett inbyggt system för hantering av utbildningsinnehåll. Användarna hanterar sitt utbildningsinnehåll genom att ladda upp det till Learning Manager så att Learning Manager utför versionshantering, allokering till kurser, definierar synligheten för elever , spårar förbrukning och rapporterar tillbaka till administratörer.
contentowner: saghosh
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '1031'
ht-degree: 0%

---



# Integrera Learning Manager med AEM

Learning Manager är ett system för hantering av inlärning med ett inbyggt system för hantering av utbildningsinnehåll. Användarna hanterar sitt utbildningsinnehåll genom att ladda upp det till Learning Manager så att Learning Manager utför versionshantering, allokering till kurser, definierar synligheten för elever , spårar förbrukning och rapporterar tillbaka till administratörer.

Det finns dock användare som lagrar och hanterar sitt innehåll i resurshanteringssystem. Innehållet återanvänds sedan för olika andra funktioner.

De olika remsorna som finns i elevappen kan bäddas in på AEM-webbplatserna. Alla elever som loggar in på AEM-webbplatsen kommer att se sina specifika utbildningsdata i dessa områden.

## Hämta innehållspaketet {#downloadthecontentpackage}

Installationsprogrammet levereras som ett AEM-innehållspaket. [***Hämta paketet***](https://github.com/adobe/adobe-learning-manager-reference-site).

Innehållspaketet, som finns som en zip-fil, är kompatibelt med AEM 6.4 och AEM 6.5.

## Installera Learning Manager-komponent {#installcaptivateprimecomponent}

Installera Learning Manager-innehållspaketet med hjälp av AEM Package Manager:

>[!NOTE]
>
>Information om hur du installerar paket finns i  [***Arbeta med paket***](https://experienceleague.adobe.com/docs/experience-manager-65/administering/contentmanagement/package-manager.html?lang=en#how-to-work-with-packages).

1. Öppna AEM Package Manager när du är AEM-författare.
1. Klicka på knappen **[!UICONTROL Upload Package]**.
1. Klicka **[!UICONTROL Browse]** och överför innehållspaketet.
1. Klicka på **[!UICONTROL Upload]**.
1. När paketet har överförts installerar du innehållspaketet genom att markera det och klicka på **[!UICONTROL Install]**.

   ![](assets/install-package.jpg)

   *Installera innehållspaketet*

## Generera uppdateringstoken {#generatetherefreshtoken}

AEM-administratören behöver en uppdateringstoken från Learning Manager-kontot. Integreringsadministratören för Learning Manager genererar uppdateringstoken.

1. Godkänn AEM Sites-programmet som visas.

   Klicka på **[!UICONTROL Applications]** > **[!UICONTROL Featured Apps]** > **[!UICONTROL Adobe Experience Manager - Sites]**.

   ![](assets/launch-aem.jpg)

   *Godkänn appen*

1. Klicka **[!UICONTROL Applications]** > **[!UICONTROL Featured Apps]** och öppna programmet AEM-webbplatser.

   Kopiera program-id och beskrivningen.

1. Klicka **[!UICONTROL Developer Resources]** > **[!UICONTROL Access Tokens]**.

   ![](assets/click-tokens.jpg)

   *Generera åtkomsttokens*

1. Ange följande uppgifter:

   * Klient-ID, som är program-ID.
   * Klienthemlighet, som finns i Beskrivning.

1. Hämta OAuth-koden. Du måste använda v2 API i omdirigerings-URI:n.
1. Klicka **[!UICONTROL Submit]** och hämta uppdateringstoken.

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

AEM-författaren kan sedan dra och släppa komponenten Adobe Learning Manager och konfigurera därefter.

Learning Manager-komponenten kräver att den konfiguration som skapades i ovanstående steg mappas till sidan.  Författaren kan mappa konfigurationen genom att redigera sidegenskaper under **[!UICONTROL Advanced]** > **[!UICONTROL Configuration]** > **[!UICONTROL Cloud Configuration]** och ange konfigurationssökväg. På så sätt kan författaren skapa konfigurationer för flera Learning Manager-konton och mappa var och en till olika webbplatser-sidor. Om en konfiguration inte mappas till sidan läser komponenten konfigurationen från mallsidan rekursivt tills den hittar en.

## Elev {#learner}

Eleven kan ta kurserna från sidan.

För att kunna komma åt Learning Manager-widgeten måste eleven vara en inloggad AEM-användare. Egendom **mejl** bör finnas i noden /profile i elevens rep:user -nod. Denna e-postadress ska vara exakt densamma som den som finns i Learning Manager-kontot.

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

Stegen för att konfigurera Skyline nämns i  [GitHub-repo](https://github.com/adobe/captivate-prime-aem-components).

## Katalogwidget

I katalogwidgeten visas utbildning från en specifik katalog eller en uppsättning kataloger till en användare. I avsnittet Egenskaper i sidans egenskaper väljer du Katalog från de listade alternativen.

<!--![](assets/catalog-widget.png)-->

Katalogwidgeten innehåller följande alternativ:

* **[!UICONTROL Catalog ids]:** Kommaseparerade katalog-ID:n som utbildningen måste visas för.
* **[!UICONTROL Sort]:** Sorteringsordning för utbildningen. Alternativen är - namn, datum, skapad, datumRegistrerad och så vidare.
* **[!UICONTROL Learner State]:** Returnerar all utbildning som använder följande som filter - registrerad, påbörjad, slutförd och inte registrerad. Sökresultaten visas inte om sorteringsalternativet är dateEnrolled, dueDate eller dateEnrolled.
* **[!UICONTROL Skill name]:** Den skicklighet som används för att filtrera exakt utbildning.
* **[!UICONTROL Tag name]:** Den tagg som används för att filtrera exakta resultat.

Här är några ytterligare komponenter som du kan anpassa:

**[!UICONTROL Learning Object Types]:** Filtrera enligt typen av utbildningsobjekt. De typer som stöds är: kurs, certifiering, jobAid och learningProgram.

I AEM kommer korttiteln i en remsa att vara tom från början. I Egenskaper skriver du titeln i widgets.html.

**Anpassning**

Du kan anpassa utseendet och känslan på layouten med hjälp av widgets.html. Du kan ändra utseendet på korten som visas och anpassa temat.

I dialogrutan **[!UICONTROL General Settings]** kan du välja primär- och sekundärfärger för korten och ange egenskaper för att anpassa temat.

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

### Ignorera högre ordning för LO-registrering

Om **Ignorera registrering av högre order i LO** kryssrutan är aktiverad och en användare registreras direkt i ett utbildningsprogram eller en certifiering, kommer kurserna för det certifierings- eller utbildningsprogrammet att visas för användaren i widgetarna.

Om kryssrutan är inaktiverad visas inte de kurser som finns i utbildningsprogrammet eller certifieringen där användaren inte har registrerat sig direkt.

![](assets/higher-order-lo.png)

*Markera kryssrutan Ignorera registrering till högre order-LO.

Inställningen används sedan på widgeten.

### Säkerhet

Fälten Klient-ID och Klienthemlighet läggs till. Dessutom maskeras uppdateringstoken. När en användare har skapat hela konfigurationen, om användaren öppnar konfigurationen igen för att redigera den eller om någon annan användare öppnar den här konfigurationen, maskeras uppdateringstoken.
