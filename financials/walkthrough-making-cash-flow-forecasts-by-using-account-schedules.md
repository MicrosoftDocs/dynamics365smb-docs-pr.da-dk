---
title: "Gennemgang - Udarbejd likviditetsforecast ved hjælp af kontoskemaer | Microsoft Docs"
description: "Denne gennemgang beskriver, hvordan du kan bruge kontoskemaer til at foretage likviditetsforecasts. Kontoskemaer udfører beregninger, der ikke kan foretages direkte i diagrammet for kassekonti. I kontoskemaerne kan du oprette subtotaler for likviditetsindbetalinger og -udbetalinger. Disse subtotaler kan medtages i nye totaler, der kan bruges i forbindelse med udarbejdelse af likviditetsforecasts."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 25319bae1d601d6beddca35cf8edc032ac11eda6
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="52395-106">Gennemgang: Udarbejd likviditetsforecast ved hjælp af kontoskemaer</span><span class="sxs-lookup"><span data-stu-id="52395-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="52395-107">Denne gennemgang beskriver, hvordan du kan bruge kontoskemaer til at foretage likviditetsforecasts.</span><span class="sxs-lookup"><span data-stu-id="52395-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="52395-108">Kontoskemaer udfører beregninger, der ikke kan foretages direkte i diagrammet for kassekonti.</span><span class="sxs-lookup"><span data-stu-id="52395-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="52395-109">I kontoskemaerne kan du oprette subtotaler for likviditetsindbetalinger og -udbetalinger.</span><span class="sxs-lookup"><span data-stu-id="52395-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="52395-110">Disse subtotaler kan medtages i nye totaler, der kan bruges i forbindelse med udarbejdelse af likviditetsforecasts.</span><span class="sxs-lookup"><span data-stu-id="52395-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="52395-111">Om denne gennemgang</span><span class="sxs-lookup"><span data-stu-id="52395-111">About This Walkthrough</span></span>  
<span data-ttu-id="52395-112">Denne gennemgang beskriver følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="52395-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="52395-113">Opsætning af et nyt kassekontoskemanavn.</span><span class="sxs-lookup"><span data-stu-id="52395-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="52395-114">Opsætning af kontoskemalinjer.</span><span class="sxs-lookup"><span data-stu-id="52395-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="52395-115">Opsætning af et nyt kolonneformat.</span><span class="sxs-lookup"><span data-stu-id="52395-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="52395-116">Tildeling et kolonneformat til et kontoskema.</span><span class="sxs-lookup"><span data-stu-id="52395-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="52395-117">Visning og udskrift af likviditetsforecastet.</span><span class="sxs-lookup"><span data-stu-id="52395-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="52395-118">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="52395-118">Prerequisites</span></span>  
<span data-ttu-id="52395-119">For at gennemføre denne gennemgang skal:</span><span class="sxs-lookup"><span data-stu-id="52395-119">To complete this walkthrough, you will need:</span></span>  

- [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="52395-120"> være installeret</span><span class="sxs-lookup"><span data-stu-id="52395-120"> installed.</span></span>  
- <span data-ttu-id="52395-121">Likviditetskladdelinjerne registreres.</span><span class="sxs-lookup"><span data-stu-id="52395-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="52395-122">Roller</span><span class="sxs-lookup"><span data-stu-id="52395-122">Roles</span></span>  
<span data-ttu-id="52395-123">Denne gennemgang viser de opgaver, der udføres af følgende brugerrolle:</span><span class="sxs-lookup"><span data-stu-id="52395-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="52395-124">Controller</span><span class="sxs-lookup"><span data-stu-id="52395-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="52395-125">Historie</span><span class="sxs-lookup"><span data-stu-id="52395-125">Story</span></span>  
<span data-ttu-id="52395-126">Ken er controller hos CRONUS, der udarbejder månedlige likviditetsforecasts.</span><span class="sxs-lookup"><span data-stu-id="52395-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="52395-127">Han medtager økonomi, salg, køb og anlæg i budgettet, og derefter præsenterer han det for Økonomichefen Sara med henblik på brancheindsigt.</span><span class="sxs-lookup"><span data-stu-id="52395-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="52395-128">Opsætning af et nyt kontoskemanavn.</span><span class="sxs-lookup"><span data-stu-id="52395-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="52395-129">Et kontoskema består af et kassekontoskemanavn med en række linjer og et kolonneformat.</span><span class="sxs-lookup"><span data-stu-id="52395-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="52395-130">Sådan opsættes et nyt kontoskemanavn</span><span class="sxs-lookup"><span data-stu-id="52395-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="52395-131">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoskemaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="52395-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="52395-132">I vinduet **Kontoskemanavne** i skal du vælge handlingen **Ny** for at oprette et nyt kassekontoskemanavn.</span><span class="sxs-lookup"><span data-stu-id="52395-132">In the **Account Schedule Names** window, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="52395-133">I feltet **Navn** skal du skrive **Forecast**.</span><span class="sxs-lookup"><span data-stu-id="52395-133">In the **Name** field, enter **Forecast**.</span></span>  
4.  <span data-ttu-id="52395-134">I feltet **Beskrivelse** skal du angive **Pengestrømsprognose**.</span><span class="sxs-lookup"><span data-stu-id="52395-134">In the **Description** field, enter **Cash Flow Forecast**.</span></span>  
5.  <span data-ttu-id="52395-135">Lad felterne **Standard kolonneformat** og **Analysenavn** være tomme.</span><span class="sxs-lookup"><span data-stu-id="52395-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="52395-136">Opsætning af kontoskemalinjer</span><span class="sxs-lookup"><span data-stu-id="52395-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="52395-137">Efter opsætning af et kontoskemanavn, definerer Ken hver linje, der vises i kassekontoskemaet.</span><span class="sxs-lookup"><span data-stu-id="52395-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="52395-138">Ken definerer linjer, der kan vises i rapporter, foruden de linjer, der kun er til beregning.</span><span class="sxs-lookup"><span data-stu-id="52395-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="52395-139">Opsætning af kontoskemalinjer</span><span class="sxs-lookup"><span data-stu-id="52395-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="52395-140">I vinduet **Kontoskemanavne** skal du vælge det nye **forecast**-kontoskemanavn, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="52395-140">In the **Account Schedule Names** window, select the new **Forecast** account schedule name that you have created.</span></span> <span data-ttu-id="52395-141">Under fanen **Startside** i gruppen **Proces** skal du vælge **Rediger kontoskema**.</span><span class="sxs-lookup"><span data-stu-id="52395-141">On the **Home** tab, in the **Process** group, choose **Edit Account Schedule**.</span></span>  
2.  <span data-ttu-id="52395-142">I vinduet **Kontoskema** skal du angive hver linje nøjagtigt som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="52395-142">In the **Account Schedule** window, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="52395-143">Ved hjælp af funktionen **Indsæt CF-konti** kan du hurtigt markere pengestrømskonti fra diagrammet for pengestrømkonti og kopiere dem til linjer i kontoskemaet.</span><span class="sxs-lookup"><span data-stu-id="52395-143">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    <span data-ttu-id="52395-144">|Rækkenr.|Beskrivelsen|Sammentællingstype|Sammentælling|Rækketypen|Beløbstype|Vis|</span><span class="sxs-lookup"><span data-stu-id="52395-144">|Row No.|Description|Totaling Type|Totaling|Row Type|Amount Type|Show|</span></span>  
    <span data-ttu-id="52395-145">|-------|-----------|-------------|--------|--------|---  ------|----| |C10|Beløb|Bevægelse|Poster|Nettobeløb|Altid|</span><span class="sxs-lookup"><span data-stu-id="52395-145">|-------|-----------|-------------|--------|--------|---  ------|----| |C10|Amount|Net Change|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="52395-146">|C20|Beløb til dato|Saldo til dato|Poster|Nettobeløb|Altid|</span><span class="sxs-lookup"><span data-stu-id="52395-146">|C20|Amount until Date|Balance at Date|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="52395-147">|C30|Helt regnskabsår|Helt regnskabsår|Poster|Nettobeløb|Altid|</span><span class="sxs-lookup"><span data-stu-id="52395-147">|C30|Entire Fiscal Year|Entire Fiscal Year|Entries|Net Amount|Always|</span></span>  

4.  <span data-ttu-id="52395-148">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="52395-148">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="52395-149">Tildele kolonneformatet til navnet på kontoskemaet</span><span class="sxs-lookup"><span data-stu-id="52395-149">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="52395-150">Ken er nu klar til at tildele kolonneformatet til kontoskemanavnet.</span><span class="sxs-lookup"><span data-stu-id="52395-150">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="52395-151">Sådan tildeles kolonneformatet til navnet på kontoskemaet</span><span class="sxs-lookup"><span data-stu-id="52395-151">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="52395-152">I vinduet **Kontoskemanavne** skal du vælge **Forecast** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="52395-152">In the **Account Schedule Names** window, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="52395-153">I feltet **Standard kolonneformat** skal du vælge kolonneformatet **Pengestrøm** for at angive det som standardkolonneformat.</span><span class="sxs-lookup"><span data-stu-id="52395-153">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="52395-154">Visning og udskrift af likviditetsforecastet</span><span class="sxs-lookup"><span data-stu-id="52395-154">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="52395-155">I vinduet **Kontoskemanavne** skal du vælge handlingen **Oversigt** for at få vist pengestrømsprognosen.</span><span class="sxs-lookup"><span data-stu-id="52395-155">In the **Account Schedule Names** window, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="52395-156">I vinduet **Kontoskemaoversigt** kan du vælge et beløb og derefter få vist pengestrømsprognoseposterne, der udgør beløbet.</span><span class="sxs-lookup"><span data-stu-id="52395-156">In the **Acc. Schedule Overview** window, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="52395-157">Derudover kan du få vist den formel, der bruges til at beregne beløbet.</span><span class="sxs-lookup"><span data-stu-id="52395-157">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="52395-158">Du kan også filtrere beløbene efter dato og dimension.</span><span class="sxs-lookup"><span data-stu-id="52395-158">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="52395-159">Vælg handlingen **Udskriv** for at udskrive pengestrømsprognosen.</span><span class="sxs-lookup"><span data-stu-id="52395-159">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="52395-160">Se også</span><span class="sxs-lookup"><span data-stu-id="52395-160">See Also</span></span>  
 <span data-ttu-id="52395-161">[Arbejde med kontoskemaer](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="52395-161">[Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="52395-162">Gennemgang af forretningsprocesser</span><span class="sxs-lookup"><span data-stu-id="52395-162">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="52395-163">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="52395-163">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

