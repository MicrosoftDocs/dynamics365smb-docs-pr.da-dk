---
title: Sådan opretter du forudbetalingsfakturaer | Microsoft Docs
description: Få at vide, hvordan du håndterer situationer, hvor du eller din leverandør kræver forudbetaling.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5f227cc73531111ae15f69d6fba5ac541e28560c
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746862"
---
# <a name="create-prepayment-invoices"></a><span data-ttu-id="16679-103">Oprette forudbetalingsfakturaer</span><span class="sxs-lookup"><span data-stu-id="16679-103">Create Prepayment Invoices</span></span>

<span data-ttu-id="16679-104">Hvis du kræver, at kunderne skal indsende en betaling, før du leverer en ordre til dem, kan du bruge forudbetalingsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="16679-104">If you require your customers to submit payment before you ship an order to them, you can use the prepayment functionality.</span></span> <span data-ttu-id="16679-105">Det samme gælder, hvis din leverandør kræver, at du indsender betalingen, før de leverer en ordre til dig.</span><span class="sxs-lookup"><span data-stu-id="16679-105">The same applies if your vendor requires you to submit payment before they ship an order to you.</span></span>  

<span data-ttu-id="16679-106">Når du har oprettet en salgs- eller købsordre, kan du starte forudbetalingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="16679-106">You can start the prepayment process when you create a sales or purchase order.</span></span> <span data-ttu-id="16679-107">Hvis du har en standardforudbetalingsprocent for denne debitor eller kreditor, vil den automatisk blive medtaget i den oprettede forudbetalingsfaktura.</span><span class="sxs-lookup"><span data-stu-id="16679-107">If you have a default prepayment percentage for this customer or vendor, that will be included automatically in the resulting prepayment invoice.</span></span> <span data-ttu-id="16679-108">Du kan også angive en forudbetalingsprocent for hele dokumentet.</span><span class="sxs-lookup"><span data-stu-id="16679-108">You can also specify a prepayment percentage to the entire document.</span></span>

<span data-ttu-id="16679-109">Når du har oprettet en salgs- eller købsordre, kan du oprette en forudbetalingsfaktura.</span><span class="sxs-lookup"><span data-stu-id="16679-109">After you create a sales or purchase order, you can create a prepayment invoice.</span></span> <span data-ttu-id="16679-110">Du kan bruge standardprocenterne til hver enkelt salgs- eller købslinje, eller du kan regulere beløbet efter behov.</span><span class="sxs-lookup"><span data-stu-id="16679-110">You can use the default percentages for each sales or purchase line, or you can adjust the amount as necessary.</span></span> <span data-ttu-id="16679-111">Du kan f.eks. angive et samlet beløb til hele ordren.</span><span class="sxs-lookup"><span data-stu-id="16679-111">For example, you can specify a total amount for the entire order.</span></span>  

<span data-ttu-id="16679-112">Følgende procedure beskriver, hvordan du fakturerer en forudbetaling for en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="16679-112">The following procedure describes how to invoice a prepayment for a sales order.</span></span> <span data-ttu-id="16679-113">Fremgangsmåden er den samme for købsordrer.</span><span class="sxs-lookup"><span data-stu-id="16679-113">The steps are similar for purchase orders.</span></span>  

## <a name="to-create-a-prepayment-invoice"></a><span data-ttu-id="16679-114">Sådan oprettes en forudbetalingsfaktura</span><span class="sxs-lookup"><span data-stu-id="16679-114">To create a prepayment invoice</span></span>

1. <span data-ttu-id="16679-115">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordre**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="16679-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="16679-116">Opret en ny salgsordre for den ønskede kunde.</span><span class="sxs-lookup"><span data-stu-id="16679-116">Create a new sales order for the relevant customer.</span></span> <span data-ttu-id="16679-117">Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="16679-117">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>  

    <span data-ttu-id="16679-118">I oversigtspanelet **Forudbetaling** angiver feltet **Forudbetaling i %** den procentsats, der skal bruges til at beregne forudbetalingsbeløbet.</span><span class="sxs-lookup"><span data-stu-id="16679-118">On the **Prepayment** FastTab, the **Prepayment %** field specifies the percentage to use to calculate the prepayment amount.</span></span> <span data-ttu-id="16679-119">Feltet udfyldes automatisk, hvis der er angivet en standardforudbetalingsprocent på debitorkortet.</span><span class="sxs-lookup"><span data-stu-id="16679-119">If there is a default prepayment percentage on the customer card, the field is filled in automatically.</span></span> <span data-ttu-id="16679-120">Du kan ændre procentsatsen.</span><span class="sxs-lookup"><span data-stu-id="16679-120">You can change the percentage.</span></span> <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    <span data-ttu-id="16679-121">Vælg feltet **Komprimer forudbetaling**, hvis du vil oprette linjer på forudbetalingsfakturaen, der kombinerer linjer fra salgsordren, hvis:</span><span class="sxs-lookup"><span data-stu-id="16679-121">Choose the **Compress Prepayment** field if you want to create lines on the prepayment invoice that combine lines from the sales order if:</span></span>  

    - <span data-ttu-id="16679-122">De har samme finanskonto til forudbetalinger, som angivet i bogføringsopsætning.</span><span class="sxs-lookup"><span data-stu-id="16679-122">They have the same general ledger account for prepayments as determined by the general posting setup.</span></span>  
    - <span data-ttu-id="16679-123">De har samme dimensioner.</span><span class="sxs-lookup"><span data-stu-id="16679-123">They have the same dimensions.</span></span>  

    <span data-ttu-id="16679-124">Hvis du vil angive en forudbetalingsfaktura med én linje for hver salgsordre, der har en forudbetalingsprocent, skal du ikke vælge feltet **Komprimer forudbetaling**.</span><span class="sxs-lookup"><span data-stu-id="16679-124">If you want to specify a prepayment invoice with one line for each sales order line that has a prepayment percentage, then do not choose the **Compress Prepayment** field.</span></span>  

    <span data-ttu-id="16679-125">Forfaldsdatoen for forudbetalingen beregnes automatisk på grundlag af værdien af **Forudb. - kode for betal.betingelser**.</span><span class="sxs-lookup"><span data-stu-id="16679-125">The due date for the prepayment is calculated automatically based on the value of the **Prepmt. Payment Terms Code**.</span></span>

3. <span data-ttu-id="16679-126">Udfyld salgslinjerne.</span><span class="sxs-lookup"><span data-stu-id="16679-126">Fill in the sales lines.</span></span>  

    <span data-ttu-id="16679-127">Hvis du har angivet en standardforudbetalingsprocent enten for debitoren eller i oversigtspanelet **Forudbetaling** i dette dokument, kopieres denne værdi til hver linje.</span><span class="sxs-lookup"><span data-stu-id="16679-127">If you have specified a default prepayment percentage either for the customer or on the **Prepayment** FastTab on this document, this value is copied to each line.</span></span> <span data-ttu-id="16679-128">Du kan ændre indholdet i feltet **Forudbetaling i %** på linjen.</span><span class="sxs-lookup"><span data-stu-id="16679-128">You can change the contents of the **Prepayment %** field on the line.</span></span>  

4. <span data-ttu-id="16679-129">Du kan se det samlede forudbetalingsbeløb ved at vælge handlingen **Statistik**.</span><span class="sxs-lookup"><span data-stu-id="16679-129">To view the total prepayment amount, choose the **Statistics** action.</span></span>

    <span data-ttu-id="16679-130">Hvis du vil regulere det samlede forudbetalingsbeløb for ordren, kan du ændre indholdet i feltet **Forudbetalingsbeløb** på siden **Salgsordrestatistik**.</span><span class="sxs-lookup"><span data-stu-id="16679-130">If you want to adjust the total prepayment amount for the order, you can change the contents of the **Prepayment Amount** field on the **Sales Order Statistics** page.</span></span>  

    <span data-ttu-id="16679-131">Hvis feltet **Priser inkl. moms** er markeret, kan feltet **Forudbetalingsbeløb Inkl. moms** redigeres.</span><span class="sxs-lookup"><span data-stu-id="16679-131">If the **Prices Including VAT** field is selected, the **Prepayment Amount Incl. VAT** field is editable.</span></span>  

    <span data-ttu-id="16679-132">Hvis du ændrer indholdet i feltet **Forudbetalingsbeløb**, fordeles beløbet proportionalt mellem alle linjerne bortset fra dem, hvor der står **0** i feltet **Forudbetaling i %**.</span><span class="sxs-lookup"><span data-stu-id="16679-132">If you change the contents of the **Prepayment Amount** field, the amount will be distributed proportionately between all lines, except those that have **0** in the **Prepayment %** field.</span></span>  

5. <span data-ttu-id="16679-133">For at udskrive en kontrolrapport, inden du bogfører forudbetalingsfakturaen, skal du vælge handlingen **Forudbetaling** og derefter vælge **Forudbetalingstestrapport**.</span><span class="sxs-lookup"><span data-stu-id="16679-133">To print a test report before posting the prepayment invoice, choose the **Prepayment** action, and then choose the **Prepayment Test Report** action.</span></span>  
6. <span data-ttu-id="16679-134">For at bogføre forudbetalingsfakturaen skal du vælge handlingen **Forudbetaling** og derefter vælge handlingen **Bogfør forudbetalingsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="16679-134">To post the prepayment invoice, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action.</span></span>  

    <span data-ttu-id="16679-135">Hvis du både vil bogføre og udskrive forudbetalingsfakturaen, skal du vælge handlingen **Bogfør og udskriv forudbetalingsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="16679-135">To post and print the prepayment invoice, choose the **Post and Print Prepmt. Invoice** action.</span></span>  

<span data-ttu-id="16679-136">Du kan udstede flere forudbetalingsfakturaer til ordren.</span><span class="sxs-lookup"><span data-stu-id="16679-136">You can issue additional prepayment invoices for the order.</span></span> <span data-ttu-id="16679-137">I så fald skal du øge forudbetalingsbeløbet på en eller flere linjer, justere dokumentdatoen, hvis det er nødvendigt, og bogføre forudbetalingsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="16679-137">To do this, increase the prepayment amount on one or more lines, adjust the document date if necessary, and post the prepayment invoice.</span></span> <span data-ttu-id="16679-138">Der oprettes en ny faktura, som dækker differencen mellem de forudbetalte beløb, der er faktureret indtil videre, og det nye forudbetalingsbeløb.</span><span class="sxs-lookup"><span data-stu-id="16679-138">A new invoice will be created for the difference between the prepayment amounts invoiced so far and the new prepayment amount.</span></span>  

> [!NOTE]  
> <span data-ttu-id="16679-139">Hvis du befinder dig i USA, kan du ikke ændre forudbetalingsprocenten, når forudbetalingsfakturaen er blevet bogført.</span><span class="sxs-lookup"><span data-stu-id="16679-139">If you are located in North America, you cannot change the prepayment percentage after the prepayment invoice has been posted.</span></span> <span data-ttu-id="16679-140">Dette forhindres i den amerikanske version af [!INCLUDE[prod_short](includes/prod_short.md)], fordi beregningen af moms ellers ville være forkert.</span><span class="sxs-lookup"><span data-stu-id="16679-140">This is prevented in the North American version of [!INCLUDE[prod_short](includes/prod_short.md)] because the calculation of sales tax will otherwise be incorrect.</span></span>  

 <span data-ttu-id="16679-141">Når du er klar til at bogføre resten af fakturaen, skal du benytte samme fremgangsmåde som med alle andre fakturaer, hvorefter det forudbetalte beløb automatisk trækkes fra det forfaldne beløb.</span><span class="sxs-lookup"><span data-stu-id="16679-141">When you are ready to post the rest of the invoice, post it as you would post any invoice, and the prepayment amount will automatically be deducted from the amount due.</span></span>  

## <a name="see-also"></a><span data-ttu-id="16679-142">Se også</span><span class="sxs-lookup"><span data-stu-id="16679-142">See Also</span></span>

[<span data-ttu-id="16679-143">Fakturere forudbetalinger</span><span class="sxs-lookup"><span data-stu-id="16679-143">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="16679-144">Gennemgang: Opsætning og fakturering af salgsforudbetalinger</span><span class="sxs-lookup"><span data-stu-id="16679-144">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="16679-145">Finans</span><span class="sxs-lookup"><span data-stu-id="16679-145">Finance</span></span>](finance.md)  
<span data-ttu-id="16679-146">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="16679-146">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
