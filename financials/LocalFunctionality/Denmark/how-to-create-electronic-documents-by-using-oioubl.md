---
title: "Sådan oprettes elektroniske dokumenter ved hjælp af OIOUBL | Microsoft Docs"
description: "Når du sælger varer eller tjenesteydelser til en kunde i den offentlige sektor, skal du sende dokumenter elektronisk."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 6a524d65f3994ae882f9addd58c9c144defa7913
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-create-electronic-documents-by-using-oioubl"></a><span data-ttu-id="1bc63-103">Fremgangsmåde: Oprette elektroniske dokumenter ved hjælp af OIOUBL</span><span class="sxs-lookup"><span data-stu-id="1bc63-103">How to: Create Electronic Documents by Using OIOUBL</span></span>
<span data-ttu-id="1bc63-104">Når du sælger varer eller tjenesteydelser til en kunde i den offentlige sektor, skal du sende dokumenter elektronisk.</span><span class="sxs-lookup"><span data-stu-id="1bc63-104">When you sell goods or services to a customer in the public sector, you must submit documents electronically.</span></span> <span data-ttu-id="1bc63-105">I [!INCLUDE[d365fin](../../includes/d365fin_md.md)], kan du oprette elektroniske dokumenter til fakturaer, kreditnotaer, rykkere og rentenotaer.</span><span class="sxs-lookup"><span data-stu-id="1bc63-105">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can create electronic documents for invoices, credit memos, reminders, and finance charge memos.</span></span> <span data-ttu-id="1bc63-106">Før du kan oprette elektroniske dokumenter, skal du have angivet filplaceringer og oplysninger om kunderne.</span><span class="sxs-lookup"><span data-stu-id="1bc63-106">Before you can create the electronic documents, you must have set up file locations and information about the customers.</span></span> <span data-ttu-id="1bc63-107">Du kan få flere oplysninger i [Fremgangsmåde: Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md).</span><span class="sxs-lookup"><span data-stu-id="1bc63-107">For more information, see [How to: Set Up Customers for OIOUBL](how-to-set-up-customers-for-oioubl.md).</span></span>  

## <a name="creating-electronic-documents"></a><span data-ttu-id="1bc63-108">Oprettelse af elektroniske dokumenter</span><span class="sxs-lookup"><span data-stu-id="1bc63-108">Creating Electronic Documents</span></span>  
<span data-ttu-id="1bc63-109">Elektroniske dokumenter kan kun oprettes, når et dokument er bogført eller udstedt.</span><span class="sxs-lookup"><span data-stu-id="1bc63-109">Electronic documents can only be created after a document has been posted or issued.</span></span> <span data-ttu-id="1bc63-110">I følgende afsnit beskrives, hvordan du bogfører en salgsfaktura med de nødvendige oplysninger og derefter opretter en elektronisk salgsfaktura, men samme fremgangsmåde gælder for salgskreditnotaer, rykkere, rentenotaer, servicefakturaer og servicekreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="1bc63-110">The following sections describe how to post a sales invoice with the required information and then create an electronic sales invoice, but the same procedure applies to sales credit memos, reminders, finance charge memos, service invoices, and service credit memos.</span></span>  

### <a name="to-post-a-sales-invoice"></a><span data-ttu-id="1bc63-111">Sådan bogføres en salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="1bc63-111">To post a sales invoice</span></span>  

1.  <span data-ttu-id="1bc63-112">Vælg ikonet ![Søg efter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="1bc63-112">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1bc63-113">Åbn den salgsfaktura, som du vil bogføre.</span><span class="sxs-lookup"><span data-stu-id="1bc63-113">Open the sales invoice that you want to post.</span></span>  
3.  <span data-ttu-id="1bc63-114">I oversigtspanelet **Generelt** skal du kontrollere, at feltet **Eksternt bilagsnr.** indeholder nummeret på det dokument, kunden har leveret.</span><span class="sxs-lookup"><span data-stu-id="1bc63-114">On the **General** FastTab, make sure that the **External Document No.** field contains the document number that the customer supplied.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="1bc63-115">Dette er nødvendigt, hvis du vil oprette en elektronisk faktura.</span><span class="sxs-lookup"><span data-stu-id="1bc63-115">This is required if you want to create an electronic invoice.</span></span>  

    <span data-ttu-id="1bc63-116">For servicedokumenter skal du udfylde feltet **Din reference** i oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="1bc63-116">For service documents, you must fill in the **Your Reference** field on the **General** FastTab.</span></span>  

4.  <span data-ttu-id="1bc63-117">I oversigtspanelet **Fakturering** skal du sørge for, at følgende felter indeholder værdier:</span><span class="sxs-lookup"><span data-stu-id="1bc63-117">On the **Invoicing** FastTab, make sure that the following fields have values:</span></span>  

    -   <span data-ttu-id="1bc63-118">**EAN-nr.**</span><span class="sxs-lookup"><span data-stu-id="1bc63-118">**EAN No.**</span></span>  
    -   <span data-ttu-id="1bc63-119">**Kontokode**</span><span class="sxs-lookup"><span data-stu-id="1bc63-119">**Account Code**</span></span>  
    -   <span data-ttu-id="1bc63-120">**Betalingskanal**</span><span class="sxs-lookup"><span data-stu-id="1bc63-120">**Payment Channel**</span></span>  

    <span data-ttu-id="1bc63-121">Til rykkere og rentenotaer findes felterne i oversigtspanelet **Bogføring**.</span><span class="sxs-lookup"><span data-stu-id="1bc63-121">For reminders and finance charge memos, the fields are on the **Posting** FastTab.</span></span>  

5.  <span data-ttu-id="1bc63-122">Bogfør fakturaen.</span><span class="sxs-lookup"><span data-stu-id="1bc63-122">Post the invoice.</span></span>  

### <a name="to-create-an-electronic-sales-invoice"></a><span data-ttu-id="1bc63-123">Sådan oprettes en elektronisk salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="1bc63-123">To create an electronic sales invoice</span></span>  

1.  <span data-ttu-id="1bc63-124">Vælg ikonet ![Søg efter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogf. salgsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="1bc63-124">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Sales Invoices**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1bc63-125">Åbn den relevante bogførte salgsfaktura.</span><span class="sxs-lookup"><span data-stu-id="1bc63-125">Open the relevant posted sales invoice.</span></span>  
3.  <span data-ttu-id="1bc63-126">Vælg handlingen **Opret elektronisk faktura**.</span><span class="sxs-lookup"><span data-stu-id="1bc63-126">Choose the **Create Electronic Invoice** action.</span></span>  
4.  <span data-ttu-id="1bc63-127">I vinduet **Opret elektroniske fakturaer** skal du angive yderligere filtre og derefter vælge knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="1bc63-127">Optionally, in the **Create Electronic Invoices** window, set additional filters, and then choose the **OK** button.</span></span>  

<span data-ttu-id="1bc63-128">En XML-fil oprettes og gemmes på den lokation, som er defineret i vinduet **Salgsopsætning**.</span><span class="sxs-lookup"><span data-stu-id="1bc63-128">An XML file is created and stored at the location that was defined in the **Sales & Receivables Setup** window.</span></span> <span data-ttu-id="1bc63-129">Du kan nu sende dokumentet til kunden.</span><span class="sxs-lookup"><span data-stu-id="1bc63-129">You can now submit the document to the customer.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1bc63-130">Se også</span><span class="sxs-lookup"><span data-stu-id="1bc63-130">See Also</span></span>  
[<span data-ttu-id="1bc63-131">Lokal funktionalitet for Danmark</span><span class="sxs-lookup"><span data-stu-id="1bc63-131">Denmark Local Functionality</span></span>](denmark-local-functionality.md)  
 <span data-ttu-id="1bc63-132">[Fremgangsmåde: Konfigurere OIOUBL](how-to-set-up-oioubl.md) </span><span class="sxs-lookup"><span data-stu-id="1bc63-132">[How to: Set Up OIOUBL](how-to-set-up-oioubl.md) </span></span>  
 <span data-ttu-id="1bc63-133">[Fremgangsmåde: Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md) </span><span class="sxs-lookup"><span data-stu-id="1bc63-133">[How to: Set Up Customers for OIOUBL](how-to-set-up-customers-for-oioubl.md) </span></span>  
 [<span data-ttu-id="1bc63-134">Oversigt over elektronisk OIOUBL-fakturering</span><span class="sxs-lookup"><span data-stu-id="1bc63-134">OIOUBL Electronic Invoicing Overview</span></span>](oioubl-electronic-invoicing-overview.md)
