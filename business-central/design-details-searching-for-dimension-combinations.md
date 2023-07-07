---
title: Designoplysninger – Søgning efter dimensionskombinationer | Microsoft Docs
description: 'Når du lukker en side, efter du har redigeret et sæt dimensioner, evaluerer Business Central, om det redigerede sæt dimensioner findes. Hvis det ikke findes, oprettes der et nyt sæt, og dimensionens kombinations-ID returneres.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-searching-for-dimension-combinations"></a>Designoplysninger: Søgning efter dimensionskombinationer
Når du lukker en side, efter du har redigeret et sæt dimensioner, evaluerer [!INCLUDE[prod_short](includes/prod_short.md)], om det redigerede sæt dimensioner findes. Hvis det ikke findes, oprettes der et nyt sæt, og dimensionens kombinations-ID returneres.  

## <a name="building-search-tree"></a>Oprettelse af søgetræ
 Tabel 481 **Trænode for dimensionsgruppe** bruges, når [!INCLUDE[prod_short](includes/prod_short.md)] evaluerer, om der allerede findes et sæt dimensioner i tabel 480 **Dimensionsgruppepost**. Evalueringen udføres ved rekursivt at gennemgå søgningstræet startende på øverste niveau, der er nummereret 0. Det øverste niveau 0 repræsenterer et dimensionssæt uden nogen dimensionssætposter. Underordnede til denne dimensionsgruppe repræsenterer dimensionsgrupper med kun én dimensionsgruppepost. Underordnede til disse dimensionsgrupper repræsenterer dimensionsgruppe med to underordnede, osv.  

### <a name="example-1"></a>Eksempel 1
 I følgende diagram præsenteres et søgetræ med seks dimensionsgrupper. Kun den distinkte dimensionsopsætningspost vises i diagrammet.  

 ![Eksempel på dimensionstræstruktur.](media/nav2013_dimension_tree.png "Eksempel på dimensionstræstruktur")  

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
 Dette eksempel viser, hvordan [!INCLUDE[prod_short](includes/prod_short.md)] evaluerer, om en dimensionsgruppe, der består af dimensionsgruppeposterne AREA 40, DEPT PROD, findes.  

 Først opdaterer [!INCLUDE[prod_short](includes/prod_short.md)] også tabellen **Trænode for dimensionsgruppe** for at sikre, at søgetræet ligner følgende diagram. Dermed bliver dimensionsgruppe 7 underordnet dimensionsgruppe 5.  

 ![Eksempel på dimensionstræstruktur i NAV 2013.](media/nav2013_dimension_tree_example2.png "Eksempel på dimensionstræstruktur i NAV 2013")  

### <a name="finding-dimension-set-id"></a>Søgning efter dimensionsgruppe-id
 På et konceptuelt niveau kombineres og bruges **Overordnet id**, **Dimension** og **Dimensionsværdi** i søgetræet som den primære nøgle, fordi [!INCLUDE[prod_short](includes/prod_short.md)] gennemgår træet i samme rækkefølge som dimensionsposterne. Funktionen GET (post) bruges til at søge efter dimensionsgruppe-id. Følgende kodeeksempel viser, hvordan du kan finde dimensionsgruppe-id, når der er tre dimensionsværdier.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

Men for at bevare muligheden for, at [!INCLUDE[prod_short](includes/prod_short.md)] kan omdøbe både en dimension og en dimensionsværdi, er tabel 349, **Dimensionsværdi**, udvidet med et heltalsfelt, **Dimensionsværdi-id**. Denne tabel konverterer feltparret, **Dimension** og **Dimensionsværdi**, til en heltalsværdi. Heltalsværdien ændres ikke, når du omdøber dimensionen og dimensionsværdien.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a>Se også
    
 [Designoplysninger: Dimensionsgruppeposter](/dynamics365/business-central/design-details-dimension-set-entries-overview)   
 [Oversigt over dimensionsgruppeposter](design-details-dimension-set-entries-overview.md)   
 [Designoplysninger: Tabelstruktur](design-details-table-structure.md)   
 


[!INCLUDE[footer-include](includes/footer-banner.md)]
