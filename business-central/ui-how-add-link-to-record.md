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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 84d58193fa7ee272b372403d63702348fbfb1f77
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315271"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a><span data-ttu-id="3e73f-103">Administrere vedhæftede filer, links og noter på kort og dokumenter</span><span class="sxs-lookup"><span data-stu-id="3e73f-103">Manage Attachments, Links, and Notes on Cards and Documents</span></span>

<span data-ttu-id="3e73f-104">I faktaboksen på de fleste kort og i dokumenter kan du vedhæfte filer, tilføje links og skrive noter.</span><span class="sxs-lookup"><span data-stu-id="3e73f-104">In the FactBox on most cards and documents, you can attach files, add links, and write notes.</span></span> <span data-ttu-id="3e73f-105">Ved links og noter kan du også gøre dette på listesiden ved først at vælge den relaterede linje.</span><span class="sxs-lookup"><span data-stu-id="3e73f-105">For links and notes, you can also do this on the list page by first selecting the related line.</span></span>

<span data-ttu-id="3e73f-106">Hvis du vil have vist eller ændre nogen af disse typer vedhæftede oplysninger, skal du først åbne fanen **Vedhæftede filer** i faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="3e73f-106">To view or change any of these attached information types, you must first open the **Attachments** tab in the FactBox.</span></span> <span data-ttu-id="3e73f-107">Nummeret bag fanetitlen angiver, hvor mange vedhæftede filer, links eller noter der findes for kortet eller dokumentet.</span><span class="sxs-lookup"><span data-stu-id="3e73f-107">The number behind the tab title indicates how many attached files, links, or notes exist for the card or document.</span></span>

<span data-ttu-id="3e73f-108">Vedhæftede filer, links og noter forbliver tilknyttede, når kortet eller dokumentet behandles i andre tilstande, f.eks. fra en igangværende salgsordre til en bogført salgsfaktura.</span><span class="sxs-lookup"><span data-stu-id="3e73f-108">Attachments, links, and notes stay attached as the card or document is processed into other states, such as from an ongoing sales order to a posted sales invoice.</span></span> <span data-ttu-id="3e73f-109">Bemærk dog, at ingen af de vedhæftede filtyper er output fra systemet, f.eks. ved udskrivning eller lagring til en fil.</span><span class="sxs-lookup"><span data-stu-id="3e73f-109">Note, however, that none of the attachment types are output from the system, for example, when printing or when saving to a file.</span></span>

## <a name="to-attach-a-file-to-a-purchase-invoice"></a><span data-ttu-id="3e73f-110">Sådan vedhæftes en fil til en købsfaktura</span><span class="sxs-lookup"><span data-stu-id="3e73f-110">To attach a file to a purchase invoice</span></span>
<span data-ttu-id="3e73f-111">Du kan vedhæfte alle filtyper, der indeholder tekst, billeder eller video, på et kort eller et dokument.</span><span class="sxs-lookup"><span data-stu-id="3e73f-111">You can attach any type of file, containing text, image, or video, to a card or document.</span></span> <span data-ttu-id="3e73f-112">Det er nyttigt, når du f.eks. vil gemme en kreditorfaktura som PDF-fil på den relaterede købsfaktura i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3e73f-112">This is useful, for example, when you want to store a vendor's invoice as a PDF file on the related purchase invoice in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="3e73f-113">Filer, der er vedhæftet med funktionen Indgående bilag, medtages ikke under fanen **Vedhæftede filer**. Du kan finde flere oplysninger i [Indgående bilag](across-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="3e73f-113">Files attached with the Incoming Documents feature are not included on the **Attachments** tab. For more information, see [Incoming Documents](across-income-documents.md).</span></span>

<span data-ttu-id="3e73f-114">Følgende procedure er baseret på en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="3e73f-114">The following procedure is based on a sales order.</span></span> <span data-ttu-id="3e73f-115">Trinene er de samme for alle andre understøttede dokumenter og kort.</span><span class="sxs-lookup"><span data-stu-id="3e73f-115">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="3e73f-116">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="3e73f-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="3e73f-117">Åbn den salgsordre, som du vil vedhæfte en fil til.</span><span class="sxs-lookup"><span data-stu-id="3e73f-117">Open the sales order that you want to attach a file to.</span></span>
3. <span data-ttu-id="3e73f-118">Åbn fanen **Vedhæftede filer** i faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="3e73f-118">In the FactBox, open the **Attachments** tab.</span></span>
4. <span data-ttu-id="3e73f-119">Vælg værdien bag feltet **Dokumenter**, f.eks. "0".</span><span class="sxs-lookup"><span data-stu-id="3e73f-119">Choose the value behind the **Documents** field, such as "0".</span></span>
5. <span data-ttu-id="3e73f-120">På siden **Vedhæftede bilag** i feltet **Vedhæftet fil** skal du vælge knappen **Vælg fil**.</span><span class="sxs-lookup"><span data-stu-id="3e73f-120">On the **Attached Documents** page, in the **Attachment** field, choose the **Select File** button.</span></span>
5. <span data-ttu-id="3e73f-121">Vælg en fil fra en placering, og vælg derefter knappen **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="3e73f-121">Select a file from any location, and then choose the **Open** button.</span></span>

<span data-ttu-id="3e73f-122">Filen er nu vedhæftet til købsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="3e73f-122">The file is now attached to the purchase invoice.</span></span>

## <a name="to-add-a-link-from-an-item-card"></a><span data-ttu-id="3e73f-123">Sådan tilføjes et link fra et varekort</span><span class="sxs-lookup"><span data-stu-id="3e73f-123">To add a link from an item card</span></span>
<span data-ttu-id="3e73f-124">Du kan føje et link fra et kort eller et dokument til en hvilken som helst URL-adresse eller sti.</span><span class="sxs-lookup"><span data-stu-id="3e73f-124">You can add a link from a card or document to any URL or path.</span></span> <span data-ttu-id="3e73f-125">Det er nyttigt, når du f.eks. vil knytte et varekort til leverandørens varekatalog.</span><span class="sxs-lookup"><span data-stu-id="3e73f-125">This is useful, for example, when you want to link an item card with the supplier's item catalog.</span></span>

<span data-ttu-id="3e73f-126">Den følgende procedure er baseret på et varekort.</span><span class="sxs-lookup"><span data-stu-id="3e73f-126">The following procedure is based on an item card.</span></span> <span data-ttu-id="3e73f-127">Trinene er de samme for alle andre understøttede kort og dokumenter.</span><span class="sxs-lookup"><span data-stu-id="3e73f-127">The steps are similar for all other supported cards and documents.</span></span>

1. <span data-ttu-id="3e73f-128">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="3e73f-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="3e73f-129">Marker den vare, du vil tilføje en kæde fra, og vælg derefter fanen **Vedhæftede filer** i faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="3e73f-129">Select the item that you want to add a link from, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="3e73f-130">Vælg ikonet **+** i **Links**.</span><span class="sxs-lookup"><span data-stu-id="3e73f-130">In the **Links**, choose the **+** icon.</span></span>
4. <span data-ttu-id="3e73f-131">I feltet **Hyperlinkadresse** skal du angive linket.</span><span class="sxs-lookup"><span data-stu-id="3e73f-131">In the **Link Address** field, enter the link.</span></span>

    - <span data-ttu-id="3e73f-132">Hvis du vil sammenkæde med en fil på din computer eller dit netværk, skal du angive den fulde sti og filnavn, f.eks. **C:\Dokumenter\faktura1.doc**.</span><span class="sxs-lookup"><span data-stu-id="3e73f-132">To link to a file on your computer or network, enter the full path and file name, such as **C:\My Documents\invoice1.doc**.</span></span>
    - <span data-ttu-id="3e73f-133">Hvis du vil sammenkæde med et websted, skal du angive URL-adressen (internetadressen), f.eks. **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="3e73f-133">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    - <span data-ttu-id="3e73f-134">Hvis du vil sammenkæde med et program, skal du angive en bestemt streng for at åbne programmet.</span><span class="sxs-lookup"><span data-stu-id="3e73f-134">To link to a program, enter a specific string to open the program.</span></span> <span data-ttu-id="3e73f-135">Hvis du f.eks. vil åbne Outlook med en ny tom mail til et bestemt alias, skal du angive **mailto:testalias**.</span><span class="sxs-lookup"><span data-stu-id="3e73f-135">For example, to open Outlook with a new empty email to a specific alias, enter **mailto:testalias**.</span></span>  

5. <span data-ttu-id="3e73f-136">Angiv eventuelle oplysninger om linket i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="3e73f-136">In the **Description** field, enter any information about the link.</span></span>  
6. <span data-ttu-id="3e73f-137">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e73f-137">Choose the **OK** button.</span></span>

<span data-ttu-id="3e73f-138">Linket er nu knyttet til varekortet.</span><span class="sxs-lookup"><span data-stu-id="3e73f-138">The link is now attached to the item card.</span></span>  

## <a name="to-write-a-note-on-a-sales-order"></a><span data-ttu-id="3e73f-139">Sådan skrives en note i en salgsordre</span><span class="sxs-lookup"><span data-stu-id="3e73f-139">To write a note on a sales order</span></span>
<span data-ttu-id="3e73f-140">Du kan skrive en note til et dokument eller et kort, for f.eks. at kommunikere særlige instruktioner til andre brugere af dokumentet eller kortet.</span><span class="sxs-lookup"><span data-stu-id="3e73f-140">You can write a note on a document or card, for example, to communicate special instructions to other users of the document or card.</span></span> <span data-ttu-id="3e73f-141">Du kan medtage fillinks og URL-adresser i noter.</span><span class="sxs-lookup"><span data-stu-id="3e73f-141">You can include file links and URLs in notes.</span></span>

> [!NOTE]
> <span data-ttu-id="3e73f-142">Noterne under fanen **Vedhæftede filer** er ikke relateret til interne notefunktioner, som hovedsageligt bruges til kommunikation mellem brugere af arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="3e73f-142">Notes on the **Attachments** tab are not related to internal notes functionality, which is mainly used to communicate between workflow users.</span></span> <span data-ttu-id="3e73f-143">Du kan finde flere oplysninger i [Konfiguration af arbejdsgangsnotifikationer](across-setting-up-workflow-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="3e73f-143">For more information, see [Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md).</span></span>

<span data-ttu-id="3e73f-144">Følgende procedure er baseret på en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="3e73f-144">The following procedure is based on a sales order.</span></span> <span data-ttu-id="3e73f-145">Trinene er de samme for alle andre understøttede dokumenter og kort.</span><span class="sxs-lookup"><span data-stu-id="3e73f-145">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="3e73f-146">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="3e73f-146">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="3e73f-147">Marker den salgsordre, du vil skrive en note om, og vælg derefter fanen **Vedhæftede filer** i faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="3e73f-147">Select the sales order that you want to write a note on, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="3e73f-148">Vælg ikonet **+** i sektionen **Noter**.</span><span class="sxs-lookup"><span data-stu-id="3e73f-148">In the **Notes** section, choose the **+** icon.</span></span>
4. <span data-ttu-id="3e73f-149">Skriv en tekst i feltet **Note**, f.eks. "Dette er en vigtig bestilling".</span><span class="sxs-lookup"><span data-stu-id="3e73f-149">In the **Note** field, write any text, such as "This is an urgent order.".</span></span>
5. <span data-ttu-id="3e73f-150">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e73f-150">Choose the **OK** button.</span></span>

<span data-ttu-id="3e73f-151">Noten knyttes nu til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="3e73f-151">The note is now attached to the sales order.</span></span>

## <a name="see-also"></a><span data-ttu-id="3e73f-152">Se også</span><span class="sxs-lookup"><span data-stu-id="3e73f-152">See Also</span></span>  
<span data-ttu-id="3e73f-153">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3e73f-153">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="3e73f-154">Indgående bilag</span><span class="sxs-lookup"><span data-stu-id="3e73f-154">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="3e73f-155">Konfiguration af arbejdsgangsnotifikationer</span><span class="sxs-lookup"><span data-stu-id="3e73f-155">Setting Up Workflow Notifications</span></span>](across-setting-up-workflow-notifications.md)  
