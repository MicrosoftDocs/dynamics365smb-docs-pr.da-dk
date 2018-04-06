---
title: "Designoplysninger – Håndtering af ordrer før planlægningsstartdatoen | Microsoft Docs"
description: "Dette emne beskriver de regler, planlægningen anvender for ordrer i den frosne zone."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: planning, frozen, design serial, lot
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5545fe1c2c8833eb1c97765f261777cbb1781098
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-dealing-with-orders-before-the-planning-starting-date"></a>Designoplysninger: Håndtering af ordrer før planlægningsstartdatoen
For at undgå, at en forsyningsplan viser umulige og derfor ubrugelige forslag, anser planlægningssystemet perioden indtil den planlagte startdato for en frossen zone, hvor intet er planlagt. Følgende regel gælder for den frosne zone:  
  
Alle forsyninger og behov før startdatoen for planlægningsperioden vil blive betragtet som en del af lagerbeholdningen eller leveret.  
  
Derfor vil planlægningssystemet ikke, med nogle få undtagelser, foreslå ændringer til forsyningsordrer i den frosne zone, og der oprettes eller vedligeholdes ingen ordresporingslinks for den pågældende periode.  
  
Undtagelser til denne regel er som følger:  
  
* Hvis den forventede disponible beholdning, herunder summen af forsyning og behov i den frosne zone, er under nul.  
* Hvis der kræves serienumre/lotnumre på den eller de tilbagedaterede ordrer.  
* Hvis forsyning-behov-sæt er sammenkædet af en ordre-til-ordre-politik.  
  
Hvis den første disponible lagerbeholdning er under nul, foreslås der en nødforsyningsordre dagen før planlægningsperioden til at dække den manglende mængde. Derfor vil den forventede og disponible lagerbeholdning altid være mindst nul, når planlægningen for den fremtidige periode begynder. Planlægningslinjen for denne forsyningsordre viser et Nødsituation-advarselsikon, og yderligere oplysninger kan findes ved opslag.  
  
## <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a>Serienumre/lotnumre og ordre-til-ordre-links er fritaget fra den frosne zone  
Hvis serienumre/lotnumre er nødvendige eller findes i en ordre-til-ordre-link, vil planlægningssystemet se bort fra den frosne zone og indarbejde disse mængder, der er dateret tilbage fra startdatoen, og potentielt foreslå korrigerende handlinger, hvis behov og forsyning ikke er synkroniseret. Forretningsårsagen til dette princip er, at sådanne specifikke behov-forsyningssæt skal stemme overens for at sikre, at dette specifikke behov er opfyldt.  
  
## <a name="see-also"></a>Se også  
[Designoplysninger: Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md)   
[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)
