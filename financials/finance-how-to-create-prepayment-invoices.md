---
title: "Sådan opretter du forudbetalingsfakturaer | Microsoft Docs"
description: "Få at vide, hvordan du håndterer situationer, hvor du eller din leverandør kræver forudbetaling."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 04d7703df0c1b5e4da8996f00b5f1eed293cbf56
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-prepayment-invoices"></a><span data-ttu-id="2b532-103">Sådan oprettes forudbetalingsfakturarer</span><span class="sxs-lookup"><span data-stu-id="2b532-103">How to: Create Prepayment Invoices</span></span>
<span data-ttu-id="2b532-104">Hvis det er et krav, at dine kunder skal betale, før du leverer en ordre til dem, eller hvis din leverandør kræver, at du skal betale, før de sender en ordre til dig, kan du bruge forudbetalinger.</span><span class="sxs-lookup"><span data-stu-id="2b532-104">If you require your customers to submit payment before you ship an order to them, or if your vendor requires you to submit payment before they ship an order to you, you can use the prepayment functionality.</span></span>  

<span data-ttu-id="2b532-105">Når du har oprettet en salgs- eller købsordre, kan du oprette en forudbetalingsfaktura.</span><span class="sxs-lookup"><span data-stu-id="2b532-105">After you create a sales or purchase order, you can create a prepayment invoice.</span></span> <span data-ttu-id="2b532-106">Du kan bruge standardprocenterne til hver enkelt salgs- eller købslinje, eller du kan regulere beløbet efter behov.</span><span class="sxs-lookup"><span data-stu-id="2b532-106">You can use the default percentages for each sales or purchase line, or you can adjust the amount as necessary.</span></span> <span data-ttu-id="2b532-107">Du kan f.eks. angive et samlet beløb til hele ordren.</span><span class="sxs-lookup"><span data-stu-id="2b532-107">For example, you can specify a total amount for the entire order.</span></span>  

<span data-ttu-id="2b532-108">Følgende procedure beskriver, hvordan du fakturerer en forudbetaling for en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="2b532-108">The following procedure describes how to invoice a prepayment for a sales orders.</span></span> <span data-ttu-id="2b532-109">Fremgangsmåden er den samme for købsordrer.</span><span class="sxs-lookup"><span data-stu-id="2b532-109">The steps are similar for purchase orders.</span></span>  

## <a name="to-create-a-prepayment-invoice"></a><span data-ttu-id="2b532-110">Sådan oprettes en forudbetalingsfaktura</span><span class="sxs-lookup"><span data-stu-id="2b532-110">To create a prepayment invoice</span></span>  
1. <span data-ttu-id="2b532-111">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="2b532-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2b532-112">Opret en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="2b532-112">Create a new sales order.</span></span> <span data-ttu-id="2b532-113">Du kan finde flere oplysninger i [Fremgangsmåde: Sælge produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="2b532-113">For more information, see [How to: sell Products](sales-how-sell-products.md).</span></span>  

    <span data-ttu-id="2b532-114">I oversigtspanelet **Forudbetaling**, udfyldes feltet **Forudbetaling i %** automatisk, hvis der er angivet en standardforudbetalingsprocent på debitorkortet.</span><span class="sxs-lookup"><span data-stu-id="2b532-114">On the **Prepayment** FastTab, the **Prepayment %** field will be filled in automatically if there is a default prepayment percentage on the customer card.</span></span> <span data-ttu-id="2b532-115">Du kan ændre indholdet i feltet.</span><span class="sxs-lookup"><span data-stu-id="2b532-115">You can change the contents of the field.</span></span> <span data-ttu-id="2b532-116">Forudbetalingsprocenten kopieres kun fra hovedet til de linjer, hvor standardforudbetalingsprocenten ikke kopieres fra varen.</span><span class="sxs-lookup"><span data-stu-id="2b532-116">The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.</span></span>  

    <span data-ttu-id="2b532-117">Hvis afkrydsningsfeltet **Komprimer forudbetaling** er markeret, samles linjerne på fakturaen, hvis:</span><span class="sxs-lookup"><span data-stu-id="2b532-117">If the **Compress Prepayment** field is selected, lines will be combined on the invoice if:</span></span>  
    - <span data-ttu-id="2b532-118">De har samme finanskonto til forudbetalinger, som angivet i bogføringsopsætning.</span><span class="sxs-lookup"><span data-stu-id="2b532-118">They have the same general ledger account for prepayments as determined by the general posting setup.</span></span>  
    - <span data-ttu-id="2b532-119">De har samme dimensioner.</span><span class="sxs-lookup"><span data-stu-id="2b532-119">They have the same dimensions.</span></span>  

    <span data-ttu-id="2b532-120">Lad feltet være tomt, hvis du vil angive en forudbetalingsfaktura med én linje for hver salgsordre, der har en forudbetalingsprocent.</span><span class="sxs-lookup"><span data-stu-id="2b532-120">Leave the field blank if you want to specify a prepayment invoice with one line for each sales order line that has a prepayment percentage.</span></span>  

3. <span data-ttu-id="2b532-121">Udfyld salgslinjerne.</span><span class="sxs-lookup"><span data-stu-id="2b532-121">Fill in the sales lines.</span></span>  

    <span data-ttu-id="2b532-122">Hvis der er oprettet standardforudbetalingsprocenter til dine varer, kopieres de automatisk til feltet **Forudbetaling i %** på linjen.</span><span class="sxs-lookup"><span data-stu-id="2b532-122">If default prepayment percentages have been set up for your items, they are automatically copied to the **Prepayment %** field on the line.</span></span> <span data-ttu-id="2b532-123">Ellers kopieres forudbetalingsprocenten fra hovedet.</span><span class="sxs-lookup"><span data-stu-id="2b532-123">Otherwise, the prepayment percentage is copied from the header.</span></span> <span data-ttu-id="2b532-124">Du kan ændre indholdet i feltet **Forudbetaling i %** på linjen.</span><span class="sxs-lookup"><span data-stu-id="2b532-124">You can change the contents of the **Prepayment %** field on the line.</span></span>  
4. <span data-ttu-id="2b532-125">Hvis du vil bruge én forudbetalingsprocent til hele ordren, skal du ændre feltet **Forudbetaling i %** i hovedet, efter at du har udfyldt linjerne.</span><span class="sxs-lookup"><span data-stu-id="2b532-125">If you want to apply one prepayment percentage to the entire order, change the **Prepayment %** field on the header after filling in the lines.</span></span>  
5. <span data-ttu-id="2b532-126">Du kan se det samlede forudbetalingsbeløb ved at vælge handlingen **Statistik**.</span><span class="sxs-lookup"><span data-stu-id="2b532-126">To view the total prepayment amount, choose the **Statistics** action.</span></span>

    <span data-ttu-id="2b532-127">Hvis du vil regulere det samlede forudbetalingsbeløb for ordren, kan du ændre indholdet i feltet **Forudbetalingsbeløb** i vinduet **Salgsordrestatistik**.</span><span class="sxs-lookup"><span data-stu-id="2b532-127">If you want to adjust the total prepayment amount for the order, you can change the contents of the **Prepayment Amount** field in the **Sales Order Statistics** window.</span></span>  

    <span data-ttu-id="2b532-128">Hvis feltet **Priser inkl. moms** er markeret, kan feltet **Forudbetalingsbeløb Inkl. moms** redigeres.</span><span class="sxs-lookup"><span data-stu-id="2b532-128">If the **Prices Including VAT** field is selected, the **Prepayment Amount Incl. VAT** field is editable.</span></span>  

    <span data-ttu-id="2b532-129">Hvis du ændrer indholdet i feltet **Forudbetalingsbeløb**, fordeles beløbet proportionalt mellem alle linjerne bortset fra dem, hvor der står **0** i feltet **Forudbetaling i %**.</span><span class="sxs-lookup"><span data-stu-id="2b532-129">If you change the contents of the **Prepayment Amount** field, the amount will be distributed proportionately between all lines, except those that have **0** in the **Prepayment %** field.</span></span>  
6. <span data-ttu-id="2b532-130">For at udskrive en kontrolrapport, inden du bogfører forudbetalingsfakturaen, skal du vælge handlingen **Forudbetaling** og derefter vælge **Forudbetalingstestrapport**.</span><span class="sxs-lookup"><span data-stu-id="2b532-130">To print a test report before posting the prepayment invoice, choose the **Prepayment** action, and then choose the **Prepayment Test Report** action.</span></span>  
7. <span data-ttu-id="2b532-131">For at bogføre forudbetalingsfakturaen skal du vælge handlingen **Forudbetaling** og derefter vælge handlingen **Bogfør forudbetalingsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="2b532-131">To post the prepayment invoice, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action.</span></span>  

    <span data-ttu-id="2b532-132">Hvis du både vil bogføre og udskrive forudbetalingsfakturaen, skal du vælge handlingen **Bogfør og udskriv forudbetalingsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="2b532-132">To post and print the prepayment invoice, choose the **Post and Print Prepmt. Invoice** action.</span></span>  

<span data-ttu-id="2b532-133">Du kan udstede flere forudbetalingsfakturaer til ordren.</span><span class="sxs-lookup"><span data-stu-id="2b532-133">You can issue additional prepayment invoices for the order.</span></span> <span data-ttu-id="2b532-134">I så fald skal du øge forudbetalingsbeløbet på en eller flere linjer, justere dokumentdatoen, hvis det er nødvendigt, og bogføre forudbetalingsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="2b532-134">To do this, increase the prepayment amount on one or more lines, adjust the document date if necessary, and post the prepayment invoice.</span></span> <span data-ttu-id="2b532-135">Der oprettes en ny faktura, som dækker differencen mellem de forudbetalte beløb, der er faktureret indtil videre, og det nye forudbetalingsbeløb.</span><span class="sxs-lookup"><span data-stu-id="2b532-135">A new invoice will be created for the difference between the prepayment amounts invoiced so far and the new prepayment amount.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2b532-136">Hvis du befinder dig i USA, kan du ikke ændre forudbetalingsprocenten, når forudbetalingsfakturaen er blevet bogført.</span><span class="sxs-lookup"><span data-stu-id="2b532-136">If you are located in North America, you cannot change the prepayment percentage after the prepayment invoice has been posted.</span></span> <span data-ttu-id="2b532-137">Dette forhindres i den amerikanske version af [!INCLUDE[d365fin](includes/d365fin_md.md)], fordi beregningen af moms ellers ville være forkert.</span><span class="sxs-lookup"><span data-stu-id="2b532-137">This is prevented in the North American version of [!INCLUDE[d365fin](includes/d365fin_md.md)] because the calculation of sales tax will otherwise be incorrect.</span></span>  

 <span data-ttu-id="2b532-138">Når du er klar til at bogføre resten af fakturaen, skal du benytte samme fremgangsmåde som med alle andre fakturaer, hvorefter det forudbetalte beløb automatisk trækkes fra det forfaldne beløb.</span><span class="sxs-lookup"><span data-stu-id="2b532-138">When you are ready to post the rest of the invoice, post it as you would post any invoice, and the prepayment amount will automatically be deducted from the amount due.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2b532-139">Se også</span><span class="sxs-lookup"><span data-stu-id="2b532-139">See Also</span></span>  
[<span data-ttu-id="2b532-140">Fakturere forudbetalinger</span><span class="sxs-lookup"><span data-stu-id="2b532-140">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="2b532-141">Gennemgang: Opsætning og fakturering af salgsforudbetalinger</span><span class="sxs-lookup"><span data-stu-id="2b532-141">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="2b532-142">Finans</span><span class="sxs-lookup"><span data-stu-id="2b532-142">Finance</span></span>](finance.md)  
<span data-ttu-id="2b532-143">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2b532-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
