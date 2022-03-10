---
title: 'Fremgangsmåde: Opdele lageraktivitetslinjer'
description: Læs, hvordan du opdeler lageraktivitetslinjer, hvis den disponible kapacitet på en foreslået placering ikke er tilstrækkelig.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: b7a035fd6ac2b2af6e7ceb4db63edfa66531848d
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8134587"
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
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Warehouse Management](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]