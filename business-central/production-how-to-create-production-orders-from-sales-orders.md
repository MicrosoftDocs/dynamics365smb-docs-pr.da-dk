---
title: Oprette produktionsordrer fra salgsordrer
description: Du kan oprette produktionsordrer fra salgsordrer
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/28/2021
ms.author: edupont
ms.openlocfilehash: 438f4d4e1833ba607ceedb9f5d9450c0a4dbb680
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115232"
---
# <a name="create-production-orders-from-sales-orders"></a><span data-ttu-id="4544f-103">Oprette produktionsordrer fra salgsordrer</span><span class="sxs-lookup"><span data-stu-id="4544f-103">Create Production Orders from Sales Orders</span></span>
<span data-ttu-id="4544f-104">Du kan oprette produktionsordrer til producerede varer direkte fra salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="4544f-104">You can create production orders for produced items directly from sales orders.</span></span>  

## <a name="to-create-a-production-order-from-a-sales-order"></a><span data-ttu-id="4544f-105">Sådan oprettes en produktionsordre fra en salgsordre</span><span class="sxs-lookup"><span data-stu-id="4544f-105">To create a production order from a sales order</span></span>  

1.  <span data-ttu-id="4544f-106">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordre**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="4544f-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4544f-107">Vælg den salgsordre, du vil oprette en produktionsordre for.</span><span class="sxs-lookup"><span data-stu-id="4544f-107">Select the sales order you want to create a production order for.</span></span>  
3.  <span data-ttu-id="4544f-108">Vælg handlingen **Planlægning**.</span><span class="sxs-lookup"><span data-stu-id="4544f-108">Choose the **Planning** action.</span></span> <span data-ttu-id="4544f-109">På siden **Salgsordreplanlægning** kan du få vist disponeringen for en salgsordrevare.</span><span class="sxs-lookup"><span data-stu-id="4544f-109">On the **Sales Order Planning** page, you can view the availability of the sales order item.</span></span>  
4.  <span data-ttu-id="4544f-110">Vælg handlingen **Opret prod.ordre**.</span><span class="sxs-lookup"><span data-stu-id="4544f-110">Choose the **Create Prod. Order** action.</span></span>  
5.  <span data-ttu-id="4544f-111">Vælg status og ordretype.</span><span class="sxs-lookup"><span data-stu-id="4544f-111">Select the status and order type.</span></span>  
6.  <span data-ttu-id="4544f-112">Klik på knappen **Ja** for at oprette en eller flere produktionsordrer til de linjer, der har **produktionsordre** i feltet **Genbestillingssystem**.</span><span class="sxs-lookup"><span data-stu-id="4544f-112">Choose the **Yes** button to create one or more production orders for the lines that have **Prod. Order** in their **Replenishment System** field.</span></span>


> [!NOTE]  
> <span data-ttu-id="4544f-113">Linjer i den oprettede projektproduktionsordre, der har behov for **Prod.ordre** i feltet **Genbestillingssystem**, repræsenterer underliggende produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="4544f-113">Demand lines in the created production order that have **Prod. Order** in their **Replenishment System** field represent underlying production orders.</span></span> <span data-ttu-id="4544f-114">Når du har oprettet disse produktionsordrer, skal du huske at identificere eventuelle ekspederet komponentbehov for dem ved hjælp af siden **Ordreplanlægning** eller funktionen **Omplanlæg** fra oprettede ordrer.</span><span class="sxs-lookup"><span data-stu-id="4544f-114">After you have generated these production orders, remember to identify any unfulfilled component demand for them using the **Order Planning** page or the **Replan** function from created orders.</span></span> 

## <a name="order-type"></a><span data-ttu-id="4544f-115">Ordretype</span><span class="sxs-lookup"><span data-stu-id="4544f-115">Order type</span></span>  
<span data-ttu-id="4544f-116">Du kan vælge mellem to måder at oprette produktionsordrer på, som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="4544f-116">You can choose between two ways to create the production orders as outlined in the following table.</span></span>

|<span data-ttu-id="4544f-117">Indstilling</span><span class="sxs-lookup"><span data-stu-id="4544f-117">Option</span></span>|<span data-ttu-id="4544f-118">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="4544f-118">Description</span></span>|
|------|-----------|
|<span data-ttu-id="4544f-119">Vareordre</span><span class="sxs-lookup"><span data-stu-id="4544f-119">Item Order</span></span>|<span data-ttu-id="4544f-120">En produktionsordre oprettes for hver enkelt behov produktionsordre, der repræsenteres af a linje i vinduet **Salgsordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="4544f-120">One production order is created for each needed production order that is represented by a line in the **Sales Order Planning** window.</span></span>|
|<span data-ttu-id="4544f-121">Projektordre</span><span class="sxs-lookup"><span data-stu-id="4544f-121">Project Order</span></span>|<span data-ttu-id="4544f-122">En produktionsordre oprettes for hver enkelt produktionsordre, der repræsenteres af en linje i vinduet **Salgsordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="4544f-122">One production order is created for all needed production orders order that are represented by lines in the **Sales Order Planning** window.</span></span> |

<span data-ttu-id="4544f-123">Når du bruger projektordrer, indeholder feltet **Kildetype** i produktionsordren **Salgshoved**, og ordren indeholder flere linjer, en for hver salgslinjevare, der skal produceres.</span><span class="sxs-lookup"><span data-stu-id="4544f-123">When you use project orders, the **Source Type** field of the production order contains **Sales Header** and the order has multiple lines, one for each sales line item that must be produced.</span></span>  


## <a name="see-also"></a><span data-ttu-id="4544f-124">Se også</span><span class="sxs-lookup"><span data-stu-id="4544f-124">See Also</span></span>  
[<span data-ttu-id="4544f-125">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="4544f-125">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="4544f-126">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="4544f-126">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="4544f-127">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="4544f-127">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="4544f-128">Køb</span><span class="sxs-lookup"><span data-stu-id="4544f-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="4544f-129">[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="4544f-129">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="4544f-130">Konfigurere bedste fremgangsmåder: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="4544f-130">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="4544f-131">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4544f-131">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
