---
title: Sådan arkiveres salgs- og købsdokumenter | Microsoft Docs
description: Du kan arkivere salgs- og købsdokumenter, ordrer, tilbud, returvareordrer og rammeordrer, og du kan bruge det arkiverede dokument til at genskabe det dokument, som det blev arkiveret fra.
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
ms.openlocfilehash: 32a50a2b1b967fa2f19022ab6e07865716243d8e
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "917162"
---
# <a name="archive-documents"></a><span data-ttu-id="fb888-103">Arkivere dokumenter</span><span class="sxs-lookup"><span data-stu-id="fb888-103">Archive Documents</span></span>
<span data-ttu-id="fb888-104">Du kan arkivere salgs- og købsordrer, tilbud, returvareordrer og rammeordrer, f.eks. fordi du vil gemme en kopi af et dokument til senere genbrug.</span><span class="sxs-lookup"><span data-stu-id="fb888-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, for example because you want to save a copy of a document for reuse later.</span></span> <span data-ttu-id="fb888-105">Du kan arkiverer et salgs- eller købsdokument flere gange og gemme en ny arkiveret version hver gang.</span><span class="sxs-lookup"><span data-stu-id="fb888-105">You can archive a sales or purchase document several times, saving a different archived version each time.</span></span>

<span data-ttu-id="fb888-106">For arkiverede dokumenter, hvor originalen stadig findes og ikke er bogført, kan du bruge funktionen **Gendan**, hvis du vil overskrive originalen med den arkiverede version af dokumentet.</span><span class="sxs-lookup"><span data-stu-id="fb888-106">For archived documents where the original still exists and is not posted, you can use the **Restore** function to overwrite the original with the archived version of the document.</span></span> <span data-ttu-id="fb888-107">Dette er nyttigt, hvis du vil gendanne indholdet af et dokument i en tidligere tilstand.</span><span class="sxs-lookup"><span data-stu-id="fb888-107">This is practical if you need to restore the contents of a document to an earlier state.</span></span>

<span data-ttu-id="fb888-108">Du kan kun genbruge indholdet af arkiverede dokumenter, hvor originalen er sletter, ved at kopiere dataene, for eksempel med funktionen **Kopiér dokument**.</span><span class="sxs-lookup"><span data-stu-id="fb888-108">For archived documents where the original is deleted, you can only reuse the content by copying the data, for example with the **Copy Document** function.</span></span>   

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="fb888-109">Sådan konfigurerer du automatisk dokumentarkivering</span><span class="sxs-lookup"><span data-stu-id="fb888-109">To set up automatic document archiving</span></span>  
<span data-ttu-id="fb888-110">Du kan konfigurere automatisk arkivering af salgs- og indkøbsordrer, tilbud, rammeordrer og returordrer, før du sletter dokumenter.</span><span class="sxs-lookup"><span data-stu-id="fb888-110">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="fb888-111">Nedenstående fremgangsmåde beskriver konfigurationen af automatisk arkivering af salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="fb888-111">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="fb888-112">Fremgangsmåden er den samme for købsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="fb888-112">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="fb888-113">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning af salg og tilgodehavender**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="fb888-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="fb888-114">På siden **Salgsopsætning** skal du udfylde felterne på følgende måde.</span><span class="sxs-lookup"><span data-stu-id="fb888-114">On the **Sales & Receivables Setup** page, fill in the fields as follows.</span></span>

|<span data-ttu-id="fb888-115">Felt</span><span class="sxs-lookup"><span data-stu-id="fb888-115">Field</span></span>|<span data-ttu-id="fb888-116">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="fb888-116">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="fb888-117">**Arkivering af salgstilbud**</span><span class="sxs-lookup"><span data-stu-id="fb888-117">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="fb888-118">**Aldrig**, hvis du aldrig vil arkivere salgstilbud, når de slettes.</span><span class="sxs-lookup"><span data-stu-id="fb888-118">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="fb888-119">**Spørgsmål**, hvis brugeren skal vælge, om salgstilbud skal arkiveres, når de slettes.</span><span class="sxs-lookup"><span data-stu-id="fb888-119">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="fb888-120">**Altid**, hvis du automatisk vil arkivere salgstilbud, når de slettes.</span><span class="sxs-lookup"><span data-stu-id="fb888-120">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="fb888-121">**Arkivering af rammesalgsordrer**</span><span class="sxs-lookup"><span data-stu-id="fb888-121">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="fb888-122">Vælg dette, hvis du vil arkivere rammesalgsordrer automatisk, hver gang de slettes.</span><span class="sxs-lookup"><span data-stu-id="fb888-122">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="fb888-123">**Arkivering af ordrer og returvareordrer**</span><span class="sxs-lookup"><span data-stu-id="fb888-123">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="fb888-124">Vælg dette, hvis du vil arkivere salgsordrer automatisk, hver gang de slettes.</span><span class="sxs-lookup"><span data-stu-id="fb888-124">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="fb888-125">Sådan arkiveres en salgsordre</span><span class="sxs-lookup"><span data-stu-id="fb888-125">To archive a sales order</span></span>
<span data-ttu-id="fb888-126">Nedenstående procedure beskriver, hvordan du arkiverer en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="fb888-126">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="fb888-127">Fremgangsmåden er den samme for alle ordrer, rammeordrer, returvareordrer og tilbud.</span><span class="sxs-lookup"><span data-stu-id="fb888-127">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="fb888-128">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="fb888-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="fb888-129">Åbn en salgsordre, som du vil arkivere.</span><span class="sxs-lookup"><span data-stu-id="fb888-129">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="fb888-130">Vælg handlingen **Arkivér bilag**.</span><span class="sxs-lookup"><span data-stu-id="fb888-130">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="fb888-131">Salgsordren arkiveres.</span><span class="sxs-lookup"><span data-stu-id="fb888-131">The sales order is archived.</span></span> <span data-ttu-id="fb888-132">Du kan se den på siden **Arkiverede salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="fb888-132">You can view it on the **Archived Sales orders** page.</span></span>

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a><span data-ttu-id="fb888-133">Sådan gendannes en ikke-bogført salgsordre fra arkivet</span><span class="sxs-lookup"><span data-stu-id="fb888-133">To restore a non-posted sales order from the archive</span></span>
<span data-ttu-id="fb888-134">Følgende procedure beskriver, hvordan du får indholdet af en arkiveret salgsordre tilbage til den oprindelige salgsordre.</span><span class="sxs-lookup"><span data-stu-id="fb888-134">The following procedure describes how to bring the contents of an archived sales order back to the original sales order.</span></span> <span data-ttu-id="fb888-135">Det er kun muligt, når det oprindelige dokument ikke er bogført.</span><span class="sxs-lookup"><span data-stu-id="fb888-135">This is only possible when the original document has not been posted.</span></span> <span data-ttu-id="fb888-136">Fremgangsmåden er den samme for alle ordrer, rammeordrer, returvareordrer og tilbud.</span><span class="sxs-lookup"><span data-stu-id="fb888-136">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1. <span data-ttu-id="fb888-137">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Arkiverede salgsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="fb888-137">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="fb888-138">Vælg den arkiverede salgsordre eller en version af den, som du vil gendanne, og vælg derefter handlingen **Gendan**.</span><span class="sxs-lookup"><span data-stu-id="fb888-138">Select the archived sales order, or version of it, that you want to restore, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="fb888-139">Oplysningerne i den oprindelige salgsordre erstattes med oplysningerne fra den valgte arkiverede version.</span><span class="sxs-lookup"><span data-stu-id="fb888-139">The contents of the original sales order is replaced with that of the selected archived version.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="fb888-140">Sådan sletter du arkiverede salgsordrer</span><span class="sxs-lookup"><span data-stu-id="fb888-140">To delete archived sales orders</span></span>
<span data-ttu-id="fb888-141">Nedenstående procedure beskriver, hvordan du sletter arkiverede salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="fb888-141">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="fb888-142">Trinene er de samme for andre arkiverede salgs- og købsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="fb888-142">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="fb888-143">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Slet arkiverede salgsordreversioner**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="fb888-143">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="fb888-144">På siden **Slet arkiverede salgsordreversioner** skal du vælge de relevante filtre.</span><span class="sxs-lookup"><span data-stu-id="fb888-144">On the **Delete Archived Sales Order Versions** page, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="fb888-145">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="fb888-145">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="fb888-146">Se også</span><span class="sxs-lookup"><span data-stu-id="fb888-146">See Also</span></span>
[<span data-ttu-id="fb888-147">Spor dokumentlinjer</span><span class="sxs-lookup"><span data-stu-id="fb888-147">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="fb888-148">Salg</span><span class="sxs-lookup"><span data-stu-id="fb888-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="fb888-149">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="fb888-149">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="fb888-150">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fb888-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
