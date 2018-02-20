---
title: Udstede, udskrive og annullere checks | Microsoft Docs
description: "Beskriver, hvordan du udsteder checks ved hjælp af udbetalingskladden, udskriver checks og annullerer eller får vist checkposter i Finance and Operations, Business edition."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b3f8bece0d0d1de9a6fd17b84df73d466ccdf403
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="work-with-checks"></a><span data-ttu-id="67b15-103">Arbejde med checks</span><span class="sxs-lookup"><span data-stu-id="67b15-103">Work With Checks</span></span>
<span data-ttu-id="67b15-104">Du kan udstede elektroniske og manuelle check [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="67b15-104">You can issue electronic and manual checks in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="67b15-105">Udbetalingskladden bruges i begge tilfælde, når der udstedes checks til leverandører/kreditorer.</span><span class="sxs-lookup"><span data-stu-id="67b15-105">Both methods use the payment journal to issue checks to vendors.</span></span> <span data-ttu-id="67b15-106">Du kan også annullere checks og se checkposter.</span><span class="sxs-lookup"><span data-stu-id="67b15-106">You can also void checks and view check ledger entries.</span></span>

<span data-ttu-id="67b15-107">Under proceduren til udstedelse af checks foreslås der betalinger, der oprettes poster, og der udskrives computerchecks.</span><span class="sxs-lookup"><span data-stu-id="67b15-107">The process of issuing checks suggests payments, creates ledger entries, and prints the computer checks.</span></span>

> [!NOTE]  
>   <span data-ttu-id="67b15-108">Du kan kontrollere, at din bank kun afregner validerede checks og beløb, ved at sende banken en fil, der indeholder kreditor- check- og betalingsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="67b15-108">To make sure that your bank only clears validated checks and amounts, you can send them a file that contains vendor, check, and payment information.</span></span> <span data-ttu-id="67b15-109">Du kan finde flere oplysninger under [Eksportere en Positive Pay-fil](finance-how-positive-pay.md).</span><span class="sxs-lookup"><span data-stu-id="67b15-109">For more information, see [Export a Positive Pay file](finance-how-positive-pay.md).</span></span>

<span data-ttu-id="67b15-110">Printeren skal være konfigureret korrekt med checkformater, og du skal definere hvilket checklayout, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="67b15-110">Your printer must be correctly set up with the check forms, and you must define which check layout to use.</span></span> <span data-ttu-id="67b15-111">Du kan finde flere oplysninger under [Definere checklayouts](finance-how-define-check-layouts.md)</span><span class="sxs-lookup"><span data-stu-id="67b15-111">For more information, see [Define Check Layouts](finance-how-define-check-layouts.md)</span></span>

## <a name="to-issue-checks"></a><span data-ttu-id="67b15-112">Sådan udsteder du checks</span><span class="sxs-lookup"><span data-stu-id="67b15-112">To issue checks</span></span>
1. <span data-ttu-id="67b15-113">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Udbetalingskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="67b15-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="67b15-114">Udfyld kladden med relevante betalinger, f.eks. ved hjælp af funktionen Lav kreditorbetalingsforslag.</span><span class="sxs-lookup"><span data-stu-id="67b15-114">Fill in the journal with relevant payments, for example by using the Suggest Vendor Payments function.</span></span> <span data-ttu-id="67b15-115">Du kan finde flere oplysninger i [Lave kreditorbetalingsforslag](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="67b15-115">For more information, see [Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>
3. <span data-ttu-id="67b15-116">I feltet **Bankbetalingstype** på kladdelinjer til betaling, du vil foretage med check, skal du vælge en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="67b15-116">In the **Bank Payment Type** field on journal lines for payment that you want to make with checks, select one of the following options:</span></span>

   * <span data-ttu-id="67b15-117">**Computercheck**: Vælg denne mulighed, hvis du vil udskrive en check på beløbet fra udbetalingskladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="67b15-117">**Computer Check**: Select this option if you want to print a check for the amount on the payment journal line.</span></span> <span data-ttu-id="67b15-118">Du skal udskrive checkene, før du kan bogføre kladdelinjerne.</span><span class="sxs-lookup"><span data-stu-id="67b15-118">You must print the checks before you can post the journal lines.</span></span> <span data-ttu-id="67b15-119">Du kan kun vælge **Computercheck**, hvis **Modkontotype** eller **Kontotype** er **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="67b15-119">You can only select **Computer Check** if the **Bal. Account Type** or the **Account Type** is **Bank Account**.</span></span>
   * <span data-ttu-id="67b15-120">**Manuel check**: Vælg denne mulighed, hvis du har oprettet en check manuelt og vil oprette en tilsvarende checkpost på beløbet.</span><span class="sxs-lookup"><span data-stu-id="67b15-120">**Manual Check**: Select this option if you have created a check manually and want to create a corresponding check ledger entry for this amount.</span></span> <span data-ttu-id="67b15-121">Du kan ikke udskrive check fra [!INCLUDE[d365fin](includes/d365fin_md.md)] med denne indstilling.</span><span class="sxs-lookup"><span data-stu-id="67b15-121">By using this option, you cannot print checks from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="67b15-122">Du kan kun vælge **Manuel check**, hvis **Modkontotype** eller **Kontotype** er **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="67b15-122">You can only select **Manual Check** if the **Bal. Account Type** or the **Account Type** is **Bank Account**.</span></span>

     > [!NOTE]  
>   <span data-ttu-id="67b15-123">Du skal udskrive computerchecks, før du bogfører de relaterede kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="67b15-123">You must print computer checks before you post the related journal lines.</span></span>
4. <span data-ttu-id="67b15-124">I tilfælde af computercheck skal du vælge **Udskriv check**.</span><span class="sxs-lookup"><span data-stu-id="67b15-124">In case of computer checks, choose **Print Check**.</span></span>
5. <span data-ttu-id="67b15-125">I vinduet **Check** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="67b15-125">In the **Check** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. <span data-ttu-id="67b15-126">Vælg knappen **Udskriv**.</span><span class="sxs-lookup"><span data-stu-id="67b15-126">Choose the **Print** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="67b15-127">Hvis du vil udskrive check i mere end én valuta fra forskellige bankkonti, skal du udføre kørslen **Udskriv check** separat for hver valuta og angive den korrekte bankkonto.</span><span class="sxs-lookup"><span data-stu-id="67b15-127">If you want to print checks in more than one currency from different bank accounts, you must run the **Print Check** batch job separately for each currency and specify the appropriate bank account.</span></span>

## <a name="to-cancel-printed-checks-that-are-not-posted"></a><span data-ttu-id="67b15-128">Sådan annulleres udskrevne checks, der ikke er blevet bogført</span><span class="sxs-lookup"><span data-stu-id="67b15-128">To cancel printed checks that are not posted</span></span>
<span data-ttu-id="67b15-129">Du kan annullere ikke-bogførte checks, når de er blevet udskrevet, ved hjælp af handlingen **Annuller check** i vinduet **Udbetalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="67b15-129">You can cancel non-posted checks after they have been printed by using the **Void Check** action in the **Payment Journal** window.</span></span>

1. <span data-ttu-id="67b15-130">I vinduet **Udbetalingskladde** skal du vælge **Annuller Check**, og vælg derefter hvilke checks der skal annulleres.</span><span class="sxs-lookup"><span data-stu-id="67b15-130">In the **Payment Journal** window, choose the **Void Check**, and then choose which checks to cancel.</span></span>

## <a name="to-void-checks"></a><span data-ttu-id="67b15-131">Sådan annulleres checks</span><span class="sxs-lookup"><span data-stu-id="67b15-131">To void checks</span></span>
<span data-ttu-id="67b15-132">Når checkbetalingen er blevet bogført, kan du kun annullere checks fra de resulterende bankposter.</span><span class="sxs-lookup"><span data-stu-id="67b15-132">When check payment have been posted, you can only cancel (void) checks from the resulting bank ledger entries.</span></span>

1. <span data-ttu-id="67b15-133">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bankkonti**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="67b15-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="67b15-134">Vælg den relevante bankkonto, vælg handlingen **Rediger**, og vælg derefter handlingen **Checkposter**.</span><span class="sxs-lookup"><span data-stu-id="67b15-134">Select the relevant bank account, choose the **Edit** action, and then choose the **Check Ledger Entries** action.</span></span>
3. <span data-ttu-id="67b15-135">I vinduet **Checkposter** skal du vælge handlingen **Annuller check**.</span><span class="sxs-lookup"><span data-stu-id="67b15-135">In the **Check Ledger Entries** window, choose the **Void Check** action.</span></span>
4. <span data-ttu-id="67b15-136">Markér afkrydsningsfeltet **Kun annulleringskontrol**.</span><span class="sxs-lookup"><span data-stu-id="67b15-136">Select the **Void Check Only** check box.</span></span>
5. <span data-ttu-id="67b15-137">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="67b15-137">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="67b15-138">Se også</span><span class="sxs-lookup"><span data-stu-id="67b15-138">See Also</span></span>
[<span data-ttu-id="67b15-139">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="67b15-139">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="67b15-140">Konfigurere banktransaktioner</span><span class="sxs-lookup"><span data-stu-id="67b15-140">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="67b15-141">Eksportere en Positive Pay-fil</span><span class="sxs-lookup"><span data-stu-id="67b15-141">Export a Positive Pay file</span></span>](finance-how-positive-pay.md)  
<span data-ttu-id="67b15-142">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="67b15-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

