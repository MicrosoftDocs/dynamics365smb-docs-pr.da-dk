---
title: "Sådan samles leverancer | Microsoft Docs"
description: "Hvis du vil fakturere mere end én købsleverance ad gangen, kan du bruge funktionen Saml leverancer."
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
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: c6a6707c9968bca856fda51984283277b27e8e84
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="combine-receipts-on-a-single-invoice"></a><span data-ttu-id="b1b91-103">Kombinere modtagelser på én enkelt faktura</span><span class="sxs-lookup"><span data-stu-id="b1b91-103">Combine Receipts on a Single Invoice</span></span>
<span data-ttu-id="b1b91-104">Hvis du vil fakturere mere end én købsleverance ad gangen, kan du bruge funktionen **Saml leverancer**.</span><span class="sxs-lookup"><span data-stu-id="b1b91-104">If you want to invoice more than one purchase receipt at a time, you can use the **Combine Receipts** function.</span></span>  

<span data-ttu-id="b1b91-105">Inden du kan oprette en samlet købsleverance, skal der være bogført mere end én leverance fra den samme leverandør i den samme valuta.</span><span class="sxs-lookup"><span data-stu-id="b1b91-105">Before you can create a combined purchase receipt, more than one receipt from the same vendor in the same currency must be posted.</span></span> <span data-ttu-id="b1b91-106">Du skal med andre ord have udfyldt to eller flere købsordrer og bogført dem som modtaget, men ikke faktureret.</span><span class="sxs-lookup"><span data-stu-id="b1b91-106">In other words, you must have filled in two or more purchase orders and posted them as received, but not invoiced.</span></span>  

<span data-ttu-id="b1b91-107">Når købsleverancer er samlet på en faktura og bogført, oprettes der en bogført købsfaktura for de fakturerede linjer.</span><span class="sxs-lookup"><span data-stu-id="b1b91-107">When purchase receipts are combined on an invoice and posted, then a posted purchase invoice is created for the invoiced lines.</span></span> <span data-ttu-id="b1b91-108">Feltet **Faktureret (antal)** på den oprindelige købsordre eller rammekøbsordre opdateres på basis af det fakturerede antal.</span><span class="sxs-lookup"><span data-stu-id="b1b91-108">The **Quantity Invoiced** field on the originating purchase order, or blanket purchase order, is updated based on the invoiced quantity.</span></span> <span data-ttu-id="b1b91-109">Dog slettes det oprindelige købsdokument ikke, selvom det er blevet fuldt modtaget og faktureret, og du skal derfor slette købsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="b1b91-109">However, this original purchase document is not deleted, even if it has been fully received and invoiced, and you must therefore delete the purchase document.</span></span>  

## <a name="to-combine-receipts"></a><span data-ttu-id="b1b91-110">Sådan samles leverancer</span><span class="sxs-lookup"><span data-stu-id="b1b91-110">To combine receipts</span></span>  
1. <span data-ttu-id="b1b91-111">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="b1b91-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b1b91-112">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b1b91-112">Choose the **New** action.</span></span> <span data-ttu-id="b1b91-113">Du kan finde flere oplysninger under [Registrere køb](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="b1b91-113">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>  
3. <span data-ttu-id="b1b91-114">I oversigtspanelet **Linjer** skal du vælge handlingen **Hent købsleverancelinjer**.</span><span class="sxs-lookup"><span data-stu-id="b1b91-114">On the **Lines** FastTab, choose the **Get Receipt Lines** action.</span></span>  
4. <span data-ttu-id="b1b91-115">Vælg flere købsleverancelinjer, der skal indgå i fakturaen.</span><span class="sxs-lookup"><span data-stu-id="b1b91-115">Select multiple receipt lines that you want to include in the invoice.</span></span>  

    <span data-ttu-id="b1b91-116">Hvis du har valgt en forkert leverancelinje, eller hvis du vil begynde forfra, kan du bare slette linjerne på købsfakturaen og derefter bruge funktionen **Hent købsleverancelinjer** igen.</span><span class="sxs-lookup"><span data-stu-id="b1b91-116">If an incorrect receipt line was selected or you want to start over, you can just delete the lines on the purchase invoice and then use the **Get Receipt Lines** function again.</span></span>  
5. <span data-ttu-id="b1b91-117">Vælg handlingen **Bogfør** for at fakturere kladden.</span><span class="sxs-lookup"><span data-stu-id="b1b91-117">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a><span data-ttu-id="b1b91-118">Sådan fjernes åbne købsordrer efter bogføring af kombineret modtagelse</span><span class="sxs-lookup"><span data-stu-id="b1b91-118">To remove open purchase orders after combined receipt posting</span></span>  
1. <span data-ttu-id="b1b91-119">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Slet fakturerede købsordrer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="b1b91-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Purchase Orders**, and select the related link.</span></span>  
2. <span data-ttu-id="b1b91-120">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="b1b91-120">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="b1b91-121">.</span><span class="sxs-lookup"><span data-stu-id="b1b91-121">.</span></span>
3. <span data-ttu-id="b1b91-122">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1b91-122">Choose the **OK** button.</span></span>  

<span data-ttu-id="b1b91-123">Du kan også slette de individuelle ordrer manuelt.</span><span class="sxs-lookup"><span data-stu-id="b1b91-123">Alternatively, delete the individual orders manually.</span></span>

<span data-ttu-id="b1b91-124">Gentag trin 1 til 3 for eventuelle andre berørte dokumenter, f.eks. rammekøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="b1b91-124">Repeat steps 1 through 3 for any other affected documents, such as blanket purchase orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1b91-125">Se også</span><span class="sxs-lookup"><span data-stu-id="b1b91-125">See Also</span></span>  
[<span data-ttu-id="b1b91-126">Køb</span><span class="sxs-lookup"><span data-stu-id="b1b91-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="b1b91-127">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b1b91-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

