---
jcr-language: en_us
title: Hantera anpassade roller via CSV-filer
description: Integreringsadministratören kan lägga till flera anpassade roller till sitt konto i grupp via CSV och tilldela olika användare samma roller. Detta tillvägagångssätt automatiserar processen för att skapa anpassade roller.
contentowner: saghosh
exl-id: fce2f457-2834-491a-8331-64086f5a51b5
source-git-commit: f328076016d8c41455cad71f00d1dc9a1531e007
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 1%

---

# Hantera anpassade roller via CSV-filer

Integreringsadministratören kan lägga till flera anpassade roller till sitt konto i grupp via CSV och tilldela olika användare samma roller. Detta tillvägagångssätt automatiserar processen för att skapa anpassade roller.

Du kan konfigurera roller via FTP- och Box-anslutningarna för Learning Manager.

När du har loggat in på ditt Box-lagringskonto kan integreringsadministratören lägga till följande CSV-filer i kontot:

* user.csv
* role.csv
* user_role.csv

Kom igång genom att hämta CSV-filerna och ändra värdena enligt dina krav.

* Exempelfil: [role.csv](assets/role.csv)
* Exempelfil: [user_role.csv](assets/user_role.csv)

**role.csv**

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Kolumnnamn</b></p></td>
   <td>
    <p><b>Beskrivning</b></p></td>
   <td>
    <p><b>Exempelvärden</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Namn</p></td>
   <td>
    <p>Identifiera en roll i CSV-filen som ska tilldelas användare.</p></td>
   <td>
    <p>Försäljningsförfattare</p></td>
  </tr>
  <tr>
   <td>
    <p>&lt;Entity&gt;</p></td>
   <td>
    <p>Identifiera åtkomsttyp (FULLSTÄNDIG, SKRIV, REGISTRERA, RAPPORT, INGEN) för varje entitetstyp, t.ex. Kurs, KATALOG osv.</p></td>
   <td>
    <p>KOMPLETT</p>
    <p>INGA</p>
    <p>SKRIVA | RAPPORT</p>
    <p>Kolumnnamn motsvarar entitetstypnamn som katalog, kurs, utbildningsplan osv.</p>
    <p>En kolumn för varje enhetstyp kommer att finnas i CSV-filen. Enheter för vilka tillstånd inte ska ges bör inkluderas med värdet INGET</p></td>
  </tr>
  <tr>
   <td>
    <p>Katalogomfattningens specificerare</p></td>
   <td>
    <p>Enskilt katalognamn eller en PIPE (|)-avgränsad lista med katalognamn som bestämmer omfattningen av den här rollen.</p></td>
   <td>
    <p>Försäljningskatalog | Allmän katalog</p></td>
  </tr>
  <tr>
   <td>
    <p>Omfångsspecificerare för användargrupp</p></td>
   <td>
    <p>Användargruppens attributnamn och värde som avgör omfattningen av rollens användare.</p>
    <p>Se avsnittet nedan om omfång.</p></td>
   <td>
    <p>location=London</p></td>
  </tr>
  <tr>
   <td>
    <p>Beskrivning</p></td>
   <td>
    <p>Valfri användarvänlig beskrivning som hjälper dig att förstå syftet med rollen och senare referens.</p></td>
   <td>
    <p>Fullständig författaråtkomst till LO:er i Sales Catalog</p></td>
  </tr>
 </tbody>
</table>

Alla kolumner utom Beskrivning är obligatoriska.

## Definiera användargruppernas omfattning {#definescopeofusergroups}

Du kan ange omfång för användargrupper för olika typer av grupper på följande sätt:

* Användargruppens namn som det är (till exempel Alla författare, Min anpassade grupp)
* Leaf-attribut och -värde (till exempel Department=HR)
* Profilgrupper för självregistrering (self_registration=profilename)
* Profilgrupper för extern registrering (ext_registration=profilename)
* En chefs team med direkt underställda (manager_direct=`<emailid>`)
* En chefs fullständiga organisation (manager_org=`<emailid>`)

**user_role.csv**

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Kolumnnamn</b></p></td>
   <td>
    <p><b>Beskrivning</b></p></td>
   <td>
    <p><b>Kommentar</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Id</p></td>
   <td>
    <p>Mejl-ID för användaren som ska tilldelas en konfigurerbar roll.</p></td>
   <td>
    <p>Om användaren redan har en konfigurerbar roll tilldelad ersätts rollen med en ny roll som anges i CSV-filen. Inga fel rapporteras.</p></td>
  </tr>
  <tr>
   <td>
    <p>AnpassadRoll</p></td>
   <td>
    <p>Namnet på den konfigurerbara roll som ska tilldelas användaren</p></td>
   <td>
    <p>Rollnamnet måste vara en befintlig roll enligt specifikationen i CSV-filen. Roller som skapas av administratören via användargränssnittet kan användas här.</p></td>
  </tr>
 </tbody>
</table>

**Funktioner med fullständig omfattning**

När fullständig behörighet har tilldelats för någon av följande funktioner (funktioner på kontonivå) anses användargruppens omfång och katalogomfånget automatiskt vara FULLSTÄNDIGT, eftersom användaren inte kan ha begränsad åtkomst till dessa funktioner.

Om några katalognamn eller användargruppsnamn anges i CSV-filen åsidosätts de av fullständig behörighet.

* Meddelanden
* Kompetenser
* Spelifiering
* Användare
* Utbildningsplaner
* E-postmallar

## Lägg till roll-CSV:er i kontot {#addtherolecsvsintheaccount}

I ditt Box-konto väljer du **Importera > Användare > internt** och ladda upp filerna role.csv och user_role.csv.

* Role.csv och user_role.csv måste kopieras till mappen **Importera** > **användare** > **intern** > **user_role**.
* user.csv måste kopieras i mappen **Importera** > **användare** > **intern**.

Båda CSV-filerna måste endast överföras via Box och kan inte överföras via användargränssnittet.

>[!NOTE]
>
>CSV-filen för användare är obligatorisk, men CSV-filerna för anpassade roller är valfria. Alla filer som finns bearbetas, och andra hoppas över.

De anpassade roller som skapas med CSV-filen är inte synliga för administratörer i användargränssnittet. Dessa roller kommer inte att relateras till eller påverkas av roller som skapas (eller skapas senare) av användargränssnittet.

Anpassade roller som har skapats av en CSV-fil kan hanteras helt via själva CSV-filen. Detta omfattar att lägga till, ändra och ta bort roller.

Tilldelade roller kan återkallas genom att ta bort tilldelningsposter från user_role csv. Men tilldelningar som görs via administratörsgränssnittet påverkas inte av detta.

Uppdatera CSV-filerna om du vill tilldela och återkalla en anpassad roll.

## Synkronisering av anpassade roller {#synchronizationofcustomroles}

När integreringsadministratören har överfört rollbaserade CSV-filer i Connector-lagringen kan administratören aktivera synkronisering till CSV-filerna. Varje gång en anpassad roll uppdateras, läggs till eller tas bort i CSV-filerna kan administratören synka informationen i filerna och göra listan över roller aktuell.

På sidan Komma igång på administratörspanelen klickar du på **[!UICONTROL Settings]** > **[!UICONTROL Data Sources]**.

Aktivera alternativet i avsnittet Synkronisera inställningar **[!UICONTROL Enable Auto Sync]**.

![](assets/sync-settings.png)

*Välj alternativet Aktivera automatisk synkronisering*

När du väljer det här alternativet kan du schemalägga synkroniseringstiden vid exakt den tidpunkt som du anger i fältet Synkroniseringstid. Om du anger synkroniseringstiden till klockan 00:00 uppdateras de anpassade rollerna vid exakt den angivna tiden varje dag.

Om du vill synkronisera data på begäran klickar du på **[!UICONTROL Sync Now]**.

## Begränsningar när roller konfigureras {#constraintswhileconfiguringroles}

Namnet på en roll måste vara unikt i alla konton. Därför får en roll som skapats via användargränssnittet eller CSV inte ha samma namn som en annan roll som redan skapats av användargränssnittet eller CSV.

På liknande rader kan en användare inte tilldelas en konfigurerbar roll från administratörsgränssnittet som skapats via CSV eftersom dessa roller inte är tillgängliga.

CSV-filer för användartilldelning kan dock användas för att tilldela roller som skapas av användargränssnittet.
