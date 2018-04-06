---
title: Oversigt over opgaver til administration af kreditorer | Microsoft Docs
description: "Beskriver opgaver til administration af kreditorer, f.eks. betaling af kreditorer eller udligning af udgående betalinger til finansposter, for at lukke fakturaer eller kreditnotaer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: d59c00f7a00854639250ae587805dece50fd1d78
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="managing-payables"></a><span data-ttu-id="824fc-103">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="824fc-103">Managing Payables</span></span>
<span data-ttu-id="824fc-104">En vigtig del af styring af kreditorer er betaling af dine kreditorer eller refundering af medarbejderne for udgifter.</span><span class="sxs-lookup"><span data-stu-id="824fc-104">A big part of managing accounts payable is paying your vendors, or reimbursing your employees for expenses.</span></span> <span data-ttu-id="824fc-105">Du kan bruge funktioner til at tilføje betalingslinjer for forfaldne købsfakturaer i vinduet **Udbetalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="824fc-105">You can use functions to add payments lines for purchase invoices that are due in the **Payment Journal** window.</span></span> <span data-ttu-id="824fc-106">Du kan transaktionerne til din bank ved at eksportere flere betalingskladdelinjer til en fil og derefter overføre filen til din bank.</span><span class="sxs-lookup"><span data-stu-id="824fc-106">To send transactions to your bank, you can export multiple payment journal lines to a file, and then upload the file to your bank.</span></span> <span data-ttu-id="824fc-107">Du kan også oprette betalinger med check, herunder overføre checks som elektronisk betaling.</span><span class="sxs-lookup"><span data-stu-id="824fc-107">You can also make payments by check, including transmitting checks as electronic payments.</span></span>

<span data-ttu-id="824fc-108">En anden typiske opgave er at udligne udgående betalinger til de relaterede kreditor- eller medarbejderposter for at lukke købsfakturaer, købskreditnotaer eller medarbejderkonti som betalt.</span><span class="sxs-lookup"><span data-stu-id="824fc-108">Another typical task is to apply outgoing payments to their related vendor or employee ledger entries in order to close purchase invoices, purchase credit memos, or employee accounts as paid.</span></span> <span data-ttu-id="824fc-109">Du kan gøre dette i vinduet **Betalingsudligningskladde** ved at importere en bankkontoudtogsfil for at registrere betalinger.</span><span class="sxs-lookup"><span data-stu-id="824fc-109">You can do this in the **Payment Reconciliation Journal** window by importing a bank statement file to register the payments.</span></span> <span data-ttu-id="824fc-110">Betalingerne udlignes til at åbne kreditor-, debitor- eller medarbejderposter ved at sammenligne betalingstekst og oplysninger i posten.</span><span class="sxs-lookup"><span data-stu-id="824fc-110">The payments are applied to open vendor, customer, or employee ledger entries by matching payment text and entry information.</span></span> <span data-ttu-id="824fc-111">Der er forskellige måder at gennemgå og ændre mulighederne, før du bogfører kladden.</span><span class="sxs-lookup"><span data-stu-id="824fc-111">There are various ways to review and change the matches before you post the journal.</span></span> <span data-ttu-id="824fc-112">Du kan vælge at lukke alle åbne bankposter vedrørende de udlignede poster, når du bogfører kladden.</span><span class="sxs-lookup"><span data-stu-id="824fc-112">You can choose to close any open bank account ledger entries related to the applied ledger entries when you post the journal.</span></span> <span data-ttu-id="824fc-113">Bankkontoen udlignes automatisk, når alle betalinger er udlignet.</span><span class="sxs-lookup"><span data-stu-id="824fc-113">The bank account is automatically reconciled when all payments are applied.</span></span>

<span data-ttu-id="824fc-114">Du kan også udligne udgående betalinger manuelt i vinduet **Udbetalingskladde** eller fra de relaterede kreditor- eller medarbejderposter.</span><span class="sxs-lookup"><span data-stu-id="824fc-114">Alternatively, you can apply outgoing payments manually in the **Payment Journal** window or from the related vendor or employee ledger entries.</span></span>

<span data-ttu-id="824fc-115">Den følgende tabel indeholder en opgavesekvens i kreditorer med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="824fc-115">The following table describes a sequence of tasks within accounts payable, with links to the topics that describe them.</span></span>

| <span data-ttu-id="824fc-116">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="824fc-116">To</span></span> | <span data-ttu-id="824fc-117">Se</span><span class="sxs-lookup"><span data-stu-id="824fc-117">See</span></span> |
| --- | --- |
| <span data-ttu-id="824fc-118">Oprette forfaldne kreditorbetalinger eller medarbejderrefusioner, skal du forberede checkindbetalinger og udlæse betalinger til en bankfil, når du bogfører.</span><span class="sxs-lookup"><span data-stu-id="824fc-118">Generate due vendor payments or employee reimbursements, prepare check payments, and export payments to a bank file when posting.</span></span> |[<span data-ttu-id="824fc-119">Foretage betaling</span><span class="sxs-lookup"><span data-stu-id="824fc-119">Making Payments</span></span>](payables-make-payments.md) |
| <span data-ttu-id="824fc-120">Udlign kreditorbetalinger automatisk til ubetalte købsfakturaer ved at importere en bankkontoudtogsfil.</span><span class="sxs-lookup"><span data-stu-id="824fc-120">Apply vendor payments automatically to unpaid purchase invoices by importing a bank statement file.</span></span> |[<span data-ttu-id="824fc-121">Udligne betalinger automatisk og afstemme bankkonti</span><span class="sxs-lookup"><span data-stu-id="824fc-121">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="824fc-122">Udlign kreditorbetalinger til ubetalte købsfakturaer manuelt.</span><span class="sxs-lookup"><span data-stu-id="824fc-122">Apply vendor payments to unpaid purchase invoices manually.</span></span> |[<span data-ttu-id="824fc-123">Udligne kreditorbetalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="824fc-123">Reconcile Vendor Payments Manually</span></span>](payables-how-apply-purchase-transactions-manually.md) |
|<span data-ttu-id="824fc-124">Du kan sikre korrekt værdiansættelse af lageret ved at tildele ekstra vareomkostninger, f.eks. fragt, fysisk håndtering, forsikring og transport, som du har ved køb eller salg af varer.</span><span class="sxs-lookup"><span data-stu-id="824fc-124">Ensure correct inventory valuation by assigning added item costs, such as freight, physical handling, insurance, and transportation that you incur when purchasing.</span></span>|[<span data-ttu-id="824fc-125">Bruge varegebyrer til at angive ekstra handelsomkostninger</span><span class="sxs-lookup"><span data-stu-id="824fc-125">Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)|

## <a name="see-also"></a><span data-ttu-id="824fc-126">Se også</span><span class="sxs-lookup"><span data-stu-id="824fc-126">See Also</span></span>
[<span data-ttu-id="824fc-127">Køb</span><span class="sxs-lookup"><span data-stu-id="824fc-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="824fc-128">Administrere tilgodehavender</span><span class="sxs-lookup"><span data-stu-id="824fc-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="824fc-129">Bruge varegebyrer til at angive ekstra handelsomkostninger</span><span class="sxs-lookup"><span data-stu-id="824fc-129">Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)  
[<span data-ttu-id="824fc-130">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="824fc-130">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="824fc-131">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="824fc-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

