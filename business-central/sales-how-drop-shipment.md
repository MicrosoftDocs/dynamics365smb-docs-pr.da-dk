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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 50198afaa8caae9a11a06a25357fa94ad26b0b8f
ms.sourcegitcommit: b570997f93d1f7141bc9539c93a67a91226660a8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/08/2020
ms.locfileid: "2943181"
---
# <a name="make-drop-shipments"></a><span data-ttu-id="67266-103">Foretage direkte leveringer</span><span class="sxs-lookup"><span data-stu-id="67266-103">Make Drop Shipments</span></span>
<span data-ttu-id="67266-104">En direkte levering er en levering af varer fra en af dine leverandører direkte til din kunde.</span><span class="sxs-lookup"><span data-stu-id="67266-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="67266-105">Når en salgsordre er markeret til direkte levering, og du opretter en købsordre, der angiver kunden i feltet **Leveres til**, **Debitoradresse**, kan du sammenkæde de to dokumenter og dermed give kreditoren besked om at levere direkte til debitoren.</span><span class="sxs-lookup"><span data-stu-id="67266-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Ship-to** field, **Customer Address**, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM]

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="67266-106">Sådan oprettes en salgsordre til direkte levering</span><span class="sxs-lookup"><span data-stu-id="67266-106">To create a sales order for drop shipment</span></span>
<span data-ttu-id="67266-107">Hvis du vil forberede en direkte levering, skal du oprette en salgsordre for en vare som normalt, bortset fra at du skal angive på salgslinjen, at salget kræver direkte levering.</span><span class="sxs-lookup"><span data-stu-id="67266-107">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="67266-108">Opret en salgsordre for en vare.</span><span class="sxs-lookup"><span data-stu-id="67266-108">Create a sales order for an item.</span></span> <span data-ttu-id="67266-109">Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="67266-109">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="67266-110">Markér afkrydsningsfeltet **Direkte levering** på salgsordrelinjen for den direkte levering.</span><span class="sxs-lookup"><span data-stu-id="67266-110">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="67266-111">Brug funktionen **Vis kolonner**, hvis feltet ikke vises.</span><span class="sxs-lookup"><span data-stu-id="67266-111">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="67266-112">Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="67266-112">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="67266-113">Sådan oprettes købsordren til direkte levering</span><span class="sxs-lookup"><span data-stu-id="67266-113">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="67266-114">Hvis du vil forberede en direkte levering af den vare, der skal sælges, kan du oprette en købsordre som normalt, bortset fra skal du angive på købsordren, at den skal leveres til kunden, ikke til dig selv.</span><span class="sxs-lookup"><span data-stu-id="67266-114">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="67266-115">Opret en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="67266-115">Create a purchase order.</span></span> <span data-ttu-id="67266-116">Du skal ikke udfylde nogen felter på linjerne.</span><span class="sxs-lookup"><span data-stu-id="67266-116">Do not fill any fields on the lines.</span></span> <span data-ttu-id="67266-117">Du kan finde flere oplysninger under [Registrere køb](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="67266-117">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="67266-118">Vælg **Debitoradresse** i feltet **Leveres til**.</span><span class="sxs-lookup"><span data-stu-id="67266-118">In the **Ship-to** field, select **Customer Address**.</span></span>
3. <span data-ttu-id="67266-119">Vælg den kunde, du sælger til, i feltet **Debitor**.</span><span class="sxs-lookup"><span data-stu-id="67266-119">In the **Customer** field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="67266-120">Vælg handlingen **Direkte leveringer**, og vælg derefter handlingen **Hent salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="67266-120">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="67266-121">På siden **Salgsoversigt** skal du vælge den salgsordre, du forberedt i [Sådan oprettes en salgsordre til direkte levering](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="67266-121">On the **Sales List** page, select the sales order that you prepared in [To create a sales order for drop shipment](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span></span>
5. <span data-ttu-id="67266-122">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="67266-122">Choose the **OK** button.</span></span>

<span data-ttu-id="67266-123">Linjeoplysningerne på salgsordren indsættes på købsordrelinjen(erne).</span><span class="sxs-lookup"><span data-stu-id="67266-123">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="67266-124">Nu kan du bede leverandøren levere varerne til kunden, f.eks. ved at sende købsordren som en PDF.</span><span class="sxs-lookup"><span data-stu-id="67266-124">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="67266-125">Sådan får du vist den tilknyttede købsordre fra salgsordren</span><span class="sxs-lookup"><span data-stu-id="67266-125">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="67266-126">Markér salgsordrelinjen til direkte levering, vælg handlingen **Ordre**, vælg handlingen **Direkte levering**, og vælg derefter handlingen **Købsordre**.</span><span class="sxs-lookup"><span data-stu-id="67266-126">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="67266-127">Sådan bogfører du en direkte levering</span><span class="sxs-lookup"><span data-stu-id="67266-127">To post a drop shipment</span></span>
<span data-ttu-id="67266-128">Når kreditoren har leveret varerne, kan du bogføre salgsordren som leveret.</span><span class="sxs-lookup"><span data-stu-id="67266-128">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="67266-129">Du kan også bogføre købsordren, men kun med indstillingen **Modtag**, indtil salgsordren er faktureret.</span><span class="sxs-lookup"><span data-stu-id="67266-129">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="67266-130">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordre**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="67266-130">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="67266-131">Åbn den salgsordre, du oprettede i [Sådan oprettes en salgsordre til direkte levering]().</span><span class="sxs-lookup"><span data-stu-id="67266-131">Open the sales order that you created in [To create a sales order for drop shipment]().</span></span>
3. <span data-ttu-id="67266-132">I feltet **Levér (antal)** skal du angive, hvor mange varer af ordreantallet der skal leveres, hele eller en del af ordreantallet.</span><span class="sxs-lookup"><span data-stu-id="67266-132">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="67266-133">Vælg handlingen **Bogfør** eller **Bogfør og send**.</span><span class="sxs-lookup"><span data-stu-id="67266-133">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="67266-134">Vælg enten indstillingen **Levér** for at fakturere senere, eller vælg indstillingen **Levér og fakturer** for at fakturere med det samme.</span><span class="sxs-lookup"><span data-stu-id="67266-134">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="67266-135">Se også</span><span class="sxs-lookup"><span data-stu-id="67266-135">See Also</span></span>
[<span data-ttu-id="67266-136">Oprette specialordrer</span><span class="sxs-lookup"><span data-stu-id="67266-136">Create Special Orders</span></span>](sales-how-to-create-special-orders.md)  
[<span data-ttu-id="67266-137">Købe varer til et salg</span><span class="sxs-lookup"><span data-stu-id="67266-137">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="67266-138">Sælge produkter</span><span class="sxs-lookup"><span data-stu-id="67266-138">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="67266-139">Registrere køb</span><span class="sxs-lookup"><span data-stu-id="67266-139">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="67266-140">Salg</span><span class="sxs-lookup"><span data-stu-id="67266-140">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="67266-141">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="67266-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="67266-142">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="67266-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
