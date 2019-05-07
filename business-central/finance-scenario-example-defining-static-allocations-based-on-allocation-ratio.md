---
title: Definition af statisk allokeringer baseret på fordelingsforholdet | Microsoft Docs
description: 'Metoden statisk allokering er baseret på en endelig værdi, for eksempel anvendt antal kvadratmeter eller et etableret fordelingsforhold såsom 5: 2: 4.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: bd17923913355f883d14beb24136e97a839116e3
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "914834"
---
# <a name="scenario-example-defining-static-allocations-based-on-allocation-ratio"></a><span data-ttu-id="d8971-103">Scenarieeksempel: Definition af statisk allokeringer baseret på fordelingsforholdet</span><span class="sxs-lookup"><span data-stu-id="d8971-103">Scenario Example: Defining Static Allocations Based on Allocation Ratio</span></span>
<span data-ttu-id="d8971-104">Metoden statisk allokering er baseret på en endelig værdi, for eksempel anvendt antal kvadratmeter eller et etableret fordelingsforhold såsom 5: 2: 4.</span><span class="sxs-lookup"><span data-stu-id="d8971-104">Static allocation method is based on a definite value, such as square meters used, or an established allocation ratio such as 5:2:4.</span></span>  

<span data-ttu-id="d8971-105">Dette emne beskriver, hvordan du definerer tre nye fordelingsmålsomkostningsobjekter til fordelingskilden PROD-omkostningssted ved hjælp af det etablerede fordelingsforhold 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="d8971-105">This topic describes how to define three new allocation target cost objects for the allocation source PROD cost center using the established allocation ratio 5:2:4.</span></span> <span data-ttu-id="d8971-106">De tre målomkostningsobjekter er ACCESSO, PAINT og FITTINGS.</span><span class="sxs-lookup"><span data-stu-id="d8971-106">The three target cost objects are ACCESSO, PAINT, and FITTINGS.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="d8971-107">I eksemplet bruges demonstrationsdataene i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d8971-107">The example uses the demo data in the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a><span data-ttu-id="d8971-108">Sådan defineres fordelingskilden PROD-omkostningssted på oversigtspanelet Generelt</span><span class="sxs-lookup"><span data-stu-id="d8971-108">To define the allocation source PROD cost center on the General FastTab</span></span>  

1.  <span data-ttu-id="d8971-109">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Omkostningsfordeling**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d8971-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cost Allocation**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d8971-110">På siden **Omkostningsfordeling** skal du vælge handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d8971-110">On the **Cost Allocation** page, choose the **New** action.</span></span>  
3.  <span data-ttu-id="d8971-111">I feltet **Id** skal du trykke på Enter eller indtaste et id.</span><span class="sxs-lookup"><span data-stu-id="d8971-111">In the **ID** field, press Enter or enter an ID.</span></span>  
4.  <span data-ttu-id="d8971-112">Angiv **1** i feltet **Niveau**.</span><span class="sxs-lookup"><span data-stu-id="d8971-112">In the **Level** field, enter **1**.</span></span>  
5.  <span data-ttu-id="d8971-113">I felterne **Gyldig fra** og **Gyldig til** skal du angive relevante datoer.</span><span class="sxs-lookup"><span data-stu-id="d8971-113">In the **Valid From** and **Valid To** fields, enter appropriate dates.</span></span>  
6.  <span data-ttu-id="d8971-114">I feltet **Omkostningsstedskode** skal du angive **PROD**.</span><span class="sxs-lookup"><span data-stu-id="d8971-114">In the **Cost Center Code** field, enter **PROD**.</span></span>  
7.  <span data-ttu-id="d8971-115">Angiv omkostningstypen **9903** i feltet **Kredit til omkostningstype**.</span><span class="sxs-lookup"><span data-stu-id="d8971-115">In the **Credit to Cost Type** field, enter the cost type **9903**.</span></span>  

## <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a><span data-ttu-id="d8971-116">Sådan angives fordelingsmålsomkostningsobjekter på oversigtspanelet Linjer</span><span class="sxs-lookup"><span data-stu-id="d8971-116">To define the allocation target cost objects on the Lines FastTab</span></span>  

1.  <span data-ttu-id="d8971-117">Angiv **9903** i feltet **Målomkostningstype** på den første linje.</span><span class="sxs-lookup"><span data-stu-id="d8971-117">On the first line, in the **Target Cost Type** field, enter **9903**.</span></span>  
2.  <span data-ttu-id="d8971-118">Vælg **TILBEHØR** i feltet **Målomkostningstype** på den første linje.</span><span class="sxs-lookup"><span data-stu-id="d8971-118">On the first line, in the **Target Cost Object** field, select **ACCESSO**.</span></span>  
3.  <span data-ttu-id="d8971-119">På den første linje i feltet **Fordelingsmåltype** skal du vælge **Alle omkostninger** for at definere, hvordan alle påløbne omkostninger allokeres.</span><span class="sxs-lookup"><span data-stu-id="d8971-119">On the first line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
4.  <span data-ttu-id="d8971-120">På den første linje i feltet **Basis** skal du vælge **Statisk** for at bruge den statiske allokeringsmetode.</span><span class="sxs-lookup"><span data-stu-id="d8971-120">On the first line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
5.  <span data-ttu-id="d8971-121">På den første linje i feltet **Fordeling** skal du angive fordelingsforholdet **5**.</span><span class="sxs-lookup"><span data-stu-id="d8971-121">On the first line, in the **Share** field, enter the allocation ratio **5**.</span></span>  
6.  <span data-ttu-id="d8971-122">Angiv **9903** i feltet **Målomkostningstype** på den anden linje.</span><span class="sxs-lookup"><span data-stu-id="d8971-122">On the second line, in the **Target Cost Type** field, enter **9903**.</span></span>  
7.  <span data-ttu-id="d8971-123">Vælg **MALING** i feltet **Målomkostningsemne** på den anden linje.</span><span class="sxs-lookup"><span data-stu-id="d8971-123">On the second line, in the **Target Cost Object** field, select **PAINT**.</span></span>  
8.  <span data-ttu-id="d8971-124">På den anden linje i feltet **Fordelingsmåltype** skal du vælge **Alle omkostninger** for at definere, hvordan alle påløbne omkostninger allokeres.</span><span class="sxs-lookup"><span data-stu-id="d8971-124">On the second line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
9. <span data-ttu-id="d8971-125">På den anden linje i feltet **Basis** skal du vælge **Statisk** for at bruge den statiske allokeringsmetode.</span><span class="sxs-lookup"><span data-stu-id="d8971-125">On the second line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
10. <span data-ttu-id="d8971-126">På den anden linje i feltet **Fordeling** skal du angive fordelingsforholdet **2**.</span><span class="sxs-lookup"><span data-stu-id="d8971-126">On the second line, in the **Share** field, enter the allocation ratio **2**.</span></span>  
11. <span data-ttu-id="d8971-127">Angiv **9903** i feltet **Målomkostningstype** på den tredje linje.</span><span class="sxs-lookup"><span data-stu-id="d8971-127">On the third line, in the **Target Cost Type** field, enter **9903**.</span></span>  
12. <span data-ttu-id="d8971-128">Vælg **BESLAG** i feltet **Målomkostningsemne** på den første linje.</span><span class="sxs-lookup"><span data-stu-id="d8971-128">On the third line, in the **Target Cost Object** field, select **FITTINGS**.</span></span>  
13. <span data-ttu-id="d8971-129">På den tredje linje i feltet **Fordelingsmåltype** skal du vælge **Alle omkostninger** for at definere, hvordan alle påløbne omkostninger allokeres.</span><span class="sxs-lookup"><span data-stu-id="d8971-129">On the third line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
14. <span data-ttu-id="d8971-130">På den tredje linje i feltet **Basis** skal du vælge **Statisk** for at bruge den statiske allokeringsmetode.</span><span class="sxs-lookup"><span data-stu-id="d8971-130">On the third line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
15. <span data-ttu-id="d8971-131">På den tredje linje i feltet **Fordeling** skal du angive fordelingsforholdet **4**.</span><span class="sxs-lookup"><span data-stu-id="d8971-131">On the third line, in the **Share** field, enter the allocation ratio **4**.</span></span>  

> [!IMPORTANT]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="d8971-132">beregner automatisk feltet **Procent** ved hjælp af en procentsats , der er afhængig af alle tre fordelingsforhold, der er angivet i feltet **Fordeling** for alle tre linjer.</span><span class="sxs-lookup"><span data-stu-id="d8971-132">automatically calculates the **Percent** field using a percentage rate that is dependent on all three allocation ratios that are entered in the **Share** field for all three lines.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d8971-133">Se også</span><span class="sxs-lookup"><span data-stu-id="d8971-133">See Also</span></span>  
[<span data-ttu-id="d8971-134">Definere og allokere omkostninger</span><span class="sxs-lookup"><span data-stu-id="d8971-134">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)   
