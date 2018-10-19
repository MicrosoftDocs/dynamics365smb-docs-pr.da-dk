---
title: "Designoplysninger – Oversigt over logistik | Microsoft Docs"
description: "Alle oplysninger skal spores for hver transaktion eller bevægelse på lageret for at understøtte den fysiske håndtering af varerne på zone- og placeringsniveauet. Dette administreres i tabellen **Lagerpost**. Hver transaktion gemmes i en lagerjournal."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: cea5bb76f8fdb8c9c52a5f341d29a34bcb8f0cdc
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-warehouse-overview"></a><span data-ttu-id="48944-105">Designoplysninger: Oversigt over logistik</span><span class="sxs-lookup"><span data-stu-id="48944-105">Design Details: Warehouse Overview</span></span>
<span data-ttu-id="48944-106">Alle oplysninger skal spores for hver transaktion eller bevægelse på lageret for at understøtte den fysiske håndtering af varerne på zone- og placeringsniveauet.</span><span class="sxs-lookup"><span data-stu-id="48944-106">To support the physical handling of items on the zone and bin level, all information must be traced for each transaction or movement in the warehouse.</span></span> <span data-ttu-id="48944-107">Dette administreres i tabellen **Lagerpost**.</span><span class="sxs-lookup"><span data-stu-id="48944-107">This is managed in the **Warehouse Entry** table.</span></span> <span data-ttu-id="48944-108">Hver transaktion gemmes i en lagerjournal.</span><span class="sxs-lookup"><span data-stu-id="48944-108">Each transaction is stored in a warehouse register.</span></span>  

<span data-ttu-id="48944-109">Lagerdokumenter og en lagerkladde bruges til at registrere varebevægelser på lageret.</span><span class="sxs-lookup"><span data-stu-id="48944-109">Warehouse documents and a warehouse journal are used to register item movements in the warehouse.</span></span> <span data-ttu-id="48944-110">Hver gang en vare på lageret flyttes, modtages, lægges på lager, plukkes, leveres eller reguleres, registreres lagerposter for at gemme de fysiske oplysninger om zone, placering og antal.</span><span class="sxs-lookup"><span data-stu-id="48944-110">Every time that an item in the warehouse is moved, received, put away, picked, shipped, or adjusted, warehouse entries are registered to store the physical information about zone, bin, and quantity.</span></span> <span data-ttu-id="48944-111">Du kan finde flere oplysninger i [Designoplysninger: Indgående lagerflow](design-details-outbound-warehouse-flow.md)</span><span class="sxs-lookup"><span data-stu-id="48944-111">For more information, see [Design Details: Inbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="48944-112">Tabellen **Placeringsindhold** bruges til at håndtere de forskellige dimensioner af indholdet i en placering pr. vare som f.eks. måleenhed, maksimalt antal, og minimumantal.</span><span class="sxs-lookup"><span data-stu-id="48944-112">The **Bin Content** table is used to handle all the different dimensions of the contents of a bin per item, such as unit of measure, maximum quantity, and minimum quantity.</span></span> <span data-ttu-id="48944-113">Tabellen **Placeringsindhold** indeholder også flow-felter til de lagerposter, lagerinstruktioner og lagerkladdelinjer, der sikrer, at tilgængeligheden af en vare pr. placering og en placering for en vare kan beregnes hurtigt.</span><span class="sxs-lookup"><span data-stu-id="48944-113">The **Bin Content** table also contains flow fields to the warehouse entries, warehouse instructions, and warehouse journal lines, which ensures that the availability of an item per bin and a bin for an item can be calculated quickly.</span></span> <span data-ttu-id="48944-114">Du kan finde flere oplysninger i [Designoplysninger: Tilgængelighed i lageret](design-details-availability-in-the-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="48944-114">For more information, see [Design Details: Availability in the Warehouse](design-details-availability-in-the-warehouse.md).</span></span>  

<span data-ttu-id="48944-115">Når vareposteringer forekommer uden for lagermodulet, bruges der en standardreguleringsplacering pr. lokation til at synkronisere lagerposter med lagerbeholdningsposter.</span><span class="sxs-lookup"><span data-stu-id="48944-115">When item postings occur outside the warehouse module, a default adjustment bin per location is used to synchronize warehouse entries with inventory entries.</span></span> <span data-ttu-id="48944-116">Under lageropgørelse registreres eventuelle forskelle mellem det beregnede og optalte antal på justeringsplaceringen og bogføres derefter som rettede vareposter.</span><span class="sxs-lookup"><span data-stu-id="48944-116">During physical inventory of the warehouse, any differences between the calculated and counted quantities are recorded in the adjustment bin and then posted as correcting item ledger entries.</span></span> <span data-ttu-id="48944-117">Du kan finde flere oplysninger i [Designoplysninger: Integration med lager](design-details-integration-with-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="48944-117">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="48944-118">Følgende illustration viser typiske lagerstrømme.</span><span class="sxs-lookup"><span data-stu-id="48944-118">The following illustration outlines typical warehouse flows.</span></span>  

<span data-ttu-id="48944-119">![Oversigt over lagerprocesser](media/design_details_warehouse_management_overview.png "Oversigt over lagerprocesser")</span><span class="sxs-lookup"><span data-stu-id="48944-119">![Overview of warehouse processes](media/design_details_warehouse_management_overview.png "Overview of warehouse processes")</span></span>  

## <a name="basic-or-advanced-warehousing"></a><span data-ttu-id="48944-120">Grundlæggende eller avanceret logistik</span><span class="sxs-lookup"><span data-stu-id="48944-120">Basic or Advanced Warehousing</span></span>  
<span data-ttu-id="48944-121">Lagerfunktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)] kan implementeres i forskellige kompleksitetsniveauer, afhængig af virksomhedens processer og ordrevolumen.</span><span class="sxs-lookup"><span data-stu-id="48944-121">Warehouse functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)] can be implemented in different complexity levels, depending on a company’s processes and order volume.</span></span> <span data-ttu-id="48944-122">Den væsentligste forskel er, at aktiviteter udføres ordre for ordre i basislogistik, når de er fælles for flere ordrer i avanceret logistik.</span><span class="sxs-lookup"><span data-stu-id="48944-122">The main difference is that activities are performed order-by-order in basic warehousing when they are consolidated for multiple orders in advanced warehousing.</span></span>  

 <span data-ttu-id="48944-123">Med henblik på at skelne mellem de forskellige kompleksitetsniveauer refererer denne dokumentation til to almindelige betegnelser, Grundlæggende og Avanceret logistik.</span><span class="sxs-lookup"><span data-stu-id="48944-123">To differentiate between the different complexity levels, this documentation refers to two general denominations, Basic and Advanced Warehousing.</span></span> <span data-ttu-id="48944-124">Denne simple differentiering dækker flere forskellige kompleksitetsniveauer, som defineret af produktdetaljer og lokationsopsætning, hver understøttet af forskellige brugergrænsefladedokumenter.</span><span class="sxs-lookup"><span data-stu-id="48944-124">This simple differentiation covers several different complexity levels as defined by product granules and location setup, each supported by different UI documents.</span></span> <span data-ttu-id="48944-125">Du kan finde flere oplysninger i [Designoplysninger: Opsætning af lager](design-details-warehouse-setup.md)</span><span class="sxs-lookup"><span data-stu-id="48944-125">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="48944-126">Det mest avancerede niveau for logistik kaldes "logistikinstallationer" i denne dokumentation, da dette niveau kræver det mest avancerede modul, Logistik.</span><span class="sxs-lookup"><span data-stu-id="48944-126">The most advanced level of warehousing is referred to as “WMS installations” in this documentation, since this level requires the most advanced granule, Warehouse Management Systems.</span></span>  

 <span data-ttu-id="48944-127">Følgende forskellige UI-dokumenter, der bruges i grundlæggende og avanceret logistik.</span><span class="sxs-lookup"><span data-stu-id="48944-127">The following different UI documents are used in basic and advanced warehousing.</span></span>  

## <a name="basic-ui-documents"></a><span data-ttu-id="48944-128">Grundlæggende brugergrænsefladedokumenter</span><span class="sxs-lookup"><span data-stu-id="48944-128">Basic UI Documents</span></span>  

-   <span data-ttu-id="48944-129">**Læg-på-lager**</span><span class="sxs-lookup"><span data-stu-id="48944-129">**Inventory Put-away**</span></span>  
-   <span data-ttu-id="48944-130">**Pluk**</span><span class="sxs-lookup"><span data-stu-id="48944-130">**Inventory Pick**</span></span>  
-   <span data-ttu-id="48944-131">**Flytning (lager)**</span><span class="sxs-lookup"><span data-stu-id="48944-131">**Inventory Movement**</span></span>  
-   <span data-ttu-id="48944-132">**Varekladde**</span><span class="sxs-lookup"><span data-stu-id="48944-132">**Item Journal**</span></span>  
-   <span data-ttu-id="48944-133">**Vareomposteringskladde**</span><span class="sxs-lookup"><span data-stu-id="48944-133">**Item Reclassification Journal**</span></span>  
-   <span data-ttu-id="48944-134">(Forskellige rapporter)</span><span class="sxs-lookup"><span data-stu-id="48944-134">(Various reports)</span></span>  

## <a name="advanced-ui-documents"></a><span data-ttu-id="48944-135">Avancerede brugergrænsefladedokumenter</span><span class="sxs-lookup"><span data-stu-id="48944-135">Advanced UI Documents</span></span>  

-   <span data-ttu-id="48944-136">**Lagermodtagelse**</span><span class="sxs-lookup"><span data-stu-id="48944-136">**Warehouse Receipt**</span></span>  
-   <span data-ttu-id="48944-137">**Læg-på-lager-kladde**</span><span class="sxs-lookup"><span data-stu-id="48944-137">**Put-away Worksheet**</span></span>  
-   <span data-ttu-id="48944-138">**Læg-på-lager (logistik)**</span><span class="sxs-lookup"><span data-stu-id="48944-138">**Warehouse Put-away**</span></span>  
-   <span data-ttu-id="48944-139">**Plukkladde**</span><span class="sxs-lookup"><span data-stu-id="48944-139">**Pick Worksheet**</span></span>  
-   <span data-ttu-id="48944-140">**Pluk (logistik)**</span><span class="sxs-lookup"><span data-stu-id="48944-140">**Warehouse Pick**</span></span>  
-   <span data-ttu-id="48944-141">**Bevægelseskladde**</span><span class="sxs-lookup"><span data-stu-id="48944-141">**Movement Worksheet**</span></span>  
-   <span data-ttu-id="48944-142">**Bevægelse (logistik)**</span><span class="sxs-lookup"><span data-stu-id="48944-142">**Warehouse Movement**</span></span>  
-   <span data-ttu-id="48944-143">**Internt lagerpluk**</span><span class="sxs-lookup"><span data-stu-id="48944-143">**Internal Whse. Pick**</span></span>  
-   <span data-ttu-id="48944-144">**Intern læg-på-lager-aktivitet**</span><span class="sxs-lookup"><span data-stu-id="48944-144">**Internal Whse. Put-away**</span></span>  
-   <span data-ttu-id="48944-145">**Placeringsopr.kladde**</span><span class="sxs-lookup"><span data-stu-id="48944-145">**Bin Creation Worksheet**</span></span>  
-   <span data-ttu-id="48944-146">**Opr.kladde til placeringsindh.**</span><span class="sxs-lookup"><span data-stu-id="48944-146">**Bin Content Creation Worksheet**</span></span>  
-   <span data-ttu-id="48944-147">**Lagerkladde**</span><span class="sxs-lookup"><span data-stu-id="48944-147">**Whse. Item Journal**</span></span>  
-   <span data-ttu-id="48944-148">**Lagervareomposteringskladde**</span><span class="sxs-lookup"><span data-stu-id="48944-148">**Whse. Item Reclass. Journal**</span></span>  
-   <span data-ttu-id="48944-149">(Forskellige rapporter)</span><span class="sxs-lookup"><span data-stu-id="48944-149">(Various reports)</span></span>  

<span data-ttu-id="48944-150">Hvis du ønsker yderligere oplysninger om de enkelte dokumenter, kan du se de respektive emner.</span><span class="sxs-lookup"><span data-stu-id="48944-150">For more information about each document, see the respective window topics.</span></span>  

### <a name="terminology"></a><span data-ttu-id="48944-151">Terminologi</span><span class="sxs-lookup"><span data-stu-id="48944-151">Terminology</span></span>  
<span data-ttu-id="48944-152">For at opnå overensstemmelse med økonomiske begreber køb og salg, henviser [!INCLUDE[d365fin](includes/d365fin_md.md)]-lagerdokumentation til følgende vilkår for vareflowet på lageret.</span><span class="sxs-lookup"><span data-stu-id="48944-152">To align with the financial concepts of purchases and sales, [!INCLUDE[d365fin](includes/d365fin_md.md)] warehouse documentation refers to the following terms for item flow in the warehouse.</span></span>  

|<span data-ttu-id="48944-153">Begreb</span><span class="sxs-lookup"><span data-stu-id="48944-153">Term</span></span>|<span data-ttu-id="48944-154">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="48944-154">Description</span></span>|  
|----------|---------------------------------------|  
|<span data-ttu-id="48944-155">Indgående strøm</span><span class="sxs-lookup"><span data-stu-id="48944-155">Inbound flow</span></span>|<span data-ttu-id="48944-156">Varer, der flyttes til lagerlokationen, som køb og indgående overflytninger.</span><span class="sxs-lookup"><span data-stu-id="48944-156">Items moving into the warehouse location, such as purchases and inbound transfers.</span></span>|  
|<span data-ttu-id="48944-157">Internt forløb</span><span class="sxs-lookup"><span data-stu-id="48944-157">Internal flow</span></span>|<span data-ttu-id="48944-158">Varer, der flytter inden for lagerlokationen, som produktionskomponenter og afgang.</span><span class="sxs-lookup"><span data-stu-id="48944-158">Items moving inside the warehouse location, such as production components and output.</span></span>|  
|<span data-ttu-id="48944-159">Udgående strøm</span><span class="sxs-lookup"><span data-stu-id="48944-159">Outbound flow</span></span>|<span data-ttu-id="48944-160">Varer, der flyttes ud af lagerlokationen, som salg og udgående overflytninger.</span><span class="sxs-lookup"><span data-stu-id="48944-160">Items moving out of the warehouse location, such as sales and outbound transfers.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="48944-161">Se også</span><span class="sxs-lookup"><span data-stu-id="48944-161">See Also</span></span>  
 [<span data-ttu-id="48944-162">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="48944-162">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)

