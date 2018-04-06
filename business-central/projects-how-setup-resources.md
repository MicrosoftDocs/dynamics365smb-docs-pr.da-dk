---
title: Angive ressourcekostpriser, priser og kapacitet | Microsoft Docs
description: For at bruge ressourcer og lette projektstyring skal du angive omkostninger og priser for individuelle ressourcer eller ressourcegrupper og angive ressourcekapacitet.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 982c250becec74472b89ae705057d1b34f95e338
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-resources"></a>Konfigurere ressourcer
For at kunne administrere ressourceaktiviteterne korrekt skal du oprette ressourcerne og de tilhørende omkostninger og priser. De sagsrelaterede pris-, rabat- og kostfaktorregler oprettes på jobkortet. Du kan angive omkostninger og priser for individuelle ressourcer, ressourcegrupper eller alle tilgængelige ressourcer i virksomheden.

Når der bruges eller sælges ressourcer i en sag, hentes de tilhørende priser og omkostninger fra de oplysninger, du har oprettet.

Du kan angive standardbeløbet pr. time, når ressourcen oprettes. Hvis du f.eks. bruger en bestemt maskine i fem timer i en sag, udregnes sagen ud fra beløbet pr. time.

## <a name="to-set-up-a-resource"></a>Sådan defineres en ressource
Opret et kort for hver ressource, du vil bruge i projekter.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ressourcer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-a-resource-group"></a>Sådan oprettes en ressourcegruppe
Du kan samle flere forskellige ressourcer i en ressourcegruppe. Ressourcegruppens kapaciteter og budgetter bliver akkumuleret fra de enkelte ressourcer i gruppen. Du kan også indtaste kapaciteter for ressourcegrupper, enten uafhængigt af de akkumulerede værdier eller som supplement til dem.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ressourcer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld felterne efter behov.

## <a name="to-set-capacity-for-a-resource"></a>Sådan angives kapaciteten for en ressource
For at beregne, hvor lang tid en ressource kan bruge på sager, skal der først ressourcenes kapacitet først angives som disponible tid pr. periode i arbejdskalenderen. Denne opsætning anvendes, når du udfylder sagsplanlægningslinjer, som indeholder ressourcen. Du kan finde flere oplysninger i [Oprette sager](projects-how-create-jobs.md).

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ressourcer**, og vælg derefter det relaterede link.
2. Åbn det relevante ressourcekort, og vælg derefter handlingen **Ressourcekapacitet**.
3. I vinduet **Ressourcekapacitet** feltet **Vis efter** skal du angive periodens længde, f.eks **Dag**, som vises i kolonnerne på oversigtspanelet **Matrix for ressourcekapacitet**.
4. For hver ressource på en linje skal du for hver periode i kolonnerne angive det antal timer, hvor ressourcen er tilgængelig.
5. Du kan også angive ressourcens ugentlige kapacitet med en startdato og en slutdato ved at vælge handlingen **Angiv kapacitet**.
6. I vinduet **Ressourcekap.indstillinger** skal du udfylde felterne efter behov.
7. Vælg handlingen **Opdater kapacitet**. Vinduet **Ressourcekapacitet** opdateres med den angivne kapacitet.
8. Luk vinduet.

## <a name="to-set-up-alternate-resource-costs"></a>Sådan angives ressourcekostpriser
Udover de omkostninger, der er angivet på ressourcekortet, kan du oprette alternative omkostninger for hver ressource. Hvis en medarbejder f.eks. har en højere timesats for overarbejde, kan du i denne tabel oprette en ressourcekostpris for overtidsbetalingen. Den alternative kostpris, du angiver for ressourcen, tilsidesætter kostprisen på ressourcekortet, når du bruger ressourcen i ressourcekladden.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ressourcer**, og vælg derefter det relaterede link.  
2. Vælg ressource, som du vil angive en eller flere alternative omkostninger for, og vælg derefter handlingen **Kostpriser**.  
3. I vinduet **Ressourcekostpriser** skal du udfylde felterne på en linje efter behov.  
4. Gentag trin 3 for hver alternativ ressourcekostpris, du vil oprette.

**Bemærk**! Åbn vinduet **Ressourcekostpriser** og udfyld felterne for at angive ressourcekostpriser, der kan anvendes til alle ressourcer og ressourcegrupper.

## <a name="to-set-up-alternate-resource-prices"></a>Sådan angives ressourcepriser
Udover den pris, der er angivet på ressourcekortet, kan du oprette alternative priser for hver ressource. Alternative priser kan være betingede. De kan være betinget af, om ressourcen anvendes med et bestemt job eller en bestemt arbejdstype.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ressourcer**, og vælg derefter det relaterede link.
2. Vælg ressource, som du vil angive en eller flere alternative priser for, og vælg derefter handlingen **Priser**.
3. I vinduet **Ressourcepriser** skal du udfylde felterne på en linje efter behov.
4. Gentag trin 3 for hver alternativ ressourcepris, du vil oprette.

## <a name="see-also"></a>Se også
[Konfigurere projektstyring](projects-setup-projects.md)  
[Projektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)      
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

