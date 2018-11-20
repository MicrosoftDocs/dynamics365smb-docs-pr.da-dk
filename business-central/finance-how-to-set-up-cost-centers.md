---
title: "Sådan opsættes omkostningssteder | Microsoft Docs"
description: "Omkostningssteder er afdelinger, der er ansvarlige for omkostninger og indtægter. Diagrammet over omkostningssteder er lig dimensionsoplysningerne for regnskabet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.translationtype: HT
ms.sourcegitcommit: 67400e424305cc705db5c1bd52a8e4de17ecc5a9
ms.openlocfilehash: 352933268e482424033d2213d2a6849c3702cb03
ms.contentlocale: da-dk
ms.lasthandoff: 11/20/2018

---
# <a name="set-up-cost-centers"></a><span data-ttu-id="cf373-104">Oprette omkostningssteder</span><span class="sxs-lookup"><span data-stu-id="cf373-104">Set Up Cost Centers</span></span>
<span data-ttu-id="cf373-105">Omkostningssteder er afdelinger, der er ansvarlige for omkostninger og indtægter.</span><span class="sxs-lookup"><span data-stu-id="cf373-105">Cost centers are departments that are responsible for costs and income.</span></span> <span data-ttu-id="cf373-106">Diagrammet over omkostningssteder er lig dimensionsoplysningerne for regnskabet.</span><span class="sxs-lookup"><span data-stu-id="cf373-106">The chart of cost centers is similar to the dimension information for the general ledger.</span></span> <span data-ttu-id="cf373-107">Du kan angive diagrammet over omkostningssteder på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="cf373-107">You can set up the chart of cost centers in the following ways:</span></span>  

-   <span data-ttu-id="cf373-108">Overfør dimensionsværdier i regnskabet til diagrammet over omkostningssteder.</span><span class="sxs-lookup"><span data-stu-id="cf373-108">Transfer dimension values in the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="cf373-109">Du kan foretage de nødvendige justeringer efter overførslen.</span><span class="sxs-lookup"><span data-stu-id="cf373-109">You can make any necessary adjustments after the transfer.</span></span>  
-   <span data-ttu-id="cf373-110">Opret et nyt diagram over omkostningssteder, der er uafhængigt af regnskabet, eller tilføj et nyt omkostningssted til et eksisterende diagram over omkostningssteder.</span><span class="sxs-lookup"><span data-stu-id="cf373-110">Create a new chart of cost center that is independent of the general ledger or add a new cost center to an existing chart of cost center.</span></span> <span data-ttu-id="cf373-111">Du skal oprette hvert omkostningssted individuelt.</span><span class="sxs-lookup"><span data-stu-id="cf373-111">You must create each cost center individually.</span></span>  

## <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a><span data-ttu-id="cf373-112">Sådan overføres dimensionsværdier i regnskabet til diagrammet over omkostningssteder.</span><span class="sxs-lookup"><span data-stu-id="cf373-112">To transfer dimension values in the general ledger to the chart of cost centers</span></span>  
1.  <span data-ttu-id="cf373-113">Angiv en dimension, der skal være omkostningsstedsdimensionen i vinduet **Opdater CA-dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="cf373-113">Set up a dimension to be the cost center dimension in the **Update Cost Acctg. Dimensions** window.</span></span> <span data-ttu-id="cf373-114">Kun værdierne fra denne dimension overføres.</span><span class="sxs-lookup"><span data-stu-id="cf373-114">Only the values from this dimension are transferred.</span></span>  
2.  <span data-ttu-id="cf373-115">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Omkostningssteder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="cf373-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Centers**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="cf373-116">På fanen **Handlinger** i gruppen **Funktioner** skal du vælge **Hent omkostningssteder fra dimensionen** for at overføre dimensionsværdier til diagrammet over omkostningssteder.</span><span class="sxs-lookup"><span data-stu-id="cf373-116">On the **Actions** tab, in the **Functions** group, choose **Get Cost Centers from Dimension** to transfer dimension values to the chart of cost centers.</span></span> <span data-ttu-id="cf373-117">Funktionen overfører de dimensionsværdier, som du definerede i trin 1.</span><span class="sxs-lookup"><span data-stu-id="cf373-117">The function transfers the dimension values that you defined in step 1.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="cf373-118">Du kan indstille feltet **Opdater omkostningsstedsdimension** til at definere en envejssynkronisering af dimensionsværdier fra regnskabet til diagrammet over omkostningssteder.</span><span class="sxs-lookup"><span data-stu-id="cf373-118">You can set up the **Align Cost Center Dimension**  field to define a one-way synchronization of dimension values from the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="cf373-119">Du kan ikke definere en synkronisering af diagrammet over omkostningssteder fra regnskabet.</span><span class="sxs-lookup"><span data-stu-id="cf373-119">You cannot define a synchronization of the chart of cost centers to dimension values from the general ledger.</span></span>  

<span data-ttu-id="cf373-120">Diagrammet over omkostningssteder indeholder alle de angivne dimensionsværdier fra regnskabet og indeholder titler og subtotaler.</span><span class="sxs-lookup"><span data-stu-id="cf373-120">The chart of cost centers now contains all specified dimension values from the general ledger and includes titles and subtotals.</span></span>  

## <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-window"></a><span data-ttu-id="cf373-121">Sådan oprettes nye omkostningssteder i vinduet Diagram over omkostningssteder</span><span class="sxs-lookup"><span data-stu-id="cf373-121">To create new cost centers in the Chart of Cost Centers window</span></span>  
<span data-ttu-id="cf373-122">Du kan oprette og vedligeholde omkostningssteder enten på kortet **Omkostningsstedskort** eller i vinduet **Diagram over omkostningssteder**.</span><span class="sxs-lookup"><span data-stu-id="cf373-122">You can set up and maintain cost centers in either the **Cost Center Card** card or in the **Chart of Cost Centers** window.</span></span> <span data-ttu-id="cf373-123">I denne procedure opretter du omkostningssteder i vinduet **Diagram over omkostningssteder**.</span><span class="sxs-lookup"><span data-stu-id="cf373-123">In this procedure, you set up cost centers in the **Chart of Cost Centers** window.</span></span>  

1. <span data-ttu-id="cf373-124">Åbn vinduet **Diagram over omkostningssteder** i redigeringstilstand.</span><span class="sxs-lookup"><span data-stu-id="cf373-124">Open the **Chart of Cost Centers** window in edit mode.</span></span>  
2. <span data-ttu-id="cf373-125">I feltet **Kode** angives omkostningsstedets kode.</span><span class="sxs-lookup"><span data-stu-id="cf373-125">In the **Code** field, enter the cost center code.</span></span> <span data-ttu-id="cf373-126">Alle omkostningssteder skal have en kode.</span><span class="sxs-lookup"><span data-stu-id="cf373-126">All cost centers must have a code.</span></span>  
3. <span data-ttu-id="cf373-127">I feltet **Navn** angives omkostningsstedets navn.</span><span class="sxs-lookup"><span data-stu-id="cf373-127">In the **Name** field, enter the cost center name.</span></span>  
4. <span data-ttu-id="cf373-128">Vælg rullepilen i feltet **Linjetype** for at angive formålet med omkostningsstedet.</span><span class="sxs-lookup"><span data-stu-id="cf373-128">Choose the drop-down arrow in the **Line Type** field to specify the purpose of the cost center.</span></span>  

    - <span data-ttu-id="cf373-129">For omkostningssteder af typen **I alt** skal du udfylde feltet **Sammentælling**.</span><span class="sxs-lookup"><span data-stu-id="cf373-129">For cost centers of the **Total** type, you must fill in the **Totaling** field.</span></span> <span data-ttu-id="cf373-130">Brug operatoren **eller**, som er en lodret linje (**&#124;**) til at angive områder for omkostningssteder.</span><span class="sxs-lookup"><span data-stu-id="cf373-130">Use the **or** operator, which is a vertical line (**&#124;**) to set ranges of cost centers.</span></span>  
    - <span data-ttu-id="cf373-131">For omkostningssteder af typen **Til-sum**udfyldes dette felt automatisk, når du bruger indrykningsfunktion.</span><span class="sxs-lookup"><span data-stu-id="cf373-131">For cost centers of the **End-Total** line type, this field is filled in automatically when you use the indent function.</span></span>  
5.  <span data-ttu-id="cf373-132">Udfyld felterne **Sorteringsrækkefølge** og **Omkostningsundertype**.</span><span class="sxs-lookup"><span data-stu-id="cf373-132">Fill in the **Sorting Order** and **Cost Subtype** fields.</span></span>  
6.  <span data-ttu-id="cf373-133">Vælg den næste tomme linje for at oprette et nyt omkostningssteder, og gentag derefter trin 2 til 5.</span><span class="sxs-lookup"><span data-stu-id="cf373-133">Choose the next empty line to create a new cost center, and then repeat steps 2 through 5.</span></span>  
7.  <span data-ttu-id="cf373-134">Når du har oprettet alle omkostningssteder, kan du vælge handlingen **Indryk omkostningssteder**.</span><span class="sxs-lookup"><span data-stu-id="cf373-134">After you have set up all the cost centers, choose the **Indent Cost Centers** action.</span></span> <span data-ttu-id="cf373-135">Vælg knappen **Ja**.</span><span class="sxs-lookup"><span data-stu-id="cf373-135">Choose the **Yes** button.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="cf373-136">Hvis du har angivet definitioner i felterne **Sammentælling** for **Til-sum**-omkostningssteder, før du kører indrykningsfunktionen, skal du angive dem igen.</span><span class="sxs-lookup"><span data-stu-id="cf373-136">If you have entered definitions in the **Totaling** fields for **End-Total** cost centers before you run the indent function, then you must enter them again.</span></span> <span data-ttu-id="cf373-137">Funktionen overskriver værdierne i alle **Til-sum**-felter.</span><span class="sxs-lookup"><span data-stu-id="cf373-137">The function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cf373-138">Se også</span><span class="sxs-lookup"><span data-stu-id="cf373-138">See Also</span></span>  
[<span data-ttu-id="cf373-139">Regnskab for omkostninger</span><span class="sxs-lookup"><span data-stu-id="cf373-139">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="cf373-140">[Konfigurere omkostningsregnskab](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="cf373-140">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="cf373-141">[Terminologi i omkostningsregnskab](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="cf373-141">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="cf373-142">Om omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="cf373-142">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="cf373-143">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cf373-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

