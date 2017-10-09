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
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 41804dc183f9fa05ec1599db34c2b4f76a790a72
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-transfer-inventory-between-locations"></a><span data-ttu-id="07618-103">Fremgangsmåde: Overflytte lagerbeholdning mellem lokationer</span><span class="sxs-lookup"><span data-stu-id="07618-103">How to: Transfer Inventory Between Locations</span></span>
<span data-ttu-id="07618-104">Du kan overføre lagervarer mellem lokationer ved at oprette overflytningsordrer.</span><span class="sxs-lookup"><span data-stu-id="07618-104">You can transfer inventory items between locations by creating transfer orders.</span></span> <span data-ttu-id="07618-105">Du kan også bruge vareomposteringskladden.</span><span class="sxs-lookup"><span data-stu-id="07618-105">Alternatively, you can use the item reclassification journal.</span></span>

<span data-ttu-id="07618-106">Med overflytningsordrer leverer du den udgående overflytning fra én placering og modtager den indgående overflytning på en anden.</span><span class="sxs-lookup"><span data-stu-id="07618-106">With transfer orders, you ship the outbound transfer from one location and receive the inbound transfer at the other location.</span></span> <span data-ttu-id="07618-107">Dette giver dig mulighed for at administrere de involverede lageraktiviteter og giver større sikkerhed for, at lagerantallet opdateres korrekt.</span><span class="sxs-lookup"><span data-stu-id="07618-107">This allows you to manage the involved warehouse activities and provides more certainty that inventory quantities are updated correctly.</span></span>

<span data-ttu-id="07618-108">Med omposteringskladden skal du blot udfylde felterne **Lokationskode** og **Ny lokationskode**.</span><span class="sxs-lookup"><span data-stu-id="07618-108">With the reclassification journal, you simply fill in the **Location Code** and the **New Location Code** fields.</span></span> <span data-ttu-id="07618-109">Når du bogfører kladden, justeres vareposterne på de pågældende lokationer.</span><span class="sxs-lookup"><span data-stu-id="07618-109">When you post the journal, the item ledger entries are adjusted at the locations in question.</span></span> <span data-ttu-id="07618-110">Med denne metode administreres lageraktiviteter ikke.</span><span class="sxs-lookup"><span data-stu-id="07618-110">With this method, warehouse activities are not managed.</span></span>

> [!NOTE]  
>   <span data-ttu-id="07618-111">Hvis du har varer, der er registreret i lagerbeholdningen uden en lokationskode, f.eks. fra et tidspunkt, hvor du kun havde ét lagersted, kan du ikke overføre disse varer ved hjælp af overflytningsordrer.</span><span class="sxs-lookup"><span data-stu-id="07618-111">If you have items recorded in your inventory without a location code, for example from a time when you only had one warehouse, then you cannot transfer those items using transfer orders.</span></span> <span data-ttu-id="07618-112">I stedet skal du bruge omposteringskladden til at ompostere varerne fra en tom lokationskode til en faktisk lokationskode.</span><span class="sxs-lookup"><span data-stu-id="07618-112">Instead, you must use the reclassification journal to reclassify the items from a blank location code to an actual location code.</span></span>  <span data-ttu-id="07618-113">Du kan finde flere oplysninger under trin 3 i afsnittet "Sådan overflyttes varer i vareomposteringskladden".</span><span class="sxs-lookup"><span data-stu-id="07618-113">For more information, see step 3 in the "To transfer items with the item reclassification journal" section.</span></span>

<span data-ttu-id="07618-114">Hvis du vil overflytte varer, skal lokationer og overflytningsruter oprettes.</span><span class="sxs-lookup"><span data-stu-id="07618-114">To transfer items, locations and transfer routes must be set up.</span></span> <span data-ttu-id="07618-115">Du kan finde flere oplysninger i [Fremgangsmåde: Opsætning af lokationer](inventory-how-setup-locations.md).</span><span class="sxs-lookup"><span data-stu-id="07618-115">For more information, see [How to: Set Up Locations](inventory-how-setup-locations.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="07618-116">Denne funktion kræver, at oplevelsen er indstillet til **Suite**.</span><span class="sxs-lookup"><span data-stu-id="07618-116">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="07618-117">Du kan finde flere oplysninger under [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="07618-117">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-transfer-items-with-a-transfer-order"></a><span data-ttu-id="07618-118">Såden overflyttes varer med en overflytningsordre</span><span class="sxs-lookup"><span data-stu-id="07618-118">To transfer items with a transfer order</span></span>
1. <span data-ttu-id="07618-119">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Overflytningsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="07618-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="07618-120">I vinduet **Overflytningsordre** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="07618-120">In the **Transfer Order** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
>   <span data-ttu-id="07618-121">Hvis du har udfyldt felterne **Transitkode**, **Speditørkode** og **Speditørservice** i vinduet **Overflytningsrutespec.**, udfyldes de tilsvarende felter på overflytningsordren automatisk, når du opretter overflytningsruten.</span><span class="sxs-lookup"><span data-stu-id="07618-121">If you have filled in the **In-Transit Code**, **Shipping Agent Code**, and **Shipping Agent Service** fields in the **Trans. Route Spec.** window when you set up the transfer route, then the corresponding fields on the transfer order are filled in automatically.</span></span>

    <span data-ttu-id="07618-122">Når du udfylder feltet **Speditørservice** beregnes modtagelsesdatoen på den lokation, der overflyttes til, ved at lægge speditørens transporttid til afsendelsesdatoen.</span><span class="sxs-lookup"><span data-stu-id="07618-122">When you fill in the **Shipping Agent Service** field, the receipt date at the transfer-to location is calculated by adding the shipping time of the shipping agent service to the shipment date.</span></span>

    <span data-ttu-id="07618-123">Fortsæt med at levere varerne som lagermedarbejder på den lokation, der overflyttes fra.</span><span class="sxs-lookup"><span data-stu-id="07618-123">As a warehouse worker at the transfer-from location, proceed to ship the items.</span></span>
3. <span data-ttu-id="07618-124">Vælg handlingen **Bogfør**, vælg indstillingen **Lever**, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="07618-124">Choose the **Post** action, choose the **Ship** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="07618-125">Varerne er nu i transit mellem de angivne lokationer i overensstemmelse med den angivne overflytningsrute.</span><span class="sxs-lookup"><span data-stu-id="07618-125">The items are now in transit between the specified locations, according to the specifies transfer route.</span></span>

    <span data-ttu-id="07618-126">Fortsæt ved at modtage varerne som lagermedarbejder på den lokation, der overflyttes fra.</span><span class="sxs-lookup"><span data-stu-id="07618-126">As a warehouse worker at the transfer-from location, proceed to receive the items.</span></span>
4. <span data-ttu-id="07618-127">Vælg handlingen **Bogfør**, vælg indstillingen **Modtag**, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="07618-127">Choose the **Post** action, choose the **Receive** option, and then choose the **OK** button.</span></span>

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a><span data-ttu-id="07618-128">Sådan overflyttes varer i vareomposteringskladden</span><span class="sxs-lookup"><span data-stu-id="07618-128">To transfer items with the item reclassification journal</span></span>
1. <span data-ttu-id="07618-129">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Vareomposteringskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="07618-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Reclass. Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="07618-130">I vinduet **Vareomposteringskladder** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="07618-130">In the **Item Reclass. Journal** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="07618-131">I feltet **Lokationskode** skal du indtaste den lokation, hvor varerne opbevares i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="07618-131">In the **Location Code** field, enter the location where the items are currently stored.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="07618-132">For at overflytte varer, der ikke har en lokationskode, skal du lade feltet **Lokationskode** stå tomt.</span><span class="sxs-lookup"><span data-stu-id="07618-132">To transfer items that have no location code, leave the **Location Code** field blank.</span></span>
4. <span data-ttu-id="07618-133">I feltet **Ny lokationskode** skal du angive den lokation, som du vil overflytte varerne til.</span><span class="sxs-lookup"><span data-stu-id="07618-133">In the **New Location Code** field, enter the location that you want to transfer the items to.</span></span>
5. <span data-ttu-id="07618-134">Vælg handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="07618-134">Choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="07618-135">Se også</span><span class="sxs-lookup"><span data-stu-id="07618-135">See Also</span></span>
[<span data-ttu-id="07618-136">Administrere lager</span><span class="sxs-lookup"><span data-stu-id="07618-136">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="07618-137">Sådan oprettes lokationer</span><span class="sxs-lookup"><span data-stu-id="07618-137">How to: Set Up Locations</span></span>](inventory-how-setup-locations.md)  
  
<span data-ttu-id="07618-138">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="07618-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="07618-139">[Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md)</span><span class="sxs-lookup"><span data-stu-id="07618-139">[Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md)</span></span>  
[<span data-ttu-id="07618-140">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="07618-140">General Business Functionality</span></span>](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
