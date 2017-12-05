---
title: Oversigt over opgaver til administration af tilgodehavender | Microsoft Docs
description: Beskrives opgaver til administration af tilgodehavender og udligning af betalinger til debitor- eller kreditorposter.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer payment, debtor, balance due, AR
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: daa014eaa78caa7a317b05ca92ff27c1d1530c06
ms.openlocfilehash: e8e6098cf6efe91153fe4e112cf3f6f6635032ed
ms.contentlocale: da-dk
ms.lasthandoff: 10/17/2017

---
# <a name="managing-receivables"></a>Administrere tilgodehavender
Almindelige trin i en økonomisk cyklus er at udligne bankkonti, hvilket indebærer, at du udligner betalinger til debitor- eller kreditorposter for at lukke salgsfakturaer og købskreditnotaer.  

I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du hurtigt registrere betalinger i vinduet **Betalingsudligningskladde** ved at importere en bankkontoudtogsfil eller et -feed. Betalingerne udlignes til åbne debitor- eller kreditorposter baseret på sammenligninger af data i betalingstekst og oplysninger i poster. Du kan gennemse og ændre de fundne data, før du bogfører kladden, og lukke bankposter for poster, når du bogfører kladden. Bankkontoen er udlignet, når alle betalinger er udlignet.

Der findes imidlertid andre steder, hvor det er praktisk at udligne betalinger og afstemme bankkonti:  

* Vinduet **Bankkontoafstemninger**, hvor du kan også kontrollere poster. Du kan finde flere oplysninger i [Fremgangsmåde: Afstemme bankkonti separat](bank-how-reconcile-bank-accounts-separately.md).  
* Vinduet **Betalingsregistrering**, hvor du kan udligne og manuelt kontrollere betalinger modtaget som kontant, check eller banktransaktion ud fra en genereret liste over ubetalte salgsdokumenter. Bemærk, at denne funktion kun er tilgængelig for salgsdokumenter.  
* Vinduet **Indbetalingskladde**, hvor du manuelt bogfører indbetalinger til den relevante finans- eller debitorkonto eller anden konto ved at indtaste en betalingslinje. Du kan enten udligne indbetalingen eller refunderingen til en eller flere åbne poster, før du bogfører indbetalingskladden, eller fra debitorposterne.  

En andet område af administration af tilgodehavender er at indhente udestående beløb, herunder gebyrer, og udstede rykkere. [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder også måder at gøre dette på. Du kan finde flere oplysninger under [Fremgangsmåde: Indhente udestående beløb](receivables-collect-outstanding-balances.md).  

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.  

| Hvis du vil | Se |
| --- | --- |
| Udligne betalinger for at åbne debitor- eller kreditorposter baseret på et importeret bankkontoudtogsfil eller -feed og afstemme bankkontoen, når alle betalinger er udlignet. |[Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Udligne betalinger for at åbne debitorposter baseret på manuel indtastning på en liste over ubetalte salgsdokumenter. |[Fremgangsmåde: Udligne debitorbetalinger manuelt på en liste over ubetalte salgsdokumenter](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Bogføre indbetalinger eller refusioner for debitorer i indbetalingskladden og udligne debitorposter, fra kladden eller fra bogførte poster. |[Fremgangsmåde: Udligne debitorbetalinger manuelt](receivables-how-apply-sales-transactions-manually.md) |
| Minde debitorer om forfaldne beløb, beregne rente, oprette rentenotaer og håndtere tilgodehavender. |[Fremgangsmåde: Indhente udestående beløb](receivables-collect-outstanding-balances.md) |
|Du kan sikre dig, at du kender omkostningerne for leverede varer ved at tildele ekstra vareomkostninger, f.eks. fragt, fysisk håndtering, forsikring og transport, som du har efter salg af varer.|[Fremgangsmåde: Bruge varegebyrer til at angive ekstra handelsomkostninger](payables-how-assign-item-charges.md)|
|Angive en tolerance, som systemet lukker en faktura efter, også selvom betalingen, inklusive eventuel rabat, ikke fuldt ud dækker beløbet på fakturaen.|[Fremgangsmåde: Arbejde med betalingstolerancer og kontantrabattolerancer](finance-payment-tolerance-and-payment-discount-tolerance.md)|
## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Administrere skyldige beløb](payables-manage-payables.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)

