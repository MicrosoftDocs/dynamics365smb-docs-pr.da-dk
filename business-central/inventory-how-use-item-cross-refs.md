---
title: Bruge varereferencer | Microsoft Docs
description: Hvis du har oprettet en reference mellem varebeskrivelsen, du bruger til en vare, og den beskrivelse, som leverandøren af den pågældende vare bruger, indsættes leverandørens varebeskrivelse automatisk i købsdokumenter for leverandøren, når du udfylder feltet **Varereferencenr.** .
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 03/12/2019
ms.author: sgroespe
ms.openlocfilehash: 09fb7c17e2fccbd3b2ad3195cffa37493ad40f61
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/19/2019
ms.locfileid: "852259"
---
# <a name="use-item-cross-references"></a><span data-ttu-id="a3c14-104">Bruge varereferencer</span><span class="sxs-lookup"><span data-stu-id="a3c14-104">Use Item Cross References</span></span>
<span data-ttu-id="a3c14-105">Hvis du har oprettet en reference mellem varebeskrivelsen, du bruger til en vare, og den beskrivelse, som leverandøren af den pågældende vare bruger, indsættes leverandørens varebeskrivelse automatisk i købsdokumenter for leverandøren, når du udfylder feltet **Varereferencenr.**</span><span class="sxs-lookup"><span data-stu-id="a3c14-105">If you set up a cross reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.**</span></span> <span data-ttu-id="a3c14-106">.</span><span class="sxs-lookup"><span data-stu-id="a3c14-106">field.</span></span> <span data-ttu-id="a3c14-107">De samme funktioner gælder for debitorvarenumre i salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="a3c14-107">The same functionality applies for customer item numbers on sales documents.</span></span>

<span data-ttu-id="a3c14-108">Følgende procedurer beskriver, hvordan du kan bruge varereferencer på købssiden.</span><span class="sxs-lookup"><span data-stu-id="a3c14-108">The following procedures describe how to use item cross references on the purchase side.</span></span> <span data-ttu-id="a3c14-109">Fremgangsmåden er den samme på salgssiden.</span><span class="sxs-lookup"><span data-stu-id="a3c14-109">The steps are similar for the sales side.</span></span>

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a><span data-ttu-id="a3c14-110">Sådan oprettes en varereference til en kreditors varebeskrivelse</span><span class="sxs-lookup"><span data-stu-id="a3c14-110">To set up an item cross reference to a vendor's item description</span></span>
1. <span data-ttu-id="a3c14-111">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="a3c14-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="a3c14-112">Åbn kortet for den vare, som du vil oprette en reference for til den varebeskrivelse, som leverandøren bruger til den pågældende vare.</span><span class="sxs-lookup"><span data-stu-id="a3c14-112">Open the card for an item for which you want to create a cross reference to the item description that the vendor uses for that item.</span></span>
3. <span data-ttu-id="a3c14-113">Vælg handlingen **Varereferencer**.</span><span class="sxs-lookup"><span data-stu-id="a3c14-113">Choose the **Cross References** action.</span></span>
4. <span data-ttu-id="a3c14-114">På en ny linje på siden **Varereferenceposter** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="a3c14-114">On a new line on the **Item Cross-Reference Entries** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="a3c14-115">.</span><span class="sxs-lookup"><span data-stu-id="a3c14-115">.</span></span>

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a><span data-ttu-id="a3c14-116">Sådan angiver du en kreditors varebeskrivelse på en købsordre</span><span class="sxs-lookup"><span data-stu-id="a3c14-116">To enter a vendor's item description on a purchase order</span></span>
1. <span data-ttu-id="a3c14-117">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="a3c14-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="a3c14-118">Opret en købsordre for den leverandør, som du angav en varereference for ovenfor.</span><span class="sxs-lookup"><span data-stu-id="a3c14-118">Create a purchase order for the vendor that you set up an item cross reference for in the previous procedure.</span></span>
3. <span data-ttu-id="a3c14-119">Opret en købslinje for den vare, som du angav en varereference for ovenfor.</span><span class="sxs-lookup"><span data-stu-id="a3c14-119">Create a purchase line for the item that you set up an item cross reference for in the previous procedure.</span></span>
4. <span data-ttu-id="a3c14-120">I feltet **Varereferencenr.**</span><span class="sxs-lookup"><span data-stu-id="a3c14-120">In the **Cross-Reference No.**</span></span> <span data-ttu-id="a3c14-121">skal du vælge den varereference, du har oprettet, og derefter vælge knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3c14-121">field, select the item cross reference that you have created, and then choose the **OK** button.</span></span>

<span data-ttu-id="a3c14-122">Feltet **Beskrivelse** på linjen overskrives med kreditorens varebeskrivelse, som blev oprettet i varereferenceposten.</span><span class="sxs-lookup"><span data-stu-id="a3c14-122">The **Description** field on the line is overwritten with the vendor's item description, as set up on the item cross-reference entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3c14-123">Se også</span><span class="sxs-lookup"><span data-stu-id="a3c14-123">See Also</span></span>
[<span data-ttu-id="a3c14-124">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="a3c14-124">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="a3c14-125">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="a3c14-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="a3c14-126">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a3c14-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
