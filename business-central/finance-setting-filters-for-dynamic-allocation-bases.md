---
title: Indstilling af filtre for dynamiske fordelingsbaser | Microsoft Docs
description: Metoden til dynamisk fordeling er baseret på værdier, der kan ændres. For eksempel antal medarbejdere et omkostningssted eller antal solgte varer for et omkostningsobjekt i en bestemt tidsperiode. Der findes ni foruddefinerede fordelingsbaser og tolv dynamiske datointervaller. Du kan angive forskellige filtre, der er baseret på allokeringsbasen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: fcf97328900bb21a85be51452b9e86da8398d195
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "793340"
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
[Definere og allokere omkostninger](finance-define-and-allocate-costs.md)
