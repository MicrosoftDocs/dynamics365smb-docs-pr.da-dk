---
title: "Sådan tildeles standardplaceringer til varer | Microsoft Docs"
description: "Hvis du bruger placeringer på en lokation, kan du levere, modtage og flytte varerne meget mere effektivt ved at tildele varerne standardplaceringer. Når en vare tildeles en standardplacering, foreslås denne placering, hver gang du starter en transaktion for denne vare."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 826e1392143b166566619c5aef8c28ac2b09bc22
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="assign-default-bins-to-items"></a><span data-ttu-id="8c666-104">Tildele standardplaceringer til varer</span><span class="sxs-lookup"><span data-stu-id="8c666-104">Assign Default Bins to Items</span></span>
<span data-ttu-id="8c666-105">Hvis du bruger placeringer på en lokation, kan du levere, modtage og flytte varerne meget mere effektivt ved at tildele varerne standardplaceringer.</span><span class="sxs-lookup"><span data-stu-id="8c666-105">If you are using bins at a location, assigning default bins to your items can make the process of shipping, receiving, and moving your items much easier.</span></span> <span data-ttu-id="8c666-106">Når en vare tildeles en standardplacering, foreslås denne placering, hver gang du starter en transaktion for denne vare.</span><span class="sxs-lookup"><span data-stu-id="8c666-106">When a default bin is assigned to an item, this bin is suggested every time you initiate a transaction for this item.</span></span> <span data-ttu-id="8c666-107">Standardplaceringer er defineret i vinduet **Placeringsindhold**.</span><span class="sxs-lookup"><span data-stu-id="8c666-107">Default bins are defined in the **Bin Content** window.</span></span>  

## <a name="to-assign-a-default-bin-to-an-item"></a><span data-ttu-id="8c666-108">Sådan tildeles en standardplacering til en vare</span><span class="sxs-lookup"><span data-stu-id="8c666-108">To assign a default bin to an item</span></span>
1.  <span data-ttu-id="8c666-109">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opr.kladde til placeringsindh.**, og vælg det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="8c666-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bin Content Creation Worksheet**, and choose the related link.</span></span>  
2.  <span data-ttu-id="8c666-110">Udfyld oplysningerne om placeringskoden og varen for hver placering, du vil angive som standard for en vare.</span><span class="sxs-lookup"><span data-stu-id="8c666-110">Fill in the bin code and item information for each bin that you would like to set up as a default for an item.</span></span> <span data-ttu-id="8c666-111">Sørg for at vælge feltet **Standard**.</span><span class="sxs-lookup"><span data-stu-id="8c666-111">Make sure to select the **Default** field.</span></span>  
3.  <span data-ttu-id="8c666-112">Vælg handlingen **Opret placeringsindhold**.</span><span class="sxs-lookup"><span data-stu-id="8c666-112">Choose the **Create Bin Content** action.</span></span> <span data-ttu-id="8c666-113">Varen tildeles nu standardplaceringer.</span><span class="sxs-lookup"><span data-stu-id="8c666-113">Default bins are now assigned for your item.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="8c666-114">Når en vare lægges på lager, og varen ikke er tildelt en standardplacering, bliver den placering, som varen lægges på lager på, standardplaceringen.</span><span class="sxs-lookup"><span data-stu-id="8c666-114">When an item is put away, if the item does not have a default bin assigned, the bin where the item is put away is assigned as the default.</span></span>  

## <a name="to-change-the-default-bin-for-an-item"></a><span data-ttu-id="8c666-115">Sådan ændres standardplaceringen for en vare</span><span class="sxs-lookup"><span data-stu-id="8c666-115">To change the default bin for an item</span></span>  
<span data-ttu-id="8c666-116">Det kan være nødvendigt at ændre den tildelte standardplacering for en vare eller at tildele en standardplacering til en ny vare.</span><span class="sxs-lookup"><span data-stu-id="8c666-116">You may need to change the default bin assignment for an item or assign a default bin to a new item.</span></span>    
1.  <span data-ttu-id="8c666-117">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Placeringsindhold**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="8c666-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bin Contents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="8c666-118">Vælg den relevante lokationskode i feltet **Lokationsfilter**.</span><span class="sxs-lookup"><span data-stu-id="8c666-118">In the **Location Filter** field, select the appropriate location code.</span></span>  
3.  <span data-ttu-id="8c666-119">Søg efter den aktuelle post for standardplaceringsindholdet for varen, og fjern markeringen i afkrydsningsfeltet **Standardplacering**.</span><span class="sxs-lookup"><span data-stu-id="8c666-119">Find the current default bin content entry for the item and clear the **Default Bin** check box.</span></span>  
4.  <span data-ttu-id="8c666-120">Søg efter linjen Placeringsindhold for den placering, du vil anvende som den nye standardplacering.</span><span class="sxs-lookup"><span data-stu-id="8c666-120">Find the bin content line for the bin that you would like as the new default bin.</span></span> <span data-ttu-id="8c666-121">Marker afkrydsningsfeltet **Standardplacering**.</span><span class="sxs-lookup"><span data-stu-id="8c666-121">Select the **Default Bin** check box.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="8c666-122">Når en vare lægges på lager første gang, og varen ikke er tildelt en standardplacering, bliver den placering, som varen lægges på lager på, standardplaceringen for varen.</span><span class="sxs-lookup"><span data-stu-id="8c666-122">When an item is put away for the first time, and the item does not have a default bin assigned, the system will assign the bin where the item is put away as the default bin for the item.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8c666-123">Se også</span><span class="sxs-lookup"><span data-stu-id="8c666-123">See Also</span></span>  
[<span data-ttu-id="8c666-124">Logistik</span><span class="sxs-lookup"><span data-stu-id="8c666-124">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="8c666-125">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="8c666-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="8c666-126">[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="8c666-126">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="8c666-127">[Montagestyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="8c666-127">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="8c666-128">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="8c666-128">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="8c666-129">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8c666-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

