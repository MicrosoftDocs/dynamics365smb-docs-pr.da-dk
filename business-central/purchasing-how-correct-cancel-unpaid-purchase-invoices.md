---
title: Ændre eller annullere ubetalte købsfakturaer | Microsoft Docs
description: Forklarer, hvordan du retter, annuller eller fortryder en bogført købsfaktura og automatisk opretter en købskreditnota.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 07/02/2020
ms.author: edupont
ms.openlocfilehash: 3badffb854323a385123e86066f14de5a2b75b28
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783120"
---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a><span data-ttu-id="b0f10-103">Rette eller annullere ubetalte købsfakturaer</span><span class="sxs-lookup"><span data-stu-id="b0f10-103">Correct or Cancel Unpaid Purchase Invoices</span></span>

<span data-ttu-id="b0f10-104">Du kan rette eller annullere en bogført købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="b0f10-104">You can correct or cancel a posted purchase invoice.</span></span> <span data-ttu-id="b0f10-105">Dette er nyttigt, hvis du vil rette en skrivefejl, eller hvis du ønsker at ændre købet tidligt i ordreprocessen.</span><span class="sxs-lookup"><span data-stu-id="b0f10-105">This is useful if you want to correct a typing mistake, or if you want to change the purchase early in the order process.</span></span>

<span data-ttu-id="b0f10-106">Hvis du allerede har betalt for produkter på den bogførte købsfaktura, kan ikke du rette eller annullere den fra selve den bogførte købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="b0f10-106">If you have already paid for products on the posted purchase invoice, you cannot correct or cancel it from the posted purchase invoice itself.</span></span> <span data-ttu-id="b0f10-107">I stedet skal du manuelt oprette en købskreditnota for at tilbageføre købet eventuelt styret via en købsreturvareordre.</span><span class="sxs-lookup"><span data-stu-id="b0f10-107">Instead, you must manually create a purchase credit memo to reverse the purchase, optionally managed with a purchase return order.</span></span> <span data-ttu-id="b0f10-108">Det samme gælder, hvis du vil ændre en bogført købsfaktura, der er baseret på kombinerede købsleverancer.</span><span class="sxs-lookup"><span data-stu-id="b0f10-108">The same applies if you want to modify a posted purchase invoice that was based on combined purchase receipts.</span></span> <span data-ttu-id="b0f10-109">Du kan finde flere oplysninger i [Behandle købsreturvarer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="b0f10-109">For more information, see [Process Purchase Returns or Cancellations](purchasing-how-process-purchase-returns-cancellations.md).</span></span>

<span data-ttu-id="b0f10-110">På siden **Bogført købsfaktura** kan du vælge knappen **Ret** eller **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="b0f10-110">On the **Posted Purchase Invoice** page, you can choose the **Correct** button or the **Cancel** button.</span></span> <span data-ttu-id="b0f10-111">Når du retter eller annullerer en bogført købsfaktura, anvendes den rettede købskreditnota på alle finanskonti og lageropgørelsesposter, der blev oprettet, da den oprindelige købsfaktura blev bogført.</span><span class="sxs-lookup"><span data-stu-id="b0f10-111">When you correct or cancel a posted purchase invoice, the corrective purchase credit memo is applied to all general ledger and inventory ledger entries that were created when the initial purchase invoice was posted.</span></span> <span data-ttu-id="b0f10-112">På denne måde tilbageføres den bogførte købsfaktura i dine finansposter, og rettelseskøbskreditnotaen efterlades til revisionsspor.</span><span class="sxs-lookup"><span data-stu-id="b0f10-112">This reverses the posted purchase invoice in your financial records and leaves the corrective posted purchase credit memo for your audit trail.</span></span> <span data-ttu-id="b0f10-113">Nedenfor beskrives anvendelsen af **Ret** og **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="b0f10-113">In the following the use of **Correct** and **Cancel** is described.</span></span>
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE4dhoc?rel=0]

## <a name="to-correct-a-posted-purchase-invoice"></a><span data-ttu-id="b0f10-114">Sådan rettes en bogført købsfaktura</span><span class="sxs-lookup"><span data-stu-id="b0f10-114">To correct a posted purchase invoice</span></span>
1. <span data-ttu-id="b0f10-115">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bogførte købsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="b0f10-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b0f10-116">Vælg den bogførte købsfaktura, som du vil rette.</span><span class="sxs-lookup"><span data-stu-id="b0f10-116">Select the posted purchase invoice that you want to correct.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="b0f10-117">Hvis afkrydsningsfeltet **Annulleret** er markeret, kan du ikke rette den bogførte købsfaktura, da den allerede er rettet eller annulleret.</span><span class="sxs-lookup"><span data-stu-id="b0f10-117">If the **Canceled** check box is selected, then you cannot correct the posted purchase invoice because it has already been corrected or canceled.</span></span>
3. <span data-ttu-id="b0f10-118">På siden **Bogført købsfaktura** skal du vælge **Ret**.</span><span class="sxs-lookup"><span data-stu-id="b0f10-118">On the **Posted Purchase Invoice** page, choose **Correct**.</span></span>

    <span data-ttu-id="b0f10-119">En ny købsfaktura med de samme oplysninger oprettes, hvor du kan foretage en rettelse.</span><span class="sxs-lookup"><span data-stu-id="b0f10-119">A new purchase invoice with the same information is created where you can make the correction.</span></span> <span data-ttu-id="b0f10-120">Du kan finde flere oplysninger under [Registrere køb](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="b0f10-120">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span> <span data-ttu-id="b0f10-121">Feltet **Annulleret** på den første bogførte købsfaktura ændres til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b0f10-121">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>

    <span data-ttu-id="b0f10-122">En købskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="b0f10-122">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span>
4. <span data-ttu-id="b0f10-123">Vælg **Vis rettelseskreditnota** for at få vist den bogførte købskreditnota, som gør den oprindelige bogførte købsfaktura ugyldig.</span><span class="sxs-lookup"><span data-stu-id="b0f10-123">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="to-cancel-a-posted-purchase-invoice"></a><span data-ttu-id="b0f10-124">Sådan annulleres en bogført købsfaktura</span><span class="sxs-lookup"><span data-stu-id="b0f10-124">To cancel a posted purchase invoice</span></span>
1. <span data-ttu-id="b0f10-125">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bogførte købsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="b0f10-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b0f10-126">Vælg den bogførte købsfaktura, som du vil annullere.</span><span class="sxs-lookup"><span data-stu-id="b0f10-126">Select the posted purchase invoice that you want to cancel.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="b0f10-127">Hvis afkrydsningsfeltet **Annulleret** er markeret, kan du ikke annullere den bogførte købsfaktura, da den allerede er annulleret eller rettet.</span><span class="sxs-lookup"><span data-stu-id="b0f10-127">If the **Canceled** check box is selected, then you cannot cancel the posted purchase invoice because it has already been canceled or corrected.</span></span>
3. <span data-ttu-id="b0f10-128">På siden **Bogført købsfaktura** skal du vælge **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="b0f10-128">On the **Posted Purchase Invoice** page, choose **Cancel**.</span></span>

    <span data-ttu-id="b0f10-129">En købskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="b0f10-129">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span> <span data-ttu-id="b0f10-130">Feltet **Annulleret** på den første bogførte købsfaktura ændres til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b0f10-130">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>
4. <span data-ttu-id="b0f10-131">Vælg **Vis rettelseskreditnota** for at få vist den bogførte købskreditnota, som gør den oprindelige bogførte købsfaktura ugyldig.</span><span class="sxs-lookup"><span data-stu-id="b0f10-131">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

### <a name="partial-invoice-posting-also-supported"></a><span data-ttu-id="b0f10-132">Delvis fakturabogføring understøttes også</span><span class="sxs-lookup"><span data-stu-id="b0f10-132">Partial Invoice Posting also Supported</span></span>
<span data-ttu-id="b0f10-133">Hvis annulleringen vedrører en delvis fakturabogføring, opdateres den oprindelige indkøbsordrelinje, så den afspejler det annullerede fakturerede antal.</span><span class="sxs-lookup"><span data-stu-id="b0f10-133">If the cancellation is related to a partial invoice posting, then the originating purchase order line is updated to reflect the canceled invoiced quantity.</span></span> <span data-ttu-id="b0f10-134">Felterne **Fakturer antal** og **Fakt. antal** på den relaterede købsordrelinje nulstilles til værdierne før den delvise fakturabogføring.</span><span class="sxs-lookup"><span data-stu-id="b0f10-134">The **Qty. to Invoice** and **Qty. Invoiced** fields on the related purchase order line are reset to the values before the partial posting.</span></span>

## <a name="see-also"></a><span data-ttu-id="b0f10-135">Se også</span><span class="sxs-lookup"><span data-stu-id="b0f10-135">See Also</span></span>
[<span data-ttu-id="b0f10-136">Køb</span><span class="sxs-lookup"><span data-stu-id="b0f10-136">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="b0f10-137">Registrere køb</span><span class="sxs-lookup"><span data-stu-id="b0f10-137">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="b0f10-138">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b0f10-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
