---
title: Bruge kørslen Lav kreditorbetalingsforslag | Microsoft Docs
description: Du kan angive kreditorbetalingsindstillinger for at få vist forslag eller forslag til betalinger, der forfalder snart, eller hvor en rabat er tilgængelig.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 4f146894489cd1292558916068758e4b3c9c15fb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3190247"
---
# <a name="suggest-vendor-payments"></a><span data-ttu-id="e252a-103">Lav forslag</span><span class="sxs-lookup"><span data-stu-id="e252a-103">Suggest Vendor Payments</span></span>
<span data-ttu-id="e252a-104">På siden **Udbetalingskladde** kan du bruge kørslen **Lav kreditorbetalingsforslag** til at foreslå betalingslinjer.</span><span class="sxs-lookup"><span data-stu-id="e252a-104">On the **Payment Journal** page, you can use the **Suggest Vendor Payments** batch job to suggest payment lines.</span></span> <span data-ttu-id="e252a-105">Linjer til betalinger, som snart forfalder, eller betalinger, hvor en kontantrabat er tilgængelig, foreslås baseret på dine indstillinger.</span><span class="sxs-lookup"><span data-stu-id="e252a-105">Lines for payments that are due soon or payments where a payment discount is available are suggested based on your settings.</span></span>

<span data-ttu-id="e252a-106">For at få det fulde udbytte af betalingsforslag skal du først prioritere dine kreditorer.</span><span class="sxs-lookup"><span data-stu-id="e252a-106">To benefit fully from payment suggestions, you must first prioritize your vendors.</span></span> <span data-ttu-id="e252a-107">Du kan finde flere oplysninger i [Tildele kreditorer prioritet](purchasing-how-prioritize-vendors.md).</span><span class="sxs-lookup"><span data-stu-id="e252a-107">For more information, see [Prioritize Vendors](purchasing-how-prioritize-vendors.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="e252a-108">Kreditorposter, der er markeret med **Afvent**, medtages ikke.</span><span class="sxs-lookup"><span data-stu-id="e252a-108">Vendor ledger entries that are **On Hold** are not included in the batch job.</span></span>  

> [!IMPORTANT]  
>   <span data-ttu-id="e252a-109">Hvis du vil have fordel af kontantrabatter og har indtastet et disponibelt beløb, bliver beløbet brugt til:</span><span class="sxs-lookup"><span data-stu-id="e252a-109">If you want to take advantage of payment discounts, and have entered an available amount, the amount will be used for:</span></span>  
    * <span data-ttu-id="e252a-110">Prioriterede forfaldne kreditorposter først i prioriteret rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="e252a-110">Prioritized overdue vendor entries first in order of priority.</span></span>   
    * <span data-ttu-id="e252a-111">Forfaldne kreditorposter, der ikke er prioriteret.</span><span class="sxs-lookup"><span data-stu-id="e252a-111">Overdue vendor entries that are not prioritized.</span></span>  
    * <span data-ttu-id="e252a-112">Åbne kreditorposter, hvor der ydes kontantrabat, arrangeret efter kreditornummer.</span><span class="sxs-lookup"><span data-stu-id="e252a-112">Open vendor entries that qualify for payment discounts, arranged by vendor number.</span></span>  

## <a name="to-use-the-suggest-vendor-payments-function"></a><span data-ttu-id="e252a-113">Sådan bruges funktionen Lav kreditorbetalingsforslag</span><span class="sxs-lookup"><span data-stu-id="e252a-113">To use the Suggest Vendor Payments function</span></span>
1. <span data-ttu-id="e252a-114">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Udbetalingskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="e252a-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e252a-115">Åbn den relevante kladde, og vælg derefter handlingen **Lav kreditorbetalingsforslag**.</span><span class="sxs-lookup"><span data-stu-id="e252a-115">Open the relevant journal, and then choose the **Suggest Vendor Payments** action.</span></span>  
3. <span data-ttu-id="e252a-116">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="e252a-116">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="e252a-117">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="e252a-117">Choose the **OK** button.</span></span>  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a><span data-ttu-id="e252a-118">Sådan indsættes forfaldsdatoen som bogføringsdato på betalingskladdelinjer</span><span class="sxs-lookup"><span data-stu-id="e252a-118">To insert the due date as posting date on payment journal lines</span></span>
<span data-ttu-id="e252a-119">Når du udfører kørslen **Lav kreditorbetalingsforslag** til at oprette betalingslinjer for dine kreditorer, kan du udfylde to særlige felter for at sikre, at de genererede linjer bruger forfaldsdatoen til at beregne bogføringsdatoen.</span><span class="sxs-lookup"><span data-stu-id="e252a-119">When you use the **Suggest Vendor Payments** batch job to create payment lines for your vendors, you can fill two special fields to make sure that the generated lines use the due date to calculate the posting date.</span></span> <span data-ttu-id="e252a-120">Disse felter er **Beregn bogføringsdato fra forfaldsdato for udligningsbilag** og **Forskydning af forfaldsdato for udligningsbilag**.</span><span class="sxs-lookup"><span data-stu-id="e252a-120">These fields are **Calculate Posting Date from Applies-to-Doc Due Date** and **Applies-to-Doc Due Date Offset**.</span></span>  

> [!IMPORTANT]  
>   <span data-ttu-id="e252a-121">Du kan ikke bruge feltet **Beregn bogføringsdato fra forfaldsdato for udligningsbilag** sammen med **Find kontantrabatter** eller feltet **Sammenfat pr. kreditor**.</span><span class="sxs-lookup"><span data-stu-id="e252a-121">You cannot use the **Calculate Posting Date from Applies-to-Doc Due Date** field together with the **Find Payment Discounts** field or the **Summarize per Vendor** field.</span></span> <span data-ttu-id="e252a-122">Hvis bogføringsdatoen er baseret på forfaldsdatoen, beregnes nogle kontantrabatter måske ikke korrekt, da bogføringsdatoen ligger efter kontantrabatdatoen.</span><span class="sxs-lookup"><span data-stu-id="e252a-122">If the posting date is based on the due date, some payment discounts may not calculate correctly because the posting date is after the payment discount date.</span></span>  

<span data-ttu-id="e252a-123">Hvis den beregnede bogføringsdato er i fortiden, bliver bogføringsdatoen desuden flyttet til arbejdsdatoen, og der vises en advarsel.</span><span class="sxs-lookup"><span data-stu-id="e252a-123">Also, if the calculated posting date is in the past, then the posting date is moved up to the work date, and a warning is displayed.</span></span>  

<span data-ttu-id="e252a-124">Du kan manuelt oprette betalingslinjer ved at bruge forfaldsdatoen til at beregne bogføringsdatoen.</span><span class="sxs-lookup"><span data-stu-id="e252a-124">Alternatively, you can manually create payment lines using the due date to calculate the posting date.</span></span> <span data-ttu-id="e252a-125">Når du udligner kreditorposter, kan du bruge handlingen **Beregn bogføringsdato** til at opdatere bogføringsdatoen på kladdelinjen med forfaldsdatoen for den relaterede købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="e252a-125">After you apply vendor ledger entries, you can use the **Calculate Posting Date** action to update the posting date on the journal line with the due date of the related purchase invoice.</span></span> <span data-ttu-id="e252a-126">Du kan finde flere oplysninger i [Udligne købstransaktioner manuelt](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="e252a-126">For more information, see [Apply Purchase Transactions Manually](payables-how-apply-purchase-transactions-manually.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="e252a-127">Hvis købsfakturaen er overskredet, bliver bogføringsdatoen indstillet til arbejdsdatoen, og skrifttypen på linjen bliver rød.</span><span class="sxs-lookup"><span data-stu-id="e252a-127">If the purchase invoice is overdue, the posting date is set to the work date, and the font on the line becomes red.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e252a-128">Se også</span><span class="sxs-lookup"><span data-stu-id="e252a-128">See Also</span></span>
[<span data-ttu-id="e252a-129">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="e252a-129">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="e252a-130">Foretage betaling</span><span class="sxs-lookup"><span data-stu-id="e252a-130">Making Payments</span></span>](payables-make-payments.md)  
[<span data-ttu-id="e252a-131">Arbejde med finanskladder</span><span class="sxs-lookup"><span data-stu-id="e252a-131">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="e252a-132">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e252a-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
