---
title: Sådan oprettes speditører | Microsoft Docs
description: Du kan angive en kode for hver speditør og angive oplysninger om dem.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fbd27caed8be1e7231f98964890fafed66c7bbbb
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748214"
---
# <a name="set-up-shipping-agents"></a><span data-ttu-id="5395e-103">Oprette speditører</span><span class="sxs-lookup"><span data-stu-id="5395e-103">Set Up Shipping Agents</span></span>
<span data-ttu-id="5395e-104">Du kan angive en kode for hver speditør og angive oplysninger om dem.</span><span class="sxs-lookup"><span data-stu-id="5395e-104">You can set up a code for each of your shipping agents and enter information about them.</span></span>  

<span data-ttu-id="5395e-105">Hvis du angiver en internetadresse for speditøren, og denne tilbyder pakkesporing over internettet, kan du anvende programmets automatiske pakkesporingsfunktion.</span><span class="sxs-lookup"><span data-stu-id="5395e-105">If you enter an Internet address for the shipping agent, and the agent provides package tracking services on the Internet, you can use the automatic package tracking feature.</span></span> <span data-ttu-id="5395e-106">Du kan finde flere oplysninger under [Spore pakker](sales-how-track-packages.md).</span><span class="sxs-lookup"><span data-stu-id="5395e-106">For more information, see [Track Packages](sales-how-track-packages.md).</span></span>

<span data-ttu-id="5395e-107">Når du angiver speditører i salgsordrerne, kan du også angive den service, som den enkelte speditør tilbyder.</span><span class="sxs-lookup"><span data-stu-id="5395e-107">When you set up shipping agents on your sales orders, you can also specify the services that each shipping agent offers.</span></span>  
<span data-ttu-id="5395e-108">Du kan angive et ubegrænset antal serviceydelser for hver speditør, og du kan angive en transporttid for hver service.</span><span class="sxs-lookup"><span data-stu-id="5395e-108">For each shipping agent, you can set up an unlimited number of services, and you can specify a shipping time for each service.</span></span>  

<span data-ttu-id="5395e-109">Når du har tilknyttet en speditørservice til salgsordrelinjen, medtages transporttiden for den pågældende service i beregningen af ordrebekræftelsen for linjen.</span><span class="sxs-lookup"><span data-stu-id="5395e-109">When you have assigned a shipping agent service to a sales order line, the shipping time of the service will be included in the order promising calculation, for that line.</span></span> <span data-ttu-id="5395e-110">Du kan finde flere oplysninger i [Beregne ordrebekræftelsesdatoer](sales-how-to-calculate-order-promising-dates.md).</span><span class="sxs-lookup"><span data-stu-id="5395e-110">For more information, see [Calculate Order Promising Dates](sales-how-to-calculate-order-promising-dates.md).</span></span>

## <a name="to-set-up-a-shipping-agent"></a><span data-ttu-id="5395e-111">Sådan oprettes en speditør</span><span class="sxs-lookup"><span data-stu-id="5395e-111">To set up a shipping agent</span></span>  
1.  <span data-ttu-id="5395e-112">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Speditører**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="5395e-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipping Agents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5395e-113">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="5395e-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="5395e-114">.</span><span class="sxs-lookup"><span data-stu-id="5395e-114">.</span></span>  
3.  <span data-ttu-id="5395e-115">Vælg handlingen **Speditørservice**.</span><span class="sxs-lookup"><span data-stu-id="5395e-115">Choose the **Shipping Agent Services** action.</span></span>
4. <span data-ttu-id="5395e-116">I feltet **Speditørservice** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="5395e-116">In the **Shipping Agent Services**, fill in the fields as necessary.</span></span>

> [!NOTE]  
>  <span data-ttu-id="5395e-117">Hvis du sletter speditøren på ordrelinjen, slettes speditørservicekoden også.</span><span class="sxs-lookup"><span data-stu-id="5395e-117">If you delete the shipping agent on the order line, the shipping agent service code is also deleted.</span></span> <span data-ttu-id="5395e-118">Derefter beregnes oplysningerne i de felter, der er baseret på speditørservicen, igen.</span><span class="sxs-lookup"><span data-stu-id="5395e-118">The contents of fields that were based in part on the shipping agent service are recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5395e-119">Se også</span><span class="sxs-lookup"><span data-stu-id="5395e-119">See Also</span></span>
[<span data-ttu-id="5395e-120">Oprette leveringsformer</span><span class="sxs-lookup"><span data-stu-id="5395e-120">Set Up Shipment Methods</span></span>](sales-how-set-up-shipment-methods.md)  
<span data-ttu-id="5395e-121">[Spore pakker](sales-how-track-packages.md)  </span><span class="sxs-lookup"><span data-stu-id="5395e-121">[Track Packages](sales-how-track-packages.md)  </span></span>  
[<span data-ttu-id="5395e-122">Logistik</span><span class="sxs-lookup"><span data-stu-id="5395e-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="5395e-123">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="5395e-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="5395e-124">[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="5395e-124">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="5395e-125">[Montagestyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="5395e-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="5395e-126">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="5395e-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="5395e-127">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5395e-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
