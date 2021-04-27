---
title: Oprette elektroniske dokumenter i et OIOUBL-format | Microsoft Docs
description: Når du sælger varer eller tjenesteydelser til en kunde i den offentlige sektor i Danmark, skal du sende dokumenter elektronisk. I dette emne kan du læse, hvordan du gør dette.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 6830f9927b8f5b7aca1281f558c72d918913e2aa
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784059"
---
# <a name="create-electronic-documents-by-using-oioubl"></a><span data-ttu-id="13a98-104">Oprette elektroniske dokumenter ved hjælp af OIOUBL</span><span class="sxs-lookup"><span data-stu-id="13a98-104">Create Electronic Documents by Using OIOUBL</span></span>
<span data-ttu-id="13a98-105">Når du sælger varer eller tjenesteydelser til en kunde i den offentlige sektor, skal du sende dokumenter elektronisk.</span><span class="sxs-lookup"><span data-stu-id="13a98-105">When you sell goods or services to a customer in the public sector, you must submit documents electronically.</span></span> <span data-ttu-id="13a98-106">I [!INCLUDE[prod_short](../../includes/prod_short.md)], kan du oprette elektroniske dokumenter til fakturaer, kreditnotaer, rykkere og rentenotaer.</span><span class="sxs-lookup"><span data-stu-id="13a98-106">In [!INCLUDE[prod_short](../../includes/prod_short.md)], you can create electronic documents for invoices, credit memos, reminders, and finance charge memos.</span></span> <span data-ttu-id="13a98-107">Før du kan oprette elektroniske dokumenter, skal du have angivet filplaceringer og oplysninger om kunderne.</span><span class="sxs-lookup"><span data-stu-id="13a98-107">Before you can create the electronic documents, you must have set up file locations and information about the customers.</span></span> <span data-ttu-id="13a98-108">Du kan få flere oplysninger i [Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md).</span><span class="sxs-lookup"><span data-stu-id="13a98-108">For more information, see [Set Up Customers for OIOUBL](how-to-set-up-customers-for-oioubl.md).</span></span>  

<span data-ttu-id="13a98-109">Du kan oprette et elektronisk dokument, når du har bogført et salgs- eller servicedokument.</span><span class="sxs-lookup"><span data-stu-id="13a98-109">You can create an electronic document after you post the sales or service document.</span></span> <span data-ttu-id="13a98-110">I følgende afsnit beskrives, hvordan du bogfører en salgsfaktura med de nødvendige oplysninger og derefter opretter en elektronisk salgsfaktura, men samme fremgangsmåde gælder for salgs-og servicekreditnotaer og rykkere.</span><span class="sxs-lookup"><span data-stu-id="13a98-110">The following sections describe how to post a sales invoice with the required information and then create an electronic sales invoice, but the same procedure applies to sales and service credit memos and reminders.</span></span>  

## <a name="to-post-a-sales-invoice"></a><span data-ttu-id="13a98-111">Sådan bogføres en salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="13a98-111">To post a sales invoice</span></span>  
1.  <span data-ttu-id="13a98-112">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="13a98-112">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="13a98-113">Åbn den salgsfaktura, som du vil bogføre.</span><span class="sxs-lookup"><span data-stu-id="13a98-113">Open the sales invoice that you want to post.</span></span>  
3.  <span data-ttu-id="13a98-114">Kontrollér, at feltet **Eksternt bilagsnr.** indeholder nummeret på det dokument, kunden har leveret.</span><span class="sxs-lookup"><span data-stu-id="13a98-114">Make sure that the **External Document No.** field contains the document number that the customer supplied.</span></span> <span data-ttu-id="13a98-115">Elektroniske OIOUBL-dokumenter kræver dette nummer.</span><span class="sxs-lookup"><span data-stu-id="13a98-115">OIOUBL electronic documents require this number.</span></span>

    > [!Note]  
    > <span data-ttu-id="13a98-116">For servicedokumenter skal du udfylde feltet **Din reference**.</span><span class="sxs-lookup"><span data-stu-id="13a98-116">For service documents, you must fill in the **Your Reference** field.</span></span>  

4.  <span data-ttu-id="13a98-117">I oversigtspanelet **Fakturering** skal du udfylde felterne **GLN** og **OIOUB-kontokode**.</span><span class="sxs-lookup"><span data-stu-id="13a98-117">On the **Invoicing** FastTab, fill in the **GLN** and **OIOUBL Account Code** fields.</span></span>  

    <span data-ttu-id="13a98-118">Til rykkere og rentenotaer findes felterne i oversigtspanelet **Bogføring**.</span><span class="sxs-lookup"><span data-stu-id="13a98-118">For reminders and finance charge memos, the fields are on the **Posting** FastTab.</span></span>  

5.  <span data-ttu-id="13a98-119">Bogfør fakturaen.</span><span class="sxs-lookup"><span data-stu-id="13a98-119">Post the invoice.</span></span>  

## <a name="to-create-an-electronic-sales-invoice"></a><span data-ttu-id="13a98-120">Sådan oprettes en elektronisk salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="13a98-120">To create an electronic sales invoice</span></span>  
<span data-ttu-id="13a98-121">Når du har bogført et dokument, kan du oprette en elektronisk faktura i OIOUBL-format.</span><span class="sxs-lookup"><span data-stu-id="13a98-121">After you post a document, you can create an electronic invoice in an OIOUBL format.</span></span> <span data-ttu-id="13a98-122">Nedenfor beskrives processen for bogførte salgsfakturaer, men proceduren er den samme for andre dokumenter.</span><span class="sxs-lookup"><span data-stu-id="13a98-122">The following steps describe the process for posted sales invoices, but the process is the same for other documents.</span></span>

1.  <span data-ttu-id="13a98-123">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bogførte salgsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="13a98-123">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Sales Invoices**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="13a98-124">Åbn den relevante bogførte salgsfaktura.</span><span class="sxs-lookup"><span data-stu-id="13a98-124">Open the relevant posted sales invoice.</span></span>  
3.  <span data-ttu-id="13a98-125">Vælg handlingen **Opret elektronisk <*dokumenttype*>**.</span><span class="sxs-lookup"><span data-stu-id="13a98-125">Choose the **Create Electronic <*document type*>** action.</span></span>  
4.  <span data-ttu-id="13a98-126">På siden **Opret elektronisk <*dokumenttype*>** kan du angive yderligere filtre og derefter vælge knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="13a98-126">Optionally, in the **Create Electronic <*document type*>** page, set additional filters, and then choose the **OK** button.</span></span>  

<span data-ttu-id="13a98-127">Derved oprettes en XML-fil, der gemmes på standardplaceringen for hentning på din enhed.</span><span class="sxs-lookup"><span data-stu-id="13a98-127">This generates an XML file that is stored at the default download location on your device.</span></span>


> [!Note]
> <span data-ttu-id="13a98-128">Med onlineversionen af Business Central oprettes XML-filen automatisk i mappen med overførsler på pc'en.</span><span class="sxs-lookup"><span data-stu-id="13a98-128">With the online version of Business Central, the XML file is automatically created in the Download folder on the pc.</span></span>

## <a name="see-also"></a><span data-ttu-id="13a98-129">Se også</span><span class="sxs-lookup"><span data-stu-id="13a98-129">See Also</span></span>  
[<span data-ttu-id="13a98-130">Lokal funktionalitet for Danmark</span><span class="sxs-lookup"><span data-stu-id="13a98-130">Denmark Local Functionality</span></span>](denmark-local-functionality.md)  
 <span data-ttu-id="13a98-131">[Konfigurere OIOUBL](how-to-set-up-oioubl.md) </span><span class="sxs-lookup"><span data-stu-id="13a98-131">[Set Up OIOUBL](how-to-set-up-oioubl.md) </span></span>  
 <span data-ttu-id="13a98-132">[Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md) </span><span class="sxs-lookup"><span data-stu-id="13a98-132">[Set Up Customers for OIOUBL](how-to-set-up-customers-for-oioubl.md) </span></span>  
 [<span data-ttu-id="13a98-133">Oversigt over elektronisk OIOUBL-fakturering</span><span class="sxs-lookup"><span data-stu-id="13a98-133">OIOUBL Electronic Invoicing Overview</span></span>](oioubl-electronic-invoicing-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]