---
title: "Datoberegning for køb | Microsoft Docs"
description: "Programmet beregner automatisk den dato, hvor du skal bestille en vare for at have den på lager på en bestemt dato. Dette er den dato, du kan forvente, at varer, der er bestilt på en bestemt dato, er disponible til pluk."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7e569474e3d222a56500665fa73408f47480f338
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="date-calculation-for-purchases"></a>Beregning af forfaldsdato for køb
[!INCLUDE[d365fin](includes/d365fin_md.md)] beregner automatisk den dato, hvor du skal bestille en vare for at have den på lager på en bestemt dato. Dette er den dato, du kan forvente, at varer, der er bestilt på en bestemt dato, er disponible til pluk.  

Hvis du angiver en ønsket modtagelsesdato på et købsordrehoved, er den beregnede ordredato den dato, hvor ordren skal være placeret for at modtage varerne på den dato, du har anmodet om. Derefter beregnes den dato, hvor varerne er disponible til pluk, og datoen indsættes i feltet **Forventet modt.dato**.  

Hvis du ikke indtaster en ønsket modtagelsesdato, er det ordredatoen på linjen, der bruges som udgangspunkt for beregning af den dato, hvor du kan forvente at modtage varerne samt datoen, hvor varerne er disponible til plukning.  

## <a name="calculating-with-a-requested-receipt-date"></a>Beregning med en ønsket modtagelsesdato  
Hvis der står en ønsket modtagelsesdato på købslinjen, bruges denne dato som udgangspunkt for følgende beregninger.  

- Ønsket modtagelsesdato - Leveringstidsberegning = Ordredato  
- Ønsket modtagelsesdato + Indgående lagerekspeditionstid + Sikkerhedstid = Forventet modtagelsesdato  

Hvis du har indtastet en ønsket modtagelsesdato på købsordrehovedet, kopieres denne dato til det tilsvarende felt på alle ordrelinjerne. Du kan ændre eller fjerne datoen på en eller flere linjer.  

## <a name="calculating-without-a-requested-delivery-date"></a>Beregning uden en ønsket leveringsdato  
Hvis du angiver en købslinje uden en ønsket leveringsdato, udfyldes feltet **Ordredato** automatisk med datoen fra feltet **Ordredato** på købshovedet. Denne dato kan enten være en indtastet dato eller arbejdsdatoen. Med ordredatoen som udgangspunkt beregnes følgende datoer derefter automatisk til købsordrelinjen.  

- Ordre dato + Leveringstidsberegning = Planlagt modtagelsesdato  
- Planlagt modtagelsesdato + Indgående lagerekspeditionstid + Sikkerhedstid = Forventet modtagelsesdato  

Hvis du ændrer ordredato på linjen, f.eks. når varerne ikke er disponible hos din leverandør før på en senere dato, genberegnes de relevante datoer på linjen automatisk.  

Hvis du ændrer ordredatoen på hovedet, kopieres denne dato til feltet **Ordredato** på alle linjerne, og alle relaterede datofelter genberegnes derefter.  

## <a name="see-also"></a>Se også  
 [Beregning af forfaldsdato for salg](sales-date-calculation-for-sales.md)   
 [Sådan beregnes ordrebekræftelsesdatoer](sales-how-to-calculate-order-promising-dates.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

