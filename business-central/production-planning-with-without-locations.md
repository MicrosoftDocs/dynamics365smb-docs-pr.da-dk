---
title: Planlægning med eller uden lokationer | Microsoft Docs
description: Det er vigtigt at forstå planlægning med eller uden lokationskoder på behovslinjer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 09faf5a92d242addb5805101fe99cb2c12f9f710
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191327"
---
# <a name="planning-with-or-without-locations"></a><span data-ttu-id="645a3-103">Planlægge med eller uden lokationer</span><span class="sxs-lookup"><span data-stu-id="645a3-103">Planning With or Without Locations</span></span>
<span data-ttu-id="645a3-104">Med hensyn til planlægning med eller uden lokationskoder på behovslinjer fungerer planlægningssystemet på samme ukomplicerede måde, når:</span><span class="sxs-lookup"><span data-stu-id="645a3-104">Concerning planning with or without location codes on demand lines, the planning system operates in a straight forward way when:</span></span>  

-   <span data-ttu-id="645a3-105">behovslinjer altid har lokationskoder, og systemet bruger lagervarer i fuld udstrækning, herunder den relevante lokationsopsætning.</span><span class="sxs-lookup"><span data-stu-id="645a3-105">demand lines always carry location codes and the system fully uses stockkeeping units, including the relevant location setup.</span></span>  
-   <span data-ttu-id="645a3-106">behovslinjer aldrig har lokationskoder, og systemet ikke bruger lagervarer eller nogen form for lokationsopsætning (se sidste eksempel nedenfor).</span><span class="sxs-lookup"><span data-stu-id="645a3-106">demand lines never carry location codes and the system does not use SKUs or any location setup (see last scenario below).</span></span>  

<span data-ttu-id="645a3-107">Hvis behovslinjerne derimod sommetider har lokationskoder og sommetider ikke, vil planlægningssystemet følge visse regler afhængigt af opsætningen.</span><span class="sxs-lookup"><span data-stu-id="645a3-107">However, if demand lines sometimes have location codes and other times do not, the planning system will follow certain rules depending on setup.</span></span>  

## <a name="demand-at-location"></a><span data-ttu-id="645a3-108">Behov på lokation</span><span class="sxs-lookup"><span data-stu-id="645a3-108">Demand at Location</span></span>  
<span data-ttu-id="645a3-109">Når planlægningssystemet registrerer behov på en lokation (en linje med en lokationskode), fungerer det forskelligt afhængigt af 3 vigtige opsætningsværdier.</span><span class="sxs-lookup"><span data-stu-id="645a3-109">When the planning system detects demand at a location (a line with a location code), it will behave in different ways depending on 3 critical setup values.</span></span>  

<span data-ttu-id="645a3-110">Under et planlægningsforløb kontrollerer systemet de 3 opsætningsværdier en efter en og planlægger i overensstemmelse med dem:</span><span class="sxs-lookup"><span data-stu-id="645a3-110">During a planning run, the system checks for the 3 setup values in sequence and plans accordingly:</span></span>  

1.  <span data-ttu-id="645a3-111">Er feltet **Tvungen lokationskode** markeret?</span><span class="sxs-lookup"><span data-stu-id="645a3-111">Is there a check mark in the **Location Mandatory** field?</span></span>  

    <span data-ttu-id="645a3-112">Hvis ja, så:</span><span class="sxs-lookup"><span data-stu-id="645a3-112">If yes, then:</span></span>  

2.  <span data-ttu-id="645a3-113">Er varen registreret som lagervare?</span><span class="sxs-lookup"><span data-stu-id="645a3-113">Does SKU exist for the item?</span></span>  

    <span data-ttu-id="645a3-114">Hvis ja, så:</span><span class="sxs-lookup"><span data-stu-id="645a3-114">If yes, then:</span></span>  

    <span data-ttu-id="645a3-115">Varen planlægges i overensstemmelse med planlægningsparametrene på lagerkortet.</span><span class="sxs-lookup"><span data-stu-id="645a3-115">The item is planned according to planning parameters on the SKU card.</span></span>  

    <span data-ttu-id="645a3-116">Hvis nej, så:</span><span class="sxs-lookup"><span data-stu-id="645a3-116">If no, then:</span></span>  

3.  <span data-ttu-id="645a3-117">Indeholder feltet **Komponenter på lokation** den efterspurgte lokationskode?</span><span class="sxs-lookup"><span data-stu-id="645a3-117">Does the **Components at Location** field contain the demanded location code?</span></span>  

    <span data-ttu-id="645a3-118">Hvis ja, så:</span><span class="sxs-lookup"><span data-stu-id="645a3-118">If yes, then:</span></span>  

    <span data-ttu-id="645a3-119">Varen planlægges i overensstemmelse med planlægningsparametrene på varekortet.</span><span class="sxs-lookup"><span data-stu-id="645a3-119">The item is planned according to planning parameters on the item card.</span></span>  

    <span data-ttu-id="645a3-120">Hvis nej, så:</span><span class="sxs-lookup"><span data-stu-id="645a3-120">If no, then:</span></span>  

    <span data-ttu-id="645a3-121">Varen planlægges i overensstemmelse med: Genbestillingsmetode =  *Lot-for-Lot*, Medtag lager =  *Ja*, alle andre planlægningsparametre = tomme.</span><span class="sxs-lookup"><span data-stu-id="645a3-121">The item is planned according to: Reordering Policy =  *Lot-for-Lot*, Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span> <span data-ttu-id="645a3-122">(Varer, der benytter genbestillingsmetoden  *Ordre*, fortsætter med at bruge  *Ordre* såvel som de andre indstillinger.)</span><span class="sxs-lookup"><span data-stu-id="645a3-122">(Items using reordering policy  *Order* remain using  *Order* as well as the other settings.)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="645a3-123">Dette minimale alternativ dækker kun det nøjagtige behov.</span><span class="sxs-lookup"><span data-stu-id="645a3-123">This minimal alternative only covers the exact demand.</span></span> <span data-ttu-id="645a3-124">Eventuelle definerede planlægningsparametre ignoreres.</span><span class="sxs-lookup"><span data-stu-id="645a3-124">Any planning parameters defined are ignored.</span></span>  

<span data-ttu-id="645a3-125">Se forskellene i eksemplerne nedenfor.</span><span class="sxs-lookup"><span data-stu-id="645a3-125">See variations in the scenarios below.</span></span>  

## <a name="demand-at-blank-location"></a><span data-ttu-id="645a3-126">Behov på "tom lokation"</span><span class="sxs-lookup"><span data-stu-id="645a3-126">Demand at "Blank Location"</span></span>  
<span data-ttu-id="645a3-127">Selv hvis afkrydsningsfeltet **Tvungen lokationskode** er markeret, tillader systemet, at behovslinjer oprettes uden lokationskode – hedder også *TOM* lokation.</span><span class="sxs-lookup"><span data-stu-id="645a3-127">Even if the **Location Mandatory** check box is selected, the system will allow demand lines to be created without a location code – also referred to as *BLANK* location.</span></span> <span data-ttu-id="645a3-128">Dette er en afvigelse for systemet, da det har forskellige opsætningsværdier, der er indstillet til at håndtere lokationer (se ovenfor), og som et resultat opretter planlægningsprogrammet ikke en planlægningslinje for en behovslinje.</span><span class="sxs-lookup"><span data-stu-id="645a3-128">This is a deviation for the system because it has various setup values tuned to dealing with locations (see above) and as a result, the planning engine will not create a planning line for such a demand line.</span></span> <span data-ttu-id="645a3-129">Hvis feltet **Tvungen lokationskode** ikke er markeret, men alle lokationsopsætningsværdierne findes, skal dette også betragtes en afvigelse, og planlægningssystemet reagerer ved at udføre det "minimale alternativ":</span><span class="sxs-lookup"><span data-stu-id="645a3-129">If the **Location Mandatory** field is not selected but any of the location setup values exist, then that is also considered a deviation and the planning system will react by outputting the "minimal alternative":</span></span>   
<span data-ttu-id="645a3-130">Varen planlægges i overensstemmelse med Genbestillingsmetode =  *Lot-for-Lot* ( *Ordre* forbliver *Ordre)*, Medtag lager =  *Ja*, alle andre planlægningsparametre = tomme.</span><span class="sxs-lookup"><span data-stu-id="645a3-130">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains *Order)*, Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

<span data-ttu-id="645a3-131">Se forskellene i opsætningseksemplerne nedenfor.</span><span class="sxs-lookup"><span data-stu-id="645a3-131">See variations in the setup scenarios below.</span></span>  

### <a name="setup-1"></a><span data-ttu-id="645a3-132">Opsætning 1:</span><span class="sxs-lookup"><span data-stu-id="645a3-132">Setup 1:</span></span>  

-   <span data-ttu-id="645a3-133">Tvungen lokationskode = *Ja*</span><span class="sxs-lookup"><span data-stu-id="645a3-133">Location Mandatory = *Yes*</span></span>  
-   <span data-ttu-id="645a3-134">Lagervare er konfigureret for  *RØD*</span><span class="sxs-lookup"><span data-stu-id="645a3-134">SKU is set up for  *RED*</span></span>  
-   <span data-ttu-id="645a3-135">Komponenter på lokation =  *BLÅ*</span><span class="sxs-lookup"><span data-stu-id="645a3-135">Component at Location =  *BLUE*</span></span>  

#### <a name="case-11-demand-is-at--red-location"></a><span data-ttu-id="645a3-136">Situation 1.1: Behovet findes på lokationen *RØD*</span><span class="sxs-lookup"><span data-stu-id="645a3-136">Case 1.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="645a3-137">Varen planlægges i overensstemmelse med planlægningsparametrene på lagerkortet (herunder mulig overflytning).</span><span class="sxs-lookup"><span data-stu-id="645a3-137">The item is planned according to planning parameters on the SKU card (including possible transfer).</span></span>  

#### <a name="case-12-demand-is-at--blue-location"></a><span data-ttu-id="645a3-138">Situation 1.2: Behovet findes på lokationen *BLÅ*</span><span class="sxs-lookup"><span data-stu-id="645a3-138">Case 1.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="645a3-139">Varen planlægges i overensstemmelse med planlægningsparametrene på varekortet.</span><span class="sxs-lookup"><span data-stu-id="645a3-139">The item is planned according to planning parameters on the item card.</span></span>  

#### <a name="case-13-demand-is-at--green-location"></a><span data-ttu-id="645a3-140">Situation 1.3: Behovet findes på lokationen  *GRØN*</span><span class="sxs-lookup"><span data-stu-id="645a3-140">Case 1.3: Demand is at  *GREEN* location</span></span>  

<span data-ttu-id="645a3-141">Varen planlægges i overensstemmelse med: Genbestillingsmetode =  *Lot-for-Lot* ( *Ordre* forbliver  *Ordre*), Medtag lager =  *Ja*, alle andre planlægningsparametre = tomme.</span><span class="sxs-lookup"><span data-stu-id="645a3-141">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-14-demand-is-at--blank-location"></a><span data-ttu-id="645a3-142">Situation 1.4: Behovet findes på lokationen *TOM*</span><span class="sxs-lookup"><span data-stu-id="645a3-142">Case 1.4: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="645a3-143">Varen planlægges ikke, fordi der ikke er defineret en lokation på behovslinjen.</span><span class="sxs-lookup"><span data-stu-id="645a3-143">The item is not planned because no location is defined on the demand line.</span></span>  

### <a name="setup-2"></a><span data-ttu-id="645a3-144">Opsætning 2:</span><span class="sxs-lookup"><span data-stu-id="645a3-144">Setup 2:</span></span>  

-   <span data-ttu-id="645a3-145">Tvungen lokationskode = *Ja*</span><span class="sxs-lookup"><span data-stu-id="645a3-145">Location Mandatory = *Yes*</span></span>  
-   <span data-ttu-id="645a3-146">Ingen lagervare defineret</span><span class="sxs-lookup"><span data-stu-id="645a3-146">No SKU exists</span></span>  
-   <span data-ttu-id="645a3-147">Komponenter på lokation =  *BLÅ*</span><span class="sxs-lookup"><span data-stu-id="645a3-147">Component at Location =  *BLUE*</span></span>  

#### <a name="case-21-demand-is-at--red-location"></a><span data-ttu-id="645a3-148">Situation 2.1: Behovet findes på lokationen  *RØD*</span><span class="sxs-lookup"><span data-stu-id="645a3-148">Case 2.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="645a3-149">Varen planlægges i overensstemmelse med: Genbestillingsmetode =  *Lot-for-Lot* ( *Ordre* forbliver  *Ordre*), Medtag lager =  *Ja*, alle andre planlægningsparametre = tomme.</span><span class="sxs-lookup"><span data-stu-id="645a3-149">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-22-demand-is-at--blue-location"></a><span data-ttu-id="645a3-150">Situation 2.2: Behovet findes på lokationen *BLÅ*</span><span class="sxs-lookup"><span data-stu-id="645a3-150">Case 2.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="645a3-151">Varen planlægges i overensstemmelse med planlægningsparametrene på varekortet.</span><span class="sxs-lookup"><span data-stu-id="645a3-151">The item is planned according to planning parameters on the item card.</span></span>  

### <a name="setup-3"></a><span data-ttu-id="645a3-152">Opsætning 3:</span><span class="sxs-lookup"><span data-stu-id="645a3-152">Setup 3:</span></span>  

-   <span data-ttu-id="645a3-153">Tvungen lokationskode = *Nej*</span><span class="sxs-lookup"><span data-stu-id="645a3-153">Location Mandatory = *No*</span></span>  
-   <span data-ttu-id="645a3-154">Ingen lagervare defineret</span><span class="sxs-lookup"><span data-stu-id="645a3-154">No SKU exists</span></span>  
-   <span data-ttu-id="645a3-155">Komponenter på lokation =  *BLÅ*</span><span class="sxs-lookup"><span data-stu-id="645a3-155">Component at Location =  *BLUE*</span></span>  

#### <a name="case-31-demand-is-at--red-location"></a><span data-ttu-id="645a3-156">Situation 3.1: Behovet findes på lokationen  *RØD*</span><span class="sxs-lookup"><span data-stu-id="645a3-156">Case 3.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="645a3-157">Varen planlægges i overensstemmelse med: Genbestillingsmetode =  *Lot-for-Lot* ( *Ordre* forbliver  *Ordre*), Medtag lager =  *Ja*, alle andre planlægningsparametre = tomme.</span><span class="sxs-lookup"><span data-stu-id="645a3-157">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-32-demand-is-at--blue-location"></a><span data-ttu-id="645a3-158">Situation 3.2: Behovet findes på lokationen *BLÅ*</span><span class="sxs-lookup"><span data-stu-id="645a3-158">Case 3.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="645a3-159">Varen planlægges i overensstemmelse med planlægningsparametrene på varekortet.</span><span class="sxs-lookup"><span data-stu-id="645a3-159">The item is planned according to planning parameters on the item card.</span></span>  

#### <a name="case-33-demand-is-at--blank-location"></a><span data-ttu-id="645a3-160">Situation 3.3: Behovet findes på lokationen  *TOM*</span><span class="sxs-lookup"><span data-stu-id="645a3-160">Case 3.3: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="645a3-161">Varen planlægges i overensstemmelse med: Genbestillingsmetode =  *Lot-for-Lot* ( *Ordre* forbliver  *Ordre*), Medtag lager =  *Ja*, alle andre planlægningsparametre = tomme.</span><span class="sxs-lookup"><span data-stu-id="645a3-161">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

### <a name="setup-4"></a><span data-ttu-id="645a3-162">Opsætning 4:</span><span class="sxs-lookup"><span data-stu-id="645a3-162">Setup 4:</span></span>  

-   <span data-ttu-id="645a3-163">Tvungen lokationskode = *Nej*</span><span class="sxs-lookup"><span data-stu-id="645a3-163">Location Mandatory = *No*</span></span>  
-   <span data-ttu-id="645a3-164">Ingen lagervare defineret</span><span class="sxs-lookup"><span data-stu-id="645a3-164">No SKU exists</span></span>  
-   <span data-ttu-id="645a3-165">Komponenter på lokation =  *TOM*</span><span class="sxs-lookup"><span data-stu-id="645a3-165">Component at Location =  *BLANK*</span></span>  

#### <a name="case-41-demand-is-at--blue-location"></a><span data-ttu-id="645a3-166">Situation 4.1: Behovet findes på lokationen  *BLÅ*</span><span class="sxs-lookup"><span data-stu-id="645a3-166">Case 4.1: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="645a3-167">Varen planlægges i overensstemmelse med: Genbestillingsmetode =  *Lot-for-Lot* ( *Ordre* forbliver  *Ordre*), Medtag lager =  *Ja*, alle andre planlægningsparametre = tomme.</span><span class="sxs-lookup"><span data-stu-id="645a3-167">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-42-demand-is-at--blank-location"></a><span data-ttu-id="645a3-168">Situation 4.2: Behovet findes på lokationen  *TOM*</span><span class="sxs-lookup"><span data-stu-id="645a3-168">Case 4.2: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="645a3-169">Varen planlægges i overensstemmelse med planlægningsparametrene på varekortet.</span><span class="sxs-lookup"><span data-stu-id="645a3-169">The item is planned according to planning parameters on the item card.</span></span>  

<span data-ttu-id="645a3-170">Som det fremgår af det sidste eksempel, kan man kun få det rigtige resultat for en behovslinje uden en lokationskode ved at deaktivere alle opsætningsværdier, der er knyttet til lokationer.</span><span class="sxs-lookup"><span data-stu-id="645a3-170">As you can see from the last scenario, the only way to get a correct result for a demand line without a location code is to disable all setup values relating to locations.</span></span> <span data-ttu-id="645a3-171">Ligeledes kan man kun få stabile planlægningsresultater for behov på lokationer ved at bruge lagervarer.</span><span class="sxs-lookup"><span data-stu-id="645a3-171">Similarly, the only way to get stable planning results for demand at locations is to use stockkeeping units.</span></span>  

<span data-ttu-id="645a3-172">Hvis du ofte planlægger med behov på lokationer, anbefales det derfor kraftigt at benytte lagervarefunktionen.</span><span class="sxs-lookup"><span data-stu-id="645a3-172">Therefore, if you often plan for demand at locations, it is strongly advised to use the Stockkeeping Units feature.</span></span>  

## <a name="see-also"></a><span data-ttu-id="645a3-173">Se også</span><span class="sxs-lookup"><span data-stu-id="645a3-173">See Also</span></span>
<span data-ttu-id="645a3-174">[Planlægning](production-planning.md)  </span><span class="sxs-lookup"><span data-stu-id="645a3-174">[Planning](production-planning.md)  </span></span>  
[<span data-ttu-id="645a3-175">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="645a3-175">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="645a3-176">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="645a3-176">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="645a3-177">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="645a3-177">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="645a3-178">Køb</span><span class="sxs-lookup"><span data-stu-id="645a3-178">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="645a3-179">[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="645a3-179">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="645a3-180">Konfigurere bedste fremgangsmåder: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="645a3-180">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="645a3-181">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="645a3-181">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
