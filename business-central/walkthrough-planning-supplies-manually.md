---
title: Gennemgang - Manuel planlægning af forsyninger | Microsoft Docs
description: Denne gennemgang viser processen med at planlægge forsyningsordrer til opfyldning af nye behov. Du kan starte forsyningsplanlægningen med faste intervaller, f.eks. hver morgen eller hver mandag, eller når du får besked om det af salg eller produktion, afhængigt af behovstypen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2020
ms.author: edupont
ms.openlocfilehash: cb9db1430a9d2a5628bc14bebd5896dac671318d
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786767"
---
# <a name="walkthrough-planning-supplies-manually"></a><span data-ttu-id="60299-104">Gennemgang: Manuel planlægning af forsyninger</span><span class="sxs-lookup"><span data-stu-id="60299-104">Walkthrough: Planning Supplies Manually</span></span>

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]  

<span data-ttu-id="60299-105">Denne gennemgang viser processen med at planlægge forsyningsordrer til opfyldning af nye behov.</span><span class="sxs-lookup"><span data-stu-id="60299-105">This walkthrough demonstrates the process of planning supply orders to fulfill new demand.</span></span> <span data-ttu-id="60299-106">Du kan starte forsyningsplanlægningen med faste intervaller, f.eks. hver morgen eller hver mandag, eller når du får besked om det af salg eller produktion, afhængigt af behovstypen.</span><span class="sxs-lookup"><span data-stu-id="60299-106">You can initiate supply planning at fixed intervals, for example, every morning or every Monday, or when you are notified by sales or production, depending on the type of demand.</span></span> <span data-ttu-id="60299-107">I denne gennemgang kommer du til at bruge siden **Ordreplanlægning**, der er et simpelt forsyningsplanlægningsværktøj, der er baseret på manuel beslutningstagning i stedet for en parameterbaseret automatisk planlægning.</span><span class="sxs-lookup"><span data-stu-id="60299-107">In this walkthrough you will use the **Order Planning** page, a simple supply planning tool that is based on manual decision-making instead of parameter-based automatic planning.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="60299-108">Om denne gennemgang</span><span class="sxs-lookup"><span data-stu-id="60299-108">About This Walkthrough</span></span>  
 <span data-ttu-id="60299-109">Denne gennemgang illustrerer følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="60299-109">This walkthrough illustrates the following tasks:</span></span>  

-   <span data-ttu-id="60299-110">Planlægning af en købsordre for produktionskomponenter.</span><span class="sxs-lookup"><span data-stu-id="60299-110">Planning a purchase order for manufacturing components.</span></span>  
-   <span data-ttu-id="60299-111">Planlægning af en overflytningsordre til opfyldning af et salgsbehov.</span><span class="sxs-lookup"><span data-stu-id="60299-111">Planning a transfer order to fulfill sales demand.</span></span>  
-   <span data-ttu-id="60299-112">Planlægning af en produktionsordre for en vare med flere niveauer.</span><span class="sxs-lookup"><span data-stu-id="60299-112">Planning a production order for a multilevel item.</span></span>  

## <a name="roles"></a><span data-ttu-id="60299-113">Roller</span><span class="sxs-lookup"><span data-stu-id="60299-113">Roles</span></span>  
 <span data-ttu-id="60299-114">Denne gennemgang viser de opgaver, der udføres af følgende brugerroller:</span><span class="sxs-lookup"><span data-stu-id="60299-114">This walkthrough demonstrates tasks performed by the following user roles:</span></span>  

-   <span data-ttu-id="60299-115">Produktionsplanlægger</span><span class="sxs-lookup"><span data-stu-id="60299-115">Production Planner</span></span>  
-   <span data-ttu-id="60299-116">Indkøbsagent</span><span class="sxs-lookup"><span data-stu-id="60299-116">Purchasing Agent</span></span>  
-   <span data-ttu-id="60299-117">Salgsordrebehandler</span><span class="sxs-lookup"><span data-stu-id="60299-117">Sales Order Processor</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="60299-118">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="60299-118">Prerequisites</span></span>  
 <span data-ttu-id="60299-119">Inden du begynder denne gennemgang, skal du installere [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="60299-119">Before you begin this walkthrough, you must install the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="60299-120">Der skal foretages følgende ændringer i databasen:</span><span class="sxs-lookup"><span data-stu-id="60299-120">The following modifications must be made to the database:</span></span>  

-   <span data-ttu-id="60299-121">Slet alle eksisterende salgsordrer på cykler.</span><span class="sxs-lookup"><span data-stu-id="60299-121">Delete all existing sales orders for bicycles.</span></span>  
-   <span data-ttu-id="60299-122">Opret én salgsordre på ti cykler på lokationen BLÅ.</span><span class="sxs-lookup"><span data-stu-id="60299-122">Create one sales order for 10 bicycles at BLUE location.</span></span>  
-   <span data-ttu-id="60299-123">Slet alle planlagte og fastlagte produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="60299-123">Delete all planned and firm planned production orders.</span></span> <span data-ttu-id="60299-124">Slet ikke startede ordrer med poster, der allerede er bogførte.</span><span class="sxs-lookup"><span data-stu-id="60299-124">Do not delete started orders with entries that are already posted.</span></span>  

 <span data-ttu-id="60299-125">Du skal som hovedregel bruge de foreslåede data i denne gennemgang, da disse data indeholder de nødvendige poster.</span><span class="sxs-lookup"><span data-stu-id="60299-125">As a rule, use the suggested data in this walkthrough because this data has the necessary records.</span></span>  

## <a name="story"></a><span data-ttu-id="60299-126">Historie</span><span class="sxs-lookup"><span data-stu-id="60299-126">Story</span></span>  
 <span data-ttu-id="60299-127">Erik, der er produktionsplanlægger i en mindre produktionsvirksomhed, er ved at planlægge produktions og købsordrer til opfyldning af nye salgsbehov.</span><span class="sxs-lookup"><span data-stu-id="60299-127">Eduardo, the Production Planner of a small manufacturing company, is about to plan production and purchase orders to fulfill new sales demand.</span></span>  

 <span data-ttu-id="60299-128">Da der er få styklisteniveauer i produkterne, og ordrestrømmen er relativ beskeden, anvender Erik siden **Ordreplanlægning** til manuelt at oprette forsyningsordrer – ét produktniveau ad gangen.</span><span class="sxs-lookup"><span data-stu-id="60299-128">Because the products have few BOM levels and the flow of orders is relatively low, Eduardo uses the **Order Planning** page to manually create supply orders, one product level at a time.</span></span>  

 <span data-ttu-id="60299-129">Ved mere komplekse produktionsmiljøer, bruges planlægningskladden til at planlægge forsyningen baseret på vareparametre, som f.eks. ændringsperiode, sikkerhedstid, genbestillingspunkt og batchberegninger af den samlede efterspørgsel fra alle produktniveauer.</span><span class="sxs-lookup"><span data-stu-id="60299-129">In a more complex manufacturing environment, the planning worksheet is used to plan supply based on item parameters such as rescheduling period, safety lead time, reorder point, and batch calculations of consolidated demand from all product levels.</span></span>  

## <a name="setting-up-the-sample-data"></a><span data-ttu-id="60299-130">Oprette eksempeldata</span><span class="sxs-lookup"><span data-stu-id="60299-130">Setting Up the Sample Data</span></span>  
 <span data-ttu-id="60299-131">Standarddemoregnskabet CRONUS har p.t. en stor mængde ikke-planlagte behov.</span><span class="sxs-lookup"><span data-stu-id="60299-131">The standard CRONUS demonstration company currently has lots of unplanned demand.</span></span> <span data-ttu-id="60299-132">Under de forskellige planlægningsopgaver i denne gennemgang vil du få brug for at afvige fra den realistiske forretningsgang ved at ignorere behov med tætte forfaldsdatoer og i stedet bruge behov med senere forfaldsdatoer.</span><span class="sxs-lookup"><span data-stu-id="60299-132">During the different planning tasks in this walkthrough, you will have to deviate from the realistic business flow by ignoring demand with close due dates and instead use demand with later due dates.</span></span>  

## <a name="using-the-order-planning-page"></a><span data-ttu-id="60299-133">Bruge siden Ordreplanlægning</span><span class="sxs-lookup"><span data-stu-id="60299-133">Using the Order Planning Page</span></span>  

<span data-ttu-id="60299-134">Du kan få adgang til siden **Ordreplanlægning** fra flere forskellige lokationer:</span><span class="sxs-lookup"><span data-stu-id="60299-134">The **Order Planning** page can be accessed from several different locations:</span></span>  

-   <span data-ttu-id="60299-135">Produktion, Planlægning</span><span class="sxs-lookup"><span data-stu-id="60299-135">Manufacturing, Planning</span></span>  
-   <span data-ttu-id="60299-136">Salg & Marketing, Ordrebehandling</span><span class="sxs-lookup"><span data-stu-id="60299-136">Sales & Marketing, Order Processing</span></span>  
-   <span data-ttu-id="60299-137">Køb, Planlægning</span><span class="sxs-lookup"><span data-stu-id="60299-137">Purchase, Planning</span></span>  
-   <span data-ttu-id="60299-138">Derudover kan du åbne siden for en bestemt produktionsordre ved at vælge handlingen **Planlægning**.</span><span class="sxs-lookup"><span data-stu-id="60299-138">In addition, you can open this page for a specific production order by choosing the **Planning** action.</span></span>

### <a name="to-use-the-order-planning-page"></a><span data-ttu-id="60299-139">Sådan bruges siden Ordreplanlægning</span><span class="sxs-lookup"><span data-stu-id="60299-139">To use the Order Planning page</span></span>  

1.  <span data-ttu-id="60299-140">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Ordreplanlægning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="60299-140">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Order Planning**, and then choose the related link.</span></span>  

     <span data-ttu-id="60299-141">Når siden **Ordreplanlægning** først åbnes, skal der beregnes en plan for at få vist det nye behov, siden det sidst blev beregnet.</span><span class="sxs-lookup"><span data-stu-id="60299-141">When the **Order Planning** page first opens, a plan must be calculated to show the new demand since it was last calculated.</span></span>  

2.  <span data-ttu-id="60299-142">Vælg handlingen **Beregn plan**.</span><span class="sxs-lookup"><span data-stu-id="60299-142">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="60299-143">Planlægningssystemet analyserer et eventuelt nyt behov, der er kommet til, som f.eks. nye salg, ændrede salg eller produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="60299-143">The planning system analyzes any new demand that has been introduced, such as new sales, changed sales, or production orders.</span></span>  

     <span data-ttu-id="60299-144">Det nødvendige antal for hvert behovslinje beregnes baseret på den samlede tilgængelighed.</span><span class="sxs-lookup"><span data-stu-id="60299-144">Based on total availability, the quantity needed for each demand line is calculated.</span></span> <span data-ttu-id="60299-145">Denne beregning udføres ordre-for-ordre.</span><span class="sxs-lookup"><span data-stu-id="60299-145">This calculation is performed order-by-order.</span></span> <span data-ttu-id="60299-146">Dette betyder, at den ordre, der indeholder behovslinjen med den tidligste forfaldsdato eller afsendelsesdato, beregnes først.</span><span class="sxs-lookup"><span data-stu-id="60299-146">This means that the order which includes the demand line with the earliest due date or shipment date will be calculated first.</span></span> <span data-ttu-id="60299-147">Derefter vil de andre behovslinjer blive beregnet i samme ordre, uanset forfaldsdato eller afsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="60299-147">After that, additional demand lines will be calculated in the same order, regardless of the due date or shipment date.</span></span>  

3.  <span data-ttu-id="60299-148">Sørg for, at siden **Ordreplanlægning** er maksimeret, og at kolonnefelterne er tilpasset, så de viser alle standardfeltnavnene.</span><span class="sxs-lookup"><span data-stu-id="60299-148">Be sure that the **Order Planning** page is maximized and that column fields are resized to show all the default field names.</span></span>  

     <span data-ttu-id="60299-149">Når beregningen er færdig, viser siden alle ikke-opfyldte behov som ikke-udvidede ordrehovedlinjer sorteret efter tidligste behovsdato.</span><span class="sxs-lookup"><span data-stu-id="60299-149">When the calculation is completed, the page displays all unfulfilled demand as collapsed order header lines sorted by earliest demand date.</span></span>  

     <span data-ttu-id="60299-150">Bemærk, at CRONUS har flere ordrer med ikke-opfyldte behov.</span><span class="sxs-lookup"><span data-stu-id="60299-150">Notice that CRONUS has several orders with unfulfilled demand.</span></span> <span data-ttu-id="60299-151">Hver planlægningslinje, der står med fed skrift, repræsenterer en ordre, salgsordre eller produktionsordre, inklusive mindst én ordrelinje med utilstrækkelig disponering.</span><span class="sxs-lookup"><span data-stu-id="60299-151">Each bold planning line represents an order, sales order, or production order, including at least one order line with insufficient availability.</span></span>  

4.  <span data-ttu-id="60299-152">Gå til feltet **Vis behov som**, og vælg filteret **Alle behov**.</span><span class="sxs-lookup"><span data-stu-id="60299-152">In the **Show Demand As** field, select the **All Demand** filter.</span></span>  

     <span data-ttu-id="60299-153">I feltet **Behovstype** kan du vælge, hvilke ordretyper der skal vises.</span><span class="sxs-lookup"><span data-stu-id="60299-153">With the **Demand Type** field, you can choose which order types that you want to display.</span></span>  

     <span data-ttu-id="60299-154">Ordrer, der ikke har disponeringsproblemer, vises ikke.</span><span class="sxs-lookup"><span data-stu-id="60299-154">Orders that do not have availability problems are not shown.</span></span> <span data-ttu-id="60299-155">Hvis der ikke findes nogle ordrer, når en plan beregnes, vil der blive vist en meddelelse, og der vil ikke blive vist nogen planlægningslinjer.</span><span class="sxs-lookup"><span data-stu-id="60299-155">If no orders exist when a plan is calculated, a message will display and no planning lines will appear.</span></span>  

## <a name="planning-a-purchase-order-to-fulfill-component-demand"></a><span data-ttu-id="60299-156">Planlægge en købsordre for at opfylde et komponentbehov</span><span class="sxs-lookup"><span data-stu-id="60299-156">Planning a Purchase Order to Fulfill Component Demand</span></span>  
 <span data-ttu-id="60299-157">I denne procedure opretter du en købsordre til manglende produktionskomponenter.</span><span class="sxs-lookup"><span data-stu-id="60299-157">In this procedure, you create a purchase order for needed manufacturing components.</span></span>  

### <a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a><span data-ttu-id="60299-158">Sådan planlægges en købsordre for at opfylde et komponentbehov i produktionen</span><span class="sxs-lookup"><span data-stu-id="60299-158">To plan a purchase order to fulfill component need in production</span></span>  

1.  <span data-ttu-id="60299-159">Udvid den første linje (vælg symbolet +).</span><span class="sxs-lookup"><span data-stu-id="60299-159">Expand the first line (choose the + symbol).</span></span>  
2.  <span data-ttu-id="60299-160">Vælg den første behovslinje med varen **LSU-15**, og vælg derefter handlingen **Vis dokument**.</span><span class="sxs-lookup"><span data-stu-id="60299-160">Choose the first demand line, with item **LSU-15**, and then choose the **Show Document** action.</span></span>  
3.  <span data-ttu-id="60299-161">Luk den åbnede produktionsordre for at vende tilbage til siden **Ordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="60299-161">Close the opened production order to return to the **Order Planning** page.</span></span>  
4.  <span data-ttu-id="60299-162">Gå til feltet **Genbestillingssystem**, og vælg **Køb**.</span><span class="sxs-lookup"><span data-stu-id="60299-162">In the **Replenishment System** field, select **Purchase**.</span></span>  

     <span data-ttu-id="60299-163">Standardværdien er fra vare- eller lagerkortet, men du kan ændre det til et af følgende muligheder:</span><span class="sxs-lookup"><span data-stu-id="60299-163">The default value is from the item card, or SKU card, but you can change it to one of the following options:</span></span>  

    -   <span data-ttu-id="60299-164">**Køb** – for at oprette en købsordre.</span><span class="sxs-lookup"><span data-stu-id="60299-164">**Purchase** – To create a purchase order.</span></span>  
    -   <span data-ttu-id="60299-165">**Overførsel** – for at oprette en overflytningsordre.</span><span class="sxs-lookup"><span data-stu-id="60299-165">**Transfer** – To create a transfer order.</span></span>  
    -   <span data-ttu-id="60299-166">**Produktionsordre** – for at oprette en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="60299-166">**Prod. Order** – To create a production order.</span></span>  

5.  <span data-ttu-id="60299-167">Vælg en af følgende indstillinger, der svarer til det valgte genbestillingssystem i feltet **Forsyning fra**:</span><span class="sxs-lookup"><span data-stu-id="60299-167">In the **Supply From** field, select one of the following options according to the selected replenishment system:</span></span>  

    -   <span data-ttu-id="60299-168">**Kreditor** – For køb</span><span class="sxs-lookup"><span data-stu-id="60299-168">**Vendor** – For purchases</span></span>  
    -   <span data-ttu-id="60299-169">**Lokation** – til overførsler</span><span class="sxs-lookup"><span data-stu-id="60299-169">**Location** – For transfers</span></span>  

     <span data-ttu-id="60299-170">Hvis feltet ikke er udfyldt, vises der en fejlmeddelelse, når du prøver at oprette forsyningsordren.</span><span class="sxs-lookup"><span data-stu-id="60299-170">If the field is not filled in, an error message will display when you try to create the supply orders.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="60299-171">Hvis der er oprettet et standardleverandørnummer på varekortene for komponenterne, vil linjerne være forudindstillet.</span><span class="sxs-lookup"><span data-stu-id="60299-171">If the components have a default vendor number set up on the item cards, the lines will be preset.</span></span>  

6.  <span data-ttu-id="60299-172">Markér feltet **Forsyning fra**.</span><span class="sxs-lookup"><span data-stu-id="60299-172">Choose the **Supply From**  field.</span></span>  
7.  <span data-ttu-id="60299-173">På siden **Vare/leverandører** skal du vælge handlingen **Ny** og derefter vælge leverandør **30000**.</span><span class="sxs-lookup"><span data-stu-id="60299-173">On the **Item Vendor Catalogue** page, choose the **New** action, and then select vendor **30000**.</span></span>  
8.  <span data-ttu-id="60299-174">Vælg knappen **OK** for at gå tilbage til siden **Ordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="60299-174">Choose the **OK** button to return to the **Order Planning** page.</span></span>  
9. <span data-ttu-id="60299-175">Kopier leverandør **30000** for til andre linjer for højttalerkomponenterne på denne produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="60299-175">Copy vendor **30000** to the other lines for loudspeaker components on this production order.</span></span>  

     <span data-ttu-id="60299-176">Du er nu klar til at oprette en købsordre.</span><span class="sxs-lookup"><span data-stu-id="60299-176">You are now ready to create a purchase order.</span></span>  

10. <span data-ttu-id="60299-177">Vælg handlingen **Lav ordrer**.</span><span class="sxs-lookup"><span data-stu-id="60299-177">Choose the **Make Orders** action.</span></span> <span data-ttu-id="60299-178">Siden **Opret forsyningsordrer** åbnes.</span><span class="sxs-lookup"><span data-stu-id="60299-178">The **Make Supply Orders** page opens.</span></span>  
11. <span data-ttu-id="60299-179">På oversigtspanelet **Ordreplanlægning**, i feltet **Lav ordrer for**, skal du vælge muligheden **Aktiv ordre**.</span><span class="sxs-lookup"><span data-stu-id="60299-179">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **Active Order** option.</span></span>  
12. <span data-ttu-id="60299-180">Gå til oversigtspanelet **indstillinger** og feltet **Opret købsordre**, og vælg indstillingen **Opret købsordrer**.</span><span class="sxs-lookup"><span data-stu-id="60299-180">On the **Options** FastTab, in the **Create Purchase Order** field, choose the **Make Purch. Order** option.</span></span>  
13. <span data-ttu-id="60299-181">Vælg **OK**-knappen for at oprette købsordrer for alle komponenterne i ordren.</span><span class="sxs-lookup"><span data-stu-id="60299-181">Choose the **OK** button to create purchase orders for all the components of the order.</span></span>  

     <span data-ttu-id="60299-182">Købsordrerne er nu oprettet og gemt som de sidste ordrer på listen over købsordrer.</span><span class="sxs-lookup"><span data-stu-id="60299-182">The purchase orders are now created and saved as the last orders in the list of purchase orders.</span></span>  

## <a name="planning-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="60299-183">Planlægge en overflytningsordre for at opfylde et salgsbehov</span><span class="sxs-lookup"><span data-stu-id="60299-183">Planning a Transfer Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="60299-184">I denne procedure kommer du til at planlægge ud fra et behov fra en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="60299-184">In this procedure, you will plan for demand from a sales order.</span></span> <span data-ttu-id="60299-185">Behovslinjerne repræsenterer salgslinjer og ikke komponentlinjer som ved produktionsbehov.</span><span class="sxs-lookup"><span data-stu-id="60299-185">Demand lines represent sales lines and not component lines, as in production demand.</span></span>  

### <a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="60299-186">Sådan planlægges en overflytningsordre til opfyldning af et salgsbehov.</span><span class="sxs-lookup"><span data-stu-id="60299-186">To plan a transfer order to fulfill sales demand</span></span>  

1.  <span data-ttu-id="60299-187">Flyt markøren til planlægningslinjen for ordre **2008**.</span><span class="sxs-lookup"><span data-stu-id="60299-187">Move the pointer to the planning line for order **2008**.</span></span>  
2.  <span data-ttu-id="60299-188">Udvid linjen, og flyt markøren til behovslinjen.</span><span class="sxs-lookup"><span data-stu-id="60299-188">Expand the line and move the pointer to the demand line.</span></span>  

     <span data-ttu-id="60299-189">Salgsordre **2008** er på ti højttalere, vare **LS-120**, der er bestilt af Lauritzen Kontormøbler A/S.</span><span class="sxs-lookup"><span data-stu-id="60299-189">Sales order **2008** is for ten loudspeakers, item **LS-120**, ordered by John Haddock Insurance Co.</span></span>  

     <span data-ttu-id="60299-190">Varens definerede genbestillingssystem og standardleverandør vises.</span><span class="sxs-lookup"><span data-stu-id="60299-190">The item’s defined replenishment system and default vendor will display.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="60299-191">Nederst på siden er der fire oplysningsfelter.</span><span class="sxs-lookup"><span data-stu-id="60299-191">At the bottom of the page, there are four information fields.</span></span> <span data-ttu-id="60299-192">I feltet **Tidligste disponible dato** vil de ti stykker, der er behov for, være til disposition på en indgående forsyningsordre ni dage senere end den aktuelle forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="60299-192">In the **Earliest Date Available** field, the ten pieces that are needed will be available, on an inbound supply order, nine days later than the current due date.</span></span> <span data-ttu-id="60299-193">Hvis dette er for sent for kunden, viser feltet **Disponibel til overflytning** 13 stykker af varen på en anden lokation.</span><span class="sxs-lookup"><span data-stu-id="60299-193">If this is too late for the customer, the **Available for Transfer** field shows 13 pieces of the item at another location.</span></span> <span data-ttu-id="60299-194">Du vil skulle planlægge denne lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="60299-194">You will want to plan for this stock.</span></span>  

3.  <span data-ttu-id="60299-195">Vælg feltet **Disponibel til overflytning** for at åbne siden **Hent alternativ forsyning**.</span><span class="sxs-lookup"><span data-stu-id="60299-195">Choose the **Available for Transfer** field to open the **Get Alternative Supply** page.</span></span>  
4.  <span data-ttu-id="60299-196">Vælg **OK**-knappen for at registrere de ti varer, der er til disposition.</span><span class="sxs-lookup"><span data-stu-id="60299-196">Choose the **OK** button to book the ten items that are available.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="60299-197">Det foreslåede køb i behovslinjen er erstattet med en overførsel fra lokationen GRØN.</span><span class="sxs-lookup"><span data-stu-id="60299-197">In the demand line, the suggested purchase has been exchanged with a transfer from GREEN location.</span></span> <span data-ttu-id="60299-198">Funktionen **Lav ordrer** opretter en overflytningsordre fra GRØN til den påkrævede lokation.</span><span class="sxs-lookup"><span data-stu-id="60299-198">The **Make Orders** function creates a transfer order from GREEN to the demanded location.</span></span> <span data-ttu-id="60299-199">Feltet **Erstatning findes** fungerer på samme måde.</span><span class="sxs-lookup"><span data-stu-id="60299-199">The **Substitutes Exists** field works in the same way.</span></span>  

5.  <span data-ttu-id="60299-200">Vælg handlingen **Lav ordrer**.</span><span class="sxs-lookup"><span data-stu-id="60299-200">Choose the **Make Orders** action.</span></span> <span data-ttu-id="60299-201">Siden **Opret forsyningsordrer** åbnes.</span><span class="sxs-lookup"><span data-stu-id="60299-201">The **Make Supply Orders** page opens.</span></span>  
6.  <span data-ttu-id="60299-202">På oversigtspanelet **Ordreplanlægning**, i feltet **Lav ordrer for**, skal du vælge muligheden **Den aktive ordre**.</span><span class="sxs-lookup"><span data-stu-id="60299-202">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **The Active Order** option.</span></span>  
7.  <span data-ttu-id="60299-203">Gå til oversigtspanelet **indstillinger** og feltet **Opret overflytningsordre**, og vælg indstillingen **Opret overførselsordrer**.</span><span class="sxs-lookup"><span data-stu-id="60299-203">On the **Options** FastTab, in the **Create Transfer Order** field, select the **Make Trans. Orders** option.</span></span>  
8.  <span data-ttu-id="60299-204">Vælg knappen **OK** for at oprette overførselsordren til forsyning af salgsordren.</span><span class="sxs-lookup"><span data-stu-id="60299-204">Choose the **OK** button to create the transfer order to supply the sales order.</span></span>  

     <span data-ttu-id="60299-205">Overførselsordren er nu oprettet og gemt som den sidste ordre på listen over åbne overførselsordrer.</span><span class="sxs-lookup"><span data-stu-id="60299-205">The transfer order is now created and saved in the list as the last order in the list of open transfer orders.</span></span>  

## <a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a><span data-ttu-id="60299-206">Planlægge en Produktionsordre med flere niveauer for at opfylde et salgsbehov</span><span class="sxs-lookup"><span data-stu-id="60299-206">Planning a Multilevel Production Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="60299-207">I denne procedure kommer du til at planlægge en opfyldning af et salgsbehov for en produceret vare med flere produktniveauer, der hver opretter afhængige produktionsbehov.</span><span class="sxs-lookup"><span data-stu-id="60299-207">In this procedure, you will plan to fulfill sales demand for a produced item with multiple product levels, each creating dependent production demand.</span></span>  

### <a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a><span data-ttu-id="60299-208">Sådan planlægges en produktion med flere niveauer for at opfylde et salgsbehov</span><span class="sxs-lookup"><span data-stu-id="60299-208">To plan multilevel production to fulfill sales demand</span></span>  

1.  <span data-ttu-id="60299-209">Vælg planlægningslinjen med salgsbehovet for ordre **1001**, oprettet tidligere som forudsætningsdata.</span><span class="sxs-lookup"><span data-stu-id="60299-209">Select the planning line with sales demand for order **1001**, created earlier as prerequisite data.</span></span>  

     <span data-ttu-id="60299-210">Behovet er en salgslinje, men varen har et defineret genbestillingssystem for **Prod.ordre**.</span><span class="sxs-lookup"><span data-stu-id="60299-210">This demand is a sales line, but the item has a defined replenishment system of **Prod. Order**.</span></span> <span data-ttu-id="60299-211">Fortsæt med at tilføje en ekstra ringeklokke til komponentbehovet for hver cykel.</span><span class="sxs-lookup"><span data-stu-id="60299-211">Proceed to add an extra bell to the component need of each bicycle.</span></span>  

2.  <span data-ttu-id="60299-212">Vælg handlingen **Komponenter** for at åbne siden **Planlægning - komponenter**.</span><span class="sxs-lookup"><span data-stu-id="60299-212">Choose the **Components** action to open the **Planning Components** page.</span></span>  
3.  <span data-ttu-id="60299-213">På linjen for Ringeklokke skal du ændre feltet **Antal pr.** fra **1** til **2**.</span><span class="sxs-lookup"><span data-stu-id="60299-213">On the line with the Bell item, change the **Quantity per** field from **1** to **2**.</span></span>  
4.  <span data-ttu-id="60299-214">Overvej dine planlægningsalternativer på siden **Ordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="60299-214">On the **Order Planning** page, consider your planning alternatives.</span></span> <span data-ttu-id="60299-215">I dette tilfælde har du ingen alternative forsyningsmuligheder, ingen overførsel, erstatning eller senere levering.</span><span class="sxs-lookup"><span data-stu-id="60299-215">In this case, you have no alternative means of supply, no transfer, substitute, or later delivery.</span></span> <span data-ttu-id="60299-216">Du skal oprette den foreslåede forsyningsordre, en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="60299-216">You must create the suggested supply order, a production order.</span></span>  
5.  <span data-ttu-id="60299-217">Vælg handlingen knappen **Lav ordrer** for at oprette produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="60299-217">Choose the **Make Orders** action to create the production order.</span></span>  

     <span data-ttu-id="60299-218">På siden **Ordreplanlægning** kan du se, at planlægningslinjen for salgsordre **1001** ikke længere findes, og at det første salgsbehov er dækket.</span><span class="sxs-lookup"><span data-stu-id="60299-218">On the **Order Planning** page, notice that the planning line for sales order **1001** no longer exists and that the initial sales demand has been covered.</span></span>  

6.  <span data-ttu-id="60299-219">Luk siden **Ordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="60299-219">Close the **Order Planning** page.</span></span>  

     <span data-ttu-id="60299-220">Nu kunne du vælge at blive i denne visning og færdiggøre planlægningsopgaverne.</span><span class="sxs-lookup"><span data-stu-id="60299-220">Now, you could choose to stay in this view and complete all the planning tasks.</span></span> <span data-ttu-id="60299-221">I stedet vil du dog nu antage rollen som produktionsplanlægger ved at gå til den produktionsordre, som du lige har oprettet, og åbne siden **Ordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="60299-221">Instead, you will now take on the Production Planner role by going to the production order that you just created and access the **Order Planning** page.</span></span>  

 <span data-ttu-id="60299-222">Som produktionsplanlægger skal du planlægge en specifik produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="60299-222">As a production planner you now must plan a specific production order.</span></span>  

### <a name="to-plan-a-specific-production-order"></a><span data-ttu-id="60299-223">Sådan planlægges en specifik produktionsordre</span><span class="sxs-lookup"><span data-stu-id="60299-223">To plan a specific production order</span></span>  

1.  <span data-ttu-id="60299-224">Åbn produktionsordren **101001**, på ti cykler, som du oprettede ved at bruge funktionen **Lav ordrer**.</span><span class="sxs-lookup"><span data-stu-id="60299-224">Open the production order **101001**, for ten bicycles, that you just created by using the **Make Orders** function.</span></span>  
2.  <span data-ttu-id="60299-225">Åbn siden **Prod.ordrekomponenter** for at kontrollere, at de ekstra ringeklokker afspejles på produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="60299-225">Open the **Prod. Order Components** page to check that the extra bell is reflected on the production order.</span></span>  
3.  <span data-ttu-id="60299-226">Vælg handlingen **Planlægning**.</span><span class="sxs-lookup"><span data-stu-id="60299-226">Choose the **Planning** action.</span></span>  

     <span data-ttu-id="60299-227">Siden **Ordreplanlægning** åbnes i en visning, der altid er filtreret ud fra det specifikke produktionsbehov.</span><span class="sxs-lookup"><span data-stu-id="60299-227">The **Order Planning** page opens in a view that is always filtered on the specific production demand.</span></span> <span data-ttu-id="60299-228">Salgsbehovet vises ikke.</span><span class="sxs-lookup"><span data-stu-id="60299-228">Sales demand is not displayed.</span></span> <span data-ttu-id="60299-229">Du skal beregne en plan, før du kan se et eventuelt ekstra behov.</span><span class="sxs-lookup"><span data-stu-id="60299-229">You must calculate a plan before you can see any additional demand.</span></span>  

4.  <span data-ttu-id="60299-230">Vælg handlingen **Beregn plan**.</span><span class="sxs-lookup"><span data-stu-id="60299-230">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="60299-231">Bemærk, at de nye produktionsordrer vises som ikke-planlagt produktionsbehov, der er afledt af ordren **101001**.</span><span class="sxs-lookup"><span data-stu-id="60299-231">Notice that four new production orders appear as unplanned production demand derived from order **101001**.</span></span> <span data-ttu-id="60299-232">De nye linjer repræsenterer et nyt produktionsbehov fra de underordnede samlinger, der skal oprettes for at producere ordren.</span><span class="sxs-lookup"><span data-stu-id="60299-232">The new lines represent new production demand from the subassemblies that must be created to produce the order.</span></span>  

5.  <span data-ttu-id="60299-233">Vælg handlingen **Udvid alle** for at få vist en oversigt over alle produktionsbehov for produktionsordrerne.</span><span class="sxs-lookup"><span data-stu-id="60299-233">Choose the **Expand All** action to get an overview of all the production demand for the production orders.</span></span>  

     <span data-ttu-id="60299-234">Hvis du vil angive yderligere oplysninger om behovslinjerne, kan du tilføjefelterne **Behovsmængde** og **Tilgængelig behovsmængde** til visningen.</span><span class="sxs-lookup"><span data-stu-id="60299-234">To provide additional information about the demand lines, you may want to add the **Demand Quantity** and **Demand Qty. Available** fields to your view.</span></span>  

     <span data-ttu-id="60299-235">Nu skal du levere ti af hver komponent.</span><span class="sxs-lookup"><span data-stu-id="60299-235">Now you must supply ten of each component.</span></span>  

     <span data-ttu-id="60299-236">Bemærk, at fire af behovslinjerne har angivet genbestillingssystemet Prod.ordre.</span><span class="sxs-lookup"><span data-stu-id="60299-236">Note that four of the demand lines have replenishment system Prod. Order.</span></span> <span data-ttu-id="60299-237">Disse fire halvfabrikata repræsenterer det andet produktniveau af cyklen.</span><span class="sxs-lookup"><span data-stu-id="60299-237">These four subassemblies represent the second product level of the bicycle.</span></span>  

     <span data-ttu-id="60299-238">Standardindstillingerne for genbestilling er allerede udfyldt, og du kan fortsætte til at lave ordrer.</span><span class="sxs-lookup"><span data-stu-id="60299-238">The default replenishment settings are already filled in and you can proceed to make orders.</span></span>  

6.  <span data-ttu-id="60299-239">Vælg handlingen **Lav ordrer**.</span><span class="sxs-lookup"><span data-stu-id="60299-239">Choose the **Make Orders** action.</span></span>  

     <span data-ttu-id="60299-240">Før du klikker på **OK**, skal du bemærke teksten i oversigtspanelet **Ordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="60299-240">Before you choose the **OK** button, notice the text on the **Order Planning** FastTab.</span></span> <span data-ttu-id="60299-241">Denne tekst er vigtig, fordi du ved, at cyklen har adskillige producerede komponenter, halvfabrikata, i produktstrukturen, som der kan være behov for, når du opretter denne produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="60299-241">This text is important because you know that the bicycle has several produced components, subassemblies, in its product structure that might be in demand when you create this production order.</span></span>  

7.  <span data-ttu-id="60299-242">Vælg indstillingen **Alle linjer**, og derefter knappen **OK** i feltet **Lav ordrer for** på siden **Opret forsyningsordre for** for at oprette produktionsordrer for det andet ordreproduktniveau.</span><span class="sxs-lookup"><span data-stu-id="60299-242">On the **Make Supply Order** page, in the **Make Orders for** field, choose the **All Lines** option, and then choose the **OK** button to create production orders for the second product level of the order.</span></span>  

     <span data-ttu-id="60299-243">Bemærk, at det øverste niveau i produktionsbehovet for produktionsordre 101001 ikke længere findes.</span><span class="sxs-lookup"><span data-stu-id="60299-243">Note that the top-level production demand for production order 101001 no longer exists.</span></span> <span data-ttu-id="60299-244">Dette betyder, at der er foretage planlægning for det første produktionsbehov for de underordnede samlinger.</span><span class="sxs-lookup"><span data-stu-id="60299-244">This means that the initial production demand for subassemblies has been planned for.</span></span>  

     <span data-ttu-id="60299-245">På siden **Ordreplanlægning** beregner du igen en plan for at planlægge cykelstrukturen.</span><span class="sxs-lookup"><span data-stu-id="60299-245">On the **Order Planning** page, you calculate a plan again in order to plan the bicycle structure.</span></span>  

8.  <span data-ttu-id="60299-246">Vælg handlingen **Beregn plan** for at genberegne planen som angivet i den integrerede hjælpetekst.</span><span class="sxs-lookup"><span data-stu-id="60299-246">Choose the **Calculate Plan** action to recalculate the plan as instructed by the embedded Help text.</span></span>  

     <span data-ttu-id="60299-247">De to nye linjer repræsenterer et yderligere produktionsbehov fra de underordnede samlinger, der er planlagt i de forrige trin.</span><span class="sxs-lookup"><span data-stu-id="60299-247">The two new lines represent additional production demand derived from the subassemblies planned in the previous steps.</span></span> <span data-ttu-id="60299-248">Det foreslås, at du opretter to produktionsordrer til forsyning af hjulnav, én til 10 nav fortil og én til 10 nav bagtil.</span><span class="sxs-lookup"><span data-stu-id="60299-248">It is suggested that you make two production orders to supply the wheel hubs, one for 10 front hubs and one for 10 back hubs.</span></span>  

9. <span data-ttu-id="60299-249">Vælg handlingen **Udvid alle** for at få vist en oversigt over alle behov for de to produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="60299-249">Choose the **Expand All** action to get an overview of all the demand for the two production orders.</span></span>  

     <span data-ttu-id="60299-250">Den foreslåede forsyningsplan indikerer, at der i alt oprettes fire købsordrer for komponenterne.</span><span class="sxs-lookup"><span data-stu-id="60299-250">The suggested supply plan indicates that a total of four purchase orders will be created for the components.</span></span> <span data-ttu-id="60299-251">Du beslutter dig for at lave de foreslåede ordrer.</span><span class="sxs-lookup"><span data-stu-id="60299-251">You decide to make the proposed orders.</span></span>  

10. <span data-ttu-id="60299-252">Vælg handlingen **Lav ordrer**.</span><span class="sxs-lookup"><span data-stu-id="60299-252">Choose the **Make Orders** action.</span></span>  
11. <span data-ttu-id="60299-253">Vælg indstillinger **Alle linjer** og derefter knappen **OK** i feltet **Lav ordrer for**.</span><span class="sxs-lookup"><span data-stu-id="60299-253">In the **Make Orders for** field, select the **All Lines** option, and then choose the **OK** button.</span></span> <span data-ttu-id="60299-254">Kontroller, om der stadig findes et behov for produktionen af den overordnede vare, cyklen, der sælges på salgsordren 1001.</span><span class="sxs-lookup"><span data-stu-id="60299-254">Check if additional demand exists for the production of the parent item, the bicycle, which is being sold on sales order 1001.</span></span>  
12. <span data-ttu-id="60299-255">Vælg handlingen **Beregn plan**.</span><span class="sxs-lookup"><span data-stu-id="60299-255">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="60299-256">Meddelelsen angiver, at alle påkrævede varer nu er leveret.</span><span class="sxs-lookup"><span data-stu-id="60299-256">The message indicates that all required items are now supplied.</span></span> <span data-ttu-id="60299-257">Kontrollér de fastlagte produktionsordrer, der er oprettet.</span><span class="sxs-lookup"><span data-stu-id="60299-257">Verify the firm planned production orders that are created.</span></span>  

13. <span data-ttu-id="60299-258">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Fastlagt produktionsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="60299-258">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  

     <span data-ttu-id="60299-259">Se, hvordan start- og sluttiderne for de enkelte ordrer er planlagt i overensstemmelse med produktstrukturen på siden **Fastlagte prod.ordrer**.</span><span class="sxs-lookup"><span data-stu-id="60299-259">On the **Firm Planned Prod. Orders** page review how start times and end times of individual orders are scheduled according to the product structure.</span></span> <span data-ttu-id="60299-260">Komponenterne til de laveste niveauer i strukturen produceres først.</span><span class="sxs-lookup"><span data-stu-id="60299-260">The lowest-level components are produced first.</span></span> <span data-ttu-id="60299-261">Derfor skal du planlægge ordrer med flere niveauer som vist i denne planlægningsprocedure.</span><span class="sxs-lookup"><span data-stu-id="60299-261">Therefore, you must plan multilevel orders as demonstrated in this planning workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="60299-262">Se også</span><span class="sxs-lookup"><span data-stu-id="60299-262">See Also</span></span>  
 <span data-ttu-id="60299-263">[Gennemgang af forretningsproces](walkthrough-business-process-walkthroughs.md) </span><span class="sxs-lookup"><span data-stu-id="60299-263">[Business Process Walkthroughs](walkthrough-business-process-walkthroughs.md) </span></span>  
 [<span data-ttu-id="60299-264">Gennemgang: Automatisk planlægning af forsyninger</span><span class="sxs-lookup"><span data-stu-id="60299-264">Walkthrough: Planning Supplies Automatically</span></span>](walkthrough-planning-supplies-automatically.md)
