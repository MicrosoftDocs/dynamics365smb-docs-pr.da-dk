---
title: Sådan får du Business Central-tilføjelsesprogram til Excel
description: 'Få mere at vide om, hvordan du får brugerne til tilføjelsesprogrammet Business Central til Excel.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.form: 1480
ms.search.keywords: 'Excel, add-in, centralized deployment, M365 admin center, individual acquisition, appsource'
ms.date: 10/07/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="get-the-business-central-add-in-for-excel"></a>Få Business Central-tilføjelsesprogram til Excel

[!INCLUDE[prod_short](includes/prod_short.md)] indeholder et tilføjelsesprogram til Excel, der giver brugerne mulighed for at vælge handlingen **Rediger i Excel** på bestemte sider for at åbne dataene i et Excel-regneark. Denne handling er en anden end handlingen **Åbn i Excel**, fordi den giver brugerne mulighed for at foretage ændringer i Excel og derefter udgive ændringerne tilbage til [!INCLUDE[prod_short](includes/prod_short.md)]

## <a name="overview"></a>Oversigt

### <a name="about-the-add-in"></a>Om tilføjelsesprogrammet

Tilføjelsesprogrammet kaldes **Microsoft Dynamics Office-tilføjelsesprogram**, og det kan installeres fra [Office Store (AppSource)](https://appsource.microsoft.com/). Når tilføjelsesprogrammet er installeret, er handlingen **Rediger i Excel** tilgængelig på de fleste liste- og listedelsider fra ikonet **Del** ![Del en side i en anden app](media/share-icon.png). Du kan finde flere oplysninger om brug af tilføjelsesprogram i [Vise og redigere i Excel fra Business Central](across-work-with-excel.md).

> [!NOTE]
> Tilføjelsesprogrammet fungerer kun i Windows, ikke i macOS.

### <a name="about-deployment-as-an-admin"></a>Om implementering som administrator

Med [!INCLUDE[prod_short](includes/prod_short.md)] online er der et par installationsmuligheder for at få tilføjelsesprogrammet til brugerne. En mulighed er *individuel anskaffelse*, hvor du lader brugerne installere tilføjelsesprogrammet selv. Med denne indstilling skal brugerne have adgang til at hente filer fra Office Store. En anden mulighed er at konfigurere *centraliseret installation* i Microsoft 365 Administration til automatisk at installere tilføjelsesprogrammet til hele organisationen, grupperne eller bestemte brugere. Centraliseret installation giver brugerne mulighed for at få tilføjelsesprogrammet til brugerne, hvis din organisation ikke giver brugerne adgang til Office Store.

For slutbrugeren er installationsoplevelsen forskellig for de to installationsscenarier:

- Første gang brugerne vælger handlingen **Rediger i Excel**, åbnes ruden **Nyt Office-tilføjelsesprogram** i Excel, første gang brugerne vælger handlingen Rediger i Excel. Hvis du vil installere tilføjelsesprogrammet, skal brugeren vælge **Hav tillid til tilføjelsesprogrammet**, som vil installere tilføjelsesprogrammet direkte fra Office store. Brugerne logger derefter på [!INCLUDE[prod_short](includes/prod_short.md)] med deres brugernavn og adgangskode.

- Med centraliseret installation, første gang brugerne vælger handlingen **Rediger i Excel**, installeres tilføjelsesprogrammet automatisk i Excel fra centraliseret installation og ikke Office Store. Det eneste, brugerne skal gøre, er at logge ind på [!INCLUDE[prod_short](includes/prod_short.md)]

Med begge disse installationsindstillinger konfigureres tilføjelsesprogrammet automatisk til at oprette forbindelse til [!INCLUDE[prod_short](includes/prod_short.md)]. En tredje installationsindstilling er en manuel installation af tilføjelsesprogrammet direkte fra Excel. Med denne indstilling skal brugerne konfigurere tilføjelsesprogrammet for at oprette forbindelse til [!INCLUDE[prod_short](includes/prod_short.md)]

### <a name="switching-from-individual-acquisition-to-centralized-deployment-or-the-other-way-around"></a><a name="switch"></a>Skift fra individuel anskaffelse til centraliseret installation eller omvendt

Når du skifter fra individuel anskaffelse af tilføjelsesprogrammet til Centraliseret installation eller omvendt Excel-filer, som brugerne oprettede, før overgangen påvirkes. Efter overgangen kan brugerne stadig åbne alle Excel-regneark, der tidligere er oprettet ved hjælp af handlingen **Rediger i Excel** eller oprettet manuelt ved at konfigurere Excel-tilføjelsesprogrammet. Men de kan ikke opdatere dataene i filen fra Business Central eller skubbe opdateringer til Business Central

Denne betingelse skyldes, at hver Excel-fil får tildelt et "tilføjelsesprogram"-id. I overgangen til eller fra centraliseret installation tildeles et andet id, så det tidligere id blokeres.

## <a name="preparation-on-premises-only"></a>Forberedelse (kun lokalt)

[!INCLUDE[prod_short](includes/prod_short.md)] det lokale miljø kræver, at dit miljø er konfigureret til tilføjelsesprogrammet. Hvis ikke, er handlingen **Rediger i Excel** ikke tilgængelig for brugerne. Du kan finde flere oplysninger under [Konfigurere Excel-tilføjelsesprogrammet til redigering af Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin) i Developer og IT Pro i Hjælp.

## <a name="deploy-the-add-in-by-using-centralized-deployment"></a>Installere tilføjelsesprogrammet ved hjælp af centraliseret installation

Centraliseret installation er en funktion i Microsoft 365 Administration, som du bruger til automatisk at installere tilføjelsesprogrammer i brugernes Office-apps, f.eks. Excel. Som en hjælp til centraliseret installation inkluderer [!INCLUDE[prod_short](includes/prod_short.md)] den **centraliserede installation af excel-tilføjelsesprogrammet**.

### <a name="before-you-begin"></a>Inden du starter

- Du kan få mere at vide om, hvordan du forhindrer brugere i at hente fra Office under [Administrer tilføjelsesprogrammer i Administration](/microsoft-365/admin/manage/manage-addins-in-the-admin-center).
- Kontroller, at centraliseret installation fungerer for organisationen. Du kan finde flere oplysninger under [Bestemme, om centraliseret installation af tilføjelsesprogrammer fungerer for organisationen](/microsoft-365/admin/manage/centralized-deployment-of-add-ins)
- Hvis du skifter fra individuel anskaffelse, skal du se [Skifte fra individuel anskaffelse til centraliseret installation](#switch)

> [!NOTE]
> Aktivering af centraliseret installation påvirker funktioner, der bruger Excel-tilføjelsesprogrammet, f.eks. handlingen **Rediger i Excel**. Det har ingen indflydelse på andre Excel-relaterede funktioner og eller tilladelser, der er tildelt brugere i [!INCLUDE[prod_short](includes/prod_short.md)]

### <a name="set-up-centralized-deployment-of-the-add-in"></a>Konfigurere centraliseret udrulning af Excel-tilføjelsesprogram

Du skal arbejde i både [!INCLUDE[prod_short](includes/prod_short.md)] og Microsoft 365 Administration.

1. I [!INCLUDE[prod_short](includes/prod_short.md)] kan du vælge ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikonet, skal du skrive **Centraliseret installation af Excel-tilføjelsesprogrammet** og derefter vælge det relaterede link.
2. Læs oplysningerne på **installationssiden til tilføjelsesprogrammet Business Central Excel**, og vælg **Næste**.
3. Log på [Microsoft 365 Administration](https://go.microsoft.com/fwlink/?linkid=2163967), og gå til **Integrerede apps**<!--**Add-ins**-->.

    Udfør følgende trin for at konfigurere tilføjelsesprogrammet, der skal installeres fra Office Store: 
    1. Vælg **Hent apps** for at åbne Office Store (AppSource). <!--**Deploy Add-in** 5. In the **Deploy a new add-in**, select **Choose from the store**.-->
    2. Søg efter **Microsoft Dynamics Office-tilføjelsesprogrammet**, og vælg **hent det nu**. <!--On the **Select add-in** page, search for and select **Microsoft Dynamics Office Add-in** > **Add** > **Continue**.-->
    3. Angiv de brugere, du vil installere tilføjelsesprogrammet til, på siden **Tilføj brugere**, og vælg derefter **Næste**.<!--On the **Configure add-in**, specify the users that you want to deploy the add-in for.-->
    4. Gennemse **anmodninger om accepter tilladelser**, og vælg derefter **Næste** > **afslutning af installation**.
    5. Vent på, at det grønne afkrydsningsfelt ud for **Installeret** vises for tilføjelsesprogrammet, og vælg derefter **Udført**. <!--Select **Deploy** and wait til successful, then **Next** > **Continue**.-->

       Tilføjelsesprogrammet vises på siden **Tilføjelsesprogrammer**. Du kan finde flere oplysninger om installation af tilføjelsesprogrammer i Microsoft 365 Administration under [Installere tilføjelsesprogrammer i Administration](/power-platform/admin/use-service-admin-role-manage-tenant?azure-portal=true).
4. Gå tilbage til den **centraliserede installation af installationsprogrammet til Excel**-assisterede opsætning i [!INCLUDE[prod_short](includes/prod_short.md)], og vælg **Næste**.
5. Vælg **Brug centraliseret installation**, og vælg **Udfør**.

    Hvis du ikke slår denne parameter til, får du [!INCLUDE[prod_short](includes/prod_short.md)]-tilføjelsesprogrammet direkte fra Office Store.

Når du er færdig, kan du altid ændre installationen i Microsoft 365 Administration, f.eks. ved at tildele flere brugere. Du kan finde flere oplysninger om installation af tilføjelsesprogrammer i Administration under [Installere tilføjelsesprogrammer i Administration](/power-platform/admin/use-service-admin-role-manage-tenant?azure-portal=true).

> [!IMPORTANT]
> Hvis du har mere end ét miljø, skal du køre **Excel-tilføjelsesprogrammet Centraliseret installation** assisteret opsætning i hvert miljø, hvor du vil bruge Centraliseret installation. Du behøver dog ikke at konfigurere den centraliserede installation i Microsoft 365 igen. Det eneste, du skal gøre, er at aktivere **Brug centraliseret installation** i den assisterede opsætning. 

> [!NOTE]
> Det kan tage op til 24 timer, før brugerne af tilføjelsesprogrammet installeres automatisk i Excel af brugere.

## <a name="individual-acquisition-install-the-add-in-manually-for-your-own-use"></a><a name="install"></a>Individuel anskaffelse: Du kan finde flere oplysninger i installere tilføjelsesprogrammet manuelt til eget brug

I de fleste tilfælde installeres tilføjelsesprogrammet, når du åbner Excel fra Business Central, enten automatisk for dig, eller du bliver bedt om at installere det. Der kan dog være tilfælde, hvor du skal installere tilføjelsesprogrammet manuelt.

1. Åbn Excel, og åbn derefter en Excel-projektmappe.
2. Vælg **Tilføjelsesprogrammer**  > **Hent tilføjelsesprogrammer** i menuen **Indsæt**
3. Gå til **Administreret administrator**, og søg efter **Microsoft Dynamics Office-tilføjelsesprogram**. Hvis du ser der, skal du markere den og derefter vælge **Tilføj**. Hvis du ikke kan se det, skal du gå til **Store**, derefter søge efter *Microsoft Dynamics Office-tilføjelsesprogram* og følge vejledningen på skærmen for at tilføje det.

Når tilføjelsesprogrammet er installeret, vises det som et panel i Excel. Nu skal forbindelsen konfigureres.

### <a name="configure-the-business-central-connection"></a>Konfigurer Business Central-forbindelsen

Hvis en bruger ikke kan oprette forbindelse automatisk, kan du fjerne blokeringen af dem ved at bede vedkommende om at følge disse trin:

1. Vælg i **Microsoft Dynamics**-tilføjelsesruden i excel **Tilføj serveroplysninger**. Hvis du ikke kan se den, skal du vælge ![knappen Mere i Excel.](media/cogwheel.png) ikonet øverst for at åbne dialogboksen med indstillinger. 
2. Angiv [!INCLUDE[prod_short](includes/prod_short.md)] **URL-adressen til Serveren** til `https://exceladdinprovider.smb.dynamics.com` online. I det [!INCLUDE[prod_short](includes/prod_short.md)]-lokale miljø skal du angive URL-adressen til webklienten, f.eks. `https://myBCserver/190`.
3. Vælg **OK**, og bekræft derefter, at appen genindlæses.
4. Log på Business central med gyldigt brugernavn og adgangskode, når du bliver bedt om det.
5. Vælg alternativt det miljø og regnskab, der indeholder de data, du vil oprette forbindelse til.

Tilføjelsesprogrammet er nu forbundet til [!INCLUDE [prod_short](includes/prod_short.md)], og du kan redigere data og udgive ændringerne i [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="prepare-devices-and-network-for-the-excel-add-in"></a>Forberede enheder og netværk til Excel-tilføjelsesprogrammet

Netværkstjenester som proxyer eller firewalls skal tillade routing mellem hver klientenhed, hvor tilføjelsesprogrammet er installeret, og mange serviceslutpunkter. Du kan finde en liste over slutpunkter under [Forberede netværket til Tilføjelsesprogrammet i Excel](/dynamics365/business-central/dev-itpro/administration/configuring-network-for-addins).

## <a name="troubleshooting"></a>Fejlfinding

Nogle gange løber brugerne ind i problemer med Excel-tilføjelsesprogrammet. Dette afsnit indeholder nogle tip til, hvordan du fjerner blokeringen af brugere under visse omstændigheder.

|Problem  |Løsning eller løsning  |Bemærkninger  |
|---------|---------|---------|
|Tilføjelsesprogrammet starter ikke <br><br>Brugeren får f. eks. meddelelsen "Advarsel til tilføjelsesprogram: Dette tilføjelsesprogram er ikke længere tilgængeligt." når du forsøger at bruge tilføjelsesprogrammet. Dette problem kan opstå, hvis centraliseret installation er konfigureret korrekt, men brugeren ikke fik tildelt adgang.|Kontroller, om tilføjelsesprogrammet er installeret centralt. Du kan også kontrollere, om brugeren er blokeret fra at installere den lokalt. | Administratoren kan konfigurere Office, så brugerne ikke kan hente tilføjelsesprogrammer. I disse tilfælde skal administratoren installere tilføjelsesprogrammet centralt. Yderligere oplysninger finder du under [Installere tilføjelsesprogrammer i Administration](/microsoft-365/admin/manage/manage-deployment-of-add-ins?view=o365-worldwide&preserve-view=true).|
|Data indlæses ikke i Excel|Test forbindelsen ved at åbne en anden liste i Excel fra [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan også åbne projektmappen i Excel i en browser.|Hvis brugeren har angivet et firmanavn, der indeholder specialtegn, kan tilføjelsesprogrammet ikke oprette forbindelse. |
|Data kan ikke udgives tilbage til [!INCLUDE [prod_short](includes/prod_short.md)].|Test forbindelsen ved at åbne projektmappen i Excel i en browser. |Nogle gange kan en udvidelse blokere udgivelsesjobbet. Hvis siden er udvidet eller tilpasset, skal du fjerne udvidelserne og derefter prøve igen.|
|Datoerne er forkerte  |Excel kan vise klokkeslæt og datoer i et andet format end [!INCLUDE [prod_short](includes/prod_short.md)]. Denne betingelse gør dem ikke forkerte, og dataene i [!INCLUDE [prod_short](includes/prod_short.md)] bliver ikke blandet.|         |
|For nogle listesider forårsager redigering af flere linjer i Excel konsekvent fejl. Denne betingelse kan opstå, hvis OData-kald omfatter FlowFields og felter uden for repeaterkontrolelementet.|Marker afkrydsningsfelterne **Udelad ikke-redigerbare FlowFields** og **Udelad felter uden for repeater** for den udgivne side på siden **Webtjenester**. Hvis du markerer disse afkrydsningsfelter, udelades ikke-redigerbare FlowFields og -felter fra eTag-beregningen. |Disse afkrydsningsfelter er som standard skjult. Hvis du vil have dem vist på siden **Webtjenester**, skal du bruge [tilpasning](/dynamics365/business-central/ui-personalization-user). |
|Brugere kan ikke længere logge på tilføjelsesprogrammet. Når de forsøger at logge på, stopper processen uden at være færdig.| Dette problem kan skyldes en opdatering, som vi har lavet i tilføjelsesprogrammet. det kan i juli 2022. Du kan finde flere oplysninger om og en rettelse i afsnittet [ændre konfigurationen af Excel-Tilføjelsesprogrammet for at understøtte juli 2022 Update](/dynamics365/business-central/dev-itpro/administration/update-excel-addin-configuration).|Gælder for [!INCLUDE [prod_short](includes/prod_short.md)] kun lokalt|
| Tilføjelsesprogrammet kommunikerer ved hjælp af API v2.0 til Dynamics 365 Business Central, og eventuelle begrænsninger for denne API nedarves automatisk. En eksempelbegrænsning er, hvis du forsøger at redigere en liste, og det underliggende kort bruger en bekræftelsesdialogboks i AL-logikken, f.eks. som valideringslogik. | Nogle gange er der ikke noget at gøre, fordi det er et designvalg, at brugeren eksplicit skal bekræfte ændringen. Hvis bekræftelsen er ubetydelig, når du bruger **Rediger i Excel**, kan du pakke bekræftelsesdialogopkaldet ind i en if-betinget sætning, der kontrollerer, om klienttypen er forskellig fra ODataV4, f.eks. `if SESSION.CurrentClientType() <> ClientType::ODataV4 then`. | Der kan være andre klienter, som du vil fjerne bekræftelsesdialogen fra, f.eks. OData og SOAP. |

<!--
## <a name="deploy-the-excel-add-in-for-business-central-online"></a>Deploy the Excel add-in for Business Central online

For [!INCLUDE [prod_short](includes/prod_short.md)] online, the administrator can deploy the add-in for all users. But users can also install the add-in themselves, provided they have permission to configure their Office experience.  

> [!TIP]
> In some organizations, administrators cannot deploy add-ins centrally. For more information, see [Determine if Centralized Deployment of add-ins works for your organization](/microsoft-365/admin/manage/centralized-deployment-of-add-ins?view=o365-worldwide&preserve-view=true).

### <a name="to-deploy-the-excel-add-in-for-all-users"></a>To deploy the Excel add-in for all users

1. As the administrator, sign in to the Microsoft commercial website and find the add-in at [https://appsource.microsoft.com/product/office/WA104379629](https://appsource.microsoft.com/product/office/WA104379629).
2. Choose the **Get it now** button.

    You'll be redirected to the Microsoft 365 admin center.
3. In the left panel, go to **Settings**, and then choose **Add-ins**.
4. In the **Configure add-in** pane, specify which users to grant access to the add-in.
5. Save your changes.


### <a name="to-add-the-excel-add-in-locally"></a>To add the Excel add-in locally

1. Open Excel, and then open any Excel workbook.
2. On the **Insert** menu, choose **Office Add-ins**, and then choose **Admin managed** or **Store** as appropriate.
3. Search for *Dynamics Office Add-In*, and then install the add-in.

When the add-in is installed, it shows up as a panel in Excel. Next, you must configure the connection.

> [!TIP]
> If the workbook is not automatically saved to the user's OneDrive, then recommend them to save all workbooks that they export from [!INCLUDE [prod_short](includes/prod_short.md)].When they open the workbook again, the connection is still available, so they do not have to configure the connection again.

> [!NOTE]
> In certain deployments, the administrator must configure network access to unblock the Excel add-in. For more information, see [Preparing Your Network for the Excel Add-In](configuring-network-for-addins.md).-->

## <a name="see-also"></a>Se også

[Analysere regnskaber i Microsoft Excel](finance-analyze-excel.md)  
[Arbejde med Business Central](ui-work-product.md)  
[Forbedringer af Excel-integration i frigivelsesbølge 2 i 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
