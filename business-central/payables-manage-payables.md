---
title: Oversigt over opgaver til administration af kreditorer
description: Beskriver opgaver til administration af kreditorer, f.eks. betaling af kreditorer eller udligning af udgående betalinger til finansposter, for at lukke fakturaer eller kreditnotaer.
author: edupont04
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.search.form: 161, 254, 256, 347, 574, 599, 9002
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c3049cc4dd488a7ff7648d2a11d0371ac463daa6
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531437"
---
# <a name="managing-payables"></a><a name="managing-payables"></a>Administrere skyldige beløb

En vigtig del af styring af kreditorer er betaling af dine kreditorer eller refundering af medarbejderne for udgifter. Du kan bruge funktioner til at tilføje betalingslinjer for forfaldne købsfakturaer på siden **Udbetalingskladde**. Du kan transaktionerne til din bank ved at eksportere flere betalingskladdelinjer til en fil og derefter overføre filen til din bank. Du kan også oprette betalinger med check, herunder overføre checks som elektronisk betaling.

En anden typiske opgave er at udligne udgående betalinger til de relaterede kreditor- eller medarbejderposter for at lukke købsfakturaer, købskreditnotaer eller medarbejderkonti som betalt. Du kan gøre dette på siden **Betalingsudligningskladde** ved at importere en bankkontoudtogsfil for at registrere betalinger. Betalingerne udlignes til at åbne kreditor-, debitor- eller medarbejderposter ved at sammenligne betalingstekst og oplysninger i posten. Der er forskellige måder at gennemgå og ændre mulighederne, før du bogfører kladden. Du kan vælge at lukke alle åbne bankposter vedrørende de udlignede poster, når du bogfører kladden. Bankkontoen udlignes automatisk, når alle betalinger er udlignet.

Du kan også udligne udgående betalinger manuelt på siden **Udbetalingskladde** eller fra de relaterede kreditor- eller medarbejderposter.

Den følgende tabel indeholder en opgavesekvens i kreditorer med links til de emner, der rummer beskrivelserne af opgaverne.

| Hvis du vil | Se |
| --- | --- |
| Oprette forfaldne kreditorbetalinger eller medarbejderrefusioner, skal du forberede checkindbetalinger og udlæse betalinger til en bankfil, når du bogfører. |[Foretage betaling](payables-make-payments.md) |
| Udlign kreditorbetalinger automatisk til ubetalte købsfakturaer ved at importere en bankkontoudtogsfil. |[Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Udlign kreditorbetalinger til ubetalte købsfakturaer manuelt. |[Afstemme kreditorbetalinger med udbetalingskladden eller fra kreditorposter](payables-how-apply-purchase-transactions-manually.md) |
|Du kan sikre korrekt værdiansættelse af lageret ved at tildele ekstra vareomkostninger, f.eks. fragt, fysisk håndtering, forsikring og transport, som du har ved køb eller salg af varer.|[Bruge varegebyrer til at angive ekstra handelsomkostninger](payables-how-assign-item-charges.md)|
|Refunder medarbejdere for personlige udgifter under forretningsaktiviteter ved at foretage betaling til deres bankkonto.|[Registrere og refundere medarbejdernes udgifter](finance-how-record-reimburse-employee-expenses.md)|

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/paths/process-customer-vendor-payments-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Se også
[Køb](purchasing-manage-purchasing.md)  
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Bruge varegebyrer til at angive ekstra handelsomkostninger](payables-how-assign-item-charges.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
