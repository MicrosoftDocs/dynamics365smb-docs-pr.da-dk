---
title: Gennemgang - Udarbejd likviditetsforecast ved hjælp af kontoskemaer | Microsoft Docs
description: Denne gennemgang beskriver, hvordan du kan bruge kontoskemaer til at foretage likviditetsforecasts. Kontoskemaer udfører beregninger, der ikke kan foretages direkte i diagrammet for kassekonti. I kontoskemaerne kan du oprette subtotaler for likviditetsindbetalinger og -udbetalinger. Disse subtotaler kan medtages i nye totaler, der kan bruges i forbindelse med udarbejdelse af likviditetsforecasts.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 70f1e51a0cd2c1b6c90ca3d76013fb3a5f30f80e
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2314840"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="8886c-106">Gennemgang: Udarbejd likviditetsforecast ved hjælp af kontoskemaer</span><span class="sxs-lookup"><span data-stu-id="8886c-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="8886c-107">Denne gennemgang beskriver, hvordan du kan bruge kontoskemaer til at foretage likviditetsforecasts.</span><span class="sxs-lookup"><span data-stu-id="8886c-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="8886c-108">Kontoskemaer udfører beregninger, der ikke kan foretages direkte i diagrammet for kassekonti.</span><span class="sxs-lookup"><span data-stu-id="8886c-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="8886c-109">I kontoskemaerne kan du oprette subtotaler for likviditetsindbetalinger og -udbetalinger.</span><span class="sxs-lookup"><span data-stu-id="8886c-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="8886c-110">Disse subtotaler kan medtages i nye totaler, der kan bruges i forbindelse med udarbejdelse af likviditetsforecasts.</span><span class="sxs-lookup"><span data-stu-id="8886c-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="8886c-111">Om denne gennemgang</span><span class="sxs-lookup"><span data-stu-id="8886c-111">About This Walkthrough</span></span>  
<span data-ttu-id="8886c-112">Denne gennemgang beskriver følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="8886c-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="8886c-113">Opsætning af et nyt kassekontoskemanavn.</span><span class="sxs-lookup"><span data-stu-id="8886c-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="8886c-114">Opsætning af kontoskemalinjer.</span><span class="sxs-lookup"><span data-stu-id="8886c-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="8886c-115">Opsætning af et nyt kolonneformat.</span><span class="sxs-lookup"><span data-stu-id="8886c-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="8886c-116">Tildeling et kolonneformat til et kontoskema.</span><span class="sxs-lookup"><span data-stu-id="8886c-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="8886c-117">Visning og udskrift af likviditetsforecastet.</span><span class="sxs-lookup"><span data-stu-id="8886c-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="8886c-118">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="8886c-118">Prerequisites</span></span>  
<span data-ttu-id="8886c-119">For at gennemføre denne gennemgang skal:</span><span class="sxs-lookup"><span data-stu-id="8886c-119">To complete this walkthrough, you will need:</span></span>  

- [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="8886c-120">være installeret</span><span class="sxs-lookup"><span data-stu-id="8886c-120">installed.</span></span>  
- <span data-ttu-id="8886c-121">Likviditetskladdelinjerne registreres.</span><span class="sxs-lookup"><span data-stu-id="8886c-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="8886c-122">Roller</span><span class="sxs-lookup"><span data-stu-id="8886c-122">Roles</span></span>  
<span data-ttu-id="8886c-123">Denne gennemgang viser de opgaver, der udføres af følgende brugerrolle:</span><span class="sxs-lookup"><span data-stu-id="8886c-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="8886c-124">Controller</span><span class="sxs-lookup"><span data-stu-id="8886c-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="8886c-125">Historie</span><span class="sxs-lookup"><span data-stu-id="8886c-125">Story</span></span>  
<span data-ttu-id="8886c-126">Ken er controller hos CRONUS, der udarbejder månedlige likviditetsforecasts.</span><span class="sxs-lookup"><span data-stu-id="8886c-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="8886c-127">Han medtager økonomi, salg, køb og anlæg i budgettet, og derefter præsenterer han det for Økonomichefen Sara med henblik på brancheindsigt.</span><span class="sxs-lookup"><span data-stu-id="8886c-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="8886c-128">Opsætning af et nyt kontoskemanavn.</span><span class="sxs-lookup"><span data-stu-id="8886c-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="8886c-129">Et kontoskema består af et kassekontoskemanavn med en række linjer og et kolonneformat.</span><span class="sxs-lookup"><span data-stu-id="8886c-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="8886c-130">Sådan opsættes et nyt kontoskemanavn</span><span class="sxs-lookup"><span data-stu-id="8886c-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="8886c-131">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontoskemaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="8886c-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="8886c-132">På siden **Kontoskemanavne** i skal du vælge handlingen **Ny** for at oprette et nyt kassekontoskemanavn.</span><span class="sxs-lookup"><span data-stu-id="8886c-132">On the **Account Schedule Names** page, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="8886c-133">I feltet **Navn** skal du skrive **Forecast**.</span><span class="sxs-lookup"><span data-stu-id="8886c-133">In the **Name** field, enter **Forecast**.</span></span>  
4.  <span data-ttu-id="8886c-134">I feltet **Beskrivelse** skal du angive **Pengestrømsprognose**.</span><span class="sxs-lookup"><span data-stu-id="8886c-134">In the **Description** field, enter **Cash Flow Forecast**.</span></span>  
5.  <span data-ttu-id="8886c-135">Lad felterne **Standard kolonneformat** og **Analysenavn** være tomme.</span><span class="sxs-lookup"><span data-stu-id="8886c-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="8886c-136">Opsætning af kontoskemalinjer</span><span class="sxs-lookup"><span data-stu-id="8886c-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="8886c-137">Efter opsætning af et kontoskemanavn, definerer Ken hver linje, der vises i kassekontoskemaet.</span><span class="sxs-lookup"><span data-stu-id="8886c-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="8886c-138">Ken definerer linjer, der kan vises i rapporter, foruden de linjer, der kun er til beregning.</span><span class="sxs-lookup"><span data-stu-id="8886c-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="8886c-139">Opsætning af kontoskemalinjer</span><span class="sxs-lookup"><span data-stu-id="8886c-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="8886c-140">På siden **Kontoskemanavne** skal du vælge det nye **forecast**-kontoskemanavn, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="8886c-140">On the **Account Schedule Names** page, select the new **Forecast** account schedule name that you have created.</span></span> <span data-ttu-id="8886c-141">Under fanen **Startside** i gruppen **Proces** skal du vælge **Rediger kontoskema**.</span><span class="sxs-lookup"><span data-stu-id="8886c-141">On the **Home** tab, in the **Process** group, choose **Edit Account Schedule**.</span></span>  
2.  <span data-ttu-id="8886c-142">På siden **Kontoskema** skal du angive hver linje nøjagtigt som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="8886c-142">On the **Account Schedule** page, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="8886c-143">Ved hjælp af funktionen **Indsæt CF-konti** kan du hurtigt markere pengestrømskonti fra diagrammet for pengestrømkonti og kopiere dem til linjer i kontoskemaet.</span><span class="sxs-lookup"><span data-stu-id="8886c-143">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    |<span data-ttu-id="8886c-144">Rækkenr.</span><span class="sxs-lookup"><span data-stu-id="8886c-144">Row No.</span></span>|<span data-ttu-id="8886c-145">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="8886c-145">Description</span></span>|<span data-ttu-id="8886c-146">Sammentællingstype</span><span class="sxs-lookup"><span data-stu-id="8886c-146">Totaling Type</span></span>|<span data-ttu-id="8886c-147">Sammentælling</span><span class="sxs-lookup"><span data-stu-id="8886c-147">Totaling</span></span>|<span data-ttu-id="8886c-148">Rækketype</span><span class="sxs-lookup"><span data-stu-id="8886c-148">Row Type</span></span>|<span data-ttu-id="8886c-149">Beløbstype</span><span class="sxs-lookup"><span data-stu-id="8886c-149">Amount Type</span></span>|<span data-ttu-id="8886c-150">Vis</span><span class="sxs-lookup"><span data-stu-id="8886c-150">Show</span></span>|  
    |-------|-----------|-------------|--------|--------|-----------|----|
    |<span data-ttu-id="8886c-151">C10</span><span class="sxs-lookup"><span data-stu-id="8886c-151">C10</span></span>|<span data-ttu-id="8886c-152">Beløb</span><span class="sxs-lookup"><span data-stu-id="8886c-152">Amount</span></span>|<span data-ttu-id="8886c-153">Bevægelse</span><span class="sxs-lookup"><span data-stu-id="8886c-153">Net Change</span></span>|<span data-ttu-id="8886c-154">Poster</span><span class="sxs-lookup"><span data-stu-id="8886c-154">Entries</span></span>|<span data-ttu-id="8886c-155">Nettobeløb</span><span class="sxs-lookup"><span data-stu-id="8886c-155">Net Amount</span></span>|<span data-ttu-id="8886c-156">Altid</span><span class="sxs-lookup"><span data-stu-id="8886c-156">Always</span></span>|  
    |<span data-ttu-id="8886c-157">C20</span><span class="sxs-lookup"><span data-stu-id="8886c-157">C20</span></span>|<span data-ttu-id="8886c-158">Beløb til dato</span><span class="sxs-lookup"><span data-stu-id="8886c-158">Amount until Date</span></span>|<span data-ttu-id="8886c-159">Saldo til dato</span><span class="sxs-lookup"><span data-stu-id="8886c-159">Balance at Date</span></span>|<span data-ttu-id="8886c-160">Poster</span><span class="sxs-lookup"><span data-stu-id="8886c-160">Entries</span></span>|<span data-ttu-id="8886c-161">Nettobeløb</span><span class="sxs-lookup"><span data-stu-id="8886c-161">Net Amount</span></span>|<span data-ttu-id="8886c-162">Altid</span><span class="sxs-lookup"><span data-stu-id="8886c-162">Always</span></span>|  
    |<span data-ttu-id="8886c-163">C30</span><span class="sxs-lookup"><span data-stu-id="8886c-163">C30</span></span>|<span data-ttu-id="8886c-164">Hele regnskabsåret</span><span class="sxs-lookup"><span data-stu-id="8886c-164">Entire Fiscal Year</span></span>|<span data-ttu-id="8886c-165">Hele regnskabsåret</span><span class="sxs-lookup"><span data-stu-id="8886c-165">Entire Fiscal Year</span></span>|<span data-ttu-id="8886c-166">Poster</span><span class="sxs-lookup"><span data-stu-id="8886c-166">Entries</span></span>|<span data-ttu-id="8886c-167">Nettobeløb</span><span class="sxs-lookup"><span data-stu-id="8886c-167">Net Amount</span></span>|<span data-ttu-id="8886c-168">Altid</span><span class="sxs-lookup"><span data-stu-id="8886c-168">Always</span></span>|  

4.  <span data-ttu-id="8886c-169">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="8886c-169">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="8886c-170">Tildele kolonneformatet til navnet på kontoskemaet</span><span class="sxs-lookup"><span data-stu-id="8886c-170">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="8886c-171">Ken er nu klar til at tildele kolonneformatet til kontoskemanavnet.</span><span class="sxs-lookup"><span data-stu-id="8886c-171">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="8886c-172">Sådan tildeles kolonneformatet til navnet på kontoskemaet</span><span class="sxs-lookup"><span data-stu-id="8886c-172">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="8886c-173">På siden **Kontoskemanavne** skal du vælge **Forecast** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="8886c-173">On the **Account Schedule Names** page, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="8886c-174">I feltet **Standard kolonneformat** skal du vælge kolonneformatet **Pengestrøm** for at angive det som standardkolonneformat.</span><span class="sxs-lookup"><span data-stu-id="8886c-174">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="8886c-175">Visning og udskrift af likviditetsforecastet</span><span class="sxs-lookup"><span data-stu-id="8886c-175">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="8886c-176">På siden **Kontoskemanavne** skal du vælge handlingen **Oversigt** for at få vist pengestrømsprognosen.</span><span class="sxs-lookup"><span data-stu-id="8886c-176">On the **Account Schedule Names** page, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="8886c-177">På siden **Kontoskemaoversigt** kan du vælge et beløb og derefter få vist pengestrømsprognoseposterne, der udgør beløbet.</span><span class="sxs-lookup"><span data-stu-id="8886c-177">On the **Acc. Schedule Overview** page, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="8886c-178">Derudover kan du få vist den formel, der bruges til at beregne beløbet.</span><span class="sxs-lookup"><span data-stu-id="8886c-178">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="8886c-179">Du kan også filtrere beløbene efter dato og dimension.</span><span class="sxs-lookup"><span data-stu-id="8886c-179">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="8886c-180">Vælg handlingen **Udskriv** for at udskrive pengestrømsprognosen.</span><span class="sxs-lookup"><span data-stu-id="8886c-180">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8886c-181">Se også</span><span class="sxs-lookup"><span data-stu-id="8886c-181">See Also</span></span>  
 <span data-ttu-id="8886c-182">[Arbejde med kontoskemaer](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="8886c-182">[Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="8886c-183">Gennemgang af forretningsprocesser</span><span class="sxs-lookup"><span data-stu-id="8886c-183">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="8886c-184">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8886c-184">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
