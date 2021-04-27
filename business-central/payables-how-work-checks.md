---
title: Udstede, udskrive og annullere checks | Microsoft Docs
description: Beskriver, hvordan du udsteder checks ved hjælp af udbetalingskladden, udskriver checks og annullerer eller får vist checkposter i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 6d2f204daefe5ed9473d64592d67e3c4cf026bce
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775086"
---
# <a name="make-check-payments"></a><span data-ttu-id="08cb7-103">Foretage betalinger med check</span><span class="sxs-lookup"><span data-stu-id="08cb7-103">Make Check Payments</span></span>

<span data-ttu-id="08cb7-104">Du kan udstede elektroniske og manuelle check [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="08cb7-104">You can issue electronic and manual checks in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="08cb7-105">Udbetalingskladden bruges i begge tilfælde, når der udstedes checks til leverandører/kreditorer.</span><span class="sxs-lookup"><span data-stu-id="08cb7-105">Both methods use the payment journal to issue checks to vendors.</span></span> <span data-ttu-id="08cb7-106">Du kan også annullere checks og se checkposter.</span><span class="sxs-lookup"><span data-stu-id="08cb7-106">You can also void checks and view check ledger entries.</span></span>

<span data-ttu-id="08cb7-107">Følgende procedure viser, hvordan du kan betale en kreditor med en computercheck ved at udligne betalingen til den relevante kreditorfaktura, udskrive checken og derefter bogføre betalingen som betalt.</span><span class="sxs-lookup"><span data-stu-id="08cb7-107">The following procedure shows how to pay a vendor with a computer checks by applying the payment to the relevant vendor invoice, printing the check, and then posting the payment as paid.</span></span> <span data-ttu-id="08cb7-108">Dette resulterer i positive kreditorposter, udlignet til negative bankposter og fysiske checks til behandling i banken.</span><span class="sxs-lookup"><span data-stu-id="08cb7-108">This results in positive vendor ledger entries, applied to negative bank ledger entries, and physical checks for processing in the bank.</span></span>

<span data-ttu-id="08cb7-109">Du kan betale med to checktyper.</span><span class="sxs-lookup"><span data-stu-id="08cb7-109">You can pay with two types of checks.</span></span> <span data-ttu-id="08cb7-110">Ved begge typer skal feltet **Modkontotype** eller **Kontotype** indeholde **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="08cb7-110">For both types, the **Bal. Account Type** or the **Account Type** field must contain **Bank Account**.</span></span>

- <span data-ttu-id="08cb7-111">**Computercheck**: Vælg denne mulighed, hvis du vil udskrive en check på beløbet fra udbetalingskladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="08cb7-111">**Computer Check**: Select this option if you want to print a check for the amount on the payment journal line.</span></span> <span data-ttu-id="08cb7-112">Du skal udskrive checkene, før du kan bogføre kladdelinjerne.</span><span class="sxs-lookup"><span data-stu-id="08cb7-112">You must print the checks before you can post the journal lines.</span></span>
- <span data-ttu-id="08cb7-113">**Manuel check**: Vælg denne mulighed, hvis du har oprettet en check manuelt og vil oprette en tilsvarende checkpost på beløbet.</span><span class="sxs-lookup"><span data-stu-id="08cb7-113">**Manual Check**: Select this option if you have created a check manually and want to create a corresponding check ledger entry for this amount.</span></span> <span data-ttu-id="08cb7-114">Du kan ikke udskrive checken med denne indstilling.</span><span class="sxs-lookup"><span data-stu-id="08cb7-114">By using this option, you cannot print the check.</span></span>

> [!NOTE]  
> <span data-ttu-id="08cb7-115">Du kan kontrollere, at din bank kun afregner validerede checks og beløb, ved at sende banken en fil, der indeholder kreditor- check- og betalingsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="08cb7-115">To make sure that your bank only clears validated checks and amounts, you can send them a file that contains vendor, check, and payment information.</span></span> <span data-ttu-id="08cb7-116">Du kan finde flere oplysninger i [Eksportere en Positive Pay-fil](finance-how-positive-pay.md).</span><span class="sxs-lookup"><span data-stu-id="08cb7-116">For more information, see [Export a Positive Pay file](finance-how-positive-pay.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08cb7-117">Printeren skal være konfigureret korrekt med checkformater, og du skal definere hvilket checklayout, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="08cb7-117">Your printer must be correctly set up with the check forms, and you must define which check layout to use.</span></span> <span data-ttu-id="08cb7-118">Du kan finde flere oplysninger i [Vælge et checklayout](finance-how-define-check-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="08cb7-118">For more information, see [Select a Check Layout](finance-how-define-check-layouts.md).</span></span> <span data-ttu-id="08cb7-119">Du kan også sende checken som PDF-fil, f.eks.</span><span class="sxs-lookup"><span data-stu-id="08cb7-119">Alternatively, you can send the check as a PDF file, for example.</span></span>  

<span data-ttu-id="08cb7-120">Du kan udskrive op til 10 fakturaer på en side til en checktalon.</span><span class="sxs-lookup"><span data-stu-id="08cb7-120">You can print up to 10 invoices on a page for a check stub.</span></span> <span data-ttu-id="08cb7-121">Hvis en check skal gælde for mere end 10 fakturaer, annullere vi checken på første side, når du udskriver talonen, og skriver ordet ANNULLERET på checken.</span><span class="sxs-lookup"><span data-stu-id="08cb7-121">If a check applies to more than 10 invoices, when you print the stub we void the check on the first page and print the word VOID on the check.</span></span> <span data-ttu-id="08cb7-122">Vi udskriver derefter resten af fakturaerne og det samlede checkbeløb på den anden side.</span><span class="sxs-lookup"><span data-stu-id="08cb7-122">We then print the remainder of the invoices and the total check amount on the second page.</span></span>

## <a name="to-pay-a-vendor-invoice-with-a-computer-check"></a><span data-ttu-id="08cb7-123">Sådan betales en kreditorfaktura med en computercheck</span><span class="sxs-lookup"><span data-stu-id="08cb7-123">To pay a vendor invoice with a computer check</span></span>
<span data-ttu-id="08cb7-124">I følgende fremgangsmåde vises, hvordan du betaler en kreditor med check.</span><span class="sxs-lookup"><span data-stu-id="08cb7-124">The following describes how to pay a vendor by check.</span></span> <span data-ttu-id="08cb7-125">Fremgangsmåden er den samme, hvis du vil refundere en debitor med check.</span><span class="sxs-lookup"><span data-stu-id="08cb7-125">The steps are similar to refund a customer by check.</span></span>

1. <span data-ttu-id="08cb7-126">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Udbetalingskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="08cb7-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="08cb7-127">Udfyld betalingskladdelinjerne.</span><span class="sxs-lookup"><span data-stu-id="08cb7-127">Fill in the payment journal lines.</span></span> <span data-ttu-id="08cb7-128">Du kan finde flere oplysninger i [Registrere betalinger og refusioner](payables-how-post-payments-refunds.md).</span><span class="sxs-lookup"><span data-stu-id="08cb7-128">For more information, see [Record Payments and Refunds](payables-how-post-payments-refunds.md).</span></span>
3. <span data-ttu-id="08cb7-129">I feltet **Betalingsformkode** skal du vælge **Check**.</span><span class="sxs-lookup"><span data-stu-id="08cb7-129">In the **Payment Method Code** field, select **Check**.</span></span>
4. <span data-ttu-id="08cb7-130">I feltet **Bankbetalingstype** skal du vælge **Computercheck**.</span><span class="sxs-lookup"><span data-stu-id="08cb7-130">In the **Bank Payment Type** field, select **Computer Check**.</span></span>
5. <span data-ttu-id="08cb7-131">Vælg handlingen **Udskriv check**.</span><span class="sxs-lookup"><span data-stu-id="08cb7-131">Choose the **Print Check** action.</span></span>
6. <span data-ttu-id="08cb7-132">På siden **Check** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="08cb7-132">On the **Check** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. <span data-ttu-id="08cb7-133">Hvis printeren er indstillet til at udskrive checks, skal du vælge knappen **Udskriv**.</span><span class="sxs-lookup"><span data-stu-id="08cb7-133">If your printer is set up to print checks, choose the **Print** button.</span></span> <span data-ttu-id="08cb7-134">Vælg ellers knappen **Send til**, vælg indstillingen **PDF-dokument**, vælg knappen **OK**, og udskriv derefter PDF-dokumentet.</span><span class="sxs-lookup"><span data-stu-id="08cb7-134">Otherwise, choose the **Send to** button, select the **PDF Document** option, choose the **OK** button, and then print the PDF document.</span></span>

    <span data-ttu-id="08cb7-135">Den fysiske check kan nu sendes til ekspedition hos leverandører.</span><span class="sxs-lookup"><span data-stu-id="08cb7-135">The physical checks can now be sent to the vendors for processing.</span></span> <span data-ttu-id="08cb7-136">Fortsæt med at bogføre betalingen som udlignet til leverandøren og dermed betalt i systemet.</span><span class="sxs-lookup"><span data-stu-id="08cb7-136">Proceed to post the payment as applied to the vendor and thereby paid in the system.</span></span>
8. <span data-ttu-id="08cb7-137">Vælg handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="08cb7-137">Choose the **Post** action.</span></span>

<span data-ttu-id="08cb7-138">Der oprettes helt udlignede kreditorposter og bankposter.</span><span class="sxs-lookup"><span data-stu-id="08cb7-138">Fully applied vendor ledger entries and bank ledger entries are created.</span></span>

> [!NOTE]  
> <span data-ttu-id="08cb7-139">Hvis du vil udskrive og betale checks i mere end én valuta fra forskellige bankkonti, skal du udføre kørslen **Udskriv check** separat for hver valuta og angive den korrekte bankkonto.</span><span class="sxs-lookup"><span data-stu-id="08cb7-139">If you want to print and pay checks in more than one currency from different bank accounts, you must run the **Print Check** batch job separately for each currency and specify the appropriate bank account.</span></span>

## <a name="to-cancel-printed-checks-that-are-not-posted"></a><span data-ttu-id="08cb7-140">Sådan annulleres udskrevne checks, der ikke er blevet bogført</span><span class="sxs-lookup"><span data-stu-id="08cb7-140">To cancel printed checks that are not posted</span></span>
<span data-ttu-id="08cb7-141">Du kan annullere ikke-bogførte checks, når de er blevet udskrevet, ved hjælp af handlingen **Annuller check** på siden **Udbetalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="08cb7-141">You can cancel non-posted checks after they have been printed by using the **Void Check** action on the **Payment Journal** page.</span></span>

1. <span data-ttu-id="08cb7-142">På siden **Udbetalingskladde** skal du vælge **Annuller Check**, og vælg derefter hvilke checks der skal annulleres.</span><span class="sxs-lookup"><span data-stu-id="08cb7-142">On the **Payment Journal** page, choose the **Void Check**, and then choose which checks to cancel.</span></span>

## <a name="to-void-checks"></a><span data-ttu-id="08cb7-143">Sådan annulleres checks</span><span class="sxs-lookup"><span data-stu-id="08cb7-143">To void checks</span></span>

<span data-ttu-id="08cb7-144">Når checkbetalingen er blevet bogført, kan du kun annullere checks fra de resulterende bankposter.</span><span class="sxs-lookup"><span data-stu-id="08cb7-144">When check payment have been posted, you can only cancel (void) checks from the resulting bank ledger entries.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08cb7-145">Hvis checken er udlignet med en faktura, skal du fjerne markeringen først, så fakturaen kan tilbagebetales, og checken kan annulleres.</span><span class="sxs-lookup"><span data-stu-id="08cb7-145">If the check is applied to an invoice, unapply the check first so that the invoice can be repaid, and then void the check.</span></span> <span data-ttu-id="08cb7-146">Hvis checken er udskrevet og ikke har betalt en faktura, så vælg **Kun annulleringskontrol** som beskrevet i dette afsnit.</span><span class="sxs-lookup"><span data-stu-id="08cb7-146">If the check was printed and did not pay an invoice, then choose **Void Check Only** as described in this section.</span></span>

1. <span data-ttu-id="08cb7-147">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bankkonti**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="08cb7-147">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="08cb7-148">Vælg den relevante bankkonto, vælg handlingen **Rediger**, og vælg derefter handlingen **Checkposter**.</span><span class="sxs-lookup"><span data-stu-id="08cb7-148">Select the relevant bank account, choose the **Edit** action, and then choose the **Check Ledger Entries** action.</span></span>
3. <span data-ttu-id="08cb7-149">På siden **Checkposter** skal du vælge handlingen **Annuller check**.</span><span class="sxs-lookup"><span data-stu-id="08cb7-149">On the **Check Ledger Entries** page, choose the **Void Check** action.</span></span>
4. <span data-ttu-id="08cb7-150">Markér afkrydsningsfeltet **Kun annulleringskontrol**.</span><span class="sxs-lookup"><span data-stu-id="08cb7-150">Select the **Void Check Only** check box.</span></span>
5. <span data-ttu-id="08cb7-151">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="08cb7-151">Choose the **OK** button.</span></span>

## <a name="to-view-a-summary-of-posted-checks"></a><span data-ttu-id="08cb7-152">Sådan får du vist en oversigt over bogførte checks</span><span class="sxs-lookup"><span data-stu-id="08cb7-152">To view a summary of posted checks</span></span>
<span data-ttu-id="08cb7-153">Hvis du vil gennemse bogførte checks, for eksempel for at kontrollere flere checks, der er betalt til én kreditor, kan du bruge rapporten **Bankkonto - checkoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="08cb7-153">If you want to review posted checks, for example to verify multiple checks paid to one vendor, you can use the **Bank Account - Check Details** report.</span></span>
1. <span data-ttu-id="08cb7-154">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bankkonto - checkoplysninger**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="08cb7-154">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Account - Check Details**, and then choose the related link.</span></span>
2. <span data-ttu-id="08cb7-155">Angiv filtre som relevante, og vælg derefter knappen **Eksempel**.</span><span class="sxs-lookup"><span data-stu-id="08cb7-155">Set filters as relevant, and then choose the **Preview** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="08cb7-156">Se også</span><span class="sxs-lookup"><span data-stu-id="08cb7-156">See Also</span></span>
[<span data-ttu-id="08cb7-157">Foretage betaling</span><span class="sxs-lookup"><span data-stu-id="08cb7-157">Making Payments</span></span>](payables-make-payments.md)  
[<span data-ttu-id="08cb7-158">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="08cb7-158">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="08cb7-159">Konfigurere banktransaktioner</span><span class="sxs-lookup"><span data-stu-id="08cb7-159">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="08cb7-160">Eksportere en Positive Pay-fil</span><span class="sxs-lookup"><span data-stu-id="08cb7-160">Export a Positive Pay file</span></span>](finance-how-positive-pay.md)  
<span data-ttu-id="08cb7-161">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="08cb7-161">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]