---
title: Ændre eller annullere ubetalte købsfakturaer | Microsoft Docs
description: Forklarer, hvordan du retter, annuller eller fortryder en bogført købsfaktura og automatisk opretter en købskreditnota.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b2e2e64cd3845f20e9c3e0fea5c114ebcd08491d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5780228"
---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a><span data-ttu-id="b3d1f-103">Rette eller annullere ubetalte købsfakturaer</span><span class="sxs-lookup"><span data-stu-id="b3d1f-103">Correct or Cancel Unpaid Purchase Invoices</span></span>

<span data-ttu-id="b3d1f-104">Du kan rette eller annullere en bogført købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-104">You can correct or cancel a posted purchase invoice.</span></span> <span data-ttu-id="b3d1f-105">Dette er nyttigt, hvis du vil rette en skrivefejl, eller hvis du ønsker at ændre købet tidligt i ordreprocessen.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-105">This is useful if you want to correct a typing mistake, or if you want to change the purchase early in the order process.</span></span>

<span data-ttu-id="b3d1f-106">Hvis du allerede har betalt for produkter på den bogførte købsfaktura, kan ikke du rette eller annullere den fra selve den bogførte købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-106">If you have already paid for products on the posted purchase invoice, you cannot correct or cancel it from the posted purchase invoice itself.</span></span> <span data-ttu-id="b3d1f-107">I stedet skal du manuelt oprette en købskreditnota for at tilbageføre købet eventuelt styret via en købsreturvareordre.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-107">Instead, you must manually create a purchase credit memo to reverse the purchase, optionally managed with a purchase return order.</span></span> <span data-ttu-id="b3d1f-108">Det samme gælder, hvis du vil ændre en bogført købsfaktura, der er baseret på kombinerede købsleverancer.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-108">The same applies if you want to modify a posted purchase invoice that was based on combined purchase receipts.</span></span> <span data-ttu-id="b3d1f-109">Du kan finde flere oplysninger i [Behandle købsreturvarer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="b3d1f-109">For more information, see [Process Purchase Returns or Cancellations](purchasing-how-process-purchase-returns-cancellations.md).</span></span>

<span data-ttu-id="b3d1f-110">På siden **Bogført købsfaktura** kan du vælge knappen **Ret** eller **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-110">On the **Posted Purchase Invoice** page, you can choose the **Correct** button or the **Cancel** button.</span></span> <span data-ttu-id="b3d1f-111">Når du retter eller annullerer en bogført købsfaktura, anvendes den rettede købskreditnota på alle finanskonti og lageropgørelsesposter, der blev oprettet, da den oprindelige købsfaktura blev bogført.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-111">When you correct or cancel a posted purchase invoice, the corrective purchase credit memo is applied to all general ledger and inventory ledger entries that were created when the initial purchase invoice was posted.</span></span> <span data-ttu-id="b3d1f-112">På denne måde tilbageføres den bogførte købsfaktura i dine finansposter, og rettelseskøbskreditnotaen efterlades til revisionsspor.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-112">This reverses the posted purchase invoice in your financial records and leaves the corrective posted purchase credit memo for your audit trail.</span></span> <span data-ttu-id="b3d1f-113">Nedenfor beskrives anvendelsen af **Ret** og **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-113">In the following the use of **Correct** and **Cancel** is described.</span></span>
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE4dhoc?rel=0]

## <a name="to-correct-a-posted-purchase-invoice"></a><span data-ttu-id="b3d1f-114">Sådan rettes en bogført købsfaktura</span><span class="sxs-lookup"><span data-stu-id="b3d1f-114">To correct a posted purchase invoice</span></span>
1. <span data-ttu-id="b3d1f-115">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bogførte købsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b3d1f-116">Vælg den bogførte købsfaktura, som du vil rette.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-116">Select the posted purchase invoice that you want to correct.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="b3d1f-117">Hvis afkrydsningsfeltet **Annulleret** er markeret, kan du ikke rette den bogførte købsfaktura, da den allerede er rettet eller annulleret.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-117">If the **Canceled** check box is selected, then you cannot correct the posted purchase invoice because it has already been corrected or canceled.</span></span>
3. <span data-ttu-id="b3d1f-118">På siden **Bogført købsfaktura** skal du vælge **Ret**.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-118">On the **Posted Purchase Invoice** page, choose **Correct**.</span></span>

    <span data-ttu-id="b3d1f-119">En ny købsfaktura med de samme oplysninger oprettes, hvor du kan foretage en rettelse.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-119">A new purchase invoice with the same information is created where you can make the correction.</span></span> <span data-ttu-id="b3d1f-120">Du kan finde flere oplysninger i [Registrere køb](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="b3d1f-120">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span> <span data-ttu-id="b3d1f-121">Feltet **Annulleret** på den første bogførte købsfaktura ændres til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-121">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>

    <span data-ttu-id="b3d1f-122">En købskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-122">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span>
4. <span data-ttu-id="b3d1f-123">Vælg **Vis rettelseskreditnota** for at få vist den bogførte købskreditnota, som gør den oprindelige bogførte købsfaktura ugyldig.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-123">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="to-cancel-a-posted-purchase-invoice"></a><span data-ttu-id="b3d1f-124">Sådan annulleres en bogført købsfaktura</span><span class="sxs-lookup"><span data-stu-id="b3d1f-124">To cancel a posted purchase invoice</span></span>
1. <span data-ttu-id="b3d1f-125">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bogførte købsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b3d1f-126">Vælg den bogførte købsfaktura, som du vil annullere.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-126">Select the posted purchase invoice that you want to cancel.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="b3d1f-127">Hvis afkrydsningsfeltet **Annulleret** er markeret, kan du ikke annullere den bogførte købsfaktura, da den allerede er annulleret eller rettet.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-127">If the **Canceled** check box is selected, then you cannot cancel the posted purchase invoice because it has already been canceled or corrected.</span></span>
3. <span data-ttu-id="b3d1f-128">På siden **Bogført købsfaktura** skal du vælge **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-128">On the **Posted Purchase Invoice** page, choose **Cancel**.</span></span>

    <span data-ttu-id="b3d1f-129">En købskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-129">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span> <span data-ttu-id="b3d1f-130">Feltet **Annulleret** på den første bogførte købsfaktura ændres til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-130">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>
4. <span data-ttu-id="b3d1f-131">Vælg **Vis rettelseskreditnota** for at få vist den bogførte købskreditnota, som gør den oprindelige bogførte købsfaktura ugyldig.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-131">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

### <a name="partial-invoice-posting-also-supported"></a><span data-ttu-id="b3d1f-132">Delvis fakturabogføring understøttes også</span><span class="sxs-lookup"><span data-stu-id="b3d1f-132">Partial Invoice Posting also Supported</span></span>
<span data-ttu-id="b3d1f-133">Hvis annulleringen vedrører en delvis fakturabogføring, opdateres den oprindelige indkøbsordrelinje, så den afspejler det annullerede fakturerede antal.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-133">If the cancellation is related to a partial invoice posting, then the originating purchase order line is updated to reflect the canceled invoiced quantity.</span></span> <span data-ttu-id="b3d1f-134">Felterne **Fakturer antal** og **Fakt. antal** på den relaterede købsordrelinje nulstilles til værdierne før den delvise fakturabogføring.</span><span class="sxs-lookup"><span data-stu-id="b3d1f-134">The **Qty. to Invoice** and **Qty. Invoiced** fields on the related purchase order line are reset to the values before the partial posting.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3d1f-135">Se også</span><span class="sxs-lookup"><span data-stu-id="b3d1f-135">See Also</span></span>
[<span data-ttu-id="b3d1f-136">Køb</span><span class="sxs-lookup"><span data-stu-id="b3d1f-136">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="b3d1f-137">Registrere køb</span><span class="sxs-lookup"><span data-stu-id="b3d1f-137">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="b3d1f-138">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b3d1f-138">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]