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
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 32f67c058570f03d4aa1c84d9bb32289b1f07bec
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="design-details-codeunit-408-dimension-management"></a><span data-ttu-id="8399a-103">Designoplysninger: Kodeenhed 408 Dimensionsstyring</span><span class="sxs-lookup"><span data-stu-id="8399a-103">Design Details: Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="8399a-104">Kodeenhed 408-dimensionsstyring er et funktionsbibliotek, der håndterer almindelige opgaver, der er relateret til dimensioner, som f.eks. kopiering fra én tabel til en anden eller fra et dokument til en andet.</span><span class="sxs-lookup"><span data-stu-id="8399a-104">Codeunit 408 Dimension Management is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span> <span data-ttu-id="8399a-105">I dette emne beskrives de funktioner, der er ændret i Microsoft Dynamics NAV 2013 R2, og hvad der skal gøres ved funktionerne.</span><span class="sxs-lookup"><span data-stu-id="8399a-105">This topic lists the functions that are modified in Microsoft Dynamics NAV 2013 R2 and specifies what has to be done to the functions.</span></span> <span data-ttu-id="8399a-106">Mange funktioner er slettet, fordi der er ingen grund til at kopiere mellem dimensionstabeller.</span><span class="sxs-lookup"><span data-stu-id="8399a-106">Many functions are deleted because there is no need for copying between dimension tables.</span></span>  

## <a name="modified-functions"></a><span data-ttu-id="8399a-107">Ændrede funktioner</span><span class="sxs-lookup"><span data-stu-id="8399a-107">Modified Functions</span></span>  

|<span data-ttu-id="8399a-108">Funktionsnavn</span><span class="sxs-lookup"><span data-stu-id="8399a-108">Function Name</span></span>|<span data-ttu-id="8399a-109">Beskrivelse af ændring</span><span class="sxs-lookup"><span data-stu-id="8399a-109">Modification Description</span></span>|  
|-------------------|------------------------------|  
|<span data-ttu-id="8399a-110">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="8399a-110">CheckDimSetIDComb</span></span>|<span data-ttu-id="8399a-111">Ny funktion, der erstatter de andre kontrolfunktioner og tager et dimensionsgruppe-id som argument i stedet for en dimensionstabel.</span><span class="sxs-lookup"><span data-stu-id="8399a-111">New function that substitutes the other check functions and takes a Dimension Set ID as an argument instead of a dimension table.</span></span>|  
|<span data-ttu-id="8399a-112">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="8399a-112">CheckDimSetIDComb</span></span><br /><br /> <span data-ttu-id="8399a-113">CheckDocDimComb</span><span class="sxs-lookup"><span data-stu-id="8399a-113">CheckDocDimComb</span></span><br /><br /> <span data-ttu-id="8399a-114">CheckServContractDimComb</span><span class="sxs-lookup"><span data-stu-id="8399a-114">CheckServContractDimComb</span></span><br /><br /> <span data-ttu-id="8399a-115">CheckDimBuffer</span><span class="sxs-lookup"><span data-stu-id="8399a-115">CheckDimBuffer</span></span><br /><br /> <span data-ttu-id="8399a-116">CheckDimComb</span><span class="sxs-lookup"><span data-stu-id="8399a-116">CheckDimComb</span></span><br /><br /> <span data-ttu-id="8399a-117">CheckDimValueComb</span><span class="sxs-lookup"><span data-stu-id="8399a-117">CheckDimValueComb</span></span>|<span data-ttu-id="8399a-118">Slet.</span><span class="sxs-lookup"><span data-stu-id="8399a-118">Delete.</span></span> <span data-ttu-id="8399a-119">Alt forbrug skal ændres til CheckDimSetIDComb.</span><span class="sxs-lookup"><span data-stu-id="8399a-119">All usage should be changed to CheckDimSetIDComb.</span></span>|  
|<span data-ttu-id="8399a-120">GetDefaultDim</span><span class="sxs-lookup"><span data-stu-id="8399a-120">GetDefaultDim</span></span>|<span data-ttu-id="8399a-121">Rediger for at returnere et heltal som dimensionsgruppe-id i stedet for et sæt poster.</span><span class="sxs-lookup"><span data-stu-id="8399a-121">Modify to return an integer Dimension Set ID instead of a set of records.</span></span>|  
|<span data-ttu-id="8399a-122">CopyJnlLineDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="8399a-122">CopyJnlLineDimToICJnlDim</span></span><br /><br /> <span data-ttu-id="8399a-123">CopyICJnlDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="8399a-123">CopyICJnlDimToJnlLineDim</span></span><br /><br /> <span data-ttu-id="8399a-124">CopyDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-124">CopyDocDimtoICDocDim</span></span><br /><br /> <span data-ttu-id="8399a-125">CopyICDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-125">CopyICDocDimtoICDocDim</span></span>|<span data-ttu-id="8399a-126">Rediger for at arbejde med DimSetID -> ICJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="8399a-126">Modify to work with DimSetID -> ICJnlLineDim</span></span>|  

## <a name="deleted-functions"></a><span data-ttu-id="8399a-127">Slettede funktioner</span><span class="sxs-lookup"><span data-stu-id="8399a-127">Deleted Functions</span></span>  
 <span data-ttu-id="8399a-128">Funktioner, der slettes fra codeunit 408 i forbindelse med funktionen Angiv dimensionsposter er angivet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="8399a-128">Functions that are deleted from codeunit 408 in connection with the Dimension Set Entries feature are listed below.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="8399a-129">Under opgradering af programkode fra Microsoft Dynamics NAV 2009 eller tidligere versioner til Microsoft Dynamics NAV 2016, er følgende funktioner ikke tilgængelige i Microsoft Dynamics NAV 2016.</span><span class="sxs-lookup"><span data-stu-id="8399a-129">During the upgrade of application code from Microsoft Dynamics NAV 2009 or earlier versions to Microsoft Dynamics NAV 2016, the following functions are not available in Microsoft Dynamics NAV 2016.</span></span> <span data-ttu-id="8399a-130">Hvis du har tilpasninger, der bruger en eller flere af funktionerne, skal du opgraderer denne kode i overensstemmelse hermed.</span><span class="sxs-lookup"><span data-stu-id="8399a-130">If you have customizations that use one or more of the functions, you must upgrade that code accordingly.</span></span>

 <span data-ttu-id="8399a-131">InsertJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="8399a-131">InsertJnlLineDim</span></span>  

 <span data-ttu-id="8399a-132">UpdateJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="8399a-132">UpdateJnlLineDefaultDim</span></span>  

 <span data-ttu-id="8399a-133">GetJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="8399a-133">GetJnlLineDefaultDim</span></span>  

 <span data-ttu-id="8399a-134">GetPreviousDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="8399a-134">GetPreviousDocDefaultDim</span></span>  

 <span data-ttu-id="8399a-135">GetPreviousProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="8399a-135">GetPreviousProdDocDefaultDim</span></span>  

 <span data-ttu-id="8399a-136">InsertDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-136">InsertDocDim</span></span>  

 <span data-ttu-id="8399a-137">UpdateDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="8399a-137">UpdateDocDefaultDim</span></span>  

 <span data-ttu-id="8399a-138">ExtractDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="8399a-138">ExtractDocDefaultDim</span></span>  

 <span data-ttu-id="8399a-139">InsertProdDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-139">InsertProdDocDim</span></span>  

 <span data-ttu-id="8399a-140">UpdateProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="8399a-140">UpdateProdDocDefaultDim</span></span>  

 <span data-ttu-id="8399a-141">InsertServContractDim</span><span class="sxs-lookup"><span data-stu-id="8399a-141">InsertServContractDim</span></span>  

 <span data-ttu-id="8399a-142">UpdateServcontractDim</span><span class="sxs-lookup"><span data-stu-id="8399a-142">UpdateServcontractDim</span></span>  

 <span data-ttu-id="8399a-143">UpdateDefaultDimNewDimValue</span><span class="sxs-lookup"><span data-stu-id="8399a-143">UpdateDefaultDimNewDimValue</span></span>  

 <span data-ttu-id="8399a-144">GetDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-144">GetDocDim</span></span>  

 <span data-ttu-id="8399a-145">GetProdDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-145">GetProdDocDim</span></span>  

 <span data-ttu-id="8399a-146">TypeToTableID1</span><span class="sxs-lookup"><span data-stu-id="8399a-146">TypeToTableID1</span></span>  

 <span data-ttu-id="8399a-147">TypeToTableID2</span><span class="sxs-lookup"><span data-stu-id="8399a-147">TypeToTableID2</span></span>  

 <span data-ttu-id="8399a-148">TypeToTableID3</span><span class="sxs-lookup"><span data-stu-id="8399a-148">TypeToTableID3</span></span>  

 <span data-ttu-id="8399a-149">TypeToTableID4</span><span class="sxs-lookup"><span data-stu-id="8399a-149">TypeToTableID4</span></span>  

 <span data-ttu-id="8399a-150">TypeToTableID5</span><span class="sxs-lookup"><span data-stu-id="8399a-150">TypeToTableID5</span></span>  

 <span data-ttu-id="8399a-151">DeleteJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="8399a-151">DeleteJnlLineDim</span></span>  

 <span data-ttu-id="8399a-152">DeleteDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-152">DeleteDocDim</span></span>  

 <span data-ttu-id="8399a-153">DeletePostedDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-153">DeletePostedDocDim</span></span>  

 <span data-ttu-id="8399a-154">DeleteProdDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-154">DeleteProdDocDim</span></span>  

 <span data-ttu-id="8399a-155">DeleteServContractDim</span><span class="sxs-lookup"><span data-stu-id="8399a-155">DeleteServContractDim</span></span>  

 <span data-ttu-id="8399a-156">ShowJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="8399a-156">ShowJnlLineDim</span></span>  

 <span data-ttu-id="8399a-157">SaveJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="8399a-157">SaveJnlLineDim</span></span>  

 <span data-ttu-id="8399a-158">ShowJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="8399a-158">ShowJnlLineNewDim</span></span>  

 <span data-ttu-id="8399a-159">SaveJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="8399a-159">SaveJnlLineNewDim</span></span>  

 <span data-ttu-id="8399a-160">ShowDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-160">ShowDocDim</span></span>  

 <span data-ttu-id="8399a-161">SaveDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-161">SaveDocDim</span></span>  

 <span data-ttu-id="8399a-162">ShowProdDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-162">ShowProdDocDim</span></span>  

 <span data-ttu-id="8399a-163">SaveProdDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-163">SaveProdDocDim</span></span>  

 <span data-ttu-id="8399a-164">ShowTempDim</span><span class="sxs-lookup"><span data-stu-id="8399a-164">ShowTempDim</span></span>  

 <span data-ttu-id="8399a-165">SaveTempDim</span><span class="sxs-lookup"><span data-stu-id="8399a-165">SaveTempDim</span></span>  

 <span data-ttu-id="8399a-166">ShowTempNewDim</span><span class="sxs-lookup"><span data-stu-id="8399a-166">ShowTempNewDim</span></span>  

 <span data-ttu-id="8399a-167">SaveTempNewDim</span><span class="sxs-lookup"><span data-stu-id="8399a-167">SaveTempNewDim</span></span>  

 <span data-ttu-id="8399a-168">SaveServContractDim</span><span class="sxs-lookup"><span data-stu-id="8399a-168">SaveServContractDim</span></span>  

 <span data-ttu-id="8399a-169">MoveJnlLineDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="8399a-169">MoveJnlLineDimToLedgEntryDim</span></span>  

 <span data-ttu-id="8399a-170">MoveDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-170">MoveDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="8399a-171">MoveOneDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-171">MoveOneDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="8399a-172">MoveLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="8399a-172">MoveLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="8399a-173">MoveDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="8399a-173">MoveDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="8399a-174">MoveDimBufToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="8399a-174">MoveDimBufToLedgEntryDim</span></span>  

 <span data-ttu-id="8399a-175">MoveDimBufToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-175">MoveDimBufToPostedDocDim</span></span>  

 <span data-ttu-id="8399a-176">MoveDimBufToGLBudgetDim</span><span class="sxs-lookup"><span data-stu-id="8399a-176">MoveDimBufToGLBudgetDim</span></span>  

 <span data-ttu-id="8399a-177">CopyJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="8399a-177">CopyJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="8399a-178">CopyLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="8399a-178">CopyLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="8399a-179">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-179">CopyDocDimToDocDim</span></span>  

 <span data-ttu-id="8399a-180">CopyPostedDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-180">CopyPostedDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="8399a-181">CopyDocDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="8399a-181">CopyDocDimToJnlLineDim</span></span>  

 <span data-ttu-id="8399a-182">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="8399a-182">CopyDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="8399a-183">CopyDimBufToDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-183">CopyDimBufToDocDim</span></span>  

 <span data-ttu-id="8399a-184">CopySCDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-184">CopySCDimToDocDim</span></span>  

 <span data-ttu-id="8399a-185">MoveDocDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="8399a-185">MoveDocDimToLedgEntryDim</span></span>  

 <span data-ttu-id="8399a-186">MoveDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-186">MoveDocDimToDocDim</span></span>  

 <span data-ttu-id="8399a-187">MoveDocDimArchvToDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-187">MoveDocDimArchvToDocDim</span></span>  

 <span data-ttu-id="8399a-188">MoveLedgEntryDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-188">MoveLedgEntryDimToDocDim</span></span>  

 <span data-ttu-id="8399a-189">MoveProdDocDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-189">MoveProdDocDimToProdDocDim</span></span>  

 <span data-ttu-id="8399a-190">MoveJnlLineDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-190">MoveJnlLineDimToProdDocDim</span></span>  

 <span data-ttu-id="8399a-191">MoveJnlLineDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-191">MoveJnlLineDimToDocDim</span></span>  

 <span data-ttu-id="8399a-192">MoveJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="8399a-192">MoveJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="8399a-193">CopyLedgEntryDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="8399a-193">CopyLedgEntryDimToLedgEntryDim</span></span>  

 <span data-ttu-id="8399a-194">MoveTempFromDimToTempToDim</span><span class="sxs-lookup"><span data-stu-id="8399a-194">MoveTempFromDimToTempToDim</span></span>  

 <span data-ttu-id="8399a-195">TransferTempToDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="8399a-195">TransferTempToDimToDocDim</span></span>  

 <span data-ttu-id="8399a-196">MoveJnlLineDimToBuf</span><span class="sxs-lookup"><span data-stu-id="8399a-196">MoveJnlLineDimToBuf</span></span>  

 <span data-ttu-id="8399a-197">CopyICJnlDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="8399a-197">CopyICJnlDimToICJnlDim</span></span>  

 <span data-ttu-id="8399a-198">TestDimValue</span><span class="sxs-lookup"><span data-stu-id="8399a-198">TestDimValue</span></span>  

 <span data-ttu-id="8399a-199">TestNewDimValue</span><span class="sxs-lookup"><span data-stu-id="8399a-199">TestNewDimValue</span></span>  

 <span data-ttu-id="8399a-200">MoveDimBufToItemBudgetDim.</span><span class="sxs-lookup"><span data-stu-id="8399a-200">MoveDimBufToItemBudgetDim.</span></span> <span data-ttu-id="8399a-201">(Slet, fordi tabellen ItemBudgetDim er slettet.)</span><span class="sxs-lookup"><span data-stu-id="8399a-201">(Delete because the ItemBudgetDim Table is deleted.)</span></span>  

 <span data-ttu-id="8399a-202">GetServContractDim</span><span class="sxs-lookup"><span data-stu-id="8399a-202">GetServContractDim</span></span>  

 <span data-ttu-id="8399a-203">MoveTempDimToBuf</span><span class="sxs-lookup"><span data-stu-id="8399a-203">MoveTempDimToBuf</span></span>  

 <span data-ttu-id="8399a-204">UpdateSCInvLineDim</span><span class="sxs-lookup"><span data-stu-id="8399a-204">UpdateSCInvLineDim</span></span>  

 <span data-ttu-id="8399a-205">CopyJnlLineDimToBuffer</span><span class="sxs-lookup"><span data-stu-id="8399a-205">CopyJnlLineDimToBuffer</span></span>  

 <span data-ttu-id="8399a-206">UpdateDocDefaultDim2</span><span class="sxs-lookup"><span data-stu-id="8399a-206">UpdateDocDefaultDim2</span></span>  

## <a name="see-also"></a><span data-ttu-id="8399a-207">Se også</span><span class="sxs-lookup"><span data-stu-id="8399a-207">See Also</span></span>
 <span data-ttu-id="8399a-208">[Designoplysninger: Dimensionsgruppeposter](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="8399a-208">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="8399a-209">[Designoplysninger: Oversigt over dimensionsgruppeposter](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="8399a-209">[Design Details: Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="8399a-210">[Designoplysninger: Søgning efter dimensionskombinationer](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="8399a-210">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
 <span data-ttu-id="8399a-211">[Designoplysninger: Tabelstruktur](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="8399a-211">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
 [<span data-ttu-id="8399a-212">Designoplysninger: Kodeeksempler af ændrede mønstre i Ændringer</span><span class="sxs-lookup"><span data-stu-id="8399a-212">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)
