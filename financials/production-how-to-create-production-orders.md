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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0c792dbb7d7261e8f8b89ca4f3d39d875142c4eb
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-production-order-headers"></a><span data-ttu-id="a71cd-103">Sådan oprettes produktionsordrehoveder</span><span class="sxs-lookup"><span data-stu-id="a71cd-103">How to: Create Production Order Headers</span></span>
<span data-ttu-id="a71cd-104">Du kan oprette en produktionsordre manuelt, og det første trin i denne procedure er at oprette et produktionsordrehoved.</span><span class="sxs-lookup"><span data-stu-id="a71cd-104">You can create a production order manually, and the first step is to create a production order header.</span></span>

<span data-ttu-id="a71cd-105">Produktionsordrer oprettes typisk automatisk af en planlægningsfunktion til opfyldning af et kendt behov.</span><span class="sxs-lookup"><span data-stu-id="a71cd-105">Production orders are typically created automatically by a planning function to fulfill a known demand.</span></span> <span data-ttu-id="a71cd-106">Du kan finde flere oplysninger i [Planlægning](production-planning.md).</span><span class="sxs-lookup"><span data-stu-id="a71cd-106">For more information, see [Planning](production-planning.md).</span></span>   

<span data-ttu-id="a71cd-107">I proceduren nedenfor oprettes en fastlagt produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="a71cd-107">In the following procedure, a firm planned production order is created.</span></span> <span data-ttu-id="a71cd-108">Du kan også oprette produktionsordrer med en anden status.</span><span class="sxs-lookup"><span data-stu-id="a71cd-108">You can also create production orders with a different status.</span></span>  

## <a name="to-create-a-production-order-header"></a><span data-ttu-id="a71cd-109">Sådan oprettes et produktionsordrehovede</span><span class="sxs-lookup"><span data-stu-id="a71cd-109">To create a production order header</span></span>  
1.  <span data-ttu-id="a71cd-110">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ordreplanlægning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="a71cd-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a71cd-111">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a71cd-111">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="a71cd-112">I feltet **Nummer**</span><span class="sxs-lookup"><span data-stu-id="a71cd-112">In the **No.**</span></span> <span data-ttu-id="a71cd-113">skal du indsætte næste nummer i serien.</span><span class="sxs-lookup"><span data-stu-id="a71cd-113">field, insert the next number in the series.</span></span>  
4.  <span data-ttu-id="a71cd-114">Marker kilden til produktionsordren i feltet **Kildetype**.</span><span class="sxs-lookup"><span data-stu-id="a71cd-114">In the **Source Type** field, select the source of the production order.</span></span>

    <span data-ttu-id="a71cd-115">Her kan du vælge at oprette til en familie af varer.</span><span class="sxs-lookup"><span data-stu-id="a71cd-115">Here you can select to produce for a family of items.</span></span> <span data-ttu-id="a71cd-116">Du kan finde flere oplysninger under [Fremgangsmåde: Arbejde med produktionsfamilier](production-how-work-family.md).</span><span class="sxs-lookup"><span data-stu-id="a71cd-116">For more information, see [How to: Work With Production Families](production-how-work-family.md).</span></span>
5.  <span data-ttu-id="a71cd-117">Marker varenummer, familie eller salgshoved, som produktionsordren genereres for, i feltet **Kildenr.**.</span><span class="sxs-lookup"><span data-stu-id="a71cd-117">In the **Source No.** field, select the item number, family, or sales header for which the production order is to be generated.</span></span>  
6.  <span data-ttu-id="a71cd-118">Udfyld felterne **Antal** og **Forfaldsdato** i overensstemmelse med dine specifikationer.</span><span class="sxs-lookup"><span data-stu-id="a71cd-118">Fill in the **Quantity** and **Due Date** fields according to your specifications.</span></span>  

<span data-ttu-id="a71cd-119">Når du ændrer produktionskravene, f.eks. komponenter og operationer, kan du hurtigt omplanlægge produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="a71cd-119">When production requirements change, such as components or operations, you can quickly replan the production order.</span></span> <span data-ttu-id="a71cd-120">Du kan finde flere oplysninger i [Fremgangsmåde: Omplanlæg eller forny produktionsordrer direkte](production-how-to-replan-refresh-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="a71cd-120">For more information, see [How to: Replan or Refresh Production Orders Directly](production-how-to-replan-refresh-production-orders.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="a71cd-121">Se også</span><span class="sxs-lookup"><span data-stu-id="a71cd-121">See Also</span></span>  
<span data-ttu-id="a71cd-122">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="a71cd-122">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="a71cd-123">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="a71cd-123">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="a71cd-124">[Planlægning](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="a71cd-124">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="a71cd-125">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="a71cd-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="a71cd-126">Køb</span><span class="sxs-lookup"><span data-stu-id="a71cd-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="a71cd-127">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a71cd-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

