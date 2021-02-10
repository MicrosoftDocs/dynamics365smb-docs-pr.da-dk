---
title: Datoberegning for køb | Microsoft Docs
description: Programmet beregner automatisk den dato, hvor du skal bestille en vare for at have den på lager på en bestemt dato. Dette er den dato, du kan forvente, at varer, der er bestilt på en bestemt dato, er disponible til pluk.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 22153df1e56d274256b53d426e2dff30cad3e4bc
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758588"
---
# <a name="date-calculation-for-purchases"></a>Beregning af forfaldsdato for køb

[!INCLUDE[prod_short](includes/prod_short.md)] beregner automatisk den dato, hvor du skal bestille en vare for at have den på lager på en bestemt dato. Dette er den dato, du kan forvente, at varer, der er bestilt på en bestemt dato, er disponible til pluk.  

Hvis du angiver en ønsket modtagelsesdato på et købsordrehoved, er den beregnede ordredato den dato, hvor ordren skal være placeret for at modtage varerne på den dato, du har anmodet om. Derefter beregnes den dato, hvor varerne er disponible til pluk, og datoen indsættes i feltet **Forventet modt.dato**.  

Hvis du ikke indtaster en ønsket modtagelsesdato, er det ordredatoen på linjen, der bruges som udgangspunkt for beregning af den dato, hvor du kan forvente at modtage varerne samt datoen, hvor varerne er disponible til plukning.  

## <a name="calculating-with-a-requested-receipt-date"></a>Beregning med en ønsket modtagelsesdato

Hvis der står en ønsket modtagelsesdato på købslinjen, bruges denne dato som udgangspunkt for følgende beregninger.  

- Ønsket modtagelsesdato - Leveringstidsberegning = Ordredato  
- Ønsket modtagelsesdato + Indgående lagerekspeditionstid + Sikkerhedstid = Forventet modtagelsesdato  

Hvis du har indtastet en ønsket modtagelsesdato på købsordrehovedet, kopieres denne dato til det tilsvarende felt på alle ordrelinjerne. Du kan ændre eller fjerne datoen på en eller flere linjer.  

> [!NOTE]
> Hvis processen er baseret på bagudrettet beregning, f.eks. hvis du bruger den ønskede modtagelsesdato til at hente ordredatoen, anbefales det, at du bruger datoformler med faste varigheder, f.eks. "5D" for fem dage eller "1U" for én uge. Datoformler uden faste varigheder, f.eks. "AU" for aktuelle uge eller AM for den aktuelle måned, kan resultere i forkerte datoberegninger. Du kan finde flere oplysninger om datoformler i [Arbejde med kalenderdatoer og-klokkeslæt](ui-enter-date-ranges.md).

## <a name="calculating-without-a-requested-delivery-date"></a>Beregning uden en ønsket leveringsdato

Hvis du angiver en købslinje uden en ønsket leveringsdato, udfyldes feltet **Ordredato** automatisk med datoen fra feltet **Ordredato** på købshovedet. Denne dato kan enten være en indtastet dato eller arbejdsdatoen. Med ordredatoen som udgangspunkt beregnes følgende datoer derefter automatisk til købsordrelinjen.  

- Ordre dato + Leveringstidsberegning = Planlagt modtagelsesdato  
- Planlagt modtagelsesdato + Indgående lagerekspeditionstid + Sikkerhedstid = Forventet modtagelsesdato  

Hvis du ændrer ordredato på linjen, f.eks. når varerne ikke er disponible hos din leverandør før på en senere dato, genberegnes de relevante datoer på linjen automatisk.  

Hvis du ændrer ordredatoen på hovedet, kopieres denne dato til feltet **Ordredato** på alle linjerne, og alle relaterede datofelter genberegnes derefter.  

## <a name="default-values-for-lead-time-calculation"></a>Standardværdier for beregning af leveringstid

[!INCLUDE[prod_short](includes/prod_short.md)] bruger værdien fra feltet **Leveringstid** på købsordrelinjen til at beregne ordren og de forventede modtagelsesdatoer.  

Du kan angive værdien på linjen manuelt eller lade programmet bruge værdier, der er defineret på kreditorkortet, varekortet, lagervarekortet eller vare/leverandør-kataloget.
Men værdien af leveringstiden på kreditorkortet bruges kun, hvis der ikke er angivet en leveringsperiode på varekortet, lagervarekortet eller vare/leverandør-kataloget for varen. Dette er også den prioriterede rækkefølge for disse værdier. Hvis de alle er angivet, har leveringstiden fra kreditorkortet den laveste prioritet, og leveringstiden fra vare/leverandør-kataloget har den højeste prioritet.  

## <a name="see-also"></a>Se også

[Beregning af forfaldsdato for salg](sales-date-calculation-for-sales.md)   
[Beregne ordrebekræftelsesdatoer](sales-how-to-calculate-order-promising-dates.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
