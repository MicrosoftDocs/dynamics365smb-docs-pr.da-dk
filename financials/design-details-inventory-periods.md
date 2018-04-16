---
title: "Designoplysninger – Lagerperioder | Microsoft Docs"
description: "Tilbagedaterede transaktioner eller omkostningsreguleringer påvirker ofte saldi og lagerreguleringer for regnskabsperioder, der kan betragtes som afsluttet. Dette kan have negativ virkning på nøjagtig rapportering, især inden for globale virksomheder. Funktionen af lagerperioder kan bruges til at undgå sådanne problemer ved at åbne eller lukke lagerperioder for at begrænse bogføring i et angivet tidsrum."
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
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: 8ac32d8ec4d438be99e0dbcada61473ca91c1c45
ms.contentlocale: da-dk
ms.lasthandoff: 04/16/2018

---
# <a name="design-details-inventory-periods"></a><span data-ttu-id="4013b-105">Designoplysninger: Lagerperioder</span><span class="sxs-lookup"><span data-stu-id="4013b-105">Design Details: Inventory Periods</span></span>
<span data-ttu-id="4013b-106">Tilbagedaterede transaktioner eller omkostningsreguleringer påvirker ofte saldi og lagerreguleringer for regnskabsperioder, der kan betragtes som afsluttet.</span><span class="sxs-lookup"><span data-stu-id="4013b-106">Backdated transactions or cost adjustments often affect balances and stock valuations for accounting periods that may be considered closed.</span></span> <span data-ttu-id="4013b-107">Dette kan have negativ virkning på nøjagtig rapportering, især inden for globale virksomheder.</span><span class="sxs-lookup"><span data-stu-id="4013b-107">This can have adverse effects on accurate reporting, especially within global corporations.</span></span> <span data-ttu-id="4013b-108">Funktionen af lagerperioder kan bruges til at undgå sådanne problemer ved at åbne eller lukke lagerperioder for at begrænse bogføring i et angivet tidsrum.</span><span class="sxs-lookup"><span data-stu-id="4013b-108">The Inventory Periods feature can be used to avoid such problems by opening or closing inventory periods to limit posting in a set period of time.</span></span>  

 <span data-ttu-id="4013b-109">En lagerperiode er et stykke tid, defineret ved en slutdato, hvor du bogfører lagertransaktioner.</span><span class="sxs-lookup"><span data-stu-id="4013b-109">An inventory period is a period of time, defined by an ending date, in which you post inventory transactions.</span></span> <span data-ttu-id="4013b-110">Når du lukker en lagerperiode, kan der ingen værdiændringer bogføres i den periode, der er lukket.</span><span class="sxs-lookup"><span data-stu-id="4013b-110">When you close an inventory period, no value changes can be posted in the closed period.</span></span> <span data-ttu-id="4013b-111">Dette omfatter nye værdibogføringer, forventede eller fakturerede bogføringer, ændringer til eksisterende værdier og prisreguleringer.</span><span class="sxs-lookup"><span data-stu-id="4013b-111">This includes new value postings, expected or invoiced postings, changes to existing values, and cost adjustments.</span></span> <span data-ttu-id="4013b-112">Du kan dog stadig anvende den på en åben varepost, der falder i den lukkede periode.</span><span class="sxs-lookup"><span data-stu-id="4013b-112">However, you can still apply to an open item ledger entry that falls in the closed period.</span></span> <span data-ttu-id="4013b-113">Du kan finde flere oplysninger i [Designoplysninger: Vareudligning](design-details-item-application.md).</span><span class="sxs-lookup"><span data-stu-id="4013b-113">For more information, see [Design Details: Item Application](design-details-item-application.md).</span></span>  

 <span data-ttu-id="4013b-114">Med henblik på at sikre, at alle transaktionsposter i en lukket periode er endelige, skal følgende betingelser være opfyldt, før en lagerperiode kan lukkes:</span><span class="sxs-lookup"><span data-stu-id="4013b-114">To make sure that all transaction entries in a closed period are final, the following conditions must be met before an inventory period can close:</span></span>  

- <span data-ttu-id="4013b-115">Alle udgående vareposter i perioden skal lukkes (ingen negativ lagerbeholdning).</span><span class="sxs-lookup"><span data-stu-id="4013b-115">All outbound item ledger entries in the period must be closed (no negative inventory).</span></span>  
- <span data-ttu-id="4013b-116">Alle vareomkostninger i perioden skal reguleres.</span><span class="sxs-lookup"><span data-stu-id="4013b-116">All item costs in the period must be adjusted.</span></span>  
- <span data-ttu-id="4013b-117">Alle frigivne og færdige produktionsordrer i perioden skal være kostprisreguleret.</span><span class="sxs-lookup"><span data-stu-id="4013b-117">All released and finished production orders in the period must be cost adjusted.</span></span>  

  <span data-ttu-id="4013b-118">Når du lukker en lagerperiode, oprettes der en lagerperiodepost ved brug af nummeret på den sidste varejournal, der falder i lagerperioden.</span><span class="sxs-lookup"><span data-stu-id="4013b-118">When you close an inventory period, an inventory period entry is created by using the number of the last item register that falls in the inventory period.</span></span> <span data-ttu-id="4013b-119">Den tid, dato og brugerkode for den bruger, der lukker perioden, registreres desuden i lagerperiodeposten.</span><span class="sxs-lookup"><span data-stu-id="4013b-119">In addition, the time, date, and user code of the user closing the period are recorded in the inventory period entry.</span></span> <span data-ttu-id="4013b-120">Ved hjælp af disse oplysninger sammen med den seneste varejournal for den forrige periode, kan du se, hvilke lagertransaktioner der er bogført i lagerperioden.</span><span class="sxs-lookup"><span data-stu-id="4013b-120">By using this information with the last item register for the previous period, you can see which inventory transactions were posted in the inventory period.</span></span> <span data-ttu-id="4013b-121">Det er også muligt at genåbne lagerperioder, hvis du skal bogføre i en lukket periode.</span><span class="sxs-lookup"><span data-stu-id="4013b-121">It is also possible to reopen inventory periods if you need to post in a closed period.</span></span> <span data-ttu-id="4013b-122">Når du genåbner en lagerperiode, oprettes der en lagerperiodepost.</span><span class="sxs-lookup"><span data-stu-id="4013b-122">When you reopen an inventory period, an inventory period entry is created.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4013b-123">Se også</span><span class="sxs-lookup"><span data-stu-id="4013b-123">See Also</span></span>  
 <span data-ttu-id="4013b-124">[Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md) [Administrere lageromkostninger](finance-manage-inventory-costs.md) [Finans](finance.md)</span><span class="sxs-lookup"><span data-stu-id="4013b-124">[Design Details: Inventory Costing](design-details-inventory-costing.md) [Managing Inventory Costs](finance-manage-inventory-costs.md) [Finance](finance.md)</span></span>  
 [<span data-ttu-id="4013b-125">Arbejde med Financials</span><span class="sxs-lookup"><span data-stu-id="4013b-125">Working with Financials</span></span>](ui-work-product.md)

