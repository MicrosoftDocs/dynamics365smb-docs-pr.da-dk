---
title: "Opsætning af lagerværdi og lageromkostningsadministration | Microsoft Docs"
description: "Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 86fd8f6b15b8a2f868db2938278df6147a092725
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="setting-up-inventory-valuation-and-costing"></a>Opsætte lagerværdi og kostprisberegning
For at sikre, at lageromkostningerne registreres korrekt, skal du angive forskellige felter og vinduer, før du begynder at foretage varetransaktioner.

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Definere en prisberegningsmetode for hver vare, der skal styre, hvordan varens indgående kostpris bruges til at vurdere lagerværdi og kostprisen på solgte varer.|[Fremgangsmåde: Registrere nye varer](inventory-how-register-new-items.md)|  
|Kontrollere, at kostprisen automatisk bogføres til finansposterne, hver gang en lagertransaktion bogføres.|Feltet **Aut. lagerværdibogføring** på siden **Lageropsætning**|  
|Kontrollere, at forventede kostpriser bogføres til finansposterne, så der fra de midlertidige lagerbeholdningskonti kan ses et estimat over forfaldne beløb og kostprisen for de handlede varer, før de reelt faktureres.|Feltet **Bogf. af forventet kostpris** på siden **Lageropsætning**|  
|Definere systemet, så der automatisk reguleres for eventuelle kostprisændringer, hver gang du bogfører lagertransaktioner.|[Fremgangsmåde: Regulere varepriser](inventory-how-adjust-item-costs.md)|  
|Definere, om gennemsnitskostprisen kun skal beregnes pr. vare for hver lagerenhed og for hver varevariant.|Feltet **Beregn.type for gnsn. kostpris** på siden **Lageropsætning**|  
|Vælge den tidsperiode, programmet skal anvende til beregning af den vægtede gennemsnitsomkostning for varer, der bruger gennemsnitsprisberegningsmetoden.|Feltet **Gennemsnitlig omkostningsperiode** på siden **Lageropsætning**|  
|Definere lagerperioder for at kontrollere lagerværdi over tid ved ikke at tillade bogføring af transaktioner i lukkede lagerperioder.|[Sådan gør du: Arbejde med lagerperioder](finance-how-to-work-with-inventory-periods.md)|  
|Sørg for, at salgsopgørelser udlignes til den oprindelige udgående transaktion for at bevare lagerværdi.|Feltet **Obl. præcis kostprisudligning** på siden **Salg og tilgodehavender**|  
|Sørg for, at returneringer af køb udlignes til den oprindelige indgående transaktion for at bevare lagerværdi.|Feltet **Obl. præcis kostprisudligning** på siden **Køb og tilgodehavender**|
|Definere afrundingsregler, der skal anvendes ved regulering af eller forslag til varepriser eller standardomkostninger.|Siden **Afrundingsmetode**|  

## <a name="see-also"></a>Se også  
[Administrere lageromkostninger](finance-manage-inventory-costs.md)  
[Arbejde med Dynamics 365](ui-work-product.md)  
[Finans](finance.md)  

