---
title: Datoberegning for køb | Microsoft Docs
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
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 08d2f6498019b8ee0a646cec891ff897a62dc9de
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792846"
---
# <a name="date-calculation-for-purchases"></a><span data-ttu-id="f3af7-104">Beregning af forfaldsdato for køb</span><span class="sxs-lookup"><span data-stu-id="f3af7-104">Date Calculation for Purchases</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="f3af7-105">beregner automatisk den dato, hvor du skal bestille en vare for at have den på lager på en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="f3af7-105">automatically calculates the date on which you must order an item to have it in inventory on a certain date.</span></span> <span data-ttu-id="f3af7-106">Dette er den dato, du kan forvente, at varer, der er bestilt på en bestemt dato, er disponible til pluk.</span><span class="sxs-lookup"><span data-stu-id="f3af7-106">This is the date on which you can expect items ordered on a particular date to be available for picking.</span></span>  

<span data-ttu-id="f3af7-107">Hvis du angiver en ønsket modtagelsesdato på et købsordrehoved, er den beregnede ordredato den dato, hvor ordren skal være placeret for at modtage varerne på den dato, du har anmodet om.</span><span class="sxs-lookup"><span data-stu-id="f3af7-107">If you specify a requested receipt date on a purchase order header, then the calculated order date is the date on which the order must be placed to receive the items on the date that you requested.</span></span> <span data-ttu-id="f3af7-108">Derefter beregnes den dato, hvor varerne er disponible til pluk, og datoen indsættes i feltet **Forventet modt.dato**.</span><span class="sxs-lookup"><span data-stu-id="f3af7-108">Then, the date on which the items are available for picking is calculated and entered in the **Expected Receipt Date** field.</span></span>  

<span data-ttu-id="f3af7-109">Hvis du ikke indtaster en ønsket modtagelsesdato, er det ordredatoen på linjen, der bruges som udgangspunkt for beregning af den dato, hvor du kan forvente at modtage varerne samt datoen, hvor varerne er disponible til plukning.</span><span class="sxs-lookup"><span data-stu-id="f3af7-109">If you do not specify a requested receipt date, then the order date on the line is used as the starting point for calculating the date on which you can expect to receive the items and the date on which the items are available for picking.</span></span>  

## <a name="calculating-with-a-requested-receipt-date"></a><span data-ttu-id="f3af7-110">Beregning med en ønsket modtagelsesdato</span><span class="sxs-lookup"><span data-stu-id="f3af7-110">Calculating with a Requested Receipt Date</span></span>  
<span data-ttu-id="f3af7-111">Hvis der står en ønsket modtagelsesdato på købslinjen, bruges denne dato som udgangspunkt for følgende beregninger.</span><span class="sxs-lookup"><span data-stu-id="f3af7-111">If there is a requested receipt date on the purchase order line, then that date is used as the starting point for the following calculations.</span></span>  

- <span data-ttu-id="f3af7-112">Ønsket modtagelsesdato - Leveringstidsberegning = Ordredato</span><span class="sxs-lookup"><span data-stu-id="f3af7-112">requested receipt date - lead time calculation = order date</span></span>  
- <span data-ttu-id="f3af7-113">Ønsket modtagelsesdato + Indgående lagerekspeditionstid + Sikkerhedstid = Forventet modtagelsesdato</span><span class="sxs-lookup"><span data-stu-id="f3af7-113">requested receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="f3af7-114">Hvis du har indtastet en ønsket modtagelsesdato på købsordrehovedet, kopieres denne dato til det tilsvarende felt på alle ordrelinjerne.</span><span class="sxs-lookup"><span data-stu-id="f3af7-114">If you entered a requested receipt date on the purchase order header, then that date is copied to the corresponding field on all the lines.</span></span> <span data-ttu-id="f3af7-115">Du kan ændre eller fjerne datoen på en eller flere linjer.</span><span class="sxs-lookup"><span data-stu-id="f3af7-115">You can change this date on any of the lines, or you can remove the date on the line.</span></span>  

## <a name="calculating-without-a-requested-delivery-date"></a><span data-ttu-id="f3af7-116">Beregning uden en ønsket leveringsdato</span><span class="sxs-lookup"><span data-stu-id="f3af7-116">Calculating without a Requested Delivery Date</span></span>  
<span data-ttu-id="f3af7-117">Hvis du angiver en købslinje uden en ønsket leveringsdato, udfyldes feltet **Ordredato** automatisk med datoen fra feltet **Ordredato** på købshovedet.</span><span class="sxs-lookup"><span data-stu-id="f3af7-117">If you enter a purchase order line without a requested delivery date, then the **Order Date** field on the line is filled with the date in the **Order Date** field on the purchase order header.</span></span> <span data-ttu-id="f3af7-118">Denne dato kan enten være en indtastet dato eller arbejdsdatoen.</span><span class="sxs-lookup"><span data-stu-id="f3af7-118">This is either the date that you entered or the work date.</span></span> <span data-ttu-id="f3af7-119">Med ordredatoen som udgangspunkt beregnes følgende datoer derefter automatisk til købsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="f3af7-119">The following dates are then calculated for the purchase order line, with the order date as the starting point.</span></span>  

- <span data-ttu-id="f3af7-120">Ordre dato + Leveringstidsberegning = Planlagt modtagelsesdato</span><span class="sxs-lookup"><span data-stu-id="f3af7-120">order date + lead time calculation = planned receipt date</span></span>  
- <span data-ttu-id="f3af7-121">Planlagt modtagelsesdato + Indgående lagerekspeditionstid + Sikkerhedstid = Forventet modtagelsesdato</span><span class="sxs-lookup"><span data-stu-id="f3af7-121">planned receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="f3af7-122">Hvis du ændrer ordredato på linjen, f.eks. når varerne ikke er disponible hos din leverandør før på en senere dato, genberegnes de relevante datoer på linjen automatisk.</span><span class="sxs-lookup"><span data-stu-id="f3af7-122">If you change the order date on the line, such as when items are not available at your vendor until a later date, then the relevant dates on the line are automatically recalculated.</span></span>  

<span data-ttu-id="f3af7-123">Hvis du ændrer ordredatoen på hovedet, kopieres denne dato til feltet **Ordredato** på alle linjerne, og alle relaterede datofelter genberegnes derefter.</span><span class="sxs-lookup"><span data-stu-id="f3af7-123">If you change the order date on the header, then that date is copied to the **Order Date** field on all the lines, and all the related date fields are then recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f3af7-124">Se også</span><span class="sxs-lookup"><span data-stu-id="f3af7-124">See Also</span></span>  
 <span data-ttu-id="f3af7-125">[Beregning af forfaldsdato for salg](sales-date-calculation-for-sales.md) </span><span class="sxs-lookup"><span data-stu-id="f3af7-125">[Date Calculation for Sales](sales-date-calculation-for-sales.md) </span></span>  
 [<span data-ttu-id="f3af7-126">Beregne ordrebekræftelsesdatoer</span><span class="sxs-lookup"><span data-stu-id="f3af7-126">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="f3af7-127">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f3af7-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
