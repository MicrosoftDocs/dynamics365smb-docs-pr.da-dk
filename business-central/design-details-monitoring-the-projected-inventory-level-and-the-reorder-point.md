---
title: Designoplysninger – Overvågning af det forventede lagerniveau og genbestillingspunktet | Microsoft Docs
description: Få mere at vide, hvordan lagerplanlægningen skelner mellem planlagt beholdning og projekterede tilgængelige lagerniveauer.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, inventory, planning
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 3ae50295fd77de376ac25f2f2e267b765e5de58e
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307008"
---
# <a name="design-details-monitoring-the-projected-inventory-level-and-the-reorder-point"></a><span data-ttu-id="68830-103">Designoplysninger: Overvågning af det forventede lagerniveau og genbestillingspunktet</span><span class="sxs-lookup"><span data-stu-id="68830-103">Design Details: Monitoring the Projected Inventory Level and the Reorder Point</span></span>
<span data-ttu-id="68830-104">Lageret er en slags forsyning, men for lagerplanlægning skelner planlægningssystemet mellem to lagerniveauer:</span><span class="sxs-lookup"><span data-stu-id="68830-104">Inventory is a type of supply, but for inventory planning, the planning system distinguishes between two inventory levels:</span></span>  

* <span data-ttu-id="68830-105">Planlagt beholdning</span><span class="sxs-lookup"><span data-stu-id="68830-105">Projected inventory</span></span>  
* <span data-ttu-id="68830-106">Forventet disponibel beholdning</span><span class="sxs-lookup"><span data-stu-id="68830-106">Projected available inventory</span></span>  

## <a name="projected-inventory"></a><span data-ttu-id="68830-107">Planlagt beholdning</span><span class="sxs-lookup"><span data-stu-id="68830-107">Projected Inventory</span></span>  
<span data-ttu-id="68830-108">Oprindeligt er planlagt lagerbeholdning mængden af bruttolager, herunder forsyning og behov i fortiden, selvom det ikke er bogført, når du starter planlægningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="68830-108">Initially, projected inventory is the quantity of gross inventory, including supply and demand in the past even if not posted, when starting the planning process.</span></span> <span data-ttu-id="68830-109">I fremtiden bliver det et bevægeligt planlagt lagerniveau, der vedligeholdes af bruttomængder fra fremtidig forsyning og behov, fordi det føres langs tidslinjen (uanset om det er reserveret eller på andre måder tildelt).</span><span class="sxs-lookup"><span data-stu-id="68830-109">In the future, this becomes a moving projected inventory level that is maintained by gross quantities from future supply and demand because those are introduced along the time line (whether reserved or in other ways allocated).</span></span>  

<span data-ttu-id="68830-110">Den planlagte beholdning bruges af systemet til at overvåge genbestillingspunktet og bestemme genbestillingsantallet, når du bruger genbestillingsmetoden Maks. antal.</span><span class="sxs-lookup"><span data-stu-id="68830-110">The projected inventory is used by the planning system to monitor the reorder point and to determine the reorder quantity when using the Maximum Qty. reordering policy.</span></span>  

## <a name="projected-available-inventory"></a><span data-ttu-id="68830-111">Forventet disponibel beholdning</span><span class="sxs-lookup"><span data-stu-id="68830-111">Projected Available Inventory</span></span>  
<span data-ttu-id="68830-112">Den forventede disponible beholdning er en del af det planlagte lager, der er tilgængeligt til at opfylde behov på et givet tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="68830-112">The projected available inventory is the part of the projected inventory that at a given point in time is available to fulfill demand.</span></span> <span data-ttu-id="68830-113">Den forventede disponible beholdning der bruges af planlægningssystemet ved overvågning af niveauet for sikkerhedslageret.</span><span class="sxs-lookup"><span data-stu-id="68830-113">The projected available inventory is used by the planning engine when monitoring the safety stock level.</span></span>  

<span data-ttu-id="68830-114">Den forventede disponible beholdning bruges i planlægningssystemet til at overvåge niveauet for sikkerhedslageret, da sikkerhedslageret altid skal være tilgængeligt til at afhjælpe uventede behov.</span><span class="sxs-lookup"><span data-stu-id="68830-114">The projected available inventory is used by the planning system to monitor the safety stock level, since the safety stock must always be available to serve unexpected demand.</span></span>  

## <a name="time-buckets"></a><span data-ttu-id="68830-115">Intervaller</span><span class="sxs-lookup"><span data-stu-id="68830-115">Time Buckets</span></span>  
<span data-ttu-id="68830-116">Det er afgørende at have streng kontrol med den forventede lagerbeholdning for at registrere, når genbestillingspunktet nås eller passeres, og for at beregne det korrekte ordreantal, når du bruger genbestillingsmetoden Maks. antal.</span><span class="sxs-lookup"><span data-stu-id="68830-116">Having a tight control of the projected inventory is crucial to detect when the reorder point is reached or crossed and to calculate the right order quantity when using the Maximum Qty. reordering policy.</span></span>  

<span data-ttu-id="68830-117">Som tidligere nævnt beregnes den forventede lagerbeholdning i starten af planlægningsperioden.</span><span class="sxs-lookup"><span data-stu-id="68830-117">As stated earlier, the projected inventory level is calculated at the start of the planning period.</span></span> <span data-ttu-id="68830-118">Det er et bruttoniveau, der ikke medtager reservationer og lignende fordelinger.</span><span class="sxs-lookup"><span data-stu-id="68830-118">It is a gross level that does not consider reservations and similar allocations.</span></span> <span data-ttu-id="68830-119">Systemet overvåger de aggregerede ændringer over en tidsperiode, et interval, for at overvåge dette lagerniveau under planlægningssekvensen.</span><span class="sxs-lookup"><span data-stu-id="68830-119">To monitor this inventory level during the planning sequence, the system monitors the aggregated changes over a period of time, a time bucket.</span></span> <span data-ttu-id="68830-120">Systemet sikrer, at tidsintervallet er mindst én dag, da det er den mest nøjagtige tidsenhed for en behovs- eller forsyningshændelse.</span><span class="sxs-lookup"><span data-stu-id="68830-120">The system ensures that the time bucket is at least one day since it is the most precise unit of time for a demand or supply event.</span></span>  

## <a name="determining-the-projected-inventory-level"></a><span data-ttu-id="68830-121">Bestemmelse af det forventede lagerniveau</span><span class="sxs-lookup"><span data-stu-id="68830-121">Determining the Projected Inventory Level</span></span>  
<span data-ttu-id="68830-122">Følgende sekvens beskriver, hvordan det planlagte lagerniveau bestemmes:</span><span class="sxs-lookup"><span data-stu-id="68830-122">The following sequence describes how the projected inventory level is determined:</span></span>  

* <span data-ttu-id="68830-123">Når en forsyningshændelse, f.eks. en indkøbsordre, er blevet fuldstændig planlagt, øges den projekterede lagerbeholdning på forfaldsdatoen.</span><span class="sxs-lookup"><span data-stu-id="68830-123">When a supply event, such as a purchase order has been totally planned, it will increase the projected inventory on its due date.</span></span>  
* <span data-ttu-id="68830-124">Når en behovshændelse har opfyldt behovet, formindskes den projekterede lagerbeholdning ikke straks.</span><span class="sxs-lookup"><span data-stu-id="68830-124">When a demand event has been fully satisfied, it will not decrease the projected inventory right away.</span></span> <span data-ttu-id="68830-125">Der bogføres i stedet en påmindelse om reducering, som er en intern post, der indeholder dato og mængdebidrag til den planlagte lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="68830-125">Instead, it posts a decrease reminder, which is an internal record that holds the date and quantity of the contribution to the projected inventory.</span></span>  
* <span data-ttu-id="68830-126">Når en efterfølgende forsyningshændelse planlægges og placeres på tidslinjen, undersøges de bogførte reduktionsrykkerne én efter én indtil den planlagte dato for levering, mens den projekterede lagerbeholdning opdateres.</span><span class="sxs-lookup"><span data-stu-id="68830-126">When a subsequent supply event is planned and placed on the time line, the posted decrease reminders are investigated one by one up until the planned date of the supply while updating the projected inventory.</span></span> <span data-ttu-id="68830-127">Under denne proces kan niveauet for genbestillingspunktet for den interne forøgelse blive nået eller passeret.</span><span class="sxs-lookup"><span data-stu-id="68830-127">During this process, the reorder point level of the internal increase reminder may be reached or crossed.</span></span>  
* <span data-ttu-id="68830-128">Hvis der er indført en ny forsyningsordre, kontrollerer systemet, om den er indtastet før den aktuelle forsyning.</span><span class="sxs-lookup"><span data-stu-id="68830-128">If a new supply order is introduced, the system checks if it is entered before the current supply.</span></span> <span data-ttu-id="68830-129">Hvis det er, bliver den nye forsyning den aktuelle forsyning, og den udlignende procedure starter forfra.</span><span class="sxs-lookup"><span data-stu-id="68830-129">If it is, the new supply becomes current supply and the balancing procedure starts over.</span></span>  

<span data-ttu-id="68830-130">Nedenstående viser en grafisk illustration af dette princip:</span><span class="sxs-lookup"><span data-stu-id="68830-130">The following shows a graphical illustration of this principle:</span></span>  

<span data-ttu-id="68830-131">![Bestemme det planlagte lagerniveau](media/nav_app_supply_planning_2_projected_inventory.png "Bestemme det planlagte lagerniveau")</span><span class="sxs-lookup"><span data-stu-id="68830-131">![Determining the Projected Inventory Level](media/nav_app_supply_planning_2_projected_inventory.png "Determining the Projected Inventory Level")</span></span>  

1. <span data-ttu-id="68830-132">Forsyning **Sa** af 4 (faste) lukker behov **Da** af -3.</span><span class="sxs-lookup"><span data-stu-id="68830-132">Supply **Sa** of 4 (fixed) closes Demand **Da** of -3.</span></span>  
2. <span data-ttu-id="68830-133">CloseDemand: Opret en påmindelse om reducering af -3 (ikke vist).</span><span class="sxs-lookup"><span data-stu-id="68830-133">CloseDemand: Create a decrease reminder of -3 (not shown).</span></span>  
3. <span data-ttu-id="68830-134">Forsyning **Sa** er lukket med et overskud på 1 (der findes ingen yderligere behov).</span><span class="sxs-lookup"><span data-stu-id="68830-134">Supply **Sa** is closed with a surplus of 1 (no more demand exists).</span></span>  

     <span data-ttu-id="68830-135">Dette øger det forventede lagerniveau til +4, mens den forventede **disponible** beholdning bliver -1.</span><span class="sxs-lookup"><span data-stu-id="68830-135">This increases the projected inventory level to +4, while the projected **available** inventory becomes -1.</span></span>  

4. <span data-ttu-id="68830-136">Den næste forsyning **Sb** af 2 (en anden ordre) er allerede placeret på tidslinjen.</span><span class="sxs-lookup"><span data-stu-id="68830-136">The next supply **Sb** of 2 (another order) has already been placed on the timeline.</span></span>  
5. <span data-ttu-id="68830-137">Systemet kontrollerer, om der er påmindelse om reducering før **Sb** (det er der ikke, så ingen handling).</span><span class="sxs-lookup"><span data-stu-id="68830-137">System checks if there is any decrease reminder preceding **Sb** (there is not, so no action is taken).</span></span>  
6. <span data-ttu-id="68830-138">Systemet lukker forsyning **Sb** (der findes ingen yderligere behov) – enten A: ved at reducere den til 0 (annullere) eller B: ved at lade den være.</span><span class="sxs-lookup"><span data-stu-id="68830-138">System closes supply **Sb** (no more demand exists)—either A: by reducing it to 0 (cancel) or B: by leaving as is.</span></span>  

     <span data-ttu-id="68830-139">Dette øger den projekterede lagerbeholdning (A: +0 => +4 eller B: +2 = +6).</span><span class="sxs-lookup"><span data-stu-id="68830-139">This increases the projected inventory level (A: +0 => +4 or B: +2 = +6).</span></span>  

7. <span data-ttu-id="68830-140">Systemet foretager endelig kontrol: Er der nogen påmindelse om reducering?</span><span class="sxs-lookup"><span data-stu-id="68830-140">System makes a final check: Is there any decrease reminder?</span></span> <span data-ttu-id="68830-141">Ja, der er en på datoen for **Da**.</span><span class="sxs-lookup"><span data-stu-id="68830-141">Yes, there is one on the date of **Da**.</span></span>  
8. <span data-ttu-id="68830-142">Systemet føjer reduktionsrykkeren af -3-rykker til det planlagte lagerniveau enten A: +4 -3 = 1 eller B: +6 -3 = +3.</span><span class="sxs-lookup"><span data-stu-id="68830-142">System adds the decrease reminder of -3 reminder to the projected inventory level, either A: +4 -3 = 1 or B: +6 -3 = +3.</span></span>  
9. <span data-ttu-id="68830-143">I tilfælde af A opretter systemet en fremad planlagt ordre fra datoen **Da**.</span><span class="sxs-lookup"><span data-stu-id="68830-143">In case of A, the system creates a forward-scheduled order starting on date **Da**.</span></span>  

     <span data-ttu-id="68830-144">Genbestillingspunktet er ikke nået i B, og der oprettes ingen ny ordre.</span><span class="sxs-lookup"><span data-stu-id="68830-144">In case of B, the reorder point is reached and a new order is created.</span></span>  

## <a name="see-also"></a><span data-ttu-id="68830-145">Se også</span><span class="sxs-lookup"><span data-stu-id="68830-145">See Also</span></span>  
<span data-ttu-id="68830-146">[Designoplysninger: Genbestillingsmetoder](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="68830-146">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="68830-147">[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="68830-147">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="68830-148">[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="68830-148">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="68830-149">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="68830-149">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
