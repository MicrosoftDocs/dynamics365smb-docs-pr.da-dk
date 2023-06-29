---
title: Designoplysninger – Design af varesporing
description: 'I dette emne beskrives designet bag varesporing i Business Central, sådan som det har udviklet sig gennem produktversionerne.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, item, tracking, tracing'
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-item-tracking-design"></a><a name="design-details-item-tracking-design"></a>Designoplysninger: Design af varesporing

Varesporing i [!INCLUDE[prod_short](includes/prod_short.md)], der er startet med [!INCLUDE [navnow_md](includes/navnow_md.md)]. Varesporingsfunktionen findes i en separat objektstruktur med komplicerede links til bogførte dokumenter og vareposter, og den er integreret i reservationssystemet, som håndterer reservation, ordresporing og aktionsmeddelelser. Du kan få flere oplysninger i [Designoplysninger: Reservation, ordresporing og aktionsmeddelelser](design-details-reservation-order-tracking-and-action-messaging.md) i designdetaljerne for Forsyningsplanlægning.  

Dette design omfatter varesporingsposter i samlede disponeringsberegninger i hele systemet, herunder planlægning, produktion og logistik. Serie- og lotnumre anvendes til vareposterne for at sikre nem adgang til historiske data i forbindelse med varesporing. Med 2021 udgivelsesbølge 1, omfatter varesporingen i [!INCLUDE [prod_short](includes/prod_short.md)] pakkenumre.  

Med tilføjelsen af serie-, lot- og pakkenumre håndterer reservationssystemet permanente vareattributter, mens det også håndterer periodiske links mellem forsyning og behov i form af ordresporings- og reservationsposter. Et andet træk ved serienumre eller lotnumre sammenlignet med konventionelle reservationsdata er det faktum, at de kan bogføres enten helt eller delvist. Derfor fungerer tabellen **Reservationspost** (T337) nu med en relateret tabel, tabellen **Sporingsspecifikation** (T336), som administrerer og viser en opsummering på tværs af aktive og bogførte varesporingsantal. Du kan finde flere oplysninger i [Designoplysninger: Aktive kontra historiske varesporingsposter](design-details-active-versus-historic-item-tracking-entries.md).  

I følgende diagram beskrives udformningen af varesporingsfunktionen i [!INCLUDE[prod_short](includes/prod_short.md)].  

![Eksempel på flow for varesporing.](media/design_details_item_tracking_design.png "Eksempel på flow for varesporing")  

Objektet til central bogføring er ændret for at håndtere entydig underklassifikation af en bilagslinje i form af serie- eller lotnumre, og særlige relationstabeller er tilføjet for at oprette en-til-mange-relationer mellem bogførte dokumenter og deres opdelte vareposter og værdiposter.  

Kodeenhed 22 **Varekladde – Bogfør linje** opdeler nu bogføringen i overensstemmelse med de varesporingsnumre, der er angivet på dokumentlinjen. Hvert entydigt varesporingsnummer på linjen opretter dets egen varepost for varen. Det betyder, at tilknytningen fra den bogførte dokumentlinje til de tilknyttede vareposter nu er en en-til-mange-relation. Denne relation håndteres af de følgende ordresporingsrelationstabeller.  

|Felt|Beskrivelse|  
|---------------|---------------------------------------|  
|**Varepostrelation** (T6507)|Relaterer afsendte eller modtagne linjer til vareposter|  
|**Værdipostrelation** (T6508)|Relaterer fakturerede linjer til værdiposter|  

Du kan finde flere oplysninger i [Designoplysninger: Bogføringsstruktur for varesporing](design-details-item-tracking-posting-structure.md).  

## <a name="see-also"></a><a name="see-also"></a>Se også

[Designoplysninger: Varesporing](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]  
