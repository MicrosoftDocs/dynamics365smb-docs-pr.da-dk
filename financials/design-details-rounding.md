---
title: "Designoplysninger – Afrunding | Microsoft Docs"
description: "Afrunding af restværdier kan opstå, når du værdisætter omkostningerne til en lagerreducering, der måles i et andet antal end den tilsvarende lagerforøgelse. Afrunding af restværdier beregnes for alle kostmetoder, når du udfører kørslen **Juster kostpris – vareposter**."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 39d4bdc430fc74452e7f089c38b28b3214304725
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

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

|Bogføringsdato|Antal|Kostbeløb (faktisk)|Vareløbenr.|Løbenr.|  
|------------------|--------------|----------------------------|---------------------------|---------------|  
|01-01-20|3|10|1|1|  
|02-01-20|-1|-3,33|2|2|  
|03-01-20|-1|-3,34|3|3|  
|04-01-20|-1|-3,33|4|4|  

 For en vare, der bruger en anden kostmetode end Gennemsnitlig, beregnes restværdien ved afrunding (0,01), når det resterende antal for lagerforøgelsen er nul. Restværdien ved afrunding har en separat post (nummer 5).  

 Følgende tabel viser de resulterende værdiposter.  

|Bogføringsdato|Antal|Kostbeløb (faktisk)|Vareløbenr.|Løbenr.|  
|------------------|--------------|----------------------------|---------------------------|---------------|  
|01-01-20|3|10|1|1|  
|02-01-20|-1|-3,33|2|2|  
|03-01-20|-1|-3,33|3|3|  
|04-01-20|-1|-3,33|4|4|  
|01-01-20|0|-0,01|0|5|  

## <a name="see-also"></a>Se også  
 [Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)   
 [Designoplysninger: Omkostningsregulering](design-details-cost-adjustment.md)   
 [Designoplysninger – Kostmetoder](design-details-costing-methods.md) [Administrere lageromkostninger](finance-manage-inventory-costs.md)  
 [Finans](finance.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

