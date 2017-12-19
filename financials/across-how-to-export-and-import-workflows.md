---
title: "Sådan eksporterer og importerer du workflows | Microsoft Docs"
description: "Du kan overføre workflows til andre Dynamics 365-databaser, f.eks. for at spare tid ved oprettelse af nye workflows, ved at eksportere og importere workflows."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 520c81b9c550b4ef29b077685541a2e7ea30d4d7
ms.contentlocale: da-dk
ms.lasthandoff: 12/14/2017

---
# <a name="how-to-export-and-import-workflows"></a>Fremgangsmåde: Importere og eksportere workflows
Du kan overføre workflows til andre [!INCLUDE[d365fin](includes/d365fin_md.md)]-databaser, f.eks. for at spare tid ved oprettelse af nye workflows, ved at eksportere og importere workflows.  

 En anden måde til hurtigt at oprette workflows er at oprette workflows fra workflowskabeloner. Du kan finde flere oplysninger i [Fremgangsmåde: Oprette workflows ud fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md).  

 I vinduet **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne. Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder. Du definerer arbejdsgangstrin ved at udfylde felter om arbejdsganglinjer fra faste lister over hændelses- og svarværdier, der repræsenterer scenarier, der understøttes af programkoden. Du kan finde flere oplysninger i [Fremgangsmåde: Oprette arbejdsgange](across-how-to-create-workflows.md).  

## <a name="to-export-a-workflow"></a>Sådan eksporteres et workflow  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), og angiv **Workflows**, og vælg derefter det relaterede link.  
2.  Vælg et workflow, og vælg derefter handlingen **Eksportér til fil**.  
3.  Vælg knappen **Gem** i vinduet **Udlæs fil**.  
4.  I vinduet **Udlæs** skal du vælge en filplacering og derefter klikke på knappen **Gem**.  

## <a name="to-import-a-workflow"></a>Sådan indlæses et workflow  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), og angiv **Workflows**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Importér fra fil**.  
3.  Vælg den XML-fil, der indeholder workflowet, i vinduet **Indlæs**, og vælg derefter knappen **Åbn**.  

> [!CAUTION]  
>  Hvis workflowkoden allerede findes i databasen, overskrives workflowtrinene med trinene i det indlæste workflow.  

## <a name="see-also"></a>Se også  
 [Fremgangsmåde: Oprette arbejdsgange](across-how-to-create-workflows.md)   
 [Fremgangsmåde: Oprette workflows ud fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md)   
 [Fremgangsmåde: Se arkiverede forekomster af arbejdsgangstrin](across-how-to-view-archived-workflow-step-instances.md)   
 [Fremgangsmåde: Slette arbejdsgange](across-how-to-delete-workflows.md)   
 [Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Opsætte workflows](across-set-up-workflows.md)   
 [Anvende workflows](across-use-workflows.md)   
 [Workflow](across-workflow.md)   

