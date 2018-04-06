---
title: Oversigt over opgaver til administration af betalinger til kreditorer | Microsoft Docs
description: "Beskrives opgaver til administration af betalinger til leverandører eller kreditorer, herunder bogføring af betalingslinjer og visning af en oversigt over den forfaldne saldo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 11/17/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: fb3a95c63963c2f209dfa8d6c04711a3e5dc8339
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="making-payments"></a>Foretage betaling
Når du foretager betalinger til kreditorer eller refusioner til medarbejdere, bogfører du relaterede de betalingslinjer i vinduet **Udbetalingskladde**. Du kan bruge funktionen **Lav kreditorbetalingsforslag** for at finde kreditorbetalinger, der er forfaldne. Du kan også bruge rapporten **Kreditor - forfaldsoversigt** til at få vist en oversigt over forfaldne kreditorbetalinger.

Fra betalingskladden kan du udskrive computercheck eller registrere, når der skrives check. Hvis du markerer **Computercheck** i feltet **Bankbetalingstype**, skal linjer, der repræsenterer checks udskrives, før udbetalingskladden kan bogføres.

Når betalingerne er bogført, kan du eksportere dem til en bankfil for at overføre dem til behandling i din bank.

Efter at betalingerne er foretaget i din bank, skal du udligne dem til de relaterede åbne kreditor- eller medarbejderposter. Du kan gøre det manuelt eller ved at importere en bankkontoudtogsfil og udligne betalingerne automatisk. Du kan finde flere oplysninger under [Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.

| Hvis du vil | Se |
| --- | --- |
|Bruge vinduet **Udbetalingskladde**, som er baseret på finanskladden, til at bogføre betalinger til kreditorer eller medarbejdere.|[Arbejde med finanskladder](ui-work-general-journals.md)|
| Brug en funktion til at foreslå kreditorbetalinger i overensstemmelse med de valgte kriterier, f.eks. forfaldsdato, ret til rabat og din likviditet. |[Lav forslag](payables-how-suggest-vendor-payments.md) |
|Refunder medarbejdere for personlige udgifter under forretningsaktiviteter ved at foretage betaling til deres bankkonto.|[Registrere og refundere medarbejdernes udgifter](finance-how-record-reimburse-employee-expenses.md)|
| Udsted checks for kreditorbetalinger enten som udskrifter eller som computercheck. Annullere checks før eller efter bogføringen. |[Arbejde med checks](payables-how-work-checks.md) |
| Betale kreditoren med kontanter eller check og bogfører betalingen, når du bogfører fakturaen. |[Afregne købsfakturaer omgående](finance-how-to-settle-purchase-invoices-promptly.md) |
| Kontroller, at din bank kun afregner validerede checks og beløb, ved at sende banken en fil, der indeholder kreditor- check- og betalingsoplysninger. |[Eksportere en Positive Pay-fil](finance-how-positive-pay.md) |
|Udlæs betalinger fra vinduet **Udbetalingskladde** til en bankfil, du overfører til din bank til behandling, herunder EFT (elektroniske pengeoverførsler) i Nordamerika. |[Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md)|
|Oprette elektroniske betalinger i henhold til standarden for EU-SEPA-kreditoverførsel.|[Foretage indbetalinger med tjenesten til konvertering af bankdata eller SEPA Kreditoverførsel](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|    

## <a name="see-also"></a>Se også
[Administrere skyldige beløb](payables-manage-payables.md)  
[Køb](purchasing-manage-purchasing.md)  
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

