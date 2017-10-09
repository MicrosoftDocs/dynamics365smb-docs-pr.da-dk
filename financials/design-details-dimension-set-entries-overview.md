---
title: Oversigt over dimensionsgruppeposter | Microsoft Docs
description: "Dette emne beskriver, hvordan dimensionsgruppeposter gemmes og bogføres i [!INCLUDE[d365fin](includes/d365fin_md.md)]."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 53c85ecbb42db92e95921203d24781bcb82f942d
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="dimension-set-entries-overview"></a><span data-ttu-id="f614e-103">Oversigt over dimensionsgruppeposter</span><span class="sxs-lookup"><span data-stu-id="f614e-103">Dimension Set Entries Overview</span></span>
<span data-ttu-id="f614e-104">Dette emne beskriver, hvordan dimensionsgruppeposter gemmes og bogføres i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f614e-104">This topic describes how dimension set entries are stored and posted in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
  
## <a name="dimension-sets"></a><span data-ttu-id="f614e-105">Dimensionsopsætninger</span><span class="sxs-lookup"><span data-stu-id="f614e-105">Dimension Sets</span></span>  
<span data-ttu-id="f614e-106">En dimensionsgruppe er en entydig kombination af dimensionsværdier.</span><span class="sxs-lookup"><span data-stu-id="f614e-106">A dimension set is a unique combination of dimension values.</span></span> <span data-ttu-id="f614e-107">Det er gemt som dimensionsgruppeposter i databasen.</span><span class="sxs-lookup"><span data-stu-id="f614e-107">It is stored as dimension set entries in the database.</span></span> <span data-ttu-id="f614e-108">Hver dimensionsgruppepost repræsenterer en enkelt dimensionsværdi.</span><span class="sxs-lookup"><span data-stu-id="f614e-108">Each dimension set entry represents a single dimension value.</span></span> <span data-ttu-id="f614e-109">Dimensionsgruppen er identificeret med en fælles dimensionsgruppe-id, der tildeles til hver dimensionsgruppepost, der hører til dimensionsgruppen.</span><span class="sxs-lookup"><span data-stu-id="f614e-109">The dimension set is identified by a common dimension set ID that is assigned to each dimension set entry that belongs to the dimension set.</span></span>  
  
<span data-ttu-id="f614e-110">Følgende eksempel viser en dimensionsgruppe, der har tre poster for dimensionsgruppe .</span><span class="sxs-lookup"><span data-stu-id="f614e-110">The following example shows a dimension set that has three dimension set entries.</span></span> <span data-ttu-id="f614e-111">Dimensionsgruppe er identificeret med en dimensionsgruppe-id, som er 108.</span><span class="sxs-lookup"><span data-stu-id="f614e-111">The dimension set is identified by a dimension set ID, which is 108.</span></span>  
  
|<span data-ttu-id="f614e-112">Dimensionsgruppe-id</span><span class="sxs-lookup"><span data-stu-id="f614e-112">Dimension Set ID</span></span>|<span data-ttu-id="f614e-113">Dimensionskode</span><span class="sxs-lookup"><span data-stu-id="f614e-113">Dimension Code</span></span>|<span data-ttu-id="f614e-114">Dimensionsværdikode</span><span class="sxs-lookup"><span data-stu-id="f614e-114">Dimension Value Code</span></span>|<span data-ttu-id="f614e-115">Dimensionsværdinavn</span><span class="sxs-lookup"><span data-stu-id="f614e-115">Dimension Value Name</span></span>|  
|----------------------|--------------------|--------------------------|--------------------------|  
|<span data-ttu-id="f614e-116">108</span><span class="sxs-lookup"><span data-stu-id="f614e-116">108</span></span>|<span data-ttu-id="f614e-117">OMRÅDE</span><span class="sxs-lookup"><span data-stu-id="f614e-117">AREA</span></span>|<span data-ttu-id="f614e-118">70</span><span class="sxs-lookup"><span data-stu-id="f614e-118">70</span></span>|<span data-ttu-id="f614e-119">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="f614e-119">America North</span></span>|  
|<span data-ttu-id="f614e-120">108</span><span class="sxs-lookup"><span data-stu-id="f614e-120">108</span></span>|<span data-ttu-id="f614e-121">FORRETNINGSGRUPPE</span><span class="sxs-lookup"><span data-stu-id="f614e-121">BUSINESSGROUP</span></span>|<span data-ttu-id="f614e-122">HOME</span><span class="sxs-lookup"><span data-stu-id="f614e-122">HOME</span></span>|<span data-ttu-id="f614e-123">Start</span><span class="sxs-lookup"><span data-stu-id="f614e-123">Home</span></span>|  
|<span data-ttu-id="f614e-124">108</span><span class="sxs-lookup"><span data-stu-id="f614e-124">108</span></span>|<span data-ttu-id="f614e-125">AFDELING</span><span class="sxs-lookup"><span data-stu-id="f614e-125">DEPARTMENT</span></span>|<span data-ttu-id="f614e-126">SALG</span><span class="sxs-lookup"><span data-stu-id="f614e-126">SALES</span></span>|<span data-ttu-id="f614e-127">Salg</span><span class="sxs-lookup"><span data-stu-id="f614e-127">Sales</span></span>|  
  
## <a name="dimension-set-entries"></a><span data-ttu-id="f614e-128">Dimensionsgruppeposter</span><span class="sxs-lookup"><span data-stu-id="f614e-128">Dimension Set Entries</span></span>  
<span data-ttu-id="f614e-129">Dimensionsgrupper er gemt i tabellen **Dimensionsgruppepost** som dimensionsgruppeposter med samme dimensionsgruppe-id.</span><span class="sxs-lookup"><span data-stu-id="f614e-129">Dimension sets are stored in the **Dimension Set Entry** table as dimension set entries with the same dimension set ID.</span></span>  
  
<span data-ttu-id="f614e-130">![Oversigt over dimensionspost](media/dimensionentrynav7.png "DimensionEntryNAV7")</span><span class="sxs-lookup"><span data-stu-id="f614e-130">![Dimension Entry overview](media/dimensionentrynav7.png "DimensionEntryNAV7")</span></span>  
  
<span data-ttu-id="f614e-131">Når du opretter en ny kladdelinje, et nyt bilagshoved eller en ny bilagslinje, kan du angive en kombination af dimensionsværdier.</span><span class="sxs-lookup"><span data-stu-id="f614e-131">When you create a new journal line, document header, or document line, you can specify a combination of dimension values.</span></span> <span data-ttu-id="f614e-132">I stedet for at eksplicit at gemme hver dimensionsværdi i databasen, tildeles kladdelinjen, bilagshovedet eller bilagslinjen en dimensionsgruppe-id, der angiver dimensionsgruppen.</span><span class="sxs-lookup"><span data-stu-id="f614e-132">Instead of explicitly storing each dimension value in the database, a dimension set ID is assigned to the journal line, document header, or document line to specify the dimension set.</span></span>  
  
<span data-ttu-id="f614e-133">Når du redigerer og lukker vinduet **Rediger dimensionsgruppeposter** udføres en kontrol for at se, om kombinationen af dimensionsværdier findes som en dimensionsgruppe i tabellen.</span><span class="sxs-lookup"><span data-stu-id="f614e-133">When you edit and close the **Edit Dimension Set Entries** window, a check is performed to see whether the combination of dimension values exists as a dimension set in the table.</span></span> <span data-ttu-id="f614e-134">Hvis kombinationen findes i tabellen, tildeles den tilsvarende dimensionsgruppe-id til kladdelinjen, bilagshovedet eller bilagslinjen.</span><span class="sxs-lookup"><span data-stu-id="f614e-134">If the combination occurs in the table, then the corresponding dimension set ID is assigned to the journal line, document header, or document line.</span></span> <span data-ttu-id="f614e-135">Ellers tilføjes en ny dimensionsgruppe til tabellen, og den nye dimensionsgruppe-id knyttes til kladdelinjen, bilagshovedet eller bilagslinjen.</span><span class="sxs-lookup"><span data-stu-id="f614e-135">Otherwise, a new dimension set is added to the table, and the new dimension set ID is assigned to the journal line, document header, or document line.</span></span>  
  
## <a name="performance-improvement"></a><span data-ttu-id="f614e-136">Forbedring af ydeevne</span><span class="sxs-lookup"><span data-stu-id="f614e-136">Performance Improvement</span></span>  
<span data-ttu-id="f614e-137">Ved at gemme dimensionsgrupper én gang i databasen, gemmes der plads i databasen, og den overordnede ydeevne forbedres.</span><span class="sxs-lookup"><span data-stu-id="f614e-137">By storing dimension sets once in the database, database space is preserved, and overall performance is improved.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f614e-138">Se også</span><span class="sxs-lookup"><span data-stu-id="f614e-138">See Also</span></span>  
<span data-ttu-id="f614e-139">[Designoplysninger: Søgning efter dimensionskombinationer](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="f614e-139">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
<span data-ttu-id="f614e-140">[Designoplysninger: Tabelstruktur](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="f614e-140">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
<span data-ttu-id="f614e-141">[Designoplysninger: Kodeenhed 408 Dimensionsstyring](design-details-codeunit-408-dimension-management.md) </span><span class="sxs-lookup"><span data-stu-id="f614e-141">[Design Details: Codeunit 408 Dimension Management](design-details-codeunit-408-dimension-management.md) </span></span>  
<span data-ttu-id="f614e-142">[Designoplysninger: Kodeeksempler af ændrede mønstre i Ændringer](design-details-code-examples-of-changed-patterns-in-modifications.md) </span><span class="sxs-lookup"><span data-stu-id="f614e-142">[Design Details: Code Examples of Changed Patterns in Modifications](design-details-code-examples-of-changed-patterns-in-modifications.md) </span></span>  
[<span data-ttu-id="f614e-143">Designoplysninger: Dimensionsgruppeposter</span><span class="sxs-lookup"><span data-stu-id="f614e-143">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)   

