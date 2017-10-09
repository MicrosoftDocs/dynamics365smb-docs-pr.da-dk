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
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 990867cb428f860b1001177738d1a027f72485bc
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-make-drop-shipments"></a><span data-ttu-id="99d86-103">Fremgangsmåde: Foretage direkte leveringer</span><span class="sxs-lookup"><span data-stu-id="99d86-103">How to: Make Drop Shipments</span></span>
<span data-ttu-id="99d86-104">En direkte levering er en levering af varer fra en af dine leverandører direkte til din kunde.</span><span class="sxs-lookup"><span data-stu-id="99d86-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="99d86-105">Når en salgsordre er markeret til direkte levering, og du opretter en købsordre, som angiver kunden i feltet **Sælg til kundenr.**,</span><span class="sxs-lookup"><span data-stu-id="99d86-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Sell-to Customer No.**</span></span> <span data-ttu-id="99d86-106">kan du sammenkæde de to dokumenter og dermed bede leverandøren levere direkte til kunden.</span><span class="sxs-lookup"><span data-stu-id="99d86-106">field, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="99d86-107">Sådan oprettes en salgsordre til direkte levering</span><span class="sxs-lookup"><span data-stu-id="99d86-107">To create a sales order for drop shipment</span></span>
<span data-ttu-id="99d86-108">Hvis du vil forberede en direkte levering, skal du oprette en salgsordre for en vare som normalt, bortset fra at du skal angive på salgslinjen, at salget kræver direkte levering.</span><span class="sxs-lookup"><span data-stu-id="99d86-108">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="99d86-109">Opret en salgsordre for en vare.</span><span class="sxs-lookup"><span data-stu-id="99d86-109">Create a sales order for an item.</span></span> <span data-ttu-id="99d86-110">Du kan finde flere oplysninger i [Fremgangsmåde: Sælge produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="99d86-110">For more information, see [How to: Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="99d86-111">Markér afkrydsningsfeltet **Direkte levering** på salgsordrelinjen for den direkte levering.</span><span class="sxs-lookup"><span data-stu-id="99d86-111">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="99d86-112">Brug funktionen **Vis kolonner**, hvis feltet ikke vises.</span><span class="sxs-lookup"><span data-stu-id="99d86-112">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="99d86-113">Du kan finde flere oplysninger under [Brugertilpasning](ui-user-personalization.md).</span><span class="sxs-lookup"><span data-stu-id="99d86-113">For more information, see [User Personalization](ui-user-personalization.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="99d86-114">Denne funktion kræver, at oplevelsen er indstillet til **Suite**.</span><span class="sxs-lookup"><span data-stu-id="99d86-114">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="99d86-115">Du kan finde flere oplysninger under [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="99d86-115">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="99d86-116">Sådan oprettes købsordren til direkte levering</span><span class="sxs-lookup"><span data-stu-id="99d86-116">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="99d86-117">Hvis du vil forberede en direkte levering af den vare, der skal sælges, kan du oprette en købsordre som normalt, bortset fra skal du angive på købsordren, at den skal leveres til kunden, ikke til dig selv.</span><span class="sxs-lookup"><span data-stu-id="99d86-117">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="99d86-118">Opret en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="99d86-118">Create a purchase order.</span></span> <span data-ttu-id="99d86-119">Du skal ikke udfylde nogen felter på linjerne.</span><span class="sxs-lookup"><span data-stu-id="99d86-119">Do not fill any fields on the lines.</span></span> <span data-ttu-id="99d86-120">Du kan finde flere oplysninger under [Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="99d86-120">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="99d86-121">I feltet **Kundenr**</span><span class="sxs-lookup"><span data-stu-id="99d86-121">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="99d86-122">skal du vælge den kunde, som du sælger til.</span><span class="sxs-lookup"><span data-stu-id="99d86-122">field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="99d86-123">Vælg handlingen **Direkte leveringer**, og vælg derefter handlingen **Hent salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="99d86-123">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="99d86-124">I vinduet **Salgsoversigt** skal du vælge den salgsordre, du forberedt i afsnittet "Sådan oprettes en salgsordre til direkte levering".</span><span class="sxs-lookup"><span data-stu-id="99d86-124">In the **Sales List** window, select the sales order that you prepared in the "To create a sales order for drop shipment" section.</span></span>
5. <span data-ttu-id="99d86-125">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="99d86-125">Choose the **OK** button.</span></span>

<span data-ttu-id="99d86-126">Linjeoplysningerne på salgsordren indsættes på købsordrelinjen(erne).</span><span class="sxs-lookup"><span data-stu-id="99d86-126">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="99d86-127">Nu kan du bede leverandøren levere varerne til kunden, f.eks. ved at sende købsordren som en PDF.</span><span class="sxs-lookup"><span data-stu-id="99d86-127">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="99d86-128">Sådan får du vist den tilknyttede købsordre fra salgsordren</span><span class="sxs-lookup"><span data-stu-id="99d86-128">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="99d86-129">Markér salgsordrelinjen til direkte levering, vælg handlingen **Ordre**, vælg handlingen **Direkte levering**, og vælg derefter handlingen **Købsordre**.</span><span class="sxs-lookup"><span data-stu-id="99d86-129">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="99d86-130">Sådan bogfører du en direkte levering</span><span class="sxs-lookup"><span data-stu-id="99d86-130">To post a drop shipment</span></span>
<span data-ttu-id="99d86-131">Når kreditoren har leveret varerne, kan du bogføre salgsordren som leveret.</span><span class="sxs-lookup"><span data-stu-id="99d86-131">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="99d86-132">Du kan også bogføre købsordren, men kun med indstillingen **Modtag**, indtil salgsordren er faktureret.</span><span class="sxs-lookup"><span data-stu-id="99d86-132">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="99d86-133">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="99d86-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="99d86-134">Åbn den salgsordre, du oprettede i afsnittet "Sådan oprettes en salgsordre til direkte levering".</span><span class="sxs-lookup"><span data-stu-id="99d86-134">Open the sales order that you created in the "To create a sales order for a drop shipment" section.</span></span>
3. <span data-ttu-id="99d86-135">I feltet **Levér (antal)** skal du angive, hvor mange varer af ordreantallet der skal leveres, hele eller en del af ordreantallet.</span><span class="sxs-lookup"><span data-stu-id="99d86-135">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="99d86-136">Vælg handlingen **Bogfør** eller **Bogfør og send**.</span><span class="sxs-lookup"><span data-stu-id="99d86-136">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="99d86-137">Vælg enten indstillingen **Levér** for at fakturere senere, eller vælg indstillingen **Levér og fakturer** for at fakturere med det samme.</span><span class="sxs-lookup"><span data-stu-id="99d86-137">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="99d86-138">Se også</span><span class="sxs-lookup"><span data-stu-id="99d86-138">See Also</span></span>
<span data-ttu-id="99d86-139">[Sådan oprettes specialordrer](sales-how-to-create-special-orders.md)|</span><span class="sxs-lookup"><span data-stu-id="99d86-139">[How to: Create Special Orders](sales-how-to-create-special-orders.md)|</span></span>  
[<span data-ttu-id="99d86-140">Fremgangsmåde: Sælge produkter</span><span class="sxs-lookup"><span data-stu-id="99d86-140">How to: Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="99d86-141">Fremgangsmåde: Registrere køb</span><span class="sxs-lookup"><span data-stu-id="99d86-141">How to: Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="99d86-142">Salg</span><span class="sxs-lookup"><span data-stu-id="99d86-142">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="99d86-143">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="99d86-143">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="99d86-144">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="99d86-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

