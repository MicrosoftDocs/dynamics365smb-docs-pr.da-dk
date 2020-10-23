---
title: Oversigt over opgaver til administration af betalinger til kreditorer | Microsoft Docs
description: Beskrives opgaver til administration af betalinger til leverandører eller kreditorer, herunder bogføring af betalingslinjer og visning af en oversigt over den forfaldne saldo.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7d063b4b6a78f9a75cdb16050ffe14305df27d95
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3916672"
---
# <a name="making-payments"></a>Foretage betaling

Når du foretager betalinger til kunder eller kreditorer eller refusioner til medarbejdere, bogfører du relaterede de betalingslinjer på siden **Udbetalingskladde**. Betalingskladden er en kassekladde, der er optimeret til betalinger og indeholder en række effektive funktioner, f.eks. funktionen **Lav forslag**, der finder forslag, som er forfaldne, og rapporten **Kreditor - forfaldsoversigt**, der viser en oversigt over forfaldne kreditorbetalinger.  

Du kan gå i gang med at indbetale fra lister, kort og poster for kreditorer, debitorer og medarbejdere. Hver af disse sider har en knap, der starter betalingsprocessen og hjælper dig med udfyldelse i udbetalingskladden.  

Fra betalingskladden kan du udskrive computercheck eller registrere, når der skrives check. Hvis du markerer **Computercheck** i feltet **Bankbetalingstype**, skal linjer, der repræsenterer checks udskrives, før udbetalingskladden kan bogføres.

Når betalingerne er bogført, kan du eksportere dem til en bankfil for at overføre dem til behandling i din bank.

Efter at betalingerne er foretaget i din bank, skal du udligne dem til de relaterede åbne kreditor- eller medarbejderposter. Du kan gøre det manuelt eller ved at importere en bankkontoudtogsfil og udligne betalingerne automatisk. Du kan finde flere oplysninger under [Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.

| Hvis du vil | Se |
| --- | --- |
|Forstå grundlæggende funktioner på siden **Udbetalingskladde**, som er baseret på finanskladden, for at gøre klar til at bogføre betalinger til kreditorer eller medarbejdere.|[Arbejde med finanskladder](ui-work-general-journals.md)|
|Bogføre betalinger til kreditorer eller medarbejdere og refusioner til debitorer og eventuelt udligne betalingerne til de relaterede ubetalte fakturaer eller kreditnotaer for at lukke dem som betalt.|[Registrere betalinger og refusioner](payables-how-post-payments-refunds.md)|
| Bruge en funktion på siden **Udbetalingskladde** til at foreslå kreditorbetalinger i overensstemmelse med de valgte kriterier, f.eks. forfaldsdato, ret til rabat og din likviditet. |[Lav forslag](payables-how-suggest-vendor-payments.md) |
| Udstede checks for kreditorbetalinger eller debitorrefusioner enten som udskrifter eller som computercheck. Annullere checks før eller efter bogføringen. |[Foretage betalinger med check](payables-how-work-checks.md) |
|Oprette elektroniske betalinger i henhold til standarden for EU-SEPA-kreditoverførsel.|[Foretage betalinger med AMC Banking 365 Fundamentals-udvidelsen eller SEPA-kreditoverførsel](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|
| Betale en kreditor med kontanter eller check og bogfører betalingen, når du bogfører fakturaen. |[Afregne købsfakturaer omgående](finance-how-to-settle-purchase-invoices-promptly.md) |
| Kontroller, at din bank kun afregner validerede checks og beløb, ved at sende banken en fil, der indeholder kreditor- check- og betalingsoplysninger. |[Eksportere en Positive Pay-fil](finance-how-positive-pay.md) |

## <a name="see-also"></a>Se også
[Administrere skyldige beløb](payables-manage-payables.md)  
[Køb](purchasing-manage-purchasing.md)  
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
