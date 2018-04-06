---
title: "Designoplysninger – Intervallets rolle | Microsoft Docs"
description: "Formålet med intervallet er at indsamle behovshændelser inden for tidsvinduet for at oprette en fælles forsyningsordre."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 099465f0ef7bdafa3df80c377cd83b177bb68072
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-the-role-of-the-time-bucket"></a>Designoplysninger: Intervallets rolle
Formålet med intervallet er at indsamle behovshændelser inden for tidsvinduet for at oprette en fælles forsyningsordre.  
  
 For genbestillingspolitikker, der bruger et genbestillingspunkt, kan du angive et interval. Dette sikrer, at behov inden for den samme tidsperiode er akkumuleret, før du tjekker indvirkningen på den forventede lagerbeholdning, og om genbestillingspunktet er blevet overskredet. Hvis genbestillingspunktet er overskredet, er en ny forsyningsordre planlagt fremad fra udgangen af den periode, der er defineret i intervallet. Intervaller starter på den planlagte startdato.  
  
 Begrebet interval afspejler den manuelle proces til hyppig kontrol af lagerniveauet i stedet for hver transaktion. Brugeren skal definere frekvensen (intervallet). Brugeren samler f.eks. alle varebehov fra en kreditor for at foretage en ugentlig bestilling.  
  
 ![](media/nav_app_supply_planning_2_reorder_cycle.png "NAV_APP_supply_planning_2_reorder_cycle")  
  
 Intervallet bruges normalt til at undgå en overlapningseffekt. For eksempel en afstemt række af behov og forsyning, hvor et tidligt behov annulleres, eller et ny oprettes. Resultatet ville være, at hver forsyningsordre (undtagen den sidste) skal omplanlægges.  
  
## <a name="see-also"></a>Se også  
 [Designoplysninger: Genbestillingsmetoder](design-details-reordering-policies.md)   
 [Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md)   
 [Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md)   
 [Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)
