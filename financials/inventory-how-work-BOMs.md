---
title: Arbejde med styklister for at styre komponenter | Microsoft Docs
description: "Du opretter en montagestykliste for at angive de komponenter eller ressourcer, der kræves for at sammensætte den vare, som montagestyklisten repræsenterer, og du kan få vist komponenterne for et montageelement."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: e6aef60ee5b206b0ae978f72b92e6f8778290509
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-work-with-bills-of-material"></a><span data-ttu-id="c330e-103">Fremgangsmåde: Arbejde med styklister</span><span class="sxs-lookup"><span data-stu-id="c330e-103">How to: Work with Bills of Material</span></span>
> [!NOTE]  
>   <span data-ttu-id="c330e-104">Den aktuelle version af [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder kun den første del af funktionen Montagestyring.</span><span class="sxs-lookup"><span data-stu-id="c330e-104">The current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] only contains the first part of the Assembly Management feature.</span></span> <span data-ttu-id="c330e-105">Indtil videre kan du kun oprette montagestyklister og håndtere de relaterede overordnede varer som almindelige varer.</span><span class="sxs-lookup"><span data-stu-id="c330e-105">For now, you can only create assembly BOMs and then handle the related parent items as normal inventory items.</span></span> <span data-ttu-id="c330e-106">Med en senere opdatering kan du styre den egentlige montage af varer fra komponenter, enten i montage til lager- eller montage til ordre-flows, og du kan sælge komponenter som pakker.</span><span class="sxs-lookup"><span data-stu-id="c330e-106">In a future update, you can manage the actual assembly of items from components, either in assemble-to-stock or assemble-to-order flows, and you can sell components as kits.</span></span>

<span data-ttu-id="c330e-107">Du bruger styklister til at strukturere overordnede varer, du sælger som pakker, der består af den overordnede vares komponenter eller af montage til ordre- eller montage til lager-pakker.</span><span class="sxs-lookup"><span data-stu-id="c330e-107">You use bills of materials (BOMs) to structure parent items that you sell as kits consisting of the parent's components or that you assemble to order or to stock.</span></span>

<span data-ttu-id="c330e-108">I [!INCLUDE[d365fin](includes/d365fin_md.md)] kaldes en stykliste en "montagestykliste".</span><span class="sxs-lookup"><span data-stu-id="c330e-108">In [!INCLUDE[d365fin](includes/d365fin_md.md)], a bill of materials is referred to as an "assembly BOM".</span></span> <span data-ttu-id="c330e-109">Montagestyklister angiver, hvilke komponenter der er indeholdt i overordnede varer.</span><span class="sxs-lookup"><span data-stu-id="c330e-109">Assembly BOMs specify which components are contained in parent items.</span></span> <span data-ttu-id="c330e-110">En overordnet vare omtales som et "montageelement" i denne dokumentation.</span><span class="sxs-lookup"><span data-stu-id="c330e-110">In this documentation, a parent item is referred to as an "assembly item".</span></span>

<span data-ttu-id="c330e-111">Montagestyklister indeholder normalt varer, men kan også indeholde en eller flere ressourcer, der er påkrævet for at sammensætte montageelementet.</span><span class="sxs-lookup"><span data-stu-id="c330e-111">Assembly BOMs usually contain items but can also contain one or more resources that are required to put the assembly item together.</span></span>

<span data-ttu-id="c330e-112">Montagestyklister kan have flere niveauer, hvilket betyder, at en komponent på montagestyklisten selv kan være et montageelement.</span><span class="sxs-lookup"><span data-stu-id="c330e-112">Assembly BOMs can have multiple levels, which means that a component on the assembly BOM can be an assembly item itself.</span></span> <span data-ttu-id="c330e-113">I så fald skal feltet **Montagestykliste** på montagestyklistelinjen vise **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c330e-113">In that case, the **Assembly BOM** field on the assembly BOM line contains **Yes**.</span></span>

<span data-ttu-id="c330e-114">Der gælder særlige krav for elementerne på montagestyklister for så vidt angår varedisponering.</span><span class="sxs-lookup"><span data-stu-id="c330e-114">Special requirements apply to items on assembly BOMs with regards to availability.</span></span> <span data-ttu-id="c330e-115">Du kan finde flere oplysninger i afsnittet "Sådan får du vist tilgængeligheden af en vare via brugen af den i montagestyklister" i [Sådan gør du: Vise varedisponering](inventory-how-availability-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c330e-115">For more information, see the "To see the availability of an item by its use in assembly BOMs" section in [How to: View the Availability of Items](inventory-how-availability-overview.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="c330e-116">Denne funktion kræver, at oplevelsen er indstillet til **Pakke**.</span><span class="sxs-lookup"><span data-stu-id="c330e-116">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="c330e-117">Du kan finde flere oplysninger under [Tilpasse din Financials-oplevelse](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="c330e-117">For more information, see [Customizing Your Financials Experience](ui-experiences.md).</span></span>

## <a name="to-create-an-assembly-bom"></a><span data-ttu-id="c330e-118">Sådan oprettes en montagestykliste</span><span class="sxs-lookup"><span data-stu-id="c330e-118">To create an assembly BOM</span></span>
<span data-ttu-id="c330e-119">For at definere en overordnet vare, der består af andre elementer og potentielt af ressourcer, der kræves for at sammensætte den overordnede vare, skal du oprette en montagestykliste.</span><span class="sxs-lookup"><span data-stu-id="c330e-119">To define a parent item that consists of other items, and potentially of resources required to put the parent together, you must create an assembly BOM.</span></span>  

<span data-ttu-id="c330e-120">Montagestyklister oprettes ad to omgange:</span><span class="sxs-lookup"><span data-stu-id="c330e-120">There are two parts to creating an assembly BOM:</span></span>
- <span data-ttu-id="c330e-121">Oprette en ny vare</span><span class="sxs-lookup"><span data-stu-id="c330e-121">Setting up a new item</span></span>
- <span data-ttu-id="c330e-122">Angive montageelementets styklistestruktur.</span><span class="sxs-lookup"><span data-stu-id="c330e-122">Defining the BOM structure of the assembly item.</span></span>

1. <span data-ttu-id="c330e-123">Opret en ny vare.</span><span class="sxs-lookup"><span data-stu-id="c330e-123">Set up a new item.</span></span> <span data-ttu-id="c330e-124">Du kan finde flere oplysninger under [Fremgangsmåde: Registrere nye varer](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="c330e-124">For more information, see [How to: Register New Items](inventory-how-register-new-items.md).</span></span>

    <span data-ttu-id="c330e-125">Fortsæt med at angive komponenter eller ressourcer på montagestyklisten.</span><span class="sxs-lookup"><span data-stu-id="c330e-125">Proceed to enter components or resources on the assembly BOM.</span></span>  
2. <span data-ttu-id="c330e-126">I vinduet **Varekort** for et montageelement skal du vælge handlingen **Montage** og derefter vælge handlingen **Montagestykliste**.</span><span class="sxs-lookup"><span data-stu-id="c330e-126">In the **Item Card** window for an assembly item, choose the **Assembly** action, and then choose the **Assembly BOM** action.</span></span>
3. <span data-ttu-id="c330e-127">I vinduet **Montagestykliste** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="c330e-127">In the **Assembly BOM** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a><span data-ttu-id="c330e-128">Sådan får du vist komponenterne for et montageelement indrykket i overensstemmelse med styklistestrukturen</span><span class="sxs-lookup"><span data-stu-id="c330e-128">To view the components of an assembly item indented according to the BOM structure</span></span>
<span data-ttu-id="c330e-129">Fra vinduet **Montagestykliste** kan du åbne et separat vindue, der viser komponenterne og evt. ressourcer, der er indrykket i henhold til deres placering på styklisten under montageelementet.</span><span class="sxs-lookup"><span data-stu-id="c330e-129">From the **Assembly BOM** window, you can open a separate window that shows the components and any resources indented according to their BOM position under the assembly item.</span></span>

1. <span data-ttu-id="c330e-130">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c330e-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="c330e-131">Åbn kortet for et montageelement.</span><span class="sxs-lookup"><span data-stu-id="c330e-131">Open the card for an assembly item.</span></span> <span data-ttu-id="c330e-132">(Feltet **Montagestykliste** i vinduet **Varer** indeholder **Ja**).</span><span class="sxs-lookup"><span data-stu-id="c330e-132">(The **Assembly BOM** field in the **Items** window contains **Yes**.)</span></span>
3. <span data-ttu-id="c330e-133">I vinduet **Varekort** skal du vælge handlingen **Montage** og derefter vælge handlingen **Montagestykliste**.</span><span class="sxs-lookup"><span data-stu-id="c330e-133">In the **Item Card** window, choose the **Assembly** action, and then choose the **Assembly BOM** action.</span></span>
4. <span data-ttu-id="c330e-134">I vinduet **Montagestykliste** skal du vælge handlingen **Vis stykliste**.</span><span class="sxs-lookup"><span data-stu-id="c330e-134">In the **Assembly BOM** window, choose the **Show BOM** action.</span></span>

## <a name="to-buy-sell-or-transfer-assembly-items"></a><span data-ttu-id="c330e-135">Sådan køber, sælger eller overfører du montageelementer</span><span class="sxs-lookup"><span data-stu-id="c330e-135">To buy, sell, or transfer assembly items</span></span>
<span data-ttu-id="c330e-136">Da den aktuelle version af [!INCLUDE[d365fin](includes/d365fin_md.md)] kun giver mulighed for at definere og tildele montagestyklister til varer, kan du kun håndtere montageelementer på dokumentlinjer som almindelige varer.</span><span class="sxs-lookup"><span data-stu-id="c330e-136">Because the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] only contains the ability to define and assign assembly BOMs to items, you can handle assembly items on document lines as normal items only.</span></span>

<span data-ttu-id="c330e-137">**Advarsel!** Lagerantallet for styklistekomponenter reguleres ikke, hvis du gør dette.</span><span class="sxs-lookup"><span data-stu-id="c330e-137">**Caution**: The inventory quantity of BOM components will not be adjusted if you do so.</span></span>

## <a name="see-also"></a><span data-ttu-id="c330e-138">Se også</span><span class="sxs-lookup"><span data-stu-id="c330e-138">See Also</span></span>
[<span data-ttu-id="c330e-139">Fremgangsmåde: Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="c330e-139">How to: Register New Items</span></span>](inventory-how-register-new-items.md)  
<span data-ttu-id="c330e-140">[Sådan gør du: Vise varedisponering](inventory-how-availability-overview.md)   </span><span class="sxs-lookup"><span data-stu-id="c330e-140">[How to: View the Availability of Items](inventory-how-availability-overview.md)   </span></span>  
[<span data-ttu-id="c330e-141">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="c330e-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="c330e-142">[Arbejde med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c330e-142">[Working with [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>

