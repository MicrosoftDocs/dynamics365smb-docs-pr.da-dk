---
title: Oprette og køre en kørsel | Microsoft Docs
description: Du kører kørsler for at behandle data og opdatere oplysninger, f.eks. for at foretage periodiske regnskabsaktiviteter eller udføre beregninger.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 10/01/2018
ms.author: solsen
ms.openlocfilehash: 260cd7761b130bbe3748de3cc109a9f4f56c1384
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/19/2019
ms.locfileid: "853254"
---
# <a name="run-batch-jobs"></a><span data-ttu-id="7792c-103">Afvikle kørsler</span><span class="sxs-lookup"><span data-stu-id="7792c-103">Run Batch Jobs</span></span>
<span data-ttu-id="7792c-104">En kørsel er en rutine, hvor data behandles i bundter, f.eks. kørslen **Kursreguler valutabeholdninger**.</span><span class="sxs-lookup"><span data-stu-id="7792c-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="7792c-105">Der findes kørsler, som udfører periodiske regnskabsaktiviteter, som f.eks. opgørelse af resultatopgørelsen ved afslutning af regnskabsåret.</span><span class="sxs-lookup"><span data-stu-id="7792c-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="7792c-106">Mange kørsler udfører beregninger, som f.eks. beregningen af rentenotaer, kursjusteringer og beregning af salgspriser.</span><span class="sxs-lookup"><span data-stu-id="7792c-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="7792c-107">En kørsel minder om en rapport med den undtagelse, at kørslen bruger resultatet af sit arbejde til at opdatere oplysningerne direkte i stedet for at udskrive resultaterne.</span><span class="sxs-lookup"><span data-stu-id="7792c-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="7792c-108">Sådan foretages en kørsel</span><span class="sxs-lookup"><span data-stu-id="7792c-108">To run a batch job</span></span>
1. <span data-ttu-id="7792c-109">Åbn anmodningssiden for den ønskede kørsel ved at vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv navnet på kørslen, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="7792c-109">To open the request page for the relevant batch job, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="7792c-110">Hvis der er et oversigtspanel med **Indstillinger** for kørslen, skal du udfylde felterne for at angive, hvad kørslen skal gøre.</span><span class="sxs-lookup"><span data-stu-id="7792c-110">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="7792c-111">Siden kan indeholde mere end et oversigtspanel med filtre, som du kan bruge til at begrænse de data, der inkluderes i kørslen.</span><span class="sxs-lookup"><span data-stu-id="7792c-111">The page may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="7792c-112">Du kan angive kriterier i de foreslåede filtre eller tilføje flere filtre.</span><span class="sxs-lookup"><span data-stu-id="7792c-112">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="7792c-113">Vælg **OK** for at starte kørslen.</span><span class="sxs-lookup"><span data-stu-id="7792c-113">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="7792c-114">Se også</span><span class="sxs-lookup"><span data-stu-id="7792c-114">See Also</span></span>
[<span data-ttu-id="7792c-115">Sortering af, søgning i og filtrering af lister</span><span class="sxs-lookup"><span data-stu-id="7792c-115">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
<span data-ttu-id="7792c-116">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7792c-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
