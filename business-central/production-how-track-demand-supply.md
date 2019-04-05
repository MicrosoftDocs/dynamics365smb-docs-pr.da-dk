---
title: Sådan spores relationer mellem behov og forsyning | Microsoft Docs
description: Fra ethvert forsynings- eller behovsdokument i det såkaldte ordrenetværk, kan du spore ordrebehov (sporet antal), forecast, rammesalgsordre eller planlægningsparameter (ikkesporet antal), der er årsag til den pågældende planlægningslinje.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: de71e4c305b775df8c10306ecc474bc6944d0787
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "793076"
---
# <a name="track-relations-between-demand-and-supply"></a>Spore relationer mellem behov og forsyning
Fra ethvert forsynings- eller behovsdokument i det såkaldte ordrenetværk, kan du spore ordrebehov (sporet antal), forecast, rammesalgsordre eller planlægningsparameter (ikkesporet antal), der er årsag til den pågældende planlægningslinje.

Planlægningskladderne indeholder også yderligere planlægningsoplysninger om ikke-ordreenheder for at hjælpe planlæggeren med at opnå den optimale forsyningsplan. Du kan finde flere oplysninger i [Ikke-sporede planlægningselementer](production-how-track-demand-supply.md#untracked-planning-elements).

## <a name="to-track-linked-items"></a>Sådan spores tilknyttede varer
Ordresporing viser, hvordan salgsordrer, produktionsordrer og købsordrer er relaterede til produktionsordrer via planlægnings- og reservationssystemerne.

Nedenstående beskrives, hvordan tilknyttede varer spores på en fastlagt produktionsordre. Trinene er de samme for alle andre typer og i forbindelse med planlægningskladdelinjer.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Fastlagt produktionsordre**, og vælg derefter det relaterede link.
2. Åbn den relevante fastlagte produktionsordre på listen.
3. I oversigtspanelet **Linjer** skal du vælge handlingen **Funktioner** og derefter vælge handlingen **Ordresporing**.

På linjerne i vinduet **Ordresporing** vises de bilag, der har relation til den aktuelle produktionsordrelinje.

## <a name="untracked-planning-elements"></a>Ikke-sporede planlægningselementer
Siden **Ikke-sporede planlægningselementer** åbnes, når du klikker på feltet **Ikke-sporet antal** på siden **Ordreplanlægning**. Det tjener to formål:

1. Indeholde oplysninger om ikke-sporet antal, der vises, når brugeren slår op fra siden Ordresporing for at få vist ikke-sporede antal.
2. Det skal indeholde advarselsmeddelelser, der vises, når brugeren vælge ikonet **Advarsel** på siden **Planlægningskladde**.

Siden indeholder poster for ikke-sporet overskud i ordresporingsnetværket. Disse poster genereres i forbindelse med planlægningskørslen og forklarer, hvor det ikke-sporede overskud på ordresporingslinjerne stammer fra. Det ikke-sporede overskud kan stamme fra:

- Produktionsforecast
- Rammeordrer
- Sikkerhedslager
- Genbestillingspunkt
- Maks. lagerbeholdning
- Ordrekvantum
- Maks. ordrestørrelse
- Min. ordrestørrelse
- Oprundingsfaktor
- Aktionsgrænse (% af lotstr.)

## <a name="see-also"></a>Se også  
[Planlægning](production-planning.md)   
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Designoplysninger: Reservation, sporing og aktionsmeddelelser](design-details-reservation-order-tracking-and-action-messaging.md)  
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)   
[Konfigurere bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
