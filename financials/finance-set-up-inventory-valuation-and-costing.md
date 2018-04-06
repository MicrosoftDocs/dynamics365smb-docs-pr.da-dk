---
title: "Opsætning af lagerværdi og lageromkostningsadministration | Microsoft Docs"
description: "Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f6d1d0da42bbc6bf186845648552eb639731759f
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-inventory-valuation-and-costing"></a><span data-ttu-id="1ef02-103">Opsætte lagerværdi og kostprisberegning</span><span class="sxs-lookup"><span data-stu-id="1ef02-103">Setting Up Inventory Valuation and Costing</span></span>
<span data-ttu-id="1ef02-104">For at sikre, at lageromkostningerne registreres korrekt, skal du angive forskellige felter og vinduer, før du begynder at foretage varetransaktioner.</span><span class="sxs-lookup"><span data-stu-id="1ef02-104">To make sure that inventory costs are recorded correctly, you must set up various fields and windows before you begin to make item transactions.</span></span>

<span data-ttu-id="1ef02-105">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="1ef02-105">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="1ef02-106">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="1ef02-106">**To**</span></span>|<span data-ttu-id="1ef02-107">**Se**</span><span class="sxs-lookup"><span data-stu-id="1ef02-107">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="1ef02-108">Definere en prisberegningsmetode for hver vare, der skal styre, hvordan varens indgående kostpris bruges til at vurdere lagerværdi og kostprisen på solgte varer.</span><span class="sxs-lookup"><span data-stu-id="1ef02-108">Set a costing method for each item to govern how its incoming cost is used to assess inventory value and the cost of goods sold.</span></span>|[<span data-ttu-id="1ef02-109">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="1ef02-109">Register New Items</span></span>](inventory-how-register-new-items.md)|  
|<span data-ttu-id="1ef02-110">Kontrollere, at kostprisen automatisk bogføres til finansposterne, hver gang en lagertransaktion bogføres.</span><span class="sxs-lookup"><span data-stu-id="1ef02-110">Ensure that the cost is automatically posted to the general ledger whenever an inventory transaction is posted.</span></span>|<span data-ttu-id="1ef02-111">Feltet **Aut. lagerværdibogføring** på siden **Lageropsætning**</span><span class="sxs-lookup"><span data-stu-id="1ef02-111">**Automatic Cost Posting** field in the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="1ef02-112">Kontrollere, at forventede kostpriser bogføres til finansposterne, så der fra de midlertidige lagerbeholdningskonti kan ses et estimat over forfaldne beløb og kostprisen for de handlede varer, før de reelt faktureres.</span><span class="sxs-lookup"><span data-stu-id="1ef02-112">Ensure that expected costs are posted to the general ledger to see from the interim G/L accounts an estimate of the amounts due and the cost of the traded items before they are actually invoiced.</span></span>|<span data-ttu-id="1ef02-113">Feltet **Bogf. af forventet kostpris** på siden **Lageropsætning**</span><span class="sxs-lookup"><span data-stu-id="1ef02-113">**Expected Cost Posting to G/L** field in the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="1ef02-114">Definere systemet, så der automatisk reguleres for eventuelle kostprisændringer, hver gang du bogfører lagertransaktioner.</span><span class="sxs-lookup"><span data-stu-id="1ef02-114">Set the system up to adjust for any cost changes automatically every time you post inventory transactions.</span></span>|[<span data-ttu-id="1ef02-115">Regulere varepriser</span><span class="sxs-lookup"><span data-stu-id="1ef02-115">Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|  
|<span data-ttu-id="1ef02-116">Definere, om gennemsnitskostprisen kun skal beregnes pr. vare for hver lagerenhed og for hver varevariant.</span><span class="sxs-lookup"><span data-stu-id="1ef02-116">Define if the average cost is to be calculated per item only or per item for each stockkeping unit and for each variant of the item.</span></span>|<span data-ttu-id="1ef02-117">Feltet **Beregn.type for gnsn. kostpris** på siden **Lageropsætning**</span><span class="sxs-lookup"><span data-stu-id="1ef02-117">**Average Cost Calc. Type** field in the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="1ef02-118">Vælge den tidsperiode, programmet skal anvende til beregning af den vægtede gennemsnitsomkostning for varer, der bruger gennemsnitsprisberegningsmetoden.</span><span class="sxs-lookup"><span data-stu-id="1ef02-118">Select the period of time you would like the program to use for calculating the weighted average cost of items that use the average costing method.</span></span>|<span data-ttu-id="1ef02-119">Feltet **Gennemsnitlig omkostningsperiode** på siden **Lageropsætning**</span><span class="sxs-lookup"><span data-stu-id="1ef02-119">**Average Cost Period** field in the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="1ef02-120">Definere lagerperioder for at kontrollere lagerværdi over tid ved ikke at tillade bogføring af transaktioner i lukkede lagerperioder.</span><span class="sxs-lookup"><span data-stu-id="1ef02-120">Define inventory periods to control inventory value over time by disallowing transaction posting in closed inventory periods.</span></span>|[<span data-ttu-id="1ef02-121">Arbejde med lagerperioder</span><span class="sxs-lookup"><span data-stu-id="1ef02-121">Work with Inventory Periods</span></span>](finance-how-to-work-with-inventory-periods.md)|  
|<span data-ttu-id="1ef02-122">Sørg for, at salgsopgørelser udlignes til den oprindelige udgående transaktion for at bevare lagerværdi.</span><span class="sxs-lookup"><span data-stu-id="1ef02-122">Ensure that sales returns are applied to the original outbound transaction to preserve inventory value.</span></span>|<span data-ttu-id="1ef02-123">Feltet **Obl. præcis kostprisudligning** på siden **Salg og tilgodehavender**</span><span class="sxs-lookup"><span data-stu-id="1ef02-123">**Exact Cost Reversing Mandatory** field in the **Sales & Receivables** page</span></span>|  
|<span data-ttu-id="1ef02-124">Sørg for, at returneringer af køb udlignes til den oprindelige indgående transaktion for at bevare lagerværdi.</span><span class="sxs-lookup"><span data-stu-id="1ef02-124">Ensure that purchase returns are applied to the original inbound transaction to preserve inventory value.</span></span>|<span data-ttu-id="1ef02-125">Feltet **Obl. præcis kostprisudligning** på siden **Køb og tilgodehavender**</span><span class="sxs-lookup"><span data-stu-id="1ef02-125">**Exact Cost Reversing Mandatory** field in the **´Purchases & Payables** page</span></span>|
|<span data-ttu-id="1ef02-126">Definere afrundingsregler, der skal anvendes ved regulering af eller forslag til varepriser eller standardomkostninger.</span><span class="sxs-lookup"><span data-stu-id="1ef02-126">Set up the rounding rules to apply when adjusting or suggesting item prices and when adjusting or suggesting standard costs.</span></span>|<span data-ttu-id="1ef02-127">Siden **Afrundingsmetode**</span><span class="sxs-lookup"><span data-stu-id="1ef02-127">**Rounding Method** page</span></span>|  

## <a name="see-also"></a><span data-ttu-id="1ef02-128">Se også</span><span class="sxs-lookup"><span data-stu-id="1ef02-128">See Also</span></span>  
[<span data-ttu-id="1ef02-129">Administrere lageromkostninger</span><span class="sxs-lookup"><span data-stu-id="1ef02-129">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="1ef02-130">Arbejde med Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="1ef02-130">Working with Finance and Operations, Business edition</span></span>](ui-work-product.md)  
[<span data-ttu-id="1ef02-131">Finans</span><span class="sxs-lookup"><span data-stu-id="1ef02-131">Finance</span></span>](finance.md)  

