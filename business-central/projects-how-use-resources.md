---
title: Registrere og regulere ressourceforbrug og priser | Microsoft Docs
description: "Beskriver, hvordan du kan registrere ressourceforbrug eller forbrug, der er knyttet til en sag, for at holde styr på og styre omkostninger, priser, og arbejdstyper."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: cd7561e97439b6ffcac28937a24b75a11bb31987
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="use-resources-for-jobs"></a><span data-ttu-id="ef775-103">Bruge ressourcer til sager</span><span class="sxs-lookup"><span data-stu-id="ef775-103">Use Resources for Jobs</span></span>
<span data-ttu-id="ef775-104">Du registrerer forbruget af ressourcer i jobkladden, for at holde styr på omkostninger, priser og de arbejdstyper, der er knyttet til sagerne.</span><span class="sxs-lookup"><span data-stu-id="ef775-104">You record the usage of resources in the job journal to keep track of costs, prices, and the work types that are linked to jobs.</span></span> <span data-ttu-id="ef775-105">Du kan finde flere oplysninger under [Registrere forbrug for sager](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="ef775-105">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

<span data-ttu-id="ef775-106">Du kan også bogføre forbruget af en ressource i en ressourcekladde.</span><span class="sxs-lookup"><span data-stu-id="ef775-106">You can also post the usage of a resource in a resource journal.</span></span> <span data-ttu-id="ef775-107">Posteringer i en ressourcekladde har ingen indflydelse på finanskontiene.</span><span class="sxs-lookup"><span data-stu-id="ef775-107">Entries posted in a resource journal have no effect on the general ledger.</span></span>

## <a name="to-assign-resources-to-jobs"></a><span data-ttu-id="ef775-108">Sådan tildeles ressourcer til sager</span><span class="sxs-lookup"><span data-stu-id="ef775-108">To assign resources to jobs</span></span>
<span data-ttu-id="ef775-109">Du kan tildele ressourcer til sager ved at oprette sagsplanlægningslinjer for sagen.</span><span class="sxs-lookup"><span data-stu-id="ef775-109">You assign resources to jobs by creating job planning lines for the job.</span></span> <span data-ttu-id="ef775-110">Du kan finde flere oplysninger i [Oprette sager](projects-how-create-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="ef775-110">For more information, see [Create Jobs](projects-how-create-jobs.md).</span></span>

## <a name="to-record-resource-usage-for-a-job"></a><span data-ttu-id="ef775-111">Sådan registreres ressourceforbrug for en sag</span><span class="sxs-lookup"><span data-stu-id="ef775-111">To record resource usage for a job</span></span>
1. <span data-ttu-id="ef775-112">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Sagskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ef775-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="ef775-113">Åbn en relevante sagskladde, og udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="ef775-113">Open a relevant job journal batch, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="ef775-114">Når kladden er fuldført, skal du vælge handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="ef775-114">When the journal is complete, choose the **Post** action.</span></span>

## <a name="to-adjust-resource-prices"></a><span data-ttu-id="ef775-115">Sådan reguleres ressourcepriser</span><span class="sxs-lookup"><span data-stu-id="ef775-115">To adjust resource prices</span></span>
<span data-ttu-id="ef775-116">Hvis du vil ændre kost- eller salgspriser for et større antal ressourcer, kan du anvende en kørsel.</span><span class="sxs-lookup"><span data-stu-id="ef775-116">If you want to change costs or prices for a large number of resources, you can use a batch job.</span></span>  

1. <span data-ttu-id="ef775-117">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Reguler ressourcepriser**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ef775-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Adjust Resource Costs/Prices**, and then choose the related link.</span></span>
2. <span data-ttu-id="ef775-118">Udfyld felterne på linjen efter behov, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef775-118">Fill in the fields on a line as necessary, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="ef775-119">Denne kørsel kan ikke bruges til at ændre eller oprette alternative salgs- eller købspriser for ressourcer.</span><span class="sxs-lookup"><span data-stu-id="ef775-119">This batch job does not create or adjust alternate costs or prices for resources.</span></span> <span data-ttu-id="ef775-120">Den ændrer kun indholdet af feltet på ressourcekortet for feltet **Reguler felt**, som du har markeret i kørslen.</span><span class="sxs-lookup"><span data-stu-id="ef775-120">It only changes the contents of the field on the resource card for the **Adjust Field** field that you selected in the batch job.</span></span> <span data-ttu-id="ef775-121">Reguleringen træder i kraft med det samme for ressourcen, så du bør kontrollere reguleringsfaktorerne før kørslen.</span><span class="sxs-lookup"><span data-stu-id="ef775-121">The adjustment will take effect immediately for resources, so check your adjustment factors before you run the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a><span data-ttu-id="ef775-122">Sådan hentes forslag til ændring af ressourcepriser ud fra eksisterende alternative priser</span><span class="sxs-lookup"><span data-stu-id="ef775-122">To get resource price change suggestions based on existing alternate prices</span></span>
<span data-ttu-id="ef775-123">Hvis du allerede har angivet en alternativ ressourcepris for nogle ressourcer, kan du bruge en kørsel til at angive flere alternative ressourcepriser.</span><span class="sxs-lookup"><span data-stu-id="ef775-123">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="ef775-124">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ressourceprisforslag**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ef775-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="ef775-125">Vælg handlingen **Foreslå ress.salgspris (pris)**, og udfyld derefter felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="ef775-125">Choose the **Suggest Res. Price Chg. (Price)** action, and then fill in the fields as necessary.</span></span>
3. <span data-ttu-id="ef775-126">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef775-126">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="ef775-127">Vinduet **Ressourceprisforslag** viser resultatet af kørslen, når den er færdig.</span><span class="sxs-lookup"><span data-stu-id="ef775-127">When the batch job is finished, the **Resource Price Changes** window shows the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a><span data-ttu-id="ef775-128">Sådan henter du forslag til ændring af ressourcepriser ud fra standardpriser</span><span class="sxs-lookup"><span data-stu-id="ef775-128">To get resource price change suggestions based on standard prices</span></span>
<span data-ttu-id="ef775-129">Hvis du vil angive flere alternative ressourcepriser ud fra standardpriserne på ressourcekortet, kan du anvende en kørsel.</span><span class="sxs-lookup"><span data-stu-id="ef775-129">If you want to set up multiple alternate resource prices based on the standard prices on the resource cards, you can use a batch job.</span></span>  

1. <span data-ttu-id="ef775-130">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ressourceprisforslag**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ef775-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="ef775-131">Vælg handlingen **Foreslå ress.salgspris (ress.)**, og udfyld derefter felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="ef775-131">Choose the **Suggest Res. Price Chg. (Res.)** action, and then fill in the fields as necessary.</span></span>  
3. <span data-ttu-id="ef775-132">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef775-132">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="ef775-133">Åbn vinduet **Ressourceprisforslag** for at se resultatet af kørslen, når den er færdig.</span><span class="sxs-lookup"><span data-stu-id="ef775-133">When the batch job is finished, open the **Resource Price Changes** window to see the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a><span data-ttu-id="ef775-134">Sådan henter du forslag til ændring af ressourcepriser ud fra standardpriser</span><span class="sxs-lookup"><span data-stu-id="ef775-134">To get resource price change suggestions based on alternate prices</span></span>
<span data-ttu-id="ef775-135">Hvis du allerede har angivet en alternativ ressourcepris for nogle ressourcer, kan du bruge en kørsel til at angive flere alternative ressourcepriser.</span><span class="sxs-lookup"><span data-stu-id="ef775-135">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="ef775-136">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Foreslå ress.salgs&pris (ress.)**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ef775-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Suggest Res. Price Chg. (Price)**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ef775-137">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="ef775-137">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="ef775-138">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef775-138">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="ef775-139">Åbn vinduet **Ressourceprisforslag** for at se resultatet af kørslen, når den er færdig.</span><span class="sxs-lookup"><span data-stu-id="ef775-139">When the batch job is finished, open the **Resource Price Changes** window to see the results of the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef775-140">Se også</span><span class="sxs-lookup"><span data-stu-id="ef775-140">See Also</span></span>
[<span data-ttu-id="ef775-141">Projektstyring</span><span class="sxs-lookup"><span data-stu-id="ef775-141">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="ef775-142">Finans</span><span class="sxs-lookup"><span data-stu-id="ef775-142">Finance</span></span>](finance.md)  
<span data-ttu-id="ef775-143">[Køb](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="ef775-143">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="ef775-144">[Salg](sales-manage-sales.md)   </span><span class="sxs-lookup"><span data-stu-id="ef775-144">[Sales](sales-manage-sales.md)   </span></span>  
<span data-ttu-id="ef775-145">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ef775-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

