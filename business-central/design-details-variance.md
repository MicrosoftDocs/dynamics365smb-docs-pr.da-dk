---
title: Designoplysninger – Afvigelse | Microsoft Docs
description: Afvigelsen er defineret som forskellen mellem den faktiske kostpris og standardkostprisen, som beskrevet i følgende formel.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 02e8992c7a116d62cad767e10f318005c7eed2ca
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786458"
---
# <a name="design-details-variance"></a>Designoplysninger: Afvigelse
Afvigelsen er defineret som forskellen mellem den faktiske kostpris og standardkostprisen, som beskrevet i følgende formel.  

 faktiske omkostninger – standardomkostninger = afvigelse  

 Hvis de faktiske omkostninger ændres, eksempelvis fordi du bogfører et varegebyr på en senere dato, opdateres afvigelsen tilsvarende.  

> [!NOTE]  
>  Værdiregulering påvirker ikke beregningen af afvigelse, fordi værdiregulering kun ændrer lagerværdien.  

## <a name="example"></a>Eksempel  
 Følgende eksempel illustrerer, hvordan afvigelsen beregnes for købte varer. Den bygger på følgende scenario:  

1.  Brugeren køber en vare til RV 90,00, men standardkostprisen er RV 100,00. Derfor bliver købsafvigelsen RV -10,00.  
2.  RV 10,00 krediteres købsafvigelseskontoen.  
3.  Brugeren bogfører et varegebyr på RV 20,00. Derfor øges de faktiske omkostninger til RV 110,00, og værdien af købsafvigelsen bliver RV 10,00.  
4.  RV 20,00 debiteres købsafvigelseskontoen. Derfor bliver nettokøbsafvigelsen RV 10,00.  
5.  Brugeren regulerer varen fra RV 100,00 til 70,00. Dette påvirker ikke beregningen af afvigelse, kun lagerværdien.  

 Følgende tabel viser de resulterende værdiposter.  

 ![Beregning af købsafvigelse](media/design_details_inventory_costing_11_purchase_variance.png "Beregning af købsafvigelse")  

## <a name="determining-the-standard-cost"></a>Bestemmelse af standardkostpris  
 Standardkostprisen bruges til beregning af afvigelse og beløbet, der skal kapitaliseres. Da standardkostprisen kan ændres med tiden på grund af manuel opdateringsberegning, skal du bruge et tidspunkt, hvor standardkostprisen er fast til beregning af varians. Dette punkt er, når lagerforøgelsen er faktureret. For producerede eller monterede varer er punktet for, hvornår standardomkostninger bestemmes, når omkostningerne reguleres.  

 Følgende tabel viser, hvordan forskellige kostprisfordelinger beregnes for producerede og monterede varer, når du bruger funktionen Beregn standardkostpris.  

|Kostprisfordeling|Købt vare|Produceret/monteret vare|  
|----------------|--------------------|------------------------------|  
|**Kostpris (standard)**||Materialekostprisen på enkeltniveau + kapacitetskostpris på enkeltniveau + underlev.kostpris på enkeltniveau + ind. kap.kostpris på enkeltniveau + ind. prod.kostpris på enkeltniveau|  
|**Materialekostpris (enkeltniv.)**|Kostpris|![Ligning 1](media/design_details_inventory_costing_11_equation_1.png "Ligning 1")|  
|**Kapacitetskostpris (enkeltniv)**|Ikke tilgængelig|![Ligning 2](media/design_details_inventory_costing_11_equation_2.png "Ligning 2")|  
|**Underlev.kostpris (enkeltniv.)**|Ikke tilgængelig|![Ligning 3](media/design_details_inventory_costing_11_equation_3.png "Ligning 3")|  
|**Ind. kap.kostpris (enkeltniv.)**|Ikke tilgængelig|![Ligning 4](media/design_details_inventory_costing_11_equation_4.png "Ligning 4")|  
|**Ind. prod.kostpris (enkeltniv)**|Ikke tilgængelig|(Materialekostpris (enkeltniv.) + Kapacitetskostpris (enkeltniv) + Underlev.kostpris (enkeltniv.)) * Indir. omkostninger % / 100 + IPO-bidrag|  
|**Akkum. materialekostpris**|Kostpris|![Ligning 5](media/design_details_inventory_costing_11_equation_5.png "Ligning 5")|  
|**Akkum. kapacitetskostpris**|Ikke tilgængelig|![Ligning 6](media/design_details_inventory_costing_11_equation_6.png "Ligning 6")|  
|**Underlev.kostpris (akkum.)**|Ikke tilgængelig|![Ligning 7](media/design_details_inventory_costing_11_equation_7.png "Ligning 7")|  
|**Akkumulerede indirekte kapacitetsomkostninger**|Ikke tilgængelig|![Ligning 8](media/design_details_inventory_costing_11_equation_8.png "Ligning 8")|  
|**Ind. prod.kostpris (akkum.)**|Ikke tilgængelig|![Ligning 9](media/design_details_inventory_costing_11_equation_9.png "Ligning 9")|  

## <a name="see-also"></a>Se også  
 [Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)   
 [Designoplysninger – Kostmetoder](design-details-costing-methods.md) [Administrere lageromkostninger](finance-manage-inventory-costs.md)  
 [Finans](finance.md)  
 [Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]