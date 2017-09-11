---
title: "Definere anlægsforsikring | Microsoft Docs"
description: "Når du vil administrere forsikringsdækning for anlægsaktiver, skal du konfigurere et forsikringskort og nogle generelle forsikringsoplysninger pr. police."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 8e88002c920e392cd61f2a899811fd0434d8cb4b
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-fixed-asset-insurance"></a><span data-ttu-id="6cb82-103">Fremgangsmåde: Konfigurere forsikring af anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="6cb82-103">How to: Set Up Fixed Asset Insurance</span></span>
<span data-ttu-id="6cb82-104">Hvis du vil administrere forsikringsdækning for anlægsaktiver, skal du først angive nogle generelle forsikringsoplysninger og forsikringskort pr. police.</span><span class="sxs-lookup"><span data-stu-id="6cb82-104">To manage fixed asset insurance coverage, you must first set up some general insurance information and an insurance card per policy.</span></span>

## <a name="to-set-up-general-insurance-information"></a><span data-ttu-id="6cb82-105">Sådan angives generelle forsikringsoplysninger</span><span class="sxs-lookup"><span data-stu-id="6cb82-105">To set up general insurance information</span></span>
<span data-ttu-id="6cb82-106">Du skal angive nogle generelle forsikringsoplysninger for at bruge forsikringsfunktionerne i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6cb82-106">To use the insurance features in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must set up some general insurance information.</span></span>  

1. <span data-ttu-id="6cb82-107">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlægsaktiver - Opsætning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="6cb82-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA Setups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6cb82-108">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="6cb82-108">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a><span data-ttu-id="6cb82-109">Sådan defineres forsikringstyper</span><span class="sxs-lookup"><span data-stu-id="6cb82-109">To set up insurance types</span></span>
<span data-ttu-id="6cb82-110">Du kan gruppere forsikringspolicer i kategorier, som f.eks. forsikring mod tyveri eller brand.</span><span class="sxs-lookup"><span data-stu-id="6cb82-110">You can group your insurance policies into categories, such as insurance against theft or fire insurance.</span></span> <span data-ttu-id="6cb82-111">Forsikringstyperne bruges på forsikringskortet.</span><span class="sxs-lookup"><span data-stu-id="6cb82-111">The insurance types are used on the insurance card.</span></span>

1. <span data-ttu-id="6cb82-112">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Forsikringstyper**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="6cb82-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Insurance Types**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6cb82-113">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="6cb82-113">Fill in the fields as necessary.</span></span>

## <a name="to-set-up-insurance-cards"></a><span data-ttu-id="6cb82-114">Sådan defineres forsikringskort</span><span class="sxs-lookup"><span data-stu-id="6cb82-114">To set up insurance cards</span></span>
<span data-ttu-id="6cb82-115">Du kan samle oplysninger om hver enkelt forsikringspolice på forsikringskortet.</span><span class="sxs-lookup"><span data-stu-id="6cb82-115">You may accumulate information about each insurance policy on the insurance card.</span></span>  

1. <span data-ttu-id="6cb82-116">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Forsikring**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="6cb82-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Insurance**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6cb82-117">I vinduet **Forsikring** skal du vælge handlingen **Ny** for at oprette et forsikringskort.</span><span class="sxs-lookup"><span data-stu-id="6cb82-117">In the **Insurance** window, choose the **New** action to create a  new insurance card.</span></span>  
3. <span data-ttu-id="6cb82-118">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="6cb82-118">Fill in the fields as necessary.</span></span>

## <a name="to-set-up-insurance-journal-templates"></a><span data-ttu-id="6cb82-119">Sådan defineres forsikringskladdetyper</span><span class="sxs-lookup"><span data-stu-id="6cb82-119">To set up insurance journal templates</span></span>
<span data-ttu-id="6cb82-120">Første gang du åbner vinduet **Forsikringskladde** i [!INCLUDE[d365fin](includes/d365fin_md.md)], oprettes der automatisk en forsikringskladdetype, men du kan oprette flere kladdetyper.</span><span class="sxs-lookup"><span data-stu-id="6cb82-120">[!INCLUDE[d365fin](includes/d365fin_md.md)] automatically creates an insurance journal template the first time that you open the **Insurance Journal** window, but you can set up additional journal templates.</span></span> <span data-ttu-id="6cb82-121">Du kan finde flere oplysninger under [Arbejde med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="6cb82-121">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>  

1. <span data-ttu-id="6cb82-122">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Forsikringskladdetyper**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="6cb82-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Insurance Journal Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6cb82-123">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="6cb82-123">Fill in the fields as necessary.</span></span>

## <a name="to-set-up-insurance-journal-batches"></a><span data-ttu-id="6cb82-124">Sådan defineres forsikringskladdenavne</span><span class="sxs-lookup"><span data-stu-id="6cb82-124">To set up insurance journal batches</span></span>
<span data-ttu-id="6cb82-125">Du kan definere navne i en forsikringskladdetype.</span><span class="sxs-lookup"><span data-stu-id="6cb82-125">You can set up batches in an insurance journal template.</span></span> <span data-ttu-id="6cb82-126">Værdierne i kladdenavnet bruges som standardværdier, hvis felterne ikke er udfyldt på kladdelinjerne.</span><span class="sxs-lookup"><span data-stu-id="6cb82-126">The values in the journal batch are used as default values if the fields are not filled in on the journal lines.</span></span> <span data-ttu-id="6cb82-127">Du kan finde flere oplysninger under [Arbejde med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="6cb82-127">For more information, see [Work with General Journals](ui-work-general-journals.md)</span></span>  

1. <span data-ttu-id="6cb82-128">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Forsikringskladdetyper**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="6cb82-128">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Insurance Journal Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6cb82-129">Markér en forsikringskladdetype, og vælg derefter handlingen **Navne**.</span><span class="sxs-lookup"><span data-stu-id="6cb82-129">Select an insurance journal template, and then choose the **Batches** action.</span></span>
3. <span data-ttu-id="6cb82-130">I vinduet **Forsikringskladdenavne** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="6cb82-130">In the **Insurance Journal Batches** window, fill in the fields as necessary.</span></span>

> [!NOTE]  
>   <span data-ttu-id="6cb82-131">Tallene har en særlig funktion i kladdenavne.</span><span class="sxs-lookup"><span data-stu-id="6cb82-131">Numbers have a special function in journal names.</span></span> <span data-ttu-id="6cb82-132">Hvis et kladdetypenavn eller et kladdenavn indeholder et tal, vil tallet automatisk forøges med 1, hver gang kladden bogføres.</span><span class="sxs-lookup"><span data-stu-id="6cb82-132">If a journal template name or journal batch name contains a number, the number automatically advances by one every time that the journal is posted.</span></span> <span data-ttu-id="6cb82-133">Hvis du f.eks. angiver HH1 i feltet **Navn**, ændres kladdenavnet til HH2, når kladden HH1 er blevet bogført.</span><span class="sxs-lookup"><span data-stu-id="6cb82-133">For example, if HH1 is entered in the **Name** field, the journal name will change to HH2 after the journal named HH1 has been posted.</span></span>

## <a name="see-also"></a><span data-ttu-id="6cb82-134">Se også</span><span class="sxs-lookup"><span data-stu-id="6cb82-134">See Also</span></span>
[<span data-ttu-id="6cb82-135">Opsætning af anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="6cb82-135">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="6cb82-136">Anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="6cb82-136">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="6cb82-137">Finans</span><span class="sxs-lookup"><span data-stu-id="6cb82-137">Finance</span></span>](finance.md)  
<span data-ttu-id="6cb82-138">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="6cb82-138">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="6cb82-139">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6cb82-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

