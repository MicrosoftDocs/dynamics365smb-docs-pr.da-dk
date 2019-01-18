---
title: "Designoplysninger – Tilgængelighed i lageret | Microsoft Docs"
description: "Systemet skal holde en konstant kontrol over varedisponering på lageret, så udgående ordrer kan flyde effektivt og levere optimale leverancer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 5fd4bedcef6fcec79b1b2c8744c7c08d8170d97e
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="design-details-availability-in-the-warehouse"></a><span data-ttu-id="e350f-103">Designoplysninger: Tilgængelighed i lageret</span><span class="sxs-lookup"><span data-stu-id="e350f-103">Design Details: Availability in the Warehouse</span></span>
<span data-ttu-id="e350f-104">Systemet skal holde en konstant kontrol over varedisponering på lageret, så udgående ordrer kan flyde effektivt og levere optimale leverancer.</span><span class="sxs-lookup"><span data-stu-id="e350f-104">The system must keep a constant control of item availability in the warehouse, so that outbound orders can flow efficiently and provide optimal deliveries.</span></span>  

 <span data-ttu-id="e350f-105">Tilgængeligheden varierer afhængigt af allokeringer på placeringsniveauet, når lageraktiviteter som pluk og bevægelser forekommer, og når lagerreservationssystemet pålægger begrænsninger, der skal overholdes.</span><span class="sxs-lookup"><span data-stu-id="e350f-105">Availability varies depending on allocations at the bin level when warehouse activities such as picks and movements occur and when the inventory reservation system imposes restrictions to comply with.</span></span> <span data-ttu-id="e350f-106">En meget kompleks algoritme kontrollerer, at alle betingelser er opfyldt, før der tildeles antal til pluk for udgående forløb.</span><span class="sxs-lookup"><span data-stu-id="e350f-106">A rather complex algorithm verifies that all conditions are met before allocating quantities to picks for outbound flows.</span></span>  

## <a name="bin-content-and-reservations"></a><span data-ttu-id="e350f-107">Placeringsindhold og reservationer</span><span class="sxs-lookup"><span data-stu-id="e350f-107">Bin Content and Reservations</span></span>  
 <span data-ttu-id="e350f-108">I en installation af logistik findes vareantal både som lagerposter, i logistikmodulet, og som vareposter i modulet Lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="e350f-108">In any installation of warehouse management, item quantities exist both as warehouse entries, in the Warehouse application area, and as item ledger entries, in the Inventory application area.</span></span> <span data-ttu-id="e350f-109">Disse to typer indeholder forskellige oplysninger om, hvor varer findes, og om de er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="e350f-109">These two entry types contain different information about where items exist and whether they are available.</span></span> <span data-ttu-id="e350f-110">Lagerposter definerer en vares tilgængelighed efter placering og placeringstype, samlet kaldet placeringsindhold.</span><span class="sxs-lookup"><span data-stu-id="e350f-110">Warehouse entries define an item’s availability by bin and bin type, which is called bin content.</span></span> <span data-ttu-id="e350f-111">Vareposter definerer en varedisponering ved sin reservation til udgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="e350f-111">Item ledger entries define an item’s availability by its reservation to outbound documents.</span></span>  

 <span data-ttu-id="e350f-112">Der findes specielle funktioner i pluk-algoritme til beregning af den mængde, der er disponibel til pluk, når placeringsindholdet er kombineret med reservationer.</span><span class="sxs-lookup"><span data-stu-id="e350f-112">Special functionality in the picking algorithm exists to calculate the quantity that is available to pick when bin content is coupled with reservations.</span></span>  

## <a name="quantity-available-to-pick"></a><span data-ttu-id="e350f-113">Mængde, der kan plukkes</span><span class="sxs-lookup"><span data-stu-id="e350f-113">Quantity Available to Pick</span></span>  
 <span data-ttu-id="e350f-114">Hvis for eksempel algoritmen for pluk ikke tager højde for vareantal, der er reserveret til en ventende salgsordreforsendelse, kan disse varer plukkes til en anden salgsordre, der er sendt tidligere, hvilket forhindrer, at det første salg er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="e350f-114">If, for example, the picking algorithm does not consider item quantities that are reserved for a pending sales order shipment, then those items might be picked for another sales order that is shipped earlier, which prevents the first sales from being fulfilled.</span></span> <span data-ttu-id="e350f-115">Hvis du vil undgå denne situation, fratrækker plukalgoritmen antal, der er reserveret til andre udgående dokumenter, antal på eksisterende plukdokumenter og antal, der er plukket, men endnu ikke leveret eller forbrugt.</span><span class="sxs-lookup"><span data-stu-id="e350f-115">To avoid this situation, the picking algorithm subtracts quantities that are reserved for other outbound documents, quantities on existing pick documents, and quantities that are picked but not yet shipped or consumed.</span></span>  

 <span data-ttu-id="e350f-116">Resultatet vises i feltet **Disp. antal til pluk** på siden **Plukkladde**, hvor feltet beregnes dynamisk.</span><span class="sxs-lookup"><span data-stu-id="e350f-116">The result is displayed in the **Available Qty. to Pick** field on the **Pick Worksheet** page, where the field is calculated dynamically.</span></span> <span data-ttu-id="e350f-117">Værdien beregnes også, når brugere opretter lagerpluk direkte for udgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="e350f-117">The value is also calculated when users create warehouse picks directly for outbound documents.</span></span> <span data-ttu-id="e350f-118">Disse udgående dokumenter kan være salgsordrer, produktionsforbrug eller udgående overflytninger, hvor resultatet er afspejlet i de relaterede antalsfelter, f.eks. **Mgd. at håndtere**.</span><span class="sxs-lookup"><span data-stu-id="e350f-118">Such outbound documents could be sales orders, production consumption, or outbound transfers, where the result is reflected in the related quantity fields, such as **Qty. to Handle**.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="e350f-119">Med hensyn til prioriteten af reservationer fratrækkes antallet, der skal reserveres, fra antallet, der er disponibelt til pluk.</span><span class="sxs-lookup"><span data-stu-id="e350f-119">Concerning the priority of reservations, the quantity to reserve is subtracted from the quantity available to pick.</span></span> <span data-ttu-id="e350f-120">Hvis det tilgængelige antal i plukplaceringer f.eks. er 5 enheder, men der er 100 enheder på læg-på-lager-placeringer, vises der en fejlmeddelelse, når du prøver at reservere mere end 5 enheder til en anden ordre, fordi det ekstra antal skal være tilgængeligt på plukplaceringer.</span><span class="sxs-lookup"><span data-stu-id="e350f-120">For example, if the quantity available in pick bins is 5 units, but 100 units are in put-away bins, then when you try to reserve more than 5 units for another order, an error message is displayed because the additional quantity must be available in pick bins.</span></span>  

### <a name="calculating-the-quantity-available-to-pick"></a><span data-ttu-id="e350f-121">Beregning af det antal, der er disponibelt til pluk</span><span class="sxs-lookup"><span data-stu-id="e350f-121">Calculating the Quantity Available to Pick</span></span>  
 <span data-ttu-id="e350f-122">Det antal, der kan plukkes, beregnes sådan:</span><span class="sxs-lookup"><span data-stu-id="e350f-122">The quantity available to pick is calculated as follows:</span></span>  

 <span data-ttu-id="e350f-123">mængde, der kan plukkes = antal i plukplaceringer - antal på pluk og bevægelser – (reserveret antal i plukplaceringer + reserveret antal på pluk og bevægelser)</span><span class="sxs-lookup"><span data-stu-id="e350f-123">quantity available to pick = quantity in pick bins - quantity on picks and movements – (reserved quantity in pick bins + reserved quantity on picks and movements)</span></span>  

 <span data-ttu-id="e350f-124">Følgende diagram viser de forskellige elementer i beregningen.</span><span class="sxs-lookup"><span data-stu-id="e350f-124">The following diagram shows the different elements of the calculation.</span></span>  

 <span data-ttu-id="e350f-125">![Disponibel til pluk med reservationsoverlap](media/design_details_warehouse_management_availability_2.png "Disponibel til pluk med reservationsoverlap")</span><span class="sxs-lookup"><span data-stu-id="e350f-125">![Available to pick with reservation overlap](media/design_details_warehouse_management_availability_2.png "Available to pick with reservation overlap")</span></span>  

## <a name="quantity-available-to-reserve"></a><span data-ttu-id="e350f-126">Antal disponible til reservation</span><span class="sxs-lookup"><span data-stu-id="e350f-126">Quantity Available to Reserve</span></span>  
 <span data-ttu-id="e350f-127">Da begreberne om placeringsindhold og reservation eksisterer side om side, skal antallet af varer, der kan reserveres, justeres med fordelinger på udgående lagerdokumenter.</span><span class="sxs-lookup"><span data-stu-id="e350f-127">Because the concepts of bin content and reservation co-exist, the quantity of items that are available to reserve must be aligned with allocations to outbound warehouse documents.</span></span>  

 <span data-ttu-id="e350f-128">Det bør være muligt at reservere alle varer på lager, bortset fra dem, der har startet udgående behandling.</span><span class="sxs-lookup"><span data-stu-id="e350f-128">It should be possible to reserve all items in inventory, except those that have started outbound processing.</span></span> <span data-ttu-id="e350f-129">Derfor defineres det antal, der kan reserveres, som antallet på alle dokumenter og alle placeringstyper, undtagen følgende udgående mængder:</span><span class="sxs-lookup"><span data-stu-id="e350f-129">Accordingly, the quantity that is available to reserve is defined as the quantity on all documents and all bin types, except the following outbound quantities:</span></span>  

-   <span data-ttu-id="e350f-130">Antal på uregistrerede plukdokumenter</span><span class="sxs-lookup"><span data-stu-id="e350f-130">Quantity on unregistered pick documents</span></span>  
-   <span data-ttu-id="e350f-131">Antal på forsendelsesplaceringer</span><span class="sxs-lookup"><span data-stu-id="e350f-131">Quantity in shipment bins</span></span>  
-   <span data-ttu-id="e350f-132">Antal til produktionsplaceringer</span><span class="sxs-lookup"><span data-stu-id="e350f-132">Quantity in to-production bins</span></span>  
-   <span data-ttu-id="e350f-133">Antal åbne produktionsplaceringer</span><span class="sxs-lookup"><span data-stu-id="e350f-133">Quantity in open shop floor bins</span></span>  
-   <span data-ttu-id="e350f-134">Antal til montageplaceringer</span><span class="sxs-lookup"><span data-stu-id="e350f-134">Quantity in to-assembly bins</span></span>  
-   <span data-ttu-id="e350f-135">Antal på reguleringsplaceringer</span><span class="sxs-lookup"><span data-stu-id="e350f-135">Quantity in adjustment bins</span></span>  

 <span data-ttu-id="e350f-136">Resultatet vises i feltet **Beholdning i alt** på siden **Reservation**.</span><span class="sxs-lookup"><span data-stu-id="e350f-136">The result is displayed in the **Total Available Quantity** field on the **Reservation** page.</span></span>  

 <span data-ttu-id="e350f-137">På en reservationslinje vises det antal, der ikke kan reserveres, fordi det er fordelt i lageret, i feltet **Allokeret antal på lager** på siden **Reservation**.</span><span class="sxs-lookup"><span data-stu-id="e350f-137">On a reservation line, the quantity that cannot be reserved, because it is allocated in the warehouse, is displayed in the **Qty. Allocated in Warehouse** field on the **Reservation** page.</span></span>  

### <a name="calculating-the-quantity-available-to-reserve"></a><span data-ttu-id="e350f-138">Beregning af det antal, der er disponibelt til reservation</span><span class="sxs-lookup"><span data-stu-id="e350f-138">Calculating the Quantity Available to Reserve</span></span>  
 <span data-ttu-id="e350f-139">Det antal, der kan reserveres, beregnes sådan:</span><span class="sxs-lookup"><span data-stu-id="e350f-139">The quantity available to reserve is calculated as follows:</span></span>  

 <span data-ttu-id="e350f-140">mængde, der kan reserveres = samlet antal på lager - antal på pluk og bevægelser for kildedokumenter - reserveret antal - antal i udgående placeringer</span><span class="sxs-lookup"><span data-stu-id="e350f-140">quantity available to reserve = total quantity in inventory - quantity on picks and movements for source documents - reserved quantity - quantity in outbound bins</span></span>  

 <span data-ttu-id="e350f-141">Følgende diagram viser de forskellige elementer i beregningen.</span><span class="sxs-lookup"><span data-stu-id="e350f-141">The following diagram shows the different elements of the calculation.</span></span>  

 <span data-ttu-id="e350f-142">![Disponibel til reservation pr. lagerstedsallokering](media/design_details_warehouse_management_availability_3.png "Disponibel til reservation pr. lagerstedsallokering")</span><span class="sxs-lookup"><span data-stu-id="e350f-142">![Avaliable to reserve per warehouse allocation](media/design_details_warehouse_management_availability_3.png "Avaliable to reserve per warehouse allocation")</span></span>  

## <a name="see-also"></a><span data-ttu-id="e350f-143">Se også</span><span class="sxs-lookup"><span data-stu-id="e350f-143">See Also</span></span>  
 [<span data-ttu-id="e350f-144">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="e350f-144">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)

