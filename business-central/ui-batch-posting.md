---
title: Sådan bogføres flere dokumenter på én gang | Microsoft Docs
description: I stedet for at bogføre individuelle dokumenter ét ad gangen, kan du vælge flere ikke-bogførte dokumenter i en oversigt til baggrundsbogføring, enten med det samme eller planlagt til f.eks. dagens slutning.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 08/18/2020
ms.author: edupont
ms.openlocfilehash: 2c04dac37b043995a9b78e2f662f9411c3cf9ae1
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782514"
---
# <a name="post-multiple-documents-at-the-same-time"></a><span data-ttu-id="d9955-103">Bogføre flere dokumenter på én gang</span><span class="sxs-lookup"><span data-stu-id="d9955-103">Post Multiple Documents at the Same Time</span></span>

<span data-ttu-id="d9955-104">I stedet for at bogføre individuelle dokumenter ét ad gangen, kan du vælge flere ikke-bogførte dokumenter i en oversigt til bogføring med det samme eller til baggrundsbogføring i henhold til en plan, f.eks. ved dagens slutning.</span><span class="sxs-lookup"><span data-stu-id="d9955-104">Instead of posting individual documents one by one, you can select multiple non-posted documents in a list for immediate posting or for batch posting according to a schedule, such as at the end of the day.</span></span> <span data-ttu-id="d9955-105">Dette kan være nyttigt, hvis det kun er en supervisor, der kan bogføre dokumenter, der er oprettet af andre brugere, eller for at undgå, at der opstår problemer med systemydeevnen under bogføring i arbejdstiden.</span><span class="sxs-lookup"><span data-stu-id="d9955-105">This may be useful if only a supervisor can post documents created by other users or to avoid system performance issues from posting during work hours.</span></span>

## <a name="to-post-multiple-purchase-orders-immediately"></a><span data-ttu-id="d9955-106">Sådan bogføres flere købsordrer med det samme</span><span class="sxs-lookup"><span data-stu-id="d9955-106">To post multiple purchase orders immediately</span></span>

<span data-ttu-id="d9955-107">Følgende procedure beskriver, hvordan flere købsordrer kan bogføres med det samme.</span><span class="sxs-lookup"><span data-stu-id="d9955-107">The following procedure explains how to post multiple purchase orders immediately.</span></span> <span data-ttu-id="d9955-108">Trinene er de samme for alle købs- og salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="d9955-108">The steps are similar for all purchase and sales documents.</span></span>

1. <span data-ttu-id="d9955-109">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsordre**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d9955-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="d9955-110">Fortsæt med at vælge alle de ordrer, der skal bogføres, på siden **Købsordrer**:</span><span class="sxs-lookup"><span data-stu-id="d9955-110">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="d9955-111">I feltet **Nummer**</span><span class="sxs-lookup"><span data-stu-id="d9955-111">In the **No.**</span></span> <span data-ttu-id="d9955-112">skal du vælge de tre lodrette prikker for at åbne genvejsmenuen og derefter vælge handlingen **Markér flere**.</span><span class="sxs-lookup"><span data-stu-id="d9955-112">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="d9955-113">Marker afkrydsningsfeltet for alle de linjer, der repræsenterer ordrer, som du vil bogføre på samme tid.</span><span class="sxs-lookup"><span data-stu-id="d9955-113">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="d9955-114">Vælg handlingen **Bogføring**, og vælg derefter handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="d9955-114">Choose the **Posting** action, and then choose the **Post** action.</span></span>
6. <span data-ttu-id="d9955-115">Vælg knappen **Ja** i bekræftelsesmeddelelsen.</span><span class="sxs-lookup"><span data-stu-id="d9955-115">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-batch-post-multiple-purchase-orders"></a><span data-ttu-id="d9955-116">Sådan massebogføres flere købsordrer</span><span class="sxs-lookup"><span data-stu-id="d9955-116">To batch post multiple purchase orders</span></span>

<span data-ttu-id="d9955-117">Følgende procedure beskriver, hvordan du kan massebogføre flere købsordrer.</span><span class="sxs-lookup"><span data-stu-id="d9955-117">The following procedure explains how to batch post purchase orders.</span></span> <span data-ttu-id="d9955-118">Fremgangsmåden er den samme for alle købs- og salgsdokumenter, hvor handlingen **Massebogfør** er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="d9955-118">The steps are similar for all purchase and sales documents where the **Batch Post** action is available.</span></span>

> [!NOTE]
> <span data-ttu-id="d9955-119">Massebogføring af dokumenter sker i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="d9955-119">Batch posting of documents happens in the background.</span></span> <span data-ttu-id="d9955-120">[!INCLUDE [prodshort](includes/prodshort.md)] online indeholder standardjobs til baggrundsbogføring og massebogføring.</span><span class="sxs-lookup"><span data-stu-id="d9955-120">[!INCLUDE [prodshort](includes/prodshort.md)] online includes default jobs for background posting and batch posting.</span></span> <span data-ttu-id="d9955-121">Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="d9955-121">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

1. <span data-ttu-id="d9955-122">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsordre**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d9955-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d9955-123">Fortsæt med at vælge alle de ordrer, der skal bogføres, på siden **Købsordrer**:</span><span class="sxs-lookup"><span data-stu-id="d9955-123">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="d9955-124">I feltet **Nummer**</span><span class="sxs-lookup"><span data-stu-id="d9955-124">In the **No.**</span></span> <span data-ttu-id="d9955-125">skal du vælge de tre lodrette prikker for at åbne genvejsmenuen og derefter vælge handlingen **Markér flere**.</span><span class="sxs-lookup"><span data-stu-id="d9955-125">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="d9955-126">Marker afkrydsningsfeltet for alle de linjer, der repræsenterer ordrer, som du vil bogføre på samme tid.</span><span class="sxs-lookup"><span data-stu-id="d9955-126">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="d9955-127">Vælg handlingen **Bogføring**, og vælg derefter handlingen **Massebogfør**.</span><span class="sxs-lookup"><span data-stu-id="d9955-127">Choose the **Posting** action, and then choose the **Post Batch** action.</span></span>
6. <span data-ttu-id="d9955-128">Udfyld felterne efter behov på siden **Massebogfør købsordre**.</span><span class="sxs-lookup"><span data-stu-id="d9955-128">On the **Batch Post Purchase Order** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. <span data-ttu-id="d9955-129">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="d9955-129">Choose the **OK** button.</span></span>
8. <span data-ttu-id="d9955-130">Hvis du vil have vist potentielle problemer, der er opstået under massebogføring af dokumenter, skal du åbne siden **Registrer over fejlmeddelelser**.</span><span class="sxs-lookup"><span data-stu-id="d9955-130">To view potential issues that occurred during batch posting of documents, open the **Error Message Register** page.</span></span>

<span data-ttu-id="d9955-131">Købsordrerne føjes nu til en dedikeret opgavekøpost, der definerer, hvornår dokumenterne bliver bogført.</span><span class="sxs-lookup"><span data-stu-id="d9955-131">The purchase orders will now be added to a dedicated job queue entry, which defines when the documents are posted.</span></span> <span data-ttu-id="d9955-132">Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="d9955-132">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

<span data-ttu-id="d9955-133">Hvis du vælger **PDF** i feltet **Rapportresultattype**, er alle købsordrer, der er blevet bogført, tilgængelige i delen **Rapportindbakke** i rollecenteret.</span><span class="sxs-lookup"><span data-stu-id="d9955-133">If you select **PDF** in the **Report Output Type** field, successfully posted purchase orders will be available in the **Report Inbox** part on your Role Center.</span></span>

## <a name="see-also"></a><span data-ttu-id="d9955-134">Se også</span><span class="sxs-lookup"><span data-stu-id="d9955-134">See Also</span></span>

[<span data-ttu-id="d9955-135">Bogføring af dokumenter og kladder</span><span class="sxs-lookup"><span data-stu-id="d9955-135">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
[<span data-ttu-id="d9955-136">Bruge opgavekøer til at planlægge opgaver</span><span class="sxs-lookup"><span data-stu-id="d9955-136">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
[<span data-ttu-id="d9955-137">Redigere bogførte dokumenter</span><span class="sxs-lookup"><span data-stu-id="d9955-137">Edit Posted Documents</span></span>](across-edit-posted-document.md)  
[<span data-ttu-id="d9955-138">Rette eller annullere ubetalte købsfakturaer</span><span class="sxs-lookup"><span data-stu-id="d9955-138">Correct or Cancel Unpaid Purchase Invoices</span></span>](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[<span data-ttu-id="d9955-139">Søge efter sider og oplysninger med Fortæl mig</span><span class="sxs-lookup"><span data-stu-id="d9955-139">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="d9955-140">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d9955-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
