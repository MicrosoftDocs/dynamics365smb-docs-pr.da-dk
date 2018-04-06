---
title: "Sådan planlægges projektordrer | Microsoft Docs"
description: "Denne planlægningsopgave starter ud fra en salgsordre og bruger vinduet **Salgsordreplanlægning**. Når du har oprettet en projektproduktionsordre, kan du planlægge den yderligere i vinduet **Ordreplanlægning**."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 27b2571df137b489a72673251fb5a176bfa771fe
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="plan-project-orders"></a>Planlægge projektordrer
Denne planlægningsopgave starter ud fra en salgsordre og bruger vinduet **Salgsordreplanlægning**. Når du har oprettet en projektproduktionsordre, kan du planlægge den yderligere i vinduet **Ordreplanlægning**.  

## <a name="to-create-a-project-production-order"></a>Sådan oprettes en projektproduktionsordre  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsordrer**, og vælg derefter det relaterede link.  
2.  Vælg den salgsordre, der repræsenterer produktionsprojektet, og vælg derefter handlingen **Planlægning**.  
4.  I vinduet **Salgsordreplanlægning** skal du vælge handlingen **Opret prod.ordre**.  
5.  Vælg **Projektordre** i feltet **Ordretype** i vinduet **Opret ordre fra salg**.  
6.  Vælg knappen **Ja**.  
7.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Produktionsordrer**, og vælg derefter det relaterede link.
8. Åbn den produktionsordre, du lige har oprettet.  

    Bemærk, at feltet **Kildetype** i produktionsordren indeholder **Salgshoved**, og ordren indeholder flere linjer, en for hver salgslinjevare, der skal produceres.  
9. Vælg handlingen **Planlægning**.
10. Vælg handlingen **Opdater** i vinduet **Ordreplanlægning** for at beregne et nyt behov.  

Produktionsordrens ordrehovedlinje vises med alle uopfyldte behovslinjer udvidet under den. Selvom produktionsordren indeholder linjer for flere produktionsvarer, vises det samlede behov for alle produktionsordrelinjer under én ordrehovedlinje i vinduet **Ordreplanlægning**, og det oprindelige kundenavn vises. Du kan nu fortsætte med at planlægge efter behovet som beskrevet i emnet [Planlægge efter nyt behov ordre for ordre](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
>  Linjer i projektproduktionsordren, der har behov for **Prod.ordre** i feltet **Genbestillingssystem**, repræsenterer underliggende produktionsordrer. Når du har oprettet disse produktionsordrer, skal der beregnes en plan vinduet **Ordreplanlægning** for at identificere eventuelle ekspederet komponentbehov for dem. I så fald vises de som behovslinjer under en normal produktionsordrehovedlinje, hvilket betyder, at projektrelationen ikke længere er synlig i vinduet. Men hvis du bruger funktionen til ordresporing, kan du derefter se frem og tilbage i alle forsyningsordrer, der er foretaget under den oprindelige salgsordre.  

## <a name="see-also"></a>Se også
[Planlægning](production-planning.md)   
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)   
[Konfigurere bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

