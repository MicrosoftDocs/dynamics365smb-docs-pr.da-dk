---
title: Designoplysninger – Oversigt over logistik | Microsoft Docs
description: Alle oplysninger skal spores for hver transaktion eller bevægelse på lageret for at understøtte den fysiske håndtering af varerne på zone- og placeringsniveauet. Dette administreres i tabellen **Lagerpost**. Hver transaktion gemmes i en lagerjournal.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8842bd23f6d2d470599afe9b4382b35cec3d9251
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749539"
---
# <a name="design-details-warehouse-overview"></a>Designoplysninger: Oversigt over logistik
Alle oplysninger skal spores for hver transaktion eller bevægelse på lageret for at understøtte den fysiske håndtering af varerne på zone- og placeringsniveauet. Dette administreres i tabellen **Lagerpost**. Hver transaktion gemmes i en lagerjournal.  

Lagerdokumenter og en lagerkladde bruges til at registrere varebevægelser på lageret. Hver gang en vare på lageret flyttes, modtages, lægges på lager, plukkes, leveres eller reguleres, registreres lagerposter for at gemme de fysiske oplysninger om zone, placering og antal.

Tabellen **Placeringsindhold** bruges til at håndtere de forskellige dimensioner af indholdet i en placering pr. vare som f.eks. måleenhed, maksimalt antal, og minimumantal. Tabellen **Placeringsindhold** indeholder også flow-felter til de lagerposter, lagerinstruktioner og lagerkladdelinjer, der sikrer, at tilgængeligheden af en vare pr. placering og en placering for en vare kan beregnes hurtigt. Du kan finde flere oplysninger i [Designoplysninger: Tilgængelighed i lageret](design-details-availability-in-the-warehouse.md).  

Når vareposteringer forekommer uden for lagermodulet, bruges der en standardreguleringsplacering pr. lokation til at synkronisere lagerposter med lagerbeholdningsposter. Under lageropgørelse registreres eventuelle forskelle mellem det beregnede og optalte antal på justeringsplaceringen og bogføres derefter som rettede vareposter. Du kan finde flere oplysninger i [Designoplysninger: Integration med lager](design-details-integration-with-inventory.md).  

Følgende illustration viser typiske lagerstrømme.  

![Oversigt over lagerstedsprocesser](media/design_details_warehouse_management_overview.png "Oversigt over lagerstedsprocesser")  

## <a name="basic-or-advanced-warehousing"></a>Grundlæggende eller avanceret logistik  
Lagerfunktioner i [!INCLUDE[prod_short](includes/prod_short.md)] kan implementeres i forskellige kompleksitetsniveauer, afhængig af virksomhedens processer og ordrevolumen. Den væsentligste forskel er, at aktiviteter udføres ordre for ordre i basislogistik, når de er fælles for flere ordrer i avanceret logistik.  

 Med henblik på at skelne mellem de forskellige kompleksitetsniveauer refererer denne dokumentation til to almindelige betegnelser, Grundlæggende og Avanceret logistik. Denne simple differentiering dækker flere forskellige kompleksitetsniveauer, som defineret af produktdetaljer og lokationsopsætning, hver understøttet af forskellige brugergrænsefladedokumenter. Du kan finde flere oplysninger i [Designoplysninger: Opsætning af lager](design-details-warehouse-setup.md)  

> [!NOTE]  
>  Det mest avancerede niveau for logistik kaldes "logistikinstallationer" i denne dokumentation, da dette niveau kræver det mest avancerede modul, Logistik.  

 Følgende forskellige UI-dokumenter, der bruges i grundlæggende og avanceret logistik.  

## <a name="basic-ui-documents"></a>Grundlæggende brugergrænsefladedokumenter  

-   **Læg-på-lager**  
-   **Pluk**  
-   **Flytning (lager)**  
-   **Varekladde**  
-   **Vareomposteringskladde**  
-   (Forskellige rapporter)  

## <a name="advanced-ui-documents"></a>Avancerede brugergrænsefladedokumenter  

-   **Lagermodtagelse**  
-   **Læg-på-lager-kladde**  
-   **Læg-på-lager (logistik)**  
-   **Plukkladde**  
-   **Pluk (logistik)**  
-   **Bevægelseskladde**  
-   **Bevægelse (logistik)**  
-   **Internt lagerpluk**  
-   **Intern læg-på-lager-aktivitet**  
-   **Placeringsopr.kladde**  
-   **Opr.kladde til placeringsindh.**  
-   **Lagerkladde**  
-   **Lagervareomposteringskladde**  
-   (Forskellige rapporter)  

Hvis du ønsker yderligere oplysninger om de enkelte dokumenter, kan du se de respektive emner.  

### <a name="terminology"></a>Terminologi  
For at opnå overensstemmelse med økonomiske begreber køb og salg, henviser [!INCLUDE[prod_short](includes/prod_short.md)]-lagerdokumentation til følgende vilkår for vareflowet på lageret.  

|Begreb|Beskrivelse|  
|----------|---------------------------------------|  
|Indgående strøm|Varer, der flyttes til lagerlokationen, som køb og indgående overflytninger.|  
|Internt forløb|Varer, der flytter inden for lagerlokationen, som produktionskomponenter og afgang.|  
|Udgående strøm|Varer, der flyttes ud af lagerlokationen, som salg og udgående overflytninger.|  

## <a name="see-also"></a>Se også  
 [Designoplysninger: Logistik](design-details-warehouse-management.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]