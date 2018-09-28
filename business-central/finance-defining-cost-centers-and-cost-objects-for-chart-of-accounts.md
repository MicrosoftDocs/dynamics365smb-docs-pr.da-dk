---
title: Definere omkostningssteder og omkostningsemner for kontoplanen | Microsoft Docs
description: "Du kan automatisk overføre posterne udgifter og indtægter fra regnskabet til omkostningsregnskab, enten for hver bogføring til regnskab eller med et batchjob. Når du foretager overførslen, overfører systemet kun de poster, der allerede er knyttet til et omkostningssted eller et omkostningsobjekt. For at oprette en relevant overførsel skal du sikre omkostningssteder og omkostningsobjekter er korrekt defineret."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8bbfcad34b0b717d961ccd2ebe3eb095aaef1335
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a><span data-ttu-id="c047e-105">Definition af omkostningssteder og omkostningsobjekter for kontoplanen</span><span class="sxs-lookup"><span data-stu-id="c047e-105">Defining Cost Centers and Cost Objects for Chart of Accounts</span></span>
<span data-ttu-id="c047e-106">Du kan automatisk overføre posterne udgifter og indtægter fra regnskabet til omkostningsregnskab, enten for hver bogføring til regnskab eller med et batchjob.</span><span class="sxs-lookup"><span data-stu-id="c047e-106">You can automatically transfer the expense and income entries from the general ledger to cost accounting either for each general ledger posting or with a batch job.</span></span> <span data-ttu-id="c047e-107">Når du foretager overførslen, overfører [!INCLUDE[d365fin](includes/d365fin_md.md)] kun de poster, der allerede er knyttet til et omkostningssted eller et omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="c047e-107">When you do the transfer, [!INCLUDE[d365fin](includes/d365fin_md.md)] only transfers the entries that are already linked to a cost center or a cost object.</span></span> <span data-ttu-id="c047e-108">For at oprette en relevant overførsel skal du sikre omkostningssteder og omkostningsobjekter er korrekt defineret.</span><span class="sxs-lookup"><span data-stu-id="c047e-108">To establish a meaningful transfer, you must ensure that the cost centers and cost objects are correctly defined.</span></span>  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a><span data-ttu-id="c047e-109">Definere standarddimensionsværdier for finanskonti</span><span class="sxs-lookup"><span data-stu-id="c047e-109">Defining Default Dimension Values for General Ledger Accounts</span></span>  
<span data-ttu-id="c047e-110">For hver enkelt finanskonto kan du definere standarddimensionsværdier i tabellen **Standarddimension**.</span><span class="sxs-lookup"><span data-stu-id="c047e-110">For each general ledger account, you can define default dimension values in the **Default Dimension** table.</span></span> <span data-ttu-id="c047e-111">Følgende eksempel viser, hvordan du definerer, at der altid skal være et omkostningssted DEPARTMENT, men aldrig et omkostningsobjekt PROJECT, når du bogfører til en finanskonto.</span><span class="sxs-lookup"><span data-stu-id="c047e-111">The following example shows how to define that there should always be a DEPARTMENT cost center, but never be a PROJECT cost object when posting to a general ledger account.</span></span>  

|<span data-ttu-id="c047e-112">**Dimensionskode**</span><span class="sxs-lookup"><span data-stu-id="c047e-112">**Dimension Code**</span></span>|<span data-ttu-id="c047e-113">**Værdibogføring**</span><span class="sxs-lookup"><span data-stu-id="c047e-113">**Value Posting**</span></span>|  
|------------------------------------------|-----------------------------------------|  
|<span data-ttu-id="c047e-114">Afdeling</span><span class="sxs-lookup"><span data-stu-id="c047e-114">Department</span></span>|<span data-ttu-id="c047e-115">Tvungen kode</span><span class="sxs-lookup"><span data-stu-id="c047e-115">Code Mandatory</span></span>|  
|<span data-ttu-id="c047e-116">Projekt</span><span class="sxs-lookup"><span data-stu-id="c047e-116">Project</span></span>|<span data-ttu-id="c047e-117">Ingen kode</span><span class="sxs-lookup"><span data-stu-id="c047e-117">No Code</span></span>|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a><span data-ttu-id="c047e-118">Definition af dimensionsværdier for faste og direkte omkostninger</span><span class="sxs-lookup"><span data-stu-id="c047e-118">Defining Dimension Values for Overhead Costs and Direct Costs</span></span>  
 <span data-ttu-id="c047e-119">Du kan overføre faste omkostninger til et omkostningssted og direkte omkostninger til et omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="c047e-119">You can transfer overhead costs to a cost center and direct costs to a cost object.</span></span> <span data-ttu-id="c047e-120">Følgende tabel viser den optimale kombination af dimensionsopsætningsværdierne.</span><span class="sxs-lookup"><span data-stu-id="c047e-120">The following table shows the optimal combination of the dimension setup values.</span></span>  

|<span data-ttu-id="c047e-121">Kopiér til</span><span class="sxs-lookup"><span data-stu-id="c047e-121">Transfer To</span></span>|<span data-ttu-id="c047e-122">Omkostningsstedbogføring</span><span class="sxs-lookup"><span data-stu-id="c047e-122">Cost Center Posting</span></span>|<span data-ttu-id="c047e-123">Omkostningsobjektbogføring</span><span class="sxs-lookup"><span data-stu-id="c047e-123">Cost Object Posting</span></span>|  
|-----------------|-------------------------|-------------------------|  
|<span data-ttu-id="c047e-124">Omkostningssted</span><span class="sxs-lookup"><span data-stu-id="c047e-124">Cost Center</span></span>|<span data-ttu-id="c047e-125">Tvungen kode</span><span class="sxs-lookup"><span data-stu-id="c047e-125">Code Mandatory</span></span>|<span data-ttu-id="c047e-126">Ingen kode</span><span class="sxs-lookup"><span data-stu-id="c047e-126">No Code</span></span>|  
|<span data-ttu-id="c047e-127">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="c047e-127">Cost Object</span></span>|<span data-ttu-id="c047e-128">Ingen kode</span><span class="sxs-lookup"><span data-stu-id="c047e-128">No Code</span></span>|<span data-ttu-id="c047e-129">Tvungen kode</span><span class="sxs-lookup"><span data-stu-id="c047e-129">Code Mandatory</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="c047e-130">For at sikre, at det foruddefinerede omkostningssted og omkostningsemne, du har oprettet i regnskabet, automatisk overføres til omkostningsregnskab, skal du markere afkrydsningsfeltet **Kontroller finansbogføringer** i vinduet Konfiguration af omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="c047e-130">To make sure that the predefined cost center and cost object that you set up in the general ledger are automatically carried over to cost accounting, select the **Check G/L Postings** check box in the Cost Accounting Setup window.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c047e-131">Se også</span><span class="sxs-lookup"><span data-stu-id="c047e-131">See Also</span></span>  
[<span data-ttu-id="c047e-132">Regnskab for omkostninger</span><span class="sxs-lookup"><span data-stu-id="c047e-132">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="c047e-133">[Oprette omkostningssteder](finance-how-to-set-up-cost-centers.md) </span><span class="sxs-lookup"><span data-stu-id="c047e-133">[Set Up Cost Centers](finance-how-to-set-up-cost-centers.md) </span></span>  
[<span data-ttu-id="c047e-134">Oprette omkostningsemner</span><span class="sxs-lookup"><span data-stu-id="c047e-134">Set Up Cost Objects</span></span>](finance-how-to-set-up-cost-objects.md)  
<span data-ttu-id="c047e-135">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c047e-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

