---
title: "Om bogføring af købsdokumenter | Microsoft Docs"
description: "Få mere at vide om de forskellige bogføringsfunktioner, der bruges til at bogføre købsdokumenter."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/12/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 06c22658518d504c80a5a379d579cf7f7e8a0757
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="posting-purchases"></a><span data-ttu-id="7820a-103">Bogføring af køb</span><span class="sxs-lookup"><span data-stu-id="7820a-103">Posting Purchases</span></span>
<span data-ttu-id="7820a-104">I **Prod.bogf.gruppe** på et købsdokument kan du vælge mellem følgende bogføringsfunktioner:</span><span class="sxs-lookup"><span data-stu-id="7820a-104">In the **Posting group** on a purchase document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="7820a-105">**Bogfør**</span><span class="sxs-lookup"><span data-stu-id="7820a-105">**Post**</span></span>
* <span data-ttu-id="7820a-106">**Vis bogføring**</span><span class="sxs-lookup"><span data-stu-id="7820a-106">**Preview Posting**</span></span>
* <span data-ttu-id="7820a-107">**Bogfør og udskriv**</span><span class="sxs-lookup"><span data-stu-id="7820a-107">**Post and Print**</span></span>
* <span data-ttu-id="7820a-108">**Testrapport**</span><span class="sxs-lookup"><span data-stu-id="7820a-108">**Test Report**</span></span>
* <span data-ttu-id="7820a-109">**Massebogfør**</span><span class="sxs-lookup"><span data-stu-id="7820a-109">**Post Batch**</span></span>

<span data-ttu-id="7820a-110">Når du har udfyldt alle linjer og har indsat alle oplysninger i købsordren, kan du bogføre den, dvs. modtage og fakturere.</span><span class="sxs-lookup"><span data-stu-id="7820a-110">When you have completed all the lines and entered all the information on the purchase order, you can post it, that is, create a receipt and an invoice.</span></span>

<span data-ttu-id="7820a-111">Når en købsordre bogføres, opdateres kreditorens konto, regnskabet og vareposterne.</span><span class="sxs-lookup"><span data-stu-id="7820a-111">When a purchase order is posted, the vendor's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="7820a-112">For hver købsordre bliver der oprettet en købspost i tabellen **Finanspost**.</span><span class="sxs-lookup"><span data-stu-id="7820a-112">For each purchase order, a purchase entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="7820a-113">Der oprettes også en post i kreditorkontoen i tabellen **Kreditorpost**, og der oprettes en finanspost i den relevante samlekonto.</span><span class="sxs-lookup"><span data-stu-id="7820a-113">An entry is also created in the vendor's account in the **Vendor Ledger Entry** table and a G/L entry is created in the relevant payables account.</span></span> <span data-ttu-id="7820a-114">Desuden kan der eventuelt blive dannet en momspost og en finanspost med rabat.</span><span class="sxs-lookup"><span data-stu-id="7820a-114">In addition, posting the order may result in a VAT entry and a G/L entry for the discount amount.</span></span> <span data-ttu-id="7820a-115">Om der bogføres en post med rabat, afhænger af oplysningerne i feltet **Bogføring med rabat** i vinduet **Købsopsætning**.</span><span class="sxs-lookup"><span data-stu-id="7820a-115">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field in the **Purchases & Payables Setup** window.</span></span>

<span data-ttu-id="7820a-116">For hver købsordrelinje bliver der oprettet en varepost i tabellen **Varepost** (hvis købslinjerne indeholder varenumre) eller en finanspost i tabellen **Finanspost** (hvis der er indsat en finanskonto på købslinjerne).</span><span class="sxs-lookup"><span data-stu-id="7820a-116">For each purchase order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the purchase lines contain item numbers) or a G/L entry will be created in the **G/L Entry** table (if the purchase lines contain a G/L account).</span></span> <span data-ttu-id="7820a-117">Købsordrer bliver desuden altid registreret i tabellerne **Købsleverancehoved** og **Købsfakturahoved**.</span><span class="sxs-lookup"><span data-stu-id="7820a-117">In addition, purchase orders are always recorded in the **Purch. Recpt. Header** and **Purch. Inv. Header** tables.</span></span>

<span data-ttu-id="7820a-118">Inden du starter på selve bogføringen, kan du udskrive en kontrolrapport med alle oplysninger i købsordren og eventuelle fejl.</span><span class="sxs-lookup"><span data-stu-id="7820a-118">Before you start to post, you can print a test report that contains all the information in the purchase order and indicates any errors there.</span></span> <span data-ttu-id="7820a-119">Hvis du vil udskrive rapporten, skal du vælge **Bogføring** og derefter vælge **Kontrollér rapport**.</span><span class="sxs-lookup"><span data-stu-id="7820a-119">To print the report, choose **Posting**, and then choose **Test Report**.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="7820a-120">Når du bogfører en ordre, har du mulighed for både at modtage og fakturere.</span><span class="sxs-lookup"><span data-stu-id="7820a-120">When you post an order, you can create both a receipt and an invoice.</span></span> <span data-ttu-id="7820a-121">Det kan gøres samtidigt eller hver for sig.</span><span class="sxs-lookup"><span data-stu-id="7820a-121">These can be done simultaneously or independently.</span></span> <span data-ttu-id="7820a-122">Du kan også oprette en delkvittering og en delfaktura ved at udfylde felterne **Modtag (antal)** og **Fakturer (antal)** på de enkelte købsordrelinjer, før du bogfører.</span><span class="sxs-lookup"><span data-stu-id="7820a-122">You can also create a partial receipt and a partial invoice by completing the **Qty. to Receive** and **Qty. to Invoice** fields on the individual purchase order lines before you post.</span></span> <span data-ttu-id="7820a-123">Bemærk, at du ikke kan oprette en faktura for noget, der ikke er modtaget.</span><span class="sxs-lookup"><span data-stu-id="7820a-123">Note that you cannot create an invoice for something that has not been received.</span></span> <span data-ttu-id="7820a-124">For at kunne fakturere er det altså nødvendigt, at du på forhånd har registreret en modtagelse, eller at du nu vælger at modtage og fakturere samtidigt.</span><span class="sxs-lookup"><span data-stu-id="7820a-124">That is, before you can invoice, you must have recorded a receipt, or you must choose to receive and invoice at the same time.</span></span>

<span data-ttu-id="7820a-125">Du kan enten bogføre eller bogføre og udskrive.</span><span class="sxs-lookup"><span data-stu-id="7820a-125">You can either post, or post and print.</span></span> <span data-ttu-id="7820a-126">Hvis du vælger at bogføre og udskrive, udskrives der en rapport, når ordren bogføres.</span><span class="sxs-lookup"><span data-stu-id="7820a-126">If you choose to post and print, a report is printed when the order is posted.</span></span> <span data-ttu-id="7820a-127">Du kan også vælge funktionen **Massebogfør**, der giver mulighed for at bogføre flere ordrer samtidig.</span><span class="sxs-lookup"><span data-stu-id="7820a-127">You can also choose the **Post Batch** function, which lets you post several orders at the same time.</span></span>

<span data-ttu-id="7820a-128">Når bogføringen er gennemført, fjernes de bogførte købslinjer fra ordren.</span><span class="sxs-lookup"><span data-stu-id="7820a-128">When the posting is completed, the posted purchase lines are removed from the order.</span></span> <span data-ttu-id="7820a-129">Der vises en meddelelse, når bogføringen er gennemført.</span><span class="sxs-lookup"><span data-stu-id="7820a-129">A message tells you when the posting is completed.</span></span> <span data-ttu-id="7820a-130">Herefter kan du se de bogførte poster i forskellige vinduer, der indeholder bogførte poster, f.eks. **Kreditorposter**, **Finansposter**, **Vareposter**, **Købsleverance** og **Bogf. købsfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="7820a-130">After this, you will be able to see the posted entries in the various windows that contain posted entries, such as the **Vendor Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Purchase Receipts**, and **Posted Purchase Invoices** windows.</span></span>

## <a name="see-also"></a><span data-ttu-id="7820a-131">Se også</span><span class="sxs-lookup"><span data-stu-id="7820a-131">See Also</span></span>
[<span data-ttu-id="7820a-132">Køb</span><span class="sxs-lookup"><span data-stu-id="7820a-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="7820a-133">Bogføre dokumenter og kladder</span><span class="sxs-lookup"><span data-stu-id="7820a-133">Post Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="7820a-134">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7820a-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


