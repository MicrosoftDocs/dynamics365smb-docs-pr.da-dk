---
title: Afregne købsfakturaer omgående
description: Hvis det er nødvendigt at betale kreditoren kontant eller med check, kan du få ordnet bogføringen, når du bogfører fakturaen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: d7962031aa7dda7dafa96ade8e11339c06ebb305
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784588"
---
# <a name="settle-purchase-invoices-promptly"></a><span data-ttu-id="109e3-103">Afregne købsfakturaer omgående</span><span class="sxs-lookup"><span data-stu-id="109e3-103">Settle Purchase Invoices Promptly</span></span>

<span data-ttu-id="109e3-104">Hvis det er nødvendigt at betale kreditoren kontant eller med check, kan du bogføre betalingen, når du bogfører fakturaen.</span><span class="sxs-lookup"><span data-stu-id="109e3-104">If you need to pay the vendor by cash or check, you can post the payment when you post the invoice.</span></span>  

> [!NOTE]  
> <span data-ttu-id="109e3-105">Hvis du ofte afregner købsfakturaer kontant, med check eller bankoverførsel, kan det muligvis svare sig at oprette en specifik betalingsform med en tilknyttet modkonto og angive betalingsformen i feltet **Betalingsform** på kreditorkortet.</span><span class="sxs-lookup"><span data-stu-id="109e3-105">If you frequently pay purchase invoices in cash, check, or bank transfer, it is a good idea to set up a specific payment method with a balancing account and enter this method in the **Payment Method** field on the vendor card.</span></span> <span data-ttu-id="109e3-106">Modkontonummeret indsættes automatisk på fakturahovedet, hver gang du opretter en ny faktura.</span><span class="sxs-lookup"><span data-stu-id="109e3-106">The balancing account number is inserted automatically on the invoice header every time you create a new invoice.</span></span> <span data-ttu-id="109e3-107">Du kan finde flere oplysninger i [Definere betalingsmetoder](finance-payment-methods.md).</span><span class="sxs-lookup"><span data-stu-id="109e3-107">For more information, see [Defining Payment Methods](finance-payment-methods.md).</span></span>  

## <a name="to-settle-purchase-invoices-promptly"></a><span data-ttu-id="109e3-108">Sådan afregnes købsfakturaer omgående</span><span class="sxs-lookup"><span data-stu-id="109e3-108">To settle purchase invoices promptly</span></span>

1. <span data-ttu-id="109e3-109">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="109e3-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="109e3-110">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="109e3-110">Choose the **New** action.</span></span>  
3. <span data-ttu-id="109e3-111">Du kan afregne kontant eller via bankoverførsel ved at angive nummeret på finanskontoen eller bankkontoen i feltet **Modkonto**.</span><span class="sxs-lookup"><span data-stu-id="109e3-111">To pay either in cash or by bank transfer, enter the number of the general ledger cash account or the bank account in the **Bal. Account No.** field.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="109e3-112">Felterne **Modkontotype** og **Modkonto** er ikke med i standardopsætningen for et fakturahoved.</span><span class="sxs-lookup"><span data-stu-id="109e3-112">The **Bal. Account Type** and **Bal. Account No.** fields are not included in the standard layout of the invoice header.</span></span> <span data-ttu-id="109e3-113">Hvis du vil bogføre betalingen af en faktura, skal du kontakte en Microsoft-partner, som kan føje felterne via kode.</span><span class="sxs-lookup"><span data-stu-id="109e3-113">In order to post the payment of an invoice, you must contact a Microsoft partner who can add the fields through code.</span></span>  
>
> <span data-ttu-id="109e3-114">Denne tilpasning er kun nødvendig, hvis du ikke angiver modkonti ved betalingsmetoderne som beskrevet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="109e3-114">This customization is only required if you do not specify balancing accounts on the payment methods as describe above.</span></span>

## <a name="see-also"></a><span data-ttu-id="109e3-115">Se også</span><span class="sxs-lookup"><span data-stu-id="109e3-115">See Also</span></span>

[<span data-ttu-id="109e3-116">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="109e3-116">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="109e3-117">Køb</span><span class="sxs-lookup"><span data-stu-id="109e3-117">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="109e3-118">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="109e3-118">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]