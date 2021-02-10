---
title: Sådan bogføres kapaciteter | Microsoft Docs
description: I kapacitetskladden kan du bogføre forbrugt kapacitet, der ikke er knyttet til produktionsordren. Vedligeholdelsesarbejde skal f.eks. knyttes til kapaciteten, men ikke til en produktionsordre.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2fa0038745664c269d6d471c6d9373a9174df201
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759188"
---
# <a name="post-capacities"></a><span data-ttu-id="e53f4-104">Bogføre kapaciteter</span><span class="sxs-lookup"><span data-stu-id="e53f4-104">Post Capacities</span></span>
<span data-ttu-id="e53f4-105">I kapacitetskladden kan du bogføre forbrugt kapacitet, der ikke er knyttet til produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="e53f4-105">In the capacity journal, you post consumed capacities that are not assigned to the production order.</span></span> <span data-ttu-id="e53f4-106">Vedligeholdelsesarbejde skal f.eks. knyttes til kapaciteten, men ikke til en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="e53f4-106">For example, maintenance work must be assigned to capacity, but not to a production order.</span></span>  

## <a name="to-post-capacities"></a><span data-ttu-id="e53f4-107">Sådan bogføres kapaciteter</span><span class="sxs-lookup"><span data-stu-id="e53f4-107">To post capacities</span></span>  
1.  <span data-ttu-id="e53f4-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kapacitetskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="e53f4-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Capacity Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e53f4-109">Udfyld felterne **Bogføringsdato** og **Bilagsnr** .</span><span class="sxs-lookup"><span data-stu-id="e53f4-109">Fill in the **Posting Date** and **Document No.** fields.</span></span>  
3.  <span data-ttu-id="e53f4-110">Angiv den type kapacitet, du bogfører, i feltet **Type**, enten **Produktionsressource** eller **Arbejdscenter**.</span><span class="sxs-lookup"><span data-stu-id="e53f4-110">In the **Type** field, enter the type of the capacity, either **Machine Center** or **Work Center**, that you are posting.</span></span>  
4.  <span data-ttu-id="e53f4-111">I feltet **Nummer**</span><span class="sxs-lookup"><span data-stu-id="e53f4-111">In the **No.**</span></span> <span data-ttu-id="e53f4-112">skal du angive nummeret på produktionsressourcen eller arbejdscentret.</span><span class="sxs-lookup"><span data-stu-id="e53f4-112">field, enter the number of the machine center or work center.</span></span>  
5.  <span data-ttu-id="e53f4-113">Angiv de relevante data i de andre felter, f.eks. **Starttidspunkt**, **Sluttidspunkt**, **Antal** og **Spild**.</span><span class="sxs-lookup"><span data-stu-id="e53f4-113">Enter the relevant data in the other fields, such as **Starting Time**, **Ending Time**, **Quantity**, and **Scrap**.</span></span>  
6.  <span data-ttu-id="e53f4-114">Vælg handlingen **Bogfør** for at bogføre kapaciteterne.</span><span class="sxs-lookup"><span data-stu-id="e53f4-114">Choose the **Post** action to post the capacities.</span></span>  

## <a name="to-view-work-center-ledger-entries"></a><span data-ttu-id="e53f4-115">Sådan vises arbejdscenterposter</span><span class="sxs-lookup"><span data-stu-id="e53f4-115">To view work center ledger entries</span></span>  
<span data-ttu-id="e53f4-116">På siderne **Arbejdscenterkort** og **Prod.ress.kort** kan du få vist de bogførte kapaciteter som følge af færdige produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="e53f4-116">In the **Work Center Card** and **Machine Center Card** pages, you can view the posted capacities as a result of finished production orders.</span></span>    
1.  <span data-ttu-id="e53f4-117">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Arbejdscentre**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="e53f4-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Centers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e53f4-118">Åbn det relevante **arbejdscenter**-kort på listen, og vælg derefter handlingen **Kapacitetsposter**.</span><span class="sxs-lookup"><span data-stu-id="e53f4-118">Open the relevant **Work Center** card from the list, and then choose the **Capacity Ledger Entries** action.</span></span>  

<span data-ttu-id="e53f4-119">Siden **Kapacitetsposter** vises med posterne i den rækkefølge, de er bogført.</span><span class="sxs-lookup"><span data-stu-id="e53f4-119">The **Capacity Ledger Entries** page displays the posted entries from the work center in the order they were posted.</span></span>   

## <a name="see-also"></a><span data-ttu-id="e53f4-120">Se også</span><span class="sxs-lookup"><span data-stu-id="e53f4-120">See Also</span></span>  
<span data-ttu-id="e53f4-121">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="e53f4-121">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="e53f4-122">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="e53f4-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="e53f4-123">[Planlægning](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="e53f4-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="e53f4-124">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="e53f4-124">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="e53f4-125">Køb</span><span class="sxs-lookup"><span data-stu-id="e53f4-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="e53f4-126">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e53f4-126">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
