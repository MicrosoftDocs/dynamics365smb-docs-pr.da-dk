---
title: Designdetaljer – Bogføringsstruktur for varesporing | Microsoft Docs
description: Få at vide, hvordan du bruger vareposter som den primære bærer af varesporingsnumre.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item tracking, posting, inventory
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: a016863dc7dd5667074060a21e352ce4a56444cd
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2019
ms.locfileid: "2880156"
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
  
## <a name="codeunits-80-and-90"></a>Kodeenheder 80 og 90  
Med henblik på at opdele vareposter ved bogføring indsættes koden i kodeenhed 80 og kodeenhed 90 i løkker, der kører gennem globale, midlertidige postvariabler. Denne kode kalder kodeenhed 22 med en varekladdelinje. Disse variabler er initialiseret, når der findes varesporingsnumre for dokumentlinjen. Denne løkkestruktur bruges altid for at bevare koden enkel. Hvis der ikke findes varesporingsnumre til bilagslinjen, vil en enkelt post indsættes, og løkken køres kun en gang.  
  
## <a name="posting-the-item-journal"></a>Bogføring af varekladden  
Varesporingsnumre overføres via reservationsposter, der vedrører en bestemt varepost, og gennemløbet af varesporingsnumre sker i codeunit 22. Dette begreb fungerer på samme måde, når en varekladdelinje indirekte bruges til at bogføre et salg eller en indkøbsordre, ligesom når en varekladdelinje bruges direkte. Når varekladden bruges direkte, peger feltet **Kilderække-id** på selve varekladdelinjen.  
  
## <a name="code-unit-22"></a>Kodeenhed 22  
Kodeenheder 80 og 90 gentager kaldet fra kodenhed 22 under fakturabogføring af varesporingsnumre og under fakturering af eksisterende leverancer eller modtagelser.  
  
Under antalsbogføring af varesporingsnumre, henter kodeenhed 22 varesporingsnumre fra posterne i T337, der vedrører bogføringen. Disse poster placeres direkte på varekladdelinjen.  
  
Kodeenhed 22 gentages via varesporingsnumrene og opdeler bogføringen i de respektive vareposter, der har varesporingsnumrene. Oplysninger om, hvilke vareposter der oprettes returneres til T337 ved hjælp af en midlertidig T336 post, der kaldes af en procedure i codeunit 22. Denne procedure udløses, når kodeenhed 22 har afsluttet kørslen, da kodeenhed 22-objektet på dette tidspunkt indeholder oplysninger. Når den midlertidige T336-post er hentet, opretter kodeenhederne 80 og 90 poster i tabellen **Varepostrelation** for at knytte de oprettede vareposter til den oprettede leverance- eller modtagelseslinje. Kodeenhed 80 eller kodeenhed 90 konverterer derefter de midlertidige T336-poster til reelle T336-poster, der er relateret til den pågældende linje. Men konverteringen sker kun, hvis den bogførte bilagslinje ikke er slettet, fordi den er kun delvist bogført.  
  
## <a name="see-also"></a>Se også  
[Designoplysninger: Varesporing](design-details-item-tracking.md)   
[Designoplysninger: Design af varesporing](design-details-item-tracking-design.md)