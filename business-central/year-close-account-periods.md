---
title: "Afslutte regnskabsperioder for et regnskabsår | Microsoft Docs"
description: "Beskriver, hvordan du afslutter regnskabsperioder, der indgår i regnskabsåret."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: c8f086e0dc7479ece62ab28b64f9553ba2d13b82
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="close-accounting-periods"></a>Afslutte regnskabsperioder
Når regnskabsåret er slut, skal du afslutte de perioder, det indeholder.

## <a name="to-close-accounting-periods"></a>Sådan afsluttes regnskabsperioder
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Regnskabsperioder**, og vælg derefter det relaterede link.
2. På siden **Regnskabsperioder** skal du vælge handlingen **Afslut år**.

    Hvis mere end et regnskabsår er åbent, vælges det tidligste år, der skal afsluttes, automatisk. Du får vist en meddelelse om, hvilket år der afsluttes, og om konsekvenserne af at afslutte året.
3. For at lukke året skal du trykke på knappen **Ja**.

Regnskabsåret er afsluttet, og felterne **Afsluttet** og **Dato låst** markeres for alle perioder i året. Regnskabsåret kan ikke længere åbnes, og du kan ikke fjerne markeringen fra felterne **Afsluttet** og **Dato låst**.

> [!NOTE]  
>   Det er ikke muligt at afslutte et regnskabsår, før et nyt regnskabsår er oprettet. Bemærk, at når et regnskabsår er afsluttet, er det ikke muligt at ændre startdatoen for det efterfølgende regnskabsår.

Selvom et regnskabsår er afsluttet, kan du stadig bogføre finansposter i det. Hvis du gør det, bliver posterne i forbindelse med bogføringen markeret som bogførte i et afsluttet regnskabsår, og afkrydsningsfeltet **Efterpost** markeres.

Når et regnskabsår er afsluttet, skal du lukke resultatopgørelseskontiene og overføre årets resultat til resultatkontoen i balancen. Du kan gentage dette, hver gang du bogfører i det afsluttede regnskabsår.

## <a name="see-also"></a>Se også
[Afslutningregnskab](year-close-books.md)  
[Bogføre årsafslutningsposten](year-how-post-year-end-close-entry.md)  
[Åbne et nyt regnskabsår](finance-how-open-new-fiscal-year.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

