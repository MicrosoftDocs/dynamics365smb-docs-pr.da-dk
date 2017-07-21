---
title: Oversigt over opgaver til administration af betalinger til kreditorer | Microsoft Docs
description: "Beskrives opgaver til administration af betalinger til leverandører eller kreditorer, herunder bogføring af betalingslinjer og visning af en oversigt over den forfaldne saldo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d0b9020596484a8910db2f5720adfe159ad96fe7
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="make-payments"></a>Foretage indbetalinger
Når du foretager betalinger til kreditorer, bogfører du relaterede de betalingslinjer i vinduet **Udbetalingskladde**. Du kan bruge funktionen **Lav kreditorbetalingsforslag** for at finde betalinger, der er forfaldne. Du kan også bruge rapporten **Kreditor - forfaldsoversigt** til at få vist en oversigt over forfaldne betalinger.

Fra betalingskladden kan du udskrive computercheck eller registrere, når der skrives check. Hvis du markerer **Computercheck** i feltet **Bankbetalingstype**, skal linjer, der repræsenterer checks udskrives, før udbetalingskladden kan bogføres.

Når betalingerne er bogført, kan du eksportere dem til en bankfil for at overføre dem til behandling i din bank.

Efter at betalingerne er foretaget i din bank, skal du udligne dem til de relaterede åbne kreditorposter. Du kan gøre det manuelt eller ved at importere en bankkontoudtogsfil og udligne betalingerne automatisk. Du kan finde flere oplysninger under [Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.

| Hvis du vil | Se |
| --- | --- |
| Brug en funktion til at foreslå kreditorbetalinger i overensstemmelse med de valgte kriterier, f.eks. forfaldsdato, ret til rabat og din likviditet. |[Fremgangsmåde: Lave kreditorbetalingsforslag](payables-how-suggest-vendor-payments.md) |
| Udsted checks for betalinger enten som udskrifter eller som computercheck. Annullere checks før eller efter bogføringen. |[Fremgangsmåde: Arbejde med checks](payables-how-work-checks.md) |
| Kontroller, at din bank kun afregner validerede checks og beløb, ved at sende banken en fil, der indeholder kreditor- check- og betalingsoplysninger. |[Fremgangsmåde: Eksportere en Positive Pay-fil](finance-how-positive-pay.md) |
|Udlæs betalinger fra vinduet **Udbetalingskladde** til en bankfil, du overfører til din bank til behandling, herunder EFT (elektroniske pengeoverførsler) i Nordamerika. |[Fremgangsmåde: Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md)|  

## <a name="see-also"></a>Se også
[Administrere skyldige beløb](payables-manage-payables.md)  
[Køb](purchasing-manage-purchasing.md)  
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

