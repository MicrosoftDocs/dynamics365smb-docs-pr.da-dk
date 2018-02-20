---
title: FIK-detaljer i betalingsudligningskladden | Microsoft Docs
description: "Feltet **Transaktionstekst** i vinduet **Betalingsudligningskladde** viser oplysninger om automatisk udligning af betalinger ved hjælp af den danske FIK-standard."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d9481f086d59bf2e496e11570fc9dc0a240e30a1
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="fik-details-in-the-payment-reconciliation-journal"></a><span data-ttu-id="73dd3-103">FIK-detaljer i betalingsudligningskladden</span><span class="sxs-lookup"><span data-stu-id="73dd3-103">FIK Details in the Payment Reconciliation Journal</span></span>
<span data-ttu-id="73dd3-104">Feltet **Transaktionstekst** i vinduet **Betalingsudligningskladde** viser oplysninger om automatisk udligning af betalinger ved hjælp af den danske FIK-standard.</span><span class="sxs-lookup"><span data-stu-id="73dd3-104">The **Transaction Text** field in the **Payment Reconciliation Journal** window shows information about the automatic application of payments using the Danish FIK standard.</span></span> <span data-ttu-id="73dd3-105">Du kan finde flere oplysninger i [Afstemme betalinger ved hjælp af automatisk udligning](../../receivables-how-reconcile-payments-auto-application.md).</span><span class="sxs-lookup"><span data-stu-id="73dd3-105">For more information, see [Reconcile Payments Using Automatic Application](../../receivables-how-reconcile-payments-auto-application.md).</span></span>  

 <span data-ttu-id="73dd3-106">I følgende tabel beskrives seks værdier, der kan vises i feltet **Transaktionstekst**.</span><span class="sxs-lookup"><span data-stu-id="73dd3-106">The following table describes the six values that may be shown in the **Transaction Text** field.</span></span>  

|<span data-ttu-id="73dd3-107">Transaktionstekst</span><span class="sxs-lookup"><span data-stu-id="73dd3-107">Transaction Text</span></span>|<span data-ttu-id="73dd3-108">Description</span><span class="sxs-lookup"><span data-stu-id="73dd3-108">Description</span></span>|  
|-----------------------------------------|---------------------------------------|  
|<span data-ttu-id="73dd3-109">**Tilsvarende beløb**</span><span class="sxs-lookup"><span data-stu-id="73dd3-109">**Matching Amount**</span></span>|<span data-ttu-id="73dd3-110">Det betalte beløb dækker nøjagtigt det resterende beløb på en ubetalte salgsfaktura, der er identificeret af FIK-nummeret.</span><span class="sxs-lookup"><span data-stu-id="73dd3-110">The amount paid covers exactly the remaining amount on an unpaid sales invoice that is identified by the FIK number.</span></span>|  
|<span data-ttu-id="73dd3-111">**Delvist beløb**</span><span class="sxs-lookup"><span data-stu-id="73dd3-111">**Partial Amount**</span></span>|<span data-ttu-id="73dd3-112">Det betalte beløb er mindre end det resterende beløb på en ubetalte salgsfaktura, der er identificeret af FIK-nummeret.</span><span class="sxs-lookup"><span data-stu-id="73dd3-112">The amount paid is less than the remaining amount on an unpaid sales invoice that is identified by the FIK number.</span></span>|  
|<span data-ttu-id="73dd3-113">**Overskydende beløb**</span><span class="sxs-lookup"><span data-stu-id="73dd3-113">**Excess Amount**</span></span>|<span data-ttu-id="73dd3-114">Det betalte beløb er mere end det resterende beløb på en ubetalte salgsfaktura, der er identificeret af FIK-nummeret.</span><span class="sxs-lookup"><span data-stu-id="73dd3-114">The amount paid is more than the remaining amount on an unpaid sales invoice that is identified by the FIK number.</span></span>|  
|<span data-ttu-id="73dd3-115">**Ingen matchende FIK-kode**</span><span class="sxs-lookup"><span data-stu-id="73dd3-115">**No Matching FIK Number**</span></span>|<span data-ttu-id="73dd3-116">Systemet har ikke fundet nogen skyldige eller betalte salgsfakturaer med et FIK-nummer, der svarer til FIK-nummeret på betalingen.</span><span class="sxs-lookup"><span data-stu-id="73dd3-116">The system has not found any unpaid or paid sales invoices with a FIK number that matches the FIK number on the payment.</span></span>|  
|<span data-ttu-id="73dd3-117">**FIK-dubletnummer**</span><span class="sxs-lookup"><span data-stu-id="73dd3-117">**Duplicate FIK Number**</span></span>|<span data-ttu-id="73dd3-118">Systemet har registreret, at der er betalinger, der har lignende FIK-numre.</span><span class="sxs-lookup"><span data-stu-id="73dd3-118">The system has discovered that there are payments that have similar FIK numbers.</span></span>|  
|<span data-ttu-id="73dd3-119">**Fakturaen er allerede betalt**</span><span class="sxs-lookup"><span data-stu-id="73dd3-119">**Invoice Already Paid**</span></span>|<span data-ttu-id="73dd3-120">Systemet har registreret, at nogle FIK-numre på en betaling svarer til en salgsfaktura, som er fuldt udlignet og lukket.</span><span class="sxs-lookup"><span data-stu-id="73dd3-120">The system has discovered that a FIK number on a payment matches a sales invoice that is fully applied and closed.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="73dd3-121">Se også</span><span class="sxs-lookup"><span data-stu-id="73dd3-121">See Also</span></span>  
[<span data-ttu-id="73dd3-122">Lokal funktionalitet for Danmark</span><span class="sxs-lookup"><span data-stu-id="73dd3-122">Denmark Local Functionality</span></span>](denmark-local-functionality.md)  
[<span data-ttu-id="73dd3-123">Afstemme betalinger ved hjælp af automatisk udligning</span><span class="sxs-lookup"><span data-stu-id="73dd3-123">Reconcile Payments Using Automatic Application</span></span>](../../receivables-how-reconcile-payments-auto-application.md)

