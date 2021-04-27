---
title: Arbejdsgangsnotifikationer
description: Mange arbejdsgangssvar vedrører notifikationer til en bruger om, at der er forekommet en hændelse, som brugeren skal reagere på. F.eks. på kan hændelsen på ét arbejdsgangstrin være, at bruger 1 anmoder om godkendelse af en ny post, og svaret er, at der er sendt en notifikation til bruger 2, godkenderen. På næste arbejdsgangstrin kan hændelsen være, at bruger 2 godkender posten, og svaret er, at der er sendt en notifikation til bruger 3 om at påbegynde en relateret behandling af den godkendte post. For trin i arbejdsgangen, der vedrører godkendelse, er hver notifikation knyttet til en godkendelsespost.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d72c3ba220c98d0c77806466f467ab233b3db65c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787042"
---
# <a name="workflow-notifications"></a><span data-ttu-id="472d8-106">Arbejdsgangsnotifikationer</span><span class="sxs-lookup"><span data-stu-id="472d8-106">Workflow Notifications</span></span>

<span data-ttu-id="472d8-107">Konfigurere arbejdsgange, så brugerne automatisk får besked, når de skal være opmærksomme på et trin i den arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="472d8-107">Set up your workflows to automatically notify users when their attention is required for a step in that workflow.</span></span> <span data-ttu-id="472d8-108">Mange arbejdsgangssvar vedrører notifikationer til en bruger om, at der er forekommet en hændelse, som brugeren skal reagere på.</span><span class="sxs-lookup"><span data-stu-id="472d8-108">Many workflow responses are about notifying a user that an event has occurred that they must act on.</span></span> <span data-ttu-id="472d8-109">F.eks. på kan hændelsen på ét arbejdsgangstrin være, at bruger 1 anmoder om godkendelse af en ny post, og svaret er, at der er sendt en notifikation til bruger 2, godkenderen.</span><span class="sxs-lookup"><span data-stu-id="472d8-109">For example, on one workflow step, the event can be that User 1 requests approval of a new record, and the response is that a notification is sent to User 2, the approver.</span></span> <span data-ttu-id="472d8-110">På næste arbejdsgangstrin kan hændelsen være, at bruger 2 godkender posten, og svaret er, at der er sendt en notifikation til bruger 3 om at påbegynde en relateret behandling af den godkendte post.</span><span class="sxs-lookup"><span data-stu-id="472d8-110">On the next workflow step, the event can be that User 2 approves the record, and the response is that a notification is sent to User 3 to start a related processing of the approved record.</span></span> <span data-ttu-id="472d8-111">For trin i arbejdsgangen, der vedrører godkendelse, er hver notifikation knyttet til en godkendelsespost.</span><span class="sxs-lookup"><span data-stu-id="472d8-111">For workflow steps that are about approval, each notification is tied to an approval entry.</span></span> <span data-ttu-id="472d8-112">Du kan finde flere oplysninger i [Workflow](across-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="472d8-112">For more information, see [Workflow](across-workflow.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="472d8-113">Den generiske version af [!INCLUDE[prod_short](includes/prod_short.md)] understøtter notifikationer som mail og som interne noter.</span><span class="sxs-lookup"><span data-stu-id="472d8-113">The generic version of [!INCLUDE[prod_short](includes/prod_short.md)] supports notifications as email and as internal notes.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="472d8-114">Alle arbejdsgangsnotifikationer sendes via en opgavekø.</span><span class="sxs-lookup"><span data-stu-id="472d8-114">All workflow notifications are sent through a job queue.</span></span> <span data-ttu-id="472d8-115">Kontrollér, at opgavekøen i installationen er konfigureret til at håndtere arbejdsgangsnotifikationer, og at afkrydsningsfeltet **Start automatisk fra server** er markeret.</span><span class="sxs-lookup"><span data-stu-id="472d8-115">Make sure that the job queue in your installation is set up to handle workflow notifications, and that the **Start Automatically From Server** check box is selected.</span></span> <span data-ttu-id="472d8-116">Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="472d8-116">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

## <a name="set-up-notifications"></a><span data-ttu-id="472d8-117">Opsætning af notifikationer.</span><span class="sxs-lookup"><span data-stu-id="472d8-117">Set up notifications</span></span>

<span data-ttu-id="472d8-118">Du konfigurerer forskellige aspekter af arbejdsgangsnotifikationer følgende steder:</span><span class="sxs-lookup"><span data-stu-id="472d8-118">You set up different aspects of workflow notifications in the following places:</span></span>  

* <span data-ttu-id="472d8-119">Godkender notifikation</span><span class="sxs-lookup"><span data-stu-id="472d8-119">Approver notification</span></span>

    <span data-ttu-id="472d8-120">For godkendelsesarbejdsgange konfigurerer du modtagerne af arbejdsgangsnotifikationer ved at udfylde en linje på siden **Konfiguration af godkendelsesbruger** for hver bruger, der indgår i arbejdsprocessen.</span><span class="sxs-lookup"><span data-stu-id="472d8-120">For approval workflows, you set up the recipients of workflow notifications by filling a line on the **Approval User Setup** page for each user that takes part in the workflow.</span></span>  

    <span data-ttu-id="472d8-121">Hvis f.eks. bruger 2 angives i feltet **Godkender-id** på linjen for bruger 1, sendes notifikationen for godkendelsesanmodningen til bruger 1.</span><span class="sxs-lookup"><span data-stu-id="472d8-121">For example, if User 2 is specified in the **Approver ID** field on the line for User 1, then the approval request notification is sent to User 1.</span></span> <span data-ttu-id="472d8-122">Du kan finde flere oplysninger i [Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)</span><span class="sxs-lookup"><span data-stu-id="472d8-122">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>  
* <span data-ttu-id="472d8-123">Notifikationsplaner</span><span class="sxs-lookup"><span data-stu-id="472d8-123">Notification schedules</span></span>

    <span data-ttu-id="472d8-124">Du kan konfigurere, hvornår og hvordan brugere får arbejdsgangsnotifikationer, ved at udfylde siden **Notifikationsplan** for hver bruger i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="472d8-124">You set up when and how users receive workflow notifications by filling the **Notification Schedule** page for each workflow user.</span></span> <span data-ttu-id="472d8-125">Du kan finde flere oplysninger i [Angive, hvornår og hvordan notifikationer modtages](across-how-to-specify-when-and-how-to-receive-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="472d8-125">For more information, see [Specify When and How to Receive Notifications](across-how-to-specify-when-and-how-to-receive-notifications.md).</span></span>  
* <span data-ttu-id="472d8-126">Tilpas e-mailnotifikationer</span><span class="sxs-lookup"><span data-stu-id="472d8-126">Customize the email notifications</span></span>

    <span data-ttu-id="472d8-127">Hvis du vil, kan du tilpasse indholdet af e-mailmeddelelserne ved at tilpasse rapport 1320, Notifikationsmail.</span><span class="sxs-lookup"><span data-stu-id="472d8-127">If you want, you can customize the content of the email notification by modifying report 1320, Notification Email.</span></span> <span data-ttu-id="472d8-128">Du kan finde flere oplysninger i [Oprette og ændre et brugerdefineret rapportlayouts](ui-how-create-custom-report-layout.md).</span><span class="sxs-lookup"><span data-stu-id="472d8-128">For more information, see [Create and Modify Custom Report Layouts](ui-how-create-custom-report-layout.md).</span></span>  
* <span data-ttu-id="472d8-129">Svarmuligheder</span><span class="sxs-lookup"><span data-stu-id="472d8-129">Response options</span></span>

    <span data-ttu-id="472d8-130">Du konfigurerer det specifikke indhold og de specifikke regler for en arbejdsgangsnotifikation, når du opretter den pågældende arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="472d8-130">You set up specific content and rules of a workflow notification when you create the workflow in question.</span></span> <span data-ttu-id="472d8-131">Det gør du ved at vælge indstillinger på siden **Indstillinger for workflowrespons** for det arbejdsgangssvar, der repræsenterer notifikationen.</span><span class="sxs-lookup"><span data-stu-id="472d8-131">You do this by selecting options on the **Workflow Response Options** page for the workflow response that represents the notification.</span></span> <span data-ttu-id="472d8-132">Du kan finde flere oplysninger i trin 9 i [Oprette arbejdsgange](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="472d8-132">For more information, see step 9 in [Create Workflows](across-how-to-create-workflows.md).</span></span>  

* <span data-ttu-id="472d8-133">Giv afsender besked</span><span class="sxs-lookup"><span data-stu-id="472d8-133">Notify sender</span></span>

    <span data-ttu-id="472d8-134">I forbindelse med godkendelsesarbejdsprocesser skal du tilføje et trin i arbejdsgangs svaret for at give afsenderen besked, når anmodningen er godkendt eller afvist.</span><span class="sxs-lookup"><span data-stu-id="472d8-134">For approval workflows, add a workflow response step to notify the sender when the request has been approved or rejected.</span></span> <span data-ttu-id="472d8-135">Du kan finde flere oplysninger i trin 9 i [Oprette arbejdsgange](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="472d8-135">For more information, see step 9 in [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="472d8-136">Se også</span><span class="sxs-lookup"><span data-stu-id="472d8-136">See Also</span></span>

[<span data-ttu-id="472d8-137">Konfigurere godkendelsesbrugere</span><span class="sxs-lookup"><span data-stu-id="472d8-137">Set Up Approval Users</span></span>](across-how-to-set-up-approval-users.md)  
[<span data-ttu-id="472d8-138">Oprette brugere til arbejdsgange</span><span class="sxs-lookup"><span data-stu-id="472d8-138">Set Up Workflow Users</span></span>](across-how-to-set-up-workflow-users.md)  
[<span data-ttu-id="472d8-139">Angive, hvornår og hvordan notifikationer modtages</span><span class="sxs-lookup"><span data-stu-id="472d8-139">Specify When and How to Receive Notifications</span></span>](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[<span data-ttu-id="472d8-140">Oprette arbejdsgange</span><span class="sxs-lookup"><span data-stu-id="472d8-140">Create Workflows</span></span>](across-how-to-create-workflows.md)  
[<span data-ttu-id="472d8-141">Sådan opretter og ændrer du Brugerdefinerede rapportlayouts</span><span class="sxs-lookup"><span data-stu-id="472d8-141">Create and Modify Custom Report Layouts</span></span>](ui-how-create-custom-report-layout.md)  
[<span data-ttu-id="472d8-142">Du kan bruge opgavekøer til at planlægge opgaver</span><span class="sxs-lookup"><span data-stu-id="472d8-142">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
[<span data-ttu-id="472d8-143">Konfigurere mail</span><span class="sxs-lookup"><span data-stu-id="472d8-143">Set up Email</span></span>](admin-how-setup-email.md)  
[<span data-ttu-id="472d8-144">Gennemgang: Opsætning og brug af workflow for godkendelse af køb</span><span class="sxs-lookup"><span data-stu-id="472d8-144">Walkthrough: Setting Up and Using a Purchase Approval Workflow</span></span>](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[<span data-ttu-id="472d8-145">Workflow</span><span class="sxs-lookup"><span data-stu-id="472d8-145">Workflow</span></span>](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]