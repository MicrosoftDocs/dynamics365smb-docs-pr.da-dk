---
title: "Fremgangsmåde: Afslutte regnskabsperioder | Microsoft Docs"
description: Beskriver, hvordan du afsluttes regnskabsperioder.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 69bea225084f239523c4ed67471b52ad91e914d9
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-close-accounting-periods"></a>Fremgangsmåde: Afslutte regnskabsperioder
Når regnskabsåret er slut, skal du afslutte de perioder, det indeholder.

## <a name="to-close-accounting-periods"></a>Sådan afsluttes regnskabsperioder
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Regnskabsperioder** og derefter vælge det relaterede link.
2. I vinduet **Regnskabsperioder** skal du vælge handlingen **Afslut år**.

    Hvis mere end et regnskabsår er åbent, vælges det tidligste år, der skal afsluttes, automatisk. Du får vist en meddelelse om, hvilket år der afsluttes, og om konsekvenserne af at afslutte året.
3. For at lukke året skal du trykke på knappen **Ja**.

Regnskabsåret er afsluttet, og felterne **Afsluttet** og **Dato låst** markeres for alle perioder i året. Regnskabsåret kan ikke længere åbnes, og du kan ikke fjerne markeringen fra felterne **Afsluttet** og **Dato låst**.

**Bemærk**: Det er ikke muligt at afslutte et regnskabsår, før et nyt regnskabsår er oprettet. Bemærk, at når et regnskabsår er afsluttet, er det ikke muligt at ændre startdatoen for det efterfølgende regnskabsår.

Selvom et regnskabsår er afsluttet, kan du stadig bogføre finansposter i det. Hvis du gør det, bliver posterne i forbindelse med bogføringen markeret som bogførte i et afsluttet regnskabsår, og afkrydsningsfeltet **Efterpost** markeres.

Når et regnskabsår er afsluttet, skal du lukke resultatopgørelseskontiene og overføre årets resultat til resultatkontoen i balancen. Du kan gentage dette, hver gang du bogfører i det afsluttede regnskabsår.

## <a name="see-also"></a>Se også
[Afslutningregnskab](year-close-books.md)  
[Fremgangsmåde: Bogføre årsafslutningsposten](year-how-post-year-end-close-entry.md)  
[Fremgangsmåde: Åbne et nyt regnskabsår](finance-how-open-new-fiscal-year.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

