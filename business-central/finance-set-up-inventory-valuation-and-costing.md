---
title: Konfigurere lagerværdi og efterkalkulation
description: 'For at sikre, at lageromkostningerne registreres korrekt, skal du angive forskellige felter og sider, før du begynder at foretage varetransaktioner.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 07/29/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="set-up-inventory-valuation-and-costing"></a>Konfigurere lagerværdi og efterkalkulation

For at sikre, at lageromkostningerne registreres korrekt, skal du angive forskellige felter og sider, før du begynder at foretage varetransaktioner. Virksomheder vælger typisk en bestemt kostmetode og anvender den på lagervarer, f.eks. for at hjælpe dem med at spore værdien på lager.  

> [!TIP]
> Du kan finde en introduktion til efterkalkulation i [!INCLUDE [prod_short](includes/prod_short.md)], se [Om lagerkostmetode](finance-learn-about-costing.md).

Den følgende tabel indeholder en opgavesekvens med links til de artikler, der rummer beskrivelserne af opgaverne.

|**Hvis du vil**|**Se**|  
|------------|-------------|
|Angiv en standardprisberegningsmetode for hver vare, der skal styre, hvordan varens indgående kostpris bruges til at vurdere lagerværdi og kostprisen på solgte varer.|[Konfigurere generelle lageroplysninger](inventory-how-setup-general.md)|  
|Angive en kostmetode for individuelle varer, hvis de kræver en anden kostmetode.|[Registrere nye varer](inventory-how-register-new-items.md)|  
|Kontrollere, at kostprisen automatisk bogføres til finansposterne, hver gang en lagertransaktion bogføres.|Feltet **Aut. lagerværdibogføring** på siden **Lageropsætning**|  
|Kontrollere, at forventede kostpriser bogføres til finansposterne, så der fra de midlertidige finanskonti kan ses et estimat over forfaldne beløb og kostprisen for de handlede varer, før de faktureres.|Feltet **Bogf. af forventet kostpris** på siden **Lageropsætning**|  
|Definere systemet, så der automatisk reguleres for eventuelle kostprisændringer, hver gang du bogfører lagertransaktioner.|[Regulere varepriser](inventory-how-adjust-item-costs.md)|  
|Definere, om gennemsnitskostprisen kun skal beregnes pr. vare for hver lagervare og for hver varevariant.|Feltet **Beregn.type for gnsn. kostpris** på siden **Lageropsætning**|  
|Vælge den tidsperiode, programmet skal anvende til beregning af den vægtede gennemsnitsomkostning for varer, der bruger gennemsnitsprisberegningsmetoden.|Feltet **Gennemsnitlig omkostningsperiode** på siden **Lageropsætning**|  
|Definere lagerperioder for at kontrollere lagerværdi over tid ved ikke at tillade bogføring af transaktioner i lukkede lagerperioder.|[Arbejde med lagerperioder](finance-how-to-work-with-inventory-periods.md)|  
|Sørg for, at salgsopgørelser udlignes til den oprindelige udgående transaktion for at bevare lagerværdi.|Feltet **Obl. præcis kostprisudligning** på siden **Salg og tilgodehavender**|  
|Sørg for, at returneringer af køb udlignes til den oprindelige indgående transaktion for at bevare lagerværdi.|Feltet **Obl. præcis kostprisudligning** på siden **Køb og tilgodehavender**|
|Definere afrundingsregler, der skal anvendes ved regulering af eller forslag til varepriser eller standardomkostninger.|Siden **Afrundingsmetode**|  

## <a name="see-also"></a>Se også

[Administrere lageromkostninger](finance-manage-inventory-costs.md)    
[Oprette generelle lageroplysninger](inventory-how-setup-general.md)    
[Afstemme lageromkostninger med finans](finance-how-to-post-inventory-costs-to-the-general-ledger.md)    
[Bedste fremgangsmåder for opsætning: Kostmetode](setup-best-practices-costing-method.md)    
[Designoplysninger: Lagerregulering](design-details-inventory-costing.md)    
[Designoplysninger: Ændre kostmetoden for varer](design-details-changing-costing-methods.md)    
[Arbejde med Business Central](ui-work-product.md)    
[Finans](finance.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
