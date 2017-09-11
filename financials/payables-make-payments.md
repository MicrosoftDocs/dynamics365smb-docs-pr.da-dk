---
title: Oversigt over opgaver til administration af betalinger til kreditorer | Microsoft Docs
description: "Beskrives opgaver til administration af betalinger til leverandører eller kreditorer, herunder bogføring af betalingslinjer og visning af en oversigt over den forfaldne saldo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d0b9020596484a8910db2f5720adfe159ad96fe7
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="make-payments"></a><span data-ttu-id="39633-103">Foretage indbetalinger</span><span class="sxs-lookup"><span data-stu-id="39633-103">Make Payments</span></span>
<span data-ttu-id="39633-104">Når du foretager betalinger til kreditorer, bogfører du relaterede de betalingslinjer i vinduet **Udbetalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="39633-104">When you make payments to vendors, you post the related payment lines in the **Payment Journal** window.</span></span> <span data-ttu-id="39633-105">Du kan bruge funktionen **Lav kreditorbetalingsforslag** for at finde betalinger, der er forfaldne.</span><span class="sxs-lookup"><span data-stu-id="39633-105">You can use the **Suggest Vendor Payments** function to find payments that are due.</span></span> <span data-ttu-id="39633-106">Du kan også bruge rapporten **Kreditor - forfaldsoversigt** til at få vist en oversigt over forfaldne betalinger.</span><span class="sxs-lookup"><span data-stu-id="39633-106">You can also use the **Vendor - Summary Aging** report to get an overview of due payments.</span></span>

<span data-ttu-id="39633-107">Fra betalingskladden kan du udskrive computercheck eller registrere, når der skrives check.</span><span class="sxs-lookup"><span data-stu-id="39633-107">From the payment journal, you can print computer checks or record when checks are written.</span></span> <span data-ttu-id="39633-108">Hvis du markerer **Computercheck** i feltet **Bankbetalingstype**, skal linjer, der repræsenterer checks udskrives, før udbetalingskladden kan bogføres.</span><span class="sxs-lookup"><span data-stu-id="39633-108">If you select **Computer Check** in the **Bank Payment Type** field, then any lines representing checks must be printed before the payment journal can be posted.</span></span>

<span data-ttu-id="39633-109">Når betalingerne er bogført, kan du eksportere dem til en bankfil for at overføre dem til behandling i din bank.</span><span class="sxs-lookup"><span data-stu-id="39633-109">When the payments are posted, you can export them to a bank file for upload to your bank for processing.</span></span>

<span data-ttu-id="39633-110">Efter at betalingerne er foretaget i din bank, skal du udligne dem til de relaterede åbne kreditorposter.</span><span class="sxs-lookup"><span data-stu-id="39633-110">After the payments are made at your bank, you must apply them to their related open vendor ledger entries.</span></span> <span data-ttu-id="39633-111">Du kan gøre det manuelt eller ved at importere en bankkontoudtogsfil og udligne betalingerne automatisk.</span><span class="sxs-lookup"><span data-stu-id="39633-111">You can do this manually or by importing a bank statement file and applying the payments automatically.</span></span> <span data-ttu-id="39633-112">Du kan finde flere oplysninger under [Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="39633-112">For more information, see [Apply Payments Automatically and Reconcile Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span>

<span data-ttu-id="39633-113">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="39633-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="39633-114">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="39633-114">To</span></span> | <span data-ttu-id="39633-115">Se</span><span class="sxs-lookup"><span data-stu-id="39633-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="39633-116">Brug en funktion til at foreslå kreditorbetalinger i overensstemmelse med de valgte kriterier, f.eks. forfaldsdato, ret til rabat og din likviditet.</span><span class="sxs-lookup"><span data-stu-id="39633-116">Use a function to suggest vendor payments according to selected criteria, such as due date, discount eligibility, and your liquidity.</span></span> |[<span data-ttu-id="39633-117">Fremgangsmåde: Lave kreditorbetalingsforslag</span><span class="sxs-lookup"><span data-stu-id="39633-117">How to: Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md) |
| <span data-ttu-id="39633-118">Udsted checks for betalinger enten som udskrifter eller som computercheck.</span><span class="sxs-lookup"><span data-stu-id="39633-118">Issue checks for payments, either as print-outs or as computer checks.</span></span> <span data-ttu-id="39633-119">Annullere checks før eller efter bogføringen.</span><span class="sxs-lookup"><span data-stu-id="39633-119">Void checks before or after posting.</span></span> |[<span data-ttu-id="39633-120">Fremgangsmåde: Arbejde med checks</span><span class="sxs-lookup"><span data-stu-id="39633-120">How to: Work with Checks</span></span>](payables-how-work-checks.md) |
| <span data-ttu-id="39633-121">Kontroller, at din bank kun afregner validerede checks og beløb, ved at sende banken en fil, der indeholder kreditor- check- og betalingsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="39633-121">Make sure that your bank only clears validated checks and amounts by sending them a file that contains vendor, check, and payment information.</span></span> |[<span data-ttu-id="39633-122">Fremgangsmåde: Eksportere en Positive Pay-fil</span><span class="sxs-lookup"><span data-stu-id="39633-122">How to: Export a Positive Pay file</span></span>](finance-how-positive-pay.md) |
|<span data-ttu-id="39633-123">Udlæs betalinger fra vinduet **Udbetalingskladde** til en bankfil, du overfører til din bank til behandling, herunder EFT (elektroniske pengeoverførsler) i Nordamerika.</span><span class="sxs-lookup"><span data-stu-id="39633-123">Export payments from the **Payment Journal** window to a bank file that you upload to your bank for processing, including EFT (electronic funds transfer) in North America.</span></span> |[<span data-ttu-id="39633-124">Fremgangsmåde: Eksportere betalinger til en bankfil</span><span class="sxs-lookup"><span data-stu-id="39633-124">How to: Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  

## <a name="see-also"></a><span data-ttu-id="39633-125">Se også</span><span class="sxs-lookup"><span data-stu-id="39633-125">See Also</span></span>
[<span data-ttu-id="39633-126">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="39633-126">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="39633-127">Køb</span><span class="sxs-lookup"><span data-stu-id="39633-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="39633-128">Administrere tilgodehavender</span><span class="sxs-lookup"><span data-stu-id="39633-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="39633-129">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="39633-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

