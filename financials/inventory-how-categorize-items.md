---
title: Organisere varer i kategorier | Microsoft Docs
description: "Du kan tildele vareattributter og organisere varerne i kategorier for at gøre det nemmere at søge efter og finde varer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 64511e0979671d13740bd18d95d53e8e37564583
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="categorize-items"></a><span data-ttu-id="2683a-103">Kategorisere varer</span><span class="sxs-lookup"><span data-stu-id="2683a-103">Categorize Items</span></span>
<span data-ttu-id="2683a-104">Hvis du vil have en oversigt over dine varer og hjælp til at sortere og finde varer, er det nyttigt at arrangere varerne i varekategorier.</span><span class="sxs-lookup"><span data-stu-id="2683a-104">To maintain an overview of your items and to help you sort and find items, it is useful to organize your items in item categories.</span></span>

<span data-ttu-id="2683a-105">Hvis du vil kunne finde varer ud fra egenskaber, kan du tildele vareattributter til varer og til varekategorier.</span><span class="sxs-lookup"><span data-stu-id="2683a-105">To find items by characteristics, you can assign item attributes to items and also to item categories.</span></span> <span data-ttu-id="2683a-106">Du kan finde flere oplysninger under [Arbejde med vareattributter](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="2683a-106">For more information, see [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

## <a name="to-create-an-item-category"></a><span data-ttu-id="2683a-107">Sådan oprettes en varekategori</span><span class="sxs-lookup"><span data-stu-id="2683a-107">To create an item category</span></span>
1. <span data-ttu-id="2683a-108">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kategorier**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="2683a-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Categories**, and then choose the related link.</span></span>
2. <span data-ttu-id="2683a-109">I vinduet **Varekategorier** skal du vælge handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2683a-109">In the **Item Categories** window, choose the **New** action.</span></span>
3. <span data-ttu-id="2683a-110">Udfyld felterne efter behov i vinduet **Varekategorikort** i oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="2683a-110">In the **Item Category Card** window, on the **General** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="2683a-111">I oversigtspanelet **Attributter** skal du angive eventuelle vareattributter for varekategorien.</span><span class="sxs-lookup"><span data-stu-id="2683a-111">On the **Attributes** FastTab, specify any item attributes for the item category.</span></span> <span data-ttu-id="2683a-112">Hvis du vil finde flere oplysninger, skal du se afsnittet "Sådan tildeles vareattributter til en varekategori" i [Arbejde med vareattributter](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="2683a-112">For more information, see the "To assign item attributes to an item category" section in [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="2683a-113">Hvis varekategorikoden har en overordnet varekategori som angivet af feltet **Overordnet kategori**, udfyldes de vareattributter på forhånd i oversigtspanelet **Attributter**, som er tildelt den pågældende overordnede varekategori.</span><span class="sxs-lookup"><span data-stu-id="2683a-113">If the item category has a parent item category, as indicated by the **Parent Category** field, then any item attributes that are assigned to that parent item category are prefilled on the **Attributes** FastTab.</span></span>

> [!NOTE]  
>   <span data-ttu-id="2683a-114">Vareattributter, som du tildeler til en varekategori, anvendes automatisk til den vare, der er tildelt varekategorien.</span><span class="sxs-lookup"><span data-stu-id="2683a-114">Item attributes that you assign to an item category will automatically apply to the item that the item category is assigned to.</span></span>

## <a name="to-assign-an-item-category-to-an-item"></a><span data-ttu-id="2683a-115">Sådan tildeles en varekategori til en vare</span><span class="sxs-lookup"><span data-stu-id="2683a-115">To assign an item category to an item</span></span>
1. <span data-ttu-id="2683a-116">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="2683a-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="2683a-117">Åbn kortet for den vare, du vil tildele til en varekategori.</span><span class="sxs-lookup"><span data-stu-id="2683a-117">Open the card for the item that you want to assign to an item category.</span></span>
3. <span data-ttu-id="2683a-118">Vælg opslagsknappen i feltet **Kategorikode**, og vælg en eksisterende varekategori.</span><span class="sxs-lookup"><span data-stu-id="2683a-118">Choose the lookup button in the **Item Category Code** field and select an existing item category.</span></span> <span data-ttu-id="2683a-119">Du kan også vælge handlingen **Ny** for først at oprette en ny varekategori som beskrevet i afsnittet "Sådan oprettes en varekategori".</span><span class="sxs-lookup"><span data-stu-id="2683a-119">Alternatively, choose the **New** action to first create a new item category as explained in the "To create an item category" section.</span></span>

## <a name="see-also"></a><span data-ttu-id="2683a-120">Se også</span><span class="sxs-lookup"><span data-stu-id="2683a-120">See Also</span></span>
[<span data-ttu-id="2683a-121">Arbejde med vareattributter</span><span class="sxs-lookup"><span data-stu-id="2683a-121">Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
[<span data-ttu-id="2683a-122">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="2683a-122">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="2683a-123">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="2683a-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="2683a-124">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2683a-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

