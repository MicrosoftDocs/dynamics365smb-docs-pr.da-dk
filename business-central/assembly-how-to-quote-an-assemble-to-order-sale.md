---
title: "Sådan oprettes tilbud på montage til ordre-salg | Microsoft Docs"
description: "Du kan bruge montagestyring til at tilpasse et montageelement på anmodning af en debitor under salgsprocessen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 046a42582dc66368fded90a4bb45add71a95d979
ms.openlocfilehash: 497d19dfdc8c972ff22aa0bcb65d96791bc8390e
ms.contentlocale: da-dk
ms.lasthandoff: 07/02/2018

---
# <a name="quote-an-assemble-to-order-sale"></a>Oprette tilbud på montage til ordre-salg
Du kan bruge montagestyring til at tilpasse et montageelement på anmodning af en debitor under salgsprocessen. Du kan finde flere oplysninger i [Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md).  

Du kan også oprette et salgstilbud for en tilpasset montageelement, som når du sælger en anden type emne, før det konverteres til en salgsordre. Denne proces omfatter flere ekstra trin, når du sammenligner med oprettelse af et normalt salgstilbud, og det bruger en variation af tilknyttet montageordre, som er et montagetilbud.

> [!NOTE]  
>  Ligesom alle typer tilbud bruges mængderne med montagetilbud ikke i forbindelse med tilgængelighed, planlægning eller reservationer.  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a>Sådan oprettes et salgstilbud til et montage efter ordre-element  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgstilbud**, og vælg derefter det relaterede link.  
2.  Opret en ny salgstilbudslinje med en linje til et montageelement. Der er flere oplysninger i [Give salgstilbud](sales-how-make-offers.md).  
3.  I feltet **Antal til montage efter ordre** skal du angive den samlede mængde.

    > [!NOTE]  
    >  Du bør ikke give tilbud på en delmængde. Derfor skal du angive det samme antal, som du har angivet i feltet **Antal** på salgstilbudslinjen.  

4.  På oversigtspanelet **Linjer** skal du vælge **Linje**, vælg **Montage efter ordre**, og vælg derefter **Montage efter ordre-linjer**. Du kan også vælge feltet **Antal til montage efter ordre** på linjen.  
5.  I vinduet **Montage efter ordre-linjer** kan du gennemse eller ændre linjerne til montageordre efter det tilbud, som kunden anmoder om. Hvis du vil se flere oplysninger, kan du vælge handlingen **Vis dokument** for at åbne den samlede rammetilbudsordre. Du kan ikke ændre indholdet af de fleste felter, og du kan ikke bogføre.  
6.  Når du har reguleret montageordrelinjerne i overensstemmelse med tilbuddet, skal du lukke vinduet **Montage efter ordre-linjer** for at vende tilbage til vinduet **Salgstilbud**.  
7.  Hvis debitor accepterer tilbuddet, kan du oprette en salgsordre for det tilbudte montageelement. Der er flere oplysninger i [Give salgstilbud](sales-how-make-offers.md). Det sammenkædede montagetilbud og eventuelle tilpasninger er knyttet til den pågældende nye salgsordre for at forberede til montage af varen eller de varer, der skal sælges.  

## <a name="see-also"></a>Se også  
[Montagestyring](assembly-assemble-items.md)  
[Arbejde med styklister](inventory-how-work-BOMs.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

