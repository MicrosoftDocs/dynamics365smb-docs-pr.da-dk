---
title: Sådan oprettes brugerdefinerede virksomhedsskabeloner | Microsoft Docs
description: Efterhånden som din virksomhed vokser, vil du sandsynligvis have oprettet et sæt virksomhedstyper, som du kan bruge til de fleste af dine kunder. Du kan strømline implementeringsprocessen ved at gøre disse typiske typer til virksomhedskonfigurationsskabeloner, der kan genbruges.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e6781b01a80acfd3431fc000069dd2c8b96dffc5
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779903"
---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="285bb-104">Oprette brugerdefinerede virksomhedsskabeloner</span><span class="sxs-lookup"><span data-stu-id="285bb-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="285bb-105">Efterhånden som din virksomhed vokser, vil du sandsynligvis have oprettet et sæt virksomhedstyper, som du kan bruge til de fleste af dine kunder.</span><span class="sxs-lookup"><span data-stu-id="285bb-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="285bb-106">Du kan strømline implementeringsprocessen ved at gøre disse typiske typer til virksomhedskonfigurationsskabeloner, der kan genbruges.</span><span class="sxs-lookup"><span data-stu-id="285bb-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="285bb-107">Generelt skal du oprette en konfigurationspakke pr. funktionsområde. Du skal f.eks. oprette en pakke til produktionsfunktionerne.</span><span class="sxs-lookup"><span data-stu-id="285bb-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="285bb-108">På den måde kan du anvende og konfigurere nye områder i en virksomhed, efterhånden som du har brug for dem.</span><span class="sxs-lookup"><span data-stu-id="285bb-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="285bb-109">En anden fremgangsmåde er at oprette en pakke, der indeholder de tabeller, der definerer konfigurationen, som følgende:</span><span class="sxs-lookup"><span data-stu-id="285bb-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="285bb-110">Anlægsopsætning</span><span class="sxs-lookup"><span data-stu-id="285bb-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="285bb-111">Opsætning af Finans</span><span class="sxs-lookup"><span data-stu-id="285bb-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="285bb-112">Opsætning af Lager</span><span class="sxs-lookup"><span data-stu-id="285bb-112">Inventory Setup</span></span>  
-   <span data-ttu-id="285bb-113">Produktionsopsætning</span><span class="sxs-lookup"><span data-stu-id="285bb-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="285bb-114">Købsopsætning</span><span class="sxs-lookup"><span data-stu-id="285bb-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="285bb-115">Marketingopsætning</span><span class="sxs-lookup"><span data-stu-id="285bb-115">Marketing Setup</span></span>  
-   <span data-ttu-id="285bb-116">Serviceopsætning</span><span class="sxs-lookup"><span data-stu-id="285bb-116">Service Setup</span></span>  
-   <span data-ttu-id="285bb-117">Salgsopsætning</span><span class="sxs-lookup"><span data-stu-id="285bb-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="285bb-118">Logistikopsætning</span><span class="sxs-lookup"><span data-stu-id="285bb-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="285bb-119">Bogføringsopsætning</span><span class="sxs-lookup"><span data-stu-id="285bb-119">General Posting Setup</span></span>  
-   <span data-ttu-id="285bb-120">Momsbogf.opsætning</span><span class="sxs-lookup"><span data-stu-id="285bb-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="285bb-121">Opsætning af varebogføring</span><span class="sxs-lookup"><span data-stu-id="285bb-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="285bb-122">For at få vist en komplet liste over opsætningstabeller skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angive **Manuel opsætning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="285bb-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Manual Setup**, and then choose the related link.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="285bb-123">Vær forsigtig, hvis du vælger tabeller eller felter, der har samme stinavn, men er adskilt med specialtegn som f.eks .%, &, <, >, (og).</span><span class="sxs-lookup"><span data-stu-id="285bb-123">Use caution if you choose tables or fields that have the same temporal name but are differentiated by special characters, such as %, &, <, >, (, and ).</span></span> <span data-ttu-id="285bb-124">F.eks. kan tabellen "XYZ" indeholde felterne "Felt 1" og "Felt 1%".</span><span class="sxs-lookup"><span data-stu-id="285bb-124">For example, table "XYZ" might contain the "Field 1" and "Field 1%" fields.</span></span>
>
> <span data-ttu-id="285bb-125">XML-behandleren accepterer kun specialtegn og fjerner dem, den ikke accepterer.</span><span class="sxs-lookup"><span data-stu-id="285bb-125">The XML processor accepts only some special characters, and will remove those it does not.</span></span> <span data-ttu-id="285bb-126">Hvis der fjernes et specialtegn som f.eks. %-tegnet i "Felt 1%", er der to eller flere tabeller eller felter med samme navn, og der opstår en fejl, når du eksporterer eller importerer en konfigurationspakke.</span><span class="sxs-lookup"><span data-stu-id="285bb-126">If removing a special character, such as the % sign in "Field 1%," results in two or more tables or fields with the same name an error will occur when you export or import a configuration package.</span></span>

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="285bb-127">Sådan oprettes en brugerdefineret virksomhedskonfigurationspakke</span><span class="sxs-lookup"><span data-stu-id="285bb-127">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="285bb-128">Oprette en ny virksomhed.</span><span class="sxs-lookup"><span data-stu-id="285bb-128">Create a new company.</span></span> <span data-ttu-id="285bb-129">Du kan finde flere oplysninger i [Oprettelse af ny virksomheder i Business Central](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="285bb-129">For more information, see [Creating New Companies in Business Central](about-new-company.md).</span></span>  
3.  <span data-ttu-id="285bb-130">Konfigurer den nye virksomhed på den måde, som du har brug for.</span><span class="sxs-lookup"><span data-stu-id="285bb-130">Set up the new company in the way you need.</span></span> <span data-ttu-id="285bb-131">Udfyld alle nødvendige konfigurationstabeller.</span><span class="sxs-lookup"><span data-stu-id="285bb-131">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="285bb-132">Åbn det nye regnskab.</span><span class="sxs-lookup"><span data-stu-id="285bb-132">Open the new company.</span></span>
5. <span data-ttu-id="285bb-133">Åbn siden **Konfigurationskladde**.</span><span class="sxs-lookup"><span data-stu-id="285bb-133">Open the **Configuration Worksheet** page.</span></span>  
6.  <span data-ttu-id="285bb-134">Tilføj de tabeller, du vil overføre til en anden virksomhed, til regnearket.</span><span class="sxs-lookup"><span data-stu-id="285bb-134">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="285bb-135">Tildel kladdelinjerne til pakken.</span><span class="sxs-lookup"><span data-stu-id="285bb-135">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="285bb-136">Opret et spørgeskema til de hyppigst anvendte konfigurationstabeller.</span><span class="sxs-lookup"><span data-stu-id="285bb-136">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="285bb-137">Opret konfigurationsskabeloner til at gøre det lettere at oprette masterdata, f.eks. kunder eller varer.</span><span class="sxs-lookup"><span data-stu-id="285bb-137">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="285bb-138">Udlæs pakken som en .rapidstart-fil.</span><span class="sxs-lookup"><span data-stu-id="285bb-138">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="285bb-139">Se også</span><span class="sxs-lookup"><span data-stu-id="285bb-139">See Also</span></span>  
[<span data-ttu-id="285bb-140">Oprette en virksomhed med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="285bb-140">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="285bb-141">Opsætning</span><span class="sxs-lookup"><span data-stu-id="285bb-141">Administration</span></span>](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]