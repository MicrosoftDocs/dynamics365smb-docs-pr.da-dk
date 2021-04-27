---
title: Sådan aktiveres pluk efter FEFO | Microsoft Docs
description: Første-udløbet-først ud (FEFO) er en sorteringsmetode, der sikrer, at de ældste elementer med den tidligste udløbsdato plukkes først.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3a47c9daeeab036055a0644e1b389735f7440106
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784063"
---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="5664d-103">Aktivere pluk af varer efter FEFO</span><span class="sxs-lookup"><span data-stu-id="5664d-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="5664d-104">Første-udløbet-først ud (FEFO) er en sorteringsmetode, der sikrer, at de ældste elementer med den tidligste udløbsdato plukkes først.</span><span class="sxs-lookup"><span data-stu-id="5664d-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="5664d-105">Denne funktionalitet fungerer kun, når følgende kriterier er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="5664d-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="5664d-106">Varen skal have et serie-/lotnummer.</span><span class="sxs-lookup"><span data-stu-id="5664d-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="5664d-107">I opsætningen af varens varesporingskode skal feltet **SN-logistiksporing** eller feltet **Lot-lagersporing** være markeret.</span><span class="sxs-lookup"><span data-stu-id="5664d-107">On the item’s item tracking code setup, the **SN Warehouse Tracking** field or the **Lot Warehouse Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="5664d-108">Varen skal bogføres til lageret med en udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="5664d-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="5664d-109">På lokationen skal du aktivere **Kræv pluk**, **Pluk i overensstemmelse med FEFO** og **Tvungen placering**.</span><span class="sxs-lookup"><span data-stu-id="5664d-109">On the location, the **Require Pick**, **Pick According to FEFO**, and **Bin Mandatory** toggles must be turned on.</span></span>  

 <span data-ttu-id="5664d-110">Når alle kriterierne er opfyldt, sorteres serie-/lotnummererede varer, som skal plukkes, med de ældste først i alle pluk og bevægelser, undtagen for varer, der bruger SN-specifik eller lotspecifik sporing.</span><span class="sxs-lookup"><span data-stu-id="5664d-110">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
> <span data-ttu-id="5664d-111">Hvis varer med serie- eller lotnumre bruger specifik sporing, vises disse først, og dernæst vises de resterende, ikke-specifikke serie - eller lotnumre i overensstemmelse med FEFO.</span><span class="sxs-lookup"><span data-stu-id="5664d-111">If some serial or lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>
<br /><br />
<span data-ttu-id="5664d-112">Hvis der er to varer med serie- eller lotnumre, der har samme udløbsdato, vælges varen med det laveste serie- eller lotnummer.</span><span class="sxs-lookup"><span data-stu-id="5664d-112">If two serial or lot-numbered items have the same expiration date, then the application selects the item with the lowest serial or lot number.</span></span>
<br /><br />
<span data-ttu-id="5664d-113">Når du plukker varer med serie- eller lotnumre på lokationer, der er konfigureret til styret læg-på-lager og pluk, er det kun antal på placeringer af typen *Pluk*, der plukkes i overensstemmelse med FEFO.</span><span class="sxs-lookup"><span data-stu-id="5664d-113">When picking serial or lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
<br /><br />
<span data-ttu-id="5664d-114">Hvis du vil aktivere bevægelser i overensstemmelse med FEFO, skal du lade feltet **Fra placeringskode** være tomt på siden **Flytning (lager)** eller **Bevægelseskladde**.</span><span class="sxs-lookup"><span data-stu-id="5664d-114">To enable movements according to FEFO, leave the **From Bin** field empty on the **Inventory Movement** page or the **Movement Worksheet** pages.</span></span>  
<br /><br />
<span data-ttu-id="5664d-115">Hvis feltet **Nøje bogføring af udløbsdato** er markeret på **Varesporingskodekortet**, medtages kun varer, der ikke er udløbet, i plukket, og linjerne sorteres efter FEFO-princippet.</span><span class="sxs-lookup"><span data-stu-id="5664d-115">If the **Strict Expiration Posting** field is selected on the **Item Tracking Code Card**, only items that are not expired will be included in the pick, and the lines are sorted according to the FEFO principle.</span></span>

## <a name="see-also"></a><span data-ttu-id="5664d-116">Se også</span><span class="sxs-lookup"><span data-stu-id="5664d-116">See Also</span></span>  
<span data-ttu-id="5664d-117">[Plukke varer](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="5664d-117">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="5664d-118">[Plukke varer til lagerleverance](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="5664d-118">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="5664d-119">[Plukke varer med Pluk fra lager](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="5664d-119">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="5664d-120">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="5664d-120">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="5664d-121">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="5664d-121">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="5664d-122">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5664d-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]