---
title: Definere omkostningssteder og omkostningsemner for kontoplanen | Microsoft Docs
description: "Du kan automatisk overføre posterne udgifter og indtægter fra regnskabet til omkostningsregnskab, enten for hver bogføring til regnskab eller med et batchjob. Når du foretager overførslen, overfører systemet kun de poster, der allerede er knyttet til et omkostningssted eller et omkostningsobjekt. For at oprette en relevant overførsel skal du sikre omkostningssteder og omkostningsobjekter er korrekt defineret."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 92ad393733c758304743ec0b63c98c1612e7240b
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a><span data-ttu-id="f8071-105">Definition af omkostningssteder og omkostningsobjekter for kontoplanen</span><span class="sxs-lookup"><span data-stu-id="f8071-105">Defining Cost Centers and Cost Objects for Chart of Accounts</span></span>
<span data-ttu-id="f8071-106">Du kan automatisk overføre posterne udgifter og indtægter fra regnskabet til omkostningsregnskab, enten for hver bogføring til regnskab eller med et batchjob.</span><span class="sxs-lookup"><span data-stu-id="f8071-106">You can automatically transfer the expense and income entries from the general ledger to cost accounting either for each general ledger posting or with a batch job.</span></span> <span data-ttu-id="f8071-107">Når du foretager overførslen, overfører [!INCLUDE[d365fin](includes/d365fin_md.md)] kun de poster, der allerede er knyttet til et omkostningssted eller et omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="f8071-107">When you do the transfer, [!INCLUDE[d365fin](includes/d365fin_md.md)] only transfers the entries that are already linked to a cost center or a cost object.</span></span> <span data-ttu-id="f8071-108">For at oprette en relevant overførsel skal du sikre omkostningssteder og omkostningsobjekter er korrekt defineret.</span><span class="sxs-lookup"><span data-stu-id="f8071-108">To establish a meaningful transfer, you must ensure that the cost centers and cost objects are correctly defined.</span></span>  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a><span data-ttu-id="f8071-109">Definere standarddimensionsværdier for finanskonti</span><span class="sxs-lookup"><span data-stu-id="f8071-109">Defining Default Dimension Values for General Ledger Accounts</span></span>  
<span data-ttu-id="f8071-110">For hver enkelt finanskonto kan du definere standarddimensionsværdier i tabellen **Standarddimension**.</span><span class="sxs-lookup"><span data-stu-id="f8071-110">For each general ledger account, you can define default dimension values in the **Default Dimension** table.</span></span> <span data-ttu-id="f8071-111">Følgende eksempel viser, hvordan du definerer, at der altid skal være et omkostningssted DEPARTMENT, men aldrig et omkostningsobjekt PROJECT, når du bogfører til en finanskonto.</span><span class="sxs-lookup"><span data-stu-id="f8071-111">The following example shows how to define that there should always be a DEPARTMENT cost center, but never be a PROJECT cost object when posting to a general ledger account.</span></span>  

|<span data-ttu-id="f8071-112">**Dimensionskode**</span><span class="sxs-lookup"><span data-stu-id="f8071-112">**Dimension Code**</span></span>|<span data-ttu-id="f8071-113">**Værdibogføring**</span><span class="sxs-lookup"><span data-stu-id="f8071-113">**Value Posting**</span></span>|  
|------------------------------------------|-----------------------------------------|  
|<span data-ttu-id="f8071-114">Afdeling</span><span class="sxs-lookup"><span data-stu-id="f8071-114">Department</span></span>|<span data-ttu-id="f8071-115">Tvungen kode</span><span class="sxs-lookup"><span data-stu-id="f8071-115">Code Mandatory</span></span>|  
|<span data-ttu-id="f8071-116">Projekt</span><span class="sxs-lookup"><span data-stu-id="f8071-116">Project</span></span>|<span data-ttu-id="f8071-117">Ingen kode</span><span class="sxs-lookup"><span data-stu-id="f8071-117">No Code</span></span>|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a><span data-ttu-id="f8071-118">Definition af dimensionsværdier for faste og direkte omkostninger</span><span class="sxs-lookup"><span data-stu-id="f8071-118">Defining Dimension Values for Overhead Costs and Direct Costs</span></span>  
 <span data-ttu-id="f8071-119">Du kan overføre faste omkostninger til et omkostningssted og direkte omkostninger til et omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="f8071-119">You can transfer overhead costs to a cost center and direct costs to a cost object.</span></span> <span data-ttu-id="f8071-120">Følgende tabel viser den optimale kombination af dimensionsopsætningsværdierne.</span><span class="sxs-lookup"><span data-stu-id="f8071-120">The following table shows the optimal combination of the dimension setup values.</span></span>  

|<span data-ttu-id="f8071-121">Kopiér til</span><span class="sxs-lookup"><span data-stu-id="f8071-121">Transfer To</span></span>|<span data-ttu-id="f8071-122">Omkostningsstedbogføring</span><span class="sxs-lookup"><span data-stu-id="f8071-122">Cost Center Posting</span></span>|<span data-ttu-id="f8071-123">Omkostningsobjektbogføring</span><span class="sxs-lookup"><span data-stu-id="f8071-123">Cost Object Posting</span></span>|  
|-----------------|-------------------------|-------------------------|  
|<span data-ttu-id="f8071-124">Omkostningssted</span><span class="sxs-lookup"><span data-stu-id="f8071-124">Cost Center</span></span>|<span data-ttu-id="f8071-125">Tvungen kode</span><span class="sxs-lookup"><span data-stu-id="f8071-125">Code Mandatory</span></span>|<span data-ttu-id="f8071-126">Ingen kode</span><span class="sxs-lookup"><span data-stu-id="f8071-126">No Code</span></span>|  
|<span data-ttu-id="f8071-127">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="f8071-127">Cost Object</span></span>|<span data-ttu-id="f8071-128">Ingen kode</span><span class="sxs-lookup"><span data-stu-id="f8071-128">No Code</span></span>|<span data-ttu-id="f8071-129">Tvungen kode</span><span class="sxs-lookup"><span data-stu-id="f8071-129">Code Mandatory</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="f8071-130">For at sikre, at det foruddefinerede omkostningssted og omkostningsemne, du har oprettet i regnskabet, automatisk overføres til omkostningsregnskab, skal du markere afkrydsningsfeltet **Kontroller finansbogføringer** i vinduet Konfiguration af omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="f8071-130">To make sure that the predefined cost center and cost object that you set up in the general ledger are automatically carried over to cost accounting, select the **Check G/L Postings** check box in the Cost Accounting Setup window.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f8071-131">Se også</span><span class="sxs-lookup"><span data-stu-id="f8071-131">See Also</span></span>  
[<span data-ttu-id="f8071-132">Regnskab for omkostninger</span><span class="sxs-lookup"><span data-stu-id="f8071-132">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="f8071-133">[Oprette omkostningssteder](finance-how-to-set-up-cost-centers.md) </span><span class="sxs-lookup"><span data-stu-id="f8071-133">[Set Up Cost Centers](finance-how-to-set-up-cost-centers.md) </span></span>  
[<span data-ttu-id="f8071-134">Oprette omkostningsemner</span><span class="sxs-lookup"><span data-stu-id="f8071-134">Set Up Cost Objects</span></span>](finance-how-to-set-up-cost-objects.md)  
<span data-ttu-id="f8071-135">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f8071-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

