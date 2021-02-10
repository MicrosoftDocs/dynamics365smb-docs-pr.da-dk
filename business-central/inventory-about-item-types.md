---
title: Om varetyper | Microsoft Docs
description: Du kan regulere lagerværdien for en vare ved hjælp af FIFO eller gennemsnitlige kostmetoder, f.eks., når varepriser ændres af andre årsager end transaktioner.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b3c9b79701296cd21492752e94b2a0ec7848658b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746312"
---
# <a name="about-item-types"></a>Om varetyper
I feltet **Type** på siden **Varekort** kan du vælge, hvad varen bruges til i virksomheden, og dermed hvordan den håndteres i systemet. Der er tre muligheder:

|Indstilling|Typisk formål|
|------|-----------|
|Lagerbeholdning|En fysisk enhed, f.eks. en cykel, til brug i hele virksomheden.|
|Ikke-lager|En fysisk enhed, f.eks. en bolt, til begrænset brug i virksomheden, f.eks. fordi varen kun bruges internt og er en lav pris.|
|Tjeneste|En arbejdstidsenhed, f.eks. en konsulenttime, til begrænset brug i virksomheden.|

Typen **Lagerbeholdning** omfatter fuld sporing af lagerantal og -værdi. Derfor understøttes alle varetransaktionstyper, og varer af typen Lagerbeholdning kan bruges sammen med alle funktioner til håndtering af varer.

Typerne **Service** og **Ikke-lager** involverer ikke sporing af lagerantal og -værdi. Derfor understøttes kun valgte transaktionstyper og -funktioner.

De tre varetyper understøtter hver især følgende funktioner.

|Elementtype|Salg|Indkøb|Sagsforbrug|Serviceforbrug|Montageforbrug|Produktion Forbrug|Montageafgang|Produktionsafgang|Lokationsoverflytning|Fysisk optælling|Regulering af lagerværdi|Lagerkostmetode|Varesporing|Reservation|Lagersted|Planlægning|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Lagerbeholdning|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|
|Ikke-lager|Ja|Ja|Ja|Ja|Ja|Ja|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|
|Tjeneste|Ja|Ja|Ja|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|

## <a name="costing-methods-for-types-of-items"></a>Kostmetoder for varetyper
Når du bogfører lagertransaktioner, registreres ændringer i antal og værdi på lageret i henholdsvis vareposterne og værdiposterne. 

For lagervarer registreres omkostningen i feltet **Kostbeløb (faktisk)** på siden **Værdiposter**, og når den afstemmes med Finans, vises omkostningen i feltet **Bogført kostværdi**. Du kan finde flere oplysninger i [Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md).

For ikke-lager og serviceartikler registreres omkostningen i feltet **Kostbeløb (ikke-lager)** på siden **Værdiposter**. For ikke-lager og serviceartikler er omkostningen angivet i salgs-, montage- og produktionsbilag og kladder. Standardkostprisen kan angives i feltet **Kostpris** på siderne **Varekort** og **Lagervare (pr. lok.)**. Kostpriser for disse typer af varer afstemmes ikke med Finans. 

## <a name="catalog-and-service-items"></a>Katalog og serviceartikler
Varer, som du tilbyder til dine kunder, men som du ikke vil administrere i dit system, før du begynder at sælge dem, kan oprettes som katalogvarer. Katalogvarer må ikke forveksles med almindelige varer af typen Ikke-lager. Du kan finde flere oplysninger under [Arbejde med katalogvarer](inventory-how-work-nonstock-items.md).

Kunders varer, du udfører reparation på, f.eks. en printer, kaldes serviceartikler. Serviceartikler har intet at gøre med almindelige varer eller katalogvarer. Servicekomponenterne kan dog være almindelige varer. Du kan finde flere oplysninger i [Konfigurere serviceartikler og serviceartikelkomponenter](service-how-setup-service-items.md).

## <a name="see-also"></a>Se også
[Registrere nye varer](inventory-how-register-new-items.md)  
[Opsætning af lagerbeholdning](inventory-setup-inventory.md)  
[Administrere lageromkostninger](finance-manage-inventory-costs.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
