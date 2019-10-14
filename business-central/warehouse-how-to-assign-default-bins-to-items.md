---
title: Sådan tildeles standardplaceringer til varer | Microsoft Docs
description: Hvis du bruger placeringer på en lokation, kan du levere, modtage og flytte varerne meget mere effektivt ved at tildele varerne standardplaceringer. Når en vare tildeles en standardplacering, foreslås denne placering, hver gang du starter en transaktion for denne vare.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 5183ce89e13b7d8aa33d3a32ebbe462cb024e9f2
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310416"
---
# <a name="assign-default-bins-to-items"></a><span data-ttu-id="27c8a-104">Tildele standardplaceringer til varer</span><span class="sxs-lookup"><span data-stu-id="27c8a-104">Assign Default Bins to Items</span></span>
<span data-ttu-id="27c8a-105">Hvis du bruger placeringer på en lokation, kan du levere, modtage og flytte varerne meget mere effektivt ved at tildele varerne standardplaceringer.</span><span class="sxs-lookup"><span data-stu-id="27c8a-105">If you are using bins at a location, assigning default bins to your items can make the process of shipping, receiving, and moving your items much easier.</span></span> <span data-ttu-id="27c8a-106">Når en vare tildeles en standardplacering, foreslås denne placering, hver gang du starter en transaktion for denne vare.</span><span class="sxs-lookup"><span data-stu-id="27c8a-106">When a default bin is assigned to an item, this bin is suggested every time you initiate a transaction for this item.</span></span> <span data-ttu-id="27c8a-107">Standardplaceringer er defineret på siden **Placeringsindhold**.</span><span class="sxs-lookup"><span data-stu-id="27c8a-107">Default bins are defined on the **Bin Content** page.</span></span>  

## <a name="to-assign-a-default-bin-to-an-item"></a><span data-ttu-id="27c8a-108">Sådan tildeles en standardplacering til en vare</span><span class="sxs-lookup"><span data-stu-id="27c8a-108">To assign a default bin to an item</span></span>
1.  <span data-ttu-id="27c8a-109">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opr.kladde til placeringsindh.**, og vælg det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="27c8a-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bin Content Creation Worksheet**, and choose the related link.</span></span>  
2.  <span data-ttu-id="27c8a-110">Udfyld oplysningerne om placeringskoden og varen for hver placering, du vil angive som standard for en vare.</span><span class="sxs-lookup"><span data-stu-id="27c8a-110">Fill in the bin code and item information for each bin that you would like to set up as a default for an item.</span></span> <span data-ttu-id="27c8a-111">Sørg for at vælge feltet **Standard**.</span><span class="sxs-lookup"><span data-stu-id="27c8a-111">Make sure to select the **Default** field.</span></span>  
3.  <span data-ttu-id="27c8a-112">Vælg handlingen **Opret placeringsindhold**.</span><span class="sxs-lookup"><span data-stu-id="27c8a-112">Choose the **Create Bin Content** action.</span></span> <span data-ttu-id="27c8a-113">Varen tildeles nu standardplaceringer.</span><span class="sxs-lookup"><span data-stu-id="27c8a-113">Default bins are now assigned for your item.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="27c8a-114">Når en vare lægges på lager, og varen ikke er tildelt en standardplacering, bliver den placering, som varen lægges på lager på, standardplaceringen.</span><span class="sxs-lookup"><span data-stu-id="27c8a-114">When an item is put away, if the item does not have a default bin assigned, the bin where the item is put away is assigned as the default.</span></span>  

## <a name="to-change-the-default-bin-for-an-item"></a><span data-ttu-id="27c8a-115">Sådan ændres standardplaceringen for en vare</span><span class="sxs-lookup"><span data-stu-id="27c8a-115">To change the default bin for an item</span></span>  
<span data-ttu-id="27c8a-116">Det kan være nødvendigt at ændre den tildelte standardplacering for en vare eller at tildele en standardplacering til en ny vare.</span><span class="sxs-lookup"><span data-stu-id="27c8a-116">You may need to change the default bin assignment for an item or assign a default bin to a new item.</span></span>    
1.  <span data-ttu-id="27c8a-117">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Placeringsindhold**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="27c8a-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bin Contents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="27c8a-118">Vælg den relevante lokationskode i feltet **Lokationsfilter**.</span><span class="sxs-lookup"><span data-stu-id="27c8a-118">In the **Location Filter** field, select the appropriate location code.</span></span>  
3.  <span data-ttu-id="27c8a-119">Søg efter den aktuelle post for standardplaceringsindholdet for varen, og fjern markeringen i afkrydsningsfeltet **Standardplacering**.</span><span class="sxs-lookup"><span data-stu-id="27c8a-119">Find the current default bin content entry for the item and clear the **Default Bin** check box.</span></span>  
4.  <span data-ttu-id="27c8a-120">Søg efter linjen Placeringsindhold for den placering, du vil anvende som den nye standardplacering.</span><span class="sxs-lookup"><span data-stu-id="27c8a-120">Find the bin content line for the bin that you would like as the new default bin.</span></span> <span data-ttu-id="27c8a-121">Marker afkrydsningsfeltet **Standardplacering**.</span><span class="sxs-lookup"><span data-stu-id="27c8a-121">Select the **Default Bin** check box.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="27c8a-122">Når en vare lægges på lager første gang, og varen ikke er tildelt en standardplacering, bliver den placering, som varen lægges på lager på, standardplaceringen for varen.</span><span class="sxs-lookup"><span data-stu-id="27c8a-122">When an item is put away for the first time, and the item does not have a default bin assigned, the system will assign the bin where the item is put away as the default bin for the item.</span></span>  

## <a name="see-also"></a><span data-ttu-id="27c8a-123">Se også</span><span class="sxs-lookup"><span data-stu-id="27c8a-123">See Also</span></span>  
[<span data-ttu-id="27c8a-124">Logistik</span><span class="sxs-lookup"><span data-stu-id="27c8a-124">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="27c8a-125">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="27c8a-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="27c8a-126">[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="27c8a-126">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="27c8a-127">[Montagestyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="27c8a-127">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="27c8a-128">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="27c8a-128">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="27c8a-129">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="27c8a-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
