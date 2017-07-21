---
title: Administrere lager | Microsoft Docs
description: "Bruges til at styre de fysiske produkter, som du handler med, f.eks. håndtering af lagerbeholdning på lagerstedet."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 920df314dc8b671d4e2d99d8449ee02a74cb9078
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017

---

# <a name="inventory"></a>Lagerbeholdning
For hvert fysisk produkt, som du vil handle med, skal du oprette et varekort af typen **Lager**. De varer, du tilbyder kunderne, men ikke lagerfører, kan du registrere som katalogvarer, som du kan konvertere til lagervarer, når det er nødvendigt. Du kan øge eller mindske antallet af en vare på lager ved at bogføre direkte til vareposterne, f.eks. efter en fysisk optælling eller hvis du ikke registrerer indkøb.

Lagerforøgelser og -reduktioner registreres naturligt også, når du bogfører købs- og salgsdokumenter. Du kan finde flere oplysninger i [Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md) og [Fremgangsmåde: Sælge produkter](sales-how-sell-products.md) og [Fremgangsmåde: Fakturere salg](sales-how-invoice-sales.md). Overførsler mellem lokationer ændrer lagerbeholdningen på tværs af virksomhedens lagersteder.   

Hvis du vil øge dit overblik over varerne og lettere kunne finde dem, kan du kategorisere varer og give dem attributter, du kan søge og sortere efter.

Du skal sikre, at omkostningerne for varerne overføres til den relaterede udgående salgstransaktion, især i situationer, hvor du sælger varer, før du fakturerer købet af de pågældende varer. Dette kaldes kostregulering, som du kan udføre manuelt eller indstille til at ske automatisk, når du bogfører en varetransaktion.

## <a name="inventory-reconciliation"></a>Lagerafstemning
Når du bogfører lagertransaktioner, f.eks. salgsleverancer, købsfakturaer eller lagerreguleringer, registreres ændringen i varepriser i værdiposterne. For at afspejle ændringen af lagerværdien i dine finansielle regnskaber bogføres lagerværdien automatisk i de relaterede lagerkonti i finansbogholderiet. For hver lagertransaktion du bogfører, bogføres den relevante værdi på lagerkontoen, reguleringskontoen og vareforbrugskontoen i finansregnskabet.

Selvom lagerværdien automatisk bogføres i Finans, er det stadig nødvendigt at sikre, at værdien af varerne overføres til de relaterede udgående transaktioner, f.eks salg eller overflytninger. Dette er især vigtigt i de situationer, hvor du sælger varer, inden du fakturerer købet af varerne. Dette omtales som omkostningsregulering. Varepriser reguleres automatisk, når du bogfører transaktioner, men du kan også justere varepriser manuelt. Du kan finde flere oplysninger i Fremgangsmåde: Regulere varepriser.

|Til |Se |
|---|----|
|Opret varekort for lagervarer, som du handler med.|[Fremgangsmåde: Registrere nye varer](inventory-how-register-new-items.md)|
|Strukturer overordnede varer, du sælger som pakker, der består af den overordnede vares komponenter eller af montage til ordre- eller montage til lager-pakker.|[Fremgangsmåde: Arbejde med styklister](inventory-how-work-BOMs.md)|
|Hav altid overblik over varer, og få hjælp til at finde og sortere varer ved at arrangere dem i kategorier.|[Fremgangsmåde: Kategorisere varer](inventory-how-categorize-items.md)|
|Tildel vareattributter af forskellige værdityper til dine varer for lettere at kunne sortere og finde varer.|[Fremgangsmåde: Arbejde med vareattributter](inventory-how-work-item-attributes.md)|
|Opret særlige varekort for de varer, du tilbyder kunderne, men ikke lagerfører.|[Fremgangsmåde: Arbejde med katalogvarer](inventory-how-work-nonstock-items.md)|
|Foretag fysisk optælling, foretag negative eller positive reguleringer, og rediger oplysninger, f.eks. placering eller lotnummer, på vareposter.|[Fremgangsmåde: Tælle, justere og ompostere lager](inventory-how-count-adjust-reclassify.md)|
|Få vist tilgængeligheden af varer pr. lokation og pr. periode efter salgs- eller købshændelse eller efter deres brug i montagestyklister.|[Sådan gør du: Vise varedisponering](inventory-how-availability-overview.md)|
|Overflyt lagervarer mellem lokationer med overflytningsordrer for at styre lageraktiviteter eller med vareomposteringskladden.|[Fremgangsmåde: Overflytte lagerbeholdning mellem lokationer](inventory-how-transfer-between-locations.md)|
|Op- eller nedskriv værdien af en eller flere varer på lageret ved at bogføre deres aktuelle, beregnede værdi.|[Fremgangsmåde: Regulere lagerbeholdningen](inventory-how-revalue-inventory.md)|
|Reguler varepriser, enten automatisk eller manuelt, for at videresende kostprisændringer fra indgående poster til deres relaterede udgående poster.|[Fremgangsmåde: Regulere varepriser](inventory-how-adjust-item-costs.md)|

## <a name="see-also"></a>Se også  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)    
[Forsyningskæde](madeira-supply-chain.md)  
[Arbejde med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
