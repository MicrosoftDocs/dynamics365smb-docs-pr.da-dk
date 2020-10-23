---
title: Sådan oprettes rammemontageordrer | Microsoft Docs
description: Opret rammesalgsordrer for tilpassede montageelementer, før du regelmæssigt opretter de faktiske salgsordrer i overensstemmelse med rammeordreaftalen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 84232aadd133527d06ff0bf2b65490d5dfe8d651
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3917697"
---
# <a name="create-blanket-assembly-orders"></a>Oprette rammemontageordrer
Du kan bruge montagestyring til at tilpasse et montageelement på anmodning af en debitor under salgsprocessen. Du kan finde flere oplysninger i [Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md).  

 Som med enhver anden type emne, kan du også oprette rammesalgsordrer til tilpassede montagevarer før du regelmæssigt foretager faktiske salgsordrer i overensstemmelse med rammeordreaftale. Denne proces omfatter flere ekstra trin, når du sammenligner med oprettelse af en normal rammesalgsordre, og det bruger en variation af tilknyttet montageordre, som er en montagerammeordre.

> [!NOTE]  
>  Ligesom alle rammeordrer forecastes mængder på montagerammeordrer kun og er ikke operationelle, før de konverteres til faktiske montageordrer. Ordrefunktionalitet, som f.eks. disponeringsberegning, reservation og varesporing , er derfor ikke aktiv på rammemontageordrer.  

## <a name="to-create-a-blanket-assembly-order-for-an-assemble-to-order-item"></a>Sådan oprettes en rammemontageordre til en montage\-til\-ordre-vare  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rammesalgsordrer**, og vælg derefter det relaterede link.  
2. Opret en ny rammesalgsordre med en linje til et montageelement. Du kan finde flere oplysninger i [Oprette rammesalgsordrer](sales-how-to-create-blanket-sales-orders.md).  
3. Indtast den samlede mængde i feltet **Antal til montage til ordre** på rammemontageordrelinjen.

    > [!NOTE]  
    >  Du skal ikke oprette rammeordreaftaler for en delmængde. Derfor skal du angive det samme antal, som du har angivet i feltet **Antal** på rammeordrens salgsordrelinje.  

4. Vælg handlingen **Montage til ordre**, og vælg derefter handlingen **Montage til ordre-linjer**. Du kan også vælge feltet **Antal til montage til ordre** på linjen.  
5. På siden **Montage til ordre-linjer** kan du gennemse eller ændre linjerne til montageordren efter den rammeordreaftale, du har lavet med debitor. Hvis du vil se flere oplysninger, kan du vælge handlingen **Vis dokument** for at åbne den samlede rammemontageordre. Du kan ikke ændre indholdet af de fleste felter, og du kan ikke bogføre.  
6. Når du har reguleret montageordrelinjerne i overensstemmelse med rammeordreaftalen, skal du lukke siden **Montage til ordre-linjer** for at vende tilbage til siden **Rammesalgsordre**.  
7. Når debitor anmoder om at oprette en salgsordre, der er baseret på aftalte rammesalgsordre, skal du oprette en salgsordre for det aftalte montageelement eller elementer. Du kan finde flere oplysninger i [Oprette rammesalgsordrer](sales-how-to-create-blanket-sales-orders.md).

Den sammenkædede montagerammeordre og eventuelle tilpasninger er knyttet til den pågældende nye salgsordre for at forberede til montage for varen eller de varer, der skal sælges.  

## <a name="see-also"></a>Se også
[Oprette rammesalgsordrer](sales-how-to-create-blanket-sales-orders.md)  
[Montagestyring](assembly-assemble-items.md)  
[Arbejde med styklister](inventory-how-work-BOMs.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
