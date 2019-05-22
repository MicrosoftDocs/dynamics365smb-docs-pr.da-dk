---
title: Registrere og regulere ressourceforbrug og priser | Microsoft Docs
description: Beskriver, hvordan du kan registrere ressourceforbrug eller forbrug, der er knyttet til en sag, for at holde styr på og styre omkostninger, priser, og arbejdstyper.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: fc51b47b71d37daaccc4133d648c90b84d5a3494
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251741"
---
# <a name="use-resources-for-jobs"></a><span data-ttu-id="f055c-103">Bruge ressourcer til sager</span><span class="sxs-lookup"><span data-stu-id="f055c-103">Use Resources for Jobs</span></span>
<span data-ttu-id="f055c-104">Du registrerer forbruget af ressourcer i jobkladden, for at holde styr på omkostninger, priser og de arbejdstyper, der er knyttet til sagerne.</span><span class="sxs-lookup"><span data-stu-id="f055c-104">You record the usage of resources in the job journal to keep track of costs, prices, and the work types that are linked to jobs.</span></span> <span data-ttu-id="f055c-105">Du kan finde flere oplysninger under [Registrere forbrug for sager](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="f055c-105">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

<span data-ttu-id="f055c-106">Du kan også bogføre forbruget af en ressource i en ressourcekladde.</span><span class="sxs-lookup"><span data-stu-id="f055c-106">You can also post the usage of a resource in a resource journal.</span></span> <span data-ttu-id="f055c-107">Posteringer i en ressourcekladde har ingen indflydelse på finanskontiene.</span><span class="sxs-lookup"><span data-stu-id="f055c-107">Entries posted in a resource journal have no effect on the general ledger.</span></span>

## <a name="to-assign-resources-to-jobs"></a><span data-ttu-id="f055c-108">Sådan tildeles ressourcer til sager</span><span class="sxs-lookup"><span data-stu-id="f055c-108">To assign resources to jobs</span></span>
<span data-ttu-id="f055c-109">Du kan tildele ressourcer til sager ved at oprette sagsplanlægningslinjer for sagen.</span><span class="sxs-lookup"><span data-stu-id="f055c-109">You assign resources to jobs by creating job planning lines for the job.</span></span> <span data-ttu-id="f055c-110">Du kan finde flere oplysninger i [Oprette sager](projects-how-create-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="f055c-110">For more information, see [Create Jobs](projects-how-create-jobs.md).</span></span>

## <a name="to-record-resource-usage-for-a-job"></a><span data-ttu-id="f055c-111">Sådan registreres ressourceforbrug for en sag</span><span class="sxs-lookup"><span data-stu-id="f055c-111">To record resource usage for a job</span></span>
1. <span data-ttu-id="f055c-112">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sagskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f055c-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="f055c-113">Åbn en relevante sagskladde, og udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="f055c-113">Open a relevant job journal batch, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="f055c-114">Når kladden er fuldført, skal du vælge handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="f055c-114">When the journal is complete, choose the **Post** action.</span></span>

## <a name="to-adjust-resource-prices"></a><span data-ttu-id="f055c-115">Sådan reguleres ressourcepriser</span><span class="sxs-lookup"><span data-stu-id="f055c-115">To adjust resource prices</span></span>
<span data-ttu-id="f055c-116">Hvis du vil ændre kost- eller salgspriser for et større antal ressourcer, kan du anvende en kørsel.</span><span class="sxs-lookup"><span data-stu-id="f055c-116">If you want to change costs or prices for a large number of resources, you can use a batch job.</span></span>  

1. <span data-ttu-id="f055c-117">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Reguler ressourcepriser**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f055c-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Adjust Resource Costs/Prices**, and then choose the related link.</span></span>
2. <span data-ttu-id="f055c-118">Udfyld felterne på linjen efter behov, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="f055c-118">Fill in the fields on a line as necessary, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="f055c-119">Denne kørsel kan ikke bruges til at ændre eller oprette alternative salgs- eller købspriser for ressourcer.</span><span class="sxs-lookup"><span data-stu-id="f055c-119">This batch job does not create or adjust alternate costs or prices for resources.</span></span> <span data-ttu-id="f055c-120">Den ændrer kun indholdet af feltet på ressourcekortet for feltet **Reguler felt**, som du har markeret i kørslen.</span><span class="sxs-lookup"><span data-stu-id="f055c-120">It only changes the contents of the field on the resource card for the **Adjust Field** field that you selected in the batch job.</span></span> <span data-ttu-id="f055c-121">Reguleringen træder i kraft med det samme for ressourcen, så du bør kontrollere reguleringsfaktorerne før kørslen.</span><span class="sxs-lookup"><span data-stu-id="f055c-121">The adjustment will take effect immediately for resources, so check your adjustment factors before you run the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a><span data-ttu-id="f055c-122">Sådan hentes forslag til ændring af ressourcepriser ud fra eksisterende alternative priser</span><span class="sxs-lookup"><span data-stu-id="f055c-122">To get resource price change suggestions based on existing alternate prices</span></span>
<span data-ttu-id="f055c-123">Hvis du allerede har angivet en alternativ ressourcepris for nogle ressourcer, kan du bruge en kørsel til at angive flere alternative ressourcepriser.</span><span class="sxs-lookup"><span data-stu-id="f055c-123">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="f055c-124">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Ressourceprisforslag**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f055c-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="f055c-125">Vælg handlingen **Foreslå ress.salgspris (pris)**, og udfyld derefter felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="f055c-125">Choose the **Suggest Res. Price Chg. (Price)** action, and then fill in the fields as necessary.</span></span>
3. <span data-ttu-id="f055c-126">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="f055c-126">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="f055c-127">Siden **Ressourceprisforslag** viser resultatet af kørslen, når den er færdig.</span><span class="sxs-lookup"><span data-stu-id="f055c-127">When the batch job is finished, the **Resource Price Changes** page shows the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a><span data-ttu-id="f055c-128">Sådan henter du forslag til ændring af ressourcepriser ud fra standardpriser</span><span class="sxs-lookup"><span data-stu-id="f055c-128">To get resource price change suggestions based on standard prices</span></span>
<span data-ttu-id="f055c-129">Hvis du vil angive flere alternative ressourcepriser ud fra standardpriserne på ressourcekortet, kan du anvende en kørsel.</span><span class="sxs-lookup"><span data-stu-id="f055c-129">If you want to set up multiple alternate resource prices based on the standard prices on the resource cards, you can use a batch job.</span></span>  

1. <span data-ttu-id="f055c-130">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Ressourceprisforslag**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f055c-130">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="f055c-131">Vælg handlingen **Foreslå ress.salgspris (ress.)**, og udfyld derefter felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="f055c-131">Choose the **Suggest Res. Price Chg. (Res.)** action, and then fill in the fields as necessary.</span></span>  
3. <span data-ttu-id="f055c-132">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="f055c-132">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="f055c-133">Åbn siden **Ressourceprisforslag** for at se resultatet af kørslen, når den er færdig.</span><span class="sxs-lookup"><span data-stu-id="f055c-133">When the batch job is finished, open the **Resource Price Changes** page to see the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a><span data-ttu-id="f055c-134">Sådan henter du forslag til ændring af ressourcepriser ud fra standardpriser</span><span class="sxs-lookup"><span data-stu-id="f055c-134">To get resource price change suggestions based on alternate prices</span></span>
<span data-ttu-id="f055c-135">Hvis du allerede har angivet en alternativ ressourcepris for nogle ressourcer, kan du bruge en kørsel til at angive flere alternative ressourcepriser.</span><span class="sxs-lookup"><span data-stu-id="f055c-135">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="f055c-136">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Foreslå ress.salgs&pris (ress.)**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f055c-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Suggest Res. Price Chg. (Price)**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f055c-137">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="f055c-137">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="f055c-138">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="f055c-138">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="f055c-139">Åbn siden **Ressourceprisforslag** for at se resultatet af kørslen, når den er færdig.</span><span class="sxs-lookup"><span data-stu-id="f055c-139">When the batch job is finished, open the **Resource Price Changes** page to see the results of the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="f055c-140">Se også</span><span class="sxs-lookup"><span data-stu-id="f055c-140">See Also</span></span>
[<span data-ttu-id="f055c-141">Projektstyring</span><span class="sxs-lookup"><span data-stu-id="f055c-141">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="f055c-142">Finans</span><span class="sxs-lookup"><span data-stu-id="f055c-142">Finance</span></span>](finance.md)  
<span data-ttu-id="f055c-143">[Køb](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="f055c-143">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="f055c-144">[Salg](sales-manage-sales.md)   </span><span class="sxs-lookup"><span data-stu-id="f055c-144">[Sales](sales-manage-sales.md)   </span></span>  
<span data-ttu-id="f055c-145">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f055c-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
