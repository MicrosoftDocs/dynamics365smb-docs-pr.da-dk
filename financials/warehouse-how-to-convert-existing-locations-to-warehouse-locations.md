---
title: "Sådan konverteres eksisterende lokationer til lagerlokationer | Microsoft Docs"
description: Du kan aktivere en eksisterende lagerlokation til at anvende zoner og placeringer og til at fungere som en lagerlokation.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7d4b2c86174386faa86ab6c09faa463d26d3d2ac
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="convert-existing-locations-to-warehouse-locations"></a><span data-ttu-id="aabe2-103">Konvertere eksisterende lokationer til lagerlokationer</span><span class="sxs-lookup"><span data-stu-id="aabe2-103">Convert Existing Locations to Warehouse Locations</span></span>
<span data-ttu-id="aabe2-104">Du kan aktivere en eksisterende lagerlokation til at anvende zoner og placeringer og til at fungere som en lagerlokation.</span><span class="sxs-lookup"><span data-stu-id="aabe2-104">You can enable an existing inventory location to use zones and bins and to operate as a warehouse location.</span></span>  

<span data-ttu-id="aabe2-105">Kørslen, der aktiverer en lokation til lagerhåndteringen, opretter lagerposter til lagerreguleringsplaceringen for alle varer med et lager på lokationen.</span><span class="sxs-lookup"><span data-stu-id="aabe2-105">The batch job to enable a location for warehouse operation creates initial warehouse entries for the warehouse adjustment bin for all items that have inventory in the location.</span></span> <span data-ttu-id="aabe2-106">De første poster afstemmes, når lagerstedets fysiske lagerposter bogføres, efter at kørslen er udført.</span><span class="sxs-lookup"><span data-stu-id="aabe2-106">These initial entries will be balanced when warehouse physical inventory entries are entered after the batch job is run.</span></span>  

<span data-ttu-id="aabe2-107">Du kan oprette zoner og placeringer enten før eller efter konverteringen.</span><span class="sxs-lookup"><span data-stu-id="aabe2-107">You can create zones and bins either before or after the conversion.</span></span> <span data-ttu-id="aabe2-108">Den eneste placering, som du skal oprette inden konverteringen, er den, som skal anvendes som fremtidig reguleringsplacering.</span><span class="sxs-lookup"><span data-stu-id="aabe2-108">The only bin that you must create before the conversion is the one that is to be used as the future adjustment bin.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="aabe2-109">Du kan rydde alt negativt lager og alle åbne lagerdokumenter, før du konverterer lokationen for lagerekspedition ved at køre en rapport for at identificere varer med negativt lager og åbne lagerdokumenter, der hører til lokationen.</span><span class="sxs-lookup"><span data-stu-id="aabe2-109">To clear all negative inventory and any open warehouse documents before you convert the location for warehouse handling, run a report to identify the items with negative inventory and open warehouse documents for the location.</span></span> <span data-ttu-id="aabe2-110">Du kan finde flere oplysninger i Kontroller for negativt lager.</span><span class="sxs-lookup"><span data-stu-id="aabe2-110">For more information, see Check on Negative Inventory.</span></span>  

## <a name="to-enable-an-existing-location-to-operate-as-a-warehouse-location"></a><span data-ttu-id="aabe2-111">Sådan aktiveres en eksisterende lokation til at fungere som en lagerlokation</span><span class="sxs-lookup"><span data-stu-id="aabe2-111">To enable an existing location to operate as a warehouse location</span></span>  
1.  <span data-ttu-id="aabe2-112">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opret lagerlokation**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="aabe2-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Create Warehouse Location**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="aabe2-113">I feltet **Lokationskode** skal du angive den lokation, du vil aktivere til behandling af lageret.</span><span class="sxs-lookup"><span data-stu-id="aabe2-113">In the **Location Code** field, specify the location that you want to enable for warehouse processing.</span></span>  
3.  <span data-ttu-id="aabe2-114">I feltet **Reguleringsplaceringskode** skal du angive placeringen på den lokation, hvor ikke-synkroniserede lagerposter gemmes.</span><span class="sxs-lookup"><span data-stu-id="aabe2-114">In the **Adjustment Bin Code** field, specify the bin at the location where unsynchronized warehouse entries are stored.</span></span> <span data-ttu-id="aabe2-115">Du kan finde flere oplysninger i afsnittet "Sådan synkroniseres de regulerede lagerposter med de relaterede vareposter" i [Tælle, justere og ompostere lager](inventory-how-count-adjust-reclassify.md).</span><span class="sxs-lookup"><span data-stu-id="aabe2-115">For more information, see the "To synchronize the adjusted warehouse entries with the related item ledger entries" section in [Count, Adjust, and Reclassify Inventory](inventory-how-count-adjust-reclassify.md).</span></span>  

    <span data-ttu-id="aabe2-116">Ved hjælp af åbne vareposter til den angivne lokation oprettes lagerkladdelinjer, der summerer hver kombination af Varenr., Variantkode, Enhedskode, og hvis det er relevant, Partinr. og Serienr. i vareposterne.</span><span class="sxs-lookup"><span data-stu-id="aabe2-116">Using the open item ledger entries for the specified location, warehouse journal lines are created that sum up every combination of Item No., Variant Code, Unit of Measure Code, and, if necessary, Lot No. and Serial No. in the item ledger entries.</span></span> <span data-ttu-id="aabe2-117">Derefter bogføres lagerkladdelinjerne.</span><span class="sxs-lookup"><span data-stu-id="aabe2-117">The warehouse journal lines are then posted.</span></span> <span data-ttu-id="aabe2-118">Denne bogføring opretter lagerposter, som placerer lageret i lagerreguleringsplaceringen.</span><span class="sxs-lookup"><span data-stu-id="aabe2-118">This posting creates warehouse entries that place the inventory in the warehouse adjustment bin.</span></span> <span data-ttu-id="aabe2-119">**Reguleringsplaceringskoden** på lokationskortet er også angivet.</span><span class="sxs-lookup"><span data-stu-id="aabe2-119">The **Adjustment Bin Code** on the location card is also set.</span></span>  

4.  <span data-ttu-id="aabe2-120">Hvis du vil se, hvilke varer der er føjet til reguleringsplaceringen, kan du køre rapporten **Regul.placering (logistik)**.</span><span class="sxs-lookup"><span data-stu-id="aabe2-120">To see which items were added to the adjustment bin during the batch job, run the **Warehouse Adjustment Bin** report.</span></span>  
5.  <span data-ttu-id="aabe2-121">Når kørslen af **Opret lagerlokation** er afsluttet, skal du udføre og bogføre en lagerplaceringsopgørelseskladde.</span><span class="sxs-lookup"><span data-stu-id="aabe2-121">When the **Create Warehouse Location** batch job has completed, perform and post a warehouse physical inventory.</span></span> <span data-ttu-id="aabe2-122">Du kan finde flere oplysninger i [Tælle, justere og ompostere inventar](inventory-how-count-adjust-reclassify.md).</span><span class="sxs-lookup"><span data-stu-id="aabe2-122">For more information, see [Count, Adjust, and Reclassify Inventory](inventory-how-count-adjust-reclassify.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="aabe2-123">Det anbefales, at du udfører kørslen **Opret lagerlokation** på et tidspunkt, hvor det ikke influerer på det daglige arbejde i systemet.</span><span class="sxs-lookup"><span data-stu-id="aabe2-123">It is recommended that you run the **Create Warehouse Location** batch job at a time when it will not impact the daily work in the system.</span></span> <span data-ttu-id="aabe2-124">Denne opgave behandler hver post i **vareposttabellen**, og hvis der er et større antal vareposter, kan denne opgave tage flere timer.</span><span class="sxs-lookup"><span data-stu-id="aabe2-124">This job processes each entry in the **Item Ledger Entry** table, and if there are a large number of item ledger entries, the job can last several hours.</span></span>  

 <span data-ttu-id="aabe2-125">For lokationer, der ikke anvendte lageradministrationsdokumenter inden konverteringen, skal du genåbne og frigive alle kildedokumenter, der blev delvist modtaget eller delvist leveret inden konverteringen.</span><span class="sxs-lookup"><span data-stu-id="aabe2-125">For those locations that did not use warehouse management documents before the conversion, you must re-open and release any source documents that were partially received or partially shipped before the conversion.</span></span>  

## <a name="see-also"></a><span data-ttu-id="aabe2-126">Se også</span><span class="sxs-lookup"><span data-stu-id="aabe2-126">See Also</span></span>  
[<span data-ttu-id="aabe2-127">Logistik</span><span class="sxs-lookup"><span data-stu-id="aabe2-127">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="aabe2-128">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="aabe2-128">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="aabe2-129">[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="aabe2-129">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="aabe2-130">[Montagestyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="aabe2-130">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="aabe2-131">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="aabe2-131">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="aabe2-132">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="aabe2-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

