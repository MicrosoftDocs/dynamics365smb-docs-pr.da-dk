---
title: Designoplysninger – Håndtering af ordrer før planlægningsstartdatoen | Microsoft Docs
description: Dette emne beskriver de regler, planlægningen anvender for ordrer i den frosne zone.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: planning, frozen, design serial, lot
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: 32c523eda09620bd74df53f09bc103a44fbb367a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "919770"
---
# <a name="design-details-dealing-with-orders-before-the-planning-starting-date"></a><span data-ttu-id="f65b0-103">Designoplysninger: Håndtering af ordrer før planlægningsstartdatoen</span><span class="sxs-lookup"><span data-stu-id="f65b0-103">Design Details: Dealing with Orders Before the Planning Starting Date</span></span>
<span data-ttu-id="f65b0-104">For at undgå, at en forsyningsplan viser umulige og derfor ubrugelige forslag, anser planlægningssystemet perioden indtil den planlagte startdato for en frossen zone, hvor intet er planlagt.</span><span class="sxs-lookup"><span data-stu-id="f65b0-104">To avoid that a supply plan shows impossible and therefore useless suggestions, the planning system regards the period up until the planning starting date a frozen zone where nothing is planned for.</span></span> <span data-ttu-id="f65b0-105">Følgende regel gælder for den frosne zone:</span><span class="sxs-lookup"><span data-stu-id="f65b0-105">The following rule applies to the frozen zone:</span></span>  

<span data-ttu-id="f65b0-106">Alle forsyninger og behov før startdatoen for planlægningsperioden vil blive betragtet som en del af lagerbeholdningen eller leveret.</span><span class="sxs-lookup"><span data-stu-id="f65b0-106">All supply and demand before the starting date of the planning period will be considered a part of inventory or shipped.</span></span>  

<span data-ttu-id="f65b0-107">Derfor vil planlægningssystemet ikke, med nogle få undtagelser, foreslå ændringer til forsyningsordrer i den frosne zone, og der oprettes eller vedligeholdes ingen ordresporingslinks for den pågældende periode.</span><span class="sxs-lookup"><span data-stu-id="f65b0-107">Accordingly, the planning system will not, with a few exceptions, suggest any changes to supply orders in the frozen zone, and no order tracking links are created or maintained for that period.</span></span>  

<span data-ttu-id="f65b0-108">Undtagelser til denne regel er som følger:</span><span class="sxs-lookup"><span data-stu-id="f65b0-108">The exceptions to this rule are as follows:</span></span>  

* <span data-ttu-id="f65b0-109">Hvis den forventede disponible beholdning, herunder summen af forsyning og behov i den frosne zone, er under nul.</span><span class="sxs-lookup"><span data-stu-id="f65b0-109">If the projected available inventory, including the sum of supply and demand in the frozen zone, is below zero.</span></span>  
* <span data-ttu-id="f65b0-110">Hvis der kræves serienumre/lotnumre på den eller de tilbagedaterede ordrer.</span><span class="sxs-lookup"><span data-stu-id="f65b0-110">If serial/lot numbers are required on the backdated order(s).</span></span>  
* <span data-ttu-id="f65b0-111">Hvis forsyning-behov-sæt er sammenkædet af en ordre-til-ordre-politik.</span><span class="sxs-lookup"><span data-stu-id="f65b0-111">If the supply-demand set is linked by an order-to-order policy.</span></span>  

<span data-ttu-id="f65b0-112">Hvis den første disponible lagerbeholdning er under nul, foreslås der en nødforsyningsordre dagen før planlægningsperioden til at dække den manglende mængde.</span><span class="sxs-lookup"><span data-stu-id="f65b0-112">If the initial available inventory is below zero, the planning system suggests an emergency supply order on the day before the planning period to cover the missing quantity.</span></span> <span data-ttu-id="f65b0-113">Derfor vil den forventede og disponible lagerbeholdning altid være mindst nul, når planlægningen for den fremtidige periode begynder.</span><span class="sxs-lookup"><span data-stu-id="f65b0-113">Consequently, the projected and available inventory will always be at least zero when planning for the future period begins.</span></span> <span data-ttu-id="f65b0-114">Planlægningslinjen for denne forsyningsordre viser et Nødsituation-advarselsikon, og yderligere oplysninger kan findes ved opslag.</span><span class="sxs-lookup"><span data-stu-id="f65b0-114">The planning line for this supply order will display an Emergency warning icon and additional information is provided upon lookup.</span></span>  

## <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a><span data-ttu-id="f65b0-115">Serienumre/lotnumre og ordre-til-ordre-links er fritaget fra den frosne zone</span><span class="sxs-lookup"><span data-stu-id="f65b0-115">Serial/Lot Numbers and Order-to-Order Links are Exempt from the Frozen Zone</span></span>  
<span data-ttu-id="f65b0-116">Hvis serienumre/lotnumre er nødvendige eller findes i en ordre-til-ordre-link, vil planlægningssystemet se bort fra den frosne zone og indarbejde disse mængder, der er dateret tilbage fra startdatoen, og potentielt foreslå korrigerende handlinger, hvis behov og forsyning ikke er synkroniseret.</span><span class="sxs-lookup"><span data-stu-id="f65b0-116">If serial/lot numbers are required or an order-to-order link exists, the planning system will disregard the frozen zone and incorporate such quantities that are back-dated from the starting date and potentially suggest corrective actions if demand and supply is not synchronized.</span></span> <span data-ttu-id="f65b0-117">Forretningsårsagen til dette princip er, at sådanne specifikke behov-forsyningssæt skal stemme overens for at sikre, at dette specifikke behov er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="f65b0-117">The business reason for this principle is that such specific demand-supply sets must match to ensure that this specific demand is fulfilled.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f65b0-118">Se også</span><span class="sxs-lookup"><span data-stu-id="f65b0-118">See Also</span></span>  
<span data-ttu-id="f65b0-119">[Designoplysninger: Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="f65b0-119">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="f65b0-120">[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="f65b0-120">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="f65b0-121">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="f65b0-121">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
