---
title: Analyse af pengestrømme | Microsoft Docs
description: Beskriver, hvordan du bruger diagrammerne Kassebeholdningsproces, Indtægter og udgifter, Pengestrøm og Pengestrømsprognose til at analysere tidligere og fremtidige pengestrømme til og fra din virksomhed.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 7bc87f8fc096241e7f77efb0eb4e7bceb1d28aef
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391170"
---
# <a name="analyzing-cash-flow-in-your-company"></a><span data-ttu-id="edba7-103">Analysere pengestrømme i din virksomhed</span><span class="sxs-lookup"><span data-stu-id="edba7-103">Analyzing Cash Flow in Your Company</span></span>
<span data-ttu-id="edba7-104">Diagrammer i rollecenteret Regnskabsmedarbejder giver indsigt, som kan hjælpe dig med at træffe beslutninger vedrørende dine pengestrømme.</span><span class="sxs-lookup"><span data-stu-id="edba7-104">The charts on the Accountant Role Center provide insights that can help you make solid decisions about what to do with your cash.</span></span>  

| <span data-ttu-id="edba7-105">For at besvare spørgsmål som de følgende</span><span class="sxs-lookup"><span data-stu-id="edba7-105">To answer questions like these</span></span> | <span data-ttu-id="edba7-106">Skal du bruge dette diagram</span><span class="sxs-lookup"><span data-stu-id="edba7-106">Use this chart</span></span> |
| --- | --- |
| <span data-ttu-id="edba7-107">Hvor længe lægger salgsprocessen beslag på mine kontanter?</span><span class="sxs-lookup"><span data-stu-id="edba7-107">How long does the sales process tie up my cash?</span></span></br> <span data-ttu-id="edba7-108">Skal jeg øge eller mindske lagerniveauer?</span><span class="sxs-lookup"><span data-stu-id="edba7-108">Should I increase or reduce inventory levels?</span></span> |<span data-ttu-id="edba7-109">Kassebeholdningsproces</span><span class="sxs-lookup"><span data-stu-id="edba7-109">Cash Cycle</span></span> |
| <span data-ttu-id="edba7-110">Hvornår er et pengebeløb ankommet til og har forladt min virksomhed?</span><span class="sxs-lookup"><span data-stu-id="edba7-110">When did cash move in and out of my company?</span></span></br> <span data-ttu-id="edba7-111">Er nogle perioder bedre end andre?</span><span class="sxs-lookup"><span data-stu-id="edba7-111">Are some periods better than others?</span></span> |<span data-ttu-id="edba7-112">Pengestrøm</span><span class="sxs-lookup"><span data-stu-id="edba7-112">Cash Flow</span></span> |
| <span data-ttu-id="edba7-113">Ser tallene negative ud for en periode?</span><span class="sxs-lookup"><span data-stu-id="edba7-113">Do the numbers seem off for a period?</span></span></br> <span data-ttu-id="edba7-114">Skal jeg undersøge det?</span><span class="sxs-lookup"><span data-stu-id="edba7-114">Should I investigate?</span></span> |<span data-ttu-id="edba7-115">Indtægter og udgifter</span><span class="sxs-lookup"><span data-stu-id="edba7-115">Income & Expense</span></span> |
| <span data-ttu-id="edba7-116">Hvornår kan jeg forvente kontante overskud eller underskud?</span><span class="sxs-lookup"><span data-stu-id="edba7-116">When might a cash surplus or deficit happen?</span></span></br> <span data-ttu-id="edba7-117">Skal jeg nedbringe gæld eller låne for at imødegå kommende udgifter?</span><span class="sxs-lookup"><span data-stu-id="edba7-117">Should I pay down debt, or borrow to meet upcoming expenses?</span></span> |<span data-ttu-id="edba7-118">Pengestrømsprognoser</span><span class="sxs-lookup"><span data-stu-id="edba7-118">Cash Flow Forecasts</span></span> |

<span data-ttu-id="edba7-119">I rollecentret Regnskabsmedarbejder under **Finansydeevne** giver diagrammerne **Kassebeholdningsproces**, **Pengestrøm** og **Indtægter og udgifter** dig måder at analysere pengestrømme på:</span><span class="sxs-lookup"><span data-stu-id="edba7-119">On the Accountant Role Center, under **Finance Performance**, the **Cash Cycle**, **Cash Flow**, and **Income & Expense** charts offer ways to analyze cash flow:</span></span>  

* <span data-ttu-id="edba7-120">Få vist tallene i en periode ved hjælp af tidslinjeskyderen.</span><span class="sxs-lookup"><span data-stu-id="edba7-120">See figures for a period by using the timeline slider.</span></span>  
* <span data-ttu-id="edba7-121">Filtrer diagrammet ved at vælge kilden i forklaringen.</span><span class="sxs-lookup"><span data-stu-id="edba7-121">Filter the chart by choosing the source in the legend.</span></span>  
* <span data-ttu-id="edba7-122">Skift tidsrum, eller gå til forrige eller næste periode ved at vælge indstillinger i rullemenuen **Finansydeevne**.</span><span class="sxs-lookup"><span data-stu-id="edba7-122">Change the length of the period, or go to the previous or next period, by choosing options on the **Finance Performance** drop down.</span></span>  
* <span data-ttu-id="edba7-123">Få vist posterne ved at vælge et punkt i diagrammet.</span><span class="sxs-lookup"><span data-stu-id="edba7-123">View the entries by choosing a point in the chart.</span></span> <span data-ttu-id="edba7-124">F.eks. et punkt på tidslinjen eller en målgruppe i en kolonne.</span><span class="sxs-lookup"><span data-stu-id="edba7-124">For example, a point on the timeline or a column segment.</span></span> <span data-ttu-id="edba7-125">Hvis tallene afviger fra det forventede, er det her, du kan foretage ændringer.</span><span class="sxs-lookup"><span data-stu-id="edba7-125">If the numbers seem off, this is where you can make adjustments.</span></span>  

<span data-ttu-id="edba7-126">Selvom **Pengestrømsprognose** er adskilt fra de andre diagrammer, minder det om dem.</span><span class="sxs-lookup"><span data-stu-id="edba7-126">Although it's separate, the **Cash Flow Forecast** chart is similar.</span></span> <span data-ttu-id="edba7-127">Du kan få vist detaljer, filterresultater og ændre det viste på samme måde.</span><span class="sxs-lookup"><span data-stu-id="edba7-127">You view details, filter results, and change what is displayed in the same ways.</span></span> <span data-ttu-id="edba7-128">Hvis du ændrer en indstilling, kan du opdatere prognosen ved at vælge **Pengestrømsprognose** og derefter **Genberegn prognose**.</span><span class="sxs-lookup"><span data-stu-id="edba7-128">If you change a setting, you can refresh the forecast by choosing **Cash Flow Forecast**, and then **Recalculate Forecast**.</span></span>

<span data-ttu-id="edba7-129">Hvis du vil undersøge prognosen ud over prognoseposter, kan du også se pengestrømskladden.</span><span class="sxs-lookup"><span data-stu-id="edba7-129">If you want to examine the forecast, in addition to forecast entries, you can also look at the cash flow worksheet.</span></span> <span data-ttu-id="edba7-130">Du kan f.eks. se, hvordan prognosen:</span><span class="sxs-lookup"><span data-stu-id="edba7-130">For example, you can see how the forecast:</span></span>

* <span data-ttu-id="edba7-131">Håndterer bekræftede salg og køb.</span><span class="sxs-lookup"><span data-stu-id="edba7-131">Handles confirmed sales and purchases.</span></span>  
* <span data-ttu-id="edba7-132">Fratrækker skyldige beløb og tilføjer tilgodehavender.</span><span class="sxs-lookup"><span data-stu-id="edba7-132">Subtracts payables and adds receivables.</span></span>  
* <span data-ttu-id="edba7-133">Springer dubletter af salgsordrer og købsordrer over.</span><span class="sxs-lookup"><span data-stu-id="edba7-133">Skips duplicate sales orders and purchase orders.</span></span>  

## <a name="to-view-a-cash-flow-worksheet"></a><span data-ttu-id="edba7-134">Sådan vises en pengestrømskladde</span><span class="sxs-lookup"><span data-stu-id="edba7-134">To view a cash flow worksheet</span></span>
1. <span data-ttu-id="edba7-135">Søg efter **Pengestrømsprognoser**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="edba7-135">Search for **Cash Flow Forecasts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="edba7-136">Vælg en pengestrømsprognose, og vælg derefter handlingen **Pengestrømskladde**.</span><span class="sxs-lookup"><span data-stu-id="edba7-136">Choose a cash flow forecast, and then choose the **Cash Flow Worksheet** action.</span></span>  
3. <span data-ttu-id="edba7-137">På siden **Pengestrømskladde** skal du vælge handlingen **Foreslå kladdelinjer**.</span><span class="sxs-lookup"><span data-stu-id="edba7-137">On the **Cash Flow Worksheet** page, choose the **Suggest Worksheet Lines** action.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="edba7-138">Se relateret oplæring på [Microsoft Learn](/learn/modules/forecast-cash-flow-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="edba7-138">See Related Training at [Microsoft Learn](/learn/modules/forecast-cash-flow-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="edba7-139">Se også</span><span class="sxs-lookup"><span data-stu-id="edba7-139">See Also</span></span>
[<span data-ttu-id="edba7-140">Konfigurere Finans</span><span class="sxs-lookup"><span data-stu-id="edba7-140">Setting Up Finance</span></span>](finance-setup-finance.md)  
<span data-ttu-id="edba7-141">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="edba7-141">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="edba7-142">Opsætning af pengestrømsanalyse</span><span class="sxs-lookup"><span data-stu-id="edba7-142">Setting Up Cash Flow Analysis</span></span>](finance-setup-cash-flow-analyses.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]