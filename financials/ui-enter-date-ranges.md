---
title: Angive datointervaller i Dynamics 365 for Financials | Microsoft Docs
description: "Få mere at vide om, hvordan du i en rapport kan få vist data fra bestemte tidsperioder, ved at bruge datointervaller i Dynamics 365 for Financials."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 05/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: dc7cd392843ce7c39200bb2331c09cc44c7a394a
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="entering-date-ranges-in-dynamics-365-for-financials"></a>Angive datointervaller i Dynamics 365 for Financials
Du kan angive filtre, der indeholder en startdato og en slutdato for kun at få vist dataene for dette dato- eller tidsinterval. Der gælder særlige regler for den måde, du angiver datointervaller på. Lad os tage **Debitor - top 10** som eksempel:

![Angive et datointerval på anmodningssiden for Debitor - top 10-liste](./media/ui-enter-date-ranges/customer-top10-list.png)

Her kan du begrænse rapporten til et bestemt datointerval, f.eks. de seneste to uger eller i alt 6 uger, eller det interval, du ønsker. Når du vil angive datointervaller, angiver du datoer og bruger enten **..** eller **|** til at vælge intervallet. I eksemplet for at få vist top 10 debitorer i de første to uger i maj, skal du indstille filteret til *01 05 17..14 05 17*.
Her er nogle andre eksempler:

| Betyder | Eksempel | Forklaring |
|---|---|---|
|Lig med| 15 12 16 |Kun dem, der er bogført den 15. december 2016.|
|Interval| 15 12 16..15 17 17<br /><br />..15 12 16|Dem, der er bogført fra den 15. december 2016 til og med 15. januar 2017.<br /><br />Dem, der er bogført den 15. december 2016 eller tidligere.|
|Enten/ eller|15 12 16&#124;16 12 16|Dem, der er bogført enten den 15. december eller 16. december 2016. Hvis der er bogført poster på begge dage, vises de ikke.|

Du kan også kombinere de forskellige formattyper.

| Eksempel | Forklaring |
|---|---|
|15 12 16&#124;01 12 16..31 05 17 | Poster, som er bogført enten den 15. december 2016 eller på datoen fra den 1. december 2016 til og med den 31. maj 2017. |
|..14 12 16&#124;30 12 16.. | Poster bogført den 14. december eller tidligere, eller poster bogført den 30. december eller tidligere - dvs. alle poster undtagen dem, der er bogført på datoer mellem og inklusive den 15. og 29. december. |

Bemærk, at vi har brugt det amerikanske format MMDDYY her. Efterhånden som [!INCLUDE[d365fin](includes/d365fin_md.md)] bliver tilgængeligt på andre markeder, du vil kunne bruge de formater, som du plejer.

## <a name="see-also"></a>Se også
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Indtaste kriterier i filtre ](ui-enter-criteria-filters.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)

