---
title: "Administrere anlægsbudgetter | Microsoft Docs"
description: "Du kan oprette oplysninger om fremtidige investeringer, salg og afskrivning på anlægsaktiver for at forberede budgetter og prognoser."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: forecast
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: 0c798fca44d9c57e38e5bb3f930e773d12b69636
ms.contentlocale: da-dk
ms.lasthandoff: 04/16/2018

---
# <a name="manage-budgets-for-fixed-assets"></a><span data-ttu-id="53fae-103">Administrere budgetter for anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="53fae-103">Manage Budgets for Fixed Assets</span></span>
<span data-ttu-id="53fae-104">Du kan konfigurere budgetterede anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="53fae-104">You can set up budgeted fixed assets.</span></span> <span data-ttu-id="53fae-105">Du kan f.eks. inkludere forventede anskaffelser og salg i rapporterne.</span><span class="sxs-lookup"><span data-stu-id="53fae-105">For example, this lets you include anticipated acquisitions and sales in reports.</span></span>  

<span data-ttu-id="53fae-106">Hvis du vil forberede din budgetterede resultatopgørelse, balance og kontantbudget, skal du bruge oplysninger om fremtidige investeringer, salg og afskrivning på anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="53fae-106">To prepare your budgeted income statement, budgeted balance sheet, and cash budget, you need information about future investments, disposals and depreciation of fixed assets.</span></span> <span data-ttu-id="53fae-107">Du kan få disse oplysninger fra rapporten **Anlæg - forventet værdi**.</span><span class="sxs-lookup"><span data-stu-id="53fae-107">You can get this information from the **Fixed Asset - Projected Value** report.</span></span> <span data-ttu-id="53fae-108">Inden du udskriver rapporten, skal du have forberedt budgettet.</span><span class="sxs-lookup"><span data-stu-id="53fae-108">Before you print this report, you must prepare the budget.</span></span>  

## <a name="to-budget-the-acquisition-cost-of-a-fixed-asset"></a><span data-ttu-id="53fae-109">Sådan budgetteres anskaffelsesprisen for et anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="53fae-109">To budget the acquisition cost of a fixed asset</span></span>
<span data-ttu-id="53fae-110">Når du skal forberede et budget, skal du oprette anlægskort for de anlægsaktiver, du har planlagt at købe.</span><span class="sxs-lookup"><span data-stu-id="53fae-110">To prepare a budget, you have to set up fixed asset cards for fixed assets that you intend to buy in the future.</span></span> <span data-ttu-id="53fae-111">De budgetterede anlægsaktiver oprettes som almindelige anlægsaktiver, men de skal være angivet til ikke at blive bogført i finansregnskabet.</span><span class="sxs-lookup"><span data-stu-id="53fae-111">The budget fixed assets are set up as ordinary fixed assets, but it must be set up to not post to the general ledger.</span></span>

<span data-ttu-id="53fae-112">Når du bogfører anskaffelsesprisen, skal du angive nummeret på det budgetterede anlægsaktiv i feltet **Budgetanlægsnr.**</span><span class="sxs-lookup"><span data-stu-id="53fae-112">When you post the acquisition cost, you enter the number of the budgeted fixed asset in the **Budgeted FA No.** field.</span></span> <span data-ttu-id="53fae-113">Dermed bogføres automatisk en anskaffelsespris med modsat fortegn for budgetanlægget.</span><span class="sxs-lookup"><span data-stu-id="53fae-113">This will post an acquisition cost with an opposite sign for the budgeted asset.</span></span> <span data-ttu-id="53fae-114">Det betyder, at de samlede anskaffelsesomkostninger for budgetanlægget er forskellen mellem den budgetterede og den faktiske anskaffelsesomkostning.</span><span class="sxs-lookup"><span data-stu-id="53fae-114">This means that the total acquisition cost on the budgeted asset is the difference between the budgeted and the actual acquisition cost.</span></span>

1. <span data-ttu-id="53fae-115">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlægsaktiver**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="53fae-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="53fae-116">Vælg handlingen **Ny** for at oprette et nyt anlægskort for det budgetterede anlægsaktiv.</span><span class="sxs-lookup"><span data-stu-id="53fae-116">Choose the **New** action to create a new fixed asset card for the budgeted fixed asset.</span></span>
3. <span data-ttu-id="53fae-117">Markér afkrydsningsfeltet **Budgetanlæg** for at forhindre bogføring i finansregnskabet.</span><span class="sxs-lookup"><span data-stu-id="53fae-117">Select the **Budgeted Asset** check box to prevent posting to the general ledger.</span></span>
4. <span data-ttu-id="53fae-118">Udfyld resten af felterne, tildel en afskrivningsprofil, og bogfør derefter den første anskaffelsespris for det budgetterede anlægsaktiv, der er angivet i feltet **Budgetanlægsnr.** på kladdelinjen</span><span class="sxs-lookup"><span data-stu-id="53fae-118">Fill in the remaining fields, assign a depreciation book, and then post the first acquisition cost with the budgeted fixed asset entered in the **Budgeted FA No.** field on the journal line.</span></span> <span data-ttu-id="53fae-119">Du kan finde flere oplysninger i [Anskaffe anlægsaktiver](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="53fae-119">For more information, see [Acquire Fixed Assets](fa-how-acquire.md).</span></span>

## <a name="to-budget-the-disposal-of-a-fixed-asset"></a><span data-ttu-id="53fae-120">Sådan budgetteres salget af et anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="53fae-120">To budget the disposal of a fixed asset</span></span>
<span data-ttu-id="53fae-121">Hvis du planlægger at sælge anlæg inden for budgetperioden, kan du angive oplysninger om salgspris og -dato.</span><span class="sxs-lookup"><span data-stu-id="53fae-121">If you plan to sell assets within the budget period, you can enter information about sales price and sales date.</span></span>

1. <span data-ttu-id="53fae-122">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlægsaktiver**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="53fae-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="53fae-123">Vælg det anlægsaktiv, der skal sælges, og vælg derefter handlingen **Afskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="53fae-123">Select the fixed asset to be disposed of, and then choose the **Depreciation Books** action.</span></span>
3. <span data-ttu-id="53fae-124">I vinduet **Anlægsafskrivningsprofiler** skal du udfylde felterne **Forventet salgsdato** og **Forventet salgspris**.</span><span class="sxs-lookup"><span data-stu-id="53fae-124">In the **FA Depreciation Books** window, fill in the **Projected Disposal Date** and **Projected Proceeds on Disposal** fields.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-projected-disposal-values"></a><span data-ttu-id="53fae-125">Sådan vises forventede salgsværdier</span><span class="sxs-lookup"><span data-stu-id="53fae-125">To view projected disposal values</span></span>
<span data-ttu-id="53fae-126">Hvis du vil have vist de forventede salgsværdier og beregne gevinst eller tab, kan du bruge rapporten **Anlæg - forventet værdi**.</span><span class="sxs-lookup"><span data-stu-id="53fae-126">To see the projected disposal values and have the gain and loss calculated, you can use the **FA Projected Value** report.</span></span>

1. <span data-ttu-id="53fae-127">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlæg - forventet værdi**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="53fae-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA Projected Value**, and then choose the related link.</span></span>
2. <span data-ttu-id="53fae-128">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="53fae-128">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="53fae-129">Vælg knappen **Udskriv** eller **Vis udskrift**.</span><span class="sxs-lookup"><span data-stu-id="53fae-129">Choose the **Print** or **Preview** button.</span></span>

## <a name="to-budget-depreciation"></a><span data-ttu-id="53fae-130">Sådan budgetteres afskrivning</span><span class="sxs-lookup"><span data-stu-id="53fae-130">To budget depreciation</span></span>
<span data-ttu-id="53fae-131">Du kan bruge rapporten **Anlæg - forventet værdi** til at beregne den fremtidige afskrivning.</span><span class="sxs-lookup"><span data-stu-id="53fae-131">You can use the **Fixed Asset - Projected Value** report to calculate future depreciation.</span></span> <span data-ttu-id="53fae-132">I rapporten vises bogført værdi og akkumuleret afskrivning i starten af den valgte periode og ved ændringer i løbet af perioden, og den bogførte værdi og den akkumulerede afskrivning vises ved slutningen af den valgte periode.</span><span class="sxs-lookup"><span data-stu-id="53fae-132">The report shows the book value and accumulated depreciation at the start of the selected period, changes during the period, and the book value and accumulated depreciation at the end of the selected period.</span></span>

1. <span data-ttu-id="53fae-133">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlæg - forventet værdi**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="53fae-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA Projected Value**, and then choose the related link.</span></span>
2. <span data-ttu-id="53fae-134">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="53fae-134">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="53fae-135">Hvis du vil have vist de samlede værdier for alle aktiver, skal du rydde afkrydsningsfeltet **Udskrift pr. anlæg**.</span><span class="sxs-lookup"><span data-stu-id="53fae-135">To see total values for all assets, clear the **Print per Fixed Asset** check box.</span></span>
4. <span data-ttu-id="53fae-136">Lad oversigtspanelet **Anlæg** stå tomt, hvis alle anlægsaktiver skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="53fae-136">Leave the **Fixed Asset** FastTab blank to have all assets included.</span></span> <span data-ttu-id="53fae-137">I feltet **Budgetanlæg** skal du angive **Nej** for at udelukke budgetanlæg eller **Ja** for kun at få vist budgetanlæg.</span><span class="sxs-lookup"><span data-stu-id="53fae-137">In the **Budgeted Asset** field, enter **No** to exclude budgeted assets or **Yes** to see budgeted assets only.</span></span>
5. <span data-ttu-id="53fae-138">Vælg knappen **Udskriv** eller **Vis udskrift**.</span><span class="sxs-lookup"><span data-stu-id="53fae-138">Choose the **Print** or **Preview** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="53fae-139">Se også</span><span class="sxs-lookup"><span data-stu-id="53fae-139">See Also</span></span>
[<span data-ttu-id="53fae-140">Anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="53fae-140">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="53fae-141">Opsætning af anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="53fae-141">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="53fae-142">Finans</span><span class="sxs-lookup"><span data-stu-id="53fae-142">Finance</span></span>](finance.md)  
<span data-ttu-id="53fae-143">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="53fae-143">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="53fae-144">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="53fae-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

