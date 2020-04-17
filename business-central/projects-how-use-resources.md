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
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: b1c91caed8fb682af4c754aef83801083a714d4f
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3193799"
---
# <a name="use-resources-for-jobs"></a><span data-ttu-id="64115-103">Bruge ressourcer til sager</span><span class="sxs-lookup"><span data-stu-id="64115-103">Use Resources for Jobs</span></span>
<span data-ttu-id="64115-104">Du registrerer forbruget af ressourcer i jobkladden, for at holde styr på omkostninger, priser og de arbejdstyper, der er knyttet til sagerne.</span><span class="sxs-lookup"><span data-stu-id="64115-104">You record the usage of resources in the job journal to keep track of costs, prices, and the work types that are linked to jobs.</span></span> <span data-ttu-id="64115-105">Du kan finde flere oplysninger under [Registrere forbrug for sager](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="64115-105">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

> [!NOTE]
> <span data-ttu-id="64115-106">Du kan også købe eksterne ressourcer, f. eks. for at fakturere en kreditor for udført arbejde.</span><span class="sxs-lookup"><span data-stu-id="64115-106">You can also purchase external resources, for example, to invoice a vendor for work delivered.</span></span> <span data-ttu-id="64115-107">Du kan finde flere oplysninger under [Registrere køb](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="64115-107">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

<span data-ttu-id="64115-108">Du kan også bogføre forbruget af en ressource i en ressourcekladde.</span><span class="sxs-lookup"><span data-stu-id="64115-108">You can also post the usage of a resource in a resource journal.</span></span> <span data-ttu-id="64115-109">Posteringer i en ressourcekladde har ingen indflydelse på finanskontiene.</span><span class="sxs-lookup"><span data-stu-id="64115-109">Entries posted in a resource journal have no effect on the general ledger.</span></span>

## <a name="to-assign-resources-to-jobs"></a><span data-ttu-id="64115-110">Sådan tildeles ressourcer til sager</span><span class="sxs-lookup"><span data-stu-id="64115-110">To assign resources to jobs</span></span>
<span data-ttu-id="64115-111">Du kan tildele ressourcer til sager ved at oprette sagsplanlægningslinjer for sagen.</span><span class="sxs-lookup"><span data-stu-id="64115-111">You assign resources to jobs by creating job planning lines for the job.</span></span> <span data-ttu-id="64115-112">Du kan finde flere oplysninger i [Oprette sager](projects-how-create-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="64115-112">For more information, see [Create Jobs](projects-how-create-jobs.md).</span></span>

## <a name="to-record-resource-usage-for-a-job"></a><span data-ttu-id="64115-113">Sådan registreres ressourceforbrug for en sag</span><span class="sxs-lookup"><span data-stu-id="64115-113">To record resource usage for a job</span></span>
1. <span data-ttu-id="64115-114">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sagskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="64115-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="64115-115">Åbn en relevante sagskladde, og udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="64115-115">Open a relevant job journal batch, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="64115-116">Når kladden er fuldført, skal du vælge handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="64115-116">When the journal is complete, choose the **Post** action.</span></span>

## <a name="to-adjust-resource-prices"></a><span data-ttu-id="64115-117">Sådan reguleres ressourcepriser</span><span class="sxs-lookup"><span data-stu-id="64115-117">To adjust resource prices</span></span>
<span data-ttu-id="64115-118">Hvis du vil ændre kost- eller salgspriser for et større antal ressourcer, kan du anvende en kørsel.</span><span class="sxs-lookup"><span data-stu-id="64115-118">If you want to change costs or prices for a large number of resources, you can use a batch job.</span></span>  

1. <span data-ttu-id="64115-119">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Reguler ressourcepriser**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="64115-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Adjust Resource Costs/Prices**, and then choose the related link.</span></span>
2. <span data-ttu-id="64115-120">Udfyld felterne på linjen efter behov, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="64115-120">Fill in the fields on a line as necessary, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="64115-121">Denne kørsel kan ikke bruges til at ændre eller oprette alternative salgs- eller købspriser for ressourcer.</span><span class="sxs-lookup"><span data-stu-id="64115-121">This batch job does not create or adjust alternate costs or prices for resources.</span></span> <span data-ttu-id="64115-122">Den ændrer kun indholdet af feltet på ressourcekortet for feltet **Reguler felt**, som du har markeret i kørslen.</span><span class="sxs-lookup"><span data-stu-id="64115-122">It only changes the contents of the field on the resource card for the **Adjust Field** field that you selected in the batch job.</span></span> <span data-ttu-id="64115-123">Reguleringen træder i kraft med det samme for ressourcen, så du bør kontrollere reguleringsfaktorerne før kørslen.</span><span class="sxs-lookup"><span data-stu-id="64115-123">The adjustment will take effect immediately for resources, so check your adjustment factors before you run the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a><span data-ttu-id="64115-124">Sådan hentes forslag til ændring af ressourcepriser ud fra eksisterende alternative priser</span><span class="sxs-lookup"><span data-stu-id="64115-124">To get resource price change suggestions based on existing alternate prices</span></span>
<span data-ttu-id="64115-125">Hvis du allerede har angivet en alternativ ressourcepris for nogle ressourcer, kan du bruge en kørsel til at angive flere alternative ressourcepriser.</span><span class="sxs-lookup"><span data-stu-id="64115-125">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="64115-126">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Ressourceprisforslag**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="64115-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="64115-127">Vælg handlingen **Foreslå ress.salgspris (pris)**, og udfyld derefter felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="64115-127">Choose the **Suggest Res. Price Chg. (Price)** action, and then fill in the fields as necessary.</span></span>
3. <span data-ttu-id="64115-128">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="64115-128">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="64115-129">Siden **Ressourceprisforslag** viser resultatet af kørslen, når den er færdig.</span><span class="sxs-lookup"><span data-stu-id="64115-129">When the batch job is finished, the **Resource Price Changes** page shows the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a><span data-ttu-id="64115-130">Sådan henter du forslag til ændring af ressourcepriser ud fra standardpriser</span><span class="sxs-lookup"><span data-stu-id="64115-130">To get resource price change suggestions based on standard prices</span></span>
<span data-ttu-id="64115-131">Hvis du vil angive flere alternative ressourcepriser ud fra standardpriserne på ressourcekortet, kan du anvende en kørsel.</span><span class="sxs-lookup"><span data-stu-id="64115-131">If you want to set up multiple alternate resource prices based on the standard prices on the resource cards, you can use a batch job.</span></span>  

1. <span data-ttu-id="64115-132">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Ressourceprisforslag**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="64115-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="64115-133">Vælg handlingen **Foreslå ress.salgspris (ress.)**, og udfyld derefter felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="64115-133">Choose the **Suggest Res. Price Chg. (Res.)** action, and then fill in the fields as necessary.</span></span>  
3. <span data-ttu-id="64115-134">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="64115-134">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="64115-135">Åbn siden **Ressourceprisforslag** for at se resultatet af kørslen, når den er færdig.</span><span class="sxs-lookup"><span data-stu-id="64115-135">When the batch job is finished, open the **Resource Price Changes** page to see the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a><span data-ttu-id="64115-136">Sådan henter du forslag til ændring af ressourcepriser ud fra standardpriser</span><span class="sxs-lookup"><span data-stu-id="64115-136">To get resource price change suggestions based on alternate prices</span></span>
<span data-ttu-id="64115-137">Hvis du allerede har angivet en alternativ ressourcepris for nogle ressourcer, kan du bruge en kørsel til at angive flere alternative ressourcepriser.</span><span class="sxs-lookup"><span data-stu-id="64115-137">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="64115-138">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Foreslå ress.salgspris (pris)**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="64115-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Suggest Res. Price Chg. (Price)**, and then choose the related link.</span></span>  
2. <span data-ttu-id="64115-139">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="64115-139">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="64115-140">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="64115-140">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="64115-141">Åbn siden **Ressourceprisforslag** for at se resultatet af kørslen, når den er færdig.</span><span class="sxs-lookup"><span data-stu-id="64115-141">When the batch job is finished, open the **Resource Price Changes** page to see the results of the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="64115-142">Se også</span><span class="sxs-lookup"><span data-stu-id="64115-142">See Also</span></span>
[<span data-ttu-id="64115-143">Projektstyring</span><span class="sxs-lookup"><span data-stu-id="64115-143">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="64115-144">Finans</span><span class="sxs-lookup"><span data-stu-id="64115-144">Finance</span></span>](finance.md)  
<span data-ttu-id="64115-145">[Køb](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="64115-145">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="64115-146">[Salg](sales-manage-sales.md)   </span><span class="sxs-lookup"><span data-stu-id="64115-146">[Sales](sales-manage-sales.md)   </span></span>  
<span data-ttu-id="64115-147">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="64115-147">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
