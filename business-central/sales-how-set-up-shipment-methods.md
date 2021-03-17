---
title: Oprette leveringsformer
description: Du kan angive en kode for hver leveringsform, du tilbyder, og angive oplysninger om dem.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 03/09/2021
ms.author: edupont
ms.openlocfilehash: 096b609d26ad24785f90634d725d751ac57b346e
ms.sourcegitcommit: 35f7e24c301926b39094aa64fe608afd04fdb8e1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573297"
---
# <a name="set-up-shipment-methods"></a>Oprette leveringsformer

Leveringsmetoder afhænger ofte af varerne, kunderne og leverandørerne. En kunde, der bor på en ø, vælger måske, at varerne altid skal flyves eller sejles til øen. Nogle kunder kan kræve levering næste dag. Det ønsker at afhente ordren. På debitor- og kreditorkortene kan du derfor angive den ønskede leveringsform.

Du opretter beskrivelsen og koden for hver leveringsform på siden **Leveringsformer**. Du kan f.eks. oprette koden FOB (Free on board) og skrive Free on Board i feltet **Beskrivelse**. Du kan indtaste koden i **Leveringskode**-felterne et andet sted i systemet, f.eks. på et debitorkort. Når du derefter opretter nye ordrer, fakturaer, kreditnotaer osv., bruges den beskrivelse, som koden repræsenterer, automatisk af systemet. Du kan ændre dette i dokumentet efter behov.

## <a name="to-set-up-a-shipment-method"></a>Sådan defineres en leveringsform

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Forsendelsesformer**, og vælg derefter det relaterede link.
2. På siden **Leveringsformer** skal du vælge handlingen **Ny**.
3. Angiv en kode og en beskrivelse af leveringsformen på den nye linje.

> [!TIP]
> Hvis du bruger Incoterms, skal du oprette leveringsmetoder for at angive de relevante Incoterms-regler.  

## <a name="see-also"></a>Se også

[Oprette speditører](sales-how-to-set-up-shipping-agents.md)  
[Spore pakker](sales-how-track-packages.md)  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)  
[Montagestyring](assembly-assemble-items.md)  
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Incoterms på iccwbo.org](https://iccwbo.org/resources-for-business/incoterms-rules)  

[!INCLUDE[footer-include](includes/footer-banner.md)]