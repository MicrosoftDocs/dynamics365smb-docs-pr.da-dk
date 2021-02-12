---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/20/2021
ms.author: edupont
ms.openlocfilehash: 718845561c1a18701d20b93ebdc8339308ce7ac8
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035777"
---
<span data-ttu-id="be332-101">Når alle varer er indsat på salgsordrelinjerne, kan du beregne fakturarabatten for det samlede salgsdokument ved at vælge Handlinger og derefter vælge **Beregn fakturarabat**.</span><span class="sxs-lookup"><span data-stu-id="be332-101">When all the items have been entered on the sales order lines, you can calculate the invoice discount for the entire sales document by choosing the **Calculate Invoice Discount** action.</span></span>

<span data-ttu-id="be332-102">Hvis feltet **Beregn fakturarabat** er markeret i vinduet **Salgsopsætning**, beregnes fakturarabatten automatisk, når du gør ét af følgende på salgsdokumentet:</span><span class="sxs-lookup"><span data-stu-id="be332-102">If the **Calc. Inv. Discount** field is selected in the **Sales and Receivables Setup** window, then the invoice discount is calculated automatically when you do either of the following on a sales document:</span></span>

* <span data-ttu-id="be332-103">Vis statistik</span><span class="sxs-lookup"><span data-stu-id="be332-103">View statistics</span></span>
* <span data-ttu-id="be332-104">Vis a kontrolrapport</span><span class="sxs-lookup"><span data-stu-id="be332-104">View a test report</span></span>
* <span data-ttu-id="be332-105">Udskriv</span><span class="sxs-lookup"><span data-stu-id="be332-105">Print</span></span>
* <span data-ttu-id="be332-106">Post</span><span class="sxs-lookup"><span data-stu-id="be332-106">Post</span></span>

<span data-ttu-id="be332-107">Rabatten er fordelt på samtlige linjer i salgsdokumentet for de varer, hvor der står **Ja** i feltet **Beregn fakturarabat** på salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="be332-107">The discount is apportioned over all the lines in the sales document for items where the **Allow Invoice Disc.** field on the sales order line contains **Yes**.</span></span> <span data-ttu-id="be332-108">Dette er standardindstillingen for varer.</span><span class="sxs-lookup"><span data-stu-id="be332-108">This is the default setting for items.</span></span>

<span data-ttu-id="be332-109">Fakturarabatbetingelserne defineres på siden **Deb./fakturarabat**, hvor fakturarabatten beregnes.</span><span class="sxs-lookup"><span data-stu-id="be332-109">The invoice discount terms are defined in the **Cust. Invoice Discounts** page to calculate the invoice discount.</span></span> <span data-ttu-id="be332-110">Desuden anvendes valutakoden på salgsdokumentet til at fastsætte fakturarabatbetingelserne i den tilsvarende valuta.</span><span class="sxs-lookup"><span data-stu-id="be332-110">The currency code on the sales document is used to find the invoice discount terms in the corresponding currency.</span></span>

<span data-ttu-id="be332-111">Hvis der ikke er defineret fakturarabatter i udenlandske valutaer, bliver fakturarabatbetingelserne for den relevante valuta, der er defineret i tabellen **Deb./fakt.rabat** med beløbene i den lokale valuta, og kursen pr. bogføringsdatoen på salgsdokumentet bruges automatisk til at beregne fakturarabatten i udenlandsk valuta.</span><span class="sxs-lookup"><span data-stu-id="be332-111">If invoice discounts have not been defined for foreign currencies, then the invoice discount terms defined in the **Cust. Invoice Discounts** page with amounts in your local currency and the exchange rate on the posting date on the sales document are used to calculate the invoice discount in the foreign currency.</span></span>
