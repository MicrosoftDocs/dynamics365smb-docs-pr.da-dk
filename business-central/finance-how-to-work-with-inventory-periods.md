---
title: "Sådan arbejder du med lagerperioder | Microsoft Docs"
description: "Du kan styre den tidsramme, hvor brugere kan bogføre ændringer af lageret ved at definere lagerperioder."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: inventory, periods
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d302483ca2d66870670aaa0914533472a807d04f
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-inventory-periods"></a><span data-ttu-id="2e65e-103">Arbejde med lagerperioder</span><span class="sxs-lookup"><span data-stu-id="2e65e-103">Work with Inventory Periods</span></span>
<span data-ttu-id="2e65e-104">Lagerperioder definerer en tidsperiode, hvor du kan bogføre ændringer i lageret.</span><span class="sxs-lookup"><span data-stu-id="2e65e-104">Inventory periods define a period of time in which you can post changes to inventory.</span></span> <span data-ttu-id="2e65e-105">En lagerperiode er defineret af periodens slutdato.</span><span class="sxs-lookup"><span data-stu-id="2e65e-105">An inventory period is defined by the date on which it ends, or the ending date.</span></span> <span data-ttu-id="2e65e-106">Når du lukker en lagerperiode kan du ikke bogføre ændringer af lageret, hverken forventede eller fakturerede, før denne slutdato.</span><span class="sxs-lookup"><span data-stu-id="2e65e-106">When you close an inventory period, you cannot post any changes to inventory, either expected or invoiced, before this ending date.</span></span> <span data-ttu-id="2e65e-107">Desuden kan du ikke bogføre nye værdier til lageret før denne slutdato.</span><span class="sxs-lookup"><span data-stu-id="2e65e-107">You cannot post any new values to inventory before the ending date.</span></span> <span data-ttu-id="2e65e-108">Hvis der er åbne poster i den lukkede periode, dvs. positive antal, der endnu ikke er blevet udlignet med udgående transaktioner, kan du stadig udligne udgående antal med disse poster, selvom perioden er lukket.</span><span class="sxs-lookup"><span data-stu-id="2e65e-108">If you have open item entries in the closed period, meaning positive quantities that have not yet been applied to outbound transactions, you can still apply outbound quantities to these entries, even if the period is closed.</span></span>  

<span data-ttu-id="2e65e-109">Følgende afsnit beskriver, hvordan du kan:</span><span class="sxs-lookup"><span data-stu-id="2e65e-109">The following sections describe how to:</span></span>  

* <span data-ttu-id="2e65e-110">Opret lagerperioder.</span><span class="sxs-lookup"><span data-stu-id="2e65e-110">Create inventory periods.</span></span>  
* <span data-ttu-id="2e65e-111">Luk lagerperioder.</span><span class="sxs-lookup"><span data-stu-id="2e65e-111">Close inventory periods.</span></span>  
* <span data-ttu-id="2e65e-112">Genåbn lagerperioder.</span><span class="sxs-lookup"><span data-stu-id="2e65e-112">Reopen inventory periods.</span></span>  

## <a name="to-create-an-inventory-period"></a><span data-ttu-id="2e65e-113">Sådan oprettes en lagerperiode</span><span class="sxs-lookup"><span data-stu-id="2e65e-113">To create an inventory period</span></span>  
1. <span data-ttu-id="2e65e-114">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lagerperioder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="2e65e-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Inventory Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2e65e-115">Opret en ny linje.</span><span class="sxs-lookup"><span data-stu-id="2e65e-115">Create a new line.</span></span>  
3. <span data-ttu-id="2e65e-116">I feltet **Slutdato** skal du angive den sidste dato i den lagerperiode, du vil oprette.</span><span class="sxs-lookup"><span data-stu-id="2e65e-116">In the **Ending Date** field, enter the last date in the inventory period that you want to define.</span></span> <span data-ttu-id="2e65e-117">Når perioden lukkes, vil du ikke kunne bogføre ændringer til lagerbeholdningen før denne dato.</span><span class="sxs-lookup"><span data-stu-id="2e65e-117">When the period is closed, you will not be able to post inventory changes before this date.</span></span>  
4. <span data-ttu-id="2e65e-118">Indtast et beskrivende navn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="2e65e-118">Enter a descriptive name in the **Name** field.</span></span> <span data-ttu-id="2e65e-119">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e65e-119">Choose the **OK** button.</span></span>  

## <a name="closing-inventory-periods"></a><span data-ttu-id="2e65e-120">Lukke lagerperioder</span><span class="sxs-lookup"><span data-stu-id="2e65e-120">Closing Inventory Periods</span></span>  
<span data-ttu-id="2e65e-121">Feltet **Lukket** angiver, om lagerperioden er lukket eller ej for ændringer af lagerbeholdningsværdien.</span><span class="sxs-lookup"><span data-stu-id="2e65e-121">The **Closed** field indicates whether or not the inventory period is closed to inventory value changes.</span></span> <span data-ttu-id="2e65e-122">Du kan ikke redigere feltet.</span><span class="sxs-lookup"><span data-stu-id="2e65e-122">You cannot edit this field.</span></span>  

<span data-ttu-id="2e65e-123">Du kan lukke alle lagerperioder, hvis følgende gør sig gældende:</span><span class="sxs-lookup"><span data-stu-id="2e65e-123">You can close any inventory period, provided that the following is true:</span></span>  

* <span data-ttu-id="2e65e-124">Der er ingen åbne udgående vareposter, dvs. negativ lagerbeholdning, i perioden.</span><span class="sxs-lookup"><span data-stu-id="2e65e-124">There are no open outbound item ledger entries, meaning negative inventory, in that period.</span></span>  
* <span data-ttu-id="2e65e-125">Kostprisen for alle varer er blevet reguleret med kørslen **Reguler kostværdi - vareposter**.</span><span class="sxs-lookup"><span data-stu-id="2e65e-125">The cost of all items has been adjusted using the **Adjust Cost – Item Entries** batch job.</span></span>  

<span data-ttu-id="2e65e-126">Det betyder, at alle udgående transaktionsantal, f.eks. dem fra salgsordrer, udgående overflytninger, salgsfakturaer, købsreturvarer eller købskreditnotaer, skal være anvendt på eksisterende antal i lagerbeholdningen.</span><span class="sxs-lookup"><span data-stu-id="2e65e-126">This means that all outbound transaction quantities, such as those from sales orders, outbound transfers, sales invoices, purchase returns, or purchase credit memos, must be applied to existing quantity in inventory.</span></span>  

### <a name="to-close-an-inventory-period"></a><span data-ttu-id="2e65e-127">Sådan lukkes en lagerperiode</span><span class="sxs-lookup"><span data-stu-id="2e65e-127">To close an inventory period</span></span>  
1. <span data-ttu-id="2e65e-128">Før du lukker en lagerperiode, skal du udføre kørslen **Juster kostværdi – vareposter** for at sikre, at alle kostprisreguleringer er bogført.</span><span class="sxs-lookup"><span data-stu-id="2e65e-128">Before closing an inventory period, run the **Adjust Cost – Item Entries** batch job to ensure that all cost adjustments are posted.</span></span> <span data-ttu-id="2e65e-129">På fanen **Handlinger** i gruppen **Funktioner** vælges **Juster kostpris - vareposter**.</span><span class="sxs-lookup"><span data-stu-id="2e65e-129">On the **Actions** tab, in the **Functions** group, choose **Adjust Cost – Item Entries**.</span></span>  

     <span data-ttu-id="2e65e-130">Udfør rapporten **Luk lagerperiode - kontrol** for at kontrollere, om der er nogen udgående vareposter i lagerperioden eller nogen varer, hvor kostprisen endnu ikke er blevet reguleret.</span><span class="sxs-lookup"><span data-stu-id="2e65e-130">Run the **Close Inventory Period – Test** report to determine if there are any open outbound item entries within the inventory period or any items whose cost has not yet been adjusted.</span></span>  
2. <span data-ttu-id="2e65e-131">Vælg handlingen **Luk lagerperiode – kontrol**.</span><span class="sxs-lookup"><span data-stu-id="2e65e-131">Choose the **Close Inventory Period – Test** action.</span></span>  

     <span data-ttu-id="2e65e-132">Udfør kørslen **Bogfør lagerregulering** for at sikre, at alle kostpriser er bogført i Finans.</span><span class="sxs-lookup"><span data-stu-id="2e65e-132">Run the **Post Inventory Cost to G/L** batch job to ensure that all costs are posted to the general ledger.</span></span>  
3. <span data-ttu-id="2e65e-133">Vælg handlingen **Bogfør lagerbeholdning**.</span><span class="sxs-lookup"><span data-stu-id="2e65e-133">Choose the **Post Inventory to G/L** action.</span></span>  
4. <span data-ttu-id="2e65e-134">I vinduet **Lagerperioder** skal du vælge den lagerperiode, du vil lukke.</span><span class="sxs-lookup"><span data-stu-id="2e65e-134">In the **Inventory Periods** window, select the inventory period you want to close.</span></span>  
5. <span data-ttu-id="2e65e-135">Vælg handlingen **Luk periode**.</span><span class="sxs-lookup"><span data-stu-id="2e65e-135">Choose the **Close Period** action.</span></span> <span data-ttu-id="2e65e-136">Når lagerperioden er blevet lukket, kan du ikke bogføre ændringer til lagerbeholdningen før slutdatoen.</span><span class="sxs-lookup"><span data-stu-id="2e65e-136">After the inventory period has been closed, you cannot post inventory changes before the ending date.</span></span> <span data-ttu-id="2e65e-137">Kostprisen på alle varer skal reguleres med kørslen **Reguler kostværdi - vareposter**, før du kan lukke lagerperioden.</span><span class="sxs-lookup"><span data-stu-id="2e65e-137">The cost of all items must be adjusted with the **Adjust Cost – Item Entries** batch job before you close the inventory period.</span></span>  
6. <span data-ttu-id="2e65e-138">Klik på **Ja** for at bekræfte, at du vil lukke perioden, eller klik på **Nej** for at annullere lukningen.</span><span class="sxs-lookup"><span data-stu-id="2e65e-138">Choose the **Yes** button to confirm that you want to close the period, or choose **No** to cancel the closing.</span></span>  
7. <span data-ttu-id="2e65e-139">Lagerperioden lukkes, og der vises en meddelelse, når det er udført.</span><span class="sxs-lookup"><span data-stu-id="2e65e-139">The inventory period is closed and a confirmation message is displayed when it is finished.</span></span>  

## <a name="reopening-inventory-periods"></a><span data-ttu-id="2e65e-140">Genåbne lagerperioder</span><span class="sxs-lookup"><span data-stu-id="2e65e-140">Reopening Inventory Periods</span></span>  
<span data-ttu-id="2e65e-141">Når du har lukket lagerperioden, kan du ikke slette den.</span><span class="sxs-lookup"><span data-stu-id="2e65e-141">After you have closed the inventory period, you cannot delete the inventory period.</span></span> <span data-ttu-id="2e65e-142">Du kan dog genåbne den, hvis du vil tillade bogføring før lagerperiodens slutdato.</span><span class="sxs-lookup"><span data-stu-id="2e65e-142">You can, however, reopen it, if you would like to allow posting before the ending date of the inventory period.</span></span> <span data-ttu-id="2e65e-143">Hvis du genåbner en periode, genåbnes også alle de lagerperioder med slutdatoer, som er efter den periode, du genåbnede.</span><span class="sxs-lookup"><span data-stu-id="2e65e-143">Reopening a period also reopens all inventory periods with ending dates later than the period you reopen.</span></span>  

### <a name="to-reopen-an-inventory-period"></a><span data-ttu-id="2e65e-144">Sådan genåbnes en lagerperiode</span><span class="sxs-lookup"><span data-stu-id="2e65e-144">To reopen an inventory period</span></span>  
1. <span data-ttu-id="2e65e-145">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lagerperioder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="2e65e-145">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Inventory Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2e65e-146">Vælg den lagerperiode, du vil åbne igen.</span><span class="sxs-lookup"><span data-stu-id="2e65e-146">Select the inventory period you want to reopen.</span></span>  
3. <span data-ttu-id="2e65e-147">Vælg handlingen **Åbn periode igen**.</span><span class="sxs-lookup"><span data-stu-id="2e65e-147">Choose the **Reopen Period** period action.</span></span> <span data-ttu-id="2e65e-148">Bekræft, at du vil genåbne perioden.</span><span class="sxs-lookup"><span data-stu-id="2e65e-148">Confirm that you want to reopen the period.</span></span>  
4. <span data-ttu-id="2e65e-149">Alle lagerperioder med slutdatoer efter den periode, du valgte, genåbnes.</span><span class="sxs-lookup"><span data-stu-id="2e65e-149">All inventory periods with ending dates later than the period you selected are reopened.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2e65e-150">Se også</span><span class="sxs-lookup"><span data-stu-id="2e65e-150">See Also</span></span>  
[<span data-ttu-id="2e65e-151">Designoplysninger: Lagerperioder</span><span class="sxs-lookup"><span data-stu-id="2e65e-151">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="2e65e-152">Finans</span><span class="sxs-lookup"><span data-stu-id="2e65e-152">Finance</span></span>](finance.md)  
[<span data-ttu-id="2e65e-153">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="2e65e-153">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="2e65e-154">Arbejde med Financials</span><span class="sxs-lookup"><span data-stu-id="2e65e-154">Working with Financials</span></span>](ui-work-product.md)

