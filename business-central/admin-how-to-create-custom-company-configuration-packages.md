---
title: "Sådan oprettes brugerdefinerede virksomhedsskabeloner | Microsoft Docs"
description: "Efterhånden som din virksomhed vokser, vil du sandsynligvis have oprettet et sæt virksomhedstyper, som du kan bruge til de fleste af dine kunder. Du kan strømline implementeringsprocessen ved at gøre disse typiske typer til virksomhedskonfigurationsskabeloner, der kan genbruges."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/07/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: a51628085e640cc2e5f022272eccb89d5cec38b7
ms.contentlocale: da-dk
ms.lasthandoff: 12/11/2018

---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="6f0fd-104">Oprette brugerdefinerede virksomhedsskabeloner</span><span class="sxs-lookup"><span data-stu-id="6f0fd-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="6f0fd-105">Efterhånden som din virksomhed vokser, vil du sandsynligvis have oprettet et sæt virksomhedstyper, som du kan bruge til de fleste af dine kunder.</span><span class="sxs-lookup"><span data-stu-id="6f0fd-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="6f0fd-106">Du kan strømline implementeringsprocessen ved at gøre disse typiske typer til virksomhedskonfigurationsskabeloner, der kan genbruges.</span><span class="sxs-lookup"><span data-stu-id="6f0fd-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="6f0fd-107">Generelt skal du oprette en konfigurationspakke pr. funktionsområde. Du skal f.eks. oprette en pakke til produktionsfunktionerne.</span><span class="sxs-lookup"><span data-stu-id="6f0fd-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="6f0fd-108">På den måde kan du anvende og konfigurere nye områder i en virksomhed, efterhånden som du har brug for dem.</span><span class="sxs-lookup"><span data-stu-id="6f0fd-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="6f0fd-109">En anden fremgangsmåde er at oprette en pakke, der indeholder de tabeller, der definerer konfigurationen, som følgende:</span><span class="sxs-lookup"><span data-stu-id="6f0fd-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="6f0fd-110">Anlægsopsætning</span><span class="sxs-lookup"><span data-stu-id="6f0fd-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="6f0fd-111">Opsætning af Finans</span><span class="sxs-lookup"><span data-stu-id="6f0fd-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="6f0fd-112">Opsætning af Lager</span><span class="sxs-lookup"><span data-stu-id="6f0fd-112">Inventory Setup</span></span>  
-   <span data-ttu-id="6f0fd-113">Produktionsopsætning</span><span class="sxs-lookup"><span data-stu-id="6f0fd-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="6f0fd-114">Købsopsætning</span><span class="sxs-lookup"><span data-stu-id="6f0fd-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="6f0fd-115">Marketingopsætning</span><span class="sxs-lookup"><span data-stu-id="6f0fd-115">Marketing Setup</span></span>  
-   <span data-ttu-id="6f0fd-116">Serviceopsætning</span><span class="sxs-lookup"><span data-stu-id="6f0fd-116">Service Setup</span></span>  
-   <span data-ttu-id="6f0fd-117">Salgsopsætning</span><span class="sxs-lookup"><span data-stu-id="6f0fd-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="6f0fd-118">Logistikopsætning</span><span class="sxs-lookup"><span data-stu-id="6f0fd-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="6f0fd-119">Bogføringsopsætning</span><span class="sxs-lookup"><span data-stu-id="6f0fd-119">General Posting Setup</span></span>  
-   <span data-ttu-id="6f0fd-120">Momsbogf.opsætning</span><span class="sxs-lookup"><span data-stu-id="6f0fd-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="6f0fd-121">Opsætning af varebogføring</span><span class="sxs-lookup"><span data-stu-id="6f0fd-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="6f0fd-122">For at få vist en komplet liste over opsætningstabeller skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Manuel opsætning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="6f0fd-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Manual Setup**, and then choose the related link.</span></span>  

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="6f0fd-123">Sådan oprettes en brugerdefineret virksomhedskonfigurationspakke</span><span class="sxs-lookup"><span data-stu-id="6f0fd-123">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="6f0fd-124">Oprette en ny virksomhed.</span><span class="sxs-lookup"><span data-stu-id="6f0fd-124">Create a new company.</span></span> <span data-ttu-id="6f0fd-125">Du kan finde flere oplysninger i [Oprettelse af ny virksomheder i Business Central](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="6f0fd-125">For more information, see [Creating New Companies in Business Central](about-new-company.md).</span></span>  
3.  <span data-ttu-id="6f0fd-126">Konfigurer den nye virksomhed på den måde, som du har brug for.</span><span class="sxs-lookup"><span data-stu-id="6f0fd-126">Set up the new company in the way you need.</span></span> <span data-ttu-id="6f0fd-127">Udfyld alle nødvendige konfigurationstabeller.</span><span class="sxs-lookup"><span data-stu-id="6f0fd-127">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="6f0fd-128">Åbn det nye regnskab.</span><span class="sxs-lookup"><span data-stu-id="6f0fd-128">Open the new company.</span></span>
5. <span data-ttu-id="6f0fd-129">Åbn siden **Konfigurationskladde**.</span><span class="sxs-lookup"><span data-stu-id="6f0fd-129">Open the **Configuration Worksheet** page.</span></span>  
6.  <span data-ttu-id="6f0fd-130">Tilføj de tabeller, du vil overføre til en anden virksomhed, til regnearket.</span><span class="sxs-lookup"><span data-stu-id="6f0fd-130">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="6f0fd-131">Tildel kladdelinjerne til pakken.</span><span class="sxs-lookup"><span data-stu-id="6f0fd-131">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="6f0fd-132">Opret et spørgeskema til de hyppigst anvendte konfigurationstabeller.</span><span class="sxs-lookup"><span data-stu-id="6f0fd-132">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="6f0fd-133">Opret konfigurationsskabeloner til at gøre det lettere at oprette masterdata, f.eks. kunder eller varer.</span><span class="sxs-lookup"><span data-stu-id="6f0fd-133">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="6f0fd-134">Udlæs pakken som en .rapidstart-fil.</span><span class="sxs-lookup"><span data-stu-id="6f0fd-134">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6f0fd-135">Se også</span><span class="sxs-lookup"><span data-stu-id="6f0fd-135">See Also</span></span>  
[<span data-ttu-id="6f0fd-136">Oprette en virksomhed med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="6f0fd-136">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="6f0fd-137">Opsætning</span><span class="sxs-lookup"><span data-stu-id="6f0fd-137">Administration</span></span>](admin-setup-and-administration.md)

