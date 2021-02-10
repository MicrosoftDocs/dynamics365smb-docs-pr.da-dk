---
title: Oprette et lokationskort og definere overflytningsruter | Microsoft Docs
description: Du kan oprette et lokationskort for hvert sted, du gemme lagervarer, for eksempel et lagersted eller distributionscenter, og definere ruter for at overflytte varer mellem lokationerne.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6cdfee54927dd6e966f1fd1ac0b4e40ba9df1135
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750076"
---
# <a name="set-up-locations"></a>Opsætte lokationer
Hvis du køber, gemme eller sælger varer i mere end ét område eller lagersted, skal du oprette hver lokation med et lokationskort og definere overflytningsruter.

Du kan derefter oprette dokumentlinjer for en bestemt lokation vis tilgængeligehed pr. lokation og vare samt overføre lagerbeholdning mellem lokationer. Der er flere oplysninger i [Administrere lager](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="to-create-a-location-card"></a>Sådan oprettes et lokationskort
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lokationer**, og vælg dernæst det relaterede link.
2. Vælg handlingen **Ny**.
3. På siden **Lokationskort** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Gentag trin 2 og 3 for hver lokation, hvor du vil foretage lageropgørelse.

> [!NOTE]  
> Mange af felterne på lokationskortet henviser til håndtering af varer i indgående og udgående lagerprocesser. Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).

## <a name="to-create-a-transfer-route"></a>Sådan oprettes en overflytningsrute
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Overflytningsruter**, og vælg derefter det relaterede link.
2. Du kan også vælge handlingen **Overflytningsruter** på enhver **Lokationskort**-side.
3. Vælg handlingen **Ny**.
4. På siden **Lokationskort** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Du kan nu overflytte lagervarer mellem to lokationer. Du kan finde flere oplysninger i [Overflytte lagerbeholdning mellem lokationer](inventory-how-transfer-between-locations.md).    

## <a name="see-also"></a>Se også
[Administrere lager](inventory-manage-inventory.md)  
[Overflytte lagerbeholdning mellem lokationer](inventory-how-transfer-between-locations.md)    
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)
