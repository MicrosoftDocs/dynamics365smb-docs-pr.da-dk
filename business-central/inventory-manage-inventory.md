---
title: Administrere lager
description: 'Denne artikel beskriver, hvordan du administrerer de fysiske produkter, som du handler i, ved at oprette et varekort.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'warehouse, stock'
ms.search.forms: '5804, 2106, 5823, 5751, 5750, 772, 5829, 5828, 513, 304, 40, 38, 167, 117, 5827, 9223, 158, 354, 9152, 286, 5754, 5402, 209, 297, 298, 99000782'
ms.date: 03/21/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="manage-inventory"></a>Administrere lager

For hvert fysisk produkt, som du vil handle med, skal du oprette et varekort af typen **Lager**. De varer, du tilbyder kunderne, men ikke lagerfører, kan du registrere som katalogvarer, som du kan konvertere til lagervarer, når det er nødvendigt. Du kan øge eller mindske antallet af en vare på lager ved at bogføre direkte til vareposterne, f.eks. efter en fysisk optælling eller hvis du ikke registrerer indkøb.

Lagerforøgelser og -reduktioner registreres naturligt også, når du bogfører købs- og salgsdokumenter. Du kan finde flere oplysninger i [Registrere køb](purchasing-how-record-purchases.md) og [Sælge produkter](sales-how-sell-products.md) og [Fakturere salg](sales-how-invoice-sales.md). Overførsler mellem lokationer ændrer lagerbeholdningen på tværs af virksomhedens lagersteder.

Hvis du vil øge dit overblik over varerne og lettere kunne finde dem, kan du kategorisere varer og give dem attributter, du kan søge og sortere efter.

> [!NOTE]
> Den fysiske håndtering af varer kaldes lageraktiviteter. Få mere at vide i [Oversigt over Warehouse Management](design-details-warehouse-management.md).

Planlægning af varer til opfyldelse af behov dækkes som en del af forsyningsplanlægningsfunktionaliteten. Få mere at vide i [Planlægning](production-planning.md).  

## <a name="inventory-analytics"></a>Lageranalyse

I dette afsnit beskrives de analyseværktøjer, du kan bruge til at få indsigt i dine lagerdata.

| Til... | Se |
| --- | --- |
| Få mere at vide om funktioner til analyse af lagerdata. | [Oversigt over salgsanalyse](inventory-analytics-overview.md) |
| Foretag ad hoc-analyser af lagerdata direkte på listesider og forespørgsler. | [Ad hoc-analyse af lagerdata](ad-hoc-analysis-inventory.md) |
| Udforsk indbyggede lagerrapporter. | [Indbygget lager og lagerrapporter](inventory-WMS-reports.md) |

## <a name="inventory-reconciliation"></a>Lagerafstemning

Når du bogfører lagertransaktioner, f.eks. salgsleverancer, købsfakturaer eller lagerreguleringer, registreres ændringen i varepriser i værdiposterne. For at afspejle ændringen af lagerværdien i dine finansielle regnskaber bogføres lagerværdien automatisk i de relaterede lagerkonti i finansbogholderiet. For hver lagertransaktion du bogfører, bogføres den relevante værdi på lagerkontoen, reguleringskontoen og vareforbrugskontoen i finansregnskabet. Flere oplysninger i [Afstemme lageromkostninger med finansregnskabet](finance-how-to-post-inventory-costs-to-the-general-ledger.md).

Selvom lagerværdien automatisk bogføres i Finans, er det stadig nødvendigt at sikre, at værdien af varerne overføres til de relaterede udgående transaktioner, f.eks. salg eller overflytninger. Dette er især vigtigt i de situationer, hvor du sælger varer, inden du fakturerer købet af varerne. Dette omtales som omkostningsregulering. Varepriser reguleres automatisk, når du bogfører transaktioner, men du kan også justere varepriser manuelt. Få mere at vide om [Regulere varepriser](inventory-how-adjust-item-costs.md).  

## <a name="related-tasks"></a>Relaterede emner

I følgende tabel beskrives relaterede opgaver.

|Til |Se |
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
|Reservere lagervarer eller indgående varer til salgsordrer, købsordrer, serviceordrer, montageordrer, overførselsordrer eller produktionsordrer.|[Reservere varer](inventory-how-to-reserve-items.md)|
|Oprette varesporing, så du kan spore vareserienumre, f. eks. for at spore varer i tilfælde af genkald.|[Konfigurere varesporing med serie-, lot- og pakkenumre](inventory-how-setup-item-tracking.md)|
|Tildel et udgående eller indgående dokument eller en kladdelinje serienumre eller lotnumre.|[Arbejde med serienumre og lotnumre](inventory-how-work-item-tracking.md)|
|Find, hvor et serie- eller lotnummer blev brugt i forsyningskæden, f.eks. i tilfælde af tilbagekaldelse.|[Spore vare via varesporing](inventory-how-to-trace-item-tracked-items.md)|
|Konfigurer en kreditors eller debitors egen varebeskrivelse på dit varekort, så du hurtigt kan indsætte deres varebeskrivelse i handelsdokumenter.|[Anvend varereferencer](inventory-how-use-item-cross-refs.md)|
|Spær for, at varer kan angives på salgs- eller købslinjer eller for, at de bogføres i nogen posteringer.|[Spærre for varer](inventory-how-block-items.md)|
|Administrer forretningsaktiviteter på salgskontorer, indkøbsafdelinger eller fabriksplanlægningskontor på tværs af flere lokationer.|[Arbejde med ansvarscentre](inventory-responsibility-centers.md)|

## <a name="see-also"></a>Se også

[Oversigt over logistik](design-details-warehouse-management.md)    
[Køb](purchasing-manage-purchasing.md)    
[Salg](sales-manage-sales.md)    
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    
[Generelle forretningsfunktioner](ui-across-business-areas.md)    

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
