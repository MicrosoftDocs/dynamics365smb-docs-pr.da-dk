---
title: Konfigurere betalingsformer | Microsoft Docs
description: Du bruger betalingsformer, for eksempel check, bankoverførsel, kontant eller PayPal, til at definere, hvordan salgs- og købsfakturaer skal betales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 708ae474b15724e151cba367842091763544a434
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182968"
---
# <a name="defining-payment-methods"></a><span data-ttu-id="ff62c-103">Definere betalingsformer</span><span class="sxs-lookup"><span data-stu-id="ff62c-103">Defining Payment Methods</span></span>
<span data-ttu-id="ff62c-104">Betalingsformer definerer, hvordan du foretrækker, at debitorer skal betale dig, og hvordan du foretrækker at betale dine kreditorer.</span><span class="sxs-lookup"><span data-stu-id="ff62c-104">Payment methods define the way you prefer for customers to pay you, and how you like to pay your vendors.</span></span> <span data-ttu-id="ff62c-105">Metoden kan variere for hver debitor eller kreditor.</span><span class="sxs-lookup"><span data-stu-id="ff62c-105">The method can vary for each customer or vendor.</span></span> <span data-ttu-id="ff62c-106">Eksempler på typiske betalingsformer er **bank**, **kontant**, **check** eller **konto**.</span><span class="sxs-lookup"><span data-stu-id="ff62c-106">Examples of typical payment methods are **bank**, **cash**, **check**, or **account**.</span></span>

<span data-ttu-id="ff62c-107">Du kan knytte en betalingsmetode til debitorer og kreditorer, så den samme metode altid bruges på de salgs- og købsdokumenter, du opretter til dem.</span><span class="sxs-lookup"><span data-stu-id="ff62c-107">You can assign a payment method to customers and vendors so that the same method is always used on the sales and purchase documents you create for them.</span></span> <span data-ttu-id="ff62c-108">Du kan om nødvendigt ændre metoden på salgs- eller købsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="ff62c-108">If needed, you can change the method on the sales or purchase document.</span></span> <span data-ttu-id="ff62c-109">F.eks. hvis du vil betale en bestemt købsfaktura kontant og frem for med check.</span><span class="sxs-lookup"><span data-stu-id="ff62c-109">For example, if you want to pay a particular purchase invoice in cash rather than by check.</span></span> <span data-ttu-id="ff62c-110">Dette ændrer ikke den betalingsmetode, der som standard er knyttet til kreditoren.</span><span class="sxs-lookup"><span data-stu-id="ff62c-110">This does not change the default payment method assigned to the vendor.</span></span>

<span data-ttu-id="ff62c-111">De samme betalingsmetoder bruges til salgs- og købsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="ff62c-111">The same payment methods are used for sales and purchase documents.</span></span> <span data-ttu-id="ff62c-112">F.eks. bruges en _kontant_-betalingsmetode både ved indbetalinger, du foretager, og når du modtager betalinger.</span><span class="sxs-lookup"><span data-stu-id="ff62c-112">For example, a _cash_ payment method is used both when you make payments and when you receive them.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="ff62c-113">ved, at når du opretter en salgsfaktura, forventer du at modtage betaling, og det modsatte for købsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="ff62c-113">knows that when you are creating a sales invoice you expect to receive payment, and the opposite for purchase invoices.</span></span>

<span data-ttu-id="ff62c-114">Kreditnotaer for returneringer er dog undtagelser, fordi pengene flyder den modsatte vej, dvs. fra dig til dine kunder og fra din leverandør til dig.</span><span class="sxs-lookup"><span data-stu-id="ff62c-114">Credit memos for returns, however, are exceptions because money is flowing in the opposite directions, from you to your customer and from your vendor to you.</span></span> <span data-ttu-id="ff62c-115">Derfor tildeles der ikke en standardbetalingsmetode til kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="ff62c-115">Therefore, a default payment method is not assigned to credit memos.</span></span> <span data-ttu-id="ff62c-116">Der er dog en løsning, hvis du har angivet betalingsbetingelser for debitoren eller kreditoren.</span><span class="sxs-lookup"><span data-stu-id="ff62c-116">There is, however, a workaround if you have specified terms of payment for the customer or vendor.</span></span> <span data-ttu-id="ff62c-117">Selvom feltet **Beregn kont.rabat på kred.notaer** ikke er beregnet til dette, og du markerer afkrydsningsfeltet på siden **Betalingsbetingelser**, tilføjes en standardbetalingsmetode, når du opretter en kreditnota.</span><span class="sxs-lookup"><span data-stu-id="ff62c-117">Though the **Calc. Pmt. Disc. on Cr. Memos** field is not intended for this, if you choose the check box on the **Payment Terms** page a default payment method will be added when you create a credit memo.</span></span> <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys?rel=0]

## <a name="to-set-up-a-payment-method"></a><span data-ttu-id="ff62c-118">Sådan defineres en betalingsform</span><span class="sxs-lookup"><span data-stu-id="ff62c-118">To set up a payment method</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="ff62c-119">indeholder et par betalingsmetoder, som virksomheder ofte bruger.</span><span class="sxs-lookup"><span data-stu-id="ff62c-119">provides a few payment methods that businesses often use.</span></span> <span data-ttu-id="ff62c-120">Du kan dog tilføje lige så mange, du vil.</span><span class="sxs-lookup"><span data-stu-id="ff62c-120">You can, however, add as many as you need.</span></span>

1. <span data-ttu-id="ff62c-121">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Betalingsformer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ff62c-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="ff62c-122">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="ff62c-122">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a><span data-ttu-id="ff62c-123">Sådan tildeles en betalingsmetode til en debitor eller kreditor</span><span class="sxs-lookup"><span data-stu-id="ff62c-123">To assign a payment method to a customer or vendor</span></span>
1. <span data-ttu-id="ff62c-124">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitor** eller **Kreditor**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ff62c-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer** or **Vendor**, and then choose the related link.</span></span>
2. <span data-ttu-id="ff62c-125">I feltet **Betalingsformkode** skal du vælge metoden, der skal bruges som standard for debitoren eller kreditoren.</span><span class="sxs-lookup"><span data-stu-id="ff62c-125">In the **Payment Method Code** field, choose the method to use by default for the customer or vendor.</span></span>

## <a name="see-also"></a><span data-ttu-id="ff62c-126">Se også</span><span class="sxs-lookup"><span data-stu-id="ff62c-126">See Also</span></span>
[<span data-ttu-id="ff62c-127">Registrere nye debitorer</span><span class="sxs-lookup"><span data-stu-id="ff62c-127">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="ff62c-128">Finans</span><span class="sxs-lookup"><span data-stu-id="ff62c-128">Finance</span></span>](finance.md)  
<span data-ttu-id="ff62c-129">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ff62c-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
