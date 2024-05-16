---
title: Ad hoc-analyse af data i anlægsaktiver
description: 'Få mere at vide om, hvordan du kan bruge dataanalysetilstand til at analysere data i analysetilstand.'
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '5604, 20'
ms.date: 05/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Ad hoc-analyse af data i anlægsaktiver

I artikel beskriver, hvordan du bruger funktionen **Dataanalyse** til at analysere anlægsaktiver direkte fra listesider og forespørgsler. Du behøver ikke at køre en rapport eller skifte til et andet program, f.eks. Excel. Funktionen indeholder en interaktiv og alsidig måde at beregne, opsummere og gennemgå data på. I stedet for at køre rapporter med indstillinger og filtre kan du tilføje flere faner, der repræsenterer forskellige opgaver eller visninger på dataene. Nogle eksempler er "Aktiver i alt", "Afskrivninger over tid" eller enhver anden visning, du kan forestille dig. Du kan få mere at vide om, hvordan du bruger funktionen **Dataanalyse** ved at gå til [Analysér liste og forespørge på data med analysetilstand](analysis-mode.md).

Brug følgende listesider for at starte en ad hoc-analyse af anlægsaktivsprocesser:

- [Anlægsfinansposter](https://businesscentral.dynamics.com/?page=5604)
- [Finansposter](https://businesscentral.dynamics.com/?page=20)

## Anlægsaktiver ad hoc-analysescenarier

Brug funktionen **Dataanalyse** til hurtig faktatjek og ad hoc-analyse:

- Hvis du ikke vil køre en rapport.
- Hvis der ikke er en rapport om dine specifikke behov.
- Hvis du hurtigt vil gentage for at få et godt overblik over en del af din virksomhed.

Følgende afsnit indeholder eksempler på faste anlægsscenarier i [!INCLUDE [prod_short](includes/prod_short.md)].

| Område | Til... | Åbn denne side i analysetilstand | Brug af disse felter |
| ---- | ----- | ------------------------------- |------------------- |
| [Anlægsaktiver (nutidsværdi)](#example-fixed-assets-current-value) | Spor aktivværdien, både på tværs af alle aktiver og på et enkelt aktiv. | [Anlægsfinansposter](https://businesscentral.dynamics.com/?page=5604) | **Afskrivningsprofil**, **Anlægsnr.**, **Bogføringsdato for anlæg**, **Anlægsbogføringstype** og **Beløb** |
|[Eksempel: afskrivning af anlægsaktiver over tid](#example-fixed-asset-depreciations-over-time) | Spor afskrivninger over tid, både på tværs af alle aktiver og på et enkelt aktiv. | [Anlægsfinansposter](https://businesscentral.dynamics.com/?page=5604) | **Afskrivningsprofil**, **Anlægsnr.**, **Bogføringsdato for anlæg**, **Anlægsbogføringstype**, **Beløb** og **Anlægsbogføringstype** |

### Eksempel: anlægsaktiver med nutidsværdi

Følg disse trin for at spore værdien af et eller flere anlægsaktiver:

1. Åbn [Anlægsposter for varer](https://businesscentral.dynamics.com/?page=5604)-listen, og vælg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivér analysetilstand."::: tænd for analysetilstand.
1. Gå til menuen **Kolonner**, og fjern alle kolonner (markér feltet ud for feltet **Søg** i højre side).
1. Træk **afskrivningsprofilen** og **anlægsnummeret** til området **Rækkegrupper**.
1. Vælg felterne **Anlægsdato** og **Anlægsbogføringstype**.
1. Træk feltet **Beløb** til området **Værdier**.
1. Omdøb din analysefane til **Oversigt over aktiv - værdi** eller noget, der beskriver denne analyse.

Følgende billede viser resultatet af disse trin.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png" alt-text="Eksempel på, hvordan du kan udføre dataanalyse på siden Anlægsposter for at se værdien af et aktiv." lightbox="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png":::

### Eksempel: afskrivning af anlægsaktiver over tid

Følg disse trin for at spore afskrivningen af et eller flere anlægsaktiver:

1. Åbn [Anlægsposter for varer](https://businesscentral.dynamics.com/?page=5604)-listen, og vælg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivér analysetilstand."::: tænd for analysetilstand.
1. Gå til menuen **Kolonner**, og fjern alle kolonner (markér feltet ud for feltet **Søg** i højre side).
1. Aktiver **Pivot* tilstand** (placeret direkte over **Søg** feltet i højre side).
1. Træk **afskrivningsprofilen** og **anlægsnummeret** til området **Rækkegrupper**.
1. Træk felterne **Bogføringsår for anlæg** og **Bogføringsmåned for anlæg** til området **Kolonnenavne**.
1. Træk feltet **Beløb** til området **Værdier**.
1. I filteret **Anlægsbogføringstype** skal du vælge **Afskrivning**.
1. Omdøb din analysefane til **Afskrivninger over tid** eller noget, der beskriver denne analyse for dig.

Følgende billede viser resultatet af disse trin.

:::image type="content" source="media/data-analysis-fa-ledger-entries-depreciation-by-asset.png" alt-text="Eksempel på, hvordan du kan udføre dataanalyse på siden Anlægsposter for at se afskrivning over tid." lightbox="media/data-analysis-fa-ledger-entries-depreciation-by-asset.png":::

## Datagrundlag for ad-hoc analyse af anlægsaktiver

Når du bogfører anlægskladder [!INCLUDE [prod_short](includes/prod_short.md)], oprettes der poster i tabellen **Anlægspost**. Derfor udføres ad hoc-analyser af anlægsaktiver typisk på siden [Anlægsposter](https://businesscentral.dynamics.com/?page=5604).

## Se også

[Analysere liste- og forespørgselsdata med analysetilstand](analysis-mode.md)  
[Oversigt over anlægsaktivsanalyser](fa-analytics-overview.md)  
[Analyse, Business Intelligence og rapporteringsoversigt](reports-bi-reporting.md)  
[Oversigt over anlægsaktiver](fa-manage.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]