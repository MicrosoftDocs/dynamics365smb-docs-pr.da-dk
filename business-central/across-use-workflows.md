---
title: Anvende workflows | Microsoft Docs
description: Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d608841bf5d5586bd0ef84ef554055517def0eb8
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3917947"
---
# <a name="using-workflows"></a><span data-ttu-id="95e89-105">Anvende workflows</span><span class="sxs-lookup"><span data-stu-id="95e89-105">Using Workflows</span></span>
<span data-ttu-id="95e89-106">Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere.</span><span class="sxs-lookup"><span data-stu-id="95e89-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="95e89-107">Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver.</span><span class="sxs-lookup"><span data-stu-id="95e89-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="95e89-108">Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin.</span><span class="sxs-lookup"><span data-stu-id="95e89-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="95e89-109">Inden du kan bruge arbejdsprocesser, skal du oprette arbejdsgangbrugere, oprette arbejdsgangene, som kan være med tilpasning af kode, og angive, hvordan brugere får vist meddelelser.</span><span class="sxs-lookup"><span data-stu-id="95e89-109">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="95e89-110">Du kan finde flere oplysninger under [Opsætte workflows](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="95e89-110">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="95e89-111">Typiske arbejdsgangstrin er om brugere, der anmoder om godkendelse af opgaver, og godkendere, der accepterer eller afviser godkendelsesanmodninger.</span><span class="sxs-lookup"><span data-stu-id="95e89-111">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="95e89-112">Derfor henviser mange emner om brug af workflows til godkendelser.</span><span class="sxs-lookup"><span data-stu-id="95e89-112">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="95e89-113">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="95e89-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="95e89-114">**For at**</span><span class="sxs-lookup"><span data-stu-id="95e89-114">**To**</span></span>|<span data-ttu-id="95e89-115">**Skal du se**</span><span class="sxs-lookup"><span data-stu-id="95e89-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="95e89-116">Angiv, at en arbejdsgang skal startes, når den første startpunkthændelse finder sted.</span><span class="sxs-lookup"><span data-stu-id="95e89-116">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="95e89-117">Aktivere arbejdsgange</span><span class="sxs-lookup"><span data-stu-id="95e89-117">Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="95e89-118">Anmode om godkendelse af en opgave, som godkender, godkende, afvise eller uddelegere godkendelser og sende eller få vist godkendelsesnotifikationer.</span><span class="sxs-lookup"><span data-stu-id="95e89-118">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="95e89-119">Bruge godkendelsesworkflows</span><span class="sxs-lookup"><span data-stu-id="95e89-119">Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="95e89-120">Opret arbejdsgangstrin, der sikrer, at en bestemt posttype ikke bruges, før en bestemt hændelse opstår, for eksempel at posten godkendes.</span><span class="sxs-lookup"><span data-stu-id="95e89-120">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="95e89-121">Begrænse og tillade brugen af en record</span><span class="sxs-lookup"><span data-stu-id="95e89-121">Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="95e89-122">Vis arbejdsgangstrinsforekomster med statussen Afsluttet.</span><span class="sxs-lookup"><span data-stu-id="95e89-122">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="95e89-123">Vise arkiverede forekomster af arbejdsgangstrin</span><span class="sxs-lookup"><span data-stu-id="95e89-123">View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="95e89-124">Slet en arbejdsgang, som du er sikker på ikke længere bruges.</span><span class="sxs-lookup"><span data-stu-id="95e89-124">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="95e89-125">Slette arbejdsgange</span><span class="sxs-lookup"><span data-stu-id="95e89-125">Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="95e89-126">Se også</span><span class="sxs-lookup"><span data-stu-id="95e89-126">See Also</span></span>  
<span data-ttu-id="95e89-127">[Opsætte workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="95e89-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="95e89-128">[Workflow](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="95e89-128">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="95e89-129">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="95e89-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
