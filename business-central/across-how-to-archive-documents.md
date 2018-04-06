---
title: "Sådan arkiveres salgs- og købsdokumenter | Microsoft Docs"
description: "Du kan arkivere salgs- og købsdokumenter, ordrer, tilbud, returvareordrer og rammeordrer, og du kan bruge det arkiverede dokument til at genskabe det dokument, som det blev arkiveret fra."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 74460bfcff36d293006229f4a89719f8c05c2631
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="archive-documents"></a><span data-ttu-id="f2402-103">Arkivere dokumenter</span><span class="sxs-lookup"><span data-stu-id="f2402-103">Archive Documents</span></span>
<span data-ttu-id="f2402-104">Du kan arkivere salgs- og købsdokumenter, ordrer, tilbud, returvareordrer og rammeordrer, og du kan bruge det arkiverede dokument til at genskabe det dokument, som det blev arkiveret fra.</span><span class="sxs-lookup"><span data-stu-id="f2402-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, and you can use the archived document to recreate the document that it was archived from.</span></span>

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="f2402-105">Sådan konfigurerer du automatisk dokumentarkivering</span><span class="sxs-lookup"><span data-stu-id="f2402-105">To set up automatic document archiving</span></span>  
<span data-ttu-id="f2402-106">Du kan konfigurere automatisk arkivering af salgs- og indkøbsordrer, tilbud, rammeordrer og returordrer, før du sletter dokumenter.</span><span class="sxs-lookup"><span data-stu-id="f2402-106">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="f2402-107">Nedenstående fremgangsmåde beskriver konfigurationen af automatisk arkivering af salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="f2402-107">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="f2402-108">Fremgangsmåden er den samme for købsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="f2402-108">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="f2402-109">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsopsætning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f2402-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="f2402-110">I vinduet **Opsætning af salg og tilgodehavender** skal du udfylde følgende felter:</span><span class="sxs-lookup"><span data-stu-id="f2402-110">In the **Sales & Receivables Setup** window, fill in the fields as follows.</span></span>

|<span data-ttu-id="f2402-111">Felt</span><span class="sxs-lookup"><span data-stu-id="f2402-111">Field</span></span>|<span data-ttu-id="f2402-112">Description</span><span class="sxs-lookup"><span data-stu-id="f2402-112">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="f2402-113">**Arkivering af salgstilbud**</span><span class="sxs-lookup"><span data-stu-id="f2402-113">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="f2402-114">**Aldrig**, hvis du aldrig vil arkivere salgstilbud, når de slettes.</span><span class="sxs-lookup"><span data-stu-id="f2402-114">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="f2402-115">**Spørgsmål**, hvis brugeren skal vælge, om salgstilbud skal arkiveres, når de slettes.</span><span class="sxs-lookup"><span data-stu-id="f2402-115">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="f2402-116">**Altid**, hvis du automatisk vil arkivere salgstilbud, når de slettes.</span><span class="sxs-lookup"><span data-stu-id="f2402-116">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="f2402-117">**Arkivering af rammesalgsordrer**</span><span class="sxs-lookup"><span data-stu-id="f2402-117">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="f2402-118">Vælg dette, hvis du vil arkivere rammesalgsordrer automatisk, hver gang de slettes.</span><span class="sxs-lookup"><span data-stu-id="f2402-118">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="f2402-119">**Arkivering af ordrer og returvareordrer**</span><span class="sxs-lookup"><span data-stu-id="f2402-119">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="f2402-120">Vælg dette, hvis du vil arkivere salgsordrer automatisk, hver gang de slettes.</span><span class="sxs-lookup"><span data-stu-id="f2402-120">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="f2402-121">Sådan arkiveres en salgsordre</span><span class="sxs-lookup"><span data-stu-id="f2402-121">To archive a sales order</span></span>
<span data-ttu-id="f2402-122">Nedenstående procedure beskriver, hvordan du arkiverer en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="f2402-122">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="f2402-123">Fremgangsmåden er den samme for alle ordrer, rammeordrer, returvareordrer og tilbud.</span><span class="sxs-lookup"><span data-stu-id="f2402-123">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="f2402-124">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f2402-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f2402-125">Åbn en salgsordre, som du vil arkivere.</span><span class="sxs-lookup"><span data-stu-id="f2402-125">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="f2402-126">Vælg handlingen **Arkivér bilag**.</span><span class="sxs-lookup"><span data-stu-id="f2402-126">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="f2402-127">Salgsordren arkiveres.</span><span class="sxs-lookup"><span data-stu-id="f2402-127">The sales order is archived.</span></span> <span data-ttu-id="f2402-128">Du kan se den i vinduet **Arkiverede salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="f2402-128">You can view it in the **Archived Sales orders** window.</span></span> <span data-ttu-id="f2402-129">Her kan du også bruge den til at genskabe den salgsordre, som den blev arkiveret fra.</span><span class="sxs-lookup"><span data-stu-id="f2402-129">From here, you can also use it to recreate the sales order that it was archived from.</span></span>

## <a name="to-recreate-a-sales-order-from-the-archive"></a><span data-ttu-id="f2402-130">Sådan genoprettes en salgsordre fra arkivet</span><span class="sxs-lookup"><span data-stu-id="f2402-130">To recreate a sales order from the archive</span></span>
<span data-ttu-id="f2402-131">Nedenstående procedure beskriver, hvordan du genopretter en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="f2402-131">The following procedure describes how to recreate a sales order.</span></span> <span data-ttu-id="f2402-132">Fremgangsmåden er den samme for alle ordrer, rammeordrer, returvareordrer og tilbud.</span><span class="sxs-lookup"><span data-stu-id="f2402-132">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="f2402-133">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Arkiverede salgsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f2402-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2.  <span data-ttu-id="f2402-134">Vælg den arkiverede salgsordre, du vil genoprette, og vælg derefter handlingen **Gendan**.</span><span class="sxs-lookup"><span data-stu-id="f2402-134">Select the archived sales order that you want to recreate, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="f2402-135">Salgsordren oprettes og føjes til vinduet **Salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="f2402-135">The sales order is created and added to the **Sales Orders** window.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="f2402-136">Sådan sletter du arkiverede salgsordrer</span><span class="sxs-lookup"><span data-stu-id="f2402-136">To delete archived sales orders</span></span>
<span data-ttu-id="f2402-137">Nedenstående procedure beskriver, hvordan du sletter arkiverede salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="f2402-137">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="f2402-138">Trinene er de samme for andre arkiverede salgs- og købsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="f2402-138">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="f2402-139">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Slet arkiverede salgsordreversioner**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f2402-139">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f2402-140">I feltet **Slet arkiverede salgsordreversioner** skal du vælge de relevante filtre.</span><span class="sxs-lookup"><span data-stu-id="f2402-140">In the **Delete Archived Sales Order Versions** window, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="f2402-141">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2402-141">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="f2402-142">Se også</span><span class="sxs-lookup"><span data-stu-id="f2402-142">See Also</span></span>
[<span data-ttu-id="f2402-143">Spor dokumentlinjer</span><span class="sxs-lookup"><span data-stu-id="f2402-143">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="f2402-144">Salg</span><span class="sxs-lookup"><span data-stu-id="f2402-144">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="f2402-145">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="f2402-145">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="f2402-146">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f2402-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

