---
title: Rapportere omkostninger og afstemme med regnskabet | Microsoft Docs
description: Ved afslutningen af regnskabsperioder, hvad enten de er månedlige, årlige eller andet, skal der udføres en række handlinger til omkostningsstyring og revision, så der rapporteres en korrekt og afstemt lagerværdi til regnskabsafdelingen. Bortset fra den bogføringsrutine, der overfører de enkelte poster med vareværdi til dedikerede finanskonti, stilles adskillige rapporter, sporingsfunktioner og et specielt afstemningsværktøj til rådighed for den revisor eller controller, der er ansvarlig for dette forretningskritiske arbejde.
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
ms.openlocfilehash: 1b2a83ddbac54d5034b043c3124f698613be4642
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "793415"
---
# <a name="reporting-costs-and-reconciling-with-the-general-ledger"></a><span data-ttu-id="6c9b1-104">Rapportere omkostninger og afstemme med regnskabet</span><span class="sxs-lookup"><span data-stu-id="6c9b1-104">Reporting Costs and Reconciling with the General Ledger</span></span>
<span data-ttu-id="6c9b1-105">Ved afslutningen af regnskabsperioder, hvad enten de er månedlige, årlige eller andet, skal der udføres en række handlinger til omkostningsstyring og revision, så der rapporteres en korrekt og afstemt lagerværdi til regnskabsafdelingen.</span><span class="sxs-lookup"><span data-stu-id="6c9b1-105">At the end of accounting periods, monthly, yearly or other, a sequence of cost control and auditing tasks must be performed to report a correct and balanced inventory value to the finance department.</span></span> <span data-ttu-id="6c9b1-106">Bortset fra den bogføringsrutine, der overfører de enkelte poster med vareværdi til dedikerede finanskonti, stilles adskillige rapporter, sporingsfunktioner og et specielt afstemningsværktøj til rådighed for den revisor eller controller, der er ansvarlig for dette forretningskritiske arbejde.</span><span class="sxs-lookup"><span data-stu-id="6c9b1-106">Apart from the posting routine that transfers the individual item value entries to dedicated general ledger accounts, several reports, tracing functions, and a special reconciliation tool are available to the auditor or controller responsible for this business-critical work.</span></span>  

 <span data-ttu-id="6c9b1-107">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="6c9b1-107">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="6c9b1-108">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="6c9b1-108">**To**</span></span>|<span data-ttu-id="6c9b1-109">**Se**</span><span class="sxs-lookup"><span data-stu-id="6c9b1-109">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="6c9b1-110">Have vist lagerværdien for de valgte varer, herunder oplysninger om antal og værdi af lagertilgange og -afgange i en valgt periode.</span><span class="sxs-lookup"><span data-stu-id="6c9b1-110">View the inventory value of selected items, including information about the quantities and values of increases and decreases in inventory over a selected period.</span></span>|<span data-ttu-id="6c9b1-111">**Lagerværdirapport**</span><span class="sxs-lookup"><span data-stu-id="6c9b1-111">**Inventory Valuation** report</span></span>|  
|<span data-ttu-id="6c9b1-112">Have vist lagerværdien for valgte produktionsordrer i lageret for igangværende arbejde (VIA), f.eks. antal og værdi af forbrug, kapacitetsudnyttelse og output i igangværende produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="6c9b1-112">View the inventory value of selected production orders in your WIP (work in process) inventory, such as the quantities and values of consumption, capacity usage, and output in ongoing production orders.</span></span>|<span data-ttu-id="6c9b1-113">**Lagerværdi – igangværende arbejde**, rapport</span><span class="sxs-lookup"><span data-stu-id="6c9b1-113">**Inventory Valuation - WIP** report</span></span>|  
|<span data-ttu-id="6c9b1-114">Have vist lagerværdien af valgte varer, herunder deres faktiske og forventede kostpris på den angivne dato.</span><span class="sxs-lookup"><span data-stu-id="6c9b1-114">View the inventory value of selected items, including their actual and expected cost on the date specified.</span></span>|<span data-ttu-id="6c9b1-115">**Lagerværdi – kostspecifikation**, rapport</span><span class="sxs-lookup"><span data-stu-id="6c9b1-115">**Invt. Valuation - Cost Spec.** report</span></span>|  
|<span data-ttu-id="6c9b1-116">Bruge en rapport til at analysere årsagerne til kostprisuoverensstemmelser eller få indsigt i vareforbruget for solgte varer.</span><span class="sxs-lookup"><span data-stu-id="6c9b1-116">Use a report to analyze the reasons for cost variances or to gain insight into the cost shares of sold items (COGS).</span></span>|<span data-ttu-id="6c9b1-117">**Grundlag for kostprisfordeling**, rapport</span><span class="sxs-lookup"><span data-stu-id="6c9b1-117">**Cost Shares Breakdown** report</span></span>|  
|<span data-ttu-id="6c9b1-118">Periodisk bogføre værdiposterne for varetransaktioner fra lagerposter til relaterede finansposter for at afstemme de to posttyper.</span><span class="sxs-lookup"><span data-stu-id="6c9b1-118">Periodically post the value entries of item transactions from the inventory ledger to the related G/L accounts to reconcile the two ledgers.</span></span>|[<span data-ttu-id="6c9b1-119">Afstemme lagerværdier med finansregnskabet</span><span class="sxs-lookup"><span data-stu-id="6c9b1-119">Reconcile Inventory Costs with the General Ledger</span></span>](finance-how-to-post-inventory-costs-to-the-general-ledger.md)|  
|<span data-ttu-id="6c9b1-120">Bruge én side til at revidere afstemningen mellem lagerposterne og finansposterne.</span><span class="sxs-lookup"><span data-stu-id="6c9b1-120">Use one page to audit the reconciliation between the inventory ledger and the general ledger.</span></span>|[<span data-ttu-id="6c9b1-121">Afstemme lagerværdier med finansregnskabet</span><span class="sxs-lookup"><span data-stu-id="6c9b1-121">Reconcile Inventory Costs with the General Ledger</span></span>](finance-how-to-post-inventory-costs-to-the-general-ledger.md)|  
|<span data-ttu-id="6c9b1-122">Fastlægge det VIA-beløb, der skal bogføres til balancekonti ved periodeafslutningsrapportering.</span><span class="sxs-lookup"><span data-stu-id="6c9b1-122">Determine the WIP amount that needs to be posted to balance sheet accounts for period-end reporting.</span></span>|[<span data-ttu-id="6c9b1-123">Overvåge jobstatus og -udførelse</span><span class="sxs-lookup"><span data-stu-id="6c9b1-123">Monitor Job Progress and Performance</span></span>](projects-how-monitor-progress-performance.md)|

## <a name="see-also"></a><span data-ttu-id="6c9b1-124">Se også</span><span class="sxs-lookup"><span data-stu-id="6c9b1-124">See Also</span></span>  
[<span data-ttu-id="6c9b1-125">Opsætte lagerværdi og kostprisberegning</span><span class="sxs-lookup"><span data-stu-id="6c9b1-125">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)  
[<span data-ttu-id="6c9b1-126">Administrere lageromkostninger</span><span class="sxs-lookup"><span data-stu-id="6c9b1-126">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="6c9b1-127">Finans</span><span class="sxs-lookup"><span data-stu-id="6c9b1-127">Finance</span></span>](finance.md)  
<span data-ttu-id="6c9b1-128">[Lagerbeholdning](inventory-manage-inventory.md) </span><span class="sxs-lookup"><span data-stu-id="6c9b1-128">[Inventory](inventory-manage-inventory.md) </span></span>  
<span data-ttu-id="6c9b1-129">[Salg](sales-manage-sales.md) </span><span class="sxs-lookup"><span data-stu-id="6c9b1-129">[Sales](sales-manage-sales.md) </span></span>  
[<span data-ttu-id="6c9b1-130">Køb</span><span class="sxs-lookup"><span data-stu-id="6c9b1-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="6c9b1-131">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6c9b1-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
