---
title: Anvende workflows | Microsoft Docs
description: "Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a42e336dba385cbf24c19702ad64d76b26c15104
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="using-workflows"></a><span data-ttu-id="52423-105">Anvende workflows</span><span class="sxs-lookup"><span data-stu-id="52423-105">Using Workflows</span></span>
<span data-ttu-id="52423-106">Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere.</span><span class="sxs-lookup"><span data-stu-id="52423-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="52423-107">Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver.</span><span class="sxs-lookup"><span data-stu-id="52423-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="52423-108">Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin.</span><span class="sxs-lookup"><span data-stu-id="52423-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="52423-109">Inden du kan bruge arbejdsprocesser, skal du oprette arbejdsgangbrugere, oprette arbejdsgangene, som kan være med tilpasning af kode, og angive, hvordan brugere får vist meddelelser.</span><span class="sxs-lookup"><span data-stu-id="52423-109">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="52423-110">Du kan finde flere oplysninger under [Opsætte workflows](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="52423-110">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="52423-111">Typiske arbejdsgangstrin er om brugere, der anmoder om godkendelse af opgaver, og godkendere, der accepterer eller afviser godkendelsesanmodninger.</span><span class="sxs-lookup"><span data-stu-id="52423-111">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="52423-112">Derfor henviser mange emner om brug af workflows til godkendelser.</span><span class="sxs-lookup"><span data-stu-id="52423-112">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="52423-113">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="52423-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="52423-114">**For at**</span><span class="sxs-lookup"><span data-stu-id="52423-114">**To**</span></span>|<span data-ttu-id="52423-115">**Skal du se**</span><span class="sxs-lookup"><span data-stu-id="52423-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="52423-116">Angiv, at en arbejdsgang skal startes, når den første startpunkthændelse finder sted.</span><span class="sxs-lookup"><span data-stu-id="52423-116">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="52423-117">Fremgangsmåde: Aktivere arbejdsgange</span><span class="sxs-lookup"><span data-stu-id="52423-117">How to: Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="52423-118">Anmode om godkendelse af en opgave, som godkender, godkende, afvise eller uddelegere godkendelser og sende eller få vist godkendelsesnotifikationer.</span><span class="sxs-lookup"><span data-stu-id="52423-118">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="52423-119">Fremgangsmåde: Bruge godkendelsesworkflows</span><span class="sxs-lookup"><span data-stu-id="52423-119">How to: Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="52423-120">Opret arbejdsgangstrin, der sikrer, at en bestemt posttype ikke bruges, før en bestemt hændelse opstår, for eksempel at posten godkendes.</span><span class="sxs-lookup"><span data-stu-id="52423-120">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="52423-121">Fremgangsmåde: Begrænse og tillade brug af en post</span><span class="sxs-lookup"><span data-stu-id="52423-121">How to: Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="52423-122">Vis arbejdsgangstrinsforekomster med statussen Afsluttet.</span><span class="sxs-lookup"><span data-stu-id="52423-122">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="52423-123">Fremgangsmåde: Se arkiverede forekomster af arbejdsgangstrin</span><span class="sxs-lookup"><span data-stu-id="52423-123">How to: View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="52423-124">Slet en arbejdsgang, som du er sikker på ikke længere bruges.</span><span class="sxs-lookup"><span data-stu-id="52423-124">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="52423-125">Fremgangsmåde: Slette arbejdsgange</span><span class="sxs-lookup"><span data-stu-id="52423-125">How to: Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="52423-126">Se også</span><span class="sxs-lookup"><span data-stu-id="52423-126">See Also</span></span>  
<span data-ttu-id="52423-127">[Opsætte workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="52423-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="52423-128">[Workflow](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="52423-128">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="52423-129">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="52423-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

