---
title: "Sådan oprettes brugerdefinerede virksomhedsskabeloner | Microsoft Docs"
description: "Efterhånden som din virksomhed vokser, vil du sandsynligvis have oprettet et sæt virksomhedstyper, som du kan bruge til de fleste af dine kunder. Du kan strømline implementeringsprocessen ved at gøre disse typiske typer til virksomhedskonfigurationsskabeloner, der kan genbruges."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 37fe7a482b88626adff1ef16496a785399d19a8d
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="feb69-104">Oprette brugerdefinerede virksomhedsskabeloner</span><span class="sxs-lookup"><span data-stu-id="feb69-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="feb69-105">Efterhånden som din virksomhed vokser, vil du sandsynligvis have oprettet et sæt virksomhedstyper, som du kan bruge til de fleste af dine kunder.</span><span class="sxs-lookup"><span data-stu-id="feb69-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="feb69-106">Du kan strømline implementeringsprocessen ved at gøre disse typiske typer til virksomhedskonfigurationsskabeloner, der kan genbruges.</span><span class="sxs-lookup"><span data-stu-id="feb69-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="feb69-107">Generelt skal du oprette en konfigurationspakke pr. funktionsområde. Du skal f.eks. oprette en pakke til produktionsfunktionerne.</span><span class="sxs-lookup"><span data-stu-id="feb69-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="feb69-108">På den måde kan du anvende og konfigurere nye områder i en virksomhed, efterhånden som du har brug for dem.</span><span class="sxs-lookup"><span data-stu-id="feb69-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="feb69-109">En anden fremgangsmåde er at oprette en pakke, der indeholder de tabeller, der definerer konfigurationen, som følgende:</span><span class="sxs-lookup"><span data-stu-id="feb69-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="feb69-110">Anlægsopsætning</span><span class="sxs-lookup"><span data-stu-id="feb69-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="feb69-111">Opsætning af Finans</span><span class="sxs-lookup"><span data-stu-id="feb69-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="feb69-112">Opsætning af Lager</span><span class="sxs-lookup"><span data-stu-id="feb69-112">Inventory Setup</span></span>  
-   <span data-ttu-id="feb69-113">Produktionsopsætning</span><span class="sxs-lookup"><span data-stu-id="feb69-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="feb69-114">Købsopsætning</span><span class="sxs-lookup"><span data-stu-id="feb69-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="feb69-115">Marketingopsætning</span><span class="sxs-lookup"><span data-stu-id="feb69-115">Marketing Setup</span></span>  
-   <span data-ttu-id="feb69-116">Serviceopsætning</span><span class="sxs-lookup"><span data-stu-id="feb69-116">Service Setup</span></span>  
-   <span data-ttu-id="feb69-117">Salgsopsætning</span><span class="sxs-lookup"><span data-stu-id="feb69-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="feb69-118">Logistikopsætning</span><span class="sxs-lookup"><span data-stu-id="feb69-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="feb69-119">Bogføringsopsætning</span><span class="sxs-lookup"><span data-stu-id="feb69-119">General Posting Setup</span></span>  
-   <span data-ttu-id="feb69-120">Momsbogf.opsætning</span><span class="sxs-lookup"><span data-stu-id="feb69-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="feb69-121">Opsætning af varebogføring</span><span class="sxs-lookup"><span data-stu-id="feb69-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="feb69-122">Hvis du vil se en fuldstændig liste over opsætningstabeller, skal du vælge ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Opsætning** og derefter vælge det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="feb69-122">To see a complete list of setup tables, Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Setup**, and then choose the related link.</span></span>  

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="feb69-123">Sådan oprettes en brugerdefineret virksomhedskonfigurationspakke</span><span class="sxs-lookup"><span data-stu-id="feb69-123">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="feb69-124">Oprette et ny [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="feb69-124">Create a new [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="feb69-125">***IKKE muligt Link til hjælp til "Oprette en ny lejer"***.</span><span class="sxs-lookup"><span data-stu-id="feb69-125">***NOT POSSIBLE Link to help for "Creating a New Tenant"***.</span></span>   
2.  <span data-ttu-id="feb69-126">Oprette en ny virksomhed for skabelonen industri eller løsning.</span><span class="sxs-lookup"><span data-stu-id="feb69-126">Create a new company for the industry or solution template.</span></span> <span data-ttu-id="feb69-127">Du kan finde flere oplysninger i [Oprette en ny virksomhed](admin-how-to-create-a-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="feb69-127">For more information, see [Create a New Company](admin-how-to-create-a-new-company.md).</span></span>  
3.  <span data-ttu-id="feb69-128">Konfigurer den nye virksomhed på den måde, som du har brug for.</span><span class="sxs-lookup"><span data-stu-id="feb69-128">Setup the new company in the way you need.</span></span> <span data-ttu-id="feb69-129">Udfyld alle nødvendige konfigurationstabeller.</span><span class="sxs-lookup"><span data-stu-id="feb69-129">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="feb69-130">Åbn det nye regnskab.</span><span class="sxs-lookup"><span data-stu-id="feb69-130">Open the new company.</span></span>
5. <span data-ttu-id="feb69-131">Åbn vinduet **Konfigurationsregneark**.</span><span class="sxs-lookup"><span data-stu-id="feb69-131">Open the **Configuration Worksheet** window.</span></span>  
6.  <span data-ttu-id="feb69-132">Tilføj de tabeller, du vil overføre til en anden virksomhed, til regnearket.</span><span class="sxs-lookup"><span data-stu-id="feb69-132">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="feb69-133">Tildel kladdelinjerne til pakken.</span><span class="sxs-lookup"><span data-stu-id="feb69-133">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="feb69-134">Opret et spørgeskema til de hyppigst anvendte konfigurationstabeller.</span><span class="sxs-lookup"><span data-stu-id="feb69-134">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="feb69-135">Opret konfigurationsskabeloner til at gøre det lettere at oprette masterdata, f.eks. kunder eller varer.</span><span class="sxs-lookup"><span data-stu-id="feb69-135">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="feb69-136">Udlæs pakken som en .rapidstart-fil.</span><span class="sxs-lookup"><span data-stu-id="feb69-136">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="feb69-137">Se også</span><span class="sxs-lookup"><span data-stu-id="feb69-137">See Also</span></span>  
[<span data-ttu-id="feb69-138">Oprette en virksomhed med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="feb69-138">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="feb69-139">Opsætning</span><span class="sxs-lookup"><span data-stu-id="feb69-139">Administration</span></span>](admin-setup-and-administration.md)

