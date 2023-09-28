---
title: Flere oplysninger om varetyper
description: 'Du kan regulere lagerværdien for en vare ved hjælp af FIFO eller gennemsnitlige kostmetoder, f.eks., når varepriser ændres af andre årsager end transaktioner.'
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '9297, 5845, 30,'
ms.date: 06/16/2021
ms.author: bholtorf
---
# <a name="about-item-types"></a>Om varetyper
I feltet **Type** på siden **Varekort** kan du vælge, hvad varen bruges til i virksomheden, hvilket påvirker, hvordan du kan administrere varen i lageret. I følgende tabel vises og beskrives de tre typer varer, der er tilgængelige.

|Indstilling|Typisk formål|
|------|-----------|
|Lager|Fysiske ting som f. eks. cykler, telefoner og skriveborde, hvor du vil kunne bruge alle lagerprocesserne. Det kan også omfatte ikke-fysiske varer, f. eks. softwarelicenser og-abonnementer, hvis varerne har identifikationsnumre, f. eks. serienumre. Du kan spore vareværdier og disponering på lageret.|
|Ikke-lager|Som regel er varer, der ikke er på lager, fysiske ting, f. eks. bolte eller penne, som en virksomhed bruger, men som ikke kan spores fuldt ud på lageret. F. eks. fordi de er billige varer og kun bruges internt.|
|Tjeneste|En arbejdstidsenhed, f.eks. en konsulenttime, til begrænset brug i virksomheden.|

> [!NOTE]
> Typerne **Service** og **Ikke-lager** understøtter ikke sporing af lagerantal og -værdi. Derfor understøttes kun valgte transaktionstyper og -funktioner.

Følgende tabel viser oversigt over de funktioner, de tre varetyper understøtter.

|Elementtype|Salg|Indkøb|Sagsforbrug|Serviceforbrug|Montageforbrug|Produktion Forbrug|Montageafgang|Produktionsafgang|Lokationsoverflytning|Fysisk optælling|Regulering af lagerværdi|Lagerkostmetode|Varesporing|Reservation|Lagersted|Skabelon|Ordreplanlægning|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Lagerbeholdning|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|
|Ikke på lager|Ja|Ja|Ja|Ja|Ja|Ja|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Ja|
|Tjeneste|Ja|Ja|Ja|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Ja|

## <a name="costing-methods-for-types-of-items"></a>Kostmetoder for varetyper
Når du bogfører lagertransaktioner, registreres ændringer i antal og værdi på lageret i henholdsvis vareposterne og værdiposterne. 

For lagervarer registreres omkostningen i feltet **Kostbeløb (faktisk)** på siden **Værdiposter**, og når den afstemmes med Finans, vises omkostningen i feltet **Bogført kostværdi**. Du kan finde flere oplysninger i [Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md).

For ikke-lager og serviceartikler registreres omkostningen i feltet **Kostbeløb (ikke-lager)** på siden **Værdiposter**. For ikke-lager og serviceartikler er omkostningen angivet i salgs-, montage- og produktionsbilag og kladder. Standardkostprisen kan angives i feltet **Kostpris** på siderne **Varekort** og **Lagervare (pr. lok.)**. Kostpriser for disse typer af varer afstemmes ikke med Finans. 

## <a name="catalog-and-service-items"></a>Katalog og serviceartikler
Varer, som du tilbyder til dine kunder, men som du ikke vil administrere i dit system, før du begynder at sælge dem, kan oprettes som katalogvarer. Katalogvarer må ikke forveksles med almindelige varer af typen Ikke-lager. Du kan finde flere oplysninger i [Arbejde med katalogvarer](inventory-how-work-nonstock-items.md).

Kunders varer, du udfører reparation på, f.eks. en printer, kaldes serviceartikler. Serviceartikler har intet at gøre med almindelige varer eller katalogvarer. Servicekomponenterne kan dog være almindelige varer. Du kan finde flere oplysninger i [Konfigurere serviceartikler og serviceartikelkomponenter](service-how-setup-service-items.md).

## <a name="see-also"></a>Se også
[Registrere nye varer](inventory-how-register-new-items.md)  
[Opsætning af lagerbeholdning](inventory-setup-inventory.md)  
[Administrere lageromkostninger](finance-manage-inventory-costs.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
