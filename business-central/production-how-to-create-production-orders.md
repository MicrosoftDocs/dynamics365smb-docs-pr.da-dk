---
title: Oprette produktionsordrehoveder
description: 'Du kan oprette en produktionsordre manuelt, og det første trin i denne procedure er at oprette et produktionsordrehoved.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '9325, 99000815, 99000829, 9900083'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="create-production-order-headers"></a>Oprette produktionsordrehoveder

Du kan oprette en produktionsordre manuelt, og det første trin i denne procedure er at oprette et produktionsordrehoved.

Produktionsordrer oprettes typisk automatisk af en planlægningsfunktion til opfyldning af et kendt behov. Du kan finde flere oplysninger i [Planlægning](production-planning.md).  

I proceduren nedenfor oprettes en fastlagt produktionsordre. Du kan også oprette produktionsordrer med en anden status.  

## <a name="to-create-a-production-order-header"></a>Sådan oprettes et produktionsordrehovede

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Fastlagt produktionsordrer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. I feltet **Nummer** skal du indsætte næste nummer i serien.  
4. Marker kilden til produktionsordren i feltet **Kildetype**.

    Her kan du vælge at oprette til en familie af varer. Du kan finde flere oplysninger i [Arbejde med produktionsfamilier](production-how-work-family.md).
5. Marker varenummer, familie eller salgshoved, som produktionsordren genereres for, i feltet **Kildenr.**.  
6. Udfyld felterne **Antal** og **Forfaldsdato** i overensstemmelse med dine specifikationer.  

Når du ændrer produktionskravene, f.eks. komponenter og operationer, kan du hurtigt omplanlægge produktionsordren. Du kan finde flere oplysninger i [Omplanlægge eller forny produktionsordrer direkte](production-how-to-replan-refresh-production-orders.md).  

## <a name="see-also"></a>Se også

[Produktion](production-manage-manufacturing.md)
[Konfigurere produktion](production-configure-production-processes.md)  
[Skabelon](production-planning.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
