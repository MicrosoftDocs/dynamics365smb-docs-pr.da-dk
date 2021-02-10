---
title: Knyt en salgsordre til en købsordre til direkte levering | Microsoft Docs
description: Beskriver, hvordan du opretter en salgsordre, der er knyttet til en købsordre for at muliggøre levering direkte fra leverandøren til kunden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c6b84d3622b4261c1f88880ba1257bf00f83e346
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748439"
---
# <a name="make-drop-shipments"></a><span data-ttu-id="099ca-103">Foretage direkte leveringer</span><span class="sxs-lookup"><span data-stu-id="099ca-103">Make Drop Shipments</span></span>

<span data-ttu-id="099ca-104">En direkte levering er en levering af varer fra en af dine leverandører direkte til din kunde.</span><span class="sxs-lookup"><span data-stu-id="099ca-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="099ca-105">Når en salgsordre er markeret til direkte levering, og du opretter en købsordre, der angiver kunden i feltet **Leveres til**, **Debitoradresse**, kan du sammenkæde de to dokumenter for at give kreditoren besked om at levere direkte til debitoren.</span><span class="sxs-lookup"><span data-stu-id="099ca-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Ship-to** field, **Customer Address**, you can link the two documents to instruct the vendor to ship directly to the customer.</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="099ca-106">Sådan oprettes en salgsordre til direkte levering</span><span class="sxs-lookup"><span data-stu-id="099ca-106">To create a sales order for drop shipment</span></span>

<span data-ttu-id="099ca-107">Hvis du vil forberede en direkte levering, skal du oprette en salgsordre for en vare og angive på salgslinjen, at salget kræver direkte levering.</span><span class="sxs-lookup"><span data-stu-id="099ca-107">To prepare a drop shipment, you create a sales order for an item and indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="099ca-108">Opret en salgsordre for en vare.</span><span class="sxs-lookup"><span data-stu-id="099ca-108">Create a sales order for an item.</span></span> <span data-ttu-id="099ca-109">Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="099ca-109">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="099ca-110">Markér afkrydsningsfeltet **Direkte levering** på salgsordrelinjen for den direkte levering.</span><span class="sxs-lookup"><span data-stu-id="099ca-110">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="099ca-111">Brug funktionen **Vis kolonner**, hvis feltet ikke vises.</span><span class="sxs-lookup"><span data-stu-id="099ca-111">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="099ca-112">Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="099ca-112">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="099ca-113">Sådan oprettes købsordren til direkte levering</span><span class="sxs-lookup"><span data-stu-id="099ca-113">To create the purchase order for drop shipment</span></span>

<span data-ttu-id="099ca-114">Hvis du vil forberede en direkte levering, skal du angive på købsordren, at den skal sendes til kunden og ikke til dig selv.</span><span class="sxs-lookup"><span data-stu-id="099ca-114">To prepare a drop shipment, you indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="099ca-115">Opret en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="099ca-115">Create a purchase order.</span></span> <span data-ttu-id="099ca-116">Du skal ikke udfylde nogen felter på linjerne.</span><span class="sxs-lookup"><span data-stu-id="099ca-116">Do not fill any fields on the lines.</span></span> <span data-ttu-id="099ca-117">Du kan finde flere oplysninger under [Registrere køb](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="099ca-117">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="099ca-118">Vælg **Debitoradresse** i feltet **Leveres til**.</span><span class="sxs-lookup"><span data-stu-id="099ca-118">In the **Ship-to** field, select **Customer Address**.</span></span>
3. <span data-ttu-id="099ca-119">Vælg den kunde, du sælger til, i feltet **Debitor**.</span><span class="sxs-lookup"><span data-stu-id="099ca-119">In the **Customer** field, select the customer that you are selling to.</span></span>
4. <span data-ttu-id="099ca-120">Vælg handlingen **Direkte leveringer**, og vælg derefter handlingen **Hent salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="099ca-120">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
5. <span data-ttu-id="099ca-121">På siden **Salgsoversigt** skal du vælge den salgsordre, du forberedt i [Sådan oprettes en salgsordre til direkte levering](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="099ca-121">On the **Sales List** page, select the sales order that you prepared in [To create a sales order for drop shipment](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span></span>
6. <span data-ttu-id="099ca-122">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="099ca-122">Choose the **OK** button.</span></span>

<span data-ttu-id="099ca-123">Linjeoplysningerne på salgsordren indsættes på købsordrelinjen(erne).</span><span class="sxs-lookup"><span data-stu-id="099ca-123">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="099ca-124">Nu kan du bede leverandøren levere varerne til kunden, f.eks. ved at sende købsordren som en PDF.</span><span class="sxs-lookup"><span data-stu-id="099ca-124">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-create-multiple-purchase-orders-for-drop-shipments"></a><span data-ttu-id="099ca-125">Sådan oprettes flere købsordrer til direkte leveringer</span><span class="sxs-lookup"><span data-stu-id="099ca-125">To create multiple purchase orders for drop shipments</span></span>

<span data-ttu-id="099ca-126">Du kan også bruge indkøbskladden til at oprette købsordren til kreditoren.</span><span class="sxs-lookup"><span data-stu-id="099ca-126">You can also use the requisition worksheet to create the purchase order for the vendor.</span></span> <span data-ttu-id="099ca-127">Fordelen ved at bruge indkøbskladden er, at den kan oprette købsordrer til alle udestående direkte leveringer, så du ikke behøver at oprette dem en ad gangen.</span><span class="sxs-lookup"><span data-stu-id="099ca-127">The advantage of using the requisition worksheet is that it can create purchase orders for all outstanding drop shipments, so you don't have to create each one individually.</span></span>

1. <span data-ttu-id="099ca-128">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), åbn **Indkøbskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="099ca-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Requistion Worksheets**, and then choose the related link.</span></span>
2. <span data-ttu-id="099ca-129">Vælg handlingen **Direkte leveringer**, og vælg derefter handlingen **Hent salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="099ca-129">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
3. <span data-ttu-id="099ca-130">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="099ca-130">Choose the **OK** button.</span></span>
4. <span data-ttu-id="099ca-131">Gennemgå købsordrelinjerne, og vælg den leverandør, der leverer de krævede varer, i feltet **Leverandørnr.**.</span><span class="sxs-lookup"><span data-stu-id="099ca-131">Review the purchase order lines, and in the **Vendor No.** field, select vendor that supplies required goods.</span></span> 
5. <span data-ttu-id="099ca-132">Vælg handlingen **Udfør aktionsmeddelelse** for at konvertere de gennemsete linjer til en købsordre.</span><span class="sxs-lookup"><span data-stu-id="099ca-132">Choose the **Carry Out Action Message** action to convert reviewed lines to a purchase order.</span></span>

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="099ca-133">Sådan får du vist den tilknyttede købsordre fra salgsordren</span><span class="sxs-lookup"><span data-stu-id="099ca-133">To view the linked purchase order from the sales order</span></span>

* <span data-ttu-id="099ca-134">Markér salgsordrelinjen til direkte levering, vælg handlingen **Ordre**, vælg handlingen **Direkte levering**, og vælg derefter handlingen **Købsordre**.</span><span class="sxs-lookup"><span data-stu-id="099ca-134">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="099ca-135">Sådan bogfører du en direkte levering</span><span class="sxs-lookup"><span data-stu-id="099ca-135">To post a drop shipment</span></span>

<span data-ttu-id="099ca-136">Når kreditoren har leveret varerne, kan du bogføre salgsordren som leveret.</span><span class="sxs-lookup"><span data-stu-id="099ca-136">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="099ca-137">Du kan også bogføre købsordren, men kun med indstillingen **Modtag**, indtil salgsordren er faktureret.</span><span class="sxs-lookup"><span data-stu-id="099ca-137">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="099ca-138">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordre**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="099ca-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="099ca-139">Åbn den salgsordre, du oprettede i [Sådan oprettes en salgsordre til direkte levering](#to-create-a-sales-order-for-drop-shipment)(sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="099ca-139">Open the sales order that you created in [To create a sales order for drop shipment](#to-create-a-sales-order-for-drop-shipment).</span></span>
3. <span data-ttu-id="099ca-140">I feltet **Levér (antal)** skal du angive, hvor mange varer af ordreantallet der skal leveres, hele eller en del af ordreantallet.</span><span class="sxs-lookup"><span data-stu-id="099ca-140">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="099ca-141">Vælg handlingen **Bogfør** eller **Bogfør og send**.</span><span class="sxs-lookup"><span data-stu-id="099ca-141">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="099ca-142">Vælg enten indstillingen **Levér** for at fakturere senere, eller vælg indstillingen **Levér og fakturer** for at fakturere med det samme.</span><span class="sxs-lookup"><span data-stu-id="099ca-142">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="099ca-143">Se også</span><span class="sxs-lookup"><span data-stu-id="099ca-143">See Also</span></span>

[<span data-ttu-id="099ca-144">Oprette specialordrer</span><span class="sxs-lookup"><span data-stu-id="099ca-144">Create Special Orders</span></span>](sales-how-to-create-special-orders.md)  
[<span data-ttu-id="099ca-145">Købe varer til et salg</span><span class="sxs-lookup"><span data-stu-id="099ca-145">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="099ca-146">Sælge produkter</span><span class="sxs-lookup"><span data-stu-id="099ca-146">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="099ca-147">Registrere køb</span><span class="sxs-lookup"><span data-stu-id="099ca-147">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="099ca-148">Salg</span><span class="sxs-lookup"><span data-stu-id="099ca-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="099ca-149">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="099ca-149">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="099ca-150">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="099ca-150">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
