---
title: "Designoplysninger – Prioritering af ordrer | Microsoft Docs"
description: "Yderligere oplysninger om, hvordan der skal prioriteres for at opfylde både behov og forsyningskrav."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, priority, prioritize, order, sku, demand, supply
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7af645f5a9dd7f34619d05cb2d4f0f7f8ad1921d
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-prioritizing-orders"></a><span data-ttu-id="faad4-103">Designoplysninger: Prioritering af ordrer</span><span class="sxs-lookup"><span data-stu-id="faad4-103">Design Details: Prioritizing Orders</span></span>
<span data-ttu-id="faad4-104">Inden for en given SKU repræsenterer den anmodede eller tilgængelige dato den højeste prioritet. Behovene i dag skal behandles før behovene for næste uge.</span><span class="sxs-lookup"><span data-stu-id="faad4-104">Within a given SKU, the requested or available date represents the highest priority; the demand of today should be dealt with before the demand of next week.</span></span> <span data-ttu-id="faad4-105">Men ud over denne overordnede prioritet foreslår planlægningssystemet også, hvilken type behov der skal være opfyldt, inden andre behov opfyldes.</span><span class="sxs-lookup"><span data-stu-id="faad4-105">But in addition to this overall priority, the planning system will also suggest which type of demand should be fulfilled before fulfilling another demand.</span></span> <span data-ttu-id="faad4-106">Det foreslås ligeledes, hvilken forsyningskilde der skal anvendes, før du anvender andre forsyningskilder.</span><span class="sxs-lookup"><span data-stu-id="faad4-106">Likewise, it will suggest what source of supply should be applied before applying other sources of supply.</span></span> <span data-ttu-id="faad4-107">Dette udføres i overensstemmelse med ordreprioriteter.</span><span class="sxs-lookup"><span data-stu-id="faad4-107">This is done according to order priorities.</span></span>  
  
<span data-ttu-id="faad4-108">Indlæst behov og forsyning, der bidrager til en profil for den planlagte lagerbeholdning i henhold til følgende prioriteter:</span><span class="sxs-lookup"><span data-stu-id="faad4-108">Loaded demand and supply contribute to a profile for the projected inventory according to the following priorities:</span></span>  
  
## <a name="priorities-on-the-demand-side"></a><span data-ttu-id="faad4-109">Prioriteter på efterspørgselssiden</span><span class="sxs-lookup"><span data-stu-id="faad4-109">Priorities on the Demand Side</span></span>  
1. <span data-ttu-id="faad4-110">Allerede leveret: varepost</span><span class="sxs-lookup"><span data-stu-id="faad4-110">Already shipped: Item Ledger Entry</span></span>  
2. <span data-ttu-id="faad4-111">Købsreturvareordre</span><span class="sxs-lookup"><span data-stu-id="faad4-111">Purchase Return Order</span></span>  
3. <span data-ttu-id="faad4-112">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="faad4-112">Sales Order</span></span>  
4. <span data-ttu-id="faad4-113">Serviceordre</span><span class="sxs-lookup"><span data-stu-id="faad4-113">Service Order</span></span>  
5. <span data-ttu-id="faad4-114">Produktionskomponentbehov</span><span class="sxs-lookup"><span data-stu-id="faad4-114">Production Component Need</span></span>  
6. <span data-ttu-id="faad4-115">Montageordrelinje</span><span class="sxs-lookup"><span data-stu-id="faad4-115">Assembly Order Line</span></span>  
7. <span data-ttu-id="faad4-116">Udgående overflytningsordre</span><span class="sxs-lookup"><span data-stu-id="faad4-116">Outbound Transfer Order</span></span>  
8. <span data-ttu-id="faad4-117">Rammeordre (der ikke allerede er brugt af relaterede salgsordrer)</span><span class="sxs-lookup"><span data-stu-id="faad4-117">Blanket Order (that has not already been consumed by related sales orders)</span></span>  
9. <span data-ttu-id="faad4-118">Forecast (der ikke allerede er anvendt af andre salgsordrer)</span><span class="sxs-lookup"><span data-stu-id="faad4-118">Forecast (that has not already been consumed by other sales orders)</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="faad4-119">Købsreturvarer er normalt ikke involveret i forsyningsplanlægning. De skal altid være reserveret fra det lot, der skal returneres.</span><span class="sxs-lookup"><span data-stu-id="faad4-119">Purchase returns are usually not involved in supply planning; they should always be reserved from the lot that is going to be returned.</span></span> <span data-ttu-id="faad4-120">Hvis den ikke er reserveret, spiller købsreturvarer en rolle i udbuddet og er højt prioriteret for at undgå, at planlægningssystemet foreslår en forsyningsordre, der blot skal tjene et købsreturnering.</span><span class="sxs-lookup"><span data-stu-id="faad4-120">If not reserved, purchase returns play a role in the availability and are highly prioritized to avoid that the planning system suggests a supply order just to serve a purchase return.</span></span>  
  
## <a name="priorities-on-the-supply-side"></a><span data-ttu-id="faad4-121">Prioriteter på forsyningssiden</span><span class="sxs-lookup"><span data-stu-id="faad4-121">Priorities on the Supply Side</span></span>  
1. <span data-ttu-id="faad4-122">Allerede på lager: Varepost (planlægningsfleksibilitet = ingen)</span><span class="sxs-lookup"><span data-stu-id="faad4-122">Already in inventory: Item Ledger Entry (Planning Flexibility = None)</span></span>  
2. <span data-ttu-id="faad4-123">Salgsreturvareordre (planlægningsfleksibilitet = ingen)</span><span class="sxs-lookup"><span data-stu-id="faad4-123">Sales Return Order (Planning Flexibility = None)</span></span>  
3. <span data-ttu-id="faad4-124">Indgående overflytningsordre</span><span class="sxs-lookup"><span data-stu-id="faad4-124">Inbound Transfer Order</span></span>  
4. <span data-ttu-id="faad4-125">Produktionsordre</span><span class="sxs-lookup"><span data-stu-id="faad4-125">Production Order</span></span>  
5. <span data-ttu-id="faad4-126">Montageordre</span><span class="sxs-lookup"><span data-stu-id="faad4-126">Assembly Order</span></span>  
6. <span data-ttu-id="faad4-127">Købsordre</span><span class="sxs-lookup"><span data-stu-id="faad4-127">Purchase Order</span></span>  
  
## <a name="priority-related-to-the-state-of-demand-and-supply"></a><span data-ttu-id="faad4-128">Prioritet, der er relateret til tilstand af efterspørgsel og udbud</span><span class="sxs-lookup"><span data-stu-id="faad4-128">Priority Related to the State of Demand and Supply</span></span>  
<span data-ttu-id="faad4-129">Bortset fra de prioriteter, der er angivet af typen af behov og forsyning, definerer den nuværende ordrestatus i udførelsesprocessen også en prioritet.</span><span class="sxs-lookup"><span data-stu-id="faad4-129">Apart from priorities given by the type of demand and supply, the present state of the orders in the execution process also defines a priority.</span></span> <span data-ttu-id="faad4-130">Lageraktiviteter har f.eks. indflydelse, og status for salg, køb, overførsel, montage og produktionsordrer tages i betragtning:</span><span class="sxs-lookup"><span data-stu-id="faad4-130">For example, warehouse activities have an impact, and the status of sales, purchase, transfer, assembly, and production orders is taken into account:</span></span>  
  
1. <span data-ttu-id="faad4-131">Delvist håndteres (planlægningsfleksibilitet = ingen)</span><span class="sxs-lookup"><span data-stu-id="faad4-131">Partly handled (Planning Flexibility = None)</span></span>  
2. <span data-ttu-id="faad4-132">Allerede under behandling i lageret (planlægningsfleksibilitet = ingen)</span><span class="sxs-lookup"><span data-stu-id="faad4-132">Already in process in the warehouse (Planning Flexibility = None)</span></span>  
3. <span data-ttu-id="faad4-133">Frigivet – alle ordretyper (planlægningsfleksibilitet = ubegrænset)</span><span class="sxs-lookup"><span data-stu-id="faad4-133">Released – all order types (Planning Flexibility = Unlimited)</span></span>  
4. <span data-ttu-id="faad4-134">Fastlagt og planlagt produktionsordre (planlægningsfleksibilitet = ubegrænset)</span><span class="sxs-lookup"><span data-stu-id="faad4-134">Firm Planned Production Order (Planning Flexibility = Unlimited)</span></span>  
5. <span data-ttu-id="faad4-135">Planlagt/åben – alle ordretyper (planlægningsfleksibilitet = ubegrænset)</span><span class="sxs-lookup"><span data-stu-id="faad4-135">Planned/Open – all order types (Planning Flexibility = Unlimited)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="faad4-136">Se også</span><span class="sxs-lookup"><span data-stu-id="faad4-136">See Also</span></span>  
<span data-ttu-id="faad4-137">[Designoplysninger: Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="faad4-137">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="faad4-138">[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="faad4-138">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="faad4-139">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="faad4-139">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)