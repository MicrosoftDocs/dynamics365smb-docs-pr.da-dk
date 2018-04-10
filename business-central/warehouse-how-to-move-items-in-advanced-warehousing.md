---
title: "Sådan flyttes varer ad hoc i avancerede lageropsætninger | Microsoft Docs"
description: "I avancerede lageropsætninger, dvs. lokationer med styret læg-på-lager og pluk, udføres lagerbevægelser fra én placering til en anden af en overordnet medarbejder, der forbereder lagerbevægelserne i bevægelseskladden og derefter opretter lagerbevægelserne, så lagermedarbejderne kan udføre dem."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: bcfe657407f4060e9f3ce12b8a87e4ff65e3bf79
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="move-items-in-advanced-warehouse-configurations"></a>Flytte varer i avancerede lageropsætninger
I avancerede lageropsætninger, dvs. lokationer med styret læg-på-lager og pluk, udføres lagerbevægelser fra én placering til en anden af en overordnet medarbejder, der forbereder lagerbevægelserne i bevægelseskladden og derefter opretter lagerbevægelserne, så lagermedarbejderne kan udføre dem.  

## <a name="to-move-items-with-the-warehouse-movement-worksheet"></a>Sådan flyttes varer med lagerbevægelseskladden
Vinduet **Bevægelseskladde** indeholder to funktioner, som kan være en hjælp til automatisk udfyldning af linjerne. Den første er funktionen **Beregn genopfyldning**. Denne funktion bruger placeringsniveauerne til at foreslå genopfyldning til placeringer med et højt niveau fra placeringer med et lavt niveau. Den anden er funktionen **Hent placeringsindh.**, som udfylder kladdelinjerne med hele placeringsindholdet af den eller de placeringer, du angiver.

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bevægelseskladde**, og vælg derefter det relaterede link.  
2.  Angiv lagerbevægelsesoplysninger på de relevante kladdelinjer.  
3. Vælg handlingen **Opret bevægelse** for at oprette et lagerbevægelsesdokument, som kan registreres, når lagerbevægelsen er færdig.  

### <a name="to-register-the-warehouse-movement"></a>Sådan registreres lagerbevægelsen  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bevægelser**, og vælg derefter det relaterede link.  
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

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lageromposteringskladde**, og vælg derefter det relaterede link.  
2.  Udfyld felterne **Varenr.**, **Fra zonekode**, **Fra placeringskode**, **Til zonekode** og **Til placeringskode**.  
3.  Vælg handlingen **Registrer**.  

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

