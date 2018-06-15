---
title: Bruge Excel til at importere data til Financials | Microsoft Docs
description: "Brug standardkonfigurationspakken til at tilføje debitordata i Excel og importere dataene tilbage til Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 05/17/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 379cfd2731bba2df6f5e31d2b8de2d72e2064ebb
ms.contentlocale: da-dk
ms.lasthandoff: 05/17/2018

---
# <a name="importing-business-data-from-other-finance-systems"></a><span data-ttu-id="fcc8e-103">Importere virksomhedsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="fcc8e-103">Importing Business Data from Other Finance Systems</span></span>
<span data-ttu-id="fcc8e-104">Når du tilmelder dig [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du oprette en tom virksomhed, så du kan overføre dine egne data og teste den nye virksomhed i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fcc8e-104">When you sign up for [!INCLUDE[d365fin](includes/d365fin_md.md)], you can choose to create an empty company so that you can upload your own data and to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="fcc8e-105">Afhængigt af hvilket økonomisystem, som virksomheden benytter i dag, kan du overføre oplysninger om debitorer, kreditorer, lagerbeholdning og bankkonti.</span><span class="sxs-lookup"><span data-stu-id="fcc8e-105">Depending on the finance solution that your business uses today, you can transfer information about customers, vendors, inventory, and bank accounts.</span></span>  

<span data-ttu-id="fcc8e-106">Fra rollecenteret kan du starte en assisterede opsætningsvejledning for at overføre forretningsdataene fra en Excel-fil eller fra andre formater.</span><span class="sxs-lookup"><span data-stu-id="fcc8e-106">From the Role Center, you can start an assisted setup guide that helps you transfer the business data from an Excel file or from other formats.</span></span> <span data-ttu-id="fcc8e-107">Hvilken type filer, du kan overføre, afhænger af de udvidelser, der findes.</span><span class="sxs-lookup"><span data-stu-id="fcc8e-107">The type of files you can upload depends on the extensions that are available.</span></span> <span data-ttu-id="fcc8e-108">F.eks. kan du overføre data fra QuickBooks, da [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder en udvidelse, der håndterer konverteringen fra QuickBooks.</span><span class="sxs-lookup"><span data-stu-id="fcc8e-108">For example, you can migrate data from QuickBooks because [!INCLUDE[d365fin](includes/d365fin_md.md)] includes an extension that handles the conversion from QuickBooks.</span></span> <span data-ttu-id="fcc8e-109">Hvis du vil overføre data fra andre økonomisystemer, skal du enten kontrollere, om en udvidelse er tilgængelig for den pågældende løsning, eller importere fra Excel.</span><span class="sxs-lookup"><span data-stu-id="fcc8e-109">If you want to migrate data from other finance solutions, you must either check if an extension is available for that solution or import from Excel.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="fcc8e-110"> indeholder skabeloner for konti, debitorer, kreditorer og lagervarer, som du kan vælge at anvende, når du importerer data.</span><span class="sxs-lookup"><span data-stu-id="fcc8e-110"> includes templates for accounts, customers, vendors, and inventory items that you can choose to apply when you import your data.</span></span>

<span data-ttu-id="fcc8e-111">Du kan importere masterdata og nogle transaktionsdata fra andre økonomisystemer baseret på standardkonfigurationspakken i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fcc8e-111">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="fcc8e-112">I vinduet **Konfigurationspakker** kan du arbejde med pakken for at importere og validere data, før du anvender pakken.</span><span class="sxs-lookup"><span data-stu-id="fcc8e-112">In the **Configuration Packages** window, you can work with the package to import and validate the data before you apply the package.</span></span>  

> [!TIP]  
> <span data-ttu-id="fcc8e-113">Du kan også bruge dataoverførselsguiderne til at importere data fra QuickBooks eller Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="fcc8e-113">Alternatively, use data migration wizards to import data from QuickBooks or Dynamics GP.</span></span> <span data-ttu-id="fcc8e-114">Du kan finde flere oplysninger i [Overførsel af QuickBooks-data](ui-extensions-quickbooks-data-migration.md) eller [Overførsel af data med Dynamics GP](ui-extensions-dynamicsgp-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="fcc8e-114">For more information, see [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md) or [Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="fcc8e-115">Til større implementeringsarbejde kan du bruge RapidStart Services til [!INCLUDE[d365fin](includes/d365fin_md.md)], som er en omfattende værktøjet til oprettelse af nye løsninger, der er baseret på kundernes forretningsbehov og opsætningsdata.</span><span class="sxs-lookup"><span data-stu-id="fcc8e-115">For larger implementation work, you can use RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], which is an extensive toolkit for setting up new solutions based on customers' business requirements and setup data.</span></span> <span data-ttu-id="fcc8e-116">RapidStart Services indeholder også funktionalitet til indlæsning af virksomhedsdata.</span><span class="sxs-lookup"><span data-stu-id="fcc8e-116">RapidStart Services also offers functionality for import of business data.</span></span> <span data-ttu-id="fcc8e-117">Du kan finde flere oplysninger i [Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span><span class="sxs-lookup"><span data-stu-id="fcc8e-117">For more information, see [Setting Up a Company With RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span></span>

## <a name="importing-data-from-configuration-packages"></a><span data-ttu-id="fcc8e-118">Importere data fra konfigurationspakker</span><span class="sxs-lookup"><span data-stu-id="fcc8e-118">Importing Data from Configuration Packages</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="fcc8e-119"> indeholder en konfigurationspakke, som du kan eksportere til Excel og konfigurere dataene der.</span><span class="sxs-lookup"><span data-stu-id="fcc8e-119"> includes a configuration package that you can export to Excel and set up your data there.</span></span> <span data-ttu-id="fcc8e-120">Derefter kan du importere dataene fra Excel igen.</span><span class="sxs-lookup"><span data-stu-id="fcc8e-120">Then, you can import the data from Excel again.</span></span> <span data-ttu-id="fcc8e-121">Pakken indeholder 27 tabeller, herunder masterdata som debitorer, kreditorer, varer og konti, andre grundlæggende opsætningstabeller f.eks. leveringsmetoder og transaktionstabeller, som f.eks. salgshoved og linjer.</span><span class="sxs-lookup"><span data-stu-id="fcc8e-121">The package consists of 27 tables, including master data such as customers, vendors, items, and accounts, other basic setup tables such as shipping methods, and transactions tables such as sales header and lines.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="fcc8e-122">Arbejde med konfigurationspakker er avanceret funktionalitet, og det anbefales, at du kontakter systemadministratoren.</span><span class="sxs-lookup"><span data-stu-id="fcc8e-122">Working with configuration packages is advanced functionality, and we recommend that you contact your administrator.</span></span> <span data-ttu-id="fcc8e-123">Du kan finde flere oplysninger under [Importere data fra ældre regnskabsprogrammer ved hjælp af en konfigurationspakke](across-import-data-configuration-packages.md).</span><span class="sxs-lookup"><span data-stu-id="fcc8e-123">For more information, see [Importing Data from Legacy Accounting Software using a Configuration Package](across-import-data-configuration-packages.md).</span></span>

## <a name="working-with-data-in-excel"></a><span data-ttu-id="fcc8e-124">Arbejde med data i Excel</span><span class="sxs-lookup"><span data-stu-id="fcc8e-124">Working with Data in Excel</span></span>
<span data-ttu-id="fcc8e-125">Når du eksporterer standardkonfigurationspakken til Excel, indeholder den projektmappe, der oprettes, et regneark for hver tabel i pakken.</span><span class="sxs-lookup"><span data-stu-id="fcc8e-125">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="fcc8e-126">For at forenkle dine opgaver, kan du drage fordel af de XML-manipulationsværktøjer, der er indbygget i Excel.</span><span class="sxs-lookup"><span data-stu-id="fcc8e-126">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="fcc8e-127">Du kan også bruge indbyggede funktioner i Excel til at hjælpe med dataformatering og til at indsætte data i den korrekte celle.</span><span class="sxs-lookup"><span data-stu-id="fcc8e-127">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="fcc8e-128">Tilføj f.eks. et tomt regneark, og kopier de oprindelige data til det.</span><span class="sxs-lookup"><span data-stu-id="fcc8e-128">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="fcc8e-129">Opret derefter en Excel-formel for at afbilde dataene i overflytningsregnearket mellem felterne i det eksporterede regneark og debitorens ældre data.</span><span class="sxs-lookup"><span data-stu-id="fcc8e-129">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="fcc8e-130">Når du har tilknyttet alle data, skal du kopiere dataområdet ind i regnearket med tabellen.</span><span class="sxs-lookup"><span data-stu-id="fcc8e-130">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="fcc8e-131">Undlad at ændre kolonnerne i regnearkene.</span><span class="sxs-lookup"><span data-stu-id="fcc8e-131">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="fcc8e-132">Hvis de flyttes, ændres eller slettes, kan regnearket ikke importeres i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fcc8e-132">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="fcc8e-133">Tabeller i standardkonfigurationspakken</span><span class="sxs-lookup"><span data-stu-id="fcc8e-133">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="fcc8e-134">Standardkonfigurationspakken understøtter følgende tabeller:</span><span class="sxs-lookup"><span data-stu-id="fcc8e-134">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="fcc8e-135">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="fcc8e-135">Payment Terms</span></span>
-   <span data-ttu-id="fcc8e-136">Debitorprisgruppe</span><span class="sxs-lookup"><span data-stu-id="fcc8e-136">Customer Price Group</span></span>
-   <span data-ttu-id="fcc8e-137">Leveringsform</span><span class="sxs-lookup"><span data-stu-id="fcc8e-137">Shipment Method</span></span>
-   <span data-ttu-id="fcc8e-138">Sælger/indkøber</span><span class="sxs-lookup"><span data-stu-id="fcc8e-138">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="fcc8e-139">Sted</span><span class="sxs-lookup"><span data-stu-id="fcc8e-139">Location</span></span>
-   <span data-ttu-id="fcc8e-140">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="fcc8e-140">GL Account</span></span>
-   <span data-ttu-id="fcc8e-141">Kunde</span><span class="sxs-lookup"><span data-stu-id="fcc8e-141">Customer</span></span>
-   <span data-ttu-id="fcc8e-142">Kreditor</span><span class="sxs-lookup"><span data-stu-id="fcc8e-142">Vendor</span></span>
-   <span data-ttu-id="fcc8e-143">Vare</span><span class="sxs-lookup"><span data-stu-id="fcc8e-143">Item</span></span>
-   <span data-ttu-id="fcc8e-144">Salgshoved</span><span class="sxs-lookup"><span data-stu-id="fcc8e-144">Sales Header</span></span>
-   <span data-ttu-id="fcc8e-145">Salgslinje</span><span class="sxs-lookup"><span data-stu-id="fcc8e-145">Sales Line</span></span>
-   <span data-ttu-id="fcc8e-146">Købshoved</span><span class="sxs-lookup"><span data-stu-id="fcc8e-146">Purchase Header</span></span>
-   <span data-ttu-id="fcc8e-147">Købslinje</span><span class="sxs-lookup"><span data-stu-id="fcc8e-147">Purchase Line</span></span>
-   <span data-ttu-id="fcc8e-148">Finanskladdelinje</span><span class="sxs-lookup"><span data-stu-id="fcc8e-148">Gen. Journal Line</span></span>
-   <span data-ttu-id="fcc8e-149">Varekladdelinje</span><span class="sxs-lookup"><span data-stu-id="fcc8e-149">Item Journal Line</span></span>
-   <span data-ttu-id="fcc8e-150">Debitorbogføringsgruppe</span><span class="sxs-lookup"><span data-stu-id="fcc8e-150">Customer Posting Group</span></span>
-   <span data-ttu-id="fcc8e-151">Kreditorbogføringsgruppe</span><span class="sxs-lookup"><span data-stu-id="fcc8e-151">Vendor Posting Group</span></span>
-   <span data-ttu-id="fcc8e-152">Varebogføringsgruppe</span><span class="sxs-lookup"><span data-stu-id="fcc8e-152">Inventory Posting Group</span></span>
-   <span data-ttu-id="fcc8e-153">Enhed</span><span class="sxs-lookup"><span data-stu-id="fcc8e-153">Unit of Measure</span></span>
-   <span data-ttu-id="fcc8e-154">Virksomhedsbogføringsgruppe</span><span class="sxs-lookup"><span data-stu-id="fcc8e-154">Gen. Business Posting Group</span></span>
-   <span data-ttu-id="fcc8e-155">Produktbogføringsgruppe</span><span class="sxs-lookup"><span data-stu-id="fcc8e-155">Gen. Product Posting Group</span></span>
-   <span data-ttu-id="fcc8e-156">Bogføringsopsætning</span><span class="sxs-lookup"><span data-stu-id="fcc8e-156">General Posting Setup</span></span>
-   <span data-ttu-id="fcc8e-157">Distrikt</span><span class="sxs-lookup"><span data-stu-id="fcc8e-157">Territory</span></span>
-   <span data-ttu-id="fcc8e-158">Varekategori</span><span class="sxs-lookup"><span data-stu-id="fcc8e-158">Item Category</span></span>
-   <span data-ttu-id="fcc8e-159">Salgspris</span><span class="sxs-lookup"><span data-stu-id="fcc8e-159">Sales Price</span></span>
-   <span data-ttu-id="fcc8e-160">Købspris</span><span class="sxs-lookup"><span data-stu-id="fcc8e-160">Purchase Price</span></span>

## <a name="see-also"></a><span data-ttu-id="fcc8e-161">Se også</span><span class="sxs-lookup"><span data-stu-id="fcc8e-161">See Also</span></span>
[<span data-ttu-id="fcc8e-162">Oprette en virksomhed med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="fcc8e-162">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="fcc8e-163">Overflytning af QuickBooks Data</span><span class="sxs-lookup"><span data-stu-id="fcc8e-163">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="fcc8e-164">Overførsel af data med Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="fcc8e-164">Dynamics GP Data Migration</span></span>](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

