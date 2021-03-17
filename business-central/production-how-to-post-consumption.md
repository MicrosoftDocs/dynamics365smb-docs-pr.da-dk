---
title: Sådan massebogføres forbrug | Microsoft Docs
description: Hvis trækmetoden er **Manuel**, skal du bogføre komponenterne manuelt ved at bruge en forbrugskladde.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0bf0a92d05b6c9ecb3d5a5ba054b4675680ad43c
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391795"
---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="f7897-103">Massebogføre produktionsforbrug</span><span class="sxs-lookup"><span data-stu-id="f7897-103">Batch Post Production Consumption</span></span>
<span data-ttu-id="f7897-104">Hvis trækmetoden er **Manuel**, skal du bogføre komponenterne manuelt ved at bruge en forbrugskladde.</span><span class="sxs-lookup"><span data-stu-id="f7897-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>

<span data-ttu-id="f7897-105">Du kan også angive systemet til automatisk for at bogføre (*trække*) komponenterne, når du starter eller afslutter produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="f7897-105">You can also set the system up to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="f7897-106">Du kan finde flere oplysninger i [Aktivere udtrækning af komponenter i henhold til operationsafgang](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="f7897-106">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="f7897-107">Sådan bogføres forbrug for en eller flere produktionsordrelinjer</span><span class="sxs-lookup"><span data-stu-id="f7897-107">To post consumption for one or more production order lines</span></span>  
1.  <span data-ttu-id="f7897-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Forbrugskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f7897-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f7897-109">Udfyld felterne med produktionsordredata og forbrugsdata.</span><span class="sxs-lookup"><span data-stu-id="f7897-109">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="f7897-110">Hvis den lagerlokation, hvor komponenterne opbevares, er angivet til at bruge placeringer, men ikke kræver pluk, skal du tildele en placeringskode til kladdelinjen for at angive, hvor varerne skal hentes på lageret.</span><span class="sxs-lookup"><span data-stu-id="f7897-110">If the warehouse location where the components are stored is set up to use bins but does not require pick processing, assign a bin code to the journal line to indicate where the items should be taken from in the warehouse.</span></span> <span data-ttu-id="f7897-111">Du kan finde flere oplysninger i [Plukke til produktion eller montage](warehouse-how-to-pick-for-production.md).</span><span class="sxs-lookup"><span data-stu-id="f7897-111">For more information, see [Pick for Production or Assembly](warehouse-how-to-pick-for-production.md).</span></span>  
3.  <span data-ttu-id="f7897-112">Vælg handlingen **Bogfør** for at bogføre forbruget.</span><span class="sxs-lookup"><span data-stu-id="f7897-112">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="f7897-113">De tilknyttede vareposter reduceres.</span><span class="sxs-lookup"><span data-stu-id="f7897-113">The related item ledger entries are reduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7897-114">Se også</span><span class="sxs-lookup"><span data-stu-id="f7897-114">See Also</span></span>  
<span data-ttu-id="f7897-115">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="f7897-115">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="f7897-116">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="f7897-116">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="f7897-117">[Planlægning](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="f7897-117">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="f7897-118">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="f7897-118">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="f7897-119">Køb</span><span class="sxs-lookup"><span data-stu-id="f7897-119">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="f7897-120">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f7897-120">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]