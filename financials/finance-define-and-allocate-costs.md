---
title: Definere og allokere omkostninger | Microsoft Docs
description: "Allokering af omkostninger flytter omkostninger og indtægter mellem omkostningstyper, omkostningssteder og omkostningsobjekter. Du kan angive så mange tildelinger, som du har brug for."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 04e5a95b7a926528cc26c254390d08e3bce6ad8a
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="defining-and-allocating-costs"></a>Definere og allokere omkostninger
Allokering af omkostninger flytter omkostninger og indtægter mellem omkostningstyper, omkostningssteder og omkostningsobjekter. Du kan angive så mange tildelinger, som du har brug for. Hver allokering består af:  

-   En fordelingskilde.  
-   Et eller flere allokeringsmål.  

Fordelingskilden fastlægger, hvilke omkostninger der skal fordeles, og allokeringsmål bestemmer, hvor omkostningerne skal fordeles til. F.eks. kan en fordelingskilde være omkostningerne for omkostningstypen Elektricitet og varme. Du allokerer alle el- og varmeomkostninger til tre omkostningssteder: Workshop, produktion og salg. Disse omkostningssteder er dine fordelingsmål.  

For hver fordelingskilde skal du definere et fordelingsniveau, en gyldighedsperiode og en variant som gruppe-id. Du kan bruge et batchjob til at angive filtre til valg af allokeringsdefinitioner og derefter køre allokering af omkostninger automatisk.  

Du kan definere en fordelingsbasis for hvert fordelingsmål. Fordelingsbasis kan være enten statisk eller dynamisk.  

-   Statisk allokeringsbasis er baseret på en endelig værdi, for eksempel anvendt antal kvadratmeter eller et etableret fordelingsforhold såsom 5:2:4.  
-   Dynamisk fordelingsbasis afhænger af værdier, der kan ændres, f.eks antallet af medarbejdere på et omkostningssted eller salgsindtægter fra et omkostningsobjekt i en bestemt tidsperiode.  

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.

|Til|Se|  
|--------|---------|  
|Konfigurer fordelingskilde og dens mål.|[Konfigurere fordelingskilde og mål](finance-how-to-set-up-allocation-source-and-targets.md)|  
|Konfigurer forskellige filtre for dynamiske fordelingsbaser.|[Indstilling af filtre for dynamiske allokeringsbaser](finance-setting-filters-for-dynamic-allocation-bases.md)|  
|Se et eksempel på, hvordan du definerer en statisk allokering.|[Scenarieeksempel: Definition af statisk allokeringer baseret på fordelingsforholdet](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)|  
|Se et eksempel på, hvordan du definerer en dynamisk fordeling.|[Scenarieeksempel: Definition af dynamiske fordelinger baseret på solgte varer](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)|  

## <a name="see-also"></a>Se også  
 [Konfigurere omkostningsregnskab](finance-set-up-cost-accounting.md)   
 [Overførsel og bogføring af omkostningsposter](finance-transfer-and-post-cost-entries.md)   
 [Regnskab for omkostninger](finance-manage-cost-accounting.md)   
 [Terminologi i omkostningsregnskab](finance-terminology-in-cost-accounting.md)   
 [Om omkostningsregnskab](finance-about-cost-accounting.md)

