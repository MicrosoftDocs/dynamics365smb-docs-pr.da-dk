---
title: Scenarieeksempel - Definition af dynamiske fordelinger baseret på solgte varer | Microsoft Docs
description: I dette emne vises et eksempel på, hvordan du definerer allokeringer ved hjælp af metoden til dynamisk fordeling.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: 3103583c9781c283479c5f66e90f0e875faf46cc
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792569"
---
# <a name="scenario-example-defining-dynamic-allocations-based-on-items-sold"></a><span data-ttu-id="eeae8-103">Scenarieeksempel: Definition af dynamiske fordelinger baseret på solgte varer</span><span class="sxs-lookup"><span data-stu-id="eeae8-103">Scenario Example: Defining Dynamic Allocations Based on Items Sold</span></span>
<span data-ttu-id="eeae8-104">I dette emne vises et eksempel på, hvordan du definerer allokeringer ved hjælp af metoden til dynamisk fordeling.</span><span class="sxs-lookup"><span data-stu-id="eeae8-104">This topic shows an example of how to define allocations by using the dynamic allocation method.</span></span> <span data-ttu-id="eeae8-105">I dette eksempel skal du ændre dynamisk fordeling af omkostningerne for omkostningsstedet SALES til understøttelse af det nye omkostningsobjekt IT-UDSTYR.</span><span class="sxs-lookup"><span data-stu-id="eeae8-105">In the example, you change the dynamic allocation of the costs for the SALES cost center to support the new cost object IT EQUIPMENT.</span></span> <span data-ttu-id="eeae8-106">IT_UDSTYR-pakker har varenumre i området fra 8904-W til 8924-W.</span><span class="sxs-lookup"><span data-stu-id="eeae8-106">IT EQUIPMENT packages have item numbers in the range from 8904-W to 8924-W.</span></span> <span data-ttu-id="eeae8-107">Du bruger salgstal for det foregående år til at beregne det andelen.</span><span class="sxs-lookup"><span data-stu-id="eeae8-107">You use the previous year’s sales figures to calculate the share.</span></span> <span data-ttu-id="eeae8-108">Allokeringen bogføres til hjælpeomkostningstypen 9903.</span><span class="sxs-lookup"><span data-stu-id="eeae8-108">The allocation is posted to the helping cost type 9903.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="eeae8-109">I eksemplet bruges demonstrationsdataene i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="eeae8-109">The example uses the demo data in the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a><span data-ttu-id="eeae8-110">Sådan defineres dynamiske fordelinger baseret på varer, der er solgt i det foregående år</span><span class="sxs-lookup"><span data-stu-id="eeae8-110">To define dynamic allocations based on items sold in the previous year</span></span>  

1.  <span data-ttu-id="eeae8-111">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Omkostningsfordelinger**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="eeae8-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cost Allocations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="eeae8-112">På siden **Omkostningsfordeling** skal du vælge handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="eeae8-112">On the **Cost Allocation** page, choose the **New** action.</span></span>  
3.  <span data-ttu-id="eeae8-113">I feltet **Id** skal du trykke på Enter eller indtaste et id.</span><span class="sxs-lookup"><span data-stu-id="eeae8-113">In the **ID** field, press Enter or enter an ID.</span></span>  
4.  <span data-ttu-id="eeae8-114">Angiv **1** i feltet **Niveau**.</span><span class="sxs-lookup"><span data-stu-id="eeae8-114">In the **Level** field, enter **1**.</span></span>  
5.  <span data-ttu-id="eeae8-115">I felterne **Gyldig fra** og **Gyldig til** skal du angive relevante datoer.</span><span class="sxs-lookup"><span data-stu-id="eeae8-115">In the **Valid From** and **Valid To** fields, enter appropriate dates.</span></span>  
6.  <span data-ttu-id="eeae8-116">I feltet **Omkostningsstedskode** skal du angive **SALG**.</span><span class="sxs-lookup"><span data-stu-id="eeae8-116">In the **Cost Center Code** field, enter **SALES**.</span></span>  
7.  <span data-ttu-id="eeae8-117">Angiv omkostningstypen **9903** i feltet **Kredit til omkostningstype**.</span><span class="sxs-lookup"><span data-stu-id="eeae8-117">In the **Credit to Cost Type** field, enter the cost type **9903**.</span></span>  
8.  <span data-ttu-id="eeae8-118">Angiv omkostningstypen **9903** i feltet **Målomkostningstype**.</span><span class="sxs-lookup"><span data-stu-id="eeae8-118">In the **Target Cost Type** field, enter the cost type **9903**.</span></span>  
9. <span data-ttu-id="eeae8-119">I feltet **Målomkostningstype** skal du vælge **Ny** for at oprette et nyt omkostningsobjekt IT-UDSTYR og udfylde felter efter behov.</span><span class="sxs-lookup"><span data-stu-id="eeae8-119">In the **Target Cost Object** field, choose **New** to create a new cost object IT EQUIPMENT and fill in fields as necessary.</span></span> <span data-ttu-id="eeae8-120">Vælg **IT-UDSTYR**.</span><span class="sxs-lookup"><span data-stu-id="eeae8-120">Select **IT EQUIPMENT**.</span></span> <span data-ttu-id="eeae8-121">Lad feltet **Målomkostningssted** stå tomt.</span><span class="sxs-lookup"><span data-stu-id="eeae8-121">Leave the **Target Cost Center** field blank.</span></span>  
10. <span data-ttu-id="eeae8-122">I feltet **Fordelingsmåltype** skal du vælge **Alle omkostninger** for at definere, hvordan alle akkumulerede omkostninger allokeres.</span><span class="sxs-lookup"><span data-stu-id="eeae8-122">In the **Allocation Target Type** field, select **All Costs** to define how all accumulated costs are allocated.</span></span>  
11. <span data-ttu-id="eeae8-123">I feltet **Basis** skal du vælge fordelingsbasen **Varer solgt (beløb)**.</span><span class="sxs-lookup"><span data-stu-id="eeae8-123">In the **Base** field, select the allocation base **Items Sold (Amount)**.</span></span>  
12. <span data-ttu-id="eeae8-124">I feltet **Nummerfilter** skal du angive **8904-W..8924-W**.</span><span class="sxs-lookup"><span data-stu-id="eeae8-124">In the **No. Filter** field, enter **8904-W..8924-W**.</span></span>  
13. <span data-ttu-id="eeae8-125">I feltet **Datofilterkode** skal du angive **Sidste år**.</span><span class="sxs-lookup"><span data-stu-id="eeae8-125">In the **Date Filter Code** field, enter **Last Year**.</span></span>  
14. <span data-ttu-id="eeae8-126">Vælg handlingen **Beregn fordelingsnøgle** for at beregne det andelen.</span><span class="sxs-lookup"><span data-stu-id="eeae8-126">Choose the **Calculate Allocation Key** action to calculate the share.</span></span>  

    > [!IMPORTANT]  
    >  [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="eeae8-127">bruger salgstal fra de foregående år til at beregne andelen af 1596,50 RV med 100 procent for IT-UDSTYR-pakkerne.</span><span class="sxs-lookup"><span data-stu-id="eeae8-127">uses the previous years’ sales figures to calculate a share of 1596.50 LCY with 100 percent for the IT EQUIPMENT packages.</span></span> <span data-ttu-id="eeae8-128">Det betyder, at alle varer, der er solgt sidste år, tildeles omkostningsobjektet IT-UDSTYR.</span><span class="sxs-lookup"><span data-stu-id="eeae8-128">This means that all of the items sold last year will be allocated to the cost object IT EQUIPMENT.</span></span>  

## <a name="see-also"></a><span data-ttu-id="eeae8-129">Se også</span><span class="sxs-lookup"><span data-stu-id="eeae8-129">See Also</span></span>  
[<span data-ttu-id="eeae8-130">Definere og allokere omkostninger</span><span class="sxs-lookup"><span data-stu-id="eeae8-130">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)  
<span data-ttu-id="eeae8-131">[Terminologi i omkostningsregnskab](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="eeae8-131">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="eeae8-132">Om omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="eeae8-132">About Cost Accounting</span></span>](finance-about-cost-accounting.md)
