---
title: "Sådan bruges produktionskladdeenheden | Microsoft Docs"
description: "Hvis en vare lagerføres i én enhed, men produceres i en anden, skal produktionsordren bruge en produktionskladdeenhed til beregning af det rigtige antal komponenter. Produktionskladdeenheden kan f.eks. bruges til beregning, når den producerede vare lagerføres i enheder, men produceres i ton."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: c7c76ce91b58d6cdba09652c54696dc38a87f950
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-manufacturing-batch-units-of-measure"></a>Arbejde med produktionskladdeenheder
Hvis en vare lagerføres i én enhed, men produceres i en anden, kan der oprettes en produktionsordre, hvor der bruges en produktionskladdeenhed til beregning af det rigtige antal komponenter under kørslen af **Opdater produktionsordre**. Produktionskladdeenheden kan f.eks. bruges til beregning, når den producerede vare lagerføres i enheder, men produceres i ton.  

## <a name="to-create-a-production-bom-using-a-batch-unit-of-measure"></a>Sådan oprettes en produktionsstykliste vha. en kladdeenhed  
1.  Produktionskladdeenheden oprettes som en alternativ enhed i vinduet **Vareenheder** på varen, der skal produceres. Kladdeenheden erstatter ikke varens basisenhed.  
2.  Opret en produktionsstykliste til den vare, som du har oprettet produktionskladdeenheden til. Du kan finde flere oplysninger i [Oprette produktionsstyklister](production-how-to-create-production-boms.md).  
3.  Vælg produktionskladdeenheden i feltet **Enhedskode**.  
4.  For hver linje i produktionsstyklisten skal du angive det komponentantal i feltet **Antal pr.** , som er en forudsætning for oprettelsen af denne kladdeenhed.  
5.  Åbn vinduet **Varekort** til den tilhørende vare.  

    Vælg den produktionsstykliste, du har oprettet ovenfor i feltet **Produktionsstyklistenr.** i oversigtspanelet **Genopfyldning**.  
6.  Opret et produktionsordrehoved ved at bruge den vare, som du har oprettet produktionskladdeenheden til. Du kan finde flere oplysninger i [Oprette produktionsordrer](production-how-to-create-production-orders.md).  
7.  Vælg handlingen **Opdater**, og vælg derefter knappen **OK**.  

På oversigtspanelet **Linjer** skal du vælge handlingen **Linje** og derefter vælge handlingen **Komponenter** for at se resultatet. Nu beregnes det antal komponenter, som skal bruges til produktionsstyklisten i overensstemmelse med produktionskladdeenheden.  

## <a name="to-calculate-a-manufacturing-batch-unit-of-measure-on-a-production-order"></a>Sådan beregnes en produktionskladdeenhed til en produktionsordre  
1.  Opret et produktionsordrehoved ved at bruge den vare, som du har oprettet produktionskladdeenheden til.  
2.  I feltet **Varenr.** på produktionsordrelinjen skal du angive det samme varenummer, som du har angivet i hovedet.  
3.  Angiv det samme antal, som du har angivet i hovedet, i feltet **Antal**.  
4.  Vælg produktionskladdeenhedskoden i feltet **Enhedskode**.  
5.  Vælg handlingen **Opdater**.
6.  I oversigtspanelet **Beregn** skal du fjerne markeringen i afkrydsningsfeltet **Linjer**.  
7.  Vælg knappen **OK**.  
8.  På oversigtspanelet **Linjer** skal du vælge handlingen **Linje** og derefter vælge handlingen **Komponenter** for at se resultatet. Nu beregnes det antal komponenter, som skal bruges til produktionsstyklisten i overensstemmelse med produktionskladdeenheden.  

## <a name="see-also"></a>Se også  
[Oprette ruter](production-how-to-create-routings.md)  
[Oprette produktionsstyklister](production-how-to-create-production-boms.md)     
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Planlægning](production-planning.md)   
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

