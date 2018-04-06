---
title: "Gennemgang - Manuel planlægning af forsyninger | Microsoft Docs"
description: "Denne gennemgang viser processen med at planlægge forsyningsordrer til opfyldning af nye behov. Du kan starte forsyningsplanlægningen med faste intervaller, f.eks. hver morgen eller hver mandag, eller når du får besked om det af salg eller produktion, afhængigt af behovstypen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2992c2a9cbd2142e69cfb59294791ec31ce4dcb1
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="walkthrough-planning-supplies-manually"></a><span data-ttu-id="a2a2f-104">Gennemgang: Manuel planlægning af forsyninger</span><span class="sxs-lookup"><span data-stu-id="a2a2f-104">Walkthrough: Planning Supplies Manually</span></span>
<span data-ttu-id="a2a2f-105">Denne gennemgang viser processen med at planlægge forsyningsordrer til opfyldning af nye behov.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-105">This walkthrough demonstrates the process of planning supply orders to fulfill new demand.</span></span> <span data-ttu-id="a2a2f-106">Du kan starte forsyningsplanlægningen med faste intervaller, f.eks. hver morgen eller hver mandag, eller når du får besked om det af salg eller produktion, afhængigt af behovstypen.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-106">You can initiate supply planning at fixed intervals, for example, every morning or every Monday, or when you are notified by sales or production, depending on the type of demand.</span></span> <span data-ttu-id="a2a2f-107">I denne gennemgang kommer du til at bruge vinduet **Ordreplanlægning**, der er et simpelt forsyningsplanlægningsværktøj, der er baseret på manuel beslutningstagning i stedet for en parameterbaseret automatisk planlægning.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-107">In this walkthrough you will use the **Order Planning** window, a simple supply planning tool that is based on manual decision-making instead of parameter-based automatic planning.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="a2a2f-108">Om denne gennemgang</span><span class="sxs-lookup"><span data-stu-id="a2a2f-108">About This Walkthrough</span></span>  
 <span data-ttu-id="a2a2f-109">Denne gennemgang illustrerer følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="a2a2f-109">This walkthrough illustrates the following tasks:</span></span>  

-   <span data-ttu-id="a2a2f-110">Planlægning af en købsordre for produktionskomponenter.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-110">Planning a purchase order for manufacturing components.</span></span>  
-   <span data-ttu-id="a2a2f-111">Planlægning af en overflytningsordre til opfyldning af et salgsbehov.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-111">Planning a transfer order to fulfill sales demand.</span></span>  
-   <span data-ttu-id="a2a2f-112">Planlægning af en produktionsordre for en vare med flere niveauer.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-112">Planning a production order for a multilevel item.</span></span>  

## <a name="roles"></a><span data-ttu-id="a2a2f-113">Roller</span><span class="sxs-lookup"><span data-stu-id="a2a2f-113">Roles</span></span>  
 <span data-ttu-id="a2a2f-114">Denne gennemgang viser de opgaver, der udføres af følgende brugerroller:</span><span class="sxs-lookup"><span data-stu-id="a2a2f-114">This walkthrough demonstrates tasks performed by the following user roles:</span></span>  

-   <span data-ttu-id="a2a2f-115">Produktionsplanlægger</span><span class="sxs-lookup"><span data-stu-id="a2a2f-115">Production Planner</span></span>  
-   <span data-ttu-id="a2a2f-116">Indkøbsagent</span><span class="sxs-lookup"><span data-stu-id="a2a2f-116">Purchasing Agent</span></span>  
-   <span data-ttu-id="a2a2f-117">Salgsordrebehandler</span><span class="sxs-lookup"><span data-stu-id="a2a2f-117">Sales Order Processor</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="a2a2f-118">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="a2a2f-118">Prerequisites</span></span>  
 <span data-ttu-id="a2a2f-119">Inden du begynder denne gennemgang, skal du installere [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a2a2f-119">Before you begin this walkthrough, you must install the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="a2a2f-120">Der skal foretages følgende ændringer i databasen:</span><span class="sxs-lookup"><span data-stu-id="a2a2f-120">The following modifications must be made to the database:</span></span>  

-   <span data-ttu-id="a2a2f-121">Slet alle eksisterende salgsordrer på cykler.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-121">Delete all existing sales orders for bicycles.</span></span>  
-   <span data-ttu-id="a2a2f-122">Opret én salgsordre på ti cykler på lokationen BLÅ.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-122">Create one sales order for 10 bicycles at BLUE location.</span></span>  
-   <span data-ttu-id="a2a2f-123">Slet alle planlagte og fastlagte produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-123">Delete all planned and firm planned production orders.</span></span> <span data-ttu-id="a2a2f-124">Slet ikke startede ordrer med poster, der allerede er bogførte.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-124">Do not delete started orders with entries that are already posted.</span></span>  

 <span data-ttu-id="a2a2f-125">Du skal som hovedregel bruge de foreslåede data i denne gennemgang, da disse data indeholder de nødvendige poster.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-125">As a rule, use the suggested data in this walkthrough because this data has the necessary records.</span></span>  

## <a name="story"></a><span data-ttu-id="a2a2f-126">Historie</span><span class="sxs-lookup"><span data-stu-id="a2a2f-126">Story</span></span>  
 <span data-ttu-id="a2a2f-127">Erik, der er produktionsplanlægger i en mindre produktionsvirksomhed, er ved at planlægge produktions og købsordrer til opfyldning af nye salgsbehov.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-127">Eduardo, the Production Planner of a small manufacturing company, is about to plan production and purchase orders to fulfill new sales demand.</span></span>  

 <span data-ttu-id="a2a2f-128">Da der er få styklisteniveauer i produkterne, og ordrestrømmen er relativ beskeden, anvender Erik vinduet **Ordreplanlægning** til manuelt at oprette forsyningsordrer, ét produktniveau ad gangen.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-128">Because the products have few BOM levels and the flow of orders is relatively low, Eduardo uses the **Order Planning** window to manually create supply orders, one product level at a time.</span></span>  

 <span data-ttu-id="a2a2f-129">Ved mere komplekse produktionsmiljøer, bruges planlægningskladden til at planlægge forsyningen baseret på vareparametre, som f.eks. ændringsperiode, sikkerhedstid, genbestillingspunkt og batchberegninger af den samlede efterspørgsel fra alle produktniveauer.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-129">In a more complex manufacturing environment, the planning worksheet is used to plan supply based on item parameters such as rescheduling period, safety lead time, reorder point, and batch calculations of consolidated demand from all product levels.</span></span>  

## <a name="setting-up-the-sample-data"></a><span data-ttu-id="a2a2f-130">Oprette eksempeldata</span><span class="sxs-lookup"><span data-stu-id="a2a2f-130">Setting Up the Sample Data</span></span>  
 <span data-ttu-id="a2a2f-131">Standarddemonstrationsvirksomheden CRONUS har p.t. en stor mængde ikke-planlagte behov.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-131">The standard CRONUS demonstration company currently has lots of unplanned demand.</span></span> <span data-ttu-id="a2a2f-132">Under de forskellige planlægningsopgaver i denne gennemgang vil du få brug for at afvige fra den realistiske forretningsgang ved at ignorere behov med tætte forfaldsdatoer og i stedet bruge behov med senere forfaldsdatoer.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-132">During the different planning tasks in this walkthrough, you will have to deviate from the realistic business flow by ignoring demand with close due dates and instead use demand with later due dates.</span></span>  

## <a name="using-the-order-planning-window"></a><span data-ttu-id="a2a2f-133">Bruge vinduet Ordreplanlægning</span><span class="sxs-lookup"><span data-stu-id="a2a2f-133">Using the Order Planning Window</span></span>  

<!-- 
The **Order Planning** window can be accessed from several different locations on the **Departments** menu in the navigation pane:  

-   Manufacturing, Planning  
-   Sales & Marketing, Order Processing  
-   Purchase, Planning  
-   In addition, you can open this window for a specific production order by choosing **Planning** on the **Navigate** tab in the **Order** group.

-->  

### <a name="to-use-the-order-planning-window"></a><span data-ttu-id="a2a2f-134">Sådan bruges vinduet Ordreplanlægning</span><span class="sxs-lookup"><span data-stu-id="a2a2f-134">To use the Order Planning window</span></span>  

1.  <span data-ttu-id="a2a2f-135">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ordreplanlægning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Order Planning**, and then choose the related link.</span></span>  

     <span data-ttu-id="a2a2f-136">Når vinduet **Ordreplanlægning** først åbnes, skal der beregnes en plan for at få vist det nye behov, siden det sidst blev beregnet.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-136">When the **Order Planning** window first opens, a plan must be calculated to show the new demand since it was last calculated.</span></span>  

2.  <span data-ttu-id="a2a2f-137">Vælg handlingen **Beregn plan**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-137">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="a2a2f-138">Planlægningssystemet analyserer et eventuelt nyt behov, der er kommet til, som f.eks. nye salg, ændrede salg eller produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-138">The planning system analyzes any new demand that has been introduced, such as new sales, changed sales, or production orders.</span></span>  

     <span data-ttu-id="a2a2f-139">Det nødvendige antal for hvert behovslinje beregnes baseret på den samlede tilgængelighed.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-139">Based on total availability, the quantity needed for each demand line is calculated.</span></span> <span data-ttu-id="a2a2f-140">Denne beregning udføres ordre-for-ordre.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-140">This calculation is performed order-by-order.</span></span> <span data-ttu-id="a2a2f-141">Dette betyder, at den ordre, der indeholder behovslinjen med den tidligste forfaldsdato eller afsendelsesdato, beregnes først.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-141">This means that the order which includes the demand line with the earliest due date or shipment date will be calculated first.</span></span> <span data-ttu-id="a2a2f-142">Derefter vil de andre behovslinjer blive beregnet i samme ordre, uanset forfaldsdato eller afsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-142">After that, additional demand lines will be calculated in the same order, regardless of the due date or shipment date.</span></span>  

3.  <span data-ttu-id="a2a2f-143">Sørg for, at vinduet **Ordreplanlægning** er maksimeret, og at kolonnefelterne er tilpasset, så de viser alle standardfeltnavnene.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-143">Be sure that the **Order Planning** window is maximized and that column fields are resized to show all the default field names.</span></span>  

     <span data-ttu-id="a2a2f-144">Når beregningen er færdig, viser vinduet alle ikke-opfyldte behov som ikke-udvidede ordrehovedlinjer sorteret efter tidligste behovsdato.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-144">When the calculation is completed, the window displays all unfulfilled demand as collapsed order header lines sorted by earliest demand date.</span></span>  

     <span data-ttu-id="a2a2f-145">Bemærk, at CRONUS har flere ordrer med ikke-opfyldte behov.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-145">Notice that CRONUS has several orders with unfulfilled demand.</span></span> <span data-ttu-id="a2a2f-146">Hver planlægningslinje, der står med fed skrift, repræsenterer en ordre, salgsordre eller produktionsordre, inklusive mindst én ordrelinje med utilstrækkelig disponering.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-146">Each bold planning line represents an order, sales order, or production order, including at least one order line with insufficient availability.</span></span>  

4.  <span data-ttu-id="a2a2f-147">Gå til feltet **Vis behov som**, og vælg filteret **Alle behov**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-147">In the **Show Demand As** field, select the **All Demand** filter.</span></span>  

     <span data-ttu-id="a2a2f-148">I feltet **Behovstype** kan du vælge, hvilke ordretyper der skal vises.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-148">With the **Demand Type** field, you can choose which order types that you want to display.</span></span>  

     <span data-ttu-id="a2a2f-149">Ordrer, der ikke har disponeringsproblemer, vises ikke.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-149">Orders that do not have availability problems are not shown.</span></span> <span data-ttu-id="a2a2f-150">Hvis der ikke findes nogle ordrer, når en plan beregnes, vil der blive vist en meddelelse, og der vil ikke blive vist nogen planlægningslinjer.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-150">If no orders exist when a plan is calculated, a message will display and no planning lines will appear.</span></span>  

## <a name="planning-a-purchase-order-to-fulfill-component-demand"></a><span data-ttu-id="a2a2f-151">Planlægge en købsordre for at opfylde et komponentbehov</span><span class="sxs-lookup"><span data-stu-id="a2a2f-151">Planning a Purchase Order to Fulfill Component Demand</span></span>  
 <span data-ttu-id="a2a2f-152">I denne procedure opretter du en købsordre til manglende produktionskomponenter.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-152">In this procedure, you create a purchase order for needed manufacturing components.</span></span>  

### <a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a><span data-ttu-id="a2a2f-153">Sådan planlægges en købsordre for at opfylde et komponentbehov i produktionen</span><span class="sxs-lookup"><span data-stu-id="a2a2f-153">To plan a purchase order to fulfill component need in production</span></span>  

1.  <span data-ttu-id="a2a2f-154">Udvid den første linje (vælg symbolet +).</span><span class="sxs-lookup"><span data-stu-id="a2a2f-154">Expand the first line (choose the + symbol).</span></span>  
2.  <span data-ttu-id="a2a2f-155">Vælg den første behovslinje med varen **LSU-15**, og vælg derefter handlingen **Vis dokument**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-155">Choose the first demand line, with item **LSU-15**, and then choose the **Show Document** action.</span></span>  
3.  <span data-ttu-id="a2a2f-156">Luk den åbnede produktionsordre for at vende tilbage til vinduet **Ordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-156">Close the opened production order to return to the **Order Planning** window.</span></span>  
4.  <span data-ttu-id="a2a2f-157">Gå til feltet **Genbestillingssystem**, og vælg **Køb**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-157">In the **Replenishment System** field, select **Purchase**.</span></span>  

     <span data-ttu-id="a2a2f-158">Standardværdien er fra vare- eller lagerkortet, men du kan ændre det til et af følgende muligheder:</span><span class="sxs-lookup"><span data-stu-id="a2a2f-158">The default value is from the item card, or SKU card, but you can change it to one of the following options:</span></span>  

    -   <span data-ttu-id="a2a2f-159">**Køb** – for at oprette en købsordre.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-159">**Purchase** – To create a purchase order.</span></span>  
    -   <span data-ttu-id="a2a2f-160">**Overførsel** – for at oprette en overflytningsordre.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-160">**Transfer** – To create a transfer order.</span></span>  
    -   <span data-ttu-id="a2a2f-161">**Produktionsordre** – for at oprette en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-161">**Prod. Order** – To create a production order.</span></span>  

5.  <span data-ttu-id="a2a2f-162">Vælg en af følgende indstillinger, der svarer til det valgte genbestillingssystem i feltet **Forsyning fra**:</span><span class="sxs-lookup"><span data-stu-id="a2a2f-162">In the **Supply From** field, select one of the following options according to the selected replenishment system:</span></span>  

    -   <span data-ttu-id="a2a2f-163">**Kreditor** – For køb</span><span class="sxs-lookup"><span data-stu-id="a2a2f-163">**Vendor** – For purchases</span></span>  
    -   <span data-ttu-id="a2a2f-164">**Lokation** – til overførsler</span><span class="sxs-lookup"><span data-stu-id="a2a2f-164">**Location** – For transfers</span></span>  

     <span data-ttu-id="a2a2f-165">Hvis feltet ikke er udfyldt, vises der en fejlmeddelelse, når du prøver at oprette forsyningsordren.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-165">If the field is not filled in, an error message will display when you try to create the supply orders.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="a2a2f-166">Hvis der er oprettet et standardleverandørnummer på varekortene for komponenterne, vil linjerne være forudindstillet.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-166">If the components have a default vendor number set up on the item cards, the lines will be preset.</span></span>  

6.  <span data-ttu-id="a2a2f-167">Markér feltet **Forsyning fra**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-167">Choose the **Supply From**  field.</span></span>  
7.  <span data-ttu-id="a2a2f-168">I vinduet **Vare/leverandører** skal du vælge handlingen **Ny** og derefter vælge leverandør **30000**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-168">In the **Item Vendor Catalogue** window, choose the **New** action, and then select vendor **30000**.</span></span>  
8.  <span data-ttu-id="a2a2f-169">Vælg knappen **OK** for at gå tilbage til vinduet **Ordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-169">Choose the **OK** button to return to the **Order Planning** window.</span></span>  
9. <span data-ttu-id="a2a2f-170">Kopier leverandør **30000** for til andre linjer for højttalerkomponenterne på denne produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-170">Copy vendor **30000** to the other lines for loudspeaker components on this production order.</span></span>  

     <span data-ttu-id="a2a2f-171">Du er nu klar til at oprette en købsordre.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-171">You are now ready to create a purchase order.</span></span>  

10. <span data-ttu-id="a2a2f-172">Vælg handlingen **Lav ordrer**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-172">Choose the **Make Orders** action.</span></span> <span data-ttu-id="a2a2f-173">Vinduet **Opret forsyningsordrer** åbnes.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-173">The **Make Supply Orders** window opens.</span></span>  
11. <span data-ttu-id="a2a2f-174">På oversigtspanelet **Ordreplanlægning**, i feltet **Lav ordrer for**, skal du vælge muligheden **Aktiv ordre**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-174">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **Active Order** option.</span></span>  
12. <span data-ttu-id="a2a2f-175">Gå til oversigtspanelet **indstillinger** og feltet **Opret købsordre**, og vælg indstillingen **Opret købsordrer**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-175">On the **Options** FastTab, in the **Create Purchase Order** field, choose the **Make Purch. Order** option.</span></span>  
13. <span data-ttu-id="a2a2f-176">Vælg **OK**-knappen for at oprette købsordrer for alle komponenterne i ordren.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-176">Choose the **OK** button to create purchase orders for all the components of the order.</span></span>  

     <span data-ttu-id="a2a2f-177">Købsordrerne er nu oprettet og gemt som de sidste ordrer på listen over købsordrer.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-177">The purchase orders are now created and saved as the last orders in the list of purchase orders.</span></span>  

## <a name="planning-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="a2a2f-178">Planlægge en overflytningsordre for at opfylde et salgsbehov</span><span class="sxs-lookup"><span data-stu-id="a2a2f-178">Planning a Transfer Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="a2a2f-179">I denne procedure kommer du til at planlægge ud fra et behov fra en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-179">In this procedure, you will plan for demand from a sales order.</span></span> <span data-ttu-id="a2a2f-180">Behovslinjerne repræsenterer salgslinjer og ikke komponentlinjer som ved produktionsbehov.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-180">Demand lines represent sales lines and not component lines, as in production demand.</span></span>  

### <a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="a2a2f-181">Sådan planlægges en overflytningsordre til opfyldning af et salgsbehov.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-181">To plan a transfer order to fulfill sales demand</span></span>  

1.  <span data-ttu-id="a2a2f-182">Flyt markøren til planlægningslinjen for ordre **2008**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-182">Move the pointer to the planning line for order **2008**.</span></span>  
2.  <span data-ttu-id="a2a2f-183">Udvid linjen, og flyt markøren til behovslinjen.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-183">Expand the line and move the pointer to the demand line.</span></span>  

     <span data-ttu-id="a2a2f-184">Salgsordre **2008** er på ti højttalere, vare **LS-120**, der er bestilt af Lauritzen Kontormøbler A/S.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-184">Sales order **2008** is for ten loudspeakers, item **LS-120**, ordered by John Haddock Insurance Co.</span></span>  

     <span data-ttu-id="a2a2f-185">Varens definerede genbestillingssystem og standardleverandør vises.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-185">The item’s defined replenishment system and default vendor will display.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="a2a2f-186">Nederst i vinduet er der fire oplysningsfelter.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-186">At the bottom of the window, there are four information fields.</span></span> <span data-ttu-id="a2a2f-187">I feltet **Tidligste disponible dato** vil de ti stykker, der er behov for, være til disposition på en indgående forsyningsordre ni dage senere end den aktuelle forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-187">In the **Earliest Date Available** field, the ten pieces that are needed will be available, on an inbound supply order, nine days later than the current due date.</span></span> <span data-ttu-id="a2a2f-188">Hvis dette er for sent for kunden, viser feltet **Disponibel til overflytning** 13 stykker af varen på en anden lokation.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-188">If this is too late for the customer, the **Available for Transfer** field shows 13 pieces of the item at another location.</span></span> <span data-ttu-id="a2a2f-189">Du vil skulle planlægge denne lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-189">You will want to plan for this stock.</span></span>  

3.  <span data-ttu-id="a2a2f-190">Vælg feltet **Disponibel til overflytning** for at åbne vinduet **Hent alternativ forsyning**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-190">Choose the **Available for Transfer** field to open the **Get Alternative Supply** window.</span></span>  
4.  <span data-ttu-id="a2a2f-191">Vælg **OK**-knappen for at registrere de ti varer, der er til disposition.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-191">Choose the **OK** button to book the ten items that are available.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="a2a2f-192">Det foreslåede køb i behovslinjen er erstattet med en overførsel fra lokationen GRØN.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-192">In the demand line, the suggested purchase has been exchanged with a transfer from GREEN location.</span></span> <span data-ttu-id="a2a2f-193">Funktionen **Lav ordrer** opretter en overflytningsordre fra GRØN til den påkrævede lokation.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-193">The **Make Orders** function creates a transfer order from GREEN to the demanded location.</span></span> <span data-ttu-id="a2a2f-194">Feltet **Erstatning findes** fungerer på samme måde.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-194">The **Substitutes Exists** field works in the same way.</span></span>  

5.  <span data-ttu-id="a2a2f-195">Vælg handlingen **Lav ordrer**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-195">Choose the **Make Orders** action.</span></span> <span data-ttu-id="a2a2f-196">Vinduet **Opret forsyningsordrer** åbnes.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-196">The **Make Supply Orders** window opens.</span></span>  
6.  <span data-ttu-id="a2a2f-197">På oversigtspanelet **Ordreplanlægning**, i feltet **Lav ordrer for**, skal du vælge muligheden **Den aktive ordre**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-197">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **The Active Order** option.</span></span>  
7.  <span data-ttu-id="a2a2f-198">Gå til oversigtspanelet **indstillinger** og feltet **Opret overflytningsordre**, og vælg indstillingen **Opret overførselsordrer**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-198">On the **Options** FastTab, in the **Create Transfer Order** field, select the **Make Trans. Orders** option.</span></span>  
8.  <span data-ttu-id="a2a2f-199">Vælg knappen **OK** for at oprette overførselsordren til forsyning af salgsordren.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-199">Choose the **OK** button to create the transfer order to supply the sales order.</span></span>  

     <span data-ttu-id="a2a2f-200">Overførselsordren er nu oprettet og gemt som den sidste ordre på listen over åbne overførselsordrer.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-200">The transfer order is now created and saved in the list as the last order in the list of open transfer orders.</span></span>  

## <a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a><span data-ttu-id="a2a2f-201">Planlægge en Produktionsordre med flere niveauer for at opfylde et salgsbehov</span><span class="sxs-lookup"><span data-stu-id="a2a2f-201">Planning a Multilevel Production Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="a2a2f-202">I denne procedure kommer du til at planlægge en opfyldning af et salgsbehov for en produceret vare med flere produktniveauer, der hver opretter afhængige produktionsbehov.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-202">In this procedure, you will plan to fulfill sales demand for a produced item with multiple product levels, each creating dependent production demand.</span></span>  

### <a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a><span data-ttu-id="a2a2f-203">Sådan planlægges en produktion med flere niveauer for at opfylde et salgsbehov</span><span class="sxs-lookup"><span data-stu-id="a2a2f-203">To plan multilevel production to fulfill sales demand</span></span>  

1.  <span data-ttu-id="a2a2f-204">Vælg planlægningslinjen med salgsbehovet for ordre **1001**, oprettet tidligere som forudsætningsdata.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-204">Select the planning line with sales demand for order **1001**, created earlier as prerequisite data.</span></span>  

     <span data-ttu-id="a2a2f-205">Behovet er en salgslinje, men varen har et defineret genbestillingssystem for **Prod.ordre**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-205">This demand is a sales line, but the item has a defined replenishment system of **Prod. Order**.</span></span> <span data-ttu-id="a2a2f-206">Fortsæt med at tilføje en ekstra ringeklokke til komponentbehovet for hver cykel.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-206">Proceed to add an extra bell to the component need of each bicycle.</span></span>  

2.  <span data-ttu-id="a2a2f-207">Vælg handlingen **Komponenter** for at åbne vinduet **Planlægning - komponenter**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-207">Choose the **Components** action to open the **Planning Components** window.</span></span>  
3.  <span data-ttu-id="a2a2f-208">På linjen for Ringeklokke skal du ændre feltet **Antal pr.** fra **1** til **2**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-208">On the line with the Bell item, change the **Quantity per** field from **1** to **2**.</span></span>  
4.  <span data-ttu-id="a2a2f-209">Overvej dine planlægningsalternativer i vinduet **Ordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-209">In the **Order Planning** window, consider your planning alternatives.</span></span> <span data-ttu-id="a2a2f-210">I dette tilfælde har du ingen alternative forsyningsmuligheder, ingen overførsel, erstatning eller senere levering.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-210">In this case, you have no alternative means of supply, no transfer, substitute, or later delivery.</span></span> <span data-ttu-id="a2a2f-211">Du skal oprette den foreslåede forsyningsordre, en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-211">You must create the suggested supply order, a production order.</span></span>  
5.  <span data-ttu-id="a2a2f-212">Vælg handlingen knappen **Lav ordrer** for at oprette produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-212">Choose the **Make Orders** action to create the production order.</span></span>  

     <span data-ttu-id="a2a2f-213">I vinduet **Ordreplanlægning** kan du se, at planlægningslinjen for salgsordre **1001** ikke længere findes, og at det første salgsbehov er dækket.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-213">In the **Order Planning** window, notice that the planning line for sales order **1001** no longer exists and that the initial sales demand has been covered.</span></span>  

6.  <span data-ttu-id="a2a2f-214">Luk vinduet **Ordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-214">Close the **Order Planning** window.</span></span>  

     <span data-ttu-id="a2a2f-215">Nu kunne du vælge at blive i denne visning og færdiggøre planlægningsopgaverne.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-215">Now, you could choose to stay in this view and complete all the planning tasks.</span></span> <span data-ttu-id="a2a2f-216">I stedet vil du dog nu antage rollen som produktionsplanlægger ved at gå til den produktionsordre, som du lige har oprettet, og åbne vinduet **Ordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-216">Instead, you will now take on the Production Planner role by going to the production order that you just created and access the **Order Planning** window.</span></span>  

 <span data-ttu-id="a2a2f-217">Som produktionsplanlægger skal du planlægge en specifik produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-217">As a production planner you now must plan a specific production order.</span></span>  

### <a name="to-plan-a-specific-production-order"></a><span data-ttu-id="a2a2f-218">Sådan planlægges en specifik produktionsordre</span><span class="sxs-lookup"><span data-stu-id="a2a2f-218">To plan a specific production order</span></span>  

1.  <span data-ttu-id="a2a2f-219">Åbn produktionsordren **101001**, på ti cykler, som du oprettede ved at bruge funktionen **Lav ordrer**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-219">Open the production order **101001**, for ten bicycles, that you just created by using the **Make Orders** function.</span></span>  
2.  <span data-ttu-id="a2a2f-220">Åbn vinduet **Prod.ordrekomponenter** for at kontrollere, at de ekstra ringeklokker afspejles på produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-220">Open the **Prod. Order Components** window to check that the extra bell is reflected on the production order.</span></span>  
3.  <span data-ttu-id="a2a2f-221">Vælg handlingen **Planlægning**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-221">Choose the **Planning** action.</span></span>  

     <span data-ttu-id="a2a2f-222">Vinduet **Ordreplanlægning** åbnes i en visning, der altid er filtreret ud fra det specifikke produktionsbehov.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-222">The **Order Planning** window opens in a view that is always filtered on the specific production demand.</span></span> <span data-ttu-id="a2a2f-223">Salgsbehovet vises ikke.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-223">Sales demand is not displayed.</span></span> <span data-ttu-id="a2a2f-224">Du skal beregne en plan, før du kan se et eventuelt ekstra behov.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-224">You must calculate a plan before you can see any additional demand.</span></span>  

4.  <span data-ttu-id="a2a2f-225">Vælg handlingen **Beregn plan**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-225">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="a2a2f-226">Bemærk, at de nye produktionsordrer vises som ikke-planlagt produktionsbehov, der er afledt af ordren **101001**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-226">Notice that four new production orders appear as unplanned production demand derived from order **101001**.</span></span> <span data-ttu-id="a2a2f-227">De nye linjer repræsenterer et nyt produktionsbehov fra de underordnede samlinger, der skal oprettes for at producere ordren.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-227">The new lines represent new production demand from the subassemblies that must be created to produce the order.</span></span>  

5.  <span data-ttu-id="a2a2f-228">Vælg handlingen **Udvid alle** for at få vist en oversigt over alle produktionsbehov for produktionsordrerne.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-228">Choose the **Expand All** action to get an overview of all the production demand for the production orders.</span></span>  

     <span data-ttu-id="a2a2f-229">Hvis du vil angive yderligere oplysninger om behovslinjerne, kan du tilføjefelterne **Behovsmængde** og **Tilgængelig behovsmængde** til visningen.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-229">To provide additional information about the demand lines, you may want to add the **Demand Quantity** and **Demand Qty. Available** fields to your view.</span></span>  

     <span data-ttu-id="a2a2f-230">Nu skal du levere ti af hver komponent.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-230">Now you must supply ten of each component.</span></span>  

     <span data-ttu-id="a2a2f-231">Bemærk, at fire af behovslinjerne har angivet genbestillingssystemet Prod.ordre.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-231">Note that four of the demand lines have replenishment system Prod. Order.</span></span> <span data-ttu-id="a2a2f-232">Disse fire halvfabrikata repræsenterer det andet produktniveau af cyklen.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-232">These four subassemblies represent the second product level of the bicycle.</span></span>  

     <span data-ttu-id="a2a2f-233">Standardindstillingerne for genbestilling er allerede udfyldt, og du kan fortsætte til at lave ordrer.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-233">The default replenishment settings are already filled in and you can proceed to make orders.</span></span>  

6.  <span data-ttu-id="a2a2f-234">Vælg handlingen **Lav ordrer**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-234">Choose the **Make Orders** action.</span></span>  

     <span data-ttu-id="a2a2f-235">Før du klikker på **OK**, skal du bemærke teksten i oversigtspanelet **Ordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-235">Before you choose the **OK** button, notice the text on the **Order Planning** FastTab.</span></span> <span data-ttu-id="a2a2f-236">Denne tekst er vigtig, fordi du ved, at cyklen har adskillige producerede komponenter, halvfabrikata, i produktstrukturen, som der kan være behov for, når du opretter denne produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-236">This text is important because you know that the bicycle has several produced components, subassemblies, in its product structure that might be in demand when you create this production order.</span></span>  

7.  <span data-ttu-id="a2a2f-237">Vælg indstillingen **Alle linjer**, og derefter knappen **OK** i feltet **Lav ordrer for** i vinduet **Opret forsyningsordre for** for at oprette produktionsordrer for det andet ordreproduktniveau.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-237">In the **Make Supply Order** window, in the **Make Orders for** field, choose the **All Lines** option, and then choose the **OK** button to create production orders for the second product level of the order.</span></span>  

     <span data-ttu-id="a2a2f-238">Bemærk, at det øverste niveau i produktionsbehovet for produktionsordre 101001 ikke længere findes.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-238">Note that the top-level production demand for production order 101001 no longer exists.</span></span> <span data-ttu-id="a2a2f-239">Dette betyder, at der er foretage planlægning for det første produktionsbehov for de underordnede samlinger.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-239">This means that the initial production demand for subassemblies has been planned for.</span></span>  

     <span data-ttu-id="a2a2f-240">I vinduet **Ordreplanlægning** beregner du igen en plan for at planlægge cykelstrukturen.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-240">In the **Order Planning** window, you calculate a plan again in order to plan the bicycle structure.</span></span>  

8.  <span data-ttu-id="a2a2f-241">Vælg handlingen **Beregn plan** for at genberegne planen som angivet i den integrerede hjælpetekst.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-241">Choose the **Calculate Plan** action to recalculate the plan as instructed by the embedded Help text.</span></span>  

     <span data-ttu-id="a2a2f-242">De to nye linjer repræsenterer et yderligere produktionsbehov fra de underordnede samlinger, der er planlagt i de forrige trin.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-242">The two new lines represent additional production demand derived from the subassemblies planned in the previous steps.</span></span> <span data-ttu-id="a2a2f-243">Det foreslås, at du opretter to produktionsordrer til forsyning af hjulnav, én til 10 nav fortil og én til 10 nav bagtil.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-243">It is suggested that you make two production orders to supply the wheel hubs, one for 10 front hubs and one for 10 back hubs.</span></span>  

9. <span data-ttu-id="a2a2f-244">Vælg handlingen **Udvid alle** for at få vist en oversigt over alle behov for de to produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-244">Choose the **Expand All** action to get an overview of all the demand for the two production orders.</span></span>  

     <span data-ttu-id="a2a2f-245">Den foreslåede forsyningsplan indikerer, at der i alt oprettes fire købsordrer for komponenterne.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-245">The suggested supply plan indicates that a total of four purchase orders will be created for the components.</span></span> <span data-ttu-id="a2a2f-246">Du beslutter dig for at lave de foreslåede ordrer.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-246">You decide to make the proposed orders.</span></span>  

10. <span data-ttu-id="a2a2f-247">Vælg handlingen **Lav ordrer**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-247">Choose the **Make Orders** action.</span></span>  
11. <span data-ttu-id="a2a2f-248">Vælg indstillinger **Alle linjer** og derefter knappen **OK** i feltet **Lav ordrer for**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-248">In the **Make Orders for** field, select the **All Lines** option, and then choose the **OK** button.</span></span> <span data-ttu-id="a2a2f-249">Kontroller, om der stadig findes et behov for produktionen af den overordnede vare, cyklen, der sælges på salgsordren 1001.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-249">Check if additional demand exists for the production of the parent item, the bicycle, which is being sold on sales order 1001.</span></span>  
12. <span data-ttu-id="a2a2f-250">Vælg handlingen **Beregn plan**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-250">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="a2a2f-251">Meddelelsen angiver, at alle påkrævede varer nu er leveret.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-251">The message indicates that all required items are now supplied.</span></span> <span data-ttu-id="a2a2f-252">Kontrollér de fastlagte produktionsordrer, der er oprettet.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-252">Verify the firm planned production orders that are created.</span></span>  

13. <span data-ttu-id="a2a2f-253">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ordreplanlægning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-253">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  

     <span data-ttu-id="a2a2f-254">Se, hvordan start- og sluttiderne for de enkelte ordrer er planlagt i overensstemmelse med produktstrukturen i vinduet **Fastlagte prod.ordrer**.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-254">In the **Firm Planned Prod. Orders** window review how start times and end times of individual orders are scheduled according to the product structure.</span></span> <span data-ttu-id="a2a2f-255">Komponenterne til de laveste niveauer i strukturen produceres først.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-255">The lowest-level components are produced first.</span></span> <span data-ttu-id="a2a2f-256">Derfor skal du planlægge ordrer med flere niveauer som vist i denne planlægningsprocedure.</span><span class="sxs-lookup"><span data-stu-id="a2a2f-256">Therefore, you must plan multilevel orders as demonstrated in this planning workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a2a2f-257">Se også</span><span class="sxs-lookup"><span data-stu-id="a2a2f-257">See Also</span></span>  
 <span data-ttu-id="a2a2f-258">[Gennemgang af forretningsproces](walkthrough-business-process-walkthroughs.md) </span><span class="sxs-lookup"><span data-stu-id="a2a2f-258">[Business Process Walkthroughs](walkthrough-business-process-walkthroughs.md) </span></span>  
 [<span data-ttu-id="a2a2f-259">Gennemgang: Automatisk planlægning af forsyninger</span><span class="sxs-lookup"><span data-stu-id="a2a2f-259">Walkthrough: Planning Supplies Automatically</span></span>](walkthrough-planning-supplies-automatically.md)

