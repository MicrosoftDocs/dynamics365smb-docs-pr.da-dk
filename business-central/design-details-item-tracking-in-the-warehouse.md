---
title: "Designoplysninger – Varesporing i lageret | Microsoft Docs"
description: "Serienummer og lotnummer håndteres primært som lageropgave, så alle indgående og udgående lagerdokumenter har derfor standardfunktioner til at tildele og markere varesporingsnumre. Da reservationssystemet er baseret på vareposter, understøttes lageraktivitetsdokumenter, der kun registrerer lagerposter, dog ikke fuldt ud."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, serial number, lot number, outbound documents
ms.date: 01/15/2019
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 5d6d2d9527e81a92987f6b8fcdbe8e087c3c537a
ms.openlocfilehash: e780dba122374bd80e48ca6bbc74b7540e034ac6
ms.contentlocale: da-dk
ms.lasthandoff: 01/22/2019

---
# <a name="design-details-item-tracking-in-the-warehouse"></a><span data-ttu-id="d8f70-104">Designoplysninger: Varesporing i lageret</span><span class="sxs-lookup"><span data-stu-id="d8f70-104">Design Details: Item Tracking in the Warehouse</span></span>
<span data-ttu-id="d8f70-105">Serienummer og lotnummer håndteres primært som lageropgave, så alle indgående og udgående lagerdokumenter har derfor standardfunktioner til at tildele og markere varesporingsnumre.</span><span class="sxs-lookup"><span data-stu-id="d8f70-105">Serial number and lot number handling is primarily a warehouse task and therefore all inbound and outbound warehouse documents have standard functionality for assigning and selecting item tracking numbers.</span></span>  

<span data-ttu-id="d8f70-106">Da reservationssystemet er baseret på vareposter, understøttes lageraktivitetsdokumenter, der kun registrerer lagerposter, dog ikke fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="d8f70-106">However, because the reservation system is based on item ledger entries, warehouse activity documents that register only warehouse entries are not fully supported.</span></span> <span data-ttu-id="d8f70-107">Da reservationer og varesporingsnumre kun kan håndteres på lokationsniveau, og ikke på placerings- og zoneniveau, kan siden **Varesporingslinjer** ikke åbnes fra lageraktivitetsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="d8f70-107">Because reservations and item tracking numbers can be handled only at the location level, not at the bin and zone level, the **Item Tracking Lines** page cannot be opened from warehouse activity documents.</span></span> <span data-ttu-id="d8f70-108">Det samme gælder for siden **Reservation**.</span><span class="sxs-lookup"><span data-stu-id="d8f70-108">The same applies to the **Reservation** page.</span></span>  

<span data-ttu-id="d8f70-109">Efter et serienummer eller et lotnummer er føjet til en vare på en placering i lageret, kan det frit flyttes og omposteres inden for lageret ved hjælp af en uafhængig varesporingsstruktur, som ikke er relateret til reservationssystemet.</span><span class="sxs-lookup"><span data-stu-id="d8f70-109">After a serial or lot number has been added to an item at a warehouse location, it can be moved and reclassified freely within the warehouse by using an independent item tracking structure that is unrelated to the reservation system.</span></span> <span data-ttu-id="d8f70-110">**Serienr.** og **Lotnr.** er felter med direkte adgang på lagerdokumentlinjer.</span><span class="sxs-lookup"><span data-stu-id="d8f70-110">**Serial No.** and **Lot No.** fields are accessed directly on warehouse document lines.</span></span> <span data-ttu-id="d8f70-111">Når serie- eller lotnummer senere indgår i udgående bogføring, synkroniseres det med reservationssystemet som en del af den almindelige placeringsregulering.</span><span class="sxs-lookup"><span data-stu-id="d8f70-111">When the serial or lot number later partakes in outbound posting, it is synchronized with the reservation system as a part of ordinary bin adjustment.</span></span> <span data-ttu-id="d8f70-112">Du kan finde flere oplysninger i [Designoplysninger: Integration med lager](design-details-integration-with-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="d8f70-112">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="d8f70-113">Dog tager reservationssystemet lageraktiviteter i betragtning ved beregning af tilgængelighed.</span><span class="sxs-lookup"><span data-stu-id="d8f70-113">However, the reservation system does take warehouse activities into consideration when it calculates availability.</span></span> <span data-ttu-id="d8f70-114">Varer, der allokeres til pluk eller registreres som plukket, kan f.eks. ikke reserveres.</span><span class="sxs-lookup"><span data-stu-id="d8f70-114">For example, items that are allocated to picks, or registered as picked, cannot be reserved.</span></span> <span data-ttu-id="d8f70-115">Du kan finde flere oplysninger i [Designoplysninger: Lagertilgængelighed](design-details-availability-in-the-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="d8f70-115">For more information, see [Design Details: Warehouse Availability](design-details-availability-in-the-warehouse.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d8f70-116">Se også</span><span class="sxs-lookup"><span data-stu-id="d8f70-116">See Also</span></span>  
[<span data-ttu-id="d8f70-117">Designoplysninger: Varesporing</span><span class="sxs-lookup"><span data-stu-id="d8f70-117">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)  
[<span data-ttu-id="d8f70-118">Designoplysninger: Integration med lager</span><span class="sxs-lookup"><span data-stu-id="d8f70-118">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)  
[<span data-ttu-id="d8f70-119">Designoplysninger - Lagertilgængelighed</span><span class="sxs-lookup"><span data-stu-id="d8f70-119">Design Details: Warehouse Availability</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="d8f70-120">Designoplysninger: Design af varesporing</span><span class="sxs-lookup"><span data-stu-id="d8f70-120">Design Details: Item Tracking Design</span></span>](design-details-item-tracking-design.md)

