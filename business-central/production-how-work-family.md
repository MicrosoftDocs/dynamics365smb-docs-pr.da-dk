---
title: Sådan bruges varefamilier i produktionen | Microsoft Docs
description: Den vigtigste opgave i forbindelse med tilpasning af en basiskalender for din virksomhed eller en samarbejdspartner, er at angive eventuelle ændringer i statussen for arbejdsdage eller fridage.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f33ac3e581325eb714af67ee7040157a61e59fc7
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758863"
---
# <a name="work-with-production-families"></a>Arbejde med produktionsfamilier
En produktfamilie er en gruppe individuelle varer, hvis slægtskab er baseret på lighedspunkter i fremstillingsprocesserne. Ved hjælp af produktionsfamilier kan visse varer forarbejdes to eller flere gange i samme proces, hvilket optimerer materialeforbruget.

I feltet **Antal** på siden **Familie** skal du angive det antal, der er produceret, når hele familien er produceret én gang.

## <a name="example"></a>Eksempel
Ved en udstansning kan fire stk. af samme vare produceres fra et emne og ti stk. af en anden vare samtidig. Stansemaskinen vil udstanse alle 14 stykker i en arbejdsgang.

Ved at oprette produktionsfamilier reduceres spildantallet, fordi det, der normalt ville være tilovers som spild ved produktion af store stykker, i stedet kan benyttes til at producere små stykker.

## <a name="to-set-up-a-production-family"></a>Sådan oprettes en produktionsfamilie
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Familier**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-family"></a>Sådan produceres på basis af en produktionsfamilie
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Fastlagt produktionsordrer**, og vælg derefter det relaterede link.
2. Opret et ny produktionsordre. Du kan finde flere oplysninger i [Oprette produktionsordrer](production-how-to-create-production-orders.md).
3. Vælg **Familie** i feltet **Kildetype**.  
4. Vælg den relevante produktionsfamilie i feltet **Kildenr.**.

## <a name="see-also"></a>Se også
[Oprette produktionsstyklister](production-how-to-create-production-boms.md)  
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Planlægning](production-planning.md)   
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]