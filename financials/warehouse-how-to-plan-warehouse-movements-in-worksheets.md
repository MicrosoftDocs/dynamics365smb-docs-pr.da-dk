---
title: "Sådan planlægges lagerbevægelser i kladder | Microsoft Docs"
description: "Planlæg bevægelser i en kladde vha. funktionen Placeringsgenopfyldning eller manuelt ved at planlægge de linjer, som du vil oprette bevægelsesinstruktioner til."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 397b7d3de0355ce6be1be6607e5cfc7f61b5f55d
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="plan-warehouse-movements-in-worksheets"></a><span data-ttu-id="9aeed-103">Planlægge lagerbevægelser i kladder</span><span class="sxs-lookup"><span data-stu-id="9aeed-103">Plan Warehouse Movements in Worksheets</span></span>
<span data-ttu-id="9aeed-104">Planlæg bevægelser i en kladde vha. funktionen Placeringsgenopfyldning eller manuelt ved at planlægge de linjer, som du vil oprette bevægelsesinstruktioner til.</span><span class="sxs-lookup"><span data-stu-id="9aeed-104">Plan movements in the worksheet using a bin replenishment function or manually planning the lines that you want to create as movement instructions.</span></span>  

## <a name="to-calculate-a-replenishment-movement"></a><span data-ttu-id="9aeed-105">Sådan beregnes placeringsgenopfyldning</span><span class="sxs-lookup"><span data-stu-id="9aeed-105">To calculate a replenishment movement</span></span>  
<span data-ttu-id="9aeed-106">Efterhånden som lagerstedet afsender varer, bliver der færre og færre varer på placeringerne med de højeste placeringsniveauer.</span><span class="sxs-lookup"><span data-stu-id="9aeed-106">As the warehouse ships items out to customers, the bins with the highest bin rankings contain fewer and fewer items.</span></span> <span data-ttu-id="9aeed-107">For at genopfylde disse placeringer med varer fra andre placeringer bruger du funktionen **Beregn genopfyldning** i vinduet **Bevægelseskladde**.</span><span class="sxs-lookup"><span data-stu-id="9aeed-107">To fill up these high-ranking pick bins with items from other bins, run the **Calculate Bin Replenishment** function in the **Movement Worksheet** window</span></span>

1.  <span data-ttu-id="9aeed-108">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bevægelseskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="9aeed-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9aeed-109">Vælg handlingen **Beregn genopfyldning**.</span><span class="sxs-lookup"><span data-stu-id="9aeed-109">Choose the **Calculate Bin Replenishment** action.</span></span>  

    [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="9aeed-110"> opretter automatisk linjer, der præcist angiver, hvordan du skal flytte varer fra placeringer med lavt placeringsniveau til placeringer med højt placeringsniveau.</span><span class="sxs-lookup"><span data-stu-id="9aeed-110">creates lines that indicate precisely how you should move items from the low-ranking bins to the higher-ranking bins.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="9aeed-111">Der foreslås en bevægelse i henhold til FEFO, når du aktiverer funktionen **Opret bevægelse**, hvis følgende betingelser er opfyldt for en vare:</span><span class="sxs-lookup"><span data-stu-id="9aeed-111">A movement is suggested according to FEFO when you activate the **Create Movement** function if the following conditions are met for an item:</span></span>  
    >   
    >  -   <span data-ttu-id="9aeed-112">Varen har en udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="9aeed-112">The item has an expiration date.</span></span>  
    > -   <span data-ttu-id="9aeed-113">Afkrydsningsfeltet **Vælg i overensstemmelse med FEFO** på lokationskortet er markeret.</span><span class="sxs-lookup"><span data-stu-id="9aeed-113">The **Pick According to FEFO** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="9aeed-114">Afkrydsningsfeltet **Tvungen placering** på lokationskortet er markeret.</span><span class="sxs-lookup"><span data-stu-id="9aeed-114">The **Bin Mandatory** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="9aeed-115">Felterne **Fra zonekode** og **Fra placeringskode** er tomme.</span><span class="sxs-lookup"><span data-stu-id="9aeed-115">The **From Zone** and **From Bin** fields are blank.</span></span>  

    <span data-ttu-id="9aeed-116">Du kan finde flere oplysninger i [Plukke efter FEFO](warehouse-picking-by-fefo.md).</span><span class="sxs-lookup"><span data-stu-id="9aeed-116">For more information, see [Picking by FEFO](warehouse-picking-by-fefo.md).</span></span>  

3.  <span data-ttu-id="9aeed-117">Kontroller linjerne, og ret dem efter behov, eller slet nogle af dem, hvis der ikke er tid nok til at udføre dem alle.</span><span class="sxs-lookup"><span data-stu-id="9aeed-117">Look through the lines and change them if necessary, or delete some of them if there is not enough time to perform them all.</span></span>  
4.  <span data-ttu-id="9aeed-118">Vælg handlingen **Opret bevægelse** for at oprette en instruktion til lagermedarbejderne.</span><span class="sxs-lookup"><span data-stu-id="9aeed-118">Choose the **Create Movement** action to make a warehouse instruction for action by warehouse employees.</span></span>  

## <a name="to-move-the-entire-contents-of-one-or-more-bins-by-using-the-get-bin-content-function"></a><span data-ttu-id="9aeed-119">Sådan kan du flytte hele indholdet af en eller flere placeringer ved hjælp af funktionen Hent placeringsindh.</span><span class="sxs-lookup"><span data-stu-id="9aeed-119">To move the entire contents of one or more bins by using the Get Bin Content function</span></span>  
<span data-ttu-id="9aeed-120">Du kan også bruge bevægelseskladden til at planlægge andre former for varebevægelser på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="9aeed-120">You can also use the movement worksheet to plan other movement of inventory within the warehouse.</span></span> <span data-ttu-id="9aeed-121">Hvis der f.eks. skal flyttes varer til en placering til kvalitetskontrol, kan du bruge bevægelseskladden til at planlægge handlingen og derefter oprette en bevægelse for at udarbejde instruktioner til en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="9aeed-121">For example, when you want to place items in a bin for quality control, you can use the movement worksheet to plan this action and then create a movement to make instructions for an employee.</span></span>  

1.  <span data-ttu-id="9aeed-122">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bevægelseskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="9aeed-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9aeed-123">Vælg handlingen **Hent placeringsindhold**.</span><span class="sxs-lookup"><span data-stu-id="9aeed-123">Choose the **Get Bin Content** action.</span></span> <span data-ttu-id="9aeed-124">Brug vinduet til at filtrere for de placeringer og varer, der skal vises på bevægelseskladdelinjerne.</span><span class="sxs-lookup"><span data-stu-id="9aeed-124">Use the request window to filter which bins and items you want to appear on the movement worksheet lines.</span></span>  
3.  <span data-ttu-id="9aeed-125">Udfyld de relevante felter i kørselsvinduet.</span><span class="sxs-lookup"><span data-stu-id="9aeed-125">Fill in the relevant fields in the batch job request window.</span></span> <span data-ttu-id="9aeed-126">Hvis du f.eks. vil se placeringsindholdet af alle placeringer i en bestemt zone på en lokation, skal du udfylde feltet **Zonekode**.</span><span class="sxs-lookup"><span data-stu-id="9aeed-126">For example, if you want to see the bin content of all the bins in a certain zone at the location, fill in the **Zone Code** field.</span></span> <span data-ttu-id="9aeed-127">Hvis du vil hente linjerne for hver placering, der indeholder en bestemt vare, skal du udfylde feltet **Varenr.**.</span><span class="sxs-lookup"><span data-stu-id="9aeed-127">If you want to retrieve lines for each bin that contains a particular item, fill in the **Item No.** field.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="9aeed-128">Du kan ikke manuelt flytte varer ind eller ud af en placering af typen MODTAG, fordi varer, der findes i en placering af typen MODTAG, skal registreres som lagt på lager, før de bliver en del af den tilgængelige lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="9aeed-128">You cannot manually move items in or out of a bin of bin type RECEIVE, because items that are in a RECEIVE-type bin must be registered as being put away before they are part of available inventory.</span></span>  

4.  <span data-ttu-id="9aeed-129">Hvis du henter mange linjer, skal du vælge **Sorter** for at vælge en sorteringsmetode for de ordrelinjer, der vises i kladden, og derefter klikke på knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="9aeed-129">If you are retrieving many lines, choose **Sort** to select a sorting method to determine the order the lines will appear in the worksheet, and then choose the **OK** button.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="9aeed-130">Bevægelseslinjer hentes i henhold til FEFO, når du aktiverer funktionen **Hent placeringsindh.**, hvis følgende betingelser er opfyldt for en vare:</span><span class="sxs-lookup"><span data-stu-id="9aeed-130">Movement lines are retrieved according to FEFO when you activate the **Get Bin Content** function if the following conditions are met for an item:</span></span>  
    >   
    >  -   <span data-ttu-id="9aeed-131">Varen har en udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="9aeed-131">The item has an expiration date.</span></span>  
    > -   <span data-ttu-id="9aeed-132">Afkrydsningsfeltet **Vælg i overensstemmelse med FEFO** på lokationskortet er markeret.</span><span class="sxs-lookup"><span data-stu-id="9aeed-132">The **Pick According to FEFO** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="9aeed-133">Afkrydsningsfeltet **Tvungen placering** på lokationskortet er markeret.</span><span class="sxs-lookup"><span data-stu-id="9aeed-133">The **Bin Mandatory** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="9aeed-134">Felterne **Fra zonekode** og **Fra placeringskode** er tomme.</span><span class="sxs-lookup"><span data-stu-id="9aeed-134">The **From Zone** and **From Bin** fields are blank.</span></span>  

5.  <span data-ttu-id="9aeed-135">Udfyld nogle af de hentede linjer, så de afspejler de ændringer, du vil foretage.</span><span class="sxs-lookup"><span data-stu-id="9aeed-135">Complete some of the retrieved lines to reflect the changes you want to make.</span></span> <span data-ttu-id="9aeed-136">Udfyld felterne **Varenr.**, **Fra placeringskode**, **Til placeringskode** og **Antal** for hver af de varer, du vil flytte.</span><span class="sxs-lookup"><span data-stu-id="9aeed-136">For each item that you want to move, you must fill in the **Item No.**, **From Bin Code**, **To Bin Code**, and **Quantity** fields.</span></span>  
6.  <span data-ttu-id="9aeed-137">Slet de ikke-udfyldte linjer, du har brugt til oplysninger.</span><span class="sxs-lookup"><span data-stu-id="9aeed-137">Delete the incomplete lines that you used for information.</span></span>  
7.  <span data-ttu-id="9aeed-138">Når bevægelseskladdelinjerne nøjagtigt beskriver, hvordan bevægelsen skal udføres af lagermedarbejderen, skal du vælge handlingen **Opret bevægelse** for at oprette instruktionerne til medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="9aeed-138">Once the movement worksheet lines accurately reflect how the movement action should be carried out by the warehouse employee, choose the **Create Movement** action to create the instructions for the employee.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9aeed-139">Se også</span><span class="sxs-lookup"><span data-stu-id="9aeed-139">See Also</span></span>  
[<span data-ttu-id="9aeed-140">Logistik</span><span class="sxs-lookup"><span data-stu-id="9aeed-140">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="9aeed-141">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="9aeed-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="9aeed-142">[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="9aeed-142">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="9aeed-143">[Montagestyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="9aeed-143">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="9aeed-144">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="9aeed-144">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="9aeed-145">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9aeed-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

