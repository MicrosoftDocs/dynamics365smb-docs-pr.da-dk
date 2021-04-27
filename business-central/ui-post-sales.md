---
title: Bogføre salgsdokumenter
description: Lære mere om de forskellige bogføringsfunktioner til bogføring af salgsdokumenter, og hvordan du kan opdatere bogførte dokumenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e59c48c31e897d235c7920f4231313a2332fdf06
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783255"
---
# <a name="posting-sales"></a><span data-ttu-id="dbd2d-103">Bogføring af salg</span><span class="sxs-lookup"><span data-stu-id="dbd2d-103">Posting Sales</span></span>

<span data-ttu-id="dbd2d-104">I menuen **Bogføring** i et salgsdokument kan du vælge mellem følgende bogføringsfunktioner:</span><span class="sxs-lookup"><span data-stu-id="dbd2d-104">Under the **Posting** menu in a sales document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="dbd2d-105">**Bogfør**</span><span class="sxs-lookup"><span data-stu-id="dbd2d-105">**Post**</span></span>
* <span data-ttu-id="dbd2d-106">**Bogfør og ny**</span><span class="sxs-lookup"><span data-stu-id="dbd2d-106">**Post and New**</span></span>
* <span data-ttu-id="dbd2d-107">**Bogfør og send**</span><span class="sxs-lookup"><span data-stu-id="dbd2d-107">**Post and Send**</span></span>
* <span data-ttu-id="dbd2d-108">**Vis bogføring**</span><span class="sxs-lookup"><span data-stu-id="dbd2d-108">**Preview Posting**</span></span>
* <span data-ttu-id="dbd2d-109">**Massebogfør**</span><span class="sxs-lookup"><span data-stu-id="dbd2d-109">**Post Batch**</span></span>
* <span data-ttu-id="dbd2d-110">**Testrapport**</span><span class="sxs-lookup"><span data-stu-id="dbd2d-110">**Test Report**</span></span>

> [!NOTE]
> <span data-ttu-id="dbd2d-111">I forbindelse med salgsordrer kan du også se indstillinger, der vedrører forudbetalingsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-111">For sales orders, you can also see options related to the prepayments functionality.</span></span> <span data-ttu-id="dbd2d-112">Du kan finde flere oplysninger i [Fakturere forudbetalinger](finance-invoice-prepayments.md).</span><span class="sxs-lookup"><span data-stu-id="dbd2d-112">For more information, see [Invoicing Prepayments](finance-invoice-prepayments.md).</span></span>

<span data-ttu-id="dbd2d-113">Når du har udfyldt alle linjer og har indsat alle oplysninger i salgsordren, kan du bogføre den.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-113">When you have completed all the lines and entered all the information on the sales order, you can post it.</span></span> <span data-ttu-id="dbd2d-114">Dette opretter en leverance og en faktura.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-114">This creates a shipment and an invoice.</span></span>

<span data-ttu-id="dbd2d-115">Når en salgsordre bogføres, opdateres kreditorens konto, regnskabet og vareposterne.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-115">When a sales order is posted, the customer's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="dbd2d-116">For hver salgsordre oprettes der en salgspost i tabellen **Finanspost**.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-116">For each sales order, a sales entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="dbd2d-117">Der oprettes også en post i debitorkontoen i tabellen **Debitorpost**, og der oprettes en finanspost i den relevante samlekonto.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-117">An entry is also created in the customer's account in the **Cust. Ledger Entry** table and a general ledger entry is created in the relevant receivables account.</span></span> <span data-ttu-id="dbd2d-118">Desuden kan der eventuelt blive dannet en momspost og en finanspost for rabatbeløbet.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-118">In addition, posting the order may result in a VAT entry and a general ledger entry for the discount amount.</span></span> <span data-ttu-id="dbd2d-119">Om der bogføres en post med rabat, afhænger af oplysningerne i feltet **Bogføring med rabat** på siden **Salgsopsætning**.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-119">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field on the **Sales & Receivables Setup** page.</span></span>

<span data-ttu-id="dbd2d-120">For hver salgsordrelinje oprettes der en varepost i tabellen **Varepost** (hvis salgslinjerne indeholder varenumre) eller en finanspost i tabellen **Finanspost** (hvis der er indsat en finanskonto på salgslinjerne).</span><span class="sxs-lookup"><span data-stu-id="dbd2d-120">For each sales order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the sales lines contain item numbers) or a general ledger entry will be created in the **G/L Entry** table (if the sales lines contain a general ledger account).</span></span> <span data-ttu-id="dbd2d-121">Salgsordrer bliver desuden altid registreret i tabellerne **Salgsleverancehoved** og **Salgsfakturahoved**.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-121">In addition to this, sales orders are always recorded in the **Sales Shipment Header** and **Sales Invoice Header** tables.</span></span>

> [!IMPORTANT]  
> <span data-ttu-id="dbd2d-122">Når du bogfører en ordre, har du mulighed for både at oprette en leverance og en faktura.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-122">When you post an order, you can create both a shipment and an invoice.</span></span> <span data-ttu-id="dbd2d-123">Det kan gøres på samme tid eller hver for sig.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-123">These can be done at the same time or independently.</span></span> <span data-ttu-id="dbd2d-124">Du kan også oprette en delleverance og en delfaktura ved at udfylde felterne **Lever (antal)** og **Fakturer (antal)** på de enkelte salgsordrelinjer, før du bogfører.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-124">You can also create a partial shipment and a partial invoice by completing the **Qty. to Ship** and **Qty. to Invoice** fields on the individual sales order lines before you post.</span></span> <span data-ttu-id="dbd2d-125">Bemærk, at du ikke kan oprette en faktura for noget, der ikke er leveret.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-125">Note that you cannot create an invoice for something that is not shipped.</span></span> <span data-ttu-id="dbd2d-126">Dvs., før du kan fakturere, skal der være registreret en leverance, eller du skal vælge at sende og fakturere på samme tid.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-126">That is, before you can invoice, you must have recorded a shipment, or you must choose to ship and invoice at the same time.</span></span>

<span data-ttu-id="dbd2d-127">Du kan enten bogføre eller bogføre og sende.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-127">You can either post, or post and send.</span></span> <span data-ttu-id="dbd2d-128">Hvis du vælger at bogføre og sende, genereres der en PDF-fil, som du derefter kan sende.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-128">If you choose to post and send, a PDF file is generated that you can then send.</span></span> <span data-ttu-id="dbd2d-129">Du kan også vælge funktionen **Massebogfør**, der giver mulighed for at bogføre flere ordrer samtidig.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-129">You can also choose the **Post Batch** function, which lets you post several orders at the same time.</span></span> <span data-ttu-id="dbd2d-130">Du kan finde flere oplysninger i [Bogføre flere dokumenter på én gang](ui-batch-posting.md).</span><span class="sxs-lookup"><span data-stu-id="dbd2d-130">For more information, see [Post Multiple Documents at the Same Time](ui-batch-posting.md).</span></span>

## <a name="viewing-ledger-entries"></a><span data-ttu-id="dbd2d-131">Visning af finansposter</span><span class="sxs-lookup"><span data-stu-id="dbd2d-131">Viewing Ledger Entries</span></span>

<span data-ttu-id="dbd2d-132">Når bogføringen er gennemført, fjernes de bogførte salgslinjer fra ordren.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-132">When the posting is completed, the posted sales lines are removed from the order.</span></span> <span data-ttu-id="dbd2d-133">Der vises en meddelelse, når bogføringen er gennemført.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-133">A message tells you when the posting is completed.</span></span> <span data-ttu-id="dbd2d-134">Herefter kan du se de bogførte poster på forskellige sider, der indeholder bogførte poster, f.eks. **Debitorposter**, **Finansposter**, **Vareposter**, **Bogf. salgsleverancer** og **Bogf. salgsfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-134">After this, you will be able to see the posted entries in the various pages that contain posted entries, such as the **Cust. Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Posted Sales Shipments**, and **Posted Sales Invoices** pages.</span></span>  

<span data-ttu-id="dbd2d-135">I de fleste tilfælde kan du åbne finansposter fra det berørte kort eller dokument.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-135">In most cases, you can open ledger entries from the affected card or document.</span></span> <span data-ttu-id="dbd2d-136">Du kan f.eks. på siden **Debitorkort** vælge handlingen **Finansposter**.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-136">For example, on the **Customer Card** page, choose the **Ledger Entries** action.</span></span>

## <a name="editing-ledger-entries"></a><span data-ttu-id="dbd2d-137">Redigering af finansposter</span><span class="sxs-lookup"><span data-stu-id="dbd2d-137">Editing Ledger Entries</span></span>

<span data-ttu-id="dbd2d-138">Du kan redigere bestemte felter i bogførte købsdokumenter, f. eks **Pakkesporingsnr.**</span><span class="sxs-lookup"><span data-stu-id="dbd2d-138">You can edit certain fields on posted purchase documents, such as the **Package Tracking No.**</span></span> <span data-ttu-id="dbd2d-139">.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-139">field.</span></span> <span data-ttu-id="dbd2d-140">Du kan finde flere oplysninger i [Redigere bogførte dokumenter](across-edit-posted-document.md).</span><span class="sxs-lookup"><span data-stu-id="dbd2d-140">For more information, see [Edit Posted Documents](across-edit-posted-document.md).</span></span> <span data-ttu-id="dbd2d-141">Er det mere kritiske felter, der påvirker overvågningssporet, skal du tilbageføre eller annullere bogføring.</span><span class="sxs-lookup"><span data-stu-id="dbd2d-141">For more critical fields that affect the auditing trail, you must reverse or undo posting.</span></span> <span data-ttu-id="dbd2d-142">Du kan finde flere oplysninger i [Tilbageføre kladdeposteringer og annullere modtagelser/leverancer](finance-how-reverse-journal-posting.md).</span><span class="sxs-lookup"><span data-stu-id="dbd2d-142">For more information, see [Reverse Journal Postings and Undo Receipts/Shipments](finance-how-reverse-journal-posting.md).</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="dbd2d-143">Se relateret oplæring på [Microsoft Learn](/learn/modules/ship-invoice-items-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="dbd2d-143">See Related Training at [Microsoft Learn](/learn/modules/ship-invoice-items-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="dbd2d-144">Se også</span><span class="sxs-lookup"><span data-stu-id="dbd2d-144">See Also</span></span>

[<span data-ttu-id="dbd2d-145">Salg</span><span class="sxs-lookup"><span data-stu-id="dbd2d-145">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="dbd2d-146">Bogføre flere dokumenter på én gang</span><span class="sxs-lookup"><span data-stu-id="dbd2d-146">Post Multiple Documents at the Same Time</span></span>](ui-batch-posting.md)  
[<span data-ttu-id="dbd2d-147">Redigere bogførte dokumenter</span><span class="sxs-lookup"><span data-stu-id="dbd2d-147">Edit Posted Documents</span></span>](across-edit-posted-document.md)  
[<span data-ttu-id="dbd2d-148">Sende dokumenter som mail</span><span class="sxs-lookup"><span data-stu-id="dbd2d-148">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
[<span data-ttu-id="dbd2d-149">Rette eller annullere ubetalte salgsfakturaer</span><span class="sxs-lookup"><span data-stu-id="dbd2d-149">Correct or Cancel Unpaid Sales Invoices</span></span>](sales-how-correct-cancel-sales-invoice.md)  
[<span data-ttu-id="dbd2d-150">Søge efter sider og oplysninger med Fortæl mig</span><span class="sxs-lookup"><span data-stu-id="dbd2d-150">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="dbd2d-151">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dbd2d-151">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>

[!INCLUDE[footer-include](includes/footer-banner.md)]  
