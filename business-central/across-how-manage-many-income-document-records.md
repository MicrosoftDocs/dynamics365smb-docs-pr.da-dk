---
title: Angive, hvilke indgående bilag der skal vises | Microsoft Docs
description: Tilpas standardvisningen af indgående bilag, f.eks. e-fakturaer, for at forbedre din oversigt over behandlede og ikke-behandlede poster.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cb25d7bf0019e75834bcb1efffc41b729f9d64ae
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384645"
---
# <a name="manage-many-incoming-document-records"></a><span data-ttu-id="7552b-103">Administrere mange indgående bilagsposter</span><span class="sxs-lookup"><span data-stu-id="7552b-103">Manage Many Incoming Document Records</span></span>
<span data-ttu-id="7552b-104">Efterhånden som du opretter eller behandler indgående bilagsposter, kan antal linjer på siden **Indgående bilag** vokse til et omfang, hvor du mister overblikket.</span><span class="sxs-lookup"><span data-stu-id="7552b-104">As you create or process incoming document records, the number of lines on the **Incoming Documents** page may grow to an extent where you lose overview.</span></span> <span data-ttu-id="7552b-105">Derfor kan du indstille indgående bilagsposter til Behandlet for at fjerne dem fra standardvisningen.</span><span class="sxs-lookup"><span data-stu-id="7552b-105">Therefore, you can set incoming document records to Processed to remove them from the default view.</span></span> <span data-ttu-id="7552b-106">Når du vælger handlingen **Vis alle**, kan du få vist både behandlede og ikke-behandlede poster.</span><span class="sxs-lookup"><span data-stu-id="7552b-106">When you choose the **Show All** action, you can view both processed and unprocessed records.</span></span>

> [!NOTE]  
>   <span data-ttu-id="7552b-107">Du kan ikke redigere oplysningerne, vedhæfte filer eller udføre andre processer på indgående bilagsposter, der er indstillet til Behandlet.</span><span class="sxs-lookup"><span data-stu-id="7552b-107">You cannot edit information, attach files, or perform other processes on incoming document records that are set to Processed.</span></span> <span data-ttu-id="7552b-108">Du skal først indstille dem til Ikke-behandlet.</span><span class="sxs-lookup"><span data-stu-id="7552b-108">You must first set it to Unprocessed.</span></span>

<span data-ttu-id="7552b-109">Afkrydsningsfeltet **Behandlet** markeres automatisk på indgående bilagsposter, der er blevet behandlet, men du kan også markere eller fjerne markeringen i feltet manuelt.</span><span class="sxs-lookup"><span data-stu-id="7552b-109">The **Processed** check box is automatically selected on incoming document records that have been processed, but you can also select or deselect the check box manually.</span></span> <span data-ttu-id="7552b-110">Afhængigt af din forretningsproces kan en indgående bilagspost blive behandlet, når der er oprettet et relateret bilag til den, eller der er vedhæftet en fil.</span><span class="sxs-lookup"><span data-stu-id="7552b-110">Depending on your business process, an incoming document record may be processed when a related document has been created for it or a file has been attached.</span></span>

> [!NOTE]  
>   <span data-ttu-id="7552b-111">Når du åbner siden **Indgående bilag** med handlingen **Indgående bilag** i Rollecenter, vises kun ikke-behandlede indgående bilagsposter som standard.</span><span class="sxs-lookup"><span data-stu-id="7552b-111">When you open the **Incoming Documents** page with the **My Incoming Documents** action on the Role Center, only unprocessed incoming document records are shown by default.</span></span> <span data-ttu-id="7552b-112">I dette emne omtales det som "standardvisningen".</span><span class="sxs-lookup"><span data-stu-id="7552b-112">This is referred to in this topic as "the default view".</span></span>

## <a name="to-remove-incoming-document-records-from-the-default-view"></a><span data-ttu-id="7552b-113">Sådan fjernes indgående bilagsposter fra standardvisningen</span><span class="sxs-lookup"><span data-stu-id="7552b-113">To remove incoming document records from the default view</span></span>
1. <span data-ttu-id="7552b-114">På siden **Indgående bilag** skal du vælge en eller flere linjer for indgående bilagsposter, du vil fjerne fra standardvinduet.</span><span class="sxs-lookup"><span data-stu-id="7552b-114">On the **Incoming Documents** page, select one or more lines for incoming document records that you want to remove from the default view.</span></span>
2. <span data-ttu-id="7552b-115">Vælg handlingen **Indstil til behandlet**.</span><span class="sxs-lookup"><span data-stu-id="7552b-115">Choose the **Set to Processed** action.</span></span>

    <span data-ttu-id="7552b-116">Indgående bilagsposter fjernes fra standardvisningen og afkrydsningsfeltet **Behandlet** markeres på linjerne.</span><span class="sxs-lookup"><span data-stu-id="7552b-116">The incoming document records are removed from the default view, and the **Processed** check box is selected on the lines.</span></span>

> [!NOTE]  
>   <span data-ttu-id="7552b-117">Du kan også udføre handlingen for den individuelle post på siden **Indgående bilagskort**.</span><span class="sxs-lookup"><span data-stu-id="7552b-117">You can also perform this action for the individual record on the **Incoming Document Card** page.</span></span>

## <a name="to-view-all-incoming-document-records"></a><span data-ttu-id="7552b-118">Sådan vises alle indgående bilagsposter</span><span class="sxs-lookup"><span data-stu-id="7552b-118">To view all incoming document records</span></span>
1. <span data-ttu-id="7552b-119">På siden **Indgående bilag** skal du vælge handlingen **Vis alle**.</span><span class="sxs-lookup"><span data-stu-id="7552b-119">On the **Incoming Documents** page, choose the **Show All** action.</span></span>

<span data-ttu-id="7552b-120">Alle indgående bilagsposter vises, herunder dem, hvor feltet **Behandlet** ikke er markeret.</span><span class="sxs-lookup"><span data-stu-id="7552b-120">All incoming document records are displayed, including those where the **Processed** check box is not selected.</span></span>

## <a name="to-add-incoming-document-records-to-the-default-view"></a><span data-ttu-id="7552b-121">Sådan føjes indgående bilagsposter til standardvisningen</span><span class="sxs-lookup"><span data-stu-id="7552b-121">To add incoming document records to the default view</span></span>
1. <span data-ttu-id="7552b-122">På siden **Indgående bilag** skal du vælge handlingen **Vis alle**.</span><span class="sxs-lookup"><span data-stu-id="7552b-122">On the **Incoming Documents** page, choose the **Show All** action.</span></span>
2. <span data-ttu-id="7552b-123">Vælg en eller flere linjer for indgående bilagsposter, der skal vises i standardvisningen.</span><span class="sxs-lookup"><span data-stu-id="7552b-123">Select one or more lines for incoming document records that you want to appear in the default view.</span></span>
3. <span data-ttu-id="7552b-124">Vælg handlingen **Indstil til ikke-behandlet**.</span><span class="sxs-lookup"><span data-stu-id="7552b-124">Choose the **Set to Unprocessed** action.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="7552b-125">Du kan også udføre handlingen for den individuelle post på siden **Indgående bilagskort**.</span><span class="sxs-lookup"><span data-stu-id="7552b-125">You can also perform this action for the individual record on the **Incoming Document Card** page.</span></span>

## <a name="see-also"></a><span data-ttu-id="7552b-126">Se også</span><span class="sxs-lookup"><span data-stu-id="7552b-126">See Also</span></span>
[<span data-ttu-id="7552b-127">Behandle indgående bilag</span><span class="sxs-lookup"><span data-stu-id="7552b-127">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="7552b-128">Indgående bilag</span><span class="sxs-lookup"><span data-stu-id="7552b-128">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="7552b-129">Køb</span><span class="sxs-lookup"><span data-stu-id="7552b-129">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="7552b-130">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7552b-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]