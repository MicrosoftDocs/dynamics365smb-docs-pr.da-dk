---
title: Ad hoc-analyse af lagerdata
description: 'Få mere at vide om, hvordan du kan bruge dataanalysetilstand til at analysere lagerdata.'
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 05/03/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="ad-hoc-analysis-of-inventory-data"></a>Ad hoc-analyse af lagerdata

I artikel beskriver, hvordan du bruger funktionen **Dataanalyse** til at analysere lagerdata direkte fra listesider og forespørgsler. Du behøver ikke at køre en rapport eller skifte til et andet program, f.eks. Excel. Funktionen indeholder en interaktiv og alsidig måde at beregne, opsummere og gennemgå data på. I stedet for at køre rapporter med indstillinger og filtre kan du tilføje flere faner, der repræsenterer forskellige opgaver eller visninger på dataene. Nogle eksempler er "lager, der udløber" eller "bedste sælgere" eller enhver anden visning, du kan forestille dig. Du kan få mere at vide om, hvordan du bruger funktionen **Dataanalyse** ved at gå til [Analysér liste og forespørge på data med analysetilstand](analysis-mode.md).

Brug følgende listesider til ad hoc-analyse af lagerprocesser:

- [Finansposter for vare](https://businesscentral.dynamics.com/?page=38)

## <a name="inventory-ad-hoc-analysis-scenarios"></a>Lager ad hoc-analysescenarier

Brug funktionen **Dataanalyse** til hurtig faktatjek og ad hoc-analyse:

- Hvis du ikke vil køre en rapport.
- Hvis der ikke er en rapport om dine specifikke behov.
- Hvis du hurtigt vil gentage for at få et godt overblik over en del af din virksomhed.

Følgende afsnit indeholder eksempler på lagerscenarier i [!INCLUDE [prod_short](includes/prod_short.md)].

| Område | Til... | Åbn denne side i analysetilstand | Brug af disse felter |
| ---- | ----- | ------------------------------- |------------------- |
| [Disponibel lagerbeholdning](#example-inventory-on-hand) | Få vist en oversigt over varer, der er tilgængelige i din lagerbeholdning. | [Finansposter for vare](https://businesscentral.dynamics.com/?page=38) | **Varenr.**, **Restantal** |
|[Eksempel: spor, der udløber, eller gammelt lager](#example-track-expiring-or-old-stock) | Få vist en oversigt over varer på lageret, der har været på lager i lang tid og ikke sælger særlig godt. | [Finansposter for vare](https://businesscentral.dynamics.com/?page=38) | **Bogføringsdato-år**, **Bogføringsdato-måned**, **,Varenr.**, **Bogføringsdato**, **Posttype**, **Antal** og **Restantal**. |
| [Returnerede varer efter returårsag](#example-returned-items-by-return-reason) | Få vist en oversigt over varer, som kunderne returnerer, kategoriseret efter returårsagen. Brug dette til analyse til kvalitetskontrol. | [Finansposter for vare](https://businesscentral.dynamics.com/?page=38) | **Returårsagskode**, **Bogføringsdato-måned**, **Antal**, **Kostbeløb**, **Bogføringsdato**, **Bilagstype**, **Varenr.** og  **Bilagsnr.**. |
| Lagerbeholdning | Få et overblik over køb og salg i lagerbeholdningen efter måned eller kvartal. | [Finansposter for vare](https://businesscentral.dynamics.com/?page=38) | **Bogføringsdato-år**, **Bogføringsdato-måned**, **Varenr.**, **Antal**, **Salgsbeløb**, **Kostbeløb (faktisk)** og **Bogføringsdato-måned** |
| [Flytninger på lager] | Få et overblik over, hvordan varer på dit lager flyttes mellem lokationer. | [Finansposter for vare](https://businesscentral.dynamics.com/?page=38) | **Lokationskode**, **Antal**, **Bogføringsdato**, **Varenr.** |

## <a name="example-inventory-on-hand"></a>Eksempel: Disponibel lagerbeholdning

Følg disse trin for at analysere varer på lager, der er på lager:

1. Åbn [Finansposter for varer](https://businesscentral.dynamics.com/?page=38)-listen, og vælg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivér analysetilstand."::: tænd for analysetilstand.
1. Gå til menuen **Kolonner**, og fjern alle kolonner (markér feltet ud for feltet **Søg**).
1. Træk feltet **Varenr.** til området **Rækkegruppe**. Træk felterne i den pågældende rækkefølge.
1. Træk feltet **Restantal** til områderne **Værdier**.
1. Angiv filteret **Ikke ens** til **0** for **Restantal**. Hvis du ikke tillader negative lagerniveauer, skal du indstille filteret **Større end** til **0**.
1. Du kan også føje andre felter til analysen og eventuelt pivotere efter placering eller andre felter.
1. Omdøb din analysefane til **Disponibelt lager** eller noget, der beskriver denne analyse.

Følgende billede viser resultatet af disse trin.

:::image type="content" source="media/data-analysis-inventory-on-hand.png" alt-text="Eksempel på, hvordan du udfører en analyse af disponible lagerdata." lightbox="media/data-analysis-inventory-on-hand.png":::

## <a name="example-track-expiring-or-old-stock"></a>Eksempel: spor, der udløber, eller gammelt lager

Analysere varer på lageret, der har været på lager i lang tid og ikke sælger særlig godt ved at følge disse trin:

1. Åbn [Finansposter for varer](https://businesscentral.dynamics.com/?page=38)-listen, og vælg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivér analysetilstand."::: tænd for analysetilstand.
1. Gå til menuen **Kolonner**, og fjern alle kolonner (markér feltet ud for feltet **Søg** i højre side).
1. Træk **Bogføringsdato-år**, **Bogføringsdato-måned** og **Varenr.** til området **Rækkegrupper**. Træk felterne i den pågældende rækkefølge.
1. Vælg felterne **Bogføringsdato**, **Posttype**, **Antal**, **Restantal** i området **Kolonnerne**.
1. Angiv filteret **Mindre end** til **Bogføringsdato** for at definere, hvad du mener med "gammel".
1. Omdøb din analysefane til **Gammelt lager** eller noget, der beskriver denne analyse.

Følgende billede viser resultatet af disse trin.

:::image type="content" source="media/data-analysis-inventory-dead-stock.png" alt-text="Eksempel på, hvordan du udfører dataanalyse på siden Finansposter." lightbox="media/data-analysis-inventory-dead-stock.png":::

## <a name="example-returned-items-by-return-reason"></a>Eksempel: returnerede varer efter returårsag

Hvis du vil analysere returnerede varer sorteret efter årsagerne til returneringen, skal du benytte følgende fremgangsmåde:

1. Åbne listen [Finansposter for vare](https://businesscentral.dynamics.com/?page=38).
1. Tilføj **Returårsagskode** ved at tilpasse siden. I menuen **Indstillinger** skal du vælge **Tilpas**.
1. Afslut tilpasningstilstand.
1. Vælg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Skift til analysetilstand."::: tænd for analysetilstand.
1. Gå til menuen **Kolonner**, og fjern alle kolonner (markér feltet ud for feltet **Søg** i højre side).
1. Træk felterne **Returårsagskode** og **Bogføringsdato-måned** til området **Rækkegrupper** . Træk felterne i den pågældende rækkefølge.
1. Træk felterne  **Antal** og **Kostbeløb** til området **Værdier**.
1. Tilføj eventuelle andre felter, du ønsker i analysen, og aktivér dem i området **Kolonner**. Du kan f.eks. tilføje felterne **Bogføringsdato**, **Bilagstype**, **Bilagsnr.** og **Varenr.**.
1. Omdøb din analysefane til **Returnerede varer efter returårsag** eller noget, der beskriver denne analyse.  

## <a name="example-inventory-throughput"></a>Eksempel: lagerbeholdning

1. Åbn [Finansposter for varer](https://businesscentral.dynamics.com/?page=38)-listen, og vælg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivér analysetilstand."::: tænd for analysetilstand.
1. Gå til menuen **Kolonner**, og fjern alle kolonner (markér feltet ud for feltet **Søg** i højre side).
1. Aktiver **Pivot-tilstand** (placeret direkte over **Søg** feltet i højre side).
1. Træk felterne **Bogføringsdato-år**, **Bogføringsdato-måned** og **Varenr.** til området **Rækkegrupper**.
1. Træk felterne **Antal**, **Salgsbeløb** og **Kostbeløb (faktisk)** til **Antal**.
1. Træk felterne **Bogføringsdato-måned** til området **Kolonnegrupper**.
1. Omdøb din analysefane til **Lagerbehandling efter måned** eller noget, der beskriver denne analyse.  

## <a name="inventory-movements"></a>Flytninger (lager)

Følg disse trin for at spore lagerbevægelser mellem lokationer:

1. Åbn [Finansposter for varer](https://businesscentral.dynamics.com/?page=38)-listen, og vælg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivér analysetilstand."::: tænd for analysetilstand.
1. Gå til menuen **Kolonner**, og fjern alle kolonner (markér feltet ud for feltet **Søg** i højre side).
1. Træk feltet **Lokationskode** til området **Rækkegruppe**.
1. Træk feltet **Antal** til området **Værdier**.
1. Tilføj eventuelle andre felter, du ønsker i analysen, og aktivér dem i området **Kolonner**. Du kan f.eks. tilføje feltet **Varenr.**.
1. Omdøb din analysefane til **Lagerbevægelser** eller noget, der beskriver denne analyse.  

   > [!TIP]
   > Hvis du tilføjer feltet Bogføringsdato, kan du også spore bevægelser over tid.

## <a name="data-foundation-for-ad-hoc-analysis-on-inventory"></a>Datagrundlag for ad-hoc analyse af lager

Når en salgsordre bogføres, opdateres [!INCLUDE [prod_short](includes/prod_short.md)] kreditorens konto, regnskabet og vareposterne.

- For hver salgsordrelinje oprettes der en varepost i tabellen **Varepost** (hvis salgslinjerne indeholder varenumre). Salgsordrer bliver desuden altid registreret i tabellerne **Salgsleverancehoved** og **Salgsfakturahoved**. Hvis du vil vide mere om bogføring af salg, skal du [Bogføre salg](ui-post-sales.md).

Når et købsdokument bogføres, opdaterer [!INCLUDE [prod_short](includes/prod_short.md)] kreditorens konto, regnskabet og vareposterne, og ressourceposterne.

- For hver købslinje oprettes der poster i tabellen **Varepost** (hvis købslinjen er af typen Vare). Købsdokumenter registreres desuden altid i tabellerne **Købsleverancehoved** og **Købsfakturahoved**. Flere oplysninger i [Bogføring af køb](purchasing-how-record-purchases.md#posting-purchases).

## <a name="see-also"></a>Se også

[Analysere liste- og forespørgselsdata med analysetilstand](analysis-mode.md)  
[Oversigt over lageranalyser](inventory-analytics-overview.md)  
[Analyse, Business Intelligence og rapporteringsoversigt](reports-bi-reporting.md)  
[Oversigt over lager](inventory-manage-inventory.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
