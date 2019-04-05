---
title: Angive, hvilke indgående dokumenter der skal vises | Microsoft Docs
description: Tilpas standardvisningen af indgående dokumenter, f.eks. e-fakturaer, for at forbedre din oversigt over behandlede og ikke-behandlede poster.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 97ca5aab24b04f6c2d0677c6fd9626b93fcd8ca8
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "793064"
---
# <a name="manage-many-incoming-document-records"></a><span data-ttu-id="fd01b-103">Administrere mange indgående dokumentposter</span><span class="sxs-lookup"><span data-stu-id="fd01b-103">Manage Many Incoming Document Records</span></span>
<span data-ttu-id="fd01b-104">Efterhånden som du opretter eller behandler indgående dokumentposter, kan antal linjer på siden **Indkommende dokumenter** vokse til et omfang, hvor du mister overblikket.</span><span class="sxs-lookup"><span data-stu-id="fd01b-104">As you create or process incoming document records, the number of lines on the **Incoming Documents** page may grow to an extent where you lose overview.</span></span> <span data-ttu-id="fd01b-105">Derfor kan du indstille indgående dokumentposter til Behandlet for at fjerne dem fra standardvisningen.</span><span class="sxs-lookup"><span data-stu-id="fd01b-105">Therefore, you can set incoming document records to Processed to remove them from the default view.</span></span> <span data-ttu-id="fd01b-106">Når du vælger handlingen **Vis alle**, kan du få vist både behandlede og ikke-behandlede poster.</span><span class="sxs-lookup"><span data-stu-id="fd01b-106">When you choose the **Show All** action, you can view both processed and unprocessed records.</span></span>

> [!NOTE]  
>   <span data-ttu-id="fd01b-107">Du kan ikke redigere oplysningerne, vedhæfte filer eller udføre andre processer på indgående dokumentposter, der er indstillet til Behandlet.</span><span class="sxs-lookup"><span data-stu-id="fd01b-107">You cannot edit information, attach files, or perform other processes on incoming document records that are set to Processed.</span></span> <span data-ttu-id="fd01b-108">Du skal først indstille dem til Ikke-behandlet.</span><span class="sxs-lookup"><span data-stu-id="fd01b-108">You must first set it to Unprocessed.</span></span>

<span data-ttu-id="fd01b-109">Afkrydsningsfeltet **Behandlet** markeres automatisk på indgående dokumentposter, der er blevet behandlet, men du kan også markere eller fjerne markeringen i feltet manuelt.</span><span class="sxs-lookup"><span data-stu-id="fd01b-109">The **Processed** check box is automatically selected on incoming document records that have been processed, but you can also select or deselect the check box manually.</span></span> <span data-ttu-id="fd01b-110">Afhængigt af din forretningsproces kan en indgående dokumentpost blive behandlet, når der er oprettet et relateret dokument til den, eller der er vedhæftet en fil.</span><span class="sxs-lookup"><span data-stu-id="fd01b-110">Depending on your business process, an incoming document record may be processed when a related document has been created for it or a file has been attached.</span></span>

> [!NOTE]  
>   <span data-ttu-id="fd01b-111">Når du åbner siden **Indkommende dokumenter** med handlingen **Indkommende dokumenter** i Rollecenter, vises kun ikke-behandlede indgående dokumentposter som standard.</span><span class="sxs-lookup"><span data-stu-id="fd01b-111">When you open the **Incoming Documents** page with the **My Incoming Documents** action on the Role Center, only unprocessed incoming document records are shown by default.</span></span> <span data-ttu-id="fd01b-112">I dette emne omtales det som "standardvisningen".</span><span class="sxs-lookup"><span data-stu-id="fd01b-112">This is referred to in this topic as "the default view".</span></span>

## <a name="to-remove-incoming-document-records-from-the-default-view"></a><span data-ttu-id="fd01b-113">Sådan fjernes indgående dokumentposter fra standardvisningen</span><span class="sxs-lookup"><span data-stu-id="fd01b-113">To remove incoming document records from the default view</span></span>
1. <span data-ttu-id="fd01b-114">På siden **Indkommende dokumenter** skal du vælge en eller flere linjer for indgående dokumentposter, du vil fjerne fra standardvinduet.</span><span class="sxs-lookup"><span data-stu-id="fd01b-114">On the **Incoming Documents** page, select one or more lines for incoming document records that you want to remove from the default view.</span></span>
2. <span data-ttu-id="fd01b-115">Vælg handlingen **Indstil til behandlet**.</span><span class="sxs-lookup"><span data-stu-id="fd01b-115">Choose the **Set to Processed** action.</span></span>

    <span data-ttu-id="fd01b-116">Indgående dokumentposter fjernes fra standardvisningen og afkrydsningsfeltet **Behandlet** markeres på linjerne.</span><span class="sxs-lookup"><span data-stu-id="fd01b-116">The incoming document records are removed from the default view, and the **Processed** check box is selected on the lines.</span></span>

> [!NOTE]  
>   <span data-ttu-id="fd01b-117">Du kan også udføre handlingen for den individuelle post på siden **Indgående bilagskort**.</span><span class="sxs-lookup"><span data-stu-id="fd01b-117">You can also perform this action for the individual record on the **Incoming Document Card** page.</span></span>

## <a name="to-view-all-incoming-document-records"></a><span data-ttu-id="fd01b-118">Sådan vises alle indgående dokumentposter</span><span class="sxs-lookup"><span data-stu-id="fd01b-118">To view all incoming document records</span></span>
1. <span data-ttu-id="fd01b-119">På siden **Indgående dokumenter** skal du vælge handlingen **Vis alle**.</span><span class="sxs-lookup"><span data-stu-id="fd01b-119">On the **Incoming Documents** page, choose the **Show All** action.</span></span>

<span data-ttu-id="fd01b-120">Alle indgående dokumentposter vises, herunder dem, hvor feltet **Behandlet** ikke er markeret.</span><span class="sxs-lookup"><span data-stu-id="fd01b-120">All incoming document records are displayed, including those where the **Processed** check box is not selected.</span></span>

## <a name="to-add-incoming-document-records-to-the-default-view"></a><span data-ttu-id="fd01b-121">Sådan føjes indgående dokumentposter til standardvisningen</span><span class="sxs-lookup"><span data-stu-id="fd01b-121">To add incoming document records to the default view</span></span>
1. <span data-ttu-id="fd01b-122">På siden **Indgående dokumenter** skal du vælge handlingen **Vis alle**.</span><span class="sxs-lookup"><span data-stu-id="fd01b-122">On the **Incoming Documents** page, choose the **Show All** action.</span></span>
2. <span data-ttu-id="fd01b-123">Vælg en eller flere linjer for indgående dokumentposter, der skal vises i standardvisningen.</span><span class="sxs-lookup"><span data-stu-id="fd01b-123">Select one or more lines for incoming document records that you want to appear in the default view.</span></span>
3. <span data-ttu-id="fd01b-124">Vælg handlingen **Indstil til ikke-behandlet**.</span><span class="sxs-lookup"><span data-stu-id="fd01b-124">Choose the **Set to Unprocessed** action.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="fd01b-125">Du kan også udføre handlingen for den individuelle post på siden **Indgående bilagskort**.</span><span class="sxs-lookup"><span data-stu-id="fd01b-125">You can also perform this action for the individual record on the **Incoming Document Card** page.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd01b-126">Se også</span><span class="sxs-lookup"><span data-stu-id="fd01b-126">See Also</span></span>
[<span data-ttu-id="fd01b-127">Behandle indgående bilag</span><span class="sxs-lookup"><span data-stu-id="fd01b-127">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="fd01b-128">Indgående bilag</span><span class="sxs-lookup"><span data-stu-id="fd01b-128">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="fd01b-129">Køb</span><span class="sxs-lookup"><span data-stu-id="fd01b-129">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="fd01b-130">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fd01b-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
