---
title: Administrere lageromkostninger | Microsoft Docs
description: "Omkostningsadministration, også kendt som \"costing\", vedrører registrering og rapportering af virksomhedens driftsomkostninger. Den omfatter rapportering af produktionsomkostninger og lageromkostninger, dvs. værdien af varer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 088b8fdb11c32594499af752d5c6be652e2f69a6
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="managing-inventory-costs"></a><span data-ttu-id="7e971-104">Administrere lageromkostninger</span><span class="sxs-lookup"><span data-stu-id="7e971-104">Managing Inventory Costs</span></span>
<span data-ttu-id="7e971-105">Omkostningsadministration, også kendt som "costing", vedrører registrering og rapportering af virksomhedens driftsomkostninger.</span><span class="sxs-lookup"><span data-stu-id="7e971-105">Cost management, also referred to as “costing”, is concerned with recording and reporting business operating costs.</span></span> <span data-ttu-id="7e971-106">Den omfatter rapportering af produktionsomkostninger og lageromkostninger, dvs. værdien af varer.</span><span class="sxs-lookup"><span data-stu-id="7e971-106">It includes the reporting of manufacturing costs and inventory costs, that is, the value of items.</span></span>   

<span data-ttu-id="7e971-107">De centrale principper, der er vigtige at forstå, er, at kostmetoder definerer den måde, varer værdiansættes på, når de forlader lageret, at kostregulering opdaterer omkostningerne ved solgte varer med relaterede købsomkostninger bogført efter salget, og at lagerværdier skal bogføres til dedikerede finanskonti med regelmæssige mellemrum.</span><span class="sxs-lookup"><span data-stu-id="7e971-107">Central principles to understand are that costing methods define how items are valued when they leave inventory, that cost adjustment updates the cost of goods sold with related purchase costs posted after the sale, and that inventory values must be posted to dedicated G/L accounts at regular intervals.</span></span>

<span data-ttu-id="7e971-108">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="7e971-108">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="7e971-109">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="7e971-109">**To**</span></span>|<span data-ttu-id="7e971-110">**Se**</span><span class="sxs-lookup"><span data-stu-id="7e971-110">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="7e971-111">Læs forskellige begrebsmæssige oplysninger for at forstå de principper og definitioner, der styrer funktionaliteten for lageromkostningsregnskab i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7e971-111">Read various conceptual information to understand the principles and definitions that govern the inventory costing accounting functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>|[<span data-ttu-id="7e971-112">Om lagerkostmetode</span><span class="sxs-lookup"><span data-stu-id="7e971-112">About Inventory Costing</span></span>](finance-learn-about-costing.md)|  
|<span data-ttu-id="7e971-113">Konfigurere lagerperioder, kostmetoder og afrundingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="7e971-113">Set up inventory periods, costing methods, and rounding methods.</span></span>|[<span data-ttu-id="7e971-114">Opsætte lagerværdi og kostprisberegning</span><span class="sxs-lookup"><span data-stu-id="7e971-114">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)|
|<span data-ttu-id="7e971-115">Op- eller nedskriv værdien af en eller flere varer på lageret ved at bogføre deres aktuelle, beregnede værdi.</span><span class="sxs-lookup"><span data-stu-id="7e971-115">Appreciate or depreciate the value of one or more items in inventory by posting their current, calculated value.</span></span>|[<span data-ttu-id="7e971-116">Regulere lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="7e971-116">Revalue Inventory</span></span>](inventory-how-revalue-inventory.md)|
|<span data-ttu-id="7e971-117">Reguler varepriser, enten automatisk eller manuelt, for at videresende kostprisændringer fra indgående poster til deres relaterede udgående poster.</span><span class="sxs-lookup"><span data-stu-id="7e971-117">Adjust item costs, either automatically or manually, to forward cost changes from inbound entries to their related outbound entries.</span></span>|[<span data-ttu-id="7e971-118">Regulere varepriser</span><span class="sxs-lookup"><span data-stu-id="7e971-118">Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|
|<span data-ttu-id="7e971-119">Brug særlige prisberegningsfunktioner for daglige transaktioner til operationer for varen.</span><span class="sxs-lookup"><span data-stu-id="7e971-119">Use special costing functions for every-day item transactions in the item operations.</span></span>|[<span data-ttu-id="7e971-120">Håndtere lager- og produktionsomkostninger</span><span class="sxs-lookup"><span data-stu-id="7e971-120">Handling Inventory and Manufacturing Costs</span></span>](finance-handle-inventory-and-manufacturing-costs.md)|  
|<span data-ttu-id="7e971-121">Opdater regelmæssigt standardkostprisen for komponenter i montage eller produktionsstyklister, og akkumuler de nye omkostninger til den overordnede vare.</span><span class="sxs-lookup"><span data-stu-id="7e971-121">Periodically update the standard costs of components, in assembly or production BOMs, and roll the new costs up to the parent item.</span></span>|[<span data-ttu-id="7e971-122">Opdatere standardkostpriser</span><span class="sxs-lookup"><span data-stu-id="7e971-122">Update Standard Costs</span></span>](finance-how-to-update-standard-costs.md)|
|<span data-ttu-id="7e971-123">Udføre periodeafslutningskontrol og rapporteringsopgaver, f.eks. beregning af lagerværdi og bogføring af omkostninger i finansposterne.</span><span class="sxs-lookup"><span data-stu-id="7e971-123">Perform period-end control and reporting tasks, such calculate the value of inventory and post costs to the general ledger.</span></span>|[<span data-ttu-id="7e971-124">Rapportere omkostninger og afstemme med regnskabet</span><span class="sxs-lookup"><span data-stu-id="7e971-124">Reporting Costs and Reconciling with the General Ledger</span></span>](finance-report-costs-and-reconcile-with-the-general-ledger.md)|  
|<span data-ttu-id="7e971-125">Få mere at vide om alle mekanismerne i kostsystemet.</span><span class="sxs-lookup"><span data-stu-id="7e971-125">Learn about all mechanisms in the costing system.</span></span>|[<span data-ttu-id="7e971-126">Designoplysninger: Lagerkostmetode</span><span class="sxs-lookup"><span data-stu-id="7e971-126">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)|  

## <a name="see-also"></a><span data-ttu-id="7e971-127">Se også</span><span class="sxs-lookup"><span data-stu-id="7e971-127">See Also</span></span>  
 [<span data-ttu-id="7e971-128">Finans</span><span class="sxs-lookup"><span data-stu-id="7e971-128">Finance</span></span>](finance.md)  
 <span data-ttu-id="7e971-129">[Lagerbeholdning](inventory-manage-inventory.md) </span><span class="sxs-lookup"><span data-stu-id="7e971-129">[Inventory](inventory-manage-inventory.md) </span></span>  
 <span data-ttu-id="7e971-130">[Salg](sales-manage-sales.md) </span><span class="sxs-lookup"><span data-stu-id="7e971-130">[Sales](sales-manage-sales.md) </span></span>  
 [<span data-ttu-id="7e971-131">Køb</span><span class="sxs-lookup"><span data-stu-id="7e971-131">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="7e971-132">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7e971-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

