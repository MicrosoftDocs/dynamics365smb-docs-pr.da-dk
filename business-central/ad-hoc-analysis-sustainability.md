---
title: Ad hoc-analyse af bæredygtighedsdata
description: 'Få mere at vide om, hvordan du kan bruge dataanalysetilstand til at analyse bæredygtighedsdata.'
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI, sustainability, ESG'
ms.search.form: '6220,'
ms.date: 06/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Ad hoc-analyse af bæredygtighedsdata

I artikel beskriver, hvordan du bruger funktionen **Dataanalyse** til at analysere bæredygtighedsdata direkte fra listesider og forespørgsler. Du behøver ikke at køre en rapport eller skifte til et andet program, f.eks. Excel. Funktionen indeholder en interaktiv og alsidig måde at beregne, opsummere og gennemgå data på. I stedet for at køre rapporter med indstillinger og filtre kan du tilføje flere faner, der repræsenterer forskellige opgaver eller visninger på dataene. Nogle eksempler er "Emissionsoversigt" eller "Emission efter omfang" eller enhver anden visning, du kan forestille dig. Du kan få mere at vide om, hvordan du bruger funktionen **Dataanalyse** ved at gå til [Analysér liste og forespørge på data med analysetilstand](analysis-mode.md).

Brug følgende listesider til ad hoc-analyse af bæredygtighedsdata:

- [Finansposter for bæredygtighed](https://businesscentral.dynamics.com/?page=6220)

## Ad hoc-analysescenarier for bæredygtighed

Brug funktionen **Dataanalyse** til hurtig faktatjek og ad hoc-analyse:

- Hvis du ikke vil køre en rapport.
- Hvis der ikke er en rapport om dine specifikke behov.
- Hvis du hurtigt vil gentage for at få et godt overblik over en del af din virksomhed.

Følgende afsnit indeholder eksempler på bæredygtighedsscenarier i [!INCLUDE [prod_short](includes/prod_short.md)].

| Område | Til... | Åbn denne side i analysetilstand | Brug af disse felter |
| ---- | ----- | ------------------------------- |------------------- |
| [Emissionsoversigt (summen efter kategori)](#example-emission-overview-sum-by-category) | Analysér dine emissioner efter kategori. | [Finansposter for bæredygtighed](https://businesscentral.dynamics.com/?page=6220) | **Kontokategori**, **Kontonavn**, **Emission NH4**. **Emission CO2** og **Emission N2O**.|
| [Gennemsnitlige emissioner pr. kategori](#example-average-emissions-by-category) | Analysér dine gennemsnitlige emissioner efter kategori. | [Finansposter for bæredygtighed](https://businesscentral.dynamics.com/?page=6220) | **Kontokategori**, **Kontonavn**, **Emission NH4**. **Emission CO2** og **Emission N2O**.|
| [Emissioner efter omfang](#example-emissions-by-scope) | Analysér dine emissioner efter omfang. | [Finansposter for bæredygtighed](https://businesscentral.dynamics.com/?page=6220) | **Emissionsomfang**, **Kontokategori**, **Emission NH4**, **Emission CO2** og **Emission N2O**.|

## Eksempel: Emissionsoversigt (sum efter kategori)

Følg disse trin for at analysere dine emissioner efter kategori:

1. Åbn siden [Finansposter for bæredygtighed](https://businesscentral.dynamics.com/?page=6220), og slå analysetilstand til.
1. Gå til menuen **Kolonner**, og fjern alle kolonner (markér feltet ud for feltet **Søg**).
1. Slå **Pivot** tilstand (placeret direkte over **Søg** feltet).
1. Træk felterne **Kontokategori** og **Kontonummer** til området **Rækkegrupper**. Træk felterne i den pågældende rækkefølge.
1. Træk felterne **Emission NH4**, **Emission CO2** og **Emission N2O** til området **Værdier**.
1. Omdøb din analysefane til **Emissionsoversigt (sum)** eller noget, der beskriver denne analyse for dig.

Følgende billede viser resultatet af disse trin.

:::image type="content" source="media/data-analysis-sustainability-entries.png" alt-text="Eksempel 1 på, hvordan du udfører dataanalyse på siden Finansposter for bæredygtighed." lightbox="media/data-analysis-sustainability-entries.png":::

## Eksempel: Gennemsnitlige emissioner pr. kategori

Følg disse trin for at analysere dine gennemsnitlige emissioner efter kategori:

1. Åbn siden [Finansposter for bæredygtighed](https://businesscentral.dynamics.com/?page=6220), og slå analysetilstand til.
1. Gå til menuen **Kolonner**, og fjern alle kolonner (markér feltet ud for feltet **Søg**).
1. Slå **Pivot** tilstand (placeret direkte over **Søg** feltet).
1. Træk felterne **Kontokategori** og **Kontonummer** til området **Rækkegrupper**. Træk felterne i den pågældende rækkefølge.
1. Træk felterne **Emission NH4**, **Emission CO2** og **Emission N2O** til området **Værdier**.
1. For hvert felt i området **Værdier** skal du markere dem og ændre sammenlægningsfunktionen til `Average`.
1. Omdøb din analysefane til **Emissionsoversigt (gns)** eller noget, der beskriver denne analyse for dig.

Følgende billede viser resultatet af disse trin.

:::image type="content" source="media/data-analysis-sustainability-entries-avg.png" alt-text="Eksempel 2 på, hvordan du udfører dataanalyse på siden Finansposter for bæredygtighed." lightbox="media/data-analysis-sustainability-entries-avg.png":::

## Eksempel: Emissioner efter omfang

Følg disse trin for at analysere dine emissioner efter omfang:

1. Åbn siden [Finansposter for bæredygtighed](https://businesscentral.dynamics.com/?page=6220), og slå analysetilstand til.
1. Gå til menuen **Kolonner**, og fjern alle kolonner (markér feltet ud for feltet **Søg**).
1. Slå **Pivot** tilstand (placeret direkte over **Søg** feltet).
1. Træk felterne **Emissionsomfang** og **Kontokategori** til området **Rækkegrupper**. Træk felterne i den pågældende rækkefølge.
1. Træk felterne **Emission NH4**, **Emission CO2** og **Emission N2O** til området **Værdier**.
1. Omdøb din analysefane til **Emissionsoversigt efter omfang** eller noget, der beskriver denne analyse for dig.

Følgende billede viser resultatet af disse trin.

:::image type="content" source="media/data-analysis-sustainability-entries-scope.png" alt-text="Eksempel 3 på, hvordan du udfører dataanalyse på siden Finansposter for bæredygtighed." lightbox="media/data-analysis-sustainability-entries-scope.png":::

## Datagrundlag for ad-hoc analyse af bæredygtighed

De oplysninger, du angiver i en bæredygtighedskladde, er midlertidige, og du kan ændre dem, mens de er i kladden. Når du bogfører en bæredygtighedskladde, overføres oplysningerne til finansposter for bæredygtighed på individuelle bæredygtighedskonti, hvor du ikke kan ændre dem. Du kan dog bogføre tilbageførsels- eller rettelsesposter.  [Listesiden Bæredygtighedsposter](https://businesscentral.dynamics.com/?page=6220) er den vigtigste datakilde til ad hoc-analyse af bæredygtighedsdata.

Du kan få mere at vide om offentliggørelse af bæredygtighedsposter ved at gå til [Registrere bæredygtighedsposter](finance-sustainability-journal.md).

## Se også

[Registrer bæredygtighedsposter](finance-sustainability-journal.md)  
[Indbyggede rapporter om bæredygtighed](sustainability-reports.md)   
[Analyse, Business Intelligence og rapporteringsoversigt](reports-bi-reporting.md)  
[Oversigt over styring af bæredygtighed](finance-manage-sustainability.md)   
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
