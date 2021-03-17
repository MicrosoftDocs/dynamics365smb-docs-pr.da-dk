---
title: Vise brugerdefinerede Power BI-rapporter for Business Central-data| Microsoft Docs
description: Du kan bruge Power BI-rapporter til at få ekstra indsigt i data på lister.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6c818940357ed21a994e7553517989a0c16accec
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379269"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a><span data-ttu-id="3edfb-103">Oprette Power BI-rapporter til visning af listedata i [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="3edfb-103">Creating Power BI Reports for Displaying List Data in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

[!INCLUDE[prod_long](includes/prod_long.md)] <span data-ttu-id="3edfb-104">indeholder et faktaboks-kontrolelement på en række vigtige sider, der giver ekstra indsigt i dataene på listen.</span><span class="sxs-lookup"><span data-stu-id="3edfb-104">includes a FactBox control element on a number of key list pages that provide additional insight into the data in the list.</span></span> <span data-ttu-id="3edfb-105">Når du flytter mellem rækkerne på listen, opdateres rapporten og filtreres for den valgte post.</span><span class="sxs-lookup"><span data-stu-id="3edfb-105">As you move between rows in the list, the report is updated and filtered for the selected entry.</span></span> <span data-ttu-id="3edfb-106">Du kan oprette brugerdefinerede rapporter, der skal vises i dette kontrolelement.</span><span class="sxs-lookup"><span data-stu-id="3edfb-106">You can create custom reports to display in this control.</span></span> <span data-ttu-id="3edfb-107">Der er dog nogle få regler, du skal følge for at sikre, at rapporter fungerer som forventet.</span><span class="sxs-lookup"><span data-stu-id="3edfb-107">However, there are a few rules to follow to ensure that reports work as expected.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="3edfb-108">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="3edfb-108">Prerequisites</span></span>

- <span data-ttu-id="3edfb-109">En Power BI-konto.</span><span class="sxs-lookup"><span data-stu-id="3edfb-109">A Power BI account.</span></span>
- <span data-ttu-id="3edfb-110">Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="3edfb-110">Power BI Desktop.</span></span>

<span data-ttu-id="3edfb-111">Du kan finde flere oplysninger om at komme i gang under [Bruge [!INCLUDE[prod_short](includes/prod_short.md)] som Power BI-datakilde](across-how-use-financials-data-source-powerbi.md).</span><span class="sxs-lookup"><span data-stu-id="3edfb-111">For more information about getting started, see [Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).</span></span>

## <a name="defining-the-report-data-set"></a><span data-ttu-id="3edfb-112">Definere rapportdatasættet</span><span class="sxs-lookup"><span data-stu-id="3edfb-112">Defining the report data set</span></span>

<span data-ttu-id="3edfb-113">Angiv den datakilde, der indeholder de data, som vedrører listen.</span><span class="sxs-lookup"><span data-stu-id="3edfb-113">Specify the data source that contains the data related to the list.</span></span> <span data-ttu-id="3edfb-114">Hvis du f.eks. vil oprette en rapport til salgslisten, skal du sikre, at datasættet indeholder salgsrelaterede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="3edfb-114">For example, to create a report for the Sales List, ensure the data set contains information related to sales.</span></span>  

## <a name="defining-the-report-filter"></a><span data-ttu-id="3edfb-115">Definere rapportfilteret</span><span class="sxs-lookup"><span data-stu-id="3edfb-115">Defining the report filter</span></span>

<span data-ttu-id="3edfb-116">Hvis du vil foretage dataopdatering til den valgte post på listen, skal du føje et filter til rapporten.</span><span class="sxs-lookup"><span data-stu-id="3edfb-116">To make the data update to the selected record in the list, you add a filter to the report.</span></span> <span data-ttu-id="3edfb-117">Filteret skal indeholde et felt fra den datakilde, der bruges som *primær nøgle*.</span><span class="sxs-lookup"><span data-stu-id="3edfb-117">The filter must include a field of the data source that's used as the *primary key*.</span></span> <span data-ttu-id="3edfb-118">I de fleste tilfælde er primærnøglen for en liste feltet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="3edfb-118">In most cases, the primary key for a list is the **No.**</span></span> <span data-ttu-id="3edfb-119">.</span><span class="sxs-lookup"><span data-stu-id="3edfb-119">field.</span></span>

<span data-ttu-id="3edfb-120">Du kan definere et filter for rapporten, vælge primærnøglen på listen over tilgængelige felter og derefter trække og slippe direkte i sektionen **Rapportfilter**.</span><span class="sxs-lookup"><span data-stu-id="3edfb-120">To define a filter for the report, select the primary key from the list of available fields, and then drag and drop that field into the **Report Filter** section.</span></span> <span data-ttu-id="3edfb-121">Filteret skal være et grundlæggende rapportfilter, som er defineret for alle sider.</span><span class="sxs-lookup"><span data-stu-id="3edfb-121">The filter must be a basic report filter that's defined for all pages.</span></span> <span data-ttu-id="3edfb-122">Det kan ikke være sidefilter, visuelt eller avanceret filter.</span><span class="sxs-lookup"><span data-stu-id="3edfb-122">It can't be page, visual, or advanced filter.</span></span>

![Angive rapportfilteret for rapporten Salgsfakturaaktivitet](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)

## <a name="setting-the-report-size-and-color"></a><span data-ttu-id="3edfb-124">Angive størrelse og farve på rapporten</span><span class="sxs-lookup"><span data-stu-id="3edfb-124">Setting the report size and color</span></span>

<span data-ttu-id="3edfb-125">Størrelsen på rapporten skal angives til 325 x 310 pixel.</span><span class="sxs-lookup"><span data-stu-id="3edfb-125">The size of the report must be set to 325 pixels by 310 pixels.</span></span> <span data-ttu-id="3edfb-126">Denne størrelse angiver rapportens korrekte skalering på den ledige plads i Power BI-faktaboksens kontrolelementet i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="3edfb-126">This size provides the proper scaling of the report in the available space of the Power BI FactBox control in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="3edfb-127">Hvis du vil angive størrelsen på rapporten, skal du placere fokus uden for rapportens layoutområde og derefter vælge malerulleikonet.</span><span class="sxs-lookup"><span data-stu-id="3edfb-127">To define the size of the report, place focus outside of the report layout area, and then choose the paint roller icon.</span></span>

![Angive rapportbredde og højde for rapporten Salgsfakturaaktivitet](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

<span data-ttu-id="3edfb-129">Du kan ændre bredden og højden for rapporten ved at vælge **Brugerdefineret** i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="3edfb-129">You can change the width and height of the report by choosing **Custom** in the **Type** field.</span></span>

<span data-ttu-id="3edfb-130">Hvis baggrunden for rapporten skal blende i med baggrundsfarven for Power BI-faktabokskontrolelementet, skal du angive baggrundsfarven *#FFFFFF* til rapporten.</span><span class="sxs-lookup"><span data-stu-id="3edfb-130">If you want the background of the report to blend with the background color of the Power BI FactBox control, set report background color to *#FFFFFF*.</span></span> 

## <a name="using-reports-with-multiple-pages"></a><span data-ttu-id="3edfb-131">Bruge rapporter med flere sider</span><span class="sxs-lookup"><span data-stu-id="3edfb-131">Using reports with multiple pages</span></span>

<span data-ttu-id="3edfb-132">Med Power BI kan du oprette en enkelt rapport med flere sider.</span><span class="sxs-lookup"><span data-stu-id="3edfb-132">With Power BI, you can create a single report with multiple pages.</span></span> <span data-ttu-id="3edfb-133">Men i forbindelse med rapporter, der vises med listesider, kan vi ikke anbefale, at de har mere end én side.</span><span class="sxs-lookup"><span data-stu-id="3edfb-133">However, for reports that will display with list pages, we don't recommend that they have more than one page.</span></span> <span data-ttu-id="3edfb-134">Power BI-faktaboksen viser kun den første side i rapporten.</span><span class="sxs-lookup"><span data-stu-id="3edfb-134">The Power BI FactBox will only show the first page of your report.</span></span>

## <a name="naming-the-report"></a><span data-ttu-id="3edfb-135">Navngive rapporten</span><span class="sxs-lookup"><span data-stu-id="3edfb-135">Naming the report</span></span>

<span data-ttu-id="3edfb-136">Giv rapporten et navn, der indeholder navnet på den listeside, der er tilknyttet rapporten.</span><span class="sxs-lookup"><span data-stu-id="3edfb-136">Give the report a name that contains the name of the list page associated with the report.</span></span> <span data-ttu-id="3edfb-137">Hvis rapporten f.eks. er til **Kreditor**-listesiden, skal du medtage ordet *kreditor* et sted i navnet.</span><span class="sxs-lookup"><span data-stu-id="3edfb-137">For example, if the report is for the **Vendor** list page, include the word *vendor* somewhere in the name.</span></span>  

<span data-ttu-id="3edfb-138">Denne navngivningskonvention er ikke et krav.</span><span class="sxs-lookup"><span data-stu-id="3edfb-138">This naming convention isn't a requirement.</span></span> <span data-ttu-id="3edfb-139">Det gør imidlertid hurtigere at vælge rapporter i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="3edfb-139">However, it makes selecting reports in [!INCLUDE[prod_short](includes/prod_short.md)] quicker.</span></span> <span data-ttu-id="3edfb-140">Når siden til valg af rapporter åbnes fra en listeside, filtreres den automatisk på basis af navnet på siden.</span><span class="sxs-lookup"><span data-stu-id="3edfb-140">When the report selection page opens from a list page, it's automatically filtered based on the page name.</span></span> <span data-ttu-id="3edfb-141">Denne filtrering sker for at begrænse de viste rapporter.</span><span class="sxs-lookup"><span data-stu-id="3edfb-141">This filtering is done to limit the reports that are displayed.</span></span> <span data-ttu-id="3edfb-142">Brugerne kan rydde filteret for at se en komplet liste over tilgængelige rapporter i Power BI.</span><span class="sxs-lookup"><span data-stu-id="3edfb-142">Users can clear the filter to get a full list of reports available in Power BI.</span></span>  

## <a name="fixing-problems"></a><span data-ttu-id="3edfb-143">Løse problemer</span><span class="sxs-lookup"><span data-stu-id="3edfb-143">Fixing problems</span></span>

<span data-ttu-id="3edfb-144">Denne sektion indeholder en løsning på de mest almindelige problemer, der kan opstå, når du opretter Power BI-rapporten.</span><span class="sxs-lookup"><span data-stu-id="3edfb-144">This section provides a workaround for the most typical problems that can occur when you create the Power BI report.</span></span>  

#### <a name="you-cant-see-a-report-on-the-select-report-page"></a><span data-ttu-id="3edfb-145">Du kan ikke se en rapport på siden Vælg rapport</span><span class="sxs-lookup"><span data-stu-id="3edfb-145">You can't see a report on the Select Report page</span></span>

<span data-ttu-id="3edfb-146">Det skyldes sandsynligvis, at rapportens navn ikke indeholder navnet på listesiden.</span><span class="sxs-lookup"><span data-stu-id="3edfb-146">It's probably because the report's name doesn't contain the name of the list page.</span></span> <span data-ttu-id="3edfb-147">Ryd filteret for at se en komplet liste over tilgængelige rapporter i Power BI.</span><span class="sxs-lookup"><span data-stu-id="3edfb-147">Clear the filter to get a full list of Power BI reports available.</span></span>  

#### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a><span data-ttu-id="3edfb-148">Rapporten er indlæst, men tom og ikke filtreret eller filtreret forkert</span><span class="sxs-lookup"><span data-stu-id="3edfb-148">Report is loaded but blank, not filtered or filtered incorrectly</span></span>

<span data-ttu-id="3edfb-149">Kontrollér, at rapportfilteret indeholder den rette primære nøgle.</span><span class="sxs-lookup"><span data-stu-id="3edfb-149">Verify that the report filter contains the right primary key.</span></span> <span data-ttu-id="3edfb-150">I de fleste tilfælde er dette felt **Nr.**</span><span class="sxs-lookup"><span data-stu-id="3edfb-150">In most cases, this field is the **No.**</span></span> <span data-ttu-id="3edfb-151">men i tabellen **Finanspost** skal du f.eks. bruge feltet **Løbenr.**</span><span class="sxs-lookup"><span data-stu-id="3edfb-151">field, but in the **G/L Entry** table, for example, you must use the **Entry No.** field.</span></span>

#### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a><span data-ttu-id="3edfb-152">Rapporten indlæses, men viser en side, du ikke forventede</span><span class="sxs-lookup"><span data-stu-id="3edfb-152">Report is loaded, but it shows a page you didn't expect</span></span>

<span data-ttu-id="3edfb-153">Kontrollér, at den side, du vil have vist, er den første side i rapporten.</span><span class="sxs-lookup"><span data-stu-id="3edfb-153">Verify that the page you want displayed is the first page in your report.</span></span>  

#### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a><span data-ttu-id="3edfb-154">Rapporten vises med en uønsket grå kant, er for lille eller for stor</span><span class="sxs-lookup"><span data-stu-id="3edfb-154">Report appears with an unwanted gray boarder, or it's too small or too large</span></span>

<span data-ttu-id="3edfb-155">Kontroller, at rapportstørrelse er indstillet til 325 x 310 pixel.</span><span class="sxs-lookup"><span data-stu-id="3edfb-155">Verify that the report size is set to 325 pixels x 310 pixels.</span></span> <span data-ttu-id="3edfb-156">Gem rapporten, og opdater derefter oversigtssiden.</span><span class="sxs-lookup"><span data-stu-id="3edfb-156">Save the report, and then refresh the list page.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="3edfb-157">Se relateret oplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="3edfb-157">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="3edfb-158">Se også</span><span class="sxs-lookup"><span data-stu-id="3edfb-158">See Also</span></span>

[<span data-ttu-id="3edfb-159">Aktivere virksomhedens data til Power BI</span><span class="sxs-lookup"><span data-stu-id="3edfb-159">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
<span data-ttu-id="3edfb-160">[Bruge [!INCLUDE[prod_short](includes/prod_short.md)] som Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="3edfb-160">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
[<span data-ttu-id="3edfb-161">Introduktion</span><span class="sxs-lookup"><span data-stu-id="3edfb-161">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="3edfb-162">[Opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="3edfb-162">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
[<span data-ttu-id="3edfb-163">Finans</span><span class="sxs-lookup"><span data-stu-id="3edfb-163">Finance</span></span>](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]