---
title: Brug Excel til at importere data til Business Central
description: Brug standardkonfigurationspakken til at tilføje debitordata i Excel og importere dataene tilbage til Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 984186e8bb08cc9e99ab91dbc08f0e85c58e0804
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777944"
---
# <a name="importing-business-data-from-other-finance-systems"></a><span data-ttu-id="2630e-103">Importere virksomhedsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="2630e-103">Importing Business Data from Other Finance Systems</span></span>

<span data-ttu-id="2630e-104">Når du tilmelder dig [!INCLUDE[prod_short](includes/prod_short.md)], kan du oprette en tom virksomhed, så du kan overføre dine egne data og teste den nye virksomhed i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="2630e-104">When you sign up for [!INCLUDE[prod_short](includes/prod_short.md)], you can choose to create an empty company so that you can upload your own data and to test your new [!INCLUDE[prod_short](includes/prod_short.md)] company.</span></span> <span data-ttu-id="2630e-105">Afhængigt af hvilket økonomisystem, som virksomheden benytter i dag, kan du overføre oplysninger om debitorer, kreditorer, lagerbeholdning og bankkonti.</span><span class="sxs-lookup"><span data-stu-id="2630e-105">Depending on the finance solution that your business uses today, you can transfer information about customers, vendors, inventory, and bank accounts.</span></span>  

<span data-ttu-id="2630e-106">Fra rollecenteret kan du starte en assisterede opsætningsvejledning for at overføre forretningsdataene fra en Excel-fil eller fra andre formater.</span><span class="sxs-lookup"><span data-stu-id="2630e-106">From the Role Center, you can start an assisted setup guide that helps you transfer the business data from an Excel file or from other formats.</span></span> <span data-ttu-id="2630e-107">Hvilken type filer, du kan overføre, afhænger af de udvidelser, der findes.</span><span class="sxs-lookup"><span data-stu-id="2630e-107">The type of files you can upload depends on the extensions that are available.</span></span> <span data-ttu-id="2630e-108">F.eks. kan du overføre data fra QuickBooks, da [!INCLUDE[prod_short](includes/prod_short.md)] indeholder en udvidelse, der håndterer konverteringen fra QuickBooks.</span><span class="sxs-lookup"><span data-stu-id="2630e-108">For example, you can migrate data from QuickBooks because [!INCLUDE[prod_short](includes/prod_short.md)] includes an extension that handles the conversion from QuickBooks.</span></span> <span data-ttu-id="2630e-109">Hvis du vil overføre data fra andre økonomisystemer, skal du enten kontrollere, om en udvidelse er tilgængelig for den pågældende løsning, eller importere fra Excel.</span><span class="sxs-lookup"><span data-stu-id="2630e-109">If you want to migrate data from other finance solutions, you must either check if an extension is available for that solution or import from Excel.</span></span>  

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="2630e-110">indeholder skabeloner for konti, debitorer, kreditorer og lagervarer, som du kan vælge at anvende, når du importerer data.</span><span class="sxs-lookup"><span data-stu-id="2630e-110">includes templates for accounts, customers, vendors, and inventory items that you can choose to apply when you import your data.</span></span>

<span data-ttu-id="2630e-111">Du kan importere masterdata og nogle transaktionsdata fra andre økonomisystemer baseret på standardkonfigurationspakken i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="2630e-111">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="2630e-112">På siden **Konfigurationspakker** kan du arbejde med pakken for at importere og validere data, før du anvender pakken.</span><span class="sxs-lookup"><span data-stu-id="2630e-112">On the **Configuration Packages** page, you can work with the package to import and validate the data before you apply the package.</span></span>  

> [!TIP]  
> <span data-ttu-id="2630e-113">Vi anbefaler at du bruger dataoverførselsguiderne til at importere data fra Dynamics GP, Dynamics NAV eller QuickBooks.</span><span class="sxs-lookup"><span data-stu-id="2630e-113">We recommend that you use data migration wizards to import data from Dynamics GP, Dynamics NAV, or QuickBooks.</span></span> <span data-ttu-id="2630e-114">Du kan finde flere oplysninger i [Overførsel af lokale data til Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) i administrationsindholdet eller [Overførsel af QuickBooks-data](ui-extensions-quickbooks-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="2630e-114">For more information, see [Migrating On-Premises Data to Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in the administration content, or [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="2630e-115">Til større implementeringsarbejde kan du bruge RapidStart Services til [!INCLUDE[prod_short](includes/prod_short.md)], som er omfattende værktøj til oprettelse af nye løsninger, der er baseret på kundernes forretningsbehov og opsætningsdata.</span><span class="sxs-lookup"><span data-stu-id="2630e-115">For larger implementation work, you can use RapidStart Services for [!INCLUDE[prod_short](includes/prod_short.md)], which is an extensive toolkit for setting up new solutions based on customers' business requirements and setup data.</span></span> <span data-ttu-id="2630e-116">RapidStart Services indeholder også funktionalitet til import af forretningsdata.</span><span class="sxs-lookup"><span data-stu-id="2630e-116">RapidStart Services also offers functionality for import of business data.</span></span> <span data-ttu-id="2630e-117">Du kan finde flere oplysninger i [Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span><span class="sxs-lookup"><span data-stu-id="2630e-117">For more information, see [Setting Up a Company With RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span></span>

<span data-ttu-id="2630e-118">Du kan bruge en dedikeret funktion på siden **Lageropsætning** til at indlæse varebilleder.</span><span class="sxs-lookup"><span data-stu-id="2630e-118">To import item pictures, you can use a dedicated function on the **Inventory Setup** page.</span></span> <span data-ttu-id="2630e-119">Du kan finde flere oplysninger i [Importér flere varebilleder](inventory-how-import-item-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="2630e-119">For more information, see [Import Multiple Item Pictures](inventory-how-import-item-pictures.md).</span></span>

## <a name="importing-data-from-configuration-packages"></a><span data-ttu-id="2630e-120">Importere data fra konfigurationspakker</span><span class="sxs-lookup"><span data-stu-id="2630e-120">Importing Data from Configuration Packages</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="2630e-121">indeholder en konfigurationspakke, som du kan eksportere til Excel og konfigurere dataene der.</span><span class="sxs-lookup"><span data-stu-id="2630e-121">includes a configuration package that you can export to Excel and set up your data there.</span></span> <span data-ttu-id="2630e-122">Derefter kan du importere dataene fra Excel igen.</span><span class="sxs-lookup"><span data-stu-id="2630e-122">Then, you can import the data from Excel again.</span></span> <span data-ttu-id="2630e-123">Pakken indeholder 27 tabeller, herunder masterdata som debitorer, kreditorer, varer og konti, andre grundlæggende opsætningstabeller f.eks. leveringsmetoder og transaktionstabeller, som f.eks. salgshoved og linjer.</span><span class="sxs-lookup"><span data-stu-id="2630e-123">The package consists of 27 tables, including master data such as customers, vendors, items, and accounts, other basic setup tables such as shipping methods, and transactions tables such as sales header and lines.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="2630e-124">Arbejde med konfigurationspakker er avanceret funktionalitet, og det anbefales, at du kontakter systemadministratoren.</span><span class="sxs-lookup"><span data-stu-id="2630e-124">Working with configuration packages is advanced functionality, and we recommend that you contact your administrator.</span></span> <span data-ttu-id="2630e-125">Du kan finde flere oplysninger i [Importere data fra ældre regnskabsprogrammer ved hjælp af en konfigurationspakke](across-import-data-configuration-packages.md).</span><span class="sxs-lookup"><span data-stu-id="2630e-125">For more information, see [Importing Data from Legacy Accounting Software using a Configuration Package](across-import-data-configuration-packages.md).</span></span>

## <a name="working-with-data-in-excel"></a><span data-ttu-id="2630e-126">Arbejde med data i Excel</span><span class="sxs-lookup"><span data-stu-id="2630e-126">Working with Data in Excel</span></span>
<span data-ttu-id="2630e-127">Når du eksporterer standardkonfigurationspakken til Excel, indeholder den projektmappe, der oprettes, et regneark for hver tabel i pakken.</span><span class="sxs-lookup"><span data-stu-id="2630e-127">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="2630e-128">For at forenkle dine opgaver, kan du drage fordel af de XML-manipulationsværktøjer, der er indbygget i Excel.</span><span class="sxs-lookup"><span data-stu-id="2630e-128">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="2630e-129">Du kan også bruge indbyggede funktioner i Excel til at hjælpe med dataformatering og til at indsætte data i den korrekte celle.</span><span class="sxs-lookup"><span data-stu-id="2630e-129">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="2630e-130">Tilføj f.eks. et tomt regneark, og kopier de oprindelige data til det.</span><span class="sxs-lookup"><span data-stu-id="2630e-130">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="2630e-131">Opret derefter en Excel-formel for at afbilde dataene i overflytningsregnearket mellem felterne i det eksporterede regneark og debitorens ældre data.</span><span class="sxs-lookup"><span data-stu-id="2630e-131">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="2630e-132">Når du har tilknyttet alle data, skal du kopiere dataområdet ind i regnearket med tabellen.</span><span class="sxs-lookup"><span data-stu-id="2630e-132">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="2630e-133">Undlad at ændre kolonnerne i regnearkene.</span><span class="sxs-lookup"><span data-stu-id="2630e-133">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="2630e-134">Hvis de flyttes, ændres eller slettes, kan regnearket ikke importeres i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="2630e-134">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="2630e-135">Felter af typen Blob kan ikke eksporteres/importeres ved hjælp af Excel.</span><span class="sxs-lookup"><span data-stu-id="2630e-135">Fields of type Blob cannot be exported/imported using Excel.</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="2630e-136">Tabeller i standardkonfigurationspakken</span><span class="sxs-lookup"><span data-stu-id="2630e-136">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="2630e-137">Standardkonfigurationspakken understøtter følgende tabeller:</span><span class="sxs-lookup"><span data-stu-id="2630e-137">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="2630e-138">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="2630e-138">Payment Terms</span></span>
-   <span data-ttu-id="2630e-139">Debitorprisgruppe</span><span class="sxs-lookup"><span data-stu-id="2630e-139">Customer Price Group</span></span>
-   <span data-ttu-id="2630e-140">Leveringsform</span><span class="sxs-lookup"><span data-stu-id="2630e-140">Shipment Method</span></span>
-   <span data-ttu-id="2630e-141">Sælger/indkøber</span><span class="sxs-lookup"><span data-stu-id="2630e-141">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="2630e-142">Sted</span><span class="sxs-lookup"><span data-stu-id="2630e-142">Location</span></span>
-   <span data-ttu-id="2630e-143">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="2630e-143">GL Account</span></span>
-   <span data-ttu-id="2630e-144">Kunde</span><span class="sxs-lookup"><span data-stu-id="2630e-144">Customer</span></span>
-   <span data-ttu-id="2630e-145">Kreditor</span><span class="sxs-lookup"><span data-stu-id="2630e-145">Vendor</span></span>
-   <span data-ttu-id="2630e-146">Vare</span><span class="sxs-lookup"><span data-stu-id="2630e-146">Item</span></span>
-   <span data-ttu-id="2630e-147">Salgshoved</span><span class="sxs-lookup"><span data-stu-id="2630e-147">Sales Header</span></span>
-   <span data-ttu-id="2630e-148">Salgslinje</span><span class="sxs-lookup"><span data-stu-id="2630e-148">Sales Line</span></span>
-   <span data-ttu-id="2630e-149">Købshoved</span><span class="sxs-lookup"><span data-stu-id="2630e-149">Purchase Header</span></span>
-   <span data-ttu-id="2630e-150">Købslinje</span><span class="sxs-lookup"><span data-stu-id="2630e-150">Purchase Line</span></span>
-   <span data-ttu-id="2630e-151">Finans-</span><span class="sxs-lookup"><span data-stu-id="2630e-151">Gen.</span></span> <span data-ttu-id="2630e-152">kladdelinje</span><span class="sxs-lookup"><span data-stu-id="2630e-152">Journal Line</span></span>
-   <span data-ttu-id="2630e-153">Varekladdelinje</span><span class="sxs-lookup"><span data-stu-id="2630e-153">Item Journal Line</span></span>
-   <span data-ttu-id="2630e-154">Debitorbogføringsgruppe</span><span class="sxs-lookup"><span data-stu-id="2630e-154">Customer Posting Group</span></span>
-   <span data-ttu-id="2630e-155">Kreditorbogføringsgruppe</span><span class="sxs-lookup"><span data-stu-id="2630e-155">Vendor Posting Group</span></span>
-   <span data-ttu-id="2630e-156">Varebogføringsgruppe</span><span class="sxs-lookup"><span data-stu-id="2630e-156">Inventory Posting Group</span></span>
-   <span data-ttu-id="2630e-157">Enhed</span><span class="sxs-lookup"><span data-stu-id="2630e-157">Unit of Measure</span></span>
-   <span data-ttu-id="2630e-158">Finans-</span><span class="sxs-lookup"><span data-stu-id="2630e-158">Gen.</span></span> <span data-ttu-id="2630e-159">Virksomhedsbogf.gruppe</span><span class="sxs-lookup"><span data-stu-id="2630e-159">Business Posting Group</span></span>
-   <span data-ttu-id="2630e-160">Finans-</span><span class="sxs-lookup"><span data-stu-id="2630e-160">Gen.</span></span> <span data-ttu-id="2630e-161">Produktbogf.gruppe</span><span class="sxs-lookup"><span data-stu-id="2630e-161">Product Posting Group</span></span>
-   <span data-ttu-id="2630e-162">Bogføringsopsætning</span><span class="sxs-lookup"><span data-stu-id="2630e-162">General Posting Setup</span></span>
-   <span data-ttu-id="2630e-163">Distrikt</span><span class="sxs-lookup"><span data-stu-id="2630e-163">Territory</span></span>
-   <span data-ttu-id="2630e-164">Varekategori</span><span class="sxs-lookup"><span data-stu-id="2630e-164">Item Category</span></span>
-   <span data-ttu-id="2630e-165">Salgspris</span><span class="sxs-lookup"><span data-stu-id="2630e-165">Sales Price</span></span>
-   <span data-ttu-id="2630e-166">Købspris</span><span class="sxs-lookup"><span data-stu-id="2630e-166">Purchase Price</span></span>

## <a name="see-also"></a><span data-ttu-id="2630e-167">Se også</span><span class="sxs-lookup"><span data-stu-id="2630e-167">See Also</span></span>
[<span data-ttu-id="2630e-168">Oprette en virksomhed med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="2630e-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="2630e-169">Overførsel af lokale data til Business Central Online</span><span class="sxs-lookup"><span data-stu-id="2630e-169">Migrating On-Premises Data to Business Central Online</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-data)  
[<span data-ttu-id="2630e-170">Overflytning af QuickBooks Data</span><span class="sxs-lookup"><span data-stu-id="2630e-170">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="2630e-171">Importere flere varebilleder</span><span class="sxs-lookup"><span data-stu-id="2630e-171">Import Multiple Item Pictures</span></span>](inventory-how-import-item-pictures.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]