---
title: Ad hoc-analyse af finansdata
description: 'Få mere at vide om, hvordan du kan bruge dataanalysetilstand til at analysere finansdata.'
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 05/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="ad-hoc-analysis-of-finance-data"></a>Ad hoc-analyse af finansdata

I artikel beskriver, hvordan du bruger funktionen **Dataanalyse** til at analysere finansdata direkte fra listesider og forespørgsler. Du behøver ikke at køre en rapport eller skifte til et andet program, f.eks. Excel. Funktionen indeholder en interaktiv og alsidig måde at beregne, opsummere og gennemgå data på. I stedet for at køre rapporter med indstillinger og filtre kan du tilføje flere faner, der repræsenterer forskellige opgaver eller visninger på dataene. Nogle eksempler er "Aktiver i alt", "Afskrivninger over tid", "Tilgodehavender" eller enhver anden visning, du kan forestille dig. Du kan få mere at vide om, hvordan du bruger funktionen **Dataanalyse** ved at gå til [Analysér liste og forespørge på data med analysetilstand](analysis-mode.md).

Brug følgende listesider for at starte en ad hoc-analyse af finansprocesser:

- [Finansposter](https://businesscentral.dynamics.com/?page=20)
- [Debitorposter](https://businesscentral.dynamics.com/?page=25)
- [Kreditorposter](https://businesscentral.dynamics.com/?page=29)

## <a name="ad-hoc-analysis-scenarios-in-finance"></a>Ad-hoc analyse scenarier i finansiering

Brug funktionen **Dataanalyse** til hurtig faktatjek og ad hoc-analyse:

- Hvis du ikke vil køre en rapport.
- Hvis der ikke er en rapport om dine specifikke behov.
- Hvis du hurtigt vil gentage for at få et godt overblik over en del af din virksomhed.

Følgende afsnit indeholder eksempler på finansscenarier i [!INCLUDE [prod_short](includes/prod_short.md)].

| Område | Til... | Åbn denne side i analysetilstand | Brug af disse felter |
| ---- | ----- | ------------------------------- |------------------- |
|[Eksempel: Finans (tilgodehavender)](#example-finance-accounts-receivable) | Se, hvad dine kunder skylder dig, f.eks. opdelt i tidsintervaller for, hvornår beløb er forfaldne. | [Debitorposter](https://businesscentral.dynamics.com/?page=25) | **Debitornavn**, **Forfaldsdato** og **Restbeløb** |
| [Finance (Kreditorer)](#example-finance-accounts-payable) | Se, hvad du skylder dine kreditorer, eventuelt opdelt i tidsintervaller for, hvornår beløb er forfaldne. | [Kreditorposter](https://businesscentral.dynamics.com/?page=29) | **Kreditornavn**, **Bilagstype**, **,Bilagsnr.**, **Forfaldsdato-år**, **,Forfaldsdato-måned** og **Restbeløb**. |
| [Finans (salgsfakturaer efter finanskonto)](#example-finance-sales-invoices-by-gl-account) | Se, hvordan salgsfakturaer fordeler sig over finanskonti fra kontoplanen, f.eks. opdelt i tidsintervaller for, hvornår beløb blev bogført. | [Finansposter](https://businesscentral.dynamics.com/?page=20) | **Finanskontonavn,Kildespor,Finanskontonavn,Finanskontonr** **·** **·** **.**, **Debetbeløb,Kreditbeløb,Bogføringsdatoår,Bogføringsdatokvartal** **·** **·** **og** **Bogføringsdatomåned** |
| [Finance (Resultatopgørelse)](#example-finance-income-statement) | Se din indkomst over resultatkontiene fra kontoplaner, f.eks. opdelt i tidsintervaller for, hvornår beløb blev bogført. | [Finansposter](https://businesscentral.dynamics.com/?page=20) | **Finanskontonr.**, **Bogføringsdato** og **Beløb**. |
| [Finance (samlede aktiver)](#example-finance-total-assets) | Se dine aktiver over anlægskonti fra kontoplanen, f.eks. opdelt i tidsintervaller for, hvornår beløb blev bogført. | [Finansposter](https://businesscentral.dynamics.com/?page=20) | **Finanskontonr.**, **Bogføringsdato** og **Beløb**. |

### <a name="example-finance-accounts-receivable"></a>Eksempel: Finans (tilgodehavender)

Se, hvad du dine debitorer skylder dig, eventuelt opdelt i tidsintervaller for, hvornår beløb er forfaldne ved at følge disse trin:

1. Åbn [Debitorposter](https://businesscentral.dynamics.com/?page=25)-listen, og vælg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivér analysetilstand."::: tænd for analysetilstand.
1. Gå til menuen **Kolonner**, og fjern alle kolonner (markér feltet ud for feltet *Søg* i højre side).
1. Aktiver **Pivot* tilstand** (placeret direkte over **Søg** feltet i højre side).
1. Træk feltet **Debitornavn** til området **Rækkegrupper**, og træk feltet **Restbeløb** til området **Værdier**.
1. Træk felterne **Forfaldsdato måned** til området **Kolonnenavne**.
1. Hvis du vil udføre analysen for et givet år eller kvartal, skal du anvende et filter i menuen **Analysefiltre** (placeret under menuen **Kolonner** i højre side).
1. Omdøb din analysefane til **Aldersfordel gæld efter måned** eller noget, der beskriver denne analyse.

### <a name="example-finance-accounts-payable"></a>Eksempel: Finance (Kreditorer)

Se, hvad du skylder dine kreditorer, eventuelt opdelt i tidsintervaller for, hvornår beløb er forfaldne ved at følge disse trin:

1. Åbn listesiden [Kreditorposter](https://businesscentral.dynamics.com/?page=29), og vælg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Slå analysetilstand til."::: tænd for analysetilstand.
1. Gå til menuen **Kolonner**, og fjern alle kolonner (markér feltet ud for feltet **Søg**).
1. Aktiver **Pivot-tilstand** (placeret direkte over **Søg** feltet i højre side).
1. Træk **Leverandørnavn**, **Dokumenttype** og felterne **Dokumentnr.** til området **Rækkegrupper** , og træk derefter feltet **Restbeløb** til området **Værdier**.
1. Træk felterne **Forfaldsdato** og **Forfaldsdatomåned** til området **Kolonnenavne**. Træk felterne i den pågældende rækkefølge.
1. Hvis du vil udføre analysen for et givet år eller kvartal, skal du anvende et filter i menuen **Analysefiltre** (placeret under menuen **Kolonner** i højre side).
1. Omdøb din analysefane til **Aldersfordelt gæld efter måned** eller noget, der beskriver denne analyse.

Følgende billede viser resultatet af disse trin.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Eksempel på, hvordan du udfører dataanalyse på siden Finansposter." lightbox="media/data-analysis-vendor-ledger-entries.png":::

### <a name="example-finance-sales-invoices-by-gl-account"></a>Eksempel: Finans (salgsfakturaer efter finanskonto)

Hvis du vil se, hvordan salgsfakturaerne fordeler sig over finanskonti fra kontoplanen, f.eks. opdelt i tidsintervaller for, hvornår beløb blev bogført, skal du benytte følgende fremgangsmåde:

1. Åbn siden [Finansposter](https://businesscentral.dynamics.com/?page=20) .
1. Tilføj felterne **Finanskontonavn** og **Kildespor** ved at tilpasse siden. I menuen **Indstillinger** skal du vælge **Tilpas**.
1. Afslut tilpasningstilstand.
1. Vælg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Skift til analysetilstand."::: tænd for analysetilstand.
1.  **I menuen Analysefiltre** skal du angive et filter på **feltet Kildespor** til **SALG.** Hvis du har tilpasninger, der tilføjer andre værdier, kan du også tilføje dem.
1. Fjern alle kolonner i menuen **Kolonner** (markér feltet ud for feltet **Søg**).
1. Aktiver **Pivot-tilstand** (placeret direkte over **Søg** feltet i højre side).
1. Træk navnet **på** finanskontoen og **feltet Finanskontonr.**  **til området Rækkegrupper** .
1. Træk felterne **Debetbeløb** og **Kreditbeløb** til **området Værdier** .
1. Træk felterne Bogføringsdato **År**, **Bogføringsdato, Kvartal** og **Bogføringsdatomåned** til **området Kolonnenavne** .
1. Omdøb din analysefane til **Fakturaopdeling efter konto** eller noget, der beskriver denne analyse.

Følgende billede viser resultatet af disse trin.

:::image type="content" source="media/data-analysis-gl-entries-invoices.png" alt-text="Eksempel på, hvordan du kan udføre dataanalyse på siden Finansposter (for at forstå salgsbogføringer)." lightbox="media/data-analysis-gl-entries-invoices.png":::

### <a name="example-finance-income-statement"></a>Eksempel: Finance (Resultatopgørelse)

Se din indkomst over resultatkontiene fra kontoplanen, opdelt i tidsintervaller for, hvornår beløb blev bogført, ved at følge disse trin:

1. Åbn [Finansposter](https://businesscentral.dynamics.com/?page=20)-listen, og vælg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivér analysetilstand."::: tænd for analysetilstand.
1. Gå til menuen **Kolonner**, og fjern alle kolonner (markér feltet ud for feltet **Søg** i højre side).
1. Aktiver **Pivot-tilstand** (placeret direkte over **Søg** feltet i højre side).
1. Træk feltet **Finanskontonummer** til området **Rækkegrupper**, og træk feltet **Beløb** til området **Værdier**.
1. Træk felterne **Bogføringsdato-måned** til området **Kolonnenavne**.
1. I resultatopgørelsen skal du filtrere de konti, du bruger. I [!INCLUDE [prod_short](includes/prod_short.md)] -demodataene starter disse konti med "4", men din kontoplan kan være anderledes. Angiv et filter på passende konti i menuen **Analysefiltre** (til højre lige under menuen **Kolonner**.)

   > [!TIP]
   > Hvis du vil se de konti, der bruges i din opsætning, skala du køre rapporten [Saldo pr. periode](https://businesscentral.dynamics.com/?report=38).

1. Omdøb din analysefane til **Indtægt efter måned** eller noget, der beskriver denne analyse.

### <a name="example-finance-total-assets"></a>Eksempel: Finance (samlede aktiver)

Se dine aktiver over anlægskonti fra kontoplanen, opdelt i tidsintervaller for, hvornår beløb blev bogført, ved at gøre følgende.

1. Åbn [Finansposter](https://businesscentral.dynamics.com/?page=20)-listen, og vælg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivér analysetilstand."::: tænd for analysetilstand.
1. Gå til menuen **Kolonner**, og fjern alle kolonner (markér feltet ud for feltet **Søg** i højre side).
1. Aktiver **Pivot-tilstand** (placeret direkte over **Søg** feltet i højre side).
1. Træk feltet **Finanskontonummer** til området **Rækkegrupper**, og træk feltet **Beløb** til området **Værdier**.
1. Træk felterne **Bogføringsdato-måned** til området **Kolonnenavne**.
1. I opgørelsen af samlede aktiver skal du filtrere de konti, du bruger. I [!INCLUDE [prod_short](includes/prod_short.md)] -demodataene starter disse konti med "10", men din kontoplan kan være anderledes. Angiv et filter på passende konti i menuen **Yderligere filtre** (til højre lige under menuen **Kolonner**.)

   > [!TIP]
   > Hvis du vil se de konti, der bruges i din opsætning, skala du køre rapporten [Saldo pr. periode](https://businesscentral.dynamics.com/?report=38).

1. Omdøb din analysefane til **Indtægt efter måned** eller noget, der beskriver denne analyse.

## <a name="data-foundation-for-ad-hoc-analysis-on-finance"></a>Datagrundlag for ad-hoc analyse af finans

Når du bogfører anlægskladder [!INCLUDE [prod_short](includes/prod_short.md)], oprettes der poster i tabellen **Finanspost**. Derfor udføres ad hoc-analyser af finanser typisk på siden [Finansposter](https://businesscentral.dynamics.com/?page=20). I forbindelse med tilgodehavender og gæld kan du analysere [henholdsvis debitorposter](https://businesscentral.dynamics.com/?page=25) og [kreditorposter](https://businesscentral.dynamics.com/?page=29).

+Hvis du vil vide mere, skal du gå til følgende artikler:

- [Datagrundlag for ad-hoc analyse af salg](ad-hoc-analysis-sales.md#data-foundation-for-ad-hoc-analysis-on-sales)
- [Datagrundlag for ad-hoc analyse af indkøb](ad-hoc-analysis-purchasing.md#data-foundation-for-ad-hoc-analysis-on-purchasing)

## <a name="see-also"></a>Se også

[Analysere liste- og forespørgselsdata med analysetilstand](analysis-mode.md)  
[Oversigt over økonomisk analyse](bi.md)  
[Analyse, Business Intelligence og rapporteringsoversigt](reports-bi-reporting.md)  
[Oversigt for Finance](finance.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
