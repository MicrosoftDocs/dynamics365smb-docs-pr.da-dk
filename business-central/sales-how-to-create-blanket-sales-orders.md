---
title: "Sådan oprettes rammesalgsordrer | Microsoft Docs"
description: "Rammeordrer bruges typisk, når en kunde har indvilliget i at købe et stort antal varer, der skal leveres i flere mindre portioner i løbet af en bestemt periode."
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
ms.openlocfilehash: 8e0668e39891f6e0924afd8d9ec3ee39af95e587
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="work-with-blanket-sales-orders"></a><span data-ttu-id="f3eb2-103">Arbejde med rammesalgsordrer</span><span class="sxs-lookup"><span data-stu-id="f3eb2-103">Work with Blanket Sales Orders</span></span>
<span data-ttu-id="f3eb2-104">En rammesalgsordre udgør rammen om en langsigtet aftale mellem dig og en kunde.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-104">A blanket sales order represents a framework for a long-term agreement between you and your customer.</span></span>

<span data-ttu-id="f3eb2-105">Der indgås ofte en rammeaftale, hvor en kunde har forpligtet sig til at købe et stort antal varer, der skal leveres i flere mindre portioner i løbet af en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-105">A blanket order is typically made when a customer has committed to purchasing large quantities that are to be delivered in several smaller shipments over a certain period of time.</span></span> <span data-ttu-id="f3eb2-106">En rammeordre omfatter ofte kun en enkelt vare med leveringsdatoer, der er fastsat på forhånd.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-106">Often blanket orders cover only one item with predetermined delivery dates.</span></span> <span data-ttu-id="f3eb2-107">Den væsentligste årsag til at bruge en rammeordre i stedet for en salgsordre er, at de antal, der angives i en rammeordre, ikke påvirker varedisponeringen, og at oplysningerne dermed kan bruges til overvågnings-, prognose- og planlægningsformål.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-107">The main reason for using a blanket order rather than a sales order is that quantities entered on a blanket order do not affect item availability and thus can be used as a worksheet for monitoring, forecasting, and planning purposes.</span></span>

<span data-ttu-id="f3eb2-108">I rammeordren kan hver enkelt leverance oprettes som en ordrelinje, der derefter kan konverteres til en salgsordre på leveringstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-108">On the blanket order, each separate shipment can be set up as an order line, which can then be converted into a sales order at the time of shipping.</span></span>

<span data-ttu-id="f3eb2-109">Det kan f.eks. være relevant at bruge en rammesalgsordre, når en kunder ringer og bestiller 1000 enheder af en vare, som skal leveres i portioner på 250 enheder en gang om ugen i løbet af den næste måned.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-109">An example of when a blanket sales order could be used is if a customer calls and places an order of 1000 units of an item and they want the items to be delivered in 250 units every week over the next month.</span></span>

> [!NOTE]
> <span data-ttu-id="f3eb2-110">Rammekøbsordrer fungerer på samme måde som rammesalgsordrer.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-110">Blanket purchase orders work in a similar way as blanket sales orders.</span></span> <span data-ttu-id="f3eb2-111">Denne dokumentation dækker ikke rammekøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-111">This documentation does not cover blanket purchase orders.</span></span>

## <a name="to-create-a-blanket-sales-order"></a><span data-ttu-id="f3eb2-112">Sådan oprettes en rammesalgsordre.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-112">To create a blanket sales order</span></span>  
1. <span data-ttu-id="f3eb2-113">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rammesalgsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Blanket Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f3eb2-114">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-114">Choose the **New** action.</span></span>  
3. <span data-ttu-id="f3eb2-115">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  <span data-ttu-id="f3eb2-116">Lad feltet **Ordredato** være tomt.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-116">Leave the **Order Date** field blank.</span></span> <span data-ttu-id="f3eb2-117">Når de enkelte salgsordrer oprettes på basis af rammeordren, angives salgsordrens ordredato til den faktiske arbejdsdato.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-117">When the separate sales orders are created from the blanket order, the order date of the sales order is set to equal the actual work date.</span></span>
5. <span data-ttu-id="f3eb2-118">I oversigtspanelet **Linjer** skal du oprette separate linjer for hver enkelt leverance.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-118">On the **Lines** FastTab, create separate lines for each shipment.</span></span> <span data-ttu-id="f3eb2-119">Hvis kunden f.eks. skal have 1000 enheder fordelt jævnt over fire uger, kan du angive fire separate linjer på 250 enheder hver.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-119">For instance, if your customer wants 1000 units split out equally between four weeks, you would enter four separate lines of 250 units each.</span></span>   

## <a name="to-create-a-sales-order-from-a-blanket-sales-order"></a><span data-ttu-id="f3eb2-120">Sådan oprettes en salgsordre med udgangspunkt i en rammesalgsordre</span><span class="sxs-lookup"><span data-stu-id="f3eb2-120">To create a sales order from a blanket sales order</span></span>  

1.  <span data-ttu-id="f3eb2-121">Når du skal oprette en ordre til en af linjerne i rammemontageordren, skal du fjerne antallet i feltet **Lever (antal)** på alle de linjer, som IKKE skal leveres på nuværende tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-121">To create an order for any of the lines in the blanket assembly order, remove the quantity in the **Qty. to Ship** field on all the lines that you DO NOT wish to ship at this time.</span></span>  
2.  <span data-ttu-id="f3eb2-122">Når du er klar til at oprette ordrer, skal du vælge handlingen **Lav ordre** og derefter vælge **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-122">When you are ready to create orders, choose the **Make Order**m action, and then choose **Yes**.</span></span> <span data-ttu-id="f3eb2-123">Der vises en meddelelse med besked om, at rammeordren har fået tildelt et ordrenummer.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-123">A message appears informing you that the blanket order has been assigned an order number.</span></span> <span data-ttu-id="f3eb2-124">Bemærk, at rammeordren ikke er slettet.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-124">Note that the blanket order has not been deleted.</span></span>  
3.  <span data-ttu-id="f3eb2-125">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-125">Choose the **OK** button.</span></span>  
4.  <span data-ttu-id="f3eb2-126">Hvis du vil se resultatet af de foregående trin, skal du vælge handlingen **Linje**, vælge handlingen **Ikkebogførte linjer** og derefter vælge handlingen **Ordrer**.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-126">To see the results of the preceding steps, choose the **Line** action, choose the **Unposted Lines** action, and then choose the **Orders** action.</span></span>  
5.  <span data-ttu-id="f3eb2-127">Markér den relevante salgsordre i vinduet **Salgslinjer**, vælg handlingen **Linje** og derefter vælge handlingen **Vis dokument**.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-127">In the **Sales Lines** window, select the appropriate sales order, choose the **Line** action, and then choose the **Show Document** action.</span></span>  

<span data-ttu-id="f3eb2-128">Følgende gælder for salgsordrer, når de er oprettet ud fra rammesalgsordrer:</span><span class="sxs-lookup"><span data-stu-id="f3eb2-128">The following applies to sales orders after they have been created from blanket sales orders:</span></span>  

- <span data-ttu-id="f3eb2-129">Når rammeordren konverteres til en salgsordre, indeholder salgsordren samtlige linjer fra rammeordren.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-129">After the blanket order is converted into a sales order, the sales order contains all the lines from the blanket order.</span></span> <span data-ttu-id="f3eb2-130">Ordren omfatter også de linjer, hvor du slettede antallene i feltet **Lever (antal)**, men **Antal**-felterne er tomme.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-130">The lines where the quantity in the **Qty. to Ship** field was deleted appear, but with blank **Quantity** fields.</span></span> <span data-ttu-id="f3eb2-131">Du bestemmer selv, om du vil lade linjerne være, redigere dem eller slette dem.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-131">You may choose to leave, edit, or delete the lines.</span></span>  
- <span data-ttu-id="f3eb2-132">Det er vigtigt at huske, at antallet i salgsordren ikke må være større end antallet på den tilhørende rammeordrelinje.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-132">It is important to remember that the sales order line quantity must not exceed the quantity of the associated blanket order line.</span></span> <span data-ttu-id="f3eb2-133">Ellers kan salgsordren ikke bogføres.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-133">Otherwise, posting of the sales order will not be possible.</span></span>  
- <span data-ttu-id="f3eb2-134">Når salgsordren bogføres som leveret og/eller faktureret, opdateres felterne **Leveret (antal)** og **Faktureret (antal)** i den tilhørende rammeordre.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-134">When the sales order is posted as shipped and/or invoiced, the **Quantity Shipped** and **Quantity Invoiced** fields are updated on the related blanket order.</span></span>  
- <span data-ttu-id="f3eb2-135">Rammeordrenummeret og linjenummeret registreres som egenskaber for salgslinjerne, når de oprettes på basis af en rammeordre.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-135">The blanket order number and line number are recorded as properties of the sales lines when created from a blanket order.</span></span>  
- <span data-ttu-id="f3eb2-136">Hvis salgsordrerne ikke oprettes direkte fra rammeordren, men stadig har forbindelse til den, kan du oprette en forbindelse mellem en salgsordre og en rammeordre ved at angive det tilhørende rammeordrenummer i feltet **Rammeordrenr.**</span><span class="sxs-lookup"><span data-stu-id="f3eb2-136">When sales orders are not created directly from the blanket order but still relate to it, a link between a sales order and a blanket order can be established by entering the associated blanket order number in the **Blanket Order No.**</span></span> <span data-ttu-id="f3eb2-137">på salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-137">field on the sales order line.</span></span>  
- <span data-ttu-id="f3eb2-138">Når salgsordren er oprettet på hele antallet på en rammeordrelinje, kan en anden salgsordre ikke oprettes for den samme linje.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-138">After the sales order has been created for the total quantity of a blanket order line, no other sales order can be created for the same line.</span></span> <span data-ttu-id="f3eb2-139">Brugere kan ikke indtaste et antal i feltet **Lever antal**.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-139">Users are prevented from entering a quantity in the **Qty. to Ship** field.</span></span> <span data-ttu-id="f3eb2-140">Men hvis det er nødvendigt at føje flere enheder til en rammeordre, kan værdien i feltet **Antal** øges, hvorefter der kan oprettes flere ordrer.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-140">If, however, additional quantities need to be added to a blanket order, the value in the **Quantity** field can be increased and additional orders can then be created.</span></span>  
- <span data-ttu-id="f3eb2-141">Den fakturerede rammesalgsordre bliver liggende i systemet, indtil den slettes, enten ved sletning af bestemte rammesalgsordrer eller ved at køre kørslen **Slet fakturerede rammesalgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-141">The invoiced blanket sales order remains in the system until it is deleted, either by deleting individual blanket orders or by running the **Delete Invoiced Blanket Sales Orders** batch job.</span></span>  
- <span data-ttu-id="f3eb2-142">Hvis en kunde også er registreret som kontakt i modulet Marketing, og du har angivet en interaktionsskabelonkode for rammesalgsordrer i vinduet **Marketingopsætning**, registreres der en interaktion i tabellen Interaktionslogpost, når du vælger **Udskriv** for at udskrive rammesalgsordrerne.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-142">If a customer is also recorded as a contact in the Marketing application area, and if you have specified an interaction template code for blanket sales order in the **Marketing Setup** window, an interaction is recorded in the Interaction Log Entry table when you select **Print** to print the blanket sales order.</span></span>

## <a name="to-view-the-status-of-a-blanket-purchase-order"></a><span data-ttu-id="f3eb2-143">Sådan får du vist status på en rammekøbsordre</span><span class="sxs-lookup"><span data-stu-id="f3eb2-143">To view the status of a blanket purchase order</span></span>  
<span data-ttu-id="f3eb2-144">Du kan se den aktuelle status for en rammesalgsordre i vinduet **Købsordrestatistik**.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-144">You can see the status of a blanket sales order in the **Purchase Blanket Order Statistics** window.</span></span> <span data-ttu-id="f3eb2-145">Dette kan være relevant, når du begynder at fakturere den ordre, der er oprettet fra rammekøbsordren.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-145">This may be relevant when you start to invoice the order that is created from the blanket purchase order.</span></span>  

1.  <span data-ttu-id="f3eb2-146">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rammekøbsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-146">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Blanket Purchase Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f3eb2-147">Vælg en rammekøbsordre, og vælg derefter handlingen **Statistik**.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-147">Select a blanket purchase order, and then choose the **Statistics** action.</span></span>  
3.  <span data-ttu-id="f3eb2-148">I oversigtspanelet **Generelt** i vinduet **Rammekøbsordrestatistik** kan du se en oversigt med oplysninger om hele ordren baseret på den samlede mængde i felterne **Antal** på rammekøbsordrelinjerne.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-148">In the **Purchase Blanket Order Statistics** window, on the **General** FastTab, you can see summary information about the entire order based on the total quantity in the various **Quantity fields** on the blanket purchase order lines.</span></span>  

    - <span data-ttu-id="f3eb2-149">I oversigtspanelet **Fakturering** kan du se en oversigt med oplysninger om hele ordren baseret på den samlede mængde i felterne **Antal** på fakturarammeordrelinjerne.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-149">On the **Invoicing** FastTab, you can see summary information based on the total quantity in the **Qty. to Invoice** fields on the purchase blanket order lines.</span></span>  
    - <span data-ttu-id="f3eb2-150">I oversigtspanelet **Afsendelse** kan du se en oversigt med oplysninger baseret på den samlede mængde i felterne **Antal** der skal modtages på rammekøbsordrelinjerne.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-150">On the **Shipping** FastTab, you can see summary information based on the total quantity in the **Qty. to Receive** fields on the purchase blanket order lines.</span></span>  
    - <span data-ttu-id="f3eb2-151">I oversigtspanelet **Forudbetaling** kan du se en oversigt med oplysninger om alle forudbetalte beløb.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-151">On the **Prepayment** FastTab, you can see summary information about any prepaid amounts.</span></span>  
    - <span data-ttu-id="f3eb2-152">Oversigtspanelet **Kreditor** indeholder forskellige stamoplysninger om kreditoren.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-152">On the **Vendor** FastTab, you can see certain basic information about the vendor.</span></span>    

## <a name="to-view-unposted-and-posted-blanket-sales-order-lines"></a><span data-ttu-id="f3eb2-153">Sådan vises ikke-bogførte og bogførte rammesalgsordrelinjer</span><span class="sxs-lookup"><span data-stu-id="f3eb2-153">To view unposted and posted blanket sales order lines</span></span>   
<span data-ttu-id="f3eb2-154">Sammenkædningen mellem rammesalgsordre og den oprindelige salgsordre og ethvert andet salgsbilag bevares efter bogføring som en liste over bogførte og ikke-bogførte salgsordrefakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-154">The link between the blanket sales order and the originating sales order, and any other sales document, is retained after posting as a list of posted and unposted sales order invoice lines.</span></span>  

1. <span data-ttu-id="f3eb2-155">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rammesalgsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-155">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon enter **Blanket Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="f3eb2-156">Åbn den rammesalgsordre, du ønsker at se.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-156">Open the blanket sales order you want to view.</span></span>
3. <span data-ttu-id="f3eb2-157">Du kan få vist poster, der ikke er bogført, ved at vælge linjen, vælge handlingen **Linje** og derefter vælge handlingen **Ikkebogførte linjer**.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-157">To view unposted entries, select the line in question, choose the **Line** action, and then choose the **Unposted Lines** action.</span></span> <span data-ttu-id="f3eb2-158">Vælg en af følgende indstillinger.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-158">Choose one of the following options.</span></span>  

    <table>
    <tr>
    <th><span data-ttu-id="f3eb2-159">Indstilling</span><span class="sxs-lookup"><span data-stu-id="f3eb2-159">Option</span></span></th>
    <th><span data-ttu-id="f3eb2-160">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f3eb2-160">Description</span></span></th>
    </tr>
    <tr>
    <td><span data-ttu-id="f3eb2-161">**Ordrer**</span><span class="sxs-lookup"><span data-stu-id="f3eb2-161">**Orders**</span></span></td>
    <td><span data-ttu-id="f3eb2-162">Angiver åbne ordrer med tilknytning til den valgte linje.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-162">Specifies open orders associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="f3eb2-163">**Fakturaer**</span><span class="sxs-lookup"><span data-stu-id="f3eb2-163">**Invoices**</span></span></td>
    <td><span data-ttu-id="f3eb2-164">Angiver åbne fakturaer, der har været tilknyttet den valgte linje.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-164">Specifies open invoices that have been associated with the selected line.</span></span> <span data-ttu-id="f3eb2-165">Udestående fakturaer knyttes manuelt til en rammeordre, når du angiver rammeordrenummeret på salgsfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-165">Open invoices are manually associated with a blanket order by entering the blanket order number on the sales invoice line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="f3eb2-166">**Returvareordrer**</span><span class="sxs-lookup"><span data-stu-id="f3eb2-166">**Return Orders**</span></span></td>
    <td><span data-ttu-id="f3eb2-167">Angiver åbne returvareordrer, der har været tilknyttet den valgte linje.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-167">Specifies open return orders that have been associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="f3eb2-168">**Kreditnotaer**</span><span class="sxs-lookup"><span data-stu-id="f3eb2-168">**Credit Memos**</span></span></td>
    <td><span data-ttu-id="f3eb2-169">Angiver åbne kreditnotaer, der har været tilknyttet den valgte linje.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-169">Specifies open credit memos that have been associated with the selected line.</span></span></td>
    </tr>
    </table><span data-ttu-id="f3eb2-170">
4. Du kan få vist bogførte poster ved at vælge linjen, vælge handlingen *\*Linje** og derefter vælge handlingen *\*Bogførte linjer*\*.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-170">
4. To view posted entries, select the line in question, choose the *\*Line** action, and then choose the *\*Posted Lines** action.</span></span> <span data-ttu-id="f3eb2-171">Vælg en af følgende indstillinger.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-171">Choose one of the following options.</span></span>  

    <table>
    <tr>
    <th><span data-ttu-id="f3eb2-172">Indstilling</span><span class="sxs-lookup"><span data-stu-id="f3eb2-172">Option</span></span></th>
    <th><span data-ttu-id="f3eb2-173">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f3eb2-173">Description</span></span></th>
    </tr>
    <tr>
    <td><span data-ttu-id="f3eb2-174">**Leverancer**</span><span class="sxs-lookup"><span data-stu-id="f3eb2-174">**Shipments**</span></span></td>
    <td><span data-ttu-id="f3eb2-175">Bogførte leverancer med tilknytning til den valgte linje.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-175">Posted shipments associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="f3eb2-176">**Fakturaer**</span><span class="sxs-lookup"><span data-stu-id="f3eb2-176">**Invoices**</span></span></td>
    <td><span data-ttu-id="f3eb2-177">Bogførte fakturaer med tilknytning til den valgte linje.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-177">Posted invoices associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="f3eb2-178">**Returvaremodtagelse**</span><span class="sxs-lookup"><span data-stu-id="f3eb2-178">**Return Receipts**</span></span></td>
    <td><span data-ttu-id="f3eb2-179">Bogførte returvaremodtagelser med tilknytning til den valgte linje.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-179">Posted return receipts that have been associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="f3eb2-180">**Kreditnotaer**</span><span class="sxs-lookup"><span data-stu-id="f3eb2-180">**Credit Memos**</span></span></td>
    <td><span data-ttu-id="f3eb2-181">Bogførte kreditnotaer med tilknytning til den valgte linje.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-181">Posted credit memos that have been associated with the selected line.</span></span></td>
    </tr>
    </table><span data-ttu-id="f3eb2-182">
5. I vinduet *\*Salgslinjer** skal du vælge handlingen *\*Vis dokument** for at få vist posten.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-182">
5. In the *\*Sales Lines** window, choose the *\*Show Document** action to view the entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="f3eb2-183">Se også</span><span class="sxs-lookup"><span data-stu-id="f3eb2-183">See Also</span></span>
[<span data-ttu-id="f3eb2-184">Salg</span><span class="sxs-lookup"><span data-stu-id="f3eb2-184">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="f3eb2-185">Konfigurere salg</span><span class="sxs-lookup"><span data-stu-id="f3eb2-185">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="f3eb2-186">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f3eb2-186">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

