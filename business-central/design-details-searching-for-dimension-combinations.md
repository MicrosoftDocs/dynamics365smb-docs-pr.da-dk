---
title: Designoplysninger – Søgning efter dimensionskombinationer | Microsoft Docs
description: Når du lukker en side, efter du har redigeret et sæt dimensioner, evaluerer Business Central, om det redigerede sæt dimensioner findes. Hvis det ikke findes, oprettes der et nyt sæt, og dimensionens kombinations-ID returneres.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: e118ad07537cdaa0d6ed526ab8e91461cd430f08
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303000"
---
# <a name="design-details-searching-for-dimension-combinations"></a><span data-ttu-id="d0cce-104">Designoplysninger: Søgning efter dimensionskombinationer</span><span class="sxs-lookup"><span data-stu-id="d0cce-104">Design Details: Searching for Dimension Combinations</span></span>
<span data-ttu-id="d0cce-105">Når du lukker en side, efter du har redigeret et sæt dimensioner, evaluerer [!INCLUDE[d365fin](includes/d365fin_md.md)], om det redigerede sæt dimensioner findes.</span><span class="sxs-lookup"><span data-stu-id="d0cce-105">When you close a page after you edit a set of dimensions, [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether the edited set of dimensions exists.</span></span> <span data-ttu-id="d0cce-106">Hvis det ikke findes, oprettes der et nyt sæt, og dimensionens kombinations-ID returneres.</span><span class="sxs-lookup"><span data-stu-id="d0cce-106">If the set does not exist, a new set is created and the dimension combination ID is returned.</span></span>  

## <a name="building-search-tree"></a><span data-ttu-id="d0cce-107">Oprettelse af søgetræ</span><span class="sxs-lookup"><span data-stu-id="d0cce-107">Building Search Tree</span></span>  
 <span data-ttu-id="d0cce-108">Tabel 481 **Trænode for dimensionsgruppe** bruges, når [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluerer, om der allerede findes et sæt dimensioner i tabel 480 **Dimensionsgruppepost**.</span><span class="sxs-lookup"><span data-stu-id="d0cce-108">Table 481 **Dimension Set Tree Node** is used when [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether a set of dimensions already exists in table 480 **Dimension Set Entry** table.</span></span> <span data-ttu-id="d0cce-109">Evalueringen udføres ved rekursivt at gennemgå søgningstræet startende på øverste niveau, der er nummereret 0.</span><span class="sxs-lookup"><span data-stu-id="d0cce-109">The evaluation is performed by recursively traversing the search tree starting at the top level numbered 0.</span></span> <span data-ttu-id="d0cce-110">Det øverste niveau 0 repræsenterer et dimensionssæt uden nogen dimensionssætposter.</span><span class="sxs-lookup"><span data-stu-id="d0cce-110">The top level 0 represents a dimension set with no dimension set entries.</span></span> <span data-ttu-id="d0cce-111">Underordnede til denne dimensionsgruppe repræsenterer dimensionsgrupper med kun én dimensionsgruppepost.</span><span class="sxs-lookup"><span data-stu-id="d0cce-111">The children of this dimension set represent dimension sets with only one dimension set entry.</span></span> <span data-ttu-id="d0cce-112">Underordnede til disse dimensionsgrupper repræsenterer dimensionsgruppe med to underordnede, osv.</span><span class="sxs-lookup"><span data-stu-id="d0cce-112">The children of these dimension sets represent dimension sets with two children, and so on.</span></span>  

### <a name="example-1"></a><span data-ttu-id="d0cce-113">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="d0cce-113">Example 1</span></span>  
 <span data-ttu-id="d0cce-114">I følgende diagram præsenteres et søgetræ med seks dimensionsgrupper.</span><span class="sxs-lookup"><span data-stu-id="d0cce-114">The following diagram represents a search tree with six dimension sets.</span></span> <span data-ttu-id="d0cce-115">Kun den distinkte dimensionsopsætningspost vises i diagrammet.</span><span class="sxs-lookup"><span data-stu-id="d0cce-115">Only the distinguishing dimension set entry is displayed in the diagram.</span></span>  

 <span data-ttu-id="d0cce-116">![Eksempel på træstruktur for dimension](media/nav2013_dimension_tree.png "Eksempel på træstruktur for dimension")</span><span class="sxs-lookup"><span data-stu-id="d0cce-116">![Example of dimension tree structure](media/nav2013_dimension_tree.png "Example of dimension tree structure")</span></span>  

 <span data-ttu-id="d0cce-117">I følgende tabel beskrives en komplet liste over dimensionsgruppeposter, der udgør hver dimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="d0cce-117">The following table describes a complete list of dimension set entries that make up each dimension set.</span></span>  

|<span data-ttu-id="d0cce-118">Dimensionsopsætninger</span><span class="sxs-lookup"><span data-stu-id="d0cce-118">Dimension Sets</span></span>|<span data-ttu-id="d0cce-119">Dimensionsgruppeposter</span><span class="sxs-lookup"><span data-stu-id="d0cce-119">Dimension Set Entries</span></span>|  
|--------------------|---------------------------|  
|<span data-ttu-id="d0cce-120">Gruppe 0</span><span class="sxs-lookup"><span data-stu-id="d0cce-120">Set 0</span></span>|<span data-ttu-id="d0cce-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="d0cce-121">None</span></span>|  
|<span data-ttu-id="d0cce-122">Gruppe 1</span><span class="sxs-lookup"><span data-stu-id="d0cce-122">Set 1</span></span>|<span data-ttu-id="d0cce-123">AREA 30</span><span class="sxs-lookup"><span data-stu-id="d0cce-123">AREA 30</span></span>|  
|<span data-ttu-id="d0cce-124">Gruppe 2</span><span class="sxs-lookup"><span data-stu-id="d0cce-124">Set 2</span></span>|<span data-ttu-id="d0cce-125">AREA 30, DEPT ADM</span><span class="sxs-lookup"><span data-stu-id="d0cce-125">AREA 30, DEPT ADM</span></span>|  
|<span data-ttu-id="d0cce-126">Gruppe 3</span><span class="sxs-lookup"><span data-stu-id="d0cce-126">Set 3</span></span>|<span data-ttu-id="d0cce-127">AREA 30, DEPT PROD</span><span class="sxs-lookup"><span data-stu-id="d0cce-127">AREA 30, DEPT PROD</span></span>|  
|<span data-ttu-id="d0cce-128">Gruppe 4</span><span class="sxs-lookup"><span data-stu-id="d0cce-128">Set 4</span></span>|<span data-ttu-id="d0cce-129">AREA 30, DEPT ADM, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="d0cce-129">AREA 30, DEPT ADM, PROJ VW</span></span>|  
|<span data-ttu-id="d0cce-130">Gruppe 5</span><span class="sxs-lookup"><span data-stu-id="d0cce-130">Set 5</span></span>|<span data-ttu-id="d0cce-131">AREA 40</span><span class="sxs-lookup"><span data-stu-id="d0cce-131">AREA 40</span></span>|  
|<span data-ttu-id="d0cce-132">Gruppe 6</span><span class="sxs-lookup"><span data-stu-id="d0cce-132">Set 6</span></span>|<span data-ttu-id="d0cce-133">AREA 40, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="d0cce-133">AREA 40, PROJ VW</span></span>|  

### <a name="example-2"></a><span data-ttu-id="d0cce-134">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="d0cce-134">Example 2</span></span>  
 <span data-ttu-id="d0cce-135">Dette eksempel viser, hvordan [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluerer, om en dimensionsgruppe, der består af dimensionsgruppeposterne AREA 40, DEPT PROD, findes.</span><span class="sxs-lookup"><span data-stu-id="d0cce-135">This example shows how [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether a dimension set that consists of the dimension set entries AREA 40, DEPT PROD exists.</span></span>  

 <span data-ttu-id="d0cce-136">Først opdaterer [!INCLUDE[d365fin](includes/d365fin_md.md)] også tabellen **Trænode for dimensionsgruppe** for at sikre, at søgetræet ligner følgende diagram.</span><span class="sxs-lookup"><span data-stu-id="d0cce-136">First, [!INCLUDE[d365fin](includes/d365fin_md.md)] also updates the **Dimension Set Tree Node** table to make sure that the search tree looks like the following diagram.</span></span> <span data-ttu-id="d0cce-137">Dermed bliver dimensionsgruppe 7 underordnet dimensionsgruppe 5.</span><span class="sxs-lookup"><span data-stu-id="d0cce-137">Thus dimension set 7 becomes a child of the dimension set 5.</span></span>  

 <span data-ttu-id="d0cce-138">![Eksempel på træstruktur for dimension i NAV 2013](media/nav2013_dimension_tree_example2.png "Eksempel på træstruktur for dimension i NAV 2013")</span><span class="sxs-lookup"><span data-stu-id="d0cce-138">![Example of dimension tree structure in NAV 2013](media/nav2013_dimension_tree_example2.png "Example of dimension tree structure in NAV 2013")</span></span>  

### <a name="finding-dimension-set-id"></a><span data-ttu-id="d0cce-139">Søgning efter dimensionsgruppe-id</span><span class="sxs-lookup"><span data-stu-id="d0cce-139">Finding Dimension Set ID</span></span>  
 <span data-ttu-id="d0cce-140">På et konceptuelt niveau kombineres og bruges **Overordnet id**, **Dimension** og **Dimensionsværdi** i søgetræet som den primære nøgle, fordi [!INCLUDE[d365fin](includes/d365fin_md.md)] gennemgår træet i samme rækkefølge som dimensionsposterne.</span><span class="sxs-lookup"><span data-stu-id="d0cce-140">At a conceptual level, **Parent ID**, **Dimension**, and **Dimension Value**, in the search tree, are combined and used as the primary key because [!INCLUDE[d365fin](includes/d365fin_md.md)] traverses the tree in the same order as the dimension entries.</span></span> <span data-ttu-id="d0cce-141">Funktionen GET (post) bruges til at søge efter dimensionsgruppe-id.</span><span class="sxs-lookup"><span data-stu-id="d0cce-141">The GET function (record) is used to search for dimension set ID.</span></span> <span data-ttu-id="d0cce-142">Følgende kodeeksempel viser, hvordan du kan finde dimensionsgruppe-id, når der er tre dimensionsværdier.</span><span class="sxs-lookup"><span data-stu-id="d0cce-142">The following code example shows how to find the dimension set ID when there are three dimension values.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

<span data-ttu-id="d0cce-143">Men for at bevare muligheden for, at [!INCLUDE[d365fin](includes/d365fin_md.md)] kan omdøbe både en dimension og en dimensionsværdi, er tabel 349, **Dimensionsværdi**, udvidet med et heltalsfelt, **Dimensionsværdi-id**.</span><span class="sxs-lookup"><span data-stu-id="d0cce-143">However, to preserve the ability of [!INCLUDE[d365fin](includes/d365fin_md.md)] to rename both a dimension and a dimension value, table 349, **Dimension Value**, is extended with an integer field, **Dimension Value ID**.</span></span> <span data-ttu-id="d0cce-144">Denne tabel konverterer feltparret, **Dimension** og **Dimensionsværdi**, til en heltalsværdi.</span><span class="sxs-lookup"><span data-stu-id="d0cce-144">This table converts the field pair, **Dimension** and **Dimension Value**, to an integer value.</span></span> <span data-ttu-id="d0cce-145">Heltalsværdien ændres ikke, når du omdøber dimensionen og dimensionsværdien.</span><span class="sxs-lookup"><span data-stu-id="d0cce-145">When you rename the dimension and dimension value, the integer value is not changed.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a><span data-ttu-id="d0cce-146">Se også</span><span class="sxs-lookup"><span data-stu-id="d0cce-146">See Also</span></span>  
 <span data-ttu-id="d0cce-147">[Funktionen GET (post)](/dynamics-nav/GET-Function--Record-)  </span><span class="sxs-lookup"><span data-stu-id="d0cce-147">[GET Function (Record)](/dynamics-nav/GET-Function--Record-)  </span></span>  
 <span data-ttu-id="d0cce-148">[Designoplysninger: Dimensionsgruppeposter](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="d0cce-148">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="d0cce-149">[Oversigt over dimensionsgruppeposter](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="d0cce-149">[Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 [<span data-ttu-id="d0cce-150">Designoplysninger: Tabelstruktur</span><span class="sxs-lookup"><span data-stu-id="d0cce-150">Design Details: Table Structure</span></span>](design-details-table-structure.md)   
 
