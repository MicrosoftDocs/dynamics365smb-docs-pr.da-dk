---
title: "Forsyningsplanlægning | Microsoft Docs"
description: Opret en detaljeret, eksekverbar plan og produktionsplanen med endelig montage til salgs- og produktionsbehov.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b2a4a682100b0963b540f6f032c4b90061265cc1
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="planning"></a><span data-ttu-id="b489a-103">Planlægning</span><span class="sxs-lookup"><span data-stu-id="b489a-103">Planning</span></span>
<span data-ttu-id="b489a-104">De produktionsoperationer, der kræves for at omdanne tilgange til færdigvarer, skal planlægges dagligt eller ugentligt afhængigt af produkternes omfang og egenskaber.</span><span class="sxs-lookup"><span data-stu-id="b489a-104">The production operations required to transform inputs into finished goods must be planned daily or weekly depending on the volume and nature of the products.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="b489a-105"> indeholder funktioner til levering af forventet og faktisk behov fra salg, montage og produktion samt funktioner til distributionsplanlægning ved hjælp af lagervarer og overflytning af lokationer.</span><span class="sxs-lookup"><span data-stu-id="b489a-105"> offers features to supply for anticipated and actual demand from sale, assembly, and production as well as features for distribution planning using stockkeeping units and location transfers.</span></span>

> [!NOTE]
> <span data-ttu-id="b489a-106">I dette emne beskrives primært planlægning for virksomheder, der er involveret i produktion eller montagestyring, hvor de resulterende forsyningsordrer kan være enten produktion, montage, overflytning eller købsordrer.</span><span class="sxs-lookup"><span data-stu-id="b489a-106">This topic mainly describes planning for companies involved in manufacturing or assembly management where the resulting supply orders can be either production, assembly, transfer, or purchase orders.</span></span> <span data-ttu-id="b489a-107">Den primære brugergrænseflade for dette planlægningsarbejde er vinduet **Planlægningskladde**.</span><span class="sxs-lookup"><span data-stu-id="b489a-107">The main interface for this planning work is the **Planning Worksheet** window.</span></span>

> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="b489a-108"> understøtter også forsyningsplanlægning for engrosvirksomheder, hvor de oprettede forsyningsordrer kun være overførsels- og købsordrer.</span><span class="sxs-lookup"><span data-stu-id="b489a-108"> also supports supply planning for wholesale companies where the resulting supply orders can only be transfer and purchase orders.</span></span> <span data-ttu-id="b489a-109">Den primære brugergrænseflade for dette planlægningsarbejde er vinduet **Indkøbskladde**, som beskrives indirekte i dette emne, da de fleste planlægningsfunktioner gælder for begge kladder.</span><span class="sxs-lookup"><span data-stu-id="b489a-109">The main interface for this planning work is the **Requisition Worksheet** window, which is described indirectly in this topic as most planning functionality applies to both worksheets.</span></span>

<span data-ttu-id="b489a-110">Før du planlægger og udfører produktionsordrer, skal du konfigurere produktionskapaciteter, f.eks. oprette produktionskalendere, ruter, produktionsstyklister og produktionsprocesser.</span><span class="sxs-lookup"><span data-stu-id="b489a-110">Before you can plan and execute production orders, you must configure production capacities, such as creating shop calendars, routings, production BOMs, and machine centers.</span></span> <span data-ttu-id="b489a-111">Du kan finde flere oplysninger i [Konfigurere produktion](production-configure-production-processes.md).</span><span class="sxs-lookup"><span data-stu-id="b489a-111">For more information, see [Setting Up Manufacturing](production-configure-production-processes.md).</span></span>

<span data-ttu-id="b489a-112">Planlægning kan betragtes som forberedelsen af forsyningsordrer i montage- eller produktionsafdelinger til at imødekomme behov.</span><span class="sxs-lookup"><span data-stu-id="b489a-112">Planning can be seen as the preparation required supply orders in the assembly or manufacturing departments to fulfill demand.</span></span> <span data-ttu-id="b489a-113">Du kan finde flere oplysninger i [Montagestyring](assembly-assemble-items.md) og [Produktion](production-manage-manufacturing.md).</span><span class="sxs-lookup"><span data-stu-id="b489a-113">For more information, see [Assembly Management](assembly-assemble-items.md) and [Manufacturing](production-manage-manufacturing.md).</span></span>

<span data-ttu-id="b489a-114">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="b489a-114">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="b489a-115">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="b489a-115">**To**</span></span>|<span data-ttu-id="b489a-116">**Se**</span><span class="sxs-lookup"><span data-stu-id="b489a-116">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="b489a-117">Få er kort introduktion til, hvordan planlægningssystemet kan bruges til at registrere og prioritere behov og foreslå en afstemt forsyningsplan.</span><span class="sxs-lookup"><span data-stu-id="b489a-117">Get a brief introduction to how the planning system can be used to detect and prioritize demand and suggest a balanced supply plan.</span></span>|[<span data-ttu-id="b489a-118">Om planlægningsfunktionen</span><span class="sxs-lookup"><span data-stu-id="b489a-118">About Planning Functionality</span></span>](production-about-planning-functionality.md)|
|<span data-ttu-id="b489a-119">Forstå, hvordan alle aspekter af planlægningssystemet fungerer, og hvordan du justerer algoritmer for at opfylde planlægningsbehov i forskellige miljøer.</span><span class="sxs-lookup"><span data-stu-id="b489a-119">Understand how all aspects of the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span>|[<span data-ttu-id="b489a-120">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="b489a-120">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)|
|<span data-ttu-id="b489a-121">Vide, hvordan planlægningslogikken differentierer mellem behov på lokationer i henhold til lagervareopsætningen og behov uden lokationskoder.</span><span class="sxs-lookup"><span data-stu-id="b489a-121">Learn how the planning logic differentiates between demand at locations according to the SKU setup and demand without location codes.</span></span>|[<span data-ttu-id="b489a-122">Planlægge med eller uden lokationer</span><span class="sxs-lookup"><span data-stu-id="b489a-122">Planning With or Without Locations</span></span>](production-planning-with-without-locations.md)|
|<span data-ttu-id="b489a-123">Lave et forecast over produktionsbehov afledt af de forventede salgs- og produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="b489a-123">Forecast production demand presented by expected sales and production orders.</span></span>|[<span data-ttu-id="b489a-124">Fremgangsmåde: Oprette et produktionsforecast</span><span class="sxs-lookup"><span data-stu-id="b489a-124">How to: Create a Production Forecast</span></span>](production-how-to-create-a-forecast.md)|  
|<span data-ttu-id="b489a-125">Oprette en-til-en-produktionsordrer automatisk fra en salgsordre for at dække det nøjagtige behov for denne salgsordreline.</span><span class="sxs-lookup"><span data-stu-id="b489a-125">Create one-to-one production orders automatically from a sales order to cover the exact demand of that sales order line.</span></span>|[<span data-ttu-id="b489a-126">Fremgangsmåde: Oprette produktionsordrer fra salgsordrer</span><span class="sxs-lookup"><span data-stu-id="b489a-126">How to: Create Production Orders from Sales Orders</span></span>](production-how-to-create-production-orders-from-sales-orders.md)|
|<span data-ttu-id="b489a-127">Oprette en projektproduktionsordre direkte fra en salgsordre med flere linjer, som udgør et produktionsprojekt.</span><span class="sxs-lookup"><span data-stu-id="b489a-127">Create a project production order directly from a multiline sales order representing a production project.</span></span>|[<span data-ttu-id="b489a-128">Fremgangsmåde: Planlægge projektordrer</span><span class="sxs-lookup"><span data-stu-id="b489a-128">How to: Plan Project Orders</span></span>](production-how-to-plan-project-orders.md)|
|<span data-ttu-id="b489a-129">Bruge vinduet **Ordreplanlægning** til manuel planlægning af salgs- eller produktionsbehov for et styklisteniveau ad gangen.</span><span class="sxs-lookup"><span data-stu-id="b489a-129">Use the **Order Planning** window to manually plan for sales or production demand one production BOM level at a time.</span></span>|[<span data-ttu-id="b489a-130">Fremgangsmåde: Planlægge efter nyt behov ordre for ordre</span><span class="sxs-lookup"><span data-stu-id="b489a-130">How to: Plan for New Demand Order by Order</span></span>](production-how-to-plan-for-new-demand.md)|
|<span data-ttu-id="b489a-131">Brug vinduet **Planlægningskladde** til at køre både MPS- og MRP-funktionerne for automatisk at oprette enten en overordnet eller en detaljeret forsyningsplan på alle vareniveauer.</span><span class="sxs-lookup"><span data-stu-id="b489a-131">Use the **Planning Worksheet** window to run both the MPS and MRP options to automatically create either a high-level or detailed supply plan at all item levels.</span></span>|[<span data-ttu-id="b489a-132">Fremgangsmåde: Køre fuld planlægning, MPS eller MRP</span><span class="sxs-lookup"><span data-stu-id="b489a-132">How to: Run Full Planning, MPS or MRP</span></span>](production-how-to-run-mps-and-mrp.md)|
|<span data-ttu-id="b489a-133">Køre indkøbskladden for automatisk at oprette en detaljeret forsyningsplan for at dække behovet for varer, der kun kan opfyldes med et et køb eller ene overførsel.</span><span class="sxs-lookup"><span data-stu-id="b489a-133">Run the requisition worksheet to automatically create a detailed supply plan to cover demand for items that are replenished by purchase or transfer only.</span></span>|<span data-ttu-id="b489a-134">Siden **Indkøbskladde**</span><span class="sxs-lookup"><span data-stu-id="b489a-134">**Requisition Worksheet** page</span></span>|  
|<span data-ttu-id="b489a-135">Starte eller opdatere en produktionsordre som grovplanlagte operationer i masterproduktionsskemaet.</span><span class="sxs-lookup"><span data-stu-id="b489a-135">Initiate or update a production order as rough-scheduled operations in the master production schedule.</span></span>|[<span data-ttu-id="b489a-136">Fremgangsmåde: Omplanlægge eller forny produktionsordrer direkte</span><span class="sxs-lookup"><span data-stu-id="b489a-136">How to: Replan or Refresh Production Orders Directly</span></span>](production-how-to-replan-refresh-production-orders.md)|
|<span data-ttu-id="b489a-137">Genberegne arbejdscenter- eller produktionsressourcekalendere på grund af planlægningsændringer.</span><span class="sxs-lookup"><span data-stu-id="b489a-137">Recalculate work or machine center calendars due to planning changes.</span></span>|<span data-ttu-id="b489a-138">Afsnittet "Sådan beregnes en arbejdscenterkalender" i [Fremgangsmåde: Opsætte produktionskalendere](production-how-to-create-work-center-calendars.md)</span><span class="sxs-lookup"><span data-stu-id="b489a-138">"To calculate a work center calendar" section in [How to: Set Up Shop Calendars](production-how-to-create-work-center-calendars.md)</span></span>|
|<span data-ttu-id="b489a-139">Spore ordrebehov (sporet antal), forecast, rammesalgsordre eller planlægningsparameter (ikkesporet antal), der er årsag til den pågældende planlægningslinje.</span><span class="sxs-lookup"><span data-stu-id="b489a-139">Track the order demand (tracked quantity), forecast, blanket sales order, or planning parameter (untracked quantity) that has given rise to the planning line in question.</span></span>|[<span data-ttu-id="b489a-140">Fremgangsmåde: Spore relationer mellem behov og forsyning</span><span class="sxs-lookup"><span data-stu-id="b489a-140">How to: Track Relations Between Demand and Supply</span></span>](production-how-track-demand-supply.md)|
|<span data-ttu-id="b489a-141">Få vist en vares planlagte disponible lager ved forskellige visninger og se, hvilke bruttobehov, planlagte ordretilgange og andre hændelser, der påvirker over tid.</span><span class="sxs-lookup"><span data-stu-id="b489a-141">View an item's projected available inventory by different views and see which gross requirements, planned order receipts, and other events influence it over time.</span></span>|[<span data-ttu-id="b489a-142">Sådan gør du: Vise varedisponering</span><span class="sxs-lookup"><span data-stu-id="b489a-142">How to: View the Availability of Items</span></span>](inventory-how-availability-overview.md)|  
|<span data-ttu-id="b489a-143">Udfør udvalgte planlægningsaktiviteter, f.eks. ændring eller tilføjelse af planlægningskladdelinjer, i en grafisk oversigt over forsyningsplanen.</span><span class="sxs-lookup"><span data-stu-id="b489a-143">Perform selected planning activities, such as changing or adding planning worksheet lines, in a graphical view of the supply plan.</span></span>|[<span data-ttu-id="b489a-144">Fremgangsmåde: Ændre planlægningsforslag i en grafisk visning</span><span class="sxs-lookup"><span data-stu-id="b489a-144">How to: Modify Planning Suggestions in a Graphical View</span></span>](production-how-to-modify-planning-suggestions-in-a-graphical-view.md)|

## <a name="see-also"></a><span data-ttu-id="b489a-145">Se også</span><span class="sxs-lookup"><span data-stu-id="b489a-145">See Also</span></span>
[<span data-ttu-id="b489a-146">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="b489a-146">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="b489a-147">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="b489a-147">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="b489a-148">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="b489a-148">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="b489a-149">Køb</span><span class="sxs-lookup"><span data-stu-id="b489a-149">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="b489a-150">[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="b489a-150">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="b489a-151">Konfigurere bedste fremgangsmåder: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="b489a-151">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="b489a-152">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b489a-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
