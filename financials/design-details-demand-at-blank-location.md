---
title: "Designoplysninger – Behov og forsyning | Microsoft Docs"
description: "I dette emne introduceres begrebet behov, der er fællesbetegnelsen for enhver form for bruttobehov, som f.eks. en salgsordre og et komponentbehov fra en produktionsordre."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 69d5e574b390fe50490ff98616983a5e9ea31d94
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-demand-and-supply"></a>Designoplysninger: Behov og forsyning
Behov er fællesbetegnelsen for enhver form for bruttobehov, som f.eks. en salgsordre og et komponentbehov fra en produktionsordre. Programmet giver desuden mulighed for mere tekniske typer behov som negativ lagerbeholdning og købsreturvarer.  
  
Forsyning er fællesbetegnelsen for enhver form for positiv eller indgående mængde, f.eks. lagerbeholdning, køb, montage, produktion eller indgående overførsler. Desuden kan en salgsreturvare også repræsentere forsyning.  
  
Planlægningssystemet organiserer de mange kilder for behov og forsyning på to tidslinjer, der kaldes lagerprofiler, for at få dem sorteret. En profil indeholder efterspørgsler, og den anden indeholder de tilsvarende forsyningshændelser. Hver hændelse repræsenterer én ordrenetværksenhed, f.eks. en salgsordrelinje, en varepost eller en produktionsordrelinje.  
  
Når lagerprofiler er indlæst, afstemmes de forskellige behov-forsyningssæt for at fremstille en forsyningsplan, der opfylder de angivne mål.  
  
Planlægningsparametre og lagerbeholdninger er andre typer af behov og forsyning, som underkastes integreret justering for at genbestille lagervarer. Du kan finde flere oplysninger i [Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md).  
  
## <a name="see-also"></a>Se også  
[Designoplysninger: Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md)   
[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)
