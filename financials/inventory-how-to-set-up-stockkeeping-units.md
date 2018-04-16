---
title: "Sådan oprettes lagervarer | Microsoft Docs"
description: "Du kan bruge lagervarer til at registrere oplysninger om dine varer på en bestemt lokation eller med en bestemt variantkode."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: aa25b3b809b27160f1493408fc8f61f14b651b67
ms.contentlocale: da-dk
ms.lasthandoff: 04/16/2018

---
# <a name="set-up-stockkeeping-units"></a><span data-ttu-id="7b021-103">Opsætte lagervarer</span><span class="sxs-lookup"><span data-stu-id="7b021-103">Set Up Stockkeeping Units</span></span>
<span data-ttu-id="7b021-104">Du kan bruge lagervarer til at registrere oplysninger om dine varer på en bestemt lokation eller med en bestemt variantkode.</span><span class="sxs-lookup"><span data-stu-id="7b021-104">You can use stockkeeping units to record information about your items for a specific location or a specific variant code.</span></span>  

 <span data-ttu-id="7b021-105">Lagervarer er et supplement til varekortene.</span><span class="sxs-lookup"><span data-stu-id="7b021-105">Stockkeeping units are a supplement to item cards.</span></span> <span data-ttu-id="7b021-106">De erstatter dem ikke, selvom de er relateret til dem.</span><span class="sxs-lookup"><span data-stu-id="7b021-106">They do not replace them, although they are related to them.</span></span> <span data-ttu-id="7b021-107">Med lagervarer kan du udskille oplysningerne om den samme vare, så de kun vedrører en bestemt lokation, f.eks. et lager eller distributionscenter, eller en bestemt variant, f.eks. forskellige hyldenumre og forskellige genbestillingsdata.</span><span class="sxs-lookup"><span data-stu-id="7b021-107">Stockkeeping units allow you to differentiate information about an item for a specific location, such as a warehouse or distribution center, or a specific variant, such as different shelf numbers and different replenishment information, for the same item.</span></span>  

## <a name="to-set-up-a-stockkeeping-unit"></a><span data-ttu-id="7b021-108">Sådan opsættes en lagervare</span><span class="sxs-lookup"><span data-stu-id="7b021-108">To set up a stockkeeping unit</span></span>  

1. <span data-ttu-id="7b021-109">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lagervarer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="7b021-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Stockkeeping Units**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7b021-110">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7b021-110">Choose the **New** action.</span></span>  
3. <span data-ttu-id="7b021-111">Udfyld felterne på kortet.</span><span class="sxs-lookup"><span data-stu-id="7b021-111">Fill in the fields on the card.</span></span> <span data-ttu-id="7b021-112">Følgende felter er obligatoriske: **Varenr.**, **Lokationskode** og/eller **Variantkode**.</span><span class="sxs-lookup"><span data-stu-id="7b021-112">The following fields are required: **Item No.**, **Location Code**, and/or **Variant Code**.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

<span data-ttu-id="7b021-113">Når du har angivet den første lagervare, bliver afkrydsningsfeltet **Lagervare findes** automatisk markeret på **Vare**-kortet.</span><span class="sxs-lookup"><span data-stu-id="7b021-113">When you have set up the first stockkeeping unit for an item, the **Stockkeeping Unit Exists** check box on the **Item** card is selected.</span></span>  

<span data-ttu-id="7b021-114">Brug kørslen **Opret lagervare**, hvis du vil oprette flere lagerførte varer.</span><span class="sxs-lookup"><span data-stu-id="7b021-114">To create several stockkeeping units for an item, use the **Create Stockkeeping Unit** batch job.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="7b021-115">Oplysningerne på **lagervarekortet** tilsidesætter oplysningerne på **varekortet**.</span><span class="sxs-lookup"><span data-stu-id="7b021-115">The information on the **Stockkeeping Unit** card has priority over the **Item** card.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7b021-116">Se også</span><span class="sxs-lookup"><span data-stu-id="7b021-116">See Also</span></span>  
[<span data-ttu-id="7b021-117">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="7b021-117">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="7b021-118">Sådan konfigureres logistikfunktioner</span><span class="sxs-lookup"><span data-stu-id="7b021-118">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="7b021-119">Logistik</span><span class="sxs-lookup"><span data-stu-id="7b021-119">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="7b021-120">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="7b021-120">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="7b021-121">[Montagestyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="7b021-121">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="7b021-122">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="7b021-122">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="7b021-123">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7b021-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

