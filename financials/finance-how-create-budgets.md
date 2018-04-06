---
title: Oprette finansbudgetter | Microsoft Docs
description: Beskriver, hvordan du opretter finansbudgetter for at estimere forskellige finansielle aktiviteter og tildele dimensioner i forbindelse med business intelligence.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f6969d05cfde9ba7ce5767a961d4af1c7b3bd983
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="create-gl-budgets"></a><span data-ttu-id="50f6b-103">Oprette finansbudgetter</span><span class="sxs-lookup"><span data-stu-id="50f6b-103">Create G/L Budgets</span></span>
<span data-ttu-id="50f6b-104">Du kan have flere budgetter for identiske tidsperioder ved at oprette budgetter med separate navne.</span><span class="sxs-lookup"><span data-stu-id="50f6b-104">You can have multiple budgets for identical time periods by creating budgets with separate names.</span></span> <span data-ttu-id="50f6b-105">Ført opretter du budgetnavnene og angiver budgettal.</span><span class="sxs-lookup"><span data-stu-id="50f6b-105">First, you set up the budget name and enter the budget figures.</span></span> <span data-ttu-id="50f6b-106">Derefter medtages budgetnavnene på alle de budgetposter, du opretter.</span><span class="sxs-lookup"><span data-stu-id="50f6b-106">The budget name is then included on all the budget entries you create.</span></span>  

 <span data-ttu-id="50f6b-107">Når du opretter et budget, kan du definere fire dimensioner for hvert budget.</span><span class="sxs-lookup"><span data-stu-id="50f6b-107">When you create a budget, you can define four dimensions for each budget.</span></span> <span data-ttu-id="50f6b-108">Disse budgetspecifikke dimensioner kaldes budgetdimensioner.</span><span class="sxs-lookup"><span data-stu-id="50f6b-108">These budget-specific dimensions are called budget dimensions.</span></span> <span data-ttu-id="50f6b-109">Du kan vælge budgetdimensioner fra hvert budget blandt de dimensioner, du allerede har oprettet.</span><span class="sxs-lookup"><span data-stu-id="50f6b-109">You select the budget dimensions for each budget from among the dimensions you have already set up.</span></span> <span data-ttu-id="50f6b-110">Budgetdimensioner kan bruges til at angive filtre for et budget og til at tilføje dimensionsoplysninger til budgetposter.</span><span class="sxs-lookup"><span data-stu-id="50f6b-110">Budget dimensions can be used to set filters on a budget and to add dimension information to budget entries.</span></span> <span data-ttu-id="50f6b-111">Du kan finde flere oplysninger i [Arbejde med dimensioner](finance-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="50f6b-111">For more information, see [Working with Dimensions](finance-dimensions.md).</span></span>

 <span data-ttu-id="50f6b-112">Budgetter spiller en vigtig rolle i business intelligence, f.eks. i finansregnskab, der er baseret på kontoplaner, der indeholder budgetposter, eller når du analyserer budgetterede vs. faktiske beløb i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="50f6b-112">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="50f6b-113">Du kan finde flere oplysninger i [Business Intelligence](bi.md).</span><span class="sxs-lookup"><span data-stu-id="50f6b-113">For more information, see [Business Intelligence](bi.md).</span></span>

 <span data-ttu-id="50f6b-114">Budgetter spiller en vigtig rolle i business intelligence, f.eks. i finansregnskab, der er baseret på kontoplaner, der indeholder budgetposter, eller når du analyserer budgetterede vs. faktiske beløb i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="50f6b-114">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="50f6b-115">Du kan finde flere oplysninger i [Business Intelligence](bi.md).</span><span class="sxs-lookup"><span data-stu-id="50f6b-115">For more information, see [Business Intelligence](bi.md).</span></span>

<span data-ttu-id="50f6b-116">I Omkostningsberegning arbejder du med omkostningsbudgetter på samme måde.</span><span class="sxs-lookup"><span data-stu-id="50f6b-116">In cost accounting, you work with cost budgets in a similar way.</span></span> <span data-ttu-id="50f6b-117">Du kan finde flere oplysninger i [Oprette omkostningsbudgetter](finance-create-cost-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="50f6b-117">For more information, see [Creating Cost Budgets](finance-create-cost-budgets.md).</span></span>    

## <a name="to-create-a-new-gl-budget"></a><span data-ttu-id="50f6b-118">Sådan oprettes et nyt finansbudget</span><span class="sxs-lookup"><span data-stu-id="50f6b-118">To create a new G/L budget</span></span>  
1. <span data-ttu-id="50f6b-119">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finansbudgetter**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="50f6b-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **G/L Budgets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="50f6b-120">Vælg handlingen **Rediger liste**, og udfyld derefter felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="50f6b-120">Choose the **Edit List** action, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="50f6b-121">Vælg handlingen **Rediger budget**.</span><span class="sxs-lookup"><span data-stu-id="50f6b-121">Choose the **Edit Budget** action.</span></span>
4. <span data-ttu-id="50f6b-122">Øverst i vinduet **Budget** skal du udfylde felterne efter behov for at definere, hvad der vises.</span><span class="sxs-lookup"><span data-stu-id="50f6b-122">At the top of the **Budget** window, fill in the fields as necessary to define what is displayed.</span></span>  

    <span data-ttu-id="50f6b-123">Kun de poster, der indeholder det budgetnavn, du har angivet i feltet **Budgetnavn** vises.</span><span class="sxs-lookup"><span data-stu-id="50f6b-123">Only entries that contain the budget name that you entered in the **budget Name** field are shown.</span></span> <span data-ttu-id="50f6b-124">Fordi budgetnavnet lige er oprettet, er der ikke nogen poster, der passer til filtret.</span><span class="sxs-lookup"><span data-stu-id="50f6b-124">Because the budget name has just been created, there are no entries that match the filter.</span></span> <span data-ttu-id="50f6b-125">Vinduet er derfor tomt.</span><span class="sxs-lookup"><span data-stu-id="50f6b-125">Therefore, the window is empty.</span></span>  
5. <span data-ttu-id="50f6b-126">Angiv et beløb ved at vælge den relevante celle i matrixen.</span><span class="sxs-lookup"><span data-stu-id="50f6b-126">To enter an amount, choose the relevant cell in the matrix.</span></span> <span data-ttu-id="50f6b-127">Vinduet **Finansbudgetposter** åbnes.</span><span class="sxs-lookup"><span data-stu-id="50f6b-127">The **G/L Budget Entries** window opens.</span></span>  
6. <span data-ttu-id="50f6b-128">Opret en ny linje, og udfyld feltet **Beløb**.</span><span class="sxs-lookup"><span data-stu-id="50f6b-128">Create a new line and fill in the **Amount** field.</span></span> <span data-ttu-id="50f6b-129">Luk vinduet **Finansbudgetposter**.</span><span class="sxs-lookup"><span data-stu-id="50f6b-129">Close the **G/L Budget Entries** window.</span></span>  
7. <span data-ttu-id="50f6b-130">Gentag trin 5 og 6, indtil du har indtastet alle budgetbeløbene.</span><span class="sxs-lookup"><span data-stu-id="50f6b-130">Repeat steps 5 and 6 until you have entered all of the budget amounts.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="50f6b-131">I oversigtspanelet **Filtre** kan du filtrere budgetoplysningerne efter de budgetdimensioner, du har oprettet under budgetnavnet.</span><span class="sxs-lookup"><span data-stu-id="50f6b-131">On the **Filters** FastTab, you can filter the budget information by budget dimensions you have set up under the budget name.</span></span>   

## <a name="see-also"></a><span data-ttu-id="50f6b-132">Se også</span><span class="sxs-lookup"><span data-stu-id="50f6b-132">See Also</span></span>
[<span data-ttu-id="50f6b-133">Finans</span><span class="sxs-lookup"><span data-stu-id="50f6b-133">Finance</span></span>](finance.md)  
[<span data-ttu-id="50f6b-134">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="50f6b-134">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="50f6b-135">Konfigurere Finans</span><span class="sxs-lookup"><span data-stu-id="50f6b-135">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="50f6b-136">Finans- og kontoplanen</span><span class="sxs-lookup"><span data-stu-id="50f6b-136">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="50f6b-137">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="50f6b-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

