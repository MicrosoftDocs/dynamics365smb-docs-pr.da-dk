---
title: Sådan oprettes speditører | Microsoft Docs
description: Du kan angive en kode for hver speditør og angive oplysninger om dem.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fbd27caed8be1e7231f98964890fafed66c7bbbb
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748214"
---
# <a name="set-up-shipping-agents"></a>Oprette speditører
Du kan angive en kode for hver speditør og angive oplysninger om dem.  

Hvis du angiver en internetadresse for speditøren, og denne tilbyder pakkesporing over internettet, kan du anvende programmets automatiske pakkesporingsfunktion. Du kan finde flere oplysninger under [Spore pakker](sales-how-track-packages.md).

Når du angiver speditører i salgsordrerne, kan du også angive den service, som den enkelte speditør tilbyder.  
Du kan angive et ubegrænset antal serviceydelser for hver speditør, og du kan angive en transporttid for hver service.  

Når du har tilknyttet en speditørservice til salgsordrelinjen, medtages transporttiden for den pågældende service i beregningen af ordrebekræftelsen for linjen. Du kan finde flere oplysninger i [Beregne ordrebekræftelsesdatoer](sales-how-to-calculate-order-promising-dates.md).

## <a name="to-set-up-a-shipping-agent"></a>Sådan oprettes en speditør  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Speditører**, og vælg derefter det relaterede link.  
2.  Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  
3.  Vælg handlingen **Speditørservice**.
4. I feltet **Speditørservice** skal du udfylde felterne efter behov.

> [!NOTE]  
>  Hvis du sletter speditøren på ordrelinjen, slettes speditørservicekoden også. Derefter beregnes oplysningerne i de felter, der er baseret på speditørservicen, igen.  

## <a name="see-also"></a>Se også
[Oprette leveringsformer](sales-how-set-up-shipment-methods.md)  
[Spore pakker](sales-how-track-packages.md)    
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
