---
title: Oprette nye værdiposter for varer i lagerbeholdningen | Microsoft Docs
description: Beskriver, hvordan værdiposterne for en eller flere varer på lageret kan op- eller nedskrives ved at bogføre deres aktuelle, beregnede værdi.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 3570d5e7347745763c8d8e18dfdf65166e7839e0
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782039"
---
# <a name="revalue-inventory"></a><span data-ttu-id="c4b0a-103">Regulere lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="c4b0a-103">Revalue Inventory</span></span>
<span data-ttu-id="c4b0a-104">Hvis du vil op- eller nedskrive en vare eller en bestemt varepost, skal du bruge reguleringskladden.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-104">If you want to appreciate or depreciate an item or a specific item ledger entry, you must use the revaluation journal.</span></span>

## <a name="to-revalue-inventory"></a><span data-ttu-id="c4b0a-105">Sådan reguleres lagerbeholdningen</span><span class="sxs-lookup"><span data-stu-id="c4b0a-105">To revalue inventory</span></span>
1. <span data-ttu-id="c4b0a-106">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Værdireguleringskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Revaluation Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="c4b0a-107">Vælg handlingen **Beregn lagerværdi**.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-107">Choose the **Calculate Inventory Value** action.</span></span>
3. <span data-ttu-id="c4b0a-108">På siden **Beregn lagerværdi** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-108">On the **Calculate Inventory Value** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="c4b0a-109">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-109">Choose the **OK** button.</span></span>
5. <span data-ttu-id="c4b0a-110">Angiv den nye kostpris på hver linje på siden **Værdireguleringskladde** i feltet **Kostpris (reguleret)**.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-110">On each line on the **Revaluation Journal** page, in the **Unit Cost (Revalued)** field, enter the new unit cost.</span></span> <span data-ttu-id="c4b0a-111">Eller du kan i stedet angive det nye, samlede beløb i feltet **Lagerværdi (reguleret)**.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-111">Alternatively, enter the new total amount in the **Inventory Value (Revalued)** field.</span></span>

    <span data-ttu-id="c4b0a-112">De relevante felter opdateres automatisk.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-112">The relevant fields are automatically updated.</span></span> <span data-ttu-id="c4b0a-113">Bemærk, at feltet **Beløb** indeholder den faktiske ændring i lagerværdien for den valgte varepost.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-113">Note that the **Amount** field shows the actual change in inventory value for the selected item ledger entry.</span></span> <span data-ttu-id="c4b0a-114">Det er differencen mellem feltet **Lagerværdi (beregnet)** og feltet **Lagerværdi (reguleret)**, der beregnes.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-114">It calculates the difference between the **Inventory Value (Calculated)** field and the **Inventory Value (Revalued)** field.</span></span>
6. <span data-ttu-id="c4b0a-115">Når du har udfyldt alle linjerne i reguleringskladden, skal du vælge handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-115">When you have completed all lines in the revaluation journal, choose the **Post** action.</span></span>

<span data-ttu-id="c4b0a-116">Nye værdiposter oprettes nu for at afspejle de værdireguleringer, du har bogført.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-116">New value entries are now created to reflect the revaluations that you have posted.</span></span> <span data-ttu-id="c4b0a-117">Du kan se de nye værdier på de respektive varekort.</span><span class="sxs-lookup"><span data-stu-id="c4b0a-117">You can see the new values on the respective item cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="c4b0a-118">Se også</span><span class="sxs-lookup"><span data-stu-id="c4b0a-118">See Also</span></span>
[<span data-ttu-id="c4b0a-119">Designoplysninger: Regulering</span><span class="sxs-lookup"><span data-stu-id="c4b0a-119">Design Details: Revaluation</span></span>](design-details-revaluation.md)  
[<span data-ttu-id="c4b0a-120">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="c4b0a-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="c4b0a-121">Salg</span><span class="sxs-lookup"><span data-stu-id="c4b0a-121">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="c4b0a-122">Køb</span><span class="sxs-lookup"><span data-stu-id="c4b0a-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="c4b0a-123">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c4b0a-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
