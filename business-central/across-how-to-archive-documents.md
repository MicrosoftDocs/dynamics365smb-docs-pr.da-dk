---
title: Sådan arkiveres salgs- og købsdokumenter | Microsoft Docs
description: Du kan arkivere salgs- og købsdokumenter, ordrer, tilbud, returvareordrer og rammeordrer, og du kan bruge det arkiverede dokument til at genskabe det dokument, som det blev arkiveret fra.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 209ef492bf5620921ce371a17227653576dcae8a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775893"
---
# <a name="archive-documents"></a><span data-ttu-id="57544-103">Arkivere dokumenter</span><span class="sxs-lookup"><span data-stu-id="57544-103">Archive Documents</span></span>
<span data-ttu-id="57544-104">Du kan arkivere salgs- og købsordrer, tilbud, returvareordrer og rammeordrer, f.eks. fordi du vil gemme en kopi af et dokument til senere genbrug.</span><span class="sxs-lookup"><span data-stu-id="57544-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, for example because you want to save a copy of a document for reuse later.</span></span> <span data-ttu-id="57544-105">Du kan arkiverer et salgs- eller købsdokument flere gange og gemme en ny arkiveret version hver gang.</span><span class="sxs-lookup"><span data-stu-id="57544-105">You can archive a sales or purchase document several times, saving a different archived version each time.</span></span>

<span data-ttu-id="57544-106">For arkiverede dokumenter, hvor originalen stadig findes og ikke er bogført, kan du bruge funktionen **Gendan**, hvis du vil overskrive originalen med den arkiverede version af dokumentet.</span><span class="sxs-lookup"><span data-stu-id="57544-106">For archived documents where the original still exists and is not posted, you can use the **Restore** function to overwrite the original with the archived version of the document.</span></span> <span data-ttu-id="57544-107">Dette er nyttigt, hvis du vil gendanne indholdet af et dokument i en tidligere tilstand.</span><span class="sxs-lookup"><span data-stu-id="57544-107">This is practical if you need to restore the contents of a document to an earlier state.</span></span>

<span data-ttu-id="57544-108">Du kan kun genbruge indholdet i arkiverede dokumenter, hvis originalen er slettet, ved at kopiere dataene, for eksempel med funktionen **Kopiér fra dokument**.</span><span class="sxs-lookup"><span data-stu-id="57544-108">For archived documents where the original is deleted, you can only reuse the content by copying the data, for example with the **Copy from Document** function.</span></span>   

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="57544-109">Sådan konfigurerer du automatisk dokumentarkivering</span><span class="sxs-lookup"><span data-stu-id="57544-109">To set up automatic document archiving</span></span>  
<span data-ttu-id="57544-110">Du kan konfigurere automatisk arkivering af salgs- og indkøbsordrer, tilbud, rammeordrer og returordrer, før du sletter dokumenter.</span><span class="sxs-lookup"><span data-stu-id="57544-110">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="57544-111">Nedenstående fremgangsmåde beskriver konfigurationen af automatisk arkivering af salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="57544-111">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="57544-112">Fremgangsmåden er den samme for købsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="57544-112">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="57544-113">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsopsætning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="57544-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="57544-114">På siden **Salgsopsætning** skal du udfylde felterne på følgende måde.</span><span class="sxs-lookup"><span data-stu-id="57544-114">On the **Sales & Receivables Setup** page, fill in the fields as follows.</span></span>

|<span data-ttu-id="57544-115">Felt</span><span class="sxs-lookup"><span data-stu-id="57544-115">Field</span></span>|<span data-ttu-id="57544-116">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="57544-116">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="57544-117">**Arkivering af salgstilbud**</span><span class="sxs-lookup"><span data-stu-id="57544-117">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="57544-118">**Aldrig**, hvis du aldrig vil arkivere salgstilbud, når de slettes.</span><span class="sxs-lookup"><span data-stu-id="57544-118">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="57544-119">**Spørgsmål**, hvis brugeren skal vælge, om salgstilbud skal arkiveres, når de slettes.</span><span class="sxs-lookup"><span data-stu-id="57544-119">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="57544-120">**Altid**, hvis du automatisk vil arkivere salgstilbud, når de slettes.</span><span class="sxs-lookup"><span data-stu-id="57544-120">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="57544-121">**Arkivering af rammesalgsordrer**</span><span class="sxs-lookup"><span data-stu-id="57544-121">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="57544-122">Vælg dette, hvis du vil arkivere rammesalgsordrer automatisk, hver gang de slettes.</span><span class="sxs-lookup"><span data-stu-id="57544-122">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="57544-123">**Arkivering af ordrer og returvareordrer**</span><span class="sxs-lookup"><span data-stu-id="57544-123">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="57544-124">Vælg dette, hvis du vil arkivere salgsordrer automatisk, hver gang de slettes.</span><span class="sxs-lookup"><span data-stu-id="57544-124">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="57544-125">Sådan arkiveres en salgsordre</span><span class="sxs-lookup"><span data-stu-id="57544-125">To archive a sales order</span></span>
<span data-ttu-id="57544-126">Nedenstående procedure beskriver, hvordan du arkiverer en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="57544-126">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="57544-127">Fremgangsmåden er den samme for alle ordrer, rammeordrer, returvareordrer og tilbud.</span><span class="sxs-lookup"><span data-stu-id="57544-127">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="57544-128">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordre**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="57544-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="57544-129">Åbn en salgsordre, som du vil arkivere.</span><span class="sxs-lookup"><span data-stu-id="57544-129">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="57544-130">Vælg handlingen **Arkivér bilag**.</span><span class="sxs-lookup"><span data-stu-id="57544-130">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="57544-131">Salgsordren arkiveres.</span><span class="sxs-lookup"><span data-stu-id="57544-131">The sales order is archived.</span></span> <span data-ttu-id="57544-132">Du kan se den på siden **Arkiverede salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="57544-132">You can view it on the **Archived Sales Orders** page.</span></span>

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a><span data-ttu-id="57544-133">Sådan gendannes en ikke-bogført salgsordre fra arkivet</span><span class="sxs-lookup"><span data-stu-id="57544-133">To restore a non-posted sales order from the archive</span></span>
<span data-ttu-id="57544-134">Følgende procedure beskriver, hvordan du får indholdet af en arkiveret salgsordre tilbage til den oprindelige salgsordre.</span><span class="sxs-lookup"><span data-stu-id="57544-134">The following procedure describes how to bring the contents of an archived sales order back to the original sales order.</span></span> <span data-ttu-id="57544-135">Det er kun muligt, når det oprindelige dokument ikke er bogført.</span><span class="sxs-lookup"><span data-stu-id="57544-135">This is only possible when the original document has not been posted.</span></span> <span data-ttu-id="57544-136">Fremgangsmåden er den samme for alle ordrer, rammeordrer, returvareordrer og tilbud.</span><span class="sxs-lookup"><span data-stu-id="57544-136">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1. <span data-ttu-id="57544-137">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Arkiverede salgsordre**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="57544-137">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="57544-138">Vælg den arkiverede salgsordre eller en version af den, som du vil gendanne, og vælg derefter handlingen **Gendan**.</span><span class="sxs-lookup"><span data-stu-id="57544-138">Select the archived sales order, or version of it, that you want to restore, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="57544-139">Oplysningerne i den oprindelige salgsordre erstattes med oplysningerne fra den valgte arkiverede version.</span><span class="sxs-lookup"><span data-stu-id="57544-139">The contents of the original sales order is replaced with that of the selected archived version.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="57544-140">Sådan sletter du arkiverede salgsordrer</span><span class="sxs-lookup"><span data-stu-id="57544-140">To delete archived sales orders</span></span>
<span data-ttu-id="57544-141">Nedenstående procedure beskriver, hvordan du sletter arkiverede salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="57544-141">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="57544-142">Trinene er de samme for andre arkiverede salgs- og købsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="57544-142">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="57544-143">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Slet arkiverede salgsordreversioner**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="57544-143">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="57544-144">På siden **Slet arkiverede salgsordreversioner** skal du vælge de relevante filtre.</span><span class="sxs-lookup"><span data-stu-id="57544-144">On the **Delete Archived Sales Order Versions** page, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="57544-145">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="57544-145">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="57544-146">Se også</span><span class="sxs-lookup"><span data-stu-id="57544-146">See Also</span></span>
[<span data-ttu-id="57544-147">Spor dokumentlinjer</span><span class="sxs-lookup"><span data-stu-id="57544-147">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="57544-148">Salg</span><span class="sxs-lookup"><span data-stu-id="57544-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="57544-149">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="57544-149">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="57544-150">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="57544-150">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]