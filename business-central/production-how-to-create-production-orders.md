---
title: Sådan oprettes produktionsordrehoveder | Microsoft Docs
description: Du kan oprette en produktionsordre manuelt, og det første trin i denne procedure er at oprette et produktionsordrehoved.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 70a6f2e583e5ba78eecae0a25d6533d8265414ca
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "913625"
---
# <a name="create-production-order-headers"></a>Oprette produktionsordrehoveder
Du kan oprette en produktionsordre manuelt, og det første trin i denne procedure er at oprette et produktionsordrehoved.

Produktionsordrer oprettes typisk automatisk af en planlægningsfunktion til opfyldning af et kendt behov. Du kan finde flere oplysninger i [Planlægning](production-planning.md).   

I proceduren nedenfor oprettes en fastlagt produktionsordre. Du kan også oprette produktionsordrer med en anden status.  

## <a name="to-create-a-production-order-header"></a>Sådan oprettes et produktionsordrehovede  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Fastlagte prod.ordrer**, og vælg derefter det relaterede link.  
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
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
