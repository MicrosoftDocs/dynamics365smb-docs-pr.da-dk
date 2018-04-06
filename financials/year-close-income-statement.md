---
title: "Nulstille resultatopgørelseskonti | Microsoft Docs"
description: "Ved årsregnskabets afslutning skal du udføre kørslen Nulstil resultatopgørelse for at afslutte de regnskabsperioder, der udgør regnskabsåret."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 237c03e2ba6408bde65aba5f652468a3b700fa0a
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="close-income-statement-accounts"></a><span data-ttu-id="0664c-103">Nulstille resultatopgørelseskonti</span><span class="sxs-lookup"><span data-stu-id="0664c-103">Close Income Statement Accounts</span></span>
<span data-ttu-id="0664c-104">Når regnskabsåret er slut, skal du afslutte de perioder, det indeholder.</span><span class="sxs-lookup"><span data-stu-id="0664c-104">When a fiscal year is over, you must close the periods that comprise it.</span></span> <span data-ttu-id="0664c-105">Brug kørslen **Nulstil resultatopgørelse** for at gøre dette.</span><span class="sxs-lookup"><span data-stu-id="0664c-105">To do this, you run the **Close Income Statement** batch job.</span></span> <span data-ttu-id="0664c-106">Denne kørsel overfører årets resultat til en konto i balancen og nulstiller resultatopgørelseskonti.</span><span class="sxs-lookup"><span data-stu-id="0664c-106">This job transfers the year's result to an account in the balance sheet and closes the income statement accounts.</span></span> <span data-ttu-id="0664c-107">Det gør du ved at oprette linjer i en kladde, som du derefter kan bogføre.</span><span class="sxs-lookup"><span data-stu-id="0664c-107">You do this by creating lines in a journal, which you then can post.</span></span>

## <a name="to-run-the-close-income-statement-batch-job"></a><span data-ttu-id="0664c-108">Sådan udføres kørslen Nulstil resultatopgørelse</span><span class="sxs-lookup"><span data-stu-id="0664c-108">To run the Close Income Statement batch job</span></span>
1. <span data-ttu-id="0664c-109">Afslut regnskabsåret.</span><span class="sxs-lookup"><span data-stu-id="0664c-109">Close the fiscal year.</span></span> <span data-ttu-id="0664c-110">Regnskabsåret skal være afsluttet, før kørslen kan sættes i gang.</span><span class="sxs-lookup"><span data-stu-id="0664c-110">The fiscal year must closed before the batch job can be run.</span></span> <span data-ttu-id="0664c-111">Du kan finde flere oplysninger i [Afslutte regnskabsperioder](year-close-account-periods.md).</span><span class="sxs-lookup"><span data-stu-id="0664c-111">For more information, see [Close Accounting Periods](year-close-account-periods.md).</span></span>
2. <span data-ttu-id="0664c-112">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Nulstil resultatopgørelse**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="0664c-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Close Income Statement**, and then choose the related link.</span></span>
3. <span data-ttu-id="0664c-113">Vælg **OK** for at eksekvere kørslen.</span><span class="sxs-lookup"><span data-stu-id="0664c-113">Choose the **OK** button to run the batch job.</span></span>

## <a name="about-the-close-income-statement-batch-job"></a><span data-ttu-id="0664c-114">Om kørslen Nulstil resultatopgørelse</span><span class="sxs-lookup"><span data-stu-id="0664c-114">About the Close Income Statement Batch Job</span></span>
<span data-ttu-id="0664c-115">Ved kørslen behandles alle finansposter af typen Resultatopgørelse, og der oprettes poster, som tilbagefører balancerne.</span><span class="sxs-lookup"><span data-stu-id="0664c-115">The batch job processes all general accounts of the income statement type and creates entries that cancel out their respective balances.</span></span> <span data-ttu-id="0664c-116">Hver post er totalen af alle finansposter i kontoen i regnskabsåret.</span><span class="sxs-lookup"><span data-stu-id="0664c-116">That is, each entry is the sum of all the general ledger entries on the account in the fiscal year.</span></span> <span data-ttu-id="0664c-117">Disse nye poster placeres i en kladde, hvor du skal angive en modkonto og en resultatkonto i balancen, inden du bogfører.</span><span class="sxs-lookup"><span data-stu-id="0664c-117">These new entries are placed in a journal in which you must specify a balancing account and retained earnings account in the balance sheet before you post.</span></span> <span data-ttu-id="0664c-118">Når du bogfører kladden, bliver der bogført en post på hver resultatopgørelseskonto, der får saldoen til at gå i nul, og samtidig overfører årets resultat til balancen.</span><span class="sxs-lookup"><span data-stu-id="0664c-118">When you post the journal, an entry is posted to each income statement account so that its balance becomes zero and at the same time the year's result is transferred to the balance sheet.</span></span>

<span data-ttu-id="0664c-119">Du skal selv bogføre kladden.</span><span class="sxs-lookup"><span data-stu-id="0664c-119">You must post the journal yourself.</span></span> <span data-ttu-id="0664c-120">Posterne bogføres ikke automatisk ved kørslen, undtagen når der bruges en ekstra rapporteringsvaluta.</span><span class="sxs-lookup"><span data-stu-id="0664c-120">The batch job does not post the entries automatically, except when an additional reporting currency is being used.</span></span> <span data-ttu-id="0664c-121">Når der bruges ekstra rapporteringsvaluta, bogfører kørslen posterne direkte til finansposterne.</span><span class="sxs-lookup"><span data-stu-id="0664c-121">When an additional reporting currency is being used, the batch job posts entries directly to the general ledger.</span></span>

<span data-ttu-id="0664c-122">Datoen på de linjer, som kørslen indsætter i kladden, vil altid være en ultimodato for regnskabsåret.</span><span class="sxs-lookup"><span data-stu-id="0664c-122">The date on the lines that the batch job inserts in the journal is always a closing date for the fiscal year.</span></span> <span data-ttu-id="0664c-123">Ultimodatoen er en fiktiv dato mellem den sidste dag i det gamle regnskabsår og den første i det nye.</span><span class="sxs-lookup"><span data-stu-id="0664c-123">The closing date is a fictitious date between the last day of the old fiscal year and the first day of the new year.</span></span> <span data-ttu-id="0664c-124">Fordelen ved at bogføre på ultimodatoen er, at du stadig har de korrekte saldi for de almindelig dage i regnskabsåret.</span><span class="sxs-lookup"><span data-stu-id="0664c-124">The advantage of posting on a closing date is that you maintain the correct balances for the ordinary dates of the fiscal year.</span></span>

<span data-ttu-id="0664c-125">Kørslen **Nulstil resultatopgørelse** kan bruges flere gange.</span><span class="sxs-lookup"><span data-stu-id="0664c-125">The **Close Income Statement** batch job can be used several times.</span></span> <span data-ttu-id="0664c-126">Du kan bogføre i et tidligere regnskabsår, også efter resultatopgørelseskontiene er nulstillet, hvis du udfører kørslen igen.</span><span class="sxs-lookup"><span data-stu-id="0664c-126">You can post in a previous fiscal year, even after the income statement accounts have been closed, if you run the batch job again.</span></span>

## <a name="see-also"></a><span data-ttu-id="0664c-127">Se også</span><span class="sxs-lookup"><span data-stu-id="0664c-127">See Also</span></span>
[<span data-ttu-id="0664c-128">Afslutningregnskab</span><span class="sxs-lookup"><span data-stu-id="0664c-128">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="0664c-129">Bogføre årsafslutningsposten</span><span class="sxs-lookup"><span data-stu-id="0664c-129">Post the Year-End Closing Entry</span></span>](year-how-post-year-end-close-entry.md)  
[<span data-ttu-id="0664c-130">Åbne et nyt regnskabsår</span><span class="sxs-lookup"><span data-stu-id="0664c-130">Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md)  
<span data-ttu-id="0664c-131">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0664c-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

