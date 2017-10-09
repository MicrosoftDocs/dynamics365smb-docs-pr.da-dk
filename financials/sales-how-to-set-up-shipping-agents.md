---
title: "Sådan oprettes speditører | Microsoft Docs"
description: "Du kan angive en kode for hver speditør og angive oplysninger om dem."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 84a5d9eb8757dc82834c17327ffbb510cd15fa1a
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-shipping-agents"></a>Sådan oprettes speditører
Du kan angive en kode for hver speditør og angive oplysninger om dem.  

Hvis du angiver en internetadresse for speditøren, og denne tilbyder pakkesporing over internettet, kan du anvende programmets automatiske pakkesporingsfunktion. Du kan finde flere oplysninger under [Sådan spores pakker](sales-how-track-packages.md).

Når du angiver speditører i salgsordrerne, kan du også angive den service, som den enkelte speditør tilbyder.  
Du kan angive et ubegrænset antal serviceydelser for hver speditør, og du kan angive en transporttid for hver service.  

Når du har tilknyttet en speditørservice til salgsordrelinjen, medtages transporttiden for den pågældende service i beregningen af ordrebekræftelsen for linjen. Du kan finde flere oplysninger i [Sådan beregnes ordrebekræftelsesdatoer](sales-how-to-calculate-order-promising-dates.md).

## <a name="to-set-up-a-shipping-agent"></a>Sådan oprettes en speditør  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Speditører**, og vælg derefter det relaterede link.  
2.  Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  
3.  Vælg handlingen **Speditørservice**.
4. I feltet **Speditørservice** skal du udfylde felterne efter behov.

> [!NOTE]  
>  Hvis du sletter speditøren på ordrelinjen, slettes speditørservicekoden også. Derefter beregnes oplysningerne i de felter, der er baseret på speditørservicen, igen.  

## <a name="see-also"></a>Se også
[Sådan spores pakker](sales-how-track-packages.md)    
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

