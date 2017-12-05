---
title: "Oprette nye virksomheder ved hjælp af en assisterende opsætningsvejledning | Microsoft Docs"
description: "Det er nemt at oprette en ny, tom virksomhed i Dynamics 365 Business edition. En assisterede opsætningsvejledning hjælper dig gennem trinene, og du kan indlæse eksisterende forretningsdata."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.date: 07/14/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: c4152a77fcd3e5995aaf09c17b0a3a2c227aa2fa
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="creating-new-companies-in-included365finlongincludesd365finlongmdmd"></a><span data-ttu-id="d1a85-104">Oprettelse af nye virksomheder i [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]</span><span class="sxs-lookup"><span data-stu-id="d1a85-104">Creating New Companies in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]</span></span>
<span data-ttu-id="d1a85-105">I [!INCLUDE[d365fin](includes/d365fin_md.md)] bliver beholdere til forretningsdata, der hører til en afdeling eller en juridisk enhed, kaldet en *virksomhed*.</span><span class="sxs-lookup"><span data-stu-id="d1a85-105">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the containers for business data that belongs to a business unit or legal entity is referred to as a *company*.</span></span> <span data-ttu-id="d1a85-106">Når du logger på [!INCLUDE[d365fin](includes/d365fin_md.md)], får du angivet en demonstrationsvirksomhed og en tom virksomhed, *Min virksomhed*.</span><span class="sxs-lookup"><span data-stu-id="d1a85-106">When you sign up for [!INCLUDE[d365fin](includes/d365fin_md.md)], you are given a demonstration company and an empty company, *My Company*.</span></span> <span data-ttu-id="d1a85-107">Det er nemt at skifte mellem virksomhederne – du skal bare gå til **Mine indstillinger** og flytte til den anden virksomhed.</span><span class="sxs-lookup"><span data-stu-id="d1a85-107">Switching between the companies is easy - just got to **My Settings** and move to the other company.</span></span> <span data-ttu-id="d1a85-108">Men du kan også oprette nye virksomheder i [!INCLUDE[d365fin](includes/d365fin_md.md)], afhængigt af dine forretningsmæssige behov.</span><span class="sxs-lookup"><span data-stu-id="d1a85-108">But you can also create new companies in [!INCLUDE[d365fin](includes/d365fin_md.md)], depending on your business needs.</span></span> <span data-ttu-id="d1a85-109">Når du opretter en ny virksomhed, hjælper en assisterede opsætningsvejledning dig med at få styr på det grundlæggende.</span><span class="sxs-lookup"><span data-stu-id="d1a85-109">When you create a new company, an assisted setup guide helps you get the basics in place.</span></span> <span data-ttu-id="d1a85-110">Du kan derefter indlæse relevante data fra dit gamle system eller en anden virksomhed i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d1a85-110">Then, you can import relevant data from your legacy system or another company in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="create-new-company"></a><span data-ttu-id="d1a85-111">Opret ny virksomhed</span><span class="sxs-lookup"><span data-stu-id="d1a85-111">Create New Company</span></span>
<span data-ttu-id="d1a85-112">Hvis du vil indsætte en virksomhed i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du bruge den assisterende opsætningsguide **Opret ny virksomhed** for at komme i gang.</span><span class="sxs-lookup"><span data-stu-id="d1a85-112">If you decide to add a company to your [!INCLUDE[d365fin](includes/d365fin_md.md)], you can use the **Create New Company** assisted setup wizard to get you started.</span></span> <span data-ttu-id="d1a85-113">Opsætningsguiden er tilgængelig fra vinduet **Virksomheder** og fra opslag i feltet **Virksomhed** i **Mine indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="d1a85-113">The setup wizard is available from the **Companies** window and from the lookup in the **Company** field in **My Settings**.</span></span>  

<span data-ttu-id="d1a85-114">Opsætningsguiden indeholder tre skabeloner:</span><span class="sxs-lookup"><span data-stu-id="d1a85-114">The setup wizard offers three templates:</span></span>

-   <span data-ttu-id="d1a85-115">**Suite-evaluering**</span><span class="sxs-lookup"><span data-stu-id="d1a85-115">**Suite Evaluation**</span></span>  
    <span data-ttu-id="d1a85-116">Den opretter en virksomhed, der ligner demonstrationsvirksomheden med eksempeldata og opsætningsdata.</span><span class="sxs-lookup"><span data-stu-id="d1a85-116">This creates a company that is similar to the demonstration company with sample data and setup data.</span></span>  
-   <span data-ttu-id="d1a85-117">**Suite-produktion**</span><span class="sxs-lookup"><span data-stu-id="d1a85-117">**Suite Production**</span></span>  
    <span data-ttu-id="d1a85-118">Den opretter en virksomhed, der ligner **Min virksomhed** med opsætningsdata, men uden eksempeldata.</span><span class="sxs-lookup"><span data-stu-id="d1a85-118">This creates a company that is similar to **My Company** with setup data but without sample data.</span></span>  
-   <span data-ttu-id="d1a85-119">**Nyt**</span><span class="sxs-lookup"><span data-stu-id="d1a85-119">**New**</span></span>  
    <span data-ttu-id="d1a85-120">Der oprettes en tom virksomhed uden opsætningsdata.</span><span class="sxs-lookup"><span data-stu-id="d1a85-120">This creates a blank company without setup data.</span></span>  

<span data-ttu-id="d1a85-121">Hvis du vil komme hurtigt i gang med en ny virksomhed, kan du vælge **Suite-produktion** og derefter importere dine egne forretningsdata, som f.eks. debitorer, varer og kreditorer.</span><span class="sxs-lookup"><span data-stu-id="d1a85-121">If you want to get started easily with a new company, choose **Suite Production** and then import your own business data, such as customers, items, and vendors.</span></span> <span data-ttu-id="d1a85-122">Vælg skabelonen **Nyt**, hvis du vil oprette alt fra bunden.</span><span class="sxs-lookup"><span data-stu-id="d1a85-122">Choose the **New** template if you want to set everything up from scratch.</span></span> <span data-ttu-id="d1a85-123">I så fald kan du bruge den assisterende opsætningsguide **Virksomhedsopsætning** til at hjælpe dig i gang med de vigtige opsætningsdata.</span><span class="sxs-lookup"><span data-stu-id="d1a85-123">In that case, you can use the **Company Setup** assisted setup wizard to help you get started with essential setup data.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="d1a85-124">Når du opretter en ny virksomhed, tager det nogle minutter, før du kan få adgang til den i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d1a85-124">When you create a new company, it takes a few minutes before you can access it in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="d1a85-125">Opsætningsstatussen i vinduet **Virksomheder** vises som standard, når den nye virksomhed er klar til dig.</span><span class="sxs-lookup"><span data-stu-id="d1a85-125">The setup status in the **Companies** window shows when the new company is ready for you.</span></span> <span data-ttu-id="d1a85-126">Derefter kan du skifte til den nye virksomhed ved hjælp af **Mine indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="d1a85-126">Then, you can switch to the new company by using **My Settings**.</span></span>  

<span data-ttu-id="d1a85-127">Under din 30-dages prøveperiode kan du oprette et ubegrænset antal nye virksomheder, men de er kun tilgængelige under prøveperioden.</span><span class="sxs-lookup"><span data-stu-id="d1a85-127">During your 30 day trial, you can create any number of new companies, but they will only be available during your trial.</span></span> <span data-ttu-id="d1a85-128">Kontakt din [!INCLUDE[d365fin](includes/d365fin_md.md)]-partner for at få yderligere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="d1a85-128">For more information, contact your [!INCLUDE[d365fin](includes/d365fin_md.md)] partner.</span></span>  

## <a name="company-setup"></a><span data-ttu-id="d1a85-129">Virksomhedsopsætning</span><span class="sxs-lookup"><span data-stu-id="d1a85-129">Company Setup</span></span>
<span data-ttu-id="d1a85-130">Når du logger på en ny virksomhed, kører guiden **Virksomhedsopsætning** automatisk og hjælper dig i gang.</span><span class="sxs-lookup"><span data-stu-id="d1a85-130">When you sign in to a new company, the **Company Setup** wizard runs automatically and helps you get started.</span></span> <span data-ttu-id="d1a85-131">Du bliver bedt om at angive oplysninger om virksomheden, f.eks. adresse, bankoplysninger og lagerets kostmetode.</span><span class="sxs-lookup"><span data-stu-id="d1a85-131">You will be asked for information about your business, such as the address, bank details, and inventory costing method.</span></span> <span data-ttu-id="d1a85-132">Vi beder dig om disse oplysninger, fordi de bruges som udgangspunkt for mange områder i [!INCLUDE[d365fin](includes/d365fin_md.md)], som du så derefter ikke behøver at oprette manuelt senere.</span><span class="sxs-lookup"><span data-stu-id="d1a85-132">We ask for this information because it is used as a basis for many areas in [!INCLUDE[d365fin](includes/d365fin_md.md)] that you will then not have to set up manually later.</span></span>  

<span data-ttu-id="d1a85-133">Din virksomhedsadresse medtages f.eks. i fakturaer og andre dokumenter, bankoplysningerne bruges i betalinger, og kostmetoden bruges til at beregne priser samt lagerværdi.</span><span class="sxs-lookup"><span data-stu-id="d1a85-133">For example, your company address is included in invoices and other documents, your bank information is used in payments, and the costing method is used to calculate prices as well as inventory valuation.</span></span>  

<span data-ttu-id="d1a85-134">Når du har styr på det grundlæggende, kan du oprette de resterende centrale områder.</span><span class="sxs-lookup"><span data-stu-id="d1a85-134">Once you have the basics in place, you can set up remaining core areas.</span></span> <span data-ttu-id="d1a85-135">Du er klar til at tilføje forretningsdata, f.eks. debitorer og kreditorer.</span><span class="sxs-lookup"><span data-stu-id="d1a85-135">Then, you are ready to add business data, such as customers and vendors.</span></span> <span data-ttu-id="d1a85-136">Du kan finde flere oplysninger i [Konfigurere Dynamics 365 Business edition](setup.md).</span><span class="sxs-lookup"><span data-stu-id="d1a85-136">For more information, see [Setting Up Dynamics 365 Business edition ](setup.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="d1a85-137">Se også</span><span class="sxs-lookup"><span data-stu-id="d1a85-137">See Also</span></span>
[<span data-ttu-id="d1a85-138">Konfigurere Dynamics 365 Business edition</span><span class="sxs-lookup"><span data-stu-id="d1a85-138">Setting Up Dynamics 365 Business edition </span></span>](setup.md)  
[<span data-ttu-id="d1a85-139">Importere virksomhedsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="d1a85-139">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="d1a85-140">Ændring af grundlæggende indstillinger</span><span class="sxs-lookup"><span data-stu-id="d1a85-140">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
<span data-ttu-id="d1a85-141">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="d1a85-141">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
