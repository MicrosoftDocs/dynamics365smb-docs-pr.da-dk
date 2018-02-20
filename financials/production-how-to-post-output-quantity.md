---
title: "Sådan massebogføres produktionsafgang og operationstid | Microsoft Docs"
description: "Afgangsantallet angiver arbejdsforløbet i form af det færdige antal."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e885149e28c2e09dc244bc5c0a431e7b2fe047a5
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="766e8-103">Massebogføre afgang og operationstider</span><span class="sxs-lookup"><span data-stu-id="766e8-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="766e8-104">Afgangsantallet angiver arbejdsforløbet i form af det færdige antal.</span><span class="sxs-lookup"><span data-stu-id="766e8-104">The output quantity represents the work progress in the form of the finished quantity.</span></span>  

> [!NOTE]
> <span data-ttu-id="766e8-105">Lageret opdateres kun automatisk, når du bogfører afgangsantal i den sidste operation.</span><span class="sxs-lookup"><span data-stu-id="766e8-105">Only when you post output quantity on the last operation, the inventory is updated automatically.</span></span>  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a><span data-ttu-id="766e8-106">Sådan bogføres afgangsantal for en eller flere produktionsordrelinjer</span><span class="sxs-lookup"><span data-stu-id="766e8-106">To post output quantities for one or more production order lines</span></span>
1. <span data-ttu-id="766e8-107">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Afgangskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="766e8-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="766e8-108">Udfyld felterne med produktionsordredataene og afgangsdataene.</span><span class="sxs-lookup"><span data-stu-id="766e8-108">Fill in the fields with the production order data and the output data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="766e8-109">Hvis operationen er afsluttet, skal du markere feltet **Afsluttet**.</span><span class="sxs-lookup"><span data-stu-id="766e8-109">If the operation has been completed, select the **Finished** field.</span></span>  

    <span data-ttu-id="766e8-110">Hvis den lagerlokation, hvor varerne skal lægges på lager, bruger placeringer, men ikke kræver læg-på-lager, skal du  tildele en placeringskode til kladdelinjen for at angive, hvor varerne skal lægges på lageret.</span><span class="sxs-lookup"><span data-stu-id="766e8-110">If the warehouse location where the items should be put away uses bins but does not require put-away processing,  assign a bin code to the journal line to specify where the items should be placed in the warehouse.</span></span> <span data-ttu-id="766e8-111">Du kan finde flere oplysninger i [Lægge produktions- eller montageafgange på lager](warehouse-how-to-put-away-production-output.md).</span><span class="sxs-lookup"><span data-stu-id="766e8-111">For more information, see [Put Away Production or Assembly Output](warehouse-how-to-put-away-production-output.md).</span></span>  

4. <span data-ttu-id="766e8-112">Vælg handlingen **Bogfør** for at bogføre operationerne.</span><span class="sxs-lookup"><span data-stu-id="766e8-112">Choose the **Post** acto post the operations.</span></span> <span data-ttu-id="766e8-113">Afgangsantallet bogføres.</span><span class="sxs-lookup"><span data-stu-id="766e8-113">The output quantity will be posted.</span></span> <span data-ttu-id="766e8-114">Varen er nu klar til afsendelse.</span><span class="sxs-lookup"><span data-stu-id="766e8-114">The item is now available for shipping.</span></span>  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="766e8-115">Sådan bogføres operationstider for en eller flere produktionsordrelinjer</span><span class="sxs-lookup"><span data-stu-id="766e8-115">To post run times for one or more production order lines</span></span>
<span data-ttu-id="766e8-116">Operationstiden angiver arbejdsforløbet i form af den nødvendige arbejdstid.</span><span class="sxs-lookup"><span data-stu-id="766e8-116">The run time represents work progress in the form of the necessary working time.</span></span>    

1.  <span data-ttu-id="766e8-117">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Afgangskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="766e8-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="766e8-118">Udfyld felterne med produktionsordredataene og afgangsdataene.</span><span class="sxs-lookup"><span data-stu-id="766e8-118">Fill in the fields with the production order data and the output data.</span></span>  
3.  <span data-ttu-id="766e8-119">Hvis operationen er afsluttet, skal du vælge feltet **Afsluttet**.</span><span class="sxs-lookup"><span data-stu-id="766e8-119">If the operation is completed, select the **Finished** field.</span></span>  
4. <span data-ttu-id="766e8-120">Vælg handlingen **Bogfør** for at bogføre den tid, der bruges pr. operation.</span><span class="sxs-lookup"><span data-stu-id="766e8-120">Choose the **Post** action to post the time spent per operation.</span></span> <span data-ttu-id="766e8-121">Kapacitetsposter opdateres for de anvendte arbejdscentre eller produktionsressourcer.</span><span class="sxs-lookup"><span data-stu-id="766e8-121">Capacity ledger entries are updated for the used work or machine centers.</span></span>

## <a name="see-also"></a><span data-ttu-id="766e8-122">Se også</span><span class="sxs-lookup"><span data-stu-id="766e8-122">See Also</span></span>  
<span data-ttu-id="766e8-123">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="766e8-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="766e8-124">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="766e8-124">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="766e8-125">[Planlægning](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="766e8-125">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="766e8-126">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="766e8-126">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="766e8-127">Køb</span><span class="sxs-lookup"><span data-stu-id="766e8-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="766e8-128">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="766e8-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

