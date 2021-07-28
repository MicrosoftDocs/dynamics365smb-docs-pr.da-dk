---
title: 'Fremgangsmåde: Tilbageføre afgangsbogføring'
description: Det kan ske, at bogført afgang skal tilbageføres. I dette emne beskrives fremgangsmåden til tilbageførsel af afgangsbogføring.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: b1d3d05876beb452d8a3fd1ac917e40f1ffe7320
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6440349"
---
# <a name="reverse-output-posting"></a>Tilbageføre bogføring af afgang
Det kan ske, at bogført afgang skal tilbageføres. Det kan f.eks. ske, hvis en oplysning registreres forkert, så et forkert afgangsantal bogføres på en produktionsordre.  

## <a name="to-reverse-an-output-posting"></a>Tilbageføre en afgangsbogføring  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Afgangskladde**, og vælg derefter det relaterede link. Vælg en kørsel.  
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
 [Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]