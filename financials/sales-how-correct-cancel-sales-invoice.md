---
title: "Rette eller annullere en bogført salgsfaktura | Microsoft Docs"
description: "Beskriver, hvordan du kan rette, fortryde eller annullere en bogført salgsfaktura og anvende en salgskreditnota."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e8e5a4762564d036ac8c0e7bdaf9e13b448d37f4
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="correct-or-cancel-unpaid-sales-invoices"></a><span data-ttu-id="e8b2d-103">Rette eller annullere ubetalte salgsfakturaer</span><span class="sxs-lookup"><span data-stu-id="e8b2d-103">Correct or Cancel Unpaid Sales Invoices</span></span>
<span data-ttu-id="e8b2d-104">Du kan rette eller annullere en bogført salgsfaktura.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-104">You can correct or cancel a posted sales invoice.</span></span> <span data-ttu-id="e8b2d-105">Dette er nyttigt, hvis du laver en fejl, eller hvis debitoren anmoder om en ændring.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-105">This is useful if you make a mistake or if the customer requests a change.</span></span>

> [!NOTE]  
>   <span data-ttu-id="e8b2d-106">Efter en bogført salgsfaktura er blevet helt eller delvist betalt, kan du ikke rette eller annullere den fra selve den bogførte salgsfaktura.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-106">After a posted sales invoice has been partially or fully paid, you cannot correct or cancel it from the posted sales invoice itself.</span></span> <span data-ttu-id="e8b2d-107">I stedet for skal du manuelt oprette en salgskreditnota for at gøre salget ugyldigt og tilbagebetale debitoren, evt. administreret med en salgsreturvareordre.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-107">Instead, you must manually create a sales credit memo to void the sale and reimburse the customer, optionally managed with a sales return order.</span></span> <span data-ttu-id="e8b2d-108">Du kan finde flere oplysninger i [Behandle salgsreturvarer eller annulleringer](sales-how-process-sales-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="e8b2d-108">For more information, see [Process Sales Returns or Cancellations](sales-how-process-sales-returns-cancellations.md).</span></span>

<span data-ttu-id="e8b2d-109">I vinduet **Bogført salgsfaktura** skal du vælge handlingen **Ret** eller **Annuller** for at udføre de handlinger, der er beskrevet i den følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-109">In the **Posted Sales Invoice** window, you can choose the **Correct** action or the **Cancel** action to perform the actions that are described in the following table.</span></span>

| <span data-ttu-id="e8b2d-110">Handling</span><span class="sxs-lookup"><span data-stu-id="e8b2d-110">Action</span></span> | <span data-ttu-id="e8b2d-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e8b2d-111">Description</span></span> |
| --- | --- |
| <span data-ttu-id="e8b2d-112">**Ret**</span><span class="sxs-lookup"><span data-stu-id="e8b2d-112">**Correct**</span></span> |<span data-ttu-id="e8b2d-113">Den bogførte salgsfaktura er annulleret.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-113">The posted sales invoice is canceled.</span></span> <span data-ttu-id="e8b2d-114">En ny salgsfaktura med de samme oplysninger oprettes.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-114">A new sales invoice with the same information is created.</span></span> <span data-ttu-id="e8b2d-115">Du kan foretage rettelsen og derefter fortsætte salget.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-115">You can make the correction and then continue the sales process.</span></span> <span data-ttu-id="e8b2d-116">Den nye salgsfaktura har et andet nummer end den første salgsfaktura.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-116">The new sales invoice has a different number than the initial sales invoice.</span></span> <span data-ttu-id="e8b2d-117">En rettelsessalgskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte salgsfaktura.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-117">A corrective sales credit memo is automatically created and posted to void the initial posted sales invoice.</span></span> <span data-ttu-id="e8b2d-118">På den oprindeligt bogførte salgsfaktura er afkrydsningsfelterne Annuller og Betalt markeret.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-118">On the initial posted sales invoice, the Canceled and Paid check boxes are selected.</span></span> |
| <span data-ttu-id="e8b2d-119">**Annuller**</span><span class="sxs-lookup"><span data-stu-id="e8b2d-119">**Cancel**</span></span> |<span data-ttu-id="e8b2d-120">Den bogførte salgsfaktura er annulleret.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-120">The posted sales invoice is canceled.</span></span> <span data-ttu-id="e8b2d-121">En rettelsessalgskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte salgsfaktura.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-121">A corrective sales credit memo is automatically created and posted to void the initial posted sales invoice.</span></span> <span data-ttu-id="e8b2d-122">På den oprindeligt bogførte salgsfaktura er afkrydsningsfelterne Annuller og Betalt markeret.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-122">On the initial posted sales invoice, the Canceled and Paid check boxes are selected.</span></span> |

<span data-ttu-id="e8b2d-123">Når du retter eller annullerer en bogført salgsfaktura, anvendes den rettede salgskreditnota på alle finanskonti og lageropgørelsesposter, der blev oprettet, da den oprindelige salgsfaktura blev bogført.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-123">When you correct or cancel a posted sales invoice, the corrective sales credit memo is applied to all general ledger and inventory ledger entries that were created when the initial sales invoice was posted.</span></span> <span data-ttu-id="e8b2d-124">På denne måde tilbageføres den bogførte salgsfaktura i dine finansposter, og rettelsessalgskreditnotaen efterlades til revisionsspor.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-124">This reverses the posted sales invoice in your financial records and leaves the corrective posted sales credit memo for your audit trail.</span></span>

## <a name="to-correct-a-posted-sales-invoice"></a><span data-ttu-id="e8b2d-125">Hvis du vil rette en bogført salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="e8b2d-125">To correct a posted sales invoice</span></span>
1. <span data-ttu-id="e8b2d-126">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogf. salgsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e8b2d-127">Vælg den bogførte salgsfaktura, som du vil rette.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-127">Select the posted sales invoice that you want to correct.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="e8b2d-128">Hvis afkrydsningsfeltet **Annulleret** er markeret, kan du ikke rette den bogførte salgsfaktura, da den allerede er rettet eller annulleret.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-128">If the **Canceled** check box is selected, then you cannot correct the posted sales invoice because it has already been corrected or canceled.</span></span>
3. <span data-ttu-id="e8b2d-129">I vinduet **Bogført salgsfaktura** skal du vælge handlingen **Ret**.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-129">In the **Posted Sales Invoice** window, choose the **Correct** action.</span></span>  
4. <span data-ttu-id="e8b2d-130">En ny salgsfaktura med de samme oplysninger oprettes, hvor du kan foretage en rettelse.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-130">A new sales invoice with the same information is created where you can make the correction.</span></span> <span data-ttu-id="e8b2d-131">Feltet **Annulleret** på den første bogførte salgsfaktura ændres til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-131">The **Canceled** field on the initial posted sales invoice is changed to **Yes**.</span></span>

    <span data-ttu-id="e8b2d-132">En salgskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte salgsfaktura.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-132">A sales credit memo is automatically created and posted to void the initial posted sales invoice.</span></span>
5. <span data-ttu-id="e8b2d-133">Vælg handlingen **Vis rettelseskreditnota** for at få vist den bogførte salgskreditnota, som gør den oprindelige bogførte salgsfaktura ugyldig.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-133">Choose the **Show Corrective Credit Memo** action to view the posted sales credit memo that voids the initial posted sales invoice.</span></span>

## <a name="to-cancel-a-posted-sales-invoice"></a><span data-ttu-id="e8b2d-134">Hvis du vil annullere en bogført salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="e8b2d-134">To cancel a posted sales invoice</span></span>
1. <span data-ttu-id="e8b2d-135">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogf. salgsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e8b2d-136">Vælg den bogførte salgsfaktura, som du vil annullere.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-136">Select the posted sales invoice that you want to cancel.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="e8b2d-137">Hvis afkrydsningsfeltet **Annulleret** er markeret, kan du ikke annullere den bogførte salgsfaktura, da den allerede er rettet eller annulleret.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-137">If the **Canceled** check box is selected, then you cannot cancel the posted sales invoice because it has already been canceled or corrected.</span></span>
3. <span data-ttu-id="e8b2d-138">I vinduet **Bogført salgsfaktura** skal du vælge handlingen **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-138">In the **Posted Sales Invoice** window, choose the **Cancel** action.</span></span>

    <span data-ttu-id="e8b2d-139">En salgskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte salgsfaktura.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-139">A sales credit memo is automatically created and posted to void the initial posted sales invoice.</span></span> <span data-ttu-id="e8b2d-140">Feltet **Annulleret** på den første bogførte salgsfaktura ændres til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-140">The **Canceled** field on the initial posted sales invoice is changed to **Yes**.</span></span>
4. <span data-ttu-id="e8b2d-141">Vælg **Vis rettelseskreditnota** for at få vist den bogførte salgskreditnota, som gør den oprindelige bogførte salgsfaktura ugyldig.</span><span class="sxs-lookup"><span data-stu-id="e8b2d-141">Choose **Show Corrective Credit Memo** to view the posted sales credit memo that voids the initial posted sales invoice.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8b2d-142">Se også</span><span class="sxs-lookup"><span data-stu-id="e8b2d-142">See Also</span></span>
[<span data-ttu-id="e8b2d-143">Salg</span><span class="sxs-lookup"><span data-stu-id="e8b2d-143">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="e8b2d-144">Konfigurere salg</span><span class="sxs-lookup"><span data-stu-id="e8b2d-144">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="e8b2d-145">Sende dokumenter som mail</span><span class="sxs-lookup"><span data-stu-id="e8b2d-145">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="e8b2d-146">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e8b2d-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

