---
title: "Sådan rettes forudbetalinger | Microsoft Docs"
description: "Du kan foretage en rettelse af en ordre, efter at du har bogført en forudbetalingsfaktura for den. Du kan indsætte nye linjer i ordren, efter at der er udstedt en forudbetaling, og derefter kan du bogføre en anden forudbetalingsfaktura, men du kan ikke slette en linje fra en ordre, hvis der allerede er faktureret en forudbetaling for linjen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b51fba1ee8c9a040836ac24c51f39a036f3c0e23
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-correct-prepayments"></a><span data-ttu-id="5f30c-104">Sådan rettes forudbetalinger</span><span class="sxs-lookup"><span data-stu-id="5f30c-104">How to: Correct Prepayments</span></span>
<span data-ttu-id="5f30c-105">Du kan foretage en rettelse af en ordre, efter at du har bogført en forudbetalingsfaktura for den.</span><span class="sxs-lookup"><span data-stu-id="5f30c-105">You can make a correction to an order after you have posted a prepayment invoice for the order.</span></span> <span data-ttu-id="5f30c-106">Du kan indsætte nye linjer i ordren, efter at der er udstedt en forudbetaling, og derefter kan du bogføre en anden forudbetalingsfaktura, men du kan ikke slette en linje fra en ordre, hvis der allerede er faktureret en forudbetaling for linjen.</span><span class="sxs-lookup"><span data-stu-id="5f30c-106">You can add new lines to an order after issuing a prepayment, and then you can post another prepayment invoice, but you cannot delete a line from an order after a prepayment has been invoiced for the line.</span></span>  

## <a name="to-correct-a-prepayment"></a><span data-ttu-id="5f30c-107">Sådan rettes en forudbetaling</span><span class="sxs-lookup"><span data-stu-id="5f30c-107">To correct a prepayment</span></span>
<span data-ttu-id="5f30c-108">Følgende procedure viser, hvordan du kan udstede en forudbetalingskreditnota for at annullere alle fakturerede forudbetalinger for en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="5f30c-108">The following procedure shows how to issue a prepayment credit memo to cancel all invoiced prepayments for a sales order.</span></span>  
1. <span data-ttu-id="5f30c-109">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="5f30c-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="5f30c-110">Åbn den relevante Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="5f30c-110">Open the relevant sales order.</span></span>
3. <span data-ttu-id="5f30c-111">Vælg handlingen **Forudbetaling**, og vælg derefter handlingen **Forudbetalingskreditnota** eller handlingen **Bogfør og udskriv forudbetalingskreditnota**.</span><span class="sxs-lookup"><span data-stu-id="5f30c-111">Choose the **Prepayment** action, and then choose the **Post Prepayment Credit Memo** action or the **Post and Print Prepmt. Cr. Memo** action.</span></span>  
4. <span data-ttu-id="5f30c-112">I vinduet **Salgskreditnota** skal du fortsætte med at løse de relevante poster som for en salgskreditnota.</span><span class="sxs-lookup"><span data-stu-id="5f30c-112">In the **Sales Credit Memo** window, proceed to correct the relevant entries, as for any sales credit memo.</span></span> <span data-ttu-id="5f30c-113">Du kan finde flere oplysninger i [Fremgangsmåde: Behandle salgsreturvarer eller annulleringer](sales-how-process-sales-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="5f30c-113">For more information, see [How to: Process Sales Returns or Cancellations](sales-how-process-sales-returns-cancellations.md).</span></span>     

    > [!NOTE]  
    > <span data-ttu-id="5f30c-114">For at reducere beløbet i feltet **Linjebeløb** skal du først øge forudbetalingsprocenten på linjen, så værdien i feltet **Linjebeløb for forudbetaling** ikke bliver mindre end værdien i feltet **Forudbetalt beløb faktureret**.</span><span class="sxs-lookup"><span data-stu-id="5f30c-114">To Reduce the amount in the **Line Amount** field, you must first increase the prepayment percentage on the line so that the value in the **Prepmt. Line Amount** field is not decreased below the value in the **Prepmt. Amt. Inv.** field.</span></span>

5. <span data-ttu-id="5f30c-115">Du kan oprette en forudbetalingsfaktura for en hvilken som helst ny linje i salgskreditnotaen ved at vælge handlingen **Forudbetaling** og derefter vælge handlingen **Bogfør forudbetalingsfaktura** eller handlingen **Bogfør og udskriv forudbetalingsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="5f30c-115">To make a prepayment invoice for any new lines in the sales credit memo, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action or the **Post and Print Prepmt. Invoice** action.</span></span>  
6. <span data-ttu-id="5f30c-116">Hvis du vil udstede en ekstra forudbetalingsfaktura, skal du øge forudbetalingsbeløbet på en eller flere linjer og bogføre forudbetalingsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="5f30c-116">To issue an additional prepayment invoice, increase the prepayment amount on one or more lines and post the prepayment invoice.</span></span> <span data-ttu-id="5f30c-117">Der oprettes en ny faktura, som dækker differencen mellem de forudbetalte beløb, der er faktureret indtil videre, og det nye forudbetalingsbeløbene.</span><span class="sxs-lookup"><span data-stu-id="5f30c-117">A new invoice will be created for the difference between the prepayment amounts invoiced and the new prepayment amounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5f30c-118">Se også</span><span class="sxs-lookup"><span data-stu-id="5f30c-118">See Also</span></span>  
[<span data-ttu-id="5f30c-119">Fakturere forudbetalinger</span><span class="sxs-lookup"><span data-stu-id="5f30c-119">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="5f30c-120">Gennemgang: Opsætning og fakturering af salgsforudbetalinger</span><span class="sxs-lookup"><span data-stu-id="5f30c-120">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="5f30c-121">Finans</span><span class="sxs-lookup"><span data-stu-id="5f30c-121">Finance</span></span>](finance.md)  
<span data-ttu-id="5f30c-122">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5f30c-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
