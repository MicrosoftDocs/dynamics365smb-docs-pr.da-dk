---
title: Administrere lager
description: Dette emne beskriver, hvordan du administrerer de fysiske produkter, som du handler i, ved at oprette et varekort.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 24337d2cd96e4511f1917980c94af407381e96d2
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/30/2021
ms.locfileid: "6325314"
---
# <a name="how-to-manage-inventory"></a>Fremgangsmåde: Regulere lagerbeholdningen
For hvert fysisk produkt, som du vil handle med, skal du oprette et varekort af typen **Lager**. De varer, du tilbyder kunderne, men ikke lagerfører, kan du registrere som katalogvarer, som du kan konvertere til lagervarer, når det er nødvendigt. Du kan øge eller mindske antallet af en vare på lager ved at bogføre direkte til vareposterne, f.eks. efter en fysisk optælling eller hvis du ikke registrerer indkøb.

Lagerforøgelser og -reduktioner registreres naturligt også, når du bogfører købs- og salgsdokumenter. Du kan finde flere oplysninger i [Registrere køb](purchasing-how-record-purchases.md) og [Sælge produkter](sales-how-sell-products.md) og [Fakturere salg](sales-how-invoice-sales.md). Overførsler mellem lokationer ændrer lagerbeholdningen på tværs af virksomhedens lagersteder.   

Hvis du vil øge dit overblik over varerne og lettere kunne finde dem, kan du kategorisere varer og give dem attributter, du kan søge og sortere efter.

> [!NOTE]
> Den fysiske håndtering af varer kaldes lageraktiviteter. Du kan finde flere oplysninger i [Logistik](warehouse-manage-warehouse.md).

Planlægning af varer til opfyldelse af behov dækkes som en del af forsyningsplanlægningsfunktionaliteten. Du kan finde flere oplysninger i [Planlægning](production-planning.md).  

## <a name="inventory-reconciliation"></a>Lagerafstemning
Når du bogfører lagertransaktioner, f.eks. salgsleverancer, købsfakturaer eller lagerreguleringer, registreres ændringen i varepriser i værdiposterne. For at afspejle ændringen af lagerværdien i dine finansielle regnskaber bogføres lagerværdien automatisk i de relaterede lagerkonti i finansbogholderiet. For hver lagertransaktion du bogfører, bogføres den relevante værdi på lagerkontoen, reguleringskontoen og vareforbrugskontoen i finansregnskabet. Du kan finde flere oplysninger i [Afstemme kostpriser med finansregnskabet](finance-how-to-post-inventory-costs-to-the-general-ledger.md).

Selvom lagerværdien automatisk bogføres i Finans, er det stadig nødvendigt at sikre, at værdien af varerne overføres til de relaterede udgående transaktioner, f.eks salg eller overflytninger. Dette er især vigtigt i de situationer, hvor du sælger varer, inden du fakturerer købet af varerne. Dette omtales som omkostningsregulering. Varepriser reguleres automatisk, når du bogfører transaktioner, men du kan også justere varepriser manuelt. Du kan finde flere oplysninger i [Regulere varepriser](inventory-how-adjust-item-costs.md).  

## <a name="related-tasks"></a>Relaterede emner

I følgende tabel beskrives relaterede opgaver.

|Hvis du vil |Skal du se |
|---|----|
|Oprette varekort for lagervarer, som du handler med.|[Registrere nye varer](inventory-how-register-new-items.md)|
|Strukturer overordnede varer, du sælger som pakker, der består af den overordnede vares komponenter eller af montage til ordre- eller montage til lager-pakker.|[Arbejde med styklister](inventory-how-work-BOMs.md)|
|Hav altid overblik over varer, og få hjælp til at finde og sortere varer ved at arrangere dem i kategorier.|[Kategorisere varer](inventory-how-categorize-items.md)|
|Tildel vareattributter af forskellige værdityper til dine varer for lettere at kunne sortere og finde varer.|[Arbejde med vareattributter](inventory-how-work-item-attributes.md)|
|Opret særlige varekort for de varer, du tilbyder kunderne, men ikke lagerfører.|[Arbejde med katalogvarer](inventory-how-work-nonstock-items.md)|
|Udfør lageroptælling ved hjælp af siderne **Lageropgørelsesordre** og **Registrering af lageropgørelse**.|[Lageroptælling ved hjælp af dokumenter](inventory-how-count-inventory-with-documents.md)|
|Foretag fysisk optælling, foretag negative eller positive reguleringer, og rediger oplysninger, f.eks. placering eller lotnummer, på vareposter.|[Tælle, justere og ompostere inventar ved hjælp af kladder](inventory-how-count-adjust-reclassify.md)|
|Få vist tilgængeligheden af varer pr. lokation og pr. periode efter salgs- eller købshændelse eller efter deres brug i montage- eller produktionsstyklister.|[Vise varedisponering](inventory-how-availability-overview.md)|
|Overflyt lagervarer mellem lokationer med overflytningsordrer for at styre lageraktiviteter eller med vareomposteringskladden.|[Overflytte lagerbeholdning mellem lokationer](inventory-how-transfer-between-locations.md)|
|Reservere lagervarer eller indgående varer til salgsordrer, købsordrer, serviceordrer, montageordrer eller produktionsordrer.|[Reservere varer](inventory-how-to-reserve-items.md)|
|Tildel serienumre eller lotnumre til en udgående eller indgående bilags- eller kladdelinje, for eksempel for at spore varer i tilfælde af tilbagekaldelser.|[Arbejde med serienumre og lotnumre](inventory-how-work-item-tracking.md)|
|Konfigurer en kreditors eller debitors egen varebeskrivelse på dit varekort, så du hurtigt kan indsætte deres varebeskrivelse i handelsdokumenter.|[Bruge varereferencer](inventory-how-use-item-cross-refs.md)|
|Find, hvor et serie- eller lotnummer blev brugt i forsyningskæden, f.eks. i tilfælde af tilbagekaldelse.|[Spore vare via varesporing](inventory-how-to-trace-item-tracked-items.md)|
|Spær for, at varer kan angives på salgs- eller købslinjer eller for, at de bogføres i nogen posteringer.|[Spærre for varer](inventory-how-block-items.md)|
|Administrer forretningsaktiviteter på salgskontorer, indkøbsafdelinger eller fabriksplanlægningskontor på tværs af flere lokationer.|[Arbejde med ansvarscentre](inventory-responsibility-centers.md)|
|Bruge ressourcer med specifikke kvalifikationer til forskellige tjenester og serviceartikler.|[Opsætte ressourceallokering](service-how-setup-resource-allocation.md)|

## <a name="see-also"></a>Se også

[Logistik](warehouse-manage-warehouse.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]