---
title: Lageraktiviteter | Microsoft Docs
description: "Når varer er modtaget, og før varerne afsendes, finder der en serie interne lageraktiviteter sted for at sikre et effektivt forløb gennem lagerstedet og for at organisere og vedligeholde virksomhedens lagerbeholdninger."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c1ea1c4a5ea4b917243d60981ec35050895f82a7
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="warehouse-management"></a><span data-ttu-id="16bba-103">Logistik</span><span class="sxs-lookup"><span data-stu-id="16bba-103">Warehouse Management</span></span>
<span data-ttu-id="16bba-104">Når varer er modtaget, og før varerne afsendes, finder der en serie interne lageraktiviteter sted for at sikre et effektivt forløb gennem lagerstedet og for at organisere og vedligeholde virksomhedens lagerbeholdninger.</span><span class="sxs-lookup"><span data-stu-id="16bba-104">After goods are received and before goods are shipped, a series of internal warehouse activities take place to ensure an effective flow through the warehouse and to organize and maintain company inventories.</span></span>

<span data-ttu-id="16bba-105">Blandt typiske lageraktiviteter er at lægge varer på lager, flytte varer til eller mellem lagersteder og plukke varer til montage, produktion eller afsendelse.</span><span class="sxs-lookup"><span data-stu-id="16bba-105">Typical warehouse activities include putting items away, moving items inside or between warehouses, and picking items for assembly, production, or shipment.</span></span> <span data-ttu-id="16bba-106">Montageelementer til salg eller lager kan også betragtes som lageraktiviteter, men de beskrives andre steder.</span><span class="sxs-lookup"><span data-stu-id="16bba-106">Assembling items for sale or inventory may also be considered warehouse activities, but these are covered elsewhere.</span></span> <span data-ttu-id="16bba-107">Du kan finde flere oplysninger i [Montagestyring](assembly-assemble-items.md).</span><span class="sxs-lookup"><span data-stu-id="16bba-107">For more information, see [Assembly Management](assembly-assemble-items.md).</span></span>  

<span data-ttu-id="16bba-108">På store lagre kan de forskellige håndteringsopgaver opdeles efter afdelinger, og integrationen håndteres af en styret arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="16bba-108">In large warehouses, these different handling tasks can be separated by departments and the integration managed by a directed workflow.</span></span> <span data-ttu-id="16bba-109">I simplere installationer er arbejdsgangen mindre formaliseret, og lageraktiviteterne udføres via de såkaldte læg-på-lager og lagerpluk.</span><span class="sxs-lookup"><span data-stu-id="16bba-109">In simpler installations, the flow is less formalized and the warehouse activities are performed with so-called inventory put-aways and inventory picks.</span></span> <span data-ttu-id="16bba-110">Du kan finde flere oplysninger om de grundlæggende kontra avancerede lageropsætninger i [Designoplysninger: Oversigt over logistik](design-details-warehouse-overview.md).</span><span class="sxs-lookup"><span data-stu-id="16bba-110">For more information about basic versus advanced warehouse configurations, see [Design Details: Warehouse Overview](design-details-warehouse-overview.md).</span></span>

<span data-ttu-id="16bba-111">Før du kan udføre lageraktiviteter, skal du konfigurere systemet til den relevante lagerbehandlingskompleksitet.</span><span class="sxs-lookup"><span data-stu-id="16bba-111">Before you can perform warehouse activities, you must set the system up for the relevant complexity of warehouse processing.</span></span> <span data-ttu-id="16bba-112">Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="16bba-112">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

 <span data-ttu-id="16bba-113">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="16bba-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="16bba-114">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="16bba-114">**To**</span></span>|<span data-ttu-id="16bba-115">**Se**</span><span class="sxs-lookup"><span data-stu-id="16bba-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="16bba-116">Registrere modtagelsen af varer på lagerlokationer, enten med en købsordre, i enkle lokationsopsætninger eller med en lagermodtagelse, i tilfælde af halvt eller fuldt automatiseret lagerbehandling på lokationen.</span><span class="sxs-lookup"><span data-stu-id="16bba-116">Record the receipt of items at warehouse locations, either with a purchase order only, in simple location setups, or with a warehouse receipt, in case of semi or fully automated warehouse processing at the location.</span></span>|[<span data-ttu-id="16bba-117">Sådan modtages varer</span><span class="sxs-lookup"><span data-stu-id="16bba-117">How to: Receive Items</span></span>](warehouse-how-receive-items.md)|
|<span data-ttu-id="16bba-118">Spring læg-på-lager- og plukprocesserne over for at fremskynde en vare direkte fra modtagelse eller produktion til levering.</span><span class="sxs-lookup"><span data-stu-id="16bba-118">Bypass the put-away and pick processes to expedite an item straight from receiving or production to shipping.</span></span>|[<span data-ttu-id="16bba-119">Fremgangsmåde: Afsendelse</span><span class="sxs-lookup"><span data-stu-id="16bba-119">How to: Cross-Dock Items</span></span>](warehouse-how-to-cross-dock-items.md)|    
|<span data-ttu-id="16bba-120">Lægge varer på lager, der er modtaget fra køb, salgsreturvarer, overflytninger eller produktionsafgange, i henhold til den konfigurerede lagerproces.</span><span class="sxs-lookup"><span data-stu-id="16bba-120">Put away items received from purchases, sales returns, transfers, or production output according to the configured warehouse process.</span></span>|[<span data-ttu-id="16bba-121">Lægge varer på lager</span><span class="sxs-lookup"><span data-stu-id="16bba-121">Putting Items Away</span></span>](warehouse-put-away-items.md)|
|<span data-ttu-id="16bba-122">Flytte varer mellem placeringer på lageret.</span><span class="sxs-lookup"><span data-stu-id="16bba-122">Move items between bins in the warehouse.</span></span>|[<span data-ttu-id="16bba-123">Flytte varer</span><span class="sxs-lookup"><span data-stu-id="16bba-123">Moving Items</span></span>](warehouse-move-items.md)|
|<span data-ttu-id="16bba-124">Plukke varer der skal afsendes, overflyttes eller forbruges i montage eller produktionen, i henhold til den konfigurerede lagerproces.</span><span class="sxs-lookup"><span data-stu-id="16bba-124">Pick items to be shipped, transferred, or consumed in assembly or production, according to the configured warehouse process.</span></span>|[<span data-ttu-id="16bba-125">Plukke varer</span><span class="sxs-lookup"><span data-stu-id="16bba-125">Picking Items</span></span>](warehouse-pick-items.md)|
|<span data-ttu-id="16bba-126">Registrere leveringen af varer fra lagerlokationer, enten med en salgsordre, i enkle lokationsopsætninger eller med en lagerleverance, i tilfælde af halvt eller fuldt automatiserede lagerprocesser på lokationen.</span><span class="sxs-lookup"><span data-stu-id="16bba-126">Record the shipment of items from warehouse locations, either with a sales order only, in simple location setups, or with a warehouse shipment, in case of semi or fully automated warehouse processes at the location.</span></span>|[<span data-ttu-id="16bba-127">Fremgangsmåde: Sende varer</span><span class="sxs-lookup"><span data-stu-id="16bba-127">How to: Ship Items</span></span>](warehouse-how-ship-items.md)|  

## <a name="see-also"></a><span data-ttu-id="16bba-128">Se også</span><span class="sxs-lookup"><span data-stu-id="16bba-128">See Also</span></span>  
 [<span data-ttu-id="16bba-129">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="16bba-129">Inventory</span></span>](inventory-manage-inventory.md)  
 <span data-ttu-id="16bba-130">[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="16bba-130">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
 <span data-ttu-id="16bba-131">[Montagestyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="16bba-131">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="16bba-132">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="16bba-132">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
 <span data-ttu-id="16bba-133">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="16bba-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

