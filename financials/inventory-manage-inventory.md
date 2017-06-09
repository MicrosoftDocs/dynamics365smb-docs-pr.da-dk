---
title: Lagerbeholdning | Microsoft Docs
description: Beskriver, hvordan du administrerer fysiske varer.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: b53cae82cfa532fb0620cc9e1f305216c2321785
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017

---

# <a name="inventory"></a>Lagerbeholdning
For hvert fysisk produkt, som du vil handle med, skal du oprette et varekort af typen **Lager**. De varer, du tilbyder kunderne, men ikke lagerfører, kan du registrere som katalogvarer, som du kan konvertere til lagervarer, når det er nødvendigt. Du kan øge eller mindske antallet af en vare på lager ved at bogføre direkte til vareposterne, f.eks. efter en fysisk optælling eller hvis du ikke registrerer indkøb.

Lagerforøgelser og -reduktioner registreres naturligt også, når du bogfører købs- og salgsdokumenter. Du kan finde flere oplysninger i [Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md) og [Fremgangsmåde: Sælge produkter](sales-how-sell-products.md) og [Fremgangsmåde: Fakturere salg](sales-how-invoice-sales.md). Overførsler mellem lokationer ændrer lagerbeholdningen på tværs af virksomhedens lagersteder.   

Hvis du vil øge dit overblik over varerne og lettere kunne finde dem, kan du kategorisere varer og give dem attributter, du kan søge og sortere efter.

Du skal sikre, at omkostningerne for varerne overføres til den relaterede udgående salgstransaktion, især i situationer, hvor du sælger varer, før du fakturerer købet af de pågældende varer. Dette kaldes kostregulering, som du kan udføre manuelt eller indstille til at ske automatisk, når du bogfører en varetransaktion.

Ændringer i lagerværdien fra handel afstemmes automatisk med dine finansielle regnskaber ved bogføring af varetransaktioner.

|Hvis du vil |Se |
|---|----|
|Opret varekort for lagervarer, som du handler med.|[Fremgangsmåde: Registrere nye varer](inventory-how-register-new-items.md)|
|Strukturer overordnede varer, du sælger som pakker, der består af den overordnede vares komponenter eller af montage til ordre- eller montage til lager-pakker.|[Fremgangsmåde: Arbejde med styklister](inventory-how-work-BOMs.md)|
|Hav altid overblik over varer, og få hjælp til at finde og sortere varer ved at arrangere dem i kategorier.|[Fremgangsmåde: Kategorisere varer](inventory-how-categorize-items.md)|
|Tildel vareattributter af forskellige værdityper til dine varer for lettere at kunne sortere og finde varer.|[Fremgangsmåde: Arbejde med vareattributter](inventory-how-work-item-attributes.md)|
|Opret særlige varekort for de varer, du tilbyder kunderne, men ikke lagerfører.|[Fremgangsmåde: Arbejde med katalogvarer](inventory-how-work-nonstock-items.md)|
|Forøg eller reducer en vares lagerantal, for eksempel efter en fysisk optælling eller som en nem måde at registrere købsleverancer.|[Fremgangsmåde: Regulere lageret](inventory-how-adjust-inventory.md)|
|Få vist tilgængeligheden af varer pr. lokation og pr. periode efter salgs- eller købshændelse eller efter deres brug i montagestyklister.|[Fremgangsmåde: Få en oversigt over disponering](inventory-how-availability-overview.md)|
|Overflyt lagervarer mellem lokationer med overflytningsordrer for at styre lageraktiviteter eller med vareomposteringskladden.|[Fremgangsmåde: Overflytte lagerbeholdning mellem lokationer](inventory-how-transfer-between-locations.md)|
|Op- eller nedskriv værdien af en eller flere varer på lageret ved at bogføre deres aktuelle, beregnede værdi.|[Fremgangsmåde: Regulere lagerbeholdningen](inventory-how-revalue-inventory.md)|
|Reguler varepriser, enten automatisk eller manuelt, for at videresende kostprisændringer fra indgående poster til deres relaterede udgående poster.|[Fremgangsmåde: Regulere varepriser](inventory-how-adjust-item-costs.md)|
|Få at vide, hvordan ændringer i lagerværdien fra handel afstemmes automatisk med dine finansielle regnskaber.|[Avanceret: Lagerafstemning](advanced-inventory-reconciliation.md).|

## <a name="see-also"></a>Se også  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)    
[Forsyningskæde](madeira-supply-chain.md)  
[Arbejde med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
