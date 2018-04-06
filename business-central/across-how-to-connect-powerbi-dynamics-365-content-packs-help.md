---
title: "Sådan forbindes Power BI med Business Central | Microsoft Docs"
description: "Du kan nemt få indsigt, business intelligence og nøgletal i dine Business Central-data med Power BI og Business Central-indholdspakker."
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 03/16/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 315d4b188cdd834e82676a0c5ef77272ad873eb7
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="connecting-power-bi-to-business-central-content-packs"></a><span data-ttu-id="cf374-103">Forbinde Power BI med Business Central-indholdspakker</span><span class="sxs-lookup"><span data-stu-id="cf374-103">Connecting Power BI to Business Central Content Packs</span></span>
<span data-ttu-id="cf374-104">Du kan nemt få indsigt i dine Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data med Power BI og Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-indholdspakker.</span><span class="sxs-lookup"><span data-stu-id="cf374-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="cf374-105">Power BI henter dine data og opretter derefter et out-of-the-box dashboard og rapporter baseret på dataene.</span><span class="sxs-lookup"><span data-stu-id="cf374-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

> [!NOTE]  
>  <span data-ttu-id="cf374-106">Du skal have en gyldig konto til [!INCLUDE[d365fin](includes/d365fin_md.md)] og til Power BI.</span><span class="sxs-lookup"><span data-stu-id="cf374-106">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Power BI.</span></span> <span data-ttu-id="cf374-107">Desuden skal du hente [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span><span class="sxs-lookup"><span data-stu-id="cf374-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span></span>  
>  <span data-ttu-id="cf374-108">Power BI-indholdspakker kræver tilladelser til de tabeller, hvor data hentes fra.</span><span class="sxs-lookup"><span data-stu-id="cf374-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="cf374-109">Yderligere oplysninger om kravene beskrives nedenfor.</span><span class="sxs-lookup"><span data-stu-id="cf374-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="cf374-110">Sådan oprettes forbindelse</span><span class="sxs-lookup"><span data-stu-id="cf374-110">How to Connect</span></span>
1. <span data-ttu-id="cf374-111">Vælg **Hent data** nederst i venstre navigationsrude.</span><span class="sxs-lookup"><span data-stu-id="cf374-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="cf374-112">![Navigere til Hent data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="cf374-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>
2. <span data-ttu-id="cf374-113">I feltet **Tjenester** skal du vælge **Hent**.</span><span class="sxs-lookup"><span data-stu-id="cf374-113">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="cf374-114">Dermed åbnes et vindue med **AppSource** og **Apps til Power BI-apps**.</span><span class="sxs-lookup"><span data-stu-id="cf374-114">This will open a window with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="cf374-115">![Vælg indholdspakker fra onlinetjenester](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="cf374-115">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="cf374-116">Vælg **Apps** under fanen **Apps til Power BI-apps**, og vælg den **Microsoft Dynamics 365 Business Central**-indholdspakke, du vil bruge, og vælg derefter **Hent nu**.</span><span class="sxs-lookup"><span data-stu-id="cf374-116">Select **Apps** from the **Apps for Power BI apps** tab, and choose the **Microsoft Dynamics 365 Business Central** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="cf374-117">![Vælg Dynamics 365 Business Central, og vælg Hent det nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="cf374-117">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="cf374-118">Når du bliver bedt om det, skal du angive navnet på *virksomheden* i [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="cf374-118">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="cf374-119">Dette er ikke det viste navn.</span><span class="sxs-lookup"><span data-stu-id="cf374-119">This is not the display name.</span></span>  
<span data-ttu-id="cf374-120">![Vælg Dynamics 365 Business Central, og vælg Hent det nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="cf374-120">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="cf374-121">Når der er oprettet forbindelse, indlæses et dashboard, en rapport og et datasæt automatisk i dit Power BI-arbejdsområde.</span><span class="sxs-lookup"><span data-stu-id="cf374-121">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="cf374-122">Når dette er fuldført, opdateres felterne med data fra din konto.</span><span class="sxs-lookup"><span data-stu-id="cf374-122">When completed, the tiles will update with data from your account.</span></span>
<span data-ttu-id="cf374-123">![Vælg Dynamics 365 Business Central, og vælg Hent det nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="cf374-123">![Select Dynamics 365 Business Central  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="cf374-124">Hvad nu?</span><span class="sxs-lookup"><span data-stu-id="cf374-124">What Now?</span></span>

- <span data-ttu-id="cf374-125">[Ændre felterne](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) i dashboardet.</span><span class="sxs-lookup"><span data-stu-id="cf374-125">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="cf374-126">[Vælg et felt](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) for at åbne den underliggende rapport.</span><span class="sxs-lookup"><span data-stu-id="cf374-126">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="cf374-127">Selv om dit datasæt planlægges til at blive opdateret dagligt, kan du ændre tidsplanen for opdatering eller prøve at opdatere det på behov ved hjælp af **Opdater nu**.</span><span class="sxs-lookup"><span data-stu-id="cf374-127">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="cf374-128">Systemkrav</span><span class="sxs-lookup"><span data-stu-id="cf374-128">System Requirements</span></span>
<span data-ttu-id="cf374-129">Hvis du vil importere dine [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data i Power BI, skal du have rettigheder til de webtjenester, der bruges til at hente data.</span><span class="sxs-lookup"><span data-stu-id="cf374-129">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="cf374-130">De webtjenester, der er nødvendige for hver indholdspakke omfatter:</span><span class="sxs-lookup"><span data-stu-id="cf374-130">The web services required for each content pack include:</span></span>

<span data-ttu-id="cf374-131">**Microsoft Dynamics 365 Business Central – CRM**</span><span class="sxs-lookup"><span data-stu-id="cf374-131">**Microsoft Dynamics 365 Business Central – CRM**</span></span>
- <span data-ttu-id="cf374-132">SalesOpportunities</span><span class="sxs-lookup"><span data-stu-id="cf374-132">SalesOpportunities</span></span>
- <span data-ttu-id="cf374-133">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="cf374-133">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="cf374-134">**Microsoft Dynamics 365 Business Central – Sales**</span><span class="sxs-lookup"><span data-stu-id="cf374-134">**Microsoft Dynamics 365 Business Central – Sales**</span></span>
- <span data-ttu-id="cf374-135">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="cf374-135">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="cf374-136">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="cf374-136">SalesDashboard</span></span>
- <span data-ttu-id="cf374-137">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="cf374-137">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="cf374-138">**Microsoft Dynamics 365 Business Central – Finance**</span><span class="sxs-lookup"><span data-stu-id="cf374-138">**Microsoft Dynamics 365 Business Central – Finance**</span></span>
- <span data-ttu-id="cf374-139">PowerBIFinance</span><span class="sxs-lookup"><span data-stu-id="cf374-139">PowerBIFinance</span></span>
- <span data-ttu-id="cf374-140">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="cf374-140">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="cf374-141">**Microsoft Dynamics 365 Business Central – Jobs**</span><span class="sxs-lookup"><span data-stu-id="cf374-141">**Microsoft Dynamics 365 Business Central – Jobs**</span></span>
- <span data-ttu-id="cf374-142">Sagsoversigt</span><span class="sxs-lookup"><span data-stu-id="cf374-142">Job List</span></span>
- <span data-ttu-id="cf374-143">Sagsplanlægningslinjer</span><span class="sxs-lookup"><span data-stu-id="cf374-143">Job Planning Lines</span></span>
- <span data-ttu-id="cf374-144">Sagsopgavelinjer</span><span class="sxs-lookup"><span data-stu-id="cf374-144">Job Task Lines</span></span>

<span data-ttu-id="cf374-145">**Microsoft Dynamics 365 Business Central – Debitorliste**</span><span class="sxs-lookup"><span data-stu-id="cf374-145">**Microsoft Dynamics 365 Business Central – Customers List**</span></span>
- <span data-ttu-id="cf374-146">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="cf374-146">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="cf374-147">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="cf374-147">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="cf374-148">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="cf374-148">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="cf374-149">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="cf374-149">SalesDashboard</span></span>
- <span data-ttu-id="cf374-150">Power BI-debitorliste</span><span class="sxs-lookup"><span data-stu-id="cf374-150">Power_BI_Customer_List</span></span>
- <span data-ttu-id="cf374-151">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="cf374-151">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="cf374-152">**Microsoft Dynamics 365 Business Central – Vareliste**</span><span class="sxs-lookup"><span data-stu-id="cf374-152">**Microsoft Dynamics 365 Business Central – Items List**</span></span>
- <span data-ttu-id="cf374-153">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="cf374-153">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="cf374-154">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="cf374-154">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="cf374-155">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="cf374-155">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="cf374-156">Varer</span><span class="sxs-lookup"><span data-stu-id="cf374-156">Items</span></span>
- <span data-ttu-id="cf374-157">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="cf374-157">SalesDashboard</span></span>
- <span data-ttu-id="cf374-158">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="cf374-158">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="cf374-159">**Microsoft Dynamics 365 Business Central – Kreditorliste**</span><span class="sxs-lookup"><span data-stu-id="cf374-159">**Microsoft Dynamics 365 Business Central – Vendors List**</span></span>
- <span data-ttu-id="cf374-160">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="cf374-160">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="cf374-161">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="cf374-161">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="cf374-162">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="cf374-162">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="cf374-163">Varer</span><span class="sxs-lookup"><span data-stu-id="cf374-163">Items</span></span>
- <span data-ttu-id="cf374-164">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="cf374-164">SalesDashboard</span></span>
- <span data-ttu-id="cf374-165">Power BI-debitorliste</span><span class="sxs-lookup"><span data-stu-id="cf374-165">Power_BI_Customer_List</span></span>
- <span data-ttu-id="cf374-166">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="cf374-166">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="cf374-167">Power_BI_Vendor_List</span><span class="sxs-lookup"><span data-stu-id="cf374-167">Power_BI_Vendor_List</span></span>
- <span data-ttu-id="cf374-168">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="cf374-168">ExcelTemplateViewCompany</span></span>

## <a name="web-services"></a><span data-ttu-id="cf374-169">Webtjeneste</span><span class="sxs-lookup"><span data-stu-id="cf374-169">Web Services</span></span>
<span data-ttu-id="cf374-170">En nem måde at finde webtjenesterne på er at søge efter webtjenester i [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="cf374-170">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="cf374-171">På listen skal du sørge for at feltet Publicer er markeret for de webtjenester, der er anført ovenfor.</span><span class="sxs-lookup"><span data-stu-id="cf374-171">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="cf374-172">Fejlfinding</span><span class="sxs-lookup"><span data-stu-id="cf374-172">Troubleshooting</span></span>
<span data-ttu-id="cf374-173">Power BI-dashboardet er baseret på de publicerede webtjenester, der er anført ovenfor, og viser data fra demonstrationsvirksomheden eller din egen virksomhed, hvis du indlæser data fra dit aktuelle økonomisystem.</span><span class="sxs-lookup"><span data-stu-id="cf374-173">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="cf374-174">Men hvis noget går galt indeholder dette afsnit en løsning til de mest almindelige problemer.</span><span class="sxs-lookup"><span data-stu-id="cf374-174">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="cf374-175">Forkert navn på virksomhed</span><span class="sxs-lookup"><span data-stu-id="cf374-175">Incorrect Company Name</span></span>  
<span data-ttu-id="cf374-176">Det er en normal fejl at angive fælles virksomhedens visningsnavn i stedet for navnet på virksomheden.</span><span class="sxs-lookup"><span data-stu-id="cf374-176">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="cf374-177">Du kan finde navnet på virksomheden ved at søge efter **virksomheder**.</span><span class="sxs-lookup"><span data-stu-id="cf374-177">To find the company name search for **Companies**.</span></span> <span data-ttu-id="cf374-178">Brug derefter feltet **Navn**, når du angiver navnet på virksomheden.</span><span class="sxs-lookup"><span data-stu-id="cf374-178">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="cf374-179">Forkert brugernavn og adgangskode</span><span class="sxs-lookup"><span data-stu-id="cf374-179">Incorrect User Name and Password</span></span>  
<span data-ttu-id="cf374-180">Brugernavnet og adgangskoden, der bruges til at oprette forbindelse, skal være de samme, som bruges til at oprette forbindelse til din Microsoft Office 365-konto.</span><span class="sxs-lookup"><span data-stu-id="cf374-180">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="cf374-181">Indholdspakkerne kræver også, at du har en Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto.</span><span class="sxs-lookup"><span data-stu-id="cf374-181">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="cf374-182">Når du har indtastet dine legitimationsoplysninger, får du automatisk vist alle Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-lejere, du har adgang til.</span><span class="sxs-lookup"><span data-stu-id="cf374-182">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="cf374-183">Hvis du ikke har en licenseret eller prøveversion af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto, får du vist en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="cf374-183">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="cf374-184">Nøglen svarer ikke nogen rækker i tabellen</span><span class="sxs-lookup"><span data-stu-id="cf374-184">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="cf374-185">Hvis du angiver et ikke gyldigt firmanavn under oprettelsen af forbindelsen, kan du få vist meddelelsen "Nøglen svarer ikke nogen rækker i tabellen".</span><span class="sxs-lookup"><span data-stu-id="cf374-185">If you enter a non valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="cf374-186">Angiv det korrekte firmanavn, og forsøg igen.</span><span class="sxs-lookup"><span data-stu-id="cf374-186">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="cf374-187">Se også</span><span class="sxs-lookup"><span data-stu-id="cf374-187">See Also</span></span>
[<span data-ttu-id="cf374-188">Kom i gang med Power BI</span><span class="sxs-lookup"><span data-stu-id="cf374-188">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
<span data-ttu-id="cf374-189">[Power BI - grundlæggende begreber](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
["Business Intelligence"](bi.md)</span><span class="sxs-lookup"><span data-stu-id="cf374-189">[Power BI - Basic Concepts](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Business Intelligence](bi.md)</span></span>  
<span data-ttu-id="cf374-190">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="cf374-190">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="cf374-191">Importere virksomhedsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="cf374-191">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="cf374-192">[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="cf374-192">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="cf374-193">Finans</span><span class="sxs-lookup"><span data-stu-id="cf374-193">Finance</span></span>](finance.md)  
<span data-ttu-id="cf374-194">[Opsætning af rapportering for [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="cf374-194">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  

