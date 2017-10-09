---
title: "Håndtere lager- og produktionsomkostninger | Microsoft Docs"
description: "Selvom meget af funktionaliteten i omkostningsberegningen er udtrykt i underliggende processer, der ikke kræver brugermedvirken, f.eks. efterudligning og automatisk kostregulering, er en række felter, vinduer og rapporter beregnet til brugere, som direkte eller indirekte styrer varepriser eller drift."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/09/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 2745d8b06967549b32c8014a24ab9958c72c1c9d
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="handling-inventory-and-manufacturing-costs"></a><span data-ttu-id="c8dbc-103">Håndtere lager- og produktionsomkostninger</span><span class="sxs-lookup"><span data-stu-id="c8dbc-103">Handling Inventory and Manufacturing Costs</span></span>
<span data-ttu-id="c8dbc-104">Selvom meget af funktionaliteten i omkostningsberegningen er udtrykt i underliggende processer, der ikke kræver brugermedvirken, f.eks. efterudligning og automatisk kostregulering, er en række felter, vinduer og rapporter beregnet til brugere, som direkte eller indirekte styrer varepriser eller drift.</span><span class="sxs-lookup"><span data-stu-id="c8dbc-104">Although much of the cost accounting functionality is expressed in underlying processes with no user interaction, such as entry application and automatic cost adjustment, a number of fields, windows, and reports are aimed at users who directly or indirectly manage the cost of items or operations.</span></span>  

 <span data-ttu-id="c8dbc-105">Tildeling af varegebyrer til købsdokumenter er et eksempel på en opgave til indirekte omkostningsberegning.</span><span class="sxs-lookup"><span data-stu-id="c8dbc-105">Assigning item charges to purchase documents is an example of an indirect cost accounting task.</span></span> <span data-ttu-id="c8dbc-106">Opdatering af kostprisen for montage eller produktionsstyklistevare er et eksempel på en opgave til en mere direkte omkostningsberegning.</span><span class="sxs-lookup"><span data-stu-id="c8dbc-106">Updating the unit cost of assembly or production BOM item is an example of a more direct cost accounting task.</span></span>  

 <span data-ttu-id="c8dbc-107">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="c8dbc-107">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="c8dbc-108">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="c8dbc-108">**To**</span></span>|<span data-ttu-id="c8dbc-109">**Se**</span><span class="sxs-lookup"><span data-stu-id="c8dbc-109">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="c8dbc-110">Opdatere købsprisen for en eller flere varer - periodisk eller automatisk - for at videresende eventuelle kostprisændringer fra indgående poster, f.eks. posterne for køb eller produktionsoutput, til de relaterede udgående poster, f.eks. forbrug eller overførsler.</span><span class="sxs-lookup"><span data-stu-id="c8dbc-110">Periodically or automatically update the unit cost of one or multiple items to forward any cost changes from inbound entries, such as those for purchases or production output, to the related outbound entries, such as consumption or transfers.</span></span>|[<span data-ttu-id="c8dbc-111">Fremgangsmåde: Regulere varepriser</span><span class="sxs-lookup"><span data-stu-id="c8dbc-111">How to: Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|  
|<span data-ttu-id="c8dbc-112">Få indsigt i dynamikken i forbindelse med gennemsnitsomkostninger, når der træffes prissætningsbeslutninger eller spores udsving i omkostningerne, som skyldes fejl i dataposterne.</span><span class="sxs-lookup"><span data-stu-id="c8dbc-112">Get insight into average cost dynamics to make pricing decisions or to track cost fluctuations caused by data entry errors.</span></span>|[<span data-ttu-id="c8dbc-113">Fremgangsmåde: Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="c8dbc-113">How to: Register New Items</span></span>](inventory-how-register-new-items.md)|  
|<span data-ttu-id="c8dbc-114">Oprette en produktionsvares standardkostpris ved at angive de tre omkostningselementer: materialer, kapacitet og underleverandør.</span><span class="sxs-lookup"><span data-stu-id="c8dbc-114">Create a manufacturing item's standard cost by entering the three cost elements: material cost, capacity cost, and subcontractor cost.</span></span>|[<span data-ttu-id="c8dbc-115">Om beregning af standardomkostning</span><span class="sxs-lookup"><span data-stu-id="c8dbc-115">About Calculating Standard Cost</span></span>](finance-about-calculating-standard-cost.md)|  
|<span data-ttu-id="c8dbc-116">Beregne kostprisen for en styklistevare baseret på købsprisen for de underliggende komponenter.</span><span class="sxs-lookup"><span data-stu-id="c8dbc-116">Calculate the unit cost of a BOM item based on the unit costs of its underlying components.</span></span>|[<span data-ttu-id="c8dbc-117">Fremgangsmåde: Arbejde med styklister</span><span class="sxs-lookup"><span data-stu-id="c8dbc-117">How to: Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)|  
|<span data-ttu-id="c8dbc-118">Fuldføre prisberegningens livscyklus for en produceret vare ved at regulere omkostningerne og afstemme værdiposterne med finansposterne.</span><span class="sxs-lookup"><span data-stu-id="c8dbc-118">Complete the costing life cycle of a produced item by adjusting the costs and reconciling the value entries with the general ledger.</span></span>|[<span data-ttu-id="c8dbc-119">Om de færdige produktionsomkostninger</span><span class="sxs-lookup"><span data-stu-id="c8dbc-119">About Finished Production Order Costs</span></span>](finance-about-finished-production-order-costs.md)|  
|<span data-ttu-id="c8dbc-120">Ændre værdien for en vare på lageret eller værdien af én varepost, f.eks. en købstransaktion.</span><span class="sxs-lookup"><span data-stu-id="c8dbc-120">Change the value of an item in inventory or the value of one item ledger entry, such as a purchase transaction.</span></span>|[<span data-ttu-id="c8dbc-121">Fremgangsmåde: Regulere lagerbeholdningen</span><span class="sxs-lookup"><span data-stu-id="c8dbc-121">How to: Revalue Inventory</span></span>](inventory-how-revalue-inventory.md)|
|<span data-ttu-id="c8dbc-122">Fortryde en vareudligning manuelt eller udligne automatisk oprettede vareposter igen.</span><span class="sxs-lookup"><span data-stu-id="c8dbc-122">Manually undo an item application or reapply item ledger entries created by the program.</span></span>|[<span data-ttu-id="c8dbc-123">Fremgangsmåde: Fjerne og genanvende poster</span><span class="sxs-lookup"><span data-stu-id="c8dbc-123">How to: Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)|  
|<span data-ttu-id="c8dbc-124">Brug feltet **Udlign fra-post** i varekladden til manuelt at oprette en fast udligning mellem en indgående transaktion og den oprindelige udgående transaktion.</span><span class="sxs-lookup"><span data-stu-id="c8dbc-124">Use the **Applies-from Entry** field in the item journal to manually create a fixed application between an inbound transaction and the original outbound transaction.</span></span>|[<span data-ttu-id="c8dbc-125">Sådan gør du: Lukke åbne vareposter, der fremkommer ved fast udligning i varekladden</span><span class="sxs-lookup"><span data-stu-id="c8dbc-125">How to: Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)|  

## <a name="see-also"></a><span data-ttu-id="c8dbc-126">Se også</span><span class="sxs-lookup"><span data-stu-id="c8dbc-126">See Also</span></span>  
<span data-ttu-id="c8dbc-127">[Administrere lageromkostninger](finance-manage-inventory-costs.md)
[Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)</span><span class="sxs-lookup"><span data-stu-id="c8dbc-127">[Manage Inventory Costs](finance-manage-inventory-costs.md)
[Design Details: Inventory Costing](design-details-inventory-costing.md)</span></span>

