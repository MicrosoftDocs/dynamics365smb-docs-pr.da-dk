---
title: Fortryde en postering ved at bogføre en tilbageføringspost | Microsoft Docs
description: Hvis du har oprettet en forkert bogføring i finanskladden, kan du bruge funktionen Tilbagefør transaktion til at fortryde bogføringen med et korrekt revisionsspor.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: f2767fca96e1f3689fc4806d878381d02622f261
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243729"
---
# <a name="reverse-postings"></a><span data-ttu-id="1487e-103">Tilbageføre poster</span><span class="sxs-lookup"><span data-stu-id="1487e-103">Reverse Postings</span></span>
<span data-ttu-id="1487e-104">Hvis du vil tilbageføre en fejlpostering i en kladde, skal du vælge posten og oprette en modpost (poster, der er identiske med den originale post, men med modsat fortegn i beløbsfeltet) med det samme bilagsnummer og den samme bogføringsdato som den oprindelige post.</span><span class="sxs-lookup"><span data-stu-id="1487e-104">To undo an erroneous journal posting, you select the entry and create a reverse entry (entries identical to the original entry but with opposite sign in the amount field) with the same document number and posting date as the original entry.</span></span> <span data-ttu-id="1487e-105">Når du har tilbageført en post, skal du oprette den korrekte post.</span><span class="sxs-lookup"><span data-stu-id="1487e-105">After reversing an entry, you must make the correct entry.</span></span>

<span data-ttu-id="1487e-106">Du kan kun tilbageføre poster, der er bogført fra en finanskladdelinje.</span><span class="sxs-lookup"><span data-stu-id="1487e-106">You can only reverse entries that are posted from a general journal line.</span></span> <span data-ttu-id="1487e-107">En post kan kun tilbageføres én gang.</span><span class="sxs-lookup"><span data-stu-id="1487e-107">An entry can only be reversed once.</span></span>

<span data-ttu-id="1487e-108">Du kan finde flere oplysninger om bogføring fra en finanskladde i [Bogføre transaktioner direkte i finansposter](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="1487e-108">For more information about posting from a general journal, see [Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>

<span data-ttu-id="1487e-109">Hvis du har oprettet en bogføring af et forkert negativt antal, som f.eks. en købsordre med det forkerte antal varer og bogført dem som modtaget, men ikke faktureret, kan du annullere bogføringen.</span><span class="sxs-lookup"><span data-stu-id="1487e-109">If you have made an incorrect negative quantity posting, such as a purchase order with the wrong number of items and posted it as received but not invoiced, then you can undo the posting.</span></span>

<span data-ttu-id="1487e-110">Hvis du har oprettet en bogføring af et forkert positivt antal, som f.eks. en købsreturvareordre med det forkerte antal varer og bogført dem som leveret, men ikke faktureret, kan du annullere bogføringen.</span><span class="sxs-lookup"><span data-stu-id="1487e-110">If you have made an incorrect positive quantity posting, such as a purchase return order with the wrong number of items and posted it as shipped but not invoiced, then you can undo the posting.</span></span>   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><span data-ttu-id="1487e-111">Sådan tilbageføres kladdepost på en finanspost</span><span class="sxs-lookup"><span data-stu-id="1487e-111">To reverse the journal posting of a general ledger entry</span></span>
<span data-ttu-id="1487e-112">Du kan tilbageføre poster fra alle **Poster**-sider:</span><span class="sxs-lookup"><span data-stu-id="1487e-112">You can reverse entries from all **Ledger Entries** pages.</span></span> <span data-ttu-id="1487e-113">Følgende procedure er baseret på siden **Finansposter**.</span><span class="sxs-lookup"><span data-stu-id="1487e-113">The following procedure is based on the **General Ledger Entries** page.</span></span>
1. <span data-ttu-id="1487e-114">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Finansposter**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="1487e-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Ledger Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="1487e-115">Marker den post, du vil tilbageføre, og vælg derefter handlingen **Tilbagefør transaktion**.</span><span class="sxs-lookup"><span data-stu-id="1487e-115">Select the entry that you want to reverse, and then choose the **Reverse Transaction** action.</span></span> <span data-ttu-id="1487e-116">Bemærk, at den skal stamme fra en kladdepost.</span><span class="sxs-lookup"><span data-stu-id="1487e-116">Note that is must originate from a journal posting.</span></span>
3. <span data-ttu-id="1487e-117">På siden **Tilbagefør transaktionsposter** skal du vælge den relevante post og derefter vælge handlingen **Tilbagefør**.</span><span class="sxs-lookup"><span data-stu-id="1487e-117">On the **Reverse Transaction Entries** page, select the relevant entry, and then choose the **Reverse** action.</span></span>
4. <span data-ttu-id="1487e-118">Vælg knappen **Ja** i bekræftelsesmeddelelsen.</span><span class="sxs-lookup"><span data-stu-id="1487e-118">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a><span data-ttu-id="1487e-119">Sådan fortrydes et bogført antal på en bogført købsmodtagelse</span><span class="sxs-lookup"><span data-stu-id="1487e-119">To undo a quantity posting on a posted purchase receipt</span></span>  

1.  <span data-ttu-id="1487e-120">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bogførte købsmodtagelser**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="1487e-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Receipts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1487e-121">Åbn den bogført modtagelse, du vil fortryde.</span><span class="sxs-lookup"><span data-stu-id="1487e-121">Open the posted receipt that you want to undo.</span></span>  
3.  <span data-ttu-id="1487e-122">Vælg den eller de linjer, der skal fortrydes.</span><span class="sxs-lookup"><span data-stu-id="1487e-122">Select the line or lines that you want to undo.</span></span>  
4.  <span data-ttu-id="1487e-123">Vælg handlingen **Annuller modtagelse**.</span><span class="sxs-lookup"><span data-stu-id="1487e-123">Choose **Undo Receipt** action.</span></span>

    <span data-ttu-id="1487e-124">Der indsættes en korrektionslinje under den valgte modtagelseslinje.</span><span class="sxs-lookup"><span data-stu-id="1487e-124">A corrective line is inserted under the selected receipt line.</span></span>  

    <span data-ttu-id="1487e-125">Hvis mængden blev modtaget i en lagermodtagelse, indsættes der en korrektionslinje i den bogførte lagermodtagelse.</span><span class="sxs-lookup"><span data-stu-id="1487e-125">If the quantity was received in a warehouse receipt, then a corrective line is inserted in the posted warehouse receipt.</span></span>  

    <span data-ttu-id="1487e-126">Felterne **Modtaget (antal)** og **Modt. antal (ufakt.)** på den relaterede købsordre , der er angivet til nul.</span><span class="sxs-lookup"><span data-stu-id="1487e-126">The **Quantity Received** and **Qty. Rcd. Not Invoiced** fields on the related purchase order are set to zero.</span></span>

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a><span data-ttu-id="1487e-127">Sådan fortryder du og derefter annullerer et bogført antal på en bogført returvareleverance</span><span class="sxs-lookup"><span data-stu-id="1487e-127">To undo and then redo a quantity posting on a posted return shipment</span></span>

1.  <span data-ttu-id="1487e-128">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bogførte returvareleverancer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="1487e-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Return Shipments**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1487e-129">Åbn den bogførte returvareleverance, du vil fortryde.</span><span class="sxs-lookup"><span data-stu-id="1487e-129">Open the posted return shipment that you want to undo.</span></span>
3. <span data-ttu-id="1487e-130">Vælg den eller de linjer, der skal fortrydes.</span><span class="sxs-lookup"><span data-stu-id="1487e-130">Select the line or lines you want to undo.</span></span>  

4.  <span data-ttu-id="1487e-131">Vælg handlingen **Annuller returvareleverance**.</span><span class="sxs-lookup"><span data-stu-id="1487e-131">Choose the **Undo Return Shipment** action.</span></span>  

    <span data-ttu-id="1487e-132">En rettelseslinje indsættes i det bogførte dokument, og felterne **Antal sendt retur** og **Afs. ret.vare - ikke fakt.** på returvareordren nulstilles.</span><span class="sxs-lookup"><span data-stu-id="1487e-132">A corrective line is inserted in the posted document, and the **Return Qty. Shipped** and **Return Shpd. Not Invd.** fields on the return order are set to zero.</span></span>  

    <span data-ttu-id="1487e-133">Gå nu tilbage til købsreturvareordren for at annullere Fortryd bogføring.</span><span class="sxs-lookup"><span data-stu-id="1487e-133">Now go back to the purchase return order to redo the posting.</span></span>  

5.  <span data-ttu-id="1487e-134">Notér tallet i feltet **Returvareordrenr.** på siden **Bogført returvareleverance**</span><span class="sxs-lookup"><span data-stu-id="1487e-134">On the **Posted Return Shipment** page, take a note of the number in the **Return Order No.**</span></span> <span data-ttu-id="1487e-135">.</span><span class="sxs-lookup"><span data-stu-id="1487e-135">field.</span></span>  
6.  <span data-ttu-id="1487e-136">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsreturvareordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="1487e-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Return Orders**, and then select the related link.</span></span>  
7.  <span data-ttu-id="1487e-137">Åbn den pågældende returordre, og vælg derefter handlingen **Genåbn**.</span><span class="sxs-lookup"><span data-stu-id="1487e-137">Open the return order in question, and then choose the **Reopen** action.</span></span>  
8.  <span data-ttu-id="1487e-138">Ret antallet i feltet **Antal**, og bogfør købsreturvareordren igen.</span><span class="sxs-lookup"><span data-stu-id="1487e-138">Correct the entry in the **Quantity** field and post the purchase return order again.</span></span>  

## <a name="to-post-a-negative-entry"></a><span data-ttu-id="1487e-139">Sådan bogføres en negativ post</span><span class="sxs-lookup"><span data-stu-id="1487e-139">To post a negative entry</span></span>  
<span data-ttu-id="1487e-140">Du kan bruge feltet **Rettelse** til at bogføre en negativ debet i stedet for kredit eller til at bogføre en negativ kredit i stedet for en debet på en konto.</span><span class="sxs-lookup"><span data-stu-id="1487e-140">You can use the **Correction** field to post a negative debit instead of a credit, or to post a negative credit instead of a debit on an account.</span></span> <span data-ttu-id="1487e-141">Dette felt kan ses som standard i alle kladder for at imødekomme lovgivningsmæssige krav.</span><span class="sxs-lookup"><span data-stu-id="1487e-141">To meet legal requirements, this field is visible by default in all journals.</span></span> <span data-ttu-id="1487e-142">Felterne **Debetbeløb** og **Kreditbeløb** indeholdet både den oprindelige post og den rettede post.</span><span class="sxs-lookup"><span data-stu-id="1487e-142">The **Debit Amount** and **Credit Amount** fields include both the original entry, and the corrected entry.</span></span> <span data-ttu-id="1487e-143">Disse felter har ingen indflydelse på kontosaldoen.</span><span class="sxs-lookup"><span data-stu-id="1487e-143">These fields have no effect on the account balance.</span></span>  

1.  <span data-ttu-id="1487e-144">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Finanskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="1487e-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link</span></span>  
2.  <span data-ttu-id="1487e-145">Vælg det krævede kladdenavn i feltet **Kladdenavn**.</span><span class="sxs-lookup"><span data-stu-id="1487e-145">In the **Batch Name** field, select the required batch name.</span></span>  
3.  <span data-ttu-id="1487e-146">Angiv oplysningerne i de relevante felter.</span><span class="sxs-lookup"><span data-stu-id="1487e-146">Enter information into the relevant fields.</span></span>  
4.  <span data-ttu-id="1487e-147">I den kladdelinje, som du vil aktivere for negative poster, skal du markere afkrydsningsfeltet **Rettelse**.</span><span class="sxs-lookup"><span data-stu-id="1487e-147">In the journal line that you want to activate for negative entries, select the **Correction** check box.</span></span>  
5.  <span data-ttu-id="1487e-148">Hvis du vil postere kladden, skal du vælge handlingen **Bogfør** og derefter vælge knappen **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1487e-148">To post the journal, choose the **Post** action, and then choose the **Yes** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="1487e-149">Se også</span><span class="sxs-lookup"><span data-stu-id="1487e-149">See Also</span></span>
[<span data-ttu-id="1487e-150">Bogføre transaktioner direkte i finansposterne</span><span class="sxs-lookup"><span data-stu-id="1487e-150">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="1487e-151">Arbejde med finanskladder</span><span class="sxs-lookup"><span data-stu-id="1487e-151">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="1487e-152">Finans</span><span class="sxs-lookup"><span data-stu-id="1487e-152">Finance</span></span>](finance.md)  
<span data-ttu-id="1487e-153">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1487e-153">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
