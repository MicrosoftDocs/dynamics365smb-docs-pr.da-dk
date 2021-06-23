---
title: Oversigt over likviditet
description: En oversigt over indgående og udgående pengestrømme, som medvirker til at forudsige penge, der skal modtages og betales.
author: jill-kotel-andersson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cash flow, money flow, expense and income, liquidity, cash receipts minus cash payments
ms.date: 06/08/2021
ms.author: a-jillk
ms.reviewer: edupont
ms.openlocfilehash: 8359d95b36d6c16b179de2fce400c44fd93ec0f1
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216338"
---
# <a name="cash-flow-overview"></a><span data-ttu-id="dc623-103">Oversigt over likviditet</span><span class="sxs-lookup"><span data-stu-id="dc623-103">Cash Flow Overview</span></span>

<span data-ttu-id="dc623-104">Forståelse af indgående og udgående pengestrømme er nøglen til at drive en succesrig forretning.</span><span class="sxs-lookup"><span data-stu-id="dc623-104">Understanding cash inflows and outflows is the key to running a successful business.</span></span> <span data-ttu-id="dc623-105">Du kan bruge likviditet til nemt for at oprette en kortfristet forecast, der forudsiger, hvordan og hvornår du kan forvente at modtage penge og skal betale penge i din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="dc623-105">You can use cash flow to easily create a short-term forecast that predicts how and when you expect money to be received and paid out by your business.</span></span> <span data-ttu-id="dc623-106">Det er vigtigt at vide, at din virksomhed har nok penge til at betale gæld og udgifter, når de forfalder.</span><span class="sxs-lookup"><span data-stu-id="dc623-106">It is important for you to know that your business will have enough cash to pay creditors and expenses when they fall due.</span></span>

## <a name="definition-of-cash-flow"></a><span data-ttu-id="dc623-107">Definition af likviditet</span><span class="sxs-lookup"><span data-stu-id="dc623-107">Definition of Cash Flow</span></span>

<span data-ttu-id="dc623-108">Betegnelsen *likviditet* bruges til at angive indbetalinger minus kontantbetalinger over en valgt periode.</span><span class="sxs-lookup"><span data-stu-id="dc623-108">The term *cash flow* is used to designate cash receipts minus cash payments over a selected period.</span></span> <span data-ttu-id="dc623-109">Det er et skøn over det beløb, du forventer, vil flyde ind og ud af din virksomhed, og det omfatter alle de forventede indtægter og udgifter.</span><span class="sxs-lookup"><span data-stu-id="dc623-109">It is an estimate of the amount of money that you expect to flow in and out of your business, and it includes all your forecasted income and expenses.</span></span>

## <a name="cash-flow-overview"></a><span data-ttu-id="dc623-110">Oversigt over likviditet</span><span class="sxs-lookup"><span data-stu-id="dc623-110">Cash Flow Overview</span></span>

<span data-ttu-id="dc623-111">Følgende illustration viser en oversigt over, hvordan du kan arbejde med likviditet.</span><span class="sxs-lookup"><span data-stu-id="dc623-111">The following illustration shows an overview of how you can work with cash flow.</span></span>

<span data-ttu-id="dc623-112">![Oversigt over likviditet](media/finance_cash_flow_overview.png "Oversigt over likviditet")</span><span class="sxs-lookup"><span data-stu-id="dc623-112">![Cash Flow overview](media/finance_cash_flow_overview.png "Cash Flow overview")</span></span>

- <span data-ttu-id="dc623-113">Du konfigurerer et likviditetsforecast.</span><span class="sxs-lookup"><span data-stu-id="dc623-113">You set up a cash flow forecast.</span></span>  

- <span data-ttu-id="dc623-114">Du kan få likviditetsforecastkilder fra følgende områder:</span><span class="sxs-lookup"><span data-stu-id="dc623-114">You get cash flow forecast sources from the following areas:</span></span>  

  - <span data-ttu-id="dc623-115">Finans – oplysninger om likvide midler og budgetterede indtægter og udgifter for din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="dc623-115">General ledger – Information about the liquid funds and the budgeted revenues and expenses of your company.</span></span>  
  - <span data-ttu-id="dc623-116">Køb – oplysninger om de aktuelle skyldige beløb og budgetterede fordringer fra åbne købsordrer.</span><span class="sxs-lookup"><span data-stu-id="dc623-116">Purchasing – Information about the current payables and any forecasted debts from open purchase orders.</span></span>  
  - <span data-ttu-id="dc623-117">Salg – oplysninger om de aktuelle tilgodehavender og budgetterede indbetalinger fra åbne salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="dc623-117">Sales – Information about the current receivables and any forecasted receipts from open sales orders.</span></span>  
  - <span data-ttu-id="dc623-118">Service – oplysninger om åbne serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="dc623-118">Service – Information about open service orders.</span></span>  
  - <span data-ttu-id="dc623-119">Anlægsaktiver – oplysninger om planlagte bortskaffelser og budgetterede køb af anlæg.</span><span class="sxs-lookup"><span data-stu-id="dc623-119">Fixed assets – Information about planned disposal and budgeted purchases of fixed assets.</span></span>  
  - <span data-ttu-id="dc623-120">Manuelle indtægter og udgifter – administrer manuelle indtægter og udgifter og medtag dem i likviditetsforecastet.</span><span class="sxs-lookup"><span data-stu-id="dc623-120">Manual revenues and expenses – Manage manual revenues and expenses and include them in the cash flow forecast.</span></span>  
- <span data-ttu-id="dc623-121">Brug en kørsel til at overføre oplysninger fra områderne finans, indkøb, salg, service og faste anlægsaktiver til pengestrømskladden. Du skal bruge kørslen til at lave en pengestrømsprognose.</span><span class="sxs-lookup"><span data-stu-id="dc623-121">You use a batch job to transfer information from the areas of general ledger, sales, purchasing, service, and fixed assets to the worksheet Then, you register worksheet lines to make a cash flow forecast.</span></span>  
- <span data-ttu-id="dc623-122">Du kan bruge forskellige vinduer, rapporter og diagrammer til at analysere og udskrive en likviditetsforecast, der vedrører tilgængelighed og oversigter på tidslinjen.</span><span class="sxs-lookup"><span data-stu-id="dc623-122">You use various windows, reports, and charts to analyze and print a cash flow forecast that relates to availability and timeline overviews.</span></span>  

## <a name="making-a-cash-flow-forecast"></a><span data-ttu-id="dc623-123">Foretage likviditetsforecast</span><span class="sxs-lookup"><span data-stu-id="dc623-123">Making a Cash Flow Forecast</span></span>

<span data-ttu-id="dc623-124">Baseret på registrerede kladdelinjer kan du med jævne mellemrum foretage en likviditetsforecast.</span><span class="sxs-lookup"><span data-stu-id="dc623-124">Based on the registered worksheet lines, you can periodically make a cash flow forecast.</span></span> <span data-ttu-id="dc623-125">Følgende layout er et ofte anvendt layout for en likviditetsforecast.</span><span class="sxs-lookup"><span data-stu-id="dc623-125">The following layout is a frequently used layout for a cash flow forecast.</span></span> <span data-ttu-id="dc623-126">Layout indeholder tre sektioner:</span><span class="sxs-lookup"><span data-stu-id="dc623-126">The layout has three sections:</span></span>

  - <span data-ttu-id="dc623-127">Indbetaling kladde</span><span class="sxs-lookup"><span data-stu-id="dc623-127">Cash receipts</span></span>  
  - <span data-ttu-id="dc623-128">Kontante udbetalinger</span><span class="sxs-lookup"><span data-stu-id="dc623-128">Cash disbursements</span></span>  
  - <span data-ttu-id="dc623-129">Nettolikviditet eller kontanter i hånden</span><span class="sxs-lookup"><span data-stu-id="dc623-129">Net cash flow or cash-in-hand</span></span>  

<span data-ttu-id="dc623-130">Indbetalinger giver oplysninger om den indtægt, som virksomheden modtager.</span><span class="sxs-lookup"><span data-stu-id="dc623-130">Cash receipts provide details of the income that the business receives.</span></span>

<span data-ttu-id="dc623-131">*indbetalinger i alt* = *tilgodehavender* + *åbne salgsordrer* + *åbne serviceordrer* + *afhændelse af faste anlægsaktiver* + *manuelle indtægter* + *budgetterede indtægter*</span><span class="sxs-lookup"><span data-stu-id="dc623-131">*total cash receipts* = *receivables* + *open sales orders* + *open service orders* + *fixed assets disposals* + *manual revenues* + *budgeted revenues*</span></span>

> [!NOTE]
> <span data-ttu-id="dc623-132">Manuelle indtægter kan være lejeindtægt, renter fra finansielle aktiver eller ny privat kapital.</span><span class="sxs-lookup"><span data-stu-id="dc623-132">Manual revenues can be rental income, interest from financial assets, or new private capital.</span></span> <span data-ttu-id="dc623-133">Du kan planlægge manuelle indtægter for et tidsrum og bruge dem til beregning af likviditetsforecast.</span><span class="sxs-lookup"><span data-stu-id="dc623-133">You can plan manual revenues for a period of time and use them in the calculation of cash flow forecast.</span></span>

<span data-ttu-id="dc623-134">Kontante udbetalinger giver oplysninger om betalinger foretaget af virksomheden.</span><span class="sxs-lookup"><span data-stu-id="dc623-134">Cash disbursements provide details of the payments made by the business.</span></span>

<span data-ttu-id="dc623-135">*kontante udbetalinger i alt* = *skyldige beløb* + *åbne købsordrer* + *investering i anlæg* + *manuelle udgifter* + *budgetterede udgifter*</span><span class="sxs-lookup"><span data-stu-id="dc623-135">*total cash disbursements* = *payables* + *open purchase orders* + *fixed asset investment* + *manual expenses* + *budgeted expenses*</span></span>

> [!NOTE]
> <span data-ttu-id="dc623-136">Manuelle udgifter kan være lønninger, renter på kredit eller privat forbrug.</span><span class="sxs-lookup"><span data-stu-id="dc623-136">Manual expenses can be salaries, interest on credit, or private consumptions.</span></span> <span data-ttu-id="dc623-137">Du kan planlægge manuelle udgifter for et tidsrum og bruge dem til beregning af likviditetsforecast.</span><span class="sxs-lookup"><span data-stu-id="dc623-137">You can plan manual expenses for a period of time and use them in the calculation of cash flow forecast.</span></span>

<span data-ttu-id="dc623-138">Nettolikviditet eller kontanter i hånden beregnes som samlede indtægter minus samlede udbetalinger i slutningen af hver periode.</span><span class="sxs-lookup"><span data-stu-id="dc623-138">Net cash flow or cash-in-hand is calculated as total receipts minus total disbursements at the end of each period.</span></span>

<span data-ttu-id="dc623-139">*nettolikviditet* = *samlede indbetalinger* – *samlede kontante udbetalinger* + *likvide midler*</span><span class="sxs-lookup"><span data-stu-id="dc623-139">*net cash flow* = *total cash receipts* – *total cash disbursements* + *liquid funds*</span></span>

<span data-ttu-id="dc623-140">Budgettet kan derefter bruges som et internt beslutningsværktøj til ledelsen, som hjælper dig med at planlægge og foretage vigtige strategiske beslutninger om driften af virksomheden.</span><span class="sxs-lookup"><span data-stu-id="dc623-140">The forecast can then be used as an internal management decision-making tool that helps you plan ahead and make important strategic decisions about the operation of the business.</span></span>

## <a name="see-also"></a><span data-ttu-id="dc623-141">Se også</span><span class="sxs-lookup"><span data-stu-id="dc623-141">See Also</span></span>
[<span data-ttu-id="dc623-142">Opsætning af pengestrømsanalyse</span><span class="sxs-lookup"><span data-stu-id="dc623-142">Setting Up Cash Flow Analysis</span></span>](finance-setup-cash-flow-analyses.md)  
[<span data-ttu-id="dc623-143">Analysér pengestrøm</span><span class="sxs-lookup"><span data-stu-id="dc623-143">Analyze Cash Flow</span></span>](finance-analyze-cash-flow.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
