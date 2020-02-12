---
title: Konfigurere indgående bilag | Microsoft Docs
description: Du kan bruge funktionen Indgående bilag til at oprette elektroniske dokumenter, administrere OCR-opgaver, indlæse fakturaer og konvertere billedfiler.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 12/09/2019
ms.author: sgroespe
ms.openlocfilehash: e67ca1c0b26d7e4a81e53854ca31efc64a366c3f
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2910488"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="85b69-103">Konfigurere indgående bilag</span><span class="sxs-lookup"><span data-stu-id="85b69-103">Set Up Incoming Documents</span></span>
<span data-ttu-id="85b69-104">Hvis du opretter finanskladdelinjer fra indgående bilagsposter, skal du på siden **Konfiguration af indgående bilag** angive hvilken kladdetype og hvilket kladdenavn der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="85b69-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="85b69-105">Hvis du ikke ønsker, at brugere kan oprette fakturaer eller finanskladdelinjer fra indgående bilagsposter, medmindre bilagene først er godkendt, skal du konfigurere workflowgodkendere.</span><span class="sxs-lookup"><span data-stu-id="85b69-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up workflow approvers.</span></span>

<span data-ttu-id="85b69-106">Hvis du vil aktivere PDF-og billedfiler til elektroniske dokumenter, som du kan konvertere til f.eks. købsfakturaer, skal du først definere OCR-funktionen og aktivere tjenesten i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="85b69-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="85b69-107">Når funktionen Indgående bilag er konfigureret, kan du bruge forskellige funktioner til at gennemgå udgiftsbilag, administrere OCR-opgaver og konvertere indgående bilagsfiler, manuelt eller automatisk, til de relevante købs- og salgsbilag eller kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="85b69-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="85b69-108">Eksterne filer kan tilknyttes i enhver procesfase, herunder til bogførte dokumenter og til de derved oprettede kreditor-, debitor- og finansposter.</span><span class="sxs-lookup"><span data-stu-id="85b69-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="85b69-109">Du kan finde flere oplysninger i [Behandle indgående bilag](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="85b69-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="85b69-110">Sådan konfigureres funktionen for indgående bilag</span><span class="sxs-lookup"><span data-stu-id="85b69-110">To set up the Incoming Documents feature</span></span>
1. <span data-ttu-id="85b69-111">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning for indgående bilag**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="85b69-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="85b69-112">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="85b69-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="85b69-113">Sådan konfigureres godkendere af indgående bilagsposter</span><span class="sxs-lookup"><span data-stu-id="85b69-113">To set up approvers of incoming document records</span></span>
<span data-ttu-id="85b69-114">Godkendere af indgående bilag skal konfigureres som brugere i godkendelsesworkflow.</span><span class="sxs-lookup"><span data-stu-id="85b69-114">Approvers of incoming documents must be set up as approval workflow users.</span></span>

<span data-ttu-id="85b69-115">Før du kan oprette workflows, der omfatter godkendelsestrin, skal du angive workflowbrugere, der er involveret i godkendelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="85b69-115">Before you can create workflows that involve approval steps, you must set up the workflow users who are involved in approval processes.</span></span> <span data-ttu-id="85b69-116">På siden **Konfiguration af godkendelsesbruger** skal du også angive beløbsgrænser for bestemte typer anmodninger og angive stedfortrædende godkendere, som godkendelsesanmodninger skal uddelegeres til, når den oprindelige godkender er fraværende.</span><span class="sxs-lookup"><span data-stu-id="85b69-116">On the **Approval User Setup** page, you also set amount limits for specific types of requests and define substitute approvers to whom approval requests are delegated when the original approver is absent.</span></span> <span data-ttu-id="85b69-117">Du kan finde flere oplysninger i [Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)</span><span class="sxs-lookup"><span data-stu-id="85b69-117">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="85b69-118">Sådan konfigureres en OCR-tjeneste</span><span class="sxs-lookup"><span data-stu-id="85b69-118">To set up an OCR service</span></span>
1. <span data-ttu-id="85b69-119">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning af OCR-tjeneste**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="85b69-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="85b69-120">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="85b69-120">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="85b69-121">Dine logondata krypteres automatisk.</span><span class="sxs-lookup"><span data-stu-id="85b69-121">You login data is automatically encrypted.</span></span>

## <a name="see-also"></a><span data-ttu-id="85b69-122">Se også</span><span class="sxs-lookup"><span data-stu-id="85b69-122">See Also</span></span>
[<span data-ttu-id="85b69-123">Behandle indgående bilag</span><span class="sxs-lookup"><span data-stu-id="85b69-123">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="85b69-124">Indgående bilag</span><span class="sxs-lookup"><span data-stu-id="85b69-124">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="85b69-125">Køb</span><span class="sxs-lookup"><span data-stu-id="85b69-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="85b69-126">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="85b69-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
