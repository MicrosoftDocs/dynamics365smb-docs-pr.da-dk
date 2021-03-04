---
title: Designoplysninger – Design af varesporing | Microsoft Docs
description: I dette emne beskrives designet bag varesporing i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, tracing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 87c85de9f501e093679512b709841d0027fe17bf
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751326"
---
# <a name="design-details-item-tracking-design"></a>Designoplysninger: Design af varesporing
I den første version af Varesporing i [!INCLUDE[prod_short](includes/prod_short.md)] 2.60 er serie- eller lotnumre registreret direkte i vareposter. Dette design leverede komplette tilgængelighedsoplysninger og simpel sporing af historiske poster, men det manglede fleksibilitet og funktionalitet.  

Fra [!INCLUDE[prod_short](includes/prod_short.md)] 3.00 fandtes varesporingsfunktionen i en separat objektstruktur med komplicerede links til bogførte dokumenter og vareposter. Dette design var fleksibelt og omfattende i funktionalitet, men varesporingsposter var ikke fuldt inddraget i disponeringsberegningerne.  

Siden [!INCLUDE[prod_short](includes/prod_short.md)] 3.60 er varesporingsfunktionen integreret med reservationssystemet, som håndterer reservation, ordresporing og aktionsmeddelelser. Hvis du ønsker yderligere oplysninger, kan du se "Designoplysninger: Reservation, ordresporing og aktionsmeddelelser" i "Designoplysninger: Forsyningsplanlægning".  

Dette seneste design omfatter varesporingsposter i samlede disponeringsberegninger i hele systemet, herunder planlægning, produktion og logistik. Det gamle ide med at overføre serie- og lotnumre på vareposterne introduceres igen for at sikre nem adgang til historiske data af varesporingsformål. I forbindelse med varesporingsforbedringer i [!INCLUDE[prod_short](includes/prod_short.md)] 3.60 blev reservationssystemet udvidet til ikke-ordrenetværksenheder som kladder, fakturaer og kreditnotaer.  

Med tilføjelsen af serie- eller lotnumre håndterer reservationssystemet permanente vareattributter, mens der også håndteres periodiske links mellem forsyning og behov i form af ordresporings- og reservationsposter. Et andet træk ved serienumre eller lotnumre sammenlignet med konventionelle reservationsdata er det faktum, at de kan bogføres enten helt eller delvist. Derfor fungerer tabellen **Reservationspost** (T337) nu med en relateret tabel, tabellen **Sporingsspecifikation** (T336), som administrerer og viser en opsummering på tværs af aktive og bogførte varesporingsantal. Du kan finde flere oplysninger i [Designoplysninger: Aktive kontra historiske varesporingsposter](design-details-active-versus-historic-item-tracking-entries.md).  

I følgende diagram beskrives udformningen af varesporingsfunktionen i [!INCLUDE[prod_short](includes/prod_short.md)].  

![Eksempel på flow for varesporing](media/design_details_item_tracking_design.png "Eksempel på flow for varesporing")  

Objektet til central bogføring er ændret for at håndtere entydig underklassifikation af en bilagslinje i form af serie- eller lotnumre, og særlige relationstabeller er tilføjet for at oprette en-til-mange-relationer mellem bogførte dokumenter og deres opdelte vareposter og værdiposter.  

Kodeenhed 22 **Varekladde – Bogfør linje** opdeler nu bogføringen i overensstemmelse med de varesporingsnumre, der er angivet på dokumentlinjen. Hvert entydigt varesporingsnummer på linjen opretter dets egen varepost for varen. Det betyder, at tilknytningen fra den bogførte dokumentlinje til de tilknyttede vareposter nu er en en-til-mange-relation. Denne relation håndteres af de følgende ordresporingsrelationstabeller.  

|Felt|Beskrivelse|  
|---------------|---------------------------------------|  
|**Varepostrelation** (T6507)|Relaterer afsendte eller modtagne linjer til vareposter|  
|**Værdipostrelation** (T6508)|Relaterer fakturerede linjer til værdiposter|  

Du kan finde flere oplysninger i [Designoplysninger: Bogføringsstruktur for varesporing](design-details-item-tracking-posting-structure.md).  

## <a name="see-also"></a>Se også  
[Designoplysninger: Varesporing](design-details-item-tracking.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]