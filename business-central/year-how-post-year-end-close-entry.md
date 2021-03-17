---
title: Bogføre årsafslutningsposten
description: Beskriver, hvordan du åbner den kladde, du angav i kørslen Nulstil resultatopgørelse, og derefter gennemser og bogfører årsafslutningsposten.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 02/23/2021
ms.author: edupont
ms.openlocfilehash: 728a3edc1ef2200d4f28130cad6653d6b26a5b3b
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5493349"
---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="1d634-103">Bogføre årsafslutningsposten</span><span class="sxs-lookup"><span data-stu-id="1d634-103">Post the Year-End Closing Entry</span></span>

<span data-ttu-id="1d634-104">Når du har udført kørslen **Nulstil resultatopgørelse** for at oprette årsafslutningens lukkepost eller -poster, skal du åbne den kladde, du angav i kørslen, og derefter gennemse og bogføre posterne.</span><span class="sxs-lookup"><span data-stu-id="1d634-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>  

> [!TIP]
> <span data-ttu-id="1d634-105">Afhængigt af virksomhedens arbejdsprocesser kan du vælge at lukke eller undlade at lukke regnskabsperioder og regnskabsår i [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="1d634-105">Depending on your organizations work processes, you can choose to close or not close accounting periods and fiscal years in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="1d634-106">I følgende procedure antages det, at du har lukket regnskabsåret ved hjælp af indstillingen *Regnskabsperioder*, genererede en årsafslutningspost ved hjælp af kørslen **Nulstil resultatopgørelse** og er nu klar til at bogføre årsafslutningsposten sammen med modregningskontoposterne for egenkapitalen.</span><span class="sxs-lookup"><span data-stu-id="1d634-106">The following procedure assumes that you have closed the fiscal year using the *Accounting Periods* option, generated a year-end closing entry using the **Close Income Statement** batch job, and are now ready to post the year-end closing entry along with the offsetting equity account entries.</span></span> <span data-ttu-id="1d634-107">Organisationen kan vælge at arbejde forskelligt, f. eks. bogføre årsafslutningsposten som en del af lukningen af regnskabsåret.</span><span class="sxs-lookup"><span data-stu-id="1d634-107">Your organization can choose to work differently, such as post the year-end closing entry as part of closing the fiscal year.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="1d634-108">Sådan bogføre årsafslutningsposten</span><span class="sxs-lookup"><span data-stu-id="1d634-108">To post the year end closing entry</span></span>

1. <span data-ttu-id="1d634-109">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Finanskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="1d634-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="1d634-110">På siden **Kassekladde** skal du i feltet **Kladdenavn** vælge den kørsel, der indeholder lukkeposterne.</span><span class="sxs-lookup"><span data-stu-id="1d634-110">On the **General Journal** page, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="1d634-111">Gennemse posterne.</span><span class="sxs-lookup"><span data-stu-id="1d634-111">Review the entries.</span></span>
4. <span data-ttu-id="1d634-112">Vælg handlingen **Bogfør** for at bogføre kladden.</span><span class="sxs-lookup"><span data-stu-id="1d634-112">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
> <span data-ttu-id="1d634-113">Hvis der opstår en fejl, vises der en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="1d634-113">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="1d634-114">Hvis bogføringen lykkes, fjernes de bogførte poster fra kladden.</span><span class="sxs-lookup"><span data-stu-id="1d634-114">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="1d634-115">Når bogføringen er fuldført, bogføres en post til alle resultatopgørelseskonti, så saldoen går i nul, og årsresultatet overføres til balancen.</span><span class="sxs-lookup"><span data-stu-id="1d634-115">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="1d634-116">Se også</span><span class="sxs-lookup"><span data-stu-id="1d634-116">See Also</span></span>

[<span data-ttu-id="1d634-117">Afslutte regnskabsperioder</span><span class="sxs-lookup"><span data-stu-id="1d634-117">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="1d634-118">Afslutningregnskab</span><span class="sxs-lookup"><span data-stu-id="1d634-118">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="1d634-119">Nulstil resultatopgørelse</span><span class="sxs-lookup"><span data-stu-id="1d634-119">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="1d634-120">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1d634-120">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]