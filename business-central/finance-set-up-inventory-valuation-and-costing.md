---
title: Opsætning af lagerværdi og lageromkostningsadministration | Microsoft Docs
description: Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 26b7f280afa61bc42af7b728272116731e6947b1
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305664"
---
# <a name="setting-up-inventory-valuation-and-costing"></a><span data-ttu-id="172b9-103">Opsætte lagerværdi og kostprisberegning</span><span class="sxs-lookup"><span data-stu-id="172b9-103">Setting Up Inventory Valuation and Costing</span></span>
<span data-ttu-id="172b9-104">For at sikre, at lageromkostningerne registreres korrekt, skal du angive forskellige felter og sider, før du begynder at foretage varetransaktioner.</span><span class="sxs-lookup"><span data-stu-id="172b9-104">To make sure that inventory costs are recorded correctly, you must set up various fields and pages before you begin to make item transactions.</span></span>

<span data-ttu-id="172b9-105">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="172b9-105">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="172b9-106">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="172b9-106">**To**</span></span>|<span data-ttu-id="172b9-107">**Se**</span><span class="sxs-lookup"><span data-stu-id="172b9-107">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="172b9-108">Definere en prisberegningsmetode for hver vare, der skal styre, hvordan varens indgående kostpris bruges til at vurdere lagerværdi og kostprisen på solgte varer.</span><span class="sxs-lookup"><span data-stu-id="172b9-108">Set a costing method for each item to govern how its incoming cost is used to assess inventory value and the cost of goods sold.</span></span>|[<span data-ttu-id="172b9-109">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="172b9-109">Register New Items</span></span>](inventory-how-register-new-items.md)|  
|<span data-ttu-id="172b9-110">Kontrollere, at kostprisen automatisk bogføres til finansposterne, hver gang en lagertransaktion bogføres.</span><span class="sxs-lookup"><span data-stu-id="172b9-110">Ensure that the cost is automatically posted to the general ledger whenever an inventory transaction is posted.</span></span>|<span data-ttu-id="172b9-111">Feltet **Aut. lagerværdibogføring** på siden **Lageropsætning**</span><span class="sxs-lookup"><span data-stu-id="172b9-111">**Automatic Cost Posting** field on the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="172b9-112">Kontrollere, at forventede kostpriser bogføres til finansposterne, så der fra de midlertidige lagerbeholdningskonti kan ses et estimat over forfaldne beløb og kostprisen for de handlede varer, før de reelt faktureres.</span><span class="sxs-lookup"><span data-stu-id="172b9-112">Ensure that expected costs are posted to the general ledger to see from the interim G/L accounts an estimate of the amounts due and the cost of the traded items before they are actually invoiced.</span></span>|<span data-ttu-id="172b9-113">Feltet **Bogf. af forventet kostpris** på siden **Lageropsætning**</span><span class="sxs-lookup"><span data-stu-id="172b9-113">**Expected Cost Posting to G/L** field on the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="172b9-114">Definere systemet, så der automatisk reguleres for eventuelle kostprisændringer, hver gang du bogfører lagertransaktioner.</span><span class="sxs-lookup"><span data-stu-id="172b9-114">Set the system up to adjust for any cost changes automatically every time you post inventory transactions.</span></span>|[<span data-ttu-id="172b9-115">Regulere varepriser</span><span class="sxs-lookup"><span data-stu-id="172b9-115">Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|  
|<span data-ttu-id="172b9-116">Definere, om gennemsnitskostprisen kun skal beregnes pr. vare for hver lagerenhed og for hver varevariant.</span><span class="sxs-lookup"><span data-stu-id="172b9-116">Define if the average cost is to be calculated per item only or per item for each stockkeping unit and for each variant of the item.</span></span>|<span data-ttu-id="172b9-117">Feltet **Beregn.type for gnsn. kostpris** på siden **Lageropsætning**</span><span class="sxs-lookup"><span data-stu-id="172b9-117">**Average Cost Calc. Type** field on the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="172b9-118">Vælge den tidsperiode, programmet skal anvende til beregning af den vægtede gennemsnitsomkostning for varer, der bruger gennemsnitsprisberegningsmetoden.</span><span class="sxs-lookup"><span data-stu-id="172b9-118">Select the period of time you would like application to use for calculating the weighted average cost of items that use the average costing method.</span></span>|<span data-ttu-id="172b9-119">Feltet **Gennemsnitlig omkostningsperiode** på siden **Lageropsætning**</span><span class="sxs-lookup"><span data-stu-id="172b9-119">**Average Cost Period** field on the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="172b9-120">Definere lagerperioder for at kontrollere lagerværdi over tid ved ikke at tillade bogføring af transaktioner i lukkede lagerperioder.</span><span class="sxs-lookup"><span data-stu-id="172b9-120">Define inventory periods to control inventory value over time by disallowing transaction posting in closed inventory periods.</span></span>|[<span data-ttu-id="172b9-121">Arbejde med lagerperioder</span><span class="sxs-lookup"><span data-stu-id="172b9-121">Work with Inventory Periods</span></span>](finance-how-to-work-with-inventory-periods.md)|  
|<span data-ttu-id="172b9-122">Sørg for, at salgsopgørelser udlignes til den oprindelige udgående transaktion for at bevare lagerværdi.</span><span class="sxs-lookup"><span data-stu-id="172b9-122">Ensure that sales returns are applied to the original outbound transaction to preserve inventory value.</span></span>|<span data-ttu-id="172b9-123">Feltet **Obl. præcis kostprisudligning** på siden **Salg og tilgodehavender**</span><span class="sxs-lookup"><span data-stu-id="172b9-123">**Exact Cost Reversing Mandatory** field on the **Sales & Receivables** page</span></span>|  
|<span data-ttu-id="172b9-124">Sørg for, at returneringer af køb udlignes til den oprindelige indgående transaktion for at bevare lagerværdi.</span><span class="sxs-lookup"><span data-stu-id="172b9-124">Ensure that purchase returns are applied to the original inbound transaction to preserve inventory value.</span></span>|<span data-ttu-id="172b9-125">Feltet **Obl. præcis kostprisudligning** på siden **Køb og tilgodehavender**</span><span class="sxs-lookup"><span data-stu-id="172b9-125">**Exact Cost Reversing Mandatory** field on the **´Purchases & Payables** page</span></span>|
|<span data-ttu-id="172b9-126">Definere afrundingsregler, der skal anvendes ved regulering af eller forslag til varepriser eller standardomkostninger.</span><span class="sxs-lookup"><span data-stu-id="172b9-126">Set up the rounding rules to apply when adjusting or suggesting item prices and when adjusting or suggesting standard costs.</span></span>|<span data-ttu-id="172b9-127">Siden **Afrundingsmetode**</span><span class="sxs-lookup"><span data-stu-id="172b9-127">**Rounding Method** page</span></span>|  

## <a name="see-also"></a><span data-ttu-id="172b9-128">Se også</span><span class="sxs-lookup"><span data-stu-id="172b9-128">See Also</span></span>  
[<span data-ttu-id="172b9-129">Administrere lageromkostninger</span><span class="sxs-lookup"><span data-stu-id="172b9-129">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="172b9-130">Arbejde med Business Central</span><span class="sxs-lookup"><span data-stu-id="172b9-130">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="172b9-131">Finans</span><span class="sxs-lookup"><span data-stu-id="172b9-131">Finance</span></span>](finance.md)  
