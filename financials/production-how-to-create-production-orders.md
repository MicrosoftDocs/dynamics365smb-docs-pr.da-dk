---
title: "Sådan oprettes produktionsordrehoveder | Microsoft Docs"
description: "Du kan oprette en produktionsordre manuelt, og det første trin i denne procedure er at oprette et produktionsordrehoved."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0c792dbb7d7261e8f8b89ca4f3d39d875142c4eb
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-production-order-headers"></a>Sådan oprettes produktionsordrehoveder
Du kan oprette en produktionsordre manuelt, og det første trin i denne procedure er at oprette et produktionsordrehoved.

Produktionsordrer oprettes typisk automatisk af en planlægningsfunktion til opfyldning af et kendt behov. Du kan finde flere oplysninger i [Planlægning](production-planning.md).   

I proceduren nedenfor oprettes en fastlagt produktionsordre. Du kan også oprette produktionsordrer med en anden status.  

## <a name="to-create-a-production-order-header"></a>Sådan oprettes et produktionsordrehovede  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ordreplanlægning**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3.  I feltet **Nummer** skal du indsætte næste nummer i serien.  
4.  Marker kilden til produktionsordren i feltet **Kildetype**.

    Her kan du vælge at oprette til en familie af varer. Du kan finde flere oplysninger under [Fremgangsmåde: Arbejde med produktionsfamilier](production-how-work-family.md).
5.  Marker varenummer, familie eller salgshoved, som produktionsordren genereres for, i feltet **Kildenr.**.  
6.  Udfyld felterne **Antal** og **Forfaldsdato** i overensstemmelse med dine specifikationer.  

Når du ændrer produktionskravene, f.eks. komponenter og operationer, kan du hurtigt omplanlægge produktionsordren. Du kan finde flere oplysninger i [Fremgangsmåde: Omplanlæg eller forny produktionsordrer direkte](production-how-to-replan-refresh-production-orders.md). 

## <a name="see-also"></a>Se også  
[Produktion](production-manage-manufacturing.md)    
[Konfigurere produktion](production-configure-production-processes.md)  
[Planlægning](production-planning.md)      
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

