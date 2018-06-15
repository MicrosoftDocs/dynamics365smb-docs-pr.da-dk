---
title: Oversigt over opgaver til administration af tilgodehavender | Microsoft Docs
description: Beskrives opgaver til administration af tilgodehavender og udligning af betalinger til debitor- eller kreditorposter.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer payment, debtor, balance due, AR
ms.date: 04/30/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 01a195130a6834256b30efea8c06841c88af354d
ms.contentlocale: da-dk
ms.lasthandoff: 05/15/2018

---
# <a name="managing-receivables"></a>Administrere tilgodehavender
Almindelige trin i en økonomisk cyklus er at udligne bankkonti, hvilket indebærer, at du udligner indgående betalinger til debitor- eller kreditorposter for at lukke salgsfakturaer og købskreditnotaer som betalte.

Mens de fleste kunder i B2B-miljøer betaler et stykke tid efter levering, og de bogførte salgsfakturaer forbliver åbne, indtil betalingen modtages, hvorefter afdelingen for tilgodehavender kan lukke (udligne) dem, kan nogle salgsfakturaer betales med det samme, for eksempel via PayPal. Disse fakturaer udlignes med det samme som betalte, når de bogføres og vises derfor ikke som betalinger, der skal behandles i Tilgodehavender. Du kan finde flere oplysninger i f.eks. [Fakturere salg](sales-how-invoice-sales.md).  

I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du hurtigt registrere betalinger i vinduet **Betalingsudligningskladde** ved at importere en bankkontoudtogsfil eller et -feed. Betalingerne udlignes til åbne debitor- eller kreditorposter baseret på sammenligninger af data i betalingstekst og oplysninger i poster. Du kan gennemse og ændre de fundne data, før du bogfører kladden, og lukke bankposter for poster, når du bogfører kladden. Bankkontoen er udlignet, når alle betalinger er udlignet.

Der findes andre vinduer, hvor du kan udligne betalinger eller afstemme bankkonti:

* Vinduet **Bankkontoafstemninger**, hvor du afstemmer bankkonti ved at sammenligne indlæste kontoudtogslinjer med dit systems bankkontoposter. Her kan du også afstemme checkindbetalinger. Du kan finde flere oplysninger i [Afstemme bankkonti separat](bank-how-reconcile-bank-accounts-separately.md). Her kan du ikke udligne betalinger.
* Vinduet **Betalingsregistrering**, hvor du manuelt kan udligne betalinger modtaget som kontant, med check eller via banktransaktion ud fra en genereret liste over ubetalte salgsdokumenter. Bemærk, at denne funktion kun er tilgængelig for salgsdokumenter. Her kan du kan ikke anvende udgående betalinger, og du kan ikke afstemme bankkonti.
* Vinduet **Indbetalingskladde**, hvor du manuelt bogfører indbetalinger til den relevante finans- eller debitorkonto eller anden konto ved at indtaste en betalingslinje. Du kan enten udligne indbetalingen eller refunderingen til en eller flere åbne poster, før du bogfører indbetalingskladden, eller fra debitorposterne. Her kan du ikke afstemme bankkonti.  

En andet område af administration af tilgodehavender er at indhente udestående beløb, herunder gebyrer, og udstede rykkere. [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder også måder at gøre dette på. Du kan finde flere oplysninger under [Indhente udestående beløb](receivables-collect-outstanding-balances.md).  

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.  

| Hvis du vil | Se |
| --- | --- |
| Udligne betalinger for at åbne debitor- eller kreditorposter baseret på et importeret bankkontoudtogsfil eller -feed og afstemme bankkontoen, når alle betalinger er udlignet. |[Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Udligne betalinger for at åbne debitorposter baseret på manuel indtastning på en liste over ubetalte salgsdokumenter. |[Afstemme debitorbetalinger manuelt på en liste over ubetalte salgsdokumenter](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Bogføre indbetalinger eller refusioner for debitorer i indbetalingskladden og udligne debitorposter, fra kladden eller fra bogførte poster. |[Afstemme debitorbetalinger manuelt](receivables-how-apply-sales-transactions-manually.md) |
| Minde debitorer om forfaldne beløb, beregne rente, oprette rentenotaer og håndtere tilgodehavender. |[Indhente udestående beløb](receivables-collect-outstanding-balances.md) |
|Du kan sikre dig, at du kender omkostningerne for leverede varer ved at tildele ekstra vareomkostninger, f.eks. fragt, fysisk håndtering, forsikring og transport, som du har efter salg af varer.|[Bruge varegebyrer til at angive ekstra handelsomkostninger](payables-how-assign-item-charges.md)|
|Angive en tolerance, som systemet lukker en faktura efter, også selvom betalingen, inklusive eventuel rabat, ikke fuldt ud dækker beløbet på fakturaen.|[Arbejde med betalingstolerancer og kontantrabattolerancer](finance-payment-tolerance-and-payment-discount-tolerance.md)|
## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Administrere skyldige beløb](payables-manage-payables.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

