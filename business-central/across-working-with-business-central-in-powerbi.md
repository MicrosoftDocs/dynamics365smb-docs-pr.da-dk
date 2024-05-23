---
title: Opret forbindelse til Power BI fra Business Central i det lokale miljø | Microsoft Docs
description: 'Få indsigt, business intelligence og KPI''er fra Business Central-data ved hjælp af Power BI.'
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 01/22/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Opret forbindelse til Power BI fra Business Central i det lokale miljø

<!--In this article, you learn some of the basics about working with reports and dashboards in Power BI that use [!INCLUDE [prod_short](includes/prod_short.md)] as a data source. The article discusses some aspects that will help you get started as a [!INCLUDE[prod_short](includes/prod_short.md)] user. For general guidelines and instructions about using Power BI, see [Power BI documentation for consumers](/power-bi/consumer).

## Get ready

Sign up for the Power BI service. If you haven't already signed up, go to [https://powerbi.microsoft.com](https://powerbi.microsoft.com). When you sign up, use a work email address and password.-->

## Kom i gang

Hvis du bruger [!INCLUDE [prod_short](includes/prod_short.md)] i det lokale miljø, skal det aktiveres til Power BI-integration. Denne opgave udføres typisk af en administrator. Du kan finde flere oplysninger om aktivering af Power BI-integration med Business Central online i [Konfigurere Business Central i det lokale miljø til Power BI-integration](admin-powerbi-setup.md).

Nogle funktioner er tilgængelige med Business Central online, men ikke i det lokale miljø. Du kan finde flere oplysninger i [Introduktion til Business Central og Power BI](admin-powerbi.md#what-you-can-do-with-power-bi-and-business-central)

## <a name="setup"></a>Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø for Power BI-integration

I dette afsnit forklares kravene til en installation af [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø, der kan integreres med Power BI.

1. Konfigurer enten [NavUserPassword](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-navuserpassword) eller [Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-ad-overview) som godkendelsesmetode for installationen.  
    
    > [!NOTE]
    > Power BI-integration understøtter ikke Windows-godkendelse og understøttes ikke på Windows-klient.

2. Aktivere OData-webtjenester og ODataV4-slutpunkt.

    OData-webtjenesten skal være aktiveret på [!INCLUDE[server](includes/server.md)], og OData-porten skal være åbnet i firewall. Du kan finde flere oplysninger i [Konfiguration af Business Central Server - OData-webtjenester](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    Den lokale server skal være tilgængelig fra internettet.

3. Tildele [!INCLUDE[prod_short](includes/prod_short.md)]-brugerkonti adgangsnøgle til webtjenesten.

    Der kræves kun en adgangsnøgle til webtjenester for at få vist [!INCLUDE[prod_short](includes/prod_short.md)]-data i Power BI. Du kan tildele hver brugerkonto en adgangsnøgle til webtjenesten. Du kan i stedet oprette en specifik konto med en adgangsnøgle til webtjeneste, så alle brugere kan anvende den. Du kan finde flere oplysninger i [Godkendelse af webtjenester](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

4. Oprette en programregistrering for [!INCLUDE[prod_short](includes/prod_short.md)] i Microsoft Azure.

    Hvis du vil have vist Power BI-rapporter integreret på [!INCLUDE[prod_short](includes/prod_short.md)]-sider, skal et program registreres for [!INCLUDE[prod_short](includes/prod_short.md)] i Microsoft Azure. Det registrerede program skal have tilladelse til Power BI-tjenester. Som minimum kræver app'en **User.ReadWrite.All**-tilladelser. For at brugerne kan få vist rapporter fra delte Power BI-arbejdsområder, kræver appen **Workspace.Read.All**-tilladelse. Du kan finde flere oplysninger i [Registrering af [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø i Microsoft Entra ID til integration med andre tjenester](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Hvis din installation benytter NavUserPassword-godkendelse, opretter [!INCLUDE[prod_short](includes/prod_short.md)] forbindelse til den samme Power BI-tjeneste for alle brugere. Du skal angive denne tjenestekonto som en del af registreringen af programmet. Med Microsoft Entra-godkendelse opretter [!INCLUDE[prod_short](includes/prod_short.md)] forbindelse til den Power BI-tjeneste, der er knyttet til de enkelte brugerkonti.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
5. Foretage den første forbindelse mellem Business central og Power BI.

    Før slutbrugere kan bruge Power BI i [!INCLUDE[prod_short](includes/prod_short.md)], skal en Azure-programadministrator give samtykke til Power BI-tjenesten.

    Hvis du vil oprette den første forbindelse, skal du åbne [!INCLUDE[prod_short](includes/prod_short.md)] og køre **Introduktion til Power BI** fra startsiden. Handlingen vil føre dig gennem samtykkeprocessen og kontrollere Power BI-licensen. Når du bliver bedt om at logge på med en Microsoft Entra admin-konto. Du kan få flere oplysninger i [Tilknyt til Power BI - én gang](across-working-with-powerbi.md#connect)..

## Oprette Power BI-rapporter, der viser [!INCLUDE [prod_long](includes/prod_long.md)]-data

Du kan gøre dine Dynamics 365 Business Central-data tilgængelige som datakilde i Power BI Desktop og opbygge nyttige rapporter over status for din virksomhed.

Brug Power BI Desktop til at oprette rapporter til visning af Dynamics 365 Business Central-data. Når du har oprettet rapporter, kan du udgive dem til din egen Power BI-tjeneste eller dele dem med andre brugere i din organisation. Når disse rapporter er i Power BI-tjenesten, kan de brugere, der er oprettet til den, se rapporterne i Dynamics 365 Business Central.

- For [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø skal du have følgende oplysninger:

  - URL-adressen til OData for [!INCLUDE[prod_short](includes/prod_short.md)].
  
    Denne URL-adresse har typisk formatet `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, f.eks. `https://localhost:7048/BC190/ODataV4`. Hvis du har en installation med flere lejere, skal du medtage lejeren i URL-adressen, f.eks. `https://localhost:7048/BC190/ODataV4?tenant=tenant1`.
  - Et brugernavn og en adgangskode til webtjenesten for en [!INCLUDE[prod_short](includes/prod_short.md)]-konto.

    For at få data fra [!INCLUDE[prod_short](includes/prod_short.md)] bruger Power BI basisgodkendelse. Derfor skal du bruge et brugernavn og en adgangsnøgle til webtjenesten for at oprette forbindelse. Kontoen kan være din egen brugerkonto, eller din organisation kan have en specifik konto til dette formål.

## <a name="getdata"></a>Tilføje [!INCLUDE[prod_short](includes/prod_short.md)] som en datakilde i Power BI Desktop

Den første opgave i oprettelsen af rapporter er at tilføje [!INCLUDE[prod_short](includes/prod_short.md)] som en datakilde i Power BI Desktop. Når forbindelsen er oprettet, kan du starte med at generere rapporten.

1. Start Power BI Desktop.
2. Vælg **Hent data**.

    Hvis du ikke kan se **Hent data**, skal du vælge menuen **Filer** og derefter **Hent data**.
3. Vælg **Onlinetjenester** på siden **Hent data**.
4. I ruden **Online tjenester** skal du oprette forbindelse til [!INCLUDE [prod_short](includes/prod_short.md)] i det lokale miljø, skal du vælge **Dynamics 365 Business Central (i det lokale miljø)** og derefter **Opret forbindelse**.
5. Log på [!INCLUDE [prod_short](includes/prod_short.md)] (kun én gang).

    Hvis du ikke har logget ind [!INCLUDE [prod_short](includes/prod_short.md)] fra Power BI desktop før, bliver du bedt om at logge på.

   - For [!INCLUDE [prod_short](includes/prod_short.md)] lokalt skal du først angive URL-adressen til OData [!INCLUDE[prod_short](includes/prod_short.md)], og derefter skal du vælge **OK**. Angiv derefter brugernavnet og adgangskoden på den konto, der skal bruges til at oprette forbindelse til [!INCLUDE[prod_short](includes/prod_short.md)], når du bliver bedt om det. Angiv webtjenestens adgangsnøgle i feltet **Adgangskode**. Vælg **Tilslut**, når du er færdig.
   
    > [!NOTE]  
    > Når du har oprettet forbindelse til [!INCLUDE[prod_short](includes/prod_short.md)], bliver du ikke bedt om at logge på igen. [Hvordan kan jeg ændre eller rydde den konto, jeg bruger for at oprette forbindelse til Business central fra Power BI Desktop?](/dynamics365/business-central/power-bi-faq?tabs=designer#perms)

6. Når forbindelsen er oprettet, kontakter Power BI til Business Central-service. **Navigations**-vinduerne vises, og der vises tilgængelige datakilder til oprettelse af rapporter. Vælg en mappe for at udvide den og få vist de tilgængelige datakilder. 

   Disse datakilder repræsenterer de webtjenester og API'er, som du har publiceret fra for [!INCLUDE [prod_short](includes/prod_short.md)]. Datakilderne er inddelt i Business Central-miljøer og firmaer.

   > [!NOTE]
    > Strukturen for den lokale Business Central er forskellig fra, da den ikke understøtter API-sider.

7. Angiv de datakilder, du vil føje til dine datamodel, og vælg derefter knappen **Indlæsning**.
8. Hvis du senere vil tilføje flere Business Central-data, kan du gentage de forrige trin.

Når dataene er indlæst, kan du se dem i den højre navigation på siden. Nu har du oprettet forbindelse til dine [!INCLUDE[prod_short](includes/prod_short.md)]-data og er klar til at begynde at oprette din Power BI-rapport.  

> [!TIP]
> Du kan finde flere oplysninger om brugen af Power BI Desktop under [Introduktion til Power BI Desktop](/power-bi/fundamentals/desktop-getting-started).

## Administrere og redigere rapporter

> [!NOTE]
> Du kan ikke administrere og redigere rapporter. 

## Overføre rapporter

For [!INCLUDE [prod_short](includes/prod_short.md)] i det lokale miljø er der ingen tilgængelige demorapporter, så du bliver nødt til at starte fra bunden ved at bruge Power BI Desktop. Alternativt kan Power BI-rapporter kan distribueres som filer, som du kan overføre direkte fra Power BI-onlinetjeneste. Du kan finde flere oplysninger i [Overføre rapporten til tjenesten](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

<!--
> [!NOTE]
> Uploading a report requires that you have SUPER user permissions in [!INCLUDE[prod_short](includes/prod_short.md)]. Also, you can't upload reports with [!INCLUDE [prod_short](includes/prod_short.md)] on-premises. With on-premises, you upload reports directly to your Power BI workspace. For more information, see [Connect to Power BI from [!INCLUDE [prod_short](includes/prod_short.md)] on-premises](across-working-with-business-central-in-powerbi.md).

<!--Once you have a Power BI account, you can sign in at [https://powerbi.microsoft.com/](https://powerbi.microsoft.com/).

The Power BI service hosts all the reports available to you. To see the report, select **My Workspace** > **Reports**. Then just select the report that you want to view.

With [!INCLUDE[prod_short](includes/prod_short.md)] online, you'll automatically have a set of default reports on your workspace. If you want to create your own reports, you can use Power BI Desktop to create reports, and then publish them to your workspace. For more information, see [Getting Started Building Reports in Power BI Desktop to Display [!INCLUDE [prod_long](includes/prod_long.md)] Data](across-how-use-financials-data-source-powerbi.md).

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

If you're using [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, you'll have to start from scratch by using Power BI Desktop. Optionally, Power BI reports can be distributed as files, that you can upload.

<!--## Get the latest data

Each Power BI report is based on a dataset that gets data from the [!INCLUDE[prod_short](includes/prod_short.md)] sources. You want to make sure that the data in your Power BI reports is up to date with the data in [!INCLUDE[prod_short](includes/prod_short.md)]. This concept is referred to as *refreshing*.  Depending on how your organization has set up Power BI, refreshing might not happen automatically. There are two ways to refresh data: manually or by scheduling a refresh. Manual refreshing is done on-demand, as needed. Scheduled refreshing lets you refresh automatically at defined time intervals.

### Refresh manually

In the navigation pane, under **Datasets**, select **More options (...)** next to the dataset, then select **Refresh now**.

### Schedule a refresh

In the navigation pane, under Datasets, select More options (...) next to the dataset, then select **Schedule refresh**. Fill in the information under the **Schedule refresh** section, and select **Apply**.

For more information, see [Configure scheduled refresh](/power-bi/connect-data/refresh-scheduled-refresh)-->

<!--## <a name="upload"></a>Upload reports from files

Power BI Reports can be distributed among users as .pbix files. If you have a .pbix file, you can upload the file to a workspace. To upload a report, do the following steps:

1. In your new workspace, select **Get Data**.

2. In the Files box, select **Get**.

3. Select **Local File**, navigate to where you saved the file, and select **Open**.

For more information, see [Upload the report to the service](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

> [!NOTE]
> Uploading a report requires that you have a [Premium capacity](/power-bi/service-premium-what-is) work space. For more information, see [Managing Premium capacities](/power-bi/admin/service-premium-capacity-manage). 

> [!TIP]
> If you're using [!INCLUDE[prod_short](includes/prod_short.md)] online, you can also upload a report from within [!INCLUDE[prod_short](includes/prod_short.md)]. For more information, see [Work with Power BI Reports in [!INCLUDE [prod_short](includes/prod_short.md)] - Upload Reports](across-working-with-powerbi.md#upload).

## <a name="share"></a>Share reports with others

Once a report is in your workspace, you can share it with others in your organization.

To share a report, in a list reports, or in an open report, select **Share**. In the **Share report** pane, enter the full email addresses for individuals or distribution groups you want to share with. Follow the instructions on screen to complete the sharing. For more information, see [Share a dashboard or report](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

> [!NOTE]
> You must have  [Power BI Pro license](/power-bi/service-features-license-type), and the people you share with do too. The content must be in a workspace in a [Premium capacity](/power-bi/service-premium-what-is). For more information, see [Ways to share your work in Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).-->

## Se også

[Business Central og Power BI](admin-powerbi.md)  
[Overføre rapport fra filer](across-working-with-powerbi.md#upload-reports)  
 
[!INCLUDE[footer-include](includes/footer-banner.md)]
