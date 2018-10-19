---
title: "Gennemse og bogføre årsafslutningsposten | Microsoft Docs"
description: "Beskriver, hvordan du åbner den kladde, du angav i kørslen Nulstil resultatopgørelse, og derefter gennemser og bogfører årsafslutningsposten."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 0a5eaa15fdfbc1d578d755b246b0304030a82b1c
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="358b2-103">Bogføre årsafslutningsposten</span><span class="sxs-lookup"><span data-stu-id="358b2-103">Post the Year-End Closing Entry</span></span>
<span data-ttu-id="358b2-104">Når du har udført kørslen **Nulstil resultatopgørelse** for at oprette årsafslutningens lukkepost eller -poster, skal du åbne den kladde, du angav i kørslen, og derefter gennemse og bogføre posterne.</span><span class="sxs-lookup"><span data-stu-id="358b2-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="358b2-105">Sådan bogføre årsafslutningsposten</span><span class="sxs-lookup"><span data-stu-id="358b2-105">To post the year end closing entry</span></span>
1. <span data-ttu-id="358b2-106">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kassekladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="358b2-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="358b2-107">I vinduet **Kassekladde** skal du i feltet **Kladdenavn** vælge den kørsel, der indeholder lukkeposterne.</span><span class="sxs-lookup"><span data-stu-id="358b2-107">In the **General Journal** window, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="358b2-108">Gennemse posterne.</span><span class="sxs-lookup"><span data-stu-id="358b2-108">Review the entries.</span></span>
4. <span data-ttu-id="358b2-109">Vælg handlingen **Bogfør** for at bogføre kladden.</span><span class="sxs-lookup"><span data-stu-id="358b2-109">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="358b2-110">Hvis der opstår en fejl, vises der en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="358b2-110">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="358b2-111">Hvis bogføringen lykkes, fjernes de bogførte poster fra kladden.</span><span class="sxs-lookup"><span data-stu-id="358b2-111">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="358b2-112">Når bogføringen er fuldført, bogføres en post til alle resultatopgørelseskonti, så saldoen går i nul, og årsresultatet overføres til balancen.</span><span class="sxs-lookup"><span data-stu-id="358b2-112">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="358b2-113">Se også</span><span class="sxs-lookup"><span data-stu-id="358b2-113">See Also</span></span>
[<span data-ttu-id="358b2-114">Afslutte regnskabsperioder</span><span class="sxs-lookup"><span data-stu-id="358b2-114">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="358b2-115">Afslutningregnskab</span><span class="sxs-lookup"><span data-stu-id="358b2-115">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="358b2-116">Nulstil resultatopgørelse</span><span class="sxs-lookup"><span data-stu-id="358b2-116">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="358b2-117">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="358b2-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

