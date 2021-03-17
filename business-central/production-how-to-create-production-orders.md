---
title: Sådan oprettes produktionsordrehoveder | Microsoft Docs
description: Du kan oprette en produktionsordre manuelt, og det første trin i denne procedure er at oprette et produktionsordrehoved.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 683631572b7898ede3b7f1418f68a7ce95743ff8
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380887"
---
# <a name="create-production-order-headers"></a><span data-ttu-id="5e635-103">Oprette produktionsordrehoveder</span><span class="sxs-lookup"><span data-stu-id="5e635-103">Create Production Order Headers</span></span>
<span data-ttu-id="5e635-104">Du kan oprette en produktionsordre manuelt, og det første trin i denne procedure er at oprette et produktionsordrehoved.</span><span class="sxs-lookup"><span data-stu-id="5e635-104">You can create a production order manually, and the first step is to create a production order header.</span></span>

<span data-ttu-id="5e635-105">Produktionsordrer oprettes typisk automatisk af en planlægningsfunktion til opfyldning af et kendt behov.</span><span class="sxs-lookup"><span data-stu-id="5e635-105">Production orders are typically created automatically by a planning function to fulfill a known demand.</span></span> <span data-ttu-id="5e635-106">Du kan finde flere oplysninger i [Planlægning](production-planning.md).</span><span class="sxs-lookup"><span data-stu-id="5e635-106">For more information, see [Planning](production-planning.md).</span></span>   

<span data-ttu-id="5e635-107">I proceduren nedenfor oprettes en fastlagt produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="5e635-107">In the following procedure, a firm planned production order is created.</span></span> <span data-ttu-id="5e635-108">Du kan også oprette produktionsordrer med en anden status.</span><span class="sxs-lookup"><span data-stu-id="5e635-108">You can also create production orders with a different status.</span></span>  

## <a name="to-create-a-production-order-header"></a><span data-ttu-id="5e635-109">Sådan oprettes et produktionsordrehovede</span><span class="sxs-lookup"><span data-stu-id="5e635-109">To create a production order header</span></span>  
1.  <span data-ttu-id="5e635-110">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Fastlagt produktionsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="5e635-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5e635-111">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5e635-111">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="5e635-112">I feltet **Nummer**</span><span class="sxs-lookup"><span data-stu-id="5e635-112">In the **No.**</span></span> <span data-ttu-id="5e635-113">skal du indsætte næste nummer i serien.</span><span class="sxs-lookup"><span data-stu-id="5e635-113">field, insert the next number in the series.</span></span>  
4.  <span data-ttu-id="5e635-114">Marker kilden til produktionsordren i feltet **Kildetype**.</span><span class="sxs-lookup"><span data-stu-id="5e635-114">In the **Source Type** field, select the source of the production order.</span></span>

    <span data-ttu-id="5e635-115">Her kan du vælge at oprette til en familie af varer.</span><span class="sxs-lookup"><span data-stu-id="5e635-115">Here you can select to produce for a family of items.</span></span> <span data-ttu-id="5e635-116">Du kan finde flere oplysninger under [Arbejde med produktionsfamilier](production-how-work-family.md).</span><span class="sxs-lookup"><span data-stu-id="5e635-116">For more information, see [Work With Production Families](production-how-work-family.md).</span></span>
5.  <span data-ttu-id="5e635-117">Marker varenummer, familie eller salgshoved, som produktionsordren genereres for, i feltet **Kildenr.**.</span><span class="sxs-lookup"><span data-stu-id="5e635-117">In the **Source No.** field, select the item number, family, or sales header for which the production order is to be generated.</span></span>  
6.  <span data-ttu-id="5e635-118">Udfyld felterne **Antal** og **Forfaldsdato** i overensstemmelse med dine specifikationer.</span><span class="sxs-lookup"><span data-stu-id="5e635-118">Fill in the **Quantity** and **Due Date** fields according to your specifications.</span></span>  

<span data-ttu-id="5e635-119">Når du ændrer produktionskravene, f.eks. komponenter og operationer, kan du hurtigt omplanlægge produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="5e635-119">When production requirements change, such as components or operations, you can quickly replan the production order.</span></span> <span data-ttu-id="5e635-120">Du kan finde flere oplysninger i [Omplanlægge eller forny produktionsordrer direkte](production-how-to-replan-refresh-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="5e635-120">For more information, see [Replan or Refresh Production Orders Directly](production-how-to-replan-refresh-production-orders.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="5e635-121">Se også</span><span class="sxs-lookup"><span data-stu-id="5e635-121">See Also</span></span>  
<span data-ttu-id="5e635-122">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="5e635-122">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="5e635-123">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="5e635-123">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="5e635-124">[Planlægning](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="5e635-124">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="5e635-125">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="5e635-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="5e635-126">Køb</span><span class="sxs-lookup"><span data-stu-id="5e635-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="5e635-127">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5e635-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]