---
title: Oprette et lokationskort og definere overflytningsruter | Microsoft Docs
description: Du kan oprette et lokationskort for hvert sted, du gemme lagervarer, for eksempel et lagersted eller distributionscenter, og definere ruter for at overflytte varer mellem lokationerne.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5017df2ba46ba81884b2e99e3ea4a1bb983ea681
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785798"
---
# <a name="set-up-locations"></a><span data-ttu-id="34f5d-103">Opsætte lokationer</span><span class="sxs-lookup"><span data-stu-id="34f5d-103">Set Up Locations</span></span>
<span data-ttu-id="34f5d-104">Hvis du køber, gemme eller sælger varer i mere end ét område eller lagersted, skal du oprette hver lokation med et lokationskort og definere overflytningsruter.</span><span class="sxs-lookup"><span data-stu-id="34f5d-104">If you buy, store, or sell items at more than one place or warehouse, you must set each location up with a location card and define transfer routes.</span></span>

<span data-ttu-id="34f5d-105">Du kan derefter oprette dokumentlinjer for en bestemt lokation vis tilgængeligehed pr. lokation og vare samt overføre lagerbeholdning mellem lokationer.</span><span class="sxs-lookup"><span data-stu-id="34f5d-105">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="34f5d-106">Der er flere oplysninger i [Administrere lager](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="34f5d-106">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="to-create-a-location-card"></a><span data-ttu-id="34f5d-107">Sådan oprettes et lokationskort</span><span class="sxs-lookup"><span data-stu-id="34f5d-107">To create a location card</span></span>
1. <span data-ttu-id="34f5d-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lokationer**, og vælg derefter det tilknyttede link.</span><span class="sxs-lookup"><span data-stu-id="34f5d-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="34f5d-109">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="34f5d-109">Choose the **New** action.</span></span>
3. <span data-ttu-id="34f5d-110">På siden **Lokationskort** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="34f5d-110">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="34f5d-111">Gentag trin 2 og 3 for hver lokation, hvor du vil foretage lageropgørelse.</span><span class="sxs-lookup"><span data-stu-id="34f5d-111">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="34f5d-112">Mange af felterne på lokationskortet henviser til håndtering af varer i indgående og udgående lagerprocesser.</span><span class="sxs-lookup"><span data-stu-id="34f5d-112">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="34f5d-113">Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="34f5d-113">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

## <a name="to-create-a-transfer-route"></a><span data-ttu-id="34f5d-114">Sådan oprettes en overflytningsrute</span><span class="sxs-lookup"><span data-stu-id="34f5d-114">To create a transfer route</span></span>
1. <span data-ttu-id="34f5d-115">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Overflytningsruter**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="34f5d-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="34f5d-116">Du kan også vælge handlingen **Overflytningsruter** på enhver **Lokationskort**-side.</span><span class="sxs-lookup"><span data-stu-id="34f5d-116">Alternatively, from any **Location Card** page, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="34f5d-117">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="34f5d-117">Choose the **New** action.</span></span>
4. <span data-ttu-id="34f5d-118">På siden **Lokationskort** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="34f5d-118">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="34f5d-119">Du kan nu overflytte lagervarer mellem to lokationer.</span><span class="sxs-lookup"><span data-stu-id="34f5d-119">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="34f5d-120">Du kan finde flere oplysninger i [Overflytte lagerbeholdning mellem lokationer](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="34f5d-120">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="see-also"></a><span data-ttu-id="34f5d-121">Se også</span><span class="sxs-lookup"><span data-stu-id="34f5d-121">See Also</span></span>
[<span data-ttu-id="34f5d-122">Administrere lager</span><span class="sxs-lookup"><span data-stu-id="34f5d-122">Manage Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="34f5d-123">[Overflytte lagerbeholdning mellem lokationer](inventory-how-transfer-between-locations.md)  </span><span class="sxs-lookup"><span data-stu-id="34f5d-123">[Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md)  </span></span>  
<span data-ttu-id="34f5d-124">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="34f5d-124">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="34f5d-125">Ændre, hvilke funktioner der vises</span><span class="sxs-lookup"><span data-stu-id="34f5d-125">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="34f5d-126">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="34f5d-126">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]