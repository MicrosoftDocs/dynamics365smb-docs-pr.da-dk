---
title: Registrere og refundere medarbejdernes forretningsrelaterede udgifter | Microsoft Docs
description: "Bogfør medarbejdernes udgifter med finanskladden til medarbejderens konto, og bogfør senere en betaling til medarbejderens bankkonto for at refundere for de forretningsrelaterede udgift."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c12561f4851cd75bdc4098e506c113e50d3bc3be
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="record-and-reimburse-employees-expenses"></a>Registrere og refundere medarbejdernes udgifter
[!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter transaktioner for medarbejderen på samme måde som for kreditorer. Derfor findes der medarbejderbogføringsgrupper for at sikre, at medarbejderposter bogføres på de relevante konti i regnskabet.

> [!NOTE]  
> Medarbejdertransaktioner kan kun bogføres i den lokale valuta. Refusion af betalinger til medarbejdere understøtter ikke rabatter og betalingstolerancer.

Hvis medarbejdere bruger deres egne penge under forretningsaktiviteter, kan du bogføre udgiften til medarbejderens konto. Du kan derefter refundere medarbejderen ved at foretage en betaling til medarbejderens bankkonto, på samme måde som når du betaler leverandører.

## <a name="to-record-an-employees-expense"></a>Sådan registrerer du en medarbejders udgift
Du bogfører medarbejdernes udgifter i vinduet **Finanskladde**.
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finanskladder**, og vælg derefter det relaterede link.
2. Åbn det relevante finanskladdenavn. Du kan finde flere oplysninger under [Arbejde med finanskladder](ui-work-general-journals.md).
3. Udfyld felterne efter behov på en ny kladdelinje. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. Gentag trin 3 for alle de udgifter, som er påløbet medarbejderen.

    > [!TIP]  
    > Hvis du vil angive flere udgiftslinjer over én modkontolinje for medarbejderens bankkonto, skal du markere afkrydsningsfeltet **Foreslå modkontobeløb** på linjen for kørslen i vinduet **Finanskladdenavne**. Feltet **Beløb** på modkontolinjen udfyldes derefter automatisk med den værdi, der skal bruges til at afstemme udgifterne.
5. Vælg handlingen **Bogfør** for at registrere udgifter på medarbejderens konto.

## <a name="to-reimburse-an-employee"></a>Sådan refunderer du en medarbejder
Du refunderer medarbejdere ved at bogføre betalinger til deres bankkonto i vinduet **Udbetalingskladde**.
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Udbetalingskladder**, og vælg derefter det relaterede link.
2. Åbn den relevante udbetalingskladdekørsel. Du kan finde flere oplysninger under [Arbejde med finanskladder](ui-work-general-journals.md).
3. Udfyld felterne efter behov. Du kan finde flere oplysninger under [Foretage betalinger](payables-make-payments.md).
4. Du kan også vælge handlingen **Foreslå medarbejderbetaling** for automatisk at indsætte kladdelinjerne for ventende medarbejderrefusioner.
5. Vælg handlingen **Bogfør** for at registrere refusionen.  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a>Sådan afstemmes refusioner med medarbejderposter
Du udligner medarbejderbetalinger til deres relaterede åbne medarbejderposter på samme måde som for kreditorbetalinger, f.eks. i vinduet **Betalingsudligningskladde**, baseret på de relaterede bankkontoudtogsposter. Du kan finde flere oplysninger under [Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md). Du kan også udligne manuelt i vinduet **Medarbejderposter**. Du kan finde flere oplysninger i den tilhørende [Afstemme kreditorbetalinger manuelt](payables-how-apply-purchase-transactions-manually.md).  

## <a name="see-also"></a>Se også
[Bogføre transaktioner direkte i finansposterne](finance-how-post-transactions-directly.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Tilbageføre poster](finance-how-reverse-journal-posting.md)  
[Finans](finance.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

