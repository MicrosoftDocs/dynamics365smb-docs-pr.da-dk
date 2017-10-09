---
title: "Designoplysninger – Intervallets rolle | Microsoft Docs"
description: "Formålet med intervallet er at indsamle behovshændelser inden for tidsvinduet for at oprette en fælles forsyningsordre."
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
ms.openlocfilehash: eb1b1a401dabe09a77c44558e9f5a83388078aaa
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-the-role-of-the-time-bucket"></a><span data-ttu-id="7a40a-103">Designoplysninger: Intervallets rolle</span><span class="sxs-lookup"><span data-stu-id="7a40a-103">Design Details: The Role of the Time Bucket</span></span>
<span data-ttu-id="7a40a-104">Formålet med intervallet er at indsamle behovshændelser inden for tidsvinduet for at oprette en fælles forsyningsordre.</span><span class="sxs-lookup"><span data-stu-id="7a40a-104">The purpose of the time bucket is to collect demand events within the time window in order to make a joint supply order.</span></span>  
  
 <span data-ttu-id="7a40a-105">For genbestillingspolitikker, der bruger et genbestillingspunkt, kan du angive et interval.</span><span class="sxs-lookup"><span data-stu-id="7a40a-105">For reordering policies that use a reorder point, you can define a time bucket.</span></span> <span data-ttu-id="7a40a-106">Dette sikrer, at behov inden for den samme tidsperiode er akkumuleret, før du tjekker indvirkningen på den forventede lagerbeholdning, og om genbestillingspunktet er blevet overskredet.</span><span class="sxs-lookup"><span data-stu-id="7a40a-106">This ensures that demand within the same time period is accumulated before checking the impact on the projected inventory and whether the reorder point has been passed.</span></span> <span data-ttu-id="7a40a-107">Hvis genbestillingspunktet er overskredet, er en ny forsyningsordre planlagt fremad fra udgangen af den periode, der er defineret i intervallet.</span><span class="sxs-lookup"><span data-stu-id="7a40a-107">If the reorder point is passed, a new supply order is scheduled forward from the end of the period defined by the time bucket.</span></span> <span data-ttu-id="7a40a-108">Intervaller starter på den planlagte startdato.</span><span class="sxs-lookup"><span data-stu-id="7a40a-108">The time buckets begin on the planning starting date.</span></span>  
  
 <span data-ttu-id="7a40a-109">Begrebet interval afspejler den manuelle proces til hyppig kontrol af lagerniveauet i stedet for hver transaktion.</span><span class="sxs-lookup"><span data-stu-id="7a40a-109">The time-bucketed concept reflects the manual process of checking the inventory level on a frequent basis rather than for each transaction.</span></span> <span data-ttu-id="7a40a-110">Brugeren skal definere frekvensen (intervallet).</span><span class="sxs-lookup"><span data-stu-id="7a40a-110">The user needs to define the frequency (the time bucket).</span></span> <span data-ttu-id="7a40a-111">Brugeren samler f.eks. alle varebehov fra en kreditor for at foretage en ugentlig bestilling.</span><span class="sxs-lookup"><span data-stu-id="7a40a-111">For example, the user gathers all item needs from one vendor to place a weekly order.</span></span>  
  
 ![](media/nav_app_supply_planning_2_reorder_cycle.png "NAV_APP_supply_planning_2_reorder_cycle")  
  
 <span data-ttu-id="7a40a-112">Intervallet bruges normalt til at undgå en overlapningseffekt.</span><span class="sxs-lookup"><span data-stu-id="7a40a-112">The time bucket is generally used to avoid a cascade effect.</span></span> <span data-ttu-id="7a40a-113">For eksempel en afstemt række af behov og forsyning, hvor et tidligt behov annulleres, eller et ny oprettes.</span><span class="sxs-lookup"><span data-stu-id="7a40a-113">For example, a balanced row of demand and supply where an early demand is canceled, or a new one is created.</span></span> <span data-ttu-id="7a40a-114">Resultatet ville være, at hver forsyningsordre (undtagen den sidste) skal omplanlægges.</span><span class="sxs-lookup"><span data-stu-id="7a40a-114">The result would be that every supply order (except the last one) is rescheduled.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7a40a-115">Se også</span><span class="sxs-lookup"><span data-stu-id="7a40a-115">See Also</span></span>  
 <span data-ttu-id="7a40a-116">[Designoplysninger: Genbestillingsmetoder](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="7a40a-116">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="7a40a-117">[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="7a40a-117">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="7a40a-118">[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="7a40a-118">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="7a40a-119">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="7a40a-119">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
