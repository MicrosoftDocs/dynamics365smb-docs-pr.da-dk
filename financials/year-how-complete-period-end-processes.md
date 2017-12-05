---
title: Valgfrie aktiviteter til afslutning af perioder | Microsoft Docs
description: I dette emne beskriver de valgfrie processer og aktiviteter til afslutning af regnskabsperioder i Dynamics 365.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 06/19/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 526ae1811768f38b04f961e378454fed79a8426b
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="overview-of-tasks-to-close-accounting-periods"></a><span data-ttu-id="5c240-103">Oversigt over opgaver til afslutning af regnskabsperioder</span><span class="sxs-lookup"><span data-stu-id="5c240-103">Overview of Tasks to Close Accounting Periods</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="5c240-104"> tvinger dig ikke at lukke perioder, men der er mange periodeafslutnings- (månedsafslutning) aktiviteter, du kan udføre.</span><span class="sxs-lookup"><span data-stu-id="5c240-104"> does not force you to close periods, however, there are many period-end (month-end) activities that you can do.</span></span> <span data-ttu-id="5c240-105">Dette emne indeholder en oversigt over valgfrie processer og aktiviteter til afslutning af perioder.</span><span class="sxs-lookup"><span data-stu-id="5c240-105">This topic provides an overview of optional processes and activities for closing periods.</span></span>  

## <a name="general-ledger"></a><span data-ttu-id="5c240-106">Finansposter</span><span class="sxs-lookup"><span data-stu-id="5c240-106">General Ledger</span></span>
* <span data-ttu-id="5c240-107">Angiv bogføringsperioder, som enten er brugerspecifikke, eller som gælder på tværs af hele systemet.</span><span class="sxs-lookup"><span data-stu-id="5c240-107">Specify system-wide and user-specific posting periods.</span></span>  

    <span data-ttu-id="5c240-108">Dette angiver de datoer, du tillader bogføring mellem.</span><span class="sxs-lookup"><span data-stu-id="5c240-108">This specifies the dates between which you allow posting.</span></span> <span data-ttu-id="5c240-109">Afhængigt af dine forretningsmæssige behov kan det være en god idé at tillade bogføring i begyndelsen af perioden eller mod afslutningen af den.</span><span class="sxs-lookup"><span data-stu-id="5c240-109">Depending on your business, you may want to allow posting at the start of the period, or toward the end.</span></span> <span data-ttu-id="5c240-110">Du kan finde flere oplysninger i [Fremgangsmåde: Angive bogføringsperioder](finance-how-specify-posting-periods.md).</span><span class="sxs-lookup"><span data-stu-id="5c240-110">For more information, see [How to: Specify Posting Periods](finance-how-specify-posting-periods.md).</span></span>  
* <span data-ttu-id="5c240-111">Foretag alle nødvendige Finanspostreguleringer.</span><span class="sxs-lookup"><span data-stu-id="5c240-111">Make all necessary G/L adjustments.</span></span>  
* <span data-ttu-id="5c240-112">Opdater og bogfør gentagelseskladder.</span><span class="sxs-lookup"><span data-stu-id="5c240-112">Update and post Recurring Journals.</span></span>  
  <!--* Process Consolidations-->
* <span data-ttu-id="5c240-113">Kør kontoskemaer på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="5c240-113">Run account schedules as follows:</span></span>  
  * <span data-ttu-id="5c240-114">Åbn vinduet **Kontoskema**, og vælg derefter handlingen **Udskriv**.</span><span class="sxs-lookup"><span data-stu-id="5c240-114">Open the **Account Schedule** window, and then choose the **Print** action.</span></span>  

## <a name="sales-and-receivables"></a><span data-ttu-id="5c240-115">Salg</span><span class="sxs-lookup"><span data-stu-id="5c240-115">Sales and Receivables</span></span>
* <span data-ttu-id="5c240-116">Bogfør alle salgsordrer, fakturaer, kreditnotaer og returvareordrer.</span><span class="sxs-lookup"><span data-stu-id="5c240-116">Post all sales orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="5c240-117">Bogfør alle indbetalingskladder.</span><span class="sxs-lookup"><span data-stu-id="5c240-117">Post all cash receipt journals.</span></span>  
* <span data-ttu-id="5c240-118">Opdater og bogfør de gentagelseskladder, som vedrører salg.</span><span class="sxs-lookup"><span data-stu-id="5c240-118">Update and post recurring journals that are related to sales and receivables.</span></span>  
* <span data-ttu-id="5c240-119">Afstem aldersfordelte tilgodehavender, med finansposterne.</span><span class="sxs-lookup"><span data-stu-id="5c240-119">Reconcile accounts receivable to the general ledger.</span></span>  
* <span data-ttu-id="5c240-120">Udfør kørslen **Slet fakturerede salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="5c240-120">Run the **Delete Invoiced Sales Orders** batch job.</span></span>  

## <a name="purchases-and-payables"></a><span data-ttu-id="5c240-121">Køb og gæld</span><span class="sxs-lookup"><span data-stu-id="5c240-121">Purchases and Payables</span></span>
* <span data-ttu-id="5c240-122">Bogfør alle købsordrer, fakturaer, kreditnotaer og returvareordrer.</span><span class="sxs-lookup"><span data-stu-id="5c240-122">Post all purchase orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="5c240-123">Bogfør alle udbetalingskladder.</span><span class="sxs-lookup"><span data-stu-id="5c240-123">Post all payment journals.</span></span>  
* <span data-ttu-id="5c240-124">Opdater og bogfør de gentagelseskladder, som vedrører Køb.</span><span class="sxs-lookup"><span data-stu-id="5c240-124">Update and post recurring journals that are related to purchases & payables.</span></span>  
* <span data-ttu-id="5c240-125">Udfør rapporten **Aldersfordelt gæld**, og afstem gæld med finansposterne.</span><span class="sxs-lookup"><span data-stu-id="5c240-125">Run the **Aged Accounts Payable** report and reconcile accounts payable to the general ledger.</span></span>  
* <span data-ttu-id="5c240-126">Udfør kørslen **Slet fakturerede købsordrer**.</span><span class="sxs-lookup"><span data-stu-id="5c240-126">Run the **Delete Invoiced Purchase Orders** batch job.</span></span>  

<span data-ttu-id="5c240-127">Anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="5c240-127">Fixed Assets</span></span>
* <span data-ttu-id="5c240-128">Bogfør alle vedligeholdelsesomkostninger via anlægskladderne eller fakturaerne</span><span class="sxs-lookup"><span data-stu-id="5c240-128">Post all maintenance costs have been posted through the fixed asset journals or invoices.</span></span>
* <span data-ttu-id="5c240-129">Bogfør reguleringer.</span><span class="sxs-lookup"><span data-stu-id="5c240-129">Post adjustments.</span></span>
* <span data-ttu-id="5c240-130">Bogfør opskrivning.</span><span class="sxs-lookup"><span data-stu-id="5c240-130">Post appreciation.</span></span>
* <span data-ttu-id="5c240-131">Bogfør nedskrivning.</span><span class="sxs-lookup"><span data-stu-id="5c240-131">Post depreciation.</span></span>
* <span data-ttu-id="5c240-132">Opdater og bogfør anlægsgentagelseskladden.</span><span class="sxs-lookup"><span data-stu-id="5c240-132">Update and post the recurring fixed asset journal.</span></span>

<span data-ttu-id="5c240-133">Koncernintern</span><span class="sxs-lookup"><span data-stu-id="5c240-133">Intercompany</span></span>
* <span data-ttu-id="5c240-134">Behandle koncerninterne transaktioner</span><span class="sxs-lookup"><span data-stu-id="5c240-134">Process Intercompany Transactions</span></span>

## <a name="calculate-and-process-sales-tax"></a><span data-ttu-id="5c240-135">Beregn og behandl moms</span><span class="sxs-lookup"><span data-stu-id="5c240-135">Calculate and Process Sales Tax</span></span>
* <span data-ttu-id="5c240-136">Udfyld momsangivelser.</span><span class="sxs-lookup"><span data-stu-id="5c240-136">Complete Tax Statements.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5c240-137">Se også</span><span class="sxs-lookup"><span data-stu-id="5c240-137">See Also</span></span>
[<span data-ttu-id="5c240-138">Afslutning af år og perioder</span><span class="sxs-lookup"><span data-stu-id="5c240-138">Closing Years and Periods</span></span>](year-close-years-periods.md)  
[<span data-ttu-id="5c240-139">Afslutningregnskab</span><span class="sxs-lookup"><span data-stu-id="5c240-139">Closing Books</span></span>](year-close-books.md)  
<span data-ttu-id="5c240-140">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5c240-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

