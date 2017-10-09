---
title: "Designoplysninger – Tilgængelighed af varesporing | Microsoft Docs"
description: "Vinduerne **Varesporingslinjer** og **Varesporingsoversigt** indeholder dynamiske disponeringsoplysninger for serie- eller lotnumre. Formålet med dette er at øge gennemsigtigheden for brugere på udgående dokumenter, f.eks. salgsordrer, ved at vise dem, hvilke serienumre eller hvor mange enheder af et lotnummer, der aktuelt er tildelt på andre åbne dokumenter. Dette mindsker usikkerhed, der er forårsaget af dobbelt allokering, og giver ordrebehandlere tillid til, at varesporingsnumre og datoer, som de lover på ikke-bogførte salgsordre, kan opfyldes."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: cacedb1252133c5370e13fda36e984a784217e51
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-item-tracking-availability"></a>Designoplysninger: Tilgængelighed af varesporing
Vinduerne **Varesporingslinjer** og **Varesporingsoversigt** indeholder dynamiske disponeringsoplysninger for serie- eller lotnumre. Formålet med dette er at øge gennemsigtigheden for brugere på udgående dokumenter, f.eks. salgsordrer, ved at vise dem, hvilke serienumre eller hvor mange enheder af et lotnummer, der aktuelt er tildelt på andre åbne dokumenter. Dette mindsker usikkerhed, der er forårsaget af dobbelt allokering, og giver ordrebehandlere tillid til, at varesporingsnumre og datoer, som de lover på ikke-bogførte salgsordre, kan opfyldes. Du kan finde flere oplysninger i [Designoplysninger: Vinduet Varesporingslinjer](design-details-item-tracking-lines-window.md).  

 Når du åbner vinduet **Varesporingslinjer**, hentes der tilgængelighedsdata fra tabellen **Varepost** og tabellen **Reservationspost** uden datofilter. Når du vælger feltet **Serienr.** eller feltet **Lotnr.**, åbnes vinduet **Varesporingsoversigt** og viser en oversigt over varesporingsoplysninger i tabellen **Reservationspost**. Oversigten indeholder følgende oplysninger om hvert serie- eller lotnummer på varesporingslinjen:  

|Felt|Description|  
|---------------------------------|---------------------------------------|  
|**I alt**|Det samlede antal af serie- eller lotnumre, der aktuelt er på lager.|  
|**Ønsket antal i alt**|Det samlede antal af serie- og lotnumre, der aktuelt er anmodet om i alle dokumenter.|  
|**Aktuelt ventende antal**|Det antal, der angives i den aktuelle forekomst af vinduet **Varesporingslinjer**, men som endnu ikke er overført til databasen.|  
|**Beholdning i alt**|Antallet af serie- eller lotnumre, som brugeren kan anmode om.<br /><br /> Dette antal beregnes ud fra andre felter i vinduet på følgende måde:<br /><br /> aktuelt antal – (anmodet antal i alt + aktuelt ventende antal).|  

> [!NOTE]  
>  Du kan også se oplysningerne i den foregående tabel ved hjælp af funktionen **Marker poster** i vinduet **Varesporingslinjer**.  

 Hvis du vil bevare databasens ydeevne, hentes tilgængelighedsdata kun én gang fra databasen, når du åbner vinduet **Varesporingslinjer** og bruger funktionen **Opdater disponering**.  

## <a name="calculation-formula"></a>Beregningsformel  
 Som beskrevet i foregående tabel beregnes tilgængeligheden af et bestemt serienummer eller lotnummer på følgende måde.  

 beholdning i alt = antal på lager – (alle behov + antal, der endnu ikke er disponeret i databasen)  

> [!IMPORTANT]  
>  Denne formel angiver, at disponeringsberegningen for serie- eller lotnummer kun tager lagerbeholdningen i betragtning og ignorerer forventede modtagelser. Forsyning, der endnu ikke er bogført til lageret, påvirker derfor ikke tilgængelighed i forbindelse med varesporing, i modsætning til almindelig varedisponering, hvor forventede tilgange er inkluderet.  

## <a name="see-also"></a>Se også  
 [Designoplysninger: Varesporing](design-details-item-tracking.md)

