---
title: Vise indsigt, der kan handles på, i rollecentre | Microsoft Docs
description: Udvidelsen Vigtig forretningsindsigt roterer en række forretningsmæssig indsigt i rollecentre.
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: BI, add-in, insight, headline, data
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 5fe9f0907611843951b682a9bf07c0c153486700
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377319"
---
# <a name="the-essential-business-insights-extension"></a><span data-ttu-id="b7ae9-103">Udvidelsen Vigtig forretningsindsigt</span><span class="sxs-lookup"><span data-stu-id="b7ae9-103">The Essential Business Insights Extension</span></span>
<span data-ttu-id="b7ae9-104">Udvidelsen Vigtig forretningsindsigt finder interessante forretningsmæssige oplysninger i dine virksomhedsdata og vises som avislignende overskrifter i rollecentre.</span><span class="sxs-lookup"><span data-stu-id="b7ae9-104">The Essential Business Insights extension finds interesting business facts in your company data and displays them as newspaper-like headlines in Role Centers.</span></span> <span data-ttu-id="b7ae9-105">Afhængigt af hvad udvidelsen finder i dataene, er indsigt fra sidste uge, måned eller tre måneder fra dags dato.</span><span class="sxs-lookup"><span data-stu-id="b7ae9-105">Depending on what the extension finds in the data, the insights are from the last week, month, or three months from the current date.</span></span> <span data-ttu-id="b7ae9-106">Indsigten opdateres hvert 10. minut.</span><span class="sxs-lookup"><span data-stu-id="b7ae9-106">The insights update every 10 minutes.</span></span>  

<span data-ttu-id="b7ae9-107">Hvis du vil se nærmere på en indsigt, kan du vælge den for at gå til kilden.</span><span class="sxs-lookup"><span data-stu-id="b7ae9-107">If you want to take a closer look at an insight, you can choose it to go to its source.</span></span> <span data-ttu-id="b7ae9-108">Hvis du f.eks. vil have oplysninger om den største salgsfaktura, der blev bogført sidste uge, kan du vælge at indsigten skal vise fakturaen.</span><span class="sxs-lookup"><span data-stu-id="b7ae9-108">For example, if you want details about the largest sales invoice that was posted last week, you can choose the insight to display the invoice.</span></span>

<span data-ttu-id="b7ae9-109">I følgende tabel beskrives den indsigt, som udvidelsen sender til hvert rollecenter.</span><span class="sxs-lookup"><span data-stu-id="b7ae9-109">The following table describes the insights that this extension provides for each Role Center.</span></span>

|<span data-ttu-id="b7ae9-110">Rollecenter</span><span class="sxs-lookup"><span data-stu-id="b7ae9-110">Role Center</span></span>|<span data-ttu-id="b7ae9-111">Spørgsmål indsigten besvarer</span><span class="sxs-lookup"><span data-stu-id="b7ae9-111">Questions the Insights Answer</span></span>|
|----|-----|
|<span data-ttu-id="b7ae9-112">Standard</span><span class="sxs-lookup"><span data-stu-id="b7ae9-112">Default</span></span>|<span data-ttu-id="b7ae9-113">Viser en hilsen og et link til produktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="b7ae9-113">Displays a greeting, and link to product information.</span></span>|
|<span data-ttu-id="b7ae9-114">Virksomhedsleder</span><span class="sxs-lookup"><span data-stu-id="b7ae9-114">Business Manager</span></span>|<li> <span data-ttu-id="b7ae9-115">Hvad var den mest populære vare sidste uge, måned eller sidste kvartal, og hvor mange solgte vi?</span><span class="sxs-lookup"><span data-stu-id="b7ae9-115">What was the most popular item last week, month, or last three months, and how many did we sell?</span></span><br><li> <span data-ttu-id="b7ae9-116">Hvad var den største salgsordre sidste uge, måned eller sidste kvartal?</span><span class="sxs-lookup"><span data-stu-id="b7ae9-116">What was the largest sale order last week, month, or last three months?</span></span><br><li> <span data-ttu-id="b7ae9-117">Hvem, eller hvad, var den travleste ressource, og hvad var reservationerne?</span><span class="sxs-lookup"><span data-stu-id="b7ae9-117">Who, or what, was the busiest resource, and what were the bookings?</span></span><br><li> <span data-ttu-id="b7ae9-118">Er salget gået op i sidste uge, måned eller kvartal, sammenlignet med den samme periode sidste år?</span><span class="sxs-lookup"><span data-stu-id="b7ae9-118">Have sales gone up in the last week, month, or three months, compared to the same period last year?</span></span><br><li> <span data-ttu-id="b7ae9-119">Hvad er den største salgsfaktura vi bogførte sidste uge, måned eller sidste kvartal, og til hvilken kunde sendte vi fakturaen?</span><span class="sxs-lookup"><span data-stu-id="b7ae9-119">What was the biggest sales invoice we posted last week, month, or last three months, and to which customer did we send the bill?</span></span></li> |
|<span data-ttu-id="b7ae9-120">Revisor</span><span class="sxs-lookup"><span data-stu-id="b7ae9-120">Accountant</span></span>|<li> <span data-ttu-id="b7ae9-121">Hvad var den største salgsordre og bogførte faktura i sidste uge, måned eller sidste kvartal?</span><span class="sxs-lookup"><span data-stu-id="b7ae9-121">What was the largest sales order and posted invoice last week, month, or last three months?</span></span><br><li> <span data-ttu-id="b7ae9-122">Er salget gået op i sidste uge, måned eller kvartal, sammenlignet med den samme periode sidste år?</span><span class="sxs-lookup"><span data-stu-id="b7ae9-122">Have sales gone up in the last week, month, or three months, compared to the same period last year?</span></span> |
|<span data-ttu-id="b7ae9-123">Ordrebehandler</span><span class="sxs-lookup"><span data-stu-id="b7ae9-123">Order Processor</span></span>| <span data-ttu-id="b7ae9-124">Hvad var den største salgsordre og bogførte faktura i sidste uge, måned eller sidste kvartal?</span><span class="sxs-lookup"><span data-stu-id="b7ae9-124">What was the largest sale order and posted invoice last week, month, or last three months?</span></span>|
|<span data-ttu-id="b7ae9-125">CRM-chef</span><span class="sxs-lookup"><span data-stu-id="b7ae9-125">Relationship Manager</span></span>| <span data-ttu-id="b7ae9-126">Hvad var det største fakturerede beløb, og hvilken kunde sendte vi fakturaen til?</span><span class="sxs-lookup"><span data-stu-id="b7ae9-126">What was the largest invoiced amount, and to which customer did we send the bill?</span></span>|
|<span data-ttu-id="b7ae9-127">Teammedlem</span><span class="sxs-lookup"><span data-stu-id="b7ae9-127">Team Member</span></span>| <span data-ttu-id="b7ae9-128">Viser en hilsen og et link til produktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="b7ae9-128">Displays a greeting, and link to product information.</span></span>|
|<span data-ttu-id="b7ae9-129">Projektleder</span><span class="sxs-lookup"><span data-stu-id="b7ae9-129">Project Manager</span></span>| <span data-ttu-id="b7ae9-130">Viser en hilsen og et link til produktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="b7ae9-130">Displays a greeting, and link to product information.</span></span>|
|<span data-ttu-id="b7ae9-131">Administrator</span><span class="sxs-lookup"><span data-stu-id="b7ae9-131">Administrator</span></span>| <span data-ttu-id="b7ae9-132">Viser en hilsen og et link til produktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="b7ae9-132">Displays a greeting, and link to product information.</span></span>|

## <a name="see-also"></a><span data-ttu-id="b7ae9-133">Se også</span><span class="sxs-lookup"><span data-stu-id="b7ae9-133">See Also</span></span>
<span data-ttu-id="b7ae9-134">[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="b7ae9-134">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]