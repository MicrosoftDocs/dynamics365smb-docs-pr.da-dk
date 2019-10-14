---
title: Konfigurere og administrere et budget for en sag | Microsoft Docs
description: Beskriver, hvordan du planlægger ressourcer og estimerer og styrer omkostningerne for et projekt ved at oprette et budget for hver sag.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 639955ef4ac9e782207d4cfee7a89f38d5c99501
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312864"
---
# <a name="manage-job-budgets"></a><span data-ttu-id="16755-103">Administrere sagsbudgetter</span><span class="sxs-lookup"><span data-stu-id="16755-103">Manage Job Budgets</span></span>
<span data-ttu-id="16755-104">Du kan oprette et budget for hver sag.</span><span class="sxs-lookup"><span data-stu-id="16755-104">You can set up a budget for each job.</span></span> <span data-ttu-id="16755-105">Budgettet bruges til at planlægge de ressourcer, som du kan allokere til en sag.</span><span class="sxs-lookup"><span data-stu-id="16755-105">The budget is used to plan the resources that you allocate to a job.</span></span> <span data-ttu-id="16755-106">Budgettet kan enten være generelt med få poster, eller det kan indeholde flere poster, der er inddelt i aktivitetsniveauer.</span><span class="sxs-lookup"><span data-stu-id="16755-106">The budget can be either general with few entries or it can contain more entries that are divided into activity levels.</span></span> <span data-ttu-id="16755-107">Du kan derefter sammenligne de budgetterede beløb med det faktiske forbrug som registreret i sagskladden.</span><span class="sxs-lookup"><span data-stu-id="16755-107">You can then compare the budgeted amounts with the actual usage as recorded in the job journal.</span></span> <span data-ttu-id="16755-108">Ved at overvåge forskellene mellem det faktiske forbrug og det budgetterede forbrug kan du kontrollere et igangværende projekt og forbedre kvaliteten af fremtidige sager ved at reducere risikoen for at undervurdere omkostningerne.</span><span class="sxs-lookup"><span data-stu-id="16755-108">By monitoring differences between actual usage and budgeted usage, you can control an ongoing project and improve the quality of future jobs by reducing the risk of underestimating costs.</span></span>

<span data-ttu-id="16755-109">Følgende fremgangsmåde beskriver, hvordan du vurderer budgetterede omkostninger under planlægningen.</span><span class="sxs-lookup"><span data-stu-id="16755-109">The following procedure describes how to estimate budgeted costs during planning.</span></span> <span data-ttu-id="16755-110">Du kan finde oplysninger om registrering af budgetterede og faktiske sagspriser og -omkostninger i [Registrere forbrug for sager](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="16755-110">For information about recording budgeted versus actual job prices and costs, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>  

## <a name="JobBudgetCosts"></a> <span data-ttu-id="16755-111">Sådan vurderes de budgetterede omkostninger for en sag</span><span class="sxs-lookup"><span data-stu-id="16755-111">To estimate the budgeted costs for a job</span></span>
<span data-ttu-id="16755-112">Når en debitor vil have oplyst prisen for en sag, som faktureres på basis af forbrug, skal du bestemme det budgetterede kostbeløb for sagen.</span><span class="sxs-lookup"><span data-stu-id="16755-112">When a customer wants to know the price of a job that will be invoiced based on usage, you must have to determine the budgeted costs for the job.</span></span> <span data-ttu-id="16755-113">Det gør du på siden **Sagsopgavelinjer**.</span><span class="sxs-lookup"><span data-stu-id="16755-113">You use the **Job Task Lines** page to do this.</span></span>

1. <span data-ttu-id="16755-114">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sager**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="16755-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="16755-115">Åbn en relevant sag.</span><span class="sxs-lookup"><span data-stu-id="16755-115">Open a relevant job.</span></span>
3. <span data-ttu-id="16755-116">Vælg en opgavelinje af typen Bogføring, og vælg derefter handlingen **Sagsplanlægningslinjer**.</span><span class="sxs-lookup"><span data-stu-id="16755-116">Select a task line of type Posting, and then choose the **Job Planning Lines** action.</span></span>
4. <span data-ttu-id="16755-117">Udfyld felterne på en ny linje efter behov.</span><span class="sxs-lookup"><span data-stu-id="16755-117">On a new line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

<span data-ttu-id="16755-118">For feltet **Linjetype** skal du se følgende oplysninger.</span><span class="sxs-lookup"><span data-stu-id="16755-118">For the **Line Type** field, refer to the following information.</span></span>  

| <span data-ttu-id="16755-119">Linjetype</span><span class="sxs-lookup"><span data-stu-id="16755-119">Line Type</span></span> | <span data-ttu-id="16755-120">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="16755-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="16755-121">**Både budget og fakturerbar**</span><span class="sxs-lookup"><span data-stu-id="16755-121">**Both Budget and Billable**</span></span> |<span data-ttu-id="16755-122">De kost- og prisbeløb, der er angivet på planlægningslinjen, er de budgetterede kostbeløb for netop denne planlægningslinje.</span><span class="sxs-lookup"><span data-stu-id="16755-122">The cost and price amounts entered on the planning line are the budgeted costs for the particular planning line.</span></span> <span data-ttu-id="16755-123">Prisbeløbet vil blive faktureret.</span><span class="sxs-lookup"><span data-stu-id="16755-123">The price amount will be invoiced.</span></span> |
| <span data-ttu-id="16755-124">**Budget**</span><span class="sxs-lookup"><span data-stu-id="16755-124">**Budget**</span></span> |<span data-ttu-id="16755-125">Kunden faktureres ikke for forbruget.</span><span class="sxs-lookup"><span data-stu-id="16755-125">The customer is not charged for usage.</span></span> <span data-ttu-id="16755-126">Forbrug overføres ikke til en faktura, men vil stadig blive brugt i VIA-beregningen.</span><span class="sxs-lookup"><span data-stu-id="16755-126">Usage is not transferred to an invoice, but will still be used in the calculation of WIP.</span></span> |
| <span data-ttu-id="16755-127">**Fakturerbar**</span><span class="sxs-lookup"><span data-stu-id="16755-127">**Billable**</span></span> |<span data-ttu-id="16755-128">Kunden faktureres for forbruget.</span><span class="sxs-lookup"><span data-stu-id="16755-128">The customer is charged for usage.</span></span> <span data-ttu-id="16755-129">Forbrug overføres til fakturaen, baseret på det antal, der er angivet i feltet Antal til overførsel til faktura.</span><span class="sxs-lookup"><span data-stu-id="16755-129">Usage is transferred to the invoice, based on the quantity specified in the Qty. to Transfer to Invoice field.</span></span> |

> [!NOTE]  
> <span data-ttu-id="16755-130">Feltet **Planlagt leveringsdato** for planlægningslinjen er den dato, hvor forbrug, der vedrører planlægningslinjen, forventes at fuldføres.</span><span class="sxs-lookup"><span data-stu-id="16755-130">The **Planned Delivery Date** field for the planning line contains the date when usage related to the planning line is expected to be completed.</span></span> <span data-ttu-id="16755-131">Det er også den dato, hvor planlægningslinjen kan overføres til en salgsfaktura og bogføres.</span><span class="sxs-lookup"><span data-stu-id="16755-131">It is also the date when the planning line may be transferred to a sales invoice and posted.</span></span> <br /><br /> <span data-ttu-id="16755-132">I den underliggende sagsopgave på siden **Jobkort** indeholder felterne **Startdato** og **Slutdato** værdien af feltet **Planlagt leveringsdato** på de tidligste og seneste sagsplanlægningslinjer på den tilhørende **Sagsplanlægningslinjer**-side.</span><span class="sxs-lookup"><span data-stu-id="16755-132">On the underlying job task on the **Job Card** page, the **Start Date** and **End Date** fields respectively contain the value of the **Planned Delivery Date** field on the earliest and latest job planning lines in the related **Job Planning Lines** page.</span></span>

> [!NOTE]  
>   <span data-ttu-id="16755-133">Når du udfylder feltet **Antal**, beregnes og udfyldes alle oplysninger om salgsbeløb og kostbeløb for planlægningslinjen.</span><span class="sxs-lookup"><span data-stu-id="16755-133">When you fill in the **Quantity** field, all total price and total cost information will be calculated and filled in for that planning line.</span></span> <span data-ttu-id="16755-134">Du kan redigere dem når som helst.</span><span class="sxs-lookup"><span data-stu-id="16755-134">You can edit them at any time.</span></span>

<span data-ttu-id="16755-135">På siden **Jobkort** , kan du nu se en oversigt over de samlede budgetterede omkostninger, budgetteret pris, fakturerbare omkostninger og fakturerbar pris for hver opgave.</span><span class="sxs-lookup"><span data-stu-id="16755-135">On the **Job Card** page, you can now see a summary of the total budgeted costs, budgeted price, billable cost and billable price for each task.</span></span>

<span data-ttu-id="16755-136">Du kan finde oplysninger om registrering af budgetterede og faktiske sagspriser og -omkostninger i [Registrere forbrug for sager](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="16755-136">For information about recording budgeted versus actual job prices and costs, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="16755-137">Se også</span><span class="sxs-lookup"><span data-stu-id="16755-137">See Also</span></span>
[<span data-ttu-id="16755-138">Projektstyring</span><span class="sxs-lookup"><span data-stu-id="16755-138">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="16755-139">Finans</span><span class="sxs-lookup"><span data-stu-id="16755-139">Finance</span></span>](finance.md)  
<span data-ttu-id="16755-140">[Køb](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="16755-140">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="16755-141">[Salg](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="16755-141">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="16755-142">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="16755-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
