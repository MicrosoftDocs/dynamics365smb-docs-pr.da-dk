---
title: "Om bogføring af salgsdokumenter | Microsoft Docs"
description: "Få mere at vide om de forskellige bogføringsfunktioner, der bruges til at bogføre salgsdokumenter."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/02/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 8f0ba4e8bb0770f612594e6af8a47838852a3d25
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="posting-sales"></a><span data-ttu-id="94e65-103">Bogføring af salg</span><span class="sxs-lookup"><span data-stu-id="94e65-103">Posting Sales</span></span>
<span data-ttu-id="94e65-104">I **Prod.bogf.gruppe** på et salgsdokument kan du vælge mellem følgende bogføringsfunktioner:</span><span class="sxs-lookup"><span data-stu-id="94e65-104">In the **Posting group** on a sales document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="94e65-105">**Bogfør**</span><span class="sxs-lookup"><span data-stu-id="94e65-105">**Post**</span></span>
* <span data-ttu-id="94e65-106">**Testrapport**</span><span class="sxs-lookup"><span data-stu-id="94e65-106">**Test Report**</span></span>
* <span data-ttu-id="94e65-107">**Bogfør og send**</span><span class="sxs-lookup"><span data-stu-id="94e65-107">**Post and Send**</span></span>
* <span data-ttu-id="94e65-108">**Bogfør og udskriv**</span><span class="sxs-lookup"><span data-stu-id="94e65-108">**Post and Print**</span></span>
* <span data-ttu-id="94e65-109">**Bogfør og mail**</span><span class="sxs-lookup"><span data-stu-id="94e65-109">**Post and Email**</span></span>
* <span data-ttu-id="94e65-110">**Massebogfør**</span><span class="sxs-lookup"><span data-stu-id="94e65-110">**Post Batch**</span></span>
* <span data-ttu-id="94e65-111">**Vis bogføring**</span><span class="sxs-lookup"><span data-stu-id="94e65-111">**Preview Posting**</span></span>

<span data-ttu-id="94e65-112">Når du har udfyldt alle linjer og har indsat alle oplysninger i salgsordren, kan du bogføre den.</span><span class="sxs-lookup"><span data-stu-id="94e65-112">When you have completed all the lines and entered all the information on the sales order, you can post it.</span></span> <span data-ttu-id="94e65-113">Dette opretter en leverance og en faktura.</span><span class="sxs-lookup"><span data-stu-id="94e65-113">This creates a shipment and an invoice.</span></span>

<span data-ttu-id="94e65-114">Når en salgsordre bogføres, opdateres kreditorens konto, regnskabet og vareposterne.</span><span class="sxs-lookup"><span data-stu-id="94e65-114">When a sales order is posted, the customer's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="94e65-115">For hver salgsordre oprettes der en salgspost i tabellen **Finanspost**.</span><span class="sxs-lookup"><span data-stu-id="94e65-115">For each sales order, a sales entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="94e65-116">Der oprettes også en post i debitorkontoen i tabellen **Debitorpost**, og der oprettes en finanspost i den relevante samlekonto.</span><span class="sxs-lookup"><span data-stu-id="94e65-116">An entry is also created in the customer's account in the **Cust. Ledger Entry** table and a general ledger entry is created in the relevant receivables account.</span></span> <span data-ttu-id="94e65-117">Desuden kan der eventuelt blive dannet en momspost og en finanspost for rabatbeløbet.</span><span class="sxs-lookup"><span data-stu-id="94e65-117">In addition, posting the order may result in a VAT entry and a general ledger entry for the discount amount.</span></span> <span data-ttu-id="94e65-118">Om der bogføres en post med rabat, afhænger af oplysningerne i feltet **Bogføring med rabat** i vinduet **Salgsopsætning**.</span><span class="sxs-lookup"><span data-stu-id="94e65-118">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field in the **Sales & Receivables Setup** window.</span></span>

<span data-ttu-id="94e65-119">For hver salgsordrelinje oprettes der en varepost i tabellen **Varepost** (hvis salgslinjerne indeholder varenumre) eller en finanspost i tabellen **Finanspost** (hvis der er indsat en finanskonto på salgslinjerne).</span><span class="sxs-lookup"><span data-stu-id="94e65-119">For each sales order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the sales lines contain item numbers) or a general ledger entry will be created in the **G/L Entry** table (if the sales lines contain a general ledger account).</span></span> <span data-ttu-id="94e65-120">Salgsordrer bliver desuden altid registreret i tabellerne **Salgsleverancehoved** og **Salgsfakturahoved**.</span><span class="sxs-lookup"><span data-stu-id="94e65-120">In addition to this, sales orders are always recorded in the **Sales Shipment Header** and **Sales Invoice Header** tables.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="94e65-121">Når du bogfører en ordre, har du mulighed for både at oprette en leverance og en faktura.</span><span class="sxs-lookup"><span data-stu-id="94e65-121">When you post an order, you can create both a shipment and an invoice.</span></span> <span data-ttu-id="94e65-122">Det kan gøres på samme tid eller hver for sig.</span><span class="sxs-lookup"><span data-stu-id="94e65-122">These can be done at the same time or independently.</span></span> <span data-ttu-id="94e65-123">Du kan også oprette en delleverance og en delfaktura ved at udfylde felterne **Lever (antal)** og **Fakturer (antal)** på de enkelte salgsordrelinjer, før du bogfører.</span><span class="sxs-lookup"><span data-stu-id="94e65-123">You can also create a partial shipment and a partial invoice by completing the **Qty. to Ship** and **Qty. to Invoice** fields on the individual sales order lines before you post.</span></span> <span data-ttu-id="94e65-124">Bemærk, at du ikke kan oprette en faktura for noget, der ikke er leveret.</span><span class="sxs-lookup"><span data-stu-id="94e65-124">Note that you cannot create an invoice for something that is not shipped.</span></span> <span data-ttu-id="94e65-125">Dvs., før du kan fakturere, skal der være registreret en leverance, eller du skal vælge at sende og fakturere på samme tid.</span><span class="sxs-lookup"><span data-stu-id="94e65-125">That is, before you can invoice, you must have recorded a shipment, or you must choose to ship and invoice at the same time.</span></span>

<span data-ttu-id="94e65-126">Når bogføringen er gennemført, fjernes de bogførte salgslinjer fra ordren.</span><span class="sxs-lookup"><span data-stu-id="94e65-126">When the posting is completed, the posted sales lines are removed from the order.</span></span> <span data-ttu-id="94e65-127">Der vises en meddelelse, når bogføringen er gennemført.</span><span class="sxs-lookup"><span data-stu-id="94e65-127">A message tells you when the posting is completed.</span></span> <span data-ttu-id="94e65-128">Herefter kan du se de bogførte poster i forskellige vinduer, der indeholder bogførte poster, f.eks. **Debitorposter**, **Finansposter**, **Vareposter**, **Bogf. salgsleverancer** og **Bogf. salgsfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="94e65-128">After this, you will be able to see the posted entries in the various windows that contain posted entries, such as the **Cust. Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Posted Sales Shipments**, and **Posted Sales Invoices** windows.</span></span>

## <a name="see-also"></a><span data-ttu-id="94e65-129">Se også</span><span class="sxs-lookup"><span data-stu-id="94e65-129">See Also</span></span>
[<span data-ttu-id="94e65-130">Salg</span><span class="sxs-lookup"><span data-stu-id="94e65-130">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="94e65-131">Sende dokumenter som mail</span><span class="sxs-lookup"><span data-stu-id="94e65-131">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="94e65-132">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="94e65-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


