---
title: Flytte varer
description: Få mere at vide om flytning af varer mellem placeringer på lagerstedet.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7315, 7349, 7351, 7382, 7384, 7386, 7387, 7399, 7400, 9314, 9330, 9345'
---
# Flytte varer

Du kan flytte varer på lagerstedet på forskellige måder afhængigt af, hvordan du har konfigureret lagerstedet. Kompleksiteten kan variere:

* Små lagersteder kan bruge grundlæggende lageropsætninger til at håndtere ordrer individuelt i et enkelt eller flere trin.
* Store lagersteder kan bruge avancerede konfigurationer, hvor alle lageraktiviteter koordineres af en styret arbejdsgang. Flere oplysninger i [Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md).

Varer skal måske flyttes mellem placeringer, f.eks. på grund af interne operationer:

* En produktionsordre kræver komponenter leveret, eller den færdige varer lægges på lager.
* Lagerchefen vil optimere pladsen.
* Ikke-planlagte bevægelser til og fra handlinger.
* Genopfylde plukplaceringer eller produktionsplaceringer.
* Opdatere placeringsindhold.

Optælling, regulering og ompostering af varer kan omfatte lagerstedsopgaver, der skal udføres på lagerposter, før de kan blive synkroniseret med de tilknyttede vareposter. Flere oplysninger i [Tælle, justere og ompostere lagerbeholdning ved hjælp af kladder](inventory-how-count-adjust-reclassify.md).  

 Den følgende tabel indeholder en opgavesekvens med links til de artikler, der rummer beskrivelserne af opgaverne.

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Flytte varer mellem lokationer|[Overflytte lagerbeholdning mellem lokationer](inventory-how-transfer-between-locations.md)|
|Flytte varer mellem placeringer i grundlæggende lageropsætninger til enhver tid og uden kildedokumenter.|[Flytte varer i grundlæggende lageropsætninger](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)|
|Du kan bruge lagerbevægelseskladden til internt at plukke og lægge elementer på lager i avancerede lageropsætninger med styret pluk og læg på lager.|[Flytte varer i avancerede lageropsætninger](warehouse-how-to-move-items-in-advanced-warehousing.md)|  
|Omstrukturere lagerstedet med nye placeringskoder og nye karakteristika for placeringer og evt. flytte rundt på dem.|[Omstrukturere lagersteder](warehouse-how-to-restructure-warehouses.md)|  

## Se også

[Oversigt over Warehouse Management](design-details-warehouse-management.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
