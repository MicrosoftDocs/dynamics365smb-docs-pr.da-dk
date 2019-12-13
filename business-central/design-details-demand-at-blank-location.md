---
title: Designoplysninger – Behov og forsyning | Microsoft Docs
description: I dette emne introduceres begrebet behov, der er fællesbetegnelsen for enhver form for bruttobehov, som f.eks. en salgsordre og et komponentbehov fra en produktionsordre.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 11/11/2019
ms.author: sgroespe
ms.openlocfilehash: b5434f4f8b5df6a23d01401be442ec08de329d1d
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2019
ms.locfileid: "2880516"
---
# <a name="design-details-demand-at-blank-location"></a><span data-ttu-id="b2c4c-103">Designoplysninger: Behov på lokationen TOM</span><span class="sxs-lookup"><span data-stu-id="b2c4c-103">Design Details: Demand at Blank Location</span></span>
<span data-ttu-id="b2c4c-104">Når en bruger opretter en behovshændelse, f.eks. en salgsordrelinje, tillader programme sommetider brugeren at angive en lokationskode, og andre gange gør det ikke og bruger dermed en tom lokation.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-104">When a user creates a demand event, such as a sales order line, the program allows the user to sometimes specify a location code and other times not, that is, use blank location.</span></span>

<span data-ttu-id="b2c4c-105">For behov med eller uden lokationskoder fungerer planlægningssystemet på samme ukomplicerede måde, når:</span><span class="sxs-lookup"><span data-stu-id="b2c4c-105">For demand with or without location codes, the planning system operates in a straight forward way when:</span></span>

- <span data-ttu-id="b2c4c-106">Behovslinjer altid har lokationskoder, og systemet bruger lagervarer i fuld udstrækning, herunder den relevante lokationsopsætning.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-106">Demand lines always carry location codes and the system fully uses SKUs, including the relevant location setup.</span></span>
- <span data-ttu-id="b2c4c-107">Behovslinjer aldrig har lokationskoder, og systemet ikke bruger lagervarer eller nogen form for lokationsopsætning (se sidste eksempel i følgende afsnit).</span><span class="sxs-lookup"><span data-stu-id="b2c4c-107">Demand lines never carry location codes, and the system does not use SKUs or any location setup (see the last scenario in the following section).</span></span>

<span data-ttu-id="b2c4c-108">Men hvis behovshændelser sommetider har lokationskoder og sommetider ikke, vil planlægningssystemet følge visse regler afhængigt af opsætningen.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-108">However, if demand events sometimes have location codes and other times do not, the planning system will follow certain rules depending on setup.</span></span>

## <a name="demand-at-location"></a><span data-ttu-id="b2c4c-109">Behov på lokation</span><span class="sxs-lookup"><span data-stu-id="b2c4c-109">Demand at Location</span></span>
<span data-ttu-id="b2c4c-110">Når planlægningssystemet registrerer behov på en lokation, fungerer det forskelligt afhængigt af tre vigtige opsætningsværdier.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-110">When the planning system detects demand at a location, it will behave in different ways depending on three critical setup values.</span></span> <span data-ttu-id="b2c4c-111">Under et planlægningsforløb kontrollerer systemet de tre opsætningsværdier en efter en og planlægger i overensstemmelse med dem.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-111">During a planning run, the system checks for three setup values in sequence and plans accordingly.</span></span>

1. <span data-ttu-id="b2c4c-112">Er feltet **Tvungen lokationskode** markeret?</span><span class="sxs-lookup"><span data-stu-id="b2c4c-112">Is there a check mark in the **Location Mandatory** field?</span></span>

    <span data-ttu-id="b2c4c-113">Hvis ja, så:</span><span class="sxs-lookup"><span data-stu-id="b2c4c-113">If yes, then:</span></span>

2. <span data-ttu-id="b2c4c-114">Er varen registreret som lagervare?</span><span class="sxs-lookup"><span data-stu-id="b2c4c-114">Does SKU exist for the item?</span></span>

    <span data-ttu-id="b2c4c-115">Hvis ja, så:</span><span class="sxs-lookup"><span data-stu-id="b2c4c-115">If yes, then:</span></span>

    <span data-ttu-id="b2c4c-116">Varen planlægges i overensstemmelse med planlægningsparametrene på lagerkortet.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-116">The item is planned according to planning parameters on the SKU card.</span></span>

    <span data-ttu-id="b2c4c-117">Hvis nej, så:</span><span class="sxs-lookup"><span data-stu-id="b2c4c-117">If no, then:</span></span>

3. <span data-ttu-id="b2c4c-118">Indeholder feltet Komponenter på lokation den efterspurgte lokationskode?</span><span class="sxs-lookup"><span data-stu-id="b2c4c-118">Does the Components at Location field contain the demanded location code?</span></span>

  <span data-ttu-id="b2c4c-119">Hvis ja, så:</span><span class="sxs-lookup"><span data-stu-id="b2c4c-119">If yes, then:</span></span>

  <span data-ttu-id="b2c4c-120">Varen planlægges i overensstemmelse med planlægningsparametrene på varekortet.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-120">The item is planned according to planning parameters on the item card.</span></span>

  <span data-ttu-id="b2c4c-121">Hvis nej, så:</span><span class="sxs-lookup"><span data-stu-id="b2c4c-121">If no, then:</span></span>

  <span data-ttu-id="b2c4c-122">Varen planlægges i overensstemmelse med: Genbestillingsmetode = Lot-for-Lot, Medtag lager = Ja, alle andre planlægningsparametre = tomme, varer der bruger genbestillingsmetoden Ordre, fortsætter med at bruge Ordre sammen med de andre indstillinger.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-122">The item is planned according to: Reordering Policy = Lot-for-Lot, Include Inventory = Yes, all other planning parameters = Empty, items using Reordering Policy = Order will remain using Order along with the other settings.</span></span>

> [!NOTE]
> <span data-ttu-id="b2c4c-123">Den ekstraordinære opsætning af planlægningen, der er output som den sidste reaktion i trin 3 ovenfor, omtales i det følgende som det "minimale alternativ".</span><span class="sxs-lookup"><span data-stu-id="b2c4c-123">The exceptional planning setup that is output as the last reaction in step 3 above is referred to in the following as the “minimal alternative”.</span></span> <span data-ttu-id="b2c4c-124">Denne planlægningsopsætning dækker kun det nøjagtige behov, og alle andre planlægningsparametre ignoreres.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-124">This planning setup only covers the exact demand, and all other planning parameters are ignored.</span></span>

<span data-ttu-id="b2c4c-125">Hvis du ønsker oplysninger om variationer af denne planlægningslogik, kan du se afsnittet Scenarier herunder.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-125">For information about variations of this planning logic, see the Scenarios section below.</span></span>

## <a name="demand-at-blank-location"></a><span data-ttu-id="b2c4c-126">Behov på tom lokation</span><span class="sxs-lookup"><span data-stu-id="b2c4c-126">Demand at Blank Location</span></span>
<span data-ttu-id="b2c4c-127">Selv hvis feltet **Tvungen lokationskode** er markeret, tillader systemet, at behovslinjer oprettes uden lokationskode, også kaldet en tom lokation.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-127">Even if the **Location Mandatory** field is selected, the program will allow demand lines to be created without a location code, also referred to as blank location.</span></span> <span data-ttu-id="b2c4c-128">Dette er en afvigelse for systemet, da det har forskellige opsætningsværdier, der er indstillet til at håndtere lokationer (se ovenfor), og som et resultat opretter planlægningsprogrammet ikke en planlægningslinje for en behovslinje.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-128">This is a deviation for the system because it has various setup values tuned to dealing with locations (see above) and as a result, the planning engine will not create a planning line for such a demand line.</span></span>

<span data-ttu-id="b2c4c-129">Hvis feltet **Tvungen lokationskode** ikke er markeret, men en eller flere af opsætningsværdierne findes, anses det også for en afvigelse, og planlægningssystemet reagerer ved at bruge det "minimale alternativ": Varen planlægges i henhold til: Genbestillingsmetode = Lot-for-Lot (ordre forbliver ordre), Medtag lager = Ja, alle andre planlægningsparametre = tomme.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-129">If the **Location Mandatory** field is not selected but any of the location setup values exist, it is also considered a deviation, and the planning system will react by using the “minimal alternative”: The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

## <a name="scenarios"></a><span data-ttu-id="b2c4c-130">Eksempler</span><span class="sxs-lookup"><span data-stu-id="b2c4c-130">Scenarios</span></span>
<span data-ttu-id="b2c4c-131">Følgende scenarier beskriver variationer af behov på tom lokation, og hvordan planlægningssystemet oversætter til det "minimale alternativ".</span><span class="sxs-lookup"><span data-stu-id="b2c4c-131">The following scenarios describe variations of demand at blank location and how the planning system resolves to the “minimal alternative.”</span></span>

### <a name="setup-1"></a><span data-ttu-id="b2c4c-132">Opsætning 1:</span><span class="sxs-lookup"><span data-stu-id="b2c4c-132">Setup 1:</span></span>
<span data-ttu-id="b2c4c-133">Tvungen lokationskode = Ja</span><span class="sxs-lookup"><span data-stu-id="b2c4c-133">Location Mandatory = Yes</span></span>

<span data-ttu-id="b2c4c-134">Lagervare er konfigureret for RØD</span><span class="sxs-lookup"><span data-stu-id="b2c4c-134">SKU is set up for RED</span></span>

<span data-ttu-id="b2c4c-135">Komponenter på lokation = BLÅ</span><span class="sxs-lookup"><span data-stu-id="b2c4c-135">Components at Location = BLUE</span></span>

#### <a name="case-11-demand-is-at-red-location"></a><span data-ttu-id="b2c4c-136">Situation 1.1: Behov findes på lokationen RØD</span><span class="sxs-lookup"><span data-stu-id="b2c4c-136">Case 1.1: Demand is at RED location</span></span>
<span data-ttu-id="b2c4c-137">Varen planlægges i overensstemmelse med planlægningsparametrene på lagerkortet.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-137">The item is planned according to planning parameters on the SKU card.</span></span>

#### <a name="case-12-demand-is-at-blue-location"></a><span data-ttu-id="b2c4c-138">Situation 1.2: Behov findes på lokationen BLÅ</span><span class="sxs-lookup"><span data-stu-id="b2c4c-138">Case 1.2: Demand is at BLUE location</span></span>
<span data-ttu-id="b2c4c-139">Varen planlægges i overensstemmelse med: Genbestillingsmetode = Lot-for-Lot ( Ordre forbliver Ordre), Medtag lager = Ja, alle andre planlægningsparametre = tomme.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-139">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-13-demand-is-at-green-location"></a><span data-ttu-id="b2c4c-140">Situation 1.3: Behov findes på lokationen GRØN</span><span class="sxs-lookup"><span data-stu-id="b2c4c-140">Case 1.3: Demand is at GREEN location</span></span>
<span data-ttu-id="b2c4c-141">Varen planlægges i overensstemmelse med: Genbestillingsmetode = Lot-for-Lot ( Ordre forbliver Ordre), Medtag lager = Ja, alle andre planlægningsparametre = tomme.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-141">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-14-demand-is-at-blank-location"></a><span data-ttu-id="b2c4c-142">Situation 1.4: Behov findes på lokationen TOM</span><span class="sxs-lookup"><span data-stu-id="b2c4c-142">Case 1.4: Demand is at BLANK location</span></span>
<span data-ttu-id="b2c4c-143">Varen planlægges ikke, fordi der ikke er defineret en lokation på behovslinjen.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-143">The item is not planned because no location is defined on the demand line.</span></span>

### <a name="setup-2"></a><span data-ttu-id="b2c4c-144">Opsætning 2:</span><span class="sxs-lookup"><span data-stu-id="b2c4c-144">Setup 2:</span></span>
<span data-ttu-id="b2c4c-145">Tvungen lokationskode = Ja</span><span class="sxs-lookup"><span data-stu-id="b2c4c-145">Location Mandatory = Yes</span></span>

<span data-ttu-id="b2c4c-146">Ingen lagervare defineret</span><span class="sxs-lookup"><span data-stu-id="b2c4c-146">No SKU exists</span></span>

<span data-ttu-id="b2c4c-147">Komponenter på lokation = BLÅ</span><span class="sxs-lookup"><span data-stu-id="b2c4c-147">Components at Location = BLUE</span></span>

#### <a name="case-21-demand-is-at-red-location"></a><span data-ttu-id="b2c4c-148">Situation 2.1: Behov findes på lokationen RØD</span><span class="sxs-lookup"><span data-stu-id="b2c4c-148">Case 2.1: Demand is at RED location</span></span>
<span data-ttu-id="b2c4c-149">Varen planlægges i overensstemmelse med: Genbestillingsmetode = Lot-for-Lot ( Ordre forbliver Ordre), Medtag lager = Ja, alle andre planlægningsparametre = tomme.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-149">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-22-demand-is-at-blue-location"></a><span data-ttu-id="b2c4c-150">Situation 2.2: Behov findes på lokationen BLÅ</span><span class="sxs-lookup"><span data-stu-id="b2c4c-150">Case 2.2: Demand is at BLUE location</span></span>
<span data-ttu-id="b2c4c-151">Varen planlægges i overensstemmelse med planlægningsparametrene på varekortet.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-151">The item is planned according to planning parameters on the item card.</span></span>

### <a name="setup-3"></a><span data-ttu-id="b2c4c-152">Opsætning 3:</span><span class="sxs-lookup"><span data-stu-id="b2c4c-152">Setup 3:</span></span>
<span data-ttu-id="b2c4c-153">Tvungen lokationskode = Nej</span><span class="sxs-lookup"><span data-stu-id="b2c4c-153">Location Mandatory = No</span></span>

<span data-ttu-id="b2c4c-154">Ingen lagervare defineret</span><span class="sxs-lookup"><span data-stu-id="b2c4c-154">No SKU exists</span></span>

<span data-ttu-id="b2c4c-155">Komponenter på lokation = BLÅ</span><span class="sxs-lookup"><span data-stu-id="b2c4c-155">Components at Location = BLUE</span></span>

#### <a name="case-31-demand-is-at-red-location"></a><span data-ttu-id="b2c4c-156">Situation 3.1: Behov findes på lokationen RØD</span><span class="sxs-lookup"><span data-stu-id="b2c4c-156">Case 3.1: Demand is at RED location</span></span>
<span data-ttu-id="b2c4c-157">Varen planlægges i overensstemmelse med: Genbestillingsmetode = Lot-for-Lot ( Ordre forbliver Ordre), Medtag lager = Ja, alle andre planlægningsparametre = tomme.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-157">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-32-demand-is-at-blue-location"></a><span data-ttu-id="b2c4c-158">Situation 3.2: Behov findes på lokationen BLÅ</span><span class="sxs-lookup"><span data-stu-id="b2c4c-158">Case 3.2: Demand is at BLUE location</span></span>
<span data-ttu-id="b2c4c-159">Varen planlægges i overensstemmelse med planlægningsparametrene på varekortet.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-159">The item is planned according to planning parameters on the item card.</span></span>

#### <a name="case-33-demand-is-at-blank-location"></a><span data-ttu-id="b2c4c-160">Situation 3.3: Behov findes på lokationen TOM</span><span class="sxs-lookup"><span data-stu-id="b2c4c-160">Case 3.3: Demand is at BLANK location</span></span>
<span data-ttu-id="b2c4c-161">Varen planlægges i overensstemmelse med: Genbestillingsmetode = Lot-for-Lot ( Ordre forbliver Ordre), Medtag lager = Ja, alle andre planlægningsparametre = tomme.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-161">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

### <a name="setup-4"></a><span data-ttu-id="b2c4c-162">Opsætning 4:</span><span class="sxs-lookup"><span data-stu-id="b2c4c-162">Setup 4:</span></span>
<span data-ttu-id="b2c4c-163">Tvungen lokationskode = Nej</span><span class="sxs-lookup"><span data-stu-id="b2c4c-163">Location Mandatory = No</span></span>

<span data-ttu-id="b2c4c-164">Ingen lagervare defineret</span><span class="sxs-lookup"><span data-stu-id="b2c4c-164">No SKU exists</span></span>

<span data-ttu-id="b2c4c-165">Komponenter på lokation = TOM</span><span class="sxs-lookup"><span data-stu-id="b2c4c-165">Components at Location = BLANK</span></span>

#### <a name="case-41-demand-is-at-blue-location"></a><span data-ttu-id="b2c4c-166">Situation 4.1: Behov findes på lokationen BLÅ</span><span class="sxs-lookup"><span data-stu-id="b2c4c-166">Case 4.1: Demand is at BLUE location</span></span>
<span data-ttu-id="b2c4c-167">Varen planlægges i overensstemmelse med: Genbestillingsmetode = Lot-for-Lot ( Ordre forbliver Ordre), Medtag lager = Ja, alle andre planlægningsparametre = tomme.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-167">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-42-demand-is-at-blank-location"></a><span data-ttu-id="b2c4c-168">Situation 4.2: Behov findes på lokationen TOM</span><span class="sxs-lookup"><span data-stu-id="b2c4c-168">Case 4.2: Demand is at BLANK location</span></span>
<span data-ttu-id="b2c4c-169">Varen planlægges i overensstemmelse med planlægningsparametrene på varekortet.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-169">The item is planned according to planning parameters on the item card.</span></span>

<span data-ttu-id="b2c4c-170">Som det er illustreret i det sidste eksempel, kan man kun få det rigtige resultat for en behovslinje uden en lokationskode ved at deaktivere alle opsætningsværdier, der er knyttet til lokationer.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-170">As illustrated in the last scenario, the only way to get a correct result for a demand line without a location code is to disable all setup values relating to locations.</span></span> <span data-ttu-id="b2c4c-171">Ligeledes kan man kun få stabile planlægningsresultater for behov på lokationer ved at bruge lagervarer.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-171">Similarly, the only way to get stable planning results for demand at locations is to use SKUs.</span></span> <span data-ttu-id="b2c4c-172">Hvis virksomheder ofte planlægger ud fra behov på lokationer, anbefales de derfor kraftigt at benytte begrebet Lagervarer.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-172">Therefore, if companies often plan for demand at locations, they are strongly advised to use the Stockkeeping Units granule.</span></span>

## <a name="see-also"></a><span data-ttu-id="b2c4c-173">Se også</span><span class="sxs-lookup"><span data-stu-id="b2c4c-173">See Also</span></span>  
<span data-ttu-id="b2c4c-174">[Designoplysninger: Afstemning af behov og efterspørgsel](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="b2c4c-174">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="b2c4c-175">[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="b2c4c-175">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="b2c4c-176">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="b2c4c-176">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
