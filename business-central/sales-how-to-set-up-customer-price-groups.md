---
title: Oprette debitorprisgrupper
description: Se, hvordan du opretter debitorprisgrupper og opretter salgspriser for disse grupper.
author: jill-kotel-andersson
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer price groups, discounts, sales prices
ms.date: 09/30/2021
ms.author: edupont
ms.openlocfilehash: 9b2ff8cca6abf8c1f849039deff5a441427bf112
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8143136"
---
# <a name="set-up-customer-price-groups"></a>Oprette debitorprisgrupper
  
Salgspriser kan gøres afhængige af de debitorgrupper, du sælger til. Disse kaldes debitorprisgrupper.

Før du opsætter debitorprisgrupper, skal du afgøre, hvor mange grupper der skal være, og hvilke kunder der skal høre til de enkelte grupper.  

## <a name="how-to-create-sales-prices-for-a-group-of-customers"></a>Sådan oprettes salgspriser for en gruppe debitorer  

Når du har aftalt den pris, en gruppe debitorer skal betale for en bestemt vare, kan du registrere aftaler for de enkelte varer på linjerne på siden **Salgspriser**.

### <a name="to-create-sales-prices-for-a-group-of-customers"></a>Sådan oprettes salgspriser for en gruppe debitorer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Debitorprisgrupper**, og vælg derefter det relaterede link.  

2. Vælg linjen for den aktuelle debitorprisgruppe. Hvis der ikke allerede findes en linje, kan du oprette en ny linje. Vælg **ny** for at oprette en ny enhed og give det et navn.  
    
    For den valgte linje skal du kontrollere indholdet i felterne **Tillad linjerabat.**, **Tillad fakturarabat**, **Pris inkl moms** og **Momsvirks.bogf.gruppe (pris)**. 
  
3. Vælg handlingen **Naviger**, og vælg **Salgspriser**. Siden **Salgspriser** åbnes. feltet **Salgstype** udfyldes med **debitorprisgruppen**.  
  
4. Udfyld **Salgskode** med den Salgskode, du har valgt på forrige side.  
  
5. Udfyld felterne på linjerne med **Varenr.**, **vareenhedskode** og den aftalte **enhedspris**. Du kan også få vist kolonnen **Variantkode** og angive **Variantkoden**, hvis der er flere varianter af varen.  
  
6. Hvis debitorgruppen skal købe et minimumsantal for at opnå den aftalte pris, skal du udfylde feltet **Min. antal**.  

7. Angiv evt. **Startdato** og **Slutdato** for prisaftalen.  
  
8. Hvis det er relevant, kan du også **Valutakode**.

Gentag trin 4-8 for hver vare, som du vil oprette salgspriser for.

## <a name="how-to-enter-customer-price-group-codes-on-customer-cards"></a>Sådan angives debitorprisgruppekoder på debitorkort  

Når du har oprettet debitorprisgrupperne, kan du angive debitorprisgruppekoder på debitorkortene.

### <a name="to-enter-customer-price-group-codes-on-a-customer-card"></a>Sådan angives debitorprisgruppekoder på et debitorkort  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.  

2. Åbn det relevante **Debitorkort** for en debitor, der skal være en del af en debitorprisgruppe.  

3. I oversigtspanelet **Fakturering** skal du i feltet **Debitorprisgruppe** åbne koden **Debitorprisgruppe** .  


## <a name="see-also"></a>Se også

[Registrere specialsalgspriser og -rabatter](sales-how-record-sales-price-discount-payment-agreements.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
