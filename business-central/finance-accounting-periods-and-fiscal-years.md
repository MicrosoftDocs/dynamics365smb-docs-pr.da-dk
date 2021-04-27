---
title: Arbejde med regnskabsperioder og regnskabsår | Microsoft Docs
description: Lær, hvordan du arbejder med regnskabsperioder, der kan definere, hvornår virksomheden rapporterer finansielle resultater.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: b4daacd73987e4e747f97d288ecfb51b564de7e6
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781032"
---
# <a name="working-with-accounting-periods-and-fiscal-years"></a><span data-ttu-id="d92a6-103">Arbejde med regnskabsperioder og regnskabsår</span><span class="sxs-lookup"><span data-stu-id="d92a6-103">Working with Accounting Periods and Fiscal Years</span></span>

<span data-ttu-id="d92a6-104">Regnskabsperioder, der kaldes også rapporteringsperioder, er tidsperioder, hvor en virksomhed eller organisation rapporterer finansielle resultater, f.eks. ved at generere deres resultatopgørelse eller balance.</span><span class="sxs-lookup"><span data-stu-id="d92a6-104">Accounting periods, which are also known as reporting periods, are periods of time for which a company or organization reports financial performance, for example, by generating their income statement or balance sheet.</span></span> <span data-ttu-id="d92a6-105">Typisk henviser regnskabsperioder til virksomhedens regnskabsår, der kan indeholde flere regnskabsperioder, f.eks. måneder eller kvartaler.</span><span class="sxs-lookup"><span data-stu-id="d92a6-105">Typically, accounting periods refer to the company's fiscal year, which can contain several accounting periods, such as months or quarters.</span></span>

<span data-ttu-id="d92a6-106">For mange virksomheder falder regnskabsåret ikke sammen med kalenderåret.</span><span class="sxs-lookup"><span data-stu-id="d92a6-106">For many companies the fiscal year does not align with the calendar year.</span></span> <span data-ttu-id="d92a6-107">For eksempel kan regnskabsåret slutte den 30 juni i stedet for 31. december.</span><span class="sxs-lookup"><span data-stu-id="d92a6-107">For example, the fiscal year might end on June 30th rather than December 31st.</span></span> <span data-ttu-id="d92a6-108">For nyoprettede virksomheder kan regnskabsåret i realiteten være længere end 12 måneder.</span><span class="sxs-lookup"><span data-stu-id="d92a6-108">For newly created companies, the fiscal might actually be longer than 12 months.</span></span>  

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="d92a6-109">kræver kun regnskabsperioder, hvis du vil lukke en resultatopgørelse eller udføre opgaver til komprimering af data.</span><span class="sxs-lookup"><span data-stu-id="d92a6-109">only requires accounting periods only if you want to close an income statement, or run data compression tasks.</span></span> 

<span data-ttu-id="d92a6-110">Du kan bruge regnskabsperioder i forbindelse med rapportering.</span><span class="sxs-lookup"><span data-stu-id="d92a6-110">You can use accounting periods in reporting.</span></span> <span data-ttu-id="d92a6-111">F.eks. når du gennemgår bogførte poster på siden **Saldo/Budget**, hvor du kan angive rapporteringsintervallet.</span><span class="sxs-lookup"><span data-stu-id="d92a6-111">For example, when you are reviewing posted entries on the **Balance/Budget** page where the reporting interval can be specified.</span></span> <span data-ttu-id="d92a6-112">En af de indstillinger kan du angive for at rapportere regnskabsperiode.</span><span class="sxs-lookup"><span data-stu-id="d92a6-112">One of the options you may specify to report by accounting period.</span></span> <span data-ttu-id="d92a6-113">Du kan også oprette et kontoskema, der sammenligner resultaterne for forskellige perioder.</span><span class="sxs-lookup"><span data-stu-id="d92a6-113">You can also build an account schedule that compares results for different accounting periods.</span></span>

## <a name="creating-a-new-fiscal-year"></a><span data-ttu-id="d92a6-114">Oprette et nyt regnskabsår</span><span class="sxs-lookup"><span data-stu-id="d92a6-114">Creating a new fiscal year</span></span>

<span data-ttu-id="d92a6-115">Du kan oprette flere regnskabsperioder ad gangen ved hjælp af **Opret regnskabsår**-kørslen eller manuelt.</span><span class="sxs-lookup"><span data-stu-id="d92a6-115">You can create accounting periods in bulk, by using the **Create Fiscal Year** batch job, or manually.</span></span>

### <a name="how-to-create-accounting-periods-in-bulk"></a><span data-ttu-id="d92a6-116">Sådan oprettes flere regnskabsperioder ad gangen</span><span class="sxs-lookup"><span data-stu-id="d92a6-116">How to create accounting periods in-bulk</span></span>

<span data-ttu-id="d92a6-117">Brug **Opret regnskabsår**-kørslen til at opdele et regnskabsår i perioder af samme varighed.</span><span class="sxs-lookup"><span data-stu-id="d92a6-117">Use the **Create Fiscal Year** batch job to divide a fiscal year into periods of equal length.</span></span>  

1. <span data-ttu-id="d92a6-118">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Regnskabsperioder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d92a6-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Accounting Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d92a6-119">Vælg handlingen **Opret år**.</span><span class="sxs-lookup"><span data-stu-id="d92a6-119">Choose the **Create Year** action.</span></span>  <!--What about the Scheduling option? Should we mention that? There's also the Report Output Type field...-->
3. <span data-ttu-id="d92a6-120">I feltet **Startdato** kan du angive den dato, hvor regnskabsåret begynder.</span><span class="sxs-lookup"><span data-stu-id="d92a6-120">In the **Starting Date** field, enter the date on which the fiscal year starts.</span></span>  
4. <span data-ttu-id="d92a6-121">I feltet **Antal perioder** kan du angive det antal perioder, du vil opdele regnskabsåret i.</span><span class="sxs-lookup"><span data-stu-id="d92a6-121">In the **No. of Periods** field, enter the number of accounting periods to divide the fiscal year into.</span></span> <span data-ttu-id="d92a6-122">Der kan være op til 365 perioder pr. år.</span><span class="sxs-lookup"><span data-stu-id="d92a6-122">There can be up to 365 periods in a year.</span></span>  
5. <span data-ttu-id="d92a6-123">I feltet **Periodelængde** skal du angive en varighed for hver periode.</span><span class="sxs-lookup"><span data-stu-id="d92a6-123">In the **Period Length** field, enter a duration for each period.</span></span> <span data-ttu-id="d92a6-124">F.eks. 1M for én måned, 1K for et kvartal og 1Å for et år.</span><span class="sxs-lookup"><span data-stu-id="d92a6-124">For example, 1M for one month, 1Q for one quarter, and 1Y for one year.</span></span>  
6. <span data-ttu-id="d92a6-125">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d92a6-125">Choose **OK**.</span></span>  

### <a name="how-to-create-accounting-periods-manually"></a><span data-ttu-id="d92a6-126">Sådan oprettes regnskabsperioder manuelt</span><span class="sxs-lookup"><span data-stu-id="d92a6-126">How to create accounting periods manually</span></span>

<span data-ttu-id="d92a6-127">Hvis regnskabsperioderne i regnskabsåret, der har forskellig varigheder som 4-4-5-kalender, der anvendes i detail, du kan oprette det manuelt.</span><span class="sxs-lookup"><span data-stu-id="d92a6-127">If the accounting periods in your fiscal year have different durations, like the 4-4-5 calendar used in retail, you can manually set it up.</span></span>  
  
1. <span data-ttu-id="d92a6-128">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Regnskabsperioder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d92a6-128">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Accounting Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d92a6-129">I feltet **Startdato** kan du angive den dato, hvor regnskabsåret begynder.</span><span class="sxs-lookup"><span data-stu-id="d92a6-129">In the **Starting Date** field, enter the date on which the fiscal year starts.</span></span> <span data-ttu-id="d92a6-130">Feltet **Navn** viser navnet på måneden.</span><span class="sxs-lookup"><span data-stu-id="d92a6-130">The **Name** field will show the name of the month.</span></span>  
3. <span data-ttu-id="d92a6-131">Marker afkrydsningsfeltet **Nyt regnskabsår** for at angive, at dette er den første periode i året.</span><span class="sxs-lookup"><span data-stu-id="d92a6-131">Choose the **New Fiscal Year** check box to indicate that this is the first period in the year.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="d92a6-132">bruger denne periode til at bestemme, hvilke perioder der skal lukkes ved udgangen af året.</span><span class="sxs-lookup"><span data-stu-id="d92a6-132">will use this period to determine which periods to close at year-end.</span></span>
4. <span data-ttu-id="d92a6-133">Gentag trin 2 og 3 for hver resterende periode.</span><span class="sxs-lookup"><span data-stu-id="d92a6-133">Repeat steps 2 and 3 for each remaining period.</span></span>  

## <a name="closing-a-fiscal-year"></a><span data-ttu-id="d92a6-134">Afslutning af regnskabsår</span><span class="sxs-lookup"><span data-stu-id="d92a6-134">Closing a Fiscal Year</span></span>

<span data-ttu-id="d92a6-135">Lukning af regnskabsåret er en af opgaverne, når regnskaberne skal afsluttes.</span><span class="sxs-lookup"><span data-stu-id="d92a6-135">Closing the fiscal year is one of the tasks for closing the books.</span></span> <span data-ttu-id="d92a6-136">Når regnskabsåret er afsluttet, er felterne **Afsluttet** og **Dato låst** markeret for alle perioder i året.</span><span class="sxs-lookup"><span data-stu-id="d92a6-136">After you close a fiscal year, the **Closed** and **Date Locked** check boxes are selected for all periods in the year.</span></span> <span data-ttu-id="d92a6-137">Du kan ikke genåbne et år eller fjerne markeringen i felterne.</span><span class="sxs-lookup"><span data-stu-id="d92a6-137">You cannot reopen a year or clear the check boxes.</span></span>

> [!NOTE]  
> <span data-ttu-id="d92a6-138">Du skal altid være mindst ét åbent regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="d92a6-138">You must always have at least one open fiscal year.</span></span> <span data-ttu-id="d92a6-139">Når du lukker et år, skal du sikre dig, der er oprettet et nyt år.</span><span class="sxs-lookup"><span data-stu-id="d92a6-139">When closing a year, ensure that a new year has been created.</span></span> <span data-ttu-id="d92a6-140">Bemærk også, at når du har afsluttet ét regnskabsår, er det ikke muligt at ændre startdatoen for det efterfølgende år.</span><span class="sxs-lookup"><span data-stu-id="d92a6-140">Also, note that after you close one year, you cannot change the starting date of the following year.</span></span>

1. <span data-ttu-id="d92a6-141">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Regnskabsperioder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d92a6-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Accounting Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d92a6-142">Vælg handlingen **Afslut år**.</span><span class="sxs-lookup"><span data-stu-id="d92a6-142">Choose the **Close Year** action.</span></span>  

## <a name="posting-entries-to-a-closed-fiscal-year"></a><span data-ttu-id="d92a6-143">Bogføre poster til et afsluttet regnskabsår</span><span class="sxs-lookup"><span data-stu-id="d92a6-143">Posting Entries to a Closed Fiscal Year</span></span>

<span data-ttu-id="d92a6-144">Selvom et regnskabsår er afsluttet, kan du stadig bogføre finansposter i det.</span><span class="sxs-lookup"><span data-stu-id="d92a6-144">Although a fiscal year is closed, you can still post general ledger entries to it.</span></span> <span data-ttu-id="d92a6-145">Hvis du gør det, bliver posterne i forbindelse med bogføringen markeret som bogførte i et afsluttet regnskabsår, og afkrydsningsfeltet **Efterpost** bliver markeret.</span><span class="sxs-lookup"><span data-stu-id="d92a6-145">When you do, the entries are marked as posted to a closed fiscal year and the **Prior Year Entry** check box is selected.</span></span> <span data-ttu-id="d92a6-146">Afkrydsningsfeltet vises ikke på siden som standard, men du kan tilføje det.</span><span class="sxs-lookup"><span data-stu-id="d92a6-146">By default, the check box is not displayed on the page, but you can add it.</span></span> <span data-ttu-id="d92a6-147">Som det næste skal du afslutte resultatopgørelsens konti og overføre årets resultater til en konto i balancen.</span><span class="sxs-lookup"><span data-stu-id="d92a6-147">The next steps are to close the income statement accounts and transfer the year's results to an account in the balance sheet.</span></span> <span data-ttu-id="d92a6-148">Gentag disse trin, hver gang du bogfører poster i et afsluttet regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="d92a6-148">Repeat these steps each time you post entries to a closed fiscal year.</span></span>

## <a name="see-also"></a><span data-ttu-id="d92a6-149">Se også</span><span class="sxs-lookup"><span data-stu-id="d92a6-149">See Also</span></span>

[<span data-ttu-id="d92a6-150">Afslutte regnskaberne</span><span class="sxs-lookup"><span data-stu-id="d92a6-150">Closing the Books</span></span>](year-close-books.md)  
[<span data-ttu-id="d92a6-151">Afslutning af år og perioder</span><span class="sxs-lookup"><span data-stu-id="d92a6-151">Closing Years and Periods</span></span>](year-close-years-periods.md)  
[<span data-ttu-id="d92a6-152">Sådan arbejder du med kontoskemaer</span><span class="sxs-lookup"><span data-stu-id="d92a6-152">How to Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]