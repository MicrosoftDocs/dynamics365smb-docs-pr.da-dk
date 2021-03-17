---
title: Sende elektroniske dokumenter
description: Lær, hvordan du sender fakturaer elektronisk.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d547f031d9d33c0d7cd5f8b20398fd7b6dbe0393
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382996"
---
# <a name="send-electronic-documents"></a><span data-ttu-id="abf8b-103">Sende elektroniske dokumenter</span><span class="sxs-lookup"><span data-stu-id="abf8b-103">Send Electronic Documents</span></span>

<span data-ttu-id="abf8b-104">Den generiske version af [!INCLUDE[prod_short](includes/prod_short.md)] understøtter afsendelse af elektroniske fakturaer og kreditnotaer i PEPPOL-formatet, som understøttes af de største udbydere af dokumentudvekslingstjenester.</span><span class="sxs-lookup"><span data-stu-id="abf8b-104">The generic version of [!INCLUDE[prod_short](includes/prod_short.md)] supports sending electronic invoices and credit memos in the PEPPOL format, a format that the largest document exchange service providers support.</span></span> <span data-ttu-id="abf8b-105">En udbyder af dokumentudvekslingstjenester sender elektroniske dokumenter mellem handelspartnere.</span><span class="sxs-lookup"><span data-stu-id="abf8b-105">A document exchange service provider dispatches electronic documents between trading partners.</span></span> <span data-ttu-id="abf8b-106">For at understøtte andre elektroniske dokumentformater kan du bruge dataudvekslingsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="abf8b-106">To provide support for other electronic document formats, you use the data exchange framework.</span></span>  

 <span data-ttu-id="abf8b-107">I den generiske version af [!INCLUDE[prod_short](includes/prod_short.md)] er en dokumentudvekslingstjeneste forudkonfigureret og klar til at blive konfigureret til din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="abf8b-107">In the generic version of [!INCLUDE[prod_short](includes/prod_short.md)], a document exchange service is preconfigured and ready to be set up for your company.</span></span> <span data-ttu-id="abf8b-108">Du kan finde flere oplysninger i [Konfigurere en dokumentudvekslingstjeneste](across-how-to-set-up-a-document-exchange-service.md).</span><span class="sxs-lookup"><span data-stu-id="abf8b-108">For more information, see [Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).</span></span> <span data-ttu-id="abf8b-109">Du skal imidlertid installere en app i nogle tilfælde.</span><span class="sxs-lookup"><span data-stu-id="abf8b-109">However, in some cases, you must install an app.</span></span> <span data-ttu-id="abf8b-110">Du kan finde flere oplysninger i [Ofte stillede spørgsmål til Oversigt over elektronisk fakturering](faq-electronic-invoicing.yml).</span><span class="sxs-lookup"><span data-stu-id="abf8b-110">For more information, see [Electronic Invoicing FAQ](faq-electronic-invoicing.yml).</span></span>  

 <span data-ttu-id="abf8b-111">Når du vil sende en salgsfaktura som et elektronisk PEPPOL dokument, skal du vælge indstillingen **Elektronisk dokument** i dialogboksen **Bogfør og send**.</span><span class="sxs-lookup"><span data-stu-id="abf8b-111">To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box.</span></span> <span data-ttu-id="abf8b-112">Herfra kan du også angive debitorens standardprofil for afsendelse af dokumenter.</span><span class="sxs-lookup"><span data-stu-id="abf8b-112">You can also set up the customer's default document sending profile from that dialog box.</span></span> <span data-ttu-id="abf8b-113">Først skal du konfigurere forskellige stamdata, såsom firmaoplysninger, debitorer, varer og enheder.</span><span class="sxs-lookup"><span data-stu-id="abf8b-113">First, you must set up various master data, such as company information, customers, items, and units of measure.</span></span> <span data-ttu-id="abf8b-114">Disse bruges til at identificere forretningspartnere og varer ved konvertering af data i felterne i [Konfigurere afsendelse og modtagelse af elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="abf8b-114">These are used to identify the business partners and items when converting data in fields in [Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span></span>  

### <a name="to-send-an-electronic-sales-invoice"></a><span data-ttu-id="abf8b-115">Sådan sendes en elektronisk salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="abf8b-115">To send an electronic sales invoice</span></span>

1. <span data-ttu-id="abf8b-116">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="abf8b-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  

2. <span data-ttu-id="abf8b-117">Opret en ny salgsfaktura.</span><span class="sxs-lookup"><span data-stu-id="abf8b-117">Create a new sales invoice.</span></span>  

3. <span data-ttu-id="abf8b-118">Når salgsfakturaerne er klar til at blive faktureret, skal du vælge handlingen **Bogfør og send**.</span><span class="sxs-lookup"><span data-stu-id="abf8b-118">When the sales invoice is ready to be invoiced, choose the **Post and Send** action.</span></span>  

     <span data-ttu-id="abf8b-119">Hvis debitorens standardprofil til afsendelse er **Elektronisk dokument**, vises det i dialogboksen **Bekræftelse af bogfør og send**.</span><span class="sxs-lookup"><span data-stu-id="abf8b-119">If the customer's default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box.</span></span> <span data-ttu-id="abf8b-120">På den måde behøver du kun at vælge knappen **Ja** for at bogføre og sende fakturaen elektronisk i det valgte format.</span><span class="sxs-lookup"><span data-stu-id="abf8b-120">This way, you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.</span></span>  

4. <span data-ttu-id="abf8b-121">I dialogboksen **Bekræftelse af bogfør og send** skal du vælge knappen AssistEdit til højre for feltet **Send bilag til**.</span><span class="sxs-lookup"><span data-stu-id="abf8b-121">In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.</span></span>  

5. <span data-ttu-id="abf8b-122">I **Send dokument til** dialogboksen og i feltet **Elektronisk dokument** skal du vælge **Via dokumentudvekslingstjeneste**.</span><span class="sxs-lookup"><span data-stu-id="abf8b-122">In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.</span></span>  

6. <span data-ttu-id="abf8b-123">I feltet **Format** skal du vælge **PEPPOL**.</span><span class="sxs-lookup"><span data-stu-id="abf8b-123">In the **Format** field, choose **PEPPOL**.</span></span>  

7. <span data-ttu-id="abf8b-124">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="abf8b-124">Choose the **OK** button.</span></span> <span data-ttu-id="abf8b-125">Dialogboksen **Bekræftelse af bogfør og send** vises.</span><span class="sxs-lookup"><span data-stu-id="abf8b-125">The **Post and Send Confirmation** dialog box appears.</span></span> <span data-ttu-id="abf8b-126">**Elektronisk dokument (PEPPOL)** føjes til feltet **Send dokument til**.</span><span class="sxs-lookup"><span data-stu-id="abf8b-126">**Electronic Document (PEPPOL)** is added to the **Send Document to** field.</span></span>  

8. <span data-ttu-id="abf8b-127">Vælg knappen **Ja**.</span><span class="sxs-lookup"><span data-stu-id="abf8b-127">Choose the **Yes** button.</span></span>  

     <span data-ttu-id="abf8b-128">Salgsfakturaen bogføres og sendes til kunden som et elektronisk dokument i PEPPOL-format.</span><span class="sxs-lookup"><span data-stu-id="abf8b-128">The sales invoice is posted and sent to the customer in the PEPPOL format.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="abf8b-129">Du kan også sende en bogført salgsfaktura som et elektronisk dokument.</span><span class="sxs-lookup"><span data-stu-id="abf8b-129">You can also send a posted sales invoice as an electronic document.</span></span> <span data-ttu-id="abf8b-130">Fremgangsmåden er den samme som beskrevet i dette emne for ikke-bogførte salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="abf8b-130">The procedure is the same as described in this topic for non-posted sales documents.</span></span> <span data-ttu-id="abf8b-131">På siden **Bogført salgsfaktura** skal du vælge handlingen **Aktivitetslog** for at få vist statussen for det elektroniske dokument.</span><span class="sxs-lookup"><span data-stu-id="abf8b-131">On the **Posted Sales Invoice** page, choose the **Activity Log** action to view the status of the electronic document.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="abf8b-132">Se relateret oplæring på [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="abf8b-132">See Related Training at [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="abf8b-133">Se også</span><span class="sxs-lookup"><span data-stu-id="abf8b-133">See Also</span></span>

[<span data-ttu-id="abf8b-134">Fakturere salg</span><span class="sxs-lookup"><span data-stu-id="abf8b-134">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="abf8b-135">Konfigurere dokumentafsendelsesprofiler</span><span class="sxs-lookup"><span data-stu-id="abf8b-135">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md)  
[<span data-ttu-id="abf8b-136">Konfigurere afsendelse og modtagelse af elektroniske dokumenter</span><span class="sxs-lookup"><span data-stu-id="abf8b-136">Set Up Electronic Document Sending and Receiving</span></span>](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[<span data-ttu-id="abf8b-137">Konfigurere en dokumentudvekslingstjeneste</span><span class="sxs-lookup"><span data-stu-id="abf8b-137">Set Up a Document Exchange Service</span></span>](across-how-to-set-up-a-document-exchange-service.md)  
[<span data-ttu-id="abf8b-138">Konfigurere dataudvekslingsdefinitioner</span><span class="sxs-lookup"><span data-stu-id="abf8b-138">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="abf8b-139">Udveksle data elektronisk</span><span class="sxs-lookup"><span data-stu-id="abf8b-139">Exchanging Data Electronically</span></span>](across-data-exchange.md)  
[<span data-ttu-id="abf8b-140">Ofte stillede spørgsmål om elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="abf8b-140">Electronic Invoicing FAQ</span></span>](faq-electronic-invoicing.yml)  
[<span data-ttu-id="abf8b-141">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="abf8b-141">General Business Functionality</span></span>](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]