---
jcr-language: en_us
title: Integrering med Adobe Connect
description: Författare kan skapa virtuella klassrumskurser med Adobe Connect när kurser skapas. För att aktivera Adobe Connect för ditt Learning Manager-konto måste du kontakta organisationens administratör.
contentowner: jayakarr
exl-id: 13458f93-9ea7-4aab-8b33-3c4f4dd5886d
source-git-commit: 857dddf46e3900fbe2db4e345da2d29050ef3c82
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 0%

---

# Integrering med Adobe Connect

Administratörer för en organisation kan konfigurera inställningarna för Learning Manager-kontot för att aktivera Adobe Connect-integrering.

## Konfigurera Adobe Connect {#configureadobeconnect}

1. I administratörsinloggningen klickar du på **[!UICONTROL Settings]** i den vänstra rutan för att visa grundläggande information om ditt företag. Klicka på **[!UICONTROL Adobe Connect]** i den vänstra rutan.

   ![](assets/left-pane.png)

   *Markera Adobe Connect i den vänstra rutan*

1. Klicka på länken **[!UICONTROL Configure Now]** i avsnittet **[!UICONTROL Adobe Connect Configuration]**.

   <!--![](assets/configure-now-connect.png)-->

1. Ange ditt företags Adobe Connect-domännamn och logga in autentiseringsuppgifter.

   ![](assets/adobeconnect-config.png)

   *Lägg till domännamn och autentiseringsuppgifter*

   Ett exempel på en Adobe Connect-URL: mycompany.adobeconnect.com\
   Du måste ange e-post-ID för Adobe Connect-kontoadministratören.

   Endast Adobe-värdbaserade anslutningskonton stöds i Learning Manager. Exempel: &#39;.adobeconnect.com&#39;.

1. Klicka på **[!UICONTROL Integrate].**

   När du har autentiserat e-post-ID visar Learning Manager meddelandet eftersom Connect har integrerats. Du kan börja visa dina virtuella klassrumskurser automatiskt med Adobe Connect.

   Adobe Connect-kontoadministratören bör acceptera villkoren för att använda Adobe Connect. Om detta inte accepteras kan din inloggningsautentisering misslyckas. Logga in på Adobe Connect-kontot en gång när du har skapat det. Vid den första inloggningen visas sidan med allmänna villkor.

   <!--![](assets/mail-confirmation.png)-->

## Lägg till information om virtuell klassrumssession {#addvirtualclassroomsessioninformation}

Om författaren till en virtuell klassrumskurs inte har angett sessionsinformationen kan administratören inkludera sessionsinformationen.

Klicka på VC-kursnamnet vid administratörsinloggning. Klicka på **[!UICONTROL Instances]** i den vänstra rutan och klicka på **[!UICONTROL Session Details]**.  Klicka på ikonen Redigera till höger på sidan Sessionsdetaljer för att lägga till sessionsinformationen.

![](assets/session-creation-admin.png)

*Lägg till information om virtuell klassrumssession*

Med integreringen av Adobe Learning Manager och Adobe Connect för att skapa virtuella klassrumsmoduler eller sessioner bör ditt Connect-konto stödja mötesrum med tillräckligt antal rum och samtidiga användare för ditt användningsfall. Dessa mötesrum används som värd för virtuella klassrumsmoduler i Learning Manager. Ett nytt Connect-mötesrum skapas dynamiskt av Learning Manager för varje virtuell klassrumsmodul eller session i Learning Manager.

Du måste köpa Adobe Connect separat, förutom Adobe Learning Manager.

## Elevers närvaro {#learnersattendance}

Om värden för den virtuella klassrumskursen inte deltar i sessionen registreras inte närvaron automatiskt för elever som deltog i sessionen. I sådana fall kan administratören registrera närvaron manuellt.

Klicka på kursen om virtuella klassrum, klicka på Närvaro i den vänstra rutan på följande sida och notera närvaron.

## Stöd till Adobe Connect-seminarier med stor publik

Adobe Learning Manager har stöd för att välja seminarierum från Adobe Connect när du konfigurerar en virtuell klassrumssession i Connect. Tidigare kunde administratören bara välja mötesrumstyp. Med den här funktionen kan administratören med en giltig seminarielicens schemalägga och hantera engångs- eller storskaliga evenemang (upp till 1 500 deltagare) i ALM.

Mer information om seminarierummet finns i den här [artikeln](https://helpx.adobe.com/adobe-connect/using/creating-seminars.html).

### Stöd för åtkomst till sessionsanalys

Instruktörer kan komma åt Sessionsanalys för sina slutförda Adobe Connect-sessioner via en ny länk som finns på deras sessionsinstrumentpanel.

![](assets/adobe-connect-session-url.png)
_Välj sessions-URL_

Den här länken öppnar instrumentpanelen för sessionsanalys i Connect, som ger detaljerade insikter om sessionsengagemanget.
Den här funktionen är endast tillgänglig för sessioner som genomförs via Adobe Connect. Sessionsanalyserna inkluderar:

* **[!UICONTROL Engagement]**: Översikt över livesessionens övergripande prestanda
* **[!UICONTROL Interactions]**: Detaljerad uppdelning av deltagaraktivitet i olika poder
* **[!UICONTROL Attendee Activity]**: Sammanfattning av deltagarengagemang
* **[!UICONTROL Download Reports]**: Möjlighet att hämta rapporter för podspecifika engagemangsdata

![](assets/session-dashboard.png)
_Sessionens instrumentpanel_

Läs den här [artikeln](https://helpx.adobe.com/in/adobe-connect/using/session-dashboard.html) om du vill ha mer information om sessionsanalys.
