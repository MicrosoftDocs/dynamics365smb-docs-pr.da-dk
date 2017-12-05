---
title: "Sådan konfigurerer du godkendelsesbrugere | Microsoft Docs"
description: "Før du kan oprette workflows, der omfatter godkendelsestrin, skal du angive workflowbrugere, der er involveret i godkendelsesprocessen. I feltet Konfiguration af godkendelsesbruger skal du også angive beløbsgrænser for bestemte typer anmodninger og angive stedfortrædende godkendere, som godkendelsesanmodninger skal uddelegeres til, når den oprindelige godkender er fraværende."
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
ms.openlocfilehash: 49ffa181e653377f3684d138b6ee7df3775a87f6
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-approval-users"></a><span data-ttu-id="a90e7-104">Fremgangsmåde: Konfigurere godkendelsesbrugere</span><span class="sxs-lookup"><span data-stu-id="a90e7-104">How to: Set Up Approval Users</span></span>
<span data-ttu-id="a90e7-105">Før du kan oprette workflows, der omfatter godkendelsestrin, skal du angive workflowbrugere, der er involveret i godkendelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="a90e7-105">Before you can create workflows that involve approval steps, you must set up the workflow users who are involved in approval processes.</span></span> <span data-ttu-id="a90e7-106">I feltet **Konfiguration af godkendelsesbruger** skal du også angive beløbsgrænser for bestemte typer anmodninger og angive stedfortrædende godkendere, som godkendelsesanmodninger skal uddelegeres til, når den oprindelige godkender er fraværende.</span><span class="sxs-lookup"><span data-stu-id="a90e7-106">In the **Approval User Setup** window, you also set amount limits for specific types of requests and define substitute approvers to whom approval requests are delegated when the original approver is absent.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a90e7-107">Godkendelsesbrugerne, dvs. både godkendelsesanmodere og godkendere, skal først konfigureres som workflowbrugere i vinduet **Brugergruppe for workflow**.</span><span class="sxs-lookup"><span data-stu-id="a90e7-107">Approval users, both approval requesters and approvers, must first be set up as workflow users in the **Workflow User Group** window.</span></span> <span data-ttu-id="a90e7-108">Du kan finde flere oplysninger i [Fremgangsmåde: Oprette brugere til arbejdsgange](across-how-to-set-up-workflow-users.md).</span><span class="sxs-lookup"><span data-stu-id="a90e7-108">For more information, see [How to: Set Up Workflow Users](across-how-to-set-up-workflow-users.md).</span></span>  

 <span data-ttu-id="a90e7-109">Når du har angivet godkendelsesbrugere, kan du bruge opsætningen til at oprette arbejdsgangssvar for godkendelsesarbejdsgange.</span><span class="sxs-lookup"><span data-stu-id="a90e7-109">When you have set up approval users, you can use the setup to create workflow responses for approval workflows.</span></span> <span data-ttu-id="a90e7-110">Du kan finde flere oplysninger i trin 9 i [Fremgangsmåde: Oprette arbejdsgange](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="a90e7-110">For more information, see step 9 in [How to: Create Workflows](across-how-to-create-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a90e7-111">Hvis du vil angive, at en godkendelsesanmodning ikke er godkendt, før flere godkendere i en godkendelseskæde har godkendt den, skal du konfigurere godkendere i et hierarki.</span><span class="sxs-lookup"><span data-stu-id="a90e7-111">To define that an approval request is not approved until multiple approvers in an approval chain have approved it, set up approvers in a hierarchy.</span></span> <span data-ttu-id="a90e7-112">For godkendertypen **Godkender** skal du konfigurere godkendere i vinduet **Konfiguration af godkendelsesbruger**.</span><span class="sxs-lookup"><span data-stu-id="a90e7-112">For approver type **Approver**, set approvers up in the **Approval User Setup** window.</span></span> <span data-ttu-id="a90e7-113">For godkendertypen **Brugergruppe for workflow** skal du konfigurere godkendere i vinduet **Brugergrupper for workflow** og definere hierarkiet ved at tildele trinvise tal til hver enkelt godkender i feltet **Rækkefølgenr.**.</span><span class="sxs-lookup"><span data-stu-id="a90e7-113">For approver type, **Workflow User Group**, set approvers up in the **Workflow User Groups** window and define the hierarchy by assigning incremental numbers to each approver in the **Sequence No.**</span></span> <span data-ttu-id="a90e7-114">.</span><span class="sxs-lookup"><span data-stu-id="a90e7-114">field.</span></span> <span data-ttu-id="a90e7-115">Du kan finde flere oplysninger i dette emne og i [Fremgangsmåde: Oprette brugere til arbejdsgange](across-how-to-set-up-workflow-users.md).</span><span class="sxs-lookup"><span data-stu-id="a90e7-115">For more information, see this topic and [How to: Set Up Workflow Users](across-how-to-set-up-workflow-users.md).</span></span>  
>   
>  <span data-ttu-id="a90e7-116">Hvis du vil angive, at en godkendelsesanmodning ikke er godkendt, før flere lige godkendere har godkendt den, uanset et hierarki, skal du oprette en simpel brugergruppe til en arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="a90e7-116">To define that an approval request is not approved until multiple equal approvers have approved it, regardless of a hirarchy, set up a flat workflow user group.</span></span> <span data-ttu-id="a90e7-117">For godkendertypen **Brugergruppe for workflow** skal du konfigurere godkendere i vinduet **Brugergrupper for workflow** og tildele det samme nummer til hver godkender feltet **Rækkefølgenr.**.</span><span class="sxs-lookup"><span data-stu-id="a90e7-117">For approver type, **Workflow User Group**, set up approvers in the **Workflow User Groups** window and assign the same number to each approver in the **Sequence No.**</span></span> <span data-ttu-id="a90e7-118">.</span><span class="sxs-lookup"><span data-stu-id="a90e7-118">field.</span></span> <span data-ttu-id="a90e7-119">Du kan finde flere oplysninger i [Fremgangsmåde: Oprette brugere til arbejdsgange](across-how-to-set-up-workflow-users.md).</span><span class="sxs-lookup"><span data-stu-id="a90e7-119">For more information, see [How to: Set Up Workflow Users](across-how-to-set-up-workflow-users.md).</span></span>  

## <a name="to-set-up-an-approval-user"></a><span data-ttu-id="a90e7-120">Sådan konfigureres en godkendelsesbruger</span><span class="sxs-lookup"><span data-stu-id="a90e7-120">To set up an approval user</span></span>  
1. <span data-ttu-id="a90e7-121">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Brugeropsætning af godkendelser**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="a90e7-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Approval User Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a90e7-122">Opret en ny linje vinduet **Konfiguration af godkendelsesbruger**, og udfyld felterne som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="a90e7-122">Create a new line in the **Approval User Setup** window, and then fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="a90e7-123">Felt</span><span class="sxs-lookup"><span data-stu-id="a90e7-123">Field</span></span>|<span data-ttu-id="a90e7-124">Description</span><span class="sxs-lookup"><span data-stu-id="a90e7-124">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="a90e7-125">**Bruger-id**</span><span class="sxs-lookup"><span data-stu-id="a90e7-125">**User ID**</span></span>|<span data-ttu-id="a90e7-126">Vælg bruger-id'et for den bruger, der er involveret i godkendelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="a90e7-126">Select the user ID of the user who is involved in the approval process.</span></span>|  
    |<span data-ttu-id="a90e7-127">**Sælger/indkøberkode**</span><span class="sxs-lookup"><span data-stu-id="a90e7-127">**Salespers./Purch. Code**</span></span>|<span data-ttu-id="a90e7-128">Angiv den sælger- eller indkøberkode, der gælder for brugeren, i feltet **Sælger/indkøberkode**.</span><span class="sxs-lookup"><span data-stu-id="a90e7-128">Specify the salesperson or purchaser code that applies to the user in the **Salespers./Purch. Code** field.</span></span><br /><br /> <span data-ttu-id="a90e7-129">Du udfylder typisk feltet **Sælger/indkøberkode**, hvis den sælger eller indkøber, der er ansvarlig for kunden eller leverandøren, også er den person, der skal godkende salgs- eller købsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="a90e7-129">You typically fill the **Salespers./Purch. Code** field if the salesperson or purchaser who is responsible for the customer or vendor is also the person who must approve the sales or purchase request in question.</span></span>|  
    |<span data-ttu-id="a90e7-130">**Godkender-id**</span><span class="sxs-lookup"><span data-stu-id="a90e7-130">**Approver ID**</span></span>|<span data-ttu-id="a90e7-131">Vælg bruger-id'et for den bruger, der skal godkende anmodninger fra brugeren, i feltet **Bruger-id**.</span><span class="sxs-lookup"><span data-stu-id="a90e7-131">Select the user ID of the user who must approve requests made by the user in the **User ID** field.</span></span>|  
    |<span data-ttu-id="a90e7-132">**Godkendelsesgrænse for salgsbeløb**</span><span class="sxs-lookup"><span data-stu-id="a90e7-132">**Sales Amount Approval Limit**</span></span>|<span data-ttu-id="a90e7-133">Angiv det maksimale salgsbeløb i RV, som brugeren i feltet **Bruger-id** kan godkende.</span><span class="sxs-lookup"><span data-stu-id="a90e7-133">Specify the maximum sales amount in LCY that the user in the **User ID** field can approve.</span></span>|  
    |<span data-ttu-id="a90e7-134">**Ubegrænset salgsgodkendelse**</span><span class="sxs-lookup"><span data-stu-id="a90e7-134">**Unlimited Sales Approval**</span></span>|<span data-ttu-id="a90e7-135">Angiv, at brugeren i feltet **Bruger-id** kan godkende alle salgsanmodninger uanset deres beløb.</span><span class="sxs-lookup"><span data-stu-id="a90e7-135">Specify that the user in the **User ID** field can approve all sales requests regardless of their amount.</span></span><br /><br /> <span data-ttu-id="a90e7-136">Hvis du markerer dette afkrydsningsfelt, kan du ikke udfylde feltet **Godkendelsesgrænse for salgsbeløb**.</span><span class="sxs-lookup"><span data-stu-id="a90e7-136">If you select this check box, then you cannot fill the **Sales Amount Approval Limit** field.</span></span>|  
    |<span data-ttu-id="a90e7-137">**Godkendelsesgrænse for indkøbsbeløb**</span><span class="sxs-lookup"><span data-stu-id="a90e7-137">**Purchase Amount Approval Limit**</span></span>|<span data-ttu-id="a90e7-138">Angiv det maksimale købsbeløb i RV, som brugeren i feltet **Bruger-id** kan godkende.</span><span class="sxs-lookup"><span data-stu-id="a90e7-138">Specify the maximum purchase amount in LCY that the user in the **User ID** field can approve.</span></span>|  
    |<span data-ttu-id="a90e7-139">**Ubegrænset indkøbsgodkendelse**</span><span class="sxs-lookup"><span data-stu-id="a90e7-139">**Unlimited Purchase Approval**</span></span>|<span data-ttu-id="a90e7-140">Angiv, at brugeren i feltet **Bruger-id** kan godkende alle købsanmodninger uanset deres beløb.</span><span class="sxs-lookup"><span data-stu-id="a90e7-140">Specify that the user in the **User ID** field can approve all purchase requests regardless of their amount.</span></span><br /><br /> <span data-ttu-id="a90e7-141">Hvis du markerer dette afkrydsningsfelt, kan du ikke udfylde feltet **Godkendelsesgrænse for salgsbeløb**.</span><span class="sxs-lookup"><span data-stu-id="a90e7-141">If you select this check box, then you cannot fill the **Sales Amount Approval Limit** field.</span></span>|  
    |<span data-ttu-id="a90e7-142">**Godkendelsesgrænse for anmodet beløb**</span><span class="sxs-lookup"><span data-stu-id="a90e7-142">**Request Amount Approval Limit**</span></span>|<span data-ttu-id="a90e7-143">Angiv det maksimale beløb i RV, som brugeren i feltet **Bruger-id** kan godkende for købsrekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="a90e7-143">Specify the maximum amount in LCY that the user in the **User ID** field can approve for purchase quotes.</span></span><br /><br /> <span data-ttu-id="a90e7-144">Hvis du vil bruge dette felt, skal du vælge indstillingen **Godkenderkæde** i feltet **Godkenders grænsetype** i vinduet **Workflowrespons**.</span><span class="sxs-lookup"><span data-stu-id="a90e7-144">To use this field, you must select the **Approver Chain** option in the **Approver Limit Type** field in the **Workflow Response** window.</span></span>|  
    |<span data-ttu-id="a90e7-145">**Ubegrænset anmodningsgodkendelse**</span><span class="sxs-lookup"><span data-stu-id="a90e7-145">**Unlimited Request Approval**</span></span>|<span data-ttu-id="a90e7-146">Angiv, at brugeren i feltet **Bruger-id** kan godkende alle købsrekvisitioner uanset deres beløb.</span><span class="sxs-lookup"><span data-stu-id="a90e7-146">Specify that the user in the **User ID** field can approve all purchase quotes regardless of their amount.</span></span><br /><br /> <span data-ttu-id="a90e7-147">Hvis du markerer dette afkrydsningsfelt, kan du ikke udfylde feltet **Godkendelsesgrænse for anmodet beløb**.</span><span class="sxs-lookup"><span data-stu-id="a90e7-147">If you select this check box, then you cannot fill the **Request Amount Approval Limit** field.</span></span>|  
    |<span data-ttu-id="a90e7-148">**Stedfortræder**</span><span class="sxs-lookup"><span data-stu-id="a90e7-148">**Substitute**</span></span>|<span data-ttu-id="a90e7-149">Vælg bruger-id'et for den bruger, der skal godkende anmodninger fra brugeren, i feltet **Bruger-id**, hvis brugeren i **Godkender-id** ikke er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="a90e7-149">Select the user ID of the user who must approve requests made by the user in the **User ID** field if the user in the **Approver ID** is not available.</span></span> <span data-ttu-id="a90e7-150">**Bemærk:** Stedfortræderen kan enten være brugeren i feltet **Stedfortræder**, den direkte godkender eller godkendelsesadministratoren, i nævnte rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="a90e7-150">**Note:**  The substitute can either be the user in the **Substitute** field, the direct approver, or the approval administrator, in that order of priority.</span></span> <span data-ttu-id="a90e7-151">Du kan finde flere oplysninger under [Fremgangsmåde: Bruge godkendelsesworkflows](across-how-use-approval-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="a90e7-151">For more information, see [How to: Use Approval Workflows](across-how-use-approval-workflows.md).</span></span>|  
    |<span data-ttu-id="a90e7-152">**Mailadresse**</span><span class="sxs-lookup"><span data-stu-id="a90e7-152">**Email**</span></span>|<span data-ttu-id="a90e7-153">Angiv mailadressen for brugeren i feltet **Bruger-id**.</span><span class="sxs-lookup"><span data-stu-id="a90e7-153">Specify the email address of the user in the **User ID** field.</span></span>|  
    |<span data-ttu-id="a90e7-154">**Godkendelsesadministrator**</span><span class="sxs-lookup"><span data-stu-id="a90e7-154">**Approval Administrator**</span></span>|<span data-ttu-id="a90e7-155">Angiv den bruger, der har tilladelse til at genåbne godkendelsesarbejdsgange, f.eks. ved at uddelegere godkendelsesanmodninger til nye stedfortrædende godkendere og slette forfaldne godkendelsesanmodninger.</span><span class="sxs-lookup"><span data-stu-id="a90e7-155">Specify the user who has rights to unblock approval workflows, for example, by delegating approval requests to new substitute approvers and deleting overdue approval requests.</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="a90e7-156">Funktionen af feltet **Godkenders grænsetype** gælder kun for funktionalitetsområde, hvor grænser kan defineres, nemlig godkendelser af salg og køb.</span><span class="sxs-lookup"><span data-stu-id="a90e7-156">The behavior of **Approver Limit Type** field only applies to application areas where limits can be defined, namely sales and purchase approvals.</span></span> <span data-ttu-id="a90e7-157">Alle andre godkendelsestyper, hvor grænser ikke gælder, fungerer altid som beskrevet for indstillingen **Direkte godkender**.</span><span class="sxs-lookup"><span data-stu-id="a90e7-157">Any other type of approval where limits do not apply will always behave as described for the **Direct Approver** option.</span></span>  

3. <span data-ttu-id="a90e7-158">Hvis du vil teste brugeropsætningen af godkendelsen, skal du vælge handlingen **Brugeropsætning af godkendelser - kontrol**.</span><span class="sxs-lookup"><span data-stu-id="a90e7-158">To test the approval user setup, choose the **Approval User Setup Test** action.</span></span>  
4. <span data-ttu-id="a90e7-159">Gentag trin 2 og 3 for hver bruger, du vil angive som en godkendelsesbruger.</span><span class="sxs-lookup"><span data-stu-id="a90e7-159">Repeat steps 2 and 3 for every user who you want to set up as an approval user.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a90e7-160">Se også</span><span class="sxs-lookup"><span data-stu-id="a90e7-160">See Also</span></span>  
<span data-ttu-id="a90e7-161">[Fremgangsmåde: Oprette brugere til arbejdsgange](across-how-to-set-up-workflow-users.md) </span><span class="sxs-lookup"><span data-stu-id="a90e7-161">[How to: Set Up Workflow Users](across-how-to-set-up-workflow-users.md) </span></span>  
<span data-ttu-id="a90e7-162">[Konfiguration af arbejdsgangsnotifikationer](across-setting-up-workflow-notifications.md) </span><span class="sxs-lookup"><span data-stu-id="a90e7-162">[Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md) </span></span>  
<span data-ttu-id="a90e7-163">[Fremgangsmåde: Oprette arbejdsgange](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="a90e7-163">[How to: Create Workflows](across-how-to-create-workflows.md) </span></span>  
<span data-ttu-id="a90e7-164">[Opsætte workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="a90e7-164">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="a90e7-165">[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="a90e7-165">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
[<span data-ttu-id="a90e7-166">Workflow</span><span class="sxs-lookup"><span data-stu-id="a90e7-166">Workflow</span></span>](across-workflow.md)   
