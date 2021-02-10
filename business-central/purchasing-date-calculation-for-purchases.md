---
title: Datoberegning for køb | Microsoft Docs
description: Programmet beregner automatisk den dato, hvor du skal bestille en vare for at have den på lager på en bestemt dato. Dette er den dato, du kan forvente, at varer, der er bestilt på en bestemt dato, er disponible til pluk.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 22153df1e56d274256b53d426e2dff30cad3e4bc
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758588"
---
# <a name="date-calculation-for-purchases"></a><span data-ttu-id="253ba-104">Beregning af forfaldsdato for køb</span><span class="sxs-lookup"><span data-stu-id="253ba-104">Date Calculation for Purchases</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="253ba-105">beregner automatisk den dato, hvor du skal bestille en vare for at have den på lager på en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="253ba-105">automatically calculates the date on which you must order an item to have it in inventory on a certain date.</span></span> <span data-ttu-id="253ba-106">Dette er den dato, du kan forvente, at varer, der er bestilt på en bestemt dato, er disponible til pluk.</span><span class="sxs-lookup"><span data-stu-id="253ba-106">This is the date on which you can expect items ordered on a particular date to be available for picking.</span></span>  

<span data-ttu-id="253ba-107">Hvis du angiver en ønsket modtagelsesdato på et købsordrehoved, er den beregnede ordredato den dato, hvor ordren skal være placeret for at modtage varerne på den dato, du har anmodet om.</span><span class="sxs-lookup"><span data-stu-id="253ba-107">If you specify a requested receipt date on a purchase order header, then the calculated order date is the date on which the order must be placed to receive the items on the date that you requested.</span></span> <span data-ttu-id="253ba-108">Derefter beregnes den dato, hvor varerne er disponible til pluk, og datoen indsættes i feltet **Forventet modt.dato**.</span><span class="sxs-lookup"><span data-stu-id="253ba-108">Then, the date on which the items are available for picking is calculated and entered in the **Expected Receipt Date** field.</span></span>  

<span data-ttu-id="253ba-109">Hvis du ikke indtaster en ønsket modtagelsesdato, er det ordredatoen på linjen, der bruges som udgangspunkt for beregning af den dato, hvor du kan forvente at modtage varerne samt datoen, hvor varerne er disponible til plukning.</span><span class="sxs-lookup"><span data-stu-id="253ba-109">If you do not specify a requested receipt date, then the order date on the line is used as the starting point for calculating the date on which you can expect to receive the items and the date on which the items are available for picking.</span></span>  

## <a name="calculating-with-a-requested-receipt-date"></a><span data-ttu-id="253ba-110">Beregning med en ønsket modtagelsesdato</span><span class="sxs-lookup"><span data-stu-id="253ba-110">Calculating with a requested receipt date</span></span>

<span data-ttu-id="253ba-111">Hvis der står en ønsket modtagelsesdato på købslinjen, bruges denne dato som udgangspunkt for følgende beregninger.</span><span class="sxs-lookup"><span data-stu-id="253ba-111">If there is a requested receipt date on the purchase order line, then that date is used as the starting point for the following calculations.</span></span>  

- <span data-ttu-id="253ba-112">Ønsket modtagelsesdato - Leveringstidsberegning = Ordredato</span><span class="sxs-lookup"><span data-stu-id="253ba-112">requested receipt date - lead time calculation = order date</span></span>  
- <span data-ttu-id="253ba-113">Ønsket modtagelsesdato + Indgående lagerekspeditionstid + Sikkerhedstid = Forventet modtagelsesdato</span><span class="sxs-lookup"><span data-stu-id="253ba-113">requested receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="253ba-114">Hvis du har indtastet en ønsket modtagelsesdato på købsordrehovedet, kopieres denne dato til det tilsvarende felt på alle ordrelinjerne.</span><span class="sxs-lookup"><span data-stu-id="253ba-114">If you entered a requested receipt date on the purchase order header, then that date is copied to the corresponding field on all the lines.</span></span> <span data-ttu-id="253ba-115">Du kan ændre eller fjerne datoen på en eller flere linjer.</span><span class="sxs-lookup"><span data-stu-id="253ba-115">You can change this date on any of the lines, or you can remove the date on the line.</span></span>  

> [!NOTE]
> <span data-ttu-id="253ba-116">Hvis processen er baseret på bagudrettet beregning, f.eks. hvis du bruger den ønskede modtagelsesdato til at hente ordredatoen, anbefales det, at du bruger datoformler med faste varigheder, f.eks. "5D" for fem dage eller "1U" for én uge.</span><span class="sxs-lookup"><span data-stu-id="253ba-116">If your process is based on backward calculation, for example, if you use the requested receipt date to get the order date, we recommend that you use date formulas that have fixed durations, such as "5D" for five days or "1W" for one week.</span></span> <span data-ttu-id="253ba-117">Datoformler uden faste varigheder, f.eks. "AU" for aktuelle uge eller AM for den aktuelle måned, kan resultere i forkerte datoberegninger.</span><span class="sxs-lookup"><span data-stu-id="253ba-117">Date formulas without fixed durations, such as "CW" for current week or CM for current month, can result in incorrect date calculations.</span></span> <span data-ttu-id="253ba-118">Du kan finde flere oplysninger om datoformler i [Arbejde med kalenderdatoer og-klokkeslæt](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="253ba-118">For more information about date formulas, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

## <a name="calculating-without-a-requested-delivery-date"></a><span data-ttu-id="253ba-119">Beregning uden en ønsket leveringsdato</span><span class="sxs-lookup"><span data-stu-id="253ba-119">Calculating without a requested delivery date</span></span>

<span data-ttu-id="253ba-120">Hvis du angiver en købslinje uden en ønsket leveringsdato, udfyldes feltet **Ordredato** automatisk med datoen fra feltet **Ordredato** på købshovedet.</span><span class="sxs-lookup"><span data-stu-id="253ba-120">If you enter a purchase order line without a requested delivery date, then the **Order Date** field on the line is filled with the date in the **Order Date** field on the purchase order header.</span></span> <span data-ttu-id="253ba-121">Denne dato kan enten være en indtastet dato eller arbejdsdatoen.</span><span class="sxs-lookup"><span data-stu-id="253ba-121">This is either the date that you entered or the work date.</span></span> <span data-ttu-id="253ba-122">Med ordredatoen som udgangspunkt beregnes følgende datoer derefter automatisk til købsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="253ba-122">The following dates are then calculated for the purchase order line, with the order date as the starting point.</span></span>  

- <span data-ttu-id="253ba-123">Ordre dato + Leveringstidsberegning = Planlagt modtagelsesdato</span><span class="sxs-lookup"><span data-stu-id="253ba-123">order date + lead time calculation = planned receipt date</span></span>  
- <span data-ttu-id="253ba-124">Planlagt modtagelsesdato + Indgående lagerekspeditionstid + Sikkerhedstid = Forventet modtagelsesdato</span><span class="sxs-lookup"><span data-stu-id="253ba-124">planned receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="253ba-125">Hvis du ændrer ordredato på linjen, f.eks. når varerne ikke er disponible hos din leverandør før på en senere dato, genberegnes de relevante datoer på linjen automatisk.</span><span class="sxs-lookup"><span data-stu-id="253ba-125">If you change the order date on the line, such as when items are not available at your vendor until a later date, then the relevant dates on the line are automatically recalculated.</span></span>  

<span data-ttu-id="253ba-126">Hvis du ændrer ordredatoen på hovedet, kopieres denne dato til feltet **Ordredato** på alle linjerne, og alle relaterede datofelter genberegnes derefter.</span><span class="sxs-lookup"><span data-stu-id="253ba-126">If you change the order date on the header, then that date is copied to the **Order Date** field on all the lines, and all the related date fields are then recalculated.</span></span>  

## <a name="default-values-for-lead-time-calculation"></a><span data-ttu-id="253ba-127">Standardværdier for beregning af leveringstid</span><span class="sxs-lookup"><span data-stu-id="253ba-127">Default values for lead time calculation</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="253ba-128">bruger værdien fra feltet **Leveringstid** på købsordrelinjen til at beregne ordren og de forventede modtagelsesdatoer.</span><span class="sxs-lookup"><span data-stu-id="253ba-128">uses the value from the **Lead Time Calculation** field on the purchase order line to calculate the order and the expected receipt dates.</span></span>  

<span data-ttu-id="253ba-129">Du kan angive værdien på linjen manuelt eller lade programmet bruge værdier, der er defineret på kreditorkortet, varekortet, lagervarekortet eller vare/leverandør-kataloget.</span><span class="sxs-lookup"><span data-stu-id="253ba-129">You can manually specify the value on the line or let the program use values that are defined on the vendor card, item card, stockkeeping unit card, or the item vendor catalog.</span></span>
<span data-ttu-id="253ba-130">Men værdien af leveringstiden på kreditorkortet bruges kun, hvis der ikke er angivet en leveringsperiode på varekortet, lagervarekortet eller vare/leverandør-kataloget for varen.</span><span class="sxs-lookup"><span data-stu-id="253ba-130">However, the lead time value on the vendor card is used only if a lead time is not specified on the item card, stockkeeping unit card, or the item vendor catalog for the item.</span></span> <span data-ttu-id="253ba-131">Dette er også den prioriterede rækkefølge for disse værdier.</span><span class="sxs-lookup"><span data-stu-id="253ba-131">This is also the escalating order of priority for these values.</span></span> <span data-ttu-id="253ba-132">Hvis de alle er angivet, har leveringstiden fra kreditorkortet den laveste prioritet, og leveringstiden fra vare/leverandør-kataloget har den højeste prioritet.</span><span class="sxs-lookup"><span data-stu-id="253ba-132">If they are all provided, the lead time from the vendor card has the lowest priority, and the lead time from the item vendor catalog has the highest priority.</span></span>  

## <a name="see-also"></a><span data-ttu-id="253ba-133">Se også</span><span class="sxs-lookup"><span data-stu-id="253ba-133">See Also</span></span>

<span data-ttu-id="253ba-134">[Beregning af forfaldsdato for salg](sales-date-calculation-for-sales.md) </span><span class="sxs-lookup"><span data-stu-id="253ba-134">[Date Calculation for Sales](sales-date-calculation-for-sales.md) </span></span>  
[<span data-ttu-id="253ba-135">Beregne ordrebekræftelsesdatoer</span><span class="sxs-lookup"><span data-stu-id="253ba-135">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
<span data-ttu-id="253ba-136">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="253ba-136">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
