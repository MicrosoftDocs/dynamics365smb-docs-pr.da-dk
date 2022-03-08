---
title: Oprette produktionsordrer fra salgsordrer
description: Du kan oprette produktionsordrer fra salgsordrer
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/28/2021
ms.author: edupont
ms.openlocfilehash: 438f4d4e1833ba607ceedb9f5d9450c0a4dbb680
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115232"
---
# <a name="create-production-orders-from-sales-orders"></a>Oprette produktionsordrer fra salgsordrer
Du kan oprette produktionsordrer til producerede varer direkte fra salgsordrer.  

## <a name="to-create-a-production-order-from-a-sales-order"></a>Sådan oprettes en produktionsordre fra en salgsordre  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordre**, og vælg derefter det relaterede link.  
2.  Vælg den salgsordre, du vil oprette en produktionsordre for.  
3.  Vælg handlingen **Planlægning**. På siden **Salgsordreplanlægning** kan du få vist disponeringen for en salgsordrevare.  
4.  Vælg handlingen **Opret prod.ordre**.  
5.  Vælg status og ordretype.  
6.  Klik på knappen **Ja** for at oprette en eller flere produktionsordrer til de linjer, der har **produktionsordre** i feltet **Genbestillingssystem**.


> [!NOTE]  
> Linjer i den oprettede projektproduktionsordre, der har behov for **Prod.ordre** i feltet **Genbestillingssystem**, repræsenterer underliggende produktionsordrer. Når du har oprettet disse produktionsordrer, skal du huske at identificere eventuelle ekspederet komponentbehov for dem ved hjælp af siden **Ordreplanlægning** eller funktionen **Omplanlæg** fra oprettede ordrer. 

## <a name="order-type"></a>Ordretype  
Du kan vælge mellem to måder at oprette produktionsordrer på, som beskrevet i følgende tabel.

|Indstilling|Beskrivelse|
|------|-----------|
|Vareordre|En produktionsordre oprettes for hver enkelt behov produktionsordre, der repræsenteres af a linje i vinduet **Salgsordreplanlægning**.|
|Projektordre|En produktionsordre oprettes for hver enkelt produktionsordre, der repræsenteres af en linje i vinduet **Salgsordreplanlægning**. |

Når du bruger projektordrer, indeholder feltet **Kildetype** i produktionsordren **Salgshoved**, og ordren indeholder flere linjer, en for hver salgslinjevare, der skal produceres.  


## <a name="see-also"></a>Se også  
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)   
[Konfigurere bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
