---
title: Designoplysninger - Siden Varesporingslinjer
description: 'Læs om, hvordan du styrer strømmen af serienumre og lotnumre på lageret ved hjælp af varesporingslinjer.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, inventory, item, tracking, serial number, lot number'
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Designoplysninger: Siden Varesporingslinjer
Varesporingsposter og reservationsposter oprettes i reservationssystemet, og deres tilgængelighed beregnes dynamisk. Data, der er angivet på siden **Varesporingslinjer**, styres i en midlertidig version af tabellen **Sporingsspecifikation**. Når siden lukkes, bliver de aktive data bundet til tabellen **Reservationspost**, og de historiske data bliver bundet til tabellen **Sporingsspecifikation**. Du kan finde flere oplysninger i [Designoplysninger: Aktive kontra historiske varesporingsposter](design-details-active-versus-historic-item-tracking-entries.md).  
  
Opslag fra felterne **Serienr.** og **Lotnr.** viser tilgængelighed baseret på både tabellen **Varepost** og **Reservationspost**, uden datofilter. Matrixen for mængdefelter i hovedet af siden **Varesporingslinjer** viser dynamiske mængder og summer for de varesporingsnumre, der er angivet på linjerne på siden. Mængderne skal svare til mængderne på dokumentlinjen, der er angivet med **0** i **Udefineret**-felterne i sidehovedet på siden.  
  
For at koordinere flowet af serie- og lotnumre i lageret findes følgende regler for indtastning af data på siden **Varesporingslinjer**:  
  
* For hverken indgående eller udgående varesporingslinjer kan du angive et serienummer, med eller uden et lotnummer, flere gange i den samme forekomst af siden **Varesporingslinjer**. Hvis du forsøger at indtaste en vilkårlig kombination af serie- eller lotnumre, der allerede er til stede på siden, blokerer en fejlmeddelelse dataindtastningen.  
* For indgående varesporingslinjer kan du ikke bogføre det relaterede dokument, hvis en vare af samme variant og med samme serienummer allerede findes på lageret. Hvis du forsøger at bogføre en positiv linje for en lagervare med samme variant og serienummer, blokerer en fejlmeddelelse bogføringen. For både indgående og udgående varesporingslinjer i åbne dokumenter, kan du dog have den samme kombination af serie- eller lotnumre, der vedrører forskellige kildedokumentlinjer, det vil sige, at den findes i forskellige forekomster af siden **Varesporingslinjer**, indtil det relaterede dokument bogføres.  
* Hvis varen er indstillet til serienummerspecifik sporing eller lotnummerspecifik sporing, kan du ikke bogføre en udgående dokumentlinje, medmindre en vare med defineret serie- eller lotnummer findes på lageret. Hvis du forsøger at bogføre en udgående dokumentlinje for en lagervare med et serielotnummer, der ikke er i lageret, blokerer en fejlmeddelelse bogføringen.  
  
Regler for indtastning af data på siden **Varesporingslinjer** understøtter også de sammensætningsprincipper, der styrer ordresporing, planlægning og reservation. Du kan finde flere oplysninger i [Designoplysninger: Varesporing og planlægning](design-details-item-tracking-and-planning.md).  
  
## Se også  
[Designoplysninger: Varesporing](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]