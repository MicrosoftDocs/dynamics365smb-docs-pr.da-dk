---
title: Aktivering af Power BI-integration med Business Central
description: Få mere at vide om, hvordan du konfigurerer forbindelsen til Power BI. Få indsigt, business intelligence og KPI'er fra Business Central-data med Power BI.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Power BI, setup, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: c893513098d5078995e6cab09abcf0d2e0bb2769
ms.sourcegitcommit: 7b6d70798b4da283d1d3e38a05151df2209c2b72
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/12/2022
ms.locfileid: "8950352"
---
# <a name="enabling-power-bi-integration-with-prod_short"></a>Aktivering af Power BI-integration med [!INCLUDE[prod_short](includes/prod_short.md)]

Denne artikel beskriver, hvordan du får [!INCLUDE[prod_short](includes/prod_short.md)] klar til integration med Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online er allerede aktiveret til integration, selvom der er nogle oplysninger om licens, som du måske vil læse. For [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø skal du indstille dit miljø til at oprette forbindelse til Power BI, før brugerne kan arbejde med det.

## <a name="power-bi-licensing"></a><a name="license"></a>Power BI-licenser

Med [!INCLUDE[prod_short](includes/prod_short.md)] får brugerne en gratis Power BI-licens, som giver adgang til de mest almindelige funktioner i [!INCLUDE[prod_short](includes/prod_short.md)] og Power BI. Du kan også købe en Power BI Pro-licens, der giver adgang til yderligere funktioner. Følgende tabel indeholder en oversigt over de funktioner, der er tilgængelige for hver enkelt licens.

|Power-licens|Se rapporter|Oprette rapporter|Dele rapporter|Opdatere rapporter| [!INCLUDE[prod_short](includes/prod_short.md)]-apps|
|-------------|--------||
|Power BI gratis|![en markering.](media/check.png)|![en anden markering](media/check.png)|(begrænset)|(begrænset)||
|Power BI Pro|![endnu en markering.](media/check.png)|![det er en markering](media/check.png)|![endnu en markering](media/check.png)|(omfattende)|![sidste markering](media/check.png)|

Du kan finde flere oplysninger i [Licenser til Power BI-tjenesten for brugere i organisationen](/power-bi/admin/service-admin-licensing-organization) eller [Tilmelde dig Power BI-tjenesten som en person](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="expose-data-through-api-pages-or-odata-web-services"></a><a name="exposedata"></a>Vise data ved hjælp af API-sider eller OData-webtjenester

Business Central giver mulighed for at vise data, der kan forbruges af Power BI-rapporter: API-sider og åbne dataprotokol (OData) webtjenester.

### <a name="api-pages"></a>API-sider

> **GÆLDER FOR:** Kun Business Central online 

En API-side er en bestemt sidetype, der er oprettet med AL kode, som giver adgang til databasetabeller via en webhook-understøttet OData v4-enabled, REST-tjeneste. Denne type side kan ikke vises i brugergrænsefladen, men er beregnet til opbygning af pålidelige integrationstjenester.

Business Central Online leveres med et sæt indbyggede API'er, som du kan bruge til at hente data til de mest almindelige forretningsenheder, f. eks. kunder, varer, salgsordrer og meget andet. Der kræves ikke ekstra arbejde eller installation for at bruge disse API'er som datakilde til Power BI-rapporter. Du kan finde flere oplysninger om disse API'er i [Business Central API v 2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/).

Business central online understøtter også brugerdefinerede API'er. Programudviklere af Business Central-løsninger kan oprette deres egne API-sider og pakke dem ind i udvidelser. Du kan derefter installere udvidelserne på din lejer. Når du har installeret, kan du bruge API-siderne til dine Power BI-rapporter som du gjorde med indbyggede API'er (v 2.0). Du kan finde flere oplysninger om, hvordan du opretter API-sider, under [udvikling af en brugerdefineret API](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api).

> [!IMPORTANT]
> Fra og med februar 2022 er Power BI-rapporter om [!INCLUDE[prod_short](includes/prod_short.md)] Online baseret på en sekundær, skrivebeskyttet databasereplika af hensyn til ydeevne. AL-udviklere bør derfor undgå at designe API-sider, som foretager databaseændringer, mens siderne åbner eller indlæser poster. Overvej især koden på AL triggers: OnInit, OnOpenPage, OnFindRecord, OnNextRecord, OnAfterGetRecord og OnAfterGetCurrRecord. Disse databaseændringer kan i visse tilfælde medføre problemer med ydeevnen og forhindrer, at rapporten opdaterer data. Du kan finde flere oplysninger i [ydeevneartikler for udviklere](/dynamics365/business-central/dev-itpro/performance/performance-developer?branch=main#writing-efficient-web-services) i Business central Development hjælp.
>
> I sjældne tilfælde vil problemet medføre en fejl, når en bruger prøver at hente data fra API-siden til en rapport i Power BI Desktop. Hvis det er nødvendigt at foretage ændringer af databasen på den brugerdefinerede API-side, kan Power BI Desktop-brugere imidlertid gennemtvinge funktionaliteten. Du kan finde flere oplysninger i [Oprettelse af Power BI-rapporter for at få vist Business Central-data](across-how-use-financials-data-source-powerbi.md#fixing-problems).

### <a name="odata-web-services"></a>OData-webtjenester

Du kan udgive Business Central-applikationsobjekter, f. eks. kodeenheder, side og forespørgsler som [OData-webtjenester](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). Med Business central online er der som standard udgivet mange webtjenester. En nem måde at finde webtjenesterne på er at søge efter *webtjenester* i [!INCLUDE[prod_short](includes/prod_short.md)]. På siden **Webtjenester** skal du sørge for, at feltet **Udgiv** er markeret for de webtjenester, der er angivet ovenfor. Du kan finde flere oplysninger om udgivelse af webtjenester under [Udgive en webtjeneste](across-how-publish-web-service.md).

Du kan få mere at vide om, hvad du kan gøre for at sikre den bedste ydeevne af webtjenester, set fra Business Central Server (slutpunktet) og fra forbrugeren (klienten), ved at læse [Skrive effektive webtjenester](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).

### <a name="choosing-whether-to-use-api-pages-or-odata-web-services"></a>Vælg, om der skal bruges API-sider eller OData-webtjenester

Når det er muligt, anbefales det, at du bruger API-sider i stedet for OData-webtjeneste. API-sider er generelt hurtigere ved indlæsning af data i Power BI-rapporter end OData-webtjenester. Desuden er de mere fleksible, fordi de giver dig mulighed for at få data fra tabelfelter, som ikke er defineret i et sideobjekt.

## <a name="set-up-prod_short-on-premises-for-power-bi-integration"></a><a name="setup"></a>Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø for Power BI-integration

I dette afsnit forklares kravene til en installation af [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø, der kan integreres med Power BI.

1. Konfigurer enten NavUserPassword eller Azure Active Directory-godkendelse for installationen.

    Power BI-integration understøtter ikke Windows-godkendelse.  

2. Aktivere OData-webtjenester og ODataV4-slutpunkt.

    OData-webtjenesten skal være aktiveret på [!INCLUDE[server](includes/server.md)], og OData-porten skal være åbnet i firewall. Du kan finde flere oplysninger i [Konfiguration af Business Central Server - OData-webtjenester](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    Den lokale server skal være tilgængelig fra internettet.

3. Tildele [!INCLUDE[prod_short](includes/prod_short.md)]-brugerkonti adgangsnøgle til webtjenesten.

    Der kræves kun en adgangsnøgle til webtjenester for at få vist [!INCLUDE[prod_short](includes/prod_short.md)]-data i Power BI. Du kan tildele hver brugerkonto en adgangsnøgle til webtjenesten. Du kan i stedet oprette en specifik konto med en adgangsnøgle til webtjeneste, så alle brugere kan anvende den. Du kan finde flere oplysninger i [Godkendelse af webtjenester](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

    <!--
    > [!IMPORTANT]
    > With [!INCLUDE[prod_short](../developer/includes/prod_short.md)] online, the use of access keys (Basic Auth) for web service authentication is [deprecated](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#accesskeys). We recommend that you use OAuth2 instead. For more information, see [Use OAuth to Authorize Business Central Web Services](/dynamics365/business-central/dev-itpro/webservices/authenticate-web-services-using-oauth).-->

4. Oprette en programregistrering for [!INCLUDE[prod_short](includes/prod_short.md)] i Microsoft Azure.

    Hvis du vil have vist Power BI-rapporter integreret på [!INCLUDE[prod_short](includes/prod_short.md)]-sider, skal et program registreres for [!INCLUDE[prod_short](includes/prod_short.md)] i Microsoft Azure. Det registrerede program skal have tilladelse til Power BI-tjenester. Som minimum kræver app'en **User.ReadWrite.All**-tilladelser. For at brugerne kan få vist rapporter fra delte Power BI-arbejdsområder, kræver appen **Workspace.Read.All**-tilladelse. Du kan finde flere oplysninger i [Registrering af [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø i Azure AD til integration med andre tjenester](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Hvis din installation benytter NavUserPassword-godkendelse, opretter [!INCLUDE[prod_short](includes/prod_short.md)] forbindelse til den samme Power BI-tjeneste for alle brugere. Du skal angive denne tjenestekonto som en del af registreringen af programmet. Med Azure AD-godkendelse opretter [!INCLUDE[prod_short](includes/prod_short.md)] forbindelse til den Power BI-tjeneste, der er knyttet til de enkelte brugerkonti.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
5. Foretage den første forbindelse mellem Business central og Power BI.

    Før slutbrugere kan bruge Power BI i [!INCLUDE[prod_short](includes/prod_short.md)], skal en Azure-programadministrator give samtykke til Power BI-tjenesten.

    Hvis du vil oprette den første forbindelse, skal du åbne [!INCLUDE[prod_short](includes/prod_short.md)] og køre **Introduktion til Power BI** fra Rollecenter. Handlingen vil føre dig gennem samtykkeprocessen og kontrollere Power BI-licensen. Når du bliver bedt om at logge på med en Azure admin-konto. Du kan få flere oplysninger i [Tilknyt til Power BI - én gang](across-working-with-powerbi.md#connect)..


## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/Configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Business Central og Power BI](admin-powerbi.md)  
[Oversigt over Power BI-integrationskomponent og -arkitektur for [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Power BI for forbrugere](/power-bi/consumer/end-user-consumer)  
[Power BI-tjenestens nye udseende](/power-bi/service-new-look)  
[Hurtig start: Opret forbindelse til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI-dokumentation](/power-bi/)  
[Business Intelligence](bi.md)  
[Blive køreklar](ui-get-ready-business.md)  
[Import af virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Brug af [!INCLUDE[prod_short](includes/prod_short.md)] som Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Brug af [!INCLUDE[prod_short](includes/prod_short.md)] som Power Apps-datakilde](across-how-use-financials-data-source-powerapps.md)  
[Brug [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]