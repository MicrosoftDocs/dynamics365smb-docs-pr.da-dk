---
title: "Opsætning af lagerbeholdning | Microsoft Docs"
description: "Beskriver, hvordan du konfigurerer lagerbeholdnings- og lagerprocesser, herunder overførselsruter og lokationer, f.eks. lagersteder."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 09/08/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 022cd32a11546913e74aeccdd74772e6e01755d3
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-inventory"></a><span data-ttu-id="81e3b-103">Opsætning af lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="81e3b-103">Setting Up Inventory</span></span>
<span data-ttu-id="81e3b-104">Før du kan administrere lageraktiviteter og lageromkostningsberegning, skal du konfigurere de regler og værdier, der definerer virksomhedens lagerpolitikker.</span><span class="sxs-lookup"><span data-stu-id="81e3b-104">Before you can manage warehouse activities and inventory costing, you must configure the rules and values that define the company's inventory policies.</span></span>

<span data-ttu-id="81e3b-105">Du kan yde bedre kundeservice og optimere forsyningskæden ved at organisere lageret på forskellige adresser.</span><span class="sxs-lookup"><span data-stu-id="81e3b-105">You can provide better customer service and optimize your supply chain by organizing your inventory at different addresses.</span></span> <span data-ttu-id="81e3b-106">Du kan derefter købe, lagre eller sælger varer på forskellige lokationer og overføre lagerbeholdning mellem dem.</span><span class="sxs-lookup"><span data-stu-id="81e3b-106">You can then buy, store, or sell items at different locations and transfer inventory between them.</span></span>

<span data-ttu-id="81e3b-107">Når du har oprettet dit lager, kan du administrere forskellige lagerprocesser i relation til varetransaktioner.</span><span class="sxs-lookup"><span data-stu-id="81e3b-107">When you have set up your inventory, you can manage various processes related to item transactions.</span></span> <span data-ttu-id="81e3b-108">Du kan finde flere oplysninger i [Administrere lager](inventory-manage-inventory.md) og [Logistik](warehouse-manage-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="81e3b-108">For more information, see [Manage Inventory](inventory-manage-inventory.md) and [Warehouse Management](warehouse-manage-warehouse.md).</span></span>

| <span data-ttu-id="81e3b-109">Til</span><span class="sxs-lookup"><span data-stu-id="81e3b-109">To</span></span> | <span data-ttu-id="81e3b-110">Se</span><span class="sxs-lookup"><span data-stu-id="81e3b-110">See</span></span> |
| --- | --- |
| <span data-ttu-id="81e3b-111">Definere den generelle lageropsætning, f.eks nummerserier, og hvordan du bruger placeringer.</span><span class="sxs-lookup"><span data-stu-id="81e3b-111">Define the general inventory setup, such as number series and how to use locations.</span></span> |[<span data-ttu-id="81e3b-112">Fremgangsmåde: Opsætning af generelle lageroplysninger</span><span class="sxs-lookup"><span data-stu-id="81e3b-112">How to: Set Up General Inventory Information</span></span>](inventory-how-setup-general.md) |
|<span data-ttu-id="81e3b-113">Konfigurere en effektiv distributionsmodel med en kombination af forskellige lokationer og ansvarscentre, der er knyttet til forretningspartnere eller medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="81e3b-113">Configure an efficient distribution model with a combination of different locations and responsibility centers assigned to business partners or employees.</span></span>|[<span data-ttu-id="81e3b-114">Fremgangsmåde: Arbejde med ansvarscentre</span><span class="sxs-lookup"><span data-stu-id="81e3b-114">How to: Work with Responsibility Centers</span></span>](inventory-responsibility-centers.md)|
| <span data-ttu-id="81e3b-115">Organisere dit lager på flere lokationer, herunder overflytningsruter.</span><span class="sxs-lookup"><span data-stu-id="81e3b-115">Organize your inventory at multiple locations, including transfer routes.</span></span> |[<span data-ttu-id="81e3b-116">Sådan oprettes lokationer</span><span class="sxs-lookup"><span data-stu-id="81e3b-116">How to: Set Up Locations</span></span>](inventory-how-register-new-items.md) |
| <span data-ttu-id="81e3b-117">Opret varekort for lagervarer, som du handler med.</span><span class="sxs-lookup"><span data-stu-id="81e3b-117">Create item cards for inventory items that you trade in.</span></span> |[<span data-ttu-id="81e3b-118">Fremgangsmåde: Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="81e3b-118">How to: Register New Items</span></span>](inventory-how-register-new-items.md) |
|<span data-ttu-id="81e3b-119">Som et supplement til varekort kan du registrere oplysninger om dine varer på en bestemt lokation eller af en bestemt variant.</span><span class="sxs-lookup"><span data-stu-id="81e3b-119">As a supplement to item cards, record information about your items in a specific location or of a specific variant.</span></span>|[<span data-ttu-id="81e3b-120">Sådan oprettes lagervarer</span><span class="sxs-lookup"><span data-stu-id="81e3b-120">How to: Set Up Stockkeeping Units</span></span>](inventory-how-to-set-up-stockkeeping-units.md)|
| <span data-ttu-id="81e3b-121">Tildel varer til kategorier, og giv dem attributter, der kan hjælpe dig og kunderne med at finde varer.</span><span class="sxs-lookup"><span data-stu-id="81e3b-121">Assign items to categories and give them attributes to help you and customers find items.</span></span> |[<span data-ttu-id="81e3b-122">Fremgangsmåde: Kategorisere varer</span><span class="sxs-lookup"><span data-stu-id="81e3b-122">How to: Categorize Items</span></span>](inventory-how-categorize-items.md) |

## <a name="see-also"></a><span data-ttu-id="81e3b-123">Se også</span><span class="sxs-lookup"><span data-stu-id="81e3b-123">See Also</span></span>
[<span data-ttu-id="81e3b-124">Administrere lager</span><span class="sxs-lookup"><span data-stu-id="81e3b-124">Managing Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="81e3b-125">Administrere indkøb</span><span class="sxs-lookup"><span data-stu-id="81e3b-125">Managing Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="81e3b-126">[Administrere salg](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="81e3b-126">[Managing Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="81e3b-127">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="81e3b-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="81e3b-128">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="81e3b-128">General Business Functionality</span></span>](ui-across-business-areas.md)

