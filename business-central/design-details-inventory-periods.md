---
title: Designoplysninger - Lagerperioder
description: Lagerperioder kan bruges til at undgå problemer med balancen og lagerreguleringer ved at åbne eller lukke lagerperioder for at begrænse bogføring i et angivet tidsrum.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-inventory-periods" />Designoplysninger: Lagerperioder
Tilbagedaterede transaktioner eller omkostningsreguleringer påvirker ofte saldi og lagerreguleringer for regnskabsperioder, der kan betragtes som afsluttet. Dette kan have negativ virkning på nøjagtig rapportering, især inden for globale virksomheder. Funktionen af lagerperioder kan bruges til at undgå sådanne problemer ved at åbne eller lukke lagerperioder for at begrænse bogføring i et angivet tidsrum.  

 En lagerperiode er et stykke tid, defineret ved en slutdato, hvor du bogfører lagertransaktioner. Når du lukker en lagerperiode, kan der ingen værdiændringer bogføres i den periode, der er lukket. Dette omfatter nye værdibogføringer, forventede eller fakturerede bogføringer, ændringer til eksisterende værdier og prisreguleringer. Du kan dog stadig anvende den på en åben varepost, der falder i den lukkede periode. Du kan finde flere oplysninger i [Designoplysninger: Vareudligning](design-details-item-application.md).  

 Med henblik på at sikre, at alle transaktionsposter i en lukket periode er endelige, skal følgende betingelser være opfyldt, før en lagerperiode kan lukkes:  

-   Alle udgående vareposter i perioden skal lukkes (ingen negativ lagerbeholdning).  
-   Alle vareomkostninger i perioden skal reguleres.  
-   Alle frigivne og færdige produktionsordrer i perioden skal være kostprisreguleret.  

 Når du lukker en lagerperiode, oprettes der en lagerperiodepost ved brug af nummeret på den sidste varejournal, der falder i lagerperioden. Den tid, dato og brugerkode for den bruger, der lukker perioden, registreres desuden i lagerperiodeposten. Ved hjælp af disse oplysninger sammen med den seneste varejournal for den forrige periode, kan du se, hvilke lagertransaktioner der er bogført i lagerperioden. Det er også muligt at genåbne lagerperioder, hvis du skal bogføre i en lukket periode. Når du genåbner en lagerperiode, oprettes der en lagerperiodepost.  

## <a name="see-also" />Se også

[Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)  
[Administrere lageromkostninger](finance-manage-inventory-costs.md)  
[Finans](finance.md)  
[Arbejde med Business Central](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
