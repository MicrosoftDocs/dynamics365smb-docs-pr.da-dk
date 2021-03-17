---
title: Oprette en sagssalgsfaktura for at fakturere for en sag | Microsoft Docs
description: Beskriver, hvordan du fakturerer debitorer for diverse udgifter, efterhånden som et projekt skrider frem.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 870151e5071ac82bbf913ee83ed567f29937c59f
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5376508"
---
# <a name="invoice-jobs"></a><span data-ttu-id="d7f66-103">Fakturere sager</span><span class="sxs-lookup"><span data-stu-id="d7f66-103">Invoice Jobs</span></span>
<span data-ttu-id="d7f66-104">I løbet af projektet kan der akkumuleres sagsomkostninger fra ressourceforbrug, materialer og sagsrelaterede indkøb.</span><span class="sxs-lookup"><span data-stu-id="d7f66-104">During the project, job costs from resource usage, materials, and job-related purchases can accumulate.</span></span> <span data-ttu-id="d7f66-105">Efterhånden som status for sagen ændrer sig, bogføres disse transaktioner i sagskladden.</span><span class="sxs-lookup"><span data-stu-id="d7f66-105">As the job progresses, these transactions get posted to the job journal.</span></span> <span data-ttu-id="d7f66-106">Det er vigtigt, at alle omkostninger er registreret i sagskladden, før du fakturerer kunden.</span><span class="sxs-lookup"><span data-stu-id="d7f66-106">It is important that all costs get recorded in the job journal before you invoice the customer.</span></span>

> [!NOTE]
> <span data-ttu-id="d7f66-107">Du kan også købe eksterne ressourcer uden relation til en sag, f. eks. for at fakturere en kreditor for udført arbejde.</span><span class="sxs-lookup"><span data-stu-id="d7f66-107">You can also purchase external resources unrelated to a job, for example, to invoice a vendor for work delivered.</span></span> <span data-ttu-id="d7f66-108">Du kan finde flere oplysninger under [Registrere køb](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="d7f66-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

<span data-ttu-id="d7f66-109">Du kan fakturere hele sagen fra siden **Sagsopgavelinjer** eller kun fakturere de valgte fakturerbare linjer fra siden **Planlægningslinjer**.</span><span class="sxs-lookup"><span data-stu-id="d7f66-109">You can invoice the whole job from the **Job Task Lines** page or only invoice selected billable lines from the **Planning Lines** page.</span></span> <span data-ttu-id="d7f66-110">Faktureringen kan foretages, når sagen er afsluttet, eller med bestemte intervaller, efterhånden som status for sagen ændres, baseret på en faktureringsplan.</span><span class="sxs-lookup"><span data-stu-id="d7f66-110">Invoicing can be done after the job is finished or at certain intervals during the job's progress based on an invoicing schedule.</span></span>

> [!NOTE]  
> <span data-ttu-id="d7f66-111">Hvis du vælger **Fakturerbar** i feltet **Linjetype for sag** på købsdokumenter for sagsrelaterede indkøb, oprettes der sagsplanlægningslinjer, som er klar til blive faktureret til kunden.</span><span class="sxs-lookup"><span data-stu-id="d7f66-111">If you select **Billable** in the **Job Line Type** field on the purchase documents for job-related purchases, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="d7f66-112">Du kan finde flere oplysninger i [Administrere projektforsyninger](projects-how-manage-project-supplies.md).</span><span class="sxs-lookup"><span data-stu-id="d7f66-112">For more information, see [Manage Project Supplies](projects-how-manage-project-supplies.md).</span></span>

## <a name="to-create-multiple-job-sales-invoices"></a><span data-ttu-id="d7f66-113">Sådan opretter du flere salgsfakturaer for sager</span><span class="sxs-lookup"><span data-stu-id="d7f66-113">To create multiple job sales invoices</span></span>
<span data-ttu-id="d7f66-114">Du kan oprette en faktura for en sag eller for en eller flere sagsopgaver for en debitor, når det arbejde, der skal faktureres, er udført, eller når den fakturadato, som er angivet i et fakturaskema, nås.</span><span class="sxs-lookup"><span data-stu-id="d7f66-114">You can create an invoice for a job or for one or more job tasks for a customer when either the work to be invoiced is complete or the date for invoicing based on an invoicing schedule has been reached.</span></span>

<span data-ttu-id="d7f66-115">Følgende procedure viser, hvordan du kan bruge en kørsel til at fakturere flere sager.</span><span class="sxs-lookup"><span data-stu-id="d7f66-115">The following procedure shows how to use a batch job to invoice multiple jobs.</span></span>  

1. <span data-ttu-id="d7f66-116">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opret salgsfaktura for sag**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d7f66-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Create Sales Invoice**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d7f66-117">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="d7f66-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="d7f66-118">Du kan angive filtre, hvis du vil begrænse de sager, som kørslen skal behandle.</span><span class="sxs-lookup"><span data-stu-id="d7f66-118">Set filters if you want to limit the jobs that the batch job will process.</span></span>
4. <span data-ttu-id="d7f66-119">Vælg **OK** for at starte oprette fakturaen.</span><span class="sxs-lookup"><span data-stu-id="d7f66-119">Choose the **OK** button to create the invoices.</span></span>  

<span data-ttu-id="d7f66-120">Du kan gennemse og bogføre oprettede fakturaer i vinduet **Salgsfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="d7f66-120">You can review and post created invoices in the **Sales Invoices** window.</span></span>

> [!NOTE]
> <span data-ttu-id="d7f66-121">Du kan også fakturere en kunde ved at markere sagen og derefter vælge handlingen **Opret salgsfaktura for sag**.</span><span class="sxs-lookup"><span data-stu-id="d7f66-121">Alternatively, invoice a customer by selecting the job, and then choosing the **Create Job Sales Invoice** action.</span></span> 

## <a name="to-create-and-post-job-sales-invoice-from-job-planning-lines"></a><span data-ttu-id="d7f66-122">Sådan opretter og bogfører du salgsfakturaer for sager fra sagsplanlægningslinjer</span><span class="sxs-lookup"><span data-stu-id="d7f66-122">To create and post job sales invoice from job planning lines</span></span>
<span data-ttu-id="d7f66-123">Du kan oprette en faktura ud fra en sagsplanlægningslinje, og på det tidspunkt angive antallet af varen, ressourcen eller finanskontoen, som du vil fakturere.</span><span class="sxs-lookup"><span data-stu-id="d7f66-123">You can create an invoice from a job planning lines, and indicate at that time the quantity of the item, resource, or general ledger account that you want to invoice.</span></span>

1. <span data-ttu-id="d7f66-124">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sager**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d7f66-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="d7f66-125">Åbn en relevant sag.</span><span class="sxs-lookup"><span data-stu-id="d7f66-125">Open a relevant job.</span></span>
3. <span data-ttu-id="d7f66-126">Vælg en sagsopgave, hvor feltet **Sagsopgavetype** indeholder **Bogføring**, og vælg derefter handlingen **Sagsplanlægningslinjer**.</span><span class="sxs-lookup"><span data-stu-id="d7f66-126">Select a job task for which the **Job Task Type** field contains **Posting**, and then choose the **Job Planning Lines** action.</span></span>  
4. <span data-ttu-id="d7f66-127">Angiv antallet af varen, ressourcen og finanskontotype, som du vil fakturere, i feltet **Antal til overførsel til faktura** i en sagsplanlægningslinje.</span><span class="sxs-lookup"><span data-stu-id="d7f66-127">On a job planning line, in the **Qty. To Transfer to Invoice** field, enter the quantity of the item, resource, general ledger account type that you want to invoice.</span></span>  
5. <span data-ttu-id="d7f66-128">Vælg handlingen **Opret salgsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="d7f66-128">Choose the **Create Sales Invoice** action.</span></span>
6. <span data-ttu-id="d7f66-129">På siden **Opret salgsfaktura** skal du angive bogføringsdatoen, og om du vil oprette en ny faktura eller føje denne faktura til en eksisterende.</span><span class="sxs-lookup"><span data-stu-id="d7f66-129">On the **Job Create Sales Invoice** page, enter the posting date and whether you want to create a new invoice or append this invoice to an existing one.</span></span>
7. <span data-ttu-id="d7f66-130">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="d7f66-130">Choose the **OK** button.</span></span>  
8. <span data-ttu-id="d7f66-131">På siden **Sagsplanlægningslinjer** skal du vælge **Salgsfakturaer/kreditnotaer**.</span><span class="sxs-lookup"><span data-stu-id="d7f66-131">On the **Job Planning Lines** page, choose the **Sales Invoices/Credit Memos** action.</span></span>

    <span data-ttu-id="d7f66-132">Siden **Salgsfaktura** åbnes og viser det antal, du har overført til fakturaen.</span><span class="sxs-lookup"><span data-stu-id="d7f66-132">The **Sales Invoice** page opens, showing the quantity that you have transferred to the invoice.</span></span>
9. <span data-ttu-id="d7f66-133">Foretag yderligere ændringer, og vælg derefter handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="d7f66-133">Make any additional changes, and then choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d7f66-134">Ovenstående fremgangsmåde er ens for at oprette, gennemse og bogføre en sagsrelateret salgskreditnota.</span><span class="sxs-lookup"><span data-stu-id="d7f66-134">The above procedure is similar for creating, reviewing, and posting a job-related sales credit memo.</span></span>

## <a name="to-calculate-and-post-job-completion-entries"></a><span data-ttu-id="d7f66-135">Sådan beregnes og bogføres sagsafslutningsposter</span><span class="sxs-lookup"><span data-stu-id="d7f66-135">To calculate and post job completion entries</span></span>
<span data-ttu-id="d7f66-136">Når du har fuldført alle aktiviteter for en sag, inklusive bogføring og fakturering af forbrug, skal du opdatere sagen for at få **status** **Afsluttet**.</span><span class="sxs-lookup"><span data-stu-id="d7f66-136">When you have completed all activities for a job, including usage posting and invoicing, you must update the job to have a **Status** of **Completed**.</span></span> <span data-ttu-id="d7f66-137">Derefter skal du tilbageføre alt igangværende arbejde, som er blevet bogført i finansregnskabet.</span><span class="sxs-lookup"><span data-stu-id="d7f66-137">Then, you must reverse any WIP that has been posted to the general ledger.</span></span>

1. <span data-ttu-id="d7f66-138">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sager**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d7f66-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d7f66-139">Vælg en åben sag, og vælg derefter handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="d7f66-139">Select an open job, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="d7f66-140">I feltet **Status** skal du vælge **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="d7f66-140">In the **Status** field, select **Completed**.</span></span>
4. <span data-ttu-id="d7f66-141">Følg hjælpetrinnene for at beregne og bogføre igangværende arbejde.</span><span class="sxs-lookup"><span data-stu-id="d7f66-141">Follow the assistance steps to calculate and post WIP.</span></span> <span data-ttu-id="d7f66-142">Du kan også følge trin 5 og 6 for at gøre det manuelt.</span><span class="sxs-lookup"><span data-stu-id="d7f66-142">Alternatively, follows steps 5 and 6 to do so manually.</span></span>  
5. <span data-ttu-id="d7f66-143">Vælg handlingen **Beregn igangværende arbejde**.</span><span class="sxs-lookup"><span data-stu-id="d7f66-143">Choose the **Calculate WIP** action.</span></span>
6. <span data-ttu-id="d7f66-144">På siden **Beregn VIA for sag** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="d7f66-144">On the **Job Calculate WIP** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="d7f66-145">Posterne for igangværende arbejde for sagen, som blev oprettet ved at udføre kørslen, vil nu være markeret i feltet **Sagen er fuldført** for at vise, at de er færdiggørelsesposter.</span><span class="sxs-lookup"><span data-stu-id="d7f66-145">The job WIP entries created by running the batch job will have the **Job Complete** check box selected to show that they are completion entries.</span></span>  
7. <span data-ttu-id="d7f66-146">Vælg handlingen **Bogfør VIA - finansafstemning**.</span><span class="sxs-lookup"><span data-stu-id="d7f66-146">Choose the **Job Post WIP to G/L** action.</span></span>
8. <span data-ttu-id="d7f66-147">På siden **Bogfør VIA - finansafstemning** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="d7f66-147">On the **Job Post WIP to G/L** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="d7f66-148">Sagens VIA-finansposter, som blev oprettet ved at udføre kørslen, vil nu være markeret i feltet **Sagen er fuldført** for at vise, at de er færdiggørelsesposter.</span><span class="sxs-lookup"><span data-stu-id="d7f66-148">The job WIP general ledger entries created by running the batch job will have the **Job Complete** check box selected to show they are completion entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="d7f66-149">Se også</span><span class="sxs-lookup"><span data-stu-id="d7f66-149">See Also</span></span>
[<span data-ttu-id="d7f66-150">Administrere projekter</span><span class="sxs-lookup"><span data-stu-id="d7f66-150">Managing Projects</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="d7f66-151">Finans</span><span class="sxs-lookup"><span data-stu-id="d7f66-151">Finance</span></span>](finance.md)  
<span data-ttu-id="d7f66-152">[Køb](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="d7f66-152">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="d7f66-153">[Salg](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="d7f66-153">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="d7f66-154">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d7f66-154">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]