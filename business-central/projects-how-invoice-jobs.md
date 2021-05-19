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
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 873135d2fa6053b7101a999981fb3117ee8689ab
ms.sourcegitcommit: 93c8681054b059cec38cb29b86de20be37980676
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938142"
---
# <a name="invoice-jobs"></a><span data-ttu-id="fe778-103">Fakturere sager</span><span class="sxs-lookup"><span data-stu-id="fe778-103">Invoice Jobs</span></span>
<span data-ttu-id="fe778-104">I løbet af projektet kan der akkumuleres sagsomkostninger fra ressourceforbrug, materialer og sagsrelaterede indkøb.</span><span class="sxs-lookup"><span data-stu-id="fe778-104">During the project, job costs from resource usage, materials, and job-related purchases can accumulate.</span></span> <span data-ttu-id="fe778-105">Efterhånden som status for sagen ændrer sig, bogføres disse transaktioner i sagskladden.</span><span class="sxs-lookup"><span data-stu-id="fe778-105">As the job progresses, these transactions get posted to the job journal.</span></span> <span data-ttu-id="fe778-106">Det er vigtigt, at alle omkostninger er registreret i sagskladden, før du fakturerer kunden.</span><span class="sxs-lookup"><span data-stu-id="fe778-106">It is important that all costs get recorded in the job journal before you invoice the customer.</span></span>

> [!NOTE]
> <span data-ttu-id="fe778-107">Du kan også købe eksterne ressourcer uden relation til en sag, f.eks. for at fakturere en kreditor for udført arbejde.</span><span class="sxs-lookup"><span data-stu-id="fe778-107">You can also purchase external resources unrelated to a job, for example, to invoice a vendor for work delivered.</span></span> <span data-ttu-id="fe778-108">Du kan finde flere oplysninger i [Registrere køb](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="fe778-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

<span data-ttu-id="fe778-109">Du kan fakturere hele sagen fra siden **Sagsopgavelinjer** eller kun fakturere de valgte fakturerbare linjer fra siden **Planlægningslinjer**.</span><span class="sxs-lookup"><span data-stu-id="fe778-109">You can invoice the whole job from the **Job Task Lines** page or only invoice selected billable lines from the **Planning Lines** page.</span></span> <span data-ttu-id="fe778-110">Faktureringen kan foretages, når sagen er afsluttet, eller med bestemte intervaller, efterhånden som status for sagen ændres, baseret på en faktureringsplan.</span><span class="sxs-lookup"><span data-stu-id="fe778-110">Invoicing can be done after the job is finished or at certain intervals during the job's progress based on an invoicing schedule.</span></span>

> [!NOTE]  
> <span data-ttu-id="fe778-111">Hvis du vælger **Fakturerbar** i feltet **Linjetype for sag** på købsdokumenter for sagsrelaterede indkøb, oprettes der sagsplanlægningslinjer, som er klar til blive faktureret til kunden.</span><span class="sxs-lookup"><span data-stu-id="fe778-111">If you select **Billable** in the **Job Line Type** field on the purchase documents for job-related purchases, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="fe778-112">Du kan finde flere oplysninger i [Administrere projektforsyninger](projects-how-manage-project-supplies.md).</span><span class="sxs-lookup"><span data-stu-id="fe778-112">For more information, see [Manage Project Supplies](projects-how-manage-project-supplies.md).</span></span>

## <a name="to-create-multiple-job-sales-invoices"></a><span data-ttu-id="fe778-113">Sådan opretter du flere salgsfakturaer for sager</span><span class="sxs-lookup"><span data-stu-id="fe778-113">To create multiple job sales invoices</span></span>
<span data-ttu-id="fe778-114">Du kan oprette en faktura for en sag eller for en eller flere sagsopgaver for en debitor, når det arbejde, der skal faktureres, er udført, eller når den fakturadato, som er angivet i et fakturaskema, nås.</span><span class="sxs-lookup"><span data-stu-id="fe778-114">You can create an invoice for a job or for one or more job tasks for a customer when either the work to be invoiced is complete or the date for invoicing based on an invoicing schedule has been reached.</span></span>

<span data-ttu-id="fe778-115">Følgende procedure viser, hvordan du kan bruge en kørsel til at fakturere flere sager.</span><span class="sxs-lookup"><span data-stu-id="fe778-115">The following procedure shows how to use a batch job to invoice multiple jobs.</span></span>  

1. <span data-ttu-id="fe778-116">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opret salgsfaktura for sag**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="fe778-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Create Sales Invoice**, and then choose the related link.</span></span>  
2. <span data-ttu-id="fe778-117">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="fe778-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="fe778-118">Du kan angive filtre, hvis du vil begrænse de sager, som kørslen skal behandle.</span><span class="sxs-lookup"><span data-stu-id="fe778-118">Set filters if you want to limit the jobs that the batch job will process.</span></span>
4. <span data-ttu-id="fe778-119">Vælg **OK** for at starte oprette fakturaen.</span><span class="sxs-lookup"><span data-stu-id="fe778-119">Choose the **OK** button to create the invoices.</span></span>  

<span data-ttu-id="fe778-120">Du kan gennemse og bogføre oprettede fakturaer i vinduet **Salgsfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="fe778-120">You can review and post created invoices in the **Sales Invoices** window.</span></span>

> [!NOTE]
> <span data-ttu-id="fe778-121">Du kan også fakturere en kunde ved at markere sagen og derefter vælge handlingen **Opret salgsfaktura for sag**.</span><span class="sxs-lookup"><span data-stu-id="fe778-121">Alternatively, invoice a customer by selecting the job, and then choosing the **Create Job Sales Invoice** action.</span></span> 

## <a name="to-create-and-post-job-sales-invoice-from-job-planning-lines"></a><span data-ttu-id="fe778-122">Sådan opretter og bogfører du salgsfakturaer for sager fra sagsplanlægningslinjer</span><span class="sxs-lookup"><span data-stu-id="fe778-122">To create and post job sales invoice from job planning lines</span></span>
<span data-ttu-id="fe778-123">Du kan oprette en faktura ud fra en sagsplanlægningslinje, og på det tidspunkt angive antallet af varen, ressourcen eller finanskontoen, som du vil fakturere.</span><span class="sxs-lookup"><span data-stu-id="fe778-123">You can create an invoice from a job planning lines, and indicate at that time the quantity of the item, resource, or general ledger account that you want to invoice.</span></span>

1. <span data-ttu-id="fe778-124">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sager**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="fe778-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="fe778-125">Åbn en relevant sag.</span><span class="sxs-lookup"><span data-stu-id="fe778-125">Open a relevant job.</span></span>
3. <span data-ttu-id="fe778-126">Vælg en sagsopgave, hvor feltet **Sagsopgavetype** indeholder **Bogføring**, og vælg derefter handlingen **Sagsplanlægningslinjer**.</span><span class="sxs-lookup"><span data-stu-id="fe778-126">Select a job task for which the **Job Task Type** field contains **Posting**, and then choose the **Job Planning Lines** action.</span></span>  
4. <span data-ttu-id="fe778-127">Angiv antallet af varen, ressourcen og finanskontotype, som du vil fakturere, i feltet **Antal til overførsel til faktura** i en sagsplanlægningslinje.</span><span class="sxs-lookup"><span data-stu-id="fe778-127">On a job planning line, in the **Qty. To Transfer to Invoice** field, enter the quantity of the item, resource, general ledger account type that you want to invoice.</span></span>  
5. <span data-ttu-id="fe778-128">Vælg handlingen **Opret salgsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="fe778-128">Choose the **Create Sales Invoice** action.</span></span>
6. <span data-ttu-id="fe778-129">På siden **Opret salgsfaktura** skal du angive bogføringsdatoen, og om du vil oprette en ny faktura eller føje denne faktura til en eksisterende.</span><span class="sxs-lookup"><span data-stu-id="fe778-129">On the **Job Create Sales Invoice** page, enter the posting date and whether you want to create a new invoice or append this invoice to an existing one.</span></span>
7. <span data-ttu-id="fe778-130">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe778-130">Choose the **OK** button.</span></span>  
8. <span data-ttu-id="fe778-131">På siden **Sagsplanlægningslinjer** skal du vælge **Salgsfakturaer/kreditnotaer**.</span><span class="sxs-lookup"><span data-stu-id="fe778-131">On the **Job Planning Lines** page, choose the **Sales Invoices/Credit Memos** action.</span></span>

    <span data-ttu-id="fe778-132">Siden **Salgsfaktura** åbnes og viser det antal, du har overført til fakturaen.</span><span class="sxs-lookup"><span data-stu-id="fe778-132">The **Sales Invoice** page opens, showing the quantity that you have transferred to the invoice.</span></span>
9. <span data-ttu-id="fe778-133">Foretag yderligere ændringer, og vælg derefter handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="fe778-133">Make any additional changes, and then choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="fe778-134">Ovenstående fremgangsmåde er ens for at oprette, gennemse og bogføre en sagsrelateret salgskreditnota.</span><span class="sxs-lookup"><span data-stu-id="fe778-134">The above procedure is similar for creating, reviewing, and posting a job-related sales credit memo.</span></span>


## <a name="see-also"></a><span data-ttu-id="fe778-135">Se også</span><span class="sxs-lookup"><span data-stu-id="fe778-135">See Also</span></span>
[<span data-ttu-id="fe778-136">Administrere projekter</span><span class="sxs-lookup"><span data-stu-id="fe778-136">Managing Projects</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="fe778-137">Finans</span><span class="sxs-lookup"><span data-stu-id="fe778-137">Finance</span></span>](finance.md)  
<span data-ttu-id="fe778-138">[Køb](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="fe778-138">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="fe778-139">[Salg](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="fe778-139">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="fe778-140">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fe778-140">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]
