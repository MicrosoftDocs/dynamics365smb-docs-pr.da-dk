---
title: "Oprette en salgsordre, der er knyttet til en købsordre for en direkte levering | Microsoft Docs"
description: "Beskriver, hvordan du opretter en salgsordre, der er knyttet til en købsordre for at muliggøre levering direkte fra leverandøren til kunden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 087ead3b0a28d09cd687c1fcb60f6fee2c914c4a
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="make-drop-shipments"></a><span data-ttu-id="5b227-103">Foretage direkte leveringer</span><span class="sxs-lookup"><span data-stu-id="5b227-103">Make Drop Shipments</span></span>
<span data-ttu-id="5b227-104">En direkte levering er en levering af varer fra en af dine leverandører direkte til din kunde.</span><span class="sxs-lookup"><span data-stu-id="5b227-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="5b227-105">Når en salgsordre er markeret til direkte levering, og du opretter en købsordre, som angiver kunden i feltet **Sælg til kundenr.**,</span><span class="sxs-lookup"><span data-stu-id="5b227-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Sell-to Customer No.**</span></span> <span data-ttu-id="5b227-106">kan du sammenkæde de to dokumenter og dermed bede leverandøren levere direkte til kunden.</span><span class="sxs-lookup"><span data-stu-id="5b227-106">field, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="5b227-107">Sådan oprettes en salgsordre til direkte levering</span><span class="sxs-lookup"><span data-stu-id="5b227-107">To create a sales order for drop shipment</span></span>
<span data-ttu-id="5b227-108">Hvis du vil forberede en direkte levering, skal du oprette en salgsordre for en vare som normalt, bortset fra at du skal angive på salgslinjen, at salget kræver direkte levering.</span><span class="sxs-lookup"><span data-stu-id="5b227-108">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="5b227-109">Opret en salgsordre for en vare.</span><span class="sxs-lookup"><span data-stu-id="5b227-109">Create a sales order for an item.</span></span> <span data-ttu-id="5b227-110">Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="5b227-110">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="5b227-111">Markér afkrydsningsfeltet **Direkte levering** på salgsordrelinjen for den direkte levering.</span><span class="sxs-lookup"><span data-stu-id="5b227-111">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="5b227-112">Brug funktionen **Vis kolonner**, hvis feltet ikke vises.</span><span class="sxs-lookup"><span data-stu-id="5b227-112">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="5b227-113">Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="5b227-113">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="5b227-114">Sådan oprettes købsordren til direkte levering</span><span class="sxs-lookup"><span data-stu-id="5b227-114">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="5b227-115">Hvis du vil forberede en direkte levering af den vare, der skal sælges, kan du oprette en købsordre som normalt, bortset fra skal du angive på købsordren, at den skal leveres til kunden, ikke til dig selv.</span><span class="sxs-lookup"><span data-stu-id="5b227-115">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="5b227-116">Opret en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="5b227-116">Create a purchase order.</span></span> <span data-ttu-id="5b227-117">Du skal ikke udfylde nogen felter på linjerne.</span><span class="sxs-lookup"><span data-stu-id="5b227-117">Do not fill any fields on the lines.</span></span> <span data-ttu-id="5b227-118">Du kan finde flere oplysninger under [Registrere køb](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="5b227-118">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="5b227-119">I feltet **Kundenr**</span><span class="sxs-lookup"><span data-stu-id="5b227-119">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="5b227-120">skal du vælge den kunde, som du sælger til.</span><span class="sxs-lookup"><span data-stu-id="5b227-120">field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="5b227-121">Vælg handlingen **Direkte leveringer**, og vælg derefter handlingen **Hent salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="5b227-121">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="5b227-122">I vinduet **Salgsoversigt** skal du vælge den salgsordre, du forberedt i afsnittet "Sådan oprettes en salgsordre til direkte levering".</span><span class="sxs-lookup"><span data-stu-id="5b227-122">In the **Sales List** window, select the sales order that you prepared in the "To create a sales order for drop shipment" section.</span></span>
5. <span data-ttu-id="5b227-123">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b227-123">Choose the **OK** button.</span></span>

<span data-ttu-id="5b227-124">Linjeoplysningerne på salgsordren indsættes på købsordrelinjen(erne).</span><span class="sxs-lookup"><span data-stu-id="5b227-124">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="5b227-125">Nu kan du bede leverandøren levere varerne til kunden, f.eks. ved at sende købsordren som en PDF.</span><span class="sxs-lookup"><span data-stu-id="5b227-125">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="5b227-126">Sådan får du vist den tilknyttede købsordre fra salgsordren</span><span class="sxs-lookup"><span data-stu-id="5b227-126">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="5b227-127">Markér salgsordrelinjen til direkte levering, vælg handlingen **Ordre**, vælg handlingen **Direkte levering**, og vælg derefter handlingen **Købsordre**.</span><span class="sxs-lookup"><span data-stu-id="5b227-127">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="5b227-128">Sådan bogfører du en direkte levering</span><span class="sxs-lookup"><span data-stu-id="5b227-128">To post a drop shipment</span></span>
<span data-ttu-id="5b227-129">Når kreditoren har leveret varerne, kan du bogføre salgsordren som leveret.</span><span class="sxs-lookup"><span data-stu-id="5b227-129">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="5b227-130">Du kan også bogføre købsordren, men kun med indstillingen **Modtag**, indtil salgsordren er faktureret.</span><span class="sxs-lookup"><span data-stu-id="5b227-130">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="5b227-131">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="5b227-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="5b227-132">Åbn den salgsordre, du oprettede i afsnittet "Sådan oprettes en salgsordre til direkte levering".</span><span class="sxs-lookup"><span data-stu-id="5b227-132">Open the sales order that you created in the "To create a sales order for a drop shipment" section.</span></span>
3. <span data-ttu-id="5b227-133">I feltet **Levér (antal)** skal du angive, hvor mange varer af ordreantallet der skal leveres, hele eller en del af ordreantallet.</span><span class="sxs-lookup"><span data-stu-id="5b227-133">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="5b227-134">Vælg handlingen **Bogfør** eller **Bogfør og send**.</span><span class="sxs-lookup"><span data-stu-id="5b227-134">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="5b227-135">Vælg enten indstillingen **Levér** for at fakturere senere, eller vælg indstillingen **Levér og fakturer** for at fakturere med det samme.</span><span class="sxs-lookup"><span data-stu-id="5b227-135">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="5b227-136">Se også</span><span class="sxs-lookup"><span data-stu-id="5b227-136">See Also</span></span>
<span data-ttu-id="5b227-137">[Oprette specialordrer](sales-how-to-create-special-orders.md)|</span><span class="sxs-lookup"><span data-stu-id="5b227-137">[Create Special Orders](sales-how-to-create-special-orders.md)|</span></span>  
[<span data-ttu-id="5b227-138">Sælge produkter</span><span class="sxs-lookup"><span data-stu-id="5b227-138">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="5b227-139">Registrere køb</span><span class="sxs-lookup"><span data-stu-id="5b227-139">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="5b227-140">Salg</span><span class="sxs-lookup"><span data-stu-id="5b227-140">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="5b227-141">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="5b227-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="5b227-142">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5b227-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

