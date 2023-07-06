---
title: 'Fremgangsmåde: Oprette lokationer til brug af placeringer'
description: Placeringer udgør den grundlæggende lagerstruktur og bruges til at fremsætte forslag om placeringen af varer.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
---

# <a name="set-up-locations-to-use-bins"></a><a name="set-up-locations-to-use-bins"></a><a name="set-up-locations-to-use-bins"></a>Oprette lokationer til brug af placeringer

Placeringer repræsenterer den grundlæggende lagerstruktur og kan foreslå, hvor varer skal lægges på. Når du har oprettet placeringerne, kan du meget præcist definere deres indhold, eller de kan fungere som løs placering uden angivet indhold.

Hvis du vil bruge placeringsfunktionen på en lokation, skal du aktivere **Lokationskort** i til/fra-feltet **Tvungen placering**. Når du har aktiveret til/fra, er felterne **placeringskode** og **zonekode** tilgængelige i følgende dokumenter:

* Lagerstedskvitteringshoved
* Lagerstedskvitteringslinjer
* Læg-på-linjer for lagersted
* Lagerleverancehoved
* Lagerleverancelinjer
* Læg-på-linjer for lagersted

Det næste trin er at designe varestrømmen på placeringen ved at angive placeringskoder i konfigurationsfelter, der repræsenterer forskellige flows.  

> [!NOTE]  
> Du skal oprette placeringskoder, før du kan angive dem på en lokation. Du kan finde flere oplysninger i [Oprette placeringer](warehouse-how-to-create-individual-bins.md).  

## <a name="to-set-up-a-location-to-use-bins"></a><a name="to-set-up-a-location-to-use-bins"></a><a name="to-set-up-a-location-to-use-bins"></a>Sådan konfigureres en lokation til at bruge placeringer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lokationer**, og vælg derefter det relaterede link.  
2. Vælg den lokation, hvor du vil bruge placeringer.  
3. Vælg handlingen **Rediger**.  
4. Markér afkrydsningsfeltet **Tvungen placering** i oversigtspanelet **Lagersted**.  
5. Hvis du ikke bruger styret læg-på-lager og pluk for lokationen, skal du udfylde feltet **Standardplacering** med den metode, når [!INCLUDE [prod_short](includes/prod_short.md)] skal bruge til at tildele en standardplacering for en vare.  
6. Åbn kortet for den lokation, du vil konfigurere placeringer for.
7. I oversigtspanelet **Placeringer** skal du vælge de placeringer, der skal bruges som standardplaceringer for modtagelser, leverancer samt for indgående, udgående og åbne produktionsplaceringer.  

    De placeringskoder, som du angiver her, vises automatisk i hovederne og på linjerne af de forskellige lagerdokumenter. Standardplaceringerne definerer alle start- og slutplaceringer for varer på lagerstedet.  
8. Hvis du bruger styret læg-på-lager og pluk, skal du vælge en placering til lagerreguleringerne. Placeringskoden i feltet **Regul.placeringskode** angiver den virtuelle placering, hvor programmet registrerer afvigelser i lagerbeholdningen:

    * Når du observerer forskellene i lagerkladden
    * Afvigelser, der er beregnet af programmet, når du registrerer en lagerplaceringsopgørelse  
9. Eventuelt: Udfyld felterne i oversigtspanelet **Placeringspolitikker**. De vigtigste felter er **Placeringskap.regel**, **Tillad nedbrydning** og **Læg-på-lager-skabelonkode**.  
10. Vælg oversigtspanelet **Lagersted**, og udfyld felterne **Udgående lagerekspeditionstid**, **Indgående lagerekspeditionstid** og **Basiskalenderkode**. Du kan finde flere oplysninger i [Oprette basiskalendere](across-how-to-assign-base-calendars.md).

## <a name="fill-in-the-consumption-bin"></a><a name="fill-in-the-consumption-bin"></a><a name="fill-in-the-consumption-bin"></a>Udfylde forbrugsplaceringen

Følgende flow-diagram viser, hvordan feltet **Placeringskode** i produktionsordrekomponenter udfyldes i henhold til din lokationsopsætning.

:::image type="content" source="media/binflow.png" alt-text="Placeringskodefeltet på produktionsordrekomponentlinjerne.":::

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/configure-bins-location/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Montagestyring](assembly-assemble-items.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
