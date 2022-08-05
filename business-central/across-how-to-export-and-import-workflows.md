---
title: Sådan eksporterer og importerer du workflows | Microsoft Docs
description: Du kan overføre workflows til andre Business Central-databaser, f.eks. for at spare tid ved oprettelse af nye workflows, ved at eksportere og importere workflows.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1a52d4b4bff0f96023b6206e6cb8cad3d9e59276
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129925"
---
# <a name="export-and-import-workflows"></a>Eksportere og importere workflows

Du kan overføre workflows til andre [!INCLUDE[prod_short](includes/prod_short.md)]-databaser, f.eks. for at spare tid ved oprettelse af nye workflows, ved at eksportere og importere workflows.  

En anden måde til hurtigt at oprette workflows er at oprette workflows fra workflowskabeloner. Du kan finde flere oplysninger i [Oprette workflows ud fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md).  

På siden **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne. Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder. Du definerer workflowtrin ved at udfylde felter om workflowlinjer fra faste lister over hændelses- og responsværdier, der repræsenterer scenarier, der understøttes af programkoden. Du kan finde flere oplysninger i [Oprette arbejdsgange](across-how-to-create-workflows.md).  

## <a name="to-export-a-workflow"></a>Sådan eksporteres et workflow

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Arbejdsflow**, og vælg derefter det relaterede link.  
2. Vælg et workflow, og vælg derefter handlingen **Eksportér til fil**.  

## <a name="to-import-a-workflow"></a>Sådan indlæses et workflow

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Workflows**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Importér fra fil**.  
3. Vælg den XML-fil, der indeholder workflowet, og vælg knappen **Åbn** på siden **Importer**, og vælg knappen **Vælg**.  

> [!CAUTION]  
> Hvis workflowkoden allerede findes i databasen, overskrives workflowtrinene med trinene i det indlæste workflow.  

## <a name="see-also"></a>Se også

[Oprette arbejdsgange](across-how-to-create-workflows.md)  
[Oprette workflows ud fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md)  
[Vise arkiverede forekomster af workflowtrin](across-how-to-view-archived-workflow-step-instances.md)  
[Slette arbejdsgange](across-how-to-delete-workflows.md)  
[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Opsætte workflows](across-set-up-workflows.md)  
[Bruge arbejdsgange](across-use-workflows.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]