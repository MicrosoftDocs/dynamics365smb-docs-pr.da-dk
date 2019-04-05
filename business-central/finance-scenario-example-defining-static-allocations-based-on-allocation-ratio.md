---
title: Definition af statisk allokeringer baseret på fordelingsforholdet | Microsoft Docs
description: 'Metoden statisk allokering er baseret på en endelig værdi, for eksempel anvendt antal kvadratmeter eller et etableret fordelingsforhold såsom 5: 2: 4.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: d35fd5de7a0583c3864268d0749384322bf947ed
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "793307"
---
# <a name="scenario-example-defining-static-allocations-based-on-allocation-ratio"></a>Scenarieeksempel: Definition af statisk allokeringer baseret på fordelingsforholdet
Metoden statisk allokering er baseret på en endelig værdi, for eksempel anvendt antal kvadratmeter eller et etableret fordelingsforhold såsom 5: 2: 4.  

Dette emne beskriver, hvordan du definerer tre nye fordelingsmålsomkostningsobjekter til fordelingskilden PROD-omkostningssted ved hjælp af det etablerede fordelingsforhold 5:2:4. De tre målomkostningsobjekter er ACCESSO, PAINT og FITTINGS.  

> [!NOTE]  
>  I eksemplet bruges demonstrationsdataene i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a>Sådan defineres fordelingskilden PROD-omkostningssted på oversigtspanelet Generelt  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Omkostningsfordeling**, og vælg derefter det relaterede link.  
2.  På siden **Omkostningsfordeling** skal du vælge handlingen **Ny**.  
3.  I feltet **Id** skal du trykke på Enter eller indtaste et id.  
4.  Angiv **1** i feltet **Niveau**.  
5.  I felterne **Gyldig fra** og **Gyldig til** skal du angive relevante datoer.  
6.  I feltet **Omkostningsstedskode** skal du angive **PROD**.  
7.  Angiv omkostningstypen **9903** i feltet **Kredit til omkostningstype**.  

## <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a>Sådan angives fordelingsmålsomkostningsobjekter på oversigtspanelet Linjer  

1.  Angiv **9903** i feltet **Målomkostningstype** på den første linje.  
2.  Vælg **TILBEHØR** i feltet **Målomkostningstype** på den første linje.  
3.  På den første linje i feltet **Fordelingsmåltype** skal du vælge **Alle omkostninger** for at definere, hvordan alle påløbne omkostninger allokeres.  
4.  På den første linje i feltet **Basis** skal du vælge **Statisk** for at bruge den statiske allokeringsmetode.  
5.  På den første linje i feltet **Fordeling** skal du angive fordelingsforholdet **5**.  
6.  Angiv **9903** i feltet **Målomkostningstype** på den anden linje.  
7.  Vælg **MALING** i feltet **Målomkostningsemne** på den anden linje.  
8.  På den anden linje i feltet **Fordelingsmåltype** skal du vælge **Alle omkostninger** for at definere, hvordan alle påløbne omkostninger allokeres.  
9. På den anden linje i feltet **Basis** skal du vælge **Statisk** for at bruge den statiske allokeringsmetode.  
10. På den anden linje i feltet **Fordeling** skal du angive fordelingsforholdet **2**.  
11. Angiv **9903** i feltet **Målomkostningstype** på den tredje linje.  
12. Vælg **BESLAG** i feltet **Målomkostningsemne** på den første linje.  
13. På den tredje linje i feltet **Fordelingsmåltype** skal du vælge **Alle omkostninger** for at definere, hvordan alle påløbne omkostninger allokeres.  
14. På den tredje linje i feltet **Basis** skal du vælge **Statisk** for at bruge den statiske allokeringsmetode.  
15. På den tredje linje i feltet **Fordeling** skal du angive fordelingsforholdet **4**.  

> [!IMPORTANT]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)] beregner automatisk feltet **Procent** ved hjælp af en procentsats , der er afhængig af alle tre fordelingsforhold, der er angivet i feltet **Fordeling** for alle tre linjer.  

## <a name="see-also"></a>Se også  
[Definere og allokere omkostninger](finance-define-and-allocate-costs.md)   
