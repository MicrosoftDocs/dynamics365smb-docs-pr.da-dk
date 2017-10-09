---
title: "Designoplysninger – Lukning af behov og forsyning | Microsoft Docs"
description: "Dette emne indeholder et forslag til, hvad der skal gøres, når du udfører forsyningsudlignende procedurer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, planning, example, closing, supply
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0796865fa5b04630cc3ac68a63cc8113664a2d24
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-closing-demand-and-supply"></a>Designoplysninger: Lukning af behov og forsyning
Når de forsyningsudlignende procedurer er blevet udført, er der tre mulige slutsituationer:  
  
* Det påkrævede antal og den påkrævede dato for behovhændelserne er opfyldt, og planlægning af dem kan lukkes. Forsyningshændelsen er stadig åben og kan dække det næste behov, så udligningsproceduren kan starte forfra med den aktuelle forsyningshændelse og det næste behov.  
* Forsyningsordren kan ikke ændres, så den dækker alle behov. Behovshændelsen er stadig åben, med nogle udækkede antal, der kan dækkes ved næste forsyningshændelse. Derfor lukkes den aktuelle forsyning, så den udlignende handling kan starte forfra med det aktuelle behov og den næste forsyningshændelse.  
* Alle behov er blevet dækket: Der er ingen efterfølgende behov (eller der har ikke været nogen behov overhovedet). Hvis der er en eventuel overskydende forsyning, kan den reduceres (eller annulleres) og derefter lukkes. Det er muligt, at der findes yderligere forsyningshændelser i kæden, og de bør også annulleres.  
  
Endelig opretter planlægningssystemet et ordresporingslink mellem forsyning og behov.  
  
## <a name="creating-the-planning-line-suggested-action"></a>Oprettelse af planlægningslinjen (foreslået aktivitet)  
Hvis en handling – Ny, Ret antal, Omplanlæg, Omplanlæg og ret antal eller Annuller – foreslås for at revidere forsyningsordren, vil planlægningssystemet oprette en planlægningslinje i planlægningskladden. På grund af ordresporing oprettes planlægningslinjen ikke kun, når forsyningshændelsen er lukket, men også hvis behovhændelsen er lukket, selvom forsyningshændelsen stadig er åben og kan være underlagt yderligere ændringer, når næste behovshændelse behandles. Det betyder, at når planlægningslinjen er oprettet, kan den ændres igen.  
  
Planlægningslinjen kan vedligeholdes i tre niveauer for at minimere databaseadgang, når der håndteres produktionsordrer, mens det tilstræbes at udføre det mindst krævende vedligeholdelsesniveau:  
  
* Opret kun planlægningslinjen med den aktuelle forfaldsdato og antallet, men uden rute og komponenter.  
* Omfatter rute: Den planlagte rute er opstillet med beregning af start- og slutdatoer og -tidspunkter. Dette er påkrævet i forbindelse med adgang til databasen. For at bestemme slutdato og forfaldsdatoer kan det være nødvendigt at beregne dette, selvom forsyningshændelsen ikke er blevet lukket (i tilfælde af fremadrettet planlægning).  
* Omfatter styklisteudfoldelsen: Dette kan vente indtil lige før leveringshændelsen er lukket.  
  
Dette afslutter beskrivelserne af, hvordan behov og forsyning indlæses, prioriteres og afstemmes af planlægningssystemet. I integration med denne planlægningsaktivitet af forsyning skal systemet sikre, at det nødvendige lagerniveau for hver planlagt vare opretholdes i overensstemmelse med dens genbestillingsmetoder.  
  
## <a name="see-also"></a>Se også  
[Designoplysninger: Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md)   
[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)
