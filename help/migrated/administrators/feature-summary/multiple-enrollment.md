---
title: Flera registreringar i Adobe Learning Manager
description: En av dina primära uppgifter som kontoadministratör är att skapa olika instanser av VILT-sessioner i olika tidszoner och eventuellt skapa sessioner för specifika användargrupper.
exl-id: c430545d-b48e-432d-a278-658c9281818f
source-git-commit: 5676ddb238309bc643394af1dde3cba7f8ac6699
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 0%

---

# Flera registreringar i Adobe Learning Manager

I Adobe Learning Manager kan varje kurs ha olika instanser. En av dina primära uppgifter som kontoadministratör är att skapa olika instanser av VILT-sessioner i olika tidszoner och eventuellt skapa sessioner för specifika användargrupper.

Före juli 2023-versionen när en administratör registrerade en elev kunde denne endast registrera sig i en instans. Om en elev vill gå en kurs i olika instanser skapar administratören många kurser, en för varje instans.

Adobe Learning Manager funktion för flera registreringar hjälper administratörer att undvika sådana scenarier.

## Hantera instanser

>[!INFO]
>
>I den här utbildningen får du lära dig redigera instansinformation och instansegenskaper.<br><br>[![knapp](assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/8318912)</br></br>

Skriv till <almacademy@adobe.com> om du inte kan starta utbildningen.

## Vad är multiregistrering

Vid flera registreringar registreras en elev flera gånger i en kurs via olika tillgängliga instanser.  En elev kan registrera sig för flera kursinstanser oavsett i vilket tillstånd de är registrerade, slutförda eller ännu inte påbörjat. När författaren aktiverar växlingsknappen [!UICONTROL Multiple Enrollment] kan en elev sedan registrera sig för flera instanser av kursen.

![bild för flera registreringar](assets/multi-enrollment-author.png)
*Starta flera registreringar från Inställningar*

Förloppet för varje instans kan spåras individuellt och en rapport kan exporteras för att spåra förloppet för varje instans.

## Viktiga punkter

* Flerregistrering är endast tillämpligt när en kurs har flera instanser.
* När alternativet för flera registreringar är aktiverat och användare registreras i flera instanser skapas nya rader för varje kurs i rapporten Elevens betygsutdrag (en rad för varje instans och varje elev)
* Om rapporteringsautomatisering har konfigurerats som endast förutser en rad per kurs, måste du göra de nödvändiga justeringarna av rapporteringsautomatiseringen innan du aktiverar funktionen Flerregistrering.

## Så här aktiverar du Multi-Enrollment

1. Logga in på ditt Adobe Learning Manager-konto som författare.
1. Välj den kurs som du vill att elever ska registrera sig för flera gånger.
1. Välj **[!UICONTROL Settings]** > **[!UICONTROL Edit]** > **[!UICONTROL Instance configuration]** > **[!UICONTROL Enable Multiple Enrollment]** i den vänstra panelen.

![bild för flera registreringar](assets/multi-enrollment-author.png)
*Aktivera flera registreringar*

>[!NOTE]
>
>Som författare kan du inte ha instansväxling och multipla registreringar aktiverat samtidigt.

## Elevvy

Flera registreringar är till hjälp när en elev vill registrera sig till en Classroom- eller VC-kurs eller vill slutföra en kurs igen innan han eller hon går vidare till en annan kurs.

För elever som inte har registrerat sig kommer de, när de väljer en kurs, att se skärmen under kursen med flera instanser. Sedan kan de markera varje instans och registrera sig.

![Bild på elevvy](assets/learner-view.png)
*Visa instanserna*

Efter att ha registrerat sig i en instans kan de registrera sig i andra instanser genom att välja alternativet Visa alla instanser i den högra rutan.

![Kursbild för flera registreringar](assets/enroll-instance.png)
*Registrera dig för en instans*

Förloppet för varje instans kan spåras enligt nedan:

![spåra förlopp](assets/check-progress.png)
*Spåra förloppet för varje instans*

## Ändringar av multiregistrering i administratören

**Registrering:**

När du registrerar elever kan du markera följande kryssruta:

*&quot;Vald(a) elev(er) kan redan vara registrerad(a) i andra instanser av denna kurs. Tillåt att dessa elever även registreras i instansen ...&quot;*

![Administratörsändringar](assets/admin-changes.png)
*Registreringsalternativ för administratörer*

Om eleven redan är registrerad i en instans och du, som administratör, försöker registrera eleven i en annan kursinstans väljer du Ja.

## Rapportering

För en elev som är registrerad i två instanser av samma kurs skapas två rader för varje kursinstans. I rapporten visas också instansernas förlopp.
