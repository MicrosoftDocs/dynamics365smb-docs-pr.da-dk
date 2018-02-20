---
title: Bruge Excel til at importere data til Financials | Microsoft Docs
description: "Brug standardkonfigurationspakken til at tilføje debitordata i Excel og importere dataene tilbage til Finance and Operations, Business edition."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 07/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: d6ef2eccb465afffb0f16ec9de1ceac9e9a4e3fc
ms.contentlocale: da-dk
ms.lasthandoff: 02/02/2018

---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a><span data-ttu-id="6b4a4-103">Importere data fra ældre regnskabsprogrammer ved hjælp af en konfigurationspakke</span><span class="sxs-lookup"><span data-stu-id="6b4a4-103">Importing Data from Legacy Accounting Software using a Configuration Package</span></span>
<span data-ttu-id="6b4a4-104">Du kan importere masterdata og nogle transaktionsdata fra andre økonomisystemer baseret på standardkonfigurationspakken i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6b4a4-104">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="6b4a4-105">I vinduet **Konfigurationspakker** kan du arbejde med pakken for at importere og validere data, før du anvender pakken.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-105">In the **Configuration Packages** window, you can work with the package to import and validate the data before you apply the package.</span></span>  

<span data-ttu-id="6b4a4-106">Hvis du er fortrolig med RapidStart-tjenester til Microsoft Dynamics, kender du også til konfigurationspakker.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-106">If you are familiar with RapidStart Services for Microsoft Dynamics, you are also familiar with configuration packages.</span></span> <span data-ttu-id="6b4a4-107">Standardkonfigurationspakken understøtter de mest almindelige typer data, som du vil importere fra det oprindelige system.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-107">The default configuration package supports the most common types of data that you want to import from a legacy system.</span></span> <span data-ttu-id="6b4a4-108">I Excel kan du derefter tilføje data fra det oprindelige system og konfigurere dem i overensstemmelse med forretningslogikken i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6b4a4-108">In Excel, you can then add the data from the legacy system and set it up according to the business logic of the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

> [!TIP]  
>   <span data-ttu-id="6b4a4-109">Du kan også bruge dataoverførselsguiderne til at importere data fra QuickBooks eller Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-109">Alternatively, use data migration wizards to import data from QuickBooks or Dynamics GP.</span></span> <span data-ttu-id="6b4a4-110">Du kan finde flere oplysninger i [Overførsel af QuickBooks-data](ui-extensions-quickbooks-data-migration.md) eller [Overførsel af data med Dynamics GP](ui-extensions-dynamicsgp-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="6b4a4-110">For more information, see [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md) or [Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md).</span></span>  

## <a name="working-with-data-in-excel"></a><span data-ttu-id="6b4a4-111">Arbejde med data i Excel</span><span class="sxs-lookup"><span data-stu-id="6b4a4-111">Working with Data in Excel</span></span>
<span data-ttu-id="6b4a4-112">Når du eksporterer standardkonfigurationspakken til Excel, indeholder den projektmappe, der oprettes, et regneark for hver tabel i pakken.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-112">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="6b4a4-113">For at forenkle dine opgaver, kan du drage fordel af de XML-manipulationsværktøjer, der er indbygget i Excel.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-113">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="6b4a4-114">Du kan også bruge indbyggede funktioner i Excel til at hjælpe med dataformatering og til at indsætte data i den korrekte celle.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-114">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="6b4a4-115">Tilføj f.eks. et tomt regneark, og kopier de oprindelige data til det.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-115">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="6b4a4-116">Opret derefter en Excel-formel for at afbilde dataene i overflytningsregnearket mellem felterne i det eksporterede regneark og debitorens ældre data.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-116">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="6b4a4-117">Når du har tilknyttet alle data, skal du kopiere dataområdet ind i regnearket med tabellen.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-117">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="6b4a4-118">Undlad at ændre kolonnerne i regnearkene.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-118">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="6b4a4-119">Hvis de flyttes, ændres eller slettes, kan regnearket ikke importeres i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6b4a4-119">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="6b4a4-120">Tabeller i standardkonfigurationspakken</span><span class="sxs-lookup"><span data-stu-id="6b4a4-120">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="6b4a4-121">Standardkonfigurationspakken understøtter følgende tabeller:</span><span class="sxs-lookup"><span data-stu-id="6b4a4-121">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="6b4a4-122">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="6b4a4-122">Payment Terms</span></span>
-   <span data-ttu-id="6b4a4-123">Debitorprisgruppe</span><span class="sxs-lookup"><span data-stu-id="6b4a4-123">Customer Price Group</span></span>
-   <span data-ttu-id="6b4a4-124">Leveringsform</span><span class="sxs-lookup"><span data-stu-id="6b4a4-124">Shipment Method</span></span>
-   <span data-ttu-id="6b4a4-125">Sælger/indkøber</span><span class="sxs-lookup"><span data-stu-id="6b4a4-125">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="6b4a4-126">Sted</span><span class="sxs-lookup"><span data-stu-id="6b4a4-126">Location</span></span>
-   <span data-ttu-id="6b4a4-127">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="6b4a4-127">GL Account</span></span>
-   <span data-ttu-id="6b4a4-128">Kunde</span><span class="sxs-lookup"><span data-stu-id="6b4a4-128">Customer</span></span>
-   <span data-ttu-id="6b4a4-129">Kreditor</span><span class="sxs-lookup"><span data-stu-id="6b4a4-129">Vendor</span></span>
-   <span data-ttu-id="6b4a4-130">Vare</span><span class="sxs-lookup"><span data-stu-id="6b4a4-130">Item</span></span>
-   <span data-ttu-id="6b4a4-131">Salgshoved</span><span class="sxs-lookup"><span data-stu-id="6b4a4-131">Sales Header</span></span>
-   <span data-ttu-id="6b4a4-132">Salgslinje</span><span class="sxs-lookup"><span data-stu-id="6b4a4-132">Sales Line</span></span>
-   <span data-ttu-id="6b4a4-133">Købshoved</span><span class="sxs-lookup"><span data-stu-id="6b4a4-133">Purchase Header</span></span>
-   <span data-ttu-id="6b4a4-134">Købslinje</span><span class="sxs-lookup"><span data-stu-id="6b4a4-134">Purchase Line</span></span>
-   <span data-ttu-id="6b4a4-135">Finanskladdelinje</span><span class="sxs-lookup"><span data-stu-id="6b4a4-135">Gen. Journal Line</span></span>
-   <span data-ttu-id="6b4a4-136">Varekladdelinje</span><span class="sxs-lookup"><span data-stu-id="6b4a4-136">Item Journal Line</span></span>
-   <span data-ttu-id="6b4a4-137">Debitorbogføringsgruppe</span><span class="sxs-lookup"><span data-stu-id="6b4a4-137">Customer Posting Group</span></span>
-   <span data-ttu-id="6b4a4-138">Kreditorbogføringsgruppe</span><span class="sxs-lookup"><span data-stu-id="6b4a4-138">Vendor Posting Group</span></span>
-   <span data-ttu-id="6b4a4-139">Varebogføringsgruppe</span><span class="sxs-lookup"><span data-stu-id="6b4a4-139">Inventory Posting Group</span></span>
-   <span data-ttu-id="6b4a4-140">Enhed</span><span class="sxs-lookup"><span data-stu-id="6b4a4-140">Unit of Measure</span></span>
-   <span data-ttu-id="6b4a4-141">Virksomhedsbogføringsgruppe</span><span class="sxs-lookup"><span data-stu-id="6b4a4-141">Gen. Business Posting Group</span></span>
-   <span data-ttu-id="6b4a4-142">Produktbogføringsgruppe</span><span class="sxs-lookup"><span data-stu-id="6b4a4-142">Gen. Product Posting Group</span></span>
-   <span data-ttu-id="6b4a4-143">Bogføringsopsætning</span><span class="sxs-lookup"><span data-stu-id="6b4a4-143">General Posting Setup</span></span>
-   <span data-ttu-id="6b4a4-144">Distrikt</span><span class="sxs-lookup"><span data-stu-id="6b4a4-144">Territory</span></span>
-   <span data-ttu-id="6b4a4-145">Varekategori</span><span class="sxs-lookup"><span data-stu-id="6b4a4-145">Item Category</span></span>
-   <span data-ttu-id="6b4a4-146">Salgspris</span><span class="sxs-lookup"><span data-stu-id="6b4a4-146">Sales Price</span></span>
-   <span data-ttu-id="6b4a4-147">Købspris</span><span class="sxs-lookup"><span data-stu-id="6b4a4-147">Purchase Price</span></span>

## <a name="importing-customer-data"></a><span data-ttu-id="6b4a4-148">Import af debitordata</span><span class="sxs-lookup"><span data-stu-id="6b4a4-148">Importing Customer Data</span></span>
<span data-ttu-id="6b4a4-149">Når debitordata er indsat i Excel, kan du importere dataene i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6b4a4-149">After the customer data has been entered in Excel, you import the data into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="6b4a4-150">I vinduet **Konfigurationspakker** kan du indlæse dataene fra Excel-filen, og du kan kontrollere, at dataene er i overensstemmelse med [!INCLUDE[d365fin](includes/d365fin_md.md)], før du anvender pakken.</span><span class="sxs-lookup"><span data-stu-id="6b4a4-150">In the **Configuration Packages** window, you import the data from the Excel file, and you can validate that the data is consistent with [!INCLUDE[d365fin](includes/d365fin_md.md)] before you apply the package.</span></span>

## <a name="see-also"></a><span data-ttu-id="6b4a4-151">Se også</span><span class="sxs-lookup"><span data-stu-id="6b4a4-151">See Also</span></span>
[<span data-ttu-id="6b4a4-152">Importere virksomhedsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="6b4a4-152">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="6b4a4-153">Overflytning af QuickBooks Data</span><span class="sxs-lookup"><span data-stu-id="6b4a4-153">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="6b4a4-154">Overførsel af data med Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="6b4a4-154">Dynamics GP Data Migration</span></span>](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

