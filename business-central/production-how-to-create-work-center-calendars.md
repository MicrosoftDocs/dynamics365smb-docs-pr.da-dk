---
title: Sådan opsættes produktionskalendere | Microsoft Docs
description: En arbejdscenterkalender angiver de arbejdsdage og -timer, arbejdsskift, fridage og fravær, der bestemmer arbejdscentrets tilgængelige bruttokapacitet i henhold til centrets definerede værdier for effektivitet og kapacitet. Du skal udføre nogle forberedende opgaver, før du kan oprette og aktivere en arbejdscenterkalender.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 08999d66adb7327081413b54a338a10fcef7180e
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3190487"
---
# <a name="set-up-shop-calendars"></a><span data-ttu-id="0bfde-104">Konfigurere produktionskalendere</span><span class="sxs-lookup"><span data-stu-id="0bfde-104">Set Up Shop Calendars</span></span>
<span data-ttu-id="0bfde-105">En arbejdscenter- eller produktionsressourcekalender angiver de arbejdsdage og -timer, arbejdsskift, fridage og det fravær, der bestemmer arbejdscentrets tilgængelige bruttokapacitet, målt i tid, i henhold til centrets definerede værdier for effektivitet og kapacitet.</span><span class="sxs-lookup"><span data-stu-id="0bfde-105">A work center or machine calendar specifies the working days and hours, shifts, holidays, and absences that determine the center’s gross available capacity, measured in time, according to its defined efficiency and capacity values.</span></span>

<span data-ttu-id="0bfde-106">Som grundlag for at beregne en bestemt arbejdscenter- eller produktionsressourcekalender skal du først opstille en eller flere generelle produktionskalendere.</span><span class="sxs-lookup"><span data-stu-id="0bfde-106">As a foundation for calculating a specific work or machine center calendar, you must first set up one or more general shop calendars.</span></span> <span data-ttu-id="0bfde-107">En produktionskalender definerer en standardarbejdsuge i form af start- og sluttidspunkter for hver arbejdsdag og de tilhørende arbejdsskift.</span><span class="sxs-lookup"><span data-stu-id="0bfde-107">A shop calendar defines a standard work week according to start and end times of each working day and the work shift relation.</span></span> <span data-ttu-id="0bfde-108">Produktionskalenderen definerer desuden de faste fridage i året.</span><span class="sxs-lookup"><span data-stu-id="0bfde-108">In addition, the shop calendar defines the fixed holidays during a year.</span></span>  

<span data-ttu-id="0bfde-109">Nedenstående beskrives, hvordan du opretter arbejdscenterkalendere.</span><span class="sxs-lookup"><span data-stu-id="0bfde-109">The following describes how to set up work center calendars.</span></span> <span data-ttu-id="0bfde-110">Trinene er de samme som ved oprettelse af produktionsressourcekalendere.</span><span class="sxs-lookup"><span data-stu-id="0bfde-110">The steps are similar when setting up machine center calendars.</span></span>  

## <a name="to-create-work-shifts"></a><span data-ttu-id="0bfde-111">Sådan oprettes arbejdsskift</span><span class="sxs-lookup"><span data-stu-id="0bfde-111">To create work shifts</span></span>  
1.  <span data-ttu-id="0bfde-112">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Arbejdsskift**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="0bfde-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Shifts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0bfde-113">Angiv på en tom linje et tal i feltet **Kode** for at identificere arbejdsskiftet, f.eks. **1**.</span><span class="sxs-lookup"><span data-stu-id="0bfde-113">On a blank line, enter a number in the **Code** field to identify the work shift, for example, **1**.</span></span>  
3.  <span data-ttu-id="0bfde-114">Beskriv arbejdsskiftet i feltet **Beskrivelse**, f.eks. **Første skift**.</span><span class="sxs-lookup"><span data-stu-id="0bfde-114">Describe the work shift in the **Description** field, for example, **1st shift**.</span></span>  
4.  <span data-ttu-id="0bfde-115">Udfyld eventuelt linjer for et andet eller tredje arbejdsskift.</span><span class="sxs-lookup"><span data-stu-id="0bfde-115">Optionally, fill in lines for a second or third work shift.</span></span>  

<span data-ttu-id="0bfde-116">Selvom arbejdscentrene ikke arbejder i forskellige arbejdsskift, skal du angive mindst én arbejdsskiftkode.</span><span class="sxs-lookup"><span data-stu-id="0bfde-116">Even if your work centers do not work in different work shifts, enter at least one work shift code.</span></span>  

## <a name="to-set-up-a-shop-calendar"></a><span data-ttu-id="0bfde-117">Sådan oprettes en produktionskalender</span><span class="sxs-lookup"><span data-stu-id="0bfde-117">To set up a shop calendar</span></span>  
1.  <span data-ttu-id="0bfde-118">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Produktionskalendere**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="0bfde-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shop Calendars**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0bfde-119">Angiv på en tom linje et tal i feltet **Kode** for at identificere produktionskalenderen.</span><span class="sxs-lookup"><span data-stu-id="0bfde-119">On a blank line, enter a number in the **Code** field to identify the shop calendar.</span></span>  
3.  <span data-ttu-id="0bfde-120">Beskriv produktionskalenderen i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="0bfde-120">Describe the shop calendar in the **Description** field.</span></span>  
4.  <span data-ttu-id="0bfde-121">Vælg handlingen **Arbejdsdage**.</span><span class="sxs-lookup"><span data-stu-id="0bfde-121">Choose the **Working Days** action.</span></span>
5.  <span data-ttu-id="0bfde-122">På siden **Arb.dage (produktionskalender)** skal du definere en fuldstændig arbejdsuge med start- og sluttidspunkter for hver dag.</span><span class="sxs-lookup"><span data-stu-id="0bfde-122">On the **Shop Calendar Working Days** page, define a complete work week, with the start and end times for each day.</span></span>  

    <span data-ttu-id="0bfde-123">I feltet **Arbejdsskiftkode** skal du vælge en af de arbejdsskift, du tidligere har defineret.</span><span class="sxs-lookup"><span data-stu-id="0bfde-123">In the **Work Shift Code** field, select one of the shifts that you previously defined.</span></span> <span data-ttu-id="0bfde-124">Tilføj en linje for hver arbejdsdag og hvert skift.</span><span class="sxs-lookup"><span data-stu-id="0bfde-124">Add a line for every working day and every shift.</span></span> <span data-ttu-id="0bfde-125">Eksempler:</span><span class="sxs-lookup"><span data-stu-id="0bfde-125">For example:</span></span>  

    <span data-ttu-id="0bfde-126">Mandag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="0bfde-126">Monday  07:00 15:00 1</span></span>   
    <span data-ttu-id="0bfde-127">Tirsdag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="0bfde-127">Tuesday 07:00 15:00 1</span></span>  

    <span data-ttu-id="0bfde-128">Hvis du vil oprette en produktionskalender med to arbejdsskift, skal du udfylde den på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="0bfde-128">If you need a shop calendar with two work shifts, you must fill it in in this manner:</span></span>  

    <span data-ttu-id="0bfde-129">Mandag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="0bfde-129">Monday 07:00 15:00 1</span></span>   
    <span data-ttu-id="0bfde-130">Mandag 15:00 23:00 2</span><span class="sxs-lookup"><span data-stu-id="0bfde-130">Monday 15:00 23:00 2</span></span>  
    <span data-ttu-id="0bfde-131">Tirsdag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="0bfde-131">Tuesday 07:00 15:00 1</span></span>  
    <span data-ttu-id="0bfde-132">Tirsdag 15:00 23:00 2</span><span class="sxs-lookup"><span data-stu-id="0bfde-132">Tuesday 15:00 23:00 2</span></span>  

    <span data-ttu-id="0bfde-133">Alle ugedage, som du ikke definerer i produktionskalenderen, f.eks. lørdag og søndag, anses automatisk for fridage, og de har ingen tilgængelig kapacitet i arbejdscenterkalenderen.</span><span class="sxs-lookup"><span data-stu-id="0bfde-133">Any week days that you do not define in the shop calendar, such as Saturday and Sunday, are considered non-working days and will have zero available capacity in a work center calendar.</span></span>  

    <span data-ttu-id="0bfde-134">Når alle arbejdsdagene i ugen er defineret, kan du lukke siden **Arb.dage (produktionskalender)** og fortsætte med at angive fridage.</span><span class="sxs-lookup"><span data-stu-id="0bfde-134">When all the working days of a week are defined, you can close the **Shop Calendar Working Days** page and proceed to enter holidays.</span></span>  

6.  <span data-ttu-id="0bfde-135">På siden **Produktionskalendere** skal du vælge produktionskalenderen, og derefter vælge handlingen **Helligdage**.</span><span class="sxs-lookup"><span data-stu-id="0bfde-135">On the **Shop Calendars** page, select the shop calendar, and then choose the **Holidays** action.</span></span>
7. <span data-ttu-id="0bfde-136">På siden **Prod.kalender - fridage** skal du angive årets fridage ved at indtaste startdatoen/-klokkeslættet, sluttidspunktet samt beskrivelsen af hver fridag på enkelte linjer.</span><span class="sxs-lookup"><span data-stu-id="0bfde-136">On the **Shop Calendar Holidays** page, define the holidays of the year by entering the start date and time, the end time, and description of each holiday on individual lines.</span></span> <span data-ttu-id="0bfde-137">Eksempler:</span><span class="sxs-lookup"><span data-stu-id="0bfde-137">For example:</span></span>  

    <span data-ttu-id="0bfde-138">04-07-14 0:00:00 23:59:00 Sommerferie</span><span class="sxs-lookup"><span data-stu-id="0bfde-138">04/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="0bfde-139">05-07-14 0:00:00 23:59:00 Sommerferie</span><span class="sxs-lookup"><span data-stu-id="0bfde-139">05/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="0bfde-140">06-07-14 0:00:00 23:59:00 Sommerferie</span><span class="sxs-lookup"><span data-stu-id="0bfde-140">06/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  

<span data-ttu-id="0bfde-141">De definerede fridage har ingen tilgængelig kapacitet i en arbejdscenterkalender.</span><span class="sxs-lookup"><span data-stu-id="0bfde-141">The defined holidays will have zero available capacity in a work center calendar.</span></span>  

<span data-ttu-id="0bfde-142">Produktionskalenderen kan nu knyttes til et arbejdscenter for at beregne den arbejdscenterkalender, der skal styre alle operationsplaner i løbet af tiden på arbejdscentret.</span><span class="sxs-lookup"><span data-stu-id="0bfde-142">The shop calendar can now be assigned to a work center to calculate the work shop calendar that will govern all operation scheduling at that work center.</span></span>  

## <a name="to-calculate-a-work-center-calendar"></a><span data-ttu-id="0bfde-143">Sådan beregnes en arbejdscenterkalender</span><span class="sxs-lookup"><span data-stu-id="0bfde-143">To calculate a work center calendar</span></span>  

1.  <span data-ttu-id="0bfde-144">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Arbejdscentre**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="0bfde-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Centers**, and then choose the related link.</span></span>
2. <span data-ttu-id="0bfde-145">Åbn det arbejdscenter, du vil opdatere.</span><span class="sxs-lookup"><span data-stu-id="0bfde-145">Open the work center that you want to update.</span></span>  
3. <span data-ttu-id="0bfde-146">Vælg hvilken produktionskalender, der skal bruges som grundlag for en arbejdscenterkalender i feltet **Produktionskalenderkode**.</span><span class="sxs-lookup"><span data-stu-id="0bfde-146">In the **Shop Calendar Code** field, select which shop calendar to use as the foundation for a work center calendar.</span></span>  
4. <span data-ttu-id="0bfde-147">Vælg handlingen **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="0bfde-147">Choose the **Calendar** action.</span></span>  
5. <span data-ttu-id="0bfde-148">På siden **Arbejdscenterkalender** skal du vælge handlingen **Vis matrix**.</span><span class="sxs-lookup"><span data-stu-id="0bfde-148">On the **Work Center Calendar** page, choose the **Show Matrix** action.</span></span>  

    <span data-ttu-id="0bfde-149">I venstre side af matrixsiden vises de konfigurerede arbejdscentre.</span><span class="sxs-lookup"><span data-stu-id="0bfde-149">The left side of the matrix page lists the work centers that are set up.</span></span> <span data-ttu-id="0bfde-150">I højre side vises en tidskalender med værdierne for tilgængelig kapacitet pr. arbejdsdag i den definerede enhed, f.eks. **480** (minutter).</span><span class="sxs-lookup"><span data-stu-id="0bfde-150">The right side shows a calendar displaying the available capacity values for each working day in the defined unit of measure, for example, **480** minutes.</span></span> <span data-ttu-id="0bfde-151">Hver linje repræsenterer kalenderen for et arbejdscenter.</span><span class="sxs-lookup"><span data-stu-id="0bfde-151">Each line represents the calendar of one work center.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="0bfde-152">Du kan også vælge at få vist kapacitetsværdien for hver uge eller måned ved at ændre indstillingen i feltet **Vis efter** på siden **Arbejdscenterkalender**.</span><span class="sxs-lookup"><span data-stu-id="0bfde-152">You can also select to view the capacity values for each week or month by changing the selection in the **View By** field on the **Work Center Calendar** page.</span></span>  

    <span data-ttu-id="0bfde-153">For at afspejle den nye produktionskalender som en linje i det markerede arbejdscenter, skal den først beregnes.</span><span class="sxs-lookup"><span data-stu-id="0bfde-153">To reflect the new shop calendar as a line on the selected work center, it must first be calculated.</span></span>  

6.  <span data-ttu-id="0bfde-154">Vælg handlingen **Beregn**.</span><span class="sxs-lookup"><span data-stu-id="0bfde-154">Choose the **Calculate** action.</span></span>  
7.  <span data-ttu-id="0bfde-155">Du kan angive et filter i oversigtspanelet **Arbejdscenter**, hvis du kun vil udføre beregningen for ét arbejdscenter.</span><span class="sxs-lookup"><span data-stu-id="0bfde-155">On the **Work Center** FastTab, you can set a filter to only calculate for one work center.</span></span> <span data-ttu-id="0bfde-156">Hvis du ikke filtrerer, beregnes alle eksisterende arbejdscenterkalendere.</span><span class="sxs-lookup"><span data-stu-id="0bfde-156">If you do not set a filter, all existing work center calendars will be calculated.</span></span>  
8.  <span data-ttu-id="0bfde-157">Definer start- og slutdatoerne for den kalenderperiode, der skal beregnes, f.eks. et år fra 01/01/14 til 31/12/14.</span><span class="sxs-lookup"><span data-stu-id="0bfde-157">Define the starting and ending dates of the calendar period that should be calculated, for example, one year from 01/01/14 to 31/12/14.</span></span>
9. <span data-ttu-id="0bfde-158">Vælg knappen **OK** for at beregne kapaciteten.</span><span class="sxs-lookup"><span data-stu-id="0bfde-158">Choose the **OK** button to calculate capacity.</span></span>  

<span data-ttu-id="0bfde-159">Der er nu oprettet (eller opdateret) kalenderindgange, som viser den tilgængelige kapacitet for hver periode i overensstemmelse med følgende 3 sæt stamdata:</span><span class="sxs-lookup"><span data-stu-id="0bfde-159">Calendar entries are now created or updated displaying the available capacity for each period according to the following three sets of master data:</span></span>  

- <span data-ttu-id="0bfde-160">De arbejdsdage og arbejdsskift, der er defineret i den tilknyttede produktionskalender.</span><span class="sxs-lookup"><span data-stu-id="0bfde-160">The working days and shift defined in the assigned shop calendar.</span></span>  
- <span data-ttu-id="0bfde-161">Værdien i feltet **Kapacitet** på arbejdscenterkortet.</span><span class="sxs-lookup"><span data-stu-id="0bfde-161">The value in the **Capacity** field on the work center card.</span></span>  
- <span data-ttu-id="0bfde-162">Værdien i feltet **Effektivitet** på arbejdscenterkortet.</span><span class="sxs-lookup"><span data-stu-id="0bfde-162">The value in the **Efficiency** field on the work center card.</span></span>  

<span data-ttu-id="0bfde-163">Den beregnede arbejdscenterkalender definerer nu, hvor meget kapacitet der er tilgængelig på dette arbejdscenter.</span><span class="sxs-lookup"><span data-stu-id="0bfde-163">The calculated work center calendar will now define when and how much capacity is available at this work center.</span></span> <span data-ttu-id="0bfde-164">Dette styrer den detaljerede planlægning af operationer, der udføres på arbejdscenter.</span><span class="sxs-lookup"><span data-stu-id="0bfde-164">This controls the detailed scheduling of operations performed at the work center.</span></span>  

## <a name="to-record-work-center-absence"></a><span data-ttu-id="0bfde-165">Sådan registreres fraværet på arbejdscentret</span><span class="sxs-lookup"><span data-stu-id="0bfde-165">To record work center absence</span></span>  
1.  <span data-ttu-id="0bfde-166">På siden **Arbejdscenterkalender** skal du vælge handlingen **Vis matrix**.</span><span class="sxs-lookup"><span data-stu-id="0bfde-166">On the **Work Center Calendar** page, choose the **Show Matrix** action.</span></span>
2. <span data-ttu-id="0bfde-167">Vælg det arbejdscenter og den kalenderdag, fraværstiden skal registreres for, på siden **Matrix for arbejdscenterkalender**, og klik derefter på handlingen **Fravær**.</span><span class="sxs-lookup"><span data-stu-id="0bfde-167">On the **Work Center Calendar Matrix** page, select the work center and calendar day when the absence time should be recorded, and then choose the **Absence** action.</span></span>  
3.  <span data-ttu-id="0bfde-168">Definer starttidspunktet, sluttidspunktet og beskrivelsen for dagens fravær på siden **Fravær**.</span><span class="sxs-lookup"><span data-stu-id="0bfde-168">On the **Absence** page, define the starting time, ending time, and description of that day’s absence.</span></span> <span data-ttu-id="0bfde-169">Eksempler:</span><span class="sxs-lookup"><span data-stu-id="0bfde-169">For example:</span></span>  

    <span data-ttu-id="0bfde-170">25-01-01 08:00 10:00 Reparation</span><span class="sxs-lookup"><span data-stu-id="0bfde-170">25/01/01 08:00 10:00 Maintenance</span></span>  

4.  <span data-ttu-id="0bfde-171">Vælg handlingen **Opdatering**, og luk derefter siden **Fravær**.</span><span class="sxs-lookup"><span data-stu-id="0bfde-171">Choose the **Update** action, and then close the **Absence** page.</span></span>  

<span data-ttu-id="0bfde-172">Kapaciteten på den markerede dag er nu reduceret med den registrerede fraværstid.</span><span class="sxs-lookup"><span data-stu-id="0bfde-172">The capacity of the selected day has now decreased by the recorded absence time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0bfde-173">Se også</span><span class="sxs-lookup"><span data-stu-id="0bfde-173">See Also</span></span>  
[<span data-ttu-id="0bfde-174">Konfigurere basiskalendere</span><span class="sxs-lookup"><span data-stu-id="0bfde-174">Set Up Base Calendars</span></span>](across-how-to-assign-base-calendars.md)  
[<span data-ttu-id="0bfde-175">Konfigurere arbejdscentre og produktionsressourcer</span><span class="sxs-lookup"><span data-stu-id="0bfde-175">Set Up Work Centers and Machine Centers</span></span>](production-how-to-set-up-work-and-machine-centers.md)  
[<span data-ttu-id="0bfde-176">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="0bfde-176">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
[<span data-ttu-id="0bfde-177">Produktion</span><span class="sxs-lookup"><span data-stu-id="0bfde-177">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="0bfde-178">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0bfde-178">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
