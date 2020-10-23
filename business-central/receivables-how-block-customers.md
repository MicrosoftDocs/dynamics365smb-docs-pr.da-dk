---
title: Sådan spærrer du salg til kunder
description: Hvis det er nødvendigt, kan du spærre en kunde, så kunden ikke kan medtages i salgsdokumenter og andre salgstransaktioner.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: dc8014cf0896db1ebbc5f0c5ea22e0f160c1b06d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3926543"
---
# <a name="block-customers"></a><span data-ttu-id="95478-103">Blokere debitorer</span><span class="sxs-lookup"><span data-stu-id="95478-103">Block Customers</span></span>
<span data-ttu-id="95478-104">Du kan spærre en debitor, for eksempel på grund af insolvens, så kunden ikke kan føjes til salgsdokumenter, eller ingen transaktioner kan bogføres for debitoren.</span><span class="sxs-lookup"><span data-stu-id="95478-104">You can block a customer, for example because of insolvency, so that the customer cannot be added to sales documents or so that no transactions can be posted for the customer.</span></span>

<span data-ttu-id="95478-105">Foruden at blokere for en debitor kan du sætte tilgodehavendetransaktioner for kunden på hold i forbindelse med rykkere.</span><span class="sxs-lookup"><span data-stu-id="95478-105">In addition to blocking a customer, you can set receivable transactions for the customer to be on hold in connection with reminders.</span></span> <span data-ttu-id="95478-106">Du kan finde flere oplysninger under [Indhente udestående beløb](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="95478-106">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>   

<span data-ttu-id="95478-107">Den følgende tabel beskriver indstillingerne for spærring af kunder.</span><span class="sxs-lookup"><span data-stu-id="95478-107">The following table describes the options for blocking customers.</span></span>  

|<span data-ttu-id="95478-108">Indstilling</span><span class="sxs-lookup"><span data-stu-id="95478-108">Option</span></span>|<span data-ttu-id="95478-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="95478-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="95478-110">**Tomt**</span><span class="sxs-lookup"><span data-stu-id="95478-110">**Blank**</span></span>|<span data-ttu-id="95478-111">Transaktioner er tilladt for kunden.</span><span class="sxs-lookup"><span data-stu-id="95478-111">Transactions are allowed for this customer.</span></span>|
|<span data-ttu-id="95478-112">**Lever**</span><span class="sxs-lookup"><span data-stu-id="95478-112">**Ship**</span></span>|<span data-ttu-id="95478-113">Der kan ikke oprettes nye ordrer og nye leverancer til kunden.</span><span class="sxs-lookup"><span data-stu-id="95478-113">New orders and new shipments cannot be created for this customer.</span></span> <span data-ttu-id="95478-114">Eksisterende leverancer, der ikke er faktureret, kan faktureres.</span><span class="sxs-lookup"><span data-stu-id="95478-114">Existing shipments not yet invoiced can be invoiced.</span></span>|  
|<span data-ttu-id="95478-115">**Faktura**</span><span class="sxs-lookup"><span data-stu-id="95478-115">**Invoice**</span></span>|<span data-ttu-id="95478-116">Der kan ikke oprettes nye ordrer, nye leverancer og nye fakturaer til kunden.</span><span class="sxs-lookup"><span data-stu-id="95478-116">New orders, new shipments, and new invoices cannot be created for this customer.</span></span> <span data-ttu-id="95478-117">Eksisterende leverancer, der ikke er faktureret, kan ikke faktureres.</span><span class="sxs-lookup"><span data-stu-id="95478-117">Existing shipments not yet invoiced cannot be invoiced.</span></span> <span data-ttu-id="95478-118">Du kan stadig sende rykkere og rentenotaer til kunden.</span><span class="sxs-lookup"><span data-stu-id="95478-118">You can still send reminders and finance charge memos to the customer.</span></span>|  
|<span data-ttu-id="95478-119">**Alle**</span><span class="sxs-lookup"><span data-stu-id="95478-119">**All**</span></span>|<span data-ttu-id="95478-120">Ingen transaktioner er tilladt for kunden – heller ikke indbetalinger.</span><span class="sxs-lookup"><span data-stu-id="95478-120">No transaction is allowed for this customer, including payments.</span></span>|  

## <a name="to-block-a-customer"></a><span data-ttu-id="95478-121">Sådan blokeres en kunde</span><span class="sxs-lookup"><span data-stu-id="95478-121">To block a customer</span></span>  
1. <span data-ttu-id="95478-122">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="95478-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="95478-123">Vælg en kunde, og vælg derefter handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="95478-123">Select a customer, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="95478-124">I feltet **Spærret** skal du vælge, hvad der skal spærres, som beskrevet i tabellen ovenfor.</span><span class="sxs-lookup"><span data-stu-id="95478-124">In the **Blocked** field, choose what to block, as described in the table above.</span></span>

## <a name="see-also"></a><span data-ttu-id="95478-125">Se også</span><span class="sxs-lookup"><span data-stu-id="95478-125">See Also</span></span>  
[<span data-ttu-id="95478-126">Registrere nye debitorer</span><span class="sxs-lookup"><span data-stu-id="95478-126">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="95478-127">Indhente udestående beløb</span><span class="sxs-lookup"><span data-stu-id="95478-127">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="95478-128">Administrere tilgodehavender</span><span class="sxs-lookup"><span data-stu-id="95478-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
