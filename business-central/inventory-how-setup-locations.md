---
title: Oprette et lokationskort og definere overflytningsruter | Microsoft Docs
description: Du kan oprette et lokationskort for hvert sted, du gemme lagervarer, for eksempel et lagersted eller distributionscenter, og definere ruter for at overflytte varer mellem lokationerne.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 01/25/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: 45943ef97eee9d6bf24fd679e5dbbab96f5177f8
ms.contentlocale: da-dk
ms.lasthandoff: 04/18/2018

---
# <a name="set-up-locations"></a><span data-ttu-id="0a06e-103">Opsætte lokationer</span><span class="sxs-lookup"><span data-stu-id="0a06e-103">Set Up Locations</span></span>
<span data-ttu-id="0a06e-104">Hvis du køber, gemme eller sælger varer i mere end ét område eller lagersted, skal du oprette hver lokation med et lokationskort og definere overflytningsruter.</span><span class="sxs-lookup"><span data-stu-id="0a06e-104">If you buy, store, or sell items at more than one place or warehouse, you must set each location up with a location card and define transfer routes.</span></span>

<span data-ttu-id="0a06e-105">Du kan derefter oprette dokumentlinjer for en bestemt lokation vis tilgængeligehed pr. lokation og vare samt overføre lagerbeholdning mellem lokationer.</span><span class="sxs-lookup"><span data-stu-id="0a06e-105">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="0a06e-106">Der er flere oplysninger i [Administrere lager](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="0a06e-106">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>

## <a name="to-create-a-location-card"></a><span data-ttu-id="0a06e-107">Sådan oprettes et lokationskort</span><span class="sxs-lookup"><span data-stu-id="0a06e-107">To create a location card</span></span>
1. <span data-ttu-id="0a06e-108">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lokationer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="0a06e-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="0a06e-109">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0a06e-109">Choose the **New** action.</span></span>
3. <span data-ttu-id="0a06e-110">I vinduet **Lokationskort** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="0a06e-110">In the **Location Card** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="0a06e-111">Gentag trin 2 og 3 for hver lokation, hvor du vil foretage lageropgørelse.</span><span class="sxs-lookup"><span data-stu-id="0a06e-111">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="0a06e-112">Mange af felterne på lokationskortet henviser til håndtering af varer i indgående og udgående lagerprocesser.</span><span class="sxs-lookup"><span data-stu-id="0a06e-112">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="0a06e-113">Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="0a06e-113">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

## <a name="to-create-a-transfer-route"></a><span data-ttu-id="0a06e-114">Sådan oprettes en overflytningsrute</span><span class="sxs-lookup"><span data-stu-id="0a06e-114">To create a transfer route</span></span>
1. <span data-ttu-id="0a06e-115">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Overflytningsruter**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="0a06e-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="0a06e-116">Du kan også vælge handlingen **Overflytningsruter** i ethvert **Lokationskort**-vindue.</span><span class="sxs-lookup"><span data-stu-id="0a06e-116">Alternatively, from any **Location Card** window, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="0a06e-117">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0a06e-117">Choose the **New** action.</span></span>
4. <span data-ttu-id="0a06e-118">I vinduet **Lokationskort** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="0a06e-118">In the **Location Card** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="0a06e-119">Du kan nu overflytte lagervarer mellem to lokationer.</span><span class="sxs-lookup"><span data-stu-id="0a06e-119">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="0a06e-120">Du kan finde flere oplysninger i [Overflytte lagerbeholdning mellem lokationer](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="0a06e-120">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="see-also"></a><span data-ttu-id="0a06e-121">Se også</span><span class="sxs-lookup"><span data-stu-id="0a06e-121">See Also</span></span>
[<span data-ttu-id="0a06e-122">Administrere lager</span><span class="sxs-lookup"><span data-stu-id="0a06e-122">Manage Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="0a06e-123">[Overflytte lagerbeholdning mellem lokationer](inventory-how-transfer-between-locations.md)  </span><span class="sxs-lookup"><span data-stu-id="0a06e-123">[Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md)  </span></span>  
<span data-ttu-id="0a06e-124">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0a06e-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="0a06e-125">Ændre, hvilke funktioner der vises</span><span class="sxs-lookup"><span data-stu-id="0a06e-125">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="0a06e-126">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="0a06e-126">General Business Functionality</span></span>](ui-across-business-areas.md)

