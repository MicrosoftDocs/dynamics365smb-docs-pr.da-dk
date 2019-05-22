---
title: Knyt en salgsordre til en købsordre til direkte levering | Microsoft Docs
description: Beskriver, hvordan du opretter en salgsordre, der er knyttet til en købsordre for at muliggøre levering direkte fra leverandøren til kunden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7a87023445ea10aa19cc0cc4f60d76ce4cf3e365
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251213"
---
# <a name="make-drop-shipments"></a><span data-ttu-id="2a877-103">Foretage direkte leveringer</span><span class="sxs-lookup"><span data-stu-id="2a877-103">Make Drop Shipments</span></span>
<span data-ttu-id="2a877-104">En direkte levering er en levering af varer fra en af dine leverandører direkte til din kunde.</span><span class="sxs-lookup"><span data-stu-id="2a877-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="2a877-105">Når en salgsordre er markeret til direkte levering, og du opretter en købsordre, som angiver kunden i feltet **Sælg til kundenr.**,</span><span class="sxs-lookup"><span data-stu-id="2a877-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Sell-to Customer No.**</span></span> <span data-ttu-id="2a877-106">kan du sammenkæde de to dokumenter og dermed bede leverandøren levere direkte til kunden.</span><span class="sxs-lookup"><span data-stu-id="2a877-106">field, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="2a877-107">Sådan oprettes en salgsordre til direkte levering</span><span class="sxs-lookup"><span data-stu-id="2a877-107">To create a sales order for drop shipment</span></span>
<span data-ttu-id="2a877-108">Hvis du vil forberede en direkte levering, skal du oprette en salgsordre for en vare som normalt, bortset fra at du skal angive på salgslinjen, at salget kræver direkte levering.</span><span class="sxs-lookup"><span data-stu-id="2a877-108">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="2a877-109">Opret en salgsordre for en vare.</span><span class="sxs-lookup"><span data-stu-id="2a877-109">Create a sales order for an item.</span></span> <span data-ttu-id="2a877-110">Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="2a877-110">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="2a877-111">Markér afkrydsningsfeltet **Direkte levering** på salgsordrelinjen for den direkte levering.</span><span class="sxs-lookup"><span data-stu-id="2a877-111">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="2a877-112">Brug funktionen **Vis kolonner**, hvis feltet ikke vises.</span><span class="sxs-lookup"><span data-stu-id="2a877-112">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="2a877-113">Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="2a877-113">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="2a877-114">Sådan oprettes købsordren til direkte levering</span><span class="sxs-lookup"><span data-stu-id="2a877-114">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="2a877-115">Hvis du vil forberede en direkte levering af den vare, der skal sælges, kan du oprette en købsordre som normalt, bortset fra skal du angive på købsordren, at den skal leveres til kunden, ikke til dig selv.</span><span class="sxs-lookup"><span data-stu-id="2a877-115">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="2a877-116">Opret en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="2a877-116">Create a purchase order.</span></span> <span data-ttu-id="2a877-117">Du skal ikke udfylde nogen felter på linjerne.</span><span class="sxs-lookup"><span data-stu-id="2a877-117">Do not fill any fields on the lines.</span></span> <span data-ttu-id="2a877-118">Du kan finde flere oplysninger under [Registrere køb](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="2a877-118">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="2a877-119">I feltet **Kundenr**</span><span class="sxs-lookup"><span data-stu-id="2a877-119">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="2a877-120">skal du vælge den kunde, som du sælger til.</span><span class="sxs-lookup"><span data-stu-id="2a877-120">field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="2a877-121">Vælg handlingen **Direkte leveringer**, og vælg derefter handlingen **Hent salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="2a877-121">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="2a877-122">På siden **Salgsoversigt** skal du vælge den salgsordre, du forberedt i [Sådan oprettes en salgsordre til direkte levering](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="2a877-122">On the **Sales List** page, select the sales order that you prepared in [To create a sales order for drop shipment](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span></span>
5. <span data-ttu-id="2a877-123">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a877-123">Choose the **OK** button.</span></span>

<span data-ttu-id="2a877-124">Linjeoplysningerne på salgsordren indsættes på købsordrelinjen(erne).</span><span class="sxs-lookup"><span data-stu-id="2a877-124">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="2a877-125">Nu kan du bede leverandøren levere varerne til kunden, f.eks. ved at sende købsordren som en PDF.</span><span class="sxs-lookup"><span data-stu-id="2a877-125">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="2a877-126">Sådan får du vist den tilknyttede købsordre fra salgsordren</span><span class="sxs-lookup"><span data-stu-id="2a877-126">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="2a877-127">Markér salgsordrelinjen til direkte levering, vælg handlingen **Ordre**, vælg handlingen **Direkte levering**, og vælg derefter handlingen **Købsordre**.</span><span class="sxs-lookup"><span data-stu-id="2a877-127">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="2a877-128">Sådan bogfører du en direkte levering</span><span class="sxs-lookup"><span data-stu-id="2a877-128">To post a drop shipment</span></span>
<span data-ttu-id="2a877-129">Når kreditoren har leveret varerne, kan du bogføre salgsordren som leveret.</span><span class="sxs-lookup"><span data-stu-id="2a877-129">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="2a877-130">Du kan også bogføre købsordren, men kun med indstillingen **Modtag**, indtil salgsordren er faktureret.</span><span class="sxs-lookup"><span data-stu-id="2a877-130">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="2a877-131">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="2a877-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="2a877-132">Åbn den salgsordre, du oprettede i [Sådan oprettes en salgsordre til direkte levering]().</span><span class="sxs-lookup"><span data-stu-id="2a877-132">Open the sales order that you created in [To create a sales order for drop shipment]().</span></span>
3. <span data-ttu-id="2a877-133">I feltet **Levér (antal)** skal du angive, hvor mange varer af ordreantallet der skal leveres, hele eller en del af ordreantallet.</span><span class="sxs-lookup"><span data-stu-id="2a877-133">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="2a877-134">Vælg handlingen **Bogfør** eller **Bogfør og send**.</span><span class="sxs-lookup"><span data-stu-id="2a877-134">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="2a877-135">Vælg enten indstillingen **Levér** for at fakturere senere, eller vælg indstillingen **Levér og fakturer** for at fakturere med det samme.</span><span class="sxs-lookup"><span data-stu-id="2a877-135">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="2a877-136">Se også</span><span class="sxs-lookup"><span data-stu-id="2a877-136">See Also</span></span>
[<span data-ttu-id="2a877-137">Oprette specialordrer</span><span class="sxs-lookup"><span data-stu-id="2a877-137">Create Special Orders</span></span>](sales-how-to-create-special-orders.md)  
[<span data-ttu-id="2a877-138">Købe varer til et salg</span><span class="sxs-lookup"><span data-stu-id="2a877-138">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="2a877-139">Sælge produkter</span><span class="sxs-lookup"><span data-stu-id="2a877-139">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="2a877-140">Registrere køb</span><span class="sxs-lookup"><span data-stu-id="2a877-140">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="2a877-141">Salg</span><span class="sxs-lookup"><span data-stu-id="2a877-141">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="2a877-142">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="2a877-142">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="2a877-143">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2a877-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
