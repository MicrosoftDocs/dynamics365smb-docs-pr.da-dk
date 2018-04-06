---
title: "Sådan oprettes en nyt virksomhed | Microsoft Docs"
description: For at du kan bruge RapidStart Services, er tabeller og sider oprettet, men der er ingen data i dem.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8c07b7c4e6b1c82004295a187184a6f3ccb4c7c7
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="create-a-new-company"></a><span data-ttu-id="c959f-103">Oprette en ny virksomhed</span><span class="sxs-lookup"><span data-stu-id="c959f-103">Create a New Company</span></span>
<span data-ttu-id="c959f-104">Hvis du vil bruge RapidStart Services til [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du først oprette en ny virksomhed, som du ønsker at udføre en kundeimplementering for.</span><span class="sxs-lookup"><span data-stu-id="c959f-104">To use RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], you first create a new company for which you want to perform a customer implementation.</span></span> <span data-ttu-id="c959f-105">Når du opretter en ny virksomhed, oprettes standardtabellerne og -siderne i [!INCLUDE[d365fin](includes/d365fin_md.md)], men der er ingen data i dem.</span><span class="sxs-lookup"><span data-stu-id="c959f-105">When you create a new company, the standard [!INCLUDE[d365fin](includes/d365fin_md.md)] tables and pages are created, but there is no data in them.</span></span>

<span data-ttu-id="c959f-106">Du kan også anvende specifikke konfigurationsdata til din virksomhed, når du har initialiseret den.</span><span class="sxs-lookup"><span data-stu-id="c959f-106">In addition, you can apply specific setup data to your company after you initialize it.</span></span> <span data-ttu-id="c959f-107">Oplysningerne leveres i en konfigurationspakke, en .rapidstart-fil., som leverer indhold i et komprimeret format.</span><span class="sxs-lookup"><span data-stu-id="c959f-107">The information is provided in a configuration package, a .rapidstart file, which delivers content in a compressed format.</span></span>  

<span data-ttu-id="c959f-108">Eksempelkonfigurationspakker, herunder lande-/områdespecifikke filer, følger med CRONUS-demoregnskabet.</span><span class="sxs-lookup"><span data-stu-id="c959f-108">Example configuration packages, including country/region-specific files, are included with the CRONUS demonstration company.</span></span> <span data-ttu-id="c959f-109">Brug følgende fremgangsmåder for at bruge pakken med eksempelkonfiguration af et nyt firma.</span><span class="sxs-lookup"><span data-stu-id="c959f-109">Use the following procedures to use the example configuration package with a new company.</span></span>  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a><span data-ttu-id="c959f-110">Sådan bruger du eksempelkonfigurationspakken BASICCONFIG</span><span class="sxs-lookup"><span data-stu-id="c959f-110">To use the sample BASICCONFIG configuration package</span></span>  
1. <span data-ttu-id="c959f-111">Åbn regnskabet CRONUS Danmark A/S.</span><span class="sxs-lookup"><span data-stu-id="c959f-111">Open the CRONUS International Ltd. company.</span></span> <span data-ttu-id="c959f-112">Du kan finde flere oplysninger under [Ændring af grundlæggende indstillinger](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="c959f-112">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>
2. <span data-ttu-id="c959f-113">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Konfigurationspakker**, og vælg det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c959f-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Configuration Packages**, and then choose the related link.</span></span>  
3. <span data-ttu-id="c959f-114">Vælg pakken BASICCONFIG på listen, og vælg derefter handlingen **Udlæs pakke**.</span><span class="sxs-lookup"><span data-stu-id="c959f-114">Choose the BASICCONFIG package from the list, and then choose the **Export Package** action.</span></span>  

<span data-ttu-id="c959f-115">Brug følgende fremgangsmåde for at oprette en ny virksomhed, og brug pakken BASICCONFIG som en del af proceduren.</span><span class="sxs-lookup"><span data-stu-id="c959f-115">Use the following procedure to create a new company, and use the BASICCONFIG package as part of the process.</span></span>  

## <a name="to-create-a-new-company"></a><span data-ttu-id="c959f-116">Sådan oprettes en ny virksomhed</span><span class="sxs-lookup"><span data-stu-id="c959f-116">To create a new company</span></span>  
1. <span data-ttu-id="c959f-117">Oprette en ny virksomhed.</span><span class="sxs-lookup"><span data-stu-id="c959f-117">Create a new company.</span></span> <span data-ttu-id="c959f-118">Du kan finde flere oplysninger om oprettelse af pluk under [Oprettelse af nye virksomheder i [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="c959f-118">For more information, see [Creating New Companies in [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).</span></span>
2. <span data-ttu-id="c959f-119">Du kan nu importere konfigurationspakken, du har eksporteret fra demonstrationsvirksomheden CRONUS Danmark A/S fra rollecentret RapidStart Services-implementering.</span><span class="sxs-lookup"><span data-stu-id="c959f-119">From the RapidStart Services Implementer Role Center, you can now import the configuration package that you exported from the CRONUS International Ltd. company.</span></span>

<span data-ttu-id="c959f-120">Når du opretter en ny virksomhed, udfyldes nogle tabeller automatisk, selvom der ikke anvendes nogen virksomhedsskabelon.</span><span class="sxs-lookup"><span data-stu-id="c959f-120">After you create a new company, some tables are automatically filled in, even if no company template is applied.</span></span> <span data-ttu-id="c959f-121">Du kan f.eks. gennemse standardkoderne for bogføring og batchposteringer i vinduet **Kildekode**.</span><span class="sxs-lookup"><span data-stu-id="c959f-121">For example, you can review the standard codes for posting and batch transactions in the **Source Code** window.</span></span> <span data-ttu-id="c959f-122">Hvis du angiver en lokal version af [!INCLUDE[d365fin](includes/d365fin_md.md)], bør du gennemgå denne tabel og overveje eventuelle problemer med lokalt sprog.</span><span class="sxs-lookup"><span data-stu-id="c959f-122">If you provide a local version of [!INCLUDE[d365fin](includes/d365fin_md.md)], you should review this table and consider any local language issues.</span></span>

## <a name="about-data-tables"></a><span data-ttu-id="c959f-123">Om datatabeller</span><span class="sxs-lookup"><span data-stu-id="c959f-123">About Data Tables</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="c959f-124">-datatabeller leveres i to grundlæggende typer: Master og Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c959f-124">, data tables come in two basic types: Master and Setup.</span></span> <span data-ttu-id="c959f-125">Når du konfigurerer en virksomhedskonfiguration, kan du bruge disse typer for at fokusere din konfigurationsstrategi.</span><span class="sxs-lookup"><span data-stu-id="c959f-125">When you are setting up a company configuration, you can use these types to focus your configuration strategy.</span></span>  

### <a name="master-data-tables"></a><span data-ttu-id="c959f-126">Masterdatatabeller</span><span class="sxs-lookup"><span data-stu-id="c959f-126">Master Data Tables</span></span>  
<span data-ttu-id="c959f-127">I følgende tabel vises nogle eksempler på masterdatatabellerne.</span><span class="sxs-lookup"><span data-stu-id="c959f-127">The following table lists some of the master data tables.</span></span> <span data-ttu-id="c959f-128">Når du starter en ny virksomhed, vil disse tabeller være tomme.</span><span class="sxs-lookup"><span data-stu-id="c959f-128">When you initialize a new company, these tables are empty.</span></span>  

|<span data-ttu-id="c959f-129">Tabel-id</span><span class="sxs-lookup"><span data-stu-id="c959f-129">Table No.</span></span>|<span data-ttu-id="c959f-130">Tabelnavn</span><span class="sxs-lookup"><span data-stu-id="c959f-130">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="c959f-131">15</span><span class="sxs-lookup"><span data-stu-id="c959f-131">15</span></span>|<span data-ttu-id="c959f-132">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="c959f-132">G/L Account</span></span>|  
|<span data-ttu-id="c959f-133">18</span><span class="sxs-lookup"><span data-stu-id="c959f-133">18</span></span>|<span data-ttu-id="c959f-134">Kunde</span><span class="sxs-lookup"><span data-stu-id="c959f-134">Customer</span></span>|  
|<span data-ttu-id="c959f-135">23</span><span class="sxs-lookup"><span data-stu-id="c959f-135">23</span></span>|<span data-ttu-id="c959f-136">Kreditor</span><span class="sxs-lookup"><span data-stu-id="c959f-136">Vendor</span></span>|  
|<span data-ttu-id="c959f-137">27</span><span class="sxs-lookup"><span data-stu-id="c959f-137">27</span></span>|<span data-ttu-id="c959f-138">Vare</span><span class="sxs-lookup"><span data-stu-id="c959f-138">Item</span></span>|  
|<span data-ttu-id="c959f-139">5050</span><span class="sxs-lookup"><span data-stu-id="c959f-139">5050</span></span>|<span data-ttu-id="c959f-140">Kontakt</span><span class="sxs-lookup"><span data-stu-id="c959f-140">Contact</span></span>|  

### <a name="setup-data-tables"></a><span data-ttu-id="c959f-141">Konfigurationsdatatabeller</span><span class="sxs-lookup"><span data-stu-id="c959f-141">Setup Data Tables</span></span>  
<span data-ttu-id="c959f-142">Følgende tabel viser nogle af konfigurationsdatatabeller, hvor du henter konfigurationsoplysninger i konfigurationsspørgeskemaet.</span><span class="sxs-lookup"><span data-stu-id="c959f-142">The following table lists some of the setup data tables, in which you capture setup information in the configuration questionnaire.</span></span> <span data-ttu-id="c959f-143">Disse tabeller indeholder basisoplysninger, når virksomheden oprettes.</span><span class="sxs-lookup"><span data-stu-id="c959f-143">These tables contain baseline information when the company is created.</span></span>  

|<span data-ttu-id="c959f-144">Tabel-id</span><span class="sxs-lookup"><span data-stu-id="c959f-144">Table No.</span></span>|<span data-ttu-id="c959f-145">Tabelnavn</span><span class="sxs-lookup"><span data-stu-id="c959f-145">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="c959f-146">98</span><span class="sxs-lookup"><span data-stu-id="c959f-146">98</span></span>|<span data-ttu-id="c959f-147">Opsætning af Finans</span><span class="sxs-lookup"><span data-stu-id="c959f-147">General Ledger Setup</span></span>|  
|<span data-ttu-id="c959f-148">311</span><span class="sxs-lookup"><span data-stu-id="c959f-148">311</span></span>|<span data-ttu-id="c959f-149">Salgsopsætning</span><span class="sxs-lookup"><span data-stu-id="c959f-149">Sales & Receivables Setup</span></span>|  
|<span data-ttu-id="c959f-150">312</span><span class="sxs-lookup"><span data-stu-id="c959f-150">312</span></span>|<span data-ttu-id="c959f-151">Købsopsætning</span><span class="sxs-lookup"><span data-stu-id="c959f-151">Purchases & Payables Setup</span></span>|  
|<span data-ttu-id="c959f-152">313</span><span class="sxs-lookup"><span data-stu-id="c959f-152">313</span></span>|<span data-ttu-id="c959f-153">Opsætning af Lager</span><span class="sxs-lookup"><span data-stu-id="c959f-153">Inventory Setup</span></span>|  

<span data-ttu-id="c959f-154">Ud over konfigurationsdatatabeller har [!INCLUDE[d365fin](includes/d365fin_md.md)] også datatabeller med opsætningstype, der angiver centrale oplysninger om virksomheden og dens forretningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="c959f-154">In addition to setup data tables, [!INCLUDE[d365fin](includes/d365fin_md.md)] also has setup-type data tables that specify core information about the company and its business processes.</span></span> <span data-ttu-id="c959f-155">Følgende tabel indeholder nogle af dem.</span><span class="sxs-lookup"><span data-stu-id="c959f-155">The following table lists some of them.</span></span>  

|<span data-ttu-id="c959f-156">Tabel-id</span><span class="sxs-lookup"><span data-stu-id="c959f-156">Table No.</span></span>|<span data-ttu-id="c959f-157">Tabelnavn</span><span class="sxs-lookup"><span data-stu-id="c959f-157">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="c959f-158">3</span><span class="sxs-lookup"><span data-stu-id="c959f-158">3</span></span>|<span data-ttu-id="c959f-159">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="c959f-159">Payment Terms</span></span>|  
|<span data-ttu-id="c959f-160">4</span><span class="sxs-lookup"><span data-stu-id="c959f-160">4</span></span>|<span data-ttu-id="c959f-161">Valuta</span><span class="sxs-lookup"><span data-stu-id="c959f-161">Currency</span></span>|  
|<span data-ttu-id="c959f-162">6</span><span class="sxs-lookup"><span data-stu-id="c959f-162">6</span></span>|<span data-ttu-id="c959f-163">Debitorprisgrupper</span><span class="sxs-lookup"><span data-stu-id="c959f-163">Customer Price Groups</span></span>|  
|<span data-ttu-id="c959f-164">5700</span><span class="sxs-lookup"><span data-stu-id="c959f-164">5700</span></span>|<span data-ttu-id="c959f-165">Lagervare (pr. lok.)</span><span class="sxs-lookup"><span data-stu-id="c959f-165">Stockkeeping Unit</span></span>|

  

## <a name="see-also"></a><span data-ttu-id="c959f-166">Se også</span><span class="sxs-lookup"><span data-stu-id="c959f-166">See Also</span></span>  
[<span data-ttu-id="c959f-167">Anvende konfigurationer på nye virksomheder</span><span class="sxs-lookup"><span data-stu-id="c959f-167">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="c959f-168">Oprette en virksomhed med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="c959f-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="c959f-169">Opsætning</span><span class="sxs-lookup"><span data-stu-id="c959f-169">Administration</span></span>](admin-setup-and-administration.md)

