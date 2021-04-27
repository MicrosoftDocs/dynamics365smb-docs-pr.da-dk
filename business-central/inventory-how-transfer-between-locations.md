---
title: Overflytte varer mellem lagerlokationer | Microsoft Docs
description: Beskriver, hvordan du flytter lager fra ét sted eller lagersted til et andet enten med omposteringskladden eller overflytningsordrer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 008b9a50f2374b13e30114769520c7b18bba8e0e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785669"
---
# <a name="transfer-inventory-between-locations"></a><span data-ttu-id="5f3e4-103">Overflytte lagerbeholdning mellem lokationer</span><span class="sxs-lookup"><span data-stu-id="5f3e4-103">Transfer Inventory Between Locations</span></span>
<span data-ttu-id="5f3e4-104">Du kan overføre lagervarer mellem lokationer ved at oprette overflytningsordrer.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-104">You can transfer inventory items between locations by creating transfer orders.</span></span> <span data-ttu-id="5f3e4-105">Du kan også bruge vareomposteringskladden.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-105">Alternatively, you can use the item reclassification journal.</span></span>

<span data-ttu-id="5f3e4-106">Med overflytningsordrer leverer du den udgående overflytning fra én placering og modtager den indgående overflytning på en anden.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-106">With transfer orders, you ship the outbound transfer from one location and receive the inbound transfer at the other location.</span></span> <span data-ttu-id="5f3e4-107">Dette giver dig mulighed for at administrere de involverede lageraktiviteter og giver større sikkerhed for, at lagerantallet opdateres korrekt.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-107">This allows you to manage the involved warehouse activities and provides more certainty that inventory quantities are updated correctly.</span></span>

<span data-ttu-id="5f3e4-108">Med omposteringskladden skal du blot udfylde felterne **Lokationskode** og **Ny lokationskode**.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-108">With the reclassification journal, you simply fill in the **Location Code** and the **New Location Code** fields.</span></span> <span data-ttu-id="5f3e4-109">Når du bogfører kladden, justeres vareposterne på de pågældende lokationer.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-109">When you post the journal, the item ledger entries are adjusted at the locations in question.</span></span> <span data-ttu-id="5f3e4-110">Med denne metode administreres lageraktiviteter ikke.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-110">With this method, warehouse activities are not managed.</span></span>

> [!NOTE]  
>   <span data-ttu-id="5f3e4-111">Hvis du har varer, der er registreret i lagerbeholdningen uden en lokationskode, f.eks. fra et tidspunkt, hvor du kun havde ét lagersted, kan du ikke overføre disse varer ved hjælp af overflytningsordrer.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-111">If you have items recorded in your inventory without a location code, for example from a time when you only had one warehouse, then you cannot transfer those items using transfer orders.</span></span> <span data-ttu-id="5f3e4-112">I stedet skal du bruge omposteringskladden til at ompostere varerne fra en tom lokationskode til en faktisk lokationskode.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-112">Instead, you must use the reclassification journal to reclassify the items from a blank location code to an actual location code.</span></span>  <span data-ttu-id="5f3e4-113">Du kan finde flere oplysninger i trin 3 i [Sådan overflyttes varer i vareomposteringskladden](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal).</span><span class="sxs-lookup"><span data-stu-id="5f3e4-113">For more information, see step 3 in [To transfer items with the item reclassification journal](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal).</span></span>

<span data-ttu-id="5f3e4-114">Hvis du vil overflytte varer, skal lokationer og overflytningsruter oprettes.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-114">To transfer items, locations and transfer routes must be set up.</span></span> <span data-ttu-id="5f3e4-115">Der er flere oplysninger i [Opsætte lokationer](inventory-how-setup-locations.md).</span><span class="sxs-lookup"><span data-stu-id="5f3e4-115">For more information, see [Set Up Locations](inventory-how-setup-locations.md).</span></span>

## <a name="to-transfer-items-with-a-transfer-order"></a><span data-ttu-id="5f3e4-116">Såden overflyttes varer med en overflytningsordre</span><span class="sxs-lookup"><span data-stu-id="5f3e4-116">To transfer items with a transfer order</span></span>
1. <span data-ttu-id="5f3e4-117">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Overflytningsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="5f3e4-118">I sidehovedet på siden **Overflytningsordre** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-118">On the header of the **Transfer Order** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   <span data-ttu-id="5f3e4-119">Hvis du har udfyldt felterne **Transitkode**, **Speditørkode** og **Speditørservice** på siden **Overflytningsrutespec.**, udfyldes de tilsvarende felter på overflytningsordren automatisk, når du opretter overflytningsruten.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-119">If you have filled in the **In-Transit Code**, **Shipping Agent Code**, and **Shipping Agent Service** fields on the **Trans. Route Spec.** page when you set up the transfer route, then the corresponding fields on the transfer order are filled in automatically.</span></span>

    <span data-ttu-id="5f3e4-120">Når du udfylder feltet **Speditørservice** beregnes modtagelsesdatoen på den lokation, der overflyttes til, ved at lægge speditørens transporttid til afsendelsesdatoen.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-120">When you fill in the **Shipping Agent Service** field, the receipt date at the transfer-to location is calculated by adding the shipping time of the shipping agent service to the shipment date.</span></span>

3. <span data-ttu-id="5f3e4-121">Du udfylder linjerne ved enten at angive dem manuelt eller ved at vælge en af følgende indstillinger under handlingen **Funktioner**:</span><span class="sxs-lookup"><span data-stu-id="5f3e4-121">To fill in the lines, either enter them manually or choose one of the following options on the under the **Functions** action:</span></span>
    - <span data-ttu-id="5f3e4-122">Vælg handlingen **Hent placeringsindhold** for at vælge eksisterende varer fra en bestemt placering på lokationen.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-122">Choose the **Get Bin Content** action to select existing items from a specific bin at the location.</span></span>
    - <span data-ttu-id="5f3e4-123">Vælg **Hent købsleverancelinjer** for at vælge varer, der lige er ankommet på den lokation, der overflyttes fra.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-123">Choose the **Get Receipt Lines** to select items that have just arrived at the transfer-from location.</span></span>   

    <span data-ttu-id="5f3e4-124">Fortsæt med at levere varerne som lagermedarbejder på den lokation, der overflyttes fra.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-124">As a warehouse worker at the transfer-from location, proceed to ship the items.</span></span>
4. <span data-ttu-id="5f3e4-125">Vælg handlingen **Bogfør**, vælg indstillingen **Lever**, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-125">Choose the **Post** action, choose the **Ship** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="5f3e4-126">Varerne er nu i transit mellem de angivne lokationer i overensstemmelse med den angivne overflytningsrute.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-126">The items are now in transit between the specified locations, according to the specifies transfer route.</span></span>

    <span data-ttu-id="5f3e4-127">Fortsæt ved at modtage varerne som lagermedarbejder på den lokation, der overflyttes fra.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-127">As a warehouse worker at the transfer-from location, proceed to receive the items.</span></span> <span data-ttu-id="5f3e4-128">Overflytningsordrelinjerne er de samme som ved levering og kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-128">The transfer order lines are the same as when shipped and cannot be edited.</span></span>
5. <span data-ttu-id="5f3e4-129">Vælg handlingen **Bogfør**, vælg indstillingen **Modtag**, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-129">Choose the **Post** action, choose the **Receive** option, and then choose the **OK** button.</span></span>

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a><span data-ttu-id="5f3e4-130">Sådan overflyttes varer i vareomposteringskladden</span><span class="sxs-lookup"><span data-stu-id="5f3e4-130">To transfer items with the item reclassification journal</span></span>
1. <span data-ttu-id="5f3e4-131">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Vareomposteringskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Reclass. Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="5f3e4-132">På siden **Vareomposteringskladder** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-132">On the **Item Reclass. Journal** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="5f3e4-133">I feltet **Lokationskode** skal du indtaste den lokation, hvor varerne opbevares i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-133">In the **Location Code** field, enter the location where the items are currently stored.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="5f3e4-134">For at overflytte varer, der ikke har en lokationskode, skal du lade feltet **Lokationskode** stå tomt.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-134">To transfer items that have no location code, leave the **Location Code** field blank.</span></span>
4. <span data-ttu-id="5f3e4-135">I feltet **Ny lokationskode** skal du angive den lokation, som du vil overflytte varerne til.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-135">In the **New Location Code** field, enter the location that you want to transfer the items to.</span></span>
5. <span data-ttu-id="5f3e4-136">Vælg handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="5f3e4-136">Choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="5f3e4-137">Se også</span><span class="sxs-lookup"><span data-stu-id="5f3e4-137">See Also</span></span>
[<span data-ttu-id="5f3e4-138">Administrere lager</span><span class="sxs-lookup"><span data-stu-id="5f3e4-138">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="5f3e4-139">Opsætte lokationer</span><span class="sxs-lookup"><span data-stu-id="5f3e4-139">Set Up Locations</span></span>](inventory-how-setup-locations.md)  
<span data-ttu-id="5f3e4-140">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5f3e4-140">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="5f3e4-141">Ændre, hvilke funktioner der vises</span><span class="sxs-lookup"><span data-stu-id="5f3e4-141">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="5f3e4-142">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="5f3e4-142">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]