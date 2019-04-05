---
title: Anvende workflows | Microsoft Docs
description: Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: b978f263f1ce6e08803202a5d2d3691974575c38
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792571"
---
# <a name="using-workflows"></a><span data-ttu-id="3a367-105">Anvende workflows</span><span class="sxs-lookup"><span data-stu-id="3a367-105">Using Workflows</span></span>
<span data-ttu-id="3a367-106">Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere.</span><span class="sxs-lookup"><span data-stu-id="3a367-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="3a367-107">Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver.</span><span class="sxs-lookup"><span data-stu-id="3a367-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="3a367-108">Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin.</span><span class="sxs-lookup"><span data-stu-id="3a367-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="3a367-109">Inden du kan bruge arbejdsprocesser, skal du oprette arbejdsgangbrugere, oprette arbejdsgangene, som kan være med tilpasning af kode, og angive, hvordan brugere får vist meddelelser.</span><span class="sxs-lookup"><span data-stu-id="3a367-109">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="3a367-110">Du kan finde flere oplysninger under [Opsætte workflows](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="3a367-110">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="3a367-111">Typiske arbejdsgangstrin er om brugere, der anmoder om godkendelse af opgaver, og godkendere, der accepterer eller afviser godkendelsesanmodninger.</span><span class="sxs-lookup"><span data-stu-id="3a367-111">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="3a367-112">Derfor henviser mange emner om brug af workflows til godkendelser.</span><span class="sxs-lookup"><span data-stu-id="3a367-112">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="3a367-113">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="3a367-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="3a367-114">**For at**</span><span class="sxs-lookup"><span data-stu-id="3a367-114">**To**</span></span>|<span data-ttu-id="3a367-115">**Skal du se**</span><span class="sxs-lookup"><span data-stu-id="3a367-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="3a367-116">Angiv, at en arbejdsgang skal startes, når den første startpunkthændelse finder sted.</span><span class="sxs-lookup"><span data-stu-id="3a367-116">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="3a367-117">Aktivere arbejdsgange</span><span class="sxs-lookup"><span data-stu-id="3a367-117">Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="3a367-118">Anmode om godkendelse af en opgave, som godkender, godkende, afvise eller uddelegere godkendelser og sende eller få vist godkendelsesnotifikationer.</span><span class="sxs-lookup"><span data-stu-id="3a367-118">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="3a367-119">Bruge godkendelsesworkflows</span><span class="sxs-lookup"><span data-stu-id="3a367-119">Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="3a367-120">Opret arbejdsgangstrin, der sikrer, at en bestemt posttype ikke bruges, før en bestemt hændelse opstår, for eksempel at posten godkendes.</span><span class="sxs-lookup"><span data-stu-id="3a367-120">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="3a367-121">Begrænse og tillade brugen af en record</span><span class="sxs-lookup"><span data-stu-id="3a367-121">Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="3a367-122">Vis arbejdsgangstrinsforekomster med statussen Afsluttet.</span><span class="sxs-lookup"><span data-stu-id="3a367-122">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="3a367-123">Vise arkiverede forekomster af arbejdsgangstrin</span><span class="sxs-lookup"><span data-stu-id="3a367-123">View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="3a367-124">Slet en arbejdsgang, som du er sikker på ikke længere bruges.</span><span class="sxs-lookup"><span data-stu-id="3a367-124">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="3a367-125">Slette arbejdsgange</span><span class="sxs-lookup"><span data-stu-id="3a367-125">Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="3a367-126">Se også</span><span class="sxs-lookup"><span data-stu-id="3a367-126">See Also</span></span>  
<span data-ttu-id="3a367-127">[Opsætte workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="3a367-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="3a367-128">[Workflow](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="3a367-128">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="3a367-129">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3a367-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
