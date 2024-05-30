---
title: Ad hoc-analyse af salgsdata
description: 'Få mere at vide om, hvordan du kan bruge dataanalysetilstand til at analysere salgsdata.'
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 04/28/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Ad hoc-analyse af salgsdata

I artikel beskriver, hvordan du bruger funktionen **Dataanalyse** til at analysere salgsdata direkte fra listesider og forespørgsler. Du behøver ikke at køre en rapport eller skifte til et andet program, f.eks. Excel. Funktionen indeholder en interaktiv og alsidig måde at beregne, opsummere og gennemgå data på. I stedet for at køre rapporter med indstillinger og filtre kan du tilføje flere faner, der repræsenterer forskellige opgaver eller visninger på dataene. Nogle eksempler er "Mine debitorer" eller "Salgsstatistik" eller enhver anden visning, du kan forestille dig. Du kan få mere at vide om, hvordan du bruger funktionen **Dataanalyse** ved at gå til [Analysér liste og forespørge på data med analysetilstand](analysis-mode.md).

Brug følgende listesider til ad hoc-analyse af salgsprocesser:

- [Salgsordrer](https://businesscentral.dynamics.com/?page=9305)
- Finansposter
- [Debitorposter](https://businesscentral.dynamics.com/?page=25)
- Finansposter for vare
- Bogførte salgsfakturaer
- Salgsreturordrer

## Salgs ad hoc-analysescenarier

Brug funktionen **Dataanalyse** til hurtig faktatjek og ad hoc-analyse:

- Hvis du ikke vil køre en rapport.
- Hvis der ikke er en rapport om dine specifikke behov.
- Hvis du hurtigt vil gentage for at få et godt overblik over en del af din virksomhed.

Følgende afsnit indeholder eksempler på salgsscenarier i [!INCLUDE [prod_short](includes/prod_short.md)].

| Område | Til... | Åbn denne side i analysetilstand | Brug af disse felter |
| ---- | ----- | ------------------------------- |------------------- |
| [Salg (forventet salgsmængde)](#example-sales-expected-sales-volume) | Analysér det forventede salgsantal. | [Salgsordrer](https://businesscentral.dynamics.com/?page=9305) | **Sælg til-debitornavn**, **Sælg til-debitornr.**, **Nr.** , **Beløb**, **Bilagsdatoår** og **Bilagsdatomåned**. |
| [Salg (Debitorsalg efter mængde)](#example-sales-customer-sales-by-volume) | Få et overblik over, hvilke debitorer der køber mest eller skylder mest. | [Debitorposter](https://businesscentral.dynamics.com/?page=25) | **Debitornavn**, **Bilagsnr.**, **Beløb** og **Restbeløb**. |
| [Finance (Tilgodehavender)](#example-finance-accounts-receivables) | Se, hvad dine kunder skylder dig, f.eks. opdelt i tidsintervaller for, hvornår beløb er forfaldne. | [Debitorposter](https://businesscentral.dynamics.com/?page=25) | **Debitornavn**, **Forfaldsdato** og **Restbeløb**. |

## Eksempel: Salg (forventet salgsmængde)

Hvis du vil analysere den forventede salgsmængde og salgsbeløbene for ikke-leverede ordrer for hver debitor efter år eller måned, skal du følge disse trin:

1. Åbn listen [Salgsordrer](https://businesscentral.dynamics.com/?page=9305), og slå analysetilstand til.
1. Gå til menuen **Kolonner**, og fjern alle kolonner (markér feltet ud for feltet **Søg**).
1. Slå **Pivot** tilstand (placeret direkte over **Søg** feltet).
1. Træk **Sælg til-debitornavn**, **Sælg til-debitornr.** og **Nr.** felterne til området **Rækkegrupper**. Træk felterne i den pågældende rækkefølge.
1. Træk feltet **Beløb** til området **Værdier**.
1. Træk felterne **Dokumentdato år** og **Dokumentdato måned** til området **Kolonnenavne**. Træk felterne i den pågældende rækkefølge.
1. Hvis du vil udføre analysen for et givet år eller kvartal, skal du anvende et filter i menuen **Yderligere filtre**. Menuen er til højre på siden, lige under menuen **Kolonner**.
1. Omdøb din analysefane til **Forventet salgsmængde** eller noget, der beskriver denne analyse for dig.

## Eksempel: Salg (Debitorsalg efter mængde)

Følg disse trin, hvis du skal bruge et overblik over, hvilke kunder der køber mest eller skylder mest.

1. Åbn listesiden [Debitorposter](https://businesscentral.dynamics.com/?page=25), og slå analysetilstand til.
1. Gå til menuen **Kolonner**, og fjern alle kolonner (markér feltet ud for feltet **Søg**).
1. Træk feltet **Debitornavn** til området **Rækkegrupper** og til **Dokumentnr.** derunder.
1. Vælg felterne **Beløb** og **Restbeløb**.
1. Hvis du vil udføre analysen for et givet år eller kvartal, skal du anvende et filter i menuen **Yderligere filtre**. Menuen er til højre på siden, lige under menuen **Kolonner**.
1. Omdøb din analysefane til **Debitor efter salgsmængde** eller noget, der beskriver denne analyse for dig.

Følgende billede viser resultatet af disse trin.

:::image type="content" source="media/data-analysis-customer-ledger-entries.png" alt-text="Eksempel på, hvordan du udfører dataanalyse på siden Finansposter." lightbox="media/data-analysis-customer-ledger-entries.png":::

## Eksempel: Finance (Tilgodehavender)

Se, hvad du dine debitorer skylder dig, eventuelt opdelt i tidsintervaller for, hvornår beløb er forfaldne ved at følge disse trin:

1. Åbn listesiden [Debitorposter](https://businesscentral.dynamics.com/?page=25), og slå analysetilstand til.
1. Fjern alle kolonner i menuen **Kolonner** (markér feltet ud for feltet **Søg**).
1. Slå **Pivot** tilstand (placeret direkte over **Søg** feltet).
1. Træk feltet **Debitornavn** til området **Rækkegrupper**, og træk feltet **Restbeløb** til området **Værdier**.
1. Træk felterne **Forfaldsdato måned** til området **Kolonnenavne**.
1. Hvis du vil udføre analysen for et givet år eller kvartal, skal du anvende et filter i menuen **Yderligere filtre**. Menuen er til højre på siden, lige under menuen **Kolonner**.
1. Omdøb din analysefane til **Aldersfordel gæld efter måned** eller noget, der beskriver denne analyse for dig.

## Datagrundlag for ad-hoc analyse af salg

Når du har udfyldt med oplysninger i en salgsordre og tilføjet alle salgsordrelinjer, kan du bogføre ordren. Bogføring opretter en leverance og en faktura. [!INCLUDE [prod_short](includes/prod_short.md)] opdaterer kundens konto, finanskonto og vareposter:

- For hver salgsordre oprettes der en salgspost i tabellen **Finanspost**. Der oprettes også en post i debitorkontoen i tabellen **Debitorpost**, og der oprettes en finanspost i den relevante samlekonto. Desuden kan der eventuelt blive dannet en momspost og en finanspost for rabatbeløbet.
- For hver salgsordrelinje oprettes der en varepost i tabellen **Varepost** (hvis salgslinjerne indeholder varenumre) eller en finanspost i tabellen **Finanspost** (hvis der er indsat en finanskonto på salgslinjerne). Salgsordrer bliver desuden altid registreret i tabellerne **Salgsleverancehoved** og **Salgsfakturahoved**.

Hvis du vil vide mere om bogføring af salg, skal du [Bogføre salg](ui-post-sales.md).

## Se også

[Bogføre salg](ui-post-sales.md)  
[Analysere liste- og forespørgselsdata med analysetilstand](analysis-mode.md)  
[Oversigt over salgsanalyse](sales-analytics-overview.md)  
[Analyse, Business Intelligence og rapporteringsoversigt](reports-bi-reporting.md)  
[Salgsoversigt](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]