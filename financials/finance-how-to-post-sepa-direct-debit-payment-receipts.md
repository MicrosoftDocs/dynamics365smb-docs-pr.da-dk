---
title: "Bogføre SEPA Direct Debit-betalinger | Microsoft Docs"
description: "Når en Direct Debit-opkrævning er behandlet af din bank, kan du fortsætte med at bogføre kvittering for betaling for de involverede salgsfakturaer."
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
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: 021c48efc6bf6b1fdb7b17bf742cb6f084d3964b
ms.contentlocale: da-dk
ms.lasthandoff: 09/27/2017

---
# <a name="how-to-post-sepa-direct-debit-payment-receipts"></a><span data-ttu-id="449b4-103">Fremgangsmåde: Bogføre SEPA Direct Debit-betalingskvitteringer</span><span class="sxs-lookup"><span data-stu-id="449b4-103">How to: Post SEPA Direct Debit Payment Receipts</span></span>
<span data-ttu-id="449b4-104">Når en Direct Debit-opkrævning er behandlet af din bank, kan du fortsætte med at bogføre kvittering for betaling for de involverede salgsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="449b4-104">When a direct debit collection is successfully processed by your bank, you can proceed to post receipt of the payment for the involved sales invoices.</span></span> <span data-ttu-id="449b4-105">Du kan finde flere oplysninger i [Fremgangsmåde: Opret poster i SEPA Direct Debit-opkrævning, og eksportér til en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="449b4-105">For more information, see [How to: Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  

<span data-ttu-id="449b4-106">Du kan bogføre betalingskvitteringen direkte fra vinduet **Direct Debit-opkrævninger** eller vinduet **Poster i Direct Debit-opkrævning**.</span><span class="sxs-lookup"><span data-stu-id="449b4-106">You can post the payment receipt directly from the **Direct Debit Collections** window or the **Direct Debit Collect. Entries** window.</span></span> <span data-ttu-id="449b4-107">Alternativt kan du overføre arbejdet til en anden bruger ved at udarbejde de relaterede kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="449b4-107">Alternatively, you can relay the work to another user by preparing the related journal lines.</span></span>  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-window"></a><span data-ttu-id="449b4-108">Sådan bogføres en betalingskvittering i Direct Debit fra vinduet Direct Debit-opkrævninger</span><span class="sxs-lookup"><span data-stu-id="449b4-108">To post a direct-debit payment receipt from the Direct Debit Collections window</span></span>  
1. <span data-ttu-id="449b4-109">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Direct Debit-opkrævninger**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="449b4-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Direct Debit Collections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="449b4-110">Vælg en linje for en Direct Debit-opkrævning, der er eksporteret til en bankfil og er blevet behandlet af banken.</span><span class="sxs-lookup"><span data-stu-id="449b4-110">Select a line for a direct debit collection that has been exported to a bank file and successfully processed by the bank.</span></span> <span data-ttu-id="449b4-111">Du kan finde flere oplysninger i [Fremgangsmåde: Opret poster i SEPA Direct Debit-opkrævning, og eksportér til en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="449b4-111">For more information, see [How to: Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  
3. <span data-ttu-id="449b4-112">Vælg handlingen **Bogfør betalingskvitteringer**.</span><span class="sxs-lookup"><span data-stu-id="449b4-112">Choose the **Post Payment Receipts** action.</span></span>  
4. <span data-ttu-id="449b4-113">I vinduet **Bogfør Direct Debit-opkrævning** skal du udfylde felterne som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="449b4-113">In the **Post Direct Debit Collection** window, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="449b4-114">Felt</span><span class="sxs-lookup"><span data-stu-id="449b4-114">Field</span></span>|<span data-ttu-id="449b4-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="449b4-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="449b4-116">**Direct Debit-opkrævningsnr.**</span><span class="sxs-lookup"><span data-stu-id="449b4-116">**Direct Debit Collection No.**</span></span>|<span data-ttu-id="449b4-117">Angiv den Direct Debit-samling, som du vil bogføre betalingskvittering for.</span><span class="sxs-lookup"><span data-stu-id="449b4-117">Specify the direct debit collection that you want to post payment receipt for.</span></span>|  
    |<span data-ttu-id="449b4-118">**Finanskladdetype**</span><span class="sxs-lookup"><span data-stu-id="449b4-118">**General Journal Template**</span></span>|<span data-ttu-id="449b4-119">Angiv, hvilken finanskladdeskabelon der skal bruges til bogføring af betalingskvitteringen, f.eks. skabelonen til indbetalinger.</span><span class="sxs-lookup"><span data-stu-id="449b4-119">Specify which general journal template to use for posting the payment receipt, such as the template for cash receipts.</span></span>|  
    |<span data-ttu-id="449b4-120">**Finanskladdenavn**</span><span class="sxs-lookup"><span data-stu-id="449b4-120">**General Journal Batch Name**</span></span>|<span data-ttu-id="449b4-121">Angiv, hvilket finanskladdenavn der skal bruges til bogføring af betalingskvitteringen.</span><span class="sxs-lookup"><span data-stu-id="449b4-121">Specify which general journal batch to use for posting the payment receipt.</span></span>|  
    |<span data-ttu-id="449b4-122">**Opret kun kladde**</span><span class="sxs-lookup"><span data-stu-id="449b4-122">**Create Journal Only**</span></span>|<span data-ttu-id="449b4-123">Markér dette afkrydsningsfelt, hvis du ikke vil bogføre betalingskvitteringen, når du vælger knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="449b4-123">Select this check box if you do not want to post the payment receipt when you choose the **OK** button.</span></span> <span data-ttu-id="449b4-124">Kvitteringen for betalingen forberedes i den angivne journal og vil ikke blive bogført, før nogen bogfører de pågældende kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="449b4-124">The payment receipt will be prepared in the specified journal and will not be posted until someone posts the journal lines in question.</span></span>|  

5. <span data-ttu-id="449b4-125">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="449b4-125">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="449b4-126">Se også</span><span class="sxs-lookup"><span data-stu-id="449b4-126">See Also</span></span>  
 <span data-ttu-id="449b4-127">[Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="449b4-127">[Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
 [<span data-ttu-id="449b4-128">Salg</span><span class="sxs-lookup"><span data-stu-id="449b4-128">Sales</span></span>](sales-manage-sales.md)

