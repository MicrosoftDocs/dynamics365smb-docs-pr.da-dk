---
title: Workflow | Microsoft Docs
description: Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 38092f364d1dee1f34d8aa0c0858ac1bc04d829b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378794"
---
# <a name="workflows-in-dynamics-365-business-central"></a><span data-ttu-id="c9821-105">Workflows i Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="c9821-105">Workflows in Dynamics 365 Business Central</span></span>

<span data-ttu-id="c9821-106">Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere.</span><span class="sxs-lookup"><span data-stu-id="c9821-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="c9821-107">Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver.</span><span class="sxs-lookup"><span data-stu-id="c9821-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="c9821-108">Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin.</span><span class="sxs-lookup"><span data-stu-id="c9821-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="c9821-109">På siden **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne.</span><span class="sxs-lookup"><span data-stu-id="c9821-109">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="c9821-110">Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder.</span><span class="sxs-lookup"><span data-stu-id="c9821-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="c9821-111">Du definerer arbejdsgangstrin ved at udfylde felter om arbejdsganglinjer fra faste lister over hændelses- og svarværdier, der repræsenterer scenarier, der understøttes af programkoden.</span><span class="sxs-lookup"><span data-stu-id="c9821-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span>  

 <span data-ttu-id="c9821-112">Den generiske version af [!INCLUDE[prod_short](includes/prod_short.md)] indeholder en række forudkonfigurerede workflows, som repræsenteres af workflowskabeloner, som du kan kopiere for at oprette workflows.</span><span class="sxs-lookup"><span data-stu-id="c9821-112">The generic version of [!INCLUDE[prod_short](includes/prod_short.md)] includes a number of preconfigured workflows represented by workflow templates that you can copy to create workflows.</span></span> <span data-ttu-id="c9821-113">Koden for workflowskabeloner, som er tilføjet af Microsoft, har "MS" foran som f.eks. i "MS-".</span><span class="sxs-lookup"><span data-stu-id="c9821-113">The code for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span> <span data-ttu-id="c9821-114">Du kan finde flere oplysninger på listen med workflowskabeloner på siden Workflowskabeloner.</span><span class="sxs-lookup"><span data-stu-id="c9821-114">For more information, see the list of workflow templates in the Workflow Templates page.</span></span>  

 <span data-ttu-id="c9821-115">Hvis et virksomhedsscenarie kræver en workflowhændelse eller et svar, der ikke understøttes, skal du enten bruge Power Automate eller en Microsoft-partner til at tilpasse programkoden.</span><span class="sxs-lookup"><span data-stu-id="c9821-115">If a business scenario requires a workflow event or response that is not supported, you can either use Power Automate or work with a Microsoft partner to customize the application code.</span></span> <span data-ttu-id="c9821-116">Du kan finde flere oplysninger under [Bruge [!INCLUDE[prod_short](includes/prod_short.md)] i et automatisk workflow](across-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="c9821-116">For more information, see [Using [!INCLUDE[prod_short](includes/prod_short.md)] in an Automated Workflow](across-how-use-financials-data-source-flow.md).</span></span>

<span data-ttu-id="c9821-117">Alle workflowskabeloner, som du opretter med, Power Automate, føjes til listen over workflowskabeloner i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="c9821-117">Any workflow template that you create with Power Automate is added to the list of workflow templates within [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="c9821-118">Du kan finde flere oplysninger i [Bruge Business Central i et automatisk workflow](across-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="c9821-118">For more information, see [Using Business Central in an Automated Workflow](across-how-use-financials-data-source-flow.md).</span></span>  

 <span data-ttu-id="c9821-119">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="c9821-119">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="c9821-120">**For at**</span><span class="sxs-lookup"><span data-stu-id="c9821-120">**To**</span></span>|<span data-ttu-id="c9821-121">**Skal du se**</span><span class="sxs-lookup"><span data-stu-id="c9821-121">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="c9821-122">Oprette arbejdsgangbrugere, angive, hvordan brugere modtager notifikationer, og oprette nye arbejdsgange.</span><span class="sxs-lookup"><span data-stu-id="c9821-122">Set up workflow users, specify how users get notified, and create new workflows.</span></span> <span data-ttu-id="c9821-123">Implementer de krævede arbejdsgangelementer ved at tilpasse programkoden for nye arbejdsgange for ikke-understøttede scenarier.</span><span class="sxs-lookup"><span data-stu-id="c9821-123">For new workflows for unsupported scenarios, implement the required workflow elements by customizing the application code.</span></span>|[<span data-ttu-id="c9821-124">Opsætte workflows</span><span class="sxs-lookup"><span data-stu-id="c9821-124">Setting Up Workflows</span></span>](across-set-up-workflows.md)|  
|<span data-ttu-id="c9821-125">Aktiver arbejdsgange, behandl meddelelser i arbejdsgangen, herunder godkendelser og godkendelsesanmodninger om at udføre trin i en arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="c9821-125">Enable workflows, act on workflow notifications, including request approvals and approve requests to perform a workflow step.</span></span> <span data-ttu-id="c9821-126">Arkiver og slet arbejdsgange.</span><span class="sxs-lookup"><span data-stu-id="c9821-126">Archive and delete workflows.</span></span>|[<span data-ttu-id="c9821-127">Anvende workflows</span><span class="sxs-lookup"><span data-stu-id="c9821-127">Using Workflows</span></span>](across-use-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="c9821-128">Se også</span><span class="sxs-lookup"><span data-stu-id="c9821-128">See Also</span></span>

[<span data-ttu-id="c9821-129">Salg</span><span class="sxs-lookup"><span data-stu-id="c9821-129">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="c9821-130">Køb</span><span class="sxs-lookup"><span data-stu-id="c9821-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="c9821-131">Administrere projekter</span><span class="sxs-lookup"><span data-stu-id="c9821-131">Managing Projects</span></span>](projects-manage-projects.md)  
<span data-ttu-id="c9821-132">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c9821-132">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]