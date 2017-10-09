---
title: "Sådan kombineres leverancer på én enkelt faktura | Microsoft Docs"
description: "Hvis du vil fakturere mere end én leverance samtidig, kan du bruge samlefunktionen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: e6be50119da5c617ce6dbf603903266f9ced821e
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="b2b05-103">Sådan kombineres leverancer på én enkelt faktura</span><span class="sxs-lookup"><span data-stu-id="b2b05-103">How to: Combine Shipments on a Single Invoice</span></span>
<span data-ttu-id="b2b05-104">Hvis du vil fakturere mere end én leverance samtidig, kan du bruge samlefunktionen.</span><span class="sxs-lookup"><span data-stu-id="b2b05-104">If you want to invoice more than one shipment at a time, you can use the combined shipments feature.</span></span>  

 <span data-ttu-id="b2b05-105">Før du kan oprette en samleleverance, skal der bogføres mere end én salgsleverance i samme valuta til den samme kunde.</span><span class="sxs-lookup"><span data-stu-id="b2b05-105">Before you can create a combined shipment, more than one sales shipment for the same customer in the same currency must be posted.</span></span> <span data-ttu-id="b2b05-106">Du skal med andre ord have udfyldt to eller flere salgsordrer og bogført dem som leveret, men ikke faktureret.</span><span class="sxs-lookup"><span data-stu-id="b2b05-106">In other words, you must have filled in two or more sales orders and posted them as shipped, but not invoiced.</span></span> <span data-ttu-id="b2b05-107">For at kombinere leverancer skal afkrydsningsfeltet **Tillad samlefaktura** være markeret i oversigtspanelet **Levering** på **debitor**-kortet.</span><span class="sxs-lookup"><span data-stu-id="b2b05-107">To combine shipments, the **Combine Shipments** check box must be selected on the **Shipping** FastTab of the **Customer** card.</span></span>  

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="b2b05-108">Sådan kombinerer du manuelt leverancer på én enkelt faktura</span><span class="sxs-lookup"><span data-stu-id="b2b05-108">To manually combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="b2b05-109">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="b2b05-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b2b05-110">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b2b05-110">Choose the **New** action.</span></span> <span data-ttu-id="b2b05-111">Du kan finde flere oplysninger under [Fremgangsmåde: Fakturere salg](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="b2b05-111">For more information, see [How to: Invoice Sales](sales-how-invoice-sales.md).</span></span>
3. <span data-ttu-id="b2b05-112">I feltet **Kundenr**</span><span class="sxs-lookup"><span data-stu-id="b2b05-112">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="b2b05-113">skal du angive den kunde, der skal modtage fakturaen for de leverede varer.</span><span class="sxs-lookup"><span data-stu-id="b2b05-113">field, enter the customer who will receive the invoice for the shipped items.</span></span>  
4. <span data-ttu-id="b2b05-114">I oversigtspanelet **Linjer** skal du vælge handlingen **Hent salgsleverancelinjer**.</span><span class="sxs-lookup"><span data-stu-id="b2b05-114">On the **Lines** FastTab, choose the **Get Shipment Lines** action.</span></span>  
5. <span data-ttu-id="b2b05-115">Vælg de leverancelinjer, der skal indgå i fakturaen:</span><span class="sxs-lookup"><span data-stu-id="b2b05-115">Select the shipment line that you want to include in the invoice:</span></span>  

    - <span data-ttu-id="b2b05-116">Hvis alle linjer skal indsættes, skal du markere samtlige linjer og vælge knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2b05-116">To insert all lines, select all lines and choose the **OK** button.</span></span>  
    - <span data-ttu-id="b2b05-117">Hvis specifikke linjer skal indsættes, skal du markere linjerne og vælge knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2b05-117">To insert specific lines, select the lines and choose the **OK** button.</span></span> <span data-ttu-id="b2b05-118">Du kan bruge Ctrl-tasten til at markere flere ikke-fortløbende linjer.</span><span class="sxs-lookup"><span data-stu-id="b2b05-118">You can use the Ctrl key to select multiple nonsequential lines.</span></span>  

    <span data-ttu-id="b2b05-119">Hvis du kommer til at vælge en forkert leveringslinje eller vil begynde forfra, skal du bare slette linjerne på fakturaen og bruge funktionen **Hent salgsleverancelinjer** igen.</span><span class="sxs-lookup"><span data-stu-id="b2b05-119">If an incorrect shipment line was selected or you want to start over, you can simply delete the lines on the invoice and re-run the **Get Shipment Lines** function.</span></span>  
7. <span data-ttu-id="b2b05-120">Vælg handlingen **Bogfør** for at fakturere kladden.</span><span class="sxs-lookup"><span data-stu-id="b2b05-120">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="b2b05-121">Sådan kombinerer du automatisk leverancer på én enkelt faktura</span><span class="sxs-lookup"><span data-stu-id="b2b05-121">To automatically combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="b2b05-122">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Tillad samlefaktura**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="b2b05-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Combine Shipments**, and then choose the related link.</span></span> <span data-ttu-id="b2b05-123">Kørselsvinduet åbner.</span><span class="sxs-lookup"><span data-stu-id="b2b05-123">The batch job request window opens.</span></span>  
2. <span data-ttu-id="b2b05-124">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="b2b05-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="b2b05-125">Markér afkrydsningsfeltet **Bogfør fakturaer**.</span><span class="sxs-lookup"><span data-stu-id="b2b05-125">Select the **Post Invoices** check box.</span></span>  
4.  <span data-ttu-id="b2b05-126">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2b05-126">Choose the **OK** button.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b2b05-127">Du er nødt til at bogføre fakturaerne manuelt, hvis afkrydsningsfeltet **Bogfør fakturaer** ikke var markeret til kørslen.</span><span class="sxs-lookup"><span data-stu-id="b2b05-127">You will need to manually post the invoices if the **Post Invoices** check box was not selected on the batch job.</span></span>  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a><span data-ttu-id="b2b05-128">Sådan fjernes åbne salgsordrer efter bogføring af kombineret leverance</span><span class="sxs-lookup"><span data-stu-id="b2b05-128">To remove open sales orders after combined shipment posting</span></span> 
<span data-ttu-id="b2b05-129">Når leverancer samles på en faktura og bogføres, oprettes der en bogført salgsfaktura for de fakturerede linjer.</span><span class="sxs-lookup"><span data-stu-id="b2b05-129">When shipments are combined on an invoice and posted, a posted sales invoice is created for the invoiced lines.</span></span> <span data-ttu-id="b2b05-130">Feltet **Faktureret (antal)** på den oprindelige rammesalgsordre eller salgsordre opdateres på basis af det fakturerede antal.</span><span class="sxs-lookup"><span data-stu-id="b2b05-130">The **Quantity Invoiced** field on the originating blanket sales order or sales order is updated based on the invoiced quantity.</span></span>  

<span data-ttu-id="b2b05-131">Når du fakturerer leverancer på denne måde, findes de ordrer, som leverancerne er bogført fra, stadig, selvom de er leveret og faktureret i fuldt omfang.</span><span class="sxs-lookup"><span data-stu-id="b2b05-131">When you invoice shipments in this way, the orders from which the shipments were posted still exist, even if they have been fully shipped and invoiced.</span></span>   

1. <span data-ttu-id="b2b05-132">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Slet fakturerede salgsordrer**, og vælg linket.</span><span class="sxs-lookup"><span data-stu-id="b2b05-132">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Invoiced Sales Orders**, and then select the link.</span></span>  
2. <span data-ttu-id="b2b05-133">I feltet **Nummer**</span><span class="sxs-lookup"><span data-stu-id="b2b05-133">Specify in the **No.**</span></span> <span data-ttu-id="b2b05-134">skal du angive, hvilke ordrer der skal slettes.</span><span class="sxs-lookup"><span data-stu-id="b2b05-134">filter field which sales orders to delete.</span></span>  
3. <span data-ttu-id="b2b05-135">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2b05-135">Choose the **OK** button.</span></span>  

<span data-ttu-id="b2b05-136">Du kan også slette individuelle salgsordrer manuelt.</span><span class="sxs-lookup"><span data-stu-id="b2b05-136">Alternatively, delete individual sales orders manually.</span></span>  

<span data-ttu-id="b2b05-137">Gentag trin 1 til 3 for eventuelle andre berørte dokumenter, f.eks. rammesalgsordrer.</span><span class="sxs-lookup"><span data-stu-id="b2b05-137">Repeat steps 1 through 3 for any other affected documents, such as blanket sales orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="b2b05-138">Se også</span><span class="sxs-lookup"><span data-stu-id="b2b05-138">See Also</span></span>  
[<span data-ttu-id="b2b05-139">Salg</span><span class="sxs-lookup"><span data-stu-id="b2b05-139">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="b2b05-140">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b2b05-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

