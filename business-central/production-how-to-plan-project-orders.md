---
title: Sådan planlægges projektordrer | Microsoft Docs
description: Denne planlægningsopgave starter ud fra en salgsordre og bruger siden **Salgsordreplanlægning**. Når du har oprettet en projektproduktionsordre, kan du planlægge den yderligere på siden **Ordreplanlægning**.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 28568cd8ab7751e15bf24acd3c727828bba9f76c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787948"
---
# <a name="plan-project-orders"></a>Planlægge projektordrer
Denne planlægningsopgave starter ud fra en salgsordre og bruger siden **Salgsordreplanlægning**. Når du har oprettet en projektproduktionsordre, kan du planlægge den yderligere på siden **Ordreplanlægning**.  

## <a name="to-create-a-project-production-order"></a>Sådan oprettes en projektproduktionsordre  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordre**, og vælg derefter det relaterede link.  
2.  Vælg den salgsordre, der repræsenterer produktionsprojektet, og vælg derefter handlingen **Planlægning**.  
4.  På siden **Salgsordreplanlægning** skal du vælge handlingen **Opret prod.ordre**.  
5.  Vælg **Projektordre** i feltet **Ordretype** på siden **Opret ordre fra salg**.  
6.  Vælg knappen **Ja**.  
7.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Produktionsordrer**, og vælg derefter det relaterede link.
8. Åbn den produktionsordre, du lige har oprettet.  

    Bemærk, at feltet **Kildetype** i produktionsordren indeholder **Salgshoved**, og ordren indeholder flere linjer, en for hver salgslinjevare, der skal produceres.  
9. Vælg handlingen **Planlægning**.
10. Vælg handlingen **Opdater** på siden **Ordreplanlægning** for at beregne et nyt behov.  

Produktionsordrens ordrehovedlinje vises med alle uopfyldte behovslinjer udvidet under den. Selvom produktionsordren indeholder linjer for flere produktionsvarer, vises det samlede behov for alle produktionsordrelinjer under én ordrehovedlinje på siden **Ordreplanlægning**, og det oprindelige kundenavn vises. Du kan nu fortsætte med at planlægge efter behovet som beskrevet i emnet [Planlægge efter nyt behov ordre for ordre](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
>  Linjer i projektproduktionsordren, der har behov for **Prod.ordre** i feltet **Genbestillingssystem**, repræsenterer underliggende produktionsordrer. Når du har oprettet disse produktionsordrer, skal der beregnes en plan på siden **Ordreplanlægning** for at identificere eventuelle ekspederet komponentbehov for dem. I så fald vises de som behovslinjer under en normal produktionsordrehovedlinje, hvilket betyder, at projektrelationen ikke længere er synlig på siden. Men hvis du bruger funktionen til ordresporing, kan du derefter se frem og tilbage i alle forsyningsordrer, der er foretaget under den oprindelige salgsordre.  

## <a name="see-also"></a>Se også
[Planlægning](production-planning.md)   
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)   
[Konfigurere bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]