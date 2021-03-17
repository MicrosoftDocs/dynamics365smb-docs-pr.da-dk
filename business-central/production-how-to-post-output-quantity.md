---
title: Sådan massebogføres produktionsafgang og operationstid | Microsoft Docs
description: Afgangsantallet angiver arbejdsforløbet i form af det færdige antal.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 83354217bac3b27457303083163cf5eae4494e79
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380452"
---
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="12f3a-103">Massebogføre afgang og operationstider</span><span class="sxs-lookup"><span data-stu-id="12f3a-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="12f3a-104">Afgangsantallet angiver arbejdsforløbet i form af det færdige antal.</span><span class="sxs-lookup"><span data-stu-id="12f3a-104">The output quantity represents the work progress in the form of the finished quantity.</span></span>  

> [!NOTE]
> <span data-ttu-id="12f3a-105">Lageret opdateres kun automatisk, når du bogfører afgangsantal i den sidste operation.</span><span class="sxs-lookup"><span data-stu-id="12f3a-105">Only when you post output quantity on the last operation, the inventory is updated automatically.</span></span>  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a><span data-ttu-id="12f3a-106">Sådan bogføres afgangsantal for en eller flere produktionsordrelinjer</span><span class="sxs-lookup"><span data-stu-id="12f3a-106">To post output quantities for one or more production order lines</span></span>
1. <span data-ttu-id="12f3a-107">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Afgangskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="12f3a-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="12f3a-108">Udfyld felterne med produktionsordredataene og afgangsdataene.</span><span class="sxs-lookup"><span data-stu-id="12f3a-108">Fill in the fields with the production order data and the output data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="12f3a-109">Hvis operationen er afsluttet, skal du markere feltet **Afsluttet**.</span><span class="sxs-lookup"><span data-stu-id="12f3a-109">If the operation has been completed, select the **Finished** field.</span></span>  

    <span data-ttu-id="12f3a-110">Hvis den lagerlokation, hvor varerne skal lægges på lager, bruger placeringer, men ikke kræver læg-på-lager, skal du tildele en placeringskode til kladdelinjen for at angive, hvor varerne skal lægges på lageret.</span><span class="sxs-lookup"><span data-stu-id="12f3a-110">If the warehouse location where the items should be put away uses bins but does not require put-away processing,  assign a bin code to the journal line to specify where the items should be placed in the warehouse.</span></span> <span data-ttu-id="12f3a-111">Du kan finde flere oplysninger i [Lægge produktions- eller montageafgange på lager](warehouse-how-to-put-away-production-output.md).</span><span class="sxs-lookup"><span data-stu-id="12f3a-111">For more information, see [Put Away Production or Assembly Output](warehouse-how-to-put-away-production-output.md).</span></span>  

4. <span data-ttu-id="12f3a-112">Vælg handlingen **Bogfør** for at bogføre operationerne.</span><span class="sxs-lookup"><span data-stu-id="12f3a-112">Choose the **Post** acto post the operations.</span></span> <span data-ttu-id="12f3a-113">Afgangsantallet bogføres.</span><span class="sxs-lookup"><span data-stu-id="12f3a-113">The output quantity will be posted.</span></span> <span data-ttu-id="12f3a-114">Varen er nu klar til afsendelse.</span><span class="sxs-lookup"><span data-stu-id="12f3a-114">The item is now available for shipping.</span></span>  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="12f3a-115">Sådan bogføres operationstider for en eller flere produktionsordrelinjer</span><span class="sxs-lookup"><span data-stu-id="12f3a-115">To post run times for one or more production order lines</span></span>
<span data-ttu-id="12f3a-116">Operationstiden angiver arbejdsforløbet i form af den nødvendige arbejdstid.</span><span class="sxs-lookup"><span data-stu-id="12f3a-116">The run time represents work progress in the form of the necessary working time.</span></span>    

1.  <span data-ttu-id="12f3a-117">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Afgangskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="12f3a-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="12f3a-118">Udfyld felterne med produktionsordredataene og afgangsdataene.</span><span class="sxs-lookup"><span data-stu-id="12f3a-118">Fill in the fields with the production order data and the output data.</span></span>  
3.  <span data-ttu-id="12f3a-119">Hvis operationen er afsluttet, skal du vælge feltet **Afsluttet**.</span><span class="sxs-lookup"><span data-stu-id="12f3a-119">If the operation is completed, select the **Finished** field.</span></span>  
4. <span data-ttu-id="12f3a-120">Vælg handlingen **Bogfør** for at bogføre den tid, der bruges pr. operation.</span><span class="sxs-lookup"><span data-stu-id="12f3a-120">Choose the **Post** action to post the time spent per operation.</span></span> <span data-ttu-id="12f3a-121">Kapacitetsposter opdateres for de anvendte arbejdscentre eller produktionsressourcer.</span><span class="sxs-lookup"><span data-stu-id="12f3a-121">Capacity ledger entries are updated for the used work or machine centers.</span></span>

## <a name="see-also"></a><span data-ttu-id="12f3a-122">Se også</span><span class="sxs-lookup"><span data-stu-id="12f3a-122">See Also</span></span>  
<span data-ttu-id="12f3a-123">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="12f3a-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="12f3a-124">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="12f3a-124">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="12f3a-125">[Planlægning](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="12f3a-125">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="12f3a-126">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="12f3a-126">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="12f3a-127">Køb</span><span class="sxs-lookup"><span data-stu-id="12f3a-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="12f3a-128">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="12f3a-128">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]