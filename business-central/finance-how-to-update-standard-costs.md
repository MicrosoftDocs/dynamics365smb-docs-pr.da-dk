---
title: Sådan opdateres standardkostpriser | Microsoft Docs
description: Du skal regelmæssigt opdatere standardkostprisen for komponenter og akkumulere de nye omkostninger til den overordnede vare.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 99783deca985a630a46b745b1e7f0a92eb327642
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784563"
---
# <a name="update-standard-costs"></a><span data-ttu-id="8c5ac-103">Opdatere standardkostpriser</span><span class="sxs-lookup"><span data-stu-id="8c5ac-103">Update Standard Costs</span></span>
<span data-ttu-id="8c5ac-104">Du skal regelmæssigt opdatere standardkostprisen for komponenter og akkumulere de nye omkostninger til den overordnede vare.</span><span class="sxs-lookup"><span data-stu-id="8c5ac-104">You must periodically update the standard costs of components and roll the new costs up to the parent item.</span></span> <span data-ttu-id="8c5ac-105">Processen består normalt af følgende fire trin:</span><span class="sxs-lookup"><span data-stu-id="8c5ac-105">The process typically consists of the following four steps:</span></span>  

1.  <span data-ttu-id="8c5ac-106">Opdatere omkostninger på komponent- og kapacitetsniveau.</span><span class="sxs-lookup"><span data-stu-id="8c5ac-106">Update costs at the component and capacity levels.</span></span> <span data-ttu-id="8c5ac-107">Du kan finde flere oplysninger i kørslen **Foreslå kostpris (standard)**.</span><span class="sxs-lookup"><span data-stu-id="8c5ac-107">For more information, see the **Suggest Item Standard Cost** batch job.</span></span>  
2.  <span data-ttu-id="8c5ac-108">Konsolidering og akkumulering af komponent- og kapacitetsomkostninger til beregning af de samlede fremstillings- eller montageomkostninger for varerne.</span><span class="sxs-lookup"><span data-stu-id="8c5ac-108">Consolidate and roll up the component and capacity costs to calculate the total manufacturing or assembly cost of the items.</span></span>  
3.  <span data-ttu-id="8c5ac-109">Implementere de standardkostpriser, der angives, når du kører de tidligere kørsler.</span><span class="sxs-lookup"><span data-stu-id="8c5ac-109">Implement the standard costs that are entered when you run the previous batch jobs.</span></span> <span data-ttu-id="8c5ac-110">Standardkostpriserne træder ikke i kraft, før de er implementeret.</span><span class="sxs-lookup"><span data-stu-id="8c5ac-110">The standard costs do not take effect until they are implemented.</span></span> <span data-ttu-id="8c5ac-111">Du kan finde flere oplysninger i Implementer std.kostprisændringer.</span><span class="sxs-lookup"><span data-stu-id="8c5ac-111">For more information, see Implement Standard Cost Changes.</span></span>  
4.  <span data-ttu-id="8c5ac-112">Implementere ændringer for at opdatere feltet **Kostpris** på varekortet og udføre regulering af lagerværdi.</span><span class="sxs-lookup"><span data-stu-id="8c5ac-112">Implement the changes to update the **Unit Cost** field on the item card and perform inventory revaluation.</span></span> <span data-ttu-id="8c5ac-113">Du kan finde flere oplysninger i [Regulere lagerbeholdningen](inventory-how-revalue-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="8c5ac-113">For more information, see [Revalue Inventory](inventory-how-revalue-inventory.md).</span></span>  

<span data-ttu-id="8c5ac-114">Du kan finde flere oplysninger i [Om beregning af standardkostpris](finance-about-calculating-standard-cost.md).</span><span class="sxs-lookup"><span data-stu-id="8c5ac-114">For more information, see [About Calculating Standard Cost](finance-about-calculating-standard-cost.md).</span></span>  
## <a name="to-update-standard-costs"></a><span data-ttu-id="8c5ac-115">Sådan opdateres standardkostpriser</span><span class="sxs-lookup"><span data-stu-id="8c5ac-115">To update standard costs</span></span>  
1.  <span data-ttu-id="8c5ac-116">Udfør kørslen **Juster kostpris - vareposter**.</span><span class="sxs-lookup"><span data-stu-id="8c5ac-116">Run the **Adjust Cost-Item Entries** batch job.</span></span>  
2.  <span data-ttu-id="8c5ac-117">Udfør kørslen **Bogfør lagerregulering**.</span><span class="sxs-lookup"><span data-stu-id="8c5ac-117">Run the **Post Inventory Cost to G/L** batch job.</span></span>  
3.  <span data-ttu-id="8c5ac-118">Åbn **Standardkostpriskladde**, og brug en eller flere af følgende funktioner:</span><span class="sxs-lookup"><span data-stu-id="8c5ac-118">Open the **Standard Cost Worksheet** and use one or more of the following functions:</span></span>  

    1.  <span data-ttu-id="8c5ac-119">Udfør kørslen **Foreslå kostpris (standard)**.</span><span class="sxs-lookup"><span data-stu-id="8c5ac-119">Run the **Suggest Item Standard Cost** batch job.</span></span>  
    2.  <span data-ttu-id="8c5ac-120">Gennemse resultaterne, og foretag de nødvendige ændringer.</span><span class="sxs-lookup"><span data-stu-id="8c5ac-120">Review the results and make changes as necessary.</span></span>  
    3.  <span data-ttu-id="8c5ac-121">Udfør kørslen **Foreslå kapacitetkostpris (standard)**.</span><span class="sxs-lookup"><span data-stu-id="8c5ac-121">Run the **Suggest Capacity Standard Cost** batch job.</span></span>  
    4.  <span data-ttu-id="8c5ac-122">Gennemse resultaterne, og foretag de nødvendige ændringer.</span><span class="sxs-lookup"><span data-stu-id="8c5ac-122">Review the results and make changes as necessary.</span></span>
    5. <span data-ttu-id="8c5ac-123">Udfør kørslen **Akkum. standardkostpris**.</span><span class="sxs-lookup"><span data-stu-id="8c5ac-123">Run the **Roll Up Standard Cost** batch job.</span></span>
    6.  <span data-ttu-id="8c5ac-124">Gennemse resultaterne, og foretag de nødvendige ændringer.</span><span class="sxs-lookup"><span data-stu-id="8c5ac-124">Review the results and make changes as necessary.</span></span>
    7.  <span data-ttu-id="8c5ac-125">Udfør kørslen **Implementer std.kostprisændringer**.</span><span class="sxs-lookup"><span data-stu-id="8c5ac-125">Run the **Implement Standard Cost Changes** batch job.</span></span>  
4.  <span data-ttu-id="8c5ac-126">Gennemse og bogfør siden **Værdireguleringskladde** , som er blevet udfyldt med posterne fra det forrige trin i processen.</span><span class="sxs-lookup"><span data-stu-id="8c5ac-126">Review and post the **Revaluation Journal** page, which has been populated with entries from the previous steps in this process.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8c5ac-127">Se også</span><span class="sxs-lookup"><span data-stu-id="8c5ac-127">See Also</span></span>  
 <span data-ttu-id="8c5ac-128">[Om beregning af standardomkostning](finance-about-calculating-standard-cost.md) </span><span class="sxs-lookup"><span data-stu-id="8c5ac-128">[About Calculating Standard Cost](finance-about-calculating-standard-cost.md) </span></span>  
 <span data-ttu-id="8c5ac-129">[Administrere lageromkostninger](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="8c5ac-129">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 <span data-ttu-id="8c5ac-130">[Designoplysninger: Kostmetoder](design-details-costing-methods.md) [Finans](finance.md)</span><span class="sxs-lookup"><span data-stu-id="8c5ac-130">[Design Details: Costing Methods](design-details-costing-methods.md) [Finance](finance.md)</span></span>  
 <span data-ttu-id="8c5ac-131">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8c5ac-131">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]