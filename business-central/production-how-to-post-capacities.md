---
title: Bogføre kapaciteter
description: 'Bogfør forbrugt kapacitet, der ikke er knyttet til produktionsordren i kapacitetskladden, og få vist bogførte kapaciteter på siden kapacitetsposter.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '5832, 99000802, 99000820'
ms.date: 03/08/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Bogføre kapaciteter

I kapacitetskladden kan du bogføre forbrugt kapacitet, der ikke er knyttet til produktionsordren. Vedligeholdelsesarbejde skal f.eks. knyttes til kapaciteten, men ikke til en produktionsordre.  

## Sådan bogføres kapaciteter  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kapacitetskladder**, og vælg derefter det relaterede link.  
2. Udfyld felterne **Bogføringsdato** og **Bilagsnr** .  
3. Angiv den type kapacitet, du bogfører, i feltet **Type**, enten **Produktionsressource** eller **Arbejdscenter**.  
4. I feltet **Nummer** skal du angive nummeret på produktionsressourcen eller arbejdscentret.  
5. Angiv de relevante data i de andre felter, f.eks. **Starttidspunkt**, **Sluttidspunkt**, **Antal** og **Spild**.  
6. Vælg handlingen **Bogfør** for at bogføre kapaciteterne.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Sådan vises arbejdscenterposter  

På siderne **Arbejdscenterkort** og **Prod.ress.kort** kan du få vist de bogførte kapaciteter som følge af færdige produktionsordrer.    
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **arbejdscentre**, og vælg derefter det relaterede link.  
2. Åbn det relevante **arbejdscenter**-kort på listen, og vælg derefter handlingen **Kapacitetsposter**.  

    Siden **Kapacitetsposter** vises med posterne i den rækkefølge, de er bogført.   

## Se også  

[Produktion](production-manage-manufacturing.md)  
[Konfigurere produktion](production-configure-production-processes.md)  
[Planlægning](production-planning.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]