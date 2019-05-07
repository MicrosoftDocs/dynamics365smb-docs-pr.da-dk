---
title: Datoberegning for salg | Microsoft Docs
description: Programmet beregner automatisk den dato, hvor du skal bestille en vare for at have den på lager på en bestemt dato. Dette er den dato, du kan forvente, at varer, der er bestilt på en bestemt dato, er disponible til pluk.
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
ms.openlocfilehash: a620b7ed9d06cdd8adf7b12bea2b55aecea32bcc
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "918907"
---
# <a name="date-calculation-for-sales"></a><span data-ttu-id="d6be4-104">Beregning af forfaldsdato for salg</span><span class="sxs-lookup"><span data-stu-id="d6be4-104">Date Calculation for Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="d6be4-105">beregner automatisk den tidligst mulige dato, som en vare eller en salgsordrelinje kan sendes på.</span><span class="sxs-lookup"><span data-stu-id="d6be4-105">automatically calculates the earliest possible date that an item on a sales order line can be shipped.</span></span>

<span data-ttu-id="d6be4-106">Hvis debitoren har anmodet om en bestemt leveringsdato, beregnes den dato, hvor varen skal være disponibel til pluk automatisk for at leveringen kan gennemføres rettidigt.</span><span class="sxs-lookup"><span data-stu-id="d6be4-106">If the customer has requested a specific delivery date, then the date on which the items must be available to pick to meet that delivery date is calculated.</span></span>

<span data-ttu-id="d6be4-107">Hvis debitoren ikke anmoder om en bestemt leveringsdato, beregnes den dato, hvor varen kan leveres. Udgangspunktet er den dato, hvor varen er disponibel for pluk.</span><span class="sxs-lookup"><span data-stu-id="d6be4-107">If the customer does not request a specific delivery date, then the date on which the items can be delivered is calculated, starting from the date on which the items are available for picking.</span></span>

## <a name="calculating-a-requested-delivery-date"></a><span data-ttu-id="d6be4-108">Beregning med en ønsket leveringsdato</span><span class="sxs-lookup"><span data-stu-id="d6be4-108">Calculating a Requested Delivery Date</span></span>
<span data-ttu-id="d6be4-109">Hvis der står en ønsket leveringsdato på salgsordrelinjen, bruges denne dato som udgangspunkt for følgende beregninger.</span><span class="sxs-lookup"><span data-stu-id="d6be4-109">If you specify a requested delivery date on the sales order line, then that date is used as the starting point for the following calculations.</span></span>

- <span data-ttu-id="d6be4-110">ønsket leveringsdato– transporttid = planlagt afsendelsesdato</span><span class="sxs-lookup"><span data-stu-id="d6be4-110">requested delivery date - shipping time = planned shipment date</span></span>
- <span data-ttu-id="d6be4-111">planlagt afsendelsesdato – udgående lagerekspeditionstid = planlagt afsendelsesdato</span><span class="sxs-lookup"><span data-stu-id="d6be4-111">planned shipment date - outbound whse. handling time = shipment date</span></span>

<span data-ttu-id="d6be4-112">Hvis varen er disponibel til pluk på afsendelsesdatoen, kan salgsprocessen fortsættes.</span><span class="sxs-lookup"><span data-stu-id="d6be4-112">If the items are available to pick on the shipment date, then the sales process can continue.</span></span>

<span data-ttu-id="d6be4-113">Hvis varen ikke er disponibel til pluk på afsendelsesdatoen, vises en advarsel om, at varen ikke er på lager.</span><span class="sxs-lookup"><span data-stu-id="d6be4-113">If the items are not available to be picked on the shipment date, then a stock-out warning is displayed.</span></span>

## <a name="calculating-the-earliest-possible-delivery-date"></a><span data-ttu-id="d6be4-114">Beregning af den tidligst mulige leveringsdato</span><span class="sxs-lookup"><span data-stu-id="d6be4-114">Calculating the Earliest Possible Delivery Date</span></span>
<span data-ttu-id="d6be4-115">Hvis du ikke angiver en ønsket leveringsdato på en salgsordrelinje, eller hvis ikke den ønskede leveringsdato kan imødekommes, vil den tidligste dato for varernes tilgængelighed blive beregnet.</span><span class="sxs-lookup"><span data-stu-id="d6be4-115">If you do not specify a requested delivery date on the sales order line, or if the requested delivery date cannot be met, then the earliest date on which that the items are available is calculated.</span></span> <span data-ttu-id="d6be4-116">Datoen kan derefter indtastes i feltet Afsendelsesdato på linjen, og den dato, som du planlægger at levere varer samt den dato, hvor de leveres til debitor beregnes ved hjælp af følgende formler.</span><span class="sxs-lookup"><span data-stu-id="d6be4-116">That date is then entered in the Shipment Date field on the line, and the date on which you plan to ship the items as well as the date on which they will be delivered to the customer are calculated using the following formulas.</span></span>

- <span data-ttu-id="d6be4-117">afsendelsesdato + udgående lagerekspeditionstid = planlagt afsendelses dato</span><span class="sxs-lookup"><span data-stu-id="d6be4-117">shipment date + outbound whse. handling time = planned shipment date</span></span>
- <span data-ttu-id="d6be4-118">planlagt afsendelsesdato + transporttid = planlagt leveringsdato</span><span class="sxs-lookup"><span data-stu-id="d6be4-118">planned shipment date + shipping time = planned delivery date</span></span>


## <a name="see-also"></a><span data-ttu-id="d6be4-119">Se også</span><span class="sxs-lookup"><span data-stu-id="d6be4-119">See Also</span></span>  
 <span data-ttu-id="d6be4-120">[Beregning af forfaldsdato for køb](purchasing-date-calculation-for-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="d6be4-120">[Date Calculation for Purchases](purchasing-date-calculation-for-purchases.md) </span></span>  
 [<span data-ttu-id="d6be4-121">Beregne ordrebekræftelsesdatoer</span><span class="sxs-lookup"><span data-stu-id="d6be4-121">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="d6be4-122">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d6be4-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
