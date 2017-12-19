---
title: "Gennemgang - Modtagelse og placering på lager i grundlæggende lageropsætninger | Microsoft Docs"
description: "I Dynamics 365 kan de indgående processer for modtagelse og placering på lager udføres på fire måder ved hjælp af forskellige funktioner afhængigt af kompleksitetsniveauet på lageret."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 52b017591b389c883e8a0bbeb35c1e3a3a9e7377
ms.contentlocale: da-dk
ms.lasthandoff: 12/14/2017

---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a><span data-ttu-id="c4636-103">Gennemgang: Modtagelse og placering på lager i grundlæggende lageropsætninger</span><span class="sxs-lookup"><span data-stu-id="c4636-103">Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations</span></span>
<span data-ttu-id="c4636-104">I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan de indgående processer for modtagelse og placering på lager udføres på fire måder ved hjælp af forskellige funktioner afhængigt af kompleksitetsniveauet på lageret.</span><span class="sxs-lookup"><span data-stu-id="c4636-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the inbound processes for receiving and putting away can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="c4636-105">Metode</span><span class="sxs-lookup"><span data-stu-id="c4636-105">Method</span></span>|<span data-ttu-id="c4636-106">Indgående proces</span><span class="sxs-lookup"><span data-stu-id="c4636-106">Inbound process</span></span>|<span data-ttu-id="c4636-107">Placering</span><span class="sxs-lookup"><span data-stu-id="c4636-107">Bins</span></span>|<span data-ttu-id="c4636-108">Modtagelser</span><span class="sxs-lookup"><span data-stu-id="c4636-108">Receipts</span></span>|<span data-ttu-id="c4636-109">Læg-på-lager-aktiviteter</span><span class="sxs-lookup"><span data-stu-id="c4636-109">Put-aways</span></span>|<span data-ttu-id="c4636-110">Kompleksitetsniveau (Se [Designoplysninger: Opsætning af lager](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="c4636-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="c4636-111">T</span><span class="sxs-lookup"><span data-stu-id="c4636-111">A</span></span>|<span data-ttu-id="c4636-112">Bogfør lagermodtagelse og læg-på-lager fra ordrelinjen</span><span class="sxs-lookup"><span data-stu-id="c4636-112">Post receipt and put-away from the order line</span></span>|<span data-ttu-id="c4636-113">X</span><span class="sxs-lookup"><span data-stu-id="c4636-113">X</span></span>|||<span data-ttu-id="c4636-114">2</span><span class="sxs-lookup"><span data-stu-id="c4636-114">2</span></span>|  
|<span data-ttu-id="c4636-115">B</span><span class="sxs-lookup"><span data-stu-id="c4636-115">B</span></span>|<span data-ttu-id="c4636-116">Bogfør lagermodtagelse og læg-på-lager fra et læg-på-lager-dokument</span><span class="sxs-lookup"><span data-stu-id="c4636-116">Post receipt and put-away from an inventory put-away document</span></span>|||<span data-ttu-id="c4636-117">X</span><span class="sxs-lookup"><span data-stu-id="c4636-117">X</span></span>|<span data-ttu-id="c4636-118">3</span><span class="sxs-lookup"><span data-stu-id="c4636-118">3</span></span>|  
|<span data-ttu-id="c4636-119">L</span><span class="sxs-lookup"><span data-stu-id="c4636-119">C</span></span>|<span data-ttu-id="c4636-120">Bogfør lagermodtagelse og læg-på-lager fra et lagermodtagelsesdokument</span><span class="sxs-lookup"><span data-stu-id="c4636-120">Post receipt and put-away from a warehouse receipt document</span></span>||<span data-ttu-id="c4636-121">X</span><span class="sxs-lookup"><span data-stu-id="c4636-121">X</span></span>||<span data-ttu-id="c4636-122">5-4-6</span><span class="sxs-lookup"><span data-stu-id="c4636-122">4/5/6</span></span>|  
|<span data-ttu-id="c4636-123">D</span><span class="sxs-lookup"><span data-stu-id="c4636-123">D</span></span>|<span data-ttu-id="c4636-124">Bogfør modtagelse fra et lagermodtagelsesdokument, og bogfør læg-på-lager fra lagerets læg-på-lager-dokument</span><span class="sxs-lookup"><span data-stu-id="c4636-124">Post receipt from a warehouse receipt document and post put-away from a warehouse put-away document</span></span>||<span data-ttu-id="c4636-125">X</span><span class="sxs-lookup"><span data-stu-id="c4636-125">X</span></span>|<span data-ttu-id="c4636-126">X</span><span class="sxs-lookup"><span data-stu-id="c4636-126">X</span></span>|<span data-ttu-id="c4636-127">5-4-6</span><span class="sxs-lookup"><span data-stu-id="c4636-127">4/5/6</span></span>|  

<span data-ttu-id="c4636-128">Du kan finde flere oplysninger i [Designoplysninger: Indgående lagerflow](design-details-inbound-warehouse-flow.md)</span><span class="sxs-lookup"><span data-stu-id="c4636-128">For more information, see [Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="c4636-129">Den følgende gennemgang viser metode B i forrige tabel.</span><span class="sxs-lookup"><span data-stu-id="c4636-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="c4636-130">Om denne gennemgang</span><span class="sxs-lookup"><span data-stu-id="c4636-130">About This Walkthrough</span></span>  
<span data-ttu-id="c4636-131">I grundlæggende lageropsætninger, hvor lokationen, du vil plukke fra, er sat op til at kræve læg-på-lager men ikke modtagelse, bruges vinduet **Læg-på-lager** til at registrere og bogføre læg-på-lager- og modtagelsesoplysninger for de indgående kildedokumenterne.</span><span class="sxs-lookup"><span data-stu-id="c4636-131">In basic warehouse configurations where your location is set up to require put-away processing but not receive processing, you use the **Inventory Put-away** window to record and post put-away and receipt information for your inbound source documents.</span></span> <span data-ttu-id="c4636-132">Det indgående kildedokument kan være en købsordre, en salgsreturvareordre, en indgående overflytningsordre eller en produktionsordre med afgang, der er klar til at blive lagt på lager.</span><span class="sxs-lookup"><span data-stu-id="c4636-132">The inbound source document can be a purchase order, sales return order, inbound transfer order, or production order with output that is ready to be put away.</span></span>

> [!NOTE]
> <span data-ttu-id="c4636-133">Selv om indstillingerne kaldes **Kræv pluk** og **Kræv læg-på-lager**, kan du bogføre modtagelser og leverancer direkte fra kildeforretningsdokumenterne på lokationer, hvor du kan markerer disse afkrydsningsfelter.</span><span class="sxs-lookup"><span data-stu-id="c4636-133">Even though the settings are called **Require Pick** and **Require Put-away**, you can still post receipts and shipments directly from the source business documents at locations where you select these check boxes.</span></span>  

<span data-ttu-id="c4636-134">Denne gennemgang viser følgende opgaver.</span><span class="sxs-lookup"><span data-stu-id="c4636-134">This walkthrough demonstrates the following tasks.</span></span>  

-   <span data-ttu-id="c4636-135">Indstilling af SØLV-lokation til læg-på-lager-aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="c4636-135">Setting up SILVER location for inventory put aways.</span></span>  
-   <span data-ttu-id="c4636-136">Indstilling af SØLV-lokation til placeringshåndtering.</span><span class="sxs-lookup"><span data-stu-id="c4636-136">Setting up SILVER location for bin handling.</span></span>  
-   <span data-ttu-id="c4636-137">Definition af en standardplacering for varen LS-81.</span><span class="sxs-lookup"><span data-stu-id="c4636-137">Defining a default bin for item LS-81.</span></span> <span data-ttu-id="c4636-138">(LS-75 er allerede oprettet i CRONUS).</span><span class="sxs-lookup"><span data-stu-id="c4636-138">(LS-75 is already set up in CRONUS.)</span></span>  
-   <span data-ttu-id="c4636-139">Oprettelse af en købsordre for kreditor 10000 til 40 højttalere.</span><span class="sxs-lookup"><span data-stu-id="c4636-139">Creating a purchase order for vendor 10000 for 40 loudspeakers.</span></span>  
-   <span data-ttu-id="c4636-140">Kontrol af, at lagerplaceringerne er forudindstillet af opsætningen.</span><span class="sxs-lookup"><span data-stu-id="c4636-140">Verifying that the put-away bins are preset by setup.</span></span>  
-   <span data-ttu-id="c4636-141">Frigivelse af købsordren til lagerekspedition.</span><span class="sxs-lookup"><span data-stu-id="c4636-141">Releasing the purchase order for warehouse handling.</span></span>  
-   <span data-ttu-id="c4636-142">Oprettelse af en læg-på-lager-aktivitet baseret på et frigivet kildedokumentet.</span><span class="sxs-lookup"><span data-stu-id="c4636-142">Creating an inventory put-away based on a released source document.</span></span>  
-   <span data-ttu-id="c4636-143">Kontrol af, at lagerplaceringerne er overført fra købsordren.</span><span class="sxs-lookup"><span data-stu-id="c4636-143">Verifying that the put-away bins are inherited from the purchase order.</span></span>  
-   <span data-ttu-id="c4636-144">Registrering af lagerbevægelsen til lageret og på samme tid bogføring af købsmodtagelsen til kildekøbsordren.</span><span class="sxs-lookup"><span data-stu-id="c4636-144">Registering the warehouse movement into the warehouse and at the same time posting the purchase receipt for the source purchase order.</span></span>  

## <a name="roles"></a><span data-ttu-id="c4636-145">Roller</span><span class="sxs-lookup"><span data-stu-id="c4636-145">Roles</span></span>  
<span data-ttu-id="c4636-146">Denne gennemgang viser de opgaver, der udføres af følgende brugerroller:</span><span class="sxs-lookup"><span data-stu-id="c4636-146">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

-   <span data-ttu-id="c4636-147">Lagerchef</span><span class="sxs-lookup"><span data-stu-id="c4636-147">Warehouse Manager</span></span>  
-   <span data-ttu-id="c4636-148">Indkøbsagent</span><span class="sxs-lookup"><span data-stu-id="c4636-148">Purchasing Agent</span></span>  
-   <span data-ttu-id="c4636-149">Lagermedarbejder</span><span class="sxs-lookup"><span data-stu-id="c4636-149">Warehouse Worker</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="c4636-150">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="c4636-150">Prerequisites</span></span>  
<span data-ttu-id="c4636-151">For at gennemføre denne gennemgang skal:</span><span class="sxs-lookup"><span data-stu-id="c4636-151">To complete this walkthrough, you will need:</span></span>  

-   <span data-ttu-id="c4636-152">CRONUS Danmark A/S være installeret.</span><span class="sxs-lookup"><span data-stu-id="c4636-152">CRONUS International Ltd. installed.</span></span>  
-   <span data-ttu-id="c4636-153">Du kan oprette dig selv som en lagermedarbejder på lokationen SØLV ved at følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="c4636-153">To make yourself a warehouse employee at SILVER location by following these steps:</span></span>  

    1.  <span data-ttu-id="c4636-154">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lagermedarbejdere**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c4636-154">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
    2.  <span data-ttu-id="c4636-155">Vælg feltet **Bruger-id**, og vælg din egen brugerkonto i vinduet **Brugere**.</span><span class="sxs-lookup"><span data-stu-id="c4636-155">Choose the **User ID** field, and select your own user account in the **Users** window.</span></span>  
    3.  <span data-ttu-id="c4636-156">Angiv SØLV i feltet **Lokationskode**.</span><span class="sxs-lookup"><span data-stu-id="c4636-156">In the **Location Code** field, enter SILVER.</span></span>  
    4.  <span data-ttu-id="c4636-157">Markér feltet **Standard**.</span><span class="sxs-lookup"><span data-stu-id="c4636-157">Select the **Default** field.</span></span>  

## <a name="story"></a><span data-ttu-id="c4636-158">Historie</span><span class="sxs-lookup"><span data-stu-id="c4636-158">Story</span></span>  
<span data-ttu-id="c4636-159">Ellen, som er indkøbschef hos CRONUS Danmark A/S, opretter en købsordre til 10 enheder af varen LS-75 og 30 enheder af varen LS-81 fra kreditoren 10000 til afsendelse til lagerstedet SØLV.</span><span class="sxs-lookup"><span data-stu-id="c4636-159">Ellen, the warehouse manager at CRONUS International Ltd., creates a purchase order for 10 units of item LS-75 and 30 units of item LS-81 from vendor 10000 to be delivered to SILVER Warehouse.</span></span> <span data-ttu-id="c4636-160">Når leveringen ankommer på lagerstedet, sætter John, som er lagerarbejder, varerne på lager på standardplaceringer, der er defineret for varerne.</span><span class="sxs-lookup"><span data-stu-id="c4636-160">When the delivery arrives at the warehouse, John, the warehouse worker, puts the items away in default bins defined for the items.</span></span> <span data-ttu-id="c4636-161">Når John bogfører placeringen på lager, bogføres varerne som modtaget på lageret og tilgængelige til salg eller andre behov.</span><span class="sxs-lookup"><span data-stu-id="c4636-161">When John posts the put-away, the items are posted as received into inventory and available for sale or other demand.</span></span>  

## <a name="setting-up-the-location"></a><span data-ttu-id="c4636-162">Indstilling af lokation</span><span class="sxs-lookup"><span data-stu-id="c4636-162">Setting up the Location</span></span>  
 <span data-ttu-id="c4636-163">Opsætningen af vinduet **Lokationskort** definerer arbejdsgangene i virksomheden.</span><span class="sxs-lookup"><span data-stu-id="c4636-163">The setup of the **Location Card** window defines the company’s warehouse flows.</span></span>  

### <a name="to-set-up-the-location"></a><span data-ttu-id="c4636-164">Sådan oprettes lokationen</span><span class="sxs-lookup"><span data-stu-id="c4636-164">To set up the location</span></span>  

1.  <span data-ttu-id="c4636-165">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lokationer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c4636-165">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c4636-166">Åbn lokationskortet SØLV.</span><span class="sxs-lookup"><span data-stu-id="c4636-166">Open the SILVER location card.</span></span>  
3.  <span data-ttu-id="c4636-167">Markér afkrydsningsfeltet **Kræv læg-på-lager**.</span><span class="sxs-lookup"><span data-stu-id="c4636-167">Select the **Require Put-away** check box.</span></span>  

    <span data-ttu-id="c4636-168">Fortsæt ved at oprette en standardplacering for de to varenumre for at kontrollere, hvor de lægges på lager.</span><span class="sxs-lookup"><span data-stu-id="c4636-168">Proceed to set up a default bin for the two item numbers to control where they are put away.</span></span>  

4.  <span data-ttu-id="c4636-169">Vælg handlingen **Placeringer**.</span><span class="sxs-lookup"><span data-stu-id="c4636-169">Choose the **Bins** action.</span></span>  
5.  <span data-ttu-id="c4636-170">Vælg den første række, til placering S-01-0001, og vælg derefter handlingen **Indhold**.</span><span class="sxs-lookup"><span data-stu-id="c4636-170">Select the first row, for bin S-01-0001, and then choose the **Contents** action.</span></span>  

    <span data-ttu-id="c4636-171">Bemærk i vinduet **Placeringsindhold**, at vare LS-75 allerede er oprettet som indhold på placering S-01-0001.</span><span class="sxs-lookup"><span data-stu-id="c4636-171">Notice in the **Bin Content** window that item LS-75 is already set up as content in bin S-01-0001.</span></span>  

6.  <span data-ttu-id="c4636-172">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c4636-172">Choose the **New** action.</span></span>  
7.  <span data-ttu-id="c4636-173">Vælg felterne **Fast** og **Standard**.</span><span class="sxs-lookup"><span data-stu-id="c4636-173">Select the **Fixed** and the **Default** fields.</span></span>  
8.  <span data-ttu-id="c4636-174">Skriv LS-81 i feltet **Bilagsnr.**.</span><span class="sxs-lookup"><span data-stu-id="c4636-174">In the **Item No.** field, enter LS-81.</span></span>  

## <a name="creating-the-purchase-order"></a><span data-ttu-id="c4636-175">Oprettelse af købsordren</span><span class="sxs-lookup"><span data-stu-id="c4636-175">Creating the Purchase Order</span></span>  
<span data-ttu-id="c4636-176">Købsordrer er den mest almindelige type indgående kildedokument.</span><span class="sxs-lookup"><span data-stu-id="c4636-176">Purchase orders are the most common type of inbound source document.</span></span>  

### <a name="to-create-the-purchase-order"></a><span data-ttu-id="c4636-177">Hvis du vil oprette købsordren</span><span class="sxs-lookup"><span data-stu-id="c4636-177">To create the purchase order</span></span>  

1.  <span data-ttu-id="c4636-178">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Købsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c4636-178">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c4636-179">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c4636-179">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="c4636-180">Opret en købsordre for kreditor 10000 på arbejdsdatoen (23. januar) med følgende købsordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="c4636-180">Create a purchase order for vendor 10000 on the work date (January 23) with the following purchase order lines.</span></span>  

    |<span data-ttu-id="c4636-181">Vare</span><span class="sxs-lookup"><span data-stu-id="c4636-181">Item</span></span>|<span data-ttu-id="c4636-182">Lokationskode</span><span class="sxs-lookup"><span data-stu-id="c4636-182">Location code</span></span>|<span data-ttu-id="c4636-183">Placeringskode</span><span class="sxs-lookup"><span data-stu-id="c4636-183">Bin code</span></span>|<span data-ttu-id="c4636-184">Antal</span><span class="sxs-lookup"><span data-stu-id="c4636-184">Quantity</span></span>|  
    |----------|-------------------|--------------|--------------|  
    |<span data-ttu-id="c4636-185">LS_75</span><span class="sxs-lookup"><span data-stu-id="c4636-185">LS_75</span></span>|<span data-ttu-id="c4636-186">SØLV</span><span class="sxs-lookup"><span data-stu-id="c4636-186">SILVER</span></span>|<span data-ttu-id="c4636-187">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="c4636-187">S-01-0001</span></span>|<span data-ttu-id="c4636-188">10</span><span class="sxs-lookup"><span data-stu-id="c4636-188">10</span></span>|  
    |<span data-ttu-id="c4636-189">LS-81</span><span class="sxs-lookup"><span data-stu-id="c4636-189">LS-81</span></span>|<span data-ttu-id="c4636-190">SØLV</span><span class="sxs-lookup"><span data-stu-id="c4636-190">SILVER</span></span>|<span data-ttu-id="c4636-191">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="c4636-191">S-01-0001</span></span>|<span data-ttu-id="c4636-192">30</span><span class="sxs-lookup"><span data-stu-id="c4636-192">30</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="c4636-193">Placeringskoden angives automatisk i overensstemmelse med opsætningen, som du har foretaget i afsnittet "Indstilling af lokation".</span><span class="sxs-lookup"><span data-stu-id="c4636-193">The bin code is entered automatically according to the setup that you performed in the “Setting up the Location” section.</span></span>  

    <span data-ttu-id="c4636-194">Fortsæt ved at meddele lageret, at købsordren er klar til lagerekspedition, når leverancen ankommer.</span><span class="sxs-lookup"><span data-stu-id="c4636-194">Proceed to notify the warehouse that the purchase order is ready for warehouse handling when the delivery arrives.</span></span>  

4.  <span data-ttu-id="c4636-195">Vælg handlingen **Frigivelse**.</span><span class="sxs-lookup"><span data-stu-id="c4636-195">Choose the **Release** action.</span></span>  

    <span data-ttu-id="c4636-196">Leverancen af højttalere fra kreditor 10000 er modtaget på SØLV-lageret, og John fortsætter med at lægge dem på plads.</span><span class="sxs-lookup"><span data-stu-id="c4636-196">The delivery of loudspeakers from vendor 10000 has arrived at SILVER warehouse, and John proceeds to put them away.</span></span>  

## <a name="receiving-and-putting-the-items-away"></a><span data-ttu-id="c4636-197">Modtagelse og placering af varer på lager</span><span class="sxs-lookup"><span data-stu-id="c4636-197">Receiving and Putting the Items Away</span></span>  
<span data-ttu-id="c4636-198">I vinduet **Læg-på-lager** kan du administrere alle indgående lageraktiviteter til et specifikt kildedokument, f.eks. en købsordre.</span><span class="sxs-lookup"><span data-stu-id="c4636-198">In the **Inventory Put-away** window, you can manage all inbound warehouse activities for a specific source document, such as a purchase order.</span></span>  

### <a name="to-receive-and-put-the-items-away"></a><span data-ttu-id="c4636-199">Sådan modtager du varerne og lægger dem på lager</span><span class="sxs-lookup"><span data-stu-id="c4636-199">To receive and put the items away</span></span>  

1.  <span data-ttu-id="c4636-200">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Læg-på-lager-akt. (lager)**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c4636-200">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Inventory Put-aways**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c4636-201">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c4636-201">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="c4636-202">Vælg feltet **Kildedokument**, og vælg derefter **Købsordre**.</span><span class="sxs-lookup"><span data-stu-id="c4636-202">Select the **Source Document** field, and then select **Purchase Order**.</span></span>  
4.  <span data-ttu-id="c4636-203">Vælg feltet **Kildenr.**, vælg linjen til købet fra kreditor 10000, og vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4636-203">Select the **Source No.** field, select the line for the purchase from vendor 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="c4636-204">Du kan også gå til fanen **Handlinger** i gruppen **Funktioner** og vælge **Hent kildedokument** og derefter vælge købsordren.</span><span class="sxs-lookup"><span data-stu-id="c4636-204">Alternatively, on the **Actions** tab, in the **Functions** group, choose **Get Source Document**, and then select the purchase order.</span></span>  

5.  <span data-ttu-id="c4636-205">Vælg handlingen **Autofyld håndteringsantal**.</span><span class="sxs-lookup"><span data-stu-id="c4636-205">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="c4636-206">Du kan også indtaste henholdsvis 10 og 30 på de to læg-på-lager-linjer i feltet **Håndteringsantal**.</span><span class="sxs-lookup"><span data-stu-id="c4636-206">Alternatively, in the **Qty. to Handle** field, enter 10 and 30 respectively on the two inventory put-away lines.</span></span>  

6.  <span data-ttu-id="c4636-207">Vælg handlingen **Bogfør**, vælg handlingen **Modtag**, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4636-207">Choose the **Post** action, select the **Receive** action, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="c4636-208">De 40 højttalere er nu registreret som lagt på lager på placering S-01-0001, og der oprettes en positiv varepost, der afspejler den bogførte købsmodtagelse.</span><span class="sxs-lookup"><span data-stu-id="c4636-208">The 40 loudspeakers are now registered as put away in bin S-01-0001, and a positive item ledger entry is created reflecting the posted purchase receipt.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c4636-209">Se også</span><span class="sxs-lookup"><span data-stu-id="c4636-209">See Also</span></span>  
 <span data-ttu-id="c4636-210">[Sådan lægges varer på lager med Læg-på-lager](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span><span class="sxs-lookup"><span data-stu-id="c4636-210">[How to: Put Items Away with Inventory Put-aways](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span></span>  
 <span data-ttu-id="c4636-211">[Fremgangsmåde: Oprette grundlæggende lagersteder med handlingsområder](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span><span class="sxs-lookup"><span data-stu-id="c4636-211">[How to: Set Up Basic Warehouses with Operations Areas](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span></span>  
 <span data-ttu-id="c4636-212">[Sådan flyttes komponenter til et handlingsområde i grundlæggende lageropsætninger](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="c4636-212">[How to: Move Components to an Operation Area in Basic Warehouse Configurations](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="c4636-213">[Fremgangsmåde: Plukke til produktion eller montage](warehouse-how-to-pick-for-production.md) </span><span class="sxs-lookup"><span data-stu-id="c4636-213">[How to: Pick for Production or Assembly](warehouse-how-to-pick-for-production.md) </span></span>  
 <span data-ttu-id="c4636-214">[Sådan flyttes varer ad hoc i grundlæggende lageropsætninger](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="c4636-214">[How to: Move Items Ad Hoc in Basic Warehouse Configurations](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="c4636-215">[Designoplysninger: Indgående lagerflow](design-details-inbound-warehouse-flow.md) </span><span class="sxs-lookup"><span data-stu-id="c4636-215">[Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md) </span></span>  
 [<span data-ttu-id="c4636-216">Gennemgang af forretningsprocesser</span><span class="sxs-lookup"><span data-stu-id="c4636-216">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="c4636-217">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c4636-217">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

