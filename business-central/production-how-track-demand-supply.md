---
title: "Sådan spores relationer mellem behov og forsyning | Microsoft Docs"
description: "Fra ethvert forsynings- eller behovsdokument i det såkaldte ordrenetværk, kan du spore ordrebehov (sporet antal), forecast, rammesalgsordre eller planlægningsparameter (ikkesporet antal), der er årsag til den pågældende planlægningslinje."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 72632dfd729806f9b96bff886d5dfce40bf8cb18
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="track-relations-between-demand-and-supply"></a>Spore relationer mellem behov og forsyning
Fra ethvert forsynings- eller behovsdokument i det såkaldte ordrenetværk, kan du spore ordrebehov (sporet antal), forecast, rammesalgsordre eller planlægningsparameter (ikkesporet antal), der er årsag til den pågældende planlægningslinje.

Planlægningskladderne indeholder også yderligere planlægningsoplysninger om ikke-ordreenheder for at hjælpe planlæggeren med at opnå den optimale forsyningsplan. Du kan finde flere oplysninger i afsnittet "Ikke-sporede planlægningselementer".

## <a name="to-track-linked-items"></a>Sådan spores tilknyttede varer
Ordresporing viser, hvordan salgsordrer, produktionsordrer og købsordrer er relaterede til produktionsordrer via planlægnings- og reservationssystemerne.

Nedenstående beskrives, hvordan tilknyttede varer spores på en fastlagt produktionsordre. Trinene er de samme for alle andre typer og i forbindelse med planlægningskladdelinjer.

1. Vælg ikonet ![Søg efter side eller en rapport](media/ui-search/search_small.png "Søg efter side eller en rapport ikonet"), angiv **Fastlagt produktionsordre**, og vælg derefter det relaterede link.
2. Åbn den relevante fastlagte produktionsordre på listen.
3. I oversigtspanelet **Linjer** skal du vælge handlingen **Funktioner** og derefter vælge handlingen **Ordresporing**.

På linjerne i vinduet **Ordresporing** vises de bilag, der har relation til den aktuelle produktionsordrelinje.

## <a name="untracked-planning-elements"></a>Ikke-sporede planlægningselementer
Vinduet **Ikke-sporede planlægningselementer** åbnes, når du klikker på feltet **Ikke-sporet antal** i vinduet **Ordreplanlægning**. Det tjener to formål:

1. Indeholde oplysninger om ikke-sporet antal, der vises, når brugeren slår op fra vinduet Ordresporing for at få vist ikke-sporede antal.
2. Det skal indeholde advarselsmeddelelser, der vises, når brugeren vælge ikonet **Advarsel** i vinduet **Planlægningskladde**.

Vinduet indeholder poster, der tager højde for et ikke-sporet overskudsantal i ordresporingsnetværket. Disse poster genereres i forbindelse med planlægningskørslen og forklarer, hvor det ikke-sporede overskud på ordresporingslinjerne stammer fra. Det ikke-sporede overskud kan stamme fra:

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

