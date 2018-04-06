---
title: "Designoplysninger – Søgning efter dimensionskombinationer | Microsoft Docs"
description: "Når du lukker et vindue, efter du har redigeret et sæt dimensioner, evaluerer Finance and Operations, Business edition, om det redigerede sæt dimensioner findes. Hvis det ikke findes, oprettes der et nyt sæt, og dimensionens kombinations-ID returneres."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 821ddebee02d1ea922c0c13a181ae0e29e4eb40e
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-searching-for-dimension-combinations"></a>Designoplysninger: Søgning efter dimensionskombinationer
Når du lukker et vindue, efter du har redigeret et sæt dimensioner, evaluerer [!INCLUDE[d365fin](includes/d365fin_md.md)], om det redigerede sæt dimensioner findes. Hvis det ikke findes, oprettes der et nyt sæt, og dimensionens kombinations-ID returneres.  

## <a name="building-search-tree"></a>Oprettelse af søgetræ  
 Tabel 481 **Trænode for dimensionsgruppe** bruges, når [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluerer, om der allerede findes et sæt dimensioner i tabel 480 **Dimensionsgruppepost**. Evalueringen udføres ved rekursivt at gennemgå søgningstræet startende på øverste niveau, der er nummereret 0. Det øverste niveau 0 repræsenterer et dimensionssæt uden nogen dimensionssætposter. Underordnede til denne dimensionsgruppe repræsenterer dimensionsgrupper med kun én dimensionsgruppepost. Underordnede til disse dimensionsgrupper repræsenterer dimensionsgruppe med to underordnede, osv.  

### <a name="example-1"></a>Eksempel 1  
 I følgende diagram præsenteres et søgetræ med seks dimensionsgrupper. Kun den distinkte dimensionsopsætningspost vises i diagrammet.  

 ![Træstruktur for dimension](media/nav2013_dimension_tree.png "NAV2013_Dimension_Tree")  

 I følgende tabel beskrives en komplet liste over dimensionsgruppeposter, der udgør hver dimensionsgruppe.  

|Dimensionsopsætninger|Dimensionsgruppeposter|  
|--------------------|---------------------------|  
|Gruppe 0|Ingen|  
|Gruppe 1|AREA 30|  
|Gruppe 2|AREA 30, DEPT ADM|  
|Gruppe 3|AREA 30, DEPT PROD|  
|Gruppe 4|AREA 30, DEPT ADM, PROJ VW|  
|Gruppe 5|AREA 40|  
|Gruppe 6|AREA 40, PROJ VW|  

### <a name="example-2"></a>Eksempel 2  
 Dette eksempel viser, hvordan [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluerer, om en dimensionsgruppe, der består af dimensionsgruppeposterne AREA 40, DEPT PROD, findes.  

 Først opdaterer [!INCLUDE[d365fin](includes/d365fin_md.md)] også tabellen **Trænode for dimensionsgruppe** for at sikre, at søgetræet ligner følgende diagram. Dermed bliver dimensionsgruppe 7 underordnet dimensionsgruppe 5.  

 ![NAV2013&#95;Dimension&#95;Tree&#95;Example 2](media/nav2013_dimension_tree_example2.png "NAV2013_Dimension_Tree_Example2")  

### <a name="finding-dimension-set-id"></a>Søgning efter dimensionsgruppe-id  
 På et konceptuelt niveau kombineres og bruges **Overordnet id**, **Dimension** og **Dimensionsværdi** i søgetræet som den primære nøgle, fordi [!INCLUDE[d365fin](includes/d365fin_md.md)] gennemgår træet i samme rækkefølge som dimensionsposterne. Funktionen GET (post) bruges til at søge efter dimensionsgruppe-id. Følgende kodeeksempel viser, hvordan du kan finde dimensionsgruppe-id, når der er tre dimensionsværdier.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

 Men for at bevare muligheden for, at [!INCLUDE[d365fin](includes/d365fin_md.md)] kan omdøbe en dimension og dimensionsværdi, er tabel 348 **Dimensionsværdi** udvidet med et heltalsfelt for **Dimensionsværdi-id**. Denne tabel konverterer feltparret **Dimension** og **Dimensionsværdi** til en heltalsværdi. Heltalsværdien ændres ikke, når du omdøber dimensionen og dimensionsværdien.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a>Se også  
 [Funktionen GET (post)](/dynamics-nav/GET-Function--Record-)    
 [Designoplysninger: Dimensionsgruppeposter](design-details-dimension-set-entries.md)   
 [Oversigt over dimensionsgruppeposter](design-details-dimension-set-entries-overview.md)   
 [Designoplysninger: Tabelstruktur](design-details-table-structure.md)   
 [Designoplysninger: Kodeenhed 408 Dimensionsstyring](design-details-codeunit-408-dimension-management.md)   
 [Designoplysninger: Kodeeksempler af ændrede mønstre i Ændringer](design-details-code-examples-of-changed-patterns-in-modifications.md)

