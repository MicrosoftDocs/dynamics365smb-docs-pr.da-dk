---
title: "Sådan konfigureres varer og lokationer til styret læg-på-lager og pluk | Microsoft Docs"
description: "Når lagerlokationen kræver styret læg-på-lager og pluk, kan du bruge en ny funktion, der hjælper dig med at styre lagerstedet på den mest effektive måde."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9b41bb902d8a2298f438233ca24c5a7bcf7f69d9
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-items-and-locations-for-directed-put-away-and-pick"></a><span data-ttu-id="f5937-103">Sådan konfigureres varer og lokationer til styret læg-på-lager og pluk</span><span class="sxs-lookup"><span data-stu-id="f5937-103">How to: Set Up Items and Locations for Directed Put-away and Pick</span></span>
<span data-ttu-id="f5937-104">Når lagerlokationen kræver styret læg-på-lager og pluk, kan du bruge en ny funktion, der hjælper dig med at styre lagerstedet på den mest effektive måde.</span><span class="sxs-lookup"><span data-stu-id="f5937-104">When you set up a warehouse location for directed put-away and pick, you have new functionality available to you to help run the warehouse in the most efficient way possible.</span></span> <span data-ttu-id="f5937-105">Hvis du vil have fuldt udbytte af denne funktion, skal du give yderligere oplysninger om varerne, som til gengæld hjælper med at foretage de nødvendige beregninger for at kunne give forslag til de mest effektive måder at styre lageraktiviteter på.</span><span class="sxs-lookup"><span data-stu-id="f5937-105">In order to make full use of this functionality, you provide additional information about the items, which in turn helps to make the calculations necessary to suggest the most efficient and effective ways to conduct warehouse activities.</span></span> <span data-ttu-id="f5937-106">Du kan finde flere oplysninger i [Designoplysninger: Opsætning af lager](design-details-warehouse-setup.md)</span><span class="sxs-lookup"><span data-stu-id="f5937-106">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>

## <a name="to-set-up-an-item-for-directed-put-away-and-pick"></a><span data-ttu-id="f5937-107">Sådan opsættes varer til styret læg-på-lager og pluk</span><span class="sxs-lookup"><span data-stu-id="f5937-107">To set up an item for directed put-away and pick</span></span>  
1.  <span data-ttu-id="f5937-108">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f5937-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f5937-109">Åbn kortet for den vare, som du vil konfigurere til styret læg-på-lager og pluk.</span><span class="sxs-lookup"><span data-stu-id="f5937-109">Open the card for the item that you want to set up for directed put-away and pick.</span></span>
3. <span data-ttu-id="f5937-110">Udfyld felterne i oversigtspanelet **Lagersted** på varekortet for at definere, hvordan varen skal håndteres på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="f5937-110">On the **Warehouse** FastTab of the item card, fill in the fields to define how the item should be handled in the warehouse.</span></span>  
4.  <span data-ttu-id="f5937-111">Vælg handlingen **Enheder**.</span><span class="sxs-lookup"><span data-stu-id="f5937-111">Choose the **Units of Measure** action.</span></span>
5. <span data-ttu-id="f5937-112">I vinduet **Enheder** skal du udfylde felterne for at definere de forskellige enheder, som varen kan håndteres i, herunder højde, bredde, længde, rummål og vægt for enheden.</span><span class="sxs-lookup"><span data-stu-id="f5937-112">In the **Item Units of Measure** window, fill in the fields to define the different units of measure in which the item may be transacted, including the height, width, length, cubage, and weight for the unit of measure.</span></span>
6. <span data-ttu-id="f5937-113">Vælg handlingen **Placeringsindhold**.</span><span class="sxs-lookup"><span data-stu-id="f5937-113">Choose the **Bin Contents** action.</span></span>
7. <span data-ttu-id="f5937-114">I vinduet **Placeringsindhold** kan du definere de lokationer og placeringer, som varen skal tilknyttes.</span><span class="sxs-lookup"><span data-stu-id="f5937-114">In the **Bin Contents** window, define the location and bin to which the item should be associated.</span></span> <span data-ttu-id="f5937-115">Feltet **Standard** bruges ikke, når lokationen kræver styret læg-på-lager og pluk.</span><span class="sxs-lookup"><span data-stu-id="f5937-115">The **Default** field is not used when the location is set up for directed put-away and pick.</span></span>  

## <a name="to-activate-directed-put-away-and-pick-functionality"></a><span data-ttu-id="f5937-116">Sådan aktiveres funktionaliteten styret læg-på-lager og pluk</span><span class="sxs-lookup"><span data-stu-id="f5937-116">To activate directed put away and pick functionality</span></span>  
<span data-ttu-id="f5937-117">Styret læg-på-lager og pluk giver dig adgang til funktioner for avanceret lageropsætning, der kan medføre en væsentlig forbedring af effektiviteten og dataenes pålidelighed.</span><span class="sxs-lookup"><span data-stu-id="f5937-117">Directed put-away and pick gives you access to advanced warehouse configuration features that can greatly enhance your efficiency and data reliability.</span></span> <span data-ttu-id="f5937-118">Hvis du vil bruge disse funktioner, skal du først opsætte en række parametre i lagerlokationen.</span><span class="sxs-lookup"><span data-stu-id="f5937-118">In order to use this functionality, you must first set up a number of parameters in your warehouse location.</span></span>  

<span data-ttu-id="f5937-119">Hvis du vil benytte styret læg-på-lager og pluk, skal du aktivere den tilknyttede funktionalitet på lokationskortet.</span><span class="sxs-lookup"><span data-stu-id="f5937-119">To use the directed put-away and pick functionality, you must activate the functionality on the location card.</span></span>    
1.  <span data-ttu-id="f5937-120">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lokationer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f5937-120">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f5937-121">Vælg den lokation, hvor du vil bruge styret læg-på-lager og pluk, og vælg derefter handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="f5937-121">Select the location where you want to use directed put-away and pick, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="f5937-122">I oversigtspanelet **Lagersted** skal du markere afkrydsningsfeltet **Styret læg-på-lager og pluk**.</span><span class="sxs-lookup"><span data-stu-id="f5937-122">On the **Warehouse** FastTab, select the **Directed Put-away and Pick** check box.</span></span>  

<span data-ttu-id="f5937-123">Det er ikke nødvendigt at udfylde andre felter på lokationskortet før senere i opsætningen.</span><span class="sxs-lookup"><span data-stu-id="f5937-123">You do not need to fill in any other fields on the location card until later in the setup process.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f5937-124">Du kan ikke sætte lageret op til at bruge placeringer, når lokationen har åbne vareposter.</span><span class="sxs-lookup"><span data-stu-id="f5937-124">You cannot set up the warehouse to use bins when the location has open item ledger entries.</span></span>  

<span data-ttu-id="f5937-125">Det næste trin er at definere de placeringer, du vil styre.</span><span class="sxs-lookup"><span data-stu-id="f5937-125">The next step is to define the type of bins you want to operate.</span></span> <span data-ttu-id="f5937-126">Du kan finde flere oplysninger i [Sådan oprettes placeringstyper](warehouse-how-to-set-up-bin-types.md).</span><span class="sxs-lookup"><span data-stu-id="f5937-126">For more information, see [How to: Set Up Bin Types](warehouse-how-to-set-up-bin-types.md).</span></span> <span data-ttu-id="f5937-127">Placeringstypen definerer, hvordan en angivet placering skal bruges, når varestrømmen behandles på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="f5937-127">The bin type defines how to use a given bin when processing the flow of items through the warehouse.</span></span> <span data-ttu-id="f5937-128">Du kan tildele en placeringstype til både en zone og en placering.</span><span class="sxs-lookup"><span data-stu-id="f5937-128">You can assign a bin type to both a zone and to a bin.</span></span>  

<span data-ttu-id="f5937-129">Du kan også definere lagerklassekoder, hvis der håndteres varer med forskellige krav til oplagringsforhold.</span><span class="sxs-lookup"><span data-stu-id="f5937-129">You can also define warehouse class codes, if the warehouse carries items that need various storage conditions.</span></span> <span data-ttu-id="f5937-130">Lagerklassekoder bruges, når der foreslås vareplaceringer. Du tildeler lagerklassekoder til produktgrupper, der derefter tildeles til varer og lagervarer eller til zoner og placeringer, der kan tilpasses de opbevaringsforhold, som er påkrævet i henhold til lagerklassekoderne.</span><span class="sxs-lookup"><span data-stu-id="f5937-130">Warehouse class codes are used when suggesting item placement in bins. You assign the warehouse class codes to product groups, which are then assigned to items and SKUs, or to zones and bins that can accommodate the storage conditions required by the warehouse class codes.</span></span>  

<span data-ttu-id="f5937-131">Du er nu klar til at opsætte zoner, hvis du vil arbejde med zoner på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="f5937-131">You are now ready to set up zones, if you want to operate zones in your warehouse.</span></span> <span data-ttu-id="f5937-132">Brugen af zoner nedsætter det antal felter, det er nødvendigt at udfylde, når du skal oprette placeringer, fordi de placeringer, der oprettes inden for en zone, automatisk overtager en række egenskaber fra denne.</span><span class="sxs-lookup"><span data-stu-id="f5937-132">Using zones reduces the number of fields you need to fill in when you set up your bins, because bins created within zones inherit several properties from the zone.</span></span> <span data-ttu-id="f5937-133">Zoner kan også gøre det nemmere for nye eller midlertidige medarbejdere at finde rundt på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="f5937-133">Zones can also make it easier for new or temporary employees to orient themselves in your warehouse.</span></span> <span data-ttu-id="f5937-134">Bemærk, at strømmen styres af placeringer. Det er derfor muligt at styre med placeringer og kun have én zone.</span><span class="sxs-lookup"><span data-stu-id="f5937-134">Note that flow is controlled by bins, therefore it is possible to operate with bins and only one zone.</span></span>  

## <a name="to-set-up-a-zone-in-your-warehouse"></a><span data-ttu-id="f5937-135">Sådan oprettes en zone på lagerstedet</span><span class="sxs-lookup"><span data-stu-id="f5937-135">To set up a zone in your warehouse</span></span>  
1.  <span data-ttu-id="f5937-136">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lokationer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f5937-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f5937-137">Vælg den lokation, hvor du vil oprette zone, åbn lokationskortet, og vælg derefter handlingen **Zoner**.</span><span class="sxs-lookup"><span data-stu-id="f5937-137">Select the location where you want to set up zone and open the location card, and then choose the **Zones** action.</span></span>  
3.  <span data-ttu-id="f5937-138">I vinduet **Zoner** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="f5937-138">In the **Zones** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

<span data-ttu-id="f5937-139">Når du ændrer en zoneparameter, vil alle placeringer i zonen, der oprettes efter dette tidspunkt, få de nye egenskaber, men de oprindelige placeringer ændres ikke.</span><span class="sxs-lookup"><span data-stu-id="f5937-139">When you change a zone parameter, all bins created thereafter in that zone will have the new characteristics, but the original bins will not be changed.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f5937-140">Hvis du vil arbejde uden zoner, skal du stadigvæk oprette en zonekode uden definition bortset fra koden.</span><span class="sxs-lookup"><span data-stu-id="f5937-140">If you want to operate without zones, you must still create one zone code that is undefined except for the code.</span></span>  

<span data-ttu-id="f5937-141">Det næste trin i opsætning af lagerstedet omfatter definition af placeringer. Du kan finde flere oplysninger under [Fremgangsmåde: Oprette lokationer til brug af placeringer](warehouse-how-to-set-up-locations-to-use-bins.md).</span><span class="sxs-lookup"><span data-stu-id="f5937-141">The next step in setting up the warehouse is to define bins. For more information, see [How to: Set Up Locations to Use Bins](warehouse-how-to-set-up-locations-to-use-bins.md).</span></span>  

<span data-ttu-id="f5937-142">Derudover skal du oprette læg-på-lager-skabeloner og optællingsperioder.</span><span class="sxs-lookup"><span data-stu-id="f5937-142">In addition, you must create put-away templates and counting periods.</span></span> <span data-ttu-id="f5937-143">Du kan finde flere oplysninger i [Sådan oprettes læg-på-lager-skabeloner](warehouse-how-to-set-up-put-away-templates.md).</span><span class="sxs-lookup"><span data-stu-id="f5937-143">For more information, see [How to: Set Up Put-away Templates](warehouse-how-to-set-up-put-away-templates.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="f5937-144">Se også</span><span class="sxs-lookup"><span data-stu-id="f5937-144">See Also</span></span>  
[<span data-ttu-id="f5937-145">Logistik</span><span class="sxs-lookup"><span data-stu-id="f5937-145">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="f5937-146">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="f5937-146">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="f5937-147">[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="f5937-147">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="f5937-148">[Montagestyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="f5937-148">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="f5937-149">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="f5937-149">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="f5937-150">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f5937-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
