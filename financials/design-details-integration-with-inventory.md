---
title: "Designoplysninger – Integration med lager | Microsoft Docs"
description: "Modulet Logistik og modulet Lager interagerer med hinanden på det fysiske lager og i lager eller logistikregulering."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 00a12f3f2203ed3b22cfee1af6aa8f155ca5fe4b
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-integration-with-inventory"></a><span data-ttu-id="e1adb-103">Designoplysninger: Integration med lager</span><span class="sxs-lookup"><span data-stu-id="e1adb-103">Design Details: Integration with Inventory</span></span>
<span data-ttu-id="e1adb-104">Modulet Logistik og modulet Lager interagerer med hinanden på det fysiske lager og i lager eller logistikregulering.</span><span class="sxs-lookup"><span data-stu-id="e1adb-104">The Warehouse Management application area and the Inventory application area interact with one another in physical inventory and in inventory or warehouse adjustment.</span></span>  
  
## <a name="physical-inventory"></a><span data-ttu-id="e1adb-105">Physical Inventory</span><span class="sxs-lookup"><span data-stu-id="e1adb-105">Physical Inventory</span></span>  
 <span data-ttu-id="e1adb-106">Vinduet **Lagerplacering - opg.kladde** bruges sammen med vinduet **Lageropgørelseskladde** til alle avancerede lagerlokationer.</span><span class="sxs-lookup"><span data-stu-id="e1adb-106">The **Whse. Phys. Inventory Journal** window is used with the **Phys. Inventory Journal** window for all advanced warehouse locations.</span></span> <span data-ttu-id="e1adb-107">Lageret på placeringsniveau er beregnet, og en udskrevet liste leveres for lagermedarbejderen.</span><span class="sxs-lookup"><span data-stu-id="e1adb-107">The inventory on bin level is calculated, and a printed list is provided for the warehouse employee.</span></span> <span data-ttu-id="e1adb-108">Listen viser, hvilke varer der skal tælles på hvilke placeringer.</span><span class="sxs-lookup"><span data-stu-id="e1adb-108">The list shows which items in which bins must be counted.</span></span>  
  
 <span data-ttu-id="e1adb-109">Lagermedarbejderen indtaster det optalte antal i vinduet **Lagerplacering - opg.kladde** og bogfører derefter kladden.</span><span class="sxs-lookup"><span data-stu-id="e1adb-109">The warehouse employee enters the counted quantity in the **Whse. Phys. Inventory Journal** window and then posts the journal.</span></span>  
  
 <span data-ttu-id="e1adb-110">Hvis det optalte antal er større end antallet på kladdelinjen, bogføres en bevægelse for denne forskel fra standardreguleringsplaceringen til den optalte placering.</span><span class="sxs-lookup"><span data-stu-id="e1adb-110">If the counted quantity is greater than the quantity on the journal line, a movement is posted for this difference from the default adjustment bin to the counted bin.</span></span> <span data-ttu-id="e1adb-111">Dette øger antallet på den placering, der er optalt, og reducerer antallet på standardreguleringsplaceringen.</span><span class="sxs-lookup"><span data-stu-id="e1adb-111">This increases the quantity in the counted bin and decreases the quantity in the default adjustment bin.</span></span>  
  
 <span data-ttu-id="e1adb-112">Hvis det optalte antal er mindre end antallet på kladdelinjen, bogføres en bevægelse for denne forskel fra den optalte placering til standardreguleringsplaceringen.</span><span class="sxs-lookup"><span data-stu-id="e1adb-112">If the quantity counted is less than the quantity on the journal line, a movement for this difference is posted from the counted bin to the default adjustment bin.</span></span> <span data-ttu-id="e1adb-113">Dette reducerer antallet på den placering, der er optalt, og øger antallet på standardreguleringsplaceringen.</span><span class="sxs-lookup"><span data-stu-id="e1adb-113">This decreases the quantity in the counted bin and increases the quantity in the default adjustment bin.</span></span>  
  
 <span data-ttu-id="e1adb-114">I avancerede lageropsætninger bliver værdien i feltet **Antal (beregnet)** hentet fra vareposter, og værdien i feltet **Antal (optalt)** er hentet fra lagerposter, bortset fra justeringen af placeringsindholdet.</span><span class="sxs-lookup"><span data-stu-id="e1adb-114">In advanced warehouse configurations, the value in the **Quantity (Calculated)** field is retrieved from item ledger entries and the value in the **Quantity (Phys. Inventory)** field is retrieved from warehouse entries, excluding the adjustment bin content.</span></span> <span data-ttu-id="e1adb-115">Feltet **Antal** angiver forskellen mellem de to første felter, som skal være lig med indholdet af reguleringsplaceringen.</span><span class="sxs-lookup"><span data-stu-id="e1adb-115">The **Quantity** field specifies the difference between the first two fields, which should be equal to the contents of the adjustment bin.</span></span>  
  
 <span data-ttu-id="e1adb-116">Når du bogfører lageropgørelseskladde, opdateres lageret og standardreguleringsplaceringen.</span><span class="sxs-lookup"><span data-stu-id="e1adb-116">When you post the physical inventory journal, the inventory and the default adjustment bin are updated.</span></span>  
  
### <a name="warehouse-adjustments-to-the-item-ledger"></a><span data-ttu-id="e1adb-117">Lagerreguleringer til vareposten</span><span class="sxs-lookup"><span data-stu-id="e1adb-117">Warehouse Adjustments to the Item Ledger</span></span>  
 <span data-ttu-id="e1adb-118">Du kan bruge vinduet **Varekladde** og funktionen **Beregn regulering (logistik)** til at regulere beholdningen på vareposten i henhold til den regulering, der er foretaget i vareantallet på en lagerplacering.</span><span class="sxs-lookup"><span data-stu-id="e1adb-118">You use the **Item Journal** window and the **Calculate Whse. Adjustment** function to adjust inventory on the item ledger in accordance with an adjustment that has been made to the item quantity in a warehouse bin.</span></span> <span data-ttu-id="e1adb-119">Hvis du vil oprette en tilknytning mellem lageret og lagerstedet, skal du definere en standardreguleringsplacering pr. lokation.</span><span class="sxs-lookup"><span data-stu-id="e1adb-119">To create a link between the inventory and the warehouse, you must define a default adjustment bin per location.</span></span>  
  
 <span data-ttu-id="e1adb-120">Reguleringsplaceringens standard registrerer varer på lageret, når du bogfører en forøgelse af lageret.</span><span class="sxs-lookup"><span data-stu-id="e1adb-120">The default adjustment bin registers items in the warehouse when you post an increase for the inventory.</span></span> <span data-ttu-id="e1adb-121">Men hvis du bogfører en reducering, reduceres antallet på standardplaceringen også.</span><span class="sxs-lookup"><span data-stu-id="e1adb-121">However, if you post a decrease, the quantity on the default bin is also decreased.</span></span> <span data-ttu-id="e1adb-122">I begge tilfælde oprettes vareposter og lagerposter.</span><span class="sxs-lookup"><span data-stu-id="e1adb-122">In both cases, item ledger entries and warehouse entries are created.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="e1adb-123">Reguleringsplaceringen er ikke inkluderet i disponeringsberegningen.</span><span class="sxs-lookup"><span data-stu-id="e1adb-123">The adjustment bin is not included in the availability calculation.</span></span>  
  
 <span data-ttu-id="e1adb-124">Hvis du vil justere placeringsindholdet, kan du bruge lagerkladden, hvorfra du kan angive det varenummer, den zonekode, den placeringskode og det antal, du vil justere.</span><span class="sxs-lookup"><span data-stu-id="e1adb-124">If you want to adjust the bin content, you can use the warehouse item journal, from which you can enter the item number, zone code, bin code, and quantity that you want to adjust.</span></span>  
  
 <span data-ttu-id="e1adb-125">Hvis du angiver et positivt antal og bogfører linjen, øges det lager, der opbevares på placeringen, og antallet på reguleringsplaceringens standard reduceres tilsvarende.</span><span class="sxs-lookup"><span data-stu-id="e1adb-125">If you enter a positive quantity and post the line, then the inventory stored in the bin increases, and the quantity of the default adjustment bin decreases correspondingly.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e1adb-126">Se også</span><span class="sxs-lookup"><span data-stu-id="e1adb-126">See Also</span></span>  
 <span data-ttu-id="e1adb-127">[Designoplysninger: Logistik](design-details-warehouse-management.md) </span><span class="sxs-lookup"><span data-stu-id="e1adb-127">[Design Details: Warehouse Management](design-details-warehouse-management.md) </span></span>  
 [<span data-ttu-id="e1adb-128">Designoplysninger: Tilgængelighed i lageret</span><span class="sxs-lookup"><span data-stu-id="e1adb-128">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)
