---
jcr-language: en_us
title: Integrering med Adobe Connect
description: Författare kan skapa virtuella klassrumskurser med Adobe Connect när kurser skapas. För att aktivera Adobe Connect för ditt Learning Manager-konto måste du kontakta organisationens administratör.
contentowner: jayakarr
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 0%

---



# Integrering med Adobe Connect

Administratörer för en organisation kan konfigurera inställningarna för Learning Manager-kontot för att aktivera Adobe Connect-integrering.

## Konfigurera Adobe Connect {#configureadobeconnect}

1. Klicka på i Administratörsinloggning **[!UICONTROL Settings]** i den vänstra rutan för att se grundläggande information om ditt företag. Klicka **[!UICONTROL Adobe Connect]** i den vänstra rutan.

   ![](assets/left-pane.png)

   *Välj Adobe Connect i den vänstra rutan*

1. Klicka **[!UICONTROL Configure Now]** länka in **[!UICONTROL Adobe Connect Configuration]** -sektionen.

   <!--![](assets/configure-now-connect.png)-->

1. Ange ditt företags Adobe Connect-domännamn och logga in autentiseringsuppgifter.

   ![](assets/adobeconnect-config.png)

   *Lägg till domännamn och autentiseringsuppgifter*

   Ett exempel på en Adobe Connect-URL: mycompany.adobeconnect.com\
   Du måste ange e-post-ID för Adobe Connect-kontoadministratören.

   Endast Adobe-värdbaserade anslutningskonton stöds i Learning Manager. Exempel: &#39;.adobeconnect.com&#39;.

1. Klicka **[!UICONTROL Integrate].**

   När du har autentiserat e-post-ID visar Learning Manager meddelandet eftersom Connect har integrerats. Du kan börja visa dina virtuella klassrumskurser automatiskt med Adobe Connect.

   Adobe Connect-kontoadministratören bör acceptera villkoren för att använda Adobe Connect. Om detta inte accepteras kan din inloggningsautentisering misslyckas. Logga in på Adobe Connect-kontot en gång när du har skapat det. Vid den första inloggningen visas sidan med allmänna villkor.

   <!--![](assets/mail-confirmation.png)-->

## Lägg till information om virtuell klassrumssession {#addvirtualclassroomsessioninformation}

Om författaren till en virtuell klassrumskurs inte har angett sessionsinformationen kan administratören inkludera sessionsinformationen.

Klicka på VC-kursnamnet vid administratörsinloggning. Klicka **[!UICONTROL Instances]** i den vänstra rutan och klicka på **[!UICONTROL Session Details]**.  Klicka på ikonen Redigera till höger på sidan Sessionsdetaljer för att lägga till sessionsinformationen.

![](assets/session-creation-admin.png)

*Lägg till information om virtuell klassrumssession*

Med integreringen av Adobe Learning Manager och Adobe Connect för att skapa virtuella klassrumsmoduler eller sessioner bör ditt Connect-konto stödja mötesrum med tillräckligt antal rum och samtidiga användare för ditt användningsfall. Dessa mötesrum används som värd för virtuella klassrumsmoduler i Learning Manager. Ett nytt Connect-mötesrum skapas dynamiskt av Learning Manager för varje virtuell klassrumsmodul eller session i Learning Manager.

Du måste köpa Adobe Connect separat, förutom Adobe Learning Manager.

## Elevers närvaro {#learnersattendance}

Om värden för den virtuella klassrumskursen inte deltar i sessionen registreras inte närvaron automatiskt för elever som deltog i sessionen. I sådana fall kan administratören registrera närvaron manuellt.

Klicka på kursen om virtuella klassrum, klicka på Närvaro i den vänstra rutan på följande sida och notera närvaron.
