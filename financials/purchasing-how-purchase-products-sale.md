---
title: "Oprette en købsfaktura fra en salgsfaktura for at købe varer til et salg | Microsoft Docs"
description: "Du kan oprette en købsfaktura for en kreditor eller en leverandør fra en salgsfaktura for at købe produkter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supply planning, sales demand, replenish
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: bb89654d7bc48ad9746265b15cf0b6270fec2f7c
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="purchase-items-for-a-sale"></a><span data-ttu-id="ad36b-103">Købe varer til et salg</span><span class="sxs-lookup"><span data-stu-id="ad36b-103">Purchase Items for a Sale</span></span>
<span data-ttu-id="ad36b-104">Fra salgsordrer og salgsfakturaer kan du bruge funktioner til hurtig oprettelse af indkøbsdokumenter for manglende vareantal, der kræves til salget.</span><span class="sxs-lookup"><span data-stu-id="ad36b-104">From sales orders and sales invoices, you can use functions to quickly create purchase documents for missing item quantities that are required by the sale.</span></span> <span data-ttu-id="ad36b-105">Du kan bruge to forskellige funktioner afhængigt af dokumenttypen.</span><span class="sxs-lookup"><span data-stu-id="ad36b-105">You can use two different functions depending on the document type.</span></span>
|<span data-ttu-id="ad36b-106">Funktion</span><span class="sxs-lookup"><span data-stu-id="ad36b-106">Function</span></span>|<span data-ttu-id="ad36b-107">Description</span><span class="sxs-lookup"><span data-stu-id="ad36b-107">Description</span></span>|
|--------|-----------|
|<span data-ttu-id="ad36b-108">**Opret købsordrer**</span><span class="sxs-lookup"><span data-stu-id="ad36b-108">**Create Purchase Orders**</span></span>|<span data-ttu-id="ad36b-109">Fra en salgsordre kan du bruge denne funktion til at oprette en købsordre for hver leverandør af varer på salgsordren.</span><span class="sxs-lookup"><span data-stu-id="ad36b-109">From a sales order, this function creates a purchase order for each vendor of items on the sales order.</span></span> <span data-ttu-id="ad36b-110">Før du opretter købsordrerne, kan du redigere købsantallet.</span><span class="sxs-lookup"><span data-stu-id="ad36b-110">You can edit the purchase quantity before you create the purchase orders.</span></span> <span data-ttu-id="ad36b-111">Der foreslås kun ikke-tilgængelige salgsantal.</span><span class="sxs-lookup"><span data-stu-id="ad36b-111">Only unavailable sales quantities are suggested.</span></span>
|<span data-ttu-id="ad36b-112">**Opret købsfaktura**</span><span class="sxs-lookup"><span data-stu-id="ad36b-112">**Create Purchase Invoice**</span></span>|<span data-ttu-id="ad36b-113">Fra en salgsordre og en salgsfaktura opretter denne funktion en købsfaktura for en valgt kreditor for alle linjer eller valgte linjer i salgsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="ad36b-113">From a sales order and from a sales invoice, this function creates a purchase invoice for a selected vendor for all lines or selected lines on the sales document.</span></span> <span data-ttu-id="ad36b-114">Det fulde salgsantal foreslås.</span><span class="sxs-lookup"><span data-stu-id="ad36b-114">The full sales quantity is suggested.</span></span>|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a><span data-ttu-id="ad36b-115">Sådan oprettes en eller flere købsordrer fra en salgsordre</span><span class="sxs-lookup"><span data-stu-id="ad36b-115">To create one or more purchase orders from a sales order</span></span>
<span data-ttu-id="ad36b-116">Hvis du vil oprette en købsordre for hvert vareantal, der ikke er tilgængeligt på salgsordren, skal du bruge funktionen **Opret købsordrer**.</span><span class="sxs-lookup"><span data-stu-id="ad36b-116">To create a purchase order for each unavailable item quantity on the sales order, you use the **Create Purchase Orders** function.</span></span>

1. <span data-ttu-id="ad36b-117">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ad36b-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="ad36b-118">Åbn en salgsordre, som du vil købe varer til.</span><span class="sxs-lookup"><span data-stu-id="ad36b-118">Open a sales order that you want to purchase items for.</span></span>
3. <span data-ttu-id="ad36b-119">Vælg handlingen **Opret købsordrer**.</span><span class="sxs-lookup"><span data-stu-id="ad36b-119">Choose the **Create Purchase Orders** action.</span></span>

    <span data-ttu-id="ad36b-120">Vinduet **Opret købsordrer** åbnes og viser en linje for hver vare på salgsordren.</span><span class="sxs-lookup"><span data-stu-id="ad36b-120">The **Create Purchase Orders** window opens showing a line for each different item on the sales order.</span></span> <span data-ttu-id="ad36b-121">Linjer for både fuldt tilgængeligt salgsantal og ikke-tilgængelige salgsantal (nedtonet) vises som standard.</span><span class="sxs-lookup"><span data-stu-id="ad36b-121">Lines for both fully available sales quantities and unavailable sales quantities (grayed) are shown by default.</span></span> <span data-ttu-id="ad36b-122">Du kan vælge handlingen **Vis utilgængelige** for kun at få vist linjer for salgsantal, der er ikke tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="ad36b-122">You can choose the **Show Unavailable** action to only see lines for unavailable sales quantities.</span></span>

    <span data-ttu-id="ad36b-123">Feltet **Købsantal** viser det antal, der ikke er tilgængeligt, som standard.</span><span class="sxs-lookup"><span data-stu-id="ad36b-123">The **Quantity to Purchase** field contains the unavailable sales quantity by default.</span></span>
4. <span data-ttu-id="ad36b-124">For at købe et andet antal end det antal, der ikke er tilgængeligt, skal du redigere værdien i feltet **Købsantal**.</span><span class="sxs-lookup"><span data-stu-id="ad36b-124">To purchase another quantity than the unavailable sales quantity, edit the value in the **Quantity to Purchase** field.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="ad36b-125">Du kan også ændre feltet **Købsantal** på nedtonede linjer, selv om de repræsenterer fuldt tilgængelige salgsantal.</span><span class="sxs-lookup"><span data-stu-id="ad36b-125">You can also change the **Quantity to Purchase** field on grayed lines even though they represent fully available sales quantities.</span></span>
5. <span data-ttu-id="ad36b-126">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="ad36b-126">Choose the **OK** button.</span></span>

    <span data-ttu-id="ad36b-127">Der oprettes en indkøbsordre for hver vareleverandør på salgsordren, herunder eventuelle ændringer af antal, du har foretaget i vinduet **Opret købsordrer**.</span><span class="sxs-lookup"><span data-stu-id="ad36b-127">A purchase order is created for each vendor of items on the sales order, including any quantity changes that you made in the **Create Purchase Orders** window.</span></span>
7. <span data-ttu-id="ad36b-128">Fortsæt med at behandle købsordrer eller ordrer, for eksempel ved at redigere eller tilføje købsordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="ad36b-128">Proceed to process the purchase order or orders, for example, by editing or adding purchase order lines.</span></span> <span data-ttu-id="ad36b-129">Du kan finde flere oplysninger under [Registrere køb](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="ad36b-129">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a><span data-ttu-id="ad36b-130">Sådan oprettes en købsfaktura fra en salgsordre eller salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="ad36b-130">To create a purchase invoice from a sales order or sales invoice</span></span>
<span data-ttu-id="ad36b-131">Når du vil oprette en enkelt købsfaktura for en eller flere linjer i et salgsdokument, skal du først at vælge, hvilken leverandør du vil købe fra ved at bruge funktionen **Opret købsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="ad36b-131">To create a single purchase invoice for one or more lines on a sales document by first selecting which vendor to buy from, you use the **Create Purchase Invoice** function.</span></span>

> [!NOTE]  
>   <span data-ttu-id="ad36b-132">Denne funktion opretter en købsfaktura for det nøjagtige vareantal i det valgte salgsdokument.</span><span class="sxs-lookup"><span data-stu-id="ad36b-132">This function creates a purchase invoice for the exact item quantity on the selected sales document.</span></span> <span data-ttu-id="ad36b-133">Hvis du vil ændre købsantallet, skal du redigere købsfakturaen, når den er oprettet.</span><span class="sxs-lookup"><span data-stu-id="ad36b-133">To change the purchase quantity, you must edit the purchase invoice after it is created.</span></span>  

1. <span data-ttu-id="ad36b-134">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ad36b-134">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="ad36b-135">Åbn en salgsfaktura, som du vil købe varer til.</span><span class="sxs-lookup"><span data-stu-id="ad36b-135">Open a sales invoice that you want to purchase items for.</span></span>
3. <span data-ttu-id="ad36b-136">Marker en eller flere fakturalinjer, som du vil bruge på købsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="ad36b-136">Select one or more sales invoice lines that you want to use on the purchase invoice.</span></span> <span data-ttu-id="ad36b-137">Hvis du vil bruge alle salgsfakturalinjer, skal du enten vælge dem alle eller ikke vælge nogen linjer.</span><span class="sxs-lookup"><span data-stu-id="ad36b-137">To use all the sales invoice lines, select either all of them or do not select any lines.</span></span>
4. <span data-ttu-id="ad36b-138">Vælg handlingen **Opret købsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="ad36b-138">Choose the **Create Purchase Invoice** action.</span></span>
5. <span data-ttu-id="ad36b-139">Vælg enten **Alle linjer** eller **Valgte linjer**, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="ad36b-139">Select either **All Lines** or **Selected Lines**, and then choose the **OK** button.</span></span>  
6. <span data-ttu-id="ad36b-140">På listen over kreditorer, der vises, skal du vælge den kreditor, du vil købe alle varerne fra, og derefter vælge knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="ad36b-140">In the list of vendors that appears, select the vendor that you want to buy all the items from, and then choose the **OK** button.</span></span>

    <span data-ttu-id="ad36b-141">Der oprettes en købsfaktura, der indeholder en, flere eller alle linjer på salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="ad36b-141">A purchase invoice is created that contains one, more, or all the lines on the sales invoice.</span></span>
7. <span data-ttu-id="ad36b-142">Fortsæt med at behandle købsfakturaen, for eksempel ved at redigere eller tilføje købsfakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="ad36b-142">Proceed to process the purchase invoice, for example, by editing or adding purchase invoice lines.</span></span> <span data-ttu-id="ad36b-143">Du kan finde flere oplysninger under [Registrere køb](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="ad36b-143">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ad36b-144">Se også</span><span class="sxs-lookup"><span data-stu-id="ad36b-144">See Also</span></span>
[<span data-ttu-id="ad36b-145">Køb</span><span class="sxs-lookup"><span data-stu-id="ad36b-145">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="ad36b-146">Registrere køb</span><span class="sxs-lookup"><span data-stu-id="ad36b-146">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="ad36b-147">Fakturere salg</span><span class="sxs-lookup"><span data-stu-id="ad36b-147">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="ad36b-148">Registrere nye kreditorer</span><span class="sxs-lookup"><span data-stu-id="ad36b-148">Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
<span data-ttu-id="ad36b-149">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ad36b-149">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

