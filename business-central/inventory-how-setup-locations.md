---
title: Oprette et lokationskort og definere overflytningsruter
description: Du kan oprette et lokationskort for hvert sted, du gemme lagervarer, for eksempel et lagersted eller distributionscenter, og definere ruter for at overflytte varer mellem lokationerne.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/01/2021
ms.author: edupont
ms.openlocfilehash: 0319f0c64dd46610aa82705257091bd9478ac14f
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184320"
---
# <a name="set-up-locations"></a>Opsætte lokationer

Hvis du køber, gemme eller sælger varer i mere end ét område eller lagersted, skal du oprette hver lokation med et lokationskort og definere overflytningsruter. [!INCLUDE [prod_short](includes/prod_short.md)] bruger lokationer til at holde styr på lagerbeholdningen i begge enkle sager og de mere komplekse lagerprocesser.

Du kan derefter oprette dokumentlinjer for en bestemt lokation vis tilgængeligehed pr. lokation og vare samt overføre lagerbeholdning mellem lokationer. Der er flere oplysninger i [Administrere lager](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a>Lokationskort

Lokationskortet angiver oplysninger om en lokation, f. eks. et lager eller distributionscenter. Du kan give hver lokation et navn og en kode, der repræsenterer lokationen. Du kan derefter angive lokationskoden i andre dele af programmet, når du vil registrere transaktioner for en given lokation.  

Du kan angive oplysninger om placeringer og lagermetoder. På baggrund af de valgte lagermetoder kan du bruge indstillingerne i oversigtspanelet **Placeringer** til at definere de placeringer, der skal bruges som standardplaceringer, når du udfører transaktioner. Hvis du bruger styret læg-på-lager og pluk, kan du bruge de fleste af indstillingerne i oversigtspanelet **Plac.metode** til at definere, hvordan du vil bruge de forskellige avancerede lagerfunktioner.  

Nogle indstillingsfelter er gråtonede og deaktiveret af andre indstillinger i vinduet **Lokationskort** for at forhindre ikke-understøttede opsætningskombinationer.  

Luk handlingen **Zoner** eller **Placeringer** for at få vist oplysninger om zoner og placeringer, der kan være defineret for den pågældende lokation.

### <a name="to-create-a-location-card"></a>Sådan oprettes et lokationskort

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lokationer**, og vælg derefter det tilknyttede link.
2. Vælg handlingen **Ny**.
3. På siden **Lokationskort** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Gentag trin 2 og 3 for hver lokation, hvor du vil foretage lageropgørelse.

> [!NOTE]  
> Mange af felterne på lokationskortet henviser til håndtering af varer i indgående og udgående lagerprocesser. Felterne er ikke relevante for virksomheder, der ikke har brug for mere komplekse lagerfunktioner. Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).

Du kan ændre konfigurationen for en lokation senere, men du kan ikke redigere opsætningen af lokationer, der har vareposter.  

Hvis du har flere lokationer, kan du definere overflytningsruter mellem lokationer.  

### <a name="to-create-a-transfer-route"></a>Sådan oprettes en overflytningsrute

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Overflytningsruter**, og vælg derefter det relaterede link.
2. Du kan også vælge handlingen **Overflytningsruter** på enhver **Lokationskort**-side.
3. Vælg handlingen **Ny**.
4. På siden **Lokationskort** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Du kan nu overflytte lagervarer mellem to lokationer. Du kan finde flere oplysninger i [Overflytte lagerbeholdning mellem lokationer](inventory-how-transfer-between-locations.md).    

## <a name="bins"></a>Placering

Placeringer udgør den grundlæggende lagerstruktur og bruges til at fremsætte forslag om placeringen af varer. Når du har oprettet placeringerne, kan du meget præcist definere det indhold, du vil placere på hver placering, eller placeringen kan fungere som en løs placering uden angivet indhold. Placeringer anvendes primært i basis-og forudlager operationer. Hvis du administrerer lagerbeholdningen i en mere simpel opsætning, har du sandsynligvis ikke brug for placeringer.

Hvis du vil bruge placeringsfunktionen på en lokation, skal du først aktivere funktionen på **Lokationer**-kortet ved at vælge feltet **Tvungen placering** i oversigtspanelet **Lagersted**. Derefter kan du designe varestrømmen på placeringen ved at angive placeringskoder i konfigurationsfelter, der repræsenterer forskellige strømme.

> [!NOTE]
> Placeringskoderne skal være oprettet, før du kan angive placeringskoder på lokationskortet.

Du kan finde flere oplysninger i [Oprette placeringer](warehouse-how-to-create-individual-bins.md) og [Oprette placeringstyper](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones"></a>Zoner

Hvis du vil strukturere placeringerne under zoner, kan du gøre det på siden **Zoner**.

[!INCLUDE [prod_short](includes/prod_short.md)] kopierer de felter, som du definerer i forbindelse med en bestemt zone, kopieres til placeringerne i denne. Det betyder, at du kan knytte en zone til en placering eller placeringsskabelon (vha. et placeringsoprettelsesfilter), så programmet udfylder en række andre felter automatisk.

Du kan også vælge kun at oprette en enkelt zone og udelukkende organisere lagerstedet efter placeringer. Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).  

## <a name="see-also"></a>Se også

[Administrere lager](inventory-manage-inventory.md)  
[Overflytte lagerbeholdning mellem lokationer](inventory-how-transfer-between-locations.md)  
[Oprette placeringer](warehouse-how-to-create-individual-bins.md)  
[Oprette placeringstyper](warehouse-how-to-set-up-bin-types.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]