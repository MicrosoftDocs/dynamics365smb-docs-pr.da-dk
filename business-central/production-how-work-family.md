---
title: "Sådan bruges varefamilier i produktionen | Microsoft Docs"
description: "Den vigtigste opgave i forbindelse med tilpasning af en basiskalender for din virksomhed eller en samarbejdspartner, er at angive eventuelle ændringer i statussen for arbejdsdage eller fridage."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/05/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 51c505decb595f1da3aba61a73a1f2a55608fc22
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-production-families"></a>Arbejde med produktionsfamilier
En produktfamilie er en gruppe individuelle varer, hvis slægtskab er baseret på lighedspunkter i fremstillingsprocesserne. Ved hjælp af produktionsfamilier kan visse varer forarbejdes to eller flere gange i samme proces, hvilket optimerer materialeforbruget.

I feltet **Antal** i vinduet **Familie** skal du angive det antal, der er produceret, når hele familien er produceret én gang.

## <a name="example"></a>Eksempel
Ved en udstansning kan fire stk. af samme vare produceres fra et emne og ti stk. af en anden vare samtidig. Stansemaskinen vil udstanse alle 14 stykker i en arbejdsgang.

Ved at oprette produktionsfamilier reduceres spildantallet, fordi det, der normalt ville være tilovers som spild ved produktion af store stykker, i stedet kan benyttes til at producere små stykker.

## <a name="to-set-up-a-production-family"></a>Sådan oprettes en produktionsfamilie
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Familier**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-familily"></a>Sådan produceres på basis af en produktionsfamilie
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ordreplanlægning**, og vælg derefter det relaterede link.
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
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

