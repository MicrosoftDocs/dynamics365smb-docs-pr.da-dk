---
title: Sådan oprettes leveringsformer | Microsoft Docs
description: Du kan angive en kode for hver leveringsform, du tilbyder, og angive oplysninger om dem.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 06/17/2019
ms.author: sgroespe
ms.openlocfilehash: 7248f49e92db98cec047d2035ce82d7caf84799f
ms.sourcegitcommit: 6dc83b27ac47f3b39a7b84cfb7446e7f48b8ce63
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/17/2019
ms.locfileid: "1632779"
---
# <a name="set-up-shipment-methods"></a><span data-ttu-id="b9eab-103">Oprette leveringsformer</span><span class="sxs-lookup"><span data-stu-id="b9eab-103">Set Up Shipment Methods</span></span>
<span data-ttu-id="b9eab-104">Leveringsformerne, der også kaldes incoterms, afhænger ofte af varerne, kunderne og leverandørerne.</span><span class="sxs-lookup"><span data-stu-id="b9eab-104">Shipment methods, also called incoterms, often depend on the items, the customers, and the vendors.</span></span> <span data-ttu-id="b9eab-105">En kunde, der bor på en ø, vælger måske, at varerne altid skal flyves eller sejles til øen.</span><span class="sxs-lookup"><span data-stu-id="b9eab-105">For example, if the customer lives on an island, they can choose to have items always shipped by air or always by sea.</span></span> <span data-ttu-id="b9eab-106">Nogle kunder kan kræve levering næste dag.</span><span class="sxs-lookup"><span data-stu-id="b9eab-106">Some customers may require next day delivery.</span></span> <span data-ttu-id="b9eab-107">Det ønsker at afhente ordren.</span><span class="sxs-lookup"><span data-stu-id="b9eab-107">Some may want to pick up the order.</span></span> <span data-ttu-id="b9eab-108">På debitor- og kreditorkortene kan du derfor angive den ønskede leveringsform.</span><span class="sxs-lookup"><span data-stu-id="b9eab-108">On the customer and vendor cards, you can specify what sort of delivery is desired.</span></span>

<span data-ttu-id="b9eab-109">Du opretter beskrivelsen og koden for hver leveringsform på siden **Leveringsformer**.</span><span class="sxs-lookup"><span data-stu-id="b9eab-109">You set up the description and code for each shipment method on the **Shipment Methods** page.</span></span> <span data-ttu-id="b9eab-110">Du kan f.eks. oprette koden FOB (Free on board) og skrive Free on Board i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="b9eab-110">For example, you can set up the code FOB, and enter Free on Board in the **Description** field.</span></span> <span data-ttu-id="b9eab-111">Du kan indtaste koden i **Leveringskode**-felterne et andet sted i systemet, f.eks. på et debitorkort.</span><span class="sxs-lookup"><span data-stu-id="b9eab-111">You can then enter the code in **Shipment Method Code** fields elsewhere in the system, such as on a customer card.</span></span> <span data-ttu-id="b9eab-112">Når du derefter opretter nye ordrer, fakturaer, kreditnotaer osv., bruges den beskrivelse, som koden repræsenterer, automatisk af systemet.</span><span class="sxs-lookup"><span data-stu-id="b9eab-112">Then when you create new orders, invoices, credit memos, and so on, the system will enter the description represented by the code.</span></span> <span data-ttu-id="b9eab-113">Du kan ændre dette i dokumentet efter behov.</span><span class="sxs-lookup"><span data-stu-id="b9eab-113">You can change it on the document as needed.</span></span>

## <a name="to-set-up-a-shipment-code"></a><span data-ttu-id="b9eab-114">Sådan defineres en leveringskode</span><span class="sxs-lookup"><span data-stu-id="b9eab-114">To set up a shipment code</span></span>
1. <span data-ttu-id="b9eab-115">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Leveringsformer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="b9eab-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="b9eab-116">På siden **Leveringsformer** skal du vælge handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b9eab-116">On the **Shipment Methods** page, choose the **New** action.</span></span>
3. <span data-ttu-id="b9eab-117">Angiv en kode og en beskrivelse af leveringsformen på den nye linje.</span><span class="sxs-lookup"><span data-stu-id="b9eab-117">On the new line, specify a code and description for the shipment method.</span></span>

## <a name="see-also"></a><span data-ttu-id="b9eab-118">Se også</span><span class="sxs-lookup"><span data-stu-id="b9eab-118">See Also</span></span>
[<span data-ttu-id="b9eab-119">Incoterms</span><span class="sxs-lookup"><span data-stu-id="b9eab-119">Incoterms</span></span>](https://iccwbo.org/resources-for-business/incoterms-rules)  
[<span data-ttu-id="b9eab-120">Oprette speditører</span><span class="sxs-lookup"><span data-stu-id="b9eab-120">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)  
<span data-ttu-id="b9eab-121">[Spore pakker](sales-how-track-packages.md)  </span><span class="sxs-lookup"><span data-stu-id="b9eab-121">[Track Packages](sales-how-track-packages.md)  </span></span>  
[<span data-ttu-id="b9eab-122">Logistik</span><span class="sxs-lookup"><span data-stu-id="b9eab-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="b9eab-123">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="b9eab-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="b9eab-124">[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="b9eab-124">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="b9eab-125">[Montagestyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="b9eab-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="b9eab-126">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="b9eab-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="b9eab-127">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b9eab-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
