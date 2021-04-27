---
title: Om de færdige produktionsomkostninger | Microsoft Docs
description: Færdiggørelse af produktionsordren er en vigtig del af fuldførelsen af hele omkostningsberegningen for den vare, der produceres. Endelige omkostninger, inklusive afvigelser i et standardkostprismiljø, faktiske omkostninger i et FIFO-, gennemsnits- eller LIFO-kostprismiljø, beregnes vha. kørslen Juster kostpris – vareposter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b250a495504272b93565752043c23e1988ca1dab
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781057"
---
# <a name="about-finished-production-order-costs"></a><span data-ttu-id="52832-104">Om de færdige produktionsomkostninger</span><span class="sxs-lookup"><span data-stu-id="52832-104">About Finished Production Order Costs</span></span>
<span data-ttu-id="52832-105">Færdiggørelse af produktionsordren er en vigtig del af fuldførelsen af hele omkostningsberegningen for den vare, der produceres.</span><span class="sxs-lookup"><span data-stu-id="52832-105">Finishing the production order is an important task in completing the costing lifecycle of the item that is being produced.</span></span> <span data-ttu-id="52832-106">Endelige omkostninger, inklusive afvigelser i et standardkostprismiljø, faktiske omkostninger i et FIFO-, gennemsnits- eller LIFO-kostprismiljø, beregnes vha. kørslen **Juster kostpris – vareposter**, der gør det muligt at udføre en økonomisk afstemning af de omkostninger, der er forbundet med produktionen af varer.</span><span class="sxs-lookup"><span data-stu-id="52832-106">Final costs, including variances in a standard cost environment, actuals in a FIFO, Average, or LIFO cost environment, are calculated using the **Adjust Cost - Item Entries** batch job, which allows for financial reconciliation of the costs of item production.</span></span> <span data-ttu-id="52832-107">En produktionsordre kan kun indgå i en kostregulering, hvis dens status er **Færdig**.</span><span class="sxs-lookup"><span data-stu-id="52832-107">For a production order to be considered for cost adjustment, the status must be **Finished**.</span></span> <span data-ttu-id="52832-108">Derfor er det afgørende, at produktionsordrens status ændres til **Færdig**, når varerne er færdigproducerede.</span><span class="sxs-lookup"><span data-stu-id="52832-108">It is therefore critical that upon completion, the status of a production order is changed to **Finished**.</span></span>  

## <a name="example"></a><span data-ttu-id="52832-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="52832-109">Example</span></span>  
 <span data-ttu-id="52832-110">Hvis du forbruger materiale for at producere en vare i et standardkostprismiljø, vil varens kostpris plus arbejdskraft og omkostninger indgå i det igangværende arbejde.</span><span class="sxs-lookup"><span data-stu-id="52832-110">In a standard cost environment, when you consume material to produce an item, stated simply, the cost of the item plus labor and overhead go into WIP.</span></span> <span data-ttu-id="52832-111">Når varen er fremstillet, reduceres mængden af igangværende arbejde til standardkostprisen for varen.</span><span class="sxs-lookup"><span data-stu-id="52832-111">When the item is produced, WIP is reduced by the amount of the standard cost of the item.</span></span> <span data-ttu-id="52832-112">Disse omkostninger giver typisk ikke nul tilsammen.</span><span class="sxs-lookup"><span data-stu-id="52832-112">Typically, these costs do not net to zero.</span></span> <span data-ttu-id="52832-113">For at disse omkostninger skal give nul tilsammen, skal du udføre kørslen **Juster kostpris – vareposter** og være opmærksom på, at det kun er produktionsordrer med statussen **Færdig**, der kommer i betragtning ved regulering.</span><span class="sxs-lookup"><span data-stu-id="52832-113">So that these costs can net to zero, you must run the **Adjust Cost - Item Entries** batch job, noting that only production orders with the status of **Finished** will be considered for adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="52832-114">Se også</span><span class="sxs-lookup"><span data-stu-id="52832-114">See Also</span></span>  
[<span data-ttu-id="52832-115">Administrere lageromkostninger</span><span class="sxs-lookup"><span data-stu-id="52832-115">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="52832-116">Produktion</span><span class="sxs-lookup"><span data-stu-id="52832-116">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="52832-117">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="52832-117">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]