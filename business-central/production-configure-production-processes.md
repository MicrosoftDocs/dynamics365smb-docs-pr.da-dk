---
title: Konfigurere produktionsprocesser
description: Hvis du vil konvertere materialer til fremstillede færdigvarer, skal produktionsressourcer, f.eks. styklister, ruter, maskinoperatører og maskiner, konfigureres i systemet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 99000768, 99000779, 99000780, 99000866
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d15f1dd84a151224189a52ae73f5276ac14afbc9
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/14/2022
ms.locfileid: "7972352"
---
# <a name="setting-up-manufacturing"></a>Konfigurere produktion

Hvis du vil konvertere materialer til fremstillede færdigvarer, skal produktionsressourcer, f.eks. styklister, ruter, maskinoperatører og maskiner, konfigureres i systemet.

Operatører og maskiner repræsenteres i systemet af produktionsressourcer, der kan være organiseret i arbejdscentre og arbejdscentergrupper. Når disse ressourcer er etableret, kan der indlæses operationer i henhold til varens definerede materialestykliste og processtruktur (rute) og i henhold til produktionsressourcens eller arbejdscentrets kapacitet. Du kan også angive produktionskapaciteten for hver ressource. Kapaciteten defineres af den tilgængelige arbejdstid i produktionsressourcerne og arbejdscentrene, som styres af kalendere for hvert niveau. En arbejdscenterkalender angiver arbejdsdage eller -timer, skiftehold, fridage og fravær, som bestemmer arbejdscentrets disponible bruttokapacitet, som typisk måles i minutter. Alt dette bestemmes af de effektivitets- og kapacitetsværdier, der er defineret.  

Når du har defineret en produktion, kan du planlægge og udføre produktionsordrer. Du kan finde flere oplysninger i [Planlægning](production-planning.md) og [Produktion](production-manage-manufacturing.md).  



 Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Konfigurere produktionsfunktioner som f.eks. angivelse af produktionsarbejdstimer og valg af planlægningsparametre.|Siden **Produktionsopsætning**.|
|På fanen **Planlægning** på siden **Produktionsopsætning** skal du angive globale planlægningsparametre, der tilsidesætter parametre, som er angivet på individuelle varekort.|[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md)|
|Definer en standardarbejdsuge i produktionen med hensyn til start- og sluttidspunkter for hver enkelt arbejdsdag og relaterede arbejdsskift.|[Opsætte produktionskalendere](production-how-to-create-work-center-calendars.md)|  
|Organiser faste værdier og behov for produktionsressourcer som arbejdscentre eller produktionsressourcer for at styre outputtet af den udførte produktion.|[Konfigurere arbejdscentre og produktionsressourcer](production-how-to-set-up-work-and-machine-centers.md)|
|Organiser produktionsoperationer i den rækkefølge, der kræves, og tildel dem til arbejdscentre eller produktionsressourcer med de nødvendige arbejdstider.|[Oprette ruter](production-how-to-create-routings.md)|
|Organiser produktionskomponenter eller underordnede samlinger under en overordnet vare, og godkend styklisten til afvikling i arbejdscentre.|[Oprette produktionsstyklister](production-how-to-create-production-boms.md)|
|Sørg for, at det rette komponentantal er tilgængeligt, når produktionsvarer lagerføres i én måleenhed, men produceres i en anden.|[Arbejde med produktionskladdeenheder](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)|  
|Definer familier af produktionselementer med lignende produktionsprocesser for at spare på forbruget. F.eks. kan fire stk. af den samme vare produceres fra én plade samtidig med ti stk. af en anden vare.|[Arbejde med produktionsfamilier](production-how-work-family.md)|
|Brug standardoperationer til at forenkle oprettelsen af ruter ved hurtigt at knytte ekstra oplysninger til gentagne operationer.|[Konfigurere standardrutelinjer](production-how-set-up-standard-routing-lines.md)|  
|Forbered arbejdscentre og ruter til at repræsentere underleverandørens produktionsoperationer.|[Produktion hos underleverandør](production-how-to-subcontract-manufacturing.md)|  

## <a name="see-also"></a>Se også
[Produktions-](production-manage-manufacturing.md)
[planlægning](production-planning.md)   
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]