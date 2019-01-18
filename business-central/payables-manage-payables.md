---
title: Oversigt over opgaver til administration af kreditorer | Microsoft Docs
description: "Beskriver opgaver til administration af kreditorer, f.eks. betaling af kreditorer eller udligning af udgående betalinger til finansposter, for at lukke fakturaer eller kreditnotaer."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 11/15/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 9bc4eaf292c20c1525c499cde715964eb6e6631f
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="managing-payables"></a>Administrere skyldige beløb

En vigtig del af styring af kreditorer er betaling af dine kreditorer eller refundering af medarbejderne for udgifter. Du kan bruge funktioner til at tilføje betalingslinjer for forfaldne købsfakturaer på siden **Udbetalingskladde**. Du kan transaktionerne til din bank ved at eksportere flere betalingskladdelinjer til en fil og derefter overføre filen til din bank. Du kan også oprette betalinger med check, herunder overføre checks som elektronisk betaling.

En anden typiske opgave er at udligne udgående betalinger til de relaterede kreditor- eller medarbejderposter for at lukke købsfakturaer, købskreditnotaer eller medarbejderkonti som betalt. Du kan gøre dette på siden **Betalingsudligningskladde** ved at importere en bankkontoudtogsfil for at registrere betalinger. Betalingerne udlignes til at åbne kreditor-, debitor- eller medarbejderposter ved at sammenligne betalingstekst og oplysninger i posten. Der er forskellige måder at gennemgå og ændre mulighederne, før du bogfører kladden. Du kan vælge at lukke alle åbne bankposter vedrørende de udlignede poster, når du bogfører kladden. Bankkontoen udlignes automatisk, når alle betalinger er udlignet.

Du kan også udligne udgående betalinger manuelt på siden **Udbetalingskladde** eller fra de relaterede kreditor- eller medarbejderposter.

Den følgende tabel indeholder en opgavesekvens i kreditorer med links til de emner, der rummer beskrivelserne af opgaverne.

| Hvis du vil | Se |
| --- | --- |
| Oprette forfaldne kreditorbetalinger eller medarbejderrefusioner, skal du forberede checkindbetalinger og udlæse betalinger til en bankfil, når du bogfører. |[Foretage betaling](payables-make-payments.md) |
| Udlign kreditorbetalinger automatisk til ubetalte købsfakturaer ved at importere en bankkontoudtogsfil. |[Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
|Opret tilknytninger mellem tekst på betalinger og specifikke debet-, kredit- og modkonti, så disse betalinger bliver bogført på de angivne konti, når du bogfører kladden til betalingsafstemning.|[Knytte tekst på tilbagevendende betalinger til automatisk afstemning af konti](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)|
| Udlign kreditorbetalinger til ubetalte købsfakturaer manuelt. |[Udligne kreditorbetalinger manuelt](payables-how-apply-purchase-transactions-manually.md) |
|Angiv automatisk betalinger, enten indgående eller udgående, der er registreret som transaktioner på din onlinebankkonto på deres relaterede åbne debitor-, kreditor- og bankkontoposter. Listen oprettes på grundlag af en bank feed eller en fil.|[Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md)|
|Håndter betalinger til din bankkonto, der ikke kan udlignes automatisk, manuelt, f.eks. fordi der ikke findes noget dokument, som betalingen kan udlignes til, eller det tilknyttede dokument har et andet beløb end transaktionsbeløbet på grund af en valutaforskel.|[Afstemme betalinger, der ikke kan udlignes automatisk](receivables-how-reconcile-payments-cannot-apply-auto.md)|
|Du kan sikre korrekt værdiansættelse af lageret ved at tildele ekstra vareomkostninger, f.eks. fragt, fysisk håndtering, forsikring og transport, som du har ved køb eller salg af varer.|[Bruge varegebyrer til at angive ekstra handelsomkostninger](payables-how-assign-item-charges.md)|
|Hvis det er nødvendigt at betale kreditoren kontant eller med check, kan du bogføre betalingen, når du bogfører fakturaen.|[Afregne købsfakturaer omgående](finance-how-to-settle-purchase-invoices-promptly.md)|
|Refunder medarbejdere for personlige udgifter under forretningsaktiviteter ved at foretage betaling til deres bankkonto.|[Registrere og refundere medarbejdernes udgifter](finance-how-record-reimburse-employee-expenses.md)|

## <a name="see-also"></a>Se også
[Køb](purchasing-manage-purchasing.md)  
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Bruge varegebyrer til at angive ekstra handelsomkostninger](payables-how-assign-item-charges.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

