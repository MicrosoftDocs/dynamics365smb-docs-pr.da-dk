---
title: Lageraktiviteter | Microsoft Docs
description: "Når varer er modtaget, og før varerne afsendes, finder der en serie interne lageraktiviteter sted for at sikre et effektivt forløb gennem lagerstedet og for at organisere og vedligeholde virksomhedens lagerbeholdninger."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: ddc2e9bdf131a68fb5ea280011971b8a8f7220f0
ms.contentlocale: da-dk
ms.lasthandoff: 06/28/2018

---
# <a name="warehouse-management"></a><span data-ttu-id="1eef7-103">Logistik</span><span class="sxs-lookup"><span data-stu-id="1eef7-103">Warehouse Management</span></span>
<span data-ttu-id="1eef7-104">Når varer er modtaget, og før varerne afsendes, finder der en serie interne lageraktiviteter sted for at sikre et effektivt forløb gennem lagerstedet og for at organisere og vedligeholde virksomhedens lagerbeholdninger.</span><span class="sxs-lookup"><span data-stu-id="1eef7-104">After goods are received and before goods are shipped, a series of internal warehouse activities take place to ensure an effective flow through the warehouse and to organize and maintain company inventories.</span></span>

<span data-ttu-id="1eef7-105">Blandt typiske lageraktiviteter er at lægge varer på lager, flytte varer til eller mellem lagersteder og plukke varer til montage, produktion eller afsendelse.</span><span class="sxs-lookup"><span data-stu-id="1eef7-105">Typical warehouse activities include putting items away, moving items inside or between warehouses, and picking items for assembly, production, or shipment.</span></span> <span data-ttu-id="1eef7-106">Montageelementer til salg eller lager kan også betragtes som lageraktiviteter, men de beskrives andre steder.</span><span class="sxs-lookup"><span data-stu-id="1eef7-106">Assembling items for sale or inventory may also be considered warehouse activities, but these are covered elsewhere.</span></span> <span data-ttu-id="1eef7-107">Du kan finde flere oplysninger i [Montagestyring](assembly-assemble-items.md).</span><span class="sxs-lookup"><span data-stu-id="1eef7-107">For more information, see [Assembly Management](assembly-assemble-items.md).</span></span>  

<span data-ttu-id="1eef7-108">På store lagre kan de forskellige håndteringsopgaver opdeles efter afdelinger, og integrationen håndteres af en styret arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="1eef7-108">In large warehouses, these different handling tasks can be separated by departments and the integration managed by a directed workflow.</span></span> <span data-ttu-id="1eef7-109">I simplere installationer er arbejdsgangen mindre formaliseret, og lageraktiviteterne udføres via de såkaldte læg-på-lager og lagerpluk.</span><span class="sxs-lookup"><span data-stu-id="1eef7-109">In simpler installations, the flow is less formalized and the warehouse activities are performed with so-called inventory put-aways and inventory picks.</span></span> <span data-ttu-id="1eef7-110">Du kan finde flere oplysninger om de grundlæggende kontra avancerede lageropsætninger i [Designoplysninger: Oversigt over logistik](design-details-warehouse-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1eef7-110">For more information about basic versus advanced warehouse configurations, see [Design Details: Warehouse Overview](design-details-warehouse-overview.md).</span></span>

<span data-ttu-id="1eef7-111">Før du kan udføre lageraktiviteter, skal du konfigurere systemet til den relevante lagerbehandlingskompleksitet.</span><span class="sxs-lookup"><span data-stu-id="1eef7-111">Before you can perform warehouse activities, you must set the system up for the relevant complexity of warehouse processing.</span></span> <span data-ttu-id="1eef7-112">Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="1eef7-112">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

 <span data-ttu-id="1eef7-113">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="1eef7-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="1eef7-114">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="1eef7-114">**To**</span></span>|<span data-ttu-id="1eef7-115">**Se**</span><span class="sxs-lookup"><span data-stu-id="1eef7-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="1eef7-116">Registrere modtagelsen af varer på lagerlokationer, enten med en købsordre, i enkle lokationsopsætninger eller med en lagermodtagelse, i tilfælde af halvt eller fuldt automatiseret lagerbehandling på lokationen.</span><span class="sxs-lookup"><span data-stu-id="1eef7-116">Record the receipt of items at warehouse locations, either with a purchase order only, in simple location setups, or with a warehouse receipt, in case of semi or fully automated warehouse processing at the location.</span></span>|[<span data-ttu-id="1eef7-117">Modtage varer</span><span class="sxs-lookup"><span data-stu-id="1eef7-117">Receive Items</span></span>](warehouse-how-receive-items.md)|
|<span data-ttu-id="1eef7-118">Spring læg-på-lager- og plukprocesserne over for at fremskynde en vare direkte fra modtagelse eller produktion til levering.</span><span class="sxs-lookup"><span data-stu-id="1eef7-118">Bypass the put-away and pick processes to expedite an item straight from receiving or production to shipping.</span></span>|[<span data-ttu-id="1eef7-119">Afsende varer direkte</span><span class="sxs-lookup"><span data-stu-id="1eef7-119">Cross-Dock Items</span></span>](warehouse-how-to-cross-dock-items.md)|    
|<span data-ttu-id="1eef7-120">Lægge varer på lager, der er modtaget fra køb, salgsreturvarer, overflytninger eller produktionsafgange, i henhold til den konfigurerede lagerproces.</span><span class="sxs-lookup"><span data-stu-id="1eef7-120">Put away items received from purchases, sales returns, transfers, or production output according to the configured warehouse process.</span></span>|[<span data-ttu-id="1eef7-121">Lægge varer på lager</span><span class="sxs-lookup"><span data-stu-id="1eef7-121">Putting Items Away</span></span>](warehouse-put-away-items.md)|
|<span data-ttu-id="1eef7-122">Flytte varer mellem placeringer på lageret.</span><span class="sxs-lookup"><span data-stu-id="1eef7-122">Move items between bins in the warehouse.</span></span>|[<span data-ttu-id="1eef7-123">Flytte varer</span><span class="sxs-lookup"><span data-stu-id="1eef7-123">Moving Items</span></span>](warehouse-move-items.md)|
|<span data-ttu-id="1eef7-124">Plukke varer der skal afsendes, overflyttes eller forbruges i montage eller produktionen, i henhold til den konfigurerede lagerproces.</span><span class="sxs-lookup"><span data-stu-id="1eef7-124">Pick items to be shipped, transferred, or consumed in assembly or production, according to the configured warehouse process.</span></span>|[<span data-ttu-id="1eef7-125">Plukke varer</span><span class="sxs-lookup"><span data-stu-id="1eef7-125">Picking Items</span></span>](warehouse-pick-items.md)|
|<span data-ttu-id="1eef7-126">Registrere leveringen af varer fra lagerlokationer, enten med en salgsordre, i enkle lokationsopsætninger eller med en lagerleverance, i tilfælde af halvt eller fuldt automatiserede lagerprocesser på lokationen.</span><span class="sxs-lookup"><span data-stu-id="1eef7-126">Record the shipment of items from warehouse locations, either with a sales order only, in simple location setups, or with a warehouse shipment, in case of semi or fully automated warehouse processes at the location.</span></span>|[<span data-ttu-id="1eef7-127">Afsende varer</span><span class="sxs-lookup"><span data-stu-id="1eef7-127">Ship Items</span></span>](warehouse-how-ship-items.md)|  

## <a name="see-also"></a><span data-ttu-id="1eef7-128">Se også</span><span class="sxs-lookup"><span data-stu-id="1eef7-128">See Also</span></span>  
[<span data-ttu-id="1eef7-129">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="1eef7-129">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="1eef7-130">[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="1eef7-130">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="1eef7-131">[Montagestyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="1eef7-131">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="1eef7-132">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="1eef7-132">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="1eef7-133">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1eef7-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

