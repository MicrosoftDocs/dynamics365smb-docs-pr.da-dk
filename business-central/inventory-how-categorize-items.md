---
title: Organisere varer i kategorier | Microsoft Docs
description: Du kan tildele vareattributter og organisere varerne i kategorier for at gøre det nemmere at søge efter og finde varer.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: d75a24a065d87cee1b40149e1a30f2bc595eaa88
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182272"
---
# <a name="categorize-items"></a><span data-ttu-id="02813-103">Kategorisere varer</span><span class="sxs-lookup"><span data-stu-id="02813-103">Categorize Items</span></span>
<span data-ttu-id="02813-104">Hvis du vil have en oversigt over dine varer og hjælp til at sortere og finde varer, er det nyttigt at arrangere varerne i varekategorier.</span><span class="sxs-lookup"><span data-stu-id="02813-104">To maintain an overview of your items and to help you sort and find items, it is useful to organize your items in item categories.</span></span>

<span data-ttu-id="02813-105">Hvis du vil kunne finde varer ud fra egenskaber, kan du tildele vareattributter til varer og til varekategorier.</span><span class="sxs-lookup"><span data-stu-id="02813-105">To find items by characteristics, you can assign item attributes to items and also to item categories.</span></span> <span data-ttu-id="02813-106">Du kan finde flere oplysninger under [Arbejde med vareattributter](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="02813-106">For more information, see [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4j4mo?rel=0]

## <a name="to-create-an-item-category"></a><span data-ttu-id="02813-107">Sådan oprettes en varekategori</span><span class="sxs-lookup"><span data-stu-id="02813-107">To create an item category</span></span>
1. <span data-ttu-id="02813-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varekategorier**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="02813-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Categories**, and then choose the related link.</span></span>
2. <span data-ttu-id="02813-109">På siden **Varekategorier** skal du vælge handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="02813-109">On the **Item Categories** page, choose the **New** action.</span></span>
3. <span data-ttu-id="02813-110">Udfyld felterne efter behov på siden **Varekategorikort** i oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="02813-110">On the **Item Category Card** page, on the **General** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="02813-111">I oversigtspanelet **Attributter** skal du angive eventuelle vareattributter for varekategorien.</span><span class="sxs-lookup"><span data-stu-id="02813-111">On the **Attributes** FastTab, specify any item attributes for the item category.</span></span> <span data-ttu-id="02813-112">Du kan finde flere oplysninger i [Sådan tildeles vareattributter til varekategorier](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).</span><span class="sxs-lookup"><span data-stu-id="02813-112">For more information, see [To assign item attributes to item categories](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).</span></span>

> [!NOTE]  
>   <span data-ttu-id="02813-113">Hvis varekategorikoden har en overordnet varekategori som angivet af feltet **Overordnet kategori**, udfyldes de vareattributter på forhånd i oversigtspanelet **Attributter**, som er tildelt den pågældende overordnede varekategori.</span><span class="sxs-lookup"><span data-stu-id="02813-113">If the item category has a parent item category, as indicated by the **Parent Category** field, then any item attributes that are assigned to that parent item category are prefilled on the **Attributes** FastTab.</span></span>

> [!NOTE]  
>   <span data-ttu-id="02813-114">Vareattributter, som du tildeler til en varekategori, anvendes automatisk til den vare, der er tildelt varekategorien.</span><span class="sxs-lookup"><span data-stu-id="02813-114">Item attributes that you assign to an item category will automatically apply to the item that the item category is assigned to.</span></span>

## <a name="to-assign-an-item-category-to-an-item"></a><span data-ttu-id="02813-115">Sådan tildeles en varekategori til en vare</span><span class="sxs-lookup"><span data-stu-id="02813-115">To assign an item category to an item</span></span>
1. <span data-ttu-id="02813-116">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="02813-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="02813-117">Åbn kortet for den vare, du vil tildele til en varekategori.</span><span class="sxs-lookup"><span data-stu-id="02813-117">Open the card for the item that you want to assign to an item category.</span></span>
3. <span data-ttu-id="02813-118">Vælg opslagsknappen i feltet **Kategorikode**, og vælg en eksisterende varekategori.</span><span class="sxs-lookup"><span data-stu-id="02813-118">Choose the lookup button in the **Item Category Code** field and select an existing item category.</span></span> <span data-ttu-id="02813-119">Du kan også vælge handlingen **Ny** for først at oprette en ny varekategori som beskrevet i [Sådan oprettes en varekategori](inventory-how-categorize-items.md#to-create-an-item-category).</span><span class="sxs-lookup"><span data-stu-id="02813-119">Alternatively, choose the **New** action to first create a new item category as explained in [To create an item category](inventory-how-categorize-items.md#to-create-an-item-category).</span></span>

## <a name="see-also"></a><span data-ttu-id="02813-120">Se også</span><span class="sxs-lookup"><span data-stu-id="02813-120">See Also</span></span>
[<span data-ttu-id="02813-121">Arbejde med vareattributter</span><span class="sxs-lookup"><span data-stu-id="02813-121">Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
[<span data-ttu-id="02813-122">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="02813-122">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="02813-123">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="02813-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="02813-124">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="02813-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
