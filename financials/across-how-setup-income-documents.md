---
title: "Konfigurere indgående dokumenter | Microsoft Docs"
description: "Du kan bruge funktionen Indgående dokumenter til at oprette elektroniske dokumenter, administrere OCR-opgaver, indlæse fakturaer og konvertere billedfiler."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ad534c9d60bbf3805f701eec6295084f6121a6d0
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="ccb63-103">Konfigurere indgående bilag</span><span class="sxs-lookup"><span data-stu-id="ccb63-103">Set Up Incoming Documents</span></span>
<span data-ttu-id="ccb63-104">Hvis du opretter finanskladdelinjer fra indgående dokumentposter, skal du i vinduet **Konfiguration af indkommende dokumenter** angive hvilken kladdetype og hvilket kladdenavn der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="ccb63-104">If you create general journal lines from incoming document records, you must specify in the **Incoming Documents Setup** window which journal template and batch to use.</span></span>

<span data-ttu-id="ccb63-105">Hvis du ikke ønsker, at brugere kan oprette fakturaer eller finanskladdelinjer fra indgående dokumentposter, medmindre dokumenterne godkendes, skal du konfigurere godkendere i vinduet **Konfiguration af indkommende dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="ccb63-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up approvers in the **Incoming Document Approvers** window.</span></span>

<span data-ttu-id="ccb63-106">Hvis du vil aktivere PDF-og billedfiler til elektroniske dokumenter, som du kan konvertere til f.eks. købsfakturaer, skal du først definere OCR-funktionen og aktivere tjenesten i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ccb63-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="ccb63-107">Når funktionen Indkommende dokumenter er konfigureret, kan du bruge forskellige funktioner til at gennemgå udgiftsbilag, administrere OCR-opgaver og konvertere indgående dokumentfiler, manuelt eller automatisk, til de relevante købs- og salgsdokumenter eller kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="ccb63-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="ccb63-108">Eksterne filer kan tilknyttes i enhver procesfase, herunder til bogførte dokumenter og til de derved oprettede kreditor-, debitor- og finansposter.</span><span class="sxs-lookup"><span data-stu-id="ccb63-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="ccb63-109">Du kan finde flere oplysninger i [Behandle indgående bilag](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="ccb63-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="ccb63-110">Sådan konfigureres funktionen for indgående dokumenter</span><span class="sxs-lookup"><span data-stu-id="ccb63-110">To set up the Incoming Documents feature</span></span>
1. <span data-ttu-id="ccb63-111">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opsætning af indgående bilag**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ccb63-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="ccb63-112">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="ccb63-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="ccb63-113">Sådan konfigureres godkendere af indgående dokumentposter</span><span class="sxs-lookup"><span data-stu-id="ccb63-113">To set up approvers of incoming document records</span></span>
1. <span data-ttu-id="ccb63-114">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opsætning af indgående bilag**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ccb63-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ccb63-115">I vinduet **Konfiguration af indkommende dokumenter** skal du vælge handlingen **Godkendere**.</span><span class="sxs-lookup"><span data-stu-id="ccb63-115">In the **Incoming Documents Setup** window, choose the **Approvers** action.</span></span>

    <span data-ttu-id="ccb63-116">Vinduet **Godkendere af indgående bilag** viser alle brugere, der er angivet i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ccb63-116">The **Incoming Document Approvers** window shows all users that are set up in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
3. <span data-ttu-id="ccb63-117">Vælg en eller flere brugere, der kan godkende et indgående dokument, før et relateret dokument eller en kladdelinje kan oprettes.</span><span class="sxs-lookup"><span data-stu-id="ccb63-117">Select one or more users that can approve an incoming document before a related document or journal line can be created.</span></span>

<span data-ttu-id="ccb63-118">Når godkendere er konfigureret i vinduet **Godkendere af indgående dokumenter**, så er det kun disse brugere, der kan godkende et indgående dokument, hvis afkrydsningsfeltet **Kræv godkendelse for at oprette** er markeret i vinduet **Konfiguration af indkommende dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="ccb63-118">When approvers have been set up in the **Incoming Document Approvers** window, only those users can approve an incoming document if the **Require Approval To Create** check box in the **Incoming Documents Setup** window is selected.</span></span>

> [!NOTE]  
>   <span data-ttu-id="ccb63-119">Denne godkenderopsætning er ikke relateret til godkendelsesworkflows.</span><span class="sxs-lookup"><span data-stu-id="ccb63-119">This approval setup is not related to approval workflows.</span></span> <span data-ttu-id="ccb63-120">Du kan finde flere oplysninger under [Bruge godkendelsesworkflows](across-how-use-approval-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="ccb63-120">For more information, see [Use Approval Workflows](across-how-use-approval-workflows.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="ccb63-121">Sådan konfigureres en OCR-tjeneste</span><span class="sxs-lookup"><span data-stu-id="ccb63-121">To set up an OCR service</span></span>
1. <span data-ttu-id="ccb63-122">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opsætning af indgående bilag**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ccb63-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="ccb63-123">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="ccb63-123">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-encrypt-your-login-information"></a><span data-ttu-id="ccb63-124">Sådan krypterer du logonoplysningerne</span><span class="sxs-lookup"><span data-stu-id="ccb63-124">To encrypt your login information</span></span>
<span data-ttu-id="ccb63-125">Det anbefales, at du beskytter de logonoplysninger, du angiver i vinduet **Opsætning af OCR-tjeneste**.</span><span class="sxs-lookup"><span data-stu-id="ccb63-125">It is recommended that you protect the logon information that you enter in the **OCR Service Setup** window.</span></span> <span data-ttu-id="ccb63-126">Du kan kryptere data på serveren ved at oprette nye eller importere eksisterende krypteringsnøgler, som du aktiverer på den serverforekomst, som opretter forbindelse til databasen.</span><span class="sxs-lookup"><span data-stu-id="ccb63-126">You can encrypt data on the server by generating new or importing existing encryption keys that you enable on the server instance that connects to the database.</span></span>

1. <span data-ttu-id="ccb63-127">I vinduet **Opsætning af OCR-tjeneste** skal du vælge handlingen **Administration af kryptering**.</span><span class="sxs-lookup"><span data-stu-id="ccb63-127">In the **OCR Service Setup** window, choose the **Encryption Management** action.</span></span>
2. <span data-ttu-id="ccb63-128">Aktiver kryptering af dine data i vinduet **Administration af datakryptering**.</span><span class="sxs-lookup"><span data-stu-id="ccb63-128">In the **Data Encryption Management** window, enable encryption of your data.</span></span>

## <a name="see-also"></a><span data-ttu-id="ccb63-129">Se også</span><span class="sxs-lookup"><span data-stu-id="ccb63-129">See Also</span></span>
[<span data-ttu-id="ccb63-130">Behandle indgående bilag</span><span class="sxs-lookup"><span data-stu-id="ccb63-130">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="ccb63-131">Indgående bilag</span><span class="sxs-lookup"><span data-stu-id="ccb63-131">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="ccb63-132">Køb</span><span class="sxs-lookup"><span data-stu-id="ccb63-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="ccb63-133">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ccb63-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

