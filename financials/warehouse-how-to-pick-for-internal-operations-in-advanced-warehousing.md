---
title: "Sådan plukkes til interne operationer i avancerede lageropsætninger | Microsoft Docs"
description: "I avancerede lageropsætninger, hvor placeringen er konfigureret til at bruge både pluk og levering, kan du plukke komponenter til produktions- og montageaktiviteter i vinduet **Lagerpluk**."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 8c07bddf7a4667f455f4512871d2a8c743c5014c
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-pick-for-assembly-or-production-in-advanced-warehouse-configurations"></a><span data-ttu-id="c2816-103">Sådan plukkes til montage eller produktion i avancerede lageropsætninger</span><span class="sxs-lookup"><span data-stu-id="c2816-103">How to: Pick for Assembly or Production in Advanced Warehouse Configurations</span></span>
<span data-ttu-id="c2816-104">I avancerede lageropsætninger, hvor placeringen er konfigureret til at bruge både pluk og levering, kan du plukke komponenter til produktions- og montageaktiviteter i vinduet **Lagerpluk**.</span><span class="sxs-lookup"><span data-stu-id="c2816-104">In advanced warehouse configurations where the location is set up to use picking as well as shipping, you can pick components for production and assembly activities with the **Warehouse Pick** window.</span></span>  

<span data-ttu-id="c2816-105">Du kan også bruge vinduet **Bevægelseskladden** til at flytte varer mellem placeringer og ad hoc, dvs. uden henvisning til et kildedokument.</span><span class="sxs-lookup"><span data-stu-id="c2816-105">Alternatively, you can use the **Movement Worksheet** window to move items between bins ad hoc, meaning without reference to a source document.</span></span> <span data-ttu-id="c2816-106">Du kan finde flere oplysninger i [Fremgangsmåde: Flytte varer i avancerede lageropsætninger](warehouse-how-to-move-items-in-advanced-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="c2816-106">For more information, see [How to: Move Items in advanced warehouse configurations](warehouse-how-to-move-items-in-advanced-warehousing.md).</span></span>  

<span data-ttu-id="c2816-107">Du kan finde oplysninger om pluk af varer til interne operationer på grundlæggende lagerlokationer, der er konfigureret kun til plukning, i [Fremgangsmåde: Flytte komponenter til et handlingsområde i grundlæggende lageropsætninger](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="c2816-107">For information about picking items for internal operations in basic warehouse locations that are set up for picking only, see [How to: Move Components to an Operation Area in Basic Warehouse Configurations](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).</span></span>  

<span data-ttu-id="c2816-108">Du kan ikke oprette et lagerplukdokument fra bunden, fordi en plukaktivitet altid er en del af en arbejdsproces, enten i et pull- eller push-scenario.</span><span class="sxs-lookup"><span data-stu-id="c2816-108">You cannot create a warehouse pick document from scratch because a pick activity is always part of a workflow, either in a pull or a push scenario.</span></span>  

<span data-ttu-id="c2816-109">Du kan oprette lagerplukdokument på en push-måde ved at vælg **Opret pluk (logistik)** i kildedokumentet, som f.eks. en frigivet montageordre eller lagerleverance.</span><span class="sxs-lookup"><span data-stu-id="c2816-109">You can create the warehouse pick document in a push fashion by selecting **Create Whse. Pick** on the source document, such as a released assembly order or warehouse shipment.</span></span> <span data-ttu-id="c2816-110">Du kan finde flere oplysninger i [Sådan plukkes varer med Pluk (logistik)](warehouse-how-to-pick-items-for-warehouse-shipment.md).</span><span class="sxs-lookup"><span data-stu-id="c2816-110">For more information, see [How to: Pick Items with Warehouse Picks](warehouse-how-to-pick-items-for-warehouse-shipment.md).</span></span>  

<span data-ttu-id="c2816-111">Du kan også oprette lagerplukdokument på en pull-måde fra vinduet **Plukkladde** for at registrere plukanmodninger, både for forsendelse og interne operationer, og derefter oprette de krævede lagerplukdokumenter.</span><span class="sxs-lookup"><span data-stu-id="c2816-111">Alternatively, you can create the warehouse pick document in a pull fashion by using the **Pick Worksheet** window to detect pick requests, both for shipment and internal operations, and then create the required warehouse pick documents.</span></span>  

<span data-ttu-id="c2816-112">Følgende procedure beskriver et pull-scenario, hvor du plukker komponenter til en frigivet produktionsordre via vinduet **Plukkladde**.</span><span class="sxs-lookup"><span data-stu-id="c2816-112">The following procedure explains a pull scenario where you pick components for a released production order through the **Pick Worksheet** window.</span></span> <span data-ttu-id="c2816-113">Fremgangsmåden gælder også for en montageordre.</span><span class="sxs-lookup"><span data-stu-id="c2816-113">The procedure also applies for an assembly order.</span></span>  

<span data-ttu-id="c2816-114">Hvis du vil oprette pluk-anmodninger, både for pull- og push-scenarier, skal de pågældende kildedokumenter være frigivet.</span><span class="sxs-lookup"><span data-stu-id="c2816-114">To create pick requests, both for pull and for push scenarios, the source documents in question must be released.</span></span> <span data-ttu-id="c2816-115">Frigiv kildedokumenter for interne operationer på følgende måder.</span><span class="sxs-lookup"><span data-stu-id="c2816-115">Release source documents for internal operations in the following ways.</span></span>  

|<span data-ttu-id="c2816-116">Kildedokument</span><span class="sxs-lookup"><span data-stu-id="c2816-116">Source Document</span></span>|<span data-ttu-id="c2816-117">Frigivelsesmetode</span><span class="sxs-lookup"><span data-stu-id="c2816-117">Release Method</span></span>|  
|---------------------|--------------------|  
|<span data-ttu-id="c2816-118">Produktionsordre</span><span class="sxs-lookup"><span data-stu-id="c2816-118">Production Order</span></span>|<span data-ttu-id="c2816-119">Skift ordretype til frigivet produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="c2816-119">Change order type to released production order.</span></span>|  
|<span data-ttu-id="c2816-120">Montageordre</span><span class="sxs-lookup"><span data-stu-id="c2816-120">Assembly Order</span></span>|<span data-ttu-id="c2816-121">Skift status til frigivet.</span><span class="sxs-lookup"><span data-stu-id="c2816-121">Change status to Released.</span></span>|  

## <a name="to-pick-components-using-the-pick-worksheet"></a><span data-ttu-id="c2816-122">Sådan plukkes komponenter ved hjælp af plukkladden</span><span class="sxs-lookup"><span data-stu-id="c2816-122">To pick components using the pick worksheet</span></span>  
1.  <span data-ttu-id="c2816-123">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Plukkladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c2816-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Pick Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c2816-124">Vælg handlingen **Hent lagerdokumenter**, og vælg derefter komponentlinjerne fra den frigivne produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="c2816-124">Choose the **Get Warehouse Documents** action, and then select the component lines from the released production order.</span></span>  
3.  <span data-ttu-id="c2816-125">Sorter linjerne for at opnå en effektiv plukrunde, og kombiner dem eventuelt med andre kladdelinjer for udnytte medarbejderens tid optimalt.</span><span class="sxs-lookup"><span data-stu-id="c2816-125">Inspect the lines, sort them to ensure an efficient picking round, and combine them with other worksheet lines if necessary to make best use of employee time.</span></span>  
4.  <span data-ttu-id="c2816-126">Vælg handlingen **Opret pluk**.</span><span class="sxs-lookup"><span data-stu-id="c2816-126">Choose the **Create Pick** action.</span></span>  
5.  <span data-ttu-id="c2816-127">Definer, hvordan du vil oprette lagerplukdokumenterne, og hvordan du vil sortere pluklinjer ved at udfylde felter i vinduet **Opret pluk**.</span><span class="sxs-lookup"><span data-stu-id="c2816-127">Define how to create the warehouse pick documents and how to sort pick lines by filling fields in the **Create Pick** window.</span></span>  
6.  <span data-ttu-id="c2816-128">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2816-128">Choose the **OK** button.</span></span> <span data-ttu-id="c2816-129">Lagerplukdokumenter oprettes med pluklinjer for hver komponent, der kræves i den interne operation.</span><span class="sxs-lookup"><span data-stu-id="c2816-129">Warehouse pick documents are created with pick lines for each component that is required in the internal operation.</span></span>  

<span data-ttu-id="c2816-130">Hvis det interne operationsområde, f.eks en produktionshal, er sat op med en standardplacering til placering af komponenter, der skal bruges i handlingen, indsættes placeringskoden i Placer-linjerne til lagerplukdokumentet, så lagermedarbejderne kan se, hvor de skal placere elementerne.</span><span class="sxs-lookup"><span data-stu-id="c2816-130">If the internal operation area, such as a production shop floor, is set up with a default bin for placement of components to be used in the operation, then that bin code is inserted in the Place lines on the warehouse pick document to instruct warehouse workers where to place the items.</span></span> <span data-ttu-id="c2816-131">Du kan finde flere oplysninger i felterne **Produktionsplaceringskode** eller **Placeringskode til til-montage**.</span><span class="sxs-lookup"><span data-stu-id="c2816-131">For more information, see the **To-Production Bin Code** or the **To-Assembly Bin Code** field.</span></span>

## <a name="filling-the-consumption-bin"></a><span data-ttu-id="c2816-132">Udfylde forbrugsplaceringen</span><span class="sxs-lookup"><span data-stu-id="c2816-132">Filling the Consumption Bin</span></span>
<span data-ttu-id="c2816-133">Dette flow-diagram viser, hvordan feltet **Placeringskode** i produktionsordrekomponenter udfyldes i henhold til din lokationsopsætning.</span><span class="sxs-lookup"><span data-stu-id="c2816-133">This flow chart shows how the **Bin Code** field on production order component lines is filled according to your location setup.</span></span>

<span data-ttu-id="c2816-134">![Placeringsrutediagram](media/binflow.png "BinFlow")</span><span class="sxs-lookup"><span data-stu-id="c2816-134">![Bin flow chart](media/binflow.png "BinFlow")</span></span>  

## <a name="see-also"></a><span data-ttu-id="c2816-135">Se også</span><span class="sxs-lookup"><span data-stu-id="c2816-135">See Also</span></span>
[<span data-ttu-id="c2816-136">Logistik</span><span class="sxs-lookup"><span data-stu-id="c2816-136">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="c2816-137">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="c2816-137">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="c2816-138">[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="c2816-138">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="c2816-139">[Montagestyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="c2816-139">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="c2816-140">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="c2816-140">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="c2816-141">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c2816-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

