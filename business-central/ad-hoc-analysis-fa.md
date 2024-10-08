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

# <a name="ad-hoc-analysis-of-fixed-assets-data"></a>Ad hoc-analyse af data i anlægsaktiver

I artikel beskriver, hvordan du bruger funktionen **Dataanalyse** til at analysere anlægsaktiver direkte fra listesider og forespørgsler. Du behøver ikke at køre en rapport eller skifte til et andet program, f.eks. Excel. Funktionen indeholder en interaktiv og alsidig måde at beregne, opsummere og gennemgå data på. I stedet for at køre rapporter med indstillinger og filtre kan du tilføje flere faner, der repræsenterer forskellige opgaver eller visninger på dataene. Nogle eksempler er "Aktiver i alt", "Afskrivninger over tid" eller enhver anden visning, du kan forestille dig. Du kan få mere at vide om, hvordan du bruger funktionen **Dataanalyse** ved at gå til [Analysér liste og forespørge på data med analysetilstand](analysis-mode.md).

Brug følgende listesider for at starte en ad hoc-analyse af anlægsaktivsprocesser:

- [Anlægsfinansposter](https://businesscentral.dynamics.com/?page=5604)
- [Finansposter](https://businesscentral.dynamics.com/?page=20)

## <a name="fixed-assets-ad-hoc-analysis-scenarios"></a>Anlægsaktiver ad hoc-analysescenarier

Brug funktionen **Dataanalyse** til hurtig faktatjek og ad hoc-analyse:

- Hvis du ikke vil køre en rapport.
- Hvis der ikke er en rapport om dine specifikke behov.
- Hvis du hurtigt vil gentage for at få et godt overblik over en del af din virksomhed.

Følgende afsnit indeholder eksempler på faste anlægsscenarier i [!INCLUDE [prod_short](includes/prod_short.md)].

| Område | Til... | Åbn denne side i analysetilstand | Brug af disse felter |
| ---- | ----- | ------------------------------- |------------------- |
| [Anlægsaktiver (nutidsværdi)](#example-fixed-assets-current-value) | Spor aktivværdien, både på tværs af alle aktiver og på et enkelt aktiv. | [Anlægsfinansposter](https://businesscentral.dynamics.com/?page=5604) | **Afskrivningsprofil**, **Anlægsnr.**, **Bogføringsdato for anlæg**, **Anlægsbogføringstype** og **Beløb** |
| [Aktivværdien ændres over tid](#example-asset-value-changes-over-time) | Spor aktivværdien ændres over tid. | [Anlægsfinansposter](https://businesscentral.dynamics.com/?page=5604) | **Anlægsbogføringstype**, **Anlægsbogføringsdato** og **Beløb** |
|[Afskrivning af anlægsaktiver over tid](#example-fixed-asset-depreciations-over-time) | Spor afskrivninger over tid, både på tværs af alle aktiver og på et enkelt aktiv. | [Anlægsfinansposter](https://businesscentral.dynamics.com/?page=5604) | **Afskrivningsprofil**, **Anlægsnr.**, **Bogføringsdato for anlæg**, **Anlægsbogføringstype**, **Beløb** og **Anlægsbogføringstype** |

### <a name="example-fixed-assets-current-value"></a>Eksempel: anlægsaktiver med nutidsværdi

Følg disse trin for at spore værdien af et eller flere anlægsaktiver:

1. Åbn [Anlægsposter for varer](https://businesscentral.dynamics.com/?page=5604)-listen, og vælg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivér analysetilstand."::: tænd for analysetilstand.
1. Gå til menuen **Kolonner**, og fjern alle kolonner (markér feltet ud for feltet **Søg** i højre side).
1. Træk **afskrivningsprofilen** og **anlægsnummeret** til området **Rækkegrupper**.
1. Vælg felterne **Anlægsdato** og **Anlægsbogføringstype**.
1. Træk feltet **Beløb** til området **Værdier**.
1. Omdøb din analysefane til **Oversigt over aktiv - værdi** eller noget, der beskriver denne analyse.

Følgende billede viser resultatet af disse trin.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png" alt-text="Eksempel på, hvordan du kan udføre dataanalyse på siden Anlægsposter for at se værdien af et aktiv." lightbox="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png":::

### <a name="example-asset-value-changes-over-time"></a>Eksempel: aktivværdien ændres over tid

Følg disse trin for at spore ændringer i aktivværdien over tid:

1. Åbn [Anlægsposter for varer](https://businesscentral.dynamics.com/?page=5604)-listen, og vælg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivér analysetilstand."::: tænd for analysetilstand.
1. Gå til menuen **Kolonner**, og fjern alle kolonner (markér feltet ud for feltet **Søg** i højre side).
1. Aktiver **Pivot-tilstand** (placeret direkte over **Søg** feltet i højre side).
1. Træk feltet **Anlægsbogføringstype** til området **Rækkegruppe**.
1. Træk felterne **Bogføringsår for anlæg** og **Bogføringsmåned for anlæg** til området **Kolonnenavne**.
1. Træk feltet **Beløb** til området **Værdier**.
1. Omdøb din analysefane til **Aktivværdien ændres over tid** eller noget, der beskriver denne analyse.

Følgende billede viser resultatet af disse trin.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-changes-over-time.png" alt-text="Eksempel på, hvordan du kan udføre dataanalyse på siden Anlægsposte over tid." lightbox="media/data-analysis-fa-ledger-entries-asset-changes-over-time.png":::

### <a name="example-fixed-asset-depreciations-over-time"></a>Eksempel: afskrivning af anlægsaktiver over tid

Følg disse trin for at spore afskrivningen af et eller flere anlægsaktiver:

1. Åbn [Anlægsposter for varer](https://businesscentral.dynamics.com/?page=5604)-listen, og vælg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivér analysetilstand."::: tænd for analysetilstand.
1. Gå til menuen **Kolonner**, og fjern alle kolonner (markér feltet ud for feltet **Søg** i højre side).
1. Aktiver **Pivot-tilstand** (placeret direkte over **Søg** feltet i højre side).
1. Træk **afskrivningsprofilen** og **anlægsnummeret** til området **Rækkegrupper**.
1. Træk felterne **Bogføringsår for anlæg** og **Bogføringsmåned for anlæg** til området **Kolonnenavne**.
1. Træk feltet **Beløb** til området **Værdier**.
1. I filteret **Anlægsbogføringstype** skal du vælge **Afskrivning**.
1. Omdøb din analysefane til **Afskrivninger over tid** eller noget, der beskriver denne analyse for dig.

Følgende billede viser resultatet af disse trin.

:::image type="content" source="media/data-analysis-fa-ledger-entries-depreciation-by-asset.png" alt-text="Eksempel på, hvordan du kan udføre dataanalyse på siden Anlægsposter for at se afskrivning over tid." lightbox="media/data-analysis-fa-ledger-entries-depreciation-by-asset.png":::

## <a name="data-foundation-for-ad-hoc-analysis-on-fixed-assets"></a>Datagrundlag for ad-hoc analyse af anlægsaktiver

Når du bogfører anlægskladder [!INCLUDE [prod_short](includes/prod_short.md)], oprettes der poster i tabellen **Anlægspost**. Derfor udføres ad hoc-analyser af anlægsaktiver typisk på siden [Anlægsposter](https://businesscentral.dynamics.com/?page=5604).

## <a name="contributors"></a>Bidragydere

*Microsoft vedligeholder denne artikel. Dele af eksemplerne blev oprindeligt skrevet af følgende bidragyder.*

* [Aldona Stec](https://www.linkedin.com/in/aldona-stec-25283bb1) | [!INCLUDE[prod_short](includes/prod_short.md)] Konsulent

## <a name="see-also"></a>Se også

[Analysere liste- og forespørgselsdata med analysetilstand](analysis-mode.md)  
[Oversigt over analyse af anlægsaktiver](fa-analytics-overview.md)  
[Analyse, Business Intelligence og rapporteringsoversigt](reports-bi-reporting.md)  
[Oversigt over anlægsaktiver](fa-manage.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
