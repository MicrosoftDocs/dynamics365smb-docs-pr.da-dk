---
title: Designoplysninger – Bogf. af forventet kostpris | Microsoft Docs
description: Forventede kostpriser repræsenterer et overslag over f.eks. en købt vares omkostninger, som du registrerer, før du modtager fakturaen for varen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 22e01f8b22c7f222674ff43090a27f5466dd8387
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751626"
---
# <a name="design-details-expected-cost-posting"></a>Designoplysninger: Bogføring af forventet kostpris
Forventede kostpriser repræsenterer et overslag over f.eks. en købt vares omkostninger, som du registrerer, før du modtager fakturaen for varen.  

 Du kan bogføre forventede omkostninger til både lagerbeholdning og finans. Når du bogfører et antal, der kun er modtaget eller leveret, men ikke faktureret, oprettes der en værdipost med de forventede omkostninger. Denne forventede omkostning påvirker lagerværdien, men bogføres ikke i finans, medmindre det er angivet i opsætningen af programmet.  

> [!NOTE]  
>  Forventede kostpriser administreres kun for varetransaktioner. Forventede kostpriser er ikke for immaterielle transaktionstyper, som f.eks. kapacitets- og varegebyrer.  

 Hvis der kun er bogført mængdedelen af en lagerforøgelse, ændres lagerværdien i finansregnskabet ikke, medmindre du har markeret afkrydsningsfeltet **Bogf. af forventet kostpris** på siden **Opsætning af Lager**. I så fald bogføres forventede kostpriser på mellemregningskonti på tidspunktet for modtagelsen. Når modtagelsen er fuldt faktureret, afstemmes mellemregningskontoerne, og de faktiske omkostninger bogføres til lagerkontoen.  

 Den fakturerede værdipost viser det forventede kostbeløb, der er bogført for at udligne mellemregningskontiene for at understøtte afstemnings- og sporingsarbejde.  

## <a name="example"></a>Eksempel  
 Nedenstående eksempel viser forventet kostpris, hvis afkrydsningsfelterne **Aut. lagerværdibogføring** og **Bogf. af forventet kostpris** er markeret på siden **Opsætning af lager**.  

 Du kan bogføre en købsordre som modtaget. Den forventede kostpris er 95,00 RV.  

 **Værdiposter**  

|Bogføringsdato|Postens type|Kostbeløb (forventet)|Bogført forventet kostpris|Forventet kostpris|Varepostløbenr.|Løbenr.|  
|------------------|----------------|------------------------------|----------------------------------|-------------------|---------------------------|---------------|  
|01-01-20|Købspris|95,00|95,00|Ja|1|1|  

 **Relationsposter i finans – relationstabel for varefinans**  

|Finansløbenr.|Værdiløbenr.|Finansjournalnr.|  
|--------------------|---------------------|-----------------------|  
|1|1|1|  
|2|1|1|  

 **Finansposter**  

|Bogføringsdato|Finanskonto|Kontonummer (En-US Demo)|Beløb|Løbenr.|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-01-20|Lagerperiodekonto (mellemregningskonto)|5530|-95,00|2|  
|01-01-20|Lagerkonto (mellemregningskonto)|2131|95,00|1|  

 Du kan senere bogføre købsordren som faktureret. Den fakturerede kostpris er 100,00 RV.  

 **Værdiposter**  

|Bogføringsdato|Kostbeløb (faktisk)|Kostbeløb (forventet)|Bogført kostværdi|Forventet kostpris|Varepostløbenr.|Løbenr.|  
|------------------|----------------------------|------------------------------|-------------------------|-------------------|---------------------------|---------------|  
|01-15-20|100.00|-95,00|100.00|Nej|1|2|  

 **Relationsposter i finans – relationstabel for varefinans**  

|Finansløbenr.|Værdiløbenr.|Finansjournalnr.|  
|--------------------|---------------------|-----------------------|  
|3|2|2|  
|4|2|2|  
|5|2|2|  
|6|2|2|  

 **Finansposter**  

|Bogføringsdato|Finanskonto|Kontonummer (En-US Demo)|Beløb|Løbenr.|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-15-20|Lagerperiodekonto (mellemregningskonto)|5530|95,00|4|  
|01-15-20|Lagerkonto (mellemregningskonto)|2131|-95,00|3|  
|01-15-20|Tillagte dir. omkost.konto|7291|-100|6|  
|01-15-20|Lagerkonto|2130|100|5|  

## <a name="see-also"></a>Se også
 [Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)   
 [Designoplysninger: Omkostningsregulering](design-details-cost-adjustment.md)   
 [Designoplysninger: Afstemning med Finans](design-details-reconciliation-with-the-general-ledger.md)   
 [Designoplysninger: Varekladde](design-details-inventory-posting.md)   
 [Designoplysninger: Afvigelse](design-details-variance.md)  
 [Administrere lageromkostninger](finance-manage-inventory-costs.md)  
 [Finans](finance.md)  
 [Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]