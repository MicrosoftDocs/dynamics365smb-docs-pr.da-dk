---
title: Oprette et lokationskort og definere overflytningsruter
description: Du kan oprette et lokationskort for hvert sted, du gemme lagervarer, for eksempel et lagersted eller distributionscenter, og definere ruter for at overflytte varer mellem lokationerne.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/01/2021
ms.author: edupont
ms.openlocfilehash: 0319f0c64dd46610aa82705257091bd9478ac14f
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184320"
---
# <a name="set-up-locations"></a><span data-ttu-id="9bedf-103">Opsætte lokationer</span><span class="sxs-lookup"><span data-stu-id="9bedf-103">Set Up Locations</span></span>

<span data-ttu-id="9bedf-104">Hvis du køber, gemme eller sælger varer i mere end ét område eller lagersted, skal du oprette hver lokation med et lokationskort og definere overflytningsruter.</span><span class="sxs-lookup"><span data-stu-id="9bedf-104">If you buy, store, or sell items at more than one place or warehouse, you must set up each location with a location card and define transfer routes.</span></span> <span data-ttu-id="9bedf-105">[!INCLUDE [prod_short](includes/prod_short.md)] bruger lokationer til at holde styr på lagerbeholdningen i begge enkle sager og de mere komplekse lagerprocesser.</span><span class="sxs-lookup"><span data-stu-id="9bedf-105">[!INCLUDE [prod_short](includes/prod_short.md)] uses locations to help keep track of inventory in both simpler cases and the more complex warehouse processes.</span></span>

<span data-ttu-id="9bedf-106">Du kan derefter oprette dokumentlinjer for en bestemt lokation vis tilgængeligehed pr. lokation og vare samt overføre lagerbeholdning mellem lokationer.</span><span class="sxs-lookup"><span data-stu-id="9bedf-106">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="9bedf-107">Der er flere oplysninger i [Administrere lager](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="9bedf-107">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a><span data-ttu-id="9bedf-108">Lokationskort</span><span class="sxs-lookup"><span data-stu-id="9bedf-108">Location cards</span></span>

<span data-ttu-id="9bedf-109">Lokationskortet angiver oplysninger om en lokation, f. eks. et lager eller distributionscenter.</span><span class="sxs-lookup"><span data-stu-id="9bedf-109">The location card specifies information about a location, such as a warehouse or distribution center.</span></span> <span data-ttu-id="9bedf-110">Du kan give hver lokation et navn og en kode, der repræsenterer lokationen.</span><span class="sxs-lookup"><span data-stu-id="9bedf-110">You give each location a name and a code that represents the location.</span></span> <span data-ttu-id="9bedf-111">Du kan derefter angive lokationskoden i andre dele af programmet, når du vil registrere transaktioner for en given lokation.</span><span class="sxs-lookup"><span data-stu-id="9bedf-111">You can then enter the location code in other parts of the program when you want to record transactions for a given location.</span></span>  

<span data-ttu-id="9bedf-112">Du kan angive oplysninger om placeringer og lagermetoder.</span><span class="sxs-lookup"><span data-stu-id="9bedf-112">You can enter information about bins and warehouse policies for each location.</span></span> <span data-ttu-id="9bedf-113">På baggrund af de valgte lagermetoder kan du bruge indstillingerne i oversigtspanelet **Placeringer** til at definere de placeringer, der skal bruges som standardplaceringer, når du udfører transaktioner.</span><span class="sxs-lookup"><span data-stu-id="9bedf-113">Based on the warehouse policies you select, you can use the options on the **Bins** FastTab to define the bins that will be used as default bins when you are performing transactions.</span></span> <span data-ttu-id="9bedf-114">Hvis du bruger styret læg-på-lager og pluk, kan du bruge de fleste af indstillingerne i oversigtspanelet **Plac.metode** til at definere, hvordan du vil bruge de forskellige avancerede lagerfunktioner.</span><span class="sxs-lookup"><span data-stu-id="9bedf-114">If you are using directed put-away and pick, you use most of the options on the **Bin Policies** FastTab to define how you would like to use the various advanced warehousing features.</span></span>  

<span data-ttu-id="9bedf-115">Nogle indstillingsfelter er gråtonede og deaktiveret af andre indstillinger i vinduet **Lokationskort** for at forhindre ikke-understøttede opsætningskombinationer.</span><span class="sxs-lookup"><span data-stu-id="9bedf-115">Some option fields are grayed and disabled by other settings in the **Location Card** page to restrict unsupported setup combinations.</span></span>  

<span data-ttu-id="9bedf-116">Luk handlingen **Zoner** eller **Placeringer** for at få vist oplysninger om zoner og placeringer, der kan være defineret for den pågældende lokation.</span><span class="sxs-lookup"><span data-stu-id="9bedf-116">Choose the **Zones** or **Bins** action to view information about zones and bins that may be defined for the location.</span></span>

### <a name="to-create-a-location-card"></a><span data-ttu-id="9bedf-117">Sådan oprettes et lokationskort</span><span class="sxs-lookup"><span data-stu-id="9bedf-117">To create a location card</span></span>

1. <span data-ttu-id="9bedf-118">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lokationer**, og vælg derefter det tilknyttede link.</span><span class="sxs-lookup"><span data-stu-id="9bedf-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="9bedf-119">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9bedf-119">Choose the **New** action.</span></span>
3. <span data-ttu-id="9bedf-120">På siden **Lokationskort** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="9bedf-120">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="9bedf-121">Gentag trin 2 og 3 for hver lokation, hvor du vil foretage lageropgørelse.</span><span class="sxs-lookup"><span data-stu-id="9bedf-121">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="9bedf-122">Mange af felterne på lokationskortet henviser til håndtering af varer i indgående og udgående lagerprocesser.</span><span class="sxs-lookup"><span data-stu-id="9bedf-122">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="9bedf-123">Felterne er ikke relevante for virksomheder, der ikke har brug for mere komplekse lagerfunktioner.</span><span class="sxs-lookup"><span data-stu-id="9bedf-123">The fields are not relevant for companies that do not require the more complex warehouse functionality.</span></span> <span data-ttu-id="9bedf-124">Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="9bedf-124">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

<span data-ttu-id="9bedf-125">Du kan ændre konfigurationen for en lokation senere, men du kan ikke redigere opsætningen af lokationer, der har vareposter.</span><span class="sxs-lookup"><span data-stu-id="9bedf-125">You can change the configuration of a location later, but you cannot edit the setup of locations that have item ledger entries.</span></span>  

<span data-ttu-id="9bedf-126">Hvis du har flere lokationer, kan du definere overflytningsruter mellem lokationer.</span><span class="sxs-lookup"><span data-stu-id="9bedf-126">Next, if you have multiple locations, you can define transfer routes between locations.</span></span>  

### <a name="to-create-a-transfer-route"></a><span data-ttu-id="9bedf-127">Sådan oprettes en overflytningsrute</span><span class="sxs-lookup"><span data-stu-id="9bedf-127">To create a transfer route</span></span>

1. <span data-ttu-id="9bedf-128">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Overflytningsruter**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="9bedf-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="9bedf-129">Du kan også vælge handlingen **Overflytningsruter** på enhver **Lokationskort**-side.</span><span class="sxs-lookup"><span data-stu-id="9bedf-129">Alternatively, from any **Location Card** page, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="9bedf-130">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9bedf-130">Choose the **New** action.</span></span>
4. <span data-ttu-id="9bedf-131">På siden **Lokationskort** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="9bedf-131">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="9bedf-132">Du kan nu overflytte lagervarer mellem to lokationer.</span><span class="sxs-lookup"><span data-stu-id="9bedf-132">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="9bedf-133">Du kan finde flere oplysninger i [Overflytte lagerbeholdning mellem lokationer](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="9bedf-133">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="bins"></a><span data-ttu-id="9bedf-134">Placering</span><span class="sxs-lookup"><span data-stu-id="9bedf-134">Bins</span></span>

<span data-ttu-id="9bedf-135">Placeringer udgør den grundlæggende lagerstruktur og bruges til at fremsætte forslag om placeringen af varer.</span><span class="sxs-lookup"><span data-stu-id="9bedf-135">Bins represent the basic warehouse structure and are used to make suggestions about the placement of items.</span></span> <span data-ttu-id="9bedf-136">Når du har oprettet placeringerne, kan du meget præcist definere det indhold, du vil placere på hver placering, eller placeringen kan fungere som en løs placering uden angivet indhold.</span><span class="sxs-lookup"><span data-stu-id="9bedf-136">When you have created your bins, you can define precisely the contents that you want to place in each bin, or the bin can function as a floating bin without specified contents.</span></span> <span data-ttu-id="9bedf-137">Placeringer anvendes primært i basis-og forudlager operationer.</span><span class="sxs-lookup"><span data-stu-id="9bedf-137">Bins are predominantly used in basic and advance warehouse operations.</span></span> <span data-ttu-id="9bedf-138">Hvis du administrerer lagerbeholdningen i en mere simpel opsætning, har du sandsynligvis ikke brug for placeringer.</span><span class="sxs-lookup"><span data-stu-id="9bedf-138">If you manage inventory in a more simple setup, you probably do not need bins.</span></span>

<span data-ttu-id="9bedf-139">Hvis du vil bruge placeringsfunktionen på en lokation, skal du først aktivere funktionen på **Lokationer**-kortet ved at vælge feltet **Tvungen placering** i oversigtspanelet **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="9bedf-139">To use the bin functionality at a location, you first activate the functionality on the **Location** card by selecting the **Bins Mandatory** field on the **Warehouse** FastTab.</span></span> <span data-ttu-id="9bedf-140">Derefter kan du designe varestrømmen på placeringen ved at angive placeringskoder i konfigurationsfelter, der repræsenterer forskellige strømme.</span><span class="sxs-lookup"><span data-stu-id="9bedf-140">Then you design the item flow at the location by specifying bin codes in setup fields that represent the different flows.</span></span>

> [!NOTE]
> <span data-ttu-id="9bedf-141">Placeringskoderne skal være oprettet, før du kan angive placeringskoder på lokationskortet.</span><span class="sxs-lookup"><span data-stu-id="9bedf-141">Before you can specify bin codes on the location card, the bin codes must be created.</span></span>

<span data-ttu-id="9bedf-142">Du kan finde flere oplysninger i [Oprette placeringer](warehouse-how-to-create-individual-bins.md) og [Oprette placeringstyper](warehouse-how-to-set-up-bin-types.md).</span><span class="sxs-lookup"><span data-stu-id="9bedf-142">For more information, see [Create Bins](warehouse-how-to-create-individual-bins.md) and [Set Up Bin Types](warehouse-how-to-set-up-bin-types.md).</span></span>  

## <a name="zones"></a><span data-ttu-id="9bedf-143">Zoner</span><span class="sxs-lookup"><span data-stu-id="9bedf-143">Zones</span></span>

<span data-ttu-id="9bedf-144">Hvis du vil strukturere placeringerne under zoner, kan du gøre det på siden **Zoner**.</span><span class="sxs-lookup"><span data-stu-id="9bedf-144">If you want to structure your bins under zones, you can do that in the **Zones** page.</span></span>

<span data-ttu-id="9bedf-145">[!INCLUDE [prod_short](includes/prod_short.md)] kopierer de felter, som du definerer i forbindelse med en bestemt zone, kopieres til placeringerne i denne.</span><span class="sxs-lookup"><span data-stu-id="9bedf-145">[!INCLUDE [prod_short](includes/prod_short.md)] copies the fields that you set for any particular zone to the bins within it.</span></span> <span data-ttu-id="9bedf-146">Det betyder, at du kan knytte en zone til en placering eller placeringsskabelon (vha. et placeringsoprettelsesfilter), så programmet udfylder en række andre felter automatisk.</span><span class="sxs-lookup"><span data-stu-id="9bedf-146">This way, you can assign a zone to a bin or a bin template (bin creation filter), and several other fields are then filled in automatically.</span></span>

<span data-ttu-id="9bedf-147">Du kan også vælge kun at oprette en enkelt zone og udelukkende organisere lagerstedet efter placeringer.</span><span class="sxs-lookup"><span data-stu-id="9bedf-147">However, you can choose to set up just one zone and to organize your warehouse according to bins alone.</span></span> <span data-ttu-id="9bedf-148">Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="9bedf-148">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="9bedf-149">Se også</span><span class="sxs-lookup"><span data-stu-id="9bedf-149">See Also</span></span>

[<span data-ttu-id="9bedf-150">Administrere lager</span><span class="sxs-lookup"><span data-stu-id="9bedf-150">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="9bedf-151">Overflytte lagerbeholdning mellem lokationer</span><span class="sxs-lookup"><span data-stu-id="9bedf-151">Transfer Inventory Between Locations</span></span>](inventory-how-transfer-between-locations.md)  
[<span data-ttu-id="9bedf-152">Oprette placeringer</span><span class="sxs-lookup"><span data-stu-id="9bedf-152">Create Bins</span></span>](warehouse-how-to-create-individual-bins.md)  
[<span data-ttu-id="9bedf-153">Oprette placeringstyper</span><span class="sxs-lookup"><span data-stu-id="9bedf-153">Set Up Bin Types</span></span>](warehouse-how-to-set-up-bin-types.md)  
[<span data-ttu-id="9bedf-154">Sådan konfigureres logistikfunktioner</span><span class="sxs-lookup"><span data-stu-id="9bedf-154">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
<span data-ttu-id="9bedf-155">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9bedf-155">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="9bedf-156">Ændre, hvilke funktioner der vises</span><span class="sxs-lookup"><span data-stu-id="9bedf-156">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="9bedf-157">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="9bedf-157">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]