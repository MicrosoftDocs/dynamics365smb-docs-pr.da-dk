---
title: "Definere anlægsvedligeholdelse | Microsoft Docs"
description: "For at kunne administrere reparation og service af anlæg skal du angive generelle vedligeholdelsesoplysninger, koder for typen af arbejde og en bogføringskonto for omkostninger."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: cdf1183fb5383311dc34d8c2c619a1eddf7e8851
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-fixed-asset-maintenance"></a><span data-ttu-id="16892-103">Fremgangsmåde: Konfigurere reparation af anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="16892-103">How to: Set Up Fixed Asset Maintenance</span></span>
<span data-ttu-id="16892-104">For at administrere vedligeholdelse af anlæg, skal du først angive nogle generelle reparationsoplysninger, en bogføringskonto for reparationsomkostninger og reparationskoder for forskellige typer arbejde, f.eks rutineeftersyn eller reparation.</span><span class="sxs-lookup"><span data-stu-id="16892-104">To manage fixed asset maintenance, you must first set up some general maintenance information, a posting account for maintenance costs, and maintenance codes for types of work, such as Routine Service or Repair.</span></span>

## <a name="to-set-up-general-maintenance-information"></a><span data-ttu-id="16892-105">Sådan angives generelle reparationsoplysninger</span><span class="sxs-lookup"><span data-stu-id="16892-105">To set up general maintenance information</span></span>
<span data-ttu-id="16892-106">Hvis du definerer felterne til reparation, kan du bogføre reparationsudgifter fra anlægskladden.</span><span class="sxs-lookup"><span data-stu-id="16892-106">If you set up the fields for maintenance, you can post maintenance expenses from the fixed asset journal.</span></span>

1. <span data-ttu-id="16892-107">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlægsaktiver**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="16892-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="16892-108">Vælg det anlægsaktiv, du vil definere forsikringsdækning for, og vælg derefter handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="16892-108">Select the fixed asset that you to define insurance coverage for, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="16892-109">Udfyld felterne efter behov i oversigtspanelet **Reparation**.</span><span class="sxs-lookup"><span data-stu-id="16892-109">On the **Maintenance** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a><span data-ttu-id="16892-110">Sådan defineres reparationskoder</span><span class="sxs-lookup"><span data-stu-id="16892-110">To set up maintenance codes</span></span>
<span data-ttu-id="16892-111">Når du bogfører reparationsudgifter fra en kassekladde, skal du udfylde feltet **Reparationskode** for at registrere, hvilken slags reparation der er blevet udført, f.eks. rutineeftersyn eller reparation.</span><span class="sxs-lookup"><span data-stu-id="16892-111">When you post maintenance costs from a general journal, you fill in the **Maintenance Code** field to record what kind of maintenance has been performed, such as routine service or repair.</span></span>

1. <span data-ttu-id="16892-112">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Reparation**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="16892-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Maintenance**, and then choose the related link.</span></span>
2. <span data-ttu-id="16892-113">I feltet **Reparation** skal du oprette koder for de forskellige typer reparationsarbejde.</span><span class="sxs-lookup"><span data-stu-id="16892-113">In the **Maintenance** window, set up codes for different types of maintenance work.</span></span>

## <a name="to-set-up-maintenance-expense-accounts"></a><span data-ttu-id="16892-114">Sådan defineres reparationskonti</span><span class="sxs-lookup"><span data-stu-id="16892-114">To set up maintenance expense accounts</span></span>
<span data-ttu-id="16892-115">Hvis du vil bogføre reparationsudgifter, skal du først angive et kontonummer i vinduet **Anlægsbogføringsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="16892-115">To post maintenance costs, you must first enter an account number in the **FA Posting Groups** window.</span></span>

1. <span data-ttu-id="16892-116">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlægsbogføringsgrupper**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="16892-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA Posting Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="16892-117">Udfyld feltet **Reparationskonto** for hver enkelt bogføringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="16892-117">Fill in the **Maintenance Expense Account** field for each posting group.</span></span>

> [!NOTE]  
>   <span data-ttu-id="16892-118">Hvis du angive, at reparationsomkostningerne skal allokeres til afdelinger eller projekter, skal du definere allokeringsnøgler.</span><span class="sxs-lookup"><span data-stu-id="16892-118">To define that maintenance costs are allocated to departments or projects, set up an allocation keys.</span></span> <span data-ttu-id="16892-119">Du kan finde flere oplysninger i [Fremgangsmåde: Angive generelle funktioner for anlægsaktiver](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="16892-119">For more information, see [How to: Set Up General Fixed Assets Features](fa-how-setup-general.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="16892-120">Se også</span><span class="sxs-lookup"><span data-stu-id="16892-120">See Also</span></span>
[<span data-ttu-id="16892-121">Opsætning af anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="16892-121">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="16892-122">Anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="16892-122">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="16892-123">Finans</span><span class="sxs-lookup"><span data-stu-id="16892-123">Finance</span></span>](finance.md)  
<span data-ttu-id="16892-124">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="16892-124">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="16892-125">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="16892-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

