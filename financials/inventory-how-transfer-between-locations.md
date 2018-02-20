---
title: Overflytte varer mellem lagerlokationer | Microsoft Docs
description: "Beskriver, hvordan du flytter lager fra ét sted eller lagersted til et andet enten med omposteringskladden eller overflytningsordrer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 01/25/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 8ee703865f86c0edcc5bff77d8bd04cc2bd107be
ms.contentlocale: da-dk
ms.lasthandoff: 02/02/2018

---
# <a name="transfer-inventory-between-locations"></a><span data-ttu-id="9e792-103">Overflytte lagerbeholdning mellem lokationer</span><span class="sxs-lookup"><span data-stu-id="9e792-103">Transfer Inventory Between Locations</span></span>
<span data-ttu-id="9e792-104">Du kan overføre lagervarer mellem lokationer ved at oprette overflytningsordrer.</span><span class="sxs-lookup"><span data-stu-id="9e792-104">You can transfer inventory items between locations by creating transfer orders.</span></span> <span data-ttu-id="9e792-105">Du kan også bruge vareomposteringskladden.</span><span class="sxs-lookup"><span data-stu-id="9e792-105">Alternatively, you can use the item reclassification journal.</span></span>

<span data-ttu-id="9e792-106">Med overflytningsordrer leverer du den udgående overflytning fra én placering og modtager den indgående overflytning på en anden.</span><span class="sxs-lookup"><span data-stu-id="9e792-106">With transfer orders, you ship the outbound transfer from one location and receive the inbound transfer at the other location.</span></span> <span data-ttu-id="9e792-107">Dette giver dig mulighed for at administrere de involverede lageraktiviteter og giver større sikkerhed for, at lagerantallet opdateres korrekt.</span><span class="sxs-lookup"><span data-stu-id="9e792-107">This allows you to manage the involved warehouse activities and provides more certainty that inventory quantities are updated correctly.</span></span>

<span data-ttu-id="9e792-108">Med omposteringskladden skal du blot udfylde felterne **Lokationskode** og **Ny lokationskode**.</span><span class="sxs-lookup"><span data-stu-id="9e792-108">With the reclassification journal, you simply fill in the **Location Code** and the **New Location Code** fields.</span></span> <span data-ttu-id="9e792-109">Når du bogfører kladden, justeres vareposterne på de pågældende lokationer.</span><span class="sxs-lookup"><span data-stu-id="9e792-109">When you post the journal, the item ledger entries are adjusted at the locations in question.</span></span> <span data-ttu-id="9e792-110">Med denne metode administreres lageraktiviteter ikke.</span><span class="sxs-lookup"><span data-stu-id="9e792-110">With this method, warehouse activities are not managed.</span></span>

> [!NOTE]  
>   <span data-ttu-id="9e792-111">Hvis du har varer, der er registreret i lagerbeholdningen uden en lokationskode, f.eks. fra et tidspunkt, hvor du kun havde ét lagersted, kan du ikke overføre disse varer ved hjælp af overflytningsordrer.</span><span class="sxs-lookup"><span data-stu-id="9e792-111">If you have items recorded in your inventory without a location code, for example from a time when you only had one warehouse, then you cannot transfer those items using transfer orders.</span></span> <span data-ttu-id="9e792-112">I stedet skal du bruge omposteringskladden til at ompostere varerne fra en tom lokationskode til en faktisk lokationskode.</span><span class="sxs-lookup"><span data-stu-id="9e792-112">Instead, you must use the reclassification journal to reclassify the items from a blank location code to an actual location code.</span></span>  <span data-ttu-id="9e792-113">Du kan finde flere oplysninger under trin 3 i afsnittet "Sådan overflyttes varer i vareomposteringskladden".</span><span class="sxs-lookup"><span data-stu-id="9e792-113">For more information, see step 3 in the "To transfer items with the item reclassification journal" section.</span></span>

<span data-ttu-id="9e792-114">Hvis du vil overflytte varer, skal lokationer og overflytningsruter oprettes.</span><span class="sxs-lookup"><span data-stu-id="9e792-114">To transfer items, locations and transfer routes must be set up.</span></span> <span data-ttu-id="9e792-115">Der er flere oplysninger i [Opsætte lokationer](inventory-how-setup-locations.md).</span><span class="sxs-lookup"><span data-stu-id="9e792-115">For more information, see [Set Up Locations](inventory-how-setup-locations.md).</span></span>

## <a name="to-transfer-items-with-a-transfer-order"></a><span data-ttu-id="9e792-116">Såden overflyttes varer med en overflytningsordre</span><span class="sxs-lookup"><span data-stu-id="9e792-116">To transfer items with a transfer order</span></span>
1. <span data-ttu-id="9e792-117">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Overflytningsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="9e792-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="9e792-118">I vinduet **Overflytningsordre** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="9e792-118">In the **Transfer Order** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
>   <span data-ttu-id="9e792-119">Hvis du har udfyldt felterne **Transitkode**, **Speditørkode** og **Speditørservice** i vinduet **Overflytningsrutespec.**, udfyldes de tilsvarende felter på overflytningsordren automatisk, når du opretter overflytningsruten.</span><span class="sxs-lookup"><span data-stu-id="9e792-119">If you have filled in the **In-Transit Code**, **Shipping Agent Code**, and **Shipping Agent Service** fields in the **Trans. Route Spec.** window when you set up the transfer route, then the corresponding fields on the transfer order are filled in automatically.</span></span>

    <span data-ttu-id="9e792-120">Når du udfylder feltet **Speditørservice** beregnes modtagelsesdatoen på den lokation, der overflyttes til, ved at lægge speditørens transporttid til afsendelsesdatoen.</span><span class="sxs-lookup"><span data-stu-id="9e792-120">When you fill in the **Shipping Agent Service** field, the receipt date at the transfer-to location is calculated by adding the shipping time of the shipping agent service to the shipment date.</span></span>

    <span data-ttu-id="9e792-121">Fortsæt med at levere varerne som lagermedarbejder på den lokation, der overflyttes fra.</span><span class="sxs-lookup"><span data-stu-id="9e792-121">As a warehouse worker at the transfer-from location, proceed to ship the items.</span></span>
3. <span data-ttu-id="9e792-122">Vælg handlingen **Bogfør**, vælg indstillingen **Lever**, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e792-122">Choose the **Post** action, choose the **Ship** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="9e792-123">Varerne er nu i transit mellem de angivne lokationer i overensstemmelse med den angivne overflytningsrute.</span><span class="sxs-lookup"><span data-stu-id="9e792-123">The items are now in transit between the specified locations, according to the specifies transfer route.</span></span>

    <span data-ttu-id="9e792-124">Fortsæt ved at modtage varerne som lagermedarbejder på den lokation, der overflyttes fra.</span><span class="sxs-lookup"><span data-stu-id="9e792-124">As a warehouse worker at the transfer-from location, proceed to receive the items.</span></span>
4. <span data-ttu-id="9e792-125">Vælg handlingen **Bogfør**, vælg indstillingen **Modtag**, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e792-125">Choose the **Post** action, choose the **Receive** option, and then choose the **OK** button.</span></span>

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a><span data-ttu-id="9e792-126">Sådan overflyttes varer i vareomposteringskladden</span><span class="sxs-lookup"><span data-stu-id="9e792-126">To transfer items with the item reclassification journal</span></span>
1. <span data-ttu-id="9e792-127">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Vareomposteringskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="9e792-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Reclass. Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="9e792-128">I vinduet **Vareomposteringskladder** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="9e792-128">In the **Item Reclass. Journal** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="9e792-129">I feltet **Lokationskode** skal du indtaste den lokation, hvor varerne opbevares i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="9e792-129">In the **Location Code** field, enter the location where the items are currently stored.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="9e792-130">For at overflytte varer, der ikke har en lokationskode, skal du lade feltet **Lokationskode** stå tomt.</span><span class="sxs-lookup"><span data-stu-id="9e792-130">To transfer items that have no location code, leave the **Location Code** field blank.</span></span>
4. <span data-ttu-id="9e792-131">I feltet **Ny lokationskode** skal du angive den lokation, som du vil overflytte varerne til.</span><span class="sxs-lookup"><span data-stu-id="9e792-131">In the **New Location Code** field, enter the location that you want to transfer the items to.</span></span>
5. <span data-ttu-id="9e792-132">Vælg handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="9e792-132">Choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e792-133">Se også</span><span class="sxs-lookup"><span data-stu-id="9e792-133">See Also</span></span>
[<span data-ttu-id="9e792-134">Administrere lager</span><span class="sxs-lookup"><span data-stu-id="9e792-134">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="9e792-135">Opsætte lokationer</span><span class="sxs-lookup"><span data-stu-id="9e792-135">Set Up Locations</span></span>](inventory-how-setup-locations.md)  

<span data-ttu-id="9e792-136">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9e792-136">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="9e792-137">[Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md)</span><span class="sxs-lookup"><span data-stu-id="9e792-137">[Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md)</span></span>  
[<span data-ttu-id="9e792-138">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="9e792-138">General Business Functionality</span></span>](ui-across-business-areas.md)

