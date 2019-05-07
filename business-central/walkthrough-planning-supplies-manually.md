---
title: Gennemgang - Manuel planlægning af forsyninger | Microsoft Docs
description: Denne gennemgang viser processen med at planlægge forsyningsordrer til opfyldning af nye behov. Du kan starte forsyningsplanlægningen med faste intervaller, f.eks. hver morgen eller hver mandag, eller når du får besked om det af salg eller produktion, afhængigt af behovstypen.
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
ms.openlocfilehash: f8c20f51997ca2ec056423b9089b645e5a258235
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "925736"
---
# <a name="walkthrough-planning-supplies-manually"></a><span data-ttu-id="aa659-104">Gennemgang: Manuel planlægning af forsyninger</span><span class="sxs-lookup"><span data-stu-id="aa659-104">Walkthrough: Planning Supplies Manually</span></span>

<span data-ttu-id="aa659-105">**Bemærk**: Denne gennemgang skal udføres på et demoregnskab med indstillingen **Fuld evaluering - Komplette eksempeldata**, der findes i sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="aa659-105">**Note**: This walkthrough must be performed on a demonstration company with the **Full Evaluation - Complete Sample Data** option, which is available in the Sandbox environment.</span></span> <span data-ttu-id="aa659-106">Du kan finde flere oplysninger i [Oprette et sandkassemiljø](across-how-create-sandbox-environment.md).</span><span class="sxs-lookup"><span data-stu-id="aa659-106">For more information, see [Creating a Sandbox Environment](across-how-create-sandbox-environment.md).</span></span>

<span data-ttu-id="aa659-107">Denne gennemgang viser processen med at planlægge forsyningsordrer til opfyldning af nye behov.</span><span class="sxs-lookup"><span data-stu-id="aa659-107">This walkthrough demonstrates the process of planning supply orders to fulfill new demand.</span></span> <span data-ttu-id="aa659-108">Du kan starte forsyningsplanlægningen med faste intervaller, f.eks. hver morgen eller hver mandag, eller når du får besked om det af salg eller produktion, afhængigt af behovstypen.</span><span class="sxs-lookup"><span data-stu-id="aa659-108">You can initiate supply planning at fixed intervals, for example, every morning or every Monday, or when you are notified by sales or production, depending on the type of demand.</span></span> <span data-ttu-id="aa659-109">I denne gennemgang kommer du til at bruge siden **Ordreplanlægning**, der er et simpelt forsyningsplanlægningsværktøj, der er baseret på manuel beslutningstagning i stedet for en parameterbaseret automatisk planlægning.</span><span class="sxs-lookup"><span data-stu-id="aa659-109">In this walkthrough you will use the **Order Planning** page, a simple supply planning tool that is based on manual decision-making instead of parameter-based automatic planning.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="aa659-110">Om denne gennemgang</span><span class="sxs-lookup"><span data-stu-id="aa659-110">About This Walkthrough</span></span>  
 <span data-ttu-id="aa659-111">Denne gennemgang illustrerer følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="aa659-111">This walkthrough illustrates the following tasks:</span></span>  

-   <span data-ttu-id="aa659-112">Planlægning af en købsordre for produktionskomponenter.</span><span class="sxs-lookup"><span data-stu-id="aa659-112">Planning a purchase order for manufacturing components.</span></span>  
-   <span data-ttu-id="aa659-113">Planlægning af en overflytningsordre til opfyldning af et salgsbehov.</span><span class="sxs-lookup"><span data-stu-id="aa659-113">Planning a transfer order to fulfill sales demand.</span></span>  
-   <span data-ttu-id="aa659-114">Planlægning af en produktionsordre for en vare med flere niveauer.</span><span class="sxs-lookup"><span data-stu-id="aa659-114">Planning a production order for a multilevel item.</span></span>  

## <a name="roles"></a><span data-ttu-id="aa659-115">Roller</span><span class="sxs-lookup"><span data-stu-id="aa659-115">Roles</span></span>  
 <span data-ttu-id="aa659-116">Denne gennemgang viser de opgaver, der udføres af følgende brugerroller:</span><span class="sxs-lookup"><span data-stu-id="aa659-116">This walkthrough demonstrates tasks performed by the following user roles:</span></span>  

-   <span data-ttu-id="aa659-117">Produktionsplanlægger</span><span class="sxs-lookup"><span data-stu-id="aa659-117">Production Planner</span></span>  
-   <span data-ttu-id="aa659-118">Indkøbsagent</span><span class="sxs-lookup"><span data-stu-id="aa659-118">Purchasing Agent</span></span>  
-   <span data-ttu-id="aa659-119">Salgsordrebehandler</span><span class="sxs-lookup"><span data-stu-id="aa659-119">Sales Order Processor</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="aa659-120">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="aa659-120">Prerequisites</span></span>  
 <span data-ttu-id="aa659-121">Inden du begynder denne gennemgang, skal du installere [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="aa659-121">Before you begin this walkthrough, you must install the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="aa659-122">Der skal foretages følgende ændringer i databasen:</span><span class="sxs-lookup"><span data-stu-id="aa659-122">The following modifications must be made to the database:</span></span>  

-   <span data-ttu-id="aa659-123">Slet alle eksisterende salgsordrer på cykler.</span><span class="sxs-lookup"><span data-stu-id="aa659-123">Delete all existing sales orders for bicycles.</span></span>  
-   <span data-ttu-id="aa659-124">Opret én salgsordre på ti cykler på lokationen BLÅ.</span><span class="sxs-lookup"><span data-stu-id="aa659-124">Create one sales order for 10 bicycles at BLUE location.</span></span>  
-   <span data-ttu-id="aa659-125">Slet alle planlagte og fastlagte produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="aa659-125">Delete all planned and firm planned production orders.</span></span> <span data-ttu-id="aa659-126">Slet ikke startede ordrer med poster, der allerede er bogførte.</span><span class="sxs-lookup"><span data-stu-id="aa659-126">Do not delete started orders with entries that are already posted.</span></span>  

 <span data-ttu-id="aa659-127">Du skal som hovedregel bruge de foreslåede data i denne gennemgang, da disse data indeholder de nødvendige poster.</span><span class="sxs-lookup"><span data-stu-id="aa659-127">As a rule, use the suggested data in this walkthrough because this data has the necessary records.</span></span>  

## <a name="story"></a><span data-ttu-id="aa659-128">Historie</span><span class="sxs-lookup"><span data-stu-id="aa659-128">Story</span></span>  
 <span data-ttu-id="aa659-129">Erik, der er produktionsplanlægger i en mindre produktionsvirksomhed, er ved at planlægge produktions og købsordrer til opfyldning af nye salgsbehov.</span><span class="sxs-lookup"><span data-stu-id="aa659-129">Eduardo, the Production Planner of a small manufacturing company, is about to plan production and purchase orders to fulfill new sales demand.</span></span>  

 <span data-ttu-id="aa659-130">Da der er få styklisteniveauer i produkterne, og ordrestrømmen er relativ beskeden, anvender Erik siden **Ordreplanlægning** til manuelt at oprette forsyningsordrer – ét produktniveau ad gangen.</span><span class="sxs-lookup"><span data-stu-id="aa659-130">Because the products have few BOM levels and the flow of orders is relatively low, Eduardo uses the **Order Planning** page to manually create supply orders, one product level at a time.</span></span>  

 <span data-ttu-id="aa659-131">Ved mere komplekse produktionsmiljøer, bruges planlægningskladden til at planlægge forsyningen baseret på vareparametre, som f.eks. ændringsperiode, sikkerhedstid, genbestillingspunkt og batchberegninger af den samlede efterspørgsel fra alle produktniveauer.</span><span class="sxs-lookup"><span data-stu-id="aa659-131">In a more complex manufacturing environment, the planning worksheet is used to plan supply based on item parameters such as rescheduling period, safety lead time, reorder point, and batch calculations of consolidated demand from all product levels.</span></span>  

## <a name="setting-up-the-sample-data"></a><span data-ttu-id="aa659-132">Oprette eksempeldata</span><span class="sxs-lookup"><span data-stu-id="aa659-132">Setting Up the Sample Data</span></span>  
 <span data-ttu-id="aa659-133">Standarddemoregnskabet CRONUS har p.t. en stor mængde ikke-planlagte behov.</span><span class="sxs-lookup"><span data-stu-id="aa659-133">The standard CRONUS demonstration company currently has lots of unplanned demand.</span></span> <span data-ttu-id="aa659-134">Under de forskellige planlægningsopgaver i denne gennemgang vil du få brug for at afvige fra den realistiske forretningsgang ved at ignorere behov med tætte forfaldsdatoer og i stedet bruge behov med senere forfaldsdatoer.</span><span class="sxs-lookup"><span data-stu-id="aa659-134">During the different planning tasks in this walkthrough, you will have to deviate from the realistic business flow by ignoring demand with close due dates and instead use demand with later due dates.</span></span>  

## <a name="using-the-order-planning-page"></a><span data-ttu-id="aa659-135">Bruge siden Ordreplanlægning</span><span class="sxs-lookup"><span data-stu-id="aa659-135">Using the Order Planning Page</span></span>  

<!--
The **Order Planning** page can be accessed from several different locations on the **Departments** menu in the navigation pane:  

-   Manufacturing, Planning  
-   Sales & Marketing, Order Processing  
-   Purchase, Planning  
-   In addition, you can open this page for a specific production order by choosing **Planning** on the **Navigate** tab in the **Order** group.

-->  

### <a name="to-use-the-order-planning-page"></a><span data-ttu-id="aa659-136">Sådan bruges siden Ordreplanlægning</span><span class="sxs-lookup"><span data-stu-id="aa659-136">To use the Order Planning page</span></span>  

1.  <span data-ttu-id="aa659-137">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Ordreplanlægning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="aa659-137">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Order Planning**, and then choose the related link.</span></span>  

     <span data-ttu-id="aa659-138">Når siden **Ordreplanlægning** først åbnes, skal der beregnes en plan for at få vist det nye behov, siden det sidst blev beregnet.</span><span class="sxs-lookup"><span data-stu-id="aa659-138">When the **Order Planning** page first opens, a plan must be calculated to show the new demand since it was last calculated.</span></span>  

2.  <span data-ttu-id="aa659-139">Vælg handlingen **Beregn plan**.</span><span class="sxs-lookup"><span data-stu-id="aa659-139">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="aa659-140">Planlægningssystemet analyserer et eventuelt nyt behov, der er kommet til, som f.eks. nye salg, ændrede salg eller produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="aa659-140">The planning system analyzes any new demand that has been introduced, such as new sales, changed sales, or production orders.</span></span>  

     <span data-ttu-id="aa659-141">Det nødvendige antal for hvert behovslinje beregnes baseret på den samlede tilgængelighed.</span><span class="sxs-lookup"><span data-stu-id="aa659-141">Based on total availability, the quantity needed for each demand line is calculated.</span></span> <span data-ttu-id="aa659-142">Denne beregning udføres ordre-for-ordre.</span><span class="sxs-lookup"><span data-stu-id="aa659-142">This calculation is performed order-by-order.</span></span> <span data-ttu-id="aa659-143">Dette betyder, at den ordre, der indeholder behovslinjen med den tidligste forfaldsdato eller afsendelsesdato, beregnes først.</span><span class="sxs-lookup"><span data-stu-id="aa659-143">This means that the order which includes the demand line with the earliest due date or shipment date will be calculated first.</span></span> <span data-ttu-id="aa659-144">Derefter vil de andre behovslinjer blive beregnet i samme ordre, uanset forfaldsdato eller afsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="aa659-144">After that, additional demand lines will be calculated in the same order, regardless of the due date or shipment date.</span></span>  

3.  <span data-ttu-id="aa659-145">Sørg for, at siden **Ordreplanlægning** er maksimeret, og at kolonnefelterne er tilpasset, så de viser alle standardfeltnavnene.</span><span class="sxs-lookup"><span data-stu-id="aa659-145">Be sure that the **Order Planning** page is maximized and that column fields are resized to show all the default field names.</span></span>  

     <span data-ttu-id="aa659-146">Når beregningen er færdig, viser siden alle ikke-opfyldte behov som ikke-udvidede ordrehovedlinjer sorteret efter tidligste behovsdato.</span><span class="sxs-lookup"><span data-stu-id="aa659-146">When the calculation is completed, the page displays all unfulfilled demand as collapsed order header lines sorted by earliest demand date.</span></span>  

     <span data-ttu-id="aa659-147">Bemærk, at CRONUS har flere ordrer med ikke-opfyldte behov.</span><span class="sxs-lookup"><span data-stu-id="aa659-147">Notice that CRONUS has several orders with unfulfilled demand.</span></span> <span data-ttu-id="aa659-148">Hver planlægningslinje, der står med fed skrift, repræsenterer en ordre, salgsordre eller produktionsordre, inklusive mindst én ordrelinje med utilstrækkelig disponering.</span><span class="sxs-lookup"><span data-stu-id="aa659-148">Each bold planning line represents an order, sales order, or production order, including at least one order line with insufficient availability.</span></span>  

4.  <span data-ttu-id="aa659-149">Gå til feltet **Vis behov som**, og vælg filteret **Alle behov**.</span><span class="sxs-lookup"><span data-stu-id="aa659-149">In the **Show Demand As** field, select the **All Demand** filter.</span></span>  

     <span data-ttu-id="aa659-150">I feltet **Behovstype** kan du vælge, hvilke ordretyper der skal vises.</span><span class="sxs-lookup"><span data-stu-id="aa659-150">With the **Demand Type** field, you can choose which order types that you want to display.</span></span>  

     <span data-ttu-id="aa659-151">Ordrer, der ikke har disponeringsproblemer, vises ikke.</span><span class="sxs-lookup"><span data-stu-id="aa659-151">Orders that do not have availability problems are not shown.</span></span> <span data-ttu-id="aa659-152">Hvis der ikke findes nogle ordrer, når en plan beregnes, vil der blive vist en meddelelse, og der vil ikke blive vist nogen planlægningslinjer.</span><span class="sxs-lookup"><span data-stu-id="aa659-152">If no orders exist when a plan is calculated, a message will display and no planning lines will appear.</span></span>  

## <a name="planning-a-purchase-order-to-fulfill-component-demand"></a><span data-ttu-id="aa659-153">Planlægge en købsordre for at opfylde et komponentbehov</span><span class="sxs-lookup"><span data-stu-id="aa659-153">Planning a Purchase Order to Fulfill Component Demand</span></span>  
 <span data-ttu-id="aa659-154">I denne procedure opretter du en købsordre til manglende produktionskomponenter.</span><span class="sxs-lookup"><span data-stu-id="aa659-154">In this procedure, you create a purchase order for needed manufacturing components.</span></span>  

### <a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a><span data-ttu-id="aa659-155">Sådan planlægges en købsordre for at opfylde et komponentbehov i produktionen</span><span class="sxs-lookup"><span data-stu-id="aa659-155">To plan a purchase order to fulfill component need in production</span></span>  

1.  <span data-ttu-id="aa659-156">Udvid den første linje (vælg symbolet +).</span><span class="sxs-lookup"><span data-stu-id="aa659-156">Expand the first line (choose the + symbol).</span></span>  
2.  <span data-ttu-id="aa659-157">Vælg den første behovslinje med varen **LSU-15**, og vælg derefter handlingen **Vis dokument**.</span><span class="sxs-lookup"><span data-stu-id="aa659-157">Choose the first demand line, with item **LSU-15**, and then choose the **Show Document** action.</span></span>  
3.  <span data-ttu-id="aa659-158">Luk den åbnede produktionsordre for at vende tilbage til siden **Ordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="aa659-158">Close the opened production order to return to the **Order Planning** page.</span></span>  
4.  <span data-ttu-id="aa659-159">Gå til feltet **Genbestillingssystem**, og vælg **Køb**.</span><span class="sxs-lookup"><span data-stu-id="aa659-159">In the **Replenishment System** field, select **Purchase**.</span></span>  

     <span data-ttu-id="aa659-160">Standardværdien er fra vare- eller lagerkortet, men du kan ændre det til et af følgende muligheder:</span><span class="sxs-lookup"><span data-stu-id="aa659-160">The default value is from the item card, or SKU card, but you can change it to one of the following options:</span></span>  

    -   <span data-ttu-id="aa659-161">**Køb** – for at oprette en købsordre.</span><span class="sxs-lookup"><span data-stu-id="aa659-161">**Purchase** – To create a purchase order.</span></span>  
    -   <span data-ttu-id="aa659-162">**Overførsel** – for at oprette en overflytningsordre.</span><span class="sxs-lookup"><span data-stu-id="aa659-162">**Transfer** – To create a transfer order.</span></span>  
    -   <span data-ttu-id="aa659-163">**Produktionsordre** – for at oprette en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="aa659-163">**Prod. Order** – To create a production order.</span></span>  

5.  <span data-ttu-id="aa659-164">Vælg en af følgende indstillinger, der svarer til det valgte genbestillingssystem i feltet **Forsyning fra**:</span><span class="sxs-lookup"><span data-stu-id="aa659-164">In the **Supply From** field, select one of the following options according to the selected replenishment system:</span></span>  

    -   <span data-ttu-id="aa659-165">**Kreditor** – For køb</span><span class="sxs-lookup"><span data-stu-id="aa659-165">**Vendor** – For purchases</span></span>  
    -   <span data-ttu-id="aa659-166">**Lokation** – til overførsler</span><span class="sxs-lookup"><span data-stu-id="aa659-166">**Location** – For transfers</span></span>  

     <span data-ttu-id="aa659-167">Hvis feltet ikke er udfyldt, vises der en fejlmeddelelse, når du prøver at oprette forsyningsordren.</span><span class="sxs-lookup"><span data-stu-id="aa659-167">If the field is not filled in, an error message will display when you try to create the supply orders.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="aa659-168">Hvis der er oprettet et standardleverandørnummer på varekortene for komponenterne, vil linjerne være forudindstillet.</span><span class="sxs-lookup"><span data-stu-id="aa659-168">If the components have a default vendor number set up on the item cards, the lines will be preset.</span></span>  

6.  <span data-ttu-id="aa659-169">Markér feltet **Forsyning fra**.</span><span class="sxs-lookup"><span data-stu-id="aa659-169">Choose the **Supply From**  field.</span></span>  
7.  <span data-ttu-id="aa659-170">På siden **Vare/leverandører** skal du vælge handlingen **Ny** og derefter vælge leverandør **30000**.</span><span class="sxs-lookup"><span data-stu-id="aa659-170">On the **Item Vendor Catalogue** page, choose the **New** action, and then select vendor **30000**.</span></span>  
8.  <span data-ttu-id="aa659-171">Vælg knappen **OK** for at gå tilbage til siden **Ordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="aa659-171">Choose the **OK** button to return to the **Order Planning** page.</span></span>  
9. <span data-ttu-id="aa659-172">Kopier leverandør **30000** for til andre linjer for højttalerkomponenterne på denne produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="aa659-172">Copy vendor **30000** to the other lines for loudspeaker components on this production order.</span></span>  

     <span data-ttu-id="aa659-173">Du er nu klar til at oprette en købsordre.</span><span class="sxs-lookup"><span data-stu-id="aa659-173">You are now ready to create a purchase order.</span></span>  

10. <span data-ttu-id="aa659-174">Vælg handlingen **Lav ordrer**.</span><span class="sxs-lookup"><span data-stu-id="aa659-174">Choose the **Make Orders** action.</span></span> <span data-ttu-id="aa659-175">Siden **Opret forsyningsordrer** åbnes.</span><span class="sxs-lookup"><span data-stu-id="aa659-175">The **Make Supply Orders** page opens.</span></span>  
11. <span data-ttu-id="aa659-176">På oversigtspanelet **Ordreplanlægning**, i feltet **Lav ordrer for**, skal du vælge muligheden **Aktiv ordre**.</span><span class="sxs-lookup"><span data-stu-id="aa659-176">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **Active Order** option.</span></span>  
12. <span data-ttu-id="aa659-177">Gå til oversigtspanelet **indstillinger** og feltet **Opret købsordre**, og vælg indstillingen **Opret købsordrer**.</span><span class="sxs-lookup"><span data-stu-id="aa659-177">On the **Options** FastTab, in the **Create Purchase Order** field, choose the **Make Purch. Order** option.</span></span>  
13. <span data-ttu-id="aa659-178">Vælg **OK**-knappen for at oprette købsordrer for alle komponenterne i ordren.</span><span class="sxs-lookup"><span data-stu-id="aa659-178">Choose the **OK** button to create purchase orders for all the components of the order.</span></span>  

     <span data-ttu-id="aa659-179">Købsordrerne er nu oprettet og gemt som de sidste ordrer på listen over købsordrer.</span><span class="sxs-lookup"><span data-stu-id="aa659-179">The purchase orders are now created and saved as the last orders in the list of purchase orders.</span></span>  

## <a name="planning-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="aa659-180">Planlægge en overflytningsordre for at opfylde et salgsbehov</span><span class="sxs-lookup"><span data-stu-id="aa659-180">Planning a Transfer Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="aa659-181">I denne procedure kommer du til at planlægge ud fra et behov fra en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="aa659-181">In this procedure, you will plan for demand from a sales order.</span></span> <span data-ttu-id="aa659-182">Behovslinjerne repræsenterer salgslinjer og ikke komponentlinjer som ved produktionsbehov.</span><span class="sxs-lookup"><span data-stu-id="aa659-182">Demand lines represent sales lines and not component lines, as in production demand.</span></span>  

### <a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="aa659-183">Sådan planlægges en overflytningsordre til opfyldning af et salgsbehov.</span><span class="sxs-lookup"><span data-stu-id="aa659-183">To plan a transfer order to fulfill sales demand</span></span>  

1.  <span data-ttu-id="aa659-184">Flyt markøren til planlægningslinjen for ordre **2008**.</span><span class="sxs-lookup"><span data-stu-id="aa659-184">Move the pointer to the planning line for order **2008**.</span></span>  
2.  <span data-ttu-id="aa659-185">Udvid linjen, og flyt markøren til behovslinjen.</span><span class="sxs-lookup"><span data-stu-id="aa659-185">Expand the line and move the pointer to the demand line.</span></span>  

     <span data-ttu-id="aa659-186">Salgsordre **2008** er på ti højttalere, vare **LS-120**, der er bestilt af Lauritzen Kontormøbler A/S.</span><span class="sxs-lookup"><span data-stu-id="aa659-186">Sales order **2008** is for ten loudspeakers, item **LS-120**, ordered by John Haddock Insurance Co.</span></span>  

     <span data-ttu-id="aa659-187">Varens definerede genbestillingssystem og standardleverandør vises.</span><span class="sxs-lookup"><span data-stu-id="aa659-187">The item’s defined replenishment system and default vendor will display.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="aa659-188">Nederst på siden er der fire oplysningsfelter.</span><span class="sxs-lookup"><span data-stu-id="aa659-188">At the bottom of the page, there are four information fields.</span></span> <span data-ttu-id="aa659-189">I feltet **Tidligste disponible dato** vil de ti stykker, der er behov for, være til disposition på en indgående forsyningsordre ni dage senere end den aktuelle forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="aa659-189">In the **Earliest Date Available** field, the ten pieces that are needed will be available, on an inbound supply order, nine days later than the current due date.</span></span> <span data-ttu-id="aa659-190">Hvis dette er for sent for kunden, viser feltet **Disponibel til overflytning** 13 stykker af varen på en anden lokation.</span><span class="sxs-lookup"><span data-stu-id="aa659-190">If this is too late for the customer, the **Available for Transfer** field shows 13 pieces of the item at another location.</span></span> <span data-ttu-id="aa659-191">Du vil skulle planlægge denne lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="aa659-191">You will want to plan for this stock.</span></span>  

3.  <span data-ttu-id="aa659-192">Vælg feltet **Disponibel til overflytning** for at åbne siden **Hent alternativ forsyning**.</span><span class="sxs-lookup"><span data-stu-id="aa659-192">Choose the **Available for Transfer** field to open the **Get Alternative Supply** page.</span></span>  
4.  <span data-ttu-id="aa659-193">Vælg **OK**-knappen for at registrere de ti varer, der er til disposition.</span><span class="sxs-lookup"><span data-stu-id="aa659-193">Choose the **OK** button to book the ten items that are available.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="aa659-194">Det foreslåede køb i behovslinjen er erstattet med en overførsel fra lokationen GRØN.</span><span class="sxs-lookup"><span data-stu-id="aa659-194">In the demand line, the suggested purchase has been exchanged with a transfer from GREEN location.</span></span> <span data-ttu-id="aa659-195">Funktionen **Lav ordrer** opretter en overflytningsordre fra GRØN til den påkrævede lokation.</span><span class="sxs-lookup"><span data-stu-id="aa659-195">The **Make Orders** function creates a transfer order from GREEN to the demanded location.</span></span> <span data-ttu-id="aa659-196">Feltet **Erstatning findes** fungerer på samme måde.</span><span class="sxs-lookup"><span data-stu-id="aa659-196">The **Substitutes Exists** field works in the same way.</span></span>  

5.  <span data-ttu-id="aa659-197">Vælg handlingen **Lav ordrer**.</span><span class="sxs-lookup"><span data-stu-id="aa659-197">Choose the **Make Orders** action.</span></span> <span data-ttu-id="aa659-198">Siden **Opret forsyningsordrer** åbnes.</span><span class="sxs-lookup"><span data-stu-id="aa659-198">The **Make Supply Orders** page opens.</span></span>  
6.  <span data-ttu-id="aa659-199">På oversigtspanelet **Ordreplanlægning**, i feltet **Lav ordrer for**, skal du vælge muligheden **Den aktive ordre**.</span><span class="sxs-lookup"><span data-stu-id="aa659-199">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **The Active Order** option.</span></span>  
7.  <span data-ttu-id="aa659-200">Gå til oversigtspanelet **indstillinger** og feltet **Opret overflytningsordre**, og vælg indstillingen **Opret overførselsordrer**.</span><span class="sxs-lookup"><span data-stu-id="aa659-200">On the **Options** FastTab, in the **Create Transfer Order** field, select the **Make Trans. Orders** option.</span></span>  
8.  <span data-ttu-id="aa659-201">Vælg knappen **OK** for at oprette overførselsordren til forsyning af salgsordren.</span><span class="sxs-lookup"><span data-stu-id="aa659-201">Choose the **OK** button to create the transfer order to supply the sales order.</span></span>  

     <span data-ttu-id="aa659-202">Overførselsordren er nu oprettet og gemt som den sidste ordre på listen over åbne overførselsordrer.</span><span class="sxs-lookup"><span data-stu-id="aa659-202">The transfer order is now created and saved in the list as the last order in the list of open transfer orders.</span></span>  

## <a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a><span data-ttu-id="aa659-203">Planlægge en Produktionsordre med flere niveauer for at opfylde et salgsbehov</span><span class="sxs-lookup"><span data-stu-id="aa659-203">Planning a Multilevel Production Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="aa659-204">I denne procedure kommer du til at planlægge en opfyldning af et salgsbehov for en produceret vare med flere produktniveauer, der hver opretter afhængige produktionsbehov.</span><span class="sxs-lookup"><span data-stu-id="aa659-204">In this procedure, you will plan to fulfill sales demand for a produced item with multiple product levels, each creating dependent production demand.</span></span>  

### <a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a><span data-ttu-id="aa659-205">Sådan planlægges en produktion med flere niveauer for at opfylde et salgsbehov</span><span class="sxs-lookup"><span data-stu-id="aa659-205">To plan multilevel production to fulfill sales demand</span></span>  

1.  <span data-ttu-id="aa659-206">Vælg planlægningslinjen med salgsbehovet for ordre **1001**, oprettet tidligere som forudsætningsdata.</span><span class="sxs-lookup"><span data-stu-id="aa659-206">Select the planning line with sales demand for order **1001**, created earlier as prerequisite data.</span></span>  

     <span data-ttu-id="aa659-207">Behovet er en salgslinje, men varen har et defineret genbestillingssystem for **Prod.ordre**.</span><span class="sxs-lookup"><span data-stu-id="aa659-207">This demand is a sales line, but the item has a defined replenishment system of **Prod. Order**.</span></span> <span data-ttu-id="aa659-208">Fortsæt med at tilføje en ekstra ringeklokke til komponentbehovet for hver cykel.</span><span class="sxs-lookup"><span data-stu-id="aa659-208">Proceed to add an extra bell to the component need of each bicycle.</span></span>  

2.  <span data-ttu-id="aa659-209">Vælg handlingen **Komponenter** for at åbne siden **Planlægning - komponenter**.</span><span class="sxs-lookup"><span data-stu-id="aa659-209">Choose the **Components** action to open the **Planning Components** page.</span></span>  
3.  <span data-ttu-id="aa659-210">På linjen for Ringeklokke skal du ændre feltet **Antal pr.** fra **1** til **2**.</span><span class="sxs-lookup"><span data-stu-id="aa659-210">On the line with the Bell item, change the **Quantity per** field from **1** to **2**.</span></span>  
4.  <span data-ttu-id="aa659-211">Overvej dine planlægningsalternativer på siden **Ordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="aa659-211">On the **Order Planning** page, consider your planning alternatives.</span></span> <span data-ttu-id="aa659-212">I dette tilfælde har du ingen alternative forsyningsmuligheder, ingen overførsel, erstatning eller senere levering.</span><span class="sxs-lookup"><span data-stu-id="aa659-212">In this case, you have no alternative means of supply, no transfer, substitute, or later delivery.</span></span> <span data-ttu-id="aa659-213">Du skal oprette den foreslåede forsyningsordre, en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="aa659-213">You must create the suggested supply order, a production order.</span></span>  
5.  <span data-ttu-id="aa659-214">Vælg handlingen knappen **Lav ordrer** for at oprette produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="aa659-214">Choose the **Make Orders** action to create the production order.</span></span>  

     <span data-ttu-id="aa659-215">På siden **Ordreplanlægning** kan du se, at planlægningslinjen for salgsordre **1001** ikke længere findes, og at det første salgsbehov er dækket.</span><span class="sxs-lookup"><span data-stu-id="aa659-215">On the **Order Planning** page, notice that the planning line for sales order **1001** no longer exists and that the initial sales demand has been covered.</span></span>  

6.  <span data-ttu-id="aa659-216">Luk siden **Ordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="aa659-216">Close the **Order Planning** page.</span></span>  

     <span data-ttu-id="aa659-217">Nu kunne du vælge at blive i denne visning og færdiggøre planlægningsopgaverne.</span><span class="sxs-lookup"><span data-stu-id="aa659-217">Now, you could choose to stay in this view and complete all the planning tasks.</span></span> <span data-ttu-id="aa659-218">I stedet vil du dog nu antage rollen som produktionsplanlægger ved at gå til den produktionsordre, som du lige har oprettet, og åbne siden **Ordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="aa659-218">Instead, you will now take on the Production Planner role by going to the production order that you just created and access the **Order Planning** page.</span></span>  

 <span data-ttu-id="aa659-219">Som produktionsplanlægger skal du planlægge en specifik produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="aa659-219">As a production planner you now must plan a specific production order.</span></span>  

### <a name="to-plan-a-specific-production-order"></a><span data-ttu-id="aa659-220">Sådan planlægges en specifik produktionsordre</span><span class="sxs-lookup"><span data-stu-id="aa659-220">To plan a specific production order</span></span>  

1.  <span data-ttu-id="aa659-221">Åbn produktionsordren **101001**, på ti cykler, som du oprettede ved at bruge funktionen **Lav ordrer**.</span><span class="sxs-lookup"><span data-stu-id="aa659-221">Open the production order **101001**, for ten bicycles, that you just created by using the **Make Orders** function.</span></span>  
2.  <span data-ttu-id="aa659-222">Åbn siden **Prod.ordrekomponenter** for at kontrollere, at de ekstra ringeklokker afspejles på produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="aa659-222">Open the **Prod. Order Components** page to check that the extra bell is reflected on the production order.</span></span>  
3.  <span data-ttu-id="aa659-223">Vælg handlingen **Planlægning**.</span><span class="sxs-lookup"><span data-stu-id="aa659-223">Choose the **Planning** action.</span></span>  

     <span data-ttu-id="aa659-224">Siden **Ordreplanlægning** åbnes i en visning, der altid er filtreret ud fra det specifikke produktionsbehov.</span><span class="sxs-lookup"><span data-stu-id="aa659-224">The **Order Planning** page opens in a view that is always filtered on the specific production demand.</span></span> <span data-ttu-id="aa659-225">Salgsbehovet vises ikke.</span><span class="sxs-lookup"><span data-stu-id="aa659-225">Sales demand is not displayed.</span></span> <span data-ttu-id="aa659-226">Du skal beregne en plan, før du kan se et eventuelt ekstra behov.</span><span class="sxs-lookup"><span data-stu-id="aa659-226">You must calculate a plan before you can see any additional demand.</span></span>  

4.  <span data-ttu-id="aa659-227">Vælg handlingen **Beregn plan**.</span><span class="sxs-lookup"><span data-stu-id="aa659-227">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="aa659-228">Bemærk, at de nye produktionsordrer vises som ikke-planlagt produktionsbehov, der er afledt af ordren **101001**.</span><span class="sxs-lookup"><span data-stu-id="aa659-228">Notice that four new production orders appear as unplanned production demand derived from order **101001**.</span></span> <span data-ttu-id="aa659-229">De nye linjer repræsenterer et nyt produktionsbehov fra de underordnede samlinger, der skal oprettes for at producere ordren.</span><span class="sxs-lookup"><span data-stu-id="aa659-229">The new lines represent new production demand from the subassemblies that must be created to produce the order.</span></span>  

5.  <span data-ttu-id="aa659-230">Vælg handlingen **Udvid alle** for at få vist en oversigt over alle produktionsbehov for produktionsordrerne.</span><span class="sxs-lookup"><span data-stu-id="aa659-230">Choose the **Expand All** action to get an overview of all the production demand for the production orders.</span></span>  

     <span data-ttu-id="aa659-231">Hvis du vil angive yderligere oplysninger om behovslinjerne, kan du tilføjefelterne **Behovsmængde** og **Tilgængelig behovsmængde** til visningen.</span><span class="sxs-lookup"><span data-stu-id="aa659-231">To provide additional information about the demand lines, you may want to add the **Demand Quantity** and **Demand Qty. Available** fields to your view.</span></span>  

     <span data-ttu-id="aa659-232">Nu skal du levere ti af hver komponent.</span><span class="sxs-lookup"><span data-stu-id="aa659-232">Now you must supply ten of each component.</span></span>  

     <span data-ttu-id="aa659-233">Bemærk, at fire af behovslinjerne har angivet genbestillingssystemet Prod.ordre.</span><span class="sxs-lookup"><span data-stu-id="aa659-233">Note that four of the demand lines have replenishment system Prod. Order.</span></span> <span data-ttu-id="aa659-234">Disse fire halvfabrikata repræsenterer det andet produktniveau af cyklen.</span><span class="sxs-lookup"><span data-stu-id="aa659-234">These four subassemblies represent the second product level of the bicycle.</span></span>  

     <span data-ttu-id="aa659-235">Standardindstillingerne for genbestilling er allerede udfyldt, og du kan fortsætte til at lave ordrer.</span><span class="sxs-lookup"><span data-stu-id="aa659-235">The default replenishment settings are already filled in and you can proceed to make orders.</span></span>  

6.  <span data-ttu-id="aa659-236">Vælg handlingen **Lav ordrer**.</span><span class="sxs-lookup"><span data-stu-id="aa659-236">Choose the **Make Orders** action.</span></span>  

     <span data-ttu-id="aa659-237">Før du klikker på **OK**, skal du bemærke teksten i oversigtspanelet **Ordreplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="aa659-237">Before you choose the **OK** button, notice the text on the **Order Planning** FastTab.</span></span> <span data-ttu-id="aa659-238">Denne tekst er vigtig, fordi du ved, at cyklen har adskillige producerede komponenter, halvfabrikata, i produktstrukturen, som der kan være behov for, når du opretter denne produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="aa659-238">This text is important because you know that the bicycle has several produced components, subassemblies, in its product structure that might be in demand when you create this production order.</span></span>  

7.  <span data-ttu-id="aa659-239">Vælg indstillingen **Alle linjer**, og derefter knappen **OK** i feltet **Lav ordrer for** på siden **Opret forsyningsordre for** for at oprette produktionsordrer for det andet ordreproduktniveau.</span><span class="sxs-lookup"><span data-stu-id="aa659-239">On the **Make Supply Order** page, in the **Make Orders for** field, choose the **All Lines** option, and then choose the **OK** button to create production orders for the second product level of the order.</span></span>  

     <span data-ttu-id="aa659-240">Bemærk, at det øverste niveau i produktionsbehovet for produktionsordre 101001 ikke længere findes.</span><span class="sxs-lookup"><span data-stu-id="aa659-240">Note that the top-level production demand for production order 101001 no longer exists.</span></span> <span data-ttu-id="aa659-241">Dette betyder, at der er foretage planlægning for det første produktionsbehov for de underordnede samlinger.</span><span class="sxs-lookup"><span data-stu-id="aa659-241">This means that the initial production demand for subassemblies has been planned for.</span></span>  

     <span data-ttu-id="aa659-242">På siden **Ordreplanlægning** beregner du igen en plan for at planlægge cykelstrukturen.</span><span class="sxs-lookup"><span data-stu-id="aa659-242">On the **Order Planning** page, you calculate a plan again in order to plan the bicycle structure.</span></span>  

8.  <span data-ttu-id="aa659-243">Vælg handlingen **Beregn plan** for at genberegne planen som angivet i den integrerede hjælpetekst.</span><span class="sxs-lookup"><span data-stu-id="aa659-243">Choose the **Calculate Plan** action to recalculate the plan as instructed by the embedded Help text.</span></span>  

     <span data-ttu-id="aa659-244">De to nye linjer repræsenterer et yderligere produktionsbehov fra de underordnede samlinger, der er planlagt i de forrige trin.</span><span class="sxs-lookup"><span data-stu-id="aa659-244">The two new lines represent additional production demand derived from the subassemblies planned in the previous steps.</span></span> <span data-ttu-id="aa659-245">Det foreslås, at du opretter to produktionsordrer til forsyning af hjulnav, én til 10 nav fortil og én til 10 nav bagtil.</span><span class="sxs-lookup"><span data-stu-id="aa659-245">It is suggested that you make two production orders to supply the wheel hubs, one for 10 front hubs and one for 10 back hubs.</span></span>  

9. <span data-ttu-id="aa659-246">Vælg handlingen **Udvid alle** for at få vist en oversigt over alle behov for de to produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="aa659-246">Choose the **Expand All** action to get an overview of all the demand for the two production orders.</span></span>  

     <span data-ttu-id="aa659-247">Den foreslåede forsyningsplan indikerer, at der i alt oprettes fire købsordrer for komponenterne.</span><span class="sxs-lookup"><span data-stu-id="aa659-247">The suggested supply plan indicates that a total of four purchase orders will be created for the components.</span></span> <span data-ttu-id="aa659-248">Du beslutter dig for at lave de foreslåede ordrer.</span><span class="sxs-lookup"><span data-stu-id="aa659-248">You decide to make the proposed orders.</span></span>  

10. <span data-ttu-id="aa659-249">Vælg handlingen **Lav ordrer**.</span><span class="sxs-lookup"><span data-stu-id="aa659-249">Choose the **Make Orders** action.</span></span>  
11. <span data-ttu-id="aa659-250">Vælg indstillinger **Alle linjer** og derefter knappen **OK** i feltet **Lav ordrer for**.</span><span class="sxs-lookup"><span data-stu-id="aa659-250">In the **Make Orders for** field, select the **All Lines** option, and then choose the **OK** button.</span></span> <span data-ttu-id="aa659-251">Kontroller, om der stadig findes et behov for produktionen af den overordnede vare, cyklen, der sælges på salgsordren 1001.</span><span class="sxs-lookup"><span data-stu-id="aa659-251">Check if additional demand exists for the production of the parent item, the bicycle, which is being sold on sales order 1001.</span></span>  
12. <span data-ttu-id="aa659-252">Vælg handlingen **Beregn plan**.</span><span class="sxs-lookup"><span data-stu-id="aa659-252">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="aa659-253">Meddelelsen angiver, at alle påkrævede varer nu er leveret.</span><span class="sxs-lookup"><span data-stu-id="aa659-253">The message indicates that all required items are now supplied.</span></span> <span data-ttu-id="aa659-254">Kontrollér de fastlagte produktionsordrer, der er oprettet.</span><span class="sxs-lookup"><span data-stu-id="aa659-254">Verify the firm planned production orders that are created.</span></span>  

13. <span data-ttu-id="aa659-255">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Fastlagte prod.ordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="aa659-255">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  

     <span data-ttu-id="aa659-256">Se, hvordan start- og sluttiderne for de enkelte ordrer er planlagt i overensstemmelse med produktstrukturen på siden **Fastlagte prod.ordrer**.</span><span class="sxs-lookup"><span data-stu-id="aa659-256">On the **Firm Planned Prod. Orders** page review how start times and end times of individual orders are scheduled according to the product structure.</span></span> <span data-ttu-id="aa659-257">Komponenterne til de laveste niveauer i strukturen produceres først.</span><span class="sxs-lookup"><span data-stu-id="aa659-257">The lowest-level components are produced first.</span></span> <span data-ttu-id="aa659-258">Derfor skal du planlægge ordrer med flere niveauer som vist i denne planlægningsprocedure.</span><span class="sxs-lookup"><span data-stu-id="aa659-258">Therefore, you must plan multilevel orders as demonstrated in this planning workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="aa659-259">Se også</span><span class="sxs-lookup"><span data-stu-id="aa659-259">See Also</span></span>  
 <span data-ttu-id="aa659-260">[Gennemgang af forretningsproces](walkthrough-business-process-walkthroughs.md) </span><span class="sxs-lookup"><span data-stu-id="aa659-260">[Business Process Walkthroughs](walkthrough-business-process-walkthroughs.md) </span></span>  
 [<span data-ttu-id="aa659-261">Gennemgang: Automatisk planlægning af forsyninger</span><span class="sxs-lookup"><span data-stu-id="aa659-261">Walkthrough: Planning Supplies Automatically</span></span>](walkthrough-planning-supplies-automatically.md)
