---
title: Afslutte et regnskabsår og regnskabsperioder | Microsoft Docs
description: Beskrives de opgaver, du skal udføre for at lukke et regnskabsår eller en regnskabsperiode, f.eks. ved at sørge for, at dokumenter og kladder er bogført, og kontrollere banksaldi.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 7f7fbfd75665b6d1cac845d1658ceab471f97525
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755613"
---
# <a name="closing-years-and-periods"></a><span data-ttu-id="8039d-103">Afslutning af år og perioder</span><span class="sxs-lookup"><span data-stu-id="8039d-103">Closing Years and Periods</span></span>

<span data-ttu-id="8039d-104">Ved afslutningen af et regnskabsår er der en række administrative opgaver, du skal udføre, som f.eks. kontrol af, at alle dokumenter og kladder er bogført, og at valutadata er opdateret, at bøger er afsluttet og meget mere.</span><span class="sxs-lookup"><span data-stu-id="8039d-104">At the end of a fiscal year, there are a number of administrative tasks that you have to perform, like making sure all documents and journals are posted, making sure currency data are up-to-date, closing the books, and more.</span></span> <span data-ttu-id="8039d-105">De faktiske opgaver afhænger af din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="8039d-105">The actual tasks will depend your company.</span></span>

<span data-ttu-id="8039d-106">Følgende tabel indeholder en oversigt over opgaver, du typisk udfører for at lukke et år og periode.</span><span class="sxs-lookup"><span data-stu-id="8039d-106">The following table provides an overview of tasks that you typically perform to close a year and period.</span></span>

| <span data-ttu-id="8039d-107">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="8039d-107">To</span></span> | <span data-ttu-id="8039d-108">Se</span><span class="sxs-lookup"><span data-stu-id="8039d-108">See</span></span> |
| --- | --- |
| <span data-ttu-id="8039d-109">Definer regnskabsåret, og opdel det i de perioder, du vil rapportere finansielle resultater for.</span><span class="sxs-lookup"><span data-stu-id="8039d-109">Define your fiscal year, and divide it into time periods for which to report financial performance.</span></span> | [<span data-ttu-id="8039d-110">Arbejde med regnskabsperioder og regnskabsår</span><span class="sxs-lookup"><span data-stu-id="8039d-110">Working with Accounting Periods and Fiscal Years</span></span>](finance-accounting-periods-and-fiscal-years.md)|
| <span data-ttu-id="8039d-111">Angive datointervaller for bogføring, som enten er brugerspecifikke, eller som gælder på tværs af hele systemet.</span><span class="sxs-lookup"><span data-stu-id="8039d-111">Specify system-wide and user-specific posting date ranges.</span></span> <span data-ttu-id="8039d-112">Afhængigt af dine forretningsmæssige behov kan det være en god idé at begrænse datointervaller for bogføring af brugere i begyndelsen af periodeafslutningsprocessen eller efter den.</span><span class="sxs-lookup"><span data-stu-id="8039d-112">Depending on your business needs, you may want to restrict user posting date ranges at the start of the period-end process or after it.</span></span> |[<span data-ttu-id="8039d-113">Angive bogføringsperioder</span><span class="sxs-lookup"><span data-stu-id="8039d-113">Specify Posting Periods</span></span>](finance-how-specify-posting-periods.md) |
| <span data-ttu-id="8039d-114">Få et overblik over aktiviteter, der almindeligvis udføres i slutningen af perioden, f.eks at alle dokumenter og kladder er bogført eller kørsel af kontoskemaer.</span><span class="sxs-lookup"><span data-stu-id="8039d-114">Get an overview of activities that are commonly performed at the end of a period, such as posting all documents and journals, or running account schedules.</span></span> |[<span data-ttu-id="8039d-115">Ultimoperioder</span><span class="sxs-lookup"><span data-stu-id="8039d-115">Closing Periods</span></span>](year-how-complete-period-end-processes.md) |
| <span data-ttu-id="8039d-116">Opdatere valutakurser og regulere kurserne for bogførte debitor-, kreditor- og bankposter.</span><span class="sxs-lookup"><span data-stu-id="8039d-116">Update currency exchange rates and adjust the exchange rates of posted customer, vendor, and bank account entries.</span></span> |[<span data-ttu-id="8039d-117">Opdatere valutakurser</span><span class="sxs-lookup"><span data-stu-id="8039d-117">Update Currency Exchange Rates</span></span>](finance-how-update-currencies.md) |
| <span data-ttu-id="8039d-118">Allokere omkostninger og indtægter mellem konti og dimensioner.</span><span class="sxs-lookup"><span data-stu-id="8039d-118">Allocate costs and income among accounts and dimensions.</span></span> |[<span data-ttu-id="8039d-119">Allokere omkostninger og indtægter</span><span class="sxs-lookup"><span data-stu-id="8039d-119">Allocating Costs and Income</span></span>](year-allocate-costs-income.md) |
| <span data-ttu-id="8039d-120">Forbered, hvordan du rapporterer momsbeløb, som du har indsamlet for salg, i skattemyndighedernes webtjeneste.</span><span class="sxs-lookup"><span data-stu-id="8039d-120">Prepare to report value-added tax amounts that you have collected for sales to the tax authorities' web service.</span></span> |[<span data-ttu-id="8039d-121">Rapportere moms til skattemyndighederne</span><span class="sxs-lookup"><span data-stu-id="8039d-121">Report VAT to Tax Authorities</span></span>](finance-how-report-vat.md)|
| <span data-ttu-id="8039d-122">Udskrive rapporter for at bekræfte finans-, debitor-, kreditor- og banksaldi, inden en periode afsluttes.</span><span class="sxs-lookup"><span data-stu-id="8039d-122">Print reports to verify general ledger, customer, vendor and bank account balances before closing a period.</span></span> |[<span data-ttu-id="8039d-123">Forberede rapporter før afslutning</span><span class="sxs-lookup"><span data-stu-id="8039d-123">Preparing Pre-Closing Reports</span></span>](year-prepare-preclose-reports.md) |
| <span data-ttu-id="8039d-124">Afslutte regnskabsperioder og -år, overføre resultatopgørelsessaldi til balancekonti og bogføre årsafslutningens lukningspost.</span><span class="sxs-lookup"><span data-stu-id="8039d-124">Close accounting periods and fiscal year, transfer income statement balances to balance sheet accounts and post the year end closing entry.</span></span> |[<span data-ttu-id="8039d-125">Afslutningregnskab</span><span class="sxs-lookup"><span data-stu-id="8039d-125">Closing Books</span></span>](year-close-books.md) |
| <span data-ttu-id="8039d-126">Udskrive rapporter, der kan være til nytte, når du skal oprette regnskabsopgørelser.</span><span class="sxs-lookup"><span data-stu-id="8039d-126">Print reports that can assist you in creating financial statements.</span></span> |[<span data-ttu-id="8039d-127">Forberedelse af ultimoopgørelser</span><span class="sxs-lookup"><span data-stu-id="8039d-127">Preparing Closing Statements</span></span>](year-prepare-close-statement.md) |

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="8039d-128">Se relateret oplæring på [Microsoft Learn](/learn/modules/close-fiscal-year-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="8039d-128">See Related Training at [Microsoft Learn](/learn/modules/close-fiscal-year-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="8039d-129">Se også</span><span class="sxs-lookup"><span data-stu-id="8039d-129">See Also</span></span>

[<span data-ttu-id="8039d-130">Arbejd med regnskabsperioder og regnskabsår</span><span class="sxs-lookup"><span data-stu-id="8039d-130">Work with Accounting Periods and Fiscal Years</span></span>](finance-accounting-periods-and-fiscal-years.md)  
<span data-ttu-id="8039d-131">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8039d-131">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
