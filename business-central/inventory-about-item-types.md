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
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: ab3da8450586928a02d17ccce14c704ed6d7c8fe
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182392"
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

> [!NOTE]
> Varer, som du tilbyder til dine kunder, men som du ikke vil administrere i dit system, før du begynder at sælge dem, kan oprettes som katalogvarer. Katalogvarer må ikke forveksles med almindelige varer af typen Ikke-lager. Du kan finde flere oplysninger under [Arbejde med katalogvarer](inventory-how-work-nonstock-items.md).

> [!NOTE]
> Kunders varer, du udfører reparation på, f.eks. en printer, kaldes serviceartikler. Serviceartikler har intet at gøre med almindelige varer eller katalogvarer. Servicekomponenterne kan dog være almindelige varer. Du kan finde flere oplysninger i [Konfigurere serviceartikler og serviceartikelkomponenter](service-how-setup-service-items.md).

## <a name="see-also"></a>Se også
[Registrere nye varer](inventory-how-register-new-items.md)  
[Opsætning af lagerbeholdning](inventory-setup-inventory.md)  
[Administrere lageromkostninger](finance-manage-inventory-costs.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
