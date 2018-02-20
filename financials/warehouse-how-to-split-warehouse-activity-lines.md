---
title: "Sådan opdeles lageraktivitetslinjer | Microsoft Docs"
description: "I læg-på-lager-aktiviteter, bevægelser eller pluk (logistik) og i læg-på-lager-aktiviteter og pluk (lager) foreslås der automatisk placeringer for varer, der plukkes eller lægges på lager. Den faktiske mængde på den foreslåede placering er muligvis ikke tilstrækkelig, eller at der ikke er nok plads på den foreslåede placering til at lægge den ønskede bestilte mængde på lager. I begge tilfælde skal du opdele linjen, så varerne for én linje enten hentes fra eller anbringes på mere end én placering."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: eee1145aaf72092d93eb9236ca065db221b85dc3
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="split-warehouse-activity-lines"></a>Opdele lageraktivitetslinjer
I læg-på-lager-aktiviteter, bevægelser eller pluk (logistik) og i læg-på-lager-aktiviteter og pluk (lager) foreslås der automatisk placeringer for varer, der plukkes eller lægges på lager. Den faktiske mængde på den foreslåede placering er muligvis ikke tilstrækkelig, eller at der ikke er nok plads på den foreslåede placering til at lægge den ønskede bestilte mængde på lager. I begge tilfælde skal du opdele linjen, så varerne for én linje enten hentes fra eller anbringes på mere end én placering.  

Følgende fremgangsmåde gælder for lagerdokumenter som f.eks. læg-på-lager (logistik), bevægelse og pluklinjer eller læg-på-lager (lager), bevægelse og pluklinjer.  

## <a name="to-split-warehouse-activity-lines"></a>Sådan opdeles lageraktivitetslinjer  
1.  Åbn en lageraktivitetslinje, hvor du forsøger at håndtere en utilstrækkelig mængde.  
2.  I feltet **Håndteringsantal** skal du angive det reducerede antal, som du er i stand til at håndtere.  
3.  I oversigtspanelet **Linjer** skal du vælge handlingen **Handlinger**, vælge handlingen **Funktioner** og derefter vælge handlingen **Opdel linje**. Der vises en ny linje, som er en kopi af den oprindelige linje, bortset fra at feltet **Håndteringsantal** indeholder det antal, du har fjernet fra den oprindelige linje.  
4.  Tildel en relevant placering, og hvis der anvendes styret læg-på-lager og pluk, en zone til denne nye linje, eller fortsæt med at opdele linjen efter behov, indtil du finder de rette placeringer for alle antallene.  

> [!NOTE]  
>  Hvis lokationen bruger styret læg-på-lager og pluk, og du opdeler linjerne, skal du være godt kendt med lagerstedet og i stand til at vælge en placering, som passer med opbevaringskravene til varen og opfylder de generelle krav for lagerdokumentet. Det er f.eks. ikke nogen god idé at opdele en linje på et plukdokument og placere nogle af varerne i massevarelageret.  

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

