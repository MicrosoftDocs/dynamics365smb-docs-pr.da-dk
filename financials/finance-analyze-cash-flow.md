---
title: "Analyse af pengestrømme | Microsoft Docs"
description: "Beskriver, hvordan du bruger diagrammerne Kassebeholdningsproces, Indtægter og udgifter, Pengestrøm og Pengestrømsprognose til at analysere tidligere og fremtidige pengestrømme til og fra din virksomhed."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b11c6ea21b507024e6024b180205e02a60fe9465
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="analyzing-cash-flow-in-your-company"></a><span data-ttu-id="e8d21-103">Analysere pengestrømme i din virksomhed</span><span class="sxs-lookup"><span data-stu-id="e8d21-103">Analyzing Cash Flow in Your Company</span></span>
<span data-ttu-id="e8d21-104">Penge styrer, som man siger.</span><span class="sxs-lookup"><span data-stu-id="e8d21-104">As they say, cash is king.</span></span> <span data-ttu-id="e8d21-105">Diagrammer i rollecenteret Regnskabsmedarbejder giver indsigt, som kan hjælpe dig med at træffe beslutninger vedrørende dine pengestrømme.</span><span class="sxs-lookup"><span data-stu-id="e8d21-105">The charts on the Accountant Role Center provide insight that can help you make solid decisions about what to do with your cash.</span></span>  

| <span data-ttu-id="e8d21-106">For at besvare spørgsmål som de følgende</span><span class="sxs-lookup"><span data-stu-id="e8d21-106">To answer questions like these</span></span> | <span data-ttu-id="e8d21-107">Skal du bruge dette diagram</span><span class="sxs-lookup"><span data-stu-id="e8d21-107">Use this chart</span></span> |
| --- | --- |
| <span data-ttu-id="e8d21-108">Hvor længe lægger salgsprocessen beslag på mine kontanter?</span><span class="sxs-lookup"><span data-stu-id="e8d21-108">How long does the sales process tie up my cash?</span></span></br> <span data-ttu-id="e8d21-109">Skal jeg øge eller mindske lagerniveauer?</span><span class="sxs-lookup"><span data-stu-id="e8d21-109">Should I increase or reduce inventory levels?</span></span> |<span data-ttu-id="e8d21-110">Kassebeholdningsproces</span><span class="sxs-lookup"><span data-stu-id="e8d21-110">Cash Cycle</span></span> |
| <span data-ttu-id="e8d21-111">Hvornår er et pengebeløb ankommet til og har forladt min virksomhed?</span><span class="sxs-lookup"><span data-stu-id="e8d21-111">When did cash move in and out of my company?</span></span></br> <span data-ttu-id="e8d21-112">Er nogle perioder bedre end andre?</span><span class="sxs-lookup"><span data-stu-id="e8d21-112">Are some periods better than others?</span></span> |<span data-ttu-id="e8d21-113">Pengestrøm</span><span class="sxs-lookup"><span data-stu-id="e8d21-113">Cash Flow</span></span> |
| <span data-ttu-id="e8d21-114">Ser tallene negative ud for en periode?</span><span class="sxs-lookup"><span data-stu-id="e8d21-114">Do the numbers seem off for a period?</span></span></br> <span data-ttu-id="e8d21-115">Skal jeg undersøge det?</span><span class="sxs-lookup"><span data-stu-id="e8d21-115">Should I investigate?</span></span> |<span data-ttu-id="e8d21-116">Indtægter og udgifter</span><span class="sxs-lookup"><span data-stu-id="e8d21-116">Income & Expense</span></span> |
| <span data-ttu-id="e8d21-117">Hvornår kan jeg forvente kontante overskud eller underskud?</span><span class="sxs-lookup"><span data-stu-id="e8d21-117">When might a cash surplus or deficit happen?</span></span></br> <span data-ttu-id="e8d21-118">Skal jeg nedbringe gæld eller låne for at imødegå kommende udgifter?</span><span class="sxs-lookup"><span data-stu-id="e8d21-118">Should I pay down debt, or borrow to meet upcoming expenses?</span></span> |<span data-ttu-id="e8d21-119">Pengestrømsprognoser</span><span class="sxs-lookup"><span data-stu-id="e8d21-119">Cash Flow Forecasts</span></span> |

<span data-ttu-id="e8d21-120">I rollecentret Regnskabsmedarbejder under **Finansydeevne** giver diagrammerne **Kassebeholdningsproces**, **Pengestrøm** og **Indtægter og udgifter** dig måder at analysere pengestrømme på:</span><span class="sxs-lookup"><span data-stu-id="e8d21-120">On the Accountant Role Center, under **Finance Performance**, the **Cash Cycle**, **Cash Flow**, and **Income & Expense** charts offer ways to analyze cash flow:</span></span>  

* <span data-ttu-id="e8d21-121">Få vist tallene i en periode ved hjælp af tidslinjeskyderen.</span><span class="sxs-lookup"><span data-stu-id="e8d21-121">See figures for a period by using the timeline slider.</span></span>  
* <span data-ttu-id="e8d21-122">Filtrer diagrammet ved at vælge kilden i forklaringen.</span><span class="sxs-lookup"><span data-stu-id="e8d21-122">Filter the chart by choosing the source in the legend.</span></span>  
* <span data-ttu-id="e8d21-123">Skift tidsrum, eller gå til forrige eller næste periode ved at vælge indstillinger i rullemenuen **Finansydeevne**.</span><span class="sxs-lookup"><span data-stu-id="e8d21-123">Change the length of the period, or go to the previous or next period, by choosing options on the **Finance Performance** drop down.</span></span>  
* <span data-ttu-id="e8d21-124">Få vist posterne ved at vælge et punkt i diagrammet.</span><span class="sxs-lookup"><span data-stu-id="e8d21-124">View the entries by choosing a point in the chart.</span></span> <span data-ttu-id="e8d21-125">F.eks. et punkt på tidslinjen eller en målgruppe i en kolonne.</span><span class="sxs-lookup"><span data-stu-id="e8d21-125">For example, a point on the timeline or a column segment.</span></span> <span data-ttu-id="e8d21-126">Hvis tallene afviger fra det forventede, er det her, du kan foretage ændringer.</span><span class="sxs-lookup"><span data-stu-id="e8d21-126">If the numbers seem off, this is where you can make adjustments.</span></span>  

<span data-ttu-id="e8d21-127">Selvom **Pengestrømsprognose** er adskilt fra de andre diagrammer, minder det om dem.</span><span class="sxs-lookup"><span data-stu-id="e8d21-127">Although it's separate, the **Cash Flow Forecast** chart is similar.</span></span> <span data-ttu-id="e8d21-128">Du kan få vist detaljer, filterresultater og ændre det viste på samme måde.</span><span class="sxs-lookup"><span data-stu-id="e8d21-128">You view details, filter results, and change what is displayed in the same ways.</span></span> <span data-ttu-id="e8d21-129">Hvis du ændrer en indstilling, kan du opdatere prognosen ved at vælge **Pengestrømsprognose** og derefter **Genberegn prognose**.</span><span class="sxs-lookup"><span data-stu-id="e8d21-129">If you change a setting, you can refresh the forecast by choosing **Cash Flow Forecast**, and then **Recalculate Forecast**.</span></span>

<span data-ttu-id="e8d21-130">Hvis du vil undersøge prognosen ud over prognoseposter, kan du også se pengestrømskladden.</span><span class="sxs-lookup"><span data-stu-id="e8d21-130">If you want to examine the forecast, in addition to forecast entries, you can also look at the cash flow worksheet.</span></span> <span data-ttu-id="e8d21-131">Du kan f.eks. se, hvordan prognosen:</span><span class="sxs-lookup"><span data-stu-id="e8d21-131">For example, you can see how the forecast:</span></span>

* <span data-ttu-id="e8d21-132">Håndterer bekræftede salg og køb.</span><span class="sxs-lookup"><span data-stu-id="e8d21-132">Handles confirmed sales and purchases.</span></span>  
* <span data-ttu-id="e8d21-133">Fratrækker skyldige beløb og tilføjer tilgodehavender.</span><span class="sxs-lookup"><span data-stu-id="e8d21-133">Subtracts payables and adds receivables.</span></span>  
* <span data-ttu-id="e8d21-134">Springer dubletter af salgsordrer og købsordrer over.</span><span class="sxs-lookup"><span data-stu-id="e8d21-134">Skips duplicate sales orders and purchase orders.</span></span>  

## <a name="to-view-a-cash-flow-worksheet"></a><span data-ttu-id="e8d21-135">Sådan vises en pengestrømskladde</span><span class="sxs-lookup"><span data-stu-id="e8d21-135">To view a cash flow worksheet</span></span>
1. <span data-ttu-id="e8d21-136">Søg efter **Pengestrømsprognoser**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="e8d21-136">Search for **Cash Flow Forecasts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e8d21-137">Vælg en pengestrømsprognose, og vælg derefter handlingen **Pengestrømskladde**.</span><span class="sxs-lookup"><span data-stu-id="e8d21-137">Choose a cash flow forecast, and then choose the **Cash Flow Worksheet** action.</span></span>  
3. <span data-ttu-id="e8d21-138">På siden **Pengestrømskladde** skal du vælge handlingen **Foreslå kladdelinjer**.</span><span class="sxs-lookup"><span data-stu-id="e8d21-138">On the **Cash Flow Worksheet** page, choose the **Suggest Worksheet Lines** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e8d21-139">Se også</span><span class="sxs-lookup"><span data-stu-id="e8d21-139">See Also</span></span>
[<span data-ttu-id="e8d21-140">Konfigurere Finans</span><span class="sxs-lookup"><span data-stu-id="e8d21-140">Setting Up Finance</span></span>](finance-setup-finance.md)  
<span data-ttu-id="e8d21-141">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e8d21-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="e8d21-142">Opsætning af pengestrømsanalyse</span><span class="sxs-lookup"><span data-stu-id="e8d21-142">Setting Up Cash Flow Analysis</span></span>](finance-setup-cash-flow-analyses.md)  

