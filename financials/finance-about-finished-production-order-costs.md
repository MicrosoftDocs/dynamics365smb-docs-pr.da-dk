---
title: "Om de færdige produktionsomkostninger | Microsoft Docs"
description: "Færdiggørelse af produktionsordren er en vigtig del af fuldførelsen af hele omkostningsberegningen for den vare, der produceres. Endelige omkostninger, inklusive afvigelser i et standardkostprismiljø, faktiske omkostninger i et FIFO-, gennemsnits- eller LIFO-kostprismiljø, beregnes vha. kørslen **Juster kostpris – vareposter**."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 010d4d4568f45cbe8fe13864ac6996de1e224b76
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="about-finished-production-order-costs"></a><span data-ttu-id="f9cdc-104">Om de færdige produktionsomkostninger</span><span class="sxs-lookup"><span data-stu-id="f9cdc-104">About Finished Production Order Costs</span></span>
<span data-ttu-id="f9cdc-105">Færdiggørelse af produktionsordren er en vigtig del af fuldførelsen af hele omkostningsberegningen for den vare, der produceres.</span><span class="sxs-lookup"><span data-stu-id="f9cdc-105">Finishing the production order is an important task in completing the costing lifecycle of the item that is being produced.</span></span> <span data-ttu-id="f9cdc-106">Endelige omkostninger, inklusive afvigelser i et standardkostprismiljø, faktiske omkostninger i et FIFO-, gennemsnits- eller LIFO-kostprismiljø, beregnes vha. kørslen **Juster kostpris – vareposter**, der gør det muligt at udføre en økonomisk afstemning af de omkostninger, der er forbundet med produktionen af varer.</span><span class="sxs-lookup"><span data-stu-id="f9cdc-106">Final costs, including variances in a standard cost environment, actuals in a FIFO, Average, or LIFO cost environment, are calculated using the **Adjust Cost - Item Entries** batch job, which allows for financial reconciliation of the costs of item production.</span></span> <span data-ttu-id="f9cdc-107">En produktionsordre kan kun indgå i en kostregulering, hvis dens status er **Færdig**.</span><span class="sxs-lookup"><span data-stu-id="f9cdc-107">For a production order to be considered for cost adjustment, the status must be **Finished**.</span></span> <span data-ttu-id="f9cdc-108">Derfor er det afgørende, at produktionsordrens status ændres til **Færdig**, når varerne er færdigproducerede.</span><span class="sxs-lookup"><span data-stu-id="f9cdc-108">It is therefore critical that upon completion, the status of a production order is changed to **Finished**.</span></span>  

## <a name="example"></a><span data-ttu-id="f9cdc-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="f9cdc-109">Example</span></span>  
 <span data-ttu-id="f9cdc-110">Hvis du forbruger materiale for at producere en vare i et standardkostprismiljø, vil varens kostpris plus arbejdskraft og omkostninger indgå i det igangværende arbejde.</span><span class="sxs-lookup"><span data-stu-id="f9cdc-110">In a standard cost environment, when you consume material to produce an item, stated simply, the cost of the item plus labor and overhead go into WIP.</span></span> <span data-ttu-id="f9cdc-111">Når varen er fremstillet, reduceres mængden af igangværende arbejde til standardkostprisen for varen.</span><span class="sxs-lookup"><span data-stu-id="f9cdc-111">When the item is produced, WIP is reduced by the amount of the standard cost of the item.</span></span> <span data-ttu-id="f9cdc-112">Disse omkostninger giver typisk ikke nul tilsammen.</span><span class="sxs-lookup"><span data-stu-id="f9cdc-112">Typically, these costs do not net to zero.</span></span> <span data-ttu-id="f9cdc-113">For at disse omkostninger skal give nul tilsammen, skal du udføre kørslen **Juster kostpris – vareposter** og være opmærksom på, at det kun er produktionsordrer med statussen **Færdig**, der kommer i betragtning ved regulering.</span><span class="sxs-lookup"><span data-stu-id="f9cdc-113">So that these costs can net to zero, you must run the **Adjust Cost - Item Entries** batch job, noting that only production orders with the status of **Finished** will be considered for adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f9cdc-114">Se også</span><span class="sxs-lookup"><span data-stu-id="f9cdc-114">See Also</span></span>  
[<span data-ttu-id="f9cdc-115">Administrere lageromkostninger</span><span class="sxs-lookup"><span data-stu-id="f9cdc-115">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="f9cdc-116">Produktion</span><span class="sxs-lookup"><span data-stu-id="f9cdc-116">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="f9cdc-117">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f9cdc-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
