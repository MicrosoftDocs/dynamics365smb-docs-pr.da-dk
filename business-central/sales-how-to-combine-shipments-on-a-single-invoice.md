---
title: Sådan kombineres leverancer på én enkelt faktura | Microsoft Docs
description: Hvis du vil fakturere mere end én leverance samtidig, kan du bruge samlefunktionen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 802cb7e6d7b7bb56f994eaf2b45df9c9f9cb43d3
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383071"
---
# <a name="combine-shipments-on-a-single-invoice"></a><span data-ttu-id="c71a9-103">Kombinere leverancer på én enkelt faktura</span><span class="sxs-lookup"><span data-stu-id="c71a9-103">Combine Shipments on a Single Invoice</span></span>
<span data-ttu-id="c71a9-104">Hvis du vil fakturere mere end én leverance samtidig, kan du bruge samlefunktionen.</span><span class="sxs-lookup"><span data-stu-id="c71a9-104">If you want to invoice more than one shipment at a time, you can use the combined shipments feature.</span></span>  

<span data-ttu-id="c71a9-105">Før du kan oprette en samleleverance, skal der bogføres mere end én salgsleverance i samme valuta til den samme kunde.</span><span class="sxs-lookup"><span data-stu-id="c71a9-105">Before you can create a combined shipment, more than one sales shipment for the same customer in the same currency must be posted.</span></span> <span data-ttu-id="c71a9-106">Du skal med andre ord oprette to eller flere salgsordrer og bogføre dem som leveret, men ikke faktureret.</span><span class="sxs-lookup"><span data-stu-id="c71a9-106">In other words, you must have create two or more sales orders and post them as shipped, but not invoiced.</span></span> 

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="c71a9-107">Sådan kombinerer du manuelt leverancer på én enkelt faktura</span><span class="sxs-lookup"><span data-stu-id="c71a9-107">To manually combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="c71a9-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c71a9-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c71a9-109">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c71a9-109">Choose the **New** action.</span></span> <span data-ttu-id="c71a9-110">Du kan finde flere oplysninger i [Fakturere salg](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="c71a9-110">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>
3. <span data-ttu-id="c71a9-111">I feltet **Kundenr**</span><span class="sxs-lookup"><span data-stu-id="c71a9-111">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="c71a9-112">skal du angive den kunde, der skal modtage fakturaen for de leverede varer.</span><span class="sxs-lookup"><span data-stu-id="c71a9-112">field, enter the customer who will receive the invoice for the shipped items.</span></span>  
4. <span data-ttu-id="c71a9-113">I oversigtspanelet **Linjer** skal du vælge handlingen **Hent salgsleverancelinjer**.</span><span class="sxs-lookup"><span data-stu-id="c71a9-113">On the **Lines** FastTab, choose the **Get Shipment Lines** action.</span></span>  
5. <span data-ttu-id="c71a9-114">Vælg de leverancelinjer, der skal indgå i fakturaen:</span><span class="sxs-lookup"><span data-stu-id="c71a9-114">Select the shipment line that you want to include in the invoice:</span></span>  

    - <span data-ttu-id="c71a9-115">Hvis alle linjer skal indsættes, skal du markere samtlige linjer og vælge knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="c71a9-115">To insert all lines, select all lines and choose the **OK** button.</span></span>  
    - <span data-ttu-id="c71a9-116">Hvis specifikke linjer skal indsættes, skal du markere linjerne og vælge knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="c71a9-116">To insert specific lines, select the lines and choose the **OK** button.</span></span> <span data-ttu-id="c71a9-117">Du kan bruge Ctrl-tasten til at markere flere ikke-fortløbende linjer.</span><span class="sxs-lookup"><span data-stu-id="c71a9-117">You can use the Ctrl key to select multiple nonsequential lines.</span></span>  

    <span data-ttu-id="c71a9-118">Hvis du kommer til at vælge en forkert leveringslinje eller vil begynde forfra, skal du bare slette linjerne på fakturaen og bruge funktionen **Hent salgsleverancelinjer** igen.</span><span class="sxs-lookup"><span data-stu-id="c71a9-118">If an incorrect shipment line was selected or you want to start over, you can simply delete the lines on the invoice and re-run the **Get Shipment Lines** function.</span></span>  
7. <span data-ttu-id="c71a9-119">Vælg handlingen **Bogfør** for at fakturere kladden.</span><span class="sxs-lookup"><span data-stu-id="c71a9-119">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="c71a9-120">Sådan kombinerer du automatisk leverancer på én enkelt faktura</span><span class="sxs-lookup"><span data-stu-id="c71a9-120">To automatically combine shipments on a single invoice</span></span>  
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="c71a9-121">vælger kun salgsordrer, hvor **Tillad samlefaktura** er valgt.</span><span class="sxs-lookup"><span data-stu-id="c71a9-121">will select only sales orders where **Combine Shipments** is chosen.</span></span> 

1. <span data-ttu-id="c71a9-122">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Tillad samlefaktura**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c71a9-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Combine Shipments**, and then choose the related link.</span></span> <span data-ttu-id="c71a9-123">Kørselssiden åbnes.</span><span class="sxs-lookup"><span data-stu-id="c71a9-123">The batch job request page opens.</span></span>  
2. <span data-ttu-id="c71a9-124">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="c71a9-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="c71a9-125">Vælg afkrydsningsfeltet **Bogfør fakturaer**.</span><span class="sxs-lookup"><span data-stu-id="c71a9-125">Choose the **Post Invoices** check box.</span></span>  
4. <span data-ttu-id="c71a9-126">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="c71a9-126">Choose the **OK** button.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="c71a9-127">Du er nødt til at bogføre fakturaerne manuelt, hvis afkrydsningsfeltet **Bogfør fakturaer** ikke var markeret til kørslen.</span><span class="sxs-lookup"><span data-stu-id="c71a9-127">You will need to manually post the invoices if the **Post Invoices** check box was not selected on the batch job.</span></span>  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a><span data-ttu-id="c71a9-128">Sådan fjernes åbne salgsordrer efter bogføring af kombineret leverance</span><span class="sxs-lookup"><span data-stu-id="c71a9-128">To remove open sales orders after combined shipment posting</span></span> 
<span data-ttu-id="c71a9-129">Når leverancer samles på en faktura og bogføres, oprettes der en bogført salgsfaktura for de fakturerede linjer.</span><span class="sxs-lookup"><span data-stu-id="c71a9-129">When shipments are combined on an invoice and posted, a posted sales invoice is created for the invoiced lines.</span></span> <span data-ttu-id="c71a9-130">Feltet **Faktureret (antal)** på den oprindelige rammesalgsordre eller salgsordre opdateres på basis af det fakturerede antal.</span><span class="sxs-lookup"><span data-stu-id="c71a9-130">The **Quantity Invoiced** field on the originating blanket sales order or sales order is updated based on the invoiced quantity.</span></span>  

<span data-ttu-id="c71a9-131">Når du fakturerer leverancer på denne måde, findes de ordrer, som leverancerne er bogført fra, stadig, selvom de er leveret og faktureret i fuldt omfang.</span><span class="sxs-lookup"><span data-stu-id="c71a9-131">When you invoice shipments in this way, the orders from which the shipments were posted still exist, even if they have been fully shipped and invoiced.</span></span>   

1. <span data-ttu-id="c71a9-132">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Slet fakturerede salgsordrer**, og vælg dernæst det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c71a9-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Sales Orders**, and then select the link.</span></span>  
2. <span data-ttu-id="c71a9-133">I feltet **Nummer**</span><span class="sxs-lookup"><span data-stu-id="c71a9-133">Specify in the **No.**</span></span> <span data-ttu-id="c71a9-134">skal du angive, hvilke ordrer der skal slettes.</span><span class="sxs-lookup"><span data-stu-id="c71a9-134">filter field which sales orders to delete.</span></span>  
3. <span data-ttu-id="c71a9-135">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="c71a9-135">Choose the **OK** button.</span></span>  

<span data-ttu-id="c71a9-136">Du kan også slette individuelle salgsordrer manuelt.</span><span class="sxs-lookup"><span data-stu-id="c71a9-136">Alternatively, delete individual sales orders manually.</span></span>  

<span data-ttu-id="c71a9-137">Gentag trin 1 til 3 for eventuelle andre berørte dokumenter, f.eks. rammesalgsordrer.</span><span class="sxs-lookup"><span data-stu-id="c71a9-137">Repeat steps 1 through 3 for any other affected documents, such as blanket sales orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="c71a9-138">Se også</span><span class="sxs-lookup"><span data-stu-id="c71a9-138">See Also</span></span>  
[<span data-ttu-id="c71a9-139">Salg</span><span class="sxs-lookup"><span data-stu-id="c71a9-139">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="c71a9-140">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c71a9-140">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]