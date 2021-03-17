---
title: Sådan massebogføres produktionsafgang og operationstid | Microsoft Docs
description: Afgangsantallet angiver arbejdsforløbet i form af det færdige antal.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 83354217bac3b27457303083163cf5eae4494e79
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380452"
---
# <a name="batch-post-output-and-run-times"></a>Massebogføre afgang og operationstider
Afgangsantallet angiver arbejdsforløbet i form af det færdige antal.  

> [!NOTE]
> Lageret opdateres kun automatisk, når du bogfører afgangsantal i den sidste operation.  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a>Sådan bogføres afgangsantal for en eller flere produktionsordrelinjer
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Afgangskladde**, og vælg derefter det relaterede link.  
2. Udfyld felterne med produktionsordredataene og afgangsdataene. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis operationen er afsluttet, skal du markere feltet **Afsluttet**.  

    Hvis den lagerlokation, hvor varerne skal lægges på lager, bruger placeringer, men ikke kræver læg-på-lager, skal du tildele en placeringskode til kladdelinjen for at angive, hvor varerne skal lægges på lageret. Du kan finde flere oplysninger i [Lægge produktions- eller montageafgange på lager](warehouse-how-to-put-away-production-output.md).  

4. Vælg handlingen **Bogfør** for at bogføre operationerne. Afgangsantallet bogføres. Varen er nu klar til afsendelse.  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a>Sådan bogføres operationstider for en eller flere produktionsordrelinjer
Operationstiden angiver arbejdsforløbet i form af den nødvendige arbejdstid.    

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Afgangskladde**, og vælg derefter det relaterede link.  
2. Udfyld felterne med produktionsordredataene og afgangsdataene.  
3.  Hvis operationen er afsluttet, skal du vælge feltet **Afsluttet**.  
4. Vælg handlingen **Bogfør** for at bogføre den tid, der bruges pr. operation. Kapacitetsposter opdateres for de anvendte arbejdscentre eller produktionsressourcer.

## <a name="see-also"></a>Se også  
[Produktion](production-manage-manufacturing.md)    
[Konfigurere produktion](production-configure-production-processes.md)  
[Planlægning](production-planning.md)      
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]