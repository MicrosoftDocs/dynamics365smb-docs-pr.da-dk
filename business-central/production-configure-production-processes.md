---
title: Konfigurere produktionsprocesser | Microsoft Docs
description: "Hvis du vil konvertere materialer til fremstillede færdigvarer, skal produktionsressourcer, f.eks. styklister, ruter, maskinoperatører og maskiner, konfigureres i systemet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e167935f1bb4815093a1a9bd345da8213219ca08
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="setting-up-manufacturing"></a>Konfigurere produktion
Hvis du vil konvertere materialer til fremstillede færdigvarer, skal produktionsressourcer, f.eks. styklister, ruter, maskinoperatører og maskiner, konfigureres i systemet.

Operatører og maskiner repræsenteres i systemet af produktionsressourcer, der kan være organiseret i arbejdscentre og arbejdscentergrupper. Når disse ressourcer er etableret, kan der indlæses operationer i henhold til varens definerede materialestykliste og processtruktur (rute) og i henhold til produktionsressourcens eller arbejdscentrets kapacitet. Du kan også angive produktionskapaciteten for hver ressource. Kapaciteten defineres af den tilgængelige arbejdstid i produktionsressourcerne og arbejdscentrene, som styres af kalendere for hvert niveau. En arbejdscenterkalender angiver arbejdsdage eller -timer, skiftehold, fridage og fravær, som bestemmer arbejdscentrets disponible bruttokapacitet, som typisk måles i minutter. Alt dette bestemmes af de effektivitets- og kapacitetsværdier, der er defineret.  

Når du har defineret en produktion, kan du planlægge og udføre produktionsordrer. Du kan finde flere oplysninger i [Planlægning](production-planning.md) og [Produktion](production-manage-manufacturing.md).  

 Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Konfigurere produktionsfunktioner som f.eks. angivelse af produktionsarbejdstimer og valg af planlægningsprincipper.|Vinduet **Produktionsopsætning**.|  
|Definer en standardarbejdsuge i produktionen med hensyn til start- og sluttidspunkter for hver enkelt arbejdsdag og relaterede arbejdsskift.|[Opsætte produktionskalendere](production-how-to-create-work-center-calendars.md)|  
|Organiser faste værdier og behov for produktionsressourcer som arbejdscentre eller produktionsressourcer for at styre outputtet af den udførte produktion.|[Konfigurere arbejdscentre og produktionsressourcer](production-how-to-set-up-work-and-machine-centers.md)|
|Organiser produktionsoperationer i den rækkefølge, der kræves, og tildel dem til arbejdscentre eller produktionsressourcer med de nødvendige arbejdstider.|[Oprette ruter](production-how-to-create-routings.md)|
|Organiser produktionskomponenter eller underordnede samlinger under en overordnet vare, og godkend styklisten til afvikling i arbejdscentre.|[Oprette produktionsstyklister](production-how-to-create-production-boms.md)|
|Sørg for, at det rette komponentantal er tilgængeligt, når produktionsvarer lagerføres i én måleenhed, men produceres i en anden.|[Arbejde med produktionskladdeenheder](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)|  
|Definer familier af produktionselementer med lignende produktionsprocesser for at spare på forbruget. F.eks. kan fire stk. af den samme vare produceres fra én plade samtidig med ti stk. af en anden vare.|[Arbejde med produktionsfamilier](production-how-work-family.md)|
|Brug standardoperationer til at forenkle oprettelsen af ruter ved hurtigt at knytte ekstra oplysninger til gentagne operationer.|[Konfigurere standardrutelinjer](production-how-set-up-standard-routing-lines.md)|  
|Forbered arbejdscentre og ruter til at repræsentere underleverandørens produktionsoperationer.|[Produktion hos underleverandør](production-how-to-subcontract-manufacturing.md)|  

## <a name="see-also"></a>Se også
[Produktion](production-manage-manufacturing.md)    
[Planlægning](production-planning.md)   
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

