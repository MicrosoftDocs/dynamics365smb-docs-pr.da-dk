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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 82d288ab59f80c6e5d2e46f8168f10552b5b900d
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "912916"
---
# <a name="create-workflows-from-workflow-templates"></a><span data-ttu-id="05a69-103">Oprette workflows ud fra workflowskabeloner</span><span class="sxs-lookup"><span data-stu-id="05a69-103">Create Workflows from Workflow Templates</span></span>
<span data-ttu-id="05a69-104">For at spare tid ved oprettelse af nye workflows kan du oprette workflows ud fra workflowskabeloner.</span><span class="sxs-lookup"><span data-stu-id="05a69-104">To save time when creating new workflows, you can create workflows from workflow templates.</span></span>  

 <span data-ttu-id="05a69-105">Workflowskabeloner er workflows, som ikke kan redigeres, og som findes i den generiske version af [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="05a69-105">Workflow templates are non-editable workflows that exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="05a69-106">Koderne for workflowskabeloner, som er tilføjet af Microsoft, har "MS" foran som f.eks. i "MS-".</span><span class="sxs-lookup"><span data-stu-id="05a69-106">The codes for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span>  

 <span data-ttu-id="05a69-107">En anden måde til hurtigt at oprette et workflow på er at importere et eksisterende workflow, som du har på en fil uden for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="05a69-107">Another way to quickly create a workflow is to import an existing workflow that you have on a file outside of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="05a69-108">Du kan finde flere oplysninger i [Eksportere og importere workflows](across-how-to-export-and-import-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="05a69-108">For more information, see [Export and Import Workflows](across-how-to-export-and-import-workflows.md).</span></span>  

<span data-ttu-id="05a69-109">På siden **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne.</span><span class="sxs-lookup"><span data-stu-id="05a69-109">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="05a69-110">Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder.</span><span class="sxs-lookup"><span data-stu-id="05a69-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="05a69-111">Du definerer workflowtrin ved at udfylde felter om workflowlinjer fra faste lister over hændelses- og responsværdier, der repræsenterer scenarier, der understøttes af programkoden.</span><span class="sxs-lookup"><span data-stu-id="05a69-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="05a69-112">Du kan finde flere oplysninger i [Oprette arbejdsgange](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="05a69-112">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-create-a-workflow-from-workflow-template"></a><span data-ttu-id="05a69-113">Sådan opretter du fra et workflow ud fra en workflowskabelon</span><span class="sxs-lookup"><span data-stu-id="05a69-113">To create a workflow from workflow template</span></span>  
1.  <span data-ttu-id="05a69-114">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Workflows**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="05a69-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="05a69-115">Vælg handlingen **Opret workflow fra skabelon**.</span><span class="sxs-lookup"><span data-stu-id="05a69-115">Choose the **Create Workflow from Template** action.</span></span> <span data-ttu-id="05a69-116">Siden **Workflowskabeloner** åbnes.</span><span class="sxs-lookup"><span data-stu-id="05a69-116">The **Workflow Templates** page opens.</span></span>  
3.  <span data-ttu-id="05a69-117">Vælg et workflow, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="05a69-117">Select a workflow template, and then choose the **OK** button.</span></span>  

     <span data-ttu-id="05a69-118">Siden **Workflow** åbnes for et nyt workflow, der indeholder alle oplysninger fra den valgte skabelon.</span><span class="sxs-lookup"><span data-stu-id="05a69-118">The **Workflow** page opens for a new workflow containing all the information of the selected template.</span></span> <span data-ttu-id="05a69-119">Værdien i feltet **Kode** er udvidet med f.eks. "-01" for at angive, at dette er det første workflow, som oprettes ud fra workflowskabelonen.</span><span class="sxs-lookup"><span data-stu-id="05a69-119">The value in the **Code** field is extended with, for example, “-01” to indicate that this is the first workflow that is created from the workflow template.</span></span>  
4.  <span data-ttu-id="05a69-120">Fortsæt med at oprette workflowet ved at redigere workflowtrinene eller tilføje nye trin.</span><span class="sxs-lookup"><span data-stu-id="05a69-120">Proceed to create the workflow by editing the workflow steps or add new steps.</span></span> <span data-ttu-id="05a69-121">Du kan finde flere oplysninger i [Oprette arbejdsgange](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="05a69-121">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="05a69-122">Se også</span><span class="sxs-lookup"><span data-stu-id="05a69-122">See Also</span></span>  
 <span data-ttu-id="05a69-123">[Oprette arbejdsgange](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="05a69-123">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="05a69-124">[Eksportere og importere workflows](across-how-to-export-and-import-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="05a69-124">[Export and Import Workflows](across-how-to-export-and-import-workflows.md) </span></span>  
 <span data-ttu-id="05a69-125">[Vise arkiverede forekomster af arbejdsgangstrin](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="05a69-125">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="05a69-126">[Slette arbejdsgange](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="05a69-126">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="05a69-127">[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="05a69-127">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="05a69-128">[Opsætte workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="05a69-128">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="05a69-129">[Anvende workflows](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="05a69-129">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="05a69-130">Workflow</span><span class="sxs-lookup"><span data-stu-id="05a69-130">Workflow</span></span>](across-workflow.md)   
