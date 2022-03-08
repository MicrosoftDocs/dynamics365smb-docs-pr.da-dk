---
title: Designoplysninger – Aktive kontra historiske varesporingsposter | Microsoft Docs
description: Når dele af et dokumentlinjeantal er bogført, overføres kun det bestemte antal til vareposter og dets varesporingsnumre. Dog skal du kunne få adgang til alle relevante oplysninger om varesporing direkte fra den aktive bilagslinje. Det vil sige, at du ikke kun vil se de poster, der er relateret til det resterende antal, men du vil også have oplysninger om de enheder, der er bogført. Når du får vist eller redigerer siden **Varesporingslinjer**, vises det samlede indhold af tabellen **Sporingsspecifikation** (T336) og tabellen **Reservationspost** (T337) i en midlertidig version af T336. Dette sikrer, at historiske og aktive varesporingsdata kan åbnes som en.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 6611c6967a89d9a94110d30b0ebdfbe872df2ce8
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788292"
---
# <a name="design-details-active-versus-historic-item-tracking-entries"></a>Designoplysninger: Aktive kontra historiske varesporingsposter
Når dele af et dokumentlinjeantal er bogført, overføres kun det bestemte antal til vareposter og dets varesporingsnumre. Dog skal du kunne få adgang til alle relevante oplysninger om varesporing direkte fra den aktive bilagslinje. Det vil sige, at du ikke kun vil se de poster, der er relateret til det resterende antal, men du vil også have oplysninger om de enheder, der er bogført. Når du får vist eller redigerer siden **Varesporingslinjer**, vises det samlede indhold af tabellen **Sporingsspecifikation** (T336) og tabellen **Reservationspost** (T337) i en midlertidig version af T336. Dette sikrer, at historiske og aktive varesporingsdata kan åbnes som en.  

 Følgende tabel viser, hvordan T336 og T337 bruges i forbindelse med køb. Fede tal repræsenterer værdier, som brugeren indtaster manuelt på siden **Varesporingslinjer**.  

 Trin 1: Opret en indkøbsordrelinje for syv stykker med varesporingsnumre.  

||**Antal (basis)**|**Mgd. at håndtere**|**Fakturer antal (basis)**|**Håndteret antal (basis)**|**Faktureret antal (basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**T337**|7|0|0|0|0|  
|**T336**|0|0|0|0|0|  

 Trin 2: Modtag fire stykker.  

||**Antal (basis)**|**Mgd. at håndtere**|**Fakturer antal (basis)**|**Håndteret antal (basis)**|**Faktureret antal (basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Siden **Varesporingslinjer**|7|**4**|**0**|0|0|  
|**T337**|3|0|0|0|0|  
|**T336**|4|0|0|4|0|  

 Trin 3: Modtag to stykker, og fakturer to stykker.  

||**Antal (basis)**|**Mgd. at håndtere**|**Fakturer antal (basis)**|**Håndteret antal (basis)**|**Faktureret antal (basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Siden **Varesporingslinjer**|7|**2**|**2**|4|0|  
|**T337**|1|0|0|0|0|  
|**T336**|6|0|0|6|2|  

 Trin 4: Modtag ét stykke.  

||**Antal (basis)**|**Mgd. at håndtere**|**Fakturer antal (basis)**|**Håndteret antal (basis)**|**Faktureret antal (basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Siden **Varesporingslinjer**|7|**1**|**0**|6|2|  
|**T336**|7|0|0|7|2|  

 Fakturere 5 styk.  

||**Antal (basis)**|**Mgd. at håndtere**|**Fakturer antal (basis)**|**Håndteret antal (basis)**|**Faktureret antal (basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Siden **Varesporingslinjer**|7|0|**5**|7|2|  
|**T336**|7|0|0|7|7|  

## <a name="see-also"></a>Se også  
 [Designoplysninger: Varesporing](design-details-item-tracking.md)   
 [Designoplysninger: Siden Varesporingslinjer](design-details-item-tracking-lines-window.md)
