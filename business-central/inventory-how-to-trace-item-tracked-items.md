---
title: Spore vare via varesporing
description: Du kan se, hvor en vare med varesporing blev brugt, herunder hvordan og hvornår den blev modtaget eller fremstillet, overflyttet, solgt, forbrugt eller returneret. Du kan også finde alle aktuelle forekomster af et bestemt serienummer eller lotnummer i databasen. Du kan gøre dette ved hjælp af funktionerne Varesporing og Find poster.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: a425b974bf37b440de27f2b469694f9e8eac07de
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785694"
---
# <a name="trace-item-tracked-items"></a><span data-ttu-id="79b22-105">Spore vare via varesporing</span><span class="sxs-lookup"><span data-stu-id="79b22-105">Trace Item-Tracked Items</span></span>
<span data-ttu-id="79b22-106">Du kan se, hvor en vare med varesporing er brugt, herunder hvordan og hvornår den blev modtaget eller fremstillet, overflyttet, solgt, forbrugt eller returneret.</span><span class="sxs-lookup"><span data-stu-id="79b22-106">You can see where an item-tracked item was used, including how and when it was received or produced, transferred, sold, consumed, or returned.</span></span> <span data-ttu-id="79b22-107">Du kan også finde alle aktuelle forekomster af et bestemt serienummer eller lotnummer i databasen.</span><span class="sxs-lookup"><span data-stu-id="79b22-107">You can also find all current instances of a specific serial or lot number in the database.</span></span> <span data-ttu-id="79b22-108">Du kan gøre dette ved hjælp af funktionerne Varesporing og [Find poster](ui-find-entries.md).</span><span class="sxs-lookup"><span data-stu-id="79b22-108">You do this by using the Item Tracing and the [Find Entries](ui-find-entries.md) features.</span></span>  

<span data-ttu-id="79b22-109">Disse funktioner kan især være praktiske i kvalitetskontrol, når du vil finde ud af, hvilke kunder der har modtaget produkter med et bestemt lotnummer, eller du vil finde ud af, hvilken lot en defekt komponent stammer fra.</span><span class="sxs-lookup"><span data-stu-id="79b22-109">These features can be particularly useful in quality control when you need to find out which customers received products with a particular lot number or when you need to find out which lot a defective component came from.</span></span>  

 <span data-ttu-id="79b22-110">Du kan spore fremad og bagud i en sekvens af bogførte lagertransaktioner for serie- eller lotnummer på siden **Varesporing**.</span><span class="sxs-lookup"><span data-stu-id="79b22-110">On the **Item Tracing** page, you can trace forwards and backwards in a sequence of posted inventory transactions for the serial or lot number.</span></span>  

 <span data-ttu-id="79b22-111">På siden **Find poster** kan du ikke se sekvensen af transaktioner, men du kan se alle poster for serie- eller lotnummeret, både bogførte poster og åbne poster.</span><span class="sxs-lookup"><span data-stu-id="79b22-111">On the **Find Entries** page, you cannot see the sequence of transactions, but you can see all records of the serial or lot number, both posted entries and open records.</span></span>  

 <span data-ttu-id="79b22-112">De to funktioner kan bruges i kombination ved at overføre sporede serienummer eller lotnummer til siden **Find poster** for at afslutte et komplet sporingsscenarie.</span><span class="sxs-lookup"><span data-stu-id="79b22-112">The two features can be used in combination by transferring a traced serial or lot number to the **Find Entries** page to finish a complete trace scenario.</span></span> <span data-ttu-id="79b22-113">Du kan finde flere oplysninger i [Gennemgang: Sporing af serie-/lotnumre](walkthrough-tracing-serial-lot-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="79b22-113">For more information, see [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).</span></span>  

## <a name="to-trace-item-tracked-items"></a><span data-ttu-id="79b22-114">Sådan spores varer via varesporing</span><span class="sxs-lookup"><span data-stu-id="79b22-114">To trace item-tracked items</span></span>  

1.  <span data-ttu-id="79b22-115">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varesporing**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="79b22-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Tracing**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="79b22-116">Du kan angive bestemte varenumre i filterfelterne øverst på siden, eller du kan angive et filter for et interval af de varenumre, du vil spore.</span><span class="sxs-lookup"><span data-stu-id="79b22-116">In the filter fields at the top of the page, enter the specific item numbers or a filter on the item numbers that you would like to trace.</span></span>  
3.  <span data-ttu-id="79b22-117">I feltet **Vis komponenter** kan du vælge, om du også vil se, hvor komponenterne til varerne stammer fra.</span><span class="sxs-lookup"><span data-stu-id="79b22-117">In the **Show Components** field, select whether you would like to also see where the components for the items came from.</span></span> <span data-ttu-id="79b22-118">Der er følgende indstillinger i feltet.</span><span class="sxs-lookup"><span data-stu-id="79b22-118">Your options in this field are as follows.</span></span>  

    |<span data-ttu-id="79b22-119">Felt</span><span class="sxs-lookup"><span data-stu-id="79b22-119">Field</span></span>|<span data-ttu-id="79b22-120">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="79b22-120">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="79b22-121">**Nej**</span><span class="sxs-lookup"><span data-stu-id="79b22-121">**No**</span></span>|<span data-ttu-id="79b22-122">Vælg denne indstilling, hvis du ikke vil have vist nogen komponenter.</span><span class="sxs-lookup"><span data-stu-id="79b22-122">Select this option if you do not want to see any components.</span></span>|  
    |<span data-ttu-id="79b22-123">**Kun varesporing**</span><span class="sxs-lookup"><span data-stu-id="79b22-123">**Item-tracked Only**</span></span>|<span data-ttu-id="79b22-124">Vælg denne indstilling, hvis du kun vil se de komponenter, der har lot- eller serienumre.</span><span class="sxs-lookup"><span data-stu-id="79b22-124">Select this option if you want to see only components that have lot or serial numbers.</span></span>|  
    |<span data-ttu-id="79b22-125">**Alle**</span><span class="sxs-lookup"><span data-stu-id="79b22-125">**All**</span></span>|<span data-ttu-id="79b22-126">Vælg denne indstilling, hvis du vil se alle komponenter.</span><span class="sxs-lookup"><span data-stu-id="79b22-126">Select this option if you want to see all components.</span></span>|  

4.  <span data-ttu-id="79b22-127">Vælg den metode i feltet **Sporingsmetode**, du vil bruge til sporing af varen.</span><span class="sxs-lookup"><span data-stu-id="79b22-127">In the **Trace Method** field, select the method you would like to use for tracing the item.</span></span> <span data-ttu-id="79b22-128">Der findes følgende indstillinger</span><span class="sxs-lookup"><span data-stu-id="79b22-128">The options are as follows</span></span>  

    |<span data-ttu-id="79b22-129">Felt</span><span class="sxs-lookup"><span data-stu-id="79b22-129">Field</span></span>|<span data-ttu-id="79b22-130">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="79b22-130">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="79b22-131">**Forbrug->Oprindelse**</span><span class="sxs-lookup"><span data-stu-id="79b22-131">**Usage->Origin**</span></span>|<span data-ttu-id="79b22-132">Denne metode sporer varen ved at starte med, hvor den blev brugt til, hvor den kom fra.</span><span class="sxs-lookup"><span data-stu-id="79b22-132">This method traces the item starting from where it was used to where it came from.</span></span> <span data-ttu-id="79b22-133">Hvis f.eks. en produceret vare blev solgt til en debitor, viser siden **Varesporing** dette med salgsleverancelinjen først, som du derefter kan udvide, så du kan se, hvilken produktionsordre den kom fra.</span><span class="sxs-lookup"><span data-stu-id="79b22-133">For instance, if a manufactured item was sold to a customer, the **Item Tracing** page shows this with the sales shipment line first, which you can then expand to see from which production order it came.</span></span>|  
    |<span data-ttu-id="79b22-134">**Oprindelse->Forbrug**</span><span class="sxs-lookup"><span data-stu-id="79b22-134">**Origin->Usage**</span></span>|<span data-ttu-id="79b22-135">Denne metode sporer varen ved at starte med, hvor den ankommer til lageret, til hvor den blev brugt.</span><span class="sxs-lookup"><span data-stu-id="79b22-135">This method traces the item starting from where it came into inventory to where it was used.</span></span> <span data-ttu-id="79b22-136">Hvis f.eks. en produceret vare blev solgt til en debitor, viser siden **Varesporing** dette med den færdige produktionsordre først, som du derefter kan udvide, så du kan se, hvilken produktionsordre den kom fra.</span><span class="sxs-lookup"><span data-stu-id="79b22-136">For instance, if a manufactured item was sold to a customer, the **Item Tracing** page shows this with the finished production order first, which you can then expand to see sale shipment lines where the item was used.</span></span>|  

5.  <span data-ttu-id="79b22-137">Vælg handlingen **Sporing** for at udføre sporingen.</span><span class="sxs-lookup"><span data-stu-id="79b22-137">Choose the **Trace** action to run the trace.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="79b22-138">Hvis du har modtaget det samme parti på flere transaktioner, viser siden **Varesporing** måske ikke alle transaktioner.</span><span class="sxs-lookup"><span data-stu-id="79b22-138">If you have received the same lot on more transactions, then the **Item Tracing** page may not show all transactions.</span></span> <span data-ttu-id="79b22-139">Der vises kun de udlignede transaktioner.</span><span class="sxs-lookup"><span data-stu-id="79b22-139">Only applied transactions are shown.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="79b22-140">Hvis du allerede har sporet yderligere transaktionsoversigt under en varelinje fra en anden linje ovenfor, så vil afkrydsningsfeltet **Allerede sporet** være markeret.</span><span class="sxs-lookup"><span data-stu-id="79b22-140">If additional transaction history under an item tracing line has already been traced by another line above it, then the **Already Traced** check box is selected.</span></span> <span data-ttu-id="79b22-141">For at give en enklere visning, vises sådanne underliggende linjer ikke.</span><span class="sxs-lookup"><span data-stu-id="79b22-141">To provide a simpler view, such underlying lines are not shown.</span></span>  
>   
>  <span data-ttu-id="79b22-142">Hvis du vil finde de varesporingslinjer, hvor transaktionsoversigten allerede er sporet, skal du vælge knappen **Gå til allerede sporede**.</span><span class="sxs-lookup"><span data-stu-id="79b22-142">To find the item tracing lines where the transaction history has already been traced, choose the **Go to Already Traced** button.</span></span> <span data-ttu-id="79b22-143">Den pågældende varesporingslinje er markeret, og alle underliggende linjer er udvidet.</span><span class="sxs-lookup"><span data-stu-id="79b22-143">The item tracing line in question is selected, and all underlying lines are expanded.</span></span>  

## <a name="to-find-item-tracked-items-with-find-entries"></a><span data-ttu-id="79b22-144">Sådan findes varesporede varer med Find poster</span><span class="sxs-lookup"><span data-stu-id="79b22-144">To find item-tracked items with Find Entries</span></span>  

1. <span data-ttu-id="79b22-145">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Find poster**, og vælg derefter det tilknyttede link.</span><span class="sxs-lookup"><span data-stu-id="79b22-145">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then select the related link.</span></span>  
2. <span data-ttu-id="79b22-146">Vælg **Handlinger** > **Find efter** > **Søg efter varereference**.</span><span class="sxs-lookup"><span data-stu-id="79b22-146">Choose **Actions** > **Find by** > **Find by Item Reference**.</span></span>
3. <span data-ttu-id="79b22-147">I felterne **Serienr.** og **Lotnr.** skal du angive de varesporingsnumre, du ønsker at spore.</span><span class="sxs-lookup"><span data-stu-id="79b22-147">In the **Serial No.** and **Lot No.** fields, enter the item tracking numbers that you want to trace.</span></span>  
4. <span data-ttu-id="79b22-148">Vælg handlingen **Find** for at finde alle forekomster af serienummer eller lotnummer i databasen.</span><span class="sxs-lookup"><span data-stu-id="79b22-148">Choose the **Find** action to find all instances of the serial or lot number in the database.</span></span>  

## <a name="see-also"></a><span data-ttu-id="79b22-149">Se også</span><span class="sxs-lookup"><span data-stu-id="79b22-149">See Also</span></span>

[<span data-ttu-id="79b22-150">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="79b22-150">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="79b22-151">Arbejde med serie-, lot- og pakkenumre</span><span class="sxs-lookup"><span data-stu-id="79b22-151">Work with Serial, Lot, and Package Numbers</span></span>](inventory-how-work-item-tracking.md)  
[<span data-ttu-id="79b22-152">Designoplysninger: Varesporing</span><span class="sxs-lookup"><span data-stu-id="79b22-152">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)  
[<span data-ttu-id="79b22-153">Designoplysninger - Varesporing og reservationer</span><span class="sxs-lookup"><span data-stu-id="79b22-153">Design Details - Item Tracking and Reservations</span></span>](design-details-item-tracking-and-reservations.md)  
[<span data-ttu-id="79b22-154">Reservere varer</span><span class="sxs-lookup"><span data-stu-id="79b22-154">Reserve Items</span></span>](inventory-how-to-reserve-items.md)  
<span data-ttu-id="79b22-155">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="79b22-155">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="79b22-156">Gennemgang: Sporing af serie-/lotnumre</span><span class="sxs-lookup"><span data-stu-id="79b22-156">Walkthrough: Tracing Serial-Lot Numbers</span></span>](walkthrough-tracing-serial-lot-numbers.md)  
[<span data-ttu-id="79b22-157">Find poster</span><span class="sxs-lookup"><span data-stu-id="79b22-157">Find Entries</span></span>](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]