---
title: Konfigurere indgående bilag | Microsoft Docs
description: Du kan bruge funktionen Indgående bilag til at oprette elektroniske dokumenter, administrere OCR-opgaver, indlæse fakturaer og konvertere billedfiler.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 08/10/2020
ms.author: sgroespe
ms.openlocfilehash: 7438502e14d1aa0eecdd56db0eb4ae2f2790413a
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/10/2020
ms.locfileid: "3677112"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="b9d9b-103">Konfigurere indgående bilag</span><span class="sxs-lookup"><span data-stu-id="b9d9b-103">Set Up Incoming Documents</span></span>

<span data-ttu-id="b9d9b-104">Hvis du opretter finanskladdelinjer fra indgående bilagsposter, skal du på siden **Konfiguration af indgående bilag** angive hvilken kladdetype og hvilket kladdenavn der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="b9d9b-105">Hvis du ikke ønsker, at brugere kan oprette fakturaer eller finanskladdelinjer fra indgående bilagsposter, medmindre bilagene først er godkendt, skal du konfigurere workflowgodkendere.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up workflow approvers.</span></span>

<span data-ttu-id="b9d9b-106">Hvis du vil aktivere PDF-og billedfiler til elektroniske dokumenter, som du kan konvertere til f.eks. købsfakturaer, skal du først definere OCR-funktionen og aktivere tjenesten i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="b9d9b-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span> <span data-ttu-id="b9d9b-107">Vælg en servicepakke, der passer til din organisation og/eller dit land/område.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-107">Choose a service package that is appropriate for your organization and/or country/region.</span></span> <span data-ttu-id="b9d9b-108">Du kan også oprette poster manuelt, så de repræsenterer eksterne dokumenter.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-108">Alternatively, you can create entries manually to represent the external documents.</span></span>  

<span data-ttu-id="b9d9b-109">Når funktionen Indgående bilag er konfigureret, kan du bruge forskellige funktioner til at gennemgå udgiftsbilag, administrere OCR-opgaver og konvertere indgående bilagsfiler, manuelt eller automatisk, til de relevante købs- og salgsbilag eller kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-109">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="b9d9b-110">Eksterne filer kan tilknyttes i enhver procesfase, herunder til bogførte dokumenter og til de derved oprettede kreditor-, debitor- og finansposter.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-110">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="b9d9b-111">Du kan finde flere oplysninger i [Behandle indgående bilag](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="b9d9b-111">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="b9d9b-112">Sådan konfigureres funktionen for indgående bilag</span><span class="sxs-lookup"><span data-stu-id="b9d9b-112">To set up the Incoming Documents feature</span></span>

1. <span data-ttu-id="b9d9b-113">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning for indgående bilag**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="b9d9b-114">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="b9d9b-115">Som en del af konfigurationen skal du beslutte, om du vil kræve godkendelse af indgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-115">As part of the setup, you must decide if you want to require approval of incoming documents.</span></span> <span data-ttu-id="b9d9b-116">Hvis du vil kræve godkendelse, skal du oprette godkendere og godkendelsesworkflow.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-116">To require approval, you must set up approvers and approval workflows.</span></span> <span data-ttu-id="b9d9b-117">Hvis din organisation ikke ønsker at kræve godkendelse, kan du springe den næste sektion over.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-117">If your organization does not intend to require approval, you can skip the next section.</span></span>  

<span data-ttu-id="b9d9b-118">Hvis du bruger en tjeneste til at konvertere PDF- eller billedfiler, der repræsenterer indgående dokumenter, skal du konfigurere den.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-118">Finally, you if you use a service to convert PDF or image files representing incoming documents, you must it set up.</span></span> <span data-ttu-id="b9d9b-119">Ellers kan du også ignorere denne sektion.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-119">Otherwise, you can also skip that section.</span></span>  

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="b9d9b-120">Sådan konfigureres godkendere af indgående bilagsposter</span><span class="sxs-lookup"><span data-stu-id="b9d9b-120">To set up approvers of incoming document records</span></span>

<span data-ttu-id="b9d9b-121">Du kan også vælge at oprette en godkendelsesproces for de indgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-121">Optionally, set up an approval process for the incoming documents.</span></span> <span data-ttu-id="b9d9b-122">Godkendere af indgående bilag skal konfigureres som brugere i godkendelsesworkflow.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-122">Approvers of incoming documents must be set up as approval workflow users.</span></span>

<span data-ttu-id="b9d9b-123">Før du kan oprette workflows, der omfatter godkendelsestrin, skal du angive workflowbrugere, der er involveret i godkendelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-123">Before you can create workflows that involve approval steps, you must set up the workflow users who are involved in approval processes.</span></span> <span data-ttu-id="b9d9b-124">På siden **Konfiguration af godkendelsesbruger** skal du også angive beløbsgrænser for bestemte typer anmodninger og angive stedfortrædende godkendere, som godkendelsesanmodninger skal uddelegeres til, når den oprindelige godkender er fraværende.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-124">On the **Approval User Setup** page, you also set amount limits for specific types of requests and define substitute approvers to whom approval requests are delegated when the original approver is absent.</span></span> <span data-ttu-id="b9d9b-125">Du kan finde flere oplysninger i [Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)</span><span class="sxs-lookup"><span data-stu-id="b9d9b-125">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="b9d9b-126">Sådan konfigureres en OCR-tjeneste</span><span class="sxs-lookup"><span data-stu-id="b9d9b-126">To set up an OCR service</span></span>

1. <span data-ttu-id="b9d9b-127">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning af OCR-tjeneste**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="b9d9b-128">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-128">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="b9d9b-129">Dine logondata krypteres automatisk.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-129">You login data is automatically encrypted.</span></span>

<span data-ttu-id="b9d9b-130">Du kan finde flere oplysninger i [Bruge OCR til at gøre PDF- og billedfiler til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md).</span><span class="sxs-lookup"><span data-stu-id="b9d9b-130">For more information, see [Use OCR to Turn PDF and Image Files into Electronic Documents](across-how-use-ocr-pdf-images-files.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="b9d9b-131">Se også</span><span class="sxs-lookup"><span data-stu-id="b9d9b-131">See Also</span></span>

[<span data-ttu-id="b9d9b-132">Behandle indgående bilag</span><span class="sxs-lookup"><span data-stu-id="b9d9b-132">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="b9d9b-133">Indgående bilag</span><span class="sxs-lookup"><span data-stu-id="b9d9b-133">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="b9d9b-134">Køb</span><span class="sxs-lookup"><span data-stu-id="b9d9b-134">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="b9d9b-135">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b9d9b-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
