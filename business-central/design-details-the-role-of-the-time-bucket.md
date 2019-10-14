---
title: Designoplysninger – Intervallets rolle | Microsoft Docs
description: Formålet med intervallet er at indsamle behovshændelser inden for tidssiden for at oprette en fælles forsyningsordre.
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
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 4a8e231dbee8f26c2ac6f0420af252996302ac86
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2302908"
---
# <a name="design-details-the-role-of-the-time-bucket"></a><span data-ttu-id="a4743-103">Designoplysninger: Intervallets rolle</span><span class="sxs-lookup"><span data-stu-id="a4743-103">Design Details: The Role of the Time Bucket</span></span>
<span data-ttu-id="a4743-104">Formålet med intervallet er at indsamle behovshændelser inden for tidssiden for at oprette en fælles forsyningsordre.</span><span class="sxs-lookup"><span data-stu-id="a4743-104">The purpose of the time bucket is to collect demand events within the time page in order to make a joint supply order.</span></span>  

 <span data-ttu-id="a4743-105">For genbestillingspolitikker, der bruger et genbestillingspunkt, kan du angive et interval.</span><span class="sxs-lookup"><span data-stu-id="a4743-105">For reordering policies that use a reorder point, you can define a time bucket.</span></span> <span data-ttu-id="a4743-106">Dette sikrer, at behov inden for den samme tidsperiode er akkumuleret, før du tjekker indvirkningen på den forventede lagerbeholdning, og om genbestillingspunktet er blevet overskredet.</span><span class="sxs-lookup"><span data-stu-id="a4743-106">This ensures that demand within the same time period is accumulated before checking the impact on the projected inventory and whether the reorder point has been passed.</span></span> <span data-ttu-id="a4743-107">Hvis genbestillingspunktet er overskredet, er en ny forsyningsordre planlagt fremad fra udgangen af den periode, der er defineret i intervallet.</span><span class="sxs-lookup"><span data-stu-id="a4743-107">If the reorder point is passed, a new supply order is scheduled forward from the end of the period defined by the time bucket.</span></span> <span data-ttu-id="a4743-108">Intervaller starter på den planlagte startdato.</span><span class="sxs-lookup"><span data-stu-id="a4743-108">The time buckets begin on the planning starting date.</span></span>  

 <span data-ttu-id="a4743-109">Begrebet interval afspejler den manuelle proces til hyppig kontrol af lagerniveauet i stedet for hver transaktion.</span><span class="sxs-lookup"><span data-stu-id="a4743-109">The time-bucketed concept reflects the manual process of checking the inventory level on a frequent basis rather than for each transaction.</span></span> <span data-ttu-id="a4743-110">Brugeren skal definere frekvensen (intervallet).</span><span class="sxs-lookup"><span data-stu-id="a4743-110">The user needs to define the frequency (the time bucket).</span></span> <span data-ttu-id="a4743-111">Brugeren samler f.eks. alle varebehov fra en kreditor for at foretage en ugentlig bestilling.</span><span class="sxs-lookup"><span data-stu-id="a4743-111">For example, the user gathers all item needs from one vendor to place a weekly order.</span></span>  

 <span data-ttu-id="a4743-112">![Eksempel på interval ved planlægning](media/nav_app_supply_planning_2_reorder_cycle.png "Eksempel på interval ved planlægning")</span><span class="sxs-lookup"><span data-stu-id="a4743-112">![Example of time bucket in planning](media/nav_app_supply_planning_2_reorder_cycle.png "Example of time bucket in planning")</span></span>  

 <span data-ttu-id="a4743-113">Intervallet bruges normalt til at undgå en overlapningseffekt.</span><span class="sxs-lookup"><span data-stu-id="a4743-113">The time bucket is generally used to avoid a cascade effect.</span></span> <span data-ttu-id="a4743-114">For eksempel en afstemt række af behov og forsyning, hvor et tidligt behov annulleres, eller et ny oprettes.</span><span class="sxs-lookup"><span data-stu-id="a4743-114">For example, a balanced row of demand and supply where an early demand is canceled, or a new one is created.</span></span> <span data-ttu-id="a4743-115">Resultatet ville være, at hver forsyningsordre (undtagen den sidste) skal omplanlægges.</span><span class="sxs-lookup"><span data-stu-id="a4743-115">The result would be that every supply order (except the last one) is rescheduled.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a4743-116">Se også</span><span class="sxs-lookup"><span data-stu-id="a4743-116">See Also</span></span>  
 <span data-ttu-id="a4743-117">[Designoplysninger: Genbestillingsmetoder](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="a4743-117">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="a4743-118">[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="a4743-118">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="a4743-119">[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="a4743-119">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="a4743-120">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="a4743-120">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
