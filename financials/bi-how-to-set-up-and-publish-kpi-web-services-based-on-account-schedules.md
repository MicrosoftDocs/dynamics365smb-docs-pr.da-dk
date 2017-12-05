---
title: "Fremgangsmåde: Konfigurere og publicere KPI-webtjenester, der er baseret på kontoskemaer | Microsoft Docs"
description: "I vinduet **Konfiguration af webtjenesten Kontoskema, KPI** skal du angive, hvordan kontoskema-KPI-dataene skal vises, og hvilke specifikke kontoskemaer KPI'erne skal baseres på."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0f2f91a9813b07b0868043a4a2a3ed0b3f838536
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules"></a><span data-ttu-id="8a93b-103">Fremgangsmåde: Konfigurere og publicere KPI-webtjenester, der er baseret på kontoskemaer</span><span class="sxs-lookup"><span data-stu-id="8a93b-103">How to: Set Up and Publish KPI Web Services Based on Account Schedules</span></span>
<span data-ttu-id="8a93b-104">I vinduet **Konfiguration af webtjenesten Kontoskema, KPI** skal du angive, hvordan kontoskema-KPI-dataene skal vises, og hvilke specifikke kontoskemaer KPI'erne skal baseres på.</span><span class="sxs-lookup"><span data-stu-id="8a93b-104">In the **Account Schedule KPI Web Service Setup** window, you set up how to show the account-schedule KPI data and which specific account schedules to base the KPIs on.</span></span> <span data-ttu-id="8a93b-105">Når du vælger knappen **Publicer webtjeneste**, føjes de angivne kontoskema-KPI-data til listen over publicerede webtjenester i vinduet **Webtjenester**.</span><span class="sxs-lookup"><span data-stu-id="8a93b-105">When you choose the **Publish Web Service** button, the specified account-schedule KPI data is added to the list of published web services in the **Web Services** window.</span></span>  

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a><span data-ttu-id="8a93b-106">Sådan konfigureres og publiceres en KPI-webtjeneste, der er baseret på kontoskemaer</span><span class="sxs-lookup"><span data-stu-id="8a93b-106">To set up and publish a KPI web service that is based on account schedules</span></span>  

1.  <span data-ttu-id="8a93b-107">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Konfiguration af webtjenesten Kontoskema, KPI**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="8a93b-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedule KPI Web Service Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="8a93b-108">På oversigtspanelet **Generelt** skal du udfylde felterne som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="8a93b-108">On the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="8a93b-109">Felt</span><span class="sxs-lookup"><span data-stu-id="8a93b-109">Field</span></span>|<span data-ttu-id="8a93b-110">Description</span><span class="sxs-lookup"><span data-stu-id="8a93b-110">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="8a93b-111">**Start på prognosticerede værdier**</span><span class="sxs-lookup"><span data-stu-id="8a93b-111">**Forecasted Values Start**</span></span>|<span data-ttu-id="8a93b-112">Angiv, hvornår prognosticerede værdier vises på den grafiske visning af kontoskema-KPI'en.</span><span class="sxs-lookup"><span data-stu-id="8a93b-112">Specify at what point in time forecasted values are shown on the account-schedule KPI graphic.</span></span><br /><br /> <span data-ttu-id="8a93b-113">De prognosticerede værdier hentes fra finansbudgetposter, som du vælger i feltet **Finansbudgetnavn**.</span><span class="sxs-lookup"><span data-stu-id="8a93b-113">The forecasted values are retrieved from the general ledger budget that you select in the **G/L Budget Name** field.</span></span> <span data-ttu-id="8a93b-114">**Bemærk:** Hvis du ønsker at få KPI'er, der viser prognosticerede tal efter en bestemt dato og faktiske tal før datoen, kan du ændre feltet **Bogf. tilladt fra** i vinduet **Opsætning af Finans**.</span><span class="sxs-lookup"><span data-stu-id="8a93b-114">**Note:**  To obtain KPIs that show forecasted figures after a certain date and actual figures before the date, you can change the **Allow Posting From** field in the **General Ledger Setup** window.</span></span> <span data-ttu-id="8a93b-115">Du kan finde flere oplysninger i Bogf. tilladt fra.</span><span class="sxs-lookup"><span data-stu-id="8a93b-115">For more information, see Allow Posting From.</span></span>|  
    |<span data-ttu-id="8a93b-116">**Finansbudgetnavn**</span><span class="sxs-lookup"><span data-stu-id="8a93b-116">**G/L Budget Name**</span></span>|<span data-ttu-id="8a93b-117">Angiv navnet på det finansbudget, der indeholder budgetterede værdier til kontoskema-KPI-webtjenesten.</span><span class="sxs-lookup"><span data-stu-id="8a93b-117">Specify the name of the general ledger budget that provides forecasted values to the account-schedule KPI web service.</span></span>|  
    |<span data-ttu-id="8a93b-118">**Periode**</span><span class="sxs-lookup"><span data-stu-id="8a93b-118">**Period**</span></span>|<span data-ttu-id="8a93b-119">Angiv den periode, som kontoskema-KPI-webtjenesten er baseret på.</span><span class="sxs-lookup"><span data-stu-id="8a93b-119">Specify the period that the account-schedule KPI web service is based on.</span></span>|  
    |<span data-ttu-id="8a93b-120">**Vis efter**</span><span class="sxs-lookup"><span data-stu-id="8a93b-120">**View By**</span></span>|<span data-ttu-id="8a93b-121">Angiv, hvilket tidsinterval kontoskema-KPI'en vises i.</span><span class="sxs-lookup"><span data-stu-id="8a93b-121">Specify which time interval the account-schedule KPI is shown in.</span></span>|  
    |<span data-ttu-id="8a93b-122">**Navn på webtjeneste**</span><span class="sxs-lookup"><span data-stu-id="8a93b-122">**Web Service Name**</span></span>|<span data-ttu-id="8a93b-123">Angiv navnet på kontoskema-KPI-webtjenesten.</span><span class="sxs-lookup"><span data-stu-id="8a93b-123">Specify the name of the account-schedule KPI web service.</span></span><br /><br /> <span data-ttu-id="8a93b-124">Dette navn vises i feltet **Servicenavn** i vinduet **Webtjeneste**.</span><span class="sxs-lookup"><span data-stu-id="8a93b-124">This name will appear in the **Service Name** field in the **Web Services** window.</span></span>|  

    <span data-ttu-id="8a93b-125">Fortsæt med at angive et eller flere kontoskemaer, som du vil publicere som en KPI-webtjeneste i henhold til opsætningen, som du foretog i tabellen ovenfor.</span><span class="sxs-lookup"><span data-stu-id="8a93b-125">Proceed to specify one or more account schedules that you want to publish as a KPI web service according to the setup that you made in the previous table.</span></span>  

3.  <span data-ttu-id="8a93b-126">På oversigtspanelet **Kontoskemaer** skal du udfylde felterne som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="8a93b-126">On the **Account Schedules** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="8a93b-127">Felt</span><span class="sxs-lookup"><span data-stu-id="8a93b-127">Field</span></span>|<span data-ttu-id="8a93b-128">Description</span><span class="sxs-lookup"><span data-stu-id="8a93b-128">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="8a93b-129">**Kontoskemanavn**</span><span class="sxs-lookup"><span data-stu-id="8a93b-129">**Acc. Schedule Name**</span></span>|<span data-ttu-id="8a93b-130">Angiv det kontoskema, som KPI-webtjenesten er baseret på.</span><span class="sxs-lookup"><span data-stu-id="8a93b-130">Specify the account schedule that the KPI web service is based on.</span></span>|  
    |<span data-ttu-id="8a93b-131">**Beskrivelse af kontoskema**</span><span class="sxs-lookup"><span data-stu-id="8a93b-131">**Acc. Schedule Description**</span></span>|<span data-ttu-id="8a93b-132">Angiv beskrivelsen af det kontoskema, som KPI-webtjenesten er baseret på.</span><span class="sxs-lookup"><span data-stu-id="8a93b-132">Specify the description of the account schedule that the KPI web service is based on.</span></span>|  

4.  <span data-ttu-id="8a93b-133">Gentag trin 3 for alle de kontoskemaer, som du vil basere kontoskema-KPI-webtjenesten på.</span><span class="sxs-lookup"><span data-stu-id="8a93b-133">Repeat step 3 for all the account schedules that you want to base the account-schedule KPI web service on.</span></span>  
5.  <span data-ttu-id="8a93b-134">Hvis du ønsker at få vist det valgte kontoskema, skal du vælge handlingen **Rediger kontoskema** på oversigtspanelet **Kontoskema**.</span><span class="sxs-lookup"><span data-stu-id="8a93b-134">To view or edit the selected account schedule, on the **Account Schedule** FastTab, choose the **Edit Account Schedule** action.</span></span>  
6.  <span data-ttu-id="8a93b-135">Hvis du ønsker at få vist de kontoskema-KPI-data, som du har konfigureret, skal du vælge handlingen **Webtjenesten Kontoskema, KPI**.</span><span class="sxs-lookup"><span data-stu-id="8a93b-135">To view the account-schedule KPI data that you have set up, choose the **Account Schedule KPI Web Service** action.</span></span>  
7.  <span data-ttu-id="8a93b-136">Hvis du vil udgive kontoskema-KPI-webtjenesten, skal du vælge handlingen **Publicer webtjeneste**.</span><span class="sxs-lookup"><span data-stu-id="8a93b-136">To publish the account-schedule KPI web service, choose the **Publish Web Service** action.</span></span> <span data-ttu-id="8a93b-137">Webtjenesten føjes til listen over publicerede webtjenester i vinduet **Webtjeneste**.</span><span class="sxs-lookup"><span data-stu-id="8a93b-137">The web service is added to the list of published web services in the **Web Services** window.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="8a93b-138">Du kan også publicere KPI-webtjenesten ved at pege på sideobjektet **Konfiguration af webtjenesten Kontoskema, KPI** fra siden **Webtjeneste**.</span><span class="sxs-lookup"><span data-stu-id="8a93b-138">You can also publish the KPI web service by pointing to the **Account Schedule KPI Web Service Setup** page object from the **Web Services** window.</span></span> <span data-ttu-id="8a93b-139">Du kan finde flere oplysninger i [Fremgangsmåde: Udgive en webtjeneste](https://msdn.microsoft.com/en-us/library/dd338978.aspx) på MSDN.</span><span class="sxs-lookup"><span data-stu-id="8a93b-139">For more information, see [How to: Publish a Web Service](https://msdn.microsoft.com/en-us/library/dd338978.aspx) on MSDN.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8a93b-140">Se også</span><span class="sxs-lookup"><span data-stu-id="8a93b-140">See Also</span></span>  
[<span data-ttu-id="8a93b-141">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="8a93b-141">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="8a93b-142">Finans</span><span class="sxs-lookup"><span data-stu-id="8a93b-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="8a93b-143">Konfigurere Finans</span><span class="sxs-lookup"><span data-stu-id="8a93b-143">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="8a93b-144">Finans- og kontoplanen</span><span class="sxs-lookup"><span data-stu-id="8a93b-144">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="8a93b-145">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8a93b-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
