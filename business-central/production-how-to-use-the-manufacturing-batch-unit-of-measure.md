---
title: Sådan bruges produktionskladdeenheden | Microsoft Docs
description: Hvis en vare lagerføres i én enhed, men produceres i en anden, skal produktionsordren bruge en produktionskladdeenhed til beregning af det rigtige antal komponenter. Produktionskladdeenheden kan f.eks. bruges til beregning, når den producerede vare lagerføres i enheder, men produceres i ton.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c78430de1c45646e54fb8551cd4a8dcfbbfcc4e4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383296"
---
# <a name="work-with-manufacturing-batch-units-of-measure"></a><span data-ttu-id="2f48b-104">Arbejde med produktionskladdeenheder</span><span class="sxs-lookup"><span data-stu-id="2f48b-104">Work with Manufacturing Batch Units of Measure</span></span>
<span data-ttu-id="2f48b-105">Hvis en vare lagerføres i én enhed, men produceres i en anden, kan der oprettes en produktionsordre, hvor der bruges en produktionskladdeenhed til beregning af det rigtige antal komponenter under kørslen af **Opdater produktionsordre**.</span><span class="sxs-lookup"><span data-stu-id="2f48b-105">If an item is stocked in one unit of measure but produced in another, a production order is created that uses a manufacturing batch unit of measure to calculate the correct quantity of the components during the **Refresh Production Order** batch job.</span></span> <span data-ttu-id="2f48b-106">Produktionskladdeenheden kan f.eks. bruges til beregning, når den producerede vare lagerføres i enheder, men produceres i ton.</span><span class="sxs-lookup"><span data-stu-id="2f48b-106">An example of a manufacturing batch unit of measure calculation is when a manufactured item is stocked in pieces but produced in tons.</span></span>  

## <a name="to-create-a-production-bom-using-a-batch-unit-of-measure"></a><span data-ttu-id="2f48b-107">Sådan oprettes en produktionsstykliste vha. en kladdeenhed</span><span class="sxs-lookup"><span data-stu-id="2f48b-107">To create a production BOM using a batch unit of measure</span></span>  
1.  <span data-ttu-id="2f48b-108">Produktionskladdeenheden oprettes som en alternativ enhed på siden **Vareenheder** til den vare, der skal produceres.</span><span class="sxs-lookup"><span data-stu-id="2f48b-108">The manufacturing batch unit of measure is set up as an alternative unit of measure on the **Item Units of Measure** page on the item to be produced.</span></span> <span data-ttu-id="2f48b-109">Kladdeenheden erstatter ikke varens basisenhed.</span><span class="sxs-lookup"><span data-stu-id="2f48b-109">The batch unit of measure will not replace the base unit of measure on the item.</span></span>  
2.  <span data-ttu-id="2f48b-110">Opret en produktionsstykliste til den vare, som du har oprettet produktionskladdeenheden til.</span><span class="sxs-lookup"><span data-stu-id="2f48b-110">Create a production BOM for the item set up with the manufacturing batch unit of measure.</span></span> <span data-ttu-id="2f48b-111">Du kan finde flere oplysninger i [Oprette produktionsstyklister](production-how-to-create-production-boms.md).</span><span class="sxs-lookup"><span data-stu-id="2f48b-111">For more information, see [Create Production BOMs](production-how-to-create-production-boms.md).</span></span>  
3.  <span data-ttu-id="2f48b-112">Vælg produktionskladdeenheden i feltet **Enhedskode**.</span><span class="sxs-lookup"><span data-stu-id="2f48b-112">In the **Unit of Measure Code** field, select the manufacturing batch unit of measure.</span></span>  
4.  <span data-ttu-id="2f48b-113">For hver linje i produktionsstyklisten skal du angive det komponentantal i feltet **Antal pr.** , som er en forudsætning for oprettelsen af denne kladdeenhed.</span><span class="sxs-lookup"><span data-stu-id="2f48b-113">For each production BOM line, in the **Quantity Per** field, enter the quantity of this component item that is required to create this batch unit of measure.</span></span>  
5.  <span data-ttu-id="2f48b-114">Åbn vinduet **Varekort** til den tilhørende vare.</span><span class="sxs-lookup"><span data-stu-id="2f48b-114">Open the **Item Card** for the related item.</span></span>  

    <span data-ttu-id="2f48b-115">Vælg den produktionsstykliste, du har oprettet ovenfor i feltet **Produktionsstyklistenr.** i oversigtspanelet **Genopfyldning**.</span><span class="sxs-lookup"><span data-stu-id="2f48b-115">On the **Replenishment** FastTab, in the **Production BOM No.** field, select the production BOM created above.</span></span>  
6.  <span data-ttu-id="2f48b-116">Opret et produktionsordrehoved ved at bruge den vare, som du har oprettet produktionskladdeenheden til.</span><span class="sxs-lookup"><span data-stu-id="2f48b-116">Create a production order header using the item set up with the manufacturing batch unit of measure.</span></span> <span data-ttu-id="2f48b-117">Du kan finde flere oplysninger i [Oprette produktionsordrer](production-how-to-create-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="2f48b-117">For more information, see [Create Production Orders](production-how-to-create-production-orders.md).</span></span>  
7.  <span data-ttu-id="2f48b-118">Vælg handlingen **Opdater**, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f48b-118">Choose the **Refresh** action, and then choose  the **OK** button.</span></span>  

<span data-ttu-id="2f48b-119">På oversigtspanelet **Linjer** skal du vælge handlingen **Linje** og derefter vælge handlingen **Komponenter** for at se resultatet.</span><span class="sxs-lookup"><span data-stu-id="2f48b-119">On the **Lines** FastTab, choose the **Line** action, and then choose the **Components** action to view the result.</span></span> <span data-ttu-id="2f48b-120">Nu beregnes det antal komponenter, som skal bruges til produktionsstyklisten i overensstemmelse med produktionskladdeenheden.</span><span class="sxs-lookup"><span data-stu-id="2f48b-120">The application calculates the correct quantity of the components needed to satisfy the production BOM based on the manufacturing batch unit of measure.</span></span>  

## <a name="to-calculate-a-manufacturing-batch-unit-of-measure-on-a-production-order"></a><span data-ttu-id="2f48b-121">Sådan beregnes en produktionskladdeenhed til en produktionsordre</span><span class="sxs-lookup"><span data-stu-id="2f48b-121">To calculate a manufacturing batch unit of measure on a production order</span></span>  
1.  <span data-ttu-id="2f48b-122">Opret et produktionsordrehoved ved at bruge den vare, som du har oprettet produktionskladdeenheden til.</span><span class="sxs-lookup"><span data-stu-id="2f48b-122">Create a production order header using the item set up with the manufacturing batch unit of measure.</span></span>  
2.  <span data-ttu-id="2f48b-123">I feltet **Varenr.** på produktionsordrelinjen skal du angive det samme varenummer, som du har angivet i hovedet.</span><span class="sxs-lookup"><span data-stu-id="2f48b-123">In the **Item No.** field in the Production Order line, type the same item number used in the header.</span></span>  
3.  <span data-ttu-id="2f48b-124">Angiv det samme antal, som du har angivet i hovedet, i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="2f48b-124">In the **Quantity** field, enter the same quantity used in the header.</span></span>  
4.  <span data-ttu-id="2f48b-125">Vælg produktionskladdeenhedskoden i feltet **Enhedskode**.</span><span class="sxs-lookup"><span data-stu-id="2f48b-125">In the **Unit of Measure Code** field, select the manufacturing batch unit of measure code.</span></span>  
5.  <span data-ttu-id="2f48b-126">Vælg handlingen **Opdater**.</span><span class="sxs-lookup"><span data-stu-id="2f48b-126">Choose the **Refresh** action.</span></span>
6.  <span data-ttu-id="2f48b-127">I oversigtspanelet **Beregn** skal du fjerne markeringen i afkrydsningsfeltet **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="2f48b-127">On the **Calculate** FastTab, clear the **Lines** check box.</span></span>  
7.  <span data-ttu-id="2f48b-128">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f48b-128">Choose the **OK** button.</span></span>  
8.  <span data-ttu-id="2f48b-129">På oversigtspanelet **Linjer** skal du vælge handlingen **Linje** og derefter vælge handlingen **Komponenter** for at se resultatet.</span><span class="sxs-lookup"><span data-stu-id="2f48b-129">On the **Lines** FastTab, choose the **Line** action, and then choose the **Components** action to view the result.</span></span> <span data-ttu-id="2f48b-130">Nu beregnes det antal komponenter, som skal bruges til produktionsstyklisten i overensstemmelse med produktionskladdeenheden.</span><span class="sxs-lookup"><span data-stu-id="2f48b-130">The correct quantity of the components needed to satisfy the production BOM is calculated based on the manufacturing batch unit of measure.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2f48b-131">Se også</span><span class="sxs-lookup"><span data-stu-id="2f48b-131">See Also</span></span>  
[<span data-ttu-id="2f48b-132">Oprette ruter</span><span class="sxs-lookup"><span data-stu-id="2f48b-132">Create Routings</span></span>](production-how-to-create-routings.md)  
<span data-ttu-id="2f48b-133">[Oprette produktionsstyklister](production-how-to-create-production-boms.md)   </span><span class="sxs-lookup"><span data-stu-id="2f48b-133">[Create Production BOMs](production-how-to-create-production-boms.md)   </span></span>  
[<span data-ttu-id="2f48b-134">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="2f48b-134">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="2f48b-135">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="2f48b-135">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="2f48b-136">[Planlægning](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="2f48b-136">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="2f48b-137">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="2f48b-137">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="2f48b-138">Køb</span><span class="sxs-lookup"><span data-stu-id="2f48b-138">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="2f48b-139">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2f48b-139">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]