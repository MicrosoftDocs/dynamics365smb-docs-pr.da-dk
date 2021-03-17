---
title: Designoplysninger – Oversigt over logistik | Microsoft Docs
description: Alle oplysninger skal spores for hver transaktion eller bevægelse på lageret for at understøtte den fysiske håndtering af varerne på zone- og placeringsniveauet. Dette administreres i tabellen **Lagerpost**. Hver transaktion gemmes i en lagerjournal.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cfbc130f1e67bb1c6ac8886590cf14e5d5077731
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377794"
---
# <a name="design-details-warehouse-overview"></a><span data-ttu-id="4c914-105">Designoplysninger: Oversigt over logistik</span><span class="sxs-lookup"><span data-stu-id="4c914-105">Design Details: Warehouse Overview</span></span>
<span data-ttu-id="4c914-106">Alle oplysninger skal spores for hver transaktion eller bevægelse på lageret for at understøtte den fysiske håndtering af varerne på zone- og placeringsniveauet.</span><span class="sxs-lookup"><span data-stu-id="4c914-106">To support the physical handling of items on the zone and bin level, all information must be traced for each transaction or movement in the warehouse.</span></span> <span data-ttu-id="4c914-107">Dette administreres i tabellen **Lagerpost**.</span><span class="sxs-lookup"><span data-stu-id="4c914-107">This is managed in the **Warehouse Entry** table.</span></span> <span data-ttu-id="4c914-108">Hver transaktion gemmes i en lagerjournal.</span><span class="sxs-lookup"><span data-stu-id="4c914-108">Each transaction is stored in a warehouse register.</span></span>  

<span data-ttu-id="4c914-109">Lagerdokumenter og en lagerkladde bruges til at registrere varebevægelser på lageret.</span><span class="sxs-lookup"><span data-stu-id="4c914-109">Warehouse documents and a warehouse journal are used to register item movements in the warehouse.</span></span> <span data-ttu-id="4c914-110">Hver gang en vare på lageret flyttes, modtages, lægges på lager, plukkes, leveres eller reguleres, registreres lagerposter for at gemme de fysiske oplysninger om zone, placering og antal.</span><span class="sxs-lookup"><span data-stu-id="4c914-110">Every time that an item in the warehouse is moved, received, put away, picked, shipped, or adjusted, warehouse entries are registered to store the physical information about zone, bin, and quantity.</span></span>

<span data-ttu-id="4c914-111">Tabellen **Placeringsindhold** bruges til at håndtere de forskellige dimensioner af indholdet i en placering pr. vare som f.eks. måleenhed, maksimalt antal, og minimumantal.</span><span class="sxs-lookup"><span data-stu-id="4c914-111">The **Bin Content** table is used to handle all the different dimensions of the contents of a bin per item, such as unit of measure, maximum quantity, and minimum quantity.</span></span> <span data-ttu-id="4c914-112">Tabellen **Placeringsindhold** indeholder også flow-felter til de lagerposter, lagerinstruktioner og lagerkladdelinjer, der sikrer, at tilgængeligheden af en vare pr. placering og en placering for en vare kan beregnes hurtigt.</span><span class="sxs-lookup"><span data-stu-id="4c914-112">The **Bin Content** table also contains flow fields to the warehouse entries, warehouse instructions, and warehouse journal lines, which ensures that the availability of an item per bin and a bin for an item can be calculated quickly.</span></span> <span data-ttu-id="4c914-113">Du kan finde flere oplysninger i [Designoplysninger: Tilgængelighed i lageret](design-details-availability-in-the-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="4c914-113">For more information, see [Design Details: Availability in the Warehouse](design-details-availability-in-the-warehouse.md).</span></span>  

<span data-ttu-id="4c914-114">Når vareposteringer forekommer uden for lagermodulet, bruges der en standardreguleringsplacering pr. lokation til at synkronisere lagerposter med lagerbeholdningsposter.</span><span class="sxs-lookup"><span data-stu-id="4c914-114">When item postings occur outside the warehouse module, a default adjustment bin per location is used to synchronize warehouse entries with inventory entries.</span></span> <span data-ttu-id="4c914-115">Under lageropgørelse registreres eventuelle forskelle mellem det beregnede og optalte antal på justeringsplaceringen og bogføres derefter som rettede vareposter.</span><span class="sxs-lookup"><span data-stu-id="4c914-115">During physical inventory of the warehouse, any differences between the calculated and counted quantities are recorded in the adjustment bin and then posted as correcting item ledger entries.</span></span> <span data-ttu-id="4c914-116">Du kan finde flere oplysninger i [Designoplysninger: Integration med lager](design-details-integration-with-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="4c914-116">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="4c914-117">Følgende illustration viser typiske lagerstrømme.</span><span class="sxs-lookup"><span data-stu-id="4c914-117">The following illustration outlines typical warehouse flows.</span></span>  

<span data-ttu-id="4c914-118">![Oversigt over lagerstedsprocesser](media/design_details_warehouse_management_overview.png "Oversigt over lagerstedsprocesser")</span><span class="sxs-lookup"><span data-stu-id="4c914-118">![Overview of warehouse processes](media/design_details_warehouse_management_overview.png "Overview of warehouse processes")</span></span>  

## <a name="basic-or-advanced-warehousing"></a><span data-ttu-id="4c914-119">Grundlæggende eller avanceret logistik</span><span class="sxs-lookup"><span data-stu-id="4c914-119">Basic or Advanced Warehousing</span></span>  
<span data-ttu-id="4c914-120">Lagerfunktioner i [!INCLUDE[prod_short](includes/prod_short.md)] kan implementeres i forskellige kompleksitetsniveauer, afhængig af virksomhedens processer og ordrevolumen.</span><span class="sxs-lookup"><span data-stu-id="4c914-120">Warehouse functionality in [!INCLUDE[prod_short](includes/prod_short.md)] can be implemented in different complexity levels, depending on a company’s processes and order volume.</span></span> <span data-ttu-id="4c914-121">Den væsentligste forskel er, at aktiviteter udføres ordre for ordre i basislogistik, når de er fælles for flere ordrer i avanceret logistik.</span><span class="sxs-lookup"><span data-stu-id="4c914-121">The main difference is that activities are performed order-by-order in basic warehousing when they are consolidated for multiple orders in advanced warehousing.</span></span>  

 <span data-ttu-id="4c914-122">Med henblik på at skelne mellem de forskellige kompleksitetsniveauer refererer denne dokumentation til to almindelige betegnelser, Grundlæggende og Avanceret logistik.</span><span class="sxs-lookup"><span data-stu-id="4c914-122">To differentiate between the different complexity levels, this documentation refers to two general denominations, Basic and Advanced Warehousing.</span></span> <span data-ttu-id="4c914-123">Denne simple differentiering dækker flere forskellige kompleksitetsniveauer, som defineret af produktdetaljer og lokationsopsætning, hver understøttet af forskellige brugergrænsefladedokumenter.</span><span class="sxs-lookup"><span data-stu-id="4c914-123">This simple differentiation covers several different complexity levels as defined by product granules and location setup, each supported by different UI documents.</span></span> <span data-ttu-id="4c914-124">Du kan finde flere oplysninger i [Designoplysninger: Opsætning af lager](design-details-warehouse-setup.md)</span><span class="sxs-lookup"><span data-stu-id="4c914-124">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="4c914-125">Det mest avancerede niveau for logistik kaldes "logistikinstallationer" i denne dokumentation, da dette niveau kræver det mest avancerede modul, Logistik.</span><span class="sxs-lookup"><span data-stu-id="4c914-125">The most advanced level of warehousing is referred to as “WMS installations” in this documentation, since this level requires the most advanced granule, Warehouse Management Systems.</span></span>  

 <span data-ttu-id="4c914-126">Følgende forskellige UI-dokumenter, der bruges i grundlæggende og avanceret logistik.</span><span class="sxs-lookup"><span data-stu-id="4c914-126">The following different UI documents are used in basic and advanced warehousing.</span></span>  

## <a name="basic-ui-documents"></a><span data-ttu-id="4c914-127">Grundlæggende brugergrænsefladedokumenter</span><span class="sxs-lookup"><span data-stu-id="4c914-127">Basic UI Documents</span></span>  

-   <span data-ttu-id="4c914-128">**Læg-på-lager**</span><span class="sxs-lookup"><span data-stu-id="4c914-128">**Inventory Put-away**</span></span>  
-   <span data-ttu-id="4c914-129">**Pluk**</span><span class="sxs-lookup"><span data-stu-id="4c914-129">**Inventory Pick**</span></span>  
-   <span data-ttu-id="4c914-130">**Flytning (lager)**</span><span class="sxs-lookup"><span data-stu-id="4c914-130">**Inventory Movement**</span></span>  
-   <span data-ttu-id="4c914-131">**Varekladde**</span><span class="sxs-lookup"><span data-stu-id="4c914-131">**Item Journal**</span></span>  
-   <span data-ttu-id="4c914-132">**Vareomposteringskladde**</span><span class="sxs-lookup"><span data-stu-id="4c914-132">**Item Reclassification Journal**</span></span>  
-   <span data-ttu-id="4c914-133">(Forskellige rapporter)</span><span class="sxs-lookup"><span data-stu-id="4c914-133">(Various reports)</span></span>  

## <a name="advanced-ui-documents"></a><span data-ttu-id="4c914-134">Avancerede brugergrænsefladedokumenter</span><span class="sxs-lookup"><span data-stu-id="4c914-134">Advanced UI Documents</span></span>  

-   <span data-ttu-id="4c914-135">**Lagermodtagelse**</span><span class="sxs-lookup"><span data-stu-id="4c914-135">**Warehouse Receipt**</span></span>  
-   <span data-ttu-id="4c914-136">**Læg-på-lager-kladde**</span><span class="sxs-lookup"><span data-stu-id="4c914-136">**Put-away Worksheet**</span></span>  
-   <span data-ttu-id="4c914-137">**Læg-på-lager (logistik)**</span><span class="sxs-lookup"><span data-stu-id="4c914-137">**Warehouse Put-away**</span></span>  
-   <span data-ttu-id="4c914-138">**Plukkladde**</span><span class="sxs-lookup"><span data-stu-id="4c914-138">**Pick Worksheet**</span></span>  
-   <span data-ttu-id="4c914-139">**Pluk (logistik)**</span><span class="sxs-lookup"><span data-stu-id="4c914-139">**Warehouse Pick**</span></span>  
-   <span data-ttu-id="4c914-140">**Bevægelseskladde**</span><span class="sxs-lookup"><span data-stu-id="4c914-140">**Movement Worksheet**</span></span>  
-   <span data-ttu-id="4c914-141">**Bevægelse (logistik)**</span><span class="sxs-lookup"><span data-stu-id="4c914-141">**Warehouse Movement**</span></span>  
-   <span data-ttu-id="4c914-142">**Internt lagerpluk**</span><span class="sxs-lookup"><span data-stu-id="4c914-142">**Internal Whse. Pick**</span></span>  
-   <span data-ttu-id="4c914-143">**Intern læg-på-lager-aktivitet**</span><span class="sxs-lookup"><span data-stu-id="4c914-143">**Internal Whse. Put-away**</span></span>  
-   <span data-ttu-id="4c914-144">**Placeringsopr.kladde**</span><span class="sxs-lookup"><span data-stu-id="4c914-144">**Bin Creation Worksheet**</span></span>  
-   <span data-ttu-id="4c914-145">**Opr.kladde til placeringsindh.**</span><span class="sxs-lookup"><span data-stu-id="4c914-145">**Bin Content Creation Worksheet**</span></span>  
-   <span data-ttu-id="4c914-146">**Lagerkladde**</span><span class="sxs-lookup"><span data-stu-id="4c914-146">**Whse. Item Journal**</span></span>  
-   <span data-ttu-id="4c914-147">**Lagervareomposteringskladde**</span><span class="sxs-lookup"><span data-stu-id="4c914-147">**Whse. Item Reclass. Journal**</span></span>  
-   <span data-ttu-id="4c914-148">(Forskellige rapporter)</span><span class="sxs-lookup"><span data-stu-id="4c914-148">(Various reports)</span></span>  

<span data-ttu-id="4c914-149">Hvis du ønsker yderligere oplysninger om de enkelte dokumenter, kan du se de respektive emner.</span><span class="sxs-lookup"><span data-stu-id="4c914-149">For more information about each document, see the respective page topics.</span></span>  

### <a name="terminology"></a><span data-ttu-id="4c914-150">Terminologi</span><span class="sxs-lookup"><span data-stu-id="4c914-150">Terminology</span></span>  
<span data-ttu-id="4c914-151">For at opnå overensstemmelse med økonomiske begreber køb og salg, henviser [!INCLUDE[prod_short](includes/prod_short.md)]-lagerdokumentation til følgende vilkår for vareflowet på lageret.</span><span class="sxs-lookup"><span data-stu-id="4c914-151">To align with the financial concepts of purchases and sales, [!INCLUDE[prod_short](includes/prod_short.md)] warehouse documentation refers to the following terms for item flow in the warehouse.</span></span>  

|<span data-ttu-id="4c914-152">Begreb</span><span class="sxs-lookup"><span data-stu-id="4c914-152">Term</span></span>|<span data-ttu-id="4c914-153">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="4c914-153">Description</span></span>|  
|----------|---------------------------------------|  
|<span data-ttu-id="4c914-154">Indgående strøm</span><span class="sxs-lookup"><span data-stu-id="4c914-154">Inbound flow</span></span>|<span data-ttu-id="4c914-155">Varer, der flyttes til lagerlokationen, som køb og indgående overflytninger.</span><span class="sxs-lookup"><span data-stu-id="4c914-155">Items moving into the warehouse location, such as purchases and inbound transfers.</span></span>|  
|<span data-ttu-id="4c914-156">Internt forløb</span><span class="sxs-lookup"><span data-stu-id="4c914-156">Internal flow</span></span>|<span data-ttu-id="4c914-157">Varer, der flytter inden for lagerlokationen, som produktionskomponenter og afgang.</span><span class="sxs-lookup"><span data-stu-id="4c914-157">Items moving inside the warehouse location, such as production components and output.</span></span>|  
|<span data-ttu-id="4c914-158">Udgående strøm</span><span class="sxs-lookup"><span data-stu-id="4c914-158">Outbound flow</span></span>|<span data-ttu-id="4c914-159">Varer, der flyttes ud af lagerlokationen, som salg og udgående overflytninger.</span><span class="sxs-lookup"><span data-stu-id="4c914-159">Items moving out of the warehouse location, such as sales and outbound transfers.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="4c914-160">Se også</span><span class="sxs-lookup"><span data-stu-id="4c914-160">See Also</span></span>  
 [<span data-ttu-id="4c914-161">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="4c914-161">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]