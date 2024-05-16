---
title: Salgsanalyse
description: 'Business Central indeholder mange funktioner, som kan hjælpe dig med at indsamle, analysere og dele værdifulde salgsdata til Business Intelligence og beslutningstagning i salgsorganisation.'
author: kennienp
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 04/28/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Salgsanalyse

Virksomheder indsamler store mængder data under daglige aktiviteter, der understøtter værdifuld business intelligence (BI) for salgsmedarbejdere:

- Salgsmuligheder
- Salgskvoter
- Salgsordrer
- Salgsfakturaer

[!INCLUDE[prod_short](includes/prod_short.md)] indeholder funktioner, som kan være nyttige, når du skal indsamle, analysere og dele virksomhedens salgsdata:

- Ad hoc-analyse på lister
- Ad-hoc analyse af data i Excel (ved hjælp af Åbn i Excel)
- Indbyggede værktøjer til salgsanalyse
- Indbyggede salgsrapporter

Hver af disse funktioner har sine fordele og ulemper afhængigt af typen af dataanalyse og brugerens rolle. Du kan få mere at vide ved at gå til [Analyser, Business Intelligence og Oversigt over rapportering](reports-bi-reporting.md).

I denne artikel introduceres det, hvordan du kan bruge disse analytiske funktioner til at få Sales Insights.

## Analysebehov inden for salg

Når du tænker på analysebehov i salgsstyring, kan det hjælpe at bruge en pesona-baseret model, der beskriver forskellige analysebehov på højt niveau.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustration af forskellige personer til analyse" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Mennesker i forskellige roller har forskellige behov, når det kommer til data, og de bruger dataene på forskellige måder. Personer i aktivstyring og økonomi interagerer f.eks. anderledes med data end personer i salg.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustration af, hvordan forskellige personer har forskellige analysebehov." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rolle              | Dataopsummering  | Typiske måder at forbruge data på                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|CCO / CFO / CEO    | Ydeevnedata  | Nøgletal <br> Dashboards <br> Finansielle rapporter           |
|Salgschef      | Tendenser, resuméer | Indbyggede administrative rapporter <br> Ad hoc-analyse      | 
|Account Manager / Sælger | Detaljerede data     | Indbyggede driftsrapporter <br> Opgavedata på skærmen |

<!-- 
## Sales KPIs

A key performance indicator (KPI) is a measurable value that shows how effectively you’re meeting your goals. In sales management, people often use the following KPIs to monitor their organization's sales performance:

- TODO  
-->

## Brug financial Reporting til produktion af årsregnskaber og KPI'er relateret til salg

Du kan bruge **Financial Reporting** til at få indsigt i de finansielle oplysninger, der er gemt i din kontoplan (COA). Du kan konfigurere finansrapporter til at analysere tal i finanskonti og sammenligner finansposter med budgetposter. Specielt til styring af salg kan du oprette finansielle rapporter på de finanskonti, som du bruger til at spore bogføring af salg.

Dimensioner spiller en vigtig rolle i Business Intelligence. En dimension er data, som du kan føje til en post som en parameter. Dimensioner kan bruges til at gruppere poster med ens karakteristika, f.eks. debitorer, regioner, produkter og sælger. Du kan blandt andre bruge dimensioner til at definere analysevisninger, og når du opretter finansrapporter. Flere oplysninger i [Arbejde med dimensioner](finance-dimensions.md).

Flere oplysninger om finansrapporter i [Forberede Financial Reporting med finansdata og kontokategorier](bi-how-work-account-schedule.md).

## Økonomirapportering på tværs af afdelinger eller juridiske enheder relateret til salg

Nogle organisationer bruger [!INCLUDE [prod_short](includes/prod_short.md)] i flere afdelinger eller juridiske enheder. Andre bruger [!INCLUDE [prod_short](includes/prod_short.md)] i datterselskaber, der rapporterer til overordnede organisationer. [!INCLUDE [prod_short](includes/prod_short.md)] giver bogholdere værktøjer, der kan hjælpe dem med at overføre finansposter fra to eller flere regnskaber (datterselskaber) til et konsolideret regnskab. Specielt til salgsstyring vil du måske konsolidere finansposter for dine anlægskonti for at kunne spore KPI'er for salgskonti på tværs af forretningsenheder eller juridiske enheder.

Flere oplysninger i [Virksomhedskonsolidering](finance-consolidated-company-reporting.md).

## Ad hoc-analyse af salgsdata

Nogle gange skal du bare kontrollere, om tallene tilføjes korrekt, eller hurtigt bekræfte et tal. Følgende funktioner er gode til ad hoc-analyser:

- Dataanalyse på finanslistesider
- Åbn i Excel

Med funktionen Analyse kan du åbne næsten enhver listeside, f.eks. siderne **Finansposter**, **Debitorposter**, **Vareposter** eller **Bogførte fakturaer**, skifte til analysetilstand og derefter gruppere, filtrere og pivotere data efter behov.

:::image type="content" source="media/data-analysis-customer-ledger-entries.png" alt-text="Eksempel på, hvordan du udfører dataanalyse på siden Finansposter." lightbox="media/data-analysis-customer-ledger-entries.png":::

På samme måde kan du bruge handlingen **Åbn i Excel** til at åbne en listeside, eventuelt filtrere listen til et undersæt af dataene og derefter bruge Excel til at arbejde med dataene. For eksempel ved at bruge funktioner som Analysér data, Hvad hvis-analyse eller Prognoseark.

:::image type="content" source="media/open-in-excel-customer-ledger-entries.png" alt-text="Eksempel på, hvordan du udfører dataanalyse på siden Finansposter ved hjælp af Excel." lightbox="media/open-in-excel-customer-ledger-entries.png":::

> [!TIP]
> Hvis du konfigurerer OneDrive til systemfunktioner, åbnes Excel-projektmappen i browseren.

Du kan få mere at vide om, hvordan du udfører ad hoc-analyser af salgsdata, ved at gå til [Ad hoc-analyse af salgsdata](ad-hoc-analysis-sales.md). 

## Indbyggede salgsrapporter

[!INCLUDE [prod_short](includes/prod_short.md)] Indeholder flere indbyggede rapporter, sporingsfunktioner og værktøjer, der hjælper salgsorganisationer med at rapportere om deres data.

Hvis du vil have et overblik over tilgængelige rapporter, kan du klikke på **Alle rapporter** i den øverste rude på startsiden. Denne handling åbner Rollestifinder, som filtreres til funktionerne i indstillingen **Rapport og analyse**. Flere oplysninger i [Søg efter rapporter med Rollestifinder](ui-role-explorer.md). 

:::image type="content" source="media/report-explorer-sales.png" alt-text="Eksempel på rapporter om salgsrollecenteret." lightbox="media/report-explorer-sales.png":::

Indbyggede rapporter findes i to varianter:

- Designet til print (pdf).
- Designet til analyse i Excel.

Du kan få mere at vide om rapporter, der er relevante for salg, ved at gå til [Indbyggede salgsrapporter](sales-reports.md).

## Analyse af salg på skærmen

[!INCLUDE [prod_short](includes/prod_short.md)] har flere sider, der giver dig oversigter over salg og opgaver at gøre. Her er nogle eksempler på, hvordan du kommer i gang:

- [Åbn listen **Salgstilbud**](https://businesscentral.dynamics.com/?page=9300)
- [Åbn listen **Salgsordrer**](https://businesscentral.dynamics.com/?page=9305)
- [Åbn listen **Bogførte salgsfakturaer**](https://businesscentral.dynamics.com/?page=143)
- [Åbn listen **Salgsreturordrer**](https://businesscentral.dynamics.com/?page=9304)
- [Beregne ordrebekræftelsesdatoer](sales-how-to-calculate-order-promising-dates.md)
- [Beregning af leveringsdatoer for salgsordrer](sales-date-calculation-for-sales.md)
- [Spore pakker](sales-how-track-packages.md)
- [Vise varer, der er disponible](inventory-how-availability-overview.md)
- [Status af rammesalgsordre](sales-how-to-create-blanket-sales-orders.md#to-view-the-status-of-a-blanket-sales-order)
- [Vis ikke-bogførte og bogførte rammesalgsordrelinjer](sales-how-to-create-blanket-sales-orders.md#to-view-unposted-and-posted-blanket-sales-order-lines)


### Vise salgsrelaterede finansposter og saldi fra siden Kontoplan

Siden Kontoplan viser alle finanskonti med aggregerede tal, der bogføres i finansregnskabet. Fra denne side kan du f.eks. gøre følgende:  

- Vise rapporter med finansposter og saldi.  
- Gennemse en oversigt over bogføringsgrupper til kontoen.
- Se separate debet- og kreditsaldi for en enkelt konto.

Specielt for salg kan du oprette en visning på siden Kontoplan, der kun viser de konti, du bruger til bogføring af salgsposter.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Eksempel på, hvordan siden Kontoplan viser finansindsigt" lightbox="media/chart-of-accounts-page.png":::

Få mere at vide i [Forstå Kontoplanen](finance-general-ledger.md#the-chart-of-accounts).

### Analysere data efter dimensioner (relateret til salg)

Dimensioner er værdier, der kategoriserer poster, så du kan spore og analysere dem i dokumenter som f.eks. salgsordrer. Dimensioner kan f.eks. angive det projekt eller den afdeling, en post kommer fra.  

I stedet for at oprette separate finanskonti for hver afdeling eller lokation kan du bruge dimensioner som grundlag for analyse og undgå at skulle oprette en kompliceret kontoplanstruktur.

Få mere at vide i [Analysere data efter dimensioner](bi-how-analyze-data-dimension.md).

## Se også

[Virksomhedskonsolidering](finance-consolidated-company-reporting.md)   
[Forberede finansrapporter med finansdata og kontokategorier](bi-how-work-account-schedule.md)  
[Håndtere økonomirapportering på tværs af afdelinger eller juridiske enheder](finance-consolidated-company-reporting.md)  
[Ad hoc-analyse af salgsdata](ad-hoc-analysis-sales.md)   
[Indbyggede salgsrapporter](sales-reports.md)   
[Forstå kontoplaner](finance-general-ledger.md#the-chart-of-accounts)  
[Analysere data efter dimensioner](bi-how-analyze-data-dimension.md)  
[Analyse, Business Intelligence og rapporteringsoversigt](reports-bi-reporting.md)   
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
