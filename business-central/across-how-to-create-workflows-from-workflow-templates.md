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
# <a name="create-workflows-from-workflow-templates"></a><span data-ttu-id="f242b-103">Oprette workflows ud fra workflowskabeloner</span><span class="sxs-lookup"><span data-stu-id="f242b-103">Create Workflows from Workflow Templates</span></span>
<span data-ttu-id="f242b-104">For at spare tid ved oprettelse af nye workflows kan du oprette workflows ud fra workflowskabeloner.</span><span class="sxs-lookup"><span data-stu-id="f242b-104">To save time when creating new workflows, you can create workflows from workflow templates.</span></span>  

 <span data-ttu-id="f242b-105">Workflowskabeloner er workflows, som ikke kan redigeres, og som findes i den generiske version af [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="f242b-105">Workflow templates are non-editable workflows that exist in the generic version of [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="f242b-106">Koderne for workflowskabeloner, som er tilføjet af Microsoft, har "MS" foran som f.eks. i "MS-".</span><span class="sxs-lookup"><span data-stu-id="f242b-106">The codes for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span>  

 <span data-ttu-id="f242b-107">En anden måde til hurtigt at oprette et workflow på er at importere et eksisterende workflow, som du har på en fil uden for [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="f242b-107">Another way to quickly create a workflow is to import an existing workflow that you have on a file outside of [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="f242b-108">Du kan finde flere oplysninger i [Eksportere og importere workflows](across-how-to-export-and-import-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="f242b-108">For more information, see [Export and Import Workflows](across-how-to-export-and-import-workflows.md).</span></span>  

<span data-ttu-id="f242b-109">På siden **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne.</span><span class="sxs-lookup"><span data-stu-id="f242b-109">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="f242b-110">Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder.</span><span class="sxs-lookup"><span data-stu-id="f242b-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="f242b-111">Du definerer workflowtrin ved at udfylde felter om workflowlinjer fra faste lister over hændelses- og responsværdier, der repræsenterer scenarier, der understøttes af programkoden.</span><span class="sxs-lookup"><span data-stu-id="f242b-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="f242b-112">Du kan finde flere oplysninger i [Oprette arbejdsgange](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="f242b-112">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-create-a-workflow-from-workflow-template"></a><span data-ttu-id="f242b-113">Sådan opretter du fra et workflow ud fra en workflowskabelon</span><span class="sxs-lookup"><span data-stu-id="f242b-113">To create a workflow from workflow template</span></span>  
1.  <span data-ttu-id="f242b-114">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Arbejdsgange**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f242b-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f242b-115">Vælg handlingen **Opret workflow fra skabelon**.</span><span class="sxs-lookup"><span data-stu-id="f242b-115">Choose the **Create Workflow from Template** action.</span></span> <span data-ttu-id="f242b-116">Siden **Workflowskabeloner** åbnes.</span><span class="sxs-lookup"><span data-stu-id="f242b-116">The **Workflow Templates** page opens.</span></span>  
3.  <span data-ttu-id="f242b-117">Vælg et workflow, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="f242b-117">Select a workflow template, and then choose the **OK** button.</span></span>  

     <span data-ttu-id="f242b-118">Siden **Workflow** åbnes for et nyt workflow, der indeholder alle oplysninger fra den valgte skabelon.</span><span class="sxs-lookup"><span data-stu-id="f242b-118">The **Workflow** page opens for a new workflow containing all the information of the selected template.</span></span> <span data-ttu-id="f242b-119">Værdien i feltet **Kode** er udvidet med f.eks. "-01" for at angive, at dette er det første workflow, som oprettes ud fra workflowskabelonen.</span><span class="sxs-lookup"><span data-stu-id="f242b-119">The value in the **Code** field is extended with, for example, “-01” to indicate that this is the first workflow that is created from the workflow template.</span></span>  
4.  <span data-ttu-id="f242b-120">Fortsæt med at oprette workflowet ved at redigere workflowtrinene eller tilføje nye trin.</span><span class="sxs-lookup"><span data-stu-id="f242b-120">Proceed to create the workflow by editing the workflow steps or add new steps.</span></span> <span data-ttu-id="f242b-121">Du kan finde flere oplysninger i [Oprette arbejdsgange](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="f242b-121">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="f242b-122">Se også</span><span class="sxs-lookup"><span data-stu-id="f242b-122">See Also</span></span>  
 <span data-ttu-id="f242b-123">[Oprette arbejdsgange](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="f242b-123">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="f242b-124">[Eksportere og importere workflows](across-how-to-export-and-import-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="f242b-124">[Export and Import Workflows](across-how-to-export-and-import-workflows.md) </span></span>  
 <span data-ttu-id="f242b-125">[Vise arkiverede forekomster af arbejdsgangstrin](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="f242b-125">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="f242b-126">[Slette arbejdsgange](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="f242b-126">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="f242b-127">[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="f242b-127">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="f242b-128">[Opsætte workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="f242b-128">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="f242b-129">[Anvende workflows](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="f242b-129">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="f242b-130">Workflow</span><span class="sxs-lookup"><span data-stu-id="f242b-130">Workflow</span></span>](across-workflow.md)   
