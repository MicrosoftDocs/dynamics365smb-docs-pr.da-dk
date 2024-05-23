---
title: 'Analyse, Business Intelligence og rapporteringsoversigt'
description: 'Indeholder en oversigt over alle de funktioner til analyse, Business Intelligence og rapportering, som understøttes i Business Central.'
author: KennieNP
ms.topic: get-started
ms.devlang: al
ms.search.keywords: feature overview
ms.reviewer: bholtorf
ms.date: 09/22/2022
ms.author: kepontop
ms.service: dynamics-365-business-central
---

# <a name="analytics-business-intelligence-and-reporting-overview"></a>Analyse, Business Intelligence og rapporteringsoversigt

Små og mellemstore virksomheder afhænger af den indbyggede analyse og rapporteringsfunktioner, de kan bruge som standard til at holde styr på deres forretninger. [!INCLUDE[prod_short](includes/prod_short.md)] indeholder rapporter og analyseværktøjer, der dækker grundlæggende og komplekse forretningsprocesser for sådanne organisationer. Du kan også foretage ad-hoc-analyser direkte fra hjemmesiden.  

## <a name="analytics-needs-in-organizations"></a>Analysebehov i organisationer

Når du tænker på analysebehov i organisationer, kan det hjælpe at bruge en mental model baseret på personer beskrevet på et højt niveau og deres forskellige analysebehov.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustration af forskellige personer til analyse" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Modellen er baseret på, at forskellige roller i en organisation har forskellige behov, når det kommer til data. Jo højere en rolle placeres i organisationsdiagrammet, jo flere aggregerede data skal en person i rollen bruge for at udføre sit arbejde.

Roller har ofte foretrukne måder at forbruge og analysere data på, måder der afspejler det niveau af dataaggregering, de har brug for.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustration af, hvordan forskellige personer har forskellige analysebehov." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

Brug følgende afsnit til at få mere at vide om, hvordan du kan forbruge data fra [!INCLUDE[prod_short](includes/prod_short.md)]:

- Finansielle rapporter
- KPI'er og dashboards
- Ad hoc-analyse
- Rapporter

## <a name="using-financial-reports-to-produce-financial-statements-and-kpis"></a>Brug af finansrapporter til udarbejdelse af årsregnskaber og KPI'er

Funktionen Finansrapporter giver dig indsigt i de finansielle data, der er gemt i din kontoplan. Du kan konfigurere finansrapporter til at analysere tal i finanskonti og sammenligner finansposter med budgetposter.

:::image type="content" source="media/acc_schedule_13_columns.jpg" alt-text="Skærmbillede af en finansrapport." lightbox="media/acc_schedule_13_columns.jpg":::

Dimensioner spiller en vigtig rolle i Business Intelligence. En dimension er data, som du kan føje til en post som en parameter. Med dimensioner kan du gruppere poster med ensartede egenskaber. For eksempel grupper af kunder, regioner, produkter og sælger. Grupper gør det nemmere at hente data til analyse. Du kan blandt andre bruge dimensioner til at definere analysevisninger, og når du opretter finansrapporter. Flere oplysninger i [Arbejde med dimensioner](finance-dimensions.md).

Du kan få mere at vide om regnskabsopgørelser og KPI'er ved at gå til [Brug af finansrapporter til udarbejdelse af årsregnskaber og KPI'er](bi.md).

## <a name="using-key-performance-indicators-to-meet-your-business-goals"></a>Bruge nøgletal til at overholde din virksomheds mål

En KPI (Key Performance Indicator) er en målbar værdi, der viser, hvor effektivt du når dine mål. Tænk på KPI'er som din virksomheds scorecard, en måde at måle, om du leverer på dine mål.

Identifikation og sporing af KPI'er fortæller dig, om din virksomhed er på rette vej, eller om du skal ændre kurs. Når KPI'er bruges korrekt, er de effektive værktøjer, der hjælper dig med at:

- Overvåge virksomhedens økonomiske tilstand.
- Måle fremskridt i forhold til strategiske mål.
- Få øje på problemer tidligt.
- Foretage rettidige justeringer af taktikken.
- Motivere teammedlemmer.
- Træffe bedre beslutninger, hurtigere.

Du kan få mere at vide om KPI'er ved at gå til [Bruge nøgletal (KPI'er) til at overholde din virksomheds mål](./analytics-about-kpis.md)

## <a name="ad-hoc-data-analysis"></a>Ad hoc-dataanalyse

Du vil måske bare tjekke, om tallene er korrekte, hurtigt bekræfte eller aflive en hypotese om virksomheden eller måske kigge efter uregelmæssigheder i dine økonomiske data. I forbindelse med ad hoc-analyser har du muligvis ikke en indbygget rapport, der hjælper dig med at besvare dine spørgsmål. Brug disse to funktioner til ad hoc-analyser:

- Dataanalyse på finanslistesider
- Åbn i Excel

Med funktionen Dataanalyse kan du åbne næsten enhver listeside, f.eks. siderne Finansposter eller Debitorposter, skifte til analysetilstand og derefter gruppere, filtrere og pivotere data efter behov. 

:::image type="content" source="media/data-analysis-gl-entries.png" alt-text="Eksempel på, hvordan du udfører dataanalyse på siden Finansposter." lightbox="media/data-analysis-gl-entries.png":::

På samme måde kan du bruge handlingen **Åbn i Excel** til at åbne en listeside, eventuelt filtrere listen til et undersæt af dataene og derefter bruge Excel til at arbejde med dataene. For eksempel ved at bruge funktioner som Analysér data, Hvad hvis-analyse eller Prognoseark.

:::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Eksempel på, hvordan du udfører dataanalyse på siden Finansposter ved hjælp af Excel." lightbox="media/open-in-excel-gl-entries.png":::

> [!TIP]
> Hvis du konfigurerer OneDrive til systemfunktioner, åbnes Excel-projektmappen i browseren ved hjælp af Excel til World Wide Web.

Du kan få flere oplysninger om ad hoc-analyser ved at gå til [Ad hoc-dataanalyse](reports-adhoc-analysis.md).

## <a name="reports"></a>Rapporter

En rapport i [!INCLUDE[prod_short](includes/prod_short.md)] indsamler oplysninger baseret på et nærmere angivet sæt kriterier. Rapporter organiserer og præsenterer oplysningerne i et læsevenligt format, som du kan bruge i Excel, udskrive eller gemme som en fil.  

Som et eksempel på en interaktiv rapport i Excel giver rapporten ***Aldersfordelt tilgodehavende** dig mulighed for at analysere, hvad dine kunder skylder dig, og hvornår betalinger forfalder.

:::image type="content" source="media/aged-accounts-receivables-excel.png" alt-text="Eksempel på den interaktive rapport over aldersfordelte tilgodehavender i Excel." lightbox="media/aged-accounts-receivables-excel.png":::

For aldersfordelte tilgodehavender indeholder [!INCLUDE[prod_short](includes/prod_short.md)] også en rapport, der er beregnet til udskrivning. Muligheden for at udskrive er praktisk, hvis du foretrækker at have dataene i en .pdf-fil.

:::image type="content" source="media/aged-accounts-receivables-pdf.png" alt-text="Eksempel på rapporten over aldersfordelte tilgodehavender i pdf." lightbox="media/aged-accounts-receivables-pdf.png":::

[!INCLUDE[prod_short](includes/prod_short.md)] leveres med mere end 300 indbyggede rapporter, som du kan bruge til at understøtte dine forretningsprocesser med datadrevet indsigt. Hvis du vil have et hurtigt overblik over alle de rapporter, der er tilgængelige for din rolle, kan du åbne rapportoversigten fra rollecenteret og alle listesider samt fra **Fortæl mig**.

:::image type="content" source="media/report-explorer-finance.png" alt-text="Eksempel på, hvordan rapportoversigten viser alle rapporter for en rolle." lightbox="media/report-explorer-finance.png":::

Du kan få mere at vide om, hvordan du bruger rapportoversigten til at se alle indbyggede rapporter, ved at gå til [Udforske rapporter pr. rolle](ui-role-explorer.md).

Følgende tabel indeholder artikler om, hvordan du bruger indbyggede rapporter i [!INCLUDE[prod_short](includes/prod_short.md)].

| Til  | Se |
| --- | --- |
| Se, hvordan du bruger rapporter (bogmærke, køre, udskrive, planlægge og ændre layoutet). | [Bruge rapporter i dagligt arbejde](reports-use-reports.md) |
| Få mere at vide om, hvilke indbyggede rapporter der er tilgængelige i [!INCLUDE[prod_short](includes/prod_short.md)]. |[Rapportoversigt](reports-available-reports.md)| 
| Brug rapportoversigten til at se alle indbyggede rapporter. | [Udforske rapporter pr. rolle](ui-role-explorer.md) |

## <a name="external-business-intelligence-and-reporting-tools"></a>Eksterne business intelligence- og rapporteringsværktøjer

Hvis du foretrækker det, kan du bruge business intelligence-værktøjer, der ikke er integreret i [!INCLUDE[prod_short](includes/prod_short.md)]. Følgende tabel indeholder links til vejledning og måder at bruge eksterne værktøjer på.

| Til  | Se |
| --- | --- |
| Bruge Power BI sammen med Business Central-data | [Bruge Power BI med Business Central](admin-powerbi.md) |
| Integrer eksterne business intelligence-værktøjer med [!INCLUDE[prod_short](includes/prod_short.md)].| [Eksterne business intelligence-værktøjer](reports-external-analysis.md) |
| Udtrække data til datalagersteder eller Data Lake| [Sådan udtrækker du data til datalagre eller Data Lake](/dynamics365/business-central/dev-itpro/performance/performance-developer#efficient-extracts-to-data-lakes-or-data-warehouses) |
| Analysere Business Central-data med Microsoft Fabric| [Introduktion til Microsoft Fabric og Business Central](admin-fabric.md) |
| Læse data fra Business Central ved hjælp af API'er | [Business Central API v2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/) |

## <a name="analytics-by-functional-area"></a>Analytics efter funktionsområde

Det generelle indhold om analyser er også tilgængeligt i specielle versioner til mange af funktionsområderne i [!INCLUDE[prod_short](includes/prod_short.md)].

| Hvis du arbejder med... | Se |
| --- | --- |
| Finance | [Økonomisk analyse](bi.md) |
| Salg | [Salgsanalyse](sales-analytics-overview.md) |
| Indkøb | [Indkøbsanalyse](purchasing-analytics-overview.md) |
| Administration af anlægsaktiver | [Analyse af anlægsaktiver](fa-analytics-overview.md) |


## <a name="see-also"></a>Se også

[Bruge Financial Reporting til produktion af årsregnskaber og KPI'er](bi.md)  
[Bruge nøgletal (KPI'er) til at overholde din virksomheds mål](analytics-about-kpis.md)  
[Udføre ad hoc-dataanalyse](reports-adhoc-analysis.md)  
[Bruge rapporter i dit daglige arbejde](reports-use-reports.md)  
[Oversigt over indbyggede rapporter](reports-available-reports.md)  
[Udforske rapporter pr. rolle](ui-role-explorer.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
