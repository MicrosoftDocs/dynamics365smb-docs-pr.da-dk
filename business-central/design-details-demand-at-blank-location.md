---
title: "Designoplysninger – Behov og forsyning | Microsoft Docs"
description: "I dette emne introduceres begrebet behov, der er fællesbetegnelsen for enhver form for bruttobehov, som f.eks. en salgsordre og et komponentbehov fra en produktionsordre."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8cf7ffe90ccaf32258b4a51fb12f93a8df8ba7eb
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-demand-and-supply"></a><span data-ttu-id="cff99-103">Designoplysninger: Behov og forsyning</span><span class="sxs-lookup"><span data-stu-id="cff99-103">Design Details: Demand and Supply</span></span>
<span data-ttu-id="cff99-104">Behov er fællesbetegnelsen for enhver form for bruttobehov, som f.eks. en salgsordre og et komponentbehov fra en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="cff99-104">Demand is the common term used for any kind of gross demand, such as a sales order and component need from a production order.</span></span> <span data-ttu-id="cff99-105">Programmet giver desuden mulighed for mere tekniske typer behov som negativ lagerbeholdning og købsreturvarer.</span><span class="sxs-lookup"><span data-stu-id="cff99-105">In addition, the program allows more technical types of demand, such as negative inventory and purchase returns.</span></span>  
  
<span data-ttu-id="cff99-106">Forsyning er fællesbetegnelsen for enhver form for positiv eller indgående mængde, f.eks. lagerbeholdning, køb, montage, produktion eller indgående overførsler.</span><span class="sxs-lookup"><span data-stu-id="cff99-106">Supply is the common term used for any kind of positive or inbound quantity, such as inventory, purchases, assembly, production, or inbound transfers.</span></span> <span data-ttu-id="cff99-107">Desuden kan en salgsreturvare også repræsentere forsyning.</span><span class="sxs-lookup"><span data-stu-id="cff99-107">In addition, a sales return may also represent supply.</span></span>  
  
<span data-ttu-id="cff99-108">Planlægningssystemet organiserer de mange kilder for behov og forsyning på to tidslinjer, der kaldes lagerprofiler, for at få dem sorteret.</span><span class="sxs-lookup"><span data-stu-id="cff99-108">To sort out the many sources of demand and supply, the planning system organizes them on two time lines called inventory profiles.</span></span> <span data-ttu-id="cff99-109">En profil indeholder efterspørgsler, og den anden indeholder de tilsvarende forsyningshændelser.</span><span class="sxs-lookup"><span data-stu-id="cff99-109">One profile holds demand events, and the other holds the corresponding supply events.</span></span> <span data-ttu-id="cff99-110">Hver hændelse repræsenterer én ordrenetværksenhed, f.eks. en salgsordrelinje, en varepost eller en produktionsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="cff99-110">Each event represents one order network entity, such as a sales order line, an item ledger entry, or a production order line.</span></span>  
  
<span data-ttu-id="cff99-111">Når lagerprofiler er indlæst, afstemmes de forskellige behov-forsyningssæt for at fremstille en forsyningsplan, der opfylder de angivne mål.</span><span class="sxs-lookup"><span data-stu-id="cff99-111">When inventory profiles are loaded, the different demand-supply sets are balanced to output a supply plan that fulfills the listed goals.</span></span>  
  
<span data-ttu-id="cff99-112">Planlægningsparametre og lagerbeholdninger er andre typer af behov og forsyning, som underkastes integreret justering for at genbestille lagervarer.</span><span class="sxs-lookup"><span data-stu-id="cff99-112">Planning parameters and inventory levels are other types of demand and supply respectively, which undergo integrated balancing to replenish stock items.</span></span> <span data-ttu-id="cff99-113">Du kan finde flere oplysninger i [Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md).</span><span class="sxs-lookup"><span data-stu-id="cff99-113">For more information, see [Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cff99-114">Se også</span><span class="sxs-lookup"><span data-stu-id="cff99-114">See Also</span></span>  
<span data-ttu-id="cff99-115">[Designoplysninger: Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="cff99-115">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="cff99-116">[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="cff99-116">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="cff99-117">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="cff99-117">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
