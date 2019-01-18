---
title: "Sådan rettes forudbetalinger | Microsoft Docs"
description: "Du kan foretage en rettelse af en ordre, efter at du har bogført en forudbetalingsfaktura for den. Du kan indsætte nye linjer i ordren, efter at der er udstedt en forudbetaling, og derefter kan du bogføre en anden forudbetalingsfaktura, men du kan ikke slette en linje fra en ordre, hvis der allerede er faktureret en forudbetaling for linjen."
services: project-madeira
documentationcenter: 
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
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: b19b86b3d5168ee6fa053141af4022f5040743cb
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="correct-prepayments"></a><span data-ttu-id="54ef5-104">Rette forudbetalinger</span><span class="sxs-lookup"><span data-stu-id="54ef5-104">Correct Prepayments</span></span>
<span data-ttu-id="54ef5-105">Du kan foretage en rettelse af en ordre, efter at du har bogført en forudbetalingsfaktura for den.</span><span class="sxs-lookup"><span data-stu-id="54ef5-105">You can make a correction to an order after you have posted a prepayment invoice for the order.</span></span> <span data-ttu-id="54ef5-106">Du kan indsætte nye linjer i ordren, efter at der er udstedt en forudbetaling, og derefter kan du bogføre en anden forudbetalingsfaktura, men du kan ikke slette en linje fra en ordre, hvis der allerede er faktureret en forudbetaling for linjen.</span><span class="sxs-lookup"><span data-stu-id="54ef5-106">You can add new lines to an order after issuing a prepayment, and then you can post another prepayment invoice, but you cannot delete a line from an order after a prepayment has been invoiced for the line.</span></span>  

## <a name="to-correct-a-prepayment"></a><span data-ttu-id="54ef5-107">Sådan rettes en forudbetaling</span><span class="sxs-lookup"><span data-stu-id="54ef5-107">To correct a prepayment</span></span>
<span data-ttu-id="54ef5-108">Følgende procedure viser, hvordan du kan udstede en forudbetalingskreditnota for at annullere alle fakturerede forudbetalinger for en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="54ef5-108">The following procedure shows how to issue a prepayment credit memo to cancel all invoiced prepayments for a sales order.</span></span>  
1. <span data-ttu-id="54ef5-109">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="54ef5-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="54ef5-110">Åbn den relevante Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="54ef5-110">Open the relevant sales order.</span></span>
3. <span data-ttu-id="54ef5-111">Vælg handlingen **Forudbetaling**, og vælg derefter handlingen **Forudbetalingskreditnota** eller handlingen **Bogfør og udskriv forudbetalingskreditnota**.</span><span class="sxs-lookup"><span data-stu-id="54ef5-111">Choose the **Prepayment** action, and then choose the **Post Prepayment Credit Memo** action or the **Post and Print Prepmt. Cr. Memo** action.</span></span>  
4. <span data-ttu-id="54ef5-112">På siden **Salgskreditnota** skal du fortsætte med at løse de relevante poster som for en salgskreditnota.</span><span class="sxs-lookup"><span data-stu-id="54ef5-112">On the **Sales Credit Memo** page, proceed to correct the relevant entries, as for any sales credit memo.</span></span> <span data-ttu-id="54ef5-113">Du kan finde flere oplysninger i [Behandle salgsreturvarer eller annulleringer](sales-how-process-sales-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="54ef5-113">For more information, see [Process Sales Returns or Cancellations](sales-how-process-sales-returns-cancellations.md).</span></span>     

    > [!NOTE]  
    > <span data-ttu-id="54ef5-114">For at reducere beløbet i feltet **Linjebeløb** skal du først øge forudbetalingsprocenten på linjen, så værdien i feltet **Linjebeløb for forudbetaling** ikke bliver mindre end værdien i feltet **Forudbetalt beløb faktureret**.</span><span class="sxs-lookup"><span data-stu-id="54ef5-114">To Reduce the amount in the **Line Amount** field, you must first increase the prepayment percentage on the line so that the value in the **Prepmt. Line Amount** field is not decreased below the value in the **Prepmt. Amt. Inv.** field.</span></span>

5. <span data-ttu-id="54ef5-115">Du kan oprette en forudbetalingsfaktura for en hvilken som helst ny linje i salgskreditnotaen ved at vælge handlingen **Forudbetaling** og derefter vælge handlingen **Bogfør forudbetalingsfaktura** eller handlingen **Bogfør og udskriv forudbetalingsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="54ef5-115">To make a prepayment invoice for any new lines in the sales credit memo, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action or the **Post and Print Prepmt. Invoice** action.</span></span>  
6. <span data-ttu-id="54ef5-116">Hvis du vil udstede en ekstra forudbetalingsfaktura, skal du øge forudbetalingsbeløbet på en eller flere linjer og bogføre forudbetalingsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="54ef5-116">To issue an additional prepayment invoice, increase the prepayment amount on one or more lines and post the prepayment invoice.</span></span> <span data-ttu-id="54ef5-117">Der oprettes en ny faktura, som dækker differencen mellem de forudbetalte beløb, der er faktureret indtil videre, og det nye forudbetalingsbeløbene.</span><span class="sxs-lookup"><span data-stu-id="54ef5-117">A new invoice will be created for the difference between the prepayment amounts invoiced and the new prepayment amounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="54ef5-118">Se også</span><span class="sxs-lookup"><span data-stu-id="54ef5-118">See Also</span></span>  
[<span data-ttu-id="54ef5-119">Fakturere forudbetalinger</span><span class="sxs-lookup"><span data-stu-id="54ef5-119">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="54ef5-120">Gennemgang: Opsætning og fakturering af salgsforudbetalinger</span><span class="sxs-lookup"><span data-stu-id="54ef5-120">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="54ef5-121">Finans</span><span class="sxs-lookup"><span data-stu-id="54ef5-121">Finance</span></span>](finance.md)  
<span data-ttu-id="54ef5-122">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="54ef5-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

