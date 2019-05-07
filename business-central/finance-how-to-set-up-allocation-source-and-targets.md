---
title: Sådan konfigureres fordelingskilde og -mål | Microsoft Docs
description: Hver allokering, der består af en fordelingskilde og mål for en eller flere fordelinger. Fordelingskilden definerer, hvilke omkostninger, der vil blive tildelt. Fordelingsmålet bestemmer, hvortil omkostningerne fordeles.
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
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: 2e8040816ed5089188f06f76b2cd8f027ba83766
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "929764"
---
# <a name="set-up-allocation-source-and-targets"></a>Konfigurere fordelingskilde og mål
Hver allokering består af en fordelingskilde og en eller flere fordelingsmål. Fordelingskilden definerer, hvilke omkostninger, der vil blive tildelt. Fordelingsmålet bestemmer, hvortil omkostningerne fordeles.  

## <a name="to-set-up-cost-allocations"></a>Opsætning af omkostningsfordelinger  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Omkostningsfordeling**, og vælg derefter det relaterede link.  
2.  På siden **Omkostningsfordeling** skal du vælge handlingen **Rediger**.  
3.  Angiv et id for fordelingskilden i feltet **Id**.  
4.  Definer et niveau som et tal mellem 1 og 99 i feltet **Niveau**. Fordelingsbogføringen følger niveauernes rækkefølge.  
5.  Angiv en pristype for at definere, hvilken pris der skal fordeles, i feltet **Omkostningstypeinterval**. Hvis alle omkostninger for en pristype fordeles, defineres der intet område.  
6.  Angiv et omkostningssted sammen med de omkostninger, der skal allokeres, i feltet **Omkostningsstedskode**.  
7.  Angiv et omkostningsemne sammen med de omkostninger, der skal allokeres, i feltet **Omkostningsstedskode**. Feltet forbliver oftest tomt, da der sjældent allokeres omkostningsobjekter til andre omkostningsobjekter.  
8.  Angiv en omkostningstype i feltet **Kredit til omkostningstype**. Omkostningerne, der fordeles, krediteres til kildeomkostningstypen. Kreditnotaen bogføres til den omkostningstype, der er angivet her.  
9. Definer fordelingsmålene på oversigtspanelet **Linjer**. Angiv en omkostningstype på første linje i feltet **Målomkostningstype**. Den definerer, hvilken pristype fordelingen fordeles til.  
10. På den første linje, skal du angive første fordelingsmål i feltet **Målomkostningssted** eller feltet **Målomkostningsemne**. Disse to felter definere, hvilket omkostningssted eller omkostningsobjekt fordeling debiteres til. Du kan kun udfylde et disse felter, ikke begge.  
11. Gentag de samme trin på den anden linje for at angive yderligere fordelingsmål.  
12. Når du har angivet fordelingsmål og -kilder, skal du vælge handlingen **Beregn fordelingsnøgle** for at beregne de samlede fordelingsværdier.  

> [!NOTE]  
>  Vælg afkrydsningsfeltet **Spærret** for at deaktivere fordelingsopsætningen.  

## <a name="see-also"></a>Se også  
[Regnskab for omkostninger](finance-manage-cost-accounting.md)  
 [Indstilling af filtre for dynamiske allokeringsbaser](finance-setting-filters-for-dynamic-allocation-bases.md)   
 [Scenarieeksempel: Definition af statisk allokeringer baseret på fordelingsforholdet](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)   
 [Scenarieeksempel: Definition af dynamiske fordelinger baseret på solgte varer](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)   
 [Definere og allokere omkostninger](finance-define-and-allocate-costs.md)   
 [Terminologi i omkostningsregnskab](finance-terminology-in-cost-accounting.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
