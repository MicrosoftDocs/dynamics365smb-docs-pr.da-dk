---
title: Oversigt over dimensionsgruppeposter | Microsoft Docs
description: Dette emne beskriver, hvordan dimensionsgruppeposter gemmes og bogføres i Dynamics 365.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 40f6a55adc0c2ade279638b43136475d81cb2c58
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751676"
---
# <a name="dimension-set-entries-overview"></a><span data-ttu-id="faadd-103">Oversigt over dimensionsgruppeposter</span><span class="sxs-lookup"><span data-stu-id="faadd-103">Dimension Set Entries Overview</span></span>
<span data-ttu-id="faadd-104">Dette emne beskriver, hvordan dimensionsgruppeposter gemmes og bogføres i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="faadd-104">This topic describes how dimension set entries are stored and posted in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="dimension-sets"></a><span data-ttu-id="faadd-105">Dimensionsopsætninger</span><span class="sxs-lookup"><span data-stu-id="faadd-105">Dimension Sets</span></span>  
<span data-ttu-id="faadd-106">En dimensionsgruppe er en entydig kombination af dimensionsværdier.</span><span class="sxs-lookup"><span data-stu-id="faadd-106">A dimension set is a unique combination of dimension values.</span></span> <span data-ttu-id="faadd-107">Det er gemt som dimensionsgruppeposter i databasen.</span><span class="sxs-lookup"><span data-stu-id="faadd-107">It is stored as dimension set entries in the database.</span></span> <span data-ttu-id="faadd-108">Hver dimensionsgruppepost repræsenterer en enkelt dimensionsværdi.</span><span class="sxs-lookup"><span data-stu-id="faadd-108">Each dimension set entry represents a single dimension value.</span></span> <span data-ttu-id="faadd-109">Dimensionsgruppen er identificeret med en fælles dimensionsgruppe-id, der tildeles til hver dimensionsgruppepost, der hører til dimensionsgruppen.</span><span class="sxs-lookup"><span data-stu-id="faadd-109">The dimension set is identified by a common dimension set ID that is assigned to each dimension set entry that belongs to the dimension set.</span></span>  

<span data-ttu-id="faadd-110">Følgende eksempel viser en dimensionsgruppe, der har tre poster for dimensionsgruppe .</span><span class="sxs-lookup"><span data-stu-id="faadd-110">The following example shows a dimension set that has three dimension set entries.</span></span> <span data-ttu-id="faadd-111">Dimensionsgruppe er identificeret med en dimensionsgruppe-id, som er 108.</span><span class="sxs-lookup"><span data-stu-id="faadd-111">The dimension set is identified by a dimension set ID, which is 108.</span></span>  

|<span data-ttu-id="faadd-112">Dimensionsgruppe-id</span><span class="sxs-lookup"><span data-stu-id="faadd-112">Dimension Set ID</span></span>|<span data-ttu-id="faadd-113">Dimensionskode</span><span class="sxs-lookup"><span data-stu-id="faadd-113">Dimension Code</span></span>|<span data-ttu-id="faadd-114">Dimensionsværdikode</span><span class="sxs-lookup"><span data-stu-id="faadd-114">Dimension Value Code</span></span>|<span data-ttu-id="faadd-115">Dimensionsværdinavn</span><span class="sxs-lookup"><span data-stu-id="faadd-115">Dimension Value Name</span></span>|  
|----------------------|--------------------|--------------------------|--------------------------|  
|<span data-ttu-id="faadd-116">108</span><span class="sxs-lookup"><span data-stu-id="faadd-116">108</span></span>|<span data-ttu-id="faadd-117">OMRÅDE</span><span class="sxs-lookup"><span data-stu-id="faadd-117">AREA</span></span>|<span data-ttu-id="faadd-118">70</span><span class="sxs-lookup"><span data-stu-id="faadd-118">70</span></span>|<span data-ttu-id="faadd-119">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="faadd-119">America North</span></span>|  
|<span data-ttu-id="faadd-120">108</span><span class="sxs-lookup"><span data-stu-id="faadd-120">108</span></span>|<span data-ttu-id="faadd-121">FORRETNINGSGRUPPE</span><span class="sxs-lookup"><span data-stu-id="faadd-121">BUSINESSGROUP</span></span>|<span data-ttu-id="faadd-122">HOME</span><span class="sxs-lookup"><span data-stu-id="faadd-122">HOME</span></span>|<span data-ttu-id="faadd-123">Start</span><span class="sxs-lookup"><span data-stu-id="faadd-123">Home</span></span>|  
|<span data-ttu-id="faadd-124">108</span><span class="sxs-lookup"><span data-stu-id="faadd-124">108</span></span>|<span data-ttu-id="faadd-125">AFDELING</span><span class="sxs-lookup"><span data-stu-id="faadd-125">DEPARTMENT</span></span>|<span data-ttu-id="faadd-126">SALG</span><span class="sxs-lookup"><span data-stu-id="faadd-126">SALES</span></span>|<span data-ttu-id="faadd-127">Salg</span><span class="sxs-lookup"><span data-stu-id="faadd-127">Sales</span></span>|  

## <a name="dimension-set-entries"></a><span data-ttu-id="faadd-128">Dimensionsgruppeposter</span><span class="sxs-lookup"><span data-stu-id="faadd-128">Dimension Set Entries</span></span>  
<span data-ttu-id="faadd-129">Dimensionsgrupper er gemt i tabellen **Dimensionsgruppepost** som dimensionsgruppeposter med samme dimensionsgruppe-id.</span><span class="sxs-lookup"><span data-stu-id="faadd-129">Dimension sets are stored in the **Dimension Set Entry** table as dimension set entries with the same dimension set ID.</span></span>  

<span data-ttu-id="faadd-130">![Flow af dimensionsgruppeposter](media/dimensionentrynav7.png "Flow af dimensionsgruppeposter")</span><span class="sxs-lookup"><span data-stu-id="faadd-130">![Flow of dimension set entries](media/dimensionentrynav7.png "Flow of dimension set entries")</span></span>  

<span data-ttu-id="faadd-131">Når du opretter en ny kladdelinje, et nyt bilagshoved eller en ny bilagslinje, kan du angive en kombination af dimensionsværdier.</span><span class="sxs-lookup"><span data-stu-id="faadd-131">When you create a new journal line, document header, or document line, you can specify a combination of dimension values.</span></span> <span data-ttu-id="faadd-132">I stedet for at eksplicit at gemme hver dimensionsværdi i databasen, tildeles kladdelinjen, bilagshovedet eller bilagslinjen en dimensionsgruppe-id, der angiver dimensionsgruppen.</span><span class="sxs-lookup"><span data-stu-id="faadd-132">Instead of explicitly storing each dimension value in the database, a dimension set ID is assigned to the journal line, document header, or document line to specify the dimension set.</span></span>  

<span data-ttu-id="faadd-133">Når du redigerer og lukker siden **Rediger dimensionsgruppeposter** udføres en kontrol for at se, om kombinationen af dimensionsværdier findes som en dimensionsgruppe i tabellen.</span><span class="sxs-lookup"><span data-stu-id="faadd-133">When you edit and close the **Edit Dimension Set Entries** page, a check is performed to see whether the combination of dimension values exists as a dimension set in the table.</span></span> <span data-ttu-id="faadd-134">Hvis kombinationen findes i tabellen, tildeles den tilsvarende dimensionsgruppe-id til kladdelinjen, bilagshovedet eller bilagslinjen.</span><span class="sxs-lookup"><span data-stu-id="faadd-134">If the combination occurs in the table, then the corresponding dimension set ID is assigned to the journal line, document header, or document line.</span></span> <span data-ttu-id="faadd-135">Ellers tilføjes en ny dimensionsgruppe til tabellen, og den nye dimensionsgruppe-id knyttes til kladdelinjen, bilagshovedet eller bilagslinjen.</span><span class="sxs-lookup"><span data-stu-id="faadd-135">Otherwise, a new dimension set is added to the table, and the new dimension set ID is assigned to the journal line, document header, or document line.</span></span>

## <a name="codeunit-408-dimension-management"></a><span data-ttu-id="faadd-136">Codeunit 408 Dimensionsstyring</span><span class="sxs-lookup"><span data-stu-id="faadd-136">Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="faadd-137">Codeunit 408 Dimensionsstyring er et funktionsbibliotek, der håndterer almindelige opgaver, der er relateret til dimensioner, f.eks. kopiering fra én tabel til en anden eller fra et dokument til en andet.</span><span class="sxs-lookup"><span data-stu-id="faadd-137">Codeunit 408, Dimension Management, is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span>

## <a name="performance-improvement"></a><span data-ttu-id="faadd-138">Forbedring af ydeevne</span><span class="sxs-lookup"><span data-stu-id="faadd-138">Performance Improvement</span></span>  
<span data-ttu-id="faadd-139">Ved at gemme dimensionsgrupper én gang i databasen gemmes der plads i databasen, og den overordnede ydeevne forbedres.</span><span class="sxs-lookup"><span data-stu-id="faadd-139">By storing dimension sets once in the database, database space is preserved and overall performance is improved.</span></span>  

## <a name="see-also"></a><span data-ttu-id="faadd-140">Se også</span><span class="sxs-lookup"><span data-stu-id="faadd-140">See Also</span></span>  
<span data-ttu-id="faadd-141">[Designoplysninger: Søgning efter dimensionskombinationer](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="faadd-141">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
<span data-ttu-id="faadd-142">[Designoplysninger: Tabelstruktur](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="faadd-142">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
[<span data-ttu-id="faadd-143">Designoplysninger: Dimensionsgruppeposter</span><span class="sxs-lookup"><span data-stu-id="faadd-143">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)   
