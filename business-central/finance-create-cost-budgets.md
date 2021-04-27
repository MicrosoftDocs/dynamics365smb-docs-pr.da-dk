---
title: Oprette omkostningsbudgetter | Microsoft Docs
description: Dette emne indeholder en oversigt over, hvor du kan oprette og analysere omkostningsbudgetter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: da976e1e8ac2988aa2842925c2b10f4f8515ea47
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785240"
---
# <a name="creating-cost-budgets"></a><span data-ttu-id="a00c0-103">Oprette omkostningsbudgetter</span><span class="sxs-lookup"><span data-stu-id="a00c0-103">Creating Cost Budgets</span></span>
<span data-ttu-id="a00c0-104">Budgettering i omkostningsregnskab minder om budgettering i regnskabet.</span><span class="sxs-lookup"><span data-stu-id="a00c0-104">Budgeting in cost accounting resembles budgeting in the general ledger.</span></span> <span data-ttu-id="a00c0-105">Et omkostningsbudget oprettes baseret på omkostningstyper, ligesom et budget for regnskabet oprettes baseret på finanskonti.</span><span class="sxs-lookup"><span data-stu-id="a00c0-105">A cost budget is created based on cost types just as a budget for the general ledger is created based on general ledger accounts.</span></span>  

<span data-ttu-id="a00c0-106">Et omkostningsbudget oprettes for en bestemt periode, f.eks. et regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="a00c0-106">A cost budget is created for a certain period of time, for example, a fiscal year.</span></span> <span data-ttu-id="a00c0-107">Du kan oprette lige så mange omkostningsbudgetter, der er behov for.</span><span class="sxs-lookup"><span data-stu-id="a00c0-107">You can create as many cost budgets as needed.</span></span> <span data-ttu-id="a00c0-108">Du kan oprette et nyt omkostningsbudget manuelt eller ved at importere et omkostningsbudget eller ved at kopiere et eksisterende omkostningsbudget som basis for budgettet.</span><span class="sxs-lookup"><span data-stu-id="a00c0-108">You can create a new cost budget manually, or by importing a cost budget, or by copying an existing cost budget as the budget base.</span></span> <span data-ttu-id="a00c0-109">Du kan finde flere oplysninger i [Oprette finansbudgetter](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="a00c0-109">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

<span data-ttu-id="a00c0-110">Brug følgende sider til at oprette og analysere omkostningsbudgetter.</span><span class="sxs-lookup"><span data-stu-id="a00c0-110">You use the following pages to create and analyze cost budgets.</span></span> <span data-ttu-id="a00c0-111">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") for at finde en side, og læs derefter værktøjstippet for hvert.</span><span class="sxs-lookup"><span data-stu-id="a00c0-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon to find a page, and then read the tooltip for each.</span></span>

|<span data-ttu-id="a00c0-112">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="a00c0-112">To</span></span>|<span data-ttu-id="a00c0-113">Skal du se</span><span class="sxs-lookup"><span data-stu-id="a00c0-113">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="a00c0-114">Overføre budgetter fra regnskabet.</span><span class="sxs-lookup"><span data-stu-id="a00c0-114">Transfer budgets from the general ledger.</span></span>|<span data-ttu-id="a00c0-115">Kørslen **Kopier finansbudget til omk.regnskab**</span><span class="sxs-lookup"><span data-stu-id="a00c0-115">**Copy G-L Budget to Cost Acctg.** batch job</span></span>|  
|<span data-ttu-id="a00c0-116">Kopiere omkostningsbudgetter.</span><span class="sxs-lookup"><span data-stu-id="a00c0-116">Copy cost budgets.</span></span>|<span data-ttu-id="a00c0-117">Kørslen **Kopier omkostningsbudget**</span><span class="sxs-lookup"><span data-stu-id="a00c0-117">**Copy Cost Budget** batch job</span></span>|  
|<span data-ttu-id="a00c0-118">Fordele budgetter.</span><span class="sxs-lookup"><span data-stu-id="a00c0-118">Allocate budgets.</span></span>|<span data-ttu-id="a00c0-119">Siden **Omkostningsfordeling**</span><span class="sxs-lookup"><span data-stu-id="a00c0-119">**Cost Allocation** page</span></span>|  
|<span data-ttu-id="a00c0-120">Se omkostningsbudgetregistre og omkostningsbudgetposter.</span><span class="sxs-lookup"><span data-stu-id="a00c0-120">See cost budget registers and cost budget entries.</span></span>|<span data-ttu-id="a00c0-121">Siden **Omkostningsbudgetregistre**</span><span class="sxs-lookup"><span data-stu-id="a00c0-121">**Cost Budget Registers** page</span></span>|  
|<span data-ttu-id="a00c0-122">Udskrive omkostningsbudgetsammenligninger med forskellige rapporter.</span><span class="sxs-lookup"><span data-stu-id="a00c0-122">Print cost budget comparisons using various reports.</span></span>|<span data-ttu-id="a00c0-123">Rapporten **Omk.regnskabssaldo/budget**</span><span class="sxs-lookup"><span data-stu-id="a00c0-123">**Cost Acctg. Balance-Budget** report</span></span><br /><br /> <span data-ttu-id="a00c0-124">Rapporten **Omk.regnskabskontoudtog/budget**</span><span class="sxs-lookup"><span data-stu-id="a00c0-124">**Cost Acctg. Statement-Budget** report</span></span><br /><br /> <span data-ttu-id="a00c0-125">Rapporten **Omkostningsbudget efter omkostningssted**</span><span class="sxs-lookup"><span data-stu-id="a00c0-125">**Cost Budget by Cost Center** report</span></span><br /><br /> <span data-ttu-id="a00c0-126">Rapporten **Omkostningsbudget efter omkostningsemne**</span><span class="sxs-lookup"><span data-stu-id="a00c0-126">**Cost Budget by Cost Object** report</span></span>|  

## <a name="see-also"></a><span data-ttu-id="a00c0-127">Se også</span><span class="sxs-lookup"><span data-stu-id="a00c0-127">See Also</span></span>  
[<span data-ttu-id="a00c0-128">Regnskab for omkostninger</span><span class="sxs-lookup"><span data-stu-id="a00c0-128">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
[<span data-ttu-id="a00c0-129">Oprette finansbudgetter</span><span class="sxs-lookup"><span data-stu-id="a00c0-129">Create G/L Budgets</span></span>](finance-how-create-budgets.md)  
<span data-ttu-id="a00c0-130">[Terminologi i omkostningsregnskab](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="a00c0-130">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="a00c0-131">Definere og allokere omkostninger</span><span class="sxs-lookup"><span data-stu-id="a00c0-131">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)  
<span data-ttu-id="a00c0-132">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a00c0-132">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]