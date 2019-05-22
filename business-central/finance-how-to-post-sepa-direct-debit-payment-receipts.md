---
title: Bogføre SEPA Direct Debit-betalinger | Microsoft Docs
description: Når en Direct Debit-opkrævning er behandlet af din bank, kan du fortsætte med at bogføre kvittering for betaling for de involverede salgsfakturaer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.openlocfilehash: 6c646575ba803358aa00309ce02742423bcc7de8
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242648"
---
# <a name="post-sepa-direct-debit-payment-receipts"></a><span data-ttu-id="fb617-103">Bogføre SEPA Direct Debit-betalingskvitteringer</span><span class="sxs-lookup"><span data-stu-id="fb617-103">Post SEPA Direct Debit Payment Receipts</span></span>
<span data-ttu-id="fb617-104">Når en Direct Debit-opkrævning er behandlet af din bank, kan du fortsætte med at bogføre kvittering for betaling for de involverede salgsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="fb617-104">When a direct debit collection is successfully processed by your bank, you can proceed to post receipt of the payment for the involved sales invoices.</span></span> <span data-ttu-id="fb617-105">Du kan finde flere oplysninger i [Oprette poster i SEPA Direct Debit-opkrævning og eksportere til en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="fb617-105">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  

<span data-ttu-id="fb617-106">Du kan bogføre betalingskvitteringen direkte fra siden **Direct Debit-opkrævninger** eller siden **Poster i Direct Debit-opkrævning**.</span><span class="sxs-lookup"><span data-stu-id="fb617-106">You can post the payment receipt directly from the **Direct Debit Collections** page or the **Direct Debit Collect. Entries** page.</span></span> <span data-ttu-id="fb617-107">Alternativt kan du overføre arbejdet til en anden bruger ved at udarbejde de relaterede kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="fb617-107">Alternatively, you can relay the work to another user by preparing the related journal lines.</span></span>  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a><span data-ttu-id="fb617-108">Sådan bogføres en betalingskvittering i Direct Debit fra siden Direct Debit-opkrævninger</span><span class="sxs-lookup"><span data-stu-id="fb617-108">To post a direct-debit payment receipt from the Direct Debit Collections page</span></span>  
1. <span data-ttu-id="fb617-109">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Direct Debit-opkrævninger**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="fb617-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Direct Debit Collections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="fb617-110">Vælg en linje for en Direct Debit-opkrævning, der er eksporteret til en bankfil og er blevet behandlet af banken.</span><span class="sxs-lookup"><span data-stu-id="fb617-110">Select a line for a direct debit collection that has been exported to a bank file and successfully processed by the bank.</span></span> <span data-ttu-id="fb617-111">Du kan finde flere oplysninger i [Oprette poster i SEPA Direct Debit-opkrævning og eksportere til en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="fb617-111">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  
3. <span data-ttu-id="fb617-112">Vælg handlingen **Bogfør betalingskvitteringer**.</span><span class="sxs-lookup"><span data-stu-id="fb617-112">Choose the **Post Payment Receipts** action.</span></span>  
4. <span data-ttu-id="fb617-113">På siden **Bogfør Direct Debit-opkrævning** skal du udfylde felterne som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="fb617-113">On the **Post Direct Debit Collection** page, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="fb617-114">Felt</span><span class="sxs-lookup"><span data-stu-id="fb617-114">Field</span></span>|<span data-ttu-id="fb617-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="fb617-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="fb617-116">**Direct Debit-opkrævningsnr.**</span><span class="sxs-lookup"><span data-stu-id="fb617-116">**Direct Debit Collection No.**</span></span>|<span data-ttu-id="fb617-117">Angiv den Direct Debit-samling, som du vil bogføre betalingskvittering for.</span><span class="sxs-lookup"><span data-stu-id="fb617-117">Specify the direct debit collection that you want to post payment receipt for.</span></span>|  
    |<span data-ttu-id="fb617-118">**Finanskladdetype**</span><span class="sxs-lookup"><span data-stu-id="fb617-118">**General Journal Template**</span></span>|<span data-ttu-id="fb617-119">Angiv, hvilken finanskladdeskabelon der skal bruges til bogføring af betalingskvitteringen, f.eks. skabelonen til indbetalinger.</span><span class="sxs-lookup"><span data-stu-id="fb617-119">Specify which general journal template to use for posting the payment receipt, such as the template for cash receipts.</span></span>|  
    |<span data-ttu-id="fb617-120">**Finanskladdenavn**</span><span class="sxs-lookup"><span data-stu-id="fb617-120">**General Journal Batch Name**</span></span>|<span data-ttu-id="fb617-121">Angiv, hvilket finanskladdenavn der skal bruges til bogføring af betalingskvitteringen.</span><span class="sxs-lookup"><span data-stu-id="fb617-121">Specify which general journal batch to use for posting the payment receipt.</span></span>|  
    |<span data-ttu-id="fb617-122">**Opret kun kladde**</span><span class="sxs-lookup"><span data-stu-id="fb617-122">**Create Journal Only**</span></span>|<span data-ttu-id="fb617-123">Markér dette afkrydsningsfelt, hvis du ikke vil bogføre betalingskvitteringen, når du vælger knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="fb617-123">Select this check box if you do not want to post the payment receipt when you choose the **OK** button.</span></span> <span data-ttu-id="fb617-124">Kvitteringen for betalingen forberedes i den angivne journal og vil ikke blive bogført, før nogen bogfører de pågældende kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="fb617-124">The payment receipt will be prepared in the specified journal and will not be posted until someone posts the journal lines in question.</span></span>|  

5. <span data-ttu-id="fb617-125">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="fb617-125">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fb617-126">Se også</span><span class="sxs-lookup"><span data-stu-id="fb617-126">See Also</span></span>  
 <span data-ttu-id="fb617-127">[Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="fb617-127">[Collect Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
 [<span data-ttu-id="fb617-128">Salg</span><span class="sxs-lookup"><span data-stu-id="fb617-128">Sales</span></span>](sales-manage-sales.md)
