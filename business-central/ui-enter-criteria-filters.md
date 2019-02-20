---
title: "Sortering af, søgning i og filtrering af lister | Microsoft Docs"
description: "Arbejde effektivt på lister ved at søge på tværs af dine data, sorterer kolonner og præcisere resultater ved at bruge effektive filtersymboler og tastaturgenveje."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 5d6d2d9527e81a92987f6b8fcdbe8e087c3c537a
ms.openlocfilehash: c6eb9465d07b702e545347cad5acf0a42f01d1de
ms.contentlocale: da-dk
ms.lasthandoff: 01/22/2019

---
# <a name="sorting-searching-and-filtering-lists"></a><span data-ttu-id="78396-103">Sortering af, søgning i og filtrering af lister</span><span class="sxs-lookup"><span data-stu-id="78396-103">Sorting, Searching, and Filtering Lists</span></span>
<span data-ttu-id="78396-104">Der er et par ting, du kan gøre som en hjælp til at scanne, finde og begrænse poster på en liste.</span><span class="sxs-lookup"><span data-stu-id="78396-104">There are a few things that you can do that will help you scan, find, and limit records in a list.</span></span> <span data-ttu-id="78396-105">Disse omfatter sortering, søgning og filtrering.</span><span class="sxs-lookup"><span data-stu-id="78396-105">These include sorting, searching and filtering.</span></span> <span data-ttu-id="78396-106">Du kan anvende nogle eller alle af disse samtidigt til hurtigt at finde eller analysere dataene.</span><span class="sxs-lookup"><span data-stu-id="78396-106">You can apply some or all of these simultaneously to quickly find or analyze your data.</span></span>

> [!TIP]
> <span data-ttu-id="78396-107">Når du får vist dataene som felter, kan du søge og bruge grundlæggende filtrering.</span><span class="sxs-lookup"><span data-stu-id="78396-107">When viewing your data as tiles, you can search and use basic filtering.</span></span> <span data-ttu-id="78396-108">Når du vil bruge et komplet sæt af effektive funktioner til sortering, søgning eller filtrering, skal du vælge ikonet ![Vis som liste](media/ui_show_as_list_icon.png "Pil til venstre Vis som liste") for at få vist en liste.</span><span class="sxs-lookup"><span data-stu-id="78396-108">To use the full set of powerful features for sorting, searching and filtering, choose the ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to show as a list.</span></span>

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a><span data-ttu-id="78396-109">Sortering</span><span class="sxs-lookup"><span data-stu-id="78396-109">Sorting</span></span>
<span data-ttu-id="78396-110">Sortering gør det nemt og hurtigt for dig at overskue dine oplysninger.</span><span class="sxs-lookup"><span data-stu-id="78396-110">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="78396-111">Hvis du har mange kunder, f.eks. kan du vælge at sortere dem efter **Kundenr.**, **Debitorbogføringsgruppe**, **Valutakode**, **Lande-/områdekode** eller **Momsregistreringsnr.** for at få det nødvendige overblik.</span><span class="sxs-lookup"><span data-stu-id="78396-111">If you have many customers, for example, you can choose to sort them by **Customer No.**, **Customer Posting Group**, **Currency Code**, **Country Region Code**, or **Sales Tax Registration No.** to get the overview you need.</span></span>

<span data-ttu-id="78396-112">Hvis du vil sortere en liste, kan du enten vælge en kolonneoverskriftstekst, hvor du kan skifte mellem stigende og faldende rækkefølge, eller du kan vælge den lille nedadgående pil i kolonneoverskriften og derefter vælge **Stigende** eller **Faldende**.</span><span class="sxs-lookup"><span data-stu-id="78396-112">To sort a list, you can either choose a column heading text to toggle between ascending and descending order, or choose the small down arrow in the column heading, and then choose **Ascending** or **Descending**.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="78396-113">Sortering understøttes ikke af billeder, BLOB-felter, FlowFilters og felter, der ikke tilhører en tabel.</span><span class="sxs-lookup"><span data-stu-id="78396-113">Sorting is not supported on images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching"></a><span data-ttu-id="78396-114">Søgning</span><span class="sxs-lookup"><span data-stu-id="78396-114">Searching</span></span>
<span data-ttu-id="78396-115"><!--## Searching by using the Quick Filter --> Øverst på hver listeside finder du ikonet ![Søg på liste](media/ui-search/search-list.png "Ikonet Søg på liste") **Søg**, der giver en hurtig og nem måde at reducere posterne på en liste og kun vise de poster, der indeholder de data, du er interesseret i at se.</span><span class="sxs-lookup"><span data-stu-id="78396-115"><!--## Searching by using the Quick Filter --> At the top of each list page, there is a ![Search list](media/ui-search/search-list.png "Search list icon") **Search** icon that provides a quick and easy way to reduce the records in a list and display only those records that contain the data that you are interested in seeing.</span></span>

<span data-ttu-id="78396-116">Du søger ved at vælge søgeikonet og derefter skrive den tekst, du leder efter, i feltet.</span><span class="sxs-lookup"><span data-stu-id="78396-116">To search, simply select the search icon, and then in the box, type the text that you are looking for.</span></span> <span data-ttu-id="78396-117">Du kan skrive bogstaver, tal og andre symboler.</span><span class="sxs-lookup"><span data-stu-id="78396-117">You can enter letters, numbers, and other symbols.</span></span>

### <a name="fine-tune-the-search"></a><span data-ttu-id="78396-118">Finjustere søgningen</span><span class="sxs-lookup"><span data-stu-id="78396-118">Fine-tune the search</span></span>
<span data-ttu-id="78396-119">Generelt forsøger søgningen at matche teksten på tværs af alle felter. Den skelner ikke mellem store og små bogstaver og sammenligner tekst, hvor som helst i feltet (ved begyndelsen, slutningen eller i midten).</span><span class="sxs-lookup"><span data-stu-id="78396-119">In general, search will attempt to match text across all fields; it does not distinguish between uppercase and lowercase characters (in other words, case insensitive), and will match text placed anwhere in the field (at the beginning, end, or in the middle).</span></span>

<span data-ttu-id="78396-120">Dog kan du foretage en mere nøjagtig søgning ved hjælp af følgende specialtegn:</span><span class="sxs-lookup"><span data-stu-id="78396-120">However, you can make a more exact search by using the following special characters:</span></span>

- <span data-ttu-id="78396-121">Sæt søgeteksten i enkelte anførselstegn `''` (f.eks. `'man'`) for kun at finde feltværdier, der er identiske med hele teksten, og hvor små og store bogstaver er identiske.</span><span class="sxs-lookup"><span data-stu-id="78396-121">To find only field values that match the entire text and case exactly, place the search text between single quotes `''` (for example, `'man'`).</span></span>

- <span data-ttu-id="78396-122">Sæt `*` efter søgeteksten (f.eks. `man*`) for at finde feltværdier, der begynder med en bestemt tekst, og hvor små og store bogstaver er identiske.</span><span class="sxs-lookup"><span data-stu-id="78396-122">To find field values that start with a certain text and match the case, place `*` after the search text (for example `man*`).</span></span>

- <span data-ttu-id="78396-123">Sæt `*` før søgeteksten (f.eks. `*man`) for at finde feltværdier, der slutter med en bestemt tekst, og hvor små og store bogstaver er identiske.</span><span class="sxs-lookup"><span data-stu-id="78396-123">To find field values that end with a certain text and match the case, place `*` before the search text (for example `*man`).</span></span>

- <span data-ttu-id="78396-124">Når du bruger `''` eller `*`, skelnes der mellem små og store bogstaver i søgningen.</span><span class="sxs-lookup"><span data-stu-id="78396-124">When using  `''` or `*`, the search is case sensitive.</span></span> <span data-ttu-id="78396-125">Hvis du vil have, at der skelnes mellem små og store bogstaver i søgningen, skal du indsætte `@` foran søgeteksten (for eksempel `@man*`).</span><span class="sxs-lookup"><span data-stu-id="78396-125">If you want to make the search case insensitive, place `@` before the search text (for example `@man*`).</span></span>

<span data-ttu-id="78396-126">Følgende tabel indeholder nogle eksempler, der forklarer, hvordan du kan bruge søgningen.</span><span class="sxs-lookup"><span data-stu-id="78396-126">The following table provides some examples to explain how you can use the search.</span></span>


<!--
In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.-->

<!--
The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options. Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.  

* If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.  
* If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.
-->
<!--

|Search Criteria|Interpreted as...|Finds...|
|---------------|----------------|----------|
|`man`<br />or <br />`Man`|Contains the text; case insensitive|All records with fields that contain the text **man**, regardless of the case.|
|`'Man'`|Entire text match; case sensitive.|All records with fields that only contain **Man** exactly.|
|`Man*`|Starts with the text; case sensitive.|All records with fields that start with the text <b>Man</b> exactly.|
|`@Man*`|Starts with the text; case insensitive.|All records with fields that start with **man**, regardless of the case.|
|`@*man`|Ends with the text; case insensitive.|All records that end with **man**, regardless of the case.|
-->

|<span data-ttu-id="78396-127">Søgekriterier</span><span class="sxs-lookup"><span data-stu-id="78396-127">Search Criteria</span></span>|<span data-ttu-id="78396-128">Finder...</span><span class="sxs-lookup"><span data-stu-id="78396-128">Finds...</span></span>|
|---------------|----------|
|`man`<br /><span data-ttu-id="78396-129">eller</span><span class="sxs-lookup"><span data-stu-id="78396-129">or</span></span> <br />`Man`|<span data-ttu-id="78396-130">Alle poster med felter, der indeholder teksten **man**, uanset store eller små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="78396-130">All records with fields that contain the text **man**, regardless of the case.</span></span> <span data-ttu-id="78396-131">F.eks. **Manchester**, **manual** eller **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="78396-131">For example, **Manchester**, **manual**, or **Sportsman**.</span></span> |
|`'Man'`|<span data-ttu-id="78396-132">Alle poster med felter, der kun indeholder **Man**. Samme brug af store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="78396-132">All records with fields that contain only **Man**, matching the case.</span></span>|
|`Man*`|<span data-ttu-id="78396-133">Alle poster med felter, der begynder med teksten <b>Man</b>. Samme brug af store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="78396-133">All records with fields that start with the text <b>Man</b>, matching the case.</span></span> <span data-ttu-id="78396-134">F.eks. **Manchester**, men ikke **manual** eller **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="78396-134">For example, **Manchester** but not **manual** or **Sportsman**.</span></span>|
|`@Man*`|<span data-ttu-id="78396-135">Alle poster med felter, der begynder med teksten **man**, uanset om der bruges store eller små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="78396-135">All records with fields that start with **man**, regardless of the case.</span></span> <span data-ttu-id="78396-136">F.eks. **Manchester** og **manual**, men ikke **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="78396-136">For example, **Manchester** and **manual**, but not **Sportsman**.</span></span>|
|`@*man`|<span data-ttu-id="78396-137">Alle poster der slutter med teksten **man**, uanset om der er brugt store eller små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="78396-137">All records that end with **man**, regardless of the case.</span></span> <span data-ttu-id="78396-138">F.eks. **Sportsman**, men ikke **Manchester** eller **manual**.</span><span class="sxs-lookup"><span data-stu-id="78396-138">For example **Sportsman**, but not **Manchester** or **manual**.</span></span>|

> [!TIP]
> <span data-ttu-id="78396-139">Du kan trykke på F3 for at aktivere og deaktivere søgefeltet.</span><span class="sxs-lookup"><span data-stu-id="78396-139">You can press F3 to activate and deactivate the search box.</span></span> <span data-ttu-id="78396-140">Du kan finde flere oplysninger i [Tastaturgenveje](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="78396-140">For more information see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

## <a name="filtering"></a><span data-ttu-id="78396-141">Filtrering</span><span class="sxs-lookup"><span data-stu-id="78396-141">Filtering</span></span>
<span data-ttu-id="78396-142">Filtrering giver en mere avanceret og fleksibel må de at kontrollere, hvilke poster der vises på en liste.</span><span class="sxs-lookup"><span data-stu-id="78396-142">Filtering provides a more advanced and versatile way of controlling which records display in a list.</span></span> <span data-ttu-id="78396-143">Der er to vigtige forskelle mellem søgning eller filtrering, som beskrevet i nedenstående tabel.</span><span class="sxs-lookup"><span data-stu-id="78396-143">There are two major differences between searching and filtering, as described in the table below.</span></span>

|| <span data-ttu-id="78396-144">**Søgning**</span><span class="sxs-lookup"><span data-stu-id="78396-144">**Searching**</span></span> | <span data-ttu-id="78396-145">**Filtrering**</span><span class="sxs-lookup"><span data-stu-id="78396-145">**Filtering**</span></span> |
|--|----------|------------|
| <span data-ttu-id="78396-146">**Relevante felter**</span><span class="sxs-lookup"><span data-stu-id="78396-146">**Applicable fields**</span></span> | <span data-ttu-id="78396-147">Søger på tværs af alle de felter, der kan ses på siden.</span><span class="sxs-lookup"><span data-stu-id="78396-147">Searches across all fields that are visible on the page.</span></span> | <span data-ttu-id="78396-148">Filtrerer et eller flere felter hver for sig og vælger fra et felt i tabellen, herunder felter, ikke der kan ses på siden.</span><span class="sxs-lookup"><span data-stu-id="78396-148">Filters one or more fields individually, selecting from any field on the table, including fields that are not visible on the page.</span></span> |
| <span data-ttu-id="78396-149">**Matching**</span><span class="sxs-lookup"><span data-stu-id="78396-149">**Matching**</span></span> | <span data-ttu-id="78396-150">Viser poster med felter, der stemmer overens med søgeteksten, uanset store eller små bogstaver eller placeringen af teksten.</span><span class="sxs-lookup"><span data-stu-id="78396-150">Displays records with fields that match the search text, irrespective of casing or placement of that text.</span></span> | <span data-ttu-id="78396-151">Viser poster, hvor feltet nøjagtigt svarer til filteret, og der skelnes mellem små og store bogstaver, medmindre der er angivet særlige filtersymboler.</span><span class="sxs-lookup"><span data-stu-id="78396-151">Displays records where the field matches the filter exactly and is case sensitive, unless special filter symbols are entered.</span></span>

<span data-ttu-id="78396-152">Filtrering giver dig mulighed at få vist poster for bestemte konti eller kunder, datoer, beløb og andre oplysninger ved at angive filterkriterier.</span><span class="sxs-lookup"><span data-stu-id="78396-152">Filtering enables you to display records for specific accounts or customers, dates, amounts, and other information by specifying filter criteria.</span></span> <span data-ttu-id="78396-153">Det er kun poster, der svarer til kriterierne, som vises.</span><span class="sxs-lookup"><span data-stu-id="78396-153">Only records that match the criteria are displayed.</span></span> <span data-ttu-id="78396-154">Hvis du angiver kriterier for flere felter, vises kun poster, der svarer til alle kriterier.</span><span class="sxs-lookup"><span data-stu-id="78396-154">If you specify criteria for multiple fields, then only records that match all criteria will be displayed.</span></span>

### <a name="working-in-the-filter-pane"></a><span data-ttu-id="78396-155">Arbejde i filterruden</span><span class="sxs-lookup"><span data-stu-id="78396-155">Working in the filter pane</span></span>
<span data-ttu-id="78396-156">Filterruden viser de aktuelle filtre på en liste, og gør det muligt at angive dine egne brugerdefinerede filtre i en eller flere felter.</span><span class="sxs-lookup"><span data-stu-id="78396-156">The filter pane displays the current filters for a list, and enables you to set your own custom filters on one or more fields.</span></span> <span data-ttu-id="78396-157">Følgende figur viser et eksempel på filterruden for en liste over salgstilbud.</span><span class="sxs-lookup"><span data-stu-id="78396-157">The following figure shows an example filter pane for a Sales Quotes list.</span></span>

<span data-ttu-id="78396-158">![Oversigt over Filterrude](media/filter-pane-overview.png "Filterikon")</span><span class="sxs-lookup"><span data-stu-id="78396-158">![Filter pane overview ](media/filter-pane-overview.png "Filter icon")</span></span>

<span data-ttu-id="78396-159">Hvis du vil have vist filterruden, skal du bruge tastaturgenvejen **Skift + F3**.</span><span class="sxs-lookup"><span data-stu-id="78396-159">To display the filter pane, use the **Shift+F3** keyboard shortcut.</span></span> <span data-ttu-id="78396-160">Du kan også vælge pil ned tæt på sidetitlen på navigationslinjen over listen for lister i rollecentret, og derefter vælge **Vis Filterrude**.</span><span class="sxs-lookup"><span data-stu-id="78396-160">For lists within the Role Center, you can also choose the down arrow near the page title in the navigation bar above the list, and then choose **Show filter pane**.</span></span>

<span data-ttu-id="78396-161">![Vis Filterrude](media/open-filter-pane.png "Vis Filterrude")</span><span class="sxs-lookup"><span data-stu-id="78396-161">![Show filter pane](media/open-filter-pane.png "Show filter pane")</span></span>

<span data-ttu-id="78396-162">En filterrude er inddelt i tre afsnit: **Visninger**, **Filtrer listen efter** og **Filtrer totaler efter**:</span><span class="sxs-lookup"><span data-stu-id="78396-162">A filter pane is divided in three sections: **Views**, **Filter list by**, and **Filter totals by**:</span></span>

- <span data-ttu-id="78396-163">**Visninger**</span><span class="sxs-lookup"><span data-stu-id="78396-163">**Views**</span></span>

  <span data-ttu-id="78396-164">Nogle lister indeholder sektionen **Visninger**.</span><span class="sxs-lookup"><span data-stu-id="78396-164">Some lists will include the **Views** section.</span></span> <span data-ttu-id="78396-165">Visninger er variationer af listen, der er forudkonfigureret med filtre.</span><span class="sxs-lookup"><span data-stu-id="78396-165">Views are variations of the list that have been preconfigured with filters.</span></span> <span data-ttu-id="78396-166">For at skifte til en anden visning af listen skal du blot vælge et andet link.</span><span class="sxs-lookup"><span data-stu-id="78396-166">To switch to a different view of your list, simply select another link.</span></span> <span data-ttu-id="78396-167">Du kan midlertidigt ændre filtrene i en visning, men ændringerne gemmes ikke permanent.</span><span class="sxs-lookup"><span data-stu-id="78396-167">You can temporarily change the filters on a view, but the changes will not be permanently saved.</span></span>

- <span data-ttu-id="78396-168">**Filtrer listen efter**</span><span class="sxs-lookup"><span data-stu-id="78396-168">**Filter list by**</span></span>

  <span data-ttu-id="78396-169">Sektionen **Filtrer listen efter** er der, hvor du tilføjer filtre i bestemte felter for at reducere antallet af viste poster.</span><span class="sxs-lookup"><span data-stu-id="78396-169">The **Filter list by** section is where you add filters on specific fields to reduce the number of displayed records.</span></span> <span data-ttu-id="78396-170">Du kan tilføje et filter ved at vælge **+ Filter**, markere det felt, du vil filtrere fra et felt i tabellen, og derefter angive filterkriterierne i feltet.</span><span class="sxs-lookup"><span data-stu-id="78396-170">To add a filter, select **+ Filter**, select the field that you want to filter from any field in the table, and then enter filter criteria in the box.</span></span>

- <span data-ttu-id="78396-171">**Filtrer totaler efter**</span><span class="sxs-lookup"><span data-stu-id="78396-171">**Filter totals by**</span></span>

  <span data-ttu-id="78396-172">Nogle lister, der viser beregnede felter, som beløb og antal, indeholder sektionen **Filtrer totaler efter**, hvor du kan justere forskellige dimensioner, der påvirker beregninger.</span><span class="sxs-lookup"><span data-stu-id="78396-172">Some lists that display calculated fields, such as amounts and quantities, will include the **Filter totals by** section where you can adjust various dimensions that influence calculations.</span></span> <span data-ttu-id="78396-173">F.eks. kan du hurtigt analysere din kontoplan ved at filtrere beløb til en bestemt periode, eller du kan få vist de samlede beløb for f.eks. salgsordrer fra et bestemt lagersted.</span><span class="sxs-lookup"><span data-stu-id="78396-173">For example, you can quickly analyze your chart of accounts by filtering amounts to a specific period, or you can view the totals for sales orders only from a specific warehouse.</span></span>

  <span data-ttu-id="78396-174">Du kan tilføje et filter ved at vælge **+ Filter**, vælge en af de foruddefinerede dimensioner og derefter tilføje filterkriterierne i feltet.</span><span class="sxs-lookup"><span data-stu-id="78396-174">To add a filter, select **+ Filter**, select one of the predefined dimensions, and then add the filter criteria in the box.</span></span>

  > [!NOTE]
  > <span data-ttu-id="78396-175">Filtre i sektionen **Filtrer totaler efter** styres af FlowFilters i sideopsætningen.</span><span class="sxs-lookup"><span data-stu-id="78396-175">Filters in the **Filter totals by** section are controlled by FlowFilters on the page design.</span></span> <span data-ttu-id="78396-176">Du kan finde tekniske oplysninger i [FlowFilters](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span><span class="sxs-lookup"><span data-stu-id="78396-176">For technical information, see [FlowFilters](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span></span>


### <a name="entering-filter-criteria-in-the-filter-pane"></a><span data-ttu-id="78396-177">Angivelse af filterkriterier i filterruden</span><span class="sxs-lookup"><span data-stu-id="78396-177">Entering filter criteria in the filter pane</span></span>
<span data-ttu-id="78396-178">Når du vil vælge et felt, du vil filtrere, skal du gøre et af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="78396-178">To select a field to filter, do one of the following:</span></span>
  - <span data-ttu-id="78396-179">Vælg **+ Felt** i filterruden.</span><span class="sxs-lookup"><span data-stu-id="78396-179">In the filter pane, choose **+ Field**.</span></span> <span data-ttu-id="78396-180">Skriv navnet på det felt, du vil filtrere, eller vælg et felt i den menu, der viser alle felter i tabellen.</span><span class="sxs-lookup"><span data-stu-id="78396-180">Type the name of the field you wish to filter, or pick a field from the menu that displays all fields in the table.</span></span>

  - <span data-ttu-id="78396-181">Vælg rullepilen i en kolonneoverskrift, og vælg derefter **Filter...**. Derved åbnes filterruden, og kolonnen føjes til filterruden.</span><span class="sxs-lookup"><span data-stu-id="78396-181">In a column heading, choose the down arrow, and then choose **Filter...**. This will open the filter pane and add the column to the filter pane.</span></span>

<span data-ttu-id="78396-182">Du kan nu skrive eller vælge filterkriterierne i feltet.</span><span class="sxs-lookup"><span data-stu-id="78396-182">You can now type or select your filter criteria in the box.</span></span> <span data-ttu-id="78396-183">Den typen felt, du filtrerer bestemmer, hvilke kriterier du kan angive.</span><span class="sxs-lookup"><span data-stu-id="78396-183">The type of field you filter determines which criteria you can enter.</span></span> <span data-ttu-id="78396-184">For eksempel kan du, når du filtrerer et felt, der har faste værdier, kun vælge mellem disse værdier.</span><span class="sxs-lookup"><span data-stu-id="78396-184">For example, filtering a field that has fixed values will only let you choose from those values.</span></span> <span data-ttu-id="78396-185">Du kan finde yderligere oplysninger om særlige filtersymboler i [Filterkriterier](#FilterCriteria) og [Filtertokens](#FilterTokens).</span><span class="sxs-lookup"><span data-stu-id="78396-185">For more information about special filter symbols, see [Filter criteria](#FilterCriteria) and [Filter tokens](#FilterTokens).</span></span>

<span data-ttu-id="78396-186">Kolonner, som allerede indeholder filtre, er angivet med ![Filterikonet](media/ui-search/filter-icon.png "Filterikonet") i kolonneoverskriften.</span><span class="sxs-lookup"><span data-stu-id="78396-186">Columns that already have filters are indicated by the ![Filter icon](media/ui-search/filter-icon.png "Filter icon") in the column heading.</span></span> <span data-ttu-id="78396-187">Hvis du vil fjerne et filter, skal du markere kolonneoverskriften og derefter vælge **Ryd filter**.</span><span class="sxs-lookup"><span data-stu-id="78396-187">To remove a filter, select the column heading, then choose **Clear Filter**.</span></span>


### <a name="entering-filter-criteria-without-the-filter-pane"></a><span data-ttu-id="78396-188">Angivelse af filterkriterier uden filterruden</span><span class="sxs-lookup"><span data-stu-id="78396-188">Entering filter criteria without the filter pane</span></span>
<span data-ttu-id="78396-189">Du kan angive simple filtre direkte på listen uden at skulle bruge filterruden.</span><span class="sxs-lookup"><span data-stu-id="78396-189">You can specify simple filters directly within the list without having to use the filter pane.</span></span>
<span data-ttu-id="78396-190">Med et eller flere felter markere i en række skal du bruge tastaturgenvejen **Alt + F3** til at få vist kun de poster, der har den samme værdi.</span><span class="sxs-lookup"><span data-stu-id="78396-190">With any field selected on a row, use the **Alt+F3** keyboard shortcut to display only the records having that same value.</span></span> <span data-ttu-id="78396-191">Du kan derefter vælge et andet felt og bruge den samme genvej igen for at fortsatte med at præcisere filtrene.</span><span class="sxs-lookup"><span data-stu-id="78396-191">You can then select another field and use the same shortcut again to continue refining your filters.</span></span> <span data-ttu-id="78396-192">Hvis det valgte felt allerede er filtreret, kan du bruge **Alt + F3** til at fjerne filteret.</span><span class="sxs-lookup"><span data-stu-id="78396-192">If the selected field is already filtered, using **Alt+F3** will clear that filter.</span></span>

> [!TIP]
> <span data-ttu-id="78396-193">Fremskynd søgning efter og analyse af dine data ved hjælp af kombinationer af genvejstaster.</span><span class="sxs-lookup"><span data-stu-id="78396-193">Accelerate finding and analyzing your data by using combinations of keyboard shortcuts.</span></span> <span data-ttu-id="78396-194">For f.eks. at markere et felt skal du bruge **Skift + Alt + F3** for at føje dette felt til filterruden, angive filterkriterierne, bruge **Ctrl + Enter** for at vende tilbage til rækkerne, vælge et andet felt og bruge **Alt + F3** til at filtrere til værdien.</span><span class="sxs-lookup"><span data-stu-id="78396-194">For example, select a field, use **Shift+Alt+F3** to add that field to the filter pane, type the filter criteria, use **Ctrl+Enter** to return to the rows, select another field, and use **Alt+F3** to filter to that value.</span></span>
<span data-ttu-id="78396-195">Du kan finde flere oplysninger i [Tastaturgenveje](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="78396-195">For more information see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>


## <span data-ttu-id="78396-196"><a name="FilterCriteria"> </a>Filterkriterier og -symboler</span><span class="sxs-lookup"><span data-stu-id="78396-196"><a name="FilterCriteria"> </a>Filter criteria and symbols</span></span>
<span data-ttu-id="78396-197">Når du angiver kriterier, kan du bruge alle de tal og bogstaver, som du plejer at bruger i feltet.</span><span class="sxs-lookup"><span data-stu-id="78396-197">When you enter criteria, you can use all the numbers and letters that you can normally use in the field.</span></span> <span data-ttu-id="78396-198">Derudover kan du bruge nogle specialtegn til at filtrere resultaterne yderligere.</span><span class="sxs-lookup"><span data-stu-id="78396-198">In addition, you can use special symbols to further filter the results.</span></span> <span data-ttu-id="78396-199">Følgende tabeller viser de tegn, der kan bruges i filtre.</span><span class="sxs-lookup"><span data-stu-id="78396-199">The following tables show the symbols which can be used in filters.</span></span> <span data-ttu-id="78396-200">Ved datoer og klokkeslæt kan du også se [Arbejde med kalenderdatoer og klokkeslæt](ui-enter-date-ranges.md) for at få flere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="78396-200">For dates and times, you can also refer to [Working with Calendar Dates and Times](ui-enter-date-ranges.md) for more detailed information.</span></span>

> [!IMPORTANT]  
>  <span data-ttu-id="78396-201">Der kan være tilfælde, hvor feltværdierne indeholder disse symboler, og du vil filtrere efter dem.</span><span class="sxs-lookup"><span data-stu-id="78396-201">There may be instances where field values contain these symbols and you want to filter on them.</span></span> <span data-ttu-id="78396-202">Hvis du vil gøre dette, skal du medtage det filterudtryk, der indeholder symbolet i anførselstegn (").</span><span class="sxs-lookup"><span data-stu-id="78396-202">To do this, you must include the filter expression that contains the symbol in quotation marks ('').</span></span> <span data-ttu-id="78396-203">Hvis du f.eks. vil filtrere efter poster, der starter med teksten *S&R*, er filterudtrykket `'S&R*'`.</span><span class="sxs-lookup"><span data-stu-id="78396-203">For example, if you want to filter on records that start with the text *S&R*, the filter expression is `'S&R*'`.</span></span>  

### <a name="-interval"></a><span data-ttu-id="78396-204">(..) Interval</span><span class="sxs-lookup"><span data-stu-id="78396-204">(..) Interval</span></span>

|<span data-ttu-id="78396-205">Eksempel</span><span class="sxs-lookup"><span data-stu-id="78396-205">Sample Expression</span></span>|<span data-ttu-id="78396-206">Viste poster</span><span class="sxs-lookup"><span data-stu-id="78396-206">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1100..2100`|<span data-ttu-id="78396-207">Tal fra 1100 til og med 2100.</span><span class="sxs-lookup"><span data-stu-id="78396-207">Numbers 1100 through 2100</span></span>|  
|`..2500`|<span data-ttu-id="78396-208">Konti til og med 2500</span><span class="sxs-lookup"><span data-stu-id="78396-208">Up to and including 2500</span></span>|  
|`..12 31 00`|<span data-ttu-id="78396-209">Datoer til og med 31-12-00.</span><span class="sxs-lookup"><span data-stu-id="78396-209">Dates up to and including 12 31 00</span></span>|  
|`P8..`|<span data-ttu-id="78396-210">Oplysninger for regnskabsperiode 8 og frem</span><span class="sxs-lookup"><span data-stu-id="78396-210">Information for accounting period 8 and thereafter</span></span>|  
|`..23`|<span data-ttu-id="78396-211">Fra begyndelsesdatoen til 23-aktuel måned-aktuelt år 23.59.59</span><span class="sxs-lookup"><span data-stu-id="78396-211">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|`23..`|<span data-ttu-id="78396-212">Fra 23-aktuel måned-aktuelt år 0.00.00 til sluttidspunktet</span><span class="sxs-lookup"><span data-stu-id="78396-212">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|`22..23`|<span data-ttu-id="78396-213">Fra den 23-aktuel måned-aktuelt år 0.00.00 til 22-aktuel måned-aktuelt år 22.59.59</span><span class="sxs-lookup"><span data-stu-id="78396-213">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  

### <a name="124-eitheror"></a><span data-ttu-id="78396-214">(&#124;) Enten/eller</span><span class="sxs-lookup"><span data-stu-id="78396-214">(&#124;) Either/or</span></span>  

|<span data-ttu-id="78396-215">Eksempel</span><span class="sxs-lookup"><span data-stu-id="78396-215">Sample Expression</span></span>|<span data-ttu-id="78396-216">Viste poster</span><span class="sxs-lookup"><span data-stu-id="78396-216">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="78396-217">\`1200</span><span class="sxs-lookup"><span data-stu-id="78396-217">\`1200</span></span>|<span data-ttu-id="78396-218">1300\`</span><span class="sxs-lookup"><span data-stu-id="78396-218">1300\`</span></span>|<span data-ttu-id="78396-219">Tal med 1200 eller 1300.</span><span class="sxs-lookup"><span data-stu-id="78396-219">Numbers with 1200 or 1300</span></span>|  

### <a name="-not-equal-to"></a><span data-ttu-id="78396-220">(<>) Ikke lig med</span><span class="sxs-lookup"><span data-stu-id="78396-220">(<>) Not equal to</span></span>  

|<span data-ttu-id="78396-221">Eksempel</span><span class="sxs-lookup"><span data-stu-id="78396-221">Sample Expression</span></span>|<span data-ttu-id="78396-222">Viste poster</span><span class="sxs-lookup"><span data-stu-id="78396-222">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<>0`|<span data-ttu-id="78396-223">Alle tal undtagen 0</span><span class="sxs-lookup"><span data-stu-id="78396-223">All numbers except 0</span></span><br /><br /> <span data-ttu-id="78396-224">I SQL Server Option kan du kombinere dette symbol med et udtryk med jokertegn.</span><span class="sxs-lookup"><span data-stu-id="78396-224">The SQL Server Option allows you to combine this symbol with a wild card expression.</span></span> <span data-ttu-id="78396-225"><>A\* betyder f.eks. ikke lig med tekst, der starter med A.</span><span class="sxs-lookup"><span data-stu-id="78396-225">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  

### <a name="-greater-than"></a><span data-ttu-id="78396-226">(>) Større end</span><span class="sxs-lookup"><span data-stu-id="78396-226">(>) Greater than</span></span>  

|<span data-ttu-id="78396-227">Eksempel</span><span class="sxs-lookup"><span data-stu-id="78396-227">Sample Expression</span></span>|<span data-ttu-id="78396-228">Viste poster</span><span class="sxs-lookup"><span data-stu-id="78396-228">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>1200`|<span data-ttu-id="78396-229">Tal større end 1200</span><span class="sxs-lookup"><span data-stu-id="78396-229">Numbers greater than 1200</span></span>|  

### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="78396-230">(>=) Større end eller lig med</span><span class="sxs-lookup"><span data-stu-id="78396-230">(>=) Greater than or equal to</span></span>  

|<span data-ttu-id="78396-231">Eksempel</span><span class="sxs-lookup"><span data-stu-id="78396-231">Sample Expression</span></span>|<span data-ttu-id="78396-232">Viste poster</span><span class="sxs-lookup"><span data-stu-id="78396-232">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>=1200`|<span data-ttu-id="78396-233">Tal lig med eller større end 1200</span><span class="sxs-lookup"><span data-stu-id="78396-233">Numbers greater than or equal to 1200</span></span>|  

### <a name="-less-than"></a><span data-ttu-id="78396-234">(<) Mindre end</span><span class="sxs-lookup"><span data-stu-id="78396-234">(<) Less than</span></span>  

|<span data-ttu-id="78396-235">Eksempel</span><span class="sxs-lookup"><span data-stu-id="78396-235">Sample Expression</span></span>|<span data-ttu-id="78396-236">Viste poster</span><span class="sxs-lookup"><span data-stu-id="78396-236">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<1200`|<span data-ttu-id="78396-237">Tal mindre end 1200</span><span class="sxs-lookup"><span data-stu-id="78396-237">Numbers less than 1200</span></span>|  

### <a name="-less-than-or-equal-to"></a><span data-ttu-id="78396-238">(<=) Mindre end eller lig med</span><span class="sxs-lookup"><span data-stu-id="78396-238">(<=) Less than or equal to</span></span>  

|<span data-ttu-id="78396-239">Eksempel</span><span class="sxs-lookup"><span data-stu-id="78396-239">Sample Expression</span></span>|<span data-ttu-id="78396-240">Viste poster</span><span class="sxs-lookup"><span data-stu-id="78396-240">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<=1200`|<span data-ttu-id="78396-241">Tal lig med eller mindre end 1200</span><span class="sxs-lookup"><span data-stu-id="78396-241">Numbers less than or equal to 1200</span></span>|  

### <a name="-and"></a><span data-ttu-id="78396-242">(&) Og</span><span class="sxs-lookup"><span data-stu-id="78396-242">(&) And</span></span>  

|<span data-ttu-id="78396-243">Eksempel</span><span class="sxs-lookup"><span data-stu-id="78396-243">Sample Expression</span></span>|<span data-ttu-id="78396-244">Viste poster</span><span class="sxs-lookup"><span data-stu-id="78396-244">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>200&<1200`|<span data-ttu-id="78396-245">Tal større end 200 og mindre end 1200</span><span class="sxs-lookup"><span data-stu-id="78396-245">Numbers greater than 200 and less than 1200</span></span>|  

### <a name="-an-exact-character-match"></a><span data-ttu-id="78396-246">('') Tegn, der stemmer nøjagtigt overens</span><span class="sxs-lookup"><span data-stu-id="78396-246">('') An exact character match</span></span>  

|<span data-ttu-id="78396-247">Eksempel</span><span class="sxs-lookup"><span data-stu-id="78396-247">Sample Expression</span></span>|<span data-ttu-id="78396-248">Viste poster</span><span class="sxs-lookup"><span data-stu-id="78396-248">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`'man'`|<span data-ttu-id="78396-249">Tekst, der svarer nøjagtigt til man, og der skelnes mellem store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="78396-249">Text that matches man exactly and is case sensitive.</span></span>|  

### <a name="-case-insensitive"></a><span data-ttu-id="78396-250">(@) Ingen forskel på store og små bogstaver</span><span class="sxs-lookup"><span data-stu-id="78396-250">(@) Case insensitive</span></span>  

|<span data-ttu-id="78396-251">Eksempel</span><span class="sxs-lookup"><span data-stu-id="78396-251">Sample Expression</span></span>|<span data-ttu-id="78396-252">Viste poster</span><span class="sxs-lookup"><span data-stu-id="78396-252">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`@man*`|<span data-ttu-id="78396-253">Tekst, der starter med man, og der skelnes mellem store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="78396-253">Text that starts with man and is case insensitive.</span></span>|  

### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="78396-254">(\*) Mange ukendte tegn</span><span class="sxs-lookup"><span data-stu-id="78396-254">(\*) An indefinite number of unknown characters</span></span>

|<span data-ttu-id="78396-255">Eksempel</span><span class="sxs-lookup"><span data-stu-id="78396-255">Sample Expression</span></span>|<span data-ttu-id="78396-256">Viste poster</span><span class="sxs-lookup"><span data-stu-id="78396-256">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`*Co*`|<span data-ttu-id="78396-257">Tekst, der indeholder "A/S", og der skelnes mellem store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="78396-257">Text that contains "Co" and is case sensitive.</span></span>|  
|`*Co`|<span data-ttu-id="78396-258">Tekst, der ender på "A/S", og der skelnes mellem store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="78396-258">Text that ends with "Co" and is case sensitive.</span></span>|  
|`Co*`|<span data-ttu-id="78396-259">Tekst, der begynder med "A/S", og der skelnes mellem store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="78396-259">Text that begins with "Co" and is case sensitive.</span></span>|  

> [!NOTE]  
>   <span data-ttu-id="78396-260">Du kan ikke bruge en `*`, når du filtrerer i indstillingsfelter (optælling), f.eks. feltet **Status** i salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="78396-260">You cannot use `*` when filtering on option (enumeration) fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="78396-261">Hvis du vil angive et filter for denne type felt, kan du angive den numeriske værdi som en filterparameter.</span><span class="sxs-lookup"><span data-stu-id="78396-261">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="78396-262">I feltet **Status** på en salgsordre med værdierne **Åben**, **Frigivet**, **Afventer godkendelse** og **Afventer forudbetaling** kan du f.eks. bruge værdierne `0`, `1`, `2` og `3` til at filtrere efter disse indstillinger.</span><span class="sxs-lookup"><span data-stu-id="78396-262">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values `0`, `1`, `2`, and `3` to filter for these options.</span></span>

### <a name="-one-unknown-character"></a><span data-ttu-id="78396-263">(?) Ét ukendt tegn</span><span class="sxs-lookup"><span data-stu-id="78396-263">(?) One unknown character</span></span>  

|<span data-ttu-id="78396-264">Eksempel</span><span class="sxs-lookup"><span data-stu-id="78396-264">Sample Expression</span></span>|<span data-ttu-id="78396-265">Viste poster</span><span class="sxs-lookup"><span data-stu-id="78396-265">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`Hans?n`|<span data-ttu-id="78396-266">Tekst som f.eks. Hansen eller Hanson</span><span class="sxs-lookup"><span data-stu-id="78396-266">Text such as Hansen or Hanson</span></span>|  

### <a name="combined-format-expressions"></a><span data-ttu-id="78396-267">Kombinerede formatudtryk</span><span class="sxs-lookup"><span data-stu-id="78396-267">Combined format expressions</span></span>  

|<span data-ttu-id="78396-268">Eksempel</span><span class="sxs-lookup"><span data-stu-id="78396-268">Sample Expression</span></span>|<span data-ttu-id="78396-269">Viste poster</span><span class="sxs-lookup"><span data-stu-id="78396-269">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="78396-270">\`5999</span><span class="sxs-lookup"><span data-stu-id="78396-270">\`5999</span></span>|<span data-ttu-id="78396-271">8100..8490\`</span><span class="sxs-lookup"><span data-stu-id="78396-271">8100..8490\`</span></span>|<span data-ttu-id="78396-272">Tallet 5999 og tallene fra og med 8100 til og med 8490.</span><span class="sxs-lookup"><span data-stu-id="78396-272">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|<span data-ttu-id="78396-273">\`..1299</span><span class="sxs-lookup"><span data-stu-id="78396-273">\`..1299</span></span>|<span data-ttu-id="78396-274">1400..\`</span><span class="sxs-lookup"><span data-stu-id="78396-274">1400..\`</span></span>|<span data-ttu-id="78396-275">Medtag poster med et tal mindre end eller lig med 1299, eller tal lig med 1400 eller derover (alle tal undtagen 1300 til og med 1399).</span><span class="sxs-lookup"><span data-stu-id="78396-275">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|`>50&<100`|<span data-ttu-id="78396-276">Medtag poster med tal større end 50 og mindre end 100 (tal fra 51 til og med 99).</span><span class="sxs-lookup"><span data-stu-id="78396-276">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  


## <span data-ttu-id="78396-277"><a name="FilterTokens"> </a>Filtertokens</span><span class="sxs-lookup"><span data-stu-id="78396-277"><a name="FilterTokens"> </a>Filter tokens</span></span>
<span data-ttu-id="78396-278">Når du angiver filterkriterier, kan du også skrive ord, der har en særlig betydning, kaldet filtertokens.</span><span class="sxs-lookup"><span data-stu-id="78396-278">When entering filter criteria, you can also type words that have special meaning, called filter tokens.</span></span> <span data-ttu-id="78396-279">Når du har angivet et tokenordet, erstattes ordet af den eller de værdier, det repræsenterer.</span><span class="sxs-lookup"><span data-stu-id="78396-279">After entering the token word, the word is replaced by the value or values that it represents.</span></span> <span data-ttu-id="78396-280">Det gør filtrering nemmere ved at reducere behovet for at navigere til andre sider for at søge efter værdier, du vil føje til filteret.</span><span class="sxs-lookup"><span data-stu-id="78396-280">This makes filtering easier by reducing the need to navigate to other pages to look up values you want to add to your filter.</span></span> <span data-ttu-id="78396-281">Tabellerne nedenfor beskriver nogle af de tegn, du kan skrive som filterkriterier.</span><span class="sxs-lookup"><span data-stu-id="78396-281">The tables below describe some of the tokens you can type as filter criteria.</span></span>

> [!TIP]
> <span data-ttu-id="78396-282">Din organisation bruger muligvis brugerdefinerede tokens.</span><span class="sxs-lookup"><span data-stu-id="78396-282">Your organization may use custom tokens.</span></span> <span data-ttu-id="78396-283">For at få mere at vide om det komplette sæt tokens, der er tilgængelige for dig, eller tilføje flere brugerdefinerede tokens, skal du kontakte din administrator.</span><span class="sxs-lookup"><span data-stu-id="78396-283">To learn about the complete set of tokens available to you or to add more custom tokens, talk to your administrator.</span></span> <span data-ttu-id="78396-284">Du kan finde tekniske oplysninger i [Tilføje filtertokens](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens)</span><span class="sxs-lookup"><span data-stu-id="78396-284">For technical information see [Adding Filter Tokens](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens)</span></span>


### <a name="me-or-userid-records-assigned-to-you"></a><span data-ttu-id="78396-285">(%me or %userid) Poster, der er tildelt til dig</span><span class="sxs-lookup"><span data-stu-id="78396-285">(%me or %userid) Records assigned to you</span></span>

<span data-ttu-id="78396-286">Brug `%me` eller `%userid` ved filtrering af felter, der indeholder bruger-id'et, f.eks. feltet **Tildelt til bruger-id**, for at få vist alle poster, der er tildelt til dig.</span><span class="sxs-lookup"><span data-stu-id="78396-286">Use `%me` or `%userid` when filtering fields that contain the user ID, such as **Assigned to User ID** field, to display all records that are assigned to you.</span></span>

|<span data-ttu-id="78396-287">Eksempel</span><span class="sxs-lookup"><span data-stu-id="78396-287">Sample Expression</span></span>|<span data-ttu-id="78396-288">Viste poster</span><span class="sxs-lookup"><span data-stu-id="78396-288">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%me`<br /><span data-ttu-id="78396-289">eller</span><span class="sxs-lookup"><span data-stu-id="78396-289">or</span></span><br />`%userid`|<span data-ttu-id="78396-290">Poster, der er knyttet til din brugerkonto.</span><span class="sxs-lookup"><span data-stu-id="78396-290">Records that are assigned to your user account.</span></span> |  

### <a name="mycustomers-customers-in-my-customers"></a><span data-ttu-id="78396-291">(%mycustomers) Debitorer i Mine debitorer</span><span class="sxs-lookup"><span data-stu-id="78396-291">(%mycustomers) Customers in My Customers</span></span>

<span data-ttu-id="78396-292">Brug `%mycustomers` i debitorfeltet **Nej** til at vise alle poster for debitorer, der står på listen **Mine debitorer** i dit rollecenter.</span><span class="sxs-lookup"><span data-stu-id="78396-292">Use `%mycustomers` in the customer **No** field to display all records for customers that are included in the **My Customers** list on your Role Center.</span></span>

|<span data-ttu-id="78396-293">Eksempel</span><span class="sxs-lookup"><span data-stu-id="78396-293">Sample Expression</span></span>|<span data-ttu-id="78396-294">Viste poster</span><span class="sxs-lookup"><span data-stu-id="78396-294">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%mycustomers`|<span data-ttu-id="78396-295">Debitorer i **Mine debitorer** i dit rollecenter.</span><span class="sxs-lookup"><span data-stu-id="78396-295">Customers in the **My Customers** on your Role Center.</span></span> |  

### <a name="myitems-items-in-my-items"></a><span data-ttu-id="78396-296">(%myitems) Varer i Mine varer</span><span class="sxs-lookup"><span data-stu-id="78396-296">(%myitems) Items in My Items</span></span>

<span data-ttu-id="78396-297">Brug `%myitems` i varefeltet **Nej** til at vise alle poster for varer, der står på listen **Mine varer** i dit rollecenter.</span><span class="sxs-lookup"><span data-stu-id="78396-297">Use `%myitems` in the item **No** field to display all records for items that are included in the **My Items** list on your Role Center.</span></span>

|<span data-ttu-id="78396-298">Eksempel</span><span class="sxs-lookup"><span data-stu-id="78396-298">Sample Expression</span></span>|<span data-ttu-id="78396-299">Viste poster</span><span class="sxs-lookup"><span data-stu-id="78396-299">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myitems`|<span data-ttu-id="78396-300">Varer i **Mine varer** i dit rollecenter.</span><span class="sxs-lookup"><span data-stu-id="78396-300">Items in the **My Items** on your Role Center.</span></span> |  

### <a name="myvendors-vendors-in-my-vendors"></a><span data-ttu-id="78396-301">(%myvendors) Kreditorer i Mine kreditorer</span><span class="sxs-lookup"><span data-stu-id="78396-301">(%myvendors) Vendors in My Vendors</span></span>

<span data-ttu-id="78396-302">Brug `%myvendors` i kreditorfeltet **Nej** til at vise alle poster for kreditorer, der står på listen **Mine kreditor** i dit rollecenter.</span><span class="sxs-lookup"><span data-stu-id="78396-302">Use `%myvendors` in the vendor **No** field to display all records for vendors that are included in the **My Vendors** list on your Role Center.</span></span>

|<span data-ttu-id="78396-303">Eksempel</span><span class="sxs-lookup"><span data-stu-id="78396-303">Sample Expression</span></span>|<span data-ttu-id="78396-304">Viste poster</span><span class="sxs-lookup"><span data-stu-id="78396-304">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myvendors`|<span data-ttu-id="78396-305">Kreditorer i **Mine kreditorer** i dit rollecenter.</span><span class="sxs-lookup"><span data-stu-id="78396-305">Vendors in the **My Vendors** on your Role Center.</span></span> |  


## <a name="see-also"></a><span data-ttu-id="78396-306">Se også</span><span class="sxs-lookup"><span data-stu-id="78396-306">See Also</span></span>
<span data-ttu-id="78396-307">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="78396-307">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="78396-308">Almindelige spørgsmål om søgning og filtrering</span><span class="sxs-lookup"><span data-stu-id="78396-308">Common questions about Searching and Filtering</span></span>](ui-search-filter-faq.md)

