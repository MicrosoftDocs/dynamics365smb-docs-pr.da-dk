---
title: Oversigt over opgaver til administration af kreditorer | Microsoft Docs
description: "Beskriver opgaver til administration af kreditorer, f.eks. betaling af kreditorer eller udligning af udgående betalinger til finansposter, for at lukke fakturaer eller kreditnotaer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9684a91268927a4f1f4d249fef019c8f6ac00325
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="managing-payables"></a>Administrere skyldige beløb
En vigtig del af styring af gæld er at betale sine kreditorer. Du kan bruge funktioner til at tilføje betalingslinjer for forfaldne købsfakturaer i vinduet **Udbetalingskladde**. Du kan transaktionerne til din bank ved at eksportere flere betalingskladdelinjer til en fil og derefter overføre filen til din bank. Du kan også oprette betalinger med check, herunder overføre checks som elektronisk betaling.

En anden typiske opgave er at udligne udgående betalinger til de relaterede kreditorposter for at lukke købsfakturaer eller købskreditnotaer som betalt. Du kan gøre dette i vinduet **Betalingsudligningskladde** ved at importere en bankkontoudtogsfil for at registrere betalinger. Betalingerne anvendes til at åbne kreditor- eller debitorposter ved at sammenligne betalingstekst og oplysninger i posten. Der er forskellige måder at gennemgå og ændre mulighederne, før du bogfører kladden. Du kan vælge at lukke alle åbne bankposter vedrørende de udlignede poster, når du bogfører kladden. Bankkontoen udlignes automatisk, når alle betalinger er udlignet.

Du kan også udligne udgående betalinger manuelt i vinduet **Udbetalingskladde** eller fra de relaterede kreditorposter.

Den følgende tabel indeholder en opgavesekvens i kreditorer med links til de emner, der rummer beskrivelserne af opgaverne.

| Hvis du vil | Se |
| --- | --- |
| Generer forfaldne kreditorbetalinger prioriteret efter betalingsrabatter og strafgebyrer for overskridelser. Du kan også udlæse betalingerne til en bankfil ved bogføring. |[Foretage indbetalinger](payables-make-payments.md) |
| Udlign kreditorbetalinger automatisk til ubetalte købsfakturaer ved at importere en bankkontoudtogsfil. |[Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Udlign kreditorbetalinger til ubetalte købsfakturaer manuelt. |[Fremgangsmåde: Udligne kreditorbetalinger manuelt](payables-how-apply-purchase-transactions-manually.md) |
|Du kan sikre korrekt værdiansættelse af lageret ved at tildele ekstra vareomkostninger, f.eks. fragt, fysisk håndtering, forsikring og transport, som du har ved køb eller salg af varer.|[Fremgangsmåde: Bruge varegebyrer til at angive ekstra handelsomkostninger](payables-how-assign-item-charges.md)|

## <a name="see-also"></a>Se også
[Køb](purchasing-manage-purchasing.md)  
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Fremgangsmåde: Bruge varegebyrer til at angive ekstra handelsomkostninger](payables-how-assign-item-charges.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

