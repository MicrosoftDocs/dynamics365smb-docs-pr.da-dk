---
title: "Sådan massebogføres forbrug | Microsoft Docs"
description: "Hvis trækmetoden er **Manuel**, skal du bogføre komponenterne manuelt ved at bruge en forbrugskladde."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4058d16ee3bdfc10933e1f3a01c84fbc5d0b0ebb
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="batch-post-production-consumption"></a>Massebogføre produktionsforbrug
Hvis trækmetoden er **Manuel**, skal du bogføre komponenterne manuelt ved at bruge en forbrugskladde.

Du kan også angive systemet til automatisk for at bogføre (*trække*) komponenterne, når du starter eller afslutter produktionsordrer. Du kan finde flere oplysninger i [Aktivere udtrækning af komponenter i henhold til operationsafgang](production-how-to-flush-components-according-to-operation-output.md).

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a>Sådan bogføres forbrug for en eller flere produktionsordrelinjer  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Forbrugskladde**, og vælg derefter det relaterede link.  
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

