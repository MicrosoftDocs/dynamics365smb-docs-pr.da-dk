---
title: Intelligente indsigter og skymigrering | Microsoft Docs
description: Opret forbindelse til intelligent indsigt med Business Central fra din lokale løsning. Få mere at vide om, hvordan du overfører til skyen.
author: bmeier94
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms. search.keywords: cloud, edge
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ca7fd910e70deaebbf8912eecfe6d9c25ddfcc4e
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385120"
---
# <a name="intelligent-insights-with-prod_short-online"></a><span data-ttu-id="3ade4-104">Intelligent indsigt med [!INCLUDE[prod_short](includes/prod_short.md)] Online</span><span class="sxs-lookup"><span data-stu-id="3ade4-104">Intelligent Insights with [!INCLUDE[prod_short](includes/prod_short.md)] Online</span></span>

<span data-ttu-id="3ade4-105">Som bruger af [!INCLUDE[prod_short](includes/prod_short.md)] online har du fuld adgang til scenarier, der er baseret på den intelligente sky, f.eks. KPI'er, der er baseret på maskinel indlæring, eller når du får vist dataene i Power BI.</span><span class="sxs-lookup"><span data-stu-id="3ade4-105">As a user of [!INCLUDE[prod_short](includes/prod_short.md)] online, you have full access to scenarios that are based on the intelligent cloud, such as KPIs that are based on machine learning, or when you view your data in Power BI.</span></span> <span data-ttu-id="3ade4-106">[!INCLUDE[prod_short](includes/prod_short.md)] er en cloud-first service, men også de kunder, der udelukkende skal køre deres arbejdsbelastning lokalt eller på den intelligente edge, der er forbundet med skyen, kan gøre dette.</span><span class="sxs-lookup"><span data-stu-id="3ade4-106">However, while [!INCLUDE[prod_short](includes/prod_short.md)] is a cloud-first service, also those customers who need to run their workloads fully on-premises or on the intelligent edge connected to the cloud can do so.</span></span>  

<span data-ttu-id="3ade4-107">Hvis du er interesseret i [!INCLUDE[prod_short](includes/prod_short.md)], kan du tilmelde dig en gratis prøveversion online, eller du kan vælge at arbejde med en partner for at implementere [!INCLUDE[prod_short](includes/prod_short.md)] lokalt på hardware efter dit eget valg.</span><span class="sxs-lookup"><span data-stu-id="3ade4-107">If you are interested in [!INCLUDE[prod_short](includes/prod_short.md)], you can sign up for a free trial online, or you can choose to work with a partner to deploy [!INCLUDE[prod_short](includes/prod_short.md)] locally to your own choice of hardware.</span></span> <span data-ttu-id="3ade4-108">Du kan derefter vælge at få en intelligent indsigt ved at oprette forbindelse til en lejer i skyen.</span><span class="sxs-lookup"><span data-stu-id="3ade4-108">You can then decide to get intelligent insights by connecting to a tenant in the cloud.</span></span> <span data-ttu-id="3ade4-109">Data fra din on-premises installation af [!INCLUDE[prod_short](includes/prod_short.md)] kopieres derefter til skyen til brug for intelligente skyscenarier.</span><span class="sxs-lookup"><span data-stu-id="3ade4-109">As a result, the data from your [!INCLUDE[prod_short](includes/prod_short.md)] on-premises deployment replicates to the cloud for intelligent cloud scenarios.</span></span>  

<span data-ttu-id="3ade4-110">Når du vil oprette forbindelse til den intelligente sky fra en lokal løsning, skal din systemadministrator angive oplysninger om din database.</span><span class="sxs-lookup"><span data-stu-id="3ade4-110">Connecting to the intelligent cloud from an on-premises solution requires your administrator to specify information about your database.</span></span> <span data-ttu-id="3ade4-111">De værktøjer, der bruges til at forbinde din lokale installation med [!INCLUDE[prod_short](includes/prod_short.md)] online, er de samme, som også bruges til at overføre fra et lokalt miljø til et onlinemiljø.</span><span class="sxs-lookup"><span data-stu-id="3ade4-111">The tools used to connect your on-premises deployment to [!INCLUDE[prod_short](includes/prod_short.md)] online are the same that are also used to migration from on-premises to online.</span></span> <span data-ttu-id="3ade4-112">Du kan finde flere oplysninger i [Overførsel af lokale data til Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) i administrationsindholdet for [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="3ade4-112">For more information, see [Migrating On-Premises Data to Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in the administration content for [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="viewing-intelligent-cloud-insights-in-prod_short-online"></a><span data-ttu-id="3ade4-113">Visning af intelligent skyindsigt i [!INCLUDE[prod_short](includes/prod_short.md)] online</span><span class="sxs-lookup"><span data-stu-id="3ade4-113">Viewing Intelligent Cloud Insights in [!INCLUDE[prod_short](includes/prod_short.md)] Online</span></span>

<span data-ttu-id="3ade4-114">I din [!INCLUDE[prod_short](includes/prod_short.md)] online-virksomhed viser siden **Intelligent skyindsigt** fire vigtige steder, der er af interesse for de fleste virksomheder:</span><span class="sxs-lookup"><span data-stu-id="3ade4-114">In your [!INCLUDE[prod_short](includes/prod_short.md)] online company, the **Intelligent Cloud Insights** page shows four key points of interest for most businesses:</span></span>

- <span data-ttu-id="3ade4-115">Tilgængelig kassebeholdning</span><span class="sxs-lookup"><span data-stu-id="3ade4-115">Cash availability</span></span>
- <span data-ttu-id="3ade4-116">Salgsrentabilitet</span><span class="sxs-lookup"><span data-stu-id="3ade4-116">Sales profitability</span></span>
- <span data-ttu-id="3ade4-117">Årets resultat</span><span class="sxs-lookup"><span data-stu-id="3ade4-117">Net income</span></span>
- <span data-ttu-id="3ade4-118">Lagerværdi</span><span class="sxs-lookup"><span data-stu-id="3ade4-118">Inventory value</span></span>

<span data-ttu-id="3ade4-119">Ved siden af KPI-diagrammer kan få du indsigt i potentielle problemområder, herunder forfaldne betalinger.</span><span class="sxs-lookup"><span data-stu-id="3ade4-119">Next to the KPI charts, you get insights into potential areas of concern, including overdue payments.</span></span> <span data-ttu-id="3ade4-120">Vælg hver indsigt for at dykke ned i dataene.</span><span class="sxs-lookup"><span data-stu-id="3ade4-120">Choose each insight to drill into the data.</span></span>  

> [!div class="mx-imgBorder"]
> <span data-ttu-id="3ade4-121">![Intelligent cloudindsigt](media/across-intelligent-cloud/intelligentcloudApril19.png "Viser siden Intelligent cloudindsigt i Business Central")</span><span class="sxs-lookup"><span data-stu-id="3ade4-121">![Intelligent cloud insights](media/across-intelligent-cloud/intelligentcloudApril19.png "Shows the Intelligent Cloud Insights page in Business Central")</span></span>

<span data-ttu-id="3ade4-122">Siden opretter også forbindelse til Power BI, hvor du kan få endnu flere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="3ade4-122">The page also connects to Power BI for even more insights.</span></span>

## <a name="viewing-intelligent-insights-on-premises"></a><span data-ttu-id="3ade4-123">Visning af intelligent indsigt til det lokale miljø</span><span class="sxs-lookup"><span data-stu-id="3ade4-123">Viewing Intelligent Insights On-Premises</span></span>

<span data-ttu-id="3ade4-124">Når din Dynamics 365-videresalgspartner har fået den rigtige licens til din lokale løsning og kan oprette forbindelse til skyen ved hjælp af [!INCLUDE[prod_short](includes/prod_short.md)], kan din administrator oprette forbindelsen.</span><span class="sxs-lookup"><span data-stu-id="3ade4-124">When your Dynamics 365 reselling partner has acquired the right license for your on-premises solution to connect to the cloud through [!INCLUDE[prod_short](includes/prod_short.md)], your administrator can set up the connection.</span></span> <span data-ttu-id="3ade4-125">Når det er gjort, kan du få samme indsigt fra skyen i dit lokale program.</span><span class="sxs-lookup"><span data-stu-id="3ade4-125">Once that is done, you can view the same insights from the cloud in your on-premises application.</span></span> <span data-ttu-id="3ade4-126">Afhængigt af din lokale løsning kan siden **Intelligent skyindsigt** integreres på startsiden eller på en separat side som i [!INCLUDE[prod_short](includes/prod_short.md)] online og til det lokale miljø.</span><span class="sxs-lookup"><span data-stu-id="3ade4-126">Depending on the on-premises solution, the **Intelligent Cloud Insights** page can be embedded in the Home page or be a separate page as in [!INCLUDE[prod_short](includes/prod_short.md)] online and on-premises.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3ade4-127">Se også</span><span class="sxs-lookup"><span data-stu-id="3ade4-127">See Also</span></span>

[<span data-ttu-id="3ade4-128">Velkommen til Business Central</span><span class="sxs-lookup"><span data-stu-id="3ade4-128">Welcome to Business Central</span></span>](index.md)  
[<span data-ttu-id="3ade4-129">Intelligente skyudvidelser til skymigrering</span><span class="sxs-lookup"><span data-stu-id="3ade4-129">Intelligent Cloud Extensions for Cloud Migration</span></span>](ui-extensions-data-replication.md)  
[<span data-ttu-id="3ade4-130">Overførsel af lokale data til Business Central Online</span><span class="sxs-lookup"><span data-stu-id="3ade4-130">Migrating On-Premises Data to Business Central Online</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-data)  


[!INCLUDE[footer-include](includes/footer-banner.md)]