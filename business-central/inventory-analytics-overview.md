---
title: Lageranalyse
description: 'Business Central indeholder mange funktioner, som kan hjælpe dig med at indsamle, analysere og dele data om dit lager til Business Intelligence og beslutningstagning i din organisation.'
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 05/03/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Lageranalyse

Virksomheder indsamler store mængder data under daglige aktiviteter, der understøtter værdifuld business intelligence (BI) for lagerledere:

- Levering af varer, når salgsordrer er opfyldt.
- Varemodtagelser, når købsordrer er opfyldt.
- Flytninger af varer mellem lokationer.

[!INCLUDE[prod_short](includes/prod_short.md)] indeholder funktioner, som kan være nyttige, når du skal indsamle, analysere og dele virksomhedens lagerdata:

- Ad hoc-analyse på lister
- Ad-hoc analyse af data i Excel (ved hjælp af Åbn i Excel)
- Indbyggede værktøjer til lageranalyse
- Indbyggede lagerrapporter

Hver af disse funktioner har sine fordele og ulemper afhængigt af typen af dataanalyse og brugerens rolle. Du kan få mere at vide ved at gå til [Analyser, Business Intelligence og Oversigt over rapportering](reports-bi-reporting.md).

I denne artikel introduceres det, hvordan du kan bruge disse analytiske funktioner til at få indsigt i dit lager.

## Analysebehov inden for lager

Når du tænker på analysebehov i lagerstyring, kan det hjælpe at bruge en pesona-baseret model, der beskriver forskellige analysebehov på højt niveau.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustration af forskellige personer til analyse" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Mennesker i forskellige roller har forskellige behov, når det kommer til data, og de bruger dataene på forskellige måder. Personer i aktivstyring og økonomi interagerer f.eks. anderledes med data end personer i salg.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustration af, hvordan forskellige personer har forskellige analysebehov." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rolle              | Dataopsummering  | Typiske måder at forbruge data på                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|COO / CFO / CEO    | Ydeevnedata  | KPI'er, dashboards, finansielle rapporter           |
|Lagerchef  | Tendenser, resuméer | Indbyggede ledelsesrapporter, ad hoc-analyse      | 
|Lagermedarbejder   | Detaljerede data     | Indbyggede driftsrapporter, opgavedata på skærmen |

<!-- 
## Inventory KPIs

A key performance indicator (KPI) is a measurable value that shows how effectively you’re meeting your goals. In inventory management, people often use the following KPIs to monitor their organization's sales performance:

- TODO  
-->

## Brug financial Reporting til produktion af årsregnskaber og KPI'er (relateret til lager)

Du kan bruge **Financial Reporting** til at få indsigt i de finansielle oplysninger, der er gemt i din kontoplan (COA). Du kan konfigurere finansrapporter til at analysere tal i finanskonti og sammenligner finansposter med budgetposter. Specielt til styring af lager kan du oprette finansielle rapporter på de finanskonti, som du bruger til at spore bogføring af lager.

Dimensioner spiller en vigtig rolle i Business Intelligence. En dimension er data, som du kan føje til en post som en parameter. Dimensioner kan bruges til at gruppere poster med ens karakteristika, f.eks. debitorer, regioner, produkter og sælger. Du kan blandt andre bruge dimensioner til at definere analysevisninger, og når du opretter finansrapporter. Flere oplysninger i [Arbejde med dimensioner](finance-dimensions.md).

Flere oplysninger om finansrapporter i [Forberede Financial Reporting med finansdata og kontokategorier](bi-how-work-account-schedule.md).

## Økonomirapportering på tværs af afdelinger eller juridiske enheder (relateret til lager)

Nogle organisationer bruger [!INCLUDE [prod_short](includes/prod_short.md)] i flere afdelinger eller juridiske enheder. Andre bruger [!INCLUDE [prod_short](includes/prod_short.md)] i datterselskaber, der rapporterer til overordnede organisationer. [!INCLUDE [prod_short](includes/prod_short.md)] giver bogholdere værktøjer, der kan hjælpe dem med at overføre finansposter fra to eller flere regnskaber (datterselskaber) til et konsolideret regnskab. Specielt til lagerstyring vil du måske konsolidere finansposter for dine lagerkonti for at kunne spore KPI'er for salgskonti på tværs af forretningsenheder eller juridiske enheder.

Flere oplysninger i [Virksomhedskonsolidering](finance-consolidated-company-reporting.md).

## Ad hoc-analyse af lagerdata

Nogle gange skal du bare kontrollere, om tallene tilføjes korrekt, eller hurtigt bekræfte et tal. Følgende funktioner er gode til ad hoc-analyser:

- Dataanalyse på finanslistesider
- Åbn i Excel

Med dataanalysefunktionen kan du åbne næsten enhver listeside, f.eks. **Finansposter**, skifte til analysetilstand og derefter gruppere, filtrere og pivotere data efter behov.

:::image type="content" source="media/data-analysis-inventory-dead-stock.png" alt-text="Eksempel på, hvordan du udfører en gammel lagerdataanalyse på siden Finansposter." lightbox="media/data-analysis-inventory-dead-stock.png":::

På samme måde kan du bruge handlingen **Åbn i Excel** til at åbne en listeside, eventuelt filtrere listen til et undersæt af dataene og derefter bruge Excel til at arbejde med dataene. For eksempel ved at bruge funktioner som Analysér data, Hvad hvis-analyse eller Prognoseark.

<!-- :::image type="content" source="media/open-in-excel-item-ledger-entries.png" alt-text="Example of how to do data analysis on the Item Ledger Entries data using Excel." lightbox="media/open-in-excel-item-ledger-entries.png"::: -->

> [!TIP]
> Hvis du konfigurerer OneDrive til systemfunktioner, åbnes Excel-projektmappen i browseren.

Du kan få mere at vide om, hvordan du udfører ad hoc-analyser af lagerdata, ved at gå til [Ad hoc-analyse af lagerdata](ad-hoc-analysis-inventory.md).

## Indbyggede lagerrapporter

[!INCLUDE [prod_short](includes/prod_short.md)] Indeholder flere indbyggede rapporter, sporingsfunktioner og værktøjer, der hjælper lagerorganisationer med at rapportere om deres data.

Hvis du vil have et overblik over tilgængelige rapporter, kan du klikke på **Alle rapporter** over startsiden. Denne handling åbner rapportoversigten, som filtreres til funktionerne i indstillingen **Rapport og analyse**. Under overskriften **Salg og marketing** skal du vælge **Udforsk**. Flere oplysninger i [Søg efter rapporter med Rollestifinder](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-sales.png" alt-text="Eksempel på rapporter om salgsrollecenteret." lightbox="media/report-explorer-sales.png":::

<!-- The built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Du kan få mere at vide om rapporter, der er relevante for lager, ved at gå til [Indbyggede lager- og lagerstedsrapporter](inventory-WMS-reports.md).

## Analyse af lager på skærmen

[!INCLUDE [prod_short](includes/prod_short.md)] har flere sider, der giver dig oversigter over lager og opgaver at gøre. Her er nogle eksempler på, hvordan du kommer i gang:

- [Vise varer, der er disponible](inventory-how-availability-overview.md)
- [Spore varer med serie-, lot- og pakkenumre](inventory-how-work-item-tracking.md)
- [Spore varer – sporede varer](inventory-how-to-trace-item-tracked-items.md)
- [Bruge afstemningen mellem lagerposterne og Finans](finance-how-to-post-inventory-costs-to-the-general-ledger.md#to-audit-the-reconciliation-between-the-inventory-ledger-and-the-general-ledger)
- [Vise varer til direkte afsendelse i leverancer og plukkladde](warehouse-how-to-cross-dock-items.md#to-view-cross-docked-items-in-a-shipment-or-pick-worksheet)

Salgsmodulet indeholder også analysesider relateret til lagerbeholdning:

- [Beregne ordrebekræftelsesdatoer](sales-how-to-calculate-order-promising-dates.md)
- [Beregning af leveringsdatoer for salgsordrer](sales-date-calculation-for-sales.md)
- [Spore pakker](sales-how-track-packages.md)

### Vise lagerrelaterede finansposter og saldi fra siden Kontoplan

Siden **Kontoplan** viser alle finanskonti med aggregerede tal, der bogføres i finansregnskabet. Fra denne side kan du f.eks. gøre følgende:  

- Vise rapporter med finansposter og saldi.  
- Gennemse en oversigt over bogføringsgrupper til kontoen.
- Se separate debet- og kreditsaldi for en enkelt konto.

Specielt for lagerstyring kan du oprette en visning på siden Kontoplan, der kun viser de konti, du bruger til bogføring af lagerposter.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Eksempel på, hvordan siden Kontoplan viser finansindsigt" lightbox="media/chart-of-accounts-page.png":::

Få mere at vide i [Forstå Kontoplanen](finance-general-ledger.md#the-chart-of-accounts).

### Analysere lagerdata efter dimensioner

Dimensioner er værdier, der kategoriserer poster, så du kan spore og analysere dem i dokumenter som f.eks. salgsordrer. Dimensioner kan f.eks. angive det projekt eller den afdeling, en post kommer fra.  

I stedet for at oprette separate finanskonti for hver afdeling eller lokation kan du bruge dimensioner som grundlag for analyse og undgå at skulle oprette en kompliceret kontoplanstruktur.

Få mere at vide i [Analysere data efter dimensioner](bi-how-analyze-data-dimension.md).

## Se også

[Virksomhedskonsolidering](finance-consolidated-company-reporting.md)   
[Forberede finansrapporter med finansdata og kontokategorier](bi-how-work-account-schedule.md)  
[Håndtere økonomirapportering på tværs af afdelinger eller juridiske enheder](finance-consolidated-company-reporting.md)  
[Ad hoc-analyse af lagerdata](ad-hoc-analysis-inventory.md)  
[Indbygget lager og lagerrapporter](inventory-WMS-reports.md)  
[Forstå kontoplaner](finance-general-ledger.md#the-chart-of-accounts)  
[Analysere data efter dimensioner](bi-how-analyze-data-dimension.md)  
[Analyse, Business Intelligence og rapporteringsoversigt](reports-bi-reporting.md)   
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
