---
title: Oprette og administrere katalogvarer | Microsoft Docs
description: "Beskriver, hvordan du handler med ikke-lagervarer eller varer, der ikke indgår i lagerbeholdningen."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2969b3168f063e636455dd67457c01ed89a0727d
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-nonstock-items"></a><span data-ttu-id="b07fc-103">Arbejde med katalogvarer</span><span class="sxs-lookup"><span data-stu-id="b07fc-103">Work with Nonstock Items</span></span>
<span data-ttu-id="b07fc-104">Du kan tilbyde bestemte varer til dine kunder, som du ikke vil lagerføre, før du begynder at sælge dem.</span><span class="sxs-lookup"><span data-stu-id="b07fc-104">You can offer certain items to your customers for their convenience, which you do not want to maintain in inventory until you start selling them.</span></span> <span data-ttu-id="b07fc-105">Når du vil begynde at lagerføre sådanne varer, kan du konvertere dem til normale varekort på to måder.</span><span class="sxs-lookup"><span data-stu-id="b07fc-105">When you want to start maintaining such items in inventory, you can convert them to normal item cards in two ways.</span></span>

* <span data-ttu-id="b07fc-106">Opret en ny varekort ud fra en skabelon for et katalogvarekort.</span><span class="sxs-lookup"><span data-stu-id="b07fc-106">From a nonstock item card, create a new item card based on a template.</span></span>
* <span data-ttu-id="b07fc-107">Vælg en katalogvare fra en salgsordrelinje af typen **Vare** med et tomt \**Nummer*-felt.</span><span class="sxs-lookup"><span data-stu-id="b07fc-107">From a sales order line of type **Item** with an empty \**No* field, select a nonstock item.</span></span> <span data-ttu-id="b07fc-108">Der oprettes automatisk et varekort for katalogvaren.</span><span class="sxs-lookup"><span data-stu-id="b07fc-108">An item card is automatically created for the nonstock item.</span></span>

> [!NOTE]  
>   <span data-ttu-id="b07fc-109">Du kan ikke vælge en katalogvare fra vinduet **Salgsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="b07fc-109">You cannot select a nonstock item from the **Sales Invoice** window.</span></span> <span data-ttu-id="b07fc-110">Du kan vælge en katalogvare fra vinduet **Salgstilbud**, men katalogvaren konverteres ikke til en almindelig vare, når du bruger funktionen **Lav ordre**.</span><span class="sxs-lookup"><span data-stu-id="b07fc-110">You can select a nonstock item from the **Sales Quote** window, but the nonstock item will not be converted to a normal item when you use the **Make Order** function.</span></span>

<span data-ttu-id="b07fc-111">En katalogvare har typisk varenummeret fra den leverandør, som leverer den.</span><span class="sxs-lookup"><span data-stu-id="b07fc-111">A nonstock item typically has the item number of the vendor who supplies it.</span></span> <span data-ttu-id="b07fc-112">Hvis du vil aktivere konvertering af et katalogvarekort til et normalt varekort, skal du først angive, hvordan leverandørens varenumre skal konverteres til dine egne varenumre.</span><span class="sxs-lookup"><span data-stu-id="b07fc-112">To enable conversion of a nonstock item card to a normal item card, you must first set up how vendor item numbering is converted to your own item numbering.</span></span>   

## <a name="to-create-a-nonstock-item"></a><span data-ttu-id="b07fc-113">Sådan oprettes en katalogvare</span><span class="sxs-lookup"><span data-stu-id="b07fc-113">To create a nonstock item</span></span>
<span data-ttu-id="b07fc-114">Katalogvarekort indeholder meget færre oplysninger end normale varekort, da du kun bruger til at give tilbud og andre formål.</span><span class="sxs-lookup"><span data-stu-id="b07fc-114">Nonstock item cards have much less information than normal item cards because you only use them to offer on quotes and in other ways.</span></span> <span data-ttu-id="b07fc-115">Derfor skal de konverteres til normale varekort, før du kan bogføre salgstransaktioner for dem.</span><span class="sxs-lookup"><span data-stu-id="b07fc-115">For that reason, they must be converted to normal item cards before you can post sales transactions for them.</span></span>

1. <span data-ttu-id="b07fc-116">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Katalogvarer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="b07fc-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Nonstock Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="b07fc-117">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b07fc-117">Choose the **New** action.</span></span>
3. <span data-ttu-id="b07fc-118">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="b07fc-118">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-how-nonstock-item-numbers-are-converted-to-your-own-numbering"></a><span data-ttu-id="b07fc-119">Sådan angiver du, hvordan katalogvare konverteres til din egen nummerering</span><span class="sxs-lookup"><span data-stu-id="b07fc-119">To set up how nonstock item numbers are converted to your own numbering</span></span>
<span data-ttu-id="b07fc-120">Hvis du vil aktivere konvertering af et katalogvarekort til et normalt varekort, skal du først angive, hvordan leverandørens varenummerering skal konverteres til dit eget varenummerformat.</span><span class="sxs-lookup"><span data-stu-id="b07fc-120">To enable conversion of a nonstock item card to a normal item card, you must first set up how the vendor's item numbering is converted to your own item number format.</span></span>

1. <span data-ttu-id="b07fc-121">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Katalogvareopsætning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="b07fc-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Nonstock Item Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="b07fc-122">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="b07fc-122">Fill in the fields as necessary.</span></span>

## <a name="to-convert-a-nonstock-item-to-a-normal-item"></a><span data-ttu-id="b07fc-123">Sådan konverteres en katalogvare til en almindelig vare</span><span class="sxs-lookup"><span data-stu-id="b07fc-123">To convert a nonstock item to a normal item</span></span>
1. <span data-ttu-id="b07fc-124">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Katalogvarer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="b07fc-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Nonstock Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="b07fc-125">Åbn kortet for en katalogvare, som du vil konvertere til en almindelig vare.</span><span class="sxs-lookup"><span data-stu-id="b07fc-125">Open the card for a nonstock item that you want to convert to a normal item.</span></span>
3. <span data-ttu-id="b07fc-126">I vinduet **Katalogvarekort** skal du vælge handlingen **Opret vare**.</span><span class="sxs-lookup"><span data-stu-id="b07fc-126">In the **Nonstock Item Card** window, choose the **Create Item** action.</span></span>

<span data-ttu-id="b07fc-127">Der oprettes et nyt varekort, der er udfyldt på forhånd med oplysninger fra katalogvaren og en relevant vareskabelon.</span><span class="sxs-lookup"><span data-stu-id="b07fc-127">A new item card prefilled with information from the nonstock item and a relevant item template is created.</span></span> <span data-ttu-id="b07fc-128">Du kan derefter udfylde eller redigere felterne på det nye varekort efter behov.</span><span class="sxs-lookup"><span data-stu-id="b07fc-128">You can then fill or edit fields on the new item card as necessary.</span></span> <span data-ttu-id="b07fc-129">Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="b07fc-129">For more information, see [Register New Items](inventory-how-register-new-items.md).</span></span>

## <a name="to-sell-a-nonstock-item-and-convert-it-to-a-normal-item"></a><span data-ttu-id="b07fc-130">Sådan sælges en katalogvare og konverteres den til en almindelig vare</span><span class="sxs-lookup"><span data-stu-id="b07fc-130">To sell a nonstock item, and convert it to a normal item</span></span>
1. <span data-ttu-id="b07fc-131">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="b07fc-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="b07fc-132">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b07fc-132">Choose the **New** action.</span></span> <span data-ttu-id="b07fc-133">Udfyld felterne i oversigtspanelet **Generelt** for enhver salgsordre.</span><span class="sxs-lookup"><span data-stu-id="b07fc-133">Fill in the fields on the **General** FastTab as for any sales order.</span></span> <span data-ttu-id="b07fc-134">Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="b07fc-134">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
3. <span data-ttu-id="b07fc-135">På en ny salgslinje skal du vælge **Vare** i feltet **Type**, men lade feltet **Nummer**</span><span class="sxs-lookup"><span data-stu-id="b07fc-135">On a new sales line, in the **Type** field, select **Item**, but leave the **No.**</span></span> <span data-ttu-id="b07fc-136">være tomt.</span><span class="sxs-lookup"><span data-stu-id="b07fc-136">field empty.</span></span>
4. <span data-ttu-id="b07fc-137">Vælg handlingen **Linje**, og vælg derefter handlingen **Vælg katalogvarer**.</span><span class="sxs-lookup"><span data-stu-id="b07fc-137">Choose the **Line** action, and then choose the **Select Nonstock Items** action.</span></span>

    <span data-ttu-id="b07fc-138">Katalogvaren konverteres til en almindelig vare.</span><span class="sxs-lookup"><span data-stu-id="b07fc-138">The nonstock item is converted to a normal item.</span></span> <span data-ttu-id="b07fc-139">Der oprettes et nyt varekort, der er udfyldt på forhånd med oplysninger fra katalogvaren og en relevant vareskabelon.</span><span class="sxs-lookup"><span data-stu-id="b07fc-139">A new item card prefilled with information from the nonstock item and a relevant item template is created.</span></span>
5. <span data-ttu-id="b07fc-140">I vinduet **Katalogvarer** skal du vælge den katalogvare, som du vil sælge, og derefter vælge knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="b07fc-140">In the **Nonstock Items** window, select the nonstock item that you want to sell, and then choose the **OK** button.</span></span>
6. <span data-ttu-id="b07fc-141">Når salgsordren er fuldført, skal du vælge handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="b07fc-141">When the sales order is complete, choose the **Post** action.</span></span>

<span data-ttu-id="b07fc-142">Du kan derefter udfylde eller redigere felterne på det nye varekort efter behov.</span><span class="sxs-lookup"><span data-stu-id="b07fc-142">You can then fill or edit fields on the new item card as necessary.</span></span> <span data-ttu-id="b07fc-143">Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="b07fc-143">For more information, see [Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="b07fc-144">Der oprettes automatisk en varereferencepost for kreditoren til varen mellem leverandørens varenummer og dit nye varenummer.</span><span class="sxs-lookup"><span data-stu-id="b07fc-144">An Item cross reference record is automatically created for the vendor of the item between the vendor's item number and your new item number.</span></span>

## <a name="see-also"></a><span data-ttu-id="b07fc-145">Se også</span><span class="sxs-lookup"><span data-stu-id="b07fc-145">See Also</span></span>
[<span data-ttu-id="b07fc-146">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="b07fc-146">Register New Items</span></span>](inventory-how-register-new-items.md)  
<span data-ttu-id="b07fc-147">[Oprette specialordrer](sales-how-to-create-special-orders.md)|</span><span class="sxs-lookup"><span data-stu-id="b07fc-147">[Create Special Orders](sales-how-to-create-special-orders.md)|</span></span>  
[<span data-ttu-id="b07fc-148">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="b07fc-148">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="b07fc-149">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b07fc-149">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

