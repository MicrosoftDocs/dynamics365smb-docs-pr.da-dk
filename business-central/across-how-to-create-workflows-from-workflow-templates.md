---
title: Sådan opretter du workflows ud fra workflowskabeloner | Microsoft Docs
description: For at spare tid ved oprettelse af nye workflows kan du oprette workflows ud fra workflowskabeloner.
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
ms.openlocfilehash: 407bf7cd60416a178e9ec8a5d0b154a7583e87e1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754838"
---
# <a name="create-workflows-from-workflow-templates"></a>Oprette workflows ud fra workflowskabeloner
For at spare tid ved oprettelse af nye workflows kan du oprette workflows ud fra workflowskabeloner.  

 Workflowskabeloner er workflows, som ikke kan redigeres, og som findes i den generiske version af [!INCLUDE[prod_short](includes/prod_short.md)]. Koderne for workflowskabeloner, som er tilføjet af Microsoft, har "MS" foran som f.eks. i "MS-".  

 En anden måde til hurtigt at oprette et workflow på er at importere et eksisterende workflow, som du har på en fil uden for [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Eksportere og importere workflows](across-how-to-export-and-import-workflows.md).  

På siden **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne. Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder. Du definerer workflowtrin ved at udfylde felter om workflowlinjer fra faste lister over hændelses- og responsværdier, der repræsenterer scenarier, der understøttes af programkoden. Du kan finde flere oplysninger i [Oprette arbejdsgange](across-how-to-create-workflows.md).  

## <a name="to-create-a-workflow-from-workflow-template"></a>Sådan opretter du fra et workflow ud fra en workflowskabelon  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Arbejdsgange**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Opret workflow fra skabelon**. Siden **Workflowskabeloner** åbnes.  
3.  Vælg et workflow, og vælg derefter knappen **OK**.  

     Siden **Workflow** åbnes for et nyt workflow, der indeholder alle oplysninger fra den valgte skabelon. Værdien i feltet **Kode** er udvidet med f.eks. "-01" for at angive, at dette er det første workflow, som oprettes ud fra workflowskabelonen.  
4.  Fortsæt med at oprette workflowet ved at redigere workflowtrinene eller tilføje nye trin. Du kan finde flere oplysninger i [Oprette arbejdsgange](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Se også  
 [Oprette arbejdsgange](across-how-to-create-workflows.md)   
 [Eksportere og importere workflows](across-how-to-export-and-import-workflows.md)   
 [Vise arkiverede forekomster af arbejdsgangstrin](across-how-to-view-archived-workflow-step-instances.md)   
 [Slette arbejdsgange](across-how-to-delete-workflows.md)   
 [Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Opsætte workflows](across-set-up-workflows.md)   
 [Anvende workflows](across-use-workflows.md)   
 [Workflow](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]