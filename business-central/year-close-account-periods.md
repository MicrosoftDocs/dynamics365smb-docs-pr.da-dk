---
title: Afslutte regnskabsperioder for et regnskabsår | Microsoft Docs
description: Beskriver, hvordan du afslutter regnskabsperioder, der indgår i regnskabsåret.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: e49f067eb0410e3d2f6f84241ae83be041bce918
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925368"
---
# <a name="close-accounting-periods"></a><span data-ttu-id="94392-103">Afslutte regnskabsperioder</span><span class="sxs-lookup"><span data-stu-id="94392-103">Close Accounting Periods</span></span>
<span data-ttu-id="94392-104">Når regnskabsåret er slut, skal du afslutte de perioder, det indeholder.</span><span class="sxs-lookup"><span data-stu-id="94392-104">When a fiscal year is over, you must close the periods that comprise it.</span></span>

## <a name="to-close-accounting-periods"></a><span data-ttu-id="94392-105">Sådan afsluttes regnskabsperioder</span><span class="sxs-lookup"><span data-stu-id="94392-105">To close accounting periods</span></span>
1. <span data-ttu-id="94392-106">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Regnskabsperioder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="94392-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Accounting Periods**, and then choose the related link.</span></span>
2. <span data-ttu-id="94392-107">På siden **Regnskabsperioder** skal du vælge handlingen **Afslut år**.</span><span class="sxs-lookup"><span data-stu-id="94392-107">On the **Accounting Periods** page, choose the **Close Year** action.</span></span>

    <span data-ttu-id="94392-108">Hvis mere end et regnskabsår er åbent, vælges det tidligste år, der skal afsluttes, automatisk.</span><span class="sxs-lookup"><span data-stu-id="94392-108">If more than one fiscal year is open, the earliest one is automatically selected to be closed.</span></span> <span data-ttu-id="94392-109">Du får vist en meddelelse om, hvilket år der afsluttes, og om konsekvenserne af at afslutte året.</span><span class="sxs-lookup"><span data-stu-id="94392-109">A message displays identifying the year that will close and the consequences of closing the year.</span></span>
3. <span data-ttu-id="94392-110">For at lukke året skal du trykke på knappen **Ja**.</span><span class="sxs-lookup"><span data-stu-id="94392-110">To close the year, choose the **Yes** button.</span></span>

<span data-ttu-id="94392-111">Regnskabsåret er afsluttet, og felterne **Afsluttet** og **Dato låst** markeres for alle perioder i året.</span><span class="sxs-lookup"><span data-stu-id="94392-111">The fiscal year is closed, and the **Closed** and **Date Locked** fields for all the periods in the year are selected.</span></span> <span data-ttu-id="94392-112">Regnskabsåret kan ikke længere åbnes, og du kan ikke fjerne markeringen fra felterne **Afsluttet** og **Dato låst**.</span><span class="sxs-lookup"><span data-stu-id="94392-112">The fiscal year cannot be opened again and you cannot remove the check mark from the **Closed** or **Date Locked** fields.</span></span>

> [!NOTE]  
>   <span data-ttu-id="94392-113">Det er ikke muligt at afslutte et regnskabsår, før et nyt regnskabsår er oprettet.</span><span class="sxs-lookup"><span data-stu-id="94392-113">You cannot close a fiscal year before you create a new one.</span></span> <span data-ttu-id="94392-114">Bemærk, at når et regnskabsår er afsluttet, er det ikke muligt at ændre startdatoen for det efterfølgende regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="94392-114">Notice that when a fiscal year has been closed, you cannot change the starting date of the following fiscal year.</span></span>

<span data-ttu-id="94392-115">Selvom et regnskabsår er afsluttet, kan du stadig bogføre finansposter i det.</span><span class="sxs-lookup"><span data-stu-id="94392-115">Even though a fiscal year has been closed, you can still post general ledger entries to it.</span></span> <span data-ttu-id="94392-116">Hvis du gør det, bliver posterne i forbindelse med bogføringen markeret som bogførte i et afsluttet regnskabsår, og afkrydsningsfeltet **Efterpost** markeres.</span><span class="sxs-lookup"><span data-stu-id="94392-116">When you do this, the entries will be marked as posted to a closed fiscal year and the **Prior-Year Entry** field will be selected.</span></span>

<span data-ttu-id="94392-117">Når et regnskabsår er afsluttet, skal du lukke resultatopgørelseskontiene og overføre årets resultat til resultatkontoen i balancen.</span><span class="sxs-lookup"><span data-stu-id="94392-117">After a fiscal year is closed, you must close the income statement accounts and transfer the year's results to an account in the balance sheet.</span></span> <span data-ttu-id="94392-118">Du kan gentage dette, hver gang du bogfører i det afsluttede regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="94392-118">You can repeat this every time that you post to the closed fiscal year.</span></span>

## <a name="see-also"></a><span data-ttu-id="94392-119">Se også</span><span class="sxs-lookup"><span data-stu-id="94392-119">See Also</span></span>

[<span data-ttu-id="94392-120">Afslutningregnskab</span><span class="sxs-lookup"><span data-stu-id="94392-120">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="94392-121">Bogføre årsafslutningsposten</span><span class="sxs-lookup"><span data-stu-id="94392-121">Post the Year-End Closing Entry</span></span>](year-how-post-year-end-close-entry.md)  
[<span data-ttu-id="94392-122">Arbejd med regnskabsperioder og regnskabsår</span><span class="sxs-lookup"><span data-stu-id="94392-122">Work with Accounting Periods and Fiscal Years</span></span>](finance-accounting-periods-and-fiscal-years.md)  
<span data-ttu-id="94392-123">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="94392-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
