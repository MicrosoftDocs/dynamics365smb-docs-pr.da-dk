---
title: "Sådan spores relationer mellem behov og forsyning | Microsoft Docs"
description: "Fra ethvert forsynings- eller behovsdokument i det såkaldte ordrenetværk, kan du spore ordrebehov (sporet antal), forecast, rammesalgsordre eller planlægningsparameter (ikkesporet antal), der er årsag til den pågældende planlægningslinje."
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 511381e4f6d469ff16714a30fde60d3e238ad975
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-track-relations-between-demand-and-supply"></a><span data-ttu-id="b1514-103">Fremgangsmåde: Spore relationer mellem behov og forsyning</span><span class="sxs-lookup"><span data-stu-id="b1514-103">How to: Track Relations Between Demand and Supply</span></span>
<span data-ttu-id="b1514-104">Fra ethvert forsynings- eller behovsdokument i det såkaldte ordrenetværk, kan du spore ordrebehov (sporet antal), forecast, rammesalgsordre eller planlægningsparameter (ikkesporet antal), der er årsag til den pågældende planlægningslinje.</span><span class="sxs-lookup"><span data-stu-id="b1514-104">From any supply or demand document in the so-called order network, you can track the order demand (tracked quantity), forecast, blanket sales order, or planning parameter (untracked quantity) that has given rise to the planning line in question.</span></span>

<span data-ttu-id="b1514-105">Planlægningskladderne indeholder også yderligere planlægningsoplysninger om ikke-ordreenheder for at hjælpe planlæggeren med at opnå den optimale forsyningsplan.</span><span class="sxs-lookup"><span data-stu-id="b1514-105">The planning worksheets also offers supporting planning information about non-order entities to help the planner obtain an optimal supply plan.</span></span> <span data-ttu-id="b1514-106">Du kan finde flere oplysninger i afsnittet "Ikke-sporede planlægningselementer".</span><span class="sxs-lookup"><span data-stu-id="b1514-106">For more information, see the "Untracked Planning Elements" section.</span></span>

## <a name="to-track-linked-items"></a><span data-ttu-id="b1514-107">Sådan spores tilknyttede varer</span><span class="sxs-lookup"><span data-stu-id="b1514-107">To track linked items</span></span>
<span data-ttu-id="b1514-108">Ordresporing viser, hvordan salgsordrer, produktionsordrer og købsordrer er relaterede til produktionsordrer via planlægnings- og reservationssystemerne.</span><span class="sxs-lookup"><span data-stu-id="b1514-108">Order tracking shows how sales orders, production orders, and purchase orders are related to the manufacturing order through the planning and reservation systems.</span></span>

<span data-ttu-id="b1514-109">Nedenstående beskrives, hvordan tilknyttede varer spores på en fastlagt produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="b1514-109">The following describes how to track linked items on a firm planned production order.</span></span> <span data-ttu-id="b1514-110">Trinene er de samme for alle andre typer og i forbindelse med planlægningskladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="b1514-110">The steps are similar for all other order types, and from planning worksheet lines.</span></span>

1. <span data-ttu-id="b1514-111">Vælg ikonet ![Søg efter side eller en rapport](media/ui-search/search_small.png "Søg efter side eller en rapport ikonet"), angiv **Fastlagt produktionsordre**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="b1514-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Order**, and then choose the related link.</span></span>
2. <span data-ttu-id="b1514-112">Åbn den relevante fastlagte produktionsordre på listen.</span><span class="sxs-lookup"><span data-stu-id="b1514-112">Open the relevant firm planned production order from the list.</span></span>
3. <span data-ttu-id="b1514-113">I oversigtspanelet **Linjer** skal du vælge handlingen **Funktioner** og derefter vælge handlingen **Ordresporing**.</span><span class="sxs-lookup"><span data-stu-id="b1514-113">On the **Lines** FastTab, choose the **Functions** action, and then choose the **Order Tracking** action.</span></span>

<span data-ttu-id="b1514-114">På linjerne i vinduet **Ordresporing** vises de bilag, der har relation til den aktuelle produktionsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="b1514-114">The lines in the **Order Tracking** display the documents that are related to the current production order line.</span></span>

## <a name="untracked-planning-elements"></a><span data-ttu-id="b1514-115">Ikke-sporede planlægningselementer</span><span class="sxs-lookup"><span data-stu-id="b1514-115">Untracked Planning Elements</span></span>
<span data-ttu-id="b1514-116">Vinduet **Ikke-sporede planlægningselementer** åbnes, når du klikker på feltet **Ikke-sporet antal** i vinduet **Ordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="b1514-116">The **Untracked Planning Elements** window opens when you choose the **Untracked Qty.** field in the **order Planning** window.</span></span> <span data-ttu-id="b1514-117">Det tjener to formål:</span><span class="sxs-lookup"><span data-stu-id="b1514-117">It serves two purposes:</span></span>

1. <span data-ttu-id="b1514-118">Indeholde oplysninger om ikke-sporet antal, der vises, når brugeren slår op fra vinduet Ordresporing for at få vist ikke-sporede antal.</span><span class="sxs-lookup"><span data-stu-id="b1514-118">To hold information about untracked quantities displayed when the user looks up from the Order Tracking window to see untracked quantities.</span></span>
2. <span data-ttu-id="b1514-119">Det skal indeholde advarselsmeddelelser, der vises, når brugeren vælge ikonet **Advarsel** i vinduet **Planlægningskladde**.</span><span class="sxs-lookup"><span data-stu-id="b1514-119">To hold warning messages displayed when the user chooses the **Warning** icon in the **Planning Worksheet** window.</span></span>

<span data-ttu-id="b1514-120">Vinduet indeholder poster, der tager højde for et ikke-sporet overskudsantal i ordresporingsnetværket.</span><span class="sxs-lookup"><span data-stu-id="b1514-120">The window contains entries which account for an untracked surplus quantity in order tracking network.</span></span> <span data-ttu-id="b1514-121">Disse poster genereres i forbindelse med planlægningskørslen og forklarer, hvor det ikke-sporede overskud på ordresporingslinjerne stammer fra.</span><span class="sxs-lookup"><span data-stu-id="b1514-121">These entries are generated during the planning run and explain where the untracked surplus quantity in the order tracking lines came from.</span></span> <span data-ttu-id="b1514-122">Det ikke-sporede overskud kan stamme fra:</span><span class="sxs-lookup"><span data-stu-id="b1514-122">This untracked surplus can come from:</span></span>

- <span data-ttu-id="b1514-123">Produktionsforecast</span><span class="sxs-lookup"><span data-stu-id="b1514-123">Production forecast</span></span>
- <span data-ttu-id="b1514-124">Rammeordrer</span><span class="sxs-lookup"><span data-stu-id="b1514-124">Blanket orders</span></span>
- <span data-ttu-id="b1514-125">Sikkerhedslager</span><span class="sxs-lookup"><span data-stu-id="b1514-125">Safety stock quantity</span></span>
- <span data-ttu-id="b1514-126">Genbestillingspunkt</span><span class="sxs-lookup"><span data-stu-id="b1514-126">Reorder point</span></span>
- <span data-ttu-id="b1514-127">Maks. lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="b1514-127">Maximum inventory</span></span>
- <span data-ttu-id="b1514-128">Ordrekvantum</span><span class="sxs-lookup"><span data-stu-id="b1514-128">Reorder quantity</span></span>
- <span data-ttu-id="b1514-129">Maks. ordrestørrelse</span><span class="sxs-lookup"><span data-stu-id="b1514-129">Maximum order quantity</span></span>
- <span data-ttu-id="b1514-130">Min. ordrestørrelse</span><span class="sxs-lookup"><span data-stu-id="b1514-130">Minimum order quantity</span></span>
- <span data-ttu-id="b1514-131">Oprundingsfaktor</span><span class="sxs-lookup"><span data-stu-id="b1514-131">Order multiple</span></span>
- <span data-ttu-id="b1514-132">Aktionsgrænse (% af lotstr.)</span><span class="sxs-lookup"><span data-stu-id="b1514-132">Dampener (% of lot size)</span></span>

## <a name="see-also"></a><span data-ttu-id="b1514-133">Se også</span><span class="sxs-lookup"><span data-stu-id="b1514-133">See Also</span></span>  
<span data-ttu-id="b1514-134">[Planlægning](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="b1514-134">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="b1514-135">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="b1514-135">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="b1514-136">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="b1514-136">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="b1514-137">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="b1514-137">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="b1514-138">Køb</span><span class="sxs-lookup"><span data-stu-id="b1514-138">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="b1514-139">Designoplysninger: Reservation, sporing og aktionsmeddelelser</span><span class="sxs-lookup"><span data-stu-id="b1514-139">Design Details: Reservation, Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
<span data-ttu-id="b1514-140">[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="b1514-140">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="b1514-141">Konfigurere bedste fremgangsmåder: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="b1514-141">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="b1514-142">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b1514-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

