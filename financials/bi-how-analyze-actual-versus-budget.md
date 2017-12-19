---
title: Analysere faktisk kontra budget | Microsoft Docs
description: "Bruges til at analysere faktiske beløb sammenlignet med budgetterede beløb."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 12/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: cfe0eed4090ef458e774da8d0bc03910247570d7
ms.openlocfilehash: e76d590476b1236bf1d82a7f5e4f502ffdd9d02d
ms.contentlocale: da-dk
ms.lasthandoff: 12/14/2017

---
# <a name="how-to-analyze-actual-amounts-versus-budgeted-amounts"></a><span data-ttu-id="d6f26-103">Fremgangsmåde: Analysere faktiske beløb sammenlignet med budgetterede beløb</span><span class="sxs-lookup"><span data-stu-id="d6f26-103">How to: Analyze Actual Amounts Versus Budgeted Amounts</span></span>
<span data-ttu-id="d6f26-104">Som et led i indsamling, analyse og deling af virksomhedens data kan du få vist faktiske beløb sammenlignet med budgetterede beløb for alle konti og for flere perioder.</span><span class="sxs-lookup"><span data-stu-id="d6f26-104">As a part of gathering, analyzing, and sharing your company data, you view actual amounts compared to budgeted amounts for all accounts and for several periods.</span></span>

<span data-ttu-id="d6f26-105">Hvis du vil analysere budgetterede beløb, skal du først oprette finansbudgetter.</span><span class="sxs-lookup"><span data-stu-id="d6f26-105">To analyze budgeted amounts, you must first create G(L budgets.</span></span> <span data-ttu-id="d6f26-106">Du kan finde flere oplysninger i [Fremgangsmåde: Oprette finansbudgetter](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="d6f26-106">For more information, see [How to: Create G/L Budgets](finance-how-create-budgets.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="d6f26-107">Denne funktion kræver, at oplevelsen er indstillet til **Suite**.</span><span class="sxs-lookup"><span data-stu-id="d6f26-107">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="d6f26-108">Du kan finde flere oplysninger under [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="d6f26-108">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-view-a-gl-budget"></a><span data-ttu-id="d6f26-109">Sådan får du vist et finansbudget</span><span class="sxs-lookup"><span data-stu-id="d6f26-109">To view a G/L budget</span></span>
<span data-ttu-id="d6f26-110">budget med dimensioner kan du filtrere poster og få vist et bestemt budget.</span><span class="sxs-lookup"><span data-stu-id="d6f26-110">In a budget with dimensions, you can filter the entries and see specific budgets.</span></span>

1. <span data-ttu-id="d6f26-111">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finansbudgetter**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d6f26-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **G/L Budgets**, and then choose the related link.</span></span>
2. <span data-ttu-id="d6f26-112">I vinduet **Finansbudgetter** skal du åbne det budget, du ønsker at få vist.</span><span class="sxs-lookup"><span data-stu-id="d6f26-112">In the **G/L Budgets** window, open the budget that you want to view.</span></span>  
3. <span data-ttu-id="d6f26-113">Øverst i vinduet skal du udfylde felterne efter behov for at definere, hvad der vises.</span><span class="sxs-lookup"><span data-stu-id="d6f26-113">At the top of the window, fill in the fields as necessary to define what is shown.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="d6f26-114">Hvis du har valgt **Periode** i feltet **Vis som linjer** eller feltet **Vis som kolonner**, skal du udfylde feltet **Vis efter**.</span><span class="sxs-lookup"><span data-stu-id="d6f26-114">If you have selected **Period** in either the **Show as Lines** or the **Show as Columns** field, then you must fill in the **View by** field.</span></span> <span data-ttu-id="d6f26-115">Hvis du ikke har valgt **Periode** i feltet **Vis som linjer** eller **Vis som kolonner**, skal du angive den relevante periode i feltet **Datofilter**.</span><span class="sxs-lookup"><span data-stu-id="d6f26-115">If you have not selected **Period** in either the **Show as Lines** or **Show as Columns** field, then enter the appropriate period in **Date Filter** field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="d6f26-116">Kun poster i finansbudgettet med de filterkoder, du har angivet i oversigtspanelet **Filtre**, medtages i beregningen.</span><span class="sxs-lookup"><span data-stu-id="d6f26-116">Only entries from the general ledger budget with the filter codes that you enter on the **Filters** FastTab are included in the calculation.</span></span> <span data-ttu-id="d6f26-117">Budgetposter med andre filterkoder eller uden filterkoder medtages ikke.</span><span class="sxs-lookup"><span data-stu-id="d6f26-117">Budget entries with other filter codes or without any filter codes are not included.</span></span> <span data-ttu-id="d6f26-118">Så længe filtret bliver i vinduet, vises budgettet kun med de budgetposter, der har disse filterkoder.</span><span class="sxs-lookup"><span data-stu-id="d6f26-118">As long as the filter remains on the window, the budget only displays the budget entries with these filter codes.</span></span>  

> [!TIP]  
>   <span data-ttu-id="d6f26-119">Hvis du vil ændre budgettet, kan du redigere budgetposterne.</span><span class="sxs-lookup"><span data-stu-id="d6f26-119">If you want to modify the budget, you can modify the budget entries.</span></span> <span data-ttu-id="d6f26-120">Vælg et beløb for at få vist de underliggende finansbudgetposter.</span><span class="sxs-lookup"><span data-stu-id="d6f26-120">Choose an amount to view the underlying general ledger budget entries.</span></span>

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a><span data-ttu-id="d6f26-121">Sådan får du vist aktuelle og budgetterede beløb for alle konti</span><span class="sxs-lookup"><span data-stu-id="d6f26-121">To view actual and budgeted amounts for all accounts</span></span>  
<span data-ttu-id="d6f26-122">Du kan få vist finansbudgetter og sammenligne dem med faktiske tal i flere områder af [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d6f26-122">You can view general ledger budgets and compare them with actual figures in several areas of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

1. <span data-ttu-id="d6f26-123">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoplan**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d6f26-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d6f26-124">I vinduet **Kontoplan** skal du vælge handlingen **Finans - saldi/budget**.</span><span class="sxs-lookup"><span data-stu-id="d6f26-124">In the **Chart of Accounts** window, choose the **G/L Balance/Budget** action.</span></span>
3. <span data-ttu-id="d6f26-125">Øverst i vinduet skal du udfylde felterne efter behov for at definere, hvad der vises.</span><span class="sxs-lookup"><span data-stu-id="d6f26-125">At the top of the window, fill in the fields as necessary to define what is shown.</span></span>  
4. <span data-ttu-id="d6f26-126">Vælg feltet, hvis du vil se en specifikation, der udgør det viste beløb.</span><span class="sxs-lookup"><span data-stu-id="d6f26-126">To see a specification that makes up the amount shown, choose the field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="d6f26-127">Det filter, du har angivet i vinduets hoved, anvendes til både finans- og budgetposter.</span><span class="sxs-lookup"><span data-stu-id="d6f26-127">The filters you set in the window header will be applied to general ledger entries and also budget entries.</span></span>

<span data-ttu-id="d6f26-128">Den venstre kolonne indeholder kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="d6f26-128">The leftmost columns contain the chart of accounts.</span></span> <span data-ttu-id="d6f26-129">Af de fem kolonner i højre side, viser de første fire kolonner aktuelle budgetterede debet- og kreditbeløb for hver konto.</span><span class="sxs-lookup"><span data-stu-id="d6f26-129">Of the five columns on the rightmost side, the first four columns show actual and budgeted debit and credit amounts for each account.</span></span> <span data-ttu-id="d6f26-130">Den femte kolonne viser den proportionale relation mellem de aktuelle og de budgetterede beløb på finanskontoen.</span><span class="sxs-lookup"><span data-stu-id="d6f26-130">The fifth column shows the proportional relationship between the actual and the budgeted amounts on the general ledger account.</span></span>  

> [!TIP]  
>   <span data-ttu-id="d6f26-131">Brug feltet **Vis efter** i vinduet **Finans - saldi/budget** til at vælge periodelængden.</span><span class="sxs-lookup"><span data-stu-id="d6f26-131">Use the **View by** field in the **G/L Balance/Budget** window to select the period length.</span></span> <span data-ttu-id="d6f26-132">Brug feltet **Vis som** til at vælge den måde, beløbene beregnes på, **Bevægelse** eller **Saldo til dato**.</span><span class="sxs-lookup"><span data-stu-id="d6f26-132">Use the **View as** field to select the way the amounts will be calculated, **Net Change** or **Balance at Date**.</span></span> <span data-ttu-id="d6f26-133">Vælg handlingen **Forrige periode** eller **Næste periode** for at ændre perioden.</span><span class="sxs-lookup"><span data-stu-id="d6f26-133">Choose the **Previous Period** or **Next Period** action to change the period.</span></span>  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a><span data-ttu-id="d6f26-134">Sådan får du vist aktuelle og budgetterede beløb for flere perioder</span><span class="sxs-lookup"><span data-stu-id="d6f26-134">To view actual and budgeted amounts for several periods</span></span>  
<span data-ttu-id="d6f26-135">Du kan få vist et antal perioder for en enkelt konto i stedet for at få vist aktuelle og budgetterede beløb for alle beløb i en enkelt periode.</span><span class="sxs-lookup"><span data-stu-id="d6f26-135">Instead of viewing the actual and budgeted amounts for all accounts within a single period, you can view a number of periods for a single account.</span></span>  

1. <span data-ttu-id="d6f26-136">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoplan**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d6f26-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d6f26-137">I vinduet **Kontoplan** skal du vælge den relevante finanskonto og derefter vælge handlingen **Finanskonto - saldo/budget**.</span><span class="sxs-lookup"><span data-stu-id="d6f26-137">In the **Chart of Accounts** window, select the relevant general ledger account, and then choose the **G/L Account Balance/Budget** action.</span></span>  
3. <span data-ttu-id="d6f26-138">Øverst i vinduet skal du udfylde felterne efter behov for at definere, hvad der vises.</span><span class="sxs-lookup"><span data-stu-id="d6f26-138">At the top of the window, fill in the fields as necessary to define what is shown.</span></span>   
4. <span data-ttu-id="d6f26-139">Vælg feltet, hvis du vil se en specifikation af et vist beløb.</span><span class="sxs-lookup"><span data-stu-id="d6f26-139">To see a specification of an amount shown, choose the field.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d6f26-140">Se også</span><span class="sxs-lookup"><span data-stu-id="d6f26-140">See Also</span></span>
[<span data-ttu-id="d6f26-141">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="d6f26-141">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="d6f26-142">Fremgangsmåde: Arbejde med kontoskemaer</span><span class="sxs-lookup"><span data-stu-id="d6f26-142">How to: Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
[<span data-ttu-id="d6f26-143">Finans</span><span class="sxs-lookup"><span data-stu-id="d6f26-143">Finance</span></span>](finance.md)  
[<span data-ttu-id="d6f26-144">Konfigurere Finans</span><span class="sxs-lookup"><span data-stu-id="d6f26-144">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="d6f26-145">Finans- og kontoplanen</span><span class="sxs-lookup"><span data-stu-id="d6f26-145">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="d6f26-146">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d6f26-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

