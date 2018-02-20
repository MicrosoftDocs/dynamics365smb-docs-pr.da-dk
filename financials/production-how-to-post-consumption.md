---
title: "Sådan massebogføres forbrug | Microsoft Docs"
description: "Hvis trækmetoden er **Manuel**, skal du bogføre komponenterne manuelt ved at bruge en forbrugskladde."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 67d80735f7ea217fa62317283246f098294323da
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="14d3b-103">Massebogføre produktionsforbrug</span><span class="sxs-lookup"><span data-stu-id="14d3b-103">Batch Post Production Consumption</span></span>
<span data-ttu-id="14d3b-104">Hvis trækmetoden er **Manuel**, skal du bogføre komponenterne manuelt ved at bruge en forbrugskladde.</span><span class="sxs-lookup"><span data-stu-id="14d3b-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>

<span data-ttu-id="14d3b-105">Du kan også angive systemet til automatisk for at bogføre (*trække*) komponenterne, når du starter eller afslutter produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="14d3b-105">You can also set the system up to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="14d3b-106">Du kan finde flere oplysninger i [Aktivere udtrækning af komponenter i henhold til operationsafgang](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="14d3b-106">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="14d3b-107">Sådan bogføres forbrug for en eller flere produktionsordrelinjer</span><span class="sxs-lookup"><span data-stu-id="14d3b-107">To post consumption for one or more production order lines</span></span>  
1.  <span data-ttu-id="14d3b-108">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Forbrugskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="14d3b-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="14d3b-109">Udfyld felterne med produktionsordredata og forbrugsdata.</span><span class="sxs-lookup"><span data-stu-id="14d3b-109">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="14d3b-110">Hvis den lagerlokation, hvor komponenterne opbevares, er angivet til at bruge placeringer, men ikke kræver pluk, skal du tildele en placeringskode til kladdelinjen for at angive, hvor varerne skal hentes på lageret.</span><span class="sxs-lookup"><span data-stu-id="14d3b-110">If the warehouse location where the components are stored is set up to use bins but does not require pick processing, assign a bin code to the journal line to indicate where the items should be taken from in the warehouse.</span></span> <span data-ttu-id="14d3b-111">Du kan finde flere oplysninger i [Plukke til produktion eller montage](warehouse-how-to-pick-for-production.md).</span><span class="sxs-lookup"><span data-stu-id="14d3b-111">For more information, see [Pick for Production or Assembly](warehouse-how-to-pick-for-production.md).</span></span>  
3.  <span data-ttu-id="14d3b-112">Vælg handlingen **Bogfør** for at bogføre forbruget.</span><span class="sxs-lookup"><span data-stu-id="14d3b-112">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="14d3b-113">De tilknyttede vareposter reduceres.</span><span class="sxs-lookup"><span data-stu-id="14d3b-113">The related item ledger entries are reduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="14d3b-114">Se også</span><span class="sxs-lookup"><span data-stu-id="14d3b-114">See Also</span></span>  
<span data-ttu-id="14d3b-115">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="14d3b-115">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="14d3b-116">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="14d3b-116">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="14d3b-117">[Planlægning](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="14d3b-117">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="14d3b-118">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="14d3b-118">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="14d3b-119">Køb</span><span class="sxs-lookup"><span data-stu-id="14d3b-119">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="14d3b-120">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="14d3b-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

