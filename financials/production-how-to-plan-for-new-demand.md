---
title: "Sådan planlægges ordre for ordre | Microsoft Docs"
description: "Denne planlægningsopgave kan udføres i vinduet **Ordreplanlægning**, hvor alle nye behov vises sammen med tilgængelighedsoplysninger og forsyningsforslag. Vinduet giver det fornødne overblik og de nødvendige værktøjer til at planlægge behovet effektivt ud fra salgslinjer og komponentlinjer og derefter direkte oprette forskellige typer af forsyningsordrer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 143124fd2e458ee756d47d3f8523380cff6826a9
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-plan-for-new-demand-order-by-order"></a><span data-ttu-id="09d07-104">Fremgangsmåde: Planlægge efter nyt behov ordre for ordre</span><span class="sxs-lookup"><span data-stu-id="09d07-104">How to: Plan for New Demand Order by Order</span></span>
<span data-ttu-id="09d07-105">Denne planlægningsopgave kan udføres i vinduet **Ordreplanlægning**, hvor alle nye behov vises sammen med tilgængelighedsoplysninger og forsyningsforslag.</span><span class="sxs-lookup"><span data-stu-id="09d07-105">This planning task can be performed in the **Order Planning** window, which displays all new demand along with availability information and suggestions for supply.</span></span> <span data-ttu-id="09d07-106">Vinduet giver det fornødne overblik og de nødvendige værktøjer til at planlægge behovet effektivt ud fra salgslinjer og komponentlinjer og derefter direkte oprette forskellige typer af forsyningsordrer.</span><span class="sxs-lookup"><span data-stu-id="09d07-106">It provides the visibility and tools needed to effectively plan demand from sales lines and component lines and then create different types of supply orders directly.</span></span>  

<span data-ttu-id="09d07-107">Du kan gå ind i vinduet **Ordreplanlægning** på to måder afhængigt af arbejdsopgaven: Fra en ordre, du vil planlægge specifikt, eller i batchtilstand, fordi du vil planlægge efter alle nye behov.</span><span class="sxs-lookup"><span data-stu-id="09d07-107">You can enter the **Order Planning** window in two ways depending on your focus: From an order that you want to plan for specifically or in batch mode because you want to plan for all and any new demand.</span></span>  


## <a name="to-plan-for-new-production-order-demand"></a><span data-ttu-id="09d07-108">Planlægge en specifik produktionsordre</span><span class="sxs-lookup"><span data-stu-id="09d07-108">To plan for new production order demand</span></span>  
1.  <span data-ttu-id="09d07-109">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Planlagte produktionsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="09d07-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Planned Production Orders**, and then choose the related link.</span></span> <span data-ttu-id="09d07-110">(Du kan udføre disse trin for planlagte, fastlagte eller frigivne produktionsordrer).</span><span class="sxs-lookup"><span data-stu-id="09d07-110">(You can perform these steps for planned, firm planned, or released production orders).</span></span>
2.  <span data-ttu-id="09d07-111">Åbn den produktionsordre, du vil planlægge, og vælg derefter handlingen **Planlægning**.</span><span class="sxs-lookup"><span data-stu-id="09d07-111">Open the production order you want to plan for, and then choose the **Planning** action.</span></span>  
3.  <span data-ttu-id="09d07-112">Vælg handlingen **Beregn plan** i vinduet **Ordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="09d07-112">In the **Order Planning** window, choose the **Calculate Plan** action.</span></span>  

<span data-ttu-id="09d07-113">Der vises planlægningslinjer i vinduet i overensstemmelse med filteret **Produktionsbehov**, dvs. uopfyldte komponentlinjer for alle eksisterende produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="09d07-113">The window displays planning lines according to the view filter **Production Demand**, meaning unfulfilled component lines of all existing production orders.</span></span> <span data-ttu-id="09d07-114">Behovet for kun denne ene produktionsordre er ikke vist, fordi det er nødvendigt at planlægge til en produktionsordre med et overblik over behovet for eventuelle tidligere komponentlinjer.</span><span class="sxs-lookup"><span data-stu-id="09d07-114">Demand for only the one production order is not shown because it is necessary to plan for one production order with an overview of demand for potentially earlier components lines.</span></span> <span data-ttu-id="09d07-115">Planlægningslinjer for produktionsordren i kontekst udvides.</span><span class="sxs-lookup"><span data-stu-id="09d07-115">Planning lines for the production order in context are expanded.</span></span>  

## <a name="to-plan-for-any-new-demand"></a><span data-ttu-id="09d07-116">Sådan planlægges til alle nye behov</span><span class="sxs-lookup"><span data-stu-id="09d07-116">To plan for any new demand</span></span>  
1. <span data-ttu-id="09d07-117">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ordreplanlægning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="09d07-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Order Planning**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="09d07-118">Vælg handlingen **Beregn plan** i vinduet **Ordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="09d07-118">In the **Order Planning** window, choose the **Calculate Plan** action.</span></span>
3.  <span data-ttu-id="09d07-119">Vælg knappen **Udvid (+)** foran datoen i feltet **Behovsdato** for at få vist de underliggende planlægningslinjer, der repræsenterer behovslinjer med manglende tilgængelighed.</span><span class="sxs-lookup"><span data-stu-id="09d07-119">Choose the **Expand (+)** button in front of the date in the **Demand Date** field to see the underlying planning lines that represent demand lines with insufficient availability.</span></span>  
4.  <span data-ttu-id="09d07-120">For hver udvidet planlægningslinje, dvs. behovslinje, vises der værdier i oplysningsfelterne nederst i vinduet.</span><span class="sxs-lookup"><span data-stu-id="09d07-120">For each expanded planning line, that is, demand line, you can see values in information fields at the bottom of the window.</span></span>  

    |<span data-ttu-id="09d07-121">Indstilling</span><span class="sxs-lookup"><span data-stu-id="09d07-121">Option</span></span>|<span data-ttu-id="09d07-122">Description</span><span class="sxs-lookup"><span data-stu-id="09d07-122">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="09d07-123">**Mængde på andre lokationer**</span><span class="sxs-lookup"><span data-stu-id="09d07-123">**Qty. on Other Locations**</span></span>|<span data-ttu-id="09d07-124">Viser, om varen findes på en anden lokation.</span><span class="sxs-lookup"><span data-stu-id="09d07-124">Shows if the item exists on another location.</span></span> <span data-ttu-id="09d07-125">Du kan derefter søge efter og vælge den.</span><span class="sxs-lookup"><span data-stu-id="09d07-125">You can then look up and select it.</span></span>|  
    |<span data-ttu-id="09d07-126">**Erstatning findes**</span><span class="sxs-lookup"><span data-stu-id="09d07-126">**Substitutes Exist**</span></span>|<span data-ttu-id="09d07-127">Viser om der produceres en erstatningsvare for varen.</span><span class="sxs-lookup"><span data-stu-id="09d07-127">Shows if a substitute item is created for the item.</span></span> <span data-ttu-id="09d07-128">Du kan derefter søge efter og vælge den.</span><span class="sxs-lookup"><span data-stu-id="09d07-128">You can then look up and select it.</span></span> <span data-ttu-id="09d07-129">Bemærk, at denne funktion kun gælder for komponenter, dvs. behovslinjer af typen **Produktion**.</span><span class="sxs-lookup"><span data-stu-id="09d07-129">Note that this feature only applies to components, that is, from demand lines of type **Production**.</span></span>|  
    |<span data-ttu-id="09d07-130">**Disponibelt antal**</span><span class="sxs-lookup"><span data-stu-id="09d07-130">**Quantity Available**</span></span>|<span data-ttu-id="09d07-131">Viser den samlede tilgængelighed for varen, dvs. Planlagt disponibel balance.</span><span class="sxs-lookup"><span data-stu-id="09d07-131">Shows the total availability of the item, that is, the Projected Available Balance.</span></span>|  
    |<span data-ttu-id="09d07-132">**Tidligste disponible dato**</span><span class="sxs-lookup"><span data-stu-id="09d07-132">**Earliest Date Available**</span></span>|<span data-ttu-id="09d07-133">Viser ankomstdatoen for en indgående leveringsordre, der kan dække den nødvendige mængde på en dato, der er senere end behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="09d07-133">Shows the arrival date of an inbound supply order that can cover the needed quantity on a date later than the demand date.</span></span>|  

5.  <span data-ttu-id="09d07-134">Vælg, hvilken type forsyningsordre der skal oprettes, i feltet **Genbestillingssystem**.</span><span class="sxs-lookup"><span data-stu-id="09d07-134">In the **Replenishment System** field, select which type of supply order to create.</span></span>  

    <span data-ttu-id="09d07-135">Standardværdien er værdien på varekortet, eller lagerkortet, men du kan ændre den til en af disse tre indstillinger:</span><span class="sxs-lookup"><span data-stu-id="09d07-135">The default value is that of the item card, or SKU card, but you can change it to one of three options:</span></span>  

    |<span data-ttu-id="09d07-136">Indstilling</span><span class="sxs-lookup"><span data-stu-id="09d07-136">Option</span></span>|<span data-ttu-id="09d07-137">Description</span><span class="sxs-lookup"><span data-stu-id="09d07-137">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="09d07-138">**Køb**</span><span class="sxs-lookup"><span data-stu-id="09d07-138">**Purchase**</span></span>|<span data-ttu-id="09d07-139">Opretter en købsordre.</span><span class="sxs-lookup"><span data-stu-id="09d07-139">Creates a purchase order.</span></span>|  
    |<span data-ttu-id="09d07-140">**Overførsel**</span><span class="sxs-lookup"><span data-stu-id="09d07-140">**Transfer**</span></span>|<span data-ttu-id="09d07-141">Opretter en overflytningsordre.</span><span class="sxs-lookup"><span data-stu-id="09d07-141">Creates a transfer order.</span></span>|  
    |<span data-ttu-id="09d07-142">**Prod.ordre**</span><span class="sxs-lookup"><span data-stu-id="09d07-142">**Prod. Order**</span></span>|<span data-ttu-id="09d07-143">Opretter en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="09d07-143">Creates a production order.</span></span>|  

    <span data-ttu-id="09d07-144">I feltet **Forsyning fra** skal du vælge en værdi, der svarer til det valgte genbestillingssystem.</span><span class="sxs-lookup"><span data-stu-id="09d07-144">In the **Supply From** field you must select a value according to the selected replenishment system.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="09d07-145">Hvis feltet ikke udfyldes, viser systemet en fejlmeddelelse, når du bruger funktionen **Opret forsyningsordrer**, og derefter oprettes der ikke nogen forsyningsordre til den pågældende planlægningslinje.</span><span class="sxs-lookup"><span data-stu-id="09d07-145">If the field is not filled in, the system will display an error message when you use the **Make Supply Order** function, and no supply order will be created for the planning line in question.</span></span> <span data-ttu-id="09d07-146">Dette dog gælder ikke, hvis genbestillingssystemet er **Prod.ordre**.</span><span class="sxs-lookup"><span data-stu-id="09d07-146">This, however, is not the case if the replenishment system is **Prod. Order**.</span></span>  

6.  <span data-ttu-id="09d07-147">Du kan slå op i den relevante liste i feltet **Forsyning fra**, og vælge, hvor forsyningen skal komme fra:</span><span class="sxs-lookup"><span data-stu-id="09d07-147">From the **Supply From** field, you can look up in the relevant list and select where the supply should come from:</span></span>  

    - <span data-ttu-id="09d07-148">Hvis genforsyningssystemet er **Køb**, kan du bruge opslagsknappen i dette felt til at slå op i vinduet **Vare/leverandører**.</span><span class="sxs-lookup"><span data-stu-id="09d07-148">If replenishment system is **Purchase**, the look-up button in this field looks up in the **Item Vendor Catalog** window.</span></span>  
    - <span data-ttu-id="09d07-149">Hvis genforsyningssystemet er **Overførsel**, kan du bruge opslagsknappen i dette felt til at slå op i vinduet **Lokationsoversigt**.</span><span class="sxs-lookup"><span data-stu-id="09d07-149">If replenishment system is **Transfer**, the look-up button in this field looks up in the **Location List** window.</span></span>  

    <span data-ttu-id="09d07-150">Hvis varen findes på en anden lokation, vises der en værdi i feltet **Mængde på anden placering** forneden, og du kan derefter søge efter og vælge den lokation, varen skal forsynes fra, når du opretter overflytningsordren.</span><span class="sxs-lookup"><span data-stu-id="09d07-150">In case the item exists in another location, the **Qty. on Other Location** field at the bottom shows a value and you can then look up and select the location from which the item should be supplied when you make the transfer order.</span></span>  

    <span data-ttu-id="09d07-151">Hvis der findes en erstatning for den ønskede vare, er feltet **Erstatning findes** nederst i vinduet indstillet til **Ja**, og du kan derefter slå op i vinduet **Erstatningsvareposter** og vælge en erstatningsvare.</span><span class="sxs-lookup"><span data-stu-id="09d07-151">If a substitute exists for the demanded item, the **Substitute Exists** field is set to **Yes**, and you can then look up to the **Item Substitution Entries** window and select the substitute.</span></span>  

7.  <span data-ttu-id="09d07-152">Marker feltet **Reserver**, hvis der skal foretages en reservation mellem den forsyningsordre, du opretter, og den behovslinje, som den oprettes til.</span><span class="sxs-lookup"><span data-stu-id="09d07-152">Select the **Reserve** check box if you want to make a reservation between the supply order you are creating and the demand line that it is created for.</span></span> <span data-ttu-id="09d07-153">Feltet er som standard tomt.</span><span class="sxs-lookup"><span data-stu-id="09d07-153">It is empty by default.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="09d07-154">Du kan kun markere dette afkrydsningsfelt, hvis varen har **Eventuelt** eller **Altid** i feltet **Reserver** på dets varekort.</span><span class="sxs-lookup"><span data-stu-id="09d07-154">You can only select this check box if the item has **Optional** or **Always** in the **Reserve** field on its item card.</span></span>  

8.  <span data-ttu-id="09d07-155">I feltet **Antal til ordre** kan du angive det antal, der skal bestilles på den oprettede forsyningsordre.</span><span class="sxs-lookup"><span data-stu-id="09d07-155">In the **Qty. to Order** field, you can enter the quantity that will go on the supply order you are creating.</span></span>   
    <span data-ttu-id="09d07-156">Standardværdien er det samme antal som i feltet **Nødvendigt antal**.</span><span class="sxs-lookup"><span data-stu-id="09d07-156">The default value is the same quantity as that in the **Needed Quantity** field.</span></span> <span data-ttu-id="09d07-157">Men du kan beslutte at bestille mere eller mindre end dette antal på grundlag af din viden om behovet.</span><span class="sxs-lookup"><span data-stu-id="09d07-157">But you may decide to order more or less than this quantity based on your knowledge of the demand situation.</span></span> <span data-ttu-id="09d07-158">Hvis du f.eks. i vinduet **Ordreplanlægning** kan se, at der er flere ikke-relaterede behovslinjer for den samme købte vare, og de forfalder omkring den samme dato, kan du konsolidere disse ved at indtaste det samlede nødvendige antal i feltet **Antal til ordre** i én linje og derefter slette de andre, forældede planlægningslinjer for den pågældende vare.</span><span class="sxs-lookup"><span data-stu-id="09d07-158">If, for example, you see in the **Order Planning** window that several unrelated demand lines are for the same purchased item, and they are due around the same date, you can consolidate these by entering the total needed quantity in the **Qty. to Order** field of one line, and then delete the other, obsolete planning lines for that item.</span></span>  

9.  <span data-ttu-id="09d07-159">I felterne **Forfaldsdato** og **Ordredato** kan du skrive de datoer, der skal gælde for de oprettede forsyningsordrer.</span><span class="sxs-lookup"><span data-stu-id="09d07-159">In the **Due Date** and **Order Date** fields, you can enter the dates that should apply to the created supply orders.</span></span>  

    <span data-ttu-id="09d07-160">Disse to felter er afhængige af hinanden i overensstemmelse med feltet **Standardsikkerhedstid**, som du kan finde i vinduet **Produktionsopsætning**.</span><span class="sxs-lookup"><span data-stu-id="09d07-160">These two fields are interrelated according to the **Default Safety Lead Time** field, which can be found in the **Manufacturing Setup** window.</span></span> <span data-ttu-id="09d07-161">Forfaldsdatoen er som standard den samme som behovsdatoen, men du kan ændre dem efter eget ønske.</span><span class="sxs-lookup"><span data-stu-id="09d07-161">By default, the due date is the same as the demand date, but you can change this as you like.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="09d07-162"> Hvis du skriver en senere dato end behovsdatoen, modtager du en advarselsmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="09d07-162">If you enter a date later than the demand date, you will receive a warning message.</span></span>  

## <a name="to-make-supply-orders"></a><span data-ttu-id="09d07-163">Sådan laves forsyningsordrer</span><span class="sxs-lookup"><span data-stu-id="09d07-163">To make supply orders</span></span>  
1.  <span data-ttu-id="09d07-164">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Planlagte produktionsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="09d07-164">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Planned Production Orders**, and then choose the related link.</span></span> <span data-ttu-id="09d07-165">Du kan udføre disse trin for en planlagt, fastlagt eller frigivet produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="09d07-165">You can perform these steps for a planned, firm planned, or released production order.</span></span>  
2.  <span data-ttu-id="09d07-166">Åbn den produktionsordre, du vil planlægge, og vælg derefter handlingen **Planlægning**.</span><span class="sxs-lookup"><span data-stu-id="09d07-166">Open the production order you want to plan for, and then choose the **Planning** action.</span></span>  
3.  <span data-ttu-id="09d07-167">Placer markøren på en relevant planlægningslinje, og vælg derefter handlingen **Lav ordrer**.</span><span class="sxs-lookup"><span data-stu-id="09d07-167">Place the cursor on a relevant planning line, and then choose the **Make Orders** action.</span></span>  
4.  <span data-ttu-id="09d07-168">Vælg en af følgende indstillinger i feltet **Lav ordrer for** i oversigtspanelet **Ordreplanlægning** i vinduet **Opret forsyningsordrer**.</span><span class="sxs-lookup"><span data-stu-id="09d07-168">In the **Make Supply Orders** window, on the **Order Planning** FastTab, in the **Make Orders for** field, select one of the following options.</span></span>  

    |<span data-ttu-id="09d07-169">Indstilling</span><span class="sxs-lookup"><span data-stu-id="09d07-169">Option</span></span>|<span data-ttu-id="09d07-170">Description</span><span class="sxs-lookup"><span data-stu-id="09d07-170">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="09d07-171">**Den aktive linje**</span><span class="sxs-lookup"><span data-stu-id="09d07-171">**The Active Line**</span></span>|<span data-ttu-id="09d07-172">Lav en forsyningsordre kun for den linje, markøren er placeret på.</span><span class="sxs-lookup"><span data-stu-id="09d07-172">Make a supply order only for the line where the cursor is placed.</span></span>|  
    |<span data-ttu-id="09d07-173">**Den aktive ordre**</span><span class="sxs-lookup"><span data-stu-id="09d07-173">**The Active Order**</span></span>|<span data-ttu-id="09d07-174">Lav en forsyningsordre for alle linje i den ordre, hvor markøren er placeret.</span><span class="sxs-lookup"><span data-stu-id="09d07-174">Make supply orders for all lines in the order where the cursor is placed.</span></span>|  
    |<span data-ttu-id="09d07-175">**Alle linjer**</span><span class="sxs-lookup"><span data-stu-id="09d07-175">**All Lines**</span></span>|<span data-ttu-id="09d07-176">Lav forsyningsordrer for alle linjer i vinduet **Ordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="09d07-176">Make supply orders for all lines in the **Order Planning** window.</span></span>|  

5.  <span data-ttu-id="09d07-177">Angiv, hvilken type forsyningsordrer, eller indkøbskladdelinjer, der skal oprettes, i oversigtspanelet **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="09d07-177">On the **Options** FastTab, define what kind of supply orders, or requisition worksheet lines, should be made.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="09d07-178">De indstillinger, du senest har foretaget i vinduet **Opret forsyningsordrer**, gemmes under dit bruger-id, så de vises igen, næste gang du benytter vinduet.</span><span class="sxs-lookup"><span data-stu-id="09d07-178">The settings you last made in the **Make Supply Orders** window will be saved under your user ID so that they are the same the next time you use the window.</span></span>  

6.  <span data-ttu-id="09d07-179">Klik på **OK** for at oprette de angivne forsyningsordrer eller indkøbskladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="09d07-179">Choose the **OK** button to make the suggested supply orders or requisition worksheet lines.</span></span>  

<span data-ttu-id="09d07-180">Du har nu foretaget planlægning for et uopfyldt behov ved at oprette de respektive forsyningsordrer.</span><span class="sxs-lookup"><span data-stu-id="09d07-180">You have now planned for the unfulfilled demand by making respective supply orders.</span></span> <span data-ttu-id="09d07-181">De detaljerede oplysninger om bestemte arbejdsgange, når du benytter vinduet **Ordreplanlægning**, afhænger af virksomhedens interne forretningsgange.</span><span class="sxs-lookup"><span data-stu-id="09d07-181">Details about specific work flows when using the **Order Planning** window would depend on a company’s internal policies.</span></span>  

<span data-ttu-id="09d07-182">Når du er færdig med planlægningsarbejdet i vinduet **Ordreplanlægning**, og du f.eks. har angivet en alternativ måde at forsyne det korrekte antal på, kan du fortsætte med at oprette forsyningsordrer for en eller flere planlægningslinjer.</span><span class="sxs-lookup"><span data-stu-id="09d07-182">When you have finished your planning work in the **Order Planning** window, for example defined an alternative way to supply the quantity, you can proceed to create supply orders for one or more of the planning lines.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="09d07-183">De forsyningsordrer, du opretter, kan medføre nye afhængige behov, f.eks. for underliggende produktionsordrer. Du bør derfor vælge **Beregn plan** igen for at finde og løse dem, før du går nedad på listen.</span><span class="sxs-lookup"><span data-stu-id="09d07-183">The supply orders you create may introduce new dependent demand, for example for underlying production orders, and you should therefore choose **Calculate Plan** again to find and resolve this before moving down the list.</span></span>  

## <a name="see-also"></a><span data-ttu-id="09d07-184">Se også</span><span class="sxs-lookup"><span data-stu-id="09d07-184">See Also</span></span>  
[<span data-ttu-id="09d07-185">Skabelon</span><span class="sxs-lookup"><span data-stu-id="09d07-185">Planning</span></span>](production-planning.md)  
[<span data-ttu-id="09d07-186">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="09d07-186">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="09d07-187">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="09d07-187">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="09d07-188">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="09d07-188">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="09d07-189">Køb</span><span class="sxs-lookup"><span data-stu-id="09d07-189">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="09d07-190">[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="09d07-190">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="09d07-191">Konfigurere bedste fremgangsmåder: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="09d07-191">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="09d07-192">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="09d07-192">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
