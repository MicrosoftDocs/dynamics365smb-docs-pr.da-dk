---
title: 'Fremgangsmåde: Plukke varer med Pluk fra lager'
description: 'Få mere at vide om, hvordan du bruger pluk (lager) til at registrere og bogføre pluk-og leveringsoplysninger for kildedokumenter.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '931, 7377'
---
# Plukke varer med Pluk fra lager

I [!INCLUDE[prod_short](includes/prod_short.md)] kan du modtage varer og indsætte dem på en af fire måder som beskrevet i følgende tabel.

|Metode|Udgående proces|Kræv pluk|Kræv leverance|Sværhedsgrad (få mere at vide på [Warehouse Management-oversigt](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Bogfør pluk og leverance fra ordrelinjen|||Ingen dedikeret lageraktivitet.|  
|B|Bogfør pluk og leverance fra et lagerplukdokument|Aktiveret||Basis: Ordre for ordre.|  
|U|Bogfør pluk og leverance fra et lagerstedsleverancedokument||Aktiveret|Basis: Konsolideret modtagelse/levering for flere ordrer.|  
|D|Bogfør pluk fra et lagerstedsplukdokument, og bogfør leverance fra et lagerstedsleverancedokument|Aktiveret|Aktiveret|Avanceret|  

Få mere at vide på [Udgående lagerstedsflow](design-details-outbound-warehouse-flow.md).

Denne artikel henviser til metode B i den foregående tabel.

Når en lokation er sat op til at kræve pluk, men ikke leverance, skal du bruge siden **Pluk (lager)** til at registrere og bogføre pluk- og leveranceoplysninger for kildedokumenterne. Udgående kildedokumenter omfatter salgsordrer, købsreturvareordrer og udgående overflytninger.

> [!NOTE]
> Produktions-og montageordrer med komponentbehov repræsenterer også udgående kildedokumenter. Du kan finde flere oplysninger om lagerekspedition for interne indgående og udgående processer i [Designoplysninger: Internt lagerflow](design-details-internal-warehouse-flows.md).
>
> Selvom serviceordrer også er udgående kildedokumenter, understøtter de ikke gradvise kompleksitets basis, ordre for ordre.
>
> Når du plukker og leverer salgslinjemængder, der er monteret til ordren, skal du følge visse regler, når du opretter lagerpluklinjerne. Flere oplysninger i [Håndtering af montage til ordre-varer med pluk](#handling-assemble-to-order-items-with-inventory-picks).  

Du kan oprette et pluk på tre måder:

* Opret pluk direkte fra selve kildedokumentet.  
* Opret pluk for mange kildedokumenter samtidig ved hjælp af kørslen.
* Opret plukaktiviteten i to trin ved først at oprette en lageranmodning fra kildedokumentet, hvilket signalerer over for lagerstedet, at kildedokumentet er klar til at blive plukket.

Pluk kan derefter oprettes fra vinduet på siden **Pluk (lager)** på baggrund af kildedokumentet.  

## Sådan oprettes et pluk på basis af kildedokumentet

1. I kildedokumentet, som kan være en salgsordre, købsreturvareordre, udgående overflytningsordre eller produktionsordre, skal du vælge handlingen **Opret læg-på-lager/pluk (lager)**.
2. Markér afkrydsningsfeltet **Opret pluk (lager)**.  
3. Vælg knappen **OK**. Der oprettes et nyt lagerpluk.

## Sådan oprettes flere pluk fra lager med en kørsel

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opret læg-på-lager/pluk (lager)**, og vælg derefter det relaterede link.  
2. Brug felterne **Kildedokument** og **Kildenr.** i oversigtspanelet **Lageranmodning** til at filtrere på bestemte typer dokumenter eller rækker af dokumentnumre. Du kan for eksempel oprette pluk til kun salgsordrer.  
3. I oversigtspanelet **Indstillinger** skal du markere afkrydsningsfeltet **Opret pluk (lager)**.
4. Vælg knappen **OK**.

## Sådan oprettes pluk i to trin

### Sådan anmoder du om et lagerpluk ved at frigive kildedokumentet

I forbindelse med salgsordrer, købsreturvareordrer og udgående overflytningsordrer opretter du lageranmodningen ved at frigive ordren. Når ordren frigives, bliver varerne disponible til pluk.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.
2. Vælg den salgsordre, du vil frigive, og vælg derefter handlingen **Frigiv**.

### Sådan oprettes et pluk på basis af kildedokumentet

Når du frigiver en ordre, kan lagermedarbejderen oprette et lagerpluk.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Pluk fra lager**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. I feltet **Kildedokumentet** skal du vælge den kildedokumenttype, du plukker fra.  
4. Vælg kildedokumentet i feltet **Kildenr.**.  
5. Du kan også vælge handlingen **Hent kildedokument** for at vælge kildedokumentet på en liste over udgående kildedokumenter, der er klar til plukning på lokationen.  
6. Vælg knappen **OK** for at udfylde pluklinjerne i overensstemmelse med det valgte kildedokument.  

## Sådan registreres lagerpluk

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Plukliste (lager)**, og vælg derefter det relaterede link.  
2. I feltet **Placeringskode** på pluklinjerne, foreslås den placering, som varerne skal plukkes fra, pr. varens standardplacering. Du kan eventuelt ændre placeringen på denne side.  
3. Pluk varerne, og indtast det antal varer, der er plukket, i feltet **Håndteringsantal**.

    Hvis det er nødvendigt at placere varerne for en enkelt linje på mere end én placering, f.eks. fordi den angivne placering er fuld, skal du bruge funktionen **Opdel linje** i oversigtspanelet **Linjer**. Handlingen opretter en linje for det resterende antal til ekspedition.

4. Vælg handlingen **Bogfør**.  

    * Bogfør leverancen af de kildedokumentlinjer, der er blevet plukket.
    * Hvis lokationen anvender placeringer, oprettes der også lagerposter til bogføring af ændringer af placeringsantallet.  

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## Håndtering af montage til ordre-varer med pluk (lager)

Siden **Pluk (lager)** bruges også til at plukke og afsende salg, hvor varerne skal monteres, inden de kan leveres. Lær mere i [Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md)

Varer, der skal leveres, findes ikke fysisk i en placering, før de er monteret og bogført som afgang til en placering i montageområdet. Det betyder, at pluk af ordremontagevarer til levering følger et specielt flow.

1. Lagermedarbejderne fra en placering fragter montageelementerne til afsendelsesområdet og bogfører derefter lagerpluk.
2. Den bogførte lagerpluk bogfører derefter montageafgang, komponentforbrug og salgsleverance.

Du kan konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] til automatisk at oprette en flytning (lager), når lagerpluk for varen montageelementet oprettes. Du kan angive dette ved at vælge feltet **Opret bevægelser automatisk** på siden **Montagekonfiguration** Flere oplysninger i [Oprette grundlæggende lagersteder med handlingsområder](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md).

Lagerpluklinjer for salgsvarer oprettes på forskellige måder afhængigt af, om ingen, nogle eller alle salgslinjemængderne samles til ordre. I kombinationsscenarier, hvor en del af mængden først skal samles, og en anden skal plukkes fra lageret, oprettes minimum to lagerpluklinjer.

I montage efter ordre-salg hvor hele mængden i salgsordrelinjen monteres efter ordre, oprettes der en lagerpluklinje for den mængde. Det betyder, at værdien i feltet **Antal til montage** svarer til værdien i feltet **Lever (antal)**. Feltet **Montage til ordre** vælges på linjen.

Hvis en placeringskode ikke er angivet på salgsordrelinjen, og montageafgangsstrøm ikke er konfigureret for lokationen, så er feltet **Placeringskode** i lagerpluklinjen tomt.

* ***Pla.kode til ordremontagelev.** <!-- not applicable for inv pick-->
* **Placeringskode til fra-montage**

Hvis en placeringskode ikke er angivet på salgsordrelinjen, og montageafgangsstrøm ikke er konfigureret for lokationen, så er feltet **Placeringskode** i lagerpluklinjen tomt. Lagermedarbejderen skal åbne siden **Placeringsindhold** og vælge den placering, hvor montageelementerne monteres.

I kombinationsscenarier, hvor en del af mængden først skal samles, og en anden skal plukkes fra lageret, oprettes minimum to lagerpluklinjer.

* En pluklinje er for ordremontageantal. [!INCLUDE [prod_short](includes/prod_short.md)] bruger følgende felter i denne rækkefølge til at angive placeringskode: **Placeringskode**, **Pla.kode til ordremontagelev** og derefter **Fra-placeringskode**. Lagermedarbejderen skal åbne siden **Placeringsindhold** og vælge den placering, hvor montageelementerne monteres.  
* De andre pluklinje afhænger af, hvilke placeringer der kan opfylde restantal. Hvis varen opbevares på flere placeringer, oprettes der flere linjer. Denne pluklinje er baseret på mængden i feltet **Lever (antal)**.

> [!NOTE]  
> Hvis varerne er monteret efter ordre, opretter lagerpluk for den sammenkædede salgsordre en flytning (lager) for alle montagekomponenter.  

## Se også

[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Montagestyring](assembly-assemble-items.md)  
[Gennemgang: Pluk og forsendelse i grundlæggende lageropsætninger](walkthrough-picking-and-shipping-in-basic-warehousing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
