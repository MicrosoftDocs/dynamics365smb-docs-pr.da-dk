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
ms.date: 05/31/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e73c2dd0533aade4aa6225c9d2f385baaea3cfd1
ms.openlocfilehash: 69034b0eb97b595d0fbf5795e1fac34ecd775afe
ms.contentlocale: da-dk
ms.lasthandoff: 06/11/2018

---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a><span data-ttu-id="d547e-103">Forberede finansrapporter med kontoskemaer og kontokategorier</span><span class="sxs-lookup"><span data-stu-id="d547e-103">Prepare Financial Reporting with Account Schedules and Account Categories</span></span>
<span data-ttu-id="d547e-104">Du kan bruge kontoskemaer til at få indsigt i de finansielle oplysninger, der er gemt i din kontoplan.</span><span class="sxs-lookup"><span data-stu-id="d547e-104">Use account schedules to get insight into the financial data stored in your chart of accounts.</span></span> <span data-ttu-id="d547e-105">Kontoskemaer analyserer tal i finanskonti og sammenligner finansposter med finansbudgetposter.</span><span class="sxs-lookup"><span data-stu-id="d547e-105">Account schedules analyze figures in G/L accounts, and compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="d547e-106">Resultaterne vises i diagrammer på rollecenteret, f.eks. tabellen Likviditet, og i rapporter, f.eks. resultatopgørelsen og balancerapporterne.</span><span class="sxs-lookup"><span data-stu-id="d547e-106">The results display in charts on your Role Center, such as the Cash Flow chart, and in reports, such as the Income Statement and the Balance Sheet reports.</span></span>

<span data-ttu-id="d547e-107">Du kan få adgang til disse to rapporter, f.eks. med handlingen **Regnskabsopgørelser** i rollecentrene Virksomhedsleder og Bogholder.</span><span class="sxs-lookup"><span data-stu-id="d547e-107">You access these two reports, for example, with the **Financials Statements** action on the Business Manager and Accountant Role Centers.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="d547e-108"> indeholder et par eksempelkontoskemaer, som du kan bruge det samme, eller du kan konfigurere dine egen rækker og kolonner for at angive de tal, du vil sammenligne.</span><span class="sxs-lookup"><span data-stu-id="d547e-108"> provides a few sample account schedules that you can use right away, or you can set up your own rows and columns to specify the figures to compare.</span></span> <span data-ttu-id="d547e-109">Du kan f.eks. oprette kontoskemaer for at beregne avancer på dimensioner som afdelinger eller debitorgrupper.</span><span class="sxs-lookup"><span data-stu-id="d547e-109">For example, you can create account schedules to calculate profit margins on dimensions like departments or customer groups.</span></span> <span data-ttu-id="d547e-110">Du kan oprette så mange tilpassede kontoudtog, som du har behov for.</span><span class="sxs-lookup"><span data-stu-id="d547e-110">You can create as many customized financial statements as you want.</span></span>  

<span data-ttu-id="d547e-111">Oprettelse af kontoskemaer kræver en forståelse af de finansielle data i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="d547e-111">Setting up account schedules requires an understanding of the financial data in the chart of accounts.</span></span> <span data-ttu-id="d547e-112">Du kan f.eks. få vist finansposter som procenter af budgetposterne.</span><span class="sxs-lookup"><span data-stu-id="d547e-112">For example, you can view general ledger entries as percentages of budget entries.</span></span> <span data-ttu-id="d547e-113">Dette kræver, at der er oprettet budgetter.</span><span class="sxs-lookup"><span data-stu-id="d547e-113">This requires that budgets are created.</span></span> <span data-ttu-id="d547e-114">Du kan finde flere oplysninger i [Oprette finansbudgetter](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="d547e-114">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="account-categories-and-account-schedules"></a><span data-ttu-id="d547e-115">Kontokategorier og kontoskemaer</span><span class="sxs-lookup"><span data-stu-id="d547e-115">Account Categories and Account Schedules</span></span>
<span data-ttu-id="d547e-116">Du kan bruge kontokategorier til at ændre layoutet af regnskabet.</span><span class="sxs-lookup"><span data-stu-id="d547e-116">You can use account categories to change the layout of your financial statements.</span></span> <span data-ttu-id="d547e-117">Når du har oprettet kontokategorierne i vinduet **Finanskontokategorier**, og du vælger handlingen **Opret kontoskemaer** opdateres de underliggende kontoskemaer for de grundlæggende regnskabsrapporter.</span><span class="sxs-lookup"><span data-stu-id="d547e-117">After you set up your account categories in the **G/L Account Categories** window, and you choose the **Generate Account Schedules** action, the underlying account schedules for the core financial reports are updated.</span></span> <span data-ttu-id="d547e-118">Næste gang du kører en af disse rapporter, f.eks. rapporten Saldoopgørelse, tilføjes nye totaler og underordnede linjer, baseret på dine ændringer.</span><span class="sxs-lookup"><span data-stu-id="d547e-118">The next time you run one of these reports, such as the Balance Statement report, new totals and subentries are added, based on your changes.</span></span> <span data-ttu-id="d547e-119">Du kan finde flere oplysninger i afsnittet "Kontokategorier" i [Om finans- og kontoplanen](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="d547e-119">For more information, see The "Account Categories" section in [Understanding the General Ledger and the COA](finance-general-ledger.md).</span></span>  

## <a name="to-create-new-account-schedules"></a><span data-ttu-id="d547e-120">Sådan oprettes nye kontoskemaer</span><span class="sxs-lookup"><span data-stu-id="d547e-120">To create new account schedules</span></span>  
 <span data-ttu-id="d547e-121">Du bruger kontoskemaer til at analysere tal i finanskonti eller til at sammenligne finansposter med finansbudgetposter.</span><span class="sxs-lookup"><span data-stu-id="d547e-121">You use account schedules to analyze figures in general ledger accounts or to compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="d547e-122">Du kan f.eks. få vist finansposter som procenter af budgetposter.</span><span class="sxs-lookup"><span data-stu-id="d547e-122">For example, you can view the general ledger entries as percentages of the budget entries.</span></span>

1. <span data-ttu-id="d547e-123">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoskemaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d547e-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d547e-124">I vinduet **Kontoskemanavne** i skal du vælge handlingen **Ny** for at oprette et nyt kontoskemanavn.</span><span class="sxs-lookup"><span data-stu-id="d547e-124">In the **Account Schedule Names** window, choose the **New** action to create a new account schedule name.</span></span>
3. <span data-ttu-id="d547e-125">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="d547e-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="d547e-126">Vælg handlingen **Rediger kontoskema**.</span><span class="sxs-lookup"><span data-stu-id="d547e-126">Choose the **Edit Account Schedule** action.</span></span>
5. <span data-ttu-id="d547e-127">Udfyld felterne efter behov i vinduet **Kontoskema**.</span><span class="sxs-lookup"><span data-stu-id="d547e-127">In the **Account Schedule** window, fill in the fields as necessary.</span></span>  

    <span data-ttu-id="d547e-128">Når du har oprettet et nyt kontoskema og oprettet rækkerne, skal du angive kolonner.</span><span class="sxs-lookup"><span data-stu-id="d547e-128">When you have created a new account schedule and set up the rows, you must set up columns.</span></span> <span data-ttu-id="d547e-129">Du kan oprette dem manuelt eller tilknytte et foruddefineret kolonneformat til kontoskemaet.</span><span class="sxs-lookup"><span data-stu-id="d547e-129">You can either set them up manually or assign a predefined column layout to your account schedule.</span></span>
6. <span data-ttu-id="d547e-130">Vælg handlingen **Rediger opsætning af kolonneformat**.</span><span class="sxs-lookup"><span data-stu-id="d547e-130">Choose the **Edit Column Layout Setup** action.</span></span>
7. <span data-ttu-id="d547e-131">Udfyld felterne efter behov i vinduet **Kolonnelayout**.</span><span class="sxs-lookup"><span data-stu-id="d547e-131">In the **Column Layout** window, fill in the fields as necessary.</span></span>

> [!NOTE]  
> <span data-ttu-id="d547e-132">Hvis du ikke har tildelt et standard kolonneformat til kontoskemaet, skal du definere kolonnerne manuelt.</span><span class="sxs-lookup"><span data-stu-id="d547e-132">If you did not assign a default column layout to the account schedule, you must set the columns up manually.</span></span>

### <a name="to-copy-an-existing-account-schedule"></a><span data-ttu-id="d547e-133">Sådan kopieres et eksisterende kontoskema</span><span class="sxs-lookup"><span data-stu-id="d547e-133">To copy an existing account schedule</span></span>
<span data-ttu-id="d547e-134">Kontoskemaerne i standardversionen af [!INCLUDE[d365fin](includes/d365fin_md.md)] er grundlaget for de økonomiske standardrapporter, som muligvis ikke er egnet til din virksomheds behov.</span><span class="sxs-lookup"><span data-stu-id="d547e-134">The account schedules in the standard version of [!INCLUDE[d365fin](includes/d365fin_md.md)] are the basis of the standard financial reports, which may not suit the needs of your business.</span></span> <span data-ttu-id="d547e-135">Du kan starte ved at kopiere et eksisterende kontoskema for hurtigt at oprette din egne regnskabsrapporter.</span><span class="sxs-lookup"><span data-stu-id="d547e-135">To quickly create your own financial reports, you can start by copying an existing account schedule.</span></span>
1. <span data-ttu-id="d547e-136">I vinduet **Kontoskemaer** skal du vælge et kontoskema og derefter vælge handlingen **Kopiér kontoskema**.</span><span class="sxs-lookup"><span data-stu-id="d547e-136">In the **Account Schedules** window, select an account schedule, and then choose the **Copy Account Schedule** action.</span></span>
2. <span data-ttu-id="d547e-137">I vinduet **Kopiér kontoskema** skal du udfylde felterne efter behov, og derefter vælge knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="d547e-137">In the **Copy Account Schedule** window, fill in the fields as necessary, and then choose the **OK** button.</span></span>

### <a name="to-create-a-column-that-calculates-percentages"></a><span data-ttu-id="d547e-138">Sådan oprettes en kolonne, hvor procenten beregnes</span><span class="sxs-lookup"><span data-stu-id="d547e-138">To create a column that calculates percentages</span></span>  
<span data-ttu-id="d547e-139">Du vil muligvis gerne medtage en kolonne i et kontoskema for at beregne procenter af et totalbeløb.</span><span class="sxs-lookup"><span data-stu-id="d547e-139">Sometimes you may want to include a column in an account schedule to calculate percentages of a total.</span></span> <span data-ttu-id="d547e-140">Hvis du f.eks. har et antal rækker, som specificerer salg efter dimension, kan du have en kolonne, som angiver procenten af det samlede salg, som hver række repræsenterer.</span><span class="sxs-lookup"><span data-stu-id="d547e-140">For example, if you have a number of rows that break down sales by dimension, you may want a column to indicate the percentage of total sales that each row represents.</span></span>

1. <span data-ttu-id="d547e-141">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoskemaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d547e-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="d547e-142">Vælg et kontoskema i vinduet **Kontoskemanavne**.</span><span class="sxs-lookup"><span data-stu-id="d547e-142">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="d547e-143">Vælg handlingen **Rediger kontoskema** for at konfigurere en kontoskemarække til beregning af den total, som procentdelene baseres på.</span><span class="sxs-lookup"><span data-stu-id="d547e-143">Choose the **Edit Account Schedule** action to set up an account schedule row to calculate the total on which the percentages will be based.</span></span>  
4. <span data-ttu-id="d547e-144">Indsæt en linje lige over den første række, som du vil vise en procent for.</span><span class="sxs-lookup"><span data-stu-id="d547e-144">Insert a line immediately above the first row for which you want to display a percentage.</span></span>  
5. <span data-ttu-id="d547e-145">Udfyld felterne på linjen på følgende måde: I feltet **Sammentællingstype** skal du angive **Angiv grundlag for procent**.</span><span class="sxs-lookup"><span data-stu-id="d547e-145">Fill in the fields on the line as follows: In the **Totaling Type** field, enter **Set Base for Percent**.</span></span> <span data-ttu-id="d547e-146">I feltet **Sammentælling** skal du indtaste en formel for den total, som procentdelen skal baseres på.</span><span class="sxs-lookup"><span data-stu-id="d547e-146">In the **Totaling** field, enter a formula for the total that the percentage will be based on.</span></span> <span data-ttu-id="d547e-147">Hvis række 11 f.eks. indeholder det samlede salg, indtastes **11**.</span><span class="sxs-lookup"><span data-stu-id="d547e-147">For example, if row 11 contains the total sales, enter **11**.</span></span>  
6. <span data-ttu-id="d547e-148">Vælg handlingen **Rediger opsætning af kolonneformat** for at oprette en kolonne.</span><span class="sxs-lookup"><span data-stu-id="d547e-148">Choose the **Edit Column Layout Setup** action to set up a column.</span></span>  
7. <span data-ttu-id="d547e-149">Udfyld felterne på linjen på følgende måde: I feltet **Kolonnetype** skal du vælge **Formel**.</span><span class="sxs-lookup"><span data-stu-id="d547e-149">Fill in the fields on the line as follows: In the **Column Type** field, select **Formula**.</span></span> <span data-ttu-id="d547e-150">I feltet **Formel** skal du indtaste en formel for det beløb, som du vil beregne en procentdel for, efterfulgt af %.</span><span class="sxs-lookup"><span data-stu-id="d547e-150">In the **Formula** field, enter a formula for the amount that you want to calculate a percentage for, followed by %.</span></span> <span data-ttu-id="d547e-151">Hvis kolonnenummer N f.eks. indeholder bevægelsen, indtastes **N %**.</span><span class="sxs-lookup"><span data-stu-id="d547e-151">For example, if column number N contains the net change, enter **N%**.</span></span>  
8. <span data-ttu-id="d547e-152">Gentag trin 4 til 7 for alle de grupper af rækker, du vil specificere efter procent.</span><span class="sxs-lookup"><span data-stu-id="d547e-152">Repeat steps 4 through 7 for each group of rows that you want to break down by percentage.</span></span>

## <a name="to-set-up-account-schedules-with-overviews"></a><span data-ttu-id="d547e-153">Sådan oprettes kontoskemaer med oversigter</span><span class="sxs-lookup"><span data-stu-id="d547e-153">To set up account schedules with overviews</span></span>  
<span data-ttu-id="d547e-154">Du kan bruge et kontoskema til at oprette en opgørelse, hvor tallene i finansposter sammenlignes med tallene i finansbudgettet.</span><span class="sxs-lookup"><span data-stu-id="d547e-154">You can use an account schedule to create a statement comparing general ledger figures and general leger budget figures.</span></span>

1. <span data-ttu-id="d547e-155">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoskemaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d547e-155">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="d547e-156">Vælg et kontoskema i vinduet **Kontoskemanavne**.</span><span class="sxs-lookup"><span data-stu-id="d547e-156">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="d547e-157">Vælg handlingen **Rediger kontoskema**</span><span class="sxs-lookup"><span data-stu-id="d547e-157">Choose the **Edit Account Schedule** action</span></span>  
4. <span data-ttu-id="d547e-158">I vinduet **Kontoskema** skal du vælge standardkontoskemanavnet i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="d547e-158">In the **Account Schedule** window, in the **Name** field, select the default account schedule name.</span></span>
5. <span data-ttu-id="d547e-159">Vælg handlingen **Indsæt konti**.</span><span class="sxs-lookup"><span data-stu-id="d547e-159">Choose the **Insert Accounts** action.</span></span>  
6. <span data-ttu-id="d547e-160">Marker de konti, som du ønsker at medtage i opgørelsen, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="d547e-160">Select the accounts that you want to include in your statement, and then choose the **OK** button.</span></span>

    <span data-ttu-id="d547e-161">Kontiene indsættes i kontoskemaet.</span><span class="sxs-lookup"><span data-stu-id="d547e-161">The accounts are now inserted into your account schedule.</span></span> <span data-ttu-id="d547e-162">Hvis du vil, kan du også ændre kolonneformatet.</span><span class="sxs-lookup"><span data-stu-id="d547e-162">If you want you can also change the column layout.</span></span>  
7. <span data-ttu-id="d547e-163">Vælg handlingen **Oversigt**.</span><span class="sxs-lookup"><span data-stu-id="d547e-163">Choose the **Overview** action.</span></span>  
8. <span data-ttu-id="d547e-164">Klik på oversigtspanelet **Dimensionsfiltre**, og sæt budgetfilteret til det ønskede filternavn.</span><span class="sxs-lookup"><span data-stu-id="d547e-164">On the **Dimension Filters** FastTab, set the budget filter to the desired filter name.</span></span>  
9. <span data-ttu-id="d547e-165">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="d547e-165">Choose the **OK** button.</span></span>  

<span data-ttu-id="d547e-166">Du kan nu kopiere og indsætte budgetoversigten i et regneark..</span><span class="sxs-lookup"><span data-stu-id="d547e-166">Now you can copy and paste your budget statement into a spreadsheet.</span></span>  

## <a name="comparing-accounting-periods-using-period-formulas"></a><span data-ttu-id="d547e-167">Sammenligne regnskabsperioder ved hjælp af periodeformler</span><span class="sxs-lookup"><span data-stu-id="d547e-167">Comparing Accounting Periods using Period Formulas</span></span>
<span data-ttu-id="d547e-168">Kontoskemaet kan sammenligne resultaterne af forskellige regnskabsperioder, f.eks. denne måned sammenlignet med samme måned sidste år.</span><span class="sxs-lookup"><span data-stu-id="d547e-168">Your account schedule can compare the results of different accounting periods, such as this month versus same month last year.</span></span> <span data-ttu-id="d547e-169">For at gøre det skal du tilføje en kolonne i feltet **Sammenligningsperiodeformel** og derefter indstille dette felt til en periodeformel.</span><span class="sxs-lookup"><span data-stu-id="d547e-169">To do that, you add a column with the **Comparison Period Formula** field, and then set that field to a period formula.</span></span>  

<span data-ttu-id="d547e-170">En regnskabsperiode skal ikke følge kalenderåret, men hvert regnskabsår skal have det samme antal regnskabsperioder, selvom hver periode kan variere i længde.</span><span class="sxs-lookup"><span data-stu-id="d547e-170">An accounting period does not have to match the calendar, but each fiscal year must have the same number of accounting periods, even though each period can be different in length.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="d547e-171"> bruger periodeformlen til at beregne beløbet fra sammenligningsperioden i relation til den periode, som er defineret af datofiltret i rapportanmodningen.</span><span class="sxs-lookup"><span data-stu-id="d547e-171"> uses the period formula to calculate the amount from the comparison period in relation to the period represented by the date filter on the report request.</span></span> <span data-ttu-id="d547e-172">Sammenligningsperioden er baseret på perioden fra startdatoen i datofilteret.</span><span class="sxs-lookup"><span data-stu-id="d547e-172">The comparison period is based on the period of the start date of the date filter.</span></span> <span data-ttu-id="d547e-173">Periodeangivelserne forkortes på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="d547e-173">The abbreviations for period specifications are:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d547e-174">Forkortelse</span><span class="sxs-lookup"><span data-stu-id="d547e-174">Abbreviation</span></span></th>
<th><span data-ttu-id="d547e-175">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d547e-175">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d547e-176">P</span><span class="sxs-lookup"><span data-stu-id="d547e-176">P</span></span></p></td>
<td><p><span data-ttu-id="d547e-177">Periode</span><span class="sxs-lookup"><span data-stu-id="d547e-177">Period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d547e-178">FP</span><span class="sxs-lookup"><span data-stu-id="d547e-178">LP</span></span></p></td>
<td><p><span data-ttu-id="d547e-179">Forrige periode i et regnskabsår, halvår eller kvartal.</span><span class="sxs-lookup"><span data-stu-id="d547e-179">Last period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d547e-180">NP</span><span class="sxs-lookup"><span data-stu-id="d547e-180">CP</span></span></p></td>
<td><p><span data-ttu-id="d547e-181">Nuværende periode i et regnskabsår, halvår eller kvartal.</span><span class="sxs-lookup"><span data-stu-id="d547e-181">Current period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d547e-182">RÅ</span><span class="sxs-lookup"><span data-stu-id="d547e-182">FY</span></span></p></td>
<td><p><span data-ttu-id="d547e-183">Regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="d547e-183">Fiscal year.</span></span> <span data-ttu-id="d547e-184">RÅ[1..3] betegner f.eks. det første kvartal i det indeværende regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="d547e-184">For example, FY[1..3] denotes first quarter of the current fiscal year</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d547e-185">Eksempler på formler:</span><span class="sxs-lookup"><span data-stu-id="d547e-185">Examples of formulas:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d547e-186">Formel</span><span class="sxs-lookup"><span data-stu-id="d547e-186">Formula</span></span></th>
<th><span data-ttu-id="d547e-187">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d547e-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d547e-188">&lt;Tomt&gt;</span><span class="sxs-lookup"><span data-stu-id="d547e-188">&lt;Blank&gt;</span></span></p></td>
<td><p><span data-ttu-id="d547e-189">Nuværende periode</span><span class="sxs-lookup"><span data-stu-id="d547e-189">Current period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d547e-190">-1P</span><span class="sxs-lookup"><span data-stu-id="d547e-190">-1P</span></span></p></td>
<td><p><span data-ttu-id="d547e-191">Forrige periode</span><span class="sxs-lookup"><span data-stu-id="d547e-191">Previous period</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d547e-192">-1RÅ[1..FP]</span><span class="sxs-lookup"><span data-stu-id="d547e-192">-1FY[1..LP]</span></span></p></td>
<td><p><span data-ttu-id="d547e-193">Hele forrige regnskabsår</span><span class="sxs-lookup"><span data-stu-id="d547e-193">Entire previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d547e-194">-1RÅ</span><span class="sxs-lookup"><span data-stu-id="d547e-194">-1FY</span></span></p></td>
<td><p><span data-ttu-id="d547e-195">Den aktuelle periode i forrige regnskabsår</span><span class="sxs-lookup"><span data-stu-id="d547e-195">Current period in previous fiscal year</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d547e-196">-1RÅ[1..3]</span><span class="sxs-lookup"><span data-stu-id="d547e-196">-1FY[1..3]</span></span></p></td>
<td><p><span data-ttu-id="d547e-197">Først kvartal i forrige regnskabsår</span><span class="sxs-lookup"><span data-stu-id="d547e-197">First quarter of previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d547e-198">-1RÅ[1..NP]</span><span class="sxs-lookup"><span data-stu-id="d547e-198">-1FY[1..CP]</span></span></p></td>
<td><p><span data-ttu-id="d547e-199">Fra starten af forrige regnskabsår til den nuværende periode i forrige regnskabsår, begge inklusive</span><span class="sxs-lookup"><span data-stu-id="d547e-199">From the beginning of previous fiscal year to current period in previous fiscal year, inclusive</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d547e-200">-1RÅ[NP..FP]</span><span class="sxs-lookup"><span data-stu-id="d547e-200">-1FY[CP..LP]</span></span></p></td>
<td><p><span data-ttu-id="d547e-201">Fra den nuværende periode i det forrige regnskabsår til den sidste periode i det sidste regnskabsår, begge inklusive</span><span class="sxs-lookup"><span data-stu-id="d547e-201">From current period in previous fiscal year to last period of previous fiscal year, inclusive</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d547e-202">Hvis du vil foretage beregninger efter almindelige tidsperioder, skal du angive en formel i feltet **Sammenligningsdatoformel** i stedet.</span><span class="sxs-lookup"><span data-stu-id="d547e-202">If you want to calculate by regular time periods, you must enter a formula in the **Comparison Date Formula** field instead.</span></span>

> [!NOTE]
> <span data-ttu-id="d547e-203">Det er ikke altid gennemskueligt, hvilke perioder der sammenlignes, fordi du kan indstille et datofilter i en rapport, der dækker andre datoer end de regnskabsperioder, der afspejles i dataene i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="d547e-203">It is not always transparent which periods you are comparing because you can set a date filter on a report that spans different dates than the accounting periods that are reflected in the data in the chart of accounts.</span></span> <span data-ttu-id="d547e-204">Hvis du f.eks. vil oprette et kontoskema, hvor du vil sammenligne denne periode, hvor den samme periode sidste år, skal du indstille feltet **Filter for sammenligningsdatoperiode** til *-1FY*.</span><span class="sxs-lookup"><span data-stu-id="d547e-204">For example, you create an account schedule where you want to compare this period with the same period last year, so you set the **Comparison Date Period Filter** field to *-1FY*.</span></span> <span data-ttu-id="d547e-205">Derefter skal du køre rapporten den 28. februar og indstille datofilteret til januar og februar.</span><span class="sxs-lookup"><span data-stu-id="d547e-205">Then, you run the report on February 28th and set the date filter to January and February.</span></span> <span data-ttu-id="d547e-206">Kontoskemaet sammenligner nu januar og februar i indeværende år med januar sidste år, som er den eneste afsluttede regnskabsperiode af de to for sidste år.</span><span class="sxs-lookup"><span data-stu-id="d547e-206">As a result, the account schedule compares January and February this year to January last year, which is the only completed accounting period of the two for last year.</span></span>  


## <a name="see-also"></a><span data-ttu-id="d547e-207">Se også</span><span class="sxs-lookup"><span data-stu-id="d547e-207">See Also</span></span>
[<span data-ttu-id="d547e-208">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="d547e-208">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="d547e-209">Finans</span><span class="sxs-lookup"><span data-stu-id="d547e-209">Finance</span></span>](finance.md)  
[<span data-ttu-id="d547e-210">Konfigurere Finans</span><span class="sxs-lookup"><span data-stu-id="d547e-210">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="d547e-211">Finans- og kontoplanen</span><span class="sxs-lookup"><span data-stu-id="d547e-211">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="d547e-212">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d547e-212">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

