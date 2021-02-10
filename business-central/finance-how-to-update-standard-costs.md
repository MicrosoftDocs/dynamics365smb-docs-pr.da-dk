---
title: Sådan opdateres standardkostpriser | Microsoft Docs
description: Du skal regelmæssigt opdatere standardkostprisen for komponenter og akkumulere de nye omkostninger til den overordnede vare.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: faa5b0f7ffc30d0f575f9b6e61d925f9606b4581
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750651"
---
# <a name="update-standard-costs"></a>Opdatere standardkostpriser
Du skal regelmæssigt opdatere standardkostprisen for komponenter og akkumulere de nye omkostninger til den overordnede vare. Processen består normalt af følgende fire trin:  

1.  Opdatere omkostninger på komponent- og kapacitetsniveau. Du kan finde flere oplysninger i kørslen **Foreslå kostpris (standard)**.  
2.  Konsolidering og akkumulering af komponent- og kapacitetsomkostninger til beregning af de samlede fremstillings- eller montageomkostninger for varerne.  
3.  Implementere de standardkostpriser, der angives, når du kører de tidligere kørsler. Standardkostpriserne træder ikke i kraft, før de er implementeret. Du kan finde flere oplysninger i Implementer std.kostprisændringer.  
4.  Implementere ændringer for at opdatere feltet **Kostpris** på varekortet og udføre regulering af lagerværdi. Du kan finde flere oplysninger under [Regulere lagerbeholdningen](inventory-how-revalue-inventory.md).  

Du kan finde flere oplysninger i [Om beregning af standardkostpris](finance-about-calculating-standard-cost.md).  
## <a name="to-update-standard-costs"></a>Sådan opdateres standardkostpriser  
1.  Udfør kørslen **Juster kostpris - vareposter**.  
2.  Udfør kørslen **Bogfør lagerregulering**.  
3.  Åbn **Standardkostpriskladde**, og brug en eller flere af følgende funktioner:  

    1.  Udfør kørslen **Foreslå kostpris (standard)**.  
    2.  Gennemse resultaterne, og foretag de nødvendige ændringer.  
    3.  Udfør kørslen **Foreslå kapacitetkostpris (standard)**.  
    4.  Gennemse resultaterne, og foretag de nødvendige ændringer.
    5. Udfør kørslen **Akkum. standardkostpris**.
    6.  Gennemse resultaterne, og foretag de nødvendige ændringer.
    7.  Udfør kørslen **Implementer std.kostprisændringer**.  
4.  Gennemse og bogfør siden **Værdireguleringskladde** , som er blevet udfyldt med posterne fra det forrige trin i processen.  

## <a name="see-also"></a>Se også  
 [Om beregning af standardomkostning](finance-about-calculating-standard-cost.md)   
 [Administrere lageromkostninger](finance-manage-inventory-costs.md)   
 [Designoplysninger: Kostmetoder](design-details-costing-methods.md) [Finans](finance.md)  
 [Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
