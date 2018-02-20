---
title: "Oprette og køre en kørsel | Microsoft Docs"
description: "Du kører kørsler for at behandle data og opdatere oplysninger, f.eks. for at foretage periodiske regnskabsaktiviteter eller udføre beregninger."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 8478a983da5020a4a7a49f6212c45a7a4c4d21a3
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="run-batch-jobs"></a><span data-ttu-id="3d4c5-103">Afvikle kørsler</span><span class="sxs-lookup"><span data-stu-id="3d4c5-103">Run Batch Jobs</span></span>
<span data-ttu-id="3d4c5-104">En kørsel er en rutine, hvor data behandles i bundter, f.eks. kørslen **Kursreguler valutabeholdninger**.</span><span class="sxs-lookup"><span data-stu-id="3d4c5-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="3d4c5-105">Der findes kørsler, som udfører periodiske regnskabsaktiviteter, som f.eks. opgørelse af resultatopgørelsen ved afslutning af regnskabsåret.</span><span class="sxs-lookup"><span data-stu-id="3d4c5-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="3d4c5-106">Mange kørsler udfører beregninger, som f.eks. beregningen af rentenotaer, kursjusteringer og beregning af salgspriser.</span><span class="sxs-lookup"><span data-stu-id="3d4c5-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="3d4c5-107">En kørsel minder om en rapport med den undtagelse, at kørslen bruger resultatet af sit arbejde til at opdatere oplysningerne direkte i stedet for at udskrive resultaterne.</span><span class="sxs-lookup"><span data-stu-id="3d4c5-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="3d4c5-108">Sådan foretages en kørsel</span><span class="sxs-lookup"><span data-stu-id="3d4c5-108">To run a batch job</span></span>
1. <span data-ttu-id="3d4c5-109">For at åbne vinduet til den ønskede kørsel skal du vælge ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive navnet på kørslen og derefter vælge det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="3d4c5-109">To open the request window for the relevant batch job, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="3d4c5-110">Hvis der er et oversigtspanel med **Indstillinger** for kørslen, skal du udfylde felterne for at angive, hvad kørslen skal gøre.</span><span class="sxs-lookup"><span data-stu-id="3d4c5-110">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="3d4c5-111">Vinduet kan indeholde mere end et oversigtspanel med filtre, som du kan bruge til at begrænse de data, der inkluderes i kørslen.</span><span class="sxs-lookup"><span data-stu-id="3d4c5-111">The window may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="3d4c5-112">Du kan angive kriterier i de foreslåede filtre eller tilføje flere filtre.</span><span class="sxs-lookup"><span data-stu-id="3d4c5-112">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="3d4c5-113">Vælg **OK** for at starte kørslen.</span><span class="sxs-lookup"><span data-stu-id="3d4c5-113">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="3d4c5-114">Se også</span><span class="sxs-lookup"><span data-stu-id="3d4c5-114">See Also</span></span>
[<span data-ttu-id="3d4c5-115">Indtaste kriterier i filtre</span><span class="sxs-lookup"><span data-stu-id="3d4c5-115">Entering Criteria in Filters</span></span>](ui-enter-criteria-filters.md)  
<span data-ttu-id="3d4c5-116">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3d4c5-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

