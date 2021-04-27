---
title: Designoplysninger – Afrunding | Microsoft Docs
description: Afrunding af restværdier kan opstå, når du værdisætter omkostningerne til en lagerreducering, der måles i et andet antal end den tilsvarende lagerforøgelse. Afrunding af restværdier beregnes for alle kostmetoder, når du udfører kørslen **Juster kostpris – vareposter**.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 78da80b026c29040766cc67d1cd6ad32f74f4bcc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777744"
---
# <a name="design-details-rounding"></a>Designoplysninger: Afrunding
Afrunding af restværdier kan opstå, når du værdisætter omkostningerne til en lagerreducering, der måles i et andet antal end den tilsvarende lagerforøgelse. Afrunding af restværdier beregnes for alle kostmetoder, når du udfører kørslen **Juster kostpris – vareposter**.  

 Når du bruger kostmetoden Gennemsnit, beregnes restværdien ved afrunding og registreres på en akkumuleret post-for-post-basis.  

 Når du bruger en anden kostmetode end Gennemsnit, beregnes restværdien ved afrunding, når lagerforøgelsen er helt udlignet, dvs. når det resterende antal for lagerforøgelsen er lig med nul. Der oprettes så en separat post for restværdi ved afrunding, og bogføringsdatoen på denne afrundingspost er bogføringsdatoen for den seneste fakturerede værdipost for lagerforøgelsen.  

## <a name="example"></a>Eksempel  
 Følgende eksempel illustrerer, hvordan forskellige restværdier ved afrunding håndteres for henholdsvis den gennemsnitlige kostmetode og ikke gennemsnitlige kostmetode. I begge tilfælde skal kørslen **Reguler kostværdi – vareposter** køres.  

 Følgende tabel indeholder de vareposter, som eksemplet er baseret på.  

|Bogføringsdato|Antal|Løbenr.|  
|------------------|--------------|---------------|  
|01-01-20|3|1|  
|02-01-20|-1|2|  
|03-01-20|-1|3|  
|04-01-20|-1|4|  

 For en vare, der bruger kostmetoden Gennemsnit, beregnes restværdien ved afrunding (1/300) med den første reducering (løbenummer 2) og er overført til løbenummer 3. Derfor vurderes løbenummer 3 til -3,34.  

 Følgende tabel viser de resulterende værdiposter.  

|Bogføringsdato|Antal|Kostbeløb (faktisk)|Varepostløbenr.|Løbenr.|  
|------------------|--------------|----------------------------|---------------------------|---------------|  
|01-01-20|3|10|1|1|  
|02-01-20|-1|-3,33|2|2|  
|03-01-20|-1|-3,34|3|3|  
|04-01-20|-1|-3,33|4|4|  

 For en vare, der bruger en anden kostmetode end Gennemsnitlig, beregnes restværdien ved afrunding (0,01), når det resterende antal for lagerforøgelsen er nul. Restværdien ved afrunding har en separat post (nummer 5).  

 Følgende tabel viser de resulterende værdiposter.  

|Bogføringsdato|Antal|Kostbeløb (faktisk)|Varepostløbenr.|Løbenr.|  
|------------------|--------------|----------------------------|---------------------------|---------------|  
|01-01-20|3|10|1|1|  
|02-01-20|-1|-3,33|2|2|  
|03-01-20|-1|-3,33|3|3|  
|04-01-20|-1|-3,33|4|4|  
|01-01-20|0|-0,01|1|5|  

## <a name="see-also"></a>Se også  
 [Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)   
 [Designoplysninger: Omkostningsregulering](design-details-cost-adjustment.md)   
 [Designoplysninger – Kostmetoder](design-details-costing-methods.md) [Administrere lageromkostninger](finance-manage-inventory-costs.md)  
 [Finans](finance.md)  
 [Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]