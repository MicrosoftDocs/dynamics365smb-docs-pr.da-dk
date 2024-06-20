---
title: Regnskab og bogholderi
description: 'Denne artikel indeholder oplysninger, der kan hjælpe dig med at bruge Microsoft Dynamics 365 Business Central til korrekt udførelse af regnskab og bogholderi for din virksomhed.'
author: altotovi
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'accounting, bookkeeping'
ms.search.form: '16, 39, 108'
ms.date: 03/14/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="accounting-and-bookkeeping"></a>Regnskab og bogholderi

Bogføring er en kritisk funktion i enhver ERP-løsning (Enterprise Resource Planning) og i de fleste virksomheder. Regnskabet er den proces, der bruges til at registrere og katalogisere virksomhedens økonomiske transaktioner og derefter hente, måle, opsummere og præsentere resultaterne ved hjælp af forskellige rapporter, der ofte kræves af lokal lovgivning. Det primære mål for denne proces er at hjælpe virksomhedens ledelse med at håndtere virksomhedens finans og måleresultaterne af virksomhedens økonomiske aktiviteter.

Bogføring er en del af regnskabsprocessen, og de omfatter regelmæssigt alle økonomiske transaktioner i en virksomhed. [!INCLUDE[prod_short](includes/prod_short.md)] er et ERP-system, der indeholder integrerede værktøjer, der gør bogføring nemmere i systemet. Mange handlinger kan gøres automatisk.

Denne artikel indeholder en oversigt over bogholderiprocesser, herunder regler, procedurer og andre retningslinjer i [!INCLUDE[prod_short](includes/prod_short.md)]. Indholdet af denne artikel er beregnet til at hjælpe revisorer og bogholdere med at fuldføre deres daglige arbejde i dette ERP-system. Hvis du ønsker yderligere hjælp, inkorporeres kontekstbaseret assistent i [!INCLUDE[prod_short](includes/prod_short.md)]. Denne assistent indeholder links til oplysninger, der er relateret til den aktuelle side og instruktioner til at arbejde med den relevante proces. Hvis du vil åbne, skal du vælge knappen [**Hjælp**](product-help-and-support.md) i øverste højre hjørne for at åbne ruden **Hjælp**. Brug derefter linkene i **Om denne opgave eller side** og **Relaterede ressourcer fra Microsoft Learn**-sektioner.

I følgende video introduceres nogle af de vigtigste funktioner i forbindelse med regnskab og bogholderi.

> [!Video https://www.microsoft.com/videoplayer/embed/RE4Fss4?rel=0]

Den følgende tabel indeholder en opgavesekvens og leverer links til de artikler, der dækker opgaverne.

| Opgave | Artikel |
|------|---------|
| Vis eller rediger de finanskonti, hvor alle finansposter bogføres | [Konfigurere eller ændre kontoplanen](finance-setup-chart-accounts.md) |
| Angiv, hvordan du vil betale for kunder, og hvordan du vil betale kreditorerne. | [Konfigurere betalingsformer](finance-payment-methods.md) |
| Angiv betalingsbetingelser til styring af forfaldsdatoer og til beregning af kontantrabatter. | [Konfigurere betalingsvilkår](finance-payment-terms.md) |
| Angiv de bogføringsgrupper, der knytter enheder (som debitorer, kreditorer, varer, ressourcer og salgs- og købsdokumenter) til finanskonti. | [Konfigurere bogføringsgrupper](finance-posting-groups.md)|
| Oprette finansrapporter og definere kontokategorier, der definerer indholdet af finansielle diagrammer og rapporter, f.eks. **Balancen** og **Resultatopgørelse**. | [Forberede Financial Reporting med finansdata og kontokategorier](bi-how-work-account-schedule.md)|
| Angive en tolerance, som systemet lukker en faktura efter, også selvom betalingen, inklusive eventuel rabat, ikke fuldt ud dækker beløbet på fakturaen. | [Arbejde med betalingstolerancer og kontantrabattolerancer](finance-payment-tolerance-and-payment-discount-tolerance.md) |
| Konfigurere regnskabsperioder. | [Arbejd med regnskabsperioder og regnskabsår](finance-accounting-periods-and-fiscal-years.md) |
| Definere faktura betingelser, som du kan bruge til at rykke debitorer for at foretage betalinger. | [Konfigurere rykkerbetingelser og -niveauer](finance-setup-reminders.md)|
| Definere, hvordan du rapporterer momsbeløb, som du har indsamlet for salg, til skattemyndighederne. | [Konfigurere merværdiafgift (moms)](finance-setup-vat.md) |
| Forbered håndtering af urealiseret moms i forbindelse med bogføringsmetoder, der er baseret på kontanter. | [Konfigurere urealiseret moms i forbindelse med bogføring baseret på kontanter](finance-setup-unrealized-vat.md) |
| Definere udenlandske valutaer, som du handler med, eller rapportere transaktioner i. | [Definere valutaer](finance-set-up-currencies.md) |
| Angive salgs- og købsfunktioner til at håndtere betalinger i fremmed valuta. | [Aktivere anvendelse af finansposter i forskellige valutaer](finance-how-enable-application-ledger-entries-different-currencies.md) |
| Definere en eller flere ekstra valutaer, så beløbene automatisk rapporteres i både lokal valuta (RV) og den ekstra rapporteringsvaluta i hver finanspost og i andre poster. | [Konfigurere en ekstra rapporteringsvaluta](finance-how-setup-additional-currencies.md) |
| Reguler de ekstra valutaer med jævne mellemrum for at afhjælpe varierende valutakurser. | [Opdatere valutakurser](finance-how-update-currencies.md)|
| Definer flere rentesatser, der skal bruges til forskellige perioder for forsinkede betalinger i handelstransaktioner. | [Konfigurere flere rentesatser](finance-how-to-set-up-multiple-interest-rates.md) |
| Arranger for beløb, der automatisk skal afrundes, når der oprettes fakturaer. | [Konfigurere fakturaafrunding](finance-set-up-invoice-rounding.md) |
| Føje nye konti til den eksisterende kontoplan (COA). | [Konfigurere kontoplanen](finance-setup-chart-accounts.md) |
| Oprette business intelligence (BI)-diagrammer til at analysere likviditet. | [Opsætning af pengestrømsanalyse](finance-setup-cash-flow-analyses.md) |
| Aktivere fakturering af en debitor, der ikke er sat op i systemet. | [Konfigurere kontantkunder](finance-how-to-set-up-cash-customers.md) |
| Oprette Intrastatrapportering og sende rapporten til en myndighed. | [Konfigurere og rapportere Intrastat](finance-how-setup-report-intrastat.md) |
| Kontrollér, at en post i en finanskladde knyttes til flere forskellige konti, når du bogfører kladden, enten efter antal, procent eller beløb. | [Bruge fordelingsnøgler i finanskladder](ui-how-use-allocation-keys-general-journals.md) |
| Definere kilde- og årsagskoder, som du kan bruge til at holde øje med revisionsspor. | [Opret kilde- og årsagskoder til revisionsspor](finance-setup-trail-codes.md) |
| Angiv standardrapporter, der skal bruges til forskellige dokumenttyper. | [Rapportvalg i Business Central](across-report-selections.md) |
| Udligne indgående betalinger, afstemme bankkonti under betalingsudligning og indhente udestående beløb. | [Administrere tilgodehavender](receivables-manage-receivables.md) |
| Foretage indbetalinger, udligne udgående betalinger og arbejde med check. | [Administrere skyldige beløb](payables-manage-payables.md) |
| Bed dine debitorer om at sende betaling, før du sender til dem, eller send betaling til dine kreditorer, før de sender til dig. | [Fakturere forudbetalinger](finance-invoice-prepayments.md) |
| Afstemme og overføre beløb mellem bankkonti. | [Bankkontoafstemning](bank-manage-bank-accounts.md) |
| Opret koncerninterne partnere, og behandl transaktioner, manuelt eller automatisk, mellem juridiske enheder inden for samme virksomhed. | [Administrere Intercompany-transaktioner (IC)](intercompany-manage.md) |
| Analysér omkostningerne til virksomhedens drift ved at fordele faktiske og budgetterede omkostninger for operationer, afdelinger, produkter og projekter til omkostningssteder. | [Regnskab for omkostninger](finance-manage-cost-accounting.md) |
| Styre lager- og produktionsomkostninger og rapportere og afstemme omkostninger med finansposterne. | [Administrere lageromkostninger](finance-manage-inventory-costs.md) |
| Administrere og rapportere indgående og udgående pengestrømme. | [Oversigt over pengestrøm]( finance-cash-flow-overview.md) |
| Overvåge pengestrømme ind og ud af din virksomhed. | [Analysere pengestrømme i din virksomhed](finance-analyze-cash-flow.md) |
| Bruge finansrapporter til at foretage pengestrømsbudgetter for at følge en hel proces. | [Udarbejd likviditetsforecast ved hjælp af finansrapporter](walkthrough-making-cash-flow-forecasts-by-using-account-schedules.md) |
| Få mere at vide om Finans og kontoplan | [Om Finans og kontoplanen](finance-general-ledger.md) |
| Kombiner finansposter fra flere regnskaber i ét virtuelt konsolideret regnskab til finansielle analyser. | [Konsolidering af finansielle oplysninger fra flere regnskaber](finance-consolidated-company-reporting.md)|
| Tilføje dimensioner for mere detaljeret business intelligence. | [Arbejde med dimensioner](finance-dimensions.md) |
| Opret finansbudgetter for at estimere forskellige finansielle aktiviteter og tildele dimensioner i forbindelse med business intelligence. | [Oprette Finansbudgetter](finance-how-create-budgets.md) |
| Registrere indtægter og udgifter direkte i finansregnskabet uden at bogføre dedikerede forretningsdokumenter. | [Bogføre transaktioner direkte i finansposterne](finance-how-post-transactions-directly.md) |
| Tilbagefør poster for at fortryde værdibogføringer i den generelle kladde eller mængdebogføringer på købs- og salgsdokumenter. | [Tilbageføre kladdeposteringer og annullere modtagelser/leverancer](finance-how-reverse-journal-posting.md) |
| Allokere en post i en finanskladden til forskellige konti, når du bogfører kladden. | [Fordele omkostninger og indtægter](year-allocate-costs-income.md) |
| Tildel ekstra omkostninger såsom fragt og udgifter til fysisk håndtering, som du har under handel, til de varer, der er involveret. På den måde afspejles omkostningen ved lagerværdi. | [Bruge varegebyrer til at angive ekstra handelsomkostninger](payables-how-assign-item-charges.md) |
| Bogføre medarbejderrelaterede aktiviteter og foretage refusioner direkte på bankkonti for medarbejdere. | [Registrere og refundere medarbejdernes udgifter](finance-how-record-reimburse-employee-expenses.md) |
| Alloker indtægter og udgifter til andre perioder, end når transaktionerne faktisk blev bogført. | [Periodisere indtægter og udgifter](finance-how-defer-revenue-expenses.md) |
| Få mere at vide om de tilgængelige muligheder for at automatisere afsendelse af abonnementsfakturaer til dine kunder og registrering af tilbagevendende indtægter. | [Arbejde med tilbagevendende indtægt](finance-recurring-invoicing.md) |
| Få mere at vide om, hvordan du bruger flere valutaer og opdaterer valutakurser automatisk. | [Opdatere valutakurser](finance-how-update-currencies.md) |
| Importere løntransaktioner fra din lønningslisteudbyder i finansbogholderiet. | [Importere løntransaktioner](finance-how-import-payroll-transactions.md) |
| Beregn moms på salgs- og købstransaktioner, så du kan rapportere beløbene til skattemyndighederne. | [Arbejde med moms af salg og køb](finance-work-with-vat.md) |
| Udarbejd en rapport over moms fra salg, og send rapporten til en skattemyndighed i Den Europæiske Union (EU). | [Rapportere moms til skattemyndighederne](finance-how-report-vat.md) |
| Manuelt konvertere servicekontrakterne for at ændre deres momssats. | [Konvertere servicekontrakter, der omfatter momsbeløb](service-how-to-convert-service-contracts.md) |
| Arbejde med regnskabsopgørelser og oversigter i Microsoft Excel. | [Analysere regnskabsopgørelser i Excel](finance-analyze-excel.md) |
| Brug rollecenteret Revisor, engagere en ekstern revisor og brug virksomhedshubben til at administrere konti for flere klienter. | [Revisoroplevelser i Business Central](finance-accounting.md) |
| Oprette Intrastat-rapporter for at tilvejebringe handel med andre EU-medlemmer ifølge lokal lovgivning. | [Konfigurere intrastat-rapportering]( finance-how-setup-report-intrastat.md) |
| Udfyld, valider og send Intrastat-rapporten. | [Arbejde med Intrastat-rapportering]( finance-how-report-intrastat.md) |
| Oprette, udfylde, validere og sende rapporten service rapport til handels serviceydelser på tværs af EU. | [ Konfigurere og bruge udvidelsen af Servicedeklaration]( finance-how-setup-use-service-declaration.md) |
| Oprette anlægsaktiver, tilknytte afskrivningsmetoder, bogføre anskaffelser og skrapværdier og udskrive oversigter over anlægsaktiver. | [Anskaffede anlægsaktiver](fa-how-acquire.md) |
| Registrere servicebesøg, bogføre og overvåge reparationsomkostninger. | [Vedligeholde anlægsaktiver](fa-how-maintain.md) |
| Opdatere forsikringsoplysninger, bogføre anskaffelsespriser til forsikringspolicer, ændre forsikringsdækning, få vist forsikringsstatistik og oversigter over forsikringspolicer. | [Forsikring af anlægsaktiver](fa-how-insure.md) |
| Ompostere anlægsaktiver, overføre anlægsaktiver til forskellige lokationer, opdele eller kombinere anlæg. | [Overføre, opdele eller kombinere anlægsaktiver](fa-how-trans-split-combine.md) |
| Regulere anlægsaktivernes værdier, bogføre opskrivnings- og nedskrivningstransaktioner. | [Omvurdere anlægsaktiver](fa-how-revalue.md) |
| Beregne afskrivning, bogføre afskrivning og analysere afskrivning i anlægsrapporter. | [Afskrive eller amortisere anlægsaktiver](fa-how-depreciate-amortize.md) |
| Bogføre salgstransaktioner, have vist salgsposter og bogføre delvist salg. | [Afhænde eller lade anlægsaktiver udgå](fa-how-dispose-retire.md) |
| Administrere anlægsbudgetter, budgettere anskaffelsesomkostninger, salg af anlægsaktiver og afskrivning. | [Administrere budgetter for anlægsaktiver](fa-how-manage-budgets.md) |
| Oprette godkendelsesworkflowbrugere, angive, hvordan brugere modtager notifikationer, og oprette nye arbejdsgange. Sådan oprettes nye workflows til ikke-understøttede scenarier, implementeres de krævede workflowelementer ved at tilpasse programkoden. | [Konfigurere godkendelsesworkflows](across-set-up-workflows.md) |
| Aktiver godkendelsesworkflows, behandl meddelelser i arbejdsgangen (f.eks. godkendelser og godkendelsesanmodninger om at udføre trin i en arbejdsgang) og arkiver og slet arbejdsflows. | [Bruge godkendelsesworkflows](across-use-workflows.md) |
| Få vist budgetter, og faktiske beløb sammenlignet med budgetterede beløb for alle konti og for flere perioder. | [Analysere faktiske beløb sammenlignet med budgetterede beløb](bi-how-analyze-actual-versus-budget.md) |
| Oprette nye finansrapporter for at definere regnskaber til rapportering eller visning som diagrammer. | [Forberede finansrapporter med finansdata og kontokategorier](bi-how-work-account-schedule.md) |
| Analyser din finansielle ydeevne ved at konfigurere KPI'er baseret på finansrapporter, som du derefter publicerer som webtjenester. De publicerede finansrapporters KPI'er kan ses på et websted eller importeres i Excel ved hjælp af OData-webtjenester. | [Konfigurere og udgive KPI-webtjenester, der er baseret på finansielle rapporter](bi-how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules.md) |
| Oprette visninger for at analysere data vha. dimensioner. | [Analysere data efter dimensioner](bi-how-analyze-data-dimension.md) |
| Oprette nye analyserapporter for salg, køb og lager og oprette analyseskabeloner. | [Oprette analyserapporter](bi-how-create-analysis-views-reports.md) |
| Aktivere global finansiel rapportering til internationale revisionsfirmaer med XBRL-standarden (eXtensible Business Reporting Language). | [Oprette rapporter med XBRL](bi-create-reports-with-xbrl.md) |
| Rediger formål for adgang til databaser på rapporter, sider af typen API og forespørgsler for at reducere belastningen og forbedre ydeevnen. | [Administrere hensigter med databaseadgang](admin-data-access-intent.md) |

## <a name="see-also"></a>Se også

[Konfigurere Finans](finance-setup-finance.md)  
[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Afslutte regnskabsperioder](year-close-years-periods.md)  
[Administrere projekter](projects-manage-projects.md)  
[Importere data fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
