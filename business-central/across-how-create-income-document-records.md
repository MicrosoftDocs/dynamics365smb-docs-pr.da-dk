---
title: Oprette poster for indgående bilag | Microsoft Docs
description: Du kan oprette poster for indgående bilag, f.eks. e-fakturaer, og administrere OCR-opgaver eCommerce og dokumentudveksling.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 163b352e55ca85644bc833093f39ea8c422e5030
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3780581"
---
# <a name="create-incoming-document-records"></a><span data-ttu-id="95ff2-103">Oprette indgående bilagsposter</span><span class="sxs-lookup"><span data-stu-id="95ff2-103">Create Incoming Document Records</span></span>
<span data-ttu-id="95ff2-104">På siden **Indgående bilag** kan du bruge forskellige funktioner til at gennemgå udgiftsbilag, administrere OCR-opgaver og konvertere indgående bilagsfiler, manuelt eller automatisk, til de relevante købs- og salgsdokumenter eller kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="95ff2-104">On the **Incoming Documents** page, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="95ff2-105">Eksterne filer kan tilknyttes i enhver procesfase, herunder til bogførte dokumenter og til de derved oprettede kreditor-, debitor- og finansposter.</span><span class="sxs-lookup"><span data-stu-id="95ff2-105">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span>

<span data-ttu-id="95ff2-106">Når du vil registrere et eksternt dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du først oprette eller fuldføre en indgående bilagspost.</span><span class="sxs-lookup"><span data-stu-id="95ff2-106">To record an external document in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first create or complete an incoming document record.</span></span> <span data-ttu-id="95ff2-107">Du kan gøre dette manuelt, eller du kan tage et billede af det eksterne bilag og derefter oprette den indgående bilagspost med billedfilen vedhæftet.</span><span class="sxs-lookup"><span data-stu-id="95ff2-107">You can do this manually, or you can take a photo of the external document and then create the incoming document record with the image file attached.</span></span>

<span data-ttu-id="95ff2-108">Før du kan bruge funktionen Indgående bilag, skal du foretage den nødvendige opsætning.</span><span class="sxs-lookup"><span data-stu-id="95ff2-108">Before you can use the Incoming Documents feature, you must perform the required setup.</span></span> <span data-ttu-id="95ff2-109">Du kan finde flere oplysninger under [Konfigurere indgående bilag](across-how-setup-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="95ff2-109">For more information, see [Set Up Incoming Documents](across-how-setup-income-documents.md).</span></span>

## <a name="to-approve-or-reject-an-incoming-document"></a><span data-ttu-id="95ff2-110">Sådan godkendes eller afvises et indgående bilag</span><span class="sxs-lookup"><span data-stu-id="95ff2-110">To approve or reject an incoming document</span></span>
<span data-ttu-id="95ff2-111">Hvis du vil tillade brugere at oprette fakturaer eller finanskladdelinjer fra indgående bilagsposter, medmindre de er godkendt, kan du angive godkendere, der skal godkende posterne, før de kan behandles.</span><span class="sxs-lookup"><span data-stu-id="95ff2-111">If you do want to allow users to create invoices or general journal lines from incoming document records unless they are approved, you can set up approvers who must approve the records before they can be processed.</span></span>

1. <span data-ttu-id="95ff2-112">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Indgående bilag**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="95ff2-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Documents**, and then choose the related link.</span></span>
2. <span data-ttu-id="95ff2-113">Marker linjen i det dokument, du vil godkende eller afvise, og vælg derefter handlingen **Godkend** eller **Afvis**.</span><span class="sxs-lookup"><span data-stu-id="95ff2-113">Select the line with the document that you want to approve or reject, and then choose the **Approve** or **Reject** actions.</span></span>

<span data-ttu-id="95ff2-114">Hvis du godkender den indgående bilagspost, markeres afkrydsningsfeltet **Frigivet** på den indgående bilagslinje.</span><span class="sxs-lookup"><span data-stu-id="95ff2-114">If you approve the incoming document record, the **Released** check box on the incoming document line is selected.</span></span> <span data-ttu-id="95ff2-115">Brugeren, der har ansvaret for at godkende, f.eks, købsfakturaer, kan fortsætte med at behandle posten.</span><span class="sxs-lookup"><span data-stu-id="95ff2-115">The user in charge of creating, for example, purchase invoices can proceed to process the record.</span></span>

## <a name="to-create-an-incoming-document-record-by-taking-a-photo"></a><span data-ttu-id="95ff2-116">Sådan opretter du en indgående bilagspost ved at tage et billede</span><span class="sxs-lookup"><span data-stu-id="95ff2-116">To create an incoming document record by taking a photo</span></span>
> [!NOTE]  
>   <span data-ttu-id="95ff2-117">Følgende procedure gælder kun for [!INCLUDE[d365fin](includes/d365fin_md.md)] tablet- og telefonklienter.</span><span class="sxs-lookup"><span data-stu-id="95ff2-117">The following procedure only applies to the [!INCLUDE[d365fin](includes/d365fin_md.md)] Tablet and Phone clients.</span></span>

1. <span data-ttu-id="95ff2-118">På applinjen skal du vælge feltet **Opret indgående bilag fra kamera** og derefter gå til trin 4.</span><span class="sxs-lookup"><span data-stu-id="95ff2-118">On the app bar, choose the **Create Incoming Document from Camera** tile, and then go to step 4.</span></span>
2. <span data-ttu-id="95ff2-119">Du kan også vælge alternativknappen på applinjen, vælge **Indgående bilag** og derefter vælge **Alle**.</span><span class="sxs-lookup"><span data-stu-id="95ff2-119">Alternatively, on the app bar, choose the options button, choose **Incoming Documents**, and then choose **All**.</span></span>
3. <span data-ttu-id="95ff2-120">På siden **Indgående bilag** skal du vælge ellipseknappen og derefter vælge **Opret fra kamera**.</span><span class="sxs-lookup"><span data-stu-id="95ff2-120">On the **Incoming Documents** page, choose the ellipsis button, and then choose **Create from Camera**.</span></span> <span data-ttu-id="95ff2-121">Kameraet på tabletten eller telefonen aktiveres.</span><span class="sxs-lookup"><span data-stu-id="95ff2-121">The camera on the tablet or phone is activated.</span></span>
4. <span data-ttu-id="95ff2-122">Tag et billede af et dokument, f.eks en købsleverance, som du vil behandle som et indgående bilag, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="95ff2-122">Take a photo of a document, such as a purchase receipt, that you want to process as an incoming document, and then choose the **OK** button.</span></span>

    <span data-ttu-id="95ff2-123">Der oprettes en ny indgående bilagspost med billedet vedhæftet.</span><span class="sxs-lookup"><span data-stu-id="95ff2-123">A new incoming document record is created, with the image attached.</span></span>

## <a name="to-attach-an-image-to-an-incoming-document-record-by-taking-a-photo"></a><span data-ttu-id="95ff2-124">Sådan vedhæfter du et billede til en indgående bilagspost ved at tage et billede</span><span class="sxs-lookup"><span data-stu-id="95ff2-124">To attach an image to an incoming document record by taking a photo</span></span>
> [!NOTE]  
>   <span data-ttu-id="95ff2-125">Følgende procedure gælder kun for [!INCLUDE[d365fin](includes/d365fin_md.md)] tablet- og telefonklienter.</span><span class="sxs-lookup"><span data-stu-id="95ff2-125">The following procedure only applies to the [!INCLUDE[d365fin](includes/d365fin_md.md)] Tablet and Phone clients.</span></span>

1. <span data-ttu-id="95ff2-126">På applinjen skal du vælge alternativknappen, vælg **Indgående bilag** og vælg derefter **Alle**.</span><span class="sxs-lookup"><span data-stu-id="95ff2-126">On the app bar, choose the options button, choose **Incoming Documents**, and then choose **All**.</span></span>
2. <span data-ttu-id="95ff2-127">Åbn kortet for en eksisterende indgående bilagspost.</span><span class="sxs-lookup"><span data-stu-id="95ff2-127">Open the card for an existing incoming document record.</span></span>
3. <span data-ttu-id="95ff2-128">På siden **Indgående bilag** skal du vælge ellipseknappen og derefter vælge **Vedhæft billede fra kamera**.</span><span class="sxs-lookup"><span data-stu-id="95ff2-128">On the **Incoming Document** page, choose the ellipsis button, and then choose **Attach Image from Camera**.</span></span> <span data-ttu-id="95ff2-129">Kameraet på tabletten eller telefonen aktiveres.</span><span class="sxs-lookup"><span data-stu-id="95ff2-129">The camera on the tablet or phone is activated.</span></span>
4. <span data-ttu-id="95ff2-130">Tag et billede af et bilag, f.eks en købsleverance, som du vil behandle som et indgående bilag, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="95ff2-130">Take a photo of a document, such as a purchase receipt, that you want to process as an incoming document, and then choose the **OK** button.</span></span>

    <span data-ttu-id="95ff2-131">Billedet vedhæftes til den indgående bilagspost.</span><span class="sxs-lookup"><span data-stu-id="95ff2-131">The image is attached to the incoming document record.</span></span>

## <a name="to-create-an-incoming-document-record-manually"></a><span data-ttu-id="95ff2-132">Sådan oprettes en indgående bilagspost manuelt</span><span class="sxs-lookup"><span data-stu-id="95ff2-132">To create an incoming document record manually</span></span>
1. <span data-ttu-id="95ff2-133">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Indgående bilag**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="95ff2-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Documents**, and then choose the related link.</span></span>
2. <span data-ttu-id="95ff2-134">Vælg handlingen **Opret fra fil**.</span><span class="sxs-lookup"><span data-stu-id="95ff2-134">Choose the **Create from File** action.</span></span>  
3. <span data-ttu-id="95ff2-135">På siden **Indsæt fil** skal du vælge en fil og derefter klikke på **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="95ff2-135">On the **Insert File** page, select a file, and then choose **Open**.</span></span> <span data-ttu-id="95ff2-136">Filen vedhæftes automatisk.</span><span class="sxs-lookup"><span data-stu-id="95ff2-136">The file is automatically attached.</span></span>
4. <span data-ttu-id="95ff2-137">Du kan også vælge handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="95ff2-137">Alternatively, choose the **New** action.</span></span>
5. <span data-ttu-id="95ff2-138">Du kan vedhæfte en fil ved at vælge handlingen **Vedhæft fil**.</span><span class="sxs-lookup"><span data-stu-id="95ff2-138">To attach a file, choose the **Attach File** action.</span></span>
6. <span data-ttu-id="95ff2-139">På siden **Indsæt fil** , skal du vælge den fil, der repræsenterer det pågældende indgående bilag og derefter vælge knappen **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="95ff2-139">On the **Insert File** page, select the file that represents the incoming document in question, and then choose the **Open** button.</span></span>
7. <span data-ttu-id="95ff2-140">På siden **Indgående bilag** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="95ff2-140">On the **Incoming Document** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="95ff2-141">Se også</span><span class="sxs-lookup"><span data-stu-id="95ff2-141">See Also</span></span>
[<span data-ttu-id="95ff2-142">Behandle indgående bilag</span><span class="sxs-lookup"><span data-stu-id="95ff2-142">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="95ff2-143">Indgående bilag</span><span class="sxs-lookup"><span data-stu-id="95ff2-143">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="95ff2-144">Køb</span><span class="sxs-lookup"><span data-stu-id="95ff2-144">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="95ff2-145">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="95ff2-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
