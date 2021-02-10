---
title: Føje vedhæftede filer, links og noter til poster | Microsoft Docs
description: Indsæt et hyperlink i et dokument eller websted til en bestemt post, f.eks. en debitor eller et dokument.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0d13ffa03e4a123158e2f350ff9eab5e274741b5
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760563"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a><span data-ttu-id="359d6-103">Administrere vedhæftede filer, links og noter på kort og dokumenter</span><span class="sxs-lookup"><span data-stu-id="359d6-103">Manage Attachments, Links, and Notes on Cards and Documents</span></span>

<span data-ttu-id="359d6-104">I faktaboksen på de fleste kort og i dokumenter kan du vedhæfte filer, tilføje links og skrive noter.</span><span class="sxs-lookup"><span data-stu-id="359d6-104">In the FactBox on most cards and documents, you can attach files, add links, and write notes.</span></span> <span data-ttu-id="359d6-105">Ved links og noter kan du også gøre dette på listesiden ved først at vælge den relaterede linje.</span><span class="sxs-lookup"><span data-stu-id="359d6-105">For links and notes, you can also do this on the list page by first selecting the related line.</span></span>

<span data-ttu-id="359d6-106">Hvis du vil have vist eller ændre nogen af disse typer vedhæftede oplysninger, skal du først åbne fanen **Vedhæftede filer** i faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="359d6-106">To view or change any of these attached information types, you must first open the **Attachments** tab in the FactBox.</span></span> <span data-ttu-id="359d6-107">Nummeret bag fanetitlen angiver, hvor mange vedhæftede filer, links eller noter der findes for kortet eller dokumentet.</span><span class="sxs-lookup"><span data-stu-id="359d6-107">The number behind the tab title indicates how many attached files, links, or notes exist for the card or document.</span></span>

<span data-ttu-id="359d6-108">Vedhæftede filer, links og noter forbliver tilknyttede, når kortet eller dokumentet behandles i andre tilstande, f.eks. fra en igangværende salgsordre til en bogført salgsfaktura.</span><span class="sxs-lookup"><span data-stu-id="359d6-108">Attachments, links, and notes stay attached as the card or document is processed into other states, such as from an ongoing sales order to a posted sales invoice.</span></span> <span data-ttu-id="359d6-109">Ingen af de vedhæftede filtyper er dog output fra systemet, f.eks. ved udskrivning eller lagring til en fil.</span><span class="sxs-lookup"><span data-stu-id="359d6-109">However, none of the attachment types are output from the system, for example, when printing or when saving to a file.</span></span>

> [!NOTE]
> <span data-ttu-id="359d6-110">Når du delvist sender og fakturerer en salgsordre eller indkøbsordre, knyttes den vedhæftede fil kun til den endelige faktura for den pågældende ordre.</span><span class="sxs-lookup"><span data-stu-id="359d6-110">When you partially ship and invoice a sales order or purchase order, the attachment will only be attached to the final invoice of that order.</span></span> <span data-ttu-id="359d6-111">På samme måde knyttes den vedhæftede fil kun til finansposterne for dokumentet, men ikke til periodiseringsposterne, når du fakturerer ved hjælp af funktionen Udskydelser.</span><span class="sxs-lookup"><span data-stu-id="359d6-111">Likewise, when you invoice using the Deferrals feature, the attachment is only attached to the G/L entries for the document but not for the deferral entries.</span></span>

## <a name="to-attach-a-file-to-a-purchase-invoice"></a><span data-ttu-id="359d6-112">Sådan vedhæftes en fil til en købsfaktura</span><span class="sxs-lookup"><span data-stu-id="359d6-112">To attach a file to a purchase invoice</span></span>
<span data-ttu-id="359d6-113">Du kan vedhæfte alle filtyper, der indeholder tekst, billeder eller video, på et kort eller et dokument.</span><span class="sxs-lookup"><span data-stu-id="359d6-113">You can attach any type of file, containing text, image, or video, to a card or document.</span></span> <span data-ttu-id="359d6-114">Det er nyttigt, når du f.eks. vil gemme en kreditorfaktura som PDF-fil på den relaterede købsfaktura i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="359d6-114">This is useful, for example, when you want to store a vendor's invoice as a PDF file on the related purchase invoice in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="359d6-115">Filer, der er vedhæftet med funktionen Indgående bilag, medtages ikke under fanen **Vedhæftede filer**. Du kan finde flere oplysninger i [Indgående bilag](across-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="359d6-115">Files attached with the Incoming Documents feature are not included on the **Attachments** tab. For more information, see [Incoming Documents](across-income-documents.md).</span></span>

<span data-ttu-id="359d6-116">Følgende procedure er baseret på en købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="359d6-116">The following procedure is based on a purchase invoice.</span></span> <span data-ttu-id="359d6-117">Trinene er de samme for alle andre understøttede dokumenter og kort.</span><span class="sxs-lookup"><span data-stu-id="359d6-117">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="359d6-118">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="359d6-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="359d6-119">Åbn den salgsordre, som du vil vedhæfte en fil til.</span><span class="sxs-lookup"><span data-stu-id="359d6-119">Open the sales order that you want to attach a file to.</span></span>
3. <span data-ttu-id="359d6-120">Åbn fanen **Vedhæftede filer** i faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="359d6-120">In the FactBox, open the **Attachments** tab.</span></span>
4. <span data-ttu-id="359d6-121">Vælg værdien bag feltet **Dokumenter**, f.eks. "0".</span><span class="sxs-lookup"><span data-stu-id="359d6-121">Choose the value behind the **Documents** field, such as "0".</span></span>
5. <span data-ttu-id="359d6-122">På siden **Vedhæftede bilag** i feltet **Vedhæftet fil** skal du vælge handlingen **Vælg fil**.</span><span class="sxs-lookup"><span data-stu-id="359d6-122">On the **Attached Documents** page, in the **Attachment** field, choose the **Select File** action.</span></span>
5. <span data-ttu-id="359d6-123">Vælg en fil fra en placering, og vælg derefter knappen **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="359d6-123">Select a file from any location, and then choose the **Open** button.</span></span>

<span data-ttu-id="359d6-124">Filen er nu vedhæftet til købsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="359d6-124">The file is now attached to the purchase invoice.</span></span>

## <a name="to-view-an-attached-file"></a><span data-ttu-id="359d6-125">Sådan ser du en vedhæftet fil</span><span class="sxs-lookup"><span data-stu-id="359d6-125">To view an attached file</span></span>
1. <span data-ttu-id="359d6-126">Åbn fanen **Vedhæftede filer** i faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="359d6-126">In the FactBox, open the **Attachments** tab.</span></span>
2. <span data-ttu-id="359d6-127">Vælg værdien bag feltet **Dokumenter**, f.eks. "1".</span><span class="sxs-lookup"><span data-stu-id="359d6-127">Choose the value behind the **Documents** field, such as "1".</span></span>
3. <span data-ttu-id="359d6-128">På siden **Vedhæftede bilag** skal du vælge handlingen **Eksempel**.</span><span class="sxs-lookup"><span data-stu-id="359d6-128">On the **Attached Documents** page, choose the **Preview** action.</span></span>
4. <span data-ttu-id="359d6-129">Åbne den overførte file.</span><span class="sxs-lookup"><span data-stu-id="359d6-129">Open the downloaded file.</span></span>

## <a name="to-save-a-document-as-a-pdf-attachment"></a><span data-ttu-id="359d6-130">Sådan gemmer du et dokument som en vedhæftet PDF-fil</span><span class="sxs-lookup"><span data-stu-id="359d6-130">To save a document as a PDF attachment</span></span>
<span data-ttu-id="359d6-131">Når du har brug for at gemme et dokument som en fil, kan du bruge handlingen **Vedhæft som PDF** til at hente det aktuelle dokumentindhold som en PDF-fil, der er vedhæftet dokumentets faktaboks.</span><span class="sxs-lookup"><span data-stu-id="359d6-131">Whenever you need to save a document as a file, you can use the **Attach as PDF** action to capture the current document content as a PDF file attached to the FactBox of the document.</span></span> <span data-ttu-id="359d6-132">Det er f. eks. nyttigt, når dokumenter følger flere trin i en proces, f. eks. en salgsproces eller en godkendelsesproces, og du vil henvise til en udskrift af det forrige trin.</span><span class="sxs-lookup"><span data-stu-id="359d6-132">This is useful, for example, when documents follow multiple steps in a process, such as a sales process or an approval workflow, and you want to refer to a printout of the previous step.</span></span>

<span data-ttu-id="359d6-133">Følgende procedure er baseret på en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="359d6-133">The following procedure is based on a sales order.</span></span> <span data-ttu-id="359d6-134">Fremgangsmåden er den samme for alle understøttede dokumenter.</span><span class="sxs-lookup"><span data-stu-id="359d6-134">The steps are similar for all supported documents.</span></span>

1. <span data-ttu-id="359d6-135">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordre**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="359d6-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="359d6-136">Vælg en salgsordre, og vælg derefter handlingen **Vedhæft som PDF**.</span><span class="sxs-lookup"><span data-stu-id="359d6-136">Select a sales order, and then choose the **Attach as PDF** action.</span></span>

<span data-ttu-id="359d6-137">En PDF-fil med det aktuelle indhold i salgsordren tilføjes på fanen **Vedhæftede filer** i faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="359d6-137">A PDF file with the current content of the sales order is added to the **Attachments** tab in the FactBox.</span></span>

## <a name="to-add-a-link-from-an-item-card"></a><span data-ttu-id="359d6-138">Sådan tilføjes et link fra et varekort</span><span class="sxs-lookup"><span data-stu-id="359d6-138">To add a link from an item card</span></span>
<span data-ttu-id="359d6-139">Du kan føje et link fra et kort eller et dokument til en hvilken som helst URL-adresse eller sti.</span><span class="sxs-lookup"><span data-stu-id="359d6-139">You can add a link from a card or document to any URL or path.</span></span> <span data-ttu-id="359d6-140">Det er nyttigt, når du f.eks. vil knytte et varekort til leverandørens varekatalog.</span><span class="sxs-lookup"><span data-stu-id="359d6-140">This is useful, for example, when you want to link an item card with the supplier's item catalog.</span></span>

<span data-ttu-id="359d6-141">Den følgende procedure er baseret på et varekort.</span><span class="sxs-lookup"><span data-stu-id="359d6-141">The following procedure is based on an item card.</span></span> <span data-ttu-id="359d6-142">Trinene er de samme for alle andre understøttede kort og dokumenter.</span><span class="sxs-lookup"><span data-stu-id="359d6-142">The steps are similar for all other supported cards and documents.</span></span>

1. <span data-ttu-id="359d6-143">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="359d6-143">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="359d6-144">Marker den vare, du vil tilføje en kæde fra, og vælg derefter fanen **Vedhæftede filer** i faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="359d6-144">Select the item that you want to add a link from, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="359d6-145">Vælg ikonet **+** i **Links**.</span><span class="sxs-lookup"><span data-stu-id="359d6-145">In the **Links**, choose the **+** icon.</span></span>
4. <span data-ttu-id="359d6-146">I feltet **Hyperlinkadresse** skal du angive linket.</span><span class="sxs-lookup"><span data-stu-id="359d6-146">In the **Link Address** field, enter the link.</span></span>

    <span data-ttu-id="359d6-147">Linket skal være en gyldig URL-adresse til internettet eller intranettet.</span><span class="sxs-lookup"><span data-stu-id="359d6-147">The link must be a valid internet or intranet URL.</span></span>

5. <span data-ttu-id="359d6-148">Angiv eventuelle oplysninger om linket i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="359d6-148">In the **Description** field, enter any information about the link.</span></span>  
6. <span data-ttu-id="359d6-149">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="359d6-149">Choose the **OK** button.</span></span>

<span data-ttu-id="359d6-150">Linket er nu knyttet til varekortet.</span><span class="sxs-lookup"><span data-stu-id="359d6-150">The link is now attached to the item card.</span></span>  

## <a name="to-write-a-note-on-a-sales-order"></a><span data-ttu-id="359d6-151">Sådan skrives en note i en salgsordre</span><span class="sxs-lookup"><span data-stu-id="359d6-151">To write a note on a sales order</span></span>
<span data-ttu-id="359d6-152">Du kan skrive en note til et dokument eller et kort, for f.eks. at kommunikere særlige instruktioner til andre brugere af dokumentet eller kortet.</span><span class="sxs-lookup"><span data-stu-id="359d6-152">You can write a note on a document or card, for example, to communicate special instructions to other users of the document or card.</span></span> <span data-ttu-id="359d6-153">Du kan medtage fillinks og URL-adresser i noter.</span><span class="sxs-lookup"><span data-stu-id="359d6-153">You can include file links and URLs in notes.</span></span>

> [!NOTE]
> <span data-ttu-id="359d6-154">Noterne under fanen **Vedhæftede filer** er ikke relateret til interne notefunktioner, som hovedsageligt bruges til kommunikation mellem brugere af arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="359d6-154">Notes on the **Attachments** tab are not related to internal notes functionality, which is mainly used to communicate between workflow users.</span></span> <span data-ttu-id="359d6-155">Du kan finde flere oplysninger i [Konfiguration af arbejdsgangsnotifikationer](across-setting-up-workflow-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="359d6-155">For more information, see [Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md).</span></span>

<span data-ttu-id="359d6-156">Følgende procedure er baseret på en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="359d6-156">The following procedure is based on a sales order.</span></span> <span data-ttu-id="359d6-157">Trinene er de samme for alle andre understøttede dokumenter og kort.</span><span class="sxs-lookup"><span data-stu-id="359d6-157">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="359d6-158">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordre**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="359d6-158">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="359d6-159">Marker den salgsordre, du vil skrive en note om, og vælg derefter fanen **Vedhæftede filer** i faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="359d6-159">Select the sales order that you want to write a note on, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="359d6-160">Vælg ikonet **+** i sektionen **Noter**.</span><span class="sxs-lookup"><span data-stu-id="359d6-160">In the **Notes** section, choose the **+** icon.</span></span>
4. <span data-ttu-id="359d6-161">Skriv en tekst i feltet **Note**, f.eks. "Dette er en vigtig bestilling".</span><span class="sxs-lookup"><span data-stu-id="359d6-161">In the **Note** field, write any text, such as "This is an urgent order.".</span></span>
5. <span data-ttu-id="359d6-162">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="359d6-162">Choose the **OK** button.</span></span>

<span data-ttu-id="359d6-163">Noten knyttes nu til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="359d6-163">The note is now attached to the sales order.</span></span>

## <a name="see-also"></a><span data-ttu-id="359d6-164">Se også</span><span class="sxs-lookup"><span data-stu-id="359d6-164">See Also</span></span>  
<span data-ttu-id="359d6-165">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="359d6-165">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="359d6-166">Indgående bilag</span><span class="sxs-lookup"><span data-stu-id="359d6-166">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="359d6-167">Konfiguration af arbejdsgangsnotifikationer</span><span class="sxs-lookup"><span data-stu-id="359d6-167">Setting Up Workflow Notifications</span></span>](across-setting-up-workflow-notifications.md)  
