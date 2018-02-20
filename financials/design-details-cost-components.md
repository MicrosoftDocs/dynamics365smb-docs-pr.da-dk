---
title: "Designoplysninger – Omkostningskomponenter | Microsoft Docs"
description: "Omkostningskomponenter er forskellige typer af omkostninger, der udgør værdien af en lagerforøgelse eller -reducering."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0a134142bfcb11692ed6157e873fcfa2900b9222
ms.contentlocale: da-dk
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-cost-components"></a>Designoplysninger: Kostkomponenter
Omkostningskomponenter er forskellige typer af omkostninger, der udgør værdien af en lagerforøgelse eller -reducering.  

 Følgende tabel viser de forskellige omkostningskomponenter og eventuelle underordnede omkostningskomponenter, de består af.  

|Omkostningskomponent|Underordnet omkostningskomponent|Description|  
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
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

