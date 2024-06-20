---
author: brentholtorf
ms.topic: include
ms.date: 11/14/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

Felterne **Bilagsdato** og **Bogføringsdato** på salgs- og købsdokumenter hjælper dig med at overholde regnskabsstandarder og få nøjagtige økonomiske beregninger. Felterne tjener forskellige formål:

- Hvis [!INCLUDE [prod_short](prod_short.md)] du vil beregne rentenotaer og det skyldige beløb på salgsfakturaer korrekt, skal **dokumentdatoen** stemme overens med en af følgende datoer:

   - Datoen på den salgsfaktura, du har sendt til kunden. 
   - Datoen på den købsfaktura, du har modtaget fra din kreditor.
- **Bogføringsdatoen** viser, hvornår et dokument blev registreret i [!INCLUDE [prod_short](prod_short.md)]. Mange regnskabsstandarder og -regler kræver, at virksomheder registrerer og rapporterer finansielle transaktioner baseret på den dato, de fandt sted.

Afhængigt af dine forretningsprocesser er disse datoer måske eller måske ikke de samme. Hvis de er ens, kan du indstille [!INCLUDE [prod_short](prod_short.md)] til at opdatere bilagsdatoen på salgs- og købsdokumenter med den dato, hvor du bogførte dem.  
  
Hvis du automatisk vil indstille bilagsdatoer til bogføringsdatoer, skal du slå **Tilknyt bilagsdato til** og **Købsopsætning** på siderne **Bogføringsdato og Købsopsætning**.

> [!NOTE]
> Indstillingen påvirker ikke salgs- eller købskladder.