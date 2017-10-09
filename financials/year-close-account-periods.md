---
title: "Afslutte regnskabsperioder for et regnskabsår | Microsoft Docs"
description: "Beskriver, hvordan du afslutter regnskabsperioder, der indgår i regnskabsåret."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 859801a5e9d9b900aed6af5fe672f650932b2e79
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-close-accounting-periods"></a>Fremgangsmåde: Afslutte regnskabsperioder
Når regnskabsåret er slut, skal du afslutte de perioder, det indeholder.

## <a name="to-close-accounting-periods"></a>Sådan afsluttes regnskabsperioder
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Regnskabsperioder**, og vælg derefter det relaterede link.
2. I vinduet **Regnskabsperioder** skal du vælge handlingen **Afslut år**.

    Hvis mere end et regnskabsår er åbent, vælges det tidligste år, der skal afsluttes, automatisk. Du får vist en meddelelse om, hvilket år der afsluttes, og om konsekvenserne af at afslutte året.
3. For at lukke året skal du trykke på knappen **Ja**.

Regnskabsåret er afsluttet, og felterne **Afsluttet** og **Dato låst** markeres for alle perioder i året. Regnskabsåret kan ikke længere åbnes, og du kan ikke fjerne markeringen fra felterne **Afsluttet** og **Dato låst**.

> [!NOTE]  
>   Det er ikke muligt at afslutte et regnskabsår, før et nyt regnskabsår er oprettet. Bemærk, at når et regnskabsår er afsluttet, er det ikke muligt at ændre startdatoen for det efterfølgende regnskabsår.

Selvom et regnskabsår er afsluttet, kan du stadig bogføre finansposter i det. Hvis du gør det, bliver posterne i forbindelse med bogføringen markeret som bogførte i et afsluttet regnskabsår, og afkrydsningsfeltet **Efterpost** markeres.

Når et regnskabsår er afsluttet, skal du lukke resultatopgørelseskontiene og overføre årets resultat til resultatkontoen i balancen. Du kan gentage dette, hver gang du bogfører i det afsluttede regnskabsår.

## <a name="see-also"></a>Se også
[Afslutningregnskab](year-close-books.md)  
[Fremgangsmåde: Bogføre årsafslutningsposten](year-how-post-year-end-close-entry.md)  
[Fremgangsmåde: Åbne et nyt regnskabsår](finance-how-open-new-fiscal-year.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

