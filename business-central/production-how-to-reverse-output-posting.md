---
title: Sådan fortryder du bogføring af afgang | Microsoft Docs
description: Det kan ske, at bogført afgang skal tilbageføres. Det kan f.eks. ske, hvis en oplysning registreres forkert, så et forkert afgangsantal bogføres på en produktionsordre.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 33be858c687381a50f42d1c59ca735358f113d72
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788746"
---
# <a name="reverse-output-posting"></a>Tilbageføre bogføring af afgang
Det kan ske, at bogført afgang skal tilbageføres. Det kan f.eks. ske, hvis en oplysning registreres forkert, så et forkert afgangsantal bogføres på en produktionsordre.  

## <a name="to-reverse-an-output-posting"></a>Tilbageføre en afgangsbogføring  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Afgangskladde**, og vælg derefter det relaterede link. Vælg en kørsel.  
2. Udfyld felterne efter behov. Du kan finde flere oplysninger i [Massebogføre afgang og operationstider](production-how-to-post-output-quantity.md).
3.  Vælg den tilknyttede varepost i feltet **Udlign.postløbenr.**. Det tilbagefører kapacitets- og vareposterne.  
4. Bogfør tilbageførslen ved at bogføre kladden.  

Posterne i afgangskladden bogføres til vareposten som en positiv regulering.  

## <a name="see-also"></a>Se også  
 [Produktion](production-manage-manufacturing.md)    
 [Konfigurere produktion](production-configure-production-processes.md)  
 [Planlægning](production-planning.md)      
 [Lagerbeholdning](inventory-manage-inventory.md)  
 [Køb](purchasing-manage-purchasing.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
