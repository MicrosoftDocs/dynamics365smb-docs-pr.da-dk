---
title: Workflow | Microsoft Docs
description: Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 95290ba7170e2390e83d4b12e5d988760c2f3c5f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752921"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Workflows i Dynamics 365 Business Central

Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin.  

 På siden **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne. Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder. Du definerer arbejdsgangstrin ved at udfylde felter om arbejdsganglinjer fra faste lister over hændelses- og svarværdier, der repræsenterer scenarier, der understøttes af programkoden.  

 Den generiske version af [!INCLUDE[prod_short](includes/prod_short.md)] indeholder en række forudkonfigurerede workflows, som repræsenteres af workflowskabeloner, som du kan kopiere for at oprette workflows. Koden for workflowskabeloner, som er tilføjet af Microsoft, har "MS" foran som f.eks. i "MS-". Du kan finde flere oplysninger på listen med workflowskabeloner på siden Workflowskabeloner.  

 Hvis et virksomhedsscenarie kræver en workflowhændelse eller et svar, der ikke understøttes, skal du enten bruge Power Automate eller en Microsoft-partner til at tilpasse programkoden. Du kan finde flere oplysninger under [Bruge [!INCLUDE[prod_short](includes/prod_short.md)] i et automatisk workflow](across-how-use-financials-data-source-flow.md).

Alle workflowskabeloner, som du opretter med, Power Automate, føjes til listen over workflowskabeloner i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Bruge Business Central i et automatisk workflow](across-how-use-financials-data-source-flow.md).  

 Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.  

|**For at**|**Skal du se**|  
|------------|-------------|  
|Oprette arbejdsgangbrugere, angive, hvordan brugere modtager notifikationer, og oprette nye arbejdsgange. Implementer de krævede arbejdsgangelementer ved at tilpasse programkoden for nye arbejdsgange for ikke-understøttede scenarier.|[Opsætte workflows](across-set-up-workflows.md)|  
|Aktiver arbejdsgange, behandl meddelelser i arbejdsgangen, herunder godkendelser og godkendelsesanmodninger om at udføre trin i en arbejdsgang. Arkiver og slet arbejdsgange.|[Anvende workflows](across-use-workflows.md)|  

## <a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Administrere projekter](projects-manage-projects.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
