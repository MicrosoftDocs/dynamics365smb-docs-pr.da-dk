---
title: Håndtere lager- og produktionsomkostninger | Microsoft Docs
description: Selvom meget af funktionaliteten i omkostningsberegningen er udtrykt i underliggende processer, der ikke kræver brugermedvirken, f.eks. efterudligning og automatisk kostregulering, er en række felter, sider og rapporter beregnet til brugere, som direkte eller indirekte styrer varepriser eller drift.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 1f858457bcf667d158642fe42f3ea85e668adff3
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306360"
---
# <a name="handling-inventory-and-manufacturing-costs"></a>Håndtere lager- og produktionsomkostninger
Selvom meget af funktionaliteten i omkostningsberegningen er udtrykt i underliggende processer, der ikke kræver brugermedvirken, f.eks. efterudligning og automatisk kostregulering, er en række felter, sider og rapporter beregnet til brugere, som direkte eller indirekte styrer varepriser eller drift.  

 Tildeling af varegebyrer til købsdokumenter er et eksempel på en opgave til indirekte omkostningsberegning. Opdatering af kostprisen for montage eller produktionsstyklistevare er et eksempel på en opgave til en mere direkte omkostningsberegning.  

 Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Opdatere købsprisen for en eller flere varer - periodisk eller automatisk - for at videresende eventuelle kostprisændringer fra indgående poster, f.eks. posterne for køb eller produktionsoutput, til de relaterede udgående poster, f.eks. forbrug eller overførsler.|[Regulere varepriser](inventory-how-adjust-item-costs.md)|  
|Få indsigt i dynamikken i forbindelse med gennemsnitsomkostninger, når der træffes prissætningsbeslutninger eller spores udsving i omkostningerne, som skyldes fejl i dataposterne.|[Registrere nye varer](inventory-how-register-new-items.md)|  
|Oprette en produktionsvares standardkostpris ved at angive de tre omkostningselementer: materialer, kapacitet og underleverandør.|[Om beregning af standardomkostning](finance-about-calculating-standard-cost.md)|  
|Beregne kostprisen for en styklistevare baseret på købsprisen for de underliggende komponenter.|[Arbejde med styklister](inventory-how-work-BOMs.md)|  
|Fuldføre prisberegningens livscyklus for en produceret vare ved at regulere omkostningerne og afstemme værdiposterne med finansposterne.|[Om de færdige produktionsomkostninger](finance-about-finished-production-order-costs.md)|  
|Ændre værdien for en vare på lageret eller værdien af én varepost, f.eks. en købstransaktion.|[Regulere lagerbeholdning](inventory-how-revalue-inventory.md)|
|Fortryde en vareudligning manuelt eller udligne automatisk oprettede vareposter igen.|[Fjerne og genanvende vareposter](finance-how-to-remove-and-reapply-item-entries.md)|  
|Brug feltet **Udlign fra-post** i varekladden til manuelt at oprette en fast udligning mellem en indgående transaktion og den oprindelige udgående transaktion.|[Lukke åbne vareposter, der fremkommer ved fast udligning i varekladden](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)|  

## <a name="see-also"></a>Se også  
[Administrere lageromkostninger](finance-manage-inventory-costs.md)
[Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)
