---
title: Konfigurere finansielle processer | Microsoft Docs
description: Få mere at vide om opgaver til konfiguration af finans i din virksomhed, der dækker alle dine regnskabs-, revisions- og bogholderibehov.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b18d4406f77594486104e2348487a3380cca0af4
ms.sourcegitcommit: 32bfc2acaaf3693afc9aeb86feea505fd328caa1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/19/2021
ms.locfileid: "5024458"
---
# <a name="setting-up-finance"></a>Konfigurere Finans
Før du kan begynde at køre din virksomhed, skal du angive regler og standarder for, hvordan du vil administrere finansprocesser for den pågældende virksomhed. Du starter med at definere kernen i regnskabets poster- kontoplanen. Derefter definerer du bogføringsgrupper, som gør det mere effektivt, når du skal tildele standardkonti til finanspostering til kunder, leverandører og varer.

Noget opsætning af finans kan udføres automatisk med assisterede opsætningsvejledninger, mens andet skal udføres manuelt. Du kan finde flere oplysninger under [Blive klar til at handle](ui-get-ready-business.md).

Du kan bruge dimensioner til at føje forskellige typer oplysninger til hver transaktion. Du kan konfigurere de grundlæggende dimensioner i regnskabet, f.eks. Projekter og Afdelinger. Senere kan du tilføje flere dimensioner, når du får brug for dem, og du kan definere midlertidige dimensioner til brug i en begrænset periode, f.eks. i forbindelse med en salgskampagne. Du kan finde flere oplysninger i [Arbejde med dimensioner](finance-dimensions.md).

Mange af opsætningsopgaverne skal være fuldført, før du kan begynde at registrere finansielle transaktioner, men de fleste indstillinger kan ændres på et senere tidspunkt. Nogle af opsætningsopgaverne er valgfri, f.eks. kan du kun definere Intercompany-bogføring og konsolidering, hvis du arbejder med flere regnskaber. Nogle opsætningsopgaver, f.eks. angivelse af den periode, hvor bogføring er tilladt, skal måske gentages periodisk.  

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.

| Hvis du vil | Skal du se |
| --- | --- |
| Angiv, hvordan du vil betale for kunder, og hvordan du vil betale kreditorerne. |[Konfigurere betalingsmetoder](finance-payment-methods.md) |
| Angiv betalingsbetingelser til styring af forfaldsdatoer og til beregning af kontantrabatter.|[Definere betalingsbetingelser](finance-payment-terms.md) |
| Angiv de bogføringsgrupper, der knytter enheder som debitorer, kreditorer, varer, ressourcer og salgs- og købsdokumenter til finanskonti. |[Konfigurere bogføringsgrupper](finance-posting-groups.md)|
|Oprette kontoskemaer og definere kontokategorier for at definere indholdet af finansielle diagrammer og rapporter, f.eks. balancen og årsopgørelsesrapporter.|[Forberede finansrapporter med kontoskemaer og kontokategorier](bi-how-work-account-schedule.md)|
|Angive en tolerance, som systemet lukker en faktura efter, også selvom betalingen, inklusive eventuel rabat, ikke fuldt ud dækker beløbet på fakturaen.|[Arbejde med betalingstolerancer og kontantrabattolerancer](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Konfigurere regnskabsperioder. |[Arbejd med regnskabsperioder og regnskabsår](finance-accounting-periods-and-fiscal-years.md) |
|Opret rykkerbetingelser, der kan hjælpe dig med at samle for forfaldne betalinger.|[Konfiguration af rykkerbetingelser og -niveauer](finance-setup-reminders.md)|
| Definere, hvordan du rapporterer momsbeløb, som du har indsamlet for salg, til skattemyndighederne. |[Konfigurere moms](finance-setup-vat.md)|
|Forbered håndtering af urealiseret moms i forbindelse med bogføringsmetoder, der er baseret på kontanter.|[Konfigurere urealiseret moms i forbindelse med bogføring baseret på kontanter](finance-setup-unrealized-vat.md)|
| Angive salgs- og købsfunktioner til at håndtere betalinger i fremmed valuta.|[Aktivere anvendelsen af finansposter i forskellige valutaer](finance-how-enable-application-ledger-entries-different-currencies.md)
|Definere en eller flere ekstra valutaer, så beløbene automatisk rapporteres i både RV og den ekstra rapporteringsvaluta i hver finanspost og i andre poster.|[Oprette en ekstra rapporteringsvaluta](finance-how-setup-additional-currencies.md)|
|Reguler de ekstra valutaer med jævne mellemrum for at afhjælpe varierende valutakurser.|[Opdatere valutakurser](finance-how-update-currencies.md)|
|Definer flere rentesatser, der skal bruges til forskellige perioder for forsinkede betalinger i handelstransaktioner.|[Angive flere rentesatser](finance-how-to-set-up-multiple-interest-rates.md)|
|Forbered automatisk afrunding af fakturabeløb, når du opretter fakturaer.|[Opsætning af fakturaafrunding](finance-set-up-invoice-rounding.md)|
| Føje nye konti til den eksisterende kontoplan. |[Konfigurere kontoplanen](finance-setup-chart-accounts.md) |
| Oprette business intelligence (BI)-diagrammer til at analysere likviditet. |[Opsætning af pengestrømsanalyse](finance-setup-cash-flow-analyses.md) |
|Aktivere fakturering af en debitor, der ikke er sat op i systemet.|[Konfigurere kontantkunder](finance-how-to-set-up-cash-customers.md)|
| Oprette Intrastatrapportering og sende rapporten til en myndighed | [Konfigurere og rapportere Intrastat](finance-how-setup-report-intrastat.md)|
|Kontrollér, at en post i en finanskladde knyttes til flere forskellige konti, når du bogfører kladden, enten efter antal, procent eller beløb.|[Bruge fordelingsnøgler i finanskladder](ui-how-use-allocation-keys-general-journals.md)|
|Definere kilde- og årsagskoder, som du kan bruge til at holde øje med revisionsspor|[Opret kilde- og årsagskoder til revisionsspor](finance-setup-trail-codes.md)|
|Angiv standardrapporter, der skal bruges til forskellige dokumenttyper.|[Rapportvalg i Business Central](across-report-selections.md)|

> [!TIP]
> Nogle sider kan indeholde felter, der ikke er beskrevet i de artikler, der er angivet her, fordi de gælder for lokal funktionalitet eller tilpasninger, afhængigt af din geografiske placering. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Finans](finance.md)  
[Bankkontoafstemning](bank-manage-bank-accounts.md)  
[Arbejde med dimensioner](finance-dimensions.md)  
[Importer virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Analysere pengestrømme i din virksomhed](finance-analyze-cash-flow.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]