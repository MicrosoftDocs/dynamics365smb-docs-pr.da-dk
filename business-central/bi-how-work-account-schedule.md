---
title: "Oprette finansrapporter ved hjælp af kontoskemaer"
description: Beskriver, hvordan du kan bruge kontoskemaer til at oprette forskellige visninger og rapporter til analyse af data for finansiel ydeevne.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/16/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: f9f5b3a25a24d4d10c80d048153e68030733bf9e
ms.contentlocale: da-dk
ms.lasthandoff: 04/18/2018

---
# <a name="work-with-account-schedules"></a><span data-ttu-id="ee343-103">Arbejde med kontoskemaer</span><span class="sxs-lookup"><span data-stu-id="ee343-103">Work with Account Schedules</span></span>
<span data-ttu-id="ee343-104">Du kan bruge kontoskemaer til at få indsigt i de finansielle oplysninger, der er gemt i din kontoplan.</span><span class="sxs-lookup"><span data-stu-id="ee343-104">Use account schedules to get insight into the financial data stored in your chart of accounts.</span></span> <span data-ttu-id="ee343-105">Kontoskemaer analyserer tal i finanskonti og sammenligner finansposter med finansbudgetposter.</span><span class="sxs-lookup"><span data-stu-id="ee343-105">Account schedules analyze figures in G/L accounts, and compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="ee343-106">Resultaterne vises i diagrammer på dit rollecenter, f.eks. pengestrømsdiagrammet.</span><span class="sxs-lookup"><span data-stu-id="ee343-106">The results display in charts on your Role Center, such as the Cash Flow chart.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="ee343-107"> indeholder et par eksempelkontoskemaer, som du kan bruge det samme, eller du kan konfigurere dine egen rækker og kolonner for at angive de tal, du vil sammenligne.</span><span class="sxs-lookup"><span data-stu-id="ee343-107"> provides a few sample account schedules that you can use right away, or you can set up your own rows and columns to specify the figures to compare.</span></span> <span data-ttu-id="ee343-108">Du kan f.eks. oprette kontoskemaer for at beregne avancer på dimensioner som afdelinger eller debitorgrupper.</span><span class="sxs-lookup"><span data-stu-id="ee343-108">For example, you can create account schedules to calculate profit margins on dimensions like departments or customer groups.</span></span> <span data-ttu-id="ee343-109">Du kan oprette så mange tilpassede kontoudtog, som du har behov for.</span><span class="sxs-lookup"><span data-stu-id="ee343-109">You can create as many customized financial statements as you want.</span></span>  

<span data-ttu-id="ee343-110">Oprettelse af kontoskemaer kræver en forståelse af de finansielle data i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="ee343-110">Setting up account schedules requires an understanding of the financial data in the chart of accounts.</span></span> <span data-ttu-id="ee343-111">Du kan f.eks. få vist finansposter som procenter af budgetposterne.</span><span class="sxs-lookup"><span data-stu-id="ee343-111">For example, you can view general ledger entries as percentages of budget entries.</span></span> <span data-ttu-id="ee343-112">Dette kræver, at der er oprettet budgetter.</span><span class="sxs-lookup"><span data-stu-id="ee343-112">This requires that budgets are created.</span></span> <span data-ttu-id="ee343-113">Du kan finde flere oplysninger i [Oprette finansbudgetter](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="ee343-113">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="account-categories-and-account-schedules"></a><span data-ttu-id="ee343-114">Kontokategorier og kontoskemaer</span><span class="sxs-lookup"><span data-stu-id="ee343-114">Account Categories and Account Schedules</span></span>
<span data-ttu-id="ee343-115">Du kan bruge kontokategorier til at ændre layoutet af regnskabet.</span><span class="sxs-lookup"><span data-stu-id="ee343-115">You can use account categories to change the layout of your financial statements.</span></span> <span data-ttu-id="ee343-116">Når du har oprettet kontokategorierne i vinduet **Finanskontokategorier**, og du vælger handlingen **Opret kontoskemaer** opdateres de underliggende kontoskemaer for de grundlæggende regnskabsrapporter.</span><span class="sxs-lookup"><span data-stu-id="ee343-116">After you set up your account categories in the **G/L Account Categories** window, and you choose the **Generate Account Schedules** action, the underlying account schedules for the core financial reports are updated.</span></span> <span data-ttu-id="ee343-117">Næste gang du kører en af disse rapporter, f.eks. saldoopgørelsen, tilføjes nye totaler og underordnede linjer, baseret på dine ændringer.</span><span class="sxs-lookup"><span data-stu-id="ee343-117">The next time you run one of these reports, such as the balance statement, new totals and subentries are added, based on your changes.</span></span> <span data-ttu-id="ee343-118">Du kan finde flere oplysninger i [Finans- og kontoplanen](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="ee343-118">For more information, see [The General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span>  

## <a name="to-create-new-account-schedules"></a><span data-ttu-id="ee343-119">Sådan oprettes nye kontoskemaer</span><span class="sxs-lookup"><span data-stu-id="ee343-119">To create new account schedules</span></span>  
 <span data-ttu-id="ee343-120">Du bruger kontoskemaer til at analysere tal i finanskonti eller til at sammenligne finansposter med finansbudgetposter.</span><span class="sxs-lookup"><span data-stu-id="ee343-120">You use account schedules to analyze figures in general ledger accounts or to compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="ee343-121">Du kan f.eks. få vist finansposter som procenter af budgetposter.</span><span class="sxs-lookup"><span data-stu-id="ee343-121">For example, you can view the general ledger entries as percentages of the budget entries.</span></span>

1. <span data-ttu-id="ee343-122">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoskemaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ee343-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ee343-123">I vinduet **Kontoskemanavne** i skal du vælge handlingen **Ny** for at oprette et nyt kontoskemanavn.</span><span class="sxs-lookup"><span data-stu-id="ee343-123">In the **Account Schedule Names** window, choose the **New** action to create a new account schedule name.</span></span>
3. <span data-ttu-id="ee343-124">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="ee343-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="ee343-125">Vælg handlingen **Rediger kontoskema**.</span><span class="sxs-lookup"><span data-stu-id="ee343-125">Choose the **Edit Account Schedule** action.</span></span>
5. <span data-ttu-id="ee343-126">Udfyld felterne efter behov i vinduet **Kontoskema**.</span><span class="sxs-lookup"><span data-stu-id="ee343-126">In the **Account Schedule** window, fill in the fields as necessary.</span></span>  

    <span data-ttu-id="ee343-127">Når du har oprettet et nyt kontoskema og oprettet rækkerne, skal du angive kolonner.</span><span class="sxs-lookup"><span data-stu-id="ee343-127">When you have created a new account schedule and set up the rows, you must set up columns.</span></span> <span data-ttu-id="ee343-128">Du kan oprette dem manuelt eller tilknytte et foruddefineret kolonneformat til kontoskemaet.</span><span class="sxs-lookup"><span data-stu-id="ee343-128">You can either set them up manually or assign a predefined column layout to your account schedule.</span></span>
6. <span data-ttu-id="ee343-129">Vælg handlingen **Rediger opsætning af kolonneformat**.</span><span class="sxs-lookup"><span data-stu-id="ee343-129">Choose the **Edit Column Layout Setup** action.</span></span>
7. <span data-ttu-id="ee343-130">Udfyld felterne efter behov i vinduet **Kolonnelayout**.</span><span class="sxs-lookup"><span data-stu-id="ee343-130">In the **Column Layout** window, fill in the fields as necessary.</span></span>

> [!NOTE]  
>   <span data-ttu-id="ee343-131">Hvis du ikke har tildelt et standard kolonneformat til kontoskemaet, skal du definere kolonnerne manuelt.</span><span class="sxs-lookup"><span data-stu-id="ee343-131">If you did not assign a default column layout to the account schedule, you must set the columns up manually.</span></span>   

### <a name="to-create-a-column-that-calculates-percentages"></a><span data-ttu-id="ee343-132">Sådan oprettes en kolonne, hvor procenten beregnes</span><span class="sxs-lookup"><span data-stu-id="ee343-132">To create a column that calculates percentages</span></span>  
<span data-ttu-id="ee343-133">Du vil muligvis gerne medtage en kolonne i et kontoskema for at beregne procenter af et totalbeløb.</span><span class="sxs-lookup"><span data-stu-id="ee343-133">Sometimes you may want to include a column in an account schedule to calculate percentages of a total.</span></span> <span data-ttu-id="ee343-134">Hvis du f.eks. har et antal rækker, som specificerer salg efter dimension, kan du have en kolonne, som angiver procenten af det samlede salg, som hver række repræsenterer.</span><span class="sxs-lookup"><span data-stu-id="ee343-134">For example, if you have a number of rows that break down sales by dimension, you may want a column to indicate the percentage of total sales that each row represents.</span></span>

1. <span data-ttu-id="ee343-135">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoskemaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ee343-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="ee343-136">Vælg et kontoskema i vinduet **Kontoskemanavne**.</span><span class="sxs-lookup"><span data-stu-id="ee343-136">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="ee343-137">Vælg handlingen **Rediger kontoskema** for at konfigurere en kontoskemarække til beregning af den total, som procentdelene baseres på.</span><span class="sxs-lookup"><span data-stu-id="ee343-137">Choose the **Edit Account Schedule** action to set up an account schedule row to calculate the total on which the percentages will be based.</span></span>  
4. <span data-ttu-id="ee343-138">Indsæt en linje lige over den første række, som du vil vise en procent for.</span><span class="sxs-lookup"><span data-stu-id="ee343-138">Insert a line immediately above the first row for which you want to display a percentage.</span></span>  
5. <span data-ttu-id="ee343-139">Udfyld felterne på linjen på følgende måde: I feltet **Sammentællingstype** skal du angive **Angiv grundlag for procent**.</span><span class="sxs-lookup"><span data-stu-id="ee343-139">Fill in the fields on the line as follows: In the **Totaling Type** field, enter **Set Base for Percent**.</span></span> <span data-ttu-id="ee343-140">I feltet **Sammentælling** skal du indtaste en formel for den total, som procentdelen skal baseres på.</span><span class="sxs-lookup"><span data-stu-id="ee343-140">In the **Totaling** field, enter a formula for the total that the percentage will be based on.</span></span> <span data-ttu-id="ee343-141">Hvis række 11 f.eks. indeholder det samlede salg, indtastes **11**.</span><span class="sxs-lookup"><span data-stu-id="ee343-141">For example, if row 11 contains the total sales, enter **11**.</span></span>  
6. <span data-ttu-id="ee343-142">Vælg handlingen **Rediger opsætning af kolonneformat** for at oprette en kolonne.</span><span class="sxs-lookup"><span data-stu-id="ee343-142">Choose the **Edit Column Layout Setup** action to set up a column.</span></span>  
7. <span data-ttu-id="ee343-143">Udfyld felterne på linjen på følgende måde: I feltet **Kolonnetype** skal du vælge **Formel**.</span><span class="sxs-lookup"><span data-stu-id="ee343-143">Fill in the fields on the line as follows: In the **Column Type** field, select **Formula**.</span></span> <span data-ttu-id="ee343-144">I feltet **Formel** skal du indtaste en formel for det beløb, som du vil beregne en procentdel for, efterfulgt af %.</span><span class="sxs-lookup"><span data-stu-id="ee343-144">In the **Formula** field, enter a formula for the amount that you want to calculate a percentage for, followed by %.</span></span> <span data-ttu-id="ee343-145">Hvis kolonnenummer N f.eks. indeholder bevægelsen, indtastes **N %**.</span><span class="sxs-lookup"><span data-stu-id="ee343-145">For example, if column number N contains the net change, enter **N%**.</span></span>  
8. <span data-ttu-id="ee343-146">Gentag trin 4 til 7 for alle de grupper af rækker, du vil specificere efter procent.</span><span class="sxs-lookup"><span data-stu-id="ee343-146">Repeat steps 4 through 7 for each group of rows that you want to break down by percentage.</span></span>

## <a name="to-set-up-account-schedules-with-overviews"></a><span data-ttu-id="ee343-147">Sådan oprettes kontoskemaer med oversigter</span><span class="sxs-lookup"><span data-stu-id="ee343-147">To set up account schedules with overviews</span></span>  
<span data-ttu-id="ee343-148">Du kan bruge et kontoskema til at oprette en opgørelse, hvor tallene i finansposter sammenlignes med tallene i finansbudgettet.</span><span class="sxs-lookup"><span data-stu-id="ee343-148">You can use an account schedule to create a statement comparing general ledger figures and general leger budget figures.</span></span>

1. <span data-ttu-id="ee343-149">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoskemaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ee343-149">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="ee343-150">Vælg et kontoskema i vinduet **Kontoskemanavne**.</span><span class="sxs-lookup"><span data-stu-id="ee343-150">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="ee343-151">Vælg handlingen **Rediger kontoskema**</span><span class="sxs-lookup"><span data-stu-id="ee343-151">Choose the **Edit Account Schedule** action</span></span>  
4. <span data-ttu-id="ee343-152">I vinduet **Kontoskema** skal du vælge standardkontoskemanavnet i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="ee343-152">In the **Account Schedule** window, in the **Name** field, select the default account schedule name.</span></span>
5. <span data-ttu-id="ee343-153">Vælg handlingen **Indsæt konti**.</span><span class="sxs-lookup"><span data-stu-id="ee343-153">Choose the **Insert Accounts** action.</span></span>  
6. <span data-ttu-id="ee343-154">Marker de konti, som du ønsker at medtage i opgørelsen, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="ee343-154">Select the accounts that you want to include in your statement, and then choose the **OK** button.</span></span>

    <span data-ttu-id="ee343-155">Kontiene indsættes i kontoskemaet.</span><span class="sxs-lookup"><span data-stu-id="ee343-155">The accounts are now inserted into your account schedule.</span></span> <span data-ttu-id="ee343-156">Hvis du vil, kan du også ændre kolonneformatet.</span><span class="sxs-lookup"><span data-stu-id="ee343-156">If you want you can also change the column layout.</span></span>  
7. <span data-ttu-id="ee343-157">Vælg handlingen **Oversigt**.</span><span class="sxs-lookup"><span data-stu-id="ee343-157">Choose the **Overview** action.</span></span>  
8. <span data-ttu-id="ee343-158">Klik på oversigtspanelet **Dimensionsfiltre**, og sæt budgetfilteret til det ønskede filternavn.</span><span class="sxs-lookup"><span data-stu-id="ee343-158">On the **Dimension Filters** FastTab, set the budget filter to the desired filter name.</span></span>  
9. <span data-ttu-id="ee343-159">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="ee343-159">Choose the **OK** button.</span></span>  

<span data-ttu-id="ee343-160">Du kan nu kopiere og indsætte budgetoversigten i et regneark..</span><span class="sxs-lookup"><span data-stu-id="ee343-160">Now you can copy and paste your budget statement into a spreadsheet.</span></span>  

## <a name="comparing-accounting-periods-using-period-formulas"></a><span data-ttu-id="ee343-161">Sammenligne regnskabsperioder ved hjælp af periodeformler</span><span class="sxs-lookup"><span data-stu-id="ee343-161">Comparing Accounting Periods using Period Formulas</span></span>
<span data-ttu-id="ee343-162">Kontoskemaet kan sammenligne resultaterne af forskellige regnskabsperioder, f.eks. denne måned sammenlignet med samme måned sidste år.</span><span class="sxs-lookup"><span data-stu-id="ee343-162">Your account schedule can compare the results of different accounting periods, such as this month versus same month last year.</span></span> <span data-ttu-id="ee343-163">For at gøre det skal du tilføje en kolonne i feltet **Sammenligningsperiodeformel** og derefter indstille dette felt til en periodeformel.</span><span class="sxs-lookup"><span data-stu-id="ee343-163">To do that, you add a column with the **Comparison Period Formula** field, and then set that field to a period formula.</span></span>  

<span data-ttu-id="ee343-164">En regnskabsperiode skal ikke følge kalenderåret, men hvert regnskabsår skal have det samme antal regnskabsperioder, selvom hver periode kan variere i længde.</span><span class="sxs-lookup"><span data-stu-id="ee343-164">An accounting period does not have to match the calendar, but each fiscal year must have the same number of accounting periods, even though each period can be different in length.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="ee343-165"> bruger periodeformlen til at beregne beløbet fra sammenligningsperioden i relation til den periode, som er defineret af datofiltret i rapportanmodningen.</span><span class="sxs-lookup"><span data-stu-id="ee343-165"> uses the period formula to calculate the amount from the comparison period in relation to the period represented by the date filter on the report request.</span></span> <span data-ttu-id="ee343-166">Sammenligningsperioden er baseret på perioden fra startdatoen i datofilteret.</span><span class="sxs-lookup"><span data-stu-id="ee343-166">The comparison period is based on the period of the start date of the date filter.</span></span> <span data-ttu-id="ee343-167">Periodeangivelserne forkortes på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="ee343-167">The abbreviations for period specifications are:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee343-168">Forkortelse</span><span class="sxs-lookup"><span data-stu-id="ee343-168">Abbreviation</span></span></th>
<th><span data-ttu-id="ee343-169">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ee343-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee343-170">P</span><span class="sxs-lookup"><span data-stu-id="ee343-170">P</span></span></p></td>
<td><p><span data-ttu-id="ee343-171">Periode</span><span class="sxs-lookup"><span data-stu-id="ee343-171">Period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee343-172">FP</span><span class="sxs-lookup"><span data-stu-id="ee343-172">LP</span></span></p></td>
<td><p><span data-ttu-id="ee343-173">Forrige periode i et regnskabsår, halvår eller kvartal.</span><span class="sxs-lookup"><span data-stu-id="ee343-173">Last period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee343-174">NP</span><span class="sxs-lookup"><span data-stu-id="ee343-174">CP</span></span></p></td>
<td><p><span data-ttu-id="ee343-175">Nuværende periode i et regnskabsår, halvår eller kvartal.</span><span class="sxs-lookup"><span data-stu-id="ee343-175">Current period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee343-176">RÅ</span><span class="sxs-lookup"><span data-stu-id="ee343-176">FY</span></span></p></td>
<td><p><span data-ttu-id="ee343-177">Regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="ee343-177">Fiscal year.</span></span> <span data-ttu-id="ee343-178">RÅ[1..3] betegner f.eks. det første kvartal i det indeværende regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="ee343-178">For example, FY[1..3] denotes first quarter of the current fiscal year</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ee343-179">Eksempler på formler:</span><span class="sxs-lookup"><span data-stu-id="ee343-179">Examples of formulas:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee343-180">Formel</span><span class="sxs-lookup"><span data-stu-id="ee343-180">Formula</span></span></th>
<th><span data-ttu-id="ee343-181">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ee343-181">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee343-182">&lt;Tomt&gt;</span><span class="sxs-lookup"><span data-stu-id="ee343-182">&lt;Blank&gt;</span></span></p></td>
<td><p><span data-ttu-id="ee343-183">Nuværende periode</span><span class="sxs-lookup"><span data-stu-id="ee343-183">Current period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee343-184">-1P</span><span class="sxs-lookup"><span data-stu-id="ee343-184">-1P</span></span></p></td>
<td><p><span data-ttu-id="ee343-185">Forrige periode</span><span class="sxs-lookup"><span data-stu-id="ee343-185">Previous period</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee343-186">-1RÅ[1..FP]</span><span class="sxs-lookup"><span data-stu-id="ee343-186">-1FY[1..LP]</span></span></p></td>
<td><p><span data-ttu-id="ee343-187">Hele forrige regnskabsår</span><span class="sxs-lookup"><span data-stu-id="ee343-187">Entire previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee343-188">-1RÅ</span><span class="sxs-lookup"><span data-stu-id="ee343-188">-1FY</span></span></p></td>
<td><p><span data-ttu-id="ee343-189">Den aktuelle periode i forrige regnskabsår</span><span class="sxs-lookup"><span data-stu-id="ee343-189">Current period in previous fiscal year</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee343-190">-1RÅ[1..3]</span><span class="sxs-lookup"><span data-stu-id="ee343-190">-1FY[1..3]</span></span></p></td>
<td><p><span data-ttu-id="ee343-191">Først kvartal i forrige regnskabsår</span><span class="sxs-lookup"><span data-stu-id="ee343-191">First quarter of previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee343-192">-1RÅ[1..NP]</span><span class="sxs-lookup"><span data-stu-id="ee343-192">-1FY[1..CP]</span></span></p></td>
<td><p><span data-ttu-id="ee343-193">Fra starten af forrige regnskabsår til den nuværende periode i forrige regnskabsår, begge inklusive</span><span class="sxs-lookup"><span data-stu-id="ee343-193">From the beginning of previous fiscal year to current period in previous fiscal year, inclusive</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee343-194">-1RÅ[NP..FP]</span><span class="sxs-lookup"><span data-stu-id="ee343-194">-1FY[CP..LP]</span></span></p></td>
<td><p><span data-ttu-id="ee343-195">Fra den nuværende periode i det forrige regnskabsår til den sidste periode i det sidste regnskabsår, begge inklusive</span><span class="sxs-lookup"><span data-stu-id="ee343-195">From current period in previous fiscal year to last period of previous fiscal year, inclusive</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ee343-196">Hvis du vil foretage beregninger efter almindelige tidsperioder, skal du angive en formel i feltet **Sammenligningsdatoformel** i stedet.</span><span class="sxs-lookup"><span data-stu-id="ee343-196">If you want to calculate by regular time periods, you must enter a formula in the **Comparison Date Formula** field instead.</span></span>

> [!NOTE]
> <span data-ttu-id="ee343-197">Det er ikke altid gennemskueligt, hvilke perioder der sammenlignes, fordi du kan indstille et datofilter i en rapport, der dækker andre datoer end de regnskabsperioder, der afspejles i dataene i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="ee343-197">It is not always transparent which periods you are comparing because you can set a date filter on a report that spans different dates than the accounting periods that are reflected in the data in the chart of accounts.</span></span> <span data-ttu-id="ee343-198">Hvis du f.eks. vil oprette et kontoskema, hvor du vil sammenligne denne periode, hvor den samme periode sidste år, skal du indstille feltet **Filter for sammenligningsdatoperiode** til *-1FY*.</span><span class="sxs-lookup"><span data-stu-id="ee343-198">For example, you create an account schedule where you want to compare this period with the same period last year, so you set the **Comparison Date Period Filter** field to *-1FY*.</span></span> <span data-ttu-id="ee343-199">Derefter skal du køre rapporten den 28. februar og indstille datofilteret til januar og februar.</span><span class="sxs-lookup"><span data-stu-id="ee343-199">Then, you run the report on February 28th and set the date filter to January and February.</span></span> <span data-ttu-id="ee343-200">Kontoskemaet sammenligner nu januar og februar i indeværende år med januar sidste år, som er den eneste afsluttede regnskabsperiode af de to for sidste år.</span><span class="sxs-lookup"><span data-stu-id="ee343-200">As a result, the account schedule compares January and February this year to January last year, which is the only completed accounting period of the two for last year.</span></span>  


## <a name="see-also"></a><span data-ttu-id="ee343-201">Se også</span><span class="sxs-lookup"><span data-stu-id="ee343-201">See Also</span></span>
[<span data-ttu-id="ee343-202">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="ee343-202">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="ee343-203">Finans</span><span class="sxs-lookup"><span data-stu-id="ee343-203">Finance</span></span>](finance.md)  
[<span data-ttu-id="ee343-204">Konfigurere Finans</span><span class="sxs-lookup"><span data-stu-id="ee343-204">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="ee343-205">Finans- og kontoplanen</span><span class="sxs-lookup"><span data-stu-id="ee343-205">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="ee343-206">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ee343-206">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

