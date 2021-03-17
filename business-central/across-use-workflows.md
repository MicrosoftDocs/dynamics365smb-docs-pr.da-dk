---
title: Anvende workflows
description: Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Få mere at vide om de forskellige trin, du skal udføre for at begynde at bruge arbejdsgange.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fc2917a304a5a43228f9156dffd0a9a8011f9047
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378894"
---
# <a name="using-workflows"></a><span data-ttu-id="ea5fa-104">Anvende workflows</span><span class="sxs-lookup"><span data-stu-id="ea5fa-104">Using Workflows</span></span>
<span data-ttu-id="ea5fa-105">Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere.</span><span class="sxs-lookup"><span data-stu-id="ea5fa-105">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="ea5fa-106">Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver.</span><span class="sxs-lookup"><span data-stu-id="ea5fa-106">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="ea5fa-107">Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin.</span><span class="sxs-lookup"><span data-stu-id="ea5fa-107">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="ea5fa-108">Inden du kan bruge arbejdsprocesser, skal du oprette arbejdsgangbrugere, oprette arbejdsgangene, som kan være med tilpasning af kode, og angive, hvordan brugere får vist meddelelser.</span><span class="sxs-lookup"><span data-stu-id="ea5fa-108">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="ea5fa-109">Du kan finde flere oplysninger under [Opsætte workflows](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="ea5fa-109">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ea5fa-110">Typiske arbejdsgangstrin er om brugere, der anmoder om godkendelse af opgaver, og godkendere, der accepterer eller afviser godkendelsesanmodninger.</span><span class="sxs-lookup"><span data-stu-id="ea5fa-110">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="ea5fa-111">Derfor henviser mange emner om brug af workflows til godkendelser.</span><span class="sxs-lookup"><span data-stu-id="ea5fa-111">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="ea5fa-112">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="ea5fa-112">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="ea5fa-113">**For at**</span><span class="sxs-lookup"><span data-stu-id="ea5fa-113">**To**</span></span>|<span data-ttu-id="ea5fa-114">**Skal du se**</span><span class="sxs-lookup"><span data-stu-id="ea5fa-114">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="ea5fa-115">Angiv, at en arbejdsgang skal startes, når den første startpunkthændelse finder sted.</span><span class="sxs-lookup"><span data-stu-id="ea5fa-115">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="ea5fa-116">Aktivere arbejdsgange</span><span class="sxs-lookup"><span data-stu-id="ea5fa-116">Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="ea5fa-117">Anmode om godkendelse af en opgave, som godkender, godkende, afvise eller uddelegere godkendelser og sende eller få vist godkendelsesnotifikationer.</span><span class="sxs-lookup"><span data-stu-id="ea5fa-117">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="ea5fa-118">Bruge godkendelsesworkflows</span><span class="sxs-lookup"><span data-stu-id="ea5fa-118">Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="ea5fa-119">Opret arbejdsgangstrin, der sikrer, at en bestemt posttype ikke bruges, før en bestemt hændelse opstår, for eksempel at posten godkendes.</span><span class="sxs-lookup"><span data-stu-id="ea5fa-119">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="ea5fa-120">Begrænse og tillade brugen af en record</span><span class="sxs-lookup"><span data-stu-id="ea5fa-120">Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="ea5fa-121">Vis arbejdsgangstrinsforekomster med statussen Afsluttet.</span><span class="sxs-lookup"><span data-stu-id="ea5fa-121">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="ea5fa-122">Vise arkiverede forekomster af arbejdsgangstrin</span><span class="sxs-lookup"><span data-stu-id="ea5fa-122">View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="ea5fa-123">Slet en arbejdsgang, som du er sikker på ikke længere bruges.</span><span class="sxs-lookup"><span data-stu-id="ea5fa-123">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="ea5fa-124">Slette arbejdsgange</span><span class="sxs-lookup"><span data-stu-id="ea5fa-124">Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="ea5fa-125">Se også</span><span class="sxs-lookup"><span data-stu-id="ea5fa-125">See Also</span></span>  
<span data-ttu-id="ea5fa-126">[Opsætte workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="ea5fa-126">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="ea5fa-127">[Workflow](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="ea5fa-127">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="ea5fa-128">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ea5fa-128">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]