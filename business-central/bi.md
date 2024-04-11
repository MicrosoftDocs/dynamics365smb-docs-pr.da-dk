---
title: Finansanalyser i Business Central
description: 'Business Central indeholder mange funktioner, som kan hjælpe dig med at indsamle, analysere og dele værdifulde virksomhedsdata til Business Intelligence og beslutningstagning.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: kepontop
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '103, 108, 198, 490'
ms.date: 03/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Finansanalyser i Business Central

Virksomheder indsamler en enorm mængde data under daglige aktiviteter, der understøtter værdifuld business intelligence (BI) for beslutningstagere: 

- Salgstal
- Køb
- Driftsudgifter
- Medarbejderlønninger
- Budgetter

[!INCLUDE[prod_short](includes/prod_short.md)] indeholder mange funktioner, som kan være nyttige, når du skal indsamle, analysere og dele virksomhedens finansdata.

- Financial Reporting (til regnskabsopgørelser og KPI'er)
- Ad hoc-analyse på lister
- Ad-hoc analyse af data i Excel (ved hjælp af åben i Excel)
- Indbyggede økonomiske rapporter

Hver af disse funktioner har sine egne fordele og ulemper afhængigt af typen af dataanalyse og brugerens rolle. Du kan få mere at vide ved at gå til [Analyser, Business Intelligence og Oversigt over rapportering](reports-bi-reporting.md).

I denne artikel introduceres det, at du kan bruge disse analytiske funktioner til at få økonomisk indsigt.

## Analysebehov inden for økonomi

Når man tænker på analysebehov inden for økonomi, kan det hjælpe at bruge en mental model baseret på personer beskrevet på et højt niveau og deres forskellige analysebehov.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustration af forskellige personer til analyse" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Mennesker i forskellige roller har forskellige behov, når det kommer til data, og de bruger dataene på forskellige måder. Personer i økonomi interagerer f.eks. anderledes med data end personer i salg.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustration af, hvordan forskellige personer har forskellige analysebehov." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rolle              | Dataopsummering  | Typiske måder at forbruge data på                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|CFO / CEO          | Ydeevnedata  | Nøgletal <br> Dashboards <br> Finansielle rapporter           |
|Økonomistyring | Tendenser, resuméer | Indbyggede administrative rapporter <br> Ad hoc-analyse      | 
|Bogholder         | Detaljerede data     | Indbyggede driftsrapporter <br> Opgavedata på skærmen |

## KPI'er for økonomi

En KPI (Key Performance Indicator) er en målbar værdi, der viser, hvor effektivt du når dine mål. I økonomi bruger folk ofte følgende KPI'er til at overvåge deres organisations økonomiske sundhed:

- Dækningsgrad
- Nettodækningsgrad
- Arbejdskapital
- Strøm/hurtigt-forhold
- Finansiel gearing, også kendt som aktiemultiplikatoren
- Gældskvote
- Samlet anlægsomsætning
- Forrentning af egenkapitalen
- Afkast af aktiver

<!-- Not ready to publish yet
For more information, see [Financial KPIs in Business Central](bi-finance-kpis.md) 
-->

## Brug af financial Reporting til produktion af årsregnskaber og KPI'er

Du kan bruge **finansrapporter** til at få indsigt i de finansielle oplysninger, der er gemt i din kontoplan (COA). Du kan konfigurere finansrapporter til at analysere tal i finanskonti og sammenligner finansposter med budgetposter. Resultaterne vises i diagrammer og rapporter på hjemmesiden, f.eks. tabellen Likviditet og resultatopgørelsen og balancerapporterne.

Dimensioner spiller en vigtig rolle i Business Intelligence. En dimension er data, som du kan føje til en post som en parameter. Dimensioner kan bruges til at gruppere poster med ens karakteristika, f.eks. debitorer, regioner, produkter og sælger, og disse grupper kan nemt hentes frem til analyse. Du kan blandt andre bruge dimensioner til at definere analysevisninger, og når du opretter finansrapporter. Flere oplysninger i [Arbejde med dimensioner](finance-dimensions.md).

> [!TIP]
> For hurtigt at analysere transaktionsdata kan du filtrere totaler i kontoplanen og alle poster på siden **Poster** efter dimensioner. Kig efter handlingen **Angiv dimensionsfilter**.  

Den følgende tabel indeholder en opgavesekvens i Financial Reporting med links til de artikler, der rummer beskrivelserne af opgaverne.  

| Til | Se |
| --- | --- |
| Oprette nye finansrapporter for at definere regnskaber til rapportering eller visning som diagrammer.| [Forberede finansrapporter med finansdata og kontokategorier](bi-how-work-account-schedule.md)|
| Brug statistiske konti til at supplere oplysninger i regnskabsrapporter. Med statistiske konti kan du tilføje målinger, der er baseret på ikke-transaktionsdata. Du kan tilføje ikke-transaktionsdata som talbaserede enheder, f.eks. antal medarbejdere, kvadratmeter eller antal kunder med forfaldne konti. | [Analysere data med statistiske konti](bi-use-statistical-accounts.md) |
| Få flere oplysninger om, hvordan du konfigurerer en ny økonomisk rapport ved hjælp af eksempler. | [Gennemgang: Brug Financial Reporting til at oprette en pengestrømsprognose](walkthrough-making-cash-flow-forecasts-by-using-account-schedules.md) |
| Analyser din finansielle ydeevne ved at konfigurere KPI'er baseret på finansrapporter, som du derefter publicerer som webtjenester. De publicerede finansrapporters KPI'er kan ses på et websted eller importeres i Microsoft Excel ved hjælp af OData-webtjenester. |[Konfigurere og udgive KPI-webtjenester, der er baseret på finansielle rapporter](bi-how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules.md) |
| Oprette visninger for at analysere data vha. dimensioner.|[Analysere data efter dimensioner](bi-how-analyze-data-dimension.md)|
| Oprette nye analyserapporter for salg, køb og lager og oprette analyseskabeloner. |[Oprette analyserapporter](bi-how-create-analysis-views-reports.md)|

## Økonomirapportering på tværs af afdelinger eller juridiske enheder

Nogle organisationer bruger [!INCLUDE [prod_short](includes/prod_short.md)] i flere afdelinger eller juridiske enheder. Andre bruger [!INCLUDE [prod_short](includes/prod_short.md)] i datterselskaber, der skal rapportere til overordnede organisationer. [!INCLUDE [prod_short](includes/prod_short.md)] giver bogholdere værktøjer, der kan hjælpe dem med at overføre finansposter fra to eller flere regnskaber (datterselskaber) til et konsolideret regnskab.  

Flere oplysninger i [Virksomhedskonsolidering](finance-consolidated-company-reporting.md).

## Ad hoc-analyse af finansdata

Nogle gange skal du bare kontrollere, om tallene tilføjes korrekt, eller hurtigt bekræfte et tal. Følgende funktioner er gode til ad hoc-analyser:

- Dataanalyse på finanslistesider
- Åbn i Excel

Med funktionen Dataanalyse kan du åbne næsten en listeside, f.eks. Finansposter, Anlægsposter, Checkposter eller Bankposter, skifte til analysetilstand og derefter gruppere, filtrere og pivotere data efter behov.

:::image type="content" source="media/data-analysis-gl-entries.png" alt-text="Eksempel på, hvordan du udfører dataanalyse på siden Finansposter." lightbox="media/data-analysis-gl-entries.png":::

På samme måde kan du bruge handlingen **Åbn i Excel** til at åbne en listeside for finansposter, eventuelt filtrere listen til et undersæt af dataene og derefter bruge Excel til at arbejde med dataene. For eksempel ved at bruge funktioner som Analysér data, Hvad hvis-analyse eller Prognoseark.

:::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Eksempel på, hvordan du udfører dataanalyse på siden Finansposter ved hjælp af Excel." lightbox="media/open-in-excel-gl-entries.png":::

> [!TIP]
> Hvis du konfigurerer OneDrive til systemfunktioner, åbnes Excel-projektmappen i browseren ved hjælp af Excel til World Wide Web. 

<!-- Not ready yet
For more information on how to do ad-hoc analysis on ledgers, see [Ad-hoc analysis on finance data](ad-hoc-analysis-finance.md). 
-->
## Indbyggede økonomiske rapporter

[!INCLUDE [prod_short](includes/prod_short.md)] indeholder flere indbyggede rapporter, sporingsfunktioner og værktøjer, som kan hjælpe revisorer eller controllere, som er ansvarlige for at rapportere til finansafdelingen.

Hvis du vil have et overblik over tilgængelige rapporter, kan du klikke på **Alle rapporter** i den øverste rude på startsiden. Dette fører dig til rollestifinderen, som filtreres til funktionerne i indstillingen **Rapport og analyse**. Flere oplysninger i [Søg efter rapporter med Rollestifinder](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-finance.png" alt-text="Eksempel på rapporter om økonomirollecenteret." lightbox="media/report-explorer-finance.png":::

Indbyggede rapporter findes i to varianter:

- Designet til print (pdf).
- Designet til analyse i Excel.

Du kan finde flere oplysninger i disse oversigter for rapporter, der er relevante for økonomi.

- [Indbyggede økonomiske Excel-rapporter](finance-analyze-excel.md)
- [Indbyggede vigtige økonomiske rapporter](finance-reports.md)
- [Indbyggede anlægsrapporter](fa-reports.md)
- [Indbyggede rapporter med tilgodehavender](receivables-reports.md)
- [Indbyggede kreditorrapporter](payables-reports.md)

<!-- TODO: add when we have these articles
* [Built-in Cost Accounting reports](cost-accounting-reports.md) 
* [Built-in Cash Management reports](cost-accounting-reports.md) 
* [Built-in Tax and VAT reports](tax-and-vat-reports.md) 
-->

## Opgavesider for økonomi på skærmen

[!INCLUDE [prod_short](includes/prod_short.md)] har et antal sider, der giver dig økonomiske oversigter og opgaver at gøre.

### Vise finansposter og saldi fra siden Kontoplan

Siden Kontoplan viser alle finanskonti med aggregerede tal på det, der bogføres i finansregnskabet. Fra denne side kan du f.eks. gøre følgende:  

- Vise rapporter med finansposter og saldi.  
- Gennemse en oversigt over bogføringsgrupper til kontoen.
- Se separate debet- og kreditsaldi for en enkelt konto.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Eksempel på, hvordan siden Kontoplan viser finansindsigt" lightbox="media/chart-of-accounts-page.png":::

Få mere at vide i [Forstå Kontoplanen](finance-general-ledger.md#the-chart-of-accounts).

### Få vist budgetter, og faktiske beløb sammenlignet med budgetterede beløb for alle konti og for flere perioder

Som et led i indsamling, analyse og deling af virksomhedens data kan du få vist faktiske beløb sammenlignet med budgetterede beløb for alle konti og for flere perioder. Du kan gøre dette fra siden **Kontoplan** ved at vælge handlingen **Finans - saldi/budget**.

Du kan få flere oplysninger ved at gå til [Analyse af faktiske beløb sammenlignet med budgetterede beløb](bi-how-analyze-actual-versus-budget.md).

### Analysere data efter dimensioner

Dimensioner er værdier, der kategoriserer poster, så du kan spore og analysere dem i dokumenter som f.eks. salgsordrer. Dimensioner kan f.eks. angive det projekt eller den afdeling, en post kommer fra.  

I stedet for at oprette separate finanskonti for hver afdeling og hvert projekt kan du bruge dimensioner som grundlag for analyse og undgå at skulle oprette en kompliceret kontoplanstruktur.

I finansielle analyser er en dimension data, som du kan føje til en finanspost som en slags markør. Disse data bruges til at gruppere finansposter med ens karakteristika, f.eks. debitorer, regioner, produkter og sælger, og disse grupper kan nemt hentes frem til analyse. Du kan bruge dimensioner til poster i kladder, dokumenter og budgetter. Du kan finde flere oplysninger i [Analysere data efter dimensioner](bi-how-analyze-data-dimension.md)

### Analyse af pengestrømme

På hjemmesiden Revisor under **Finansydeevne** giver diagrammerne Kassebeholdningsproces, Pengestrøm og Indtægter og udgifter dig måder at analysere pengestrømme på:

- Gennemse tallene i en periode ved hjælp af tidslinjeskyderen.
- Filtrer diagrammet ved at vælge kilden i forklaringen.
- Skift tidsrum, eller gå til forrige eller næste periode ved at vælge indstillinger i rullemenuen Finansydeevne.

:::image type="content" source="media/cashflow-accountant-rolecentre.png" alt-text="Eksempel på, hvordan pengestrømsvisualiseringerne ser ud i rollecenteret for revisor" lightbox="media/cashflow-accountant-rolecentre.png":::

Hvis du vil undersøge prognosen ud over prognoseposter, kan du også se pengestrømskladden. Du kan f.eks. se, hvordan prognosen:

- Håndterer bekræftede salg og køb.
- Fratrækker skyldige beløb og tilføjer tilgodehavender.
- Springer dubletter af salgsordrer og købsordrer over.

Få mere at vide i [Analysere pengestrømme i din virksomhed](finance-analyze-cash-flow.md).

## Se også

[Håndtere økonomirapportering på tværs af afdelinger eller juridiske enheder](finance-consolidated-company-reporting.md)  
<!-- [Financial KPIs in Business Central](bi-finance-kpis.md)    -->
[Forberede finansrapporter med finansdata og kontokategorier](bi-how-work-account-schedule.md)  
<!-- [Ad-hoc analysis on finance data](ad-hoc-analysis-finance.md)   -->
[Forstå kontoplaner](finance-general-ledger.md#the-chart-of-accounts)  
[Indbyggede økonomiske Excel-rapporter](finance-analyze-excel.md)  
[Indbyggede vigtige økonomiske rapporter](finance-reports.md)  
[Indbyggede anlægsrapporter](fa-reports.md)  
[Indbyggede rapporter med tilgodehavender](receivables-reports.md)  
[Indbyggede kreditorrapporter](payables-reports.md)  
[Oversigt for Finance](finance.md)  
[Analyse, Business Intelligence og rapporteringsoversigt](reports-bi-reporting.md)   
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
