---
title: Oversigt over opgaver til at administrere betalinger til kreditorer
description: 'Beskrives opgaver til administration af betalinger til leverandører eller kreditorer, herunder bogføring af betalingslinjer og visning af en oversigt over den forfaldne saldo.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.search.keywords: 'print check, vendor payment, creditor, debt, balance due, AP'
ms.search.form: '254, 256, 1190, 1191, 1227, 1228, 1229'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="make-payments"></a>Foretage betalinger

Du betaler kreditorer eller debitorer eller refusioner dine medarbejdere ved at bogfører betalingslinjer på siden **Udbetalingskladde**. Betalingskladden er en kassekladde, der er optimeret til betalinger og tilbyder mange stærke handlinger. Det kan f.eks. være handlingen **Lav kreditorbetalingsforslag**, som finder forfaldne kreditorbetalinger, og rapporten **Kreditor - forfaldsoversigt**, der indeholder en oversigt over forfaldne kreditorbetalinger.  

Du kan starte betalingsprocessen fra lister, kort og poster for kreditorer, debitorer og medarbejdere. Hver af disse sider har en knap, der starter betalingsprocessen og hjælper dig med udfyldelse i udbetalingskladden.  

Fra betalingskladden kan du udskrive computercheck eller registrere, når der skrives check. Hvis du markerer **Computercheck** i feltet **Bankbetalingstype**, skal du udskrive linjer, der repræsenterer checks, før du kan bogføre udbetalingskladden.

Når du bogfører betalingerne, kan du eksportere dem til en bankfil for at uploade dem til behandling i din bank.

Efter at betalingerne er foretaget i din bank, skal du udligne dem til de relaterede åbne kreditor- eller medarbejderposter. Du kan anvende dem manuelt eller ved at importere en bankkontoudtogsfil og udligne betalingerne automatisk. Du kan finde flere oplysninger i [Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Den følgende tabel indeholder en opgavesekvens med links til de artikler, der rummer beskrivelserne af opgaverne.

| Til | Se |
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
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
