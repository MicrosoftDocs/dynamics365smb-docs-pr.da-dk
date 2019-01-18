---
title: "Sådan opsættes omkostningsemner | Microsoft Docs"
description: "Få at vide, hvordan du opsætter omkostningsemner, der svarer til dimensioner i finansregnskabet."
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
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 616fcbe937e556c17e8beb79f68bc961ea8bbe18
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="set-up-cost-objects"></a><span data-ttu-id="8a3aa-103">Oprette omkostningsemner</span><span class="sxs-lookup"><span data-stu-id="8a3aa-103">Set Up Cost Objects</span></span>
<span data-ttu-id="8a3aa-104">Omkostningsobjekter er en virksomheds projekter, produkter eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-104">Cost objects are projects, products, or services of a company.</span></span> <span data-ttu-id="8a3aa-105">Diagrammet over omkostningsobjekter er lig dimensionsoplysningerne for regnskabet.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-105">The chart of cost objects is similar to the dimension information for the general ledger.</span></span> <span data-ttu-id="8a3aa-106">Du kan angive diagrammet over omkostningsobjekter på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="8a3aa-106">You can set up the chart of cost objects in the following ways:</span></span>  

* <span data-ttu-id="8a3aa-107">Overfør dimensionsværdier i regnskabet til diagrammet over omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-107">Transfer dimension values in the general ledger to the chart of cost objects.</span></span> <span data-ttu-id="8a3aa-108">Du kan foretage de nødvendige justeringer efter overførslen.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-108">You can make any necessary adjustments after the transfer.</span></span>  
* <span data-ttu-id="8a3aa-109">Opret et nyt diagram over omkostningsobjekter, der er uafhængigt af regnskabet, eller tilføje et nyt omkostningsobjekt til et eksisterende diagram over omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-109">Create a new chart of cost object that is independent of the general ledger or add a new cost object to an existing chart of cost objects.</span></span> <span data-ttu-id="8a3aa-110">Du skal oprette hvert omkostningsobjekt individuelt.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-110">You must create each cost object individually.</span></span>  

## <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a><span data-ttu-id="8a3aa-111">Sådan overføres dimensionsværdier fra regnskabet til diagrammet over omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-111">To transfer dimension values from the general ledger to the chart of cost objects</span></span>  
1.  <span data-ttu-id="8a3aa-112">Angiv en dimension, der skal være omkostningsobjektdimensionen på siden **Opdater CA-dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-112">Set a dimension to be the cost object dimension on the **Update CA Dimensions** page.</span></span> <span data-ttu-id="8a3aa-113">Kun værdierne fra denne dimension overføres.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-113">Only the values from this dimension are transferred.</span></span>  
2.  <span data-ttu-id="8a3aa-114">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Omkostningsemner**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Objects**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="8a3aa-115">Vælg handlingen **Hent omkostningsemner fra dimensionen** for at overføre dimensionsværdier til diagrammet over omkostningsemner.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-115">Choose the **Get Cost Objects from Dimension** action to transfer dimension values to the chart of cost objects.</span></span> <span data-ttu-id="8a3aa-116">Funktionen overfører de dimensionsværdier, som du definerede i trin 1.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-116">The function transfers the dimension values that you defined in step 1.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="8a3aa-117">Du kan indstille feltet **Opdater omkostningsemnedimension** til at definere en envejssynkronisering af dimensionsværdier fra regnskabet til diagrammet over omkostningsemner.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-117">You can set up the **Align Cost Object Dimension**  field to define a one-way synchronization of dimension values from the general ledger to the chart of cost objects.</span></span> <span data-ttu-id="8a3aa-118">Du kan ikke definere en synkronisering af diagrammet over omkostningsobjekter fra regnskabet.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-118">You cannot define a synchronization of the chart of cost objects to dimension values from the general ledger.</span></span>  

<span data-ttu-id="8a3aa-119">Diagrammet over omkostningsobjekter indeholder alle de angivne dimensionsværdier fra regnskabet og indeholder titler og subtotaler.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-119">The chart of cost objects now contains all specified dimension values from the general ledger and includes titles and subtotals.</span></span>  

## <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-page"></a><span data-ttu-id="8a3aa-120">Sådan oprettes nye omkostningsemner på siden Diagram over omkostningsemner</span><span class="sxs-lookup"><span data-stu-id="8a3aa-120">To create new cost objects in the Chart of Cost Objects page</span></span>  
<span data-ttu-id="8a3aa-121">Du kan oprette og vedligeholde omkostningsemner enten på **Omkostningsemnekortet** eller på siden **Diagram over omkostningsemner**.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-121">You can set up and maintain cost objects in either the **Cost Object Card** card or on the **Chart of Cost Objects** page.</span></span> <span data-ttu-id="8a3aa-122">I denne procedure opretter du omkostningsobjekter på siden **Diagram over omkostningsemner**.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-122">In this procedure, you set up cost objects on the **Chart of Cost Objects** page.</span></span>  

1.  <span data-ttu-id="8a3aa-123">Åbn siden **Diagram over omkostningsemner** i redigeringstilstand.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-123">Open the **Chart of Cost Objects** page in edit mode.</span></span>  
2.  <span data-ttu-id="8a3aa-124">I feltet **Kode** angives omkostningsemnets kode.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-124">In the **Code** field, enter the cost object code.</span></span> <span data-ttu-id="8a3aa-125">Alle omkostningsobjekter skal have en kode.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-125">All cost objects must have a code.</span></span>  
3.  <span data-ttu-id="8a3aa-126">I feltet **Navn** angives omkostningsemnets navn.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-126">In the **Name** field, enter the cost object name.</span></span>  
4.  <span data-ttu-id="8a3aa-127">Vælg rullepilen i feltet **Linjetype** for at angive formålet med omkostningsemnet.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-127">Choose the drop-down arrow in the **Line Type** field to specify the purpose of the cost object.</span></span>  

    * <span data-ttu-id="8a3aa-128">For omkostningsemner af linjetypen **I alt** skal du udfylde feltet **I alt fra/til**.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-128">For cost objects of the **Total** line type, fill in the **Total From/To** field.</span></span> <span data-ttu-id="8a3aa-129">Brug operatoren **eller**, som er en lodret linje (**&#124;**), til at angive områder for omkostningsemner.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-129">Use the **or** operator, which is a vertical line (**&#124;**), to set ranges of cost objects.</span></span>  
    * <span data-ttu-id="8a3aa-130">For omkostningsobjekter af typen **Til-sum** udfyldes dette felt automatisk, når du bruger indrykningsfunktion.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-130">For cost objects of the **End-Total** line type, this field is filled in automatically when you use  the indent function.</span></span>  
5.  <span data-ttu-id="8a3aa-131">Udfyld feltet **Sorteringsrækkefølge**.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-131">Fill in the **Sorting Order** field.</span></span>  
6.  <span data-ttu-id="8a3aa-132">Vælger den næste tomme linje for at oprette et nyt omkostningsobjekt, og gentag derefter trin 2 til 5.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-132">Chose the next empty line to create a new cost object, and then repeat steps 2 through 5.</span></span>  
7.  <span data-ttu-id="8a3aa-133">Når du har oprettet alle omkostningsemner, kan du vælge handlingen **Indryk omkostningsemner**.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-133">After you have set up all the cost objects, choose the **Indent Cost Objects** action.</span></span> <span data-ttu-id="8a3aa-134">Vælg knappen **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-134">Choose the **Yes** button.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="8a3aa-135">Hvis du har angivet definitioner i felterne **I alt fra/til** for **Til-sum**-omkostningsemner, før du kører indrykningsfunktionen, skal du angive dem igen.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-135">If you have entered definitions in the **Total From/To** fields for **End-Total** cost objects before you run the indent function, then you must enter them again.</span></span> <span data-ttu-id="8a3aa-136">Funktionen overskriver værdierne i alle **Til-sum**-felter.</span><span class="sxs-lookup"><span data-stu-id="8a3aa-136">The function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8a3aa-137">Se også</span><span class="sxs-lookup"><span data-stu-id="8a3aa-137">See Also</span></span>  
[<span data-ttu-id="8a3aa-138">Regnskab for omkostninger</span><span class="sxs-lookup"><span data-stu-id="8a3aa-138">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="8a3aa-139">[Definition af omkostningssteder og omkostningsobjekter for kontoplanen](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="8a3aa-139">[Defining Cost Centers and Cost Objects for Chart of Accounts](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span></span>  
<span data-ttu-id="8a3aa-140">[Saldi mellem omkostningstype, omkostningssted og omkostningsobjekt](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span><span class="sxs-lookup"><span data-stu-id="8a3aa-140">[Balances Between Cost Type, Cost Center, and Cost Object](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span></span>  
<span data-ttu-id="8a3aa-141">[Konfigurere omkostningsregnskab](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="8a3aa-141">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="8a3aa-142">[Terminologi i omkostningsregnskab](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="8a3aa-142">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="8a3aa-143">Om omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="8a3aa-143">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="8a3aa-144">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8a3aa-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

