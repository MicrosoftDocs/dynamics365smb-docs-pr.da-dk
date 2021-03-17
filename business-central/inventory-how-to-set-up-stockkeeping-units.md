---
title: Sådan oprettes lagervarer | Microsoft Docs
description: Du kan bruge lagervarer til at registrere oplysninger om dine varer på en bestemt lokation eller med en bestemt variantkode.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4136cdb7dd89e2998a3fe0e8107dd82b3ab40619
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393045"
---
# <a name="set-up-stockkeeping-units"></a><span data-ttu-id="fddc9-103">Opsætte lagervarer</span><span class="sxs-lookup"><span data-stu-id="fddc9-103">Set Up Stockkeeping Units</span></span>
<span data-ttu-id="fddc9-104">Du kan bruge lagervarer til at registrere oplysninger om dine varer på en bestemt lokation eller med en bestemt variantkode.</span><span class="sxs-lookup"><span data-stu-id="fddc9-104">You can use stockkeeping units to record information about your items for a specific location or a specific variant code.</span></span>  

 <span data-ttu-id="fddc9-105">Lagervarer er et supplement til varekortene.</span><span class="sxs-lookup"><span data-stu-id="fddc9-105">Stockkeeping units are a supplement to item cards.</span></span> <span data-ttu-id="fddc9-106">De erstatter dem ikke, selvom de er relateret til dem.</span><span class="sxs-lookup"><span data-stu-id="fddc9-106">They do not replace them, although they are related to them.</span></span> <span data-ttu-id="fddc9-107">Med lagervarer kan du udskille oplysningerne om den samme vare, så de kun vedrører en bestemt lokation, f.eks. et lager eller distributionscenter, eller en bestemt variant, f.eks. forskellige hyldenumre og forskellige genbestillingsdata.</span><span class="sxs-lookup"><span data-stu-id="fddc9-107">Stockkeeping units allow you to differentiate information about an item for a specific location, such as a warehouse or distribution center, or a specific variant, such as different shelf numbers and different replenishment information, for the same item.</span></span>  

## <a name="to-set-up-a-stockkeeping-unit"></a><span data-ttu-id="fddc9-108">Sådan opsættes en lagervare</span><span class="sxs-lookup"><span data-stu-id="fddc9-108">To set up a stockkeeping unit</span></span>  

1.  <span data-ttu-id="fddc9-109">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lagervarer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="fddc9-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Stockkeeping Units**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="fddc9-110">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="fddc9-110">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="fddc9-111">Udfyld felterne på kortet.</span><span class="sxs-lookup"><span data-stu-id="fddc9-111">Fill in the fields on the card.</span></span> <span data-ttu-id="fddc9-112">Følgende felter er obligatoriske: **Varenr.**, **Lokationskode** og/eller **Variantkode**.</span><span class="sxs-lookup"><span data-stu-id="fddc9-112">The following fields are required: **Item No.**, **Location Code**, and/or **Variant Code**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

<span data-ttu-id="fddc9-113">Når du har angivet den første lagervare, bliver afkrydsningsfeltet **Lagervare findes** automatisk markeret på **Vare**-kortet.</span><span class="sxs-lookup"><span data-stu-id="fddc9-113">When you have set up the first stockkeeping unit for an item, the **Stockkeeping Unit Exists** check box on the **Item** card is selected.</span></span>  

<span data-ttu-id="fddc9-114">Brug kørslen **Opret lagervare**, hvis du vil oprette flere lagerførte varer.</span><span class="sxs-lookup"><span data-stu-id="fddc9-114">To create several stockkeeping units for an item, use the **Create Stockkeeping Unit** batch job.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="fddc9-115">Oplysningerne på **lagervarekortet** tilsidesætter oplysningerne på **varekortet**.</span><span class="sxs-lookup"><span data-stu-id="fddc9-115">The information on the **Stockkeeping Unit** card has priority over the **Item** card.</span></span>

> [!Warning]
> <span data-ttu-id="fddc9-116">Hvis lagervaren angives via produktion, bruges feltet **Kostpris (standard)** ikke ved fakturering og justering af den faktiske kostpris for den producerede vare.</span><span class="sxs-lookup"><span data-stu-id="fddc9-116">If the SKU is supplied through production, then the **Standard Cost** field is not used when invoicing and adjusting the actual cost of the produced item.</span></span> <span data-ttu-id="fddc9-117">I stedet anvendes feltet **Kostpris (standard)** på det underliggende varekort, og eventuelle afvigelser beregnes mod kostprisfordelingen for den vare.</span><span class="sxs-lookup"><span data-stu-id="fddc9-117">Instead, the **Standard Cost** field on the underlying item card is used, and any variances are calculated against the cost shares of that item.</span></span><br /><br />
> <span data-ttu-id="fddc9-118">Fordi produktionsstyklister og rute ikke kan tildeles lagervarer, så er kostprisakkumulering og den relaterede beregning af kostprisfordelingen heller ikke tilgængelig på lagervarer.</span><span class="sxs-lookup"><span data-stu-id="fddc9-118">Because production BOMs and routing cannot be assigned to SKUs, then the unit cost roll-up and the related calculation of cost shares are also not available on SKUs.</span></span> <span data-ttu-id="fddc9-119">Du kan finde flere oplysninger i [Om beregning af standardkostpris](finance-about-calculating-standard-cost.md)</span><span class="sxs-lookup"><span data-stu-id="fddc9-119">For more information, see [About Calculating Standard Cost](finance-about-calculating-standard-cost.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="fddc9-120">Se også</span><span class="sxs-lookup"><span data-stu-id="fddc9-120">See Also</span></span>  
[<span data-ttu-id="fddc9-121">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="fddc9-121">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="fddc9-122">Sådan konfigureres logistikfunktioner</span><span class="sxs-lookup"><span data-stu-id="fddc9-122">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="fddc9-123">Logistik</span><span class="sxs-lookup"><span data-stu-id="fddc9-123">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="fddc9-124">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="fddc9-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="fddc9-125">[Montagestyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="fddc9-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="fddc9-126">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="fddc9-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="fddc9-127">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fddc9-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]