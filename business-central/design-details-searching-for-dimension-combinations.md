---
title: Designoplysninger – Søgning efter dimensionskombinationer | Microsoft Docs
description: Når du lukker en side, efter du har redigeret et sæt dimensioner, evaluerer Business Central, om det redigerede sæt dimensioner findes. Hvis det ikke findes, oprettes der et nyt sæt, og dimensionens kombinations-ID returneres.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cc5b128d3e9655697b5dc3a2176dcfe926442bc8
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388620"
---
# <a name="design-details-searching-for-dimension-combinations"></a><span data-ttu-id="5d6e4-104">Designoplysninger: Søgning efter dimensionskombinationer</span><span class="sxs-lookup"><span data-stu-id="5d6e4-104">Design Details: Searching for Dimension Combinations</span></span>
<span data-ttu-id="5d6e4-105">Når du lukker en side, efter du har redigeret et sæt dimensioner, evaluerer [!INCLUDE[prod_short](includes/prod_short.md)], om det redigerede sæt dimensioner findes.</span><span class="sxs-lookup"><span data-stu-id="5d6e4-105">When you close a page after you edit a set of dimensions, [!INCLUDE[prod_short](includes/prod_short.md)] evaluates whether the edited set of dimensions exists.</span></span> <span data-ttu-id="5d6e4-106">Hvis det ikke findes, oprettes der et nyt sæt, og dimensionens kombinations-ID returneres.</span><span class="sxs-lookup"><span data-stu-id="5d6e4-106">If the set does not exist, a new set is created and the dimension combination ID is returned.</span></span>  

## <a name="building-search-tree"></a><span data-ttu-id="5d6e4-107">Oprettelse af søgetræ</span><span class="sxs-lookup"><span data-stu-id="5d6e4-107">Building Search Tree</span></span>  
 <span data-ttu-id="5d6e4-108">Tabel 481 **Trænode for dimensionsgruppe** bruges, når [!INCLUDE[prod_short](includes/prod_short.md)] evaluerer, om der allerede findes et sæt dimensioner i tabel 480 **Dimensionsgruppepost**.</span><span class="sxs-lookup"><span data-stu-id="5d6e4-108">Table 481 **Dimension Set Tree Node** is used when [!INCLUDE[prod_short](includes/prod_short.md)] evaluates whether a set of dimensions already exists in table 480 **Dimension Set Entry** table.</span></span> <span data-ttu-id="5d6e4-109">Evalueringen udføres ved rekursivt at gennemgå søgningstræet startende på øverste niveau, der er nummereret 0.</span><span class="sxs-lookup"><span data-stu-id="5d6e4-109">The evaluation is performed by recursively traversing the search tree starting at the top level numbered 0.</span></span> <span data-ttu-id="5d6e4-110">Det øverste niveau 0 repræsenterer et dimensionssæt uden nogen dimensionssætposter.</span><span class="sxs-lookup"><span data-stu-id="5d6e4-110">The top level 0 represents a dimension set with no dimension set entries.</span></span> <span data-ttu-id="5d6e4-111">Underordnede til denne dimensionsgruppe repræsenterer dimensionsgrupper med kun én dimensionsgruppepost.</span><span class="sxs-lookup"><span data-stu-id="5d6e4-111">The children of this dimension set represent dimension sets with only one dimension set entry.</span></span> <span data-ttu-id="5d6e4-112">Underordnede til disse dimensionsgrupper repræsenterer dimensionsgruppe med to underordnede, osv.</span><span class="sxs-lookup"><span data-stu-id="5d6e4-112">The children of these dimension sets represent dimension sets with two children, and so on.</span></span>  

### <a name="example-1"></a><span data-ttu-id="5d6e4-113">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="5d6e4-113">Example 1</span></span>  
 <span data-ttu-id="5d6e4-114">I følgende diagram præsenteres et søgetræ med seks dimensionsgrupper.</span><span class="sxs-lookup"><span data-stu-id="5d6e4-114">The following diagram represents a search tree with six dimension sets.</span></span> <span data-ttu-id="5d6e4-115">Kun den distinkte dimensionsopsætningspost vises i diagrammet.</span><span class="sxs-lookup"><span data-stu-id="5d6e4-115">Only the distinguishing dimension set entry is displayed in the diagram.</span></span>  

 <span data-ttu-id="5d6e4-116">![Eksempel på dimensionstræstruktur](media/nav2013_dimension_tree.png "Eksempel på dimensionstræstruktur")</span><span class="sxs-lookup"><span data-stu-id="5d6e4-116">![Example of dimension tree structure](media/nav2013_dimension_tree.png "Example of dimension tree structure")</span></span>  

 <span data-ttu-id="5d6e4-117">I følgende tabel beskrives en komplet liste over dimensionsgruppeposter, der udgør hver dimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="5d6e4-117">The following table describes a complete list of dimension set entries that make up each dimension set.</span></span>  

|<span data-ttu-id="5d6e4-118">Dimensionsopsætninger</span><span class="sxs-lookup"><span data-stu-id="5d6e4-118">Dimension Sets</span></span>|<span data-ttu-id="5d6e4-119">Dimensionsgruppeposter</span><span class="sxs-lookup"><span data-stu-id="5d6e4-119">Dimension Set Entries</span></span>|  
|--------------------|---------------------------|  
|<span data-ttu-id="5d6e4-120">Gruppe 0</span><span class="sxs-lookup"><span data-stu-id="5d6e4-120">Set 0</span></span>|<span data-ttu-id="5d6e4-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="5d6e4-121">None</span></span>|  
|<span data-ttu-id="5d6e4-122">Gruppe 1</span><span class="sxs-lookup"><span data-stu-id="5d6e4-122">Set 1</span></span>|<span data-ttu-id="5d6e4-123">AREA 30</span><span class="sxs-lookup"><span data-stu-id="5d6e4-123">AREA 30</span></span>|  
|<span data-ttu-id="5d6e4-124">Gruppe 2</span><span class="sxs-lookup"><span data-stu-id="5d6e4-124">Set 2</span></span>|<span data-ttu-id="5d6e4-125">AREA 30, DEPT ADM</span><span class="sxs-lookup"><span data-stu-id="5d6e4-125">AREA 30, DEPT ADM</span></span>|  
|<span data-ttu-id="5d6e4-126">Gruppe 3</span><span class="sxs-lookup"><span data-stu-id="5d6e4-126">Set 3</span></span>|<span data-ttu-id="5d6e4-127">AREA 30, DEPT PROD</span><span class="sxs-lookup"><span data-stu-id="5d6e4-127">AREA 30, DEPT PROD</span></span>|  
|<span data-ttu-id="5d6e4-128">Gruppe 4</span><span class="sxs-lookup"><span data-stu-id="5d6e4-128">Set 4</span></span>|<span data-ttu-id="5d6e4-129">AREA 30, DEPT ADM, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="5d6e4-129">AREA 30, DEPT ADM, PROJ VW</span></span>|  
|<span data-ttu-id="5d6e4-130">Gruppe 5</span><span class="sxs-lookup"><span data-stu-id="5d6e4-130">Set 5</span></span>|<span data-ttu-id="5d6e4-131">AREA 40</span><span class="sxs-lookup"><span data-stu-id="5d6e4-131">AREA 40</span></span>|  
|<span data-ttu-id="5d6e4-132">Gruppe 6</span><span class="sxs-lookup"><span data-stu-id="5d6e4-132">Set 6</span></span>|<span data-ttu-id="5d6e4-133">AREA 40, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="5d6e4-133">AREA 40, PROJ VW</span></span>|  

### <a name="example-2"></a><span data-ttu-id="5d6e4-134">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="5d6e4-134">Example 2</span></span>  
 <span data-ttu-id="5d6e4-135">Dette eksempel viser, hvordan [!INCLUDE[prod_short](includes/prod_short.md)] evaluerer, om en dimensionsgruppe, der består af dimensionsgruppeposterne AREA 40, DEPT PROD, findes.</span><span class="sxs-lookup"><span data-stu-id="5d6e4-135">This example shows how [!INCLUDE[prod_short](includes/prod_short.md)] evaluates whether a dimension set that consists of the dimension set entries AREA 40, DEPT PROD exists.</span></span>  

 <span data-ttu-id="5d6e4-136">Først opdaterer [!INCLUDE[prod_short](includes/prod_short.md)] også tabellen **Trænode for dimensionsgruppe** for at sikre, at søgetræet ligner følgende diagram.</span><span class="sxs-lookup"><span data-stu-id="5d6e4-136">First, [!INCLUDE[prod_short](includes/prod_short.md)] also updates the **Dimension Set Tree Node** table to make sure that the search tree looks like the following diagram.</span></span> <span data-ttu-id="5d6e4-137">Dermed bliver dimensionsgruppe 7 underordnet dimensionsgruppe 5.</span><span class="sxs-lookup"><span data-stu-id="5d6e4-137">Thus dimension set 7 becomes a child of the dimension set 5.</span></span>  

 <span data-ttu-id="5d6e4-138">![Eksempel på dimensionstræstruktur i NAV 2013](media/nav2013_dimension_tree_example2.png "Eksempel på dimensionstræstruktur i NAV 2013")</span><span class="sxs-lookup"><span data-stu-id="5d6e4-138">![Example of dimension tree structure in NAV 2013](media/nav2013_dimension_tree_example2.png "Example of dimension tree structure in NAV 2013")</span></span>  

### <a name="finding-dimension-set-id"></a><span data-ttu-id="5d6e4-139">Søgning efter dimensionsgruppe-id</span><span class="sxs-lookup"><span data-stu-id="5d6e4-139">Finding Dimension Set ID</span></span>  
 <span data-ttu-id="5d6e4-140">På et konceptuelt niveau kombineres og bruges **Overordnet id**, **Dimension** og **Dimensionsværdi** i søgetræet som den primære nøgle, fordi [!INCLUDE[prod_short](includes/prod_short.md)] gennemgår træet i samme rækkefølge som dimensionsposterne.</span><span class="sxs-lookup"><span data-stu-id="5d6e4-140">At a conceptual level, **Parent ID**, **Dimension**, and **Dimension Value**, in the search tree, are combined and used as the primary key because [!INCLUDE[prod_short](includes/prod_short.md)] traverses the tree in the same order as the dimension entries.</span></span> <span data-ttu-id="5d6e4-141">Funktionen GET (post) bruges til at søge efter dimensionsgruppe-id.</span><span class="sxs-lookup"><span data-stu-id="5d6e4-141">The GET function (record) is used to search for dimension set ID.</span></span> <span data-ttu-id="5d6e4-142">Følgende kodeeksempel viser, hvordan du kan finde dimensionsgruppe-id, når der er tre dimensionsværdier.</span><span class="sxs-lookup"><span data-stu-id="5d6e4-142">The following code example shows how to find the dimension set ID when there are three dimension values.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

<span data-ttu-id="5d6e4-143">Men for at bevare muligheden for, at [!INCLUDE[prod_short](includes/prod_short.md)] kan omdøbe både en dimension og en dimensionsværdi, er tabel 349, **Dimensionsværdi**, udvidet med et heltalsfelt, **Dimensionsværdi-id**.</span><span class="sxs-lookup"><span data-stu-id="5d6e4-143">However, to preserve the ability of [!INCLUDE[prod_short](includes/prod_short.md)] to rename both a dimension and a dimension value, table 349, **Dimension Value**, is extended with an integer field, **Dimension Value ID**.</span></span> <span data-ttu-id="5d6e4-144">Denne tabel konverterer feltparret, **Dimension** og **Dimensionsværdi**, til en heltalsværdi.</span><span class="sxs-lookup"><span data-stu-id="5d6e4-144">This table converts the field pair, **Dimension** and **Dimension Value**, to an integer value.</span></span> <span data-ttu-id="5d6e4-145">Heltalsværdien ændres ikke, når du omdøber dimensionen og dimensionsværdien.</span><span class="sxs-lookup"><span data-stu-id="5d6e4-145">When you rename the dimension and dimension value, the integer value is not changed.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a><span data-ttu-id="5d6e4-146">Se også</span><span class="sxs-lookup"><span data-stu-id="5d6e4-146">See Also</span></span>  
 <span data-ttu-id="5d6e4-147">[Funktionen GET (post)](/dynamics-nav/GET-Function--Record-)  </span><span class="sxs-lookup"><span data-stu-id="5d6e4-147">[GET Function (Record)](/dynamics-nav/GET-Function--Record-)  </span></span>  
 <span data-ttu-id="5d6e4-148">[Designoplysninger: Dimensionsgruppeposter](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="5d6e4-148">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="5d6e4-149">[Oversigt over dimensionsgruppeposter](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="5d6e4-149">[Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 [<span data-ttu-id="5d6e4-150">Designoplysninger: Tabelstruktur</span><span class="sxs-lookup"><span data-stu-id="5d6e4-150">Design Details: Table Structure</span></span>](design-details-table-structure.md)   
 


[!INCLUDE[footer-include](includes/footer-banner.md)]