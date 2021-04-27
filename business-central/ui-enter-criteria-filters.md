---
title: Sortering af, søgning i og filtrering af lister | Microsoft Docs
description: Arbejd effektivt på lister ved at søge på tværs af dine data, sorterer kolonner og præcisere resultater ved at bruge effektive filtersymboler og tastaturgenveje.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: a3d42fccebafdfa80346f04b43a0e3dd29f467d8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5770634"
---
# <a name="sorting-searching-and-filtering"></a><span data-ttu-id="fdc23-103">Sortering, søgning og filtrering</span><span class="sxs-lookup"><span data-stu-id="fdc23-103">Sorting, Searching, and Filtering</span></span>

<span data-ttu-id="fdc23-104">Der er et par ting, du kan gøre som en hjælp til at scanne, finde og begrænse poster på en liste eller i en rapport eller XMLport.</span><span class="sxs-lookup"><span data-stu-id="fdc23-104">There are a few things that you can do that will help you scan, find, and limit records on a list or in a report or XMLport.</span></span> <span data-ttu-id="fdc23-105">Disse omfatter sortering, søgning og filtrering.</span><span class="sxs-lookup"><span data-stu-id="fdc23-105">These include sorting, searching, and filtering.</span></span> <span data-ttu-id="fdc23-106">Du kan anvende nogle eller alle af disse samtidigt til hurtigt at finde eller analysere dataene.</span><span class="sxs-lookup"><span data-stu-id="fdc23-106">You can apply some or all of these simultaneously to quickly find or analyze your data.</span></span>

<span data-ttu-id="fdc23-107">I forbindelse med rapporter og XMLporte kan du angive filtre for at afgrænse, hvilke data der skal medtages i rapporten eller XMLport, men du kan ikke sortere og søge.</span><span class="sxs-lookup"><span data-stu-id="fdc23-107">For reports and XMLports, as on lists, you can set filters to delimit which data to include in the report or XMLport, but you can't sort and search.</span></span>

> [!TIP]
> <span data-ttu-id="fdc23-108">Når du får vist dataene som felter, kan du søge og bruge grundlæggende filtrering.</span><span class="sxs-lookup"><span data-stu-id="fdc23-108">When viewing your data as tiles, you can search and use filtering.</span></span> <span data-ttu-id="fdc23-109">Når du vil bruge et komplet sæt af effektive funktioner til sortering, søgning eller filtrering, skal du vælge ikonet ![Vis som liste](media/ui_show_as_list_icon.png "Vis som liste pil til venstre") for at få vist posterne som en liste.</span><span class="sxs-lookup"><span data-stu-id="fdc23-109">To use the full set of powerful features for sorting, searching, and filtering, choose the ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to view the records as a list.</span></span>

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria, you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a><span data-ttu-id="fdc23-110">Sortering</span><span class="sxs-lookup"><span data-stu-id="fdc23-110">Sorting</span></span>

<span data-ttu-id="fdc23-111">Sortering gør det nemt og hurtigt for dig at overskue dine oplysninger.</span><span class="sxs-lookup"><span data-stu-id="fdc23-111">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="fdc23-112">Hvis du har mange kunder, f.eks. kan du vælge at sortere dem efter **Kundenr.**, **vvalutakode** eller **Lande-/områdekode** for at få det nødvendige overblik.</span><span class="sxs-lookup"><span data-stu-id="fdc23-112">For example, if you have many customers,  you could sort them by **Customer No.**, **Currency Code**, or **Country Region Code** to get the overview you need.</span></span>

<span data-ttu-id="fdc23-113">Hvis du vil sortere en liste, kan du enten:</span><span class="sxs-lookup"><span data-stu-id="fdc23-113">To sort a list, you can either:</span></span>

- <span data-ttu-id="fdc23-114">Vælg en kolonneoverskriftstekst til skift mellem stigende og faldende rækkefølge, eller</span><span class="sxs-lookup"><span data-stu-id="fdc23-114">Choose a column heading text to toggle between ascending and descending order, or</span></span>
- <span data-ttu-id="fdc23-115">Vælg rullepilen i kolonneoverskriften, og vælg derefter **stigende** eller **faldende**.</span><span class="sxs-lookup"><span data-stu-id="fdc23-115">Choose the drop-down arrow in the column heading, then choose the **Ascending** or **Descending** action.</span></span>  

> [!NOTE]  
> <span data-ttu-id="fdc23-116">Sortering understøttes ikke af billeder, BLOB-felter, FlowFilters og felter, der ikke tilhører en tabel.</span><span class="sxs-lookup"><span data-stu-id="fdc23-116">Sorting isn't supported on images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching"></a><span data-ttu-id="fdc23-117">Søgning</span><span class="sxs-lookup"><span data-stu-id="fdc23-117">Searching</span></span>

<!--## Searching by using the Quick Filter -->
<span data-ttu-id="fdc23-118">Øverst på hver oversigtsside finder du handlingen ![Søgeoversigt](media/ui-search/search-list.png "Ikonet Søgeoversigt") **Søg**, der er en hurtig og nem måde at reducere posterne på en liste på og kun viser de poster, der indeholder data, som du er interesseret i at få vist.</span><span class="sxs-lookup"><span data-stu-id="fdc23-118">At the top of each list page, there's a ![Search list](media/ui-search/search-list.png "Search list icon") **Search** action that provides a quick and easy way to reduce the records in a list and display only those records that contain the data that you're interested in seeing.</span></span>

<span data-ttu-id="fdc23-119">Du søger ved at vælge handlingen **Søg** og derefter skrive den tekst, du leder efter, i feltet.</span><span class="sxs-lookup"><span data-stu-id="fdc23-119">To search, just choose the **Search** action, and then in the box, type the text that you're looking for.</span></span> <span data-ttu-id="fdc23-120">Du kan skrive bogstaver, tal og andre symboler.</span><span class="sxs-lookup"><span data-stu-id="fdc23-120">You can enter letters, numbers, and other symbols.</span></span>

<span data-ttu-id="fdc23-121">Normalt vil søgningen forsøge at matche teksten på tværs af alle felter.</span><span class="sxs-lookup"><span data-stu-id="fdc23-121">In general, search will attempt to match text across all fields.</span></span> <span data-ttu-id="fdc23-122">Den skelner ikke mellem store og små bogstaver og sammenligner tekst, hvor som helst i feltet, ved begyndelsen, slutningen eller i midten.</span><span class="sxs-lookup"><span data-stu-id="fdc23-122">It doesn't distinguish between uppercase and lowercase characters (case insensitive) and will match text placed anywhere in the field, at the beginning, end, or in the middle.</span></span>

> [!TIP]
> <span data-ttu-id="fdc23-123">Du kan trykke på **F3** for at aktivere og deaktivere søgefeltet.</span><span class="sxs-lookup"><span data-stu-id="fdc23-123">You can press **F3** to activate and deactivate the search box.</span></span> <span data-ttu-id="fdc23-124">Du kan finde flere oplysninger i [Tastaturgenveje](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="fdc23-124">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

> [!NOTE]  
> <span data-ttu-id="fdc23-125">Søgning matcher ikke værdier i billeder, BLOB-felter, FlowFilter, FlowField og andre felter, der ikke er en del af en tabel.</span><span class="sxs-lookup"><span data-stu-id="fdc23-125">Search won't match values in images, BLOB fields, FlowFilters, FlowFields, and other fields that aren't part of a table.</span></span>


### <a name="fine-tuning-the-search-with-filter-criteria"></a><span data-ttu-id="fdc23-126">Finjustere søgningen med filterkriterier</span><span class="sxs-lookup"><span data-stu-id="fdc23-126">Fine-tuning the Search with Filter criteria</span></span>

<span data-ttu-id="fdc23-127">Du kan foretage en mere præcis søgning ved hjælp af filteroperatorer, udtryk og filter-tokens.</span><span class="sxs-lookup"><span data-stu-id="fdc23-127">You can make a more exact search by using filter operators, expressions, and filter tokens.</span></span> <span data-ttu-id="fdc23-128">I modsætning til filtrering anvendes alle felter på tværs af alle felter, når de bruges i søgefeltet, så de bliver mindre effektive end filtrering.</span><span class="sxs-lookup"><span data-stu-id="fdc23-128">Unlike filtering, these are applied across all fields when used in the search box, making them less efficient than filtering.</span></span>

- <span data-ttu-id="fdc23-129">Sæt søgeteksten i enkelte anførselstegn `''` (f.eks. `'man'`) for kun at finde feltværdier, der er identiske med hele teksten, og hvor små og store bogstaver er identiske.</span><span class="sxs-lookup"><span data-stu-id="fdc23-129">To find only field values that match the entire text and case exactly, place the search text between single quotes `''` (for example, `'man'`).</span></span>

- <span data-ttu-id="fdc23-130">Sæt `*` efter søgeteksten (f.eks. `man*`) for at finde feltværdier, der begynder med en bestemt tekst, og hvor små og store bogstaver er identiske.</span><span class="sxs-lookup"><span data-stu-id="fdc23-130">To find field values that start with a certain text and match the case, place `*` after the search text (for example `man*`).</span></span>

- <span data-ttu-id="fdc23-131">Sæt `*` før søgeteksten (f.eks. `*man`) for at finde feltværdier, der slutter med en bestemt tekst, og hvor små og store bogstaver er identiske.</span><span class="sxs-lookup"><span data-stu-id="fdc23-131">To find field values that end with a certain text and match the case, place `*` before the search text (for example `*man`).</span></span>

- <span data-ttu-id="fdc23-132">Når du bruger `''` eller `*`, skelnes der mellem små og store bogstaver i søgningen.</span><span class="sxs-lookup"><span data-stu-id="fdc23-132">When using  `''` or `*`, the search is case-sensitive.</span></span> <span data-ttu-id="fdc23-133">Hvis du vil have, at der skelnes mellem små og store bogstaver i søgningen, skal du indsætte `@` foran søgeteksten (for eksempel `@man*`).</span><span class="sxs-lookup"><span data-stu-id="fdc23-133">If you want to make the search case insensitive, place `@` before the search text (for example `@man*`).</span></span>

<span data-ttu-id="fdc23-134">Følgende tabel indeholder nogle eksempler, der forklarer, hvordan du kan bruge søgningen.</span><span class="sxs-lookup"><span data-stu-id="fdc23-134">The following table provides some examples to explain how you can use the search.</span></span>

|<span data-ttu-id="fdc23-135">Søgekriterier</span><span class="sxs-lookup"><span data-stu-id="fdc23-135">Search Criteria</span></span>|<span data-ttu-id="fdc23-136">Finder...</span><span class="sxs-lookup"><span data-stu-id="fdc23-136">Finds...</span></span>|
|---------------|----------|
|`man`<br /><span data-ttu-id="fdc23-137">eller</span><span class="sxs-lookup"><span data-stu-id="fdc23-137">or</span></span> <br />`Man`|<span data-ttu-id="fdc23-138">Alle poster med felter, der indeholder teksten **man**, uanset store eller små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="fdc23-138">All records with fields that contain the text **man**, regardless of the case.</span></span> <span data-ttu-id="fdc23-139">F.eks. **Manchester**, **manual** eller **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="fdc23-139">For example, **Manchester**, **manual**, or **Sportsman**.</span></span> |
|`'Man'`|<span data-ttu-id="fdc23-140">Alle poster med felter, der kun indeholder **Man**. Samme brug af store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="fdc23-140">All records with fields that contain only **Man**, matching the case.</span></span>|
|`Man*`|<span data-ttu-id="fdc23-141">Alle poster med felter, der begynder med teksten <b>Man</b>. Samme brug af store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="fdc23-141">All records with fields that start with the text <b>Man</b>, matching the case.</span></span> <span data-ttu-id="fdc23-142">F.eks. **Manchester**, men ikke **manual** eller **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="fdc23-142">For example, **Manchester** but not **manual** or **Sportsman**.</span></span>|
|`@Man*`|<span data-ttu-id="fdc23-143">Alle poster med felter, der begynder med teksten **man**, uanset om der bruges store eller små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="fdc23-143">All records with fields that start with **man**, regardless of the case.</span></span> <span data-ttu-id="fdc23-144">F.eks. **Manchester** og **manual**, men ikke **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="fdc23-144">For example, **Manchester** and **manual**, but not **Sportsman**.</span></span>|
|`@*man`|<span data-ttu-id="fdc23-145">Alle poster der slutter med teksten **man**, uanset om der er brugt store eller små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="fdc23-145">All records that end with **man**, regardless of the case.</span></span> <span data-ttu-id="fdc23-146">F.eks. **Sportsman**, men ikke **Manchester** eller **manual**.</span><span class="sxs-lookup"><span data-stu-id="fdc23-146">For example **Sportsman**, but not **Manchester** or **manual**.</span></span>|


## <a name="filtering"></a><a name="filtering"></a><span data-ttu-id="fdc23-147">Filtrering</span><span class="sxs-lookup"><span data-stu-id="fdc23-147">Filtering</span></span>

<span data-ttu-id="fdc23-148">Filtrering giver en mere avanceret og fleksibel må de at kontrollere, hvilke poster der skal vises på en liste eller medtages i en rapport eller XMLport.</span><span class="sxs-lookup"><span data-stu-id="fdc23-148">Filtering provides a more advanced and versatile way to control which records are included in a list, report, or XMLport.</span></span> <span data-ttu-id="fdc23-149">Der er to vigtige forskelle mellem søgning eller filtrering, som beskrevet i nedenstående tabel.</span><span class="sxs-lookup"><span data-stu-id="fdc23-149">There are two major differences between searching and filtering, as described in the table below.</span></span>

|| <span data-ttu-id="fdc23-150">**Søgning**</span><span class="sxs-lookup"><span data-stu-id="fdc23-150">**Searching**</span></span> | <span data-ttu-id="fdc23-151">**Filtrering**</span><span class="sxs-lookup"><span data-stu-id="fdc23-151">**Filtering**</span></span> |
|--|----------|------------|
| <span data-ttu-id="fdc23-152">**Relevante felter**</span><span class="sxs-lookup"><span data-stu-id="fdc23-152">**Applicable Fields**</span></span> | <span data-ttu-id="fdc23-153">Søger på tværs af alle de felter, der kan ses på siden.</span><span class="sxs-lookup"><span data-stu-id="fdc23-153">Searches across all fields that are visible on the page.</span></span> | <span data-ttu-id="fdc23-154">Filtrerer et eller flere felter hver for sig og vælger fra et felt i tabellen, herunder felter, ikke der kan ses på siden.</span><span class="sxs-lookup"><span data-stu-id="fdc23-154">Filters one or more fields individually, selecting from any field on the table, including fields that aren't visible on the page.</span></span> |
| <span data-ttu-id="fdc23-155">**Matching**</span><span class="sxs-lookup"><span data-stu-id="fdc23-155">**Matching**</span></span> | <span data-ttu-id="fdc23-156">Viser poster med felter, der stemmer overens med søgeteksten, uanset store eller små bogstaver eller placeringen af teksten.</span><span class="sxs-lookup"><span data-stu-id="fdc23-156">Displays records with fields that match the search text, no matter the text's case or placement in the field.</span></span> | <span data-ttu-id="fdc23-157">Viser poster, hvor feltet nøjagtigt svarer til filteret, og der skelnes mellem små og store bogstaver, medmindre der er angivet særlige filtersymboler.</span><span class="sxs-lookup"><span data-stu-id="fdc23-157">Displays records where the field exactly matches the filter, including the text's case, unless special filter symbols are entered.</span></span>

<span data-ttu-id="fdc23-158">Filtrering giver dig mulighed at få vist poster for bestemte konti eller kunder, datoer, beløb og andre oplysninger ved at angive filterkriterier.</span><span class="sxs-lookup"><span data-stu-id="fdc23-158">Filtering enables you to display records for specific accounts or customers, dates, amounts, and other information by specifying filter criteria.</span></span> <span data-ttu-id="fdc23-159">Kun poster, der opfylder de kriterier, som vises på listen, medtages i rapporten, kørslen eller XMLport.</span><span class="sxs-lookup"><span data-stu-id="fdc23-159">Only records that match the criteria are displayed on the list or included in the report, batch job, or XMLport.</span></span> <span data-ttu-id="fdc23-160">Hvis du angiver kriterier for flere felter, vises kun poster, der svarer til alle kriterier.</span><span class="sxs-lookup"><span data-stu-id="fdc23-160">If you specify criteria for multiple fields, then only records that match all criteria will be displayed.</span></span>

<span data-ttu-id="fdc23-161">I forbindelse med lister vises filtrene i en filterrude, der vises til venstre på listen, når du aktiverer den.</span><span class="sxs-lookup"><span data-stu-id="fdc23-161">For lists, the filters are displayed on a filter pane that appears to the left of the list when you activate it.</span></span> <span data-ttu-id="fdc23-162">For rapporter, kørsler og XMLporte kan filtrene ses direkte på anmodningssiden.</span><span class="sxs-lookup"><span data-stu-id="fdc23-162">For reports, batch jobs, and XMLports, the filters are visible directly on the request page.</span></span>

### <a name="filtering-with-option-fields"></a><span data-ttu-id="fdc23-163">Filtrere med indstillingsfelter</span><span class="sxs-lookup"><span data-stu-id="fdc23-163">Filtering with Option Fields</span></span>

<span data-ttu-id="fdc23-164">I forbindelse med "almindelige" felter, der indeholder data, opsætningsdata eller virksomhedsdata, kan du indsætte filtre både ved at vælge data og indtaste filterværdier, og du kan bruge symboler til at angive avancerede filterkriterier.</span><span class="sxs-lookup"><span data-stu-id="fdc23-164">For "ordinary" fields that hold data, setup date, or business data, you can set filters both by selecting data and by typing filter values, and you can use symbols to define advanced filter criteria.</span></span> <span data-ttu-id="fdc23-165">Du kan finde flere oplysninger i [Angivelse af filerkriterier](ui-enter-criteria-filters.md#entering-filter-criteria).</span><span class="sxs-lookup"><span data-stu-id="fdc23-165">For more information, see [Entering Filter Criteria](ui-enter-criteria-filters.md#entering-filter-criteria).</span></span>

<span data-ttu-id="fdc23-166">Ved felter af typen **Indstilling** kan du imidlertid kun angive et filter ved at vælge en eller flere indstillinger på en rulleliste med tilgængelige indstillinger.</span><span class="sxs-lookup"><span data-stu-id="fdc23-166">For fields of type **Option**, however, you can only set a filter by selecting one or more options from a drop-down list of the available options.</span></span> <span data-ttu-id="fdc23-167">Et eksempel på et indstillingsfelt er feltet **Status** på siden **Salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="fdc23-167">An example of an option field is the **Status** field on the **Sales Orders** page.</span></span>

> [!NOTE]
> <span data-ttu-id="fdc23-168">Hvis du vælger flere indstillinger som en filterværdi, defineres relationen mellem indstillingerne som *OR*.</span><span class="sxs-lookup"><span data-stu-id="fdc23-168">When you select multiple options as a filter value, the relationship between the options is defined as *OR*.</span></span> <span data-ttu-id="fdc23-169">Hvis du f.eks. både markerer afkrydsningsfeltet **Åbne** og afkrydsningsfeltet **Frigivet** i filterfeltet **Status** på siden **Salgsordrer**, betyder det, at salgsordrer, der enten er åbne eller frigivne, vises.</span><span class="sxs-lookup"><span data-stu-id="fdc23-169">For example, if you select both the **Open** and the **Released** check box in the **Status** filter field on the **Sales Orders** page, it means that sales orders that are either open or released are displayed.</span></span>

### <a name="setting-filters-on-lists"></a><span data-ttu-id="fdc23-170">Angive filtre på lister</span><span class="sxs-lookup"><span data-stu-id="fdc23-170">Setting Filters on Lists</span></span>

<span data-ttu-id="fdc23-171">På lister kan du indstille filtre ved hjælp af filterruden.</span><span class="sxs-lookup"><span data-stu-id="fdc23-171">On lists, you set filters by using the filter pane.</span></span> <span data-ttu-id="fdc23-172">Hvis du vil have vist filterruden for en liste, skal du vælge rullepilen ud for navnet på siden og derefter vælge handlingen **Vis filterrude**.</span><span class="sxs-lookup"><span data-stu-id="fdc23-172">To display the filter pane for a list, choose the drop-down arrow next to the name of the page, and then choose the **Show filter pane** action.</span></span> <span data-ttu-id="fdc23-173">Du kan også trykke på **Skift+F3**.</span><span class="sxs-lookup"><span data-stu-id="fdc23-173">Alternatively, press **Shift+F3**.</span></span>

<span data-ttu-id="fdc23-174">Hvis du vil have vist filterruden for kolonne på en liste, skal du vælge rullepilen og derefter vælge handlingen **Filter**.</span><span class="sxs-lookup"><span data-stu-id="fdc23-174">To display the filter pane for a column on a list, choose the drop-down arrow, and then choose the **Filter** action.</span></span> <span data-ttu-id="fdc23-175">Du kan også trykke på **Skift+F3**.</span><span class="sxs-lookup"><span data-stu-id="fdc23-175">Alternatively, press **Shift+F3**.</span></span> <span data-ttu-id="fdc23-176">Filterruden åbnes med den valgte kolonne vist som filterfelt i sektionen **Filtrer listen efter**.</span><span class="sxs-lookup"><span data-stu-id="fdc23-176">The filter pane opens with the selected column shown as a filter field in the **Filter list by** section.</span></span>

<span data-ttu-id="fdc23-177">Filterruden viser de aktuelle filtre på en liste, og gør det muligt at angive dine egne brugerdefinerede filtre i et eller flere felter ved at vælge handlingen **+ Filter**.</span><span class="sxs-lookup"><span data-stu-id="fdc23-177">The filter pane displays the current filters for a list, and enables you to set your own custom filters on one or more fields by choosing the **+ Filter** action.</span></span>

 <span data-ttu-id="fdc23-178">En filterrude er inddelt i tre afsnit: **Visninger**, **Filtrer listen efter** og **Filtrer totaler efter**:</span><span class="sxs-lookup"><span data-stu-id="fdc23-178">A filter pane is divided in three sections: **Views**, **Filter list by**, and **Filter totals by**:</span></span>

- <span data-ttu-id="fdc23-179">**Visninger**</span><span class="sxs-lookup"><span data-stu-id="fdc23-179">**Views**</span></span>

  <span data-ttu-id="fdc23-180">Nogle lister indeholder sektionen **Visninger**.</span><span class="sxs-lookup"><span data-stu-id="fdc23-180">Some lists include the **Views** section.</span></span> <span data-ttu-id="fdc23-181">Visninger er variationer af listen, der er forudkonfigureret med filtre.</span><span class="sxs-lookup"><span data-stu-id="fdc23-181">Views are variations of the list that have been preconfigured with filters.</span></span> <span data-ttu-id="fdc23-182">Du kan definere og gemme så mange visninger, du ønsker, pr. liste.</span><span class="sxs-lookup"><span data-stu-id="fdc23-182">You can define and save as many views as you want per list.</span></span> <span data-ttu-id="fdc23-183">Visningerne er tilgængelige for dig på alle de enheder, du logger på.</span><span class="sxs-lookup"><span data-stu-id="fdc23-183">The views will be available to you on any device you sign into.</span></span> <span data-ttu-id="fdc23-184">Du kan finde flere oplysninger i [Gemme og tilpasse listevisninger](ui-views.md).</span><span class="sxs-lookup"><span data-stu-id="fdc23-184">For more information, see [Save and Personalize List Views](ui-views.md).</span></span>

- <span data-ttu-id="fdc23-185">**Filtrer listen efter**</span><span class="sxs-lookup"><span data-stu-id="fdc23-185">**Filter list by**</span></span>

  <span data-ttu-id="fdc23-186">Det er i denne sektion, du kan tilføje filtre i bestemte felter for at reducere antallet af viste poster.</span><span class="sxs-lookup"><span data-stu-id="fdc23-186">This section is where you add filters on specific fields to reduce the number of displayed records.</span></span> <span data-ttu-id="fdc23-187">Hvis du vil tilføje et filter, skal du vælge handlingen **+ Filter**.</span><span class="sxs-lookup"><span data-stu-id="fdc23-187">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="fdc23-188">Når du vil tilføje et filter, skal du skrive navnet på det felt, du vil filtrere listen efter, eller vælge et felt på rullelisten.</span><span class="sxs-lookup"><span data-stu-id="fdc23-188">Then, type the name of the field that you want to filter the list by or pick a field from the drop-down list.</span></span>

- <span data-ttu-id="fdc23-189">**Filtrer totaler efter**</span><span class="sxs-lookup"><span data-stu-id="fdc23-189">**Filter totals by**</span></span>

  <span data-ttu-id="fdc23-190">Nogle lister, der viser beregnede felter, som beløb og antal, indeholder sektionen **Filtrer totaler efter**, hvor du kan justere forskellige dimensioner, der påvirker beregninger.</span><span class="sxs-lookup"><span data-stu-id="fdc23-190">Some lists that display calculated fields, such as amounts and quantities, will include the **Filter totals by** section where you can adjust various dimensions that influence calculations.</span></span> <span data-ttu-id="fdc23-191">Hvis du vil tilføje et filter, skal du vælge handlingen **+ Filter**.</span><span class="sxs-lookup"><span data-stu-id="fdc23-191">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="fdc23-192">Når du vil tilføje et filter, skal du skrive navnet på det felt, du vil filtrere listen efter, eller vælge et felt på rullelisten.</span><span class="sxs-lookup"><span data-stu-id="fdc23-192">Then, type the name of the field that you want to filter the list by or pick a field from the drop-down list.</span></span>

  > [!NOTE]
  > <span data-ttu-id="fdc23-193">Filtre i sektionen **Filtrer totaler efter** styres af FlowFilters i sideopsætningen.</span><span class="sxs-lookup"><span data-stu-id="fdc23-193">Filters in the **Filter totals by** section are controlled by FlowFilters on the page design.</span></span> <span data-ttu-id="fdc23-194">Du kan finde tekniske oplysninger i [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span><span class="sxs-lookup"><span data-stu-id="fdc23-194">For technical information, see [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span></span>

<span data-ttu-id="fdc23-195">Du kan angive et enkelt filter direkte på en liste under brug af filterruden, dvs. et filter, hvor der kun vises poster med den samme værdi som i den markerede celle.</span><span class="sxs-lookup"><span data-stu-id="fdc23-195">You can set a simple filter directly on a list within using the filter pane, namely a filter that displays only records with the same value as in the selected cell.</span></span> <span data-ttu-id="fdc23-196">Vælg en celle på listen, vælg rullepilen, og vælg derefter handlingen **Filtrer til denne værdi**.</span><span class="sxs-lookup"><span data-stu-id="fdc23-196">Select a cell on the list, choose the drop-down arrow, and then choose the **Filter to This Value** action.</span></span> <span data-ttu-id="fdc23-197">Du kan også trykke på **Alt+F3**.</span><span class="sxs-lookup"><span data-stu-id="fdc23-197">Alternatively, press **Alt+F3**.</span></span>

### <a name="setting-filters-in-reports-batch-jobs-and-xmlports"></a><span data-ttu-id="fdc23-198">Angive filtre i rapporter, kørsler og XMLporte</span><span class="sxs-lookup"><span data-stu-id="fdc23-198">Setting Filters in Reports, Batch Jobs, and XMLports</span></span>

<span data-ttu-id="fdc23-199">For rapporter og XMLporte kan filtrene ses direkte på anmodningssiden.</span><span class="sxs-lookup"><span data-stu-id="fdc23-199">For reports and XMLports, the filters are visible directly on the request page.</span></span> <span data-ttu-id="fdc23-200">På anmodningssiden vises de senest anvendte filtre på grundlag af dit valg i feltet **Brug standardværdier fra**.</span><span class="sxs-lookup"><span data-stu-id="fdc23-200">The request page displays the last used filters according to your selection in the **Use default values from** field.</span></span> <span data-ttu-id="fdc23-201">Du kan finde flere oplysninger i [Bruge gemte indstillinger](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="fdc23-201">For more information, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

<span data-ttu-id="fdc23-202">**Filter**-hovedsektionen viser de standardfilterfelter, som du kan bruge til at afgrænse, hvilke poster der skal medtages i rapporten eller i XMLport.</span><span class="sxs-lookup"><span data-stu-id="fdc23-202">The main **Filter** section shows the default filter fields that you use to delimit which records to include in the report or XMLport.</span></span> <span data-ttu-id="fdc23-203">Hvis du vil tilføje et filter, skal du vælge handlingen **+ Filter**.</span><span class="sxs-lookup"><span data-stu-id="fdc23-203">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="fdc23-204">Når du vil tilføje et filter, skal du skrive navnet på det felt, du vil filtrere listen efter, eller vælge et felt på rullelisten.</span><span class="sxs-lookup"><span data-stu-id="fdc23-204">Then, type the name of the field that you want to filter by, or pick a field from the drop-down list.</span></span>

<span data-ttu-id="fdc23-205">I sektionen **Filtrer totaler efter** kan du justere forskellige dimensioner, der påvirker beregninger i rapporten eller i XMLport.</span><span class="sxs-lookup"><span data-stu-id="fdc23-205">In the **Filter totals by** section, you can adjust various dimensions that influence calculations in the report or XMLport.</span></span> <span data-ttu-id="fdc23-206">Hvis du vil tilføje et filter, skal du vælge handlingen **+ Filter**.</span><span class="sxs-lookup"><span data-stu-id="fdc23-206">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="fdc23-207">Når du vil tilføje et filter, skal du skrive navnet på det felt, du vil filtrere listen efter, eller vælge et felt på rullelisten.</span><span class="sxs-lookup"><span data-stu-id="fdc23-207">Then, type the name of the field that you want to filter by, or pick a field from the drop-down list.</span></span>

## <a name="entering-filter-criteria"></a><span data-ttu-id="fdc23-208">Angivelse af filterkriterier</span><span class="sxs-lookup"><span data-stu-id="fdc23-208">Entering Filter Criteria</span></span>

<span data-ttu-id="fdc23-209">Både i filterruden og på en anmodningsside angiver du filterkriterierne i feltet under filterfeltet.</span><span class="sxs-lookup"><span data-stu-id="fdc23-209">Both in the filter pane and on a request page, you enter your filter criteria in the box under the filter field.</span></span>

<span data-ttu-id="fdc23-210">Filterfeltets type er bestemmende for, hvilke kriterier du kan angive.</span><span class="sxs-lookup"><span data-stu-id="fdc23-210">The type of the filter field determines which criteria you can enter.</span></span> <span data-ttu-id="fdc23-211">For eksempel kan du, når du filtrerer et felt, der har faste værdier, kun vælge mellem disse værdier.</span><span class="sxs-lookup"><span data-stu-id="fdc23-211">For example, filtering a field that has fixed values will only let you choose from those values.</span></span> <span data-ttu-id="fdc23-212">Du kan finde yderligere oplysninger om særlige filtersymboler i [Filterkriterier](#FilterCriteria) og [Filtertokens](#FilterTokens).</span><span class="sxs-lookup"><span data-stu-id="fdc23-212">For more information about special filter symbols, see [Filter criteria](#FilterCriteria) and [Filter tokens](#FilterTokens).</span></span>

<span data-ttu-id="fdc23-213">Kolonner, som allerede indeholder filtre, er angivet med ikonet ![Filter](media/ui-search/filter-icon.png "Filter-ikon") i kolonneoverskriften.</span><span class="sxs-lookup"><span data-stu-id="fdc23-213">Columns that already have filters are indicated by the ![Filter icon](media/ui-search/filter-icon.png "Filter icon") icon in the column heading.</span></span> <span data-ttu-id="fdc23-214">Hvis du vil fjerne et filter, skal du vælge rullepilen og derefter vælge handlingen **Ryd filter**.</span><span class="sxs-lookup"><span data-stu-id="fdc23-214">To remove a filter, choose the drop-down arrow, and then choose the **Clear Filter** action.</span></span>

> [!TIP]
> <span data-ttu-id="fdc23-215">Fremskynd søgning efter og analyse af dine data ved hjælp af kombinationer af genvejstaster.</span><span class="sxs-lookup"><span data-stu-id="fdc23-215">Accelerate finding and analyzing your data by using combinations of keyboard shortcuts.</span></span> <span data-ttu-id="fdc23-216">For f.eks. at markere et felt skal du bruge **Skift + Alt + F3** for at føje dette felt til filterruden, angive filterkriterierne, bruge **Ctrl + Enter** for at vende tilbage til rækkerne, vælge et andet felt og bruge **Alt + F3** til at filtrere til værdien.</span><span class="sxs-lookup"><span data-stu-id="fdc23-216">For example, select a field, use **Shift+Alt+F3** to add that field to the filter pane, type the filter criteria, use **Ctrl+Enter** to return to the rows, select another field, and use **Alt+F3** to filter to that value.</span></span> <span data-ttu-id="fdc23-217">Du kan finde flere oplysninger i [Tastaturgenveje](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="fdc23-217">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

### <a name="filter-criteria-and-operators"></a><span data-ttu-id="fdc23-218"><a name="FilterCriteria"> </a>Filterkriterier og -operatorer</span><span class="sxs-lookup"><span data-stu-id="fdc23-218"><a name="FilterCriteria"> </a>Filter Criteria and Operators</span></span>

<span data-ttu-id="fdc23-219">Når du angiver kriterier, kan du bruge alle de tal og bogstaver, som du plejer at bruger i feltet.</span><span class="sxs-lookup"><span data-stu-id="fdc23-219">When you enter criteria, you can use all the numbers and letters that you normally use in the field.</span></span> <span data-ttu-id="fdc23-220">Men der er også en række specielle symboler, som du kan bruge som operatorer for at filtrere resultaterne yderligere.</span><span class="sxs-lookup"><span data-stu-id="fdc23-220">But there's also a set of special symbols that you can use as operators to further filter the results.</span></span> <span data-ttu-id="fdc23-221">I følgende afsnit beskrives disse symboler, og hvordan de bruges som operatorer i filtre.</span><span class="sxs-lookup"><span data-stu-id="fdc23-221">The following sections describe these symbols and how to use them as operators in filters.</span></span>

> [!TIP]
> <span data-ttu-id="fdc23-222">Du kan finde flere oplysninger om filtrering af dato og klokkeslæt i [Arbejde med kalenderdatoer og-klokkeslæt](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="fdc23-222">For more information about filtering dates and times, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="fdc23-223">Der kan være situationer, hvor den værdi, der skal filtreres efter, indeholder et symbol, som er en operator.</span><span class="sxs-lookup"><span data-stu-id="fdc23-223">There may be situations where the value that you want to filter on contains a symbol that's an operator.</span></span> <span data-ttu-id="fdc23-224">Du kan finde flere oplysninger om håndtering af disse situationer i [Filtrering på værdier, der indeholder symboler](#symbols) for at få flere oplysninger om håndtering af denne situation.</span><span class="sxs-lookup"><span data-stu-id="fdc23-224">For more information about handling these situtions, see [Filtering on Values That Contain Symbols](#symbols) for more instructions about handling this situation.</span></span>
>
> - <span data-ttu-id="fdc23-225">Hvis der er mere end 200 operatorer i et enkelt filter, vil systemet automatisk gruppere nogle udtryk i parenteser `()` med henblik på behandling.</span><span class="sxs-lookup"><span data-stu-id="fdc23-225">If there are more than 200 operators in a single filter, the system will automatically group some expressions in parentheses `()` for the purpose of processing.</span></span> <span data-ttu-id="fdc23-226">Det har ingen indflydelse på filteret eller resultaterne.</span><span class="sxs-lookup"><span data-stu-id="fdc23-226">This has no effect on the filter or the results.</span></span>  

#### <a name="-interval"></a><span data-ttu-id="fdc23-227">(..) Interval</span><span class="sxs-lookup"><span data-stu-id="fdc23-227">(..) Interval</span></span>

|<span data-ttu-id="fdc23-228">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fdc23-228">Sample Expression</span></span>|<span data-ttu-id="fdc23-229">Viste poster</span><span class="sxs-lookup"><span data-stu-id="fdc23-229">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1100..2100`|<span data-ttu-id="fdc23-230">Tal fra 1100 til og med 2100.</span><span class="sxs-lookup"><span data-stu-id="fdc23-230">Numbers 1100 through 2100</span></span>|  
|`..2500`|<span data-ttu-id="fdc23-231">Konti til og med 2500</span><span class="sxs-lookup"><span data-stu-id="fdc23-231">Up to and including 2500</span></span>|  
|`..12 31 00`|<span data-ttu-id="fdc23-232">Datoer til og med 31-12-00.</span><span class="sxs-lookup"><span data-stu-id="fdc23-232">Dates up to and including 12 31 00</span></span>|  
|`P8..`|<span data-ttu-id="fdc23-233">Oplysninger for regnskabsperiode 8 og frem</span><span class="sxs-lookup"><span data-stu-id="fdc23-233">Information for accounting period 8 and after</span></span>|  
|`..23`|<span data-ttu-id="fdc23-234">Fra begyndelsesdatoen til 23-aktuel måned-aktuelt år 23.59.59</span><span class="sxs-lookup"><span data-stu-id="fdc23-234">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|`23..`|<span data-ttu-id="fdc23-235">Fra 23-aktuel måned-aktuelt år 0.00.00 til sluttidspunktet</span><span class="sxs-lookup"><span data-stu-id="fdc23-235">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|`22..23`|<span data-ttu-id="fdc23-236">Fra den 23-aktuel måned-aktuelt år 0.00.00 til 22-aktuel måned-aktuelt år 22.59.59</span><span class="sxs-lookup"><span data-stu-id="fdc23-236">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  

#### <a name="124-eitheror"></a><span data-ttu-id="fdc23-237">(&#124;) Enten/eller</span><span class="sxs-lookup"><span data-stu-id="fdc23-237">(&#124;) Either/or</span></span>

|<span data-ttu-id="fdc23-238">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fdc23-238">Sample Expression</span></span>|<span data-ttu-id="fdc23-239">Viste poster</span><span class="sxs-lookup"><span data-stu-id="fdc23-239">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1200|1300`|<span data-ttu-id="fdc23-240">Tal med 1200 eller 1300.</span><span class="sxs-lookup"><span data-stu-id="fdc23-240">Numbers with 1200 or 1300</span></span>|  

#### <a name="-not-equal-to"></a><span data-ttu-id="fdc23-241">(<>) Ikke lig med</span><span class="sxs-lookup"><span data-stu-id="fdc23-241">(<>) Not equal to</span></span>  

|<span data-ttu-id="fdc23-242">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fdc23-242">Sample Expression</span></span>|<span data-ttu-id="fdc23-243">Viste poster</span><span class="sxs-lookup"><span data-stu-id="fdc23-243">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<>0`|<span data-ttu-id="fdc23-244">Alle tal undtagen 0</span><span class="sxs-lookup"><span data-stu-id="fdc23-244">All numbers except 0</span></span><br /><br /> <span data-ttu-id="fdc23-245">I SQL Server Option kan du kombinere dette symbol med et udtryk med jokertegn.</span><span class="sxs-lookup"><span data-stu-id="fdc23-245">The SQL Server Option allows you to combine this symbol with a wild-card expression.</span></span> <span data-ttu-id="fdc23-246"><>A\* betyder f.eks. ikke lig med tekst, der starter med A.</span><span class="sxs-lookup"><span data-stu-id="fdc23-246">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  

#### <a name="-greater-than"></a><span data-ttu-id="fdc23-247">(>) Større end</span><span class="sxs-lookup"><span data-stu-id="fdc23-247">(>) Greater than</span></span>  

|<span data-ttu-id="fdc23-248">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fdc23-248">Sample Expression</span></span>|<span data-ttu-id="fdc23-249">Viste poster</span><span class="sxs-lookup"><span data-stu-id="fdc23-249">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>1200`|<span data-ttu-id="fdc23-250">Tal større end 1200</span><span class="sxs-lookup"><span data-stu-id="fdc23-250">Numbers greater than 1200</span></span>|  

#### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="fdc23-251">(>=) Større end eller lig med</span><span class="sxs-lookup"><span data-stu-id="fdc23-251">(>=) Greater than or equal to</span></span>  

|<span data-ttu-id="fdc23-252">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fdc23-252">Sample Expression</span></span>|<span data-ttu-id="fdc23-253">Viste poster</span><span class="sxs-lookup"><span data-stu-id="fdc23-253">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>=1200`|<span data-ttu-id="fdc23-254">Tal lig med eller større end 1200</span><span class="sxs-lookup"><span data-stu-id="fdc23-254">Numbers greater than or equal to 1200</span></span>|  

#### <a name="-less-than"></a><span data-ttu-id="fdc23-255">(<) Mindre end</span><span class="sxs-lookup"><span data-stu-id="fdc23-255">(<) Less than</span></span>  

|<span data-ttu-id="fdc23-256">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fdc23-256">Sample Expression</span></span>|<span data-ttu-id="fdc23-257">Viste poster</span><span class="sxs-lookup"><span data-stu-id="fdc23-257">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<1200`|<span data-ttu-id="fdc23-258">Tal mindre end 1200</span><span class="sxs-lookup"><span data-stu-id="fdc23-258">Numbers less than 1200</span></span>|  

#### <a name="-less-than-or-equal-to"></a><span data-ttu-id="fdc23-259">(<=) Mindre end eller lig med</span><span class="sxs-lookup"><span data-stu-id="fdc23-259">(<=) Less than or equal to</span></span>  

|<span data-ttu-id="fdc23-260">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fdc23-260">Sample Expression</span></span>|<span data-ttu-id="fdc23-261">Viste poster</span><span class="sxs-lookup"><span data-stu-id="fdc23-261">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<=1200`|<span data-ttu-id="fdc23-262">Tal lig med eller mindre end 1200</span><span class="sxs-lookup"><span data-stu-id="fdc23-262">Numbers less than or equal to 1200</span></span>|  

#### <a name="-and"></a><span data-ttu-id="fdc23-263">(&) Og</span><span class="sxs-lookup"><span data-stu-id="fdc23-263">(&) And</span></span>  

|<span data-ttu-id="fdc23-264">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fdc23-264">Sample Expression</span></span>|<span data-ttu-id="fdc23-265">Viste poster</span><span class="sxs-lookup"><span data-stu-id="fdc23-265">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>200&<1200`|<span data-ttu-id="fdc23-266">Tal større end 200 og mindre end 1200</span><span class="sxs-lookup"><span data-stu-id="fdc23-266">Numbers greater than 200 and less than 1200</span></span>|  

#### <a name="-an-exact-character-match"></a><span data-ttu-id="fdc23-267">('') Tegn, der stemmer nøjagtigt overens</span><span class="sxs-lookup"><span data-stu-id="fdc23-267">('') An exact character match</span></span>  

|<span data-ttu-id="fdc23-268">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fdc23-268">Sample Expression</span></span>|<span data-ttu-id="fdc23-269">Viste poster</span><span class="sxs-lookup"><span data-stu-id="fdc23-269">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`'man'`|<span data-ttu-id="fdc23-270">Tekst, der svarer nøjagtigt til **man**, og der skelnes mellem store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="fdc23-270">Text that matches **man** exactly and is case-sensitive.</span></span>|  

#### <a name="-case-insensitive"></a><span data-ttu-id="fdc23-271">(@) Ingen forskel på store og små bogstaver</span><span class="sxs-lookup"><span data-stu-id="fdc23-271">(@) Case insensitive</span></span>  

|<span data-ttu-id="fdc23-272">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fdc23-272">Sample Expression</span></span>|<span data-ttu-id="fdc23-273">Viste poster</span><span class="sxs-lookup"><span data-stu-id="fdc23-273">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`@man*`|<span data-ttu-id="fdc23-274">Tekst, der starter med **man**, og der skelnes mellem store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="fdc23-274">Text that starts with **man** and is case insensitive.</span></span>|  

#### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="fdc23-275">(\*) Mange ukendte tegn</span><span class="sxs-lookup"><span data-stu-id="fdc23-275">(\*) An indefinite number of unknown characters</span></span>

|<span data-ttu-id="fdc23-276">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fdc23-276">Sample Expression</span></span>|<span data-ttu-id="fdc23-277">Viste poster</span><span class="sxs-lookup"><span data-stu-id="fdc23-277">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`*Co*`|<span data-ttu-id="fdc23-278">Tekst, der indeholder **A/S**, og der skelnes mellem store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="fdc23-278">Text that contains **Co** and is case-sensitive.</span></span>|  
|`*Co`|<span data-ttu-id="fdc23-279">Tekst, der ender på **A/S**, og der skelnes mellem store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="fdc23-279">Text that ends with **Co"** and is case-sensitive.</span></span>|  
|`Co*`|<span data-ttu-id="fdc23-280">Tekst, der begynder med **A/S**, og der skelnes mellem store og små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="fdc23-280">Text that begins with **Co** and is case-sensitive.</span></span>|  

#### <a name="-one-unknown-character"></a><span data-ttu-id="fdc23-281">(?) Ét ukendt tegn</span><span class="sxs-lookup"><span data-stu-id="fdc23-281">(?) One unknown character</span></span>  

|<span data-ttu-id="fdc23-282">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fdc23-282">Sample Expression</span></span>|<span data-ttu-id="fdc23-283">Viste poster</span><span class="sxs-lookup"><span data-stu-id="fdc23-283">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`Hans?n`|<span data-ttu-id="fdc23-284">Tekst som f.eks. **Hansen** eller **Hanson**</span><span class="sxs-lookup"><span data-stu-id="fdc23-284">Text such as **Hansen** or **Hanson**</span></span>|  

#### <a name="combined-format-expressions"></a><span data-ttu-id="fdc23-285">Kombinerede formatudtryk</span><span class="sxs-lookup"><span data-stu-id="fdc23-285">Combined Format Expressions</span></span>  

|<span data-ttu-id="fdc23-286">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fdc23-286">Sample Expression</span></span>|<span data-ttu-id="fdc23-287">Viste poster</span><span class="sxs-lookup"><span data-stu-id="fdc23-287">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|<span data-ttu-id="fdc23-288">Tallet 5999 og tallene fra og med 8100 til og med 8490.</span><span class="sxs-lookup"><span data-stu-id="fdc23-288">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|`..1299|1400..`|<span data-ttu-id="fdc23-289">Medtag poster med et tal mindre end eller lig med 1299, eller tal lig med 1400 eller derover (alle tal undtagen 1300 til og med 1399).</span><span class="sxs-lookup"><span data-stu-id="fdc23-289">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|`>50&<100`|<span data-ttu-id="fdc23-290">Medtag poster med tal større end 50 og mindre end 100 (tal fra 51 til og med 99).</span><span class="sxs-lookup"><span data-stu-id="fdc23-290">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  

### <a name="filtering-on-values-that-contain-symbols"></a><a name="symbols"></a><span data-ttu-id="fdc23-291">Filtrere på værdier, der indeholder symboler</span><span class="sxs-lookup"><span data-stu-id="fdc23-291">Filtering on Values That Contain Symbols</span></span>

<span data-ttu-id="fdc23-292">Der kan være tilfælde, hvor feltværdier indeholder et af følgende symboler:</span><span class="sxs-lookup"><span data-stu-id="fdc23-292">There may be cases where field values contain the one of the following symbols:</span></span>

- &
- <span data-ttu-id="fdc23-293">(</span><span class="sxs-lookup"><span data-stu-id="fdc23-293">(</span></span>
- <span data-ttu-id="fdc23-294">)</span><span class="sxs-lookup"><span data-stu-id="fdc23-294">)</span></span>
- =
- <span data-ttu-id="fdc23-295">&#124;</span><span class="sxs-lookup"><span data-stu-id="fdc23-295">&#124;</span></span>

<span data-ttu-id="fdc23-296">Hvis du vil filtrere efter et af disse symboler, skal du placere filterudtrykket i anførselstegn (' ').</span><span class="sxs-lookup"><span data-stu-id="fdc23-296">If you want to filter on any of these symbols, place the filter expression in quotation marks ('').</span></span> <span data-ttu-id="fdc23-297">Hvis du f.eks. vil filtrere efter poster, der starter med teksten *J & V*, er filterudtrykket `'J & V*'`.</span><span class="sxs-lookup"><span data-stu-id="fdc23-297">For example, if you wanted to filter on records that start with the text *J & V*, the filter expression would be `'J & V*'`.</span></span>

<span data-ttu-id="fdc23-298">Dette krav er ikke nødvendigt for andre symboler.</span><span class="sxs-lookup"><span data-stu-id="fdc23-298">This requirement isn't necessary for other symbols.</span></span>

### <a name="filter-tokens"></a><span data-ttu-id="fdc23-299"><a name="FilterTokens"> </a>Filtertokens</span><span class="sxs-lookup"><span data-stu-id="fdc23-299"><a name="FilterTokens"> </a>Filter Tokens</span></span>

<span data-ttu-id="fdc23-300">Når du angiver filterkriterier, kan du også skrive ord, der har en særlig betydning, kaldet filtertokens.</span><span class="sxs-lookup"><span data-stu-id="fdc23-300">When entering filter criteria, you can also type words that have special meaning, called filter tokens.</span></span> <span data-ttu-id="fdc23-301">Når du har angivet et tokenordet, erstattes ordet af den eller de værdier, det repræsenterer.</span><span class="sxs-lookup"><span data-stu-id="fdc23-301">After entering the token word, the word is replaced by the value or values that it represents.</span></span> <span data-ttu-id="fdc23-302">Med filter-tokens bliver filtrering nemmere ved at reducere behovet for at navigere til andre sider for at søge efter værdier, du vil føje til filteret.</span><span class="sxs-lookup"><span data-stu-id="fdc23-302">Filter tokens make filtering easier by reducing the need to navigate to other pages to look up values you want to add to your filter.</span></span> <span data-ttu-id="fdc23-303">Tabellerne nedenfor beskriver nogle af de tegn, du kan skrive som filterkriterier.</span><span class="sxs-lookup"><span data-stu-id="fdc23-303">The tables below describe some of the tokens you can type as filter criteria.</span></span>

> [!TIP]
> <span data-ttu-id="fdc23-304">Din organisation bruger muligvis brugerdefinerede tokens.</span><span class="sxs-lookup"><span data-stu-id="fdc23-304">Your organization may use custom tokens.</span></span> <span data-ttu-id="fdc23-305">For at få mere at vide om det komplette sæt tokens, der er tilgængelige for dig, eller tilføje flere brugerdefinerede tokens, skal du kontakte din administrator.</span><span class="sxs-lookup"><span data-stu-id="fdc23-305">To learn about the complete set of tokens available to you or to add more custom tokens, talk to your administrator.</span></span> <span data-ttu-id="fdc23-306">Du kan finde tekniske oplysninger i [Tilføje filtertokens](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span><span class="sxs-lookup"><span data-stu-id="fdc23-306">For technical information see [Adding Filter Tokens](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span></span>

#### <a name="me-or-userid-records-assigned-to-you"></a><span data-ttu-id="fdc23-307">(%me eller %userid) Poster, der er tildelt til dig</span><span class="sxs-lookup"><span data-stu-id="fdc23-307">(%me or %userid) Records Assigned to You</span></span>

<span data-ttu-id="fdc23-308">Brug `%me` eller `%userid` ved filtrering af felter, der indeholder bruger-id'et, f.eks. feltet **Tildelt til bruger-id**, for at få vist alle poster, der er tildelt til dig.</span><span class="sxs-lookup"><span data-stu-id="fdc23-308">Use `%me` or `%userid` when filtering fields that contain the user ID, such as **Assigned to User ID** field, to display all records that are assigned to you.</span></span>

|<span data-ttu-id="fdc23-309">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fdc23-309">Sample Expression</span></span>|<span data-ttu-id="fdc23-310">Viste poster</span><span class="sxs-lookup"><span data-stu-id="fdc23-310">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%me`<br /><span data-ttu-id="fdc23-311">eller</span><span class="sxs-lookup"><span data-stu-id="fdc23-311">or</span></span><br />`%userid`|<span data-ttu-id="fdc23-312">Poster, der er knyttet til din brugerkonto.</span><span class="sxs-lookup"><span data-stu-id="fdc23-312">Records that are assigned to your user account.</span></span> |  

#### <a name="mycustomers-customers-in-my-customers"></a><span data-ttu-id="fdc23-313">(%mycustomers) Debitorer i Mine debitorer</span><span class="sxs-lookup"><span data-stu-id="fdc23-313">(%mycustomers) Customers in My Customers</span></span>

<span data-ttu-id="fdc23-314">Brug `%mycustomers` i debitorfeltet **Nej** til at vise alle poster for debitorer, der står på listen **Mine debitorer** i dit rollecenter.</span><span class="sxs-lookup"><span data-stu-id="fdc23-314">Use `%mycustomers` in the customer **No** field to display all records for customers that are included in the **My Customers** list on your Role Center.</span></span>

|<span data-ttu-id="fdc23-315">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fdc23-315">Sample Expression</span></span>|<span data-ttu-id="fdc23-316">Viste poster</span><span class="sxs-lookup"><span data-stu-id="fdc23-316">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%mycustomers`|<span data-ttu-id="fdc23-317">Debitorer i **Mine debitorer** i dit rollecenter.</span><span class="sxs-lookup"><span data-stu-id="fdc23-317">Customers in the **My Customers** on your Role Center.</span></span> |  

#### <a name="myitems-items-in-my-items"></a><span data-ttu-id="fdc23-318">(%myitems) Varer i Mine varer</span><span class="sxs-lookup"><span data-stu-id="fdc23-318">(%myitems) Items in My Items</span></span>

<span data-ttu-id="fdc23-319">Brug `%myitems` i varefeltet **Nej** til at vise alle poster for varer, der står på listen **Mine varer** i dit rollecenter.</span><span class="sxs-lookup"><span data-stu-id="fdc23-319">Use `%myitems` in the item **No** field to display all records for items that are included in the **My Items** list on your Role Center.</span></span>

|<span data-ttu-id="fdc23-320">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fdc23-320">Sample Expression</span></span>|<span data-ttu-id="fdc23-321">Viste poster</span><span class="sxs-lookup"><span data-stu-id="fdc23-321">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myitems`|<span data-ttu-id="fdc23-322">Varer i **Mine varer** i dit rollecenter.</span><span class="sxs-lookup"><span data-stu-id="fdc23-322">Items in the **My Items** on your Role Center.</span></span> |  

#### <a name="myvendors-vendors-in-my-vendors"></a><span data-ttu-id="fdc23-323">(%myvendors) Kreditorer i Mine kreditorer</span><span class="sxs-lookup"><span data-stu-id="fdc23-323">(%myvendors) Vendors in My Vendors</span></span>

<span data-ttu-id="fdc23-324">Brug `%myvendors` i kreditorfeltet **Nej** til at vise alle poster for kreditorer, der står på listen **Mine kreditor** i dit rollecenter.</span><span class="sxs-lookup"><span data-stu-id="fdc23-324">Use `%myvendors` in the vendor **No** field to display all records for vendors that are included in the **My Vendors** list on your Role Center.</span></span>

|<span data-ttu-id="fdc23-325">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fdc23-325">Sample Expression</span></span>|<span data-ttu-id="fdc23-326">Viste poster</span><span class="sxs-lookup"><span data-stu-id="fdc23-326">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myvendors`|<span data-ttu-id="fdc23-327">Kreditorer i **Mine kreditorer** i dit rollecenter.</span><span class="sxs-lookup"><span data-stu-id="fdc23-327">Vendors in the **My Vendors** on your Role Center.</span></span> |  

## <a name="see-also"></a><span data-ttu-id="fdc23-328">Se også</span><span class="sxs-lookup"><span data-stu-id="fdc23-328">See Also</span></span>

[<span data-ttu-id="fdc23-329">Ofte stillede spørgsmål om søgning og filtrering</span><span class="sxs-lookup"><span data-stu-id="fdc23-329">Searching and Filtering FAQ</span></span>](ui-search-filter-faq.md)  
[<span data-ttu-id="fdc23-330">Gemme og tilpasse listevisninger</span><span class="sxs-lookup"><span data-stu-id="fdc23-330">Save and Personalize List Views</span></span>](ui-views.md)  
<span data-ttu-id="fdc23-331">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fdc23-331">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]