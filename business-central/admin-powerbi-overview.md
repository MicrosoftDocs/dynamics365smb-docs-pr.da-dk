---
title: Oversigt over Power BI-integrationskomponent og -arkitektur for Business central| Microsoft Docs
description: Du kan nemt få indsigt, business intelligence og nøgletal i dine Business Central-data med Business Central-apps for Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 9514f0355932c1b1cbd30acfdb9f6dab46db8a0a
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697742"
---
# <a name="power-bi-integration-component-and-architecture-overview-for-prodshort"></a><span data-ttu-id="9a4fa-103">Oversigt over Power BI-integrationskomponent og -arkitektur for [!INCLUDE[prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="9a4fa-103">Power BI Integration Component and Architecture Overview for [!INCLUDE[prodshort](includes/prodshort.md)]</span></span>

<span data-ttu-id="9a4fa-104">I denne artikel kan du læse om de forskellige aspekter ved Power BI-integration med [!INCLUDE[prodshort](includes/prodshort.md)] som hjælp til at forstå implementering og brug.</span><span class="sxs-lookup"><span data-stu-id="9a4fa-104">In this article, you'll learn about the different aspects of Power BI integration with [!INCLUDE[prodshort](includes/prodshort.md)] to help you understand its implementation and use.</span></span>

## <a name="components"></a><span data-ttu-id="9a4fa-105">Komponenter</span><span class="sxs-lookup"><span data-stu-id="9a4fa-105">Components</span></span>

<span data-ttu-id="9a4fa-106">I følgende tabel beskrives de vigtigste komponenter, der indgår i Power BI-integrationen.</span><span class="sxs-lookup"><span data-stu-id="9a4fa-106">The following table describes the major components involved with Power BI integration.</span></span>

|<span data-ttu-id="9a4fa-107">Komponent</span><span class="sxs-lookup"><span data-stu-id="9a4fa-107">Component</span></span>|<span data-ttu-id="9a4fa-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="9a4fa-108">Description</span></span>|
|---------|-----------|
|<span data-ttu-id="9a4fa-109">Power BI</span><span class="sxs-lookup"><span data-stu-id="9a4fa-109">Power BI</span></span>|<span data-ttu-id="9a4fa-110">En skybaseret rapporttjeneste, der er baseret på vært og administration.</span><span class="sxs-lookup"><span data-stu-id="9a4fa-110">A cloud-based report hosting and management service.</span></span>|
|<span data-ttu-id="9a4fa-111">Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="9a4fa-111">Power BI Desktop</span></span>|<span data-ttu-id="9a4fa-112">Et oprettelsesværktøj til opbygning af rapporter og dashboards, og du kan køre rapporter.</span><span class="sxs-lookup"><span data-stu-id="9a4fa-112">An authoring tool for building reports and dashboards, and allows you to run reports.</span></span> <span data-ttu-id="9a4fa-113">Den kan hentes gratis på Microsoft Store og installeres lokalt.</span><span class="sxs-lookup"><span data-stu-id="9a4fa-113">It's available as a free download on Microsoft Store and is installed locally.</span></span>|
|[!INCLUDE[prodshort](includes/prodshort.md)]|<span data-ttu-id="9a4fa-114">Online eller lokal løsning med connectorer til Power BI og mulighed for at integrere en Power BI-del.</span><span class="sxs-lookup"><span data-stu-id="9a4fa-114">Online or on-premises solution with connectors exposed to Power BI and the ability to embed a Power BI part.</span></span>|

## <a name="whats-available-from-the-start"></a><span data-ttu-id="9a4fa-115">Hvad er tilgængeligt fra begyndelsen</span><span class="sxs-lookup"><span data-stu-id="9a4fa-115">What's available from the start</span></span>

<span data-ttu-id="9a4fa-116">Følgende tabel beskriver de tilgængelige funktioner.</span><span class="sxs-lookup"><span data-stu-id="9a4fa-116">The following table describes available features.</span></span>

|<span data-ttu-id="9a4fa-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="9a4fa-117">Feature</span></span>|[!INCLUDE[prodshort](includes/prodshort.md)] <span data-ttu-id="9a4fa-118">online eller lokal understøttelse</span><span class="sxs-lookup"><span data-stu-id="9a4fa-118">online or on-premises support</span></span>|
|-------|---------------------|
|<span data-ttu-id="9a4fa-119">Power BI-connectorer</span><span class="sxs-lookup"><span data-stu-id="9a4fa-119">Power BI connectors</span></span>|<span data-ttu-id="9a4fa-120">Begge dele.</span><span class="sxs-lookup"><span data-stu-id="9a4fa-120">Both.</span></span> <span data-ttu-id="9a4fa-121">Forskellige connectorer til online og lokal version.</span><span class="sxs-lookup"><span data-stu-id="9a4fa-121">Different connectors for online and on-premises.</span></span> <span data-ttu-id="9a4fa-122">Samme connector, der bruges til Power BI Desktop og Power BI-service</span><span class="sxs-lookup"><span data-stu-id="9a4fa-122">Same connector used for Power BI Desktop and Power BI Service</span></span> |
|<span data-ttu-id="9a4fa-123">Integreret oplevelse ved visning af en bestemt rapport i en faktaboks i [!INCLUDE[prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="9a4fa-123">Embedded experience for viewing a given report inside a FactBox in [!INCLUDE[prodshort](includes/prodshort.md)]</span></span>|<span data-ttu-id="9a4fa-124">Begge dele.</span><span class="sxs-lookup"><span data-stu-id="9a4fa-124">Both.</span></span> <span data-ttu-id="9a4fa-125">Kræver konfiguration for at vise rapporter lokalt.</span><span class="sxs-lookup"><span data-stu-id="9a4fa-125">Requires configuration to display reports for on-premises.</span></span>|
|<span data-ttu-id="9a4fa-126">Power BI-rapportstyring fra [!INCLUDE[prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="9a4fa-126">Power BI report management from [!INCLUDE[prodshort](includes/prodshort.md)]</span></span>|<span data-ttu-id="9a4fa-127">Online</span><span class="sxs-lookup"><span data-stu-id="9a4fa-127">Online</span></span>|
|<span data-ttu-id="9a4fa-128">Standardrapporter fra Power BI i rollecentre, der er udrullet til Power BI</span><span class="sxs-lookup"><span data-stu-id="9a4fa-128">Default Power BI reports on role centers deployed to Power BI</span></span>|<span data-ttu-id="9a4fa-129">Online</span><span class="sxs-lookup"><span data-stu-id="9a4fa-129">Online</span></span>|
|<span data-ttu-id="9a4fa-130">Power BI-apps på Microsoft AppSource</span><span class="sxs-lookup"><span data-stu-id="9a4fa-130">Power BI Apps on Microsoft AppSource</span></span>|<span data-ttu-id="9a4fa-131">Online.</span><span class="sxs-lookup"><span data-stu-id="9a4fa-131">Online.</span></span>|

## <a name="architecture"></a><span data-ttu-id="9a4fa-132">Arkitektur</span><span class="sxs-lookup"><span data-stu-id="9a4fa-132">Architecture</span></span>

[!INCLUDE[prodshort](includes/prodshort.md)] <span data-ttu-id="9a4fa-133">integreres med Power BI via en connector, der bruger OData.</span><span class="sxs-lookup"><span data-stu-id="9a4fa-133">integrates with Power BI through a connector using OData.</span></span> <span data-ttu-id="9a4fa-134">Datakilden til Power BI-rapporter vises som OData-webtjenester.</span><span class="sxs-lookup"><span data-stu-id="9a4fa-134">The data source for Power BI reports is exposed as OData web services.</span></span>

![Power BI-arkitektur til integration med Business Central](./media/power-bi-architecture.png)

## <a name="general-flow"></a><span data-ttu-id="9a4fa-136">Generelt flow</span><span class="sxs-lookup"><span data-stu-id="9a4fa-136">General Flow</span></span>

<span data-ttu-id="9a4fa-137">I følgende diagram illustreres den grundlæggende arbejdsgang for brugere, når der oprettes forbindelse mellem [!INCLUDE[prodshort](includes/prodshort.md)] og Power BI.</span><span class="sxs-lookup"><span data-stu-id="9a4fa-137">The following diagram illustrates the basic workflow for users when connecting [!INCLUDE[prodshort](includes/prodshort.md)] to Power BI.</span></span>

![Power BI-arbejdsgang til integration med Business Central](./media/power-bi-flow.png)

1. <span data-ttu-id="9a4fa-139">Bruger tilmelder sig en Power BI-konto.</span><span class="sxs-lookup"><span data-stu-id="9a4fa-139">User signs up for a Power BI account.</span></span>
2. <span data-ttu-id="9a4fa-140">Bruger opretter forbindelse til Power BI fra [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="9a4fa-140">User connects to Power BI from [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>
3. [!INCLUDE[prodshort](includes/prodshort.md)] <span data-ttu-id="9a4fa-141">kontrollerer licensen.</span><span class="sxs-lookup"><span data-stu-id="9a4fa-141">verifies the license.</span></span>
4. [!INCLUDE[prodshort](includes/prodshort.md)] <span data-ttu-id="9a4fa-142">installerer standardrapporter til Power BI-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="9a4fa-142">deploys default reports to the Power BI service.</span></span> <span data-ttu-id="9a4fa-143">Dette trin forekommer kun for [!INCLUDE[prodshort](includes/prodshort.md)] online.</span><span class="sxs-lookup"><span data-stu-id="9a4fa-143">This step only happens for [!INCLUDE[prodshort](includes/prodshort.md)] online.</span></span>
5. [!INCLUDE[prodshort](includes/prodshort.md)] <span data-ttu-id="9a4fa-144">gør rapporter i Power BI tilgængelige for valg i [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="9a4fa-144">makes reports in Power BI available for selection in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="9a4fa-145">Standardrapporter vises automatisk i Power BI-dele.</span><span class="sxs-lookup"><span data-stu-id="9a4fa-145">Default reports are automatically displayed in Power BI parts.</span></span>
6. <span data-ttu-id="9a4fa-146">Bruger opretter en rapport i Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="9a4fa-146">User creates a report in Power BI Desktop.</span></span>
7. <span data-ttu-id="9a4fa-147">Bruger udgiver rapporten til Power BI-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="9a4fa-147">User publishes the report to the Power BI service.</span></span> <span data-ttu-id="9a4fa-148">Rapporterne kan derefter vælges i [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="9a4fa-148">The reports are then available for selection in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="9a4fa-149">Se relateret oplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="9a4fa-149">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="9a4fa-150">Se også</span><span class="sxs-lookup"><span data-stu-id="9a4fa-150">See Also</span></span>

[<span data-ttu-id="9a4fa-151">Business Central og Power BI</span><span class="sxs-lookup"><span data-stu-id="9a4fa-151">Business Central and Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="9a4fa-152">Power BI for forbrugere</span><span class="sxs-lookup"><span data-stu-id="9a4fa-152">Power BI for consumers</span></span>](/power-bi/consumer/end-user-consumer)  
[<span data-ttu-id="9a4fa-153">Power BI-tjenestens nye udseende</span><span class="sxs-lookup"><span data-stu-id="9a4fa-153">The 'new look' of the Power BI service</span></span>](/power-bi/service-new-look)  
[<span data-ttu-id="9a4fa-154">Hurtig start: Opret forbindelse til data i Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="9a4fa-154">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
[<span data-ttu-id="9a4fa-155">Power BI-dokumentation</span><span class="sxs-lookup"><span data-stu-id="9a4fa-155">Power BI documentation</span></span>](/power-bi/)  
[<span data-ttu-id="9a4fa-156">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="9a4fa-156">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="9a4fa-157">Introduktion</span><span class="sxs-lookup"><span data-stu-id="9a4fa-157">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="9a4fa-158">Importere virksomhedsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="9a4fa-158">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="9a4fa-159">[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="9a4fa-159">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
<span data-ttu-id="9a4fa-160">[Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] som Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="9a4fa-160">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
<span data-ttu-id="9a4fa-161">[Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] som Power Apps-datakilde](across-how-use-financials-data-source-powerapps.md)</span><span class="sxs-lookup"><span data-stu-id="9a4fa-161">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as a Power Apps Data Source](across-how-use-financials-data-source-powerapps.md)</span></span>  
<span data-ttu-id="9a4fa-162">[Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power Automate](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="9a4fa-162">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power Automate](across-how-use-financials-data-source-flow.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
