---
title: "Sådan sletter du workflows | Microsoft Docs"
description: "Hvis du er sikker på, at en arbejdsgang ikke længere bruges, kan du slette den. Alle forekomster af trin i arbejdsgangen, der er defineret i arbejdsgangen, skal have status **Afsluttet**."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 05404279ee0967b1ffd48e010cdf1f9dcac157d9
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="delete-workflows"></a><span data-ttu-id="d38b6-104">Slette arbejdsgange</span><span class="sxs-lookup"><span data-stu-id="d38b6-104">Delete Workflows</span></span>
<span data-ttu-id="d38b6-105">Hvis du er sikker på, at en arbejdsgang ikke længere bruges, kan du slette den.</span><span class="sxs-lookup"><span data-stu-id="d38b6-105">If you are certain that a workflow is no longer being used, you can delete it.</span></span> <span data-ttu-id="d38b6-106">Alle forekomster af trin i arbejdsgangen, der er defineret i arbejdsgangen, skal have status **Afsluttet**.</span><span class="sxs-lookup"><span data-stu-id="d38b6-106">All workflow step instances that are defined in the workflow must have status **Completed**.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="d38b6-107">Når du sletter en arbejdsgang, mistes alle oplysninger i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="d38b6-107">When you delete a workflow, all information in the workflow will be lost.</span></span>  

 <span data-ttu-id="d38b6-108">På siden **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne.</span><span class="sxs-lookup"><span data-stu-id="d38b6-108">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="d38b6-109">Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder.</span><span class="sxs-lookup"><span data-stu-id="d38b6-109">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="d38b6-110">Du definerer workflowtrin ved at udfylde felter om workflowlinjer fra faste lister over hændelses- og responsværdier, der repræsenterer scenarier, der understøttes af programkoden.</span><span class="sxs-lookup"><span data-stu-id="d38b6-110">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="d38b6-111">Du kan finde flere oplysninger i [Oprette arbejdsgange](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="d38b6-111">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-delete-a-workflow"></a><span data-ttu-id="d38b6-112">Sådan slettes en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="d38b6-112">To delete a workflow</span></span>  
1.  <span data-ttu-id="d38b6-113">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Workflows**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d38b6-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d38b6-114">Vælg den arbejdsgang du vil slette.</span><span class="sxs-lookup"><span data-stu-id="d38b6-114">Select the workflow that you want to delete.</span></span>  
3.  <span data-ttu-id="d38b6-115">Vælg handlingen **Slet**.</span><span class="sxs-lookup"><span data-stu-id="d38b6-115">Choose the **Delete** action.</span></span>  
4.  <span data-ttu-id="d38b6-116">Du kan også åbne den arbejdsgang du vil slette.</span><span class="sxs-lookup"><span data-stu-id="d38b6-116">Alternatively, open the workflow that you want to delete.</span></span>  
5.  <span data-ttu-id="d38b6-117">På siden **Workflow** skal du vælge handlingen **Slet**.</span><span class="sxs-lookup"><span data-stu-id="d38b6-117">On the **Workflow** page, choose the **Delete** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d38b6-118">Se også</span><span class="sxs-lookup"><span data-stu-id="d38b6-118">See Also</span></span>  
 <span data-ttu-id="d38b6-119">[Oprette arbejdsgange](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d38b6-119">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="d38b6-120">[Aktivere arbejdsgange](across-how-to-enable-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d38b6-120">[Enable Workflows](across-how-to-enable-workflows.md) </span></span>  
 <span data-ttu-id="d38b6-121">[Vise arkiverede forekomster af arbejdsgangstrin](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="d38b6-121">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="d38b6-122">[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="d38b6-122">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="d38b6-123">[Opsætte workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d38b6-123">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="d38b6-124">[Anvende workflows](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d38b6-124">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="d38b6-125">Workflow</span><span class="sxs-lookup"><span data-stu-id="d38b6-125">Workflow</span></span>](across-workflow.md)   

