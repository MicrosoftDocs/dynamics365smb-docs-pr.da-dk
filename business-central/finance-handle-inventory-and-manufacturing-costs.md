---
title: Håndtere lager- og produktionsomkostninger
description: 'Lære, hvor mange felter, sider og rapporter der henvender sig til brugere, som direkte eller indirekte styrer varepriser eller operationer.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 07/30/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="handling-inventory-and-manufacturing-costs"></a>Håndtering af lager- og produktionsomkostninger

Selvom meget af funktionaliteten i omkostningsberegningen er udtrykt i underliggende processer, der ikke kræver brugermedvirken, f.eks. efterudligning og automatisk kostregulering, er mange felter, sider og rapporter beregnet til brugere, som direkte eller indirekte styrer varepriser eller drift.  

 Tildeling af varegebyrer til købsdokumenter er et eksempel på en opgave til indirekte omkostningsberegning. Opdatering af kostprisen for montage eller produktionsstyklistevare er et eksempel på en opgave til en mere direkte omkostningsberegning.  

 Den følgende tabel indeholder en opgavesekvens med links til de artikler, der rummer beskrivelserne af opgaverne.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Opdatere købsprisen for en eller flere varer - periodisk eller automatisk - for at videresende eventuelle kostprisændringer fra indgående poster, f.eks. posterne for køb eller produktionsoutput, til de relaterede udgående poster, f.eks. forbrug eller overførsler.|[Regulere varepriser](inventory-how-adjust-item-costs.md)|  
|Få indsigt i dynamikken i forbindelse med gennemsnitsomkostninger, når der træffes prissætningsbeslutninger eller spores udsving i omkostningerne, som skyldes fejl i dataposterne.|[Registrere nye varer](inventory-how-register-new-items.md)|  
|Oprette en produktionsvares standardkostpris ved at angive de tre omkostningselementer: materialer, kapacitet og underleverandør.|[Om beregning af standardomkostning](finance-about-calculating-standard-cost.md)|  
|Beregne kostprisen for en styklistevare baseret på købsprisen for de underliggende komponenter.|[Arbejde med styklister](inventory-how-work-BOMs.md) |  
|Fuldføre prisberegningens livscyklus for en produceret vare ved at regulere omkostningerne og afstemme værdiposterne med finansposterne.|[Om de færdige produktionsomkostninger](finance-about-finished-production-order-costs.md)|  
|Ændre værdien for en vare på lageret eller værdien af én varepost, f.eks. en købstransaktion.|[Regulere lagerbeholdning](inventory-how-revalue-inventory.md)|
|Fortryde en vareudligning manuelt eller udligne automatisk oprettede vareposter igen.|[Fjerne og genanvende vareposter](finance-how-to-remove-and-reapply-item-entries.md)|  
|Brug feltet **Udlign fra-post** i varekladden til manuelt at oprette en fast udligning mellem en indgående transaktion og den oprindelige udgående transaktion.|[Lukke åbne vareposter, der fremkommer ved fast udligning i varekladden](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)|  

## <a name="see-also"></a>Se også

[Håndtere lageromkostninger](finance-manage-inventory-costs.md)    
[Designoplysninger: Lagerberegning](design-details-inventory-costing.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
