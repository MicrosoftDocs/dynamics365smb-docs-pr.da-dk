---
title: "Ændre eller annullere ubetalte købsfakturaer | Microsoft Docs"
description: "Forklarer, hvordan du retter, annuller eller fortryder en bogført købsfaktura og automatisk opretter en købskreditnota."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 7d5b59d15304a497dc4f3c35ac1d19dcd491aaed
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a><span data-ttu-id="b386a-103">Rette eller annullere ubetalte købsfakturaer</span><span class="sxs-lookup"><span data-stu-id="b386a-103">Correct or Cancel Unpaid Purchase Invoices</span></span>
<span data-ttu-id="b386a-104">Du kan rette eller annullere en bogført købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="b386a-104">You can correct or cancel a posted purchase invoice.</span></span> <span data-ttu-id="b386a-105">Dette er nyttigt, hvis du vil rette en skrivefejl, eller hvis du ønsker at ændre købet tidligt i ordreprocessen.</span><span class="sxs-lookup"><span data-stu-id="b386a-105">This is useful if you want to correct a typing mistake, or if you want to change the purchase early in the order process.</span></span>

<span data-ttu-id="b386a-106">Hvis du allerede har betalt for produkter på den bogførte købsfaktura, kan ikke du rette eller annullere den fra selve den bogførte købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="b386a-106">If you have already paid for products on the posted purchase invoice, you cannot correct or cancel it from the posted purchase invoice itself.</span></span> <span data-ttu-id="b386a-107">I stedet skal du manuelt oprette en købskreditnota for at tilbageføre købet eventuelt styret via en købsreturvareordre.</span><span class="sxs-lookup"><span data-stu-id="b386a-107">Instead, you must manually create a purchase credit memo to reverse the purchase, optionally managed with a purchase return order.</span></span> <span data-ttu-id="b386a-108">Du kan finde flere oplysninger i [Behandle købsreturvarer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="b386a-108">For more information, see [Process Purchase Returns or Cancellations](purchasing-how-process-purchase-returns-cancellations.md).</span></span>

<span data-ttu-id="b386a-109">I vinduet **Bogført købsfaktura** kan du vælge knappen **Ret** eller **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="b386a-109">In the **Posted Purchase Invoice** window, you can choose the **Correct** button or the **Cancel** button.</span></span> <span data-ttu-id="b386a-110">Når du retter eller annullerer en bogført købsfaktura, anvendes den rettede købskreditnota på alle finanskonti og lageropgørelsesposter, der blev oprettet, da den oprindelige købsfaktura blev bogført.</span><span class="sxs-lookup"><span data-stu-id="b386a-110">When you correct or cancel a posted purchase invoice, the corrective purchase credit memo is applied to all general ledger and inventory ledger entries that were created when the initial purchase invoice was posted.</span></span> <span data-ttu-id="b386a-111">På denne måde tilbageføres den bogførte købsfaktura i dine finansposter, og rettelseskøbskreditnotaen efterlades til revisionsspor.</span><span class="sxs-lookup"><span data-stu-id="b386a-111">This reverses the posted purchase invoice in your financial records and leaves the corrective posted purchase credit memo for your audit trail.</span></span> <span data-ttu-id="b386a-112">Nedenfor beskrives anvendelsen af **Ret** og **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="b386a-112">In the following the use of **Correct** and **Cancel** is described.</span></span>

## <a name="to-correct-a-posted-purchase-invoice"></a><span data-ttu-id="b386a-113">Sådan rettes en bogført købsfaktura</span><span class="sxs-lookup"><span data-stu-id="b386a-113">To correct a posted purchase invoice</span></span>
1. <span data-ttu-id="b386a-114">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogførte købsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="b386a-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b386a-115">Vælg den bogførte købsfaktura, som du vil rette.</span><span class="sxs-lookup"><span data-stu-id="b386a-115">Select the posted purchase invoice that you want to correct.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="b386a-116">Hvis afkrydsningsfeltet **Annulleret** er markeret, kan du ikke rette den bogførte købsfaktura, da den allerede er rettet eller annulleret.</span><span class="sxs-lookup"><span data-stu-id="b386a-116">If the **Canceled** check box is selected, then you cannot correct the posted purchase invoice because it has already been corrected or canceled.</span></span>
3. <span data-ttu-id="b386a-117">I vinduet **Bogført købsfaktura** skal du vælge **Ret**.</span><span class="sxs-lookup"><span data-stu-id="b386a-117">In the **Posted Purchase Invoice** window, choose **Correct**.</span></span>

    <span data-ttu-id="b386a-118">En ny købsfaktura med de samme oplysninger oprettes, hvor du kan foretage en rettelse.</span><span class="sxs-lookup"><span data-stu-id="b386a-118">A new purchase invoice with the same information is created where you can make the correction.</span></span> <span data-ttu-id="b386a-119">Du kan finde flere oplysninger under [Registrere køb](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="b386a-119">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span> <span data-ttu-id="b386a-120">Feltet **Annulleret** på den første bogførte købsfaktura ændres til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b386a-120">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>

    <span data-ttu-id="b386a-121">En købskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="b386a-121">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span>
4. <span data-ttu-id="b386a-122">Vælg **Vis rettelseskreditnota** for at få vist den bogførte købskreditnota, som gør den oprindelige bogførte købsfaktura ugyldig.</span><span class="sxs-lookup"><span data-stu-id="b386a-122">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="to-cancel-a-posted-purchase-invoice"></a><span data-ttu-id="b386a-123">Sådan annulleres en bogført købsfaktura</span><span class="sxs-lookup"><span data-stu-id="b386a-123">To cancel a posted purchase invoice</span></span>
1. <span data-ttu-id="b386a-124">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogførte købsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="b386a-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b386a-125">Vælg den bogførte købsfaktura, som du vil annullere.</span><span class="sxs-lookup"><span data-stu-id="b386a-125">Select the posted purchase invoice that you want to cancel.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="b386a-126">Hvis afkrydsningsfeltet **Annulleret** er markeret, kan du ikke annullere den bogførte købsfaktura, da den allerede er annulleret eller rettet.</span><span class="sxs-lookup"><span data-stu-id="b386a-126">If the **Canceled** check box is selected, then you cannot cancel the posted purchase invoice because it has already been canceled or corrected.</span></span>
3. <span data-ttu-id="b386a-127">I vinduet **Bogført købsfaktura** skal du vælge **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="b386a-127">In the **Posted Purchase Invoice** window, choose **Cancel**.</span></span>

    <span data-ttu-id="b386a-128">En købskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="b386a-128">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span> <span data-ttu-id="b386a-129">Feltet **Annulleret** på den første bogførte købsfaktura ændres til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b386a-129">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>
4. <span data-ttu-id="b386a-130">Vælg **Vis rettelseskreditnota** for at få vist den bogførte købskreditnota, som gør den oprindelige bogførte købsfaktura ugyldig.</span><span class="sxs-lookup"><span data-stu-id="b386a-130">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="see-also"></a><span data-ttu-id="b386a-131">Se også</span><span class="sxs-lookup"><span data-stu-id="b386a-131">See Also</span></span>
[<span data-ttu-id="b386a-132">Køb</span><span class="sxs-lookup"><span data-stu-id="b386a-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="b386a-133">Registrere køb</span><span class="sxs-lookup"><span data-stu-id="b386a-133">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="b386a-134">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b386a-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

