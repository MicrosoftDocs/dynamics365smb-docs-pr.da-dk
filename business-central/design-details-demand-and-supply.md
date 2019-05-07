---
title: Designoplysninger – Behov og forsyning | Microsoft Docs
description: Behov er fællesbetegnelsen for enhver form for bruttobehov, som f.eks. en salgsordre og et komponentbehov fra en produktionsordre. Programmet giver desuden mulighed for mere tekniske typer behov som negativ lagerbeholdning og købsreturvarer.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: c26e74cb2a362339b1e7c95809fb19e13869c61e
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "924659"
---
# <a name="design-details-demand-and-supply"></a><span data-ttu-id="0b55e-104">Designoplysninger: Behov og forsyning</span><span class="sxs-lookup"><span data-stu-id="0b55e-104">Design Details: Demand and Supply</span></span>
<span data-ttu-id="0b55e-105">Behov er fællesbetegnelsen for enhver form for bruttobehov, som f.eks. en salgsordre og et komponentbehov fra en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="0b55e-105">Demand is the common term used for any kind of gross demand, such as a sales order and component need from a production order.</span></span> <span data-ttu-id="0b55e-106">Programmet giver desuden mulighed for mere tekniske typer behov som negativ lagerbeholdning og købsreturvarer.</span><span class="sxs-lookup"><span data-stu-id="0b55e-106">In addition, the program allows more technical types of demand, such as negative inventory and purchase returns.</span></span>  

 <span data-ttu-id="0b55e-107">Forsyning er fællesbetegnelsen for enhver form for positiv eller indgående mængde, f.eks. lagerbeholdning, køb, montage, produktion eller indgående overførsler.</span><span class="sxs-lookup"><span data-stu-id="0b55e-107">Supply is the common term used for any kind of positive or inbound quantity, such as inventory, purchases, assembly, production, or inbound transfers.</span></span> <span data-ttu-id="0b55e-108">Desuden kan en salgsreturvare også repræsentere forsyning.</span><span class="sxs-lookup"><span data-stu-id="0b55e-108">In addition, a sales return may also represent supply.</span></span>  

 <span data-ttu-id="0b55e-109">Planlægningssystemet organiserer de mange kilder for behov og forsyning på to tidslinjer, der kaldes lagerprofiler, for at få dem sorteret.</span><span class="sxs-lookup"><span data-stu-id="0b55e-109">To sort out the many sources of demand and supply, the planning system organizes them on two time lines called inventory profiles.</span></span> <span data-ttu-id="0b55e-110">En profil indeholder efterspørgsler, og den anden indeholder de tilsvarende forsyningshændelser.</span><span class="sxs-lookup"><span data-stu-id="0b55e-110">One profile holds demand events, and the other holds the corresponding supply events.</span></span> <span data-ttu-id="0b55e-111">Hver hændelse repræsenterer én ordrenetværksenhed, f.eks. en salgsordrelinje, en varepost eller en produktionsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="0b55e-111">Each event represents one order network entity, such as a sales order line, an item ledger entry, or a production order line.</span></span>  

 <span data-ttu-id="0b55e-112">Når lagerprofiler er indlæst, afstemmes de forskellige behov-forsyningssæt for at fremstille en forsyningsplan, der opfylder de angivne mål.</span><span class="sxs-lookup"><span data-stu-id="0b55e-112">When inventory profiles are loaded, the different demand-supply sets are balanced to output a supply plan that fulfills the listed goals.</span></span>  

 <span data-ttu-id="0b55e-113">Planlægningsparametre og lagerbeholdninger er andre typer af behov og forsyning, som underkastes integreret justering for at genbestille lagervarer.</span><span class="sxs-lookup"><span data-stu-id="0b55e-113">Planning parameters and inventory levels are other types of demand and supply respectively, which undergo integrated balancing to replenish stock items.</span></span> <span data-ttu-id="0b55e-114">Du kan finde flere oplysninger i [Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md).</span><span class="sxs-lookup"><span data-stu-id="0b55e-114">For more information, see [Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="0b55e-115">Se også</span><span class="sxs-lookup"><span data-stu-id="0b55e-115">See Also</span></span>  
 <span data-ttu-id="0b55e-116">[Designoplysninger: Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="0b55e-116">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
 <span data-ttu-id="0b55e-117">[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="0b55e-117">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 [<span data-ttu-id="0b55e-118">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="0b55e-118">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
