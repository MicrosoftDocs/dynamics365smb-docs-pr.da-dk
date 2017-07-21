---
title: Opdatere valutakurser | Microsoft Docs
description: Hvis du vil bruge flere forskellige valutaer i virksomheden, skal du angive en kode for hver valuta og bruge en ekstern valutakurstjeneste, som Yahoo.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, Yahoo
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: cc60569091b3aa37d17e981f1fae8f46c4a004df
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-update-currency-exchange-rates"></a>Fremgangsmåde: Opdatere valutakurser
Du skal oprette koder for hver valuta, du bruger, hvis du foretager køb og salg i andre valutaer end din lokale valuta, eller hvis du registrerer finanstransaktioner i forskellige valutaer.  

> [!NOTE]  
>   Denne funktion kræver, at oplevelsen er indstillet til **Pakke**. Du kan finde flere oplysninger under [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).

Du kan bruge en ekstern tjeneste til at holde dine valutakurser opdaterede. Tjenesten Yahoo Currency Exchange Rates er forudinstalleret og klar til at blive aktiveret.

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Sådan konfigureres en valutakurstjeneste
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Valutakurstjenester**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. I vinduet **Valutakurstjenester** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Marker afkrydsningsfeltet **Aktiveret** for at aktivere tjenesten.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Sådan opdateres valutakurser fra en tjeneste
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Valutaer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Opdater valutakurser**.

Værdien i feltet **Valutakurs** i vinduet **Valutaer** opdateres med den seneste valutakurs.

## <a name="see-also"></a>Se også
[Afslutning af år og perioder](year-close-years-periods.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

