---
title: Datoberegning for salg | Microsoft Docs
description: "Programmet beregner automatisk den dato, hvor du skal bestille en vare for at have den på lager på en bestemt dato. Dette er den dato, du kan forvente, at varer, der er bestilt på en bestemt dato, er disponible til pluk."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 4e8bc9e8b99db8afda83edb4aff13f5daf9f5a31
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="date-calculation-for-sales"></a>Beregning af forfaldsdato for salg
[!INCLUDE[d365fin](includes/d365fin_md.md)] beregner automatisk den tidligst mulige dato, som en vare eller en salgsordrelinje kan sendes på.

Hvis debitoren har anmodet om en bestemt leveringsdato, beregnes den dato, hvor varen skal være disponibel til pluk automatisk for at leveringen kan gennemføres rettidigt.

Hvis debitoren ikke anmoder om en bestemt leveringsdato, beregnes den dato, hvor varen kan leveres. Udgangspunktet er den dato, hvor varen er disponibel for pluk.

## <a name="calculating-a-requested-delivery-date"></a>Beregning med en ønsket leveringsdato
Hvis der står en ønsket leveringsdato på salgsordrelinjen, bruges denne dato som udgangspunkt for følgende beregninger.

- ønsket leveringsdato– transporttid = planlagt afsendelsesdato
- planlagt afsendelsesdato – udgående lagerekspeditionstid = planlagt afsendelsesdato

Hvis varen er disponibel til pluk på afsendelsesdatoen, kan salgsprocessen fortsættes.

Hvis varen ikke er disponibel til pluk på afsendelsesdatoen, vises en advarsel om, at varen ikke er på lager.

## <a name="calculating-the-earliest-possible-delivery-date"></a>Beregning af den tidligst mulige leveringsdato
Hvis du ikke angiver en ønsket leveringsdato på en salgsordrelinje, eller hvis ikke den ønskede leveringsdato kan imødekommes, vil den tidligste dato for varernes tilgængelighed blive beregnet. Datoen kan derefter indtastes i feltet Afsendelsesdato på linjen, og den dato, som du planlægger at levere varer samt den dato, hvor de leveres til debitor beregnes ved hjælp af følgende formler.

- afsendelsesdato + udgående lagerekspeditionstid = planlagt afsendelses dato
- planlagt afsendelsesdato + transporttid = planlagt leveringsdato


## <a name="see-also"></a>Se også  
 [Beregning af forfaldsdato for køb](purchasing-date-calculation-for-purchases.md)   
 [Sådan beregnes ordrebekræftelsesdatoer](sales-how-to-calculate-order-promising-dates.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

