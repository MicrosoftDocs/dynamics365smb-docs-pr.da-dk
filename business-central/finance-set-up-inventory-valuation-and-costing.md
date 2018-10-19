---
title: "Opsætning af lagerværdi og lageromkostningsadministration | Microsoft Docs"
description: "Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 296f660f2ca4dfe7a605d2990e18567c5062a482
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="setting-up-inventory-valuation-and-costing"></a>Opsætte lagerværdi og kostprisberegning
For at sikre, at lageromkostningerne registreres korrekt, skal du angive forskellige felter og vinduer, før du begynder at foretage varetransaktioner.

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Definere en prisberegningsmetode for hver vare, der skal styre, hvordan varens indgående kostpris bruges til at vurdere lagerværdi og kostprisen på solgte varer.|[Registrere nye varer](inventory-how-register-new-items.md)|  
|Kontrollere, at kostprisen automatisk bogføres til finansposterne, hver gang en lagertransaktion bogføres.|Feltet **Aut. lagerværdibogføring** i vinduet **Lageropsætning**|  
|Kontrollere, at forventede kostpriser bogføres til finansposterne, så der fra de midlertidige lagerbeholdningskonti kan ses et estimat over forfaldne beløb og kostprisen for de handlede varer, før de reelt faktureres.|Feltet **Bogf. af forventet kostpris** i vinduet **Lageropsætning**|  
|Definere systemet, så der automatisk reguleres for eventuelle kostprisændringer, hver gang du bogfører lagertransaktioner.|[Regulere varepriser](inventory-how-adjust-item-costs.md)|  
|Definere, om gennemsnitskostprisen kun skal beregnes pr. vare for hver lagerenhed og for hver varevariant.|Feltet **Beregn.type for gnsn. kostpris** i vinduet **Lageropsætning**|  
|Vælge den tidsperiode, programmet skal anvende til beregning af den vægtede gennemsnitsomkostning for varer, der bruger gennemsnitsprisberegningsmetoden.|Feltet **Gennemsnitlig omkostningsperiode** i vinduet **Lageropsætning**|  
|Definere lagerperioder for at kontrollere lagerværdi over tid ved ikke at tillade bogføring af transaktioner i lukkede lagerperioder.|[Arbejde med lagerperioder](finance-how-to-work-with-inventory-periods.md)|  
|Sørg for, at salgsopgørelser udlignes til den oprindelige udgående transaktion for at bevare lagerværdi.|Feltet **Obl. præcis kostprisudligning** i vinduet **Salg og tilgodehavender**|  
|Sørg for, at returneringer af køb udlignes til den oprindelige indgående transaktion for at bevare lagerværdi.|Feltet **Obl. præcis kostprisudligning** i vinduet **Køb og tilgodehavender**|
|Definere afrundingsregler, der skal anvendes ved regulering af eller forslag til varepriser eller standardomkostninger.|Vinduet **Afrundingsmetode**|  

## <a name="see-also"></a>Se også  
[Administrere lageromkostninger](finance-manage-inventory-costs.md)  
[Arbejde med Business Central](ui-work-product.md)  
[Finans](finance.md)  

