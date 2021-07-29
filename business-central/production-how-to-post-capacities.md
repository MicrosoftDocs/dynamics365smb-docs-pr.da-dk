---
title: 'Fremgangsmåde: Bogføre kapaciteter'
description: Bogfør forbrugt kapacitet, der ikke er knyttet til produktionsordren i kapacitetskladden, og få vist bogførte kapaciteter på siden kapacitetsposter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: 024985cb4a2615f374465e5a387901976509a5db
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6444201"
---
# <a name="post-capacities"></a>Bogføre kapaciteter
I kapacitetskladden kan du bogføre forbrugt kapacitet, der ikke er knyttet til produktionsordren. Vedligeholdelsesarbejde skal f.eks. knyttes til kapaciteten, men ikke til en produktionsordre.  

## <a name="to-post-capacities"></a>Sådan bogføres kapaciteter  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kapacitetskladder**, og vælg derefter det relaterede link.  
2.  Udfyld felterne **Bogføringsdato** og **Bilagsnr** .  
3.  Angiv den type kapacitet, du bogfører, i feltet **Type**, enten **Produktionsressource** eller **Arbejdscenter**.  
4.  I feltet **Nummer** skal du angive nummeret på produktionsressourcen eller arbejdscentret.  
5.  Angiv de relevante data i de andre felter, f.eks. **Starttidspunkt**, **Sluttidspunkt**, **Antal** og **Spild**.  
6.  Vælg handlingen **Bogfør** for at bogføre kapaciteterne.  

## <a name="to-view-work-center-ledger-entries"></a>Sådan vises arbejdscenterposter  
På siderne **Arbejdscenterkort** og **Prod.ress.kort** kan du få vist de bogførte kapaciteter som følge af færdige produktionsordrer.    
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **arbejdscentre**, og vælg derefter det relaterede link.  
2.  Åbn det relevante **arbejdscenter**-kort på listen, og vælg derefter handlingen **Kapacitetsposter**.  

Siden **Kapacitetsposter** vises med posterne i den rækkefølge, de er bogført.   

## <a name="see-also"></a>Se også  
[Produktion](production-manage-manufacturing.md)    
[Konfigurere produktion](production-configure-production-processes.md)  
[Planlægning](production-planning.md)      
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]