---
title: "Sådan oprettes tilbud på montage til ordre-salg | Microsoft Docs"
description: "Du kan bruge montagestyring til at tilpasse et montageelement på anmodning af en debitor under salgsprocessen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4b91b8a0ee359c1dc8dc4507cade6b635dace644
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="quote-an-assemble-to-order-sale"></a>Oprette tilbud på montage til ordre-salg
Du kan bruge montagestyring til at tilpasse et montageelement på anmodning af en debitor under salgsprocessen. Du kan finde flere oplysninger i [Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md).  

Du kan også oprette et salgstilbud for en tilpasset montageelement, som når du sælger en anden type emne, før det konverteres til en salgsordre. Denne proces omfatter flere ekstra trin, når du sammenligner med oprettelse af et normalt salgstilbud, og det bruger en variation af tilknyttet montageordre, som er et montagetilbud.

> [!NOTE]  
>  Ligesom alle typer tilbud bruges mængderne med montagetilbud ikke i forbindelse med tilgængelighed, planlægning eller reservationer.  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a>Sådan oprettes et salgstilbud til et montage efter ordre-element  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgstilbud**, og vælg derefter det relaterede link.  
2.  Opret en ny salgstilbudslinje med en linje til et montageelement. Du kan finde flere oplysninger under [Fremsætte tilbud](sales-how-make-offers.md).  
3.  I feltet **Antal til montage efter ordre** skal du angive den samlede mængde.

    > [!NOTE]  
    >  Du bør ikke give tilbud på en delmængde. Derfor skal du angive det samme antal, som du har angivet i feltet **Antal** på salgstilbudslinjen.  

4.  På oversigtspanelet **Linjer** skal du vælge **Linje**, vælg **Montage efter ordre**, og vælg derefter **Montage efter ordre-linjer**. Du kan også vælge feltet **Antal til montage efter ordre** på linjen.  
5.  I vinduet **Montage efter ordre-linjer** kan du gennemse eller ændre linjerne til montageordre efter det tilbud, som kunden anmoder om. Hvis du vil se flere oplysninger, kan du vælge handlingen **Vis dokument** for at åbne den samlede rammetilbudsordre. Du kan ikke ændre indholdet af de fleste felter, og du kan ikke bogføre.  
6.  Når du har reguleret montageordrelinjerne i overensstemmelse med tilbuddet, skal du lukke vinduet **Montage efter ordre-linjer** for at vende tilbage til vinduet **Salgstilbud**.  
7.  Hvis debitor accepterer tilbuddet, kan du oprette en salgsordre for det tilbudte montageelement. Du kan finde flere oplysninger under [Fremsætte tilbud](sales-how-make-offers.md). Det sammenkædede montagetilbud og eventuelle tilpasninger er knyttet til den pågældende nye salgsordre for at forberede til montage af varen eller de varer, der skal sælges.  

## <a name="see-also"></a>Se også  
[Montagestyring](assembly-assemble-items.md)  
[Arbejde med styklister](inventory-how-work-BOMs.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

