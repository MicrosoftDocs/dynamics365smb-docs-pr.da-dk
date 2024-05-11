---
title: Ad-hoc analyser i indkøb
description: 'Få mere at vide om, hvordan du kan bruge dataanalysetilstand i indkøb.'
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '9306, 9307, 518, 29'
ms.date: 04/29/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Ad-hoc analyser i indkøb

I artikel beskriver, hvordan du analyserer køb af data fra listesider og forespørgsler ved hjælp af tilstanden **Dataanalyse**. Med funktionen kan du analysere data direkte fra siden uden at skulle køre en rapport eller åbne et andet program, f.eks. Excel. Dataanalyser leverer en interaktiv og alsidig måde at beregne, opsummere og gennemgå data på. I stedet for at køre rapporter med indstillinger og filtre kan du tilføje flere faner, der repræsenterer forskellige opgaver eller visninger på dataene. Nogle eksempler er "Mine leverandører" eller "Indkøbsstatistik" eller enhver anden visning, du kan forestille dig. Du kan få mere at vide om, hvordan du bruger funktionen **Dataanalyse** ved at gå til [Analysér liste og forespørge på data med analysetilstand](analysis-mode.md).

Brug følgende listesider til ad hoc-analyse af købsprocesser:

- [Købsordrer](https://businesscentral.dynamics.com/?page=9307)
- [Købslinjer](https://businesscentral.dynamics.com/?page=518)
- [Bogførte købsfakturaer](https://businesscentral.dynamics.com/?page=146)
- [Kreditorposter](https://businesscentral.dynamics.com/?page=29)
- [Finansposter](https://businesscentral.dynamics.com/?page=20)

## Ad hoc-analysescenarier for indkøb

Brug funktionen **Dataanalyse** til hurtig faktatjek og ad hoc-analyse:

- Hvis du ikke vil køre en rapport
- Hvis der ikke er en rapport om dine specifikke behov
- Hvis du hurtigt vil gentage for at få et godt overblik over en del af din virksomhed.

Følgende afsnit indeholder eksempler på købsscenarier i [!INCLUDE [prod_short](includes/prod_short.md)].

| Område | Til... | Åbn denne side i analysetilstand | Brug af disse felter |
| ---- | ----- | ------------------------------- |------------------- |
| [GRNI-oversigt](#example-goods-received-not-invoiced-grni-overview) | Få en GRNI-oversigt (Goods Received, Not Invoiced) på tværs af leverandører. | **Type**, **Amt. Rec. Ikke faktureret (LV)** (filtrer i disse felter), **Kreditornr.**, **Bilagsnr.**, **Nr.** og **Modt. Ikke faktureret (LV)** <br> **Bemærk:** Du kan tilpasse siden for at tilføje disse felter. Flere oplysninger i [Tilpasse dit arbejdsområde](ui-personalization-user.md). | 
| [Finance (Kreditorer)](#example-finance-accounts-payable) | Se, hvad du skylder dine kreditorer, eventuelt opdelt i tidsintervaller for, hvornår beløb er forfaldne. | [Kreditorposter](https://businesscentral.dynamics.com/?page=29) | **Kreditornavn**, **Bilagstype**, **,Bilagsnr.**, **Forfaldsdatoår**, **,Forfaldsdatomåned** og **Restbeløb**. |

## Eksempel: Oversigt over varer modtaget, ikke faktureret (GRNI)

Hvis du vil oprette en GRNI-oversigt (Goods Received, Not Invoiced) på tværs af kreditorer, skal du følge disse trin:
 
1. Åbn [Købslinjer](https://businesscentral.dynamics.com/?page=518)-siden.
1. Tilpas siden for at tilføje feltet **Modtaget beløb, der ikke er faktureret**. Hvis du vil tilpasse siden, skal du vælge **Indstillinger** og derefter **Tilpas**.
1. Tænd for analysetilstand.
1. Gå til menuen **Kolonner**, og fjern alle kolonner (markér feltet ud for feltet **Søg**).
1. Angiv følgende filtre i menuen **Yderligere filtre** (til højre på siden lige under menuen **Kolonner**):
    - **Type = Vare**
    - **Amt. Rec. Ikke faktureret (LV) > 0**. 
1. Træk **Kreditornr.**, **Bilagsnr.** og **Nummer.** felterne til området **Rækkegrupper**. Træk felterne i den pågældende rækkefølge.
1. Tilføj **Amt. Rec. Ikke faktureret (LV)** for at medtage det i oversigten.
1. Hvis du vil udføre analysen for et givet år eller kvartal, skal du anvende et filter i menuen **Yderligere filtre**. Menuen er til højre på siden, lige under menuen **Kolonner**.
1. Omdøb din analysefane til **Varer modtaget, Ikke faktureret (GRNI)** eller noget, der beskriver denne analyse for dig.

## Eksempel: Finance (Kreditorer)

Se, hvad du skylder dine kreditorer, eventuelt opdelt i tidsintervaller for, hvornår beløb er forfaldne ved at følge disse trin:

1. Åbn listesiden [Kreditorposter](https://businesscentral.dynamics.com/?page=29), og slå analysetilstand til.
1. Gå til menuen **Kolonner**, og fjern alle kolonner (markér feltet ud for feltet **Søg**).
1. Slå **Pivot** tilstand (placeret direkte over **Søg** feltet).
1. Træk **Leverandørnavn**, **Dokumenttype** og felterne **Dokumentnr.** til området **Rækkegrupper** , og træk derefter feltet **Restbeløb** til området **Værdier**.
1. Træk felterne **Forfaldsdato** og **Forfaldsdatomåned** til området **Kolonnenavne**. Træk felterne i den pågældende rækkefølge.
1. Hvis du vil udføre analysen for et givet år eller kvartal, skal du anvende et filter i menuen **Yderligere filtre** (til højre på siden lige under menuen **Kolonner**.)
1. Omdøb din analysefane til **Aldersfordel gæld efter måned** eller noget, der beskriver denne analyse for dig.

Følgende billede viser resultatet af disse trin.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Eksempel på, hvordan du udfører dataanalyse på siden Finansposter." lightbox="media/data-analysis-vendor-ledger-entries.png":::

## Datagrundlag for ad-hoc analyse af indkøb

Når et købsdokument bogføres, opdaterer [!INCLUDE [prod_short](includes/prod_short.md)] kreditorens konto, regnskabet og vareposterne, og ressourceposterne:

- For hvert købsdokument oprettes der en købspost i tabellen **Finanspost**. Der oprettes også en post i kreditorkontoen i tabellen **Leverandørfinanspost**, og der oprettes en finanspost i den relevante samlekonto. Desuden kan bogføring af købet medføre oprettelse af en moms- og en finanspost med rabat.
- For hver købslinje oprettes følgende poster i:
  - Tabellen **Varepost**, hvis købslinjen er af typen Vare.
  - **Finanspost**-tabel, hvis købslinjerne er af typen Finanskonto.
  - **Ressourcepost**-tabellen, hvis købslinjen er af typen Ressource.
- Købsdokumenter registreres desuden altid i tabellerne **Købsleverancehoved** og **Købsfakturahoved**.

Flere oplysninger i [Bogføring af køb](purchasing-how-record-purchases.md#posting-purchases).

## Se også

[Bogføring af køb](purchasing-how-record-purchases.md#posting-purchases)  
[Analysere liste- og forespørgselsdata med analysetilstand](analysis-mode.md)  
[Købsoversigt](purchasing-manage-purchasing.md)  
[Analyse, Business Intelligence og rapporteringsoversigt](reports-bi-reporting.md)  
[Købsoversigt](purchasing-manage-purchasing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]