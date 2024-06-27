---
title: Flere oplysninger om varetyper
description: 'Få mere at vide om de typer varer, du kan administrere i lageret, og hvordan typer påvirkes. Du kan regulere lagerværdien for en vare ved hjælp af FIFO eller gennemsnitlige kostmetoder, f.eks., når varepriser ændres af andre årsager end transaktioner.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.search.form: '9297, 5845, 30,'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Om varetyper

I feltet **Type** på siden **Varekort** kan du vælge, hvad varen bruges til i virksomheden, hvilket påvirker, hvordan du kan administrere varen i lageret. I følgende tabel vises og beskrives de tre typer varer, der er tilgængelige.

|Indstilling|Typisk formål|
|------|-----------|
|Lager|Fysiske ting som f. eks. cykler, telefoner og skriveborde, hvor du vil kunne bruge alle lagerprocesserne. Lagervarer kan også omfatte ikke-fysiske varer, f.eks. softwarelicenser og-abonnementer, hvis varerne har identifikationsnumre, f.eks. serienumre. Du kan spore vareværdier og disponering på lageret.|
|Ikke på lager|Som regel er varer, der ikke er på lager, fysiske ting, f.eks. bolte eller penne, som en virksomhed bruger, men som ikke kan spores fuldt ud på lageret. For eksempel fordi de er billige varer og kun bruges internt.|
|Tjeneste|En arbejdstidsenhed, f.eks. en konsulenttime, til begrænset brug i virksomheden.|

> [!NOTE]
> Typerne **Service** og **Ikke-lager** understøtter ikke sporing af lagerantal og -værdi. Derfor understøttes kun valgte transaktionstyper og -funktioner. Følgende tabel viser oversigt over de funktioner, de tre varetyper understøtter.

|Elementtype|Salg|Indkøb|Sagsforbrug|Serviceforbrug|Montageforbrug|Produktion Forbrug|Montageafgang|Produktionsafgang|Lokationsoverflytning|Fysisk optælling|Regulering af lagerværdi|Lagerkostmetode|Varesporing|Reservation|Lagersted|Skabelon|Ordreplanlægning|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Lagerbeholdning|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|
|Ikke på lager|Ja|Ja|Ja|Ja|Ja|Ja|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Ja|
|Tjeneste|Ja|Ja|Ja|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Ja|

## Kostmetoder for varetyper

Når du bogfører lagertransaktioner, registreres ændringer i antal og værdi på lageret i henholdsvis vareposterne og værdiposterne.

Du registrerer omkostningen af lagervarer i feltet **Kostbeløb (ikke-lager)** på siden **Værdiposter**. Når du afstemmer posten med finansposterne, vises kostprisen i feltet **Bogført kostværdi** . Du kan få mere at vide om lageromkostningsberegning ved at gå til [Designoplysninger: Kostmetoder](design-details-inventory-costing.md).

For ikke-lager og serviceartikler registreres omkostningen i feltet **Kostbeløb (ikke-lager)** på siden **Værdiposter**. For ikke-lager og serviceartikler er omkostningen angivet i salgs-, montage- og produktionsbilag og kladder. Angiv standardkostprisen i feltet **Kostpris** på siderne **Varekort** og **Lagervare (pr. lok.)**. Kostpriser for disse typer af varer afstemmes ikke med Finans.

## Katalog og serviceartikler

Du kan opsætte varer, som du tilbyder til dine kunder, men som du ikke vil administrere i dit system, før du begynder at sælge dem som katalogvarer. Selvom katalogvarer ligner almindelige varer af typen **Ikke-lager** i denne henseende, skal du ikke forveksle de to, fordi der er forskelle. Hvis du vil vide mere, skal du gå til [Arbejde med katalogvarer](inventory-how-work-nonstock-items.md).

Debitorvarer, du udfører servicerer, f.eks. en printer, kaldes serviceartikler. Serviceartikler har intet at gøre med almindelige varer eller katalogvarer. Servicekomponenterne kan dog være almindelige varer. Du kan finde flere oplysninger i [Konfigurere serviceartikler og serviceartikelkomponenter](service-how-setup-service-items.md).

## Se også

[Registrere nye varer](inventory-how-register-new-items.md)  
[Opsætning af lagerbeholdning](inventory-setup-inventory.md)  
[Administrere lageromkostninger](finance-manage-inventory-costs.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
