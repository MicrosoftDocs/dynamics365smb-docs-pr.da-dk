---
title: Valgfrie aktiviteter til afslutning af perioder | Microsoft Docs
description: I dette emne beskriver de valgfrie processer og aktiviteter til afslutning af regnskabsperioder i Financials.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 678cebc065594ed0ed6fea897676f109ff2c1dce
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="overview-of-tasks-to-close-accounting-periods"></a><span data-ttu-id="0b276-103">Oversigt over opgaver til afslutning af regnskabsperioder</span><span class="sxs-lookup"><span data-stu-id="0b276-103">Overview of Tasks to Close Accounting Periods</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="0b276-104"> tvinger dig ikke at lukke perioder, men der er mange periodeafslutnings- (månedsafslutning) aktiviteter, du kan udføre.</span><span class="sxs-lookup"><span data-stu-id="0b276-104"> does not force you to close periods, however, there are many period-end (month-end) activities that you can do.</span></span> <span data-ttu-id="0b276-105">Dette emne indeholder en oversigt over valgfrie processer og aktiviteter til afslutning af perioder.</span><span class="sxs-lookup"><span data-stu-id="0b276-105">This topic provides an overview of optional processes and activities for closing periods.</span></span>  

## <a name="general-ledger"></a><span data-ttu-id="0b276-106">Finansposter</span><span class="sxs-lookup"><span data-stu-id="0b276-106">General Ledger</span></span>
* <span data-ttu-id="0b276-107">Angiv bogføringsperioder, som enten er brugerspecifikke, eller som gælder på tværs af hele systemet.</span><span class="sxs-lookup"><span data-stu-id="0b276-107">Specify system-wide and user-specific posting periods.</span></span>  

    <span data-ttu-id="0b276-108">Dette angiver de datoer, du tillader bogføring mellem.</span><span class="sxs-lookup"><span data-stu-id="0b276-108">This specifies the dates between which you allow posting.</span></span> <span data-ttu-id="0b276-109">Afhængigt af dine forretningsmæssige behov kan det være en god idé at tillade bogføring i begyndelsen af perioden eller mod afslutningen af den.</span><span class="sxs-lookup"><span data-stu-id="0b276-109">Depending on your business, you may want to allow posting at the start of the period, or toward the end.</span></span> <span data-ttu-id="0b276-110">Du kan finde flere oplysninger i [Fremgangsmåde: Angive bogføringsperioder](finance-how-specify-posting-periods.md).</span><span class="sxs-lookup"><span data-stu-id="0b276-110">For more information, see [How to: Specify Posting Periods](finance-how-specify-posting-periods.md).</span></span>  
* <span data-ttu-id="0b276-111">Foretag alle nødvendige Finanspostreguleringer.</span><span class="sxs-lookup"><span data-stu-id="0b276-111">Make all necessary G/L adjustments.</span></span>  
* <span data-ttu-id="0b276-112">Opdater og bogfør gentagelseskladder.</span><span class="sxs-lookup"><span data-stu-id="0b276-112">Update and post Recurring Journals.</span></span>  
  <!--* Process Consolidations-->
* <span data-ttu-id="0b276-113">Kør kontoskemaer på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="0b276-113">Run account schedules as follows:</span></span>  
  * <span data-ttu-id="0b276-114">Åbn vinduet **Kontoskema**, og vælg derefter handlingen **Udskriv**.</span><span class="sxs-lookup"><span data-stu-id="0b276-114">Open the **Account Schedule** window, and then choose the **Print** action.</span></span>  

## <a name="sales-and-receivables"></a><span data-ttu-id="0b276-115">Salg</span><span class="sxs-lookup"><span data-stu-id="0b276-115">Sales and Receivables</span></span>
* <span data-ttu-id="0b276-116">Bogfør alle salgsordrer, fakturaer, kreditnotaer og returvareordrer.</span><span class="sxs-lookup"><span data-stu-id="0b276-116">Post all sales orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="0b276-117">Bogfør alle indbetalingskladder.</span><span class="sxs-lookup"><span data-stu-id="0b276-117">Post all cash receipt journals.</span></span>  
* <span data-ttu-id="0b276-118">Opdater og bogfør de gentagelseskladder, som vedrører salg.</span><span class="sxs-lookup"><span data-stu-id="0b276-118">Update and post recurring journals that are related to sales and receivables.</span></span>  
* <span data-ttu-id="0b276-119">Afstem aldersfordelte tilgodehavender, med finansposterne.</span><span class="sxs-lookup"><span data-stu-id="0b276-119">Reconcile accounts receivable to the general ledger.</span></span>  
* <span data-ttu-id="0b276-120">Udfør kørslen **Slet fakturerede salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="0b276-120">Run the **Delete Invoiced Sales Orders** batch job.</span></span>  

## <a name="purchases-and-payables"></a><span data-ttu-id="0b276-121">Køb og gæld</span><span class="sxs-lookup"><span data-stu-id="0b276-121">Purchases and Payables</span></span>
* <span data-ttu-id="0b276-122">Bogfør alle købsordrer, fakturaer, kreditnotaer og returvareordrer.</span><span class="sxs-lookup"><span data-stu-id="0b276-122">Post all purchase orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="0b276-123">Bogfør alle udbetalingskladder.</span><span class="sxs-lookup"><span data-stu-id="0b276-123">Post all payment journals.</span></span>  
* <span data-ttu-id="0b276-124">Opdater og bogfør de gentagelseskladder, som vedrører Køb.</span><span class="sxs-lookup"><span data-stu-id="0b276-124">Update and post recurring journals that are related to purchases & payables.</span></span>  
* <span data-ttu-id="0b276-125">Udfør rapporten **Aldersfordelt gæld**, og afstem gæld med finansposterne.</span><span class="sxs-lookup"><span data-stu-id="0b276-125">Run the **Aged Accounts Payable** report and reconcile accounts payable to the general ledger.</span></span>  
* <span data-ttu-id="0b276-126">Udfør kørslen **Slet fakturerede købsordrer**.</span><span class="sxs-lookup"><span data-stu-id="0b276-126">Run the **Delete Invoiced Purchase Orders** batch job.</span></span>  

<!-- ### Fixed Assets
* Post all maintenance costs have been posted through the fixed asset journals or invoices.
* Post adjustments.
* Post appreciation.
* Post depreciation.
* Update and post the recurring fixed asset journal.-->

<!--### Intercompany
* Process Intercompany Postings.-->

## <a name="calculate-and-process-sales-tax"></a><span data-ttu-id="0b276-127">Beregn og behandl moms</span><span class="sxs-lookup"><span data-stu-id="0b276-127">Calculate and Process Sales Tax</span></span>
* <span data-ttu-id="0b276-128">Udfyld momsangivelser.</span><span class="sxs-lookup"><span data-stu-id="0b276-128">Complete Tax Statements.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0b276-129">Se også</span><span class="sxs-lookup"><span data-stu-id="0b276-129">See Also</span></span>
[<span data-ttu-id="0b276-130">Afslutning af år og perioder</span><span class="sxs-lookup"><span data-stu-id="0b276-130">Closing Years and Periods</span></span>](year-close-years-periods.md)  
[<span data-ttu-id="0b276-131">Afslutningregnskab</span><span class="sxs-lookup"><span data-stu-id="0b276-131">Closing Books</span></span>](year-close-books.md)  
<span data-ttu-id="0b276-132">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0b276-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

