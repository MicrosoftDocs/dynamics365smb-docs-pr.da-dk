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
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9684a91268927a4f1f4d249fef019c8f6ac00325
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="managing-payables"></a><span data-ttu-id="4c3a7-103">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="4c3a7-103">Managing Payables</span></span>
<span data-ttu-id="4c3a7-104">En vigtig del af styring af gæld er at betale sine kreditorer.</span><span class="sxs-lookup"><span data-stu-id="4c3a7-104">A big part of managing accounts payable is paying your vendors.</span></span> <span data-ttu-id="4c3a7-105">Du kan bruge funktioner til at tilføje betalingslinjer for forfaldne købsfakturaer i vinduet **Udbetalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="4c3a7-105">You can use functions to add payments lines for purchase invoices that are due in the **Payment Journal** window.</span></span> <span data-ttu-id="4c3a7-106">Du kan transaktionerne til din bank ved at eksportere flere betalingskladdelinjer til en fil og derefter overføre filen til din bank.</span><span class="sxs-lookup"><span data-stu-id="4c3a7-106">To send transactions to your bank, you can export multiple payment journal lines to a file, and then upload the file to your bank.</span></span> <span data-ttu-id="4c3a7-107">Du kan også oprette betalinger med check, herunder overføre checks som elektronisk betaling.</span><span class="sxs-lookup"><span data-stu-id="4c3a7-107">You can also make payments by check, including transmitting checks as electronic payments.</span></span>

<span data-ttu-id="4c3a7-108">En anden typiske opgave er at udligne udgående betalinger til de relaterede kreditorposter for at lukke købsfakturaer eller købskreditnotaer som betalt.</span><span class="sxs-lookup"><span data-stu-id="4c3a7-108">Another typical task is to apply outgoing payments to their related vendor ledger entries in order to close purchase invoices or purchase credit memos as paid.</span></span> <span data-ttu-id="4c3a7-109">Du kan gøre dette i vinduet **Betalingsudligningskladde** ved at importere en bankkontoudtogsfil for at registrere betalinger.</span><span class="sxs-lookup"><span data-stu-id="4c3a7-109">You can do this in the **Payment Reconciliation Journal** window by importing a bank statement file to register the payments.</span></span> <span data-ttu-id="4c3a7-110">Betalingerne anvendes til at åbne kreditor- eller debitorposter ved at sammenligne betalingstekst og oplysninger i posten.</span><span class="sxs-lookup"><span data-stu-id="4c3a7-110">The payments are applied to open vendor or customer ledger entries by matching payment text and entry information.</span></span> <span data-ttu-id="4c3a7-111">Der er forskellige måder at gennemgå og ændre mulighederne, før du bogfører kladden.</span><span class="sxs-lookup"><span data-stu-id="4c3a7-111">There are various ways to review and change the matches before you post the journal.</span></span> <span data-ttu-id="4c3a7-112">Du kan vælge at lukke alle åbne bankposter vedrørende de udlignede poster, når du bogfører kladden.</span><span class="sxs-lookup"><span data-stu-id="4c3a7-112">You can choose to close any open bank account ledger entries related to the applied ledger entries when you post the journal.</span></span> <span data-ttu-id="4c3a7-113">Bankkontoen udlignes automatisk, når alle betalinger er udlignet.</span><span class="sxs-lookup"><span data-stu-id="4c3a7-113">The bank account is automatically reconciled when all payments are applied.</span></span>

<span data-ttu-id="4c3a7-114">Du kan også udligne udgående betalinger manuelt i vinduet **Udbetalingskladde** eller fra de relaterede kreditorposter.</span><span class="sxs-lookup"><span data-stu-id="4c3a7-114">Alternatively, you can apply outgoing payments manually in the **Payment Journal** window or from the related vendor ledger entries.</span></span>

<span data-ttu-id="4c3a7-115">Den følgende tabel indeholder en opgavesekvens i kreditorer med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="4c3a7-115">The following table describes a sequence of tasks within accounts payable, with links to the topics that describe them.</span></span>

| <span data-ttu-id="4c3a7-116">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="4c3a7-116">To</span></span> | <span data-ttu-id="4c3a7-117">Se</span><span class="sxs-lookup"><span data-stu-id="4c3a7-117">See</span></span> |
| --- | --- |
| <span data-ttu-id="4c3a7-118">Generer forfaldne kreditorbetalinger prioriteret efter betalingsrabatter og strafgebyrer for overskridelser.</span><span class="sxs-lookup"><span data-stu-id="4c3a7-118">Generate due vendor payments prioritized according to payment discounts and overdue penalties.</span></span> <span data-ttu-id="4c3a7-119">Du kan også udlæse betalingerne til en bankfil ved bogføring.</span><span class="sxs-lookup"><span data-stu-id="4c3a7-119">Optionally, export the payments to a bank file when posting.</span></span> |[<span data-ttu-id="4c3a7-120">Foretage indbetalinger</span><span class="sxs-lookup"><span data-stu-id="4c3a7-120">Make Payments</span></span>](payables-make-payments.md) |
| <span data-ttu-id="4c3a7-121">Udlign kreditorbetalinger automatisk til ubetalte købsfakturaer ved at importere en bankkontoudtogsfil.</span><span class="sxs-lookup"><span data-stu-id="4c3a7-121">Apply vendor payments automatically to unpaid purchase invoices by importing a bank statement file.</span></span> |[<span data-ttu-id="4c3a7-122">Udligne betalinger automatisk og afstemme bankkonti</span><span class="sxs-lookup"><span data-stu-id="4c3a7-122">Apply Payments Automatically and Reconcile Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="4c3a7-123">Udlign kreditorbetalinger til ubetalte købsfakturaer manuelt.</span><span class="sxs-lookup"><span data-stu-id="4c3a7-123">Apply vendor payments to unpaid purchase invoices manually.</span></span> |[<span data-ttu-id="4c3a7-124">Fremgangsmåde: Udligne kreditorbetalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="4c3a7-124">How to: Reconcile Vendor Payments Manually</span></span>](payables-how-apply-purchase-transactions-manually.md) |
|<span data-ttu-id="4c3a7-125">Du kan sikre korrekt værdiansættelse af lageret ved at tildele ekstra vareomkostninger, f.eks. fragt, fysisk håndtering, forsikring og transport, som du har ved køb eller salg af varer.</span><span class="sxs-lookup"><span data-stu-id="4c3a7-125">Ensure correct inventory valuation by assigning added item costs, such as freight, physical handling, insurance, and transportation that you incur when purchasing.</span></span>|[<span data-ttu-id="4c3a7-126">Fremgangsmåde: Bruge varegebyrer til at angive ekstra handelsomkostninger</span><span class="sxs-lookup"><span data-stu-id="4c3a7-126">How to: Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)|

## <a name="see-also"></a><span data-ttu-id="4c3a7-127">Se også</span><span class="sxs-lookup"><span data-stu-id="4c3a7-127">See Also</span></span>
[<span data-ttu-id="4c3a7-128">Køb</span><span class="sxs-lookup"><span data-stu-id="4c3a7-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="4c3a7-129">Administrere tilgodehavender</span><span class="sxs-lookup"><span data-stu-id="4c3a7-129">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="4c3a7-130">Fremgangsmåde: Bruge varegebyrer til at angive ekstra handelsomkostninger</span><span class="sxs-lookup"><span data-stu-id="4c3a7-130">How to: Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)  
[<span data-ttu-id="4c3a7-131">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="4c3a7-131">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="4c3a7-132">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4c3a7-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

