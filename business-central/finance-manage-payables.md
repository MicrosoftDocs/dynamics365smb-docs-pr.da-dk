---
title: Administrere Kreditor | Microsoft Docs
description: "Oversigt over, hvordan du administrerer kreditorer (Kreditor), herunder kreditorbetalinger, kreditorerne, gæld og forfalden saldo."
services: project-madeira
documentationcenter: 
author: bholtorf
manager: edupont
editor: 
ms.service: dynamics365-business-central
ms.workload: na
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 10/01/2018
ms.author: bholtorf
redirect_url: finance-set-up-cost-accounting
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: abf7e9cf01c8d394a022e384584e32e78c754639
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="managing-payables"></a><span data-ttu-id="8d05c-103">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="8d05c-103">Managing Payables</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="8d05c-104">indeholder det, du behøver for effektivt at administrere kreditorer.</span><span class="sxs-lookup"><span data-stu-id="8d05c-104">has what you need to effectively manage accounts payable.</span></span>  

## <a name="payments"></a><span data-ttu-id="8d05c-105">Udbetaling kladde</span><span class="sxs-lookup"><span data-stu-id="8d05c-105">Payments</span></span>
<span data-ttu-id="8d05c-106">Det er nemt at prioritere betalinger, tage højde for strafgebyrer for forfaldne betalinger og håndtere kontantrabatter for førtidige betalinger.</span><span class="sxs-lookup"><span data-stu-id="8d05c-106">It's easy to prioritize payments, account for penalties for overdue payments, and handle discounts for early payments.</span></span>

<span data-ttu-id="8d05c-107">Du kan registrere betalinger i en finanskladde og derefter udskrive checks, inden du bogfører udbetalingskladden.</span><span class="sxs-lookup"><span data-stu-id="8d05c-107">You can record payments in a general journal, and then print checks before posting the payment journal.</span></span>

<span data-ttu-id="8d05c-108">Du kan udligne betalinger for at lukke fakturaer, når du bogfører betalingen, eller efter du har bogført betalingen.</span><span class="sxs-lookup"><span data-stu-id="8d05c-108">You can apply payments to close invoices when you post the payment, or after you post the payment.</span></span> <span data-ttu-id="8d05c-109">Feltet **Udligningsmetode**, som er angivet for kreditoren (på **Kreditorkort**), er bestemmende for, om du skal foretage betalingen manuelt, eller om det sker automatisk.</span><span class="sxs-lookup"><span data-stu-id="8d05c-109">The **Application Method** specified for the vendor (on the **Vendor Card**) determines whether you apply the payment manually, or automatically.</span></span> <span data-ttu-id="8d05c-110">Du kan altid udligne transaktioner manuelt.</span><span class="sxs-lookup"><span data-stu-id="8d05c-110">You can always apply transactions manually.</span></span> <span data-ttu-id="8d05c-111">Men hvis udligningsmetoden for kreditor er **Saldo**, og du ikke angiver et dokument som betalingen skal udlignes til, bliver betalingen udlignet til den ældste åbne post for kreditoren.</span><span class="sxs-lookup"><span data-stu-id="8d05c-111">However, if the application method for the vendor is **Apply to Oldest**, and you do not specify a document to apply the payment to, the payment is applied to the oldest open entry for the vendor.</span></span>

## <a name="suggest-vendor-payments"></a><span data-ttu-id="8d05c-112">Lav forslag</span><span class="sxs-lookup"><span data-stu-id="8d05c-112">Suggest Vendor Payments</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="8d05c-113">kan foreslå forskellige betalinger til kreditorer. Det kan f.eks. være betalinger, som snart forfalder, eller som omfatter rabat.</span><span class="sxs-lookup"><span data-stu-id="8d05c-113">can suggest various payments to vendors, such as payments that will be due soon, or payments where a discount is available.</span></span> <span data-ttu-id="8d05c-114">Betalingsforslaget kan tage et beløb i betragtning, som du angiver som tilgængelige midler til betaling og berettigelse af kontantrabat.</span><span class="sxs-lookup"><span data-stu-id="8d05c-114">The payment suggestion can consider an amount that you specify as available funds for payment, and eligibility for payment discounts.</span></span>

## <a name="issue-checks"></a><span data-ttu-id="8d05c-115">Udstede checks</span><span class="sxs-lookup"><span data-stu-id="8d05c-115">Issue Checks</span></span>
<span data-ttu-id="8d05c-116">I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du udstede checks til kreditorer manuelt og elektronisk.</span><span class="sxs-lookup"><span data-stu-id="8d05c-116">[!INCLUDE[d365fin](includes/d365fin_md.md)] lets you issue checks to vendors manually and electronically.</span></span> <span data-ttu-id="8d05c-117">Du kan gøre begge dele på siden **Udbetalingskladder**, hvor du kan også annullere checks og se checkposter.</span><span class="sxs-lookup"><span data-stu-id="8d05c-117">You do both on the **Payment Journals** page, where you can also void checks and view check ledger entries.</span></span>

## <a name="export-payments-to-a-bank-file"></a><span data-ttu-id="8d05c-118">Eksportere betalinger til en bankfil</span><span class="sxs-lookup"><span data-stu-id="8d05c-118">Export Payments to a Bank File</span></span>
<span data-ttu-id="8d05c-119">Når du er klar til at betale en kreditor fra siden **Udbetalingskladde**, kan du eksportere en fil med betalingsoplysningerne fra kladdelinjerne.</span><span class="sxs-lookup"><span data-stu-id="8d05c-119">When you are ready to pay a vendor, from the **Payment Journal** page you can export a file with the payment information from the journal lines.</span></span> <span data-ttu-id="8d05c-120">Derefter kan du overføre filen til din elektroniske bank for at behandle pengeoverførslerne.</span><span class="sxs-lookup"><span data-stu-id="8d05c-120">You can then upload the file to your electronic bank to process the money transfers.</span></span>

<span data-ttu-id="8d05c-121">Hvis du ikke vil bogføre en betalingskladdelinje for en eksporteret betaling, for eksempel fordi du venter på, at banken skal bekræfte transaktionen, kan du bare slette kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="8d05c-121">If you do not want to post a payment journal line for an exported payment, for example because you are waiting for the bank to confirm the transaction, just delete the journal line.</span></span> <span data-ttu-id="8d05c-122">Senere, når du opretter en betalingskladdelinje for at betale det resterende beløb på fakturaen, kan du i feltet **Samlet eksporteret beløb** se, hvor meget af betalingsbeløbet der allerede er blevet eksporteret.</span><span class="sxs-lookup"><span data-stu-id="8d05c-122">Later, when you create a payment journal line to pay the remaining amount on the invoice, the **Total Exported Amount** field shows how much of the payment amount has already been exported.</span></span> <span data-ttu-id="8d05c-123">Du kan også finde detaljerede oplysninger om den eksporterede total ved at vælge knappen **Poster i kreditoverførselsjournal**.</span><span class="sxs-lookup"><span data-stu-id="8d05c-123">Also, you can find detailed information about the exported total by choosing the **Credit Transfer Reg. Entries** button.</span></span>

<span data-ttu-id="8d05c-124">Hvis du venter med at bogføre betalinger, til banken har bekræftet, at den har behandlet transaktionerne, er der to måder, du kan bruge for at undgå at komme til at eksportere betalinger af åbne dokumenter igen ved et uheld:</span><span class="sxs-lookup"><span data-stu-id="8d05c-124">If you wait to post payments until after your bank confirms that it has processed transactions, there are two ways to avoid accidentally re-exporting payments for open documents:</span></span>  

* <span data-ttu-id="8d05c-125">I en betalingskladde med foreslåede betalingslinjer skal du sortere på kolonnen **Eksporteret til betalingsfil** eller kolonnen **Samlet eksporteret beløb** og derefter slette betalingsforslag for åbne fakturaer for betalinger, der allerede er foretaget, og du ikke vil foretage betalinger af.</span><span class="sxs-lookup"><span data-stu-id="8d05c-125">In a payment journal with suggested payment lines, sort on either the **Exported to Payment File** or **Total Exported Amount** columns, and then delete payment suggestions for open invoices for which payments have already been made and you do not want to make payments for.</span></span>

    <span data-ttu-id="8d05c-126">**Bemærk** Det være nødvendigt at føje kolonnerne til listen.</span><span class="sxs-lookup"><span data-stu-id="8d05c-126">**Note** You might have to add these columns to the list.</span></span> <span data-ttu-id="8d05c-127">Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="8d05c-127">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  
* <span data-ttu-id="8d05c-128">Du kan også i batchjobbet **Lav kreditorbetalingsforslag**, hvor du angiver, hvilke betalinger der indsættes i betalingskladden, angive, at der ikke skal indsættes kladdelinjer for betalinger, der allerede er eksporteret, ved at markere afkrydsningsfeltet **Spring over eksporterede betalinger**.</span><span class="sxs-lookup"><span data-stu-id="8d05c-128">Alternatively, on the **Suggest Vendor Payments** batch job, where you specify the payments to include in the payment journal, you can specify not to insert journal lines for payments that have already been exported by choosing the **Skip Exported Payments** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="8d05c-129">Se også</span><span class="sxs-lookup"><span data-stu-id="8d05c-129">See Also</span></span>
[<span data-ttu-id="8d05c-130">Betalingsformer</span><span class="sxs-lookup"><span data-stu-id="8d05c-130">Payment Methods</span></span>](finance-payment-methods.md)  
[<span data-ttu-id="8d05c-131">Finans</span><span class="sxs-lookup"><span data-stu-id="8d05c-131">Finance</span></span>](finance.md)  
<span data-ttu-id="8d05c-132">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8d05c-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

