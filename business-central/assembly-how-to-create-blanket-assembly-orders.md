---
title: Oprette rammemontageordrer
description: 'Opret rammesalgsordrer for tilpassede montageelementer, før du regelmæssigt opretter de faktiske salgsordrer i overensstemmelse med rammeordreaftalen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Oprette rammemontageordrer

Du kan bruge montagestyring til at tilpasse et montageelement på anmodning fra en kunde under salgsprocessen. Du kan finde flere oplysninger i [Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md).  

 Som med enhver anden type emne, kan du også oprette rammesalgsordrer til tilpassede montagevarer før du regelmæssigt foretager faktiske salgsordrer i overensstemmelse med rammeordreaftale. Denne proces omfatter flere ekstra trin, når du sammenligner med oprettelse af en normal rammesalgsordre, og det bruger en variation af tilknyttet montageordre, som er en montagerammeordre.

> [!NOTE]  
>  Ligesom alle rammeordrer forecastes mængder på montagerammeordrer kun og er ikke operationelle, før de konverteres til faktiske montageordrer. Ordrefunktionalitet, som f.eks. disponeringsberegning, reservation og varesporing , er derfor ikke aktiv på rammemontageordrer.  

## Sådan oprettes en rammemontageordre til en montage\-til\-ordre-vare  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Rammesalgsordrer**, og vælg derefter det relaterede link.  
2. Opret en ny rammesalgsordre med en linje til et montageelement. Du kan finde flere oplysninger i [Oprette rammesalgsordrer](sales-how-to-create-blanket-sales-orders.md).  
3. Indtast den samlede mængde i feltet **Antal til montage til ordre** på rammemontageordrelinjen.

    > [!NOTE]  
    >  Du skal ikke oprette rammeordreaftaler for en delmængde. Derfor skal du angive det samme antal, som du har angivet i feltet **Antal** på rammeordrens salgsordrelinje.  

4. Vælg handlingen **Montage til ordre**, og vælg derefter handlingen **Montage til ordre-linjer**. Du kan også vælge feltet **Antal til montage til ordre** på linjen.  
5. På siden **Montage til ordre-linjer** kan du gennemse eller ændre linjerne til montageordren efter den rammeordreaftale, du har lavet med debitor. Hvis du vil se flere oplysninger, kan du vælge handlingen **Vis dokument** for at åbne den samlede rammemontageordre. Du kan ikke ændre indholdet af de fleste felter, og du kan ikke bogføre.  
6. Når du har reguleret montageordrelinjerne i overensstemmelse med rammeordreaftalen, skal du lukke siden **Montage til ordre-linjer** for at vende tilbage til siden **Rammesalgsordre**.  
7. Når debitor anmoder om at oprette en salgsordre, der er baseret på aftalte rammesalgsordre, skal du oprette en salgsordre for det aftalte montageelement eller elementer. Du kan finde flere oplysninger i [Oprette rammesalgsordrer](sales-how-to-create-blanket-sales-orders.md).

Den sammenkædede montagerammeordre og eventuelle tilpasninger er knyttet til den pågældende nye salgsordre for at forberede til montage for varen eller de varer, der skal sælges.  

## Se også

[Oprette rammesalgsordrer](sales-how-to-create-blanket-sales-orders.md)  
[Montagestyring](assembly-assemble-items.md)  
[Arbejde med montagestyklister](assembly-how-work-assembly-boms.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]