---
title: Montagestyring
description: 'Se, hvordan du kan levere produkter til kunder ved at kombinere komponenter i enkle processer uden produktionsfunktionen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="assembly-management" />Montagestyring

Firmaer kan levere produkter til kunder ved at kombinere komponenter i enkle processer uden produktionsfunktionen. Funktioner til samling af varer integreres med relaterede funktioner som f. eks. salg, planlægning, reservationer og logistik.  

Et montageelement er et salgbart element, der indeholder en montagestykliste. Hvis du vil vide mere om montagestyklister, skal du gå til [Arbejde med montagestyklister](assembly-how-work-assembly-boms.md).

Montageordrer er interne ordrer, f. eks. produktionsordrer. Bruge montageordrer til at administrere montageprocessen og oprette forbindelse mellem salgsbehov og lageraktiviteter. Montageordrer omfatter både afgang og forbrug ved bogføring. Montageordrehoveder svarer til Afgangskladdelinjer. Montageordrelinjer svarer til forbrugskladdelinjer.  

Du kan bruge en Just-in-time-lagerstrategi og tilpasse produkter for at imødekomme kundeanmodninger. Montageordrer kan automatisk oprettes og tilknyttes, når du opretter en salgsordrelinje. Linket mellem salgsbehovet og montage leveringen åbnes for flere leads, når du behandler salgsordrer:

* Tilpasse montageelementer løbende.
* Love leveringsdatoer i henhold til komponenttilgængeligheden.
* Bogføre afgang og levering af montage varen direkte fra deres salgsordrer.

Du kan lære mere om montage efter ordre ved at gå til [Sælge varer, der er samlet til ordre](assembly-how-to-sell-items-assembled-to-order.md).  

Linjer i salgsordrer kan indeholde varer, der skal plukkes fra lager, og varer, der skal monteres for ordren. Montage efter ordre-mængderne tilsidesætter lagerbeholdningsantal i delvis levering. Du kan lære mere om montage efter ordre ved at gå til [Kombinationsscenarier](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

Når en montage efter ordre-mængde er klar til at blive leveret, bogfører den ansvarlige lagermedarbejder et lagerpluk for de pågældende salgsordrelinjer. Når du bogfører et lagerpluk, sker der et par ting:

* Oprette en flytning (lager) for komponenterne
* Bogfør montage-output og salgsordreleverance.

Du kan finde flere oplysninger om montage til ordre-varer og lagerpluk i [Håndtering af montage til ordre-varer med pluk](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

Den følgende tabel indeholder en opgavesekvens med links til de artikler, der rummer beskrivelserne af opgaverne.

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Lære, hvordan du samler varer til salgsordrer og lager.|[Om montage til ordre og montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md)|
|Brug lokationskort i din lageropsætning for at definere, hvordan varer strømmer til og fra montageafdelingen.|[Oprette grundlæggende lagersteder med handlingsområder](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|
|Tilbud på et tilpasses montageelement, og konverter tilbuddet til et salg, når kunden accepterer det.|[Oprette tilbud på montage til ordre-salg](assembly-how-to-quote-an-assemble-to-order-sale.md)|
|Kombiner komponenter for at oprette et element i en enkel proces, til bestilling eller til lager.|[Montere varer](assembly-how-to-assemble-items.md)|  
|Sælg montageelementer, der ikke er tilgængelige i øjeblikket, ved at oprette en tilknyttet montageordre for at levere den fulde eller delvise salgsordremængde.|[Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md)|
|Når nogle montage til ordre-elementer allerede findes i lageret, kan du fratrække mængden fra montageordren og reservere den fra lageret.|[Sælge lagervarer i montage til ordre-forløb](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)|  
|Hvis montageelementer ikke er på lager, skal du bruge en montageordre til at levere noget eller alle mængder.|[Sælge montage til ordre-varer og lagervarer sammen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)|
|Gøre tilpassede montageelementer til rammesalgsordrer, før du opretter salgsordrerne.|[Oprette rammemontageordrer](assembly-how-to-create-blanket-assembly-orders.md)|
|Annuller en bogført montageordre, for eksempel fordi ordren er bogført med fejl.|[Fortryde bogføring af montage](assembly-how-to-undo-assembly-posting.md)|
|Få mere at vide om, hvordan du arbejder med montagestyklister, og hvordan de er forskellige fra produktionsstyklister.|[Arbejde med montagestyklister](assembly-how-work-assembly-boms.md)|
|Se, hvordan du bogfører montageforbrug og afgang, og hvordan [!INCLUDE [prod_short](includes/prod_short.md)] distribuerer vare- og ressourcekostpriser til finansposterne.|[Designoplysninger: Bogføring af montageordre](design-details-assembly-order-posting.md)|  

## <a name="see-related-microsoft-trainingtrainingpathsassemble-items-dynamics--business-central" />Se relateret [Microsoft-træning](/training/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also" />Se også

[Arbejde med styklister](inventory-how-work-BOMs.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Oversigt over lagerstyring](design-details-warehouse-management.md)
[Designdetaljer: Leveringsplanlægning](design-details-supply-planning.md)  
<!-- [Walkthrough: Planning Supplies Manually](walkthrough-planning-supplies-manually.md)   -->
<!-- [Walkthrough: Selling, Assembling, and Shipping Kits](walkthrough-selling-assembling-and-shipping-kits.md)   -->
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## <a name="includeprodshortincludesfreetrialmdmd" />[!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
