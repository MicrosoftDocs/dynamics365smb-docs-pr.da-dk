---
title: "Sådan forbindes Power BI til Finance and Operations, Business edition | Microsoft Docs"
description: "Det er let at få indsigt, business intelligence og nøgletal fra dine data i Finance and Operations, Business edition med Power BI og indholdspakkerne til Finance and Operations, Business edition."
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 02/05/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: b4e2e7bc1c2622d329c73ae5bf47b4accff10aa8
ms.openlocfilehash: aff8d95b13f795fa12d3146e5613712fb3baf9b4
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="connecting-power-bi-to-finance-and-operations-business-edition-content-packs"></a><span data-ttu-id="fe150-103">Forbinde Power BI med indholdspakker i Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="fe150-103">Connecting Power BI to Finance and Operations, Business edition Content Packs</span></span>
<span data-ttu-id="fe150-104">Du kan nemt få indsigt i dine Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data med Power BI og Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-indholdspakker.</span><span class="sxs-lookup"><span data-stu-id="fe150-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="fe150-105">Power BI henter dine data og opretter derefter et out-of-the-box dashboard og rapporter baseret på dataene.</span><span class="sxs-lookup"><span data-stu-id="fe150-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

> [!NOTE]  
>  <span data-ttu-id="fe150-106">Du skal have en gyldig konto til Dynamics 365 og til Power BI.</span><span class="sxs-lookup"><span data-stu-id="fe150-106">You must have a valid account with Dynamics 365 and with Power BI.</span></span> <span data-ttu-id="fe150-107">Desuden skal du hente [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span><span class="sxs-lookup"><span data-stu-id="fe150-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span></span>  
>  <span data-ttu-id="fe150-108">Power BI-indholdspakker kræver tilladelser til de tabeller, hvor data hentes fra.</span><span class="sxs-lookup"><span data-stu-id="fe150-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="fe150-109">Yderligere oplysninger om kravene beskrives nedenfor.</span><span class="sxs-lookup"><span data-stu-id="fe150-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="fe150-110">Sådan oprettes forbindelse</span><span class="sxs-lookup"><span data-stu-id="fe150-110">How to Connect</span></span>
1. <span data-ttu-id="fe150-111">Vælg **Hent data** nederst i venstre navigationsrude.</span><span class="sxs-lookup"><span data-stu-id="fe150-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="fe150-112">![Navigere til Hent data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="fe150-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>
2. <span data-ttu-id="fe150-113">I feltet **Tjenester** skal du vælge **Hent**.</span><span class="sxs-lookup"><span data-stu-id="fe150-113">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="fe150-114">Dermed åbnes et vindue med **AppSource** og **Apps til Power BI-apps**.</span><span class="sxs-lookup"><span data-stu-id="fe150-114">This will open a window with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="fe150-115">![Vælg indholdspakker fra onlinetjenester](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="fe150-115">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="fe150-116">Vælg **Apps** under fanen **Apps til Power BI-apps**, og vælg den **Microsoft Dynamics 365 for Finance and Operations**-indholdspakke, du vil bruge, og vælg derefter **Hent nu**.</span><span class="sxs-lookup"><span data-stu-id="fe150-116">Select **Apps** from the **Apps for Power BI apps** tab, and choose the **Microsoft Dynamics 365 for Finance and Operations** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="fe150-117">![Vælg Dynamics 365 for Finance and Operations, Business edition, og vælg Hent nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="fe150-117">![Select Dynamics 365 for Finance and Operations, Business edition and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="fe150-118">Når du bliver bedt om det, skal du angive navnet på *virksomheden* i [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fe150-118">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="fe150-119">Dette er ikke det viste navn.</span><span class="sxs-lookup"><span data-stu-id="fe150-119">This is not the display name.</span></span>  
<span data-ttu-id="fe150-120">![Vælg Dynamics 365 for Finance and Operations, Business edition, og vælg Hent nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="fe150-120">![Select Dynamics 365 for Finance and Operations, Business edition and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="fe150-121">Når der er oprettet forbindelse, indlæses et dashboard, en rapport og et datasæt automatisk i dit Power BI-arbejdsområde.</span><span class="sxs-lookup"><span data-stu-id="fe150-121">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="fe150-122">Når dette er fuldført, opdateres felterne med data fra din konto.</span><span class="sxs-lookup"><span data-stu-id="fe150-122">When completed, the tiles will update with data from your account.</span></span>
<span data-ttu-id="fe150-123">![Vælg Dynamics 365 for Finance and Operations, Business edition, og vælg Hent nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="fe150-123">![Select Dynamics 365 for Finance and Operations, Business edition  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="fe150-124">Hvad nu?</span><span class="sxs-lookup"><span data-stu-id="fe150-124">What Now?</span></span>

- <span data-ttu-id="fe150-125">Prøv [at stille et spørgsmål i feltet Spørgsmål og svar](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) øverst i dashboardet.</span><span class="sxs-lookup"><span data-stu-id="fe150-125">Try [asking a question in the Q&A box](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) at the top of the dashboard.</span></span>  
- <span data-ttu-id="fe150-126">[Ændre felterne](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) i dashboardet.</span><span class="sxs-lookup"><span data-stu-id="fe150-126">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="fe150-127">[Vælg et felt](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) for at åbne den underliggende rapport.</span><span class="sxs-lookup"><span data-stu-id="fe150-127">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="fe150-128">Selv om dit datasæt planlægges til at blive opdateret dagligt, kan du ændre tidsplanen for opdatering eller prøve at opdatere det på behov ved hjælp af **Opdater nu**.</span><span class="sxs-lookup"><span data-stu-id="fe150-128">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="fe150-129">Systemkrav</span><span class="sxs-lookup"><span data-stu-id="fe150-129">System Requirements</span></span>
<span data-ttu-id="fe150-130">Hvis du vil importere dine [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data i Power BI, skal du have rettigheder til de webtjenester, der bruges til at hente data.</span><span class="sxs-lookup"><span data-stu-id="fe150-130">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="fe150-131">De webtjenester, der er nødvendige for hver indholdspakke omfatter:</span><span class="sxs-lookup"><span data-stu-id="fe150-131">The web services required for each content pack include:</span></span>

<span data-ttu-id="fe150-132">**Microsoft Dynamics 365 for Finance and Operations, Business edition – CRM**</span><span class="sxs-lookup"><span data-stu-id="fe150-132">**Microsoft Dynamics 365 for Finance and Operations, Business edition – CRM**</span></span>
- <span data-ttu-id="fe150-133">SalesOpportunities</span><span class="sxs-lookup"><span data-stu-id="fe150-133">SalesOpportunities</span></span>
- <span data-ttu-id="fe150-134">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="fe150-134">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="fe150-135">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Sales**</span><span class="sxs-lookup"><span data-stu-id="fe150-135">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Sales**</span></span>
- <span data-ttu-id="fe150-136">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="fe150-136">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="fe150-137">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="fe150-137">SalesDashboard</span></span>
- <span data-ttu-id="fe150-138">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="fe150-138">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="fe150-139">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Finance**</span><span class="sxs-lookup"><span data-stu-id="fe150-139">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Finance**</span></span>
- <span data-ttu-id="fe150-140">PowerBIFinance</span><span class="sxs-lookup"><span data-stu-id="fe150-140">PowerBIFinance</span></span>
- <span data-ttu-id="fe150-141">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="fe150-141">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="fe150-142">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Jobs**</span><span class="sxs-lookup"><span data-stu-id="fe150-142">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Jobs**</span></span>
- <span data-ttu-id="fe150-143">Sagsoversigt</span><span class="sxs-lookup"><span data-stu-id="fe150-143">Job List</span></span>
- <span data-ttu-id="fe150-144">Sagsplanlægningslinjer</span><span class="sxs-lookup"><span data-stu-id="fe150-144">Job Planning Lines</span></span>
- <span data-ttu-id="fe150-145">Sagsopgavelinjer</span><span class="sxs-lookup"><span data-stu-id="fe150-145">Job Task Lines</span></span>

<span data-ttu-id="fe150-146">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Debitorliste**</span><span class="sxs-lookup"><span data-stu-id="fe150-146">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Customers List**</span></span>
- <span data-ttu-id="fe150-147">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="fe150-147">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="fe150-148">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="fe150-148">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="fe150-149">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="fe150-149">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="fe150-150">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="fe150-150">SalesDashboard</span></span>
- <span data-ttu-id="fe150-151">Power BI-debitorliste</span><span class="sxs-lookup"><span data-stu-id="fe150-151">Power_BI_Customer_List</span></span>
- <span data-ttu-id="fe150-152">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="fe150-152">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="fe150-153">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Vareliste**</span><span class="sxs-lookup"><span data-stu-id="fe150-153">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Items List**</span></span>
- <span data-ttu-id="fe150-154">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="fe150-154">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="fe150-155">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="fe150-155">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="fe150-156">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="fe150-156">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="fe150-157">Varer</span><span class="sxs-lookup"><span data-stu-id="fe150-157">Items</span></span>
- <span data-ttu-id="fe150-158">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="fe150-158">SalesDashboard</span></span>
- <span data-ttu-id="fe150-159">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="fe150-159">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="fe150-160">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Kreditorliste**</span><span class="sxs-lookup"><span data-stu-id="fe150-160">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Vendors List**</span></span>
- <span data-ttu-id="fe150-161">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="fe150-161">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="fe150-162">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="fe150-162">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="fe150-163">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="fe150-163">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="fe150-164">Varer</span><span class="sxs-lookup"><span data-stu-id="fe150-164">Items</span></span>
- <span data-ttu-id="fe150-165">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="fe150-165">SalesDashboard</span></span>
- <span data-ttu-id="fe150-166">Power BI-debitorliste</span><span class="sxs-lookup"><span data-stu-id="fe150-166">Power_BI_Customer_List</span></span>
- <span data-ttu-id="fe150-167">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="fe150-167">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="fe150-168">Power_BI_Vendor_List</span><span class="sxs-lookup"><span data-stu-id="fe150-168">Power_BI_Vendor_List</span></span>
- <span data-ttu-id="fe150-169">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="fe150-169">ExcelTemplateViewCompany</span></span>

## <a name="web-services"></a><span data-ttu-id="fe150-170">Webtjeneste</span><span class="sxs-lookup"><span data-stu-id="fe150-170">Web Services</span></span>
<span data-ttu-id="fe150-171">En nem måde at finde webtjenesterne på er at søge efter webtjenester i [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fe150-171">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="fe150-172">På listen skal du sørge for at feltet Publicer er markeret for de webtjenester, der er anført ovenfor.</span><span class="sxs-lookup"><span data-stu-id="fe150-172">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="fe150-173">Fejlfinding</span><span class="sxs-lookup"><span data-stu-id="fe150-173">Troubleshooting</span></span>
<span data-ttu-id="fe150-174">Power BI-dashboardet er baseret på de publicerede webtjenester, der er anført ovenfor, og viser data fra demonstrationsvirksomheden eller din egen virksomhed, hvis du indlæser data fra dit aktuelle økonomisystem.</span><span class="sxs-lookup"><span data-stu-id="fe150-174">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="fe150-175">Men hvis noget går galt indeholder dette afsnit en løsning til de mest almindelige problemer.</span><span class="sxs-lookup"><span data-stu-id="fe150-175">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="fe150-176">Forkert navn på virksomhed</span><span class="sxs-lookup"><span data-stu-id="fe150-176">Incorrect Company Name</span></span>  
<span data-ttu-id="fe150-177">Det er en normal fejl at angive fælles virksomhedens visningsnavn i stedet for navnet på virksomheden.</span><span class="sxs-lookup"><span data-stu-id="fe150-177">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="fe150-178">Du kan finde navnet på virksomheden ved at søge efter **virksomheder**.</span><span class="sxs-lookup"><span data-stu-id="fe150-178">To find the company name search for **Companies**.</span></span> <span data-ttu-id="fe150-179">Brug derefter feltet **Navn**, når du angiver navnet på virksomheden.</span><span class="sxs-lookup"><span data-stu-id="fe150-179">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="fe150-180">Forkert brugernavn og adgangskode</span><span class="sxs-lookup"><span data-stu-id="fe150-180">Incorrect User Name and Password</span></span>  
<span data-ttu-id="fe150-181">Brugernavnet og adgangskoden, der bruges til at oprette forbindelse, skal være de samme, som bruges til at oprette forbindelse til din Microsoft Office 365-konto.</span><span class="sxs-lookup"><span data-stu-id="fe150-181">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="fe150-182">Indholdspakkerne kræver også, at du har en Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto.</span><span class="sxs-lookup"><span data-stu-id="fe150-182">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="fe150-183">Når du har indtastet dine legitimationsoplysninger, får du automatisk vist alle Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-lejere, du har adgang til.</span><span class="sxs-lookup"><span data-stu-id="fe150-183">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="fe150-184">Hvis du ikke har en licenseret eller prøveversion af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto, får du vist en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="fe150-184">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="fe150-185">Nøglen svarer ikke nogen rækker i tabellen</span><span class="sxs-lookup"><span data-stu-id="fe150-185">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="fe150-186">Hvis du angiver et ikke gyldigt firmanavn under oprettelsen af forbindelsen, kan du få vist meddelelsen "Nøglen svarer ikke nogen rækker i tabellen".</span><span class="sxs-lookup"><span data-stu-id="fe150-186">If you enter a non valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="fe150-187">Angiv det korrekte firmanavn, og forsøg igen.</span><span class="sxs-lookup"><span data-stu-id="fe150-187">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="fe150-188">Se også</span><span class="sxs-lookup"><span data-stu-id="fe150-188">See Also</span></span>
[<span data-ttu-id="fe150-189">Kom i gang med Power BI</span><span class="sxs-lookup"><span data-stu-id="fe150-189">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
<span data-ttu-id="fe150-190">[Power BI - grundlæggende begreber](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
["Business Intelligence"](bi.md)</span><span class="sxs-lookup"><span data-stu-id="fe150-190">[Power BI - Basic Concepts](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Business Intelligence](bi.md)</span></span>  
<span data-ttu-id="fe150-191">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="fe150-191">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="fe150-192">Importere virksomhedsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="fe150-192">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="fe150-193">[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="fe150-193">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="fe150-194">Finans</span><span class="sxs-lookup"><span data-stu-id="fe150-194">Finance</span></span>](finance.md)  
<span data-ttu-id="fe150-195">[Opsætning af rapportering for [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="fe150-195">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  

