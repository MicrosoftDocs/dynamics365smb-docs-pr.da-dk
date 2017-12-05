---
title: Om lagerkostmetode | Microsoft Docs
description: "Administration af lagerkostmetoder vedrører registrering og rapportering af virksomhedens driftsomkostninger. Den omfatter rapportering af produktionsomkostninger og lageromkostninger, dvs. værdien af varer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5e6b691eae1663cdc93d851f531306c472291484
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="about-inventory-costing"></a><span data-ttu-id="ebc0e-104">Om lagerkostmetode</span><span class="sxs-lookup"><span data-stu-id="ebc0e-104">About Inventory Costing</span></span>
<span data-ttu-id="ebc0e-105">Administration af lagerkostmetoder vedrører registrering og rapportering af virksomhedens driftsomkostninger.</span><span class="sxs-lookup"><span data-stu-id="ebc0e-105">Managing inventory costs is concerned with recording and reporting business operating costs.</span></span> <span data-ttu-id="ebc0e-106">Den omfatter rapportering af produktionsomkostninger og lageromkostninger, dvs. værdien af varer.</span><span class="sxs-lookup"><span data-stu-id="ebc0e-106">It includes the reporting of manufacturing costs and inventory costs, that is, the value of items.</span></span>  

 <span data-ttu-id="ebc0e-107">De centrale principper, der er vigtige at forstå, er, at kostmetoder definerer den måde, varer værdiansættes på, når de forlader lageret, at kostregulering opdaterer omkostningerne ved solgte varer med relaterede købsomkostninger bogført efter salget, og at lagerværdier skal bogføres til dedikerede finanskonti med regelmæssige mellemrum.</span><span class="sxs-lookup"><span data-stu-id="ebc0e-107">Central principles to understand are that costing methods define how items are valued when they leave inventory, that cost adjustment updates the cost of goods sold with related purchase costs posted after the sale, and that inventory values must be posted to dedicated G/L accounts at regular intervals.</span></span>  

 <span data-ttu-id="ebc0e-108">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="ebc0e-108">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="ebc0e-109">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="ebc0e-109">**To**</span></span>|<span data-ttu-id="ebc0e-110">**Se**</span><span class="sxs-lookup"><span data-stu-id="ebc0e-110">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="ebc0e-111">Kunne skelne mellem de fem forskellige prisberegningsmetoder og deres virkning på omkostningsforløb.</span><span class="sxs-lookup"><span data-stu-id="ebc0e-111">Distinguish the five different costing methods and their effect on cost flows.</span></span>|[<span data-ttu-id="ebc0e-112">Designoplysninger: Kostmetoder</span><span class="sxs-lookup"><span data-stu-id="ebc0e-112">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)|  
|<span data-ttu-id="ebc0e-113">Lære, hvordan vareudligningsposter dynamisk sammenkæder lagerafgange med tilgange for at bevare kontrollen med omkostningsforløb.</span><span class="sxs-lookup"><span data-stu-id="ebc0e-113">Learn how item application entries dynamically link inventory decreases with increases to keep control of cost flows.</span></span>|[<span data-ttu-id="ebc0e-114">Designoplysninger: Vareudligning</span><span class="sxs-lookup"><span data-stu-id="ebc0e-114">Design Details: Item Application</span></span>](design-details-item-application.md)|  
|<span data-ttu-id="ebc0e-115">Lære, hvordan en vares købspris fortsat opdateres med omkostningerne ved de seneste transaktioner i overensstemmelse med prisberegningsmetoden for varen.</span><span class="sxs-lookup"><span data-stu-id="ebc0e-115">Learn how an item's unit cost is continuously updated with the cost of its latest transaction according to the item's costing method.</span></span>|[<span data-ttu-id="ebc0e-116">Designoplysninger: Omkostningsregulering</span><span class="sxs-lookup"><span data-stu-id="ebc0e-116">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)|  
|<span data-ttu-id="ebc0e-117">Lære, hvordan gennemsnitsomkostningerne for en vare beregnes dynamisk i overensstemmelse med den valgte gennemsnitlige omkostningsperiode.</span><span class="sxs-lookup"><span data-stu-id="ebc0e-117">Learn how an item's average cost is dynamically calculated according to the selected average cost period.</span></span>|[<span data-ttu-id="ebc0e-118">Designoplysninger: Gennemsnitlig kostpris</span><span class="sxs-lookup"><span data-stu-id="ebc0e-118">Design Details: Average Cost</span></span>](design-details-average-cost.md)|  
|<span data-ttu-id="ebc0e-119">Kunne skelne forventede omkostninger (endnu ikke faktureret) fra faktiske omkostninger og lære, hvordan de håndteres i finansposterne.</span><span class="sxs-lookup"><span data-stu-id="ebc0e-119">Distinguish expected cost (not yet invoiced) from actual cost and learn how it is managed in the general ledger.</span></span>|[<span data-ttu-id="ebc0e-120">Designoplysninger: Bogføring af forventet kostpris</span><span class="sxs-lookup"><span data-stu-id="ebc0e-120">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)|  
|<span data-ttu-id="ebc0e-121">Forstå omkostningsreguleringsmekanismen, som sikrer, at omkostningerne sendes videre, selvom lagertransaktioner forekommer med uregelmæssige mellemrum.</span><span class="sxs-lookup"><span data-stu-id="ebc0e-121">Understand the cost adjustment mechanism, which ensures that costs are brought forward even if inventory transactions happen in a random manner.</span></span>|[<span data-ttu-id="ebc0e-122">Designoplysninger: Omkostningsregulering</span><span class="sxs-lookup"><span data-stu-id="ebc0e-122">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)|  
|<span data-ttu-id="ebc0e-123">Læse om årsagen til, at standardomkostninger ofte bruges af produktionsvirksomheder som værdigrundlag for komponenter og varer.</span><span class="sxs-lookup"><span data-stu-id="ebc0e-123">Read why standard costs are often used by manufacturing companies as a valuation base for components and end items.</span></span>|[<span data-ttu-id="ebc0e-124">Om beregning af standardomkostning</span><span class="sxs-lookup"><span data-stu-id="ebc0e-124">About Calculating Standard Cost</span></span>](finance-about-calculating-standard-cost.md)|  
|<span data-ttu-id="ebc0e-125">Forstå, hvordan værdien af lageret afspejles i finansposterne.</span><span class="sxs-lookup"><span data-stu-id="ebc0e-125">Understand how the value of inventory is reflected in the general ledger.</span></span>|[<span data-ttu-id="ebc0e-126">Rapportere omkostninger og afstemme med regnskabet</span><span class="sxs-lookup"><span data-stu-id="ebc0e-126">Reporting Costs and Reconciling with the General Ledger</span></span>](finance-report-costs-and-reconcile-with-the-general-ledger.md)|  
|<span data-ttu-id="ebc0e-127">Lære, hvordan varegebyrer, f.eks. for fragt og forsikring, kan føje ekstra omkostningskomponenter til en vares enhedspris.</span><span class="sxs-lookup"><span data-stu-id="ebc0e-127">Learn how item charges, such as freight and insurance, can assign additional cost components to an item's unit cost.</span></span>|[<span data-ttu-id="ebc0e-128">Fremgangsmåde: Bruge varegebyrer til at angive ekstra handelsomkostninger</span><span class="sxs-lookup"><span data-stu-id="ebc0e-128">How to: Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)|  
|<span data-ttu-id="ebc0e-129">Læse, hvordan lagerperioder hjælper en virksomhed med at styre lagerværdi over tid, hvis der defineres kortere perioder, hvor der kan være lukket for bogføringer, efterhånden som regnskabsåret skrider frem.</span><span class="sxs-lookup"><span data-stu-id="ebc0e-129">Read how inventory periods help a company to control inventory value over time by defining shorter periods that can be closed for posting as the fiscal year progresses.</span></span>|[<span data-ttu-id="ebc0e-130">Sådan gør du: Arbejde med lagerperioder</span><span class="sxs-lookup"><span data-stu-id="ebc0e-130">How to: Work with Inventory Periods</span></span>](finance-how-to-work-with-inventory-periods.md)|  
|<span data-ttu-id="ebc0e-131">Forstå alle mekanismerne i prisberegningsprogrammet, herunder hvad der sker, når du bogfører montage og produktionstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="ebc0e-131">Understand all mechanisms in the costing engine, including what happens when you post assembly and production transactions.</span></span>|[<span data-ttu-id="ebc0e-132">Designoplysninger: Lagerkostmetode</span><span class="sxs-lookup"><span data-stu-id="ebc0e-132">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)|

## <a name="see-also"></a><span data-ttu-id="ebc0e-133">Se også</span><span class="sxs-lookup"><span data-stu-id="ebc0e-133">See Also</span></span>
<span data-ttu-id="ebc0e-134">[Administrere lageromkostninger](finance-manage-inventory-costs.md)  </span><span class="sxs-lookup"><span data-stu-id="ebc0e-134">[Managing Inventory Costs](finance-manage-inventory-costs.md)  </span></span>  
<span data-ttu-id="ebc0e-135">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ebc0e-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
