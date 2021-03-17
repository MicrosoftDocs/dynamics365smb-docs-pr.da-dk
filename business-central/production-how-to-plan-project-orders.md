---
title: Sådan planlægges projektordrer | Microsoft Docs
description: Denne planlægningsopgave starter ud fra en salgsordre og bruger siden **Salgsordreplanlægning**. Når du har oprettet en projektproduktionsordre, kan du planlægge den yderligere på siden **Ordreplanlægning**.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1d86f30c39065488b82f4f2594098a18aa1c790a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5381261"
---
# <a name="plan-project-orders"></a><span data-ttu-id="5eb96-104">Planlægge projektordrer</span><span class="sxs-lookup"><span data-stu-id="5eb96-104">Plan Project Orders</span></span>
<span data-ttu-id="5eb96-105">Denne planlægningsopgave starter ud fra en salgsordre og bruger siden **Salgsordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="5eb96-105">This planning task starts from a sales order and uses the **Sales Order Planning** page.</span></span> <span data-ttu-id="5eb96-106">Når du har oprettet en projektproduktionsordre, kan du planlægge den yderligere på siden **Ordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="5eb96-106">Once you have created a project production order, you can plan it further by using the **Order Planning** page.</span></span>  

## <a name="to-create-a-project-production-order"></a><span data-ttu-id="5eb96-107">Sådan oprettes en projektproduktionsordre</span><span class="sxs-lookup"><span data-stu-id="5eb96-107">To create a project production order</span></span>  

1.  <span data-ttu-id="5eb96-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordre**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="5eb96-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5eb96-109">Vælg den salgsordre, der repræsenterer produktionsprojektet, og vælg derefter handlingen **Planlægning**.</span><span class="sxs-lookup"><span data-stu-id="5eb96-109">Select the sales order that represents the production project, and then choose the **Planning** action.</span></span>  
4.  <span data-ttu-id="5eb96-110">På siden **Salgsordreplanlægning** skal du vælge handlingen **Opret prod.ordre**.</span><span class="sxs-lookup"><span data-stu-id="5eb96-110">On the **Sales Order Planning** page, choose  the **Create Prod. Order** action.</span></span>  
5.  <span data-ttu-id="5eb96-111">Vælg **Projektordre** i feltet **Ordretype** på siden **Opret ordre fra salg**.</span><span class="sxs-lookup"><span data-stu-id="5eb96-111">On the **Create Order from Sales** page, in the **Order Type** field, select **Project Order**.</span></span>  
6.  <span data-ttu-id="5eb96-112">Vælg knappen **Ja**.</span><span class="sxs-lookup"><span data-stu-id="5eb96-112">Choose the **Yes** button.</span></span>  
7.  <span data-ttu-id="5eb96-113">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Produktionsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="5eb96-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Production Orders**, and then choose the related link.</span></span>
8. <span data-ttu-id="5eb96-114">Åbn den produktionsordre, du lige har oprettet.</span><span class="sxs-lookup"><span data-stu-id="5eb96-114">Open the production order just created.</span></span>  

    <span data-ttu-id="5eb96-115">Bemærk, at feltet **Kildetype** i produktionsordren indeholder **Salgshoved**, og ordren indeholder flere linjer, en for hver salgslinjevare, der skal produceres.</span><span class="sxs-lookup"><span data-stu-id="5eb96-115">Notice that the **Source Type** field of the production order contains **Sales Header** and the order has multiple lines, one for each sales line item that must be produced.</span></span>  
9. <span data-ttu-id="5eb96-116">Vælg handlingen **Planlægning**.</span><span class="sxs-lookup"><span data-stu-id="5eb96-116">Choose the **Planning** action.</span></span>
10. <span data-ttu-id="5eb96-117">Vælg handlingen **Opdater** på siden **Ordreplanlægning** for at beregne et nyt behov.</span><span class="sxs-lookup"><span data-stu-id="5eb96-117">On the **Order Planning** page, choose the **Refresh** action to calculate new demand.</span></span>  

<span data-ttu-id="5eb96-118">Produktionsordrens ordrehovedlinje vises med alle uopfyldte behovslinjer udvidet under den.</span><span class="sxs-lookup"><span data-stu-id="5eb96-118">The order header line for the project order is displayed with all unfulfilled demand lines expanded under it.</span></span> <span data-ttu-id="5eb96-119">Selvom produktionsordren indeholder linjer for flere produktionsvarer, vises det samlede behov for alle produktionsordrelinjer under én ordrehovedlinje på siden **Ordreplanlægning**, og det oprindelige kundenavn vises.</span><span class="sxs-lookup"><span data-stu-id="5eb96-119">Although the production order contains lines for several produced items, the total demand for all production order lines is listed under one order header line on the **Order Planning** page, and the original customer name is displayed.</span></span> <span data-ttu-id="5eb96-120">Du kan nu fortsætte med at planlægge efter behovet som beskrevet i emnet [Planlægge efter nyt behov ordre for ordre](production-how-to-plan-for-new-demand.md).</span><span class="sxs-lookup"><span data-stu-id="5eb96-120">You can now proceed to plan for the demand as described in [Plan for New Demand Order by Order](production-how-to-plan-for-new-demand.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="5eb96-121">Linjer i projektproduktionsordren, der har behov for **Prod.ordre** i feltet **Genbestillingssystem**, repræsenterer underliggende produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="5eb96-121">Demand lines in the project production order that have **Prod. Order** in their **Replenishment System** field represent underlying production orders.</span></span> <span data-ttu-id="5eb96-122">Når du har oprettet disse produktionsordrer, skal der beregnes en plan på siden **Ordreplanlægning** for at identificere eventuelle ekspederet komponentbehov for dem.</span><span class="sxs-lookup"><span data-stu-id="5eb96-122">After you have generated these production orders, you must again calculate a plan on the **Order Planning** page to identify any unfulfilled component demand for them.</span></span> <span data-ttu-id="5eb96-123">I så fald vises de som behovslinjer under en normal produktionsordrehovedlinje, hvilket betyder, at projektrelationen ikke længere er synlig på siden.</span><span class="sxs-lookup"><span data-stu-id="5eb96-123">In that case, they are displayed as demand lines under a normal production order header line, meaning, the project relation is no longer visible on the page.</span></span> <span data-ttu-id="5eb96-124">Men hvis du bruger funktionen til ordresporing, kan du derefter se frem og tilbage i alle forsyningsordrer, der er foretaget under den oprindelige salgsordre.</span><span class="sxs-lookup"><span data-stu-id="5eb96-124">However, if you are using the Order Tracking feature, then you can look back and forth to all supply orders made under the original sales order.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5eb96-125">Se også</span><span class="sxs-lookup"><span data-stu-id="5eb96-125">See Also</span></span>
<span data-ttu-id="5eb96-126">[Planlægning](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="5eb96-126">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="5eb96-127">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="5eb96-127">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="5eb96-128">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="5eb96-128">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="5eb96-129">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="5eb96-129">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="5eb96-130">Køb</span><span class="sxs-lookup"><span data-stu-id="5eb96-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="5eb96-131">[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="5eb96-131">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="5eb96-132">Konfigurere bedste fremgangsmåder: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="5eb96-132">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="5eb96-133">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5eb96-133">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]