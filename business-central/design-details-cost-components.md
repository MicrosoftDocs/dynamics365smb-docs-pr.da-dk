---
title: Designoplysninger – Omkostningskomponenter | Microsoft Docs
description: Omkostningskomponenter er forskellige typer af omkostninger, der udgør værdien af en lagerforøgelse eller -reducering.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 1c1dd2eafb648a7c6053406ea3c931d6e7cecb76
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215354"
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