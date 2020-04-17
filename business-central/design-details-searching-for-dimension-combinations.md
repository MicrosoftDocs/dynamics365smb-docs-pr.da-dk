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
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 3fe943fd3c2925f1c80107e23b389cd09958a47b
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3184696"
---
# <a name="design-details-searching-for-dimension-combinations"></a>Designoplysninger: Søgning efter dimensionskombinationer
Når du lukker en side, efter du har redigeret et sæt dimensioner, evaluerer [!INCLUDE[d365fin](includes/d365fin_md.md)], om det redigerede sæt dimensioner findes. Hvis det ikke findes, oprettes der et nyt sæt, og dimensionens kombinations-ID returneres.  

## <a name="building-search-tree"></a>Oprettelse af søgetræ  
 Tabel 481 **Trænode for dimensionsgruppe** bruges, når [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluerer, om der allerede findes et sæt dimensioner i tabel 480 **Dimensionsgruppepost**. Evalueringen udføres ved rekursivt at gennemgå søgningstræet startende på øverste niveau, der er nummereret 0. Det øverste niveau 0 repræsenterer et dimensionssæt uden nogen dimensionssætposter. Underordnede til denne dimensionsgruppe repræsenterer dimensionsgrupper med kun én dimensionsgruppepost. Underordnede til disse dimensionsgrupper repræsenterer dimensionsgruppe med to underordnede, osv.  

### <a name="example-1"></a>Eksempel 1  
 I følgende diagram præsenteres et søgetræ med seks dimensionsgrupper. Kun den distinkte dimensionsopsætningspost vises i diagrammet.  

 ![Eksempel på dimensionstræstruktur](media/nav2013_dimension_tree.png "Eksempel på dimensionstræstruktur")  

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

 ![Eksempel på dimensionstræstruktur i NAV 2013](media/nav2013_dimension_tree_example2.png "Eksempel på dimensionstræstruktur i NAV 2013")  

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

Men for at bevare muligheden for, at [!INCLUDE[d365fin](includes/d365fin_md.md)] kan omdøbe både en dimension og en dimensionsværdi, er tabel 349, **Dimensionsværdi**, udvidet med et heltalsfelt, **Dimensionsværdi-id**. Denne tabel konverterer feltparret, **Dimension** og **Dimensionsværdi**, til en heltalsværdi. Heltalsværdien ændres ikke, når du omdøber dimensionen og dimensionsværdien.  

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
 
