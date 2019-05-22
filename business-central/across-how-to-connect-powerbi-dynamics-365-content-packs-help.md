---
title: Sådan forbindes Power BI med Business Central | Microsoft Docs
description: Du kan nemt få indsigt, business intelligence og nøgletal i dine Business Central-data med Power BI og Business Central-indholdspakker.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/01/2019
ms.author: solsen
redirect_url: admin-powerbi
ms.openlocfilehash: b7e844f64a96ba02c1a5fa0231f7b6992f972677
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1247394"
---
# <a name="connecting-power-bi-to-dynamics-365-business-central-content-packs"></a><span data-ttu-id="eba96-103">Oprette forbindelse fra Power BI til Dynamics 365 Business Central-indholdspakker</span><span class="sxs-lookup"><span data-stu-id="eba96-103">Connecting Power BI to Dynamics 365 Business Central Content Packs</span></span>
<span data-ttu-id="eba96-104">Du kan nemt få indsigt i dine Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data med Power BI og Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-indholdspakker.</span><span class="sxs-lookup"><span data-stu-id="eba96-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="eba96-105">Power BI henter dine data og opretter derefter et out-of-the-box dashboard og rapporter baseret på dataene.</span><span class="sxs-lookup"><span data-stu-id="eba96-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

<span data-ttu-id="eba96-106">Du skal have en gyldig konto til Dynamics 365 og til Power BI.</span><span class="sxs-lookup"><span data-stu-id="eba96-106">You must have a valid account with Dynamics 365 and with Power BI.</span></span> <span data-ttu-id="eba96-107">Desuden skal du hente [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/), hvis du vil oprette dine egne Power BI rapporter.</span><span class="sxs-lookup"><span data-stu-id="eba96-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) if you wish to create your own Power BI reports.</span></span> <span data-ttu-id="eba96-108">Power BI-indholdspakker kræver tilladelser til de tabeller, hvor data hentes fra.</span><span class="sxs-lookup"><span data-stu-id="eba96-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="eba96-109">Yderligere oplysninger om kravene beskrives nedenfor.</span><span class="sxs-lookup"><span data-stu-id="eba96-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="eba96-110">Sådan oprettes forbindelse</span><span class="sxs-lookup"><span data-stu-id="eba96-110">How to Connect</span></span>
1. <span data-ttu-id="eba96-111">Vælg **Hent data** nederst i venstre navigationsrude.</span><span class="sxs-lookup"><span data-stu-id="eba96-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="eba96-112">![Navigere til Hent data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="eba96-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>

<span data-ttu-id="eba96-113">Du kan også komme i gang fra Dynamics 365 Business Edition.</span><span class="sxs-lookup"><span data-stu-id="eba96-113">You may also get starting from within Dynamics 365 Business Edition.</span></span> <span data-ttu-id="eba96-114">I rollecentret kan du gå til **Rapportvalg** i Power BI Rollecenter-delen.</span><span class="sxs-lookup"><span data-stu-id="eba96-114">From the role center, navigate to **Report Selection** in the Power BI Role Center part.</span></span> <span data-ttu-id="eba96-115">Vælg enten **Service** eller **Min virksomhed** på båndet.</span><span class="sxs-lookup"><span data-stu-id="eba96-115">Select either **Service** or **My Organization** from the ribbon.</span></span> <span data-ttu-id="eba96-116">Hvis en af disse handlinger er markeret, åbnes enten galleriet Organisation i Power BI eller tjenestebiblioteket i Power BI, som også bliver filtreret, så det kun viser indholdspakker, der er relateret til [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="eba96-116">When either of these actions are selected, you will be taken to either the Organization gallery in Power BI or to the services library in Power BI, which will also be filtered to only display content packs related to [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span>

2. <span data-ttu-id="eba96-117">I feltet **Tjenester** skal du vælge **Hent**.</span><span class="sxs-lookup"><span data-stu-id="eba96-117">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="eba96-118">Der åbnes en side med **AppSource** og **Apps til Power BI-apps**.</span><span class="sxs-lookup"><span data-stu-id="eba96-118">This will open a page with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="eba96-119">![Vælg indholdspakker fra onlinetjenester](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="eba96-119">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="eba96-120">Vælg **Apps** under fanen **Apps til Power BI-apps**, vælg den **Microsoft Dynamics 365 Business Central**-indholdspakke, du vil bruge, og vælg derefter **Hent nu**.</span><span class="sxs-lookup"><span data-stu-id="eba96-120">Select **Apps** from the **Apps for Power BI apps** tab, choose the **Microsoft Dynamics 365 Business Central** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="eba96-121">![Vælg Dynamics 365 Business Central, og vælg Hent nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="eba96-121">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="eba96-122">Når du bliver bedt om det, skal du angive navnet på *virksomheden* i [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="eba96-122">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="eba96-123">Dette er ikke det viste navn.</span><span class="sxs-lookup"><span data-stu-id="eba96-123">This is not the display name.</span></span> <span data-ttu-id="eba96-124">Virksomhedsnavnet findes på siden 'Virksomheder' i din [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]-forekomst.</span><span class="sxs-lookup"><span data-stu-id="eba96-124">The company name can be found on the 'Companies' page within your [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] instance.</span></span> 
<span data-ttu-id="eba96-125">![Vælg Dynamics 365 Business Central, og vælg Hent nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="eba96-125">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="eba96-126">Når der er oprettet forbindelse, indlæses et dashboard, en rapport og et datasæt automatisk i dit Power BI-arbejdsområde.</span><span class="sxs-lookup"><span data-stu-id="eba96-126">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="eba96-127">Når dette er fuldført, opdateres felterne med data fra din [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]-virksomhed.</span><span class="sxs-lookup"><span data-stu-id="eba96-127">When completed, the tiles will update with data from your [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] company.</span></span>
<span data-ttu-id="eba96-128">![Vælg Dynamics 365 Business Central, og vælg Hent nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="eba96-128">![Select Dynamics 365 Business Central  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="eba96-129">Hvad nu?</span><span class="sxs-lookup"><span data-stu-id="eba96-129">What Now?</span></span>

- <span data-ttu-id="eba96-130">Prøv [at stille et spørgsmål i feltet Spørgsmål og svar](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) øverst i dashboardet.</span><span class="sxs-lookup"><span data-stu-id="eba96-130">Try [asking a question in the Q&A box](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) at the top of the dashboard.</span></span>
- <span data-ttu-id="eba96-131">[Ændre felterne](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) i dashboardet.</span><span class="sxs-lookup"><span data-stu-id="eba96-131">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="eba96-132">[Vælg et felt](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) for at åbne den underliggende rapport.</span><span class="sxs-lookup"><span data-stu-id="eba96-132">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="eba96-133">Selv om dit datasæt planlægges til at blive opdateret dagligt, kan du ændre tidsplanen for opdatering eller prøve at opdatere det på behov ved hjælp af **Opdater nu**.</span><span class="sxs-lookup"><span data-stu-id="eba96-133">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="eba96-134">Systemkrav</span><span class="sxs-lookup"><span data-stu-id="eba96-134">System Requirements</span></span>
<span data-ttu-id="eba96-135">Hvis du vil importere dine [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data i Power BI, skal du have rettigheder til de webtjenester, der bruges til at hente data.</span><span class="sxs-lookup"><span data-stu-id="eba96-135">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="eba96-136">De webtjenester, der er nødvendige for hver indholdspakke omfatter:</span><span class="sxs-lookup"><span data-stu-id="eba96-136">The web services required for each content pack include:</span></span>

## <a name="role-center-reports"></a><span data-ttu-id="eba96-137">Rollecenter-rapporter</span><span class="sxs-lookup"><span data-stu-id="eba96-137">Role Center Reports</span></span>

<span data-ttu-id="eba96-138">**Microsoft Dynamics 365 Business Central – CRM**</span><span class="sxs-lookup"><span data-stu-id="eba96-138">**Microsoft Dynamics 365 Business Central – CRM**</span></span>
- <span data-ttu-id="eba96-139">Salgsmuligheder</span><span class="sxs-lookup"><span data-stu-id="eba96-139">Sales Opportunities</span></span>
- <span data-ttu-id="eba96-140">Vis virksomhed i Excel-skabelon</span><span class="sxs-lookup"><span data-stu-id="eba96-140">Excel Template View Company</span></span>
- <span data-ttu-id="eba96-141">Power BI-rapportetiketter</span><span class="sxs-lookup"><span data-stu-id="eba96-141">Power BI Report Labels</span></span>

<span data-ttu-id="eba96-142">**Microsoft Dynamics 365 Business Central – Finance**</span><span class="sxs-lookup"><span data-stu-id="eba96-142">**Microsoft Dynamics 365 Business Central – Finance**</span></span>
- <span data-ttu-id="eba96-143">PowerBIFinance</span><span class="sxs-lookup"><span data-stu-id="eba96-143">PowerBIFinance</span></span>
- <span data-ttu-id="eba96-144">Vis virksomhed i Excel-skabelon</span><span class="sxs-lookup"><span data-stu-id="eba96-144">Excel Template View Company</span></span>
- <span data-ttu-id="eba96-145">Power BI-rapportetiketter</span><span class="sxs-lookup"><span data-stu-id="eba96-145">Power BI Report Labels</span></span>

<span data-ttu-id="eba96-146">**Microsoft Dynamics 365 Business Central – Jobs**</span><span class="sxs-lookup"><span data-stu-id="eba96-146">**Microsoft Dynamics 365 Business Central – Jobs**</span></span>
- <span data-ttu-id="eba96-147">Sagsoversigt</span><span class="sxs-lookup"><span data-stu-id="eba96-147">Job List</span></span>
- <span data-ttu-id="eba96-148">Sagsplanlægningslinjer</span><span class="sxs-lookup"><span data-stu-id="eba96-148">Job Planning Lines</span></span>
- <span data-ttu-id="eba96-149">Sagsopgavelinjer</span><span class="sxs-lookup"><span data-stu-id="eba96-149">Job Task Lines</span></span>
- <span data-ttu-id="eba96-150">Power BI-rapportetiketter</span><span class="sxs-lookup"><span data-stu-id="eba96-150">Power BI Report Labels</span></span>
- <span data-ttu-id="eba96-151">Vis virksomhed i Excel-skabelon</span><span class="sxs-lookup"><span data-stu-id="eba96-151">Excel Template View Company</span></span>

<span data-ttu-id="eba96-152">**Microsoft Dynamics 365 Business Central - Sales**</span><span class="sxs-lookup"><span data-stu-id="eba96-152">**Microsoft Dynamics 365 Business Central - Sales**</span></span>
- <span data-ttu-id="eba96-153">Salgsdashboard</span><span class="sxs-lookup"><span data-stu-id="eba96-153">Sales Dashboard</span></span>
- <span data-ttu-id="eba96-154">Vis virksomhed i Excel-skabelon</span><span class="sxs-lookup"><span data-stu-id="eba96-154">Excel Template View Company</span></span>
- <span data-ttu-id="eba96-155">Power BI-rapportetiketter</span><span class="sxs-lookup"><span data-stu-id="eba96-155">Power BI Report Labels</span></span>

## <a name="list-page-reports"></a><span data-ttu-id="eba96-156">Oversigtssiderapporter</span><span class="sxs-lookup"><span data-stu-id="eba96-156">List Page Reports</span></span> 

<span data-ttu-id="eba96-157">**Microsoft Dynamics 365 Business Central – Customers List**</span><span class="sxs-lookup"><span data-stu-id="eba96-157">**Microsoft Dynamics 365 Business Central – Customers List**</span></span>
- <span data-ttu-id="eba96-158">Varestatistik efter kunde</span><span class="sxs-lookup"><span data-stu-id="eba96-158">Item Sales by Customer</span></span>
- <span data-ttu-id="eba96-159">Power BI-varekøbsoversigt</span><span class="sxs-lookup"><span data-stu-id="eba96-159">Power BI Item Purchase List</span></span>
- <span data-ttu-id="eba96-160">Power BI-varesalgsoversigt</span><span class="sxs-lookup"><span data-stu-id="eba96-160">Power BI Item Sales List</span></span>
- <span data-ttu-id="eba96-161">Salgsdashboard</span><span class="sxs-lookup"><span data-stu-id="eba96-161">Sales Dashboard</span></span>
- <span data-ttu-id="eba96-162">Power BI-debitoroversigt</span><span class="sxs-lookup"><span data-stu-id="eba96-162">Power BI Customer List</span></span>
- <span data-ttu-id="eba96-163">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="eba96-163">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="eba96-164">Power BI-rapportetiketter</span><span class="sxs-lookup"><span data-stu-id="eba96-164">Power BI Report Labels</span></span> 

<span data-ttu-id="eba96-165">**Microsoft Dynamics 365 Business Central - General Ledger Entries List**</span><span class="sxs-lookup"><span data-stu-id="eba96-165">**Microsoft Dynamics 365 Business Central - General Ledger Entries List**</span></span>
- <span data-ttu-id="eba96-166">Power BI-finansbeløbsoversigt</span><span class="sxs-lookup"><span data-stu-id="eba96-166">Power BI GL Amount List</span></span>
- <span data-ttu-id="eba96-167">Budgetteret Power BI-finansbeløb</span><span class="sxs-lookup"><span data-stu-id="eba96-167">Power BI GL Budgeted Amount</span></span>
- <span data-ttu-id="eba96-168">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="eba96-168">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="eba96-169">Power BI-rapportetiketter</span><span class="sxs-lookup"><span data-stu-id="eba96-169">Power BI Report Labels</span></span>

<span data-ttu-id="eba96-170">**Microsoft Dynamics 365 Business Central – Items List**</span><span class="sxs-lookup"><span data-stu-id="eba96-170">**Microsoft Dynamics 365 Business Central – Items List**</span></span>
- <span data-ttu-id="eba96-171">Varestatistik efter kunde</span><span class="sxs-lookup"><span data-stu-id="eba96-171">Item Sales by Customer</span></span>
- <span data-ttu-id="eba96-172">Power BI-varekøbsoversigt</span><span class="sxs-lookup"><span data-stu-id="eba96-172">Power BI Item Purchase List</span></span>
- <span data-ttu-id="eba96-173">Power BI-varesalgsoversigt</span><span class="sxs-lookup"><span data-stu-id="eba96-173">Power BI Item Sales List</span></span>
- <span data-ttu-id="eba96-174">Salgsdashboard</span><span class="sxs-lookup"><span data-stu-id="eba96-174">Sales Dashboard</span></span>
- <span data-ttu-id="eba96-175">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="eba96-175">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="eba96-176">Power BI-rapportetiketter</span><span class="sxs-lookup"><span data-stu-id="eba96-176">Power BI Report Labels</span></span>

<span data-ttu-id="eba96-177">**Microsoft Dynamics 365 Business Central – Jobs List**</span><span class="sxs-lookup"><span data-stu-id="eba96-177">**Microsoft Dynamics 365 Business Central – Jobs List**</span></span>
- <span data-ttu-id="eba96-178">Power BI-sagsoversigt</span><span class="sxs-lookup"><span data-stu-id="eba96-178">Power BI Jobs List</span></span>
- <span data-ttu-id="eba96-179">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="eba96-179">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="eba96-180">Power BI-rapportetiketter</span><span class="sxs-lookup"><span data-stu-id="eba96-180">Power BI Report Labels</span></span>

<span data-ttu-id="eba96-181">**Microsoft Dynamics 365 Business Central – Purchase Invoices List**</span><span class="sxs-lookup"><span data-stu-id="eba96-181">**Microsoft Dynamics 365 Business Central – Purchase Invoices List**</span></span>
- <span data-ttu-id="eba96-182">Power BI-købsoversigt</span><span class="sxs-lookup"><span data-stu-id="eba96-182">Power BI Purchase List</span></span>
- <span data-ttu-id="eba96-183">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="eba96-183">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="eba96-184">Power BI-rapportetiketter</span><span class="sxs-lookup"><span data-stu-id="eba96-184">Power BI Report Labels</span></span>

<span data-ttu-id="eba96-185">**Microsoft Dynamics 365 Business Central – Sales Orders List**</span><span class="sxs-lookup"><span data-stu-id="eba96-185">**Microsoft Dynamics 365 Business Central – Sales Orders List**</span></span>
- <span data-ttu-id="eba96-186">Power BI-salgsoversigt</span><span class="sxs-lookup"><span data-stu-id="eba96-186">Power BI Sales List</span></span>
- <span data-ttu-id="eba96-187">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="eba96-187">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="eba96-188">Power BI-rapportetiketter</span><span class="sxs-lookup"><span data-stu-id="eba96-188">Power BI Report Labels</span></span>


<span data-ttu-id="eba96-189">**Microsoft Dynamics 365 Business Central – Vendors List**</span><span class="sxs-lookup"><span data-stu-id="eba96-189">**Microsoft Dynamics 365 Business Central – Vendors List**</span></span>
- <span data-ttu-id="eba96-190">Power BI-varekøbsoversigt</span><span class="sxs-lookup"><span data-stu-id="eba96-190">Power BI Item Purchase List</span></span>
- <span data-ttu-id="eba96-191">Power BI-varesalgsoversigt</span><span class="sxs-lookup"><span data-stu-id="eba96-191">Power BI Item Sales List</span></span>
- <span data-ttu-id="eba96-192">Power BI-kreditoroversigt</span><span class="sxs-lookup"><span data-stu-id="eba96-192">Power BI Vendor List</span></span>
- <span data-ttu-id="eba96-193">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="eba96-193">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="eba96-194">Power BI-rapportetiketter</span><span class="sxs-lookup"><span data-stu-id="eba96-194">Power BI Report Labels</span></span>

## <a name="web-services"></a><span data-ttu-id="eba96-195">Webtjeneste</span><span class="sxs-lookup"><span data-stu-id="eba96-195">Web Services</span></span>
<span data-ttu-id="eba96-196">En nem måde at finde webtjenesterne på er at søge efter webtjenester i [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="eba96-196">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="eba96-197">På listen skal du sørge for at feltet Publicer er markeret for de webtjenester, der er anført ovenfor.</span><span class="sxs-lookup"><span data-stu-id="eba96-197">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="eba96-198">Fejlfinding</span><span class="sxs-lookup"><span data-stu-id="eba96-198">Troubleshooting</span></span>
<span data-ttu-id="eba96-199">Power BI-dashboardet er baseret på de publicerede webtjenester, der er anført ovenfor, og viser data fra demoregnskabet eller dit eget regnskab, hvis du indlæser data fra dit aktuelle økonomisystem.</span><span class="sxs-lookup"><span data-stu-id="eba96-199">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="eba96-200">Men hvis noget går galt indeholder dette afsnit en løsning til de mest almindelige problemer.</span><span class="sxs-lookup"><span data-stu-id="eba96-200">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="eba96-201">Forkert navn på virksomhed</span><span class="sxs-lookup"><span data-stu-id="eba96-201">Incorrect Company Name</span></span>  
<span data-ttu-id="eba96-202">Det er en normal fejl at angive fælles virksomhedens visningsnavn i stedet for navnet på virksomheden.</span><span class="sxs-lookup"><span data-stu-id="eba96-202">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="eba96-203">Du kan finde navnet på virksomheden ved at søge efter **virksomheder**.</span><span class="sxs-lookup"><span data-stu-id="eba96-203">To find the company name search for **Companies**.</span></span> <span data-ttu-id="eba96-204">Brug derefter feltet **Navn**, når du angiver navnet på virksomheden.</span><span class="sxs-lookup"><span data-stu-id="eba96-204">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="eba96-205">Forkert brugernavn og adgangskode</span><span class="sxs-lookup"><span data-stu-id="eba96-205">Incorrect User Name and Password</span></span>  
<span data-ttu-id="eba96-206">Brugernavnet og adgangskoden, der bruges til at oprette forbindelse, skal være de samme, som bruges til at oprette forbindelse til din Microsoft Office 365-konto.</span><span class="sxs-lookup"><span data-stu-id="eba96-206">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="eba96-207">Indholdspakkerne kræver også, at du har en Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto.</span><span class="sxs-lookup"><span data-stu-id="eba96-207">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="eba96-208">Når du har indtastet dine legitimationsoplysninger, får du automatisk vist alle Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-lejere, du har adgang til.</span><span class="sxs-lookup"><span data-stu-id="eba96-208">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="eba96-209">Hvis du ikke har en licenseret eller prøveversion af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto, får du vist en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="eba96-209">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="eba96-210">Nøglen svarer ikke nogen rækker i tabellen</span><span class="sxs-lookup"><span data-stu-id="eba96-210">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="eba96-211">Hvis du angiver et ikke gyldigt firmanavn under oprettelsen af forbindelsen, kan du få vist meddelelsen "Nøglen svarer ikke nogen rækker i tabellen".</span><span class="sxs-lookup"><span data-stu-id="eba96-211">If you enter a non-valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="eba96-212">Angiv det korrekte firmanavn, og forsøg igen.</span><span class="sxs-lookup"><span data-stu-id="eba96-212">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="eba96-213">Se også</span><span class="sxs-lookup"><span data-stu-id="eba96-213">See Also</span></span>
[<span data-ttu-id="eba96-214">Kom i gang med Power BI</span><span class="sxs-lookup"><span data-stu-id="eba96-214">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[<span data-ttu-id="eba96-215">Power BI- grundlæggende begreber</span><span class="sxs-lookup"><span data-stu-id="eba96-215">Power BI - Basic Concepts</span></span>](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)  
[<span data-ttu-id="eba96-216">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="eba96-216">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="eba96-217">Introduktion</span><span class="sxs-lookup"><span data-stu-id="eba96-217">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="eba96-218">Importere virksomhedsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="eba96-218">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="eba96-219">[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="eba96-219">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="eba96-220">Finans</span><span class="sxs-lookup"><span data-stu-id="eba96-220">Finance</span></span>](finance.md)  
<span data-ttu-id="eba96-221">[Opsætning af rapportering for [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="eba96-221">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  
