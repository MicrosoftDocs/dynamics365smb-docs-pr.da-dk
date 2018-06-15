---
title: Udstede, udskrive og annullere checks | Microsoft Docs
description: "Beskriver, hvordan du udsteder checks ved hjælp af udbetalingskladden, udskriver checks og annullerer eller får vist checkposter i Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 04/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: db28ad9a4adb45514b1d1287d269d8daefe64865
ms.openlocfilehash: 39b48fbd34b29db56b39712fbd2cbf5dc91fefc6
ms.contentlocale: da-dk
ms.lasthandoff: 04/26/2018

---
# <a name="make-check-payments"></a><span data-ttu-id="2334d-103">Foretage betalinger med check</span><span class="sxs-lookup"><span data-stu-id="2334d-103">Make Check Payments</span></span>
<span data-ttu-id="2334d-104">Du kan udstede elektroniske og manuelle check [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2334d-104">You can issue electronic and manual checks in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="2334d-105">Udbetalingskladden bruges i begge tilfælde, når der udstedes checks til leverandører/kreditorer.</span><span class="sxs-lookup"><span data-stu-id="2334d-105">Both methods use the payment journal to issue checks to vendors.</span></span> <span data-ttu-id="2334d-106">Du kan også annullere checks og se checkposter.</span><span class="sxs-lookup"><span data-stu-id="2334d-106">You can also void checks and view check ledger entries.</span></span>

<span data-ttu-id="2334d-107">Følgende procedure viser, hvordan du kan betale en kreditor med en computercheck ved at udligne betalingen til den relevante kreditorfaktura, udskrive checken og derefter bogføre betalingen som betalt.</span><span class="sxs-lookup"><span data-stu-id="2334d-107">The following procedure shows how to pay a vendor with a computer checks by applying the payment to the relevant vendor invoice, printing the check, and then posting the payment as paid.</span></span> <span data-ttu-id="2334d-108">Dette resulterer i positive kreditorposter, udlignet til negative bankposter og fysiske checks til behandling i banken.</span><span class="sxs-lookup"><span data-stu-id="2334d-108">This results in positive vendor ledger entries, applied to negative bank ledger entries, and physical checks for processing in the bank.</span></span>

<span data-ttu-id="2334d-109">Du kan betale med to checktyper.</span><span class="sxs-lookup"><span data-stu-id="2334d-109">You can pay with two types of checks.</span></span> <span data-ttu-id="2334d-110">Ved begge typer skal feltet **Modkontotype** eller **Kontotype** indeholde **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="2334d-110">For both types, the **Bal. Account Type** or the **Account Type** field must contain **Bank Account**.</span></span>

- <span data-ttu-id="2334d-111">**Computercheck**: Vælg denne mulighed, hvis du vil udskrive en check på beløbet fra udbetalingskladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="2334d-111">**Computer Check**: Select this option if you want to print a check for the amount on the payment journal line.</span></span> <span data-ttu-id="2334d-112">Du skal udskrive checkene, før du kan bogføre kladdelinjerne.</span><span class="sxs-lookup"><span data-stu-id="2334d-112">You must print the checks before you can post the journal lines.</span></span> <span data-ttu-id="2334d-113">Du kan kun vælge **Computercheck**, hvis</span><span class="sxs-lookup"><span data-stu-id="2334d-113">You can only select **Computer Check** if</span></span>
- <span data-ttu-id="2334d-114">**Manuel check**: Vælg denne mulighed, hvis du har oprettet en check manuelt og vil oprette en tilsvarende checkpost på beløbet.</span><span class="sxs-lookup"><span data-stu-id="2334d-114">**Manual Check**: Select this option if you have created a check manually and want to create a corresponding check ledger entry for this amount.</span></span> <span data-ttu-id="2334d-115">Du kan ikke udskrive checken med denne indstilling.</span><span class="sxs-lookup"><span data-stu-id="2334d-115">By using this option, you cannot print the check.</span></span>

> [!NOTE]  
> <span data-ttu-id="2334d-116">Du kan kontrollere, at din bank kun afregner validerede checks og beløb, ved at sende banken en fil, der indeholder kreditor- check- og betalingsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="2334d-116">To make sure that your bank only clears validated checks and amounts, you can send them a file that contains vendor, check, and payment information.</span></span> <span data-ttu-id="2334d-117">Du kan finde flere oplysninger under [Eksportere en Positive Pay-fil](finance-how-positive-pay.md).</span><span class="sxs-lookup"><span data-stu-id="2334d-117">For more information, see [Export a Positive Pay file](finance-how-positive-pay.md).</span></span>

<span data-ttu-id="2334d-118">Printeren skal være konfigureret korrekt med checkformater, og du skal definere hvilket checklayout, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="2334d-118">Your printer must be correctly set up with the check forms, and you must define which check layout to use.</span></span> <span data-ttu-id="2334d-119">Du kan finde flere oplysninger under [Definere checklayouts](finance-how-define-check-layouts.md)</span><span class="sxs-lookup"><span data-stu-id="2334d-119">For more information, see [Define Check Layouts](finance-how-define-check-layouts.md)</span></span>

## <a name="to-pay-a-vendor-invoice-with-a-computer-check"></a><span data-ttu-id="2334d-120">Sådan betales en kreditorfaktura med en computercheck</span><span class="sxs-lookup"><span data-stu-id="2334d-120">To pay a vendor invoice with a computer check</span></span>
<span data-ttu-id="2334d-121">I følgende fremgangsmåde vises, hvordan du betaler en kreditor med check.</span><span class="sxs-lookup"><span data-stu-id="2334d-121">The following describes how to pay a vendor by check.</span></span> <span data-ttu-id="2334d-122">Fremgangsmåden er den samme, hvis du vil refundere en debitor med check.</span><span class="sxs-lookup"><span data-stu-id="2334d-122">The steps are similar to refund a customer by check.</span></span>

1. <span data-ttu-id="2334d-123">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Udbetalingskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="2334d-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="2334d-124">Udfyld betalingskladdelinjerne.</span><span class="sxs-lookup"><span data-stu-id="2334d-124">Fill in the payment journal lines.</span></span> <span data-ttu-id="2334d-125">Du kan finde flere oplysninger i [Registrere betalinger og refusioner](payables-how-post-payments-refunds.md).</span><span class="sxs-lookup"><span data-stu-id="2334d-125">For more information, see [Record Payments and Refunds](payables-how-post-payments-refunds.md).</span></span>
3. <span data-ttu-id="2334d-126">I feltet **Betalingsformkode** skal du vælge **Check**.</span><span class="sxs-lookup"><span data-stu-id="2334d-126">In the **Payment Method Code** field, select **Check**.</span></span>
4. <span data-ttu-id="2334d-127">I feltet **Bankbetalingstype** skal du vælge **Computercheck**.</span><span class="sxs-lookup"><span data-stu-id="2334d-127">In the **Bank Payment Type** field, select **Computer Check**.</span></span>
5. <span data-ttu-id="2334d-128">Vælg handlingen **Udskriv check**.</span><span class="sxs-lookup"><span data-stu-id="2334d-128">Choose the **Print Check** action.</span></span>
6. <span data-ttu-id="2334d-129">I vinduet **Check** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="2334d-129">In the **Check** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. <span data-ttu-id="2334d-130">Vælg knappen **Send til**, vælg indstillingen **PDF-dokument**, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="2334d-130">Choose the **Send to** button, select the **PDF Document** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="2334d-131">Den fysiske check kan nu sendes til behandling i banken.</span><span class="sxs-lookup"><span data-stu-id="2334d-131">The physical checks can now be brought to the bank for processing.</span></span> <span data-ttu-id="2334d-132">Fortsæt med at bogføre betalingen som udlignet til leverandøren og dermed betalt i systemet.</span><span class="sxs-lookup"><span data-stu-id="2334d-132">Proceed to post the payment as applied to the vendor and thereby paid in the system.</span></span>
8. <span data-ttu-id="2334d-133">Vælg handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="2334d-133">Choose the **Post** action.</span></span>

<span data-ttu-id="2334d-134">Der oprettes helt udlignede kreditorposter og bankposter.</span><span class="sxs-lookup"><span data-stu-id="2334d-134">Fully applied vendor ledger entries and bank ledger entries are created.</span></span>

> [!NOTE]  
> <span data-ttu-id="2334d-135">Hvis du vil udskrive og betale checks i mere end én valuta fra forskellige bankkonti, skal du udføre kørslen **Udskriv check** separat for hver valuta og angive den korrekte bankkonto.</span><span class="sxs-lookup"><span data-stu-id="2334d-135">If you want to print and pay checks in more than one currency from different bank accounts, you must run the **Print Check** batch job separately for each currency and specify the appropriate bank account.</span></span>

## <a name="to-cancel-printed-checks-that-are-not-posted"></a><span data-ttu-id="2334d-136">Sådan annulleres udskrevne checks, der ikke er blevet bogført</span><span class="sxs-lookup"><span data-stu-id="2334d-136">To cancel printed checks that are not posted</span></span>
<span data-ttu-id="2334d-137">Du kan annullere ikke-bogførte checks, når de er blevet udskrevet, ved hjælp af handlingen **Annuller check** i vinduet **Udbetalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="2334d-137">You can cancel non-posted checks after they have been printed by using the **Void Check** action in the **Payment Journal** window.</span></span>

1. <span data-ttu-id="2334d-138">I vinduet **Udbetalingskladde** skal du vælge **Annuller Check**, og vælg derefter hvilke checks der skal annulleres.</span><span class="sxs-lookup"><span data-stu-id="2334d-138">In the **Payment Journal** window, choose the **Void Check**, and then choose which checks to cancel.</span></span>

## <a name="to-void-checks"></a><span data-ttu-id="2334d-139">Sådan annulleres checks</span><span class="sxs-lookup"><span data-stu-id="2334d-139">To void checks</span></span>
<span data-ttu-id="2334d-140">Når checkbetalingen er blevet bogført, kan du kun annullere checks fra de resulterende bankposter.</span><span class="sxs-lookup"><span data-stu-id="2334d-140">When check payment have been posted, you can only cancel (void) checks from the resulting bank ledger entries.</span></span>

1. <span data-ttu-id="2334d-141">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bankkonti**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="2334d-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="2334d-142">Vælg den relevante bankkonto, vælg handlingen **Rediger**, og vælg derefter handlingen **Checkposter**.</span><span class="sxs-lookup"><span data-stu-id="2334d-142">Select the relevant bank account, choose the **Edit** action, and then choose the **Check Ledger Entries** action.</span></span>
3. <span data-ttu-id="2334d-143">I vinduet **Checkposter** skal du vælge handlingen **Annuller check**.</span><span class="sxs-lookup"><span data-stu-id="2334d-143">In the **Check Ledger Entries** window, choose the **Void Check** action.</span></span>
4. <span data-ttu-id="2334d-144">Markér afkrydsningsfeltet **Kun annulleringskontrol**.</span><span class="sxs-lookup"><span data-stu-id="2334d-144">Select the **Void Check Only** check box.</span></span>
5. <span data-ttu-id="2334d-145">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="2334d-145">Choose the **OK** button.</span></span>

## <a name="to-view-a-summary-of-posted-checks"></a><span data-ttu-id="2334d-146">Sådan får du vist en oversigt over bogførte checks</span><span class="sxs-lookup"><span data-stu-id="2334d-146">To view a summary of posted checks</span></span>
<span data-ttu-id="2334d-147">Hvis du vil gennemse bogførte checks, for eksempel for at kontrollere flere checks, der er betalt til én kreditor, kan du bruge rapporten **Bankkonto - checkoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="2334d-147">If you want to review posted checks, for example to verify multiple checks paid to one vendor, you can use the **Bank Account - Check Details** report.</span></span>
1. <span data-ttu-id="2334d-148">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bankkonto - checkoplysninger**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="2334d-148">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Account - Check Details**, and then choose the related link.</span></span>
2. <span data-ttu-id="2334d-149">Angiv filtre som relevante, og vælg derefter knappen **Eksempel**.</span><span class="sxs-lookup"><span data-stu-id="2334d-149">Set filters as relevant, and then choose the **Preview** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="2334d-150">Se også</span><span class="sxs-lookup"><span data-stu-id="2334d-150">See Also</span></span>
[<span data-ttu-id="2334d-151">Foretage betaling</span><span class="sxs-lookup"><span data-stu-id="2334d-151">Making Payments</span></span>](payables-make-payments.md)  
[<span data-ttu-id="2334d-152">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="2334d-152">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="2334d-153">Konfigurere banktransaktioner</span><span class="sxs-lookup"><span data-stu-id="2334d-153">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="2334d-154">Eksportere en Positive Pay-fil</span><span class="sxs-lookup"><span data-stu-id="2334d-154">Export a Positive Pay file</span></span>](finance-how-positive-pay.md)  
<span data-ttu-id="2334d-155">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2334d-155">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

