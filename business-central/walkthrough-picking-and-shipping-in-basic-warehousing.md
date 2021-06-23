---
title: Pluk og forsendelse i grundlæggende lageropsætninger
description: I Business Central kan de udgående processer for pluk og levering udføres på fire måder ved hjælp af forskellige funktioner afhængigt af kompleksitetsniveauet på lageret.
author: jill-kotel-andersson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: e1763e6288c8b8218955049ba7ef4c461ee5164e
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214649"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a><span data-ttu-id="80839-103">Gennemgang: Pluk og forsendelse i grundlæggende lageropsætninger</span><span class="sxs-lookup"><span data-stu-id="80839-103">Walkthrough: Picking and Shipping in Basic Warehouse Configurations</span></span>

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)] -->

<span data-ttu-id="80839-104">I [!INCLUDE[prod_short](includes/prod_short.md)] kan de udgående processer for pluk og levering udføres på fire måder ved hjælp af forskellige funktioner afhængigt af kompleksitetsniveauet på lageret.</span><span class="sxs-lookup"><span data-stu-id="80839-104">In [!INCLUDE[prod_short](includes/prod_short.md)], the outbound processes for picking and shipping can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="80839-105">Metode</span><span class="sxs-lookup"><span data-stu-id="80839-105">Method</span></span>|<span data-ttu-id="80839-106">Indgående proces</span><span class="sxs-lookup"><span data-stu-id="80839-106">Inbound process</span></span>|<span data-ttu-id="80839-107">Placering</span><span class="sxs-lookup"><span data-stu-id="80839-107">Bins</span></span>|<span data-ttu-id="80839-108">Pluk</span><span class="sxs-lookup"><span data-stu-id="80839-108">Picks</span></span>|<span data-ttu-id="80839-109">Leverancer</span><span class="sxs-lookup"><span data-stu-id="80839-109">Shipments</span></span>|<span data-ttu-id="80839-110">Kompleksitetsniveau (Se [Designoplysninger: Opsætning af lager](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="80839-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="80839-111">T</span><span class="sxs-lookup"><span data-stu-id="80839-111">A</span></span>|<span data-ttu-id="80839-112">Bogfør pluk og leverance fra ordrelinjen</span><span class="sxs-lookup"><span data-stu-id="80839-112">Post pick and shipment from the order line</span></span>|<span data-ttu-id="80839-113">X</span><span class="sxs-lookup"><span data-stu-id="80839-113">X</span></span>|||<span data-ttu-id="80839-114">2</span><span class="sxs-lookup"><span data-stu-id="80839-114">2</span></span>|  
|<span data-ttu-id="80839-115">B</span><span class="sxs-lookup"><span data-stu-id="80839-115">B</span></span>|<span data-ttu-id="80839-116">Bogfør pluk og leverance fra et lagerplukdokument</span><span class="sxs-lookup"><span data-stu-id="80839-116">Post pick and shipment from an inventory pick document</span></span>||<span data-ttu-id="80839-117">X</span><span class="sxs-lookup"><span data-stu-id="80839-117">X</span></span>||<span data-ttu-id="80839-118">3</span><span class="sxs-lookup"><span data-stu-id="80839-118">3</span></span>|  
|<span data-ttu-id="80839-119">L</span><span class="sxs-lookup"><span data-stu-id="80839-119">C</span></span>|<span data-ttu-id="80839-120">Bogfør pluk og leverance fra et lagerleverancedokument</span><span class="sxs-lookup"><span data-stu-id="80839-120">Post pick and shipment from a warehouse shipment document</span></span>|||<span data-ttu-id="80839-121">X</span><span class="sxs-lookup"><span data-stu-id="80839-121">X</span></span>|<span data-ttu-id="80839-122">5-4-6</span><span class="sxs-lookup"><span data-stu-id="80839-122">4/5/6</span></span>|  
|<span data-ttu-id="80839-123">D</span><span class="sxs-lookup"><span data-stu-id="80839-123">D</span></span>|<span data-ttu-id="80839-124">Bogfør pluk fra et lagerplukdokument, og bogfør leverance fra et lagerleverancedokument</span><span class="sxs-lookup"><span data-stu-id="80839-124">Post pick from a warehouse pick document and post shipment from a warehouse shipment document</span></span>||<span data-ttu-id="80839-125">X</span><span class="sxs-lookup"><span data-stu-id="80839-125">X</span></span>|<span data-ttu-id="80839-126">X</span><span class="sxs-lookup"><span data-stu-id="80839-126">X</span></span>|<span data-ttu-id="80839-127">5-4-6</span><span class="sxs-lookup"><span data-stu-id="80839-127">4/5/6</span></span>|  

<span data-ttu-id="80839-128">Du kan finde flere oplysninger i [Designoplysninger: Udgående lagerflow](design-details-outbound-warehouse-flow.md)</span><span class="sxs-lookup"><span data-stu-id="80839-128">For more information, see [Design Details: Outbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="80839-129">Den følgende gennemgang viser metode B i forrige tabel.</span><span class="sxs-lookup"><span data-stu-id="80839-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="80839-130">Om denne gennemgang</span><span class="sxs-lookup"><span data-stu-id="80839-130">About This Walkthrough</span></span>

<span data-ttu-id="80839-131">I grundlæggende lageropsætninger, hvor lokationen, du vil plukke fra, er sat op til at kræve pluk, men ikke leverance, bruges siden **Pluk (lager)** til at registrere og bogføre pluk- og leveranceoplysninger for de udgående kildedokumenterne.</span><span class="sxs-lookup"><span data-stu-id="80839-131">In basic warehouse configurations where your location is set up to require pick processing but not ship processing, you use the **Inventory Pick** page to record and post pick and ship information for your outbound source documents.</span></span> <span data-ttu-id="80839-132">Det udgående kildedokumentet kan være en salgsordre, en købsreturvareordre, en udgående overflytning eller en produktionsordre med komponentbehov.</span><span class="sxs-lookup"><span data-stu-id="80839-132">The outbound source document can be a sales order, purchase return order, outbound transfer order, or a production order with component need.</span></span>  

<span data-ttu-id="80839-133">Denne gennemgang viser følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="80839-133">This walkthrough demonstrates the following tasks:</span></span>  

- <span data-ttu-id="80839-134">Indstilling af SYD-lokation til pluk fra lager.</span><span class="sxs-lookup"><span data-stu-id="80839-134">Setting up SOUTH location for inventory picks.</span></span>  
- <span data-ttu-id="80839-135">Oprettelse af en salgsordre for debitor 10000 til 30 Amsterdam Lamps.</span><span class="sxs-lookup"><span data-stu-id="80839-135">Creating a sales order for customer 10000 for 30 Amsterdam Lamps.</span></span>  
- <span data-ttu-id="80839-136">Frigivelse af salgsordren til lagerekspedition.</span><span class="sxs-lookup"><span data-stu-id="80839-136">Releasing the sales order for warehouse handling.</span></span>  
- <span data-ttu-id="80839-137">Oprette et pluk baseret på et frigivet kildedokumentet.</span><span class="sxs-lookup"><span data-stu-id="80839-137">Creating an inventory pick based on a released source document.</span></span>  
- <span data-ttu-id="80839-138">Registrering af lagerbevægelsen fra lageret og på samme tid bogføring af salgsleverancen til kildesalgsordren.</span><span class="sxs-lookup"><span data-stu-id="80839-138">Registering the warehouse movement from the warehouse and at the same time posting the sales shipment for the source sales order.</span></span>  

## <a name="roles"></a><span data-ttu-id="80839-139">Roller</span><span class="sxs-lookup"><span data-stu-id="80839-139">Roles</span></span>

<span data-ttu-id="80839-140">Denne gennemgang viser de opgaver, der udføres af følgende brugerroller:</span><span class="sxs-lookup"><span data-stu-id="80839-140">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

- <span data-ttu-id="80839-141">Lagerchef</span><span class="sxs-lookup"><span data-stu-id="80839-141">Warehouse Manager</span></span>  
- <span data-ttu-id="80839-142">Ordrebehandler</span><span class="sxs-lookup"><span data-stu-id="80839-142">Order Processor</span></span>  
- <span data-ttu-id="80839-143">Lagermedarbejder</span><span class="sxs-lookup"><span data-stu-id="80839-143">Warehouse Worker</span></span>  

<!-- ## Prerequisites

To complete this walkthrough, you will need:  

- For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment. For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS installed.
 -->

## <a name="story"></a><span data-ttu-id="80839-144">Historie</span><span class="sxs-lookup"><span data-stu-id="80839-144">Story</span></span>

<span data-ttu-id="80839-145">Ellen, lagerlederen hos CRONUS, konfigurerer lagerstedet SYD til grundlæggende håndtering af pluk, hvor lagermedarbejdere kan behandle udgående ordrer enkeltvis.</span><span class="sxs-lookup"><span data-stu-id="80839-145">Ellen, the warehouse manager at CRONUS, sets up SOUTH warehouse for basic pick handling where warehouse workers process outbound orders individually.</span></span> <span data-ttu-id="80839-146">Susan, ordrebehandleren, opretter en salgsordre for 30 enheder af varen LS-1928-S, der skal sendes til debitor 10000 på lagerstedet SYD.</span><span class="sxs-lookup"><span data-stu-id="80839-146">Susan, the order processor, creates a sales order for 30 units of item 1928-S to be shipped to customer 10000 from the SOUTH Warehouse.</span></span> <span data-ttu-id="80839-147">John, som arbejder på lageret, skal sørge for, at forsendelsen klargøres og leveres til debitoren.</span><span class="sxs-lookup"><span data-stu-id="80839-147">John, the warehouse worker must make sure that the shipment is prepared and delivered to the customer.</span></span> <span data-ttu-id="80839-148">John administrerer alle involverede opgaver på siden **Pluk (lager)**, som automatisk peger på de placeringer, hvor 1928-S opbevares.</span><span class="sxs-lookup"><span data-stu-id="80839-148">John manages all involved tasks on the **Inventory Pick** page, which automatically points to the bins where 1928-S is stored.</span></span>

[!INCLUDE[set_up_location.md](includes/set_up_location.md)]

### <a name="setting-up-the-bin-codes"></a><span data-ttu-id="80839-149">Indstilling af placeringskoder</span><span class="sxs-lookup"><span data-stu-id="80839-149">Setting Up the Bin Codes</span></span>
<span data-ttu-id="80839-150">Når du har oprettet lokationen, skal du tilføje to placeringer.</span><span class="sxs-lookup"><span data-stu-id="80839-150">Once you have the location set up, you must add two bins.</span></span>

#### <a name="to-setup-the-bin-codes"></a><span data-ttu-id="80839-151">Indstilling af placeringskoder</span><span class="sxs-lookup"><span data-stu-id="80839-151">To setup the bin codes</span></span>

1. <span data-ttu-id="80839-152">Vælg handlingen **Placeringer**.</span><span class="sxs-lookup"><span data-stu-id="80839-152">Select the **Bins** action.</span></span>
2. <span data-ttu-id="80839-153">Opret to placeringer med koderne *S-01-0001* og *S-01-0002*.</span><span class="sxs-lookup"><span data-stu-id="80839-153">Create two bins, with the codes *S-01-0001* and *S-01-0002*.</span></span>

### <a name="making-yourself-a-warehouse-employee-at-location-south"></a><span data-ttu-id="80839-154">Selv oprette en lagermedarbejder på lokationen SYD</span><span class="sxs-lookup"><span data-stu-id="80839-154">Making Yourself a Warehouse Employee at Location SOUTH</span></span>

<span data-ttu-id="80839-155">Hvis du vil bruge denne funktion, skal du føje dig selv til lokationen som en lagermedarbejder.</span><span class="sxs-lookup"><span data-stu-id="80839-155">In order to use this functionality, you must add yourself to the location as a warehouse worker.</span></span> 

#### <a name="to-make-yourself-a-warehouse-employee"></a><span data-ttu-id="80839-156">Sådan oprettes en lagermedarbejder som en lagermedarbejder</span><span class="sxs-lookup"><span data-stu-id="80839-156">To make yourself a warehouse employee</span></span>

  1. <span data-ttu-id="80839-157">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig først](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lagermedarbejdere**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="80839-157">Choose the ![Lightbulb that opens the Tell Me feature first](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="80839-158">Vælg feltet **Bruger-id**, og vælg din egen brugerkonto på siden **Lagerstedsansatte**.</span><span class="sxs-lookup"><span data-stu-id="80839-158">Choose the **User ID** field, and select your own user account on the **Warehouse Employees** page.</span></span>
  3. <span data-ttu-id="80839-159">Angiv SYD i feltet **Lokationskode**.</span><span class="sxs-lookup"><span data-stu-id="80839-159">In the **Location Code** field, choose SOUTH.</span></span>  
  4. <span data-ttu-id="80839-160">Vælg handlingen **Bogfør**, og vælg derefter knappen **Ja**.</span><span class="sxs-lookup"><span data-stu-id="80839-160">Select the **Default** field, and then select the **Yes** button.</span></span>  

### <a name="making-item-1928-s-available"></a><span data-ttu-id="80839-161">Gør vare 1928-S tilgængelig</span><span class="sxs-lookup"><span data-stu-id="80839-161">Making Item 1928-S Available</span></span>

<span data-ttu-id="80839-162">Gør varen 1928-S tilgængelig på SYD-lokationen ved at følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="80839-162">To make item 1928-S available at the SOUTH location follow these steps:</span></span>  

  1. <span data-ttu-id="80839-163">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Vareomposteringskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="80839-163">Choose the ![Lightbulb that opens the Tell Me feature second](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Journals**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="80839-164">Åbn standardkladden, og opret derefter to varekladdelinjer med de følgende oplysninger om arbejdsdatoen (23. januar).</span><span class="sxs-lookup"><span data-stu-id="80839-164">Open the default journal, and then create two item journal lines with the following information about the work date (January 23).</span></span>  

        |<span data-ttu-id="80839-165">Postens type</span><span class="sxs-lookup"><span data-stu-id="80839-165">Entry Type</span></span>|<span data-ttu-id="80839-166">Varenummer</span><span class="sxs-lookup"><span data-stu-id="80839-166">Item Number</span></span>|<span data-ttu-id="80839-167">Lokationskode</span><span class="sxs-lookup"><span data-stu-id="80839-167">Location Code</span></span>|<span data-ttu-id="80839-168">Placeringskode</span><span class="sxs-lookup"><span data-stu-id="80839-168">Bin Code</span></span>|<span data-ttu-id="80839-169">Antal</span><span class="sxs-lookup"><span data-stu-id="80839-169">Quantity</span></span>|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |<span data-ttu-id="80839-170">Opregulering</span><span class="sxs-lookup"><span data-stu-id="80839-170">Positive Adjmt.</span></span>|<span data-ttu-id="80839-171">1928-S</span><span class="sxs-lookup"><span data-stu-id="80839-171">1928-S</span></span>|<span data-ttu-id="80839-172">SYD</span><span class="sxs-lookup"><span data-stu-id="80839-172">SOUTH</span></span>|<span data-ttu-id="80839-173">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="80839-173">S-01-0001</span></span>|<span data-ttu-id="80839-174">20</span><span class="sxs-lookup"><span data-stu-id="80839-174">20</span></span>|  
        |<span data-ttu-id="80839-175">Opregulering</span><span class="sxs-lookup"><span data-stu-id="80839-175">Positive Adjmt.</span></span>|<span data-ttu-id="80839-176">1928-S</span><span class="sxs-lookup"><span data-stu-id="80839-176">1928-S</span></span>|<span data-ttu-id="80839-177">SYD</span><span class="sxs-lookup"><span data-stu-id="80839-177">SOUTH</span></span>|<span data-ttu-id="80839-178">S-01-0002</span><span class="sxs-lookup"><span data-stu-id="80839-178">S-01-0002</span></span>|<span data-ttu-id="80839-179">20</span><span class="sxs-lookup"><span data-stu-id="80839-179">20</span></span>|  

        <span data-ttu-id="80839-180">Feltet **Placeringskode** på salgslinjerne er som standard skjult, så de skal vises.</span><span class="sxs-lookup"><span data-stu-id="80839-180">By default, the **Bin Code** field on the sales lines are hidden, so you must display it.</span></span> <span data-ttu-id="80839-181">Hvis du vil gøre dette, skal du tilpasse siden.</span><span class="sxs-lookup"><span data-stu-id="80839-181">To do this you need to personalize the page.</span></span> <span data-ttu-id="80839-182">Du kan finde flere oplysninger i [Start af tilpasning af en side gennem det personlige banner](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).</span><span class="sxs-lookup"><span data-stu-id="80839-182">For more information, see [To start personalizing a page through the Personalizing banner](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).</span></span>

  3. <span data-ttu-id="80839-183">Vælg **Bogfør** i gruppen **Bogføring** under fanen **Handlinger**.</span><span class="sxs-lookup"><span data-stu-id="80839-183">Choose **Actions**, then **Posting**, and then choose **Post**.</span></span>  
  4. <span data-ttu-id="80839-184">Vælg knappen **Ja**.</span><span class="sxs-lookup"><span data-stu-id="80839-184">Select the **Yes** button.</span></span>  

## <a name="creating-the-sales-order"></a><span data-ttu-id="80839-185">Oprettelse af salgsordren</span><span class="sxs-lookup"><span data-stu-id="80839-185">Creating the Sales Order</span></span>

<span data-ttu-id="80839-186">Salgsordrer er den mest almindelige type udgående kildedokument.</span><span class="sxs-lookup"><span data-stu-id="80839-186">Sales orders are the most common type of outbound source document.</span></span>  

### <a name="to-create-the-sales-order"></a><span data-ttu-id="80839-187">Sådan oprettes salgsordren</span><span class="sxs-lookup"><span data-stu-id="80839-187">To create the sales order</span></span>

1. <span data-ttu-id="80839-188">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordre**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="80839-188">Choose the ![Lightbulb that opens the Tell Me feature third](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="80839-189">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="80839-189">Choose the **New** action.</span></span>  
3. <span data-ttu-id="80839-190">Opret en salgsordre for debitor 10000 på arbejdsdatoen (23. januar) med følgende salgsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="80839-190">Create a sales order for customer 10000 on the work date (January 23) with the following sales order line.</span></span>  

    |<span data-ttu-id="80839-191">Vare</span><span class="sxs-lookup"><span data-stu-id="80839-191">Item</span></span>|<span data-ttu-id="80839-192">Lokationskode</span><span class="sxs-lookup"><span data-stu-id="80839-192">Location Code</span></span>|<span data-ttu-id="80839-193">Antal</span><span class="sxs-lookup"><span data-stu-id="80839-193">Quantity</span></span>|  
    |----|-------------|--------|  
    |<span data-ttu-id="80839-194">1928-S</span><span class="sxs-lookup"><span data-stu-id="80839-194">1928-S</span></span>|<span data-ttu-id="80839-195">SYD</span><span class="sxs-lookup"><span data-stu-id="80839-195">SOUTH</span></span>|<span data-ttu-id="80839-196">30</span><span class="sxs-lookup"><span data-stu-id="80839-196">30</span></span>|  

     <span data-ttu-id="80839-197">Fortsæt ved at meddele lageret, at salgsordren er klar til lagerekspedition.</span><span class="sxs-lookup"><span data-stu-id="80839-197">Proceed to notify the warehouse that the sales order is ready for warehouse handling.</span></span>  

4. <span data-ttu-id="80839-198">Vælg handlingen **Frigivelse**.</span><span class="sxs-lookup"><span data-stu-id="80839-198">Choose the **Release** action.</span></span>  

    <span data-ttu-id="80839-199">John fortsætter ved at vælge og sende de solgte varer.</span><span class="sxs-lookup"><span data-stu-id="80839-199">John proceeds to pick and ship the sold items.</span></span>  

## <a name="picking-and-shipping-items"></a><span data-ttu-id="80839-200">Sådan plukkes og leveres varer</span><span class="sxs-lookup"><span data-stu-id="80839-200">Picking and Shipping Items</span></span>

<span data-ttu-id="80839-201">På siden **Pluk (lager)** kan du administrere alle udgående lageraktiviteter til et specifikt kildedokument såsom en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="80839-201">On the **Inventory Pick** page, you can manage all outbound warehouse activities for a specific source document, such as a sales order.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a><span data-ttu-id="80839-202">Sådan foretages pluk og levering af varer</span><span class="sxs-lookup"><span data-stu-id="80839-202">To pick and ship items</span></span>

1. <span data-ttu-id="80839-203">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lagerpluk**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="80839-203">Choose the ![Lightbulb that opens the Tell Me feature fourth](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Picks**, and then choose the related link.</span></span>  
2. <span data-ttu-id="80839-204">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="80839-204">Choose the **New** action.</span></span>  

    <span data-ttu-id="80839-205">Sørg for, at feltet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="80839-205">Make sure that the **No.**</span></span> <span data-ttu-id="80839-206">er udfyldt i oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="80839-206">field on the **General** FastTab is filled in.</span></span>
3. <span data-ttu-id="80839-207">Vælg feltet **Kildedokument**, og vælg derefter **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="80839-207">Select the **Source Document** field, and then select **Sales Order**.</span></span>  
4. <span data-ttu-id="80839-208">Vælg feltet **Kildenr.**, vælg linjen for salget til debitor 10000, og vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="80839-208">Select the **Source No.** field, select the line for the sale to customer 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="80839-209">Du kan også vælge handlingen **Hent kildedokument** og derefter vælge salgsordren.</span><span class="sxs-lookup"><span data-stu-id="80839-209">Alternatively, choose the **Get Source Document** action, and then select the sales order.</span></span>  
5. <span data-ttu-id="80839-210">Vælg handlingen **Autofyld håndteringsantal**.</span><span class="sxs-lookup"><span data-stu-id="80839-210">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="80839-211">Du kan også indtaste henholdsvis 10 og 20 på de to lagerpluklinjer i feltet **Håndteringsantal**.</span><span class="sxs-lookup"><span data-stu-id="80839-211">Alternatively, in the **Qty. to Handle** field, enter 10 and 20 respectively on the two inventory pick lines.</span></span>  
6. <span data-ttu-id="80839-212">Vælg handlingen **Bogfør**, vælg **Lever**, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="80839-212">Choose the **Post** action, select **Ship**, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="80839-213">De 30 Amsterdam Lamps er nu registreret som plukket fra placeringerne S-01-0001 og S-01-0002, og der oprettes en negativ varepost, der afspejler den bogførte salgsleverance.</span><span class="sxs-lookup"><span data-stu-id="80839-213">The 30 Amsterdam Lamps are now registered as picked from bins S-01-0001 and S-01-0002, and a negative item ledger entry is created reflecting the posted sales shipment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="80839-214">Se også</span><span class="sxs-lookup"><span data-stu-id="80839-214">See Also</span></span>

[<span data-ttu-id="80839-215">Plukke varer med Pluk fra lager</span><span class="sxs-lookup"><span data-stu-id="80839-215">Pick Items with Inventory Picks</span></span>](warehouse-how-to-pick-items-with-inventory-picks.md)  
[<span data-ttu-id="80839-216">Plukke varer til lagerleverance</span><span class="sxs-lookup"><span data-stu-id="80839-216">Pick Items for Warehouse Shipment</span></span>](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[<span data-ttu-id="80839-217">Oprette grundlæggende lagersteder med handlingsområder</span><span class="sxs-lookup"><span data-stu-id="80839-217">Set Up Basic Warehouses with Operations Areas</span></span>](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[<span data-ttu-id="80839-218">Flytte komponenter til et handlingsområde i grundlæggende lageropsætninger</span><span class="sxs-lookup"><span data-stu-id="80839-218">Move Components to an Operation Area in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[<span data-ttu-id="80839-219">Plukke til produktion eller montage</span><span class="sxs-lookup"><span data-stu-id="80839-219">Pick for Production or Assembly</span></span>](warehouse-how-to-pick-for-production.md)  
[<span data-ttu-id="80839-220">Flytte varer ad hoc i grundlæggende lageropsætninger</span><span class="sxs-lookup"><span data-stu-id="80839-220">Move Items Ad Hoc in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[<span data-ttu-id="80839-221">Designoplysninger: Udgående lagerflow</span><span class="sxs-lookup"><span data-stu-id="80839-221">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="80839-222">Gennemgang af forretningsprocesser</span><span class="sxs-lookup"><span data-stu-id="80839-222">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
<span data-ttu-id="80839-223">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="80839-223">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]
