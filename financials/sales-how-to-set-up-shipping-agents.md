---
title: "Sådan oprettes speditører | Microsoft Docs"
description: "Du kan angive en kode for hver speditør og angive oplysninger om dem."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 84a5d9eb8757dc82834c17327ffbb510cd15fa1a
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-shipping-agents"></a><span data-ttu-id="0a56a-103">Sådan oprettes speditører</span><span class="sxs-lookup"><span data-stu-id="0a56a-103">How to: Set Up Shipping Agents</span></span>
<span data-ttu-id="0a56a-104">Du kan angive en kode for hver speditør og angive oplysninger om dem.</span><span class="sxs-lookup"><span data-stu-id="0a56a-104">You can set up a code for each of your shipping agents and enter information about them.</span></span>  

<span data-ttu-id="0a56a-105">Hvis du angiver en internetadresse for speditøren, og denne tilbyder pakkesporing over internettet, kan du anvende programmets automatiske pakkesporingsfunktion.</span><span class="sxs-lookup"><span data-stu-id="0a56a-105">If you enter an Internet address for the shipping agent, and the agent provides package tracking services on the Internet, you can use the automatic package tracking feature.</span></span> <span data-ttu-id="0a56a-106">Du kan finde flere oplysninger under [Sådan spores pakker](sales-how-track-packages.md).</span><span class="sxs-lookup"><span data-stu-id="0a56a-106">For more information, see [How to: Track Packages](sales-how-track-packages.md).</span></span>

<span data-ttu-id="0a56a-107">Når du angiver speditører i salgsordrerne, kan du også angive den service, som den enkelte speditør tilbyder.</span><span class="sxs-lookup"><span data-stu-id="0a56a-107">When you set up shipping agents on your sales orders, you can also specify the services that each shipping agent offers.</span></span>  
<span data-ttu-id="0a56a-108">Du kan angive et ubegrænset antal serviceydelser for hver speditør, og du kan angive en transporttid for hver service.</span><span class="sxs-lookup"><span data-stu-id="0a56a-108">For each shipping agent, you can set up an unlimited number of services, and you can specify a shipping time for each service.</span></span>  

<span data-ttu-id="0a56a-109">Når du har tilknyttet en speditørservice til salgsordrelinjen, medtages transporttiden for den pågældende service i beregningen af ordrebekræftelsen for linjen.</span><span class="sxs-lookup"><span data-stu-id="0a56a-109">When you have assigned a shipping agent service to a sales order line, the shipping time of the service will be included in the order promising calculation, for that line.</span></span> <span data-ttu-id="0a56a-110">Du kan finde flere oplysninger i [Sådan beregnes ordrebekræftelsesdatoer](sales-how-to-calculate-order-promising-dates.md).</span><span class="sxs-lookup"><span data-stu-id="0a56a-110">For more information, see [How to: Calculate Order Promising Dates](sales-how-to-calculate-order-promising-dates.md).</span></span>

## <a name="to-set-up-a-shipping-agent"></a><span data-ttu-id="0a56a-111">Sådan oprettes en speditør</span><span class="sxs-lookup"><span data-stu-id="0a56a-111">To set up a shipping agent</span></span>  
1.  <span data-ttu-id="0a56a-112">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Speditører**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="0a56a-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Shipping Agents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0a56a-113">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="0a56a-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="0a56a-114">.</span><span class="sxs-lookup"><span data-stu-id="0a56a-114">.</span></span>  
3.  <span data-ttu-id="0a56a-115">Vælg handlingen **Speditørservice**.</span><span class="sxs-lookup"><span data-stu-id="0a56a-115">Choose the **Shipping Agent Services** action.</span></span>
4. <span data-ttu-id="0a56a-116">I feltet **Speditørservice** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="0a56a-116">In the **Shipping Agent Services**, fill in the fields as necessary.</span></span>

> [!NOTE]  
>  <span data-ttu-id="0a56a-117">Hvis du sletter speditøren på ordrelinjen, slettes speditørservicekoden også.</span><span class="sxs-lookup"><span data-stu-id="0a56a-117">If you delete the shipping agent on the order line, the shipping agent service code is also deleted.</span></span> <span data-ttu-id="0a56a-118">Derefter beregnes oplysningerne i de felter, der er baseret på speditørservicen, igen.</span><span class="sxs-lookup"><span data-stu-id="0a56a-118">The contents of fields that were based in part on the shipping agent service are recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0a56a-119">Se også</span><span class="sxs-lookup"><span data-stu-id="0a56a-119">See Also</span></span>
<span data-ttu-id="0a56a-120">[Sådan spores pakker](sales-how-track-packages.md)  </span><span class="sxs-lookup"><span data-stu-id="0a56a-120">[How to: Track Packages](sales-how-track-packages.md)  </span></span>  
[<span data-ttu-id="0a56a-121">Logistik</span><span class="sxs-lookup"><span data-stu-id="0a56a-121">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="0a56a-122">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="0a56a-122">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="0a56a-123">[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="0a56a-123">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="0a56a-124">[Montagestyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="0a56a-124">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="0a56a-125">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="0a56a-125">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="0a56a-126">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0a56a-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
