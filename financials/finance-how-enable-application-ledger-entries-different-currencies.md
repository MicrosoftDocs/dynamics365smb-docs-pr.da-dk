---
title: Udligne poster i forskellige valutaer | Microsoft Docs
description: "Du kan udligne finansposter i flere valutaer, f.eks. hvis du sælger i én valuta og modtager betaling i en anden."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 035f4c0e98e3b7ba308319c2017568de832e26c5
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-enable-application-of-ledger-entries-in-different-currencies"></a>Fremgangsmåde: Muliggøre udligning af finansposter i forskellige valutaer
Hvis du køber varer fra en leverandør i én valuta, men foretager betaling i en anden valuta, kan du udligne betalingen med købet.

Ligeledes, hvis du sælger til en debitor i en valuta og modtager betaling i en anden, kan du knytte betalingen til salgsfakturaen.

Følgende procedure beskriver, hvordan du kan angive dette for kreditorposter i vinduet **Købsopsætning**. Der er tilsvarende opsætning for debitorposter i vinduet **Salgsopsætning**.

> [!NOTE]  
>   Denne funktion kræver, at oplevelsen er indstillet til **Pakke**. Du kan finde flere oplysninger under [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a>Sådan aktiveres udligning af kreditorposter i forskellige valutaer
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Købsopsætning**, og vælg derefter det relaterede link.
2. Vælg en af følgende indstillinger i feltet **Valutaudligning**.

| Indstilling | Beskrivelse |
| --- | --- |
| Ingen |Udligning mellem valutaer er ikke tilladt. |
| ØMU |Udligning mellem ØMU-valutaer er tilladt. |
| Alle |Udligning mellem alle valutaer er tilladt. |

## <a name="see-also"></a>Se også
[Administrere skyldige beløb](payables-manage-payables.md)  
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

