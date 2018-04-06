---
title: Angive datointervaller i Business Central | Microsoft Docs
description: "Få mere at vide om, hvordan du i en rapport kan få vist data fra bestemte tidsperioder, ved at bruge datointervaller i Business Central."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 05/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 552578ce097f7f647ed0962fec0448059d3ca3b2
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="entering-date-ranges"></a><span data-ttu-id="8006c-103">Angive datointervaller</span><span class="sxs-lookup"><span data-stu-id="8006c-103">Entering Date Ranges</span></span> 
<span data-ttu-id="8006c-104">Du kan angive filtre, der indeholder en startdato og en slutdato for kun at få vist dataene for dette dato- eller tidsinterval.</span><span class="sxs-lookup"><span data-stu-id="8006c-104">You can set filters containing a start date and an end date to display only the data contained in that date range or time interval.</span></span> <span data-ttu-id="8006c-105">Der gælder særlige regler for den måde, du angiver datointervaller på.</span><span class="sxs-lookup"><span data-stu-id="8006c-105">Special rules apply to the way you set date ranges.</span></span> <span data-ttu-id="8006c-106">Lad os tage **Debitor - top 10** som eksempel:</span><span class="sxs-lookup"><span data-stu-id="8006c-106">Let's take the **Customer Top 10** as an example:</span></span>

![Angive et datointerval på anmodningssiden for Debitor - top 10-liste](./media/ui-enter-date-ranges/customer-top10-list.png)

<span data-ttu-id="8006c-108">Her kan du begrænse rapporten til et bestemt datointerval, f.eks. de seneste to uger eller i alt 6 uger, eller det interval, du ønsker.</span><span class="sxs-lookup"><span data-stu-id="8006c-108">Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want.</span></span> <span data-ttu-id="8006c-109">Når du vil angive datointervaller, angiver du datoer og bruger enten **..**</span><span class="sxs-lookup"><span data-stu-id="8006c-109">To set date ranges, you enter dates and then use either **..**</span></span> <span data-ttu-id="8006c-110">eller **|** til at vælge intervallet.</span><span class="sxs-lookup"><span data-stu-id="8006c-110">or **|** to set the range.</span></span> <span data-ttu-id="8006c-111">I eksemplet for at få vist top 10 debitorer i de første to uger i maj, skal du indstille filteret til *01 05 17..14 05 17*.</span><span class="sxs-lookup"><span data-stu-id="8006c-111">In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.</span></span>
<span data-ttu-id="8006c-112">Her er nogle andre eksempler:</span><span class="sxs-lookup"><span data-stu-id="8006c-112">Here are a couple of other examples:</span></span>

| <span data-ttu-id="8006c-113">Betyder</span><span class="sxs-lookup"><span data-stu-id="8006c-113">Meaning</span></span> | <span data-ttu-id="8006c-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="8006c-114">Example</span></span> | <span data-ttu-id="8006c-115">Forklaring</span><span class="sxs-lookup"><span data-stu-id="8006c-115">Entries included</span></span> |
|---|---|---|
|<span data-ttu-id="8006c-116">Lig med</span><span class="sxs-lookup"><span data-stu-id="8006c-116">Equal to</span></span>| <span data-ttu-id="8006c-117">15 12 16</span><span class="sxs-lookup"><span data-stu-id="8006c-117">12 15 16</span></span> |<span data-ttu-id="8006c-118">Kun dem, der er bogført den 15. december 2016.</span><span class="sxs-lookup"><span data-stu-id="8006c-118">Only those posted on December 15 2016.</span></span>|
|<span data-ttu-id="8006c-119">Interval</span><span class="sxs-lookup"><span data-stu-id="8006c-119">Interval</span></span>| <span data-ttu-id="8006c-120">15 12 16..15 17 17</span><span class="sxs-lookup"><span data-stu-id="8006c-120">12 15 16..01 15 17</span></span><br /><br /><span data-ttu-id="8006c-121">..15 12 16</span><span class="sxs-lookup"><span data-stu-id="8006c-121">..12 15 16</span></span>|<span data-ttu-id="8006c-122">Dem, der er bogført fra den 15. december 2016 til og med 15. januar 2017.</span><span class="sxs-lookup"><span data-stu-id="8006c-122">Those posted on dates between and including December 15 2016 and January 15 2017.</span></span><br /><br /><span data-ttu-id="8006c-123">Dem, der er bogført den 15. december 2016 eller tidligere.</span><span class="sxs-lookup"><span data-stu-id="8006c-123">Those posted on December 15 2016 or earlier.</span></span>|
|<span data-ttu-id="8006c-124">Enten/ eller</span><span class="sxs-lookup"><span data-stu-id="8006c-124">Either/or</span></span>|<span data-ttu-id="8006c-125">15 12 16&#124;16 12 16</span><span class="sxs-lookup"><span data-stu-id="8006c-125">12 15 16&#124;12 16 16</span></span>|<span data-ttu-id="8006c-126">Dem, der er bogført enten den 15. december eller 16. december 2016.</span><span class="sxs-lookup"><span data-stu-id="8006c-126">Those posted on either December 15 or December 16 2016.</span></span> <span data-ttu-id="8006c-127">Hvis der er bogført poster på begge dage, vises de ikke.</span><span class="sxs-lookup"><span data-stu-id="8006c-127">If there are entries posted on both days, they will all be displayed.</span></span>|

<span data-ttu-id="8006c-128">Du kan også kombinere de forskellige formattyper.</span><span class="sxs-lookup"><span data-stu-id="8006c-128">You can also combine the various format types.</span></span>

| <span data-ttu-id="8006c-129">Eksempel</span><span class="sxs-lookup"><span data-stu-id="8006c-129">Example</span></span> | <span data-ttu-id="8006c-130">Forklaring</span><span class="sxs-lookup"><span data-stu-id="8006c-130">Entries included</span></span> |
|---|---|
|<span data-ttu-id="8006c-131">15 12 16&#124;01 12 16..31 05 17</span><span class="sxs-lookup"><span data-stu-id="8006c-131">12 15 16&#124;12 01 16..05 31 17</span></span> | <span data-ttu-id="8006c-132">Poster, som er bogført enten den 15. december 2016 eller på datoen fra den 1. december 2016 til og med den 31. maj 2017.</span><span class="sxs-lookup"><span data-stu-id="8006c-132">Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017.</span></span> |
|<span data-ttu-id="8006c-133">..14 12 16&#124;30 12 16..</span><span class="sxs-lookup"><span data-stu-id="8006c-133">..12 14 16&#124;12 30 16..</span></span> | <span data-ttu-id="8006c-134">Poster bogført den 14. december eller tidligere, eller poster bogført den 30. december eller tidligere - dvs. alle poster undtagen dem, der er bogført på datoer mellem og inklusive den 15. og 29. december.</span><span class="sxs-lookup"><span data-stu-id="8006c-134">Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29.</span></span> |

<span data-ttu-id="8006c-135">Bemærk, at vi har brugt det amerikanske format MMDDYY her.</span><span class="sxs-lookup"><span data-stu-id="8006c-135">Note that we have used the US date format MMDDYY here.</span></span> <span data-ttu-id="8006c-136">Efterhånden som [!INCLUDE[d365fin](includes/d365fin_md.md)] bliver tilgængeligt på andre markeder, du vil kunne bruge de formater, som du plejer.</span><span class="sxs-lookup"><span data-stu-id="8006c-136">As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.</span></span>

## <a name="see-also"></a><span data-ttu-id="8006c-137">Se også</span><span class="sxs-lookup"><span data-stu-id="8006c-137">See Also</span></span>
<span data-ttu-id="8006c-138">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8006c-138">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="8006c-139">Indtaste kriterier i filtre</span><span class="sxs-lookup"><span data-stu-id="8006c-139">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  
[<span data-ttu-id="8006c-140">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="8006c-140">General Business Functionality</span></span>](ui-across-business-areas.md)

