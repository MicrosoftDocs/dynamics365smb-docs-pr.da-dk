---
title: Analyse af anlægsaktiver
description: 'Få mere at vide om, hvordan du indsamler, analyserer og deler data om anlægsaktiver til business intelligence.'
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '5601, 5600, 5615, 5616, 5617'
ms.date: 04/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Analyse af anlægsaktiver

Virksomheder med anlægsaktiver indsamler en masse data om dem under de daglige aktiviteter. Disse data understøtter værdifuld business intelligence (BI) for anlægsforvaltere:

- Anlægsanskaffelse
- Udfasning af aktiver
- Forsikring og vedligeholdelse
- Anlægsbudgetter

[!INCLUDE[prod_short](includes/prod_short.md)] indeholder funktioner, som kan være nyttige, når du skal indsamle, analysere og dele data om virksomhedens anlægsaktiver.

- Financial reporting (til regnskabsopgørelser og KPI'er om anlægskonti)
- Ad hoc-analyse på lister
- Ad-hoc analyse af data i Excel (ved hjælp af åben i Excel)
- Indbyggede anlægsaktivers analyseværktøjer
- Indbyggede anlægsrapporter

> [!NOTE]
> Analyser for anlægsaktiver er lidt anderledes end i andre områder. Du skal analysere data, der allerede findes, f.eks. anskaffelse af aktiver, udfasning og forsikring, men også data om fremtidige (forventede) data, f.eks. afskrivning og tilbagetrækning af aktiver. For sidstnævnte type analyse har [!INCLUDE[prod_short](includes/prod_short.md)] indbyggede rapporter, der kan beregne disse tal.

Hver funktion har sine egne fordele og ulemper afhængigt af typen af dataanalyse og brugerens rolle. Du kan få mere at vide ved at gå til [Analyser, Business Intelligence og Oversigt over rapportering](reports-bi-reporting.md).

I denne artikel beskrives, hvordan du kan bruge disse analysefunktioner til at få indsigt i anlægsaktiverne.

## Analysebehov i aktivstyring

Når man tænker på analysebehov inden for aktivstyring, kan det hjælpe at bruge en persona-baseret model, der beskriver deres analysebehov på et højt niveau.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustration af forskellige personer til analyse" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Når det angå data, har personer i forskellige roller forskellige behov, og de bruger dataene på forskellige måder. Personer i aktivstyring og økonomi interagerer f.eks. anderledes med data end personer i salg.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustration af, hvordan forskellige personer har forskellige analysebehov." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rolle              | Dataopsummering  | Typiske måder at forbruge data på                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|CFO / COO / CEO                 | Ydeevnedata  | Nøgletal <br> Dashboards <br> Finansielle rapporter           |
|Aktivstyring / Controller   | Tendenser, resuméer | Indbyggede administrative rapporter <br> Ad hoc-analyse      | 
|Bogholder                      | Detaljerede data     | Indbyggede driftsrapporter <br> Opgavedata på skærmen |

## Aktivstyring KPI'er

En KPI (Key Performance Indicator) er en målbar værdi, der viser, hvor effektivt du når dine mål. I aktivstyring bruger folk ofte følgende KPI'er til at overvåge deres organisations brug af aktiver:

- Samlet anlægsomsætning
- Afkast af aktiver

## Brug financial Reporting til produktion af årsregnskaber og KPI'er relateret til faste aktiver

Du kan bruge **Financial Reporting** til at få indsigt i de finansielle oplysninger, der er gemt i din kontoplan (COA). Du kan konfigurere finansrapporter til at analysere tal i finanskonti og sammenligner finansposter med budgetposter. Specielt til styring af aktiver kan du oprette finansielle rapporter på de finanskonti, som du bruger til at spore bogføring af anlægsaktiver.

Dimensioner spiller en vigtig rolle i Business Intelligence. En dimension er data, som du kan føje til en post som en parameter. Dimensioner kan bruges til at gruppere poster med ens karakteristika, f.eks. debitorer, produkter og sælger, og disse grupper kan nemt hentes frem til analyse. Du kan blandt andre bruge dimensioner til at definere analysevisninger, og når du opretter finansrapporter. Flere oplysninger i [Arbejde med dimensioner](finance-dimensions.md).

Flere oplysninger om finansrapporter i [Forberede finansielle rapporter med finansdata og kontokategorier](bi-how-work-account-schedule.md).

## Økonomirapportering på tværs af afdelinger eller juridiske enheder (relateret til faste aktiver)

Nogle organisationer bruger [!INCLUDE [prod_short](includes/prod_short.md)] i flere afdelinger eller juridiske enheder. Andre bruger [!INCLUDE [prod_short](includes/prod_short.md)] i datterselskaber, der skal rapportere til overordnede organisationer. [!INCLUDE [prod_short](includes/prod_short.md)] giver bogholdere værktøjer, der kan hjælpe dem med at overføre finansposter fra to eller flere regnskaber (datterselskaber) til et konsolideret regnskab. Specielt til styring af aktiver vil du måske konsolidere finansposter for dine anlægskonti for at kunne spore KPI'er for anlægsaktiver på tværs af forretningsenheder eller juridiske enheder.

Flere oplysninger i [Virksomhedskonsolidering](finance-consolidated-company-reporting.md).

## Ad hoc-analyse af data i anlægsaktiver

Nogle gange skal du bare kontrollere, om tallene tilføjes korrekt, eller hurtigt bekræfte et tal. Følgende funktioner er gode til ad hoc-analyser:

- Dataanalyse på finanslistesider
- Åbn i Excel

Med dataanalysefunktionen kan du åbne næsten enhver listeside, f.eks. siderne **Finansposter** eller **Anlægsposter**, skifte til analysetilstand og derefter gruppere, filtrere og pivotere data efter behov.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png" alt-text="Eksempel på, hvordan du kan udføre dataanalyse på siden Anlægsposter for at se værdien af et aktiv." lightbox="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png":::

På samme måde kan du bruge handlingen **Åbn i Excel** til at åbne en listeside for finansposter, eventuelt filtrere listen til et undersæt af dataene og derefter bruge Excel til at arbejde med dataene. For eksempel ved at bruge funktioner som Analysér data, Hvad hvis-analyse eller Prognoseark.

<!-- :::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Example of how to do data analysis on the G/L entries data using Excel." lightbox="media/open-in-excel-gl-entries.png"::: -->

> [!TIP]
> Hvis du konfigurerer OneDrive til systemfunktioner, åbnes Excel-projektmappen i browseren ved hjælp af Excel til World Wide Web. 

Du kan finde flere oplysninger om, hvordan du udfører ad hoc-analyser af anlægsposter, i [Ad hoc-analyse af anlægsdata](ad-hoc-analysis-fa.md).


## Indbyggede rapporter til anlægsaktiver

[!INCLUDE [prod_short](includes/prod_short.md)] indeholder flere indbyggede rapporter, sporingsfunktioner og værktøjer, som kan hjælpe revisorer eller controllere, som rapporterer om faste aktiver.

Hvis du vil have et overblik over tilgængelige rapporter, kan du klikke på **Alle rapporter** i den øverste rude på startsiden. Denne handling åbner siden Rollestifinder, som filtreres til funktionerne i indstillingen **Rapport og analyse**. Hvis du vil finde rapporter vedrørende anlægsaktiver, skal du angive **anlægsaktiver** i feltet **Find**. Flere oplysninger i [Søg efter rapporter med Rollestifinder](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-fixed-assets.png" alt-text="Eksempel på rapporter om økonomirollecenteret." lightbox="media/report-explorer-fixed-assets.png":::

<!-- Built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Yderligere oplysninger om rapporter, der er relevante for anlægsaktiver, finder du i [Indbyggede anlægsrapporter](fa-reports.md).

## Anlægsaktivers analyser på skærmen

[!INCLUDE [prod_short](includes/prod_short.md)] har flere sider, der giver dig oversigter over faste aktiver og opgaver at gøre. Her er nogle eksempler på, hvordan du kommer i gang:

- [Beregne afskrivning, bogføre afskrivning og analysere afskrivning](fa-how-depreciate-amortize.md)
- [Overvåge reparationsomkostninger](fa-how-maintain.md#to-monitor-maintenance-costs)
- [Overvåge forsikringsdækning](fa-how-insure.md#to-monitor-insurance-coverage)
- [Vise ændrede afskrivningsprofilværdier](fa-how-trans-split-combine.md#to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification)
- [Vise anlægsposter](fa-how-dispose-retire.md#to-view-disposal-ledger-entries)
- [Vise forventede salgsværdier](fa-how-manage-budgets.md#to-view-projected-disposal-values)

### Vise poster til finanskladden for anlægsaktiver og saldi fra siden Kontoplan

Siden Kontoplan viser alle finanskonti med aggregerede tal i finansregnskabet. Fra denne side kan du f.eks. gøre følgende:  

- Vise rapporter med finansposter og saldi.  
- Gennemse en oversigt over bogføringsgrupper til kontoen.
- Se separate debet- og kreditsaldi for en enkelt konto.

Specielt for anlægsaktiver kan du oprette en visning på siden Kontoplan, der kun viser de aktivkonti - eller måske kun de aktivkonti, du bruger til bogføring af anlægsposter.

:::image type="content" source="media/chart-of-accounts-page-fa.png" alt-text="Eksempel på, hvordan siden Kontoplan viser finansindsigt" lightbox="media/chart-of-accounts-page-fa.png":::

Få mere at vide i [Forstå Kontoplanen](finance-general-ledger.md#the-chart-of-accounts).

### Analysere data efter dimensioner (relateret til anlægsaktiver)

Dimensioner er værdier, der kategoriserer poster, så du kan spore og analysere dem i dokumenter som f.eks. anlægskladder. Dimensioner kan f.eks. angive det projekt eller den afdeling eller lokation, en post kommer fra.  

I stedet for at oprette separate finanskonti for hver afdeling eller lokation kan du bruge dimensioner som grundlag for analyse og undgå at skulle oprette en kompliceret kontoplanstruktur.

Få mere at vide i [Analysere data efter dimensioner](bi-how-analyze-data-dimension.md)

## Se også

[Håndtere økonomirapportering på tværs af afdelinger eller juridiske enheder](finance-consolidated-company-reporting.md)  
[Forberede finansrapporter med finansdata og kontokategorier](bi-how-work-account-schedule.md)  
[Forstå kontoplaner](finance-general-ledger.md#the-chart-of-accounts)  
[Ad hoc-analyse af data i anlægsaktiver](ad-hoc-analysis-fa.md)   
[Indbyggede anlægsrapporter](fa-reports.md)  
[Analyse, Business Intelligence og rapporteringsoversigt](reports-bi-reporting.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
