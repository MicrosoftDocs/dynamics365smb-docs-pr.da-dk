---
title: "Designoplysninger – Kodeenhed 408 Dimensionsstyring | Microsoft Docs"
description: "Kodeenhed 408-dimensionsstyring er et funktionsbibliotek, der håndterer almindelige opgaver, der er relateret til dimensioner, som f.eks. kopiering fra én tabel til en anden eller fra et dokument til en andet."
services: project-madeira
documentationcenter: 
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a811c565a8eb0ce774d35d15776e65b6dce6a31a
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-codeunit-408-dimension-management"></a>Designoplysninger: Kodeenhed 408 Dimensionsstyring
Kodeenhed 408-dimensionsstyring er et funktionsbibliotek, der håndterer almindelige opgaver, der er relateret til dimensioner, som f.eks. kopiering fra én tabel til en anden eller fra et dokument til en andet. I dette emne beskrives de funktioner, der er ændret i Microsoft Dynamics NAV 2013 R2, og hvad der skal gøres ved funktionerne. Mange funktioner er slettet, fordi der er ingen grund til at kopiere mellem dimensionstabeller.  

## <a name="modified-functions"></a>Ændrede funktioner  

|Funktionsnavn|Beskrivelse af ændring|  
|-------------------|------------------------------|  
|CheckDimSetIDComb|Ny funktion, der erstatter de andre kontrolfunktioner og tager et dimensionsgruppe-id som argument i stedet for en dimensionstabel.|  
|CheckDimSetIDComb<br /><br /> CheckDocDimComb<br /><br /> CheckServContractDimComb<br /><br /> CheckDimBuffer<br /><br /> CheckDimComb<br /><br /> CheckDimValueComb|Slet. Alt forbrug skal ændres til CheckDimSetIDComb.|  
|GetDefaultDim|Rediger for at returnere et heltal som dimensionsgruppe-id i stedet for et sæt poster.|  
|CopyJnlLineDimToICJnlDim<br /><br /> CopyICJnlDimToJnlLineDim<br /><br /> CopyDocDimtoICDocDim<br /><br /> CopyICDocDimtoICDocDim|Rediger for at arbejde med DimSetID -> ICJnlLineDim|  

## <a name="deleted-functions"></a>Slettede funktioner  
 Funktioner, der slettes fra codeunit 408 i forbindelse med funktionen Angiv dimensionsposter er angivet nedenfor.  

> [!CAUTION]  
>  Under opgradering af programkode fra Microsoft Dynamics NAV 2009 eller tidligere versioner til Microsoft Dynamics NAV 2016, er følgende funktioner ikke tilgængelige i Microsoft Dynamics NAV 2016. Hvis du har tilpasninger, der bruger en eller flere af funktionerne, skal du opgraderer denne kode i overensstemmelse hermed.

 InsertJnlLineDim  

 UpdateJnlLineDefaultDim  

 GetJnlLineDefaultDim  

 GetPreviousDocDefaultDim  

 GetPreviousProdDocDefaultDim  

 InsertDocDim  

 UpdateDocDefaultDim  

 ExtractDocDefaultDim  

 InsertProdDocDim  

 UpdateProdDocDefaultDim  

 InsertServContractDim  

 UpdateServcontractDim  

 UpdateDefaultDimNewDimValue  

 GetDocDim  

 GetProdDocDim  

 TypeToTableID1  

 TypeToTableID2  

 TypeToTableID3  

 TypeToTableID4  

 TypeToTableID5  

 DeleteJnlLineDim  

 DeleteDocDim  

 DeletePostedDocDim  

 DeleteProdDocDim  

 DeleteServContractDim  

 ShowJnlLineDim  

 SaveJnlLineDim  

 ShowJnlLineNewDim  

 SaveJnlLineNewDim  

 ShowDocDim  

 SaveDocDim  

 ShowProdDocDim  

 SaveProdDocDim  

 ShowTempDim  

 SaveTempDim  

 ShowTempNewDim  

 SaveTempNewDim  

 SaveServContractDim  

 MoveJnlLineDimToLedgEntryDim  

 MoveDocDimToPostedDocDim  

 MoveOneDocDimToPostedDocDim  

 MoveLedgEntryDimToJnlLineDim  

 MoveDimBufToJnlLineDim  

 MoveDimBufToLedgEntryDim  

 MoveDimBufToPostedDocDim  

 MoveDimBufToGLBudgetDim  

 CopyJnlLineDimToJnlLineDim  

 CopyLedgEntryDimToJnlLineDim  

 CopyDocDimToDocDim  

 CopyPostedDocDimToPostedDocDim  

 CopyDocDimToJnlLineDim  

 CopyDimBufToJnlLineDim  

 CopyDimBufToDocDim  

 CopySCDimToDocDim  

 MoveDocDimToLedgEntryDim  

 MoveDocDimToDocDim  

 MoveDocDimArchvToDocDim  

 MoveLedgEntryDimToDocDim  

 MoveProdDocDimToProdDocDim  

 MoveJnlLineDimToProdDocDim  

 MoveJnlLineDimToDocDim  

 MoveJnlLineDimToJnlLineDim  

 CopyLedgEntryDimToLedgEntryDim  

 MoveTempFromDimToTempToDim  

 TransferTempToDimToDocDim  

 MoveJnlLineDimToBuf  

 CopyICJnlDimToICJnlDim  

 TestDimValue  

 TestNewDimValue  

 MoveDimBufToItemBudgetDim. (Slet, fordi tabellen ItemBudgetDim er slettet.  

 GetServContractDim  

 MoveTempDimToBuf  

 UpdateSCInvLineDim  

 CopyJnlLineDimToBuffer  

 UpdateDocDefaultDim2  

## <a name="see-also"></a>Se også
 [Designoplysninger: Dimensionsgruppeposter](design-details-dimension-set-entries.md)   
 [Designoplysninger: Oversigt over dimensionsgruppeposter](design-details-dimension-set-entries-overview.md)   
 [Designoplysninger: Søgning efter dimensionskombinationer](design-details-searching-for-dimension-combinations.md)   
 [Designoplysninger: Tabelstruktur](design-details-table-structure.md)   
 [Designoplysninger: Kodeeksempler af ændrede mønstre i Ændringer](design-details-code-examples-of-changed-patterns-in-modifications.md)

