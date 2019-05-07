---
title: Designoplysninger – Varesporing i lageret | Microsoft Docs
description: Serienummer og lotnummer håndteres primært som lageropgave, så alle indgående og udgående lagerdokumenter har derfor standardfunktioner til at tildele og markere varesporingsnumre. Da reservationssystemet er baseret på vareposter, understøttes lageraktivitetsdokumenter, der kun registrerer lagerposter, dog ikke fuldt ud.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, serial number, lot number, outbound documents
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a482e0fed80d5e9380b6c6e0ec03557abbc02953
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "917812"
---
# <a name="design-details-item-tracking-in-the-warehouse"></a><span data-ttu-id="8c0f7-104">Designoplysninger: Varesporing i lageret</span><span class="sxs-lookup"><span data-stu-id="8c0f7-104">Design Details: Item Tracking in the Warehouse</span></span>
<span data-ttu-id="8c0f7-105">Serienummer og lotnummer håndteres primært som lageropgave, så alle indgående og udgående lagerdokumenter har derfor standardfunktioner til at tildele og markere varesporingsnumre.</span><span class="sxs-lookup"><span data-stu-id="8c0f7-105">Serial number and lot number handling is primarily a warehouse task and therefore all inbound and outbound warehouse documents have standard functionality for assigning and selecting item tracking numbers.</span></span>  

<span data-ttu-id="8c0f7-106">Da reservationssystemet er baseret på vareposter, understøttes lageraktivitetsdokumenter, der kun registrerer lagerposter, dog ikke fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="8c0f7-106">However, because the reservation system is based on item ledger entries, warehouse activity documents that register only warehouse entries are not fully supported.</span></span> <span data-ttu-id="8c0f7-107">Da reservationer og varesporingsnumre kun kan håndteres på lokationsniveau, og ikke på placerings- og zoneniveau, kan siden **Varesporingslinjer** ikke åbnes fra lageraktivitetsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="8c0f7-107">Because reservations and item tracking numbers can be handled only at the location level, not at the bin and zone level, the **Item Tracking Lines** page cannot be opened from warehouse activity documents.</span></span> <span data-ttu-id="8c0f7-108">Det samme gælder for siden **Reservation**.</span><span class="sxs-lookup"><span data-stu-id="8c0f7-108">The same applies to the **Reservation** page.</span></span>  

<span data-ttu-id="8c0f7-109">Efter et serienummer eller et lotnummer er føjet til en vare på en placering i lageret, kan det frit flyttes og omposteres inden for lageret ved hjælp af en uafhængig varesporingsstruktur, som ikke er relateret til reservationssystemet.</span><span class="sxs-lookup"><span data-stu-id="8c0f7-109">After a serial or lot number has been added to an item at a warehouse location, it can be moved and reclassified freely within the warehouse by using an independent item tracking structure that is unrelated to the reservation system.</span></span> <span data-ttu-id="8c0f7-110">**Serienr.** og **Lotnr.** er felter med direkte adgang på lagerdokumentlinjer.</span><span class="sxs-lookup"><span data-stu-id="8c0f7-110">**Serial No.** and **Lot No.** fields are accessed directly on warehouse document lines.</span></span> <span data-ttu-id="8c0f7-111">Når serie- eller lotnummer senere indgår i udgående bogføring, synkroniseres det med reservationssystemet som en del af den almindelige placeringsregulering.</span><span class="sxs-lookup"><span data-stu-id="8c0f7-111">When the serial or lot number later partakes in outbound posting, it is synchronized with the reservation system as a part of ordinary bin adjustment.</span></span> <span data-ttu-id="8c0f7-112">Du kan finde flere oplysninger i [Designoplysninger: Integration med lager](design-details-integration-with-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="8c0f7-112">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="8c0f7-113">Dog tager reservationssystemet lageraktiviteter i betragtning ved beregning af tilgængelighed.</span><span class="sxs-lookup"><span data-stu-id="8c0f7-113">However, the reservation system does take warehouse activities into consideration when it calculates availability.</span></span> <span data-ttu-id="8c0f7-114">Varer, der allokeres til pluk eller registreres som plukket, kan f.eks. ikke reserveres.</span><span class="sxs-lookup"><span data-stu-id="8c0f7-114">For example, items that are allocated to picks, or registered as picked, cannot be reserved.</span></span> <span data-ttu-id="8c0f7-115">Du kan finde flere oplysninger i [Designoplysninger: Lagertilgængelighed](design-details-availability-in-the-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="8c0f7-115">For more information, see [Design Details: Warehouse Availability](design-details-availability-in-the-warehouse.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8c0f7-116">Se også</span><span class="sxs-lookup"><span data-stu-id="8c0f7-116">See Also</span></span>  
[<span data-ttu-id="8c0f7-117">Designoplysninger: Varesporing</span><span class="sxs-lookup"><span data-stu-id="8c0f7-117">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)  
[<span data-ttu-id="8c0f7-118">Designoplysninger: Integration med lager</span><span class="sxs-lookup"><span data-stu-id="8c0f7-118">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)  
[<span data-ttu-id="8c0f7-119">Designoplysninger - Lagertilgængelighed</span><span class="sxs-lookup"><span data-stu-id="8c0f7-119">Design Details: Warehouse Availability</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="8c0f7-120">Designoplysninger: Design af varesporing</span><span class="sxs-lookup"><span data-stu-id="8c0f7-120">Design Details: Item Tracking Design</span></span>](design-details-item-tracking-design.md)
