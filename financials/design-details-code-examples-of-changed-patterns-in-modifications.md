---
title: "Designoplysninger – Lukning af behov og forsyning | Microsoft Docs"
description: "Når de forsyningsudlignende procedurer er blevet udført, er der tre mulige slutsituationer."
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
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: f682e2fdaa5be20ae8e6f3ff6ee2ff4769b48545
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="design-details-closing-demand-and-supply"></a><span data-ttu-id="94c8b-103">Designoplysninger: Lukning af behov og forsyning</span><span class="sxs-lookup"><span data-stu-id="94c8b-103">Design Details: Closing Demand and Supply</span></span>
<span data-ttu-id="94c8b-104">Når de forsyningsudlignende procedurer er blevet udført, er der tre mulige slutsituationer:</span><span class="sxs-lookup"><span data-stu-id="94c8b-104">When the supply balancing procedures have been performed, there are three possible end situations:</span></span>  

-   <span data-ttu-id="94c8b-105">Det påkrævede antal og den påkrævede dato for behovhændelserne er opfyldt, og planlægning af dem kan lukkes.</span><span class="sxs-lookup"><span data-stu-id="94c8b-105">The required quantity and date of the demand events have been met and the planning for them can be closed.</span></span> <span data-ttu-id="94c8b-106">Forsyningshændelsen er stadig åben og kan dække det næste behov, så udligningsproceduren kan starte forfra med den aktuelle forsyningshændelse og det næste behov.</span><span class="sxs-lookup"><span data-stu-id="94c8b-106">The supply event is still open and may be able to cover the next demand, so the balancing procedure can start over with the current supply event and the next demand.</span></span>  

-   <span data-ttu-id="94c8b-107">Forsyningsordren kan ikke ændres, så den dækker alle behov.</span><span class="sxs-lookup"><span data-stu-id="94c8b-107">The supply order cannot be modified to cover all of the demand.</span></span> <span data-ttu-id="94c8b-108">Behovshændelsen er stadig åben, med nogle udækkede antal, der kan dækkes ved næste forsyningshændelse.</span><span class="sxs-lookup"><span data-stu-id="94c8b-108">The demand event is still open, with some uncovered quantity that may be covered by the next supply event.</span></span> <span data-ttu-id="94c8b-109">Derfor lukkes den aktuelle forsyning, så den udlignende handling kan starte forfra med det aktuelle behov og den næste forsyningshændelse.</span><span class="sxs-lookup"><span data-stu-id="94c8b-109">Thus the current supply event is closed, so the balancing act can start over with the current demand and the next supply event.</span></span>  

-   <span data-ttu-id="94c8b-110">Alle behov er blevet dækket: Der er ingen efterfølgende behov (eller der har ikke været nogen behov overhovedet).</span><span class="sxs-lookup"><span data-stu-id="94c8b-110">All of the demand has been covered; there is no subsequent demand (or there has been no demand at all).</span></span> <span data-ttu-id="94c8b-111">Hvis der er en eventuel overskydende forsyning, kan den reduceres (eller annulleres) og derefter lukkes.</span><span class="sxs-lookup"><span data-stu-id="94c8b-111">If there is any surplus supply, it may be decreased (or canceled) and then closed.</span></span> <span data-ttu-id="94c8b-112">Det er muligt, at der findes yderligere forsyningshændelser i kæden, og de bør også annulleres.</span><span class="sxs-lookup"><span data-stu-id="94c8b-112">It is possible that additional supply events exist further along in the chain, and they should also be canceled.</span></span>  

 <span data-ttu-id="94c8b-113">Endelig opretter planlægningssystemet et ordresporingslink mellem forsyning og behov.</span><span class="sxs-lookup"><span data-stu-id="94c8b-113">Last, the planning system will create an order tracking link between the supply and the demand.</span></span>  

## <a name="creating-the-planning-line-suggested-action"></a><span data-ttu-id="94c8b-114">Oprettelse af planlægningslinjen (foreslået aktivitet)</span><span class="sxs-lookup"><span data-stu-id="94c8b-114">Creating the Planning Line (Suggested Action)</span></span>  
 <span data-ttu-id="94c8b-115">Hvis en handling – Ny, Ret antal, Omplanlæg, Omplanlæg og ret antal eller Annuller – foreslås for at revidere forsyningsordren, vil planlægningssystemet oprette en planlægningslinje i planlægningskladden.</span><span class="sxs-lookup"><span data-stu-id="94c8b-115">If any action – New, Change Quantity, Reschedule, Reschedule and Change Quantity, or Cancel – is suggested to revise the supply order, the planning system creates a planning line in the planning worksheet.</span></span> <span data-ttu-id="94c8b-116">På grund af ordresporing oprettes planlægningslinjen ikke kun, når forsyningshændelsen er lukket, men også hvis behovhændelsen er lukket, selvom forsyningshændelsen stadig er åben og kan være underlagt yderligere ændringer, når næste behovshændelse behandles.</span><span class="sxs-lookup"><span data-stu-id="94c8b-116">Due to order tracking, the planning line is created not only when the supply event is closed, but also if the demand event is closed, even though the supply event is still open and may be subject to additional changes when the next demand event is processed.</span></span> <span data-ttu-id="94c8b-117">Det betyder, at når planlægningslinjen er oprettet, kan den ændres igen.</span><span class="sxs-lookup"><span data-stu-id="94c8b-117">This means that when first created, the planning line may be changed again.</span></span>  

 <span data-ttu-id="94c8b-118">Planlægningslinjen kan vedligeholdes i tre niveauer for at minimere databaseadgang, når der håndteres produktionsordrer, mens det tilstræbes at udføre det mindst krævende vedligeholdelsesniveau:</span><span class="sxs-lookup"><span data-stu-id="94c8b-118">To minimize database access when handling production orders, the planning line can be maintained in three levels, while aiming to perform the least demanding maintenance level:</span></span>  

-   <span data-ttu-id="94c8b-119">Opret kun planlægningslinjen med den aktuelle forfaldsdato og antallet, men uden rute og komponenter.</span><span class="sxs-lookup"><span data-stu-id="94c8b-119">Create only the planning line with the current due date and quantity but without the routing and components.</span></span>  

-   <span data-ttu-id="94c8b-120">Omfatter rute: Den planlagte rute er opstillet med beregning af start- og slutdatoer og -tidspunkter.</span><span class="sxs-lookup"><span data-stu-id="94c8b-120">Include routing: the planned routing is laid out including calculation of starting and ending dates and times.</span></span> <span data-ttu-id="94c8b-121">Dette er påkrævet i forbindelse med adgang til databasen.</span><span class="sxs-lookup"><span data-stu-id="94c8b-121">This is demanding in terms of database accesses.</span></span> <span data-ttu-id="94c8b-122">For at bestemme slutdato og forfaldsdatoer kan det være nødvendigt at beregne dette, selvom forsyningshændelsen ikke er blevet lukket (i tilfælde af fremadrettet planlægning).</span><span class="sxs-lookup"><span data-stu-id="94c8b-122">To determine the ending and due dates, it may be necessary to calculate this even if the supply event has not been closed (in the case of forward scheduling).</span></span>  

-   <span data-ttu-id="94c8b-123">Omfatter styklisteudfoldelsen: Dette kan vente indtil lige før leveringshændelsen er lukket.</span><span class="sxs-lookup"><span data-stu-id="94c8b-123">Include BOM explosion: this can wait until just before the supply event is closed.</span></span>  

 <span data-ttu-id="94c8b-124">Dette afslutter beskrivelserne af, hvordan behov og forsyning indlæses, prioriteres og afstemmes af planlægningssystemet.</span><span class="sxs-lookup"><span data-stu-id="94c8b-124">This concludes the descriptions of how demand and supply is loaded, prioritized, and balanced by the planning system.</span></span> <span data-ttu-id="94c8b-125">I integration med denne planlægningsaktivitet af forsyning skal systemet sikre, at det nødvendige lagerniveau for hver planlagt vare opretholdes i overensstemmelse med dens genbestillingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="94c8b-125">In integration with this supply planning activity, the system must ensure that the required inventory level of each planned item is maintained according to its reordering policies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="94c8b-126">Se også</span><span class="sxs-lookup"><span data-stu-id="94c8b-126">See Also</span></span>  
 <span data-ttu-id="94c8b-127">[Designoplysninger: Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="94c8b-127">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
 <span data-ttu-id="94c8b-128">[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="94c8b-128">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 [<span data-ttu-id="94c8b-129">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="94c8b-129">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
