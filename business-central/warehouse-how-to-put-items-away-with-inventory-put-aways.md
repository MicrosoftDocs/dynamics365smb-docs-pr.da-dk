---
title: 'Fremgangsmåde: Lægge varer på lager med Læg-på-lager'
description: 'Lær om, hvordan du kan bruge dokumentet Læg-på-lager til at registrere og bogføre læg-på-lager-og modtagelsesoplysninger.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 09/19/2023
ms.custom: bap-template
ms.search.forms: '7375,'
---
# Lægge varer på lager med Læg-på-lager (lager)

I [!INCLUDE[prod_short](includes/prod_short.md)] kan du modtage varer og indsætte dem på en af fire måder som beskrevet i følgende tabel.

|Metode|Indgående proces|Kræv modtagelse|Kræv læg-på-lager|Sværhedsgrad (få mere at vide på [Warehouse Management-oversigt](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bogfør lagermodtagelse og læg-på-lager fra ordrelinjen|||Ingen dedikeret lageraktivitet.|  
|B|Bogfør lagermodtagelse og læg-på-lager fra et læg-på-lager-dokument||Aktiveret|Basis: Ordre for ordre.|  
|U|Bogfør lagermodtagelse og læg-på-lager fra et lagermodtagelsesdokument|Aktiveret||Basis: Konsolideret modtagelse/levering for flere ordrer.|  
|D|Bogfør modtagelse fra et lagermodtagelsesdokument, og bogfør læg-på-lager fra lagerets læg-på-lager-dokument|Aktiveret|Aktiveret|Avanceret|  

Få mere at vide i [Udgående lagerstedsflow](design-details-inbound-warehouse-flow.md).

Denne artikel henviser til metode B i den foregående tabel.

Hvis lokationen er sat op til at kræve læg-på-lager, men ikke modtagelse, bruger du dokumentet **Læg-på-lager (lager)** til at registrere og bogføre læg-på-lager- og modtagelsesoplysninger for kildedokumenterne. Indgående kildedokumenter omfatter salgsordrer, købsreturvareordrer og indgående overflytninger.

> [!NOTE]
> Produktions- og montage-output repræsenterer også indgående kildedokumenter. Du kan finde flere oplysninger om lagerekspedition for interne indgående og udgående processer i [Designoplysninger: Internt lagerflow](design-details-internal-warehouse-flows.md).

Du kan oprette et læg-på-lager på tre måder:  

* Opret læg-på-lager-aktiviteten direkte fra selve kildedokumentet.  
* Du kan oprette læg-på-lager-aktiviteter for mange kildedokumenter samtidig ved hjælp af kørslen.  
* Opret læg-på-lager-aktiviteten i to trin ved først at frigive kildedokumentet for at gøre varerne disponible til at blive lagt på lager. Læg-på-lager-aktiviteten kan derefter oprettes fra siden **Læg-på-lager (lager)** på baggrund af kildedokumentet.  

## Sådan oprettes en læg-på-lager-aktivitet fra kildedokumentet

1. I kildedokumentet, som kan være en købsordre, salgsreturvareordre, indgående overflytningsordre eller produktionsordre, skal du vælge handlingen **Opret læg-på-lager/pluk (lager)**.  
2. Markér afkrydsningsfeltet **Opret læg-på-lager/pluk (lager)**.
3. Vælg knappen **OK**. Der oprettes en ny læg-på-lager-aktivitet.

## Sådan oprettes flere læg-på-lager-aktiviteter med en kørsel

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opret læg-på-lager/pluk (lager)**, og vælg derefter det relaterede link. 
2. Brug felterne **Kildedokument** og **Kildenr.** i oversigtspanelet **Lageranmodning** til at filtrere på bestemte typer dokumenter eller rækker af dokumentnumre. Du kan for eksempel oprette pluk til kun salgsordrer.
3. I oversigtspanelet **Indstillinger** skal du markere afkrydsningsfeltet **Opret læg-på-lager (lager)**.
4. Vælg knappen **OK**. De angivne læg-på-lager-aktiviteter oprettes.

## Sådan oprettes læg-på-lager i to trin

### Sådan anmoder du om en læg-på-lager-aktivitet ved at frigive kildedokumentet

Når du frigiver købsordrer, salgsreturvareordrer og indgående overflytningsordrer, bliver varerne i ordrerne disponible til at blive lagt på lager. Følgende fremgangsmåde beskriver, hvordan du kan gøre varerne på en købsordre klar til at blive lagt på lager.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **købsordrer**, og vælg derefter det relaterede link.
2. Vælg den købsordre, du vil frigive, og vælg derefter handlingen **Frigiv**.  

### Sådan oprettes en læg-på-lager-aktivitet ud fra kildedokumentet

En lagermedarbejder kan oprette en ny læg-på-lager-aktivitet baseret på det frigivne kildedokument.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Læg-på-lager (lager)**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. I feltet **Kildedokumentet** skal du vælge den kildedokumenttype, du lægger på lager for.  
4. Vælg kildedokumentet i feltet **Kildenr.**.  
5. Du kan også vælge handlingen **Hent kildedokument** for at vælge kildedokumentet på en liste over indgående kildedokumenter, der er klar til læg-på-lager på lokationen.  
6. Vælg knappen **OK** for at udfylde læg-på-lager-linjerne i overensstemmelse med det valgte kildedokument.  

## Sådan registreres læg-på-lager-aktiviteten

1. Åbn et tidligere oprettet læg-på-lager-dokument ved at vælge et på siden **Læg-på-lager akt. (lager)**.  
2. I feltet **Placeringskode** på læg-på-lager-linjerne, foreslås den placering, hvor varerne skal lægges på lager, pr. varens standardplacering. Om nødvendigt kan du ændre placeringen.  
3. Udfør læg-på-lager-aktiviteten, og angiv oplysningerne for den faktiske mængde, der er lagt på lager, i feltet **Håndteringsantal**.

    Hvis det er nødvendigt at placere varerne for en enkelt linje på mere end én placering, f.eks. fordi den angivne placering er fuld, skal du bruge funktionen **Opdel linje** i oversigtspanelet **Linjer**. Handlingen opretter en linje for det resterende antal til ekspedition.  
4. Når du har lagt varerne på lager, skal du vælge handlingen **Bogfør**.  

    * Bogføre modtagelsen af de kildedokumentlinjer, der er lagt på lager
    * Hvis lokationen anvender placeringer, oprettes der også lagerposter til bogføring af ændringer af placeringsantallet.

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## Se også

[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
