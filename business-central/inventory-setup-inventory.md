---
title: Opsætning af lagerbeholdning | Microsoft Docs
description: Beskriver, hvordan du konfigurerer lagerbeholdnings- og lagerprocesser, herunder overførselsruter og lokationer, f.eks. lagersteder.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 04/01/2019
ms.author: SorenGP
ms.openlocfilehash: 038e3a9bfdb66a8d714f4f9452f0322623e6ddc4
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238505"
---
# <a name="setting-up-inventory"></a><span data-ttu-id="2d736-103">Opsætning af lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="2d736-103">Setting Up Inventory</span></span>
<span data-ttu-id="2d736-104">Før du kan administrere lageraktiviteter og lageromkostningsberegning, skal du konfigurere de regler og værdier, der definerer virksomhedens lagerpolitikker.</span><span class="sxs-lookup"><span data-stu-id="2d736-104">Before you can manage warehouse activities and inventory costing, you must configure the rules and values that define the company's inventory policies.</span></span>

<span data-ttu-id="2d736-105">Du kan yde bedre kundeservice og optimere forsyningskæden ved at organisere lageret på forskellige adresser.</span><span class="sxs-lookup"><span data-stu-id="2d736-105">You can provide better customer service and optimize your supply chain by organizing your inventory at different addresses.</span></span> <span data-ttu-id="2d736-106">Du kan derefter købe, lagre eller sælger varer på forskellige lokationer og overføre lagerbeholdning mellem dem.</span><span class="sxs-lookup"><span data-stu-id="2d736-106">You can then buy, store, or sell items at different locations and transfer inventory between them.</span></span>

<span data-ttu-id="2d736-107">Når du har oprettet dit lager, kan du administrere forskellige lagerprocesser i relation til varetransaktioner.</span><span class="sxs-lookup"><span data-stu-id="2d736-107">When you have set up your inventory, you can manage various processes related to item transactions.</span></span> <span data-ttu-id="2d736-108">Du kan finde flere oplysninger i [Administrere lager](inventory-manage-inventory.md) og [Logistik](warehouse-manage-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="2d736-108">For more information, see [Manage Inventory](inventory-manage-inventory.md) and [Warehouse Management](warehouse-manage-warehouse.md).</span></span>

| <span data-ttu-id="2d736-109">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="2d736-109">To</span></span> | <span data-ttu-id="2d736-110">Skal du se</span><span class="sxs-lookup"><span data-stu-id="2d736-110">See</span></span> |
| --- | --- |
| <span data-ttu-id="2d736-111">Definere den generelle lageropsætning, f.eks nummerserier, og hvordan du bruger placeringer.</span><span class="sxs-lookup"><span data-stu-id="2d736-111">Define the general inventory setup, such as number series and how to use locations.</span></span> |[<span data-ttu-id="2d736-112">Konfigurere generelle lageroplysninger</span><span class="sxs-lookup"><span data-stu-id="2d736-112">Set Up General Inventory Information</span></span>](inventory-how-setup-general.md) |
|<span data-ttu-id="2d736-113">Konfigurere en effektiv distributionsmodel med en kombination af forskellige lokationer og ansvarscentre, der er knyttet til forretningspartnere eller medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="2d736-113">Configure an efficient distribution model with a combination of different locations and responsibility centers assigned to business partners or employees.</span></span>|[<span data-ttu-id="2d736-114">Arbejde med ansvarscentre</span><span class="sxs-lookup"><span data-stu-id="2d736-114">Work with Responsibility Centers</span></span>](inventory-responsibility-centers.md)|
| <span data-ttu-id="2d736-115">Organisere dit lager på flere lokationer, herunder overflytningsruter.</span><span class="sxs-lookup"><span data-stu-id="2d736-115">Organize your inventory at multiple locations, including transfer routes.</span></span> |[<span data-ttu-id="2d736-116">Opsætte lokationer</span><span class="sxs-lookup"><span data-stu-id="2d736-116">Set Up Locations</span></span>](inventory-how-register-new-items.md) |
| <span data-ttu-id="2d736-117">Opret varekort for lager-, ikke-lager- eller servicevarer, som du handler med.</span><span class="sxs-lookup"><span data-stu-id="2d736-117">Create item cards for inventory, non-inventory, or service items that you trade in.</span></span> |[<span data-ttu-id="2d736-118">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="2d736-118">Register New Items</span></span>](inventory-how-register-new-items.md) |
|<span data-ttu-id="2d736-119">Lære, hvordan du udfylder feltet **Type** på varekort i henhold til forretningsformål.</span><span class="sxs-lookup"><span data-stu-id="2d736-119">Learn how to fill in the **Type** field on item cards according to the business purpose.</span></span>|[<span data-ttu-id="2d736-120">Om varetyper</span><span class="sxs-lookup"><span data-stu-id="2d736-120">About Item Types</span></span>](inventory-about-item-types.md)|
|<span data-ttu-id="2d736-121">Oprette flere enheder for en vare, der kan bruges som alternative vareenheder, f.eks. ved salg, køb eller produktionstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="2d736-121">Set up multiple units of measure for an item that you can use as alternate UOMs, for example on sales, purchasing, or production transactions.</span></span>|[<span data-ttu-id="2d736-122">Oprette vareenheder</span><span class="sxs-lookup"><span data-stu-id="2d736-122">Set Up Item Units of Measure</span></span>](inventory-how-setup-units-of-measure.md)|
|<span data-ttu-id="2d736-123">Som et supplement til varekort kan du registrere oplysninger om dine varer på en bestemt lokation eller af en bestemt variant.</span><span class="sxs-lookup"><span data-stu-id="2d736-123">As a supplement to item cards, record information about your items in a specific location or of a specific variant.</span></span>|[<span data-ttu-id="2d736-124">Opsætte lagervarer</span><span class="sxs-lookup"><span data-stu-id="2d736-124">Set Up Stockkeeping Units</span></span>](inventory-how-to-set-up-stockkeeping-units.md)|
| <span data-ttu-id="2d736-125">Tildel varer til kategorier, og giv dem attributter, der kan hjælpe dig og kunderne med at finde varer.</span><span class="sxs-lookup"><span data-stu-id="2d736-125">Assign items to categories and give them attributes to help you and customers find items.</span></span> |[<span data-ttu-id="2d736-126">Kategorisere varer</span><span class="sxs-lookup"><span data-stu-id="2d736-126">Categorize Items</span></span>](inventory-how-categorize-items.md) |
|<span data-ttu-id="2d736-127">Importér flere varebilleder i én omgang fra en zip-fil, hvor filerne er navngivet efter varenumre.</span><span class="sxs-lookup"><span data-stu-id="2d736-127">Import multiple item pictures in one go from a zip file where the files are named according to item numbers.</span></span>|[<span data-ttu-id="2d736-128">Importér flere varebilleder</span><span class="sxs-lookup"><span data-stu-id="2d736-128">Import Multiple Item Pictures</span></span>](inventory-how-import-item-pictures.md)|

## <a name="see-also"></a><span data-ttu-id="2d736-129">Se også</span><span class="sxs-lookup"><span data-stu-id="2d736-129">See Also</span></span>
[<span data-ttu-id="2d736-130">Administrere lager</span><span class="sxs-lookup"><span data-stu-id="2d736-130">Managing Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="2d736-131">Administrere indkøb</span><span class="sxs-lookup"><span data-stu-id="2d736-131">Managing Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="2d736-132">[Administrere salg](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="2d736-132">[Managing Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="2d736-133">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2d736-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="2d736-134">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="2d736-134">General Business Functionality</span></span>](ui-across-business-areas.md)
