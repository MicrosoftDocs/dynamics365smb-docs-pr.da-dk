---
title: Massebogføre produktionsafgang og operationstider
description: Afgangsantallet repræsenterer arbejdsforløbet i form af den færdige mængde og den anvendte kapacitet for arbejdscentret eller produktionsressourcen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 923f68b13619013dd54062438c66192a682868bc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787873"
---
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="67afc-103">Massebogføre afgang og operationstider</span><span class="sxs-lookup"><span data-stu-id="67afc-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="67afc-104">Afgangsantallet repræsenterer arbejdsforløbet i form af den færdige mængde og den anvendte kapacitet for arbejdscentret eller produktionsressourcen.</span><span class="sxs-lookup"><span data-stu-id="67afc-104">The output quantity represents the work progress in the form of the finished quantity and used capacity of work or machine center.</span></span>

<span data-ttu-id="67afc-105">Du kan bruge afgangskladden til at:</span><span class="sxs-lookup"><span data-stu-id="67afc-105">You can use the output journal to:</span></span>
*  <span data-ttu-id="67afc-106">Justere lagerbeholdningen i forbindelse med afgang af færdige varer fra produktion.</span><span class="sxs-lookup"><span data-stu-id="67afc-106">Adjust inventory in connection with output of finished items from production.</span></span>
*  <span data-ttu-id="67afc-107">Registrere antal og spild for hver operation i produktionsruten.</span><span class="sxs-lookup"><span data-stu-id="67afc-107">Register quantities and scrap for each operation in production routing.</span></span>
*  <span data-ttu-id="67afc-108">Registrere opsætning og operationstid for arbejdscentre og produktionsressourcer.</span><span class="sxs-lookup"><span data-stu-id="67afc-108">Register setup and run time for work and machine centers.</span></span>

> [!NOTE]
> <span data-ttu-id="67afc-109">Hvis produktionsrute anvendes, opdateres lagerbeholdningen kun, når du bogfører afgangsantal for den sidste operation.</span><span class="sxs-lookup"><span data-stu-id="67afc-109">If production routing are used, the inventory is updated only when you post output quantity on the last operation.</span></span>

<span data-ttu-id="67afc-110">Med vinduet **Produktionskladde** kan du udføre de samme opgaver som i vinduet **Afgangskladde** og samtidigt udføre relaterede forbrugsbogføringsopgaver.</span><span class="sxs-lookup"><span data-stu-id="67afc-110">With the **Production Journal** window, you can perform the same tasks as in the **Output Journal** window and at the same time perform the related consumption posting tasks.</span></span> <span data-ttu-id="67afc-111">Du kan finde flere oplysninger i [Registrere forbrug og afgang for én frigivet produktionsordrelinje](production-how-to-register-consumption-and-output.md).</span><span class="sxs-lookup"><span data-stu-id="67afc-111">For more information, see [Register Consumption and Output for One Released Production order line](production-how-to-register-consumption-and-output.md).</span></span>

## <a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="67afc-112">Sådan bogfører du afgangsantal og/eller registrerer du operationstider for en eller flere produktionsordrelinjer</span><span class="sxs-lookup"><span data-stu-id="67afc-112">To post output quantities and/or register run times for one or more production order lines</span></span>
1. <span data-ttu-id="67afc-113">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Afgangskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="67afc-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="67afc-114">Udfyld felterne med produktionsordredata, afgangsdata og/eller operationstid.</span><span class="sxs-lookup"><span data-stu-id="67afc-114">Fill in the fields with the production order data and the output data and/or run time.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    <span data-ttu-id="67afc-115">Du kan bruge funktionen **Udfold rute** til at generere kladdelinjer fra produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="67afc-115">You can use the **Explode Routing** function to generate journal lines from production orders.</span></span>
  
4. <span data-ttu-id="67afc-116">Hvis operationen er afsluttet, skal du markere feltet **Afsluttet**.</span><span class="sxs-lookup"><span data-stu-id="67afc-116">If the operation has been completed, select the **Finished** field.</span></span>  
5. <span data-ttu-id="67afc-117">Vælg handlingen **Bogfør** for at bogføre operationer.</span><span class="sxs-lookup"><span data-stu-id="67afc-117">Choose the **Post** action to post the operations.</span></span> 
 
<span data-ttu-id="67afc-118">Kapacitetsposterne opdateres for de anvendte arbejdscentre eller produktionsressourcer med oplysninger om tid, antal og spild.</span><span class="sxs-lookup"><span data-stu-id="67afc-118">Capacity ledger entries are updated for the used work or machine centers with information about time and quantity of output and scrap.</span></span> <span data-ttu-id="67afc-119">Hvis du har bogført den sidste operation, føjes varen til lageret.</span><span class="sxs-lookup"><span data-stu-id="67afc-119">If you posted the last operation, the item will be added to the inventory.</span></span> 

## <a name="see-also"></a><span data-ttu-id="67afc-120">Se også</span><span class="sxs-lookup"><span data-stu-id="67afc-120">See Also</span></span>  
<span data-ttu-id="67afc-121">[Bogføre spild manuelt](production-how-to-post-scrap.md)
[Tilbageføre bogføring af afgang](production-how-to-reverse-output-posting.md)
[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="67afc-121">[Post Scrap Manually](production-how-to-post-scrap.md)
[Reverse Output Posting](production-how-to-reverse-output-posting.md)
[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="67afc-122">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="67afc-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="67afc-123">[Planlægning](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="67afc-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="67afc-124">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="67afc-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="67afc-125">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="67afc-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
