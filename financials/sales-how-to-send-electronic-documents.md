---
title: Sende elektroniske dokumenter | Microsoft Docs
description: "Lær, hvordan du sender fakturaer elektronisk."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c41e8c59ced776591b1740930effa2420803eb65
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-send-electronic-documents"></a><span data-ttu-id="f3332-103">Fremgangsmåde: Sende elektroniske dokumenter</span><span class="sxs-lookup"><span data-stu-id="f3332-103">How to: Send Electronic Documents</span></span>
<span data-ttu-id="f3332-104">Den generiske version af [!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter afsendelse af elektroniske fakturaer og kreditnotaer i PEPPOL-formatet, som understøttes af de største udbydere af dokumentudvekslingstjenester.</span><span class="sxs-lookup"><span data-stu-id="f3332-104">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] supports sending electronic invoices and credit memos in the PEPPOL format, which is supported by the largest document exchange service providers.</span></span> <span data-ttu-id="f3332-105">En udbyder af dokumentudvekslingstjenester sender elektroniske dokumenter mellem handelspartnere.</span><span class="sxs-lookup"><span data-stu-id="f3332-105">A document exchange service provider dispatches electronic documents between trading partners.</span></span> <span data-ttu-id="f3332-106">For at understøtte andre elektroniske dokumentformater kan du bruge dataudvekslingsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="f3332-106">To provide support for other electronic document formats, you use the data exchange framework.</span></span>  

 <span data-ttu-id="f3332-107">I den generiske version af [!INCLUDE[d365fin](includes/d365fin_md.md)] er en dokumentudvekslingstjeneste forudkonfigureret og klar til at blive konfigureret til din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="f3332-107">In the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)], a document exchange service is preconfigured and ready to be set up for your company.</span></span> <span data-ttu-id="f3332-108">Du kan finde flere oplysninger i [Fremgangsmåde: Konfigurere en dokumentudvekslingstjeneste](across-how-to-set-up-a-document-exchange-service.md).</span><span class="sxs-lookup"><span data-stu-id="f3332-108">For more information, see [How to: Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).</span></span>  

 <span data-ttu-id="f3332-109">For at sende en salgsfaktura som et elektronisk PEPPOL-dokument skal du vælge indstillingen **Elektronisk dokument** i dialogboksen **Bogfør og send**, hvor du også kan konfigurere kundens standardprofil til afsendelse af dokumenter.</span><span class="sxs-lookup"><span data-stu-id="f3332-109">To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box from where you can also set up the customer’s default document sending profile.</span></span> <span data-ttu-id="f3332-110">Først skal du konfigurere forskellige stamdata, såsom firmaoplysninger, debitorer, varer og enheder.</span><span class="sxs-lookup"><span data-stu-id="f3332-110">First, you must set up various master data, such as company information, customers, items, and units of measure.</span></span> <span data-ttu-id="f3332-111">Disse bruges til at identificere forretningspartnere og varer ved konvertering af data i felterne i [Fremgangsmåde: Konfigurere afsendelse og modtagelse af elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="f3332-111">These are used to identify the business partners and items when converting data in fields in [How to: Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span></span>  

### <a name="to-send-an-electronic-sales-invoice"></a><span data-ttu-id="f3332-112">Sådan sendes en elektronisk salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="f3332-112">To send an electronic sales invoice</span></span>  

1.  <span data-ttu-id="f3332-113">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f3332-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="f3332-114">Opret en ny salgsfaktura.</span><span class="sxs-lookup"><span data-stu-id="f3332-114">Create a new sales invoice.</span></span>  

3.  <span data-ttu-id="f3332-115">Når salgsfakturaen er klar til blive faktureret, skal du bruge fanen **Handlinger** i gruppen **Bogføring** og vælge **Bogfør og send**.</span><span class="sxs-lookup"><span data-stu-id="f3332-115">When the sales invoice is ready to be invoiced, on the **Actions** tab, in the **Posting** group, choose **Post and Send**.</span></span>  

     <span data-ttu-id="f3332-116">Hvis kundens standardafsendelsesprofil er **Elektronisk dokument**, bliver den vist i dialogboksen **Bekræftelse af bogfør og send**, og du skal bare klikke på knappen **Ja** for at bogføre og sende fakturaen elektronisk i det valgte format.</span><span class="sxs-lookup"><span data-stu-id="f3332-116">If the customer’s default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box and you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.</span></span>  

4.  <span data-ttu-id="f3332-117">I dialogboksen **Bekræftelse af bogfør og send** skal du vælge knappen AssistEdit til højre for feltet **Send bilag til**.</span><span class="sxs-lookup"><span data-stu-id="f3332-117">In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.</span></span>  

5.  <span data-ttu-id="f3332-118">I **Send dokument til** dialogboksen og i feltet **Elektronisk dokument** skal du vælge **Via dokumentudvekslingstjeneste**.</span><span class="sxs-lookup"><span data-stu-id="f3332-118">In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.</span></span>  

6.  <span data-ttu-id="f3332-119">I feltet **Format** skal du vælge **PEPPOL**.</span><span class="sxs-lookup"><span data-stu-id="f3332-119">In the **Format** field, choose **PEPPOL**.</span></span>  

7.  <span data-ttu-id="f3332-120">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="f3332-120">Choose the **OK** button.</span></span> <span data-ttu-id="f3332-121">Dialogboksen **Bekræftelse af bogfør og send** vises.</span><span class="sxs-lookup"><span data-stu-id="f3332-121">The **Post and Send Confirmation** dialog box appears.</span></span> <span data-ttu-id="f3332-122">**Elektronisk dokument (PEPPOL)** føjes til feltet **Send dokument til**.</span><span class="sxs-lookup"><span data-stu-id="f3332-122">**Electronic Document (PEPPOL)** is added to the **Send Document to** field.</span></span>  

8.  <span data-ttu-id="f3332-123">Vælg knappen **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f3332-123">Choose the **Yes** button.</span></span>  

     <span data-ttu-id="f3332-124">Salgsfakturaen bogføres og sendes til kunden som et elektronisk dokument i PEPPOL-format.</span><span class="sxs-lookup"><span data-stu-id="f3332-124">The sales invoice is posted and sent to the customer as an electronic document in the PEPPOL format.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="f3332-125">Du kan også sende en bogført salgsfaktura som et elektronisk dokument.</span><span class="sxs-lookup"><span data-stu-id="f3332-125">You can also send a posted sales invoice as an electronic document.</span></span> <span data-ttu-id="f3332-126">Fremgangsmåden er den samme som beskrevet i dette emne for ikke-bogførte salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="f3332-126">The procedure is the same as described in this topic for non-posted sales documents.</span></span> <span data-ttu-id="f3332-127">I vinduet **Bogført salgsfaktura** under fanen **Handlinger** i gruppen **Generelt** skal du vælge **Aktivitetslog** for at få vist status for det elektroniske dokument.</span><span class="sxs-lookup"><span data-stu-id="f3332-127">In the **Posted Sales Invoice** window, on the **Actions** tab, in the **General** group, choose **Activity Log** to view the status of the electronic document.</span></span> <span data-ttu-id="f3332-128">Du kan finde flere oplysninger **Aktivitetslog**.</span><span class="sxs-lookup"><span data-stu-id="f3332-128">For more information, see **Activity Log**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f3332-129">Se også</span><span class="sxs-lookup"><span data-stu-id="f3332-129">See Also</span></span>  
[<span data-ttu-id="f3332-130">Fremgangsmåde: Fakturere salg</span><span class="sxs-lookup"><span data-stu-id="f3332-130">How to: Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="f3332-131">Fremgangsmåde: Konfigurere dokumentafsendelsesprofiler</span><span class="sxs-lookup"><span data-stu-id="f3332-131">How to: Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md)  
[<span data-ttu-id="f3332-132">Fremgangsmåde: Konfigurere afsendelse og modtagelse af elektroniske dokumenter</span><span class="sxs-lookup"><span data-stu-id="f3332-132">How to: Set Up Electronic Document Sending and Receiving</span></span>](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[<span data-ttu-id="f3332-133">Fremgangsmåde: Konfigurere en dokumentudvekslingstjeneste</span><span class="sxs-lookup"><span data-stu-id="f3332-133">How to: Set Up a Document Exchange Service</span></span>](across-how-to-set-up-a-document-exchange-service.md)  
[<span data-ttu-id="f3332-134">Fremgangsmåde: Konfigurere dataudvekslingsdefinitioner</span><span class="sxs-lookup"><span data-stu-id="f3332-134">How to: Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="f3332-135">Udveksle data som elektroniske dokumenter</span><span class="sxs-lookup"><span data-stu-id="f3332-135">Exchanging Data as Electronic Documents</span></span>](across-data-exchange.md)  
[<span data-ttu-id="f3332-136">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="f3332-136">General Business Functionality</span></span>](ui-across-business-areas.md)  

