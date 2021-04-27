---
title: Fortryde en postering ved at bogføre en tilbageføringspost | Microsoft Docs
description: Hvis du har oprettet en forkert bogføring i finanskladden, kan du bruge funktionen Tilbagefør transaktion til at fortryde bogføringen med et korrekt revisionsspor.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: cdbf4b682b4ad99524ea0aace9a123283668fb43
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779093"
---
# <a name="reverse-journal-postings-and-undo-receiptsshipments"></a><span data-ttu-id="c2124-103">Tilbageføre kladdeposteringer og annullere modtagelser/leverancer</span><span class="sxs-lookup"><span data-stu-id="c2124-103">Reverse Journal Postings and Undo Receipts/Shipments</span></span>
<span data-ttu-id="c2124-104">Hvis du vil tilbageføre en fejlpostering i en kladde, skal du vælge posten og oprette en modpost (poster, der er identiske med den originale post, men med modsat fortegn i beløbsfeltet) med det samme bilagsnummer og den samme bogføringsdato som den oprindelige post.</span><span class="sxs-lookup"><span data-stu-id="c2124-104">To undo an erroneous journal posting, you select the entry and create a reverse entry (entries identical to the original entry but with opposite sign in the amount field) with the same document number and posting date as the original entry.</span></span> <span data-ttu-id="c2124-105">Når du har tilbageført en post, skal du oprette den korrekte post.</span><span class="sxs-lookup"><span data-stu-id="c2124-105">After reversing an entry, you must make the correct entry.</span></span>

<span data-ttu-id="c2124-106">Du kan kun tilbageføre poster, der er bogført fra en finanskladdelinje.</span><span class="sxs-lookup"><span data-stu-id="c2124-106">You can only reverse entries that are posted from a general journal line.</span></span> <span data-ttu-id="c2124-107">En post kan kun tilbageføres én gang.</span><span class="sxs-lookup"><span data-stu-id="c2124-107">An entry can only be reversed once.</span></span>

<span data-ttu-id="c2124-108">Hvis du vil annullere bogføringen af en modtagelse eller leverance, før de bogføres som faktureret, kan du bruge funktionen **Fortryd** i det bogførte dokument.</span><span class="sxs-lookup"><span data-stu-id="c2124-108">To undo a receipt or shipment posting, before they are posted as invoiced, you can use the **Undo** function on the posted document.</span></span> <span data-ttu-id="c2124-109">Du kan annullere antal af typen **Vare** og **Ressource**.</span><span class="sxs-lookup"><span data-stu-id="c2124-109">You can undo quantities of type **Item** and **Resource**.</span></span>

<span data-ttu-id="c2124-110">Hvis du har oprettet en bogføring af et forkert negativt antal, som f.eks. en købsordre med det forkerte antal varer og bogført dem som modtaget, men ikke faktureret, kan du annullere bogføringen.</span><span class="sxs-lookup"><span data-stu-id="c2124-110">If you have made an incorrect negative quantity posting, such as a purchase order with the wrong number of items, and posted it as received but not invoiced, then you can undo the posting.</span></span>

<span data-ttu-id="c2124-111">Hvis du har oprettet en bogføring af et forkert positivt antal som f.eks. en salgsleverance eller købsreturvare med det forkerte antal varer og bogført dem som leveret, men ikke faktureret, kan du annullere bogføringen.</span><span class="sxs-lookup"><span data-stu-id="c2124-111">If you have made an incorrect positive quantity posting, such as a sales shipment or a purchase return shipment with the wrong number of items, and posted it as shipped but not invoiced, then you can undo the posting.</span></span>   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><span data-ttu-id="c2124-112">Sådan tilbageføres kladdepost på en finanspost</span><span class="sxs-lookup"><span data-stu-id="c2124-112">To reverse the journal posting of a general ledger entry</span></span>
<span data-ttu-id="c2124-113">Du kan tilbageføre poster fra alle **Poster**-sider:</span><span class="sxs-lookup"><span data-stu-id="c2124-113">You can reverse entries from all **Ledger Entries** pages.</span></span> <span data-ttu-id="c2124-114">Følgende procedure er baseret på siden **Finansposter**.</span><span class="sxs-lookup"><span data-stu-id="c2124-114">The following procedure is based on the **General Ledger Entries** page.</span></span>
1. <span data-ttu-id="c2124-115">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Finansposter**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c2124-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Ledger Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="c2124-116">Marker den post, du vil tilbageføre, og vælg derefter handlingen **Tilbagefør transaktion**.</span><span class="sxs-lookup"><span data-stu-id="c2124-116">Select the entry that you want to reverse, and then choose the **Reverse Transaction** action.</span></span> <span data-ttu-id="c2124-117">Bemærk, at den skal stamme fra en kladdepost.</span><span class="sxs-lookup"><span data-stu-id="c2124-117">Note that is must originate from a journal posting.</span></span>
3. <span data-ttu-id="c2124-118">Vælg handlingen **Tilbagefør** på siden **Tilbagefør transaktionsposter**.</span><span class="sxs-lookup"><span data-stu-id="c2124-118">On the **Reverse Transaction Entries** page, choose the **Reverse** action.</span></span>
4. <span data-ttu-id="c2124-119">Vælg knappen **Ja** i bekræftelsesmeddelelsen.</span><span class="sxs-lookup"><span data-stu-id="c2124-119">Choose the **Yes** button on the confirmation message.</span></span>

> [!NOTE]
> <span data-ttu-id="c2124-120">Du kan ikke tilbageføre poster, der er bogført med oplysninger fra en sag, eller som har realiserede gevinster og tab inden for samme transaktion.</span><span class="sxs-lookup"><span data-stu-id="c2124-120">You cannot reverse entries that have been posted with information from a job, or which have realized gains and losses within the same transaction.</span></span>

## <a name="to-post-a-negative-entry"></a><span data-ttu-id="c2124-121">Sådan bogføres en negativ post</span><span class="sxs-lookup"><span data-stu-id="c2124-121">To post a negative entry</span></span>  
<span data-ttu-id="c2124-122">Du kan bruge feltet **Rettelse** til at bogføre en negativ debet i stedet for kredit eller til at bogføre en negativ kredit i stedet for en debet på en konto.</span><span class="sxs-lookup"><span data-stu-id="c2124-122">You can use the **Correction** field to post a negative debit instead of a credit, or to post a negative credit instead of a debit on an account.</span></span> <span data-ttu-id="c2124-123">Dette felt kan ses som standard i alle kladder for at imødekomme lovgivningsmæssige krav.</span><span class="sxs-lookup"><span data-stu-id="c2124-123">To meet legal requirements, this field is visible by default in all journals.</span></span> <span data-ttu-id="c2124-124">Felterne **Debetbeløb** og **Kreditbeløb** indeholdet både den oprindelige post og den rettede post.</span><span class="sxs-lookup"><span data-stu-id="c2124-124">The **Debit Amount** and **Credit Amount** fields include both the original entry, and the corrected entry.</span></span> <span data-ttu-id="c2124-125">Disse felter har ingen indflydelse på kontosaldoen.</span><span class="sxs-lookup"><span data-stu-id="c2124-125">These fields have no effect on the account balance.</span></span>  

1.  <span data-ttu-id="c2124-126">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Finanskladder**, og vælg derefter det relaterede link</span><span class="sxs-lookup"><span data-stu-id="c2124-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link</span></span>  
2.  <span data-ttu-id="c2124-127">Vælg det krævede kladdenavn i feltet **Kladdenavn**.</span><span class="sxs-lookup"><span data-stu-id="c2124-127">In the **Batch Name** field, select the required batch name.</span></span>  
3.  <span data-ttu-id="c2124-128">Angiv oplysningerne i de relevante felter.</span><span class="sxs-lookup"><span data-stu-id="c2124-128">Enter information into the relevant fields.</span></span>  
4.  <span data-ttu-id="c2124-129">I den kladdelinje, som du vil aktivere for negative poster, skal du markere afkrydsningsfeltet **Rettelse**.</span><span class="sxs-lookup"><span data-stu-id="c2124-129">In the journal line that you want to activate for negative entries, select the **Correction** check box.</span></span>  
5.  <span data-ttu-id="c2124-130">Hvis du vil postere kladden, skal du vælge handlingen **Bogfør** og derefter vælge knappen **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c2124-130">To post the journal, choose the **Post** action, and then choose the **Yes** button.</span></span>

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a><span data-ttu-id="c2124-131">Sådan fortrydes et bogført antal på en bogført købsmodtagelse</span><span class="sxs-lookup"><span data-stu-id="c2124-131">To undo a quantity posting on a posted purchase receipt</span></span>  
<span data-ttu-id="c2124-132">Følgende beskriver, hvordan du kan fortryde en bogført modtagelse af vare eller ressourcer.</span><span class="sxs-lookup"><span data-stu-id="c2124-132">The following described how to undo a posted receipt of items or resources.</span></span> <span data-ttu-id="c2124-133">Fremgangsmåden er tilsvarende for bogførte leverancer.</span><span class="sxs-lookup"><span data-stu-id="c2124-133">The steps are similar for posted shipments.</span></span>

1.  <span data-ttu-id="c2124-134">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bogførte købsmodtagelser**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c2124-134">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Receipts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c2124-135">Åbn den bogført modtagelse, du vil fortryde.</span><span class="sxs-lookup"><span data-stu-id="c2124-135">Open the posted receipt that you want to undo.</span></span>  
3.  <span data-ttu-id="c2124-136">Vælg den eller de linjer, der skal fortrydes.</span><span class="sxs-lookup"><span data-stu-id="c2124-136">Select the line or lines that you want to undo.</span></span>  
4.  <span data-ttu-id="c2124-137">Vælg handlingen **Annuller modtagelse**.</span><span class="sxs-lookup"><span data-stu-id="c2124-137">Choose **Undo Receipt** action.</span></span>

<span data-ttu-id="c2124-138">Der indsættes en korrektionslinje under den valgte modtagelseslinje.</span><span class="sxs-lookup"><span data-stu-id="c2124-138">A corrective line is inserted under the selected receipt line.</span></span> <span data-ttu-id="c2124-139">Hvis mængden blev modtaget i en lagermodtagelse, indsættes der en korrektionslinje i den bogførte lagermodtagelse.</span><span class="sxs-lookup"><span data-stu-id="c2124-139">If the quantity was received in a warehouse receipt, then a corrective line is inserted on the posted warehouse receipt.</span></span>  

<span data-ttu-id="c2124-140">Felterne **Modtaget (antal)** og **Modt. antal (ufakt.)** på den relaterede købsordre , der er angivet til nul.</span><span class="sxs-lookup"><span data-stu-id="c2124-140">The **Quantity Received** and **Qty. Rcd. Not Invoiced** fields on the related purchase order are set to zero.</span></span>

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a><span data-ttu-id="c2124-141">Sådan fortryder du og derefter annullerer et bogført antal på en bogført returvareleverance</span><span class="sxs-lookup"><span data-stu-id="c2124-141">To undo and then redo a quantity posting on a posted return shipment</span></span>
<span data-ttu-id="c2124-142">Følgende beskriver, hvordan du kan fortryde en bogført returvareleverance af varer eller ressourcer og derefter bogføre købsreturvaren igen med et nyt antal.</span><span class="sxs-lookup"><span data-stu-id="c2124-142">The following describes how to undo a posted return shipment of items or resources and then repost the purchase return with a new quantity.</span></span> <span data-ttu-id="c2124-143">Fremgangsmåden er tilsvarende for bogførte returvaremodtagelser.</span><span class="sxs-lookup"><span data-stu-id="c2124-143">The steps are similar for posted return receipts.</span></span>

1.  <span data-ttu-id="c2124-144">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bogførte returvareleverancer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c2124-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Return Shipments**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c2124-145">Åbn den bogførte returvareleverance, du vil fortryde.</span><span class="sxs-lookup"><span data-stu-id="c2124-145">Open the posted return shipment that you want to undo.</span></span>
3. <span data-ttu-id="c2124-146">Vælg den eller de linjer, der skal fortrydes.</span><span class="sxs-lookup"><span data-stu-id="c2124-146">Select the line or lines you want to undo.</span></span>  

4.  <span data-ttu-id="c2124-147">Vælg handlingen **Annuller returvareleverance**.</span><span class="sxs-lookup"><span data-stu-id="c2124-147">Choose the **Undo Return Shipment** action.</span></span>  

    <span data-ttu-id="c2124-148">En rettelseslinje indsættes i det bogførte dokument, og felterne **Antal sendt retur** og **Afs. ret.vare - ikke fakt.** på returvareordren nulstilles.</span><span class="sxs-lookup"><span data-stu-id="c2124-148">A corrective line is inserted in the posted document, and the **Return Qty. Shipped** and **Return Shpd. Not Invd.** fields on the return order are set to zero.</span></span>  

    <span data-ttu-id="c2124-149">Gå nu tilbage til købsreturvareordren for at annullere Fortryd bogføring.</span><span class="sxs-lookup"><span data-stu-id="c2124-149">Now go back to the purchase return order to redo the posting.</span></span>  

5.  <span data-ttu-id="c2124-150">Notér tallet i feltet **Returvareordrenr.** på siden **Bogført returvareleverance**</span><span class="sxs-lookup"><span data-stu-id="c2124-150">On the **Posted Return Shipment** page, take a note of the number in the **Return Order No.**</span></span> <span data-ttu-id="c2124-151">.</span><span class="sxs-lookup"><span data-stu-id="c2124-151">field.</span></span>  
6.  <span data-ttu-id="c2124-152">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsreturvareordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c2124-152">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Return Orders**, and then select the related link.</span></span>  
7.  <span data-ttu-id="c2124-153">Åbn den pågældende returordre, og vælg derefter handlingen **Genåbn**.</span><span class="sxs-lookup"><span data-stu-id="c2124-153">Open the return order in question, and then choose the **Reopen** action.</span></span>  
8.  <span data-ttu-id="c2124-154">Ret antallet i feltet **Antal**, og bogfør købsreturvareordren igen.</span><span class="sxs-lookup"><span data-stu-id="c2124-154">Correct the entry in the **Quantity** field and post the purchase return order again.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c2124-155">Se også</span><span class="sxs-lookup"><span data-stu-id="c2124-155">See Also</span></span>
[<span data-ttu-id="c2124-156">Fortryde bogføring af montage</span><span class="sxs-lookup"><span data-stu-id="c2124-156">Undo Assembly Posting</span></span>](assembly-how-to-undo-assembly-posting.md)  
[<span data-ttu-id="c2124-157">Bogføre transaktioner direkte i finansposterne</span><span class="sxs-lookup"><span data-stu-id="c2124-157">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="c2124-158">Arbejde med finanskladder</span><span class="sxs-lookup"><span data-stu-id="c2124-158">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="c2124-159">Finans</span><span class="sxs-lookup"><span data-stu-id="c2124-159">Finance</span></span>](finance.md)  
<span data-ttu-id="c2124-160">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c2124-160">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]