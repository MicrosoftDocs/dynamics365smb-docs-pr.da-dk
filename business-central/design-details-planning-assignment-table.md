---
title: Designoplysninger – Tabellen Planlægningsopgave | Microsoft Docs
description: Dette emne indeholder indsigt i, hvad der sker, når du ændrer den måde, du planlægger på for en vare.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 3bc3699e7ec5d356ed1bd1b85ad574f2e50d831b
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303216"
---
# <a name="design-details-planning-assignment-table"></a><span data-ttu-id="7b8a1-103">Designoplysninger: Tabellen Planlægningsopgave</span><span class="sxs-lookup"><span data-stu-id="7b8a1-103">Design Details: Planning Assignment Table</span></span>
<span data-ttu-id="7b8a1-104">Der skal foretages planlægning for alle varer, men der er ingen grund til at beregne en plan for en vare, medmindre der er sket en ændring i mønstret for behov eller forsyning, siden sidst en plan blev beregnet.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-104">All items should be planned for, however, there is no reason to calculate a plan for an item unless there has been a change in the demand or supply pattern since the last time a plan was calculated.</span></span>  

<span data-ttu-id="7b8a1-105">Hvis brugeren har angivet en ny salgsordre eller ændret en eksisterende, er der grund til at genberegne planen.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-105">If the user has entered a new sales order or changed an existing one, there is reason to recalculate the plan.</span></span> <span data-ttu-id="7b8a1-106">Andre årsager omfatter en ændring i budgettet eller den ønskede mængde sikkerhedslager.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-106">Other reasons include a change in forecast or the desired safety stock quantity.</span></span> <span data-ttu-id="7b8a1-107">Ændring af en stykliste ved at tilføje eller fjerne en komponent ville sandsynligvis angive en ændring, men kun for komponentvaren.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-107">Changing a bill of material by adding or removing a component would most likely indicate a change, but for the component item only.</span></span>  

<span data-ttu-id="7b8a1-108">For flere lokationer finder tildelingen sted på niveauet for vare pr. lokationskombination.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-108">For multiple locations, the assignment takes place at the level of item per location combination.</span></span> <span data-ttu-id="7b8a1-109">Hvis en salgsordre f.eks. er blevet oprettet på kun én lokation, bliver varen tildelt på den pågældende lokation til planlægning.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-109">If, for example, a sales order has been created at only one location, application will assign the item at that specific location for planning.</span></span>  

<span data-ttu-id="7b8a1-110">Årsagen til at vælge varer til planlægning er et spørgsmål om systemets ydeevne.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-110">The reason for selecting items for planning is a matter of system performance.</span></span> <span data-ttu-id="7b8a1-111">Hvis der ikke er opstået nogen ændring af en vares behov-forsyningsmønster, foreslår planlægningssystemet ikke nogen handlinger, der skal udføres.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-111">If no change in an item’s demand-supply pattern has occurred, the planning system will not suggest any actions to be taken.</span></span> <span data-ttu-id="7b8a1-112">Uden planlægningsopgave ville systemet skulle udføre beregningerne for alle varer for at finde ud af, hvad der skal planlægges, og det ville forbruge systemressourcer.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-112">Without the planning assignment, the system would have to perform the calculations for all items in order to find out what to plan for, and that would drain system resources.</span></span>  

<span data-ttu-id="7b8a1-113">Tabellen **Planlægningsopgave** overvåger behovs- og forsyningshændelser og tildeler de relevante varer til planlægning.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-113">The **Planning Assignment** table monitors demand and supply events and assigns the appropriate items for planning.</span></span> <span data-ttu-id="7b8a1-114">Følgende hændelser overvåges:</span><span class="sxs-lookup"><span data-stu-id="7b8a1-114">The following events are monitored:</span></span>  

* <span data-ttu-id="7b8a1-115">En ny salgsordre, prognose, komponent, købsordre, produktionsordre, montageordre eller overflytningsordre.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-115">A new sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="7b8a1-116">Ændring af vare, antal, lokation, variant eller dato på en salgsordre, forecast, komponent, købsordre, produktionsordre, montageordre eller overflytningsordre.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-116">Change of item, quantity, location, variant, or date on a sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="7b8a1-117">Annullering af en salgsordre, forecast, komponent, købsordre, produktionsordre, montageordre eller overflytningsordre.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-117">Cancellation of a sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="7b8a1-118">Forbrug af varer udover det planlagte.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-118">Consumption of items other than planned.</span></span>  
* <span data-ttu-id="7b8a1-119">Afgang af andre varer end de planlagte.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-119">Output of items other than planned.</span></span>  
* <span data-ttu-id="7b8a1-120">Ikke-planlagte ændringer i lageret.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-120">Unplanned changes in inventory.</span></span>  

<span data-ttu-id="7b8a1-121">For disse direkte forsyning-behov-flytninger, vedligeholder ordresporings- og aktionsmeddelelsessystemet tabellen Planlægningsopgave og angiver en planlægningsårsag som en aktionsmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-121">For these direct supply-demand displacements, the order tracking and action messaging system maintains the Planning Assignment table and states a planning reason as an action message.</span></span>  

<span data-ttu-id="7b8a1-122">Følgende ændringer i stamdata kan også forårsage en uligevægt i planlægning:</span><span class="sxs-lookup"><span data-stu-id="7b8a1-122">The following changes in master data can also cause a planning imbalance:</span></span>  

* <span data-ttu-id="7b8a1-123">Skift status til Certificeret i produktionsstyklistehovedet (for alle varer, der bruger det pågældende hoved).</span><span class="sxs-lookup"><span data-stu-id="7b8a1-123">Change of status to Certified in the production BOM header (for all items using that header).</span></span>  
* <span data-ttu-id="7b8a1-124">Slettet linje (underordnet vare).</span><span class="sxs-lookup"><span data-stu-id="7b8a1-124">Deleted line (child item).</span></span>  
* <span data-ttu-id="7b8a1-125">Skift status til Certificeret i rutehovedet (for alle varer, der bruger den rute).</span><span class="sxs-lookup"><span data-stu-id="7b8a1-125">Change of status to Certified in the routing header (for all items using that routing).</span></span>  
* <span data-ttu-id="7b8a1-126">Ændringer i følgende felter på varekort.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-126">Changes in the following item card fields.</span></span>  
* <span data-ttu-id="7b8a1-127">Sikkerhedslagerantal eller sikkerhedstid</span><span class="sxs-lookup"><span data-stu-id="7b8a1-127">Safety Stock Quantity or Safety Lead Time.</span></span>  
* <span data-ttu-id="7b8a1-128">Leveringstid.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-128">Lead Time Calculation.</span></span>  
* <span data-ttu-id="7b8a1-129">Genbestillingspunkt.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-129">Reorder Point.</span></span>  
* <span data-ttu-id="7b8a1-130">Produktionsstyklistenr. (og alle underordnede af gammel styklistereference).</span><span class="sxs-lookup"><span data-stu-id="7b8a1-130">Production BOM No. (and all children of old BOM reference).</span></span>  
* <span data-ttu-id="7b8a1-131">Rutenr.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-131">Routing No.</span></span>  
* <span data-ttu-id="7b8a1-132">Genbestillingsmetode.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-132">Reordering Policy.</span></span>  

<span data-ttu-id="7b8a1-133">I disse tilfælde vil en ny funktion, administration af planlægning, vedligeholde tabellen og angive årsagen til planlægning som Bevægelse.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-133">In these cases, a new function, Planning Assignment Management, maintains the table and states the planning reason as Net Change.</span></span>  

<span data-ttu-id="7b8a1-134">Følgende ændringer medfører ikke en planlægningsopgave:</span><span class="sxs-lookup"><span data-stu-id="7b8a1-134">The following changes do not cause a planning assignment:</span></span>  

* <span data-ttu-id="7b8a1-135">Kalendere</span><span class="sxs-lookup"><span data-stu-id="7b8a1-135">Calendars</span></span>  
* <span data-ttu-id="7b8a1-136">Andre planlægningsparametre på varekortet</span><span class="sxs-lookup"><span data-stu-id="7b8a1-136">Other planning parameters on the item card</span></span>  

<span data-ttu-id="7b8a1-137">Ved beregning af en hovedplan eller en MRP gælder følgende begrænsninger:</span><span class="sxs-lookup"><span data-stu-id="7b8a1-137">When calculating an MPS or an MRP, the following restrictions apply:</span></span>  

* <span data-ttu-id="7b8a1-138">Hovedplan: Planlægningssystemet kontrollerer, at varen har en behovsprognose eller en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-138">MPS: The planning system checks that the item carries a demand forecast or a sales order.</span></span> <span data-ttu-id="7b8a1-139">Hvis ikke, medtages varen ikke i planen.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-139">If not, the item is not included in the plan.</span></span>  
* <span data-ttu-id="7b8a1-140">MRP: Hvis planlægningssystemet registrerer, at varen genbestilles af en hovedplans planlægningslinje eller forsyningsordre, udelades varen i planlægningen.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-140">MRP: If the planning system detects that the item is being replenished by an MPS planning line or MPS supply order, the item will be left out of the planning.</span></span> <span data-ttu-id="7b8a1-141">Et hvilket som helst behov fra relevante komponenter er imidlertid inkluderet.</span><span class="sxs-lookup"><span data-stu-id="7b8a1-141">However, any demand from relevant components is included.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7b8a1-142">Se også</span><span class="sxs-lookup"><span data-stu-id="7b8a1-142">See Also</span></span>  
<span data-ttu-id="7b8a1-143">[Designoplysninger: Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="7b8a1-143">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="7b8a1-144">[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="7b8a1-144">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
<span data-ttu-id="7b8a1-145">[Designoplysninger: Overførsler i planlægning](design-details-transfers-in-planning.md) </span><span class="sxs-lookup"><span data-stu-id="7b8a1-145">[Design Details: Transfers in Planning](design-details-transfers-in-planning.md) </span></span>  
[<span data-ttu-id="7b8a1-146">Designoplysninger: Planlægningsparametre</span><span class="sxs-lookup"><span data-stu-id="7b8a1-146">Design Details: Planning Parameters</span></span>](design-details-planning-parameters.md)  
