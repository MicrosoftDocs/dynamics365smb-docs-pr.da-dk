---
title: "Sådan sletter du workflows | Microsoft Docs"
description: "Hvis du er sikker på, at en arbejdsgang ikke længere bruges, kan du slette den. Alle forekomster af trin i arbejdsgangen, der er defineret i arbejdsgangen, skal have status **Afsluttet**."
services: project-madeira
documentationcenter: 
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d1b7b29735983e2de0bdaf5d382679d9546a6278
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-delete-workflows"></a><span data-ttu-id="80a3e-104">Fremgangsmåde: Slette arbejdsgange</span><span class="sxs-lookup"><span data-stu-id="80a3e-104">How to: Delete Workflows</span></span>
<span data-ttu-id="80a3e-105">Hvis du er sikker på, at en arbejdsgang ikke længere bruges, kan du slette den.</span><span class="sxs-lookup"><span data-stu-id="80a3e-105">If you are certain that a workflow is no longer being used, you can delete it.</span></span> <span data-ttu-id="80a3e-106">Alle forekomster af trin i arbejdsgangen, der er defineret i arbejdsgangen, skal have status **Afsluttet**.</span><span class="sxs-lookup"><span data-stu-id="80a3e-106">All workflow step instances that are defined in the workflow must have status **Completed**.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="80a3e-107">Når du sletter en arbejdsgang, mistes alle oplysninger i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="80a3e-107">When you delete a workflow, all information in the workflow will be lost.</span></span>  

 <span data-ttu-id="80a3e-108">I vinduet **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne.</span><span class="sxs-lookup"><span data-stu-id="80a3e-108">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="80a3e-109">Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder.</span><span class="sxs-lookup"><span data-stu-id="80a3e-109">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="80a3e-110">Du definerer arbejdsgangstrin ved at udfylde felter om arbejdsganglinjer fra faste lister over hændelses- og svarværdier, der repræsenterer scenarier, der understøttes af programkoden.</span><span class="sxs-lookup"><span data-stu-id="80a3e-110">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="80a3e-111">Du kan finde flere oplysninger i [Fremgangsmåde: Oprette arbejdsgange](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="80a3e-111">For more information, see [How to: Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-delete-a-workflow"></a><span data-ttu-id="80a3e-112">Sådan slettes en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="80a3e-112">To delete a workflow</span></span>  
1.  <span data-ttu-id="80a3e-113">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), og angiv **Workflows**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="80a3e-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="80a3e-114">Vælg den arbejdsgang du vil slette.</span><span class="sxs-lookup"><span data-stu-id="80a3e-114">Select the workflow that you want to delete.</span></span>  
3.  <span data-ttu-id="80a3e-115">Vælg handlingen **Slet**.</span><span class="sxs-lookup"><span data-stu-id="80a3e-115">Choose the **Delete** action.</span></span>  
4.  <span data-ttu-id="80a3e-116">Du kan også åbne den arbejdsgang du vil slette.</span><span class="sxs-lookup"><span data-stu-id="80a3e-116">Alternatively, open the workflow that you want to delete.</span></span>  
5.  <span data-ttu-id="80a3e-117">I vinduet **Workflow** skal du vælge handlingen **Slet**.</span><span class="sxs-lookup"><span data-stu-id="80a3e-117">In the **Workflow** window, choose the **Delete** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="80a3e-118">Se også</span><span class="sxs-lookup"><span data-stu-id="80a3e-118">See Also</span></span>  
 <span data-ttu-id="80a3e-119">[Fremgangsmåde: Oprette arbejdsgange](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="80a3e-119">[How to: Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="80a3e-120">[Fremgangsmåde: Aktivere arbejdsgange](across-how-to-enable-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="80a3e-120">[How to: Enable Workflows](across-how-to-enable-workflows.md) </span></span>  
 <span data-ttu-id="80a3e-121">[Fremgangsmåde: Se arkiverede forekomster af arbejdsgangstrin](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="80a3e-121">[How to: View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="80a3e-122">[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="80a3e-122">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="80a3e-123">[Opsætte workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="80a3e-123">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="80a3e-124">[Anvende workflows](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="80a3e-124">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="80a3e-125">Workflow</span><span class="sxs-lookup"><span data-stu-id="80a3e-125">Workflow</span></span>](across-workflow.md)   

