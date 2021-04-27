---
title: Oprette og køre en kørsel | Microsoft Docs
description: Du kører kørsler for at behandle data og opdatere oplysninger, f.eks. for at foretage periodiske regnskabsaktiviteter eller udføre beregninger.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 04/01/2021
ms.author: solsen
ms.openlocfilehash: 05b65f5b001259fff25d0f59dfc6267d9ee00c7f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782249"
---
# <a name="run-batch-jobs-and-xmlports"></a><span data-ttu-id="30678-103">Udføre kørsler og XMLporte</span><span class="sxs-lookup"><span data-stu-id="30678-103">Run Batch Jobs and XMLports</span></span>
<span data-ttu-id="30678-104">En kørsel er en rutine, hvor data behandles i bundter, f.eks. kørslen **Kursreguler valutabeholdninger**.</span><span class="sxs-lookup"><span data-stu-id="30678-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="30678-105">Der findes kørsler, som udfører periodiske regnskabsaktiviteter, som f.eks. opgørelse af resultatopgørelsen ved afslutning af regnskabsåret.</span><span class="sxs-lookup"><span data-stu-id="30678-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="30678-106">Mange kørsler udfører beregninger, som f.eks. beregningen af rentenotaer, kursjusteringer og beregning af salgspriser.</span><span class="sxs-lookup"><span data-stu-id="30678-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="30678-107">En kørsel minder om en rapport med den undtagelse, at kørslen bruger resultatet af sit arbejde til at opdatere oplysningerne direkte i stedet for at udskrive resultaterne.</span><span class="sxs-lookup"><span data-stu-id="30678-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

<span data-ttu-id="30678-108">Du kan planlægge, hvornår en kørsel skal udføres.</span><span class="sxs-lookup"><span data-stu-id="30678-108">You can schedule when a batch job runs.</span></span> <span data-ttu-id="30678-109">Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="30678-109">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="30678-110">Sådan foretages en kørsel</span><span class="sxs-lookup"><span data-stu-id="30678-110">To run a batch job</span></span>
1. <span data-ttu-id="30678-111">Åbn anmodningssiden for den ønskede kørsel ved at vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv navnet på kørslen, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="30678-111">To open the request page for the relevant batch job, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="30678-112">Hvis der er et oversigtspanel med **Indstillinger** for kørslen, skal du udfylde felterne for at angive, hvad kørslen skal gøre.</span><span class="sxs-lookup"><span data-stu-id="30678-112">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="30678-113">Siden kan indeholde mere end et oversigtspanel med filtre, som du kan bruge til at begrænse de data, der inkluderes i kørslen.</span><span class="sxs-lookup"><span data-stu-id="30678-113">The page may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="30678-114">Du kan angive kriterier i de foreslåede filtre eller tilføje flere filtre.</span><span class="sxs-lookup"><span data-stu-id="30678-114">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="30678-115">Vælg **OK** for at starte kørslen.</span><span class="sxs-lookup"><span data-stu-id="30678-115">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="30678-116">Se også</span><span class="sxs-lookup"><span data-stu-id="30678-116">See Also</span></span>
[<span data-ttu-id="30678-117">Sortering af, søgning i og filtrering af lister</span><span class="sxs-lookup"><span data-stu-id="30678-117">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
[<span data-ttu-id="30678-118">Du kan bruge opgavekøer til at planlægge opgaver</span><span class="sxs-lookup"><span data-stu-id="30678-118">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
<span data-ttu-id="30678-119">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="30678-119">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]