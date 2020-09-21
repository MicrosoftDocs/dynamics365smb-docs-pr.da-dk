---
title: Aktivering af Power BI-integration med Business Central| Microsoft Docs
description: Du kan nemt få indsigt, business intelligence og nøgletal i dine Business Central-data med Business Central-apps for Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 92b3bb1d04c58332db20c978928fe1b04ed2ab37
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697745"
---
# <a name="enabling-power-bi-integration-with-prodshort"></a>Aktivering af Power BI-integration med [!INCLUDE[prodshort](includes/prodshort.md)]

Denne artikel beskriver, hvordan du får [!INCLUDE[prodshort](includes/prodshort.md)] klar til integration med Power BI. [!INCLUDE[prodshort](includes/prodshort.md)] online er allerede aktiveret til integration, selvom der er nogle oplysninger om licens, som du måske vil læse. For [!INCLUDE[prodshort](includes/prodshort.md)] i det lokale miljø skal du indstille dit miljø til at oprette forbindelse til Power BI, før brugerne kan arbejde med det.

## <a name="power-bi-licensing"></a><a name="license"></a>Power BI-licenser

Med [!INCLUDE[prodshort](includes/prodshort.md)] får brugerne en gratis Power BI-licens, som giver adgang til de mest almindelige funktioner i [!INCLUDE[prodshort](includes/prodshort.md)] og Power BI. Du kan også købe en Power BI Pro-licens, der giver adgang til yderligere funktioner. Følgende tabel indeholder en oversigt over de funktioner, der er tilgængelige for hver enkelt licens.

|Power-licens|Se rapporter|Oprette rapporter|Dele rapporter|Opdatere rapporter| [!INCLUDE[prodshort](includes/prodshort.md)]-apps|
|-------------|--------||
|Power BI gratis|![check](media/check.png)|![check](media/check.png)|(begrænset)|(begrænset)||
|Power BI Pro|![check](media/check.png)|![check](media/check.png)|![check](media/check.png)|(omfattende)|![check](media/check.png)|

Du kan finde flere oplysninger under [Licenser til Power BI-tjenesten for brugere i organisationen](/power-bi/admin/service-admin-licensing-organization) eller [Tilmelde dig Power BI-tjenesten som en person](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="set-up-prodshort-on-premises-for-power-bi-integration"></a><a name="setup"></a>Konfigurere [!INCLUDE[prodshort](includes/prodshort.md)] i det lokale miljø for Power BI-integration

I dette afsnit forklares kravene til en installation af [!INCLUDE[prodshort](includes/prodshort.md)] i det lokale miljø, der kan integreres med Power BI.

1. OData-webtjenester og ODataV4-slutpunktet er aktiveret.

    OData-webtjenesten skal være aktiveret på [!INCLUDE[server](includes/server.md)], og OData-porten skal være åbnet i firewall. Du kan finde flere oplysninger under [Konfiguration af Business Central Server - OData-webtjenester](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).
    
    Den lokale server skal være tilgængelig fra internettet.

2. [!INCLUDE[prodshort](includes/prodshort.md)]-brugerkonti har adgangsnøgle til webtjenesten.

    Der kræves en adgangsnøgle til webtjenester for at få vist [!INCLUDE[prodshort](includes/prodshort.md)]-data i Power BI. Du kan tildele hver brugerkonto en adgangsnøgle til webtjenesten. Du kan i stedet oprette en specifik konto med en adgangsnøgle til webtjeneste, så alle brugere kan anvende den. Du kan finde flere oplysninger i [Godkendelse af webtjenester](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

3. NavUserPassword eller Azure Active Directory-godkendelse er konfigureret.

4. Hvis du vil have vist Power BI-rapporter integreret på [!INCLUDE[prodshort](includes/prodshort.md)]-sider, skal et program registreres for [!INCLUDE[prodshort](includes/prodshort.md)] i Microsoft Azure.

    Det registrerede program skal have tilladelse til Power BI-tjenester. Du kan finde flere oplysninger i [Registrering af [!INCLUDE[prodshort](includes/prodshort.md)] i det lokale miljø i Azure AD til integration med andre tjenester](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Hvis din installation benytter NavUserPassword-godkendelse, opretter [!INCLUDE[prodshort](includes/prodshort.md)] forbindelse til den samme Power BI-tjeneste for alle brugere. Du skal angive denne tjenestekonto som en del af registreringen af programmet. Med Azure AD-godkendelse opretter [!INCLUDE[prodshort](includes/prodshort.md)] forbindelse til den Power BI-tjeneste, der er knyttet til de enkelte brugerkonti.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->

## <a name="publish-data-as-web-services"></a>Udgive data som webtjenester

Codeunits, sider og forespørgsler, som du vil bruge som datakilder i Power BI-rapporter, skal udgives som webtjenester. Der udgives mange webtjenester som standard. En nem måde at finde webtjenesterne på er at søge efter *webtjenester* i [!INCLUDE[prodshort](includes/prodshort.md)]. På siden **Webtjenester** skal du sørge for, at feltet **Udgiv** er markeret for de webtjenester, der er angivet ovenfor. Denne opgave er typisk en administrativ opgave.

Du kan finde flere oplysninger om udgivelse af webtjenester under [Udgive en webtjeneste](across-how-publish-web-service.md).

> [!TIP]
> Du kan få mere at vide om, hvad du kan gøre for at sikre den bedste ydeevne af webtjenester, set fra Business Central Server (slutpunktet) og fra forbrugeren (klienten), ved at læse [Skrive effektive webtjenester](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).




## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/Configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Business Central og Power BI](admin-powerbi.md)  
[Oversigt over Power BI-integrationskomponent og -arkitektur for [!INCLUDE[prodshort](includes/prodshort.md)]](admin-powerbi-overview.md)  
[Power BI for forbrugere](/power-bi/consumer/end-user-consumer)  
[Power BI-tjenestens nye udseende](/power-bi/service-new-look)  
[Hurtig start: Opret forbindelse til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI-dokumentation](/power-bi/)  
[Business Intelligence](bi.md)  
[Introduktion](product-get-started.md)  
[Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] som Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] som Power Apps-datakilde](across-how-use-financials-data-source-powerapps.md)  
[Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
