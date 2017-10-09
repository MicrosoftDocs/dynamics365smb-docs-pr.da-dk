---
title: "Sådan opsættes produktionskalendere | Microsoft Docs"
description: "En arbejdscenterkalender angiver de arbejdsdage og -timer, arbejdsskift, fridage og fravær, der bestemmer arbejdscentrets tilgængelige bruttokapacitet i henhold til centrets definerede værdier for effektivitet og kapacitet. Du skal udføre nogle forberedende opgaver, før du kan oprette og aktivere en arbejdscenterkalender."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: f42941328d49aee4e823007284fd14417866cbae
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-shop-calendars"></a><span data-ttu-id="89c26-104">Sådan opsættes produktionskalendere</span><span class="sxs-lookup"><span data-stu-id="89c26-104">How to: Set Up Shop Calendars</span></span>
<span data-ttu-id="89c26-105">En arbejdscenter- eller produktionsressourcekalender angiver de arbejdsdage og -timer, arbejdsskift, fridage og det fravær, der bestemmer arbejdscentrets tilgængelige bruttokapacitet, målt i tid, i henhold til centrets definerede værdier for effektivitet og kapacitet.</span><span class="sxs-lookup"><span data-stu-id="89c26-105">A work center or machine calendar specifies the working days and hours, shifts, holidays, and absences that determine the center’s gross available capacity, measured in time, according to its defined efficiency and capacity values.</span></span>

<span data-ttu-id="89c26-106">Som grundlag for at beregne en bestemt arbejdscenter- eller produktionsressourcekalender skal du først opstille en eller flere generelle produktionskalendere.</span><span class="sxs-lookup"><span data-stu-id="89c26-106">As a foundation for calculating a specific work or machine center calendar, you must first set up one or more general shop calendars.</span></span> <span data-ttu-id="89c26-107">En produktionskalender definerer en standardarbejdsuge i form af start- og sluttidspunkter for hver arbejdsdag og de tilhørende arbejdsskift.</span><span class="sxs-lookup"><span data-stu-id="89c26-107">A shop calendar defines a standard work week according to start and end times of each working day and the work shift relation.</span></span> <span data-ttu-id="89c26-108">Produktionskalenderen definerer desuden de faste fridage i året.</span><span class="sxs-lookup"><span data-stu-id="89c26-108">In addition, the shop calendar defines the fixed holidays during a year.</span></span>  

<span data-ttu-id="89c26-109">Nedenstående beskrives, hvordan du opretter arbejdscenterkalendere.</span><span class="sxs-lookup"><span data-stu-id="89c26-109">The following describes how to set up work center calendars.</span></span> <span data-ttu-id="89c26-110">Trinene er de samme som ved oprettelse af produktionsressourcekalendere.</span><span class="sxs-lookup"><span data-stu-id="89c26-110">The steps are similar when setting up machine center calendars.</span></span>  

## <a name="to-create-work-shifts"></a><span data-ttu-id="89c26-111">Sådan oprettes arbejdsskift</span><span class="sxs-lookup"><span data-stu-id="89c26-111">To create work shifts</span></span>  
1.  <span data-ttu-id="89c26-112">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), og angiv **Arbejdsskift**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="89c26-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Shifts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="89c26-113">Angiv på en tom linje et tal i feltet **Kode** for at identificere arbejdsskiftet, f.eks. **1**.</span><span class="sxs-lookup"><span data-stu-id="89c26-113">On a blank line, enter a number in the **Code** field to identify the work shift, for example, **1**.</span></span>  
3.  <span data-ttu-id="89c26-114">Beskriv arbejdsskiftet i feltet **Beskrivelse**, f.eks. **Første skift**.</span><span class="sxs-lookup"><span data-stu-id="89c26-114">Describe the work shift in the **Description** field, for example, **1st shift**.</span></span>  
4.  <span data-ttu-id="89c26-115">Udfyld eventuelt linjer for et andet eller tredje arbejdsskift.</span><span class="sxs-lookup"><span data-stu-id="89c26-115">Optionally, fill in lines for a second or third work shift.</span></span>  

<span data-ttu-id="89c26-116">Selvom arbejdscentrene ikke arbejder i forskellige arbejdsskift, skal du angive mindst én arbejdsskiftkode.</span><span class="sxs-lookup"><span data-stu-id="89c26-116">Even if your work centers do not work in different work shifts, enter at least one work shift code.</span></span>  

## <a name="to-set-up-a-shop-calendar"></a><span data-ttu-id="89c26-117">Sådan oprettes en produktionskalender</span><span class="sxs-lookup"><span data-stu-id="89c26-117">To set up a shop calendar</span></span>  
1.  <span data-ttu-id="89c26-118">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), og angiv **Arbejdsskift**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="89c26-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Shop Calendars**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="89c26-119">Angiv på en tom linje et tal i feltet **Kode** for at identificere produktionskalenderen.</span><span class="sxs-lookup"><span data-stu-id="89c26-119">On a blank line, enter a number in the **Code** field to identify the shop calendar.</span></span>  
3.  <span data-ttu-id="89c26-120">Beskriv produktionskalenderen i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="89c26-120">Describe the shop calendar in the **Description** field.</span></span>  
4.  <span data-ttu-id="89c26-121">Vælg handlingen **Arbejdsdage**.</span><span class="sxs-lookup"><span data-stu-id="89c26-121">Choose the **Working Days** action.</span></span>
5.  <span data-ttu-id="89c26-122">I feltet **Arb.dage (produktionskalender)** skal du definere en fuldstændig arbejdsuge med start- og sluttidspunkter for hver dag.</span><span class="sxs-lookup"><span data-stu-id="89c26-122">In the **Shop Calendar Working Days** window, define a complete work week, with the start and end times for each day.</span></span>  

    <span data-ttu-id="89c26-123">I feltet **Arbejdsskiftkode** skal du vælge en af de arbejdsskift, du tidligere har defineret.</span><span class="sxs-lookup"><span data-stu-id="89c26-123">In the **Work Shift Code** field, select one of the shifts that you previously defined.</span></span> <span data-ttu-id="89c26-124">Tilføj en linje for hver arbejdsdag og hvert skift.</span><span class="sxs-lookup"><span data-stu-id="89c26-124">Add a line for every working day and every shift.</span></span> <span data-ttu-id="89c26-125">Eksempler:</span><span class="sxs-lookup"><span data-stu-id="89c26-125">For example:</span></span>  

    <span data-ttu-id="89c26-126">Mandag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="89c26-126">Monday  07:00 15:00 1</span></span>   
    <span data-ttu-id="89c26-127">Tirsdag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="89c26-127">Tuesday 07:00 15:00 1</span></span>  

    <span data-ttu-id="89c26-128">Hvis du vil oprette en produktionskalender med to arbejdsskift, skal du udfylde den på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="89c26-128">If you need a shop calendar with two work shifts, you must fill it in in this manner:</span></span>  

    <span data-ttu-id="89c26-129">Mandag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="89c26-129">Monday 07:00 15:00 1</span></span>   
    <span data-ttu-id="89c26-130">Mandag 15:00 23:00 2</span><span class="sxs-lookup"><span data-stu-id="89c26-130">Monday 15:00 23:00 2</span></span>  
    <span data-ttu-id="89c26-131">Tirsdag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="89c26-131">Tuesday 07:00 15:00 1</span></span>  
    <span data-ttu-id="89c26-132">Tirsdag 15:00 23:00 2</span><span class="sxs-lookup"><span data-stu-id="89c26-132">Tuesday 15:00 23:00 2</span></span>  

    <span data-ttu-id="89c26-133">Alle ugedage, som du ikke definerer i produktionskalenderen, f.eks. lørdag og søndag, anses automatisk for fridage, og de har ingen tilgængelig kapacitet i arbejdscenterkalenderen.</span><span class="sxs-lookup"><span data-stu-id="89c26-133">Any week days that you do not define in the shop calendar, such as Saturday and Sunday, are considered non-working days and will have zero available capacity in a work center calendar.</span></span>  

    <span data-ttu-id="89c26-134">Når alle arbejdsdagene i ugen er defineret, kan du lukke vinduet **Arb.dage (produktionskalender)** og fortsætte med at angive fridage.</span><span class="sxs-lookup"><span data-stu-id="89c26-134">When all the working days of a week are defined, you can close the **Shop Calendar Working Days** window and proceed to enter holidays.</span></span>  

6.  <span data-ttu-id="89c26-135">I vinduet **Produktionskalendere** skal du vælge produktionskalenderen, og derefter vælge handlingen **Helligdage**.</span><span class="sxs-lookup"><span data-stu-id="89c26-135">In the **Shop Calendars** window, select the shop calendar, and then choose the **Holidays** action.</span></span>
7. <span data-ttu-id="89c26-136">I vinduet **Prod.kalender - fridage** skal du angive årets fridage ved at indtaste startdatoen/-klokkeslættet, sluttidspunktet samt beskrivelsen af hver fridag på enkelte linjer.</span><span class="sxs-lookup"><span data-stu-id="89c26-136">In the **Shop Calendar Holidays** window, define the holidays of the year by entering the start date and time, the end time, and description of each holiday on individual lines.</span></span> <span data-ttu-id="89c26-137">Eksempler:</span><span class="sxs-lookup"><span data-stu-id="89c26-137">For example:</span></span>  

    <span data-ttu-id="89c26-138">04-07-14 0:00:00 23:59:00 Sommerferie</span><span class="sxs-lookup"><span data-stu-id="89c26-138">04/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="89c26-139">05-07-14 0:00:00 23:59:00 Sommerferie</span><span class="sxs-lookup"><span data-stu-id="89c26-139">05/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="89c26-140">06-07-14 0:00:00 23:59:00 Sommerferie</span><span class="sxs-lookup"><span data-stu-id="89c26-140">06/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  

<span data-ttu-id="89c26-141">De definerede fridage har ingen tilgængelig kapacitet i en arbejdscenterkalender.</span><span class="sxs-lookup"><span data-stu-id="89c26-141">The defined holidays will have zero available capacity in a work center calendar.</span></span>  

<span data-ttu-id="89c26-142">Produktionskalenderen kan nu knyttes til et arbejdscenter for at beregne den arbejdscenterkalender, der skal styre alle operationsplaner i løbet af tiden på arbejdscentret.</span><span class="sxs-lookup"><span data-stu-id="89c26-142">The shop calendar can now be assigned to a work center to calculate the work shop calendar that will govern all operation scheduling at that work center.</span></span>  

## <a name="to-calculate-a-work-center-calendar"></a><span data-ttu-id="89c26-143">Sådan beregnes en arbejdscenterkalender</span><span class="sxs-lookup"><span data-stu-id="89c26-143">To calculate a work center calendar</span></span>  

1.  <span data-ttu-id="89c26-144">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), og angiv **Arbejdsskift**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="89c26-144">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Centers**, and then choose the related link.</span></span>
2. <span data-ttu-id="89c26-145">Åbn det arbejdscenter, du vil opdatere.</span><span class="sxs-lookup"><span data-stu-id="89c26-145">Open the work center that you want to update.</span></span>  
3. <span data-ttu-id="89c26-146">Vælg hvilken produktionskalender, der skal bruges som grundlag for en arbejdscenterkalender i feltet **Produktionskalenderkode**.</span><span class="sxs-lookup"><span data-stu-id="89c26-146">In the **Shop Calendar Code** field, select which shop calendar to use as the foundation for a work center calendar.</span></span>  
4. <span data-ttu-id="89c26-147">Vælg handlingen **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="89c26-147">Choose the **Calendar** action.</span></span>  
5. <span data-ttu-id="89c26-148">I vinduet **Arbejdscenterkalender** skal du vælge handlingen **Vis matrix**.</span><span class="sxs-lookup"><span data-stu-id="89c26-148">In the **Work Center Calendar** window, choose the **Show Matrix** action.</span></span>  

    <span data-ttu-id="89c26-149">I venstre side af matrixvinduet vises de konfigurerede arbejdscentre.</span><span class="sxs-lookup"><span data-stu-id="89c26-149">The left side of the matrix window lists the work centers that are set up.</span></span> <span data-ttu-id="89c26-150">I højre side vises en tidskalender med værdierne for tilgængelig kapacitet pr. arbejdsdag i den definerede enhed, f.eks. **480** (minutter).</span><span class="sxs-lookup"><span data-stu-id="89c26-150">The right side shows a calendar displaying the available capacity values for each working day in the defined unit of measure, for example, **480** minutes.</span></span> <span data-ttu-id="89c26-151">Hver linje repræsenterer kalenderen for et arbejdscenter.</span><span class="sxs-lookup"><span data-stu-id="89c26-151">Each line represents the calendar of one work center.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="89c26-152">Du kan også vælge at få vist kapacitetsværdien for hver uge eller måned ved at ændre indstillingen i feltet **Vis efter** i vinduet **Arbejdscenterkalender**.</span><span class="sxs-lookup"><span data-stu-id="89c26-152">You can also select to view the capacity values for each week or month by changing the selection in the **View By** field in the **Work Center Calendar** window.</span></span>  

    <span data-ttu-id="89c26-153">For at afspejle den nye produktionskalender som en linje i det markerede arbejdscenter, skal den først beregnes.</span><span class="sxs-lookup"><span data-stu-id="89c26-153">To reflect the new shop calendar as a line on the selected work center, it must first be calculated.</span></span>  

6.  <span data-ttu-id="89c26-154">Vælg handlingen **Beregn**.</span><span class="sxs-lookup"><span data-stu-id="89c26-154">Choose the **Calculate** action.</span></span>  
7.  <span data-ttu-id="89c26-155">Du kan angive et filter i oversigtspanelet **Arbejdscenter**, hvis du kun vil udføre beregningen for ét arbejdscenter.</span><span class="sxs-lookup"><span data-stu-id="89c26-155">On the **Work Center** FastTab, you can set a filter to only calculate for one work center.</span></span> <span data-ttu-id="89c26-156">Hvis du ikke filtrerer, beregnes alle eksisterende arbejdscenterkalendere.</span><span class="sxs-lookup"><span data-stu-id="89c26-156">If you do not set a filter, all existing work center calendars will be calculated.</span></span>  
8.  <span data-ttu-id="89c26-157">Definer start- og slutdatoerne for den kalenderperiode, der skal beregnes, f.eks. et år fra 01/01/14 til 31/12/14.</span><span class="sxs-lookup"><span data-stu-id="89c26-157">Define the starting and ending dates of the calendar period that should be calculated, for example, one year from 01/01/14 to 31/12/14.</span></span>
9. <span data-ttu-id="89c26-158">Vælg knappen **OK** for at beregne kapaciteten.</span><span class="sxs-lookup"><span data-stu-id="89c26-158">Choose the **OK** button to calculate capacity.</span></span>  

<span data-ttu-id="89c26-159">Der er nu oprettet (eller opdateret) kalenderindgange, som viser den tilgængelige kapacitet for hver periode i overensstemmelse med følgende 3 sæt stamdata:</span><span class="sxs-lookup"><span data-stu-id="89c26-159">Calendar entries are now created or updated displaying the available capacity for each period according to the following three sets of master data:</span></span>  

- <span data-ttu-id="89c26-160">De arbejdsdage og arbejdsskift, der er defineret i den tilknyttede produktionskalender.</span><span class="sxs-lookup"><span data-stu-id="89c26-160">The working days and shift defined in the assigned shop calendar.</span></span>  
- <span data-ttu-id="89c26-161">Værdien i feltet **Kapacitet** på arbejdscenterkortet.</span><span class="sxs-lookup"><span data-stu-id="89c26-161">The value in the **Capacity** field on the work center card.</span></span>  
- <span data-ttu-id="89c26-162">Værdien i feltet **Effektivitet** på arbejdscenterkortet.</span><span class="sxs-lookup"><span data-stu-id="89c26-162">The value in the **Efficiency** field on the work center card.</span></span>  

<span data-ttu-id="89c26-163">Den beregnede arbejdscenterkalender definerer nu, hvor meget kapacitet der er tilgængelig på dette arbejdscenter.</span><span class="sxs-lookup"><span data-stu-id="89c26-163">The calculated work center calendar will now define when and how much capacity is available at this work center.</span></span> <span data-ttu-id="89c26-164">Dette styrer den detaljerede planlægning af operationer, der udføres på arbejdscenter.</span><span class="sxs-lookup"><span data-stu-id="89c26-164">This controls the detailed scheduling of operations performed at the work center.</span></span>  

## <a name="to-record-work-center-absence"></a><span data-ttu-id="89c26-165">Sådan registreres fraværet på arbejdscentret</span><span class="sxs-lookup"><span data-stu-id="89c26-165">To record work center absence</span></span>  
1.  <span data-ttu-id="89c26-166">I vinduet **Arbejdscenterkalender** skal du vælge handlingen **Vis matrix**.</span><span class="sxs-lookup"><span data-stu-id="89c26-166">In the **Work Center Calendar** window, choose the **Show Matrix** action.</span></span>
2. <span data-ttu-id="89c26-167">Vælg det arbejdscenter og den kalenderdag, fraværstiden skal registreres for, i vinduet **Matrix for arbejdscenterkalender**, og klik derefter på handlingen **Fravær**.</span><span class="sxs-lookup"><span data-stu-id="89c26-167">In the **Work Center Calendar Matrix** window, select the work center and calendar day when the absence time should be recorded, and then choose the **Absence** action.</span></span>  
3.  <span data-ttu-id="89c26-168">Definer starttidspunktet, sluttidspunktet og beskrivelsen for dagens fravær i vinduet **Fravær**.</span><span class="sxs-lookup"><span data-stu-id="89c26-168">In the **Absence** window, define the starting time, ending time, and description of that day’s absence.</span></span> <span data-ttu-id="89c26-169">Eksempler:</span><span class="sxs-lookup"><span data-stu-id="89c26-169">For example:</span></span>  

    <span data-ttu-id="89c26-170">25-01-01 08:00 10:00 Reparation</span><span class="sxs-lookup"><span data-stu-id="89c26-170">25/01/01 08:00 10:00 Maintenance</span></span>  

4.  <span data-ttu-id="89c26-171">Vælg handlingen **Opdatering**, og luk derefter vinduet **Fravær**.</span><span class="sxs-lookup"><span data-stu-id="89c26-171">Choose the **Update** action, and then close the **Absence** window.</span></span>  

<span data-ttu-id="89c26-172">Kapaciteten på den markerede dag er nu reduceret med den registrerede fraværstid.</span><span class="sxs-lookup"><span data-stu-id="89c26-172">The capacity of the selected day has now decreased by the recorded absence time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="89c26-173">Se også</span><span class="sxs-lookup"><span data-stu-id="89c26-173">See Also</span></span>  
[<span data-ttu-id="89c26-174">Fremgangsmåde: Opsætte basiskalendere</span><span class="sxs-lookup"><span data-stu-id="89c26-174">How to: Set Up Base Calendars</span></span>](across-how-to-assign-base-calendars.md)  
[<span data-ttu-id="89c26-175">Fremgangsmåde: Konfigurere arbejdscentre og produktionsressourcer</span><span class="sxs-lookup"><span data-stu-id="89c26-175">How to: Set Up Work Centers and Machine Centers</span></span>](production-how-to-set-up-work-and-machine-centers.md)  
[<span data-ttu-id="89c26-176">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="89c26-176">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
[<span data-ttu-id="89c26-177">Produktion</span><span class="sxs-lookup"><span data-stu-id="89c26-177">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="89c26-178">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="89c26-178">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

