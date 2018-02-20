---
title: "Designoplysninger – Vinduet Varesporingslinjer | Microsoft Docs"
description: "Læs om, hvordan du styrer strømmen af serienumre og lotnumre på lageret."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, item, tracking, serial number, lot number
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 62070ef4e580a3bd665130c9b017bf164bbe2142
ms.contentlocale: da-dk
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-item-tracking-lines-window"></a>Designoplysninger: Vinduet Varesporingslinjer
Varesporingsposter og reservationsposter oprettes i reservationssystemet, og deres tilgængelighed beregnes dynamisk. Data, der er angivet i vinduet **Varesporingslinjer**, styres i en midlertidig version af tabellen **Sporingsspecifikation**. Når vinduet lukkes, bliver de aktive data bundet til tabellen **Reservationspost**, og de historiske data bliver bundet til tabellen **Sporingsspecifikation**. Du kan finde flere oplysninger i [Designoplysninger: Aktive kontra historiske varesporingsposter](design-details-active-versus-historic-item-tracking-entries.md).  
  
Opslag fra felterne **Serienr.** og **Lotnr.** viser tilgængelighed baseret på både tabellen **Varepost** og **Reservationspost**, uden datofilter. Matrixen for mængdefelter i hovedet af vinduet **Varesporingslinjer** viser dynamiske mængder og summer for de varesporingsnumre, der er angivet på linjerne i vinduet. Mængderne skal svare til mængderne på dokumentlinjen, der er angivet med **0** i **Udefineret**-felterne i sidehovedet i vinduet.  
  
For at koordinere flowet af serie- og lotnumre i lageret findes følgende regler for indtastning af data i vinduet **Varesporingslinjer**:  
  
* For hverken indgående eller udgående varesporingslinjer kan du angive et serienummer, med eller uden et lotnummer, flere gange i den samme forekomst af vinduet **Varesporingslinjer**. Hvis du forsøger at indtaste en vilkårlig kombination af serie- eller lotnumre, der allerede er til stede i vinduet, blokerer en fejlmeddelelse dataindtastningen.  
* For indgående varesporingslinjer kan du ikke bogføre det relaterede dokument, hvis en vare af samme variant og med samme serienummer allerede findes på lageret. Hvis du forsøger at bogføre en positiv linje for en lagervare med samme variant og serienummer, blokerer en fejlmeddelelse bogføringen. For både indgående og udgående varesporingslinjer i åbne dokumenter, kan du dog have den samme kombination af serie- eller lotnumre, der vedrører forskellige kildedokumentlinjer, det vil sige, at den findes i forskellige forekomster af vinduet **Varesporingslinjer**, indtil det relaterede dokument bogføres.  
* Hvis varen er indstillet til serienummerspecifik sporing eller lotnummerspecifik sporing, kan du ikke bogføre en udgående dokumentlinje, medmindre en vare med defineret serie- eller lotnummer findes på lageret. Hvis du forsøger at bogføre en udgående dokumentlinje for en lagervare med et serielotnummer, der ikke er i lageret, blokerer en fejlmeddelelse bogføringen.  
  
Regler for indtastning af data i vinduet **Varesporingslinjer** understøtter også de sammensætningsprincipper, der styrer ordresporing, planlægning og reservation. Du kan finde flere oplysninger i [Designoplysninger: Varesporing og planlægning](design-details-item-tracking-and-planning.md).  
  
## <a name="see-also"></a>Se også  
[Designoplysninger: Varesporing](design-details-item-tracking.md)
