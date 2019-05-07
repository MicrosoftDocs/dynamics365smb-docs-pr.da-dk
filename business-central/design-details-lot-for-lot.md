---
title: Designoplysninger – Lot-for-Lot | Microsoft Docs
description: Få at vide, hvordan du bruger lot-for-lot-politikken til at udligne ordreantal på baggrund af behov.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 3b80738be6dfe9d171a3cad56edf56cfa4960180
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/16/2019
ms.locfileid: "938130"
---
# <a name="design-details-lot-for-lot"></a><span data-ttu-id="d5d74-103">Designoplysninger: Lot-for-lot</span><span class="sxs-lookup"><span data-stu-id="d5d74-103">Design Details: Lot-for-Lot</span></span>
<span data-ttu-id="d5d74-104">Lot-for-lot-politik er den mest fleksible, fordi systemet kun reagerer på det faktiske behov, plus det fungerer på forventet behov fra forecast og rammeordrer og udligner derefter ordreantallet på baggrund af behovet.</span><span class="sxs-lookup"><span data-stu-id="d5d74-104">The lot-for-lot policy is the most flexible because the system only reacts on actual demand, plus it acts on anticipated demand from forecast and blanket orders and then settles the order quantity based on the demand.</span></span> <span data-ttu-id="d5d74-105">Lot-for-lot-politik tager sigte på A - og B-varer, hvor lageret kan accepteres, men bør undgås.</span><span class="sxs-lookup"><span data-stu-id="d5d74-105">The lot-for-lot policy is aimed at A- and B-items where inventory can be accepted but should be avoided.</span></span>  

<span data-ttu-id="d5d74-106">På nogle måder ser lot-for-lot politik ud som ordrepolitikken, men der er en generisk tilgang til varer: Den kan acceptere antal på lager, og den kombinerer behov og tilsvarende forsyning i intervaller, der er defineret af brugeren.</span><span class="sxs-lookup"><span data-stu-id="d5d74-106">In some ways, the lot-for-lot policy looks like the Order policy, but it has a generic approach to items; it can accept quantities in inventory, and it bundles demand and corresponding supply in time buckets defined by the user.</span></span>  

<span data-ttu-id="d5d74-107">Intervallet er defineret i feltet **Interval**.</span><span class="sxs-lookup"><span data-stu-id="d5d74-107">The time bucket is defined in the **Time Bucket** field.</span></span> <span data-ttu-id="d5d74-108">Systemet fungerer med et mindste interval på én dag, da det er den mindste tidsenhed på behovs- og forsyningshændelser i systemet (selvom tidsenheden på produktionsordrer og komponentbehov i praksis kan være sekunder).</span><span class="sxs-lookup"><span data-stu-id="d5d74-108">The system works with a minimum time bucket of one day, since this is the smallest time unit of measure on demand and supply events in the system (although, in practice, the time unit of measure on production orders and component needs can be seconds).</span></span>  

<span data-ttu-id="d5d74-109">Intervallet angiver også grænser for, hvornår en eksisterende forsyningsordre bør omplanlægges for at opfylde et bestemt behov.</span><span class="sxs-lookup"><span data-stu-id="d5d74-109">The time bucket also sets limits on when an existing supply order should be rescheduled to meet a given demand.</span></span> <span data-ttu-id="d5d74-110">Hvis forsyningen ligger i intervallet, bliver den flyttet ind eller ud for at opfylde behovet.</span><span class="sxs-lookup"><span data-stu-id="d5d74-110">If the supply lies within the time bucket, it will be rescheduled in or out to meet the demand.</span></span> <span data-ttu-id="d5d74-111">Hvis den ligger tidligere, vil det medføre unødvendig ophobning af lageret og skal annulleres.</span><span class="sxs-lookup"><span data-stu-id="d5d74-111">Otherwise, if it lies earlier, it will cause unnecessary build-up of inventory and should be canceled.</span></span> <span data-ttu-id="d5d74-112">Hvis den ligger senere, oprettes en ny forsyningsordre i stedet.</span><span class="sxs-lookup"><span data-stu-id="d5d74-112">If it lies later, a new supply order will be created instead.</span></span>  

<span data-ttu-id="d5d74-113">Med denne politik er det også muligt at definere et sikkerhedslager for at kompensere for mulige udsving i udbud eller for at imødekomme pludselige behov.</span><span class="sxs-lookup"><span data-stu-id="d5d74-113">With this policy, it is also possible to define a safety stock in order to compensate for possible fluctuations in supply, or to meet sudden demand.</span></span>  

<span data-ttu-id="d5d74-114">Da forsyningsordreantallet er baseret på det faktiske behov, kan det være smart at bruge ordremodifikatorer: Rund ordreantallet op, så det passer med en specifik oprundingsfaktor (eller købsenhedskoden), forøg ordren til et fastsat minimumsordreantal, eller reducer antallet til det angivne maksimale antal (og opret derefter to eller flere forsyninger for at nå det nødvendige samlede antal).</span><span class="sxs-lookup"><span data-stu-id="d5d74-114">Because the supply order quantity is based on the actual demand it can make sense to use the order modifiers: round the order quantity up to meet a specified order multiple (or purchase unit of measure), increase the order to a specified minimum order quantity, or decrease the quantity to the specified maximum quantity (and thus create two or more supplies to reach the total needed quantity).</span></span>  

## <a name="see-also"></a><span data-ttu-id="d5d74-115">Se også</span><span class="sxs-lookup"><span data-stu-id="d5d74-115">See Also</span></span>  
<span data-ttu-id="d5d74-116">[Designoplysninger: Genbestillingsmetoder](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="d5d74-116">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="d5d74-117">[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="d5d74-117">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="d5d74-118">[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="d5d74-118">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="d5d74-119">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="d5d74-119">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
