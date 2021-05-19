---
title: Massebogføre forbrug
description: Hvis trækmetoden er Manuel, skal du bogføre komponenterne manuelt ved at bruge en forbrugskladde.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0b3ee6ca54e21605b4e9cf340b04656694c9801e
ms.sourcegitcommit: c11ad91a389ed72532f5513654fdc7909b20aed9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935182"
---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="73008-103">Massebogføre produktionsforbrug</span><span class="sxs-lookup"><span data-stu-id="73008-103">Batch Post Production Consumption</span></span>

<span data-ttu-id="73008-104">Hvis trækmetoden er **Manuel**, skal du bogføre komponenterne manuelt ved at bruge en forbrugskladde.</span><span class="sxs-lookup"><span data-stu-id="73008-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>  

>[!NOTE]
> <span data-ttu-id="73008-105">Hvis du har markeret feltet **Kræv pluk** på lokationskortet for at angive, at lokationen kræver behandling af lagerpluk, behøver du ikke bruge denne kørsel.</span><span class="sxs-lookup"><span data-stu-id="73008-105">If you have placed a check mark in the **Require Pick** field on the location card to indicate that the location requires inventory pick processing, then you do not need to use this batch job.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="73008-106">håndterer forbruget, når du bogfører lagerpluk.</span><span class="sxs-lookup"><span data-stu-id="73008-106">will handle consumption when you post the inventory pick.</span></span> <span data-ttu-id="73008-107">Du kan finde flere oplysninger i [Plukke til produktion i grundlæggende lageropsætninger](warehouse-how-to-pick-for-production.md#pick-for-production-in-basic-warehouse-configurations)</span><span class="sxs-lookup"><span data-stu-id="73008-107">For more information, see [Pick for Production in Basic Warehouse Configurations](warehouse-how-to-pick-for-production.md#pick-for-production-in-basic-warehouse-configurations).</span></span>  

<span data-ttu-id="73008-108">Du kan også konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] til automatisk at bogføre (*trække*) komponenterne, når du starter eller afslutter produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="73008-108">You can also set up [!INCLUDE[prod_short](includes/prod_short.md)] to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="73008-109">Du kan finde flere oplysninger i [Aktivere udtrækning af komponenter i henhold til operationsafgang](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="73008-109">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="73008-110">Sådan bogføres forbrug for en eller flere produktionsordrelinjer</span><span class="sxs-lookup"><span data-stu-id="73008-110">To post consumption for one or more production order lines</span></span>

1. <span data-ttu-id="73008-111">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Forbrugskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="73008-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="73008-112">Udfyld felterne med produktionsordredata og forbrugsdata.</span><span class="sxs-lookup"><span data-stu-id="73008-112">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="73008-113">Brug handlingen **Beregn forbrug** til at generere kladdelinjer fra produktionsordrer, der er baseres på den aktuelle afgang (mængden af færdige varer, der er rapporteret), eller den forventede afgang (mængden af færdige varer, du forventer at producere).</span><span class="sxs-lookup"><span data-stu-id="73008-113">Use the **Calc. Consumption** action to generate journal lines from production orders based on the actual output (the quantity of finished goods that you have reported) or on the expected output (the quantity of finished goods that you expect to produce).</span></span>

    > [!NOTE]
    > <span data-ttu-id="73008-114">Hvis du har konfigureret lokationskortet til at kræve behandling af lagerpluk, er det kun de antal, der allerede er plukket via en lageraktivitet, der kan angives i feltet **Antal** på siden **Forbrugskladde**, ikke beregnede antal.</span><span class="sxs-lookup"><span data-stu-id="73008-114">If you configured the location card to require warehouse pick processing, then only quantities that are already picked through a warehouse activity can be entered in the **Quantity** field in the **Consumption Journal** page, not any calculated quantity.</span></span> <span data-ttu-id="73008-115">Du kan finde flere oplysninger i [Plukke til produktion eller montage i avancerede lageropsætninger](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)</span><span class="sxs-lookup"><span data-stu-id="73008-115">For more information, see [Pick for Production or Assembly in Advanced Warehouse Configurations](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)</span></span>

3. <span data-ttu-id="73008-116">Vælg handlingen **Bogfør** for at bogføre forbruget.</span><span class="sxs-lookup"><span data-stu-id="73008-116">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="73008-117">De relaterede lagerbeholdninger er reduceret.</span><span class="sxs-lookup"><span data-stu-id="73008-117">The related inventories are reduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="73008-118">Se også</span><span class="sxs-lookup"><span data-stu-id="73008-118">See Also</span></span>

[<span data-ttu-id="73008-119">Produktion</span><span class="sxs-lookup"><span data-stu-id="73008-119">Manufacturing</span></span>](production-manage-manufacturing.md)  
[<span data-ttu-id="73008-120">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="73008-120">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
[<span data-ttu-id="73008-121">Skabelon</span><span class="sxs-lookup"><span data-stu-id="73008-121">Planning</span></span>](production-planning.md)  
[<span data-ttu-id="73008-122">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="73008-122">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="73008-123">Køb</span><span class="sxs-lookup"><span data-stu-id="73008-123">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="73008-124">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="73008-124">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

[!INCLUDE[footer-include](includes/footer-banner.md)]
