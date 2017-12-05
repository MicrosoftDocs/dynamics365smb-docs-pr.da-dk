---
title: "Sådan plukkes til produktion i grundlæggende lageropsætninger | Microsoft Docs"
description: "Når lagerlokationen kræver pluk, men ikke leverance, skal du bruge vinduet **Pluk (lager)** til at organisere og registrere pluk af komponenter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 35eb4fdb15eded48510a232ed26aa02b4f5700c2
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-pick-for-production-or-assembly"></a><span data-ttu-id="213fd-103">Fremgangsmåde: Plukke til produktion eller montage</span><span class="sxs-lookup"><span data-stu-id="213fd-103">How to: Pick for Production or Assembly</span></span>
<span data-ttu-id="213fd-104">Hvordan du skal lægge komponenter på lager til produktions- eller montageordrer afhænger af den måde, som lagerstedet er sat op på som en lokation.</span><span class="sxs-lookup"><span data-stu-id="213fd-104">How you put away your pick components for production or assembly orders depends on how your warehouse is set up as a location.</span></span> <span data-ttu-id="213fd-105">Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="213fd-105">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

<span data-ttu-id="213fd-106">I grundlæggende lageropsætninger, hvor lokationen kræver pluk, men ikke leverance, skal du bruge vinduet **Pluk (lager)** til at organisere og registrere pluk af komponenter.</span><span class="sxs-lookup"><span data-stu-id="213fd-106">In basic warehouse configurations where the location requires pick processing but not shipment processing, you use the **Inventory Pick** window to organize and record the picking of components.</span></span>  

<span data-ttu-id="213fd-107">I grundlæggende lageropsætninger skal du plukke til montageordrer i vinduet **Flytning (lager)**.</span><span class="sxs-lookup"><span data-stu-id="213fd-107">In basic warehouse configurations, you must pick for assembly orders with the **Inventory Movement** window.</span></span> <span data-ttu-id="213fd-108">Du kan finde flere oplysninger i afsnittet "Håndtering af Ordremontagevarer med Pluk (lager)" i [Sådan plukkes varer med Pluk fra lager](warehouse-how-to-pick-items-with-inventory-picks.md).</span><span class="sxs-lookup"><span data-stu-id="213fd-108">For more information, see the "Handling Assemble-to-Order Item with Inventory Picks" section in [How to: Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md).</span></span>  

<span data-ttu-id="213fd-109">I avancerede lageropsætninger, hvor lokationer kræver både pluk og leverancer, skal du bruge vinduet **Lagerpluk** til at flytte komponenter til produktions- eller montageordrer.</span><span class="sxs-lookup"><span data-stu-id="213fd-109">In advanced warehouse configurations where locations require both picks and shipments, you use the **Warehouse Pick** window to bring components to production or assembly orders.</span></span>

> [!NOTE]  
>  <span data-ttu-id="213fd-110">Der er følgende vigtige forskelle mellem plukninger fra lager og lagerbevægelser:</span><span class="sxs-lookup"><span data-stu-id="213fd-110">The following important differences exist between inventory picks and inventory movements:</span></span>  
>   
>  -   <span data-ttu-id="213fd-111">Når du registrerer et pluk for en intern handling, såsom produktion, bogføres forbrug af de komponenter, der er plukket på samme tid.</span><span class="sxs-lookup"><span data-stu-id="213fd-111">When you register an inventory pick for an internal operation, such as production, the consumption of the picked components is posted at the same time.</span></span> <span data-ttu-id="213fd-112">Når du registrerer en flytning (lager) for en intern handling, registrerer du kun fysisk flytning af nødvendige komponenter til en placering i handlingsområdet uden bogføring af forbrug.</span><span class="sxs-lookup"><span data-stu-id="213fd-112">When you register an inventory movement for an internal operation, you only record the physical movement of the required components to a bin in the operation area without posting the consumption.</span></span>  
> -   <span data-ttu-id="213fd-113">Når du bruger pluk fra lager definerer feltet **Placeringskode** på en produktionsordrekomponentlinje den *hente*-placering, som komponenter tages fra, når forbruget posteres.</span><span class="sxs-lookup"><span data-stu-id="213fd-113">When you use inventory picks, the **Bin Code** field on a production order component line defines the *take* bin from where components are decreased when posting consumption.</span></span> <span data-ttu-id="213fd-114">Når du bruger lagerbevægelser, definerer feltet **Placeringskode** på produktionsordrekomponentlinjerne den *område*-placering i handlingsområdet, hvor lagermedarbejderen skal placere komponenterne.</span><span class="sxs-lookup"><span data-stu-id="213fd-114">When you use inventory movements, the **Bin Code** field on production order component lines defines the *place* bin in the operation area where the warehouse worker must place the components.</span></span>  

<span data-ttu-id="213fd-115">En systemforudsætning for plukning eller flytning af komponenter til kildedokumenter er, at der findes en udgående lageranmodning til at give lagerområdet besked om komponentbehovet.</span><span class="sxs-lookup"><span data-stu-id="213fd-115">A system precondition for picking, or moving, components for source documents is that an outbound warehouse request exists to notify the warehouse area of the component need.</span></span> <span data-ttu-id="213fd-116">Den udgående lageranmodning oprettes, hver gang produktionsordrestatus ændres til Frigivet, eller når en frigivet produktionsordre oprettes.</span><span class="sxs-lookup"><span data-stu-id="213fd-116">The outbound warehouse request is created whenever the production order status is changed to Released or when a released production order is created.</span></span>  

## <a name="to-pick-components-in-basic-warehouse-configurations"></a><span data-ttu-id="213fd-117">Sådan plukkes komponenter i grundlæggende lageropsætninger</span><span class="sxs-lookup"><span data-stu-id="213fd-117">To pick components in basic warehouse configurations</span></span>
<span data-ttu-id="213fd-118">I grundlæggende lageropsætninger, hvor placeringen er konfigureret til kun at bruge pluk, kan du plukke komponenter til produktionsaktiviteter i vinduet **Pluk (lager)**.</span><span class="sxs-lookup"><span data-stu-id="213fd-118">In basic warehouse configurations where the location is set up to use picking only, you can pick components for production activities with the **Inventory Pick** window.</span></span> <span data-ttu-id="213fd-119">Du kan finde flere oplysninger i [Sådan plukkes varer med Pluk fra lager](warehouse-how-to-pick-items-with-inventory-picks.md).</span><span class="sxs-lookup"><span data-stu-id="213fd-119">For more information, see [How to: Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md).</span></span>

1.  <span data-ttu-id="213fd-120">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Pluk (lager)**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="213fd-120">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Inventory Picks**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="213fd-121">Du kan få adgang til produktionsordrekomponenterne ved at vælge handlingen **Hent kildedokumenter** og derefter vælge den frigivne produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="213fd-121">To access the production order components, choose the **Get Source Documents** action, and then select the released production order.</span></span>  
3.  <span data-ttu-id="213fd-122">Foretag plukningen, og registrer derefter de faktiske plukoplysninger i feltet **Plukket antal**.</span><span class="sxs-lookup"><span data-stu-id="213fd-122">Perform the pick, and then record the actual picking information in the **Qty. Picked** field.</span></span>  
4.  <span data-ttu-id="213fd-123">Når linjerne er klar til at blive bogført, skal du vælge handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="213fd-123">When the lines are ready for posting, choose the **Post** action.</span></span> <span data-ttu-id="213fd-124">Bogføringen opretter de nødvendige lagerposter og bogfører forbruget af varer.</span><span class="sxs-lookup"><span data-stu-id="213fd-124">The posting creates the necessary warehouse entries and posts the consumption of the items.</span></span>  

<span data-ttu-id="213fd-125">Du kan også oprette et **Pluk (lager)** direkte fra den frigivne produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="213fd-125">You can also create an **Inventory Pick** directly from the released production order.</span></span> <span data-ttu-id="213fd-126">Vælg handlingen **Opret læg-på-lager/pluk**, marker afkrydsningsfeltet **Opret pluk (lager)**, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="213fd-126">Choose the **Create Inventory Put-away/Pick** action, select the **Create Invt. Pick** check box, and then choose the **OK** button.</span></span>

<span data-ttu-id="213fd-127">Du kan også bruge vinduet **Flytning (lager)** til at flytte varer mellem placeringer og ad hoc, dvs. uden henvisning til et kildedokument.</span><span class="sxs-lookup"><span data-stu-id="213fd-127">Alternatively, you can use the **Inventory Movement** window to move items between bins ad hoc, meaning without reference to a source document.</span></span>
<span data-ttu-id="213fd-128">Du kan finde flere oplysninger i [Fremgangsmåde: Flytte komponenter til et handlingsområde i grundlæggende lageropsætninger](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="213fd-128">For more information, see [How to: Move Components to an Operation Area in Basic Warehouse Configurations](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).</span></span>

### <a name="handling-assemble-to-order-items-with-inventory-picks"></a><span data-ttu-id="213fd-129">Håndtering af montage til ordre-varer med pluk (lager)</span><span class="sxs-lookup"><span data-stu-id="213fd-129">Handling Assemble-to-Order Items with Inventory Picks</span></span>
<span data-ttu-id="213fd-130">Vinduet **Pluk (lager)** bruges også til at plukke og afsende salg, hvor varerne skal monteres, inden de kan leveres.</span><span class="sxs-lookup"><span data-stu-id="213fd-130">The **Inventory Pick** window is also used to pick and ship for sales where items must be assembled before they can be shipped.</span></span> <span data-ttu-id="213fd-131">Du kan finde flere oplysninger i [Sådan sælger du en vare, der er monteret efter ordre](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="213fd-131">For more information, see [How to: Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span>

<span data-ttu-id="213fd-132">Varer, der skal leveres, findes ikke fysisk i en placering, før de er monteret og bogført som afgang til en placering i montageområdet.</span><span class="sxs-lookup"><span data-stu-id="213fd-132">Items to be shipped are not physically present in a bin until they are assembled and posted as output to a bin in the assembly area.</span></span> <span data-ttu-id="213fd-133">Det betyder, at pluk af ordremontagevarer til levering følger en speciel strøm.</span><span class="sxs-lookup"><span data-stu-id="213fd-133">This means that picking assemble-to-order items for shipment follows a special flow.</span></span> <span data-ttu-id="213fd-134">Lagermedarbejderne fra en placering fragter montageelementerne til afsendelsesområdet og bogfører derefter lagerpluk.</span><span class="sxs-lookup"><span data-stu-id="213fd-134">From a bin, warehouse workers take the assembly items to the shipping dock and then post the inventory pick.</span></span> <span data-ttu-id="213fd-135">Den bogførte lagerpluk bogfører derefter montageafgang, komponentforbrug og salgsleverance.</span><span class="sxs-lookup"><span data-stu-id="213fd-135">The posted inventory pick then posts the assembly output, the component consumption, and the sales shipment.</span></span>

<span data-ttu-id="213fd-136">Du kan konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)] til automatisk at oprette en flytning (lager), når lagerpluk for varen montageelementet oprettes.</span><span class="sxs-lookup"><span data-stu-id="213fd-136">You can set up [!INCLUDE[d365fin](includes/d365fin_md.md)] to automatically create an inventory movement when the inventory pick for the assembly item is created.</span></span> <span data-ttu-id="213fd-137">Når du vil gøre det, skal du vælge feltet **Opret bevægelser automatisk** i vinduet **Montagekonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="213fd-137">To enable this, you must select the **Create Movements Automatically** field in the **Assembly Setup** window.</span></span> <span data-ttu-id="213fd-138">Du kan finde flere oplysninger i [Fremgangsmåde: Flytte komponenter til et handlingsområde i basislogistik](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="213fd-138">For more information, see [How to: Move Components to an Operation Area in Basic Warehousing](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).</span></span>

<span data-ttu-id="213fd-139">Lagerpluklinjer for salgsvarer oprettes på forskellige måder afhængigt af, om ingen, nogle eller alle salgslinjemængderne samles til ordre.</span><span class="sxs-lookup"><span data-stu-id="213fd-139">Inventory pick lines for sales items are created in different ways depending on whether none, some, or all of the sales line quantities are assembled to order.</span></span>

<span data-ttu-id="213fd-140">Ved almindeligt salg, hvor du bruger pluk fra lager til at bogføre leverancer af lagerantal, oprettes der én lagerpluklinje – eller flere, hvis varen lægges på flere placeringer – for hver salgsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="213fd-140">In regular sales where you use inventory picks to post shipment of inventory quantities, one inventory pick line, or several if the item is placed in different bins, is created for each sales order line.</span></span> <span data-ttu-id="213fd-141">Denne pluklinje er baseret på mængden i feltet **Lever (antal)**.</span><span class="sxs-lookup"><span data-stu-id="213fd-141">This pick line is based on the quantity in the **Qty. to Ship** field.</span></span>

<span data-ttu-id="213fd-142">I montage efter ordre-salg hvor hele mængden i salgsordrelinjen monteres efter ordre, oprettes der en lagerpluklinje for den mængde.</span><span class="sxs-lookup"><span data-stu-id="213fd-142">In assemble-to-order sales where the full quantity on the sales order line is assembled to order, one inventory pick line is created for that quantity.</span></span> <span data-ttu-id="213fd-143">Det betyder, at værdien i feltet Antal til montage svarer til værdien i feltet **Lever (antal)**.</span><span class="sxs-lookup"><span data-stu-id="213fd-143">This means that the value in the Quantity to Assemble field is the same as the value in the **Qty. to Ship** field.</span></span> <span data-ttu-id="213fd-144">Feltet **Montage til ordre** vælges på linjen.</span><span class="sxs-lookup"><span data-stu-id="213fd-144">The **Assemble to Order** field is selected on the line.</span></span>

<span data-ttu-id="213fd-145">Hvis montageoutputflow er konfigureret for lokationen, så indsættes værdien i feltet **Pla.kode til ordremontagelev.** eller værdien i feltet **Placeringskode til fra-montage**, i den rækkefølge, i feltet **Placeringskode** i lagerpluklinjen.</span><span class="sxs-lookup"><span data-stu-id="213fd-145">If an assembly output flow is set up for the location, then the value in the **Asm.-to-Order Shpt. Bin Code** field or the value in the **From-Assembly Bin Code** field, in that order, is inserted in the **Bin Code** field on the inventory pick line.</span></span>

<span data-ttu-id="213fd-146">Hvis en placeringskode ikke er angivet på salgsordrelinjen, og montageafgangsstrøm ikke er konfigureret for lokationen, så er feltet **Placeringskode** i lagerpluklinjen tomt.</span><span class="sxs-lookup"><span data-stu-id="213fd-146">If no bin code is specified on the sales order line, and no assembly output flow is set up for the location, then the **Bin Code** field on the inventory pick line is empty.</span></span> <span data-ttu-id="213fd-147">Lagermedarbejderen skal åbne vinduet **Placeringsindhold** og vælge den placering, hvor montageelementerne monteres.</span><span class="sxs-lookup"><span data-stu-id="213fd-147">The warehouse worker must open the **Bin Contents** window and select the bin where the assembly items are assembled.</span></span>

<span data-ttu-id="213fd-148">I kombinationsscenarier, hvor en del af mængden først skal samles, og en anden skal plukkes fra lageret, oprettes minimum to lagerpluklinjer.</span><span class="sxs-lookup"><span data-stu-id="213fd-148">In combination scenarios, where a part of the quantity must first be assembled and another must be picked from inventory, a minimum of two inventory pick lines are created.</span></span> <span data-ttu-id="213fd-149">En pluklinje er for ordremontageantal.</span><span class="sxs-lookup"><span data-stu-id="213fd-149">One pick line is for the assemble-to-order quantity.</span></span> <span data-ttu-id="213fd-150">De andre pluklinje afhænger af, hvilke placeringer der kan opfylde restantal fra lageret.</span><span class="sxs-lookup"><span data-stu-id="213fd-150">The other pick line depends on which bins can fulfill the remaining quantity from inventory.</span></span> <span data-ttu-id="213fd-151">Placeringskoder på de to linjer udfyldes på forskellige måder, som beskrevet for de to forskellige salgtyper.</span><span class="sxs-lookup"><span data-stu-id="213fd-151">Bin codes on the two lines are filled in different ways as described for the two different sales types respectively.</span></span> <span data-ttu-id="213fd-152">Du kan finde flere oplysninger i afsnittet "Kombinationsscenarier" i [Om montage til ordre og montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md).</span><span class="sxs-lookup"><span data-stu-id="213fd-152">For more information, see the “Combination Scenarios” section in [Understanding Assemble to Order and Assemble to Stock](assembly-assemble-to-order-or-assemble-to-stock.md).</span></span>

## <a name="to-pick-components-in-advanced-warehouse-configurations"></a><span data-ttu-id="213fd-153">Sådan plukkes komponenter i avancerede lageropsætninger</span><span class="sxs-lookup"><span data-stu-id="213fd-153">To pick components in advanced warehouse configurations</span></span>
<span data-ttu-id="213fd-154">I avancerede lageropsætninger, hvor placeringen er konfigureret til at bruge både pluk og levering, kan du plukke komponenter til produktions- og montageaktiviteter i vinduet **Lagerpluk**.</span><span class="sxs-lookup"><span data-stu-id="213fd-154">In advanced warehouse configurations where the location is set up to use picking as well as shipping, you can pick components for production and assembly activities with the **Warehouse Pick** window.</span></span> <span data-ttu-id="213fd-155">Du kan finde flere oplysninger i [Sådan plukkes varer med Pluk (logistik)](warehouse-how-to-pick-items-for-warehouse-shipment.md).</span><span class="sxs-lookup"><span data-stu-id="213fd-155">For more information, see [How to: Pick Items with Warehouse Picks](warehouse-how-to-pick-items-for-warehouse-shipment.md).</span></span>

<span data-ttu-id="213fd-156">Du kan også bruge vinduet **Bevægelseskladden** til at flytte varer mellem placeringer og ad hoc, dvs. uden henvisning til et kildedokument.</span><span class="sxs-lookup"><span data-stu-id="213fd-156">Alternatively, you can use the **Movement Worksheet** window to move items between bins ad hoc, meaning without reference to a source document.</span></span> <span data-ttu-id="213fd-157">Du kan finde flere oplysninger i [Fremgangsmåde: Flytte varer i avancerede lageropsætninger](warehouse-how-to-move-items-in-advanced-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="213fd-157">For more information, see [How to: Move Items in Advanced Warehouse Configurations](warehouse-how-to-move-items-in-advanced-warehousing.md).</span></span>  

<span data-ttu-id="213fd-158">Du kan ikke oprette et lagerplukdokument fra bunden, fordi en plukaktivitet altid er en del af en arbejdsproces, enten i et pull- eller push-scenario.</span><span class="sxs-lookup"><span data-stu-id="213fd-158">You cannot create a warehouse pick document from scratch because a pick activity is always part of a workflow, either in a pull or a push scenario.</span></span>  

<span data-ttu-id="213fd-159">Du kan oprette lagerplukdokument på en push-måde ved at vælge handlingen **Opret pluk (logistik)** i kildedokumentet, som f.eks. en frigivet montageordre eller lagerleverance.</span><span class="sxs-lookup"><span data-stu-id="213fd-159">You can create the warehouse pick document in a push fashion by selecting the **Create Whse. Pick** action on the source document, such as a released assembly order or warehouse shipment.</span></span> <span data-ttu-id="213fd-160">Du kan finde flere oplysninger i [Sådan plukkes varer med Pluk (logistik)](warehouse-how-to-pick-items-for-warehouse-shipment.md).</span><span class="sxs-lookup"><span data-stu-id="213fd-160">For more information, see [How to: Pick Items with Warehouse Picks](warehouse-how-to-pick-items-for-warehouse-shipment.md).</span></span>  

<span data-ttu-id="213fd-161">Du kan også oprette lagerplukdokument på en pull-måde fra vinduet **Plukkladde** for at registrere plukanmodninger, både for forsendelse og interne operationer, og derefter oprette de krævede lagerplukdokumenter.</span><span class="sxs-lookup"><span data-stu-id="213fd-161">Alternatively, you can create the warehouse pick document in a pull fashion by using the **Pick Worksheet** window to detect pick requests, both for shipment and internal operations, and then create the required warehouse pick documents.</span></span>  

<span data-ttu-id="213fd-162">Følgende procedure beskriver et pull-scenario, hvor du plukker komponenter til en frigivet produktionsordre via vinduet **Plukkladde**.</span><span class="sxs-lookup"><span data-stu-id="213fd-162">The following procedure explains a pull scenario where you pick components for a released production order through the **Pick Worksheet** window.</span></span> <span data-ttu-id="213fd-163">Fremgangsmåden gælder også for montageordrer.</span><span class="sxs-lookup"><span data-stu-id="213fd-163">The procedure also applies to assembly orders.</span></span>  

<span data-ttu-id="213fd-164">Hvis du vil oprette pluk-anmodninger, både for pull- og push-scenarier, skal de pågældende kildedokumenter være frigivet.</span><span class="sxs-lookup"><span data-stu-id="213fd-164">To create pick requests, both for pull and for push scenarios, the source documents in question must be released.</span></span> <span data-ttu-id="213fd-165">Frigiv kildedokumenter for interne operationer på følgende måder.</span><span class="sxs-lookup"><span data-stu-id="213fd-165">Release source documents for internal operations in the following ways.</span></span>  

 |<span data-ttu-id="213fd-166">Kildedokument</span><span class="sxs-lookup"><span data-stu-id="213fd-166">Source Document</span></span>|<span data-ttu-id="213fd-167">Frigivelsesmetode</span><span class="sxs-lookup"><span data-stu-id="213fd-167">Release Method</span></span>|  
 |---------------------|--------------------|  
 |<span data-ttu-id="213fd-168">Produktionsordre</span><span class="sxs-lookup"><span data-stu-id="213fd-168">Production Order</span></span>|<span data-ttu-id="213fd-169">Skift ordretype til frigivet produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="213fd-169">Change order type to released production order.</span></span>|  
 |<span data-ttu-id="213fd-170">Montageordre</span><span class="sxs-lookup"><span data-stu-id="213fd-170">Assembly Order</span></span>|<span data-ttu-id="213fd-171">Skift status til frigivet.</span><span class="sxs-lookup"><span data-stu-id="213fd-171">Change status to Released.</span></span>|  

## <a name="to-pick-components-using-the-pick-worksheet"></a><span data-ttu-id="213fd-172">Sådan plukkes komponenter ved hjælp af plukkladden</span><span class="sxs-lookup"><span data-stu-id="213fd-172">To pick components using the pick worksheet</span></span>  

1.  <span data-ttu-id="213fd-173">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Plukkladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="213fd-173">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Pick Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="213fd-174">Vælg handlingen **Hent lagerdokumenter**, og vælg derefter komponentlinjerne fra den frigivne produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="213fd-174">Choose the **Get Warehouse Documents** action, and then select the component lines from the released production order.</span></span>  
3.  <span data-ttu-id="213fd-175">Sorter linjerne for at opnå en effektiv plukrunde, og kombiner dem eventuelt med andre kladdelinjer for udnytte medarbejderens tid optimalt.</span><span class="sxs-lookup"><span data-stu-id="213fd-175">Inspect the lines, sort them to ensure an efficient picking round, and combine them with other worksheet lines if necessary to make best use of employee time.</span></span>  
4.  <span data-ttu-id="213fd-176">Vælg handlingen **Opret pluk**.</span><span class="sxs-lookup"><span data-stu-id="213fd-176">Choose the **Create Pick** action.</span></span>  
5.  <span data-ttu-id="213fd-177">Definer, hvordan du vil oprette lagerplukdokumenterne, og hvordan du vil sortere pluklinjer ved at udfylde felter i vinduet **Opret pluk**.</span><span class="sxs-lookup"><span data-stu-id="213fd-177">Define how to create the warehouse pick documents and how to sort pick lines by filling fields in the **Create Pick** window.</span></span>  
6.  <span data-ttu-id="213fd-178">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="213fd-178">Choose the **OK** button.</span></span>

<span data-ttu-id="213fd-179">Lagerplukdokumenter oprettes nu med pluklinjer for hver komponent, der kræves i den interne operation.</span><span class="sxs-lookup"><span data-stu-id="213fd-179">Warehouse pick documents are now created with pick lines for each component that is required in the internal operation.</span></span>

<span data-ttu-id="213fd-180">Hvis det interne operationsområde, f.eks en produktionshal, er sat op med en standardplacering til placering af komponenter, der skal bruges i handlingen, indsættes placeringskoden i Placer-linjerne til lagerplukdokumentet, så lagermedarbejderne kan se, hvor de skal placere elementerne.</span><span class="sxs-lookup"><span data-stu-id="213fd-180">If the internal operation area, such as a production shop floor, is set up with a default bin for placement of components to be used in the operation, then that bin code is inserted in the Place lines on the warehouse pick document to instruct warehouse workers where to place the items.</span></span> <span data-ttu-id="213fd-181">Du kan finde flere oplysninger i [Fremgangsmåde: Oprette grundlæggende lagersteder med handlingsområder](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md).</span><span class="sxs-lookup"><span data-stu-id="213fd-181">For more information, see [How to: Set Up Basic Warehouses with Operation Areas](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md).</span></span>

## <a name="filling-the-consumption-bin"></a><span data-ttu-id="213fd-182">Udfylde forbrugsplaceringen</span><span class="sxs-lookup"><span data-stu-id="213fd-182">Filling the Consumption Bin</span></span>
<span data-ttu-id="213fd-183">Dette flow-diagram viser, hvordan feltet **Placeringskode** i produktionsordrekomponenter udfyldes i henhold til din lokationsopsætning.</span><span class="sxs-lookup"><span data-stu-id="213fd-183">This flow chart shows how the **Bin Code** field on production order component lines is filled according to your location setup.</span></span>

<span data-ttu-id="213fd-184">![Placeringsrutediagram](media/binflow.png "BinFlow")</span><span class="sxs-lookup"><span data-stu-id="213fd-184">![Bin flow chart](media/binflow.png "BinFlow")</span></span>

## <a name="see-also"></a><span data-ttu-id="213fd-185">Se også</span><span class="sxs-lookup"><span data-stu-id="213fd-185">See Also</span></span>
[<span data-ttu-id="213fd-186">Logistik</span><span class="sxs-lookup"><span data-stu-id="213fd-186">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="213fd-187">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="213fd-187">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="213fd-188">[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="213fd-188">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="213fd-189">[Montagestyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="213fd-189">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="213fd-190">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="213fd-190">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="213fd-191">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="213fd-191">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
