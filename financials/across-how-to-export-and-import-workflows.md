---
title: "Sådan eksporterer og importerer du workflows | Microsoft Docs"
description: "Du kan overføre workflows til andre databaser i Finance and Operations, Business edition, f.eks. for at spare tid ved oprettelse af nye workflows, ved at eksportere og importere workflows."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6da772f9eefab9aa0ef8b9f47f6ea7656ebef1b4
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="export-and-import-workflows"></a>Eksportere og importere workflows
Du kan overføre workflows til andre [!INCLUDE[d365fin](includes/d365fin_md.md)]-databaser, f.eks. for at spare tid ved oprettelse af nye workflows, ved at eksportere og importere workflows.  

 En anden måde til hurtigt at oprette workflows er at oprette workflows fra workflowskabeloner. Du kan finde flere oplysninger i [Oprette workflows ud fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md).  

 I vinduet **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne. Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder. Du definerer workflowtrin ved at udfylde felter om workflowlinjer fra faste lister over hændelses- og responsværdier, der repræsenterer scenarier, der understøttes af programkoden. Du kan finde flere oplysninger i [Oprette arbejdsgange](across-how-to-create-workflows.md).  

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
 [Oprette arbejdsgange](across-how-to-create-workflows.md)   
 [Oprette workflows ud fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md)   
 [Vise arkiverede forekomster af arbejdsgangstrin](across-how-to-view-archived-workflow-step-instances.md)   
 [Slette arbejdsgange](across-how-to-delete-workflows.md)   
 [Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Opsætte workflows](across-set-up-workflows.md)   
 [Anvende workflows](across-use-workflows.md)   
 [Workflow](across-workflow.md)   

