---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/25/2021
ms.author: edupont
ms.openlocfilehash: 539ee2eb2c9e4a71eacfb78d95320870128fb1d9
ms.sourcegitcommit: cb06aa973f5c767df774b0e1e199c6fbe0e85b88
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470283"
---
<span data-ttu-id="61d6e-101">Når alle varer er indsat på salgslinjerne, kan du beregne fakturarabatten for det samlede dokument ved at vælge Handlinger og derefter vælge **Beregn fakturarabat**.</span><span class="sxs-lookup"><span data-stu-id="61d6e-101">When all the items have been entered on the sales lines, you can calculate the invoice discount for the entire document by choosing the **Calculate Invoice Discount** action.</span></span>

<span data-ttu-id="61d6e-102">Rabatten er beregnet baseret på samtlige linjer i salgsdokumentet for de varer, hvor der står **Ja** i feltet **Beregn fakturarabat** på salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="61d6e-102">The discount is calculated based on all the lines in the sales document for items where the **Allow Invoice Disc.** field on the sales order line contains **Yes**.</span></span> <span data-ttu-id="61d6e-103">Dette er standardindstillingen for varer.</span><span class="sxs-lookup"><span data-stu-id="61d6e-103">This is the default setting for items.</span></span> <span data-ttu-id="61d6e-104">Linjer med varegebyrer er f. eks. ikke medtaget i beregningen af fakturarabatten.</span><span class="sxs-lookup"><span data-stu-id="61d6e-104">Lines with item charges, for example, are not included in the calculation of the invoice discount.</span></span> <span data-ttu-id="61d6e-105">Hvis du vil anvende en rabat på disse linjer, skal du angive feltet **Linjerabat i %** på de relevante linjer.</span><span class="sxs-lookup"><span data-stu-id="61d6e-105">If you want to apply a discount to such lines, you must set the **Line Discount %** field on the relevant lines.</span></span>  

> [!TIP]
> <span data-ttu-id="61d6e-106">Hvis feltet **Beregn fakturarabat** er markeret i vinduet **Salgsopsætning**, beregnes fakturarabatten automatisk, når du gør ét af følgende på salgsdokumentet:</span><span class="sxs-lookup"><span data-stu-id="61d6e-106">If the **Calc. Inv. Discount** field is selected in the **Sales and Receivables Setup** page, then the invoice discount is calculated automatically when you do either of the following on a sales document:</span></span>
>
> * <span data-ttu-id="61d6e-107">Vis statistik</span><span class="sxs-lookup"><span data-stu-id="61d6e-107">View statistics</span></span>
> * <span data-ttu-id="61d6e-108">Vis a kontrolrapport</span><span class="sxs-lookup"><span data-stu-id="61d6e-108">View a test report</span></span>
> * <span data-ttu-id="61d6e-109">Udskriv</span><span class="sxs-lookup"><span data-stu-id="61d6e-109">Print</span></span>
> * <span data-ttu-id="61d6e-110">Post</span><span class="sxs-lookup"><span data-stu-id="61d6e-110">Post</span></span>

<span data-ttu-id="61d6e-111">Fakturarabatbetingelserne for en debitor defineres på siden **Deb./fakturarabat** for debitoren.</span><span class="sxs-lookup"><span data-stu-id="61d6e-111">The invoice discount terms for a customer are defined in the **Cust. Invoice Discounts** page for the customer.</span></span> <span data-ttu-id="61d6e-112">Desuden anvendes valutakoden på salgsdokumentet til at fastsætte fakturarabatbetingelserne i den tilsvarende valuta.</span><span class="sxs-lookup"><span data-stu-id="61d6e-112">The currency code on the sales document is used to find the invoice discount terms in the corresponding currency.</span></span>

<span data-ttu-id="61d6e-113">Hvis der ikke er defineret fakturarabatter i udenlandske valutaer, bliver fakturarabatbetingelserne for den relevante valuta, der er defineret i tabellen **Deb./fakt.rabat** med beløbene i den lokale valuta, og kursen pr. bogføringsdatoen på salgsdokumentet bruges automatisk til at beregne fakturarabatten i udenlandsk valuta.</span><span class="sxs-lookup"><span data-stu-id="61d6e-113">If invoice discounts have not been defined for foreign currencies, then the invoice discount terms defined in the **Cust. Invoice Discounts** page with amounts in your local currency and the exchange rate on the posting date on the sales document are used to calculate the invoice discount in the foreign currency.</span></span>
