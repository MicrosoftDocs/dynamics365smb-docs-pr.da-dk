---
title: Designoplysninger – Prioritering af ordrer | Microsoft Docs
description: Yderligere oplysninger om, hvordan der skal prioriteres for at opfylde både behov og forsyningskrav.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, priority, prioritize, order, sku, demand, supply
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: 06eb5221369d8777330ae844adfb5d87658d591d
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "924206"
---
# <a name="design-details-prioritizing-orders"></a>Designoplysninger: Prioritering af ordrer
Inden for en given SKU repræsenterer den anmodede eller tilgængelige dato den højeste prioritet. Behovene i dag skal behandles før behovene for næste uge. Men ud over denne overordnede prioritet foreslår planlægningssystemet også, hvilken type behov der skal være opfyldt, inden andre behov opfyldes. Det foreslås ligeledes, hvilken forsyningskilde der skal anvendes, før du anvender andre forsyningskilder. Dette udføres i overensstemmelse med ordreprioriteter.  

Indlæst behov og forsyning, der bidrager til en profil for den planlagte lagerbeholdning i henhold til følgende prioriteter:  

## <a name="priorities-on-the-demand-side"></a>Prioriteter på efterspørgselssiden  
1. Allerede leveret: varepost  
2. Købsreturvareordre  
3. Salgsordre  
4. Serviceordre  
5. Produktionskomponentbehov  
6. Montageordrelinje  
7. Udgående overflytningsordre  
8. Rammeordre (der ikke allerede er brugt af relaterede salgsordrer)  
9. Forecast (der ikke allerede er anvendt af andre salgsordrer)  

> [!NOTE]  
>  Købsreturvarer er normalt ikke involveret i forsyningsplanlægning. De skal altid være reserveret fra det lot, der skal returneres. Hvis den ikke er reserveret, spiller købsreturvarer en rolle i udbuddet og er højt prioriteret for at undgå, at planlægningssystemet foreslår en forsyningsordre, der blot skal tjene et købsreturnering.  

## <a name="priorities-on-the-supply-side"></a>Prioriteter på forsyningssiden  
1. Allerede på lager: Varepost (planlægningsfleksibilitet = ingen)  
2. Salgsreturvareordre (planlægningsfleksibilitet = ingen)  
3. Indgående overflytningsordre  
4. Produktionsordre  
5. Montageordre  
6. Købsordre  

## <a name="priority-related-to-the-state-of-demand-and-supply"></a>Prioritet, der er relateret til tilstand af efterspørgsel og udbud  
Bortset fra de prioriteter, der er angivet af typen af behov og forsyning, definerer den nuværende ordrestatus i udførelsesprocessen også en prioritet. Lageraktiviteter har f.eks. indflydelse, og status for salg, køb, overførsel, montage og produktionsordrer tages i betragtning:  

1. Delvist håndteres (planlægningsfleksibilitet = ingen)  
2. Allerede under behandling i lageret (planlægningsfleksibilitet = ingen)  
3. Frigivet – alle ordretyper (planlægningsfleksibilitet = ubegrænset)  
4. Fastlagt og planlagt produktionsordre (planlægningsfleksibilitet = ubegrænset)  
5. Planlagt/åben – alle ordretyper (planlægningsfleksibilitet = ubegrænset)  

## <a name="see-also"></a>Se også  
[Designoplysninger: Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md)   
[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)
