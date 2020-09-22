---
title: Designoplysninger – Tilgængelighed af varesporing | Microsoft Docs
description: Siderne Varesporingslinjer og Varesporingsoversigt indeholder dynamiske disponeringsoplysninger for serie- eller lotnumre. Formålet med dette er at øge gennemsigtigheden for brugere på udgående dokumenter, f.eks. salgsordrer, ved at vise dem, hvilke serienumre eller hvor mange enheder af et lotnummer, der aktuelt er tildelt på andre åbne dokumenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 9763f513f4c80247f246cd835c30335ffd0d64b2
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787592"
---
# <a name="design-details-item-tracking-availability"></a>Designoplysninger: Tilgængelighed af varesporing
Siderne **Varesporingslinjer** og **Varesporingsoversigt** indeholder dynamiske disponeringsoplysninger for serie- eller lotnumre. Formålet med dette er at øge gennemsigtigheden for brugere på udgående dokumenter, f.eks. salgsordrer, ved at vise dem, hvilke serienumre eller hvor mange enheder af et lotnummer, der aktuelt er tildelt på andre åbne dokumenter. Dette mindsker usikkerhed, der er forårsaget af dobbelt allokering, og giver ordrebehandlere tillid til, at varesporingsnumre og datoer, som de lover på ikke-bogførte salgsordre, kan opfyldes. Du kan finde flere oplysninger i [Designoplysninger: Siden Varesporingslinjer](design-details-item-tracking-lines-window.md).  

 Når du åbner siden **Varesporingslinjer**, hentes der tilgængelighedsdata fra tabellen **Varepost** og tabellen **Reservationspost** uden datofilter. Når du vælger feltet **Serienr.** eller feltet **Lotnr.**, åbnes siden **Varesporingsoversigt** og viser en oversigt over varesporingsoplysninger i tabellen **Reservationspost**. Oversigten indeholder følgende oplysninger om hvert serie- eller lotnummer på varesporingslinjen:  

|Felt|Beskrivelse|  
|---------------------------------|---------------------------------------|  
|**I alt**|Det samlede antal af serie- eller lotnumre, der aktuelt er på lager.|  
|**Ønsket antal i alt**|Det samlede antal af serie- og lotnumre, der aktuelt er anmodet om i alle dokumenter.|  
|**Aktuelt ventende antal**|Det antal, der angives i den aktuelle forekomst af siden **Varesporingslinjer**, men som endnu ikke er overført til databasen.|  
|**Beholdning i alt**|Antallet af serie- eller lotnumre, som brugeren kan anmode om.<br /><br /> Dette antal beregnes ud fra andre felter på siden på følgende måde:<br /><br /> aktuelt antal – (anmodet antal i alt + aktuelt ventende antal).|  

> [!NOTE]  
>  Du kan også se oplysningerne i den foregående tabel ved hjælp af funktionen **Marker poster** på siden **Varesporingslinjer**.  

 Hvis du vil bevare databasens ydeevne, hentes tilgængelighedsdata kun én gang fra databasen, når du åbner siden **Varesporingslinjer**, og når du bruger funktionen **Opdater disponering** på siden.  

## <a name="calculation-formula"></a>Beregningsformel  
 Som beskrevet i foregående tabel beregnes tilgængeligheden af et bestemt serienummer eller lotnummer på følgende måde.  

 beholdning i alt = antal på lager – (alle behov + antal, der endnu ikke er disponeret i databasen)  

> [!IMPORTANT]  
>  Denne formel angiver, at disponeringsberegningen for serie- eller lotnummer kun tager lagerbeholdningen i betragtning og ignorerer forventede modtagelser. Forsyning, der endnu ikke er bogført til lageret, påvirker derfor ikke tilgængelighed i forbindelse med varesporing, i modsætning til almindelig varedisponering, hvor forventede tilgange er inkluderet.  

## <a name="see-also"></a>Se også  
 [Designoplysninger: Varesporing](design-details-item-tracking.md)
