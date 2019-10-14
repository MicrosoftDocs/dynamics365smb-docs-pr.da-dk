---
title: Designoplysninger – Tilgængelighed i lageret | Microsoft Docs
description: Systemet skal holde en konstant kontrol over varedisponering på lageret, så udgående ordrer kan flyde effektivt og levere optimale leverancer.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 67e30773683fbf8497a1668e1c4ca3d176e0781e
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303792"
---
# <a name="design-details-availability-in-the-warehouse"></a><span data-ttu-id="43077-103">Designoplysninger: Tilgængelighed i lageret</span><span class="sxs-lookup"><span data-stu-id="43077-103">Design Details: Availability in the Warehouse</span></span>
<span data-ttu-id="43077-104">Systemet skal holde en konstant kontrol over varedisponering på lageret, så udgående ordrer kan flyde effektivt og levere optimale leverancer.</span><span class="sxs-lookup"><span data-stu-id="43077-104">The system must keep a constant control of item availability in the warehouse, so that outbound orders can flow efficiently and provide optimal deliveries.</span></span>  

<span data-ttu-id="43077-105">Tilgængeligheden varierer afhængigt af allokeringer på placeringsniveauet, når lageraktiviteter som pluk og bevægelser forekommer, og når lagerreservationssystemet pålægger begrænsninger, der skal overholdes.</span><span class="sxs-lookup"><span data-stu-id="43077-105">Availability varies depending on allocations at the bin level when warehouse activities such as picks and movements occur and when the inventory reservation system imposes restrictions to comply with.</span></span> <span data-ttu-id="43077-106">En meget kompleks algoritme kontrollerer, at alle betingelser er opfyldt, før der tildeles antal til pluk for udgående forløb.</span><span class="sxs-lookup"><span data-stu-id="43077-106">A rather complex algorithm verifies that all conditions are met before allocating quantities to picks for outbound flows.</span></span>

<span data-ttu-id="43077-107">Hvis en eller flere af betingelserne ikke er opfyldt, kan der vises forskellige fejlmeddelelser, herunder "Der er intet at håndtere"</span><span class="sxs-lookup"><span data-stu-id="43077-107">If one or more conditions are not met, different error messages can be shown, including the generic "Nothing to handle."</span></span> <span data-ttu-id="43077-108">.</span><span class="sxs-lookup"><span data-stu-id="43077-108">message.</span></span> <span data-ttu-id="43077-109">Meddelelsen "Der er intet at håndtere"</span><span class="sxs-lookup"><span data-stu-id="43077-109">The "Nothing to handle."</span></span> <span data-ttu-id="43077-110">kan blive vist af mange forskellige årsager, både i udgående og indgående strømme, hvor en direkte eller indirekte anvendt bilagslinje indeholder feltet **Håndteringsantal**.</span><span class="sxs-lookup"><span data-stu-id="43077-110">message can occur for many different reasons, both in outbound and inbound flows, where a directly or indirectly involved document line contains the **Qty. to Handle** field.</span></span>

> [!NOTE]
> <span data-ttu-id="43077-111">Der bliver snart publiceret oplysninger her om mulige årsager og løsninger til "Der er intet at håndtere".</span><span class="sxs-lookup"><span data-stu-id="43077-111">Information will soon be published here about possible reasons and solutions for the "Nothing to handle."</span></span> <span data-ttu-id="43077-112">.</span><span class="sxs-lookup"><span data-stu-id="43077-112">message.</span></span>

## <a name="bin-content-and-reservations"></a><span data-ttu-id="43077-113">Placeringsindhold og reservationer</span><span class="sxs-lookup"><span data-stu-id="43077-113">Bin Content and Reservations</span></span>  
 <span data-ttu-id="43077-114">I en installation af logistik findes vareantal både som lagerposter, i logistikmodulet, og som vareposter i modulet Lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="43077-114">In any installation of warehouse management, item quantities exist both as warehouse entries, in the Warehouse application area, and as item ledger entries, in the Inventory application area.</span></span> <span data-ttu-id="43077-115">Disse to typer indeholder forskellige oplysninger om, hvor varer findes, og om de er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="43077-115">These two entry types contain different information about where items exist and whether they are available.</span></span> <span data-ttu-id="43077-116">Lagerposter definerer en vares tilgængelighed efter placering og placeringstype, samlet kaldet placeringsindhold.</span><span class="sxs-lookup"><span data-stu-id="43077-116">Warehouse entries define an item’s availability by bin and bin type, which is called bin content.</span></span> <span data-ttu-id="43077-117">Vareposter definerer en varedisponering ved sin reservation til udgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="43077-117">Item ledger entries define an item’s availability by its reservation to outbound documents.</span></span>  

 <span data-ttu-id="43077-118">Der findes specielle funktioner i pluk-algoritme til beregning af den mængde, der er disponibel til pluk, når placeringsindholdet er kombineret med reservationer.</span><span class="sxs-lookup"><span data-stu-id="43077-118">Special functionality in the picking algorithm exists to calculate the quantity that is available to pick when bin content is coupled with reservations.</span></span>  

## <a name="quantity-available-to-pick"></a><span data-ttu-id="43077-119">Mængde, der kan plukkes</span><span class="sxs-lookup"><span data-stu-id="43077-119">Quantity Available to Pick</span></span>  
 <span data-ttu-id="43077-120">Hvis for eksempel algoritmen for pluk ikke tager højde for vareantal, der er reserveret til en ventende salgsordreforsendelse, kan disse varer plukkes til en anden salgsordre, der er sendt tidligere, hvilket forhindrer, at det første salg er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="43077-120">If, for example, the picking algorithm does not consider item quantities that are reserved for a pending sales order shipment, then those items might be picked for another sales order that is shipped earlier, which prevents the first sales from being fulfilled.</span></span> <span data-ttu-id="43077-121">Hvis du vil undgå denne situation, fratrækker plukalgoritmen antal, der er reserveret til andre udgående dokumenter, antal på eksisterende plukdokumenter og antal, der er plukket, men endnu ikke leveret eller forbrugt.</span><span class="sxs-lookup"><span data-stu-id="43077-121">To avoid this situation, the picking algorithm subtracts quantities that are reserved for other outbound documents, quantities on existing pick documents, and quantities that are picked but not yet shipped or consumed.</span></span>  

 <span data-ttu-id="43077-122">Resultatet vises i feltet **Disp. antal til pluk** på siden **Plukkladde**, hvor feltet beregnes dynamisk.</span><span class="sxs-lookup"><span data-stu-id="43077-122">The result is displayed in the **Available Qty. to Pick** field on the **Pick Worksheet** page, where the field is calculated dynamically.</span></span> <span data-ttu-id="43077-123">Værdien beregnes også, når brugere opretter lagerpluk direkte for udgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="43077-123">The value is also calculated when users create warehouse picks directly for outbound documents.</span></span> <span data-ttu-id="43077-124">Disse udgående dokumenter kan være salgsordrer, produktionsforbrug eller udgående overflytninger, hvor resultatet er afspejlet i de relaterede antalsfelter, f.eks. **Mgd. at håndtere**.</span><span class="sxs-lookup"><span data-stu-id="43077-124">Such outbound documents could be sales orders, production consumption, or outbound transfers, where the result is reflected in the related quantity fields, such as **Qty. to Handle**.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="43077-125">Med hensyn til prioriteten af reservationer fratrækkes antallet, der skal reserveres, fra antallet, der er disponibelt til pluk.</span><span class="sxs-lookup"><span data-stu-id="43077-125">Concerning the priority of reservations, the quantity to reserve is subtracted from the quantity available to pick.</span></span> <span data-ttu-id="43077-126">Hvis det tilgængelige antal i plukplaceringer f.eks. er 5 enheder, men der er 100 enheder på læg-på-lager-placeringer, vises der en fejlmeddelelse, når du prøver at reservere mere end 5 enheder til en anden ordre, fordi det ekstra antal skal være tilgængeligt på plukplaceringer.</span><span class="sxs-lookup"><span data-stu-id="43077-126">For example, if the quantity available in pick bins is 5 units, but 100 units are in put-away bins, then when you try to reserve more than 5 units for another order, an error message is displayed because the additional quantity must be available in pick bins.</span></span>  

### <a name="calculating-the-quantity-available-to-pick"></a><span data-ttu-id="43077-127">Beregning af det antal, der er disponibelt til pluk</span><span class="sxs-lookup"><span data-stu-id="43077-127">Calculating the Quantity Available to Pick</span></span>  
 <span data-ttu-id="43077-128">Det antal, der kan plukkes, beregnes sådan:</span><span class="sxs-lookup"><span data-stu-id="43077-128">The quantity available to pick is calculated as follows:</span></span>  

 <span data-ttu-id="43077-129">mængde, der kan plukkes = antal i plukplaceringer - antal på pluk og bevægelser – (reserveret antal i plukplaceringer + reserveret antal på pluk og bevægelser)</span><span class="sxs-lookup"><span data-stu-id="43077-129">quantity available to pick = quantity in pick bins - quantity on picks and movements – (reserved quantity in pick bins + reserved quantity on picks and movements)</span></span>  

 <span data-ttu-id="43077-130">Følgende diagram viser de forskellige elementer i beregningen.</span><span class="sxs-lookup"><span data-stu-id="43077-130">The following diagram shows the different elements of the calculation.</span></span>  

 <span data-ttu-id="43077-131">![Disponibel til pluk med reservationsoverlap](media/design_details_warehouse_management_availability_2.png "Disponibel til pluk med reservationsoverlap")</span><span class="sxs-lookup"><span data-stu-id="43077-131">![Available to pick with reservation overlap](media/design_details_warehouse_management_availability_2.png "Available to pick with reservation overlap")</span></span>  

## <a name="quantity-available-to-reserve"></a><span data-ttu-id="43077-132">Antal disponible til reservation</span><span class="sxs-lookup"><span data-stu-id="43077-132">Quantity Available to Reserve</span></span>  
 <span data-ttu-id="43077-133">Da begreberne om placeringsindhold og reservation eksisterer side om side, skal antallet af varer, der kan reserveres, justeres med fordelinger på udgående lagerdokumenter.</span><span class="sxs-lookup"><span data-stu-id="43077-133">Because the concepts of bin content and reservation co-exist, the quantity of items that are available to reserve must be aligned with allocations to outbound warehouse documents.</span></span>  

 <span data-ttu-id="43077-134">Det bør være muligt at reservere alle varer på lager, bortset fra dem, der har startet udgående behandling.</span><span class="sxs-lookup"><span data-stu-id="43077-134">It should be possible to reserve all items in inventory, except those that have started outbound processing.</span></span> <span data-ttu-id="43077-135">Derfor defineres det antal, der kan reserveres, som antallet på alle dokumenter og alle placeringstyper, undtagen følgende udgående mængder:</span><span class="sxs-lookup"><span data-stu-id="43077-135">Accordingly, the quantity that is available to reserve is defined as the quantity on all documents and all bin types, except the following outbound quantities:</span></span>  

-   <span data-ttu-id="43077-136">Antal på uregistrerede plukdokumenter</span><span class="sxs-lookup"><span data-stu-id="43077-136">Quantity on unregistered pick documents</span></span>  
-   <span data-ttu-id="43077-137">Antal på forsendelsesplaceringer</span><span class="sxs-lookup"><span data-stu-id="43077-137">Quantity in shipment bins</span></span>  
-   <span data-ttu-id="43077-138">Antal til produktionsplaceringer</span><span class="sxs-lookup"><span data-stu-id="43077-138">Quantity in to-production bins</span></span>  
-   <span data-ttu-id="43077-139">Antal åbne produktionsplaceringer</span><span class="sxs-lookup"><span data-stu-id="43077-139">Quantity in open shop floor bins</span></span>  
-   <span data-ttu-id="43077-140">Antal til montageplaceringer</span><span class="sxs-lookup"><span data-stu-id="43077-140">Quantity in to-assembly bins</span></span>  
-   <span data-ttu-id="43077-141">Antal på reguleringsplaceringer</span><span class="sxs-lookup"><span data-stu-id="43077-141">Quantity in adjustment bins</span></span>  

 <span data-ttu-id="43077-142">Resultatet vises i feltet **Beholdning i alt** på siden **Reservation**.</span><span class="sxs-lookup"><span data-stu-id="43077-142">The result is displayed in the **Total Available Quantity** field on the **Reservation** page.</span></span>  

 <span data-ttu-id="43077-143">På en reservationslinje vises det antal, der ikke kan reserveres, fordi det er fordelt i lageret, i feltet **Allokeret antal på lager** på siden **Reservation**.</span><span class="sxs-lookup"><span data-stu-id="43077-143">On a reservation line, the quantity that cannot be reserved, because it is allocated in the warehouse, is displayed in the **Qty. Allocated in Warehouse** field on the **Reservation** page.</span></span>  

### <a name="calculating-the-quantity-available-to-reserve"></a><span data-ttu-id="43077-144">Beregning af det antal, der er disponibelt til reservation</span><span class="sxs-lookup"><span data-stu-id="43077-144">Calculating the Quantity Available to Reserve</span></span>  
 <span data-ttu-id="43077-145">Det antal, der kan reserveres, beregnes sådan:</span><span class="sxs-lookup"><span data-stu-id="43077-145">The quantity available to reserve is calculated as follows:</span></span>  

 <span data-ttu-id="43077-146">mængde, der kan reserveres = samlet antal på lager - antal på pluk og bevægelser for kildedokumenter - reserveret antal - antal i udgående placeringer</span><span class="sxs-lookup"><span data-stu-id="43077-146">quantity available to reserve = total quantity in inventory - quantity on picks and movements for source documents - reserved quantity - quantity in outbound bins</span></span>  

 <span data-ttu-id="43077-147">Følgende diagram viser de forskellige elementer i beregningen.</span><span class="sxs-lookup"><span data-stu-id="43077-147">The following diagram shows the different elements of the calculation.</span></span>  

 <span data-ttu-id="43077-148">![Disponibel til reservation pr. lagerstedsallokering](media/design_details_warehouse_management_availability_3.png "Disponibel til reservation pr. lagerstedsallokering")</span><span class="sxs-lookup"><span data-stu-id="43077-148">![Avaliable to reserve per warehouse allocation](media/design_details_warehouse_management_availability_3.png "Avaliable to reserve per warehouse allocation")</span></span>  

## <a name="see-also"></a><span data-ttu-id="43077-149">Se også</span><span class="sxs-lookup"><span data-stu-id="43077-149">See Also</span></span>  
 [<span data-ttu-id="43077-150">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="43077-150">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
 [<span data-ttu-id="43077-151">Vise varedisponering</span><span class="sxs-lookup"><span data-stu-id="43077-151">View the Availability of Items</span></span>](inventory-how-availability-overview.md)
