---
title: Vise brugerdefinerede Power BI-rapporter for Business Central-data
description: Du kan bruge Power BI-rapporter til at få ekstra indsigt i data på lister.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/26/2021
ms.author: jswymer
ms.openlocfilehash: d2ce2588604ae676ba8b2cb73878a2d8dfd32b63
ms.sourcegitcommit: 652e4b0e1a09bff265014d9f8eb3b038ab0db79e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087690"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a><span data-ttu-id="661b1-103">Oprettelse af Power BI-rapporter til visning af listedata i [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="661b1-103">Creating Power BI Reports for Displaying List Data in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

[!INCLUDE[prod_long](includes/prod_long.md)] <span data-ttu-id="661b1-104">indeholder et kontrolelement for Power BI-faktaboksen på mange nøglelistesider.</span><span class="sxs-lookup"><span data-stu-id="661b1-104">includes a Power BI FactBox control element on many key list pages.</span></span> <span data-ttu-id="661b1-105">Formålet med denne faktaboks er at vise Power BI-rapporter, der er relateret til poster på listerne, hvilket giver ekstra indblik i dataene.</span><span class="sxs-lookup"><span data-stu-id="661b1-105">The purpose of this FactBox is to display Power BI reports that are related to records in the lists, providing extra insight into the data.</span></span> <span data-ttu-id="661b1-106">Formålet er, at rapporten opdateres for den valgte post, når du bevæger dig mellem rækkerne på listen.</span><span class="sxs-lookup"><span data-stu-id="661b1-106">The idea is that as you move between rows in the list, the report updates for the selected entry.</span></span>

[!INCLUDE[prod_long](includes/prod_long.md)] <span data-ttu-id="661b1-107">er klar med nogle af disse rapporter.</span><span class="sxs-lookup"><span data-stu-id="661b1-107">comes ready with some of these reports.</span></span> <span data-ttu-id="661b1-108">Du kan også oprette dine egne brugerdefinerede rapporter, der skal vises i denne faktaboks.</span><span class="sxs-lookup"><span data-stu-id="661b1-108">You can also create your own custom reports that display in this FactBox.</span></span> <span data-ttu-id="661b1-109">Oprettelse af disse rapporter svarer til andre rapporter.</span><span class="sxs-lookup"><span data-stu-id="661b1-109">Creating these reports is similar to other reports.</span></span> <span data-ttu-id="661b1-110">Men der er nogle få designregler, som du skal følge for at sikre, at rapporterne vises som forventet.</span><span class="sxs-lookup"><span data-stu-id="661b1-110">But there are a few design rules you'll have to follow to make sure the reports display as expected.</span></span> <span data-ttu-id="661b1-111">Reglerne beskrives i denne artikel.</span><span class="sxs-lookup"><span data-stu-id="661b1-111">These rules are explained in this article.</span></span>

> [!NOTE]
> <span data-ttu-id="661b1-112">Generelle oplysninger om oprettelse og udgivelse af Power BI-rapporter til Business Central finder du i [Oprettelse af Power BI-rapporter for at vise [!INCLUDE [prod_long](includes/prod_long.md)]-data](across-how-use-financials-data-source-powerbi.md).</span><span class="sxs-lookup"><span data-stu-id="661b1-112">For general information about creating and publishing Power BI reports for Business Central, see [Building Power BI Reports to Display [!INCLUDE [prod_long](includes/prod_long.md)] Data](across-how-use-financials-data-source-powerbi.md).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="661b1-113">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="661b1-113">Prerequisites</span></span>

- <span data-ttu-id="661b1-114">En Power BI-konto.</span><span class="sxs-lookup"><span data-stu-id="661b1-114">A Power BI account.</span></span>
- <span data-ttu-id="661b1-115">Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="661b1-115">Power BI Desktop.</span></span>

<!-- 
For more information about getting started, see [Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).-->

## <a name="create-a-report-for-a-list-page"></a><span data-ttu-id="661b1-116">Oprette en rapport til en listeside</span><span class="sxs-lookup"><span data-stu-id="661b1-116">Create a report for a list page</span></span>

1. <span data-ttu-id="661b1-117">Start Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="661b1-117">Start Power BI Desktop.</span></span>
2. <span data-ttu-id="661b1-118">Vælg **Hent data**, og begynd at vælge datakilden for rapporten.</span><span class="sxs-lookup"><span data-stu-id="661b1-118">Select **Get Data**, and start choosing the data source for the report.</span></span>

    <span data-ttu-id="661b1-119">Angiv, hvilke listesider for Business Central, der skal indeholde de data, du vil have med i rapporten.</span><span class="sxs-lookup"><span data-stu-id="661b1-119">Specify the Business Central list pages that contain the data that you want in the report.</span></span> <span data-ttu-id="661b1-120">Hvis du f. eks. vil oprette en rapport til listen **Salgsfakturaer**, skal du medtage sider, der vedrører salg.</span><span class="sxs-lookup"><span data-stu-id="661b1-120">For example, to create a report for the **Sales Invoices** list, include pages related to sales.</span></span>

    <span data-ttu-id="661b1-121">Du kan finde flere oplysninger ved at følge instruktioner i [Tilføje [!INCLUDE[prod_short](includes/prod_short.md)] som en datakilde i Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).</span><span class="sxs-lookup"><span data-stu-id="661b1-121">For more information, follow the instructions [Add [!INCLUDE[prod_short](includes/prod_short.md)] as a data source in Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).</span></span>

3. <span data-ttu-id="661b1-122">Angive rapportfilteret.</span><span class="sxs-lookup"><span data-stu-id="661b1-122">Set the report filter.</span></span>

    <span data-ttu-id="661b1-123">Sådan foretager du dataopdatering til den valgte post på listen ved at føje et filter til rapporten.</span><span class="sxs-lookup"><span data-stu-id="661b1-123">To make the data update to the selected record in the list, you add a filter to the report.</span></span> <span data-ttu-id="661b1-124">Filteret skal indeholde et felt i den datakilde, der bruges til entydigt at identificere hver post på listen.</span><span class="sxs-lookup"><span data-stu-id="661b1-124">The filter must include a field of the data source that's used to uniquely identify each record in the list.</span></span> <span data-ttu-id="661b1-125">I forhold til udviklere er dette felt den *primære nøgle*.</span><span class="sxs-lookup"><span data-stu-id="661b1-125">In developer terms, this field is the *primary key*.</span></span> <span data-ttu-id="661b1-126">I de fleste tilfælde er primærnøglen for en liste feltet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="661b1-126">In most cases, the primary key for a list is the **No.**</span></span> <span data-ttu-id="661b1-127">.</span><span class="sxs-lookup"><span data-stu-id="661b1-127">field.</span></span>

    <span data-ttu-id="661b1-128">Sådan kan du benytte følgende fremgangsmåde for at angive filteret:</span><span class="sxs-lookup"><span data-stu-id="661b1-128">To set the filter, do the following steps:</span></span>

    1. <span data-ttu-id="661b1-129">I **Filtre** skal du vælge feltet for den primære nøgle på listen over tilgængelige felter.</span><span class="sxs-lookup"><span data-stu-id="661b1-129">In the **Filters**, select the primary key field from the list of available fields.</span></span>
    2. <span data-ttu-id="661b1-130">Træk feltet til ruden **Filter**, og slip den i boksen **Filtrer på alle sider**.</span><span class="sxs-lookup"><span data-stu-id="661b1-130">Drag the field to **Filters** pane and drop it in the **Filters on all pages** box.</span></span>
    3. <span data-ttu-id="661b1-131">Indstil **Filtertype** til **Grundlæggende filtrering**.</span><span class="sxs-lookup"><span data-stu-id="661b1-131">Set the **Filter type** to **Basic filtering**.</span></span> <span data-ttu-id="661b1-132">Det kan ikke være sidefilter, visuelt eller avanceret filter.</span><span class="sxs-lookup"><span data-stu-id="661b1-132">It can't be page, visual, or advanced filter.</span></span>

    ![Indstilling af rapportfilteret for rapporten Salgsfakturaaktivitet](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)
4. <span data-ttu-id="661b1-134">Design rapportlayoutet.</span><span class="sxs-lookup"><span data-stu-id="661b1-134">Design the report layout.</span></span>

    <span data-ttu-id="661b1-135">Opret layoutet ved at trække felter og tilføje visuelle effekter.</span><span class="sxs-lookup"><span data-stu-id="661b1-135">Create the layout by dragging fields and adding visualizations.</span></span> <span data-ttu-id="661b1-136">Du kan finde flere oplysninger i [Arbejde med rapportvisning i Power BI Desktop](/power-bi/create-reports/desktop-report-view) i dokumentationen til Power BI.</span><span class="sxs-lookup"><span data-stu-id="661b1-136">For more information, see, [Work with Report view in Power BI Desktop](/power-bi/create-reports/desktop-report-view) in the Power BI documentation.</span></span>

5. <span data-ttu-id="661b1-137">Se de næste afsnit om at tilpasning af rapporten og brug af flere sider.</span><span class="sxs-lookup"><span data-stu-id="661b1-137">See the next sections about sizing the report and using multiple pages.</span></span>

6. <span data-ttu-id="661b1-138">Gem og navngiv rapporten.</span><span class="sxs-lookup"><span data-stu-id="661b1-138">Save and name the report.</span></span>

    <span data-ttu-id="661b1-139">Giv rapporten et navn, der indeholder navnet på den listeside, der er tilknyttet rapporten, da det er i klienten.</span><span class="sxs-lookup"><span data-stu-id="661b1-139">Give the report a name that contains the name of the list page associated with the report, as it is in the client.</span></span> <span data-ttu-id="661b1-140">Navnet skelner ikke mellem store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="661b1-140">The name isn't case-sensitive though.</span></span> <span data-ttu-id="661b1-141">Antag, at rapporten er til listesiden **Salgsfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="661b1-141">Suppose the report is for the **Sales Invoices** list page.</span></span> <span data-ttu-id="661b1-142">Hvis det er tilfældet, skal du indsætte ordene **Salgsfakturaer** et sted i navnet, f. eks. **Mine salgsfakturaer.pbix** eller **my_Sales Invoices_list.pbix**.</span><span class="sxs-lookup"><span data-stu-id="661b1-142">In this case, include the words **sales invoices** somewhere in the name, like **my sales invoices.pbix** or **my_Sales Invoices_list.pbix**.</span></span>

    <span data-ttu-id="661b1-143">Denne navngivningskonvention er ikke et krav.</span><span class="sxs-lookup"><span data-stu-id="661b1-143">This naming convention isn't a requirement.</span></span> <span data-ttu-id="661b1-144">Det gør imidlertid hurtigere at vælge rapporter i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="661b1-144">However, it makes selecting reports in [!INCLUDE[prod_short](includes/prod_short.md)] quicker.</span></span> <span data-ttu-id="661b1-145">Når siden til valg af rapporter åbnes fra en listeside, tilføres automatisk et filter på basis af navnet på siden.</span><span class="sxs-lookup"><span data-stu-id="661b1-145">When the report selection page opens from a list page, it's automatically applied a filter based on the page name.</span></span> <span data-ttu-id="661b1-146">Filteret har syntaksen: `@*<caption>*` som `@*Sales Invoices*`.</span><span class="sxs-lookup"><span data-stu-id="661b1-146">The filter has the syntax: `@*<caption>*`,  like `@*Sales Invoices*`.</span></span> <span data-ttu-id="661b1-147">Denne filtrering sker for at begrænse de viste rapporter.</span><span class="sxs-lookup"><span data-stu-id="661b1-147">This filtering is done to limit the reports that are displayed.</span></span> <span data-ttu-id="661b1-148">Brugerne kan rydde filteret for at se en komplet liste over tilgængelige rapporter i Power BI.</span><span class="sxs-lookup"><span data-stu-id="661b1-148">Users can clear the filter to get a full list of reports available in Power BI.</span></span>

7. <span data-ttu-id="661b1-149">Udgiv rapporten, når du er færdig.</span><span class="sxs-lookup"><span data-stu-id="661b1-149">When you're done, publish the report as usual.</span></span>

    <span data-ttu-id="661b1-150">Du kan få flere oplysninger [Udgivelse af en rapport](across-how-use-financials-data-source-powerbi.md#publish-reports).</span><span class="sxs-lookup"><span data-stu-id="661b1-150">For more information, see [Publishing a Report](across-how-use-financials-data-source-powerbi.md#publish-reports).</span></span>

8. <span data-ttu-id="661b1-151">Test rapporten.</span><span class="sxs-lookup"><span data-stu-id="661b1-151">Test the report.</span></span>

    <span data-ttu-id="661b1-152">Når rapporten er udgivet til dit arbejdsområde, skal de være tilgængelige fra Power BI-faktaboksen på listesiden i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="661b1-152">Once the report's been published to your workspace, it should be available from the Power BI FactBox on the list page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

    <span data-ttu-id="661b1-153">Benyt følgende fremgangsmåde for at teste den.</span><span class="sxs-lookup"><span data-stu-id="661b1-153">To test it, do the following steps.</span></span>

    1. <span data-ttu-id="661b1-154">Åbn [!INCLUDE[prod_short](includes/prod_short.md)], og gå til listesiden.</span><span class="sxs-lookup"><span data-stu-id="661b1-154">Open [!INCLUDE[prod_short](includes/prod_short.md)] and go to the list page.</span></span>
    2. <span data-ttu-id="661b1-155">Hvis du ikke kan se Power BI-faktaboksen, skal du på handlingslinjen og derefter vælge **Handlinger** > **Vis** > **Vis/skjul Power BI-rapporter**.</span><span class="sxs-lookup"><span data-stu-id="661b1-155">If you don't see the Power BI FactBox, go the action bar, then select **Actions** > **Display** > **Show/Hide Power BI Reports**.</span></span>
    3. <span data-ttu-id="661b1-156">I Power BI-faktaboksen skal du vælge **Vælg rapporter**, markere boksen **Aktivér** for rapporten og derefter klikke på **OK**.</span><span class="sxs-lookup"><span data-stu-id="661b1-156">In the Power BI FactBox, select **Select Reports**, select the **Enable** box for the report, then select **OK**.</span></span>

    <span data-ttu-id="661b1-157">Hvis rapporten er designet korrekt, vises den.</span><span class="sxs-lookup"><span data-stu-id="661b1-157">If designed correctly, the report displays.</span></span>  

## <a name="set-the-report-size-and-color"></a><span data-ttu-id="661b1-158">Angive størrelse og farve for rapporten</span><span class="sxs-lookup"><span data-stu-id="661b1-158">Set the report size and color</span></span>

<span data-ttu-id="661b1-159">Størrelsen på rapporten skal angives til 325 x 310 pixel.</span><span class="sxs-lookup"><span data-stu-id="661b1-159">The size of the report must be set to 325 pixels by 310 pixels.</span></span> <span data-ttu-id="661b1-160">Denne størrelse angiver rapportens korrekte skalering på den ledige plads i Power BI-faktaboksens kontrolelementet i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="661b1-160">This size provides the proper scaling of the report in the available space of the Power BI FactBox control in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="661b1-161">Hvis du vil angive størrelsen på rapporten, skal du placere fokus uden for rapportens layoutområde og derefter vælge malerulleikonet.</span><span class="sxs-lookup"><span data-stu-id="661b1-161">To define the size of the report, place focus outside of the report layout area, and then choose the paint roller icon.</span></span>

![Angive rapportbredde og højde for rapporten Salgsfakturaaktivitet](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

<span data-ttu-id="661b1-163">Du kan ændre bredden og højden for rapporten ved at vælge **Brugerdefineret** i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="661b1-163">You can change the width and height of the report by choosing **Custom** in the **Type** field.</span></span>

<span data-ttu-id="661b1-164">Hvis baggrunden for rapporten skal passe ind i baggrundsfarven for kontrolelementet for Power BI-faktaboksen, skal du angive rapportens baggrundsfarve til *#FFFFFF* (hvid).</span><span class="sxs-lookup"><span data-stu-id="661b1-164">If you want the background of the report to blend with the background color of the Power BI FactBox control, set report background color to *#FFFFFF* (white).</span></span> 

> [!TIP]
> <span data-ttu-id="661b1-165">Brug [!INCLUDE [prod_short](includes/prod_short.md)]-temafilen til at oprette rapporter med samme farveskema som [!INCLUDE [prod_short](includes/prod_short.md)]-apps.</span><span class="sxs-lookup"><span data-stu-id="661b1-165">Use the [!INCLUDE [prod_short](includes/prod_short.md)] theme file to build reports with the same color styling as the [!INCLUDE [prod_short](includes/prod_short.md)] apps.</span></span> <span data-ttu-id="661b1-166">Du kan finde flere oplysninger i [Brug af [!INCLUDE [prod_short](includes/prod_short.md)]-rapporttemaet](across-how-use-financials-data-source-powerbi.md#theme).</span><span class="sxs-lookup"><span data-stu-id="661b1-166">For more information, see [Using the [!INCLUDE [prod_short](includes/prod_short.md)] report theme](across-how-use-financials-data-source-powerbi.md#theme).</span></span>

## <a name="reports-with-multiple-pages"></a><span data-ttu-id="661b1-167">Rapporter med flere sider</span><span class="sxs-lookup"><span data-stu-id="661b1-167">Reports with multiple pages</span></span>

<span data-ttu-id="661b1-168">Med Power BI kan du oprette en enkelt rapport med flere sider.</span><span class="sxs-lookup"><span data-stu-id="661b1-168">With Power BI, you can create a single report with multiple pages.</span></span> <span data-ttu-id="661b1-169">Men i forbindelse med rapporter, der vises med listesider, kan vi ikke anbefale, at de har mere end én side.</span><span class="sxs-lookup"><span data-stu-id="661b1-169">However, for reports that will display with list pages, we recommend that they don't have more than one page.</span></span> <span data-ttu-id="661b1-170">Power BI-faktaboksen viser kun den første side i rapporten.</span><span class="sxs-lookup"><span data-stu-id="661b1-170">The Power BI FactBox will only show the first page of your report.</span></span>

## <a name="fixing-problems"></a><span data-ttu-id="661b1-171">Løsning af problemer</span><span class="sxs-lookup"><span data-stu-id="661b1-171">Fixing problems</span></span>

<span data-ttu-id="661b1-172">Denne sektion forklarer, hvordan du løser problemer, som du kan støde på, når du forsøger at få vist en Power BI-rapport for en listeside i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="661b1-172">This section explains how to fix problems that you might run into when you try to view a Power BI report for a list page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

### <a name="you-cant-see-the-power-bi-factbox-on-a-list-page"></a><span data-ttu-id="661b1-173">Du kan ikke se Power BI-faktaboksen på en listeside</span><span class="sxs-lookup"><span data-stu-id="661b1-173">You can't see the Power BI FactBox on a list page</span></span>

<span data-ttu-id="661b1-174">Power BI-faktaboksen er som standard skjult.</span><span class="sxs-lookup"><span data-stu-id="661b1-174">By default, the Power BI FactBox is hidden from view.</span></span> <span data-ttu-id="661b1-175">Hvis du vil have vist faktaboksen på en side, skal du vælge **Handlinger** > **Vis** > **Vis/skjul Power BI-rapporter** på handlingslinjen.</span><span class="sxs-lookup"><span data-stu-id="661b1-175">To show the FactBox on a page, from the action bar, select **Actions** > **Display** > **Show/Hide Power BI Reports**.</span></span>

### <a name="you-cant-see-the-report-in-the-select-report-pane"></a><span data-ttu-id="661b1-176">Du kan ikke se rapporten i ruden Vælg rapport</span><span class="sxs-lookup"><span data-stu-id="661b1-176">You can't see the report in the Select Report pane</span></span>

<span data-ttu-id="661b1-177">Rapportens navn indeholder ikke navnet på den viste listeside.</span><span class="sxs-lookup"><span data-stu-id="661b1-177">The report's name doesn't contain the name of the list page that's being shown.</span></span> <span data-ttu-id="661b1-178">Ryd filteret for at se en komplet liste over tilgængelige Power BI-rapporter.</span><span class="sxs-lookup"><span data-stu-id="661b1-178">Clear the filter to get a full list of Power BI reports available.</span></span>  

### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a><span data-ttu-id="661b1-179">Rapporten er indlæst, men tom, ikke filtreret eller filtreret forkert</span><span class="sxs-lookup"><span data-stu-id="661b1-179">Report is loaded but blank, not filtered, or filtered incorrectly</span></span>

<span data-ttu-id="661b1-180">Kontrollér, at rapportfilteret indeholder den rette primære nøgle.</span><span class="sxs-lookup"><span data-stu-id="661b1-180">Verify the report filter contains the right primary key.</span></span> <span data-ttu-id="661b1-181">I de fleste tilfælde er dette felt **Nr.**</span><span class="sxs-lookup"><span data-stu-id="661b1-181">In most cases, this field is the **No.**</span></span> <span data-ttu-id="661b1-182">men i tabellen **Finanspost** skal du f.eks. bruge feltet **Løbenr.**</span><span class="sxs-lookup"><span data-stu-id="661b1-182">field, but in the **G/L Entry** table, for example, you must use the **Entry No.** field.</span></span>

### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a><span data-ttu-id="661b1-183">Rapporten indlæses, men viser en side, du ikke forventede</span><span class="sxs-lookup"><span data-stu-id="661b1-183">Report is loaded, but it shows a page you didn't expect</span></span>

<span data-ttu-id="661b1-184">Kontrollér, at den side, du vil have vist, er den første side i rapporten.</span><span class="sxs-lookup"><span data-stu-id="661b1-184">Verify that the page you want displayed is the first page in your report.</span></span>  

### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a><span data-ttu-id="661b1-185">Rapporten vises med en uønsket grå kant, er for lille eller for stor</span><span class="sxs-lookup"><span data-stu-id="661b1-185">Report appears with an unwanted gray boarder, or it's too small or too large</span></span>

<span data-ttu-id="661b1-186">Kontroller, at rapportstørrelse er indstillet til 325 x 310 pixel.</span><span class="sxs-lookup"><span data-stu-id="661b1-186">Verify that the report size is set to 325 pixels x 310 pixels.</span></span> <span data-ttu-id="661b1-187">Gem rapporten, og opdater derefter oversigtssiden.</span><span class="sxs-lookup"><span data-stu-id="661b1-187">Save the report, and then refresh the list page.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="661b1-188">Se relateret oplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="661b1-188">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="661b1-189">Se også</span><span class="sxs-lookup"><span data-stu-id="661b1-189">See Also</span></span>

[<span data-ttu-id="661b1-190">Aktivering af dine virksomhedsdata for Power BI</span><span class="sxs-lookup"><span data-stu-id="661b1-190">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
<span data-ttu-id="661b1-191">[Brug af [!INCLUDE[prod_short](includes/prod_short.md)] som Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="661b1-191">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
[<span data-ttu-id="661b1-192">Blive køreklar</span><span class="sxs-lookup"><span data-stu-id="661b1-192">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
<span data-ttu-id="661b1-193">[Opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="661b1-193">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
[<span data-ttu-id="661b1-194">Finans</span><span class="sxs-lookup"><span data-stu-id="661b1-194">Finance</span></span>](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]