---
title: Oprette omkostningsbudgetter | Microsoft Docs
description: Dette emne indeholder en oversigt over, hvor du kan oprette og analysere omkostningsbudgetter.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: cfe0eed4090ef458e774da8d0bc03910247570d7
ms.openlocfilehash: 19fbfd60beb973dc65a09b7bfeee95b976a89905
ms.contentlocale: da-dk
ms.lasthandoff: 12/14/2017

---
# <a name="creating-cost-budgets"></a><span data-ttu-id="14b60-103">Oprette omkostningsbudgetter</span><span class="sxs-lookup"><span data-stu-id="14b60-103">Creating Cost Budgets</span></span>
<span data-ttu-id="14b60-104">Budgettering i omkostningsregnskab minder om budgettering i regnskabet.</span><span class="sxs-lookup"><span data-stu-id="14b60-104">Budgeting in cost accounting resembles budgeting in the general ledger.</span></span> <span data-ttu-id="14b60-105">Et omkostningsbudget oprettes baseret på omkostningstyper, ligesom et budget for regnskabet oprettes baseret på finanskonti.</span><span class="sxs-lookup"><span data-stu-id="14b60-105">A cost budget is created based on cost types just as a budget for the general ledger is created based on general ledger accounts.</span></span>  

<span data-ttu-id="14b60-106">Et omkostningsbudget oprettes for en bestemt periode, f.eks. et regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="14b60-106">A cost budget is created for a certain period of time, for example, a fiscal year.</span></span> <span data-ttu-id="14b60-107">Du kan oprette lige så mange omkostningsbudgetter, der er behov for.</span><span class="sxs-lookup"><span data-stu-id="14b60-107">You can create as many cost budgets as needed.</span></span> <span data-ttu-id="14b60-108">Du kan oprette et nyt omkostningsbudget manuelt eller ved at importere et omkostningsbudget eller ved at kopiere et eksisterende omkostningsbudget som basis for budgettet.</span><span class="sxs-lookup"><span data-stu-id="14b60-108">You can create a new cost budget manually, or by importing a cost budget, or by copying an existing cost budget as the budget base.</span></span> <span data-ttu-id="14b60-109">Du kan finde flere oplysninger i [Fremgangsmåde: Oprette finansbudgetter](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="14b60-109">For more information, see [How to: Create G/L Budgets](finance-how-create-budgets.md).</span></span>

<span data-ttu-id="14b60-110">Brug følgende vinduer til at oprette og analysere omkostningsbudgetter.</span><span class="sxs-lookup"><span data-stu-id="14b60-110">You use the following windows to create and analyze cost budgets.</span></span> <span data-ttu-id="14b60-111">Vælg ikonet ![Søg efter side eller en rapport](media/ui-search/search_small.png "ikonet Søg efter side eller en rapport") for at finde et vindue, og læs værktøjstippet for hver.</span><span class="sxs-lookup"><span data-stu-id="14b60-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon to find a window, and then read the tooltip for each.</span></span>

|<span data-ttu-id="14b60-112">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="14b60-112">To</span></span>|<span data-ttu-id="14b60-113">Se</span><span class="sxs-lookup"><span data-stu-id="14b60-113">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="14b60-114">Overføre budgetter fra regnskabet.</span><span class="sxs-lookup"><span data-stu-id="14b60-114">Transfer budgets from the general ledger.</span></span>|<span data-ttu-id="14b60-115">Kørslen **Kopier finansbudget til omk.regnskab**</span><span class="sxs-lookup"><span data-stu-id="14b60-115">**Copy G-L Budget to Cost Acctg.** batch job</span></span>|  
|<span data-ttu-id="14b60-116">Kopiere omkostningsbudgetter.</span><span class="sxs-lookup"><span data-stu-id="14b60-116">Copy cost budgets.</span></span>|<span data-ttu-id="14b60-117">Kørslen **Kopier omkostningsbudget**</span><span class="sxs-lookup"><span data-stu-id="14b60-117">**Copy Cost Budget** batch job</span></span>|  
|<span data-ttu-id="14b60-118">Fordele budgetter.</span><span class="sxs-lookup"><span data-stu-id="14b60-118">Allocate budgets.</span></span>|<span data-ttu-id="14b60-119">Siden **Omkostningsfordeling**</span><span class="sxs-lookup"><span data-stu-id="14b60-119">**Cost Allocation** page</span></span>|  
|<span data-ttu-id="14b60-120">Se omkostningsbudgetregistre og omkostningsbudgetposter.</span><span class="sxs-lookup"><span data-stu-id="14b60-120">See cost budget registers and cost budget entries.</span></span>|<span data-ttu-id="14b60-121">Siden **Omkostningsbudgetregistre**</span><span class="sxs-lookup"><span data-stu-id="14b60-121">**Cost Budget Registers** page</span></span>|  
|<span data-ttu-id="14b60-122">Udskrive omkostningsbudgetsammenligninger med forskellige rapporter.</span><span class="sxs-lookup"><span data-stu-id="14b60-122">Print cost budget comparisons using various reports.</span></span>|<span data-ttu-id="14b60-123">Rapporten **Omk.regnskabssaldo/budget**</span><span class="sxs-lookup"><span data-stu-id="14b60-123">**Cost Acctg. Balance-Budget** report</span></span><br /><br /> <span data-ttu-id="14b60-124">Rapporten **Omk.regnskabskontoudtog/budget**</span><span class="sxs-lookup"><span data-stu-id="14b60-124">**Cost Acctg. Statement-Budget** report</span></span><br /><br /> <span data-ttu-id="14b60-125">Rapporten **Omkostningsbudget efter omkostningssted**</span><span class="sxs-lookup"><span data-stu-id="14b60-125">**Cost Budget by Cost Center** report</span></span><br /><br /> <span data-ttu-id="14b60-126">Rapporten **Omkostningsbudget efter omkostningsemne**</span><span class="sxs-lookup"><span data-stu-id="14b60-126">**Cost Budget by Cost Object** report</span></span>|  

## <a name="see-also"></a><span data-ttu-id="14b60-127">Se også</span><span class="sxs-lookup"><span data-stu-id="14b60-127">See Also</span></span>  
[<span data-ttu-id="14b60-128">Regnskab for omkostninger</span><span class="sxs-lookup"><span data-stu-id="14b60-128">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
[<span data-ttu-id="14b60-129">Fremgangsmåde: Oprette finansbudgetter</span><span class="sxs-lookup"><span data-stu-id="14b60-129">How to: Create G/L Budgets</span></span>](finance-how-create-budgets.md)  
<span data-ttu-id="14b60-130">[Terminologi i omkostningsregnskab](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="14b60-130">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="14b60-131">Definere og allokere omkostninger</span><span class="sxs-lookup"><span data-stu-id="14b60-131">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)  
<span data-ttu-id="14b60-132">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="14b60-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

