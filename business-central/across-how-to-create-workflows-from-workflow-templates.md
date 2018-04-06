---
title: "Sådan opretter du workflows ud fra workflowskabeloner | Microsoft Docs"
description: For at spare tid ved oprettelse af nye workflows kan du oprette workflows ud fra workflowskabeloner.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0f923c6d40093f35eb051e69ec149c3296bd0ee7
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="create-workflows-from-workflow-templates"></a><span data-ttu-id="f0b61-103">Oprette workflows ud fra workflowskabeloner</span><span class="sxs-lookup"><span data-stu-id="f0b61-103">Create Workflows from Workflow Templates</span></span>
<span data-ttu-id="f0b61-104">For at spare tid ved oprettelse af nye workflows kan du oprette workflows ud fra workflowskabeloner.</span><span class="sxs-lookup"><span data-stu-id="f0b61-104">To save time when creating new workflows, you can create workflows from workflow templates.</span></span>  

 <span data-ttu-id="f0b61-105">Workflowskabeloner er workflows, som ikke kan redigeres, og som findes i den generiske version af [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f0b61-105">Workflow templates are non-editable workflows that exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="f0b61-106">Koderne for workflowskabeloner, som er tilføjet af Microsoft, har "MS" foran som f.eks. i "MS-".</span><span class="sxs-lookup"><span data-stu-id="f0b61-106">The codes for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span>  

 <span data-ttu-id="f0b61-107">En anden måde til hurtigt at oprette et workflow på er at importere et eksisterende workflow, som du har på en fil uden for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f0b61-107">Another way to quickly create a workflow is to import an existing workflow that you have on a file outside of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="f0b61-108">Du kan finde flere oplysninger i [Eksportere og importere workflows](across-how-to-export-and-import-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="f0b61-108">For more information, see [Export and Import Workflows](across-how-to-export-and-import-workflows.md).</span></span>  

<span data-ttu-id="f0b61-109">I vinduet **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne.</span><span class="sxs-lookup"><span data-stu-id="f0b61-109">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="f0b61-110">Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder.</span><span class="sxs-lookup"><span data-stu-id="f0b61-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="f0b61-111">Du definerer workflowtrin ved at udfylde felter om workflowlinjer fra faste lister over hændelses- og responsværdier, der repræsenterer scenarier, der understøttes af programkoden.</span><span class="sxs-lookup"><span data-stu-id="f0b61-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="f0b61-112">Du kan finde flere oplysninger i [Oprette arbejdsgange](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="f0b61-112">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-create-a-workflow-from-workflow-template"></a><span data-ttu-id="f0b61-113">Sådan opretter du fra et workflow ud fra en workflowskabelon</span><span class="sxs-lookup"><span data-stu-id="f0b61-113">To create a workflow from workflow template</span></span>  
1.  <span data-ttu-id="f0b61-114">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), og angiv **Workflows**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f0b61-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f0b61-115">Vælg handlingen **Opret workflow fra skabelon**.</span><span class="sxs-lookup"><span data-stu-id="f0b61-115">Choose the **Create Workflow from Template** action.</span></span> <span data-ttu-id="f0b61-116">Vinduet **Workflowskabeloner** åbnes.</span><span class="sxs-lookup"><span data-stu-id="f0b61-116">The **Workflow Templates** window opens.</span></span>  
3.  <span data-ttu-id="f0b61-117">Vælg et workflow, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0b61-117">Select a workflow template, and then choose the **OK** button.</span></span>  

     <span data-ttu-id="f0b61-118">Vinduet **Workflow** åbnes for et nyt workflow, der indeholder alle oplysninger fra den valgte skabelon.</span><span class="sxs-lookup"><span data-stu-id="f0b61-118">The **Workflow** window opens for a new workflow containing all the information of the selected template.</span></span> <span data-ttu-id="f0b61-119">Værdien i feltet **Kode** er udvidet med f.eks. "-01" for at angive, at dette er det første workflow, som oprettes ud fra workflowskabelonen.</span><span class="sxs-lookup"><span data-stu-id="f0b61-119">The value in the **Code** field is extended with, for example, “-01” to indicate that this is the first workflow that is created from the workflow template.</span></span>  
4.  <span data-ttu-id="f0b61-120">Fortsæt med at oprette workflowet ved at redigere workflowtrinene eller tilføje nye trin.</span><span class="sxs-lookup"><span data-stu-id="f0b61-120">Proceed to create the workflow by editing the workflow steps or add new steps.</span></span> <span data-ttu-id="f0b61-121">Du kan finde flere oplysninger i [Oprette arbejdsgange](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="f0b61-121">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="f0b61-122">Se også</span><span class="sxs-lookup"><span data-stu-id="f0b61-122">See Also</span></span>  
 <span data-ttu-id="f0b61-123">[Oprette arbejdsgange](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="f0b61-123">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="f0b61-124">[Eksportere og importere workflows](across-how-to-export-and-import-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="f0b61-124">[Export and Import Workflows](across-how-to-export-and-import-workflows.md) </span></span>  
 <span data-ttu-id="f0b61-125">[Vise arkiverede forekomster af arbejdsgangstrin](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="f0b61-125">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="f0b61-126">[Slette arbejdsgange](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="f0b61-126">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="f0b61-127">[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="f0b61-127">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="f0b61-128">[Opsætte workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="f0b61-128">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="f0b61-129">[Anvende workflows](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="f0b61-129">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="f0b61-130">Workflow</span><span class="sxs-lookup"><span data-stu-id="f0b61-130">Workflow</span></span>](across-workflow.md)   

