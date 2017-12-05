---
title: "Sådan beregnes genopfyldning | Microsoft Docs"
description: "Når lokationen er konfigureret til at bruge styret læg-på-lager og pluk, tages prioriteterne i læg-på-lager-skabelonen for lokationen i betragtning, når leverancer lægges på lager."
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
ms.openlocfilehash: a683d2f88f8c30d457d44facd21b0068688ad05a
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-calculate-bin-replenishment"></a><span data-ttu-id="0cf30-103">Sådan beregnes genopfyldning</span><span class="sxs-lookup"><span data-stu-id="0cf30-103">How to: Calculate Bin Replenishment</span></span>
<span data-ttu-id="0cf30-104">Når lokationen er konfigureret til at bruge styret læg-på-lager og pluk, tages prioriteterne i læg-på-lager-skabelonen for lokationen i betragtning, når leverancer lægges på lager.</span><span class="sxs-lookup"><span data-stu-id="0cf30-104">When the location is set up to use directed put-away and pick, priorities of the put-away template for the location are taken into account when putting receipts away.</span></span> <span data-ttu-id="0cf30-105">Prioriteter omfatter de minimale og maksimale mængder af placeringsindhold, der er fastsat for en bestemt placering og placeringsniveauerne.</span><span class="sxs-lookup"><span data-stu-id="0cf30-105">Priorities include the minimum and maximum quantities of bin content that have been fixed for a particular bin, and the bin rankings.</span></span> <span data-ttu-id="0cf30-106">Hvis varerne ankommer i en stadig strøm, fyldes de oftest benyttede plukplaceringer derfor op, efterhånden som de tømmes.</span><span class="sxs-lookup"><span data-stu-id="0cf30-106">Therefore, if items are arriving at a steady pace, the most-used pick bins will be filled up as they are emptied.</span></span>  

<span data-ttu-id="0cf30-107">Men lagervarer ankommer ikke altid i en stadig strøm.</span><span class="sxs-lookup"><span data-stu-id="0cf30-107">But inventory does not always arrive in a steady trickle.</span></span> <span data-ttu-id="0cf30-108">Nogle gange købes varer i store mængder, så virksomheden kan få en rabat, eller en produktionsenhed kan give mange af ét element for at opnå en lav kostpris.</span><span class="sxs-lookup"><span data-stu-id="0cf30-108">Sometimes, items are purchased in large quantities so that the company can obtain a rebate, or your production unit might produce a lot of one item to achieve a low unit cost.</span></span> <span data-ttu-id="0cf30-109">Derefter vil varer ikke blive modtaget på lageret igen i et stykke tid, og lageret skal med jævne mellemrum flytte varer til plukplaceringer fra massevarelageret.</span><span class="sxs-lookup"><span data-stu-id="0cf30-109">Then items will not be received in the warehouse again for some time, and the warehouse needs to periodically move items to pick bins from bulk storage areas.</span></span>  

<span data-ttu-id="0cf30-110">Det kan også være, at lagerstedet vil foregribe modtagelsen af nye varer ved at tømme massevarelageret for varer, før de nye varer ankommer.</span><span class="sxs-lookup"><span data-stu-id="0cf30-110">It could also be that the warehouse is expecting new stock to arrive soon and wants to empty the bulk storage area of items before the new merchandise arrives.</span></span>  

<span data-ttu-id="0cf30-111">Hvis du udelukkende har fastsat placeringstypen for massevareplaceringer til **Læg-på-lager**, dvs. at handlingen **Pluk** ikke er markeret for placeringstypen, skal du altid sørge for, at plukplaceringerne genopfyldes, da typen Læg-på-lager ikke er foreslået for et pluk fra placeringer.</span><span class="sxs-lookup"><span data-stu-id="0cf30-111">Finally, if you have defined your bulk storage bins with a bin type action **Put Away** only, that is, the bin type does not have the **Pick** action selected, you must always keep your pick bins replenished, since Put Away-type bins are not suggested for a pick of inventory.</span></span>  

## <a name="to-replenish-pick-bins"></a><span data-ttu-id="0cf30-112">Sådan genopfyldes plukplaceringer</span><span class="sxs-lookup"><span data-stu-id="0cf30-112">To replenish pick bins</span></span>  
1.  <span data-ttu-id="0cf30-113">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bevægelseskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="0cf30-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0cf30-114">Vælg handlingen **Beregn genopfyldning** for at åbne rapportanmodningssiden.</span><span class="sxs-lookup"><span data-stu-id="0cf30-114">Choose the **Calculate Bin Replenishment** action to open the report request page.</span></span>  
3.  <span data-ttu-id="0cf30-115">Udfyld de relevante felter i vinduet for at begrænse omfanget af genopfyldningsforslag, der skal beregnes.</span><span class="sxs-lookup"><span data-stu-id="0cf30-115">Fill in the batch job request window to limit the scope of the replenishment suggestions that will be calculated.</span></span> <span data-ttu-id="0cf30-116">Det kan f.eks. være, at du kun vil have forslag, der berører bestemte varer, zoner eller placeringer.</span><span class="sxs-lookup"><span data-stu-id="0cf30-116">For example, you might be concerned with particular items, zones, or bins.</span></span>  
4.  <span data-ttu-id="0cf30-117">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="0cf30-117">Choose the **OK** button.</span></span> <span data-ttu-id="0cf30-118">Der oprettes nu linjer for de genopfyldningsbevægelser, der skal udføres ifølge de regler, der er defineret for placeringer og placeringsindhold varerne på placeringerne.</span><span class="sxs-lookup"><span data-stu-id="0cf30-118">Lines are created for the replenishment movements that need to be performed according to the rules that have been set up for the bins and bin contents, that is, items in bins.</span></span>  
5.  <span data-ttu-id="0cf30-119">Vælg handlingen **Opret bevægelse**, hvis du vil udføre alle de foreslåede genopfyldninger.</span><span class="sxs-lookup"><span data-stu-id="0cf30-119">If you want to perform all the suggested replenishments, choose the **Create Movement** action.</span></span> <span data-ttu-id="0cf30-120">Der er nu oprettet instruktioner i menuen **Bevægelser**, som kan udføres og registreres af lagermedarbejderne.</span><span class="sxs-lookup"><span data-stu-id="0cf30-120">Employees can now find instructions in the **Movements** menu item, carry them out and register them.</span></span>  
6.  <span data-ttu-id="0cf30-121">Hvis du kun vil have udført nogle af forslagene, skal du slette de mindst vigtige og derefter oprette en bevægelse.</span><span class="sxs-lookup"><span data-stu-id="0cf30-121">If you only want some of the suggestions to be performed, delete the lines that are less important and then create a movement.</span></span>  

<span data-ttu-id="0cf30-122">Næste gang du beregner genopfyldning, vil de forslag, som du har slettet, blive genoprettet, hvis de stadig er gyldige til den tid.</span><span class="sxs-lookup"><span data-stu-id="0cf30-122">The next time you calculate bin replenishment, the suggestions that you have deleted will be recreated, if they are still valid at that time.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0cf30-123">Hvis en vare opfylder følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="0cf30-123">If the following conditions are met for an item:</span></span>  
>   
>  -   <span data-ttu-id="0cf30-124">Varen har en udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="0cf30-124">The item has an expiration date, and</span></span>  
> -   <span data-ttu-id="0cf30-125">Feltet **Vælg i overensstemmelse med FEFO** på lokationskortet er markeret, og</span><span class="sxs-lookup"><span data-stu-id="0cf30-125">The **Pick According to FEFO** field on the location card is selected, and</span></span>  
> -   <span data-ttu-id="0cf30-126">Du bruger funktionen **Beregn genopfyldning**</span><span class="sxs-lookup"><span data-stu-id="0cf30-126">You use the **Calculate Bin Replenishment** functionality</span></span>  
>   
>  <span data-ttu-id="0cf30-127">Hvis alle disse betingelser er opfyldt, vil felterne **Fra zonekode** og **Fra placeringskode** være tomme, fordi den algoritme, der beregner, hvorfra varerne skal bevæges, kun udløses, når du aktiverer funktionen **Opret bevægelse**.</span><span class="sxs-lookup"><span data-stu-id="0cf30-127">then the **From Zone** and **From Bin** fields will be blank because the algorithm to calculate from where to move the items is triggered only when you activate the **Create Movement** function.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0cf30-128">Se også</span><span class="sxs-lookup"><span data-stu-id="0cf30-128">See Also</span></span>  
[<span data-ttu-id="0cf30-129">Logistik</span><span class="sxs-lookup"><span data-stu-id="0cf30-129">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="0cf30-130">Plukke efter FEFO</span><span class="sxs-lookup"><span data-stu-id="0cf30-130">Picking by FEFO</span></span>](warehouse-picking-by-fefo.md)  
[<span data-ttu-id="0cf30-131">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="0cf30-131">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="0cf30-132">[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="0cf30-132">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="0cf30-133">[Montagestyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="0cf30-133">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="0cf30-134">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="0cf30-134">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="0cf30-135">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0cf30-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
