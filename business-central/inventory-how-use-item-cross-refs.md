---
title: Bruge varereferencer
description: Konfigurer referencer mellem de beskrivelser, som du og leverandøren bruger til en vare, så du kan indsætte leverandørens varebeskrivelse på købsdokumenter.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 01/12/2021
ms.author: edupont
ms.openlocfilehash: 7d670f6553a1bd70dcc3d97f90436f36c6627c56
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013788"
---
# <a name="use-item-cross-references"></a><span data-ttu-id="c26e5-103">Bruge varereferencer</span><span class="sxs-lookup"><span data-stu-id="c26e5-103">Use Item Cross References</span></span>
<span data-ttu-id="c26e5-104">Hvis du har oprettet en reference mellem varebeskrivelsen, du bruger til en vare, og den beskrivelse, som leverandøren af den pågældende vare bruger, indsættes leverandørens varebeskrivelse automatisk i købsdokumenter for leverandøren, når du udfylder feltet **Varereferencenr.**</span><span class="sxs-lookup"><span data-stu-id="c26e5-104">If you set up a cross reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.**</span></span> <span data-ttu-id="c26e5-105">.</span><span class="sxs-lookup"><span data-stu-id="c26e5-105">field.</span></span> <span data-ttu-id="c26e5-106">De samme funktioner gælder for debitorvarenumre i salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="c26e5-106">The same functionality applies for customer item numbers on sales documents.</span></span>

<span data-ttu-id="c26e5-107">Følgende procedurer beskriver, hvordan du kan bruge varereferencer på købssiden.</span><span class="sxs-lookup"><span data-stu-id="c26e5-107">The following procedures describe how to use item cross references on the purchase side.</span></span> <span data-ttu-id="c26e5-108">Fremgangsmåden er den samme på salgssiden.</span><span class="sxs-lookup"><span data-stu-id="c26e5-108">The steps are similar for the sales side.</span></span>

> [!NOTE]
> <span data-ttu-id="c26e5-109">Det bliver mere almindeligt for vare-id'er, f. eks. GTIN eller GUID, der indeholder 30 eller flere tegn, hvilket er mere end den aktuelle funktion for varereferencer, der kan håndtere.</span><span class="sxs-lookup"><span data-stu-id="c26e5-109">It's becoming more common for item identifiers such as GTINs or GUIDs to contain 30 or more characters, which is more than the current feature for item cross references can handle.</span></span> <span data-ttu-id="c26e5-110">Hvis du skal bruge referencer, der indeholder mere end 30 tegn, kan administratoren aktivere funktionen **Skriv længere varereferencer** på siden [Funktionsadministration ](https://businesscentral.dynamics.com/?page=2610) (linket kræver, at du har en [!INCLUDE[prod_short](includes/prod_short.md)]-lejer).</span><span class="sxs-lookup"><span data-stu-id="c26e5-110">If you need to use references that contain more than 30 characters, your administrator can turn on the **Write longer item references** feature on the [Feature Management](https://businesscentral.dynamics.com/?page=2610) page (link requires that you have a [!INCLUDE[prod_short](includes/prod_short.md)] tenant).</span></span> <span data-ttu-id="c26e5-111">Hvordan du bruger referencer, ændres ikke, men navnene på ting som f. eks. sider og knapper ændres.</span><span class="sxs-lookup"><span data-stu-id="c26e5-111">How you use references doesn't change, but the names of things like pages and buttons will.</span></span> <span data-ttu-id="c26e5-112">F.eks. bliver siden **Varens krydshenvisningsposter** til **Varereferenceposter**.</span><span class="sxs-lookup"><span data-stu-id="c26e5-112">For example, the **Item Cross-Reference Entries** page will become the **Item Reference Entries** page.</span></span>

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a><span data-ttu-id="c26e5-113">Sådan oprettes en varereference til en kreditors varebeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c26e5-113">To set up an item cross reference to a vendor's item description</span></span>

1. <span data-ttu-id="c26e5-114">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c26e5-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="c26e5-115">Åbn kortet for den vare, som du vil oprette en reference for til den varebeskrivelse, som leverandøren bruger til den pågældende vare.</span><span class="sxs-lookup"><span data-stu-id="c26e5-115">Open the card for an item for which you want to create a cross reference to the item description that the vendor uses for that item.</span></span>
3. <span data-ttu-id="c26e5-116">Vælg handlingen **Varereferencer**.</span><span class="sxs-lookup"><span data-stu-id="c26e5-116">Choose the **Cross References** action.</span></span>

     <span data-ttu-id="c26e5-117">Hvis du ikke kan finde handlingen **Varereferencer**, skal du vælge at få vist flere indstillinger og derefter finde den under **Relateret** > **Vare**.</span><span class="sxs-lookup"><span data-stu-id="c26e5-117">If you cannot find the **Cross References** action, choose to view more options, and then find it under **Related** > **Item**.</span></span>
  
4. <span data-ttu-id="c26e5-118">På en ny linje på siden **Varereferenceposter** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="c26e5-118">On a new line on the **Item Cross-Reference Entries** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="c26e5-119">.</span><span class="sxs-lookup"><span data-stu-id="c26e5-119">.</span></span>

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a><span data-ttu-id="c26e5-120">Sådan angiver du en kreditors varebeskrivelse på en købsordre</span><span class="sxs-lookup"><span data-stu-id="c26e5-120">To enter a vendor's item description on a purchase order</span></span>

1. <span data-ttu-id="c26e5-121">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsordre**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c26e5-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="c26e5-122">Opret en købsordre for den leverandør, som du angav en varereference for ovenfor.</span><span class="sxs-lookup"><span data-stu-id="c26e5-122">Create a purchase order for the vendor that you set up an item cross reference for in the previous procedure.</span></span>
3. <span data-ttu-id="c26e5-123">Opret en købslinje for den vare, som du angav en varereference for ovenfor.</span><span class="sxs-lookup"><span data-stu-id="c26e5-123">Create a purchase line for the item that you set up an item cross reference for in the previous procedure.</span></span>
4. <span data-ttu-id="c26e5-124">I feltet **Varereferencenr.**</span><span class="sxs-lookup"><span data-stu-id="c26e5-124">In the **Cross-Reference No.**</span></span> <span data-ttu-id="c26e5-125">skal du vælge den varereference, du har oprettet, og derefter vælge knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="c26e5-125">field, select the item cross reference that you have created, and then choose the **OK** button.</span></span>

<span data-ttu-id="c26e5-126">Feltet **Beskrivelse** på linjen overskrives med kreditorens varebeskrivelse, som blev oprettet i varereferenceposten.</span><span class="sxs-lookup"><span data-stu-id="c26e5-126">The **Description** field on the line is overwritten with the vendor's item description, as set up on the item cross-reference entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="c26e5-127">Se også</span><span class="sxs-lookup"><span data-stu-id="c26e5-127">See Also</span></span>
[<span data-ttu-id="c26e5-128">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="c26e5-128">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="c26e5-129">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="c26e5-129">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="c26e5-130">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c26e5-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
