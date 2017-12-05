---
title: "Designoplysninger – Ordre | Microsoft Docs"
description: "Dette emne indeholder oplysninger om ordre-til-ordre-links i et miljø med fremstil-til-ordre."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, order
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 24f5c56e9e148128d83593757d820fa62686403e
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-order"></a><span data-ttu-id="039e9-103">Designoplysninger: Ordre</span><span class="sxs-lookup"><span data-stu-id="039e9-103">Design Details: Order</span></span>
<span data-ttu-id="039e9-104">I et Fremstil-til-ordre-miljø bliver en vare købt eller produceret udelukkende til at dække et bestemt behov.</span><span class="sxs-lookup"><span data-stu-id="039e9-104">In a make-to-order environment, an item is purchased or produced to exclusively cover a specific demand.</span></span> <span data-ttu-id="039e9-105">Normalt relateres det til A-varer, og motivationen for at vælge denne ordregenbestillingsmetode kan være, at behovet er sjældent, leveringstiden er ubetydelig, eller de påkrævede attributter varierer.</span><span class="sxs-lookup"><span data-stu-id="039e9-105">Typically it relates to A-items, and the motivation for choosing the order reordering policy can be that the demand is infrequent, the lead-time is insignificant, or the required attributes vary.</span></span>  
  
<span data-ttu-id="039e9-106">Programmet opretter et ordre-til-ordre-link, der fungerer som en indledende forbindelse mellem forsyningen, en forsyningsordre eller lager og det behov, som den eller det skal opfylde.</span><span class="sxs-lookup"><span data-stu-id="039e9-106">The program creates an order-to-order link, which acts as a preliminary connection between the supply, a supply order or inventory, and the demand that it is going to fulfill.</span></span>  
  
<span data-ttu-id="039e9-107">Bortset fra brug af prdrepolitikken, kan ordre-til-ordre-linket anvendes under planlægningen på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="039e9-107">Apart from using the Order policy, the order-to-order link can be applied during planning in the following ways:</span></span>  
  
* <span data-ttu-id="039e9-108">Når produktionsmetoden Fremstil-til-ordre bruges til at oprette produktionsordrer med flere niveauer eller produktionsordrer af projekttype (fremstilling af nødvendige komponenter på den samme produktionsordre).</span><span class="sxs-lookup"><span data-stu-id="039e9-108">When using the Make-to-Order manufacturing policy to create multi-level or project type production orders (producing needed components on the same production order).</span></span>  
* <span data-ttu-id="039e9-109">Når funktionen Salgsordreplanlægning bruges til at oprette en produktionsordre fra en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="039e9-109">When using the Sales Order Planning feature to create a production order from a sales order.</span></span>  
  
<span data-ttu-id="039e9-110">Selvom en produktionsvirksomhed anser sig selv som værende et Fremstil-til-ordre-miljø, kan det være bedst at bruge en genbestillingsmetode med lot-for-lot, hvis varerne er ren standard uden variation i attributter.</span><span class="sxs-lookup"><span data-stu-id="039e9-110">Even if a manufacturing company considers itself as a make-to-order environment, it might be best to use a Lot-for-Lot reordering policy if the items are pure standard without variation in attributes.</span></span> <span data-ttu-id="039e9-111">Som resultat vil systemet bruge ikke-planlagt lagerbeholdning og akkumulerer kun salgsordrer med samme afsendelsesdato eller inden for et defineret interval.</span><span class="sxs-lookup"><span data-stu-id="039e9-111">As a result, the system will use unplanned inventory and only accumulates sales orders with the same shipment date or within a defined time bucket.</span></span>  
  
## <a name="order-to-order-links-and-past-due-dates"></a><span data-ttu-id="039e9-112">Ordre-til-ordre-links og overskredne datoer</span><span class="sxs-lookup"><span data-stu-id="039e9-112">Order-to-Order Links and Past Due Dates</span></span>  
<span data-ttu-id="039e9-113">I modsætning til de fleste forsyning-behov-sæt, planlægges tilknyttede ordrer med forfaldsdatoer, før planlægningsstartdatoen er fuldt planlagt af systemet.</span><span class="sxs-lookup"><span data-stu-id="039e9-113">Unlike most supply-demand sets, linked orders with due dates before the planning starting date are fully planned for by the system.</span></span> <span data-ttu-id="039e9-114">Forretningsårsagen til denne undtagelse er, at bestemte behov-forsyningssæt skal synkroniseres til kørsel.</span><span class="sxs-lookup"><span data-stu-id="039e9-114">The business reason for this exception is that specific demand-supply sets must be synchronized through to execution.</span></span> <span data-ttu-id="039e9-115">Du kan finde flere oplysninger om den fastlåste zone, der gælder for de fleste behovsforsyningstyper i [Designoplysninger: Håndtering af ordrer før planlægningsstartdatoen](design-details-dealing-with-orders-before-the-planning-starting-date.md).</span><span class="sxs-lookup"><span data-stu-id="039e9-115">For more information about the frozen zone that applies to most demand-supply types, see [Design Details: Dealing with Orders Before the Planning Starting Date](design-details-dealing-with-orders-before-the-planning-starting-date.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="039e9-116">Se også</span><span class="sxs-lookup"><span data-stu-id="039e9-116">See Also</span></span>  
<span data-ttu-id="039e9-117">[Designoplysninger: Genbestillingsmetoder](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="039e9-117">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="039e9-118">[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="039e9-118">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="039e9-119">[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="039e9-119">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="039e9-120">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="039e9-120">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)