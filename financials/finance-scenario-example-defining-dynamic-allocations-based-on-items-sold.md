---
title: "Scenarieeksempel - Definition af dynamiske fordelinger baseret på solgte varer | Microsoft Docs"
description: "I dette emne vises et eksempel på, hvordan du definerer allokeringer ved hjælp af metoden til dynamisk fordeling."
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
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: d87e01cb987a019c6e71b50dcdeae55dc0375146
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="scenario-example-defining-dynamic-allocations-based-on-items-sold"></a>Scenarieeksempel: Definition af dynamiske fordelinger baseret på solgte varer
I dette emne vises et eksempel på, hvordan du definerer allokeringer ved hjælp af metoden til dynamisk fordeling. I dette eksempel skal du ændre dynamisk fordeling af omkostningerne for omkostningsstedet SALES til understøttelse af det nye omkostningsobjekt IT-UDSTYR. IT_UDSTYR-pakker har varenumre i området fra 8904-W til 8924-W. Du bruger salgstal for det foregående år til at beregne det andelen. Allokeringen bogføres til hjælpeomkostningstypen 9903.  

> [!NOTE]  
>  I eksemplet bruges demonstrationsdataene i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a>Sådan defineres dynamiske fordelinger baseret på varer, der er solgt i det foregående år  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Omkostningsfordelinger**, og vælg derefter det relaterede link.  
2.  I vinduet **Omkostningsfordeling** skal du vælge handlingen **Ny**.  
3.  I feltet **Id** skal du trykke på Enter eller indtaste et id.  
4.  Angiv **1** i feltet **Niveau**.  
5.  I felterne **Gyldig fra** og **Gyldig til** skal du angive relevante datoer.  
6.  I feltet **Omkostningsstedskode** skal du angive **SALG**.  
7.  Angiv omkostningstypen **9903** i feltet **Kredit til omkostningstype**.  
8.  Angiv omkostningstypen **9903** i feltet **Målomkostningstype**.  
9. I feltet **Målomkostningstype** skal du vælge **Ny** for at oprette et nyt omkostningsobjekt IT-UDSTYR og udfylde felter efter behov. Vælg **IT-UDSTYR**. Lad feltet **Målomkostningssted** stå tomt.  
10. I feltet **Fordelingsmåltype** skal du vælge **Alle omkostninger** for at definere, hvordan alle akkumulerede omkostninger allokeres.  
11. I feltet **Basis** skal du vælge fordelingsbasen **Varer solgt (beløb)**.  
12. I feltet **Nummerfilter** skal du angive **8904-W..8924-W**.  
13. I feltet **Datofilterkode** skal du angive **Sidste år**.  
14. Vælg handlingen **Beregn fordelingsnøgle** for at beregne det andelen.  

    > [!IMPORTANT]  
    >  [!INCLUDE[d365fin](includes/d365fin_md.md)] bruger salgstal fra de foregående år til at beregne andelen af 1596,50 RV med 100 procent for IT-UDSTYR-pakkerne. Det betyder, at alle varer, der er solgt sidste år, tildeles omkostningsobjektet IT-UDSTYR.  

## <a name="see-also"></a>Se også  
 [Indstilling af filtre for dynamiske allokeringsbaser](finance-setting-filters-for-dynamic-allocation-bases.md)   
 [Fremgangsmåde: Konfigurere fordelingskilde og -mål](finance-how-to-set-up-allocation-source-and-targets.md)   
 [Definere og allokere omkostninger](finance-define-and-allocate-costs.md)   
 [Terminologi i omkostningsregnskab](finance-terminology-in-cost-accounting.md)   
 [Om omkostningsregnskab](finance-about-cost-accounting.md)

