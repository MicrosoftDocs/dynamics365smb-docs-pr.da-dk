---
title: Sådan oprettes produktionsordrehoveder | Microsoft Docs
description: Du kan oprette en produktionsordre manuelt, og det første trin i denne procedure er at oprette et produktionsordrehoved.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 76d4b69de41343815175a7acd4329bb47b889f5a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759363"
---
# <a name="create-production-order-headers"></a>Oprette produktionsordrehoveder
Du kan oprette en produktionsordre manuelt, og det første trin i denne procedure er at oprette et produktionsordrehoved.

Produktionsordrer oprettes typisk automatisk af en planlægningsfunktion til opfyldning af et kendt behov. Du kan finde flere oplysninger i [Planlægning](production-planning.md).   

I proceduren nedenfor oprettes en fastlagt produktionsordre. Du kan også oprette produktionsordrer med en anden status.  

## <a name="to-create-a-production-order-header"></a>Sådan oprettes et produktionsordrehovede  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Fastlagt produktionsordrer**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3.  I feltet **Nummer** skal du indsætte næste nummer i serien.  
4.  Marker kilden til produktionsordren i feltet **Kildetype**.

    Her kan du vælge at oprette til en familie af varer. Du kan finde flere oplysninger under [Arbejde med produktionsfamilier](production-how-work-family.md).
5.  Marker varenummer, familie eller salgshoved, som produktionsordren genereres for, i feltet **Kildenr.**.  
6.  Udfyld felterne **Antal** og **Forfaldsdato** i overensstemmelse med dine specifikationer.  

Når du ændrer produktionskravene, f.eks. komponenter og operationer, kan du hurtigt omplanlægge produktionsordren. Du kan finde flere oplysninger i [Omplanlægge eller forny produktionsordrer direkte](production-how-to-replan-refresh-production-orders.md). 

## <a name="see-also"></a>Se også  
[Produktion](production-manage-manufacturing.md)    
[Konfigurere produktion](production-configure-production-processes.md)  
[Planlægning](production-planning.md)      
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
