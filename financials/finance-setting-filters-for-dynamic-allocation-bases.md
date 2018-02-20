---
title: Indstilling af filtre for dynamiske fordelingsbaser | Microsoft Docs
description: "Metoden til dynamisk fordeling er baseret på værdier, der kan ændres. For eksempel antal medarbejdere et omkostningssted eller antal solgte varer for et omkostningsobjekt i en bestemt tidsperiode. Der findes ni foruddefinerede fordelingsbaser og tolv dynamiske datointervaller. Du kan angive forskellige filtre, der er baseret på allokeringsbasen."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: cd6aaf4ca0c1de1cea400ce5abe434f7c37040f9
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="setting-filters-for-dynamic-allocation-bases"></a>Indstilling af filtre for dynamiske allokeringsbaser
Metoden til dynamisk fordeling er baseret på værdier, der kan ændres. For eksempel antal medarbejdere et omkostningssted eller antal solgte varer for et omkostningsobjekt i en bestemt tidsperiode. Der findes ni foruddefinerede fordelingsbaser og tolv dynamiske datointervaller. Du kan angive forskellige filtre, der er baseret på allokeringsbasen.  

## <a name="setting-filters-for-dynamic-allocation-bases"></a>Indstilling af filtre for dynamiske allokeringsbaser  
 Følgende tabel viser, hvilke filtre der er mulige for forskellige tildelingsbaser, og hvilke værdier der er gyldige i felterne **Nummerfilter** og **Gruppefilter**. Tryk på F1 i feltet **Datofilterkode** for at læse detaljerede beskrivelser.  

|**Basis**|**Nummerfilter**|**Datofilterkode**|**Omkostningsstedsfilter**|**Omkostningsemnefilter**|**Gruppefilter**|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|Finansposter|Finanskonto|Ja|Ja|Ja|I/R|  
|Finansbudgetposter|Finanskonto|Ja|Ja|Ja|Finansbudgetnavn|  
|Pristypeposter|Pristype|Ja|Ja|Ja|I/R|  
|Omkostningsbudgetposter|Pristype|Ja|Ja|Ja|Budgetnavn|  
|Antal ansatte|I/R|Ja|Ja|Ja|I/R|  
|Varer solgt (antal)|Varenr.|Ja|Ja|Ja|Varebogføringsgruppe|  
|Varer købt (antal)|Varenr.|Ja|Ja|Ja|Varebogføringsgruppe|  
|Varer solgt (beløb)|Varenr.|Ja|Ja|Ja|Varebogføringsgruppe|  
|Varer købt (beløb)|Varenr.|Ja|Ja|Ja|Varebogføringsgruppe|  

## <a name="see-also"></a>Se også  
 [Scenarieeksempel: Definition af dynamiske fordelinger baseret på solgte varer](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)   
 [Konfigurere fordelingskilde og mål](finance-how-to-set-up-allocation-source-and-targets.md)   
 [Definere og allokere omkostninger](finance-define-and-allocate-costs.md)

