---
title: "Designoplysninger – Lot-for-Lot | Microsoft Docs"
description: "Få at vide, hvordan du bruger lot-for-lot-politikken til at udligne ordreantal på baggrund af behov."
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
ms.openlocfilehash: 2e0d1d18685f3395c31071ca9a2495c0091c564d
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-lot-for-lot"></a>Designoplysninger: Lot-for-lot
Lot-for-lot-politik er den mest fleksible, fordi systemet kun reagerer på det faktiske behov, plus det fungerer på forventet behov fra forecast og rammeordrer og udligner derefter ordreantallet på baggrund af behovet. Lot-for-lot-politik tager sigte på A - og B-varer, hvor lageret kan accepteres, men bør undgås.  
  
På nogle måder ser lot-for-lot politik ud som ordrepolitikken, men der er en generisk tilgang til varer: Den kan acceptere antal på lager, og den kombinerer behov og tilsvarende forsyning i intervaller, der er defineret af brugeren.  
  
Intervallet er defineret i feltet **Interval**. Systemet fungerer med et mindste interval på én dag, da det er den mindste tidsenhed på behovs- og forsyningshændelser i systemet (selvom tidsenheden på produktionsordrer og komponentbehov i praksis kan være sekunder).  
  
Intervallet angiver også grænser for, hvornår en eksisterende forsyningsordre bør omplanlægges for at opfylde et bestemt behov. Hvis forsyningen ligger i intervallet, bliver den flyttet ind eller ud for at opfylde behovet. Hvis den ligger tidligere, vil det medføre unødvendig ophobning af lageret og skal annulleres. Hvis den ligger senere, oprettes en ny forsyningsordre i stedet.  
  
Med denne politik er det også muligt at definere et sikkerhedslager for at kompensere for mulige udsving i udbud eller for at imødekomme pludselige behov.  
  
Da forsyningsordreantallet er baseret på det faktiske behov, kan det være smart at bruge ordremodifikatorer: Rund ordreantallet op, så det passer med en specifik oprundingsfaktor (eller købsenhedskoden), forøg ordren til et fastsat minimumsordreantal, eller reducer antallet til det angivne maksimale antal (og opret derefter to eller flere forsyninger for at nå det nødvendige samlede antal).  
  
## <a name="see-also"></a>Se også  
[Designoplysninger: Genbestillingsmetoder](design-details-reordering-policies.md)   
[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md)   
[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md)   
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)
