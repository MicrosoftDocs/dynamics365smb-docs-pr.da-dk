---
title: Registrere og refundere medarbejdernes forretningsrelaterede udgifter
description: Bogfør medarbejdernes udgifter med finanskladden til medarbejderens konto, og bogfør senere en betaling til medarbejderens bankkonto for at refundere for de forretningsrelaterede udgift.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: dd4ce755e3414f19ae501c1d437f3e1d78d565a1
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184395"
---
# <a name="record-and-reimburse-employees-expenses"></a><span data-ttu-id="f71b8-103">Registrere og refundere medarbejdernes udgifter</span><span class="sxs-lookup"><span data-stu-id="f71b8-103">Record and Reimburse Employees' Expenses</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="f71b8-104">understøtter transaktioner for medarbejdere på samme måde som for kreditorer.</span><span class="sxs-lookup"><span data-stu-id="f71b8-104">supports transactions for employees in a similar way as for vendors.</span></span> <span data-ttu-id="f71b8-105">Derfor findes der medarbejderbogføringsgrupper for at sikre, at medarbejderposter bogføres på de relevante konti i regnskabet.</span><span class="sxs-lookup"><span data-stu-id="f71b8-105">Accordingly, employee posting groups exist to make sure that employee ledger entries are posted to the relevant accounts in the general ledger.</span></span>

> [!NOTE]  
> <span data-ttu-id="f71b8-106">Medarbejdertransaktioner kan kun bogføres i den lokale valuta.</span><span class="sxs-lookup"><span data-stu-id="f71b8-106">Employee transactions can be posted in the local currency only.</span></span> <span data-ttu-id="f71b8-107">Refusion af betalinger til medarbejdere understøtter ikke rabatter og betalingstolerancer.</span><span class="sxs-lookup"><span data-stu-id="f71b8-107">Reimbursement payments to employees do not support discounts and payment tolerances.</span></span>

<span data-ttu-id="f71b8-108">Hvis medarbejdere bruger deres egne penge under forretningsaktiviteter, kan du bogføre udgiften til medarbejderens konto.</span><span class="sxs-lookup"><span data-stu-id="f71b8-108">If employees spend their own money during business activities, you can post the expense to the employee's account.</span></span> <span data-ttu-id="f71b8-109">Du kan derefter refundere medarbejderen ved at foretage en betaling til medarbejderens bankkonto, på samme måde som når du betaler leverandører.</span><span class="sxs-lookup"><span data-stu-id="f71b8-109">Then you can reimburse the employee by making a payment to the employee's bank account, similarly to how you pay vendors.</span></span>  

> [!TIP]
> <span data-ttu-id="f71b8-110">I denne artikel forklares det, hvordan du registrerer udgiften i bøgerne og refunderer medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="f71b8-110">This article explains how to record the expense in the books and how to reimburse the employee.</span></span> <span data-ttu-id="f71b8-111">Din organisation kan have en portal eller app, som medarbejderne kan sende deres udgiftsrapporter til.</span><span class="sxs-lookup"><span data-stu-id="f71b8-111">Your organization may have a portal or app where employees can submit their expense reports.</span></span>

<span data-ttu-id="f71b8-112">[!INCLUDE [prod_short](includes/prod_short.md)] er fleksibel nok til at dække mange forskellige fremgangsmåder.</span><span class="sxs-lookup"><span data-stu-id="f71b8-112">[!INCLUDE [prod_short](includes/prod_short.md)] is flexible enough to suit many different practices.</span></span> <span data-ttu-id="f71b8-113">De nøjagtige kontonumre, der skal bruges, afhænger af organisationens konfiguration og processer.</span><span class="sxs-lookup"><span data-stu-id="f71b8-113">The exact account numbers to use depends on your organization's configuration and processes.</span></span>  

## <a name="to-record-an-employees-expense"></a><span data-ttu-id="f71b8-114">Sådan registrerer du en medarbejders udgift</span><span class="sxs-lookup"><span data-stu-id="f71b8-114">To record an employee's expense</span></span>

<span data-ttu-id="f71b8-115">Du bogfører medarbejdernes udgifter på siden **Finanskladde**.</span><span class="sxs-lookup"><span data-stu-id="f71b8-115">You post employees' expenses on the **General Journal** page.</span></span>

1. <span data-ttu-id="f71b8-116">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Finanskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f71b8-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f71b8-117">Åbn det relevante finanskladdenavn.</span><span class="sxs-lookup"><span data-stu-id="f71b8-117">Open the relevant general journal batch.</span></span> <span data-ttu-id="f71b8-118">Du kan finde flere oplysninger i [Arbejde med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="f71b8-118">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="f71b8-119">Udfyld felterne efter behov på en ny kladdelinje.</span><span class="sxs-lookup"><span data-stu-id="f71b8-119">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="f71b8-120">Gentag trin 3 for alle de udgifter, som er påløbet medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="f71b8-120">Repeat step 3 for all the expenses that the employee has incurred.</span></span>

    > [!TIP]  
    > <span data-ttu-id="f71b8-121">Hvis du vil angive flere udgiftslinjer over én modkontolinje for medarbejderens bankkonto, skal du markere afkrydsningsfeltet **Foreslå modkontobeløb** på linjen for kørslen på siden **Finanskladdenavne**.</span><span class="sxs-lookup"><span data-stu-id="f71b8-121">If you want to enter multiple expense lines above one balance-account line for the employee's bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="f71b8-122">Feltet **Beløb** på modkontolinjen udfyldes derefter automatisk med den værdi, der skal bruges til at afstemme udgifterne.</span><span class="sxs-lookup"><span data-stu-id="f71b8-122">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the expenses.</span></span>
5. <span data-ttu-id="f71b8-123">Vælg handlingen **Bogfør** for at registrere udgifter på medarbejderens konto.</span><span class="sxs-lookup"><span data-stu-id="f71b8-123">Choose the **Post** action to record the expenses on the employee's account.</span></span>

## <a name="to-reimburse-an-employee"></a><span data-ttu-id="f71b8-124">Sådan refunderer du en medarbejder</span><span class="sxs-lookup"><span data-stu-id="f71b8-124">To reimburse an employee</span></span>

<span data-ttu-id="f71b8-125">Du refunderer medarbejdere ved at bogføre betalinger til deres bankkonto på siden **Udbetalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="f71b8-125">You reimburse employees by posting payments to their bank account on the **Payment Journal** page.</span></span>  

1. <span data-ttu-id="f71b8-126">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Udbetalingskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f71b8-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="f71b8-127">Åbn den relevante udbetalingskladdekørsel.</span><span class="sxs-lookup"><span data-stu-id="f71b8-127">Open the relevant payment journal batch.</span></span> <span data-ttu-id="f71b8-128">Du kan finde flere oplysninger i [Arbejde med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="f71b8-128">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="f71b8-129">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="f71b8-129">Fill in the fields as necessary.</span></span> <span data-ttu-id="f71b8-130">Du kan finde flere oplysninger i [Foretage betalinger](payables-make-payments.md).</span><span class="sxs-lookup"><span data-stu-id="f71b8-130">For more information, see [Making Payments](payables-make-payments.md).</span></span>
4. <span data-ttu-id="f71b8-131">Du kan også vælge handlingen **Foreslå medarbejderbetaling** for automatisk at indsætte kladdelinjerne for ventende medarbejderrefusioner.</span><span class="sxs-lookup"><span data-stu-id="f71b8-131">Alternatively, choose the **Suggest Employee Payment** action to automatically insert journal lines for pending employee reimbursements.</span></span>
5. <span data-ttu-id="f71b8-132">Vælg handlingen **Bogfør** for at registrere refusionen.</span><span class="sxs-lookup"><span data-stu-id="f71b8-132">Choose the **Post** action to register the reimbursement.</span></span>  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a><span data-ttu-id="f71b8-133">Sådan afstemmes refusioner med medarbejderposter</span><span class="sxs-lookup"><span data-stu-id="f71b8-133">To reconcile reimbursements with employee ledger entries</span></span>

<span data-ttu-id="f71b8-134">Du udligner medarbejderbetalinger til deres relaterede åbne medarbejderposter på samme måde som for kreditorbetalinger, f.eks. på siden **Betalingsudligningskladde**, baseret på de relaterede bankkontoudtogsposter.</span><span class="sxs-lookup"><span data-stu-id="f71b8-134">You apply employee payments to their related open employee ledger entries in the same way as you do for vendor payments, for example on the **Payment Reconciliation Journal** page, based on the related bank statement entries.</span></span> <span data-ttu-id="f71b8-135">Du kan finde flere oplysninger i [Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="f71b8-135">For more information, see [Applying Payments Automatically and Reconciling Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span> <span data-ttu-id="f71b8-136">Du kan også udligne manuelt på siden **Medarbejderposter**.</span><span class="sxs-lookup"><span data-stu-id="f71b8-136">Alternatively, you can apply manually on the **Employee Ledger Entries** page.</span></span> <span data-ttu-id="f71b8-137">Du kan finde flere oplysninger i det relaterede emne [Afstemme kreditorbetalinger med udbetalingskladden eller fra kreditorposter](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="f71b8-137">For more information, see the related [Reconcile Vendor Payments with the Payment Journal or from Vendor Ledger Entries](payables-how-apply-purchase-transactions-manually.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="f71b8-138">Se også</span><span class="sxs-lookup"><span data-stu-id="f71b8-138">See Also</span></span>

[<span data-ttu-id="f71b8-139">Bogføre transaktioner direkte i finansposterne</span><span class="sxs-lookup"><span data-stu-id="f71b8-139">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="f71b8-140">Arbejde med finanskladder</span><span class="sxs-lookup"><span data-stu-id="f71b8-140">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="f71b8-141">Tilbageføre kladdeposteringer og annullere modtagelser/leverancer</span><span class="sxs-lookup"><span data-stu-id="f71b8-141">Reverse Journal Postings and Undo Receipts/Shipments</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="f71b8-142">Finans</span><span class="sxs-lookup"><span data-stu-id="f71b8-142">Finance</span></span>](finance.md)  
<span data-ttu-id="f71b8-143">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f71b8-143">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]