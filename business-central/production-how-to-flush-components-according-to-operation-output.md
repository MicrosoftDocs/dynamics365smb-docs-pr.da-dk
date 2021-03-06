---
title: Sådan udtrækkes komponenter i henhold til operationsafgang | Microsoft Docs
description: For varer, der er konfigureret med baglæns trækmetode, er standardfunktionsmåden at beregne og bogføre komponentforbrug, når du ændrer status på en frigivet produktionsordre til **Afsluttet**. Du kan finde flere oplysninger i Trækmetode.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f7f6c0c4be56c5f7e25f44063923cfe02e03e4c8
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759288"
---
# <a name="flush-components-according-to-operation-output"></a>Udtrække komponenter i henhold til operationsafgang
For varer, der er konfigureret med baglæns trækmetode, er standardfunktionsmåden at beregne og bogføre komponentforbrug, når du ændrer status på en frigivet produktionsordre til **Afsluttet**.  

Hvis du også definerer rutebindingskoder, forekommer beregning og bogføring, når hver operation er afsluttet, og den mængde, der rent faktisk er forbrugt i handlingen, der er bogført. Du kan finde flere oplysninger i [Oprette ruter](production-how-to-create-routings.md).  

Hvis f.eks. en produktionsordre om at fremstille 800 meter kræver 8 kg af en komponent, bogføres derefter, når du bogfører 200 meter som afgang, 2 kg automatisk som forbrug.  

Denne funktion er nyttig, af følgende årsager:  

-   **Lagerværdi** -værdiposterne for afgang og forbrug oprettes parallelt, efterhånden som produktionsordren skrider frem. Uden rutebindingskoder vil lagerværdien forøges efterhånden som afgangen bogføres, og derefter formindsk på et senere tidspunkt, når værdien af komponentforbruget bogføres sammen med den færdige produktionsordre.  
-   **Varedisponering** - med gradvis bogføring af forbrug, vil tilgængeligheden af komponentvarer være mere opdateret, hvilket er vigtigt for at opretholde den interne balance mellem efterspørgsel og udbud. Uden rutebindingskoder vil andre efterspørgsler efter komponenten mene, at den er tilgængelig, så længe der ventes på et forsinket bogføring af forbruget.  
-   **Just-in-Time** – med muligheden for at tilpasse produkter til debitorbehov, kan du minimere affald ved at sørge for, at arbejde og ændringer i systemet kun forekomme, når det er nødvendigt.  

Følgende procedure viser, hvordan du kombinerer Bagudtrækning og rutebindingskode, så den mængde, der udtrækkes for hver operation er proportional med den faktiske afgang af den afsluttede operation.  

## <a name="to-flush-components-according-to-operation-output"></a>Udtrække komponenter i henhold til operationsafgang  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Rediger**.  
3.  Vælg **Fremad** i feltet **Trækmetode** oversigtspanel under fanen **Genopfyldning**.  

    > [!NOTE]  
    >  Vælg **Pluk + Fremad**, hvis komponenten bruges på en placering, der er sat op til styret læg-på-lager og pluk.  

4.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Ruter**, og vælg derefter det relaterede link.  
5.  Definer rutebindingskoder for hver operation, der bruger komponenten. Du kan finde flere oplysninger i [Oprette ruter](production-how-to-create-routings.md).  
6.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Produktionsstykliste**, og vælg dernæst det relaterede link.  
7.  Definer rutebindingskoder fra hver forekomst af komponenten til den operation, hvor den forbruges.

    > [!IMPORTANT]  
    >  Komponenten skal have en rutebinding til den sidste operation i ruten.  

## <a name="see-also"></a>Se også  
[Oprette produktionsstyklister](production-how-to-create-production-boms.md)  
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Planlægning](production-planning.md)   
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]