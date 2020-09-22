---
title: Sådan aktiveres pluk efter FEFO | Microsoft Docs
description: Første-udløbet-først ud (FEFO) er en sorteringsmetode, der sikrer, at de ældste elementer med den tidligste udløbsdato plukkes først.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 721b980f8c52e07356fe47bc69aaec90c7fc185f
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784917"
---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="1195d-103">Aktivere pluk af varer efter FEFO</span><span class="sxs-lookup"><span data-stu-id="1195d-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="1195d-104">Første-udløbet-først ud (FEFO) er en sorteringsmetode, der sikrer, at de ældste elementer med den tidligste udløbsdato plukkes først.</span><span class="sxs-lookup"><span data-stu-id="1195d-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="1195d-105">Denne funktionalitet fungerer kun, når følgende kriterier er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="1195d-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="1195d-106">Varen skal have et serie-/lotnummer.</span><span class="sxs-lookup"><span data-stu-id="1195d-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="1195d-107">I opsætningen af varens varesporingskode skal feltet **SN-logistiksporing** eller feltet **Lot-lagersporing** være markeret.</span><span class="sxs-lookup"><span data-stu-id="1195d-107">On the item’s item tracking code setup, the **SN Warehouse Tracking** field or the **Lot Warehouse Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="1195d-108">Varen skal bogføres til lageret med en udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="1195d-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="1195d-109">Afkrydsningsfeltet **Kræv pluk** skal være markeret på lokationskortet.</span><span class="sxs-lookup"><span data-stu-id="1195d-109">On the location card, the **Require Pick** check box must be selected.</span></span>  
-   <span data-ttu-id="1195d-110">Afkrydsningsfeltet **Vælg i overensstemmelse med FEFO** skal være markeret på lokationskortet.</span><span class="sxs-lookup"><span data-stu-id="1195d-110">On the location card, the **Pick According to FEFO** check box must be selected.</span></span>  
-   <span data-ttu-id="1195d-111">Afkrydsningsfeltet **Tvungen placering** skal være markeret på lokationskortet.</span><span class="sxs-lookup"><span data-stu-id="1195d-111">On the location card, the **Bin Mandatory** check box must be selected.</span></span>  

 <span data-ttu-id="1195d-112">Når alle kriterierne er opfyldt, sorteres serie-/lotnummererede varer, som skal plukkes, med de ældste først i alle pluk og bevægelser, undtagen for varer, der bruger SN-specifik eller lotspecifik sporing.</span><span class="sxs-lookup"><span data-stu-id="1195d-112">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
> <span data-ttu-id="1195d-113">Hvis nogen varer med serie-/lotnumre bruger specifik sporing, overholdes de først, og under dem vises de resterende, ikke-specifikke serienumre/lotnumre i henhold til FEFO.</span><span class="sxs-lookup"><span data-stu-id="1195d-113">If some serial/lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>
<br /><br />
<span data-ttu-id="1195d-114">Hvis der er to varer med serie- eller lotnumre, der har samme udløbsdato, vælges varen med det laveste serie- eller lotnummer.</span><span class="sxs-lookup"><span data-stu-id="1195d-114">If two serial/lot-numbered items have the same expiration date, then application selects the item with the lowest serial or lot number.</span></span>
<br /><br />
<span data-ttu-id="1195d-115">Når du plukker varer med serie- eller lotnumre på lokationer, der er sat op til styret læg-på-lager, er det kun antal på placeringer af typen *Pluk*, der plukkes i overensstemmelse med FEFO.</span><span class="sxs-lookup"><span data-stu-id="1195d-115">When picking serial/lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
<br /><br />
<span data-ttu-id="1195d-116">Hvis du vil aktivere bevægelser i henhold til FEFO, skal du enten på siden **Flytning (lager)** eller på siden **Bevægelseskladde** lade feltet **Fra placering** være tomt.</span><span class="sxs-lookup"><span data-stu-id="1195d-116">To enable movements according to FEFO, either on the **Inventory Movement** page or the **Movement Worksheet** page, you must leave the **From Bin** field empty.</span></span>  
<br /><br />
<span data-ttu-id="1195d-117">Hvis feltet **Nøje bogføring af udløbsdato** er markeret, er det kun varer, der ikke er udløbet, der inkluderes i plukket.</span><span class="sxs-lookup"><span data-stu-id="1195d-117">If the **Strict Expiration Posting** field is selected, then only items that are not expired will be included in the pick.</span></span> <span data-ttu-id="1195d-118">Dette gælder, selvom du ikke bruger Vælg i overensstemmelse med FEFO.</span><span class="sxs-lookup"><span data-stu-id="1195d-118">This applies even if you are not using Pick according to FEFO.</span></span>

## <a name="see-also"></a><span data-ttu-id="1195d-119">Se også</span><span class="sxs-lookup"><span data-stu-id="1195d-119">See Also</span></span>  
<span data-ttu-id="1195d-120">[Plukke varer](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="1195d-120">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="1195d-121">[Plukke varer til lagerleverance](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="1195d-121">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="1195d-122">[Plukke varer med Pluk fra lager](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="1195d-122">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="1195d-123">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="1195d-123">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="1195d-124">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="1195d-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="1195d-125">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1195d-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
