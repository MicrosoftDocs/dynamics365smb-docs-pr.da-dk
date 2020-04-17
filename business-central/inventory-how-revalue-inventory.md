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
ms.author: sgroespe
ms.openlocfilehash: c961d15d04da5fcad18a460adc269f3099962f6a
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182128"
---
# <a name="revalue-inventory"></a><span data-ttu-id="cf384-103">Regulere lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="cf384-103">Revalue Inventory</span></span>
<span data-ttu-id="cf384-104">Hvis du vil op- eller nedskrive en vare eller en bestemt varepost, skal du bruge reguleringskladden.</span><span class="sxs-lookup"><span data-stu-id="cf384-104">If you want to appreciate or depreciate an item or a specific item ledger entry, you must use the revaluation journal.</span></span>

## <a name="to-revalue-inventory"></a><span data-ttu-id="cf384-105">Sådan reguleres lagerbeholdningen</span><span class="sxs-lookup"><span data-stu-id="cf384-105">To revalue inventory</span></span>
1. <span data-ttu-id="cf384-106">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Værdireguleringskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="cf384-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Revaluation Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="cf384-107">Vælg handlingen **Beregn lagerværdi**.</span><span class="sxs-lookup"><span data-stu-id="cf384-107">Choose the **Calculate Inventory Value** action.</span></span>
3. <span data-ttu-id="cf384-108">På siden **Beregn lagerværdi** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="cf384-108">On the **Calculate Inventory Value** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="cf384-109">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="cf384-109">Choose the **OK** button.</span></span>
5. <span data-ttu-id="cf384-110">Angiv den nye kostpris på hver linje på siden **Værdireguleringskladde** i feltet **Kostpris (reguleret)**.</span><span class="sxs-lookup"><span data-stu-id="cf384-110">On each line on the **Revaluation Journal** page, in the **Unit Cost (Revalued)** field, enter the new unit cost.</span></span> <span data-ttu-id="cf384-111">Eller du kan i stedet angive det nye, samlede beløb i feltet **Lagerværdi (reguleret)**.</span><span class="sxs-lookup"><span data-stu-id="cf384-111">Alternatively, enter the new total amount in the **Inventory Value (Revalued)** field.</span></span>

    <span data-ttu-id="cf384-112">De relevante felter opdateres automatisk.</span><span class="sxs-lookup"><span data-stu-id="cf384-112">The relevant fields are automatically updated.</span></span> <span data-ttu-id="cf384-113">Bemærk, at feltet **Beløb** indeholder den faktiske ændring i lagerværdien for den valgte varepost.</span><span class="sxs-lookup"><span data-stu-id="cf384-113">Note that the **Amount** field shows the actual change in inventory value for the selected item ledger entry.</span></span> <span data-ttu-id="cf384-114">Det er differencen mellem feltet **Lagerværdi (beregnet)** og feltet **Lagerværdi (reguleret)**, der beregnes.</span><span class="sxs-lookup"><span data-stu-id="cf384-114">It calculates the difference between the **Inventory Value (Calculated)** field and the **Inventory Value (Revalued)** field.</span></span>
6. <span data-ttu-id="cf384-115">Når du har udfyldt alle linjerne i reguleringskladden, skal du vælge handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="cf384-115">When you have completed all lines in the revaluation journal, choose the **Post** action.</span></span>

<span data-ttu-id="cf384-116">Nye værdiposter oprettes nu for at afspejle de værdireguleringer, du har bogført.</span><span class="sxs-lookup"><span data-stu-id="cf384-116">New value entries are now created to reflect the revaluations that you have posted.</span></span> <span data-ttu-id="cf384-117">Du kan se de nye værdier på de respektive varekort.</span><span class="sxs-lookup"><span data-stu-id="cf384-117">You can see the new values on the respective item cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="cf384-118">Se også</span><span class="sxs-lookup"><span data-stu-id="cf384-118">See Also</span></span>
[<span data-ttu-id="cf384-119">Designoplysninger: Regulering</span><span class="sxs-lookup"><span data-stu-id="cf384-119">Design Details: Revaluation</span></span>](design-details-revaluation.md)  
[<span data-ttu-id="cf384-120">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="cf384-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="cf384-121">Salg</span><span class="sxs-lookup"><span data-stu-id="cf384-121">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="cf384-122">Køb</span><span class="sxs-lookup"><span data-stu-id="cf384-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="cf384-123">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cf384-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
