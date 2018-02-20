---
title: Definere og allokere omkostninger | Microsoft Docs
description: "Allokering af omkostninger flytter omkostninger og indtægter mellem omkostningstyper, omkostningssteder og omkostningsobjekter. Du kan angive så mange tildelinger, som du har brug for."
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
ms.openlocfilehash: 04e5a95b7a926528cc26c254390d08e3bce6ad8a
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="defining-and-allocating-costs"></a><span data-ttu-id="3b7e7-104">Definere og allokere omkostninger</span><span class="sxs-lookup"><span data-stu-id="3b7e7-104">Defining and Allocating Costs</span></span>
<span data-ttu-id="3b7e7-105">Allokering af omkostninger flytter omkostninger og indtægter mellem omkostningstyper, omkostningssteder og omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="3b7e7-105">Cost allocations move costs and revenues between cost types, cost centers, and cost objects.</span></span> <span data-ttu-id="3b7e7-106">Du kan angive så mange tildelinger, som du har brug for.</span><span class="sxs-lookup"><span data-stu-id="3b7e7-106">You can define as many allocations as you need.</span></span> <span data-ttu-id="3b7e7-107">Hver allokering består af:</span><span class="sxs-lookup"><span data-stu-id="3b7e7-107">Each allocation consists of:</span></span>  

-   <span data-ttu-id="3b7e7-108">En fordelingskilde.</span><span class="sxs-lookup"><span data-stu-id="3b7e7-108">An allocation source.</span></span>  
-   <span data-ttu-id="3b7e7-109">Et eller flere allokeringsmål.</span><span class="sxs-lookup"><span data-stu-id="3b7e7-109">One or more allocation targets.</span></span>  

<span data-ttu-id="3b7e7-110">Fordelingskilden fastlægger, hvilke omkostninger der skal fordeles, og allokeringsmål bestemmer, hvor omkostningerne skal fordeles til.</span><span class="sxs-lookup"><span data-stu-id="3b7e7-110">The allocation source establishes which costs must be allocated, and the allocation targets determine where the costs must be allocated.</span></span> <span data-ttu-id="3b7e7-111">F.eks. kan en fordelingskilde være omkostningerne for omkostningstypen Elektricitet og varme.</span><span class="sxs-lookup"><span data-stu-id="3b7e7-111">For example, an allocation source can be the costs for the Electricity and Heating cost type.</span></span> <span data-ttu-id="3b7e7-112">Du allokerer alle el- og varmeomkostninger til tre omkostningssteder: Workshop, produktion og salg.</span><span class="sxs-lookup"><span data-stu-id="3b7e7-112">You allocate all electricity and heating costs to three cost centers: Workshop, Production, and Sales.</span></span> <span data-ttu-id="3b7e7-113">Disse omkostningssteder er dine fordelingsmål.</span><span class="sxs-lookup"><span data-stu-id="3b7e7-113">These cost centers are your allocation targets.</span></span>  

<span data-ttu-id="3b7e7-114">For hver fordelingskilde skal du definere et fordelingsniveau, en gyldighedsperiode og en variant som gruppe-id.</span><span class="sxs-lookup"><span data-stu-id="3b7e7-114">For each allocation source, you define an allocation level, a validity period, and a variant as grouping identifier.</span></span> <span data-ttu-id="3b7e7-115">Du kan bruge et batchjob til at angive filtre til valg af allokeringsdefinitioner og derefter køre allokering af omkostninger automatisk.</span><span class="sxs-lookup"><span data-stu-id="3b7e7-115">You can use a batch job to set filters to select allocation definitions and then run cost allocations automatically.</span></span>  

<span data-ttu-id="3b7e7-116">Du kan definere en fordelingsbasis for hvert fordelingsmål.</span><span class="sxs-lookup"><span data-stu-id="3b7e7-116">For each allocation target, you define an allocation base.</span></span> <span data-ttu-id="3b7e7-117">Fordelingsbasis kan være enten statisk eller dynamisk.</span><span class="sxs-lookup"><span data-stu-id="3b7e7-117">The allocation base can be either static or dynamic.</span></span>  

-   <span data-ttu-id="3b7e7-118">Statisk allokeringsbasis er baseret på en endelig værdi, for eksempel anvendt antal kvadratmeter eller et etableret fordelingsforhold såsom 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="3b7e7-118">Static allocation bases are based on a definite value, such as square footage or an established allocation ratio, such as 5:2:4.</span></span>  
-   <span data-ttu-id="3b7e7-119">Dynamisk fordelingsbasis afhænger af værdier, der kan ændres, f.eks antallet af medarbejdere på et omkostningssted eller salgsindtægter fra et omkostningsobjekt i en bestemt tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="3b7e7-119">Dynamic allocation bases depend on changeable values, such as the number of employees in a cost center or sales revenue of a cost object throughout a certain time period.</span></span>  

<span data-ttu-id="3b7e7-120">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="3b7e7-120">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="3b7e7-121">Til</span><span class="sxs-lookup"><span data-stu-id="3b7e7-121">To</span></span>|<span data-ttu-id="3b7e7-122">Se</span><span class="sxs-lookup"><span data-stu-id="3b7e7-122">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="3b7e7-123">Konfigurer fordelingskilde og dens mål.</span><span class="sxs-lookup"><span data-stu-id="3b7e7-123">Set up allocation source and its targets.</span></span>|[<span data-ttu-id="3b7e7-124">Konfigurere fordelingskilde og mål</span><span class="sxs-lookup"><span data-stu-id="3b7e7-124">Set Up Allocation Source and Targets</span></span>](finance-how-to-set-up-allocation-source-and-targets.md)|  
|<span data-ttu-id="3b7e7-125">Konfigurer forskellige filtre for dynamiske fordelingsbaser.</span><span class="sxs-lookup"><span data-stu-id="3b7e7-125">Set up various filters for dynamic allocation bases.</span></span>|[<span data-ttu-id="3b7e7-126">Indstilling af filtre for dynamiske allokeringsbaser</span><span class="sxs-lookup"><span data-stu-id="3b7e7-126">Setting Filters for Dynamic Allocation Bases</span></span>](finance-setting-filters-for-dynamic-allocation-bases.md)|  
|<span data-ttu-id="3b7e7-127">Se et eksempel på, hvordan du definerer en statisk allokering.</span><span class="sxs-lookup"><span data-stu-id="3b7e7-127">See an example of how to define a static allocation.</span></span>|[<span data-ttu-id="3b7e7-128">Scenarieeksempel: Definition af statisk allokeringer baseret på fordelingsforholdet</span><span class="sxs-lookup"><span data-stu-id="3b7e7-128">Scenario Example: Defining Static Allocations Based on Allocation Ratio</span></span>](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)|  
|<span data-ttu-id="3b7e7-129">Se et eksempel på, hvordan du definerer en dynamisk fordeling.</span><span class="sxs-lookup"><span data-stu-id="3b7e7-129">See an example of how to define a dynamic allocation.</span></span>|[<span data-ttu-id="3b7e7-130">Scenarieeksempel: Definition af dynamiske fordelinger baseret på solgte varer</span><span class="sxs-lookup"><span data-stu-id="3b7e7-130">Scenario Example: Defining Dynamic Allocations Based on Items Sold</span></span>](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)|  

## <a name="see-also"></a><span data-ttu-id="3b7e7-131">Se også</span><span class="sxs-lookup"><span data-stu-id="3b7e7-131">See Also</span></span>  
 <span data-ttu-id="3b7e7-132">[Konfigurere omkostningsregnskab](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="3b7e7-132">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
 <span data-ttu-id="3b7e7-133">[Overførsel og bogføring af omkostningsposter](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="3b7e7-133">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="3b7e7-134">[Regnskab for omkostninger](finance-manage-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="3b7e7-134">[Accounting for Costs](finance-manage-cost-accounting.md) </span></span>  
 <span data-ttu-id="3b7e7-135">[Terminologi i omkostningsregnskab](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="3b7e7-135">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
 [<span data-ttu-id="3b7e7-136">Om omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="3b7e7-136">About Cost Accounting</span></span>](finance-about-cost-accounting.md)

