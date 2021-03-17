---
title: Designoplysninger – Lagerværdi | Microsoft Docs
description: Lagerværdi er bestemmelsen af kostprisen for en lagervare.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 497c2fb891af31af20a6b7a150edd9a9907748e2
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389845"
---
# <a name="design-details-inventory-valuation"></a><span data-ttu-id="d396c-103">Designoplysninger: Lagerværdi</span><span class="sxs-lookup"><span data-stu-id="d396c-103">Design Details: Inventory Valuation</span></span>
<span data-ttu-id="d396c-104">Lagerværdi er bestemmelse af de omkostninger, der er tildelt en lagervare, som udtrykt ved følgende ligning.</span><span class="sxs-lookup"><span data-stu-id="d396c-104">Inventory valuation is the determination of the cost that is assigned to an inventory item, as expressed by the following equation.</span></span>  

<span data-ttu-id="d396c-105">Afslutningslager = begyndelseslager + nettokøb – produktionspris</span><span class="sxs-lookup"><span data-stu-id="d396c-105">Ending inventory = beginning inventory + net purchases – cost of goods sold</span></span>  

<span data-ttu-id="d396c-106">Beregningen af lagerværdien bruger feltet **Kostbeløb (faktisk)** i værdiposterne for varen.</span><span class="sxs-lookup"><span data-stu-id="d396c-106">The calculation of inventory valuation uses the **Cost Amount (Actual)** field of the value entries for the item.</span></span> <span data-ttu-id="d396c-107">Posterne er klassificeret i henhold til den posttype, der svarer til omkostningskomponenter, direkte omkostninger, indirekte omkostninger, afvigelse, værdiregulering og afrunding.</span><span class="sxs-lookup"><span data-stu-id="d396c-107">The entries are classified according to the entry type that corresponds to the cost components, direct cost, indirect cost, variance, revaluation, and rounding.</span></span> <span data-ttu-id="d396c-108">Du kan finde flere oplysninger i [Designoplysninger: Omkostningskomponenter](design-details-cost-components.md).</span><span class="sxs-lookup"><span data-stu-id="d396c-108">For more information, see [Design Details: Cost Components](design-details-cost-components.md).</span></span>  

<span data-ttu-id="d396c-109">Poster udlignes med hinanden, enten ved fast udligning eller i henhold til det forventede generelle kostprisforløb, der er defineret af kostmetoden.</span><span class="sxs-lookup"><span data-stu-id="d396c-109">Entries are applied against each other, either by the fixed application or according to the general cost-flow assumption defined by the costing method.</span></span> <span data-ttu-id="d396c-110">En post på lagerreducering kan anvendes til mere end én tilgangspost med forskellige bogføringsdatoer og eventuelle andre anskaffelsesomkostninger.</span><span class="sxs-lookup"><span data-stu-id="d396c-110">One entry of inventory decrease can be applied to more than one increase entry with different posting dates and possibly different acquisition costs.</span></span> <span data-ttu-id="d396c-111">Du kan finde flere oplysninger i [Designoplysninger: Vareudligning](design-details-item-application.md).</span><span class="sxs-lookup"><span data-stu-id="d396c-111">For more information, see [Design Details: Item Application](design-details-item-application.md).</span></span> <span data-ttu-id="d396c-112">Beregning af lagerværdien for en given dato er derfor baseret på en opsummering af positive og negative værdiposter.</span><span class="sxs-lookup"><span data-stu-id="d396c-112">Therefore, calculation of the inventory value for a given date is based on summing up positive and negative value entries.</span></span>  

## <a name="inventory-valuation-report"></a><span data-ttu-id="d396c-113">Lagerværdirapport</span><span class="sxs-lookup"><span data-stu-id="d396c-113">Inventory Valuation report</span></span>  
<span data-ttu-id="d396c-114">For at beregne lagerværdien i rapporten **Lagerværdi** begynder rapporten at beregne varens lagerværdi på en angivet startdato.</span><span class="sxs-lookup"><span data-stu-id="d396c-114">To calculate the inventory value in the **Inventory Valuation** report, the report begins by calculating the value of the item’s inventory at a given starting date.</span></span> <span data-ttu-id="d396c-115">Derefter tilføjes værdien af lagerforøgelser, og værdien af lagerreduceringer fratrækkes op til en bestemt slutdato.</span><span class="sxs-lookup"><span data-stu-id="d396c-115">It then adds the value of inventory increases and subtracts the value of inventory decreases up to a given ending date.</span></span> <span data-ttu-id="d396c-116">Slutresultatet er lagerværdien på slutdatoen.</span><span class="sxs-lookup"><span data-stu-id="d396c-116">The end result is the inventory value on the ending date.</span></span> <span data-ttu-id="d396c-117">Rapporten beregner disse værdier ved at addere værdierne i feltet **Kostbeløb (faktisk)** i værdiposterne med bogføringsdatoerne som filtre.</span><span class="sxs-lookup"><span data-stu-id="d396c-117">The report calculates these values by summing the values in the **Cost Amount (Actual)** field in the value entries, using the posting dates as filters.</span></span>  

<span data-ttu-id="d396c-118">Den udskrevne rapport viser altid faktiske beløb, det vil sige købsprisen for poster, der er bogført som fakturerede.</span><span class="sxs-lookup"><span data-stu-id="d396c-118">The printed report always shows actual amounts, that is, the cost of entries that have been posted as invoiced.</span></span> <span data-ttu-id="d396c-119">Rapporten udskriver også den forventede købspris på poster, der er bogført som modtaget eller leveret, hvis du markerer feltet Medtag forventet kostpris på oversigtspanelet Indstillinger.</span><span class="sxs-lookup"><span data-stu-id="d396c-119">The report will also print the expected cost of entries that have posted as received or shipped, if you select the Include Expected Cost field on the Options FastTab.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="d396c-120">Værdier i rapporten **Lagerværdi** er afstemt med lagerkontoen i Finans, hvilket betyder, at de pågældende værdiposter, er bogført i Finans.</span><span class="sxs-lookup"><span data-stu-id="d396c-120">Values in the **Inventory Valuation** report is reconciled with the Inventory account in the general ledger, meaning the value entries in question have been posted to the general ledger.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="d396c-121">Beløb i kolonnen **Værdi** i rapporten er baseret på bogføringsdatoen af transaktioner for en vare.</span><span class="sxs-lookup"><span data-stu-id="d396c-121">Amounts in the **Value** columns of the report are based on the posting date of transactions for an item.</span></span>  

## <a name="inventory-valuation---wip-report"></a><span data-ttu-id="d396c-122">Lagerværdi – igangværende arbejde, rapport</span><span class="sxs-lookup"><span data-stu-id="d396c-122">Inventory Valuation - WIP report</span></span>  
<span data-ttu-id="d396c-123">En produktionsvirksomhed skal bestemme værdien af tre typer af lagerbeholdning:</span><span class="sxs-lookup"><span data-stu-id="d396c-123">A manufacturing company needs to determine the value of three types of inventory:</span></span>  

* <span data-ttu-id="d396c-124">Lager af råmaterialer</span><span class="sxs-lookup"><span data-stu-id="d396c-124">Raw Materials inventory</span></span>  
* <span data-ttu-id="d396c-125">VIA-lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="d396c-125">WIP inventory</span></span>  
* <span data-ttu-id="d396c-126">Færdigvarelager</span><span class="sxs-lookup"><span data-stu-id="d396c-126">Finished Goods inventory</span></span>  

<span data-ttu-id="d396c-127">Værdien af VIA-lagerbeholdningen bestemmes af følgende ligning:</span><span class="sxs-lookup"><span data-stu-id="d396c-127">The value of WIP inventory is determined by the following equation:</span></span>  

* <span data-ttu-id="d396c-128">Afslutning af igangværende arbejde på lager = Begyndelse på igangværende arbejde på lager + produktionsomkostninger – omkostninger ved producerede varer</span><span class="sxs-lookup"><span data-stu-id="d396c-128">Ending WIP inventory = Beginning WIP inventory + manufacturing costs – cost of goods manufactured</span></span>  

<span data-ttu-id="d396c-129">Hvad angår købt lager, danner værdiposterne grundlag for lagerværdien.</span><span class="sxs-lookup"><span data-stu-id="d396c-129">As for purchased inventory, the value entries provide the basis of the inventory valuation.</span></span> <span data-ttu-id="d396c-130">Beregningen foretages ved hjælp af værdierne i feltet **Kostbeløb (faktisk)** for de vare- og kapacitetsværdiposter, der er knyttet til en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="d396c-130">The calculation is made using the values in the **Cost Amount (Actual)** field of the item and capacity value entries associated with a production order.</span></span>  

<span data-ttu-id="d396c-131">Formålet med VIA-lagerværdi er at bestemme værdien af de varer, hvis produktion endnu ikke er fuldført på en given dato.</span><span class="sxs-lookup"><span data-stu-id="d396c-131">The purpose of WIP inventory valuation is to determine the value of the items whose manufacturing has not yet been completed on a given date.</span></span> <span data-ttu-id="d396c-132">Derfor er VIA-lagerbeholdningen baseret på de værdiposter, der er relateret til forbrugs- og kapacitetsposter.</span><span class="sxs-lookup"><span data-stu-id="d396c-132">Therefore the WIP inventory value is based on the value entries related to the consumption and capacity ledger entries.</span></span> <span data-ttu-id="d396c-133">Forbrugsposter skal være fuldt faktureret ved værdiansættelsesdatoen.</span><span class="sxs-lookup"><span data-stu-id="d396c-133">Consumption ledger entries must be completely invoiced at the date of the valuation.</span></span> <span data-ttu-id="d396c-134">Derfor viser rapporten **Lagerværdi - igangværende arb.** omkostningerne, der repræsenterer det igangværende arbejdes værdi i to kategorier: forbrug og kapacitet.</span><span class="sxs-lookup"><span data-stu-id="d396c-134">Therefore, the **Inventory Valuation – WIP** report shows the costs representing the WIP inventory value in two categories: consumption and capacity.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d396c-135">Se også</span><span class="sxs-lookup"><span data-stu-id="d396c-135">See Also</span></span>  
<span data-ttu-id="d396c-136">[Designoplysninger: Afstemning med Finans](design-details-reconciliation-with-the-general-ledger.md) </span><span class="sxs-lookup"><span data-stu-id="d396c-136">[Design Details: Reconciliation with the General Ledger](design-details-reconciliation-with-the-general-ledger.md) </span></span>  
<span data-ttu-id="d396c-137">[Designoplysninger: Regulering](design-details-revaluation.md) </span><span class="sxs-lookup"><span data-stu-id="d396c-137">[Design Details: Revaluation](design-details-revaluation.md) </span></span>  
<span data-ttu-id="d396c-138">[Designoplysninger: Bogføring af produktionsordrer](design-details-production-order-posting.md)
[Administrere lageromkostninger](finance-manage-inventory-costs.md)</span><span class="sxs-lookup"><span data-stu-id="d396c-138">[Design Details: Production Order Posting](design-details-production-order-posting.md)
[Managing Inventory Costs](finance-manage-inventory-costs.md)</span></span>  
[<span data-ttu-id="d396c-139">Finans</span><span class="sxs-lookup"><span data-stu-id="d396c-139">Finance</span></span>](finance.md)  
<span data-ttu-id="d396c-140">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d396c-140">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]