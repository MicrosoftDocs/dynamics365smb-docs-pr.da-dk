---
title: Købe varer eller tjenester til en sag og administrere forsyningerne | Microsoft Docs
description: Bruges til at administrere forsyning og køb af materialer og tjenester til sager.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, material, purchase
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 676658e869d0310fac71dda592c892994dac0edc
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312840"
---
# <a name="manage-job-supplies"></a><span data-ttu-id="f5ed2-103">Administrere sagsforsyninger</span><span class="sxs-lookup"><span data-stu-id="f5ed2-103">Manage Job Supplies</span></span>
<span data-ttu-id="f5ed2-104">Administration af projektforsyninger i form af varer, tjenester og udgifter er et integreret og vigtigt aspekt af udførelse af alle sager.</span><span class="sxs-lookup"><span data-stu-id="f5ed2-104">Managing project supplies of items, services, and expenses is an integral and critical aspect of the execution of all jobs.</span></span> <span data-ttu-id="f5ed2-105">Du kan benytte lagerbeholdningsantal eller oprette sagsspecifikke køb vha. købsordrer eller købsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="f5ed2-105">You can use inventory quantities or make job-specific purchases using purchase orders or purchase invoices.</span></span> <span data-ttu-id="f5ed2-106">Et servicejob på en computer kræver f.eks. en ny disk.</span><span class="sxs-lookup"><span data-stu-id="f5ed2-106">For example, a service job on a computer requires a new disk.</span></span> <span data-ttu-id="f5ed2-107">Du opretter en købsfaktura for at købe en ny disk og registrerer den sag, disken skal bruges i.</span><span class="sxs-lookup"><span data-stu-id="f5ed2-107">You create a purchase invoice to buy a new disk and record the job that it will be used on.</span></span>

<span data-ttu-id="f5ed2-108">Hvis købsprocessen ikke kræver, at den fysiske transaktion registreres separat, kan købet behandles på siden **Finanskladde for sag**.</span><span class="sxs-lookup"><span data-stu-id="f5ed2-108">If the purchase process does not require that the physical transaction be recorded separately, then a purchase may be processed on the **Job G/L Journal** page.</span></span> <span data-ttu-id="f5ed2-109">Du kan finde flere oplysninger under [Registrere forbrug for sager](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="f5ed2-109">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="to-purchase-items-or-services-for-a-job"></a><span data-ttu-id="f5ed2-110">Sådan køber du varer eller tjenesteydelser for en sag</span><span class="sxs-lookup"><span data-stu-id="f5ed2-110">To purchase items or services for a job</span></span>
<span data-ttu-id="f5ed2-111">Følgende procedure viser, hvordan du bruger en købsfaktura til at købe produkter for en sag.</span><span class="sxs-lookup"><span data-stu-id="f5ed2-111">The following procedure shows how to use a purchase invoice to purchase products for a job.</span></span> <span data-ttu-id="f5ed2-112">Samme fremgangsmåde anvendes, når du anvender en købsordre.</span><span class="sxs-lookup"><span data-stu-id="f5ed2-112">The same steps apply when using a purchase order.</span></span>  

1. <span data-ttu-id="f5ed2-113">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f5ed2-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f5ed2-114">Vælg handlingen **Ny**, og udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="f5ed2-114">Choose the **New** action and fill in the fields as necessary.</span></span> <span data-ttu-id="f5ed2-115">Du kan finde flere oplysninger under [Registrere køb](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="f5ed2-115">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
3. <span data-ttu-id="f5ed2-116">I felterne **Sagsnr.** og **Sagsopgavenr.** skal du vælge oplysningerne, for den sag, som du vil købe varer eller tjenester til.</span><span class="sxs-lookup"><span data-stu-id="f5ed2-116">In the **Job No.** and **Job Task No.** fields, select the information of the job that you want to purchase items or services for.</span></span> <span data-ttu-id="f5ed2-117">Brug funktionen **Vælg kolonner**, hvis feltet ikke vises.</span><span class="sxs-lookup"><span data-stu-id="f5ed2-117">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="f5ed2-118">Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="f5ed2-118">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

    <span data-ttu-id="f5ed2-119">Den værdi, du har valgt i feltet **Sagslinjetype**, angiver, om der oprettes en planlægningslinje, når du bogfører forbruget af varen.</span><span class="sxs-lookup"><span data-stu-id="f5ed2-119">The value that you select in the **Job Line Type** field defines whether a planning line is created when you post the usage of the item.</span></span> <span data-ttu-id="f5ed2-120">Hvis feltet indeholder **Fakturerbar**, oprettes der sagsplanlægningslinjer, som er klar til blive faktureret til kunden.</span><span class="sxs-lookup"><span data-stu-id="f5ed2-120">If the field contains **Billable**, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="f5ed2-121">Du kan finde flere oplysninger i [Fakturere sager](projects-how-invoice-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="f5ed2-121">For more information, see [Invoice Jobs](projects-how-invoice-jobs.md).</span></span>
4. <span data-ttu-id="f5ed2-122">Vælg handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="f5ed2-122">Choose the **Post** action.</span></span>

## <a name="to-view-the-value-of-purchases-for-a-job"></a><span data-ttu-id="f5ed2-123">Sådan får du vist værdien for køb for en sag</span><span class="sxs-lookup"><span data-stu-id="f5ed2-123">To view the value of purchases for a job</span></span>
1. <span data-ttu-id="f5ed2-124">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sager**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f5ed2-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="f5ed2-125">Åbn et relevant sagskort.</span><span class="sxs-lookup"><span data-stu-id="f5ed2-125">Open a relevant job card.</span></span>

    <span data-ttu-id="f5ed2-126">På oversigtspanelet **Opgaver** viser feltet **Udestående ordrer** det samlede udestående beløb i lokal valuta for lagervarer og tjenester på købsdokumenter for sagsopgavelinjen.</span><span class="sxs-lookup"><span data-stu-id="f5ed2-126">On the **Tasks** FastTab, the **Outstanding Orders** field shows the total outstanding amount, in local currency, of inventory items and services on purchase documents for the job task line.</span></span>  

    <span data-ttu-id="f5ed2-127">Feltet **Modt. beløb (ufakt.)** viser værdien af de varer, der er leveret på købsdokumenter, men endnu ikke faktureret.</span><span class="sxs-lookup"><span data-stu-id="f5ed2-127">The **Amt. Rec. Not Invoiced** field shows the value of items delivered on purchase documents, but not yet invoiced.</span></span>  
3. <span data-ttu-id="f5ed2-128">Vælg et af felterne for at åbne siden **Købslinjer**, hvor kan du gennemse oplysninger om de relaterede købsdokumentlinjer, herunder hvilke varer eller tjenesteydelser der er modtaget.</span><span class="sxs-lookup"><span data-stu-id="f5ed2-128">Choose either of the fields to open the **Purchase Lines** page where you can review information about the related purchase document lines, including which items or services have been received.</span></span>

## <a name="to-post-a-job-related-expense"></a><span data-ttu-id="f5ed2-129">Sådan bogføres en sagsrelateret udgift</span><span class="sxs-lookup"><span data-stu-id="f5ed2-129">To post a job-related expense</span></span>
<span data-ttu-id="f5ed2-130">Hvis der påløber specielle udgifter eller engangsudgifter, kan du bruge siden **Finanskladde for sag** til at bogføre dem direkte til den relevante sagskonto.</span><span class="sxs-lookup"><span data-stu-id="f5ed2-130">If you incur extraordinary or one-time job expenses, you can use the **Job G/L Journal** page to post them directly to the relevant job account.</span></span>

1. <span data-ttu-id="f5ed2-131">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sagsfinanskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f5ed2-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f5ed2-132">Opret en ny linje, og angiv oplysninger om udgiften, inklusive oplysninger i felterne **Sagsnr.** og **Sagsopgavenr**.</span><span class="sxs-lookup"><span data-stu-id="f5ed2-132">Create a new line and enter information about the expense, including information in the **Job No.** and **Job Task No** fields.</span></span>  
3. <span data-ttu-id="f5ed2-133">Når kladden er fuldført, skal du vælge handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="f5ed2-133">When the journal is complete, choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="f5ed2-134">Se også</span><span class="sxs-lookup"><span data-stu-id="f5ed2-134">See Also</span></span>
[<span data-ttu-id="f5ed2-135">Projektstyring</span><span class="sxs-lookup"><span data-stu-id="f5ed2-135">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="f5ed2-136">Finans</span><span class="sxs-lookup"><span data-stu-id="f5ed2-136">Finance</span></span>](finance.md)  
<span data-ttu-id="f5ed2-137">[Køb](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="f5ed2-137">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="f5ed2-138">[Salg](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="f5ed2-138">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="f5ed2-139">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f5ed2-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
