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
ms.date: 01/25/2020
ms.author: sgroespe
ms.openlocfilehash: 2896bfc5cafed679bd54dced6c7726a1c49859de
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/28/2020
ms.locfileid: "2992020"
---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a><span data-ttu-id="13df0-103">Rette eller annullere ubetalte købsfakturaer</span><span class="sxs-lookup"><span data-stu-id="13df0-103">Correct or Cancel Unpaid Purchase Invoices</span></span>
<span data-ttu-id="13df0-104">Du kan rette eller annullere en bogført købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="13df0-104">You can correct or cancel a posted purchase invoice.</span></span> <span data-ttu-id="13df0-105">Dette er nyttigt, hvis du vil rette en skrivefejl, eller hvis du ønsker at ændre købet tidligt i ordreprocessen.</span><span class="sxs-lookup"><span data-stu-id="13df0-105">This is useful if you want to correct a typing mistake, or if you want to change the purchase early in the order process.</span></span>

<span data-ttu-id="13df0-106">Hvis du allerede har betalt for produkter på den bogførte købsfaktura, kan ikke du rette eller annullere den fra selve den bogførte købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="13df0-106">If you have already paid for products on the posted purchase invoice, you cannot correct or cancel it from the posted purchase invoice itself.</span></span> <span data-ttu-id="13df0-107">I stedet skal du manuelt oprette en købskreditnota for at tilbageføre købet eventuelt styret via en købsreturvareordre.</span><span class="sxs-lookup"><span data-stu-id="13df0-107">Instead, you must manually create a purchase credit memo to reverse the purchase, optionally managed with a purchase return order.</span></span> <span data-ttu-id="13df0-108">Du kan finde flere oplysninger i [Behandle købsreturvarer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="13df0-108">For more information, see [Process Purchase Returns or Cancellations](purchasing-how-process-purchase-returns-cancellations.md).</span></span>

<span data-ttu-id="13df0-109">På siden **Bogført købsfaktura** kan du vælge knappen **Ret** eller **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="13df0-109">On the **Posted Purchase Invoice** page, you can choose the **Correct** button or the **Cancel** button.</span></span> <span data-ttu-id="13df0-110">Når du retter eller annullerer en bogført købsfaktura, anvendes den rettede købskreditnota på alle finanskonti og lageropgørelsesposter, der blev oprettet, da den oprindelige købsfaktura blev bogført.</span><span class="sxs-lookup"><span data-stu-id="13df0-110">When you correct or cancel a posted purchase invoice, the corrective purchase credit memo is applied to all general ledger and inventory ledger entries that were created when the initial purchase invoice was posted.</span></span> <span data-ttu-id="13df0-111">På denne måde tilbageføres den bogførte købsfaktura i dine finansposter, og rettelseskøbskreditnotaen efterlades til revisionsspor.</span><span class="sxs-lookup"><span data-stu-id="13df0-111">This reverses the posted purchase invoice in your financial records and leaves the corrective posted purchase credit memo for your audit trail.</span></span> <span data-ttu-id="13df0-112">Nedenfor beskrives anvendelsen af **Ret** og **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="13df0-112">In the following the use of **Correct** and **Cancel** is described.</span></span>
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE4dhoc]

## <a name="to-correct-a-posted-purchase-invoice"></a><span data-ttu-id="13df0-113">Sådan rettes en bogført købsfaktura</span><span class="sxs-lookup"><span data-stu-id="13df0-113">To correct a posted purchase invoice</span></span>
1. <span data-ttu-id="13df0-114">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bogførte købsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="13df0-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="13df0-115">Vælg den bogførte købsfaktura, som du vil rette.</span><span class="sxs-lookup"><span data-stu-id="13df0-115">Select the posted purchase invoice that you want to correct.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="13df0-116">Hvis afkrydsningsfeltet **Annulleret** er markeret, kan du ikke rette den bogførte købsfaktura, da den allerede er rettet eller annulleret.</span><span class="sxs-lookup"><span data-stu-id="13df0-116">If the **Canceled** check box is selected, then you cannot correct the posted purchase invoice because it has already been corrected or canceled.</span></span>
3. <span data-ttu-id="13df0-117">På siden **Bogført købsfaktura** skal du vælge **Ret**.</span><span class="sxs-lookup"><span data-stu-id="13df0-117">On the **Posted Purchase Invoice** page, choose **Correct**.</span></span>

    <span data-ttu-id="13df0-118">En ny købsfaktura med de samme oplysninger oprettes, hvor du kan foretage en rettelse.</span><span class="sxs-lookup"><span data-stu-id="13df0-118">A new purchase invoice with the same information is created where you can make the correction.</span></span> <span data-ttu-id="13df0-119">Du kan finde flere oplysninger under [Registrere køb](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="13df0-119">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span> <span data-ttu-id="13df0-120">Feltet **Annulleret** på den første bogførte købsfaktura ændres til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="13df0-120">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>

    <span data-ttu-id="13df0-121">En købskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="13df0-121">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span>
4. <span data-ttu-id="13df0-122">Vælg **Vis rettelseskreditnota** for at få vist den bogførte købskreditnota, som gør den oprindelige bogførte købsfaktura ugyldig.</span><span class="sxs-lookup"><span data-stu-id="13df0-122">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="to-cancel-a-posted-purchase-invoice"></a><span data-ttu-id="13df0-123">Sådan annulleres en bogført købsfaktura</span><span class="sxs-lookup"><span data-stu-id="13df0-123">To cancel a posted purchase invoice</span></span>
1. <span data-ttu-id="13df0-124">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bogførte købsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="13df0-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="13df0-125">Vælg den bogførte købsfaktura, som du vil annullere.</span><span class="sxs-lookup"><span data-stu-id="13df0-125">Select the posted purchase invoice that you want to cancel.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="13df0-126">Hvis afkrydsningsfeltet **Annulleret** er markeret, kan du ikke annullere den bogførte købsfaktura, da den allerede er annulleret eller rettet.</span><span class="sxs-lookup"><span data-stu-id="13df0-126">If the **Canceled** check box is selected, then you cannot cancel the posted purchase invoice because it has already been canceled or corrected.</span></span>
3. <span data-ttu-id="13df0-127">På siden **Bogført købsfaktura** skal du vælge **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="13df0-127">On the **Posted Purchase Invoice** page, choose **Cancel**.</span></span>

    <span data-ttu-id="13df0-128">En købskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="13df0-128">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span> <span data-ttu-id="13df0-129">Feltet **Annulleret** på den første bogførte købsfaktura ændres til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="13df0-129">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>
4. <span data-ttu-id="13df0-130">Vælg **Vis rettelseskreditnota** for at få vist den bogførte købskreditnota, som gør den oprindelige bogførte købsfaktura ugyldig.</span><span class="sxs-lookup"><span data-stu-id="13df0-130">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

### <a name="partial-invoice-posting-also-supported"></a><span data-ttu-id="13df0-131">Delvis fakturabogføring understøttes også</span><span class="sxs-lookup"><span data-stu-id="13df0-131">Partial Invoice Posting also Supported</span></span>
<span data-ttu-id="13df0-132">Hvis annulleringen vedrører en delvis fakturabogføring, opdateres den oprindelige indkøbsordrelinje, så den afspejler det annullerede fakturerede antal.</span><span class="sxs-lookup"><span data-stu-id="13df0-132">If the cancellation is related to a partial invoice posting, then the originating purchase order line is updated to reflect the canceled invoiced quantity.</span></span> <span data-ttu-id="13df0-133">Felterne **Fakturer antal** og **Fakt. antal** på den relaterede købsordrelinje nulstilles til værdierne før den delvise fakturabogføring.</span><span class="sxs-lookup"><span data-stu-id="13df0-133">The **Qty. to Invoice** and **Qty. Invoiced** fields on the related purchase order line are reset to the values before the partial posting.</span></span>

## <a name="see-also"></a><span data-ttu-id="13df0-134">Se også</span><span class="sxs-lookup"><span data-stu-id="13df0-134">See Also</span></span>
[<span data-ttu-id="13df0-135">Køb</span><span class="sxs-lookup"><span data-stu-id="13df0-135">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="13df0-136">Registrere køb</span><span class="sxs-lookup"><span data-stu-id="13df0-136">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="13df0-137">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="13df0-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
