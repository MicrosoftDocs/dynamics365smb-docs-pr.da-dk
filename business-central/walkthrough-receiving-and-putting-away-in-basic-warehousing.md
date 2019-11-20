---
title: Gennemgang - Modtagelse og placering på lager i grundlæggende lageropsætninger | Microsoft Docs
description: I Business Central kan de indgående processer for modtagelse og placering på lager udføres på fire måder ved hjælp af forskellige funktioner afhængigt af kompleksitetsniveauet på lageret.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 31ac21dbba331748c9eef7bce199a5709147016b
ms.sourcegitcommit: 319023e53627dbe8e68643908aacc6fd594a4957
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/04/2019
ms.locfileid: "2554640"
---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a><span data-ttu-id="a80a4-103">Gennemgang: Modtagelse og placering på lager i grundlæggende lageropsætninger</span><span class="sxs-lookup"><span data-stu-id="a80a4-103">Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations</span></span>

<span data-ttu-id="a80a4-104">**Bemærk**: Denne gennemgang skal udføres på et demoregnskab med indstillingen **Fuld evaluering - Komplette eksempeldata**, der findes i sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="a80a4-104">**Note**: This walkthrough must be performed on a demonstration company with the **Full Evaluation - Complete Sample Data** option, which is available in the Sandbox environment.</span></span> <span data-ttu-id="a80a4-105">Du kan finde flere oplysninger i [Oprette et sandkassemiljø](across-how-create-sandbox-environment.md).</span><span class="sxs-lookup"><span data-stu-id="a80a4-105">For more information, see [Creating a Sandbox Environment](across-how-create-sandbox-environment.md).</span></span>

<span data-ttu-id="a80a4-106">I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan de indgående processer for modtagelse og placering på lager udføres på fire måder ved hjælp af forskellige funktioner afhængigt af kompleksitetsniveauet på lageret.</span><span class="sxs-lookup"><span data-stu-id="a80a4-106">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the inbound processes for receiving and putting away can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="a80a4-107">Metode</span><span class="sxs-lookup"><span data-stu-id="a80a4-107">Method</span></span>|<span data-ttu-id="a80a4-108">Indgående proces</span><span class="sxs-lookup"><span data-stu-id="a80a4-108">Inbound process</span></span>|<span data-ttu-id="a80a4-109">Placering</span><span class="sxs-lookup"><span data-stu-id="a80a4-109">Bins</span></span>|<span data-ttu-id="a80a4-110">Modtagelser</span><span class="sxs-lookup"><span data-stu-id="a80a4-110">Receipts</span></span>|<span data-ttu-id="a80a4-111">Læg-på-lager-aktiviteter</span><span class="sxs-lookup"><span data-stu-id="a80a4-111">Put-aways</span></span>|<span data-ttu-id="a80a4-112">Kompleksitetsniveau (Se [Designoplysninger: Opsætning af lager](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="a80a4-112">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="a80a4-113">T</span><span class="sxs-lookup"><span data-stu-id="a80a4-113">A</span></span>|<span data-ttu-id="a80a4-114">Bogfør lagermodtagelse og læg-på-lager fra ordrelinjen</span><span class="sxs-lookup"><span data-stu-id="a80a4-114">Post receipt and put-away from the order line</span></span>|<span data-ttu-id="a80a4-115">X</span><span class="sxs-lookup"><span data-stu-id="a80a4-115">X</span></span>|||<span data-ttu-id="a80a4-116">2</span><span class="sxs-lookup"><span data-stu-id="a80a4-116">2</span></span>|  
|<span data-ttu-id="a80a4-117">B</span><span class="sxs-lookup"><span data-stu-id="a80a4-117">B</span></span>|<span data-ttu-id="a80a4-118">Bogfør lagermodtagelse og læg-på-lager fra et læg-på-lager-dokument</span><span class="sxs-lookup"><span data-stu-id="a80a4-118">Post receipt and put-away from an inventory put-away document</span></span>|||<span data-ttu-id="a80a4-119">X</span><span class="sxs-lookup"><span data-stu-id="a80a4-119">X</span></span>|<span data-ttu-id="a80a4-120">3</span><span class="sxs-lookup"><span data-stu-id="a80a4-120">3</span></span>|  
|<span data-ttu-id="a80a4-121">L</span><span class="sxs-lookup"><span data-stu-id="a80a4-121">C</span></span>|<span data-ttu-id="a80a4-122">Bogfør lagermodtagelse og læg-på-lager fra et lagermodtagelsesdokument</span><span class="sxs-lookup"><span data-stu-id="a80a4-122">Post receipt and put-away from a warehouse receipt document</span></span>||<span data-ttu-id="a80a4-123">X</span><span class="sxs-lookup"><span data-stu-id="a80a4-123">X</span></span>||<span data-ttu-id="a80a4-124">5-4-6</span><span class="sxs-lookup"><span data-stu-id="a80a4-124">4/5/6</span></span>|  
|<span data-ttu-id="a80a4-125">D</span><span class="sxs-lookup"><span data-stu-id="a80a4-125">D</span></span>|<span data-ttu-id="a80a4-126">Bogfør modtagelse fra et lagermodtagelsesdokument, og bogfør læg-på-lager fra lagerets læg-på-lager-dokument</span><span class="sxs-lookup"><span data-stu-id="a80a4-126">Post receipt from a warehouse receipt document and post put-away from a warehouse put-away document</span></span>||<span data-ttu-id="a80a4-127">X</span><span class="sxs-lookup"><span data-stu-id="a80a4-127">X</span></span>|<span data-ttu-id="a80a4-128">X</span><span class="sxs-lookup"><span data-stu-id="a80a4-128">X</span></span>|<span data-ttu-id="a80a4-129">5-4-6</span><span class="sxs-lookup"><span data-stu-id="a80a4-129">4/5/6</span></span>|  

<span data-ttu-id="a80a4-130">Du kan finde flere oplysninger i [Designoplysninger: Indgående lagerflow](design-details-inbound-warehouse-flow.md)</span><span class="sxs-lookup"><span data-stu-id="a80a4-130">For more information, see [Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="a80a4-131">Den følgende gennemgang viser metode B i forrige tabel.</span><span class="sxs-lookup"><span data-stu-id="a80a4-131">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="a80a4-132">Om denne gennemgang</span><span class="sxs-lookup"><span data-stu-id="a80a4-132">About This Walkthrough</span></span>  
<span data-ttu-id="a80a4-133">I grundlæggende lageropsætninger, hvor lokationen, du vil plukke fra, er sat op til at kræve læg-på-lager men ikke modtagelse, bruges siden **Læg-på-lager** til at registrere og bogføre læg-på-lager- og modtagelsesoplysninger for de indgående kildedokumenterne.</span><span class="sxs-lookup"><span data-stu-id="a80a4-133">In basic warehouse configurations where your location is set up to require put-away processing but not receive processing, you use the **Inventory Put-away** page to record and post put-away and receipt information for your inbound source documents.</span></span> <span data-ttu-id="a80a4-134">Det indgående kildedokument kan være en købsordre, en salgsreturvareordre, en indgående overflytningsordre eller en produktionsordre med afgang, der er klar til at blive lagt på lager.</span><span class="sxs-lookup"><span data-stu-id="a80a4-134">The inbound source document can be a purchase order, sales return order, inbound transfer order, or production order with output that is ready to be put away.</span></span>

> [!NOTE]
> <span data-ttu-id="a80a4-135">Selv om indstillingerne kaldes **Kræv pluk** og **Kræv læg-på-lager**, kan du bogføre modtagelser og leverancer direkte fra kildeforretningsdokumenterne på lokationer, hvor du kan markerer disse afkrydsningsfelter.</span><span class="sxs-lookup"><span data-stu-id="a80a4-135">Even though the settings are called **Require Pick** and **Require Put-away**, you can still post receipts and shipments directly from the source business documents at locations where you select these check boxes.</span></span>  

<span data-ttu-id="a80a4-136">Denne gennemgang viser følgende opgaver.</span><span class="sxs-lookup"><span data-stu-id="a80a4-136">This walkthrough demonstrates the following tasks.</span></span>  

-   <span data-ttu-id="a80a4-137">Indstilling af SØLV-lokation til læg-på-lager-aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="a80a4-137">Setting up SILVER location for inventory put aways.</span></span>  
-   <span data-ttu-id="a80a4-138">Indstilling af SØLV-lokation til placeringshåndtering.</span><span class="sxs-lookup"><span data-stu-id="a80a4-138">Setting up SILVER location for bin handling.</span></span>  
-   <span data-ttu-id="a80a4-139">Definition af en standardplacering for varen LS-81.</span><span class="sxs-lookup"><span data-stu-id="a80a4-139">Defining a default bin for item LS-81.</span></span> <span data-ttu-id="a80a4-140">(LS-75 er allerede oprettet i CRONUS).</span><span class="sxs-lookup"><span data-stu-id="a80a4-140">(LS-75 is already set up in CRONUS.)</span></span>  
-   <span data-ttu-id="a80a4-141">Oprettelse af en købsordre for kreditor 10000 til 40 højttalere.</span><span class="sxs-lookup"><span data-stu-id="a80a4-141">Creating a purchase order for vendor 10000 for 40 loudspeakers.</span></span>  
-   <span data-ttu-id="a80a4-142">Kontrol af, at lagerplaceringerne er forudindstillet af opsætningen.</span><span class="sxs-lookup"><span data-stu-id="a80a4-142">Verifying that the put-away bins are preset by setup.</span></span>  
-   <span data-ttu-id="a80a4-143">Frigivelse af købsordren til lagerekspedition.</span><span class="sxs-lookup"><span data-stu-id="a80a4-143">Releasing the purchase order for warehouse handling.</span></span>  
-   <span data-ttu-id="a80a4-144">Oprettelse af en læg-på-lager-aktivitet baseret på et frigivet kildedokumentet.</span><span class="sxs-lookup"><span data-stu-id="a80a4-144">Creating an inventory put-away based on a released source document.</span></span>  
-   <span data-ttu-id="a80a4-145">Kontrol af, at lagerplaceringerne er overført fra købsordren.</span><span class="sxs-lookup"><span data-stu-id="a80a4-145">Verifying that the put-away bins are inherited from the purchase order.</span></span>  
-   <span data-ttu-id="a80a4-146">Registrering af lagerbevægelsen til lageret og på samme tid bogføring af købsmodtagelsen til kildekøbsordren.</span><span class="sxs-lookup"><span data-stu-id="a80a4-146">Registering the warehouse movement into the warehouse and at the same time posting the purchase receipt for the source purchase order.</span></span>  

## <a name="roles"></a><span data-ttu-id="a80a4-147">Roller</span><span class="sxs-lookup"><span data-stu-id="a80a4-147">Roles</span></span>  
<span data-ttu-id="a80a4-148">Denne gennemgang viser de opgaver, der udføres af følgende brugerroller:</span><span class="sxs-lookup"><span data-stu-id="a80a4-148">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

-   <span data-ttu-id="a80a4-149">Lagerchef</span><span class="sxs-lookup"><span data-stu-id="a80a4-149">Warehouse Manager</span></span>  
-   <span data-ttu-id="a80a4-150">Indkøbsagent</span><span class="sxs-lookup"><span data-stu-id="a80a4-150">Purchasing Agent</span></span>  
-   <span data-ttu-id="a80a4-151">Lagermedarbejder</span><span class="sxs-lookup"><span data-stu-id="a80a4-151">Warehouse Worker</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="a80a4-152">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="a80a4-152">Prerequisites</span></span>  
<span data-ttu-id="a80a4-153">For at gennemføre denne gennemgang skal du:</span><span class="sxs-lookup"><span data-stu-id="a80a4-153">To complete this walkthrough, you will need:</span></span>  

-   <span data-ttu-id="a80a4-154">CRONUS Danmark A/S være installeret.</span><span class="sxs-lookup"><span data-stu-id="a80a4-154">CRONUS International Ltd. installed.</span></span>  
-   <span data-ttu-id="a80a4-155">Du kan oprette dig selv som lagermedarbejder på lokationen SØLV ved at følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="a80a4-155">To make yourself a warehouse employee at SILVER location by following these steps:</span></span>  

    1.  <span data-ttu-id="a80a4-156">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lagermedarbejdere**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="a80a4-156">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
    2.  <span data-ttu-id="a80a4-157">Vælg feltet **Bruger-id**, og vælg din egen brugerkonto på siden **Brugere**.</span><span class="sxs-lookup"><span data-stu-id="a80a4-157">Choose the **User ID** field, and select your own user account on the **Users** page.</span></span>  
    3.  <span data-ttu-id="a80a4-158">Angiv SØLV i feltet **Lokationskode**.</span><span class="sxs-lookup"><span data-stu-id="a80a4-158">In the **Location Code** field, enter SILVER.</span></span>  
    4.  <span data-ttu-id="a80a4-159">Markér feltet **Standard**.</span><span class="sxs-lookup"><span data-stu-id="a80a4-159">Select the **Default** field.</span></span>  

## <a name="story"></a><span data-ttu-id="a80a4-160">Historie</span><span class="sxs-lookup"><span data-stu-id="a80a4-160">Story</span></span>  
<span data-ttu-id="a80a4-161">Ellen, som er indkøbschef hos CRONUS Danmark A/S, opretter en købsordre til 10 enheder af varen LS-75 og 30 enheder af varen LS-81 fra kreditoren 10000 til afsendelse til lagerstedet SØLV.</span><span class="sxs-lookup"><span data-stu-id="a80a4-161">Ellen, the warehouse manager at CRONUS International Ltd., creates a purchase order for 10 units of item LS-75 and 30 units of item LS-81 from vendor 10000 to be delivered to SILVER Warehouse.</span></span> <span data-ttu-id="a80a4-162">Når leveringen ankommer på lagerstedet, sætter John, som er lagerarbejder, varerne på lager på standardplaceringer, der er defineret for varerne.</span><span class="sxs-lookup"><span data-stu-id="a80a4-162">When the delivery arrives at the warehouse, John, the warehouse worker, puts the items away in default bins defined for the items.</span></span> <span data-ttu-id="a80a4-163">Når John bogfører placeringen på lager, bogføres varerne som modtaget på lageret og tilgængelige til salg eller andre behov.</span><span class="sxs-lookup"><span data-stu-id="a80a4-163">When John posts the put-away, the items are posted as received into inventory and available for sale or other demand.</span></span>  

## <a name="setting-up-the-location"></a><span data-ttu-id="a80a4-164">Indstilling af lokation</span><span class="sxs-lookup"><span data-stu-id="a80a4-164">Setting up the Location</span></span>  
 <span data-ttu-id="a80a4-165">Opsætningen af siden **Lokationskort** definerer flows i virksomheden.</span><span class="sxs-lookup"><span data-stu-id="a80a4-165">The setup of the **Location Card** page defines the company’s warehouse flows.</span></span>  

### <a name="to-set-up-the-location"></a><span data-ttu-id="a80a4-166">Sådan oprettes lokationen</span><span class="sxs-lookup"><span data-stu-id="a80a4-166">To set up the location</span></span>  

1.  <span data-ttu-id="a80a4-167">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lokationer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="a80a4-167">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a80a4-168">Åbn lokationskortet SØLV.</span><span class="sxs-lookup"><span data-stu-id="a80a4-168">Open the SILVER location card.</span></span>  
3.  <span data-ttu-id="a80a4-169">Markér afkrydsningsfeltet **Kræv læg-på-lager**.</span><span class="sxs-lookup"><span data-stu-id="a80a4-169">Select the **Require Put-away** check box.</span></span>  

    <span data-ttu-id="a80a4-170">Fortsæt ved at oprette en standardplacering for de to varenumre for at kontrollere, hvor de lægges på lager.</span><span class="sxs-lookup"><span data-stu-id="a80a4-170">Proceed to set up a default bin for the two item numbers to control where they are put away.</span></span>  

4.  <span data-ttu-id="a80a4-171">Vælg handlingen **Placeringer**.</span><span class="sxs-lookup"><span data-stu-id="a80a4-171">Choose the **Bins** action.</span></span>  
5.  <span data-ttu-id="a80a4-172">Vælg den første række, til placering S-01-0001, og vælg derefter handlingen **Indhold**.</span><span class="sxs-lookup"><span data-stu-id="a80a4-172">Select the first row, for bin S-01-0001, and then choose the **Contents** action.</span></span>  

    <span data-ttu-id="a80a4-173">Bemærk på siden **Placeringsindhold**, at vare LS-75 allerede er oprettet som indhold på placering S-01-0001.</span><span class="sxs-lookup"><span data-stu-id="a80a4-173">Notice on the **Bin Content** page that item LS-75 is already set up as content in bin S-01-0001.</span></span>  

6.  <span data-ttu-id="a80a4-174">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a80a4-174">Choose the **New** action.</span></span>  
7.  <span data-ttu-id="a80a4-175">Vælg felterne **Fast** og **Standard**.</span><span class="sxs-lookup"><span data-stu-id="a80a4-175">Select the **Fixed** and the **Default** fields.</span></span>  
8.  <span data-ttu-id="a80a4-176">Skriv LS-81 i feltet **Bilagsnr.**.</span><span class="sxs-lookup"><span data-stu-id="a80a4-176">In the **Item No.** field, enter LS-81.</span></span>  

## <a name="creating-the-purchase-order"></a><span data-ttu-id="a80a4-177">Oprettelse af købsordren</span><span class="sxs-lookup"><span data-stu-id="a80a4-177">Creating the Purchase Order</span></span>  
<span data-ttu-id="a80a4-178">Købsordrer er den mest almindelige type indgående kildedokument.</span><span class="sxs-lookup"><span data-stu-id="a80a4-178">Purchase orders are the most common type of inbound source document.</span></span>  

### <a name="to-create-the-purchase-order"></a><span data-ttu-id="a80a4-179">Hvis du vil oprette købsordren</span><span class="sxs-lookup"><span data-stu-id="a80a4-179">To create the purchase order</span></span>  

1.  <span data-ttu-id="a80a4-180">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="a80a4-180">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a80a4-181">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a80a4-181">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="a80a4-182">Opret en købsordre for kreditor 10000 på arbejdsdatoen (23. januar) med følgende købsordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="a80a4-182">Create a purchase order for vendor 10000 on the work date (January 23) with the following purchase order lines.</span></span>  

    |<span data-ttu-id="a80a4-183">Vare</span><span class="sxs-lookup"><span data-stu-id="a80a4-183">Item</span></span>|<span data-ttu-id="a80a4-184">Lokationskode</span><span class="sxs-lookup"><span data-stu-id="a80a4-184">Location code</span></span>|<span data-ttu-id="a80a4-185">Placeringskode</span><span class="sxs-lookup"><span data-stu-id="a80a4-185">Bin code</span></span>|<span data-ttu-id="a80a4-186">Antal</span><span class="sxs-lookup"><span data-stu-id="a80a4-186">Quantity</span></span>|  
    |----------|-------------------|--------------|--------------|  
    |<span data-ttu-id="a80a4-187">LS_75</span><span class="sxs-lookup"><span data-stu-id="a80a4-187">LS_75</span></span>|<span data-ttu-id="a80a4-188">SØLV</span><span class="sxs-lookup"><span data-stu-id="a80a4-188">SILVER</span></span>|<span data-ttu-id="a80a4-189">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="a80a4-189">S-01-0001</span></span>|<span data-ttu-id="a80a4-190">10</span><span class="sxs-lookup"><span data-stu-id="a80a4-190">10</span></span>|  
    |<span data-ttu-id="a80a4-191">LS-81</span><span class="sxs-lookup"><span data-stu-id="a80a4-191">LS-81</span></span>|<span data-ttu-id="a80a4-192">SØLV</span><span class="sxs-lookup"><span data-stu-id="a80a4-192">SILVER</span></span>|<span data-ttu-id="a80a4-193">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="a80a4-193">S-01-0001</span></span>|<span data-ttu-id="a80a4-194">30</span><span class="sxs-lookup"><span data-stu-id="a80a4-194">30</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="a80a4-195">Placeringskoden angives automatisk i overensstemmelse med opsætningen, som du har foretaget i afsnittet "Indstilling af lokation".</span><span class="sxs-lookup"><span data-stu-id="a80a4-195">The bin code is entered automatically according to the setup that you performed in the “Setting up the Location” section.</span></span>  

    <span data-ttu-id="a80a4-196">Fortsæt ved at meddele lageret, at købsordren er klar til lagerekspedition, når leverancen ankommer.</span><span class="sxs-lookup"><span data-stu-id="a80a4-196">Proceed to notify the warehouse that the purchase order is ready for warehouse handling when the delivery arrives.</span></span>  

4.  <span data-ttu-id="a80a4-197">Vælg handlingen **Frigivelse**.</span><span class="sxs-lookup"><span data-stu-id="a80a4-197">Choose the **Release** action.</span></span>  

    <span data-ttu-id="a80a4-198">Leverancen af højttalere fra kreditor 10000 er modtaget på SØLV-lageret, og John fortsætter med at lægge dem på plads.</span><span class="sxs-lookup"><span data-stu-id="a80a4-198">The delivery of loudspeakers from vendor 10000 has arrived at SILVER warehouse, and John proceeds to put them away.</span></span>  

## <a name="receiving-and-putting-the-items-away"></a><span data-ttu-id="a80a4-199">Modtagelse og placering af varer på lager</span><span class="sxs-lookup"><span data-stu-id="a80a4-199">Receiving and Putting the Items Away</span></span>  
<span data-ttu-id="a80a4-200">På siden **Læg-på-lager** kan du administrere alle indgående lageraktiviteter til et specifikt kildedokument, f.eks. en købsordre.</span><span class="sxs-lookup"><span data-stu-id="a80a4-200">On the **Inventory Put-away** page, you can manage all inbound warehouse activities for a specific source document, such as a purchase order.</span></span>  

### <a name="to-receive-and-put-the-items-away"></a><span data-ttu-id="a80a4-201">Sådan modtager du varerne og lægger dem på lager</span><span class="sxs-lookup"><span data-stu-id="a80a4-201">To receive and put the items away</span></span>  

1.  <span data-ttu-id="a80a4-202">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Læg-på-lager-akt. (lager)**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="a80a4-202">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Put-aways**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a80a4-203">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a80a4-203">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="a80a4-204">Vælg feltet **Kildedokument**, og vælg derefter **Købsordre**.</span><span class="sxs-lookup"><span data-stu-id="a80a4-204">Select the **Source Document** field, and then select **Purchase Order**.</span></span>  
4.  <span data-ttu-id="a80a4-205">Vælg feltet **Kildenr.**, vælg linjen til købet fra kreditor 10000, og vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="a80a4-205">Select the **Source No.** field, select the line for the purchase from vendor 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="a80a4-206">Du kan også vælge handlingen **Hent kildedokument** og derefter vælge købsordren.</span><span class="sxs-lookup"><span data-stu-id="a80a4-206">Alternatively, choose the **Get Source Document** action, and then select the purchase order.</span></span>  

5.  <span data-ttu-id="a80a4-207">Vælg handlingen **Autofyld håndteringsantal**.</span><span class="sxs-lookup"><span data-stu-id="a80a4-207">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="a80a4-208">Du kan også indtaste henholdsvis 10 og 30 på de to læg-på-lager-linjer i feltet **Håndteringsantal**.</span><span class="sxs-lookup"><span data-stu-id="a80a4-208">Alternatively, in the **Qty. to Handle** field, enter 10 and 30 respectively on the two inventory put-away lines.</span></span>  

6.  <span data-ttu-id="a80a4-209">Vælg handlingen **Bogfør**, vælg handlingen **Modtag**, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="a80a4-209">Choose the **Post** action, select the **Receive** action, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="a80a4-210">De 40 højttalere er nu registreret som lagt på lager på placering S-01-0001, og der oprettes en positiv varepost, der afspejler den bogførte købsmodtagelse.</span><span class="sxs-lookup"><span data-stu-id="a80a4-210">The 40 loudspeakers are now registered as put away in bin S-01-0001, and a positive item ledger entry is created reflecting the posted purchase receipt.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a80a4-211">Se også</span><span class="sxs-lookup"><span data-stu-id="a80a4-211">See Also</span></span>  
 <span data-ttu-id="a80a4-212">[Lægge varer på lager med Læg-på-lager (lager)](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span><span class="sxs-lookup"><span data-stu-id="a80a4-212">[Put Items Away with Inventory Put-aways](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span></span>  
 <span data-ttu-id="a80a4-213">[Oprette grundlæggende lagersteder med handlingsområder](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span><span class="sxs-lookup"><span data-stu-id="a80a4-213">[Set Up Basic Warehouses with Operations Areas](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span></span>  
 <span data-ttu-id="a80a4-214">[Flytte komponenter til et handlingsområde i grundlæggende lageropsætninger](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="a80a4-214">[Move Components to an Operation Area in Basic Warehouse Configurations](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="a80a4-215">[Plukke til produktion eller montage](warehouse-how-to-pick-for-production.md) </span><span class="sxs-lookup"><span data-stu-id="a80a4-215">[Pick for Production or Assembly](warehouse-how-to-pick-for-production.md) </span></span>  
 <span data-ttu-id="a80a4-216">[Flytte varer ad hoc i grundlæggende lageropsætninger](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="a80a4-216">[Move Items Ad Hoc in Basic Warehouse Configurations](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="a80a4-217">[Designoplysninger: Indgående lagerflow](design-details-inbound-warehouse-flow.md) </span><span class="sxs-lookup"><span data-stu-id="a80a4-217">[Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md) </span></span>  
 [<span data-ttu-id="a80a4-218">Gennemgang af forretningsprocesser</span><span class="sxs-lookup"><span data-stu-id="a80a4-218">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="a80a4-219">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a80a4-219">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
