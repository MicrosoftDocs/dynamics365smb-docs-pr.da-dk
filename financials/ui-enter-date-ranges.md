---
title: Angive datointervaller i Finance and Operations, Business edition | Microsoft Docs
description: "Få mere at vide om, hvordan du i en rapport kan få vist data fra bestemte tidsperioder, ved at bruge datointervaller i Finance and Operations, Business edition."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 05/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: da2fea4e095c8211f30aaa7c570a84a005e7cbc8
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="entering-date-ranges-in-finance-and-operations-business-edition"></a><span data-ttu-id="85df5-103">Angivelse af datointervaller i Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="85df5-103">Entering Date Ranges in Finance and Operations, Business edition</span></span> 
<span data-ttu-id="85df5-104">Du kan angive filtre, der indeholder en startdato og en slutdato for kun at få vist dataene for dette dato- eller tidsinterval.</span><span class="sxs-lookup"><span data-stu-id="85df5-104">You can set filters containing a start date and an end date to display only the data contained in that date range or time interval.</span></span> <span data-ttu-id="85df5-105">Der gælder særlige regler for den måde, du angiver datointervaller på.</span><span class="sxs-lookup"><span data-stu-id="85df5-105">Special rules apply to the way you set date ranges.</span></span> <span data-ttu-id="85df5-106">Lad os tage **Debitor - top 10** som eksempel:</span><span class="sxs-lookup"><span data-stu-id="85df5-106">Let's take the **Customer Top 10** as an example:</span></span>

![Angive et datointerval på anmodningssiden for Debitor - top 10-liste](./media/ui-enter-date-ranges/customer-top10-list.png)

<span data-ttu-id="85df5-108">Her kan du begrænse rapporten til et bestemt datointerval, f.eks. de seneste to uger eller i alt 6 uger, eller det interval, du ønsker.</span><span class="sxs-lookup"><span data-stu-id="85df5-108">Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want.</span></span> <span data-ttu-id="85df5-109">Når du vil angive datointervaller, angiver du datoer og bruger enten **..**</span><span class="sxs-lookup"><span data-stu-id="85df5-109">To set date ranges, you enter dates and then use either **..**</span></span> <span data-ttu-id="85df5-110">eller **|** til at vælge intervallet.</span><span class="sxs-lookup"><span data-stu-id="85df5-110">or **|** to set the range.</span></span> <span data-ttu-id="85df5-111">I eksemplet for at få vist top 10 debitorer i de første to uger i maj, skal du indstille filteret til *01 05 17..14 05 17*.</span><span class="sxs-lookup"><span data-stu-id="85df5-111">In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.</span></span>
<span data-ttu-id="85df5-112">Her er nogle andre eksempler:</span><span class="sxs-lookup"><span data-stu-id="85df5-112">Here are a couple of other examples:</span></span>

| <span data-ttu-id="85df5-113">Betyder</span><span class="sxs-lookup"><span data-stu-id="85df5-113">Meaning</span></span> | <span data-ttu-id="85df5-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="85df5-114">Example</span></span> | <span data-ttu-id="85df5-115">Forklaring</span><span class="sxs-lookup"><span data-stu-id="85df5-115">Entries included</span></span> |
|---|---|---|
|<span data-ttu-id="85df5-116">Lig med</span><span class="sxs-lookup"><span data-stu-id="85df5-116">Equal to</span></span>| <span data-ttu-id="85df5-117">15 12 16</span><span class="sxs-lookup"><span data-stu-id="85df5-117">12 15 16</span></span> |<span data-ttu-id="85df5-118">Kun dem, der er bogført den 15. december 2016.</span><span class="sxs-lookup"><span data-stu-id="85df5-118">Only those posted on December 15 2016.</span></span>|
|<span data-ttu-id="85df5-119">Interval</span><span class="sxs-lookup"><span data-stu-id="85df5-119">Interval</span></span>| <span data-ttu-id="85df5-120">15 12 16..15 17 17</span><span class="sxs-lookup"><span data-stu-id="85df5-120">12 15 16..01 15 17</span></span><br /><br /><span data-ttu-id="85df5-121">..15 12 16</span><span class="sxs-lookup"><span data-stu-id="85df5-121">..12 15 16</span></span>|<span data-ttu-id="85df5-122">Dem, der er bogført fra den 15. december 2016 til og med 15. januar 2017.</span><span class="sxs-lookup"><span data-stu-id="85df5-122">Those posted on dates between and including December 15 2016 and January 15 2017.</span></span><br /><br /><span data-ttu-id="85df5-123">Dem, der er bogført den 15. december 2016 eller tidligere.</span><span class="sxs-lookup"><span data-stu-id="85df5-123">Those posted on December 15 2016 or earlier.</span></span>|
|<span data-ttu-id="85df5-124">Enten/ eller</span><span class="sxs-lookup"><span data-stu-id="85df5-124">Either/or</span></span>|<span data-ttu-id="85df5-125">15 12 16&#124;16 12 16</span><span class="sxs-lookup"><span data-stu-id="85df5-125">12 15 16&#124;12 16 16</span></span>|<span data-ttu-id="85df5-126">Dem, der er bogført enten den 15. december eller 16. december 2016.</span><span class="sxs-lookup"><span data-stu-id="85df5-126">Those posted on either December 15 or December 16 2016.</span></span> <span data-ttu-id="85df5-127">Hvis der er bogført poster på begge dage, vises de ikke.</span><span class="sxs-lookup"><span data-stu-id="85df5-127">If there are entries posted on both days, they will all be displayed.</span></span>|

<span data-ttu-id="85df5-128">Du kan også kombinere de forskellige formattyper.</span><span class="sxs-lookup"><span data-stu-id="85df5-128">You can also combine the various format types.</span></span>

| <span data-ttu-id="85df5-129">Eksempel</span><span class="sxs-lookup"><span data-stu-id="85df5-129">Example</span></span> | <span data-ttu-id="85df5-130">Forklaring</span><span class="sxs-lookup"><span data-stu-id="85df5-130">Entries included</span></span> |
|---|---|
|<span data-ttu-id="85df5-131">15 12 16&#124;01 12 16..31 05 17</span><span class="sxs-lookup"><span data-stu-id="85df5-131">12 15 16&#124;12 01 16..05 31 17</span></span> | <span data-ttu-id="85df5-132">Poster, som er bogført enten den 15. december 2016 eller på datoen fra den 1. december 2016 til og med den 31. maj 2017.</span><span class="sxs-lookup"><span data-stu-id="85df5-132">Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017.</span></span> |
|<span data-ttu-id="85df5-133">..14 12 16&#124;30 12 16..</span><span class="sxs-lookup"><span data-stu-id="85df5-133">..12 14 16&#124;12 30 16..</span></span> | <span data-ttu-id="85df5-134">Poster bogført den 14. december eller tidligere, eller poster bogført den 30. december eller tidligere - dvs. alle poster undtagen dem, der er bogført på datoer mellem og inklusive den 15. og 29. december.</span><span class="sxs-lookup"><span data-stu-id="85df5-134">Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29.</span></span> |

<span data-ttu-id="85df5-135">Bemærk, at vi har brugt det amerikanske format MMDDYY her.</span><span class="sxs-lookup"><span data-stu-id="85df5-135">Note that we have used the US date format MMDDYY here.</span></span> <span data-ttu-id="85df5-136">Efterhånden som [!INCLUDE[d365fin](includes/d365fin_md.md)] bliver tilgængeligt på andre markeder, du vil kunne bruge de formater, som du plejer.</span><span class="sxs-lookup"><span data-stu-id="85df5-136">As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.</span></span>

## <a name="see-also"></a><span data-ttu-id="85df5-137">Se også</span><span class="sxs-lookup"><span data-stu-id="85df5-137">See Also</span></span>
<span data-ttu-id="85df5-138">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="85df5-138">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="85df5-139">Indtaste kriterier i filtre</span><span class="sxs-lookup"><span data-stu-id="85df5-139">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  
[<span data-ttu-id="85df5-140">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="85df5-140">General Business Functionality</span></span>](ui-across-business-areas.md)

