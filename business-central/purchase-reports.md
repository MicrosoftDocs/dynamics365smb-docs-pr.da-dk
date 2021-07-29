---
title: Købsrapporter og analyser
description: Se, hvilke købsrapporter og analyser der er tilgængelige i standardversionen af Business Central, så du kan holde styr på virksomheden.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 3f818e556b2ebe3f50189b0057f1302a5598d904
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543166"
---
# <a name="purchase-reports-and-analytics-in-business-central"></a>Købsrapporter og analyser i Business Central

Købsrapportering i [!INCLUDE [prod_short](includes/prod_short.md)] gør det muligt for indkøbs-og erhvervs medarbejdere at få indsigt i og statistikker om aktuelle og tidligere montageaktiviteter.  

## <a name="reports"></a>Rapporter

I følgende tabel beskrives nogle af nøglerapporterne i købsrapporter.

|Report |Objekt-id|Beskrivlse  |
|---------|---------|---------|
|**Købsstatistikker**|312|[!INCLUDE [reports-purchase-statistics](includes/reports-purchase-statistics.md)]|
|**Kreditor - top 10-liste**|311|Viser oplysninger om køb fra kreditorerne inden for en valgt periode. Du kan bestemme antallet af kreditorer, der skal med i rapporten.<br>Kreditorerne sorteres efter beløb, og du kan vælge, om beløbene i rapporten skal sorteres efter køb fra kreditorerne eller efter kreditorernes saldo. Rapporten giver et hurtigt overblik over, hvilke kreditorer du skylder mest eller køber mest hos.|
|**Kreditorvarekatalog** eller **vare/kreditorkatalog**|320 eller 720|Viser en oversigt over kreditorer for de valgte varer eller varer for de valgte kreditorer. Der vises oplysninger om købspris, beregning af leveringstid og leverandørers varenummer.<br>I USA, Canada og Mexico er denne rapport ikke tilgængelig. Brug i stedet rapporten **vare/leverandørkatalog** (10164).|
|**Kreditor/varekøb**|313|Viser en liste over poster for hver enkelt kreditor for en valgt periode. Rapporten viser oplysninger om faktureret antal, beløb og eventuel rabat. Rapporten kan f.eks. bruges, når virksomhedens varekøb skal analyseres og til at vise, om der er sammenhæng mellem rabat og varekøb.|
|**Lagerbeholdsudgift og prisliste**|716|Viser en oversigt over prisoplysninger om de valgte varer eller lagervarer: købspris, sidste købspris, salgspris, avanceprocent og avance.|
|**Lagerbeholdning - tilgængelighedsplan**|707|Hvis du vil have en oversigt over specifikke varer/lagervarer og deres tilgængelighed. Denne rapport viser akkumulerede værdier som f. eks. bruttobehov, planlagte tilgange, lager osv. |
|**Vare/leverandørkøb**|714|Viser en liste over de leverandører, virksomheden har indkøbt varer hos i den valgte periode. Der vises oplysninger om faktureret antal, beløb og rabat. Rapporten kan bruges til analyse af virksomhedens varekøb.|
|**Varer i købsordrer**|709|Viser en oversigt over varer, der er bestilt hos leverandører. Den indeholder også oplysninger om forventet modtagelsesdato og restordrer i antal og beløb. Rapporten kan f.eks. bruges til at give et overblik over det forventede leveringstidspunkt for varerne og om der skal rykkes for restordrer.|
|**Disponibel købsreservation**|409|Viser hvilke varer der er disponible til levering på købsdokumenter, f.eks. returordrer. Du angiver, om rapporten skal vise status på hvert dokument eller på hver købslinje. <br>Når du udskriver rapporten, kan du automatisk få indsat det antal, der kan leveres, i feltet **Modtag (antal)** på købslinjerne. Feltet **Modtag (antal)** viser leveringsantallet på købskreditnotaer eller negative købsordrelinjer. Derefter kan rapporten bruges til at afgøre, hvilke dokumenter der skal leveres. **Bemærk**: Denne funktionalitet er ikke tilgængelig for avancerede lagerfunktioner.|
<!--|**Forfaldne debitorposter**|11006| DACH-specifik: en rapport, som kan bruges af teamlederen hos den indkøbte afdeling, som det er regnskabet. Her kan du få et overblik over de ubetalte kreditorfakturaer, herunder forfaldsdatoer, valutaer og beløb. Basis er de åbne kreditorposter.| -->




## <a name="tasks"></a>Opgaver

I følgende artikler beskrives nogle af de vigtigste opgaver i forbindelse med analyse af virksomhedens tilstand:

* [Oprette analyserapporter](bi-how-create-analysis-views-reports.md)  
* [Vise varedisponering](inventory-how-availability-overview.md)  


## <a name="see-also"></a>Se også

[Opsætning af indkøb](purchasing-setup-purchasing.md)  
[Køb](purchasing-manage-purchasing.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
