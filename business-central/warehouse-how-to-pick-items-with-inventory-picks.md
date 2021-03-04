---
title: Sådan plukkes varer med Pluk fra lager | Microsoft Docs
description: Når en lokation, du vil plukke fra, er sat op til at kræve pluk men ikke leverance, bruges plukdokumenterne til at registrere og bogføre pluk- og leveranceoplysninger for kildedokumenterne.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7b3dafdf2341567d2bf294065cf7508295e60aa3
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759763"
---
# <a name="pick-items-with-inventory-picks"></a>Plukke varer med Pluk fra lager

Når en lokation er sat op til at kræve pluk, men ikke leverance, skal du bruge siden **Pluk (lager)** til at registrere og bogføre pluk- og leveranceoplysninger for kildedokumenterne. De udgående kildedokumenter kan være en salgsordre, en købsreturvareordre, en udgående overflytning eller en produktionsordre, hvor komponenterne er klar til at blive plukket.

> [!NOTE]  
> Komponenter til montageordrer kan ikke plukkes eller bogføres med pluk. Brug i stedet siden **Flytning (lager)**. Du kan finde flere oplysninger i [Flytte komponenter til et handlingsområde i basislogistik](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).
>
> Når du plukker og leverer salgslinjemængder, der er monteret til ordren, skal du følge visse regler, når du opretter lagerpluklinjerne. Du kan finde flere oplysninger i afsnittet [Håndtere montage til ordre-varer i Pluk (lager)](#handling-assemble-to-order-items-with-inventory-picks).  

Du kan oprette et pluk på tre måder:  

- Opret plukaktiviteten i to trin ved først at anmode om et lagerpluk ved frigivelse af kildedokumentet. Dette signalerer til lageret, at kildedokument er klar til pluk. Pluk kan derefter oprettes fra vinduet på siden **Pluk (lager)** på baggrund af kildedokumentet.  
- Opret pluk direkte fra selve kildedokumentet.  
- Du kan oprette pluk for mange kildedokumenter samtidig ved hjælp af kørslen.  

## <a name="to-request-an-inventory-pick-by-releasing-the-source-document"></a>Sådan anmoder du om et lagerpluk ved at frigive kildedokumentet

I forbindelse med salgsordrer, købsreturvareordrer og udgående overflytningsordrer opretter du lageranmodningen ved at frigive ordren. Nedenfor kan du se, hvordan du gør det fra en salgsordre.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordre**, og vælg derefter det relaterede link.
2. Vælg den salgsordre, du vil frigive, og vælg derefter handlingen **Frigiv**.

I forbindelse med produktionsordrer opretter du automatisk lageranmodningen til pluk af komponenter, kaldet *træk* når status på produktionsordren ændres til **Frigivet**, eller når den frigivne produktionsordre oprettes. Du kan finde flere oplysninger i [Plukke til produktion eller montage](warehouse-how-to-pick-for-production.md).

Når lageranmodningen er oprettet, kan en lagermedarbejder, der er tildelt til plukning af varer, se, at kildedokumentet er klar til at blive plukket, og oprette et nyt plukdokument på basis af lageranmodningen.  

## <a name="to-create-an-inventory-pick-based-on-the-source-document"></a>Sådan oprettes et pluk på basis af kildedokumentet

Nu, hvor anmodningen er oprettet, kan lagermedarbejderen oprette et ny lagerpluk baseret på det frigivne kildedokument.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lagerpluk**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
    Sørg for, at feltet **Nr.** er udfyldt i oversigtspanelet **Generelt**.
3. I feltet **Kildedokumentet** skal du vælge den kildedokumenttype, du plukker fra.  
4. Vælg kildedokumentet i feltet **Kildenr.**.  
5. Du kan også vælge handlingen **Hent kildedokument** for at vælge kildedokumentet på en liste over udgående kildedokumenter, der er klar til plukning på lokationen.  
6. Vælg knappen **OK** for at udfylde pluklinjerne i overensstemmelse med det valgte kildedokument.  

## <a name="to-create-an-inventory-pick-from-the-source-document"></a>Sådan oprettes et pluk på basis af kildedokumentet

1. I kildedokumentet, som kan være en salgsordre, købsreturvareordre, udgående overflytningsordre eller produktionsordre, skal du vælge handlingen **Opret læg-på-lager/pluk (lager)**.
2. Markér afkrydsningsfeltet **Opret pluk (lager)**.  
3. Vælg knappen **OK**. Der oprettes et nyt lagerpluk.

## <a name="to-create-multiple-inventory-picks-with-a-batch-job"></a>Sådan oprettes flere pluk fra lager med en kørsel

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opret læg-på-lager/pluk (lager)**, og vælg derefter det relaterede link.  
2. Brug felterne **Kildedokument** og **Kildenr.** i oversigtspanelet **Lageranmodning** til at filtrere på bestemte typer dokumenter eller rækker af dokumentnumre. Du kan for eksempel oprette pluk til kun salgsordrer.  
3. I oversigtspanelet **Indstillinger** skal du markere afkrydsningsfeltet **Opret pluk (lager)**.
4. Vælg knappen **OK**. De angivne lagerpluk oprettes.

> [!NOTE]  
> Hvis du plukker og leverer salgslinjemængder, der er monteret til ordren, skal du følge visse regler, når du opretter lagerpluklinjerne. Du kan finde flere oplysninger i afsnittet [Håndtere montage til ordre-varer i Pluk (lager)](#handling-assemble-to-order-items-with-inventory-picks).  
>
> I grundlæggende lageropsætninger plukkes varer, der er monteret til salgsordrer, fra den tilknyttede salgsordre som beskrevet i dette emne. Du kan finde flere oplysninger i afsnittet [Håndtere montage til ordre-varer i Pluk (lager)](#handling-assemble-to-order-items-with-inventory-picks).  

## <a name="to-record-the-inventory-picks"></a>Sådan registreres lagerpluk

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lagerpluk**, og vælg derefter det relaterede link.  
2. I feltet **Placeringskode** på pluklinjerne, foreslås den placering, som varerne skal plukkes fra, pr. varens standardplacering. Du kan eventuelt ændre placeringen på denne side.  
3. Udfør plukaktiviteten, og angiv oplysningerne for den faktiske mængde, der er lagt på lager, i feltet **Håndteringsantal**.

    Hvis det er nødvendigt at plukke varerne for en enkelt linje fra mere end én placering, f.eks. fordi de ikke er tilgængelige på den angivne placering, skal du bruge funktionen **Opdel linje** i oversigtspanelet **Linjer**. Du kan finde flere oplysninger om opdeling af linjer i [Opdele lageraktivitetslinjer](warehouse-how-to-split-warehouse-activity-lines.md).  
4. Når du har plukket varerne, skal du vælge handlingen **Bogfør**.  

Bogføringsprocessen bogfører leverancen af de kildedokumentlinjer, der er plukket, og i forbindelse med produktionsordrer bogføres forbruget. Hvis lokationen anvender placeringer, oprettes der også lagerposter til bogføring af ændringer af placeringsantallet.  

## <a name="to-delete-inventory-pick-lines"></a>Sådan slettes pluklinjer for lager

Hvis varer på lagerpluk ikke er tilgængelige, kan du kan slette disse lagerpluklinjer, når du har bogført dem og derefter slette lagerplukdokumentet. Kildedokumentet, f.eks en salgsordre eller en produktionsordre, har derefter resterende varer, der skal plukkes, som kan opnås gennem et nyt lagerpluk senere, når varerne bliver disponible.  

> [!WARNING]  
> Denne proces er ikke mulig, hvis serienumre/lotnumre er angivet i kildedokument. For eksempel hvis en salgsordrelinje indeholder et serienummer/lotnummer, så slettes den varesporingsspecifikation, hvis en lagerpluklinje for serienummeret/lotnummeret slettes.  
>
> Hvis lagerpluklinjer har serienumre/lotnumre, der ikke er tilgængelige, skal du ikke slette de pågældende linjer. I stedet skal du ændre feltet **Håndteringsantal** til nul, bogføre de faktiske pluk og derefter slette lagerplukdokumentet. Dette garanterer, at lagerpluklinjerne for disse serie-/lotnumre kan genoprettes senere fra salgsordren.  

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Håndtering af montage til ordre-varer med pluk (lager)

Siden **Pluk (lager)** bruges også til at plukke og afsende salg, hvor varerne skal monteres, inden de kan leveres. Du kan finde flere oplysninger i [Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md).

Varer, der skal leveres, findes ikke fysisk i en placering, før de er monteret og bogført som afgang til en placering i montageområdet. Det betyder, at pluk af ordremontagevarer til levering følger en speciel strøm. Lagermedarbejderne fra en placering fragter montageelementerne til afsendelsesområdet og bogfører derefter lagerpluk. Den bogførte lagerpluk bogfører derefter montageafgang, komponentforbrug og salgsleverance.

Du kan konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] til automatisk at oprette en flytning (lager), når lagerpluk for varen montageelementet oprettes. Når du vil gøre det, skal du vælge feltet **Opret bevægelser automatisk** på siden **Montagekonfiguration**. Du kan finde flere oplysninger i [Flytte komponenter til et handlingsområde i basislogistik](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Lagerpluklinjer for salgsvarer oprettes på forskellige måder afhængigt af, om ingen, nogle eller alle salgslinjemængderne samles til ordre.

Ved almindeligt salg, hvor du bruger pluk fra lager til at bogføre leverancer af lagerantal, oprettes der én lagerpluklinje – eller flere, hvis varen lægges på flere placeringer – for hver salgsordrelinje. Denne pluklinje er baseret på mængden i feltet **Lever (antal)**.

I montage efter ordre-salg hvor hele mængden i salgsordrelinjen monteres efter ordre, oprettes der en lagerpluklinje for den mængde. Det betyder, at værdien i feltet Antal til montage svarer til værdien i feltet **Lever (antal)**. Feltet **Montage til ordre** vælges på linjen.

Hvis montageoutputflow er konfigureret for lokationen, så indsættes værdien i feltet **Pla.kode til ordremontagelev.** eller værdien i feltet **Placeringskode til fra-montage**, i den rækkefølge, i feltet **Placeringskode** i lagerpluklinjen.

Hvis en placeringskode ikke er angivet på salgsordrelinjen, og montageafgangsstrøm ikke er konfigureret for lokationen, så er feltet **Placeringskode** i lagerpluklinjen tomt. Lagermedarbejderen skal åbne siden **Placeringsindhold** og vælge den placering, hvor montageelementerne monteres.

I kombinationsscenarier, hvor en del af mængden først skal samles, og en anden skal plukkes fra lageret, oprettes minimum to lagerpluklinjer. En pluklinje er for ordremontageantal. De andre pluklinje afhænger af, hvilke placeringer der kan opfylde restantal fra lageret. Placeringskoder på de to linjer udfyldes på forskellige måder, som beskrevet for de to forskellige salgtyper. Du kan finde flere oplysninger i afsnittet "Kombinationsscenarier" i [Om Montage til ordre og Montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-also"></a>Se også

[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)  
[Montagestyring](assembly-assemble-items.md)  
[Gennemgang: Pluk og forsendelse i grundlæggende lageropsætninger](walkthrough-picking-and-shipping-in-basic-warehousing.md)  
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]