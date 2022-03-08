---
title: Sådan massebogføres forbrug | Microsoft Docs
description: Hvis trækmetoden er **Manuel**, skal du bogføre komponenterne manuelt ved at bruge en forbrugskladde.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: d84d7d3961a466025b6e38665f88ee58baf153b3
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2313296"
---
# <a name="batch-post-production-consumption"></a>Massebogføre produktionsforbrug
Hvis trækmetoden er **Manuel**, skal du bogføre komponenterne manuelt ved at bruge en forbrugskladde.

Du kan også angive systemet til automatisk for at bogføre (*trække*) komponenterne, når du starter eller afslutter produktionsordrer. Du kan finde flere oplysninger i [Aktivere udtrækning af komponenter i henhold til operationsafgang](production-how-to-flush-components-according-to-operation-output.md).

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a>Sådan bogføres forbrug for en eller flere produktionsordrelinjer  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Forbrugskladde**, og vælg derefter det relaterede link.  
2.  Udfyld felterne med produktionsordredata og forbrugsdata. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Hvis den lagerlokation, hvor komponenterne opbevares, er angivet til at bruge placeringer, men ikke kræver pluk, skal du tildele en placeringskode til kladdelinjen for at angive, hvor varerne skal hentes på lageret. Du kan finde flere oplysninger i [Plukke til produktion eller montage](warehouse-how-to-pick-for-production.md).  
3.  Vælg handlingen **Bogfør** for at bogføre forbruget. De tilknyttede vareposter reduceres.

## <a name="see-also"></a>Se også  
[Produktion](production-manage-manufacturing.md)    
[Konfigurere produktion](production-configure-production-processes.md)  
[Planlægning](production-planning.md)      
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
