---
title: Flytte varer i avanceret lageropsætning
description: I dette emne forklares det, hvordan en erfaren medarbejder kan arrangere flytning af varer i avancerede logistik konfigurationer – kan anvendes på lokationer med styret læg-på-lager og pluk.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7351
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 02a96b48049207d2272c62b008148c000cf676e0
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8520574"
---
# <a name="move-items-in-advanced-warehouse-configurations"></a>Flytte varer i avancerede lageropsætninger
I avancerede lageropsætninger, dvs. lokationer med styret læg-på-lager og pluk, udføres lagerbevægelser fra én placering til en anden af en overordnet medarbejder, der forbereder lagerbevægelserne i bevægelseskladden og derefter opretter lagerbevægelserne, så lagermedarbejderne kan udføre dem.  

## <a name="to-move-items-with-the-warehouse-movement-worksheet"></a>Sådan flyttes varer med lagerbevægelseskladden
Siden **Bevægelseskladde** indeholder to funktioner, som kan være en hjælp til automatisk udfyldning af linjerne. Den første er funktionen **Beregn genopfyldning**. Denne funktion bruger placeringsniveauerne til at foreslå genopfyldning til placeringer med et højt niveau fra placeringer med et lavt niveau. Den anden er funktionen **Hent placeringsindh.**, som udfylder kladdelinjerne med hele placeringsindholdet af den eller de placeringer, du angiver.

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bevægelseskladde**, og vælg derefter det relaterede link.  
2.  Angiv lagerbevægelsesoplysninger på de relevante kladdelinjer.  
3. Vælg handlingen **Opret bevægelse** for at oprette et lagerbevægelsesdokument, som kan registreres, når lagerbevægelsen er færdig.  

### <a name="to-register-the-warehouse-movement"></a>Sådan registreres lagerbevægelsen  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bevægelser**, og vælg derefter det relaterede link.  
2.  Åbn den lagerbevægelse, du vil behandle.  
3.  På linjer af handlingstypen **Placer** skal du angive, hvor, hvilken og hvornår den pågældende vare skal flyttes ved at redigere feltet **Zonekode**, **Placeringskode**, **Håndteringsantal** eller **Forfaldsdato**.  

    Hvis lagerstedet er sat op, så placeringskoderne afspejler lagerstedets fysiske struktur, kan du hente de forskellige varer fra massevareplaceringer, der ligger lige efter hinanden, og derefter placere dem på de forreste plukplaceringer, der måske også ligger tæt på hinanden.  
4.  På linjer af handlingstypen **Hent** skal du i feltet **Håndteringsantal** angive en delmængde af det placeringsindhold, du vil flytte. Alle andre felter på linjer af handlingstypen **Hent** er skrivebeskyttede.  
5.  Hvis du vil flytte alle foreslåede mængder som anført i feltet **Antal**, skal du vælge handlingen **Autofyld håndteringsantal**.  
6. Vælg handlingen **Registrer**.  

> [!NOTE]  
>  Hvis lokationen bruger styret læg-på-lager og pluk, kan du ikke manuelt flytte varer ind eller ud af en placering af typen MODTAG, fordi varer på sådanne placeringer, skal registreres som lagt på lager, før de bliver en del af den tilgængelige lagerbeholdning.

## <a name="to-register-the-movement-of-an-item-that-has-already-occurred"></a>Sådan registreres flytning af en vare, der allerede er foregået  
Hvis lokationen bruger styret læg-på-lager og pluk, og du skal flytte varer til andre placeringer, der ikke allerede benytter læg-på-lager, pluk eller bevægelse, kan du angive den korrekte anbringelse af varerne ved hjælp af **Lageromposteringskladde**.

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lageromposteringskladde**, og vælg derefter det relaterede link.  
2.  Udfyld felterne **Varenr.**, **Fra zonekode**, **Fra placeringskode**, **Til zonekode** og **Til placeringskode**.  
3.  Vælg handlingen **Registrer**.  

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Warehouse Management](design-details-warehouse-management.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]