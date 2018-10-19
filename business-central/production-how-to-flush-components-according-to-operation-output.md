---
title: "Sådan udtrækkes komponenter i henhold til operationsafgang | Microsoft Docs"
description: "For varer, der er konfigureret med baglæns trækmetode, er standardfunktionsmåden at beregne og bogføre komponentforbrug, når du ændrer status på en frigivet produktionsordre til **Afsluttet**. Du kan finde flere oplysninger i Trækmetode."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 53f2dac9a2ea3b2ec44827e8404abfd10d03e32a
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="flush-components-according-to-operation-output"></a><span data-ttu-id="04ff0-104">Udtrække komponenter i henhold til operationsafgang</span><span class="sxs-lookup"><span data-stu-id="04ff0-104">Flush Components According to Operation Output</span></span>
<span data-ttu-id="04ff0-105">For varer, der er konfigureret med baglæns trækmetode, er standardfunktionsmåden at beregne og bogføre komponentforbrug, når du ændrer status på en frigivet produktionsordre til **Afsluttet**.</span><span class="sxs-lookup"><span data-stu-id="04ff0-105">For items that are set up with backward flushing method, the default behavior is to calculate and post component consumption when you change the status of a released production order to **Finished**.</span></span>  

<span data-ttu-id="04ff0-106">Hvis du også definerer rutebindingskoder, forekommer beregning og bogføring, når hver operation er afsluttet, og den mængde, der rent faktisk er forbrugt i handlingen, der er bogført.</span><span class="sxs-lookup"><span data-stu-id="04ff0-106">If you also define routing link codes, then calculation and posting occurs when each operation is finished, and the quantity that was actually consumed in the operation is posted.</span></span> <span data-ttu-id="04ff0-107">Du kan finde flere oplysninger i [Oprette ruter](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="04ff0-107">For more information, see [Create Routings](production-how-to-create-routings.md).</span></span>  

<span data-ttu-id="04ff0-108">Hvis f.eks. en produktionsordre om at fremstille 800 meter kræver 8 kg af en komponent, bogføres derefter, når du bogfører 200 meter som afgang, 2 kg automatisk som forbrug.</span><span class="sxs-lookup"><span data-stu-id="04ff0-108">For example, if a production order to produce 800 meters requires 8 kg of a component, then when you post 200 meters as output, 2 kg are automatically posted as consumption.</span></span>  

<span data-ttu-id="04ff0-109">Denne funktion er nyttig, af følgende årsager:</span><span class="sxs-lookup"><span data-stu-id="04ff0-109">This functionality is useful for the following reasons:</span></span>  

-   <span data-ttu-id="04ff0-110">**Lagerværdi** -værdiposterne for afgang og forbrug oprettes parallelt, efterhånden som produktionsordren skrider frem.</span><span class="sxs-lookup"><span data-stu-id="04ff0-110">**Inventory Valuation** - Value entries for output and consumption are created in parallel as the production order progresses.</span></span> <span data-ttu-id="04ff0-111">Uden rutebindingskoder vil lagerværdien forøges efterhånden som afgangen bogføres, og derefter formindsk på et senere tidspunkt, når værdien af komponentforbruget bogføres sammen med den færdige produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="04ff0-111">Without routing link codes, the inventory value will increase as output is posted and then decrease at a later point in time when the value of component consumption is posted together with the finished production order.</span></span>  
-   <span data-ttu-id="04ff0-112">**Varedisponering** - med gradvis bogføring af forbrug, vil tilgængeligheden af komponentvarer være mere opdateret, hvilket er vigtigt for at opretholde den interne balance mellem efterspørgsel og udbud.</span><span class="sxs-lookup"><span data-stu-id="04ff0-112">**Inventory Availability** - With gradual consumption posting, the availability of component items is more up-to-date, which is important to maintain the internal balance between demand and supply.</span></span> <span data-ttu-id="04ff0-113">Uden rutebindingskoder vil andre efterspørgsler efter komponenten mene, at den er tilgængelig, så længe der ventes på et forsinket bogføring af forbruget.</span><span class="sxs-lookup"><span data-stu-id="04ff0-113">Without routing link codes, other demands for the component may believe that it is available as long as it is pending a delayed consumption posting.</span></span>  
-   <span data-ttu-id="04ff0-114">**Just-in-Time** – med muligheden for at tilpasse produkter til debitorbehov, kan du minimere affald ved at sørge for, at arbejde og ændringer i systemet kun forekomme, når det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="04ff0-114">**Just-in-Time** – With the ability to customize products to customer requests, you can minimize waste by making sure that work and system changes only occur when it is necessary.</span></span>  

<span data-ttu-id="04ff0-115">Følgende procedure viser, hvordan du kombinerer Bagudtrækning og rutebindingskode, så den mængde, der udtrækkes for hver operation er proportional med den faktiske afgang af den afsluttede operation.</span><span class="sxs-lookup"><span data-stu-id="04ff0-115">The following procedure shows how to combine backward flushing and routing link codes so that the quantity that is flushed for each operation is proportional to the actual output of the finished operation.</span></span>  

## <a name="to-flush-components-according-to-operation-output"></a><span data-ttu-id="04ff0-116">Udtrække komponenter i henhold til operationsafgang</span><span class="sxs-lookup"><span data-stu-id="04ff0-116">To flush components according to operation output</span></span>  
1.  <span data-ttu-id="04ff0-117">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="04ff0-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="04ff0-118">Vælg handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="04ff0-118">Choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="04ff0-119">Vælg **Fremad** i feltet **Trækmetode** oversigtspanel under fanen **Genopfyldning**.</span><span class="sxs-lookup"><span data-stu-id="04ff0-119">On the **Replenishment** FastTab, in the **Flushing Method** field, select **Forward**.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="04ff0-120">Vælg **Pluk + Fremad**, hvis komponenten bruges på en placering, der er sat op til styret læg-på-lager og pluk.</span><span class="sxs-lookup"><span data-stu-id="04ff0-120">Select **Pick+ Forward** if the component is used in a location that is set up for directed put-away and pick.</span></span>  

4.  <span data-ttu-id="04ff0-121">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Ruter**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="04ff0-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Routings**, and then choose the related link.</span></span>  
5.  <span data-ttu-id="04ff0-122">Definer rutebindingskoder for hver operation, der bruger komponenten.</span><span class="sxs-lookup"><span data-stu-id="04ff0-122">Define routing link codes for every operation that consumes the component.</span></span> <span data-ttu-id="04ff0-123">Du kan finde flere oplysninger i [Oprette ruter](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="04ff0-123">For more information, see [Create Routings ](production-how-to-create-routings.md).</span></span>  
6.  <span data-ttu-id="04ff0-124">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Produktionsstykliste**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="04ff0-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Production BOM**, and then choose the related link.</span></span>  
7.  <span data-ttu-id="04ff0-125">Definer rutebindingskoder fra hver forekomst af komponenten til den operation, hvor den forbruges.</span><span class="sxs-lookup"><span data-stu-id="04ff0-125">Define routing link codes from each instance of the component to the operation where it is consumed.</span></span>

    > [!IMPORTANT]  
    >  <span data-ttu-id="04ff0-126">Komponenten skal have en rutebinding til den sidste operation i ruten.</span><span class="sxs-lookup"><span data-stu-id="04ff0-126">The component must have a routing link to the last operation in the routing.</span></span>  

## <a name="see-also"></a><span data-ttu-id="04ff0-127">Se også</span><span class="sxs-lookup"><span data-stu-id="04ff0-127">See Also</span></span>  
[<span data-ttu-id="04ff0-128">Oprette produktionsstyklister</span><span class="sxs-lookup"><span data-stu-id="04ff0-128">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="04ff0-129">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="04ff0-129">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="04ff0-130">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="04ff0-130">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="04ff0-131">[Planlægning](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="04ff0-131">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="04ff0-132">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="04ff0-132">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="04ff0-133">Køb</span><span class="sxs-lookup"><span data-stu-id="04ff0-133">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="04ff0-134">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="04ff0-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

