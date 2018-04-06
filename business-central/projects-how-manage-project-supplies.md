---
title: "Købe varer eller tjenester til en sag og administrere forsyningerne | Microsoft Docs"
description: "Bruges til at administrere forsyning og køb af materialer og tjenester til sager."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, material, purchase
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 958439cc8faa62baa044fcfac160797d609323ad
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="manage-job-supplies"></a><span data-ttu-id="58da5-103">Administrere sagsforsyninger</span><span class="sxs-lookup"><span data-stu-id="58da5-103">Manage Job Supplies</span></span>
<span data-ttu-id="58da5-104">Administration af projektforsyninger i form af varer, tjenester og udgifter er et integreret og vigtigt aspekt af udførelse af alle sager.</span><span class="sxs-lookup"><span data-stu-id="58da5-104">Managing project supplies of items, services, and expenses is an integral and critical aspect of the execution of all jobs.</span></span> <span data-ttu-id="58da5-105">Du kan benytte lagerbeholdningsantal eller oprette sagsspecifikke køb vha. købsordrer eller købsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="58da5-105">You can use inventory quantities or make job-specific purchases using purchase orders or purchase invoices.</span></span> <span data-ttu-id="58da5-106">Et servicejob på en computer kræver f.eks. en ny disk.</span><span class="sxs-lookup"><span data-stu-id="58da5-106">For example, a service job on a computer requires a new disk.</span></span> <span data-ttu-id="58da5-107">Du opretter en købsfaktura for at købe en ny disk og registrerer den sag, disken skal bruges i.</span><span class="sxs-lookup"><span data-stu-id="58da5-107">You create a purchase invoice to buy a new disk and record the job that it will be used on.</span></span>

<span data-ttu-id="58da5-108">Hvis købsprocessen ikke kræver, at den fysiske transaktion registreres separat, kan købet behandles i vinduet **Finanskladde for sag**.</span><span class="sxs-lookup"><span data-stu-id="58da5-108">If the purchase process does not require that the physical transaction be recorded separately, then a purchase may be processed in the **Job G/L Journal** window.</span></span> <span data-ttu-id="58da5-109">Du kan finde flere oplysninger under [Registrere forbrug for sager](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="58da5-109">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="to-purchase-items-or-services-for-a-job"></a><span data-ttu-id="58da5-110">Sådan køber du varer eller tjenesteydelser for en sag</span><span class="sxs-lookup"><span data-stu-id="58da5-110">To purchase items or services for a job</span></span>
<span data-ttu-id="58da5-111">Følgende procedure viser, hvordan du bruger en købsfaktura til at købe produkter for en sag.</span><span class="sxs-lookup"><span data-stu-id="58da5-111">The following procedure shows how to use a purchase invoice to purchase products for a job.</span></span> <span data-ttu-id="58da5-112">Samme fremgangsmåde anvendes, når du anvender en købsordre.</span><span class="sxs-lookup"><span data-stu-id="58da5-112">The same steps apply when using a purchase order.</span></span>  

1. <span data-ttu-id="58da5-113">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Købsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="58da5-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="58da5-114">Vælg handlingen **Ny**, og udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="58da5-114">Choose the **New** action and fill in the fields as necessary.</span></span> <span data-ttu-id="58da5-115">Du kan finde flere oplysninger under [Registrere køb](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="58da5-115">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
3. <span data-ttu-id="58da5-116">I felterne **Sagsnr.** og **Sagsopgavenr.** skal du vælge oplysningerne, for den sag, som du vil købe varer eller tjenester til.</span><span class="sxs-lookup"><span data-stu-id="58da5-116">In the **Job No.** and **Job Task No.** fields, select the information of the job that you want to purchase items or services for.</span></span> <span data-ttu-id="58da5-117">Brug funktionen **Vis kolonner**, hvis feltet ikke vises.</span><span class="sxs-lookup"><span data-stu-id="58da5-117">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="58da5-118">Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="58da5-118">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

    <span data-ttu-id="58da5-119">Den værdi, du har valgt i feltet **Sagslinjetype**, angiver, om der oprettes en planlægningslinje, når du bogfører forbruget af varen.</span><span class="sxs-lookup"><span data-stu-id="58da5-119">The value that you select in the **Job Line Type** field defines whether a planning line is created when you post the usage of the item.</span></span> <span data-ttu-id="58da5-120">Hvis feltet indeholder **Fakturerbar**, oprettes der sagsplanlægningslinjer, som er klar til blive faktureret til kunden.</span><span class="sxs-lookup"><span data-stu-id="58da5-120">If the field contains **Billable**, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="58da5-121">Du kan finde flere oplysninger i [Fakturere sager](projects-how-invoice-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="58da5-121">For more information, see [Invoice Jobs](projects-how-invoice-jobs.md).</span></span>
4. <span data-ttu-id="58da5-122">Vælg handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="58da5-122">Choose the **Post** action.</span></span>

## <a name="to-view-the-value-of-purchases-for-a-job"></a><span data-ttu-id="58da5-123">Sådan får du vist værdien for køb for en sag</span><span class="sxs-lookup"><span data-stu-id="58da5-123">To view the value of purchases for a job</span></span>
1. <span data-ttu-id="58da5-124">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Sager**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="58da5-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="58da5-125">Åbn et relevant sagskort.</span><span class="sxs-lookup"><span data-stu-id="58da5-125">Open a relevant job card.</span></span>

    <span data-ttu-id="58da5-126">På oversigtspanelet **Opgaver** viser feltet **Udestående ordrer** det samlede udestående beløb i lokal valuta for lagervarer og tjenester på købsdokumenter for sagsopgavelinjen.</span><span class="sxs-lookup"><span data-stu-id="58da5-126">On the **Tasks** FastTab, the **Outstanding Orders** field shows the total outstanding amount, in local currency, of inventory items and services on purchase documents for the job task line.</span></span>  

    <span data-ttu-id="58da5-127">Feltet **Modt. beløb (ufakt.)** viser værdien af de varer, der er leveret på købsdokumenter, men endnu ikke faktureret.</span><span class="sxs-lookup"><span data-stu-id="58da5-127">The **Amt. Rec. Not Invoiced** field shows the value of items delivered on purchase documents, but not yet invoiced.</span></span>  
3. <span data-ttu-id="58da5-128">Vælg et af felterne for at åbne vinduet **Købslinjer**, hvor kan du gennemse oplysninger om de relaterede købsdokumentlinjer, herunder hvilke varer eller tjenesteydelser der er modtaget.</span><span class="sxs-lookup"><span data-stu-id="58da5-128">Choose either of the fields to open the **Purchase Lines** window where you can review information about the related purchase document lines, including which items or services have been received.</span></span>

## <a name="to-post-a-job-related-expense"></a><span data-ttu-id="58da5-129">Sådan bogføres en sagsrelateret udgift</span><span class="sxs-lookup"><span data-stu-id="58da5-129">To post a job-related expense</span></span>
<span data-ttu-id="58da5-130">Hvis der påløber specielle udgifter eller engangsudgifter, kan du bruge vinduet **Finanskladde for sag** til at bogføre dem direkte til den relevante sagskonto.</span><span class="sxs-lookup"><span data-stu-id="58da5-130">If you incur extraordinary or one-time job expenses, you can use the **Job G/L Journal** window to post them directly to the relevant job account.</span></span>

1. <span data-ttu-id="58da5-131">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Sagsfinanskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="58da5-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="58da5-132">Opret en ny linje, og angiv oplysninger om udgiften, inklusive oplysninger i felterne **Sagsnr.** og **Sagsopgavenr**.</span><span class="sxs-lookup"><span data-stu-id="58da5-132">Create a new line and enter information about the expense, including information in the **Job No.** and **Job Task No** fields.</span></span>  
3. <span data-ttu-id="58da5-133">Når kladden er fuldført, skal du vælge handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="58da5-133">When the journal is complete, choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="58da5-134">Se også</span><span class="sxs-lookup"><span data-stu-id="58da5-134">See Also</span></span>
[<span data-ttu-id="58da5-135">Projektstyring</span><span class="sxs-lookup"><span data-stu-id="58da5-135">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="58da5-136">Finans</span><span class="sxs-lookup"><span data-stu-id="58da5-136">Finance</span></span>](finance.md)  
<span data-ttu-id="58da5-137">[Køb](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="58da5-137">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="58da5-138">[Salg](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="58da5-138">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="58da5-139">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="58da5-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

