---
title: Designoplysninger – Omkostningskomponenter | Microsoft Docs
description: Omkostningskomponenter er forskellige typer af omkostninger, der udgør værdien af en lagerforøgelse eller -reducering.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d8e2d00e82f2ed5342e3c06dfaf54d8d6a88e941
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751742"
---
# <a name="design-details-cost-components"></a>Designoplysninger: Kostkomponenter
Omkostningskomponenter er forskellige typer af omkostninger, der udgør værdien af en lagerforøgelse eller -reducering.  

 Følgende tabel viser de forskellige omkostningskomponenter og eventuelle underordnede omkostningskomponenter, de består af.  

|Omkostningskomponent|Underordnet omkostningskomponent|Beskrivelse|  
|--------------------|--------------------------------|---------------------------------------|  
|Købspris|Kostpris (direkte købspris)|Kostpris, som kan spores direkte til et kostobjekt.|  
|Købspris|Fragtomkostninger (varegebyr)|Kostpris, som kan spores direkte til et kostobjekt.|  
|Købspris|Forsikringsomkostninger (varegebyr)|Kostpris, som kan spores direkte til et kostobjekt.|  
|Indir. omkostninger||Kostpris, som kan spores til et omkostningsemne.|  
|Varians|Købsafvigelse|Forskellen mellem faktiske kostpriser og standardkostpriser, som kun bogføres for varer ved hjælp af kostmetoden **Standard** .|  
|Varians|Materialeomkostningsafvigelse|Forskellen mellem faktiske kostpriser og standardkostpriser, som kun bogføres for varer ved hjælp af kostmetoden **Standard** .|  
|Varians|Kapacitetsomkostningsafvigelse|Forskellen mellem faktiske kostpriser og standardkostpriser, som kun bogføres for varer ved hjælp af kostmetoden **Standard** .|  
|Varians|Underlev.kostafvigelse|Forskellen mellem faktiske kostpriser og standardkostpriser, som kun bogføres for varer ved hjælp af kostmetoden **Standard** .|  
|Varians|Afvigelse i indirekte kapacitetsomkostning|Forskellen mellem faktiske kostpriser og standardkostpriser, som kun bogføres for varer ved hjælp af kostmetoden **Standard** .|  
|Varians|Afvigelse i indirekte produktionskostpriser|Forskellen mellem faktiske kostpriser og standardkostpriser, som kun bogføres for varer ved hjælp af kostmetoden **Standard** .|  
|Værdiregulering||En afskrivning eller opskrivning af den aktuelle lagerværdi.|  
|Afrunding||Restværdier som følge af beregningsmetoden for værdiansættelsen af lagerreduktioner.|  

> [!NOTE]  
>  Fragt og forsikringsomkostninger er varegebyrer, der når som helst kan føjes til en vares kostpris. Når du udfører kørslen **Juster kostpris - vareposter**, opdateres værdien af enhver relateret lagerreduktion tilsvarende.  

## <a name="see-also"></a>Se også  
 [Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)   
 [Designoplysninger: Afvigelse](design-details-variance.md) [Administrere lageromkostninger](finance-manage-inventory-costs.md)  
 [Finans](finance.md)  
 [Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]