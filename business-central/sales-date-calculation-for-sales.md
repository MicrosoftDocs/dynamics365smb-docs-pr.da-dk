---
title: Datoberegning for salg | Microsoft Docs
description: Programmet beregner automatisk den dato, hvor du skal bestille en vare for at have den på lager på en bestemt dato. Dette er den dato, du kan forvente, at varer, der er bestilt på en bestemt dato, er disponible til pluk.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6080fd58b299a0bda74c1cdd9ff5758d8805b3a8
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881373"
---
# <a name="date-calculation-for-sales"></a><span data-ttu-id="66a8a-104">Beregning af forfaldsdato for salg</span><span class="sxs-lookup"><span data-stu-id="66a8a-104">Date Calculation for Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="66a8a-105">beregner automatisk den tidligst mulige dato, som en vare eller en salgsordrelinje kan sendes på.</span><span class="sxs-lookup"><span data-stu-id="66a8a-105">automatically calculates the earliest possible date that an item on a sales order line can be shipped.</span></span>

<span data-ttu-id="66a8a-106">Hvis debitoren har anmodet om en bestemt leveringsdato, beregnes den dato, hvor varen skal være disponibel til pluk automatisk for at leveringen kan gennemføres rettidigt.</span><span class="sxs-lookup"><span data-stu-id="66a8a-106">If the customer has requested a specific delivery date, then the date on which the items must be available to pick to meet that delivery date is calculated.</span></span>

<span data-ttu-id="66a8a-107">Hvis debitoren ikke anmoder om en bestemt leveringsdato, beregnes den dato, hvor varen kan leveres. Udgangspunktet er den dato, hvor varen er disponibel for pluk.</span><span class="sxs-lookup"><span data-stu-id="66a8a-107">If the customer does not request a specific delivery date, then the date on which the items can be delivered is calculated, starting from the date on which the items are available for picking.</span></span>

## <a name="calculating-a-requested-delivery-date"></a><span data-ttu-id="66a8a-108">Beregning med en ønsket leveringsdato</span><span class="sxs-lookup"><span data-stu-id="66a8a-108">Calculating a Requested Delivery Date</span></span>
<span data-ttu-id="66a8a-109">Hvis du angiver en ønsket leveringsdato på salgsordrelinjen, bliver denne dato til udgangspunktet for de efterfølgende beregninger.</span><span class="sxs-lookup"><span data-stu-id="66a8a-109">If you specify a requested delivery date on the sales order line, that date becomes the starting point for the following calculations.</span></span>

- <span data-ttu-id="66a8a-110">ønsket leveringsdato– transporttid = planlagt afsendelsesdato</span><span class="sxs-lookup"><span data-stu-id="66a8a-110">requested delivery date - shipping time = planned shipment date</span></span>
- <span data-ttu-id="66a8a-111">planlagt afsendelsesdato – udgående lagerekspeditionstid = planlagt afsendelsesdato</span><span class="sxs-lookup"><span data-stu-id="66a8a-111">planned shipment date - outbound whse. handling time = shipment date</span></span>

<span data-ttu-id="66a8a-112">Hvis varen er disponibel til pluk på afsendelsesdatoen, kan salgsprocessen fortsættes.</span><span class="sxs-lookup"><span data-stu-id="66a8a-112">If the items are available to pick on the shipment date, then the sales process can continue.</span></span> <span data-ttu-id="66a8a-113">Ellers vises der en advarsel om, at varen ikke er på lager.</span><span class="sxs-lookup"><span data-stu-id="66a8a-113">Otherwise, a stock-out warning is displayed.</span></span>

> [!Note]
> <span data-ttu-id="66a8a-114">Hvis processen er baseret på bagudrettet beregning, f.eks. hvis du bruger den ønskede leveringsdato til at hente den planlagte afsendelsesdato, anbefales det, at du bruger datoformler med faste varigheder, f.eks. "5D" for fem dage eller "1U" for én uge.</span><span class="sxs-lookup"><span data-stu-id="66a8a-114">If your process is based on backward calculation, for example, if you use the requested delivery date to get the planned shipment date, we recommend that you use date formulas that have fixed durations, such as "5D" for five days or "1W" for one week.</span></span> <span data-ttu-id="66a8a-115">Datoformler uden faste varigheder, f.eks. "AU" for aktuelle uge eller AM for den aktuelle måned, kan resultere i forkerte datoberegninger.</span><span class="sxs-lookup"><span data-stu-id="66a8a-115">Date formulas without fixed durations, such as "CW" for current week or CM for current month, can result in incorrect date calculations.</span></span> <span data-ttu-id="66a8a-116">Du kan finde flere oplysninger om datoformler i [Arbejde med kalenderdatoer og-klokkeslæt](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="66a8a-116">For more information about date formulas, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

## <a name="calculating-the-earliest-possible-delivery-date"></a><span data-ttu-id="66a8a-117">Beregning af den tidligst mulige leveringsdato</span><span class="sxs-lookup"><span data-stu-id="66a8a-117">Calculating the Earliest Possible Delivery Date</span></span>
<span data-ttu-id="66a8a-118">Hvis du ikke angiver en ønsket leveringsdato på en salgsordrelinje, eller hvis ikke den ønskede leveringsdato kan imødekommes, vil den tidligste dato for varernes tilgængelighed blive beregnet.</span><span class="sxs-lookup"><span data-stu-id="66a8a-118">If you do not specify a requested delivery date on the sales order line, or if the requested delivery date cannot be met, then the earliest date on which that the items are available is calculated.</span></span> <span data-ttu-id="66a8a-119">Datoen kan derefter indtastes i feltet Afsendelsesdato på linjen, og den dato, som du planlægger at levere varer samt den dato, hvor de leveres til debitor beregnes ved hjælp af følgende formler.</span><span class="sxs-lookup"><span data-stu-id="66a8a-119">That date is then entered in the Shipment Date field on the line, and the date on which you plan to ship the items as well as the date on which they will be delivered to the customer are calculated using the following formulas.</span></span>

- <span data-ttu-id="66a8a-120">afsendelsesdato + udgående lagerekspeditionstid = planlagt afsendelses dato</span><span class="sxs-lookup"><span data-stu-id="66a8a-120">shipment date + outbound whse. handling time = planned shipment date</span></span>
- <span data-ttu-id="66a8a-121">planlagt afsendelsesdato + transporttid = planlagt leveringsdato</span><span class="sxs-lookup"><span data-stu-id="66a8a-121">planned shipment date + shipping time = planned delivery date</span></span>


## <a name="see-also"></a><span data-ttu-id="66a8a-122">Se også</span><span class="sxs-lookup"><span data-stu-id="66a8a-122">See Also</span></span>  
 <span data-ttu-id="66a8a-123">[Beregning af forfaldsdato for køb](purchasing-date-calculation-for-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="66a8a-123">[Date Calculation for Purchases](purchasing-date-calculation-for-purchases.md) </span></span>  
 [<span data-ttu-id="66a8a-124">Beregne ordrebekræftelsesdatoer</span><span class="sxs-lookup"><span data-stu-id="66a8a-124">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="66a8a-125">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="66a8a-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
