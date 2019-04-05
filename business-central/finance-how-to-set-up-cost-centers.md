---
title: Sådan opsættes omkostningssteder | Microsoft Docs
description: Omkostningssteder er afdelinger, der er ansvarlige for omkostninger og indtægter. Diagrammet over omkostningssteder er lig dimensionsoplysningerne for regnskabet.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 252ebf514635ada8e07bfb1e950d0cff156d0bfc
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792182"
---
# <a name="set-up-cost-centers"></a><span data-ttu-id="6c396-104">Oprette omkostningssteder</span><span class="sxs-lookup"><span data-stu-id="6c396-104">Set Up Cost Centers</span></span>
<span data-ttu-id="6c396-105">Omkostningssteder er afdelinger, der er ansvarlige for omkostninger og indtægter.</span><span class="sxs-lookup"><span data-stu-id="6c396-105">Cost centers are departments that are responsible for costs and income.</span></span> <span data-ttu-id="6c396-106">Diagrammet over omkostningssteder er lig dimensionsoplysningerne for regnskabet.</span><span class="sxs-lookup"><span data-stu-id="6c396-106">The chart of cost centers is similar to the dimension information for the general ledger.</span></span> <span data-ttu-id="6c396-107">Du kan angive diagrammet over omkostningssteder på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="6c396-107">You can set up the chart of cost centers in the following ways:</span></span>  

-   <span data-ttu-id="6c396-108">Overfør dimensionsværdier i regnskabet til diagrammet over omkostningssteder.</span><span class="sxs-lookup"><span data-stu-id="6c396-108">Transfer dimension values in the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="6c396-109">Du kan foretage de nødvendige justeringer efter overførslen.</span><span class="sxs-lookup"><span data-stu-id="6c396-109">You can make any necessary adjustments after the transfer.</span></span>  
-   <span data-ttu-id="6c396-110">Opret et nyt diagram over omkostningssteder, der er uafhængigt af regnskabet, eller tilføj et nyt omkostningssted til et eksisterende diagram over omkostningssteder.</span><span class="sxs-lookup"><span data-stu-id="6c396-110">Create a new chart of cost center that is independent of the general ledger or add a new cost center to an existing chart of cost center.</span></span> <span data-ttu-id="6c396-111">Du skal oprette hvert omkostningssted individuelt.</span><span class="sxs-lookup"><span data-stu-id="6c396-111">You must create each cost center individually.</span></span>  

## <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a><span data-ttu-id="6c396-112">Sådan overføres dimensionsværdier i regnskabet til diagrammet over omkostningssteder.</span><span class="sxs-lookup"><span data-stu-id="6c396-112">To transfer dimension values in the general ledger to the chart of cost centers</span></span>  
1.  <span data-ttu-id="6c396-113">Angiv en dimension, der skal være omkostningsstedsdimensionen på siden **Opdater CA-dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="6c396-113">Set up a dimension to be the cost center dimension on the **Update Cost Acctg. Dimensions** page.</span></span> <span data-ttu-id="6c396-114">Kun værdierne fra denne dimension overføres.</span><span class="sxs-lookup"><span data-stu-id="6c396-114">Only the values from this dimension are transferred.</span></span>  
2.  <span data-ttu-id="6c396-115">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Omkostningssteder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="6c396-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Centers**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="6c396-116">På fanen **Handlinger** i gruppen **Funktioner** skal du vælge **Hent omkostningssteder fra dimensionen** for at overføre dimensionsværdier til diagrammet over omkostningssteder.</span><span class="sxs-lookup"><span data-stu-id="6c396-116">On the **Actions** tab, in the **Functions** group, choose **Get Cost Centers from Dimension** to transfer dimension values to the chart of cost centers.</span></span> <span data-ttu-id="6c396-117">Funktionen overfører de dimensionsværdier, som du definerede i trin 1.</span><span class="sxs-lookup"><span data-stu-id="6c396-117">The function transfers the dimension values that you defined in step 1.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="6c396-118">Du kan indstille feltet **Opdater omkostningsstedsdimension** til at definere en envejssynkronisering af dimensionsværdier fra regnskabet til diagrammet over omkostningssteder.</span><span class="sxs-lookup"><span data-stu-id="6c396-118">You can set up the **Align Cost Center Dimension**  field to define a one-way synchronization of dimension values from the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="6c396-119">Du kan ikke definere en synkronisering af diagrammet over omkostningssteder fra regnskabet.</span><span class="sxs-lookup"><span data-stu-id="6c396-119">You cannot define a synchronization of the chart of cost centers to dimension values from the general ledger.</span></span>  

<span data-ttu-id="6c396-120">Diagrammet over omkostningssteder indeholder alle de angivne dimensionsværdier fra regnskabet og indeholder titler og subtotaler.</span><span class="sxs-lookup"><span data-stu-id="6c396-120">The chart of cost centers now contains all specified dimension values from the general ledger and includes titles and subtotals.</span></span>  

## <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-page"></a><span data-ttu-id="6c396-121">Sådan oprettes nye omkostningssteder på siden Diagram over omkostningssteder</span><span class="sxs-lookup"><span data-stu-id="6c396-121">To create new cost centers in the Chart of Cost Centers page</span></span>  
<span data-ttu-id="6c396-122">Du kan oprette og vedligeholde omkostningssteder enten på kortet **Omkostningsstedskort** eller på siden **Diagram over omkostningssteder**.</span><span class="sxs-lookup"><span data-stu-id="6c396-122">You can set up and maintain cost centers in either the **Cost Center Card** card or on the **Chart of Cost Centers** page.</span></span> <span data-ttu-id="6c396-123">I denne procedure opretter du omkostningssteder på siden **Diagram over omkostningssteder**.</span><span class="sxs-lookup"><span data-stu-id="6c396-123">In this procedure, you set up cost centers on the **Chart of Cost Centers** page.</span></span>  

1. <span data-ttu-id="6c396-124">Åbn siden **Diagram over omkostningssteder** i redigeringstilstand.</span><span class="sxs-lookup"><span data-stu-id="6c396-124">Open the **Chart of Cost Centers** page in edit mode.</span></span>  
2. <span data-ttu-id="6c396-125">I feltet **Kode** angives omkostningsstedets kode.</span><span class="sxs-lookup"><span data-stu-id="6c396-125">In the **Code** field, enter the cost center code.</span></span> <span data-ttu-id="6c396-126">Alle omkostningssteder skal have en kode.</span><span class="sxs-lookup"><span data-stu-id="6c396-126">All cost centers must have a code.</span></span>  
3. <span data-ttu-id="6c396-127">I feltet **Navn** angives omkostningsstedets navn.</span><span class="sxs-lookup"><span data-stu-id="6c396-127">In the **Name** field, enter the cost center name.</span></span>  
4. <span data-ttu-id="6c396-128">Vælg rullepilen i feltet **Linjetype** for at angive formålet med omkostningsstedet.</span><span class="sxs-lookup"><span data-stu-id="6c396-128">Choose the drop-down arrow in the **Line Type** field to specify the purpose of the cost center.</span></span>  

    - <span data-ttu-id="6c396-129">For omkostningssteder af typen **I alt** skal du udfylde feltet **Sammentælling**.</span><span class="sxs-lookup"><span data-stu-id="6c396-129">For cost centers of the **Total** type, you must fill in the **Totaling** field.</span></span> <span data-ttu-id="6c396-130">Brug operatoren **eller**, som er en lodret linje (**&#124;**) til at angive områder for omkostningssteder.</span><span class="sxs-lookup"><span data-stu-id="6c396-130">Use the **or** operator, which is a vertical line (**&#124;**) to set ranges of cost centers.</span></span>  
    - <span data-ttu-id="6c396-131">For omkostningssteder af typen **Til-sum** udfyldes dette felt automatisk, når du bruger indrykningsfunktion.</span><span class="sxs-lookup"><span data-stu-id="6c396-131">For cost centers of the **End-Total** line type, this field is filled in automatically when you use the indent function.</span></span>  
5.  <span data-ttu-id="6c396-132">Udfyld felterne **Sorteringsrækkefølge** og **Omkostningsundertype**.</span><span class="sxs-lookup"><span data-stu-id="6c396-132">Fill in the **Sorting Order** and **Cost Subtype** fields.</span></span>  
6.  <span data-ttu-id="6c396-133">Vælg den næste tomme linje for at oprette et nyt omkostningssteder, og gentag derefter trin 2 til 5.</span><span class="sxs-lookup"><span data-stu-id="6c396-133">Choose the next empty line to create a new cost center, and then repeat steps 2 through 5.</span></span>  
7.  <span data-ttu-id="6c396-134">Når du har oprettet alle omkostningssteder, kan du vælge handlingen **Indryk omkostningssteder**.</span><span class="sxs-lookup"><span data-stu-id="6c396-134">After you have set up all the cost centers, choose the **Indent Cost Centers** action.</span></span> <span data-ttu-id="6c396-135">Vælg knappen **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6c396-135">Choose the **Yes** button.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="6c396-136">Hvis du har angivet definitioner i felterne **Sammentælling** for **Til-sum**-omkostningssteder, før du kører indrykningsfunktionen, skal du angive dem igen.</span><span class="sxs-lookup"><span data-stu-id="6c396-136">If you have entered definitions in the **Totaling** fields for **End-Total** cost centers before you run the indent function, then you must enter them again.</span></span> <span data-ttu-id="6c396-137">Funktionen overskriver værdierne i alle **Til-sum**-felter.</span><span class="sxs-lookup"><span data-stu-id="6c396-137">The function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6c396-138">Se også</span><span class="sxs-lookup"><span data-stu-id="6c396-138">See Also</span></span>  
[<span data-ttu-id="6c396-139">Regnskab for omkostninger</span><span class="sxs-lookup"><span data-stu-id="6c396-139">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="6c396-140">[Konfigurere omkostningsregnskab](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="6c396-140">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="6c396-141">[Terminologi i omkostningsregnskab](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="6c396-141">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="6c396-142">Om omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="6c396-142">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="6c396-143">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6c396-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
