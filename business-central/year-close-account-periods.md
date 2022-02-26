---
title: Afslutte regnskabsperioder for et regnskabsår
description: Beskriver, hvordan du afslutter regnskabsperioder, der indgår i regnskabsåret ved årsafslutningen.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.search.form: 100
ms.date: 06/25/2021
ms.author: jswymer
ms.openlocfilehash: 44f7b577855f1df9967fd59bee5148d9ec06d087
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/14/2022
ms.locfileid: "7973728"
---
# <a name="close-accounting-periods"></a>Afslutte regnskabsperioder

Når regnskabsåret er slut, skal du afslutte de perioder, det indeholder.

## <a name="to-close-accounting-periods"></a>Sådan afsluttes regnskabsperioder

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Regnskabsperioder**, og vælg derefter det relaterede link.
2. På siden **Regnskabsperioder** skal du vælge handlingen **Afslut år**.

    Hvis mere end et regnskabsår er åbent, vælges det tidligste år, der skal afsluttes, automatisk. Du får vist en meddelelse om, hvilket år der afsluttes, og om konsekvenserne af at afslutte året.
3. For at lukke året skal du trykke på knappen **Ja**.

Regnskabsåret er afsluttet, og felterne **Afsluttet** og **Dato låst** markeres for alle perioder i året. Regnskabsåret kan ikke længere åbnes, og du kan ikke fjerne markeringen fra felterne **Afsluttet** og **Dato låst**.

> [!NOTE]  
> Det er ikke muligt at afslutte et regnskabsår, før et nyt regnskabsår er oprettet. Bemærk, at når et regnskabsår er afsluttet, er det ikke muligt at ændre startdatoen for det efterfølgende regnskabsår.

Selvom et regnskabsår er afsluttet, kan du stadig bogføre finansposter i det. Hvis du gør det, bliver posterne i forbindelse med bogføringen markeret som bogførte i et afsluttet regnskabsår, og afkrydsningsfeltet **Efterpost** markeres.

Når et regnskabsår er afsluttet, skal du lukke resultatopgørelseskontiene og overføre årets resultat til resultatkontoen i balancen. Du kan gentage dette, hver gang du bogfører i det afsluttede regnskabsår.

## <a name="see-also"></a>Se også

[Afslutningregnskab](year-close-books.md)  
[Bogføre årsafslutningsposten](year-how-post-year-end-close-entry.md)  
[Arbejd med regnskabsperioder og regnskabsår](finance-accounting-periods-and-fiscal-years.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]