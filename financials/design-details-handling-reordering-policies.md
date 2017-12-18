---
title: "Designoplysninger – Håndtering af genbestillingsmetoder | Microsoft Docs"
description: "Oversigt over opgaver til at definere en genbestillingsmetode i forsyningsplanlægning."
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
ms.openlocfilehash: 2a6658508f8e12a11989d54da6d6c8e3a36631cc
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-handling-reordering-policies"></a>Designoplysninger: Håndtering af genbestillingsmetoder
En genbestillingsmetode skal defineres for, at en vare kan være en del af forsyningsplanlægning. Der findes følgende fire genbestillingsmetoder:  
  
* Fast genbestil.antal  
* Maks. antal  
* Ordre  
* Lot-for-Lot  
  
Fast genbestil.antal- og Maks. antal-metoder, der er relateret til lagerplanlægning. Selvom lagerplanlægning er teknisk enklere end udligningsproceduren, skal disse politikker fungere sammen med den trinvise afstemning af forsyning og ordresporing. For at styre integrationen mellem de to og for at give indsigt i den involverede planlægningslogik styrer strenge principper, hvordan genbestillingsmetoder håndteres.  
  
## <a name="in-this-section"></a>Dette afsnit indeholder  
[Designoplysninger: Genbestillingspunktets rolle](design-details-the-role-of-the-reorder-point.md)  
[Designoplysninger: Overvågning af det forventede lagerniveau og genbestillingspunktet](design-details-monitoring-the-projected-inventory-level-and-the-reorder-point.md)  
[Designoplysninger: Intervallets rolle](design-details-the-role-of-the-time-bucket.md)  
[Designoplysninger: Forblive under overløbsniveauet](design-details-staying-under-the-overflow-level.md)  
[Designoplysninger: Håndtering af forventet negativt lager](design-details-handling-projected-negative-inventory.md)  
[Designoplysninger: Genbestillingsmetoder](design-details-reordering-policies.md)  
  
## <a name="see-also"></a>Se også  
[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md)   
[Designoplysninger: Tabellen Planlægningsopgave](design-details-planning-assignment-table.md)   
[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designoplysninger: Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md)   
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)
