---
title: Sådan flyttes varer ad hoc i grundlæggende lageropsætninger | Microsoft Docs
description: Du kan undertiden have brug for at flytte varer mellem interne placeringer ikke modtagelse eller leveranceplacering uden et bestemt krav fra et kildedokument. Du kan udføre disse ad hoc-bevægelser, for eksempel for at omstrukturere lageret, for at bringe elementer til et inspektionsområde eller for at flytte flere elementer til og fra et produktionsområde uden en systemrelation til produktionsordrens kildedokument.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: b3760be8694f8c65ae07abaea9234a5dd524bb47
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "913103"
---
# <a name="move-items-ad-hoc-in-basic-warehouse-configurations"></a>Flytte varer ad hoc i grundlæggende lageropsætninger
Du kan undertiden have brug for at flytte varer mellem interne placeringer ikke modtagelse eller leveranceplacering uden et bestemt krav fra et kildedokument. Du kan udføre disse ad hoc-bevægelser, for eksempel for at omstrukturere lageret, for at bringe elementer til et inspektionsområde eller for at flytte flere elementer til og fra et produktionsområde uden en systemrelation til produktionsordrens kildedokument.  

I grundlæggende lageropsætninger, dvs. lokationer, der bruger opsætningsfeltet **Tvungen placering** og eventuelt opsætningsfelterne **Kræv pluk** og **Kræv læg-på-lager**, kan du registrere ad hoc-bevægelser uden kildedokumenter på følgende måder:  

- På siden **Intern flytning**.  
- Med siden **Vareomposteringskladde**.  

> [!NOTE]  
>  I avancerede lageropsætninger, dvs. lokationer, der bruger opsætningsfeltet **Styret læg-på-lager og pluk**, bruges siden **Bevægelseskladde** eller **Internt lagerpluk** eller **Internt læg-på-lager** til ad hoc-flytning af varer mellem placeringer.  

## <a name="to-move-items-as-an-internal-movement"></a>Sådan flyttes varer som en intern overførsel  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Intern flytning**, og vælg derefter det relaterede link.  
2.  Udfyld feltet **Nummer** i oversigtspanelet **Generelt**. enten ved at lade værdien i feltet være eller ved at vælge knappen **AssistEdit** for at vælge fra nummerserien.  
3.  I feltet **Lokationskode** skal du indtaste den lokation, hvor flytningen finder sted.  

    Hvis lokationen er angivet som din standardlokation som lagermedarbejder, indsættes lokationskoden automatisk.  
4.  I feltet **Til placeringskode** skal du indtaste en kode for den placering, du vil flytte elementet til. Til produktionsformål kunne dette f.eks. være koden for den åbne produktionsplacering som defineret på lokationskort eller i arbejdscenteret.  
5.  I feltet **Forfaldsdato** skal du indtaste den dato, som bevægelsen skal være udført inden.  
6.  På oversigtspanelet **Linjer** skal du vælge feltet **Varenr.** for at åbne siden **Placeringsindh.oversigt** og vælge den vare, der skal flyttes baseret på dens tilgængelighed på placeringerne. Alternativt kan du vælge handlingen **Hent placeringsindh.** for at udfylde de interne overflytningslinjer på grundlag af dine filtre. Du kan finde flere oplysninger i værktøjstip til handlingen **Hent placeringsindh**.   

    Når du har markeret elementet, udfyldes feltet **Fra placeringskode** automatisk i henhold til det valgte placeringsindhold, men du kan ændre det til en anden placering, hvor varen er tilgængelig.  

    > [!NOTE]  
    >  Da felterne **Varenr.** og **Fra placeringskode** er forbundet, kan deres værdier ændres i forhold til hinanden, når du redigerer et af felterne.  

    Feltet **Til placeringskode** udfyldes med den værdi, du har angivet i hovedet, men du kan ændre den på linjen til anden placeringskode, der ikke er blokeret eller dedikeret til særlige formål. Du kan finde flere oplysninger om oprettelse af dedikerede placeringer i Dedikeret.  
7.  Når du har defineret, hvilke placeringer du vil flytte elementet fra og til, skal du angive det antal, der skal flyttes, i feltet **Antal**.  

    > [!NOTE]  
    >  Antallet skal være tilgængelig i Fra placeringskode.  

8.  Når du er klar til at behandle den interne overførsel, skal du vælge handlingen **Opret flytning (lager)**.  

    > [!NOTE]  
    >  Når du har oprettet lagerflytningen, slettes de interne overførselslinjer.  

    Du udfører resten af ad hoc-bevægelsen på siden **Flytning (lager)** på samme måde som i en bevægelse, der er baseret på kildedokumenter. Du kan finde flere oplysninger i f.eks. [Flytte komponenter til et handlingsområde i grundlæggende lageropsætninger](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  

## <a name="to-move-items-with-the-item-reclassification-journal"></a>Sådan flyttes varer i vareomposteringskladden
I stedet for at bruge lagerbevægelsesdokument kan du registrere flytningen af varer ved at ompostere deres placeringskoder. Du kan finde flere oplysninger i [Tælle, justere og ompostere inventar ved hjælp af kladder](inventory-how-count-adjust-reclassify.md).   
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Vareomposteringskladde**, og vælg derefter det relaterede link.  
2.  På hver kladdelinje skal du definere placeringer, og som du vil flytte elementer til og fra, ved at udfylde felterne **Placeringskode** og **Ny placeringskode**.  

    1.  Hvis du vil flytte hele indholdet i en placering til en anden placering, skal du klikke på handlingen og vælge handlingen **Hent placeringsindh.**.  
    2.  Udfyld filtrene for at finde den placering, hvis indhold du vil flytte, og klik derefter på knappen **OK**. Kladdelinjerne udfyldes med indholdet af placeringen.  
3.  Udfyld resten af felterne på de enkelte kladdelinjer.   
4.  Bogfør omposteringskladden.  

    > [!NOTE]  
    >  I modsætning til transportdokumenter opretter en bevægelse, der er bogført i omposteringskladden, ikke en lageranmodning for at udføre den fysiske opgave.  

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
