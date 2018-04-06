---
title: "Sådan oprettes produktionsordrehoveder | Microsoft Docs"
description: "Du kan oprette en produktionsordre manuelt, og det første trin i denne procedure er at oprette et produktionsordrehoved."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3ffbe781830a492256be864bace38bbef3050596
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="create-production-order-headers"></a><span data-ttu-id="e4b36-103">Oprette produktionsordrehoveder</span><span class="sxs-lookup"><span data-stu-id="e4b36-103">Create Production Order Headers</span></span>
<span data-ttu-id="e4b36-104">Du kan oprette en produktionsordre manuelt, og det første trin i denne procedure er at oprette et produktionsordrehoved.</span><span class="sxs-lookup"><span data-stu-id="e4b36-104">You can create a production order manually, and the first step is to create a production order header.</span></span>

<span data-ttu-id="e4b36-105">Produktionsordrer oprettes typisk automatisk af en planlægningsfunktion til opfyldning af et kendt behov.</span><span class="sxs-lookup"><span data-stu-id="e4b36-105">Production orders are typically created automatically by a planning function to fulfill a known demand.</span></span> <span data-ttu-id="e4b36-106">Du kan finde flere oplysninger i [Planlægning](production-planning.md).</span><span class="sxs-lookup"><span data-stu-id="e4b36-106">For more information, see [Planning](production-planning.md).</span></span>   

<span data-ttu-id="e4b36-107">I proceduren nedenfor oprettes en fastlagt produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="e4b36-107">In the following procedure, a firm planned production order is created.</span></span> <span data-ttu-id="e4b36-108">Du kan også oprette produktionsordrer med en anden status.</span><span class="sxs-lookup"><span data-stu-id="e4b36-108">You can also create production orders with a different status.</span></span>  

## <a name="to-create-a-production-order-header"></a><span data-ttu-id="e4b36-109">Sådan oprettes et produktionsordrehovede</span><span class="sxs-lookup"><span data-stu-id="e4b36-109">To create a production order header</span></span>  
1.  <span data-ttu-id="e4b36-110">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ordreplanlægning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="e4b36-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e4b36-111">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e4b36-111">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="e4b36-112">I feltet **Nummer**</span><span class="sxs-lookup"><span data-stu-id="e4b36-112">In the **No.**</span></span> <span data-ttu-id="e4b36-113">skal du indsætte næste nummer i serien.</span><span class="sxs-lookup"><span data-stu-id="e4b36-113">field, insert the next number in the series.</span></span>  
4.  <span data-ttu-id="e4b36-114">Marker kilden til produktionsordren i feltet **Kildetype**.</span><span class="sxs-lookup"><span data-stu-id="e4b36-114">In the **Source Type** field, select the source of the production order.</span></span>

    <span data-ttu-id="e4b36-115">Her kan du vælge at oprette til en familie af varer.</span><span class="sxs-lookup"><span data-stu-id="e4b36-115">Here you can select to produce for a family of items.</span></span> <span data-ttu-id="e4b36-116">Du kan finde flere oplysninger under [Arbejde med produktionsfamilier](production-how-work-family.md).</span><span class="sxs-lookup"><span data-stu-id="e4b36-116">For more information, see [Work With Production Families](production-how-work-family.md).</span></span>
5.  <span data-ttu-id="e4b36-117">Marker varenummer, familie eller salgshoved, som produktionsordren genereres for, i feltet **Kildenr.**.</span><span class="sxs-lookup"><span data-stu-id="e4b36-117">In the **Source No.** field, select the item number, family, or sales header for which the production order is to be generated.</span></span>  
6.  <span data-ttu-id="e4b36-118">Udfyld felterne **Antal** og **Forfaldsdato** i overensstemmelse med dine specifikationer.</span><span class="sxs-lookup"><span data-stu-id="e4b36-118">Fill in the **Quantity** and **Due Date** fields according to your specifications.</span></span>  

<span data-ttu-id="e4b36-119">Når du ændrer produktionskravene, f.eks. komponenter og operationer, kan du hurtigt omplanlægge produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="e4b36-119">When production requirements change, such as components or operations, you can quickly replan the production order.</span></span> <span data-ttu-id="e4b36-120">Du kan finde flere oplysninger i [Omplanlægge eller forny produktionsordrer direkte](production-how-to-replan-refresh-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="e4b36-120">For more information, see [Replan or Refresh Production Orders Directly](production-how-to-replan-refresh-production-orders.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="e4b36-121">Se også</span><span class="sxs-lookup"><span data-stu-id="e4b36-121">See Also</span></span>  
<span data-ttu-id="e4b36-122">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="e4b36-122">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="e4b36-123">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="e4b36-123">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="e4b36-124">[Planlægning](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="e4b36-124">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="e4b36-125">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="e4b36-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="e4b36-126">Køb</span><span class="sxs-lookup"><span data-stu-id="e4b36-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="e4b36-127">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e4b36-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

