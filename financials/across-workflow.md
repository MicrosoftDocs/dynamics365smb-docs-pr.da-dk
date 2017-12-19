---
title: Workflow | Microsoft Docs
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
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: a49e50213f808fb72b43dfa22a34833b306ef12d
ms.openlocfilehash: 58f2aa5a26275820d0fafcc79fec5be118857d78
ms.contentlocale: da-dk
ms.lasthandoff: 12/14/2017

---
# <a name="workflow"></a><span data-ttu-id="c0f67-105">Workflow</span><span class="sxs-lookup"><span data-stu-id="c0f67-105">Workflow</span></span>
<span data-ttu-id="c0f67-106">Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere.</span><span class="sxs-lookup"><span data-stu-id="c0f67-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="c0f67-107">Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver.</span><span class="sxs-lookup"><span data-stu-id="c0f67-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="c0f67-108">Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin.</span><span class="sxs-lookup"><span data-stu-id="c0f67-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="c0f67-109">I vinduet **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne.</span><span class="sxs-lookup"><span data-stu-id="c0f67-109">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="c0f67-110">Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder.</span><span class="sxs-lookup"><span data-stu-id="c0f67-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="c0f67-111">Du definerer arbejdsgangstrin ved at udfylde felter om arbejdsganglinjer fra faste lister over hændelses- og svarværdier, der repræsenterer scenarier, der understøttes af programkoden.</span><span class="sxs-lookup"><span data-stu-id="c0f67-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span>  

 <span data-ttu-id="c0f67-112">Den generiske version af [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder en række forudkonfigurerede workflows, som repræsenteres af workflowskabeloner, som du kan kopiere for at oprette workflows.</span><span class="sxs-lookup"><span data-stu-id="c0f67-112">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] includes a number of preconfigured workflows represented by workflow templates that you can copy to create workflows.</span></span> <span data-ttu-id="c0f67-113">Koden for workflowskabeloner, som er tilføjet af Microsoft, har "MS" foran som f.eks. i "MS-".</span><span class="sxs-lookup"><span data-stu-id="c0f67-113">The code for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span> <span data-ttu-id="c0f67-114">Du kan finde flere oplysninger på listen med workflowskabeloner i vinduet Workflowskabeloner.</span><span class="sxs-lookup"><span data-stu-id="c0f67-114">For more information, see the list of workflow templates in the Workflow Templates window.</span></span>  

 <span data-ttu-id="c0f67-115">Hvis et virksomhedsscenarie kræver en workflowhændelse eller et svar, der ikke understøttes, skal en Microsoft-partner implementere dem ved at tilpasse programkoden.</span><span class="sxs-lookup"><span data-stu-id="c0f67-115">If a business scenario requires a workflow event or response that is not supported, a Microsoft partner must implement them by customizing the application code.</span></span> <span data-ttu-id="c0f67-116">Du kan finde flere oplysninger i [Gennemgang: Implementering af nye workflowhændelser og -responser](/dynamics_nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) i hjælpen til udviklere og it-eksperter.</span><span class="sxs-lookup"><span data-stu-id="c0f67-116">For more information, see [Walkthrough: Implementing New Workflow Events and Responses](/dynamics_nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) in the developer and IT-pro help.</span></span>  

 <span data-ttu-id="c0f67-117">Følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="c0f67-117">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="c0f67-118">**For at**</span><span class="sxs-lookup"><span data-stu-id="c0f67-118">**To**</span></span>|<span data-ttu-id="c0f67-119">**Skal du se**</span><span class="sxs-lookup"><span data-stu-id="c0f67-119">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="c0f67-120">Oprette arbejdsgangbrugere, angive, hvordan brugere modtager notifikationer, og oprette nye arbejdsgange.</span><span class="sxs-lookup"><span data-stu-id="c0f67-120">Set up workflow users, specify how users get notified, and create new workflows.</span></span> <span data-ttu-id="c0f67-121">Implementer de krævede arbejdsgangelementer ved at tilpasse programkoden for nye arbejdsgange for ikke-understøttede scenarier.</span><span class="sxs-lookup"><span data-stu-id="c0f67-121">For new workflows for unsupported scenarios, implement the required workflow elements by customizing the application code.</span></span>|[<span data-ttu-id="c0f67-122">Opsætte workflows</span><span class="sxs-lookup"><span data-stu-id="c0f67-122">Setting Up Workflows</span></span>](across-set-up-workflows.md)|  
|<span data-ttu-id="c0f67-123">Aktiver arbejdsgange, behandl meddelelser i arbejdsgangen, herunder godkendelser og godkendelsesanmodninger om at udføre trin i en arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="c0f67-123">Enable workflows, act on workflow notifications, including request approvals and approve requests to perform a workflow step.</span></span> <span data-ttu-id="c0f67-124">Arkiver og slet arbejdsgange.</span><span class="sxs-lookup"><span data-stu-id="c0f67-124">Archive and delete workflows.</span></span>|[<span data-ttu-id="c0f67-125">Anvende workflows</span><span class="sxs-lookup"><span data-stu-id="c0f67-125">Using Workflows</span></span>](across-use-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="c0f67-126">Se også</span><span class="sxs-lookup"><span data-stu-id="c0f67-126">See Also</span></span>  
[<span data-ttu-id="c0f67-127">Salg</span><span class="sxs-lookup"><span data-stu-id="c0f67-127">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="c0f67-128">Køb</span><span class="sxs-lookup"><span data-stu-id="c0f67-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="c0f67-129">Administrere projekter</span><span class="sxs-lookup"><span data-stu-id="c0f67-129">Managing Projects</span></span>](projects-manage-projects.md)  
<span data-ttu-id="c0f67-130">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c0f67-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

