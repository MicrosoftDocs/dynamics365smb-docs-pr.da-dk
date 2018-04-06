---
title: "Designoplysninger – Intervallets rolle | Microsoft Docs"
description: "Formålet med intervallet er at indsamle behovshændelser inden for tidsvinduet for at oprette en fælles forsyningsordre."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 099465f0ef7bdafa3df80c377cd83b177bb68072
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-the-role-of-the-time-bucket"></a><span data-ttu-id="06bf7-103">Designoplysninger: Intervallets rolle</span><span class="sxs-lookup"><span data-stu-id="06bf7-103">Design Details: The Role of the Time Bucket</span></span>
<span data-ttu-id="06bf7-104">Formålet med intervallet er at indsamle behovshændelser inden for tidsvinduet for at oprette en fælles forsyningsordre.</span><span class="sxs-lookup"><span data-stu-id="06bf7-104">The purpose of the time bucket is to collect demand events within the time window in order to make a joint supply order.</span></span>  
  
 <span data-ttu-id="06bf7-105">For genbestillingspolitikker, der bruger et genbestillingspunkt, kan du angive et interval.</span><span class="sxs-lookup"><span data-stu-id="06bf7-105">For reordering policies that use a reorder point, you can define a time bucket.</span></span> <span data-ttu-id="06bf7-106">Dette sikrer, at behov inden for den samme tidsperiode er akkumuleret, før du tjekker indvirkningen på den forventede lagerbeholdning, og om genbestillingspunktet er blevet overskredet.</span><span class="sxs-lookup"><span data-stu-id="06bf7-106">This ensures that demand within the same time period is accumulated before checking the impact on the projected inventory and whether the reorder point has been passed.</span></span> <span data-ttu-id="06bf7-107">Hvis genbestillingspunktet er overskredet, er en ny forsyningsordre planlagt fremad fra udgangen af den periode, der er defineret i intervallet.</span><span class="sxs-lookup"><span data-stu-id="06bf7-107">If the reorder point is passed, a new supply order is scheduled forward from the end of the period defined by the time bucket.</span></span> <span data-ttu-id="06bf7-108">Intervaller starter på den planlagte startdato.</span><span class="sxs-lookup"><span data-stu-id="06bf7-108">The time buckets begin on the planning starting date.</span></span>  
  
 <span data-ttu-id="06bf7-109">Begrebet interval afspejler den manuelle proces til hyppig kontrol af lagerniveauet i stedet for hver transaktion.</span><span class="sxs-lookup"><span data-stu-id="06bf7-109">The time-bucketed concept reflects the manual process of checking the inventory level on a frequent basis rather than for each transaction.</span></span> <span data-ttu-id="06bf7-110">Brugeren skal definere frekvensen (intervallet).</span><span class="sxs-lookup"><span data-stu-id="06bf7-110">The user needs to define the frequency (the time bucket).</span></span> <span data-ttu-id="06bf7-111">Brugeren samler f.eks. alle varebehov fra en kreditor for at foretage en ugentlig bestilling.</span><span class="sxs-lookup"><span data-stu-id="06bf7-111">For example, the user gathers all item needs from one vendor to place a weekly order.</span></span>  
  
 <span data-ttu-id="06bf7-112">![](media/nav_app_supply_planning_2_reorder_cycle.png "NAV_APP_supply_planning_2_reorder_cycle")</span><span class="sxs-lookup"><span data-stu-id="06bf7-112">![](media/nav_app_supply_planning_2_reorder_cycle.png "NAV_APP_supply_planning_2_reorder_cycle")</span></span>  
  
 <span data-ttu-id="06bf7-113">Intervallet bruges normalt til at undgå en overlapningseffekt.</span><span class="sxs-lookup"><span data-stu-id="06bf7-113">The time bucket is generally used to avoid a cascade effect.</span></span> <span data-ttu-id="06bf7-114">For eksempel en afstemt række af behov og forsyning, hvor et tidligt behov annulleres, eller et ny oprettes.</span><span class="sxs-lookup"><span data-stu-id="06bf7-114">For example, a balanced row of demand and supply where an early demand is canceled, or a new one is created.</span></span> <span data-ttu-id="06bf7-115">Resultatet ville være, at hver forsyningsordre (undtagen den sidste) skal omplanlægges.</span><span class="sxs-lookup"><span data-stu-id="06bf7-115">The result would be that every supply order (except the last one) is rescheduled.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="06bf7-116">Se også</span><span class="sxs-lookup"><span data-stu-id="06bf7-116">See Also</span></span>  
 <span data-ttu-id="06bf7-117">[Designoplysninger: Genbestillingsmetoder](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="06bf7-117">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="06bf7-118">[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="06bf7-118">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="06bf7-119">[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="06bf7-119">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="06bf7-120">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="06bf7-120">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
