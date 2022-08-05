---
title: Sådan oprettes workflows ud fra workflowskabeloner
description: Hvis du vil spare tid, når du opretter nye arbejdsprocesser, kan du oprette ikke-redigerbare arbejdsprocesser fra de arbejdsprocesskabeloner, der er blevet løst med "MS".
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 18a9d4ba7e2865e41d660261a598b1b755c68023
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129699"
---
# <a name="create-workflows-from-workflow-templates"></a>Oprette workflows ud fra workflowskabeloner

For at spare tid ved oprettelse af nye workflows kan du oprette workflows ud fra workflowskabeloner.  

Workflowskabeloner er workflows, som ikke kan redigeres, og som findes i standardversionen af [!INCLUDE[prod_short](includes/prod_short.md)]. Koderne for workflowskabeloner, som er oprettet af Microsoft, har "MS-" foran.  

En anden måde til hurtigt at oprette et workflow på er at importere et eksisterende workflow, som du har på en fil uden for [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Eksportere og importere workflows](across-how-to-export-and-import-workflows.md).  

På siden **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne. Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder. Du definerer workflowtrin ved at udfylde felter om workflowlinjer fra faste lister over hændelses- og responsværdier, der repræsenterer scenarier, der understøttes af programkoden. Du kan finde flere oplysninger i [Oprette arbejdsgange](across-how-to-create-workflows.md).  

## <a name="to-create-a-workflow-from-a-workflow-template"></a>Sådan opretter du fra et workflow ud fra en workflowskabelon

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Arbejdsflow**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Nyt workflow fra skabelon**. Siden **Workflowskabeloner** åbnes.  
3. Vælg et workflow, og vælg derefter knappen **OK**.  

   Siden **Workflow** åbnes for et nyt workflow, der indeholder alle oplysninger fra den valgte skabelon. Værdien i feltet **Kode** er udvidet med f.eks. "-01" for at angive, at dette er det første workflow, som oprettes ud fra workflowskabelonen.  
4. Fortsæt med at oprette workflowet ved at redigere workflowtrinene eller tilføje nye trin. Du kan finde flere oplysninger i [Oprette arbejdsgange](across-how-to-create-workflows.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/modules/create-workflows/)

## <a name="see-also"></a>Se også

[Oprette arbejdsgange](across-how-to-create-workflows.md)  
[Eksportere og importere workflows](across-how-to-export-and-import-workflows.md)  
[Vise arkiverede forekomster af arbejdsgangstrin](across-how-to-view-archived-workflow-step-instances.md)  
[Slette arbejdsgange](across-how-to-delete-workflows.md)  
[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Opsætte workflows](across-set-up-workflows.md)  
[Bruge arbejdsgange](across-use-workflows.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]