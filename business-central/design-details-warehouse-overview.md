---
title: "Designoplysninger – Oversigt over logistik | Microsoft Docs"
description: "Alle oplysninger skal spores for hver transaktion eller bevægelse på lageret for at understøtte den fysiske håndtering af varerne på zone- og placeringsniveauet. Dette administreres i tabellen **Lagerpost**. Hver transaktion gemmes i en lagerjournal."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/19/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 2d1fc180b971a7a0003847ea6b5830cc124cf5c7
ms.contentlocale: da-dk
ms.lasthandoff: 11/22/2018

---
# <a name="design-details-warehouse-overview"></a>Designoplysninger: Oversigt over logistik
Alle oplysninger skal spores for hver transaktion eller bevægelse på lageret for at understøtte den fysiske håndtering af varerne på zone- og placeringsniveauet. Dette administreres i tabellen **Lagerpost**. Hver transaktion gemmes i en lagerjournal.  

Lagerdokumenter og en lagerkladde bruges til at registrere varebevægelser på lageret. Hver gang en vare på lageret flyttes, modtages, lægges på lager, plukkes, leveres eller reguleres, registreres lagerposter for at gemme de fysiske oplysninger om zone, placering og antal.

Tabellen **Placeringsindhold** bruges til at håndtere de forskellige dimensioner af indholdet i en placering pr. vare som f.eks. måleenhed, maksimalt antal, og minimumantal. Tabellen **Placeringsindhold** indeholder også flow-felter til de lagerposter, lagerinstruktioner og lagerkladdelinjer, der sikrer, at tilgængeligheden af en vare pr. placering og en placering for en vare kan beregnes hurtigt. Du kan finde flere oplysninger i [Designoplysninger: Tilgængelighed i lageret](design-details-availability-in-the-warehouse.md).  

Når vareposteringer forekommer uden for lagermodulet, bruges der en standardreguleringsplacering pr. lokation til at synkronisere lagerposter med lagerbeholdningsposter. Under lageropgørelse registreres eventuelle forskelle mellem det beregnede og optalte antal på justeringsplaceringen og bogføres derefter som rettede vareposter. Du kan finde flere oplysninger i [Designoplysninger: Integration med lager](design-details-integration-with-inventory.md).  

Følgende illustration viser typiske lagerstrømme.  

![Oversigt over lagerprocesser](media/design_details_warehouse_management_overview.png "Oversigt over lagerprocesser")  

## <a name="basic-or-advanced-warehousing"></a>Grundlæggende eller avanceret logistik  
Lagerfunktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)] kan implementeres i forskellige kompleksitetsniveauer, afhængig af virksomhedens processer og ordrevolumen. Den væsentligste forskel er, at aktiviteter udføres ordre for ordre i basislogistik, når de er fælles for flere ordrer i avanceret logistik.  

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
For at opnå overensstemmelse med økonomiske begreber køb og salg, henviser [!INCLUDE[d365fin](includes/d365fin_md.md)]-lagerdokumentation til følgende vilkår for vareflowet på lageret.  

|Begreb|Beskrivelse|  
|----------|---------------------------------------|  
|Indgående strøm|Varer, der flyttes til lagerlokationen, som køb og indgående overflytninger.|  
|Internt forløb|Varer, der flytter inden for lagerlokationen, som produktionskomponenter og afgang.|  
|Udgående strøm|Varer, der flyttes ud af lagerlokationen, som salg og udgående overflytninger.|  

## <a name="see-also"></a>Se også  
 [Designoplysninger: Logistik](design-details-warehouse-management.md)

