---
title: Workflow | Microsoft Docs
description: "Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin."
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
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 7a7782fcb51eb9078cb62c4892814cd178518332
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="workflow"></a><span data-ttu-id="7551e-105">Workflow</span><span class="sxs-lookup"><span data-stu-id="7551e-105">Workflow</span></span>
<span data-ttu-id="7551e-106">Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere.</span><span class="sxs-lookup"><span data-stu-id="7551e-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="7551e-107">Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver.</span><span class="sxs-lookup"><span data-stu-id="7551e-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="7551e-108">Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin.</span><span class="sxs-lookup"><span data-stu-id="7551e-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="7551e-109">I vinduet **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne.</span><span class="sxs-lookup"><span data-stu-id="7551e-109">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="7551e-110">Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder.</span><span class="sxs-lookup"><span data-stu-id="7551e-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="7551e-111">Du definerer arbejdsgangstrin ved at udfylde felter om arbejdsganglinjer fra faste lister over hændelses- og svarværdier, der repræsenterer scenarier, der understøttes af programkoden.</span><span class="sxs-lookup"><span data-stu-id="7551e-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span>  

 <span data-ttu-id="7551e-112">Den generiske version af [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder en række forudkonfigurerede workflows, som repræsenteres af workflowskabeloner, som du kan kopiere for at oprette workflows.</span><span class="sxs-lookup"><span data-stu-id="7551e-112">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] includes a number of preconfigured workflows represented by workflow templates that you can copy to create workflows.</span></span> <span data-ttu-id="7551e-113">Koden for workflowskabeloner, som er tilføjet af Microsoft, har "MS" foran som f.eks. i "MS-".</span><span class="sxs-lookup"><span data-stu-id="7551e-113">The code for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span> <span data-ttu-id="7551e-114">Du kan finde flere oplysninger på listen med workflowskabeloner i vinduet Workflowskabeloner.</span><span class="sxs-lookup"><span data-stu-id="7551e-114">For more information, see the list of workflow templates in the Workflow Templates window.</span></span>  

 <span data-ttu-id="7551e-115">Hvis et virksomhedsscenarie kræver en workflowhændelse eller et svar, der ikke understøttes, skal en Microsoft-partner implementere dem ved at tilpasse programkoden.</span><span class="sxs-lookup"><span data-stu-id="7551e-115">If a business scenario requires a workflow event or response that is not supported, a Microsoft partner must implement them by customizing the application code.</span></span> <span data-ttu-id="7551e-116">Du kan finde flere oplysninger i [Gennemgang: Implementering af nye workflowhændelser og -responser](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) i hjælpen til udviklere og it-eksperter.</span><span class="sxs-lookup"><span data-stu-id="7551e-116">For more information, see [Walkthrough: Implementing New Workflow Events and Responses](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) in the developer and IT-pro help.</span></span>

> [!NOTE]  
> <span data-ttu-id="7551e-117">Workflows kan også initieres fra Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="7551e-117">Workflows can also be initiated from Microsoft Flow.</span></span> <span data-ttu-id="7551e-118">Du kan finde flere oplysninger i [Bruge Business Central i et automatisk workflow](across-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="7551e-118">For more information, see [Using Business Central in an Automated Workflow](across-how-use-financials-data-source-flow.md).</span></span>  

 <span data-ttu-id="7551e-119">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="7551e-119">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="7551e-120">**For at**</span><span class="sxs-lookup"><span data-stu-id="7551e-120">**To**</span></span>|<span data-ttu-id="7551e-121">**Skal du se**</span><span class="sxs-lookup"><span data-stu-id="7551e-121">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="7551e-122">Oprette arbejdsgangbrugere, angive, hvordan brugere modtager notifikationer, og oprette nye arbejdsgange.</span><span class="sxs-lookup"><span data-stu-id="7551e-122">Set up workflow users, specify how users get notified, and create new workflows.</span></span> <span data-ttu-id="7551e-123">Implementer de krævede arbejdsgangelementer ved at tilpasse programkoden for nye arbejdsgange for ikke-understøttede scenarier.</span><span class="sxs-lookup"><span data-stu-id="7551e-123">For new workflows for unsupported scenarios, implement the required workflow elements by customizing the application code.</span></span>|[<span data-ttu-id="7551e-124">Opsætte workflows</span><span class="sxs-lookup"><span data-stu-id="7551e-124">Setting Up Workflows</span></span>](across-set-up-workflows.md)|  
|<span data-ttu-id="7551e-125">Aktiver arbejdsgange, behandl meddelelser i arbejdsgangen, herunder godkendelser og godkendelsesanmodninger om at udføre trin i en arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="7551e-125">Enable workflows, act on workflow notifications, including request approvals and approve requests to perform a workflow step.</span></span> <span data-ttu-id="7551e-126">Arkiver og slet arbejdsgange.</span><span class="sxs-lookup"><span data-stu-id="7551e-126">Archive and delete workflows.</span></span>|[<span data-ttu-id="7551e-127">Anvende workflows</span><span class="sxs-lookup"><span data-stu-id="7551e-127">Using Workflows</span></span>](across-use-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="7551e-128">Se også</span><span class="sxs-lookup"><span data-stu-id="7551e-128">See Also</span></span>  
[<span data-ttu-id="7551e-129">Salg</span><span class="sxs-lookup"><span data-stu-id="7551e-129">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="7551e-130">Køb</span><span class="sxs-lookup"><span data-stu-id="7551e-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="7551e-131">Administrere projekter</span><span class="sxs-lookup"><span data-stu-id="7551e-131">Managing Projects</span></span>](projects-manage-projects.md)  
<span data-ttu-id="7551e-132">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7551e-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

