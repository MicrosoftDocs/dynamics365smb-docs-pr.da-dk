---
title: "Designoplysninger – Håndtering af genbestillingsmetoder | Microsoft Docs"
description: "Oversigt over opgaver til at definere en genbestillingsmetode i forsyningsplanlægning."
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
ms.openlocfilehash: 2a6658508f8e12a11989d54da6d6c8e3a36631cc
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-handling-reordering-policies"></a><span data-ttu-id="3458a-103">Designoplysninger: Håndtering af genbestillingsmetoder</span><span class="sxs-lookup"><span data-stu-id="3458a-103">Design Details: Handling Reordering Policies</span></span>
<span data-ttu-id="3458a-104">En genbestillingsmetode skal defineres for, at en vare kan være en del af forsyningsplanlægning.</span><span class="sxs-lookup"><span data-stu-id="3458a-104">For an item to participate in supply planning, a reorder policy must be defined.</span></span> <span data-ttu-id="3458a-105">Der findes følgende fire genbestillingsmetoder:</span><span class="sxs-lookup"><span data-stu-id="3458a-105">The following four reordering policies exist:</span></span>  
  
* <span data-ttu-id="3458a-106">Fast genbestil.antal</span><span class="sxs-lookup"><span data-stu-id="3458a-106">Fixed Reorder Qty.</span></span>  
* <span data-ttu-id="3458a-107">Maks. antal</span><span class="sxs-lookup"><span data-stu-id="3458a-107">Maximum Qty.</span></span>  
* <span data-ttu-id="3458a-108">Ordre</span><span class="sxs-lookup"><span data-stu-id="3458a-108">Order</span></span>  
* <span data-ttu-id="3458a-109">Lot-for-Lot</span><span class="sxs-lookup"><span data-stu-id="3458a-109">Lot-for-Lot</span></span>  
  
<span data-ttu-id="3458a-110">Fast genbestil.antal- og Maks. antal-metoder, der er relateret til lagerplanlægning.</span><span class="sxs-lookup"><span data-stu-id="3458a-110">Fixed Reorder Qty. and Maximum Qty. policies relate to inventory planning.</span></span> <span data-ttu-id="3458a-111">Selvom lagerplanlægning er teknisk enklere end udligningsproceduren, skal disse politikker fungere sammen med den trinvise afstemning af forsyning og ordresporing.</span><span class="sxs-lookup"><span data-stu-id="3458a-111">Although inventory planning is technically simpler than the balancing procedure, these policies must coexist with the step-by-step balancing of supply and order tracking.</span></span> <span data-ttu-id="3458a-112">For at styre integrationen mellem de to og for at give indsigt i den involverede planlægningslogik styrer strenge principper, hvordan genbestillingsmetoder håndteres.</span><span class="sxs-lookup"><span data-stu-id="3458a-112">To control the integration between the two, and to provide visibility into the involved planning logic, strict principles govern how reordering policies are handled.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="3458a-113">Dette afsnit indeholder</span><span class="sxs-lookup"><span data-stu-id="3458a-113">In This Section</span></span>  
[<span data-ttu-id="3458a-114">Designoplysninger: Genbestillingspunktets rolle</span><span class="sxs-lookup"><span data-stu-id="3458a-114">Design Details: The Role of the Reorder Point</span></span>](design-details-the-role-of-the-reorder-point.md)  
[<span data-ttu-id="3458a-115">Designoplysninger: Overvågning af det forventede lagerniveau og genbestillingspunktet</span><span class="sxs-lookup"><span data-stu-id="3458a-115">Design Details: Monitoring the Projected Inventory Level and the Reorder Point</span></span>](design-details-monitoring-the-projected-inventory-level-and-the-reorder-point.md)  
[<span data-ttu-id="3458a-116">Designoplysninger: Intervallets rolle</span><span class="sxs-lookup"><span data-stu-id="3458a-116">Design Details: The Role of the Time Bucket</span></span>](design-details-the-role-of-the-time-bucket.md)  
[<span data-ttu-id="3458a-117">Designoplysninger: Forblive under overløbsniveauet</span><span class="sxs-lookup"><span data-stu-id="3458a-117">Design Details: Staying under the Overflow Level</span></span>](design-details-staying-under-the-overflow-level.md)  
[<span data-ttu-id="3458a-118">Designoplysninger: Håndtering af forventet negativt lager</span><span class="sxs-lookup"><span data-stu-id="3458a-118">Design Details: Handling Projected Negative Inventory</span></span>](design-details-handling-projected-negative-inventory.md)  
[<span data-ttu-id="3458a-119">Designoplysninger: Genbestillingsmetoder</span><span class="sxs-lookup"><span data-stu-id="3458a-119">Design Details: Reordering Policies</span></span>](design-details-reordering-policies.md)  
  
## <a name="see-also"></a><span data-ttu-id="3458a-120">Se også</span><span class="sxs-lookup"><span data-stu-id="3458a-120">See Also</span></span>  
<span data-ttu-id="3458a-121">[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="3458a-121">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="3458a-122">[Designoplysninger: Tabellen Planlægningsopgave](design-details-planning-assignment-table.md) </span><span class="sxs-lookup"><span data-stu-id="3458a-122">[Design Details: Planning Assignment Table](design-details-planning-assignment-table.md) </span></span>  
<span data-ttu-id="3458a-123">[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="3458a-123">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
<span data-ttu-id="3458a-124">[Designoplysninger: Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="3458a-124">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
[<span data-ttu-id="3458a-125">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="3458a-125">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
