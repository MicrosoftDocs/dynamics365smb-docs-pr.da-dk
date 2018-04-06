---
title: "Opsætning af fakturaafrunding | Microsoft Docs"
description: "Du kan afrunde fakturabeløb, når du opretter fakturaer. Derudover kan lokale regler eller skikke kræve, at du afrunder på en bestemt måde, f.eks. til et beløb, der er deleligt med 0,05."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ceebeeac325c00d6aef25d8ca51fcfee1ab4e1d5
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-invoice-rounding"></a><span data-ttu-id="e1403-104">Opsætning af fakturaafrunding</span><span class="sxs-lookup"><span data-stu-id="e1403-104">Set Up Invoice Rounding</span></span>
<span data-ttu-id="e1403-105">Hvis du vil afrunde fakturabeløb, når du opretter fakturaer, kan du bruge funktionen til automatisk afrunding.</span><span class="sxs-lookup"><span data-stu-id="e1403-105">If you need to round invoice amounts when you create invoices, you can use the automatic rounding function.</span></span> <span data-ttu-id="e1403-106">Når en faktura afrundes, tilføjes en ekstra linje med afrundingsbeløbet og bogføres sammen med de andre fakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="e1403-106">When an invoice is rounded, an extra line is added with the rounding amount and posted with the other invoice lines.</span></span>

> [!NOTE]  
>  <span data-ttu-id="e1403-107">Lokale regler eller skikke kan kræve, at fakturaen afrundes på en bestemt måde, f.eks. til et beløb, der er deleligt med 0,05.</span><span class="sxs-lookup"><span data-stu-id="e1403-107">Local regulations or local custom may require the invoice to be rounded in a specific way, for example, to an amount divisible by 0.05.</span></span>  
  
<span data-ttu-id="e1403-108">Når du vil bruge automatisk fakturaafrunding, skal du:</span><span class="sxs-lookup"><span data-stu-id="e1403-108">To use automatic invoice rounding, you must:</span></span>  
  
* <span data-ttu-id="e1403-109">Angive de finanskonti, som afrundingsdifferencerne bogføres til.</span><span class="sxs-lookup"><span data-stu-id="e1403-109">Specify the general ledger accounts to which rounding differences will be posted.</span></span>  
* <span data-ttu-id="e1403-110">Definere regler for afrunding af fakturaer i lokal valuta og i udenlandsk valuta.</span><span class="sxs-lookup"><span data-stu-id="e1403-110">Set up rules for rounding invoices in local currency and in foreign currency.</span></span>  
* <span data-ttu-id="e1403-111">Aktivere funktionen.</span><span class="sxs-lookup"><span data-stu-id="e1403-111">Activate the function.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="e1403-112">Ud over funktionerne til fakturaafrunding kan du afrunde beløb på fakturaer vha. funktionen pris-afrundingspræcision og afrundingsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="e1403-112">In addition to the invoice rounding features, you can round amounts on invoices by the unit-amount rounding feature and the amount rounding feature.</span></span>  
 
## <a name="set-up-general-ledger-accounts-for-invoice-rounding-differences"></a><span data-ttu-id="e1403-113">Opsætte finanskonti til fakturaafrundingsdifferencer</span><span class="sxs-lookup"><span data-stu-id="e1403-113">Set up general ledger accounts for invoice rounding differences</span></span>
<span data-ttu-id="e1403-114">Du skal oprette finanskonti eller konti, hvor afrundingsdifferencer kan bogføres, for at bruge den automatiske fakturaafrundingsfunktion.</span><span class="sxs-lookup"><span data-stu-id="e1403-114">To use the automatic invoice rounding function, you must set up the general ledger account or accounts where rounding differences will be posted.</span></span> <span data-ttu-id="e1403-115">Du skal først oprette momsproduktbogføringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="e1403-115">Before you can do this, you must set up VAT product posting groups.</span></span> <span data-ttu-id="e1403-116">Du kan finde flere oplysninger i [Konfigurer moms](finance-setup-vat.md).</span><span class="sxs-lookup"><span data-stu-id="e1403-116">For more information, see [Set up VAT](finance-setup-vat.md).</span></span>  
  
### <a name="to-set-up-general-ledger-accounts-for-invoice-rounding-differences"></a><span data-ttu-id="e1403-117">Sådan opsættes finanskonti til fakturaafrundingsdifferencer</span><span class="sxs-lookup"><span data-stu-id="e1403-117">To set up general ledger accounts for invoice rounding differences</span></span>  
1. <span data-ttu-id="e1403-118">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoplan**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="e1403-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e1403-119">På siden **Kontoplan** skal du opsætte kontoen og kalde den **Fakturaafrunding** eller noget tilsvarende.</span><span class="sxs-lookup"><span data-stu-id="e1403-119">On the **Chart of Accounts** page, set up the account and name it **Invoice Rounding** or something similar.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="e1403-120"> bruger kontonavnet som tekst på fakturaer, der afrundes.</span><span class="sxs-lookup"><span data-stu-id="e1403-120"> will use the account name as text for invoices that are rounded.</span></span>  
3. <span data-ttu-id="e1403-121">Afhængigt af om du bruger moms eller sales tax, skal du i feltet **Momsproduktbogf.gruppe** eller **Momsprod.bogf.gruppe** vælge en bogføringsgruppe til afrundede beløb.</span><span class="sxs-lookup"><span data-stu-id="e1403-121">Depending on whether you use VAT or sales tax, in the **Tax Prod. Posting Group** or **VAT Prod. Posting Group** fields, choose a posting group for rounded amounts.</span></span> <span data-ttu-id="e1403-122">Du kan oprette en ny gruppekode, som kan anvendes til fakturaafrunding.</span><span class="sxs-lookup"><span data-stu-id="e1403-122">You may want to set up a new group code to use for invoice rounding.</span></span>
4. <span data-ttu-id="e1403-123">Lad feltet **Bogføringstype** og enten feltet **Momsvirksomhedsbogf.gruppe** eller **Momsvirk.bogf.gruppe** stå tomme.</span><span class="sxs-lookup"><span data-stu-id="e1403-123">Leave the **Gen. Posting Type**, and either the **Tax Bus. Posting Group** or **VAT Bus. Posting Group** fields blank.</span></span> <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->  
  
<span data-ttu-id="e1403-124">Du kan nu knytte fakturaafrundingskontoen til bogføringsgrupper på siden **Kreditorbogføringsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="e1403-124">Now you can assign the invoice rounding account to posting groups on the **Vendor Posting Groups** page.</span></span>  <!-- Why only the vendor posting groups? -->

## <a name="set-up-rounding-for-foreign-and-local-currencies"></a><span data-ttu-id="e1403-125">Oprette afrunding for fremmed og lokal valuta</span><span class="sxs-lookup"><span data-stu-id="e1403-125">Set up rounding for foreign and local currencies</span></span>
<span data-ttu-id="e1403-126">Før du kan bruge den automatiske fakturaafrundingsfunktion, skal du oprette afrundingsregler for fremmed og lokal valuta.</span><span class="sxs-lookup"><span data-stu-id="e1403-126">Before you can use the automatic invoice rounding function, you must set up rounding rules for foreign and local currencies.</span></span>

### <a name="to-set-up-rounding-for-foreign-currencies"></a><span data-ttu-id="e1403-127">Sådan oprettes afrundingsregler for fremmed valuta</span><span class="sxs-lookup"><span data-stu-id="e1403-127">To set up rounding for foreign currencies</span></span>  
1. <span data-ttu-id="e1403-128">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Valutaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="e1403-128">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currencies**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e1403-129">På siden **Valutaer** skal du vælge den udenlandske valuta for at åbne **Valutakort**, og udfyld derefter felterne **Afrundingspræcision**, **Pris-afrundingspræcision**, **Fakturaafrundingspræcision** og **Fakturaafrundingsretning**.</span><span class="sxs-lookup"><span data-stu-id="e1403-129">On the **Currencies** page, choose the foreign currency to open the **Currency Card**, and then fill in the **Amount Rounding Precision**, **Unit-Amount Rounding Precision**, **Invoice Rounding Precision** and **Invoice Rounding Type** fields.</span></span>
  
### <a name="to-set-up-rounding-for-your-local-currency"></a><span data-ttu-id="e1403-130">Sådan oprettes afrunding for lokal valuta</span><span class="sxs-lookup"><span data-stu-id="e1403-130">To set up rounding for your local currency</span></span>
1. <span data-ttu-id="e1403-131">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opsætning af Finans**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="e1403-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Ledger Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e1403-132">På siden **Opsætning af Finans** på oversigtspanelet **Generelt** skal du udfylde feltet **Fakturaafrundingspræcision** og **Fakturaafrundningsretning**.</span><span class="sxs-lookup"><span data-stu-id="e1403-132">On the **General Ledger Setup** page, on the **General** FastTab, fill in the **Inv. Rounding Precision** and **Inv. Rounding Type** fields.</span></span>  

## <a name="activate-the-invoice-rounding-function"></a><span data-ttu-id="e1403-133">Aktivere fakturaafrundingsfunktionen</span><span class="sxs-lookup"><span data-stu-id="e1403-133">Activate the invoice rounding function</span></span>  
<span data-ttu-id="e1403-134">For at sikre, at salgs- og købsfakturaer afrundes automatisk, skal du aktivere fakturaafrundingsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="e1403-134">To ensure that sales and purchase invoices are rounded automatically, you must activate the invoice rounding function.</span></span> <span data-ttu-id="e1403-135">Du aktiverer fakturaafrunding separat for salgs- og købsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="e1403-135">You activate invoice rounding separately for sales and purchase invoices.</span></span>

1. <span data-ttu-id="e1403-136">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsopsætning** eller **Købsopsætning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="e1403-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales & Receivables Setup** or **Purchases & Payables Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e1403-137">På oversigtspanelet **Generelt** skal du vælge afkrydsningsfeltet **Fakturaafrunding**.</span><span class="sxs-lookup"><span data-stu-id="e1403-137">On the **General** FastTab, choose the **Invoice Rounding** check box.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e1403-138">Se også</span><span class="sxs-lookup"><span data-stu-id="e1403-138">See Also</span></span>  
[<span data-ttu-id="e1403-139">Fakturere salg</span><span class="sxs-lookup"><span data-stu-id="e1403-139">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="e1403-140">Registrere køb</span><span class="sxs-lookup"><span data-stu-id="e1403-140">Record Purchases</span></span>](purchasing-how-record-purchases.md)
