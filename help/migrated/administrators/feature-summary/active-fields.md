---
description: Lär dig använda Aktiva fält i Adobe Learning Manager för att hämta, ordna och hantera anpassad användarinformation. Förbättra rapportering, filtrering och användarsegmentering med flexibla fältkonfigurationer.
jcr-language: en_us
title: Konfigurera aktiva fält i Adobe Learning Manager
exl-id: e68300d6-9f19-4e42-b485-c4bbbbcf5518
source-git-commit: a01ec6117ad49a1f9af0b31d48ad19ddc8443dde
workflow-type: tm+mt
source-wordcount: '1062'
ht-degree: 0%

---

# Aktiva fält

Aktiva fält i Adobe Learning Manager är anpassade användarattribut som hjälper administratörer att ordna och hantera användare effektivt. Med dem kan du hämta extra information om användaren, till exempel avdelning, plats eller befattning. Administratörer kan använda dessa data för att skapa användargrupper, anpassa utbildningen och filtrera rapporter mer effektivt.

Användarattribut är information som en användares förnamn, efternamn och e-postadress. Dessa attribut hjälper administratörer att:

* Identifiera användare
* Gruppanvändare
* Hantera användarbehörigheter och åtkomstbegränsningar

Genom att lägga till anpassade attribut i användarprofiler samlar aktiva fält in ytterligare information som är relevant för din organisation.

>[!INFO]
>
>Titta på ALM Academy-utbildningen och lär dig lägga till, anpassa och konfigurera aktiva fält.<br>[![knapp](assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/7555741)</br>

## Lägg till aktiva fält

Aktiva fält gäller för både interna och externa elever, vilket gör att organisationer kan definiera och hantera anpassade användarattribut för alla användare.

Så här lägger du till eller hanterar aktiva fält för interna användare:

1. Välj **Användare** på administratörens startsida.

2. Välj **Aktiva fält**.

3. Skriv det aktiva fältnamnet och välj sedan **Lägg till**. Processen för att lägga till aktiva fält för externa elever är densamma som för interna elever.

   ![](assets/add-active-field-alm.png)
   _Fält för att ange namnet på ett nytt anpassat attribut för användare_

4. Välj **Spara**.

## Lägg till anpassade värden i aktiva fält

Aktiva fält kan innehålla fördefinierade eller anpassade värden som matchar organisationens struktur. Om du lägger till anpassade värden kan du hämta information som är specifik för dina interna användare, som avdelningsnamn, jobbnivåer och regionkontor.

Så här lägger du till anpassade värden för interna användare:

1. Välj **Visa värden** under avsnittet **Aktivt fält**.
2. I dialogrutan **Värden i anpassade fält**:

   * Välj ett aktivt fält i listrutan **Välj fält**.
   * Skriv in värdena för det aktiva fältet i fältet **Nytt värde**.

   ![](assets/add-value-active-fields.png)
   _Dialogruta för att ange anpassade värden för ett specifikt aktivt fält_

3. Välj **Klar** och välj sedan **Spara** för att tillämpa ändringarna.

## Konfigurera inställningar för aktivt fält

Anpassa aktiva fält för att underlätta användarhantering och rapportaktiviteter och konfigurera de aktiva fältegenskaperna:

* **Grupperbar**: Med det här alternativet kan du gruppera elever baserat på aktiva fältvärden.
* **Rapporteringsbar**: Med det här alternativet kan du skapa en rapporteringsanvändargrupp baserat på det aktiva fältvärdet och aktivera rapporteringsfiltret för fältet i kontrollpanelsrapporter.
* **Elever-konfigurerbar**: Med det här alternativet kan elever konfigurera fältet själva.
* **Kan exporteras**: Det här alternativet inkluderar det aktiva fältet i exporterade användargruppsrapporter.
* **Flera värden**: Det här alternativet stöder flera värden för det aktiva fältet.

Så här konfigurerar du inställningar för aktiva fält:

1. Välj fliken **Inställningar** och gå sedan till avsnittet **Användarvisning**.

   ![](assets/settings-active-field.png)
   _Välj fliken Inställningar för att anpassa de aktiva fälten_

2. Välj ett eller båda alternativen efter behov.:

   * **Visa endast ofyllda fält vid elevinloggning:** När det här alternativet är markerat ser eleverna bara de aktiva fält som de inte har fyllt i än. Detta uppmanar dem att fylla i sina profiler, vilket hjälper dem att se till att användardata är korrekta och aktuella. Att visa dessa fält har stöd för fullständiga elevprofiler och möjliggör anpassade utbildningsupplevelser.
   * **Om alternativet är avmarkerat visas inte sidan Slutför din profil för användarna:** När alternativet är inaktiverat ser eleverna inte sidan **Slutför din profil** vid inloggningen. De uppmanas inte att uppdatera eller fylla i någon profilinformation och har direkt åtkomst till plattformen.

   ![](assets/user-display-alm.png)
   _Inställningsgränssnitt för att styra hur och när aktiva fält visas_

3. Välj **Spara** för att tillämpa ändringarna.

>[!NOTE]
>
>Anpassade användargrupper påverkas inte om du tilldelar en ny roll. Det kommer dock att påverka automatiskt genererade användargrupper som Alla administratörer, Alla författare och liknande rollbaserade grupper.

## Aktiva fält med flera värden

Med aktiva fält med flera värden kan du tilldela flera värden till ett enda användarattribut, t.ex. platser, jobbtitlar eller projektteam. Detta hjälper till att samla in mer detaljerad och flexibel användarinformation.

Du kan konfigurera upp till tre aktiva fält med flera värden per konto. De är tillgängliga för både interna och externa användare. När ett fält har angetts som flera värden kan den här inställningen inte ändras tillbaka.

Så här tilldelar du flera värden till ett aktivt fält:

1. Välj **Användare** och välj sedan **Aktiva fält**.
2. På fliken **Inställningar** väljer du **Flera värden**.

![](assets/multi-values.png)
_Inställningsgränssnitt för att styra hur och när aktiva fält visas_

Du kan lägga till flera värden via CSV-filen eller användargränssnittet. När multivärdesfältet har använts i en användargrupp kan det inte ändras till enkelvärdesfält.

## Lägg till aktiva fält genom att överföra en CSV-fil

Lägg till aktiva fält när du överför användare via CSV genom att inkludera matchande rubriker för varje definierat fält. Administratörer kan överföra användare i grupp med hjälp av en CSV-fil. CSV-filen ska innehålla de nya aktiva fälten som definierar de användare som ska importeras. Se till att filens rubriknamn exakt matchar de aktiva fält som är konfigurerade i systemet så att data mappas korrekt. Överför CSV-filen från avsnittet **Användare**.

I den här [artikeln](/help/migrated/administrators/feature-summary/add-users-user-groups.md) finns mer information om hur du lägger till flera användare samtidigt.

## Begränsa värden för CSV-fält

Alternativet **Begränsa markering** i **Värden i anpassade fält** styr om användare som importerar data via CSV-filer endast kan välja bland fördefinierade värden för anpassade fält. När det här alternativet är aktiverat måste användarna välja i en värdelista och se till att data är konsekventa och förhindra nya eller oväntade poster. Om detta är inaktiverat kan användare ange valfritt värde, vilket ger större flexibilitet men mindre kontroll över datanoggrannheten.

![](assets/restrict-active.png)
_Kryssruta för att aktivera värdebegränsning under CSV-överföring_

## Hantera saknade aktiva fält i användar-CSV-import

I vissa fall föredrar administratörer att elever fyller i vissa aktiva fält manuellt när de loggar in på Adobe Learning Manager. Detta stöds för användare som importeras via en CSV-fil. I den här [artikeln](/help/migrated/administrators/feature-summary/add-users-user-groups.md) finns information om hur du lägger till flera användare samtidigt. Användare läggs automatiskt till i aktiva fält eller rollbaserade grupper baserat på Boxs FTP-fältvärden. De kan inte läggas till i anpassade grupper.

Om en CSV-fil inte innehåller alla aktiva fält måste administratören manuellt ange de värden som saknas efter importen.

Som standard måste varje aktivt fält mappas till ett motsvarande fält i CSV-källfilen. Om du inte vill mappa ett specifikt aktivt fält till en kolumn i CSV-filen kan du välja värdet **DontImportFromSource** i listrutan under både Box- och FTP-importprocessen. Det här alternativet är tillgängligt när du importerar användare via FTP- eller Box-anslutningar. Läs den här [artikeln](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/connectors) om du vill ha mer information om anslutningarna.


