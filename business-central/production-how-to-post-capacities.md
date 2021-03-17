---
title: Sådan bogføres kapaciteter | Microsoft Docs
description: I kapacitetskladden kan du bogføre forbrugt kapacitet, der ikke er knyttet til produktionsordren. Vedligeholdelsesarbejde skal f.eks. knyttes til kapaciteten, men ikke til en produktionsordre.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cab8b2e4670a04e52bdc1edcc91c50a44da06b0d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5381236"
---
# <a name="post-capacities"></a><span data-ttu-id="2511a-104">Bogføre kapaciteter</span><span class="sxs-lookup"><span data-stu-id="2511a-104">Post Capacities</span></span>
<span data-ttu-id="2511a-105">I kapacitetskladden kan du bogføre forbrugt kapacitet, der ikke er knyttet til produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="2511a-105">In the capacity journal, you post consumed capacities that are not assigned to the production order.</span></span> <span data-ttu-id="2511a-106">Vedligeholdelsesarbejde skal f.eks. knyttes til kapaciteten, men ikke til en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="2511a-106">For example, maintenance work must be assigned to capacity, but not to a production order.</span></span>  

## <a name="to-post-capacities"></a><span data-ttu-id="2511a-107">Sådan bogføres kapaciteter</span><span class="sxs-lookup"><span data-stu-id="2511a-107">To post capacities</span></span>  
1.  <span data-ttu-id="2511a-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kapacitetskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="2511a-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Capacity Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2511a-109">Udfyld felterne **Bogføringsdato** og **Bilagsnr** .</span><span class="sxs-lookup"><span data-stu-id="2511a-109">Fill in the **Posting Date** and **Document No.** fields.</span></span>  
3.  <span data-ttu-id="2511a-110">Angiv den type kapacitet, du bogfører, i feltet **Type**, enten **Produktionsressource** eller **Arbejdscenter**.</span><span class="sxs-lookup"><span data-stu-id="2511a-110">In the **Type** field, enter the type of the capacity, either **Machine Center** or **Work Center**, that you are posting.</span></span>  
4.  <span data-ttu-id="2511a-111">I feltet **Nummer**</span><span class="sxs-lookup"><span data-stu-id="2511a-111">In the **No.**</span></span> <span data-ttu-id="2511a-112">skal du angive nummeret på produktionsressourcen eller arbejdscentret.</span><span class="sxs-lookup"><span data-stu-id="2511a-112">field, enter the number of the machine center or work center.</span></span>  
5.  <span data-ttu-id="2511a-113">Angiv de relevante data i de andre felter, f.eks. **Starttidspunkt**, **Sluttidspunkt**, **Antal** og **Spild**.</span><span class="sxs-lookup"><span data-stu-id="2511a-113">Enter the relevant data in the other fields, such as **Starting Time**, **Ending Time**, **Quantity**, and **Scrap**.</span></span>  
6.  <span data-ttu-id="2511a-114">Vælg handlingen **Bogfør** for at bogføre kapaciteterne.</span><span class="sxs-lookup"><span data-stu-id="2511a-114">Choose the **Post** action to post the capacities.</span></span>  

## <a name="to-view-work-center-ledger-entries"></a><span data-ttu-id="2511a-115">Sådan vises arbejdscenterposter</span><span class="sxs-lookup"><span data-stu-id="2511a-115">To view work center ledger entries</span></span>  
<span data-ttu-id="2511a-116">På siderne **Arbejdscenterkort** og **Prod.ress.kort** kan du få vist de bogførte kapaciteter som følge af færdige produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="2511a-116">In the **Work Center Card** and **Machine Center Card** pages, you can view the posted capacities as a result of finished production orders.</span></span>    
1.  <span data-ttu-id="2511a-117">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Arbejdscentre**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="2511a-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Centers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2511a-118">Åbn det relevante **arbejdscenter**-kort på listen, og vælg derefter handlingen **Kapacitetsposter**.</span><span class="sxs-lookup"><span data-stu-id="2511a-118">Open the relevant **Work Center** card from the list, and then choose the **Capacity Ledger Entries** action.</span></span>  

<span data-ttu-id="2511a-119">Siden **Kapacitetsposter** vises med posterne i den rækkefølge, de er bogført.</span><span class="sxs-lookup"><span data-stu-id="2511a-119">The **Capacity Ledger Entries** page displays the posted entries from the work center in the order they were posted.</span></span>   

## <a name="see-also"></a><span data-ttu-id="2511a-120">Se også</span><span class="sxs-lookup"><span data-stu-id="2511a-120">See Also</span></span>  
<span data-ttu-id="2511a-121">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="2511a-121">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="2511a-122">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="2511a-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="2511a-123">[Planlægning](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="2511a-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="2511a-124">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="2511a-124">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="2511a-125">Køb</span><span class="sxs-lookup"><span data-stu-id="2511a-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="2511a-126">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2511a-126">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]