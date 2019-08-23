---
title: Datoberegning for salg | Microsoft Docs
description: Programmet beregner automatisk den dato, hvor du skal bestille en vare for at have den på lager på en bestemt dato. Dette er den dato, du kan forvente, at varer, der er bestilt på en bestemt dato, er disponible til pluk.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 927c16f0fb1d12ff1202e4e675b97078d354375f
ms.sourcegitcommit: 8c0d734c7202fec81da79c7db382243aa49e37f6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/10/2019
ms.locfileid: "1737116"
---
# <a name="date-calculation-for-sales"></a>Beregning af forfaldsdato for salg
[!INCLUDE[d365fin](includes/d365fin_md.md)] beregner automatisk den tidligst mulige dato, som en vare eller en salgsordrelinje kan sendes på.

Hvis debitoren har anmodet om en bestemt leveringsdato, beregnes den dato, hvor varen skal være disponibel til pluk automatisk for at leveringen kan gennemføres rettidigt.

Hvis debitoren ikke anmoder om en bestemt leveringsdato, beregnes den dato, hvor varen kan leveres. Udgangspunktet er den dato, hvor varen er disponibel for pluk.

## <a name="calculating-a-requested-delivery-date"></a>Beregning med en ønsket leveringsdato
Hvis du angiver en ønsket leveringsdato på salgsordrelinjen, bliver denne dato til udgangspunktet for de efterfølgende beregninger.

- ønsket leveringsdato– transporttid = planlagt afsendelsesdato
- planlagt afsendelsesdato – udgående lagerekspeditionstid = planlagt afsendelsesdato

Hvis varen er disponibel til pluk på afsendelsesdatoen, kan salgsprocessen fortsættes. Ellers vises der en advarsel om, at varen ikke er på lager.

> [!Note]
> Hvis processen er baseret på bagudrettet beregning, f.eks. hvis du bruger den ønskede leveringsdato til at hente den planlagte afsendelsesdato, anbefales det, at du bruger datoformler med faste varigheder, f.eks. "5D" for fem dage eller "1U" for én uge. Datoformler uden faste varigheder, f.eks. "AU" for aktuelle uge eller AM for den aktuelle måned, kan resultere i forkerte datoberegninger. Du kan finde flere oplysninger om datoformler i [Arbejde med kalenderdatoer og-klokkeslæt](ui-enter-date-ranges.md).

## <a name="calculating-the-earliest-possible-delivery-date"></a>Beregning af den tidligst mulige leveringsdato
Hvis du ikke angiver en ønsket leveringsdato på en salgsordrelinje, eller hvis ikke den ønskede leveringsdato kan imødekommes, vil den tidligste dato for varernes tilgængelighed blive beregnet. Datoen kan derefter indtastes i feltet Afsendelsesdato på linjen, og den dato, som du planlægger at levere varer samt den dato, hvor de leveres til debitor beregnes ved hjælp af følgende formler.

- afsendelsesdato + udgående lagerekspeditionstid = planlagt afsendelses dato
- planlagt afsendelsesdato + transporttid = planlagt leveringsdato


## <a name="see-also"></a>Se også  
 [Beregning af forfaldsdato for køb](purchasing-date-calculation-for-purchases.md)   
 [Beregne ordrebekræftelsesdatoer](sales-how-to-calculate-order-promising-dates.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
