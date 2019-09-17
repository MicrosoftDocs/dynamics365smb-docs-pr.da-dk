---
title: Designoplysninger - Kodeeksempler af ændrede mønstre i Ændringer | Microsoft Docs
description: Kodeeksempler, der viser ændrede mønstre i dimensionskodeændring og overflytning for fem forskellige scenarier. Det sammenligner kodeeksempler i tidligere versioner med kodeeksempler i Business Central.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-dimension-set-entries
ms.openlocfilehash: 59fce0a432c7f433552cff21ef304fa16fa85a8a
ms.sourcegitcommit: 1fa3d33db7bc71e3a27c826308a80ff24a436a72
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/30/2019
ms.locfileid: "1970897"
---
# <a name="design-details-code-examples-of-changed-patterns-in-modifications"></a><span data-ttu-id="9b409-104">Designoplysninger: Kodeeksempler af ændrede mønstre i Ændringer</span><span class="sxs-lookup"><span data-stu-id="9b409-104">Design Details: Code Examples of Changed Patterns in Modifications</span></span>
<span data-ttu-id="9b409-105">Dette emne indeholder kodeeksempler til at vise ændrede mønstre i dimensionskodeændring og overflytning for fem forskellige scenarier.</span><span class="sxs-lookup"><span data-stu-id="9b409-105">This topic provides code examples to show changed patterns in dimension code modification and migration for five different scenarios.</span></span> <span data-ttu-id="9b409-106">Det sammenligner kodeeksempler i tidligere versioner med kodeeksempler i Business Central.</span><span class="sxs-lookup"><span data-stu-id="9b409-106">It compares the code examples in earlier versions to the code examples in Business Central.</span></span>

## <a name="posting-a-journal-line"></a><span data-ttu-id="9b409-107">Bogføring af en kladdelinje</span><span class="sxs-lookup"><span data-stu-id="9b409-107">Posting a Journal Line</span></span>  
<span data-ttu-id="9b409-108">Vigtigste ændringer er angivet som følger:</span><span class="sxs-lookup"><span data-stu-id="9b409-108">Key changes are listed as follows:</span></span>  

- <span data-ttu-id="9b409-109">Kladdelinjers dimensionstabeller fjernes.</span><span class="sxs-lookup"><span data-stu-id="9b409-109">Journal line dimension tables are removed.</span></span>  

- <span data-ttu-id="9b409-110">Et dimensionsgruppe-id oprettes i feltet **Dimensionsgruppe-id**.</span><span class="sxs-lookup"><span data-stu-id="9b409-110">A dimension set ID is created in the **Dimension Set ID** field.</span></span>  

<span data-ttu-id="9b409-111">**Tidligere versioner**</span><span class="sxs-lookup"><span data-stu-id="9b409-111">**Earlier Versions**</span></span>  

```  
ResJnlLine."Qty. per Unit of Measure" :=   
  SalesLine."Qty. per Unit of Measure";  

TempJnlLineDim.DELETEALL;  
TempDocDim.RESET;  
TempDocDim.SETRANGE(  
  "Table ID",DATABASE::"Sales Line");  
TempDocDim.SETRANGE(  
  "Line No.",SalesLine."Line No.");  
DimMgt.CopyDocDimToJnlLineDim(  
  TempDocDim,TempJnlLineDim);  
ResJnlPostLine.RunWithCheck(  
  ResJnlLine,TempJnlLineDim);  

```  

 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  

```  

ResJnlLine."Qty. per Unit of Measure" :=   
  SalesLine."Qty. per Unit of Measure";  

ResJnlLine."Dimension Set ID" :=   
  SalesLine." Dimension Set ID ";  
ResJnlPostLine.Run(ResJnlLine);  

```  

## <a name="posting-a-document"></a><span data-ttu-id="9b409-112">Bogføring af et dokument</span><span class="sxs-lookup"><span data-stu-id="9b409-112">Posting a Document</span></span>  
 <span data-ttu-id="9b409-113">Når du bogfører et dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)], behøver du ikke længere at kopiere dokumentdimensioner.</span><span class="sxs-lookup"><span data-stu-id="9b409-113">When you post a document in [!INCLUDE[d365fin](includes/d365fin_md.md)], you no longer have to copy the document dimensions.</span></span>  

 <span data-ttu-id="9b409-114">**Tidligere versioner**</span><span class="sxs-lookup"><span data-stu-id="9b409-114">**Earlier Versions**</span></span>  

```  
DimMgt.MoveOneDocDimToPostedDocDim(  
  TempDocDim,DATABASE::"Sales Line",  
  "Document Type",  
  "No.",  
  SalesShptLine."Line No.",  
  DATABASE::"Sales Shipment Line",  
  SalesShptHeader."No.");  
```  

 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  

```  
SalesShptLine."Dimension Set ID”  
  := SalesLine."Dimension Set ID”  
```  

## <a name="editing-dimensions-from-a-document"></a><span data-ttu-id="9b409-115">Redigering af dimensioner fra et dokument.</span><span class="sxs-lookup"><span data-stu-id="9b409-115">Editing Dimensions from a Document</span></span>  
 <span data-ttu-id="9b409-116">Du kan redigere dimensioner fra et dokument.</span><span class="sxs-lookup"><span data-stu-id="9b409-116">You can edit dimensions from a document.</span></span> <span data-ttu-id="9b409-117">Du kan f.eks. redigere en salgsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="9b409-117">For example, you can edit a sales order line.</span></span>  

 <span data-ttu-id="9b409-118">**Tidligere versioner**</span><span class="sxs-lookup"><span data-stu-id="9b409-118">**Earlier Versions**</span></span>  

```  
Table 37, function ShowDimensions:  
TESTFIELD("Document No.");  
TESTFIELD("Line No.");  
DocDim.SETRANGE("Table ID",DATABASE::"Sales Line");  
DocDim.SETRANGE("Document Type","Document Type");  
DocDim.SETRANGE("Document No.","Document No.");  
DocDim.SETRANGE("Line No.","Line No.");  
DocDimensions.SETTABLEVIEW(DocDim);  
DocDimensions.RUNMODAL;  
```  

 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  

```  
Table 37, function ShowDimensions:  
"Dimension ID" :=   
  DimSetEntry.EditDimensionSet(  
    "Dimension ID");  
```  

## <a name="showing-dimensions-from-posted-entries"></a><span data-ttu-id="9b409-119">Viser dimensionerne fra bogførte poster</span><span class="sxs-lookup"><span data-stu-id="9b409-119">Showing Dimensions from Posted Entries</span></span>  
 <span data-ttu-id="9b409-120">Du kan få vist dimensionerne fra bogførte poster, f.eks. salgsleverancelinjer.</span><span class="sxs-lookup"><span data-stu-id="9b409-120">You can show dimensions from posted entries, such as sales shipment lines.</span></span>  

 <span data-ttu-id="9b409-121">**Tidligere versioner**</span><span class="sxs-lookup"><span data-stu-id="9b409-121">**Earlier Versions**</span></span>  

```  
Table 111, function ShowDimensions:  
TESTFIELD("No.");  
TESTFIELD("Line No.");  
PostedDocDim.SETRANGE(  
  "Table ID",DATABASE::"Sales Shipment Line");  
PostedDocDim.SETRANGE(  
  "Document No.","Document No.");  
PostedDocDim.SETRANGE("Line No.","Line No.");  
PostedDocDimensions.SETTABLEVIEW(PostedDocDim);  
PostedDocDimensions.RUNMODAL;  
```  

 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  

```  
Table 111, function ShowDimensions:  
DimSetEntry.ShowDimensionSet(  
  "Dimension ID");  
```  

## <a name="getting-default-dimensions-for-a-document"></a><span data-ttu-id="9b409-122">Henter standarddimensioner for et dokument</span><span class="sxs-lookup"><span data-stu-id="9b409-122">Getting Default Dimensions for a Document</span></span>  
 <span data-ttu-id="9b409-123">Du kan hente standarddimensioner for et dokument, f.eks en salgsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="9b409-123">You can get default dimensions for a document, such as a sales order line.</span></span>  

 <span data-ttu-id="9b409-124">**Tidligere versioner**</span><span class="sxs-lookup"><span data-stu-id="9b409-124">**Earlier Versions**</span></span>  

```  
Table 37, function CreateDim()  
SourceCodeSetup.GET;  
TableID[1] := Type1;  
No[1] := No1;  
TableID[2] := Type2;  
No[2] := No2;  
TableID[3] := Type3;  
No[3] := No3;  
"Shortcut Dimension 1 Code" := '';  
"Shortcut Dimension 2 Code" := '';  
DimMgt.GetPreviousDocDefaultDim(  
  DATABASE::"Sales Header","Document Type",  
  "Document No.",0,  
  DATABASE::Customer,  
  "Shortcut Dimension 1 Code",  
  "Shortcut Dimension 2 Code");  
DimMgt.GetDefaultDim(  
  TableID,No,SourceCodeSetup.Sales,  
  "Shortcut Dimension 1 Code",  
  "Shortcut Dimension 2 Code");  
IF "Line No." <> 0 THEN  
  DimMgt.UpdateDocDefaultDim(  
    DATABASE::"Sales Line","Document Type",  
    "Document No.","Line No.",  
    "Shortcut Dimension 1 Code",  
    "Shortcut Dimension 2 Code");  
```  

 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  

```  
Table 37, function CreateDim()  
SourceCodeSetup.GET;  
TableID[1] := Type1;  
No[1] := No1;  
TableID[2] := Type2;  
No[2] := No2;  
TableID[3] := Type3;  
No[3] := No3;  
"Shortcut Dimension 1 Code" := '';  
"Shortcut Dimension 2 Code" := '';  
GetSalesHeader;  
"Dimension ID" :=  
  DimMgt.GetDefaultDimID(  
    TableID,No,SourceCodeSetup.Sales,  
    "Shortcut Dimension 1 Code",  
    "Shortcut Dimension 2 Code",  
    SalesHeader."Dimension ID",  
    DATABASE::"Sales Header");

```  

## <a name="see-also"></a><span data-ttu-id="9b409-125">Se også</span><span class="sxs-lookup"><span data-stu-id="9b409-125">See Also</span></span>  
<span data-ttu-id="9b409-126">[Designoplysninger: Dimensionsgruppeposter](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="9b409-126">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
[<span data-ttu-id="9b409-127">Designoplysninger: Tabelstruktur</span><span class="sxs-lookup"><span data-stu-id="9b409-127">Design Details: Table Structure</span></span>](design-details-table-structure.md)   
