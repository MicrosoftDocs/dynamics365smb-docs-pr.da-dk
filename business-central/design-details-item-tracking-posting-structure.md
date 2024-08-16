---
title: Designdetaljer - Bogføringsstruktur for varesporing
description: 'Få at vide, hvordan du bruger vareposter som den primære bærer af varesporingsnumre i bogføringsstruktur for varesporing.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, item tracking, posting, inventory'
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="design-details-item-tracking-posting-structure"></a>Designdetaljer: Bogføringsstruktur for varesporing
Med henblik på at tilpasse lageromkostningsfunktionalitet og for at opnå en enklere og mere stabil løsning bruges vareposter som den primære bærer af varesporingsnumre.  
  
Varesporingsnumre på ordrenetværksenheder og netværksenheder, der ikke er ordrer, er angivet i tabellen **Reservationspost** (T337). Varesporingsnumre, der vedrører historiske oplysninger, er hentet direkte fra de vareposter, der vedrører den pågældende transaktion. Det betyder, at vareposter afspejler varesporingsspecifikation af den bogførte ordrelinje.  
  
Siden **Varesporingslinjer** henter oplysningerne fra T337 og vareposterne og viser dem igennem den midlertidige tabel, **Sporingsspecifikation** (T336). T336 indeholder også midlertidige data i **siden Varesporingslinjer** for varesporingsantal, der mangler at blive faktureret.  
  
## <a name="one-to-many-relation"></a>En til mange-relation
Tabellen **Varepostrelation**, som bruges til at knytte en bogført dokumentlinje til de relaterede vareposter, består af to primære dele:  
  
* En henvisning til den bogførte dokumentlinje, feltet **Ordrelinjenr.**. .  
* Et løbenummer, der peger på en varepost, feltet **Vareløbenr.**.  
  
Funktionaliteten af det eksisterende **Løbenr.**-felt, som vedrører en varepost til en bogført dokumentlinje, håndterer den typiske én til én-relation, når der ikke findes nogen varesporingsnumre på den bogførte bilagslinje. Hvis der findes varesporingsnumre, så er feltet **Løbenr.** tomt, og en-til-mange-relationen håndteres af tabellen **Varepostrelation**. Hvis den bogførte bilagslinje indeholder varesporingsnumre, men kun vedrører en enkelt varepost, vil feltet **Løbenr.** håndtere relationen, og der oprettes ingen post i tabellen **Varepostrelation**.  
  
## <a name="codeunits-80-sales-post--and-90-purch-post"></a>Kodeenhed 80 (Salgsbog) og 90 (Købsbog)
Med henblik på at opdele vareposter ved bogføring indsættes koden i kodeenhed 80 og kodeenhed 90 i løkker, der kører gennem globale, midlertidige postvariabler. Denne kode kalder kodeenhed 22 med en varekladdelinje. Disse variabler er initialiseret, når der findes varesporingsnumre for dokumentlinjen. Denne løkkestruktur bruges altid for at bevare koden enkel. Hvis der ikke findes varesporingsnumre til bilagslinjen, vil en enkelt post indsættes, og løkken køres kun en gang.  
  
## <a name="posting-the-item-journal"></a>Bogføring af varekladden
Varesporingsnumre overføres via de reservationsposter, der vedrører vareposten, og gennemgangen af varesporingsnumre sker i kodeenhed 22 (Varekladdebogslinje). Dette begreb fungerer på samme måde, når en varekladdelinje indirekte bruges til at bogføre et salg eller en indkøbsordre, ligesom når en varekladdelinje bruges direkte. Når varekladden bruges direkte, peger feltet **Kilderække-id** på selve varekladdelinjen.  
  
## <a name="code-unit-22--item-jnl-post-line"></a>Kodeenhed 22 (Varekladde-Boglinje)
Kodeenhed 80 (Salgsbog) og 90 (Købsbog) opretter kald til kodeenhed 22 (Varekladde-Bog-linje) i forbindelse med bogføring af varesporingsnumre og fakturering af eksisterende leverancer eller modtagelser.  
  
Ved antalsbogføring af varesporingsnumre henter kodeenhed 22 (Varekladdebogslinje) varesporingsnumre fra de poster i T337 (Reservationspost), der vedrører bogføringen. Disse poster placeres direkte på varekladdelinjen.  
  
Kodeenhed 22 (Varekladdelinje – Bogf.linje) løber gennem varesporingsnumrene og opdeler bogføringen i de respektive vareposter, der indeholder varesporingsnumrene. Oplysninger om, hvilke vareposter der oprettes, returneres til T337 (reservationspost) ved hjælp af en midlertidig T336-post, som kaldes ved en procedure i kodeenhed 22. Denne procedure udløses, når kodeenhed 22 har afsluttet kørslen, da kodeenhed 22-objektet på dette tidspunkt indeholder oplysninger. Når den midlertidige T336-post hentes, opretter kodeenhed 80 (Salgsbog) og 90 (Købsbog) poster i **tabellen Varepostrelation** for at sammenkæde de oprettede vareposter til den oprettede leverance- eller modtagelseslinje. Kodeenhed 80 (Salgsbog) og 90 (Købsbog) konverterer derefter de midlertidige T336-poster (sporingsspecifikation) til reelle T336-poster (sporingsspecifikation), der er relateret til den pågældende linje. Men konverteringen sker kun, hvis den bogførte bilagslinje ikke er slettet, fordi den er kun delvist bogført.  
  
## <a name="see-also"></a>Se også
[Designoplysninger: Varesporing](design-details-item-tracking.md)   
[Designoplysninger: Design af varesporing](design-details-item-tracking-design.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
