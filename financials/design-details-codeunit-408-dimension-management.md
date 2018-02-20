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
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-codeunit-408-dimension-management"></a><span data-ttu-id="0d429-103">Designoplysninger: Kodeenhed 408 Dimensionsstyring</span><span class="sxs-lookup"><span data-stu-id="0d429-103">Design Details: Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="0d429-104">Kodeenhed 408-dimensionsstyring er et funktionsbibliotek, der håndterer almindelige opgaver, der er relateret til dimensioner, som f.eks. kopiering fra én tabel til en anden eller fra et dokument til en andet.</span><span class="sxs-lookup"><span data-stu-id="0d429-104">Codeunit 408 Dimension Management is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span> <span data-ttu-id="0d429-105">I dette emne beskrives de funktioner, der er ændret i Microsoft Dynamics NAV 2013 R2, og hvad der skal gøres ved funktionerne.</span><span class="sxs-lookup"><span data-stu-id="0d429-105">This topic lists the functions that are modified in Microsoft Dynamics NAV 2013 R2 and specifies what has to be done to the functions.</span></span> <span data-ttu-id="0d429-106">Mange funktioner er slettet, fordi der er ingen grund til at kopiere mellem dimensionstabeller.</span><span class="sxs-lookup"><span data-stu-id="0d429-106">Many functions are deleted because there is no need for copying between dimension tables.</span></span>  

## <a name="modified-functions"></a><span data-ttu-id="0d429-107">Ændrede funktioner</span><span class="sxs-lookup"><span data-stu-id="0d429-107">Modified Functions</span></span>  

|<span data-ttu-id="0d429-108">Funktionsnavn</span><span class="sxs-lookup"><span data-stu-id="0d429-108">Function Name</span></span>|<span data-ttu-id="0d429-109">Beskrivelse af ændring</span><span class="sxs-lookup"><span data-stu-id="0d429-109">Modification Description</span></span>|  
|-------------------|------------------------------|  
|<span data-ttu-id="0d429-110">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="0d429-110">CheckDimSetIDComb</span></span>|<span data-ttu-id="0d429-111">Ny funktion, der erstatter de andre kontrolfunktioner og tager et dimensionsgruppe-id som argument i stedet for en dimensionstabel.</span><span class="sxs-lookup"><span data-stu-id="0d429-111">New function that substitutes the other check functions and takes a Dimension Set ID as an argument instead of a dimension table.</span></span>|  
|<span data-ttu-id="0d429-112">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="0d429-112">CheckDimSetIDComb</span></span><br /><br /> <span data-ttu-id="0d429-113">CheckDocDimComb</span><span class="sxs-lookup"><span data-stu-id="0d429-113">CheckDocDimComb</span></span><br /><br /> <span data-ttu-id="0d429-114">CheckServContractDimComb</span><span class="sxs-lookup"><span data-stu-id="0d429-114">CheckServContractDimComb</span></span><br /><br /> <span data-ttu-id="0d429-115">CheckDimBuffer</span><span class="sxs-lookup"><span data-stu-id="0d429-115">CheckDimBuffer</span></span><br /><br /> <span data-ttu-id="0d429-116">CheckDimComb</span><span class="sxs-lookup"><span data-stu-id="0d429-116">CheckDimComb</span></span><br /><br /> <span data-ttu-id="0d429-117">CheckDimValueComb</span><span class="sxs-lookup"><span data-stu-id="0d429-117">CheckDimValueComb</span></span>|<span data-ttu-id="0d429-118">Slet.</span><span class="sxs-lookup"><span data-stu-id="0d429-118">Delete.</span></span> <span data-ttu-id="0d429-119">Alt forbrug skal ændres til CheckDimSetIDComb.</span><span class="sxs-lookup"><span data-stu-id="0d429-119">All usage should be changed to CheckDimSetIDComb.</span></span>|  
|<span data-ttu-id="0d429-120">GetDefaultDim</span><span class="sxs-lookup"><span data-stu-id="0d429-120">GetDefaultDim</span></span>|<span data-ttu-id="0d429-121">Rediger for at returnere et heltal som dimensionsgruppe-id i stedet for et sæt poster.</span><span class="sxs-lookup"><span data-stu-id="0d429-121">Modify to return an integer Dimension Set ID instead of a set of records.</span></span>|  
|<span data-ttu-id="0d429-122">CopyJnlLineDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="0d429-122">CopyJnlLineDimToICJnlDim</span></span><br /><br /> <span data-ttu-id="0d429-123">CopyICJnlDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0d429-123">CopyICJnlDimToJnlLineDim</span></span><br /><br /> <span data-ttu-id="0d429-124">CopyDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-124">CopyDocDimtoICDocDim</span></span><br /><br /> <span data-ttu-id="0d429-125">CopyICDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-125">CopyICDocDimtoICDocDim</span></span>|<span data-ttu-id="0d429-126">Rediger for at arbejde med DimSetID -> ICJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0d429-126">Modify to work with DimSetID -> ICJnlLineDim</span></span>|  

## <a name="deleted-functions"></a><span data-ttu-id="0d429-127">Slettede funktioner</span><span class="sxs-lookup"><span data-stu-id="0d429-127">Deleted Functions</span></span>  
 <span data-ttu-id="0d429-128">Funktioner, der slettes fra codeunit 408 i forbindelse med funktionen Angiv dimensionsposter er angivet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="0d429-128">Functions that are deleted from codeunit 408 in connection with the Dimension Set Entries feature are listed below.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="0d429-129">Under opgradering af programkode fra Microsoft Dynamics NAV 2009 eller tidligere versioner til Microsoft Dynamics NAV 2016, er følgende funktioner ikke tilgængelige i Microsoft Dynamics NAV 2016.</span><span class="sxs-lookup"><span data-stu-id="0d429-129">During the upgrade of application code from Microsoft Dynamics NAV 2009 or earlier versions to Microsoft Dynamics NAV 2016, the following functions are not available in Microsoft Dynamics NAV 2016.</span></span> <span data-ttu-id="0d429-130">Hvis du har tilpasninger, der bruger en eller flere af funktionerne, skal du opgraderer denne kode i overensstemmelse hermed.</span><span class="sxs-lookup"><span data-stu-id="0d429-130">If you have customizations that use one or more of the functions, you must upgrade that code accordingly.</span></span>

 <span data-ttu-id="0d429-131">InsertJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0d429-131">InsertJnlLineDim</span></span>  

 <span data-ttu-id="0d429-132">UpdateJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="0d429-132">UpdateJnlLineDefaultDim</span></span>  

 <span data-ttu-id="0d429-133">GetJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="0d429-133">GetJnlLineDefaultDim</span></span>  

 <span data-ttu-id="0d429-134">GetPreviousDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="0d429-134">GetPreviousDocDefaultDim</span></span>  

 <span data-ttu-id="0d429-135">GetPreviousProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="0d429-135">GetPreviousProdDocDefaultDim</span></span>  

 <span data-ttu-id="0d429-136">InsertDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-136">InsertDocDim</span></span>  

 <span data-ttu-id="0d429-137">UpdateDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="0d429-137">UpdateDocDefaultDim</span></span>  

 <span data-ttu-id="0d429-138">ExtractDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="0d429-138">ExtractDocDefaultDim</span></span>  

 <span data-ttu-id="0d429-139">InsertProdDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-139">InsertProdDocDim</span></span>  

 <span data-ttu-id="0d429-140">UpdateProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="0d429-140">UpdateProdDocDefaultDim</span></span>  

 <span data-ttu-id="0d429-141">InsertServContractDim</span><span class="sxs-lookup"><span data-stu-id="0d429-141">InsertServContractDim</span></span>  

 <span data-ttu-id="0d429-142">UpdateServcontractDim</span><span class="sxs-lookup"><span data-stu-id="0d429-142">UpdateServcontractDim</span></span>  

 <span data-ttu-id="0d429-143">UpdateDefaultDimNewDimValue</span><span class="sxs-lookup"><span data-stu-id="0d429-143">UpdateDefaultDimNewDimValue</span></span>  

 <span data-ttu-id="0d429-144">GetDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-144">GetDocDim</span></span>  

 <span data-ttu-id="0d429-145">GetProdDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-145">GetProdDocDim</span></span>  

 <span data-ttu-id="0d429-146">TypeToTableID1</span><span class="sxs-lookup"><span data-stu-id="0d429-146">TypeToTableID1</span></span>  

 <span data-ttu-id="0d429-147">TypeToTableID2</span><span class="sxs-lookup"><span data-stu-id="0d429-147">TypeToTableID2</span></span>  

 <span data-ttu-id="0d429-148">TypeToTableID3</span><span class="sxs-lookup"><span data-stu-id="0d429-148">TypeToTableID3</span></span>  

 <span data-ttu-id="0d429-149">TypeToTableID4</span><span class="sxs-lookup"><span data-stu-id="0d429-149">TypeToTableID4</span></span>  

 <span data-ttu-id="0d429-150">TypeToTableID5</span><span class="sxs-lookup"><span data-stu-id="0d429-150">TypeToTableID5</span></span>  

 <span data-ttu-id="0d429-151">DeleteJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0d429-151">DeleteJnlLineDim</span></span>  

 <span data-ttu-id="0d429-152">DeleteDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-152">DeleteDocDim</span></span>  

 <span data-ttu-id="0d429-153">DeletePostedDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-153">DeletePostedDocDim</span></span>  

 <span data-ttu-id="0d429-154">DeleteProdDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-154">DeleteProdDocDim</span></span>  

 <span data-ttu-id="0d429-155">DeleteServContractDim</span><span class="sxs-lookup"><span data-stu-id="0d429-155">DeleteServContractDim</span></span>  

 <span data-ttu-id="0d429-156">ShowJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0d429-156">ShowJnlLineDim</span></span>  

 <span data-ttu-id="0d429-157">SaveJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0d429-157">SaveJnlLineDim</span></span>  

 <span data-ttu-id="0d429-158">ShowJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="0d429-158">ShowJnlLineNewDim</span></span>  

 <span data-ttu-id="0d429-159">SaveJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="0d429-159">SaveJnlLineNewDim</span></span>  

 <span data-ttu-id="0d429-160">ShowDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-160">ShowDocDim</span></span>  

 <span data-ttu-id="0d429-161">SaveDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-161">SaveDocDim</span></span>  

 <span data-ttu-id="0d429-162">ShowProdDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-162">ShowProdDocDim</span></span>  

 <span data-ttu-id="0d429-163">SaveProdDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-163">SaveProdDocDim</span></span>  

 <span data-ttu-id="0d429-164">ShowTempDim</span><span class="sxs-lookup"><span data-stu-id="0d429-164">ShowTempDim</span></span>  

 <span data-ttu-id="0d429-165">SaveTempDim</span><span class="sxs-lookup"><span data-stu-id="0d429-165">SaveTempDim</span></span>  

 <span data-ttu-id="0d429-166">ShowTempNewDim</span><span class="sxs-lookup"><span data-stu-id="0d429-166">ShowTempNewDim</span></span>  

 <span data-ttu-id="0d429-167">SaveTempNewDim</span><span class="sxs-lookup"><span data-stu-id="0d429-167">SaveTempNewDim</span></span>  

 <span data-ttu-id="0d429-168">SaveServContractDim</span><span class="sxs-lookup"><span data-stu-id="0d429-168">SaveServContractDim</span></span>  

 <span data-ttu-id="0d429-169">MoveJnlLineDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="0d429-169">MoveJnlLineDimToLedgEntryDim</span></span>  

 <span data-ttu-id="0d429-170">MoveDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-170">MoveDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="0d429-171">MoveOneDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-171">MoveOneDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="0d429-172">MoveLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0d429-172">MoveLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="0d429-173">MoveDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0d429-173">MoveDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="0d429-174">MoveDimBufToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="0d429-174">MoveDimBufToLedgEntryDim</span></span>  

 <span data-ttu-id="0d429-175">MoveDimBufToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-175">MoveDimBufToPostedDocDim</span></span>  

 <span data-ttu-id="0d429-176">MoveDimBufToGLBudgetDim</span><span class="sxs-lookup"><span data-stu-id="0d429-176">MoveDimBufToGLBudgetDim</span></span>  

 <span data-ttu-id="0d429-177">CopyJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0d429-177">CopyJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="0d429-178">CopyLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0d429-178">CopyLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="0d429-179">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-179">CopyDocDimToDocDim</span></span>  

 <span data-ttu-id="0d429-180">CopyPostedDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-180">CopyPostedDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="0d429-181">CopyDocDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0d429-181">CopyDocDimToJnlLineDim</span></span>  

 <span data-ttu-id="0d429-182">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0d429-182">CopyDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="0d429-183">CopyDimBufToDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-183">CopyDimBufToDocDim</span></span>  

 <span data-ttu-id="0d429-184">CopySCDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-184">CopySCDimToDocDim</span></span>  

 <span data-ttu-id="0d429-185">MoveDocDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="0d429-185">MoveDocDimToLedgEntryDim</span></span>  

 <span data-ttu-id="0d429-186">MoveDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-186">MoveDocDimToDocDim</span></span>  

 <span data-ttu-id="0d429-187">MoveDocDimArchvToDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-187">MoveDocDimArchvToDocDim</span></span>  

 <span data-ttu-id="0d429-188">MoveLedgEntryDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-188">MoveLedgEntryDimToDocDim</span></span>  

 <span data-ttu-id="0d429-189">MoveProdDocDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-189">MoveProdDocDimToProdDocDim</span></span>  

 <span data-ttu-id="0d429-190">MoveJnlLineDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-190">MoveJnlLineDimToProdDocDim</span></span>  

 <span data-ttu-id="0d429-191">MoveJnlLineDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-191">MoveJnlLineDimToDocDim</span></span>  

 <span data-ttu-id="0d429-192">MoveJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0d429-192">MoveJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="0d429-193">CopyLedgEntryDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="0d429-193">CopyLedgEntryDimToLedgEntryDim</span></span>  

 <span data-ttu-id="0d429-194">MoveTempFromDimToTempToDim</span><span class="sxs-lookup"><span data-stu-id="0d429-194">MoveTempFromDimToTempToDim</span></span>  

 <span data-ttu-id="0d429-195">TransferTempToDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="0d429-195">TransferTempToDimToDocDim</span></span>  

 <span data-ttu-id="0d429-196">MoveJnlLineDimToBuf</span><span class="sxs-lookup"><span data-stu-id="0d429-196">MoveJnlLineDimToBuf</span></span>  

 <span data-ttu-id="0d429-197">CopyICJnlDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="0d429-197">CopyICJnlDimToICJnlDim</span></span>  

 <span data-ttu-id="0d429-198">TestDimValue</span><span class="sxs-lookup"><span data-stu-id="0d429-198">TestDimValue</span></span>  

 <span data-ttu-id="0d429-199">TestNewDimValue</span><span class="sxs-lookup"><span data-stu-id="0d429-199">TestNewDimValue</span></span>  

 <span data-ttu-id="0d429-200">MoveDimBufToItemBudgetDim.</span><span class="sxs-lookup"><span data-stu-id="0d429-200">MoveDimBufToItemBudgetDim.</span></span> <span data-ttu-id="0d429-201">(Slet, fordi tabellen ItemBudgetDim er slettet.)</span><span class="sxs-lookup"><span data-stu-id="0d429-201">(Delete because the ItemBudgetDim Table is deleted.)</span></span>  

 <span data-ttu-id="0d429-202">GetServContractDim</span><span class="sxs-lookup"><span data-stu-id="0d429-202">GetServContractDim</span></span>  

 <span data-ttu-id="0d429-203">MoveTempDimToBuf</span><span class="sxs-lookup"><span data-stu-id="0d429-203">MoveTempDimToBuf</span></span>  

 <span data-ttu-id="0d429-204">UpdateSCInvLineDim</span><span class="sxs-lookup"><span data-stu-id="0d429-204">UpdateSCInvLineDim</span></span>  

 <span data-ttu-id="0d429-205">CopyJnlLineDimToBuffer</span><span class="sxs-lookup"><span data-stu-id="0d429-205">CopyJnlLineDimToBuffer</span></span>  

 <span data-ttu-id="0d429-206">UpdateDocDefaultDim2</span><span class="sxs-lookup"><span data-stu-id="0d429-206">UpdateDocDefaultDim2</span></span>  

## <a name="see-also"></a><span data-ttu-id="0d429-207">Se også</span><span class="sxs-lookup"><span data-stu-id="0d429-207">See Also</span></span>
 <span data-ttu-id="0d429-208">[Designoplysninger: Dimensionsgruppeposter](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="0d429-208">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="0d429-209">[Designoplysninger: Oversigt over dimensionsgruppeposter](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="0d429-209">[Design Details: Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="0d429-210">[Designoplysninger: Søgning efter dimensionskombinationer](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="0d429-210">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
 <span data-ttu-id="0d429-211">[Designoplysninger: Tabelstruktur](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="0d429-211">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
 [<span data-ttu-id="0d429-212">Designoplysninger: Kodeeksempler af ændrede mønstre i Ændringer</span><span class="sxs-lookup"><span data-stu-id="0d429-212">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)

