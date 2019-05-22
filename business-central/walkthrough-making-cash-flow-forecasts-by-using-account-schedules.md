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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c09eedbb812df909a43e514dc462dcf8c1cf182a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1249303"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="8356b-106">Gennemgang: Udarbejd likviditetsforecast ved hjælp af kontoskemaer</span><span class="sxs-lookup"><span data-stu-id="8356b-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="8356b-107">Denne gennemgang beskriver, hvordan du kan bruge kontoskemaer til at foretage likviditetsforecasts.</span><span class="sxs-lookup"><span data-stu-id="8356b-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="8356b-108">Kontoskemaer udfører beregninger, der ikke kan foretages direkte i diagrammet for kassekonti.</span><span class="sxs-lookup"><span data-stu-id="8356b-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="8356b-109">I kontoskemaerne kan du oprette subtotaler for likviditetsindbetalinger og -udbetalinger.</span><span class="sxs-lookup"><span data-stu-id="8356b-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="8356b-110">Disse subtotaler kan medtages i nye totaler, der kan bruges i forbindelse med udarbejdelse af likviditetsforecasts.</span><span class="sxs-lookup"><span data-stu-id="8356b-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="8356b-111">Om denne gennemgang</span><span class="sxs-lookup"><span data-stu-id="8356b-111">About This Walkthrough</span></span>  
<span data-ttu-id="8356b-112">Denne gennemgang beskriver følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="8356b-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="8356b-113">Opsætning af et nyt kassekontoskemanavn.</span><span class="sxs-lookup"><span data-stu-id="8356b-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="8356b-114">Opsætning af kontoskemalinjer.</span><span class="sxs-lookup"><span data-stu-id="8356b-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="8356b-115">Opsætning af et nyt kolonneformat.</span><span class="sxs-lookup"><span data-stu-id="8356b-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="8356b-116">Tildeling et kolonneformat til et kontoskema.</span><span class="sxs-lookup"><span data-stu-id="8356b-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="8356b-117">Visning og udskrift af likviditetsforecastet.</span><span class="sxs-lookup"><span data-stu-id="8356b-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="8356b-118">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="8356b-118">Prerequisites</span></span>  
<span data-ttu-id="8356b-119">For at gennemføre denne gennemgang skal:</span><span class="sxs-lookup"><span data-stu-id="8356b-119">To complete this walkthrough, you will need:</span></span>  

- [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="8356b-120">være installeret</span><span class="sxs-lookup"><span data-stu-id="8356b-120">installed.</span></span>  
- <span data-ttu-id="8356b-121">Likviditetskladdelinjerne registreres.</span><span class="sxs-lookup"><span data-stu-id="8356b-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="8356b-122">Roller</span><span class="sxs-lookup"><span data-stu-id="8356b-122">Roles</span></span>  
<span data-ttu-id="8356b-123">Denne gennemgang viser de opgaver, der udføres af følgende brugerrolle:</span><span class="sxs-lookup"><span data-stu-id="8356b-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="8356b-124">Controller</span><span class="sxs-lookup"><span data-stu-id="8356b-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="8356b-125">Historie</span><span class="sxs-lookup"><span data-stu-id="8356b-125">Story</span></span>  
<span data-ttu-id="8356b-126">Ken er controller hos CRONUS, der udarbejder månedlige likviditetsforecasts.</span><span class="sxs-lookup"><span data-stu-id="8356b-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="8356b-127">Han medtager økonomi, salg, køb og anlæg i budgettet, og derefter præsenterer han det for Økonomichefen Sara med henblik på brancheindsigt.</span><span class="sxs-lookup"><span data-stu-id="8356b-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="8356b-128">Opsætning af et nyt kontoskemanavn.</span><span class="sxs-lookup"><span data-stu-id="8356b-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="8356b-129">Et kontoskema består af et kassekontoskemanavn med en række linjer og et kolonneformat.</span><span class="sxs-lookup"><span data-stu-id="8356b-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="8356b-130">Sådan opsættes et nyt kontoskemanavn</span><span class="sxs-lookup"><span data-stu-id="8356b-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="8356b-131">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontoskemaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="8356b-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="8356b-132">På siden **Kontoskemanavne** i skal du vælge handlingen **Ny** for at oprette et nyt kassekontoskemanavn.</span><span class="sxs-lookup"><span data-stu-id="8356b-132">On the **Account Schedule Names** page, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="8356b-133">I feltet **Navn** skal du skrive **Forecast**.</span><span class="sxs-lookup"><span data-stu-id="8356b-133">In the **Name** field, enter **Forecast**.</span></span>  
4.  <span data-ttu-id="8356b-134">I feltet **Beskrivelse** skal du angive **Pengestrømsprognose**.</span><span class="sxs-lookup"><span data-stu-id="8356b-134">In the **Description** field, enter **Cash Flow Forecast**.</span></span>  
5.  <span data-ttu-id="8356b-135">Lad felterne **Standard kolonneformat** og **Analysenavn** være tomme.</span><span class="sxs-lookup"><span data-stu-id="8356b-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="8356b-136">Opsætning af kontoskemalinjer</span><span class="sxs-lookup"><span data-stu-id="8356b-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="8356b-137">Efter opsætning af et kontoskemanavn, definerer Ken hver linje, der vises i kassekontoskemaet.</span><span class="sxs-lookup"><span data-stu-id="8356b-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="8356b-138">Ken definerer linjer, der kan vises i rapporter, foruden de linjer, der kun er til beregning.</span><span class="sxs-lookup"><span data-stu-id="8356b-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="8356b-139">Opsætning af kontoskemalinjer</span><span class="sxs-lookup"><span data-stu-id="8356b-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="8356b-140">På siden **Kontoskemanavne** skal du vælge det nye **forecast**-kontoskemanavn, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="8356b-140">On the **Account Schedule Names** page, select the new **Forecast** account schedule name that you have created.</span></span> <span data-ttu-id="8356b-141">Under fanen **Startside** i gruppen **Proces** skal du vælge **Rediger kontoskema**.</span><span class="sxs-lookup"><span data-stu-id="8356b-141">On the **Home** tab, in the **Process** group, choose **Edit Account Schedule**.</span></span>  
2.  <span data-ttu-id="8356b-142">På siden **Kontoskema** skal du angive hver linje nøjagtigt som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="8356b-142">On the **Account Schedule** page, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="8356b-143">Ved hjælp af funktionen **Indsæt CF-konti** kan du hurtigt markere pengestrømskonti fra diagrammet for pengestrømkonti og kopiere dem til linjer i kontoskemaet.</span><span class="sxs-lookup"><span data-stu-id="8356b-143">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    <span data-ttu-id="8356b-144">|Rækkenr.|Beskrivelsen|Sammentællingstype|Sammentælling|Rækketypen|Beløbstype|Vis|</span><span class="sxs-lookup"><span data-stu-id="8356b-144">|Row No.|Description|Totaling Type|Totaling|Row Type|Amount Type|Show|</span></span>  
    <span data-ttu-id="8356b-145">|-------|-----------|-------------|--------|--------|---  ------|----| |C10|Beløb|Bevægelse|Poster|Nettobeløb|Altid|</span><span class="sxs-lookup"><span data-stu-id="8356b-145">|-------|-----------|-------------|--------|--------|---  ------|----| |C10|Amount|Net Change|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="8356b-146">|C20|Beløb til dato|Saldo til dato|Poster|Nettobeløb|Altid|</span><span class="sxs-lookup"><span data-stu-id="8356b-146">|C20|Amount until Date|Balance at Date|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="8356b-147">|C30|Helt regnskabsår|Helt regnskabsår|Poster|Nettobeløb|Altid|</span><span class="sxs-lookup"><span data-stu-id="8356b-147">|C30|Entire Fiscal Year|Entire Fiscal Year|Entries|Net Amount|Always|</span></span>  

4.  <span data-ttu-id="8356b-148">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="8356b-148">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="8356b-149">Tildele kolonneformatet til navnet på kontoskemaet</span><span class="sxs-lookup"><span data-stu-id="8356b-149">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="8356b-150">Ken er nu klar til at tildele kolonneformatet til kontoskemanavnet.</span><span class="sxs-lookup"><span data-stu-id="8356b-150">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="8356b-151">Sådan tildeles kolonneformatet til navnet på kontoskemaet</span><span class="sxs-lookup"><span data-stu-id="8356b-151">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="8356b-152">På siden **Kontoskemanavne** skal du vælge **Forecast** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="8356b-152">On the **Account Schedule Names** page, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="8356b-153">I feltet **Standard kolonneformat** skal du vælge kolonneformatet **Pengestrøm** for at angive det som standardkolonneformat.</span><span class="sxs-lookup"><span data-stu-id="8356b-153">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="8356b-154">Visning og udskrift af likviditetsforecastet</span><span class="sxs-lookup"><span data-stu-id="8356b-154">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="8356b-155">På siden **Kontoskemanavne** skal du vælge handlingen **Oversigt** for at få vist pengestrømsprognosen.</span><span class="sxs-lookup"><span data-stu-id="8356b-155">On the **Account Schedule Names** page, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="8356b-156">På siden **Kontoskemaoversigt** kan du vælge et beløb og derefter få vist pengestrømsprognoseposterne, der udgør beløbet.</span><span class="sxs-lookup"><span data-stu-id="8356b-156">On the **Acc. Schedule Overview** page, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="8356b-157">Derudover kan du få vist den formel, der bruges til at beregne beløbet.</span><span class="sxs-lookup"><span data-stu-id="8356b-157">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="8356b-158">Du kan også filtrere beløbene efter dato og dimension.</span><span class="sxs-lookup"><span data-stu-id="8356b-158">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="8356b-159">Vælg handlingen **Udskriv** for at udskrive pengestrømsprognosen.</span><span class="sxs-lookup"><span data-stu-id="8356b-159">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8356b-160">Se også</span><span class="sxs-lookup"><span data-stu-id="8356b-160">See Also</span></span>  
 <span data-ttu-id="8356b-161">[Arbejde med kontoskemaer](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="8356b-161">[Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="8356b-162">Gennemgang af forretningsprocesser</span><span class="sxs-lookup"><span data-stu-id="8356b-162">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="8356b-163">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8356b-163">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
