---
title: Designoplysninger – Varesporing og planlægning | Microsoft Docs
description: 'Da de er gemt i reservationssystemet, er varesporingsnumre fuldt koordineret med ordresporingsposter.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="design-details-item-tracking-and-planning"></a>Designoplysninger: Varesporing og planlægning
Da de er gemt i reservationssystemet, er varesporingsnumre fuldt koordineret med ordresporingsposter. Dette betyder, at varer, der har varesporingsposter, kan blive tildelt varesporingsnumre. Varer, der har varesporingsnumre, kan derimod blive ordresporingsposter. Du kan finde flere oplysninger i [Designoplysninger: Design af varesporing](design-details-item-tracking-design.md).

Hvis du ønsker yderligere oplysninger om de integrerede systemer, kan du se [Designoplysninger: Reservationer, Ordresporing og Aktionsmeddelelser](design-details-reservation-order-tracking-and-action-messaging.md).

Da ordresporing kun vedrører specifik vareudligning, gælder koordinering med varesporingsnumre kun for varer, der er konfigureret til at bruge specifik varesporing. Dette angives i felterne **Serienr.specifik sporing** og **Lotspecifik sporing** på varekortet, som angiver følgende:

- Varen skal have et serienummer eller lotnummer, når den bogføres.
- Varen skal gælde for det samme serienummer eller lotnummer, når den bogføres udgående.

I overensstemmelse med standarden for forsyning/behov matcher udlignende principper, planlægningssystemet og sporingsfunktionen for relaterede ordrer kun forsyning og behov, der transporterer varesporingsnumre, hvis den pågældende vare bruger specifik varesporing. I alle andre tilfælde vil planlægning og ordresporingssystemer ignorere varesporingsnumre, når de anvender forsyning til at imødekomme behov eller anvender behov på forsyning. Du kan finde flere oplysninger i [Designoplysninger: Reservation, ordresporing og aktionsmeddelelser](design-details-reservation-order-tracking-and-action-messaging.md).

Når der f.eks. er ordresporing for en bestemt vare, betyder det, at poster for varen allerede er i tabellen **Reservationspost**, som er kernen i reservationssystemet, før varesporingsnumrene defineres. Derfor gælder følgende sammenkædningsbegrænsninger for de varesporingsnumre, der skal spores:

- Behov med et serienummer eller lotnummer kan kun dække forsyning med det samme serienummer eller lotnummer.
- Behov uden et serie- eller lotnummer kan dække enhver forsyning med eller uden et serie- eller lotnummer.

Bortset fra konsekvenserne af dynamisk ordresporing påvirker sammensætningsbegrænsninger for varesporing ikke planlægningssystemet i væsentlig grad.

På forsyningssiden bliver et serienummer eller lotnummer typisk ikke indtastet indtil umiddelbart før, ordren bogføres som en købsleverance på lagerstedet. Når du angiver et serie- eller lotnummer på behovssiden, f.eks. på en salgsordre, findes det pågældende serie- eller lotnummer allerede i lagerbeholdningen. Derfor er varesporingsnumre typisk ikke et problem i forsyningsplanlægning.

For varer, der bruger specifik varesporing, skal ethvert behov, der har serie- eller lotnumre, afstemmes med den tilsvarende forsyning. I de fleste tilfælde giver det ikke mening at genbestille et bestemt serienummer eller lotnummer, så planlægning af forsyninger til køb eller produktion påvirkes sandsynligvis ikke. Men under overførsel af varer fra én placering til en anden er det sandsynligt, at overførslen er for et bestemt lot, så planlægning af forsyninger til overførsel kan være påvirket af den specifikke sammenkædningsbegrænsning.

Du kan finde flere oplysninger i [Designoplysninger: Overførsler i planlægning](design-details-transfers-in-planning.md).

## <a name="balancing-demand-and-supply"></a>Afstemning af behov og forsyning
Hvis en vare kræver specifik varesporing, foretages et ordresporingslink fra alle varens varesporingsbehov til en tilsvarende varesporingsforsyning med den eneste begrænsning, at forsyning skal komme før behov. Hvis der under disse omstændigheder ikke findes varesporingsforsyning, der svarer til varesporingsspecifikke behov, oprettes der en ny forsyning til varesporing straks og uden at overveje ordrestørrelse, planlægningsparametre eller omlægning af eksisterende forsyning af det samme serie- eller lotnummer.

Hvis der er tildelt varesporingsnumre på behovssiden eller på forsyningssiden uden at kræve specifik varesporing, foretages der et ordresporlink fra behovet til denne forsyning baseret på den mest hensigtsmæssige timing og mængde, som i den sædvanlige udlignende procedure. Det angivne varesporingsantal indgår i ordresporingsposten på samme måde, som ethvert angivet varesporingsantal definerer den ene ende af ordresporingslinket. Det betyder, at det varesporingsnummer, der er angivet, bevares, men det er også en del af ordresporingsposten.

Hvis der er tildelt varesporingsnumre på forsyningssiden uden at kræve specifik varesporing, er anses denne forsyning som fastsat af planlægningssystemet. Ingen ændring af størrelse eller omlægning foreslås for denne forsyning, men forsyningen tages i betragtning, når planlægningssystemet forsøger at opfylde bruttobehovet.

Du kan finde flere oplysninger i [Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md).  

## <a name="see-also"></a>Se også
[Designoplysninger: Design af varesporing](design-details-item-tracking-design.md)  
[Designoplysninger: Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md)  
[Designoplysninger: Reservation, ordresporing og aktionsmeddelelser](design-details-reservation-order-tracking-and-action-messaging.md)   
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
