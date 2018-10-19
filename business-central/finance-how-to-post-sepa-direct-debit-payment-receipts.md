---
title: "Bogføre SEPA Direct Debit-betalinger | Microsoft Docs"
description: "Når en Direct Debit-opkrævning er behandlet af din bank, kan du fortsætte med at bogføre kvittering for betaling for de involverede salgsfakturaer."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: ee07ca7ba498858fac794f1ee1f27f281de8ae02
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="post-sepa-direct-debit-payment-receipts"></a><span data-ttu-id="89343-103">Bogføre SEPA Direct Debit-betalingskvitteringer</span><span class="sxs-lookup"><span data-stu-id="89343-103">Post SEPA Direct Debit Payment Receipts</span></span>
<span data-ttu-id="89343-104">Når en Direct Debit-opkrævning er behandlet af din bank, kan du fortsætte med at bogføre kvittering for betaling for de involverede salgsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="89343-104">When a direct debit collection is successfully processed by your bank, you can proceed to post receipt of the payment for the involved sales invoices.</span></span> <span data-ttu-id="89343-105">Du kan finde flere oplysninger i [Oprette poster i SEPA Direct Debit-opkrævning og eksportere til en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="89343-105">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  

<span data-ttu-id="89343-106">Du kan bogføre betalingskvitteringen direkte fra vinduet **Direct Debit-opkrævninger** eller vinduet **Poster i Direct Debit-opkrævning**.</span><span class="sxs-lookup"><span data-stu-id="89343-106">You can post the payment receipt directly from the **Direct Debit Collections** window or the **Direct Debit Collect. Entries** window.</span></span> <span data-ttu-id="89343-107">Alternativt kan du overføre arbejdet til en anden bruger ved at udarbejde de relaterede kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="89343-107">Alternatively, you can relay the work to another user by preparing the related journal lines.</span></span>  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-window"></a><span data-ttu-id="89343-108">Sådan bogføres en betalingskvittering i Direct Debit fra vinduet Direct Debit-opkrævninger</span><span class="sxs-lookup"><span data-stu-id="89343-108">To post a direct-debit payment receipt from the Direct Debit Collections window</span></span>  
1. <span data-ttu-id="89343-109">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Direct Debit-opkrævninger**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="89343-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Direct Debit Collections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="89343-110">Vælg en linje for en Direct Debit-opkrævning, der er eksporteret til en bankfil og er blevet behandlet af banken.</span><span class="sxs-lookup"><span data-stu-id="89343-110">Select a line for a direct debit collection that has been exported to a bank file and successfully processed by the bank.</span></span> <span data-ttu-id="89343-111">Du kan finde flere oplysninger i [Oprette poster i SEPA Direct Debit-opkrævning og eksportere til en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="89343-111">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  
3. <span data-ttu-id="89343-112">Vælg handlingen **Bogfør betalingskvitteringer**.</span><span class="sxs-lookup"><span data-stu-id="89343-112">Choose the **Post Payment Receipts** action.</span></span>  
4. <span data-ttu-id="89343-113">I vinduet **Bogfør Direct Debit-opkrævning** skal du udfylde felterne som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="89343-113">In the **Post Direct Debit Collection** window, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="89343-114">Felt</span><span class="sxs-lookup"><span data-stu-id="89343-114">Field</span></span>|<span data-ttu-id="89343-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="89343-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="89343-116">**Direct Debit-opkrævningsnr.**</span><span class="sxs-lookup"><span data-stu-id="89343-116">**Direct Debit Collection No.**</span></span>|<span data-ttu-id="89343-117">Angiv den Direct Debit-samling, som du vil bogføre betalingskvittering for.</span><span class="sxs-lookup"><span data-stu-id="89343-117">Specify the direct debit collection that you want to post payment receipt for.</span></span>|  
    |<span data-ttu-id="89343-118">**Finanskladdetype**</span><span class="sxs-lookup"><span data-stu-id="89343-118">**General Journal Template**</span></span>|<span data-ttu-id="89343-119">Angiv, hvilken finanskladdeskabelon der skal bruges til bogføring af betalingskvitteringen, f.eks. skabelonen til indbetalinger.</span><span class="sxs-lookup"><span data-stu-id="89343-119">Specify which general journal template to use for posting the payment receipt, such as the template for cash receipts.</span></span>|  
    |<span data-ttu-id="89343-120">**Finanskladdenavn**</span><span class="sxs-lookup"><span data-stu-id="89343-120">**General Journal Batch Name**</span></span>|<span data-ttu-id="89343-121">Angiv, hvilket finanskladdenavn der skal bruges til bogføring af betalingskvitteringen.</span><span class="sxs-lookup"><span data-stu-id="89343-121">Specify which general journal batch to use for posting the payment receipt.</span></span>|  
    |<span data-ttu-id="89343-122">**Opret kun kladde**</span><span class="sxs-lookup"><span data-stu-id="89343-122">**Create Journal Only**</span></span>|<span data-ttu-id="89343-123">Markér dette afkrydsningsfelt, hvis du ikke vil bogføre betalingskvitteringen, når du vælger knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="89343-123">Select this check box if you do not want to post the payment receipt when you choose the **OK** button.</span></span> <span data-ttu-id="89343-124">Kvitteringen for betalingen forberedes i den angivne journal og vil ikke blive bogført, før nogen bogfører de pågældende kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="89343-124">The payment receipt will be prepared in the specified journal and will not be posted until someone posts the journal lines in question.</span></span>|  

5. <span data-ttu-id="89343-125">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="89343-125">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="89343-126">Se også</span><span class="sxs-lookup"><span data-stu-id="89343-126">See Also</span></span>  
 <span data-ttu-id="89343-127">[Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="89343-127">[Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
 [<span data-ttu-id="89343-128">Salg</span><span class="sxs-lookup"><span data-stu-id="89343-128">Sales</span></span>](sales-manage-sales.md)

