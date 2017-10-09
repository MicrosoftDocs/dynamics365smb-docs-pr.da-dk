---
title: Udligne poster i forskellige valutaer | Microsoft Docs
description: "Du kan udligne finansposter i flere valutaer, f.eks. hvis du sælger i én valuta og modtager betaling i en anden."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6379aea58ab7943b117e5b19b22f71193290c2cb
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="e2708-103">Fremgangsmåde: Muliggøre udligning af finansposter i forskellige valutaer</span><span class="sxs-lookup"><span data-stu-id="e2708-103">How to: Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="e2708-104">Hvis du køber varer fra en leverandør i én valuta, men foretager betaling i en anden valuta, kan du udligne betalingen med købet.</span><span class="sxs-lookup"><span data-stu-id="e2708-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="e2708-105">Ligeledes, hvis du sælger til en debitor i en valuta og modtager betaling i en anden, kan du knytte betalingen til salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="e2708-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="e2708-106">Følgende procedure beskriver, hvordan du kan angive dette for kreditorposter i vinduet **Købsopsætning**.</span><span class="sxs-lookup"><span data-stu-id="e2708-106">The following procedure describes how to set this up for vendor ledger entries in the **Purchases & Payables Setup** window.</span></span> <span data-ttu-id="e2708-107">Der er tilsvarende opsætning for debitorposter i vinduet **Salgsopsætning**.</span><span class="sxs-lookup"><span data-stu-id="e2708-107">The setup is similar for customer ledger entries in the **Sales & Receivables Setup** window.</span></span>

> [!NOTE]  
>   <span data-ttu-id="e2708-108">Denne funktion kræver, at oplevelsen er indstillet til **Suite**.</span><span class="sxs-lookup"><span data-stu-id="e2708-108">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="e2708-109">Du kan finde flere oplysninger under [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="e2708-109">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="e2708-110">Sådan aktiveres udligning af kreditorposter i forskellige valutaer</span><span class="sxs-lookup"><span data-stu-id="e2708-110">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="e2708-111">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Købsopsætning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="e2708-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="e2708-112">Vælg en af følgende indstillinger i feltet **Valutaudligning**.</span><span class="sxs-lookup"><span data-stu-id="e2708-112">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="e2708-113">Indstilling</span><span class="sxs-lookup"><span data-stu-id="e2708-113">Option</span></span> | <span data-ttu-id="e2708-114">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e2708-114">Description</span></span> |
| --- | --- |
| <span data-ttu-id="e2708-115">Ingen</span><span class="sxs-lookup"><span data-stu-id="e2708-115">None</span></span> |<span data-ttu-id="e2708-116">Udligning mellem valutaer er ikke tilladt.</span><span class="sxs-lookup"><span data-stu-id="e2708-116">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="e2708-117">ØMU</span><span class="sxs-lookup"><span data-stu-id="e2708-117">EMU</span></span> |<span data-ttu-id="e2708-118">Udligning mellem ØMU-valutaer er tilladt.</span><span class="sxs-lookup"><span data-stu-id="e2708-118">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="e2708-119">Alle</span><span class="sxs-lookup"><span data-stu-id="e2708-119">All</span></span> |<span data-ttu-id="e2708-120">Udligning mellem alle valutaer er tilladt.</span><span class="sxs-lookup"><span data-stu-id="e2708-120">Application between all currencies is allowed.</span></span> |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a><span data-ttu-id="e2708-121">Sådan opsættes finanskonti til afrundingsdifferencer ved valutaudligning</span><span class="sxs-lookup"><span data-stu-id="e2708-121">To set up G/L accounts for currency application rounding differences</span></span>  
<span data-ttu-id="e2708-122">Hvis du anvender poster i forskellige valutaer, skal du oprette finanskonti, hvor du kan bogføre afrundingsdifferencer.</span><span class="sxs-lookup"><span data-stu-id="e2708-122">If you apply entries in different currencies, you must set up the general ledger accounts to which you want to post rounding differences.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="e2708-123">Du skal oprette de pågældende finanskonti, før du kan udføre opgaven.</span><span class="sxs-lookup"><span data-stu-id="e2708-123">You must set up the general ledger accounts before you complete the task.</span></span> <span data-ttu-id="e2708-124">Du kan finde flere oplysninger i [Om finans- og kontoplanen](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="e2708-124">For more information, see [Understanding the General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span> 
  
1. <span data-ttu-id="e2708-125">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Debitorbogføringsgrupper**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="e2708-125">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer Posting Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e2708-126">I felterne **Valutaudlign.afrnd.kto (deb.)** og **Valutaudlign.afrnd.kto (kre.)** skal du indtaste de relevante finanskonti bogføring af afrundingsdifferencer.</span><span class="sxs-lookup"><span data-stu-id="e2708-126">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  
3. <span data-ttu-id="e2708-127">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kreditorbogføringsgrupper**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="e2708-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendor Posting Groups**, and then choose the related link.</span></span>  
4. <span data-ttu-id="e2708-128">I felterne **Valutaudlign.afrnd.kto (deb.)** og **Valutaudlign.afrnd.kto (kre.)** skal du indtaste de relevante finanskonti bogføring af afrundingsdifferencer.</span><span class="sxs-lookup"><span data-stu-id="e2708-128">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e2708-129">Se også</span><span class="sxs-lookup"><span data-stu-id="e2708-129">See Also</span></span>
[<span data-ttu-id="e2708-130">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="e2708-130">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="e2708-131">Administrere tilgodehavender</span><span class="sxs-lookup"><span data-stu-id="e2708-131">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="e2708-132">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e2708-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

