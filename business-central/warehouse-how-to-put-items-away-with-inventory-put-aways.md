---
title: 'Fremgangsmåde: Lægge varer på lager med Læg-på-lager'
description: Læs om, hvordan du kan bruge dokumentet Læg-på-lager til at registrere og bogføre læg-på-lager-og modtagelsesoplysninger for kildedokumenterne.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: e28e565858f4dc6fc1e01c614914b0b1620c9659
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6438103"
---
# <a name="put-items-away-with-inventory-put-aways"></a>Lægge varer på lager med Læg-på-lager (lager)
Hvis lokationen er sat op til at kræve læg-på-lager, men ikke modtagelse, bruger du dokumentet **Læg-på-lager (lager)** til at registrere og bogføre læg-på-lager- og modtagelsesoplysninger for kildedokumenterne. Det indgående kildedokument kan være en købsordre, en salgsreturvareordre, en indgående overflytningsordre eller en montage- eller produktionsordre, hvis afgang er klar til at blive lagt på lager.  

Du kan oprette et læg-på-lager på tre måder:  

- Opret læg-på-lager-aktiviteten i to trin ved først at oprette en lageranmodning fra kildedokumentet, hvilket signalerer over for lagerstedet, at kildedokumentet er klar til at blive lagt på lager. Læg-på-lager-aktiviteten kan derefter oprettes fra siden **Læg-på-lager (lager)** på baggrund af kildedokumentet.  
- Opret læg-på-lager-aktiviteten direkte fra selve kildedokumentet.  
- Opret læg-på-lager-aktiviteter for mange kildedokumenter samtidig ved hjælp af en kørsel.  

## <a name="to-request-an-inventory-put-away-by-releasing-the-source-document"></a>Sådan anmoder du om en læg-på-lager-aktivitet ved at frigive kildedokumentet
I forbindelse med købsordrer, salgsreturvareordrer, indgående overflytningsordrer og montageordrer opretter du lageranmodningen ved at frigive ordren. Nedenfor kan du se, hvordan du gør det fra en købsordre.  

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **købsordrer**, og vælg derefter det relaterede link.
2. Vælg den købsordre, du vil frigive, og vælg derefter handlingen **Frigiv**.  

    I tilfælde af produktionsordrer kan du oprette lageranmodningen ved at oprette en indgående anmodning fra den frigivne produktionsordre.  
3.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Frigivne produktionsordrer**, og vælg derefter det relaterede link.  
4. Vælg handlingen **Opret indgående lageranmodning**.  

> [!NOTE]  
>  Du kan også oprette en indgående lageranmodning ved at markere afkrydsningsfeltet **Opret indgående anmodning**, når du opdaterer produktionsordren. Du kan finde flere oplysninger i [Forny eller omplanlægge produktionsordrer](production-how-to-replan-refresh-production-orders.md).  

Når lageranmodningen er oprettet, kan en lagermedarbejder, der er tildelt til læg-på-lager-opgaver, se, at kildedokumentet er klar til at blive lagt på lager, og oprette et nyt læg-på-lager-dokument på basis af lageranmodningen.  

## <a name="to-create-an-inventory-put-away-based-on-the-source-document"></a>Sådan oprettes en læg-på-lager-aktivitet ud fra kildedokumentet
Nu, hvor anmodningen er oprettet, kan lagermedarbejderen oprette en ny læg-på-lager-aktivitet baseret på det frigivne kildedokument.   
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Læg-på-lager (lager)**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. I feltet **Kildedokumentet** skal du vælge den kildedokumenttype, du lægger på lager for.  
4. Vælg kildedokumentet i feltet **Kildenr.**.  
5. Du kan også vælge handlingen **Hent kildedokument** for at vælge kildedokumentet på en liste over indgående kildedokumenter, der er klar til læg-på-lager på lokationen.  
6. Vælg knappen **OK** for at udfylde læg-på-lager-linjerne i overensstemmelse med det valgte kildedokument.  

## <a name="to-create-an-inventory-put-away-from-the-source-document"></a>Sådan oprettes en læg-på-lager-aktivitet fra kildedokumentet  
1.  I kildedokumentet, som kan være en købsordre, salgsreturvareordre, indgående overflytningsordre eller produktionsordre, skal du vælge handlingen **Opret læg-på-lager/pluk (lager)**.  
2. Markér afkrydsningsfeltet **Opret læg-på-lager/pluk (lager)**.
3. Vælg knappen **OK**. Der oprettes en ny læg-på-lager-aktivitet.

## <a name="to-create-multiple-inventory-put-aways-with-a-batch-job"></a>Sådan oprettes flere læg-på-lager-aktiviteter med en kørsel  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opret læg-på-lager/pluk (lager)**, og vælg derefter det relaterede link.  
2.  Brug felterne **Kildedokument** og **Kildenr.** i oversigtspanelet **Lageranmodning** på anmodningssiden til at filtrere på bestemte typer dokumenter eller rækker af dokumentnumre.  
3.  I oversigtspanelet **Indstillinger** skal du markere afkrydsningsfeltet **Opret læg-på-lager (lager)**.
4.  Vælg knappen **OK**. De angivne læg-på-lager-aktiviteter oprettes.

## <a name="to-record-the-inventory-put-away"></a>Sådan registreres læg-på-lager-aktiviteten  
1. Åbn et tidligere oprettet læg-på-lager-dokument ved at vælge et på siden **Læg-på-lager akt. (lager)**.  
2. I feltet **Placeringskode** på læg-på-lager-linjerne, foreslås den placering, hvor varerne skal lægges på lager, pr. varens standardplacering. Du kan eventuelt ændre placeringen på denne side.  
3. Udfør læg-på-lager-aktiviteten, og angiv oplysningerne for den faktiske mængde, der er lagt på lager, i feltet **Håndteringsantal**.

    Hvis det er nødvendigt at placere varerne for en enkelt linje på mere end én placering, f.eks. fordi den angivne placering er fuld, skal du bruge funktionen **Opdel linje** i oversigtspanelet **Linjer**. Du kan finde flere oplysninger om opdeling af linjer i [Opdele lageraktivitetslinjer](warehouse-how-to-split-warehouse-activity-lines.md).  
4. Når du har lagt varerne på lager, skal du vælge handlingen **Bogfør**.  

Når du bogfører, bogføres modtagelsen, eller afgangen i forbindelse med produktionsordrer, af de kildedokumentlinjer, der er lagt på lager, og hvis der anvendes placeringer på lokationen, oprettes der også lagerposter til bogføring af ændringerne af placeringsantal.

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Warehouse Management](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]