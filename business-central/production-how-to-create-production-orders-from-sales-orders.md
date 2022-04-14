---
title: Oprette produktionsordrer fra salgsordrer
description: Flere oplysninger om at oprette produktionsordrer på forskellige måder til producerede varer direkte fra salgsordrer.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 99000883, 99000884
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: 5f24ee7b1e5fab2b54e9653e6bc98cfd87200770
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8516818"
---
# <a name="create-production-orders-from-sales-orders"></a>Oprette produktionsordrer fra salgsordrer
Du kan oprette produktionsordrer til producerede varer direkte fra salgsordrer.  

## <a name="to-create-a-production-order-from-a-sales-order"></a>Sådan oprettes en produktionsordre fra en salgsordre  

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
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
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
