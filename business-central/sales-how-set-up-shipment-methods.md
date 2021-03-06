---
title: Sådan oprettes leveringsformer | Microsoft Docs
description: Du kan angive en kode for hver leveringsform, du tilbyder, og angive oplysninger om dem.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f1916724c995f875d15b931e919d07d2253dcdb1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748290"
---
# <a name="set-up-shipment-methods"></a>Oprette leveringsformer
Leveringsformerne, der også kaldes incoterms, afhænger ofte af varerne, kunderne og leverandørerne. En kunde, der bor på en ø, vælger måske, at varerne altid skal flyves eller sejles til øen. Nogle kunder kan kræve levering næste dag. Det ønsker at afhente ordren. På debitor- og kreditorkortene kan du derfor angive den ønskede leveringsform.

Du opretter beskrivelsen og koden for hver leveringsform på siden **Leveringsformer**. Du kan f.eks. oprette koden FOB (Free on board) og skrive Free on Board i feltet **Beskrivelse**. Du kan indtaste koden i **Leveringskode**-felterne et andet sted i systemet, f.eks. på et debitorkort. Når du derefter opretter nye ordrer, fakturaer, kreditnotaer osv., bruges den beskrivelse, som koden repræsenterer, automatisk af systemet. Du kan ændre dette i dokumentet efter behov.

## <a name="to-set-up-a-shipment-code"></a>Sådan defineres en leveringskode
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Forsendelsesformer**, og vælg derefter det relaterede link.
2. På siden **Leveringsformer** skal du vælge handlingen **Ny**.
3. Angiv en kode og en beskrivelse af leveringsformen på den nye linje.

## <a name="see-also"></a>Se også
[Incoterms](https://iccwbo.org/resources-for-business/incoterms-rules)  
[Oprette speditører](sales-how-to-set-up-shipping-agents.md)  
[Spore pakker](sales-how-track-packages.md)    
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]