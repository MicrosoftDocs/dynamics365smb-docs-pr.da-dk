---
title: Oprette et lokationskort og definere overflytningsruter (indeholder video)
description: 'Hvis du køber, gemmer eller sælger varer på mere end ét sted, kan du angive hver placering som en lokation.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'warehouse, distribution center'
ms.search.forms: '5703, 15'
ms.date: 03/25/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-locations"></a>Opsætte lokationer

Lokationer er steder, f. eks. lagersteder, hvor du køber, sælger eller sælger varer. [!INCLUDE [prod_short](includes/prod_short.md)] bruger lokationer til at holde styr på lagerbeholdningen i både enkle og komplekse lagerprocesser.

Du kan derefter oprette dokumentlinjer for en bestemt lokation vis tilgængeligehed pr. lokation og vare samt overføre lagerbeholdning mellem lokationer. Hvis du vil vide mere, skal du gå til [Administrer lager](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a>Lokationskort

Du skal angive oplysninger om en lokation, f. eks. et lager eller distributionscenter på siden **Lokationskort**. Du kan give hver lokation et navn og en kode, der repræsenterer lokationen. Du kan derefter angive lokationskoden i andre dele af programmet, når du vil registrere transaktioner for en given lokation.  

Du kan angive oplysninger om placeringer og lagermetoder. Baseret på lager politikker kan du bruge indstillingerne i oversigtspanelet **Placeringer** til at angive de placeringer, der som standard skal bruges til transaktioner. Hvis du bruger styret læg-på-lager og pluk, kan du bruge de fleste af indstillingerne i oversigtspanelet **Plac.metode** til at definere, hvordan du kan bruge de forskellige avancerede lagerfunktioner.  

Nogle indstillingsfelter på indstillinger på siden **Lokationskort** for at forhindre ikke-understøttede opsætningskombinationer.  

Luk handlingen **Zoner** eller **Placeringer** for at få vist oplysninger om zoner og placeringer, der kan være defineret for den pågældende lokation.

### <a name="to-set-up-a-location"></a>Sådan oprettes en lokation

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lokationer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. På siden **Lokationskort** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Gentag trin 2 og 3 for hver lokation, hvor du vil foretage lageropgørelse.

> [!NOTE]  
> Mange af felterne på lokationskortet henviser til håndtering af varer i indgående og udgående lagerprocesser. Disse felter er ikke relevante for virksomheder, der ikke har brug for mere komplekse lagerfunktioner. Flere oplysninger i [Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md).

Du kan ændre konfigurationen for en lokation, så længe det ikke har vareposter.  

Hvis du har flere lokationer, kan du definere overflytningsruter mellem lokationer. Hvis du vil vide mere om overflytningsruter, skal du gå til [Oprette en overførselsrute](inventory-how-setup-locations.md#to-create-a-transfer-route).

### <a name="to-create-a-transfer-route"></a>Sådan oprettes en overflytningsrute

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **overflytningsruter**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
4. På siden **Lokationskort** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Du kan nu overflytte lagervarer mellem to lokationer. Hvis du vil vide mere om overførsler, skal du gå til [Overføre lager mellem lokationer](inventory-how-transfer-between-locations.md).

## <a name="bins"></a>Placering

Placeringer repræsenterer den grundlæggende lagerstruktur og kan foreslå, hvor varer skal lægges på. Placeringerne kan have indhold eller være flydende placeringer uden specifikt indhold.

Hvis du vil bruge placeringsfunktionen på en lokation, skal du først aktivere funktionen på siden **Lokationskort** ved at aktivere feltet **Tvungen placering** i oversigtspanelet **Lagersted**. Du kan designe varestrømmen på lokationen ved at angive placeringskoder i felterne for lager processerne i oversigtspanelerne **Placeringer** og **Placeringsregler**.

> [!NOTE]
> Placeringskoderne skal være oprettet, før du kan angive placeringskoder på en lokation. Hvis du vil vide mere om placeringer, skal du gå til [Oprette placeringer](warehouse-how-to-create-individual-bins.md) og [Oprette placeringstyper](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones"></a>Zoner

Hvis du vil strukturere placeringerne under zoner, kan du gøre det på siden **Zoner**. Når du tildeler en zone til placeringer, kopierer [!INCLUDE [prod_short](includes/prod_short.md)] oplysninger fra zonen til placeringerne. Du kan også vælge at oprette en zone og bruge placeringer alene til at organisere lagerstedet. Flere oplysninger om zoner [Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md).  

## <a name="default-dimensions-for-locations"></a>Standarddimensioner for lokationer

Dimensioner er værdier, der kategoriserer poster, så du kan spore og analysere dem ved hjælp af rapporteringsværktøjer. Dimensioner kan f.eks. angive det projekt eller den afdeling, en post kommer fra. Hvis du har standarddimensioner, undgår du fejl og skal angive dimensioner manuelt på transaktionsniveau, hvis alle varer kommer fra én enkelt lokation og afdeling.

Du kan angive standarddimensioner for en lokation på siden **Lokationskort** ved at klikke på lokation og derefter på **Dimensioner**. Derefter tildeles standarddimensionerne for lokationen til følgende dokumenter, når du vælger lokationen på en linje.

* Overflytningsordrer
* Fysisk lagerordrer
* Vareleverancer
* Lagermodtagelser
* Varekladder

Efter behov kan du slette eller ændre dimensionerne på linjen. I feltet **Værdibogføring** kan du kræve, at personer angiver dimensioner for bestemte lokationer, før de kan bogføre en post. Hvis du vil give brugerne mulighed for at vælge bestemte dimensionsværdier, kan du angive dem i feltet **Filter for tilladte værdier**. Du kan også medtage dimensionsværdier for lokationer på siden **Prioriteringer for standarddimensioner** og kombinationer af prioritet og dimensionsregler på siden **Dimensionskombinationer**.

Da overflytningsordre dokumenter og omposterings kladder vedrører mere end én lokation, er den rækkefølge, som du angiver data i, vigtig. Standarddimensioner kopieres fra feltet sidste lokation (den transitlokationen ignoreres).

### <a name="example-of-default-dimensions-on-locations"></a>Eksempel på standarddimensioner for lokationer

Følgende eksempler viser, hvordan standarddimensionen bruges.

Du har følgende dimensionsindstillinger:

* Lokation EAST. Afdelingsdimension er ADM
* Lokation WEST. Afdelingsdimension er PROD

Du kan angive placeringen på en overflytningsordre på følgende måde:

1. Fra lokation = EAST
2. Til lokation = WEST

PROD-dimensionen kopieres fra lokationen WEST.

Når der skal angives filtre i rapporten, skal du udfylde filterne på følgende måde:

1. Til lokation = WEST
2. Fra lokation = EAST

ADM-dimensionen kopieres fra lokationen EAST.

## <a name="see-also"></a>Se også

[Administrere lager](inventory-manage-inventory.md)  
[Overflytte lagerbeholdning mellem lokationer](inventory-how-transfer-between-locations.md)  
[Oprette placeringer](warehouse-how-to-create-individual-bins.md)  
[Oprette placeringstyper](warehouse-how-to-set-up-bin-types.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
