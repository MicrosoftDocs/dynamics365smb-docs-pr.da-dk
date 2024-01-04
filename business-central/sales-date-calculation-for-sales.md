---
title: Beregning af leveringsdato for salg
description: 'Programmet beregner automatisk den dato, hvor du skal bestille en vare for at have den på lager på en bestemt dato og tilgængelige til pluk.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/22/2022
ms.author: bholtorf
---
# Beregning af leveringsdato for salg

[!INCLUDE[prod_short](includes/prod_short.md)] beregner automatisk den tidligst mulige dato, som en vare eller en salgsordrelinje kan sendes på.

* Hvis debitoren har anmodet om en bestemt leveringsdato, beregnes den dato, hvor varen skal være disponibel til pluk automatisk for at leveringen kan gennemføres rettidigt.
* Hvis debitoren ikke anmoder om en bestemt leveringsdato, beregnes den dato, hvor varen skal være disponibel. Beregningen starter fra den dato, hvor varerne er disponible til pluk.

## Beregning en anmodet leveringsdato

Hvis du angiver en ønsket leveringsdato på salgsordrelinjen, bliver denne dato til udgangspunktet for de efterfølgende beregninger.

- *ønsket leveringsdato– transporttid = planlagt afsendelsesdato*
- *planlagt afsendelsesdato – udgående lagerekspeditionstid = planlagt afsendelsesdato*

Hvis varen er disponibel til pluk på afsendelsesdatoen, kan salgsprocessen fortsættes. Ellers vises der en advarsel om, at varen ikke er på lager.

> [!NOTE]
> Hvis processen er baseret på bagudrettet beregning, f.eks. hvis du bruger den ønskede leveringsdato til at hente den planlagte afsendelsesdato, anbefales det, at du bruger datoformler med faste varigheder, f.eks. "5D" for fem dage eller "1U" for én uge. Datoformler uden faste varigheder, f.eks. "AU" for aktuelle uge eller AM for den aktuelle måned, kan resultere i forkerte datoberegninger. Du kan finde flere oplysninger om datoformler i [Arbejde med kalenderdatoer og-klokkeslæt](ui-enter-date-ranges.md).

## Beregning af den tidligst mulige leveringsdato

Hvis du ikke angiver en ønsket leveringsdato på en salgsordrelinje, eller hvis ikke den ønskede leveringsdato kan imødekommes, vil den tidligste dato for varernes tilgængelighed blive beregnet. Datoen kan derefter indtastes i feltet **Afsendelsesdato** på linjen, og den dato, som du planlægger at levere varer samt den dato, hvor de leveres til debitor beregnes ved hjælp af følgende formler.

- *afsendelsesdato + udgående lagerekspeditionstid = planlagt afsendelses dato*
- *planlagt afsendelsesdato + transporttid = planlagt leveringsdato*

## Se også

[Beregne dato for køb](purchasing-date-calculation-for-purchases.md)  
[Beregne ordrebekræftelsesdatoer](sales-how-to-calculate-order-promising-dates.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
