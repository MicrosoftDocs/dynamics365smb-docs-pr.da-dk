---
title: FIK-detaljer i betalingsudligningskladden | Microsoft Docs
description: "Feltet Transaktionstekst på siden **Betalingsudligningskladde** viser oplysninger om automatisk udligning af betalinger ved hjælp af den danske FIK-standard."
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
ms.openlocfilehash: 4d4dc86f3238fae185d131da58365bcd42e720c3
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="fik-details-in-the-payment-reconciliation-journal"></a><span data-ttu-id="fd38d-103">FIK-detaljer i betalingsudligningskladden</span><span class="sxs-lookup"><span data-stu-id="fd38d-103">FIK Details in the Payment Reconciliation Journal</span></span>
<span data-ttu-id="fd38d-104">Feltet **Transaktionstekst** på siden **Betalingsudligningskladde** viser oplysninger om automatisk udligning af betalinger ved hjælp af den danske FIK-standard.</span><span class="sxs-lookup"><span data-stu-id="fd38d-104">The **Transaction Text** field on the **Payment Reconciliation Journal** page shows information about the automatic application of payments using the Danish FIK standard.</span></span> <span data-ttu-id="fd38d-105">Du kan finde flere oplysninger i [Afstemme betalinger ved hjælp af automatisk udligning](../../receivables-how-reconcile-payments-auto-application.md).</span><span class="sxs-lookup"><span data-stu-id="fd38d-105">For more information, see [Reconcile Payments Using Automatic Application](../../receivables-how-reconcile-payments-auto-application.md).</span></span>  

 <span data-ttu-id="fd38d-106">I følgende tabel beskrives seks værdier, der kan vises i feltet **Transaktionstekst**.</span><span class="sxs-lookup"><span data-stu-id="fd38d-106">The following table describes the six values that may be shown in the **Transaction Text** field.</span></span>  

|<span data-ttu-id="fd38d-107">Transaktionstekst</span><span class="sxs-lookup"><span data-stu-id="fd38d-107">Transaction Text</span></span>|<span data-ttu-id="fd38d-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="fd38d-108">Description</span></span>|  
|-----------------------------------------|---------------------------------------|  
|<span data-ttu-id="fd38d-109">**Tilsvarende beløb**</span><span class="sxs-lookup"><span data-stu-id="fd38d-109">**Matching Amount**</span></span>|<span data-ttu-id="fd38d-110">Det betalte beløb dækker nøjagtigt det resterende beløb på en ubetalte salgsfaktura, der er identificeret af FIK-nummeret.</span><span class="sxs-lookup"><span data-stu-id="fd38d-110">The amount paid covers exactly the remaining amount on an unpaid sales invoice that is identified by the FIK number.</span></span>|  
|<span data-ttu-id="fd38d-111">**Delvist beløb**</span><span class="sxs-lookup"><span data-stu-id="fd38d-111">**Partial Amount**</span></span>|<span data-ttu-id="fd38d-112">Det betalte beløb er mindre end det resterende beløb på en ubetalte salgsfaktura, der er identificeret af FIK-nummeret.</span><span class="sxs-lookup"><span data-stu-id="fd38d-112">The amount paid is less than the remaining amount on an unpaid sales invoice that is identified by the FIK number.</span></span>|  
|<span data-ttu-id="fd38d-113">**Overskydende beløb**</span><span class="sxs-lookup"><span data-stu-id="fd38d-113">**Excess Amount**</span></span>|<span data-ttu-id="fd38d-114">Det betalte beløb er mere end det resterende beløb på en ubetalte salgsfaktura, der er identificeret af FIK-nummeret.</span><span class="sxs-lookup"><span data-stu-id="fd38d-114">The amount paid is more than the remaining amount on an unpaid sales invoice that is identified by the FIK number.</span></span>|  
|<span data-ttu-id="fd38d-115">**Ingen matchende FIK-kode**</span><span class="sxs-lookup"><span data-stu-id="fd38d-115">**No Matching FIK Number**</span></span>|<span data-ttu-id="fd38d-116">Systemet har ikke fundet nogen skyldige eller betalte salgsfakturaer med et FIK-nummer, der svarer til FIK-nummeret på betalingen.</span><span class="sxs-lookup"><span data-stu-id="fd38d-116">The system has not found any unpaid or paid sales invoices with a FIK number that matches the FIK number on the payment.</span></span>|  
|<span data-ttu-id="fd38d-117">**FIK-dubletnummer**</span><span class="sxs-lookup"><span data-stu-id="fd38d-117">**Duplicate FIK Number**</span></span>|<span data-ttu-id="fd38d-118">Systemet har registreret, at der er betalinger, der har lignende FIK-numre.</span><span class="sxs-lookup"><span data-stu-id="fd38d-118">The system has discovered that there are payments that have similar FIK numbers.</span></span>|  
|<span data-ttu-id="fd38d-119">**Fakturaen er allerede betalt**</span><span class="sxs-lookup"><span data-stu-id="fd38d-119">**Invoice Already Paid**</span></span>|<span data-ttu-id="fd38d-120">Systemet har registreret, at nogle FIK-numre på en betaling svarer til en salgsfaktura, som er fuldt udlignet og lukket.</span><span class="sxs-lookup"><span data-stu-id="fd38d-120">The system has discovered that a FIK number on a payment matches a sales invoice that is fully applied and closed.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="fd38d-121">Se også</span><span class="sxs-lookup"><span data-stu-id="fd38d-121">See Also</span></span>  
[<span data-ttu-id="fd38d-122">Lokal funktionalitet for Danmark</span><span class="sxs-lookup"><span data-stu-id="fd38d-122">Denmark Local Functionality</span></span>](denmark-local-functionality.md)  
[<span data-ttu-id="fd38d-123">Afstemme betalinger ved hjælp af automatisk udligning</span><span class="sxs-lookup"><span data-stu-id="fd38d-123">Reconcile Payments Using Automatic Application</span></span>](../../receivables-how-reconcile-payments-auto-application.md)

