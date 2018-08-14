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
ms.date: 07/05/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7664360941313da6ea0b797ef00df2e9810ad62
ms.openlocfilehash: ff63ae71a78f956dddb7b5247ee66f9416cf7cf1
ms.contentlocale: da-dk
ms.lasthandoff: 07/09/2018

---
# <a name="entering-date-ranges"></a><span data-ttu-id="6845b-103">Angive datointervaller</span><span class="sxs-lookup"><span data-stu-id="6845b-103">Entering Date Ranges</span></span>
<span data-ttu-id="6845b-104">Du kan angive filtre, der indeholder en startdato og en slutdato for kun at få vist dataene for dette dato- eller tidsinterval.</span><span class="sxs-lookup"><span data-stu-id="6845b-104">You can set filters containing a start date and an end date to display only the data contained in that date range or time interval.</span></span> <span data-ttu-id="6845b-105">Der gælder særlige regler for den måde, du angiver datointervaller på.</span><span class="sxs-lookup"><span data-stu-id="6845b-105">Special rules apply to the way you set date ranges.</span></span> <span data-ttu-id="6845b-106">Lad os tage **Debitor - top 10** som eksempel:</span><span class="sxs-lookup"><span data-stu-id="6845b-106">Let's take the **Customer Top 10** as an example:</span></span>

![Angive et datointerval på anmodningssiden for Debitor - top 10-liste](./media/ui-enter-date-ranges/customer-top10-list.png)

<span data-ttu-id="6845b-108">Her kan du begrænse rapporten til et bestemt datointerval, f.eks. de seneste to uger eller i alt 6 uger, eller det interval, du ønsker.</span><span class="sxs-lookup"><span data-stu-id="6845b-108">Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want.</span></span> <span data-ttu-id="6845b-109">Når du vil angive datointervaller, angiver du datoer og bruger enten **..**</span><span class="sxs-lookup"><span data-stu-id="6845b-109">To set date ranges, you enter dates and then use either **..**</span></span> <span data-ttu-id="6845b-110">eller **|** til at vælge intervallet.</span><span class="sxs-lookup"><span data-stu-id="6845b-110">or **|** to set the range.</span></span> <span data-ttu-id="6845b-111">I eksemplet for at få vist top 10 debitorer i de første to uger i maj, skal du indstille filteret til *01 05 17..14 05 17*.</span><span class="sxs-lookup"><span data-stu-id="6845b-111">In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.</span></span>
<span data-ttu-id="6845b-112">Her er nogle andre eksempler:</span><span class="sxs-lookup"><span data-stu-id="6845b-112">Here are a couple of other examples:</span></span>

| <span data-ttu-id="6845b-113">Betyder</span><span class="sxs-lookup"><span data-stu-id="6845b-113">Meaning</span></span> | <span data-ttu-id="6845b-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="6845b-114">Example</span></span> | <span data-ttu-id="6845b-115">Forklaring</span><span class="sxs-lookup"><span data-stu-id="6845b-115">Entries included</span></span> |
|---|---|---|
|<span data-ttu-id="6845b-116">Lig med</span><span class="sxs-lookup"><span data-stu-id="6845b-116">Equal to</span></span>| <span data-ttu-id="6845b-117">15 12 16</span><span class="sxs-lookup"><span data-stu-id="6845b-117">12 15 16</span></span> |<span data-ttu-id="6845b-118">Kun dem, der er bogført den 15. december 2016.</span><span class="sxs-lookup"><span data-stu-id="6845b-118">Only those posted on December 15 2016.</span></span>|
|<span data-ttu-id="6845b-119">Interval</span><span class="sxs-lookup"><span data-stu-id="6845b-119">Interval</span></span>| <span data-ttu-id="6845b-120">15 12 16..15 01 17</span><span class="sxs-lookup"><span data-stu-id="6845b-120">12 15 16..01 15 17</span></span><br /><br /><span data-ttu-id="6845b-121">..15 12 16</span><span class="sxs-lookup"><span data-stu-id="6845b-121">..12 15 16</span></span>|<span data-ttu-id="6845b-122">Dem, der er bogført fra den 15. december 2016 til og med 15. januar 2017.</span><span class="sxs-lookup"><span data-stu-id="6845b-122">Those posted on dates between and including December 15 2016 and January 15 2017.</span></span><br /><br /><span data-ttu-id="6845b-123">Dem, der er bogført den 15. december 2016 eller tidligere.</span><span class="sxs-lookup"><span data-stu-id="6845b-123">Those posted on December 15 2016 or earlier.</span></span>|
|<span data-ttu-id="6845b-124">Enten/ eller</span><span class="sxs-lookup"><span data-stu-id="6845b-124">Either/or</span></span>|<span data-ttu-id="6845b-125">15 12 16&#124;16 12 16</span><span class="sxs-lookup"><span data-stu-id="6845b-125">12 15 16&#124;12 16 16</span></span>|<span data-ttu-id="6845b-126">Dem, der er bogført enten den 15. december eller 16. december 2016.</span><span class="sxs-lookup"><span data-stu-id="6845b-126">Those posted on either December 15 or December 16 2016.</span></span> <span data-ttu-id="6845b-127">Hvis der er bogført poster på begge dage, vises de ikke.</span><span class="sxs-lookup"><span data-stu-id="6845b-127">If there are entries posted on both days, they will all be displayed.</span></span>|

<span data-ttu-id="6845b-128">Du kan også kombinere de forskellige formattyper.</span><span class="sxs-lookup"><span data-stu-id="6845b-128">You can also combine the various format types.</span></span>

| <span data-ttu-id="6845b-129">Eksempel</span><span class="sxs-lookup"><span data-stu-id="6845b-129">Example</span></span> | <span data-ttu-id="6845b-130">Forklaring</span><span class="sxs-lookup"><span data-stu-id="6845b-130">Entries included</span></span> |
|---|---|
|<span data-ttu-id="6845b-131">15 12 16&#124;01 12 16..31 05 17</span><span class="sxs-lookup"><span data-stu-id="6845b-131">12 15 16&#124;12 01 16..05 31 17</span></span> | <span data-ttu-id="6845b-132">Poster, som er bogført enten den 15. december 2016 eller på datoen fra den 1. december 2016 til og med den 31. maj 2017.</span><span class="sxs-lookup"><span data-stu-id="6845b-132">Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017.</span></span> |
|<span data-ttu-id="6845b-133">..14 12 16&#124;30 12 16..</span><span class="sxs-lookup"><span data-stu-id="6845b-133">..12 14 16&#124;12 30 16..</span></span> | <span data-ttu-id="6845b-134">Poster bogført den 14. december eller tidligere, eller poster bogført den 30. december eller tidligere - dvs. alle poster undtagen dem, der er bogført på datoer mellem og inklusive den 15. og 29. december.</span><span class="sxs-lookup"><span data-stu-id="6845b-134">Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29.</span></span> |

<span data-ttu-id="6845b-135">Bemærk, at vi har brugt det amerikanske format MMDDYY her.</span><span class="sxs-lookup"><span data-stu-id="6845b-135">Note that we have used the US date format MMDDYY here.</span></span> <span data-ttu-id="6845b-136">Efterhånden som [!INCLUDE[d365fin](includes/d365fin_md.md)] bliver tilgængeligt på andre markeder, du vil kunne bruge de formater, som du plejer.</span><span class="sxs-lookup"><span data-stu-id="6845b-136">As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="6845b-137">Bruge datoformler</span><span class="sxs-lookup"><span data-stu-id="6845b-137">Using Date Formulas</span></span>
<span data-ttu-id="6845b-138">En datoformel er en kort, forkortet kombination af bogstaver og tal, der angiver, hvordan datoer skal beregnes.</span><span class="sxs-lookup"><span data-stu-id="6845b-138">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="6845b-139">Du kan indtaste datoformler i forskellige datoberegningsfelter og i gentagelsesintervalfelter i gentagelseskladder.</span><span class="sxs-lookup"><span data-stu-id="6845b-139">You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.</span></span>

> [!NOTE]
>  <span data-ttu-id="6845b-140">I alle formlens datafelter indgår en dag automatisk til at dække i dag som den dag, hvor perioden starter.</span><span class="sxs-lookup"><span data-stu-id="6845b-140">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="6845b-141">Tilsvarende, hvis du f.eks. indtaster **1U**, så er perioden faktisk otte dage, fordi i dag er inkluderet.</span><span class="sxs-lookup"><span data-stu-id="6845b-141">Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="6845b-142">Du skal indtaste **6D** eller **1U\-1D** for at angive en periode på syv dage (en hel uge), der medtager periodens startdato.</span><span class="sxs-lookup"><span data-stu-id="6845b-142">To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.</span></span>

<span data-ttu-id="6845b-143">Her følger et par eksempler på brugen af datoformler:</span><span class="sxs-lookup"><span data-stu-id="6845b-143">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="6845b-144">Datoformlen i gentagelsesintervalfeltet i en gentagelseskladde afgør, hvor tit posten på kladdelinjen skal bogføres.</span><span class="sxs-lookup"><span data-stu-id="6845b-144">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="6845b-145">Datoformlen i feltet **Respitperiode** for et bestemt rykkerniveau afgør det tidsrum, der skal gå fra forfaldsdatoen (eller fra forfaldsdatoen for den forrige rykker), før der oprettes en rykker.</span><span class="sxs-lookup"><span data-stu-id="6845b-145">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.</span></span>

-   <span data-ttu-id="6845b-146">Datoformlen i feltet **Forfaldsdatoformel** afgør, hvordan forfaldsdatoen på rykkeren beregnes.</span><span class="sxs-lookup"><span data-stu-id="6845b-146">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="6845b-147">Datoformlen kan indeholde op til 20 tegn (både tal og bogstaver).</span><span class="sxs-lookup"><span data-stu-id="6845b-147">The date calculation formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="6845b-148">Du kan bruge følgende bogstaver som forkortelser for tidsangivelser.</span><span class="sxs-lookup"><span data-stu-id="6845b-148">You can use the following letters, which are abbreviations for time specifications.</span></span>

|  <span data-ttu-id="6845b-149">Bogstav</span><span class="sxs-lookup"><span data-stu-id="6845b-149">Letter</span></span>  |  <span data-ttu-id="6845b-150">Tidsangivelse</span><span class="sxs-lookup"><span data-stu-id="6845b-150">Time specification</span></span>  |
|----------|----------------------|
|<span data-ttu-id="6845b-151">U</span><span class="sxs-lookup"><span data-stu-id="6845b-151">C</span></span>|<span data-ttu-id="6845b-152">Løbende</span><span class="sxs-lookup"><span data-stu-id="6845b-152">Current</span></span>|
|<span data-ttu-id="6845b-153">D</span><span class="sxs-lookup"><span data-stu-id="6845b-153">D</span></span>|<span data-ttu-id="6845b-154">Dag\(e\)</span><span class="sxs-lookup"><span data-stu-id="6845b-154">Day\(s\)</span></span>|
|<span data-ttu-id="6845b-155">V</span><span class="sxs-lookup"><span data-stu-id="6845b-155">W</span></span>|<span data-ttu-id="6845b-156">Uge\(r\)</span><span class="sxs-lookup"><span data-stu-id="6845b-156">Week\(s\)</span></span>|
|<span data-ttu-id="6845b-157">M</span><span class="sxs-lookup"><span data-stu-id="6845b-157">M</span></span>|<span data-ttu-id="6845b-158">Måned\(er\)</span><span class="sxs-lookup"><span data-stu-id="6845b-158">Month\(s\)</span></span>|
|<span data-ttu-id="6845b-159">K</span><span class="sxs-lookup"><span data-stu-id="6845b-159">Q</span></span>|<span data-ttu-id="6845b-160">Kvartal\(er\)</span><span class="sxs-lookup"><span data-stu-id="6845b-160">Quarter\(s\)</span></span>|
|<span data-ttu-id="6845b-161">Å</span><span class="sxs-lookup"><span data-stu-id="6845b-161">Y</span></span>|<span data-ttu-id="6845b-162">År\(\)</span><span class="sxs-lookup"><span data-stu-id="6845b-162">Year\(s\)</span></span>|

<span data-ttu-id="6845b-163">Datoformlen kan opbygges på tre måder.</span><span class="sxs-lookup"><span data-stu-id="6845b-163">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="6845b-164">Følgende eksempel viser, hvordan du skal bruge **A** for aktuel og en tidsenhed.</span><span class="sxs-lookup"><span data-stu-id="6845b-164">The following example shows how to use **C**, for current, and a time unit.</span></span>

|  <span data-ttu-id="6845b-165">Udtryk</span><span class="sxs-lookup"><span data-stu-id="6845b-165">Expression</span></span>  |  <span data-ttu-id="6845b-166">Betyder</span><span class="sxs-lookup"><span data-stu-id="6845b-166">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="6845b-167">LU</span><span class="sxs-lookup"><span data-stu-id="6845b-167">CW</span></span>|<span data-ttu-id="6845b-168">Løbende uge</span><span class="sxs-lookup"><span data-stu-id="6845b-168">Current week</span></span>|
|<span data-ttu-id="6845b-169">cm</span><span class="sxs-lookup"><span data-stu-id="6845b-169">CM</span></span>|<span data-ttu-id="6845b-170">Løbende måned</span><span class="sxs-lookup"><span data-stu-id="6845b-170">Current month</span></span>|

<span data-ttu-id="6845b-171">Følgende eksempel viser, hvordan du skal bruge et tal og en tidsenhed.</span><span class="sxs-lookup"><span data-stu-id="6845b-171">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="6845b-172">Tallet må ikke være større end 9999.</span><span class="sxs-lookup"><span data-stu-id="6845b-172">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="6845b-173">Udtryk</span><span class="sxs-lookup"><span data-stu-id="6845b-173">Expression</span></span>  |  <span data-ttu-id="6845b-174">Betyder</span><span class="sxs-lookup"><span data-stu-id="6845b-174">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="6845b-175">10D</span><span class="sxs-lookup"><span data-stu-id="6845b-175">10D</span></span>|<span data-ttu-id="6845b-176">10 dage fra i dag</span><span class="sxs-lookup"><span data-stu-id="6845b-176">10 days from today</span></span>|
|<span data-ttu-id="6845b-177">2U</span><span class="sxs-lookup"><span data-stu-id="6845b-177">2W</span></span>|<span data-ttu-id="6845b-178">2 uger fra i dag</span><span class="sxs-lookup"><span data-stu-id="6845b-178">2 weeks from today</span></span>|

<span data-ttu-id="6845b-179">Følgende eksempel viser, hvordan du skal bruge en tidsenhed og et tal.</span><span class="sxs-lookup"><span data-stu-id="6845b-179">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="6845b-180">Udtryk</span><span class="sxs-lookup"><span data-stu-id="6845b-180">Expression</span></span>  |  <span data-ttu-id="6845b-181">Betyder</span><span class="sxs-lookup"><span data-stu-id="6845b-181">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="6845b-182">D10</span><span class="sxs-lookup"><span data-stu-id="6845b-182">D10</span></span>|<span data-ttu-id="6845b-183">Den næste 10. dage i en måned</span><span class="sxs-lookup"><span data-stu-id="6845b-183">The next 10th day of a month</span></span>|
|<span data-ttu-id="6845b-184">UD4</span><span class="sxs-lookup"><span data-stu-id="6845b-184">WD4</span></span>|<span data-ttu-id="6845b-185">Den næste 4. dag i en uge \(torsdag\)</span><span class="sxs-lookup"><span data-stu-id="6845b-185">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="6845b-186">Følgende eksempel viser, hvordan du kan kombinere de tre formler efter behov.</span><span class="sxs-lookup"><span data-stu-id="6845b-186">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="6845b-187">Udtryk</span><span class="sxs-lookup"><span data-stu-id="6845b-187">Expression</span></span>  |  <span data-ttu-id="6845b-188">Betyder</span><span class="sxs-lookup"><span data-stu-id="6845b-188">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="6845b-189">LM\+10D</span><span class="sxs-lookup"><span data-stu-id="6845b-189">CM\+10D</span></span>|<span data-ttu-id="6845b-190">Løbende måned \+ 10 dage</span><span class="sxs-lookup"><span data-stu-id="6845b-190">Current month \+ 10 days</span></span>|

<span data-ttu-id="6845b-191">Følgende eksempel viser, hvordan du kan bruge et minustegn til at angive en dato i fortiden.</span><span class="sxs-lookup"><span data-stu-id="6845b-191">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="6845b-192">Udtryk</span><span class="sxs-lookup"><span data-stu-id="6845b-192">Expression</span></span>  |  <span data-ttu-id="6845b-193">Betyder</span><span class="sxs-lookup"><span data-stu-id="6845b-193">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="6845b-194">-1Å</span><span class="sxs-lookup"><span data-stu-id="6845b-194">-1Y</span></span>|<span data-ttu-id="6845b-195">1 år siden fra i dag</span><span class="sxs-lookup"><span data-stu-id="6845b-195">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="6845b-196">Hvis lokationen bruger en basiskalender, fortolkes den datoformel, du f.eks. indtaster i feltet **Transporttid**, i overensstemmelse med kalenderens arbejdsdage.</span><span class="sxs-lookup"><span data-stu-id="6845b-196">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="6845b-197">For eksempel betyder **1U** syv arbejdsdage.</span><span class="sxs-lookup"><span data-stu-id="6845b-197">For example, **1W**  means seven working days.</span></span>

## <a name="see-also"></a><span data-ttu-id="6845b-198">Se også</span><span class="sxs-lookup"><span data-stu-id="6845b-198">See Also</span></span>
<span data-ttu-id="6845b-199">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6845b-199">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="6845b-200">Beregning af forfaldsdato for køb</span><span class="sxs-lookup"><span data-stu-id="6845b-200">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="6845b-201">Indtaste kriterier i filtre</span><span class="sxs-lookup"><span data-stu-id="6845b-201">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  

