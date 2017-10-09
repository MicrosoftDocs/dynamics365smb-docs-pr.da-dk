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
ms.date: 05/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2d7eb238395a0b1060668996fbbc3e13d9dd8a94
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-purchase-items-for-a-sale"></a><span data-ttu-id="b61d4-103">Fremgangsmåde: Købe varer til et salg</span><span class="sxs-lookup"><span data-stu-id="b61d4-103">How to: Purchase Items for a Sale</span></span>
<span data-ttu-id="b61d4-104">Fra salgsordrer og salgsfakturaer kan du bruge funktioner til hurtig oprettelse af indkøbsdokumenter for manglende vareantal, der kræves til salget.</span><span class="sxs-lookup"><span data-stu-id="b61d4-104">From sales orders and sales invoices, you can use functions to quickly create purchase documents for missing item quantities that are required by the sale.</span></span> <span data-ttu-id="b61d4-105">Du kan bruge to forskellige funktioner afhængigt af dokumenttypen.</span><span class="sxs-lookup"><span data-stu-id="b61d4-105">You can use two different functions depending on the document type.</span></span>
|<span data-ttu-id="b61d4-106">Funktion</span><span class="sxs-lookup"><span data-stu-id="b61d4-106">Function</span></span>|<span data-ttu-id="b61d4-107">Description</span><span class="sxs-lookup"><span data-stu-id="b61d4-107">Description</span></span>|
|--------|-----------|
|<span data-ttu-id="b61d4-108">**Opret købsordrer**</span><span class="sxs-lookup"><span data-stu-id="b61d4-108">**Create Purchase Orders**</span></span>|<span data-ttu-id="b61d4-109">Fra en salgsordre kan du bruge denne funktion til at oprette en købsordre for hver leverandør af varer på salgsordren.</span><span class="sxs-lookup"><span data-stu-id="b61d4-109">From a sales order, this function creates a purchase order for each vendor of items on the sales order.</span></span> <span data-ttu-id="b61d4-110">Før du opretter købsordrerne, kan du redigere købsantallet.</span><span class="sxs-lookup"><span data-stu-id="b61d4-110">You can edit the purchase quantity before you create the purchase orders.</span></span> <span data-ttu-id="b61d4-111">Der foreslås kun ikke-tilgængelige salgsantal.</span><span class="sxs-lookup"><span data-stu-id="b61d4-111">Only unavailable sales quantities are suggested.</span></span>
|<span data-ttu-id="b61d4-112">**Opret købsfaktura**</span><span class="sxs-lookup"><span data-stu-id="b61d4-112">**Create Purchase Invoice**</span></span>|<span data-ttu-id="b61d4-113">Fra en salgsordre og en salgsfaktura opretter denne funktion en købsfaktura for en valgt kreditor for alle linjer eller valgte linjer i salgsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="b61d4-113">From a sales order and from a sales invoice, this function creates a purchase invoice for a selected vendor for all lines or selected lines on the sales document.</span></span> <span data-ttu-id="b61d4-114">Det fulde salgsantal foreslås.</span><span class="sxs-lookup"><span data-stu-id="b61d4-114">The full sales quantity is suggested.</span></span>|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a><span data-ttu-id="b61d4-115">Sådan oprettes en eller flere købsordrer fra en salgsordre</span><span class="sxs-lookup"><span data-stu-id="b61d4-115">To create one or more purchase orders from a sales order</span></span>
<span data-ttu-id="b61d4-116">Hvis du vil oprette en købsordre for hvert vareantal, der ikke er tilgængeligt på salgsordren, skal du bruge funktionen **Opret købsordrer**.</span><span class="sxs-lookup"><span data-stu-id="b61d4-116">To create a purchase order for each unavailable item quantity on the sales order, you use the **Create Purchase Orders** function.</span></span> 

> [!NOTE]  
>   <span data-ttu-id="b61d4-117">Denne funktion kræver, at oplevelsen er indstillet til **Suite**.</span><span class="sxs-lookup"><span data-stu-id="b61d4-117">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="b61d4-118">Du kan finde flere oplysninger under [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="b61d4-118">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

1. <span data-ttu-id="b61d4-119">På startsiden skal du vælge feltet **Igangværende salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="b61d4-119">On the Home page, choose the **Ongoing Sales Orders** tile.</span></span>
2. <span data-ttu-id="b61d4-120">Åbn en salgsordre, som du vil købe varer til.</span><span class="sxs-lookup"><span data-stu-id="b61d4-120">Open a sales order that you want to purchase items for.</span></span>
3. <span data-ttu-id="b61d4-121">Vælg handlingen **Opret købsordrer**.</span><span class="sxs-lookup"><span data-stu-id="b61d4-121">Choose the **Create Purchase Orders** action.</span></span>

    <span data-ttu-id="b61d4-122">Vinduet **Opret købsordrer** åbnes og viser en linje for hver vare på salgsordren.</span><span class="sxs-lookup"><span data-stu-id="b61d4-122">The **Create Purchase Orders** window opens showing a line for each different item on the sales order.</span></span> <span data-ttu-id="b61d4-123">Linjer for både fuldt tilgængeligt salgsantal og ikke-tilgængelige salgsantal (nedtonet) vises som standard.</span><span class="sxs-lookup"><span data-stu-id="b61d4-123">Lines for both fully available sales quantities and unavailable sales quantities (grayed) are shown by default.</span></span> <span data-ttu-id="b61d4-124">Du kan vælge handlingen **Vis utilgængelige** for kun at få vist linjer for salgsantal, der er ikke tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="b61d4-124">You can choose the **Show Unavailable** action to only see lines for unavailable sales quantities.</span></span>

    <span data-ttu-id="b61d4-125">Feltet **Købsantal** viser det antal, der ikke er tilgængeligt, som standard.</span><span class="sxs-lookup"><span data-stu-id="b61d4-125">The **Quantity to Purchase** field contains the unavailable sales quantity by default.</span></span>
4. <span data-ttu-id="b61d4-126">For at købe et andet antal end det antal, der ikke er tilgængeligt, skal du redigere værdien i feltet **Købsantal**.</span><span class="sxs-lookup"><span data-stu-id="b61d4-126">To purchase another quantity than the unavailable sales quantity, edit the value in the **Quantity to Purchase** field.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="b61d4-127">Du kan også ændre feltet **Købsantal** på nedtonede linjer, selv om de repræsenterer fuldt tilgængelige salgsantal.</span><span class="sxs-lookup"><span data-stu-id="b61d4-127">You can also change the **Quantity to Purchase** field on grayed lines even though they represent fully available sales quantities.</span></span>
5. <span data-ttu-id="b61d4-128">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="b61d4-128">Choose the **OK** button.</span></span> 
    
    <span data-ttu-id="b61d4-129">Der oprettes en indkøbsordre for hver vareleverandør på salgsordren, herunder eventuelle ændringer af antal, du har foretaget i vinduet **Opret købsordrer**.</span><span class="sxs-lookup"><span data-stu-id="b61d4-129">A purchase order is created for each vendor of items on the sales order, including any quantity changes that you made in the **Create Purchase Orders** window.</span></span>
7. <span data-ttu-id="b61d4-130">Fortsæt med at behandle købsordrer eller ordrer, for eksempel ved at redigere eller tilføje købsordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="b61d4-130">Proceed to process the purchase order or orders, for example, by editing or adding purchase order lines.</span></span> <span data-ttu-id="b61d4-131">Du kan finde flere oplysninger under [Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="b61d4-131">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a><span data-ttu-id="b61d4-132">Sådan oprettes en købsfaktura fra en salgsordre eller salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="b61d4-132">To create a purchase invoice from a sales order or sales invoice</span></span>
<span data-ttu-id="b61d4-133">Når du vil oprette en enkelt købsfaktura for en eller flere linjer i et salgsdokument, skal du først at vælge, hvilken leverandør du vil købe fra ved at bruge funktionen **Opret købsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="b61d4-133">To create a single purchase invoice for one or more lines on a sales document by first selecting which vendor to buy from, you use the **Create Purchase Invoice** function.</span></span> 

> [!NOTE]  
>   <span data-ttu-id="b61d4-134">Denne funktion opretter en købsfaktura for det nøjagtige vareantal i det valgte salgsdokument.</span><span class="sxs-lookup"><span data-stu-id="b61d4-134">This function creates a purchase invoice for the exact item quantity on the selected sales document.</span></span> <span data-ttu-id="b61d4-135">Hvis du vil ændre købsantallet, skal du redigere købsfakturaen, når den er oprettet.</span><span class="sxs-lookup"><span data-stu-id="b61d4-135">To change the purchase quantity, you must edit the purchase invoice after it is created.</span></span>  

1. <span data-ttu-id="b61d4-136">På startsiden skal du vælge feltet **Igangværende salgsfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="b61d4-136">On the Home page, choose the **Ongoing Sales Invoices** tile.</span></span>
2. <span data-ttu-id="b61d4-137">Åbn en salgsfaktura, som du vil købe varer til.</span><span class="sxs-lookup"><span data-stu-id="b61d4-137">Open a sales invoice that you want to purchase items for.</span></span>
3. <span data-ttu-id="b61d4-138">Marker en eller flere fakturalinjer, som du vil bruge på købsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="b61d4-138">Select one or more sales invoice lines that you want to use on the purchase invoice.</span></span> <span data-ttu-id="b61d4-139">Hvis du vil bruge alle salgsfakturalinjer, skal du enten vælge dem alle eller ikke vælge nogen linjer.</span><span class="sxs-lookup"><span data-stu-id="b61d4-139">To use all the sales invoice lines, select either all of them or do not select any lines.</span></span>
4. <span data-ttu-id="b61d4-140">Vælg handlingen **Opret købsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="b61d4-140">Choose the **Create Purchase Invoice** action.</span></span>
5. <span data-ttu-id="b61d4-141">Vælg enten **Alle linjer** eller **Valgte linjer**, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="b61d4-141">Select either **All Lines** or **Selected Lines**, and then choose the **OK** button.</span></span>  
6. <span data-ttu-id="b61d4-142">På listen over kreditorer, der vises, skal du vælge den kreditor, du vil købe alle varerne fra, og derefter vælge knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="b61d4-142">In the list of vendors that appears, select the vendor that you want to buy all the items from, and then choose the **OK** button.</span></span>

    <span data-ttu-id="b61d4-143">Der oprettes en købsfaktura, der indeholder en, flere eller alle linjer på salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="b61d4-143">A purchase invoice is created that contains one, more, or all the lines on the sales invoice.</span></span>
7. <span data-ttu-id="b61d4-144">Fortsæt med at behandle købsfakturaen, for eksempel ved at redigere eller tilføje købsfakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="b61d4-144">Proceed to process the purchase invoice, for example, by editing or adding purchase invoice lines.</span></span> <span data-ttu-id="b61d4-145">Du kan finde flere oplysninger under [Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="b61d4-145">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b61d4-146">Se også</span><span class="sxs-lookup"><span data-stu-id="b61d4-146">See Also</span></span>
[<span data-ttu-id="b61d4-147">Køb</span><span class="sxs-lookup"><span data-stu-id="b61d4-147">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="b61d4-148">Fremgangsmåde: Registrere køb</span><span class="sxs-lookup"><span data-stu-id="b61d4-148">How to: Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="b61d4-149">Fremgangsmåde: Fakturere salg</span><span class="sxs-lookup"><span data-stu-id="b61d4-149">How to: Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="b61d4-150">Fremgangsmåde: Registrere nye kreditorer</span><span class="sxs-lookup"><span data-stu-id="b61d4-150">How to: Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
<span data-ttu-id="b61d4-151">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b61d4-151">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

