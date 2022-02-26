---
title: Lægge produktionsafgange på lager
description: Den måde, du lægger afgang på lager fra produktion, afhænger af, hvordan lagerstedet er sat op som en lokation. Læg-på-lager kan udføres på følgende måder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 87c0a1cb86d94b673c3c4ee21ce0d62d59eeb753
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6438128"
---
# <a name="put-away-production-or-assembly-output"></a>Lægge produktions- eller montageafgange på lager

Den måde, du lægger afgang på lager fra produktion, afhænger af, hvordan lagerstedet er sat op som en lokation. Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).  

I grundlæggende lageropsætninger, hvor lokationen kræver læg-på-lager, men ikke modtagelse, skal du bruge dokumentet **Læg-på-lager (lager)** til at bogføre produktionsoutput og registrere afgangens læg-på-lager.  

> [!NOTE]  
> Læg-på-lager understøttes ikke for montageprocesser. Du bogfører en montageordre for at registrere afgang. Hvis du bruger placeringer, kan du flytte varer mellem placeringer senere. Du kan finde flere oplysninger i [Flytte varer ad hoc i grundlæggende lageropsætninger](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  

I avancerede lageropsætninger, hvor lokationen kræver både læg-på-lager og modtagelse, kan du enten oprette et internt læg-på-lager-dokument eller et bevægelsesdokument for at lægge afgangen på lager.  

## <a name="to-put-away-production-output-with-an-inventory-put-away"></a>Sådan lægges produktionsafgang på lager med en læg-på-lager-aktivitet

Det første trin til at lægge afgange på lager er at oprette den indgående lageranmodning. Denne anmodning oplyser lagerstedet om, at produktions- eller montageordreafgangen er klar til at blive lagt på lager.

### <a name="to-create-the-inbound-warehouse-request"></a>Sådan opretttes den indgående lageranmodning  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Frigivet produktionsordre**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Opret indgående lageranmodning** på den produktionsordre, der er klar til at blive lagt på lager.  

> [!NOTE]  
> Du kan også oprette en indgående lageranmodning ved at vælge feltet **Opret indgående anmodning**, når du opdaterer produktionsordren. Du kan finde flere oplysninger i [Forny eller omplanlægge produktionsordrer](production-how-to-replan-refresh-production-orders.md).  

### <a name="to-put-output-away-with-an-inventory-put-away"></a>Sådan lægges afgang på lager med en læg-på-lager-aktivitet  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Læg-på-lager (lager)**, og vælg derefter det relaterede link.  
2.  Opret en ny læg-på-lager-aktivitet. Du kan finde flere oplysninger i [Lægge varer på lager med Læg-på-lager](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3.  Du kan få adgang til produktionsordreafgangen ved at vælge handlingen **Hent kildedokumenter** og derefter vælge den frigivne produktionsordre.  
4.  Udfyld læg-på-lager-linjerne efter behov.
5.  Når linjerne er klar til at blive bogført, skal du vælge handlingen **Bogfør**. Bogføringen opretter de nødvendige lagerposter og bogfører afgangen af varer.  

Du kan også oprette et **Læg-på-lager (lager)** direkte fra den frigivne produktionsordre. Du kan finde flere oplysninger i [Lægge varer på lager med Læg-på-lager](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Når du bogfører læg-på-lager, antages det, at alle operationer er bogført i overensstemmelse med standardruten, dvs., at afgangsantal er bogført i henhold til den seneste operation. Du kan bruge afgangskladde til at bogføre afvigelser i afgangsantal og opstillings- og operationstid. Hvis der er krav om delvis bogføring, efter du har oprettet læg-på-lager, kan du gøre dette under opstillingstid og antal for alle operationer undtagen den sidste. I det tilfælde kontrolleres den sidste operation af læg-på-lager.  

Hvis du kun har behov for at bogføre opstillings- og operationstid på den sidste operation, skal du angive afgangsantallet for den sidste operation til 0. Alternativt kan du vælge overhovedet ikke at bogføre den sidste linje ved simpelthen at slette den.  

## <a name="to-put-assembly-and-production-output-away-in-advanced-warehouse-configurations"></a>Plukke til montage eller produktion til lager i avancerede lageropsætninger
Når du bogfører afgangen for produktion eller montageordre på det lagersted, der er sat op til at bruge styret læg-på-lager og pluk, placeres afgangen på den placering, der er defineret i produktions- eller montageordren. 

I følgende tabel beskrives forskellige metoder til flytning af varer inden for lagerstedet med avancerede konfigurationer, hvor alle lageraktiviteter skal udføres i en styret arbejdsgang. 

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Flytte varer med lagerbevægelseskladden.|[Flytte varer i avancerede lageropsætninger](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet)|  
|Oprette en interne montagevarer eller producerede varer på lager i en avanceret lageropsætning.|[Oprette en intern læg-på-lager-aktivitet](warehouse-how-to-create-put-aways-from-internal-put-aways.md#to-create-an-internal-put-away)|

> [!NOTE]  
> Du kan ikke angive kildedokumentnummeret, f.eks. prod.ordrenr., i dokumenterne intern læg-på-lager, læg-på-lager eller bevægelse i disse to procedurer.  

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Warehouse Management](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
